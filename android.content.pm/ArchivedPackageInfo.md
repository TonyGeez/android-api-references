# ArchivedPackageInfo

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ArchivedPackageInfo

Kotlin| [Java](https://developer.android.com/reference/android/content/pm/ArchivedPackageInfo "View this page in Java") 
| --- | --- |

```
class ArchivedPackageInfo
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.content.pm.ArchivedPackageInfo](https://developer.android.com/reference/kotlin/android/content/pm/ArchivedPackageInfo#) |

Contains fields required for archived package installation, i.e. installation without an APK.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ArchivedPackageInfo](https://developer.android.com/reference/kotlin/android/content/pm/ArchivedPackageInfo#ArchivedPackageInfo(kotlin.String,%20android.content.pm.SigningInfo,%20kotlin.collections.MutableList))`(`packageName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `signingInfo:` ` [SigningInfo](https://developer.android.com/reference/kotlin/android/content/pm/SigningInfo)`, `launcherActivities:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [ArchivedActivityInfo](https://developer.android.com/reference/kotlin/android/content/pm/ArchivedActivityInfo)!>`)` <br /> |

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getDefaultToDeviceProtectedStorage](https://developer.android.com/reference/kotlin/android/content/pm/ArchivedPackageInfo#getDefaultToDeviceProtectedStorage())`()` Package data will default to device protected storage. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [ArchivedActivityInfo](https://developer.android.com/reference/kotlin/android/content/pm/ArchivedActivityInfo)!\> | [getLauncherActivities](https://developer.android.com/reference/kotlin/android/content/pm/ArchivedPackageInfo#getLauncherActivities())`()` List of the package's activities that specify [Intent.ACTION_MAIN](https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_MAIN:kotlin.String) and [Intent.CATEGORY_LAUNCHER](https://developer.android.com/reference/kotlin/android/content/Intent.html#CATEGORY_LAUNCHER:kotlin.String). |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getPackageName](https://developer.android.com/reference/kotlin/android/content/pm/ArchivedPackageInfo#getPackageName())`()` Name of the package as used to identify it in the system |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getRequestLegacyExternalStorage](https://developer.android.com/reference/kotlin/android/content/pm/ArchivedPackageInfo#getRequestLegacyExternalStorage())`()` If`true`this app would like to run under the legacy storage model. |
| [SigningInfo](https://developer.android.com/reference/kotlin/android/content/pm/SigningInfo) | [getSigningInfo](https://developer.android.com/reference/kotlin/android/content/pm/ArchivedPackageInfo#getSigningInfo())`()` Signing certificates used to sign the package. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getTargetSdkVersion](https://developer.android.com/reference/kotlin/android/content/pm/ArchivedPackageInfo#getTargetSdkVersion())`()` This is the SDK version number that the application is targeting, as specified by the \<manifest\> tag's [android.R.styleable#AndroidManifestUsesSdk_targetSdkVersion](https://developer.android.com/reference/kotlin/android/R.styleable.html#AndroidManifestUsesSdk_targetSdkVersion:kotlin.Int) attribute. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getUserDataFragile](https://developer.android.com/reference/kotlin/android/content/pm/ArchivedPackageInfo#getUserDataFragile())`()` If`true`the user is prompted to keep the app's data on uninstall. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getVersionCode](https://developer.android.com/reference/kotlin/android/content/pm/ArchivedPackageInfo#getVersionCode())`()` The version number of the package, as specified by the \<manifest\>tag's [versionCode](https://developer.android.com/reference/kotlin/android/R.styleable.html#AndroidManifest_versionCode:kotlin.Int) attribute. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getVersionCodeMajor](https://developer.android.com/reference/kotlin/android/content/pm/ArchivedPackageInfo#getVersionCodeMajor())`()` The major version number of the package, as specified by the \<manifest\>tag's [versionCodeMajor](https://developer.android.com/reference/kotlin/android/R.styleable.html#AndroidManifest_versionCode:kotlin.Int) attribute. |
| --- | --- |
| [ArchivedPackageInfo](https://developer.android.com/reference/kotlin/android/content/pm/ArchivedPackageInfo#) | [setDefaultToDeviceProtectedStorage](https://developer.android.com/reference/kotlin/android/content/pm/ArchivedPackageInfo#setDefaultToDeviceProtectedStorage(kotlin.String))`(`value:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Package data will default to device protected storage. |
| [ArchivedPackageInfo](https://developer.android.com/reference/kotlin/android/content/pm/ArchivedPackageInfo#) | [setLauncherActivities](https://developer.android.com/reference/kotlin/android/content/pm/ArchivedPackageInfo#setLauncherActivities(kotlin.collections.MutableList))`(`value:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [ArchivedActivityInfo](https://developer.android.com/reference/kotlin/android/content/pm/ArchivedActivityInfo)!>`)` List of the package's activities that specify [Intent.ACTION_MAIN](https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_MAIN:kotlin.String) and [Intent.CATEGORY_LAUNCHER](https://developer.android.com/reference/kotlin/android/content/Intent.html#CATEGORY_LAUNCHER:kotlin.String). |
| [ArchivedPackageInfo](https://developer.android.com/reference/kotlin/android/content/pm/ArchivedPackageInfo#) | [setPackageName](https://developer.android.com/reference/kotlin/android/content/pm/ArchivedPackageInfo#setPackageName(kotlin.String))`(`value:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Name of the package as used to identify it in the system |
| --- | --- |
| [ArchivedPackageInfo](https://developer.android.com/reference/kotlin/android/content/pm/ArchivedPackageInfo#) | [setRequestLegacyExternalStorage](https://developer.android.com/reference/kotlin/android/content/pm/ArchivedPackageInfo#setRequestLegacyExternalStorage(kotlin.String))`(`value:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` If`true`this app would like to run under the legacy storage model. |
| [ArchivedPackageInfo](https://developer.android.com/reference/kotlin/android/content/pm/ArchivedPackageInfo#) | [setSigningInfo](https://developer.android.com/reference/kotlin/android/content/pm/ArchivedPackageInfo#setSigningInfo(android.content.pm.SigningInfo))`(`value:` ` [SigningInfo](https://developer.android.com/reference/kotlin/android/content/pm/SigningInfo)`)` Signing certificates used to sign the package. |
| [ArchivedPackageInfo](https://developer.android.com/reference/kotlin/android/content/pm/ArchivedPackageInfo#) | [setTargetSdkVersion](https://developer.android.com/reference/kotlin/android/content/pm/ArchivedPackageInfo#setTargetSdkVersion(kotlin.Int))`(`value:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` This is the SDK version number that the application is targeting, as specified by the \<manifest\> tag's [android.R.styleable#AndroidManifestUsesSdk_targetSdkVersion](https://developer.android.com/reference/kotlin/android/R.styleable.html#AndroidManifestUsesSdk_targetSdkVersion:kotlin.Int) attribute. |
| --- | --- |
| [ArchivedPackageInfo](https://developer.android.com/reference/kotlin/android/content/pm/ArchivedPackageInfo#) | [setUserDataFragile](https://developer.android.com/reference/kotlin/android/content/pm/ArchivedPackageInfo#setUserDataFragile(kotlin.String))`(`value:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` If`true`the user is prompted to keep the app's data on uninstall. |
| [ArchivedPackageInfo](https://developer.android.com/reference/kotlin/android/content/pm/ArchivedPackageInfo#) | [setVersionCode](https://developer.android.com/reference/kotlin/android/content/pm/ArchivedPackageInfo#setVersionCode(kotlin.Int))`(`value:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` The version number of the package, as specified by the \<manifest\>tag's [versionCode](https://developer.android.com/reference/kotlin/android/R.styleable.html#AndroidManifest_versionCode:kotlin.Int) attribute. |
| [ArchivedPackageInfo](https://developer.android.com/reference/kotlin/android/content/pm/ArchivedPackageInfo#) | [setVersionCodeMajor](https://developer.android.com/reference/kotlin/android/content/pm/ArchivedPackageInfo#setVersionCodeMajor(kotlin.Int))`(`value:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` The major version number of the package, as specified by the \<manifest\>tag's [versionCodeMajor](https://developer.android.com/reference/kotlin/android/R.styleable.html#AndroidManifest_versionCode:kotlin.Int) attribute. |
| --- | --- |

## Public constructors

### ArchivedPackageInfo

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ArchivedPackageInfo(
    packageName: String, 
    signingInfo: SigningInfo, 
    launcherActivities: MutableList<ArchivedActivityInfo!>)
```

| Parameters ||
|----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):This value cannot be`null`. |
| `signingInfo` | [SigningInfo](https://developer.android.com/reference/kotlin/android/content/pm/SigningInfo):This value cannot be`null`. |
| `launcherActivities` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [ArchivedActivityInfo](https://developer.android.com/reference/kotlin/android/content/pm/ArchivedActivityInfo)!\>:This value cannot be`null`. |
| --- | --- |

## Public methods

### getDefaultToDeviceProtectedStorage

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDefaultToDeviceProtectedStorage(): String?
```

Package data will default to device protected storage. Specified by the \<manifest\> tag's [android.R.styleable#AndroidManifestApplication_defaultToDeviceProtectedStorage](https://developer.android.com/reference/kotlin/android/R.styleable.html#AndroidManifestApplication_defaultToDeviceProtectedStorage:kotlin.Int) attribute.

| Return ||
|-----------------------------------------------------------------------------------|--------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | This value may be`null`. |

### getLauncherActivities

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getLauncherActivities(): MutableList<ArchivedActivityInfo!>
```

List of the package's activities that specify [Intent.ACTION_MAIN](https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_MAIN:kotlin.String) and [Intent.CATEGORY_LAUNCHER](https://developer.android.com/reference/kotlin/android/content/Intent.html#CATEGORY_LAUNCHER:kotlin.String).

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [ArchivedActivityInfo](https://developer.android.com/reference/kotlin/android/content/pm/ArchivedActivityInfo)!> | This value cannot be`null`. |

**See Also**

- [android.content.pm.LauncherApps#getActivityList](https://developer.android.com/reference/kotlin/android/content/pm/LauncherApps#getActivityList(kotlin.String,%20android.os.UserHandle)) 

### getPackageName

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPackageName(): String
```

Name of the package as used to identify it in the system

| Return ||
|----------------------------------------------------------------------------------|-----------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | This value cannot be`null`. |

### getRequestLegacyExternalStorage

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getRequestLegacyExternalStorage(): String?
```

If`true`this app would like to run under the legacy storage model. Specified by the \<manifest\> tag's [android.R.styleable#AndroidManifestApplication_requestLegacyExternalStorage](https://developer.android.com/reference/kotlin/android/R.styleable.html#AndroidManifestApplication_requestLegacyExternalStorage:kotlin.Int) attribute.

| Return ||
|-----------------------------------------------------------------------------------|--------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | This value may be`null`. |

### getSigningInfo

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSigningInfo(): SigningInfo
```

Signing certificates used to sign the package.

| Return ||
|----------------------------------------------------------------------------------------------|-----------------------------|
| [SigningInfo](https://developer.android.com/reference/kotlin/android/content/pm/SigningInfo) | This value cannot be`null`. |

### getTargetSdkVersion

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTargetSdkVersion(): Int
```

This is the SDK version number that the application is targeting, as specified by the \<manifest\> tag's [android.R.styleable#AndroidManifestUsesSdk_targetSdkVersion](https://developer.android.com/reference/kotlin/android/R.styleable.html#AndroidManifestUsesSdk_targetSdkVersion:kotlin.Int) attribute. 

### getUserDataFragile

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getUserDataFragile(): String?
```

If`true`the user is prompted to keep the app's data on uninstall. Specified by the \<manifest\> tag's [android.R.styleable#AndroidManifestApplication_hasFragileUserData](https://developer.android.com/reference/kotlin/android/R.styleable.html#AndroidManifestApplication_hasFragileUserData:kotlin.Int) attribute.

| Return ||
|-----------------------------------------------------------------------------------|--------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | This value may be`null`. |

### getVersionCode

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getVersionCode(): Int
```

The version number of the package, as specified by the \<manifest\>tag's [versionCode](https://developer.android.com/reference/kotlin/android/R.styleable.html#AndroidManifest_versionCode:kotlin.Int) attribute. 

### getVersionCodeMajor

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getVersionCodeMajor(): Int
```

The major version number of the package, as specified by the \<manifest\>tag's [versionCodeMajor](https://developer.android.com/reference/kotlin/android/R.styleable.html#AndroidManifest_versionCode:kotlin.Int) attribute. 

### setDefaultToDeviceProtectedStorage

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setDefaultToDeviceProtectedStorage(value: String): ArchivedPackageInfo
```

Package data will default to device protected storage. Specified by the \<manifest\> tag's [android.R.styleable#AndroidManifestApplication_defaultToDeviceProtectedStorage](https://developer.android.com/reference/kotlin/android/R.styleable.html#AndroidManifestApplication_defaultToDeviceProtectedStorage:kotlin.Int) attribute.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------|
| `value` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):This value cannot be`null`. |

| Return ||
|---------------------------------------------------------------------------------------------------------------|-----------------------------|
| [ArchivedPackageInfo](https://developer.android.com/reference/kotlin/android/content/pm/ArchivedPackageInfo#) | This value cannot be`null`. |

### setLauncherActivities

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setLauncherActivities(value: MutableList<ArchivedActivityInfo!>): ArchivedPackageInfo
```

List of the package's activities that specify [Intent.ACTION_MAIN](https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_MAIN:kotlin.String) and [Intent.CATEGORY_LAUNCHER](https://developer.android.com/reference/kotlin/android/content/Intent.html#CATEGORY_LAUNCHER:kotlin.String).

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `value` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [ArchivedActivityInfo](https://developer.android.com/reference/kotlin/android/content/pm/ArchivedActivityInfo)!\>:This value cannot be`null`. |

| Return ||
|---------------------------------------------------------------------------------------------------------------|-----------------------------|
| [ArchivedPackageInfo](https://developer.android.com/reference/kotlin/android/content/pm/ArchivedPackageInfo#) | This value cannot be`null`. |

**See Also**

- [android.content.pm.LauncherApps#getActivityList](https://developer.android.com/reference/kotlin/android/content/pm/LauncherApps#getActivityList(kotlin.String,%20android.os.UserHandle)) 

### setPackageName

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setPackageName(value: String): ArchivedPackageInfo
```

Name of the package as used to identify it in the system

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------|
| `value` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):This value cannot be`null`. |

| Return ||
|---------------------------------------------------------------------------------------------------------------|-----------------------------|
| [ArchivedPackageInfo](https://developer.android.com/reference/kotlin/android/content/pm/ArchivedPackageInfo#) | This value cannot be`null`. |

### setRequestLegacyExternalStorage

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setRequestLegacyExternalStorage(value: String): ArchivedPackageInfo
```

If`true`this app would like to run under the legacy storage model. Specified by the \<manifest\> tag's [android.R.styleable#AndroidManifestApplication_requestLegacyExternalStorage](https://developer.android.com/reference/kotlin/android/R.styleable.html#AndroidManifestApplication_requestLegacyExternalStorage:kotlin.Int) attribute.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------|
| `value` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):This value cannot be`null`. |

| Return ||
|---------------------------------------------------------------------------------------------------------------|-----------------------------|
| [ArchivedPackageInfo](https://developer.android.com/reference/kotlin/android/content/pm/ArchivedPackageInfo#) | This value cannot be`null`. |

### setSigningInfo

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setSigningInfo(value: SigningInfo): ArchivedPackageInfo
```

Signing certificates used to sign the package.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------|
| `value` | [SigningInfo](https://developer.android.com/reference/kotlin/android/content/pm/SigningInfo):This value cannot be`null`. |

| Return ||
|---------------------------------------------------------------------------------------------------------------|-----------------------------|
| [ArchivedPackageInfo](https://developer.android.com/reference/kotlin/android/content/pm/ArchivedPackageInfo#) | This value cannot be`null`. |

### setTargetSdkVersion

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setTargetSdkVersion(value: Int): ArchivedPackageInfo
```

This is the SDK version number that the application is targeting, as specified by the \<manifest\> tag's [android.R.styleable#AndroidManifestUsesSdk_targetSdkVersion](https://developer.android.com/reference/kotlin/android/R.styleable.html#AndroidManifestUsesSdk_targetSdkVersion:kotlin.Int) attribute.

| Return ||
|---------------------------------------------------------------------------------------------------------------|-----------------------------|
| [ArchivedPackageInfo](https://developer.android.com/reference/kotlin/android/content/pm/ArchivedPackageInfo#) | This value cannot be`null`. |

### setUserDataFragile

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setUserDataFragile(value: String): ArchivedPackageInfo
```

If`true`the user is prompted to keep the app's data on uninstall. Specified by the \<manifest\> tag's [android.R.styleable#AndroidManifestApplication_hasFragileUserData](https://developer.android.com/reference/kotlin/android/R.styleable.html#AndroidManifestApplication_hasFragileUserData:kotlin.Int) attribute.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------|
| `value` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):This value cannot be`null`. |

| Return ||
|---------------------------------------------------------------------------------------------------------------|-----------------------------|
| [ArchivedPackageInfo](https://developer.android.com/reference/kotlin/android/content/pm/ArchivedPackageInfo#) | This value cannot be`null`. |

### setVersionCode

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setVersionCode(value: Int): ArchivedPackageInfo
```

The version number of the package, as specified by the \<manifest\>tag's [versionCode](https://developer.android.com/reference/kotlin/android/R.styleable.html#AndroidManifest_versionCode:kotlin.Int) attribute.

| Return ||
|---------------------------------------------------------------------------------------------------------------|-----------------------------|
| [ArchivedPackageInfo](https://developer.android.com/reference/kotlin/android/content/pm/ArchivedPackageInfo#) | This value cannot be`null`. |

### setVersionCodeMajor

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setVersionCodeMajor(value: Int): ArchivedPackageInfo
```

The major version number of the package, as specified by the \<manifest\>tag's [versionCodeMajor](https://developer.android.com/reference/kotlin/android/R.styleable.html#AndroidManifest_versionCode:kotlin.Int) attribute.

| Return ||
|---------------------------------------------------------------------------------------------------------------|-----------------------------|
| [ArchivedPackageInfo](https://developer.android.com/reference/kotlin/android/content/pm/ArchivedPackageInfo#) | This value cannot be`null`. |
