# DSAParams

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DSAParams

```
interface DSAParams
```

| [java.security.interfaces.DSAParams](https://developer.android.com/reference/kotlin/java/security/interfaces/DSAParams#) |

| Known Direct Subclasses [DSAParameterSpec](https://developer.android.com/reference/kotlin/java/security/spec/DSAParameterSpec.html#) |--------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------| | [DSAParameterSpec](https://developer.android.com/reference/kotlin/java/security/spec/DSAParameterSpec.html#) | This class specifies the set of parameters used with the DSA algorithm. | |

Interface to a DSA-specific set of key parameters, which defines a DSA*key family*. DSA (Digital Signature Algorithm) is defined in NIST's FIPS-186.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| abstract [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)! | [getG](https://developer.android.com/reference/kotlin/java/security/interfaces/DSAParams#getG())`()` Returns the base,`g`. |
| abstract [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)! | [getP](https://developer.android.com/reference/kotlin/java/security/interfaces/DSAParams#getP())`()` Returns the prime,`p`. |
| abstract [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)! | [getQ](https://developer.android.com/reference/kotlin/java/security/interfaces/DSAParams#getQ())`()` Returns the subprime,`q`. |

## Public methods

### getG

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getG(): BigInteger!
```

Returns the base,`g`.

| Return ||
|------------------------------------------------------------------------------------------|---------------|
| [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)! | the base,`g`. |

### getP

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getP(): BigInteger!
```

Returns the prime,`p`.

| Return ||
|------------------------------------------------------------------------------------------|----------------|
| [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)! | the prime,`p`. |

### getQ

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getQ(): BigInteger!
```

Returns the subprime,`q`.

| Return ||
|------------------------------------------------------------------------------------------|-------------------|
| [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)! | the subprime,`q`. |
