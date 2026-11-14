# DSAPrivateKey

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DSAPrivateKey

```
interface DSAPrivateKey : DSAKey, PrivateKey
```

| [java.security.interfaces.DSAPrivateKey](DSAPrivateKey.md) |

The standard interface to a DSA private key. DSA (Digital Signature Algorithm) is defined in NIST's FIPS-186.

## Summary

| Constants ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [serialVersionUID](DSAPrivateKey.md) The class fingerprint that is set to indicate serialization compatibility with a previous version of the class. |

| Public methods ||
|--------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [BigInteger](../java.math/BigInteger.md)! | [getX](DSAPrivateKey.md))`()` Returns the value of the private key,`x`. |

| Inherited functions ||
|---|---|
| From class [DSAKey](DSAKey.md) |-------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [DSAParams](DSAParams.md)! | [getParams](DSAKey.md))`()` <br /> Returns the DSA-specific key parameters. These parameters are never secret. <br /> | ||

## Constants

### serialVersionUID

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val serialVersionUID: Long
```

**Deprecated:** *A`serialVersionUID`field in an interface is ineffectual. Do not use; no replacement.*

The class fingerprint that is set to indicate serialization compatibility with a previous version of the class. 

 Value: 7776497482533790279L

## Public methods

### getX

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getX(): BigInteger!
```

Returns the value of the private key,`x`.

| Return ||
|------------------------------------------------------------------------------------------|-----------------------------------|
| [BigInteger](../java.math/BigInteger.md)! | the value of the private key,`x`. |
