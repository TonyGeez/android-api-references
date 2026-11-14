# KeyFactory

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# KeyFactory

```
open class KeyFactory
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.security.KeyFactory](https://developer.android.com/reference/kotlin/java/security/KeyFactory#) |

Key factories are used to convert*keys* (opaque cryptographic keys of type`Key`) into*key specifications*(transparent representations of the underlying key material), and vice versa.

Key factories are bi-directional. That is, they allow you to build an opaque key object from a given key specification (key material), or to retrieve the underlying key material of a key object in a suitable format.

Multiple compatible key specifications may exist for the same key. For example, a DSA public key may be specified using`DSAPublicKeySpec`or`X509EncodedKeySpec`. A key factory can be used to translate between compatible key specifications.

The following is an example of how to use a key factory in order to instantiate a DSA public key from its encoding. Assume Alice has received a digital signature from Bob. Bob also sent her his public key (in encoded format) to verify his signature. Alice then performs the following actions: 

```kotlin
X509EncodedKeySpec bobPubKeySpec = new X509EncodedKeySpec(bobEncodedPubKey);
  KeyFactory keyFactory = KeyFactory.getInstance("DSA");
  PublicKey bobPubKey = keyFactory.generatePublic(bobPubKeySpec);
  Signature sig = Signature.getInstance("DSA");
  sig.initVerify(bobPubKey);
  sig.update(data);
  sig.verify(signature);
  
```

Android provides the following`KeyFactory`algorithms:

| Algorithm | Supported API Levels |
|-----------|----------------------|
| DH | 1+ |
| DSA | 1+ |
| EC | 11+ |
| --- | --- |
| RSA | 1+ |
| X.509 | 1-8 |
| XDH | 33+ |
| --- | --- |

## Summary

| Protected constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [KeyFactory](https://developer.android.com/reference/kotlin/java/security/KeyFactory#KeyFactory(java.security.KeyFactorySpi,%20java.security.Provider,%20kotlin.String))`(`keyFacSpi:` ` [KeyFactorySpi](https://developer.android.com/reference/kotlin/java/security/KeyFactorySpi)!`, `provider:` ` [Provider](https://developer.android.com/reference/kotlin/java/security/Provider)!`, `algorithm:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Creates a KeyFactory object. |

| Public methods ||
|---------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [PrivateKey](https://developer.android.com/reference/kotlin/java/security/PrivateKey)! | [generatePrivate](https://developer.android.com/reference/kotlin/java/security/KeyFactory#generatePrivate(java.security.spec.KeySpec))`(`keySpec:` ` [KeySpec](https://developer.android.com/reference/kotlin/java/security/spec/KeySpec)!`)` Generates a private key object from the provided key specification (key material). |
| [PublicKey](https://developer.android.com/reference/kotlin/java/security/PublicKey)! | [generatePublic](https://developer.android.com/reference/kotlin/java/security/KeyFactory#generatePublic(java.security.spec.KeySpec))`(`keySpec:` ` [KeySpec](https://developer.android.com/reference/kotlin/java/security/spec/KeySpec)!`)` Generates a public key object from the provided key specification (key material). |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getAlgorithm](https://developer.android.com/reference/kotlin/java/security/KeyFactory#getAlgorithm())`()` Gets the name of the algorithm associated with this`KeyFactory`. |
| --- | --- |
| openstatic [KeyFactory](https://developer.android.com/reference/kotlin/java/security/KeyFactory#)! | [getInstance](https://developer.android.com/reference/kotlin/java/security/KeyFactory#getInstance(kotlin.String))`(`algorithm:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns a KeyFactory object that converts public/private keys of the specified algorithm. |
| openstatic [KeyFactory](https://developer.android.com/reference/kotlin/java/security/KeyFactory#)! | [getInstance](https://developer.android.com/reference/kotlin/java/security/KeyFactory#getInstance(kotlin.String,%20kotlin.String))`(`algorithm:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `provider:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns a KeyFactory object that converts public/private keys of the specified algorithm. |
| openstatic [KeyFactory](https://developer.android.com/reference/kotlin/java/security/KeyFactory#)! | [getInstance](https://developer.android.com/reference/kotlin/java/security/KeyFactory#getInstance(kotlin.String,%20java.security.Provider))`(`algorithm:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `provider:` ` [Provider](https://developer.android.com/reference/kotlin/java/security/Provider)!`)` Returns a KeyFactory object that converts public/private keys of the specified algorithm. |
| --- | --- |
| T | [getKeySpec](https://developer.android.com/reference/kotlin/java/security/KeyFactory#getKeySpec(java.security.Key,%20java.lang.Class))`(`key:` ` [Key](https://developer.android.com/reference/kotlin/java/security/Key)!`, `keySpec:` ` [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)<T>!`)` Returns a specification (key material) of the given key object. |
| [Provider](https://developer.android.com/reference/kotlin/java/security/Provider)! | [getProvider](https://developer.android.com/reference/kotlin/java/security/KeyFactory#getProvider())`()` Returns the provider of this key factory object. |
| [Key](https://developer.android.com/reference/kotlin/java/security/Key)! | [translateKey](https://developer.android.com/reference/kotlin/java/security/KeyFactory#translateKey(java.security.Key))`(`key:` ` [Key](https://developer.android.com/reference/kotlin/java/security/Key)!`)` Translates a key object, whose provider may be unknown or potentially untrusted, into a corresponding key object of this key factory. |
| --- | --- |

## Protected constructors

### KeyFactory

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected KeyFactory(
    keyFacSpi: KeyFactorySpi!, 
    provider: Provider!, 
    algorithm: String!)
```

Creates a KeyFactory object.

| Parameters ||
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| `keyFacSpi` | [KeyFactorySpi](https://developer.android.com/reference/kotlin/java/security/KeyFactorySpi)!:the delegate |
| `provider` | [Provider](https://developer.android.com/reference/kotlin/java/security/Provider)!:the provider |
| `algorithm` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the algorithm to associate with this`KeyFactory` |
| --- | --- |

## Public methods

### generatePrivate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun generatePrivate(keySpec: KeySpec!): PrivateKey!
```

Generates a private key object from the provided key specification (key material).

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------|
| `keySpec` | [KeySpec](https://developer.android.com/reference/kotlin/java/security/spec/KeySpec)!:the specification (key material) of the private key. |

| Return ||
|----------------------------------------------------------------------------------------|------------------|
| [PrivateKey](https://developer.android.com/reference/kotlin/java/security/PrivateKey)! | the private key. |

| Exceptions ||
|----------------------------------------------|------------------------------------------------------------------------------------------------|
| `java.security.spec.InvalidKeySpecException` | if the given key specification is inappropriate for this key factory to produce a private key. |

### generatePublic

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun generatePublic(keySpec: KeySpec!): PublicKey!
```

Generates a public key object from the provided key specification (key material).

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------|
| `keySpec` | [KeySpec](https://developer.android.com/reference/kotlin/java/security/spec/KeySpec)!:the specification (key material) of the public key. |

| Return ||
|--------------------------------------------------------------------------------------|-----------------|
| [PublicKey](https://developer.android.com/reference/kotlin/java/security/PublicKey)! | the public key. |

| Exceptions ||
|----------------------------------------------|-----------------------------------------------------------------------------------------------|
| `java.security.spec.InvalidKeySpecException` | if the given key specification is inappropriate for this key factory to produce a public key. |

### getAlgorithm

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAlgorithm(): String!
```

Gets the name of the algorithm associated with this`KeyFactory`.

| Return ||
|-----------------------------------------------------------------------------------|------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the name of the algorithm associated with this`KeyFactory` |

### getInstance

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getInstance(algorithm: String!): KeyFactory!
```

Returns a KeyFactory object that converts public/private keys of the specified algorithm.

This method traverses the list of registered security Providers, starting with the most preferred Provider. A new KeyFactory object encapsulating the KeyFactorySpi implementation from the first Provider that supports the specified algorithm is returned.

Note that the list of registered providers may be retrieved via the [Security.getProviders()](https://developer.android.com/reference/kotlin/java/security/Security#getProviders())method.

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------------|
| `algorithm` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the requested key algorithm. |

| Return ||
|-----------------------------------------------------------------------------------------|---------------------------|
| [KeyFactory](https://developer.android.com/reference/kotlin/java/security/KeyFactory#)! | the new`KeyFactory`object |

| Exceptions ||
|------------------------------------------|------------------------------------------------------------------------------------|
| `java.security.NoSuchAlgorithmException` | if no`Provider`supports a`KeyFactorySpi`implementation for the specified algorithm |
| `java.lang.NullPointerException` | if`algorithm`is`null`on Android 14 or above |

**See Also**

- [java.security.Provider](https://developer.android.com/reference/kotlin/java/security/Provider) 

### getInstance

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getInstance(
    algorithm: String!, 
    provider: String!
): KeyFactory!
```

Returns a KeyFactory object that converts public/private keys of the specified algorithm.

A new KeyFactory object encapsulating the KeyFactorySpi implementation from the specified provider is returned. The specified provider must be registered in the security provider list.

Note that the list of registered providers may be retrieved via the [Security.getProviders()](https://developer.android.com/reference/kotlin/java/security/Security#getProviders())method.

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------------|
| `algorithm` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the requested key algorithm. |
| `provider` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the provider. |

| Return ||
|-----------------------------------------------------------------------------------------|---------------------------|
| [KeyFactory](https://developer.android.com/reference/kotlin/java/security/KeyFactory#)! | the new`KeyFactory`object |

| Exceptions ||
|------------------------------------------|------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the provider name is`null`or empty |
| `java.security.NoSuchAlgorithmException` | if a`KeyFactorySpi`implementation for the specified algorithm is not available from the specified provider |
| `java.security.NoSuchProviderException` | if the specified provider is not registered in the security provider list |
| --- | --- |
| `java.lang.NullPointerException` | if`algorithm`is`null`on Android 14 or above |

**See Also**

- [java.security.Provider](https://developer.android.com/reference/kotlin/java/security/Provider) 

### getInstance

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getInstance(
    algorithm: String!, 
    provider: Provider!
): KeyFactory!
```

Returns a KeyFactory object that converts public/private keys of the specified algorithm.

A new KeyFactory object encapsulating the KeyFactorySpi implementation from the specified Provider object is returned. Note that the specified Provider object does not have to be registered in the provider list.

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------------|
| `algorithm` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the requested key algorithm. |
| `provider` | [Provider](https://developer.android.com/reference/kotlin/java/security/Provider)!:the provider. |

| Return ||
|-----------------------------------------------------------------------------------------|---------------------------|
| [KeyFactory](https://developer.android.com/reference/kotlin/java/security/KeyFactory#)! | the new`KeyFactory`object |

| Exceptions ||
|------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the specified provider is`null` |
| `java.security.NoSuchAlgorithmException` | if a`KeyFactorySpi`implementation for the specified algorithm is not available from the specified`Provider`object |
| `java.lang.NullPointerException` | if`algorithm`is`null`on Android 14 or above |
| --- | --- |

**See Also**

- [java.security.Provider](https://developer.android.com/reference/kotlin/java/security/Provider) 

### getKeySpec

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun <T : KeySpec!> getKeySpec(
    key: Key!, 
    keySpec: Class<T>!
): T
```

Returns a specification (key material) of the given key object.`keySpec`identifies the specification class in which the key material should be returned. It could, for example, be`DSAPublicKeySpec.class`, to indicate that the key material should be returned in an instance of the`DSAPublicKeySpec`class.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `<T>` | the type of the key specification to be returned |
| `key` | [Key](https://developer.android.com/reference/kotlin/java/security/Key)!:the key. |
| `keySpec` | [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)\<T\>!:the specification class in which the key material should be returned. |
| --- | --- |

| Return ||
|---|------------------------------------------------------------------------------------------------------|
| T | the underlying key specification (key material) in an instance of the requested specification class. |

| Exceptions ||
|----------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.security.spec.InvalidKeySpecException` | if the requested key specification is inappropriate for the given key, or the given key cannot be processed (e.g., the given key has an unrecognized algorithm or format). |

### getProvider

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getProvider(): Provider!
```

Returns the provider of this key factory object.

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------|
| [Provider](https://developer.android.com/reference/kotlin/java/security/Provider)! | the provider of this key factory object |

### translateKey

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun translateKey(key: Key!): Key!
```

Translates a key object, whose provider may be unknown or potentially untrusted, into a corresponding key object of this key factory.

| Parameters ||
|-------|--------------------------------------------------------------------------------------------------------------------------|
| `key` | [Key](https://developer.android.com/reference/kotlin/java/security/Key)!:the key whose provider is unknown or untrusted. |

| Return ||
|--------------------------------------------------------------------------|---------------------|
| [Key](https://developer.android.com/reference/kotlin/java/security/Key)! | the translated key. |

| Exceptions ||
|-------------------------------------|-----------------------------------------------------------|
| `java.security.InvalidKeyException` | if the given key cannot be processed by this key factory. |
