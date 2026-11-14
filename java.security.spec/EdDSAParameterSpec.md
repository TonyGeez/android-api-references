# EdDSAParameterSpec

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# EdDSAParameterSpec

```
open class EdDSAParameterSpec : AlgorithmParameterSpec
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.security.spec.EdDSAParameterSpec](../java/security/spec/EdDSAParameterSpec.md) |

A class used to specify EdDSA signature and verification parameters. All algorithm modes in [RFC 8032: Edwards-Curve Digital Signature Algorithm (EdDSA)](https://tools.ietf.org/html/rfc8032) can be specified using combinations of the settings in this class.

- If prehash is true, then the mode is Ed25519ph or Ed448ph
- Otherwise, if a context is present, the mode is Ed25519ctx or Ed448
- Otherwise, the mode is Ed25519 or Ed448

<br />

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [EdDSAParameterSpec](../java/security/spec/EdDSAParameterSpec.md))`(`prehash:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Construct an`EdDSAParameterSpec`by specifying whether the prehash mode is used. |
| [EdDSAParameterSpec](../java/security/spec/EdDSAParameterSpec.md))`(`prehash:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `context:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Construct an`EdDSAParameterSpec`by specifying a context and whether the prehash mode is used. |

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Optional](../java/util/Optional.md)\< [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!\>! | [getContext](../java/security/spec/EdDSAParameterSpec.md))`()` Get the context that the signature will use. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isPrehash](../java/security/spec/EdDSAParameterSpec.md))`()` Get whether the prehash mode is specified. |

## Public constructors

### EdDSAParameterSpec

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
EdDSAParameterSpec(prehash: Boolean)
```

Construct an`EdDSAParameterSpec`by specifying whether the prehash mode is used. No context is provided so this constructor specifies a mode in which the context is null. Note that this mode may be different than the mode in which an empty array is used as the context.

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------------|
| `prehash` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):whether the prehash mode is specified. |

### EdDSAParameterSpec

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
EdDSAParameterSpec(
    prehash: Boolean, 
    context: ByteArray!)
```

Construct an`EdDSAParameterSpec`by specifying a context and whether the prehash mode is used. The context may not be null, but it may be an empty array. The mode used when the context is an empty array may not be the same as the mode used when the context is absent.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------|
| `prehash` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):whether the prehash mode is specified. |
| `context` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the context is copied and bound to the signature. |

| Exceptions ||
|-------------------------------------------|----------------------------------------|
| `java.lang.NullPointerException` | if context is null. |
| `java.security.InvalidParameterException` | if context length is greater than 255. |

## Public methods

### getContext

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getContext(): Optional<ByteArray!>!
```

Get the context that the signature will use.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [Optional](../java/util/Optional.md)< [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!>! | `Optional`contains a copy of the context or empty if context is null. |

### isPrehash

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isPrehash(): Boolean
```

Get whether the prehash mode is specified.

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | whether the prehash mode is specified. |
