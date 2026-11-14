Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CompanionDeviceManager

```
class CompanionDeviceManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.companion.CompanionDeviceManager](https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager#) |

Public interfaces for managing companion devices.

The interfaces in this class allow companion apps to `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager#associate(android.companion.AssociationRequest,%20java.util.concurrent.Executor,%20android.companion.CompanionDeviceManager.Callback)` discover and request device profiles} for companion devices, `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager#startObservingDevicePresence(kotlin.String)`, `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager#startSystemDataTransfer(kotlin.Int,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)` via `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager#attachSystemDataTransport(kotlin.Int,%20java.io.InputStream,%20java.io.OutputStream)` and more.

> [!NOTE]
>
> ### Developer Guides
>
> For more information about managing companion devices, read the [Companion Device Pairing](https://developer.android.com/guide/topics/connectivity/companion-device-pairing) developer guide.

. 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_COMPANION_DEVICE_SETUP:kotlin.String` feature which can be detected using `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#hasSystemFeature(kotlin.String)`.

## Summary

| Nested classes ||
|---|---|
| abstract | `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager.Callback` Callback for applications to receive updates about and the outcome of `https://developer.android.com/reference/kotlin/android/companion/AssociationRequest` issued via `associate()` call. |
| abstract | `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager.TrustPairingCallback` Callback for applications to receive updates about and the outcome of `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager#requestDeviceTrustPairing(kotlin.Int,%20android.companion.OutOfBandPairingRequest,%20kotlin.IntArray,%20java.util.concurrent.Executor,%20android.companion.CompanionDeviceManager.TrustPairingCallback)` |

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager#ERROR_TRUST_OUT_OF_BAND_PAIRING_FAILED:kotlin.Int` The out of band pairing failed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager#ERROR_TRUST_PAIRING_ASSOCIATION_DOES_NOT_EXIST:kotlin.Int` The association does not exist. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager#ERROR_TRUST_PAIRING_CANCELED:kotlin.Int` The trust pairing dialog was cancelled by the user or implicitly. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager#ERROR_TRUST_PAIRING_FAILED_TO_CREATE_PAIRING_DIALOG:kotlin.Int` Failed to create or send pairing dialog for trust pairing. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager#ERROR_TRUST_PAIRING_PIN_CODE_NOT_MATCHING:kotlin.Int` The PIN code confirmed by the user did not match. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager#ERROR_TRUST_PAIRING_TRANSPORT_NOT_ATTACHED:kotlin.Int` The transport was not attached for trust pairing. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager#ERROR_TRUST_RESUMPTION_FAILED:kotlin.Int` The trust resumption failed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager#ERROR_TRUST_UNKNOWN:kotlin.Int` Unknown error for trust pairing. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager#EXTRA_ASSOCIATION:kotlin.String` Extra field name for the `https://developer.android.com/reference/kotlin/android/companion/AssociationInfo` object, included into `https://developer.android.com/reference/kotlin/android/content/Intent.html#` which application receive in `https://developer.android.com/reference/kotlin/android/app/Activity.html#onActivityResult(kotlin.Int,%20kotlin.Int,%20android.content.Intent)` after the application's `https://developer.android.com/reference/kotlin/android/companion/AssociationRequest` was successfully processed and an association was created. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager#EXTRA_DEVICE:kotlin.String` A device, returned in the activity result of the `https://developer.android.com/reference/kotlin/android/content/IntentSender.html#` received in `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager.Callback#onDeviceFound(android.content.IntentSender)` Type is: - for classic Bluetooth - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice.html#` - for Bluetooth LE - `https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanResult.html#` - for WiFi - `https://developer.android.com/reference/kotlin/android/net/wifi/ScanResult.html#` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager#FLAG_AIRPLANE_MODE:kotlin.Int` Used by `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager#enableSystemDataSyncForTypes(kotlin.Int,%20kotlin.Int)`}. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager#FLAG_CALL_METADATA:kotlin.Int` Used by `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager#enableSystemDataSyncForTypes(kotlin.Int,%20kotlin.Int)`}. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager#FLAG_TASK_CONTINUITY:kotlin.Int` Used by `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager#enableSystemDataSyncForTypes(kotlin.Int,%20kotlin.Int)`}. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager#FLAG_UNIVERSAL_MODES:kotlin.Int` Used by `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager#enableSystemDataSyncForTypes(kotlin.Int,%20kotlin.Int)`}. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager#RESULT_CANCELED:kotlin.Int` The result code to propagate back to the user activity, indicates if the association dialog is implicitly cancelled. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager#RESULT_DISCOVERY_TIMEOUT:kotlin.Int` The result code to propagate back to the user activity, indicates the association dialog is dismissed if there's no device found after 20 seconds. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager#RESULT_INTERNAL_ERROR:kotlin.Int` The result code to propagate back to the user activity, indicates the internal error in CompanionDeviceManager. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager#RESULT_OK:kotlin.Int` The result code to propagate back to the user activity, indicates the association is created successfully. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager#RESULT_SECURITY_ERROR:kotlin.Int` The result code to propagate back to the user activity and `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager.Callback#onFailure(kotlin.Int,%20kotlin.CharSequence)`, indicates app is not allow to create the association due to the security issue. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager#RESULT_USER_REJECTED:kotlin.Int` The result code to propagate back to the user activity, indicates the association dialog is explicitly declined by the users. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager#TRUST_TYPE_CROSS_DEVICE_AUTHENTICATION:kotlin.Int` Trust type for platform-level cross-device authentication. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager#TRUST_TYPE_PROACTIVE_ASSISTANCE:kotlin.Int` Trust type for proactive assistance. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager#TRUST_TYPE_SCREEN_AUTOMATION:kotlin.Int` Trust type for screen automation. |

| Public methods ||
|---|---|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager#associate(android.companion.AssociationRequest,%20android.companion.CompanionDeviceManager.Callback,%20android.os.Handler)(request: https://developer.android.com/reference/kotlin/android/companion/AssociationRequest, callback: https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager.Callback, handler: https://developer.android.com/reference/kotlin/android/os/Handler.html#?)` Request to associate this app with a companion device. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager#associate(android.companion.AssociationRequest,%20java.util.concurrent.Executor,%20android.companion.CompanionDeviceManager.Callback)(request: https://developer.android.com/reference/kotlin/android/companion/AssociationRequest, executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, callback: https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager.Callback)` Request to associate this app with a companion device. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager#attachSystemDataTransport(kotlin.Int,%20java.io.InputStream,%20java.io.OutputStream)(associationId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, in: https://developer.android.com/reference/kotlin/java/io/InputStream.html#, out: https://developer.android.com/reference/kotlin/java/io/OutputStream.html#)` Attach a bidirectional communication stream to be used as a transport channel for transporting system data between associated devices. |
| --- | --- |
| [IntentSender](https://developer.android.com/reference/kotlin/android/content/IntentSender.html#)? | `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager#buildAssociationCancellationIntent()()` Cancel the current association activity. |
| [IntentSender](https://developer.android.com/reference/kotlin/android/content/IntentSender.html#)? | `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager#buildPermissionTransferUserConsentIntent(kotlin.Int)(associationId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Build a permission sync user consent dialog. |
| [DeviceId](https://developer.android.com/reference/kotlin/android/companion/DeviceId)? | `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager#createAndSetDeviceId(kotlin.Int,%20android.companion.DeviceId)(associationId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, deviceId: https://developer.android.com/reference/kotlin/android/companion/DeviceId?)` Returns a new `https://developer.android.com/reference/kotlin/android/companion/DeviceId` which can be passed to device manufacturers' apps, allowing them to fetch `https://developer.android.com/reference/kotlin/android/companion/AssociationInfo` or observe device presence for this associated device. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager#detachSystemDataTransport(kotlin.Int)(associationId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Detach the transport channel that's previously attached for the associated device. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager#disableSystemDataSyncForTypes(kotlin.Int,%20kotlin.Int)(associationId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Disable system data sync for an associated device. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager#disassociate(kotlin.Int)(associationId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Remove an association. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager#disassociate(kotlin.String)(deviceMacAddress: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Remove the association between this app and the device with the given mac address. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager#enableSystemDataSyncForTypes(kotlin.Int,%20kotlin.Int)(associationId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Enable system data sync for an associated device. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager#getAssociations()()` Calling this API requires a uses-feature `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_COMPANION_DEVICE_SETUP:kotlin.String` declaration in the manifest |
| --- | --- |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [AssociationInfo](https://developer.android.com/reference/kotlin/android/companion/AssociationInfo)!\> | `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager#getMyAssociations()()` Calling this API requires a uses-feature `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_COMPANION_DEVICE_SETUP:kotlin.String` declaration in the manifest |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager#hasNotificationAccess(android.content.ComponentName)(component: https://developer.android.com/reference/kotlin/android/content/ComponentName.html#!)` Check whether the given component can access the notifications via a `https://developer.android.com/reference/kotlin/android/service/notification/NotificationListenerService.html#` Your app must have an association with a device before calling this API |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager#isPermissionTransferUserConsented(kotlin.Int)(associationId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Return the current state of consent for permission transfer for the association. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager#isSystemDataTransportAttached(kotlin.Int)(associationId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Checks if a transport is currently attached for a given association id. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager#notifyActionResult(kotlin.Int,%20android.companion.ActionResult)(associationId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, result: https://developer.android.com/reference/kotlin/android/companion/ActionResult)` Allows a companion app to report the result of an action that was requested by the system. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager#removeBond(kotlin.Int)(associationId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Remove bonding between this device and an associated companion device. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager#requestDeviceTrustPairing(kotlin.Int,%20android.companion.OutOfBandPairingRequest,%20kotlin.IntArray,%20java.util.concurrent.Executor,%20android.companion.CompanionDeviceManager.TrustPairingCallback)(associationId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, requestOobPairing: https://developer.android.com/reference/kotlin/android/companion/OutOfBandPairingRequest?, trustTypes: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html, executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, callback: https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager.TrustPairingCallback)` Request the system to initiate a trusted pairing process for the given association. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager#requestNotificationAccess(android.content.ComponentName)(component: https://developer.android.com/reference/kotlin/android/content/ComponentName.html#!)` Request notification access for the given component. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager#setDeviceId(kotlin.Int,%20android.companion.DeviceId)(associationId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, deviceId: https://developer.android.com/reference/kotlin/android/companion/DeviceId?)` Sets the `https://developer.android.com/reference/kotlin/android/companion/DeviceId` for this association. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager#startObservingDevicePresence(android.companion.ObservingDevicePresenceRequest)(request: https://developer.android.com/reference/kotlin/android/companion/ObservingDevicePresenceRequest)` Register to receive callbacks whenever the associated device's presence changes. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager#startObservingDevicePresence(kotlin.String)(deviceAddress: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Register to receive callbacks whenever the associated device comes in and out of range. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager#startSystemDataTransfer(kotlin.Int,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)(associationId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, result: https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#<https://developer.android.com/reference/kotlin/java/lang/Void.html#!, https://developer.android.com/reference/kotlin/android/companion/CompanionException!>)` Start system data transfer which has been previously approved by the user. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager#stopObservingDevicePresence(android.companion.ObservingDevicePresenceRequest)(request: https://developer.android.com/reference/kotlin/android/companion/ObservingDevicePresenceRequest)` Unregister for receiving callbacks whenever the associated device comes in and out of range. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager#stopObservingDevicePresence(kotlin.String)(deviceAddress: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Unregister for receiving callbacks whenever the associated device comes in and out of range. |

## Constants

### ERROR_TRUST_OUT_OF_BAND_PAIRING_FAILED

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ERROR_TRUST_OUT_OF_BAND_PAIRING_FAILED: Int
```

The out of band pairing failed.

 Value: 7

### ERROR_TRUST_PAIRING_ASSOCIATION_DOES_NOT_EXIST

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ERROR_TRUST_PAIRING_ASSOCIATION_DOES_NOT_EXIST: Int
```

The association does not exist.

 Value: 5

### ERROR_TRUST_PAIRING_CANCELED

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ERROR_TRUST_PAIRING_CANCELED: Int
```

The trust pairing dialog was cancelled by the user or implicitly.

 Value: 2

### ERROR_TRUST_PAIRING_FAILED_TO_CREATE_PAIRING_DIALOG

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ERROR_TRUST_PAIRING_FAILED_TO_CREATE_PAIRING_DIALOG: Int
```

Failed to create or send pairing dialog for trust pairing.

 Value: 3

### ERROR_TRUST_PAIRING_PIN_CODE_NOT_MATCHING

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ERROR_TRUST_PAIRING_PIN_CODE_NOT_MATCHING: Int
```

The PIN code confirmed by the user did not match.

 Value: 4

### ERROR_TRUST_PAIRING_TRANSPORT_NOT_ATTACHED

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ERROR_TRUST_PAIRING_TRANSPORT_NOT_ATTACHED: Int
```

The transport was not attached for trust pairing.

 Value: 1

### ERROR_TRUST_RESUMPTION_FAILED

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ERROR_TRUST_RESUMPTION_FAILED: Int
```

The trust resumption failed.

This error is returned when the system fails to resume a previous trust relationship. You can try to re-attach the transport to resume the trust relationship.

If re-attaching fails, you can try to re-pair the devices.

 Value: 6

### ERROR_TRUST_UNKNOWN

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ERROR_TRUST_UNKNOWN: Int
```

Unknown error for trust pairing.

 Value: 0

### EXTRA_ASSOCIATION

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_ASSOCIATION: String
```

Extra field name for the `https://developer.android.com/reference/kotlin/android/companion/AssociationInfo` object, included into `https://developer.android.com/reference/kotlin/android/content/Intent.html#` which application receive in `https://developer.android.com/reference/kotlin/android/app/Activity.html#onActivityResult(kotlin.Int,%20kotlin.Int,%20android.content.Intent)` after the application's `https://developer.android.com/reference/kotlin/android/companion/AssociationRequest` was successfully processed and an association was created.

 Value: "android.companion.extra.ASSOCIATION"

### EXTRA_DEVICE

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_DEVICE: String
```

**Deprecated:** *use `https://developer.android.com/reference/kotlin/android/companion/AssociationInfo#getAssociatedDevice()` instead.*

A device, returned in the activity result of the `https://developer.android.com/reference/kotlin/android/content/IntentSender.html#` received in `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager.Callback#onDeviceFound(android.content.IntentSender)` Type is:

- for classic Bluetooth - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice.html#`
- for Bluetooth LE - `https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanResult.html#`
- for WiFi - `https://developer.android.com/reference/kotlin/android/net/wifi/ScanResult.html#`

<br />

 Value: "android.companion.extra.DEVICE"

### FLAG_AIRPLANE_MODE

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_AIRPLANE_MODE: Int
```

Used by `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager#enableSystemDataSyncForTypes(kotlin.Int,%20kotlin.Int)`}. Synchronize airplane mode state across devices. Disabled by default.

 Value: 16

### FLAG_CALL_METADATA

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_CALL_METADATA: Int
```

Used by `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager#enableSystemDataSyncForTypes(kotlin.Int,%20kotlin.Int)`}. Sync call metadata like muting, ending and silencing a call. Enabled by default.

 Value: 1

### FLAG_TASK_CONTINUITY

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_TASK_CONTINUITY: Int
```

Used by `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager#enableSystemDataSyncForTypes(kotlin.Int,%20kotlin.Int)`}. Synchronize task continuity data like open tasks, and enable this transport for Handoff. Disabled by default.

 Value: 2

### FLAG_UNIVERSAL_MODES

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_UNIVERSAL_MODES: Int
```

Used by `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager#enableSystemDataSyncForTypes(kotlin.Int,%20kotlin.Int)`}. Synchronize user settings like contextual modes across devices. Disabled by default.

 Value: 4

### RESULT_CANCELED

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESULT_CANCELED: Int
```

The result code to propagate back to the user activity, indicates if the association dialog is implicitly cancelled. E.g. phone is locked, switch to another app or press outside the dialog.

 Value: 0

### RESULT_DISCOVERY_TIMEOUT

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESULT_DISCOVERY_TIMEOUT: Int
```

The result code to propagate back to the user activity, indicates the association dialog is dismissed if there's no device found after 20 seconds.

 Value: 2

### RESULT_INTERNAL_ERROR

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESULT_INTERNAL_ERROR: Int
```

The result code to propagate back to the user activity, indicates the internal error in CompanionDeviceManager.

 Value: 3

### RESULT_OK

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESULT_OK: Int
```

The result code to propagate back to the user activity, indicates the association is created successfully.

 Value: -1

### RESULT_SECURITY_ERROR

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESULT_SECURITY_ERROR: Int
```

The result code to propagate back to the user activity and `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager.Callback#onFailure(kotlin.Int,%20kotlin.CharSequence)`, indicates app is not allow to create the association due to the security issue. E.g. There are missing necessary permissions when creating association.

 Value: 4

### RESULT_USER_REJECTED

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESULT_USER_REJECTED: Int
```

The result code to propagate back to the user activity, indicates the association dialog is explicitly declined by the users.

 Value: 1

### TRUST_TYPE_CROSS_DEVICE_AUTHENTICATION

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TRUST_TYPE_CROSS_DEVICE_AUTHENTICATION: Int
```

Trust type for platform-level cross-device authentication.

This trust type is used for features where one device can authenticate another, typically based on proximity. For example, allowing a trusted watch to unlock a companion phone.

When this trust type is requested and granted during Companion Device Manager (CDM) trust pairing, the platform utilizes the established secure channel to facilitate these authentication flows.

 Value: 2

**See Also**

- `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager#requestDeviceTrustPairing(kotlin.Int,%20android.companion.OutOfBandPairingRequest,%20kotlin.IntArray,%20java.util.concurrent.Executor,%20android.companion.CompanionDeviceManager.TrustPairingCallback)`

### TRUST_TYPE_PROACTIVE_ASSISTANCE

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TRUST_TYPE_PROACTIVE_ASSISTANCE: Int
```

Trust type for proactive assistance. E.g. agents can use your app's screen content to provide proactive assistance.

 Value: 1

**See Also**

- `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager#requestDeviceTrustPairing(kotlin.Int,%20android.companion.OutOfBandPairingRequest,%20kotlin.IntArray,%20java.util.concurrent.Executor,%20android.companion.CompanionDeviceManager.TrustPairingCallback)`

### TRUST_TYPE_SCREEN_AUTOMATION

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TRUST_TYPE_SCREEN_AUTOMATION: Int
```

Trust type for screen automation. E.g. allowing agents to see and interact with the screen to help you complete tasks even if the screen is off.

 Value: 0

**See Also**

- `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager#requestDeviceTrustPairing(kotlin.Int,%20android.companion.OutOfBandPairingRequest,%20kotlin.IntArray,%20java.util.concurrent.Executor,%20android.companion.CompanionDeviceManager.TrustPairingCallback)`

## Public methods

### associate

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun associate(
    request: AssociationRequest, 
    callback: CompanionDeviceManager.Callback, 
    handler: Handler?
): Unit
```

Request to associate this app with a companion device.

Note that before creating establishing association the system may need to show UI to collect user confirmation.

If the app needs to be excluded from battery optimizations (run in the background) or to have unrestricted data access (use data in the background) it should declare use of `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#REQUEST_COMPANION_RUN_IN_BACKGROUND:kotlin.String` and `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#REQUEST_COMPANION_USE_DATA_IN_BACKGROUND:kotlin.String` in its AndroidManifest.xml respectively. Note that these special capabilities have a negative effect on the device's battery and user's data usage, therefore you should request them when absolutely necessary.

Application can use `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager#getMyAssociations()` for retrieving the list of currently `https://developer.android.com/reference/kotlin/android/companion/AssociationInfo` objects, that represent their existing associations. Applications can also use `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager#disassociate(kotlin.Int)` to remove an association, and are recommended to do when an association is no longer relevant to avoid unnecessary battery and/or data drain resulting from special privileges that the association provides

If this API is used to associate with a Bluetooth device, initiating Bluetooth bonding (e.g. via `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice.html#createBond()`) within 10 minutes of the association being approved allows the device to skip the Bluetooth pairing confirmation dialog (if its pairing variant is android.bluetooth.BluetoothDevice#PAIRING_VARIANT_CONSENT).

Calling this API requires a uses-feature `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_COMPANION_DEVICE_SETUP:kotlin.String` declaration in the manifest

| Parameters ||
|---|---|
| `request` | [AssociationRequest](https://developer.android.com/reference/kotlin/android/companion/AssociationRequest): A request object that describes details of the request. This value cannot be `null`. |
| `callback` | [CompanionDeviceManager.Callback](https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager.Callback): The callback used to notify application when the association is created. This value cannot be `null`. |
| `handler` | [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#)?: The handler which will be used to invoke the callback. This value may be `null`. |
| --- | --- |

**See Also**

- `https://developer.android.com/reference/kotlin/android/companion/AssociationRequest.Builder`
- `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager#getMyAssociations()`
- `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager#disassociate(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager#associate(android.companion.AssociationRequest,%20java.util.concurrent.Executor,%20android.companion.CompanionDeviceManager.Callback)`
- `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice.html#createBond()`

### associate

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun associate(
    request: AssociationRequest, 
    executor: Executor, 
    callback: CompanionDeviceManager.Callback
): Unit
```

Request to associate this app with a companion device.

Note that before creating establishing association the system may need to show UI to collect user confirmation.

If the app needs to be excluded from battery optimizations (run in the background) or to have unrestricted data access (use data in the background) it should declare use of `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#REQUEST_COMPANION_RUN_IN_BACKGROUND:kotlin.String` and `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#REQUEST_COMPANION_USE_DATA_IN_BACKGROUND:kotlin.String` in its AndroidManifest.xml respectively. Note that these special capabilities have a negative effect on the device's battery and user's data usage, therefore you should request them when absolutely necessary.

Application can use `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager#getMyAssociations()` for retrieving the list of currently `https://developer.android.com/reference/kotlin/android/companion/AssociationInfo` objects, that represent their existing associations. Applications can also use `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager#disassociate(kotlin.Int)` to remove an association, and are recommended to do when an association is no longer relevant to avoid unnecessary battery and/or data drain resulting from special privileges that the association provides

Note that if you use this api to associate with a Bluetooth device, please make sure to cancel your own Bluetooth discovery before calling this api, otherwise the callback may fail to return the desired device.

If this API is used to associate with a Bluetooth device, initiating Bluetooth bonding (e.g. via `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice.html#createBond()`) within 10 minutes of the association being approved allows the device to skip the Bluetooth pairing confirmation dialog (if its pairing variant is android.bluetooth.BluetoothDevice#PAIRING_VARIANT_CONSENT).

Calling this API requires a uses-feature `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_COMPANION_DEVICE_SETUP:kotlin.String` declaration in the manifest

| Parameters ||
|---|---|
| `request` | [AssociationRequest](https://developer.android.com/reference/kotlin/android/companion/AssociationRequest): A request object that describes details of the request. This value cannot be `null`. |
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#): The executor which will be used to invoke the callback. This value cannot be `null`. |
| `callback` | [CompanionDeviceManager.Callback](https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager.Callback): The callback used to notify application when the association is created. This value cannot be `null`. |
| --- | --- |

**See Also**

- `https://developer.android.com/reference/kotlin/android/companion/AssociationRequest.Builder`
- `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager#getMyAssociations()`
- `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager#disassociate(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter.html#cancelDiscovery()`
- `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice.html#createBond()`

### attachSystemDataTransport

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun attachSystemDataTransport(
    associationId: Int, 
    in: InputStream, 
    out: OutputStream
): Unit
```

Attach a bidirectional communication stream to be used as a transport channel for transporting system data between associated devices. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#DELIVER_COMPANION_MESSAGES:kotlin.String`

| Parameters ||
|---|---|
| `associationId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): id of the associated device. |
| `in` | [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#): Already connected stream of data incoming from remote associated device. This value cannot be `null`. |
| `out` | [OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream.html#): Already connected stream of data outgoing to remote associated device. This value cannot be `null`. |
| --- | --- |

| Exceptions ||
|---|---|
| `android.companion.DeviceNotAssociatedException` | Thrown if the associationId was not previously associated with this app. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager#buildPermissionTransferUserConsentIntent(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager#startSystemDataTransfer(kotlin.Int,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)`
- `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager#detachSystemDataTransport(kotlin.Int)`

### buildAssociationCancellationIntent

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun buildAssociationCancellationIntent(): IntentSender?
```

Cancel the current association activity.

The app should launch the returned `intentSender` by calling `https://developer.android.com/reference/kotlin/android/app/Activity.html#startIntentSenderForResult(android.content.IntentSender,%20kotlin.Int,%20android.content.Intent,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)` to cancel the current association activity

Calling this API requires a uses-feature `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_COMPANION_DEVICE_SETUP:kotlin.String` declaration in the manifest

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/IntentSender.html#?` | An `https://developer.android.com/reference/kotlin/android/content/IntentSender.html#` that the app should use to launch in order to cancel the current association activity. This value may be `null`. |

### buildPermissionTransferUserConsentIntent

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun buildPermissionTransferUserConsentIntent(associationId: Int): IntentSender?
```

Build a permission sync user consent dialog.

Only the companion app which owns the association can call this method. Otherwise a null IntentSender will be returned from this method and an error will be logged. The app should launch the `https://developer.android.com/reference/kotlin/android/app/Activity.html#` in the returned `intentSender` `https://developer.android.com/reference/kotlin/android/content/IntentSender.html#` by calling `https://developer.android.com/reference/kotlin/android/app/Activity.html#startIntentSenderForResult(android.content.IntentSender,%20kotlin.Int,%20android.content.Intent,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)`.

The permission transfer doesn't happen immediately after the call or when the user consents. The app needs to call `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager#attachSystemDataTransport(kotlin.Int,%20java.io.InputStream,%20java.io.OutputStream)` to attach a transport channel and `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager#startSystemDataTransfer(kotlin.Int,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)` to trigger the system data transfer}.

| Parameters ||
|---|---|
| `associationId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The unique `https://developer.android.com/reference/kotlin/android/companion/AssociationInfo#getId()` assigned to the association of the companion device recorded by CompanionDeviceManager |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/IntentSender.html#?` | An `https://developer.android.com/reference/kotlin/android/content/IntentSender.html#` that the app should use to launch the UI for the user to confirm the system data transfer request. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager#attachSystemDataTransport(kotlin.Int,%20java.io.InputStream,%20java.io.OutputStream)`
- `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager#startSystemDataTransfer(kotlin.Int,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)`

### createAndSetDeviceId

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun createAndSetDeviceId(
    associationId: Int, 
    deviceId: DeviceId?
): DeviceId?
```

Returns a new `https://developer.android.com/reference/kotlin/android/companion/DeviceId` which can be passed to device manufacturers' apps, allowing them to fetch `https://developer.android.com/reference/kotlin/android/companion/AssociationInfo` or observe device presence for this associated device. This method creates a new object and does not mutate any existing `https://developer.android.com/reference/kotlin/android/companion/DeviceId`.

The system will generate and assign a new, random 128-bit key to this returned `https://developer.android.com/reference/kotlin/android/companion/DeviceId`. Each call to this method generates a new key, any previously associated key will be obsoleted. Therefore, the returned `https://developer.android.com/reference/kotlin/android/companion/DeviceId` is the one that contains the newly assigned key and should be used for subsequent operations.

Calling this method also refreshes the association's `https://developer.android.com/reference/kotlin/android/companion/AssociationInfo#getAssociationToken()`.

This device id also helps the system uniquely identify your device for efficient device management and prevents duplicate entries.

WARNING: Do not pass the returned DeviceId to apps you do not trust.

| Parameters ||
|---|---|
| `associationId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The unique `https://developer.android.com/reference/kotlin/android/companion/AssociationInfo#getId()` assigned to the Association of the companion device recorded by CompanionDeviceManager. |
| `deviceId` | [DeviceId](https://developer.android.com/reference/kotlin/android/companion/DeviceId)?: to be used as device identifier to represent the associated device. This value may be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/companion/DeviceId?` | This value may be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/companion/AssociationInfo#getDeviceId()`
- `https://developer.android.com/reference/kotlin/android/companion/AssociationInfo#getAssociationToken()`

### detachSystemDataTransport

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun detachSystemDataTransport(associationId: Int): Unit
```

Detach the transport channel that's previously attached for the associated device. The system will stop transferring any system data when this method is called. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#DELIVER_COMPANION_MESSAGES:kotlin.String`

| Parameters ||
|---|---|
| `associationId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): id of the associated device. |

| Exceptions ||
|---|---|
| `android.companion.DeviceNotAssociatedException` | Thrown if the associationId was not previously associated with this app. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager#attachSystemDataTransport(kotlin.Int,%20java.io.InputStream,%20java.io.OutputStream)`

### disableSystemDataSyncForTypes

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun disableSystemDataSyncForTypes(
    associationId: Int, 
    flags: Int
): Unit
```

Disable system data sync for an associated device.

For Android versions prior to `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#CINNAMON_BUN:kotlin.Int`, only the following flags are supported:

- `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager#FLAG_CALL_METADATA:kotlin.Int`

<br />

Android versions above `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#CINNAMON_BUN:kotlin.Int` supports the following additional flags, each of which has its own default toggle state and may require specific permissions:

- `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager#FLAG_TASK_CONTINUITY:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager#FLAG_UNIVERSAL_MODES:kotlin.Int`
- FLAG_UNIVERSAL_CLIPBOARD
- `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager#FLAG_AIRPLANE_MODE:kotlin.Int`

<br />

Calling this API requires a uses-feature `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_COMPANION_DEVICE_SETUP:kotlin.String` declaration in the manifest

| Parameters ||
|---|---|
| `associationId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): id of the device association. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): system data types to be disabled. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager#FLAG_CALL_METADATA:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager#FLAG_TASK_CONTINUITY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager#FLAG_UNIVERSAL_MODES:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager#FLAG_AIRPLANE_MODE:kotlin.Int` |

### disassociate

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun disassociate(associationId: Int): Unit
```

Remove an association.

Any privileges provided via being associated with a given device will be revoked

Calling this API requires a uses-feature `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_COMPANION_DEVICE_SETUP:kotlin.String` declaration in the manifest

| Parameters ||
|---|---|
| `associationId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): id of the association to be removed. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager#associate(android.companion.AssociationRequest,%20java.util.concurrent.Executor,%20android.companion.CompanionDeviceManager.Callback)`
- `https://developer.android.com/reference/kotlin/android/companion/AssociationInfo#getId()`

### disassociate

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun disassociate(deviceMacAddress: String): Unit
```

**Deprecated:** *use `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager#disassociate(kotlin.Int)`*

Remove the association between this app and the device with the given mac address.

Any privileges provided via being associated with a given device will be revoked

Consider doing so when the association is no longer relevant to avoid unnecessary battery and/or data drain resulting from special privileges that the association provides

Calling this API requires a uses-feature `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_COMPANION_DEVICE_SETUP:kotlin.String` declaration in the manifest

| Parameters ||
|---|---|
| `deviceMacAddress` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the MAC address of device to disassociate from this app. Device address is case-sensitive in API level \< 33. This value cannot be `null`. |

### enableSystemDataSyncForTypes

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun enableSystemDataSyncForTypes(
    associationId: Int, 
    flags: Int
): Unit
```

Enable system data sync for an associated device.

For Android versions prior to `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#CINNAMON_BUN:kotlin.Int`, only the following flags are supported:

- `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager#FLAG_CALL_METADATA:kotlin.Int`

<br />

Android versions above `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#CINNAMON_BUN:kotlin.Int` supports the following additional flags, each of which has its own default toggle state and may require specific permissions:

- `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager#FLAG_TASK_CONTINUITY:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager#FLAG_UNIVERSAL_MODES:kotlin.Int`
- FLAG_UNIVERSAL_CLIPBOARD
- `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager#FLAG_AIRPLANE_MODE:kotlin.Int`

<br />

Calling this API requires a uses-feature `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_COMPANION_DEVICE_SETUP:kotlin.String` declaration in the manifest

| Parameters ||
|---|---|
| `associationId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): id of the device association. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): system data types to be enabled. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager#FLAG_CALL_METADATA:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager#FLAG_TASK_CONTINUITY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager#FLAG_UNIVERSAL_MODES:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager#FLAG_AIRPLANE_MODE:kotlin.Int` |

### getAssociations

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getAssociations(): MutableList<String!>
```

**Deprecated:** *use `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager#getMyAssociations()`*

Calling this API requires a uses-feature `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_COMPANION_DEVICE_SETUP:kotlin.String` declaration in the manifest

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>` | a list of MAC addresses of devices that have been previously associated with the current app are managed by CompanionDeviceManager (ie. does not include devices managed by application itself even if they have a MAC address). This value cannot be `null`. |

### getMyAssociations

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getMyAssociations(): MutableList<AssociationInfo!>
```

Calling this API requires a uses-feature `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_COMPANION_DEVICE_SETUP:kotlin.String` declaration in the manifest

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/companion/AssociationInfo!>` | a list of associations that have been previously associated with the current app. This value cannot be `null`. |

### hasNotificationAccess

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hasNotificationAccess(component: ComponentName!): Boolean
```

**Deprecated:** *Use `https://developer.android.com/reference/kotlin/android/app/NotificationManager.html#isNotificationListenerAccessGranted(android.content.ComponentName)` instead.*

Check whether the given component can access the notifications via a `https://developer.android.com/reference/kotlin/android/service/notification/NotificationListenerService.html#` Your app must have an association with a device before calling this API

Calling this API requires a uses-feature `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_COMPANION_DEVICE_SETUP:kotlin.String` declaration in the manifest

| Parameters ||
|---|---|
| `component` | [ComponentName](https://developer.android.com/reference/kotlin/android/content/ComponentName.html#)!: the name of the component |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | whether the given component has the notification listener permission |

### isPermissionTransferUserConsented

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isPermissionTransferUserConsented(associationId: Int): Boolean
```

Return the current state of consent for permission transfer for the association. True if the user has allowed permission transfer for the association, false otherwise.

Note: The initial user consent is collected via `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager#buildPermissionTransferUserConsentIntent(kotlin.Int)`. After the user has made their initial selection, they can toggle the permission transfer feature in the settings. This method always returns the state of the toggle setting.

| Parameters ||
|---|---|
| `associationId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The unique `https://developer.android.com/reference/kotlin/android/companion/AssociationInfo#getId()` assigned to the association of the companion device recorded by CompanionDeviceManager |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the user has consented to the permission transfer, or false otherwise. |

| Exceptions ||
|---|---|
| `android.companion.DeviceNotAssociatedException` | Exception if the companion device is not associated with the user or the calling app. |

### isSystemDataTransportAttached

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isSystemDataTransportAttached(associationId: Int): Boolean
```

Checks if a transport is currently attached for a given association id.

A transport is considered attached if `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager#attachSystemDataTransport(kotlin.Int,%20java.io.InputStream,%20java.io.OutputStream)` has been successfully called for the given `associationId`, and `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager#detachSystemDataTransport(kotlin.Int)` has not yet been called.

This is useful for determining if the system is ready to handle data transfers before calling `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager#startSystemDataTransfer(kotlin.Int,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)`.

The caller must meet one of the following requirements:

- It is the package that originally created the association.
- It holds the `android.permission.ACCESS_COMPANION_MESSAGE_PCC` permission and the association must be verified as a `https://developer.android.com/reference/kotlin/android/companion/AssociationInfo#isTrusted()`

| Parameters ||
|---|---|
| `associationId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The unique `https://developer.android.com/reference/kotlin/android/companion/AssociationInfo#getId()` of the device association |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if a system data transport is attached for the given association id, `false` otherwise. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager#attachSystemDataTransport(kotlin.Int,%20java.io.InputStream,%20java.io.OutputStream)`
- `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager#detachSystemDataTransport(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager#startSystemDataTransfer(kotlin.Int,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)`
- `https://developer.android.com/reference/kotlin/android/companion/AssociationInfo#isTrusted()`

### notifyActionResult

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun notifyActionResult(
    associationId: Int, 
    result: ActionResult
): Unit
```

Allows a companion app to report the result of an action that was requested by the system.

This API should be called after the app has received a request via `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceService#onActionRequested(android.companion.AssociationInfo,%20android.companion.ActionRequest)`. For example:

- After receiving `https://developer.android.com/reference/kotlin/android/companion/ActionRequest#OP_ACTIVATE:kotlin.Int`, the app should call this method with `https://developer.android.com/reference/kotlin/android/companion/ActionResult#RESULT_ACTIVATED:kotlin.Int` upon success or `https://developer.android.com/reference/kotlin/android/companion/ActionResult#RESULT_FAILED_TO_ACTIVATE:kotlin.Int` upon failure.
- If a previously activated feature later fails or stops for any reason, the app should proactively call this method with `https://developer.android.com/reference/kotlin/android/companion/ActionResult#RESULT_DEACTIVATED:kotlin.Int`.

| Parameters ||
|---|---|
| `result` | [ActionResult](https://developer.android.com/reference/kotlin/android/companion/ActionResult): The `https://developer.android.com/reference/kotlin/android/companion/ActionResult` to report to the system. This value cannot be `null`. |

### removeBond

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun removeBond(associationId: Int): Boolean
```

Remove bonding between this device and an associated companion device.

This is an asynchronous call, it will return immediately. Register for `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice.html#ACTION_BOND_STATE_CHANGED:kotlin.String` intents to be notified when the bond removal process completes, and its result.

This API should be used to remove a bluetooth bond that was created either by using `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice.html#createBond()` or by a direct user action. The association must already exist with this device before calling this method, but this may be done retroactively to remove a bond that was created outside of the CompanionDeviceManager. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String`

| Parameters ||
|---|---|
| `associationId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): an already-associated companion device to remove bond from |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | false on immediate error, true if bond removal process will begin |

### requestDeviceTrustPairing

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun requestDeviceTrustPairing(
    associationId: Int, 
    requestOobPairing: OutOfBandPairingRequest?, 
    trustTypes: IntArray, 
    executor: Executor, 
    callback: CompanionDeviceManager.TrustPairingCallback
): Unit
```

Request the system to initiate a trusted pairing process for the given association. This process is required to enable certain features that demand a higher level of trust between the devices.

The outcome of the pairing process will be delivered via the provided `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager.TrustPairingCallback`. The callback will first receive `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager.TrustPairingCallback#onTrustPairingPending(android.content.IntentSender)` with an `https://developer.android.com/reference/kotlin/android/content/IntentSender.html#` to launch a user confirmation dialog. Upon user confirmation and successful pairing, `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager.TrustPairingCallback#onDeviceTrusted(android.companion.AssociationInfo)` will be invoked. If the process fails or is canceled, `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager.TrustPairingCallback#onFailure(kotlin.Int)` or `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager.TrustPairingCallback#onTrustPairingCanceledFromRemote(android.companion.AssociationInfo,%20android.content.IntentSender)` will be called.

| Parameters ||
|---|---|
| `associationId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the unique `https://developer.android.com/reference/kotlin/android/companion/AssociationInfo#getId()` assigned to the Association recorded by CompanionDeviceManager |
| `requestOobPairing` | [OutOfBandPairingRequest](https://developer.android.com/reference/kotlin/android/companion/OutOfBandPairingRequest)?: request for out-of-band pairing. This value may be `null`. |
| `trustTypes` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html): list of trust types to be enabled that require trust pairing (or an empty array if no trust types are requested). This value cannot be `null`. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager#TRUST_TYPE_SCREEN_AUTOMATION:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager#TRUST_TYPE_PROACTIVE_ASSISTANCE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager#TRUST_TYPE_CROSS_DEVICE_AUTHENTICATION:kotlin.Int` |
| --- | --- |
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#): the executor to use for the callback. This value cannot be `null`. |
| `callback` | [CompanionDeviceManager.TrustPairingCallback](https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager.TrustPairingCallback): the callback to be invoked for the pairing process. This value cannot be `null`. |

### requestNotificationAccess

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun requestNotificationAccess(component: ComponentName!): Unit
```

Request notification access for the given component. The given component must follow the protocol specified in `https://developer.android.com/reference/kotlin/android/service/notification/NotificationListenerService.html#` Only components from the same `https://developer.android.com/reference/kotlin/android/content/ComponentName.html#getPackageName()` as the calling app are allowed. Your app must have an association with a device before calling this API. Side-loaded apps must allow restricted settings before requesting notification access.

Calling this API requires a uses-feature `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_COMPANION_DEVICE_SETUP:kotlin.String` declaration in the manifest

### setDeviceId

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setDeviceId(
    associationId: Int, 
    deviceId: DeviceId?
): Unit
```

**Deprecated:** *use `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager#createAndSetDeviceId(kotlin.Int,%20android.companion.DeviceId)` instead.*

Sets the `https://developer.android.com/reference/kotlin/android/companion/DeviceId` for this association.

This device id helps the system uniquely identify your device for efficient device management and prevents duplicate entries.

| Parameters ||
|---|---|
| `associationId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The unique `https://developer.android.com/reference/kotlin/android/companion/AssociationInfo#getId()` assigned to the Association of the companion device recorded by CompanionDeviceManager. |
| `deviceId` | [DeviceId](https://developer.android.com/reference/kotlin/android/companion/DeviceId)?: to be used as device identifier to represent the associated device. This value may be `null`. |

### startObservingDevicePresence

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun startObservingDevicePresence(request: ObservingDevicePresenceRequest): Unit
```

Register to receive callbacks whenever the associated device's presence changes. The presence could be:

- BLE range changes (in/out)
- Bluetooth connection status changes (connected/disconnected)

<br />

Caller app must implement the `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceService` to receive callbacks via `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceService#onDevicePresenceEvent(android.companion.DevicePresenceEvent)`. The system will bind to the implemented `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceService` to deliver the callbacks.

Calling app must check for feature presence of `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_COMPANION_DEVICE_SETUP:kotlin.String` before calling this API.

For Bluetooth LE devices, this is based on scanning for device with the given address. The system will scan for the device when Bluetooth is ON or Bluetooth scanning is ON.

For Bluetooth classic devices this is triggered when the device connects/disconnects.

WiFi devices are not supported.

If a Bluetooth LE device wants to use a rotating mac address, it is recommended to use Resolvable Private Address, and ensure the device is bonded to the phone so that android OS is able to resolve the address.
. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#REQUEST_OBSERVE_COMPANION_DEVICE_PRESENCE:kotlin.String`

| Parameters ||
|---|---|
| `request` | [ObservingDevicePresenceRequest](https://developer.android.com/reference/kotlin/android/companion/ObservingDevicePresenceRequest): A request for setting the types of device for observing device presence. This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/companion/ObservingDevicePresenceRequest.Builder`
- `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceService#onDevicePresenceEvent(android.companion.DevicePresenceEvent)`

### startObservingDevicePresence

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun startObservingDevicePresence(deviceAddress: String): Unit
```

**Deprecated:** *use `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager#startObservingDevicePresence(android.companion.ObservingDevicePresenceRequest)` instead.*

Register to receive callbacks whenever the associated device comes in and out of range.

The provided device must be #associate with the calling app before calling this method.

Caller must implement a single `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceService` which will be bound to and receive callbacks to android.companion.CompanionDeviceService#onDeviceAppeared and android.companion.CompanionDeviceService#onDeviceDisappeared. The app doesn't need to remain running in order to receive its callbacks.

Calling app must declare uses-permission `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#REQUEST_OBSERVE_COMPANION_DEVICE_PRESENCE:kotlin.String`.

Calling app must check for feature presence of `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_COMPANION_DEVICE_SETUP:kotlin.String` before calling this API.

For Bluetooth LE devices, this is based on scanning for device with the given address. The system will scan for the device when Bluetooth is ON or Bluetooth scanning is ON.

For Bluetooth classic devices this is triggered when the device connects/disconnects. WiFi devices are not supported.

If a Bluetooth LE device wants to use a rotating mac address, it is recommended to use Resolvable Private Address, and ensure the device is bonded to the phone so that android OS is able to resolve the address.
. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#REQUEST_OBSERVE_COMPANION_DEVICE_PRESENCE:kotlin.String`

| Parameters ||
|---|---|
| `deviceAddress` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): a previously-associated companion device's address. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `android.companion.DeviceNotAssociatedException` | if the given device was not previously associated with this app. |

### startSystemDataTransfer

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun startSystemDataTransfer(
    associationId: Int, 
    executor: Executor, 
    result: OutcomeReceiver<Void!, CompanionException!>
): Unit
```

Start system data transfer which has been previously approved by the user.

Before calling this method, the app needs to make sure `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager#attachSystemDataTransport(kotlin.Int,%20java.io.InputStream,%20java.io.OutputStream)`, and `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager#buildPermissionTransferUserConsentIntent(kotlin.Int)`. The transfer will fail if the transport channel is disconnected or `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager#detachSystemDataTransport(kotlin.Int)` during the transfer.

| Parameters ||
|---|---|
| `associationId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The unique `https://developer.android.com/reference/kotlin/android/companion/AssociationInfo#getId()` assigned to the Association of the companion device recorded by CompanionDeviceManager |
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#): The executor which will be used to invoke the result callback. This value cannot be `null`. |
| `result` | [OutcomeReceiver](https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#)\< [Void](https://developer.android.com/reference/kotlin/java/lang/Void.html#)!, [CompanionException](https://developer.android.com/reference/kotlin/android/companion/CompanionException)!\>: The callback to notify the app of the result of the system data transfer. This value cannot be `null`. |
| --- | --- |

| Exceptions ||
|---|---|
| `android.companion.DeviceNotAssociatedException` | Exception if the companion device is not associated |

### stopObservingDevicePresence

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun stopObservingDevicePresence(request: ObservingDevicePresenceRequest): Unit
```

Unregister for receiving callbacks whenever the associated device comes in and out of range. Calling app must check for feature presence of `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_COMPANION_DEVICE_SETUP:kotlin.String` before calling this API. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#REQUEST_OBSERVE_COMPANION_DEVICE_PRESENCE:kotlin.String`

| Parameters ||
|---|---|
| `request` | [ObservingDevicePresenceRequest](https://developer.android.com/reference/kotlin/android/companion/ObservingDevicePresenceRequest): A request for setting the types of device for observing device presence. This value cannot be `null`. |

### stopObservingDevicePresence

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun stopObservingDevicePresence(deviceAddress: String): Unit
```

**Deprecated:** *use `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager#stopObservingDevicePresence(android.companion.ObservingDevicePresenceRequest)` instead.*

Unregister for receiving callbacks whenever the associated device comes in and out of range. The provided device must be #associate with the calling app before calling this method. Calling app must declare uses-permission `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#REQUEST_OBSERVE_COMPANION_DEVICE_PRESENCE:kotlin.String`. Calling app must check for feature presence of `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_COMPANION_DEVICE_SETUP:kotlin.String` before calling this API. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#REQUEST_OBSERVE_COMPANION_DEVICE_PRESENCE:kotlin.String`

| Parameters ||
|---|---|
| `deviceAddress` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): a previously-associated companion device's address. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `android.companion.DeviceNotAssociatedException` | if the given device was not previously associated with this app. |
