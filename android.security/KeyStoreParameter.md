# KeyStoreParameter

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# KeyStoreParameter

Kotlin| [Java](KeyStoreParameter.md) 
| --- | --- |

```
class KeyStoreParameter : KeyStore.ProtectionParameter
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.security.KeyStoreParameter](KeyStoreParameter.md) |

| **This class was deprecated in API level 23.**
|
| Use [KeyProtection](../android.security.keystore/KeyProtection.md) instead.

This provides the optional parameters that can be specified for`KeyStore`entries that work with [Android KeyStore facility](https://developer.android.com/training/articles/keystore.html). The Android KeyStore facility is accessed through a [java.security.KeyStore](../java.security/KeyStore.md) API using the`AndroidKeyStore`provider. The`context`passed in may be used to pop up some UI to ask the user to unlock or initialize the Android KeyStore facility.

Any entries placed in the`KeyStore`may be retrieved later. Note that there is only one logical instance of the`KeyStore`per application UID so apps using the`sharedUid`facility will also share a`KeyStore`.

Keys may be generated using the [KeyPairGenerator](../java.security/KeyPairGenerator.md) facility with a [KeyPairGeneratorSpec](KeyPairGeneratorSpec.md) to specify the entry's`alias`. A self-signed X.509 certificate will be attached to generated entries, but that may be replaced at a later time by a certificate signed by a real Certificate Authority.

## Summary

| Nested classes ||
|---|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](../android/security/KeyStoreParameter.Builder.md) Builder class for [KeyStoreParameter](KeyStoreParameter.md) objects. |

| Public methods ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEncryptionRequired](KeyStoreParameter.md))`()` Returns`true`if the [java.security.KeyStore](../java.security/KeyStore.md) entry must be encrypted at rest. |

## Public methods

### isEncryptionRequired

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isEncryptionRequired(): Boolean
```

**Deprecated:** *Data at rest encryption is enabled by default. If extra binding to the lockscreen credential is desired, use [.Builder#setUserAuthenticationRequired(boolean)](../android.security.keystore/KeyGenParameterSpec.md). This flag will be ignored from Android S.*

Returns`true`if the [java.security.KeyStore](../java.security/KeyStore.md) entry must be encrypted at rest. This will protect the entry with the secure lock screen credential (e.g., password, PIN, or pattern).

Note that encrypting the key at rest requires that the secure lock screen (e.g., password, PIN, pattern) is set up, otherwise key generation will fail. Moreover, this key will be deleted when the secure lock screen is disabled or reset (e.g., by the user or a Device Administrator). Finally, this key cannot be used until the user unlocks the secure lock screen after boot. 
**See Also**

- [android.app.KeyguardManager#isDeviceSecure()](../android.app/KeyguardManager.md))
