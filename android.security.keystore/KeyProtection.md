# KeyProtection

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# KeyProtection

Kotlin| [Java](../android/security/keystore/KeyProtection.md) 
| --- | --- |

```
class KeyProtection : KeyStore.ProtectionParameter
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.security.keystore.KeyProtection](../android/security/keystore/KeyProtection.md) |

Specification of how a key or key pair is secured when imported into the [Android Keystore system](https://developer.android.com/training/articles/keystore.html). This class specifies authorized uses of the imported key, such as whether user authentication is required for using the key, what operations the key is authorized for (e.g., decryption, but not signing) with what parameters (e.g., only with a particular padding scheme or digest), and the key's validity start and end dates. Key use authorizations expressed in this class apply only to secret keys and private keys -- public keys can be used for any supported operations.

To import a key or key pair into the Android Keystore, create an instance of this class using the [Builder](../android/security/keystore/KeyProtection.Builder.md) and pass the instance into [KeyStore.setEntry](../java/security/KeyStore.md))with the key or key pair being imported.

To obtain the secret/symmetric or private key from the Android Keystore use [KeyStore.getKey(String, null)](../java/security/KeyStore.md))or [KeyStore.getEntry(String, null)](../java/security/KeyStore.md)). To obtain the public key from the Android Keystore use [java.security.KeyStore#getCertificate(String)](../java/security/KeyStore.md))and then [Certificate.getPublicKey()](../java/security/cert/Certificate.md)).

To help obtain algorithm-specific public parameters of key pairs stored in the Android Keystore, its private keys implement [java.security.interfaces.ECKey](../java/security/interfaces/ECKey.md) or [java.security.interfaces.RSAKey](../java/security/interfaces/RSAKey.md) interfaces whereas its public keys implement [java.security.interfaces.ECPublicKey](../java/security/interfaces/ECPublicKey.md) or [java.security.interfaces.RSAPublicKey](../java/security/interfaces/RSAPublicKey.md) interfaces.

NOTE: The key material of keys stored in the Android Keystore is not accessible.

Instances of this class are immutable.

<br />

### Known issues

A known bug in Android 6.0 (API Level 23) causes user authentication-related authorizations to be enforced even for public keys. To work around this issue extract the public key material to use outside of Android Keystore. For example: 

```kotlin
<code>PublicKey unrestrictedPublicKey =
          KeyFactory.getInstance(publicKey.getAlgorithm()).generatePublic(
                  new X509EncodedKeySpec(publicKey.getEncoded()));
  </code>
```

<br />

### Example: AES key for encryption/decryption in GCM mode

This example illustrates how to import an AES key into the Android KeyStore under alias`key1`authorized to be used only for encryption/decryption in GCM mode with no padding. The key must export its key material via [Key.getEncoded()](../java/security/Key.md))in`RAW`format. 

```kotlin
<code>SecretKey key = ...; // AES key
 
  KeyStore keyStore = KeyStore.getInstance("AndroidKeyStore");
  keyStore.load(null);
  keyStore.setEntry(
          "key1",
          new KeyStore.SecretKeyEntry(key),
          new KeyProtection.Builder(KeyProperties.PURPOSE_ENCRYPT | KeyProperties.PURPOSE_DECRYPT)
                  .setBlockMode(KeyProperties.BLOCK_MODE_GCM)
                  .setEncryptionPaddings(KeyProperties.ENCRYPTION_PADDING_NONE)
                  .build());
  // Key imported, obtain a reference to it.
  SecretKey keyStoreKey = (SecretKey) keyStore.getKey("key1", null);
  // The original key can now be discarded.
 
  Cipher cipher = Cipher.getInstance("AES/GCM/NoPadding");
  cipher.init(Cipher.ENCRYPT_MODE, keyStoreKey);
  ...
  </code>
```

<br />

### Example: HMAC key for generating MACs using SHA-512

This example illustrates how to import an HMAC key into the Android KeyStore under alias`key1`authorized to be used only for generating MACs using SHA-512 digest. The key must export its key material via [Key.getEncoded()](../java/security/Key.md))in`RAW`format. 

```kotlin
<code>SecretKey key = ...; // HMAC key of algorithm "HmacSHA512".
 
  KeyStore keyStore = KeyStore.getInstance("AndroidKeyStore");
  keyStore.load(null);
  keyStore.setEntry(
          "key1",
          new KeyStore.SecretKeyEntry(key),
          new KeyProtection.Builder(KeyProperties.PURPOSE_SIGN).build());
  // Key imported, obtain a reference to it.
  SecretKey keyStoreKey = (SecretKey) keyStore.getKey("key1", null);
  // The original key can now be discarded.
 
  Mac mac = Mac.getInstance("HmacSHA512");
  mac.init(keyStoreKey);
  ...
  </code>
```

<br />

### Example: EC key pair for signing/verification using ECDSA

This example illustrates how to import an EC key pair into the Android KeyStore under alias`key2`with the private key authorized to be used only for signing with SHA-256 or SHA-512 digests. The use of the public key is unrestricted. Both the private and the public key must export their key material via [Key.getEncoded()](../java/security/Key.md))in`PKCS#8`and`X.509`format respectively. 

```kotlin
<code>PrivateKey privateKey = ...;   // EC private key
  Certificate[] certChain = ...; // Certificate chain with the first certificate
                                 // containing the corresponding EC public key.
 
  KeyStore keyStore = KeyStore.getInstance("AndroidKeyStore");
  keyStore.load(null);
  keyStore.setEntry(
          "key2",
          new KeyStore.PrivateKeyEntry(privateKey, certChain),
          new KeyProtection.Builder(KeyProperties.PURPOSE_SIGN)
                  .setDigests(KeyProperties.DIGEST_SHA256, KeyProperties.DIGEST_SHA512)
                  .build());
  // Key pair imported, obtain a reference to it.
  PrivateKey keyStorePrivateKey = (PrivateKey) keyStore.getKey("key2", null);
  PublicKey publicKey = keyStore.getCertificate("key2").getPublicKey();
  // The original private key can now be discarded.
 
  Signature signature = Signature.getInstance("SHA256withECDSA");
  signature.initSign(keyStorePrivateKey);
  ...
  </code>
```

<br />

### Example: RSA key pair for signing/verification using PKCS#1 padding

This example illustrates how to import an RSA key pair into the Android KeyStore under alias`key2`with the private key authorized to be used only for signing using the PKCS#1 signature padding scheme with SHA-256 digest and only if the user has been authenticated within the last ten minutes. The use of the public key is unrestricted (see Known Issues). Both the private and the public key must export their key material via [Key.getEncoded()](../java/security/Key.md))in`PKCS#8`and`X.509`format respectively. 

```kotlin
<code>PrivateKey privateKey = ...;   // RSA private key
  Certificate[] certChain = ...; // Certificate chain with the first certificate
                                 // containing the corresponding RSA public key.
 
  KeyStore keyStore = KeyStore.getInstance("AndroidKeyStore");
  keyStore.load(null);
  keyStore.setEntry(
          "key2",
          new KeyStore.PrivateKeyEntry(privateKey, certChain),
          new KeyProtection.Builder(KeyProperties.PURPOSE_SIGN)
                  .setDigests(KeyProperties.DIGEST_SHA256)
                  .setSignaturePaddings(KeyProperties.SIGNATURE_PADDING_RSA_PKCS1)
                  // Only permit this key to be used if the user
                  // authenticated within the last ten minutes.
                  .setUserAuthenticationRequired(true)
                  .setUserAuthenticationValidityDurationSeconds(10 * 60)
                  .build());
  // Key pair imported, obtain a reference to it.
  PrivateKey keyStorePrivateKey = (PrivateKey) keyStore.getKey("key2", null);
  PublicKey publicKey = keyStore.getCertificate("key2").getPublicKey();
  // The original private key can now be discarded.
 
  Signature signature = Signature.getInstance("SHA256withRSA");
  signature.initSign(keyStorePrivateKey);
  ...
  </code>
```

<br />

### Example: RSA key pair for encryption/decryption using PKCS#1 padding

This example illustrates how to import an RSA key pair into the Android KeyStore under alias`key2`with the private key authorized to be used only for decryption using the PKCS#1 encryption padding scheme. The use of public key is unrestricted, thus permitting encryption using any padding schemes and digests. Both the private and the public key must export their key material via [Key.getEncoded()](../java/security/Key.md))in`PKCS#8`and`X.509`format respectively. 

```kotlin
<code>PrivateKey privateKey = ...;   // RSA private key
  Certificate[] certChain = ...; // Certificate chain with the first certificate
                                 // containing the corresponding RSA public key.
 
  KeyStore keyStore = KeyStore.getInstance("AndroidKeyStore");
  keyStore.load(null);
  keyStore.setEntry(
          "key2",
          new KeyStore.PrivateKeyEntry(privateKey, certChain),
          new KeyProtection.Builder(KeyProperties.PURPOSE_DECRYPT)
                  .setEncryptionPaddings(KeyProperties.ENCRYPTION_PADDING_RSA_PKCS1)
                  .build());
  // Key pair imported, obtain a reference to it.
  PrivateKey keyStorePrivateKey = (PrivateKey) keyStore.getKey("key2", null);
  PublicKey publicKey = keyStore.getCertificate("key2").getPublicKey();
  // The original private key can now be discarded.
 
  Cipher cipher = Cipher.getInstance("RSA/ECB/PKCS1Padding");
  cipher.init(Cipher.DECRYPT_MODE, keyStorePrivateKey);
  ...
  </code>
```

## Summary

| Nested classes ||
|---|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](../android/security/keystore/KeyProtection.Builder.md) Builder of [KeyProtection](../android/security/keystore/KeyProtection.md) instances. |

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | [getBlockModes](../android/security/keystore/KeyProtection.md))`()` Gets the set of block modes (e.g., |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | [getDigests](../android/security/keystore/KeyProtection.md))`()` Gets the set of digest algorithms (e.g., |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | [getEncryptionPaddings](../android/security/keystore/KeyProtection.md))`()` Gets the set of padding schemes (e.g., |
| --- | --- |
| [Date](../java/util/Date.md)? | [getKeyValidityForConsumptionEnd](../android/security/keystore/KeyProtection.md))`()` Gets the time instant after which the key is no long valid for decryption and verification. |
| [Date](../java/util/Date.md)? | [getKeyValidityForOriginationEnd](../android/security/keystore/KeyProtection.md))`()` Gets the time instant after which the key is no long valid for encryption and signing. |
| [Date](../java/util/Date.md)? | [getKeyValidityStart](../android/security/keystore/KeyProtection.md))`()` Gets the time instant before which the key is not yet valid. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMaxUsageCount](../android/security/keystore/KeyProtection.md))`()` Returns the maximum number of times the limited use key is allowed to be used or [KeyProperties.UNRESTRICTED_USAGE_COUNT](../android/security/keystore/KeyProperties.md) if there's no restriction on the number of times the key can be used. |
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | [getMgf1Digests](../android/security/keystore/KeyProtection.md))`()` Returns the set of digests that can be used by the MGF1 mask generation function (e.g., |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPurposes](../android/security/keystore/KeyProtection.md))`()` Gets the set of purposes (e.g., encrypt, decrypt, sign) for which the key can be used. |
| --- | --- |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | [getSignaturePaddings](../android/security/keystore/KeyProtection.md))`()` Gets the set of padding schemes (e.g., |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getUserAuthenticationType](../android/security/keystore/KeyProtection.md))`()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getUserAuthenticationValidityDurationSeconds](../android/security/keystore/KeyProtection.md))`()` Gets the duration of time (seconds) for which this key is authorized to be used after the user is successfully authenticated. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isDigestsSpecified](../android/security/keystore/KeyProtection.md))`()` Returns`true`if the set of digest algorithms with which the key can be used has been specified. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isInvalidatedByBiometricEnrollment](../android/security/keystore/KeyProtection.md))`()` Returns`true`if the key is irreversibly invalidated when a new biometric is enrolled or all enrolled biometrics are removed. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isMgf1DigestsSpecified](../android/security/keystore/KeyProtection.md))`()` Returns`true`if the set of digests for the MGF1 mask generation function, with which the key can be used, has been specified. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isRandomizedEncryptionRequired](../android/security/keystore/KeyProtection.md))`()` Returns`true`if encryption using this key must be sufficiently randomized to produce different ciphertexts for the same plaintext every time. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isUnlockedDeviceRequired](../android/security/keystore/KeyProtection.md))`()` Returns`true`if the key is authorized to be used only while the device is unlocked. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isUserAuthenticationRequired](../android/security/keystore/KeyProtection.md))`()` Returns`true`if the key is authorized to be used only if the user has been authenticated. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isUserAuthenticationValidWhileOnBody](../android/security/keystore/KeyProtection.md))`()` Returns`true`if the key will be de-authorized when the device is removed from the user's body. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isUserConfirmationRequired](../android/security/keystore/KeyProtection.md))`()` Returns`true`if the key is authorized to be used only for messages confirmed by the user. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isUserPresenceRequired](../android/security/keystore/KeyProtection.md))`()` Returns`true`if the key is authorized to be used only if a test of user presence has been performed between the`Signature.initSign()`and`Signature.sign()`calls. |
| --- | --- |

## Public methods

### getBlockModes

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getBlockModes(): Array<String!>
```

Gets the set of block modes (e.g.,`GCM`,`CBC`) with which the key can be used when encrypting/decrypting. Attempts to use the key with any other block modes will be rejected.

See [KeyProperties](../android/security/keystore/KeyProperties.md).`BLOCK_MODE`constants.

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!> | This value cannot be`null`. Value is [android.security.keystore.KeyProperties#BLOCK_MODE_ECB](../android/security/keystore/KeyProperties.md), [android.security.keystore.KeyProperties#BLOCK_MODE_CBC](../android/security/keystore/KeyProperties.md), [android.security.keystore.KeyProperties#BLOCK_MODE_CTR](../android/security/keystore/KeyProperties.md), or [android.security.keystore.KeyProperties#BLOCK_MODE_GCM](../android/security/keystore/KeyProperties.md) |

### getDigests

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDigests(): Array<String!>
```

Gets the set of digest algorithms (e.g.,`SHA-256`,`SHA-384`) with which the key can be used.

See [KeyProperties](../android/security/keystore/KeyProperties.md).`DIGEST`constants.

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!> | This value cannot be`null`. Value is [android.security.keystore.KeyProperties#DIGEST_NONE](../android/security/keystore/KeyProperties.md), [android.security.keystore.KeyProperties#DIGEST_MD5](../android/security/keystore/KeyProperties.md), [android.security.keystore.KeyProperties#DIGEST_SHA1](../android/security/keystore/KeyProperties.md), [android.security.keystore.KeyProperties#DIGEST_SHA224](../android/security/keystore/KeyProperties.md), [android.security.keystore.KeyProperties#DIGEST_SHA256](../android/security/keystore/KeyProperties.md), [android.security.keystore.KeyProperties#DIGEST_SHA384](../android/security/keystore/KeyProperties.md), or [android.security.keystore.KeyProperties#DIGEST_SHA512](../android/security/keystore/KeyProperties.md) |

| Exceptions ||
|-----------------------------------|-------------------------------------|
| `java.lang.IllegalStateException` | if this set has not been specified. |

**See Also**

- <https://developer.android.com/reference/kotlin/android/security/keystore/KeyProtection#isDigestsSpecified()> 

### getEncryptionPaddings

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getEncryptionPaddings(): Array<String!>
```

Gets the set of padding schemes (e.g.,`PKCS7Padding`,`PKCS1Padding`,`NoPadding`) with which the key can be used when encrypting/decrypting. Attempts to use the key with any other padding scheme will be rejected.

See [KeyProperties](../android/security/keystore/KeyProperties.md).`ENCRYPTION_PADDING`constants.

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!> | This value cannot be`null`. Value is [android.security.keystore.KeyProperties#ENCRYPTION_PADDING_NONE](../android/security/keystore/KeyProperties.md), [android.security.keystore.KeyProperties#ENCRYPTION_PADDING_PKCS7](../android/security/keystore/KeyProperties.md), [android.security.keystore.KeyProperties#ENCRYPTION_PADDING_RSA_PKCS1](../android/security/keystore/KeyProperties.md), or [android.security.keystore.KeyProperties#ENCRYPTION_PADDING_RSA_OAEP](../android/security/keystore/KeyProperties.md) |

### getKeyValidityForConsumptionEnd

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getKeyValidityForConsumptionEnd(): Date?
```

Gets the time instant after which the key is no long valid for decryption and verification.

| Return ||
|------------------------------------------------------------------------------|------------------------------------|
| [Date](../java/util/Date.md)? | instant or`null`if not restricted. |

### getKeyValidityForOriginationEnd

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getKeyValidityForOriginationEnd(): Date?
```

Gets the time instant after which the key is no long valid for encryption and signing.

| Return ||
|------------------------------------------------------------------------------|------------------------------------|
| [Date](../java/util/Date.md)? | instant or`null`if not restricted. |

### getKeyValidityStart

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getKeyValidityStart(): Date?
```

Gets the time instant before which the key is not yet valid.

| Return ||
|------------------------------------------------------------------------------|------------------------------------|
| [Date](../java/util/Date.md)? | instant or`null`if not restricted. |

### getMaxUsageCount

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMaxUsageCount(): Int
```

Returns the maximum number of times the limited use key is allowed to be used or [KeyProperties.UNRESTRICTED_USAGE_COUNT](../android/security/keystore/KeyProperties.md) if there's no restriction on the number of times the key can be used. 
**See Also**

- [android.security.keystore.KeyProtection.Builder#setMaxUsageCount(int)](../android/security/keystore/KeyProtection.Builder.md)) 

### getMgf1Digests

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMgf1Digests(): MutableSet<String!>
```

Returns the set of digests that can be used by the MGF1 mask generation function (e.g.,`SHA-256`,`SHA-384`) with the key. Useful with the`RSA-OAEP`scheme. If not explicitly specified during key generation, the default`SHA-1`digest is used and may be specified.

See [KeyProperties](../android/security/keystore/KeyProperties.md).`DIGEST`constants.

| Return ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!> | This value cannot be`null`. Value is [android.security.keystore.KeyProperties#DIGEST_NONE](../android/security/keystore/KeyProperties.md), [android.security.keystore.KeyProperties#DIGEST_MD5](../android/security/keystore/KeyProperties.md), [android.security.keystore.KeyProperties#DIGEST_SHA1](../android/security/keystore/KeyProperties.md), [android.security.keystore.KeyProperties#DIGEST_SHA224](../android/security/keystore/KeyProperties.md), [android.security.keystore.KeyProperties#DIGEST_SHA256](../android/security/keystore/KeyProperties.md), [android.security.keystore.KeyProperties#DIGEST_SHA384](../android/security/keystore/KeyProperties.md), or [android.security.keystore.KeyProperties#DIGEST_SHA512](../android/security/keystore/KeyProperties.md) |

| Exceptions ||
|-----------------------------------|-------------------------------------|
| `java.lang.IllegalStateException` | if this set has not been specified. |

**See Also**

- <https://developer.android.com/reference/kotlin/android/security/keystore/KeyProtection#isMgf1DigestsSpecified()> 

### getPurposes

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPurposes(): Int
```

Gets the set of purposes (e.g., encrypt, decrypt, sign) for which the key can be used. Attempts to use the key for any other purpose will be rejected.

See [KeyProperties](../android/security/keystore/KeyProperties.md).`PURPOSE`flags.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is either`0`or a combination of [android.security.keystore.KeyProperties#PURPOSE_ENCRYPT](../android/security/keystore/KeyProperties.md), [android.security.keystore.KeyProperties#PURPOSE_DECRYPT](../android/security/keystore/KeyProperties.md), [android.security.keystore.KeyProperties#PURPOSE_SIGN](../android/security/keystore/KeyProperties.md), [android.security.keystore.KeyProperties#PURPOSE_VERIFY](../android/security/keystore/KeyProperties.md), [android.security.keystore.KeyProperties#PURPOSE_WRAP_KEY](../android/security/keystore/KeyProperties.md), [android.security.keystore.KeyProperties#PURPOSE_AGREE_KEY](../android/security/keystore/KeyProperties.md), and [android.security.keystore.KeyProperties#PURPOSE_ATTEST_KEY](../android/security/keystore/KeyProperties.md) |

### getSignaturePaddings

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSignaturePaddings(): Array<String!>
```

Gets the set of padding schemes (e.g.,`PSS`,`PKCS#1`) with which the key can be used when signing/verifying. Attempts to use the key with any other padding scheme will be rejected.

See [KeyProperties](../android/security/keystore/KeyProperties.md).`SIGNATURE_PADDING`constants.

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!> | This value cannot be`null`. Value is [android.security.keystore.KeyProperties#SIGNATURE_PADDING_RSA_PKCS1](../android/security/keystore/KeyProperties.md), or [android.security.keystore.KeyProperties#SIGNATURE_PADDING_RSA_PSS](../android/security/keystore/KeyProperties.md) |

### getUserAuthenticationType

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getUserAuthenticationType(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is either`0`or a combination of [android.security.keystore.KeyProperties#AUTH_BIOMETRIC_STRONG](../android/security/keystore/KeyProperties.md), and [android.security.keystore.KeyProperties#AUTH_DEVICE_CREDENTIAL](../android/security/keystore/KeyProperties.md) |

### getUserAuthenticationValidityDurationSeconds

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getUserAuthenticationValidityDurationSeconds(): Int
```

Gets the duration of time (seconds) for which this key is authorized to be used after the user is successfully authenticated. This has effect only if user authentication is required (see [isUserAuthenticationRequired()](../android/security/keystore/KeyProtection.md))).

This authorization applies only to secret key and private key operations. Public key operations are not restricted.

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | duration in seconds or`-1`if authentication is required for every use of the key. |

**See Also**

- <https://developer.android.com/reference/kotlin/android/security/keystore/KeyProtection#isUserAuthenticationRequired()>
- [android.security.keystore.KeyProtection.Builder#setUserAuthenticationValidityDurationSeconds(int)](../android/security/keystore/KeyProtection.Builder.md)) 

### isDigestsSpecified

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isDigestsSpecified(): Boolean
```

Returns`true`if the set of digest algorithms with which the key can be used has been specified. 
**See Also**

- <https://developer.android.com/reference/kotlin/android/security/keystore/KeyProtection#getDigests()> 

### isInvalidatedByBiometricEnrollment

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isInvalidatedByBiometricEnrollment(): Boolean
```

Returns`true`if the key is irreversibly invalidated when a new biometric is enrolled or all enrolled biometrics are removed. This has effect only for keys that require biometric user authentication for every use. 
**See Also**

- <https://developer.android.com/reference/kotlin/android/security/keystore/KeyProtection#isUserAuthenticationRequired()>
- <https://developer.android.com/reference/kotlin/android/security/keystore/KeyProtection#getUserAuthenticationValidityDurationSeconds()>
- [android.security.keystore.KeyProtection.Builder#setInvalidatedByBiometricEnrollment(boolean)](../android/security/keystore/KeyProtection.Builder.md)) 

### isMgf1DigestsSpecified

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isMgf1DigestsSpecified(): Boolean
```

Returns`true`if the set of digests for the MGF1 mask generation function, with which the key can be used, has been specified. Useful with the`RSA-OAEP`scheme.

| Return ||
|------------------------------------------------------------------------------------|-----------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | This value cannot be`null`. |

**See Also**

- <https://developer.android.com/reference/kotlin/android/security/keystore/KeyProtection#getMgf1Digests()> 

### isRandomizedEncryptionRequired

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isRandomizedEncryptionRequired(): Boolean
```

Returns`true`if encryption using this key must be sufficiently randomized to produce different ciphertexts for the same plaintext every time. The formal cryptographic property being required is*indistinguishability under chosen-plaintext attack (`IND-CPA`)*. This property is important because it mitigates several classes of weaknesses due to which ciphertext may leak information about plaintext. For example, if a given plaintext always produces the same ciphertext, an attacker may see the repeated ciphertexts and be able to deduce something about the plaintext. 

### isUnlockedDeviceRequired

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isUnlockedDeviceRequired(): Boolean
```

Returns`true`if the key is authorized to be used only while the device is unlocked. 
**See Also**

- [android.security.keystore.KeyProtection.Builder#setUnlockedDeviceRequired(boolean)](../android/security/keystore/KeyProtection.Builder.md)) 

### isUserAuthenticationRequired

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isUserAuthenticationRequired(): Boolean
```

Returns`true`if the key is authorized to be used only if the user has been authenticated.

This authorization applies only to secret key and private key operations. Public key operations are not restricted. 
**See Also**

- <https://developer.android.com/reference/kotlin/android/security/keystore/KeyProtection#getUserAuthenticationValidityDurationSeconds()>
- [android.security.keystore.KeyProtection.Builder#setUserAuthenticationRequired(boolean)](../android/security/keystore/KeyProtection.Builder.md)) 

### isUserAuthenticationValidWhileOnBody

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isUserAuthenticationValidWhileOnBody(): Boolean
```

Returns`true`if the key will be de-authorized when the device is removed from the user's body. This option has no effect on keys that don't have an authentication validity duration, and has no effect if the device lacks an on-body sensor.

Authorization applies only to secret key and private key operations. Public key operations are not restricted. 
**See Also**

- <https://developer.android.com/reference/kotlin/android/security/keystore/KeyProtection#isUserAuthenticationRequired()>
- <https://developer.android.com/reference/kotlin/android/security/keystore/KeyProtection#getUserAuthenticationValidityDurationSeconds()>
- [android.security.keystore.KeyProtection.Builder#setUserAuthenticationValidWhileOnBody(boolean)](../android/security/keystore/KeyProtection.Builder.md)) 

### isUserConfirmationRequired

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isUserConfirmationRequired(): Boolean
```

Returns`true`if the key is authorized to be used only for messages confirmed by the user. Confirmation is separate from user authentication (see [isUserAuthenticationRequired()](../android/security/keystore/KeyProtection.md))). Keys can be created that require confirmation but not user authentication, or user authentication but not confirmation, or both. Confirmation verifies that some user with physical possession of the device has approved a displayed message. User authentication verifies that the correct user is present and has authenticated.

This authorization applies only to secret key and private key operations. Public key operations are not restricted. 
**See Also**

- [android.security.keystore.KeyProtection.Builder#setUserConfirmationRequired(boolean)](../android/security/keystore/KeyProtection.Builder.md)) 

### isUserPresenceRequired

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isUserPresenceRequired(): Boolean
```

Returns`true`if the key is authorized to be used only if a test of user presence has been performed between the`Signature.initSign()`and`Signature.sign()`calls. It requires that the KeyStore implementation have a direct way to validate the user presence for example a KeyStore hardware backed strongbox can use a button press that is observable in hardware. A test for user presence is tangential to authentication. The test can be part of an authentication step as long as this step can be validated by the hardware protecting the key and cannot be spoofed. For example, a physical button press can be used as a test of user presence if the other pins connected to the button are not able to simulate a button press. There must be no way for the primary processor to fake a button press, or that button must not be used as a test of user presence.
