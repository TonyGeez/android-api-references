# StreamCorruptedException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# StreamCorruptedException

```
open class StreamCorruptedException : ObjectStreamException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||||
| --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||||
| | ↳ | [java.lang.Exception](../java/lang/Exception.md) ||||
| | | ↳ | [java.io.IOException](../java/io/IOException.md) |||
| --- | --- | --- | --- | --- | --- |
| | | | ↳ | [java.io.ObjectStreamException](../java/io/ObjectStreamException.md) ||
| | | | | ↳ | [java.io.StreamCorruptedException](../java/io/StreamCorruptedException.md) |

Thrown when control information that was read from an object stream violates internal consistency checks.

## Summary

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [StreamCorruptedException](../java/io/StreamCorruptedException.md))`()` Create a StreamCorruptedException and list no reason why thrown. |
| [StreamCorruptedException](../java/io/StreamCorruptedException.md))`(`reason:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Create a StreamCorruptedException and list a reason why thrown. |

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
