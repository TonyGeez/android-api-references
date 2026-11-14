# XECPrivateKeySpec

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# XECPrivateKeySpec

```
open class XECPrivateKeySpec : KeySpec
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.security.spec.XECPrivateKeySpec](../java/security/spec/XECPrivateKeySpec.md) |

A class representing elliptic curve private keys as defined in RFC 7748, including the curve and other algorithm parameters. The private key is represented as an encoded scalar value. The decoding procedure defined in the RFC includes an operation that forces certain bits of the key to either 1 or 0. This operation is known as "pruning" or "clamping" the private key. All arrays in this spec are unpruned, and implementations will need to prune the array before using it in any numerical operations.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [XECPrivateKeySpec](../java/security/spec/XECPrivateKeySpec.md))`(`params:` ` [AlgorithmParameterSpec](../java/security/spec/AlgorithmParameterSpec.md)!`, `scalar:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Construct a private key spec using the supplied parameters and encoded scalar value. |

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [AlgorithmParameterSpec](../java/security/spec/AlgorithmParameterSpec.md)! | [getParams](../java/security/spec/XECPrivateKeySpec.md))`()` Get the algorithm parameters that define the curve and other settings. |
| open [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [getScalar](../java/security/spec/XECPrivateKeySpec.md))`()` Get the scalar value encoded as an unpruned byte array. |

## Public constructors

### XECPrivateKeySpec

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
XECPrivateKeySpec(
    params: AlgorithmParameterSpec!, 
    scalar: ByteArray!)
```

Construct a private key spec using the supplied parameters and encoded scalar value.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `params` | [AlgorithmParameterSpec](../java/security/spec/AlgorithmParameterSpec.md)!:the algorithm parameters |
| `scalar` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the unpruned encoded scalar value. This array is copied to protect against subsequent modification. |

| Exceptions ||
|----------------------------------|------------------------------|
| `java.lang.NullPointerException` | if`params`or`scalar`is null. |

## Public methods

### getParams

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getParams(): AlgorithmParameterSpec!
```

Get the algorithm parameters that define the curve and other settings.

| Return ||
|---------------------------------------------------------------------------------------------------------------------|--------------------------|
| [AlgorithmParameterSpec](../java/security/spec/AlgorithmParameterSpec.md)! | the algorithm parameters |

### getScalar

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getScalar(): ByteArray!
```

Get the scalar value encoded as an unpruned byte array. A new copy of the array is returned each time this method is called.

| Return ||
|------------------------------------------------------------------------------------------|-----------------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | the unpruned encoded scalar value |
