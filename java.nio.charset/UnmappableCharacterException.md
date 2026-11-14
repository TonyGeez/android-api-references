# UnmappableCharacterException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# UnmappableCharacterException

```
open class UnmappableCharacterException : CharacterCodingException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||||
| --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) ||||
| | | ↳ | [java.io.IOException](https://developer.android.com/reference/kotlin/java/io/IOException.html#) |||
| --- | --- | --- | --- | --- | --- |
| | | | ↳ | [java.nio.charset.CharacterCodingException](https://developer.android.com/reference/kotlin/java/nio/charset/CharacterCodingException) ||
| | | | | ↳ | [java.nio.charset.UnmappableCharacterException](https://developer.android.com/reference/kotlin/java/nio/charset/UnmappableCharacterException#) |

Checked exception thrown when an input character (or byte) sequence is valid but cannot be mapped to an output byte (or character) sequence.

## Summary

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [UnmappableCharacterException](https://developer.android.com/reference/kotlin/java/nio/charset/UnmappableCharacterException#UnmappableCharacterException(kotlin.Int))`(`inputLength:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Constructs an`UnmappableCharacterException`with the given length. |

| Public methods ||
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getInputLength](https://developer.android.com/reference/kotlin/java/nio/charset/UnmappableCharacterException#getInputLength())`()` Returns the length of the input. |

| Properties ||
|---------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [message](https://developer.android.com/reference/kotlin/java/nio/charset/UnmappableCharacterException#message:kotlin.String) Returns the message. |

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
