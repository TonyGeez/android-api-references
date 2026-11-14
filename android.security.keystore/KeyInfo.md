# KeyInfo

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# KeyInfo

Kotlin| [Java](https://developer.android.com/reference/android/security/keystore/KeyInfo "View this page in Java") 

```
open class KeyInfo : KeySpec
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.security.keystore.KeyInfo](https://developer.android.com/reference/kotlin/android/security/keystore/KeyInfo#) |

Information about a key from the [Android Keystore system](https://developer.android.com/training/articles/keystore.html). This class describes whether the key material is available in plaintext outside of secure hardware, whether user authentication is required for using the key and whether this requirement is enforced by secure hardware, the key's origin, what uses the key is authorized for (e.g., only in`GCM`mode, or signing only), whether the key should be encrypted at rest, the key's and validity start and end dates.

Instances of this class are immutable.

<br />

### Example: Symmetric Key

The following example illustrates how to obtain a`KeyInfo`describing the provided Android Keystore [SecretKey](https://developer.android.com/reference/kotlin/javax/crypto/SecretKey.html#). 

```kotlin
<code>SecretKey key = ...; // Android Keystore key
 
  SecretKeyFactory factory = SecretKeyFactory.getInstance(key.getAlgorithm(), "AndroidKeyStore");
  KeyInfo keyInfo;
  try {
      keyInfo = (KeyInfo) factory.getKeySpec(key, KeyInfo.class);
  } catch (InvalidKeySpecException e) {
      // Not an Android KeyStore key.
  }</code>
```

<br />

### Example: Private Key

The following example illustrates how to obtain a`KeyInfo`describing the provided Android KeyStore [PrivateKey](https://developer.android.com/reference/kotlin/java/security/PrivateKey.html#). 

```kotlin
<code>PrivateKey key = ...; // Android KeyStore key
 
  KeyFactory factory = KeyFactory.getInstance(key.getAlgorithm(), "AndroidKeyStore");
  KeyInfo keyInfo;
  try {
      keyInfo = factory.getKeySpec(key, KeyInfo.class);
  } catch (InvalidKeySpecException e) {
      // Not an Android KeyStore key.
  }</code>
```

## Summary

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | [getBlockModes](https://developer.android.com/reference/kotlin/android/security/keystore/KeyInfo#getBlockModes())`()` Gets the set of block modes (e.g., |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | [getDigests](https://developer.android.com/reference/kotlin/android/security/keystore/KeyInfo#getDigests())`()` Gets the set of digest algorithms (e.g., |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | [getEncryptionPaddings](https://developer.android.com/reference/kotlin/android/security/keystore/KeyInfo#getEncryptionPaddings())`()` Gets the set of padding schemes (e.g., |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getKeySize](https://developer.android.com/reference/kotlin/android/security/keystore/KeyInfo#getKeySize())`()` Gets the size of the key in bits. |
| open [Date](https://developer.android.com/reference/kotlin/java/util/Date.html#)? | [getKeyValidityForConsumptionEnd](https://developer.android.com/reference/kotlin/android/security/keystore/KeyInfo#getKeyValidityForConsumptionEnd())`()` Gets the time instant after which the key is no long valid for decryption and verification. |
| open [Date](https://developer.android.com/reference/kotlin/java/util/Date.html#)? | [getKeyValidityForOriginationEnd](https://developer.android.com/reference/kotlin/android/security/keystore/KeyInfo#getKeyValidityForOriginationEnd())`()` Gets the time instant after which the key is no long valid for encryption and signing. |
| open [Date](https://developer.android.com/reference/kotlin/java/util/Date.html#)? | [getKeyValidityStart](https://developer.android.com/reference/kotlin/android/security/keystore/KeyInfo#getKeyValidityStart())`()` Gets the time instant before which the key is not yet valid. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getKeystoreAlias](https://developer.android.com/reference/kotlin/android/security/keystore/KeyInfo#getKeystoreAlias())`()` Gets the entry alias under which the key is stored in the`AndroidKeyStore`. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getOrigin](https://developer.android.com/reference/kotlin/android/security/keystore/KeyInfo#getOrigin())`()` Gets the origin of the key. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPurposes](https://developer.android.com/reference/kotlin/android/security/keystore/KeyInfo#getPurposes())`()` Gets the set of purposes (e.g., encrypt, decrypt, sign) for which the key can be used. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getRemainingUsageCount](https://developer.android.com/reference/kotlin/android/security/keystore/KeyInfo#getRemainingUsageCount())`()` Returns the remaining number of times the key is allowed to be used or [KeyProperties.UNRESTRICTED_USAGE_COUNT](https://developer.android.com/reference/kotlin/android/security/keystore/KeyProperties#UNRESTRICTED_USAGE_COUNT:kotlin.Int) if there's no restriction on the number of times the key can be used. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSecurityLevel](https://developer.android.com/reference/kotlin/android/security/keystore/KeyInfo#getSecurityLevel())`()` Returns the security level that the key is protected by. |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | [getSignaturePaddings](https://developer.android.com/reference/kotlin/android/security/keystore/KeyInfo#getSignaturePaddings())`()` Gets the set of padding schemes (e.g., |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getUserAuthenticationType](https://developer.android.com/reference/kotlin/android/security/keystore/KeyInfo#getUserAuthenticationType())`()` Gets the acceptable user authentication types for which this key can be authorized to be used. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getUserAuthenticationValidityDurationSeconds](https://developer.android.com/reference/kotlin/android/security/keystore/KeyInfo#getUserAuthenticationValidityDurationSeconds())`()` Gets the duration of time (seconds) for which this key is authorized to be used after the user is successfully authenticated. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isInsideSecureHardware](https://developer.android.com/reference/kotlin/android/security/keystore/KeyInfo#isInsideSecureHardware())`()` Returns`true`if the key resides inside secure hardware (e.g., Trusted Execution Environment (TEE) or Secure Element (SE)). |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isInvalidatedByBiometricEnrollment](https://developer.android.com/reference/kotlin/android/security/keystore/KeyInfo#isInvalidatedByBiometricEnrollment())`()` Returns`true`if the key will be invalidated by enrollment of a new fingerprint or removal of all fingerprints. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isTrustedUserPresenceRequired](https://developer.android.com/reference/kotlin/android/security/keystore/KeyInfo#isTrustedUserPresenceRequired())`()` Returns`true`if the key can only be only be used if a test for user presence has succeeded since Signature. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isUnlockedDeviceRequired](https://developer.android.com/reference/kotlin/android/security/keystore/KeyInfo#isUnlockedDeviceRequired())`()` Returns`true`if the key is authorized to be used only while the device is unlocked. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isUserAuthenticationRequired](https://developer.android.com/reference/kotlin/android/security/keystore/KeyInfo#isUserAuthenticationRequired())`()` Returns`true`if the key is authorized to be used only if the user has been authenticated. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isUserAuthenticationRequirementEnforcedBySecureHardware](https://developer.android.com/reference/kotlin/android/security/keystore/KeyInfo#isUserAuthenticationRequirementEnforcedBySecureHardware())`()` Returns`true`if the requirement that this key can only be used if the user has been authenticated is enforced by secure hardware (e.g., Trusted Execution Environment (TEE) or Secure Element (SE)). |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isUserAuthenticationValidWhileOnBody](https://developer.android.com/reference/kotlin/android/security/keystore/KeyInfo#isUserAuthenticationValidWhileOnBody())`()` Returns`true`if this key will become unusable when the device is removed from the user's body. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isUserConfirmationRequired](https://developer.android.com/reference/kotlin/android/security/keystore/KeyInfo#isUserConfirmationRequired())`()` Returns`true`if the key is authorized to be used only for messages confirmed by the user. |

## Public methods

### getBlockModes

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getBlockModes(): Array<String!>
```

Gets the set of block modes (e.g.,`GCM`,`CBC`) with which the key can be used when encrypting/decrypting. Attempts to use the key with any other block modes will be rejected.

See [KeyProperties](https://developer.android.com/reference/kotlin/android/security/keystore/KeyProperties).`BLOCK_MODE`constants.

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!> | This value cannot be`null`. Value is [android.security.keystore.KeyProperties#BLOCK_MODE_ECB](https://developer.android.com/reference/kotlin/android/security/keystore/KeyProperties#BLOCK_MODE_ECB:kotlin.String), [android.security.keystore.KeyProperties#BLOCK_MODE_CBC](https://developer.android.com/reference/kotlin/android/security/keystore/KeyProperties#BLOCK_MODE_CBC:kotlin.String), [android.security.keystore.KeyProperties#BLOCK_MODE_CTR](https://developer.android.com/reference/kotlin/android/security/keystore/KeyProperties#BLOCK_MODE_CTR:kotlin.String), or [android.security.keystore.KeyProperties#BLOCK_MODE_GCM](https://developer.android.com/reference/kotlin/android/security/keystore/KeyProperties#BLOCK_MODE_GCM:kotlin.String) |

### getDigests

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDigests(): Array<String!>
```

Gets the set of digest algorithms (e.g.,`SHA-256`,`SHA-384`) with which the key can be used.

See [KeyProperties](https://developer.android.com/reference/kotlin/android/security/keystore/KeyProperties).`DIGEST`constants.

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!> | This value cannot be`null`. Value is [android.security.keystore.KeyProperties#DIGEST_NONE](https://developer.android.com/reference/kotlin/android/security/keystore/KeyProperties#DIGEST_NONE:kotlin.String), [android.security.keystore.KeyProperties#DIGEST_MD5](https://developer.android.com/reference/kotlin/android/security/keystore/KeyProperties#DIGEST_MD5:kotlin.String), [android.security.keystore.KeyProperties#DIGEST_SHA1](https://developer.android.com/reference/kotlin/android/security/keystore/KeyProperties#DIGEST_SHA1:kotlin.String), [android.security.keystore.KeyProperties#DIGEST_SHA224](https://developer.android.com/reference/kotlin/android/security/keystore/KeyProperties#DIGEST_SHA224:kotlin.String), [android.security.keystore.KeyProperties#DIGEST_SHA256](https://developer.android.com/reference/kotlin/android/security/keystore/KeyProperties#DIGEST_SHA256:kotlin.String), [android.security.keystore.KeyProperties#DIGEST_SHA384](https://developer.android.com/reference/kotlin/android/security/keystore/KeyProperties#DIGEST_SHA384:kotlin.String), or [android.security.keystore.KeyProperties#DIGEST_SHA512](https://developer.android.com/reference/kotlin/android/security/keystore/KeyProperties#DIGEST_SHA512:kotlin.String) |

### getEncryptionPaddings

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getEncryptionPaddings(): Array<String!>
```

Gets the set of padding schemes (e.g.,`PKCS7Padding`,`PKCS1Padding`,`NoPadding`) with which the key can be used when encrypting/decrypting. Attempts to use the key with any other padding scheme will be rejected.

See [KeyProperties](https://developer.android.com/reference/kotlin/android/security/keystore/KeyProperties).`ENCRYPTION_PADDING`constants.

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!> | This value cannot be`null`. Value is [android.security.keystore.KeyProperties#ENCRYPTION_PADDING_NONE](https://developer.android.com/reference/kotlin/android/security/keystore/KeyProperties#ENCRYPTION_PADDING_NONE:kotlin.String), [android.security.keystore.KeyProperties#ENCRYPTION_PADDING_PKCS7](https://developer.android.com/reference/kotlin/android/security/keystore/KeyProperties#ENCRYPTION_PADDING_PKCS7:kotlin.String), [android.security.keystore.KeyProperties#ENCRYPTION_PADDING_RSA_PKCS1](https://developer.android.com/reference/kotlin/android/security/keystore/KeyProperties#ENCRYPTION_PADDING_RSA_PKCS1:kotlin.String), or [android.security.keystore.KeyProperties#ENCRYPTION_PADDING_RSA_OAEP](https://developer.android.com/reference/kotlin/android/security/keystore/KeyProperties#ENCRYPTION_PADDING_RSA_OAEP:kotlin.String) |

### getKeySize

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getKeySize(): Int
```

Gets the size of the key in bits. 

### getKeyValidityForConsumptionEnd

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getKeyValidityForConsumptionEnd(): Date?
```

Gets the time instant after which the key is no long valid for decryption and verification.

| Return ||
|------------------------------------------------------------------------------|------------------------------------|
| [Date](https://developer.android.com/reference/kotlin/java/util/Date.html#)? | instant or`null`if not restricted. |

### getKeyValidityForOriginationEnd

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getKeyValidityForOriginationEnd(): Date?
```

Gets the time instant after which the key is no long valid for encryption and signing.

| Return ||
|------------------------------------------------------------------------------|------------------------------------|
| [Date](https://developer.android.com/reference/kotlin/java/util/Date.html#)? | instant or`null`if not restricted. |

### getKeyValidityStart

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getKeyValidityStart(): Date?
```

Gets the time instant before which the key is not yet valid.

| Return ||
|------------------------------------------------------------------------------|------------------------------------|
| [Date](https://developer.android.com/reference/kotlin/java/util/Date.html#)? | instant or`null`if not restricted. |

### getKeystoreAlias

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getKeystoreAlias(): String!
```

Gets the entry alias under which the key is stored in the`AndroidKeyStore`. 

### getOrigin

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getOrigin(): Int
```

Gets the origin of the key. See [KeyProperties](https://developer.android.com/reference/kotlin/android/security/keystore/KeyProperties).`ORIGIN`constants.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.security.keystore.KeyProperties#ORIGIN_GENERATED](https://developer.android.com/reference/kotlin/android/security/keystore/KeyProperties#ORIGIN_GENERATED:kotlin.Int), [android.security.keystore.KeyProperties#ORIGIN_IMPORTED](https://developer.android.com/reference/kotlin/android/security/keystore/KeyProperties#ORIGIN_IMPORTED:kotlin.Int), or [android.security.keystore.KeyProperties#ORIGIN_UNKNOWN](https://developer.android.com/reference/kotlin/android/security/keystore/KeyProperties#ORIGIN_UNKNOWN:kotlin.Int) |

### getPurposes

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPurposes(): Int
```

Gets the set of purposes (e.g., encrypt, decrypt, sign) for which the key can be used. Attempts to use the key for any other purpose will be rejected.

See [KeyProperties](https://developer.android.com/reference/kotlin/android/security/keystore/KeyProperties).`PURPOSE`flags.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is either`0`or a combination of [android.security.keystore.KeyProperties#PURPOSE_ENCRYPT](https://developer.android.com/reference/kotlin/android/security/keystore/KeyProperties#PURPOSE_ENCRYPT:kotlin.Int), [android.security.keystore.KeyProperties#PURPOSE_DECRYPT](https://developer.android.com/reference/kotlin/android/security/keystore/KeyProperties#PURPOSE_DECRYPT:kotlin.Int), [android.security.keystore.KeyProperties#PURPOSE_SIGN](https://developer.android.com/reference/kotlin/android/security/keystore/KeyProperties#PURPOSE_SIGN:kotlin.Int), [android.security.keystore.KeyProperties#PURPOSE_VERIFY](https://developer.android.com/reference/kotlin/android/security/keystore/KeyProperties#PURPOSE_VERIFY:kotlin.Int), [android.security.keystore.KeyProperties#PURPOSE_WRAP_KEY](https://developer.android.com/reference/kotlin/android/security/keystore/KeyProperties#PURPOSE_WRAP_KEY:kotlin.Int), [android.security.keystore.KeyProperties#PURPOSE_AGREE_KEY](https://developer.android.com/reference/kotlin/android/security/keystore/KeyProperties#PURPOSE_AGREE_KEY:kotlin.Int), and [android.security.keystore.KeyProperties#PURPOSE_ATTEST_KEY](https://developer.android.com/reference/kotlin/android/security/keystore/KeyProperties#PURPOSE_ATTEST_KEY:kotlin.Int) |

### getRemainingUsageCount

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getRemainingUsageCount(): Int
```

Returns the remaining number of times the key is allowed to be used or [KeyProperties.UNRESTRICTED_USAGE_COUNT](https://developer.android.com/reference/kotlin/android/security/keystore/KeyProperties#UNRESTRICTED_USAGE_COUNT:kotlin.Int) if there's no restriction on the number of times the key can be used. Note that this gives a best effort count and need not be accurate (as there might be usages happening in parallel and the count maintained here need not be in sync with the usage). 

### getSecurityLevel

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSecurityLevel(): Int
```

Returns the security level that the key is protected by.`KeyProperties.SecurityLevelEnum.TRUSTED_ENVIRONMENT`and`KeyProperties.SecurityLevelEnum.STRONGBOX`indicate that the key material resides in secure hardware. Key material of such keys is available in plaintext only inside the secure hardware and is not exposed outside of it.

See [KeyProperties](https://developer.android.com/reference/kotlin/android/security/keystore/KeyProperties).`SecurityLevelEnum`constants.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.security.keystore.KeyProperties#SECURITY_LEVEL_UNKNOWN](https://developer.android.com/reference/kotlin/android/security/keystore/KeyProperties#SECURITY_LEVEL_UNKNOWN:kotlin.Int), [android.security.keystore.KeyProperties#SECURITY_LEVEL_UNKNOWN_SECURE](https://developer.android.com/reference/kotlin/android/security/keystore/KeyProperties#SECURITY_LEVEL_UNKNOWN_SECURE:kotlin.Int), [android.security.keystore.KeyProperties#SECURITY_LEVEL_SOFTWARE](https://developer.android.com/reference/kotlin/android/security/keystore/KeyProperties#SECURITY_LEVEL_SOFTWARE:kotlin.Int), [android.security.keystore.KeyProperties#SECURITY_LEVEL_TRUSTED_ENVIRONMENT](https://developer.android.com/reference/kotlin/android/security/keystore/KeyProperties#SECURITY_LEVEL_TRUSTED_ENVIRONMENT:kotlin.Int), or [android.security.keystore.KeyProperties#SECURITY_LEVEL_STRONGBOX](https://developer.android.com/reference/kotlin/android/security/keystore/KeyProperties#SECURITY_LEVEL_STRONGBOX:kotlin.Int) |

### getSignaturePaddings

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSignaturePaddings(): Array<String!>
```

Gets the set of padding schemes (e.g.,`PSS`,`PKCS#1`) with which the key can be used when signing/verifying. Attempts to use the key with any other padding scheme will be rejected.

See [KeyProperties](https://developer.android.com/reference/kotlin/android/security/keystore/KeyProperties).`SIGNATURE_PADDING`constants.

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!> | This value cannot be`null`. Value is [android.security.keystore.KeyProperties#SIGNATURE_PADDING_RSA_PKCS1](https://developer.android.com/reference/kotlin/android/security/keystore/KeyProperties#SIGNATURE_PADDING_RSA_PKCS1:kotlin.String), or [android.security.keystore.KeyProperties#SIGNATURE_PADDING_RSA_PSS](https://developer.android.com/reference/kotlin/android/security/keystore/KeyProperties#SIGNATURE_PADDING_RSA_PSS:kotlin.String) |

### getUserAuthenticationType

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getUserAuthenticationType(): Int
```

Gets the acceptable user authentication types for which this key can be authorized to be used. This has effect only if user authentication is required (see [isUserAuthenticationRequired()](https://developer.android.com/reference/kotlin/android/security/keystore/KeyInfo#isUserAuthenticationRequired())).

This authorization applies only to secret key and private key operations. Public key operations are not restricted.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | integer representing the accepted forms of user authentication for this key Value is either`0`or a combination of [android.security.keystore.KeyProperties#AUTH_BIOMETRIC_STRONG](https://developer.android.com/reference/kotlin/android/security/keystore/KeyProperties#AUTH_BIOMETRIC_STRONG:kotlin.Int), and [android.security.keystore.KeyProperties#AUTH_DEVICE_CREDENTIAL](https://developer.android.com/reference/kotlin/android/security/keystore/KeyProperties#AUTH_DEVICE_CREDENTIAL:kotlin.Int) |

**See Also**

- <https://developer.android.com/reference/kotlin/android/security/keystore/KeyInfo#isUserAuthenticationRequired()> 

### getUserAuthenticationValidityDurationSeconds

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getUserAuthenticationValidityDurationSeconds(): Int
```

Gets the duration of time (seconds) for which this key is authorized to be used after the user is successfully authenticated. This has effect only if user authentication is required (see [isUserAuthenticationRequired()](https://developer.android.com/reference/kotlin/android/security/keystore/KeyInfo#isUserAuthenticationRequired())).

This authorization applies only to secret key and private key operations. Public key operations are not restricted.

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | duration in seconds or`-1`if authentication is required for every use of the key. |

**See Also**

- <https://developer.android.com/reference/kotlin/android/security/keystore/KeyInfo#isUserAuthenticationRequired()> 

### isInsideSecureHardware

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isInsideSecureHardware(): Boolean
```

**Deprecated:** *This method is superseded by @see getSecurityLevel.*

Returns`true`if the key resides inside secure hardware (e.g., Trusted Execution Environment (TEE) or Secure Element (SE)). Key material of such keys is available in plaintext only inside the secure hardware and is not exposed outside of it. 

### isInvalidatedByBiometricEnrollment

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isInvalidatedByBiometricEnrollment(): Boolean
```

Returns`true`if the key will be invalidated by enrollment of a new fingerprint or removal of all fingerprints. 

### isTrustedUserPresenceRequired

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isTrustedUserPresenceRequired(): Boolean
```

Returns`true`if the key can only be only be used if a test for user presence has succeeded since Signature.initSign() has been called. 

### isUnlockedDeviceRequired

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isUnlockedDeviceRequired(): Boolean
```

Returns`true`if the key is authorized to be used only while the device is unlocked.

This authorization applies only to secret key and private key operations. Public key operations are not restricted. 
**See Also**

- [android.security.keystore.KeyGenParameterSpec.Builder#setUnlockedDeviceRequired(boolean)](https://developer.android.com/reference/kotlin/android/security/keystore/KeyGenParameterSpec.Builder#setUnlockedDeviceRequired(kotlin.Boolean))
- [android.security.keystore.KeyProtection.Builder#setUnlockedDeviceRequired(boolean)](https://developer.android.com/reference/kotlin/android/security/keystore/KeyProtection.Builder#setUnlockedDeviceRequired(kotlin.Boolean)) 

### isUserAuthenticationRequired

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isUserAuthenticationRequired(): Boolean
```

Returns`true`if the key is authorized to be used only if the user has been authenticated.

This authorization applies only to secret key and private key operations. Public key operations are not restricted. 
**See Also**

- <https://developer.android.com/reference/kotlin/android/security/keystore/KeyInfo#getUserAuthenticationValidityDurationSeconds()>
- [android.security.keystore.KeyGenParameterSpec.Builder#setUserAuthenticationRequired(boolean)](https://developer.android.com/reference/kotlin/android/security/keystore/KeyGenParameterSpec.Builder#setUserAuthenticationRequired(kotlin.Boolean))
- [android.security.keystore.KeyProtection.Builder#setUserAuthenticationRequired(boolean)](https://developer.android.com/reference/kotlin/android/security/keystore/KeyProtection.Builder#setUserAuthenticationRequired(kotlin.Boolean)) 

### isUserAuthenticationRequirementEnforcedBySecureHardware

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isUserAuthenticationRequirementEnforcedBySecureHardware(): Boolean
```

Returns`true`if the requirement that this key can only be used if the user has been authenticated is enforced by secure hardware (e.g., Trusted Execution Environment (TEE) or Secure Element (SE)). 
**See Also**

- <https://developer.android.com/reference/kotlin/android/security/keystore/KeyInfo#isUserAuthenticationRequired()> 

### isUserAuthenticationValidWhileOnBody

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isUserAuthenticationValidWhileOnBody(): Boolean
```

Returns`true`if this key will become unusable when the device is removed from the user's body. This is possible only for keys with a specified validity duration, and only on devices with an on-body sensor. Always returns`false`on devices that lack an on-body sensor. 

### isUserConfirmationRequired

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isUserConfirmationRequired(): Boolean
```

Returns`true`if the key is authorized to be used only for messages confirmed by the user. Confirmation is separate from user authentication (see [isUserAuthenticationRequired()](https://developer.android.com/reference/kotlin/android/security/keystore/KeyInfo#isUserAuthenticationRequired())). Keys can be created that require confirmation but not user authentication, or user authentication but not confirmation, or both. Confirmation verifies that some user with physical possession of the device has approved a displayed message. User authentication verifies that the correct user is present and has authenticated.

This authorization applies only to secret key and private key operations. Public key operations are not restricted. 
**See Also**

- [android.security.keystore.KeyGenParameterSpec.Builder#setUserConfirmationRequired(boolean)](https://developer.android.com/reference/kotlin/android/security/keystore/KeyGenParameterSpec.Builder#setUserConfirmationRequired(kotlin.Boolean))
- [android.security.keystore.KeyProtection.Builder#setUserConfirmationRequired(boolean)](https://developer.android.com/reference/kotlin/android/security/keystore/KeyProtection.Builder#setUserConfirmationRequired(kotlin.Boolean))
