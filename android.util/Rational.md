Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Rational

Kotlin | [Java](../android/util/Rational.md)
| --- | --- |

```
class Rational : Number, Comparable<Rational!>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [kotlin.Number](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-number/index.html) ||
| | ↳ | [android.util.Rational](../android/util/Rational.md) |

An immutable data type representation a rational number.

Contains a pair of `int`s representing the numerator and denominator of a Rational number.

## Summary

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/util/Rational#Rational(kotlin.Int,%20kotlin.Int)(numerator: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, denominator: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Create a `Rational` with a given numerator and denominator. |

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/util/Rational#compareTo(android.util.Rational)(other: https://developer.android.com/reference/kotlin/android/util/Rational#!)` Compare this rational to the specified rational to determine their natural order. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/util/Rational#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Compare this Rational to another object and see if they are equal. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/util/Rational#getDenominator()()` Gets the denominator of the rational |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/util/Rational#getNumerator()()` Gets the numerator of the rational. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/util/Rational#hashCode()()` Returns a hash code value for the object. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/util/Rational#isFinite()()` Indicates whether this rational represents a finite value. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/util/Rational#isInfinite()()` Indicates whether this rational represents an infinite value. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/util/Rational#isNaN()()` Indicates whether this rational is a *Not-a-Number (NaN)* value. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/util/Rational#isZero()()` Indicates whether this rational represents a zero value. |
| --- | --- |
| static [Rational](../android/util/Rational.md)! | `https://developer.android.com/reference/kotlin/android/util/Rational#parseRational(kotlin.String)(string: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Parses the specified string as a rational value. |
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | `https://developer.android.com/reference/kotlin/android/util/Rational#toDouble()()` Returns the value of the specified number as a `double`. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/android/util/Rational#toFloat()()` Returns the value of the specified number as a `float`. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/util/Rational#toInt()()` Returns the value of the specified number as a `int`. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/util/Rational#toLong()()` Returns the value of the specified number as a `long`. |
| [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | `https://developer.android.com/reference/kotlin/android/util/Rational#toShort()()` Returns the value of the specified number as a `short`. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/util/Rational#toString()()` Return a string representation of this rational, e. |

| Properties ||
|---|---|
| static [Rational](../android/util/Rational.md)! | `https://developer.android.com/reference/kotlin/android/util/Rational#NEGATIVE_INFINITY:android.util.Rational` Constant for the negative infinity value of the `Rational` type. |
| static [Rational](../android/util/Rational.md)! | `https://developer.android.com/reference/kotlin/android/util/Rational#NaN:android.util.Rational` Constant for the *Not-a-Number (NaN)* value of the `Rational` type. |
| static [Rational](../android/util/Rational.md)! | `https://developer.android.com/reference/kotlin/android/util/Rational#POSITIVE_INFINITY:android.util.Rational` Constant for the positive infinity value of the `Rational` type. |
| --- | --- |
| static [Rational](../android/util/Rational.md)! | `https://developer.android.com/reference/kotlin/android/util/Rational#ZERO:android.util.Rational` Constant for the zero value of the `Rational` type. |

## Public constructors

### Rational

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
Rational(
    numerator: Int, 
    denominator: Int)
```

Create a `Rational` with a given numerator and denominator.

The signs of the numerator and the denominator may be flipped such that the denominator is always positive. Both the numerator and denominator will be converted to their reduced forms (see `https://developer.android.com/reference/kotlin/android/util/Rational#equals(kotlin.Any)` for more details).

For example,

- a rational of `2/4` will be reduced to `1/2`.
- a rational of `1/-1` will be flipped to `-1/1`
- a rational of `5/0` will be reduced to `1/0`
- a rational of `0/5` will be reduced to `0/1`

<br />

| Parameters ||
|---|---|
| `numerator` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the numerator of the rational |
| `denominator` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the denominator of the rational |

**See Also**

- `https://developer.android.com/reference/kotlin/android/util/Rational#equals(kotlin.Any)`

## Public methods

### compareTo

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun compareTo(other: Rational!): Int
```

Compare this rational to the specified rational to determine their natural order.

`https://developer.android.com/reference/kotlin/android/util/Rational#NaN:android.util.Rational` is considered to be equal to itself and greater than all other `Rational` values. Otherwise, if the objects are not `https://developer.android.com/reference/kotlin/android/util/Rational#equals(kotlin.Any)`, then the following rules apply:

- Positive infinity is greater than any other finite number (or negative infinity)
- Negative infinity is less than any other finite number (or positive infinity)
- The finite number represented by this rational is checked numerically against the other finite number by converting both rationals to a common denominator multiple and comparing their numerators.

| Parameters ||
|---|---|
| `o` | the object to be compared. |
| `another` | the rational to be compared |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a negative integer, zero, or a positive integer as this object is less than, equal to, or greater than the specified rational. |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the specified object's type prevents it from being compared to this object. |
| `java.lang.NullPointerException` | if `another` was `null` |

### equals

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun equals(other: Any?): Boolean
```

Compare this Rational to another object and see if they are equal.

A Rational object can only be equal to another Rational object (comparing against any other type will return `false`).

A Rational object is considered equal to another Rational object if and only if one of the following holds:

- Both are `NaN`
- Both are infinities of the same sign
- Both have the same numerator and denominator in their reduced form

A reduced form of a Rational is calculated by dividing both the numerator and the denominator by their greatest common divisor.

```kotlin
<code>(new Rational(1, 2)).equals(new Rational(1, 2)) == true   // trivially true
  (new Rational(2, 3)).equals(new Rational(1, 2)) == false  // trivially false
  (new Rational(1, 2)).equals(new Rational(2, 4)) == true   // true after reduction
  (new Rational(0, 0)).equals(new Rational(0, 0)) == true   // NaN.equals(NaN)
  (new Rational(1, 0)).equals(new Rational(5, 0)) == true   // both are +infinity
  (new Rational(1, 0)).equals(new Rational(-1, 0)) == false // +infinity != -infinity
  </code>
```

| Parameters ||
|---|---|
| `obj` | a reference to another object. This value may be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | A boolean that determines whether or not the two Rational objects are equal. |

### getDenominator

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getDenominator(): Int
```

Gets the denominator of the rational

The denominator may return `0`, in which case the rational may represent positive infinity (if the numerator was positive), negative infinity (if the numerator was negative), or `NaN` (if the numerator was `0`).

The denominator will always return `1` if the numerator is `0`.

### getNumerator

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getNumerator(): Int
```

Gets the numerator of the rational.

The numerator will always return `1` if this rational represents infinity (that is, the denominator is `0`).

### hashCode

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hashCode(): Int
```

Returns a hash code value for the object. This method is supported for the benefit of hash tables such as those provided by `https://developer.android.com/reference/kotlin/java/util/HashMap.html#`.

The general contract of `hashCode` is:

- Whenever it is invoked on the same object more than once during an execution of a Java application, the `hashCode` method must consistently return the same integer, provided no information used in `equals` comparisons on the object is modified. This integer need not remain consistent from one execution of an application to another execution of the same application.
- If two objects are equal according to the `https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any)` method, then calling the `hashCode` method on each of the two objects must produce the same integer result.
- It is *not* required that if two objects are unequal according to the `https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any)` method, then calling the `hashCode` method on each of the two objects must produce distinct integer results. However, the programmer should be aware that producing distinct integer results for unequal objects may improve the performance of hash tables.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a hash code value for this object. |

### isFinite

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isFinite(): Boolean
```

Indicates whether this rational represents a finite value.

A finite value occurs when the denominator is not `0`; in other words the rational is neither infinity or `NaN`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this rational is a (positive or negative) infinite value; `false` if this is a finite number value (or `NaN`) |

### isInfinite

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isInfinite(): Boolean
```

Indicates whether this rational represents an infinite value.

An infinite value occurs when the denominator is `0` (but the numerator is not).

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this rational is a (positive or negative) infinite value; `false` if this is a finite number value (or `NaN`) |

### isNaN

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isNaN(): Boolean
```

Indicates whether this rational is a *Not-a-Number (NaN)* value.

A `NaN` value occurs when both the numerator and the denominator are `0`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this rational is a *Not-a-Number (NaN)* value; `false` if this is a (potentially infinite) number value |

### isZero

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isZero(): Boolean
```

Indicates whether this rational represents a zero value.

A zero value is a `https://developer.android.com/reference/kotlin/android/util/Rational#isFinite()` rational with a numerator of `0`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this rational is finite zero value; `false` otherwise |

### parseRational

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun parseRational(string: String!): Rational!
```

Parses the specified string as a rational value.

The ASCII characters `\``u003a` (':') and `\``u002f` ('/') are recognized as separators between the numerator and denumerator.

For any `Rational r`: `Rational.parseRational(r.toString()).equals(r)`. However, the method also handles rational numbers expressed in the following forms:

"*num* `/`*den* " or "*num* `:`*den* " `=> new Rational(num, den);`, where *num* and *den* are string integers potentially containing a sign, such as "-10", "+7" or "5".

```kotlin
<code>Rational.parseRational("3:+6").equals(new Rational(1, 2)) == true
  Rational.parseRational("-3/-6").equals(new Rational(1, 2)) == true
  Rational.parseRational("4.56") =&gt; throws NumberFormatException
  </code>
```

| Parameters ||
|---|---|
| `string` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the string representation of a rational value. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/util/Rational#!` | the rational value represented by `string`. |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if `string` was `null` |
| `java.lang.NumberFormatException` | if `string` cannot be parsed as a rational value. |

### toDouble

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toDouble(): Double
```

Returns the value of the specified number as a `double`.

The `double` is calculated by converting both the numerator and denominator to a `double`; then returning the result of dividing the numerator by the denominator.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html` | the divided value of the numerator and denominator as a `double`. |

### toFloat

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toFloat(): Float
```

Returns the value of the specified number as a `float`.

The `float` is calculated by converting both the numerator and denominator to a `float`; then returning the result of dividing the numerator by the denominator.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | the divided value of the numerator and denominator as a `float`. |

### toInt

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toInt(): Int
```

Returns the value of the specified number as a `int`.

`https://developer.android.com/reference/kotlin/android/util/Rational#isInfinite()` rationals are converted to an `int` value by dividing the numerator by the denominator; conversion for non-finite values happens identically to casting a floating point value to an `int`, in particular:

- Positive infinity saturates to the largest maximum integer `https://developer.android.com/reference/kotlin/java/lang/Integer.html#MAX_VALUE:kotlin.Int`
- Negative infinity saturates to the smallest maximum integer `https://developer.android.com/reference/kotlin/java/lang/Integer.html#MIN_VALUE:kotlin.Int`
- *Not-A-Number (NaN)* returns `0`.

<br />

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the divided value of the numerator and denominator as a `int`. |

### toLong

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toLong(): Long
```

Returns the value of the specified number as a `long`.

`https://developer.android.com/reference/kotlin/android/util/Rational#isInfinite()` rationals are converted to an `long` value by dividing the numerator by the denominator; conversion for non-finite values happens identically to casting a floating point value to a `long`, in particular:

- Positive infinity saturates to the largest maximum long `https://developer.android.com/reference/kotlin/java/lang/Long.html#MAX_VALUE:kotlin.Long`
- Negative infinity saturates to the smallest maximum long `https://developer.android.com/reference/kotlin/java/lang/Long.html#MIN_VALUE:kotlin.Long`
- *Not-A-Number (NaN)* returns `0`.

<br />

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the divided value of the numerator and denominator as a `long`. |

### toShort

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toShort(): Short
```

Returns the value of the specified number as a `short`.

`https://developer.android.com/reference/kotlin/android/util/Rational#isInfinite()` rationals are converted to a `short` value identically to `https://developer.android.com/reference/kotlin/android/util/Rational#toInt()`; the `int` result is then truncated to a `short` before returning the value.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html` | the divided value of the numerator and denominator as a `short`. |

### toString

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toString(): String
```

Return a string representation of this rational, e.g. `"1/2"`.

The following rules of conversion apply:

- `NaN` values will return `"NaN"`
- Positive infinity values will return `"Infinity"`
- Negative infinity values will return `"-Infinity"`
- All other values will return `"numerator/denominator"` where `numerator` and `denominator` are substituted with the appropriate numerator and denominator values.

<br />

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the object. |

## Properties

### NEGATIVE_INFINITY

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NEGATIVE_INFINITY: Rational!
```

Constant for the negative infinity value of the `Rational` type.

Equivalent to constructing a new rational with a negative numerator and a denominator equal to `0`.

### NaN

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NaN: Rational!
```

Constant for the *Not-a-Number (NaN)* value of the `Rational` type.

A `NaN` value is considered to be equal to itself (that is `NaN.equals(NaN)` will return `true`; it is always greater than any non-`NaN` value (that is `NaN.compareTo(notNaN)` will return a number greater than `0`).

Equivalent to constructing a new rational with both the numerator and denominator equal to `0`.

### POSITIVE_INFINITY

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val POSITIVE_INFINITY: Rational!
```

Constant for the positive infinity value of the `Rational` type.

Equivalent to constructing a new rational with a positive numerator and a denominator equal to `0`.

### ZERO

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ZERO: Rational!
```

Constant for the zero value of the `Rational` type.

Equivalent to constructing a new rational with a numerator equal to `0` and any non-zero denominator.
