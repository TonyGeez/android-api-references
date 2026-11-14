# CertStoreSpi

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CertStoreSpi

```
abstract class CertStoreSpi
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.security.cert.CertStoreSpi](CertStoreSpi.md) |

The*Service Provider Interface* (**SPI** ) for the [CertStore](CertStore.md) class. All`CertStore`implementations must include a class (the SPI class) that extends this class (`CertStoreSpi`), provides a constructor with a single argument of type`CertStoreParameters`, and implements all of its methods. In general, instances of this class should only be accessed through the`CertStore`class. For details, see the Java Cryptography Architecture.

**Concurrent Access**

The public methods of all`CertStoreSpi`objects must be thread-safe. That is, multiple threads may concurrently invoke these methods on a single`CertStoreSpi`object (or more than one) with no ill effects. This allows a`CertPathBuilder`to search for a CRL while simultaneously searching for further certificates, for instance.

Simple`CertStoreSpi`implementations will probably ensure thread safety by adding a`synchronized`keyword to their`engineGetCertificates`and`engineGetCRLs`methods. More sophisticated ones may allow truly concurrent access.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [CertStoreSpi](CertStoreSpi.md))`(`params:` ` [CertStoreParameters](CertStoreParameters.md)!`)` The sole constructor. |

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\<out [CRL](CRL.md)!\>! | [engineGetCRLs](CertStoreSpi.md))`(`selector:` ` [CRLSelector](CRLSelector.md)!`)` Returns a`Collection`of`CRL`s that match the specified selector. |
| abstract [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\<out [Certificate](Certificate.md)!\>! | [engineGetCertificates](CertStoreSpi.md))`(`selector:` ` [CertSelector](CertSelector.md)!`)` Returns a`Collection`of`Certificate`s that match the specified selector. |

## Public constructors

### CertStoreSpi

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
CertStoreSpi(params: CertStoreParameters!)
```

The sole constructor.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `params` | [CertStoreParameters](CertStoreParameters.md)!:the initialization parameters (may be`null`) |

| Exceptions ||
|----------------------------------------------------|---------------------------------------------------------------------------|
| `java.security.InvalidAlgorithmParameterException` | if the initialization parameters are inappropriate for this`CertStoreSpi` |

## Public methods

### engineGetCRLs

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun engineGetCRLs(selector: CRLSelector!): MutableCollection<out CRL!>!
```

Returns a`Collection`of`CRL`s that match the specified selector. If no`CRL`s match the selector, an empty`Collection`will be returned.

For some`CertStore`types, the resulting`Collection`may not contain**all** of the`CRL`s that match the selector. For instance, an LDAP`CertStore`may not search all entries in the directory. Instead, it may just search entries that are likely to contain the`CRL`s it is looking for.

Some`CertStore`implementations (especially LDAP`CertStore`s) may throw a`CertStoreException`unless a non-null`CRLSelector`is provided that includes specific criteria that can be used to find the CRLs. Issuer names and/or the certificate to be checked are especially useful.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `selector` | [CRLSelector](CRLSelector.md)!:A`CRLSelector`used to select which`CRL`s should be returned. Specify`null`to return all`CRL`s (if supported). |

| Return ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)<out` ` [CRL](CRL.md)!>! | A`Collection`of`CRL`s that match the specified selector (never`null`) |

| Exceptions ||
|-----------------------------------------|------------------------|
| `java.security.cert.CertStoreException` | if an exception occurs |

### engineGetCertificates

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun engineGetCertificates(selector: CertSelector!): MutableCollection<out Certificate!>!
```

Returns a`Collection`of`Certificate`s that match the specified selector. If no`Certificate`s match the selector, an empty`Collection`will be returned.

For some`CertStore`types, the resulting`Collection`may not contain**all** of the`Certificate`s that match the selector. For instance, an LDAP`CertStore`may not search all entries in the directory. Instead, it may just search entries that are likely to contain the`Certificate`s it is looking for.

Some`CertStore`implementations (especially LDAP`CertStore`s) may throw a`CertStoreException`unless a non-null`CertSelector`is provided that includes specific criteria that can be used to find the certificates. Issuer and/or subject names are especially useful criteria.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `selector` | [CertSelector](CertSelector.md)!:A`CertSelector`used to select which`Certificate`s should be returned. Specify`null`to return all`Certificate`s (if supported). |

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)<out` ` [Certificate](Certificate.md)!>! | A`Collection`of`Certificate`s that match the specified selector (never`null`) |

| Exceptions ||
|-----------------------------------------|------------------------|
| `java.security.cert.CertStoreException` | if an exception occurs |
