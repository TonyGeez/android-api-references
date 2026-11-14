# SyncFailedException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SyncFailedException

```
open class SyncFailedException : IOException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) |||
| | | ↳ | [java.io.IOException](https://developer.android.com/reference/kotlin/java/io/IOException) ||
| | | | ↳ | [java.io.SyncFailedException](https://developer.android.com/reference/kotlin/java/io/SyncFailedException#) |

Signals that a sync operation has failed.

## Summary

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SyncFailedException](https://developer.android.com/reference/kotlin/java/io/SyncFailedException#SyncFailedException(kotlin.String))`(`desc:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs an SyncFailedException with a detail message. |

## Public constructors

### SyncFailedException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SyncFailedException(desc: String!)
```

Constructs an SyncFailedException with a detail message. A detail message is a String that describes this particular exception.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------|
| `desc` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a String describing the exception. |
