# EdECPrivateKeySpec

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# EdECPrivateKeySpec

```
class EdECPrivateKeySpec : KeySpec
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.security.spec.EdECPrivateKeySpec](https://developer.android.com/reference/kotlin/java/security/spec/EdECPrivateKeySpec#) |

A class representing elliptic curve private keys as defined in [RFC 8032: Edwards-Curve Digital Signature Algorithm (EdDSA)](https://tools.ietf.org/html/rfc8032), including the curve and other algorithm parameters. The private key is a bit string represented using a byte array. This class only supports bit string lengths that are a multiple of 8.

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [EdECPrivateKeySpec](https://developer.android.com/reference/kotlin/java/security/spec/EdECPrivateKeySpec#EdECPrivateKeySpec(java.security.spec.NamedParameterSpec,%20kotlin.ByteArray))`(`params:` ` [NamedParameterSpec](https://developer.android.com/reference/kotlin/java/security/spec/NamedParameterSpec)`, `bytes:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)`)` Construct a private key spec using the supplied parameters and bit string. |

| Public methods ||
|------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html) | [getBytes](https://developer.android.com/reference/kotlin/java/security/spec/EdECPrivateKeySpec#getBytes())`()` Get the byte array representing the private key. |
| [NamedParameterSpec](https://developer.android.com/reference/kotlin/java/security/spec/NamedParameterSpec) | [getParams](https://developer.android.com/reference/kotlin/java/security/spec/EdECPrivateKeySpec#getParams())`()` Get the algorithm parameters that define the curve and other settings. |

## Public constructors

### EdECPrivateKeySpec

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
EdECPrivateKeySpec(
    params: NamedParameterSpec, 
    bytes: ByteArray)
```

Construct a private key spec using the supplied parameters and bit string.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `params` | [NamedParameterSpec](https://developer.android.com/reference/kotlin/java/security/spec/NamedParameterSpec):the algorithm parameters. |
| `bytes` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html):the key as a byte array. This array is copied to protect against subsequent modification. |

| Exceptions ||
|----------------------------------|-----------------------------|
| `java.lang.NullPointerException` | if`params`or`bytes`is null. |

## Public methods

### getBytes

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getBytes(): ByteArray
```

Get the byte array representing the private key. A new copy of the array is returned each time this method is called.

| Return ||
|-----------------------------------------------------------------------------------------|----------------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html) | the private key as a byte array. |

### getParams

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getParams(): NamedParameterSpec
```

Get the algorithm parameters that define the curve and other settings.

| Return ||
|------------------------------------------------------------------------------------------------------------|---------------------------|
| [NamedParameterSpec](https://developer.android.com/reference/kotlin/java/security/spec/NamedParameterSpec) | the algorithm parameters. |
