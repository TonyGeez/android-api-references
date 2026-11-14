# InstallSourceInfo

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# InstallSourceInfo

Kotlin | [Java](https://developer.android.com/reference/android/content/pm/InstallSourceInfo "View this page in Java") 

```
class InstallSourceInfo : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.content.pm.InstallSourceInfo](https://developer.android.com/reference/kotlin/android/content/pm/InstallSourceInfo#) |

Information about how an app was installed.

## Summary

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/content/pm/InstallSourceInfo#describeContents())`()` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getInitiatingPackageName](https://developer.android.com/reference/kotlin/android/content/pm/InstallSourceInfo#getInitiatingPackageName())`()` The name of the package that requested the installation, or null if not available. |
| [SigningInfo](https://developer.android.com/reference/kotlin/android/content/pm/SigningInfo)? | [getInitiatingPackageSigningInfo](https://developer.android.com/reference/kotlin/android/content/pm/InstallSourceInfo#getInitiatingPackageSigningInfo())`()` Information about the signing certificates used to sign the initiating package, if available. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getInstallingPackageName](https://developer.android.com/reference/kotlin/android/content/pm/InstallSourceInfo#getInstallingPackageName())`()` The name of the package responsible for the installation (the installer of record), or null if not available. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getOriginatingPackageName](https://developer.android.com/reference/kotlin/android/content/pm/InstallSourceInfo#getOriginatingPackageName())`()` The name of the package on behalf of which the initiating package requested the installation, or null if not available. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPackageSource](https://developer.android.com/reference/kotlin/android/content/pm/InstallSourceInfo#getPackageSource())`()` Information about the package source when installer installed this app. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getUpdateOwnerPackageName](https://developer.android.com/reference/kotlin/android/content/pm/InstallSourceInfo#getUpdateOwnerPackageName())`()` The name of the package that is the update owner, or null if not available. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/content/pm/InstallSourceInfo#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |

| Properties ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [InstallSourceInfo](https://developer.android.com/reference/kotlin/android/content/pm/InstallSourceInfo#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/content/pm/InstallSourceInfo#CREATOR:android.os.Parcelable.Creator) <br /> |

## Public methods

### describeContents

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### getInitiatingPackageName

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getInitiatingPackageName(): String?
```

The name of the package that requested the installation, or null if not available. This is normally the same as the installing package name. If the installing package name is changed, for example by calling [PackageManager.setInstallerPackageName(String, String)](https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#setInstallerPackageName(kotlin.String,%20kotlin.String)), the initiating package name remains unchanged. It continues to identify the actual package that performed the install or update.

Null may be returned if the app was not installed by a package (e.g. a system app) or if the initiating package has itself been uninstalled. 

### getInitiatingPackageSigningInfo

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getInitiatingPackageSigningInfo(): SigningInfo?
```

Information about the signing certificates used to sign the initiating package, if available.

| Return ||
|-----------------------------------------------------------------------------------------------|---------------------------|
| [SigningInfo](https://developer.android.com/reference/kotlin/android/content/pm/SigningInfo)? | This value may be `null`. |

### getInstallingPackageName

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getInstallingPackageName(): String?
```

The name of the package responsible for the installation (the installer of record), or null if not available. Note that this may differ from the initiating package name and can be modified via [PackageManager.setInstallerPackageName(String, String)](https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#setInstallerPackageName(kotlin.String,%20kotlin.String)).

Null may be returned if the app was not installed by a package (e.g. a system app or an app installed via adb) or if the installing package has itself been uninstalled. 

### getOriginatingPackageName

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getOriginatingPackageName(): String?
```

The name of the package on behalf of which the initiating package requested the installation, or null if not available.

For example if a downloaded APK is installed via the Package Installer this could be the app that performed the download. This value is provided by the initiating package and not verified by the framework.

Note that the `InstallSourceInfo` returned by [PackageManager.getInstallSourceInfo(String)](https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#getInstallSourceInfo(kotlin.String)) will not have this information available unless the calling application holds the INSTALL_PACKAGES permission. 

### getPackageSource

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPackageSource(): Int
```

Information about the package source when installer installed this app.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.content.pm.PackageInstaller#PACKAGE_SOURCE_UNSPECIFIED](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#PACKAGE_SOURCE_UNSPECIFIED:kotlin.Int), [android.content.pm.PackageInstaller#PACKAGE_SOURCE_STORE](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#PACKAGE_SOURCE_STORE:kotlin.Int), [android.content.pm.PackageInstaller#PACKAGE_SOURCE_LOCAL_FILE](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#PACKAGE_SOURCE_LOCAL_FILE:kotlin.Int), [android.content.pm.PackageInstaller#PACKAGE_SOURCE_DOWNLOADED_FILE](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#PACKAGE_SOURCE_DOWNLOADED_FILE:kotlin.Int), or [android.content.pm.PackageInstaller#PACKAGE_SOURCE_OTHER](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#PACKAGE_SOURCE_OTHER:kotlin.Int) |

### getUpdateOwnerPackageName

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getUpdateOwnerPackageName(): String?
```

The name of the package that is the update owner, or null if not available. This indicates the update ownership enforcement is enabled for this app, and which package is the update owner. Returns null if the update ownership enforcement is disabled for the app. 
**See Also**

- [android.content.pm.PackageInstaller.SessionParams#setRequestUpdateOwnership](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller.SessionParams#setRequestUpdateOwnership(kotlin.Boolean)) 

### writeToParcel

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

Flatten this object in to a Parcel.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#): This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either `0` or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<InstallSourceInfo!>
```
