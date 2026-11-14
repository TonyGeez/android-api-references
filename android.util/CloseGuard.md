# CloseGuard

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CloseGuard

Kotlin| [Java](https://developer.android.com/reference/android/util/CloseGuard "View this page in Java") 
| --- | --- |

```
class CloseGuard
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.util.CloseGuard](https://developer.android.com/reference/kotlin/android/util/CloseGuard#) |

CloseGuard is a mechanism for flagging implicit finalizer cleanup of resources that should have been cleaned up by explicit close methods (aka "explicit termination methods" in Effective Java).

A simple example: 

```kotlin
<code>class Foo {
 
        private final CloseGuard guard = new CloseGuard();
 
        ...
 
        public Foo() {
            ...;
            guard.open("cleanup");
        }
 
        public void cleanup() {
           guard.close();
           ...;
           if (Build.VERSION.SDK_INT &gt;= 28) {
               Reference.reachabilityFence(this);
           }
           // For full correctness in the absence of a close() call, other methods may also need
           // reachabilityFence() calls.
        }
 
        protected void finalize() throws Throwable {
            try {
                // Note that guard could be null if the constructor threw.
                if (guard != null) {
                    guard.warnIfOpen();
                }
                cleanup();
            } finally {
                super.finalize();
            }
        }
    }
  </code>
```
In usage where the resource to be explicitly cleaned up is allocated after object construction, CloseGuard protection can be deferred. For example: 

```kotlin
<code>class Bar {
 
        private final CloseGuard guard = new CloseGuard();
 
        ...
 
        public Bar() {
            ...;
        }
 
        public void connect() {
           ...;
           guard.open("cleanup");
        }
 
        public void cleanup() {
           guard.close();
           ...;
           if (Build.VERSION.SDK_INT &gt;= 28) {
               Reference.reachabilityFence(this);
           }
           // For full correctness in the absence of a close() call, other methods may also need
           // reachabilityFence() calls.
        }
 
        protected void finalize() throws Throwable {
            try {
                // Note that guard could be null if the constructor threw.
                if (guard != null) {
                    guard.warnIfOpen();
                }
                cleanup();
            } finally {
                super.finalize();
            }
        }
    }
  </code>
```
When used in a constructor, calls to`open`should occur at the end of the constructor since an exception that would cause abrupt termination of the constructor will mean that the user will not have a reference to the object to cleanup explicitly. When used in a method, the call to`open`should occur just after resource acquisition.

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------|---|
| [CloseGuard](https://developer.android.com/reference/kotlin/android/util/CloseGuard#CloseGuard())`()` Constructs a new CloseGuard instance. |

| Public methods ||
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](https://developer.android.com/reference/kotlin/android/util/CloseGuard#close())`()` Marks this CloseGuard instance as closed to avoid warnings on finalization. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [open](https://developer.android.com/reference/kotlin/android/util/CloseGuard#open(kotlin.String))`(`closeMethodName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Initializes the instance with a warning that the caller should have explicitly called the`closeMethodName`method instead of relying on finalization. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [warnIfOpen](https://developer.android.com/reference/kotlin/android/util/CloseGuard#warnIfOpen())`()` Logs a warning if the caller did not properly cleanup by calling an explicit close method before finalization. |
| --- | --- |

## Public constructors

### CloseGuard

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
CloseGuard()
```

Constructs a new CloseGuard instance. [open(java.lang.String)](https://developer.android.com/reference/kotlin/android/util/CloseGuard#open(kotlin.String))can be used to set up the instance to warn on failure to close.

## Public methods

### close

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun close(): Unit
```

Marks this CloseGuard instance as closed to avoid warnings on finalization. 

### open

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun open(closeMethodName: String): Unit
```

Initializes the instance with a warning that the caller should have explicitly called the`closeMethodName`method instead of relying on finalization.

| Parameters ||
|-------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| `closeMethodName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):non-null name of explicit termination method. Printed by warnIfOpen. |

| Exceptions ||
|----------------------------------|-----------------------------|
| `java.lang.NullPointerException` | if closeMethodName is null. |

### warnIfOpen

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun warnIfOpen(): Unit
```

Logs a warning if the caller did not properly cleanup by calling an explicit close method before finalization.
