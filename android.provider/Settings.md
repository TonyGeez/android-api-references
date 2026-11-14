Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Settings

```
class Settings
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.provider.Settings](../android/provider/Settings.md) |

The Settings provider contains global system-level device preferences.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/provider/Settings.Global` Global system settings, containing preferences that always apply identically to all defined users. |
| | `https://developer.android.com/reference/kotlin/android/provider/Settings.NameValueTable` Common base for tables of name/value settings. |
| | `https://developer.android.com/reference/kotlin/android/provider/Settings.Panel` A Settings panel is floating UI that contains a fixed subset of settings to address a particular user problem. |
| --- | --- |
| | `https://developer.android.com/reference/kotlin/android/provider/Settings.Secure` Secure system settings, containing system preferences that applications can read but are not allowed to write. |
| | `https://developer.android.com/reference/kotlin/android/provider/Settings.SettingNotFoundException` <br /> |
| | `https://developer.android.com/reference/kotlin/android/provider/Settings.System` System settings, containing miscellaneous system preferences. |
| --- | --- |

| Constants ||
|---|---|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_ACCESSIBILITY_SETTINGS:kotlin.String` Activity Action: Show settings for accessibility modules. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_ADD_ACCOUNT:kotlin.String` Activity Action: Show add account screen for creating a new account. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_ADVANCED_MEMORY_PROTECTION_SETTINGS:kotlin.String` Activity Action: Show settings to allow configuration of Advanced memory protection. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_AIRPLANE_MODE_SETTINGS:kotlin.String` Activity Action: Show settings to allow entering/exiting airplane mode. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_ALL_APPS_NOTIFICATION_SETTINGS:kotlin.String` Activity Action: Show app listing settings, filtered by those that send notifications. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_APN_SETTINGS:kotlin.String` Activity Action: Show settings to allow configuration of APNs. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_APPLICATION_DETAILS_SETTINGS:kotlin.String` Activity Action: Show screen of details about a particular application. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_APPLICATION_DEVELOPMENT_SETTINGS:kotlin.String` Activity Action: Show settings to allow configuration of application development-related settings. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_APPLICATION_SETTINGS:kotlin.String` Activity Action: Show settings to allow configuration of application-related settings. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_APP_LOCALE_SETTINGS:kotlin.String` Activity Action: Show settings to allow configuration of per application locale. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_APP_LOCK_SETTINGS:kotlin.String` Activity Action: Show App Lock settings. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_APP_NOTIFICATION_BUBBLE_SETTINGS:kotlin.String` Activity Action: Show notification bubble settings for a single app. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_APP_NOTIFICATION_PROMOTION_SETTINGS:kotlin.String` Activity Action: Show the permission screen for allowing apps to post promoted notifications. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_APP_NOTIFICATION_SETTINGS:kotlin.String` Activity Action: Show notification settings for a single app. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_APP_OPEN_BY_DEFAULT_SETTINGS:kotlin.String` Activity Action: Show the "Open by Default" page in a particular application's details page. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_APP_SEARCH_SETTINGS:kotlin.String` Activity action: Show Settings app search UI when this action is available for device. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_APP_USAGE_SETTINGS:kotlin.String` Activity Action: Show screen for controlling app usage properties for an app. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_AUTOMATIC_ZEN_RULE_SETTINGS:kotlin.String` Activity Action: Shows the settings page for an `https://developer.android.com/reference/kotlin/android/app/AutomaticZenRule.html#` mode. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_AUTO_ROTATE_SETTINGS:kotlin.String` Activity Action: Show Auto Rotate configuration settings. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_BATTERY_SAVER_SETTINGS:kotlin.String` Activity Action: Show battery saver settings. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_BIOMETRIC_ENROLL:kotlin.String` Activity Action: Show settings to enroll biometrics, and setup PIN/Pattern/Pass if necessary. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_BLUETOOTH_SETTINGS:kotlin.String` Activity Action: Show settings to allow configuration of Bluetooth. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_CAPTIONING_SETTINGS:kotlin.String` Activity Action: Show settings for video captioning. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_CAST_SETTINGS:kotlin.String` Activity Action: Show settings to allow configuration of cast endpoints. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_CHANNEL_NOTIFICATION_SETTINGS:kotlin.String` Activity Action: Show notification settings for a single `https://developer.android.com/reference/kotlin/android/app/NotificationChannel.html#`. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_CONDITION_PROVIDER_SETTINGS:kotlin.String` Activity Action: Show the automatic do not disturb rule listing page |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_CREDENTIAL_PROVIDER:kotlin.String` Activity Action: Show screen that let user enable a Credential Manager provider. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_DATA_ROAMING_SETTINGS:kotlin.String` Activity Action: Show settings for selection of 2G/3G. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_DATA_USAGE_SETTINGS:kotlin.String` Activity Action: Show settings to allow configuration of data and view data usage. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_DATE_SETTINGS:kotlin.String` Activity Action: Show settings to allow configuration of date and time. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_DEVICE_INFO_SETTINGS:kotlin.String` Activity Action: Show general device information settings (serial number, software version, phone number, etc.). |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_DISPLAY_SETTINGS:kotlin.String` Activity Action: Show settings to allow configuration of display. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_DREAM_SETTINGS:kotlin.String` Activity Action: Show Daydream settings. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_FINGERPRINT_ENROLL:kotlin.String` Activity Action: Show settings to enroll fingerprints, and setup PIN/Pattern/Pass if necessary. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_FIRST_DAY_OF_WEEK_SETTINGS:kotlin.String` Activity Action: Show first day of week configuration settings. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_HARD_KEYBOARD_SETTINGS:kotlin.String` Activity Action: Show settings to configure the hardware keyboard. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_HOME_SETTINGS:kotlin.String` Activity Action: Show Home selection settings. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_HOME_TIME_ZONE_SETTINGS:kotlin.String` Activity Action: Show settings to allow configuration of home time zone. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_IGNORE_BACKGROUND_DATA_RESTRICTIONS_SETTINGS:kotlin.String` Activity Action: Show screen for controlling background data restrictions for a particular application. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_IGNORE_BATTERY_OPTIMIZATION_SETTINGS:kotlin.String` Activity Action: Show screen for controlling which apps can ignore battery optimizations. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_INPUT_METHOD_SETTINGS:kotlin.String` Activity Action: Show settings to configure input methods, in particular allowing the user to enable input methods. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_INPUT_METHOD_SUBTYPE_SETTINGS:kotlin.String` Activity Action: Show settings to enable/disable input method subtypes. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_INTERNAL_STORAGE_SETTINGS:kotlin.String` Activity Action: Show settings for internal storage. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_LOCALE_SETTINGS:kotlin.String` Activity Action: Show settings to allow configuration of locale. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_LOCATION_SOURCE_SETTINGS:kotlin.String` Activity Action: Show settings to allow configuration of current location sources. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_MANAGE_ALL_APPLICATIONS_SETTINGS:kotlin.String` Activity Action: Show settings to manage all applications. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_MANAGE_ALL_FILES_ACCESS_PERMISSION:kotlin.String` Activity Action: Show screen for controlling which apps have access to manage external storage. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_MANAGE_ALL_SIM_PROFILES_SETTINGS:kotlin.String` Activity Action: Show settings to manage all SIM profiles. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_MANAGE_APPLICATIONS_SETTINGS:kotlin.String` Activity Action: Show settings to manage installed applications. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_MANAGE_APP_ALL_FILES_ACCESS_PERMISSION:kotlin.String` Activity Action: Show screen for controlling if the app specified in the data URI of the intent can manage external storage. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_MANAGE_APP_USE_FULL_SCREEN_INTENT:kotlin.String` Activity Action: Show screen for controlling whether an app can send full screen intents. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_MANAGE_ASSISTANT_AUDIO:kotlin.String` Activity Action: Show screen for controlling if the app specified in the data URI of the intent has MANAGE_ASSISTANT_AUDIO special app access. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_MANAGE_CONTACTS:kotlin.String` Activity Action: Show screen for controlling which apps have access to manage contacts. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_MANAGE_DEFAULT_APPS_SETTINGS:kotlin.String` Activity Action: Show Default apps settings. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_MANAGE_OVERLAY_PERMISSION:kotlin.String` Activity Action: Show screen for controlling which apps can draw on top of other apps. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_MANAGE_PERIPHERAL_CUSTOMIZATION:kotlin.String` Activity Action: Show screen for controlling which apps are allowed to manage customizations for peripherals. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_MANAGE_SUPERVISOR_RESTRICTED_SETTING:kotlin.String` Activity action: Launch UI to manage a setting restricted by supervisors. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_MANAGE_UNKNOWN_APP_SOURCES:kotlin.String` Activity Action: Show settings to allow configuration of trusted external sources Input: Optionally, the Intent's data URI can specify the application package name to directly invoke the management GUI specific to the package name. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_MANAGE_WRITE_SETTINGS:kotlin.String` Activity Action: Show screen for controlling which apps are allowed to write/modify system settings. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_MEASUREMENT_SYSTEM_SETTINGS:kotlin.String` Activity Action: Show measurement system configuration settings. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_MEMORY_CARD_SETTINGS:kotlin.String` Activity Action: Show settings for memory card storage. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_NETWORK_OPERATOR_SETTINGS:kotlin.String` Activity Action: Show settings for selecting the network operator. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_NFCSHARING_SETTINGS:kotlin.String` Activity Action: Show NFC Sharing settings. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_NFC_PAYMENT_SETTINGS:kotlin.String` Activity Action: Show NFC Tap \& Pay settings |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_NFC_SETTINGS:kotlin.String` Activity Action: Show NFC settings. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_NIGHT_DISPLAY_SETTINGS:kotlin.String` Activity Action: Show settings to allow configuration of Night display. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_NOTIFICATION_ASSISTANT_SETTINGS:kotlin.String` Activity Action: Show Notification assistant settings. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_NOTIFICATION_LISTENER_DETAIL_SETTINGS:kotlin.String` Activity Action: Show notification listener permission settings page for app. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_NOTIFICATION_LISTENER_SETTINGS:kotlin.String` Activity Action: Show Notification listener settings. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_NOTIFICATION_POLICY_ACCESS_SETTINGS:kotlin.String` Activity Action: Show Notification Policy access settings. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_PRINT_SETTINGS:kotlin.String` Activity Action: Show the top level print settings. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_PRIVACY_SETTINGS:kotlin.String` Activity Action: Show settings to allow configuration of privacy options, i. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_PROCESS_WIFI_EASY_CONNECT_URI:kotlin.String` Activity Action: Show setting page to process a Wi-Fi Easy Connect (aka DPP) URI and start configuration. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_QUICK_ACCESS_WALLET_SETTINGS:kotlin.String` Activity Action: Show screen for controlling the Quick Access Wallet. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_QUICK_LAUNCH_SETTINGS:kotlin.String` Activity Action: Show settings to allow configuration of quick launch shortcuts. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_REGIONAL_PREFERENCES_SETTINGS:kotlin.String` Activity Action: Show settings to allow configuration of regional preferences |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_REGION_SETTINGS:kotlin.String` Activity Action: Show screen for allowing the region configuration. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_REQUEST_IGNORE_BATTERY_OPTIMIZATIONS:kotlin.String` Activity Action: Ask the user to allow an app to ignore battery optimizations (that is, put them on the allowlist of apps shown by `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_IGNORE_BATTERY_OPTIMIZATION_SETTINGS:kotlin.String`). |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_REQUEST_MANAGE_MEDIA:kotlin.String` Activity Action: Show settings to allow configuration of `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MANAGE_MEDIA:kotlin.String` permission Input: Optionally, the Intent's data URI can specify the application package name to directly invoke the management GUI specific to the package name. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_REQUEST_MEDIA_ROUTING_CONTROL:kotlin.String` Activity Action: Show settings to allow configuration of `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MEDIA_ROUTING_CONTROL:kotlin.String` permission. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_REQUEST_SCHEDULE_EXACT_ALARM:kotlin.String` Activity Action: Show settings to allow configuration of `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#SCHEDULE_EXACT_ALARM:kotlin.String` permission Input: Optionally, the Intent's data URI can specify the application package name to directly invoke the management GUI specific to the package name. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_REQUEST_SET_AUTOFILL_SERVICE:kotlin.String` Activity Action: Show screen that let user select its Autofill Service. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_SATELLITE_SETTING:kotlin.String` Activity Action: Show settings to provide guide about carrier satellite messaging. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_SEARCH_SETTINGS:kotlin.String` Activity Action: Show settings for global search. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_SECURITY_SETTINGS:kotlin.String` Activity Action: Show settings to allow configuration of security and location privacy. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_SETTINGS:kotlin.String` Activity Action: Show system settings. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_SETTINGS_EMBED_DEEP_LINK_ACTIVITY:kotlin.String` Activity Action: For system or preinstalled apps to show their `https://developer.android.com/reference/kotlin/android/app/Activity.html#` embedded in Settings app on large screen devices. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_SHOW_REGULATORY_INFO:kotlin.String` Activity Action: Show the regulatory information screen for the device. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_SHOW_WORK_POLICY_INFO:kotlin.String` Activity Action: Show Work Policy info. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_SOUND_SETTINGS:kotlin.String` Activity Action: Show settings to allow configuration of sound and volume. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_STORAGE_VOLUME_ACCESS_SETTINGS:kotlin.String` Activity Action: Show screen for controlling which apps have access on volume directories. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_SUPERVISION_SETTINGS:kotlin.String` Activity Action: Show screen to manage supervision settings. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_SYNC_SETTINGS:kotlin.String` Activity Action: Show settings to allow configuration of sync settings. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_SYSTEM_UPDATE_SETTINGS:kotlin.String` Activity Action: Show settings for system update functionality. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_TEMPERATURE_UNIT_SETTINGS:kotlin.String` Activity Action: Show temperature unit configuration settings. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_USAGE_ACCESS_SETTINGS:kotlin.String` Activity Action: Show settings to control access to usage information. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_USER_DICTIONARY_SETTINGS:kotlin.String` Activity Action: Show settings to manage the user input dictionary. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_VOICE_CONTROL_AIRPLANE_MODE:kotlin.String` Activity Action: Modify Airplane mode settings using a voice command. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_VOICE_CONTROL_BATTERY_SAVER_MODE:kotlin.String` Activity Action: Modify Battery Saver mode setting using a voice command. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_VOICE_CONTROL_DO_NOT_DISTURB_MODE:kotlin.String` Activity Action: Modify do not disturb mode settings. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_VOICE_INPUT_SETTINGS:kotlin.String` Activity Action: Show settings to configure input methods, in particular allowing the user to enable input methods. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_VPN_APP_EXCLUSION_SETTINGS:kotlin.String` Activity Action: Show a settings screen to configure application exclusions for the calling package's `https://developer.android.com/reference/kotlin/android/net/VpnManager.html#` VPN. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_VPN_SETTINGS:kotlin.String` Activity Action: Show settings to allow configuration of VPN. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_VR_LISTENER_SETTINGS:kotlin.String` Activity Action: Show VR listener settings. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_WEBVIEW_SETTINGS:kotlin.String` Activity Action: Allows user to select current webview implementation. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_WIFI_ADD_NETWORKS:kotlin.String` Activity Action: Show setting page to process the addition of Wi-Fi networks to the user's saved network list. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_WIFI_IP_SETTINGS:kotlin.String` Activity Action: Show settings to allow configuration of a static IP address for Wi-Fi. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_WIFI_SETTINGS:kotlin.String` Activity Action: Show settings to allow configuration of Wi-Fi. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_WIRELESS_SETTINGS:kotlin.String` Activity Action: Show settings to allow configuration of wireless controls such as Wi-Fi, Bluetooth and Mobile networks. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_ZEN_MODE_PRIORITY_SETTINGS:kotlin.String` Activity Action: Show Zen Mode (aka Do Not Disturb) priority configuration settings. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/provider/Settings#ADD_WIFI_RESULT_ADD_OR_UPDATE_FAILED:kotlin.Int` A result of `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_WIFI_ADD_NETWORKS:kotlin.String` intent action that saving the corresponding Wi-Fi network failed. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/provider/Settings#ADD_WIFI_RESULT_ALREADY_EXISTS:kotlin.Int` A result of `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_WIFI_ADD_NETWORKS:kotlin.String` intent action that indicates the Wi-Fi network already exists. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/provider/Settings#ADD_WIFI_RESULT_SUCCESS:kotlin.Int` A result of `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_WIFI_ADD_NETWORKS:kotlin.String` intent action that saving or updating the corresponding Wi-Fi network was successful. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/Settings#AUTHORITY:kotlin.String` <br /> |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/Settings#EXTRA_ACCOUNT_TYPES:kotlin.String` Activity Extra: Limit available options in launched activity based on the given account types. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/Settings#EXTRA_AIRPLANE_MODE_ENABLED:kotlin.String` Activity Extra: Enable or disable Airplane Mode. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/Settings#EXTRA_APP_PACKAGE:kotlin.String` Activity Extra: The package owner of the notification channel settings to display. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/Settings#EXTRA_AUTHORITIES:kotlin.String` Activity Extra: Limit available options in launched activity based on the given authority. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/Settings#EXTRA_AUTOMATIC_ZEN_RULE_ID:kotlin.String` Activity Extra: The String id of the `https://developer.android.com/reference/kotlin/android/app/AutomaticZenRule.html#` settings to display. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/Settings#EXTRA_BATTERY_SAVER_MODE_ENABLED:kotlin.String` Activity Extra: Enable or disable Battery saver mode. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/Settings#EXTRA_BIOMETRIC_AUTHENTICATORS_ALLOWED:kotlin.String` Activity Extra: The minimum strength to request enrollment for. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/Settings#EXTRA_CHANNEL_FILTER_LIST:kotlin.String` Activity Extra: An `Arraylist<String>` of `https://developer.android.com/reference/kotlin/android/app/NotificationChannel.html#` field names to show on the Settings UI. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/Settings#EXTRA_CHANNEL_ID:kotlin.String` Activity Extra: The `https://developer.android.com/reference/kotlin/android/app/NotificationChannel.html#getId()` of the notification channel settings to display. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/Settings#EXTRA_CONVERSATION_ID:kotlin.String` Activity Extra: The `https://developer.android.com/reference/kotlin/android/app/NotificationChannel.html#getConversationId()` of the notification conversation settings to display. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/Settings#EXTRA_DO_NOT_DISTURB_MODE_ENABLED:kotlin.String` Activity Extra: Enable or disable Do Not Disturb mode. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/Settings#EXTRA_DO_NOT_DISTURB_MODE_MINUTES:kotlin.String` Activity Extra: How many minutes to enable do not disturb mode for. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/Settings#EXTRA_EASY_CONNECT_ATTEMPTED_SSID:kotlin.String` Activity Extra: The SSID that the Enrollee tried to connect to. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/Settings#EXTRA_EASY_CONNECT_BAND_LIST:kotlin.String` Activity Extra: The Band List that the Enrollee supports. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/Settings#EXTRA_EASY_CONNECT_CHANNEL_LIST:kotlin.String` Activity Extra: The Channel List that the Enrollee used to scan a network. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/Settings#EXTRA_EASY_CONNECT_ERROR_CODE:kotlin.String` Activity Extra: The Easy Connect operation error code |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/Settings#EXTRA_INPUT_METHOD_ID:kotlin.String` <br /> |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/Settings#EXTRA_NOTIFICATION_LISTENER_COMPONENT_NAME:kotlin.String` Activity Extra: What component name to show the notification listener permission page for. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/Settings#EXTRA_SETTINGS_EMBEDDED_DEEP_LINK_HIGHLIGHT_MENU_KEY:kotlin.String` Activity Extra: Specify a key that indicates the menu item which should be highlighted on settings home menu. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/Settings#EXTRA_SETTINGS_EMBEDDED_DEEP_LINK_INTENT_URI:kotlin.String` Activity Extra: Specify the intent for the `https://developer.android.com/reference/kotlin/android/app/Activity.html#` which will be embedded in Settings app. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/Settings#EXTRA_SUB_ID:kotlin.String` An int extra specifying a subscription ID. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/Settings#EXTRA_SUPERVISOR_RESTRICTED_SETTING_KEY:kotlin.String` Intent extra: The id of a setting restricted by supervisors. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/Settings#EXTRA_WIFI_NETWORK_LIST:kotlin.String` A bundle extra of `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_WIFI_ADD_NETWORKS:kotlin.String` intent action that indicates the list of the `https://developer.android.com/reference/kotlin/android/net/wifi/WifiNetworkSuggestion.html#` elements. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/Settings#EXTRA_WIFI_NETWORK_RESULT_LIST:kotlin.String` A bundle extra of the result of `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_WIFI_ADD_NETWORKS:kotlin.String` intent action that indicates the action result of the saved `https://developer.android.com/reference/kotlin/android/net/wifi/WifiNetworkSuggestion.html#`. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/Settings#INTENT_CATEGORY_USAGE_ACCESS_CONFIG:kotlin.String` Activity Category: Show application settings related to usage access. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/Settings#METADATA_USAGE_ACCESS_REASON:kotlin.String` Metadata key: Reason for needing usage access. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/provider/Settings#SUPERVISOR_VERIFICATION_SETTING_BIOMETRICS:kotlin.Int` Settings for supervisors to control what kinds of biometric sensors, such a face and fingerprint scanners, can be used on the device. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/provider/Settings#SUPERVISOR_VERIFICATION_SETTING_UNKNOWN:kotlin.Int` The unknown setting can usually be ignored and is used for compatibility with future supervisor settings. |

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/provider/Settings#Settings()()` <br /> |

| Public methods ||
|---|---|
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/provider/Settings#canDrawOverlays(android.content.Context)(context: https://developer.android.com/reference/kotlin/android/content/Context.html#!)` Checks if the specified context can draw on top of other apps. |

## Constants

### ACTION_ACCESSIBILITY_SETTINGS

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_ACCESSIBILITY_SETTINGS: String
```

Activity Action: Show settings for accessibility modules.

In some cases, a matching Activity may not exist, so ensure you safeguard against this.

Input: Nothing.

Output: Nothing.

 Value: "android.settings.ACCESSIBILITY_SETTINGS"

### ACTION_ADD_ACCOUNT

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_ADD_ACCOUNT: String
```

Activity Action: Show add account screen for creating a new account.

In some cases, a matching Activity may not exist, so ensure you safeguard against this.

The account types available to add may be restricted by adding an `https://developer.android.com/reference/kotlin/android/provider/Settings#EXTRA_AUTHORITIES:kotlin.String` extra to the Intent with one or more syncable content provider's authorities. Only account types which can sync with that content provider will be offered to the user.

Account types can also be filtered by adding an `https://developer.android.com/reference/kotlin/android/provider/Settings#EXTRA_ACCOUNT_TYPES:kotlin.String` extra to the Intent with one or more account types.

Input: Nothing.

Output: Nothing.

 Value: "android.settings.ADD_ACCOUNT_SETTINGS"

### ACTION_ADVANCED_MEMORY_PROTECTION_SETTINGS

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_ADVANCED_MEMORY_PROTECTION_SETTINGS: String
```

Activity Action: Show settings to allow configuration of Advanced memory protection.

Memory Tagging Extension (MTE) is a CPU extension that allows to protect against certain classes of security problems at a small runtime performance cost overhead.

In some cases, a matching Activity may not exist, so ensure you safeguard against this.

Input: Nothing.

Output: Nothing.

 Value: "android.settings.ADVANCED_MEMORY_PROTECTION_SETTINGS"

### ACTION_AIRPLANE_MODE_SETTINGS

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_AIRPLANE_MODE_SETTINGS: String
```

Activity Action: Show settings to allow entering/exiting airplane mode.

In some cases, a matching Activity may not exist, so ensure you safeguard against this.

Input: Nothing.

Output: Nothing.

 Value: "android.settings.AIRPLANE_MODE_SETTINGS"

### ACTION_ALL_APPS_NOTIFICATION_SETTINGS

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_ALL_APPS_NOTIFICATION_SETTINGS: String
```

Activity Action: Show app listing settings, filtered by those that send notifications.

 Value: "android.settings.ALL_APPS_NOTIFICATION_SETTINGS"

### ACTION_APN_SETTINGS

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_APN_SETTINGS: String
```

Activity Action: Show settings to allow configuration of APNs.

Input: Nothing.

Output: Nothing.

In some cases, a matching Activity may not exist, so ensure you safeguard against this.

 Value: "android.settings.APN_SETTINGS"

### ACTION_APPLICATION_DETAILS_SETTINGS

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_APPLICATION_DETAILS_SETTINGS: String
```

Activity Action: Show screen of details about a particular application.

In some cases, a matching Activity may not exist, so ensure you safeguard against this.

Input: The Intent's data URI specifies the application package name to be shown, with the "package" scheme. That is "package:com.my.app".

Output: Nothing.

 Value: "android.settings.APPLICATION_DETAILS_SETTINGS"

### ACTION_APPLICATION_DEVELOPMENT_SETTINGS

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_APPLICATION_DEVELOPMENT_SETTINGS: String
```

Activity Action: Show settings to allow configuration of application development-related settings. As of `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#JELLY_BEAN_MR1:kotlin.Int` this action is a required part of the platform.

Input: Nothing.

Output: Nothing.

 Value: "android.settings.APPLICATION_DEVELOPMENT_SETTINGS"

### ACTION_APPLICATION_SETTINGS

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_APPLICATION_SETTINGS: String
```

Activity Action: Show settings to allow configuration of application-related settings.

In some cases, a matching Activity may not exist, so ensure you safeguard against this.

Input: Nothing.

Output: Nothing.

 Value: "android.settings.APPLICATION_SETTINGS"

### ACTION_APP_LOCALE_SETTINGS

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_APP_LOCALE_SETTINGS: String
```

Activity Action: Show settings to allow configuration of per application locale.

Input: The Intent's data URI can specify the application package name to directly invoke the app locale details GUI specific to the package name. For example "package:com.my.app".

Output: Nothing.

 Value: "android.settings.APP_LOCALE_SETTINGS"

### ACTION_APP_LOCK_SETTINGS

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_APP_LOCK_SETTINGS: String
```

Activity Action: Show App Lock settings.

In some cases, a matching Activity may not exist, so ensure you safeguard against this.

Input: Nothing.

Output: Nothing.

 Value: "android.settings.APP_LOCK_SETTINGS"

### ACTION_APP_NOTIFICATION_BUBBLE_SETTINGS

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_APP_NOTIFICATION_BUBBLE_SETTINGS: String
```

Activity Action: Show notification bubble settings for a single app. See `https://developer.android.com/reference/kotlin/android/app/NotificationManager.html#getBubblePreference()`.

Input: `https://developer.android.com/reference/kotlin/android/provider/Settings#EXTRA_APP_PACKAGE:kotlin.String`, the package to display.

Output: Nothing.

 Value: "android.settings.APP_NOTIFICATION_BUBBLE_SETTINGS"

### ACTION_APP_NOTIFICATION_PROMOTION_SETTINGS

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_APP_NOTIFICATION_PROMOTION_SETTINGS: String
```

Activity Action: Show the permission screen for allowing apps to post promoted notifications. Properly formatted priority notifications are elevated in appearance. For example they may be able to use colors, have richer progress bars, show as chips in the status bar, and/or permanently appear on always-on-displays. This functionality is intended to be reserved for user initiated ongoing activities like navigation, phone calls, and ride sharing.

Input: `https://developer.android.com/reference/kotlin/android/provider/Settings#EXTRA_APP_PACKAGE:kotlin.String`, the package to display.

In some cases, a matching Activity may not exist, so ensure you safeguard against this.

Output: Nothing.

 Value: "android.settings.APP_NOTIFICATION_PROMOTION_SETTINGS"

### ACTION_APP_NOTIFICATION_SETTINGS

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_APP_NOTIFICATION_SETTINGS: String
```

Activity Action: Show notification settings for a single app.

Input: `https://developer.android.com/reference/kotlin/android/provider/Settings#EXTRA_APP_PACKAGE:kotlin.String`, the package to display.

Output: Nothing.

 Value: "android.settings.APP_NOTIFICATION_SETTINGS"

### ACTION_APP_OPEN_BY_DEFAULT_SETTINGS

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_APP_OPEN_BY_DEFAULT_SETTINGS: String
```

Activity Action: Show the "Open by Default" page in a particular application's details page.

In some cases, a matching Activity may not exist, so ensure you safeguard against this.

Input: The Intent's data URI specifies the application package name to be shown, with the "package" scheme. That is "package:com.my.app".

Output: Nothing.

 Value: "android.settings.APP_OPEN_BY_DEFAULT_SETTINGS"

### ACTION_APP_SEARCH_SETTINGS

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_APP_SEARCH_SETTINGS: String
```

Activity action: Show Settings app search UI when this action is available for device.

Input: Nothing.

Output: Nothing.

 Value: "android.settings.APP_SEARCH_SETTINGS"

### ACTION_APP_USAGE_SETTINGS

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_APP_USAGE_SETTINGS: String
```

Activity Action: Show screen for controlling app usage properties for an app. Input: Intent's extra `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_PACKAGE_NAME:kotlin.String` must specify the application package name. Output: Nothing.

 Value: "android.settings.action.APP_USAGE_SETTINGS"

### ACTION_AUTOMATIC_ZEN_RULE_SETTINGS

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_AUTOMATIC_ZEN_RULE_SETTINGS: String
```

Activity Action: Shows the settings page for an `https://developer.android.com/reference/kotlin/android/app/AutomaticZenRule.html#` mode.

Users can change the behavior of the mode when it's activated and access the owning app's additional configuration screen, where triggering criteria can be modified (see `https://developer.android.com/reference/kotlin/android/app/AutomaticZenRule.html#setConfigurationActivity(android.content.ComponentName)`).

A matching Activity will only be found if `https://developer.android.com/reference/kotlin/android/app/NotificationManager.html#areAutomaticZenRulesUserManaged()` is true.

Input: The id of the rule, provided in the `https://developer.android.com/reference/kotlin/android/provider/Settings#EXTRA_AUTOMATIC_ZEN_RULE_ID:kotlin.String` extra.

Output: Nothing.

 Value: "android.settings.AUTOMATIC_ZEN_RULE_SETTINGS"

### ACTION_AUTO_ROTATE_SETTINGS

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_AUTO_ROTATE_SETTINGS: String
```

Activity Action: Show Auto Rotate configuration settings.

 Value: "android.settings.AUTO_ROTATE_SETTINGS"

### ACTION_BATTERY_SAVER_SETTINGS

Added in [API level 22](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_BATTERY_SAVER_SETTINGS: String
```

Activity Action: Show battery saver settings.

In some cases, a matching Activity may not exist, so ensure you safeguard against this.

 Value: "android.settings.BATTERY_SAVER_SETTINGS"

### ACTION_BIOMETRIC_ENROLL

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_BIOMETRIC_ENROLL: String
```

Activity Action: Show settings to enroll biometrics, and setup PIN/Pattern/Pass if necessary. By default, this prompts the user to enroll biometrics with strength Weak or above, as defined by the CDD. Only biometrics that meet or exceed Strong, as defined in the CDD are allowed to participate in Keystore operations.

Input: extras `https://developer.android.com/reference/kotlin/android/provider/Settings#EXTRA_BIOMETRIC_AUTHENTICATORS_ALLOWED:kotlin.String` as an integer, with constants defined in `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricManager.Authenticators.html#`, e.g. `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricManager.Authenticators.html#BIOMETRIC_STRONG:kotlin.Int`. If not specified, the default behavior is `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricManager.Authenticators.html#BIOMETRIC_WEAK:kotlin.Int`.

Output: Nothing. Note that callers should still check `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricManager.html#canAuthenticate(kotlin.Int)` afterwards to ensure that the user actually completed enrollment.

 Value: "android.settings.BIOMETRIC_ENROLL"

### ACTION_BLUETOOTH_SETTINGS

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_BLUETOOTH_SETTINGS: String
```

Activity Action: Show settings to allow configuration of Bluetooth.

In some cases, a matching Activity may not exist, so ensure you safeguard against this.

Input: Nothing.

Output: Nothing.

 Value: "android.settings.BLUETOOTH_SETTINGS"

### ACTION_CAPTIONING_SETTINGS

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_CAPTIONING_SETTINGS: String
```

Activity Action: Show settings for video captioning.

In some cases, a matching Activity may not exist, so ensure you safeguard against this.

Input: Nothing.

Output: Nothing.

 Value: "android.settings.CAPTIONING_SETTINGS"

### ACTION_CAST_SETTINGS

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_CAST_SETTINGS: String
```

Activity Action: Show settings to allow configuration of cast endpoints.

In some cases, a matching Activity may not exist, so ensure you safeguard against this.

Input: Nothing.

Output: Nothing.

 Value: "android.settings.CAST_SETTINGS"

### ACTION_CHANNEL_NOTIFICATION_SETTINGS

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_CHANNEL_NOTIFICATION_SETTINGS: String
```

Activity Action: Show notification settings for a single `https://developer.android.com/reference/kotlin/android/app/NotificationChannel.html#`.

Input: `https://developer.android.com/reference/kotlin/android/provider/Settings#EXTRA_APP_PACKAGE:kotlin.String`, the package containing the channel to display. Input: `https://developer.android.com/reference/kotlin/android/provider/Settings#EXTRA_CHANNEL_ID:kotlin.String`, the id of the channel to display.

Output: Nothing.

 Value: "android.settings.CHANNEL_NOTIFICATION_SETTINGS"

### ACTION_CONDITION_PROVIDER_SETTINGS

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_CONDITION_PROVIDER_SETTINGS: String
```

Activity Action: Show the automatic do not disturb rule listing page

Users can add, enable, disable, and remove automatic do not disturb rules from this screen. See `https://developer.android.com/reference/kotlin/android/app/NotificationManager.html#addAutomaticZenRule(android.app.AutomaticZenRule)` for more details.

Input: Nothing Output: Nothing

 Value: "android.settings.ACTION_CONDITION_PROVIDER_SETTINGS"

### ACTION_CREDENTIAL_PROVIDER

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_CREDENTIAL_PROVIDER: String
```

Activity Action: Show screen that let user enable a Credential Manager provider.

Input: Intent's data URI set with an application package name, using the "package" schema (like "package:com.my.app").

Output: `https://developer.android.com/reference/kotlin/android/app/Activity.html#RESULT_OK:kotlin.Int` if user selected a provider belonging to the caller package.

**NOTE:** Applications should call `https://developer.android.com/reference/kotlin/android/credentials/CredentialManager.html#isEnabledCredentialProviderService(android.content.ComponentName)` and only use this action to start an activity if they return `false`.

 Value: "android.settings.CREDENTIAL_PROVIDER"

### ACTION_DATA_ROAMING_SETTINGS

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_DATA_ROAMING_SETTINGS: String
```

Activity Action: Show settings for selection of 2G/3G.

In some cases, a matching Activity may not exist, so ensure you safeguard against this.

Input: Nothing.

Output: Nothing.

 Value: "android.settings.DATA_ROAMING_SETTINGS"

### ACTION_DATA_USAGE_SETTINGS

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_DATA_USAGE_SETTINGS: String
```

Activity Action: Show settings to allow configuration of data and view data usage.

In some cases, a matching Activity may not exist, so ensure you safeguard against this.

Input: Nothing.

Output: Nothing.

 Value: "android.settings.DATA_USAGE_SETTINGS"

### ACTION_DATE_SETTINGS

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_DATE_SETTINGS: String
```

Activity Action: Show settings to allow configuration of date and time.

In some cases, a matching Activity may not exist, so ensure you safeguard against this.

Input: Nothing.

Output: Nothing.

 Value: "android.settings.DATE_SETTINGS"

### ACTION_DEVICE_INFO_SETTINGS

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_DEVICE_INFO_SETTINGS: String
```

Activity Action: Show general device information settings (serial number, software version, phone number, etc.).

In some cases, a matching Activity may not exist, so ensure you safeguard against this.

Input: Nothing.

Output: Nothing

 Value: "android.settings.DEVICE_INFO_SETTINGS"

### ACTION_DISPLAY_SETTINGS

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_DISPLAY_SETTINGS: String
```

Activity Action: Show settings to allow configuration of display.

In some cases, a matching Activity may not exist, so ensure you safeguard against this.

Input: Nothing.

Output: Nothing.

 Value: "android.settings.DISPLAY_SETTINGS"

### ACTION_DREAM_SETTINGS

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_DREAM_SETTINGS: String
```

Activity Action: Show Daydream settings.

In some cases, a matching Activity may not exist, so ensure you safeguard against this.

Input: Nothing.

Output: Nothing.

 Value: "android.settings.DREAM_SETTINGS"

**See Also**

- `https://developer.android.com/reference/kotlin/android/service/dreams/DreamService.html#`

### ACTION_FINGERPRINT_ENROLL

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_FINGERPRINT_ENROLL: String
```

**Deprecated:** *See `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_BIOMETRIC_ENROLL:kotlin.String`.*

*Input: Nothing.*
*Output: Nothing.*

<br />

Activity Action: Show settings to enroll fingerprints, and setup PIN/Pattern/Pass if necessary.

 Value: "android.settings.FINGERPRINT_ENROLL"

### ACTION_FIRST_DAY_OF_WEEK_SETTINGS

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_FIRST_DAY_OF_WEEK_SETTINGS: String
```

Activity Action: Show first day of week configuration settings.

Input: Nothing.

Output: Nothing.

 Value: "android.settings.FIRST_DAY_OF_WEEK_SETTINGS"

### ACTION_HARD_KEYBOARD_SETTINGS

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_HARD_KEYBOARD_SETTINGS: String
```

Activity Action: Show settings to configure the hardware keyboard.

In some cases, a matching Activity may not exist, so ensure you safeguard against this.

Input: Nothing.

Output: Nothing.

 Value: "android.settings.HARD_KEYBOARD_SETTINGS"

### ACTION_HOME_SETTINGS

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_HOME_SETTINGS: String
```

Activity Action: Show Home selection settings. If there are multiple activities that can satisfy the `https://developer.android.com/reference/kotlin/android/content/Intent.html#CATEGORY_HOME:kotlin.String` intent, this screen allows you to pick your preferred activity.

 Value: "android.settings.HOME_SETTINGS"

### ACTION_HOME_TIME_ZONE_SETTINGS

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_HOME_TIME_ZONE_SETTINGS: String
```

Activity Action: Show settings to allow configuration of home time zone.

In some cases, a matching Activity may not exist, so ensure you safeguard against this.

Input: Nothing.

Output: Nothing.

 Value: "android.settings.HOME_TIME_ZONE_SETTINGS"

### ACTION_IGNORE_BACKGROUND_DATA_RESTRICTIONS_SETTINGS

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_IGNORE_BACKGROUND_DATA_RESTRICTIONS_SETTINGS: String
```

Activity Action: Show screen for controlling background data restrictions for a particular application.

Input: Intent's data URI set with an application name, using the "package" schema (like "package:com.my.app").

Output: Nothing.

Applications can also use `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager.html#getRestrictBackgroundStatus()` to determine the status of the background data restrictions for them.

In some cases, a matching Activity may not exist, so ensure you safeguard against this.

 Value: "android.settings.IGNORE_BACKGROUND_DATA_RESTRICTIONS_SETTINGS"

### ACTION_IGNORE_BATTERY_OPTIMIZATION_SETTINGS

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_IGNORE_BATTERY_OPTIMIZATION_SETTINGS: String
```

Activity Action: Show screen for controlling which apps can ignore battery optimizations.

Input: Nothing.

Output: Nothing.

You can use `https://developer.android.com/reference/kotlin/android/os/PowerManager.html#isIgnoringBatteryOptimizations(kotlin.String)` to determine if an application is already ignoring optimizations. You can use `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_REQUEST_IGNORE_BATTERY_OPTIMIZATIONS:kotlin.String` to ask the user to put you on this list.

 Value: "android.settings.IGNORE_BATTERY_OPTIMIZATION_SETTINGS"

### ACTION_INPUT_METHOD_SETTINGS

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_INPUT_METHOD_SETTINGS: String
```

Activity Action: Show settings to configure input methods, in particular allowing the user to enable input methods.

In some cases, a matching Activity may not exist, so ensure you safeguard against this.

Input: Nothing.

Output: Nothing.

 Value: "android.settings.INPUT_METHOD_SETTINGS"

### ACTION_INPUT_METHOD_SUBTYPE_SETTINGS

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_INPUT_METHOD_SUBTYPE_SETTINGS: String
```

Activity Action: Show settings to enable/disable input method subtypes.

In some cases, a matching Activity may not exist, so ensure you safeguard against this.

To tell which input method's subtypes are displayed in the settings, add `https://developer.android.com/reference/kotlin/android/provider/Settings#EXTRA_INPUT_METHOD_ID:kotlin.String` extra to this Intent with the input method id. If there is no extra in this Intent, subtypes from all installed input methods will be displayed in the settings.

 Value: "android.settings.INPUT_METHOD_SUBTYPE_SETTINGS"

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodInfo.html#getId()`

### ACTION_INTERNAL_STORAGE_SETTINGS

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_INTERNAL_STORAGE_SETTINGS: String
```

Activity Action: Show settings for internal storage.

In some cases, a matching Activity may not exist, so ensure you safeguard against this.

Input: Nothing.

Output: Nothing.

 Value: "android.settings.INTERNAL_STORAGE_SETTINGS"

### ACTION_LOCALE_SETTINGS

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_LOCALE_SETTINGS: String
```

Activity Action: Show settings to allow configuration of locale.

In some cases, a matching Activity may not exist, so ensure you safeguard against this.

Input: The optional `EXTRA_EXPLICIT_LOCALES` with language tags that contains locales to limit available locales. This is only supported when device is under demo mode. If intent does not contain this extra, it will show system supported locale list. 
If `EXTRA_EXPLICIT_LOCALES` contain a unsupported locale, it will still show this locale on list, but may not be supported by the devcie. Output: Nothing.

 Value: "android.settings.LOCALE_SETTINGS"

### ACTION_LOCATION_SOURCE_SETTINGS

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_LOCATION_SOURCE_SETTINGS: String
```

Activity Action: Show settings to allow configuration of current location sources.

In some cases, a matching Activity may not exist, so ensure you safeguard against this.

Input: Nothing.

Output: Nothing.

 Value: "android.settings.LOCATION_SOURCE_SETTINGS"

### ACTION_MANAGE_ALL_APPLICATIONS_SETTINGS

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_MANAGE_ALL_APPLICATIONS_SETTINGS: String
```

Activity Action: Show settings to manage all applications.

In some cases, a matching Activity may not exist, so ensure you safeguard against this.

Input: Nothing.

Output: Nothing.

 Value: "android.settings.MANAGE_ALL_APPLICATIONS_SETTINGS"

### ACTION_MANAGE_ALL_FILES_ACCESS_PERMISSION

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_MANAGE_ALL_FILES_ACCESS_PERMISSION: String
```

Activity Action: Show screen for controlling which apps have access to manage external storage.

In some cases, a matching Activity may not exist, so ensure you safeguard against this.

If you want to control a specific app's access to manage external storage, use `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_MANAGE_APP_ALL_FILES_ACCESS_PERMISSION:kotlin.String` instead.

Output: Nothing.

 Value: "android.settings.MANAGE_ALL_FILES_ACCESS_PERMISSION"

**See Also**

- `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_MANAGE_APP_ALL_FILES_ACCESS_PERMISSION:kotlin.String`

### ACTION_MANAGE_ALL_SIM_PROFILES_SETTINGS

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_MANAGE_ALL_SIM_PROFILES_SETTINGS: String
```

Activity Action: Show settings to manage all SIM profiles.

In some cases, a matching Activity may not exist, so ensure you safeguard against this.

Input: Nothing.

Output: Nothing.

 Value: "android.settings.MANAGE_ALL_SIM_PROFILES_SETTINGS"

### ACTION_MANAGE_APPLICATIONS_SETTINGS

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_MANAGE_APPLICATIONS_SETTINGS: String
```

Activity Action: Show settings to manage installed applications.

In some cases, a matching Activity may not exist, so ensure you safeguard against this.

Input: Nothing.

Output: Nothing.

 Value: "android.settings.MANAGE_APPLICATIONS_SETTINGS"

### ACTION_MANAGE_APP_ALL_FILES_ACCESS_PERMISSION

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_MANAGE_APP_ALL_FILES_ACCESS_PERMISSION: String
```

Activity Action: Show screen for controlling if the app specified in the data URI of the intent can manage external storage.

Launching the corresponding activity requires the permission `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MANAGE_EXTERNAL_STORAGE:kotlin.String`.

In some cases, a matching Activity may not exist, so ensure you safeguard against this.

Input: The Intent's data URI MUST specify the application package name whose ability of managing external storage you want to control. For example "package:com.my.app".

Output: Nothing.

 Value: "android.settings.MANAGE_APP_ALL_FILES_ACCESS_PERMISSION"

**See Also**

- `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_MANAGE_ALL_FILES_ACCESS_PERMISSION:kotlin.String`

### ACTION_MANAGE_APP_USE_FULL_SCREEN_INTENT

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_MANAGE_APP_USE_FULL_SCREEN_INTENT: String
```

Activity Action: Show screen for controlling whether an app can send full screen intents.

Input: the intent's data URI must specify the application package name for which you want to manage full screen intents.

Output: Nothing.

 Value: "android.settings.MANAGE_APP_USE_FULL_SCREEN_INTENT"

### ACTION_MANAGE_ASSISTANT_AUDIO

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_MANAGE_ASSISTANT_AUDIO: String
```

Activity Action: Show screen for controlling if the app specified in the data URI of the intent has MANAGE_ASSISTANT_AUDIO special app access.

Input: The Intent's data URI MUST specify the application package name whose ability of managing assistant audio you want to control. For example "package:com.my.app".

Output: Nothing.

 Value: "android.settings.MANAGE_ASSISTANT_AUDIO"

### ACTION_MANAGE_CONTACTS

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_MANAGE_CONTACTS: String
```

Activity Action: Show screen for controlling which apps have access to manage contacts.

In some cases, a matching Activity may not exist, so ensure you safeguard against this.

Output: Nothing.

 Value: "android.settings.MANAGE_CONTACTS"

### ACTION_MANAGE_DEFAULT_APPS_SETTINGS

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_MANAGE_DEFAULT_APPS_SETTINGS: String
```

Activity Action: Show Default apps settings.

In some cases, a matching Activity may not exist, so ensure you safeguard against this.

Input: Nothing.

Output: Nothing.

 Value: "android.settings.MANAGE_DEFAULT_APPS_SETTINGS"

### ACTION_MANAGE_OVERLAY_PERMISSION

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_MANAGE_OVERLAY_PERMISSION: String
```

Activity Action: Show screen for controlling which apps can draw on top of other apps.

In some cases, a matching Activity may not exist, so ensure you safeguard against this.

Input: Optionally, in versions of Android prior to `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int`, the Intent's data URI can specify the application package name to directly invoke the management GUI specific to the package name. For example "package:com.my.app".

Output: Nothing.

 Value: "android.settings.action.MANAGE_OVERLAY_PERMISSION"

### ACTION_MANAGE_PERIPHERAL_CUSTOMIZATION

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_MANAGE_PERIPHERAL_CUSTOMIZATION: String
```

Activity Action: Show screen for controlling which apps are allowed to manage customizations for peripherals.

In some cases, a matching Activity may not exist, so ensure you safeguard against this.

Input: The Intent's data URI can specify the application package name to directly invoke the management GUI specific to the package name. For example "package:com.my.app".

Output: Nothing.

 Value: "android.settings.MANAGE_PERIPHERAL_CUSTOMIZATION"

### ACTION_MANAGE_SUPERVISOR_RESTRICTED_SETTING

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_MANAGE_SUPERVISOR_RESTRICTED_SETTING: String
```

Activity action: Launch UI to manage a setting restricted by supervisors.

Input: `https://developer.android.com/reference/kotlin/android/provider/Settings#EXTRA_SUPERVISOR_RESTRICTED_SETTING_KEY:kotlin.String` specifies what setting to open.

Output: Nothing.

 Value: "android.settings.MANAGE_SUPERVISOR_RESTRICTED_SETTING"

### ACTION_MANAGE_UNKNOWN_APP_SOURCES

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_MANAGE_UNKNOWN_APP_SOURCES: String
```

Activity Action: Show settings to allow configuration of trusted external sources Input: Optionally, the Intent's data URI can specify the application package name to directly invoke the management GUI specific to the package name. For example "package:com.my.app".

Output: Nothing.

 Value: "android.settings.MANAGE_UNKNOWN_APP_SOURCES"

### ACTION_MANAGE_WRITE_SETTINGS

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_MANAGE_WRITE_SETTINGS: String
```

Activity Action: Show screen for controlling which apps are allowed to write/modify system settings.

In some cases, a matching Activity may not exist, so ensure you safeguard against this.

Input: Optionally, the Intent's data URI can specify the application package name to directly invoke the management GUI specific to the package name. For example "package:com.my.app".

Output: Nothing.

 Value: "android.settings.action.MANAGE_WRITE_SETTINGS"

### ACTION_MEASUREMENT_SYSTEM_SETTINGS

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_MEASUREMENT_SYSTEM_SETTINGS: String
```

Activity Action: Show measurement system configuration settings.

Input: Nothing.

Output: Nothing.

 Value: "android.settings.MEASUREMENT_SYSTEM_SETTINGS"

### ACTION_MEMORY_CARD_SETTINGS

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_MEMORY_CARD_SETTINGS: String
```

Activity Action: Show settings for memory card storage.

In some cases, a matching Activity may not exist, so ensure you safeguard against this.

Input: Nothing.

Output: Nothing.

 Value: "android.settings.MEMORY_CARD_SETTINGS"

### ACTION_NETWORK_OPERATOR_SETTINGS

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_NETWORK_OPERATOR_SETTINGS: String
```

Activity Action: Show settings for selecting the network operator.

In some cases, a matching Activity may not exist, so ensure you safeguard against this.

The subscription ID of the subscription for which available network operators should be displayed may be optionally specified with `https://developer.android.com/reference/kotlin/android/provider/Settings#EXTRA_SUB_ID:kotlin.String`.

Input: Nothing.

Output: Nothing.

 Value: "android.settings.NETWORK_OPERATOR_SETTINGS"

### ACTION_NFCSHARING_SETTINGS

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_NFCSHARING_SETTINGS: String
```

Activity Action: Show NFC Sharing settings.

This shows UI that allows NDEF Push (Android Beam) to be turned on or off.

In some cases, a matching Activity may not exist, so ensure you safeguard against this.

Input: Nothing.

Output: Nothing

 Value: "android.settings.NFCSHARING_SETTINGS"

### ACTION_NFC_PAYMENT_SETTINGS

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_NFC_PAYMENT_SETTINGS: String
```

Activity Action: Show NFC Tap \& Pay settings

This shows UI that allows the user to configure Tap\&Pay settings.

In some cases, a matching Activity may not exist, so ensure you safeguard against this.

Input: Nothing.

Output: Nothing

 Value: "android.settings.NFC_PAYMENT_SETTINGS"

### ACTION_NFC_SETTINGS

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_NFC_SETTINGS: String
```

Activity Action: Show NFC settings.

This shows UI that allows NFC to be turned on or off.

In some cases, a matching Activity may not exist, so ensure you safeguard against this.

Input: Nothing.

Output: Nothing

 Value: "android.settings.NFC_SETTINGS"

**See Also**

- `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter.html#isEnabled()`

### ACTION_NIGHT_DISPLAY_SETTINGS

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_NIGHT_DISPLAY_SETTINGS: String
```

Activity Action: Show settings to allow configuration of Night display.

In some cases, a matching Activity may not exist, so ensure you safeguard against this.

Input: Nothing.

Output: Nothing.

 Value: "android.settings.NIGHT_DISPLAY_SETTINGS"

### ACTION_NOTIFICATION_ASSISTANT_SETTINGS

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_NOTIFICATION_ASSISTANT_SETTINGS: String
```

Activity Action: Show Notification assistant settings.

In some cases, a matching Activity may not exist, so ensure you safeguard against this.

Input: Nothing.

Output: Nothing.

 Value: "android.settings.NOTIFICATION_ASSISTANT_SETTINGS"

### ACTION_NOTIFICATION_LISTENER_DETAIL_SETTINGS

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_NOTIFICATION_LISTENER_DETAIL_SETTINGS: String
```

Activity Action: Show notification listener permission settings page for app.

Users can grant and deny access to notifications for a `https://developer.android.com/reference/kotlin/android/content/ComponentName.html#` from here. See `https://developer.android.com/reference/kotlin/android/app/NotificationManager.html#isNotificationListenerAccessGranted(android.content.ComponentName)` for more details.

Input: The extra `https://developer.android.com/reference/kotlin/android/provider/Settings#EXTRA_NOTIFICATION_LISTENER_COMPONENT_NAME:kotlin.String` containing the name of the component to grant or revoke notification listener access to.

Output: Nothing.

 Value: "android.settings.NOTIFICATION_LISTENER_DETAIL_SETTINGS"

### ACTION_NOTIFICATION_LISTENER_SETTINGS

Added in [API level 22](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_NOTIFICATION_LISTENER_SETTINGS: String
```

Activity Action: Show Notification listener settings.

In some cases, a matching Activity may not exist, so ensure you safeguard against this.

Input: Nothing.

Output: Nothing.

 Value: "android.settings.ACTION_NOTIFICATION_LISTENER_SETTINGS"

**See Also**

- `https://developer.android.com/reference/kotlin/android/service/notification/NotificationListenerService.html#`

### ACTION_NOTIFICATION_POLICY_ACCESS_SETTINGS

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_NOTIFICATION_POLICY_ACCESS_SETTINGS: String
```

Activity Action: Show Notification Policy access settings.

Users can grant and deny access to Notification Policy (DND / Modes) configuration from here. Managed profiles cannot grant Notification Policy access. See `https://developer.android.com/reference/kotlin/android/app/NotificationManager.html#isNotificationPolicyAccessGranted()` for more details.

Input: Nothing.

Output: Nothing.

In some cases, a matching Activity may not exist, so ensure you safeguard against this.

 Value: "android.settings.NOTIFICATION_POLICY_ACCESS_SETTINGS"

### ACTION_PRINT_SETTINGS

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_PRINT_SETTINGS: String
```

Activity Action: Show the top level print settings.

In some cases, a matching Activity may not exist, so ensure you safeguard against this.

Input: Nothing.

Output: Nothing.

 Value: "android.settings.ACTION_PRINT_SETTINGS"

### ACTION_PRIVACY_SETTINGS

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_PRIVACY_SETTINGS: String
```

Activity Action: Show settings to allow configuration of privacy options, i.e. permission manager, privacy dashboard, privacy controls and more.

In some cases, a matching Activity may not exist, so ensure you safeguard against this.

Input: Nothing.

Output: Nothing.

 Value: "android.settings.PRIVACY_SETTINGS"

### ACTION_PROCESS_WIFI_EASY_CONNECT_URI

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_PROCESS_WIFI_EASY_CONNECT_URI: String
```

Activity Action: Show setting page to process a Wi-Fi Easy Connect (aka DPP) URI and start configuration. This intent should be used when you want to use this device to take on the configurator role for an IoT/other device. When provided with a valid DPP URI string, Settings will open a Wi-Fi selection screen for the user to indicate which network they would like to configure the device specified in the DPP URI string and carry them through the rest of the flow for provisioning the device.

In some cases, a matching Activity may not exist, so ensure to safeguard against this by checking `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager.html#isEasyConnectSupported()`.

Input: The Intent's data URI specifies bootstrapping information for authenticating and provisioning the peer, and uses a "DPP" scheme. The URI should be attached to the intent using `https://developer.android.com/reference/kotlin/android/content/Intent.html#setData(android.net.Uri)`. The calling app can obtain a DPP URI in any way, e.g. by scanning a QR code or other out-of-band methods. The calling app may also attach the `https://developer.android.com/reference/kotlin/android/provider/Settings#EXTRA_EASY_CONNECT_BAND_LIST:kotlin.String` extra to provide information about the bands supported by the enrollee device.

Output: After calling android.app.Activity#startActivityForResult, the callback `onActivityResult` will have resultCode `https://developer.android.com/reference/kotlin/android/app/Activity.html#RESULT_OK:kotlin.Int` if the Wi-Fi Easy Connect configuration succeeded and the user tapped the 'Done' button, or `https://developer.android.com/reference/kotlin/android/app/Activity.html#RESULT_CANCELED:kotlin.Int` if the operation failed and user tapped the 'Cancel' button. In case the operation has failed, a status code from `https://developer.android.com/reference/kotlin/android/net/wifi/EasyConnectStatusCallback.html#` `EASY_CONNECT_EVENT_FAILURE_*` will be returned as an Extra `https://developer.android.com/reference/kotlin/android/provider/Settings#EXTRA_EASY_CONNECT_ERROR_CODE:kotlin.String`. Easy Connect R2 Enrollees report additional details about the error they encountered, which will be provided in the `https://developer.android.com/reference/kotlin/android/provider/Settings#EXTRA_EASY_CONNECT_ATTEMPTED_SSID:kotlin.String`, `https://developer.android.com/reference/kotlin/android/provider/Settings#EXTRA_EASY_CONNECT_CHANNEL_LIST:kotlin.String`, and `https://developer.android.com/reference/kotlin/android/provider/Settings#EXTRA_EASY_CONNECT_BAND_LIST:kotlin.String`.

 Value: "android.settings.PROCESS_WIFI_EASY_CONNECT_URI"

### ACTION_QUICK_ACCESS_WALLET_SETTINGS

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_QUICK_ACCESS_WALLET_SETTINGS: String
```

Activity Action: Show screen for controlling the Quick Access Wallet.

In some cases, a matching Activity may not exist, so ensure you safeguard against this.

Input: Nothing.

Output: Nothing.

 Value: "android.settings.QUICK_ACCESS_WALLET_SETTINGS"

### ACTION_QUICK_LAUNCH_SETTINGS

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_QUICK_LAUNCH_SETTINGS: String
```

Activity Action: Show settings to allow configuration of quick launch shortcuts.

In some cases, a matching Activity may not exist, so ensure you safeguard against this.

Input: Nothing.

Output: Nothing.

 Value: "android.settings.QUICK_LAUNCH_SETTINGS"

### ACTION_REGIONAL_PREFERENCES_SETTINGS

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_REGIONAL_PREFERENCES_SETTINGS: String
```

Activity Action: Show settings to allow configuration of regional preferences

Input: Nothing

Output: Nothing.

 Value: "android.settings.REGIONAL_PREFERENCES_SETTINGS"

### ACTION_REGION_SETTINGS

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_REGION_SETTINGS: String
```

Activity Action: Show screen for allowing the region configuration.

Input: Nothing.

Output: Nothing.

 Value: "android.settings.REGION_SETTINGS"

### ACTION_REQUEST_IGNORE_BATTERY_OPTIMIZATIONS

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_REQUEST_IGNORE_BATTERY_OPTIMIZATIONS: String
```

Activity Action: Ask the user to allow an app to ignore battery optimizations (that is, put them on the allowlist of apps shown by `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_IGNORE_BATTERY_OPTIMIZATION_SETTINGS:kotlin.String`). For an app to use this, it also must hold the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#REQUEST_IGNORE_BATTERY_OPTIMIZATIONS:kotlin.String` permission.

**Note:** most applications should *not* use this; there are many facilities provided by the platform for applications to operate correctly in the various power saving modes. This is only for unusual applications that need to deeply control their own execution, at the potential expense of the user's battery life. Note that these applications greatly run the risk of showing to the user as high power consumers on their device.

Input: The Intent's data URI must specify the application package name to be shown, with the "package" scheme. That is "package:com.my.app".

Output: Nothing.

You can use `https://developer.android.com/reference/kotlin/android/os/PowerManager.html#isIgnoringBatteryOptimizations(kotlin.String)` to determine if an application is already ignoring optimizations.

 Value: "android.settings.REQUEST_IGNORE_BATTERY_OPTIMIZATIONS"

### ACTION_REQUEST_MANAGE_MEDIA

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_REQUEST_MANAGE_MEDIA: String
```

Activity Action: Show settings to allow configuration of `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MANAGE_MEDIA:kotlin.String` permission Input: Optionally, the Intent's data URI can specify the application package name to directly invoke the management GUI specific to the package name. For example "package:com.my.app".

Output: Nothing.

 Value: "android.settings.REQUEST_MANAGE_MEDIA"

### ACTION_REQUEST_MEDIA_ROUTING_CONTROL

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_REQUEST_MEDIA_ROUTING_CONTROL: String
```

Activity Action: Show settings to allow configuration of `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MEDIA_ROUTING_CONTROL:kotlin.String` permission. Input: Optionally, the Intent's data URI can specify the application package name to directly invoke the management GUI specific to the package name. For example "package:com.my.app". However, modifying this permission setting for any package is allowed only when that package holds an appropriate companion device profile such as `https://developer.android.com/reference/kotlin/android/companion/AssociationRequest.html#DEVICE_PROFILE_WATCH:kotlin.String`.

Output: Nothing.

 Value: "android.settings.REQUEST_MEDIA_ROUTING_CONTROL"

### ACTION_REQUEST_SCHEDULE_EXACT_ALARM

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_REQUEST_SCHEDULE_EXACT_ALARM: String
```

Activity Action: Show settings to allow configuration of `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#SCHEDULE_EXACT_ALARM:kotlin.String` permission Input: Optionally, the Intent's data URI can specify the application package name to directly invoke the management GUI specific to the package name. For example "package:com.my.app".

Output: When a package data uri is passed as input, the activity result is set to `https://developer.android.com/reference/kotlin/android/app/Activity.html#RESULT_OK:kotlin.Int` if the permission was granted to the app. Otherwise, the result is set to `https://developer.android.com/reference/kotlin/android/app/Activity.html#RESULT_CANCELED:kotlin.Int`.

 Value: "android.settings.REQUEST_SCHEDULE_EXACT_ALARM"

### ACTION_REQUEST_SET_AUTOFILL_SERVICE

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_REQUEST_SET_AUTOFILL_SERVICE: String
```

Activity Action: Show screen that let user select its Autofill Service.

Input: Intent's data URI set with an application package name, using the "package" schema (like "package:com.my.app").

Output: `https://developer.android.com/reference/kotlin/android/app/Activity.html#RESULT_OK:kotlin.Int` if user selected an Autofill Service belonging to the caller package.

**NOTE:** Applications should call `https://developer.android.com/reference/kotlin/android/view/autofill/AutofillManager.html#hasEnabledAutofillServices()` and `https://developer.android.com/reference/kotlin/android/view/autofill/AutofillManager.html#isAutofillSupported()`, and only use this action to start an activity if they return `false` and `true` respectively.

 Value: "android.settings.REQUEST_SET_AUTOFILL_SERVICE"

### ACTION_SATELLITE_SETTING

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_SATELLITE_SETTING: String
```

Activity Action: Show settings to provide guide about carrier satellite messaging.

In some cases, a matching Activity may not exist, so ensure you safeguard against this.

Input: Nothing.

Output: Nothing.

 Value: "android.settings.SATELLITE_SETTING"

### ACTION_SEARCH_SETTINGS

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_SEARCH_SETTINGS: String
```

Activity Action: Show settings for global search.

In some cases, a matching Activity may not exist, so ensure you safeguard against this.

Input: Nothing.

Output: Nothing

 Value: "android.search.action.SEARCH_SETTINGS"

### ACTION_SECURITY_SETTINGS

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_SECURITY_SETTINGS: String
```

Activity Action: Show settings to allow configuration of security and location privacy.

In some cases, a matching Activity may not exist, so ensure you safeguard against this.

Input: Nothing.

Output: Nothing.

 Value: "android.settings.SECURITY_SETTINGS"

### ACTION_SETTINGS

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_SETTINGS: String
```

Activity Action: Show system settings.

Input: Nothing.

Output: Nothing.

 Value: "android.settings.SETTINGS"

### ACTION_SETTINGS_EMBED_DEEP_LINK_ACTIVITY

Added in [API level 32](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_SETTINGS_EMBED_DEEP_LINK_ACTIVITY: String
```

Activity Action: For system or preinstalled apps to show their `https://developer.android.com/reference/kotlin/android/app/Activity.html#` embedded in Settings app on large screen devices. Developers should resolve the Intent action before using it.

Input: `https://developer.android.com/reference/kotlin/android/provider/Settings#EXTRA_SETTINGS_EMBEDDED_DEEP_LINK_INTENT_URI:kotlin.String` must be included to specify the intent for the activity which will be embedded in Settings app. It's an intent URI string from `intent.toUri(Intent.URI_INTENT_SCHEME)`. Input: `https://developer.android.com/reference/kotlin/android/provider/Settings#EXTRA_SETTINGS_EMBEDDED_DEEP_LINK_HIGHLIGHT_MENU_KEY:kotlin.String` must be included to specify a key that indicates the menu item which will be highlighted on settings home menu.

Output: Nothing.

 Value: "android.settings.SETTINGS_EMBED_DEEP_LINK_ACTIVITY"

### ACTION_SHOW_REGULATORY_INFO

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_SHOW_REGULATORY_INFO: String
```

Activity Action: Show the regulatory information screen for the device.

In some cases, a matching Activity may not exist, so ensure you safeguard against this.

Input: Nothing.

Output: Nothing.

 Value: "android.settings.SHOW_REGULATORY_INFO"

### ACTION_SHOW_WORK_POLICY_INFO

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_SHOW_WORK_POLICY_INFO: String
```

Activity Action: Show Work Policy info. DPC apps can implement an activity that handles this intent in order to show device policies associated with the work profile or managed device.

Input: Nothing.

Output: Nothing.

 Value: "android.settings.SHOW_WORK_POLICY_INFO"

### ACTION_SOUND_SETTINGS

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_SOUND_SETTINGS: String
```

Activity Action: Show settings to allow configuration of sound and volume.

In some cases, a matching Activity may not exist, so ensure you safeguard against this.

Input: Nothing.

Output: Nothing.

 Value: "android.settings.SOUND_SETTINGS"

### ACTION_STORAGE_VOLUME_ACCESS_SETTINGS

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_STORAGE_VOLUME_ACCESS_SETTINGS: String
```

**Deprecated:** *use `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_APPLICATION_DETAILS_SETTINGS:kotlin.String` to manage storage permissions for a specific application*

Activity Action: Show screen for controlling which apps have access on volume directories.

Input: Nothing.

Output: Nothing.

Applications typically use this action to ask the user to revert the "Do not ask again" status of directory access requests made by `https://developer.android.com/reference/kotlin/android/os/storage/StorageVolume.html#createAccessIntent(kotlin.String)`.

 Value: "android.settings.STORAGE_VOLUME_ACCESS_SETTINGS"

### ACTION_SUPERVISION_SETTINGS

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_SUPERVISION_SETTINGS: String
```

Activity Action: Show screen to manage supervision settings.

Input: Nothing.

Output: Nothing.

 Value: "android.settings.SUPERVISION_SETTINGS"

### ACTION_SYNC_SETTINGS

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_SYNC_SETTINGS: String
```

Activity Action: Show settings to allow configuration of sync settings.

In some cases, a matching Activity may not exist, so ensure you safeguard against this.

The account types available to add via the add account button may be restricted by adding an `https://developer.android.com/reference/kotlin/android/provider/Settings#EXTRA_AUTHORITIES:kotlin.String` extra to this Intent with one or more syncable content provider's authorities. Only account types which can sync with that content provider will be offered to the user.

Input: Nothing.

Output: Nothing.

 Value: "android.settings.SYNC_SETTINGS"

### ACTION_SYSTEM_UPDATE_SETTINGS

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_SYSTEM_UPDATE_SETTINGS: String
```

Activity Action: Show settings for system update functionality.

In some cases, a matching Activity may not exist, so ensure you safeguard against this.

This intent is designed to be handled by a system component. To securely launch this intent, resolve the intent to a system application and verify that its priority is higher than the default value (0). This prevents other apps from intercepting the intent. If multiple system applications can handle this intent, the component with the highest priority will be launched.

For example:

```kotlin
final PackageManager pm = context.getPackageManager();
  final Intent intent = new Intent(Settings.ACTION_SYSTEM_UPDATE_SETTINGS);
  final List<ResolveInfo> resolveInfos =
          pm.queryIntentActivities(intent, PackageManager.MATCH_SYSTEM_ONLY);
  // ... find the ResolveInfo with the highest priority, ensure it's > 0, and launch it.
  
```

Input: Nothing.

Output: Nothing.

 Value: "android.settings.SYSTEM_UPDATE_SETTINGS"

### ACTION_TEMPERATURE_UNIT_SETTINGS

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_TEMPERATURE_UNIT_SETTINGS: String
```

Activity Action: Show temperature unit configuration settings.

Input: Nothing.

Output: Nothing.

 Value: "android.settings.TEMPERATURE_UNIT_SETTINGS"

### ACTION_USAGE_ACCESS_SETTINGS

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_USAGE_ACCESS_SETTINGS: String
```

Activity Action: Show settings to control access to usage information.

In some cases, a matching Activity may not exist, so ensure you safeguard against this.

Input: Nothing.

Output: Nothing.

 Value: "android.settings.USAGE_ACCESS_SETTINGS"

### ACTION_USER_DICTIONARY_SETTINGS

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_USER_DICTIONARY_SETTINGS: String
```

Activity Action: Show settings to manage the user input dictionary.

Starting with `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#KITKAT:kotlin.Int`, it is guaranteed there will always be an appropriate implementation for this Intent action. In prior releases of the platform this was optional, so ensure you safeguard against it.

Input: Nothing.

Output: Nothing.

 Value: "android.settings.USER_DICTIONARY_SETTINGS"

### ACTION_VOICE_CONTROL_AIRPLANE_MODE

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_VOICE_CONTROL_AIRPLANE_MODE: String
```

Activity Action: Modify Airplane mode settings using a voice command.

In some cases, a matching Activity may not exist, so ensure you safeguard against this.

This intent MUST be started using `https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession.html#startVoiceActivity(android.content.Intent)`.

Note: The activity implementing this intent MUST verify that `https://developer.android.com/reference/kotlin/android/app/Activity.html#isVoiceInteraction()` returns true before modifying the setting.

Input: To tell which state airplane mode should be set to, add the `https://developer.android.com/reference/kotlin/android/provider/Settings#EXTRA_AIRPLANE_MODE_ENABLED:kotlin.String` extra to this Intent with the state specified. If the extra is not included, no changes will be made.

Output: Nothing.

 Value: "android.settings.VOICE_CONTROL_AIRPLANE_MODE"

### ACTION_VOICE_CONTROL_BATTERY_SAVER_MODE

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_VOICE_CONTROL_BATTERY_SAVER_MODE: String
```

Activity Action: Modify Battery Saver mode setting using a voice command.

In some cases, a matching Activity may not exist, so ensure you safeguard against this.

This intent MUST be started using `https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession.html#startVoiceActivity(android.content.Intent)`.

Note: The activity implementing this intent MUST verify that `https://developer.android.com/reference/kotlin/android/app/Activity.html#isVoiceInteraction()` returns true before modifying the setting.

Input: To tell which state batter saver mode should be set to, add the `https://developer.android.com/reference/kotlin/android/provider/Settings#EXTRA_BATTERY_SAVER_MODE_ENABLED:kotlin.String` extra to this Intent with the state specified. If the extra is not included, no changes will be made.

Output: Nothing.

 Value: "android.settings.VOICE_CONTROL_BATTERY_SAVER_MODE"

### ACTION_VOICE_CONTROL_DO_NOT_DISTURB_MODE

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_VOICE_CONTROL_DO_NOT_DISTURB_MODE: String
```

Activity Action: Modify do not disturb mode settings.

In some cases, a matching Activity may not exist, so ensure you safeguard against this.

This intent MUST be started using `https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession.html#startVoiceActivity(android.content.Intent)`.

Note: The Activity implementing this intent MUST verify that `https://developer.android.com/reference/kotlin/android/app/Activity.html#isVoiceInteraction()`. returns true before modifying the setting.

Input: The optional `https://developer.android.com/reference/kotlin/android/provider/Settings#EXTRA_DO_NOT_DISTURB_MODE_MINUTES:kotlin.String` extra can be used to indicate how long the user wishes to avoid interruptions for. The optional `https://developer.android.com/reference/kotlin/android/provider/Settings#EXTRA_DO_NOT_DISTURB_MODE_ENABLED:kotlin.String` extra can be to indicate if the user is enabling or disabling do not disturb mode. If either extra is not included, the user maybe asked to provide the value.

Output: Nothing.

 Value: "android.settings.VOICE_CONTROL_DO_NOT_DISTURB_MODE"

### ACTION_VOICE_INPUT_SETTINGS

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_VOICE_INPUT_SETTINGS: String
```

Activity Action: Show settings to configure input methods, in particular allowing the user to enable input methods.

In some cases, a matching Activity may not exist, so ensure you safeguard against this.

Input: Nothing.

Output: Nothing.

 Value: "android.settings.VOICE_INPUT_SETTINGS"

### ACTION_VPN_APP_EXCLUSION_SETTINGS

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_VPN_APP_EXCLUSION_SETTINGS: String
```

Activity Action: Show a settings screen to configure application exclusions for the calling package's `https://developer.android.com/reference/kotlin/android/net/VpnManager.html#` VPN.

Invoking this Intent with android.app.Activity#startActivity displays a screen allowing the user to select applications that will be excluded from the calling package's `https://developer.android.com/reference/kotlin/android/net/VpnManager.html#` VPN. Exclusion changes will take effect immediately if the VPN is already running, or the next time the VPN is started.

The presence of this activity is not guaranteed on all devices; accordingly callers should verify `https://developer.android.com/reference/kotlin/android/content/Intent.html#resolveActivity(android.content.pm.PackageManager)` prior to android.app.Activity#startActivity or catch `https://developer.android.com/reference/kotlin/android/content/ActivityNotFoundException.html#`.

Input: Nothing.

Output: Nothing.

 Value: "android.settings.VPN_APP_EXCLUSION_SETTINGS"

### ACTION_VPN_SETTINGS

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_VPN_SETTINGS: String
```

Activity Action: Show settings to allow configuration of VPN.

In some cases, a matching Activity may not exist, so ensure you safeguard against this.

Input: Nothing.

Output: Nothing.

 Value: "android.settings.VPN_SETTINGS"

### ACTION_VR_LISTENER_SETTINGS

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_VR_LISTENER_SETTINGS: String
```

Activity Action: Show VR listener settings.

Input: Nothing.

Output: Nothing.

 Value: "android.settings.VR_LISTENER_SETTINGS"

**See Also**

- `https://developer.android.com/reference/kotlin/android/service/vr/VrListenerService.html#`

### ACTION_WEBVIEW_SETTINGS

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_WEBVIEW_SETTINGS: String
```

Activity Action: Allows user to select current webview implementation.

Input: Nothing.

Output: Nothing.

In some cases, a matching Activity may not exist, so ensure you safeguard against this.

 Value: "android.settings.WEBVIEW_SETTINGS"

### ACTION_WIFI_ADD_NETWORKS

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_WIFI_ADD_NETWORKS: String
```

Activity Action: Show setting page to process the addition of Wi-Fi networks to the user's saved network list. The app should send a new intent with an extra that holds a maximum of five `https://developer.android.com/reference/kotlin/android/net/wifi/WifiNetworkSuggestion.html#` that specify credentials for the networks to be added to the user's database. The Intent should be sent via the `https://developer.android.com/reference/kotlin/android/app/Activity.html#startActivityForResult(android.content.Intent,%20kotlin.Int)` API.

Note: The app sending the Intent to add the credentials doesn't get any ownership over the newly added network(s). For the Wi-Fi stack, these networks will look like the user manually added them from the Settings UI.

Input: The app should put parcelable array list of `https://developer.android.com/reference/kotlin/android/net/wifi/WifiNetworkSuggestion.html#` into the `https://developer.android.com/reference/kotlin/android/provider/Settings#EXTRA_WIFI_NETWORK_LIST:kotlin.String` extra.

Output: After `https://developer.android.com/reference/kotlin/android/app/Activity.html#startActivityForResult(android.content.Intent,%20kotlin.Int)`, the callback `https://developer.android.com/reference/kotlin/android/app/Activity.html#onActivityResult(kotlin.Int,%20kotlin.Int,%20android.content.Intent)` will have a result code `https://developer.android.com/reference/kotlin/android/app/Activity.html#RESULT_OK:kotlin.Int` to indicate user pressed the save button to save the networks or `https://developer.android.com/reference/kotlin/android/app/Activity.html#RESULT_CANCELED:kotlin.Int` to indicate that the user rejected the request. Additionally, an integer array list, stored in `https://developer.android.com/reference/kotlin/android/provider/Settings#EXTRA_WIFI_NETWORK_RESULT_LIST:kotlin.String`, will indicate the process result of each network.

 Value: "android.settings.WIFI_ADD_NETWORKS"

### ACTION_WIFI_IP_SETTINGS

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_WIFI_IP_SETTINGS: String
```

Activity Action: Show settings to allow configuration of a static IP address for Wi-Fi.

In some cases, a matching Activity may not exist, so ensure you safeguard against this.

Input: Nothing.

Output: Nothing.

 Value: "android.settings.WIFI_IP_SETTINGS"

### ACTION_WIFI_SETTINGS

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_WIFI_SETTINGS: String
```

Activity Action: Show settings to allow configuration of Wi-Fi.

In some cases, a matching Activity may not exist, so ensure you safeguard against this.

Input: Nothing.

Output: Nothing.

 Value: "android.settings.WIFI_SETTINGS"

### ACTION_WIRELESS_SETTINGS

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_WIRELESS_SETTINGS: String
```

Activity Action: Show settings to allow configuration of wireless controls such as Wi-Fi, Bluetooth and Mobile networks.

In some cases, a matching Activity may not exist, so ensure you safeguard against this.

Input: Nothing.

Output: Nothing.

 Value: "android.settings.WIRELESS_SETTINGS"

### ACTION_ZEN_MODE_PRIORITY_SETTINGS

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_ZEN_MODE_PRIORITY_SETTINGS: String
```

Activity Action: Show Zen Mode (aka Do Not Disturb) priority configuration settings.

 Value: "android.settings.ZEN_MODE_PRIORITY_SETTINGS"

### ADD_WIFI_RESULT_ADD_OR_UPDATE_FAILED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ADD_WIFI_RESULT_ADD_OR_UPDATE_FAILED: Int
```

A result of `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_WIFI_ADD_NETWORKS:kotlin.String` intent action that saving the corresponding Wi-Fi network failed.

 Value: 1

### ADD_WIFI_RESULT_ALREADY_EXISTS

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ADD_WIFI_RESULT_ALREADY_EXISTS: Int
```

A result of `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_WIFI_ADD_NETWORKS:kotlin.String` intent action that indicates the Wi-Fi network already exists.

 Value: 2

### ADD_WIFI_RESULT_SUCCESS

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ADD_WIFI_RESULT_SUCCESS: Int
```

A result of `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_WIFI_ADD_NETWORKS:kotlin.String` intent action that saving or updating the corresponding Wi-Fi network was successful.

 Value: 0

### AUTHORITY

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AUTHORITY: String
```

 Value: "settings"

### EXTRA_ACCOUNT_TYPES

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_ACCOUNT_TYPES: String
```

Activity Extra: Limit available options in launched activity based on the given account types.

This can be passed as an extra field in an Activity Intent with one or more account types as a String\[\]. This field is used by some intents to alter the behavior of the called activity.

Example: The `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_ADD_ACCOUNT:kotlin.String` intent restricts the account types to the specified list.

 Value: "account_types"

### EXTRA_AIRPLANE_MODE_ENABLED

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_AIRPLANE_MODE_ENABLED: String
```

Activity Extra: Enable or disable Airplane Mode.

This can be passed as an extra field to the `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_VOICE_CONTROL_AIRPLANE_MODE:kotlin.String` intent as a boolean to indicate if it should be enabled.

 Value: "airplane_mode_enabled"

### EXTRA_APP_PACKAGE

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_APP_PACKAGE: String
```

Activity Extra: The package owner of the notification channel settings to display.

This must be passed as an extra field to the `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_CHANNEL_NOTIFICATION_SETTINGS:kotlin.String`.

 Value: "android.provider.extra.APP_PACKAGE"

### EXTRA_AUTHORITIES

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_AUTHORITIES: String
```

Activity Extra: Limit available options in launched activity based on the given authority.

This can be passed as an extra field in an Activity Intent with one or more syncable content provider's authorities as a String\[\]. This field is used by some intents to alter the behavior of the called activity.

Example: The `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_ADD_ACCOUNT:kotlin.String` intent restricts the account types available based on the authority given.

 Value: "authorities"

### EXTRA_AUTOMATIC_ZEN_RULE_ID

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_AUTOMATIC_ZEN_RULE_ID: String
```

Activity Extra: The String id of the `https://developer.android.com/reference/kotlin/android/app/AutomaticZenRule.html#` settings to display.

This must be passed as an extra field to the `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_AUTOMATIC_ZEN_RULE_SETTINGS:kotlin.String`.

 Value: "android.provider.extra.AUTOMATIC_ZEN_RULE_ID"

### EXTRA_BATTERY_SAVER_MODE_ENABLED

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_BATTERY_SAVER_MODE_ENABLED: String
```

Activity Extra: Enable or disable Battery saver mode.

This can be passed as an extra field to the `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_VOICE_CONTROL_BATTERY_SAVER_MODE:kotlin.String` intent as a boolean to indicate if it should be enabled.

 Value: "android.settings.extra.battery_saver_mode_enabled"

### EXTRA_BIOMETRIC_AUTHENTICATORS_ALLOWED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_BIOMETRIC_AUTHENTICATORS_ALLOWED: String
```

Activity Extra: The minimum strength to request enrollment for.

This can be passed as an extra field to the `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_BIOMETRIC_ENROLL:kotlin.String` intent to indicate that only enrollment for sensors that meet these requirements should be shown. The value should be a combination of the constants defined in `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricManager.Authenticators.html#`.

 Value: "android.provider.extra.BIOMETRIC_AUTHENTICATORS_ALLOWED"

### EXTRA_CHANNEL_FILTER_LIST

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_CHANNEL_FILTER_LIST: String
```

Activity Extra: An `Arraylist<String>` of `https://developer.android.com/reference/kotlin/android/app/NotificationChannel.html#` field names to show on the Settings UI.

This is an optional extra field to the `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_CHANNEL_NOTIFICATION_SETTINGS:kotlin.String`. If included the system will filter out any Settings that doesn't appear in this list that otherwise would display.

 Value: "android.provider.extra.CHANNEL_FILTER_LIST"

### EXTRA_CHANNEL_ID

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_CHANNEL_ID: String
```

Activity Extra: The `https://developer.android.com/reference/kotlin/android/app/NotificationChannel.html#getId()` of the notification channel settings to display.

This must be passed as an extra field to the `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_CHANNEL_NOTIFICATION_SETTINGS:kotlin.String`.

 Value: "android.provider.extra.CHANNEL_ID"

### EXTRA_CONVERSATION_ID

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_CONVERSATION_ID: String
```

Activity Extra: The `https://developer.android.com/reference/kotlin/android/app/NotificationChannel.html#getConversationId()` of the notification conversation settings to display.

This is an optional extra field to the `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_CHANNEL_NOTIFICATION_SETTINGS:kotlin.String`. If included the system will first look up notification settings by channel and conversation id, and will fall back to channel id if a specialized channel for this conversation doesn't exist, similar to `https://developer.android.com/reference/kotlin/android/app/NotificationManager.html#getNotificationChannel(kotlin.String,%20kotlin.String)`.

 Value: "android.provider.extra.CONVERSATION_ID"

### EXTRA_DO_NOT_DISTURB_MODE_ENABLED

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_DO_NOT_DISTURB_MODE_ENABLED: String
```

Activity Extra: Enable or disable Do Not Disturb mode.

This can be passed as an extra field to the `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_VOICE_CONTROL_DO_NOT_DISTURB_MODE:kotlin.String` intent as a boolean to indicate if it should be enabled.

 Value: "android.settings.extra.do_not_disturb_mode_enabled"

### EXTRA_DO_NOT_DISTURB_MODE_MINUTES

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_DO_NOT_DISTURB_MODE_MINUTES: String
```

Activity Extra: How many minutes to enable do not disturb mode for.

This can be passed as an extra field to the `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_VOICE_CONTROL_DO_NOT_DISTURB_MODE:kotlin.String` intent to indicate how long do not disturb mode should be enabled for.

 Value: "android.settings.extra.do_not_disturb_mode_minutes"

### EXTRA_EASY_CONNECT_ATTEMPTED_SSID

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_EASY_CONNECT_ATTEMPTED_SSID: String
```

Activity Extra: The SSID that the Enrollee tried to connect to.

An extra returned on the result intent received when using the `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_PROCESS_WIFI_EASY_CONNECT_URI:kotlin.String` intent to launch the Easy Connect Operation. This extra contains the SSID of the Access Point that the remote Enrollee tried to connect to. This value is populated only by remote R2 devices, and only for the following error codes: `https://developer.android.com/reference/kotlin/android/net/wifi/EasyConnectStatusCallback.html#EASY_CONNECT_EVENT_FAILURE_CANNOT_FIND_NETWORK:kotlin.Int` `https://developer.android.com/reference/kotlin/android/net/wifi/EasyConnectStatusCallback.html#EASY_CONNECT_EVENT_FAILURE_ENROLLEE_AUTHENTICATION:kotlin.Int`. Therefore, always check if this extra is available using `https://developer.android.com/reference/kotlin/android/content/Intent.html#hasExtra(kotlin.String)`. If there is no error, i.e. if the operation returns `https://developer.android.com/reference/kotlin/android/app/Activity.html#RESULT_OK:kotlin.Int`, then this extra is not attached to the result intent.

Use the `https://developer.android.com/reference/kotlin/android/content/Intent.html#getStringExtra(kotlin.String)` to obtain the SSID.

 Value: "android.provider.extra.EASY_CONNECT_ATTEMPTED_SSID"

### EXTRA_EASY_CONNECT_BAND_LIST

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_EASY_CONNECT_BAND_LIST: String
```

Activity Extra: The Band List that the Enrollee supports.

This extra contains the bands the Enrollee supports, expressed as the Global Operating Class, see Table E-4 in IEEE Std 802.11-2016 Global operating classes. It is used both as input, to configure the Easy Connect operation and as output of the operation.

As input: an optional extra to be attached to the `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_PROCESS_WIFI_EASY_CONNECT_URI:kotlin.String`. If attached, it indicates the bands which the remote device (enrollee, device-to-be-configured) supports. The Settings operation may take this into account when presenting the user with list of networks configurations to be used. The calling app may obtain this information in any out-of-band method. The information should be attached as an array of raw integers - using the `https://developer.android.com/reference/kotlin/android/content/Intent.html#putExtra(kotlin.String,%20kotlin.IntArray)`.

As output: an extra returned on the result intent received when using the `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_PROCESS_WIFI_EASY_CONNECT_URI:kotlin.String` intent to launch the Easy Connect Operation . This value is populated only by remote R2 devices, and only for the following error codes: `https://developer.android.com/reference/kotlin/android/net/wifi/EasyConnectStatusCallback.html#EASY_CONNECT_EVENT_FAILURE_CANNOT_FIND_NETWORK:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/net/wifi/EasyConnectStatusCallback.html#EASY_CONNECT_EVENT_FAILURE_ENROLLEE_AUTHENTICATION:kotlin.Int`, or `https://developer.android.com/reference/kotlin/android/net/wifi/EasyConnectStatusCallback.html#EASY_CONNECT_EVENT_FAILURE_ENROLLEE_REJECTED_CONFIGURATION:kotlin.Int`. Therefore, always check if this extra is available using `https://developer.android.com/reference/kotlin/android/content/Intent.html#hasExtra(kotlin.String)`. If there is no error, i.e. if the operation returns `https://developer.android.com/reference/kotlin/android/app/Activity.html#RESULT_OK:kotlin.Int` , then this extra is not attached to the result intent.

Use the `https://developer.android.com/reference/kotlin/android/content/Intent.html#getIntArrayExtra(kotlin.String)` to obtain the list.

 Value: "android.provider.extra.EASY_CONNECT_BAND_LIST"

### EXTRA_EASY_CONNECT_CHANNEL_LIST

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_EASY_CONNECT_CHANNEL_LIST: String
```

Activity Extra: The Channel List that the Enrollee used to scan a network.

An extra returned on the result intent received when using the `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_PROCESS_WIFI_EASY_CONNECT_URI:kotlin.String` intent to launch the Easy Connect Operation. This extra contains the channel list that the Enrollee scanned for a network. This value is populated only by remote R2 devices, and only for the following error code: `https://developer.android.com/reference/kotlin/android/net/wifi/EasyConnectStatusCallback.html#EASY_CONNECT_EVENT_FAILURE_CANNOT_FIND_NETWORK:kotlin.Int`. Therefore, always check if this extra is available using `https://developer.android.com/reference/kotlin/android/content/Intent.html#hasExtra(kotlin.String)`. If there is no error, i.e. if the operation returns `https://developer.android.com/reference/kotlin/android/app/Activity.html#RESULT_OK:kotlin.Int`, then this extra is not attached to the result intent. The list is JSON formatted, as an array (Wi-Fi global operating classes) of arrays (Wi-Fi channels).

Use the `https://developer.android.com/reference/kotlin/android/content/Intent.html#getStringExtra(kotlin.String)` to obtain the list.

 Value: "android.provider.extra.EASY_CONNECT_CHANNEL_LIST"

### EXTRA_EASY_CONNECT_ERROR_CODE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_EASY_CONNECT_ERROR_CODE: String
```

Activity Extra: The Easy Connect operation error code

An extra returned on the result intent received when using the `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_PROCESS_WIFI_EASY_CONNECT_URI:kotlin.String` intent to launch the Easy Connect Operation. This extra contains the integer error code of the operation - one of `https://developer.android.com/reference/kotlin/android/net/wifi/EasyConnectStatusCallback.html#` `EASY_CONNECT_EVENT_FAILURE_*`. If there is no error, i.e. if the operation returns `https://developer.android.com/reference/kotlin/android/app/Activity.html#RESULT_OK:kotlin.Int`, then this extra is not attached to the result intent.

Use the `https://developer.android.com/reference/kotlin/android/content/Intent.html#hasExtra(kotlin.String)` to determine whether the extra is attached and `https://developer.android.com/reference/kotlin/android/content/Intent.html#getIntExtra(kotlin.String,%20kotlin.Int)` to obtain the error code data.

 Value: "android.provider.extra.EASY_CONNECT_ERROR_CODE"

### EXTRA_INPUT_METHOD_ID

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_INPUT_METHOD_ID: String
```

 Value: "input_method_id"

### EXTRA_NOTIFICATION_LISTENER_COMPONENT_NAME

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_NOTIFICATION_LISTENER_COMPONENT_NAME: String
```

Activity Extra: What component name to show the notification listener permission page for.

A string extra containing a `https://developer.android.com/reference/kotlin/android/content/ComponentName.html#`. This must be passed as an extra field to `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_NOTIFICATION_LISTENER_DETAIL_SETTINGS:kotlin.String`.

 Value: "android.provider.extra.NOTIFICATION_LISTENER_COMPONENT_NAME"

### EXTRA_SETTINGS_EMBEDDED_DEEP_LINK_HIGHLIGHT_MENU_KEY

Added in [API level 32](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_SETTINGS_EMBEDDED_DEEP_LINK_HIGHLIGHT_MENU_KEY: String
```

Activity Extra: Specify a key that indicates the menu item which should be highlighted on settings home menu.

This must be passed as an extra field to `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_SETTINGS_EMBED_DEEP_LINK_ACTIVITY:kotlin.String`.

 Value: "android.provider.extra.SETTINGS_EMBEDDED_DEEP_LINK_HIGHLIGHT_MENU_KEY"

### EXTRA_SETTINGS_EMBEDDED_DEEP_LINK_INTENT_URI

Added in [API level 32](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_SETTINGS_EMBEDDED_DEEP_LINK_INTENT_URI: String
```

Activity Extra: Specify the intent for the `https://developer.android.com/reference/kotlin/android/app/Activity.html#` which will be embedded in Settings app. It's an intent URI string from `intent.toUri(Intent.URI_INTENT_SCHEME)`.

This must be passed as an extra field to `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_SETTINGS_EMBED_DEEP_LINK_ACTIVITY:kotlin.String`.

 Value: "android.provider.extra.SETTINGS_EMBEDDED_DEEP_LINK_INTENT_URI"

### EXTRA_SUB_ID

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_SUB_ID: String
```

An int extra specifying a subscription ID.

 Value: "android.provider.extra.SUB_ID"

**See Also**

- `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionInfo.html#getSubscriptionId()`

### EXTRA_SUPERVISOR_RESTRICTED_SETTING_KEY

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_SUPERVISOR_RESTRICTED_SETTING_KEY: String
```

Intent extra: The id of a setting restricted by supervisors.

Type: Integer with a value from the one of the SUPERVISOR_VERIFICATION_\* constants below.

- `https://developer.android.com/reference/kotlin/android/provider/Settings#SUPERVISOR_VERIFICATION_SETTING_UNKNOWN:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/provider/Settings#SUPERVISOR_VERIFICATION_SETTING_BIOMETRICS:kotlin.Int`

<br />

 Value: "android.provider.extra.SUPERVISOR_RESTRICTED_SETTING_KEY"

### EXTRA_WIFI_NETWORK_LIST

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_WIFI_NETWORK_LIST: String
```

A bundle extra of `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_WIFI_ADD_NETWORKS:kotlin.String` intent action that indicates the list of the `https://developer.android.com/reference/kotlin/android/net/wifi/WifiNetworkSuggestion.html#` elements. The maximum count of the `https://developer.android.com/reference/kotlin/android/net/wifi/WifiNetworkSuggestion.html#` elements in the list will be five.

For example: To provide credentials for one open and one WPA2 networks:

```kotlin
<code>final WifiNetworkSuggestion suggestion1 =
        new WifiNetworkSuggestion.Builder()
        .setSsid("test111111")
        .build();
  final WifiNetworkSuggestion suggestion2 =
        new WifiNetworkSuggestion.Builder()
        .setSsid("test222222")
        .setWpa2Passphrase("test123456")
        .build();
  final List&lt;WifiNetworkSuggestion&gt; suggestionsList = new ArrayList&lt;&gt;;
  suggestionsList.add(suggestion1);
  suggestionsList.add(suggestion2);
  Bundle bundle = new Bundle();
  bundle.putParcelableArrayList(Settings.EXTRA_WIFI_NETWORK_LIST,(ArrayList&lt;? extends
  Parcelable&gt;) suggestionsList);
  final Intent intent = new Intent(Settings.ACTION_WIFI_ADD_NETWORKS);
  intent.putExtras(bundle);
  startActivityForResult(intent, 0);
  </code>
```

 Value: "android.provider.extra.WIFI_NETWORK_LIST"

### EXTRA_WIFI_NETWORK_RESULT_LIST

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_WIFI_NETWORK_RESULT_LIST: String
```

A bundle extra of the result of `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_WIFI_ADD_NETWORKS:kotlin.String` intent action that indicates the action result of the saved `https://developer.android.com/reference/kotlin/android/net/wifi/WifiNetworkSuggestion.html#`. Its value is a list of integers, and all the elements will be 1:1 mapping to the elements in `https://developer.android.com/reference/kotlin/android/provider/Settings#EXTRA_WIFI_NETWORK_LIST:kotlin.String`, if user press cancel to cancel the add networks request, then its value will be null.

Note: The integer value will be one of the `https://developer.android.com/reference/kotlin/android/provider/Settings#ADD_WIFI_RESULT_SUCCESS:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/provider/Settings#ADD_WIFI_RESULT_ADD_OR_UPDATE_FAILED:kotlin.Int`, or `https://developer.android.com/reference/kotlin/android/provider/Settings#ADD_WIFI_RESULT_ALREADY_EXISTS:kotlin.Int`}.

 Value: "android.provider.extra.WIFI_NETWORK_RESULT_LIST"

### INTENT_CATEGORY_USAGE_ACCESS_CONFIG

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val INTENT_CATEGORY_USAGE_ACCESS_CONFIG: String
```

Activity Category: Show application settings related to usage access.

An activity that provides a user interface for adjusting usage access related preferences for its containing application. Optional but recommended for apps that use `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#PACKAGE_USAGE_STATS:kotlin.String`.

The activity may define meta-data to describe what usage access is used for within their app with `https://developer.android.com/reference/kotlin/android/provider/Settings#METADATA_USAGE_ACCESS_REASON:kotlin.String`, which will be displayed in Settings.

Input: Nothing.

Output: Nothing.

 Value: "android.intent.category.USAGE_ACCESS_CONFIG"

### METADATA_USAGE_ACCESS_REASON

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val METADATA_USAGE_ACCESS_REASON: String
```

Metadata key: Reason for needing usage access.

A key for metadata attached to an activity that receives action `https://developer.android.com/reference/kotlin/android/provider/Settings#INTENT_CATEGORY_USAGE_ACCESS_CONFIG:kotlin.String`, shown to the user as description of how the app uses usage access.

<br />

 Value: "android.settings.metadata.USAGE_ACCESS_REASON"

### SUPERVISOR_VERIFICATION_SETTING_BIOMETRICS

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SUPERVISOR_VERIFICATION_SETTING_BIOMETRICS: Int
```

Settings for supervisors to control what kinds of biometric sensors, such a face and fingerprint scanners, can be used on the device.

 Value: 1

### SUPERVISOR_VERIFICATION_SETTING_UNKNOWN

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SUPERVISOR_VERIFICATION_SETTING_UNKNOWN: Int
```

The unknown setting can usually be ignored and is used for compatibility with future supervisor settings.

 Value: 0

## Public constructors

### Settings

```
Settings()
```

## Public methods

### canDrawOverlays

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun canDrawOverlays(context: Context!): Boolean
```

Checks if the specified context can draw on top of other apps. As of API level 23, an app cannot draw on top of other apps unless it declares the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#SYSTEM_ALERT_WINDOW:kotlin.String` permission in its manifest, *and* the user specifically grants the app this capability. To prompt the user to grant this approval, the app must send an intent with the action `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_MANAGE_OVERLAY_PERMISSION:kotlin.String`, which causes the system to display a permission management screen.

| Parameters ||
|---|---|
| `context` | [Context](../android/content/Context.md)!: App context. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the specified context can draw on top of other apps, false otherwise |
