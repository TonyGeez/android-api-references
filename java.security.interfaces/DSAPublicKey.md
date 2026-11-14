# DSAPublicKey

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DSAPublicKey

```
interface DSAPublicKey : DSAKey, PublicKey
```

| [java.security.interfaces.DSAPublicKey](https://developer.android.com/reference/kotlin/java/security/interfaces/DSAPublicKey#) |

The interface to a DSA public key. DSA (Digital Signature Algorithm) is defined in NIST's FIPS-186.

## Summary

| Constants ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [serialVersionUID](https://developer.android.com/reference/kotlin/java/security/interfaces/DSAPublicKey#serialVersionUID:kotlin.Long) The class fingerprint that is set to indicate serialization compatibility with a previous version of the class. |

| Public methods ||
|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)! | [getY](https://developer.android.com/reference/kotlin/java/security/interfaces/DSAPublicKey#getY())`()` Returns the value of the public key,`y`. |

| Inherited functions ||
|---|---|
| From class [DSAKey](https://developer.android.com/reference/kotlin/java/security/interfaces/DSAKey) |-------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [DSAParams](https://developer.android.com/reference/kotlin/java/security/interfaces/DSAParams)! | [getParams](https://developer.android.com/reference/kotlin/java/security/interfaces/DSAKey#getParams())`()` <br /> Returns the DSA-specific key parameters. These parameters are never secret. <br /> | ||

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
| [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)! | the value of the public key,`y`. |
