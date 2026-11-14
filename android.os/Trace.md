# Trace

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Trace

Kotlin| [Java](https://developer.android.com/reference/android/os/Trace "View this page in Java") 

```
class Trace
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.os.Trace](https://developer.android.com/reference/kotlin/android/os/Trace#) |

Writes trace events to the system trace buffer. These trace events can be collected and visualized using the Systrace tool.

This tracing mechanism is independent of the method tracing mechanism offered by android.os.Debug#startMethodTracing. In particular, it enables tracing of events that occur across multiple processes.

For information about using the Systrace tool, read [Analyzing Display and Performance with Systrace](https://developer.android.com/tools/debugging/systrace.html).

## Summary

| Public methods ||
|------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [beginAsyncSection](https://developer.android.com/reference/kotlin/android/os/Trace#beginAsyncSection(kotlin.String,%20kotlin.Int))`(`methodName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `cookie:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Writes a trace message to indicate that a given section of code has begun. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [beginSection](https://developer.android.com/reference/kotlin/android/os/Trace#beginSection(kotlin.String))`(`sectionName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Writes a trace message to indicate that a given section of code has begun. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [endAsyncSection](https://developer.android.com/reference/kotlin/android/os/Trace#endAsyncSection(kotlin.String,%20kotlin.Int))`(`methodName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `cookie:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Writes a trace message to indicate that the current method has ended. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [endSection](https://developer.android.com/reference/kotlin/android/os/Trace#endSection())`()` Writes a trace message to indicate that a given section of code has ended. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEnabled](https://developer.android.com/reference/kotlin/android/os/Trace#isEnabled())`()` Checks whether or not tracing is currently enabled. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setCounter](https://developer.android.com/reference/kotlin/android/os/Trace#setCounter(kotlin.String,%20kotlin.Long))`(`counterName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `counterValue:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Writes trace message to indicate the value of a given counter. |

## Public methods

### beginAsyncSection

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun beginAsyncSection(
    methodName: String, 
    cookie: Int
): Unit
```

Writes a trace message to indicate that a given section of code has begun. Must be followed by a call to [endAsyncSection(java.lang.String,int)](https://developer.android.com/reference/kotlin/android/os/Trace#endAsyncSection(kotlin.String,%20kotlin.Int))with the same methodName and cookie. Unlike [beginSection(java.lang.String)](https://developer.android.com/reference/kotlin/android/os/Trace#beginSection(kotlin.String))and [endSection()](https://developer.android.com/reference/kotlin/android/os/Trace#endSection()), asynchronous events do not need to be nested. The name and cookie used to begin an event must be used to end it.

| Parameters ||
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `methodName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The method name to appear in the trace. This value cannot be`null`. |
| `cookie` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Unique identifier for distinguishing simultaneous events |

### beginSection

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun beginSection(sectionName: String): Unit
```

Writes a trace message to indicate that a given section of code has begun. This call must be followed by a corresponding call to [endSection()](https://developer.android.com/reference/kotlin/android/os/Trace#endSection())on the same thread.

At this time the vertical bar character '|', newline character '\\n', and null character '\\0' are used internally by the tracing mechanism. If sectionName contains these characters they will be replaced with a space character in the trace.

| Parameters ||
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `sectionName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The name of the code section to appear in the trace. This may be at most 127 Unicode code units long. This value cannot be`null`. |

| Exceptions ||
|--------------------------------------|-----------------------------|
| `java.lang.IllegalArgumentException` | if`sectionName`is too long. |

### endAsyncSection

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun endAsyncSection(
    methodName: String, 
    cookie: Int
): Unit
```

Writes a trace message to indicate that the current method has ended. Must be called exactly once for each call to [beginAsyncSection(java.lang.String,int)](https://developer.android.com/reference/kotlin/android/os/Trace#beginAsyncSection(kotlin.String,%20kotlin.Int))using the same name and cookie.

| Parameters ||
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `methodName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The method name to appear in the trace. This value cannot be`null`. |
| `cookie` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Unique identifier for distinguishing simultaneous events |

### endSection

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun endSection(): Unit
```

Writes a trace message to indicate that a given section of code has ended. This call must be preceeded by a corresponding call to [beginSection(java.lang.String)](https://developer.android.com/reference/kotlin/android/os/Trace#beginSection(kotlin.String)). Calling this method will mark the end of the most recently begun section of code, so care must be taken to ensure that beginSection / endSection pairs are properly nested and called from the same thread. 

### isEnabled

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun isEnabled(): Boolean
```

Checks whether or not tracing is currently enabled. This is useful to avoid intermediate string creation for trace sections that require formatting. It is not necessary to guard all Trace method calls as they internally already check this. However it is recommended to use this to prevent creating any temporary objects that would then be passed to those methods to reduce runtime cost when tracing isn't enabled.

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if tracing is currently enabled, false otherwise |

### setCounter

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun setCounter(
    counterName: String, 
    counterValue: Long
): Unit
```

Writes trace message to indicate the value of a given counter.

| Parameters ||
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| `counterName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The counter name to appear in the trace. This value cannot be`null`. |
| `counterValue` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The counter value. |
