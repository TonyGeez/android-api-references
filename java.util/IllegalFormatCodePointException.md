# IllegalFormatCodePointException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# IllegalFormatCodePointException

```
open class IllegalFormatCodePointException : IllegalFormatException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||||
| --- | --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) |||||
| | | ↳ | [java.lang.RuntimeException](https://developer.android.com/reference/kotlin/java/lang/RuntimeException.html#) ||||
| --- | --- | --- | --- | --- | --- | --- |
| | | | ↳ | [java.lang.IllegalArgumentException](https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#) |||
| | | | | ↳ | [java.util.IllegalFormatException](https://developer.android.com/reference/kotlin/java/util/IllegalFormatException) ||
| | | | | | ↳ | [java.util.IllegalFormatCodePointException](https://developer.android.com/reference/kotlin/java/util/IllegalFormatCodePointException#) |
| --- | --- | --- | --- | --- | --- | --- |

Unchecked exception thrown when a character with an invalid Unicode code point as defined by [Character.isValidCodePoint](https://developer.android.com/reference/kotlin/java/lang/Character.html#isValidCodePoint(kotlin.Int))is passed to the [Formatter](https://developer.android.com/reference/kotlin/java/util/Formatter).

Unless otherwise specified, passing a`null`argument to any method or constructor in this class will cause a [NullPointerException](https://developer.android.com/reference/kotlin/java/lang/NullPointerException.html#) to be thrown.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [IllegalFormatCodePointException](https://developer.android.com/reference/kotlin/java/util/IllegalFormatCodePointException#IllegalFormatCodePointException(kotlin.Int))`(`c:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Constructs an instance of this class with the specified illegal code point as defined by [Character.isValidCodePoint](https://developer.android.com/reference/kotlin/java/lang/Character.html#isValidCodePoint(kotlin.Int)). |

| Public methods ||
|--------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getCodePoint](https://developer.android.com/reference/kotlin/java/util/IllegalFormatCodePointException#getCodePoint())`()` Returns the illegal code point as defined by [java.lang.Character#isValidCodePoint](https://developer.android.com/reference/kotlin/java/lang/Character.html#isValidCodePoint(kotlin.Int)). |

| Properties ||
|---------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [message](https://developer.android.com/reference/kotlin/java/util/IllegalFormatCodePointException#message:kotlin.String) <br /> |

## Public constructors

### IllegalFormatCodePointException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
IllegalFormatCodePointException(c: Int)
```

Constructs an instance of this class with the specified illegal code point as defined by [Character.isValidCodePoint](https://developer.android.com/reference/kotlin/java/lang/Character.html#isValidCodePoint(kotlin.Int)).

| Parameters ||
|-----|-----------------------------------------------------------------------------------------------------------|
| `c` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The illegal Unicode code point |

## Public methods

### getCodePoint

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getCodePoint(): Int
```

Returns the illegal code point as defined by [java.lang.Character#isValidCodePoint](https://developer.android.com/reference/kotlin/java/lang/Character.html#isValidCodePoint(kotlin.Int)).

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
