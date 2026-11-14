# Recipient

Kotlin | [Java](../android/crypto/hpke/Recipient.md)
| --- | --- |

```
open class Recipient
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.crypto.hpke.Recipient](../android/crypto/hpke/Recipient.md) |

A class for receiving HPKE messages.

## Summary

| Nested classes ||
|---|---|
| open | `https://developer.android.com/reference/kotlin/android/crypto/hpke/Recipient.Builder` A builder for HPKE Recipient objects. |

| Public methods ||
|---|---|
| open [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html) | `https://developer.android.com/reference/kotlin/android/crypto/hpke/Recipient#export(kotlin.Int,%20kotlin.ByteArray)(length: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, context: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html?)` Exports secret key material from this Recipient as described in RFC 9180. |
| open [Provider](../java/security/Provider.md) | `https://developer.android.com/reference/kotlin/android/crypto/hpke/Recipient#getProvider()()` Returns the `https://developer.android.com/reference/kotlin/java/security/Provider.html#` being used by this Recipient. |
| open [HpkeSpi](../android/crypto/hpke/HpkeSpi.md) | `https://developer.android.com/reference/kotlin/android/crypto/hpke/Recipient#getSpi()()` Returns the `https://developer.android.com/reference/kotlin/android/crypto/hpke/HpkeSpi` being used by this Recipient. |
| --- | --- |
| open [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html) | `https://developer.android.com/reference/kotlin/android/crypto/hpke/Recipient#open(kotlin.ByteArray,%20kotlin.ByteArray)(ciphertext: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html, aad: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html?)` Opens a message, using the internal key schedule maintained by this Recipient. |

## Public methods

### export

```
open fun export(
    length: Int, 
    context: ByteArray?
): ByteArray
```

Exports secret key material from this Recipient as described in RFC 9180.

| Parameters ||
|---|---|
| `length` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): expected output length |
| `context` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)?: optional exporter context string, may be null or empty |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html` | exported value. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the length is not valid for the KDF in use |

### getProvider

```
open fun getProvider(): Provider
```

Returns the `https://developer.android.com/reference/kotlin/java/security/Provider.html#` being used by this Recipient.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/security/Provider.html#` | the Provider. This value cannot be `null`. |

### getSpi

```
open fun getSpi(): HpkeSpi
```

Returns the `https://developer.android.com/reference/kotlin/android/crypto/hpke/HpkeSpi` being used by this Recipient.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/crypto/hpke/HpkeSpi` | the SPI. This value cannot be `null`. |

### open

```
open fun open(
    ciphertext: ByteArray, 
    aad: ByteArray?
): ByteArray
```

Opens a message, using the internal key schedule maintained by this Recipient.

| Parameters ||
|---|---|
| `ciphertext` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html): the ciphertext. This value cannot be `null`. |
| `aad` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)?: optional additional authenticated data, may be null or empty |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html` | the plaintext. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.security.GeneralSecurityException` | on decryption failures |

**See Also**
