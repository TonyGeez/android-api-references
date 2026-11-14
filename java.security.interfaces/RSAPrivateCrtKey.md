# RSAPrivateCrtKey

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RSAPrivateCrtKey

```
interface RSAPrivateCrtKey : RSAPrivateKey
```

| [java.security.interfaces.RSAPrivateCrtKey](RSAPrivateCrtKey.md) |

The interface to an RSA private key, as defined in the [PKCS#1 v2.2](https://tools.ietf.org/rfc/rfc8017.txt) standard, using the*Chinese Remainder Theorem*(CRT) information values.

## Summary

| Constants ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [serialVersionUID](RSAPrivateCrtKey.md) The type fingerprint that is set to indicate serialization compatibility with a previous version of the type. |

| Public methods ||
|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [BigInteger](../java.math/BigInteger.md)! | [getCrtCoefficient](RSAPrivateCrtKey.md))`()` Returns the crtCoefficient. |
| abstract [BigInteger](../java.math/BigInteger.md)! | [getPrimeExponentP](RSAPrivateCrtKey.md))`()` Returns the primeExponentP. |
| abstract [BigInteger](../java.math/BigInteger.md)! | [getPrimeExponentQ](RSAPrivateCrtKey.md))`()` Returns the primeExponentQ. |
| --- | --- |
| abstract [BigInteger](../java.math/BigInteger.md)! | [getPrimeP](RSAPrivateCrtKey.md))`()` Returns the primeP. |
| abstract [BigInteger](../java.math/BigInteger.md)! | [getPrimeQ](RSAPrivateCrtKey.md))`()` Returns the primeQ. |
| abstract [BigInteger](../java.math/BigInteger.md)! | [getPublicExponent](RSAPrivateCrtKey.md))`()` Returns the public exponent. |
| --- | --- |

| Inherited functions ||
|---|---|
| From class [RSAKey](RSAKey.md) |---------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [BigInteger](../java.math/BigInteger.md)! | [getModulus](RSAKey.md))`()` <br /> Returns the modulus. <br /> | | [AlgorithmParameterSpec](../java.security.spec/AlgorithmParameterSpec.md)! | [getParams](RSAKey.md))`()` <br /> Returns the parameters associated with this key. The parameters are optional and may be either explicitly specified or implicitly created during key pair generation. <br /> | ||
| From class [RSAPrivateKey](RSAPrivateKey.md) |------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [BigInteger](../java.math/BigInteger.md)! | [getPrivateExponent](RSAPrivateKey.md))`()` <br /> Returns the private exponent. <br /> | ||

## Constants

### serialVersionUID

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val serialVersionUID: Long
```

**Deprecated:** *A`serialVersionUID`field in an interface is ineffectual. Do not use; no replacement.*

The type fingerprint that is set to indicate serialization compatibility with a previous version of the type. 

 Value: -5682214253527700368L

## Public methods

### getCrtCoefficient

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getCrtCoefficient(): BigInteger!
```

Returns the crtCoefficient.

| Return ||
|------------------------------------------------------------------------------------------|--------------------|
| [BigInteger](../java.math/BigInteger.md)! | the crtCoefficient |

### getPrimeExponentP

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getPrimeExponentP(): BigInteger!
```

Returns the primeExponentP.

| Return ||
|------------------------------------------------------------------------------------------|--------------------|
| [BigInteger](../java.math/BigInteger.md)! | the primeExponentP |

### getPrimeExponentQ

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getPrimeExponentQ(): BigInteger!
```

Returns the primeExponentQ.

| Return ||
|------------------------------------------------------------------------------------------|--------------------|
| [BigInteger](../java.math/BigInteger.md)! | the primeExponentQ |

### getPrimeP

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getPrimeP(): BigInteger!
```

Returns the primeP.

| Return ||
|------------------------------------------------------------------------------------------|------------|
| [BigInteger](../java.math/BigInteger.md)! | the primeP |

### getPrimeQ

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getPrimeQ(): BigInteger!
```

Returns the primeQ.

| Return ||
|------------------------------------------------------------------------------------------|------------|
| [BigInteger](../java.math/BigInteger.md)! | the primeQ |

### getPublicExponent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getPublicExponent(): BigInteger!
```

Returns the public exponent.

| Return ||
|------------------------------------------------------------------------------------------|---------------------|
| [BigInteger](../java.math/BigInteger.md)! | the public exponent |
