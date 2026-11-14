# Destroyable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Destroyable

```
interface Destroyable
```

| [javax.security.auth.Destroyable](Destroyable.md) |

| Known Direct Subclasses [KeyStore.PasswordProtection](../java/security/KeyStore.PasswordProtection.md), [PrivateKey](../java.security/PrivateKey.md), [SecretKey](../javax.crypto/SecretKey.md), [X500PrivateCredential](../javax.security.auth.x500/X500PrivateCredential.md) |-------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------| | [KeyStore.PasswordProtection](../java/security/KeyStore.PasswordProtection.md) | A password-based implementation of`ProtectionParameter`. | | [PrivateKey](../java.security/PrivateKey.md) | A private key. | | [SecretKey](../javax.crypto/SecretKey.md) | A secret (symmetric) key. | | [X500PrivateCredential](../javax.security.auth.x500/X500PrivateCredential.md) | This class represents an`X500PrivateCredential`. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [DHPrivateKey](../javax.crypto.interfaces/DHPrivateKey.md), [DSAPrivateKey](../java.security.interfaces/DSAPrivateKey.md), [ECPrivateKey](../java.security.interfaces/ECPrivateKey.md), [EdECPrivateKey](../java.security.interfaces/EdECPrivateKey.md), [PBEKey](../javax.crypto.interfaces/PBEKey.md), [RSAMultiPrimePrivateCrtKey](../java.security.interfaces/RSAMultiPrimePrivateCrtKey.md), [RSAPrivateCrtKey](../java.security.interfaces/RSAPrivateCrtKey.md), [RSAPrivateKey](../java.security.interfaces/RSAPrivateKey.md), [SecretKeySpec](../javax.crypto.spec/SecretKeySpec.md), [XECPrivateKey](../java.security.interfaces/XECPrivateKey.md) |----------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [DHPrivateKey](../javax.crypto.interfaces/DHPrivateKey.md) | The interface to a Diffie-Hellman private key. | | [DSAPrivateKey](../java.security.interfaces/DSAPrivateKey.md) | The standard interface to a DSA private key. | | [ECPrivateKey](../java.security.interfaces/ECPrivateKey.md) | The interface to an elliptic curve (EC) private key. | | [EdECPrivateKey](../java.security.interfaces/EdECPrivateKey.md) | An interface for an elliptic curve private key as defined by [RFC 8032: Edwards-Curve Digital Signature Algorithm (EdDSA)](https://tools.ietf.org/html/rfc8032). | | [PBEKey](../javax.crypto.interfaces/PBEKey.md) | The interface to a PBE key. | | [RSAMultiPrimePrivateCrtKey](../java.security.interfaces/RSAMultiPrimePrivateCrtKey.md) | The interface to an RSA multi-prime private key, as defined in the [PKCS#1 v2.2](https://tools.ietf.org/rfc/rfc8017.txt) standard, using the*Chinese Remainder Theorem*(CRT) information values. | | [RSAPrivateCrtKey](../java.security.interfaces/RSAPrivateCrtKey.md) | The interface to an RSA private key, as defined in the [PKCS#1 v2.2](https://tools.ietf.org/rfc/rfc8017.txt) standard, using the*Chinese Remainder Theorem*(CRT) information values. | | [RSAPrivateKey](../java.security.interfaces/RSAPrivateKey.md) | The interface to an RSA private key. | | [SecretKeySpec](../javax.crypto.spec/SecretKeySpec.md) | This class specifies a secret key in a provider-independent fashion. | | [XECPrivateKey](../java.security.interfaces/XECPrivateKey.md) | An interface for an elliptic curve private key as defined by RFC 7748. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Objects such as credentials may optionally implement this interface to provide the capability to destroy its contents.

## Summary

| Public methods ||
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [destroy](Destroyable.md))`()` Destroy this`Object`. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isDestroyed](Destroyable.md))`()` Determine if this`Object`has been destroyed. |

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
