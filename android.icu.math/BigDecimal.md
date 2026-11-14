Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BigDecimal

Kotlin | [Java](BigDecimal.md)
| --- | --- |

```
open class BigDecimal : Number, Comparable<BigDecimal!>, Serializable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [kotlin.Number](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-number/index.html) ||
| | ↳ | [android.icu.math.BigDecimal](BigDecimal.md) |

The `BigDecimal` class implements immutable arbitrary-precision decimal numbers. The methods of the `BigDecimal` class provide operations for fixed and floating point arithmetic, comparison, format conversions, and hashing.

As the numbers are decimal, there is an exact correspondence between an instance of a `BigDecimal` object and its `String` representation; the `BigDecimal` class provides direct conversions to and from `String` and character array (`char[]`) objects, as well as conversions to and from the Java primitive types (which may not be exact) and `BigInteger`.

In the descriptions of constructors and methods in this documentation, the value of a `BigDecimal` number object is shown as the result of invoking the `toString()` method on the object. The internal representation of a decimal number is neither defined nor exposed, and is not permitted to affect the result of any operation.

The floating point arithmetic provided by this class is defined by the ANSI X3.274-1996 standard, and is also documented at `http://www2.hursley.ibm.com/decimal` 
*\[This URL will change.\]*

### Operator methods

Operations on `BigDecimal` numbers are controlled by a `https://developer.android.com/reference/kotlin/android/icu/math/MathContext` object, which provides the context (precision and other information) for the operation. Methods that can take a `MathContext` parameter implement the standard arithmetic operators for `BigDecimal` objects and are known as *operator methods* . The default settings provided by the constant `https://developer.android.com/reference/kotlin/android/icu/math/MathContext#DEFAULT:android.icu.math.MathContext` (`digits=9, form=SCIENTIFIC, lostDigits=false, roundingMode=ROUND_HALF_UP`) perform general-purpose floating point arithmetic to nine digits of precision. The `MathContext` parameter must not be `null`.

Each operator method also has a version provided which does not take a `MathContext` parameter. For this version of each method, the context settings used are `digits=0, form=PLAIN, lostDigits=false, roundingMode=ROUND_HALF_UP`; these settings perform fixed point arithmetic with unlimited precision, as defined for the original BigDecimal class in Java 1.1 and Java 1.2.

For monadic operators, only the optional `MathContext` parameter is present; the operation acts upon the current object.

For dyadic operators, a `BigDecimal` parameter is always present; it must not be `null`. The operation acts with the current object being the left-hand operand and the `BigDecimal` parameter being the right-hand operand.

For example, adding two `BigDecimal` objects referred to by the names `award` and `extra` could be written as any of:

` award.add(extra)
award.add(extra, MathContext.DEFAULT)
award.add(extra, acontext) `

(where `acontext` is a `MathContext` object), which would return a `BigDecimal` object whose value is the result of adding `award` and `extra` under the appropriate context settings.

When a `BigDecimal` operator method is used, a set of rules define what the result will be (and, by implication, how the result would be represented as a character string). These rules are defined in the BigDecimal arithmetic documentation (see the URL above), but in summary:

- Results are normally calculated with up to some maximum number of significant digits. For example, if the `MathContext` parameter for an operation were `MathContext.DEFAULT` then the result would be rounded to 9 digits; the division of 2 by 3 would then result in 0.666666667. 
 You can change the default of 9 significant digits by providing the method with a suitable `MathContext` object. This lets you calculate using as many digits as you need -- thousands, if necessary. Fixed point (scaled) arithmetic is indicated by using a `digits` setting of 0 (or omitting the `MathContext` parameter). 
 Similarly, you can change the algorithm used for rounding from the default "classic" algorithm.
- In standard arithmetic (that is, when the `form` setting is not `PLAIN`), a zero result is always expressed as the single digit `'0'` (that is, with no sign, decimal point, or exponent part).
- Except for the division and power operators in standard arithmetic, trailing zeros are preserved (this is in contrast to binary floating point operations and most electronic calculators, which lose the information about trailing zeros in the fractional part of results). 
 So, for example:

 ` new BigDecimal("2.40").add( new BigDecimal("2")) => "4.40"
 new BigDecimal("2.40").subtract(new BigDecimal("2")) => "0.40"
 new BigDecimal("2.40").multiply(new BigDecimal("2")) => "4.80"
 new BigDecimal("2.40").divide( new BigDecimal("2"), def) => "1.2" `

 where the value on the right of the `=>` would be the result of the operation, expressed as a `String`, and `def` (in this and following examples) refers to `MathContext.DEFAULT` ). This preservation of trailing zeros is desirable for most calculations (including financial calculations). If necessary, trailing zeros may be easily removed using division by 1.
- In standard arithmetic, exponential form is used for a result depending on its value and the current setting of `digits` (the default is 9 digits). If the number of places needed before the decimal point exceeds the `digits` setting, or the absolute value of the number is less than `0.000001`, then the number will be expressed in exponential notation; thus

 ` new BigDecimal("1e+6").multiply(new BigDecimal("1e+6"), def) `

 results in `1E+12` instead of `1000000000000`, and

 ` new BigDecimal("1").divide(new BigDecimal("3E+10"), def) `

 results in `3.33333333E-11` instead of `0.0000000000333333333`.

 The form of the exponential notation (scientific or engineering) is determined by the `form` setting.

The names of methods in this class follow the conventions established by `java.lang.Number`, `java.math.BigInteger`, and `java.math.BigDecimal` in Java 1.1 and Java 1.2.

## Summary

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#ROUND_CEILING:kotlin.Int` Rounding mode to round to a more positive number. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#ROUND_DOWN:kotlin.Int` Rounding mode to round towards zero. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#ROUND_FLOOR:kotlin.Int` Rounding mode to round to a more negative number. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#ROUND_HALF_DOWN:kotlin.Int` Rounding mode to round to nearest neighbor, where an equidistant value is rounded down. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#ROUND_HALF_EVEN:kotlin.Int` Rounding mode to round to nearest neighbor, where an equidistant value is rounded to the nearest even neighbor. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#ROUND_HALF_UP:kotlin.Int` Rounding mode to round to nearest neighbor, where an equidistant value is rounded up. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#ROUND_UNNECESSARY:kotlin.Int` Rounding mode to assert that no rounding is necessary. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#ROUND_UP:kotlin.Int` Rounding mode to round away from zero. |

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#BigDecimal(kotlin.CharArray)(inchars: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html!)` Constructs a `BigDecimal` object from an array of characters. |
| `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#BigDecimal(kotlin.CharArray,%20kotlin.Int,%20kotlin.Int)(inchars: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html!, offset: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, length: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Constructs a `BigDecimal` object from an array of characters. |
| `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#BigDecimal(kotlin.Double)(num: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)` Constructs a `BigDecimal` object directly from a `double`. |
| `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#BigDecimal(kotlin.Int)(num: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Constructs a `BigDecimal` object directly from a `int`. |
| `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#BigDecimal(kotlin.String)(string: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Constructs a `BigDecimal` object from a `String`. |
| `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#BigDecimal(java.math.BigDecimal)(bd: https://developer.android.com/reference/kotlin/java/math/BigDecimal.html#!)` Constructs a `BigDecimal` object from a `java.math.BigDecimal`. |
| `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#BigDecimal(java.math.BigInteger)(bi: https://developer.android.com/reference/kotlin/java/math/BigInteger.html#!)` Constructs a `BigDecimal` object from a `BigInteger`, with scale 0. |
| `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#BigDecimal(java.math.BigInteger,%20kotlin.Int)(bi: https://developer.android.com/reference/kotlin/java/math/BigInteger.html#!, scale: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Constructs a `BigDecimal` object from a `BigInteger` and a scale. |
| `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#BigDecimal(kotlin.Long)(num: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Constructs a `BigDecimal` object directly from a `long`. |

| Public methods ||
|---|---|
| open [BigDecimal](BigDecimal.md)! | `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#abs()()` Returns a plain `BigDecimal` whose value is the absolute value of this `BigDecimal`. |
| open [BigDecimal](BigDecimal.md)! | `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#abs(android.icu.math.MathContext)(set: https://developer.android.com/reference/kotlin/android/icu/math/MathContext!)` Returns a `BigDecimal` whose value is the absolute value of this `BigDecimal`. |
| open [BigDecimal](BigDecimal.md)! | `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#add(android.icu.math.BigDecimal)(rhs: https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#!)` Returns a plain `BigDecimal` whose value is `this+rhs`, using fixed point arithmetic. |
| --- | --- |
| open [BigDecimal](BigDecimal.md)! | `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#add(android.icu.math.BigDecimal,%20android.icu.math.MathContext)(rhs: https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#!, set: https://developer.android.com/reference/kotlin/android/icu/math/MathContext!)` Returns a `BigDecimal` whose value is `this+rhs`. |
| open [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#byteValueExact()()` Converts this `BigDecimal` to a `byte`. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#compareTo(android.icu.math.BigDecimal)(other: https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#!)` Compares this `BigDecimal` to another, using unlimited precision. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#compareTo(android.icu.math.BigDecimal,%20android.icu.math.MathContext)(rhs: https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#!, set: https://developer.android.com/reference/kotlin/android/icu/math/MathContext!)` Compares this `BigDecimal` to another. |
| open [BigDecimal](BigDecimal.md)! | `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#divide(android.icu.math.BigDecimal)(rhs: https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#!)` Returns a plain `BigDecimal` whose value is `this/rhs`, using fixed point arithmetic. |
| open [BigDecimal](BigDecimal.md)! | `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#divide(android.icu.math.BigDecimal,%20android.icu.math.MathContext)(rhs: https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#!, set: https://developer.android.com/reference/kotlin/android/icu/math/MathContext!)` Returns a `BigDecimal` whose value is `this/rhs`. |
| --- | --- |
| open [BigDecimal](BigDecimal.md)! | `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#divide(android.icu.math.BigDecimal,%20kotlin.Int)(rhs: https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#!, round: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns a plain `BigDecimal` whose value is `this/rhs`, using fixed point arithmetic and a rounding mode. |
| open [BigDecimal](BigDecimal.md)! | `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#divide(android.icu.math.BigDecimal,%20kotlin.Int,%20kotlin.Int)(rhs: https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#!, scale: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, round: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns a plain `BigDecimal` whose value is `this/rhs`, using fixed point arithmetic and a given scale and rounding mode. |
| open [BigDecimal](BigDecimal.md)! | `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#divideInteger(android.icu.math.BigDecimal)(rhs: https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#!)` Returns a plain `BigDecimal` whose value is the integer part of `this/rhs`. |
| --- | --- |
| open [BigDecimal](BigDecimal.md)! | `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#divideInteger(android.icu.math.BigDecimal,%20android.icu.math.MathContext)(rhs: https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#!, set: https://developer.android.com/reference/kotlin/android/icu/math/MathContext!)` Returns a `BigDecimal` whose value is the integer part of `this/rhs`. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Compares this `BigDecimal` with `rhs` for equality. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#format(kotlin.Int,%20kotlin.Int)(before: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, after: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the `String` representation of this `BigDecimal`, modified by layout parameters. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#format(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)(before: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, after: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, explaces: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, exdigits: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, exformint: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, exround: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the `String` representation of this `BigDecimal`, modified by layout parameters and allowing exponential notation. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#hashCode()()` Returns the hashcode for this `BigDecimal`. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#intValueExact()()` Converts this `BigDecimal` to an `int`. |
| --- | --- |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#longValueExact()()` Converts this `BigDecimal` to a `long`. |
| open [BigDecimal](BigDecimal.md)! | `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#max(android.icu.math.BigDecimal)(rhs: https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#!)` Returns a plain `BigDecimal` whose value is the maximum of `this` and `rhs`. |
| open [BigDecimal](BigDecimal.md)! | `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#max(android.icu.math.BigDecimal,%20android.icu.math.MathContext)(rhs: https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#!, set: https://developer.android.com/reference/kotlin/android/icu/math/MathContext!)` Returns a `BigDecimal` whose value is the maximum of `this` and `rhs`. |
| --- | --- |
| open [BigDecimal](BigDecimal.md)! | `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#min(android.icu.math.BigDecimal)(rhs: https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#!)` Returns a plain `BigDecimal` whose value is the minimum of `this` and `rhs`. |
| open [BigDecimal](BigDecimal.md)! | `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#min(android.icu.math.BigDecimal,%20android.icu.math.MathContext)(rhs: https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#!, set: https://developer.android.com/reference/kotlin/android/icu/math/MathContext!)` Returns a `BigDecimal` whose value is the minimum of `this` and `rhs`. |
| open [BigDecimal](BigDecimal.md)! | `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#movePointLeft(kotlin.Int)(n: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns a plain `BigDecimal` whose decimal point has been moved to the left by a specified number of positions. |
| --- | --- |
| open [BigDecimal](BigDecimal.md)! | `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#movePointRight(kotlin.Int)(n: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns a plain `BigDecimal` whose decimal point has been moved to the right by a specified number of positions. |
| open [BigDecimal](BigDecimal.md)! | `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#multiply(android.icu.math.BigDecimal)(rhs: https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#!)` Returns a plain `BigDecimal` whose value is `this*rhs`, using fixed point arithmetic. |
| open [BigDecimal](BigDecimal.md)! | `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#multiply(android.icu.math.BigDecimal,%20android.icu.math.MathContext)(rhs: https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#!, set: https://developer.android.com/reference/kotlin/android/icu/math/MathContext!)` Returns a `BigDecimal` whose value is `this*rhs`. |
| --- | --- |
| open [BigDecimal](BigDecimal.md)! | `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#negate()()` Returns a plain `BigDecimal` whose value is `-this`. |
| open [BigDecimal](BigDecimal.md)! | `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#negate(android.icu.math.MathContext)(set: https://developer.android.com/reference/kotlin/android/icu/math/MathContext!)` Returns a `BigDecimal` whose value is `-this`. |
| open [BigDecimal](BigDecimal.md)! | `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#plus()()` Returns a plain `BigDecimal` whose value is `+this`. |
| --- | --- |
| open [BigDecimal](BigDecimal.md)! | `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#plus(android.icu.math.MathContext)(set: https://developer.android.com/reference/kotlin/android/icu/math/MathContext!)` Returns a `BigDecimal` whose value is `+this`. |
| open [BigDecimal](BigDecimal.md)! | `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#pow(android.icu.math.BigDecimal)(rhs: https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#!)` Returns a plain `BigDecimal` whose value is `this**rhs`, using fixed point arithmetic. |
| open [BigDecimal](BigDecimal.md)! | `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#pow(android.icu.math.BigDecimal,%20android.icu.math.MathContext)(rhs: https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#!, set: https://developer.android.com/reference/kotlin/android/icu/math/MathContext!)` Returns a `BigDecimal` whose value is `this**rhs`. |
| --- | --- |
| open [BigDecimal](BigDecimal.md)! | `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#remainder(android.icu.math.BigDecimal)(rhs: https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#!)` Returns a plain `BigDecimal` whose value is the remainder of `this/rhs`, using fixed point arithmetic. |
| open [BigDecimal](BigDecimal.md)! | `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#remainder(android.icu.math.BigDecimal,%20android.icu.math.MathContext)(rhs: https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#!, set: https://developer.android.com/reference/kotlin/android/icu/math/MathContext!)` Returns a `BigDecimal` whose value is the remainder of `this/rhs`. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#scale()()` Returns the scale of this `BigDecimal`. |
| --- | --- |
| open [BigDecimal](BigDecimal.md)! | `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#setScale(kotlin.Int)(scale: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns a plain `BigDecimal` with a given scale. |
| open [BigDecimal](BigDecimal.md)! | `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#setScale(kotlin.Int,%20kotlin.Int)(scale: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, round: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns a plain `BigDecimal` with a given scale. |
| open [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#shortValueExact()()` Converts this `BigDecimal` to a `short`. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#signum()()` Returns the sign of this `BigDecimal`, as an `int`. |
| open [BigDecimal](BigDecimal.md)! | `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#subtract(android.icu.math.BigDecimal)(rhs: https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#!)` Returns a plain `BigDecimal` whose value is `this-rhs`, using fixed point arithmetic. |
| open [BigDecimal](BigDecimal.md)! | `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#subtract(android.icu.math.BigDecimal,%20android.icu.math.MathContext)(rhs: https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#!, set: https://developer.android.com/reference/kotlin/android/icu/math/MathContext!)` Returns a `BigDecimal` whose value is `this-rhs`. |
| --- | --- |
| open [BigDecimal](../java.math/BigDecimal.md)! | `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#toBigDecimal()()` Converts this `BigDecimal` to a `java.math.BigDecimal`. |
| open [BigInteger](../java.math/BigInteger.md)! | `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#toBigInteger()()` Converts this `BigDecimal` to a `java.math.BigInteger`. |
| open [BigInteger](../java.math/BigInteger.md)! | `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#toBigIntegerExact()()` Converts this `BigDecimal` to a `java.math.BigInteger`. |
| --- | --- |
| open [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)! | `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#toCharArray()()` Returns the `BigDecimal` as a character array. |
| open [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#toDouble()()` Converts this `BigDecimal` to a `double`. |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#toFloat()()` Converts this `BigDecimal` to a `float`. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#toInt()()` Converts this `BigDecimal` to an `int`. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#toLong()()` Converts this `BigDecimal` to a `long`. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#toString()()` Returns the `BigDecimal` as a `String`. |
| --- | --- |
| open [BigInteger](../java.math/BigInteger.md)! | `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#unscaledValue()()` Returns the number as a `BigInteger` after removing the scale. |
| open static [BigDecimal](BigDecimal.md)! | `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#valueOf(kotlin.Double)(dub: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)` Translates a `double` to a `BigDecimal`. |
| open static [BigDecimal](BigDecimal.md)! | `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#valueOf(kotlin.Long)(lint: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Translates a `long` to a `BigDecimal`. |
| --- | --- |
| open static [BigDecimal](BigDecimal.md)! | `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#valueOf(kotlin.Long,%20kotlin.Int)(lint: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html, scale: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Translates a `long` to a `BigDecimal` with a given scale. |

| Properties ||
|---|---|
| static [BigDecimal](BigDecimal.md)! | `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#ONE:android.icu.math.BigDecimal` The `BigDecimal` constant "1". |
| static [BigDecimal](BigDecimal.md)! | `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#TEN:android.icu.math.BigDecimal` The `BigDecimal` constant "10". |
| static [BigDecimal](BigDecimal.md)! | `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#ZERO:android.icu.math.BigDecimal` The `BigDecimal` constant "0". |
| --- | --- |

## Constants

### ROUND_CEILING

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ROUND_CEILING: Int
```

Rounding mode to round to a more positive number.

 Value: 2

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/math/MathContext#ROUND_CEILING:kotlin.Int`

### ROUND_DOWN

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ROUND_DOWN: Int
```

Rounding mode to round towards zero.

 Value: 1

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/math/MathContext#ROUND_DOWN:kotlin.Int`

### ROUND_FLOOR

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ROUND_FLOOR: Int
```

Rounding mode to round to a more negative number.

 Value: 3

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/math/MathContext#ROUND_FLOOR:kotlin.Int`

### ROUND_HALF_DOWN

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ROUND_HALF_DOWN: Int
```

Rounding mode to round to nearest neighbor, where an equidistant value is rounded down.

 Value: 5

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/math/MathContext#ROUND_HALF_DOWN:kotlin.Int`

### ROUND_HALF_EVEN

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ROUND_HALF_EVEN: Int
```

Rounding mode to round to nearest neighbor, where an equidistant value is rounded to the nearest even neighbor.

 Value: 6

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/math/MathContext#ROUND_HALF_EVEN:kotlin.Int`

### ROUND_HALF_UP

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ROUND_HALF_UP: Int
```

Rounding mode to round to nearest neighbor, where an equidistant value is rounded up.

 Value: 4

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/math/MathContext#ROUND_HALF_UP:kotlin.Int`

### ROUND_UNNECESSARY

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ROUND_UNNECESSARY: Int
```

Rounding mode to assert that no rounding is necessary.

 Value: 7

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/math/MathContext#ROUND_UNNECESSARY:kotlin.Int`

### ROUND_UP

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ROUND_UP: Int
```

Rounding mode to round away from zero.

 Value: 0

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/math/MathContext#ROUND_UP:kotlin.Int`

## Public constructors

### BigDecimal

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
BigDecimal(inchars: CharArray!)
```

Constructs a `BigDecimal` object from an array of characters.

Constructs a `BigDecimal` as though a `String` had been constructed from the character array and the `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#BigDecimal(kotlin.String)` constructor had then been used. The parameter must not be `null`.

Using this constructor is faster than using the `BigDecimal(String)` constructor if the string is already available in character array form.

| Parameters ||
|---|---|
| `inchars` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!: The `char[]` array containing the number to be converted. |

| Exceptions ||
|---|---|
| `java.lang.NumberFormatException` | If the parameter is not a valid number. |

### BigDecimal

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
BigDecimal(
    inchars: CharArray!, 
    offset: Int, 
    length: Int)
```

Constructs a `BigDecimal` object from an array of characters.

Constructs a `BigDecimal` as though a `String` had been constructed from the character array (or a subarray of that array) and the `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#BigDecimal(kotlin.String)` constructor had then been used. The first parameter must not be `null`, and the subarray must be wholly contained within it.

Using this constructor is faster than using the `BigDecimal(String)` constructor if the string is already available within a character array.

| Parameters ||
|---|---|
| `inchars` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!: The `char[]` array containing the number to be converted. |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The `int` offset into the array of the start of the number to be converted. |
| `length` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The `int` length of the number. |
| --- | --- |

| Exceptions ||
|---|---|
| `java.lang.NumberFormatException` | If the parameter is not a valid number for any reason. |

### BigDecimal

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
BigDecimal(num: Double)
```

Constructs a `BigDecimal` object directly from a `double`.

Constructs a `BigDecimal` which is the exact decimal representation of the 64-bit signed binary floating point parameter.

Note that this constructor it an exact conversion; it does not give the same result as converting `num ` to a `String` using the `Double.toString()` method and then using the `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#BigDecimal(kotlin.String)` constructor. To get that result, use the static `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#valueOf(kotlin.Double)` method to construct a `BigDecimal` from a `double`.

| Parameters ||
|---|---|
| `num` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html): The `double` to be converted. |

| Exceptions ||
|---|---|
| `java.lang.NumberFormatException` | If the parameter is infinite or not a number. |

### BigDecimal

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
BigDecimal(num: Int)
```

Constructs a `BigDecimal` object directly from a `int`.

Constructs a `BigDecimal` which is the exact decimal representation of the 32-bit signed binary integer parameter. The `BigDecimal` will contain only decimal digits, prefixed with a leading minus sign (hyphen) if the parameter is negative. A leading zero will be present only if the parameter is zero.

| Parameters ||
|---|---|
| `num` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The `int` to be converted. |

### BigDecimal

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
BigDecimal(string: String!)
```

Constructs a `BigDecimal` object from a `String`.

Constructs a `BigDecimal` from the parameter, which must not be `null` and must represent a valid *number* , as described formally in the documentation referred to `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#`.

In summary, numbers in `String` form must have at least one digit, may have a leading sign, may have a decimal point, and exponential notation may be used. They follow conventional syntax, and may not contain blanks.

Some valid strings from which a `BigDecimal` might be constructed are:

```kotlin
"0" -- Zero "12" -- A whole number "-76" -- A signed whole number "12.70" -- Some decimal places "+0.003" -- Plus
  sign is allowed "17." -- The same as 17 ".5" -- The same as 0.5 "4E+9" -- Exponential notation "0.73e-7" --
  Exponential notation
 
  
```

(Exponential notation means that the number includes an optional sign and a power of ten following an '`E`' that indicates how the decimal point will be shifted. Thus the `"4E+9"` above is just a short way of writing `4000000000`, and the `"0.73e-7"` is short for ` 0.000000073`.)

The `BigDecimal` constructed from the String is in a standard form, with no blanks, as though the `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#add(android.icu.math.BigDecimal)` method had been used to add zero to the number with unlimited precision. If the string uses exponential notation (that is, includes an `e` or an `E`), then the `BigDecimal ` number will be expressed in scientific notation (where the power of ten is adjusted so there is a single non-zero digit to the left of the decimal point); in this case if the number is zero then it will be expressed as the single digit 0, and if non-zero it will have an exponent unless that exponent would be 0. The exponent must fit in nine digits both before and after it is expressed in scientific notation.

Any digits in the parameter must be decimal; that is, `Character.digit(c, 10)` (where `c` is the character in question) would not return -1.

| Parameters ||
|---|---|
| `string` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The `String` to be converted. |

| Exceptions ||
|---|---|
| `java.lang.NumberFormatException` | If the parameter is not a valid number. |

### BigDecimal

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
BigDecimal(bd: BigDecimal!)
```

Constructs a `BigDecimal` object from a `java.math.BigDecimal`.

Constructs a `BigDecimal` as though the parameter had been represented as a `String` (using its `toString` method) and the `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#BigDecimal(kotlin.String)` constructor had then been used. The parameter must not be `null`.

*(Note: this constructor is provided only in the `android.icu.math` version of the BigDecimal class. It would not be present in a `java.math` version.)*

| Parameters ||
|---|---|
| `bd` | [BigDecimal](../java.math/BigDecimal.md)!: The `BigDecimal` to be translated. |

### BigDecimal

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
BigDecimal(bi: BigInteger!)
```

Constructs a `BigDecimal` object from a `BigInteger`, with scale 0.

Constructs a `BigDecimal` which is the exact decimal representation of the `BigInteger`, with a scale of zero. The value of the `BigDecimal` is identical to the value of the `BigInteger `. The parameter must not be `null`.

The `BigDecimal` will contain only decimal digits, prefixed with a leading minus sign (hyphen) if the `BigInteger` is negative. A leading zero will be present only if the `BigInteger` is zero.

| Parameters ||
|---|---|
| `bi` | [BigInteger](../java.math/BigInteger.md)!: The `BigInteger` to be converted. |

### BigDecimal

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
BigDecimal(
    bi: BigInteger!, 
    scale: Int)
```

Constructs a `BigDecimal` object from a `BigInteger` and a scale.

Constructs a `BigDecimal` which is the exact decimal representation of the `BigInteger`, scaled by the second parameter, which may not be negative. The value of the `BigDecimal` is the ` BigInteger` divided by ten to the power of the scale. The `BigInteger` parameter must not be `null`.

The `BigDecimal` will contain only decimal digits, (with an embedded decimal point followed by ` scale` decimal digits if the scale is positive), prefixed with a leading minus sign (hyphen) if the ` BigInteger` is negative. A leading zero will be present only if the `BigInteger` is zero.

| Parameters ||
|---|---|
| `bi` | [BigInteger](../java.math/BigInteger.md)!: The `BigInteger` to be converted. |
| `scale` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The `int` specifying the scale. |

| Exceptions ||
|---|---|
| `java.lang.NumberFormatException` | If the scale is negative. |

### BigDecimal

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
BigDecimal(num: Long)
```

Constructs a `BigDecimal` object directly from a `long`.

Constructs a `BigDecimal` which is the exact decimal representation of the 64-bit signed binary integer parameter. The `BigDecimal` will contain only decimal digits, prefixed with a leading minus sign (hyphen) if the parameter is negative. A leading zero will be present only if the parameter is zero.

| Parameters ||
|---|---|
| `num` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): The `long` to be converted. |

## Public methods

### abs

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun abs(): BigDecimal!
```

Returns a plain `BigDecimal` whose value is the absolute value of this `BigDecimal`.

The same as `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#abs(android.icu.math.MathContext)`, where the context is `new MathContext(0, MathContext.PLAIN)`.

The length of the decimal part (the scale) of the result will be `this.scale()`

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#!` | A `BigDecimal` whose value is the absolute value of this `BigDecimal`. |

### abs

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun abs(set: MathContext!): BigDecimal!
```

Returns a `BigDecimal` whose value is the absolute value of this `BigDecimal`.

If the current object is zero or positive, then the same result as invoking the `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#plus(android.icu.math.MathContext)` method with the same parameter is returned. Otherwise, the same result as invoking the `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#negate(android.icu.math.MathContext)` method with the same parameter is returned.

| Parameters ||
|---|---|
| `set` | [MathContext](MathContext.md)!: The `MathContext` arithmetic settings. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#!` | A `BigDecimal` whose value is the absolute value of this `BigDecimal`. |

### add

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun add(rhs: BigDecimal!): BigDecimal!
```

Returns a plain `BigDecimal` whose value is `this+rhs`, using fixed point arithmetic.

The same as `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#add(android.icu.math.BigDecimal,%20android.icu.math.MathContext)`, where the `BigDecimal` is `rhs`, and the context is `new MathContext(0, MathContext.PLAIN)`.

The length of the decimal part (the scale) of the result will be the maximum of the scales of the two operands.

| Parameters ||
|---|---|
| `rhs` | [BigDecimal](BigDecimal.md)!: The `BigDecimal` for the right hand side of the addition. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#!` | A `BigDecimal` whose value is `this+rhs`, using fixed point arithmetic. |

### add

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun add(
    rhs: BigDecimal!, 
    set: MathContext!
): BigDecimal!
```

Returns a `BigDecimal` whose value is `this+rhs`.

Implements the addition (**`+`** ) operator (as defined in the decimal documentation, see `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#`), and returns the result as a `BigDecimal` object.

| Parameters ||
|---|---|
| `rhs` | [BigDecimal](BigDecimal.md)!: The `BigDecimal` for the right hand side of the addition. |
| `set` | [MathContext](MathContext.md)!: The `MathContext` arithmetic settings. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#!` | A `BigDecimal` whose value is `this+rhs`. |

### byteValueExact

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun byteValueExact(): Byte
```

Converts this `BigDecimal` to a `byte`. If the `BigDecimal` has a non-zero decimal part or is out of the possible range for a `byte` (8-bit signed integer) result then an ` ArithmeticException` is thrown.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html` | A `byte` equal in value to `this`. |

| Exceptions ||
|---|---|
| `java.lang.ArithmeticException` | if `this` has a non-zero decimal part, or will not fit in a `byte`. |

### compareTo

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun compareTo(other: BigDecimal!): Int
```

Compares this `BigDecimal` to another, using unlimited precision.

The same as `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#compareTo(android.icu.math.BigDecimal,%20android.icu.math.MathContext)`, where the `BigDecimal` is `rhs`, and the context is `new MathContext(0, MathContext.PLAIN)`.

| Parameters ||
|---|---|
| `o` | the object to be compared. |
| `rhs` | The `BigDecimal` for the right hand side of the comparison. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | An `int` whose value is -1, 0, or 1 as `this` is numerically less than, equal to, or greater than `rhs`. |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the specified object's type prevents it from being compared to this object. |
| `java.lang.NullPointerException` | if the specified object is null |

### compareTo

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun compareTo(
    rhs: BigDecimal!, 
    set: MathContext!
): Int
```

Compares this `BigDecimal` to another.

Implements numeric comparison, (as defined in the decimal documentation, see `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#`), and returns a result of type `int`.

The result will be:

| **-1** | if the current object is less than the first parameter |
| --- | --- |
| **0** | if the current object is equal to the first parameter |
| **1** | if the current object is greater than the first parameter. |

A `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#compareTo(android.icu.math.BigDecimal)` method is also provided.

| Parameters ||
|---|---|
| `rhs` | [BigDecimal](BigDecimal.md)!: The `BigDecimal` for the right hand side of the comparison. |
| `set` | [MathContext](MathContext.md)!: The `MathContext` arithmetic settings. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | An `int` whose value is -1, 0, or 1 as `this` is numerically less than, equal to, or greater than `rhs`. |

### divide

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun divide(rhs: BigDecimal!): BigDecimal!
```

Returns a plain `BigDecimal` whose value is `this/rhs`, using fixed point arithmetic.

The same as `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#divide(android.icu.math.BigDecimal,%20kotlin.Int)`, where the `BigDecimal` is `rhs`, and the rounding mode is `https://developer.android.com/reference/kotlin/android/icu/math/MathContext#ROUND_HALF_UP:kotlin.Int`. The length of the decimal part (the scale) of the result will be the same as the scale of the current object, if the latter were formatted without exponential notation.

| Parameters ||
|---|---|
| `rhs` | [BigDecimal](BigDecimal.md)!: The `BigDecimal` for the right hand side of the division. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#!` | A plain `BigDecimal` whose value is `this/rhs`, using fixed point arithmetic. |

| Exceptions ||
|---|---|
| `java.lang.ArithmeticException` | If `rhs` is zero. |

### divide

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun divide(
    rhs: BigDecimal!, 
    set: MathContext!
): BigDecimal!
```

Returns a `BigDecimal` whose value is `this/rhs`.

Implements the division (**`/`** ) operator (as defined in the decimal documentation, see `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#`), and returns the result as a `BigDecimal` object.

| Parameters ||
|---|---|
| `rhs` | [BigDecimal](BigDecimal.md)!: The `BigDecimal` for the right hand side of the division. |
| `set` | [MathContext](MathContext.md)!: The `MathContext` arithmetic settings. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#!` | A `BigDecimal` whose value is `this/rhs`. |

| Exceptions ||
|---|---|
| `java.lang.ArithmeticException` | if `rhs` is zero. |

### divide

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun divide(
    rhs: BigDecimal!, 
    round: Int
): BigDecimal!
```

Returns a plain `BigDecimal` whose value is `this/rhs`, using fixed point arithmetic and a rounding mode.

The same as `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#divide(android.icu.math.BigDecimal,%20kotlin.Int,%20kotlin.Int)`, where the `BigDecimal` is `rhs`, and the second parameter is `this.scale()`, and the third is `round`.

The length of the decimal part (the scale) of the result will therefore be the same as the scale of the current object, if the latter were formatted without exponential notation.

<br />

| Parameters ||
|---|---|
| `rhs` | [BigDecimal](BigDecimal.md)!: The `BigDecimal` for the right hand side of the division. |
| `round` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The `int` rounding mode to be used for the division (see the `https://developer.android.com/reference/kotlin/android/icu/math/MathContext` class). |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#!` | A plain `BigDecimal` whose value is `this/rhs`, using fixed point arithmetic and the specified rounding mode. |

| Exceptions ||
|---|---|
| `java.lang.ArithmeticException` | if `round` is `https://developer.android.com/reference/kotlin/android/icu/math/MathContext#ROUND_UNNECESSARY:kotlin.Int` and `this.scale()` is insufficient to represent the result exactly. |
| `java.lang.IllegalArgumentException` | if `round` is not a valid rounding mode. |

### divide

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun divide(
    rhs: BigDecimal!, 
    scale: Int, 
    round: Int
): BigDecimal!
```

Returns a plain `BigDecimal` whose value is `this/rhs`, using fixed point arithmetic and a given scale and rounding mode.

The same as `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#divide(android.icu.math.BigDecimal,%20android.icu.math.MathContext)`, where the `BigDecimal` is `rhs`, `new MathContext(0, MathContext.PLAIN, false, round)`, except that the length of the decimal part (the scale) to be used for the result is explicit rather than being taken from `this`.

The length of the decimal part (the scale) of the result will be the same as the scale of the current object, if the latter were formatted without exponential notation.

<br />

| Parameters ||
|---|---|
| `rhs` | [BigDecimal](BigDecimal.md)!: The `BigDecimal` for the right hand side of the division. |
| `scale` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The `int` scale to be used for the result. |
| `round` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The `int` rounding mode to be used for the division (see the `https://developer.android.com/reference/kotlin/android/icu/math/MathContext` class). |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#!` | A plain `BigDecimal` whose value is `this/rhs`, using fixed point arithmetic and the specified rounding mode. |

| Exceptions ||
|---|---|
| `java.lang.ArithmeticException` | if `round` is `https://developer.android.com/reference/kotlin/android/icu/math/MathContext#ROUND_UNNECESSARY:kotlin.Int` and `scale` is insufficient to represent the result exactly. |
| `java.lang.IllegalArgumentException` | if `round` is not a valid rounding mode. |

### divideInteger

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun divideInteger(rhs: BigDecimal!): BigDecimal!
```

Returns a plain `BigDecimal` whose value is the integer part of `this/rhs`.

The same as `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#divideInteger(android.icu.math.BigDecimal,%20android.icu.math.MathContext)`, where the `BigDecimal` is `rhs `, and the context is `new MathContext(0, MathContext.PLAIN)`.

| Parameters ||
|---|---|
| `rhs` | [BigDecimal](BigDecimal.md)!: The `BigDecimal` for the right hand side of the integer division. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#!` | A `BigDecimal` whose value is the integer part of `this/rhs`. |

| Exceptions ||
|---|---|
| `java.lang.ArithmeticException` | if `rhs` is zero. |

### divideInteger

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun divideInteger(
    rhs: BigDecimal!, 
    set: MathContext!
): BigDecimal!
```

Returns a `BigDecimal` whose value is the integer part of `this/rhs`.

Implements the integer division operator (as defined in the decimal documentation, see `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#`), and returns the result as a `BigDecimal` object.

| Parameters ||
|---|---|
| `rhs` | [BigDecimal](BigDecimal.md)!: The `BigDecimal` for the right hand side of the integer division. |
| `set` | [MathContext](MathContext.md)!: The `MathContext` arithmetic settings. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#!` | A `BigDecimal` whose value is the integer part of `this/rhs`. |

| Exceptions ||
|---|---|
| `java.lang.ArithmeticException` | if the result will not fit in the number of digits specified for the context. |

### equals

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun equals(other: Any?): Boolean
```

Compares this `BigDecimal` with `rhs` for equality.

If the parameter is `null`, or is not an instance of the BigDecimal type, or is not exactly equal to the current `BigDecimal` object, then *false* is returned. Otherwise, *true* is returned.

"Exactly equal", here, means that the `String` representations of the `BigDecimal` numbers are identical (they have the same characters in the same sequence).

The `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#compareTo(android.icu.math.BigDecimal,%20android.icu.math.MathContext)` method should be used for more general comparisons.

| Parameters ||
|---|---|
| `obj` | The `Object` for the right hand side of the comparison. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | A `boolean` whose value *true* if and only if the operands have identical string representations. |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if `rhs` cannot be cast to a `BigDecimal` object. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#compareTo(android.icu.math.BigDecimal)`
- `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#compareTo(android.icu.math.BigDecimal,%20android.icu.math.MathContext)`

### format

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun format(
    before: Int, 
    after: Int
): String!
```

Returns the `String` representation of this `BigDecimal`, modified by layout parameters.

*This method is provided as a primitive for use by more sophisticated classes, such as `DecimalFormat `, that can apply locale-sensitive editing of the result. The level of formatting that it provides is a necessary part of the BigDecimal class as it is sensitive to and must follow the calculation and rounding rules for BigDecimal arithmetic. However, if the function is provided elsewhere, it may be removed from this class.*

The parameters, for both forms of the `format` method are all of type `int`. A value of -1 for any parameter indicates that the default action or value for that parameter should be used.

The parameters, `before` and `after`, specify the number of characters to be used for the integer part and decimal part of the result respectively. Exponential notation is not used. If either parameter is -1 (which indicates the default action), the number of characters used will be exactly as many as are needed for that part.

`before` must be a positive number; if it is larger than is needed to contain the integer part, that part is padded on the left with blanks to the requested length. If `before` is not large enough to contain the integer part of the number (including the sign, for negative numbers) an exception is thrown.

`after` must be a non-negative number; if it is not the same size as the decimal part of the number, the number will be rounded (or extended with zeros) to fit. Specifying 0 for `after` will cause the number to be rounded to an integer (that is, it will have no decimal part or decimal point). The rounding method will be the default, `MathContext.ROUND_HALF_UP`.

Other rounding methods, and the use of exponential notation, can be selected by using `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#format(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)`. Using the two-parameter form of the method has exactly the same effect as using the six-parameter form with the final four parameters all being -1.

| Parameters ||
|---|---|
| `before` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The `int` specifying the number of places before the decimal point. Use -1 for 'as many as are needed'. |
| `after` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The `int` specifying the number of places after the decimal point. Use -1 for 'as many as are needed'. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | A `String` representing this `BigDecimal`, laid out according to the specified parameters |

| Exceptions ||
|---|---|
| `java.lang.ArithmeticException` | if the number cannot be laid out as requested. |
| `java.lang.IllegalArgumentException` | if a parameter is out of range. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#toString()`
- `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#toCharArray()`

### format

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun format(
    before: Int, 
    after: Int, 
    explaces: Int, 
    exdigits: Int, 
    exformint: Int, 
    exround: Int
): String!
```

Returns the `String` representation of this `BigDecimal`, modified by layout parameters and allowing exponential notation.

*This method is provided as a primitive for use by more sophisticated classes, such as `DecimalFormat `, that can apply locale-sensitive editing of the result. The level of formatting that it provides is a necessary part of the BigDecimal class as it is sensitive to and must follow the calculation and rounding rules for BigDecimal arithmetic. However, if the function is provided elsewhere, it may be removed from this class.*

The parameters are all of type `int`. A value of -1 for any parameter indicates that the default action or value for that parameter should be used.

The first two parameters (`before` and `after`) specify the number of characters to be used for the integer part and decimal part of the result respectively, as defined for `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#format(kotlin.Int,%20kotlin.Int)`. If either of these is -1 (which indicates the default action), the number of characters used will be exactly as many as are needed for that part.

The remaining parameters control the use of exponential notation and rounding. Three (`explaces`, `exdigits`, and `exform`) control the exponent part of the result. As before, the default action for any of these parameters may be selected by using the value -1.

`explaces` must be a positive number; it sets the number of places (digits after the sign of the exponent) to be used for any exponent part, the default (when `explaces` is -1) being to use as many as are needed. If `explaces` is not -1, space is always reserved for an exponent; if one is not needed (for example, if the exponent will be 0) then `explaces`+2 blanks are appended to the result. (This preserves vertical alignment of similarly formatted numbers in a monospace font.) If `explaces ` is not -1 and is not large enough to contain the exponent, an exception is thrown.

`exdigits` sets the trigger point for use of exponential notation. If, before any rounding, the number of places needed before the decimal point exceeds `exdigits`, or if the absolute value of the result is less than `0.000001`, then exponential form will be used, provided that `exdigits` was specified. When `exdigits` is -1, exponential notation will never be used. If 0 is specified for `exdigits`, exponential notation is always used unless the exponent would be 0.

`exform` sets the form for exponential notation (if needed). It may be either `https://developer.android.com/reference/kotlin/android/icu/math/MathContext#SCIENTIFIC:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/icu/math/MathContext#ENGINEERING:kotlin.Int`. If the latter, engineering, form is requested, up to three digits (plus sign, if negative) may be needed for the integer part of the result (`before` ). Otherwise, only one digit (plus sign, if negative) is needed.

Finally, the sixth argument, `exround`, selects the rounding algorithm to be used, and must be one of the values indicated by a public constant in the `https://developer.android.com/reference/kotlin/android/icu/math/MathContext` class whose name starts with `ROUND_ `. The default (`ROUND_HALF_UP`) may also be selected by using the value -1, as before.

The special value `MathContext.ROUND_UNNECESSARY` may be used to detect whether non-zero digits are discarded -- if `exround` has this value than if non-zero digits would be discarded (rounded) during formatting then an `ArithmeticException` is thrown.

| Parameters ||
|---|---|
| `before` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The `int` specifying the number of places before the decimal point. Use -1 for 'as many as are needed'. |
| `after` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The `int` specifying the number of places after the decimal point. Use -1 for 'as many as are needed'. |
| `explaces` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The `int` specifying the number of places to be used for any exponent. Use -1 for 'as many as are needed'. |
| --- | --- |
| `exdigits` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The `int` specifying the trigger (digits before the decimal point) which if exceeded causes exponential notation to be used. Use 0 to force exponential notation. Use -1 to force plain notation (no exponential notation). |
| `exformint` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The `int` specifying the form of exponential notation to be used ( `https://developer.android.com/reference/kotlin/android/icu/math/MathContext#SCIENTIFIC:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/icu/math/MathContext#ENGINEERING:kotlin.Int`). |
| `exround` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The `int` specifying the rounding mode to use. Use -1 for the default, `https://developer.android.com/reference/kotlin/android/icu/math/MathContext#ROUND_HALF_UP:kotlin.Int`. |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | A `String` representing this `BigDecimal`, laid out according to the specified parameters |

| Exceptions ||
|---|---|
| `java.lang.ArithmeticException` | if the number cannot be laid out as requested. |
| `java.lang.IllegalArgumentException` | if a parameter is out of range. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#toString()`
- `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#toCharArray()`

### hashCode

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun hashCode(): Int
```

Returns the hashcode for this `BigDecimal`. This hashcode is suitable for use by the ` java.util.Hashtable` class.

Note that two `BigDecimal` objects are only guaranteed to produce the same hashcode if they are exactly equal (that is, the `String` representations of the `BigDecimal` numbers are identical -- they have the same characters in the same sequence).

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | An `int` that is the hashcode for `this`. |

### intValueExact

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun intValueExact(): Int
```

Converts this `BigDecimal` to an `int`. If the `BigDecimal` has a non-zero decimal part or is out of the possible range for an `int` (32-bit signed integer) result then an `ArithmeticException` is thrown.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | An `int` equal in value to `this`. |

| Exceptions ||
|---|---|
| `java.lang.ArithmeticException` | if `this` has a non-zero decimal part, or will not fit in an `int`. |

### longValueExact

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun longValueExact(): Long
```

Converts this `BigDecimal` to a `long`. If the `BigDecimal` has a non-zero decimal part or is out of the possible range for a `long` (64-bit signed integer) result then an `ArithmeticException` is thrown.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | A `long` equal in value to `this`. |

| Exceptions ||
|---|---|
| `java.lang.ArithmeticException` | if `this` has a non-zero decimal part, or will not fit in a `long`. |

### max

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun max(rhs: BigDecimal!): BigDecimal!
```

Returns a plain `BigDecimal` whose value is the maximum of `this` and `rhs`.

The same as `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#max(android.icu.math.BigDecimal,%20android.icu.math.MathContext)`, where the `BigDecimal` is `rhs`, and the context is `new MathContext(0, MathContext.PLAIN)`.

| Parameters ||
|---|---|
| `rhs` | [BigDecimal](BigDecimal.md)!: The `BigDecimal` for the right hand side of the comparison. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#!` | A `BigDecimal` whose value is the maximum of `this` and `rhs`. |

### max

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun max(
    rhs: BigDecimal!, 
    set: MathContext!
): BigDecimal!
```

Returns a `BigDecimal` whose value is the maximum of `this` and `rhs`.

Returns the larger of the current object and the first parameter.

If calling the `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#compareTo(android.icu.math.BigDecimal,%20android.icu.math.MathContext)` method with the same parameters would return `1 ` or `0`, then the result of calling the `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#plus(android.icu.math.MathContext)` method on the current object (using the same `MathContext` parameter) is returned. Otherwise, the result of calling the `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#plus(android.icu.math.MathContext)` method on the first parameter object (using the same `MathContext` parameter) is returned.

| Parameters ||
|---|---|
| `rhs` | [BigDecimal](BigDecimal.md)!: The `BigDecimal` for the right hand side of the comparison. |
| `set` | [MathContext](MathContext.md)!: The `MathContext` arithmetic settings. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#!` | A `BigDecimal` whose value is the maximum of `this` and `rhs`. |

### min

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun min(rhs: BigDecimal!): BigDecimal!
```

Returns a plain `BigDecimal` whose value is the minimum of `this` and `rhs`.

The same as `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#min(android.icu.math.BigDecimal,%20android.icu.math.MathContext)`, where the `BigDecimal` is `rhs`, and the context is `new MathContext(0, MathContext.PLAIN)`.

| Parameters ||
|---|---|
| `rhs` | [BigDecimal](BigDecimal.md)!: The `BigDecimal` for the right hand side of the comparison. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#!` | A `BigDecimal` whose value is the minimum of `this` and `rhs`. |

### min

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun min(
    rhs: BigDecimal!, 
    set: MathContext!
): BigDecimal!
```

Returns a `BigDecimal` whose value is the minimum of `this` and `rhs`.

Returns the smaller of the current object and the first parameter.

If calling the `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#compareTo(android.icu.math.BigDecimal,%20android.icu.math.MathContext)` method with the same parameters would return `-1 ` or `0`, then the result of calling the `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#plus(android.icu.math.MathContext)` method on the current object (using the same `MathContext` parameter) is returned. Otherwise, the result of calling the `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#plus(android.icu.math.MathContext)` method on the first parameter object (using the same `MathContext` parameter) is returned.

| Parameters ||
|---|---|
| `rhs` | [BigDecimal](BigDecimal.md)!: The `BigDecimal` for the right hand side of the comparison. |
| `set` | [MathContext](MathContext.md)!: The `MathContext` arithmetic settings. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#!` | A `BigDecimal` whose value is the minimum of `this` and `rhs`. |

### movePointLeft

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun movePointLeft(n: Int): BigDecimal!
```

Returns a plain `BigDecimal` whose decimal point has been moved to the left by a specified number of positions. The parameter, `n`, specifies the number of positions to move the decimal point. That is, if `n` is 0 or positive, the number returned is given by:

` this.multiply(TEN.pow(new BigDecimal(-n))) `

`n` may be negative, in which case the method returns the same result as `movePointRight(-n) `.

| Parameters ||
|---|---|
| `n` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The `int` specifying the number of places to move the decimal point leftwards. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#!` | A `BigDecimal` derived from `this`, with the decimal point moved `n` places to the left. |

### movePointRight

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun movePointRight(n: Int): BigDecimal!
```

Returns a plain `BigDecimal` whose decimal point has been moved to the right by a specified number of positions. The parameter, `n`, specifies the number of positions to move the decimal point. That is, if `n` is 0 or positive, the number returned is given by:

` this.multiply(TEN.pow(new BigDecimal(n))) `

`n` may be negative, in which case the method returns the same result as `movePointLeft(-n) `.

| Parameters ||
|---|---|
| `n` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The `int` specifying the number of places to move the decimal point rightwards. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#!` | A `BigDecimal` derived from `this`, with the decimal point moved `n` places to the right. |

### multiply

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun multiply(rhs: BigDecimal!): BigDecimal!
```

Returns a plain `BigDecimal` whose value is `this*rhs`, using fixed point arithmetic.

The same as `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#add(android.icu.math.BigDecimal,%20android.icu.math.MathContext)`, where the `BigDecimal` is `rhs`, and the context is `new MathContext(0, MathContext.PLAIN)`.

The length of the decimal part (the scale) of the result will be the sum of the scales of the operands, if they were formatted without exponential notation.

| Parameters ||
|---|---|
| `rhs` | [BigDecimal](BigDecimal.md)!: The `BigDecimal` for the right hand side of the multiplication. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#!` | A `BigDecimal` whose value is `this*rhs`, using fixed point arithmetic. |

### multiply

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun multiply(
    rhs: BigDecimal!, 
    set: MathContext!
): BigDecimal!
```

Returns a `BigDecimal` whose value is `this*rhs`.

Implements the multiplication (**`*`** ) operator (as defined in the decimal documentation, see `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#`), and returns the result as a `BigDecimal` object.

| Parameters ||
|---|---|
| `rhs` | [BigDecimal](BigDecimal.md)!: The `BigDecimal` for the right hand side of the multiplication. |
| `set` | [MathContext](MathContext.md)!: The `MathContext` arithmetic settings. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#!` | A `BigDecimal` whose value is `this*rhs`. |

### negate

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun negate(): BigDecimal!
```

Returns a plain `BigDecimal` whose value is `-this`.

The same as `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#negate(android.icu.math.MathContext)`, where the context is `new MathContext(0, MathContext.PLAIN)` .

The length of the decimal part (the scale) of the result will be be `this.scale()`

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#!` | A `BigDecimal` whose value is `-this`. |

### negate

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun negate(set: MathContext!): BigDecimal!
```

Returns a `BigDecimal` whose value is `-this`.

Implements the negation (Prefix **`-`** ) operator (as defined in the decimal documentation, see `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#`), and returns the result as a `BigDecimal` object.

| Parameters ||
|---|---|
| `set` | [MathContext](MathContext.md)!: The `MathContext` arithmetic settings. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#!` | A `BigDecimal` whose value is `-this`. |

### plus

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun plus(): BigDecimal!
```

Returns a plain `BigDecimal` whose value is `+this`. Note that `this` is not necessarily a plain `BigDecimal`, but the result will always be.

The same as `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#plus(android.icu.math.MathContext)`, where the context is `new MathContext(0, MathContext.PLAIN)`.

The length of the decimal part (the scale) of the result will be be `this.scale()`

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#!` | A `BigDecimal` whose value is `+this`. |

### plus

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun plus(set: MathContext!): BigDecimal!
```

Returns a `BigDecimal` whose value is `+this`.

Implements the plus (Prefix **`+`** ) operator (as defined in the decimal documentation, see `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#`), and returns the result as a `BigDecimal` object.

This method is useful for rounding or otherwise applying a context to a decimal value.

| Parameters ||
|---|---|
| `set` | [MathContext](MathContext.md)!: The `MathContext` arithmetic settings. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#!` | A `BigDecimal` whose value is `+this`. |

### pow

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun pow(rhs: BigDecimal!): BigDecimal!
```

Returns a plain `BigDecimal` whose value is `this**rhs`, using fixed point arithmetic.

The same as `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#pow(android.icu.math.BigDecimal,%20android.icu.math.MathContext)`, where the `BigDecimal` is `rhs`, and the context is `new MathContext(0, MathContext.PLAIN)`.

The parameter is the power to which the `this` will be raised; it must be in the range 0 through 999999999, and must have a decimal part of zero. Note that these restrictions may be removed in the future, so they should not be used as a test for a whole number.

In addition, the power must not be negative, as no `MathContext` is used and so the result would then always be 0.

| Parameters ||
|---|---|
| `rhs` | [BigDecimal](BigDecimal.md)!: The `BigDecimal` for the right hand side of the operation (the power). |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#!` | A `BigDecimal` whose value is `this**rhs`, using fixed point arithmetic. |

| Exceptions ||
|---|---|
| `java.lang.ArithmeticException` | if `rhs` is out of range or is not a whole number. |

### pow

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun pow(
    rhs: BigDecimal!, 
    set: MathContext!
): BigDecimal!
```

Returns a `BigDecimal` whose value is `this**rhs`.

Implements the power (**`^`** ) operator (as defined in the decimal documentation, see `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#`), and returns the result as a `BigDecimal` object.

The first parameter is the power to which the `this` will be raised; it must be in the range -999999999 through 999999999, and must have a decimal part of zero. Note that these restrictions may be removed in the future, so they should not be used as a test for a whole number.

If the `digits` setting of the `MathContext` parameter is 0, the power must be zero or positive.

| Parameters ||
|---|---|
| `rhs` | [BigDecimal](BigDecimal.md)!: The `BigDecimal` for the right hand side of the operation (the power). |
| `set` | [MathContext](MathContext.md)!: The `MathContext` arithmetic settings. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#!` | A `BigDecimal` whose value is `this**rhs`. |

| Exceptions ||
|---|---|
| `java.lang.ArithmeticException` | if `rhs` is out of range or is not a whole number. |

### remainder

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun remainder(rhs: BigDecimal!): BigDecimal!
```

Returns a plain `BigDecimal` whose value is the remainder of `this/rhs`, using fixed point arithmetic.

The same as `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#remainder(android.icu.math.BigDecimal,%20android.icu.math.MathContext)`, where the `BigDecimal` is `rhs`, and the context is `new MathContext(0, MathContext.PLAIN)`.

This is not the modulo operator -- the result may be negative.

| Parameters ||
|---|---|
| `rhs` | [BigDecimal](BigDecimal.md)!: The `BigDecimal` for the right hand side of the remainder operation. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#!` | A `BigDecimal` whose value is the remainder of `this/rhs`, using fixed point arithmetic. |

| Exceptions ||
|---|---|
| `java.lang.ArithmeticException` | if `rhs` is zero. |

### remainder

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun remainder(
    rhs: BigDecimal!, 
    set: MathContext!
): BigDecimal!
```

Returns a `BigDecimal` whose value is the remainder of `this/rhs`.

Implements the remainder operator (as defined in the decimal documentation, see `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#`), and returns the result as a `BigDecimal` object.

This is not the modulo operator -- the result may be negative.

| Parameters ||
|---|---|
| `rhs` | [BigDecimal](BigDecimal.md)!: The `BigDecimal` for the right hand side of the remainder operation. |
| `set` | [MathContext](MathContext.md)!: The `MathContext` arithmetic settings. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#!` | A `BigDecimal` whose value is the remainder of `this+rhs`. |

| Exceptions ||
|---|---|
| `java.lang.ArithmeticException` | if the integer part of the result will not fit in the number of digits specified for the context. |

### scale

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun scale(): Int
```

Returns the scale of this `BigDecimal`. Returns a non-negative `int` which is the scale of the number. The scale is the number of digits in the decimal part of the number if the number were formatted without exponential notation.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | An `int` whose value is the scale of this `BigDecimal`. |

### setScale

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setScale(scale: Int): BigDecimal!
```

Returns a plain `BigDecimal` with a given scale.

If the given scale (which must be zero or positive) is the same as or greater than the length of the decimal part (the scale) of this `BigDecimal` then trailing zeros will be added to the decimal part as necessary.

If the given scale is less than the length of the decimal part (the scale) of this `BigDecimal` then trailing digits will be removed, and in this case an `ArithmeticException` is thrown if any discarded digits are non-zero.

The same as `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#setScale(kotlin.Int,%20kotlin.Int)`, where the first parameter is the scale, and the second is ` MathContext.ROUND_UNNECESSARY`.

| Parameters ||
|---|---|
| `scale` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The `int` specifying the scale of the resulting `BigDecimal`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#!` | A plain `BigDecimal` with the given scale. |

| Exceptions ||
|---|---|
| `java.lang.ArithmeticException` | if reducing scale would discard non-zero digits. |

### setScale

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setScale(
    scale: Int, 
    round: Int
): BigDecimal!
```

Returns a plain `BigDecimal` with a given scale.

If the given scale (which must be zero or positive) is the same as or greater than the length of the decimal part (the scale) of this `BigDecimal` then trailing zeros will be added to the decimal part as necessary.

If the given scale is less than the length of the decimal part (the scale) of this `BigDecimal` then trailing digits will be removed, and the rounding mode given by the second parameter is used to determine if the remaining digits are affected by a carry. In this case, an `IllegalArgumentException` is thrown if `round` is not a valid rounding mode.

If `round` is `MathContext.ROUND_UNNECESSARY`, an `ArithmeticException` is thrown if any discarded digits are non-zero.

| Parameters ||
|---|---|
| `scale` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The `int` specifying the scale of the resulting `BigDecimal`. |
| `round` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The `int` rounding mode to be used for the division (see the `https://developer.android.com/reference/kotlin/android/icu/math/MathContext` class). |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#!` | A plain `BigDecimal` with the given scale. |

| Exceptions ||
|---|---|
| `java.lang.ArithmeticException` | if `round` is `MathContext.ROUND_UNNECESSARY`, and reducing scale would discard non-zero digits. |
| `java.lang.IllegalArgumentException` | if `round` is not a valid rounding mode. |

### shortValueExact

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun shortValueExact(): Short
```

Converts this `BigDecimal` to a `short`. If the `BigDecimal` has a non-zero decimal part or is out of the possible range for a `short` (16-bit signed integer) result then an `ArithmeticException` is thrown.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html` | A `short` equal in value to `this`. |

| Exceptions ||
|---|---|
| `java.lang.ArithmeticException` | if `this` has a non-zero decimal part, or will not fit in a `short`. |

### signum

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun signum(): Int
```

Returns the sign of this `BigDecimal`, as an `int`. This returns the *signum* function value that represents the sign of this `BigDecimal`. That is, -1 if the `BigDecimal` is negative, 0 if it is numerically equal to zero, or 1 if it is positive.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | An `int` which is -1 if the `BigDecimal` is negative, 0 if it is numerically equal to zero, or 1 if it is positive. |

### subtract

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun subtract(rhs: BigDecimal!): BigDecimal!
```

Returns a plain `BigDecimal` whose value is `this-rhs`, using fixed point arithmetic.

The same as `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#subtract(android.icu.math.BigDecimal,%20android.icu.math.MathContext)`, where the `BigDecimal` is `rhs`, and the context is `new MathContext(0, MathContext.PLAIN)`.

The length of the decimal part (the scale) of the result will be the maximum of the scales of the two operands.

| Parameters ||
|---|---|
| `rhs` | [BigDecimal](BigDecimal.md)!: The `BigDecimal` for the right hand side of the subtraction. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#!` | A `BigDecimal` whose value is `this-rhs`, using fixed point arithmetic. |

### subtract

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun subtract(
    rhs: BigDecimal!, 
    set: MathContext!
): BigDecimal!
```

Returns a `BigDecimal` whose value is `this-rhs`.

Implements the subtraction (**`-`** ) operator (as defined in the decimal documentation, see `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#`), and returns the result as a `BigDecimal` object.

| Parameters ||
|---|---|
| `rhs` | [BigDecimal](BigDecimal.md)!: The `BigDecimal` for the right hand side of the subtraction. |
| `set` | [MathContext](MathContext.md)!: The `MathContext` arithmetic settings. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#!` | A `BigDecimal` whose value is `this-rhs`. |

### toBigDecimal

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun toBigDecimal(): BigDecimal!
```

Converts this `BigDecimal` to a `java.math.BigDecimal`.

This is an exact conversion; the result is the same as if the `BigDecimal` were formatted as a plain number without any rounding or exponent and then the `java.math.BigDecimal(java.lang.String)` constructor were used to construct the result.

*(Note: this method is provided only in the `android.icu.math` version of the BigDecimal class. It would not be present in a `java.math` version.)*

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/math/BigDecimal.html#!` | The `java.math.BigDecimal` equal in value to this `BigDecimal`. |

### toBigInteger

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun toBigInteger(): BigInteger!
```

Converts this `BigDecimal` to a `java.math.BigInteger`.

Any decimal part is truncated (discarded). If an exception is desired should the decimal part be non-zero, use `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#toBigIntegerExact()`.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/math/BigInteger.html#!` | The `java.math.BigInteger` equal in value to the integer part of this `BigDecimal`. |

### toBigIntegerExact

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun toBigIntegerExact(): BigInteger!
```

Converts this `BigDecimal` to a `java.math.BigInteger`.

An exception is thrown if the decimal part (if any) is non-zero.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/math/BigInteger.html#!` | The `java.math.BigInteger` equal in value to the integer part of this `BigDecimal`. |

| Exceptions ||
|---|---|
| `java.lang.ArithmeticException` | if `this` has a non-zero decimal part. |

### toCharArray

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun toCharArray(): CharArray!
```

Returns the `BigDecimal` as a character array. The result of this method is the same as using the sequence `toString().toCharArray()`, but avoids creating the intermediate `String` and `char[]` objects.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html!` | The `char[]` array corresponding to this `BigDecimal`. |

### toDouble

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun toDouble(): Double
```

Converts this `BigDecimal` to a `double`. If the `BigDecimal` is out of the possible range for a `double` (64-bit signed floating point) result then an `ArithmeticException ` is thrown.

The double produced is identical to result of expressing the `BigDecimal` as a `String` and then converting it using the `Double(String)` constructor; this can result in values of ` Double.NEGATIVE_INFINITY` or `Double.POSITIVE_INFINITY`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html` | A `double` corresponding to `this`. |

### toFloat

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun toFloat(): Float
```

Converts this `BigDecimal` to a `float`. If the `BigDecimal` is out of the possible range for a `float` (32-bit signed floating point) result then an `ArithmeticException ` is thrown.

The float produced is identical to result of expressing the `BigDecimal` as a `String` and then converting it using the `Float(String)` constructor; this can result in values of ` Float.NEGATIVE_INFINITY` or `Float.POSITIVE_INFINITY`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | A `float` corresponding to `this`. |

### toInt

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun toInt(): Int
```

Converts this `BigDecimal` to an `int`. If the `BigDecimal` has a non-zero decimal part it is discarded. If the `BigDecimal` is out of the possible range for an `int` (32-bit signed integer) result then only the low-order 32 bits are used. (That is, the number may be *decapitated* .) To avoid unexpected errors when these conditions occur, use the `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#intValueExact()` method.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | An `int` converted from `this`, truncated and decapitated if necessary. |

### toLong

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun toLong(): Long
```

Converts this `BigDecimal` to a `long`. If the `BigDecimal` has a non-zero decimal part it is discarded. If the `BigDecimal` is out of the possible range for a `long` (64-bit signed integer) result then only the low-order 64 bits are used. (That is, the number may be *decapitated* .) To avoid unexpected errors when these conditions occur, use the `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#longValueExact()` method.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | A `long` converted from `this`, truncated and decapitated if necessary. |

### toString

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun toString(): String
```

Returns the `BigDecimal` as a `String`. This returns a `String` that exactly represents this `BigDecimal`, as defined in the decimal documentation (see `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#`).

By definition, using the `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#BigDecimal(kotlin.String)` constructor on the result `String` will create a `BigDecimal` that is exactly equal to the original `BigDecimal`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | The `String` exactly corresponding to this `BigDecimal`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#format(kotlin.Int,%20kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#format(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#toCharArray()`

### unscaledValue

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun unscaledValue(): BigInteger!
```

Returns the number as a `BigInteger` after removing the scale. That is, the number is expressed as a plain number, any decimal point is then removed (retaining the digits of any decimal part), and the result is then converted to a `BigInteger`.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/math/BigInteger.html#!` | The `java.math.BigInteger` equal in value to this `BigDecimal` multiplied by ten to the power of `this.scale()`. |

### valueOf

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun valueOf(dub: Double): BigDecimal!
```

Translates a `double` to a `BigDecimal`.

Returns a `BigDecimal` which is the decimal representation of the 64-bit signed binary floating point parameter. If the parameter is infinite, or is not a number (NaN), a `NumberFormatException` is thrown.

The number is constructed as though `num` had been converted to a `String` using the ` Double.toString()` method and the `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#BigDecimal(kotlin.String)` constructor had then been used. This is typically not an exact conversion.

| Parameters ||
|---|---|
| `dub` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html): The `double` to be translated. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#!` | The `BigDecimal` equal in value to `dub`. |

| Exceptions ||
|---|---|
| `java.lang.NumberFormatException` | if the parameter is infinite or not a number. |

### valueOf

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun valueOf(lint: Long): BigDecimal!
```

Translates a `long` to a `BigDecimal`. That is, returns a plain `BigDecimal` whose value is equal to the given `long`.

| Parameters ||
|---|---|
| `lint` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): The `long` to be translated. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#!` | The `BigDecimal` equal in value to `lint`. |

### valueOf

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun valueOf(
    lint: Long, 
    scale: Int
): BigDecimal!
```

Translates a `long` to a `BigDecimal` with a given scale. That is, returns a plain ` BigDecimal` whose unscaled value is equal to the given `long`, adjusted by the second parameter, `scale`.

The result is given by:

` (new BigDecimal(lint)).divide(TEN.pow(new BigDecimal(scale))) `

A `NumberFormatException` is thrown if `scale` is negative.

| Parameters ||
|---|---|
| `lint` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): The `long` to be translated. |
| `scale` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The `int` scale to be applied. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#!` | The `BigDecimal` equal in value to `lint`. |

| Exceptions ||
|---|---|
| `java.lang.NumberFormatException` | if the scale is negative. |

## Properties

### ONE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ONE: BigDecimal!
```

The `BigDecimal` constant "1".
**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#TEN:android.icu.math.BigDecimal`
- `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#ZERO:android.icu.math.BigDecimal`

### TEN

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TEN: BigDecimal!
```

The `BigDecimal` constant "10".
**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#ONE:android.icu.math.BigDecimal`
- `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#ZERO:android.icu.math.BigDecimal`

### ZERO

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ZERO: BigDecimal!
```

The `BigDecimal` constant "0".
**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#ONE:android.icu.math.BigDecimal`
- `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal#TEN:android.icu.math.BigDecimal`
