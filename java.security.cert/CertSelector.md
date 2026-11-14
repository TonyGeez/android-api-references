# CertSelector

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CertSelector

```
interface CertSelector : Cloneable
```

| [java.security.cert.CertSelector](https://developer.android.com/reference/kotlin/java/security/cert/CertSelector#) |

| Known Direct Subclasses [X509CertSelector](https://developer.android.com/reference/kotlin/java/security/cert/X509CertSelector) |--------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------| | [X509CertSelector](https://developer.android.com/reference/kotlin/java/security/cert/X509CertSelector) | A`CertSelector`that selects`X509Certificates`that match all specified criteria. | |

A selector that defines a set of criteria for selecting`Certificate`s. Classes that implement this interface are often used to specify which`Certificate`s should be retrieved from a`CertStore`.

**Concurrent Access**

Unless otherwise specified, the methods defined in this interface are not thread-safe. Multiple threads that need to access a single object concurrently should synchronize amongst themselves and provide the necessary locking. Multiple threads each manipulating separate objects need not synchronize.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | [clone](https://developer.android.com/reference/kotlin/java/security/cert/CertSelector#clone())`()` Makes a copy of this`CertSelector`. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [match](https://developer.android.com/reference/kotlin/java/security/cert/CertSelector#match(java.security.cert.Certificate))`(`cert:` ` [Certificate](https://developer.android.com/reference/kotlin/java/security/cert/Certificate)!`)` Decides whether a`Certificate`should be selected. |

## Public methods

### clone

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun clone(): Any
```

Makes a copy of this`CertSelector`. Changes to the copy will not affect the original and vice versa.

| Return ||
|----------------------------------------------------------------------------|------------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | a copy of this`CertSelector` |

| Exceptions ||
|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.CloneNotSupportedException` | if the object's class does not support the`Cloneable`interface. Subclasses that override the`clone`method can also throw this exception to indicate that an instance cannot be cloned. |

### match

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun match(cert: Certificate!): Boolean
```

Decides whether a`Certificate`should be selected.

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------------------------|
| `cert` | [Certificate](https://developer.android.com/reference/kotlin/java/security/cert/Certificate)!:the`Certificate`to be checked |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the`Certificate`should be selected,`false`otherwise |
