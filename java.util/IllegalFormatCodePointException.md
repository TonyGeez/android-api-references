# IllegalFormatCodePointException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# IllegalFormatCodePointException

```
open class IllegalFormatCodePointException : IllegalFormatException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||||
| --- | --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||||
| | ↳ | [java.lang.Exception](../java/lang/Exception.md) |||||
| | | ↳ | [java.lang.RuntimeException](../java/lang/RuntimeException.md) ||||
| --- | --- | --- | --- | --- | --- | --- |
| | | | ↳ | [java.lang.IllegalArgumentException](../java/lang/IllegalArgumentException.md) |||
| | | | | ↳ | [java.util.IllegalFormatException](../java/util/IllegalFormatException.md) ||
| | | | | | ↳ | [java.util.IllegalFormatCodePointException](../java/util/IllegalFormatCodePointException.md) |
| --- | --- | --- | --- | --- | --- | --- |

Unchecked exception thrown when a character with an invalid Unicode code point as defined by [Character.isValidCodePoint](../java/lang/Character.md))is passed to the [Formatter](../java/util/Formatter.md).

Unless otherwise specified, passing a`null`argument to any method or constructor in this class will cause a [NullPointerException](../java/lang/NullPointerException.md) to be thrown.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [IllegalFormatCodePointException](../java/util/IllegalFormatCodePointException.md))`(`c:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Constructs an instance of this class with the specified illegal code point as defined by [Character.isValidCodePoint](../java/lang/Character.md)). |

| Public methods ||
|--------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getCodePoint](../java/util/IllegalFormatCodePointException.md))`()` Returns the illegal code point as defined by [java.lang.Character#isValidCodePoint](../java/lang/Character.md)). |

| Properties ||
|---------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [message](../java/util/IllegalFormatCodePointException.md) <br /> |

## Public constructors

### IllegalFormatCodePointException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
IllegalFormatCodePointException(c: Int)
```

Constructs an instance of this class with the specified illegal code point as defined by [Character.isValidCodePoint](../java/lang/Character.md)).

| Parameters ||
|-----|-----------------------------------------------------------------------------------------------------------|
| `c` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The illegal Unicode code point |

## Public methods

### getCodePoint

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getCodePoint(): Int
```

Returns the illegal code point as defined by [java.lang.Character#isValidCodePoint](../java/lang/Character.md)).

| Return ||
|----------------------------------------------------------------------------|--------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The illegal Unicode code point |

## Properties

### message

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open val message: String?
```

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | the detail message string of this`Throwable`instance (which may be`null`). |
