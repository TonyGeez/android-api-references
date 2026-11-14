# UnmappableCharacterException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# UnmappableCharacterException

```
open class UnmappableCharacterException : CharacterCodingException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||||
| --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||||
| | ↳ | [java.lang.Exception](../java/lang/Exception.md) ||||
| | | ↳ | [java.io.IOException](../java/io/IOException.md) |||
| --- | --- | --- | --- | --- | --- |
| | | | ↳ | [java.nio.charset.CharacterCodingException](../java/nio/charset/CharacterCodingException.md) ||
| | | | | ↳ | [java.nio.charset.UnmappableCharacterException](../java/nio/charset/UnmappableCharacterException.md) |

Checked exception thrown when an input character (or byte) sequence is valid but cannot be mapped to an output byte (or character) sequence.

## Summary

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [UnmappableCharacterException](../java/nio/charset/UnmappableCharacterException.md))`(`inputLength:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Constructs an`UnmappableCharacterException`with the given length. |

| Public methods ||
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getInputLength](../java/nio/charset/UnmappableCharacterException.md))`()` Returns the length of the input. |

| Properties ||
|---------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [message](../java/nio/charset/UnmappableCharacterException.md) Returns the message. |

## Public constructors

### UnmappableCharacterException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
UnmappableCharacterException(inputLength: Int)
```

Constructs an`UnmappableCharacterException`with the given length.

| Parameters ||
|---------------|----------------------------------------------------------------------------------------------------|
| `inputLength` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the length of the input |

## Public methods

### getInputLength

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getInputLength(): Int
```

Returns the length of the input.

| Return ||
|----------------------------------------------------------------------------|-------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the length of the input |

## Properties

### message

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open val message: String?
```

Returns the message.

| Return ||
|-----------------------------------------------------------------------------------|-------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | the message |
