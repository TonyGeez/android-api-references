Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PermissionInfo

```
open class PermissionInfo : PackageItemInfo, Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.content.pm.PackageItemInfo](../android/content/pm/PackageItemInfo.md) ||
| | ↳ | [android.content.pm.PermissionInfo](../android/content/pm/PermissionInfo.md) |

Information you can retrieve about a particular security permission known to the system. This corresponds to information collected from the AndroidManifest.xml's \<permission\> tags.

## Summary

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo#FLAG_ALLOWED_IN_PRIVATE_COMPUTE_CORE:kotlin.Int` Flag for `https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo#flags:kotlin.Int`, corresponding to `allowedInPrivateComputeCore` Determines whether this permission can be obtained by components running in the Private Compute Core restricted environment. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo#FLAG_COSTS_MONEY:kotlin.Int` Flag for `https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo#flags:kotlin.Int`, corresponding to `costsMoney` value of `https://developer.android.com/reference/kotlin/android/R.attr.html#permissionFlags:kotlin.Int`. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo#FLAG_HARD_RESTRICTED:kotlin.Int` Flag for `https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo#flags:kotlin.Int`, corresponding to `hardRestricted` value of `https://developer.android.com/reference/kotlin/android/R.attr.html#permissionFlags:kotlin.Int`. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo#FLAG_IMMUTABLY_RESTRICTED:kotlin.Int` Flag for `https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo#flags:kotlin.Int`, corresponding to `immutablyRestricted` value of `https://developer.android.com/reference/kotlin/android/R.attr.html#permissionFlags:kotlin.Int`. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo#FLAG_INSTALLED:kotlin.Int` Flag for `https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo#flags:kotlin.Int`, indicating that this permission has been installed into the system's globally defined permissions. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo#FLAG_SOFT_RESTRICTED:kotlin.Int` Flag for `https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo#flags:kotlin.Int`, corresponding to `softRestricted` value of `https://developer.android.com/reference/kotlin/android/R.attr.html#permissionFlags:kotlin.Int`. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo#PROTECTION_DANGEROUS:kotlin.Int` Dangerous value for `https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo#protectionLevel:kotlin.Int`, corresponding to the `dangerous` value of `https://developer.android.com/reference/kotlin/android/R.attr.html#protectionLevel:kotlin.Int`. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo#PROTECTION_FLAG_APPOP:kotlin.Int` Additional flag for `https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo#protectionLevel:kotlin.Int`, corresponding to the `appop` value of `https://developer.android.com/reference/kotlin/android/R.attr.html#protectionLevel:kotlin.Int`. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo#PROTECTION_FLAG_DEVELOPMENT:kotlin.Int` Additional flag for `https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo#protectionLevel:kotlin.Int`, corresponding to the `development` value of `https://developer.android.com/reference/kotlin/android/R.attr.html#protectionLevel:kotlin.Int`. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo#PROTECTION_FLAG_INSTALLER:kotlin.Int` Additional flag for `https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo#protectionLevel:kotlin.Int`, corresponding to the `installer` value of `https://developer.android.com/reference/kotlin/android/R.attr.html#protectionLevel:kotlin.Int`. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo#PROTECTION_FLAG_INSTANT:kotlin.Int` Additional flag for `https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo#protectionLevel:kotlin.Int`, corresponding to the `instant` value of `https://developer.android.com/reference/kotlin/android/R.attr.html#protectionLevel:kotlin.Int`. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo#PROTECTION_FLAG_PRE23:kotlin.Int` Additional flag for `https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo#protectionLevel:kotlin.Int`, corresponding to the `pre23` value of `https://developer.android.com/reference/kotlin/android/R.attr.html#protectionLevel:kotlin.Int`. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo#PROTECTION_FLAG_PREINSTALLED:kotlin.Int` Additional flag for `https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo#protectionLevel:kotlin.Int`, corresponding to the `preinstalled` value of `https://developer.android.com/reference/kotlin/android/R.attr.html#protectionLevel:kotlin.Int`. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo#PROTECTION_FLAG_PRIVILEGED:kotlin.Int` Additional flag for `https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo#protectionLevel:kotlin.Int`, corresponding to the `privileged` value of `https://developer.android.com/reference/kotlin/android/R.attr.html#protectionLevel:kotlin.Int`. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo#PROTECTION_FLAG_RUNTIME_ONLY:kotlin.Int` Additional flag for `https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo#protectionLevel:kotlin.Int`, corresponding to the `runtime` value of `https://developer.android.com/reference/kotlin/android/R.attr.html#protectionLevel:kotlin.Int`. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo#PROTECTION_FLAG_SETUP:kotlin.Int` Additional flag for `https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo#protectionLevel:kotlin.Int`, corresponding to the `setup` value of `https://developer.android.com/reference/kotlin/android/R.attr.html#protectionLevel:kotlin.Int`. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo#PROTECTION_FLAG_SYSTEM:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo#PROTECTION_FLAG_VERIFIER:kotlin.Int` Additional flag for `https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo#protectionLevel:kotlin.Int`, corresponding to the `verifier` value of `https://developer.android.com/reference/kotlin/android/R.attr.html#protectionLevel:kotlin.Int`. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo#PROTECTION_INTERNAL:kotlin.Int` System-level value for `https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo#protectionLevel:kotlin.Int`, corresponding to the `internal` value of `https://developer.android.com/reference/kotlin/android/R.attr.html#protectionLevel:kotlin.Int`. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo#PROTECTION_MASK_BASE:kotlin.Int` Mask for `https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo#protectionLevel:kotlin.Int`: the basic protection type. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo#PROTECTION_MASK_FLAGS:kotlin.Int` Mask for `https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo#protectionLevel:kotlin.Int`: additional flag bits. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo#PROTECTION_NORMAL:kotlin.Int` A normal application value for `https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo#protectionLevel:kotlin.Int`, corresponding to the `normal` value of `https://developer.android.com/reference/kotlin/android/R.attr.html#protectionLevel:kotlin.Int`. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo#PROTECTION_SIGNATURE:kotlin.Int` System-level value for `https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo#protectionLevel:kotlin.Int`, corresponding to the `signature` value of `https://developer.android.com/reference/kotlin/android/R.attr.html#protectionLevel:kotlin.Int`. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo#PROTECTION_SIGNATURE_OR_SYSTEM:kotlin.Int` <br /> |
| --- | --- |

Inherited constants From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int`

Descriptor bit used with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()`: indicates that the Parcelable object's flattened representation includes a file descriptor.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`

Flag for use with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point.

<br />

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo#PermissionInfo()()` <br /> |
| `https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo#PermissionInfo(android.content.pm.PermissionInfo)(orig: https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo#)` <br /> |

| Public methods ||
|---|---|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo#describeContents()()` Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo#getProtection()()` Return the base permission type. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo#getProtectionFlags()()` Return the additional flags in `https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo#protectionLevel:kotlin.Int`. |
| --- | --- |
| open [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | `https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo#loadDescription(android.content.pm.PackageManager)(pm: https://developer.android.com/reference/kotlin/android/content/pm/PackageManager)` Retrieve the textual description of this permission. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo#toString()()` Returns a string representation of the object. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo#writeToParcel(android.os.Parcel,%20kotlin.Int)(dest: https://developer.android.com/reference/kotlin/android/os/Parcel.html#, parcelableFlags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Flatten this object in to a Parcel. |
| --- | --- |

Inherited functions From class `https://developer.android.com/reference/kotlin/android/content/pm/PackageItemInfo` `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageItemInfo#dumpBack(android.util.Printer,%20kotlin.String)(pw: https://developer.android.com/reference/kotlin/android/util/Printer.html#!, prefix: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageItemInfo#dumpFront(android.util.Printer,%20kotlin.String)(pw: https://developer.android.com/reference/kotlin/android/util/Printer.html#!, prefix: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)`

<br />

`https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#!` `https://developer.android.com/reference/kotlin/android/content/pm/PackageItemInfo#loadBanner(android.content.pm.PackageManager)(pm: https://developer.android.com/reference/kotlin/android/content/pm/PackageManager!)`

Retrieve the current graphical banner associated with this item. This will call back on the given PackageManager to load the banner from the application.

The returned drawable is subject to the same size capping limits as described in `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#getApplicationIcon(android.content.pm.ApplicationInfo)`.

<br />

`https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#!` `https://developer.android.com/reference/kotlin/android/content/pm/PackageItemInfo#loadIcon(android.content.pm.PackageManager)(pm: https://developer.android.com/reference/kotlin/android/content/pm/PackageManager!)`

Retrieve the current graphical icon associated with this item. This will call back on the given PackageManager to load the icon from the application.

The returned drawable is subject to the same size capping limits as described in `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#getApplicationIcon(android.content.pm.ApplicationInfo)`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageItemInfo#loadLabel(android.content.pm.PackageManager)(pm: https://developer.android.com/reference/kotlin/android/content/pm/PackageManager)`

Retrieve the current textual label associated with this item. This will call back on the given PackageManager to load the label from the application.

<br />

`https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#!` `https://developer.android.com/reference/kotlin/android/content/pm/PackageItemInfo#loadLogo(android.content.pm.PackageManager)(pm: https://developer.android.com/reference/kotlin/android/content/pm/PackageManager!)`

Retrieve the current graphical logo associated with this item. This will call back on the given PackageManager to load the logo from the application.

The returned drawable is subject to the same size capping limits as described in `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#getApplicationIcon(android.content.pm.ApplicationInfo)`.

<br />

`https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#!` `https://developer.android.com/reference/kotlin/android/content/pm/PackageItemInfo#loadUnbadgedIcon(android.content.pm.PackageManager)(pm: https://developer.android.com/reference/kotlin/android/content/pm/PackageManager!)`

Retrieve the current graphical icon associated with this item without the addition of a work badge if applicable. This will call back on the given PackageManager to load the icon from the application.

The returned drawable is subject to the same size capping limits as described in `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#getApplicationIcon(android.content.pm.ApplicationInfo)`.

<br />

`https://developer.android.com/reference/kotlin/android/content/res/XmlResourceParser.html#!` `https://developer.android.com/reference/kotlin/android/content/pm/PackageItemInfo#loadXmlMetaData(android.content.pm.PackageManager,%20kotlin.String)(pm: https://developer.android.com/reference/kotlin/android/content/pm/PackageManager!, name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)`

Load an XML resource attached to the meta-data of this item. This will retrieved the name meta-data entry, and if defined call back on the given PackageManager to load its XML file from the application.

<br />

| Properties ||
|---|---|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [PermissionInfo](../android/content/pm/PermissionInfo.md)!\> | `https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo#CREATOR:android.os.Parcelable.Creator` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo#descriptionRes:kotlin.Int` A string resource identifier (in the package's resources) of this permission's description. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo#flags:kotlin.Int` Additional flags about this permission as given by `https://developer.android.com/reference/kotlin/android/R.attr.html#permissionFlags:kotlin.Int`. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | `https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo#group:kotlin.String` The group this permission is a part of, as per `https://developer.android.com/reference/kotlin/android/R.attr.html#permissionGroup:kotlin.Int`. |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | `https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo#nonLocalizedDescription:kotlin.CharSequence` The description string provided in the AndroidManifest file, if any. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo#protectionLevel:kotlin.Int` The level of access this permission is protecting, as per . |
| --- | --- |

Inherited properties From class `https://developer.android.com/reference/kotlin/android/content/pm/PackageItemInfo` `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageItemInfo#banner:kotlin.Int`

A drawable resource identifier (in the package's resources) of this component's banner. From the "banner" attribute or, if not set, 0.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageItemInfo#icon:kotlin.Int`

A drawable resource identifier (in the package's resources) of this component's icon. From the "icon" attribute or, if not set, 0.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageItemInfo#isArchived:kotlin.Boolean`

Whether the package is currently in an archived state.

Packages can be archived through `https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#requestArchive(kotlin.String,%20android.content.IntentSender)` and do not have any APKs stored on the device, but do keep the data directory.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageItemInfo#labelRes:kotlin.Int`

A string resource identifier (in the package's resources) of this component's label. From the "label" attribute or, if not set, 0.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageItemInfo#logo:kotlin.Int`

A drawable resource identifier (in the package's resources) of this component's logo. Logos may be larger/wider than icons and are displayed by certain UI elements in place of a name or name/icon combination. From the "logo" attribute or, if not set, 0.

<br />

`https://developer.android.com/reference/kotlin/android/os/Bundle.html#!` `https://developer.android.com/reference/kotlin/android/content/pm/PackageItemInfo#metaData:android.os.Bundle`

Additional meta-data associated with this component. This field will only be filled in if you set the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#GET_META_DATA:kotlin.Int` flag when requesting the info.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` `https://developer.android.com/reference/kotlin/android/content/pm/PackageItemInfo#name:kotlin.String`

Public name of this item. From the "android:name" attribute.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!` `https://developer.android.com/reference/kotlin/android/content/pm/PackageItemInfo#nonLocalizedLabel:kotlin.CharSequence`

The string provided in the AndroidManifest file, if any. You probably don't want to use this. You probably want `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#getApplicationLabel(android.content.pm.ApplicationInfo)`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` `https://developer.android.com/reference/kotlin/android/content/pm/PackageItemInfo#packageName:kotlin.String`

Name of the package that this item is in.

<br />

## Constants

### FLAG_ALLOWED_IN_PRIVATE_COMPUTE_CORE

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_ALLOWED_IN_PRIVATE_COMPUTE_CORE: Int
```

Flag for `https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo#flags:kotlin.Int`, corresponding to `allowedInPrivateComputeCore` Determines whether this permission can be obtained by components running in the Private Compute Core restricted environment.

 Value: 32

### FLAG_COSTS_MONEY

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_COSTS_MONEY: Int
```

Flag for `https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo#flags:kotlin.Int`, corresponding to `costsMoney` value of `https://developer.android.com/reference/kotlin/android/R.attr.html#permissionFlags:kotlin.Int`.

 Value: 1

### FLAG_HARD_RESTRICTED

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_HARD_RESTRICTED: Int
```

Flag for `https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo#flags:kotlin.Int`, corresponding to `hardRestricted` value of `https://developer.android.com/reference/kotlin/android/R.attr.html#permissionFlags:kotlin.Int`.

This permission is restricted by the platform and it would be grantable only to apps that meet special criteria per platform policy.

 Value: 4

### FLAG_IMMUTABLY_RESTRICTED

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_IMMUTABLY_RESTRICTED: Int
```

Flag for `https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo#flags:kotlin.Int`, corresponding to `immutablyRestricted` value of `https://developer.android.com/reference/kotlin/android/R.attr.html#permissionFlags:kotlin.Int`.

This permission is restricted immutably which means that its restriction state may be specified only on the first install of the app and will stay in this initial allowlist state until the app is uninstalled.

 Value: 16

### FLAG_INSTALLED

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_INSTALLED: Int
```

Flag for `https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo#flags:kotlin.Int`, indicating that this permission has been installed into the system's globally defined permissions.

 Value: 1073741824

### FLAG_SOFT_RESTRICTED

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_SOFT_RESTRICTED: Int
```

Flag for `https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo#flags:kotlin.Int`, corresponding to `softRestricted` value of `https://developer.android.com/reference/kotlin/android/R.attr.html#permissionFlags:kotlin.Int`.

This permission is restricted by the platform and it would be grantable in its full form to apps that meet special criteria per platform policy. Otherwise, a weaker form of the permission would be granted. The weak grant depends on the permission.

 Value: 8

### PROTECTION_DANGEROUS

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PROTECTION_DANGEROUS: Int
```

Dangerous value for `https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo#protectionLevel:kotlin.Int`, corresponding to the `dangerous` value of `https://developer.android.com/reference/kotlin/android/R.attr.html#protectionLevel:kotlin.Int`.

 Value: 1

### PROTECTION_FLAG_APPOP

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PROTECTION_FLAG_APPOP: Int
```

Additional flag for `https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo#protectionLevel:kotlin.Int`, corresponding to the `appop` value of `https://developer.android.com/reference/kotlin/android/R.attr.html#protectionLevel:kotlin.Int`.

 Value: 64

### PROTECTION_FLAG_DEVELOPMENT

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PROTECTION_FLAG_DEVELOPMENT: Int
```

Additional flag for `https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo#protectionLevel:kotlin.Int`, corresponding to the `development` value of `https://developer.android.com/reference/kotlin/android/R.attr.html#protectionLevel:kotlin.Int`.

 Value: 32

### PROTECTION_FLAG_INSTALLER

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PROTECTION_FLAG_INSTALLER: Int
```

Additional flag for `https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo#protectionLevel:kotlin.Int`, corresponding to the `installer` value of `https://developer.android.com/reference/kotlin/android/R.attr.html#protectionLevel:kotlin.Int`.

 Value: 256

### PROTECTION_FLAG_INSTANT

Added in [API level 27](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PROTECTION_FLAG_INSTANT: Int
```

Additional flag for `https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo#protectionLevel:kotlin.Int`, corresponding to the `instant` value of `https://developer.android.com/reference/kotlin/android/R.attr.html#protectionLevel:kotlin.Int`.

 Value: 4096

### PROTECTION_FLAG_PRE23

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PROTECTION_FLAG_PRE23: Int
```

Additional flag for `https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo#protectionLevel:kotlin.Int`, corresponding to the `pre23` value of `https://developer.android.com/reference/kotlin/android/R.attr.html#protectionLevel:kotlin.Int`.

 Value: 128

### PROTECTION_FLAG_PREINSTALLED

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PROTECTION_FLAG_PREINSTALLED: Int
```

Additional flag for `https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo#protectionLevel:kotlin.Int`, corresponding to the `preinstalled` value of `https://developer.android.com/reference/kotlin/android/R.attr.html#protectionLevel:kotlin.Int`.

 Value: 1024

### PROTECTION_FLAG_PRIVILEGED

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PROTECTION_FLAG_PRIVILEGED: Int
```

Additional flag for `https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo#protectionLevel:kotlin.Int`, corresponding to the `privileged` value of `https://developer.android.com/reference/kotlin/android/R.attr.html#protectionLevel:kotlin.Int`.

 Value: 16

### PROTECTION_FLAG_RUNTIME_ONLY

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PROTECTION_FLAG_RUNTIME_ONLY: Int
```

Additional flag for `https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo#protectionLevel:kotlin.Int`, corresponding to the `runtime` value of `https://developer.android.com/reference/kotlin/android/R.attr.html#protectionLevel:kotlin.Int`.

 Value: 8192

### PROTECTION_FLAG_SETUP

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PROTECTION_FLAG_SETUP: Int
```

Additional flag for `https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo#protectionLevel:kotlin.Int`, corresponding to the `setup` value of `https://developer.android.com/reference/kotlin/android/R.attr.html#protectionLevel:kotlin.Int`.

 Value: 2048

### PROTECTION_FLAG_SYSTEM

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PROTECTION_FLAG_SYSTEM: Int
```

**Deprecated:** *Old name for `https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo#PROTECTION_FLAG_PRIVILEGED:kotlin.Int`, which is now very confusing because it only applies to privileged apps, not all apps on the system image.*

 Value: 16

### PROTECTION_FLAG_VERIFIER

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PROTECTION_FLAG_VERIFIER: Int
```

Additional flag for `https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo#protectionLevel:kotlin.Int`, corresponding to the `verifier` value of `https://developer.android.com/reference/kotlin/android/R.attr.html#protectionLevel:kotlin.Int`.

 Value: 512

### PROTECTION_INTERNAL

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PROTECTION_INTERNAL: Int
```

System-level value for `https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo#protectionLevel:kotlin.Int`, corresponding to the `internal` value of `https://developer.android.com/reference/kotlin/android/R.attr.html#protectionLevel:kotlin.Int`.

 Value: 4

### PROTECTION_MASK_BASE

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PROTECTION_MASK_BASE: Int
```

**Deprecated:** *Use #getProtection() instead.*

Mask for `https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo#protectionLevel:kotlin.Int`: the basic protection type.

 Value: 15

### PROTECTION_MASK_FLAGS

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PROTECTION_MASK_FLAGS: Int
```

**Deprecated:** *Use #getProtectionFlags() instead.*

Mask for `https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo#protectionLevel:kotlin.Int`: additional flag bits.

 Value: 65520

### PROTECTION_NORMAL

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PROTECTION_NORMAL: Int
```

A normal application value for `https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo#protectionLevel:kotlin.Int`, corresponding to the `normal` value of `https://developer.android.com/reference/kotlin/android/R.attr.html#protectionLevel:kotlin.Int`.

 Value: 0

### PROTECTION_SIGNATURE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PROTECTION_SIGNATURE: Int
```

System-level value for `https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo#protectionLevel:kotlin.Int`, corresponding to the `signature` value of `https://developer.android.com/reference/kotlin/android/R.attr.html#protectionLevel:kotlin.Int`.

 Value: 2

### PROTECTION_SIGNATURE_OR_SYSTEM

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PROTECTION_SIGNATURE_OR_SYSTEM: Int
```

**Deprecated:** *Use `https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo#PROTECTION_SIGNATURE:kotlin.Int`|`https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo#PROTECTION_FLAG_PRIVILEGED:kotlin.Int` instead.*
| --- | --- |

 Value: 3

## Public constructors

### PermissionInfo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
PermissionInfo()
```

**Deprecated:** *Should only be created by the system.*

### PermissionInfo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
PermissionInfo(orig: PermissionInfo)
```

**Deprecated:** *Should only be created by the system.*

| Parameters ||
|---|---|
| `orig` | [PermissionInfo](../android/content/pm/PermissionInfo.md): This value cannot be `null`. |

## Public methods

### describeContents

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### getProtection

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getProtection(): Int
```

Return the base permission type.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is one of the following: - `https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo#PROTECTION_NORMAL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo#PROTECTION_DANGEROUS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo#PROTECTION_SIGNATURE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo#PROTECTION_SIGNATURE_OR_SYSTEM:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo#PROTECTION_INTERNAL:kotlin.Int` |

### getProtectionFlags

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getProtectionFlags(): Int
```

Return the additional flags in `https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo#protectionLevel:kotlin.Int`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo#PROTECTION_FLAG_PRIVILEGED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo#PROTECTION_FLAG_SYSTEM:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo#PROTECTION_FLAG_DEVELOPMENT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo#PROTECTION_FLAG_APPOP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo#PROTECTION_FLAG_PRE23:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo#PROTECTION_FLAG_INSTALLER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo#PROTECTION_FLAG_VERIFIER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo#PROTECTION_FLAG_PREINSTALLED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo#PROTECTION_FLAG_SETUP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo#PROTECTION_FLAG_INSTANT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo#PROTECTION_FLAG_RUNTIME_ONLY:kotlin.Int` |

### loadDescription

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun loadDescription(pm: PackageManager): CharSequence?
```

Retrieve the textual description of this permission. This will call back on the given PackageManager to load the description from the application.

| Parameters ||
|---|---|
| `pm` | [PackageManager](../android/content/pm/PackageManager.md): A PackageManager from which the label can be loaded; usually the PackageManager from which you originally retrieved this item. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html?` | Returns a CharSequence containing the permission's description. If there is no description, null is returned. |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun toString(): String
```

Returns a string representation of the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the object. |

### writeToParcel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun writeToParcel(
    dest: Parcel, 
    parcelableFlags: Int
): Unit
```

Flatten this object in to a Parcel.

| Parameters ||
|---|---|
| `dest` | [Parcel](../android/os/Parcel.md): The Parcel in which the object should be written. This value cannot be `null`. |
| `flags` | Additional flags about how the object should be written. May be 0 or `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` |

## Properties

### CREATOR

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<PermissionInfo!>
```

### descriptionRes

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var descriptionRes: Int
```

A string resource identifier (in the package's resources) of this permission's description. From the "description" attribute or, if not set, 0.

### flags

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var flags: Int
```

Additional flags about this permission as given by `https://developer.android.com/reference/kotlin/android/R.attr.html#permissionFlags:kotlin.Int`. 
Value is either `0` or a combination of the following:

- `https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo#FLAG_COSTS_MONEY:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo#FLAG_HARD_RESTRICTED:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo#FLAG_SOFT_RESTRICTED:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo#FLAG_IMMUTABLY_RESTRICTED:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo#FLAG_ALLOWED_IN_PRIVATE_COMPUTE_CORE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo#FLAG_INSTALLED:kotlin.Int`

<br />

### group

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var group: String?
```

The group this permission is a part of, as per `https://developer.android.com/reference/kotlin/android/R.attr.html#permissionGroup:kotlin.Int`.

The actual grouping of platform-defined runtime permissions is subject to change and can be queried with `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#getGroupOfPlatformPermission(kotlin.String,%20java.util.concurrent.Executor,%20java.util.function.Consumer)`.

### nonLocalizedDescription

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var nonLocalizedDescription: CharSequence?
```

The description string provided in the AndroidManifest file, if any. You probably don't want to use this, since it will be null if the description is in a resource. You probably want `https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo#loadDescription(android.content.pm.PackageManager)` instead.

### protectionLevel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var protectionLevel: Int
```

**Deprecated:** *Use #getProtection() and #getProtectionFlags() instead.*

The level of access this permission is protecting, as per . Consists of a base permission type and zero or more flags. Use the following functions to extract them.

```kotlin
int basePermissionType = permissionInfo.getProtection();
  int permissionFlags = permissionInfo.getProtectionFlags();
  
```

<br />

<br />

Base permission types are `https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo#PROTECTION_NORMAL:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo#PROTECTION_DANGEROUS:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo#PROTECTION_SIGNATURE:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo#PROTECTION_INTERNAL:kotlin.Int` and the deprecated `https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo#PROTECTION_SIGNATURE_OR_SYSTEM:kotlin.Int`. Flags are listed under `https://developer.android.com/reference/kotlin/android/R.attr.html#protectionLevel:kotlin.Int`.
