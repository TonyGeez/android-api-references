Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AuthenticationPolicyManager

```
class AuthenticationPolicyManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.security.authenticationpolicy.AuthenticationPolicyManager](../android/security/authenticationpolicy/AuthenticationPolicyManager.md) |

AuthenticationPolicyManager is a centralized interface for managing authentication related policies on the device. AuthenticationPolicyManager is designed to protect Android users by integrating with apps and key system components, such as the lock screen. It is not related to enterprise control surfaces and does not offer additional administrative controls.

### Secure Lock

Secure lockdown includes a set of device locking capabilities to protect users in "at risk" environments.

<br />

To use secure lock, call #enableSecureLockDevice to enable it on the device. This will require the caller to have the android.Manifest.permission#MANAGE_SECURE_LOCK_DEVICE permission.

To disable secure lock on the device, call #disableSecureLockDevice. This will require the caller to have the android.Manifest.permission#MANAGE_SECURE_LOCK_DEVICE permission.

To check if the device meets the requirements to enable secure lock, call #getSecureLockDeviceAvailability. This will require the caller to have the android.Manifest.permission#MANAGE_SECURE_LOCK_DEVICE permission.

To check if secure lock is already enabled on the device, call #isSecureLockDeviceEnabled. This will require the caller to have the android.Manifest.permission#MANAGE_SECURE_LOCK_DEVICE permission.

To listen for changes in the availability or enabled / disabled status of Secure Lock Device, register a android.security.authenticationpolicy.AuthenticationPolicyManager.SecureLockDeviceStatusListener using #registerSecureLockDeviceStatusListener(java.util.concurrent.Executor,android.security.authenticationpolicy.AuthenticationPolicyManager.SecureLockDeviceStatusListener). To unregister a previously registered listener, use #unregisterSecureLockDeviceStatusListener(android.security.authenticationpolicy.AuthenticationPolicyManager.SecureLockDeviceStatusListener).

### Cross Device Authentication Framework

AuthenticationPolicyManager exposes a set of methods that can be used by privileged components to gate access to select functionality.

This will require the caller to have the android.Manifest.permission#MANAGE_CROSS_DEVICE_AUTHENTICATED_MESSAGES permission.

Cross device access requests can be initiated on one device by calling `https://developer.android.com/reference/kotlin/android/security/authenticationpolicy/AuthenticationPolicyManager#createCrossDeviceAuthenticationRequest(java.util.UUID,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)`. The returned token should be transmitted to another device, via any means, and the receiving service should then use that token to call #parseCrossDeviceAuthenticationRequest(byte\[\],java.lang.String,java.util.concurrent.Executor,android.os.OutcomeReceiver) before executing the request. This ensures that a common set of security checks are verified before executing the request and it decouples many form factor specific checks from the service being guarded.

## Summary

| Constants ||
|---|---|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/security/authenticationpolicy/AuthenticationPolicyManager#PROPERTY_CROSS_DEVICE_TRUSTED_CERTIFICATES:kotlin.String` An optional property that applications can define in their manifest's `<application>` element on the **target device** (the receiver of the request) to specify trusted signing certificates for cross-device authentication requests. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/security/authenticationpolicy/AuthenticationPolicyManager#PROPERTY_CROSS_DEVICE_TRUSTED_PACKAGES:kotlin.String` An optional property that applications can define in their manifest's `<application>` element on the **originating device** (the sender of the request) to specify package name aliases. |

| Public methods ||
|---|---|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/security/authenticationpolicy/AuthenticationPolicyManager#createCrossDeviceAuthenticationRequest(java.util.UUID,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)(associationToken: https://developer.android.com/reference/kotlin/java/util/UUID.html#, callbackExecutor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, callback: https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html!, https://developer.android.com/reference/kotlin/android/security/authenticationpolicy/CrossDeviceAuthenticationException!>)` Creates a new cross-device authentication request associated with the given `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager.html#`'s obfuscated remote device ID. |

## Constants

### PROPERTY_CROSS_DEVICE_TRUSTED_CERTIFICATES

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PROPERTY_CROSS_DEVICE_TRUSTED_CERTIFICATES: String
```

An optional property that applications can define in their manifest's `<application>` element on the **target device** (the receiver of the request) to specify trusted signing certificates for cross-device authentication requests.

This property is only relevant for applications that use the cross-device authentication framework (`https://developer.android.com/reference/kotlin/android/security/authenticationpolicy/AuthenticationPolicyManager#createCrossDeviceAuthenticationRequest(java.util.UUID,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)`).

This property allows the target application to trust cross-device authentication requests originating from applications signed with different certificates. The value should be a comma-separated list of SHA-256 fingerprints of the trusted certificates and a maximum of 50 entries is supported.

 Value: "android.security.authenticationpolicy.CROSS_DEVICE_TRUSTED_CERTIFICATES"

### PROPERTY_CROSS_DEVICE_TRUSTED_PACKAGES

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PROPERTY_CROSS_DEVICE_TRUSTED_PACKAGES: String
```

An optional property that applications can define in their manifest's `<application>` element on the **originating device** (the sender of the request) to specify package name aliases.

This property is only relevant for applications that use the cross-device authentication framework (`https://developer.android.com/reference/kotlin/android/security/authenticationpolicy/AuthenticationPolicyManager#createCrossDeviceAuthenticationRequest(java.util.UUID,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)`). For example, an application should use this property when the application's package name on a wearable, or any other form factor, is different than the package name on the phone.

Using these aliases does not remove the need for the applications on each device to be signed with the same certificate unless `https://developer.android.com/reference/kotlin/android/security/authenticationpolicy/AuthenticationPolicyManager#PROPERTY_CROSS_DEVICE_TRUSTED_CERTIFICATES:kotlin.String` is also used.

 Value: "android.security.authenticationpolicy.CROSS_DEVICE_TRUSTED_PACKAGES"

## Public methods

### createCrossDeviceAuthenticationRequest

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun createCrossDeviceAuthenticationRequest(
    associationToken: UUID, 
    callbackExecutor: Executor, 
    callback: OutcomeReceiver<ByteArray!, CrossDeviceAuthenticationException!>
): Unit
```

Creates a new cross-device authentication request associated with the given `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager.html#`'s obfuscated remote device ID. Callers typically get this ID from a companion application which uses `https://developer.android.com/reference/kotlin/android/companion/AssociationInfo.html#getAssociationToken()` to retrieve it along with other device information that will be shared with applications.

Returns an opaque token to be passed to the remote device and used as a parameter in #parseCrossDeviceAuthenticationRequest(byte\[\],java.lang.String,java.util.concurrent.Executor,android.os.OutcomeReceiver) to unpack the data and run authorization checks. In most cases, applications will pass this token as a parameter to another service that will parse the token to verify the request before proceeding.

Use `https://developer.android.com/reference/kotlin/android/security/authenticationpolicy/AuthenticationPolicyManager#PROPERTY_CROSS_DEVICE_TRUSTED_PACKAGES:kotlin.String` if the application is known by another name on the remote device.

Use `https://developer.android.com/reference/kotlin/android/security/authenticationpolicy/AuthenticationPolicyManager#PROPERTY_CROSS_DEVICE_TRUSTED_CERTIFICATES:kotlin.String` if the application is signed with a different certificate on the remote device.

Using this API requires that the association has been granted a supported trust type via `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager.html#requestDeviceTrustPairing(kotlin.Int,%20android.companion.OutOfBandPairingRequest,%20kotlin.IntArray,%20java.util.concurrent.Executor,%20android.companion.CompanionDeviceManager.TrustPairingCallback)` to ensure the user is informed that cross-device actions are allowed. Untrusted associations will always fail with an error.

Using this API may also require meeting additional requirements, such as showing an active notification to the user while the cross-device operation is in progress. Refer to the documentation of the service that is guarded by this API for details.

| Parameters ||
|---|---|
| `associationToken` | [UUID](../java/util/UUID.md): the association token of the remote device where this request will be processed. This value cannot be `null`. |
| `callbackExecutor` | [Executor](../java/util/concurrent/Executor.md): the executor on which to invoke the callback. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use `https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()`. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `callback` | [OutcomeReceiver](../android/os/OutcomeReceiver.md)\< [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!, [CrossDeviceAuthenticationException](../android/security/authenticationpolicy/CrossDeviceAuthenticationException.md)!\>: the receiver for the encrypted request on success, or an exception on failure. This value cannot be `null`. |
| --- | --- |
