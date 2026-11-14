# KeyStore.Entry

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Entry

```
interface Entry
```

| [java.security.KeyStore.Entry](../java/security/KeyStore.Entry.md) |

| Known Direct Subclasses [KeyStore.PrivateKeyEntry](../java/security/KeyStore.PrivateKeyEntry.md), [KeyStore.SecretKeyEntry](../java/security/KeyStore.SecretKeyEntry.md), [KeyStore.TrustedCertificateEntry](../java/security/KeyStore.TrustedCertificateEntry.md), [WrappedKeyEntry](../android/security/keystore/WrappedKeyEntry.md) |-----------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------| | [KeyStore.PrivateKeyEntry](../java/security/KeyStore.PrivateKeyEntry.md) | A`KeyStore`entry that holds a`PrivateKey`and corresponding certificate chain. | | [KeyStore.SecretKeyEntry](../java/security/KeyStore.SecretKeyEntry.md) | A`KeyStore`entry that holds a`SecretKey`. | | [KeyStore.TrustedCertificateEntry](../java/security/KeyStore.TrustedCertificateEntry.md) | A`KeyStore`entry that holds a trusted`Certificate`. | | [WrappedKeyEntry](../android/security/keystore/WrappedKeyEntry.md) | An [Entry](../java/security/KeyStore.Entry.md) that holds a wrapped key. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

A marker interface for`KeyStore`entry types.

## Summary

| Nested classes ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [Attribute](../java/security/KeyStore.Entry.Attribute.md) An attribute associated with a keystore entry. |

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [KeyStore.Entry.Attribute](../java/security/KeyStore.Entry.Attribute.md)!\>! | [getAttributes](../java/security/KeyStore.Entry.md))`()` Retrieves the attributes associated with an entry. |

## Public methods

### getAttributes

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getAttributes(): MutableSet<KeyStore.Entry.Attribute!>!
```

Retrieves the attributes associated with an entry.

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------|
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [KeyStore.Entry.Attribute](../java/security/KeyStore.Entry.Attribute.md)!>! | an unmodifiable`Set`of attributes, possibly empty |
