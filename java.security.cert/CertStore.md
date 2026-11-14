# CertStore

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CertStore

```
open class CertStore
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.security.cert.CertStore](../java/security/cert/CertStore.md) |

A class for retrieving`Certificate`s and`CRL`s from a repository.

This class uses a provider-based architecture. To create a`CertStore`, call one of the static`getInstance`methods, passing in the type of`CertStore`desired, any applicable initialization parameters and optionally the name of the provider desired.

Once the`CertStore`has been created, it can be used to retrieve`Certificate`s and`CRL`s by calling its [getCertificates](../java/security/cert/CertStore.md))and [getCRLs](../java/security/cert/CertStore.md))methods.

Unlike a [KeyStore](../java/security/KeyStore.md), which provides access to a cache of private keys and trusted certificates, a`CertStore`is designed to provide access to a potentially vast repository of untrusted certificates and CRLs. For example, an LDAP implementation of`CertStore`provides access to certificates and CRLs stored in one or more directories using the LDAP protocol and the schema as defined in the RFC service attribute.

Every implementation of the Java platform is required to support the following standard`CertStore`type:

- `Collection`

This type is described in the [CertStore section](https://docs.oracle.com/en/java/javase/17/docs/specs/security/standard-names.html#certstore-types) of the Java Security Standard Algorithm Names Specification. Consult the release documentation for your implementation to see if any other types are supported.

**Concurrent Access**

All public methods of`CertStore`objects must be thread-safe. That is, multiple threads may concurrently invoke these methods on a single`CertStore`object (or more than one) with no ill effects. This allows a`CertPathBuilder`to search for a CRL while simultaneously searching for further certificates, for instance.

The static methods of this class are also guaranteed to be thread-safe. Multiple threads may concurrently invoke the static methods defined in this class with no ill effects.

## Summary

| Protected constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [CertStore](../java/security/cert/CertStore.md))`(`storeSpi:` ` [CertStoreSpi](../java/security/cert/CertStoreSpi.md)!`, `provider:` ` [Provider](../java/security/Provider.md)!`, `type:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `params:` ` [CertStoreParameters](../java/security/cert/CertStoreParameters.md)!`)` Creates a`CertStore`object of the given type, and encapsulates the given provider implementation (SPI object) in it. |

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\<out [CRL](../java/security/cert/CRL.md)!\>! | [getCRLs](../java/security/cert/CertStore.md))`(`selector:` ` [CRLSelector](../java/security/cert/CRLSelector.md)!`)` Returns a`Collection`of`CRL`s that match the specified selector. |
| [CertStoreParameters](../java/security/cert/CertStoreParameters.md)! | [getCertStoreParameters](../java/security/cert/CertStore.md))`()` Returns the parameters used to initialize this`CertStore`. |
| [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\<out [Certificate](../java/security/cert/Certificate.md)!\>! | [getCertificates](../java/security/cert/CertStore.md))`(`selector:` ` [CertSelector](../java/security/cert/CertSelector.md)!`)` Returns a`Collection`of`Certificate`s that match the specified selector. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getDefaultType](../java/security/cert/CertStore.md))`()` Returns the default`CertStore`type as specified by the`certstore.type`security property, or the string "LDAP" if no such property exists. |
| openstatic [CertStore](../java/security/cert/CertStore.md)! | [getInstance](../java/security/cert/CertStore.md))`(`type:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `params:` ` [CertStoreParameters](../java/security/cert/CertStoreParameters.md)!`)` Returns a`CertStore`object that implements the specified`CertStore`type and is initialized with the specified parameters. |
| openstatic [CertStore](../java/security/cert/CertStore.md)! | [getInstance](../java/security/cert/CertStore.md))`(`type:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `params:` ` [CertStoreParameters](../java/security/cert/CertStoreParameters.md)!`, `provider:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns a`CertStore`object that implements the specified`CertStore`type. |
| --- | --- |
| openstatic [CertStore](../java/security/cert/CertStore.md)! | [getInstance](../java/security/cert/CertStore.md))`(`type:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `params:` ` [CertStoreParameters](../java/security/cert/CertStoreParameters.md)!`, `provider:` ` [Provider](../java/security/Provider.md)!`)` Returns a`CertStore`object that implements the specified`CertStore`type. |
| [Provider](../java/security/Provider.md)! | [getProvider](../java/security/cert/CertStore.md))`()` Returns the provider of this`CertStore`. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getType](../java/security/cert/CertStore.md))`()` Returns the type of this`CertStore`. |
| --- | --- |

## Protected constructors

### CertStore

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected CertStore(
    storeSpi: CertStoreSpi!, 
    provider: Provider!, 
    type: String!, 
    params: CertStoreParameters!)
```

Creates a`CertStore`object of the given type, and encapsulates the given provider implementation (SPI object) in it.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `storeSpi` | [CertStoreSpi](../java/security/cert/CertStoreSpi.md)!:the provider implementation |
| `provider` | [Provider](../java/security/Provider.md)!:the provider |
| `type` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the type |
| --- | --- |
| `params` | [CertStoreParameters](../java/security/cert/CertStoreParameters.md)!:the initialization parameters (may be`null`) |

## Public methods

### getCRLs

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCRLs(selector: CRLSelector!): MutableCollection<out CRL!>!
```

Returns a`Collection`of`CRL`s that match the specified selector. If no`CRL`s match the selector, an empty`Collection`will be returned.

For some`CertStore`types, the resulting`Collection`may not contain**all** of the`CRL`s that match the selector. For instance, an LDAP`CertStore`may not search all entries in the directory. Instead, it may just search entries that are likely to contain the`CRL`s it is looking for.

Some`CertStore`implementations (especially LDAP`CertStore`s) may throw a`CertStoreException`unless a non-null`CRLSelector`is provided that includes specific criteria that can be used to find the CRLs. Issuer names and/or the certificate to be checked are especially useful.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `selector` | [CRLSelector](../java/security/cert/CRLSelector.md)!:A`CRLSelector`used to select which`CRL`s should be returned. Specify`null`to return all`CRL`s (if supported). |

| Return ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)<out` ` [CRL](../java/security/cert/CRL.md)!>! | A`Collection`of`CRL`s that match the specified selector (never`null`) |

| Exceptions ||
|-----------------------------------------|------------------------|
| `java.security.cert.CertStoreException` | if an exception occurs |

### getCertStoreParameters

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCertStoreParameters(): CertStoreParameters!
```

Returns the parameters used to initialize this`CertStore`. Note that the`CertStoreParameters`object is cloned before it is returned.

| Return ||
|---------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| [CertStoreParameters](../java/security/cert/CertStoreParameters.md)! | the parameters used to initialize this`CertStore`(may be`null`) |

### getCertificates

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCertificates(selector: CertSelector!): MutableCollection<out Certificate!>!
```

Returns a`Collection`of`Certificate`s that match the specified selector. If no`Certificate`s match the selector, an empty`Collection`will be returned.

For some`CertStore`types, the resulting`Collection`may not contain**all** of the`Certificate`s that match the selector. For instance, an LDAP`CertStore`may not search all entries in the directory. Instead, it may just search entries that are likely to contain the`Certificate`s it is looking for.

Some`CertStore`implementations (especially LDAP`CertStore`s) may throw a`CertStoreException`unless a non-null`CertSelector`is provided that includes specific criteria that can be used to find the certificates. Issuer and/or subject names are especially useful criteria.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `selector` | [CertSelector](../java/security/cert/CertSelector.md)!:A`CertSelector`used to select which`Certificate`s should be returned. Specify`null`to return all`Certificate`s (if supported). |

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)<out` ` [Certificate](../java/security/cert/Certificate.md)!>! | A`Collection`of`Certificate`s that match the specified selector (never`null`) |

| Exceptions ||
|-----------------------------------------|------------------------|
| `java.security.cert.CertStoreException` | if an exception occurs |

### getDefaultType

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getDefaultType(): String!
```

Returns the default`CertStore`type as specified by the`certstore.type`security property, or the string "LDAP" if no such property exists.

The default`CertStore`type can be used by applications that do not want to use a hard-coded type when calling one of the`getInstance`methods, and want to provide a default`CertStore`type in case a user does not specify its own.

The default`CertStore`type can be changed by setting the value of the`certstore.type`security property to the desired type.

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the default`CertStore`type as specified by the`certstore.type`security property, or the string "LDAP" if no such property exists. |

**See Also**

- [java.security.Security](../java/security/Security.md) 

### getInstance

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getInstance(
    type: String!, 
    params: CertStoreParameters!
): CertStore!
```

Returns a`CertStore`object that implements the specified`CertStore`type and is initialized with the specified parameters.

This method traverses the list of registered security Providers, starting with the most preferred Provider. A new CertStore object encapsulating the CertStoreSpi implementation from the first Provider that supports the specified type is returned.

Note that the list of registered providers may be retrieved via the [Security.getProviders()](../java/security/Security.md))method.

The`CertStore`that is returned is initialized with the specified`CertStoreParameters`. The type of parameters needed may vary between different types of`CertStore`s. Note that the specified`CertStoreParameters`object is cloned.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `type` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the requested`CertStore`type. See the CertStore section in the [Java Security Standard Algorithm Names Specification](https://docs.oracle.com/en/java/javase/17/docs/specs/security/standard-names.html#certstore-types) for information about standard types. |
| `params` | [CertStoreParameters](../java/security/cert/CertStoreParameters.md)!:the initialization parameters (may be`null`). |

| Return ||
|--------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| [CertStore](../java/security/cert/CertStore.md)! | a`CertStore`object that implements the specified`CertStore`type |

| Exceptions ||
|----------------------------------------------------|----------------------------------------------------------------------------------|
| `java.security.InvalidAlgorithmParameterException` | if the specified initialization parameters are inappropriate for this`CertStore` |
| `java.security.NoSuchAlgorithmException` | if no`Provider`supports a`CertStoreSpi`implementation for the specified type |
| `java.lang.NullPointerException` | if`type`is`null` |
| --- | --- |

**See Also**

- [java.security.Provider](../java/security/Provider.md) 

### getInstance

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getInstance(
    type: String!, 
    params: CertStoreParameters!, 
    provider: String!
): CertStore!
```

Returns a`CertStore`object that implements the specified`CertStore`type.

A new CertStore object encapsulating the CertStoreSpi implementation from the specified provider is returned. The specified provider must be registered in the security provider list.

Note that the list of registered providers may be retrieved via the [Security.getProviders()](../java/security/Security.md))method.

The`CertStore`that is returned is initialized with the specified`CertStoreParameters`. The type of parameters needed may vary between different types of`CertStore`s. Note that the specified`CertStoreParameters`object is cloned.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `type` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the requested`CertStore`type. See the CertStore section in the [Java Security Standard Algorithm Names Specification](https://docs.oracle.com/en/java/javase/17/docs/specs/security/standard-names.html#certstore-types) for information about standard types. |
| `params` | [CertStoreParameters](../java/security/cert/CertStoreParameters.md)!:the initialization parameters (may be`null`). |
| `provider` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the provider. |
| --- | --- |

| Return ||
|--------------------------------------------------------------------------------------------|-------------------------------------------------------|
| [CertStore](../java/security/cert/CertStore.md)! | a`CertStore`object that implements the specified type |

| Exceptions ||
|----------------------------------------------------|------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the`provider`is`null`or empty |
| `java.security.InvalidAlgorithmParameterException` | if the specified initialization parameters are inappropriate for this`CertStore` |
| `java.security.NoSuchAlgorithmException` | if a`CertStoreSpi`implementation for the specified type is not available from the specified provider |
| --- | --- |
| `java.security.NoSuchProviderException` | if the specified provider is not registered in the security provider list |
| `java.lang.NullPointerException` | if`type`is`null` |

**See Also**

- [java.security.Provider](../java/security/Provider.md) 

### getInstance

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getInstance(
    type: String!, 
    params: CertStoreParameters!, 
    provider: Provider!
): CertStore!
```

Returns a`CertStore`object that implements the specified`CertStore`type.

A new CertStore object encapsulating the CertStoreSpi implementation from the specified Provider object is returned. Note that the specified Provider object does not have to be registered in the provider list.

The`CertStore`that is returned is initialized with the specified`CertStoreParameters`. The type of parameters needed may vary between different types of`CertStore`s. Note that the specified`CertStoreParameters`object is cloned.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `type` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the requested`CertStore`type. See the CertStore section in the [Java Security Standard Algorithm Names Specification](https://docs.oracle.com/en/java/javase/17/docs/specs/security/standard-names.html#certstore-types) for information about standard types. |
| `params` | [CertStoreParameters](../java/security/cert/CertStoreParameters.md)!:the initialization parameters (may be`null`). |
| `provider` | [Provider](../java/security/Provider.md)!:the provider. |
| --- | --- |

| Return ||
|--------------------------------------------------------------------------------------------|-------------------------------------------------------|
| [CertStore](../java/security/cert/CertStore.md)! | a`CertStore`object that implements the specified type |

| Exceptions ||
|----------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the`provider`is null |
| `java.security.InvalidAlgorithmParameterException` | if the specified initialization parameters are inappropriate for this`CertStore` |
| `java.security.NoSuchAlgorithmException` | if a`CertStoreSpi`implementation for the specified type is not available from the specified Provider object |
| --- | --- |
| `java.lang.NullPointerException` | if`type`is`null` |

**See Also**

- [java.security.Provider](../java/security/Provider.md) 

### getProvider

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getProvider(): Provider!
```

Returns the provider of this`CertStore`.

| Return ||
|------------------------------------------------------------------------------------------|---------------------------------|
| [Provider](../java/security/Provider.md)! | the provider of this`CertStore` |

### getType

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getType(): String!
```

Returns the type of this`CertStore`.

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the type of this`CertStore` |
