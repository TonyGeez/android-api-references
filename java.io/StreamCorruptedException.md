# StreamCorruptedException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# StreamCorruptedException

```
open class StreamCorruptedException : ObjectStreamException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||||
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) ||||
| | | ↳ | [java.io.IOException](https://developer.android.com/reference/kotlin/java/io/IOException) |||
| | | | ↳ | [java.io.ObjectStreamException](https://developer.android.com/reference/kotlin/java/io/ObjectStreamException) ||
| | | | | ↳ | [java.io.StreamCorruptedException](https://developer.android.com/reference/kotlin/java/io/StreamCorruptedException#) |

Thrown when control information that was read from an object stream violates internal consistency checks.

## Summary

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [StreamCorruptedException](https://developer.android.com/reference/kotlin/java/io/StreamCorruptedException#StreamCorruptedException())`()` Create a StreamCorruptedException and list no reason why thrown. |
| [StreamCorruptedException](https://developer.android.com/reference/kotlin/java/io/StreamCorruptedException#StreamCorruptedException(kotlin.String))`(`reason:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Create a StreamCorruptedException and list a reason why thrown. |

## Public constructors

### StreamCorruptedException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
StreamCorruptedException()
```

Create a StreamCorruptedException and list no reason why thrown. 

### StreamCorruptedException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
StreamCorruptedException(reason: String!)
```

Create a StreamCorruptedException and list a reason why thrown.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------|
| `reason` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:String describing the reason for the exception. |
