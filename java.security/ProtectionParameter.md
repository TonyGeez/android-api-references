# KeyStore.ProtectionParameter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ProtectionParameter

```
interface ProtectionParameter
```

| [java.security.KeyStore.ProtectionParameter](../java/security/KeyStore.ProtectionParameter.md) |

| Known Direct Subclasses [KeyProtection](../android/security/keystore/KeyProtection.md), [KeyStore.CallbackHandlerProtection](../java/security/KeyStore.CallbackHandlerProtection.md), [KeyStore.PasswordProtection](../java/security/KeyStore.PasswordProtection.md), [KeyStoreParameter](../android/security/KeyStoreParameter.md) |---------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [KeyProtection](../android/security/keystore/KeyProtection.md) | Specification of how a key or key pair is secured when imported into the [Android Keystore system](https://developer.android.com/training/articles/keystore.html). | | [KeyStore.CallbackHandlerProtection](../java/security/KeyStore.CallbackHandlerProtection.md) | A ProtectionParameter encapsulating a CallbackHandler. | | [KeyStore.PasswordProtection](../java/security/KeyStore.PasswordProtection.md) | A password-based implementation of`ProtectionParameter`. | | [KeyStoreParameter](../android/security/KeyStoreParameter.md) | This provides the optional parameters that can be specified for`KeyStore`entries that work with [Android KeyStore facility](https://developer.android.com/training/articles/keystore.html). | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

A marker interface for keystore protection parameters.

The information stored in a`ProtectionParameter`object protects the contents of a keystore. For example, protection parameters may be used to check the integrity of keystore data, or to protect the confidentiality of sensitive keystore data (such as a`PrivateKey`).

## Summary
