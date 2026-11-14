Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# IkeSaProposal

```
class IkeSaProposal : SaProposal
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.net.ipsec.ike.SaProposal](SaProposal.md) ||
| | ↳ | [android.net.ipsec.ike.IkeSaProposal](IkeSaProposal.md) |

IkeSaProposal represents a proposed configuration to negotiate an IKE SA.

IkeSaProposal will contain cryptograhic algorithms and key generation materials for the negotiation of an IKE SA.

User must provide at least one valid IkeSaProposal when they are creating a new IKE SA.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSaProposal.Builder` This class is used to incrementally construct a IkeSaProposal. |

| Inherited constants ||
|---|---|
| From class SaProposal |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/SaProposal#DH_GROUP_1024_BIT_MODP:kotlin.Int` 1024-bit MODP Diffie-Hellman Group. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/SaProposal#DH_GROUP_1536_BIT_MODP:kotlin.Int` 1536-bit MODP Diffie-Hellman Group. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/SaProposal#DH_GROUP_2048_BIT_MODP:kotlin.Int` 2048-bit MODP Diffie-Hellman Group. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/SaProposal#DH_GROUP_3072_BIT_MODP:kotlin.Int` 3072-bit MODP Diffie-Hellman Group. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/SaProposal#DH_GROUP_4096_BIT_MODP:kotlin.Int` 4096-bit MODP Diffie-Hellman Group. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/SaProposal#DH_GROUP_CURVE_25519:kotlin.Int` Elliptic Curve Diffie-Hellman 25519. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/SaProposal#DH_GROUP_NONE:kotlin.Int` None Diffie-Hellman Group. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/SaProposal#ENCRYPTION_ALGORITHM_3DES:kotlin.Int` 3DES Encryption/Ciphering Algorithm. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/SaProposal#ENCRYPTION_ALGORITHM_AES_CBC:kotlin.Int` AES-CBC Encryption/Ciphering Algorithm. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/SaProposal#ENCRYPTION_ALGORITHM_AES_CTR:kotlin.Int` AES-CTR Encryption/Ciphering Algorithm. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/SaProposal#ENCRYPTION_ALGORITHM_AES_GCM_12:kotlin.Int` AES-GCM Authentication/Integrity + Encryption/Ciphering Algorithm with 12-octet ICV (truncation). <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/SaProposal#ENCRYPTION_ALGORITHM_AES_GCM_16:kotlin.Int` AES-GCM Authentication/Integrity + Encryption/Ciphering Algorithm with 16-octet ICV (truncation). <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/SaProposal#ENCRYPTION_ALGORITHM_AES_GCM_8:kotlin.Int` AES-GCM Authentication/Integrity + Encryption/Ciphering Algorithm with 8-octet ICV (truncation). <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/SaProposal#ENCRYPTION_ALGORITHM_CHACHA20_POLY1305:kotlin.Int` ChaCha20-Poly1305 Authentication/Integrity + Encryption/Ciphering Algorithm with 16-octet ICV (truncation). <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/SaProposal#INTEGRITY_ALGORITHM_AES_CMAC_96:kotlin.Int` AES-CMAC-96 Authentication/Integrity Algorithm. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/SaProposal#INTEGRITY_ALGORITHM_AES_XCBC_96:kotlin.Int` AES-XCBC-96 Authentication/Integrity Algorithm. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/SaProposal#INTEGRITY_ALGORITHM_HMAC_SHA1_96:kotlin.Int` HMAC-SHA1 Authentication/Integrity Algorithm. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/SaProposal#INTEGRITY_ALGORITHM_HMAC_SHA2_256_128:kotlin.Int` HMAC-SHA256 Authentication/Integrity Algorithm with 128-bit truncation. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/SaProposal#INTEGRITY_ALGORITHM_HMAC_SHA2_384_192:kotlin.Int` HMAC-SHA384 Authentication/Integrity Algorithm with 192-bit truncation. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/SaProposal#INTEGRITY_ALGORITHM_HMAC_SHA2_512_256:kotlin.Int` HMAC-SHA512 Authentication/Integrity Algorithm with 256-bit truncation. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/SaProposal#INTEGRITY_ALGORITHM_NONE:kotlin.Int` None Authentication/Integrity Algorithm. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/SaProposal#KEY_LEN_AES_128:kotlin.Int` AES Encryption/Ciphering Algorithm key length 128 bits. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/SaProposal#KEY_LEN_AES_192:kotlin.Int` AES Encryption/Ciphering Algorithm key length 192 bits. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/SaProposal#KEY_LEN_AES_256:kotlin.Int` AES Encryption/Ciphering Algorithm key length 256 bits. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/SaProposal#KEY_LEN_UNUSED:kotlin.Int` Key length unused. This value should only be used with the Encryption/Ciphering Algorithm that accepts a fixed key size such as `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/SaProposal#ENCRYPTION_ALGORITHM_3DES:kotlin.Int`. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/SaProposal#PSEUDORANDOM_FUNCTION_AES128_CMAC:kotlin.Int` AES128-CMAC Pseudorandom Function. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/SaProposal#PSEUDORANDOM_FUNCTION_AES128_XCBC:kotlin.Int` AES128-XCBC Pseudorandom Function. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/SaProposal#PSEUDORANDOM_FUNCTION_HMAC_SHA1:kotlin.Int` HMAC-SHA1 Pseudorandom Function. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/SaProposal#PSEUDORANDOM_FUNCTION_SHA2_256:kotlin.Int` HMAC-SHA2-256 Pseudorandom Function. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/SaProposal#PSEUDORANDOM_FUNCTION_SHA2_384:kotlin.Int` HMAC-SHA2-384 Pseudorandom Function. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/SaProposal#PSEUDORANDOM_FUNCTION_SHA2_512:kotlin.Int` HMAC-SHA2-384 Pseudorandom Function. <br /> | ||

| Public methods ||
|---|---|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | equals Indicates whether some other object is "equal to" this one. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\> | getPseudorandomFunctions Gets all proposed Pseudorandom Functions |
| static [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\> | getSupportedEncryptionAlgorithms Returns supported encryption algorithms for IKE SA proposal negotiation. |
| --- | --- |
| static [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\> | getSupportedIntegrityAlgorithms Returns supported integrity algorithms for IKE SA proposal negotiation. |
| static [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\> | getSupportedPseudorandomFunctions Returns supported pseudorandom functions for IKE SA proposal negotiation. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | hashCode Returns a hash code value for the object. |
| --- | --- |

| Inherited functions ||
|---|---|
| From class SaProposal |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html!>` | getDhGroups Gets all proposed Diffie-Hellman groups <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/util/Pair.html#<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html!, https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html!>!>` | getEncryptionAlgorithms Gets all proposed encryption algorithms <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html!>` | getIntegrityAlgorithms Gets all proposed integrity algorithms <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html!>` | getSupportedDhGroups Returns supported DH groups for IKE and Child SA proposal negotiation. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | toString Returns a string representation of the object. <br /> | ||

## Public methods

### equals

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun equals(other: Any?): Boolean
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

### getPseudorandomFunctions

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getPseudorandomFunctions(): MutableList<Int!>
```

Gets all proposed Pseudorandom Functions

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html!>` | A list of the IANA-defined IDs for the proposed Pseudorandom Functions. This value cannot be `null`. |

### getSupportedEncryptionAlgorithms

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getSupportedEncryptionAlgorithms(): MutableSet<Int!>
```

Returns supported encryption algorithms for IKE SA proposal negotiation.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html!>` | This value cannot be `null`. |

### getSupportedIntegrityAlgorithms

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getSupportedIntegrityAlgorithms(): MutableSet<Int!>
```

Returns supported integrity algorithms for IKE SA proposal negotiation.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html!>` | This value cannot be `null`. |

### getSupportedPseudorandomFunctions

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getSupportedPseudorandomFunctions(): MutableSet<Int!>
```

Returns supported pseudorandom functions for IKE SA proposal negotiation.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html!>` | This value cannot be `null`. |

### hashCode

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hashCode(): Int
```

Returns a hash code value for the object. This method is supported for the benefit of hash tables such as those provided by `https://developer.android.com/reference/kotlin/java/util/HashMap.html#`.

The general contract of `hashCode` is:

- Whenever it is invoked on the same object more than once during an execution of a Java application, the `hashCode` method must consistently return the same integer, provided no information used in `equals` comparisons on the object is modified. This integer need not remain consistent from one execution of an application to another execution of the same application.
- If two objects are equal according to the equals method, then calling the `hashCode` method on each of the two objects must produce the same integer result.
- It is *not* required that if two objects are unequal according to the equals method, then calling the `hashCode` method on each of the two objects must produce distinct integer results. However, the programmer should be aware that producing distinct integer results for unequal objects may improve the performance of hash tables.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a hash code value for this object. |
