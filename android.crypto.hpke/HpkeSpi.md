# HpkeSpi

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# HpkeSpi

Kotlin| [Java](https://developer.android.com/reference/android/crypto/hpke/HpkeSpi "View this page in Java") 

```
interface HpkeSpi
```

| [android.crypto.hpke.HpkeSpi](https://developer.android.com/reference/kotlin/android/crypto/hpke/HpkeSpi#) |

Service Provider Interface for HPKE client API classes to communicate with implementations of HPKE as described in RFC 9180.

There are no standard Java Cryptography Architecture names or interface classes for HPKE, but instances of this class can be obtained by calling`Provider.getService("ConscryptHpke", String SuiteName)`where`suiteName`is the name of the HPKE suite, e.g.`"DHKEM_X25519_HKDF_SHA256/HKDF_SHA256/AES_128_GCM"`.

## Summary

| Public methods ||
|-------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html) | [engineExport](https://developer.android.com/reference/kotlin/android/crypto/hpke/HpkeSpi#engineExport(kotlin.Int,%20kotlin.ByteArray))`(`length:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `context:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)?`)` Exports secret key material from this SPI as described in RFC 9180. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [engineInitRecipient](https://developer.android.com/reference/kotlin/android/crypto/hpke/HpkeSpi#engineInitRecipient(kotlin.ByteArray,%20java.security.PrivateKey,%20kotlin.ByteArray,%20java.security.PublicKey,%20kotlin.ByteArray,%20kotlin.ByteArray))`(`encapsulated:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)`, `recipientKey:` ` [PrivateKey](https://developer.android.com/reference/kotlin/java/security/PrivateKey.html#)`, `info:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)?`, `senderKey:` ` [PublicKey](https://developer.android.com/reference/kotlin/java/security/PublicKey.html#)?`, `psk:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)?`, `psk_id:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)?`)` Initialises an HPKE SPI in one of the recipient modes described in RFC 9180. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [engineInitSender](https://developer.android.com/reference/kotlin/android/crypto/hpke/HpkeSpi#engineInitSender(java.security.PublicKey,%20kotlin.ByteArray,%20java.security.PrivateKey,%20kotlin.ByteArray,%20kotlin.ByteArray))`(`recipientKey:` ` [PublicKey](https://developer.android.com/reference/kotlin/java/security/PublicKey.html#)`, `info:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)?`, `senderKey:` ` [PrivateKey](https://developer.android.com/reference/kotlin/java/security/PrivateKey.html#)?`, `psk:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)?`, `psk_id:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)?`)` Initialises an HPKE SPI in one of the sender modes described in RFC 9180. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [engineInitSenderWithSeed](https://developer.android.com/reference/kotlin/android/crypto/hpke/HpkeSpi#engineInitSenderWithSeed(java.security.PublicKey,%20kotlin.ByteArray,%20java.security.PrivateKey,%20kotlin.ByteArray,%20kotlin.ByteArray,%20kotlin.ByteArray))`(`recipientKey:` ` [PublicKey](https://developer.android.com/reference/kotlin/java/security/PublicKey.html#)`, `info:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)?`, `senderKey:` ` [PrivateKey](https://developer.android.com/reference/kotlin/java/security/PrivateKey.html#)?`, `psk:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)?`, `psk_id:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)?`, `sKe:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)`)` Initialises an HPKE SPI in one of the sender modes described in RFC 9180 with a predefined random seed to allow testing against known test vectors. |
| abstract [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html) | [engineOpen](https://developer.android.com/reference/kotlin/android/crypto/hpke/HpkeSpi#engineOpen(kotlin.ByteArray,%20kotlin.ByteArray))`(`ciphertext:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)`, `aad:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)?`)` Opens a message, using the internal key schedule maintained by an HPKE recipient SPI. |
| abstract [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html) | [engineSeal](https://developer.android.com/reference/kotlin/android/crypto/hpke/HpkeSpi#engineSeal(kotlin.ByteArray,%20kotlin.ByteArray))`(`plaintext:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)`, `aad:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)?`)` Seals a message, using the internal key schedule maintained by an HPKE sender SPI. |
| abstract [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html) | [getEncapsulated](https://developer.android.com/reference/kotlin/android/crypto/hpke/HpkeSpi#getEncapsulated())`()` Returns the encapsulated key material for an HPKE sender. |

## Public methods

### engineExport

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun engineExport(
    length: Int, 
    context: ByteArray?
): ByteArray
```

Exports secret key material from this SPI as described in RFC 9180.

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------------------------------|
| `length` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):expected output length |
| `context` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)?:optional context string, may be null or empty |

| Return ||
|-----------------------------------------------------------------------------------------|--------------------------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html) | exported value This value cannot be`null`. |

| Exceptions ||
|--------------------------------------|-----------------------------------------------|
| `java.lang.IllegalArgumentException` | if the length is not valid for the KDF in use |
| `java.lang.IllegalStateException` | if this SPI has not been initialised |

### engineInitRecipient

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun engineInitRecipient(
    encapsulated: ByteArray, 
    recipientKey: PrivateKey, 
    info: ByteArray?, 
    senderKey: PublicKey?, 
    psk: ByteArray?, 
    psk_id: ByteArray?
): Unit
```

Initialises an HPKE SPI in one of the recipient modes described in RFC 9180.

If`senderKey`is supplied then Asymmetric Key Authentication will be used, (MODE_AUTH)

If`psk`and`psk_id`are supplied then Pre-Shared Key Authentication will be used (MODE_PSK).

If all of`senderKey`,`psk`and`psk_id`are supplied then both Key and PSK authentication will be used (MODE_AUTH_PSK).

If neither is supplied then no sender authentication will be used (MODE_BASE).

Note that only base mode is currently supported on Android.

Public and private keys must be supplied in a format that can be used by the implementation. An instance of the`"XDH"` [java.security.KeyFactory](https://developer.android.com/reference/kotlin/java/security/KeyFactory.html#) can be used to translate`KeySpecs`or keys from another [java.security.Provider](https://developer.android.com/reference/kotlin/java/security/Provider.html#)

| Parameters ||
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `encapsulated` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html):encapsulated ephemeral key from a sender This value cannot be`null`. |
| `recipientKey` | [PrivateKey](https://developer.android.com/reference/kotlin/java/security/PrivateKey.html#):private key of the recipient This value cannot be`null`. |
| `info` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)?:application-supplied information, may be null or empty |
| `senderKey` | [PublicKey](https://developer.android.com/reference/kotlin/java/security/PublicKey.html#)?:public key of sender, for asymmetric auth modes only, else null |
| `psk` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)?:pre-shared key, for PSK auth modes only, else null |
| `psk_id` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)?:pre-shared key ID, for PSK auth modes only, else null |

| Exceptions ||
|-------------------------------------------|------------------------------------------------------------------------------------------------|
| `java.security.InvalidKeyException` | if recipientKey is null or an unsupported key format or senderKey is an unsupported key format |
| `java.lang.UnsupportedOperationException` | if the mode is not supported by this implementation |
| `java.lang.IllegalStateException` | if this SPI has already been initialised |

### engineInitSender

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun engineInitSender(
    recipientKey: PublicKey, 
    info: ByteArray?, 
    senderKey: PrivateKey?, 
    psk: ByteArray?, 
    psk_id: ByteArray?
): Unit
```

Initialises an HPKE SPI in one of the sender modes described in RFC 9180.

If`senderKey`is supplied then Asymmetric Key Authentication will be used, (MODE_AUTH)

If`psk`and`psk_id`are supplied then Pre-Shared Key Authentication will be used (MODE_PSK).

If all of`senderKey`,`psk`and`psk_id`are supplied then both Key and PSK authentication will be used (MODE_AUTH_PSK).

If neither is supplied then no sender authentication will be used (MODE_BASE).

Note that only base mode is currently supported on Android.

Public and private keys must be supplied in a format that can be used by the implementation. An instance of the`"XDH"` [java.security.KeyFactory](https://developer.android.com/reference/kotlin/java/security/KeyFactory.html#) can be used to translate`KeySpecs`or keys from another [java.security.Provider](https://developer.android.com/reference/kotlin/java/security/Provider.html#)

| Parameters ||
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `recipientKey` | [PublicKey](https://developer.android.com/reference/kotlin/java/security/PublicKey.html#):public key of the recipient This value cannot be`null`. |
| `info` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)?:application-supplied information, may be null or empty |
| `senderKey` | [PrivateKey](https://developer.android.com/reference/kotlin/java/security/PrivateKey.html#)?:private key of the sender, for symmetric auth modes only, else null |
| `psk` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)?:pre-shared key, for PSK auth modes only, else null |
| `psk_id` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)?:pre-shared key ID, for PSK auth modes only, else null |

| Exceptions ||
|-------------------------------------------|------------------------------------------------------|
| `java.security.InvalidKeyException` | if recipientKey is null or an unsupported key format |
| `java.lang.UnsupportedOperationException` | if the mode is not supported by this implementation |
| `java.lang.IllegalStateException` | if this SPI has already been initialised |

### engineInitSenderWithSeed

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun engineInitSenderWithSeed(
    recipientKey: PublicKey, 
    info: ByteArray?, 
    senderKey: PrivateKey?, 
    psk: ByteArray?, 
    psk_id: ByteArray?, 
    sKe: ByteArray
): Unit
```

Initialises an HPKE SPI in one of the sender modes described in RFC 9180 with a predefined random seed to allow testing against known test vectors.

This mode provides absolutely no security and should only be used for testing purposes.

If`senderKey`is supplied then Asymmetric Key Authentication will be used, (MODE_AUTH)

If`psk`and`psk_id`are supplied then Pre-Shared Key Authentication will be used (MODE_PSK).

If all of`senderKey`,`psk`and`psk_id`are supplied then both Key and PSK authentication will be used (MODE_AUTH_PSK).

If neither is supplied then no sender authentication will be used (MODE_BASE).

Note that only base mode is currently supported on Android.

Public and private keys must be supplied in a format that can be used by the implementation. An instance of the`"XDH"` [java.security.KeyFactory](https://developer.android.com/reference/kotlin/java/security/KeyFactory.html#) can be used to translate`KeySpecs`or keys from another [java.security.Provider](https://developer.android.com/reference/kotlin/java/security/Provider.html#)

| Parameters ||
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `recipientKey` | [PublicKey](https://developer.android.com/reference/kotlin/java/security/PublicKey.html#):public key of the recipient This value cannot be`null`. |
| `info` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)?:application-supplied information, may be null or empty |
| `senderKey` | [PrivateKey](https://developer.android.com/reference/kotlin/java/security/PrivateKey.html#)?:private key of the sender, for symmetric auth modes only, else null |
| `psk` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)?:pre-shared key, for PSK auth modes only, else null |
| `psk_id` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)?:pre-shared key ID, for PSK auth modes only, else null |
| `sKe` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html):Predetermined random seed, should only be used for validation against known test vectors This value cannot be`null`. |

| Exceptions ||
|-------------------------------------------|------------------------------------------------------------------------------------------------|
| `java.security.InvalidKeyException` | if recipientKey is null or an unsupported key format or senderKey is an unsupported key format |
| `java.lang.UnsupportedOperationException` | if the mode is not supported by this implementation |
| `java.lang.IllegalStateException` | if this SPI has already been initialised |

### engineOpen

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun engineOpen(
    ciphertext: ByteArray, 
    aad: ByteArray?
): ByteArray
```

Opens a message, using the internal key schedule maintained by an HPKE recipient SPI.

| Parameters ||
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| `ciphertext` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html):the ciphertext This value cannot be`null`. |
| `aad` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)?:optional associated data, may be null or empty |

| Return ||
|-----------------------------------------------------------------------------------------|-------------------------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html) | the plaintext This value cannot be`null`. |

| Exceptions ||
|------------------------------------------|---------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | if this SPI has not been initialised or if it was initialised as a sender |
| `java.security.GeneralSecurityException` | on decryption failures |

### engineSeal

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun engineSeal(
    plaintext: ByteArray, 
    aad: ByteArray?
): ByteArray
```

Seals a message, using the internal key schedule maintained by an HPKE sender SPI.

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| `plaintext` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html):the plaintext This value cannot be`null`. |
| `aad` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)?:optional associated data, may be null or empty |

| Return ||
|-----------------------------------------------------------------------------------------|--------------------------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html) | the ciphertext This value cannot be`null`. |

| Exceptions ||
|-----------------------------------|------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if the plaintext is null |
| `java.lang.IllegalStateException` | if this SPI has not been initialised or if it was initialised as a recipient |

### getEncapsulated

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getEncapsulated(): ByteArray
```

Returns the encapsulated key material for an HPKE sender.

| Return ||
|-----------------------------------------------------------------------------------------|----------------------------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html) | the key material This value cannot be`null`. |

| Exceptions ||
|-----------------------------------|------------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | if this SPI has not been initialised or if it was initialised as a recipient |
