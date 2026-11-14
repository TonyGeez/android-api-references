# CoderMalfunctionError

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CoderMalfunctionError

```
open class CoderMalfunctionError : Error
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||
| | ↳ | [java.lang.Error](https://developer.android.com/reference/kotlin/java/lang/Error.html#) ||
| | | ↳ | [java.nio.charset.CoderMalfunctionError](https://developer.android.com/reference/kotlin/java/nio/charset/CoderMalfunctionError#) |
| --- | --- | --- | --- |

Error thrown when the [decodeLoop](https://developer.android.com/reference/kotlin/java/nio/charset/CharsetDecoder#decodeLoop(java.nio.ByteBuffer,%20java.nio.CharBuffer)) method of a [CharsetDecoder](https://developer.android.com/reference/kotlin/java/nio/charset/CharsetDecoder), or the [encodeLoop](https://developer.android.com/reference/kotlin/java/nio/charset/CharsetEncoder#encodeLoop(java.nio.CharBuffer,%20java.nio.ByteBuffer)) method of a [CharsetEncoder](https://developer.android.com/reference/kotlin/java/nio/charset/CharsetEncoder), throws an unexpected exception.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [CoderMalfunctionError](https://developer.android.com/reference/kotlin/java/nio/charset/CoderMalfunctionError#CoderMalfunctionError(java.lang.Exception))`(`cause:` ` [Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#)!`)` Initializes an instance of this class. |

## Public constructors

### CoderMalfunctionError

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
CoderMalfunctionError(cause: Exception!)
```

Initializes an instance of this class.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------------|
| `cause` | [Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#)!: The unexpected exception that was thrown |
