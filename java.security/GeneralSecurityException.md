# GeneralSecurityException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# GeneralSecurityException

```
open class GeneralSecurityException : Exception
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||
| | ↳ | [java.lang.Exception](../java/lang/Exception.md) ||
| | | ↳ | [java.security.GeneralSecurityException](../java/security/GeneralSecurityException.md) |
| --- | --- | --- | --- |

| Known Direct Subclasses [BadPaddingException](../javax/crypto/BadPaddingException.md), [CRLException](../java/security/cert/CRLException.md), [CertPathBuilderException](../java/security/cert/CertPathBuilderException.md), [CertPathValidatorException](../java/security/cert/CertPathValidatorException.md), [CertStoreException](../java/security/cert/CertStoreException.md), [CertificateException](../java/security/cert/CertificateException.md), [DigestException](../java/security/DigestException.md), [ExemptionMechanismException](../javax/crypto/ExemptionMechanismException.md), [IllegalBlockSizeException](../javax/crypto/IllegalBlockSizeException.md), [InvalidAlgorithmParameterException](../java/security/InvalidAlgorithmParameterException.md), [InvalidKeySpecException](../java/security/spec/InvalidKeySpecException.md), [InvalidParameterSpecException](../java/security/spec/InvalidParameterSpecException.md), and 9 others. |---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------| | [BadPaddingException](../javax/crypto/BadPaddingException.md) | This exception is thrown when a particular padding mechanism is expected for the input data but the data is not padded properly. | | [CRLException](../java/security/cert/CRLException.md) | CRL (Certificate Revocation List) Exception. | | [CertPathBuilderException](../java/security/cert/CertPathBuilderException.md) | An exception indicating one of a variety of problems encountered when building a certification path with a `CertPathBuilder`. | | [CertPathValidatorException](../java/security/cert/CertPathValidatorException.md) | An exception indicating one of a variety of problems encountered when validating a certification path. | | [CertStoreException](../java/security/cert/CertStoreException.md) | An exception indicating one of a variety of problems retrieving certificates and CRLs from a `CertStore`. | | [CertificateException](../java/security/cert/CertificateException.md) | This exception indicates one of a variety of certificate problems. | | [DigestException](../java/security/DigestException.md) | This is the generic Message Digest exception. | | [ExemptionMechanismException](../javax/crypto/ExemptionMechanismException.md) | This is the generic ExemptionMechanism exception. | | [IllegalBlockSizeException](../javax/crypto/IllegalBlockSizeException.md) | This exception is thrown when the length of data provided to a block cipher is incorrect, i. | | [InvalidAlgorithmParameterException](../java/security/InvalidAlgorithmParameterException.md) | This is the exception for invalid or inappropriate algorithm parameters. | | [InvalidKeySpecException](../java/security/spec/InvalidKeySpecException.md) | This is the exception for invalid key specifications. | | [InvalidParameterSpecException](../java/security/spec/InvalidParameterSpecException.md) | This is the exception for invalid parameter specifications. | | [KeyException](../java/security/KeyException.md) | This is the basic key exception. | | [KeyStoreException](../java/security/KeyStoreException.md) | This is the generic KeyStore exception. | | [LoginException](../javax/security/auth/login/LoginException.md) | This is the basic login exception. | | [NoSuchAlgorithmException](../java/security/NoSuchAlgorithmException.md) | This exception is thrown when a particular cryptographic algorithm is requested but is not available in the environment. | | [NoSuchPaddingException](../javax/crypto/NoSuchPaddingException.md) | This exception is thrown when a particular padding mechanism is requested but is not available in the environment. | | [NoSuchProviderException](../java/security/NoSuchProviderException.md) | This exception is thrown when a particular security provider is requested but is not available in the environment. | | [ShortBufferException](../javax/crypto/ShortBufferException.md) | This exception is thrown when an output buffer provided by the user is too short to hold the operation result. | | [SignatureException](../java/security/SignatureException.md) | This is the generic Signature exception. | | [UnrecoverableEntryException](../java/security/UnrecoverableEntryException.md) | This exception is thrown if an entry in the keystore cannot be recovered. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [AEADBadTagException](../javax/crypto/AEADBadTagException.md), [CertificateEncodingException](../java/security/cert/CertificateEncodingException.md), [CertificateExpiredException](../java/security/cert/CertificateExpiredException.md), [CertificateNotYetValidException](../java/security/cert/CertificateNotYetValidException.md), [CertificateParsingException](../java/security/cert/CertificateParsingException.md), [CertificateRevokedException](../java/security/cert/CertificateRevokedException.md), [InvalidKeyException](../java/security/InvalidKeyException.md), [KeyExpiredException](../android/security/keystore/KeyExpiredException.md), [KeyManagementException](../java/security/KeyManagementException.md), [KeyNotYetValidException](../android/security/keystore/KeyNotYetValidException.md), [KeyPermanentlyInvalidatedException](../android/security/keystore/KeyPermanentlyInvalidatedException.md), [UnrecoverableKeyException](../java/security/UnrecoverableKeyException.md), and 2 others. |---------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [AEADBadTagException](../javax/crypto/AEADBadTagException.md) | This exception is thrown when a [Cipher](../javax/crypto/Cipher.md) operating in an AEAD mode (such as GCM/CCM) is unable to verify the supplied authentication tag. | | [CertificateEncodingException](../java/security/cert/CertificateEncodingException.md) | Certificate Encoding Exception. | | [CertificateExpiredException](../java/security/cert/CertificateExpiredException.md) | Certificate Expired Exception. | | [CertificateNotYetValidException](../java/security/cert/CertificateNotYetValidException.md) | Certificate is not yet valid exception. | | [CertificateParsingException](../java/security/cert/CertificateParsingException.md) | Certificate Parsing Exception. | | [CertificateRevokedException](../java/security/cert/CertificateRevokedException.md) | An exception that indicates an X. | | [InvalidKeyException](../java/security/InvalidKeyException.md) | This is the exception for invalid Keys (invalid encoding, wrong length, uninitialized, etc). | | [KeyExpiredException](../android/security/keystore/KeyExpiredException.md) | Indicates that a cryptographic operation failed because the employed key's validity end date is in the past. | | [KeyManagementException](../java/security/KeyManagementException.md) | This is the general key management exception for all operations dealing with key management. | | [KeyNotYetValidException](../android/security/keystore/KeyNotYetValidException.md) | Indicates that a cryptographic operation failed because the employed key's validity start date is in the future. | | [KeyPermanentlyInvalidatedException](../android/security/keystore/KeyPermanentlyInvalidatedException.md) | Indicates that the key can no longer be used because it has been permanently invalidated. | | [UnrecoverableKeyException](../java/security/UnrecoverableKeyException.md) | This exception is thrown if a key in the keystore cannot be recovered. | | [UserNotAuthenticatedException](../android/security/keystore/UserNotAuthenticatedException.md) | Indicates that a cryptographic operation could not be performed because the user has not been authenticated recently enough. | | [UserPresenceUnavailableException](../android/security/keystore/UserPresenceUnavailableException.md) | Indicates the condition that a proof of user-presence was requested but this proof was not presented. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

The `GeneralSecurityException` class is a generic security exception class that provides type safety for all the security-related exception classes that extend from it.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [GeneralSecurityException](../java/security/GeneralSecurityException.md))`()` Constructs a GeneralSecurityException with no detail message. |
| [GeneralSecurityException](../java/security/GeneralSecurityException.md))`(`msg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a GeneralSecurityException with the specified detail message. |
| [GeneralSecurityException](../java/security/GeneralSecurityException.md))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Creates a `GeneralSecurityException` with the specified detail message and cause. |
| [GeneralSecurityException](../java/security/GeneralSecurityException.md))`(`cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Creates a `GeneralSecurityException` with the specified cause and a detail message of `(cause==null ? null : cause.toString())` (which typically contains the class and detail message of `cause`). |

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
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the detail message (which is saved for later retrieval by the [getMessage()](../java/lang/Throwable.md)) method). |
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!: the cause (which is saved for later retrieval by the [getCause()](../java/lang/Throwable.md)) method). (A `null` value is permitted, and indicates that the cause is nonexistent or unknown.) |

### GeneralSecurityException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
GeneralSecurityException(cause: Throwable!)
```

Creates a `GeneralSecurityException` with the specified cause and a detail message of `(cause==null ? null : cause.toString())` (which typically contains the class and detail message of `cause`).

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!: the cause (which is saved for later retrieval by the [getCause()](../java/lang/Throwable.md)) method). (A `null` value is permitted, and indicates that the cause is nonexistent or unknown.) |
