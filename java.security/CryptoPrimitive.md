# CryptoPrimitive

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CryptoPrimitive

```
class CryptoPrimitive
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [kotlin.Enum](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-enum/index.html)\< [java.security.CryptoPrimitive](https://developer.android.com/reference/kotlin/java/security/CryptoPrimitive#)\> ||
| | ↳ | [java.security.CryptoPrimitive](https://developer.android.com/reference/kotlin/java/security/CryptoPrimitive#) |

| Known Direct Subclasses [CryptoPrimitive.BLOCK_CIPHER](https://developer.android.com/reference/kotlin/java/security/CryptoPrimitive#ENUM_VALUE:BLOCK_CIPHER), [CryptoPrimitive.KEY_AGREEMENT](https://developer.android.com/reference/kotlin/java/security/CryptoPrimitive#ENUM_VALUE:KEY_AGREEMENT), [CryptoPrimitive.KEY_ENCAPSULATION](https://developer.android.com/reference/kotlin/java/security/CryptoPrimitive#ENUM_VALUE:KEY_ENCAPSULATION), [CryptoPrimitive.KEY_WRAP](https://developer.android.com/reference/kotlin/java/security/CryptoPrimitive#ENUM_VALUE:KEY_WRAP), [CryptoPrimitive.MAC](https://developer.android.com/reference/kotlin/java/security/CryptoPrimitive#ENUM_VALUE:MAC), [CryptoPrimitive.MESSAGE_DIGEST](https://developer.android.com/reference/kotlin/java/security/CryptoPrimitive#ENUM_VALUE:MESSAGE_DIGEST), [CryptoPrimitive.PUBLIC_KEY_ENCRYPTION](https://developer.android.com/reference/kotlin/java/security/CryptoPrimitive#ENUM_VALUE:PUBLIC_KEY_ENCRYPTION), [CryptoPrimitive.SECURE_RANDOM](https://developer.android.com/reference/kotlin/java/security/CryptoPrimitive#ENUM_VALUE:SECURE_RANDOM), [CryptoPrimitive.SIGNATURE](https://developer.android.com/reference/kotlin/java/security/CryptoPrimitive#ENUM_VALUE:SIGNATURE), [CryptoPrimitive.STREAM_CIPHER](https://developer.android.com/reference/kotlin/java/security/CryptoPrimitive#ENUM_VALUE:STREAM_CIPHER) |--------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------| | [CryptoPrimitive.BLOCK_CIPHER](https://developer.android.com/reference/kotlin/java/security/CryptoPrimitive#ENUM_VALUE:BLOCK_CIPHER) | Symmetric primitive: block cipher | | [CryptoPrimitive.KEY_AGREEMENT](https://developer.android.com/reference/kotlin/java/security/CryptoPrimitive#ENUM_VALUE:KEY_AGREEMENT) | Asymmetric primitive: key agreement and key distribution | | [CryptoPrimitive.KEY_ENCAPSULATION](https://developer.android.com/reference/kotlin/java/security/CryptoPrimitive#ENUM_VALUE:KEY_ENCAPSULATION) | Asymmetric primitive: key encapsulation mechanism | | [CryptoPrimitive.KEY_WRAP](https://developer.android.com/reference/kotlin/java/security/CryptoPrimitive#ENUM_VALUE:KEY_WRAP) | Symmetric primitive: key wrap | | [CryptoPrimitive.MAC](https://developer.android.com/reference/kotlin/java/security/CryptoPrimitive#ENUM_VALUE:MAC) | Symmetric primitive: message authentication code | | [CryptoPrimitive.MESSAGE_DIGEST](https://developer.android.com/reference/kotlin/java/security/CryptoPrimitive#ENUM_VALUE:MESSAGE_DIGEST) | Hash function | | [CryptoPrimitive.PUBLIC_KEY_ENCRYPTION](https://developer.android.com/reference/kotlin/java/security/CryptoPrimitive#ENUM_VALUE:PUBLIC_KEY_ENCRYPTION) | Asymmetric primitive: public key encryption | | [CryptoPrimitive.SECURE_RANDOM](https://developer.android.com/reference/kotlin/java/security/CryptoPrimitive#ENUM_VALUE:SECURE_RANDOM) | Cryptographic random number generator | | [CryptoPrimitive.SIGNATURE](https://developer.android.com/reference/kotlin/java/security/CryptoPrimitive#ENUM_VALUE:SIGNATURE) | Asymmetric primitive: signature scheme | | [CryptoPrimitive.STREAM_CIPHER](https://developer.android.com/reference/kotlin/java/security/CryptoPrimitive#ENUM_VALUE:STREAM_CIPHER) | Symmetric primitive: stream cipher | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

An enumeration of cryptographic primitives.

## Summary

| Enum values ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [BLOCK_CIPHER](https://developer.android.com/reference/kotlin/java/security/CryptoPrimitive#ENUM_VALUE:BLOCK_CIPHER) Symmetric primitive: block cipher |
| [KEY_AGREEMENT](https://developer.android.com/reference/kotlin/java/security/CryptoPrimitive#ENUM_VALUE:KEY_AGREEMENT) Asymmetric primitive: key agreement and key distribution |
| [KEY_ENCAPSULATION](https://developer.android.com/reference/kotlin/java/security/CryptoPrimitive#ENUM_VALUE:KEY_ENCAPSULATION) Asymmetric primitive: key encapsulation mechanism |
| [KEY_WRAP](https://developer.android.com/reference/kotlin/java/security/CryptoPrimitive#ENUM_VALUE:KEY_WRAP) Symmetric primitive: key wrap |
| [MAC](https://developer.android.com/reference/kotlin/java/security/CryptoPrimitive#ENUM_VALUE:MAC) Symmetric primitive: message authentication code |
| [MESSAGE_DIGEST](https://developer.android.com/reference/kotlin/java/security/CryptoPrimitive#ENUM_VALUE:MESSAGE_DIGEST) Hash function |
| [PUBLIC_KEY_ENCRYPTION](https://developer.android.com/reference/kotlin/java/security/CryptoPrimitive#ENUM_VALUE:PUBLIC_KEY_ENCRYPTION) Asymmetric primitive: public key encryption |
| [SECURE_RANDOM](https://developer.android.com/reference/kotlin/java/security/CryptoPrimitive#ENUM_VALUE:SECURE_RANDOM) Cryptographic random number generator |
| [SIGNATURE](https://developer.android.com/reference/kotlin/java/security/CryptoPrimitive#ENUM_VALUE:SIGNATURE) Asymmetric primitive: signature scheme |
| [STREAM_CIPHER](https://developer.android.com/reference/kotlin/java/security/CryptoPrimitive#ENUM_VALUE:STREAM_CIPHER) Symmetric primitive: stream cipher |

## Enum values

### BLOCK_CIPHER

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val BLOCK_CIPHER : CryptoPrimitive
```

Symmetric primitive: block cipher 

### KEY_AGREEMENT

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val KEY_AGREEMENT : CryptoPrimitive
```

Asymmetric primitive: key agreement and key distribution 

### KEY_ENCAPSULATION

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val KEY_ENCAPSULATION : CryptoPrimitive
```

Asymmetric primitive: key encapsulation mechanism 

### KEY_WRAP

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val KEY_WRAP : CryptoPrimitive
```

Symmetric primitive: key wrap 

### MAC

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val MAC : CryptoPrimitive
```

Symmetric primitive: message authentication code 

### MESSAGE_DIGEST

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val MESSAGE_DIGEST : CryptoPrimitive
```

Hash function 

### PUBLIC_KEY_ENCRYPTION

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val PUBLIC_KEY_ENCRYPTION : CryptoPrimitive
```

Asymmetric primitive: public key encryption 

### SECURE_RANDOM

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val SECURE_RANDOM : CryptoPrimitive
```

Cryptographic random number generator 

### SIGNATURE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val SIGNATURE : CryptoPrimitive
```

Asymmetric primitive: signature scheme 

### STREAM_CIPHER

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val STREAM_CIPHER : CryptoPrimitive
```

Symmetric primitive: stream cipher
