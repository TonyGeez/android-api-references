# KeyPair

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# KeyPair

```
class KeyPair : Serializable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.security.KeyPair](../java/security/KeyPair.md) |

This class is a simple holder for a key pair (a public key and a private key). It does not enforce any security, and, when initialized, should be treated like a PrivateKey.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [KeyPair](../java/security/KeyPair.md))`(`publicKey:` ` [PublicKey](../java/security/PublicKey.md)!`, `privateKey:` ` [PrivateKey](../java/security/PrivateKey.md)!`)` Constructs a key pair from the given public key and private key. |

| Public methods ||
|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [PrivateKey](../java/security/PrivateKey.md)! | [getPrivate](../java/security/KeyPair.md))`()` Returns a reference to the private key component of this key pair. |
| [PublicKey](../java/security/PublicKey.md)! | [getPublic](../java/security/KeyPair.md))`()` Returns a reference to the public key component of this key pair. |

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
| `publicKey` | [PublicKey](../java/security/PublicKey.md)!:the public key. |
| `privateKey` | [PrivateKey](../java/security/PrivateKey.md)!:the private key. |

## Public methods

### getPrivate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPrivate(): PrivateKey!
```

Returns a reference to the private key component of this key pair.

| Return ||
|----------------------------------------------------------------------------------------|---------------------------------|
| [PrivateKey](../java/security/PrivateKey.md)! | a reference to the private key. |

### getPublic

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPublic(): PublicKey!
```

Returns a reference to the public key component of this key pair.

| Return ||
|--------------------------------------------------------------------------------------|--------------------------------|
| [PublicKey](../java/security/PublicKey.md)! | a reference to the public key. |
