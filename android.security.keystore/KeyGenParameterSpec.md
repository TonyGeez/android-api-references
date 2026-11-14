Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# KeyGenParameterSpec

```
class KeyGenParameterSpec : AlgorithmParameterSpec
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.security.keystore.KeyGenParameterSpec](KeyGenParameterSpec.md) |

`https://developer.android.com/reference/kotlin/java/security/spec/AlgorithmParameterSpec.html#` for initializing a `https://developer.android.com/reference/kotlin/java/security/KeyPairGenerator.html#` or a `https://developer.android.com/reference/kotlin/javax/crypto/KeyGenerator.html#` of the [Android Keystore system](https://developer.android.com/training/articles/keystore.html). The spec determines authorized uses of the key, such as whether user authentication is required for using the key, what operations are authorized (e.g., signing, but not decryption), with what parameters (e.g., only with a particular padding scheme or digest), and the key's validity start and end dates. Key use authorizations expressed in the spec apply only to secret keys and private keys -- public keys can be used for any supported operations.

To generate an asymmetric key pair or a symmetric key, create an instance of this class using the `https://developer.android.com/reference/kotlin/android/security/keystore/KeyGenParameterSpec.Builder`, initialize a `KeyPairGenerator` or a `KeyGenerator` of the desired key type (e.g., `EC` or `AES` -- see `https://developer.android.com/reference/kotlin/android/security/keystore/KeyProperties`.`KEY_ALGORITHM` constants) from the `AndroidKeyStore` provider with the `KeyGenParameterSpec` instance, and then generate a key or key pair using `https://developer.android.com/reference/kotlin/javax/crypto/KeyGenerator.html#generateKey()` or `https://developer.android.com/reference/kotlin/java/security/KeyPairGenerator.html#generateKeyPair()`.

The generated key pair or key will be returned by the generator and also stored in the Android Keystore under the alias specified in this spec. To obtain the secret or private key from the Android Keystore use `https://developer.android.com/reference/kotlin/java/security/KeyStore.html#getKey(kotlin.String,%20kotlin.CharArray)` or `https://developer.android.com/reference/kotlin/java/security/KeyStore.html#getEntry(kotlin.String,%20java.security.KeyStore.ProtectionParameter)`. To obtain the public key from the Android Keystore use `https://developer.android.com/reference/kotlin/java/security/KeyStore.html#getCertificate(kotlin.String)` and then `https://developer.android.com/reference/kotlin/java/security/cert/Certificate.html#getPublicKey()`.

To help obtain algorithm-specific public parameters of key pairs stored in the Android Keystore, generated private keys implement `https://developer.android.com/reference/kotlin/java/security/interfaces/ECKey.html#` or `https://developer.android.com/reference/kotlin/java/security/interfaces/RSAKey.html#` interfaces whereas public keys implement `https://developer.android.com/reference/kotlin/java/security/interfaces/ECPublicKey.html#` or `https://developer.android.com/reference/kotlin/java/security/interfaces/RSAPublicKey.html#` interfaces.

For asymmetric key pairs, a X.509 certificate will be also generated and stored in the Android Keystore. This is because the `https://developer.android.com/reference/kotlin/java/security/KeyStore.html#` abstraction does not support storing key pairs without a certificate. The subject, serial number, and validity dates of the certificate can be customized in this spec. The certificate may be replaced at a later time by a certificate signed by a Certificate Authority (CA).

NOTE: If attestation is not requested using `https://developer.android.com/reference/kotlin/android/security/keystore/KeyGenParameterSpec.Builder#setAttestationChallenge(kotlin.ByteArray)`, generated certificate may be self-signed. If a private key is not authorized to sign the certificate, then the certificate will be created with an invalid signature which will not verify. Such a certificate is still useful because it provides access to the public key. To generate a valid signature for the certificate the key needs to be authorized for all of the following:

- `https://developer.android.com/reference/kotlin/android/security/keystore/KeyProperties#PURPOSE_SIGN:kotlin.Int`,
- operation without requiring the user to be authenticated (see `https://developer.android.com/reference/kotlin/android/security/keystore/KeyGenParameterSpec.Builder#setUserAuthenticationRequired(kotlin.Boolean)`),
- signing/origination at this moment in time (see `https://developer.android.com/reference/kotlin/android/security/keystore/KeyGenParameterSpec.Builder#setKeyValidityStart(java.util.Date)` and `https://developer.android.com/reference/kotlin/android/security/keystore/KeyGenParameterSpec.Builder#setKeyValidityForOriginationEnd(java.util.Date)`),
- suitable digest,
- (RSA keys only) padding scheme `https://developer.android.com/reference/kotlin/android/security/keystore/KeyProperties#SIGNATURE_PADDING_RSA_PKCS1:kotlin.String`.

NOTE: The key material of the generated symmetric and private keys is not accessible. The key material of the public keys is accessible.

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

### Example: NIST P-256 EC key pair for signing/verification using ECDSA

This example illustrates how to generate a NIST P-256 (aka secp256r1 aka prime256v1) EC key pair in the Android KeyStore system under alias `key1` where the private key is authorized to be used only for signing using SHA-256, SHA-384, or SHA-512 digest and only if the user has been authenticated within the last five minutes. The use of the public key is unrestricted (See Known Issues).

```kotlin
<code>KeyPairGenerator keyPairGenerator = KeyPairGenerator.getInstance(
          KeyProperties.KEY_ALGORITHM_EC, "AndroidKeyStore");
  keyPairGenerator.initialize(
          new KeyGenParameterSpec.Builder(
                  "key1",
                  KeyProperties.PURPOSE_SIGN)
                  .setAlgorithmParameterSpec(new ECGenParameterSpec("secp256r1"))
                  .setDigests(KeyProperties.DIGEST_SHA256,
                          KeyProperties.DIGEST_SHA384,
                          KeyProperties.DIGEST_SHA512)
                  // Only permit the private key to be used if the user authenticated
                  // within the last five minutes.
                  .setUserAuthenticationRequired(true)
                  .setUserAuthenticationValidityDurationSeconds(5 * 60)
                  .build());
  KeyPair keyPair = keyPairGenerator.generateKeyPair();
  Signature signature = Signature.getInstance("SHA256withECDSA");
  signature.initSign(keyPair.getPrivate());
  ...
 
  // The key pair can also be obtained from the Android Keystore any time as follows:
  KeyStore keyStore = KeyStore.getInstance("AndroidKeyStore");
  keyStore.load(null);
  PrivateKey privateKey = (PrivateKey) keyStore.getKey("key1", null);
  PublicKey publicKey = keyStore.getCertificate("key1").getPublicKey();
  </code>
```

<br />

### Example: RSA key pair for signing/verification using RSA-PSS

This example illustrates how to generate an RSA key pair in the Android KeyStore system under alias `key1` authorized to be used only for signing using the RSA-PSS signature padding scheme with SHA-256 or SHA-512 digests. The use of the public key is unrestricted.

```kotlin
<code>KeyPairGenerator keyPairGenerator = KeyPairGenerator.getInstance(
          KeyProperties.KEY_ALGORITHM_RSA, "AndroidKeyStore");
  keyPairGenerator.initialize(
          new KeyGenParameterSpec.Builder(
                  "key1",
                  KeyProperties.PURPOSE_SIGN)
                  .setDigests(KeyProperties.DIGEST_SHA256, KeyProperties.DIGEST_SHA512)
                  .setSignaturePaddings(KeyProperties.SIGNATURE_PADDING_RSA_PSS)
                  .build());
  KeyPair keyPair = keyPairGenerator.generateKeyPair();
  Signature signature = Signature.getInstance("SHA256withRSA/PSS");
  signature.initSign(keyPair.getPrivate());
  ...
 
  // The key pair can also be obtained from the Android Keystore any time as follows:
  KeyStore keyStore = KeyStore.getInstance("AndroidKeyStore");
  keyStore.load(null);
  PrivateKey privateKey = (PrivateKey) keyStore.getKey("key1", null);
  PublicKey publicKey = keyStore.getCertificate("key1").getPublicKey();
  </code>
```

<br />

### Example: RSA key pair for encryption/decryption using RSA OAEP

This example illustrates how to generate an RSA key pair in the Android KeyStore system under alias `key1` where the private key is authorized to be used only for decryption using RSA OAEP encryption padding scheme with SHA-256 or SHA-512 digests. The use of the public key is unrestricted.

```kotlin
<code>KeyPairGenerator keyPairGenerator = KeyPairGenerator.getInstance(
          KeyProperties.KEY_ALGORITHM_RSA, "AndroidKeyStore");
  keyPairGenerator.initialize(
          new KeyGenParameterSpec.Builder(
                  "key1",
                  KeyProperties.PURPOSE_DECRYPT)
                  .setDigests(KeyProperties.DIGEST_SHA256, KeyProperties.DIGEST_SHA512)
                  .setEncryptionPaddings(KeyProperties.ENCRYPTION_PADDING_RSA_OAEP)
                  .build());
  KeyPair keyPair = keyPairGenerator.generateKeyPair();
  Cipher cipher = Cipher.getInstance("RSA/ECB/OAEPWithSHA-256AndMGF1Padding");
  cipher.init(Cipher.DECRYPT_MODE, keyPair.getPrivate());
  ...
 
  // The key pair can also be obtained from the Android Keystore any time as follows:
  KeyStore keyStore = KeyStore.getInstance("AndroidKeyStore");
  keyStore.load(null);
  PrivateKey privateKey = (PrivateKey) keyStore.getKey("key1", null);
  PublicKey publicKey = keyStore.getCertificate("key1").getPublicKey();
  </code>
```

<br />

### Example: AES key for encryption/decryption in GCM mode

The following example illustrates how to generate an AES key in the Android KeyStore system under alias `key2` authorized to be used only for encryption/decryption in GCM mode with no padding.

```kotlin
<code>KeyGenerator keyGenerator = KeyGenerator.getInstance(
          KeyProperties.KEY_ALGORITHM_AES, "AndroidKeyStore");
  keyGenerator.init(
          new KeyGenParameterSpec.Builder("key2",
                  KeyProperties.PURPOSE_ENCRYPT | KeyProperties.PURPOSE_DECRYPT)
                  .setBlockModes(KeyProperties.BLOCK_MODE_GCM)
                  .setEncryptionPaddings(KeyProperties.ENCRYPTION_PADDING_NONE)
                  .build());
  SecretKey key = keyGenerator.generateKey();
 
  Cipher cipher = Cipher.getInstance("AES/GCM/NoPadding");
  cipher.init(Cipher.ENCRYPT_MODE, key);
  ...
 
  // The key can also be obtained from the Android Keystore any time as follows:
  KeyStore keyStore = KeyStore.getInstance("AndroidKeyStore");
  keyStore.load(null);
  key = (SecretKey) keyStore.getKey("key2", null);
  </code>
```

<br />

### Example: HMAC key for generating a MAC using SHA-256

This example illustrates how to generate an HMAC key in the Android KeyStore system under alias `key2` authorized to be used only for generating an HMAC using SHA-256.

```kotlin
<code>KeyGenerator keyGenerator = KeyGenerator.getInstance(
          KeyProperties.KEY_ALGORITHM_HMAC_SHA256, "AndroidKeyStore");
  keyGenerator.init(
          new KeyGenParameterSpec.Builder("key2", KeyProperties.PURPOSE_SIGN).build());
  SecretKey key = keyGenerator.generateKey();
  Mac mac = Mac.getInstance("HmacSHA256");
  mac.init(key);
  ...
 
  // The key can also be obtained from the Android Keystore any time as follows:
  KeyStore keyStore = KeyStore.getInstance("AndroidKeyStore");
  keyStore.load(null);
  key = (SecretKey) keyStore.getKey("key2", null);
  </code>
```

<br />

### Example: EC key for ECDH key agreement

This example illustrates how to generate an elliptic curve key pair, used to establish a shared secret with another party using ECDH key agreement.

```kotlin
<code>KeyPairGenerator keyPairGenerator = KeyPairGenerator.getInstance(
          KeyProperties.KEY_ALGORITHM_EC, "AndroidKeyStore");
  keyPairGenerator.initialize(
          new KeyGenParameterSpec.Builder(
              "eckeypair",
              KeyProperties.PURPOSE_AGREE_KEY)
              .setAlgorithmParameterSpec(new ECGenParameterSpec("secp256r1"))
              .build());
  KeyPair myKeyPair = keyPairGenerator.generateKeyPair();
 
  // Exchange public keys with server. A new ephemeral key MUST be used for every message.
  PublicKey serverEphemeralPublicKey; // Ephemeral key received from server.
 
  // Create a shared secret based on our private key and the other party's public key.
  KeyAgreement keyAgreement = KeyAgreement.getInstance("ECDH", "AndroidKeyStore");
  keyAgreement.init(myKeyPair.getPrivate());
  keyAgreement.doPhase(serverEphemeralPublicKey, true);
  byte[] sharedSecret = keyAgreement.generateSecret();
 
  // sharedSecret cannot safely be used as a key yet. We must run it through a key derivation
  // function with some other data: "salt" and "info". Salt is an optional random value,
  // omitted in this example. It's good practice to include both public keys and any other
  // key negotiation data in info. Here we use the public keys and a label that indicates
  // messages encrypted with this key are coming from the server.
  byte[] salt = {};
  ByteArrayOutputStream info = new ByteArrayOutputStream();
  info.write("ECDH secp256r1 AES-256-GCM-SIV\0".getBytes(StandardCharsets.UTF_8));
  info.write(myKeyPair.getPublic().getEncoded());
  info.write(serverEphemeralPublicKey.getEncoded());
 
  // This example uses the Tink library and the HKDF key derivation function.
  AesGcmSiv key = new AesGcmSiv(Hkdf.computeHkdf(
          "HMACSHA256", sharedSecret, salt, info.toByteArray(), 32));
  byte[] associatedData = {};
  return key.decrypt(ciphertext, associatedData);
  </code>
```

<br />

### Example: ML-DSA key pair for signing

This example illustrates how to generate an ML-DSA key pair in the Android KeyStore system under alias `key1` authorized to be used only for signing. The use of the public key is unrestricted.

The generated key pair will use the ML-DSA-65 parameter set if the `KeyPairGenerator` is instantiated with the family name `"ML-DSA"` or the parameter set name `"ML-DSA-65"`. On the other hand, the key pair will use the ML-DSA-87 parameter set only if the `KeyPairGenerator` is instantiated with the parameter set name `"ML-DSA-87"`.

In both cases, it is not required to set the `AlgorithmParameterSpec` or digest in the `KeyGenParameterSpec`. If the `AlgorithmParameterSpec` is set to a non-null value, then the value must match the algorithm name used to instantiate the `KeyPairGenerator`. Specifically, the algorithm name must be `"ML-DSA"` or `"ML-DSA-65"` if `https://developer.android.com/reference/kotlin/java/security/spec/NamedParameterSpec.html#ML_DSA_65:java.security.spec.NamedParameterSpec` is specified, or `"ML-DSA-87"` if `https://developer.android.com/reference/kotlin/java/security/spec/NamedParameterSpec.html#ML_DSA_87:java.security.spec.NamedParameterSpec` is specified.

**Note:** ML-DSA support is only available on devices with a Trusted Execution Environment running KeyMint version \>= 5. Support can be determined by checking that `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_HARDWARE_KEYSTORE:kotlin.String` has a value `>= 500`.

<br />

#### Case 1: ML-DSA-65

```kotlin
<code>// KeyProperties.KEY_ALGORITHM_ML_DSA_65 can also be used here.
  KeyPairGenerator keyPairGenerator = KeyPairGenerator.getInstance(
          KeyProperties.KEY_ALGORITHM_ML_DSA, "AndroidKeyStore");
  keyPairGenerator.initialize(
          new KeyGenParameterSpec.Builder("key1", KeyProperties.PURPOSE_SIGN).build());
  // NamedParameterSpec.ML_DSA_65 and KeyProperties.DIGEST_NONE can optionally be specified:
  // keyPairGenerator.initialize(
  //         new KeyGenParameterSpec.Builder("key1", KeyProperties.PURPOSE_SIGN)
  //                 .setAlgorithmParameterSpec(NamedParameterSpec.ML_DSA_65)
  //                 .setDigests(KeyProperties.DIGEST_NONE)
  //                 .build());
  KeyPair keyPair = keyPairGenerator.generateKeyPair();
  Signature signature = Signature.getInstance("ML-DSA");  // Or "ML-DSA-65"
  signature.initSign(keyPair.getPrivate());
  ...
 
  // The key pair can also be obtained from the Android Keystore any time as follows:
  KeyStore keyStore = KeyStore.getInstance("AndroidKeyStore");
  keyStore.load(null);
  PrivateKey privateKey = (PrivateKey) keyStore.getKey("key1", null);
  PublicKey publicKey = keyStore.getCertificate("key1").getPublicKey();
  </code>
```

<br />

#### Case 2: ML-DSA-87

```kotlin
<code>KeyPairGenerator keyPairGenerator = KeyPairGenerator.getInstance(
          KeyProperties.KEY_ALGORITHM_ML_DSA_87, "AndroidKeyStore");
  keyPairGenerator.initialize(
          new KeyGenParameterSpec.Builder("key1", KeyProperties.PURPOSE_SIGN).build());
  // NamedParameterSpec.ML_DSA_87 and KeyProperties.DIGEST_NONE can optionally be specified:
  // keyPairGenerator.initialize(
  //         new KeyGenParameterSpec.Builder("key1", KeyProperties.PURPOSE_SIGN)
  //                 .setAlgorithmParameterSpec(NamedParameterSpec.ML_DSA_87)
  //                 .setDigests(KeyProperties.DIGEST_NONE)
  //                 .build());
  KeyPair keyPair = keyPairGenerator.generateKeyPair();
  Signature signature = Signature.getInstance("ML-DSA");  // Or "ML-DSA-87"
  signature.initSign(keyPair.getPrivate());
  ...
 
  // The key pair can also be obtained from the Android Keystore any time as follows:
  KeyStore keyStore = KeyStore.getInstance("AndroidKeyStore");
  keyStore.load(null);
  PrivateKey privateKey = (PrivateKey) keyStore.getKey("key1", null);
  PublicKey publicKey = keyStore.getCertificate("key1").getPublicKey();
  </code>
```

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/security/keystore/KeyGenParameterSpec.Builder` Builder of `https://developer.android.com/reference/kotlin/android/security/keystore/KeyGenParameterSpec#` instances. |

| Public methods ||
|---|---|
| [AlgorithmParameterSpec](../java.security.spec/AlgorithmParameterSpec.md)? | `https://developer.android.com/reference/kotlin/android/security/keystore/KeyGenParameterSpec#getAlgorithmParameterSpec()()` Returns the key algorithm-specific `https://developer.android.com/reference/kotlin/java/security/spec/AlgorithmParameterSpec.html#` that will be used for creation of the key or `null` if algorithm-specific defaults should be used. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | `https://developer.android.com/reference/kotlin/android/security/keystore/KeyGenParameterSpec#getAttestKeyAlias()()` Returns the alias of the attestation key that will be used to sign the attestation certificate of the generated key. |
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | `https://developer.android.com/reference/kotlin/android/security/keystore/KeyGenParameterSpec#getAttestationChallenge()()` Returns the attestation challenge value that will be placed in attestation certificate for this key pair. |
| --- | --- |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | `https://developer.android.com/reference/kotlin/android/security/keystore/KeyGenParameterSpec#getBlockModes()()` Gets the set of block modes (e.g., |
| [Date](../java.util/Date.md) | `https://developer.android.com/reference/kotlin/android/security/keystore/KeyGenParameterSpec#getCertificateNotAfter()()` Returns the end date to be used on the X. |
| [Date](../java.util/Date.md) | `https://developer.android.com/reference/kotlin/android/security/keystore/KeyGenParameterSpec#getCertificateNotBefore()()` Returns the start date to be used on the X. |
| --- | --- |
| [BigInteger](../java.math/BigInteger.md) | `https://developer.android.com/reference/kotlin/android/security/keystore/KeyGenParameterSpec#getCertificateSerialNumber()()` Returns the serial number to be used on the X. |
| [X500Principal](../javax.security.auth.x500/X500Principal.md) | `https://developer.android.com/reference/kotlin/android/security/keystore/KeyGenParameterSpec#getCertificateSubject()()` Returns the subject distinguished name to be used on the X. |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | `https://developer.android.com/reference/kotlin/android/security/keystore/KeyGenParameterSpec#getDigests()()` Returns the set of digest algorithms (e.g., |
| --- | --- |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | `https://developer.android.com/reference/kotlin/android/security/keystore/KeyGenParameterSpec#getEncryptionPaddings()()` Returns the set of padding schemes (e.g., |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/security/keystore/KeyGenParameterSpec#getKeySize()()` Returns the requested key size. |
| [Date](../java.util/Date.md)? | `https://developer.android.com/reference/kotlin/android/security/keystore/KeyGenParameterSpec#getKeyValidityForConsumptionEnd()()` Returns the time instant after which the key is no longer valid for decryption and verification or `null` if not restricted. |
| --- | --- |
| [Date](../java.util/Date.md)? | `https://developer.android.com/reference/kotlin/android/security/keystore/KeyGenParameterSpec#getKeyValidityForOriginationEnd()()` Returns the time instant after which the key is no longer valid for encryption and signing or `null` if not restricted. |
| [Date](../java.util/Date.md)? | `https://developer.android.com/reference/kotlin/android/security/keystore/KeyGenParameterSpec#getKeyValidityStart()()` Returns the time instant before which the key is not yet valid or `null` if not restricted. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/security/keystore/KeyGenParameterSpec#getKeystoreAlias()()` Returns the alias that will be used in the `java.security.KeyStore` in conjunction with the `AndroidKeyStore`. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/security/keystore/KeyGenParameterSpec#getMaxUsageCount()()` Returns the maximum number of times the limited use key is allowed to be used or `https://developer.android.com/reference/kotlin/android/security/keystore/KeyProperties#UNRESTRICTED_USAGE_COUNT:kotlin.Int` if there's no restriction on the number of times the key can be used. |
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | `https://developer.android.com/reference/kotlin/android/security/keystore/KeyGenParameterSpec#getMgf1Digests()()` Returns the set of digests that can be used by the MGF1 mask generation function (e.g., |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/security/keystore/KeyGenParameterSpec#getPurposes()()` Returns the set of purposes (e.g., encrypt, decrypt, sign) for which the key can be used. |
| --- | --- |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | `https://developer.android.com/reference/kotlin/android/security/keystore/KeyGenParameterSpec#getSignaturePaddings()()` Gets the set of padding schemes (e.g., |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/security/keystore/KeyGenParameterSpec#getUserAuthenticationType()()` Gets the modes of authentication that can authorize use of this key. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/security/keystore/KeyGenParameterSpec#getUserAuthenticationValidityDurationSeconds()()` Gets the duration of time (seconds) for which this key is authorized to be used after the user is successfully authenticated. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/security/keystore/KeyGenParameterSpec#isDevicePropertiesAttestationIncluded()()` Returns `true` if attestation for the base device properties (`https://developer.android.com/reference/kotlin/android/os/Build.html#BRAND:kotlin.String`, `https://developer.android.com/reference/kotlin/android/os/Build.html#DEVICE:kotlin.String`, `https://developer.android.com/reference/kotlin/android/os/Build.html#MANUFACTURER:kotlin.String`, `https://developer.android.com/reference/kotlin/android/os/Build.html#MODEL:kotlin.String`, `https://developer.android.com/reference/kotlin/android/os/Build.html#PRODUCT:kotlin.String`) was requested to be added in the attestation certificate for the generated key. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/security/keystore/KeyGenParameterSpec#isDigestsSpecified()()` Returns `true` if the set of digest algorithms with which the key can be used has been specified. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/security/keystore/KeyGenParameterSpec#isInvalidatedByBiometricEnrollment()()` Returns `true` if the key is irreversibly invalidated when a new biometric is enrolled or all enrolled biometrics are removed. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/security/keystore/KeyGenParameterSpec#isMgf1DigestsSpecified()()` Returns `true` if the set of digests for the MGF1 mask generation function, with which the key can be used, has been specified. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/security/keystore/KeyGenParameterSpec#isRandomizedEncryptionRequired()()` Returns `true` if encryption using this key must be sufficiently randomized to produce different ciphertexts for the same plaintext every time. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/security/keystore/KeyGenParameterSpec#isStrongBoxBacked()()` Returns `true` if the key is protected by a Strongbox security chip. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/security/keystore/KeyGenParameterSpec#isUnlockedDeviceRequired()()` Returns `true` if the key is authorized to be used only while the device is unlocked. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/security/keystore/KeyGenParameterSpec#isUserAuthenticationRequired()()` Returns `true` if the key is authorized to be used only if the user has been authenticated. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/security/keystore/KeyGenParameterSpec#isUserAuthenticationValidWhileOnBody()()` Returns `true` if the key will remain authorized only until the device is removed from the user's body, up to the validity duration. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/security/keystore/KeyGenParameterSpec#isUserConfirmationRequired()()` Returns `true` if the key is authorized to be used only for messages confirmed by the user. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/security/keystore/KeyGenParameterSpec#isUserPresenceRequired()()` Returns `true` if the key is authorized to be used only if a test of user presence has been performed between the `Signature.initSign()` and `Signature.sign()` calls. |

## Public methods

### getAlgorithmParameterSpec

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getAlgorithmParameterSpec(): AlgorithmParameterSpec?
```

Returns the key algorithm-specific `https://developer.android.com/reference/kotlin/java/security/spec/AlgorithmParameterSpec.html#` that will be used for creation of the key or `null` if algorithm-specific defaults should be used.

### getAttestKeyAlias

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getAttestKeyAlias(): String?
```

Returns the alias of the attestation key that will be used to sign the attestation certificate of the generated key. Note that an attestation certificate will only be generated if an attestation challenge is set.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?` | This value may be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/security/keystore/KeyGenParameterSpec.Builder#setAttestKeyAlias(kotlin.String)`

### getAttestationChallenge

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getAttestationChallenge(): ByteArray!
```

Returns the attestation challenge value that will be placed in attestation certificate for this key pair.

If this method returns non-`null`, the public key certificate for this key pair will contain an extension that describes the details of the key's configuration and authorizations, including the content of the attestation challenge value. If the key is in secure hardware, and if the secure hardware supports attestation, the certificate will be signed by a chain of certificates rooted at a trustworthy CA key. Otherwise the chain will be rooted at an untrusted certificate.

If this method returns `null`, and the spec is used to generate an asymmetric (RSA or EC) key pair, the public key will have a self-signed certificate if it has purpose `https://developer.android.com/reference/kotlin/android/security/keystore/KeyProperties#PURPOSE_SIGN:kotlin.Int`. If does not have purpose `https://developer.android.com/reference/kotlin/android/security/keystore/KeyProperties#PURPOSE_SIGN:kotlin.Int`, it will have a fake certificate.

Symmetric keys, such as AES and HMAC keys, do not have public key certificates. If a KeyGenParameterSpec with getAttestationChallenge returning non-null is used to generate a symmetric (AES or HMAC) key, `https://developer.android.com/reference/kotlin/javax/crypto/KeyGenerator.html#generateKey()` will throw `https://developer.android.com/reference/kotlin/java/security/InvalidAlgorithmParameterException.html#`.
**See Also**

- `https://developer.android.com/reference/kotlin/android/security/keystore/KeyGenParameterSpec.Builder#setAttestationChallenge(kotlin.ByteArray)`

### getBlockModes

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getBlockModes(): Array<String!>
```

Gets the set of block modes (e.g., `GCM`, `CBC`) with which the key can be used when encrypting/decrypting. Attempts to use the key with any other block modes will be rejected.

See `https://developer.android.com/reference/kotlin/android/security/keystore/KeyProperties`.`BLOCK_MODE` constants.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>` | This value cannot be `null`. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/security/keystore/KeyProperties#BLOCK_MODE_ECB:kotlin.String` - `https://developer.android.com/reference/kotlin/android/security/keystore/KeyProperties#BLOCK_MODE_CBC:kotlin.String` - `https://developer.android.com/reference/kotlin/android/security/keystore/KeyProperties#BLOCK_MODE_CTR:kotlin.String` - `https://developer.android.com/reference/kotlin/android/security/keystore/KeyProperties#BLOCK_MODE_GCM:kotlin.String` |

### getCertificateNotAfter

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getCertificateNotAfter(): Date
```

Returns the end date to be used on the X.509 certificate that will be put in the `https://developer.android.com/reference/kotlin/java/security/KeyStore.html#`.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/Date.html#` | This value cannot be `null`. |

### getCertificateNotBefore

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getCertificateNotBefore(): Date
```

Returns the start date to be used on the X.509 certificate that will be put in the `https://developer.android.com/reference/kotlin/java/security/KeyStore.html#`.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/Date.html#` | This value cannot be `null`. |

### getCertificateSerialNumber

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getCertificateSerialNumber(): BigInteger
```

Returns the serial number to be used on the X.509 certificate that will be put in the `https://developer.android.com/reference/kotlin/java/security/KeyStore.html#`.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/math/BigInteger.html#` | This value cannot be `null`. |

### getCertificateSubject

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getCertificateSubject(): X500Principal
```

Returns the subject distinguished name to be used on the X.509 certificate that will be put in the `https://developer.android.com/reference/kotlin/java/security/KeyStore.html#`.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/javax/security/auth/x500/X500Principal.html#` | This value cannot be `null`. |

### getDigests

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getDigests(): Array<String!>
```

Returns the set of digest algorithms (e.g., `SHA-256`, `SHA-384` with which the key can be used.

See `https://developer.android.com/reference/kotlin/android/security/keystore/KeyProperties`.`DIGEST` constants.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>` | This value cannot be `null`. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/security/keystore/KeyProperties#DIGEST_NONE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/security/keystore/KeyProperties#DIGEST_MD5:kotlin.String` - `https://developer.android.com/reference/kotlin/android/security/keystore/KeyProperties#DIGEST_SHA1:kotlin.String` - `https://developer.android.com/reference/kotlin/android/security/keystore/KeyProperties#DIGEST_SHA224:kotlin.String` - `https://developer.android.com/reference/kotlin/android/security/keystore/KeyProperties#DIGEST_SHA256:kotlin.String` - `https://developer.android.com/reference/kotlin/android/security/keystore/KeyProperties#DIGEST_SHA384:kotlin.String` - `https://developer.android.com/reference/kotlin/android/security/keystore/KeyProperties#DIGEST_SHA512:kotlin.String` |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if this set has not been specified. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/security/keystore/KeyGenParameterSpec#isDigestsSpecified()`

### getEncryptionPaddings

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getEncryptionPaddings(): Array<String!>
```

Returns the set of padding schemes (e.g., `PKCS7Padding`, `OEAPPadding`, `PKCS1Padding`, `NoPadding`) with which the key can be used when encrypting/decrypting. Attempts to use the key with any other padding scheme will be rejected.

See `https://developer.android.com/reference/kotlin/android/security/keystore/KeyProperties`.`ENCRYPTION_PADDING` constants.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>` | This value cannot be `null`. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/security/keystore/KeyProperties#ENCRYPTION_PADDING_NONE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/security/keystore/KeyProperties#ENCRYPTION_PADDING_PKCS7:kotlin.String` - `https://developer.android.com/reference/kotlin/android/security/keystore/KeyProperties#ENCRYPTION_PADDING_RSA_PKCS1:kotlin.String` - `https://developer.android.com/reference/kotlin/android/security/keystore/KeyProperties#ENCRYPTION_PADDING_RSA_OAEP:kotlin.String` |

### getKeySize

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getKeySize(): Int
```

Returns the requested key size. If `-1`, the size should be looked up from `https://developer.android.com/reference/kotlin/android/security/keystore/KeyGenParameterSpec#getAlgorithmParameterSpec()`, if provided, otherwise an algorithm-specific default size should be used.

### getKeyValidityForConsumptionEnd

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getKeyValidityForConsumptionEnd(): Date?
```

Returns the time instant after which the key is no longer valid for decryption and verification or `null` if not restricted.

### getKeyValidityForOriginationEnd

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getKeyValidityForOriginationEnd(): Date?
```

Returns the time instant after which the key is no longer valid for encryption and signing or `null` if not restricted.

### getKeyValidityStart

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getKeyValidityStart(): Date?
```

Returns the time instant before which the key is not yet valid or `null` if not restricted.

### getKeystoreAlias

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getKeystoreAlias(): String
```

Returns the alias that will be used in the `java.security.KeyStore` in conjunction with the `AndroidKeyStore`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | This value cannot be `null`. |

### getMaxUsageCount

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getMaxUsageCount(): Int
```

Returns the maximum number of times the limited use key is allowed to be used or `https://developer.android.com/reference/kotlin/android/security/keystore/KeyProperties#UNRESTRICTED_USAGE_COUNT:kotlin.Int` if there's no restriction on the number of times the key can be used.
**See Also**

- `https://developer.android.com/reference/kotlin/android/security/keystore/KeyGenParameterSpec.Builder#setMaxUsageCount(kotlin.Int)`

### getMgf1Digests

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getMgf1Digests(): MutableSet<String!>
```

Returns the set of digests that can be used by the MGF1 mask generation function (e.g., `SHA-256`, `SHA-384`) with the key. Useful with the `RSA-OAEP` scheme. If not explicitly specified during key generation, the default `SHA-1` digest is used and may be specified when using the key.

See `https://developer.android.com/reference/kotlin/android/security/keystore/KeyProperties`.`DIGEST` constants.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>` | This value cannot be `null`. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/security/keystore/KeyProperties#DIGEST_NONE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/security/keystore/KeyProperties#DIGEST_MD5:kotlin.String` - `https://developer.android.com/reference/kotlin/android/security/keystore/KeyProperties#DIGEST_SHA1:kotlin.String` - `https://developer.android.com/reference/kotlin/android/security/keystore/KeyProperties#DIGEST_SHA224:kotlin.String` - `https://developer.android.com/reference/kotlin/android/security/keystore/KeyProperties#DIGEST_SHA256:kotlin.String` - `https://developer.android.com/reference/kotlin/android/security/keystore/KeyProperties#DIGEST_SHA384:kotlin.String` - `https://developer.android.com/reference/kotlin/android/security/keystore/KeyProperties#DIGEST_SHA512:kotlin.String` |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if this set has not been specified. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/security/keystore/KeyGenParameterSpec#isMgf1DigestsSpecified()`

### getPurposes

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getPurposes(): Int
```

Returns the set of purposes (e.g., encrypt, decrypt, sign) for which the key can be used. Attempts to use the key for any other purpose will be rejected.

See `https://developer.android.com/reference/kotlin/android/security/keystore/KeyProperties`.`PURPOSE` flags.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/security/keystore/KeyProperties#PURPOSE_ENCRYPT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/security/keystore/KeyProperties#PURPOSE_DECRYPT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/security/keystore/KeyProperties#PURPOSE_SIGN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/security/keystore/KeyProperties#PURPOSE_VERIFY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/security/keystore/KeyProperties#PURPOSE_WRAP_KEY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/security/keystore/KeyProperties#PURPOSE_AGREE_KEY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/security/keystore/KeyProperties#PURPOSE_ATTEST_KEY:kotlin.Int` |

### getSignaturePaddings

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getSignaturePaddings(): Array<String!>
```

Gets the set of padding schemes (e.g., `PSS`, `PKCS#1`) with which the key can be used when signing/verifying. Attempts to use the key with any other padding scheme will be rejected.

See `https://developer.android.com/reference/kotlin/android/security/keystore/KeyProperties`.`SIGNATURE_PADDING` constants.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>` | This value cannot be `null`. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/security/keystore/KeyProperties#SIGNATURE_PADDING_RSA_PKCS1:kotlin.String` - `https://developer.android.com/reference/kotlin/android/security/keystore/KeyProperties#SIGNATURE_PADDING_RSA_PSS:kotlin.String` |

### getUserAuthenticationType

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getUserAuthenticationType(): Int
```

Gets the modes of authentication that can authorize use of this key. This has effect only if user authentication is required (see `https://developer.android.com/reference/kotlin/android/security/keystore/KeyGenParameterSpec#isUserAuthenticationRequired()`).

This authorization applies only to secret key and private key operations. Public key operations are not restricted.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | integer representing the bitwse OR of all acceptable authentication types for the key. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/security/keystore/KeyProperties#AUTH_BIOMETRIC_STRONG:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/security/keystore/KeyProperties#AUTH_DEVICE_CREDENTIAL:kotlin.Int` |

**See Also**

- `https://developer.android.com/reference/kotlin/android/security/keystore/KeyGenParameterSpec#isUserAuthenticationRequired()`
- `https://developer.android.com/reference/kotlin/android/security/keystore/KeyGenParameterSpec.Builder#setUserAuthenticationParameters(kotlin.Int,%20kotlin.Int)`

### getUserAuthenticationValidityDurationSeconds

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getUserAuthenticationValidityDurationSeconds(): Int
```

Gets the duration of time (seconds) for which this key is authorized to be used after the user is successfully authenticated. This has effect only if user authentication is required (see `https://developer.android.com/reference/kotlin/android/security/keystore/KeyGenParameterSpec#isUserAuthenticationRequired()`).

This authorization applies only to secret key and private key operations. Public key operations are not restricted.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | duration in seconds or `-1` if authentication is required for every use of the key. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/security/keystore/KeyGenParameterSpec#isUserAuthenticationRequired()`
- `https://developer.android.com/reference/kotlin/android/security/keystore/KeyGenParameterSpec.Builder#setUserAuthenticationValidityDurationSeconds(kotlin.Int)`

### isDevicePropertiesAttestationIncluded

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isDevicePropertiesAttestationIncluded(): Boolean
```

Returns `true` if attestation for the base device properties (`https://developer.android.com/reference/kotlin/android/os/Build.html#BRAND:kotlin.String`, `https://developer.android.com/reference/kotlin/android/os/Build.html#DEVICE:kotlin.String`, `https://developer.android.com/reference/kotlin/android/os/Build.html#MANUFACTURER:kotlin.String`, `https://developer.android.com/reference/kotlin/android/os/Build.html#MODEL:kotlin.String`, `https://developer.android.com/reference/kotlin/android/os/Build.html#PRODUCT:kotlin.String`) was requested to be added in the attestation certificate for the generated key. `https://developer.android.com/reference/kotlin/javax/crypto/KeyGenerator.html#generateKey()` will throw `https://developer.android.com/reference/kotlin/java/security/ProviderException.html#` if device properties attestation fails or is not supported.
**See Also**

- `https://developer.android.com/reference/kotlin/android/security/keystore/KeyGenParameterSpec.Builder#setDevicePropertiesAttestationIncluded(kotlin.Boolean)`

### isDigestsSpecified

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isDigestsSpecified(): Boolean
```

Returns `true` if the set of digest algorithms with which the key can be used has been specified.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/security/keystore/KeyGenParameterSpec#getDigests()`

### isInvalidatedByBiometricEnrollment

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isInvalidatedByBiometricEnrollment(): Boolean
```

Returns `true` if the key is irreversibly invalidated when a new biometric is enrolled or all enrolled biometrics are removed. This has effect only for keys that require biometric user authentication for every use.
**See Also**

- `https://developer.android.com/reference/kotlin/android/security/keystore/KeyGenParameterSpec#isUserAuthenticationRequired()`
- `https://developer.android.com/reference/kotlin/android/security/keystore/KeyGenParameterSpec#getUserAuthenticationValidityDurationSeconds()`
- `https://developer.android.com/reference/kotlin/android/security/keystore/KeyGenParameterSpec.Builder#setInvalidatedByBiometricEnrollment(kotlin.Boolean)`

### isMgf1DigestsSpecified

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isMgf1DigestsSpecified(): Boolean
```

Returns `true` if the set of digests for the MGF1 mask generation function, with which the key can be used, has been specified. Useful with the `RSA-OAEP` scheme.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/security/keystore/KeyGenParameterSpec#getMgf1Digests()`

### isRandomizedEncryptionRequired

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isRandomizedEncryptionRequired(): Boolean
```

Returns `true` if encryption using this key must be sufficiently randomized to produce different ciphertexts for the same plaintext every time. The formal cryptographic property being required is *indistinguishability under chosen-plaintext attack (`IND-CPA`)*. This property is important because it mitigates several classes of weaknesses due to which ciphertext may leak information about plaintext. For example, if a given plaintext always produces the same ciphertext, an attacker may see the repeated ciphertexts and be able to deduce something about the plaintext.

### isStrongBoxBacked

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isStrongBoxBacked(): Boolean
```

Returns `true` if the key is protected by a Strongbox security chip.

### isUnlockedDeviceRequired

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isUnlockedDeviceRequired(): Boolean
```

Returns `true` if the key is authorized to be used only while the device is unlocked.
**See Also**

- `https://developer.android.com/reference/kotlin/android/security/keystore/KeyGenParameterSpec.Builder#setUnlockedDeviceRequired(kotlin.Boolean)`

### isUserAuthenticationRequired

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isUserAuthenticationRequired(): Boolean
```

Returns `true` if the key is authorized to be used only if the user has been authenticated.

This authorization applies only to secret key and private key operations. Public key operations are not restricted.
**See Also**

- `https://developer.android.com/reference/kotlin/android/security/keystore/KeyGenParameterSpec#getUserAuthenticationValidityDurationSeconds()`
- `https://developer.android.com/reference/kotlin/android/security/keystore/KeyGenParameterSpec.Builder#setUserAuthenticationRequired(kotlin.Boolean)`

### isUserAuthenticationValidWhileOnBody

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isUserAuthenticationValidWhileOnBody(): Boolean
```

Returns `true` if the key will remain authorized only until the device is removed from the user's body, up to the validity duration. This option has no effect on keys that don't have an authentication validity duration, and has no effect if the device lacks an on-body sensor.

Authorization applies only to secret key and private key operations. Public key operations are not restricted.
**See Also**

- `https://developer.android.com/reference/kotlin/android/security/keystore/KeyGenParameterSpec#isUserAuthenticationRequired()`
- `https://developer.android.com/reference/kotlin/android/security/keystore/KeyGenParameterSpec#getUserAuthenticationValidityDurationSeconds()`
- `https://developer.android.com/reference/kotlin/android/security/keystore/KeyGenParameterSpec.Builder#setUserAuthenticationValidWhileOnBody(kotlin.Boolean)`

### isUserConfirmationRequired

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isUserConfirmationRequired(): Boolean
```

Returns `true` if the key is authorized to be used only for messages confirmed by the user. Confirmation is separate from user authentication (see `https://developer.android.com/reference/kotlin/android/security/keystore/KeyGenParameterSpec.Builder#setUserAuthenticationRequired(kotlin.Boolean)`). Keys can be created that require confirmation but not user authentication, or user authentication but not confirmation, or both. Confirmation verifies that some user with physical possession of the device has approved a displayed message. User authentication verifies that the correct user is present and has authenticated.

This authorization applies only to secret key and private key operations. Public key operations are not restricted.
**See Also**

- `https://developer.android.com/reference/kotlin/android/security/keystore/KeyGenParameterSpec.Builder#setUserConfirmationRequired(kotlin.Boolean)`

### isUserPresenceRequired

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isUserPresenceRequired(): Boolean
```

Returns `true` if the key is authorized to be used only if a test of user presence has been performed between the `Signature.initSign()` and `Signature.sign()` calls. It requires that the KeyStore implementation have a direct way to validate the user presence for example a KeyStore hardware backed strongbox can use a button press that is observable in hardware. A test for user presence is tangential to authentication. The test can be part of an authentication step as long as this step can be validated by the hardware protecting the key and cannot be spoofed. For example, a physical button press can be used as a test of user presence if the other pins connected to the button are not able to simulate a button press. There must be no way for the primary processor to fake a button press, or that button must not be used as a test of user presence.
