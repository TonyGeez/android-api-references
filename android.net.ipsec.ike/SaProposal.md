Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SaProposal

```
abstract class SaProposal
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.net.ipsec.ike.SaProposal](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/SaProposal#) |

| Known Direct Subclasses [ChildSaProposal](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/ChildSaProposal), [IkeSaProposal](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSaProposal) |---|---| | [ChildSaProposal](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/ChildSaProposal) | ChildSaProposal represents a proposed configuration to negotiate a Child SA. | | [IkeSaProposal](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSaProposal) | IkeSaProposal represents a proposed configuration to negotiate an IKE SA. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

SaProposal represents a proposed configuration to negotiate an IKE or Child SA.

SaProposal will contain cryptograhic algorithms and key generation materials for the negotiation of an IKE or Child SA.

User must provide at least one valid SaProposal when they are creating a new IKE or Child SA.

## Summary

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/SaProposal#DH_GROUP_1024_BIT_MODP:kotlin.Int` 1024-bit MODP Diffie-Hellman Group. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/SaProposal#DH_GROUP_1536_BIT_MODP:kotlin.Int` 1536-bit MODP Diffie-Hellman Group. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/SaProposal#DH_GROUP_2048_BIT_MODP:kotlin.Int` 2048-bit MODP Diffie-Hellman Group. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/SaProposal#DH_GROUP_3072_BIT_MODP:kotlin.Int` 3072-bit MODP Diffie-Hellman Group. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/SaProposal#DH_GROUP_4096_BIT_MODP:kotlin.Int` 4096-bit MODP Diffie-Hellman Group. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/SaProposal#DH_GROUP_CURVE_25519:kotlin.Int` Elliptic Curve Diffie-Hellman 25519. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/SaProposal#DH_GROUP_NONE:kotlin.Int` None Diffie-Hellman Group. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/SaProposal#ENCRYPTION_ALGORITHM_3DES:kotlin.Int` 3DES Encryption/Ciphering Algorithm. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/SaProposal#ENCRYPTION_ALGORITHM_AES_CBC:kotlin.Int` AES-CBC Encryption/Ciphering Algorithm. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/SaProposal#ENCRYPTION_ALGORITHM_AES_CTR:kotlin.Int` AES-CTR Encryption/Ciphering Algorithm. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/SaProposal#ENCRYPTION_ALGORITHM_AES_GCM_12:kotlin.Int` AES-GCM Authentication/Integrity + Encryption/Ciphering Algorithm with 12-octet ICV (truncation). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/SaProposal#ENCRYPTION_ALGORITHM_AES_GCM_16:kotlin.Int` AES-GCM Authentication/Integrity + Encryption/Ciphering Algorithm with 16-octet ICV (truncation). |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/SaProposal#ENCRYPTION_ALGORITHM_AES_GCM_8:kotlin.Int` AES-GCM Authentication/Integrity + Encryption/Ciphering Algorithm with 8-octet ICV (truncation). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/SaProposal#ENCRYPTION_ALGORITHM_CHACHA20_POLY1305:kotlin.Int` ChaCha20-Poly1305 Authentication/Integrity + Encryption/Ciphering Algorithm with 16-octet ICV (truncation). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/SaProposal#INTEGRITY_ALGORITHM_AES_CMAC_96:kotlin.Int` AES-CMAC-96 Authentication/Integrity Algorithm. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/SaProposal#INTEGRITY_ALGORITHM_AES_XCBC_96:kotlin.Int` AES-XCBC-96 Authentication/Integrity Algorithm. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/SaProposal#INTEGRITY_ALGORITHM_HMAC_SHA1_96:kotlin.Int` HMAC-SHA1 Authentication/Integrity Algorithm. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/SaProposal#INTEGRITY_ALGORITHM_HMAC_SHA2_256_128:kotlin.Int` HMAC-SHA256 Authentication/Integrity Algorithm with 128-bit truncation. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/SaProposal#INTEGRITY_ALGORITHM_HMAC_SHA2_384_192:kotlin.Int` HMAC-SHA384 Authentication/Integrity Algorithm with 192-bit truncation. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/SaProposal#INTEGRITY_ALGORITHM_HMAC_SHA2_512_256:kotlin.Int` HMAC-SHA512 Authentication/Integrity Algorithm with 256-bit truncation. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/SaProposal#INTEGRITY_ALGORITHM_NONE:kotlin.Int` None Authentication/Integrity Algorithm. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/SaProposal#KEY_LEN_AES_128:kotlin.Int` AES Encryption/Ciphering Algorithm key length 128 bits. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/SaProposal#KEY_LEN_AES_192:kotlin.Int` AES Encryption/Ciphering Algorithm key length 192 bits. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/SaProposal#KEY_LEN_AES_256:kotlin.Int` AES Encryption/Ciphering Algorithm key length 256 bits. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/SaProposal#KEY_LEN_UNUSED:kotlin.Int` Key length unused. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/SaProposal#PSEUDORANDOM_FUNCTION_AES128_CMAC:kotlin.Int` AES128-CMAC Pseudorandom Function. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/SaProposal#PSEUDORANDOM_FUNCTION_AES128_XCBC:kotlin.Int` AES128-XCBC Pseudorandom Function. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/SaProposal#PSEUDORANDOM_FUNCTION_HMAC_SHA1:kotlin.Int` HMAC-SHA1 Pseudorandom Function. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/SaProposal#PSEUDORANDOM_FUNCTION_SHA2_256:kotlin.Int` HMAC-SHA2-256 Pseudorandom Function. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/SaProposal#PSEUDORANDOM_FUNCTION_SHA2_384:kotlin.Int` HMAC-SHA2-384 Pseudorandom Function. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/SaProposal#PSEUDORANDOM_FUNCTION_SHA2_512:kotlin.Int` HMAC-SHA2-384 Pseudorandom Function. |

| Public methods ||
|---|---|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/SaProposal#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Indicates whether some other object is "equal to" this one. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\> | `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/SaProposal#getDhGroups()()` Gets all proposed Diffie-Hellman groups |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Pair](https://developer.android.com/reference/kotlin/android/util/Pair.html#)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!, [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\>!\> | `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/SaProposal#getEncryptionAlgorithms()()` Gets all proposed encryption algorithms |
| --- | --- |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\> | `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/SaProposal#getIntegrityAlgorithms()()` Gets all proposed integrity algorithms |
| open static [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\> | `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/SaProposal#getSupportedDhGroups()()` Returns supported DH groups for IKE and Child SA proposal negotiation. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/SaProposal#hashCode()()` Returns a hash code value for the object. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/SaProposal#toString()()` Returns a string representation of the object. |

## Constants

### DH_GROUP_1024_BIT_MODP

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DH_GROUP_1024_BIT_MODP: Int
```

1024-bit MODP Diffie-Hellman Group.

 Value: 2

### DH_GROUP_1536_BIT_MODP

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DH_GROUP_1536_BIT_MODP: Int
```

1536-bit MODP Diffie-Hellman Group.

 Value: 5

### DH_GROUP_2048_BIT_MODP

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DH_GROUP_2048_BIT_MODP: Int
```

2048-bit MODP Diffie-Hellman Group.

 Value: 14

### DH_GROUP_3072_BIT_MODP

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DH_GROUP_3072_BIT_MODP: Int
```

3072-bit MODP Diffie-Hellman Group.

 Value: 15

### DH_GROUP_4096_BIT_MODP

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DH_GROUP_4096_BIT_MODP: Int
```

4096-bit MODP Diffie-Hellman Group.

 Value: 16

### DH_GROUP_CURVE_25519

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DH_GROUP_CURVE_25519: Int
```

Elliptic Curve Diffie-Hellman 25519.

 Value: 31

### DH_GROUP_NONE

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DH_GROUP_NONE: Int
```

None Diffie-Hellman Group.

 Value: 0

### ENCRYPTION_ALGORITHM_3DES

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ENCRYPTION_ALGORITHM_3DES: Int
```

3DES Encryption/Ciphering Algorithm.

 Value: 3

### ENCRYPTION_ALGORITHM_AES_CBC

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ENCRYPTION_ALGORITHM_AES_CBC: Int
```

AES-CBC Encryption/Ciphering Algorithm.

 Value: 12

### ENCRYPTION_ALGORITHM_AES_CTR

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ENCRYPTION_ALGORITHM_AES_CTR: Int
```

AES-CTR Encryption/Ciphering Algorithm.

 Value: 13

### ENCRYPTION_ALGORITHM_AES_GCM_12

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ENCRYPTION_ALGORITHM_AES_GCM_12: Int
```

AES-GCM Authentication/Integrity + Encryption/Ciphering Algorithm with 12-octet ICV (truncation).

 Value: 19

### ENCRYPTION_ALGORITHM_AES_GCM_16

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ENCRYPTION_ALGORITHM_AES_GCM_16: Int
```

AES-GCM Authentication/Integrity + Encryption/Ciphering Algorithm with 16-octet ICV (truncation).

 Value: 20

### ENCRYPTION_ALGORITHM_AES_GCM_8

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ENCRYPTION_ALGORITHM_AES_GCM_8: Int
```

AES-GCM Authentication/Integrity + Encryption/Ciphering Algorithm with 8-octet ICV (truncation).

 Value: 18

### ENCRYPTION_ALGORITHM_CHACHA20_POLY1305

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ENCRYPTION_ALGORITHM_CHACHA20_POLY1305: Int
```

ChaCha20-Poly1305 Authentication/Integrity + Encryption/Ciphering Algorithm with 16-octet ICV (truncation).

 Value: 28

### INTEGRITY_ALGORITHM_AES_CMAC_96

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val INTEGRITY_ALGORITHM_AES_CMAC_96: Int
```

AES-CMAC-96 Authentication/Integrity Algorithm.

 Value: 8

### INTEGRITY_ALGORITHM_AES_XCBC_96

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val INTEGRITY_ALGORITHM_AES_XCBC_96: Int
```

AES-XCBC-96 Authentication/Integrity Algorithm.

 Value: 5

### INTEGRITY_ALGORITHM_HMAC_SHA1_96

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val INTEGRITY_ALGORITHM_HMAC_SHA1_96: Int
```

HMAC-SHA1 Authentication/Integrity Algorithm.

 Value: 2

### INTEGRITY_ALGORITHM_HMAC_SHA2_256_128

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val INTEGRITY_ALGORITHM_HMAC_SHA2_256_128: Int
```

HMAC-SHA256 Authentication/Integrity Algorithm with 128-bit truncation.

 Value: 12

### INTEGRITY_ALGORITHM_HMAC_SHA2_384_192

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val INTEGRITY_ALGORITHM_HMAC_SHA2_384_192: Int
```

HMAC-SHA384 Authentication/Integrity Algorithm with 192-bit truncation.

 Value: 13

### INTEGRITY_ALGORITHM_HMAC_SHA2_512_256

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val INTEGRITY_ALGORITHM_HMAC_SHA2_512_256: Int
```

HMAC-SHA512 Authentication/Integrity Algorithm with 256-bit truncation.

 Value: 14

### INTEGRITY_ALGORITHM_NONE

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val INTEGRITY_ALGORITHM_NONE: Int
```

None Authentication/Integrity Algorithm.

 Value: 0

### KEY_LEN_AES_128

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_LEN_AES_128: Int
```

AES Encryption/Ciphering Algorithm key length 128 bits.

 Value: 128

### KEY_LEN_AES_192

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_LEN_AES_192: Int
```

AES Encryption/Ciphering Algorithm key length 192 bits.

 Value: 192

### KEY_LEN_AES_256

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_LEN_AES_256: Int
```

AES Encryption/Ciphering Algorithm key length 256 bits.

 Value: 256

### KEY_LEN_UNUSED

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_LEN_UNUSED: Int
```

Key length unused.

This value should only be used with the Encryption/Ciphering Algorithm that accepts a fixed key size such as `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/SaProposal#ENCRYPTION_ALGORITHM_3DES:kotlin.Int`.

 Value: 0

### PSEUDORANDOM_FUNCTION_AES128_CMAC

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PSEUDORANDOM_FUNCTION_AES128_CMAC: Int
```

AES128-CMAC Pseudorandom Function.

 Value: 8

### PSEUDORANDOM_FUNCTION_AES128_XCBC

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PSEUDORANDOM_FUNCTION_AES128_XCBC: Int
```

AES128-XCBC Pseudorandom Function.

 Value: 4

### PSEUDORANDOM_FUNCTION_HMAC_SHA1

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PSEUDORANDOM_FUNCTION_HMAC_SHA1: Int
```

HMAC-SHA1 Pseudorandom Function.

 Value: 2

### PSEUDORANDOM_FUNCTION_SHA2_256

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PSEUDORANDOM_FUNCTION_SHA2_256: Int
```

HMAC-SHA2-256 Pseudorandom Function.

 Value: 5

### PSEUDORANDOM_FUNCTION_SHA2_384

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PSEUDORANDOM_FUNCTION_SHA2_384: Int
```

HMAC-SHA2-384 Pseudorandom Function.

 Value: 6

### PSEUDORANDOM_FUNCTION_SHA2_512

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PSEUDORANDOM_FUNCTION_SHA2_512: Int
```

HMAC-SHA2-384 Pseudorandom Function.

 Value: 7

## Public methods

### equals

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun equals(other: Any?): Boolean
```

Indicates whether some other object is "equal to" this one.

The `equals` method implements an equivalence relation on non-null object references:

- It is *reflexive* : for any non-null reference value `x`, `x.equals(x)` should return `true`.
- It is *symmetric* : for any non-null reference values `x` and `y`, `x.equals(y)` should return `true` if and only if `y.equals(x)` returns `true`.
- It is *transitive* : for any non-null reference values `x`, `y`, and `z`, if `x.equals(y)` returns `true` and `y.equals(z)` returns `true`, then `x.equals(z)` should return `true`.
- It is *consistent* : for any non-null reference values `x` and `y`, multiple invocations of `x.equals(y)` consistently return `true` or consistently return `false`, provided no information used in `equals` comparisons on the objects is modified.
- For any non-null reference value `x`, `x.equals(null)` should return `false`.

An equivalence relation partitions the elements it operates on into *equivalence classes*; all the members of an equivalence class are equal to each other. Members of an equivalence class are substitutable for each other, at least for some purposes.

| Parameters ||
|---|---|
| `obj` | the reference object with which to compare. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this object is the same as the obj argument; `false` otherwise. |

### getDhGroups

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getDhGroups(): MutableList<Int!>
```

Gets all proposed Diffie-Hellman groups

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html!>` | A list of the IANA-defined IDs for the proposed Diffie-Hellman groups. This value cannot be `null`. |

### getEncryptionAlgorithms

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getEncryptionAlgorithms(): MutableList<Pair<Int!, Int!>!>
```

Gets all proposed encryption algorithms

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/util/Pair.html#<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html!, https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html!>!>` | A list of Pairs, with the IANA-defined ID for the proposed encryption algorithm as the first item, and the key length (in bits) as the second. This value cannot be `null`. |

### getIntegrityAlgorithms

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getIntegrityAlgorithms(): MutableList<Int!>
```

Gets all proposed integrity algorithms

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html!>` | A list of the IANA-defined IDs for the proposed integrity algorithms. This value cannot be `null`. |

### getSupportedDhGroups

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getSupportedDhGroups(): MutableSet<Int!>
```

Returns supported DH groups for IKE and Child SA proposal negotiation.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html!>` | This value cannot be `null`. |

### hashCode

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun hashCode(): Int
```

Returns a hash code value for the object. This method is supported for the benefit of hash tables such as those provided by `https://developer.android.com/reference/kotlin/java/util/HashMap.html#`.

The general contract of `hashCode` is:

- Whenever it is invoked on the same object more than once during an execution of a Java application, the `hashCode` method must consistently return the same integer, provided no information used in `equals` comparisons on the object is modified. This integer need not remain consistent from one execution of an application to another execution of the same application.
- If two objects are equal according to the `https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any)` method, then calling the `hashCode` method on each of the two objects must produce the same integer result.
- It is *not* required that if two objects are unequal according to the `https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any)` method, then calling the `hashCode` method on each of the two objects must produce distinct integer results. However, the programmer should be aware that producing distinct integer results for unequal objects may improve the performance of hash tables.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a hash code value for this object. |

### toString

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun toString(): String
```

Returns a string representation of the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | This value cannot be `null`. |
