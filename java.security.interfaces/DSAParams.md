# DSAParams

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DSAParams

```
interface DSAParams
```

| [java.security.interfaces.DSAParams](DSAParams.md) |

| Known Direct Subclasses [DSAParameterSpec](../java.security.spec/DSAParameterSpec.md) |--------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------| | [DSAParameterSpec](../java.security.spec/DSAParameterSpec.md) | This class specifies the set of parameters used with the DSA algorithm. | |
| --- | --- | --- | --- | --- | --- | --- |

Interface to a DSA-specific set of key parameters, which defines a DSA*key family*. DSA (Digital Signature Algorithm) is defined in NIST's FIPS-186.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| abstract [BigInteger](../java.math/BigInteger.md)! | [getG](DSAParams.md))`()` Returns the base,`g`. |
| abstract [BigInteger](../java.math/BigInteger.md)! | [getP](DSAParams.md))`()` Returns the prime,`p`. |
| abstract [BigInteger](../java.math/BigInteger.md)! | [getQ](DSAParams.md))`()` Returns the subprime,`q`. |
| --- | --- |

## Public methods

### getG

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getG(): BigInteger!
```

Returns the base,`g`.

| Return ||
|------------------------------------------------------------------------------------------|---------------|
| [BigInteger](../java.math/BigInteger.md)! | the base,`g`. |

### getP

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getP(): BigInteger!
```

Returns the prime,`p`.

| Return ||
|------------------------------------------------------------------------------------------|----------------|
| [BigInteger](../java.math/BigInteger.md)! | the prime,`p`. |

### getQ

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getQ(): BigInteger!
```

Returns the subprime,`q`.

| Return ||
|------------------------------------------------------------------------------------------|-------------------|
| [BigInteger](../java.math/BigInteger.md)! | the subprime,`q`. |
