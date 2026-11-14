# ArchivedPackageInfo

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ArchivedPackageInfo

Kotlin| [Java](../android/content/pm/ArchivedPackageInfo.md) 
| --- | --- |

```
class ArchivedPackageInfo
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.content.pm.ArchivedPackageInfo](../android/content/pm/ArchivedPackageInfo.md) |

Contains fields required for archived package installation, i.e. installation without an APK.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ArchivedPackageInfo](../android/content/pm/ArchivedPackageInfo.md))`(`packageName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `signingInfo:` ` [SigningInfo](../android/content/pm/SigningInfo.md)`, `launcherActivities:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [ArchivedActivityInfo](../android/content/pm/ArchivedActivityInfo.md)!>`)` <br /> |

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getDefaultToDeviceProtectedStorage](../android/content/pm/ArchivedPackageInfo.md))`()` Package data will default to device protected storage. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [ArchivedActivityInfo](../android/content/pm/ArchivedActivityInfo.md)!\> | [getLauncherActivities](../android/content/pm/ArchivedPackageInfo.md))`()` List of the package's activities that specify [Intent.ACTION_MAIN](../android/content/Intent.md) and [Intent.CATEGORY_LAUNCHER](../android/content/Intent.md). |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getPackageName](../android/content/pm/ArchivedPackageInfo.md))`()` Name of the package as used to identify it in the system |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getRequestLegacyExternalStorage](../android/content/pm/ArchivedPackageInfo.md))`()` If`true`this app would like to run under the legacy storage model. |
| [SigningInfo](../android/content/pm/SigningInfo.md) | [getSigningInfo](../android/content/pm/ArchivedPackageInfo.md))`()` Signing certificates used to sign the package. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getTargetSdkVersion](../android/content/pm/ArchivedPackageInfo.md))`()` This is the SDK version number that the application is targeting, as specified by the \<manifest\> tag's [android.R.styleable#AndroidManifestUsesSdk_targetSdkVersion](../android/R.styleable.md) attribute. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getUserDataFragile](../android/content/pm/ArchivedPackageInfo.md))`()` If`true`the user is prompted to keep the app's data on uninstall. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getVersionCode](../android/content/pm/ArchivedPackageInfo.md))`()` The version number of the package, as specified by the \<manifest\>tag's [versionCode](../android/R.styleable.md) attribute. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getVersionCodeMajor](../android/content/pm/ArchivedPackageInfo.md))`()` The major version number of the package, as specified by the \<manifest\>tag's [versionCodeMajor](../android/R.styleable.md) attribute. |
| --- | --- |
| [ArchivedPackageInfo](../android/content/pm/ArchivedPackageInfo.md) | [setDefaultToDeviceProtectedStorage](../android/content/pm/ArchivedPackageInfo.md))`(`value:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Package data will default to device protected storage. |
| [ArchivedPackageInfo](../android/content/pm/ArchivedPackageInfo.md) | [setLauncherActivities](../android/content/pm/ArchivedPackageInfo.md))`(`value:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [ArchivedActivityInfo](../android/content/pm/ArchivedActivityInfo.md)!>`)` List of the package's activities that specify [Intent.ACTION_MAIN](../android/content/Intent.md) and [Intent.CATEGORY_LAUNCHER](../android/content/Intent.md). |
| [ArchivedPackageInfo](../android/content/pm/ArchivedPackageInfo.md) | [setPackageName](../android/content/pm/ArchivedPackageInfo.md))`(`value:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Name of the package as used to identify it in the system |
| --- | --- |
| [ArchivedPackageInfo](../android/content/pm/ArchivedPackageInfo.md) | [setRequestLegacyExternalStorage](../android/content/pm/ArchivedPackageInfo.md))`(`value:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` If`true`this app would like to run under the legacy storage model. |
| [ArchivedPackageInfo](../android/content/pm/ArchivedPackageInfo.md) | [setSigningInfo](../android/content/pm/ArchivedPackageInfo.md))`(`value:` ` [SigningInfo](../android/content/pm/SigningInfo.md)`)` Signing certificates used to sign the package. |
| [ArchivedPackageInfo](../android/content/pm/ArchivedPackageInfo.md) | [setTargetSdkVersion](../android/content/pm/ArchivedPackageInfo.md))`(`value:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` This is the SDK version number that the application is targeting, as specified by the \<manifest\> tag's [android.R.styleable#AndroidManifestUsesSdk_targetSdkVersion](../android/R.styleable.md) attribute. |
| --- | --- |
| [ArchivedPackageInfo](../android/content/pm/ArchivedPackageInfo.md) | [setUserDataFragile](../android/content/pm/ArchivedPackageInfo.md))`(`value:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` If`true`the user is prompted to keep the app's data on uninstall. |
| [ArchivedPackageInfo](../android/content/pm/ArchivedPackageInfo.md) | [setVersionCode](../android/content/pm/ArchivedPackageInfo.md))`(`value:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` The version number of the package, as specified by the \<manifest\>tag's [versionCode](../android/R.styleable.md) attribute. |
| [ArchivedPackageInfo](../android/content/pm/ArchivedPackageInfo.md) | [setVersionCodeMajor](../android/content/pm/ArchivedPackageInfo.md))`(`value:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` The major version number of the package, as specified by the \<manifest\>tag's [versionCodeMajor](../android/R.styleable.md) attribute. |
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
| `signingInfo` | [SigningInfo](../android/content/pm/SigningInfo.md):This value cannot be`null`. |
| `launcherActivities` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [ArchivedActivityInfo](../android/content/pm/ArchivedActivityInfo.md)!\>:This value cannot be`null`. |
| --- | --- |

## Public methods

### getDefaultToDeviceProtectedStorage

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDefaultToDeviceProtectedStorage(): String?
```

Package data will default to device protected storage. Specified by the \<manifest\> tag's [android.R.styleable#AndroidManifestApplication_defaultToDeviceProtectedStorage](../android/R.styleable.md) attribute.

| Return ||
|-----------------------------------------------------------------------------------|--------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | This value may be`null`. |

### getLauncherActivities

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getLauncherActivities(): MutableList<ArchivedActivityInfo!>
```

List of the package's activities that specify [Intent.ACTION_MAIN](../android/content/Intent.md) and [Intent.CATEGORY_LAUNCHER](../android/content/Intent.md).

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [ArchivedActivityInfo](../android/content/pm/ArchivedActivityInfo.md)!> | This value cannot be`null`. |

**See Also**

- [android.content.pm.LauncherApps#getActivityList](../android/content/pm/LauncherApps.md)) 

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

If`true`this app would like to run under the legacy storage model. Specified by the \<manifest\> tag's [android.R.styleable#AndroidManifestApplication_requestLegacyExternalStorage](../android/R.styleable.md) attribute.

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
| [SigningInfo](../android/content/pm/SigningInfo.md) | This value cannot be`null`. |

### getTargetSdkVersion

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTargetSdkVersion(): Int
```

This is the SDK version number that the application is targeting, as specified by the \<manifest\> tag's [android.R.styleable#AndroidManifestUsesSdk_targetSdkVersion](../android/R.styleable.md) attribute. 

### getUserDataFragile

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getUserDataFragile(): String?
```

If`true`the user is prompted to keep the app's data on uninstall. Specified by the \<manifest\> tag's [android.R.styleable#AndroidManifestApplication_hasFragileUserData](../android/R.styleable.md) attribute.

| Return ||
|-----------------------------------------------------------------------------------|--------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | This value may be`null`. |

### getVersionCode

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getVersionCode(): Int
```

The version number of the package, as specified by the \<manifest\>tag's [versionCode](../android/R.styleable.md) attribute. 

### getVersionCodeMajor

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getVersionCodeMajor(): Int
```

The major version number of the package, as specified by the \<manifest\>tag's [versionCodeMajor](../android/R.styleable.md) attribute. 

### setDefaultToDeviceProtectedStorage

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setDefaultToDeviceProtectedStorage(value: String): ArchivedPackageInfo
```

Package data will default to device protected storage. Specified by the \<manifest\> tag's [android.R.styleable#AndroidManifestApplication_defaultToDeviceProtectedStorage](../android/R.styleable.md) attribute.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------|
| `value` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):This value cannot be`null`. |

| Return ||
|---------------------------------------------------------------------------------------------------------------|-----------------------------|
| [ArchivedPackageInfo](../android/content/pm/ArchivedPackageInfo.md) | This value cannot be`null`. |

### setLauncherActivities

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setLauncherActivities(value: MutableList<ArchivedActivityInfo!>): ArchivedPackageInfo
```

List of the package's activities that specify [Intent.ACTION_MAIN](../android/content/Intent.md) and [Intent.CATEGORY_LAUNCHER](../android/content/Intent.md).

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `value` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [ArchivedActivityInfo](../android/content/pm/ArchivedActivityInfo.md)!\>:This value cannot be`null`. |

| Return ||
|---------------------------------------------------------------------------------------------------------------|-----------------------------|
| [ArchivedPackageInfo](../android/content/pm/ArchivedPackageInfo.md) | This value cannot be`null`. |

**See Also**

- [android.content.pm.LauncherApps#getActivityList](../android/content/pm/LauncherApps.md)) 

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
| [ArchivedPackageInfo](../android/content/pm/ArchivedPackageInfo.md) | This value cannot be`null`. |

### setRequestLegacyExternalStorage

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setRequestLegacyExternalStorage(value: String): ArchivedPackageInfo
```

If`true`this app would like to run under the legacy storage model. Specified by the \<manifest\> tag's [android.R.styleable#AndroidManifestApplication_requestLegacyExternalStorage](../android/R.styleable.md) attribute.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------|
| `value` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):This value cannot be`null`. |

| Return ||
|---------------------------------------------------------------------------------------------------------------|-----------------------------|
| [ArchivedPackageInfo](../android/content/pm/ArchivedPackageInfo.md) | This value cannot be`null`. |

### setSigningInfo

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setSigningInfo(value: SigningInfo): ArchivedPackageInfo
```

Signing certificates used to sign the package.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------|
| `value` | [SigningInfo](../android/content/pm/SigningInfo.md):This value cannot be`null`. |

| Return ||
|---------------------------------------------------------------------------------------------------------------|-----------------------------|
| [ArchivedPackageInfo](../android/content/pm/ArchivedPackageInfo.md) | This value cannot be`null`. |

### setTargetSdkVersion

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setTargetSdkVersion(value: Int): ArchivedPackageInfo
```

This is the SDK version number that the application is targeting, as specified by the \<manifest\> tag's [android.R.styleable#AndroidManifestUsesSdk_targetSdkVersion](../android/R.styleable.md) attribute.

| Return ||
|---------------------------------------------------------------------------------------------------------------|-----------------------------|
| [ArchivedPackageInfo](../android/content/pm/ArchivedPackageInfo.md) | This value cannot be`null`. |

### setUserDataFragile

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setUserDataFragile(value: String): ArchivedPackageInfo
```

If`true`the user is prompted to keep the app's data on uninstall. Specified by the \<manifest\> tag's [android.R.styleable#AndroidManifestApplication_hasFragileUserData](../android/R.styleable.md) attribute.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------|
| `value` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):This value cannot be`null`. |

| Return ||
|---------------------------------------------------------------------------------------------------------------|-----------------------------|
| [ArchivedPackageInfo](../android/content/pm/ArchivedPackageInfo.md) | This value cannot be`null`. |

### setVersionCode

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setVersionCode(value: Int): ArchivedPackageInfo
```

The version number of the package, as specified by the \<manifest\>tag's [versionCode](../android/R.styleable.md) attribute.

| Return ||
|---------------------------------------------------------------------------------------------------------------|-----------------------------|
| [ArchivedPackageInfo](../android/content/pm/ArchivedPackageInfo.md) | This value cannot be`null`. |

### setVersionCodeMajor

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setVersionCodeMajor(value: Int): ArchivedPackageInfo
```

The major version number of the package, as specified by the \<manifest\>tag's [versionCodeMajor](../android/R.styleable.md) attribute.

| Return ||
|---------------------------------------------------------------------------------------------------------------|-----------------------------|
| [ArchivedPackageInfo](../android/content/pm/ArchivedPackageInfo.md) | This value cannot be`null`. |
