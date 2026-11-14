# DSAPublicKey

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DSAPublicKey

```
interface DSAPublicKey : DSAKey, PublicKey
```

| [java.security.interfaces.DSAPublicKey](../java/security/interfaces/DSAPublicKey.md) |

The interface to a DSA public key. DSA (Digital Signature Algorithm) is defined in NIST's FIPS-186.

## Summary

| Constants ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [serialVersionUID](../java/security/interfaces/DSAPublicKey.md) The class fingerprint that is set to indicate serialization compatibility with a previous version of the class. |

| Public methods ||
|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [BigInteger](../java/math/BigInteger.md)! | [getY](../java/security/interfaces/DSAPublicKey.md))`()` Returns the value of the public key,`y`. |

| Inherited functions ||
|---|---|
| From class [DSAKey](../java/security/interfaces/DSAKey.md) |-------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [DSAParams](../java/security/interfaces/DSAParams.md)! | [getParams](../java/security/interfaces/DSAKey.md))`()` <br /> Returns the DSA-specific key parameters. These parameters are never secret. <br /> | ||

## Constants

### serialVersionUID

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val serialVersionUID: Long
```

**Deprecated:** *A`serialVersionUID`field in an interface is ineffectual. Do not use; no replacement.*

The class fingerprint that is set to indicate serialization compatibility with a previous version of the class. 

 Value: 1234526332779022332L

## Public methods

### getY

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getY(): BigInteger!
```

Returns the value of the public key,`y`.

| Return ||
|------------------------------------------------------------------------------------------|----------------------------------|
| [BigInteger](../java/math/BigInteger.md)! | the value of the public key,`y`. |
