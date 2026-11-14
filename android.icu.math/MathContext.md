# MathContext

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MathContext

Kotlin| [Java](../android/icu/math/MathContext.md) 
| --- | --- |

```
class MathContext : Serializable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.icu.math.MathContext](../android/icu/math/MathContext.md) |

The`MathContext`immutable class encapsulates the settings understood by the operator methods of the [BigDecimal](../android/icu/math/BigDecimal.md) class (and potentially other classes). Operator methods are those that effect an operation on a number or a pair of numbers.

The settings, which are not base-dependent, comprise:

1. `digits`: the number of digits (precision) to be used for an operation
2. `form`: the form of any exponent that results from the operation
3. `lostDigits`: whether checking for lost digits is enabled
4. `roundingMode`: the algorithm to be used for rounding.

When provided, a`MathContext`object supplies the settings for an operation directly.

When`MathContext.DEFAULT`is provided for a`MathContext`parameter then the default settings are used (`9, SCIENTIFIC, false, ROUND_HALF_UP`).

In the`BigDecimal`class, all methods which accept a`MathContext`object defaults) also have a version of the method which does not accept a MathContext parameter. These versions carry out unlimited precision fixed point arithmetic (as though the settings were (`0, PLAIN, false, ROUND_HALF_UP`).

The instance variables are shared with default access (so they are directly accessible to the`BigDecimal`class), but must never be changed.

The rounding mode constants have the same names and values as the constants of the same name in`java.math.BigDecimal`, to maintain compatibility with earlier versions of`BigDecimal`.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ENGINEERING](../android/icu/math/MathContext.md) Standard floating point notation (with engineering exponential format, where the power of ten is a multiple of 3). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PLAIN](../android/icu/math/MathContext.md) Plain (fixed point) notation, without any exponent. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ROUND_CEILING](../android/icu/math/MathContext.md) Rounding mode to round to a more positive number. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ROUND_DOWN](../android/icu/math/MathContext.md) Rounding mode to round towards zero. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ROUND_FLOOR](../android/icu/math/MathContext.md) Rounding mode to round to a more negative number. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ROUND_HALF_DOWN](../android/icu/math/MathContext.md) Rounding mode to round to nearest neighbor, where an equidistant value is rounded down. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ROUND_HALF_EVEN](../android/icu/math/MathContext.md) Rounding mode to round to nearest neighbor, where an equidistant value is rounded to the nearest even neighbor. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ROUND_HALF_UP](../android/icu/math/MathContext.md) Rounding mode to round to nearest neighbor, where an equidistant value is rounded up. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ROUND_UNNECESSARY](../android/icu/math/MathContext.md) Rounding mode to assert that no rounding is necessary. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ROUND_UP](../android/icu/math/MathContext.md) Rounding mode to round away from zero. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SCIENTIFIC](../android/icu/math/MathContext.md) Standard floating point notation (with scientific exponential format, where there is one digit before any decimal point). |

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [MathContext](../android/icu/math/MathContext.md))`(`setdigits:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Constructs a new`MathContext`with a specified precision. |
| [MathContext](../android/icu/math/MathContext.md))`(`setdigits:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `setform:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Constructs a new`MathContext`with a specified precision and form. |
| [MathContext](../android/icu/math/MathContext.md))`(`setdigits:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `setform:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `setlostdigits:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Constructs a new`MathContext`with a specified precision, form, and lostDigits setting. |
| [MathContext](../android/icu/math/MathContext.md))`(`setdigits:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `setform:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `setlostdigits:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `setroundingmode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Constructs a new`MathContext`with a specified precision, form, lostDigits, and roundingMode setting. |

| Public methods ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDigits](../android/icu/math/MathContext.md))`()` Returns the digits setting. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getForm](../android/icu/math/MathContext.md))`()` Returns the form setting. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getLostDigits](../android/icu/math/MathContext.md))`()` Returns the lostDigits setting. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getRoundingMode](../android/icu/math/MathContext.md))`()` Returns the roundingMode setting. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../android/icu/math/MathContext.md))`()` Returns the`MathContext`as a readable string. |

| Properties ||
|----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [MathContext](../android/icu/math/MathContext.md)! | [DEFAULT](../android/icu/math/MathContext.md) A`MathContext`object initialized to the default settings for general-purpose arithmetic. |

## Constants

### ENGINEERING

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ENGINEERING: Int
```

Standard floating point notation (with engineering exponential format, where the power of ten is a multiple of 3). Used as a setting to control the form of the result of a`BigDecimal`operation. A zero result in plain form may have a decimal part of one or more zeros. 

 Value: 2

**See Also**

- [#PLAIN](../android/icu/math/MathContext.md)
- [#SCIENTIFIC](../android/icu/math/MathContext.md) 

### PLAIN

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PLAIN: Int
```

Plain (fixed point) notation, without any exponent. Used as a setting to control the form of the result of a`BigDecimal`operation. A zero result in plain form may have a decimal part of one or more zeros. 

 Value: 0

**See Also**

- [#ENGINEERING](../android/icu/math/MathContext.md)
- [#SCIENTIFIC](../android/icu/math/MathContext.md) 

### ROUND_CEILING

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ROUND_CEILING: Int
```

Rounding mode to round to a more positive number. Used as a setting to control the rounding mode used during a`BigDecimal`operation.

If any of the discarded digits are non-zero then the result should be rounded towards the next more positive digit. 

 Value: 2

### ROUND_DOWN

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ROUND_DOWN: Int
```

Rounding mode to round towards zero. Used as a setting to control the rounding mode used during a`BigDecimal`operation.

All discarded digits are ignored (truncated). The result is neither incremented nor decremented. 

 Value: 1

### ROUND_FLOOR

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ROUND_FLOOR: Int
```

Rounding mode to round to a more negative number. Used as a setting to control the rounding mode used during a`BigDecimal`operation.

If any of the discarded digits are non-zero then the result should be rounded towards the next more negative digit. 

 Value: 3

### ROUND_HALF_DOWN

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ROUND_HALF_DOWN: Int
```

Rounding mode to round to nearest neighbor, where an equidistant value is rounded down. Used as a setting to control the rounding mode used during a`BigDecimal`operation.

If the discarded digits represent greater than half (0.5 times) the value of a one in the next position then the result should be rounded up (away from zero). Otherwise the discarded digits are ignored. 

 Value: 5

### ROUND_HALF_EVEN

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ROUND_HALF_EVEN: Int
```

Rounding mode to round to nearest neighbor, where an equidistant value is rounded to the nearest even neighbor. Used as a setting to control the rounding mode used during a`BigDecimal`operation.

If the discarded digits represent greater than half (0.5 times) the value of a one in the next position then the result should be rounded up (away from zero). If they represent less than half, then the result should be rounded down.

Otherwise (they represent exactly half) the result is rounded down if its rightmost digit is even, or rounded up if its rightmost digit is odd (to make an even digit). 

 Value: 6

### ROUND_HALF_UP

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ROUND_HALF_UP: Int
```

Rounding mode to round to nearest neighbor, where an equidistant value is rounded up. Used as a setting to control the rounding mode used during a`BigDecimal`operation.

If the discarded digits represent greater than or equal to half (0.5 times) the value of a one in the next position then the result should be rounded up (away from zero). Otherwise the discarded digits are ignored. 

 Value: 4

### ROUND_UNNECESSARY

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ROUND_UNNECESSARY: Int
```

Rounding mode to assert that no rounding is necessary. Used as a setting to control the rounding mode used during a`BigDecimal`operation.

Rounding (potential loss of information) is not permitted. If any of the discarded digits are non-zero then an`ArithmeticException`should be thrown. 

 Value: 7

### ROUND_UP

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ROUND_UP: Int
```

Rounding mode to round away from zero. Used as a setting to control the rounding mode used during a`BigDecimal`operation.

If any of the discarded digits are non-zero then the result will be rounded up (away from zero). 

 Value: 0

### SCIENTIFIC

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SCIENTIFIC: Int
```

Standard floating point notation (with scientific exponential format, where there is one digit before any decimal point). Used as a setting to control the form of the result of a`BigDecimal`operation. A zero result in plain form may have a decimal part of one or more zeros. 

 Value: 1

**See Also**

- [#ENGINEERING](../android/icu/math/MathContext.md)
- [#PLAIN](../android/icu/math/MathContext.md)

## Public constructors

### MathContext

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
MathContext(setdigits: Int)
```

Constructs a new`MathContext`with a specified precision. The other settings are set to the default values (see [DEFAULT](../android/icu/math/MathContext.md)). An`IllegalArgumentException`is thrown if the`setdigits`parameter is out of range (\<0 or \>999999999).

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------------------------------|
| `setdigits` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The`int`digits setting for this`MathContext`. |

| Exceptions ||
|--------------------------------------|-------------------------|
| `java.lang.IllegalArgumentException` | parameter out of range. |

### MathContext

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
MathContext(
    setdigits: Int, 
    setform: Int)
```

Constructs a new`MathContext`with a specified precision and form. The other settings are set to the default values (see [DEFAULT](../android/icu/math/MathContext.md)). An`IllegalArgumentException`is thrown if the`setdigits`parameter is out of range (\<0 or \>999999999), or if the value given for the`setform`parameter is not one of the appropriate constants.

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------------------------------|
| `setdigits` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The`int`digits setting for this`MathContext`. |
| `setform` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The`int`form setting for this`MathContext`. |

| Exceptions ||
|--------------------------------------|-------------------------|
| `java.lang.IllegalArgumentException` | parameter out of range. |

### MathContext

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
MathContext(
    setdigits: Int, 
    setform: Int, 
    setlostdigits: Boolean)
```

Constructs a new`MathContext`with a specified precision, form, and lostDigits setting. The roundingMode setting is set to its default value (see [DEFAULT](../android/icu/math/MathContext.md)). An`IllegalArgumentException`is thrown if the`setdigits`parameter is out of range (\<0 or \>999999999), or if the value given for the`setform`parameter is not one of the appropriate constants.

| Parameters ||
|-----------------|------------------------------------------------------------------------------------------------------------------------------------------|
| `setdigits` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The`int`digits setting for this`MathContext`. |
| `setform` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The`int`form setting for this`MathContext`. |
| `setlostdigits` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):The`boolean`lostDigits setting for this`MathContext`. |
| --- | --- |

| Exceptions ||
|--------------------------------------|-------------------------|
| `java.lang.IllegalArgumentException` | parameter out of range. |

### MathContext

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
MathContext(
    setdigits: Int, 
    setform: Int, 
    setlostdigits: Boolean, 
    setroundingmode: Int)
```

Constructs a new`MathContext`with a specified precision, form, lostDigits, and roundingMode setting. An`IllegalArgumentException`is thrown if the`setdigits`parameter is out of range (\<0 or \>999999999), or if the value given for the`setform`or`setroundingmode`parameters is not one of the appropriate constants.

| Parameters ||
|-------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| `setdigits` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The`int`digits setting for this`MathContext`. |
| `setform` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The`int`form setting for this`MathContext`. |
| `setlostdigits` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):The`boolean`lostDigits setting for this`MathContext`. |
| --- | --- |
| `setroundingmode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The`int`roundingMode setting for this`MathContext`. |

| Exceptions ||
|--------------------------------------|-------------------------|
| `java.lang.IllegalArgumentException` | parameter out of range. |

## Public methods

### getDigits

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDigits(): Int
```

Returns the digits setting. This value is always non-negative.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | an`int`which is the value of the digits setting |

### getForm

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getForm(): Int
```

Returns the form setting. This will be one of [ENGINEERING](../android/icu/math/MathContext.md), [PLAIN](../android/icu/math/MathContext.md), or [SCIENTIFIC](../android/icu/math/MathContext.md).

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | an`int`which is the value of the form setting |

### getLostDigits

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getLostDigits(): Boolean
```

Returns the lostDigits setting. This will be either`true`(enabled) or`false`(disabled).

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | a`boolean`which is the value of the lostDigits setting |

### getRoundingMode

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getRoundingMode(): Int
```

Returns the roundingMode setting. This will be one of [ROUND_CEILING](../android/icu/math/MathContext.md), [ROUND_DOWN](../android/icu/math/MathContext.md), [ROUND_FLOOR](../android/icu/math/MathContext.md), [ROUND_HALF_DOWN](../android/icu/math/MathContext.md), [ROUND_HALF_EVEN](../android/icu/math/MathContext.md), [ROUND_HALF_UP](../android/icu/math/MathContext.md), [ROUND_UNNECESSARY](../android/icu/math/MathContext.md), or [ROUND_UP](../android/icu/math/MathContext.md).

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | an`int`which is the value of the roundingMode setting |

### toString

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

Returns the`MathContext`as a readable string. The`String`returned represents the settings of the`MathContext`object as four blank-delimited words separated by a single blank and with no leading or trailing blanks, as follows:

1. `digits=`, immediately followed by the value of the digits setting as a numeric word.
2. `form=`, immediately followed by the value of the form setting as an uppercase word (one of`SCIENTIFIC`,`PLAIN`, or`ENGINEERING`).
3. `lostDigits=`, immediately followed by the value of the lostDigits setting (`1`if enabled,`0`if disabled).
4. `roundingMode=`, immediately followed by the value of the roundingMode setting as a word. This word will be the same as the name of the corresponding public constant.

<br />

For example: 
` digits=9 form=SCIENTIFIC lostDigits=0 roundingMode=ROUND_HALF_UP `

Additional words may be appended to the result of`toString`in the future if more properties are added to the class.

| Return ||
|----------------------------------------------------------------------------------|---------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a`String`representing the context settings. |

## Properties

### DEFAULT

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DEFAULT: MathContext!
```

A`MathContext`object initialized to the default settings for general-purpose arithmetic. That is,`digits=9 form=SCIENTIFIC lostDigits=false roundingMode=ROUND_HALF_UP`. 
**See Also**

- [#SCIENTIFIC](../android/icu/math/MathContext.md)
- [#ROUND_HALF_UP](../android/icu/math/MathContext.md)
