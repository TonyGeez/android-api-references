# BigInteger

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BigInteger

```
open class BigInteger : Number, Comparable<BigInteger!>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [kotlin.Number](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-number/index.html) ||
| | ↳ | [java.math.BigInteger](BigInteger.md) |

Immutable arbitrary-precision integers. All operations behave as if BigIntegers were represented in two's-complement notation (like Java's primitive integer types). BigInteger provides analogues to all of Java's primitive integer operators, and all relevant methods from java.lang.Math. Additionally, BigInteger provides operations for modular arithmetic, GCD calculation, primality testing, prime generation, bit manipulation, and a few other miscellaneous operations.

Semantics of arithmetic operations exactly mimic those of Java's integer arithmetic operators, as defined in*The Java Language Specification* . For example, division by zero throws an`ArithmeticException`, and division of a negative by a positive yields a negative (or zero) remainder.

Semantics of shift operations extend those of Java's shift operators to allow for negative shift distances. A right-shift with a negative shift distance results in a left shift, and vice-versa. The unsigned right shift operator (`>>>`) is omitted since this operation only makes sense for a fixed sized word and not for a representation conceptually having an infinite number of leading virtual sign bits.

Semantics of bitwise logical operations exactly mimic those of Java's bitwise integer operators. The binary operators (`and`,`or`,`xor`) implicitly perform sign extension on the shorter of the two operands prior to performing the operation.

Comparison operations perform signed integer comparisons, analogous to those performed by Java's relational and equality operators.

Modular arithmetic operations are provided to compute residues, perform exponentiation, and compute multiplicative inverses. These methods always return a non-negative result, between`0`and`(modulus - 1)`, inclusive.

Bit operations operate on a single bit of the two's-complement representation of their operand. If necessary, the operand is sign-extended so that it contains the designated bit. None of the single-bit operations can produce a BigInteger with a different sign from the BigInteger being operated on, as they affect only a single bit, and the arbitrarily large abstraction provided by this class ensures that conceptually there are infinitely many "virtual sign bits" preceding each BigInteger.

For the sake of brevity and clarity, pseudo-code is used throughout the descriptions of BigInteger methods. The pseudo-code expression`(i + j)`is shorthand for "a BigInteger whose value is that of the BigInteger`i`plus that of the BigInteger`j`." The pseudo-code expression`(i == j)`is shorthand for "`true`if and only if the BigInteger`i`represents the same value as the BigInteger`j`." Other pseudo-code expressions are interpreted similarly.

All methods and constructors in this class throw`NullPointerException`when passed a null object reference for any input parameter. BigInteger must support values in the range -2`Integer.MAX_VALUE`(exclusive) to +2`Integer.MAX_VALUE`(exclusive) and may support values outside of that range. An`ArithmeticException`is thrown when a BigInteger constructor or method would generate a value outside of the supported range. The range of probable prime values is limited and may be less than the full supported positive range of`BigInteger`. The range must be at least 1 to 2500000000.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [BigInteger](BigInteger.md))`(`val:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Translates a byte array containing the two's-complement binary representation of a BigInteger into a BigInteger. |
| [BigInteger](BigInteger.md))`(`val:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `off:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `len:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Translates a byte sub-array containing the two's-complement binary representation of a BigInteger into a BigInteger. |
| [BigInteger](BigInteger.md))`(`signum:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `magnitude:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Translates the sign-magnitude representation of a BigInteger into a BigInteger. |
| [BigInteger](BigInteger.md))`(`signum:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `magnitude:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `off:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `len:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Translates the sign-magnitude representation of a BigInteger into a BigInteger. |
| [BigInteger](BigInteger.md))`(`bitLength:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `certainty:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `rnd:` ` [Random](../java.util/Random.md)`)` Constructs a randomly generated positive BigInteger that is probably prime, with the specified bitLength. |
| [BigInteger](BigInteger.md))`(`numBits:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `rnd:` ` [Random](../java.util/Random.md)`)` Constructs a randomly generated BigInteger, uniformly distributed over the range 0 to (2`numBits`- 1), inclusive. |
| [BigInteger](BigInteger.md))`(`val:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Translates the decimal String representation of a BigInteger into a BigInteger. |
| [BigInteger](BigInteger.md))`(`val:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `radix:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Translates the String representation of a BigInteger in the specified radix into a BigInteger. |

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [BigInteger](BigInteger.md) | [abs](BigInteger.md))`()` Returns a BigInteger whose value is the absolute value of this BigInteger. |
| open [BigInteger](BigInteger.md) | [add](BigInteger.md))`(`val:` ` [BigInteger](BigInteger.md)`)` Returns a BigInteger whose value is`(this + val)`. |
| open [BigInteger](BigInteger.md) | [and](BigInteger.md))`(`val:` ` [BigInteger](BigInteger.md)`)` Returns a BigInteger whose value is`(this & val)`. |
| --- | --- |
| open [BigInteger](BigInteger.md) | [andNot](BigInteger.md))`(`val:` ` [BigInteger](BigInteger.md)`)` Returns a BigInteger whose value is`(this & ~val)`. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [bitCount](BigInteger.md))`()` Returns the number of bits in the two's complement representation of this BigInteger that differ from its sign bit. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [bitLength](BigInteger.md))`()` Returns the number of bits in the minimal two's-complement representation of this BigInteger,*excluding*a sign bit. |
| --- | --- |
| open [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [byteValueExact](BigInteger.md))`()` Converts this`BigInteger`to a`byte`, checking for lost information. |
| open [BigInteger](BigInteger.md) | [clearBit](BigInteger.md))`(`n:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns a BigInteger whose value is equivalent to this BigInteger with the designated bit cleared. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [compareTo](BigInteger.md))`(`other:` ` [BigInteger](BigInteger.md)`)` Compares this BigInteger with the specified BigInteger. |
| --- | --- |
| open [BigInteger](BigInteger.md) | [divide](BigInteger.md))`(`val:` ` [BigInteger](BigInteger.md)`)` Returns a BigInteger whose value is`(this / val)`. |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [BigInteger](BigInteger.md)!\> | [divideAndRemainder](BigInteger.md))`(`val:` ` [BigInteger](BigInteger.md)`)` Returns an array of two BigIntegers containing`(this / val)`followed by`(this % val)`. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](BigInteger.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Compares this BigInteger with the specified Object for equality. |
| --- | --- |
| open [BigInteger](BigInteger.md) | [flipBit](BigInteger.md))`(`n:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns a BigInteger whose value is equivalent to this BigInteger with the designated bit flipped. |
| open [BigInteger](BigInteger.md) | [gcd](BigInteger.md))`(`val:` ` [BigInteger](BigInteger.md)`)` Returns a BigInteger whose value is the greatest common divisor of`abs(this)`and`abs(val)`. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLowestSetBit](BigInteger.md))`()` Returns the index of the rightmost (lowest-order) one bit in this BigInteger (the number of zero bits to the right of the rightmost one bit). |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](BigInteger.md))`()` Returns the hash code for this BigInteger. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [intValueExact](BigInteger.md))`()` Converts this`BigInteger`to an`int`, checking for lost information. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isProbablePrime](BigInteger.md))`(`certainty:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns`true`if this BigInteger is probably prime,`false`if it's definitely composite. |
| --- | --- |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [longValueExact](BigInteger.md))`()` Converts this`BigInteger`to a`long`, checking for lost information. |
| open [BigInteger](BigInteger.md) | [max](BigInteger.md))`(`val:` ` [BigInteger](BigInteger.md)`)` Returns the maximum of this BigInteger and`val`. |
| open [BigInteger](BigInteger.md) | [min](BigInteger.md))`(`val:` ` [BigInteger](BigInteger.md)`)` Returns the minimum of this BigInteger and`val`. |
| --- | --- |
| open [BigInteger](BigInteger.md) | [mod](BigInteger.md))`(`m:` ` [BigInteger](BigInteger.md)`)` Returns a BigInteger whose value is`(this mod m`). |
| open [BigInteger](BigInteger.md) | [modInverse](BigInteger.md))`(`m:` ` [BigInteger](BigInteger.md)`)` Returns a BigInteger whose value is`(this`-1`mod m)`. |
| open [BigInteger](BigInteger.md) | [modPow](BigInteger.md))`(`exponent:` ` [BigInteger](BigInteger.md)`, `m:` ` [BigInteger](BigInteger.md)`)` Returns a BigInteger whose value is`(thisexponent mod m)`. |
| --- | --- |
| open [BigInteger](BigInteger.md) | [multiply](BigInteger.md))`(`val:` ` [BigInteger](BigInteger.md)`)` Returns a BigInteger whose value is`(this * val)`. |
| open [BigInteger](BigInteger.md) | [negate](BigInteger.md))`()` Returns a BigInteger whose value is`(-this)`. |
| open [BigInteger](BigInteger.md) | [nextProbablePrime](BigInteger.md))`()` Returns the first integer greater than this`BigInteger`that is probably prime. |
| --- | --- |
| open [BigInteger](BigInteger.md) | [not](BigInteger.md))`()` Returns a BigInteger whose value is`(~this)`. |
| open [BigInteger](BigInteger.md) | [or](BigInteger.md))`(`val:` ` [BigInteger](BigInteger.md)`)` Returns a BigInteger whose value is`(this | val)`. |
| open [BigInteger](BigInteger.md) | [pow](BigInteger.md))`(`exponent:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns a BigInteger whose value is`(thisexponent)`. |
| --- | --- |
| openstatic [BigInteger](BigInteger.md) | [probablePrime](BigInteger.md))`(`bitLength:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `rnd:` ` [Random](../java.util/Random.md)`)` Returns a positive BigInteger that is probably prime, with the specified bitLength. |
| open [BigInteger](BigInteger.md) | [remainder](BigInteger.md))`(`val:` ` [BigInteger](BigInteger.md)`)` Returns a BigInteger whose value is`(this % val)`. |
| open [BigInteger](BigInteger.md) | [setBit](BigInteger.md))`(`n:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns a BigInteger whose value is equivalent to this BigInteger with the designated bit set. |
| --- | --- |
| open [BigInteger](BigInteger.md) | [shiftLeft](BigInteger.md))`(`n:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns a BigInteger whose value is`(this << n)`. |
| open [BigInteger](BigInteger.md) | [shiftRight](BigInteger.md))`(`n:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns a BigInteger whose value is`(this >> n)`. |
| open [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [shortValueExact](BigInteger.md))`()` Converts this`BigInteger`to a`short`, checking for lost information. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [signum](BigInteger.md))`()` Returns the signum function of this BigInteger. |
| open [BigInteger](BigInteger.md) | [sqrt](BigInteger.md))`()` Returns the integer square root of this BigInteger. |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [BigInteger](BigInteger.md)!\> | [sqrtAndRemainder](BigInteger.md))`()` Returns an array of two BigIntegers containing the integer square root`s`of`this`and its remainder`this - s*s`, respectively. |
| --- | --- |
| open [BigInteger](BigInteger.md) | [subtract](BigInteger.md))`(`val:` ` [BigInteger](BigInteger.md)`)` Returns a BigInteger whose value is`(this - val)`. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [testBit](BigInteger.md))`(`n:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns`true`if and only if the designated bit is set. |
| open [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [toByteArray](BigInteger.md))`()` Returns a byte array containing the two's-complement representation of this BigInteger. |
| --- | --- |
| open [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [toDouble](BigInteger.md))`()` Converts this BigInteger to a`double`. |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [toFloat](BigInteger.md))`()` Converts this BigInteger to a`float`. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [toInt](BigInteger.md))`()` Converts this BigInteger to an`int`. |
| --- | --- |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [toLong](BigInteger.md))`()` Converts this BigInteger to a`long`. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](BigInteger.md))`()` Returns the decimal String representation of this BigInteger. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](BigInteger.md))`(`radix:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the String representation of this BigInteger in the given radix. |
| --- | --- |
| openstatic [BigInteger](BigInteger.md) | [valueOf](BigInteger.md))`(`val:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns a BigInteger whose value is equal to that of the specified`long`. |
| open [BigInteger](BigInteger.md) | [xor](BigInteger.md))`(`val:` ` [BigInteger](BigInteger.md)`)` Returns a BigInteger whose value is`(this ^ val)`. |

| Properties ||
|------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| static [BigInteger](BigInteger.md) | [ONE](BigInteger.md) The BigInteger constant one. |
| static [BigInteger](BigInteger.md) | [TEN](BigInteger.md) The BigInteger constant ten. |
| static [BigInteger](BigInteger.md) | [TWO](BigInteger.md) The BigInteger constant two. |
| --- | --- |
| static [BigInteger](BigInteger.md) | [ZERO](BigInteger.md) The BigInteger constant zero. |

## Public constructors

### BigInteger

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
BigInteger(val: ByteArray!)
```

Translates a byte array containing the two's-complement binary representation of a BigInteger into a BigInteger. The input array is assumed to be in*big-endian* byte-order: the most significant byte is in the zeroth element. The`val`array is assumed to be unchanged for the duration of the constructor call.

| Parameters ||
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `val` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:big-endian two's-complement binary representation of a BigInteger. |

| Exceptions ||
|-----------------------------------|--------------------------|
| `java.lang.NumberFormatException` | `val`is zero bytes long. |

### BigInteger

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
BigInteger(
    val: ByteArray!, 
    off: Int, 
    len: Int)
```

Translates a byte sub-array containing the two's-complement binary representation of a BigInteger into a BigInteger. The sub-array is specified via an offset into the array and a length. The sub-array is assumed to be in*big-endian* byte-order: the most significant byte is the element at index`off`. The`val`array is assumed to be unchanged for the duration of the constructor call. An`IndexOutOfBoundsException`is thrown if the length of the array`val`is non-zero and either`off`is negative,`len`is negative, or`off+len`is greater than the length of`val`.

| Parameters ||
|-------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `val` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:byte array containing a sub-array which is the big-endian two's-complement binary representation of a BigInteger. |
| `off` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the start offset of the binary representation. |
| `len` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of bytes to use. |
| --- | --- |

| Exceptions ||
|---------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.NumberFormatException` | `val`is zero bytes long. |
| `java.lang.IndexOutOfBoundsException` | if the provided array offset and length would cause an index into the byte array to be negative or greater than or equal to the array length. |

### BigInteger

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
BigInteger(
    signum: Int, 
    magnitude: ByteArray!)
```

Translates the sign-magnitude representation of a BigInteger into a BigInteger. The sign is represented as an integer signum value: -1 for negative, 0 for zero, or 1 for positive. The magnitude is a byte array in*big-endian* byte-order: the most significant byte is the zeroth element. A zero-length magnitude array is permissible, and will result in a BigInteger value of 0, whether signum is -1, 0 or 1. The`magnitude`array is assumed to be unchanged for the duration of the constructor call.

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `signum` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):signum of the number (-1 for negative, 0 for zero, 1 for positive). |
| `magnitude` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:big-endian binary representation of the magnitude of the number. |

| Exceptions ||
|-----------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.NumberFormatException` | `signum`is not one of the three legal values (-1, 0, and 1), or`signum`is 0 and`magnitude`contains one or more non-zero bytes. |

### BigInteger

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
BigInteger(
    signum: Int, 
    magnitude: ByteArray!, 
    off: Int, 
    len: Int)
```

Translates the sign-magnitude representation of a BigInteger into a BigInteger. The sign is represented as an integer signum value: -1 for negative, 0 for zero, or 1 for positive. The magnitude is a sub-array of a byte array in*big-endian* byte-order: the most significant byte is the element at index`off`. A zero value of the length`len`is permissible, and will result in a BigInteger value of 0, whether signum is -1, 0 or 1. The`magnitude`array is assumed to be unchanged for the duration of the constructor call. An`IndexOutOfBoundsException`is thrown if the length of the array`magnitude`is non-zero and either`off`is negative,`len`is negative, or`off+len`is greater than the length of`magnitude`.

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `signum` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):signum of the number (-1 for negative, 0 for zero, 1 for positive). |
| `magnitude` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:big-endian binary representation of the magnitude of the number. |
| `off` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the start offset of the binary representation. |
| --- | --- |
| `len` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of bytes to use. |

| Exceptions ||
|---------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.NumberFormatException` | `signum`is not one of the three legal values (-1, 0, and 1), or`signum`is 0 and`magnitude`contains one or more non-zero bytes. |
| `java.lang.IndexOutOfBoundsException` | if the provided array offset and length would cause an index into the byte array to be negative or greater than or equal to the array length. |

### BigInteger

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
BigInteger(
    bitLength: Int, 
    certainty: Int, 
    rnd: Random)
```

Constructs a randomly generated positive BigInteger that is probably prime, with the specified bitLength.

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `bitLength` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):bitLength of the returned BigInteger. |
| `certainty` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):a measure of the uncertainty that the caller is willing to tolerate. The probability that the new BigInteger represents a prime number will exceed (1 - 1/2`certainty`). The execution time of this constructor is proportional to the value of this parameter. |
| `rnd` | [Random](../java.util/Random.md):source of random bits used to select candidates to be tested for primality. |
| --- | --- |

| Exceptions ||
|---------------------------------|-------------------------------------------|
| `java.lang.ArithmeticException` | `bitLength < 2`or`bitLength`is too large. |

**See Also**

- <https://developer.android.com/reference/kotlin/java/math/BigInteger#bitLength()> 

### BigInteger

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
BigInteger(
    numBits: Int, 
    rnd: Random)
```

Constructs a randomly generated BigInteger, uniformly distributed over the range 0 to (2`numBits`- 1), inclusive. The uniformity of the distribution assumes that a fair source of random bits is provided in`rnd`. Note that this constructor always constructs a non-negative BigInteger.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| `numBits` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):maximum bitLength of the new BigInteger. |
| `rnd` | [Random](../java.util/Random.md):source of randomness to be used in computing the new BigInteger. |

| Exceptions ||
|--------------------------------------|-----------------------|
| `java.lang.IllegalArgumentException` | `numBits`is negative. |

**See Also**

- <https://developer.android.com/reference/kotlin/java/math/BigInteger#bitLength()> 

### BigInteger

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
BigInteger(val: String)
```

Translates the decimal String representation of a BigInteger into a BigInteger. The String representation consists of an optional minus or plus sign followed by a sequence of one or more decimal digits. The character-to-digit mapping is provided by [Character.digit](../java.lang/Character.md)). The String may not contain any extraneous characters (whitespace, for example).

| Parameters ||
|-------|-------------------------------------------------------------------------------------------------------------------------------|
| `val` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):decimal String representation of BigInteger. |

| Exceptions ||
|-----------------------------------|-----------------------------------------------------|
| `java.lang.NumberFormatException` | `val`is not a valid representation of a BigInteger. |

### BigInteger

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
BigInteger(
    val: String, 
    radix: Int)
```

Translates the String representation of a BigInteger in the specified radix into a BigInteger. The String representation consists of an optional minus or plus sign followed by a sequence of one or more digits in the specified radix. The character-to-digit mapping is provided by [Character.digit](../java.lang/Character.md)). The String may not contain any extraneous characters (whitespace, for example).

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------|
| `val` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):String representation of BigInteger. |
| `radix` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):radix to be used in interpreting`val`. |

| Exceptions ||
|-----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.NumberFormatException` | `val`is not a valid representation of a BigInteger in the specified radix, or`radix`is outside the range from [Character.MIN_RADIX](../java.lang/Character.md) to [Character.MAX_RADIX](../java.lang/Character.md), inclusive. |

## Public methods

### abs

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun abs(): BigInteger
```

Returns a BigInteger whose value is the absolute value of this BigInteger.

| Return ||
|------------------------------------------------------------------------------------|-------------|
| [BigInteger](BigInteger.md) | `abs(this)` |

### add

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun add(val: BigInteger): BigInteger
```

Returns a BigInteger whose value is`(this + val)`.

| Parameters ||
|-------|--------------------------------------------------------------------------------------------------------------------------|
| `val` | [BigInteger](BigInteger.md):value to be added to this BigInteger. |

| Return ||
|------------------------------------------------------------------------------------|--------------|
| [BigInteger](BigInteger.md) | `this + val` |

### and

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun and(val: BigInteger): BigInteger
```

Returns a BigInteger whose value is`(this & val)`. (This method returns a negative BigInteger if and only if this and val are both negative.)

| Parameters ||
|-------|-----------------------------------------------------------------------------------------------------------------------------|
| `val` | [BigInteger](BigInteger.md):value to be AND'ed with this BigInteger. |

| Return ||
|------------------------------------------------------------------------------------|--------------|
| [BigInteger](BigInteger.md) | `this & val` |

### andNot

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun andNot(val: BigInteger): BigInteger
```

Returns a BigInteger whose value is`(this & ~val)`. This method, which is equivalent to`and(val.not())`, is provided as a convenience for masking operations. (This method returns a negative BigInteger if and only if`this`is negative and`val`is positive.)

| Parameters ||
|-------|----------------------------------------------------------------------------------------------------------------------------------------------|
| `val` | [BigInteger](BigInteger.md):value to be complemented and AND'ed with this BigInteger. |

| Return ||
|------------------------------------------------------------------------------------|---------------|
| [BigInteger](BigInteger.md) | `this & ~val` |

### bitCount

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun bitCount(): Int
```

Returns the number of bits in the two's complement representation of this BigInteger that differ from its sign bit. This method is useful when implementing bit-vector style sets atop BigIntegers.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | number of bits in the two's complement representation of this BigInteger that differ from its sign bit. |

### bitLength

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun bitLength(): Int
```

Returns the number of bits in the minimal two's-complement representation of this BigInteger,*excluding* a sign bit. For positive BigIntegers, this is equivalent to the number of bits in the ordinary binary representation. For zero this method returns`0`. (Computes`(ceil(log2(this < 0 ? -this : this+1)))`.)

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | number of bits in the minimal two's-complement representation of this BigInteger,*excluding*a sign bit. |

### byteValueExact

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun byteValueExact(): Byte
```

Converts this`BigInteger`to a`byte`, checking for lost information. If the value of this`BigInteger`is out of the range of the`byte`type, then an`ArithmeticException`is thrown.

| Return ||
|------------------------------------------------------------------------------|---------------------------------------|
| [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | this`BigInteger`converted to a`byte`. |

| Exceptions ||
|---------------------------------|-------------------------------------------------------|
| `java.lang.ArithmeticException` | if the value of`this`will not exactly fit in a`byte`. |

**See Also**

- [java.math.BigInteger#byteValue](../java.lang/Number.md)) 

### clearBit

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun clearBit(n: Int): BigInteger
```

Returns a BigInteger whose value is equivalent to this BigInteger with the designated bit cleared. (Computes`(this & ~(1<<n))`.)

| Parameters ||
|-----|---------------------------------------------------------------------------------------------------|
| `n` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):index of bit to clear. |

| Return ||
|------------------------------------------------------------------------------------|------------------|
| [BigInteger](BigInteger.md) | `this & ~(1<<n)` |

| Exceptions ||
|---------------------------------|-----------------|
| `java.lang.ArithmeticException` | `n`is negative. |

### compareTo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun compareTo(other: BigInteger): Int
```

Compares this BigInteger with the specified BigInteger. This method is provided in preference to individual methods for each of the six boolean comparison operators (\<, ==, \>, \>=, !=, \<=). The suggested idiom for performing these comparisons is:`(x.compareTo(y)`\<*op* \>`0)`, where \<*op*\> is one of the six comparison operators.

| Parameters ||
|-------|--------------------------------------------------------|
| `o` | the object to be compared. |
| `val` | BigInteger to which this BigInteger is to be compared. |

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | -1, 0 or 1 as this BigInteger is numerically less than, equal to, or greater than`val`. |

| Exceptions ||
|----------------------------------|--------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if the specified object is null |
| `java.lang.ClassCastException` | if the specified object's type prevents it from being compared to this object. |

### divide

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun divide(val: BigInteger): BigInteger
```

Returns a BigInteger whose value is`(this / val)`.

| Parameters ||
|-------|-------------------------------------------------------------------------------------------------------------------------------------|
| `val` | [BigInteger](BigInteger.md):value by which this BigInteger is to be divided. |

| Return ||
|------------------------------------------------------------------------------------|--------------|
| [BigInteger](BigInteger.md) | `this / val` |

| Exceptions ||
|---------------------------------|-----------------|
| `java.lang.ArithmeticException` | if`val`is zero. |

### divideAndRemainder

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun divideAndRemainder(val: BigInteger): Array<BigInteger!>
```

Returns an array of two BigIntegers containing`(this / val)`followed by`(this % val)`.

| Parameters ||
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `val` | [BigInteger](BigInteger.md):value by which this BigInteger is to be divided, and the remainder computed. |

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [BigInteger](BigInteger.md)!> | an array of two BigIntegers: the quotient`(this / val)`is the initial element, and the remainder`(this % val)`is the final element. |

| Exceptions ||
|---------------------------------|-----------------|
| `java.lang.ArithmeticException` | if`val`is zero. |

### equals

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun equals(other: Any?): Boolean
```

Compares this BigInteger with the specified Object for equality.

| Parameters ||
|-------|----------------------------------------------------|
| `obj` | the reference object with which to compare. |
| `x` | Object to which this BigInteger is to be compared. |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if and only if the specified Object is a BigInteger whose value is numerically equal to this BigInteger. |

### flipBit

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun flipBit(n: Int): BigInteger
```

Returns a BigInteger whose value is equivalent to this BigInteger with the designated bit flipped. (Computes`(this ^ (1<<n))`.)

| Parameters ||
|-----|--------------------------------------------------------------------------------------------------|
| `n` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):index of bit to flip. |

| Return ||
|------------------------------------------------------------------------------------|-----------------|
| [BigInteger](BigInteger.md) | `this ^ (1<<n)` |

| Exceptions ||
|---------------------------------|-----------------|
| `java.lang.ArithmeticException` | `n`is negative. |

### gcd

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun gcd(val: BigInteger): BigInteger
```

Returns a BigInteger whose value is the greatest common divisor of`abs(this)`and`abs(val)`. Returns 0 if`this == 0 && val == 0`.

| Parameters ||
|-------|--------------------------------------------------------------------------------------------------------------------------------|
| `val` | [BigInteger](BigInteger.md):value with which the GCD is to be computed. |

| Return ||
|------------------------------------------------------------------------------------|----------------------------|
| [BigInteger](BigInteger.md) | `GCD(abs(this), abs(val))` |

### getLowestSetBit

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getLowestSetBit(): Int
```

Returns the index of the rightmost (lowest-order) one bit in this BigInteger (the number of zero bits to the right of the rightmost one bit). Returns -1 if this BigInteger contains no one bits. (Computes`(this == 0? -1 : log2(this & -this))`.)

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | index of the rightmost one bit in this BigInteger. |

### hashCode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hashCode(): Int
```

Returns the hash code for this BigInteger.

| Return ||
|----------------------------------------------------------------------------|--------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | hash code for this BigInteger. |

### intValueExact

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun intValueExact(): Int
```

Converts this`BigInteger`to an`int`, checking for lost information. If the value of this`BigInteger`is out of the range of the`int`type, then an`ArithmeticException`is thrown.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | this`BigInteger`converted to an`int`. |

| Exceptions ||
|---------------------------------|-------------------------------------------------------|
| `java.lang.ArithmeticException` | if the value of`this`will not exactly fit in an`int`. |

**See Also**

- [java.math.BigInteger#intValue](BigInteger.md)) 

### isProbablePrime

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isProbablePrime(certainty: Int): Boolean
```

Returns`true`if this BigInteger is probably prime,`false`if it's definitely composite. If`certainty`is ≤ 0,`true`is returned.

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `certainty` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):a measure of the uncertainty that the caller is willing to tolerate: if the call returns`true`the probability that this BigInteger is prime exceeds (1 - 1/2`certainty`). The execution time of this method is proportional to the value of this parameter. |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this BigInteger is probably prime,`false`if it's definitely composite. |

### longValueExact

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun longValueExact(): Long
```

Converts this`BigInteger`to a`long`, checking for lost information. If the value of this`BigInteger`is out of the range of the`long`type, then an`ArithmeticException`is thrown.

| Return ||
|------------------------------------------------------------------------------|---------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | this`BigInteger`converted to a`long`. |

| Exceptions ||
|---------------------------------|-------------------------------------------------------|
| `java.lang.ArithmeticException` | if the value of`this`will not exactly fit in a`long`. |

**See Also**

- [java.math.BigInteger#longValue](BigInteger.md)) 

### max

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun max(val: BigInteger): BigInteger
```

Returns the maximum of this BigInteger and`val`.

| Parameters ||
|-------|------------------------------------------------------------------------------------------------------------------------------------|
| `val` | [BigInteger](BigInteger.md):value with which the maximum is to be computed. |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [BigInteger](BigInteger.md) | the BigInteger whose value is the greater of this and`val`. If they are equal, either may be returned. |

### min

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun min(val: BigInteger): BigInteger
```

Returns the minimum of this BigInteger and`val`.

| Parameters ||
|-------|------------------------------------------------------------------------------------------------------------------------------------|
| `val` | [BigInteger](BigInteger.md):value with which the minimum is to be computed. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [BigInteger](BigInteger.md) | the BigInteger whose value is the lesser of this BigInteger and`val`. If they are equal, either may be returned. |

### mod

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun mod(m: BigInteger): BigInteger
```

Returns a BigInteger whose value is`(this mod m`). This method differs from`remainder`in that it always returns a*non-negative*BigInteger.

| Parameters ||
|-----|-------------------------------------------------------------------------------------------------|
| `m` | [BigInteger](BigInteger.md):the modulus. |

| Return ||
|------------------------------------------------------------------------------------|--------------|
| [BigInteger](BigInteger.md) | `this mod m` |

| Exceptions ||
|---------------------------------|--------|
| `java.lang.ArithmeticException` | `m`≤ 0 |

**See Also**

- [#remainder](BigInteger.md)) 

### modInverse

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun modInverse(m: BigInteger): BigInteger
```

Returns a BigInteger whose value is`(this`-1`mod m)`.

| Parameters ||
|-----|-------------------------------------------------------------------------------------------------|
| `m` | [BigInteger](BigInteger.md):the modulus. |

| Return ||
|------------------------------------------------------------------------------------|------------------|
| [BigInteger](BigInteger.md) | `this`-1`mod m`. |

| Exceptions ||
|---------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| `java.lang.ArithmeticException` | `m`≤ 0, or this BigInteger has no multiplicative inverse mod m (that is, this BigInteger is not*relatively prime*to m). |

### modPow

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun modPow(
    exponent: BigInteger, 
    m: BigInteger
): BigInteger
```

Returns a BigInteger whose value is`(thisexponent mod m)`. (Unlike`pow`, this method permits negative exponents.)

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------|
| `exponent` | [BigInteger](BigInteger.md):the exponent. |
| `m` | [BigInteger](BigInteger.md):the modulus. |

| Return ||
|------------------------------------------------------------------------------------|----------------------|
| [BigInteger](BigInteger.md) | `thisexponent mod m` |

| Exceptions ||
|---------------------------------|----------------------------------------------------------------------------------------|
| `java.lang.ArithmeticException` | `m`≤ 0 or the exponent is negative and this BigInteger is not*relatively prime* to`m`. |

**See Also**

- [#modInverse](BigInteger.md)) 

### multiply

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun multiply(val: BigInteger): BigInteger
```

Returns a BigInteger whose value is`(this * val)`.

| Parameters ||
|-------|-------------------------------------------------------------------------------------------------------------------------------|
| `val` | [BigInteger](BigInteger.md):value to be multiplied by this BigInteger. |

| Return ||
|------------------------------------------------------------------------------------|--------------|
| [BigInteger](BigInteger.md) | `this * val` |

### negate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun negate(): BigInteger
```

Returns a BigInteger whose value is`(-this)`.

| Return ||
|------------------------------------------------------------------------------------|---------|
| [BigInteger](BigInteger.md) | `-this` |

### nextProbablePrime

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun nextProbablePrime(): BigInteger
```

Returns the first integer greater than this`BigInteger`that is probably prime. The probability that the number returned by this method is composite does not exceed 2-100. This method will never skip over a prime when searching: if it returns`p`, there is no prime`q`such that`this < q < p`.

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [BigInteger](BigInteger.md) | the first integer greater than this`BigInteger`that is probably prime. |

| Exceptions ||
|---------------------------------|---------------------------------|
| `java.lang.ArithmeticException` | `this < 0`or`this`is too large. |

### not

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun not(): BigInteger
```

Returns a BigInteger whose value is`(~this)`. (This method returns a negative value if and only if this BigInteger is non-negative.)

| Return ||
|------------------------------------------------------------------------------------|---------|
| [BigInteger](BigInteger.md) | `~this` |

### or

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun or(val: BigInteger): BigInteger
```

Returns a BigInteger whose value is`(this | val)`. (This method returns a negative BigInteger if and only if either this or val is negative.)
| --- | --- |

| Parameters ||
|-------|----------------------------------------------------------------------------------------------------------------------------|
| `val` | [BigInteger](BigInteger.md):value to be OR'ed with this BigInteger. |

| Return ||
|------------------------------------------------------------------------------------|--------------|
| [BigInteger](BigInteger.md) | `this | val` |

### pow

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun pow(exponent: Int): BigInteger
```

Returns a BigInteger whose value is`(thisexponent)`. Note that`exponent`is an integer rather than a BigInteger.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------|
| `exponent` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):exponent to which this BigInteger is to be raised. |

| Return ||
|------------------------------------------------------------------------------------|----------------|
| [BigInteger](BigInteger.md) | `thisexponent` |

| Exceptions ||
|---------------------------------|---------------------------------------------------------------------------------------|
| `java.lang.ArithmeticException` | `exponent`is negative. (This would cause the operation to yield a non-integer value.) |

### probablePrime

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun probablePrime(
    bitLength: Int, 
    rnd: Random
): BigInteger
```

Returns a positive BigInteger that is probably prime, with the specified bitLength. The probability that a BigInteger returned by this method is composite does not exceed 2-100.

| Parameters ||
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `bitLength` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):bitLength of the returned BigInteger. |
| `rnd` | [Random](../java.util/Random.md):source of random bits used to select candidates to be tested for primality. |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------|
| [BigInteger](BigInteger.md) | a BigInteger of`bitLength`bits that is probably prime |

| Exceptions ||
|---------------------------------|-------------------------------------------|
| `java.lang.ArithmeticException` | `bitLength < 2`or`bitLength`is too large. |

**See Also**

- <https://developer.android.com/reference/kotlin/java/math/BigInteger#bitLength()> 

### remainder

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun remainder(val: BigInteger): BigInteger
```

Returns a BigInteger whose value is`(this % val)`.

| Parameters ||
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `val` | [BigInteger](BigInteger.md):value by which this BigInteger is to be divided, and the remainder computed. |

| Return ||
|------------------------------------------------------------------------------------|--------------|
| [BigInteger](BigInteger.md) | `this % val` |

| Exceptions ||
|---------------------------------|-----------------|
| `java.lang.ArithmeticException` | if`val`is zero. |

### setBit

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setBit(n: Int): BigInteger
```

Returns a BigInteger whose value is equivalent to this BigInteger with the designated bit set. (Computes`(this | (1<<n))`.)
| --- | --- |

| Parameters ||
|-----|-------------------------------------------------------------------------------------------------|
| `n` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):index of bit to set. |

| Return ||
|------------------------------------------------------------------------------------|-----------------|
| [BigInteger](BigInteger.md) | `this | (1<<n)` |

| Exceptions ||
|---------------------------------|-----------------|
| `java.lang.ArithmeticException` | `n`is negative. |

### shiftLeft

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun shiftLeft(n: Int): BigInteger
```

Returns a BigInteger whose value is`(this << n)`. The shift distance,`n`, may be negative, in which case this method performs a right shift. (Computes`floor(this * 2n)`.)

| Parameters ||
|-----|-----------------------------------------------------------------------------------------------------|
| `n` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):shift distance, in bits. |

| Return ||
|------------------------------------------------------------------------------------|-------------|
| [BigInteger](BigInteger.md) | `this << n` |

**See Also**

- [#shiftRight](BigInteger.md)) 

### shiftRight

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun shiftRight(n: Int): BigInteger
```

Returns a BigInteger whose value is`(this >> n)`. Sign extension is performed. The shift distance,`n`, may be negative, in which case this method performs a left shift. (Computes`floor(this / 2n)`.)

| Parameters ||
|-----|-----------------------------------------------------------------------------------------------------|
| `n` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):shift distance, in bits. |

| Return ||
|------------------------------------------------------------------------------------|-------------|
| [BigInteger](BigInteger.md) | `this >> n` |

**See Also**

- [#shiftLeft](BigInteger.md)) 

### shortValueExact

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun shortValueExact(): Short
```

Converts this`BigInteger`to a`short`, checking for lost information. If the value of this`BigInteger`is out of the range of the`short`type, then an`ArithmeticException`is thrown.

| Return ||
|--------------------------------------------------------------------------------|----------------------------------------|
| [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | this`BigInteger`converted to a`short`. |

| Exceptions ||
|---------------------------------|--------------------------------------------------------|
| `java.lang.ArithmeticException` | if the value of`this`will not exactly fit in a`short`. |

**See Also**

- [java.math.BigInteger#shortValue](../java.lang/Number.md)) 

### signum

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun signum(): Int
```

Returns the signum function of this BigInteger.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | -1, 0 or 1 as the value of this BigInteger is negative, zero or positive. |

### sqrt

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun sqrt(): BigInteger
```

Returns the integer square root of this BigInteger. The integer square root of the corresponding mathematical integer`n`is the largest mathematical integer`s`such that`s*s <= n`. It is equal to the value of`floor(sqrt(n))`, where`sqrt(n)`denotes the real square root of`n`treated as a real. Note that the integer square root will be less than the real square root if the latter is not representable as an integral value.

| Return ||
|------------------------------------------------------------------------------------|----------------------------------|
| [BigInteger](BigInteger.md) | the integer square root of`this` |

| Exceptions ||
|---------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.ArithmeticException` | if`this`is negative. (The square root of a negative integer`val`is`(i * sqrt(-val))`where*i* is the*imaginary unit* and is equal to`sqrt(-1)`.) |

### sqrtAndRemainder

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun sqrtAndRemainder(): Array<BigInteger!>
```

Returns an array of two BigIntegers containing the integer square root`s`of`this`and its remainder`this - s*s`, respectively.

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [BigInteger](BigInteger.md)!> | an array of two BigIntegers with the integer square root at offset 0 and the remainder at offset 1 |

| Exceptions ||
|---------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.ArithmeticException` | if`this`is negative. (The square root of a negative integer`val`is`(i * sqrt(-val))`where*i* is the*imaginary unit* and is equal to`sqrt(-1)`.) |

**See Also**

- <https://developer.android.com/reference/kotlin/java/math/BigInteger#sqrt()> 

### subtract

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun subtract(val: BigInteger): BigInteger
```

Returns a BigInteger whose value is`(this - val)`.

| Parameters ||
|-------|---------------------------------------------------------------------------------------------------------------------------------|
| `val` | [BigInteger](BigInteger.md):value to be subtracted from this BigInteger. |

| Return ||
|------------------------------------------------------------------------------------|--------------|
| [BigInteger](BigInteger.md) | `this - val` |

### testBit

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun testBit(n: Int): Boolean
```

Returns`true`if and only if the designated bit is set. (Computes`((this & (1<<n)) != 0)`.)

| Parameters ||
|-----|--------------------------------------------------------------------------------------------------|
| `n` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):index of bit to test. |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if and only if the designated bit is set. |

| Exceptions ||
|---------------------------------|-----------------|
| `java.lang.ArithmeticException` | `n`is negative. |

### toByteArray

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toByteArray(): ByteArray!
```

Returns a byte array containing the two's-complement representation of this BigInteger. The byte array will be in*big-endian* byte-order: the most significant byte is in the zeroth element. The array will contain the minimum number of bytes required to represent this BigInteger, including at least one sign bit, which is`(ceil((this.bitLength() + 1)/8))`. (This representation is compatible with the[(byte[])](https://developer.android.com/reference/kotlin/java/math/BigInteger#BigInteger(kotlin.ByteArray))constructor.)

| Return ||
|------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | a byte array containing the two's-complement representation of this BigInteger. |

**See Also**

- [#BigInteger(byte[])](https://developer.android.com/reference/kotlin/java/math/BigInteger#BigInteger(kotlin.ByteArray)) 

### toDouble

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toDouble(): Double
```

Converts this BigInteger to a`double`. This conversion is similar to the*narrowing primitive conversion* from`double`to`float`as defined in The Java Language Specification: if this BigInteger has too great a magnitude to represent as a`double`, it will be converted to [Double.NEGATIVE_INFINITY](../java.lang/Double.md) or [java.lang.Double#POSITIVE_INFINITY](../java.lang/Double.md) as appropriate. Note that even when the return value is finite, this conversion can lose information about the precision of the BigInteger value.

| Return ||
|----------------------------------------------------------------------------------|-----------------------------------------|
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | this BigInteger converted to a`double`. |

### toFloat

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toFloat(): Float
```

Converts this BigInteger to a`float`. This conversion is similar to the*narrowing primitive conversion* from`double`to`float`as defined in The Java Language Specification: if this BigInteger has too great a magnitude to represent as a`float`, it will be converted to [Float.NEGATIVE_INFINITY](../java.lang/Float.md) or [java.lang.Float#POSITIVE_INFINITY](../java.lang/Float.md) as appropriate. Note that even when the return value is finite, this conversion can lose information about the precision of the BigInteger value.

| Return ||
|--------------------------------------------------------------------------------|----------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | this BigInteger converted to a`float`. |

### toInt

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toInt(): Int
```

Converts this BigInteger to an`int`. This conversion is analogous to a*narrowing primitive conversion* from`long`to`int`as defined in The Java Language Specification: if this BigInteger is too big to fit in an`int`, only the low-order 32 bits are returned. Note that this conversion can lose information about the overall magnitude of the BigInteger value as well as return a result with the opposite sign.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | this BigInteger converted to an`int`. |

**See Also**

- <https://developer.android.com/reference/kotlin/java/math/BigInteger#intValueExact()> 

### toLong

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toLong(): Long
```

Converts this BigInteger to a`long`. This conversion is analogous to a*narrowing primitive conversion* from`long`to`int`as defined in The Java Language Specification: if this BigInteger is too big to fit in a`long`, only the low-order 64 bits are returned. Note that this conversion can lose information about the overall magnitude of the BigInteger value as well as return a result with the opposite sign.

| Return ||
|------------------------------------------------------------------------------|---------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | this BigInteger converted to a`long`. |

**See Also**

- <https://developer.android.com/reference/kotlin/java/math/BigInteger#longValueExact()> 

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

Returns the decimal String representation of this BigInteger. The digit-to-character mapping provided by`Character.forDigit`is used, and a minus sign is prepended if appropriate. (This representation is compatible with the [(String)](BigInteger.md))constructor, and allows for String concatenation with Java's + operator.)

| Return ||
|----------------------------------------------------------------------------------|---------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | decimal String representation of this BigInteger. |

**See Also**

- [java.lang.Character#forDigit](../java.lang/Character.md))
- [#BigInteger(java.lang.String)](BigInteger.md)) 

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(radix: Int): String
```

Returns the String representation of this BigInteger in the given radix. If the radix is outside the range from [java.lang.Character#MIN_RADIX](../java.lang/Character.md) to [Character.MAX_RADIX](../java.lang/Character.md) inclusive, it will default to 10 (as is the case for`Integer.toString`). The digit-to-character mapping provided by`Character.forDigit`is used, and a minus sign is prepended if appropriate. (This representation is compatible with the [(String,](BigInteger.md))constructor.)

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------|
| `radix` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):radix of the String representation. |

| Return ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | String representation of this BigInteger in the given radix. |

**See Also**

- [java.lang.Character#forDigit](../java.lang/Character.md))
- [#BigInteger(java.lang.String, int)](BigInteger.md)) 

### valueOf

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun valueOf(val: Long): BigInteger
```

Returns a BigInteger whose value is equal to that of the specified`long`.

| Parameters ||
|-------|-----------------------------------------------------------------------------------------------------------------|
| `val` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):value of the BigInteger to return. |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------|
| [BigInteger](BigInteger.md) | a BigInteger with the specified value. |

### xor

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun xor(val: BigInteger): BigInteger
```

Returns a BigInteger whose value is`(this ^ val)`. (This method returns a negative BigInteger if and only if exactly one of this and val are negative.)

| Parameters ||
|-------|-----------------------------------------------------------------------------------------------------------------------------|
| `val` | [BigInteger](BigInteger.md):value to be XOR'ed with this BigInteger. |

| Return ||
|------------------------------------------------------------------------------------|--------------|
| [BigInteger](BigInteger.md) | `this ^ val` |

## Properties

### ONE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ONE: BigInteger
```

The BigInteger constant one. 

### TEN

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TEN: BigInteger
```

The BigInteger constant ten. 

### TWO

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TWO: BigInteger
```

The BigInteger constant two. 

### ZERO

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ZERO: BigInteger
```

The BigInteger constant zero.
