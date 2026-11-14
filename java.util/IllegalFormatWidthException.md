# IllegalFormatWidthException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# IllegalFormatWidthException

```
open class IllegalFormatWidthException : IllegalFormatException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||||
| --- | --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||||
| | ↳ | [java.lang.Exception](../java.lang/Exception.md) |||||
| | | ↳ | [java.lang.RuntimeException](../java.lang/RuntimeException.md) ||||
| --- | --- | --- | --- | --- | --- | --- |
| | | | ↳ | [java.lang.IllegalArgumentException](../java.lang/IllegalArgumentException.md) |||
| | | | | ↳ | [java.util.IllegalFormatException](IllegalFormatException.md) ||
| | | | | | ↳ | [java.util.IllegalFormatWidthException](IllegalFormatWidthException.md) |
| --- | --- | --- | --- | --- | --- | --- |

Unchecked exception thrown when the format width is a negative value other than`-1`or is otherwise unsupported. If a given format width is not representable by an`int`type, then the value`Integer.MIN_VALUE`will be used in the exception.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [IllegalFormatWidthException](IllegalFormatWidthException.md))`(`w:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Constructs an instance of this class with the specified width. |

| Public methods ||
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getWidth](IllegalFormatWidthException.md))`()` Returns the width. |

| Properties ||
|---------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [message](IllegalFormatWidthException.md) <br /> |

## Public constructors

### IllegalFormatWidthException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
IllegalFormatWidthException(w: Int)
```

Constructs an instance of this class with the specified width.

| Parameters ||
|-----|--------------------------------------------------------------------------------------|
| `w` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The width |

## Public methods

### getWidth

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getWidth(): Int
```

Returns the width. If the width is not representable by an`int`, then returns`Integer.MIN_VALUE`.

| Return ||
|----------------------------------------------------------------------------|-----------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The width |

## Properties

### message

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open val message: String?
```

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | the detail message string of this`Throwable`instance (which may be`null`). |
