# CollectionCertStoreParameters

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CollectionCertStoreParameters

```
open class CollectionCertStoreParameters : CertStoreParameters
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.security.cert.CollectionCertStoreParameters](https://developer.android.com/reference/kotlin/java/security/cert/CollectionCertStoreParameters#) |

Parameters used as input for the Collection `CertStore` algorithm.

This class is used to provide necessary configuration parameters to implementations of the Collection `CertStore` algorithm. The only parameter included in this class is the `Collection` from which the `CertStore` will retrieve certificates and CRLs.

**Concurrent Access**

Unless otherwise specified, the methods defined in this class are not thread-safe. Multiple threads that need to access a single object concurrently should synchronize amongst themselves and provide the necessary locking. Multiple threads each manipulating separate objects need not synchronize.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [CollectionCertStoreParameters](https://developer.android.com/reference/kotlin/java/security/cert/CollectionCertStoreParameters#CollectionCertStoreParameters())`()` Creates an instance of `CollectionCertStoreParameters` with the default parameter values (an empty and immutable `Collection`). |
| [CollectionCertStoreParameters](https://developer.android.com/reference/kotlin/java/security/cert/CollectionCertStoreParameters#CollectionCertStoreParameters(kotlin.collections.MutableCollection))`(`collection:` ` [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)<*>!`)` Creates an instance of `CollectionCertStoreParameters` which will allow certificates and CRLs to be retrieved from the specified `Collection`. |

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | [clone](https://developer.android.com/reference/kotlin/java/security/cert/CollectionCertStoreParameters#clone())`()` Returns a copy of this object. |
| open [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\<\*\>! | [getCollection](https://developer.android.com/reference/kotlin/java/security/cert/CollectionCertStoreParameters#getCollection())`()` Returns the `Collection` from which `Certificate`s and `CRL`s are retrieved. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/java/security/cert/CollectionCertStoreParameters#toString())`()` Returns a formatted string describing the parameters. |
| --- | --- |

## Public constructors

### CollectionCertStoreParameters

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
CollectionCertStoreParameters()
```

Creates an instance of `CollectionCertStoreParameters` with the default parameter values (an empty and immutable `Collection`). 

### CollectionCertStoreParameters

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
CollectionCertStoreParameters(collection: MutableCollection<*>!)
```

Creates an instance of `CollectionCertStoreParameters` which will allow certificates and CRLs to be retrieved from the specified `Collection`. If the specified `Collection` contains an object that is not a `Certificate` or `CRL`, that object will be ignored by the Collection `CertStore`.

The `Collection` is **not** copied. Instead, a reference is used. This allows the caller to subsequently add or remove `Certificates` or `CRL`s from the `Collection`, thus changing the set of `Certificates` or `CRL`s available to the Collection `CertStore`. The Collection `CertStore` will not modify the contents of the `Collection`.

If the `Collection` will be modified by one thread while another thread is calling a method of a Collection `CertStore` that has been initialized with this `Collection`, the `Collection` must have fail-fast iterators.

| Parameters ||
|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `collection` | [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\<\*\>!: a `Collection` of `Certificate`s and `CRL`s |

| Exceptions ||
|----------------------------------|---------------------------|
| `java.lang.NullPointerException` | if `collection` is `null` |

## Public methods

### clone

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun clone(): Any
```

Returns a copy of this object. Note that only a reference to the `Collection` is copied, and not the contents.

| Return ||
|----------------------------------------------------------------------------|----------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | the copy |

| Exceptions ||
|----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.CloneNotSupportedException` | if the object's class does not support the `Cloneable` interface. Subclasses that override the `clone` method can also throw this exception to indicate that an instance cannot be cloned. |

### getCollection

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getCollection(): MutableCollection<*>!
```

Returns the `Collection` from which `Certificate`s and `CRL`s are retrieved. This is **not** a copy of the `Collection`, it is a reference. This allows the caller to subsequently add or remove `Certificates` or `CRL`s from the `Collection`.

| Return ||
|-------------------------------------------------------------------------------------------------------------------------|-------------------------------|
| [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)<*>! | the `Collection` (never null) |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

Returns a formatted string describing the parameters.

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a formatted string describing the parameters |
