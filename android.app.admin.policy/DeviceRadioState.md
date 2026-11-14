Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DeviceRadioState

```
open class DeviceRadioState
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.app.admin.policy.DeviceRadioState](https://developer.android.com/reference/kotlin/android/app/admin/policy/DeviceRadioState#) |

Controls for device radio settings.

## Summary

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/admin/policy/DeviceRadioState#MANAGED_ESIM_OUTGOING_TRANSFER_ALLOWED:kotlin.Int` Specifies that the user is allowed to transfer managed eSIMs from the device. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/admin/policy/DeviceRadioState#MANAGED_ESIM_OUTGOING_TRANSFER_DISALLOWED:kotlin.Int` Specifies that the user is not allowed to transfer managed eSIMs from the device. |

| Properties ||
|---|---|
| static [PolicyIdentifier](https://developer.android.com/reference/kotlin/android/app/admin/PolicyIdentifier.html#)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\> | `https://developer.android.com/reference/kotlin/android/app/admin/policy/DeviceRadioState#MANAGED_ESIM_OUTGOING_TRANSFER:android.app.admin.PolicyIdentifier` Policy that controls whether outgoing transfer is allowed for managed embedded subscriptions. |

## Constants

### MANAGED_ESIM_OUTGOING_TRANSFER_ALLOWED

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MANAGED_ESIM_OUTGOING_TRANSFER_ALLOWED: Int
```

Specifies that the user is allowed to transfer managed eSIMs from the device.

 Value: 1

### MANAGED_ESIM_OUTGOING_TRANSFER_DISALLOWED

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MANAGED_ESIM_OUTGOING_TRANSFER_DISALLOWED: Int
```

Specifies that the user is not allowed to transfer managed eSIMs from the device.

 Value: 2

## Properties

### MANAGED_ESIM_OUTGOING_TRANSFER

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MANAGED_ESIM_OUTGOING_TRANSFER: PolicyIdentifier<Int!>
```

Policy that controls whether outgoing transfer is allowed for managed embedded subscriptions. 

| Policy details ||
|---|---|
| Settable by | This policy can be set with scope `Device` by anyone holding `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MANAGE_DEVICE_POLICY_MANAGED_SUBSCRIPTIONS:kotlin.String`, or the following DPC types: - Device Owner - Managed Profile Owner (Of Organization Owned Device) - Managed Profile Owner (Of Personally Owned Device) - Unaffiliated Full User Profile Owner - Profile Owner on User 0 - Affiliated Full User Profile Owner <br /> |
| Resources affected | This policy takes effect device-wide, so it affects all users. |
| Conflict resolution mechanism | If this policy is set by multiple admins, `https://developer.android.com/reference/kotlin/android/app/admin/policy/DeviceRadioState#MANAGED_ESIM_OUTGOING_TRANSFER_DISALLOWED:kotlin.Int` takes effect if it is set by any admin. |
| --- | --- |
| Policy value | `Integer`, value is one of the following: - `https://developer.android.com/reference/kotlin/android/app/admin/policy/DeviceRadioState#MANAGED_ESIM_OUTGOING_TRANSFER_ALLOWED:kotlin.Int` (default) - `https://developer.android.com/reference/kotlin/android/app/admin/policy/DeviceRadioState#MANAGED_ESIM_OUTGOING_TRANSFER_DISALLOWED:kotlin.Int` |

See also: `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#setPolicy(android.app.admin.PolicyIdentifier,%20kotlin.Int,%20android.app.admin.DevicePolicyManager.setPolicy.T)`, `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#getPolicy(android.app.admin.PolicyIdentifier,%20kotlin.Int)`

<br />
