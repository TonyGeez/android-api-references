# IllegalFormatPrecisionException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# IllegalFormatPrecisionException

```
open class IllegalFormatPrecisionException : IllegalFormatException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||||
| --- | --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||||
| | ↳ | [java.lang.Exception](../java/lang/Exception.md) |||||
| | | ↳ | [java.lang.RuntimeException](../java/lang/RuntimeException.md) ||||
| --- | --- | --- | --- | --- | --- | --- |
| | | | ↳ | [java.lang.IllegalArgumentException](../java/lang/IllegalArgumentException.md) |||
| | | | | ↳ | [java.util.IllegalFormatException](../java/util/IllegalFormatException.md) ||
| | | | | | ↳ | [java.util.IllegalFormatPrecisionException](../java/util/IllegalFormatPrecisionException.md) |
| --- | --- | --- | --- | --- | --- | --- |

Unchecked exception thrown when the precision is a negative value other than `-1`, the conversion does not support a precision, or the value is otherwise unsupported. If the precision is not representable by an `int` type, then the value `Integer.MIN_VALUE` will be used in the exception.

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [IllegalFormatPrecisionException](../java/util/IllegalFormatPrecisionException.md))`(`p:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Constructs an instance of this class with the specified precision. |

| Public methods ||
|---------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPrecision](../java/util/IllegalFormatPrecisionException.md))`()` Returns the precision. |

| Properties ||
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [message](../java/util/IllegalFormatPrecisionException.md) <br /> |

## Public constructors

### IllegalFormatPrecisionException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
IllegalFormatPrecisionException(p: Int)
```

Constructs an instance of this class with the specified precision.

| Parameters ||
|-----|-------------------------------------------------------------------------------------------|
| `p` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The precision |

## Public methods

### getPrecision

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPrecision(): Int
```

Returns the precision. If the precision isn't representable by an `int`, then will return `Integer.MIN_VALUE`.

| Return ||
|----------------------------------------------------------------------------|---------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The precision |

## Properties

### message

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open val message: String?
```

| Return ||
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | the detail message string of this `Throwable` instance (which may be `null`). |
