# CoderMalfunctionError

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CoderMalfunctionError

```
open class CoderMalfunctionError : Error
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||
| | ↳ | [java.lang.Error](../java/lang/Error.md) ||
| | | ↳ | [java.nio.charset.CoderMalfunctionError](../java/nio/charset/CoderMalfunctionError.md) |
| --- | --- | --- | --- |

Error thrown when the [decodeLoop](../java/nio/charset/CharsetDecoder.md)) method of a [CharsetDecoder](../java/nio/charset/CharsetDecoder.md), or the [encodeLoop](../java/nio/charset/CharsetEncoder.md)) method of a [CharsetEncoder](../java/nio/charset/CharsetEncoder.md), throws an unexpected exception.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [CoderMalfunctionError](../java/nio/charset/CoderMalfunctionError.md))`(`cause:` ` [Exception](../java/lang/Exception.md)!`)` Initializes an instance of this class. |

## Public constructors

### CoderMalfunctionError

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
CoderMalfunctionError(cause: Exception!)
```

Initializes an instance of this class.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------------|
| `cause` | [Exception](../java/lang/Exception.md)!: The unexpected exception that was thrown |
