# DeviceAdminInfo

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DeviceAdminInfo

Kotlin| [Java](https://developer.android.com/reference/android/app/admin/DeviceAdminInfo "View this page in Java") 
| --- | --- |

```
class DeviceAdminInfo : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.app.admin.DeviceAdminInfo](https://developer.android.com/reference/kotlin/android/app/admin/DeviceAdminInfo#) |

This class is used to specify meta information of a device administrator component.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [HEADLESS_DEVICE_OWNER_MODE_AFFILIATED](https://developer.android.com/reference/kotlin/android/app/admin/DeviceAdminInfo#HEADLESS_DEVICE_OWNER_MODE_AFFILIATED:kotlin.Int) Value for [getHeadlessDeviceOwnerMode](https://developer.android.com/reference/kotlin/android/app/admin/DeviceAdminInfo#getHeadlessDeviceOwnerMode())which indicates that this DPC should be provisioned into "affiliated" mode when on a Headless System User Mode device. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [HEADLESS_DEVICE_OWNER_MODE_SINGLE_USER](https://developer.android.com/reference/kotlin/android/app/admin/DeviceAdminInfo#HEADLESS_DEVICE_OWNER_MODE_SINGLE_USER:kotlin.Int) Value for [getHeadlessDeviceOwnerMode](https://developer.android.com/reference/kotlin/android/app/admin/DeviceAdminInfo#getHeadlessDeviceOwnerMode())which indicates that this DPC should be provisioned into the first secondary user when on a Headless System User Mode device. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [HEADLESS_DEVICE_OWNER_MODE_UNSUPPORTED](https://developer.android.com/reference/kotlin/android/app/admin/DeviceAdminInfo#HEADLESS_DEVICE_OWNER_MODE_UNSUPPORTED:kotlin.Int) Value for [getHeadlessDeviceOwnerMode](https://developer.android.com/reference/kotlin/android/app/admin/DeviceAdminInfo#getHeadlessDeviceOwnerMode())which indicates that this DPC should not be provisioned into Device Owner mode on a Headless System User Mode device. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [USES_ENCRYPTED_STORAGE](https://developer.android.com/reference/kotlin/android/app/admin/DeviceAdminInfo#USES_ENCRYPTED_STORAGE:kotlin.Int) A type of policy that this device admin can use: require encryption of stored data. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [USES_POLICY_DISABLE_CAMERA](https://developer.android.com/reference/kotlin/android/app/admin/DeviceAdminInfo#USES_POLICY_DISABLE_CAMERA:kotlin.Int) A type of policy that this device admin can use: disables use of all device cameras. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [USES_POLICY_DISABLE_KEYGUARD_FEATURES](https://developer.android.com/reference/kotlin/android/app/admin/DeviceAdminInfo#USES_POLICY_DISABLE_KEYGUARD_FEATURES:kotlin.Int) A type of policy that this device admin can use: disables use of keyguard features. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [USES_POLICY_EXPIRE_PASSWORD](https://developer.android.com/reference/kotlin/android/app/admin/DeviceAdminInfo#USES_POLICY_EXPIRE_PASSWORD:kotlin.Int) A type of policy that this device admin can use: force the user to change their password after an administrator-defined time limit. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [USES_POLICY_FORCE_LOCK](https://developer.android.com/reference/kotlin/android/app/admin/DeviceAdminInfo#USES_POLICY_FORCE_LOCK:kotlin.Int) A type of policy that this device admin can use: able to force the device to lock viaandroid. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [USES_POLICY_LIMIT_PASSWORD](https://developer.android.com/reference/kotlin/android/app/admin/DeviceAdminInfo#USES_POLICY_LIMIT_PASSWORD:kotlin.Int) A type of policy that this device admin can use: limit the passwords that the user can select, via [DevicePolicyManager.setPasswordQuality](https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager#setPasswordQuality(android.content.ComponentName,%20kotlin.Int))and [DevicePolicyManager.setPasswordMinimumLength](https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager#setPasswordMinimumLength(android.content.ComponentName,%20kotlin.Int)). |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [USES_POLICY_RESET_PASSWORD](https://developer.android.com/reference/kotlin/android/app/admin/DeviceAdminInfo#USES_POLICY_RESET_PASSWORD:kotlin.Int) A type of policy that this device admin can use: able to reset the user's password via [DevicePolicyManager.resetPassword](https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager#resetPassword(kotlin.String,%20kotlin.Int)). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [USES_POLICY_WATCH_LOGIN](https://developer.android.com/reference/kotlin/android/app/admin/DeviceAdminInfo#USES_POLICY_WATCH_LOGIN:kotlin.Int) A type of policy that this device admin can use: able to watch login attempts from the user, via [DeviceAdminReceiver.ACTION_PASSWORD_FAILED](https://developer.android.com/reference/kotlin/android/app/admin/DeviceAdminReceiver#ACTION_PASSWORD_FAILED:kotlin.String), [DeviceAdminReceiver.ACTION_PASSWORD_SUCCEEDED](https://developer.android.com/reference/kotlin/android/app/admin/DeviceAdminReceiver#ACTION_PASSWORD_SUCCEEDED:kotlin.String), and [DevicePolicyManager.getCurrentFailedPasswordAttempts](https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager#getCurrentFailedPasswordAttempts()). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [USES_POLICY_WIPE_DATA](https://developer.android.com/reference/kotlin/android/app/admin/DeviceAdminInfo#USES_POLICY_WIPE_DATA:kotlin.Int) A type of policy that this device admin can use: able to factory reset the device, erasing all of the user's data, via android. |
| --- | --- |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [DeviceAdminInfo](https://developer.android.com/reference/kotlin/android/app/admin/DeviceAdminInfo#DeviceAdminInfo(android.content.Context,%20android.content.pm.ResolveInfo))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`, `resolveInfo:` ` [ResolveInfo](https://developer.android.com/reference/kotlin/android/content/pm/ResolveInfo.html#)!`)` Constructor. |

| Public methods ||
|-------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/app/admin/DeviceAdminInfo#describeContents())`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [dump](https://developer.android.com/reference/kotlin/android/app/admin/DeviceAdminInfo#dump(android.util.Printer,%20kotlin.String))`(`pw:` ` [Printer](https://developer.android.com/reference/kotlin/android/util/Printer.html#)!`, `prefix:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |
| [ActivityInfo](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#)! | [getActivityInfo](https://developer.android.com/reference/kotlin/android/app/admin/DeviceAdminInfo#getActivityInfo())`()` Return the raw information about the receiver implementing this device admin. |
| --- | --- |
| [ComponentName](https://developer.android.com/reference/kotlin/android/content/ComponentName.html#) | [getComponent](https://developer.android.com/reference/kotlin/android/app/admin/DeviceAdminInfo#getComponent())`()` Return the component of the receiver that implements this device admin. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getHeadlessDeviceOwnerMode](https://developer.android.com/reference/kotlin/android/app/admin/DeviceAdminInfo#getHeadlessDeviceOwnerMode())`()` Returns the mode this DeviceAdmin wishes to use if provisioned as a Device Owner on a headless system user mode device. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getPackageName](https://developer.android.com/reference/kotlin/android/app/admin/DeviceAdminInfo#getPackageName())`()` Return the . |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getReceiverName](https://developer.android.com/reference/kotlin/android/app/admin/DeviceAdminInfo#getReceiverName())`()` Return the class name of the receiver component that implements this device admin. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getTagForPolicy](https://developer.android.com/reference/kotlin/android/app/admin/DeviceAdminInfo#getTagForPolicy(kotlin.Int))`(`policyIdent:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return the XML tag name for the given policy identifier. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isVisible](https://developer.android.com/reference/kotlin/android/app/admin/DeviceAdminInfo#isVisible())`()` Returns whether this device admin would like to be visible to the user, even when it is not enabled. |
| --- | --- |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | [loadDescription](https://developer.android.com/reference/kotlin/android/app/admin/DeviceAdminInfo#loadDescription(android.content.pm.PackageManager))`(`pm:` ` [PackageManager](https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#)!`)` Load user-visible description associated with this device admin. |
| [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#)! | [loadIcon](https://developer.android.com/reference/kotlin/android/app/admin/DeviceAdminInfo#loadIcon(android.content.pm.PackageManager))`(`pm:` ` [PackageManager](https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#)!`)` Load the user-displayed icon for this device admin. |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | [loadLabel](https://developer.android.com/reference/kotlin/android/app/admin/DeviceAdminInfo#loadLabel(android.content.pm.PackageManager))`(`pm:` ` [PackageManager](https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#)!`)` Load the user-displayed label for this device admin. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [supportsTransferOwnership](https://developer.android.com/reference/kotlin/android/app/admin/DeviceAdminInfo#supportsTransferOwnership())`()` Return true if this administrator can be a target in an ownership transfer. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/app/admin/DeviceAdminInfo#toString())`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [usesPolicy](https://developer.android.com/reference/kotlin/android/app/admin/DeviceAdminInfo#usesPolicy(kotlin.Int))`(`policyIdent:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return true if the device admin has requested that it be able to use the given policy control. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/app/admin/DeviceAdminInfo#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Used to package this object into a [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#). |

| Properties ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [DeviceAdminInfo](https://developer.android.com/reference/kotlin/android/app/admin/DeviceAdminInfo#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/app/admin/DeviceAdminInfo#CREATOR:android.os.Parcelable.Creator) Used to make this class parcelable. |

## Constants

### HEADLESS_DEVICE_OWNER_MODE_AFFILIATED

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val HEADLESS_DEVICE_OWNER_MODE_AFFILIATED: Int
```

Value for [getHeadlessDeviceOwnerMode](https://developer.android.com/reference/kotlin/android/app/admin/DeviceAdminInfo#getHeadlessDeviceOwnerMode())which indicates that this DPC should be provisioned into "affiliated" mode when on a Headless System User Mode device.

This mode adds a Profile Owner to all users other than the user the Device Owner is on.

Starting from Android version [android.os.Build.VERSION_CODES#VANILLA_ICE_CREAM](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#VANILLA_ICE_CREAM:kotlin.Int), DPCs should set the value of attribute "headless-device-owner-mode" inside the "headless-system-user" tag as "affiliated". 

 Value: 1

### HEADLESS_DEVICE_OWNER_MODE_SINGLE_USER

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val HEADLESS_DEVICE_OWNER_MODE_SINGLE_USER: Int
```

Value for [getHeadlessDeviceOwnerMode](https://developer.android.com/reference/kotlin/android/app/admin/DeviceAdminInfo#getHeadlessDeviceOwnerMode())which indicates that this DPC should be provisioned into the first secondary user when on a Headless System User Mode device.

This mode only allows a single secondary user on the device blocking the creation of additional secondary users.

Starting from Android version [android.os.Build.VERSION_CODES#VANILLA_ICE_CREAM](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#VANILLA_ICE_CREAM:kotlin.Int), DPCs should set the value of attribute "headless-device-owner-mode" inside the "headless-system-user" tag as "single_user". 

 Value: 2

### HEADLESS_DEVICE_OWNER_MODE_UNSUPPORTED

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val HEADLESS_DEVICE_OWNER_MODE_UNSUPPORTED: Int
```

Value for [getHeadlessDeviceOwnerMode](https://developer.android.com/reference/kotlin/android/app/admin/DeviceAdminInfo#getHeadlessDeviceOwnerMode())which indicates that this DPC should not be provisioned into Device Owner mode on a Headless System User Mode device. 

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

A type of policy that this device admin can use: able to force the device to lock viaandroid.app.admin.DevicePolicyManager#lockNow or limit the maximum lock timeout for the device via [DevicePolicyManager.setMaximumTimeToLock](https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager#setMaximumTimeToLock(android.content.ComponentName,%20kotlin.Long)).

To control this policy, the device admin must have a "force-lock" tag in the "uses-policies" section of its meta-data. 

 Value: 3

### USES_POLICY_LIMIT_PASSWORD

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val USES_POLICY_LIMIT_PASSWORD: Int
```

A type of policy that this device admin can use: limit the passwords that the user can select, via [DevicePolicyManager.setPasswordQuality](https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager#setPasswordQuality(android.content.ComponentName,%20kotlin.Int))and [DevicePolicyManager.setPasswordMinimumLength](https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager#setPasswordMinimumLength(android.content.ComponentName,%20kotlin.Int)).

To control this policy, the device admin must be a device owner or profile owner, and must have a "limit-password" tag in the "uses-policies" section of its meta-data. If used by a device owner, the policy only affects the primary user and its profiles, but not any secondary users on the device. 

 Value: 0

### USES_POLICY_RESET_PASSWORD

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val USES_POLICY_RESET_PASSWORD: Int
```

A type of policy that this device admin can use: able to reset the user's password via [DevicePolicyManager.resetPassword](https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager#resetPassword(kotlin.String,%20kotlin.Int)).

To control this policy, the device admin must have a "reset-password" tag in the "uses-policies" section of its meta-data. 

 Value: 2

### USES_POLICY_WATCH_LOGIN

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val USES_POLICY_WATCH_LOGIN: Int
```

A type of policy that this device admin can use: able to watch login attempts from the user, via [DeviceAdminReceiver.ACTION_PASSWORD_FAILED](https://developer.android.com/reference/kotlin/android/app/admin/DeviceAdminReceiver#ACTION_PASSWORD_FAILED:kotlin.String), [DeviceAdminReceiver.ACTION_PASSWORD_SUCCEEDED](https://developer.android.com/reference/kotlin/android/app/admin/DeviceAdminReceiver#ACTION_PASSWORD_SUCCEEDED:kotlin.String), and [DevicePolicyManager.getCurrentFailedPasswordAttempts](https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager#getCurrentFailedPasswordAttempts()).

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
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!:The Context in which we are parsing the device admin. |
| `resolveInfo` | [ResolveInfo](https://developer.android.com/reference/kotlin/android/content/pm/ResolveInfo.html#)!:The ResolveInfo returned from the package manager about this device admin's component. |

## Public methods

### describeContents

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

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
| [ComponentName](https://developer.android.com/reference/kotlin/android/content/ComponentName.html#) | This value cannot be`null`. |

### getHeadlessDeviceOwnerMode

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getHeadlessDeviceOwnerMode(): Int
```

Returns the mode this DeviceAdmin wishes to use if provisioned as a Device Owner on a headless system user mode device.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.app.admin.DeviceAdminInfo#HEADLESS_DEVICE_OWNER_MODE_UNSUPPORTED](https://developer.android.com/reference/kotlin/android/app/admin/DeviceAdminInfo#HEADLESS_DEVICE_OWNER_MODE_UNSUPPORTED:kotlin.Int), [android.app.admin.DeviceAdminInfo#HEADLESS_DEVICE_OWNER_MODE_AFFILIATED](https://developer.android.com/reference/kotlin/android/app/admin/DeviceAdminInfo#HEADLESS_DEVICE_OWNER_MODE_AFFILIATED:kotlin.Int), or [android.app.admin.DeviceAdminInfo#HEADLESS_DEVICE_OWNER_MODE_SINGLE_USER](https://developer.android.com/reference/kotlin/android/app/admin/DeviceAdminInfo#HEADLESS_DEVICE_OWNER_MODE_SINGLE_USER:kotlin.Int) |

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

Return the XML tag name for the given policy identifier. Valid identifiers are as per [usesPolicy(int)](https://developer.android.com/reference/kotlin/android/app/admin/DeviceAdminInfo#usesPolicy(kotlin.Int)). If the given identifier is not known, null is returned. 

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
| `pm` | [PackageManager](https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#)!:Supply a PackageManager used to load the device admin's resources. |

### loadIcon

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun loadIcon(pm: PackageManager!): Drawable!
```

Load the user-displayed icon for this device admin.

| Parameters ||
|------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `pm` | [PackageManager](https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#)!:Supply a PackageManager used to load the device admin's resources. |

### loadLabel

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun loadLabel(pm: PackageManager!): CharSequence!
```

Load the user-displayed label for this device admin.

| Parameters ||
|------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `pm` | [PackageManager](https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#)!:Supply a PackageManager used to load the device admin's resources. |

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

Return true if the device admin has requested that it be able to use the given policy control. The possible policy identifier inputs are: [USES_POLICY_LIMIT_PASSWORD](https://developer.android.com/reference/kotlin/android/app/admin/DeviceAdminInfo#USES_POLICY_LIMIT_PASSWORD:kotlin.Int), [USES_POLICY_WATCH_LOGIN](https://developer.android.com/reference/kotlin/android/app/admin/DeviceAdminInfo#USES_POLICY_WATCH_LOGIN:kotlin.Int), [USES_POLICY_RESET_PASSWORD](https://developer.android.com/reference/kotlin/android/app/admin/DeviceAdminInfo#USES_POLICY_RESET_PASSWORD:kotlin.Int), [USES_POLICY_FORCE_LOCK](https://developer.android.com/reference/kotlin/android/app/admin/DeviceAdminInfo#USES_POLICY_FORCE_LOCK:kotlin.Int), [USES_POLICY_WIPE_DATA](https://developer.android.com/reference/kotlin/android/app/admin/DeviceAdminInfo#USES_POLICY_WIPE_DATA:kotlin.Int), [USES_POLICY_EXPIRE_PASSWORD](https://developer.android.com/reference/kotlin/android/app/admin/DeviceAdminInfo#USES_POLICY_EXPIRE_PASSWORD:kotlin.Int), [USES_ENCRYPTED_STORAGE](https://developer.android.com/reference/kotlin/android/app/admin/DeviceAdminInfo#USES_ENCRYPTED_STORAGE:kotlin.Int), [USES_POLICY_DISABLE_CAMERA](https://developer.android.com/reference/kotlin/android/app/admin/DeviceAdminInfo#USES_POLICY_DISABLE_CAMERA:kotlin.Int). 

### writeToParcel

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

Used to package this object into a [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#).

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#):The [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#) to be written. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The flags used for parceling. |

## Properties

### CREATOR

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<DeviceAdminInfo!>
```

Used to make this class parcelable.
