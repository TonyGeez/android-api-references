# SettingsSlicesContract

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SettingsSlicesContract

Kotlin| [Java](SettingsSlicesContract.md) 
| --- | --- |

```
open class SettingsSlicesContract
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.provider.SettingsSlicesContract](SettingsSlicesContract.md) |

Provides a contract for platform-supported Settings [Slices](../android.app.slice/Slice.md).

Contains definitions for the supported [SliceProvider](../android.app.slice/SliceProvider.md) authority, authority [Uri](../android.net/Uri.md), and key constants.

[Slice](../android.app.slice/Slice.md) presenters interested in learning meta-data about the [Slice](../android.app.slice/Slice.md) should read the [Slice](../android.app.slice/Slice.md) object at runtime.

[Uri](../android.net/Uri.md) builder example: 

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
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [AUTHORITY](SettingsSlicesContract.md) Authority for platform Settings Slices. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [KEY_AIRPLANE_MODE](SettingsSlicesContract.md) [Uri](../android.net/Uri.md) key for the Airplane Mode setting. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [KEY_BATTERY_SAVER](SettingsSlicesContract.md) [Uri](../android.net/Uri.md) key for the Battery Saver setting. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [KEY_BLUETOOTH](SettingsSlicesContract.md) [Uri](../android.net/Uri.md) key for the Bluetooth setting. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [KEY_LOCATION](SettingsSlicesContract.md) [Uri](../android.net/Uri.md) key for the Location setting. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [KEY_WIFI](SettingsSlicesContract.md) [Uri](../android.net/Uri.md) key for the Wi-fi setting. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [PATH_SETTING_ACTION](SettingsSlicesContract.md) [Uri](../android.net/Uri.md) path indicating that the requested [Slice](../android.app.slice/Slice.md) should have inline controls for the corresponding setting. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [PATH_SETTING_INTENT](SettingsSlicesContract.md) [Uri](../android.net/Uri.md) path indicating that the requested [Slice](../android.app.slice/Slice.md) should be [Intent](../android.content/Intent.md)-only. |

| Properties ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Uri](../android.net/Uri.md)! | [BASE_URI](SettingsSlicesContract.md) A content:// style uri to the Settings Slices authority, [AUTHORITY](SettingsSlicesContract.md). |

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

[Uri](../android.net/Uri.md) key for the Airplane Mode setting. 

 Value: "airplane_mode"

### KEY_BATTERY_SAVER

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val KEY_BATTERY_SAVER: String
```

[Uri](../android.net/Uri.md) key for the Battery Saver setting. 

 Value: "battery_saver"

### KEY_BLUETOOTH

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val KEY_BLUETOOTH: String
```

[Uri](../android.net/Uri.md) key for the Bluetooth setting. 

 Value: "bluetooth"

### KEY_LOCATION

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val KEY_LOCATION: String
```

[Uri](../android.net/Uri.md) key for the Location setting. 

 Value: "location"

### KEY_WIFI

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val KEY_WIFI: String
```

[Uri](../android.net/Uri.md) key for the Wi-fi setting. 

 Value: "wifi"

### PATH_SETTING_ACTION

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PATH_SETTING_ACTION: String
```

[Uri](../android.net/Uri.md) path indicating that the requested [Slice](../android.app.slice/Slice.md) should have inline controls for the corresponding setting.

This path will only contain Slices defined by keys in this class. 

 Value: "action"

### PATH_SETTING_INTENT

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PATH_SETTING_INTENT: String
```

[Uri](../android.net/Uri.md) path indicating that the requested [Slice](../android.app.slice/Slice.md) should be [Intent](../android.content/Intent.md)-only.

[Slices](../android.app.slice/Slice.md) with actions should use the [PATH_SETTING_ACTION](SettingsSlicesContract.md) path.

This path will only contain Slices defined by keys in this class 

 Value: "intent"

## Properties

### BASE_URI

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BASE_URI: Uri!
```

A content:// style uri to the Settings Slices authority, [AUTHORITY](SettingsSlicesContract.md).
