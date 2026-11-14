# CRLSelector

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CRLSelector

```
interface CRLSelector : Cloneable
```

| [java.security.cert.CRLSelector](../java/security/cert/CRLSelector.md) |

| Known Direct Subclasses [X509CRLSelector](../java/security/cert/X509CRLSelector.md) |------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------| | [X509CRLSelector](../java/security/cert/X509CRLSelector.md) | A`CRLSelector`that selects`X509CRLs`that match all specified criteria. | |
| --- | --- | --- | --- | --- | --- | --- |

A selector that defines a set of criteria for selecting`CRL`s. Classes that implement this interface are often used to specify which`CRL`s should be retrieved from a`CertStore`.

**Concurrent Access**

Unless otherwise specified, the methods defined in this interface are not thread-safe. Multiple threads that need to access a single object concurrently should synchronize amongst themselves and provide the necessary locking. Multiple threads each manipulating separate objects need not synchronize.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | [clone](../java/security/cert/CRLSelector.md))`()` Makes a copy of this`CRLSelector`. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [match](../java/security/cert/CRLSelector.md))`(`crl:` ` [CRL](../java/security/cert/CRL.md)!`)` Decides whether a`CRL`should be selected. |

## Public methods

### clone

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun clone(): Any
```

Makes a copy of this`CRLSelector`. Changes to the copy will not affect the original and vice versa.

| Return ||
|----------------------------------------------------------------------------|-----------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | a copy of this`CRLSelector` |

| Exceptions ||
|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.CloneNotSupportedException` | if the object's class does not support the`Cloneable`interface. Subclasses that override the`clone`method can also throw this exception to indicate that an instance cannot be cloned. |

### match

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun match(crl: CRL!): Boolean
```

Decides whether a`CRL`should be selected.

| Parameters ||
|-------|-----------------------------------------------------------------------------------------------------|
| `crl` | [CRL](../java/security/cert/CRL.md)!:the`CRL`to be checked |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the`CRL`should be selected,`false`otherwise |
