# LocaleManager

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# LocaleManager

Kotlin| [Java](https://developer.android.com/reference/android/app/LocaleManager "View this page in Java") 

```
open class LocaleManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.app.LocaleManager](https://developer.android.com/reference/kotlin/android/app/LocaleManager#) |

This class gives access to system locale services. These services allow applications to control granular locale settings (such as per-app locales) or override their list of supported locales while running.

Third party applications should treat this as a write-side surface, and continue reading locales via their in-process [LocaleList](https://developer.android.com/reference/kotlin/android/os/LocaleList.html#) s.

## Summary

| Public methods ||
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [LocaleList](https://developer.android.com/reference/kotlin/android/os/LocaleList.html#) | [getApplicationLocales](https://developer.android.com/reference/kotlin/android/app/LocaleManager#getApplicationLocales())`()` Returns the UI locales for the calling app. |
| open [LocaleList](https://developer.android.com/reference/kotlin/android/os/LocaleList.html#) | [getApplicationLocales](https://developer.android.com/reference/kotlin/android/app/LocaleManager#getApplicationLocales(kotlin.String))`(`appPackageName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Returns the current UI locales for a specified app (described by package name). |
| open [LocaleConfig](https://developer.android.com/reference/kotlin/android/app/LocaleConfig)? | [getOverrideLocaleConfig](https://developer.android.com/reference/kotlin/android/app/LocaleManager#getOverrideLocaleConfig())`()` Returns the override LocaleConfig for the calling app. |
| open [LocaleList](https://developer.android.com/reference/kotlin/android/os/LocaleList.html#) | [getSystemLocales](https://developer.android.com/reference/kotlin/android/app/LocaleManager#getSystemLocales())`()` Returns the current system locales, ignoring app-specific overrides. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setApplicationLocales](https://developer.android.com/reference/kotlin/android/app/LocaleManager#setApplicationLocales(android.os.LocaleList))`(`locales:` ` [LocaleList](https://developer.android.com/reference/kotlin/android/os/LocaleList.html#)`)` Sets the UI locales for the calling app. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOverrideLocaleConfig](https://developer.android.com/reference/kotlin/android/app/LocaleManager#setOverrideLocaleConfig(android.app.LocaleConfig))`(`localeConfig:` ` [LocaleConfig](https://developer.android.com/reference/kotlin/android/app/LocaleConfig)?`)` Sets the override LocaleConfig for the calling app. |

## Public methods

### getApplicationLocales

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getApplicationLocales(): LocaleList
```

Returns the UI locales for the calling app.

Returns a [LocaleList.getEmptyLocaleList()](https://developer.android.com/reference/kotlin/android/os/LocaleList.html#getEmptyLocaleList())if no app-specific locales are set.

| Return ||
|------------------------------------------------------------------------------------------|-----------------------------|
| [LocaleList](https://developer.android.com/reference/kotlin/android/os/LocaleList.html#) | This value cannot be`null`. |

### getApplicationLocales

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getApplicationLocales(appPackageName: String): LocaleList
```

Returns the current UI locales for a specified app (described by package name).

Returns a [LocaleList.getEmptyLocaleList()](https://developer.android.com/reference/kotlin/android/os/LocaleList.html#getEmptyLocaleList())if no app-specific locales are set.

This API can be used by an app's installer (per [android.content.pm.InstallSourceInfo#getInstallingPackageName](https://developer.android.com/reference/kotlin/android/content/pm/InstallSourceInfo.html#getInstallingPackageName())) to retrieve the app's locales.

This API can be used by the current input method to retrieve locales of another packages. All other cases require`android.Manifest.permission#READ_APP_SPECIFIC_LOCALES`. Apps should generally retrieve their own locales via their in-process LocaleLists, or by calling [getApplicationLocales()](https://developer.android.com/reference/kotlin/android/app/LocaleManager#getApplicationLocales()).

| Parameters ||
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `appPackageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):the package name of the app for which to retrieve the locales. This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------------|-----------------------------|
| [LocaleList](https://developer.android.com/reference/kotlin/android/os/LocaleList.html#) | This value cannot be`null`. |

### getOverrideLocaleConfig

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getOverrideLocaleConfig(): LocaleConfig?
```

Returns the override LocaleConfig for the calling app.

| Return ||
|------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| [LocaleConfig](https://developer.android.com/reference/kotlin/android/app/LocaleConfig)? | the override LocaleConfig, or`null`if the LocaleConfig isn't overridden. |

### getSystemLocales

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSystemLocales(): LocaleList
```

Returns the current system locales, ignoring app-specific overrides.

**Note:** Apps should generally access the user's locale preferences as indicated in their in-process [LocaleList](https://developer.android.com/reference/kotlin/android/os/LocaleList.html#) s. However, in case an app-specific locale is set, this method helps cater to rare use-cases which might require specifically knowing the system locale.

**Note:**This API is not user-aware. It returns the system locales for the foreground user.

| Return ||
|------------------------------------------------------------------------------------------|-----------------------------|
| [LocaleList](https://developer.android.com/reference/kotlin/android/os/LocaleList.html#) | This value cannot be`null`. |

### setApplicationLocales

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setApplicationLocales(locales: LocaleList): Unit
```

Sets the UI locales for the calling app.

Pass a [LocaleList.getEmptyLocaleList()](https://developer.android.com/reference/kotlin/android/os/LocaleList.html#getEmptyLocaleList())to reset to the system locale.

**Note:** Changes to app locales will result in a configuration change (and potentially an Activity lifecycle event) being applied to the calling application. For more information, see the [section on handling configuration changes](https://developer.android.com/guide/topics/resources/runtime-changes). The set locales are persisted; they are backed up if the user has enabled Backup \& Restore.

**Note:** Users' locale preferences are passed to applications by creating a union of any app-specific locales and system locales, with the app-specific locales appearing first. Language resources are then chosen per usual (as described in the [section on locale resolution](https://developer.android.com/guide/topics/resources/multilingual-support)).

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `locales` | [LocaleList](https://developer.android.com/reference/kotlin/android/os/LocaleList.html#):the desired locales for the calling app. This value cannot be`null`. |

### setOverrideLocaleConfig

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setOverrideLocaleConfig(localeConfig: LocaleConfig?): Unit
```

Sets the override LocaleConfig for the calling app.

**Note:**Only the app itself with the same user can override its own LocaleConfig.

**Note:** This function takes in a [LocaleConfig](https://developer.android.com/reference/kotlin/android/app/LocaleConfig) which is intended to override the original config in the application's resources. This LocaleConfig will become the override config, and stored in a system file for future access.

**Note:** Using this function, applications can update their list of supported locales while running, without an update of the application's software. For more information, see the [section on dynamic updates for an app's localeConfig](https://developer.android.com/about/versions/14/features#app-languages).

Applications can remove the override LocaleConfig with a`null`object.

| Parameters ||
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `localeConfig` | [LocaleConfig](https://developer.android.com/reference/kotlin/android/app/LocaleConfig)?:the desired [LocaleConfig](https://developer.android.com/reference/kotlin/android/app/LocaleConfig) for the calling app. This value may be`null`. |
