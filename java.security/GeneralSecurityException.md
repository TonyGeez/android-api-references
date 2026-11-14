# GeneralSecurityException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# GeneralSecurityException

```
open class GeneralSecurityException : Exception
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) ||
| | | ↳ | [java.security.GeneralSecurityException](https://developer.android.com/reference/kotlin/java/security/GeneralSecurityException#) |

| Known Direct Subclasses [BadPaddingException](https://developer.android.com/reference/kotlin/javax/crypto/BadPaddingException.html#), [CRLException](https://developer.android.com/reference/kotlin/java/security/cert/CRLException), [CertPathBuilderException](https://developer.android.com/reference/kotlin/java/security/cert/CertPathBuilderException), [CertPathValidatorException](https://developer.android.com/reference/kotlin/java/security/cert/CertPathValidatorException), [CertStoreException](https://developer.android.com/reference/kotlin/java/security/cert/CertStoreException), [CertificateException](https://developer.android.com/reference/kotlin/java/security/cert/CertificateException), [DigestException](https://developer.android.com/reference/kotlin/java/security/DigestException), [ExemptionMechanismException](https://developer.android.com/reference/kotlin/javax/crypto/ExemptionMechanismException.html#), [IllegalBlockSizeException](https://developer.android.com/reference/kotlin/javax/crypto/IllegalBlockSizeException.html#), [InvalidAlgorithmParameterException](https://developer.android.com/reference/kotlin/java/security/InvalidAlgorithmParameterException), [InvalidKeySpecException](https://developer.android.com/reference/kotlin/java/security/spec/InvalidKeySpecException), [InvalidParameterSpecException](https://developer.android.com/reference/kotlin/java/security/spec/InvalidParameterSpecException), and 9 others. |---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------| | [BadPaddingException](https://developer.android.com/reference/kotlin/javax/crypto/BadPaddingException.html#) | This exception is thrown when a particular padding mechanism is expected for the input data but the data is not padded properly. | | [CRLException](https://developer.android.com/reference/kotlin/java/security/cert/CRLException) | CRL (Certificate Revocation List) Exception. | | [CertPathBuilderException](https://developer.android.com/reference/kotlin/java/security/cert/CertPathBuilderException) | An exception indicating one of a variety of problems encountered when building a certification path with a `CertPathBuilder`. | | [CertPathValidatorException](https://developer.android.com/reference/kotlin/java/security/cert/CertPathValidatorException) | An exception indicating one of a variety of problems encountered when validating a certification path. | | [CertStoreException](https://developer.android.com/reference/kotlin/java/security/cert/CertStoreException) | An exception indicating one of a variety of problems retrieving certificates and CRLs from a `CertStore`. | | [CertificateException](https://developer.android.com/reference/kotlin/java/security/cert/CertificateException) | This exception indicates one of a variety of certificate problems. | | [DigestException](https://developer.android.com/reference/kotlin/java/security/DigestException) | This is the generic Message Digest exception. | | [ExemptionMechanismException](https://developer.android.com/reference/kotlin/javax/crypto/ExemptionMechanismException.html#) | This is the generic ExemptionMechanism exception. | | [IllegalBlockSizeException](https://developer.android.com/reference/kotlin/javax/crypto/IllegalBlockSizeException.html#) | This exception is thrown when the length of data provided to a block cipher is incorrect, i. | | [InvalidAlgorithmParameterException](https://developer.android.com/reference/kotlin/java/security/InvalidAlgorithmParameterException) | This is the exception for invalid or inappropriate algorithm parameters. | | [InvalidKeySpecException](https://developer.android.com/reference/kotlin/java/security/spec/InvalidKeySpecException) | This is the exception for invalid key specifications. | | [InvalidParameterSpecException](https://developer.android.com/reference/kotlin/java/security/spec/InvalidParameterSpecException) | This is the exception for invalid parameter specifications. | | [KeyException](https://developer.android.com/reference/kotlin/java/security/KeyException) | This is the basic key exception. | | [KeyStoreException](https://developer.android.com/reference/kotlin/java/security/KeyStoreException) | This is the generic KeyStore exception. | | [LoginException](https://developer.android.com/reference/kotlin/javax/security/auth/login/LoginException.html#) | This is the basic login exception. | | [NoSuchAlgorithmException](https://developer.android.com/reference/kotlin/java/security/NoSuchAlgorithmException) | This exception is thrown when a particular cryptographic algorithm is requested but is not available in the environment. | | [NoSuchPaddingException](https://developer.android.com/reference/kotlin/javax/crypto/NoSuchPaddingException.html#) | This exception is thrown when a particular padding mechanism is requested but is not available in the environment. | | [NoSuchProviderException](https://developer.android.com/reference/kotlin/java/security/NoSuchProviderException) | This exception is thrown when a particular security provider is requested but is not available in the environment. | | [ShortBufferException](https://developer.android.com/reference/kotlin/javax/crypto/ShortBufferException.html#) | This exception is thrown when an output buffer provided by the user is too short to hold the operation result. | | [SignatureException](https://developer.android.com/reference/kotlin/java/security/SignatureException) | This is the generic Signature exception. | | [UnrecoverableEntryException](https://developer.android.com/reference/kotlin/java/security/UnrecoverableEntryException) | This exception is thrown if an entry in the keystore cannot be recovered. | |

| Known Indirect Subclasses [AEADBadTagException](https://developer.android.com/reference/kotlin/javax/crypto/AEADBadTagException.html#), [CertificateEncodingException](https://developer.android.com/reference/kotlin/java/security/cert/CertificateEncodingException), [CertificateExpiredException](https://developer.android.com/reference/kotlin/java/security/cert/CertificateExpiredException), [CertificateNotYetValidException](https://developer.android.com/reference/kotlin/java/security/cert/CertificateNotYetValidException), [CertificateParsingException](https://developer.android.com/reference/kotlin/java/security/cert/CertificateParsingException), [CertificateRevokedException](https://developer.android.com/reference/kotlin/java/security/cert/CertificateRevokedException), [InvalidKeyException](https://developer.android.com/reference/kotlin/java/security/InvalidKeyException), [KeyExpiredException](https://developer.android.com/reference/kotlin/android/security/keystore/KeyExpiredException.html#), [KeyManagementException](https://developer.android.com/reference/kotlin/java/security/KeyManagementException), [KeyNotYetValidException](https://developer.android.com/reference/kotlin/android/security/keystore/KeyNotYetValidException.html#), [KeyPermanentlyInvalidatedException](https://developer.android.com/reference/kotlin/android/security/keystore/KeyPermanentlyInvalidatedException.html#), [UnrecoverableKeyException](https://developer.android.com/reference/kotlin/java/security/UnrecoverableKeyException), and 2 others. |---------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [AEADBadTagException](https://developer.android.com/reference/kotlin/javax/crypto/AEADBadTagException.html#) | This exception is thrown when a [Cipher](https://developer.android.com/reference/kotlin/javax/crypto/Cipher.html#) operating in an AEAD mode (such as GCM/CCM) is unable to verify the supplied authentication tag. | | [CertificateEncodingException](https://developer.android.com/reference/kotlin/java/security/cert/CertificateEncodingException) | Certificate Encoding Exception. | | [CertificateExpiredException](https://developer.android.com/reference/kotlin/java/security/cert/CertificateExpiredException) | Certificate Expired Exception. | | [CertificateNotYetValidException](https://developer.android.com/reference/kotlin/java/security/cert/CertificateNotYetValidException) | Certificate is not yet valid exception. | | [CertificateParsingException](https://developer.android.com/reference/kotlin/java/security/cert/CertificateParsingException) | Certificate Parsing Exception. | | [CertificateRevokedException](https://developer.android.com/reference/kotlin/java/security/cert/CertificateRevokedException) | An exception that indicates an X. | | [InvalidKeyException](https://developer.android.com/reference/kotlin/java/security/InvalidKeyException) | This is the exception for invalid Keys (invalid encoding, wrong length, uninitialized, etc). | | [KeyExpiredException](https://developer.android.com/reference/kotlin/android/security/keystore/KeyExpiredException.html#) | Indicates that a cryptographic operation failed because the employed key's validity end date is in the past. | | [KeyManagementException](https://developer.android.com/reference/kotlin/java/security/KeyManagementException) | This is the general key management exception for all operations dealing with key management. | | [KeyNotYetValidException](https://developer.android.com/reference/kotlin/android/security/keystore/KeyNotYetValidException.html#) | Indicates that a cryptographic operation failed because the employed key's validity start date is in the future. | | [KeyPermanentlyInvalidatedException](https://developer.android.com/reference/kotlin/android/security/keystore/KeyPermanentlyInvalidatedException.html#) | Indicates that the key can no longer be used because it has been permanently invalidated. | | [UnrecoverableKeyException](https://developer.android.com/reference/kotlin/java/security/UnrecoverableKeyException) | This exception is thrown if a key in the keystore cannot be recovered. | | [UserNotAuthenticatedException](https://developer.android.com/reference/kotlin/android/security/keystore/UserNotAuthenticatedException.html#) | Indicates that a cryptographic operation could not be performed because the user has not been authenticated recently enough. | | [UserPresenceUnavailableException](https://developer.android.com/reference/kotlin/android/security/keystore/UserPresenceUnavailableException.html#) | Indicates the condition that a proof of user-presence was requested but this proof was not presented. | |

The `GeneralSecurityException` class is a generic security exception class that provides type safety for all the security-related exception classes that extend from it.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [GeneralSecurityException](https://developer.android.com/reference/kotlin/java/security/GeneralSecurityException#GeneralSecurityException())`()` Constructs a GeneralSecurityException with no detail message. |
| [GeneralSecurityException](https://developer.android.com/reference/kotlin/java/security/GeneralSecurityException#GeneralSecurityException(kotlin.String))`(`msg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a GeneralSecurityException with the specified detail message. |
| [GeneralSecurityException](https://developer.android.com/reference/kotlin/java/security/GeneralSecurityException#GeneralSecurityException(kotlin.String,%20kotlin.Throwable))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Creates a `GeneralSecurityException` with the specified detail message and cause. |
| [GeneralSecurityException](https://developer.android.com/reference/kotlin/java/security/GeneralSecurityException#GeneralSecurityException(kotlin.Throwable))`(`cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Creates a `GeneralSecurityException` with the specified cause and a detail message of `(cause==null ? null : cause.toString())` (which typically contains the class and detail message of `cause`). |

## Public constructors

### GeneralSecurityException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
GeneralSecurityException()
```

Constructs a GeneralSecurityException with no detail message. 

### GeneralSecurityException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
GeneralSecurityException(msg: String!)
```

Constructs a GeneralSecurityException with the specified detail message. A detail message is a String that describes this particular exception.

| Parameters ||
|-------|--------------------------------------------------------------------------------------------------------|
| `msg` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the detail message. |

### GeneralSecurityException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
GeneralSecurityException(
    message: String!, 
    cause: Throwable!)
```

Creates a `GeneralSecurityException` with the specified detail message and cause.

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the detail message (which is saved for later retrieval by the [getMessage()](https://developer.android.com/reference/kotlin/java/lang/Throwable.html#getMessage()) method). |
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!: the cause (which is saved for later retrieval by the [getCause()](https://developer.android.com/reference/kotlin/java/lang/Throwable.html#getCause()) method). (A `null` value is permitted, and indicates that the cause is nonexistent or unknown.) |

### GeneralSecurityException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
GeneralSecurityException(cause: Throwable!)
```

Creates a `GeneralSecurityException` with the specified cause and a detail message of `(cause==null ? null : cause.toString())` (which typically contains the class and detail message of `cause`).

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!: the cause (which is saved for later retrieval by the [getCause()](https://developer.android.com/reference/kotlin/java/lang/Throwable.html#getCause()) method). (A `null` value is permitted, and indicates that the cause is nonexistent or unknown.) |
