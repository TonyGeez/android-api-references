# MissingFormatWidthException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MissingFormatWidthException

```
open class MissingFormatWidthException : IllegalFormatException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||||
| --- | --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||||
| | ↳ | [java.lang.Exception](../java.lang/Exception.md) |||||
| | | ↳ | [java.lang.RuntimeException](../java.lang/RuntimeException.md) ||||
| --- | --- | --- | --- | --- | --- | --- |
| | | | ↳ | [java.lang.IllegalArgumentException](../java.lang/IllegalArgumentException.md) |||
| | | | | ↳ | [java.util.IllegalFormatException](IllegalFormatException.md) ||
| | | | | | ↳ | [java.util.MissingFormatWidthException](MissingFormatWidthException.md) |
| --- | --- | --- | --- | --- | --- | --- |

Unchecked exception thrown when the format width is required.

Unless otherwise specified, passing a`null`argument to any method or constructor in this class will cause a [NullPointerException](../java.lang/NullPointerException.md) to be thrown.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [MissingFormatWidthException](MissingFormatWidthException.md))`(`s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs an instance of this class with the specified format specifier. |

| Public methods ||
|---------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getFormatSpecifier](MissingFormatWidthException.md))`()` Returns the format specifier which does not have a width. |

| Properties ||
|---------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [message](MissingFormatWidthException.md) <br /> |

## Public constructors

### MissingFormatWidthException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
MissingFormatWidthException(s: String!)
```

Constructs an instance of this class with the specified format specifier.

| Parameters ||
|-----|------------------------------------------------------------------------------------------------------------------------------------|
| `s` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The format specifier which does not have a width |

## Public methods

### getFormatSpecifier

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getFormatSpecifier(): String!
```

Returns the format specifier which does not have a width.

| Return ||
|-----------------------------------------------------------------------------------|--------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | The format specifier which does not have a width |

## Properties

### message

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open val message: String?
```

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | the detail message string of this`Throwable`instance (which may be`null`). |
