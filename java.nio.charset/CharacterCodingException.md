# CharacterCodingException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CharacterCodingException

```
open class CharacterCodingException : IOException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) |||
| | | ↳ | [java.io.IOException](https://developer.android.com/reference/kotlin/java/io/IOException.html#) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [java.nio.charset.CharacterCodingException](https://developer.android.com/reference/kotlin/java/nio/charset/CharacterCodingException#) |

| Known Direct Subclasses [MalformedInputException](https://developer.android.com/reference/kotlin/java/nio/charset/MalformedInputException), [UnmappableCharacterException](https://developer.android.com/reference/kotlin/java/nio/charset/UnmappableCharacterException) |------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [MalformedInputException](https://developer.android.com/reference/kotlin/java/nio/charset/MalformedInputException) | Checked exception thrown when an input byte sequence is not legal for given charset, or an input character sequence is not a legal sixteen-bit Unicode sequence. | | [UnmappableCharacterException](https://developer.android.com/reference/kotlin/java/nio/charset/UnmappableCharacterException) | Checked exception thrown when an input character (or byte) sequence is valid but cannot be mapped to an output byte (or character) sequence. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Checked exception thrown when a character encoding or decoding error occurs.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [CharacterCodingException](https://developer.android.com/reference/kotlin/java/nio/charset/CharacterCodingException#CharacterCodingException())`()` Constructs an instance of this class. |

## Public constructors

### CharacterCodingException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
CharacterCodingException()
```

Constructs an instance of this class.
