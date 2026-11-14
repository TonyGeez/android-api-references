# android.security.keystore

# android.security.keystore

Kotlin| [Java](_package.md)
| --- | --- |

## Classes

| [KeyGenParameterSpec](KeyGenParameterSpec.md) | [AlgorithmParameterSpec](../java.security.spec/AlgorithmParameterSpec.md) for initializing a [KeyPairGenerator](../java.security/KeyPairGenerator.md) or a [KeyGenerator](../javax.crypto/KeyGenerator.md) of the [Android Keystore system](https://developer.android.com/training/articles/keystore.html). |
| --- | --- |
| [KeyInfo](KeyInfo.md) | Information about a key from the [Android Keystore system](https://developer.android.com/training/articles/keystore.html). |
| [KeyProperties](KeyProperties.md) | Properties of [Android Keystore](https://developer.android.com/training/articles/keystore.html) keys. |
| [KeyProtection](KeyProtection.md) | Specification of how a key or key pair is secured when imported into the [Android Keystore system](https://developer.android.com/training/articles/keystore.html). |
| --- | --- |
| [KeyStoreManager](KeyStoreManager.md) | This class provides methods for interacting with keys stored within the [Android Keystore](../privacy-and-security/keystore.md). |
| [WrappedKeyEntry](WrappedKeyEntry.md) | An [Entry](../java/security/KeyStore.Entry.md) that holds a wrapped key. |

## Exceptions

| [BackendBusyException](BackendBusyException.md) | Indicates a transient error that prevented a key operation from being created. |
| --- | --- |
| [KeyExpiredException](KeyExpiredException.md) | Indicates that a cryptographic operation failed because the employed key's validity end date is in the past. |
| [KeyNotYetValidException](KeyNotYetValidException.md) | Indicates that a cryptographic operation failed because the employed key's validity start date is in the future. |
| [KeyPermanentlyInvalidatedException](KeyPermanentlyInvalidatedException.md) | Indicates that the key can no longer be used because it has been permanently invalidated. |
| --- | --- |
| [SecureKeyImportUnavailableException](SecureKeyImportUnavailableException.md) | Indicates that the Keystore does not support securely importing wrapped keys. |
| [StrongBoxUnavailableException](StrongBoxUnavailableException.md) | Indicates that an operation could not be performed because the requested security hardware is not available. |
| [UserNotAuthenticatedException](UserNotAuthenticatedException.md) | Indicates that a cryptographic operation could not be performed because the user has not been authenticated recently enough. |
| --- | --- |
| [UserPresenceUnavailableException](UserPresenceUnavailableException.md) | Indicates the condition that a proof of user-presence was requested but this proof was not presented. |
