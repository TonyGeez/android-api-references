# MathContext

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MathContext

```
class MathContext : Serializable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.math.MathContext](../java/math/MathContext.md) |

Immutable objects which encapsulate the context settings which describe certain rules for numerical operators, such as those implemented by the [BigDecimal](../java/math/BigDecimal.md) class.

The base-independent settings are:

1. `precision`: the number of digits to be used for an operation; results are rounded to this precision
2. `roundingMode`: a [RoundingMode](../java/math/RoundingMode.md) object which specifies the algorithm to be used for rounding.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [MathContext](../java/math/MathContext.md))`(`setPrecision:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Constructs a new`MathContext`with the specified precision and the [HALF_UP](../java/math/RoundingMode.md) rounding mode. |
| [MathContext](../java/math/MathContext.md))`(`setPrecision:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `setRoundingMode:` ` [RoundingMode](../java/math/RoundingMode.md)!`)` Constructs a new`MathContext`with a specified precision and rounding mode. |
| [MathContext](../java/math/MathContext.md))`(`val:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a new`MathContext`from a string. |

| Public methods ||
|----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](../java/math/MathContext.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Compares this`MathContext`with the specified`Object`for equality. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPrecision](../java/math/MathContext.md))`()` Returns the`precision`setting. |
| [RoundingMode](../java/math/RoundingMode.md)! | [getRoundingMode](../java/math/MathContext.md))`()` Returns the roundingMode setting. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](../java/math/MathContext.md))`()` Returns the hash code for this`MathContext`. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../java/math/MathContext.md))`()` Returns the string representation of this`MathContext`. |

| Properties ||
|---------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [MathContext](../java/math/MathContext.md)! | [DECIMAL128](../java/math/MathContext.md) A`MathContext`object with a precision setting matching the precision of the IEEE 754-2019 decimal128 format, 34 digits, and a rounding mode of [HALF_EVEN](../java/math/RoundingMode.md). |
| static [MathContext](../java/math/MathContext.md)! | [DECIMAL32](../java/math/MathContext.md) A`MathContext`object with a precision setting matching the precision of the IEEE 754-2019 decimal32 format, 7 digits, and a rounding mode of [HALF_EVEN](../java/math/RoundingMode.md). |
| static [MathContext](../java/math/MathContext.md)! | [DECIMAL64](../java/math/MathContext.md) A`MathContext`object with a precision setting matching the precision of the IEEE 754-2019 decimal64 format, 16 digits, and a rounding mode of [HALF_EVEN](../java/math/RoundingMode.md). |
| --- | --- |
| static [MathContext](../java/math/MathContext.md)! | [UNLIMITED](../java/math/MathContext.md) A`MathContext`object whose settings have the values required for unlimited precision arithmetic. |

## Public constructors

### MathContext

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
MathContext(setPrecision: Int)
```

Constructs a new`MathContext`with the specified precision and the [HALF_UP](../java/math/RoundingMode.md) rounding mode.

| Parameters ||
|----------------|--------------------------------------------------------------------------------------------------------------------|
| `setPrecision` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The non-negative`int`precision setting. |

| Exceptions ||
|--------------------------------------|--------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the`setPrecision`parameter is less than zero. |

### MathContext

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
MathContext(
    setPrecision: Int, 
    setRoundingMode: RoundingMode!)
```

Constructs a new`MathContext`with a specified precision and rounding mode.

| Parameters ||
|-------------------|--------------------------------------------------------------------------------------------------------------------|
| `setPrecision` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The non-negative`int`precision setting. |
| `setRoundingMode` | [RoundingMode](../java/math/RoundingMode.md)!:The rounding mode to use. |

| Exceptions ||
|--------------------------------------|--------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the`setPrecision`parameter is less than zero. |
| `java.lang.NullPointerException` | if the rounding mode argument is`null` |

### MathContext

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
MathContext(val: String!)
```

Constructs a new`MathContext`from a string. The string must be in the same format as that produced by the [toString](../java/math/MathContext.md))method.

An`IllegalArgumentException`is thrown if the precision section of the string is out of range (`< 0`) or the string is not in the format created by the [toString](../java/math/MathContext.md))method.

| Parameters ||
|-------|-----------------------------------------------------------------------------------------------------------|
| `val` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The string to be parsed |

| Exceptions ||
|--------------------------------------|-----------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the precision section is out of range or of incorrect format |
| `java.lang.NullPointerException` | if the argument is`null` |

## Public methods

### equals

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

Compares this`MathContext`with the specified`Object`for equality.

| Parameters ||
|-------|------------------------------------------------------|
| `obj` | the reference object with which to compare. |
| `x` | `Object`to which this`MathContext`is to be compared. |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if and only if the specified`Object`is a`MathContext`object which has exactly the same settings as this object |

### getPrecision

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPrecision(): Int
```

Returns the`precision`setting. This value is always non-negative.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | an`int`which is the value of the`precision`setting |

### getRoundingMode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getRoundingMode(): RoundingMode!
```

Returns the roundingMode setting. This will be one of [RoundingMode.CEILING](../java/math/RoundingMode.md), [RoundingMode.DOWN](../java/math/RoundingMode.md), [RoundingMode.FLOOR](../java/math/RoundingMode.md), [RoundingMode.HALF_DOWN](../java/math/RoundingMode.md), [RoundingMode.HALF_EVEN](../java/math/RoundingMode.md), [RoundingMode.HALF_UP](../java/math/RoundingMode.md), [RoundingMode.UNNECESSARY](../java/math/RoundingMode.md), or [RoundingMode.UP](../java/math/RoundingMode.md).

| Return ||
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [RoundingMode](../java/math/RoundingMode.md)! | a`RoundingMode`object which is the value of the`roundingMode`setting |

### hashCode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

Returns the hash code for this`MathContext`.

| Return ||
|----------------------------------------------------------------------------|---------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | hash code for this`MathContext` |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

Returns the string representation of this`MathContext`. The`String`returned represents the settings of the`MathContext`object as two space-delimited words (separated by a single space character,`'\u0020'`, and with no leading or trailing white space), as follows:

1. The string`"precision="`, immediately followed by the value of the precision setting as a numeric string as if generated by the [Integer.toString](../java/lang/Integer.md))method.
2. The string`"roundingMode="`, immediately followed by the value of the`roundingMode`setting as a word. This word will be the same as the name of the corresponding public constant in the [RoundingMode](../java/math/RoundingMode.md) enum.

<br />

For example: 

```kotlin
precision=9 roundingMode=HALF_UP
  
```
Additional words may be appended to the result of`toString`in the future if more properties are added to this class.

| Return ||
|----------------------------------------------------------------------------------|--------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a`String`representing the context settings |

## Properties

### DECIMAL128

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DECIMAL128: MathContext!
```

A`MathContext`object with a precision setting matching the precision of the IEEE 754-2019 decimal128 format, 34 digits, and a rounding mode of [HALF_EVEN](../java/math/RoundingMode.md). Note the exponent range of decimal64 is*not*used for rounding. 

### DECIMAL32

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DECIMAL32: MathContext!
```

A`MathContext`object with a precision setting matching the precision of the IEEE 754-2019 decimal32 format, 7 digits, and a rounding mode of [HALF_EVEN](../java/math/RoundingMode.md). Note the exponent range of decimal32 is*not*used for rounding. 

### DECIMAL64

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DECIMAL64: MathContext!
```

A`MathContext`object with a precision setting matching the precision of the IEEE 754-2019 decimal64 format, 16 digits, and a rounding mode of [HALF_EVEN](../java/math/RoundingMode.md). Note the exponent range of decimal64 is*not*used for rounding. 

### UNLIMITED

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val UNLIMITED: MathContext!
```

A`MathContext`object whose settings have the values required for unlimited precision arithmetic. The values of the settings are:`precision=0 roundingMode=HALF_UP`
