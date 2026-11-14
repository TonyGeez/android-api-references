# InstallSourceInfo

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# InstallSourceInfo

Kotlin | [Java](InstallSourceInfo.md) 
| --- | --- |

```
class InstallSourceInfo : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.content.pm.InstallSourceInfo](InstallSourceInfo.md) |

Information about how an app was installed.

## Summary

| Inherited constants ||
|---|---|
| From class [Parcelable](../android.os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) Descriptor bit used with [describeContents()](../android.os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md) Flag for use with [writeToParcel](../android.os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](InstallSourceInfo.md))`()` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getInitiatingPackageName](InstallSourceInfo.md))`()` The name of the package that requested the installation, or null if not available. |
| [SigningInfo](SigningInfo.md)? | [getInitiatingPackageSigningInfo](InstallSourceInfo.md))`()` Information about the signing certificates used to sign the initiating package, if available. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getInstallingPackageName](InstallSourceInfo.md))`()` The name of the package responsible for the installation (the installer of record), or null if not available. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getOriginatingPackageName](InstallSourceInfo.md))`()` The name of the package on behalf of which the initiating package requested the installation, or null if not available. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPackageSource](InstallSourceInfo.md))`()` Information about the package source when installer installed this app. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getUpdateOwnerPackageName](InstallSourceInfo.md))`()` The name of the package that is the update owner, or null if not available. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](InstallSourceInfo.md))`(`dest:` ` [Parcel](../android.os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |

| Properties ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [InstallSourceInfo](InstallSourceInfo.md)!\> | [CREATOR](InstallSourceInfo.md) <br /> |

## Public methods

### describeContents

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) |

### getInitiatingPackageName

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getInitiatingPackageName(): String?
```

The name of the package that requested the installation, or null if not available. This is normally the same as the installing package name. If the installing package name is changed, for example by calling [PackageManager.setInstallerPackageName(String, String)](PackageManager.md)), the initiating package name remains unchanged. It continues to identify the actual package that performed the install or update.

Null may be returned if the app was not installed by a package (e.g. a system app) or if the initiating package has itself been uninstalled. 

### getInitiatingPackageSigningInfo

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getInitiatingPackageSigningInfo(): SigningInfo?
```

Information about the signing certificates used to sign the initiating package, if available.

| Return ||
|-----------------------------------------------------------------------------------------------|---------------------------|
| [SigningInfo](SigningInfo.md)? | This value may be `null`. |

### getInstallingPackageName

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getInstallingPackageName(): String?
```

The name of the package responsible for the installation (the installer of record), or null if not available. Note that this may differ from the initiating package name and can be modified via [PackageManager.setInstallerPackageName(String, String)](PackageManager.md)).

Null may be returned if the app was not installed by a package (e.g. a system app or an app installed via adb) or if the installing package has itself been uninstalled. 

### getOriginatingPackageName

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getOriginatingPackageName(): String?
```

The name of the package on behalf of which the initiating package requested the installation, or null if not available.

For example if a downloaded APK is installed via the Package Installer this could be the app that performed the download. This value is provided by the initiating package and not verified by the framework.

Note that the `InstallSourceInfo` returned by [PackageManager.getInstallSourceInfo(String)](PackageManager.md)) will not have this information available unless the calling application holds the INSTALL_PACKAGES permission. 

### getPackageSource

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPackageSource(): Int
```

Information about the package source when installer installed this app.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.content.pm.PackageInstaller#PACKAGE_SOURCE_UNSPECIFIED](PackageInstaller.md), [android.content.pm.PackageInstaller#PACKAGE_SOURCE_STORE](PackageInstaller.md), [android.content.pm.PackageInstaller#PACKAGE_SOURCE_LOCAL_FILE](PackageInstaller.md), [android.content.pm.PackageInstaller#PACKAGE_SOURCE_DOWNLOADED_FILE](PackageInstaller.md), or [android.content.pm.PackageInstaller#PACKAGE_SOURCE_OTHER](PackageInstaller.md) |

### getUpdateOwnerPackageName

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getUpdateOwnerPackageName(): String?
```

The name of the package that is the update owner, or null if not available. This indicates the update ownership enforcement is enabled for this app, and which package is the update owner. Returns null if the update ownership enforcement is disabled for the app. 
**See Also**

- [android.content.pm.PackageInstaller.SessionParams#setRequestUpdateOwnership](../android/content/pm/PackageInstaller.SessionParams.md)) 

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
| `dest` | [Parcel](../android.os/Parcel.md): This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md). Value is either `0` or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<InstallSourceInfo!>
```
