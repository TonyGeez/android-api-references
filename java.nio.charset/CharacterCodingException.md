# CharacterCodingException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CharacterCodingException

```
open class CharacterCodingException : IOException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](../java.lang/Exception.md) |||
| | | ↳ | [java.io.IOException](../java.io/IOException.md) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [java.nio.charset.CharacterCodingException](CharacterCodingException.md) |

| Known Direct Subclasses [MalformedInputException](MalformedInputException.md), [UnmappableCharacterException](UnmappableCharacterException.md) |------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [MalformedInputException](MalformedInputException.md) | Checked exception thrown when an input byte sequence is not legal for given charset, or an input character sequence is not a legal sixteen-bit Unicode sequence. | | [UnmappableCharacterException](UnmappableCharacterException.md) | Checked exception thrown when an input character (or byte) sequence is valid but cannot be mapped to an output byte (or character) sequence. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Checked exception thrown when a character encoding or decoding error occurs.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [CharacterCodingException](CharacterCodingException.md))`()` Constructs an instance of this class. |

## Public constructors

### CharacterCodingException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
CharacterCodingException()
```

Constructs an instance of this class.
