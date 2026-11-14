# Destroyable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Destroyable

```
interface Destroyable
```

| [javax.security.auth.Destroyable](https://developer.android.com/reference/kotlin/javax/security/auth/Destroyable#) |

| Known Direct Subclasses [KeyStore.PasswordProtection](https://developer.android.com/reference/kotlin/java/security/KeyStore.PasswordProtection.html#), [PrivateKey](https://developer.android.com/reference/kotlin/java/security/PrivateKey.html#), [SecretKey](https://developer.android.com/reference/kotlin/javax/crypto/SecretKey.html#), [X500PrivateCredential](https://developer.android.com/reference/kotlin/javax/security/auth/x500/X500PrivateCredential) |-------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------| | [KeyStore.PasswordProtection](https://developer.android.com/reference/kotlin/java/security/KeyStore.PasswordProtection.html#) | A password-based implementation of`ProtectionParameter`. | | [PrivateKey](https://developer.android.com/reference/kotlin/java/security/PrivateKey.html#) | A private key. | | [SecretKey](https://developer.android.com/reference/kotlin/javax/crypto/SecretKey.html#) | A secret (symmetric) key. | | [X500PrivateCredential](https://developer.android.com/reference/kotlin/javax/security/auth/x500/X500PrivateCredential) | This class represents an`X500PrivateCredential`. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [DHPrivateKey](https://developer.android.com/reference/kotlin/javax/crypto/interfaces/DHPrivateKey.html#), [DSAPrivateKey](https://developer.android.com/reference/kotlin/java/security/interfaces/DSAPrivateKey.html#), [ECPrivateKey](https://developer.android.com/reference/kotlin/java/security/interfaces/ECPrivateKey.html#), [EdECPrivateKey](https://developer.android.com/reference/kotlin/java/security/interfaces/EdECPrivateKey.html#), [PBEKey](https://developer.android.com/reference/kotlin/javax/crypto/interfaces/PBEKey.html#), [RSAMultiPrimePrivateCrtKey](https://developer.android.com/reference/kotlin/java/security/interfaces/RSAMultiPrimePrivateCrtKey.html#), [RSAPrivateCrtKey](https://developer.android.com/reference/kotlin/java/security/interfaces/RSAPrivateCrtKey.html#), [RSAPrivateKey](https://developer.android.com/reference/kotlin/java/security/interfaces/RSAPrivateKey.html#), [SecretKeySpec](https://developer.android.com/reference/kotlin/javax/crypto/spec/SecretKeySpec.html#), [XECPrivateKey](https://developer.android.com/reference/kotlin/java/security/interfaces/XECPrivateKey.html#) |----------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [DHPrivateKey](https://developer.android.com/reference/kotlin/javax/crypto/interfaces/DHPrivateKey.html#) | The interface to a Diffie-Hellman private key. | | [DSAPrivateKey](https://developer.android.com/reference/kotlin/java/security/interfaces/DSAPrivateKey.html#) | The standard interface to a DSA private key. | | [ECPrivateKey](https://developer.android.com/reference/kotlin/java/security/interfaces/ECPrivateKey.html#) | The interface to an elliptic curve (EC) private key. | | [EdECPrivateKey](https://developer.android.com/reference/kotlin/java/security/interfaces/EdECPrivateKey.html#) | An interface for an elliptic curve private key as defined by [RFC 8032: Edwards-Curve Digital Signature Algorithm (EdDSA)](https://tools.ietf.org/html/rfc8032). | | [PBEKey](https://developer.android.com/reference/kotlin/javax/crypto/interfaces/PBEKey.html#) | The interface to a PBE key. | | [RSAMultiPrimePrivateCrtKey](https://developer.android.com/reference/kotlin/java/security/interfaces/RSAMultiPrimePrivateCrtKey.html#) | The interface to an RSA multi-prime private key, as defined in the [PKCS#1 v2.2](https://tools.ietf.org/rfc/rfc8017.txt) standard, using the*Chinese Remainder Theorem*(CRT) information values. | | [RSAPrivateCrtKey](https://developer.android.com/reference/kotlin/java/security/interfaces/RSAPrivateCrtKey.html#) | The interface to an RSA private key, as defined in the [PKCS#1 v2.2](https://tools.ietf.org/rfc/rfc8017.txt) standard, using the*Chinese Remainder Theorem*(CRT) information values. | | [RSAPrivateKey](https://developer.android.com/reference/kotlin/java/security/interfaces/RSAPrivateKey.html#) | The interface to an RSA private key. | | [SecretKeySpec](https://developer.android.com/reference/kotlin/javax/crypto/spec/SecretKeySpec.html#) | This class specifies a secret key in a provider-independent fashion. | | [XECPrivateKey](https://developer.android.com/reference/kotlin/java/security/interfaces/XECPrivateKey.html#) | An interface for an elliptic curve private key as defined by RFC 7748. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Objects such as credentials may optionally implement this interface to provide the capability to destroy its contents.

## Summary

| Public methods ||
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [destroy](https://developer.android.com/reference/kotlin/javax/security/auth/Destroyable#destroy())`()` Destroy this`Object`. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isDestroyed](https://developer.android.com/reference/kotlin/javax/security/auth/Destroyable#isDestroyed())`()` Determine if this`Object`has been destroyed. |

## Public methods

### destroy

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun destroy(): Unit
```

Destroy this`Object`.

Sensitive information associated with this`Object`is destroyed or cleared. Subsequent calls to certain methods on this`Object`will result in an`IllegalStateException`being thrown.

The default implementation throws`DestroyFailedException`.

Android note: Up to and including API 25 this method did not have a default implementation. Implementations of this interface must provide a concrete implementation of this method in order to work on older versions of Android.

| Exceptions ||
|----------------------------------------------|-----------------------------------------------------------------|
| `javax.security.auth.DestroyFailedException` | if the destroy operation fails. <br /> |
| `java.lang.SecurityException` | if the caller does not have permission to destroy this`Object`. |

### isDestroyed

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isDestroyed(): Boolean
```

Determine if this`Object`has been destroyed.

The default implementation returns false.

Android note: Up to and including API 25 this method did not have a default implementation. Implementations of this interface must provide a concrete implementation of this method in order to work on older versions of Android.

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if this`Object`has been destroyed, false otherwise. |
