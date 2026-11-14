# BigDecimal

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BigDecimal

```
open class BigDecimal : Number, Comparable<BigDecimal!>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [kotlin.Number](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-number/index.html) ||
| | ↳ | [java.math.BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal#) |

Immutable, arbitrary-precision signed decimal numbers. A`BigDecimal`consists of an arbitrary precision integer* [unscaled value](https://developer.android.com/reference/kotlin/java/math/BigDecimal#unscaledValue())* and a 32-bit integer* [scale](https://developer.android.com/reference/kotlin/java/math/BigDecimal#scale())* . If zero or positive, the scale is the number of digits to the right of the decimal point. If negative, the unscaled value of the number is multiplied by ten to the power of the negation of the scale. The value of the number represented by the`BigDecimal`is therefore`(unscaledValue × 10-scale)`

The`BigDecimal`class provides operations for arithmetic, scale manipulation, rounding, comparison, hashing, and format conversion. The [toString](https://developer.android.com/reference/kotlin/java/math/BigDecimal#toString())method provides a canonical representation of a`BigDecimal`.

The`BigDecimal`class gives its user complete control over rounding behavior. If no rounding mode is specified and the exact result cannot be represented, an`ArithmeticException`is thrown; otherwise, calculations can be carried out to a chosen precision and rounding mode by supplying an appropriate [MathContext](https://developer.android.com/reference/kotlin/java/math/MathContext) object to the operation. In either case, eight*rounding modes* are provided for the control of rounding. Using the integer fields in this class (such as [ROUND_HALF_UP](https://developer.android.com/reference/kotlin/java/math/BigDecimal#ROUND_HALF_UP:kotlin.Int)) to represent rounding mode is deprecated; the enumeration values of the`RoundingMode``enum`, (such as [RoundingMode.HALF_UP](https://developer.android.com/reference/kotlin/java/math/RoundingMode)) should be used instead.

When a`MathContext`object is supplied with a precision setting of 0 (for example, [MathContext.UNLIMITED](https://developer.android.com/reference/kotlin/java/math/MathContext#UNLIMITED:java.math.MathContext)), arithmetic operations are exact, as are the arithmetic methods which take no`MathContext`object. As a corollary of computing the exact result, the rounding mode setting of a`MathContext`object with a precision setting of 0 is not used and thus irrelevant. In the case of divide, the exact quotient could have an infinitely long decimal expansion; for example, 1 divided by 3. If the quotient has a nonterminating decimal expansion and the operation is specified to return an exact result, an`ArithmeticException`is thrown. Otherwise, the exact result of the division is returned, as done for other operations.

When the precision setting is not 0, the rules of`BigDecimal`arithmetic are broadly compatible with selected modes of operation of the arithmetic defined in ANSI X3.274-1996 and ANSI X3.274-1996/AM 1-2000 (section 7.4). Unlike those standards,`BigDecimal`includes many rounding modes. Any conflicts between these ANSI standards and the`BigDecimal`specification are resolved in favor of`BigDecimal`.

Since the same numerical value can have different representations (with different scales), the rules of arithmetic and rounding must specify both the numerical result and the scale used in the result's representation. The different representations of the same numerical value are called members of the same*cohort* . The [natural order](https://developer.android.com/reference/kotlin/java/math/BigDecimal#compareTo(java.math.BigDecimal))of`BigDecimal`considers members of the same cohort to be equal to each other. In contrast, the [equals](https://developer.android.com/reference/kotlin/java/math/BigDecimal#equals(kotlin.Any))method requires both the numerical value and representation to be the same for equality to hold. The results of methods like [scale()](https://developer.android.com/reference/kotlin/java/math/BigDecimal#scale())and [unscaledValue()](https://developer.android.com/reference/kotlin/java/math/BigDecimal#unscaledValue())will differ for numerically equal values with different representations.

In general the rounding modes and precision setting determine how operations return results with a limited number of digits when the exact result has more digits (perhaps infinitely many in the case of division and square root) than the number of digits returned. First, the total number of digits to return is specified by the`MathContext`'s`precision`setting; this determines the result's*precision*. The digit count starts from the leftmost nonzero digit of the exact result. The rounding mode determines how any discarded trailing digits affect the returned result.

For all arithmetic operators, the operation is carried out as though an exact intermediate result were first calculated and then rounded to the number of digits specified by the precision setting (if necessary), using the selected rounding mode. If the exact result is not returned, some digit positions of the exact result are discarded. When rounding increases the magnitude of the returned result, it is possible for a new digit position to be created by a carry propagating to a leading "9" digit. For example, rounding the value 999.9 to three digits rounding up would be numerically equal to one thousand, represented as 100×101. In such cases, the new "1" is the leading digit position of the returned result.

For methods and constructors with a`MathContext`parameter, if the result is inexact but the rounding mode is [UNNECESSARY](https://developer.android.com/reference/kotlin/java/math/RoundingMode), an`ArithmeticException`will be thrown.

Besides a logical exact result, each arithmetic operation has a preferred scale for representing a result. The preferred scale for each operation is listed in the table below.

| Operation | Preferred Scale of Result |
| --- | --- |
| Add | max(addend.scale(), augend.scale()) |
| Subtract | max(minuend.scale(), subtrahend.scale()) |
| Multiply | multiplier.scale() + multiplicand.scale() |
| --- | --- |
| Divide | dividend.scale() - divisor.scale() |
| Square root | radicand.scale()/2 |
|-------------|-------------------------------------------|

These scales are the ones used by the methods which return exact arithmetic results; except that an exact divide may have to use a larger scale since the exact result may have more digits. For example,`1/32`is`0.03125`.

Before rounding, the scale of the logical exact intermediate result is the preferred scale for that operation. If the exact numerical result cannot be represented in`precision`digits, rounding selects the set of digits to return and the scale of the result is reduced from the scale of the intermediate result to the least scale which can represent the`precision`digits actually returned. If the exact result can be represented with at most`precision`digits, the representation of the result with the scale closest to the preferred scale is returned. In particular, an exactly representable quotient may be represented in fewer than`precision`digits by removing trailing zeros and decreasing the scale. For example, rounding to three digits using the [floor](https://developer.android.com/reference/kotlin/java/math/RoundingMode) rounding mode, 
`19/100 = 0.19 // integer=19, scale=2` 
but 
`21/110 = 0.190 // integer=190, scale=3` 

Note that for add, subtract, and multiply, the reduction in scale will equal the number of digit positions of the exact result which are discarded. If the rounding causes a carry propagation to create a new high-order digit position, an additional digit of the result is discarded than when no new digit position is created.

Other methods may have slightly different rounding semantics. For example, the result of the`pow`method using the [specified algorithm](https://developer.android.com/reference/kotlin/java/math/BigDecimal#pow(kotlin.Int,%20java.math.MathContext))can occasionally differ from the rounded mathematical result by more than one unit in the last place, one* [ulp](https://developer.android.com/reference/kotlin/java/math/BigDecimal#ulp())*.

Two types of operations are provided for manipulating the scale of a`BigDecimal`: scaling/rounding operations and decimal point motion operations. Scaling/rounding operations (#setScale and [round](https://developer.android.com/reference/kotlin/java/math/BigDecimal#round(java.math.MathContext))) return a`BigDecimal`whose value is approximately (or exactly) equal to that of the operand, but whose scale or precision is the specified value; that is, they increase or decrease the precision of the stored number with minimal effect on its value. Decimal point motion operations ([movePointLeft](https://developer.android.com/reference/kotlin/java/math/BigDecimal#movePointLeft(kotlin.Int))and [movePointRight](https://developer.android.com/reference/kotlin/java/math/BigDecimal#movePointRight(kotlin.Int))) return a`BigDecimal`created from the operand by moving the decimal point a specified distance in the specified direction.

As a 32-bit integer, the set of values for the scale is large, but bounded. If the scale of a result would exceed the range of a 32-bit integer, either by overflow or underflow, the operation may throw an`ArithmeticException`.

For the sake of brevity and clarity, pseudo-code is used throughout the descriptions of`BigDecimal`methods. The pseudo-code expression`(i + j)`is shorthand for "a`BigDecimal`whose value is that of the`BigDecimal``i`added to that of the`BigDecimal``j`." The pseudo-code expression`(i == j)`is shorthand for "`true`if and only if the`BigDecimal``i`represents the same value as the`BigDecimal``j`." Other pseudo-code expressions are interpreted similarly. Square brackets are used to represent the particular`BigInteger`and scale pair defining a`BigDecimal`value; for example \[19, 2\] is the`BigDecimal`numerically equal to 0.19 having a scale of 2.

All methods and constructors for this class throw`NullPointerException`when passed a`null`object reference for any input parameter.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ROUND_CEILING](https://developer.android.com/reference/kotlin/java/math/BigDecimal#ROUND_CEILING:kotlin.Int) Rounding mode to round towards positive infinity. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ROUND_DOWN](https://developer.android.com/reference/kotlin/java/math/BigDecimal#ROUND_DOWN:kotlin.Int) Rounding mode to round towards zero. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ROUND_FLOOR](https://developer.android.com/reference/kotlin/java/math/BigDecimal#ROUND_FLOOR:kotlin.Int) Rounding mode to round towards negative infinity. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ROUND_HALF_DOWN](https://developer.android.com/reference/kotlin/java/math/BigDecimal#ROUND_HALF_DOWN:kotlin.Int) Rounding mode to round towards "nearest neighbor" unless both neighbors are equidistant, in which case round down. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ROUND_HALF_EVEN](https://developer.android.com/reference/kotlin/java/math/BigDecimal#ROUND_HALF_EVEN:kotlin.Int) Rounding mode to round towards the "nearest neighbor" unless both neighbors are equidistant, in which case, round towards the even neighbor. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ROUND_HALF_UP](https://developer.android.com/reference/kotlin/java/math/BigDecimal#ROUND_HALF_UP:kotlin.Int) Rounding mode to round towards "nearest neighbor" unless both neighbors are equidistant, in which case round up. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ROUND_UNNECESSARY](https://developer.android.com/reference/kotlin/java/math/BigDecimal#ROUND_UNNECESSARY:kotlin.Int) Rounding mode to assert that the requested operation has an exact result, hence no rounding is necessary. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ROUND_UP](https://developer.android.com/reference/kotlin/java/math/BigDecimal#ROUND_UP:kotlin.Int) Rounding mode to round away from zero. |

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal#BigDecimal(kotlin.CharArray))`(`in:` ` [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!`)` Translates a character array representation of a`BigDecimal`into a`BigDecimal`, accepting the same sequence of characters as the [BigDecimal(java.lang.String)](https://developer.android.com/reference/kotlin/java/math/BigDecimal#BigDecimal(kotlin.String))constructor. |
| [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal#BigDecimal(kotlin.CharArray,%20kotlin.Int,%20kotlin.Int))`(`in:` ` [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!`, `offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `len:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Translates a character array representation of a`BigDecimal`into a`BigDecimal`, accepting the same sequence of characters as the [BigDecimal(java.lang.String)](https://developer.android.com/reference/kotlin/java/math/BigDecimal#BigDecimal(kotlin.String))constructor, while allowing a sub-array to be specified. |
| [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal#BigDecimal(kotlin.CharArray,%20kotlin.Int,%20kotlin.Int,%20java.math.MathContext))`(`in:` ` [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!`, `offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `len:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `mc:` ` [MathContext](https://developer.android.com/reference/kotlin/java/math/MathContext)!`)` Translates a character array representation of a`BigDecimal`into a`BigDecimal`, accepting the same sequence of characters as the [BigDecimal(java.lang.String)](https://developer.android.com/reference/kotlin/java/math/BigDecimal#BigDecimal(kotlin.String))constructor, while allowing a sub-array to be specified and with rounding according to the context settings. |
| [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal#BigDecimal(kotlin.CharArray,%20java.math.MathContext))`(`in:` ` [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!`, `mc:` ` [MathContext](https://developer.android.com/reference/kotlin/java/math/MathContext)!`)` Translates a character array representation of a`BigDecimal`into a`BigDecimal`, accepting the same sequence of characters as the [BigDecimal(java.lang.String)](https://developer.android.com/reference/kotlin/java/math/BigDecimal#BigDecimal(kotlin.String))constructor and with rounding according to the context settings. |
| [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal#BigDecimal(kotlin.Double))`(`val:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`)` Translates a`double`into a`BigDecimal`which is the exact decimal representation of the`double`'s binary floating-point value. |
| [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal#BigDecimal(kotlin.Double,%20java.math.MathContext))`(`val:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`, `mc:` ` [MathContext](https://developer.android.com/reference/kotlin/java/math/MathContext)!`)` Translates a`double`into a`BigDecimal`, with rounding according to the context settings. |
| [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal#BigDecimal(kotlin.Int))`(`val:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Translates an`int`into a`BigDecimal`. |
| [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal#BigDecimal(kotlin.Int,%20java.math.MathContext))`(`val:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `mc:` ` [MathContext](https://developer.android.com/reference/kotlin/java/math/MathContext)!`)` Translates an`int`into a`BigDecimal`, with rounding according to the context settings. |
| [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal#BigDecimal(kotlin.String))`(`val:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Translates the string representation of a`BigDecimal`into a`BigDecimal`. |
| [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal#BigDecimal(kotlin.String,%20java.math.MathContext))`(`val:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `mc:` ` [MathContext](https://developer.android.com/reference/kotlin/java/math/MathContext)!`)` Translates the string representation of a`BigDecimal`into a`BigDecimal`, accepting the same strings as the [BigDecimal(java.lang.String)](https://developer.android.com/reference/kotlin/java/math/BigDecimal#BigDecimal(kotlin.String))constructor, with rounding according to the context settings. |
| [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal#BigDecimal(java.math.BigInteger))`(`val:` ` [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger)!`)` Translates a`BigInteger`into a`BigDecimal`. |
| [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal#BigDecimal(java.math.BigInteger,%20kotlin.Int))`(`unscaledVal:` ` [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger)!`, `scale:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Translates a`BigInteger`unscaled value and an`int`scale into a`BigDecimal`. |
| [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal#BigDecimal(java.math.BigInteger,%20kotlin.Int,%20java.math.MathContext))`(`unscaledVal:` ` [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger)!`, `scale:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `mc:` ` [MathContext](https://developer.android.com/reference/kotlin/java/math/MathContext)!`)` Translates a`BigInteger`unscaled value and an`int`scale into a`BigDecimal`, with rounding according to the context settings. |
| [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal#BigDecimal(java.math.BigInteger,%20java.math.MathContext))`(`val:` ` [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger)!`, `mc:` ` [MathContext](https://developer.android.com/reference/kotlin/java/math/MathContext)!`)` Translates a`BigInteger`into a`BigDecimal`rounding according to the context settings. |
| [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal#BigDecimal(kotlin.Long))`(`val:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Translates a`long`into a`BigDecimal`. |
| [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal#BigDecimal(kotlin.Long,%20java.math.MathContext))`(`val:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `mc:` ` [MathContext](https://developer.android.com/reference/kotlin/java/math/MathContext)!`)` Translates a`long`into a`BigDecimal`, with rounding according to the context settings. |

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal#)! | [abs](https://developer.android.com/reference/kotlin/java/math/BigDecimal#abs())`()` Returns a`BigDecimal`whose value is the absolute value of this`BigDecimal`, and whose scale is`this.scale()`. |
| open [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal#)! | [abs](https://developer.android.com/reference/kotlin/java/math/BigDecimal#abs(java.math.MathContext))`(`mc:` ` [MathContext](https://developer.android.com/reference/kotlin/java/math/MathContext)!`)` Returns a`BigDecimal`whose value is the absolute value of this`BigDecimal`, with rounding according to the context settings. |
| open [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal#)! | [add](https://developer.android.com/reference/kotlin/java/math/BigDecimal#add(java.math.BigDecimal))`(`augend:` ` [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal#)!`)` Returns a`BigDecimal`whose value is`(this + augend)`, and whose scale is`max(this.scale(), augend.scale())`. |
| --- | --- |
| open [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal#)! | [add](https://developer.android.com/reference/kotlin/java/math/BigDecimal#add(java.math.BigDecimal,%20java.math.MathContext))`(`augend:` ` [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal#)!`, `mc:` ` [MathContext](https://developer.android.com/reference/kotlin/java/math/MathContext)!`)` Returns a`BigDecimal`whose value is`(this + augend)`, with rounding according to the context settings. |
| open [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [byteValueExact](https://developer.android.com/reference/kotlin/java/math/BigDecimal#byteValueExact())`()` Converts this`BigDecimal`to a`byte`, checking for lost information. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [compareTo](https://developer.android.com/reference/kotlin/java/math/BigDecimal#compareTo(java.math.BigDecimal))`(`other:` ` [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal#)!`)` Compares this`BigDecimal`numerically with the specified`BigDecimal`. |
| --- | --- |
| open [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal#)! | [divide](https://developer.android.com/reference/kotlin/java/math/BigDecimal#divide(java.math.BigDecimal))`(`divisor:` ` [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal#)!`)` Returns a`BigDecimal`whose value is`(this / divisor)`, and whose preferred scale is`(this.scale() - divisor.scale())`; if the exact quotient cannot be represented (because it has a non-terminating decimal expansion) an`ArithmeticException`is thrown. |
| open [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal#)! | [divide](https://developer.android.com/reference/kotlin/java/math/BigDecimal#divide(java.math.BigDecimal,%20kotlin.Int))`(`divisor:` ` [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal#)!`, `roundingMode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns a`BigDecimal`whose value is`(this / divisor)`, and whose scale is`this.scale()`. |
| open [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal#)! | [divide](https://developer.android.com/reference/kotlin/java/math/BigDecimal#divide(java.math.BigDecimal,%20kotlin.Int,%20kotlin.Int))`(`divisor:` ` [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal#)!`, `scale:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `roundingMode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns a`BigDecimal`whose value is`(this / divisor)`, and whose scale is as specified. |
| --- | --- |
| open [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal#)! | [divide](https://developer.android.com/reference/kotlin/java/math/BigDecimal#divide(java.math.BigDecimal,%20kotlin.Int,%20java.math.RoundingMode))`(`divisor:` ` [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal#)!`, `scale:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `roundingMode:` ` [RoundingMode](https://developer.android.com/reference/kotlin/java/math/RoundingMode)!`)` Returns a`BigDecimal`whose value is`(this / divisor)`, and whose scale is as specified. |
| open [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal#)! | [divide](https://developer.android.com/reference/kotlin/java/math/BigDecimal#divide(java.math.BigDecimal,%20java.math.MathContext))`(`divisor:` ` [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal#)!`, `mc:` ` [MathContext](https://developer.android.com/reference/kotlin/java/math/MathContext)!`)` Returns a`BigDecimal`whose value is`(this / divisor)`, with rounding according to the context settings. |
| open [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal#)! | [divide](https://developer.android.com/reference/kotlin/java/math/BigDecimal#divide(java.math.BigDecimal,%20java.math.RoundingMode))`(`divisor:` ` [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal#)!`, `roundingMode:` ` [RoundingMode](https://developer.android.com/reference/kotlin/java/math/RoundingMode)!`)` Returns a`BigDecimal`whose value is`(this / divisor)`, and whose scale is`this.scale()`. |
| --- | --- |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal#)!\>! | [divideAndRemainder](https://developer.android.com/reference/kotlin/java/math/BigDecimal#divideAndRemainder(java.math.BigDecimal))`(`divisor:` ` [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal#)!`)` Returns a two-element`BigDecimal`array containing the result of`divideToIntegralValue`followed by the result of`remainder`on the two operands. |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal#)!\>! | [divideAndRemainder](https://developer.android.com/reference/kotlin/java/math/BigDecimal#divideAndRemainder(java.math.BigDecimal,%20java.math.MathContext))`(`divisor:` ` [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal#)!`, `mc:` ` [MathContext](https://developer.android.com/reference/kotlin/java/math/MathContext)!`)` Returns a two-element`BigDecimal`array containing the result of`divideToIntegralValue`followed by the result of`remainder`on the two operands calculated with rounding according to the context settings. |
| open [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal#)! | [divideToIntegralValue](https://developer.android.com/reference/kotlin/java/math/BigDecimal#divideToIntegralValue(java.math.BigDecimal))`(`divisor:` ` [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal#)!`)` Returns a`BigDecimal`whose value is the integer part of the quotient`(this / divisor)`rounded down. |
| --- | --- |
| open [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal#)! | [divideToIntegralValue](https://developer.android.com/reference/kotlin/java/math/BigDecimal#divideToIntegralValue(java.math.BigDecimal,%20java.math.MathContext))`(`divisor:` ` [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal#)!`, `mc:` ` [MathContext](https://developer.android.com/reference/kotlin/java/math/MathContext)!`)` Returns a`BigDecimal`whose value is the integer part of`(this / divisor)`. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/java/math/BigDecimal#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Compares this`BigDecimal`with the specified`Object`for equality. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/java/math/BigDecimal#hashCode())`()` Returns the hash code for this`BigDecimal`. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [intValueExact](https://developer.android.com/reference/kotlin/java/math/BigDecimal#intValueExact())`()` Converts this`BigDecimal`to an`int`, checking for lost information. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [longValueExact](https://developer.android.com/reference/kotlin/java/math/BigDecimal#longValueExact())`()` Converts this`BigDecimal`to a`long`, checking for lost information. |
| open [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal#)! | [max](https://developer.android.com/reference/kotlin/java/math/BigDecimal#max(java.math.BigDecimal))`(`val:` ` [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal#)!`)` Returns the maximum of this`BigDecimal`and`val`. |
| --- | --- |
| open [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal#)! | [min](https://developer.android.com/reference/kotlin/java/math/BigDecimal#min(java.math.BigDecimal))`(`val:` ` [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal#)!`)` Returns the minimum of this`BigDecimal`and`val`. |
| open [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal#)! | [movePointLeft](https://developer.android.com/reference/kotlin/java/math/BigDecimal#movePointLeft(kotlin.Int))`(`n:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns a`BigDecimal`which is equivalent to this one with the decimal point moved`n`places to the left. |
| open [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal#)! | [movePointRight](https://developer.android.com/reference/kotlin/java/math/BigDecimal#movePointRight(kotlin.Int))`(`n:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns a`BigDecimal`which is equivalent to this one with the decimal point moved`n`places to the right. |
| --- | --- |
| open [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal#)! | [multiply](https://developer.android.com/reference/kotlin/java/math/BigDecimal#multiply(java.math.BigDecimal))`(`multiplicand:` ` [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal#)!`)` Returns a`BigDecimal`whose value is`(this × multiplicand)`, and whose scale is`(this.scale() + multiplicand.scale())`. |
| open [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal#)! | [multiply](https://developer.android.com/reference/kotlin/java/math/BigDecimal#multiply(java.math.BigDecimal,%20java.math.MathContext))`(`multiplicand:` ` [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal#)!`, `mc:` ` [MathContext](https://developer.android.com/reference/kotlin/java/math/MathContext)!`)` Returns a`BigDecimal`whose value is`(this × multiplicand)`, with rounding according to the context settings. |
| open [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal#)! | [negate](https://developer.android.com/reference/kotlin/java/math/BigDecimal#negate())`()` Returns a`BigDecimal`whose value is`(-this)`, and whose scale is`this.scale()`. |
| --- | --- |
| open [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal#)! | [negate](https://developer.android.com/reference/kotlin/java/math/BigDecimal#negate(java.math.MathContext))`(`mc:` ` [MathContext](https://developer.android.com/reference/kotlin/java/math/MathContext)!`)` Returns a`BigDecimal`whose value is`(-this)`, with rounding according to the context settings. |
| open [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal#)! | [plus](https://developer.android.com/reference/kotlin/java/math/BigDecimal#plus())`()` Returns a`BigDecimal`whose value is`(+this)`, and whose scale is`this.scale()`. |
| open [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal#)! | [plus](https://developer.android.com/reference/kotlin/java/math/BigDecimal#plus(java.math.MathContext))`(`mc:` ` [MathContext](https://developer.android.com/reference/kotlin/java/math/MathContext)!`)` Returns a`BigDecimal`whose value is`(+this)`, with rounding according to the context settings. |
| --- | --- |
| open [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal#)! | [pow](https://developer.android.com/reference/kotlin/java/math/BigDecimal#pow(kotlin.Int))`(`n:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns a`BigDecimal`whose value is`(thisn)`, The power is computed exactly, to unlimited precision. |
| open [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal#)! | [pow](https://developer.android.com/reference/kotlin/java/math/BigDecimal#pow(kotlin.Int,%20java.math.MathContext))`(`n:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `mc:` ` [MathContext](https://developer.android.com/reference/kotlin/java/math/MathContext)!`)` Returns a`BigDecimal`whose value is`(thisn)`. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [precision](https://developer.android.com/reference/kotlin/java/math/BigDecimal#precision())`()` Returns the*precision* of this`BigDecimal`. |
| --- | --- |
| open [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal#)! | [remainder](https://developer.android.com/reference/kotlin/java/math/BigDecimal#remainder(java.math.BigDecimal))`(`divisor:` ` [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal#)!`)` Returns a`BigDecimal`whose value is`(this % divisor)`. |
| open [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal#)! | [remainder](https://developer.android.com/reference/kotlin/java/math/BigDecimal#remainder(java.math.BigDecimal,%20java.math.MathContext))`(`divisor:` ` [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal#)!`, `mc:` ` [MathContext](https://developer.android.com/reference/kotlin/java/math/MathContext)!`)` Returns a`BigDecimal`whose value is`(this % divisor)`, with rounding according to the context settings. |
| open [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal#)! | [round](https://developer.android.com/reference/kotlin/java/math/BigDecimal#round(java.math.MathContext))`(`mc:` ` [MathContext](https://developer.android.com/reference/kotlin/java/math/MathContext)!`)` Returns a`BigDecimal`rounded according to the`MathContext`settings. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [scale](https://developer.android.com/reference/kotlin/java/math/BigDecimal#scale())`()` Returns the*scale* of this`BigDecimal`. |
| open [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal#)! | [scaleByPowerOfTen](https://developer.android.com/reference/kotlin/java/math/BigDecimal#scaleByPowerOfTen(kotlin.Int))`(`n:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns a BigDecimal whose numerical value is equal to (`this`\* 10n). |
| open [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal#)! | [setScale](https://developer.android.com/reference/kotlin/java/math/BigDecimal#setScale(kotlin.Int))`(`newScale:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns a`BigDecimal`whose scale is the specified value, and whose value is numerically equal to this`BigDecimal`'s. |
| --- | --- |
| open [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal#)! | [setScale](https://developer.android.com/reference/kotlin/java/math/BigDecimal#setScale(kotlin.Int,%20kotlin.Int))`(`newScale:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `roundingMode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns a`BigDecimal`whose scale is the specified value, and whose unscaled value is determined by multiplying or dividing this`BigDecimal`'s unscaled value by the appropriate power of ten to maintain its overall value. |
| open [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal#)! | [setScale](https://developer.android.com/reference/kotlin/java/math/BigDecimal#setScale(kotlin.Int,%20java.math.RoundingMode))`(`newScale:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `roundingMode:` ` [RoundingMode](https://developer.android.com/reference/kotlin/java/math/RoundingMode)!`)` Returns a`BigDecimal`whose scale is the specified value, and whose unscaled value is determined by multiplying or dividing this`BigDecimal`'s unscaled value by the appropriate power of ten to maintain its overall value. |
| open [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [shortValueExact](https://developer.android.com/reference/kotlin/java/math/BigDecimal#shortValueExact())`()` Converts this`BigDecimal`to a`short`, checking for lost information. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [signum](https://developer.android.com/reference/kotlin/java/math/BigDecimal#signum())`()` Returns the signum function of this`BigDecimal`. |
| open [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal#)! | [sqrt](https://developer.android.com/reference/kotlin/java/math/BigDecimal#sqrt(java.math.MathContext))`(`mc:` ` [MathContext](https://developer.android.com/reference/kotlin/java/math/MathContext)!`)` Returns an approximation to the square root of`this`with rounding according to the context settings. |
| open [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal#)! | [stripTrailingZeros](https://developer.android.com/reference/kotlin/java/math/BigDecimal#stripTrailingZeros())`()` Returns a`BigDecimal`which is numerically equal to this one but with any trailing zeros removed from the representation. |
| --- | --- |
| open [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal#)! | [subtract](https://developer.android.com/reference/kotlin/java/math/BigDecimal#subtract(java.math.BigDecimal))`(`subtrahend:` ` [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal#)!`)` Returns a`BigDecimal`whose value is`(this - subtrahend)`, and whose scale is`max(this.scale(), subtrahend.scale())`. |
| open [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal#)! | [subtract](https://developer.android.com/reference/kotlin/java/math/BigDecimal#subtract(java.math.BigDecimal,%20java.math.MathContext))`(`subtrahend:` ` [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal#)!`, `mc:` ` [MathContext](https://developer.android.com/reference/kotlin/java/math/MathContext)!`)` Returns a`BigDecimal`whose value is`(this - subtrahend)`, with rounding according to the context settings. |
| open [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger)! | [toBigInteger](https://developer.android.com/reference/kotlin/java/math/BigDecimal#toBigInteger())`()` Converts this`BigDecimal`to a`BigInteger`. |
| --- | --- |
| open [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger)! | [toBigIntegerExact](https://developer.android.com/reference/kotlin/java/math/BigDecimal#toBigIntegerExact())`()` Converts this`BigDecimal`to a`BigInteger`, checking for lost information. |
| open [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [toDouble](https://developer.android.com/reference/kotlin/java/math/BigDecimal#toDouble())`()` Converts this`BigDecimal`to a`double`. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [toEngineeringString](https://developer.android.com/reference/kotlin/java/math/BigDecimal#toEngineeringString())`()` Returns a string representation of this`BigDecimal`, using engineering notation if an exponent is needed. |
| --- | --- |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [toFloat](https://developer.android.com/reference/kotlin/java/math/BigDecimal#toFloat())`()` Converts this`BigDecimal`to a`float`. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [toInt](https://developer.android.com/reference/kotlin/java/math/BigDecimal#toInt())`()` Converts this`BigDecimal`to an`int`. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [toLong](https://developer.android.com/reference/kotlin/java/math/BigDecimal#toLong())`()` Converts this`BigDecimal`to a`long`. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [toPlainString](https://developer.android.com/reference/kotlin/java/math/BigDecimal#toPlainString())`()` Returns a string representation of this`BigDecimal`without an exponent field. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/java/math/BigDecimal#toString())`()` Returns the string representation of this`BigDecimal`, using scientific notation if an exponent is needed. |
| open [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal#)! | [ulp](https://developer.android.com/reference/kotlin/java/math/BigDecimal#ulp())`()` Returns the size of an ulp, a unit in the last place, of this`BigDecimal`. |
| --- | --- |
| open [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger)! | [unscaledValue](https://developer.android.com/reference/kotlin/java/math/BigDecimal#unscaledValue())`()` Returns a`BigInteger`whose value is the*unscaled value* of this`BigDecimal`. |
| openstatic [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal#)! | [valueOf](https://developer.android.com/reference/kotlin/java/math/BigDecimal#valueOf(kotlin.Double))`(`val:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`)` Translates a`double`into a`BigDecimal`, using the`double`'s canonical string representation provided by the [Double.toString(double)](https://developer.android.com/reference/kotlin/java/lang/Double.html#toString(kotlin.Double))method. |
| openstatic [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal#)! | [valueOf](https://developer.android.com/reference/kotlin/java/math/BigDecimal#valueOf(kotlin.Long))`(`val:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Translates a`long`value into a`BigDecimal`with a scale of zero. |
| --- | --- |
| openstatic [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal#)! | [valueOf](https://developer.android.com/reference/kotlin/java/math/BigDecimal#valueOf(kotlin.Long,%20kotlin.Int))`(`unscaledVal:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `scale:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Translates a`long`unscaled value and an`int`scale into a`BigDecimal`. |

| Properties ||
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| static [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal#)! | [ONE](https://developer.android.com/reference/kotlin/java/math/BigDecimal#ONE:java.math.BigDecimal) The value 1, with a scale of 0. |
| static [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal#)! | [TEN](https://developer.android.com/reference/kotlin/java/math/BigDecimal#TEN:java.math.BigDecimal) The value 10, with a scale of 0. |
| static [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal#)! | [ZERO](https://developer.android.com/reference/kotlin/java/math/BigDecimal#ZERO:java.math.BigDecimal) The value 0, with a scale of 0. |
| --- | --- |

## Constants

### ROUND_CEILING

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ROUND_CEILING: Int
```

**Deprecated:** *Use [RoundingMode.CEILING](https://developer.android.com/reference/kotlin/java/math/RoundingMode) instead.*

Rounding mode to round towards positive infinity. If the`BigDecimal`is positive, behaves as for`ROUND_UP`; if negative, behaves as for`ROUND_DOWN`. Note that this rounding mode never decreases the calculated value. 

 Value: 2

### ROUND_DOWN

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ROUND_DOWN: Int
```

**Deprecated:** *Use [RoundingMode.DOWN](https://developer.android.com/reference/kotlin/java/math/RoundingMode) instead.*

Rounding mode to round towards zero. Never increments the digit prior to a discarded fraction (i.e., truncates). Note that this rounding mode never increases the magnitude of the calculated value. 

 Value: 1

### ROUND_FLOOR

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ROUND_FLOOR: Int
```

**Deprecated:** *Use [RoundingMode.FLOOR](https://developer.android.com/reference/kotlin/java/math/RoundingMode) instead.*

Rounding mode to round towards negative infinity. If the`BigDecimal`is positive, behave as for`ROUND_DOWN`; if negative, behave as for`ROUND_UP`. Note that this rounding mode never increases the calculated value. 

 Value: 3

### ROUND_HALF_DOWN

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ROUND_HALF_DOWN: Int
```

**Deprecated:** *Use [RoundingMode.HALF_DOWN](https://developer.android.com/reference/kotlin/java/math/RoundingMode) instead.*

Rounding mode to round towards "nearest neighbor" unless both neighbors are equidistant, in which case round down. Behaves as for`ROUND_UP`if the discarded fraction is \> 0.5; otherwise, behaves as for`ROUND_DOWN`. 

 Value: 5

### ROUND_HALF_EVEN

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ROUND_HALF_EVEN: Int
```

**Deprecated:** *Use [RoundingMode.HALF_EVEN](https://developer.android.com/reference/kotlin/java/math/RoundingMode) instead.*

Rounding mode to round towards the "nearest neighbor" unless both neighbors are equidistant, in which case, round towards the even neighbor. Behaves as for`ROUND_HALF_UP`if the digit to the left of the discarded fraction is odd; behaves as for`ROUND_HALF_DOWN`if it's even. Note that this is the rounding mode that minimizes cumulative error when applied repeatedly over a sequence of calculations. 

 Value: 6

### ROUND_HALF_UP

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ROUND_HALF_UP: Int
```

**Deprecated:** *Use [RoundingMode.HALF_UP](https://developer.android.com/reference/kotlin/java/math/RoundingMode) instead.*

Rounding mode to round towards "nearest neighbor" unless both neighbors are equidistant, in which case round up. Behaves as for`ROUND_UP`if the discarded fraction is ≥ 0.5; otherwise, behaves as for`ROUND_DOWN`. Note that this is the rounding mode that most of us were taught in grade school. 

 Value: 4

### ROUND_UNNECESSARY

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ROUND_UNNECESSARY: Int
```

**Deprecated:** *Use [RoundingMode.UNNECESSARY](https://developer.android.com/reference/kotlin/java/math/RoundingMode) instead.*

Rounding mode to assert that the requested operation has an exact result, hence no rounding is necessary. If this rounding mode is specified on an operation that yields an inexact result, an`ArithmeticException`is thrown. 

 Value: 7

### ROUND_UP

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ROUND_UP: Int
```

**Deprecated:** *Use [RoundingMode.UP](https://developer.android.com/reference/kotlin/java/math/RoundingMode) instead.*

Rounding mode to round away from zero. Always increments the digit prior to a nonzero discarded fraction. Note that this rounding mode never decreases the magnitude of the calculated value. 

 Value: 0

## Public constructors

### BigDecimal

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
BigDecimal(in: CharArray!)
```

Translates a character array representation of a`BigDecimal`into a`BigDecimal`, accepting the same sequence of characters as the [BigDecimal(java.lang.String)](https://developer.android.com/reference/kotlin/java/math/BigDecimal#BigDecimal(kotlin.String))constructor.

| Parameters ||
|------|----------------------------------------------------------------------------------------------------------------------------------------|
| `in` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!:`char`array that is the source of characters. |

| Exceptions ||
|-----------------------------------|-------------------------------------------------------|
| `java.lang.NumberFormatException` | if`in`is not a valid representation of a`BigDecimal`. |

### BigDecimal

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
BigDecimal(
    in: CharArray!, 
    offset: Int, 
    len: Int)
```

Translates a character array representation of a`BigDecimal`into a`BigDecimal`, accepting the same sequence of characters as the [BigDecimal(java.lang.String)](https://developer.android.com/reference/kotlin/java/math/BigDecimal#BigDecimal(kotlin.String))constructor, while allowing a sub-array to be specified.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------|
| `in` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!:`char`array that is the source of characters. |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):first character in the array to inspect. |
| `len` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):number of characters to consider. |
| --- | --- |

| Exceptions ||
|-----------------------------------|-------------------------------------------------------------------------------------------------------|
| `java.lang.NumberFormatException` | if`in`is not a valid representation of a`BigDecimal`or the defined subarray is not wholly within`in`. |

### BigDecimal

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
BigDecimal(
    in: CharArray!, 
    offset: Int, 
    len: Int, 
    mc: MathContext!)
```

Translates a character array representation of a`BigDecimal`into a`BigDecimal`, accepting the same sequence of characters as the [BigDecimal(java.lang.String)](https://developer.android.com/reference/kotlin/java/math/BigDecimal#BigDecimal(kotlin.String))constructor, while allowing a sub-array to be specified and with rounding according to the context settings.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------|
| `in` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!:`char`array that is the source of characters. |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):first character in the array to inspect. |
| `len` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):number of characters to consider. |
| --- | --- |
| `mc` | [MathContext](https://developer.android.com/reference/kotlin/java/math/MathContext)!:the context to use. |

| Exceptions ||
|-----------------------------------|-------------------------------------------------------------------------------------------------------|
| `java.lang.NumberFormatException` | if`in`is not a valid representation of a`BigDecimal`or the defined subarray is not wholly within`in`. |

### BigDecimal

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
BigDecimal(
    in: CharArray!, 
    mc: MathContext!)
```

Translates a character array representation of a`BigDecimal`into a`BigDecimal`, accepting the same sequence of characters as the [BigDecimal(java.lang.String)](https://developer.android.com/reference/kotlin/java/math/BigDecimal#BigDecimal(kotlin.String))constructor and with rounding according to the context settings.

| Parameters ||
|------|----------------------------------------------------------------------------------------------------------------------------------------|
| `in` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!:`char`array that is the source of characters. |
| `mc` | [MathContext](https://developer.android.com/reference/kotlin/java/math/MathContext)!:the context to use. |

| Exceptions ||
|-----------------------------------|-------------------------------------------------------|
| `java.lang.NumberFormatException` | if`in`is not a valid representation of a`BigDecimal`. |

### BigDecimal

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
BigDecimal(val: Double)
```

Translates a`double`into a`BigDecimal`which is the exact decimal representation of the`double`'s binary floating-point value. The scale of the returned`BigDecimal`is the smallest value such that`(10scale × val)`is an integer.

**Notes:**

1. The results of this constructor can be somewhat unpredictable. One might assume that writing`new BigDecimal(0.1)`in Java creates a`BigDecimal`which is exactly equal to 0.1 (an unscaled value of 1, with a scale of 1), but it is actually equal to 0.1000000000000000055511151231257827021181583404541015625. This is because 0.1 cannot be represented exactly as a`double`(or, for that matter, as a binary fraction of any finite length). Thus, the value that is being passed*in*to the constructor is not exactly equal to 0.1, appearances notwithstanding.
2. The`String`constructor, on the other hand, is perfectly predictable: writing`new BigDecimal("0.1")`creates a`BigDecimal`which is*exactly* equal to 0.1, as one would expect. Therefore, it is generally recommended that the [String constructor](https://developer.android.com/reference/kotlin/java/math/BigDecimal#BigDecimal(kotlin.String))be used in preference to this one.
3. When a`double`must be used as a source for a`BigDecimal`, note that this constructor provides an exact conversion; it does not give the same result as converting the`double`to a`String`using the [Double.toString(double)](https://developer.android.com/reference/kotlin/java/lang/Double.html#toString(kotlin.Double))method and then using the [BigDecimal(java.lang.String)](https://developer.android.com/reference/kotlin/java/math/BigDecimal#BigDecimal(kotlin.String))constructor. To get that result, use the`static` [valueOf(double)](https://developer.android.com/reference/kotlin/java/math/BigDecimal#valueOf(kotlin.Double))method.

| Parameters ||
|-------|--------------------------------------------------------------------------------------------------------------------------------|
| `val` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html):`double`value to be converted to`BigDecimal`. |

| Exceptions ||
|-----------------------------------|----------------------------|
| `java.lang.NumberFormatException` | if`val`is infinite or NaN. |

### BigDecimal

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
BigDecimal(
    val: Double, 
    mc: MathContext!)
```

Translates a`double`into a`BigDecimal`, with rounding according to the context settings. The scale of the`BigDecimal`is the smallest value such that`(10scale × val)`is an integer.

The results of this constructor can be somewhat unpredictable and its use is generally not recommended; see the notes under the [BigDecimal(double)](https://developer.android.com/reference/kotlin/java/math/BigDecimal#BigDecimal(kotlin.Double))constructor.

| Parameters ||
|-------|--------------------------------------------------------------------------------------------------------------------------------|
| `val` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html):`double`value to be converted to`BigDecimal`. |
| `mc` | [MathContext](https://developer.android.com/reference/kotlin/java/math/MathContext)!:the context to use. |

| Exceptions ||
|-----------------------------------|----------------------------|
| `java.lang.NumberFormatException` | if`val`is infinite or NaN. |

### BigDecimal

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
BigDecimal(val: Int)
```

Translates an`int`into a`BigDecimal`. The scale of the`BigDecimal`is zero.

| Parameters ||
|-------|-----------------------------------------------------------------------------------------------------------------------|
| `val` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):`int`value to be converted to`BigDecimal`. |

### BigDecimal

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
BigDecimal(
    val: Int, 
    mc: MathContext!)
```

Translates an`int`into a`BigDecimal`, with rounding according to the context settings. The scale of the`BigDecimal`, before any rounding, is zero.

| Parameters ||
|-------|-----------------------------------------------------------------------------------------------------------------------|
| `val` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):`int`value to be converted to`BigDecimal`. |
| `mc` | [MathContext](https://developer.android.com/reference/kotlin/java/math/MathContext)!:the context to use. |

### BigDecimal

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
BigDecimal(val: String!)
```

Translates the string representation of a`BigDecimal`into a`BigDecimal`. The string representation consists of an optional sign,`'+'`(` '\u002B'`) or`'-'`(`'\u002D'`), followed by a sequence of zero or more decimal digits ("the integer"), optionally followed by a fraction, optionally followed by an exponent.

The fraction consists of a decimal point followed by zero or more decimal digits. The string must contain at least one digit in either the integer or the fraction. The number formed by the sign, the integer and the fraction is referred to as the*significand*.

The exponent consists of the character`'e'`(`'\u0065'`) or`'E'`(`'\u0045'`) followed by one or more decimal digits. The value of the exponent must lie between - [Integer.MAX_VALUE](https://developer.android.com/reference/kotlin/java/lang/Integer.html#MAX_VALUE:kotlin.Int)([java.lang.Integer#MIN_VALUE](https://developer.android.com/reference/kotlin/java/lang/Integer.html#MIN_VALUE:kotlin.Int)+1) and [Integer.MAX_VALUE](https://developer.android.com/reference/kotlin/java/lang/Integer.html#MAX_VALUE:kotlin.Int), inclusive.

More formally, the strings this constructor accepts are described by the following grammar:

*BigDecimalString:*
: *Signopt Significand Exponentopt*

*Sign:*
: `+`
: `-`

*Significand:*
: *IntegerPart* `.`*FractionPartopt*
: `.`*FractionPart*
: *IntegerPart*

*IntegerPart:*
: *Digits*

*FractionPart:*
: *Digits*

*Exponent:*
: *ExponentIndicator SignedInteger*

*ExponentIndicator:*
: `e`
: `E`

*SignedInteger:*
: *Signopt Digits*

*Digits:*
: *Digit*
: *Digits Digit*

*Digit:*
: any character for which java.lang.Character#isDigit returns`true`, including 0, 1, 2 ...

The scale of the returned`BigDecimal`will be the number of digits in the fraction, or zero if the string contains no decimal point, subject to adjustment for any exponent; if the string contains an exponent, the exponent is subtracted from the scale. The value of the resulting scale must lie between`Integer.MIN_VALUE`and`Integer.MAX_VALUE`, inclusive.

The character-to-digit mapping is provided by java.lang.Character#digit set to convert to radix 10. The String may not contain any extraneous characters (whitespace, for example).

**Examples:** 
The value of the returned`BigDecimal`is equal to*significand* × 10*exponent* . For each string on the left, the resulting representation \[`BigInteger`,`scale`\] is shown on the right. 

```kotlin
"0"            [0,0]
  "0.00"         [0,2]
  "123"          [123,0]
  "-123"         [-123,0]
  "1.23E3"       [123,-1]
  "1.23E+3"      [123,-1]
  "12.3E+7"      [123,-6]
  "12.0"         [120,1]
  "12.3"         [123,1]
  "0.00123"      [123,5]
  "-1.23E-12"    [-123,14]
  "1234.5E-4"    [12345,5]
  "0E+7"         [0,-7]
  "-0"           [0,0]
  
```

| Parameters ||
|-------|-------------------------------------------------------------------------------------------------------------------------|
| `val` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:String representation of`BigDecimal`. |

| Exceptions ||
|-----------------------------------|--------------------------------------------------------|
| `java.lang.NumberFormatException` | if`val`is not a valid representation of a`BigDecimal`. |

### BigDecimal

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
BigDecimal(
    val: String!, 
    mc: MathContext!)
```

Translates the string representation of a`BigDecimal`into a`BigDecimal`, accepting the same strings as the [BigDecimal(java.lang.String)](https://developer.android.com/reference/kotlin/java/math/BigDecimal#BigDecimal(kotlin.String))constructor, with rounding according to the context settings.

| Parameters ||
|-------|---------------------------------------------------------------------------------------------------------------------------|
| `val` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:string representation of a`BigDecimal`. |
| `mc` | [MathContext](https://developer.android.com/reference/kotlin/java/math/MathContext)!:the context to use. |

| Exceptions ||
|-----------------------------------|-------------------------------------------------------|
| `java.lang.NumberFormatException` | if`val`is not a valid representation of a BigDecimal. |

### BigDecimal

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
BigDecimal(val: BigInteger!)
```

Translates a`BigInteger`into a`BigDecimal`. The scale of the`BigDecimal`is zero.

| Parameters ||
|-------|--------------------------------------------------------------------------------------------------------------------------------------|
| `val` | [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger)!:`BigInteger`value to be converted to`BigDecimal`. |

### BigDecimal

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
BigDecimal(
    unscaledVal: BigInteger!, 
    scale: Int)
```

Translates a`BigInteger`unscaled value and an`int`scale into a`BigDecimal`. The value of the`BigDecimal`is`(unscaledVal × 10-scale)`.

| Parameters ||
|---------------|-----------------------------------------------------------------------------------------------------------------------|
| `unscaledVal` | [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger)!:unscaled value of the`BigDecimal`. |
| `scale` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):scale of the`BigDecimal`. |

### BigDecimal

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
BigDecimal(
    unscaledVal: BigInteger!, 
    scale: Int, 
    mc: MathContext!)
```

Translates a`BigInteger`unscaled value and an`int`scale into a`BigDecimal`, with rounding according to the context settings. The value of the`BigDecimal`is`(unscaledVal × 10-scale)`, rounded according to the`precision`and rounding mode settings.

| Parameters ||
|---------------|-----------------------------------------------------------------------------------------------------------------------|
| `unscaledVal` | [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger)!:unscaled value of the`BigDecimal`. |
| `scale` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):scale of the`BigDecimal`. |
| `mc` | [MathContext](https://developer.android.com/reference/kotlin/java/math/MathContext)!:the context to use. |
| --- | --- |

### BigDecimal

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
BigDecimal(
    val: BigInteger!, 
    mc: MathContext!)
```

Translates a`BigInteger`into a`BigDecimal`rounding according to the context settings. The scale of the`BigDecimal`is zero.

| Parameters ||
|-------|--------------------------------------------------------------------------------------------------------------------------------------|
| `val` | [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger)!:`BigInteger`value to be converted to`BigDecimal`. |
| `mc` | [MathContext](https://developer.android.com/reference/kotlin/java/math/MathContext)!:the context to use. |

### BigDecimal

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
BigDecimal(val: Long)
```

Translates a`long`into a`BigDecimal`. The scale of the`BigDecimal`is zero.

| Parameters ||
|-------|--------------------------------------------------------------------------------------------------------------------------|
| `val` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):`long`value to be converted to`BigDecimal`. |

### BigDecimal

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
BigDecimal(
    val: Long, 
    mc: MathContext!)
```

Translates a`long`into a`BigDecimal`, with rounding according to the context settings. The scale of the`BigDecimal`, before any rounding, is zero.

| Parameters ||
|-------|--------------------------------------------------------------------------------------------------------------------------|
| `val` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):`long`value to be converted to`BigDecimal`. |
| `mc` | [MathContext](https://developer.android.com/reference/kotlin/java/math/MathContext)!:the context to use. |

## Public methods

### abs

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun abs(): BigDecimal!
```

Returns a`BigDecimal`whose value is the absolute value of this`BigDecimal`, and whose scale is`this.scale()`.

| Return ||
|-------------------------------------------------------------------------------------|-------------|
| [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal#)! | `abs(this)` |

### abs

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun abs(mc: MathContext!): BigDecimal!
```

Returns a`BigDecimal`whose value is the absolute value of this`BigDecimal`, with rounding according to the context settings.

| Parameters ||
|------|----------------------------------------------------------------------------------------------------------|
| `mc` | [MathContext](https://developer.android.com/reference/kotlin/java/math/MathContext)!:the context to use. |

| Return ||
|-------------------------------------------------------------------------------------|------------------------------------|
| [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal#)! | `abs(this)`, rounded as necessary. |

### add

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun add(augend: BigDecimal!): BigDecimal!
```

Returns a`BigDecimal`whose value is`(this + augend)`, and whose scale is`max(this.scale(), augend.scale())`.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------|
| `augend` | [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal#)!:value to be added to this`BigDecimal`. |

| Return ||
|-------------------------------------------------------------------------------------|-----------------|
| [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal#)! | `this + augend` |

### add

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun add(
    augend: BigDecimal!, 
    mc: MathContext!
): BigDecimal!
```

Returns a`BigDecimal`whose value is`(this + augend)`, with rounding according to the context settings. If either number is zero and the precision setting is nonzero then the other number, rounded if necessary, is used as the result.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------|
| `augend` | [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal#)!:value to be added to this`BigDecimal`. |
| `mc` | [MathContext](https://developer.android.com/reference/kotlin/java/math/MathContext)!:the context to use. |

| Return ||
|-------------------------------------------------------------------------------------|----------------------------------------|
| [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal#)! | `this + augend`, rounded as necessary. |

### byteValueExact

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun byteValueExact(): Byte
```

Converts this`BigDecimal`to a`byte`, checking for lost information. If this`BigDecimal`has a nonzero fractional part or is out of the possible range for a`byte`result then an`ArithmeticException`is thrown.

| Return ||
|------------------------------------------------------------------------------|---------------------------------------|
| [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | this`BigDecimal`converted to a`byte`. |

| Exceptions ||
|---------------------------------|--------------------------------------------------------------------|
| `java.lang.ArithmeticException` | if`this`has a nonzero fractional part, or will not fit in a`byte`. |

### compareTo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun compareTo(other: BigDecimal!): Int
```

Compares this`BigDecimal`numerically with the specified`BigDecimal`. Two`BigDecimal`objects that are equal in value but have a different scale (like 2.0 and 2.00) are considered equal by this method. Such values are in the same*cohort* . This method is provided in preference to individual methods for each of the six boolean comparison operators (\<, ==, \>, \>=, !=, \<=). The suggested idiom for performing these comparisons is:`(x.compareTo(y)`\<*op* \>`0)`, where \<*op*\> is one of the six comparison operators.

| Parameters ||
|-------|---------------------------------------------------------|
| `o` | the object to be compared. |
| `val` | `BigDecimal`to which this`BigDecimal`is to be compared. |

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | -1, 0, or 1 as this`BigDecimal`is numerically less than, equal to, or greater than`val`. |

| Exceptions ||
|----------------------------------|--------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if the specified object is null |
| `java.lang.ClassCastException` | if the specified object's type prevents it from being compared to this object. |

### divide

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun divide(divisor: BigDecimal!): BigDecimal!
```

Returns a`BigDecimal`whose value is`(this / divisor)`, and whose preferred scale is`(this.scale() - divisor.scale())`; if the exact quotient cannot be represented (because it has a non-terminating decimal expansion) an`ArithmeticException`is thrown.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------|
| `divisor` | [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal#)!:value by which this`BigDecimal`is to be divided. |

| Return ||
|-------------------------------------------------------------------------------------|------------------|
| [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal#)! | `this / divisor` |

| Exceptions ||
|---------------------------------|-------------------------------------------------------------------------------------------------|
| `java.lang.ArithmeticException` | if the exact quotient does not have a terminating decimal expansion, including dividing by zero |

### divide

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun divide(
    divisor: BigDecimal!, 
    roundingMode: Int
): BigDecimal!
```

**Deprecated:** *The method [divide(java.math.BigDecimal,java.math.RoundingMode)](https://developer.android.com/reference/kotlin/java/math/BigDecimal#divide(java.math.BigDecimal,%20java.math.RoundingMode))should be used in preference to this legacy method.*

Returns a`BigDecimal`whose value is`(this / divisor)`, and whose scale is`this.scale()`. If rounding must be performed to generate a result with the given scale, the specified rounding mode is applied.

| Parameters ||
|----------------|--------------------------------------------------------------------------------------------------------------------------------------|
| `divisor` | [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal#)!:value by which this`BigDecimal`is to be divided. |
| `roundingMode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):rounding mode to apply. |

| Return ||
|-------------------------------------------------------------------------------------|------------------|
| [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal#)! | `this / divisor` |

| Exceptions ||
|--------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.ArithmeticException` | if`divisor==0`, or`roundingMode==ROUND_UNNECESSARY`and`this.scale()`is insufficient to represent the result of the division exactly. |
| `java.lang.IllegalArgumentException` | if`roundingMode`does not represent a valid rounding mode. |

**See Also**

- [#ROUND_UP](https://developer.android.com/reference/kotlin/java/math/BigDecimal#ROUND_UP:kotlin.Int)
- [#ROUND_DOWN](https://developer.android.com/reference/kotlin/java/math/BigDecimal#ROUND_DOWN:kotlin.Int)
- [#ROUND_CEILING](https://developer.android.com/reference/kotlin/java/math/BigDecimal#ROUND_CEILING:kotlin.Int)
- [#ROUND_FLOOR](https://developer.android.com/reference/kotlin/java/math/BigDecimal#ROUND_FLOOR:kotlin.Int)
- [#ROUND_HALF_UP](https://developer.android.com/reference/kotlin/java/math/BigDecimal#ROUND_HALF_UP:kotlin.Int)
- [#ROUND_HALF_DOWN](https://developer.android.com/reference/kotlin/java/math/BigDecimal#ROUND_HALF_DOWN:kotlin.Int)
- [#ROUND_HALF_EVEN](https://developer.android.com/reference/kotlin/java/math/BigDecimal#ROUND_HALF_EVEN:kotlin.Int)
- [#ROUND_UNNECESSARY](https://developer.android.com/reference/kotlin/java/math/BigDecimal#ROUND_UNNECESSARY:kotlin.Int) 

### divide

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun divide(
    divisor: BigDecimal!, 
    scale: Int, 
    roundingMode: Int
): BigDecimal!
```

**Deprecated:** *The method [divide(java.math.BigDecimal,int,java.math.RoundingMode)](https://developer.android.com/reference/kotlin/java/math/BigDecimal#divide(java.math.BigDecimal,%20kotlin.Int,%20java.math.RoundingMode))should be used in preference to this legacy method.*

Returns a`BigDecimal`whose value is`(this / divisor)`, and whose scale is as specified. If rounding must be performed to generate a result with the specified scale, the specified rounding mode is applied.

| Parameters ||
|----------------|--------------------------------------------------------------------------------------------------------------------------------------|
| `divisor` | [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal#)!:value by which this`BigDecimal`is to be divided. |
| `scale` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):scale of the`BigDecimal`quotient to be returned. |
| `roundingMode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):rounding mode to apply. |
| --- | --- |

| Return ||
|-------------------------------------------------------------------------------------|------------------|
| [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal#)! | `this / divisor` |

| Exceptions ||
|--------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.ArithmeticException` | if`divisor`is zero,`roundingMode==ROUND_UNNECESSARY`and the specified scale is insufficient to represent the result of the division exactly. |
| `java.lang.IllegalArgumentException` | if`roundingMode`does not represent a valid rounding mode. |

**See Also**

- [#ROUND_UP](https://developer.android.com/reference/kotlin/java/math/BigDecimal#ROUND_UP:kotlin.Int)
- [#ROUND_DOWN](https://developer.android.com/reference/kotlin/java/math/BigDecimal#ROUND_DOWN:kotlin.Int)
- [#ROUND_CEILING](https://developer.android.com/reference/kotlin/java/math/BigDecimal#ROUND_CEILING:kotlin.Int)
- [#ROUND_FLOOR](https://developer.android.com/reference/kotlin/java/math/BigDecimal#ROUND_FLOOR:kotlin.Int)
- [#ROUND_HALF_UP](https://developer.android.com/reference/kotlin/java/math/BigDecimal#ROUND_HALF_UP:kotlin.Int)
- [#ROUND_HALF_DOWN](https://developer.android.com/reference/kotlin/java/math/BigDecimal#ROUND_HALF_DOWN:kotlin.Int)
- [#ROUND_HALF_EVEN](https://developer.android.com/reference/kotlin/java/math/BigDecimal#ROUND_HALF_EVEN:kotlin.Int)
- [#ROUND_UNNECESSARY](https://developer.android.com/reference/kotlin/java/math/BigDecimal#ROUND_UNNECESSARY:kotlin.Int) 

### divide

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun divide(
    divisor: BigDecimal!, 
    scale: Int, 
    roundingMode: RoundingMode!
): BigDecimal!
```

Returns a`BigDecimal`whose value is`(this / divisor)`, and whose scale is as specified. If rounding must be performed to generate a result with the specified scale, the specified rounding mode is applied.

| Parameters ||
|----------------|--------------------------------------------------------------------------------------------------------------------------------------|
| `divisor` | [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal#)!:value by which this`BigDecimal`is to be divided. |
| `scale` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):scale of the`BigDecimal`quotient to be returned. |
| `roundingMode` | [RoundingMode](https://developer.android.com/reference/kotlin/java/math/RoundingMode)!:rounding mode to apply. |
| --- | --- |

| Return ||
|-------------------------------------------------------------------------------------|------------------|
| [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal#)! | `this / divisor` |

| Exceptions ||
|---------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.ArithmeticException` | if`divisor`is zero,`roundingMode==RoundingMode.UNNECESSARY`and the specified scale is insufficient to represent the result of the division exactly. |

### divide

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun divide(
    divisor: BigDecimal!, 
    mc: MathContext!
): BigDecimal!
```

Returns a`BigDecimal`whose value is`(this / divisor)`, with rounding according to the context settings.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------|
| `divisor` | [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal#)!:value by which this`BigDecimal`is to be divided. |
| `mc` | [MathContext](https://developer.android.com/reference/kotlin/java/math/MathContext)!:the context to use. |

| Return ||
|-------------------------------------------------------------------------------------|-----------------------------------------|
| [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal#)! | `this / divisor`, rounded as necessary. |

| Exceptions ||
|---------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.ArithmeticException` | if the result is inexact but the rounding mode is`UNNECESSARY`or`mc.precision == 0`and the quotient has a non-terminating decimal expansion,including dividing by zero |

### divide

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun divide(
    divisor: BigDecimal!, 
    roundingMode: RoundingMode!
): BigDecimal!
```

Returns a`BigDecimal`whose value is`(this / divisor)`, and whose scale is`this.scale()`. If rounding must be performed to generate a result with the given scale, the specified rounding mode is applied.

| Parameters ||
|----------------|--------------------------------------------------------------------------------------------------------------------------------------|
| `divisor` | [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal#)!:value by which this`BigDecimal`is to be divided. |
| `roundingMode` | [RoundingMode](https://developer.android.com/reference/kotlin/java/math/RoundingMode)!:rounding mode to apply. |

| Return ||
|-------------------------------------------------------------------------------------|------------------|
| [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal#)! | `this / divisor` |

| Exceptions ||
|---------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.ArithmeticException` | if`divisor==0`, or`roundingMode==RoundingMode.UNNECESSARY`and`this.scale()`is insufficient to represent the result of the division exactly. |

### divideAndRemainder

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun divideAndRemainder(divisor: BigDecimal!): Array<BigDecimal!>!
```

Returns a two-element`BigDecimal`array containing the result of`divideToIntegralValue`followed by the result of`remainder`on the two operands.

Note that if both the integer quotient and remainder are needed, this method is faster than using the`divideToIntegralValue`and`remainder`methods separately because the division need only be carried out once.

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `divisor` | [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal#)!:value by which this`BigDecimal`is to be divided, and the remainder computed. |

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal#)!>! | a two element`BigDecimal`array: the quotient (the result of`divideToIntegralValue`) is the initial element and the remainder is the final element. |

| Exceptions ||
|---------------------------------|----------------|
| `java.lang.ArithmeticException` | if`divisor==0` |

**See Also**

- [#divideToIntegralValue(java.math.BigDecimal, java.math.MathContext)](https://developer.android.com/reference/kotlin/java/math/BigDecimal#divideToIntegralValue(java.math.BigDecimal,%20java.math.MathContext))
- [#remainder(java.math.BigDecimal, java.math.MathContext)](https://developer.android.com/reference/kotlin/java/math/BigDecimal#remainder(java.math.BigDecimal,%20java.math.MathContext)) 

### divideAndRemainder

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun divideAndRemainder(
    divisor: BigDecimal!, 
    mc: MathContext!
): Array<BigDecimal!>!
```

Returns a two-element`BigDecimal`array containing the result of`divideToIntegralValue`followed by the result of`remainder`on the two operands calculated with rounding according to the context settings.

Note that if both the integer quotient and remainder are needed, this method is faster than using the`divideToIntegralValue`and`remainder`methods separately because the division need only be carried out once.

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `divisor` | [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal#)!:value by which this`BigDecimal`is to be divided, and the remainder computed. |
| `mc` | [MathContext](https://developer.android.com/reference/kotlin/java/math/MathContext)!:the context to use. |

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal#)!>! | a two element`BigDecimal`array: the quotient (the result of`divideToIntegralValue`) is the initial element and the remainder is the final element. |

| Exceptions ||
|---------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.ArithmeticException` | if the result is inexact but the rounding mode is`UNNECESSARY`, or`mc.precision`\> 0 and the result of`this.divideToIntegralValue(divisor)`would require a precision of more than`mc.precision`digits. |

**See Also**

- [#divideToIntegralValue(java.math.BigDecimal, java.math.MathContext)](https://developer.android.com/reference/kotlin/java/math/BigDecimal#divideToIntegralValue(java.math.BigDecimal,%20java.math.MathContext))
- [#remainder(java.math.BigDecimal, java.math.MathContext)](https://developer.android.com/reference/kotlin/java/math/BigDecimal#remainder(java.math.BigDecimal,%20java.math.MathContext)) 

### divideToIntegralValue

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun divideToIntegralValue(divisor: BigDecimal!): BigDecimal!
```

Returns a`BigDecimal`whose value is the integer part of the quotient`(this / divisor)`rounded down. The preferred scale of the result is`(this.scale() - divisor.scale())`.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------|
| `divisor` | [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal#)!:value by which this`BigDecimal`is to be divided. |

| Return ||
|-------------------------------------------------------------------------------------|--------------------------------------|
| [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal#)! | The integer part of`this / divisor`. |

| Exceptions ||
|---------------------------------|----------------|
| `java.lang.ArithmeticException` | if`divisor==0` |

### divideToIntegralValue

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun divideToIntegralValue(
    divisor: BigDecimal!, 
    mc: MathContext!
): BigDecimal!
```

Returns a`BigDecimal`whose value is the integer part of`(this / divisor)`. Since the integer part of the exact quotient does not depend on the rounding mode, the rounding mode does not affect the values returned by this method. The preferred scale of the result is`(this.scale() - divisor.scale())`. An`ArithmeticException`is thrown if the integer part of the exact quotient needs more than`mc.precision`digits.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------|
| `divisor` | [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal#)!:value by which this`BigDecimal`is to be divided. |
| `mc` | [MathContext](https://developer.android.com/reference/kotlin/java/math/MathContext)!:the context to use. |

| Return ||
|-------------------------------------------------------------------------------------|--------------------------------------|
| [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal#)! | The integer part of`this / divisor`. |

| Exceptions ||
|---------------------------------|--------------------------------------------------------------------------------------------|
| `java.lang.ArithmeticException` | if`mc.precision`\> 0 and the result requires a precision of more than`mc.precision`digits. |

### equals

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun equals(other: Any?): Boolean
```

Compares this`BigDecimal`with the specified`Object`for equality. Unlike [compareTo](https://developer.android.com/reference/kotlin/java/math/BigDecimal#compareTo(java.math.BigDecimal)), this method considers two`BigDecimal`objects equal only if they are equal in value and scale. Therefore 2.0 is not equal to 2.00 when compared by this method since the former has \[`BigInteger`,`scale`\] components equal to \[20, 1\] while the latter has components equal to \[200, 2\].

| Parameters ||
|-------|-----------------------------------------------------|
| `obj` | the reference object with which to compare. |
| `x` | `Object`to which this`BigDecimal`is to be compared. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if and only if the specified`Object`is a`BigDecimal`whose value and scale are equal to this`BigDecimal`'s. |

**See Also**

- <https://developer.android.com/reference/kotlin/java/math/BigDecimal#compareTo(java.math.BigDecimal)>
- [#hashCode](https://developer.android.com/reference/kotlin/java/math/BigDecimal#hashCode()) 

### hashCode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hashCode(): Int
```

Returns the hash code for this`BigDecimal`. The hash code is computed as a function of the [unscaled value](https://developer.android.com/reference/kotlin/java/math/BigDecimal#unscaledValue())and the [scale](https://developer.android.com/reference/kotlin/java/math/BigDecimal#scale())of this`BigDecimal`.

| Return ||
|----------------------------------------------------------------------------|---------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | hash code for this`BigDecimal`. |

**See Also**

- [#equals(Object)](https://developer.android.com/reference/kotlin/java/math/BigDecimal#equals(kotlin.Any)) 

### intValueExact

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun intValueExact(): Int
```

Converts this`BigDecimal`to an`int`, checking for lost information. If this`BigDecimal`has a nonzero fractional part or is out of the possible range for an`int`result then an`ArithmeticException`is thrown.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | this`BigDecimal`converted to an`int`. |

| Exceptions ||
|---------------------------------|--------------------------------------------------------------------|
| `java.lang.ArithmeticException` | if`this`has a nonzero fractional part, or will not fit in an`int`. |

### longValueExact

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun longValueExact(): Long
```

Converts this`BigDecimal`to a`long`, checking for lost information. If this`BigDecimal`has a nonzero fractional part or is out of the possible range for a`long`result then an`ArithmeticException`is thrown.

| Return ||
|------------------------------------------------------------------------------|---------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | this`BigDecimal`converted to a`long`. |

| Exceptions ||
|---------------------------------|--------------------------------------------------------------------|
| `java.lang.ArithmeticException` | if`this`has a nonzero fractional part, or will not fit in a`long`. |

### max

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun max(val: BigDecimal!): BigDecimal!
```

Returns the maximum of this`BigDecimal`and`val`.

| Parameters ||
|-------|-------------------------------------------------------------------------------------------------------------------------------------|
| `val` | [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal#)!:value with which the maximum is to be computed. |

| Return ||
|-------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal#)! | the`BigDecimal`whose value is the greater of this`BigDecimal`and`val`. If they are equal, as defined by the [compareTo](https://developer.android.com/reference/kotlin/java/math/BigDecimal#compareTo(java.math.BigDecimal))method,`this`is returned. |

**See Also**

- <https://developer.android.com/reference/kotlin/java/math/BigDecimal#compareTo(java.math.BigDecimal)> 

### min

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun min(val: BigDecimal!): BigDecimal!
```

Returns the minimum of this`BigDecimal`and`val`.

| Parameters ||
|-------|-------------------------------------------------------------------------------------------------------------------------------------|
| `val` | [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal#)!:value with which the minimum is to be computed. |

| Return ||
|-------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal#)! | the`BigDecimal`whose value is the lesser of this`BigDecimal`and`val`. If they are equal, as defined by the [compareTo](https://developer.android.com/reference/kotlin/java/math/BigDecimal#compareTo(java.math.BigDecimal))method,`this`is returned. |

**See Also**

- <https://developer.android.com/reference/kotlin/java/math/BigDecimal#compareTo(java.math.BigDecimal)> 

### movePointLeft

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun movePointLeft(n: Int): BigDecimal!
```

Returns a`BigDecimal`which is equivalent to this one with the decimal point moved`n`places to the left. If`n`is non-negative, the call merely adds`n`to the scale. If`n`is negative, the call is equivalent to`movePointRight(-n)`. The`BigDecimal`returned by this call has value`(this × 10-n)`and scale`max(this.scale()+n, 0)`.

| Parameters ||
|-----|------------------------------------------------------------------------------------------------------------------------------------|
| `n` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):number of places to move the decimal point to the left. |

| Return ||
|-------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal#)! | a`BigDecimal`which is equivalent to this one with the decimal point moved`n`places to the left. |

| Exceptions ||
|---------------------------------|---------------------|
| `java.lang.ArithmeticException` | if scale overflows. |

### movePointRight

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun movePointRight(n: Int): BigDecimal!
```

Returns a`BigDecimal`which is equivalent to this one with the decimal point moved`n`places to the right. If`n`is non-negative, the call merely subtracts`n`from the scale. If`n`is negative, the call is equivalent to`movePointLeft(-n)`. The`BigDecimal`returned by this call has value`(this × 10n)`and scale`max(this.scale()-n, 0)`.

| Parameters ||
|-----|-------------------------------------------------------------------------------------------------------------------------------------|
| `n` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):number of places to move the decimal point to the right. |

| Return ||
|-------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal#)! | a`BigDecimal`which is equivalent to this one with the decimal point moved`n`places to the right. |

| Exceptions ||
|---------------------------------|---------------------|
| `java.lang.ArithmeticException` | if scale overflows. |

### multiply

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun multiply(multiplicand: BigDecimal!): BigDecimal!
```

Returns a`BigDecimal`whose value is`(this × multiplicand)`, and whose scale is`(this.scale() + multiplicand.scale())`.

| Parameters ||
|----------------|---------------------------------------------------------------------------------------------------------------------------------|
| `multiplicand` | [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal#)!:value to be multiplied by this`BigDecimal`. |

| Return ||
|-------------------------------------------------------------------------------------|-----------------------|
| [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal#)! | `this * multiplicand` |

### multiply

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun multiply(
    multiplicand: BigDecimal!, 
    mc: MathContext!
): BigDecimal!
```

Returns a`BigDecimal`whose value is`(this × multiplicand)`, with rounding according to the context settings.

| Parameters ||
|----------------|---------------------------------------------------------------------------------------------------------------------------------|
| `multiplicand` | [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal#)!:value to be multiplied by this`BigDecimal`. |
| `mc` | [MathContext](https://developer.android.com/reference/kotlin/java/math/MathContext)!:the context to use. |

| Return ||
|-------------------------------------------------------------------------------------|----------------------------------------------|
| [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal#)! | `this * multiplicand`, rounded as necessary. |

### negate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun negate(): BigDecimal!
```

Returns a`BigDecimal`whose value is`(-this)`, and whose scale is`this.scale()`.

| Return ||
|-------------------------------------------------------------------------------------|----------|
| [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal#)! | `-this`. |

### negate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun negate(mc: MathContext!): BigDecimal!
```

Returns a`BigDecimal`whose value is`(-this)`, with rounding according to the context settings.

| Parameters ||
|------|----------------------------------------------------------------------------------------------------------|
| `mc` | [MathContext](https://developer.android.com/reference/kotlin/java/math/MathContext)!:the context to use. |

| Return ||
|-------------------------------------------------------------------------------------|--------------------------------|
| [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal#)! | `-this`, rounded as necessary. |

### plus

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun plus(): BigDecimal!
```

Returns a`BigDecimal`whose value is`(+this)`, and whose scale is`this.scale()`.

This method, which simply returns this`BigDecimal`is included for symmetry with the unary minus method [negate()](https://developer.android.com/reference/kotlin/java/math/BigDecimal#negate()).

| Return ||
|-------------------------------------------------------------------------------------|---------|
| [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal#)! | `this`. |

**See Also**

- <https://developer.android.com/reference/kotlin/java/math/BigDecimal#negate()> 

### plus

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun plus(mc: MathContext!): BigDecimal!
```

Returns a`BigDecimal`whose value is`(+this)`, with rounding according to the context settings.

The effect of this method is identical to that of the [round(java.math.MathContext)](https://developer.android.com/reference/kotlin/java/math/BigDecimal#round(java.math.MathContext))method.

| Parameters ||
|------|----------------------------------------------------------------------------------------------------------|
| `mc` | [MathContext](https://developer.android.com/reference/kotlin/java/math/MathContext)!:the context to use. |

| Return ||
|-------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal#)! | `this`, rounded as necessary. A zero result will have a scale of 0. |

**See Also**

- [#round(MathContext)](https://developer.android.com/reference/kotlin/java/math/BigDecimal#round(java.math.MathContext)) 

### pow

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun pow(n: Int): BigDecimal!
```

Returns a`BigDecimal`whose value is`(thisn)`, The power is computed exactly, to unlimited precision.

The parameter`n`must be in the range 0 through 999999999, inclusive.`ZERO.pow(0)`returns [ONE](https://developer.android.com/reference/kotlin/java/math/BigDecimal#ONE:java.math.BigDecimal). Note that future releases may expand the allowable exponent range of this method.

| Parameters ||
|-----|---------------------------------------------------------------------------------------------------------------|
| `n` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):power to raise this`BigDecimal`to. |

| Return ||
|-------------------------------------------------------------------------------------|---------|
| [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal#)! | `thisn` |

| Exceptions ||
|---------------------------------|-----------------------|
| `java.lang.ArithmeticException` | if`n`is out of range. |

### pow

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun pow(
    n: Int, 
    mc: MathContext!
): BigDecimal!
```

Returns a`BigDecimal`whose value is`(thisn)`. The current implementation uses the core algorithm defined in ANSI standard X3.274-1996 with rounding according to the context settings. In general, the returned numerical value is within two ulps of the exact numerical value for the chosen precision. Note that future releases may use a different algorithm with a decreased allowable error bound and increased allowable exponent range.

The X3.274-1996 algorithm is:

- An`ArithmeticException`exception is thrown if
 - `abs(n) > 999999999`
 - `mc.precision == 0`and`n < 0`
 - `mc.precision > 0`and`n`has more than`mc.precision`decimal digits
- if`n`is zero, [ONE](https://developer.android.com/reference/kotlin/java/math/BigDecimal#ONE:java.math.BigDecimal) is returned even if`this`is zero, otherwise
 - if`n`is positive, the result is calculated via the repeated squaring technique into a single accumulator. The individual multiplications with the accumulator use the same math context settings as in`mc`except for a precision increased to`mc.precision + elength + 1`where`elength`is the number of decimal digits in`n`.
 - if`n`is negative, the result is calculated as if`n`were positive; this value is then divided into one using the working precision specified above.
 - The final value from either the positive or negative case is then rounded to the destination precision.

| Parameters ||
|------|---------------------------------------------------------------------------------------------------------------|
| `n` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):power to raise this`BigDecimal`to. |
| `mc` | [MathContext](https://developer.android.com/reference/kotlin/java/math/MathContext)!:the context to use. |

| Return ||
|-------------------------------------------------------------------------------------|------------------------------------------------------|
| [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal#)! | `thisn`using the ANSI standard X3.274-1996 algorithm |

| Exceptions ||
|---------------------------------|---------------------------------------------------------------------------------------|
| `java.lang.ArithmeticException` | if the result is inexact but the rounding mode is`UNNECESSARY`, or`n`is out of range. |

### precision

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun precision(): Int
```

Returns the*precision* of this`BigDecimal`. (The precision is the number of digits in the unscaled value.)

The precision of a zero value is 1.

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the precision of this`BigDecimal`. |

### remainder

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun remainder(divisor: BigDecimal!): BigDecimal!
```

Returns a`BigDecimal`whose value is`(this % divisor)`.

The remainder is given by`this.subtract(this.divideToIntegralValue(divisor).multiply(divisor))`. Note that this is*not*the modulo operation (the result can be negative).

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------|
| `divisor` | [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal#)!:value by which this`BigDecimal`is to be divided. |

| Return ||
|-------------------------------------------------------------------------------------|-------------------|
| [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal#)! | `this % divisor`. |

| Exceptions ||
|---------------------------------|----------------|
| `java.lang.ArithmeticException` | if`divisor==0` |

### remainder

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun remainder(
    divisor: BigDecimal!, 
    mc: MathContext!
): BigDecimal!
```

Returns a`BigDecimal`whose value is`(this % divisor)`, with rounding according to the context settings. The`MathContext`settings affect the implicit divide used to compute the remainder. The remainder computation itself is by definition exact. Therefore, the remainder may contain more than`mc.getPrecision()`digits.

The remainder is given by`this.subtract(this.divideToIntegralValue(divisor, mc).multiply(divisor))`. Note that this is not the modulo operation (the result can be negative).

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------|
| `divisor` | [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal#)!:value by which this`BigDecimal`is to be divided. |
| `mc` | [MathContext](https://developer.android.com/reference/kotlin/java/math/MathContext)!:the context to use. |

| Return ||
|-------------------------------------------------------------------------------------|-----------------------------------------|
| [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal#)! | `this % divisor`, rounded as necessary. |

| Exceptions ||
|---------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.ArithmeticException` | if the result is inexact but the rounding mode is`UNNECESSARY`, or`mc.precision`\> 0 and the result of`this.divideToIntegralValue(divisor)`would require a precision of more than`mc.precision`digits. |

**See Also**

- [#divideToIntegralValue(java.math.BigDecimal, java.math.MathContext)](https://developer.android.com/reference/kotlin/java/math/BigDecimal#divideToIntegralValue(java.math.BigDecimal,%20java.math.MathContext)) 

### round

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun round(mc: MathContext!): BigDecimal!
```

Returns a`BigDecimal`rounded according to the`MathContext`settings. If the precision setting is 0 then no rounding takes place.

The effect of this method is identical to that of the [plus(java.math.MathContext)](https://developer.android.com/reference/kotlin/java/math/BigDecimal#plus(java.math.MathContext))method.

| Parameters ||
|------|----------------------------------------------------------------------------------------------------------|
| `mc` | [MathContext](https://developer.android.com/reference/kotlin/java/math/MathContext)!:the context to use. |

| Return ||
|-------------------------------------------------------------------------------------|-------------------------------------------------------------|
| [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal#)! | a`BigDecimal`rounded according to the`MathContext`settings. |

**See Also**

- [#plus(MathContext)](https://developer.android.com/reference/kotlin/java/math/BigDecimal#plus(java.math.MathContext)) 

### scale

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun scale(): Int
```

Returns the*scale* of this`BigDecimal`. If zero or positive, the scale is the number of digits to the right of the decimal point. If negative, the unscaled value of the number is multiplied by ten to the power of the negation of the scale. For example, a scale of`-3`means the unscaled value is multiplied by 1000.

| Return ||
|----------------------------------------------------------------------------|--------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the scale of this`BigDecimal`. |

### scaleByPowerOfTen

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun scaleByPowerOfTen(n: Int): BigDecimal!
```

Returns a BigDecimal whose numerical value is equal to (`this`\* 10n). The scale of the result is`(this.scale() - n)`.

| Parameters ||
|-----|------------------------------------------------------------------------------------------------------------------|
| `n` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the exponent power of ten to scale by |

| Return ||
|-------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal#)! | a BigDecimal whose numerical value is equal to (`this`\* 10n) |

| Exceptions ||
|---------------------------------|--------------------------------------------------------------|
| `java.lang.ArithmeticException` | if the scale would be outside the range of a 32-bit integer. |

### setScale

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setScale(newScale: Int): BigDecimal!
```

Returns a`BigDecimal`whose scale is the specified value, and whose value is numerically equal to this`BigDecimal`'s. Throws an`ArithmeticException`if this is not possible.

This call is typically used to increase the scale, in which case it is guaranteed that there exists a`BigDecimal`of the specified scale and the correct value. The call can also be used to reduce the scale if the caller knows that the`BigDecimal`has sufficiently many zeros at the end of its fractional part (i.e., factors of ten in its integer value) to allow for the rescaling without changing its value.

This method returns the same result as the two-argument versions of`setScale`, but saves the caller the trouble of specifying a rounding mode in cases where it is irrelevant.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------|
| `newScale` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):scale of the`BigDecimal`value to be returned. |

| Return ||
|-------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal#)! | a`BigDecimal`whose scale is the specified value, and whose unscaled value is determined by multiplying or dividing this`BigDecimal`'s unscaled value by the appropriate power of ten to maintain its overall value. |

| Exceptions ||
|---------------------------------|------------------------------------------------------------|
| `java.lang.ArithmeticException` | if the specified scaling operation would require rounding. |

**See Also**

- [#setScale(int, int)](https://developer.android.com/reference/kotlin/java/math/BigDecimal#setScale(kotlin.Int,%20kotlin.Int))
- [#setScale(int, RoundingMode)](https://developer.android.com/reference/kotlin/java/math/BigDecimal#setScale(kotlin.Int,%20java.math.RoundingMode)) 

### setScale

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setScale(
    newScale: Int, 
    roundingMode: Int
): BigDecimal!
```

**Deprecated:** *The method [setScale(int,java.math.RoundingMode)](https://developer.android.com/reference/kotlin/java/math/BigDecimal#setScale(kotlin.Int,%20java.math.RoundingMode))should be used in preference to this legacy method.*

Returns a`BigDecimal`whose scale is the specified value, and whose unscaled value is determined by multiplying or dividing this`BigDecimal`'s unscaled value by the appropriate power of ten to maintain its overall value. If the scale is reduced by the operation, the unscaled value must be divided (rather than multiplied), and the value may be changed; in this case, the specified rounding mode is applied to the division.

| Parameters ||
|----------------|--------------------------------------------------------------------------------------------------------------------------|
| `newScale` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):scale of the`BigDecimal`value to be returned. |
| `roundingMode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The rounding mode to apply. |

| Return ||
|-------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal#)! | a`BigDecimal`whose scale is the specified value, and whose unscaled value is determined by multiplying or dividing this`BigDecimal`'s unscaled value by the appropriate power of ten to maintain its overall value. |

| Exceptions ||
|--------------------------------------|------------------------------------------------------------------------------------------------|
| `java.lang.ArithmeticException` | if`roundingMode==ROUND_UNNECESSARY`and the specified scaling operation would require rounding. |
| `java.lang.IllegalArgumentException` | if`roundingMode`does not represent a valid rounding mode. |

**See Also**

- [#ROUND_UP](https://developer.android.com/reference/kotlin/java/math/BigDecimal#ROUND_UP:kotlin.Int)
- [#ROUND_DOWN](https://developer.android.com/reference/kotlin/java/math/BigDecimal#ROUND_DOWN:kotlin.Int)
- [#ROUND_CEILING](https://developer.android.com/reference/kotlin/java/math/BigDecimal#ROUND_CEILING:kotlin.Int)
- [#ROUND_FLOOR](https://developer.android.com/reference/kotlin/java/math/BigDecimal#ROUND_FLOOR:kotlin.Int)
- [#ROUND_HALF_UP](https://developer.android.com/reference/kotlin/java/math/BigDecimal#ROUND_HALF_UP:kotlin.Int)
- [#ROUND_HALF_DOWN](https://developer.android.com/reference/kotlin/java/math/BigDecimal#ROUND_HALF_DOWN:kotlin.Int)
- [#ROUND_HALF_EVEN](https://developer.android.com/reference/kotlin/java/math/BigDecimal#ROUND_HALF_EVEN:kotlin.Int)
- [#ROUND_UNNECESSARY](https://developer.android.com/reference/kotlin/java/math/BigDecimal#ROUND_UNNECESSARY:kotlin.Int) 

### setScale

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setScale(
    newScale: Int, 
    roundingMode: RoundingMode!
): BigDecimal!
```

Returns a`BigDecimal`whose scale is the specified value, and whose unscaled value is determined by multiplying or dividing this`BigDecimal`'s unscaled value by the appropriate power of ten to maintain its overall value. If the scale is reduced by the operation, the unscaled value must be divided (rather than multiplied), and the value may be changed; in this case, the specified rounding mode is applied to the division.

| Parameters ||
|----------------|--------------------------------------------------------------------------------------------------------------------------|
| `newScale` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):scale of the`BigDecimal`value to be returned. |
| `roundingMode` | [RoundingMode](https://developer.android.com/reference/kotlin/java/math/RoundingMode)!:The rounding mode to apply. |

| Return ||
|-------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal#)! | a`BigDecimal`whose scale is the specified value, and whose unscaled value is determined by multiplying or dividing this`BigDecimal`'s unscaled value by the appropriate power of ten to maintain its overall value. |

| Exceptions ||
|---------------------------------|------------------------------------------------------------------------------------------|
| `java.lang.ArithmeticException` | if`roundingMode==UNNECESSARY`and the specified scaling operation would require rounding. |

**See Also**

- [java.math.RoundingMode](https://developer.android.com/reference/kotlin/java/math/RoundingMode) 

### shortValueExact

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun shortValueExact(): Short
```

Converts this`BigDecimal`to a`short`, checking for lost information. If this`BigDecimal`has a nonzero fractional part or is out of the possible range for a`short`result then an`ArithmeticException`is thrown.

| Return ||
|--------------------------------------------------------------------------------|----------------------------------------|
| [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | this`BigDecimal`converted to a`short`. |

| Exceptions ||
|---------------------------------|---------------------------------------------------------------------|
| `java.lang.ArithmeticException` | if`this`has a nonzero fractional part, or will not fit in a`short`. |

### signum

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun signum(): Int
```

Returns the signum function of this`BigDecimal`.

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | -1, 0, or 1 as the value of this`BigDecimal`is negative, zero, or positive. |

### sqrt

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun sqrt(mc: MathContext!): BigDecimal!
```

Returns an approximation to the square root of`this`with rounding according to the context settings.

The preferred scale of the returned result is equal to`this.scale()/2`. The value of the returned result is always within one ulp of the exact decimal value for the precision in question. If the rounding mode is [HALF_UP](https://developer.android.com/reference/kotlin/java/math/RoundingMode), [HALF_DOWN](https://developer.android.com/reference/kotlin/java/math/RoundingMode), or [HALF_EVEN](https://developer.android.com/reference/kotlin/java/math/RoundingMode), the result is within one half an ulp of the exact decimal value.

Special case:

- The square root of a number numerically equal to`ZERO`is numerically equal to`ZERO`with a preferred scale according to the general rule above. In particular, for`ZERO`,`ZERO.sqrt(mc).equals(ZERO)`is true with any`MathContext`as an argument.

| Parameters ||
|------|----------------------------------------------------------------------------------------------------------|
| `mc` | [MathContext](https://developer.android.com/reference/kotlin/java/math/MathContext)!:the context to use. |

| Return ||
|-------------------------------------------------------------------------------------|---------------------------|
| [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal#)! | the square root of`this`. |

| Exceptions ||
|---------------------------------|-------------------------------------------------------------------------------------------------------------------|
| `java.lang.ArithmeticException` | if`(mc.getRoundingMode()==RoundingMode.UNNECESSARY`) and the exact result cannot fit in`mc.getPrecision()`digits. |

**See Also**

- [java.math.BigInteger#sqrt()](https://developer.android.com/reference/kotlin/java/math/BigInteger#sqrt()) 

### stripTrailingZeros

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun stripTrailingZeros(): BigDecimal!
```

Returns a`BigDecimal`which is numerically equal to this one but with any trailing zeros removed from the representation. For example, stripping the trailing zeros from the`BigDecimal`value`600.0`, which has \[`BigInteger`,`scale`\] components equal to \[6000, 1\], yields`6E2`with \[`BigInteger`,`scale`\] components equal to \[6, -2\]. If this BigDecimal is numerically equal to zero, then`BigDecimal.ZERO`is returned.

| Return ||
|-------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal#)! | a numerically equal`BigDecimal`with any trailing zeros removed. |

| Exceptions ||
|---------------------------------|---------------------|
| `java.lang.ArithmeticException` | if scale overflows. |

### subtract

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun subtract(subtrahend: BigDecimal!): BigDecimal!
```

Returns a`BigDecimal`whose value is`(this - subtrahend)`, and whose scale is`max(this.scale(), subtrahend.scale())`.

| Parameters ||
|--------------|-----------------------------------------------------------------------------------------------------------------------------------|
| `subtrahend` | [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal#)!:value to be subtracted from this`BigDecimal`. |

| Return ||
|-------------------------------------------------------------------------------------|---------------------|
| [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal#)! | `this - subtrahend` |

### subtract

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun subtract(
    subtrahend: BigDecimal!, 
    mc: MathContext!
): BigDecimal!
```

Returns a`BigDecimal`whose value is`(this - subtrahend)`, with rounding according to the context settings. If`subtrahend`is zero then this, rounded if necessary, is used as the result. If this is zero then the result is`subtrahend.negate(mc)`.

| Parameters ||
|--------------|-----------------------------------------------------------------------------------------------------------------------------------|
| `subtrahend` | [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal#)!:value to be subtracted from this`BigDecimal`. |
| `mc` | [MathContext](https://developer.android.com/reference/kotlin/java/math/MathContext)!:the context to use. |

| Return ||
|-------------------------------------------------------------------------------------|--------------------------------------------|
| [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal#)! | `this - subtrahend`, rounded as necessary. |

### toBigInteger

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toBigInteger(): BigInteger!
```

Converts this`BigDecimal`to a`BigInteger`. This conversion is analogous to the*narrowing primitive conversion* from`double`to`long`as defined in The Java Language Specification: any fractional part of this`BigDecimal`will be discarded. Note that this conversion can lose information about the precision of the`BigDecimal`value.

To have an exception thrown if the conversion is inexact (in other words if a nonzero fractional part is discarded), use the [toBigIntegerExact()](https://developer.android.com/reference/kotlin/java/math/BigDecimal#toBigIntegerExact())method.

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------|
| [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger)! | this`BigDecimal`converted to a`BigInteger`. |

### toBigIntegerExact

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toBigIntegerExact(): BigInteger!
```

Converts this`BigDecimal`to a`BigInteger`, checking for lost information. An exception is thrown if this`BigDecimal`has a nonzero fractional part.

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------|
| [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger)! | this`BigDecimal`converted to a`BigInteger`. |

| Exceptions ||
|---------------------------------|----------------------------------------|
| `java.lang.ArithmeticException` | if`this`has a nonzero fractional part. |

### toDouble

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toDouble(): Double
```

Converts this`BigDecimal`to a`double`. This conversion is similar to the*narrowing primitive conversion* from`double`to`float`as defined in The Java Language Specification: if this`BigDecimal`has too great a magnitude represent as a`double`, it will be converted to [Double.NEGATIVE_INFINITY](https://developer.android.com/reference/kotlin/java/lang/Double.html#NEGATIVE_INFINITY:kotlin.Double) or [java.lang.Double#POSITIVE_INFINITY](https://developer.android.com/reference/kotlin/java/lang/Double.html#POSITIVE_INFINITY:kotlin.Double) as appropriate. Note that even when the return value is finite, this conversion can lose information about the precision of the`BigDecimal`value.

| Return ||
|----------------------------------------------------------------------------------|-----------------------------------------|
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | this`BigDecimal`converted to a`double`. |

### toEngineeringString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toEngineeringString(): String!
```

Returns a string representation of this`BigDecimal`, using engineering notation if an exponent is needed.

Returns a string that represents the`BigDecimal`as described in the [toString()](https://developer.android.com/reference/kotlin/java/math/BigDecimal#toString())method, except that if exponential notation is used, the power of ten is adjusted to be a multiple of three (engineering notation) such that the integer part of nonzero values will be in the range 1 through 999. If exponential notation is used for zero values, a decimal point and one or two fractional zero digits are used so that the scale of the zero value is preserved. Note that unlike the output of [toString()](https://developer.android.com/reference/kotlin/java/math/BigDecimal#toString()), the output of this method is*not* guaranteed to recover the same \[integer, scale\] pair of this`BigDecimal`if the output string is converting back to a`BigDecimal`using the [string constructor](https://developer.android.com/reference/kotlin/java/math/BigDecimal#BigDecimal(kotlin.String)). The result of this method meets the weaker constraint of always producing a numerically equal result from applying the string constructor to the method's output.

| Return ||
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | string representation of this`BigDecimal`, using engineering notation if an exponent is needed. |

### toFloat

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toFloat(): Float
```

Converts this`BigDecimal`to a`float`. This conversion is similar to the*narrowing primitive conversion* from`double`to`float`as defined in The Java Language Specification: if this`BigDecimal`has too great a magnitude to represent as a`float`, it will be converted to [Float.NEGATIVE_INFINITY](https://developer.android.com/reference/kotlin/java/lang/Float.html#NEGATIVE_INFINITY:kotlin.Float) or [java.lang.Float#POSITIVE_INFINITY](https://developer.android.com/reference/kotlin/java/lang/Float.html#POSITIVE_INFINITY:kotlin.Float) as appropriate. Note that even when the return value is finite, this conversion can lose information about the precision of the`BigDecimal`value.

| Return ||
|--------------------------------------------------------------------------------|----------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | this`BigDecimal`converted to a`float`. |

### toInt

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toInt(): Int
```

Converts this`BigDecimal`to an`int`. This conversion is analogous to the*narrowing primitive conversion* from`double`to`short`as defined in The Java Language Specification: any fractional part of this`BigDecimal`will be discarded, and if the resulting "`BigInteger`" is too big to fit in an`int`, only the low-order 32 bits are returned. Note that this conversion can lose information about the overall magnitude and precision of this`BigDecimal`value as well as return a result with the opposite sign.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | this`BigDecimal`converted to an`int`. |

### toLong

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toLong(): Long
```

Converts this`BigDecimal`to a`long`. This conversion is analogous to the*narrowing primitive conversion* from`double`to`short`as defined in The Java Language Specification: any fractional part of this`BigDecimal`will be discarded, and if the resulting "`BigInteger`" is too big to fit in a`long`, only the low-order 64 bits are returned. Note that this conversion can lose information about the overall magnitude and precision of this`BigDecimal`value as well as return a result with the opposite sign.

| Return ||
|------------------------------------------------------------------------------|---------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | this`BigDecimal`converted to a`long`. |

### toPlainString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toPlainString(): String!
```

Returns a string representation of this`BigDecimal`without an exponent field. For values with a positive scale, the number of digits to the right of the decimal point is used to indicate scale. For values with a zero or negative scale, the resulting string is generated as if the value were converted to a numerically equal value with zero scale and as if all the trailing zeros of the zero scale value were present in the result. The entire string is prefixed by a minus sign character '-' (`'\u002D'`) if the unscaled value is less than zero. No sign character is prefixed if the unscaled value is zero or positive. Note that if the result of this method is passed to the [string constructor](https://developer.android.com/reference/kotlin/java/math/BigDecimal#BigDecimal(kotlin.String)), only the numerical value of this`BigDecimal`will necessarily be recovered; the representation of the new`BigDecimal`may have a different scale. In particular, if this`BigDecimal`has a negative scale, the string resulting from this method will have a scale of zero when processed by the string constructor. (This method behaves analogously to the`toString`method in 1.4 and earlier releases.)

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | a string representation of this`BigDecimal`without an exponent field. |

**See Also**

- <https://developer.android.com/reference/kotlin/java/math/BigDecimal#toString()>
- <https://developer.android.com/reference/kotlin/java/math/BigDecimal#toEngineeringString()> 

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

Returns the string representation of this`BigDecimal`, using scientific notation if an exponent is needed.

A standard canonical string form of the`BigDecimal`is created as though by the following steps: first, the absolute value of the unscaled value of the`BigDecimal`is converted to a string in base ten using the characters`'0'`through`'9'`with no leading zeros (except if its value is zero, in which case a single`'0'`character is used).

Next, an*adjusted exponent* is calculated; this is the negated scale, plus the number of characters in the converted unscaled value, less one. That is,`-scale+(ulength-1)`, where`ulength`is the length of the absolute value of the unscaled value in decimal digits (its*precision*).

If the scale is greater than or equal to zero and the adjusted exponent is greater than or equal to`-6`, the number will be converted to a character form without using exponential notation. In this case, if the scale is zero then no decimal point is added and if the scale is positive a decimal point will be inserted with the scale specifying the number of characters to the right of the decimal point.`'0'`characters are added to the left of the converted unscaled value as necessary. If no character precedes the decimal point after this insertion then a conventional`'0'`character is prefixed.

Otherwise (that is, if the scale is negative, or the adjusted exponent is less than`-6`), the number will be converted to a character form using exponential notation. In this case, if the converted`BigInteger`has more than one digit a decimal point is inserted after the first digit. An exponent in character form is then suffixed to the converted unscaled value (perhaps with inserted decimal point); this comprises the letter`'E'`followed immediately by the adjusted exponent converted to a character form. The latter is in base ten, using the characters`'0'`through`'9'`with no leading zeros, and is always prefixed by a sign character`'-'`(`'\u002D'`) if the adjusted exponent is negative,`'+'`(`'\u002B'`) otherwise).

Finally, the entire string is prefixed by a minus sign character`'-'`(`'\u002D'`) if the unscaled value is less than zero. No sign character is prefixed if the unscaled value is zero or positive.

**Examples:**

For each representation \[*unscaled value* ,*scale*\] on the left, the resulting string is shown on the right. 

```kotlin
[123,0]      "123"
  [-123,0]     "-123"
  [123,-1]     "1.23E+3"
  [123,-3]     "1.23E+5"
  [123,1]      "12.3"
  [123,5]      "0.00123"
  [123,10]     "1.23E-8"
  [-123,12]    "-1.23E-10"
  
```
**Notes:**

1. There is a one-to-one mapping between the distinguishable`BigDecimal`values and the result of this conversion. That is, every distinguishable`BigDecimal`value (unscaled value and scale) has a unique string representation as a result of using`toString`. If that string representation is converted back to a`BigDecimal`using the [BigDecimal(java.lang.String)](https://developer.android.com/reference/kotlin/java/math/BigDecimal#BigDecimal(kotlin.String))constructor, then the original value will be recovered.
2. The string produced for a given number is always the same; it is not affected by locale. This means that it can be used as a canonical string representation for exchanging decimal data, or as a key for a Hashtable, etc. Locale-sensitive number formatting and parsing is handled by the class and its subclasses.
3. The [toEngineeringString](https://developer.android.com/reference/kotlin/java/math/BigDecimal#toEngineeringString())method may be used for presenting numbers with exponents in engineering notation, and the [setScale](https://developer.android.com/reference/kotlin/java/math/BigDecimal#setScale(kotlin.Int,%20java.math.RoundingMode))method may be used for rounding a`BigDecimal`so it has a known number of digits after the decimal point.
4. The digit-to-character mapping provided by`Character.forDigit`is used.

| Return ||
|----------------------------------------------------------------------------------|--------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | string representation of this`BigDecimal`. |

**See Also**

- [java.lang.Character#forDigit](https://developer.android.com/reference/kotlin/java/lang/Character.html#forDigit(kotlin.Int,%20kotlin.Int))
- [#BigDecimal(java.lang.String)](https://developer.android.com/reference/kotlin/java/math/BigDecimal#BigDecimal(kotlin.String)) 

### ulp

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun ulp(): BigDecimal!
```

Returns the size of an ulp, a unit in the last place, of this`BigDecimal`. An ulp of a nonzero`BigDecimal`value is the positive distance between this value and the`BigDecimal`value next larger in magnitude with the same number of digits. An ulp of a zero value is numerically equal to 1 with the scale of`this`. The result is stored with the same scale as`this`so the result for zero and nonzero values is equal to`[1, this.scale()]`.

| Return ||
|-------------------------------------------------------------------------------------|-----------------------------|
| [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal#)! | the size of an ulp of`this` |

### unscaledValue

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun unscaledValue(): BigInteger!
```

Returns a`BigInteger`whose value is the*unscaled value* of this`BigDecimal`. (Computes`(this * 10this.scale())`.)

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------|
| [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger)! | the unscaled value of this`BigDecimal`. |

### valueOf

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun valueOf(val: Double): BigDecimal!
```

Translates a`double`into a`BigDecimal`, using the`double`'s canonical string representation provided by the [Double.toString(double)](https://developer.android.com/reference/kotlin/java/lang/Double.html#toString(kotlin.Double))method.

| Parameters ||
|-------|-----------------------------------------------------------------------------------------------------------------------|
| `val` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html):`double`to convert to a`BigDecimal`. |

| Return ||
|-------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal#)! | a`BigDecimal`whose value is equal to or approximately equal to the value of`val`. |

| Exceptions ||
|-----------------------------------|----------------------------|
| `java.lang.NumberFormatException` | if`val`is infinite or NaN. |

### valueOf

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun valueOf(val: Long): BigDecimal!
```

Translates a`long`value into a`BigDecimal`with a scale of zero.

| Parameters ||
|-------|--------------------------------------------------------------------------------------------------------|
| `val` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):value of the`BigDecimal`. |

| Return ||
|-------------------------------------------------------------------------------------|-----------------------------------|
| [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal#)! | a`BigDecimal`whose value is`val`. |

### valueOf

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun valueOf(
    unscaledVal: Long, 
    scale: Int
): BigDecimal!
```

Translates a`long`unscaled value and an`int`scale into a`BigDecimal`.

| Parameters ||
|---------------|-----------------------------------------------------------------------------------------------------------------|
| `unscaledVal` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):unscaled value of the`BigDecimal`. |
| `scale` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):scale of the`BigDecimal`. |

| Return ||
|-------------------------------------------------------------------------------------|--------------------------------------------------------|
| [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal#)! | a`BigDecimal`whose value is`(unscaledVal × 10-scale)`. |

## Properties

### ONE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ONE: BigDecimal!
```

The value 1, with a scale of 0. 

### TEN

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TEN: BigDecimal!
```

The value 10, with a scale of 0. 

### ZERO

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ZERO: BigDecimal!
```

The value 0, with a scale of 0.
