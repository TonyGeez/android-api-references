# KeyStore.ProtectionParameter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ProtectionParameter

```
interface ProtectionParameter
```

| [java.security.KeyStore.ProtectionParameter](https://developer.android.com/reference/kotlin/java/security/KeyStore.ProtectionParameter#) |

| Known Direct Subclasses [KeyProtection](https://developer.android.com/reference/kotlin/android/security/keystore/KeyProtection.html#), [KeyStore.CallbackHandlerProtection](https://developer.android.com/reference/kotlin/java/security/KeyStore.CallbackHandlerProtection), [KeyStore.PasswordProtection](https://developer.android.com/reference/kotlin/java/security/KeyStore.PasswordProtection), [KeyStoreParameter](https://developer.android.com/reference/kotlin/android/security/KeyStoreParameter.html#) |---------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [KeyProtection](https://developer.android.com/reference/kotlin/android/security/keystore/KeyProtection.html#) | Specification of how a key or key pair is secured when imported into the [Android Keystore system](https://developer.android.com/training/articles/keystore.html). | | [KeyStore.CallbackHandlerProtection](https://developer.android.com/reference/kotlin/java/security/KeyStore.CallbackHandlerProtection) | A ProtectionParameter encapsulating a CallbackHandler. | | [KeyStore.PasswordProtection](https://developer.android.com/reference/kotlin/java/security/KeyStore.PasswordProtection) | A password-based implementation of`ProtectionParameter`. | | [KeyStoreParameter](https://developer.android.com/reference/kotlin/android/security/KeyStoreParameter.html#) | This provides the optional parameters that can be specified for`KeyStore`entries that work with [Android KeyStore facility](https://developer.android.com/training/articles/keystore.html). | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

A marker interface for keystore protection parameters.

The information stored in a`ProtectionParameter`object protects the contents of a keystore. For example, protection parameters may be used to check the integrity of keystore data, or to protect the confidentiality of sensitive keystore data (such as a`PrivateKey`).

## Summary
