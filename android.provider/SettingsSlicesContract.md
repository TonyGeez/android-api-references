# SettingsSlicesContract

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SettingsSlicesContract

Kotlin| [Java](https://developer.android.com/reference/android/provider/SettingsSlicesContract "View this page in Java") 
| --- | --- |

```
open class SettingsSlicesContract
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.provider.SettingsSlicesContract](https://developer.android.com/reference/kotlin/android/provider/SettingsSlicesContract#) |

Provides a contract for platform-supported Settings [Slices](https://developer.android.com/reference/kotlin/android/app/slice/Slice.html#).

Contains definitions for the supported [SliceProvider](https://developer.android.com/reference/kotlin/android/app/slice/SliceProvider.html#) authority, authority [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#), and key constants.

[Slice](https://developer.android.com/reference/kotlin/android/app/slice/Slice.html#) presenters interested in learning meta-data about the [Slice](https://developer.android.com/reference/kotlin/android/app/slice/Slice.html#) should read the [Slice](https://developer.android.com/reference/kotlin/android/app/slice/Slice.html#) object at runtime.

[Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#) builder example: 

```kotlin
Uri wifiActionUri = BASE_URI
          .buildUpon()
          .appendPath(PATH_SETTING_ACTION)
          .appendPath(KEY_WIFI)
          .build();
  Uri bluetoothIntentUri = BASE_URI
          .buildUpon()
          .appendPath(PATH_SETTING_INTENT)
          .appendPath(KEY_BLUETOOTH)
          .build();
  
```

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [AUTHORITY](https://developer.android.com/reference/kotlin/android/provider/SettingsSlicesContract#AUTHORITY:kotlin.String) Authority for platform Settings Slices. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [KEY_AIRPLANE_MODE](https://developer.android.com/reference/kotlin/android/provider/SettingsSlicesContract#KEY_AIRPLANE_MODE:kotlin.String) [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#) key for the Airplane Mode setting. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [KEY_BATTERY_SAVER](https://developer.android.com/reference/kotlin/android/provider/SettingsSlicesContract#KEY_BATTERY_SAVER:kotlin.String) [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#) key for the Battery Saver setting. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [KEY_BLUETOOTH](https://developer.android.com/reference/kotlin/android/provider/SettingsSlicesContract#KEY_BLUETOOTH:kotlin.String) [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#) key for the Bluetooth setting. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [KEY_LOCATION](https://developer.android.com/reference/kotlin/android/provider/SettingsSlicesContract#KEY_LOCATION:kotlin.String) [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#) key for the Location setting. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [KEY_WIFI](https://developer.android.com/reference/kotlin/android/provider/SettingsSlicesContract#KEY_WIFI:kotlin.String) [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#) key for the Wi-fi setting. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [PATH_SETTING_ACTION](https://developer.android.com/reference/kotlin/android/provider/SettingsSlicesContract#PATH_SETTING_ACTION:kotlin.String) [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#) path indicating that the requested [Slice](https://developer.android.com/reference/kotlin/android/app/slice/Slice.html#) should have inline controls for the corresponding setting. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [PATH_SETTING_INTENT](https://developer.android.com/reference/kotlin/android/provider/SettingsSlicesContract#PATH_SETTING_INTENT:kotlin.String) [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#) path indicating that the requested [Slice](https://developer.android.com/reference/kotlin/android/app/slice/Slice.html#) should be [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#)-only. |

| Properties ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)! | [BASE_URI](https://developer.android.com/reference/kotlin/android/provider/SettingsSlicesContract#BASE_URI:android.net.Uri) A content:// style uri to the Settings Slices authority, [AUTHORITY](https://developer.android.com/reference/kotlin/android/provider/SettingsSlicesContract#AUTHORITY:kotlin.String). |

## Constants

### AUTHORITY

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val AUTHORITY: String
```

Authority for platform Settings Slices. 

 Value: "android.settings.slices"

### KEY_AIRPLANE_MODE

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val KEY_AIRPLANE_MODE: String
```

[Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#) key for the Airplane Mode setting. 

 Value: "airplane_mode"

### KEY_BATTERY_SAVER

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val KEY_BATTERY_SAVER: String
```

[Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#) key for the Battery Saver setting. 

 Value: "battery_saver"

### KEY_BLUETOOTH

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val KEY_BLUETOOTH: String
```

[Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#) key for the Bluetooth setting. 

 Value: "bluetooth"

### KEY_LOCATION

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val KEY_LOCATION: String
```

[Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#) key for the Location setting. 

 Value: "location"

### KEY_WIFI

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val KEY_WIFI: String
```

[Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#) key for the Wi-fi setting. 

 Value: "wifi"

### PATH_SETTING_ACTION

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PATH_SETTING_ACTION: String
```

[Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#) path indicating that the requested [Slice](https://developer.android.com/reference/kotlin/android/app/slice/Slice.html#) should have inline controls for the corresponding setting.

This path will only contain Slices defined by keys in this class. 

 Value: "action"

### PATH_SETTING_INTENT

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PATH_SETTING_INTENT: String
```

[Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#) path indicating that the requested [Slice](https://developer.android.com/reference/kotlin/android/app/slice/Slice.html#) should be [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#)-only.

[Slices](https://developer.android.com/reference/kotlin/android/app/slice/Slice.html#) with actions should use the [PATH_SETTING_ACTION](https://developer.android.com/reference/kotlin/android/provider/SettingsSlicesContract#PATH_SETTING_ACTION:kotlin.String) path.

This path will only contain Slices defined by keys in this class 

 Value: "intent"

## Properties

### BASE_URI

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BASE_URI: Uri!
```

A content:// style uri to the Settings Slices authority, [AUTHORITY](https://developer.android.com/reference/kotlin/android/provider/SettingsSlicesContract#AUTHORITY:kotlin.String).
