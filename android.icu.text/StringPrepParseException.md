Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# StringPrepParseException

Kotlin | [Java](StringPrepParseException.md)
| --- | --- |

```
open class StringPrepParseException : ParseException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](../java.lang/Exception.md) |||
| | | ↳ | [java.text.ParseException](../java.text/ParseException.md) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [android.icu.text.StringPrepParseException](StringPrepParseException.md) |

Exception that signals an error has occurred while parsing the input to StringPrep or IDNA.

## Summary

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/StringPrepParseException#ACE_PREFIX_ERROR:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/StringPrepParseException#BUFFER_OVERFLOW_ERROR:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/StringPrepParseException#CHECK_BIDI_ERROR:kotlin.Int` <br /> |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/StringPrepParseException#DOMAIN_NAME_TOO_LONG_ERROR:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/StringPrepParseException#ILLEGAL_CHAR_FOUND:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/StringPrepParseException#INVALID_CHAR_FOUND:kotlin.Int` <br /> |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/StringPrepParseException#LABEL_TOO_LONG_ERROR:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/StringPrepParseException#PROHIBITED_ERROR:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/StringPrepParseException#STD3_ASCII_RULES_ERROR:kotlin.Int` <br /> |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/StringPrepParseException#UNASSIGNED_ERROR:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/StringPrepParseException#VERIFICATION_ERROR:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/StringPrepParseException#ZERO_LENGTH_LABEL:kotlin.Int` <br /> |
| --- | --- |

| Public constructors ||
|---|---|
| StringPrepParseException Construct a ParseException object with the given message and error code |
| StringPrepParseException Construct a ParseException object with the given message and error code |
| StringPrepParseException Construct a ParseException object with the given message and error code |

| Public methods ||
|---|---|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | equals Compare this ParseException to another and evaluate if they are equal. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getError Returns the error code of this exception. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | hashCode Mock implementation of hashCode(). |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | toString Returns the position of error in the rules string |

| Inherited functions ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/java/text/ParseException.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | getErrorOffset Returns the position where the error was found. <br /> | ||

## Constants

### ACE_PREFIX_ERROR

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACE_PREFIX_ERROR: Int
```

 Value: 6

### BUFFER_OVERFLOW_ERROR

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val BUFFER_OVERFLOW_ERROR: Int
```

 Value: 9

### CHECK_BIDI_ERROR

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CHECK_BIDI_ERROR: Int
```

 Value: 4

### DOMAIN_NAME_TOO_LONG_ERROR

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DOMAIN_NAME_TOO_LONG_ERROR: Int
```

 Value: 11

### ILLEGAL_CHAR_FOUND

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ILLEGAL_CHAR_FOUND: Int
```

 Value: 1

### INVALID_CHAR_FOUND

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val INVALID_CHAR_FOUND: Int
```

 Value: 0

### LABEL_TOO_LONG_ERROR

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LABEL_TOO_LONG_ERROR: Int
```

 Value: 8

### PROHIBITED_ERROR

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PROHIBITED_ERROR: Int
```

 Value: 2

### STD3_ASCII_RULES_ERROR

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STD3_ASCII_RULES_ERROR: Int
```

 Value: 5

### UNASSIGNED_ERROR

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val UNASSIGNED_ERROR: Int
```

 Value: 3

### VERIFICATION_ERROR

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val VERIFICATION_ERROR: Int
```

 Value: 7

### ZERO_LENGTH_LABEL

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ZERO_LENGTH_LABEL: Int
```

 Value: 10

## Public constructors

### StringPrepParseException

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
StringPrepParseException(
    message: String!, 
    error: Int)
```

Construct a ParseException object with the given message and error code

| Parameters ||
|---|---|
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: A string describing the type of error that occurred |
| `error` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The error that has occurred |

### StringPrepParseException

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
StringPrepParseException(
    message: String!, 
    error: Int, 
    rules: String!, 
    pos: Int)
```

Construct a ParseException object with the given message and error code

| Parameters ||
|---|---|
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: A string describing the type of error that occurred |
| `error` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The error that has occurred |
| `rules` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The input rules string |
| --- | --- |
| `pos` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The position of error in the rules string |

### StringPrepParseException

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
StringPrepParseException(
    message: String!, 
    error: Int, 
    rules: String!, 
    pos: Int, 
    lineNumber: Int)
```

Construct a ParseException object with the given message and error code

| Parameters ||
|---|---|
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: A string describing the type of error that occurred |
| `error` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The error that has occurred |
| `rules` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The input rules string |
| --- | --- |
| `pos` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The position of error in the rules string |
| `lineNumber` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The line number at which the error has occurred. If the parse engine is not using this field, it should set it to zero. Otherwise it should be a positive integer. The default value of this field is -1. It will be set to 0 if the code populating this struct is not using line numbers. |

## Public methods

### equals

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun equals(other: Any?): Boolean
```

Compare this ParseException to another and evaluate if they are equal. The comparison works only on the type of error and does not compare the rules strings, if any, for equality.

| Parameters ||
|---|---|
| `obj` | the reference object with which to compare. |
| `other` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?: The exception that this object should be compared to |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the objects are equal, false if unequal |

### getError

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getError(): Int
```

Returns the error code of this exception. This method is only used for testing to verify the error.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The error code |

### hashCode

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun hashCode(): Int
```

Mock implementation of hashCode(). This implementation always returns a constant value. When Java assertion is enabled, this method triggers an assertion failure.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a hash code value for this object. |

### toString

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun toString(): String
```

Returns the position of error in the rules string

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | String |
