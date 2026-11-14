# Double

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Double

```
class Double : Number, Comparable<Double!>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| ↳ | [kotlin.Number](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-number/index.html) ||
| | ↳ | [java.lang.Double](https://developer.android.com/reference/kotlin/java/lang/Double#) |

The`Double`class wraps a value of the primitive type`double`in an object. An object of type`Double`contains a single field whose type is`double`.

In addition, this class provides several methods for converting a`double`to a`String`and a`String`to a`double`, as well as other constants and methods useful when dealing with a`double`.

## Floating-point Equality, Equivalence, and Comparison

IEEE 754 floating-point values include finite nonzero values, signed zeros (`+0.0`and`-0.0`), signed infinities [positive infinity](https://developer.android.com/reference/kotlin/java/lang/Double#POSITIVE_INFINITY:kotlin.Double) and [negative infinity](https://developer.android.com/reference/kotlin/java/lang/Double#NEGATIVE_INFINITY:kotlin.Double)), and [NaN](https://developer.android.com/reference/kotlin/java/lang/Double#NaN:kotlin.Double)(not-a-number).

An*equivalence relation* on a set of values is a boolean relation on pairs of values that is reflexive, symmetric, and transitive. For more discussion of equivalence relations and object equality, see the [Object.equals](https://developer.android.com/reference/kotlin/java/lang/Object#equals(kotlin.Any))specification. An equivalence relation partitions the values it operates over into sets called*equivalence classes* . All the members of the equivalence class are equal to each other under the relation. An equivalence class may contain only a single member. At least for some purposes, all the members of an equivalence class are substitutable for each other. In particular, in a numeric expression equivalent values can be*substituted*for one another without changing the result of the expression, meaning changing the equivalence class of the result of the expression.

Notably, the built-in`==`operation on floating-point values is*not* an equivalence relation. Despite not defining an equivalence relation, the semantics of the IEEE 754`==`operator were deliberately designed to meet other needs of numerical computation. There are two exceptions where the properties of an equivalence relation are not satisfied by`==`on floating-point values:

- If`v1`and`v2`are both NaN, then`v1 == v2`has the value`false`. Therefore, for two NaN arguments the*reflexive* property of an equivalence relation is*not* satisfied by the`==`operator.
- If`v1`represents`+0.0`while`v2`represents`-0.0`, or vice versa, then`v1 == v2`has the value`true`even though`+0.0`and`-0.0`are distinguishable under various floating-point operations. For example,`1.0/+0.0`evaluates to positive infinity while`1.0/-0.0`evaluates to*negative* infinity and positive infinity and negative infinity are neither equal to each other nor equivalent to each other. Thus, while a signed zero input most commonly determines the sign of a zero result, because of dividing by zero,`+0.0`and`-0.0`may not be substituted for each other in general. The sign of a zero input also has a non-substitutable effect on the result of some math library methods.

For ordered comparisons using the built-in comparison operators (`<`,`<=`, etc.), NaN values have another anomalous situation: a NaN is neither less than, nor greater than, nor equal to any value, including itself. This means the*trichotomy of comparison* does*not*hold.

To provide the appropriate semantics for`equals`and`compareTo`methods, those methods cannot simply be wrappers around`==`or ordered comparison operations. Instead, [equals](https://developer.android.com/reference/kotlin/java/lang/Double#equals(kotlin.Any))defines NaN arguments to be equal to each other and defines`+0.0`to*not* be equal to`-0.0`, restoring reflexivity. For comparisons, [compareTo](https://developer.android.com/reference/kotlin/java/lang/Double#compareTo(kotlin.Double))defines a total order where`-0.0`is less than`+0.0`and where a NaN is equal to itself and considered greater than positive infinity.

The operational semantics of`equals`and`compareTo`are expressed in terms of [bit-wise converting](https://developer.android.com/reference/kotlin/java/lang/Double#doubleToLongBits(kotlin.Double))the floating-point values to integral values.

The*natural ordering* implemented by [compareTo](https://developer.android.com/reference/kotlin/java/lang/Double#compareTo(kotlin.Double))is [consistent with equals](https://developer.android.com/reference/kotlin/java/lang/Comparable). That is, two objects are reported as equal by`equals`if and only if`compareTo`on those objects returns zero.

The adjusted behaviors defined for`equals`and`compareTo`allow instances of wrapper classes to work properly with conventional data structures. For example, defining NaN values to be`equals`to one another allows NaN to be used as an element of a [HashSet](https://developer.android.com/reference/kotlin/java/util/HashSet.html#) or as the key of a [HashMap](https://developer.android.com/reference/kotlin/java/util/HashMap.html#). Similarly, defining`compareTo`as a total ordering, including`+0.0`,`-0.0`, and NaN, allows instances of wrapper classes to be used as elements of a [SortedSet](https://developer.android.com/reference/kotlin/java/util/SortedSet.html#) or as keys of a [SortedMap](https://developer.android.com/reference/kotlin/java/util/SortedMap.html#).

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BYTES](https://developer.android.com/reference/kotlin/java/lang/Double#BYTES:kotlin.Int) The number of bytes used to represent a`double`value. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MAX_EXPONENT](https://developer.android.com/reference/kotlin/java/lang/Double#MAX_EXPONENT:kotlin.Int) Maximum exponent a finite`double`variable may have. |
| static [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [MAX_VALUE](https://developer.android.com/reference/kotlin/java/lang/Double#MAX_VALUE:kotlin.Double) A constant holding the largest positive finite value of type`double`, (2-2-52)·21023. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MIN_EXPONENT](https://developer.android.com/reference/kotlin/java/lang/Double#MIN_EXPONENT:kotlin.Int) Minimum exponent a normalized`double`variable may have. |
| static [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [MIN_NORMAL](https://developer.android.com/reference/kotlin/java/lang/Double#MIN_NORMAL:kotlin.Double) A constant holding the smallest positive normal value of type`double`, 2-1022. |
| static [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [MIN_VALUE](https://developer.android.com/reference/kotlin/java/lang/Double#MIN_VALUE:kotlin.Double) A constant holding the smallest positive nonzero value of type`double`, 2-1074. |
| static [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [NEGATIVE_INFINITY](https://developer.android.com/reference/kotlin/java/lang/Double#NEGATIVE_INFINITY:kotlin.Double) A constant holding the negative infinity of type`double`. |
| static [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [NaN](https://developer.android.com/reference/kotlin/java/lang/Double#NaN:kotlin.Double) A constant holding a Not-a-Number (NaN) value of type`double`. |
| static [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [POSITIVE_INFINITY](https://developer.android.com/reference/kotlin/java/lang/Double#POSITIVE_INFINITY:kotlin.Double) A constant holding the positive infinity of type`double`. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PRECISION](https://developer.android.com/reference/kotlin/java/lang/Double#PRECISION:kotlin.Int) The number of bits in the significand of a`double`value. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SIZE](https://developer.android.com/reference/kotlin/java/lang/Double#SIZE:kotlin.Int) The number of bits used to represent a`double`value. |

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [Double](https://developer.android.com/reference/kotlin/java/lang/Double#Double(kotlin.Double))`(`value:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`)` Constructs a newly allocated`Double`object that represents the primitive`double`argument. |
| [Double](https://developer.android.com/reference/kotlin/java/lang/Double#Double(kotlin.String))`(`s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Constructs a newly allocated`Double`object that represents the floating-point value of type`double`represented by the string. |

| Public methods ||
|------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [compare](https://developer.android.com/reference/kotlin/java/lang/Double#compare(kotlin.Double,%20kotlin.Double))`(`d1:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`, `d2:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`)` Compares the two specified`double`values. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [compareTo](https://developer.android.com/reference/kotlin/java/lang/Double#compareTo(kotlin.Double))`(`other:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`)` Compares two`Double`objects numerically. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [doubleToLongBits](https://developer.android.com/reference/kotlin/java/lang/Double#doubleToLongBits(kotlin.Double))`(`value:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`)` Returns a representation of the specified floating-point value according to the IEEE 754 floating-point "double format" bit layout. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [doubleToRawLongBits](https://developer.android.com/reference/kotlin/java/lang/Double#doubleToRawLongBits(kotlin.Double))`(`value:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`)` Returns a representation of the specified floating-point value according to the IEEE 754 floating-point "double format" bit layout, preserving Not-a-Number (NaN) values. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/java/lang/Double#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Compares this object against the specified object. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/java/lang/Double#hashCode())`()` Returns a hash code for this`Double`object. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/java/lang/Double#hashCode(kotlin.Double))`(`value:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`)` Returns a hash code for a`double`value; compatible with`Double.hashCode()`. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isFinite](https://developer.android.com/reference/kotlin/java/lang/Double#isFinite(kotlin.Double))`(`d:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`)` Returns`true`if the argument is a finite floating-point value; returns`false`otherwise (for NaN and infinity arguments). |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isInfinite](https://developer.android.com/reference/kotlin/java/lang/Double#isInfinite())`()` Returns`true`if this`Double`value is infinitely large in magnitude,`false`otherwise. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isInfinite](https://developer.android.com/reference/kotlin/java/lang/Double#isInfinite(kotlin.Double))`(`v:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`)` Returns`true`if the specified number is infinitely large in magnitude,`false`otherwise. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isNaN](https://developer.android.com/reference/kotlin/java/lang/Double#isNaN())`()` Returns`true`if this`Double`value is a Not-a-Number (NaN),`false`otherwise. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isNaN](https://developer.android.com/reference/kotlin/java/lang/Double#isNaN(kotlin.Double))`(`v:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`)` Returns`true`if the specified number is a Not-a-Number (NaN) value,`false`otherwise. |
| static [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [longBitsToDouble](https://developer.android.com/reference/kotlin/java/lang/Double#longBitsToDouble(kotlin.Long))`(`bits:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns the`double`value corresponding to a given bit representation. |
| static [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [max](https://developer.android.com/reference/kotlin/java/lang/Double#max(kotlin.Double,%20kotlin.Double))`(`a:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`, `b:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`)` Returns the greater of two`double`values as if by calling [Math.max](https://developer.android.com/reference/kotlin/java/lang/Math#max(kotlin.Double,%20kotlin.Double)). |
| static [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [min](https://developer.android.com/reference/kotlin/java/lang/Double#min(kotlin.Double,%20kotlin.Double))`(`a:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`, `b:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`)` Returns the smaller of two`double`values as if by calling [Math.min](https://developer.android.com/reference/kotlin/java/lang/Math#min(kotlin.Double,%20kotlin.Double)). |
| static [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [parseDouble](https://developer.android.com/reference/kotlin/java/lang/Double#parseDouble(kotlin.String))`(`s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Returns a new`double`initialized to the value represented by the specified`String`, as performed by the`valueOf`method of class`Double`. |
| static [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [sum](https://developer.android.com/reference/kotlin/java/lang/Double#sum(kotlin.Double,%20kotlin.Double))`(`a:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`, `b:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`)` Adds two`double`values together as per the + operator. |
| [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [toByte](https://developer.android.com/reference/kotlin/java/lang/Double#toByte())`()` Returns the value of this`Double`as a`byte`after a narrowing primitive conversion. |
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [toDouble](https://developer.android.com/reference/kotlin/java/lang/Double#toDouble())`()` Returns the`double`value of this`Double`object. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [toFloat](https://developer.android.com/reference/kotlin/java/lang/Double#toFloat())`()` Returns the value of this`Double`as a`float`after a narrowing primitive conversion. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toHexString](https://developer.android.com/reference/kotlin/java/lang/Double#toHexString(kotlin.Double))`(`d:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`)` Returns a hexadecimal string representation of the`double`argument. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [toInt](https://developer.android.com/reference/kotlin/java/lang/Double#toInt())`()` Returns the value of this`Double`as an`int`after a narrowing primitive conversion. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [toLong](https://developer.android.com/reference/kotlin/java/lang/Double#toLong())`()` Returns the value of this`Double`as a`long`after a narrowing primitive conversion. |
| [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [toShort](https://developer.android.com/reference/kotlin/java/lang/Double#toShort())`()` Returns the value of this`Double`as a`short`after a narrowing primitive conversion. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/java/lang/Double#toString())`()` Returns a string representation of this`Double`object. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/java/lang/Double#toString(kotlin.Double))`(`d:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`)` Returns a string representation of the`double`argument. |
| static [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [valueOf](https://developer.android.com/reference/kotlin/java/lang/Double#valueOf(kotlin.Double))`(`d:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`)` Returns a`Double`instance representing the specified`double`value. |
| static [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [valueOf](https://developer.android.com/reference/kotlin/java/lang/Double#valueOf(kotlin.String))`(`s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Returns a object holding the value represented by the argument string . |

| Properties ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Class](https://developer.android.com/reference/kotlin/java/lang/Class)\< [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)!\>! | [TYPE](https://developer.android.com/reference/kotlin/java/lang/Double#TYPE:java.lang.Class) The`Class`instance representing the primitive type`double`. |

## Constants

### BYTES

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BYTES: Int
```

The number of bytes used to represent a`double`value. 

 Value: 8

### MAX_EXPONENT

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MAX_EXPONENT: Int
```

Maximum exponent a finite`double`variable may have. It is equal to the value returned by`Math.getExponent(Double.MAX_VALUE)`. 

 Value: 1023

### MAX_VALUE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MAX_VALUE: Double
```

A constant holding the largest positive finite value of type`double`, (2-2-52)·21023. It is equal to the hexadecimal floating-point literal`0x1.fffffffffffffP+1023`and also equal to`Double.longBitsToDouble(0x7fefffffffffffffL)`. 

 Value: 1.7976931348623157E308

### MIN_EXPONENT

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MIN_EXPONENT: Int
```

Minimum exponent a normalized`double`variable may have. It is equal to the value returned by`Math.getExponent(Double.MIN_NORMAL)`. 

 Value: -1022

### MIN_NORMAL

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MIN_NORMAL: Double
```

A constant holding the smallest positive normal value of type`double`, 2-1022. It is equal to the hexadecimal floating-point literal`0x1.0p-1022`and also equal to`Double.longBitsToDouble(0x0010000000000000L)`. 

 Value: 2.2250738585072014E-308

### MIN_VALUE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MIN_VALUE: Double
```

A constant holding the smallest positive nonzero value of type`double`, 2-1074. It is equal to the hexadecimal floating-point literal`0x0.0000000000001P-1022`and also equal to`Double.longBitsToDouble(0x1L)`. 

 Value: 4.9E-324

### NEGATIVE_INFINITY

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NEGATIVE_INFINITY: Double
```

A constant holding the negative infinity of type`double`. It is equal to the value returned by`Double.longBitsToDouble(0xfff0000000000000L)`. 

 Value: (-1.0/0.0)

### NaN

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NaN: Double
```

A constant holding a Not-a-Number (NaN) value of type`double`. It is equivalent to the value returned by`Double.longBitsToDouble(0x7ff8000000000000L)`. 

 Value: (0.0/0.0)

### POSITIVE_INFINITY

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val POSITIVE_INFINITY: Double
```

A constant holding the positive infinity of type`double`. It is equal to the value returned by`Double.longBitsToDouble(0x7ff0000000000000L)`. 

 Value: (1.0/0.0)

### PRECISION

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PRECISION: Int
```

The number of bits in the significand of a`double`value. This is the parameter N in section {@jls 4.2.3} of The Java Language Specification. 

 Value: 53

### SIZE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SIZE: Int
```

The number of bits used to represent a`double`value. 

 Value: 64

## Public constructors

### Double

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Double(value: Double)
```

**Deprecated:** *It is rarely appropriate to use this constructor. The static factory [valueOf(double)](https://developer.android.com/reference/kotlin/java/lang/Double#valueOf(kotlin.Double))is generally a better choice, as it is likely to yield significantly better space and time performance.*

Constructs a newly allocated`Double`object that represents the primitive`double`argument.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------|
| `value` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html):the value to be represented by the`Double`. |

### Double

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Double(s: String)
```

**Deprecated:** *It is rarely appropriate to use this constructor. Use [parseDouble(java.lang.String)](https://developer.android.com/reference/kotlin/java/lang/Double#parseDouble(kotlin.String))to convert a string to a`double`primitive, or use [valueOf(java.lang.String)](https://developer.android.com/reference/kotlin/java/lang/Double#valueOf(kotlin.String))to convert a string to a`Double`object.*

Constructs a newly allocated`Double`object that represents the floating-point value of type`double`represented by the string. The string is converted to a`double`value as if by the`valueOf`method.

| Parameters ||
|-----|-------------------------------------------------------------------------------------------------------------------------|
| `s` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):a string to be converted to a`Double`. |

| Exceptions ||
|-----------------------------------|---------------------------------------------------|
| `java.lang.NumberFormatException` | if the string does not contain a parsable number. |

## Public methods

### compare

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun compare(
    d1: Double, 
    d2: Double
): Int
```

Compares the two specified`double`values. The sign of the integer value returned is the same as that of the integer that would be returned by the call: 

```kotlin
new Double(d1).compareTo(new Double(d2))
  
```

<br />

| Parameters ||
|------|---------------------------------------------------------------------------------------------------------------|
| `d1` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html):the first`double`to compare |
| `d2` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html):the second`double`to compare |

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the value`0`if`d1`is numerically equal to`d2`; a value less than`0`if`d1`is numerically less than`d2`; and a value greater than`0`if`d1`is numerically greater than`d2`. |

### compareTo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun compareTo(other: Double): Int
```

Compares two`Double`objects numerically. This method imposes a total order on`Double`objects with two differences compared to the incomplete order defined by the Java language numerical comparison operators (`<, <=, ==, >=, >`) on`double`values.

- A NaN is*unordered* with respect to other values and unequal to itself under the comparison operators. This method chooses to define`Double.NaN`to be equal to itself and greater than all other`double`values (including`Double.POSITIVE_INFINITY`).
- Positive zero and negative zero compare equal numerically, but are distinct and distinguishable values. This method chooses to define positive zero (`+0.0d`), to be greater than negative zero (`-0.0d`).

This ensures that the*natural ordering* of`Double`objects imposed by this method is*consistent with equals* ; see [this discussion](https://developer.android.com/reference/kotlin/java/lang/Double#equivalenceRelation) for details of floating-point comparison and ordering.

<br />

| Parameters ||
|-----------------|----------------------------|
| `o` | the object to be compared. |
| `anotherDouble` | the`Double`to be compared. |

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the value`0`if`anotherDouble`is numerically equal to this`Double`; a value less than`0`if this`Double`is numerically less than`anotherDouble`; and a value greater than`0`if this`Double`is numerically greater than`anotherDouble`. |

| Exceptions ||
|----------------------------------|--------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if the specified object is null |
| `java.lang.ClassCastException` | if the specified object's type prevents it from being compared to this object. |

### doubleToLongBits

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun doubleToLongBits(value: Double): Long
```

Returns a representation of the specified floating-point value according to the IEEE 754 floating-point "double format" bit layout.

Bit 63 (the bit that is selected by the mask`0x8000000000000000L`) represents the sign of the floating-point number. Bits 62-52 (the bits that are selected by the mask`0x7ff0000000000000L`) represent the exponent. Bits 51-0 (the bits that are selected by the mask`0x000fffffffffffffL`) represent the significand (sometimes called the mantissa) of the floating-point number.

If the argument is positive infinity, the result is`0x7ff0000000000000L`.

If the argument is negative infinity, the result is`0xfff0000000000000L`.

If the argument is NaN, the result is`0x7ff8000000000000L`.

In all cases, the result is a`long`integer that, when given to the [longBitsToDouble(long)](https://developer.android.com/reference/kotlin/java/lang/Double#longBitsToDouble(kotlin.Long))method, will produce a floating-point value the same as the argument to`doubleToLongBits`(except all NaN values are collapsed to a single "canonical" NaN value).

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------|
| `value` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html):a`double`precision floating-point number. |

| Return ||
|------------------------------------------------------------------------------|----------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the bits that represent the floating-point number. |

### doubleToRawLongBits

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun doubleToRawLongBits(value: Double): Long
```

Returns a representation of the specified floating-point value according to the IEEE 754 floating-point "double format" bit layout, preserving Not-a-Number (NaN) values.

Bit 63 (the bit that is selected by the mask`0x8000000000000000L`) represents the sign of the floating-point number. Bits 62-52 (the bits that are selected by the mask`0x7ff0000000000000L`) represent the exponent. Bits 51-0 (the bits that are selected by the mask`0x000fffffffffffffL`) represent the significand (sometimes called the mantissa) of the floating-point number.

If the argument is positive infinity, the result is`0x7ff0000000000000L`.

If the argument is negative infinity, the result is`0xfff0000000000000L`.

If the argument is NaN, the result is the`long`integer representing the actual NaN value. Unlike the`doubleToLongBits`method,`doubleToRawLongBits`does not collapse all the bit patterns encoding a NaN to a single "canonical" NaN value.

In all cases, the result is a`long`integer that, when given to the [longBitsToDouble(long)](https://developer.android.com/reference/kotlin/java/lang/Double#longBitsToDouble(kotlin.Long))method, will produce a floating-point value the same as the argument to`doubleToRawLongBits`.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------|
| `value` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html):a`double`precision floating-point number. |

| Return ||
|------------------------------------------------------------------------------|----------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the bits that represent the floating-point number. |

### equals

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

Compares this object against the specified object. The result is`true`if and only if the argument is not`null`and is a`Double`object that represents a`double`that has the same value as the`double`represented by this object. For this purpose, two`double`values are considered to be the same if and only if the method [doubleToLongBits(double)](https://developer.android.com/reference/kotlin/java/lang/Double#doubleToLongBits(kotlin.Double))returns the identical`long`value when applied to each.

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

**See Also**

- [java.lang.Double#doubleToLongBits(double)](https://developer.android.com/reference/kotlin/java/lang/Double#doubleToLongBits(kotlin.Double)) 

### hashCode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

Returns a hash code for this`Double`object. The result is the exclusive OR of the two halves of the`long`integer bit representation, exactly as produced by the method [doubleToLongBits(double)](https://developer.android.com/reference/kotlin/java/lang/Double#doubleToLongBits(kotlin.Double)), of the primitive`double`value represented by this`Double`object. That is, the hash code is the value of the expression:`(int)(v^(v>>>32))`where`v`is defined by:`long v = Double.doubleToLongBits(this.doubleValue());`

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a`hash code`value for this object. |

### hashCode

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun hashCode(value: Double): Int
```

Returns a hash code for a`double`value; compatible with`Double.hashCode()`.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------|
| `value` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html):the value to hash |

| Return ||
|----------------------------------------------------------------------------|---------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for a`double`value. |

### isFinite

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun isFinite(d: Double): Boolean
```

Returns`true`if the argument is a finite floating-point value; returns`false`otherwise (for NaN and infinity arguments).

| Parameters ||
|-----|----------------------------------------------------------------------------------------------------------------|
| `d` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html):the`double`value to be tested |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the argument is a finite floating-point value,`false`otherwise. |

### isInfinite

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isInfinite(): Boolean
```

Returns`true`if this`Double`value is infinitely large in magnitude,`false`otherwise.

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the value represented by this object is positive infinity or negative infinity;`false`otherwise. |

### isInfinite

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun isInfinite(v: Double): Boolean
```

Returns`true`if the specified number is infinitely large in magnitude,`false`otherwise.

| Parameters ||
|-----|----------------------------------------------------------------------------------------------------------|
| `v` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html):the value to be tested. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the value of the argument is positive infinity or negative infinity;`false`otherwise. |

### isNaN

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isNaN(): Boolean
```

Returns`true`if this`Double`value is a Not-a-Number (NaN),`false`otherwise.

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the value represented by this object is NaN;`false`otherwise. |

### isNaN

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun isNaN(v: Double): Boolean
```

Returns`true`if the specified number is a Not-a-Number (NaN) value,`false`otherwise.

| Parameters ||
|-----|----------------------------------------------------------------------------------------------------------|
| `v` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html):the value to be tested. |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the value of the argument is NaN;`false`otherwise. |

### longBitsToDouble

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun longBitsToDouble(bits: Long): Double
```

Returns the`double`value corresponding to a given bit representation. The argument is considered to be a representation of a floating-point value according to the IEEE 754 floating-point "double format" bit layout.

If the argument is`0x7ff0000000000000L`, the result is positive infinity.

If the argument is`0xfff0000000000000L`, the result is negative infinity.

If the argument is any value in the range`0x7ff0000000000001L`through`0x7fffffffffffffffL`or in the range`0xfff0000000000001L`through`0xffffffffffffffffL`, the result is a NaN. No IEEE 754 floating-point operation provided by Java can distinguish between two NaN values of the same type with different bit patterns. Distinct values of NaN are only distinguishable by use of the`Double.doubleToRawLongBits`method.

In all other cases, let*s* ,*e* , and*m*be three values that can be computed from the argument: 

```kotlin
<code>int s = ((bits &gt;&gt; 63) == 0) ? 1 : -1;
  int e = (int)((bits &gt;&gt; 52) &amp; 0x7ffL);
  long m = (e == 0) ?
                  (bits &amp; 0xfffffffffffffL) &lt;&lt; 1 :
                  (bits &amp; 0xfffffffffffffL) | 0x10000000000000L;
  </code>
```
Then the floating-point result equals the value of the mathematical expression*s* ·*m* ·2*e* -1075.

Note that this method may not be able to return a`double`NaN with exactly same bit pattern as the`long`argument. IEEE 754 distinguishes between two kinds of NaNs, quiet NaNs and*signaling NaNs* . The differences between the two kinds of NaN are generally not visible in Java. Arithmetic operations on signaling NaNs turn them into quiet NaNs with a different, but often similar, bit pattern. However, on some processors merely copying a signaling NaN also performs that conversion. In particular, copying a signaling NaN to return it to the calling method may perform this conversion. So`longBitsToDouble`may not be able to return a`double`with a signaling NaN bit pattern. Consequently, for some`long`values,`doubleToRawLongBits(longBitsToDouble(start))`may*not* equal`start`. Moreover, which particular bit patterns represent signaling NaNs is platform dependent; although all NaN bit patterns, quiet or signaling, must be in the NaN range identified above.

| Parameters ||
|--------|------------------------------------------------------------------------------------------------|
| `bits` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):any`long`integer. |

| Return ||
|----------------------------------------------------------------------------------|------------------------------------------------------------|
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | the`double`floating-point value with the same bit pattern. |

### max

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun max(
    a: Double, 
    b: Double
): Double
```

Returns the greater of two`double`values as if by calling [Math.max](https://developer.android.com/reference/kotlin/java/lang/Math#max(kotlin.Double,%20kotlin.Double)).

| Parameters ||
|-----|-----------------------------------------------------------------------------------------------------|
| `a` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html):the first operand |
| `b` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html):the second operand |

| Return ||
|----------------------------------------------------------------------------------|-------------------------|
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | the greater of`a`and`b` |

**See Also**

- [java.util.function.BinaryOperator](https://developer.android.com/reference/kotlin/java/util/function/BinaryOperator.html#) 

### min

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun min(
    a: Double, 
    b: Double
): Double
```

Returns the smaller of two`double`values as if by calling [Math.min](https://developer.android.com/reference/kotlin/java/lang/Math#min(kotlin.Double,%20kotlin.Double)).

| Parameters ||
|-----|-----------------------------------------------------------------------------------------------------|
| `a` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html):the first operand |
| `b` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html):the second operand |

| Return ||
|----------------------------------------------------------------------------------|--------------------------|
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | the smaller of`a`and`b`. |

**See Also**

- [java.util.function.BinaryOperator](https://developer.android.com/reference/kotlin/java/util/function/BinaryOperator.html#) 

### parseDouble

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun parseDouble(s: String): Double
```

Returns a new`double`initialized to the value represented by the specified`String`, as performed by the`valueOf`method of class`Double`.

| Parameters ||
|-----|-----------------------------------------------------------------------------------------------------------|
| `s` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):the string to be parsed. |

| Return ||
|----------------------------------------------------------------------------------|------------------------------------------------------|
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | the`double`value represented by the string argument. |

| Exceptions ||
|-----------------------------------|----------------------------------------------------|
| `java.lang.NullPointerException` | if the string is null |
| `java.lang.NumberFormatException` | if the string does not contain a parsable`double`. |

**See Also**

- [java.lang.Double#valueOf(String)](https://developer.android.com/reference/kotlin/java/lang/Double#valueOf(kotlin.String)) 

### sum

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun sum(
    a: Double, 
    b: Double
): Double
```

Adds two`double`values together as per the + operator.

| Parameters ||
|-----|-----------------------------------------------------------------------------------------------------|
| `a` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html):the first operand |
| `b` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html):the second operand |

| Return ||
|----------------------------------------------------------------------------------|---------------------|
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | the sum of`a`and`b` |

**See Also**

- [java.util.function.BinaryOperator](https://developer.android.com/reference/kotlin/java/util/function/BinaryOperator.html#) 

### toByte

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toByte(): Byte
```

Returns the value of this`Double`as a`byte`after a narrowing primitive conversion.

| Return ||
|------------------------------------------------------------------------------|---------------------------------------------------------------------|
| [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | the`double`value represented by this object converted to type`byte` |

### toDouble

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toDouble(): Double
```

Returns the`double`value of this`Double`object.

| Return ||
|----------------------------------------------------------------------------------|---------------------------------------------|
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | the`double`value represented by this object |

### toFloat

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toFloat(): Float
```

Returns the value of this`Double`as a`float`after a narrowing primitive conversion.

| Return ||
|--------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | the`double`value represented by this object converted to type`float` |

### toHexString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun toHexString(d: Double): String
```

Returns a hexadecimal string representation of the`double`argument. All characters mentioned below are ASCII characters.

- If the argument is NaN, the result is the string "`NaN`".
- Otherwise, the result is a string that represents the sign and magnitude of the argument. If the sign is negative, the first character of the result is '`-`' (`'\u005Cu002D'`); if the sign is positive, no sign character appears in the result. As for the magnitude*m* :
 - If*m* is infinity, it is represented by the string`"Infinity"`; thus, positive infinity produces the result`"Infinity"`and negative infinity produces the result`"-Infinity"`.
 - If*m* is zero, it is represented by the string`"0x0.0p0"`; thus, negative zero produces the result`"-0x0.0p0"`and positive zero produces the result`"0x0.0p0"`.
 - If*m* is a`double`value with a normalized representation, substrings are used to represent the significand and exponent fields. The significand is represented by the characters`"0x1."`followed by a lowercase hexadecimal representation of the rest of the significand as a fraction. Trailing zeros in the hexadecimal representation are removed unless all the digits are zero, in which case a single zero is used. Next, the exponent is represented by`"p"`followed by a decimal string of the unbiased exponent as if produced by a call to [Integer.toString](https://developer.android.com/reference/kotlin/java/lang/Integer#toString(kotlin.Int))on the exponent value.
 - If*m* is a`double`value with a subnormal representation, the significand is represented by the characters`"0x0."`followed by a hexadecimal representation of the rest of the significand as a fraction. Trailing zeros in the hexadecimal representation are removed. Next, the exponent is represented by`"p-1022"`. Note that there must be at least one nonzero digit in a subnormal significand.

| Floating-point Value | Hexadecimal String |
| `1.0` | `0x1.0p0` |
| `-1.0` | `-0x1.0p0` |
| `2.0` | `0x1.0p1` |
| `3.0` | `0x1.8p1` |
| `0.5` | `0x1.0p-1` |
| `0.25` | `0x1.0p-2` |
| `Double.MAX_VALUE` | `0x1.fffffffffffffp1023` |
| `Minimum Normal Value` | `0x1.0p-1022` |
| `Maximum Subnormal Value` | `0x0.fffffffffffffp-1022` |
| `Double.MIN_VALUE` | `0x0.0000000000001p-1022` |
|---------------------------|---------------------------|

<br />

| Parameters ||
|-----|--------------------------------------------------------------------------------------------------------------|
| `d` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html):the`double`to be converted. |

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a hex string representation of the argument. |

### toInt

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toInt(): Int
```

Returns the value of this`Double`as an`int`after a narrowing primitive conversion.

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the`double`value represented by this object converted to type`int` |

### toLong

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toLong(): Long
```

Returns the value of this`Double`as a`long`after a narrowing primitive conversion.

| Return ||
|------------------------------------------------------------------------------|---------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the`double`value represented by this object converted to type`long` |

### toShort

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toShort(): Short
```

Returns the value of this`Double`as a`short`after a narrowing primitive conversion.

| Return ||
|--------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | the`double`value represented by this object converted to type`short` |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

Returns a string representation of this`Double`object. The primitive`double`value represented by this object is converted to a string exactly as if by the method`toString`of one argument.

| Return ||
|----------------------------------------------------------------------------------|-----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a`String`representation of this object. |

**See Also**

- [java.lang.Double#toString(double)](https://developer.android.com/reference/kotlin/java/lang/Double#toString(kotlin.Double)) 

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun toString(d: Double): String
```

Returns a string representation of the`double`argument. All characters mentioned below are ASCII characters.

- If the argument is NaN, the result is the string "`NaN`".
- Otherwise, the result is a string that represents the sign and magnitude (absolute value) of the argument. If the sign is negative, the first character of the result is '`-`' (`'\u005Cu002D'`); if the sign is positive, no sign character appears in the result. As for the magnitude*m* :
 - If*m* is infinity, it is represented by the characters`"Infinity"`; thus, positive infinity produces the result`"Infinity"`and negative infinity produces the result`"-Infinity"`.
 - If*m* is zero, it is represented by the characters`"0.0"`; thus, negative zero produces the result`"-0.0"`and positive zero produces the result`"0.0"`.
 - If*m* is greater than or equal to 10-3 but less than 107, then it is represented as the integer part of*m* , in decimal form with no leading zeroes, followed by '`.`' (`'\u005Cu002E'`), followed by one or more decimal digits representing the fractional part of*m*.
 - If*m* is less than 10-3 or greater than or equal to 107, then it is represented in so-called "computerized scientific notation." Let*n* be the unique integer such that 10*n* ≤*m* \< 10*n* +1; then let*a* be the mathematically exact quotient of*m* and 10*n* so that 1 ≤*a* \< 10. The magnitude is then represented as the integer part of*a* , as a single decimal digit, followed by '`.`' (`'\u005Cu002E'`), followed by decimal digits representing the fractional part of*a* , followed by the letter '`E`' (`'\u005Cu0045'`), followed by a representation of*n* as a decimal integer, as produced by the method [Integer.toString(int)](https://developer.android.com/reference/kotlin/java/lang/Integer#toString(kotlin.Int)).

How many digits must be printed for the fractional part of*m* or*a* ? There must be at least one digit to represent the fractional part, and beyond that as many, but only as many, more digits as are needed to uniquely distinguish the argument value from adjacent values of type`double`. That is, suppose that*x* is the exact mathematical value represented by the decimal representation produced by this method for a finite nonzero argument*d* . Then*d* must be the`double`value nearest to*x* ; or if two`double`values are equally close to*x* , then*d* must be one of them and the least significant bit of the significand of*d* must be`0`.

<br />

To create localized string representations of a floating-point value, use subclasses of [java.text.NumberFormat](https://developer.android.com/reference/kotlin/java/text/NumberFormat.html#).

| Parameters ||
|-----|--------------------------------------------------------------------------------------------------------------|
| `d` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html):the`double`to be converted. |

| Return ||
|----------------------------------------------------------------------------------|------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the argument. |

### valueOf

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun valueOf(d: Double): Double
```

Returns a`Double`instance representing the specified`double`value. If a new`Double`instance is not required, this method should generally be used in preference to the constructor [Double(double)](https://developer.android.com/reference/kotlin/java/lang/Double#Double(kotlin.Double)), as this method is likely to yield significantly better space and time performance by caching frequently requested values.

| Parameters ||
|-----|--------------------------------------------------------------------------------------------------|
| `d` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html):a double value. |

| Return ||
|----------------------------------------------------------------------------------|------------------------------------|
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | a`Double`instance representing`d`. |

### valueOf

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun valueOf(s: String): Double
```

Returns a object holding the value represented by the argument string .

If`s`is`null`, then a`NullPointerException`is thrown.

Leading and trailing whitespace characters in`s`are ignored. Whitespace is removed as if by the [java.lang.String#trim](https://developer.android.com/reference/kotlin/java/lang/String#trim())method; that is, both ASCII space and control characters are removed. The rest of`s`should constitute a*FloatValue*as described by the lexical syntax rules:

*FloatValue:*
: *Signopt* `NaN`
: *Signopt* `Infinity`
: *Signopt FloatingPointLiteral*
: *Signopt HexFloatingPointLiteral*
: *SignedInteger*

*HexFloatingPointLiteral*:
: *HexSignificand BinaryExponent FloatTypeSuffixopt*

*HexSignificand:*
: *HexNumeral*
: *HexNumeral* `.`
: `0x`*HexDigitsopt* `.`*HexDigits*
: `0X`*HexDigitsopt* `.`*HexDigits*

*BinaryExponent:*
: *BinaryExponentIndicator SignedInteger*

*BinaryExponentIndicator:*
: `p`
: `P`
where*Sign* ,*FloatingPointLiteral* ,*HexNumeral* ,*HexDigits* ,*SignedInteger* and*FloatTypeSuffix* are as defined in the lexical structure sections of The Java Language Specification, except that underscores are not accepted between digits. If`s`does not have the form of a*FloatValue* , then a`NumberFormatException`is thrown. Otherwise,`s`is regarded as representing an exact decimal value in the usual "computerized scientific notation" or as an exact hexadecimal value; this exact numerical value is then conceptually converted to an "infinitely precise" binary value that is then rounded to type`double`by the usual round-to-nearest rule of IEEE 754 floating-point arithmetic, which includes preserving the sign of a zero value. Note that the round-to-nearest rule also implies overflow and underflow behaviour; if the exact value of`s`is large enough in magnitude (greater than or equal to ([MAX_VALUE](https://developer.android.com/reference/kotlin/java/lang/Double#MAX_VALUE:kotlin.Double)+ [ulp(MAX_VALUE)](https://developer.android.com/reference/kotlin/java/lang/Math#ulp(kotlin.Double))/2), rounding to`double`will result in an infinity and if the exact value of`s`is small enough in magnitude (less than or equal to [MIN_VALUE](https://developer.android.com/reference/kotlin/java/lang/Double#MIN_VALUE:kotlin.Double)/2), rounding to float will result in a zero. Finally, after rounding a`Double`object representing this`double`value is returned.

To interpret localized string representations of a floating-point value, use subclasses of .

Note that trailing format specifiers, specifiers that determine the type of a floating-point literal (`1.0f`is a`float`value;`1.0d`is a`double`value), do*not* influence the results of this method. In other words, the numerical value of the input string is converted directly to the target floating-point type. The two-step sequence of conversions, string to`float`followed by`float`to`double`, is*not* equivalent to converting a string directly to`double`. For example, the`float`literal`0.1f`is equal to the`double`value`0.10000000149011612`; the`float`literal`0.1f`represents a different numerical value than the`double`literal`0.1`. (The numerical value 0.1 cannot be exactly represented in a binary floating-point number.)

To avoid calling this method on an invalid string and having a`NumberFormatException`be thrown, the regular expression below can be used to screen the input string: 

```kotlin
<code>final String Digits     = "(\\p{Digit}+)";
   final String HexDigits  = "(\\p{XDigit}+)";
   // an exponent is 'e' or 'E' followed by an optionally
   // signed decimal integer.
   final String Exp        = "[eE][+-]?"+Digits;
   final String fpRegex    =
       ("[\\x00-\\x20]*"+  // Optional leading "whitespace"
        "[+-]?(" + // Optional sign character
        "NaN|" +           // "NaN" string
        "Infinity|" +      // "Infinity" string
 
        // A decimal floating-point string representing a finite positive
        // number without a leading sign has at most five basic pieces:
        // Digits . Digits ExponentPart FloatTypeSuffix
        //
        // Since this method allows integer-only strings as input
        // in addition to strings of floating-point literals, the
        // two sub-patterns below are simplifications of the grammar
        // productions from section 3.10.2 of
        // The Java Language Specification.
 
        // Digits ._opt Digits_opt ExponentPart_opt FloatTypeSuffix_opt
        "((("+Digits+"(\\.)?("+Digits+"?)("+Exp+")?)|"+
 
        // . Digits ExponentPart_opt FloatTypeSuffix_opt
        "(\\.("+Digits+")("+Exp+")?)|"+
 
        // Hexadecimal strings
        "((" +
         // 0[xX] HexDigits ._opt BinaryExponent FloatTypeSuffix_opt
         "(0[xX]" + HexDigits + "(\\.)?)|" +
 
         // 0[xX] HexDigits_opt . HexDigits BinaryExponent FloatTypeSuffix_opt
         "(0[xX]" + HexDigits + "?(\\.)" + HexDigits + ")" +
 
         ")[pP][+-]?" + Digits + "))" +
        "[fFdD]?))" +
        "[\\x00-\\x20]*");// Optional trailing "whitespace"
 
   if (Pattern.matches(fpRegex, myString))
       Double.valueOf(myString); // Will not throw NumberFormatException
   else {
       // Perform suitable alternative action
   }
  </code>
```

| Parameters ||
|-----|-----------------------------------------------------------------------------------------------------------|
| `s` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):the string to be parsed. |

| Return ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | a`Double`object holding the value represented by the`String`argument. |

| Exceptions ||
|-----------------------------------|---------------------------------------------------|
| `java.lang.NumberFormatException` | if the string does not contain a parsable number. |

## Properties

### TYPE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE: Class<Double!>!
```

The`Class`instance representing the primitive type`double`.
