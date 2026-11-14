Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SystemUpdatePolicy

```
class SystemUpdatePolicy : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.app.admin.SystemUpdatePolicy](https://developer.android.com/reference/kotlin/android/app/admin/SystemUpdatePolicy#) |

Determines when over-the-air system updates are installed on a device. Only a device policy controller (DPC) running in device owner mode or in profile owner mode for an organization-owned device can set an update policy for the device by calling the `DevicePolicyManager` method `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager#setSystemUpdatePolicy(android.content.ComponentName,%20android.app.admin.SystemUpdatePolicy)`. An update policy affects the pending system update (if there is one) and any future updates for the device.

If a policy is set on a device, the system doesn't notify the user about updates.

### Example

The example below shows how a DPC might set a maintenance window for system updates:

```kotlin
<code>
  private final MAINTENANCE_WINDOW_START = 1380; // 11pm
  private final MAINTENANCE_WINDOW_END = 120; // 2am
 
  // ...
 
  // Create the system update policy
  SystemUpdatePolicy policy = SystemUpdatePolicy.createWindowedInstallPolicy(
      MAINTENANCE_WINDOW_START, MAINTENANCE_WINDOW_END);
 
  // Get a DevicePolicyManager instance to set the policy on the device
  DevicePolicyManager dpm =
      (DevicePolicyManager) context.getSystemService(Context.DEVICE_POLICY_SERVICE);
  ComponentName adminComponent = getComponentName(context);
  dpm.setSystemUpdatePolicy(adminComponent, policy);
  </code>
```

### Developer guide

To learn more, read [Manage system updates](https://developer.android.com/work/dpc/system-updates).

**Note:** [Google Play system updates](https://source.android.com/docs/core/ota/modular-system) (also called Mainline updates) are automatically downloaded but require a device reboot to be installed. Refer to the mainline section in [Manage system updates](https://developer.android.com/work/dpc/system-updates#mainline) for further details.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/app/admin/SystemUpdatePolicy.ValidationFailedException` An exception class that represents various validation errors thrown from `https://developer.android.com/reference/kotlin/android/app/admin/SystemUpdatePolicy#setFreezePeriods(kotlin.collections.MutableList)` and `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager#setSystemUpdatePolicy(android.content.ComponentName,%20android.app.admin.SystemUpdatePolicy)` |

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/admin/SystemUpdatePolicy#TYPE_INSTALL_AUTOMATIC:kotlin.Int` Installs system updates (without user interaction) as soon as they become available. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/admin/SystemUpdatePolicy#TYPE_INSTALL_WINDOWED:kotlin.Int` Installs system updates (without user interaction) during a daily maintenance window. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/admin/SystemUpdatePolicy#TYPE_POSTPONE:kotlin.Int` Postpones the installation of system updates for 30 days. |
| --- | --- |

Inherited constants From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int`

Descriptor bit used with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()`: indicates that the Parcelable object's flattened representation includes a file descriptor.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`

Flag for use with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point.

<br />

| Public methods ||
|---|---|
| static [SystemUpdatePolicy](https://developer.android.com/reference/kotlin/android/app/admin/SystemUpdatePolicy#)! | `https://developer.android.com/reference/kotlin/android/app/admin/SystemUpdatePolicy#createAutomaticInstallPolicy()()` Create a policy object and set it to install update automatically as soon as one is available. |
| static [SystemUpdatePolicy](https://developer.android.com/reference/kotlin/android/app/admin/SystemUpdatePolicy#)! | `https://developer.android.com/reference/kotlin/android/app/admin/SystemUpdatePolicy#createPostponeInstallPolicy()()` Create a policy object and set it to block installation for a maximum period of 30 days. |
| static [SystemUpdatePolicy](https://developer.android.com/reference/kotlin/android/app/admin/SystemUpdatePolicy#)! | `https://developer.android.com/reference/kotlin/android/app/admin/SystemUpdatePolicy#createWindowedInstallPolicy(kotlin.Int,%20kotlin.Int)(startTime: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, endTime: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Create a policy object and set it to: new system update will only be installed automatically when the system clock is inside a daily maintenance window. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/admin/SystemUpdatePolicy#describeContents()()` Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [FreezePeriod](https://developer.android.com/reference/kotlin/android/app/admin/FreezePeriod)!\>! | `https://developer.android.com/reference/kotlin/android/app/admin/SystemUpdatePolicy#getFreezePeriods()()` Returns the list of freeze periods previously set on this system update policy object. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/admin/SystemUpdatePolicy#getInstallWindowEnd()()` Get the end of the maintenance window. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/admin/SystemUpdatePolicy#getInstallWindowStart()()` Get the start of the maintenance window. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/admin/SystemUpdatePolicy#getPolicyType()()` Returns the type of system update policy, or -1 if no policy has been set. |
| [SystemUpdatePolicy](https://developer.android.com/reference/kotlin/android/app/admin/SystemUpdatePolicy#)! | `https://developer.android.com/reference/kotlin/android/app/admin/SystemUpdatePolicy#setFreezePeriods(kotlin.collections.MutableList)(freezePeriods: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/app/admin/FreezePeriod!>!)` Configure a list of freeze periods on top of the current policy. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/admin/SystemUpdatePolicy#toString()()` Returns a string representation of the object. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/admin/SystemUpdatePolicy#writeToParcel(android.os.Parcel,%20kotlin.Int)(dest: https://developer.android.com/reference/kotlin/android/os/Parcel.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Flatten this object in to a Parcel. |

| Properties ||
|---|---|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [SystemUpdatePolicy](https://developer.android.com/reference/kotlin/android/app/admin/SystemUpdatePolicy#)!\> | `https://developer.android.com/reference/kotlin/android/app/admin/SystemUpdatePolicy#CREATOR:android.os.Parcelable.Creator` <br /> |

## Constants

### TYPE_INSTALL_AUTOMATIC

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_INSTALL_AUTOMATIC: Int
```

Installs system updates (without user interaction) as soon as they become available. Setting this policy type immediately installs any pending updates that might be postponed or waiting for a maintenance window.

 Value: 1

### TYPE_INSTALL_WINDOWED

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_INSTALL_WINDOWED: Int
```

Installs system updates (without user interaction) during a daily maintenance window. Set the start and end of the daily maintenance window, as minutes of the day, when creating a new `TYPE_INSTALL_WINDOWED` policy. See `https://developer.android.com/reference/kotlin/android/app/admin/SystemUpdatePolicy#createWindowedInstallPolicy(kotlin.Int,%20kotlin.Int)`.

No connectivity, not enough disk space, or a low battery are typical reasons Android might not install a system update in the daily maintenance window. After 30 days trying to install an update in the maintenance window (regardless of policy changes in this period), the system prompts the device user to install the update.

 Value: 2

### TYPE_POSTPONE

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_POSTPONE: Int
```

Postpones the installation of system updates for 30 days. After the 30-day period has ended, the system prompts the device user to install the update.

The system limits each update to one 30-day postponement. The period begins when the system first postpones the update and setting new `TYPE_POSTPONE` policies won't extend the period. If, after 30 days the update isn't installed (through policy changes), the system prompts the user to install the update.

**Note**: Device manufacturers or carriers might choose to exempt important security updates from a postponement policy. Exempted updates notify the device user when they become available.

 Value: 3

## Public methods

### createAutomaticInstallPolicy

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun createAutomaticInstallPolicy(): SystemUpdatePolicy!
```

Create a policy object and set it to install update automatically as soon as one is available.
**See Also**

- `https://developer.android.com/reference/kotlin/android/app/admin/SystemUpdatePolicy#TYPE_INSTALL_AUTOMATIC:kotlin.Int`

### createPostponeInstallPolicy

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun createPostponeInstallPolicy(): SystemUpdatePolicy!
```

Create a policy object and set it to block installation for a maximum period of 30 days. To learn more about this policy's behavior, see `https://developer.android.com/reference/kotlin/android/app/admin/SystemUpdatePolicy#TYPE_POSTPONE:kotlin.Int`.

**Note:** security updates (e.g. monthly security patches) will *not* be affected by this policy.
**See Also**

- `https://developer.android.com/reference/kotlin/android/app/admin/SystemUpdatePolicy#TYPE_POSTPONE:kotlin.Int`

### createWindowedInstallPolicy

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun createWindowedInstallPolicy(
    startTime: Int, 
    endTime: Int
): SystemUpdatePolicy!
```

Create a policy object and set it to: new system update will only be installed automatically when the system clock is inside a daily maintenance window. If the start and end times are the same, the window is considered to include the *whole 24 hours* . That is, updates can install at any time. If start time is later than end time, the window is considered spanning midnight (i.e. the end time denotes a time on the next day). The maintenance window will last for 30 days for any given update, after which the window will no longer be effective and the pending update will be made available for manual installation as if no system update policy were set on the device. See `https://developer.android.com/reference/kotlin/android/app/admin/SystemUpdatePolicy#TYPE_INSTALL_WINDOWED:kotlin.Int` for the details of this policy's behavior.

| Parameters ||
|---|---|
| `startTime` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the start of the maintenance window, measured as the number of minutes from midnight in the device's local time. Must be in the range of \[0, 1440). |
| `endTime` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the end of the maintenance window, measured as the number of minutes from midnight in the device's local time. Must be in the range of \[0, 1440). |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/app/admin/SystemUpdatePolicy#!` | The configured policy. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | If the `startTime` or `endTime` isn't in the accepted range. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/admin/SystemUpdatePolicy#TYPE_INSTALL_WINDOWED:kotlin.Int`

### describeContents

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### getFreezePeriods

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getFreezePeriods(): MutableList<FreezePeriod!>!
```

Returns the list of freeze periods previously set on this system update policy object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/app/admin/FreezePeriod!>!` | the list of freeze periods, or an empty list if none was set. |

### getInstallWindowEnd

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getInstallWindowEnd(): Int
```

Get the end of the maintenance window.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the end of the maintenance window measured as the number of minutes from midnight, or -1 if the policy does not have a maintenance window. |

### getInstallWindowStart

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getInstallWindowStart(): Int
```

Get the start of the maintenance window.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the start of the maintenance window measured as the number of minutes from midnight, or -1 if the policy does not have a maintenance window. |

### getPolicyType

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getPolicyType(): Int
```

Returns the type of system update policy, or -1 if no policy has been set.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The policy type or -1 if the type isn't set. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/app/admin/SystemUpdatePolicy#TYPE_INSTALL_AUTOMATIC:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/admin/SystemUpdatePolicy#TYPE_INSTALL_WINDOWED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/admin/SystemUpdatePolicy#TYPE_POSTPONE:kotlin.Int` |

### setFreezePeriods

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setFreezePeriods(freezePeriods: MutableList<FreezePeriod!>!): SystemUpdatePolicy!
```

Configure a list of freeze periods on top of the current policy. When the device's clock is within any of the freeze periods, all incoming system updates including security patches will be blocked and cannot be installed. When the device is outside the freeze periods, the normal policy behavior will apply.

Each individual freeze period is allowed to be at most 90 days long, and adjacent freeze periods need to be at least 60 days apart. Also, the list of freeze periods should not contain duplicates or overlap with each other. If any of these conditions is not met, a `https://developer.android.com/reference/kotlin/android/app/admin/SystemUpdatePolicy.ValidationFailedException` will be thrown.

Handling of leap year: we ignore leap years in freeze period calculations, in particular,

- When a freeze period is defined, February 29th is disregarded so even though a freeze period can be specified to start or end on February 29th, it will be treated as if the period started or ended on February 28th.
- When applying freeze period behavior to the device, a system clock of February 29th is treated as if it were February 28th
- When calculating the number of days of a freeze period or separation between two freeze periods, February 29th is also ignored and not counted as one day.

| Parameters ||
|---|---|
| `freezePeriods` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [FreezePeriod](https://developer.android.com/reference/kotlin/android/app/admin/FreezePeriod)!\>!: the list of freeze periods |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/app/admin/SystemUpdatePolicy#!` | this instance |

| Exceptions ||
|---|---|
| `android.app.admin.SystemUpdatePolicy.ValidationFailedException` | if the supplied freeze periods do not meet the requirement set above |

### toString

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toString(): String
```

Returns a string representation of the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the object. |

### writeToParcel

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

Flatten this object in to a Parcel.

| Parameters ||
|---|---|
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#): The Parcel in which the object should be written. This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` |

## Properties

### CREATOR

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<SystemUpdatePolicy!>
```
