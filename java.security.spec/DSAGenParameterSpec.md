# DSAGenParameterSpec

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DSAGenParameterSpec

```
class DSAGenParameterSpec : AlgorithmParameterSpec
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.security.spec.DSAGenParameterSpec](DSAGenParameterSpec.md) |

This immutable class specifies the set of parameters used for generating DSA parameters as specified in [FIPS 186-3 Digital Signature Standard (DSS)](http://csrc.nist.gov/publications/fips/fips186-3/fips_186-3.pdf).

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [DSAGenParameterSpec](DSAGenParameterSpec.md))`(`primePLen:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `subprimeQLen:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a domain parameter specification for DSA parameter generation using `primePLen` and `subprimeQLen`. |
| [DSAGenParameterSpec](DSAGenParameterSpec.md))`(`primePLen:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `subprimeQLen:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `seedLen:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a domain parameter specification for DSA parameter generation using `primePLen`, `subprimeQLen`, and `seedLen`. |

| Public methods ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPrimePLength](DSAGenParameterSpec.md))`()` Returns the desired length of the prime P of the to-be-generated DSA domain parameters in bits. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSeedLength](DSAGenParameterSpec.md))`()` Returns the desired length of the domain parameter seed in bits. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSubprimeQLength](DSAGenParameterSpec.md))`()` Returns the desired length of the sub-prime Q of the to-be-generated DSA domain parameters in bits. |
| --- | --- |

## Public constructors

### DSAGenParameterSpec

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
DSAGenParameterSpec(
    primePLen: Int, 
    subprimeQLen: Int)
```

Creates a domain parameter specification for DSA parameter generation using `primePLen` and `subprimeQLen`. The value of `subprimeQLen` is also used as the default length of the domain parameter seed in bits.

| Parameters ||
|----------------|----------------------------------------------------------------------------------------------------------------------------|
| `primePLen` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the desired length of the prime P in bits. |
| `subprimeQLen` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the desired length of the sub-prime Q in bits. |

| Exceptions ||
|--------------------------------------|----------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if `primePLen` or `subprimeQLen` is illegal per the specification of FIPS 186-3. |

### DSAGenParameterSpec

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
DSAGenParameterSpec(
    primePLen: Int, 
    subprimeQLen: Int, 
    seedLen: Int)
```

Creates a domain parameter specification for DSA parameter generation using `primePLen`, `subprimeQLen`, and `seedLen`.

| Parameters ||
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `primePLen` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the desired length of the prime P in bits. |
| `subprimeQLen` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the desired length of the sub-prime Q in bits. |
| `seedLen` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the desired length of the domain parameter seed in bits, shall be equal to or greater than `subprimeQLen`. |
| --- | --- |

| Exceptions ||
|--------------------------------------|-------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if `primePLenLen`, `subprimeQLen`, or `seedLen` is illegal per the specification of FIPS 186-3. |

## Public methods

### getPrimePLength

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPrimePLength(): Int
```

Returns the desired length of the prime P of the to-be-generated DSA domain parameters in bits.

| Return ||
|----------------------------------------------------------------------------|----------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the length of the prime P. |

### getSeedLength

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSeedLength(): Int
```

Returns the desired length of the domain parameter seed in bits.

| Return ||
|----------------------------------------------------------------------------|------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the length of the domain parameter seed. |

### getSubprimeQLength

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSubprimeQLength(): Int
```

Returns the desired length of the sub-prime Q of the to-be-generated DSA domain parameters in bits.

| Return ||
|----------------------------------------------------------------------------|--------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the length of the sub-prime Q. |
