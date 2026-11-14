# KeyInfo

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# KeyInfo

Kotlin| [Java](KeyInfo.md) 
| --- | --- |

```
open class KeyInfo : KeySpec
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.security.keystore.KeyInfo](KeyInfo.md) |

Information about a key from the [Android Keystore system](https://developer.android.com/training/articles/keystore.html). This class describes whether the key material is available in plaintext outside of secure hardware, whether user authentication is required for using the key and whether this requirement is enforced by secure hardware, the key's origin, what uses the key is authorized for (e.g., only in`GCM`mode, or signing only), whether the key should be encrypted at rest, the key's and validity start and end dates.

Instances of this class are immutable.

<br />

### Example: Symmetric Key

The following example illustrates how to obtain a`KeyInfo`describing the provided Android Keystore [SecretKey](../javax.crypto/SecretKey.md). 

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

The following example illustrates how to obtain a`KeyInfo`describing the provided Android KeyStore [PrivateKey](../java.security/PrivateKey.md). 

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
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | [getBlockModes](KeyInfo.md))`()` Gets the set of block modes (e.g., |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | [getDigests](KeyInfo.md))`()` Gets the set of digest algorithms (e.g., |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | [getEncryptionPaddings](KeyInfo.md))`()` Gets the set of padding schemes (e.g., |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getKeySize](KeyInfo.md))`()` Gets the size of the key in bits. |
| open [Date](../java.util/Date.md)? | [getKeyValidityForConsumptionEnd](KeyInfo.md))`()` Gets the time instant after which the key is no long valid for decryption and verification. |
| open [Date](../java.util/Date.md)? | [getKeyValidityForOriginationEnd](KeyInfo.md))`()` Gets the time instant after which the key is no long valid for encryption and signing. |
| --- | --- |
| open [Date](../java.util/Date.md)? | [getKeyValidityStart](KeyInfo.md))`()` Gets the time instant before which the key is not yet valid. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getKeystoreAlias](KeyInfo.md))`()` Gets the entry alias under which the key is stored in the`AndroidKeyStore`. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getOrigin](KeyInfo.md))`()` Gets the origin of the key. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPurposes](KeyInfo.md))`()` Gets the set of purposes (e.g., encrypt, decrypt, sign) for which the key can be used. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getRemainingUsageCount](KeyInfo.md))`()` Returns the remaining number of times the key is allowed to be used or [KeyProperties.UNRESTRICTED_USAGE_COUNT](KeyProperties.md) if there's no restriction on the number of times the key can be used. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSecurityLevel](KeyInfo.md))`()` Returns the security level that the key is protected by. |
| --- | --- |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | [getSignaturePaddings](KeyInfo.md))`()` Gets the set of padding schemes (e.g., |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getUserAuthenticationType](KeyInfo.md))`()` Gets the acceptable user authentication types for which this key can be authorized to be used. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getUserAuthenticationValidityDurationSeconds](KeyInfo.md))`()` Gets the duration of time (seconds) for which this key is authorized to be used after the user is successfully authenticated. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isInsideSecureHardware](KeyInfo.md))`()` Returns`true`if the key resides inside secure hardware (e.g., Trusted Execution Environment (TEE) or Secure Element (SE)). |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isInvalidatedByBiometricEnrollment](KeyInfo.md))`()` Returns`true`if the key will be invalidated by enrollment of a new fingerprint or removal of all fingerprints. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isTrustedUserPresenceRequired](KeyInfo.md))`()` Returns`true`if the key can only be only be used if a test for user presence has succeeded since Signature. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isUnlockedDeviceRequired](KeyInfo.md))`()` Returns`true`if the key is authorized to be used only while the device is unlocked. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isUserAuthenticationRequired](KeyInfo.md))`()` Returns`true`if the key is authorized to be used only if the user has been authenticated. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isUserAuthenticationRequirementEnforcedBySecureHardware](KeyInfo.md))`()` Returns`true`if the requirement that this key can only be used if the user has been authenticated is enforced by secure hardware (e.g., Trusted Execution Environment (TEE) or Secure Element (SE)). |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isUserAuthenticationValidWhileOnBody](KeyInfo.md))`()` Returns`true`if this key will become unusable when the device is removed from the user's body. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isUserConfirmationRequired](KeyInfo.md))`()` Returns`true`if the key is authorized to be used only for messages confirmed by the user. |

## Public methods

### getBlockModes

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getBlockModes(): Array<String!>
```

Gets the set of block modes (e.g.,`GCM`,`CBC`) with which the key can be used when encrypting/decrypting. Attempts to use the key with any other block modes will be rejected.

See [KeyProperties](KeyProperties.md).`BLOCK_MODE`constants.

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!> | This value cannot be`null`. Value is [android.security.keystore.KeyProperties#BLOCK_MODE_ECB](KeyProperties.md), [android.security.keystore.KeyProperties#BLOCK_MODE_CBC](KeyProperties.md), [android.security.keystore.KeyProperties#BLOCK_MODE_CTR](KeyProperties.md), or [android.security.keystore.KeyProperties#BLOCK_MODE_GCM](KeyProperties.md) |

### getDigests

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDigests(): Array<String!>
```

Gets the set of digest algorithms (e.g.,`SHA-256`,`SHA-384`) with which the key can be used.

See [KeyProperties](KeyProperties.md).`DIGEST`constants.

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!> | This value cannot be`null`. Value is [android.security.keystore.KeyProperties#DIGEST_NONE](KeyProperties.md), [android.security.keystore.KeyProperties#DIGEST_MD5](KeyProperties.md), [android.security.keystore.KeyProperties#DIGEST_SHA1](KeyProperties.md), [android.security.keystore.KeyProperties#DIGEST_SHA224](KeyProperties.md), [android.security.keystore.KeyProperties#DIGEST_SHA256](KeyProperties.md), [android.security.keystore.KeyProperties#DIGEST_SHA384](KeyProperties.md), or [android.security.keystore.KeyProperties#DIGEST_SHA512](KeyProperties.md) |

### getEncryptionPaddings

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getEncryptionPaddings(): Array<String!>
```

Gets the set of padding schemes (e.g.,`PKCS7Padding`,`PKCS1Padding`,`NoPadding`) with which the key can be used when encrypting/decrypting. Attempts to use the key with any other padding scheme will be rejected.

See [KeyProperties](KeyProperties.md).`ENCRYPTION_PADDING`constants.

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!> | This value cannot be`null`. Value is [android.security.keystore.KeyProperties#ENCRYPTION_PADDING_NONE](KeyProperties.md), [android.security.keystore.KeyProperties#ENCRYPTION_PADDING_PKCS7](KeyProperties.md), [android.security.keystore.KeyProperties#ENCRYPTION_PADDING_RSA_PKCS1](KeyProperties.md), or [android.security.keystore.KeyProperties#ENCRYPTION_PADDING_RSA_OAEP](KeyProperties.md) |

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
| [Date](../java.util/Date.md)? | instant or`null`if not restricted. |

### getKeyValidityForOriginationEnd

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getKeyValidityForOriginationEnd(): Date?
```

Gets the time instant after which the key is no long valid for encryption and signing.

| Return ||
|------------------------------------------------------------------------------|------------------------------------|
| [Date](../java.util/Date.md)? | instant or`null`if not restricted. |

### getKeyValidityStart

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getKeyValidityStart(): Date?
```

Gets the time instant before which the key is not yet valid.

| Return ||
|------------------------------------------------------------------------------|------------------------------------|
| [Date](../java.util/Date.md)? | instant or`null`if not restricted. |

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

Gets the origin of the key. See [KeyProperties](KeyProperties.md).`ORIGIN`constants.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.security.keystore.KeyProperties#ORIGIN_GENERATED](KeyProperties.md), [android.security.keystore.KeyProperties#ORIGIN_IMPORTED](KeyProperties.md), or [android.security.keystore.KeyProperties#ORIGIN_UNKNOWN](KeyProperties.md) |

### getPurposes

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPurposes(): Int
```

Gets the set of purposes (e.g., encrypt, decrypt, sign) for which the key can be used. Attempts to use the key for any other purpose will be rejected.

See [KeyProperties](KeyProperties.md).`PURPOSE`flags.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is either`0`or a combination of [android.security.keystore.KeyProperties#PURPOSE_ENCRYPT](KeyProperties.md), [android.security.keystore.KeyProperties#PURPOSE_DECRYPT](KeyProperties.md), [android.security.keystore.KeyProperties#PURPOSE_SIGN](KeyProperties.md), [android.security.keystore.KeyProperties#PURPOSE_VERIFY](KeyProperties.md), [android.security.keystore.KeyProperties#PURPOSE_WRAP_KEY](KeyProperties.md), [android.security.keystore.KeyProperties#PURPOSE_AGREE_KEY](KeyProperties.md), and [android.security.keystore.KeyProperties#PURPOSE_ATTEST_KEY](KeyProperties.md) |

### getRemainingUsageCount

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getRemainingUsageCount(): Int
```

Returns the remaining number of times the key is allowed to be used or [KeyProperties.UNRESTRICTED_USAGE_COUNT](KeyProperties.md) if there's no restriction on the number of times the key can be used. Note that this gives a best effort count and need not be accurate (as there might be usages happening in parallel and the count maintained here need not be in sync with the usage). 

### getSecurityLevel

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSecurityLevel(): Int
```

Returns the security level that the key is protected by.`KeyProperties.SecurityLevelEnum.TRUSTED_ENVIRONMENT`and`KeyProperties.SecurityLevelEnum.STRONGBOX`indicate that the key material resides in secure hardware. Key material of such keys is available in plaintext only inside the secure hardware and is not exposed outside of it.

See [KeyProperties](KeyProperties.md).`SecurityLevelEnum`constants.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.security.keystore.KeyProperties#SECURITY_LEVEL_UNKNOWN](KeyProperties.md), [android.security.keystore.KeyProperties#SECURITY_LEVEL_UNKNOWN_SECURE](KeyProperties.md), [android.security.keystore.KeyProperties#SECURITY_LEVEL_SOFTWARE](KeyProperties.md), [android.security.keystore.KeyProperties#SECURITY_LEVEL_TRUSTED_ENVIRONMENT](KeyProperties.md), or [android.security.keystore.KeyProperties#SECURITY_LEVEL_STRONGBOX](KeyProperties.md) |

### getSignaturePaddings

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSignaturePaddings(): Array<String!>
```

Gets the set of padding schemes (e.g.,`PSS`,`PKCS#1`) with which the key can be used when signing/verifying. Attempts to use the key with any other padding scheme will be rejected.

See [KeyProperties](KeyProperties.md).`SIGNATURE_PADDING`constants.

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!> | This value cannot be`null`. Value is [android.security.keystore.KeyProperties#SIGNATURE_PADDING_RSA_PKCS1](KeyProperties.md), or [android.security.keystore.KeyProperties#SIGNATURE_PADDING_RSA_PSS](KeyProperties.md) |

### getUserAuthenticationType

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getUserAuthenticationType(): Int
```

Gets the acceptable user authentication types for which this key can be authorized to be used. This has effect only if user authentication is required (see [isUserAuthenticationRequired()](KeyInfo.md))).

This authorization applies only to secret key and private key operations. Public key operations are not restricted.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | integer representing the accepted forms of user authentication for this key Value is either`0`or a combination of [android.security.keystore.KeyProperties#AUTH_BIOMETRIC_STRONG](KeyProperties.md), and [android.security.keystore.KeyProperties#AUTH_DEVICE_CREDENTIAL](KeyProperties.md) |

**See Also**

- <https://developer.android.com/reference/kotlin/android/security/keystore/KeyInfo#isUserAuthenticationRequired()> 

### getUserAuthenticationValidityDurationSeconds

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getUserAuthenticationValidityDurationSeconds(): Int
```

Gets the duration of time (seconds) for which this key is authorized to be used after the user is successfully authenticated. This has effect only if user authentication is required (see [isUserAuthenticationRequired()](KeyInfo.md))).

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

- [android.security.keystore.KeyGenParameterSpec.Builder#setUnlockedDeviceRequired(boolean)](../android/security/keystore/KeyGenParameterSpec.Builder.md))
- [android.security.keystore.KeyProtection.Builder#setUnlockedDeviceRequired(boolean)](../android/security/keystore/KeyProtection.Builder.md)) 

### isUserAuthenticationRequired

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isUserAuthenticationRequired(): Boolean
```

Returns`true`if the key is authorized to be used only if the user has been authenticated.

This authorization applies only to secret key and private key operations. Public key operations are not restricted. 
**See Also**

- <https://developer.android.com/reference/kotlin/android/security/keystore/KeyInfo#getUserAuthenticationValidityDurationSeconds()>
- [android.security.keystore.KeyGenParameterSpec.Builder#setUserAuthenticationRequired(boolean)](../android/security/keystore/KeyGenParameterSpec.Builder.md))
- [android.security.keystore.KeyProtection.Builder#setUserAuthenticationRequired(boolean)](../android/security/keystore/KeyProtection.Builder.md)) 

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

Returns`true`if the key is authorized to be used only for messages confirmed by the user. Confirmation is separate from user authentication (see [isUserAuthenticationRequired()](KeyInfo.md))). Keys can be created that require confirmation but not user authentication, or user authentication but not confirmation, or both. Confirmation verifies that some user with physical possession of the device has approved a displayed message. User authentication verifies that the correct user is present and has authenticated.

This authorization applies only to secret key and private key operations. Public key operations are not restricted. 
**See Also**

- [android.security.keystore.KeyGenParameterSpec.Builder#setUserConfirmationRequired(boolean)](../android/security/keystore/KeyGenParameterSpec.Builder.md))
- [android.security.keystore.KeyProtection.Builder#setUserConfirmationRequired(boolean)](../android/security/keystore/KeyProtection.Builder.md))
