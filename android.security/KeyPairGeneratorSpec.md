Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# KeyPairGeneratorSpec

Kotlin | [Java](https://developer.android.com/reference/android/security/KeyPairGeneratorSpec "View this page in Java")

```
class KeyPairGeneratorSpec : AlgorithmParameterSpec
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.security.KeyPairGeneratorSpec](https://developer.android.com/reference/kotlin/android/security/KeyPairGeneratorSpec#) |

| **This class was deprecated in API level 23.**
|
| Use `https://developer.android.com/reference/kotlin/android/security/keystore/KeyGenParameterSpec` instead.

This provides the required parameters needed for initializing the `KeyPairGenerator` that works with [Android KeyStore facility](https://developer.android.com/training/articles/keystore.html). The Android KeyStore facility is accessed through a `https://developer.android.com/reference/kotlin/java/security/KeyPairGenerator.html#` API using the `AndroidKeyStore` provider. The `context` passed in may be used to pop up some UI to ask the user to unlock or initialize the Android KeyStore facility.

After generation, the `keyStoreAlias` is used with the `https://developer.android.com/reference/kotlin/java/security/KeyStore.html#getEntry(kotlin.String,%20java.security.KeyStore.ProtectionParameter)` interface to retrieve the `https://developer.android.com/reference/kotlin/java/security/PrivateKey.html#` and its associated `https://developer.android.com/reference/kotlin/java/security/cert/Certificate.html#` chain.

The KeyPair generator will create a self-signed certificate with the subject as its X.509v3 Subject Distinguished Name and as its X.509v3 Issuer Distinguished Name along with the other parameters specified with the `https://developer.android.com/reference/kotlin/android/security/KeyPairGeneratorSpec.Builder`.

The self-signed X.509 certificate may be replaced at a later time by a certificate signed by a real Certificate Authority.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/security/KeyPairGeneratorSpec.Builder` Builder class for `https://developer.android.com/reference/kotlin/android/security/KeyPairGeneratorSpec#` objects. |

| Public methods ||
|---|---|
| [AlgorithmParameterSpec](https://developer.android.com/reference/kotlin/java/security/spec/AlgorithmParameterSpec.html#) | `https://developer.android.com/reference/kotlin/android/security/KeyPairGeneratorSpec#getAlgorithmParameterSpec()()` Returns the `https://developer.android.com/reference/kotlin/java/security/spec/AlgorithmParameterSpec.html#` that will be used for creation of the key pair. |
| [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)! | `https://developer.android.com/reference/kotlin/android/security/KeyPairGeneratorSpec#getContext()()` Gets the Android context used for operations with this instance. |
| [Date](https://developer.android.com/reference/kotlin/java/util/Date.html#) | `https://developer.android.com/reference/kotlin/android/security/KeyPairGeneratorSpec#getEndDate()()` Gets the end date to be used on the X. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/security/KeyPairGeneratorSpec#getKeySize()()` Returns the key size specified by this parameter. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | `https://developer.android.com/reference/kotlin/android/security/KeyPairGeneratorSpec#getKeyType()()` Returns the type of key pair (e.g., |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/security/KeyPairGeneratorSpec#getKeystoreAlias()()` Returns the alias that will be used in the `java.security.KeyStore` in conjunction with the `AndroidKeyStore`. |
| [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#) | `https://developer.android.com/reference/kotlin/android/security/KeyPairGeneratorSpec#getSerialNumber()()` Gets the serial number to be used on the X. |
| [Date](https://developer.android.com/reference/kotlin/java/util/Date.html#) | `https://developer.android.com/reference/kotlin/android/security/KeyPairGeneratorSpec#getStartDate()()` Gets the start date to be used on the X. |
| [X500Principal](https://developer.android.com/reference/kotlin/javax/security/auth/x500/X500Principal.html#) | `https://developer.android.com/reference/kotlin/android/security/KeyPairGeneratorSpec#getSubjectDN()()` Gets the subject distinguished name to be used on the X. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/security/KeyPairGeneratorSpec#isEncryptionRequired()()` Returns `true` if the key must be encrypted at rest. |

## Public methods

### getAlgorithmParameterSpec

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getAlgorithmParameterSpec(): AlgorithmParameterSpec
```

**Deprecated:** *Deprecated in Java.*

Returns the `https://developer.android.com/reference/kotlin/java/security/spec/AlgorithmParameterSpec.html#` that will be used for creation of the key pair.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/security/spec/AlgorithmParameterSpec.html#` | This value cannot be `null`. |

### getContext

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getContext(): Context!
```

**Deprecated:** *Deprecated in Java.*

Gets the Android context used for operations with this instance.

### getEndDate

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getEndDate(): Date
```

**Deprecated:** *Deprecated in Java.*

Gets the end date to be used on the X.509 certificate that will be put in the `https://developer.android.com/reference/kotlin/java/security/KeyStore.html#`.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/Date.html#` | This value cannot be `null`. |

### getKeySize

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getKeySize(): Int
```

**Deprecated:** *Deprecated in Java.*

Returns the key size specified by this parameter. For instance, for RSA this will return the modulus size and for EC it will return the field size.

### getKeyType

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getKeyType(): String?
```

**Deprecated:** *Deprecated in Java.*

Returns the type of key pair (e.g., `EC`, `RSA`) to be generated. See `https://developer.android.com/reference/kotlin/android/security/keystore/KeyProperties`.`KEY_ALGORITHM` constants.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?` | This value may be `null`. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/security/keystore/KeyProperties#KEY_ALGORITHM_RSA:kotlin.String` - `https://developer.android.com/reference/kotlin/android/security/keystore/KeyProperties#KEY_ALGORITHM_EC:kotlin.String` - `https://developer.android.com/reference/kotlin/android/security/keystore/KeyProperties#KEY_ALGORITHM_AES:kotlin.String` - `https://developer.android.com/reference/kotlin/android/security/keystore/KeyProperties#KEY_ALGORITHM_HMAC_SHA1:kotlin.String` - `https://developer.android.com/reference/kotlin/android/security/keystore/KeyProperties#KEY_ALGORITHM_HMAC_SHA224:kotlin.String` - `https://developer.android.com/reference/kotlin/android/security/keystore/KeyProperties#KEY_ALGORITHM_HMAC_SHA256:kotlin.String` - `https://developer.android.com/reference/kotlin/android/security/keystore/KeyProperties#KEY_ALGORITHM_HMAC_SHA384:kotlin.String` - `https://developer.android.com/reference/kotlin/android/security/keystore/KeyProperties#KEY_ALGORITHM_HMAC_SHA512:kotlin.String` |

### getKeystoreAlias

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getKeystoreAlias(): String!
```

**Deprecated:** *Deprecated in Java.*

Returns the alias that will be used in the `java.security.KeyStore` in conjunction with the `AndroidKeyStore`.

### getSerialNumber

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getSerialNumber(): BigInteger
```

**Deprecated:** *Deprecated in Java.*

Gets the serial number to be used on the X.509 certificate that will be put in the `https://developer.android.com/reference/kotlin/java/security/KeyStore.html#`.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/math/BigInteger.html#` | This value cannot be `null`. |

### getStartDate

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getStartDate(): Date
```

**Deprecated:** *Deprecated in Java.*

Gets the start date to be used on the X.509 certificate that will be put in the `https://developer.android.com/reference/kotlin/java/security/KeyStore.html#`.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/Date.html#` | This value cannot be `null`. |

### getSubjectDN

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getSubjectDN(): X500Principal
```

**Deprecated:** *Deprecated in Java.*

Gets the subject distinguished name to be used on the X.509 certificate that will be put in the `https://developer.android.com/reference/kotlin/java/security/KeyStore.html#`.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/javax/security/auth/x500/X500Principal.html#` | This value cannot be `null`. |

### isEncryptionRequired

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isEncryptionRequired(): Boolean
```

**Deprecated:** *Encryption at rest is on by default. If extra binding to the lockscreen screen credential is desired use `https://developer.android.com/reference/kotlin/android/security/keystore/KeyGenParameterSpec.Builder#setUserAuthenticationRequired(kotlin.Boolean)`. This flag will be ignored from Android S.*

Returns `true` if the key must be encrypted at rest. This will protect the key pair with the secure lock screen credential (e.g., password, PIN, or pattern).

Note that encrypting the key at rest requires that the secure lock screen (e.g., password, PIN, pattern) is set up, otherwise key generation will fail. Moreover, this key will be deleted when the secure lock screen is disabled or reset (e.g., by the user or a Device Administrator). Finally, this key cannot be used until the user unlocks the secure lock screen after boot.
**See Also**

- `https://developer.android.com/reference/kotlin/android/app/KeyguardManager.html#isDeviceSecure()`
