Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DeviceAdminReceiver

```
open class DeviceAdminReceiver : BroadcastReceiver
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.content.BroadcastReceiver](../android.content/BroadcastReceiver.md) ||
| | ↳ | [android.app.admin.DeviceAdminReceiver](DeviceAdminReceiver.md) |

Base class for implementing a device administration component. This class provides a convenience for interpreting the raw intent actions that are sent by the system.

The callback methods, like the base onReceive method, happen on the main thread of the process. Thus long running operations must be done on another thread. Note that because a receiver is done once returning from its receive function, such long-running operations should probably be done in a `https://developer.android.com/reference/kotlin/android/app/Service.html#`.

When publishing your DeviceAdmin subclass as a receiver, it must handle `https://developer.android.com/reference/kotlin/android/app/admin/DeviceAdminReceiver#ACTION_DEVICE_ADMIN_ENABLED:kotlin.String` and require the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BIND_DEVICE_ADMIN:kotlin.String` permission. A typical manifest entry would look like:

The meta-data referenced here provides addition information specific to the device administrator, as parsed by the DeviceAdminInfo class. A typical file would be:

<br />

> [!NOTE]
>
> ### Developer Guides
>
> For more information about device administration, read the [Device Administration](https://developer.android.com/guide/topics/admin/device-admin.html) developer guide.

## Summary

| Constants ||
|---|---|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/admin/DeviceAdminReceiver#ACTION_CHOOSE_PRIVATE_KEY_ALIAS:kotlin.String` Broadcast action: notify that some app is attempting to choose a KeyChain key. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/admin/DeviceAdminReceiver#ACTION_DEVICE_ADMIN_DISABLED:kotlin.String` Action sent to a device administrator when the user has disabled it. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/admin/DeviceAdminReceiver#ACTION_DEVICE_ADMIN_DISABLE_REQUESTED:kotlin.String` Action sent to a device administrator when the user has requested to disable it, but before this has actually been done. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/admin/DeviceAdminReceiver#ACTION_DEVICE_ADMIN_ENABLED:kotlin.String` This is the primary action that a device administrator must implement to be allowed to manage a device. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/admin/DeviceAdminReceiver#ACTION_LOCK_TASK_ENTERING:kotlin.String` Action sent to a device administrator to notify that the device is entering lock task mode. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/admin/DeviceAdminReceiver#ACTION_LOCK_TASK_EXITING:kotlin.String` Action sent to a device administrator to notify that the device is exiting lock task mode. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/admin/DeviceAdminReceiver#ACTION_NETWORK_LOGS_AVAILABLE:kotlin.String` Broadcast action: notify that a new batch of network logs is ready to be collected. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/admin/DeviceAdminReceiver#ACTION_PASSWORD_CHANGED:kotlin.String` Action sent to a device administrator when the user has changed the password of their device or profile challenge. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/admin/DeviceAdminReceiver#ACTION_PASSWORD_EXPIRING:kotlin.String` Action periodically sent to a device administrator when the device or profile challenge password is expiring. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/admin/DeviceAdminReceiver#ACTION_PASSWORD_FAILED:kotlin.String` Action sent to a device administrator when the user has entered an incorrect device or profile challenge password. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/admin/DeviceAdminReceiver#ACTION_PASSWORD_SUCCEEDED:kotlin.String` Action sent to a device administrator when the user has successfully entered their device or profile challenge password, after failing one or more times. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/admin/DeviceAdminReceiver#ACTION_PROFILE_PROVISIONING_COMPLETE:kotlin.String` Broadcast Action: This broadcast is sent to indicate that provisioning of a managed profile or managed device has completed successfully. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/admin/DeviceAdminReceiver#ACTION_SECURITY_LOGS_AVAILABLE:kotlin.String` Broadcast action: notify that a new batch of security logs is ready to be collected. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/admin/DeviceAdminReceiver#BUGREPORT_FAILURE_FAILED_COMPLETING:kotlin.Int` Bugreport completion process failed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/admin/DeviceAdminReceiver#BUGREPORT_FAILURE_FILE_NO_LONGER_AVAILABLE:kotlin.Int` Bugreport has been created, but is no longer available for collection. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/admin/DeviceAdminReceiver#DEVICE_ADMIN_META_DATA:kotlin.String` Name under which a DevicePolicy component publishes information about itself. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/admin/DeviceAdminReceiver#EXTRA_DISABLE_WARNING:kotlin.String` A CharSequence that can be shown to the user informing them of the impact of disabling your admin. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/admin/DeviceAdminReceiver#EXTRA_LOCK_TASK_PACKAGE:kotlin.String` A string containing the name of the package entering lock task mode. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/admin/DeviceAdminReceiver#EXTRA_TRANSFER_OWNERSHIP_ADMIN_EXTRAS_BUNDLE:kotlin.String` A `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` extra of type `https://developer.android.com/reference/kotlin/android/os/PersistableBundle.html#` that allows a mobile device management application to pass data to the management application instance after owner transfer. |

| Public constructors ||
|---|---|
| DeviceAdminReceiver <br /> |

| Public methods ||
|---|---|
| open [DevicePolicyManager](DevicePolicyManager.md) | getManager Retrieve the DevicePolicyManager interface for this administrator to work with the system. |
| open [ComponentName](../android.content/ComponentName.md) | getWho Retrieve the ComponentName describing who this device administrator is, for use in DevicePolicyManager APIs that require the administrator to identify itself. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onBugreportFailed Called when the bugreport collection flow has failed. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onBugreportShared Called when the bugreport has been shared with the device administrator app. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onBugreportSharingDeclined Called when sharing a bugreport has been cancelled by the user of the device. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | onChoosePrivateKeyAlias Allows this receiver to select the alias for a private key and certificate pair for authentication. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onComplianceAcknowledgementRequired Called to notify a profile owner of an organization-owned device that it needs to acknowledge device compliance to allow the user to turn the profile off if needed according to the maximum profile time off policy. |
| open [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | onDisableRequested Called when the user has asked to disable the administrator, as a result of receiving `https://developer.android.com/reference/kotlin/android/app/admin/DeviceAdminReceiver#ACTION_DEVICE_ADMIN_DISABLE_REQUESTED:kotlin.String`, giving you a chance to present a warning message to them. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onDisabled Called prior to the administrator being disabled, as a result of receiving `https://developer.android.com/reference/kotlin/android/app/admin/DeviceAdminReceiver#ACTION_DEVICE_ADMIN_DISABLED:kotlin.String`. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onEnabled Called after the administrator is first enabled, as a result of receiving `https://developer.android.com/reference/kotlin/android/app/admin/DeviceAdminReceiver#ACTION_DEVICE_ADMIN_ENABLED:kotlin.String`. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onLockTaskModeEntering Called when a device is entering lock task mode. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onLockTaskModeExiting Called when a device is exiting lock task mode. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onNetworkLogsAvailable Called each time a new batch of network logs can be retrieved. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onOperationSafetyStateChanged Called to notify the state of operations that can be unsafe to execute has changed. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onPasswordChanged Called after the user has changed their device or profile challenge password, as a result of receiving `https://developer.android.com/reference/kotlin/android/app/admin/DeviceAdminReceiver#ACTION_PASSWORD_CHANGED:kotlin.String`. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onPasswordChanged Called after the user has changed their device or profile challenge password, as a result of receiving `https://developer.android.com/reference/kotlin/android/app/admin/DeviceAdminReceiver#ACTION_PASSWORD_CHANGED:kotlin.String`. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onPasswordExpiring Called periodically when the device or profile challenge password is about to expire or has expired. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onPasswordExpiring Called periodically when the device or profile challenge password is about to expire or has expired. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onPasswordFailed Called after the user has failed at entering their device or profile challenge password, as a result of receiving `https://developer.android.com/reference/kotlin/android/app/admin/DeviceAdminReceiver#ACTION_PASSWORD_FAILED:kotlin.String`. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onPasswordFailed Called after the user has failed at entering their device or profile challenge password, as a result of receiving `https://developer.android.com/reference/kotlin/android/app/admin/DeviceAdminReceiver#ACTION_PASSWORD_FAILED:kotlin.String`. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onPasswordSucceeded Called after the user has succeeded at entering their device or profile challenge password, as a result of receiving `https://developer.android.com/reference/kotlin/android/app/admin/DeviceAdminReceiver#ACTION_PASSWORD_SUCCEEDED:kotlin.String`. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onPasswordSucceeded Called after the user has succeeded at entering their device or profile challenge password, as a result of receiving `https://developer.android.com/reference/kotlin/android/app/admin/DeviceAdminReceiver#ACTION_PASSWORD_SUCCEEDED:kotlin.String`. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onProfileProvisioningComplete Called when provisioning of a managed profile or managed device has completed successfully. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onReadyForUserInitialization Called during provisioning of a managed device to allow the device initializer to perform user setup steps. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onReceive Intercept standard device administrator broadcasts. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onSecurityLogsAvailable Called when a new batch of security logs can be retrieved. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onSystemUpdatePending Called when the information about a pending system update is available. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onTransferAffiliatedProfileOwnershipComplete Called on the device owner when the ownership of one of its affiliated profiles is transferred. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onTransferOwnershipComplete Called on the newly assigned owner (either device owner or profile owner) when the ownership transfer has completed successfully. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onUserAdded Called when a user or profile is created. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onUserRemoved Called when a user or profile is removed. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onUserStarted Called when a user or profile is started. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onUserStopped Called when a user or profile is stopped. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onUserSwitched Called when a user or profile is switched to. |

Inherited functions From class `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#` `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` abortBroadcast

Sets the flag indicating that this receiver should abort the current broadcast; only works with broadcasts sent through sendOrderedBroadcast. This will prevent any other broadcast receivers from receiving the broadcast. It will still call onReceive of the BroadcastReceiver that the caller of sendOrderedBroadcast passed in.

**This method does not work with non-ordered broadcasts such as those sent with sendBroadcast**

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` clearAbortBroadcast

Clears the flag indicating that this receiver should abort the current broadcast.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` getAbortBroadcast

Returns the flag indicating whether or not this receiver should abort the current broadcast.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` getDebugUnregister

Return the last value given to setDebugUnregister.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` getResultCode

Retrieve the current result code, as set by the previous receiver.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` getResultData

Retrieve the current result data, as set by the previous receiver. Often this is null.

<br />

`https://developer.android.com/reference/kotlin/android/os/Bundle.html#!` getResultExtras

Retrieve the current result extra data, as set by the previous receiver. Any changes you make to the returned Map will be propagated to the next receiver.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?` getSentFromPackage

Returns the package name of the app that initially sent this broadcast.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` getSentFromUid

Returns the uid of the app that initially sent this broadcast.

<br />

`https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.PendingResult.html#!` goAsync

This can be called by an application in onReceive to allow it to keep the broadcast active after returning from that function. This does *not* change the expectation of being relatively responsive to the broadcast, but does allow the implementation to move work related to it over to another thread to avoid glitching the main UI thread due to disk IO.

As a general rule, broadcast receivers are allowed to run for up to 10 seconds before the system will consider them non-responsive and ANR the app. Since these usually execute on the app's main thread, they are already bound by the \~5 second time limit of various operations that can happen there (not to mention just avoiding UI jank), so the receive limit is generally not of concern. However, once you use `goAsync`, though able to be off the main thread, the broadcast execution limit still applies, and that includes the time spent between calling this method and ultimately finish.

If you are taking advantage of this method to have more time to execute, it is useful to know that the available time can be longer in certain situations. In particular, if the broadcast you are receiving is not a foreground broadcast (that is, the sender has not used `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_RECEIVER_FOREGROUND:kotlin.Int`), then more time is allowed for the receivers to run, allowing them to execute for 30 seconds or even a bit more. This is something that receivers should rarely take advantage of (long work should be punted to another system facility such as `https://developer.android.com/reference/kotlin/android/app/job/JobScheduler.html#`, `https://developer.android.com/reference/kotlin/android/app/Service.html#`, or see especially androidx.core.app.JobIntentService), but can be useful in certain rare cases where it is necessary to do some work as soon as the broadcast is delivered. Keep in mind that the work you do here will block further broadcasts until it completes, so taking advantage of this at all excessively can be counter-productive and cause later events to be received more slowly.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` isInitialStickyBroadcast

Returns true if the receiver is currently processing the initial value of a sticky broadcast -- that is, the value that was last broadcast and is currently held in the sticky cache, so this is not directly the result of a broadcast right now.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` isOrderedBroadcast

Returns true if the receiver is currently processing an ordered broadcast.

<br />

`https://developer.android.com/reference/kotlin/android/os/IBinder.html#!` peekService

Provide a binder to an already-bound service. This method is synchronous and will not start the target service if it is not present, so it is safe to call from onReceive. For peekService() to return a non null `https://developer.android.com/reference/kotlin/android/os/IBinder.html#` interface the service must have published it before. In other words some component must have called bindService on it.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setDebugUnregister

Control inclusion of debugging help for mismatched calls to registerReceiver. If called with true, before given to registerReceiver(), then the callstack of the following unregisterReceiver call is retained, to be printed if a later incorrect unregister call is made. Note that doing this requires retaining information about the BroadcastReceiver for the lifetime of the app, resulting in a leak -- this should only be used for debugging.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setOrderedHint

For internal use, sets the hint about whether this BroadcastReceiver is running in ordered mode.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setResult

Change all of the result data returned from this broadcasts; only works with broadcasts sent through sendOrderedBroadcast. All current result data is replaced by the value given to this method.

**This method does not work with non-ordered broadcasts such as those sent with sendBroadcast**

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setResultCode

Change the current result code of this broadcast; only works with broadcasts sent through sendOrderedBroadcast. Often uses the Activity `https://developer.android.com/reference/kotlin/android/app/Activity.html#RESULT_CANCELED:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/app/Activity.html#RESULT_OK:kotlin.Int` constants, though the actual meaning of this value is ultimately up to the broadcaster.

This method does not work with non-ordered broadcasts such as those sent with sendBroadcast

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setResultData

Change the current result data of this broadcast; only works with broadcasts sent through sendOrderedBroadcast. This is an arbitrary string whose interpretation is up to the broadcaster.

**This method does not work with non-ordered broadcasts such as those sent with sendBroadcast**

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setResultExtras

Change the current result extras of this broadcast; only works with broadcasts sent through sendOrderedBroadcast. This is a Bundle holding arbitrary data, whose interpretation is up to the broadcaster. Can be set to null. Calling this method completely replaces the current map (if any).

**This method does not work with non-ordered broadcasts such as those sent with sendBroadcast**

<br />

## Constants

### ACTION_CHOOSE_PRIVATE_KEY_ALIAS

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_CHOOSE_PRIVATE_KEY_ALIAS: String
```

Broadcast action: notify that some app is attempting to choose a KeyChain key.

 Value: "android.app.action.CHOOSE_PRIVATE_KEY_ALIAS"

**See Also**

- onChoosePrivateKeyAlias
- onChoosePrivateKeyAlias

### ACTION_DEVICE_ADMIN_DISABLED

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_DEVICE_ADMIN_DISABLED: String
```

Action sent to a device administrator when the user has disabled it. Upon return, the application no longer has access to the protected device policy manager APIs. You will generally handle this in onDisabled. Note that this action will be sent the receiver regardless of whether it is explicitly listed in its intent filter.

 Value: "android.app.action.DEVICE_ADMIN_DISABLED"

### ACTION_DEVICE_ADMIN_DISABLE_REQUESTED

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_DEVICE_ADMIN_DISABLE_REQUESTED: String
```

Action sent to a device administrator when the user has requested to disable it, but before this has actually been done. This gives you a chance to supply a message to the user about the impact of disabling your admin, by setting the extra field `https://developer.android.com/reference/kotlin/android/app/admin/DeviceAdminReceiver#EXTRA_DISABLE_WARNING:kotlin.String` in the result Intent. If not set, no warning will be displayed. If set, the given text will be shown to the user before they disable your admin.

 Value: "android.app.action.DEVICE_ADMIN_DISABLE_REQUESTED"

### ACTION_DEVICE_ADMIN_ENABLED

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_DEVICE_ADMIN_ENABLED: String
```

This is the primary action that a device administrator must implement to be allowed to manage a device. This will be set to the receiver when the user enables it for administration. You will generally handle this in onEnabled. To be supported, the receiver must also require the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BIND_DEVICE_ADMIN:kotlin.String` permission so that other applications can not abuse it.

 Value: "android.app.action.DEVICE_ADMIN_ENABLED"

### ACTION_LOCK_TASK_ENTERING

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_LOCK_TASK_ENTERING: String
```

Action sent to a device administrator to notify that the device is entering lock task mode. The extra `https://developer.android.com/reference/kotlin/android/app/admin/DeviceAdminReceiver#EXTRA_LOCK_TASK_PACKAGE:kotlin.String` will describe the package using lock task mode.

The calling device admin must be the device owner or profile owner to receive this broadcast.

 Value: "android.app.action.LOCK_TASK_ENTERING"

**See Also**

- isLockTaskPermitted

### ACTION_LOCK_TASK_EXITING

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_LOCK_TASK_EXITING: String
```

Action sent to a device administrator to notify that the device is exiting lock task mode.

The calling device admin must be the device owner or profile owner to receive this broadcast.

 Value: "android.app.action.LOCK_TASK_EXITING"

**See Also**

- isLockTaskPermitted

### ACTION_NETWORK_LOGS_AVAILABLE

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_NETWORK_LOGS_AVAILABLE: String
```

Broadcast action: notify that a new batch of network logs is ready to be collected.

 Value: "android.app.action.NETWORK_LOGS_AVAILABLE"

**See Also**

- onNetworkLogsAvailable
- onNetworkLogsAvailable

### ACTION_PASSWORD_CHANGED

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_PASSWORD_CHANGED: String
```

Action sent to a device administrator when the user has changed the password of their device or profile challenge. You can at this point check the characteristics of the new password with isActivePasswordSufficient. You will generally handle this in onPasswordChanged.

The calling device admin must have requested `https://developer.android.com/reference/kotlin/android/app/admin/DeviceAdminInfo#USES_POLICY_LIMIT_PASSWORD:kotlin.Int` to receive this broadcast.

 Value: "android.app.action.ACTION_PASSWORD_CHANGED"

### ACTION_PASSWORD_EXPIRING

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_PASSWORD_EXPIRING: String
```

Action periodically sent to a device administrator when the device or profile challenge password is expiring. You will generally handle this in onPasswordExpiring.

The calling device admin must have requested `https://developer.android.com/reference/kotlin/android/app/admin/DeviceAdminInfo#USES_POLICY_EXPIRE_PASSWORD:kotlin.Int` to receive this broadcast.

 Value: "android.app.action.ACTION_PASSWORD_EXPIRING"

### ACTION_PASSWORD_FAILED

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_PASSWORD_FAILED: String
```

Action sent to a device administrator when the user has entered an incorrect device or profile challenge password. You can at this point check the number of failed password attempts there have been with getCurrentFailedPasswordAttempts. You will generally handle this in onPasswordFailed.

The calling device admin must have requested `https://developer.android.com/reference/kotlin/android/app/admin/DeviceAdminInfo#USES_POLICY_WATCH_LOGIN:kotlin.Int` to receive this broadcast.

 Value: "android.app.action.ACTION_PASSWORD_FAILED"

### ACTION_PASSWORD_SUCCEEDED

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_PASSWORD_SUCCEEDED: String
```

Action sent to a device administrator when the user has successfully entered their device or profile challenge password, after failing one or more times. You will generally handle this in onPasswordSucceeded.

The calling device admin must have requested `https://developer.android.com/reference/kotlin/android/app/admin/DeviceAdminInfo#USES_POLICY_WATCH_LOGIN:kotlin.Int` to receive this broadcast.

 Value: "android.app.action.ACTION_PASSWORD_SUCCEEDED"

### ACTION_PROFILE_PROVISIONING_COMPLETE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_PROFILE_PROVISIONING_COMPLETE: String
```

Broadcast Action: This broadcast is sent to indicate that provisioning of a managed profile or managed device has completed successfully.

The broadcast is limited to the profile that will be managed by the application that requested provisioning. In the device owner case the profile is the primary user. The broadcast will also be limited to the DeviceAdminReceiver component specified in the original intent or NFC bump that started the provisioning process (see `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager#ACTION_PROVISION_MANAGED_PROFILE:kotlin.String`).

A device admin application which listens to this intent can find out if the device was provisioned for the device owner or profile owner case by calling respectively isDeviceOwnerApp and isProfileOwnerApp. You will generally handle this in onProfileProvisioningComplete.

The intent for this action may include the following extras:

- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager#EXTRA_PROVISIONING_ADMIN_EXTRAS_BUNDLE:kotlin.String`

 Value: "android.app.action.PROFILE_PROVISIONING_COMPLETE"

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager#ACTION_PROVISIONING_SUCCESSFUL:kotlin.String`

### ACTION_SECURITY_LOGS_AVAILABLE

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_SECURITY_LOGS_AVAILABLE: String
```

Broadcast action: notify that a new batch of security logs is ready to be collected.

 Value: "android.app.action.SECURITY_LOGS_AVAILABLE"

### BUGREPORT_FAILURE_FAILED_COMPLETING

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val BUGREPORT_FAILURE_FAILED_COMPLETING: Int
```

Bugreport completion process failed.

If this error code is received, the requesting of bugreport can be retried.

 Value: 0

**See Also**

- requestBugreport

### BUGREPORT_FAILURE_FILE_NO_LONGER_AVAILABLE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val BUGREPORT_FAILURE_FILE_NO_LONGER_AVAILABLE: Int
```

Bugreport has been created, but is no longer available for collection.

This error likely occurs because the user of the device hasn't consented to share the bugreport for a long period after its creation.

If this error code is received, the requesting of bugreport can be retried.

 Value: 1

**See Also**

- requestBugreport

### DEVICE_ADMIN_META_DATA

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DEVICE_ADMIN_META_DATA: String
```

Name under which a DevicePolicy component publishes information about itself. This meta-data must reference an XML resource containing a device-admin tag.

 Value: "android.app.device_admin"

### EXTRA_DISABLE_WARNING

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_DISABLE_WARNING: String
```

A CharSequence that can be shown to the user informing them of the impact of disabling your admin.

 Value: "android.app.extra.DISABLE_WARNING"

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/admin/DeviceAdminReceiver#ACTION_DEVICE_ADMIN_DISABLE_REQUESTED:kotlin.String`

### EXTRA_LOCK_TASK_PACKAGE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_LOCK_TASK_PACKAGE: String
```

A string containing the name of the package entering lock task mode.

 Value: "android.app.extra.LOCK_TASK_PACKAGE"

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/admin/DeviceAdminReceiver#ACTION_LOCK_TASK_ENTERING:kotlin.String`

### EXTRA_TRANSFER_OWNERSHIP_ADMIN_EXTRAS_BUNDLE

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_TRANSFER_OWNERSHIP_ADMIN_EXTRAS_BUNDLE: String
```

A `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` extra of type `https://developer.android.com/reference/kotlin/android/os/PersistableBundle.html#` that allows a mobile device management application to pass data to the management application instance after owner transfer.

If the transfer is successful, the new owner receives the data in onTransferOwnershipComplete. The bundle is not changed during the ownership transfer.

 Value: "android.app.extra.TRANSFER_OWNERSHIP_ADMIN_EXTRAS_BUNDLE"

**See Also**

- transferOwnership

## Public constructors

### DeviceAdminReceiver

```
DeviceAdminReceiver()
```

## Public methods

### getManager

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getManager(context: Context): DevicePolicyManager
```

Retrieve the DevicePolicyManager interface for this administrator to work with the system.

| Parameters ||
|---|---|
| `context` | [Context](../android.content/Context.md): This value cannot be `null`. |

| Return ||
|---|---|
| DevicePolicyManager | This value cannot be `null`. |

### getWho

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getWho(context: Context): ComponentName
```

Retrieve the ComponentName describing who this device administrator is, for use in DevicePolicyManager APIs that require the administrator to identify itself.

| Parameters ||
|---|---|
| `context` | [Context](../android.content/Context.md): This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/ComponentName.html#` | This value cannot be `null`. |

### onBugreportFailed

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onBugreportFailed(
    context: Context, 
    intent: Intent, 
    failureCode: Int
): Unit
```

Called when the bugreport collection flow has failed.

This callback is only applicable to device owners.

| Parameters ||
|---|---|
| `context` | [Context](../android.content/Context.md): The running context as per onReceive. This value cannot be `null`. |
| `intent` | [Intent](../android.content/Intent.md): The received intent as per onReceive. This value cannot be `null`. |
| `failureCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): int containing failure code. One of `https://developer.android.com/reference/kotlin/android/app/admin/DeviceAdminReceiver#BUGREPORT_FAILURE_FAILED_COMPLETING:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/app/admin/DeviceAdminReceiver#BUGREPORT_FAILURE_FILE_NO_LONGER_AVAILABLE:kotlin.Int` Value is one of the following: - `https://developer.android.com/reference/kotlin/android/app/admin/DeviceAdminReceiver#BUGREPORT_FAILURE_FAILED_COMPLETING:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/admin/DeviceAdminReceiver#BUGREPORT_FAILURE_FILE_NO_LONGER_AVAILABLE:kotlin.Int` |
| --- | --- |

**See Also**

- requestBugreport

### onBugreportShared

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onBugreportShared(
    context: Context, 
    intent: Intent, 
    bugreportHash: String
): Unit
```

Called when the bugreport has been shared with the device administrator app.

This callback is only applicable to device owners.

| Parameters ||
|---|---|
| `context` | [Context](../android.content/Context.md): The running context as per onReceive. This value cannot be `null`. |
| `intent` | [Intent](../android.content/Intent.md): The received intent as per onReceive. Contains the URI of the bugreport file (with MIME type "application/vnd.android.bugreport"), that can be accessed by calling getData This value cannot be `null`. |
| `bugreportHash` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): SHA-256 hash of the bugreport file. This value cannot be `null`. |
| --- | --- |

**See Also**

- requestBugreport

### onBugreportSharingDeclined

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onBugreportSharingDeclined(
    context: Context, 
    intent: Intent
): Unit
```

Called when sharing a bugreport has been cancelled by the user of the device.

This callback is only applicable to device owners.

| Parameters ||
|---|---|
| `context` | [Context](../android.content/Context.md): The running context as per onReceive. This value cannot be `null`. |
| `intent` | [Intent](../android.content/Intent.md): The received intent as per onReceive. This value cannot be `null`. |

**See Also**

- requestBugreport

### onChoosePrivateKeyAlias

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onChoosePrivateKeyAlias(
    context: Context, 
    intent: Intent, 
    uid: Int, 
    uri: Uri?, 
    alias: String?
): String?
```

Allows this receiver to select the alias for a private key and certificate pair for authentication. If this method returns null, the default `https://developer.android.com/reference/kotlin/android/app/Activity.html#` will be shown that lets the user pick a private key and certificate pair. If this method returns `https://developer.android.com/reference/kotlin/android/security/KeyChain.html#KEY_ALIAS_SELECTION_DENIED:kotlin.String`, the default `https://developer.android.com/reference/kotlin/android/app/Activity.html#` will not be shown and the user will not be allowed to pick anything. And the app, that called android.security.KeyChain#choosePrivateKeyAlias, will receive `null` back.

| Parameters ||
|---|---|
| `context` | [Context](../android.content/Context.md): The running context as per onReceive. This value cannot be `null`. |
| `intent` | [Intent](../android.content/Intent.md): The received intent as per onReceive. This value cannot be `null`. |
| `uid` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The uid of the app asking for the private key and certificate pair. |
| --- | --- |
| `uri` | [Uri](../android.net/Uri.md)?: The URI to authenticate, may be null. |
| `alias` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: The alias preselected by the client, or null. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?` | The private key alias to return and grant access to. |

**See Also**

### onComplianceAcknowledgementRequired

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onComplianceAcknowledgementRequired(
    context: Context, 
    intent: Intent
): Unit
```

Called to notify a profile owner of an organization-owned device that it needs to acknowledge device compliance to allow the user to turn the profile off if needed according to the maximum profile time off policy.

Default implementation acknowledges compliance immediately. DPC may prefer to override this implementation to delay acknowledgement until a successful policy sync. Until compliance is acknowledged the user is still free to turn the profile off, but the timer won't be reset, so personal apps will be suspended sooner. This callback is delivered using a foreground broadcast and should be handled quickly.

| Parameters ||
|---|---|
| `context` | [Context](../android.content/Context.md): the running context as per onReceive This value cannot be `null`. |
| `intent` | [Intent](../android.content/Intent.md): The received intent as per onReceive. This value cannot be `null`. |

**See Also**

- acknowledgeDeviceCompliant
- isComplianceAcknowledgementRequired
- setManagedProfileMaximumTimeOff

### onDisableRequested

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onDisableRequested(
    context: Context, 
    intent: Intent
): CharSequence?
```

Called when the user has asked to disable the administrator, as a result of receiving `https://developer.android.com/reference/kotlin/android/app/admin/DeviceAdminReceiver#ACTION_DEVICE_ADMIN_DISABLE_REQUESTED:kotlin.String`, giving you a chance to present a warning message to them. The message is returned as the result; if null is returned (the default implementation), no message will be displayed.

| Parameters ||
|---|---|
| `context` | [Context](../android.content/Context.md): The running context as per onReceive. This value cannot be `null`. |
| `intent` | [Intent](../android.content/Intent.md): The received intent as per onReceive. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html?` | Return the warning message to display to the user before being disabled; if null is returned, no message is displayed. |

### onDisabled

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onDisabled(
    context: Context, 
    intent: Intent
): Unit
```

Called prior to the administrator being disabled, as a result of receiving `https://developer.android.com/reference/kotlin/android/app/admin/DeviceAdminReceiver#ACTION_DEVICE_ADMIN_DISABLED:kotlin.String`. Upon return, you can no longer use the protected parts of the DevicePolicyManager API.

| Parameters ||
|---|---|
| `context` | [Context](../android.content/Context.md): The running context as per onReceive. This value cannot be `null`. |
| `intent` | [Intent](../android.content/Intent.md): The received intent as per onReceive. This value cannot be `null`. |

### onEnabled

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onEnabled(
    context: Context, 
    intent: Intent
): Unit
```

Called after the administrator is first enabled, as a result of receiving `https://developer.android.com/reference/kotlin/android/app/admin/DeviceAdminReceiver#ACTION_DEVICE_ADMIN_ENABLED:kotlin.String`. At this point you can use DevicePolicyManager to set your desired policies.

If the admin is activated by a device owner, then the intent may contain private extras that are relevant to user setup. See createAndManageUser

| Parameters ||
|---|---|
| `context` | [Context](../android.content/Context.md): The running context as per onReceive. This value cannot be `null`. |
| `intent` | [Intent](../android.content/Intent.md): The received intent as per onReceive. This value cannot be `null`. |

### onLockTaskModeEntering

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onLockTaskModeEntering(
    context: Context, 
    intent: Intent, 
    pkg: String
): Unit
```

Called when a device is entering lock task mode.

| Parameters ||
|---|---|
| `context` | [Context](../android.content/Context.md): The running context as per onReceive. This value cannot be `null`. |
| `intent` | [Intent](../android.content/Intent.md): The received intent as per onReceive. This value cannot be `null`. |
| `pkg` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The authorized package using lock task mode. This value cannot be `null`. |
| --- | --- |

### onLockTaskModeExiting

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onLockTaskModeExiting(
    context: Context, 
    intent: Intent
): Unit
```

Called when a device is exiting lock task mode.

| Parameters ||
|---|---|
| `context` | [Context](../android.content/Context.md): The running context as per onReceive. This value cannot be `null`. |
| `intent` | [Intent](../android.content/Intent.md): The received intent as per onReceive. This value cannot be `null`. |

### onNetworkLogsAvailable

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onNetworkLogsAvailable(
    context: Context, 
    intent: Intent, 
    batchToken: Long, 
    networkLogsCount: Int
): Unit
```

Called each time a new batch of network logs can be retrieved. This callback method will only ever be called when network logging is enabled. The logs can only be retrieved while network logging is enabled.

If a secondary user or profile is created, this callback won't be received until all users become affiliated again (even if network logging is enabled). It will also no longer be possible to retrieve the network logs batch with the most recent `batchToken` provided by this callback. See setAffiliationIds.

This callback is only applicable to device owners and profile owners.

This callback is triggered by a foreground broadcast and the app should ensure that any long-running work is not executed synchronously inside the callback.

| Parameters ||
|---|---|
| `context` | [Context](../android.content/Context.md): The running context as per onReceive. This value cannot be `null`. |
| `intent` | [Intent](../android.content/Intent.md): The received intent as per onReceive. This value cannot be `null`. |
| `batchToken` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): The token representing the current batch of network logs. |
| --- | --- |
| `networkLogsCount` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The total count of events in the current batch of network logs. Value is 1 or greater |

**See Also**

- retrieveNetworkLogs

### onOperationSafetyStateChanged

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onOperationSafetyStateChanged(
    context: Context, 
    reason: Int, 
    isSafe: Boolean
): Unit
```

Called to notify the state of operations that can be unsafe to execute has changed.

**Note:** notice that the operation safety state might change between the time this callback is received and the operation's method on DevicePolicyManager is called, so calls to the latter could still throw a UnsafeStateException even when this method is called with `isSafe` as `true`

| Parameters ||
|---|---|
| `context` | [Context](../android.content/Context.md): the running context as per onReceive This value cannot be `null`. |
| `reason` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the reason an operation could be unsafe. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager#OPERATION_SAFETY_REASON_DRIVING_DISTRACTION:kotlin.Int` |
| `isSafe` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): whether the operation is safe to be executed. |
| --- | --- |

### onPasswordChanged

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onPasswordChanged(
    context: Context, 
    intent: Intent
): Unit
```

**Deprecated:** *From `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#O:kotlin.Int`, use onPasswordChanged instead.*

Called after the user has changed their device or profile challenge password, as a result of receiving `https://developer.android.com/reference/kotlin/android/app/admin/DeviceAdminReceiver#ACTION_PASSWORD_CHANGED:kotlin.String`. At this point you can use getPasswordQuality to retrieve the active password characteristics.

| Parameters ||
|---|---|
| `context` | [Context](../android.content/Context.md): The running context as per onReceive. This value cannot be `null`. |
| `intent` | [Intent](../android.content/Intent.md): The received intent as per onReceive. This value cannot be `null`. |

### onPasswordChanged

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onPasswordChanged(
    context: Context, 
    intent: Intent, 
    user: UserHandle
): Unit
```

Called after the user has changed their device or profile challenge password, as a result of receiving `https://developer.android.com/reference/kotlin/android/app/admin/DeviceAdminReceiver#ACTION_PASSWORD_CHANGED:kotlin.String`. At this point you can use getPasswordQuality to retrieve the active password characteristics.

| Parameters ||
|---|---|
| `context` | [Context](../android.content/Context.md): The running context as per onReceive. This value cannot be `null`. |
| `intent` | [Intent](../android.content/Intent.md): The received intent as per onReceive. This value cannot be `null`. |
| `user` | [UserHandle](../android.os/UserHandle.md): The user or profile for whom the password changed. To see whether this user is the current profile or a parent user, check for equality with myUserHandle. This value cannot be `null`. |
| --- | --- |

### onPasswordExpiring

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onPasswordExpiring(
    context: Context, 
    intent: Intent
): Unit
```

**Deprecated:** *From `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#O:kotlin.Int`, use onPasswordExpiring instead.*

Called periodically when the device or profile challenge password is about to expire or has expired. It will typically be called at these times: on device boot, once per day before the password expires, and at the time when the password expires.

If the password is not updated by the user, this method will continue to be called once per day until the password is changed or the device admin disables password expiration.

The admin will typically post a notification requesting the user to change their password in response to this call. The actual password expiration time can be obtained by calling getPasswordExpiration

The admin should be sure to take down any notifications it posted in response to this call when it receives onPasswordChanged.

| Parameters ||
|---|---|
| `context` | [Context](../android.content/Context.md): The running context as per onReceive. This value cannot be `null`. |
| `intent` | [Intent](../android.content/Intent.md): The received intent as per onReceive. This value cannot be `null`. |

### onPasswordExpiring

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onPasswordExpiring(
    context: Context, 
    intent: Intent, 
    user: UserHandle
): Unit
```

Called periodically when the device or profile challenge password is about to expire or has expired. It will typically be called at these times: on device boot, once per day before the password expires, and at the time when the password expires.

If the password is not updated by the user, this method will continue to be called once per day until the password is changed or the device admin disables password expiration.

The admin will typically post a notification requesting the user to change their password in response to this call. The actual password expiration time can be obtained by calling getPasswordExpiration

The admin should be sure to take down any notifications it posted in response to this call when it receives onPasswordChanged.

| Parameters ||
|---|---|
| `context` | [Context](../android.content/Context.md): The running context as per onReceive. This value cannot be `null`. |
| `intent` | [Intent](../android.content/Intent.md): The received intent as per onReceive. This value cannot be `null`. |
| `user` | [UserHandle](../android.os/UserHandle.md): The user or profile for whom the password is expiring. To see whether this user is the current profile or a parent user, check for equality with myUserHandle. This value cannot be `null`. |
| --- | --- |

### onPasswordFailed

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onPasswordFailed(
    context: Context, 
    intent: Intent
): Unit
```

**Deprecated:** *From `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#O:kotlin.Int`, use onPasswordFailed instead.*

Called after the user has failed at entering their device or profile challenge password, as a result of receiving `https://developer.android.com/reference/kotlin/android/app/admin/DeviceAdminReceiver#ACTION_PASSWORD_FAILED:kotlin.String`. At this point you can use getCurrentFailedPasswordAttempts to retrieve the number of failed password attempts.

| Parameters ||
|---|---|
| `context` | [Context](../android.content/Context.md): The running context as per onReceive. This value cannot be `null`. |
| `intent` | [Intent](../android.content/Intent.md): The received intent as per onReceive. This value cannot be `null`. |

### onPasswordFailed

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onPasswordFailed(
    context: Context, 
    intent: Intent, 
    user: UserHandle
): Unit
```

Called after the user has failed at entering their device or profile challenge password, as a result of receiving `https://developer.android.com/reference/kotlin/android/app/admin/DeviceAdminReceiver#ACTION_PASSWORD_FAILED:kotlin.String`. At this point you can use getCurrentFailedPasswordAttempts to retrieve the number of failed password attempts.

| Parameters ||
|---|---|
| `context` | [Context](../android.content/Context.md): The running context as per onReceive. This value cannot be `null`. |
| `intent` | [Intent](../android.content/Intent.md): The received intent as per onReceive. This value cannot be `null`. |
| `user` | [UserHandle](../android.os/UserHandle.md): The user or profile for whom the password check failed. To see whether this user is the current profile or a parent user, check for equality with myUserHandle. This value cannot be `null`. |
| --- | --- |

### onPasswordSucceeded

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onPasswordSucceeded(
    context: Context, 
    intent: Intent
): Unit
```

**Deprecated:** *From `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#O:kotlin.Int`, use onPasswordSucceeded instead.*

Called after the user has succeeded at entering their device or profile challenge password, as a result of receiving `https://developer.android.com/reference/kotlin/android/app/admin/DeviceAdminReceiver#ACTION_PASSWORD_SUCCEEDED:kotlin.String`. This will only be received the first time they succeed after having previously failed.

| Parameters ||
|---|---|
| `context` | [Context](../android.content/Context.md): The running context as per onReceive. This value cannot be `null`. |
| `intent` | [Intent](../android.content/Intent.md): The received intent as per onReceive. This value cannot be `null`. |

### onPasswordSucceeded

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onPasswordSucceeded(
    context: Context, 
    intent: Intent, 
    user: UserHandle
): Unit
```

Called after the user has succeeded at entering their device or profile challenge password, as a result of receiving `https://developer.android.com/reference/kotlin/android/app/admin/DeviceAdminReceiver#ACTION_PASSWORD_SUCCEEDED:kotlin.String`. This will only be received the first time they succeed after having previously failed.

| Parameters ||
|---|---|
| `context` | [Context](../android.content/Context.md): The running context as per onReceive. This value cannot be `null`. |
| `intent` | [Intent](../android.content/Intent.md): The received intent as per onReceive. This value cannot be `null`. |
| `user` | [UserHandle](../android.os/UserHandle.md): The user of profile for whom the password check succeeded. To see whether this user is the current profile or a parent user, check for equality with myUserHandle. This value cannot be `null`. |
| --- | --- |

### onProfileProvisioningComplete

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onProfileProvisioningComplete(
    context: Context, 
    intent: Intent
): Unit
```

Called when provisioning of a managed profile or managed device has completed successfully.

As a prerequisite for the execution of this callback the DeviceAdminReceiver has to declare an intent filter for `https://developer.android.com/reference/kotlin/android/app/admin/DeviceAdminReceiver#ACTION_PROFILE_PROVISIONING_COMPLETE:kotlin.String`. Its component must also be specified in the `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager#EXTRA_DEVICE_ADMIN:kotlin.String` of the `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager#ACTION_PROVISION_MANAGED_PROFILE:kotlin.String` intent that started the managed provisioning.

When provisioning of a managed profile is complete, the managed profile is hidden until the profile owner calls setProfileEnabled. Typically a profile owner will enable the profile when it has finished any additional setup such as adding an account by using the `https://developer.android.com/reference/kotlin/android/accounts/AccountManager.html#` and calling APIs to bring the profile into the desired state.

Note that provisioning completes without waiting for any server interactions, so the profile owner needs to wait for data to be available if required (e.g. Android device IDs or other data that is set as a result of server interactions).

From version `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#O:kotlin.Int`, when managed provisioning has completed, along with this callback the activity intent `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager#ACTION_PROVISIONING_SUCCESSFUL:kotlin.String` will also be sent to the same application.

The `Intent` may include any of the extras specified for `https://developer.android.com/reference/kotlin/android/app/admin/DeviceAdminReceiver#ACTION_PROFILE_PROVISIONING_COMPLETE:kotlin.String`.

| Parameters ||
|---|---|
| `context` | [Context](../android.content/Context.md): The running context as per onReceive. This value cannot be `null`. |
| `intent` | [Intent](../android.content/Intent.md): The received intent as per onReceive. This value cannot be `null`. |

### onReadyForUserInitialization

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onReadyForUserInitialization(
    context: Context, 
    intent: Intent
): Unit
```

**Deprecated:** *Do not use*

Called during provisioning of a managed device to allow the device initializer to perform user setup steps.

| Parameters ||
|---|---|
| `context` | [Context](../android.content/Context.md): The running context as per onReceive. This value cannot be `null`. |
| `intent` | [Intent](../android.content/Intent.md): The received intent as per onReceive. This value cannot be `null`. |

### onReceive

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onReceive(
    context: Context, 
    intent: Intent
): Unit
```

Intercept standard device administrator broadcasts. Implementations should not override this method; it is better to implement the convenience callbacks for each action.

| Parameters ||
|---|---|
| `context` | [Context](../android.content/Context.md): This value cannot be `null`. |
| `intent` | [Intent](../android.content/Intent.md): This value cannot be `null`. |

### onSecurityLogsAvailable

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onSecurityLogsAvailable(
    context: Context, 
    intent: Intent
): Unit
```

Called when a new batch of security logs can be retrieved.

If a secondary user or profile is created, this callback won't be received until all users become affiliated again (even if security logging is enabled). See setAffiliationIds

This callback will be re-triggered if the logs are not retrieved.

This callback is only applicable to device owners and profile owners of organization-owned managed profiles.

This callback is triggered by a foreground broadcast and the app should ensure that any long-running work is not executed synchronously inside the callback.

| Parameters ||
|---|---|
| `context` | [Context](../android.content/Context.md): The running context as per onReceive. This value cannot be `null`. |
| `intent` | [Intent](../android.content/Intent.md): The received intent as per onReceive. This value cannot be `null`. |

**See Also**

- retrieveSecurityLogs

### onSystemUpdatePending

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onSystemUpdatePending(
    context: Context, 
    intent: Intent, 
    receivedTime: Long
): Unit
```

Called when the information about a pending system update is available.

Allows the receiver to be notified when information about a pending system update is available from the system update service. The same pending system update can trigger multiple calls to this method, so it is necessary to examine the incoming parameters for details about the update.

This callback is only applicable to device owners and profile owners.

To get further information about a pending system update (for example, whether or not the update is a security patch), the device owner or profile owner can call getPendingSystemUpdate.

| Parameters ||
|---|---|
| `context` | [Context](../android.content/Context.md): The running context as per onReceive. This value cannot be `null`. |
| `intent` | [Intent](../android.content/Intent.md): The received intent as per onReceive. This value cannot be `null`. |
| `receivedTime` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): The time as given by currentTimeMillis indicating when the current pending update was first available. -1 if no pending update is available. |
| --- | --- |

**See Also**

- getPendingSystemUpdate

### onTransferAffiliatedProfileOwnershipComplete

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onTransferAffiliatedProfileOwnershipComplete(
    context: Context, 
    user: UserHandle
): Unit
```

Called on the device owner when the ownership of one of its affiliated profiles is transferred.

This can be used when transferring both device and profile ownership when using work profile on a fully managed device. The process would look like this:

1. Transfer profile ownership
2. The device owner gets notified with this callback
3. Transfer device ownership
4. Both profile and device ownerships have been transferred

| Parameters ||
|---|---|
| `context` | [Context](../android.content/Context.md): the running context as per onReceive This value cannot be `null`. |
| `user` | [UserHandle](../android.os/UserHandle.md): the `https://developer.android.com/reference/kotlin/android/os/UserHandle.html#` of the affiliated user. This value cannot be `null`. |

**See Also**

- transferOwnership

### onTransferOwnershipComplete

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onTransferOwnershipComplete(
    context: Context, 
    bundle: PersistableBundle?
): Unit
```

Called on the newly assigned owner (either device owner or profile owner) when the ownership transfer has completed successfully.

The `bundle` parameter allows the original owner to pass data to the new one.

| Parameters ||
|---|---|
| `context` | [Context](../android.content/Context.md): the running context as per onReceive This value cannot be `null`. |
| `bundle` | [PersistableBundle](../android.os/PersistableBundle.md)?: the data to be passed to the new owner. This value may be `null`. |

### onUserAdded

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onUserAdded(
    context: Context, 
    intent: Intent, 
    addedUser: UserHandle
): Unit
```

Called when a user or profile is created.

This callback is only applicable to device owners.

| Parameters ||
|---|---|
| `context` | [Context](../android.content/Context.md): The running context as per onReceive. This value cannot be `null`. |
| `intent` | [Intent](../android.content/Intent.md): The received intent as per onReceive. This value cannot be `null`. |
| `addedUser` | [UserHandle](../android.os/UserHandle.md): The `https://developer.android.com/reference/kotlin/android/os/UserHandle.html#` of the user that has just been added. This value cannot be `null`. |
| --- | --- |

### onUserRemoved

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onUserRemoved(
    context: Context, 
    intent: Intent, 
    removedUser: UserHandle
): Unit
```

Called when a user or profile is removed.

This callback is only applicable to device owners.

| Parameters ||
|---|---|
| `context` | [Context](../android.content/Context.md): The running context as per onReceive. This value cannot be `null`. |
| `intent` | [Intent](../android.content/Intent.md): The received intent as per onReceive. This value cannot be `null`. |
| `removedUser` | [UserHandle](../android.os/UserHandle.md): The `https://developer.android.com/reference/kotlin/android/os/UserHandle.html#` of the user that has just been removed. This value cannot be `null`. |
| --- | --- |

### onUserStarted

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onUserStarted(
    context: Context, 
    intent: Intent, 
    startedUser: UserHandle
): Unit
```

Called when a user or profile is started.

This callback is only applicable to device owners.

| Parameters ||
|---|---|
| `context` | [Context](../android.content/Context.md): The running context as per onReceive. This value cannot be `null`. |
| `intent` | [Intent](../android.content/Intent.md): The received intent as per onReceive. This value cannot be `null`. |
| `startedUser` | [UserHandle](../android.os/UserHandle.md): The `https://developer.android.com/reference/kotlin/android/os/UserHandle.html#` of the user that has just been started. This value cannot be `null`. |
| --- | --- |

### onUserStopped

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onUserStopped(
    context: Context, 
    intent: Intent, 
    stoppedUser: UserHandle
): Unit
```

Called when a user or profile is stopped.

This callback is only applicable to device owners.

| Parameters ||
|---|---|
| `context` | [Context](../android.content/Context.md): The running context as per onReceive. This value cannot be `null`. |
| `intent` | [Intent](../android.content/Intent.md): The received intent as per onReceive. This value cannot be `null`. |
| `stoppedUser` | [UserHandle](../android.os/UserHandle.md): The `https://developer.android.com/reference/kotlin/android/os/UserHandle.html#` of the user that has just been stopped. This value cannot be `null`. |
| --- | --- |

### onUserSwitched

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onUserSwitched(
    context: Context, 
    intent: Intent, 
    switchedUser: UserHandle
): Unit
```

Called when a user or profile is switched to.

This callback is only applicable to device owners.

| Parameters ||
|---|---|
| `context` | [Context](../android.content/Context.md): The running context as per onReceive. This value cannot be `null`. |
| `intent` | [Intent](../android.content/Intent.md): The received intent as per onReceive. This value cannot be `null`. |
| `switchedUser` | [UserHandle](../android.os/UserHandle.md): The `https://developer.android.com/reference/kotlin/android/os/UserHandle.html#` of the user that has just been switched to. This value cannot be `null`. |
| --- | --- |
