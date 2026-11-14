# ParseException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ParseException

```
open class ParseException : Exception
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||
| | ↳ | [java.lang.Exception](../java.lang/Exception.md) ||
| | | ↳ | [java.text.ParseException](ParseException.md) |
| --- | --- | --- | --- |

| Known Direct Subclasses [StringPrepParseException](../android.icu.text/StringPrepParseException.md) |----------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------| | [StringPrepParseException](../android.icu.text/StringPrepParseException.md) | Exception that signals an error has occurred while parsing the input to StringPrep or IDNA. | |
| --- | --- | --- | --- | --- | --- | --- |

Signals that an error has been reached unexpectedly while parsing.

## Summary

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ParseException](ParseException.md))`(`s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `errorOffset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Constructs a ParseException with the specified detail message and offset. |

| Public methods ||
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getErrorOffset](ParseException.md))`()` Returns the position where the error was found. |

## Public constructors

### ParseException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ParseException(
    s: String!, 
    errorOffset: Int)
```

Constructs a ParseException with the specified detail message and offset. A detail message is a String that describes this particular exception.

| Parameters ||
|---------------|---------------------------------------------------------------------------------------------------------------------------------|
| `s` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the detail message |
| `errorOffset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the position where the error is found while parsing. |

## Public methods

### getErrorOffset

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getErrorOffset(): Int
```

Returns the position where the error was found.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the position where the error was found |
