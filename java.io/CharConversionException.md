# CharConversionException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CharConversionException

```
open class CharConversionException : IOException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](../java/lang/Exception.md) |||
| | | ↳ | [java.io.IOException](../java/io/IOException.md) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [java.io.CharConversionException](../java/io/CharConversionException.md) |

Base class for character conversion exceptions.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [CharConversionException](../java/io/CharConversionException.md))`()` This provides no detailed message. |
| [CharConversionException](../java/io/CharConversionException.md))`(`s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` This provides a detailed message. |

## Public constructors

### CharConversionException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
CharConversionException()
```

This provides no detailed message. 

### CharConversionException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
CharConversionException(s: String!)
```

This provides a detailed message.

| Parameters ||
|-----|---------------------------------------------------------------------------------------------------------------------------------------|
| `s` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the detailed message associated with the exception. |
