# KeyStoreException

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# KeyStoreException

Kotlin| [Java](https://developer.android.com/reference/android/security/KeyStoreException "View this page in Java") 
| --- | --- |

```
open class KeyStoreException : Exception
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) ||
| | | ↳ | [android.security.KeyStoreException](https://developer.android.com/reference/kotlin/android/security/KeyStoreException#) |
| --- | --- | --- | --- |

Exception containing information about the failure at the Keystore / KeyMint layer while generating or using a key. The public error codes indicate the cause of the error and the methods indicate whether it's a system/key issue and whether re-trying the operation (with the same key or a new key) is likely to succeed.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_ATTESTATION_CHALLENGE_TOO_LARGE](https://developer.android.com/reference/kotlin/android/security/KeyStoreException#ERROR_ATTESTATION_CHALLENGE_TOO_LARGE:kotlin.Int) The attestation challenge specified is too large. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_ATTESTATION_KEYS_UNAVAILABLE](https://developer.android.com/reference/kotlin/android/security/KeyStoreException#ERROR_ATTESTATION_KEYS_UNAVAILABLE:kotlin.Int) There are no keys available for attestation. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_ID_ATTESTATION_FAILURE](https://developer.android.com/reference/kotlin/android/security/KeyStoreException#ERROR_ID_ATTESTATION_FAILURE:kotlin.Int) The error related to inclusion of device identifiers in the attestation record. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_INCORRECT_USAGE](https://developer.android.com/reference/kotlin/android/security/KeyStoreException#ERROR_INCORRECT_USAGE:kotlin.Int) The feature the caller is trying to use is not compatible with the parameters used to generate the key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_INTERNAL_SYSTEM_ERROR](https://developer.android.com/reference/kotlin/android/security/KeyStoreException#ERROR_INTERNAL_SYSTEM_ERROR:kotlin.Int) An internal system error - refer to [isTransientFailure()](https://developer.android.com/reference/kotlin/android/security/KeyStoreException#isTransientFailure())to determine whether re-trying the operation is likely to yield different results. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_KEYMINT_FAILURE](https://developer.android.com/reference/kotlin/android/security/KeyStoreException#ERROR_KEYMINT_FAILURE:kotlin.Int) General error in the KeyMint layer. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_KEYSTORE_FAILURE](https://developer.android.com/reference/kotlin/android/security/KeyStoreException#ERROR_KEYSTORE_FAILURE:kotlin.Int) Failure in the Keystore layer. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_KEYSTORE_UNINITIALIZED](https://developer.android.com/reference/kotlin/android/security/KeyStoreException#ERROR_KEYSTORE_UNINITIALIZED:kotlin.Int) Indicating that`load()`has not been called on the Keystore instance, or an attempt has been made to generate an authorization bound key while the user has not set a lock screen knowledge factor (LSKF). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_KEY_CORRUPTED](https://developer.android.com/reference/kotlin/android/security/KeyStoreException#ERROR_KEY_CORRUPTED:kotlin.Int) The key is corrupted and could not be recovered. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_KEY_DOES_NOT_EXIST](https://developer.android.com/reference/kotlin/android/security/KeyStoreException#ERROR_KEY_DOES_NOT_EXIST:kotlin.Int) The key the operation refers to doesn't exist. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_KEY_NOT_TEMPORALLY_VALID](https://developer.android.com/reference/kotlin/android/security/KeyStoreException#ERROR_KEY_NOT_TEMPORALLY_VALID:kotlin.Int) The key is not currently valid: Either at has expired or it will be valid for use in the future. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_KEY_OPERATION_EXPIRED](https://developer.android.com/reference/kotlin/android/security/KeyStoreException#ERROR_KEY_OPERATION_EXPIRED:kotlin.Int) The crypto object the caller has been using held a reference to a KeyMint operation that has been evacuated (likely due to other concurrent operations taking place). |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_OTHER](https://developer.android.com/reference/kotlin/android/security/KeyStoreException#ERROR_OTHER:kotlin.Int) This error code is for mapping errors that the caller will not know about. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_PERMISSION_DENIED](https://developer.android.com/reference/kotlin/android/security/KeyStoreException#ERROR_PERMISSION_DENIED:kotlin.Int) The caller has requested key parameters or operation which are only available to system or privileged apps. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_UNIMPLEMENTED](https://developer.android.com/reference/kotlin/android/security/KeyStoreException#ERROR_UNIMPLEMENTED:kotlin.Int) The feature the caller is trying to use is not implemented by the underlying KeyMint implementation. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_USER_AUTHENTICATION_REQUIRED](https://developer.android.com/reference/kotlin/android/security/KeyStoreException#ERROR_USER_AUTHENTICATION_REQUIRED:kotlin.Int) Indicating the key could not be used because the user needs to authenticate first. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RETRY_AFTER_NEXT_REBOOT](https://developer.android.com/reference/kotlin/android/security/KeyStoreException#RETRY_AFTER_NEXT_REBOOT:kotlin.Int) Re-try the operation that led to this error when the device has a software update downloaded and on the next reboot. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RETRY_NEVER](https://developer.android.com/reference/kotlin/android/security/KeyStoreException#RETRY_NEVER:kotlin.Int) Never re-try the operation that led to this error, since it's a permanent error. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RETRY_WHEN_CONNECTIVITY_AVAILABLE](https://developer.android.com/reference/kotlin/android/security/KeyStoreException#RETRY_WHEN_CONNECTIVITY_AVAILABLE:kotlin.Int) Re-try the operation that led to this error when the device regains connectivity. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RETRY_WITH_EXPONENTIAL_BACKOFF](https://developer.android.com/reference/kotlin/android/security/KeyStoreException#RETRY_WITH_EXPONENTIAL_BACKOFF:kotlin.Int) Re-try the operation that led to this error with an exponential back-off delay. |

| Public methods ||
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getNumericErrorCode](https://developer.android.com/reference/kotlin/android/security/KeyStoreException#getNumericErrorCode())`()` Returns one of the error codes exported by the class. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getRetryPolicy](https://developer.android.com/reference/kotlin/android/security/KeyStoreException#getRetryPolicy())`()` Returns the re-try policy for transient failures. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSystemError](https://developer.android.com/reference/kotlin/android/security/KeyStoreException#isSystemError())`()` Indicates whether the error related to the Keystore/KeyMint implementation and not a specific key. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isTransientFailure](https://developer.android.com/reference/kotlin/android/security/KeyStoreException#isTransientFailure())`()` Returns true if the failure is a transient failure - that is, performing the same operation again at a late time is likely to succeed. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [requiresUserAuthentication](https://developer.android.com/reference/kotlin/android/security/KeyStoreException#requiresUserAuthentication())`()` Indicates whether the failure is due to the device being locked. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/security/KeyStoreException#toString())`()` <br /> |
| --- | --- |

## Constants

### ERROR_ATTESTATION_CHALLENGE_TOO_LARGE

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_ATTESTATION_CHALLENGE_TOO_LARGE: Int
```

The attestation challenge specified is too large. 

 Value: 9

### ERROR_ATTESTATION_KEYS_UNAVAILABLE

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_ATTESTATION_KEYS_UNAVAILABLE: Int
```

There are no keys available for attestation. This error is returned only on devices that rely solely on remotely-provisioned keys (see [Remote Key Provisioning](https://android-developers.googleblog.com/2022/03/upgrading-android-attestation-remote.html)).

On such a device, if the caller requests key generation and includes an attestation challenge (indicating key attestation is required), the error will be returned in one of the following cases:

- The pool of remotely-provisioned keys has been exhausted.
- The device is not registered with the key provisioning server.

<br />

This error is a transient one if the pool of remotely-provisioned keys has been exhausted. However, if the device is not registered with the server, or the key provisioning server refuses key issuance, this is a permanent error. 

 Value: 16

### ERROR_ID_ATTESTATION_FAILURE

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_ID_ATTESTATION_FAILURE: Int
```

The error related to inclusion of device identifiers in the attestation record. 

 Value: 8

### ERROR_INCORRECT_USAGE

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_INCORRECT_USAGE: Int
```

The feature the caller is trying to use is not compatible with the parameters used to generate the key. For example, trying to use a key generated for a different signature algorithm, or a digest not specified during key creation. Another case is the attempt to generate a symmetric AES key and requesting key attestation. 

 Value: 13

### ERROR_INTERNAL_SYSTEM_ERROR

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_INTERNAL_SYSTEM_ERROR: Int
```

An internal system error - refer to [isTransientFailure()](https://developer.android.com/reference/kotlin/android/security/KeyStoreException#isTransientFailure())to determine whether re-trying the operation is likely to yield different results. 

 Value: 4

### ERROR_KEYMINT_FAILURE

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_KEYMINT_FAILURE: Int
```

General error in the KeyMint layer. 

 Value: 10

### ERROR_KEYSTORE_FAILURE

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_KEYSTORE_FAILURE: Int
```

Failure in the Keystore layer. 

 Value: 11

### ERROR_KEYSTORE_UNINITIALIZED

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_KEYSTORE_UNINITIALIZED: Int
```

Indicating that`load()`has not been called on the Keystore instance, or an attempt has been made to generate an authorization bound key while the user has not set a lock screen knowledge factor (LSKF). Instruct the user to set an LSKF and retry. 

 Value: 3

### ERROR_KEY_CORRUPTED

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_KEY_CORRUPTED: Int
```

The key is corrupted and could not be recovered. 

 Value: 7

### ERROR_KEY_DOES_NOT_EXIST

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_KEY_DOES_NOT_EXIST: Int
```

The key the operation refers to doesn't exist. 

 Value: 6

### ERROR_KEY_NOT_TEMPORALLY_VALID

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_KEY_NOT_TEMPORALLY_VALID: Int
```

The key is not currently valid: Either at has expired or it will be valid for use in the future. 

 Value: 14

### ERROR_KEY_OPERATION_EXPIRED

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_KEY_OPERATION_EXPIRED: Int
```

The crypto object the caller has been using held a reference to a KeyMint operation that has been evacuated (likely due to other concurrent operations taking place). The caller should re-create the crypto object and try again. 

 Value: 15

### ERROR_OTHER

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_OTHER: Int
```

This error code is for mapping errors that the caller will not know about. If the caller is targeting an API level earlier than the one the error was introduced in, then the error will be mapped to this one. In API level 33 no errors map to this error. 

 Value: 1

### ERROR_PERMISSION_DENIED

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_PERMISSION_DENIED: Int
```

The caller has requested key parameters or operation which are only available to system or privileged apps. 

 Value: 5

### ERROR_UNIMPLEMENTED

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_UNIMPLEMENTED: Int
```

The feature the caller is trying to use is not implemented by the underlying KeyMint implementation. This could happen when an unsupported algorithm is requested, or when trying to import a key in a format other than raw or PKCS#8. 

 Value: 12

### ERROR_USER_AUTHENTICATION_REQUIRED

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_USER_AUTHENTICATION_REQUIRED: Int
```

Indicating the key could not be used because the user needs to authenticate first. See [android.security.keystore.KeyGenParameterSpec.Builder#setUserAuthenticationRequired(boolean)](https://developer.android.com/reference/kotlin/android/security/keystore/KeyGenParameterSpec.Builder#setUserAuthenticationRequired(kotlin.Boolean)). 

 Value: 2

### RETRY_AFTER_NEXT_REBOOT

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RETRY_AFTER_NEXT_REBOOT: Int
```

Re-try the operation that led to this error when the device has a software update downloaded and on the next reboot. The Remote provisioning server recognizes the device, but refuses issuance of attestation keys because it contains a software version that could potentially be vulnerable and needs an update. Re-trying after the device has upgraded and rebooted may alleviate the problem.

This value is returned when [isTransientFailure()](https://developer.android.com/reference/kotlin/android/security/KeyStoreException#isTransientFailure())is`true`. 

 Value: 4

### RETRY_NEVER

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RETRY_NEVER: Int
```

Never re-try the operation that led to this error, since it's a permanent error. This value is always returned when [isTransientFailure()](https://developer.android.com/reference/kotlin/android/security/KeyStoreException#isTransientFailure())is`false`. 

 Value: 1

### RETRY_WHEN_CONNECTIVITY_AVAILABLE

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RETRY_WHEN_CONNECTIVITY_AVAILABLE: Int
```

Re-try the operation that led to this error when the device regains connectivity. Remote provisioning of keys requires reaching the remote server, and the device is currently unable to due that due to lack of network connectivity. This value is returned when [isTransientFailure()](https://developer.android.com/reference/kotlin/android/security/KeyStoreException#isTransientFailure())is`true`. 

 Value: 3

### RETRY_WITH_EXPONENTIAL_BACKOFF

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RETRY_WITH_EXPONENTIAL_BACKOFF: Int
```

Re-try the operation that led to this error with an exponential back-off delay. The first delay should be between 5 to 30 seconds, and each subsequent re-try should double the delay time. This value is returned when [isTransientFailure()](https://developer.android.com/reference/kotlin/android/security/KeyStoreException#isTransientFailure())is`true`. 

 Value: 2

## Public methods

### getNumericErrorCode

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getNumericErrorCode(): Int
```

Returns one of the error codes exported by the class.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a public error code Value is either`0`or a combination of [android.security.KeyStoreException#ERROR_OTHER](https://developer.android.com/reference/kotlin/android/security/KeyStoreException#ERROR_OTHER:kotlin.Int), [android.security.KeyStoreException#ERROR_USER_AUTHENTICATION_REQUIRED](https://developer.android.com/reference/kotlin/android/security/KeyStoreException#ERROR_USER_AUTHENTICATION_REQUIRED:kotlin.Int), [android.security.KeyStoreException#ERROR_KEYSTORE_UNINITIALIZED](https://developer.android.com/reference/kotlin/android/security/KeyStoreException#ERROR_KEYSTORE_UNINITIALIZED:kotlin.Int), [android.security.KeyStoreException#ERROR_INTERNAL_SYSTEM_ERROR](https://developer.android.com/reference/kotlin/android/security/KeyStoreException#ERROR_INTERNAL_SYSTEM_ERROR:kotlin.Int), [android.security.KeyStoreException#ERROR_PERMISSION_DENIED](https://developer.android.com/reference/kotlin/android/security/KeyStoreException#ERROR_PERMISSION_DENIED:kotlin.Int), [android.security.KeyStoreException#ERROR_KEY_DOES_NOT_EXIST](https://developer.android.com/reference/kotlin/android/security/KeyStoreException#ERROR_KEY_DOES_NOT_EXIST:kotlin.Int), [android.security.KeyStoreException#ERROR_KEY_CORRUPTED](https://developer.android.com/reference/kotlin/android/security/KeyStoreException#ERROR_KEY_CORRUPTED:kotlin.Int), [android.security.KeyStoreException#ERROR_ID_ATTESTATION_FAILURE](https://developer.android.com/reference/kotlin/android/security/KeyStoreException#ERROR_ID_ATTESTATION_FAILURE:kotlin.Int), [android.security.KeyStoreException#ERROR_ATTESTATION_CHALLENGE_TOO_LARGE](https://developer.android.com/reference/kotlin/android/security/KeyStoreException#ERROR_ATTESTATION_CHALLENGE_TOO_LARGE:kotlin.Int), [android.security.KeyStoreException#ERROR_KEYMINT_FAILURE](https://developer.android.com/reference/kotlin/android/security/KeyStoreException#ERROR_KEYMINT_FAILURE:kotlin.Int), [android.security.KeyStoreException#ERROR_KEYSTORE_FAILURE](https://developer.android.com/reference/kotlin/android/security/KeyStoreException#ERROR_KEYSTORE_FAILURE:kotlin.Int), [android.security.KeyStoreException#ERROR_UNIMPLEMENTED](https://developer.android.com/reference/kotlin/android/security/KeyStoreException#ERROR_UNIMPLEMENTED:kotlin.Int), [android.security.KeyStoreException#ERROR_INCORRECT_USAGE](https://developer.android.com/reference/kotlin/android/security/KeyStoreException#ERROR_INCORRECT_USAGE:kotlin.Int), [android.security.KeyStoreException#ERROR_KEY_NOT_TEMPORALLY_VALID](https://developer.android.com/reference/kotlin/android/security/KeyStoreException#ERROR_KEY_NOT_TEMPORALLY_VALID:kotlin.Int), [android.security.KeyStoreException#ERROR_KEY_OPERATION_EXPIRED](https://developer.android.com/reference/kotlin/android/security/KeyStoreException#ERROR_KEY_OPERATION_EXPIRED:kotlin.Int), [android.security.KeyStoreException#ERROR_ATTESTATION_KEYS_UNAVAILABLE](https://developer.android.com/reference/kotlin/android/security/KeyStoreException#ERROR_ATTESTATION_KEYS_UNAVAILABLE:kotlin.Int), and android.security.KeyStoreException.ERROR_DEVICE_REQUIRES_UPGRADE_FOR_ATTESTATION |

### getRetryPolicy

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getRetryPolicy(): Int
```

Returns the re-try policy for transient failures. Valid only if [isTransientFailure()](https://developer.android.com/reference/kotlin/android/security/KeyStoreException#isTransientFailure())returns`True`.

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is either`0`or a combination of [android.security.KeyStoreException#RETRY_NEVER](https://developer.android.com/reference/kotlin/android/security/KeyStoreException#RETRY_NEVER:kotlin.Int), [android.security.KeyStoreException#RETRY_WITH_EXPONENTIAL_BACKOFF](https://developer.android.com/reference/kotlin/android/security/KeyStoreException#RETRY_WITH_EXPONENTIAL_BACKOFF:kotlin.Int), [android.security.KeyStoreException#RETRY_WHEN_CONNECTIVITY_AVAILABLE](https://developer.android.com/reference/kotlin/android/security/KeyStoreException#RETRY_WHEN_CONNECTIVITY_AVAILABLE:kotlin.Int), and [android.security.KeyStoreException#RETRY_AFTER_NEXT_REBOOT](https://developer.android.com/reference/kotlin/android/security/KeyStoreException#RETRY_AFTER_NEXT_REBOOT:kotlin.Int) |

### isSystemError

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isSystemError(): Boolean
```

Indicates whether the error related to the Keystore/KeyMint implementation and not a specific key.

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the error is related to the system, not the key in use. System errors indicate a feature isn't working, whereas key-related errors are likely to succeed with a new key. |

### isTransientFailure

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isTransientFailure(): Boolean
```

Returns true if the failure is a transient failure - that is, performing the same operation again at a late time is likely to succeed. If [isSystemError()](https://developer.android.com/reference/kotlin/android/security/KeyStoreException#isSystemError())returns true, the transient nature of the failure relates to the device, otherwise relates to the key (so a permanent failure with an existing key likely requires creating another key to repeat the operation with). 

### requiresUserAuthentication

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun requiresUserAuthentication(): Boolean
```

Indicates whether the failure is due to the device being locked.

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the key operation failed because the user has to authenticate (e.g. by unlocking the device). |

### toString

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|--------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of this throwable. |
