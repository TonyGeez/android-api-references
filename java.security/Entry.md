# KeyStore.Entry

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Entry

```
interface Entry
```

| [java.security.KeyStore.Entry](https://developer.android.com/reference/kotlin/java/security/KeyStore.Entry#) |

| Known Direct Subclasses [KeyStore.PrivateKeyEntry](https://developer.android.com/reference/kotlin/java/security/KeyStore.PrivateKeyEntry), [KeyStore.SecretKeyEntry](https://developer.android.com/reference/kotlin/java/security/KeyStore.SecretKeyEntry), [KeyStore.TrustedCertificateEntry](https://developer.android.com/reference/kotlin/java/security/KeyStore.TrustedCertificateEntry), [WrappedKeyEntry](https://developer.android.com/reference/kotlin/android/security/keystore/WrappedKeyEntry.html#) |-----------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------| | [KeyStore.PrivateKeyEntry](https://developer.android.com/reference/kotlin/java/security/KeyStore.PrivateKeyEntry) | A`KeyStore`entry that holds a`PrivateKey`and corresponding certificate chain. | | [KeyStore.SecretKeyEntry](https://developer.android.com/reference/kotlin/java/security/KeyStore.SecretKeyEntry) | A`KeyStore`entry that holds a`SecretKey`. | | [KeyStore.TrustedCertificateEntry](https://developer.android.com/reference/kotlin/java/security/KeyStore.TrustedCertificateEntry) | A`KeyStore`entry that holds a trusted`Certificate`. | | [WrappedKeyEntry](https://developer.android.com/reference/kotlin/android/security/keystore/WrappedKeyEntry.html#) | An [Entry](https://developer.android.com/reference/kotlin/java/security/KeyStore.Entry#) that holds a wrapped key. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

A marker interface for`KeyStore`entry types.

## Summary

| Nested classes ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [Attribute](https://developer.android.com/reference/kotlin/java/security/KeyStore.Entry.Attribute) An attribute associated with a keystore entry. |

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [KeyStore.Entry.Attribute](https://developer.android.com/reference/kotlin/java/security/KeyStore.Entry.Attribute)!\>! | [getAttributes](https://developer.android.com/reference/kotlin/java/security/KeyStore.Entry#getAttributes())`()` Retrieves the attributes associated with an entry. |

## Public methods

### getAttributes

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getAttributes(): MutableSet<KeyStore.Entry.Attribute!>!
```

Retrieves the attributes associated with an entry.

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------|
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [KeyStore.Entry.Attribute](https://developer.android.com/reference/kotlin/java/security/KeyStore.Entry.Attribute)!>! | an unmodifiable`Set`of attributes, possibly empty |
