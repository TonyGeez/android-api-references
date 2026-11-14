# IllegalMonitorStateException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# IllegalMonitorStateException

```
open class IllegalMonitorStateException : RuntimeException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception) |||
| | | ↳ | [java.lang.RuntimeException](https://developer.android.com/reference/kotlin/java/lang/RuntimeException) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [java.lang.IllegalMonitorStateException](https://developer.android.com/reference/kotlin/java/lang/IllegalMonitorStateException#) |

Thrown to indicate that a thread has attempted to wait on an object's monitor or to notify other threads waiting on an object's monitor without owning the specified monitor.

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [IllegalMonitorStateException](https://developer.android.com/reference/kotlin/java/lang/IllegalMonitorStateException#IllegalMonitorStateException())`()` Constructs an`IllegalMonitorStateException`with no detail message. |
| [IllegalMonitorStateException](https://developer.android.com/reference/kotlin/java/lang/IllegalMonitorStateException#IllegalMonitorStateException(kotlin.String))`(`s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs an`IllegalMonitorStateException`with the specified detail message. |

## Public constructors

### IllegalMonitorStateException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
IllegalMonitorStateException()
```

Constructs an`IllegalMonitorStateException`with no detail message. 

### IllegalMonitorStateException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
IllegalMonitorStateException(s: String!)
```

Constructs an`IllegalMonitorStateException`with the specified detail message.

| Parameters ||
|-----|-------------------------------------------------------------------------------------------------------|
| `s` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the detail message. |
