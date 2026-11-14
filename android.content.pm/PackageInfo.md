Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PackageInfo

```
open class PackageInfo : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.content.pm.PackageInfo](../android/content/pm/PackageInfo.md) |

Overall information about the contents of a package. This corresponds to all of the information collected from AndroidManifest.xml.

## Summary

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageInfo#INSTALL_LOCATION_AUTO:kotlin.Int` Constant corresponding to `auto` in the `https://developer.android.com/reference/kotlin/android/R.attr.html#installLocation:kotlin.Int` attribute. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageInfo#INSTALL_LOCATION_INTERNAL_ONLY:kotlin.Int` Constant corresponding to `internalOnly` in the `https://developer.android.com/reference/kotlin/android/R.attr.html#installLocation:kotlin.Int` attribute. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageInfo#INSTALL_LOCATION_PREFER_EXTERNAL:kotlin.Int` Constant corresponding to `preferExternal` in the `https://developer.android.com/reference/kotlin/android/R.attr.html#installLocation:kotlin.Int` attribute. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageInfo#REQUESTED_PERMISSION_GRANTED:kotlin.Int` Flag for `https://developer.android.com/reference/kotlin/android/content/pm/PackageInfo#requestedPermissionsFlags:kotlin.IntArray`: the requested permission is currently granted to the application. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageInfo#REQUESTED_PERMISSION_IMPLICIT:kotlin.Int` Flag for `https://developer.android.com/reference/kotlin/android/content/pm/PackageInfo#requestedPermissionsFlags:kotlin.IntArray`: the requested permission was not explicitly requested via uses-permission, but was instead implicitly requested (e.g., for version compatibility reasons). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageInfo#REQUESTED_PERMISSION_NEVER_FOR_LOCATION:kotlin.Int` Flag for `https://developer.android.com/reference/kotlin/android/content/pm/PackageInfo#requestedPermissionsFlags:kotlin.IntArray`: the requested permission has declared `neverForLocation` in their manifest as a strong assertion by a developer that they will never use this permission to derive the physical location of the device, regardless of `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String` and/or `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_COARSE_LOCATION:kotlin.String` being granted. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageInfo#REQUESTED_PERMISSION_ONLY_FOR_LOCATION_BUTTON:kotlin.Int` Flag for `https://developer.android.com/reference/kotlin/android/content/pm/PackageInfo#requestedPermissionsFlags:kotlin.IntArray`: It only applies to `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String`. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageInfo#REQUESTED_PERMISSION_PRIVATE_COMPUTE_CORE_ONLY:kotlin.Int` Flag for `https://developer.android.com/reference/kotlin/android/content/pm/PackageInfo#requestedPermissionsFlags:kotlin.IntArray`: the requested permission is restricted to the Private Compute Core. |

Inherited constants From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int`

Descriptor bit used with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()`: indicates that the Parcelable object's flattened representation includes a file descriptor.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`

Flag for use with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point.

<br />

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/pm/PackageInfo#PackageInfo()()` <br /> |

| Public methods ||
|---|---|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageInfo#describeContents()()` Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | `https://developer.android.com/reference/kotlin/android/content/pm/PackageInfo#getApexPackageName()()` If the package is an APEX package (i.e. the value of |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageInfo#getArchiveTimeMillis()()` Returns the time at which the app was archived for the user. |
| --- | --- |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageInfo#getLongVersionCode()()` Return `https://developer.android.com/reference/kotlin/android/R.styleable.html#AndroidManifest_versionCode:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/R.styleable.html#AndroidManifest_versionCodeMajor:kotlin.Int` combined together as a single long value. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageInfo#isAppMetadataVerified()()` Returns the verification status of the App Metadata of the package. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageInfo#setLongVersionCode(kotlin.Long)(longVersionCode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Set the full version code in this PackageInfo, updating `https://developer.android.com/reference/kotlin/android/content/pm/PackageInfo#versionCode:kotlin.Int` with the lower bits. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageInfo#toString()()` Returns a string representation of the object. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageInfo#writeToParcel(android.os.Parcel,%20kotlin.Int)(dest: https://developer.android.com/reference/kotlin/android/os/Parcel.html#, parcelableFlags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Flatten this object in to a Parcel. |

| Properties ||
|---|---|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [PackageInfo](../android/content/pm/PackageInfo.md)!\> | `https://developer.android.com/reference/kotlin/android/content/pm/PackageInfo#CREATOR:android.os.Parcelable.Creator` <br /> |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [ActivityInfo](../android/content/pm/ActivityInfo.md)!\>? | `https://developer.android.com/reference/kotlin/android/content/pm/PackageInfo#activities:kotlin.Array` Array of all `https://developer.android.com/reference/kotlin/android/R.styleable.html#AndroidManifestActivity:kotlin.IntArray` tags included under \<application\>, or null if there were none. |
| [ApplicationInfo](../android/content/pm/ApplicationInfo.md)? | `https://developer.android.com/reference/kotlin/android/content/pm/PackageInfo#applicationInfo:android.content.pm.ApplicationInfo` Information collected from the \<application\> tag, or null if there was none. |
| --- | --- |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Attribution](../android/content/pm/Attribution.md)!\>? | `https://developer.android.com/reference/kotlin/android/content/pm/PackageInfo#attributions:kotlin.Array` Array of all `https://developer.android.com/reference/kotlin/android/R.styleable.html#AndroidManifestAttribution:kotlin.IntArray` tags included under \<manifest\>, or null if there were none. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageInfo#baseRevisionCode:kotlin.Int` The revision number of the base APK for this package, as specified by the \<manifest\> tag's `https://developer.android.com/reference/kotlin/android/R.styleable.html#AndroidManifest_revisionCode:kotlin.Int` attribute. |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [ConfigurationInfo](../android/content/pm/ConfigurationInfo.md)!\>? | `https://developer.android.com/reference/kotlin/android/content/pm/PackageInfo#configPreferences:kotlin.Array` Application specified preferred configuration `https://developer.android.com/reference/kotlin/android/R.styleable.html#AndroidManifestUsesConfiguration:kotlin.IntArray` tags included under \<manifest\>, or null if there were none. |
| --- | --- |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [FeatureGroupInfo](../android/content/pm/FeatureGroupInfo.md)!\>? | `https://developer.android.com/reference/kotlin/android/content/pm/PackageInfo#featureGroups:kotlin.Array` Groups of features that this application has requested. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageInfo#firstInstallTime:kotlin.Long` The time at which the app was first installed. |
| [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)? | `https://developer.android.com/reference/kotlin/android/content/pm/PackageInfo#gids:kotlin.IntArray` All kernel group-IDs that have been assigned to this package. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageInfo#installLocation:kotlin.Int` The install location requested by the package. |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [InstrumentationInfo](../android/content/pm/InstrumentationInfo.md)!\>? | `https://developer.android.com/reference/kotlin/android/content/pm/PackageInfo#instrumentation:kotlin.Array` Array of all `https://developer.android.com/reference/kotlin/android/R.styleable.html#AndroidManifestInstrumentation:kotlin.IntArray` tags included under \<manifest\>, or null if there were none. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageInfo#isApex:kotlin.Boolean` Whether the package is an APEX package. |
| --- | --- |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageInfo#lastUpdateTime:kotlin.Long` The time at which the app was last updated. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageInfo#packageName:kotlin.String` The name of this package. |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [PermissionInfo](../android/content/pm/PermissionInfo.md)!\>? | `https://developer.android.com/reference/kotlin/android/content/pm/PackageInfo#permissions:kotlin.Array` Array of all `https://developer.android.com/reference/kotlin/android/R.styleable.html#AndroidManifestPermission:kotlin.IntArray` tags included under \<manifest\>, or null if there were none. |
| --- | --- |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [ProviderInfo](../android/content/pm/ProviderInfo.md)!\>? | `https://developer.android.com/reference/kotlin/android/content/pm/PackageInfo#providers:kotlin.Array` Array of all `https://developer.android.com/reference/kotlin/android/R.styleable.html#AndroidManifestProvider:kotlin.IntArray` tags included under \<application\>, or null if there were none. |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [ActivityInfo](../android/content/pm/ActivityInfo.md)!\>? | `https://developer.android.com/reference/kotlin/android/content/pm/PackageInfo#receivers:kotlin.Array` Array of all `https://developer.android.com/reference/kotlin/android/R.styleable.html#AndroidManifestReceiver:kotlin.IntArray` tags included under \<application\>, or null if there were none. |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [FeatureInfo](../android/content/pm/FeatureInfo.md)!\>? | `https://developer.android.com/reference/kotlin/android/content/pm/PackageInfo#reqFeatures:kotlin.Array` Features that this application has requested. |
| --- | --- |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>? | `https://developer.android.com/reference/kotlin/android/content/pm/PackageInfo#requestedPermissions:kotlin.Array` Array of all `https://developer.android.com/reference/kotlin/android/R.styleable.html#AndroidManifestUsesPermission:kotlin.IntArray` tags included under \<manifest\>, or null if there were none. |
| [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)? | `https://developer.android.com/reference/kotlin/android/content/pm/PackageInfo#requestedPermissionsFlags:kotlin.IntArray` Array of flags of all `https://developer.android.com/reference/kotlin/android/R.styleable.html#AndroidManifestUsesPermission:kotlin.IntArray` tags included under \<manifest\>, or null if there were none. |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [ServiceInfo](../android/content/pm/ServiceInfo.md)!\>? | `https://developer.android.com/reference/kotlin/android/content/pm/PackageInfo#services:kotlin.Array` Array of all `https://developer.android.com/reference/kotlin/android/R.styleable.html#AndroidManifestService:kotlin.IntArray` tags included under \<application\>, or null if there were none. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | `https://developer.android.com/reference/kotlin/android/content/pm/PackageInfo#sharedUserId:kotlin.String` The shared user ID name of this package, as specified by the \<manifest\> tag's `https://developer.android.com/reference/kotlin/android/R.styleable.html#AndroidManifest_sharedUserId:kotlin.Int` attribute. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageInfo#sharedUserLabel:kotlin.Int` The shared user ID label of this package, as specified by the \<manifest\> tag's `https://developer.android.com/reference/kotlin/android/R.styleable.html#AndroidManifest_sharedUserLabel:kotlin.Int` attribute. |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Signature](../android/content/pm/Signature.md)!\>? | `https://developer.android.com/reference/kotlin/android/content/pm/PackageInfo#signatures:kotlin.Array` Array of all signatures read from the package file. |
| --- | --- |
| [SigningInfo](../android/content/pm/SigningInfo.md)? | `https://developer.android.com/reference/kotlin/android/content/pm/PackageInfo#signingInfo:android.content.pm.SigningInfo` Signing information read from the package file, potentially including past signing certificates no longer used after signing certificate rotation. |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | `https://developer.android.com/reference/kotlin/android/content/pm/PackageInfo#splitNames:kotlin.Array` The names of any installed split APKs for this package. |
| [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageInfo#splitRevisionCodes:kotlin.IntArray` The revision number of any split APKs for this package, as specified by the \<manifest\> tag's `https://developer.android.com/reference/kotlin/android/R.styleable.html#AndroidManifest_revisionCode:kotlin.Int` attribute. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageInfo#versionCode:kotlin.Int` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | `https://developer.android.com/reference/kotlin/android/content/pm/PackageInfo#versionName:kotlin.String` The version name of this package, as specified by the \<manifest\> tag's `https://developer.android.com/reference/kotlin/android/R.styleable.html#AndroidManifest_versionName:kotlin.Int` attribute, or null if there was none. |

## Constants

### INSTALL_LOCATION_AUTO

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val INSTALL_LOCATION_AUTO: Int
```

Constant corresponding to `auto` in the `https://developer.android.com/reference/kotlin/android/R.attr.html#installLocation:kotlin.Int` attribute.

 Value: 0

### INSTALL_LOCATION_INTERNAL_ONLY

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val INSTALL_LOCATION_INTERNAL_ONLY: Int
```

Constant corresponding to `internalOnly` in the `https://developer.android.com/reference/kotlin/android/R.attr.html#installLocation:kotlin.Int` attribute.

 Value: 1

### INSTALL_LOCATION_PREFER_EXTERNAL

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val INSTALL_LOCATION_PREFER_EXTERNAL: Int
```

Constant corresponding to `preferExternal` in the `https://developer.android.com/reference/kotlin/android/R.attr.html#installLocation:kotlin.Int` attribute.

 Value: 2

### REQUESTED_PERMISSION_GRANTED

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val REQUESTED_PERMISSION_GRANTED: Int
```

Flag for `https://developer.android.com/reference/kotlin/android/content/pm/PackageInfo#requestedPermissionsFlags:kotlin.IntArray`: the requested permission is currently granted to the application.

 Value: 2

### REQUESTED_PERMISSION_IMPLICIT

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val REQUESTED_PERMISSION_IMPLICIT: Int
```

Flag for `https://developer.android.com/reference/kotlin/android/content/pm/PackageInfo#requestedPermissionsFlags:kotlin.IntArray`: the requested permission was not explicitly requested via uses-permission, but was instead implicitly requested (e.g., for version compatibility reasons).

 Value: 4

### REQUESTED_PERMISSION_NEVER_FOR_LOCATION

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val REQUESTED_PERMISSION_NEVER_FOR_LOCATION: Int
```

Flag for `https://developer.android.com/reference/kotlin/android/content/pm/PackageInfo#requestedPermissionsFlags:kotlin.IntArray`: the requested permission has declared `neverForLocation` in their manifest as a strong assertion by a developer that they will never use this permission to derive the physical location of the device, regardless of `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String` and/or `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_COARSE_LOCATION:kotlin.String` being granted.

 Value: 65536

### REQUESTED_PERMISSION_ONLY_FOR_LOCATION_BUTTON

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val REQUESTED_PERMISSION_ONLY_FOR_LOCATION_BUTTON: Int
```

Flag for `https://developer.android.com/reference/kotlin/android/content/pm/PackageInfo#requestedPermissionsFlags:kotlin.IntArray`: It only applies to `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String`. When this flag is set, apps cannot request that permission through `https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)`, and can only use location button to obtain it temporarily.

 Value: 131072

### REQUESTED_PERMISSION_PRIVATE_COMPUTE_CORE_ONLY

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val REQUESTED_PERMISSION_PRIVATE_COMPUTE_CORE_ONLY: Int
```

Flag for `https://developer.android.com/reference/kotlin/android/content/pm/PackageInfo#requestedPermissionsFlags:kotlin.IntArray`: the requested permission is restricted to the Private Compute Core.

 Value: 262144

## Public constructors

### PackageInfo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
PackageInfo()
```

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

### getApexPackageName

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getApexPackageName(): String?
```

If the package is an APEX package (i.e. the value of `https://developer.android.com/reference/kotlin/android/content/pm/PackageInfo#isApex:kotlin.Boolean` is true), returns the package name of the APEX. If the package is one APK-in-APEX app, returns the package name of the parent APEX that contains the app. If the package is not one of the above two cases, returns `null`.

### getArchiveTimeMillis

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getArchiveTimeMillis(): Long
```

Returns the time at which the app was archived for the user. Units are as per `https://developer.android.com/reference/kotlin/java/lang/System.html#currentTimeMillis()`. 
Value is a non-negative timestamp measured as the number of milliseconds since 1970-01-01T00:00:00Z.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | Value is a non-negative timestamp measured as the number of milliseconds since 1970-01-01T00:00:00Z. |

### getLongVersionCode

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getLongVersionCode(): Long
```

Return `https://developer.android.com/reference/kotlin/android/R.styleable.html#AndroidManifest_versionCode:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/R.styleable.html#AndroidManifest_versionCodeMajor:kotlin.Int` combined together as a single long value. The `https://developer.android.com/reference/kotlin/android/R.styleable.html#AndroidManifest_versionCodeMajor:kotlin.Int` is placed in the upper 32 bits.

### isAppMetadataVerified

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isAppMetadataVerified(): Boolean
```

Returns the verification status of the App Metadata of the package. This status is set at the package installation time by the developer verification service provider.

### setLongVersionCode

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setLongVersionCode(longVersionCode: Long): Unit
```

Set the full version code in this PackageInfo, updating `https://developer.android.com/reference/kotlin/android/content/pm/PackageInfo#versionCode:kotlin.Int` with the lower bits.
**See Also**

- `https://developer.android.com/reference/kotlin/android/content/pm/PackageInfo#getLongVersionCode()`

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
static val CREATOR: Parcelable.Creator<PackageInfo!>
```

### activities

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var activities: Array<ActivityInfo!>?
```

Array of all `https://developer.android.com/reference/kotlin/android/R.styleable.html#AndroidManifestActivity:kotlin.IntArray` tags included under \<application\>, or null if there were none. This is only filled in if the flag `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#GET_ACTIVITIES:kotlin.Int` was set.

### applicationInfo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var applicationInfo: ApplicationInfo?
```

Information collected from the \<application\> tag, or null if there was none.

### attributions

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var attributions: Array<Attribution!>?
```

Array of all `https://developer.android.com/reference/kotlin/android/R.styleable.html#AndroidManifestAttribution:kotlin.IntArray` tags included under \<manifest\>, or null if there were none. This is only filled if the flag `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#GET_ATTRIBUTIONS_LONG:kotlin.Long` was set.

### baseRevisionCode

Added in [API level 22](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var baseRevisionCode: Int
```

The revision number of the base APK for this package, as specified by the \<manifest\> tag's `https://developer.android.com/reference/kotlin/android/R.styleable.html#AndroidManifest_revisionCode:kotlin.Int` attribute.

### configPreferences

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var configPreferences: Array<ConfigurationInfo!>?
```

Application specified preferred configuration `https://developer.android.com/reference/kotlin/android/R.styleable.html#AndroidManifestUsesConfiguration:kotlin.IntArray` tags included under \<manifest\>, or null if there were none. This is only filled in if the flag `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#GET_CONFIGURATIONS:kotlin.Int` was set.

### featureGroups

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var featureGroups: Array<FeatureGroupInfo!>?
```

Groups of features that this application has requested. Each group contains a set of features that are required. A device must match the features listed in `https://developer.android.com/reference/kotlin/android/content/pm/PackageInfo#reqFeatures:kotlin.Array` and one or more FeatureGroups in order to have satisfied the feature requirement.
**See Also**

- `https://developer.android.com/reference/kotlin/android/content/pm/FeatureInfo#FLAG_REQUIRED:kotlin.Int`

### firstInstallTime

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var firstInstallTime: Long
```

The time at which the app was first installed. Units are as per `https://developer.android.com/reference/kotlin/java/lang/System.html#currentTimeMillis()`.

### gids

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var gids: IntArray?
```

All kernel group-IDs that have been assigned to this package. This is only filled in if the flag `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#GET_GIDS:kotlin.Int` was set.

### installLocation

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var installLocation: Int
```

The install location requested by the package. From the `https://developer.android.com/reference/kotlin/android/R.attr.html#installLocation:kotlin.Int` attribute, one of `https://developer.android.com/reference/kotlin/android/content/pm/PackageInfo#INSTALL_LOCATION_AUTO:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/content/pm/PackageInfo#INSTALL_LOCATION_INTERNAL_ONLY:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/content/pm/PackageInfo#INSTALL_LOCATION_PREFER_EXTERNAL:kotlin.Int`

### instrumentation

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var instrumentation: Array<InstrumentationInfo!>?
```

Array of all `https://developer.android.com/reference/kotlin/android/R.styleable.html#AndroidManifestInstrumentation:kotlin.IntArray` tags included under \<manifest\>, or null if there were none. This is only filled in if the flag `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#GET_INSTRUMENTATION:kotlin.Int` was set.

### isApex

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var isApex: Boolean
```

Whether the package is an APEX package.

### lastUpdateTime

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var lastUpdateTime: Long
```

The time at which the app was last updated. Units are as per `https://developer.android.com/reference/kotlin/java/lang/System.html#currentTimeMillis()`.

### packageName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var packageName: String
```

The name of this package. From the \<manifest\> tag's "name" attribute.

### permissions

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var permissions: Array<PermissionInfo!>?
```

Array of all `https://developer.android.com/reference/kotlin/android/R.styleable.html#AndroidManifestPermission:kotlin.IntArray` tags included under \<manifest\>, or null if there were none. This is only filled in if the flag `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#GET_PERMISSIONS:kotlin.Int` was set.

### providers

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var providers: Array<ProviderInfo!>?
```

Array of all `https://developer.android.com/reference/kotlin/android/R.styleable.html#AndroidManifestProvider:kotlin.IntArray` tags included under \<application\>, or null if there were none. This is only filled in if the flag `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#GET_PROVIDERS:kotlin.Int` was set.

### receivers

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var receivers: Array<ActivityInfo!>?
```

Array of all `https://developer.android.com/reference/kotlin/android/R.styleable.html#AndroidManifestReceiver:kotlin.IntArray` tags included under \<application\>, or null if there were none. This is only filled in if the flag `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#GET_RECEIVERS:kotlin.Int` was set.

### reqFeatures

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var reqFeatures: Array<FeatureInfo!>?
```

Features that this application has requested.
**See Also**

- `https://developer.android.com/reference/kotlin/android/content/pm/FeatureInfo#FLAG_REQUIRED:kotlin.Int`

### requestedPermissions

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var requestedPermissions: Array<String!>?
```

Array of all `https://developer.android.com/reference/kotlin/android/R.styleable.html#AndroidManifestUsesPermission:kotlin.IntArray` tags included under \<manifest\>, or null if there were none. This is only filled in if the flag `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#GET_PERMISSIONS:kotlin.Int` was set. This list includes all permissions requested, even those that were not granted or known by the system at install time.

### requestedPermissionsFlags

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var requestedPermissionsFlags: IntArray?
```

Array of flags of all `https://developer.android.com/reference/kotlin/android/R.styleable.html#AndroidManifestUsesPermission:kotlin.IntArray` tags included under \<manifest\>, or null if there were none. This is only filled in if the flag `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#GET_PERMISSIONS:kotlin.Int` was set. Each value matches the corresponding entry in `https://developer.android.com/reference/kotlin/android/content/pm/PackageInfo#requestedPermissions:kotlin.Array`, and will have the flags `https://developer.android.com/reference/kotlin/android/content/pm/PackageInfo#REQUESTED_PERMISSION_GRANTED:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/content/pm/PackageInfo#REQUESTED_PERMISSION_IMPLICIT:kotlin.Int`, and `https://developer.android.com/reference/kotlin/android/content/pm/PackageInfo#REQUESTED_PERMISSION_NEVER_FOR_LOCATION:kotlin.Int` set as appropriate.

### services

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var services: Array<ServiceInfo!>?
```

Array of all `https://developer.android.com/reference/kotlin/android/R.styleable.html#AndroidManifestService:kotlin.IntArray` tags included under \<application\>, or null if there were none. This is only filled in if the flag `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#GET_SERVICES:kotlin.Int` was set.

### sharedUserId

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var sharedUserId: String?
```

The shared user ID name of this package, as specified by the \<manifest\> tag's `https://developer.android.com/reference/kotlin/android/R.styleable.html#AndroidManifest_sharedUserId:kotlin.Int` attribute.

### sharedUserLabel

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var sharedUserLabel: Int
```

The shared user ID label of this package, as specified by the \<manifest\> tag's `https://developer.android.com/reference/kotlin/android/R.styleable.html#AndroidManifest_sharedUserLabel:kotlin.Int` attribute.

### signatures

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var signatures: Array<Signature!>?
```

**Deprecated:** *use `signingInfo` instead*

Array of all signatures read from the package file. This is only filled in if the flag `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#GET_SIGNATURES:kotlin.Int` was set. A package must be signed with at least one certificate which is at position zero. The package can be signed with additional certificates which appear as subsequent entries. **Note:** Signature ordering is not guaranteed to be stable which means that a package signed with certificates A and B is equivalent to being signed with certificates B and A. This means that in case multiple signatures are reported you cannot assume the one at the first position to be the same across updates. **Deprecated** This has been replaced by the `https://developer.android.com/reference/kotlin/android/content/pm/PackageInfo#signingInfo:android.content.pm.SigningInfo` field, which takes into account signing certificate rotation. For backwards compatibility in the event of signing certificate rotation, this will return the oldest reported signing certificate, so that an application will appear to callers as though no rotation occurred.

### signingInfo

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var signingInfo: SigningInfo?
```

Signing information read from the package file, potentially including past signing certificates no longer used after signing certificate rotation. This is only filled in if the flag `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#GET_SIGNING_CERTIFICATES:kotlin.Int` was set. Use this field instead of the deprecated `signatures` field. See `https://developer.android.com/reference/kotlin/android/content/pm/SigningInfo` for more information on its contents.

### splitNames

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var splitNames: Array<String!>
```

The names of any installed split APKs for this package.

### splitRevisionCodes

Added in [API level 22](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var splitRevisionCodes: IntArray
```

The revision number of any split APKs for this package, as specified by the \<manifest\> tag's `https://developer.android.com/reference/kotlin/android/R.styleable.html#AndroidManifest_revisionCode:kotlin.Int` attribute. Indexes are a 1:1 mapping against `https://developer.android.com/reference/kotlin/android/content/pm/PackageInfo#splitNames:kotlin.Array`.

### versionCode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var versionCode: Int
```

**Deprecated:** *Use `https://developer.android.com/reference/kotlin/android/content/pm/PackageInfo#getLongVersionCode()` instead, which includes both this and the additional `https://developer.android.com/reference/kotlin/android/R.styleable.html#AndroidManifest_versionCodeMajor:kotlin.Int` attribute. The version number of this package, as specified by the \<manifest\> tag's `https://developer.android.com/reference/kotlin/android/R.styleable.html#AndroidManifest_versionCode:kotlin.Int` attribute.*
**See Also**

- `https://developer.android.com/reference/kotlin/android/content/pm/PackageInfo#getLongVersionCode()`

### versionName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var versionName: String?
```

The version name of this package, as specified by the \<manifest\> tag's `https://developer.android.com/reference/kotlin/android/R.styleable.html#AndroidManifest_versionName:kotlin.Int` attribute, or null if there was none.
