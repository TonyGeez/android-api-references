# RoundingMode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RoundingMode

```
class RoundingMode
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [kotlin.Enum](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-enum/index.html)\< [java.math.RoundingMode](https://developer.android.com/reference/kotlin/java/math/RoundingMode#)\> ||
| | ↳ | [java.math.RoundingMode](https://developer.android.com/reference/kotlin/java/math/RoundingMode#) |

| Known Direct Subclasses [RoundingMode.CEILING](https://developer.android.com/reference/kotlin/java/math/RoundingMode#ENUM_VALUE:CEILING), [RoundingMode.DOWN](https://developer.android.com/reference/kotlin/java/math/RoundingMode#ENUM_VALUE:DOWN), [RoundingMode.FLOOR](https://developer.android.com/reference/kotlin/java/math/RoundingMode#ENUM_VALUE:FLOOR), [RoundingMode.HALF_DOWN](https://developer.android.com/reference/kotlin/java/math/RoundingMode#ENUM_VALUE:HALF_DOWN), [RoundingMode.HALF_EVEN](https://developer.android.com/reference/kotlin/java/math/RoundingMode#ENUM_VALUE:HALF_EVEN), [RoundingMode.HALF_UP](https://developer.android.com/reference/kotlin/java/math/RoundingMode#ENUM_VALUE:HALF_UP), [RoundingMode.UNNECESSARY](https://developer.android.com/reference/kotlin/java/math/RoundingMode#ENUM_VALUE:UNNECESSARY), [RoundingMode.UP](https://developer.android.com/reference/kotlin/java/math/RoundingMode#ENUM_VALUE:UP) |--------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------| | [RoundingMode.CEILING](https://developer.android.com/reference/kotlin/java/math/RoundingMode#ENUM_VALUE:CEILING) | Rounding mode to round towards positive infinity. | | [RoundingMode.DOWN](https://developer.android.com/reference/kotlin/java/math/RoundingMode#ENUM_VALUE:DOWN) | Rounding mode to round towards zero. | | [RoundingMode.FLOOR](https://developer.android.com/reference/kotlin/java/math/RoundingMode#ENUM_VALUE:FLOOR) | Rounding mode to round towards negative infinity. | | [RoundingMode.HALF_DOWN](https://developer.android.com/reference/kotlin/java/math/RoundingMode#ENUM_VALUE:HALF_DOWN) | Rounding mode to round towards "nearest neighbor" unless both neighbors are equidistant, in which case round down. | | [RoundingMode.HALF_EVEN](https://developer.android.com/reference/kotlin/java/math/RoundingMode#ENUM_VALUE:HALF_EVEN) | Rounding mode to round towards the "nearest neighbor" unless both neighbors are equidistant, in which case, round towards the even neighbor. | | [RoundingMode.HALF_UP](https://developer.android.com/reference/kotlin/java/math/RoundingMode#ENUM_VALUE:HALF_UP) | Rounding mode to round towards "nearest neighbor" unless both neighbors are equidistant, in which case round up. | | [RoundingMode.UNNECESSARY](https://developer.android.com/reference/kotlin/java/math/RoundingMode#ENUM_VALUE:UNNECESSARY) | Rounding mode to assert that the requested operation has an exact result, hence no rounding is necessary. | | [RoundingMode.UP](https://developer.android.com/reference/kotlin/java/math/RoundingMode#ENUM_VALUE:UP) | Rounding mode to round away from zero. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Specifies a*rounding policy* for numerical operations capable of discarding precision. Each rounding mode indicates how the least significant returned digit of a rounded result is to be calculated. If fewer digits are returned than the digits needed to represent the exact numerical result, the discarded digits will be referred to as the*discarded fraction*regardless the digits' contribution to the value of the number. In other words, considered as a numerical value, the discarded fraction could have an absolute value greater than one.

Each rounding mode description includes a table listing how different two-digit decimal values would round to a one digit decimal value under the rounding mode in question. The result column in the tables could be gotten by creating a`BigDecimal`number with the specified value, forming a [MathContext](https://developer.android.com/reference/kotlin/java/math/MathContext) object with the proper settings (`precision`set to`1`, and the`roundingMode`set to the rounding mode in question), and calling [round](https://developer.android.com/reference/kotlin/java/math/BigDecimal#round(java.math.MathContext))on this number with the proper`MathContext`. A summary table showing the results of these rounding operations for all rounding modes appears below.
**Summary of Rounding Operations Under Different Rounding Modes**

| Input Number | Result of rounding input to one digit with the given rounding mode ||||||||
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Input Number | `UP` | `DOWN` | `CEILING` | `FLOOR` | `HALF_UP` | `HALF_DOWN` | `HALF_EVEN` | `UNNECESSARY` |
| 5.5 | 6 | 5 | 6 | 5 | 6 | 5 | 6 | throw`ArithmeticException` |
| 2.5 | 3 | 2 | 3 | 2 | 3 | 2 | 2 | throw`ArithmeticException` |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| 1.6 | 2 | 1 | 2 | 1 | 2 | 2 | 2 | throw`ArithmeticException` |
| 1.1 | 2 | 1 | 2 | 1 | 1 | 1 | 1 | throw`ArithmeticException` |
| 1.0 | 1 | 1 | 1 | 1 | 1 | 1 | 1 | 1 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| -1.0 | -1 | -1 | -1 | -1 | -1 | -1 | -1 | -1 |
| -1.1 | -2 | -1 | -1 | -2 | -1 | -1 | -1 | throw`ArithmeticException` |
| -1.6 | -2 | -1 | -1 | -2 | -2 | -2 | -2 | throw`ArithmeticException` |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| -2.5 | -3 | -2 | -2 | -3 | -3 | -2 | -2 | throw`ArithmeticException` |
| -5.5 | -6 | -5 | -5 | -6 | -6 | -5 | -6 | throw`ArithmeticException` |
|--------------|------|--------|-----------|---------|-----------|-------------|-------------|----------------------------|

This`enum`is intended to replace the integer-based enumeration of rounding mode constants in [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal)([BigDecimal.ROUND_UP](https://developer.android.com/reference/kotlin/java/math/BigDecimal#ROUND_UP:kotlin.Int), [BigDecimal.ROUND_DOWN](https://developer.android.com/reference/kotlin/java/math/BigDecimal#ROUND_DOWN:kotlin.Int), etc. ).

## Summary

| Enum values ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [CEILING](https://developer.android.com/reference/kotlin/java/math/RoundingMode#ENUM_VALUE:CEILING) Rounding mode to round towards positive infinity. |
| [DOWN](https://developer.android.com/reference/kotlin/java/math/RoundingMode#ENUM_VALUE:DOWN) Rounding mode to round towards zero. |
| [FLOOR](https://developer.android.com/reference/kotlin/java/math/RoundingMode#ENUM_VALUE:FLOOR) Rounding mode to round towards negative infinity. |
| [HALF_DOWN](https://developer.android.com/reference/kotlin/java/math/RoundingMode#ENUM_VALUE:HALF_DOWN) Rounding mode to round towards "nearest neighbor" unless both neighbors are equidistant, in which case round down. |
| [HALF_EVEN](https://developer.android.com/reference/kotlin/java/math/RoundingMode#ENUM_VALUE:HALF_EVEN) Rounding mode to round towards the "nearest neighbor" unless both neighbors are equidistant, in which case, round towards the even neighbor. |
| [HALF_UP](https://developer.android.com/reference/kotlin/java/math/RoundingMode#ENUM_VALUE:HALF_UP) Rounding mode to round towards "nearest neighbor" unless both neighbors are equidistant, in which case round up. |
| [UNNECESSARY](https://developer.android.com/reference/kotlin/java/math/RoundingMode#ENUM_VALUE:UNNECESSARY) Rounding mode to assert that the requested operation has an exact result, hence no rounding is necessary. |
| [UP](https://developer.android.com/reference/kotlin/java/math/RoundingMode#ENUM_VALUE:UP) Rounding mode to round away from zero. |

| Public methods ||
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [RoundingMode](https://developer.android.com/reference/kotlin/java/math/RoundingMode#)! | [valueOf](https://developer.android.com/reference/kotlin/java/math/RoundingMode#valueOf(kotlin.Int))`(`rm:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the`RoundingMode`object corresponding to a legacy integer rounding mode constant in [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal). |

## Enum values

### CEILING

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val CEILING : RoundingMode
```

Rounding mode to round towards positive infinity. If the result is positive, behaves as for`RoundingMode.UP`; if negative, behaves as for`RoundingMode.DOWN`. Note that this rounding mode never decreases the calculated value. This mode corresponds to the IEEE 754-2019 rounding-direction attribute roundTowardPositive.

Example:

| Input Number | Input rounded to one digit with`CEILING`rounding |
| --- | --- |
| 5.5 | 6 |
| 2.5 | 3 |
| 1.6 | 2 |
| --- | --- |
| 1.1 | 2 |
| 1.0 | 1 |
| -1.0 | -1 |
| --- | --- |
| -1.1 | -1 |
| -1.6 | -1 |
| -2.5 | -2 |
| --- | --- |
| -5.5 | -5 |
|--------------|--------------------------------------------------|

### DOWN

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val DOWN : RoundingMode
```

Rounding mode to round towards zero. Never increments the digit prior to a discarded fraction (i.e., truncates). Note that this rounding mode never increases the magnitude of the calculated value. This mode corresponds to the IEEE 754-2019 rounding-direction attribute roundTowardZero.

Example:

| Input Number | Input rounded to one digit with`DOWN`rounding |
| --- | --- |
| 5.5 | 5 |
| 2.5 | 2 |
| 1.6 | 1 |
| --- | --- |
| 1.1 | 1 |
| 1.0 | 1 |
| -1.0 | -1 |
| --- | --- |
| -1.1 | -1 |
| -1.6 | -1 |
| -2.5 | -2 |
| --- | --- |
| -5.5 | -5 |
|--------------|-----------------------------------------------|

### FLOOR

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val FLOOR : RoundingMode
```

Rounding mode to round towards negative infinity. If the result is positive, behave as for`RoundingMode.DOWN`; if negative, behave as for`RoundingMode.UP`. Note that this rounding mode never increases the calculated value. This mode corresponds to the IEEE 754-2019 rounding-direction attribute roundTowardNegative.

Example:

| Input Number | Input rounded to one digit with`FLOOR`rounding |
| --- | --- |
| 5.5 | 5 |
| 2.5 | 2 |
| 1.6 | 1 |
| --- | --- |
| 1.1 | 1 |
| 1.0 | 1 |
| -1.0 | -1 |
| --- | --- |
| -1.1 | -2 |
| -1.6 | -2 |
| -2.5 | -3 |
| --- | --- |
| -5.5 | -6 |
|--------------|------------------------------------------------|

### HALF_DOWN

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val HALF_DOWN : RoundingMode
```

Rounding mode to round towards "nearest neighbor" unless both neighbors are equidistant, in which case round down. Behaves as for`RoundingMode.UP`if the discarded fraction is \> 0.5; otherwise, behaves as for`RoundingMode.DOWN`.

Example:

| Input Number | Input rounded to one digit with`HALF_DOWN`rounding |
| --- | --- |
| 5.5 | 5 |
| 2.5 | 2 |
| 1.6 | 2 |
| --- | --- |
| 1.1 | 1 |
| 1.0 | 1 |
| -1.0 | -1 |
| --- | --- |
| -1.1 | -1 |
| -1.6 | -2 |
| -2.5 | -2 |
| --- | --- |
| -5.5 | -5 |
|--------------|----------------------------------------------------|

### HALF_EVEN

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val HALF_EVEN : RoundingMode
```

Rounding mode to round towards the "nearest neighbor" unless both neighbors are equidistant, in which case, round towards the even neighbor. Behaves as for`RoundingMode.HALF_UP`if the digit to the left of the discarded fraction is odd; behaves as for`RoundingMode.HALF_DOWN`if it's even. Note that this is the rounding mode that statistically minimizes cumulative error when applied repeatedly over a sequence of calculations. It is sometimes known as "Banker's rounding," and is chiefly used in the USA. This rounding mode is analogous to the rounding policy used for`float`and`double`arithmetic in Java. This mode corresponds to the IEEE 754-2019 rounding-direction attribute roundTiesToEven.

Example:

| Input Number | Input rounded to one digit with`HALF_EVEN`rounding |
| --- | --- |
| 5.5 | 6 |
| 2.5 | 2 |
| 1.6 | 2 |
| --- | --- |
| 1.1 | 1 |
| 1.0 | 1 |
| -1.0 | -1 |
| --- | --- |
| -1.1 | -1 |
| -1.6 | -2 |
| -2.5 | -2 |
| --- | --- |
| -5.5 | -6 |
|--------------|----------------------------------------------------|

### HALF_UP

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val HALF_UP : RoundingMode
```

Rounding mode to round towards "nearest neighbor" unless both neighbors are equidistant, in which case round up. Behaves as for`RoundingMode.UP`if the discarded fraction is ≥ 0.5; otherwise, behaves as for`RoundingMode.DOWN`. Note that this is the rounding mode commonly taught at school. This mode corresponds to the IEEE 754-2019 rounding-direction attribute roundTiesToAway.

Example:

| Input Number | Input rounded to one digit with`HALF_UP`rounding |
| --- | --- |
| 5.5 | 6 |
| 2.5 | 3 |
| 1.6 | 2 |
| --- | --- |
| 1.1 | 1 |
| 1.0 | 1 |
| -1.0 | -1 |
| --- | --- |
| -1.1 | -1 |
| -1.6 | -2 |
| -2.5 | -3 |
| --- | --- |
| -5.5 | -6 |
|--------------|--------------------------------------------------|

### UNNECESSARY

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val UNNECESSARY : RoundingMode
```

Rounding mode to assert that the requested operation has an exact result, hence no rounding is necessary. If this rounding mode is specified on an operation that yields an inexact result, an`ArithmeticException`is thrown.

Example:

| Input Number | Input rounded to one digit with`UNNECESSARY`rounding |
| --- | --- |
| 5.5 | throw`ArithmeticException` |
| 2.5 | throw`ArithmeticException` |
| 1.6 | throw`ArithmeticException` |
| --- | --- |
| 1.1 | throw`ArithmeticException` |
| 1.0 | 1 |
| -1.0 | -1 |
| --- | --- |
| -1.1 | throw`ArithmeticException` |
| -1.6 | throw`ArithmeticException` |
| -2.5 | throw`ArithmeticException` |
| --- | --- |
| -5.5 | throw`ArithmeticException` |
|--------------|------------------------------------------------------|

### UP

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val UP : RoundingMode
```

Rounding mode to round away from zero. Always increments the digit prior to a non-zero discarded fraction. Note that this rounding mode never decreases the magnitude of the calculated value.

Example:

| Input Number | Input rounded to one digit with`UP`rounding |
| --- | --- |
| 5.5 | 6 |
| 2.5 | 3 |
| 1.6 | 2 |
| --- | --- |
| 1.1 | 2 |
| 1.0 | 1 |
| -1.0 | -1 |
| --- | --- |
| -1.1 | -2 |
| -1.6 | -2 |
| -2.5 | -3 |
| --- | --- |
| -5.5 | -6 |
|--------------|---------------------------------------------|

## Public methods

### valueOf

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun valueOf(rm: Int): RoundingMode!
```

Returns the`RoundingMode`object corresponding to a legacy integer rounding mode constant in [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal).

| Parameters ||
|------|--------------------------------------------------------------------------------------------------------------------|
| `rm` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):legacy integer rounding mode to convert |

| Return ||
|-----------------------------------------------------------------------------------------|---------------------------------------------------|
| [RoundingMode](https://developer.android.com/reference/kotlin/java/math/RoundingMode#)! | `RoundingMode`corresponding to the given integer. |

| Exceptions ||
|--------------------------------------|-------------------------|
| `java.lang.IllegalArgumentException` | integer is out of range |
