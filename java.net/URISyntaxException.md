# URISyntaxException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# URISyntaxException

```
open class URISyntaxException : Exception
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) ||
| | | ↳ | [java.net.URISyntaxException](https://developer.android.com/reference/kotlin/java/net/URISyntaxException#) |
| --- | --- | --- | --- |

Checked exception thrown to indicate that a string could not be parsed as a URI reference.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [URISyntaxException](https://developer.android.com/reference/kotlin/java/net/URISyntaxException#URISyntaxException(kotlin.String,%20kotlin.String))`(`input:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `reason:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs an instance from the given input string and reason. |
| [URISyntaxException](https://developer.android.com/reference/kotlin/java/net/URISyntaxException#URISyntaxException(kotlin.String,%20kotlin.String,%20kotlin.Int))`(`input:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `reason:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Constructs an instance from the given input string, reason, and error index. |

| Public methods ||
|---------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getIndex](https://developer.android.com/reference/kotlin/java/net/URISyntaxException#getIndex())`()` Returns an index into the input string of the position at which the parse error occurred, or`-1`if this position is not known. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getInput](https://developer.android.com/reference/kotlin/java/net/URISyntaxException#getInput())`()` Returns the input string. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getReason](https://developer.android.com/reference/kotlin/java/net/URISyntaxException#getReason())`()` Returns a string explaining why the input string could not be parsed. |
| --- | --- |

| Properties ||
|---------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [message](https://developer.android.com/reference/kotlin/java/net/URISyntaxException#message:kotlin.String) Returns a string describing the parse error. |

## Public constructors

### URISyntaxException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
URISyntaxException(
    input: String!, 
    reason: String!)
```

Constructs an instance from the given input string and reason. The resulting object will have an error index of`-1`.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------|
| `input` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The input string |
| `reason` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:A string explaining why the input could not be parsed |

| Exceptions ||
|----------------------------------|-------------------------------------------------|
| `java.lang.NullPointerException` | If either the input or reason strings are`null` |

### URISyntaxException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
URISyntaxException(
    input: String!, 
    reason: String!, 
    index: Int)
```

Constructs an instance from the given input string, reason, and error index.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| `input` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The input string |
| `reason` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:A string explaining why the input could not be parsed |
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The index at which the parse error occurred, or`-1`if the index is not known |
| --- | --- |

| Exceptions ||
|--------------------------------------|-------------------------------------------------|
| `java.lang.NullPointerException` | If either the input or reason strings are`null` |
| `java.lang.IllegalArgumentException` | If the error index is less than`-1` |

## Public methods

### getIndex

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getIndex(): Int
```

Returns an index into the input string of the position at which the parse error occurred, or`-1`if this position is not known.

| Return ||
|----------------------------------------------------------------------------|-----------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The error index |

### getInput

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getInput(): String!
```

Returns the input string.

| Return ||
|-----------------------------------------------------------------------------------|------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | The input string |

### getReason

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getReason(): String!
```

Returns a string explaining why the input string could not be parsed.

| Return ||
|-----------------------------------------------------------------------------------|-------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | The reason string |

## Properties

### message

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open val message: String?
```

Returns a string describing the parse error. The resulting string consists of the reason string followed by a colon character (`':'`), a space, and the input string. If the error index is defined then the string`" at index "`followed by the index, in decimal, is inserted after the reason string and before the colon character.

| Return ||
|-----------------------------------------------------------------------------------|-------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | A string describing the parse error |
