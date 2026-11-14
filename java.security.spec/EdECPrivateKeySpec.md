# EdECPrivateKeySpec

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# EdECPrivateKeySpec

```
class EdECPrivateKeySpec : KeySpec
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.security.spec.EdECPrivateKeySpec](../java/security/spec/EdECPrivateKeySpec.md) |

A class representing elliptic curve private keys as defined in [RFC 8032: Edwards-Curve Digital Signature Algorithm (EdDSA)](https://tools.ietf.org/html/rfc8032), including the curve and other algorithm parameters. The private key is a bit string represented using a byte array. This class only supports bit string lengths that are a multiple of 8.

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [EdECPrivateKeySpec](../java/security/spec/EdECPrivateKeySpec.md))`(`params:` ` [NamedParameterSpec](../java/security/spec/NamedParameterSpec.md)`, `bytes:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)`)` Construct a private key spec using the supplied parameters and bit string. |

| Public methods ||
|------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html) | [getBytes](../java/security/spec/EdECPrivateKeySpec.md))`()` Get the byte array representing the private key. |
| [NamedParameterSpec](../java/security/spec/NamedParameterSpec.md) | [getParams](../java/security/spec/EdECPrivateKeySpec.md))`()` Get the algorithm parameters that define the curve and other settings. |

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
| `params` | [NamedParameterSpec](../java/security/spec/NamedParameterSpec.md):the algorithm parameters. |
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
| [NamedParameterSpec](../java/security/spec/NamedParameterSpec.md) | the algorithm parameters. |
