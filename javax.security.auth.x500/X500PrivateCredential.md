# X500PrivateCredential

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# X500PrivateCredential

```
class X500PrivateCredential : Destroyable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [javax.security.auth.x500.X500PrivateCredential](X500PrivateCredential.md) |

This class represents an`X500PrivateCredential`. It associates an X.509 certificate, corresponding private key and the KeyStore alias used to reference that exact key pair in the KeyStore. This enables looking up the private credentials for an X.500 principal in a subject.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [X500PrivateCredential](X500PrivateCredential.md))`(`cert:` ` [X509Certificate](../java.security.cert/X509Certificate.md)!`, `key:` ` [PrivateKey](../java.security/PrivateKey.md)!`)` Creates an X500PrivateCredential that associates an X. |
| [X500PrivateCredential](X500PrivateCredential.md))`(`cert:` ` [X509Certificate](../java.security.cert/X509Certificate.md)!`, `key:` ` [PrivateKey](../java.security/PrivateKey.md)!`, `alias:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Creates an X500PrivateCredential that associates an X. |

| Public methods ||
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [destroy](X500PrivateCredential.md))`()` Clears the references to the X. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getAlias](X500PrivateCredential.md))`()` Returns the KeyStore alias. |
| [X509Certificate](../java.security.cert/X509Certificate.md)! | [getCertificate](X500PrivateCredential.md))`()` Returns the X. |
| --- | --- |
| [PrivateKey](../java.security/PrivateKey.md)! | [getPrivateKey](X500PrivateCredential.md))`()` Returns the PrivateKey. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isDestroyed](X500PrivateCredential.md))`()` Determines if the references to the X. |

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
| `cert` | [X509Certificate](../java.security.cert/X509Certificate.md)!:X509Certificate |
| `key` | [PrivateKey](../java.security/PrivateKey.md)!:PrivateKey for the certificate |

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
| `cert` | [X509Certificate](../java.security.cert/X509Certificate.md)!:X509Certificate |
| `key` | [PrivateKey](../java.security/PrivateKey.md)!:PrivateKey for the certificate |
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
| [X509Certificate](../java.security.cert/X509Certificate.md)! | the X509Certificate |

### getPrivateKey

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPrivateKey(): PrivateKey!
```

Returns the PrivateKey.

| Return ||
|----------------------------------------------------------------------------------------------|----------------|
| [PrivateKey](../java.security/PrivateKey.md)! | the PrivateKey |

### isDestroyed

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isDestroyed(): Boolean
```

Determines if the references to the X.509 certificate and private key in this object have been cleared.

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if X509Certificate and the PrivateKey are null |
