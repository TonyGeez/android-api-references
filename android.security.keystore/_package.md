# android.security.keystore

# android.security.keystore

Kotlin| [Java](https://developer.android.com/reference/android/security/keystore/package-summary "View this page in Java")
| --- | --- |

## Classes

| [KeyGenParameterSpec](https://developer.android.com/reference/kotlin/android/security/keystore/KeyGenParameterSpec) | [AlgorithmParameterSpec](https://developer.android.com/reference/kotlin/java/security/spec/AlgorithmParameterSpec.html#) for initializing a [KeyPairGenerator](https://developer.android.com/reference/kotlin/java/security/KeyPairGenerator.html#) or a [KeyGenerator](https://developer.android.com/reference/kotlin/javax/crypto/KeyGenerator.html#) of the [Android Keystore system](https://developer.android.com/training/articles/keystore.html). |
| --- | --- |
| [KeyInfo](https://developer.android.com/reference/kotlin/android/security/keystore/KeyInfo) | Information about a key from the [Android Keystore system](https://developer.android.com/training/articles/keystore.html). |
| [KeyProperties](https://developer.android.com/reference/kotlin/android/security/keystore/KeyProperties) | Properties of [Android Keystore](https://developer.android.com/training/articles/keystore.html) keys. |
| [KeyProtection](https://developer.android.com/reference/kotlin/android/security/keystore/KeyProtection) | Specification of how a key or key pair is secured when imported into the [Android Keystore system](https://developer.android.com/training/articles/keystore.html). |
| --- | --- |
| [KeyStoreManager](https://developer.android.com/reference/kotlin/android/security/keystore/KeyStoreManager) | This class provides methods for interacting with keys stored within the [Android Keystore](https://developer.android.com/reference/kotlin/privacy-and-security/keystore). |
| [WrappedKeyEntry](https://developer.android.com/reference/kotlin/android/security/keystore/WrappedKeyEntry) | An [Entry](https://developer.android.com/reference/kotlin/java/security/KeyStore.Entry.html#) that holds a wrapped key. |

## Exceptions

| [BackendBusyException](https://developer.android.com/reference/kotlin/android/security/keystore/BackendBusyException) | Indicates a transient error that prevented a key operation from being created. |
| --- | --- |
| [KeyExpiredException](https://developer.android.com/reference/kotlin/android/security/keystore/KeyExpiredException) | Indicates that a cryptographic operation failed because the employed key's validity end date is in the past. |
| [KeyNotYetValidException](https://developer.android.com/reference/kotlin/android/security/keystore/KeyNotYetValidException) | Indicates that a cryptographic operation failed because the employed key's validity start date is in the future. |
| [KeyPermanentlyInvalidatedException](https://developer.android.com/reference/kotlin/android/security/keystore/KeyPermanentlyInvalidatedException) | Indicates that the key can no longer be used because it has been permanently invalidated. |
| --- | --- |
| [SecureKeyImportUnavailableException](https://developer.android.com/reference/kotlin/android/security/keystore/SecureKeyImportUnavailableException) | Indicates that the Keystore does not support securely importing wrapped keys. |
| [StrongBoxUnavailableException](https://developer.android.com/reference/kotlin/android/security/keystore/StrongBoxUnavailableException) | Indicates that an operation could not be performed because the requested security hardware is not available. |
| [UserNotAuthenticatedException](https://developer.android.com/reference/kotlin/android/security/keystore/UserNotAuthenticatedException) | Indicates that a cryptographic operation could not be performed because the user has not been authenticated recently enough. |
| --- | --- |
| [UserPresenceUnavailableException](https://developer.android.com/reference/kotlin/android/security/keystore/UserPresenceUnavailableException) | Indicates the condition that a proof of user-presence was requested but this proof was not presented. |
