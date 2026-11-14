# Hpke

Kotlin | [Java](Hpke.md)
| --- | --- |

```
open class Hpke
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.crypto.hpke.Hpke](Hpke.md) |

Provides access to implementations of HPKE hybrid cryptography as per RFC 9180.

Provider and HPKE suite selection are done via the `getInstance` methods, and then instances of senders and receivers can be created using `newSender` or {newReceiver}. Each sender and receiver is independent, i.e. does not share any encapsulated state with other senders or receivers created via this `Hpke`.

HPKE suites are composed of a key encapsulation mechanism (KEM), a key derivation function (KDF) and an authenticated cipher algorithm (AEAD) as defined in RFC 9180 section 7. `https://developer.android.com/reference/kotlin/java/security/spec/NamedParameterSpec.html#` for these can be found in KemParameterSpec, KdfParameterSpec and AeadParameterSpec. These can be composed into a full HPKE suite name used to request a particular implementation using getSuiteName.

## Summary

| Public methods ||
|---|---|
| open static [Hpke](Hpke.md) | getInstance Returns an Hpke instance configured for the requested HPKE suite, using the highest priority `https://developer.android.com/reference/kotlin/java/security/Provider.html#` which implements it. |
| open static [Hpke](Hpke.md) | getInstance Returns an Hpke instance configured for the requested HPKE suite, using the requested `https://developer.android.com/reference/kotlin/java/security/Provider.html#` by name. |
| open static [Hpke](Hpke.md) | getInstance Returns an Hpke instance configured for the requested HPKE suite, using the requested `https://developer.android.com/reference/kotlin/java/security/Provider.html#`. |
| --- | --- |
| open [Provider](../java.security/Provider.md) | getProvider Returns the `https://developer.android.com/reference/kotlin/java/security/Provider.html#` being used by this Hpke instance. |
| open static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | getSuiteName Generates a full HPKE suite name from the named parameter specifications of its components, which have names reflecting their usage in RFC 9180. |
| open [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html) | open One shot API to open a single ciphertext using BASE mode (no authentication). |
| --- | --- |
| open [Message](../android/crypto/hpke/Message.md) | seal One shot API to seal a single message using BASE mode (no authentication). |

## Public methods

### getInstance

```
open static fun getInstance(suiteName: String): Hpke
```

Returns an Hpke instance configured for the requested HPKE suite, using the highest priority `https://developer.android.com/reference/kotlin/java/security/Provider.html#` which implements it.

Use getSuiteName for generating HPKE suite names from `https://developer.android.com/reference/kotlin/java/security/spec/NamedParameterSpec.html#`

| Parameters ||
|---|---|
| `suiteName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the HPKE suite to use. This value cannot be `null`. |

| Return ||
|---|---|
| Hpke | an Hpke instance configured for the requested suite. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.security.NoSuchAlgorithmException` | if no Providers can be found for the requested suite |

### getInstance

```
open static fun getInstance(
    suiteName: String, 
    providerName: String
): Hpke
```

Returns an Hpke instance configured for the requested HPKE suite, using the requested `https://developer.android.com/reference/kotlin/java/security/Provider.html#` by name.

| Parameters ||
|---|---|
| `suiteName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the HPKE suite to use. This value cannot be `null`. |
| `providerName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the name of the provider to use. This value cannot be `null`. |

| Return ||
|---|---|
| Hpke | an Hpke instance configured for the requested suite and Provider. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if providerName is null or empty |
| `java.security.NoSuchAlgorithmException` | if the named Provider does not implement this suite |
| `java.security.NoSuchProviderException` | if no Provider with the requested name can be found |
| --- | --- |

### getInstance

```
open static fun getInstance(
    suiteName: String, 
    provider: Provider
): Hpke
```

Returns an Hpke instance configured for the requested HPKE suite, using the requested `https://developer.android.com/reference/kotlin/java/security/Provider.html#`.

| Parameters ||
|---|---|
| `suiteName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the HPKE suite to use. This value cannot be `null`. |
| `provider` | [Provider](../java.security/Provider.md): the provider to use. This value cannot be `null`. |

| Return ||
|---|---|
| Hpke | an Hpke instance configured for the requested suite and Provider. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if provider is null |
| `java.security.NoSuchAlgorithmException` | if the Provider does not implement this suite |

### getProvider

```
open fun getProvider(): Provider
```

Returns the `https://developer.android.com/reference/kotlin/java/security/Provider.html#` being used by this Hpke instance.

<br />

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/security/Provider.html#` | the Provider. This value cannot be `null`. |

### getSuiteName

```
open static fun getSuiteName(
    kem: KemParameterSpec, 
    kdf: KdfParameterSpec, 
    aead: AeadParameterSpec
): String
```

Generates a full HPKE suite name from the named parameter specifications of its components, which have names reflecting their usage in RFC 9180.

HPKE suites are composed of a key encapsulation mechanism (KEM), a key derivation function (KDF) and an authenticated cipher algorithm (AEAD) as defined in RFC 9180 section 7. `https://developer.android.com/reference/kotlin/java/security/spec/NamedParameterSpec.html#` for these can be foundu in KemParameterSpec, KdfParameterSpec and AeadParameterSpec.

| Parameters ||
|---|---|
| `kem` | [KemParameterSpec](KemParameterSpec.md): the key encapsulation mechanism to use. This value cannot be `null`. |
| `kdf` | [KdfParameterSpec](KdfParameterSpec.md): the key derivation function to use. This value cannot be `null`. |
| `aead` | [AeadParameterSpec](../android/crypto/hpke/AeadParameterSpec.md): the AEAD cipher to use. This value cannot be `null`. |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a fully composed HPKE suite name. This value cannot be `null`. |

**See Also**

- KemParameterSpec
- KdfParameterSpec
- AeadParameterSpec

### open

```
open fun open(
    recipientKey: PrivateKey, 
    info: ByteArray?, 
    message: Message, 
    aad: ByteArray?
): ByteArray
```

One shot API to open a single ciphertext using BASE mode (no authentication).

| Parameters ||
|---|---|
| `recipientKey` | [PrivateKey](../java.security/PrivateKey.md): private key of the recipient. This value cannot be `null`. |
| `info` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)?: application-supplied information, may be null or empty |
| `message` | [Message](../android/crypto/hpke/Message.md): the Message to open. This value cannot be `null`. |
| --- | --- |
| `aad` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)?: optional additional authenticated data, may be null or empty |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html` | decrypted plaintext. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.security.GeneralSecurityException` | if the decryption fails |
| `java.security.InvalidKeyException` | if recipientKey is null or an unsupported key format |

**See Also**

### seal

```
open fun seal(
    recipientKey: PublicKey, 
    info: ByteArray?, 
    plaintext: ByteArray, 
    aad: ByteArray?
): Message
```

One shot API to seal a single message using BASE mode (no authentication).

| Parameters ||
|---|---|
| `recipientKey` | [PublicKey](../java.security/PublicKey.md): public key of the recipient. This value cannot be `null`. |
| `info` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)?: additional application-supplied information, may be null or empty |
| `plaintext` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html): the message to send. This value cannot be `null`. |
| --- | --- |
| `aad` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)?: optional additional authenticated data, may be null or empty |

| Return ||
|---|---|
| Message | a Message object containing the encapsulated key, ciphertext and aad. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.security.InvalidKeyException` | if recipientKey is null or an unsupported key format |

**See Also**
