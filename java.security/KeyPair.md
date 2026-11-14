# KeyPair

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# KeyPair

```
class KeyPair : Serializable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.security.KeyPair](https://developer.android.com/reference/kotlin/java/security/KeyPair#) |

This class is a simple holder for a key pair (a public key and a private key). It does not enforce any security, and, when initialized, should be treated like a PrivateKey.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [KeyPair](https://developer.android.com/reference/kotlin/java/security/KeyPair#KeyPair(java.security.PublicKey,%20java.security.PrivateKey))`(`publicKey:` ` [PublicKey](https://developer.android.com/reference/kotlin/java/security/PublicKey)!`, `privateKey:` ` [PrivateKey](https://developer.android.com/reference/kotlin/java/security/PrivateKey)!`)` Constructs a key pair from the given public key and private key. |

| Public methods ||
|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [PrivateKey](https://developer.android.com/reference/kotlin/java/security/PrivateKey)! | [getPrivate](https://developer.android.com/reference/kotlin/java/security/KeyPair#getPrivate())`()` Returns a reference to the private key component of this key pair. |
| [PublicKey](https://developer.android.com/reference/kotlin/java/security/PublicKey)! | [getPublic](https://developer.android.com/reference/kotlin/java/security/KeyPair#getPublic())`()` Returns a reference to the public key component of this key pair. |

## Public constructors

### KeyPair

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
KeyPair(
    publicKey: PublicKey!, 
    privateKey: PrivateKey!)
```

Constructs a key pair from the given public key and private key.

Note that this constructor only stores references to the public and private key components in the generated key pair. This is safe, because`Key`objects are immutable.

| Parameters ||
|--------------|---------------------------------------------------------------------------------------------------------|
| `publicKey` | [PublicKey](https://developer.android.com/reference/kotlin/java/security/PublicKey)!:the public key. |
| `privateKey` | [PrivateKey](https://developer.android.com/reference/kotlin/java/security/PrivateKey)!:the private key. |

## Public methods

### getPrivate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPrivate(): PrivateKey!
```

Returns a reference to the private key component of this key pair.

| Return ||
|----------------------------------------------------------------------------------------|---------------------------------|
| [PrivateKey](https://developer.android.com/reference/kotlin/java/security/PrivateKey)! | a reference to the private key. |

### getPublic

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPublic(): PublicKey!
```

Returns a reference to the public key component of this key pair.

| Return ||
|--------------------------------------------------------------------------------------|--------------------------------|
| [PublicKey](https://developer.android.com/reference/kotlin/java/security/PublicKey)! | a reference to the public key. |
