# ConditionVariable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ConditionVariable

Kotlin| [Java](https://developer.android.com/reference/android/os/ConditionVariable "View this page in Java") 

```
open class ConditionVariable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.os.ConditionVariable](https://developer.android.com/reference/kotlin/android/os/ConditionVariable#) |

Class that implements the condition variable locking paradigm.

This differs from the built-in java.lang.Object wait() and notify() in that this class contains the condition to wait on itself. That means open(), close() and block() are sticky. If open() is called before block(), block() will not block, and instead return immediately.

This class uses itself as the object to wait on, so if you wait() or notify() on a ConditionVariable, the results are undefined.

## Summary

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ConditionVariable](https://developer.android.com/reference/kotlin/android/os/ConditionVariable#ConditionVariable())`()` Create the ConditionVariable in the default closed state. |
| [ConditionVariable](https://developer.android.com/reference/kotlin/android/os/ConditionVariable#ConditionVariable(kotlin.Boolean))`(`state:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Create the ConditionVariable with the given state. |

| Public methods ||
|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [block](https://developer.android.com/reference/kotlin/android/os/ConditionVariable#block())`()` Block the current thread until the condition is opened. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [block](https://developer.android.com/reference/kotlin/android/os/ConditionVariable#block(kotlin.Long))`(`timeoutMs:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Block the current thread until the condition is opened or until timeoutMs milliseconds have passed. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](https://developer.android.com/reference/kotlin/android/os/ConditionVariable#close())`()` Reset the condition to the closed state. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [open](https://developer.android.com/reference/kotlin/android/os/ConditionVariable#open())`()` Open the condition, and release all threads that are blocked. |

## Public constructors

### ConditionVariable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ConditionVariable()
```

Create the ConditionVariable in the default closed state. 

### ConditionVariable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ConditionVariable(state: Boolean)
```

Create the ConditionVariable with the given state.

Pass true for opened and false for closed.

## Public methods

### block

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun block(): Unit
```

Block the current thread until the condition is opened.

If the condition is already opened, return immediately. 

### block

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun block(timeoutMs: Long): Boolean
```

Block the current thread until the condition is opened or until timeoutMs milliseconds have passed.

If the condition is already opened, return immediately.

| Parameters ||
|-------------|------------------------------------------------------------------------------------------------------------------------|
| `timeoutMs` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the maximum time to wait in milliseconds. |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the condition was opened, false if the call returns because of the timeout. |

### close

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun close(): Unit
```

Reset the condition to the closed state.

Any threads that call block() will block until someone calls open. 

### open

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun open(): Unit
```

Open the condition, and release all threads that are blocked.

Any threads that later approach block() will not block unless close() is called.
