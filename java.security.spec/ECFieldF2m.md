# ECFieldF2m

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ECFieldF2m

```
open class ECFieldF2m : ECField
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [java.security.spec.ECFieldF2m](https://developer.android.com/reference/kotlin/java/security/spec/ECFieldF2m#) |

This immutable class defines an elliptic curve (EC) characteristic 2 finite field.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ECFieldF2m](https://developer.android.com/reference/kotlin/java/security/spec/ECFieldF2m#ECFieldF2m(kotlin.Int))`(`m:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates an elliptic curve characteristic 2 finite field which has 2\^`m`elements with normal basis. |
| [ECFieldF2m](https://developer.android.com/reference/kotlin/java/security/spec/ECFieldF2m#ECFieldF2m(kotlin.Int,%20kotlin.IntArray))`(`m:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `ks:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!`)` Creates an elliptic curve characteristic 2 finite field which has 2\^`m`elements with polynomial basis. |
| [ECFieldF2m](https://developer.android.com/reference/kotlin/java/security/spec/ECFieldF2m#ECFieldF2m(kotlin.Int,%20java.math.BigInteger))`(`m:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `rp:` ` [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)!`)` Creates an elliptic curve characteristic 2 finite field which has 2\^`m`elements with polynomial basis. |

| Public methods ||
|----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/java/security/spec/ECFieldF2m#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Compares this finite field for equality with the specified object. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getFieldSize](https://developer.android.com/reference/kotlin/java/security/spec/ECFieldF2m#getFieldSize())`()` Returns the field size in bits which is`m`for this characteristic 2 finite field. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getM](https://developer.android.com/reference/kotlin/java/security/spec/ECFieldF2m#getM())`()` Returns the value`m`of this characteristic 2 finite field. |
| open [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)! | [getMidTermsOfReductionPolynomial](https://developer.android.com/reference/kotlin/java/security/spec/ECFieldF2m#getMidTermsOfReductionPolynomial())`()` Returns an integer array which contains the order of the middle term(s) of the reduction polynomial for polynomial basis or null for normal basis. |
| open [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)! | [getReductionPolynomial](https://developer.android.com/reference/kotlin/java/security/spec/ECFieldF2m#getReductionPolynomial())`()` Returns a BigInteger whose i-th bit corresponds to the i-th coefficient of the reduction polynomial for polynomial basis or null for normal basis. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/java/security/spec/ECFieldF2m#hashCode())`()` Returns a hash code value for this characteristic 2 finite field. |

## Public constructors

### ECFieldF2m

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ECFieldF2m(m: Int)
```

Creates an elliptic curve characteristic 2 finite field which has 2\^`m`elements with normal basis.

| Parameters ||
|-----|---------------------------------------------------------------------------------------------------------------------|
| `m` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):with 2\^`m`being the number of elements. |

| Exceptions ||
|--------------------------------------|-----------------------|
| `java.lang.IllegalArgumentException` | if`m`is not positive. |

### ECFieldF2m

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ECFieldF2m(
    m: Int, 
    ks: IntArray!)
```

Creates an elliptic curve characteristic 2 finite field which has 2\^`m`elements with polynomial basis. The reduction polynomial for this field is based on`ks`whose content contains the order of the middle term(s) of the reduction polynomial. Note: A valid reduction polynomial is either a trinomial (X\^`m`+ X\^`k`+ 1 with`m`\>`k`\>= 1) or a pentanomial (X\^`m`+ X\^`k3`+ X\^`k2`+ X\^`k1`+ 1 with`m`\>`k3`\>`k2`\>`k1`\>= 1), so`ks`should have length 1 or 3.

| Parameters ||
|------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `m` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):with 2\^`m`being the number of elements. |
| `ks` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!:the order of the middle term(s) of the reduction polynomial. Contents of this array are copied to protect against subsequent modification. |

| Exceptions ||
|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if`ks`is null. |
| `java.lang.IllegalArgumentException` | if`m`is not positive, or the length of`ks`is neither 1 nor 3, or values in`ks`are not between`m`-1 and 1 (inclusive) and in descending order. |

### ECFieldF2m

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ECFieldF2m(
    m: Int, 
    rp: BigInteger!)
```

Creates an elliptic curve characteristic 2 finite field which has 2\^`m`elements with polynomial basis. The reduction polynomial for this field is based on`rp`whose i-th bit corresponds to the i-th coefficient of the reduction polynomial.

Note: A valid reduction polynomial is either a trinomial (X\^`m`+ X\^`k`+ 1 with`m`\>`k`\>= 1) or a pentanomial (X\^`m`+ X\^`k3`+ X\^`k2`+ X\^`k1`+ 1 with`m`\>`k3`\>`k2`\>`k1`\>= 1).

| Parameters ||
|------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `m` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):with 2\^`m`being the number of elements. |
| `rp` | [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)!:the BigInteger whose i-th bit corresponds to the i-th coefficient of the reduction polynomial. |

| Exceptions ||
|--------------------------------------|------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if`rp`is null. |
| `java.lang.IllegalArgumentException` | if`m`is not positive, or`rp`does not represent a valid reduction polynomial. |

## Public methods

### equals

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun equals(other: Any?): Boolean
```

Compares this finite field for equality with the specified object.

| Parameters ||
|-------|----------------------------|
| `obj` | the object to be compared. |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if`obj`is an instance of ECFieldF2m and both`m`and the reduction polynomial match, false otherwise. |

### getFieldSize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getFieldSize(): Int
```

Returns the field size in bits which is`m`for this characteristic 2 finite field.

| Return ||
|----------------------------------------------------------------------------|-------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the field size in bits. |

### getM

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getM(): Int
```

Returns the value`m`of this characteristic 2 finite field.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `m`with 2\^`m`being the number of elements. |

### getMidTermsOfReductionPolynomial

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getMidTermsOfReductionPolynomial(): IntArray!
```

Returns an integer array which contains the order of the middle term(s) of the reduction polynomial for polynomial basis or null for normal basis.

| Return ||
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)! | an integer array which contains the order of the middle term(s) of the reduction polynomial for polynomial basis or null for normal basis. A new array is returned each time this method is called. |

### getReductionPolynomial

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getReductionPolynomial(): BigInteger!
```

Returns a BigInteger whose i-th bit corresponds to the i-th coefficient of the reduction polynomial for polynomial basis or null for normal basis.

| Return ||
|------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)! | a BigInteger whose i-th bit corresponds to the i-th coefficient of the reduction polynomial for polynomial basis or null for normal basis. |

### hashCode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hashCode(): Int
```

Returns a hash code value for this characteristic 2 finite field.

| Return ||
|----------------------------------------------------------------------------|--------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value. |
