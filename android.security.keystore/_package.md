# android.security.keystore

# android.security.keystore

Kotlin| [Java](../android/security/keystore/_package.md)
| --- | --- |

## Classes

| [KeyGenParameterSpec](../android/security/keystore/KeyGenParameterSpec.md) | [AlgorithmParameterSpec](../java/security/spec/AlgorithmParameterSpec.md) for initializing a [KeyPairGenerator](../java/security/KeyPairGenerator.md) or a [KeyGenerator](../javax/crypto/KeyGenerator.md) of the [Android Keystore system](https://developer.android.com/training/articles/keystore.html). |
| --- | --- |
| [KeyInfo](../android/security/keystore/KeyInfo.md) | Information about a key from the [Android Keystore system](https://developer.android.com/training/articles/keystore.html). |
| [KeyProperties](../android/security/keystore/KeyProperties.md) | Properties of [Android Keystore](https://developer.android.com/training/articles/keystore.html) keys. |
| [KeyProtection](../android/security/keystore/KeyProtection.md) | Specification of how a key or key pair is secured when imported into the [Android Keystore system](https://developer.android.com/training/articles/keystore.html). |
| --- | --- |
| [KeyStoreManager](../android/security/keystore/KeyStoreManager.md) | This class provides methods for interacting with keys stored within the [Android Keystore](../privacy-and-security/keystore.md). |
| [WrappedKeyEntry](../android/security/keystore/WrappedKeyEntry.md) | An [Entry](../java/security/KeyStore.Entry.md) that holds a wrapped key. |

## Exceptions

| [BackendBusyException](../android/security/keystore/BackendBusyException.md) | Indicates a transient error that prevented a key operation from being created. |
| --- | --- |
| [KeyExpiredException](../android/security/keystore/KeyExpiredException.md) | Indicates that a cryptographic operation failed because the employed key's validity end date is in the past. |
| [KeyNotYetValidException](../android/security/keystore/KeyNotYetValidException.md) | Indicates that a cryptographic operation failed because the employed key's validity start date is in the future. |
| [KeyPermanentlyInvalidatedException](../android/security/keystore/KeyPermanentlyInvalidatedException.md) | Indicates that the key can no longer be used because it has been permanently invalidated. |
| --- | --- |
| [SecureKeyImportUnavailableException](../android/security/keystore/SecureKeyImportUnavailableException.md) | Indicates that the Keystore does not support securely importing wrapped keys. |
| [StrongBoxUnavailableException](../android/security/keystore/StrongBoxUnavailableException.md) | Indicates that an operation could not be performed because the requested security hardware is not available. |
| [UserNotAuthenticatedException](../android/security/keystore/UserNotAuthenticatedException.md) | Indicates that a cryptographic operation could not be performed because the user has not been authenticated recently enough. |
| --- | --- |
| [UserPresenceUnavailableException](../android/security/keystore/UserPresenceUnavailableException.md) | Indicates the condition that a proof of user-presence was requested but this proof was not presented. |
