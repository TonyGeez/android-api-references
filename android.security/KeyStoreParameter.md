# KeyStoreParameter

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# KeyStoreParameter

Kotlin| [Java](https://developer.android.com/reference/android/security/KeyStoreParameter "View this page in Java") 
| --- | --- |

```
class KeyStoreParameter : KeyStore.ProtectionParameter
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.security.KeyStoreParameter](https://developer.android.com/reference/kotlin/android/security/KeyStoreParameter#) |

| **This class was deprecated in API level 23.**
|
| Use [KeyProtection](https://developer.android.com/reference/kotlin/android/security/keystore/KeyProtection) instead.

This provides the optional parameters that can be specified for`KeyStore`entries that work with [Android KeyStore facility](https://developer.android.com/training/articles/keystore.html). The Android KeyStore facility is accessed through a [java.security.KeyStore](https://developer.android.com/reference/kotlin/java/security/KeyStore.html#) API using the`AndroidKeyStore`provider. The`context`passed in may be used to pop up some UI to ask the user to unlock or initialize the Android KeyStore facility.

Any entries placed in the`KeyStore`may be retrieved later. Note that there is only one logical instance of the`KeyStore`per application UID so apps using the`sharedUid`facility will also share a`KeyStore`.

Keys may be generated using the [KeyPairGenerator](https://developer.android.com/reference/kotlin/java/security/KeyPairGenerator.html#) facility with a [KeyPairGeneratorSpec](https://developer.android.com/reference/kotlin/android/security/KeyPairGeneratorSpec) to specify the entry's`alias`. A self-signed X.509 certificate will be attached to generated entries, but that may be replaced at a later time by a certificate signed by a real Certificate Authority.

## Summary

| Nested classes ||
|---|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](https://developer.android.com/reference/kotlin/android/security/KeyStoreParameter.Builder) Builder class for [KeyStoreParameter](https://developer.android.com/reference/kotlin/android/security/KeyStoreParameter#) objects. |

| Public methods ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEncryptionRequired](https://developer.android.com/reference/kotlin/android/security/KeyStoreParameter#isEncryptionRequired())`()` Returns`true`if the [java.security.KeyStore](https://developer.android.com/reference/kotlin/java/security/KeyStore.html#) entry must be encrypted at rest. |

## Public methods

### isEncryptionRequired

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isEncryptionRequired(): Boolean
```

**Deprecated:** *Data at rest encryption is enabled by default. If extra binding to the lockscreen credential is desired, use [.Builder#setUserAuthenticationRequired(boolean)](https://developer.android.com/reference/kotlin/android/security/keystore/KeyGenParameterSpec). This flag will be ignored from Android S.*

Returns`true`if the [java.security.KeyStore](https://developer.android.com/reference/kotlin/java/security/KeyStore.html#) entry must be encrypted at rest. This will protect the entry with the secure lock screen credential (e.g., password, PIN, or pattern).

Note that encrypting the key at rest requires that the secure lock screen (e.g., password, PIN, pattern) is set up, otherwise key generation will fail. Moreover, this key will be deleted when the secure lock screen is disabled or reset (e.g., by the user or a Device Administrator). Finally, this key cannot be used until the user unlocks the secure lock screen after boot. 
**See Also**

- [android.app.KeyguardManager#isDeviceSecure()](https://developer.android.com/reference/kotlin/android/app/KeyguardManager.html#isDeviceSecure())
