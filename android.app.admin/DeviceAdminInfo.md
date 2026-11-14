# DeviceAdminInfo

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DeviceAdminInfo

Kotlin| [Java](../android/app/admin/DeviceAdminInfo.md) 
| --- | --- |

```
class DeviceAdminInfo : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.app.admin.DeviceAdminInfo](../android/app/admin/DeviceAdminInfo.md) |

This class is used to specify meta information of a device administrator component.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [HEADLESS_DEVICE_OWNER_MODE_AFFILIATED](../android/app/admin/DeviceAdminInfo.md) Value for [getHeadlessDeviceOwnerMode](../android/app/admin/DeviceAdminInfo.md))which indicates that this DPC should be provisioned into "affiliated" mode when on a Headless System User Mode device. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [HEADLESS_DEVICE_OWNER_MODE_SINGLE_USER](../android/app/admin/DeviceAdminInfo.md) Value for [getHeadlessDeviceOwnerMode](../android/app/admin/DeviceAdminInfo.md))which indicates that this DPC should be provisioned into the first secondary user when on a Headless System User Mode device. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [HEADLESS_DEVICE_OWNER_MODE_UNSUPPORTED](../android/app/admin/DeviceAdminInfo.md) Value for [getHeadlessDeviceOwnerMode](../android/app/admin/DeviceAdminInfo.md))which indicates that this DPC should not be provisioned into Device Owner mode on a Headless System User Mode device. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [USES_ENCRYPTED_STORAGE](../android/app/admin/DeviceAdminInfo.md) A type of policy that this device admin can use: require encryption of stored data. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [USES_POLICY_DISABLE_CAMERA](../android/app/admin/DeviceAdminInfo.md) A type of policy that this device admin can use: disables use of all device cameras. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [USES_POLICY_DISABLE_KEYGUARD_FEATURES](../android/app/admin/DeviceAdminInfo.md) A type of policy that this device admin can use: disables use of keyguard features. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [USES_POLICY_EXPIRE_PASSWORD](../android/app/admin/DeviceAdminInfo.md) A type of policy that this device admin can use: force the user to change their password after an administrator-defined time limit. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [USES_POLICY_FORCE_LOCK](../android/app/admin/DeviceAdminInfo.md) A type of policy that this device admin can use: able to force the device to lock viaandroid. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [USES_POLICY_LIMIT_PASSWORD](../android/app/admin/DeviceAdminInfo.md) A type of policy that this device admin can use: limit the passwords that the user can select, via [DevicePolicyManager.setPasswordQuality](../android/app/admin/DevicePolicyManager.md))and [DevicePolicyManager.setPasswordMinimumLength](../android/app/admin/DevicePolicyManager.md)). |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [USES_POLICY_RESET_PASSWORD](../android/app/admin/DeviceAdminInfo.md) A type of policy that this device admin can use: able to reset the user's password via [DevicePolicyManager.resetPassword](../android/app/admin/DevicePolicyManager.md)). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [USES_POLICY_WATCH_LOGIN](../android/app/admin/DeviceAdminInfo.md) A type of policy that this device admin can use: able to watch login attempts from the user, via [DeviceAdminReceiver.ACTION_PASSWORD_FAILED](../android/app/admin/DeviceAdminReceiver.md), [DeviceAdminReceiver.ACTION_PASSWORD_SUCCEEDED](../android/app/admin/DeviceAdminReceiver.md), and [DevicePolicyManager.getCurrentFailedPasswordAttempts](../android/app/admin/DevicePolicyManager.md)). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [USES_POLICY_WIPE_DATA](../android/app/admin/DeviceAdminInfo.md) A type of policy that this device admin can use: able to factory reset the device, erasing all of the user's data, via android. |
| --- | --- |

| Inherited constants ||
|---|---|
| From class [Parcelable](../android/os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android/os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android/os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [DeviceAdminInfo](../android/app/admin/DeviceAdminInfo.md))`(`context:` ` [Context](../android/content/Context.md)!`, `resolveInfo:` ` [ResolveInfo](../android/content/pm/ResolveInfo.md)!`)` Constructor. |

| Public methods ||
|-------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](../android/app/admin/DeviceAdminInfo.md))`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [dump](../android/app/admin/DeviceAdminInfo.md))`(`pw:` ` [Printer](../android/util/Printer.md)!`, `prefix:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |
| [ActivityInfo](../android/content/pm/ActivityInfo.md)! | [getActivityInfo](../android/app/admin/DeviceAdminInfo.md))`()` Return the raw information about the receiver implementing this device admin. |
| --- | --- |
| [ComponentName](../android/content/ComponentName.md) | [getComponent](../android/app/admin/DeviceAdminInfo.md))`()` Return the component of the receiver that implements this device admin. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getHeadlessDeviceOwnerMode](../android/app/admin/DeviceAdminInfo.md))`()` Returns the mode this DeviceAdmin wishes to use if provisioned as a Device Owner on a headless system user mode device. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getPackageName](../android/app/admin/DeviceAdminInfo.md))`()` Return the . |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getReceiverName](../android/app/admin/DeviceAdminInfo.md))`()` Return the class name of the receiver component that implements this device admin. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getTagForPolicy](../android/app/admin/DeviceAdminInfo.md))`(`policyIdent:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return the XML tag name for the given policy identifier. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isVisible](../android/app/admin/DeviceAdminInfo.md))`()` Returns whether this device admin would like to be visible to the user, even when it is not enabled. |
| --- | --- |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | [loadDescription](../android/app/admin/DeviceAdminInfo.md))`(`pm:` ` [PackageManager](../android/content/pm/PackageManager.md)!`)` Load user-visible description associated with this device admin. |
| [Drawable](../android/graphics/drawable/Drawable.md)! | [loadIcon](../android/app/admin/DeviceAdminInfo.md))`(`pm:` ` [PackageManager](../android/content/pm/PackageManager.md)!`)` Load the user-displayed icon for this device admin. |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | [loadLabel](../android/app/admin/DeviceAdminInfo.md))`(`pm:` ` [PackageManager](../android/content/pm/PackageManager.md)!`)` Load the user-displayed label for this device admin. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [supportsTransferOwnership](../android/app/admin/DeviceAdminInfo.md))`()` Return true if this administrator can be a target in an ownership transfer. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../android/app/admin/DeviceAdminInfo.md))`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [usesPolicy](../android/app/admin/DeviceAdminInfo.md))`(`policyIdent:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return true if the device admin has requested that it be able to use the given policy control. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](../android/app/admin/DeviceAdminInfo.md))`(`dest:` ` [Parcel](../android/os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Used to package this object into a [Parcel](../android/os/Parcel.md). |

| Properties ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [DeviceAdminInfo](../android/app/admin/DeviceAdminInfo.md)!\> | [CREATOR](../android/app/admin/DeviceAdminInfo.md) Used to make this class parcelable. |

## Constants

### HEADLESS_DEVICE_OWNER_MODE_AFFILIATED

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val HEADLESS_DEVICE_OWNER_MODE_AFFILIATED: Int
```

Value for [getHeadlessDeviceOwnerMode](../android/app/admin/DeviceAdminInfo.md))which indicates that this DPC should be provisioned into "affiliated" mode when on a Headless System User Mode device.

This mode adds a Profile Owner to all users other than the user the Device Owner is on.

Starting from Android version [android.os.Build.VERSION_CODES#VANILLA_ICE_CREAM](../android/os/Build.VERSION_CODES.md), DPCs should set the value of attribute "headless-device-owner-mode" inside the "headless-system-user" tag as "affiliated". 

 Value: 1

### HEADLESS_DEVICE_OWNER_MODE_SINGLE_USER

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val HEADLESS_DEVICE_OWNER_MODE_SINGLE_USER: Int
```

Value for [getHeadlessDeviceOwnerMode](../android/app/admin/DeviceAdminInfo.md))which indicates that this DPC should be provisioned into the first secondary user when on a Headless System User Mode device.

This mode only allows a single secondary user on the device blocking the creation of additional secondary users.

Starting from Android version [android.os.Build.VERSION_CODES#VANILLA_ICE_CREAM](../android/os/Build.VERSION_CODES.md), DPCs should set the value of attribute "headless-device-owner-mode" inside the "headless-system-user" tag as "single_user". 

 Value: 2

### HEADLESS_DEVICE_OWNER_MODE_UNSUPPORTED

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val HEADLESS_DEVICE_OWNER_MODE_UNSUPPORTED: Int
```

Value for [getHeadlessDeviceOwnerMode](../android/app/admin/DeviceAdminInfo.md))which indicates that this DPC should not be provisioned into Device Owner mode on a Headless System User Mode device. 

 Value: 0

### USES_ENCRYPTED_STORAGE

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val USES_ENCRYPTED_STORAGE: Int
```

A type of policy that this device admin can use: require encryption of stored data.

To control this policy, the device admin must have a "encrypted-storage" tag in the "uses-policies" section of its meta-data. 

 Value: 7

### USES_POLICY_DISABLE_CAMERA

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val USES_POLICY_DISABLE_CAMERA: Int
```

A type of policy that this device admin can use: disables use of all device cameras.

To control this policy, the device admin must be a device owner or profile owner, and must have a "disable-camera" tag in the "uses-policies" section of its meta-data. If used by a device owner, the policy affects all users on the device. 

 Value: 8

### USES_POLICY_DISABLE_KEYGUARD_FEATURES

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val USES_POLICY_DISABLE_KEYGUARD_FEATURES: Int
```

A type of policy that this device admin can use: disables use of keyguard features.

To control this policy, the device admin must be a device owner or profile owner, and must have a "disable-keyguard-features" tag in the "uses-policies" section of its meta-data. If used by a device owner, the policy only affects the primary user and its profiles, but not any secondary users on the device. 

 Value: 9

### USES_POLICY_EXPIRE_PASSWORD

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val USES_POLICY_EXPIRE_PASSWORD: Int
```

A type of policy that this device admin can use: force the user to change their password after an administrator-defined time limit.

To control this policy, the device admin must be a device owner or profile owner, and must have an "expire-password" tag in the "uses-policies" section of its meta-data. If used by a device owner, the policy only affects the primary user and its profiles, but not any secondary users on the device. 

 Value: 6

### USES_POLICY_FORCE_LOCK

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val USES_POLICY_FORCE_LOCK: Int
```

A type of policy that this device admin can use: able to force the device to lock viaandroid.app.admin.DevicePolicyManager#lockNow or limit the maximum lock timeout for the device via [DevicePolicyManager.setMaximumTimeToLock](../android/app/admin/DevicePolicyManager.md)).

To control this policy, the device admin must have a "force-lock" tag in the "uses-policies" section of its meta-data. 

 Value: 3

### USES_POLICY_LIMIT_PASSWORD

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val USES_POLICY_LIMIT_PASSWORD: Int
```

A type of policy that this device admin can use: limit the passwords that the user can select, via [DevicePolicyManager.setPasswordQuality](../android/app/admin/DevicePolicyManager.md))and [DevicePolicyManager.setPasswordMinimumLength](../android/app/admin/DevicePolicyManager.md)).

To control this policy, the device admin must be a device owner or profile owner, and must have a "limit-password" tag in the "uses-policies" section of its meta-data. If used by a device owner, the policy only affects the primary user and its profiles, but not any secondary users on the device. 

 Value: 0

### USES_POLICY_RESET_PASSWORD

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val USES_POLICY_RESET_PASSWORD: Int
```

A type of policy that this device admin can use: able to reset the user's password via [DevicePolicyManager.resetPassword](../android/app/admin/DevicePolicyManager.md)).

To control this policy, the device admin must have a "reset-password" tag in the "uses-policies" section of its meta-data. 

 Value: 2

### USES_POLICY_WATCH_LOGIN

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val USES_POLICY_WATCH_LOGIN: Int
```

A type of policy that this device admin can use: able to watch login attempts from the user, via [DeviceAdminReceiver.ACTION_PASSWORD_FAILED](../android/app/admin/DeviceAdminReceiver.md), [DeviceAdminReceiver.ACTION_PASSWORD_SUCCEEDED](../android/app/admin/DeviceAdminReceiver.md), and [DevicePolicyManager.getCurrentFailedPasswordAttempts](../android/app/admin/DevicePolicyManager.md)).

To control this policy, the device admin must have a "watch-login" tag in the "uses-policies" section of its meta-data. 

 Value: 1

### USES_POLICY_WIPE_DATA

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val USES_POLICY_WIPE_DATA: Int
```

A type of policy that this device admin can use: able to factory reset the device, erasing all of the user's data, via android.app.admin.DevicePolicyManager#wipeData.

To control this policy, the device admin must have a "wipe-data" tag in the "uses-policies" section of its meta-data. 

 Value: 4

## Public constructors

### DeviceAdminInfo

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
DeviceAdminInfo(
    context: Context!, 
    resolveInfo: ResolveInfo!)
```

Constructor.

| Parameters ||
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android/content/Context.md)!:The Context in which we are parsing the device admin. |
| `resolveInfo` | [ResolveInfo](../android/content/pm/ResolveInfo.md)!:The ResolveInfo returned from the package manager about this device admin's component. |

## Public methods

### describeContents

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) |

### dump

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun dump(
    pw: Printer!, 
    prefix: String!
): Unit
```  

### getActivityInfo

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getActivityInfo(): ActivityInfo!
```

Return the raw information about the receiver implementing this device admin. Do not modify the returned object. 

### getComponent

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getComponent(): ComponentName
```

Return the component of the receiver that implements this device admin.

| Return ||
|-----------------------------------------------------------------------------------------------------|-----------------------------|
| [ComponentName](../android/content/ComponentName.md) | This value cannot be`null`. |

### getHeadlessDeviceOwnerMode

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getHeadlessDeviceOwnerMode(): Int
```

Returns the mode this DeviceAdmin wishes to use if provisioned as a Device Owner on a headless system user mode device.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.app.admin.DeviceAdminInfo#HEADLESS_DEVICE_OWNER_MODE_UNSUPPORTED](../android/app/admin/DeviceAdminInfo.md), [android.app.admin.DeviceAdminInfo#HEADLESS_DEVICE_OWNER_MODE_AFFILIATED](../android/app/admin/DeviceAdminInfo.md), or [android.app.admin.DeviceAdminInfo#HEADLESS_DEVICE_OWNER_MODE_SINGLE_USER](../android/app/admin/DeviceAdminInfo.md) |

### getPackageName

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPackageName(): String!
```

Return the .apk package that implements this device admin. 

### getReceiverName

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getReceiverName(): String!
```

Return the class name of the receiver component that implements this device admin. 

### getTagForPolicy

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTagForPolicy(policyIdent: Int): String!
```

Return the XML tag name for the given policy identifier. Valid identifiers are as per [usesPolicy(int)](../android/app/admin/DeviceAdminInfo.md)). If the given identifier is not known, null is returned. 

### isVisible

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isVisible(): Boolean
```

Returns whether this device admin would like to be visible to the user, even when it is not enabled. 

### loadDescription

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun loadDescription(pm: PackageManager!): CharSequence!
```

Load user-visible description associated with this device admin.

| Parameters ||
|------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `pm` | [PackageManager](../android/content/pm/PackageManager.md)!:Supply a PackageManager used to load the device admin's resources. |

### loadIcon

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun loadIcon(pm: PackageManager!): Drawable!
```

Load the user-displayed icon for this device admin.

| Parameters ||
|------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `pm` | [PackageManager](../android/content/pm/PackageManager.md)!:Supply a PackageManager used to load the device admin's resources. |

### loadLabel

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun loadLabel(pm: PackageManager!): CharSequence!
```

Load the user-displayed label for this device admin.

| Parameters ||
|------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `pm` | [PackageManager](../android/content/pm/PackageManager.md)!:Supply a PackageManager used to load the device admin's resources. |

### supportsTransferOwnership

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun supportsTransferOwnership(): Boolean
```

Return true if this administrator can be a target in an ownership transfer. 

### toString

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

### usesPolicy

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun usesPolicy(policyIdent: Int): Boolean
```

Return true if the device admin has requested that it be able to use the given policy control. The possible policy identifier inputs are: [USES_POLICY_LIMIT_PASSWORD](../android/app/admin/DeviceAdminInfo.md), [USES_POLICY_WATCH_LOGIN](../android/app/admin/DeviceAdminInfo.md), [USES_POLICY_RESET_PASSWORD](../android/app/admin/DeviceAdminInfo.md), [USES_POLICY_FORCE_LOCK](../android/app/admin/DeviceAdminInfo.md), [USES_POLICY_WIPE_DATA](../android/app/admin/DeviceAdminInfo.md), [USES_POLICY_EXPIRE_PASSWORD](../android/app/admin/DeviceAdminInfo.md), [USES_ENCRYPTED_STORAGE](../android/app/admin/DeviceAdminInfo.md), [USES_POLICY_DISABLE_CAMERA](../android/app/admin/DeviceAdminInfo.md). 

### writeToParcel

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

Used to package this object into a [Parcel](../android/os/Parcel.md).

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Parcel](../android/os/Parcel.md):The [Parcel](../android/os/Parcel.md) to be written. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The flags used for parceling. |

## Properties

### CREATOR

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<DeviceAdminInfo!>
```

Used to make this class parcelable.
