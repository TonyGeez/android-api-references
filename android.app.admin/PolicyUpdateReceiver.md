# PolicyUpdateReceiver

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PolicyUpdateReceiver

Kotlin| [Java](../android/app/admin/PolicyUpdateReceiver.md) 
| --- | --- |

```
abstract class PolicyUpdateReceiver : BroadcastReceiver
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.content.BroadcastReceiver](../android/content/BroadcastReceiver.md) ||
| | ↳ | [android.app.admin.PolicyUpdateReceiver](../android/app/admin/PolicyUpdateReceiver.md) |

Base class for implementing a policy update receiver. This class provides a convenience for interpreting the raw intent actions ([ACTION_DEVICE_POLICY_SET_RESULT](../android/app/admin/PolicyUpdateReceiver.md) and [ACTION_DEVICE_POLICY_CHANGED](../android/app/admin/PolicyUpdateReceiver.md)) that are sent by the system.

The callback methods happen on the main thread of the process. Thus, long-running operations must be done on another thread.

When publishing your`PolicyUpdateReceiver`subclass as a receiver, it must require the [android.Manifest.permission#BIND_DEVICE_ADMIN](../android/Manifest.permission.md) permission.

Admins can implement [DeviceAdminService](../android/app/admin/DeviceAdminService.md) to ensure they receive all policy updates (for policies they have set) via [onPolicyChanged](../android/app/admin/PolicyUpdateReceiver.md))by constantly being bound to by the system. For more information see [DeviceAdminService](../android/app/admin/DeviceAdminService.md).

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ACTION_DEVICE_POLICY_CHANGED](../android/app/admin/PolicyUpdateReceiver.md) Action for a broadcast sent to admins to communicate back a change in a policy they have previously set. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ACTION_DEVICE_POLICY_SET_RESULT](../android/app/admin/PolicyUpdateReceiver.md) Action for a broadcast sent to admins to communicate back the result of setting a policy in [DevicePolicyManager](../android/app/admin/DevicePolicyManager.md). |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_ACCOUNT_TYPE](../android/app/admin/PolicyUpdateReceiver.md) A string extra holding the account type this policy applies to, (see [PolicyUpdateReceiver.onPolicyChanged](../android/app/admin/PolicyUpdateReceiver.md))and [PolicyUpdateReceiver.onPolicySetResult](../android/app/admin/PolicyUpdateReceiver.md))) |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_INTENT_FILTER](../android/app/admin/PolicyUpdateReceiver.md) An [android.content.IntentFilter](../android/content/IntentFilter.md) extra holding the intent filter the policy relates to, (see [PolicyUpdateReceiver.onPolicyChanged](../android/app/admin/PolicyUpdateReceiver.md))and [PolicyUpdateReceiver.onPolicySetResult](../android/app/admin/PolicyUpdateReceiver.md))) |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_PACKAGE_NAME](../android/app/admin/PolicyUpdateReceiver.md) A string extra holding the package name the policy applies to, (see [PolicyUpdateReceiver.onPolicyChanged](../android/app/admin/PolicyUpdateReceiver.md))and [PolicyUpdateReceiver.onPolicySetResult](../android/app/admin/PolicyUpdateReceiver.md))) |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_PERMISSION_NAME](../android/app/admin/PolicyUpdateReceiver.md) A string extra holding the permission name the policy applies to, (see [PolicyUpdateReceiver.onPolicyChanged](../android/app/admin/PolicyUpdateReceiver.md))and [PolicyUpdateReceiver.onPolicySetResult](../android/app/admin/PolicyUpdateReceiver.md))) |
| --- | --- |

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [PolicyUpdateReceiver](../android/app/admin/PolicyUpdateReceiver.md))`()` <br /> |

| Public methods ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onPolicyChanged](../android/app/admin/PolicyUpdateReceiver.md))`(`context:` ` [Context](../android/content/Context.md)`, `policyIdentifier:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `additionalPolicyParams:` ` [Bundle](../android/os/Bundle.md)`, `targetUser:` ` [TargetUser](../android/app/admin/TargetUser.md)`, `policyUpdateResult:` ` [PolicyUpdateResult](../android/app/admin/PolicyUpdateResult.md)`)` Callback triggered when a policy previously set by the admin has changed. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onPolicySetResult](../android/app/admin/PolicyUpdateReceiver.md))`(`context:` ` [Context](../android/content/Context.md)`, `policyIdentifier:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `additionalPolicyParams:` ` [Bundle](../android/os/Bundle.md)`, `targetUser:` ` [TargetUser](../android/app/admin/TargetUser.md)`, `policyUpdateResult:` ` [PolicyUpdateResult](../android/app/admin/PolicyUpdateResult.md)`)` Callback triggered after an admin has set a policy using one of the APIs in [DevicePolicyManager](../android/app/admin/DevicePolicyManager.md) to notify the admin whether it has been successful or not. |

| Inherited functions ||
|---|---|
| From class [BroadcastReceiver](../android/content/BroadcastReceiver.md) |------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [abortBroadcast](../android/content/BroadcastReceiver.md))`()` <br /> Sets the flag indicating that this receiver should abort the current broadcast; only works with broadcasts sent through [Context.sendOrderedBroadcast](../android/content/Context.md)). This will prevent any other broadcast receivers from receiving the broadcast. It will still call [onReceive](../android/content/BroadcastReceiver.md))of the BroadcastReceiver that the caller of [Context.sendOrderedBroadcast](../android/content/Context.md))passed in. **This method does not work with non-ordered broadcasts such as those sent with [Context.sendBroadcast](../android/content/Context.md))** <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clearAbortBroadcast](../android/content/BroadcastReceiver.md))`()` <br /> Clears the flag indicating that this receiver should abort the current broadcast. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getAbortBroadcast](../android/content/BroadcastReceiver.md))`()` <br /> Returns the flag indicating whether or not this receiver should abort the current broadcast. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getDebugUnregister](../android/content/BroadcastReceiver.md))`()` <br /> Return the last value given to [setDebugUnregister](../android/content/BroadcastReceiver.md)). <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getResultCode](../android/content/BroadcastReceiver.md))`()` <br /> Retrieve the current result code, as set by the previous receiver. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getResultData](../android/content/BroadcastReceiver.md))`()` <br /> Retrieve the current result data, as set by the previous receiver. Often this is null. <br /> | | [Bundle](../android/os/Bundle.md)! | [getResultExtras](../android/content/BroadcastReceiver.md))`(`makeMap:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Retrieve the current result extra data, as set by the previous receiver. Any changes you make to the returned Map will be propagated to the next receiver. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getSentFromPackage](../android/content/BroadcastReceiver.md))`()` <br /> Returns the package name of the app that initially sent this broadcast. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSentFromUid](../android/content/BroadcastReceiver.md))`()` <br /> Returns the uid of the app that initially sent this broadcast. <br /> | | [BroadcastReceiver.PendingResult](../android/content/BroadcastReceiver.PendingResult.md)! | [goAsync](../android/content/BroadcastReceiver.md))`()` <br /> This can be called by an application in [onReceive](../android/content/BroadcastReceiver.md))to allow it to keep the broadcast active after returning from that function. This does*not*change the expectation of being relatively responsive to the broadcast, but does allow the implementation to move work related to it over to another thread to avoid glitching the main UI thread due to disk IO. As a general rule, broadcast receivers are allowed to run for up to 10 seconds before the system will consider them non-responsive and ANR the app. Since these usually execute on the app's main thread, they are already bound by the \~5 second time limit of various operations that can happen there (not to mention just avoiding UI jank), so the receive limit is generally not of concern. However, once you use`goAsync`, though able to be off the main thread, the broadcast execution limit still applies, and that includes the time spent between calling this method and ultimately [PendingResult.finish()](../android/content/BroadcastReceiver.PendingResult.md)). If you are taking advantage of this method to have more time to execute, it is useful to know that the available time can be longer in certain situations. In particular, if the broadcast you are receiving is not a foreground broadcast (that is, the sender has not used [Intent.FLAG_RECEIVER_FOREGROUND](../android/content/Intent.md)), then more time is allowed for the receivers to run, allowing them to execute for 30 seconds or even a bit more. This is something that receivers should rarely take advantage of (long work should be punted to another system facility such as [android.app.job.JobScheduler](../android/app/job/JobScheduler.md), [android.app.Service](../android/app/Service.md), or see especially androidx.core.app.JobIntentService), but can be useful in certain rare cases where it is necessary to do some work as soon as the broadcast is delivered. Keep in mind that the work you do here will block further broadcasts until it completes, so taking advantage of this at all excessively can be counter-productive and cause later events to be received more slowly. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isInitialStickyBroadcast](../android/content/BroadcastReceiver.md))`()` <br /> Returns true if the receiver is currently processing the initial value of a sticky broadcast -- that is, the value that was last broadcast and is currently held in the sticky cache, so this is not directly the result of a broadcast right now. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isOrderedBroadcast](../android/content/BroadcastReceiver.md))`()` <br /> Returns true if the receiver is currently processing an ordered broadcast. <br /> | | [IBinder](../android/os/IBinder.md)! | [peekService](../android/content/BroadcastReceiver.md))`(`myContext:` ` [Context](../android/content/Context.md)!`, `service:` ` [Intent](../android/content/Intent.md)!`)` <br /> Provide a binder to an already-bound service. This method is synchronous and will not start the target service if it is not present, so it is safe to call from [onReceive](../android/content/BroadcastReceiver.md)). For peekService() to return a non null [android.os.IBinder](../android/os/IBinder.md) interface the service must have published it before. In other words some component must have called [android.content.Context#bindService(Intent, ServiceConnection, int)](../android/content/Context.md))on it. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDebugUnregister](../android/content/BroadcastReceiver.md))`(`debug:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Control inclusion of debugging help for mismatched calls to [Context.registerReceiver()](../android/content/Context.md)). If called with true, before given to registerReceiver(), then the callstack of the following [Context.unregisterReceiver()](../android/content/Context.md))call is retained, to be printed if a later incorrect unregister call is made. Note that doing this requires retaining information about the BroadcastReceiver for the lifetime of the app, resulting in a leak -- this should only be used for debugging. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOrderedHint](../android/content/BroadcastReceiver.md))`(`isOrdered:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> For internal use, sets the hint about whether this BroadcastReceiver is running in ordered mode. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setResult](../android/content/BroadcastReceiver.md))`(`code:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `data:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `extras:` ` [Bundle](../android/os/Bundle.md)!`)` <br /> Change all of the result data returned from this broadcasts; only works with broadcasts sent through [Context.sendOrderedBroadcast](../android/content/Context.md)). All current result data is replaced by the value given to this method. **This method does not work with non-ordered broadcasts such as those sent with [Context.sendBroadcast](../android/content/Context.md))** <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setResultCode](../android/content/BroadcastReceiver.md))`(`code:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Change the current result code of this broadcast; only works with broadcasts sent through [Context.sendOrderedBroadcast](../android/content/Context.md)). Often uses the Activity [android.app.Activity#RESULT_CANCELED](../android/app/Activity.md) and [android.app.Activity#RESULT_OK](../android/app/Activity.md) constants, though the actual meaning of this value is ultimately up to the broadcaster. This method does not work with non-ordered broadcasts such as those sent with [Context.sendBroadcast](../android/content/Context.md)) <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setResultData](../android/content/BroadcastReceiver.md))`(`data:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Change the current result data of this broadcast; only works with broadcasts sent through [Context.sendOrderedBroadcast](../android/content/Context.md)). This is an arbitrary string whose interpretation is up to the broadcaster. **This method does not work with non-ordered broadcasts such as those sent with [Context.sendBroadcast](../android/content/Context.md))** <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setResultExtras](../android/content/BroadcastReceiver.md))`(`extras:` ` [Bundle](../android/os/Bundle.md)!`)` <br /> Change the current result extras of this broadcast; only works with broadcasts sent through [Context.sendOrderedBroadcast](../android/content/Context.md)). This is a Bundle holding arbitrary data, whose interpretation is up to the broadcaster. Can be set to null. Calling this method completely replaces the current map (if any). **This method does not work with non-ordered broadcasts such as those sent with [Context.sendBroadcast](../android/content/Context.md))** <br /> | ||

## Constants

### ACTION_DEVICE_POLICY_CHANGED

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACTION_DEVICE_POLICY_CHANGED: String
```

Action for a broadcast sent to admins to communicate back a change in a policy they have previously set.

Admins wishing to receive these updates should include this action in the intent filter for their receiver in the manifest, the receiver must be protected by [android.Manifest.permission#BIND_DEVICE_ADMIN](../android/Manifest.permission.md) to ensure that only the system can send updates.

Admins shouldn't implement [onReceive](../android/app/admin/PolicyUpdateReceiver.md) and should instead implement [onPolicyChanged](../android/app/admin/PolicyUpdateReceiver.md)). 

 Value: "android.app.admin.action.DEVICE_POLICY_CHANGED"

### ACTION_DEVICE_POLICY_SET_RESULT

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACTION_DEVICE_POLICY_SET_RESULT: String
```

Action for a broadcast sent to admins to communicate back the result of setting a policy in [DevicePolicyManager](../android/app/admin/DevicePolicyManager.md).

Admins wishing to receive these updates (via [onPolicySetResult](../android/app/admin/PolicyUpdateReceiver.md))) should include this action in the intent filter for their receiver in the manifest, the receiver must be protected by [android.Manifest.permission#BIND_DEVICE_ADMIN](../android/Manifest.permission.md) to ensure that only the system can send updates.

Admins shouldn't implement [onReceive](../android/app/admin/PolicyUpdateReceiver.md) and should instead implement [onPolicySetResult](../android/app/admin/PolicyUpdateReceiver.md)). 

 Value: "android.app.admin.action.DEVICE_POLICY_SET_RESULT"

### EXTRA_ACCOUNT_TYPE

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_ACCOUNT_TYPE: String
```

A string extra holding the account type this policy applies to, (see [PolicyUpdateReceiver.onPolicyChanged](../android/app/admin/PolicyUpdateReceiver.md))and [PolicyUpdateReceiver.onPolicySetResult](../android/app/admin/PolicyUpdateReceiver.md))) 

 Value: "android.app.admin.extra.ACCOUNT_TYPE"

### EXTRA_INTENT_FILTER

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_INTENT_FILTER: String
```

An [android.content.IntentFilter](../android/content/IntentFilter.md) extra holding the intent filter the policy relates to, (see [PolicyUpdateReceiver.onPolicyChanged](../android/app/admin/PolicyUpdateReceiver.md))and [PolicyUpdateReceiver.onPolicySetResult](../android/app/admin/PolicyUpdateReceiver.md))) 

 Value: "android.app.admin.extra.INTENT_FILTER"

### EXTRA_PACKAGE_NAME

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_PACKAGE_NAME: String
```

A string extra holding the package name the policy applies to, (see [PolicyUpdateReceiver.onPolicyChanged](../android/app/admin/PolicyUpdateReceiver.md))and [PolicyUpdateReceiver.onPolicySetResult](../android/app/admin/PolicyUpdateReceiver.md))) 

 Value: "android.app.admin.extra.PACKAGE_NAME"

### EXTRA_PERMISSION_NAME

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_PERMISSION_NAME: String
```

A string extra holding the permission name the policy applies to, (see [PolicyUpdateReceiver.onPolicyChanged](../android/app/admin/PolicyUpdateReceiver.md))and [PolicyUpdateReceiver.onPolicySetResult](../android/app/admin/PolicyUpdateReceiver.md))) 

 Value: "android.app.admin.extra.PERMISSION_NAME"

## Public constructors

### PolicyUpdateReceiver

```
PolicyUpdateReceiver()
```

## Public methods

### onPolicyChanged

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onPolicyChanged(
    context: Context, 
    policyIdentifier: String, 
    additionalPolicyParams: Bundle, 
    targetUser: TargetUser, 
    policyUpdateResult: PolicyUpdateResult
): Unit
```

Callback triggered when a policy previously set by the admin has changed.

Admins wishing to receive this callback should include [PolicyUpdateReceiver.ACTION_DEVICE_POLICY_CHANGED](../android/app/admin/PolicyUpdateReceiver.md) in the intent filter for their receiver in the manifest, the receiver must be protected by [android.Manifest.permission#BIND_DEVICE_ADMIN](../android/Manifest.permission.md) to ensure that only the system can send updates.

| Parameters ||
|--------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android/content/Context.md):the running context as per [onReceive](../android/app/admin/PolicyUpdateReceiver.md) This value cannot be`null`. |
| `policyIdentifier` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):Key to identify which policy this callback relates to. This value cannot be`null`. |
| `additionalPolicyParams` | [Bundle](../android/os/Bundle.md):Bundle containing additional params that may be required to identify some of the policy (e.g. [PolicyUpdateReceiver.EXTRA_PACKAGE_NAME](../android/app/admin/PolicyUpdateReceiver.md) and [PolicyUpdateReceiver.EXTRA_PERMISSION_NAME](../android/app/admin/PolicyUpdateReceiver.md)). Each policy will document the required additional params if needed. This value cannot be`null`. |
| --- | --- |
| `targetUser` | [TargetUser](../android/app/admin/TargetUser.md):The [TargetUser](../android/app/admin/TargetUser.md) which this policy relates to. This value cannot be`null`. |
| `policyUpdateResult` | [PolicyUpdateResult](../android/app/admin/PolicyUpdateResult.md):Indicates the reason the policy value has changed (e.g. [PolicyUpdateResult.RESULT_POLICY_SET](../android/app/admin/PolicyUpdateResult.md) if the policy has changed to the value set by the admin, [PolicyUpdateResult.RESULT_FAILURE_CONFLICTING_ADMIN_POLICY](../android/app/admin/PolicyUpdateResult.md) if the policy has changed because another admin has set a conflicting policy, etc) This value cannot be`null`. |

### onPolicySetResult

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onPolicySetResult(
    context: Context, 
    policyIdentifier: String, 
    additionalPolicyParams: Bundle, 
    targetUser: TargetUser, 
    policyUpdateResult: PolicyUpdateResult
): Unit
```

Callback triggered after an admin has set a policy using one of the APIs in [DevicePolicyManager](../android/app/admin/DevicePolicyManager.md) to notify the admin whether it has been successful or not.

Admins wishing to receive this callback should include [PolicyUpdateReceiver.ACTION_DEVICE_POLICY_SET_RESULT](../android/app/admin/PolicyUpdateReceiver.md) in the intent filter for their receiver in the manifest, the receiver must be protected by [android.Manifest.permission#BIND_DEVICE_ADMIN](../android/Manifest.permission.md) to ensure that only the system can send updates.

| Parameters ||
|--------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android/content/Context.md):the running context as per [onReceive](../android/app/admin/PolicyUpdateReceiver.md) This value cannot be`null`. |
| `policyIdentifier` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):Key to identify which policy this callback relates to. This value cannot be`null`. |
| `additionalPolicyParams` | [Bundle](../android/os/Bundle.md):Bundle containing additional params that may be required to identify some of the policy (e.g. [PolicyUpdateReceiver.EXTRA_PACKAGE_NAME](../android/app/admin/PolicyUpdateReceiver.md) and [PolicyUpdateReceiver.EXTRA_PERMISSION_NAME](../android/app/admin/PolicyUpdateReceiver.md)). Each policy will document the required additional params if needed. This value cannot be`null`. |
| --- | --- |
| `targetUser` | [TargetUser](../android/app/admin/TargetUser.md):The [TargetUser](../android/app/admin/TargetUser.md) which this policy relates to. This value cannot be`null`. |
| `policyUpdateResult` | [PolicyUpdateResult](../android/app/admin/PolicyUpdateResult.md):Indicates whether the policy has been set successfully ([PolicyUpdateResult.RESULT_POLICY_SET](../android/app/admin/PolicyUpdateResult.md)) or the reason it failed to apply (e.g. [PolicyUpdateResult.RESULT_FAILURE_CONFLICTING_ADMIN_POLICY](../android/app/admin/PolicyUpdateResult.md), etc). This value cannot be`null`. |
