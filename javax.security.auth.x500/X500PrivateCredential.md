# X500PrivateCredential

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# X500PrivateCredential

```
class X500PrivateCredential : Destroyable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [javax.security.auth.x500.X500PrivateCredential](https://developer.android.com/reference/kotlin/javax/security/auth/x500/X500PrivateCredential#) |

This class represents an`X500PrivateCredential`. It associates an X.509 certificate, corresponding private key and the KeyStore alias used to reference that exact key pair in the KeyStore. This enables looking up the private credentials for an X.500 principal in a subject.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [X500PrivateCredential](https://developer.android.com/reference/kotlin/javax/security/auth/x500/X500PrivateCredential#X500PrivateCredential(java.security.cert.X509Certificate,%20java.security.PrivateKey))`(`cert:` ` [X509Certificate](https://developer.android.com/reference/kotlin/java/security/cert/X509Certificate.html#)!`, `key:` ` [PrivateKey](https://developer.android.com/reference/kotlin/java/security/PrivateKey.html#)!`)` Creates an X500PrivateCredential that associates an X. |
| [X500PrivateCredential](https://developer.android.com/reference/kotlin/javax/security/auth/x500/X500PrivateCredential#X500PrivateCredential(java.security.cert.X509Certificate,%20java.security.PrivateKey,%20kotlin.String))`(`cert:` ` [X509Certificate](https://developer.android.com/reference/kotlin/java/security/cert/X509Certificate.html#)!`, `key:` ` [PrivateKey](https://developer.android.com/reference/kotlin/java/security/PrivateKey.html#)!`, `alias:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Creates an X500PrivateCredential that associates an X. |

| Public methods ||
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [destroy](https://developer.android.com/reference/kotlin/javax/security/auth/x500/X500PrivateCredential#destroy())`()` Clears the references to the X. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getAlias](https://developer.android.com/reference/kotlin/javax/security/auth/x500/X500PrivateCredential#getAlias())`()` Returns the KeyStore alias. |
| [X509Certificate](https://developer.android.com/reference/kotlin/java/security/cert/X509Certificate.html#)! | [getCertificate](https://developer.android.com/reference/kotlin/javax/security/auth/x500/X500PrivateCredential#getCertificate())`()` Returns the X. |
| --- | --- |
| [PrivateKey](https://developer.android.com/reference/kotlin/java/security/PrivateKey.html#)! | [getPrivateKey](https://developer.android.com/reference/kotlin/javax/security/auth/x500/X500PrivateCredential#getPrivateKey())`()` Returns the PrivateKey. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isDestroyed](https://developer.android.com/reference/kotlin/javax/security/auth/x500/X500PrivateCredential#isDestroyed())`()` Determines if the references to the X. |

## Public constructors

### X500PrivateCredential

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
X500PrivateCredential(
    cert: X509Certificate!, 
    key: PrivateKey!)
```

Creates an X500PrivateCredential that associates an X.509 certificate, a private key and the KeyStore alias.

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------------------------|
| `cert` | [X509Certificate](https://developer.android.com/reference/kotlin/java/security/cert/X509Certificate.html#)!:X509Certificate |
| `key` | [PrivateKey](https://developer.android.com/reference/kotlin/java/security/PrivateKey.html#)!:PrivateKey for the certificate |

| Exceptions ||
|--------------------------------------|-------------------------------|
| `java.lang.IllegalArgumentException` | if either`cert`or`key`is null |

### X500PrivateCredential

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
X500PrivateCredential(
    cert: X509Certificate!, 
    key: PrivateKey!, 
    alias: String!)
```

Creates an X500PrivateCredential that associates an X.509 certificate, a private key and the KeyStore alias.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------------|
| `cert` | [X509Certificate](https://developer.android.com/reference/kotlin/java/security/cert/X509Certificate.html#)!:X509Certificate |
| `key` | [PrivateKey](https://developer.android.com/reference/kotlin/java/security/PrivateKey.html#)!:PrivateKey for the certificate |
| `alias` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:KeyStore alias |
| --- | --- |

| Exceptions ||
|--------------------------------------|---------------------------------------|
| `java.lang.IllegalArgumentException` | if either`cert`,`key`or`alias`is null |

## Public methods

### destroy

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun destroy(): Unit
```

Clears the references to the X.509 certificate, private key and the KeyStore alias in this object. 

### getAlias

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAlias(): String!
```

Returns the KeyStore alias.

| Return ||
|-----------------------------------------------------------------------------------|--------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the KeyStore alias |

### getCertificate

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCertificate(): X509Certificate!
```

Returns the X.509 certificate.

| Return ||
|-------------------------------------------------------------------------------------------------------------|---------------------|
| [X509Certificate](https://developer.android.com/reference/kotlin/java/security/cert/X509Certificate.html#)! | the X509Certificate |

### getPrivateKey

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPrivateKey(): PrivateKey!
```

Returns the PrivateKey.

| Return ||
|----------------------------------------------------------------------------------------------|----------------|
| [PrivateKey](https://developer.android.com/reference/kotlin/java/security/PrivateKey.html#)! | the PrivateKey |

### isDestroyed

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isDestroyed(): Boolean
```

Determines if the references to the X.509 certificate and private key in this object have been cleared.

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if X509Certificate and the PrivateKey are null |
