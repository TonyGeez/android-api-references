# CharConversionException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CharConversionException

```
open class CharConversionException : IOException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) |||
| | | ↳ | [java.io.IOException](https://developer.android.com/reference/kotlin/java/io/IOException) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [java.io.CharConversionException](https://developer.android.com/reference/kotlin/java/io/CharConversionException#) |

Base class for character conversion exceptions.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [CharConversionException](https://developer.android.com/reference/kotlin/java/io/CharConversionException#CharConversionException())`()` This provides no detailed message. |
| [CharConversionException](https://developer.android.com/reference/kotlin/java/io/CharConversionException#CharConversionException(kotlin.String))`(`s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` This provides a detailed message. |

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
