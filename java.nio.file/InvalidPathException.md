# InvalidPathException

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# InvalidPathException

```
open class InvalidPathException : IllegalArgumentException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||||
| --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||||
| | ↳ | [java.lang.Exception](../java.lang/Exception.md) ||||
| | | ↳ | [java.lang.RuntimeException](../java.lang/RuntimeException.md) |||
| --- | --- | --- | --- | --- | --- |
| | | | ↳ | [java.lang.IllegalArgumentException](../java.lang/IllegalArgumentException.md) ||
| | | | | ↳ | [java.nio.file.InvalidPathException](InvalidPathException.md) |

Unchecked exception thrown when path string cannot be converted into a [Path](Path.md) because the path string contains invalid characters, or the path string is invalid for other file system specific reasons.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [InvalidPathException](InvalidPathException.md))`(`input:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `reason:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs an instance from the given input string and reason. |
| [InvalidPathException](InvalidPathException.md))`(`input:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `reason:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Constructs an instance from the given input string, reason, and error index. |

| Public methods ||
|---------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getIndex](InvalidPathException.md))`()` Returns an index into the input string of the position at which the error occurred, or`-1`if this position is not known. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getInput](InvalidPathException.md))`()` Returns the input string. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getReason](InvalidPathException.md))`()` Returns a string explaining why the input string was rejected. |
| --- | --- |

| Properties ||
|---------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [message](InvalidPathException.md) Returns a string describing the error. |

## Public constructors

### InvalidPathException

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
InvalidPathException(
    input: String!, 
    reason: String!)
```

Constructs an instance from the given input string and reason. The resulting object will have an error index of`-1`.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------|
| `input` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the input string |
| `reason` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a string explaining why the input was rejected |

| Exceptions ||
|----------------------------------|-------------------------------------------------|
| `java.lang.NullPointerException` | if either the input or reason strings are`null` |

### InvalidPathException

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
InvalidPathException(
    input: String!, 
    reason: String!, 
    index: Int)
```

Constructs an instance from the given input string, reason, and error index.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| `input` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the input string |
| `reason` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a string explaining why the input was rejected |
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index at which the error occurred, or`-1`if the index is not known |
| --- | --- |

| Exceptions ||
|--------------------------------------|-------------------------------------------------|
| `java.lang.NullPointerException` | if either the input or reason strings are`null` |
| `java.lang.IllegalArgumentException` | if the error index is less than`-1` |

## Public methods

### getIndex

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getIndex(): Int
```

Returns an index into the input string of the position at which the error occurred, or`-1`if this position is not known.

| Return ||
|----------------------------------------------------------------------------|-----------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the error index |

### getInput

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getInput(): String!
```

Returns the input string.

| Return ||
|-----------------------------------------------------------------------------------|------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the input string |

### getReason

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getReason(): String!
```

Returns a string explaining why the input string was rejected.

| Return ||
|-----------------------------------------------------------------------------------|-------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the reason string |

## Properties

### message

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open val message: String?
```

Returns a string describing the error. The resulting string consists of the reason string followed by a colon character (`':'`), a space, and the input string. If the error index is defined then the string`" at index "`followed by the index, in decimal, is inserted after the reason string and before the colon character.

| Return ||
|-----------------------------------------------------------------------------------|-------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | a string describing the error |
