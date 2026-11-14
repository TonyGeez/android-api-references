# DateTimeParseException

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DateTimeParseException

```
open class DateTimeParseException : DateTimeException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||||
| --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) ||||
| | | ↳ | [java.lang.RuntimeException](https://developer.android.com/reference/kotlin/java/lang/RuntimeException.html#) |||
| --- | --- | --- | --- | --- | --- |
| | | | ↳ | [java.time.DateTimeException](https://developer.android.com/reference/kotlin/java/time/DateTimeException.html#) ||
| | | | | ↳ | [java.time.format.DateTimeParseException](https://developer.android.com/reference/kotlin/java/time/format/DateTimeParseException#) |

An exception thrown when an error occurs during parsing.

This exception includes the text being parsed and the error index.

## Summary

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [DateTimeParseException](https://developer.android.com/reference/kotlin/java/time/format/DateTimeParseException#DateTimeParseException(kotlin.String,%20kotlin.CharSequence,%20kotlin.Int))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `parsedData:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `errorIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Constructs a new exception with the specified message. |
| [DateTimeParseException](https://developer.android.com/reference/kotlin/java/time/format/DateTimeParseException#DateTimeParseException(kotlin.String,%20kotlin.CharSequence,%20kotlin.Int,%20kotlin.Throwable))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `parsedData:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `errorIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Constructs a new exception with the specified message and cause. |

| Public methods ||
|---------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getErrorIndex](https://developer.android.com/reference/kotlin/java/time/format/DateTimeParseException#getErrorIndex())`()` Returns the index where the error was found. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getParsedString](https://developer.android.com/reference/kotlin/java/time/format/DateTimeParseException#getParsedString())`()` Returns the string that was being parsed. |

## Public constructors

### DateTimeParseException

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
DateTimeParseException(
    message: String!, 
    parsedData: CharSequence!, 
    errorIndex: Int)
```

Constructs a new exception with the specified message.

| Parameters ||
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the message to use for this exception, may be null |
| `parsedData` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:the parsed text, should not be null |
| `errorIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index in the parsed string that was invalid, should be a valid index |
| --- | --- |

### DateTimeParseException

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
DateTimeParseException(
    message: String!, 
    parsedData: CharSequence!, 
    errorIndex: Int, 
    cause: Throwable!)
```

Constructs a new exception with the specified message and cause.

| Parameters ||
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the message to use for this exception, may be null |
| `parsedData` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:the parsed text, should not be null |
| `errorIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index in the parsed string that was invalid, should be a valid index |
| --- | --- |
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!:the cause exception, may be null |

## Public methods

### getErrorIndex

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getErrorIndex(): Int
```

Returns the index where the error was found.

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the index in the parsed string that was invalid, should be a valid index |

### getParsedString

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getParsedString(): String!
```

Returns the string that was being parsed.

| Return ||
|-----------------------------------------------------------------------------------|-------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the string that was being parsed, should not be null. |
