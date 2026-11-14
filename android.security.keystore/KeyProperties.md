# KeyProperties

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# KeyProperties

Kotlin| [Java](KeyProperties.md) 
| --- | --- |

```
abstract class KeyProperties
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.security.keystore.KeyProperties](KeyProperties.md) |

Properties of [Android Keystore](https://developer.android.com/training/articles/keystore.html) keys.

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [AUTH_BIOMETRIC_STRONG](KeyProperties.md) Any biometric (e.g. fingerprint, iris, or face) on the device that meets or exceeds the requirements for |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [AUTH_DEVICE_CREDENTIAL](KeyProperties.md) The non-biometric credential used to secure the device (i.e., PIN, pattern, or password) |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [BLOCK_MODE_CBC](KeyProperties.md) Cipher Block Chaining (CBC) block mode. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [BLOCK_MODE_CTR](KeyProperties.md) Counter (CTR) block mode. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [BLOCK_MODE_ECB](KeyProperties.md) Electronic Codebook (ECB) block mode. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [BLOCK_MODE_GCM](KeyProperties.md) Galois/Counter Mode (GCM) block mode. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [DIGEST_MD5](KeyProperties.md) MD5 digest. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [DIGEST_NONE](KeyProperties.md) No digest: sign/authenticate the raw message. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [DIGEST_SHA1](KeyProperties.md) SHA-1 digest. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [DIGEST_SHA224](KeyProperties.md) SHA-2 224 (aka SHA-224) digest. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [DIGEST_SHA256](KeyProperties.md) SHA-2 256 (aka SHA-256) digest. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [DIGEST_SHA384](KeyProperties.md) SHA-2 384 (aka SHA-384) digest. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [DIGEST_SHA512](KeyProperties.md) SHA-2 512 (aka SHA-512) digest. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ENCRYPTION_PADDING_NONE](KeyProperties.md) No encryption padding. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ENCRYPTION_PADDING_PKCS7](KeyProperties.md) PKCS#7 encryption padding scheme. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ENCRYPTION_PADDING_RSA_OAEP](KeyProperties.md) RSA Optimal Asymmetric Encryption Padding (OAEP) scheme. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ENCRYPTION_PADDING_RSA_PKCS1](KeyProperties.md) RSA PKCS#1 v1. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [KEY_ALGORITHM_3DES](KeyProperties.md) Triple Data Encryption Algorithm (3DES) key. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [KEY_ALGORITHM_AES](KeyProperties.md) Advanced Encryption Standard (AES) key. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [KEY_ALGORITHM_EC](KeyProperties.md) Elliptic Curve (EC) Cryptography key. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [KEY_ALGORITHM_HMAC_SHA1](KeyProperties.md) Keyed-Hash Message Authentication Code (HMAC) key using SHA-1 as the hash. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [KEY_ALGORITHM_HMAC_SHA224](KeyProperties.md) Keyed-Hash Message Authentication Code (HMAC) key using SHA-224 as the hash. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [KEY_ALGORITHM_HMAC_SHA256](KeyProperties.md) Keyed-Hash Message Authentication Code (HMAC) key using SHA-256 as the hash. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [KEY_ALGORITHM_HMAC_SHA384](KeyProperties.md) Keyed-Hash Message Authentication Code (HMAC) key using SHA-384 as the hash. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [KEY_ALGORITHM_HMAC_SHA512](KeyProperties.md) Keyed-Hash Message Authentication Code (HMAC) key using SHA-512 as the hash. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [KEY_ALGORITHM_RSA](KeyProperties.md) Rivest Shamir Adleman (RSA) key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ORIGIN_GENERATED](KeyProperties.md) Key was generated inside AndroidKeyStore. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ORIGIN_IMPORTED](KeyProperties.md) Key was imported into AndroidKeyStore. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ORIGIN_SECURELY_IMPORTED](KeyProperties.md) Key was imported into the AndroidKeyStore in an encrypted wrapper. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ORIGIN_UNKNOWN](KeyProperties.md) Origin of the key is unknown. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PURPOSE_AGREE_KEY](KeyProperties.md) Purpose of key: creating a shared ECDH secret through key agreement. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PURPOSE_ATTEST_KEY](KeyProperties.md) Purpose of key: Signing attestations. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PURPOSE_DECRYPT](KeyProperties.md) Purpose of key: decryption. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PURPOSE_ENCRYPT](KeyProperties.md) Purpose of key: encryption. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PURPOSE_SIGN](KeyProperties.md) Purpose of key: signing or generating a Message Authentication Code (MAC). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PURPOSE_VERIFY](KeyProperties.md) Purpose of key: signature or Message Authentication Code (MAC) verification. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PURPOSE_WRAP_KEY](KeyProperties.md) Purpose of key: wrapping and unwrapping wrapped keys for secure import. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SECURITY_LEVEL_SOFTWARE](KeyProperties.md) Indicates enforcement by system software. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SECURITY_LEVEL_STRONGBOX](KeyProperties.md) Indicates enforcement by environment meeting the Strongbox security profile, such as a secure element. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SECURITY_LEVEL_TRUSTED_ENVIRONMENT](KeyProperties.md) Indicates enforcement by a trusted execution environment. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SECURITY_LEVEL_UNKNOWN](KeyProperties.md) This security level indicates that no assumptions can be made about the security level of the respective key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SECURITY_LEVEL_UNKNOWN_SECURE](KeyProperties.md) This security level indicates that due to the target API level of the caller no exact statement can be made about the security level of the key, however, the security level can be considered is at least equivalent to [SECURITY_LEVEL_TRUSTED_ENVIRONMENT](KeyProperties.md). |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SIGNATURE_PADDING_RSA_PKCS1](KeyProperties.md) RSA PKCS#1 v1. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SIGNATURE_PADDING_RSA_PSS](KeyProperties.md) RSA PKCS#1 v2. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [UNRESTRICTED_USAGE_COUNT](KeyProperties.md) This value indicates that there is no restriction on the number of times the key can be used. |
| --- | --- |

## Constants

### AUTH_BIOMETRIC_STRONG

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val AUTH_BIOMETRIC_STRONG: Int
```

Any biometric (e.g. fingerprint, iris, or face) on the device that meets or exceeds the requirements for**Strong**, as defined by the Android CDD. 

 Value: 2

### AUTH_DEVICE_CREDENTIAL

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val AUTH_DEVICE_CREDENTIAL: Int
```

The non-biometric credential used to secure the device (i.e., PIN, pattern, or password) 

 Value: 1

### BLOCK_MODE_CBC

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BLOCK_MODE_CBC: String
```

Cipher Block Chaining (CBC) block mode. 

 Value: "CBC"

### BLOCK_MODE_CTR

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BLOCK_MODE_CTR: String
```

Counter (CTR) block mode. 

 Value: "CTR"

### BLOCK_MODE_ECB

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BLOCK_MODE_ECB: String
```

Electronic Codebook (ECB) block mode. 

 Value: "ECB"

### BLOCK_MODE_GCM

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BLOCK_MODE_GCM: String
```

Galois/Counter Mode (GCM) block mode. 

 Value: "GCM"

### DIGEST_MD5

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DIGEST_MD5: String
```

MD5 digest. 

 Value: "MD5"

### DIGEST_NONE

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DIGEST_NONE: String
```

No digest: sign/authenticate the raw message. 

 Value: "NONE"

### DIGEST_SHA1

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DIGEST_SHA1: String
```

SHA-1 digest. 

 Value: "SHA-1"

### DIGEST_SHA224

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DIGEST_SHA224: String
```

SHA-2 224 (aka SHA-224) digest. 

 Value: "SHA-224"

### DIGEST_SHA256

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DIGEST_SHA256: String
```

SHA-2 256 (aka SHA-256) digest. 

 Value: "SHA-256"

### DIGEST_SHA384

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DIGEST_SHA384: String
```

SHA-2 384 (aka SHA-384) digest. 

 Value: "SHA-384"

### DIGEST_SHA512

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DIGEST_SHA512: String
```

SHA-2 512 (aka SHA-512) digest. 

 Value: "SHA-512"

### ENCRYPTION_PADDING_NONE

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ENCRYPTION_PADDING_NONE: String
```

No encryption padding. 

 Value: "NoPadding"

### ENCRYPTION_PADDING_PKCS7

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ENCRYPTION_PADDING_PKCS7: String
```

PKCS#7 encryption padding scheme. 

 Value: "PKCS7Padding"

### ENCRYPTION_PADDING_RSA_OAEP

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ENCRYPTION_PADDING_RSA_OAEP: String
```

RSA Optimal Asymmetric Encryption Padding (OAEP) scheme. 

 Value: "OAEPPadding"

### ENCRYPTION_PADDING_RSA_PKCS1

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ENCRYPTION_PADDING_RSA_PKCS1: String
```

RSA PKCS#1 v1.5 padding scheme for encryption. 

 Value: "PKCS1Padding"

### KEY_ALGORITHM_3DES

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val KEY_ALGORITHM_3DES: String
```

**Deprecated:** *Included for interoperability with legacy systems. Prefer [android.security.keystore.KeyProperties#KEY_ALGORITHM_AES](KeyProperties.md) for new development.*

Triple Data Encryption Algorithm (3DES) key. 

 Value: "DESede"

### KEY_ALGORITHM_AES

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val KEY_ALGORITHM_AES: String
```

Advanced Encryption Standard (AES) key. 

 Value: "AES"

### KEY_ALGORITHM_EC

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val KEY_ALGORITHM_EC: String
```

Elliptic Curve (EC) Cryptography key. 

 Value: "EC"

### KEY_ALGORITHM_HMAC_SHA1

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val KEY_ALGORITHM_HMAC_SHA1: String
```

Keyed-Hash Message Authentication Code (HMAC) key using SHA-1 as the hash. 

 Value: "HmacSHA1"

### KEY_ALGORITHM_HMAC_SHA224

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val KEY_ALGORITHM_HMAC_SHA224: String
```

Keyed-Hash Message Authentication Code (HMAC) key using SHA-224 as the hash. 

 Value: "HmacSHA224"

### KEY_ALGORITHM_HMAC_SHA256

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val KEY_ALGORITHM_HMAC_SHA256: String
```

Keyed-Hash Message Authentication Code (HMAC) key using SHA-256 as the hash. 

 Value: "HmacSHA256"

### KEY_ALGORITHM_HMAC_SHA384

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val KEY_ALGORITHM_HMAC_SHA384: String
```

Keyed-Hash Message Authentication Code (HMAC) key using SHA-384 as the hash. 

 Value: "HmacSHA384"

### KEY_ALGORITHM_HMAC_SHA512

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val KEY_ALGORITHM_HMAC_SHA512: String
```

Keyed-Hash Message Authentication Code (HMAC) key using SHA-512 as the hash. 

 Value: "HmacSHA512"

### KEY_ALGORITHM_RSA

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val KEY_ALGORITHM_RSA: String
```

Rivest Shamir Adleman (RSA) key. 

 Value: "RSA"

### ORIGIN_GENERATED

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ORIGIN_GENERATED: Int
```

Key was generated inside AndroidKeyStore. 

 Value: 1

### ORIGIN_IMPORTED

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ORIGIN_IMPORTED: Int
```

Key was imported into AndroidKeyStore. 

 Value: 2

### ORIGIN_SECURELY_IMPORTED

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ORIGIN_SECURELY_IMPORTED: Int
```

Key was imported into the AndroidKeyStore in an encrypted wrapper. Unlike imported keys, securely imported keys can be imported without appearing as plaintext in the device's host memory. 

 Value: 8

### ORIGIN_UNKNOWN

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ORIGIN_UNKNOWN: Int
```

Origin of the key is unknown. This can occur only for keys backed by an old TEE-backed implementation which does not record origin information. 

 Value: 4

### PURPOSE_AGREE_KEY

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PURPOSE_AGREE_KEY: Int
```

Purpose of key: creating a shared ECDH secret through key agreement.

A key having this purpose can be combined with the elliptic curve public key of another party to establish a shared secret over an insecure channel. It should be used as a parameter to [javax.crypto.KeyAgreement#init(java.security.Key)](../javax.crypto/KeyAgreement.md))(a complete example is available [here](KeyGenParameterSpec.md)). See [this article](https://en.wikipedia.org/wiki/Elliptic-curve_Diffie%E2%80%93Hellman) for a more detailed explanation. 

 Value: 64

### PURPOSE_ATTEST_KEY

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PURPOSE_ATTEST_KEY: Int
```

Purpose of key: Signing attestations. This purpose is incompatible with all others, meaning that when generating a key with PURPOSE_ATTEST_KEY, no other purposes may be specified. In addition, PURPOSE_ATTEST_KEY may not be specified for imported keys. 

 Value: 128

### PURPOSE_DECRYPT

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PURPOSE_DECRYPT: Int
```

Purpose of key: decryption. 

 Value: 2

### PURPOSE_ENCRYPT

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PURPOSE_ENCRYPT: Int
```

Purpose of key: encryption. 

 Value: 1

### PURPOSE_SIGN

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PURPOSE_SIGN: Int
```

Purpose of key: signing or generating a Message Authentication Code (MAC). 

 Value: 4

### PURPOSE_VERIFY

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PURPOSE_VERIFY: Int
```

Purpose of key: signature or Message Authentication Code (MAC) verification. 

 Value: 8

### PURPOSE_WRAP_KEY

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PURPOSE_WRAP_KEY: Int
```

Purpose of key: wrapping and unwrapping wrapped keys for secure import. 

 Value: 32

### SECURITY_LEVEL_SOFTWARE

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SECURITY_LEVEL_SOFTWARE: Int
```

Indicates enforcement by system software. 

 Value: 0

### SECURITY_LEVEL_STRONGBOX

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SECURITY_LEVEL_STRONGBOX: Int
```

Indicates enforcement by environment meeting the Strongbox security profile, such as a secure element. 

 Value: 2

### SECURITY_LEVEL_TRUSTED_ENVIRONMENT

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SECURITY_LEVEL_TRUSTED_ENVIRONMENT: Int
```

Indicates enforcement by a trusted execution environment. 

 Value: 1

### SECURITY_LEVEL_UNKNOWN

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SECURITY_LEVEL_UNKNOWN: Int
```

This security level indicates that no assumptions can be made about the security level of the respective key. 

 Value: -2

### SECURITY_LEVEL_UNKNOWN_SECURE

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SECURITY_LEVEL_UNKNOWN_SECURE: Int
```

This security level indicates that due to the target API level of the caller no exact statement can be made about the security level of the key, however, the security level can be considered is at least equivalent to [SECURITY_LEVEL_TRUSTED_ENVIRONMENT](KeyProperties.md). 

 Value: -1

### SIGNATURE_PADDING_RSA_PKCS1

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SIGNATURE_PADDING_RSA_PKCS1: String
```

RSA PKCS#1 v1.5 padding for signatures. 

 Value: "PKCS1"

### SIGNATURE_PADDING_RSA_PSS

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SIGNATURE_PADDING_RSA_PSS: String
```

RSA PKCS#1 v2.1 Probabilistic Signature Scheme (PSS) padding. 

 Value: "PSS"

### UNRESTRICTED_USAGE_COUNT

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val UNRESTRICTED_USAGE_COUNT: Int
```

This value indicates that there is no restriction on the number of times the key can be used. 

 Value: -1
