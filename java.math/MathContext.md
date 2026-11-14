# MathContext

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MathContext

```
class MathContext : Serializable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [java.math.MathContext](https://developer.android.com/reference/kotlin/java/math/MathContext#) |

Immutable objects which encapsulate the context settings which describe certain rules for numerical operators, such as those implemented by the [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal) class.

The base-independent settings are:

1. `precision`: the number of digits to be used for an operation; results are rounded to this precision
2. `roundingMode`: a [RoundingMode](https://developer.android.com/reference/kotlin/java/math/RoundingMode) object which specifies the algorithm to be used for rounding.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [MathContext](https://developer.android.com/reference/kotlin/java/math/MathContext#MathContext(kotlin.Int))`(`setPrecision:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Constructs a new`MathContext`with the specified precision and the [HALF_UP](https://developer.android.com/reference/kotlin/java/math/RoundingMode) rounding mode. |
| [MathContext](https://developer.android.com/reference/kotlin/java/math/MathContext#MathContext(kotlin.Int,%20java.math.RoundingMode))`(`setPrecision:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `setRoundingMode:` ` [RoundingMode](https://developer.android.com/reference/kotlin/java/math/RoundingMode)!`)` Constructs a new`MathContext`with a specified precision and rounding mode. |
| [MathContext](https://developer.android.com/reference/kotlin/java/math/MathContext#MathContext(kotlin.String))`(`val:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a new`MathContext`from a string. |

| Public methods ||
|----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/java/math/MathContext#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Compares this`MathContext`with the specified`Object`for equality. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPrecision](https://developer.android.com/reference/kotlin/java/math/MathContext#getPrecision())`()` Returns the`precision`setting. |
| [RoundingMode](https://developer.android.com/reference/kotlin/java/math/RoundingMode)! | [getRoundingMode](https://developer.android.com/reference/kotlin/java/math/MathContext#getRoundingMode())`()` Returns the roundingMode setting. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/java/math/MathContext#hashCode())`()` Returns the hash code for this`MathContext`. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/java/math/MathContext#toString())`()` Returns the string representation of this`MathContext`. |

| Properties ||
|---------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [MathContext](https://developer.android.com/reference/kotlin/java/math/MathContext#)! | [DECIMAL128](https://developer.android.com/reference/kotlin/java/math/MathContext#DECIMAL128:java.math.MathContext) A`MathContext`object with a precision setting matching the precision of the IEEE 754-2019 decimal128 format, 34 digits, and a rounding mode of [HALF_EVEN](https://developer.android.com/reference/kotlin/java/math/RoundingMode). |
| static [MathContext](https://developer.android.com/reference/kotlin/java/math/MathContext#)! | [DECIMAL32](https://developer.android.com/reference/kotlin/java/math/MathContext#DECIMAL32:java.math.MathContext) A`MathContext`object with a precision setting matching the precision of the IEEE 754-2019 decimal32 format, 7 digits, and a rounding mode of [HALF_EVEN](https://developer.android.com/reference/kotlin/java/math/RoundingMode). |
| static [MathContext](https://developer.android.com/reference/kotlin/java/math/MathContext#)! | [DECIMAL64](https://developer.android.com/reference/kotlin/java/math/MathContext#DECIMAL64:java.math.MathContext) A`MathContext`object with a precision setting matching the precision of the IEEE 754-2019 decimal64 format, 16 digits, and a rounding mode of [HALF_EVEN](https://developer.android.com/reference/kotlin/java/math/RoundingMode). |
| static [MathContext](https://developer.android.com/reference/kotlin/java/math/MathContext#)! | [UNLIMITED](https://developer.android.com/reference/kotlin/java/math/MathContext#UNLIMITED:java.math.MathContext) A`MathContext`object whose settings have the values required for unlimited precision arithmetic. |

## Public constructors

### MathContext

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
MathContext(setPrecision: Int)
```

Constructs a new`MathContext`with the specified precision and the [HALF_UP](https://developer.android.com/reference/kotlin/java/math/RoundingMode) rounding mode.

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
| `setRoundingMode` | [RoundingMode](https://developer.android.com/reference/kotlin/java/math/RoundingMode)!:The rounding mode to use. |

| Exceptions ||
|--------------------------------------|--------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the`setPrecision`parameter is less than zero. |
| `java.lang.NullPointerException` | if the rounding mode argument is`null` |

### MathContext

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
MathContext(val: String!)
```

Constructs a new`MathContext`from a string. The string must be in the same format as that produced by the [toString](https://developer.android.com/reference/kotlin/java/math/MathContext#toString())method.

An`IllegalArgumentException`is thrown if the precision section of the string is out of range (`< 0`) or the string is not in the format created by the [toString](https://developer.android.com/reference/kotlin/java/math/MathContext#toString())method.

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

Returns the roundingMode setting. This will be one of [RoundingMode.CEILING](https://developer.android.com/reference/kotlin/java/math/RoundingMode), [RoundingMode.DOWN](https://developer.android.com/reference/kotlin/java/math/RoundingMode), [RoundingMode.FLOOR](https://developer.android.com/reference/kotlin/java/math/RoundingMode), [RoundingMode.HALF_DOWN](https://developer.android.com/reference/kotlin/java/math/RoundingMode), [RoundingMode.HALF_EVEN](https://developer.android.com/reference/kotlin/java/math/RoundingMode), [RoundingMode.HALF_UP](https://developer.android.com/reference/kotlin/java/math/RoundingMode), [RoundingMode.UNNECESSARY](https://developer.android.com/reference/kotlin/java/math/RoundingMode), or [RoundingMode.UP](https://developer.android.com/reference/kotlin/java/math/RoundingMode).

| Return ||
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [RoundingMode](https://developer.android.com/reference/kotlin/java/math/RoundingMode)! | a`RoundingMode`object which is the value of the`roundingMode`setting |

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

1. The string`"precision="`, immediately followed by the value of the precision setting as a numeric string as if generated by the [Integer.toString](https://developer.android.com/reference/kotlin/java/lang/Integer.html#toString(kotlin.Int))method.
2. The string`"roundingMode="`, immediately followed by the value of the`roundingMode`setting as a word. This word will be the same as the name of the corresponding public constant in the [RoundingMode](https://developer.android.com/reference/kotlin/java/math/RoundingMode) enum.

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

A`MathContext`object with a precision setting matching the precision of the IEEE 754-2019 decimal128 format, 34 digits, and a rounding mode of [HALF_EVEN](https://developer.android.com/reference/kotlin/java/math/RoundingMode). Note the exponent range of decimal64 is*not*used for rounding. 

### DECIMAL32

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DECIMAL32: MathContext!
```

A`MathContext`object with a precision setting matching the precision of the IEEE 754-2019 decimal32 format, 7 digits, and a rounding mode of [HALF_EVEN](https://developer.android.com/reference/kotlin/java/math/RoundingMode). Note the exponent range of decimal32 is*not*used for rounding. 

### DECIMAL64

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DECIMAL64: MathContext!
```

A`MathContext`object with a precision setting matching the precision of the IEEE 754-2019 decimal64 format, 16 digits, and a rounding mode of [HALF_EVEN](https://developer.android.com/reference/kotlin/java/math/RoundingMode). Note the exponent range of decimal64 is*not*used for rounding. 

### UNLIMITED

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val UNLIMITED: MathContext!
```

A`MathContext`object whose settings have the values required for unlimited precision arithmetic. The values of the settings are:`precision=0 roundingMode=HALF_UP`
