Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# UserManager

```
open class UserManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.os.UserManager](https://developer.android.com/reference/kotlin/android/os/UserManager#) |

Manages users and user details on a multi-user system. There are two major categories of users: fully customizable users with their own login, and profiles that share a workspace with a related user.

Users are different from accounts, which are managed by `https://developer.android.com/reference/kotlin/android/accounts/AccountManager.html#`. Each user can have their own set of accounts.

See `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#ACTION_PROVISION_MANAGED_PROFILE:kotlin.String` for more on managed profiles.

## Summary

| Nested classes ||
|---|---|
| open | `https://developer.android.com/reference/kotlin/android/os/UserManager.UserOperationException` Thrown to indicate user operation failed. |

| Constants ||
|---|---|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/os/UserManager#ALLOW_PARENT_PROFILE_APP_LINKING:kotlin.String` Allows apps in the parent profile to handle web links from the managed profile. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_ADD_MANAGED_PROFILE:kotlin.String` Specifies if a user is disallowed from adding managed profiles. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_ADD_PRIVATE_PROFILE:kotlin.String` Specifies if a user is disallowed from creating a private profile. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_ADD_USER:kotlin.String` Specifies if a user is disallowed from adding new users. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_ADD_WIFI_CONFIG:kotlin.String` Specifies if a user is disallowed from adding a new Wi-Fi configuration. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_ADJUST_VOLUME:kotlin.String` Specifies if a user is disallowed from adjusting the global volume. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_AIRPLANE_MODE:kotlin.String` Specifies if airplane mode is disallowed on the device. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_AMBIENT_DISPLAY:kotlin.String` Specifies if ambient display is disallowed for the user. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_APPS_CONTROL:kotlin.String` Specifies if a user is disallowed from modifying applications in Settings or launchers. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_ASSIST_CONTENT:kotlin.String` This user restriction specifies if assist content is disallowed from being sent to a privileged app such as the Assistant app. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_AUTOFILL:kotlin.String` Specifies if a user is not allowed to use Autofill Services. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_BLUETOOTH:kotlin.String` Specifies if bluetooth is disallowed on the device. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_BLUETOOTH_SHARING:kotlin.String` Specifies if outgoing bluetooth sharing is disallowed. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_CAMERA_TOGGLE:kotlin.String` Specifies whether the camera toggle is available to the user. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_CELLULAR_2G:kotlin.String` Specifies if a user is not allowed to use 2g networks. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_CHANGE_NEAR_FIELD_COMMUNICATION_RADIO:kotlin.String` This user restriction specifies if Near-field communication is disallowed to change on the device. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_CHANGE_WIFI_STATE:kotlin.String` Specifies if a user is disallowed from enabling/disabling Wi-Fi. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_CONFIG_BLUETOOTH:kotlin.String` Specifies if a user is disallowed from configuring bluetooth via Settings. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_CONFIG_BRIGHTNESS:kotlin.String` Specifies if a user is disallowed from configuring brightness. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_CONFIG_CELL_BROADCASTS:kotlin.String` Specifies if a user is disallowed from configuring cell broadcasts. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_CONFIG_CREDENTIALS:kotlin.String` Specifies if a user is disallowed from configuring user credentials. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_CONFIG_DATE_TIME:kotlin.String` Specifies configuring date, time and timezone is disallowed via Settings. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_CONFIG_DEFAULT_APPS:kotlin.String` Specifies whether the user is allowed to modify default apps in settings. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_CONFIG_LOCALE:kotlin.String` Specifies if a user is disallowed from changing the device language. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_CONFIG_LOCATION:kotlin.String` Specifies if a user is disallowed from enabling or disabling location providers. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_CONFIG_MOBILE_NETWORKS:kotlin.String` Specifies if a user is disallowed from configuring mobile networks. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_CONFIG_PRIVATE_DNS:kotlin.String` Specifies whether the user is allowed to modify private DNS settings. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_CONFIG_SCREEN_TIMEOUT:kotlin.String` Specifies if a user is disallowed from changing screen off timeout. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_CONFIG_TETHERING:kotlin.String` Specifies if a user is disallowed from using and configuring Tethering and portable hotspots via Settings. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_CONFIG_VPN:kotlin.String` Specifies if a user is disallowed from configuring a VPN. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_CONFIG_WIFI:kotlin.String` Specifies if a user is disallowed from changing Wi-Fi access points via Settings. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_CONTENT_CAPTURE:kotlin.String` Specifies if the contents of a user's screen is not allowed to be captured for artificial intelligence purposes. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_CONTENT_SUGGESTIONS:kotlin.String` Specifies if the current user is able to receive content suggestions for selections based on the contents of their screen. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_CREATE_WINDOWS:kotlin.String` Specifies that windows besides app windows should not be created. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_CROSS_PROFILE_COPY_PASTE:kotlin.String` Specifies if the clipboard contents can be exported by pasting the data into other users or profiles. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_DATA_ROAMING:kotlin.String` Specifies if a user is not allowed to use cellular data when roaming. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_DEBUGGING_FEATURES:kotlin.String` Specifies if a user is disallowed from enabling or accessing debugging features. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_FACTORY_RESET:kotlin.String` Specifies if a user is disallowed from factory resetting from Settings. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_FUN:kotlin.String` Specifies if the user is not allowed to have fun. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_GRANT_ADMIN:kotlin.String` Restricts a user's ability to possess or grant admin privileges. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_INSTALL_APPS:kotlin.String` Specifies if a user is disallowed from installing applications. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_INSTALL_UNKNOWN_SOURCES:kotlin.String` Specifies if a user is disallowed from enabling the "Unknown Sources" setting, that allows installation of apps from unknown sources. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_INSTALL_UNKNOWN_SOURCES_GLOBALLY:kotlin.String` This restriction is a device-wide version of `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_INSTALL_UNKNOWN_SOURCES:kotlin.String`. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_INSTALL_UNKNOWN_SOURCES_INCLUDING_REGISTERED_APP_STORES:kotlin.String` User restriction to disallow installing apps from unknown sources, including registered app stores. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_MICROPHONE_TOGGLE:kotlin.String` Specifies whether the microphone toggle is available to the user. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_MODIFY_ACCOUNTS:kotlin.String` Specifies if a user is disallowed from adding and removing accounts, unless they are android. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_MOUNT_PHYSICAL_MEDIA:kotlin.String` Specifies if a user is disallowed from mounting physical external media. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_NEAR_FIELD_COMMUNICATION_RADIO:kotlin.String` This user restriction specifies if Near-field communication is disallowed on the device. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_NETWORK_RESET:kotlin.String` Specifies if a user is disallowed from resetting network settings from Settings. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_OUTGOING_BEAM:kotlin.String` Specifies if the user is not allowed to use NFC to beam out data from apps. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_OUTGOING_CALLS:kotlin.String` Specifies that the user is not allowed to make outgoing phone calls. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_PRINTING:kotlin.String` Specifies whether the user is allowed to print. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_REMOVE_MANAGED_PROFILE:kotlin.String` Specifies if managed profiles of this user can be removed, other than by its profile owner. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_REMOVE_USER:kotlin.String` When set on the admin user this specifies if the user can remove secondary users. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_SAFE_BOOT:kotlin.String` Specifies if the user is not allowed to reboot the device into safe boot mode. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_SET_USER_ICON:kotlin.String` Specifies if a user is not allowed to change their icon. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_SET_WALLPAPER:kotlin.String` User restriction to disallow setting a wallpaper. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_SHARE_INTO_MANAGED_PROFILE:kotlin.String` Specifies whether the user can share file / picture / data from the primary user into the managed profile, either by sending them from the primary side, or by picking up data within an app in the managed profile. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_SHARE_LOCATION:kotlin.String` Specifies if a user is disallowed from turning on location sharing. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_SHARING_ADMIN_CONFIGURED_WIFI:kotlin.String` Specifies if users are disallowed from sharing Wi-Fi for admin configured networks. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_SIM_GLOBALLY:kotlin.String` This user restriction specifies if the user is able to add embedded SIMs to the device. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_SMS:kotlin.String` Specifies that the user is not allowed to send or receive SMS messages. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_SYSTEM_ERROR_DIALOGS:kotlin.String` Specifies that system error dialogs for crashed or unresponsive apps should not be shown. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_TASK_CONTINUITY_HANDOFF:kotlin.String` Specifies if the user is not allowed to handoff tasks to other devices. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_THREAD_NETWORK:kotlin.String` This user restriction specifies if Thread network is disallowed on the device. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_ULTRA_WIDEBAND_RADIO:kotlin.String` This user restriction specifies if Ultra-wideband is disallowed on the device. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_UNIFIED_PASSWORD:kotlin.String` Specifies that the managed profile is not allowed to have unified lock screen challenge with the profile parent. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_UNINSTALL_APPS:kotlin.String` Specifies if a user is disallowed from uninstalling applications. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_UNMUTE_MICROPHONE:kotlin.String` Specifies if a user is disallowed from adjusting microphone volume. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_USB_FILE_TRANSFER:kotlin.String` Specifies if a user is disallowed from transferring files over USB. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_USER_SWITCH:kotlin.String` Specifies if user switching is blocked on the current user. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_WIFI_DIRECT:kotlin.String` Specifies if a user is disallowed from using Wi-Fi Direct. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_WIFI_TETHERING:kotlin.String` Specifies if a user is disallowed from using Wi-Fi tethering. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/os/UserManager#ENSURE_VERIFY_APPS:kotlin.String` Specifies if a user is disallowed from disabling application verification. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/os/UserManager#KEY_RESTRICTIONS_PENDING:kotlin.String` Application restriction key that is used to indicate the pending arrival of real restrictions for the app. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/UserManager#QUIET_MODE_DISABLE_ONLY_IF_CREDENTIAL_NOT_REQUIRED:kotlin.Int` Flag passed to #requestQuietModeEnabled to request disabling quiet mode only if there is no need to confirm the user credentials. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/UserManager#USER_CREATION_FAILED_NOT_PERMITTED:kotlin.Int` Error result indicating that this user is not allowed to add other users on this device. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/UserManager#USER_CREATION_FAILED_NO_MORE_USERS:kotlin.Int` Error result indicating that no more users can be created on this device. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/UserManager#USER_OPERATION_ERROR_CURRENT_USER:kotlin.Int` Indicates user operation failed because the target user is in the foreground. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/UserManager#USER_OPERATION_ERROR_LOW_STORAGE:kotlin.Int` Indicates user operation failed because device has low data storage. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/UserManager#USER_OPERATION_ERROR_MANAGED_PROFILE:kotlin.Int` Indicates user operation failed because target user is a managed profile. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/UserManager#USER_OPERATION_ERROR_MAX_RUNNING_USERS:kotlin.Int` Indicates user operation failed because maximum running user limit has been reached. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/UserManager#USER_OPERATION_ERROR_MAX_USERS:kotlin.Int` Indicates user operation failed because a relevant maximum user limit has been reached. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/UserManager#USER_OPERATION_ERROR_UNKNOWN:kotlin.Int` Indicates user operation failed for unknown reason. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/UserManager#USER_OPERATION_SUCCESS:kotlin.Int` Indicates user operation is successful. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/os/UserManager#USER_TYPE_PROFILE_CLONE:kotlin.String` User type representing a clone profile. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/os/UserManager#USER_TYPE_PROFILE_MANAGED:kotlin.String` User type representing a managed profile, which is a profile that is to be managed by a device policy controller (DPC). |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/os/UserManager#USER_TYPE_PROFILE_PRIVATE:kotlin.String` User type representing a private profile. |

| Public methods ||
|---|---|
| open static [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#)! | `https://developer.android.com/reference/kotlin/android/os/UserManager#createUserCreationIntent(kotlin.String,%20kotlin.String,%20kotlin.String,%20android.os.PersistableBundle)(userName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, accountName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, accountType: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, accountOptions: https://developer.android.com/reference/kotlin/android/os/PersistableBundle?)` Returns an intent to create a user for the provided name and account name. |
| open [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle)! | `https://developer.android.com/reference/kotlin/android/os/UserManager#getApplicationRestrictions(kotlin.String)(packageName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Returns a `https://developer.android.com/reference/kotlin/android/os/Bundle` containing any saved application restrictions for the context user, for the given package name. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/os/UserManager#getSerialNumberForUser(android.os.UserHandle)(user: https://developer.android.com/reference/kotlin/android/os/UserHandle!)` Return the serial number for a user. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/UserManager#getUserCount()()` Return the number of users currently created on the device. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/os/UserManager#getUserCreationTime(android.os.UserHandle)(userHandle: https://developer.android.com/reference/kotlin/android/os/UserHandle!)` Returns creation time of the given user. |
| open [UserHandle](https://developer.android.com/reference/kotlin/android/os/UserHandle)! | `https://developer.android.com/reference/kotlin/android/os/UserManager#getUserForSerialNumber(kotlin.Long)(serialNumber: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Return the user associated with a serial number previously returned by `https://developer.android.com/reference/kotlin/android/os/UserManager#getSerialNumberForUser(android.os.UserHandle)`. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/os/UserManager#getUserName()()` Returns the user name of the context user. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [UserHandle](https://developer.android.com/reference/kotlin/android/os/UserHandle)!\>! | `https://developer.android.com/reference/kotlin/android/os/UserManager#getUserProfiles()()` Returns a list of the users that are associated with the context user, including the user itself. |
| open [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle)! | `https://developer.android.com/reference/kotlin/android/os/UserManager#getUserRestrictions()()` Returns the user-wide restrictions imposed on the context user. |
| --- | --- |
| open [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle)! | `https://developer.android.com/reference/kotlin/android/os/UserManager#getUserRestrictions(android.os.UserHandle)(userHandle: https://developer.android.com/reference/kotlin/android/os/UserHandle!)` Returns the user-wide restrictions imposed on the user specified by `userHandle`. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/os/UserManager#hasUserRestriction(kotlin.String)(restrictionKey: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Returns whether the context user has been disallowed from performing certain actions or setting certain settings. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/os/UserManager#isAdminUser()()` Used to check if the context user is an admin user. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/os/UserManager#isDemoUser()()` Checks if the context user is a demo user. |
| open static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/os/UserManager#isHeadlessSystemUserMode()()` Checks whether the device is running in a headless system user mode. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/os/UserManager#isManagedProfile()()` Checks if the context user is a managed profile. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/os/UserManager#isProfile()()` Checks if the context user is running in a profile. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/os/UserManager#isQuietModeEnabled(android.os.UserHandle)(userHandle: https://developer.android.com/reference/kotlin/android/os/UserHandle!)` Returns whether the given profile is in quiet mode or not. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/os/UserManager#isSystemUser()()` Used to check if the context user is the system user. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/os/UserManager#isUserAGoat()()` Used to determine whether the user making this call is subject to teleportations. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/os/UserManager#isUserForeground()()` Checks if the context user is running in the foreground. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/os/UserManager#isUserRunning(android.os.UserHandle)(user: https://developer.android.com/reference/kotlin/android/os/UserHandle!)` Return whether the given user is actively running. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/os/UserManager#isUserRunningOrStopping(android.os.UserHandle)(user: https://developer.android.com/reference/kotlin/android/os/UserHandle!)` Return whether the given user is actively running *or* stopping. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/os/UserManager#isUserUnlocked()()` Return whether the context user is running in an "unlocked" state. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/os/UserManager#isUserUnlocked(android.os.UserHandle)(user: https://developer.android.com/reference/kotlin/android/os/UserHandle!)` Return whether the given user is running in an "unlocked" state. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/os/UserManager#requestQuietModeEnabled(kotlin.Boolean,%20android.os.UserHandle)(enableQuietMode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html, userHandle: https://developer.android.com/reference/kotlin/android/os/UserHandle)` Enables or disables quiet mode for a profile. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/os/UserManager#requestQuietModeEnabled(kotlin.Boolean,%20android.os.UserHandle,%20kotlin.Int)(enableQuietMode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html, userHandle: https://developer.android.com/reference/kotlin/android/os/UserHandle, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Perform the same operation as `https://developer.android.com/reference/kotlin/android/os/UserManager#requestQuietModeEnabled(kotlin.Boolean,%20android.os.UserHandle)`, but with a flag to tweak the behavior of the request. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/os/UserManager#setRestrictionsChallenge(kotlin.String)(newPin: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Sets a new challenge PIN for restrictions. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/os/UserManager#setUserRestriction(kotlin.String,%20kotlin.Boolean)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Sets the value of a specific restriction on the context user. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/os/UserManager#setUserRestrictions(android.os.Bundle)(restrictions: https://developer.android.com/reference/kotlin/android/os/Bundle!)` This will no longer work. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/os/UserManager#setUserRestrictions(android.os.Bundle,%20android.os.UserHandle)(restrictions: https://developer.android.com/reference/kotlin/android/os/Bundle!, userHandle: https://developer.android.com/reference/kotlin/android/os/UserHandle!)` This will no longer work. |
| --- | --- |
| open static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/os/UserManager#supportsMultipleUsers()()` Returns whether this device supports multiple switchable users with their own login and customizable space. |

## Constants

### ALLOW_PARENT_PROFILE_APP_LINKING

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ALLOW_PARENT_PROFILE_APP_LINKING: String
```

Allows apps in the parent profile to handle web links from the managed profile. This user restriction has an effect only in a managed profile. If set: Intent filters of activities in the parent profile with action `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_VIEW:kotlin.String`, category `https://developer.android.com/reference/kotlin/android/content/Intent.html#CATEGORY_BROWSABLE:kotlin.String`, scheme http or https, and which define a host can handle intents from the managed profile.

Holders of the permission `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MANAGE_DEVICE_POLICY_PROFILES:kotlin.String` can set this restriction using the DevicePolicyManager APIs mentioned below.

The default value is `false`.

Key for user restrictions.

Type: Boolean

 Value: "allow_parent_profile_app_linking"

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#addUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#clearUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/os/UserManager#getUserRestrictions()`

### DISALLOW_ADD_MANAGED_PROFILE

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DISALLOW_ADD_MANAGED_PROFILE: String
```

**Deprecated:** *As the ability to have a managed profile on a fully-managed device has been removed from the platform, this restriction will be silently ignored when applied by the device owner.*

Specifies if a user is disallowed from adding managed profiles.

The default value for an unmanaged user is `false`. For users with a device owner set, the default is `true`.

This restriction has no effect on managed profiles.

Key for user restrictions.

Type: Boolean

 Value: "no_add_managed_profile"

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#addUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#clearUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/os/UserManager#getUserRestrictions()`

### DISALLOW_ADD_PRIVATE_PROFILE

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DISALLOW_ADD_PRIVATE_PROFILE: String
```

Specifies if a user is disallowed from creating a private profile.

The default value for an unmanaged user is `false`. For users with a device owner set, the default value is `true` and the device owner currently cannot change it to `false`. On organization-owned managed profile devices, the default value is `false` but the profile owner can change it to `true` via the parent profile to block creating of private profiles on the personal user.

Holders of the permission `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MANAGE_DEVICE_POLICY_PROFILES:kotlin.String` can set this restriction using the DevicePolicyManager APIs mentioned below.

Key for user restrictions.

Type: Boolean

 Value: "no_add_private_profile"

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#addUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#clearUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#getParentProfileInstance(android.content.ComponentName)`
- `https://developer.android.com/reference/kotlin/android/os/UserManager#getUserRestrictions()`

### DISALLOW_ADD_USER

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DISALLOW_ADD_USER: String
```

Specifies if a user is disallowed from adding new users. This can only be set by device owners or profile owners on the main user. The default value is `false`.

When the device is an organization-owned device, this restriction will be set as a base restriction which cannot be removed by any admin.

Holders of the permission `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MANAGE_DEVICE_POLICY_MODIFY_USERS:kotlin.String` can set this restriction using the DevicePolicyManager APIs mentioned below.

Key for user restrictions.

Type: Boolean

 Value: "no_add_user"

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#addUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#clearUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/os/UserManager#getUserRestrictions()`

### DISALLOW_ADD_WIFI_CONFIG

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DISALLOW_ADD_WIFI_CONFIG: String
```

Specifies if a user is disallowed from adding a new Wi-Fi configuration.

This restriction can only be set by a device owner, a profile owner of an organization-owned managed profile on the parent profile. When it is set by any of these owners, it prevents all users from adding a new Wi-Fi configuration. This does not limit the owner and carrier's ability to add a new configuration.

Holders of the permission `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MANAGE_DEVICE_POLICY_WIFI:kotlin.String` can set this restriction using the DevicePolicyManager APIs mentioned below.

The default value is `false`.

Key for user restrictions.

Type: Boolean

 Value: "no_add_wifi_config"

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#addUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#clearUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/os/UserManager#getUserRestrictions()`

### DISALLOW_ADJUST_VOLUME

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DISALLOW_ADJUST_VOLUME: String
```

Specifies if a user is disallowed from adjusting the global volume. If set, the global volume will be muted. This can be set by device owners from API 21 and profile owners from API 24. The default value is `false`.

When the restriction is set by profile owners, then it only applies to relevant profiles.

Holders of the permission `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MANAGE_DEVICE_POLICY_AUDIO_OUTPUT:kotlin.String` can set this restriction using the DevicePolicyManager APIs mentioned below.

This restriction has no effect on managed profiles.

Key for user restrictions.

Type: Boolean

 Value: "no_adjust_volume"

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#addUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#clearUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/os/UserManager#getUserRestrictions()`

### DISALLOW_AIRPLANE_MODE

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DISALLOW_AIRPLANE_MODE: String
```

Specifies if airplane mode is disallowed on the device.

This restriction can only be set by a device owner, a profile owner on the primary user or a profile owner of an organization-owned managed profile on the parent profile. When it is set by any of these owners, it applies globally - i.e., it disables airplane mode on the entire device.

Holders of the permission `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MANAGE_DEVICE_POLICY_AIRPLANE_MODE:kotlin.String` can set this restriction using the DevicePolicyManager APIs mentioned below.

The default value is `false`.

Key for user restrictions.

Type: Boolean

 Value: "no_airplane_mode"

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#addUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#clearUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/os/UserManager#getUserRestrictions()`

### DISALLOW_AMBIENT_DISPLAY

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DISALLOW_AMBIENT_DISPLAY: String
```

Specifies if ambient display is disallowed for the user.

The default value is `false`.

Holders of the permission `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MANAGE_DEVICE_POLICY_DISPLAY:kotlin.String` can set this restriction using the DevicePolicyManager APIs mentioned below.

This user restriction has no effect on managed profiles.

Key for user restrictions.

Type: Boolean

 Value: "no_ambient_display"

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#addUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#clearUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/os/UserManager#getUserRestrictions()`

### DISALLOW_APPS_CONTROL

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DISALLOW_APPS_CONTROL: String
```

Specifies if a user is disallowed from modifying applications in Settings or launchers. The following actions will not be allowed when this restriction is enabled:
- uninstalling apps
- disabling apps
- clearing app caches
- clearing app data
- force stopping apps
- clearing app defaults
- The default value is `false`.
- **Note:** The user will still be able to perform those actions via other means (such as adb). Third party apps will also be able to uninstall apps via the `https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller.html#`. `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_UNINSTALL_APPS:kotlin.String` or `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#setUninstallBlocked(android.content.ComponentName,%20kotlin.String,%20kotlin.Boolean)` should be used to prevent the user from uninstalling apps completely, and `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#addPersistentPreferredActivity(android.content.ComponentName,%20android.content.IntentFilter,%20android.content.ComponentName)` to add a default intent handler for a given intent filter.
- Holders of the permission `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MANAGE_DEVICE_POLICY_APPS_CONTROL:kotlin.String` can set this restriction using the DevicePolicyManager APIs mentioned below.
- Key for user restrictions.
- Type: Boolean

 Value: "no_control_apps"

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#addUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#clearUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/os/UserManager#getUserRestrictions()`

### DISALLOW_ASSIST_CONTENT

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DISALLOW_ASSIST_CONTENT: String
```

This user restriction specifies if assist content is disallowed from being sent to a privileged app such as the Assistant app. Assist content includes screenshots and information about an app, such as package name.

This restriction can only be set by a device owner or a profile owner. When it is set by a device owner, it disables the assist contextual data on the entire device. When it is set by a profile owner, it disables assist content on the profile.

Default is `false`.

Key for user restrictions.

Type: Boolean

 Value: "no_assist_content"

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#addUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#clearUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/os/UserManager#getUserRestrictions()`

### DISALLOW_AUTOFILL

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DISALLOW_AUTOFILL: String
```

Specifies if a user is not allowed to use Autofill Services.

Device owner and profile owner can set this restriction. When it is set by device owner, only the target user will be affected.

Holders of the permission `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MANAGE_DEVICE_POLICY_AUTOFILL:kotlin.String` can set this restriction using the DevicePolicyManager APIs mentioned below.

The default value is `false`.

 Value: "no_autofill"

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#addUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#clearUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/os/UserManager#getUserRestrictions()`

### DISALLOW_BLUETOOTH

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DISALLOW_BLUETOOTH: String
```

Specifies if bluetooth is disallowed on the device. If bluetooth is disallowed on the device, bluetooth cannot be turned on or configured via Settings.

This restriction can only be set by a device owner, a profile owner on the primary user or a profile owner of an organization-owned managed profile on the parent profile. When it is set by a device owner, it applies globally - i.e., it disables bluetooth on the entire device and all users will be affected. When it is set by a profile owner on the primary user or by a profile owner of an organization-owned managed profile on the parent profile, it disables the primary user from using bluetooth and configuring bluetooth in Settings.

Holders of the permission `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MANAGE_DEVICE_POLICY_BLUETOOTH:kotlin.String` can set this restriction using the DevicePolicyManager APIs mentioned below.

The default value is `false`.

Key for user restrictions.

Type: Boolean

 Value: "no_bluetooth"

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#addUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#clearUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/os/UserManager#getUserRestrictions()`

### DISALLOW_BLUETOOTH_SHARING

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DISALLOW_BLUETOOTH_SHARING: String
```

Specifies if outgoing bluetooth sharing is disallowed.

A device owner and a profile owner can set this restriction. When it is set by a device owner, it applies globally. When it is set by a profile owner on the primary user or by a profile owner of an organization-owned managed profile on the parent profile, it disables the primary user from any outgoing bluetooth sharing.

Holders of the permission `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MANAGE_DEVICE_POLICY_BLUETOOTH:kotlin.String` can set this restriction using the DevicePolicyManager APIs mentioned below.

Default is `true` for managed and private profiles, false otherwise.

When a device upgrades to `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES#O:kotlin.Int`, the system sets it for all existing managed profiles.

Key for user restrictions.

Type: Boolean

 Value: "no_bluetooth_sharing"

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#addUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#clearUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/os/UserManager#getUserRestrictions()`

### DISALLOW_CAMERA_TOGGLE

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DISALLOW_CAMERA_TOGGLE: String
```

Specifies whether the camera toggle is available to the user. If this restriction is set, the user will not be able to block camera access via the system toggle. If camera access is blocked when the restriction is added, it will be automatically re-enabled. This restriction can only be set by a device owner.

The default value is `false`.

 Value: "disallow_camera_toggle"

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/SensorPrivacyManager.html#`
- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#addUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#clearUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/os/UserManager#getUserRestrictions()`

### DISALLOW_CELLULAR_2G

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DISALLOW_CELLULAR_2G: String
```

Specifies if a user is not allowed to use 2g networks.

This is a security feature. 2g has no mutual authentication between a device and cellular base station and downgrading a device's connection to 2g is a common tactic for several types of privacy and security compromising attacks that could allow an adversary to intercept, inject, or modify cellular communications.

This restriction can only be set by a device owner or a profile owner of an organization-owned managed profile on the parent profile. In all cases, the setting applies globally on the device.

Cellular connectivity loss (where a device would have otherwise successfully connected to a 2g network) occurs if the device is in an area where only 2g networks are available. Emergency calls are an exception and are never impacted. The device will still scan for and connect to a 2g network for emergency calls.

Holders of the permission `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MANAGE_DEVICE_POLICY_MOBILE_NETWORK:kotlin.String` can set this restriction using the DevicePolicyManager APIs mentioned below.

The default value is `false`.

 Value: "no_cellular_2g"

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#addUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#clearUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/os/UserManager#getUserRestrictions()`

### DISALLOW_CHANGE_NEAR_FIELD_COMMUNICATION_RADIO

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DISALLOW_CHANGE_NEAR_FIELD_COMMUNICATION_RADIO: String
```

This user restriction specifies if Near-field communication is disallowed to change on the device. If Near-field communication is disallowed it cannot be changed via Settings.

This restriction can only be set by a device owner or a profile owner of an organization-owned managed profile on the parent profile. In both cases, the restriction applies globally on the device and will not allow Near-field communication state being changed.

Near-field communication (NFC) is a radio technology that allows two devices (like your phone and a payments terminal) to communicate with each other when they're close together.

Default is `false`.

Key for user restrictions.

Type: Boolean

 Value: "no_change_near_field_communication_radio"

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#addUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#clearUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/os/UserManager#getUserRestrictions()`

### DISALLOW_CHANGE_WIFI_STATE

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DISALLOW_CHANGE_WIFI_STATE: String
```

Specifies if a user is disallowed from enabling/disabling Wi-Fi.

This restriction can only be set by a device owner, a profile owner of an organization-owned managed profile on the parent profile. When it is set by any of these owners, it applies globally - i.e., it disables airplane mode from changing Wi-Fi state.

Holders of the permission `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MANAGE_DEVICE_POLICY_WIFI:kotlin.String` can set this restriction using the DevicePolicyManager APIs mentioned below.

The default value is `false`.

Key for user restrictions.

Type: Boolean

 Value: "no_change_wifi_state"

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#addUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#clearUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/os/UserManager#getUserRestrictions()`

### DISALLOW_CONFIG_BLUETOOTH

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DISALLOW_CONFIG_BLUETOOTH: String
```

Specifies if a user is disallowed from configuring bluetooth via Settings. This does *not* restrict the user from turning bluetooth on or off.

This restriction doesn't prevent the user from using bluetooth. For disallowing usage of bluetooth completely on the device, use `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_BLUETOOTH:kotlin.String`.

A device owner and a profile owner can set this restriction, although the restriction has no effect in a managed profile. When it is set by a device owner, a profile owner on the primary user or by a profile owner of an organization-owned managed profile on the parent profile, it disallows the primary user from configuring bluetooth.

Holders of the permission `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MANAGE_DEVICE_POLICY_BLUETOOTH:kotlin.String` can set this restriction using the DevicePolicyManager APIs mentioned below.

The default value is `false`.

Key for user restrictions.

Type: Boolean

 Value: "no_config_bluetooth"

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#addUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#clearUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/os/UserManager#getUserRestrictions()`

### DISALLOW_CONFIG_BRIGHTNESS

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DISALLOW_CONFIG_BRIGHTNESS: String
```

Specifies if a user is disallowed from configuring brightness. When device owner sets it, it'll only be applied on the target(system) user.

The default value is `false`.

Holders of the permission `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MANAGE_DEVICE_POLICY_DISPLAY:kotlin.String` can set this restriction using the DevicePolicyManager APIs mentioned below.

This user restriction has no effect on managed profiles.

Key for user restrictions.

Type: Boolean

 Value: "no_config_brightness"

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#addUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#clearUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/os/UserManager#getUserRestrictions()`

### DISALLOW_CONFIG_CELL_BROADCASTS

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DISALLOW_CONFIG_CELL_BROADCASTS: String
```

Specifies if a user is disallowed from configuring cell broadcasts.

This restriction can only be set by a device owner, a profile owner on the main user or a profile owner of an organization-owned managed profile on the parent profile. When it is set by a device owner, it applies globally. When it is set by a profile owner on the main user or by a profile owner of an organization-owned managed profile on the parent profile, it disables the user from configuring cell broadcasts.

Holders of the permission `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MANAGE_DEVICE_POLICY_MOBILE_NETWORK:kotlin.String` can set this restriction using the DevicePolicyManager APIs mentioned below.

The default value is `false`.

This restriction has no effect on non-Admin users since they cannot configure cell broadcasts.

Key for user restrictions.

Type: Boolean

 Value: "no_config_cell_broadcasts"

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#addUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#clearUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/os/UserManager#getUserRestrictions()`

### DISALLOW_CONFIG_CREDENTIALS

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DISALLOW_CONFIG_CREDENTIALS: String
```

Specifies if a user is disallowed from configuring user credentials. The default value is `false`.

Holders of the permission `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MANAGE_DEVICE_POLICY_LOCK_CREDENTIALS:kotlin.String` can set this restriction using the DevicePolicyManager APIs mentioned below.

Key for user restrictions.

Type: Boolean

 Value: "no_config_credentials"

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#addUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#clearUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/os/UserManager#getUserRestrictions()`

### DISALLOW_CONFIG_DATE_TIME

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DISALLOW_CONFIG_DATE_TIME: String
```

Specifies configuring date, time and timezone is disallowed via Settings.

A device owner and a profile owner can set this restriction, although the restriction has no effect in a managed profile. When it is set by a device owner or by a profile owner of an organization-owned managed profile on the parent profile, it applies globally - i.e., it disables date, time and timezone setting on the entire device and all users are affected. When it is set by a profile owner on the primary user, it disables the primary user from configuring date, time and timezone and disables all configuring of date, time and timezone in Settings.

Holders of the permission `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MANAGE_DEVICE_POLICY_TIME:kotlin.String` can set this restriction using the DevicePolicyManager APIs mentioned below.

The default value is `false`.

Key for user restrictions.

Type: Boolean

 Value: "no_config_date_time"

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#addUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#clearUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/os/UserManager#getUserRestrictions()`

### DISALLOW_CONFIG_DEFAULT_APPS

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DISALLOW_CONFIG_DEFAULT_APPS: String
```

Specifies whether the user is allowed to modify default apps in settings.

A device owner and a profile owner can set this restriction. When it is set by a device owner, it applies globally - i.e., modifying of default apps in Settings for all users is disallowed. When it is set by a profile owner on the primary user or by a profile owner of an organization-owned managed profile on the parent profile, modifying of default apps in Settings for the primary user is disallowed.

The default value is `false`.

Key for user restrictions.

Type: Boolean

 Value: "disallow_config_default_apps"

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#addUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#clearUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/os/UserManager#getUserRestrictions()`

### DISALLOW_CONFIG_LOCALE

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DISALLOW_CONFIG_LOCALE: String
```

Specifies if a user is disallowed from changing the device language. The default value is `false`.

Holders of the permission `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MANAGE_DEVICE_POLICY_LOCALE:kotlin.String` can set this restriction using the DevicePolicyManager APIs mentioned below.

Key for user restrictions.

Type: Boolean

 Value: "no_config_locale"

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#addUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#clearUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/os/UserManager#getUserRestrictions()`

### DISALLOW_CONFIG_LOCATION

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DISALLOW_CONFIG_LOCATION: String
```

Specifies if a user is disallowed from enabling or disabling location providers. As a result, user is disallowed from turning on or off location via Settings.

A device owner and a profile owner can set this restriction. When it is set by a device owner, a profile owner on the primary user or by a profile owner of an organization-owned managed profile on the parent profile, it disallows the primary user from turning location on or off.

Holders of the permission `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MANAGE_DEVICE_POLICY_LOCATION:kotlin.String` can set this restriction using the DevicePolicyManager APIs mentioned below.

The default value is `false`.

This user restriction is different from `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_SHARE_LOCATION:kotlin.String`, as a device owner or a profile owner can still enable or disable location mode via `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#setLocationEnabled(android.content.ComponentName,%20kotlin.Boolean)` when this restriction is on.

Key for user restrictions.

Type: Boolean

 Value: "no_config_location"

**See Also**

- `https://developer.android.com/reference/kotlin/android/location/LocationManager.html#isLocationEnabled()`
- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#addUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#clearUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/os/UserManager#getUserRestrictions()`

### DISALLOW_CONFIG_MOBILE_NETWORKS

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DISALLOW_CONFIG_MOBILE_NETWORKS: String
```

Specifies if a user is disallowed from configuring mobile networks.

This restriction can only be set by a device owner, a profile owner on the main user or a profile owner of an organization-owned managed profile on the parent profile. When it is set by a device owner, it applies globally. When it is set by a profile owner on the main user or by a profile owner of an organization-owned managed profile on the parent profile, it disables the user from configuring mobile networks.

Holders of the permission `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MANAGE_DEVICE_POLICY_MOBILE_NETWORK:kotlin.String` can set this restriction using the DevicePolicyManager APIs mentioned below.

The default value is `false`.

This restriction has no effect on non-Admin users since they cannot configure mobile networks.

Key for user restrictions.

Type: Boolean

 Value: "no_config_mobile_networks"

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#addUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#clearUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/os/UserManager#getUserRestrictions()`

### DISALLOW_CONFIG_PRIVATE_DNS

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DISALLOW_CONFIG_PRIVATE_DNS: String
```

Specifies whether the user is allowed to modify private DNS settings.

This restriction can only be set by a device owner or a profile owner of an organization-owned managed profile on the parent profile. When it is set by either of these owners, it applies globally.

Holders of the permission `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MANAGE_DEVICE_POLICY_RESTRICT_PRIVATE_DNS:kotlin.String` can set this restriction using the DevicePolicyManager APIs mentioned below.

The default value is `false`.

Key for user restrictions.

Type: Boolean

 Value: "disallow_config_private_dns"

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#addUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#clearUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/os/UserManager#getUserRestrictions()`

### DISALLOW_CONFIG_SCREEN_TIMEOUT

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DISALLOW_CONFIG_SCREEN_TIMEOUT: String
```

Specifies if a user is disallowed from changing screen off timeout.

The default value is `false`.

Holders of the permission `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MANAGE_DEVICE_POLICY_DISPLAY:kotlin.String` can set this restriction using the DevicePolicyManager APIs mentioned below.

This user restriction has no effect on managed profiles.

Key for user restrictions.

Type: Boolean

 Value: "no_config_screen_timeout"

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#addUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#clearUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/os/UserManager#getUserRestrictions()`

### DISALLOW_CONFIG_TETHERING

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DISALLOW_CONFIG_TETHERING: String
```

Specifies if a user is disallowed from using and configuring Tethering and portable hotspots via Settings.

This restriction can only be set by a device owner, a profile owner on the primary user or a profile owner of an organization-owned managed profile on the parent profile. When it is set by a device owner, it applies globally. When it is set by a profile owner on the primary user or by a profile owner of an organization-owned managed profile on the parent profile, it disables the primary user from using Tethering and hotspots and disables all configuring of Tethering and hotspots in Settings.

Holders of the permission `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MANAGE_DEVICE_POLICY_MOBILE_NETWORK:kotlin.String` can set this restriction using the DevicePolicyManager APIs mentioned below.

The default value is `false`.

In Android 9.0 or higher, if tethering is enabled when this restriction is set, tethering will be automatically turned off.

Key for user restrictions.

Type: Boolean

 Value: "no_config_tethering"

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#addUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#clearUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/os/UserManager#getUserRestrictions()`

### DISALLOW_CONFIG_VPN

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DISALLOW_CONFIG_VPN: String
```

Specifies if a user is disallowed from configuring a VPN. The default value is `false `. This restriction has an effect when set by device owners and, in Android 6.0 ([API level 23](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES#M:kotlin.Int)) or higher, profile owners.

This restriction also prevents VPNs from starting. However, in Android 7.0 ([API level 24](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES#N:kotlin.Int)) or higher, the system does start always-on VPNs created by the device or profile owner.

From Android 12 ([API level 31](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES#S:kotlin.Int)) enforcing this restriction clears currently active VPN if it was configured by the user.

Holders of the permission `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MANAGE_DEVICE_POLICY_VPN:kotlin.String` can set this restriction using the DevicePolicyManager APIs mentioned below.

Key for user restrictions.

Type: Boolean

 Value: "no_config_vpn"

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#addUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#clearUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/os/UserManager#getUserRestrictions()`

### DISALLOW_CONFIG_WIFI

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DISALLOW_CONFIG_WIFI: String
```

Specifies if a user is disallowed from changing Wi-Fi access points via Settings. This restriction does not affect Wi-Fi tethering settings.

A device owner and a profile owner can set this restriction, although the restriction has no effect in a managed profile. When it is set by a device owner, a profile owner on the primary user or by a profile owner of an organization-owned managed profile on the parent profile, it disallows the primary user from changing Wi-Fi access points.

Holders of the permission `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MANAGE_DEVICE_POLICY_WIFI:kotlin.String` can set this restriction using the DevicePolicyManager APIs mentioned below.

The default value is `false`.

Key for user restrictions.

Type: Boolean

 Value: "no_config_wifi"

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#addUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#clearUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/os/UserManager#getUserRestrictions()`

### DISALLOW_CONTENT_CAPTURE

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DISALLOW_CONTENT_CAPTURE: String
```

Specifies if the contents of a user's screen is not allowed to be captured for artificial intelligence purposes.

A device owner and a profile owner can set this restriction. When it is set by a device owner, a profile owner on the primary user or by a profile owner of an organization-owned managed profile on the parent profile, it disables the primary user's screen from being captured for artificial intelligence purposes.

Holders of the permission `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MANAGE_DEVICE_POLICY_SCREEN_CONTENT:kotlin.String` can set this restriction using the DevicePolicyManager APIs mentioned below.

The default value is `false`.

 Value: "no_content_capture"

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#addUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#clearUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/os/UserManager#getUserRestrictions()`

### DISALLOW_CONTENT_SUGGESTIONS

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DISALLOW_CONTENT_SUGGESTIONS: String
```

Specifies if the current user is able to receive content suggestions for selections based on the contents of their screen.

A device owner and a profile owner can set this restriction. When it is set by a device owner, a profile owner on the primary user or by a profile owner of an organization-owned managed profile on the parent profile, it disables the primary user from receiving content suggestions for selections based on the contents of their screen.

Holders of the permission `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MANAGE_DEVICE_POLICY_SCREEN_CONTENT:kotlin.String` can set this restriction using the DevicePolicyManager APIs mentioned below.

The default value is `false`.

 Value: "no_content_suggestions"

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#addUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#clearUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/os/UserManager#getUserRestrictions()`

### DISALLOW_CREATE_WINDOWS

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DISALLOW_CREATE_WINDOWS: String
```

Specifies that windows besides app windows should not be created. This will block the creation of the following types of windows.
- `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#TYPE_TOAST:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#TYPE_APPLICATION_OVERLAY:kotlin.Int`
- This can only be set by device owners and profile owners on the primary user. The default value is `false`.
- Holders of the permission `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MANAGE_DEVICE_POLICY_WINDOWS:kotlin.String` can set this restriction using the DevicePolicyManager APIs mentioned below.
- Key for user restrictions.
- Type: Boolean

 Value: "no_create_windows"

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#addUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#clearUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/os/UserManager#getUserRestrictions()`

### DISALLOW_CROSS_PROFILE_COPY_PASTE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DISALLOW_CROSS_PROFILE_COPY_PASTE: String
```

Specifies if the clipboard contents can be exported by pasting the data into other users or profiles. This restriction doesn't prevent import, such as someone pasting clipboard data from other profiles or users. The default value is `false`.

**Note** : Because it's possible to extract data from screenshots using optical character recognition (OCR), we strongly recommend combining this user restriction with `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#setScreenCaptureDisabled(android.content.ComponentName,%20kotlin.Boolean)`.

Holders of the permission `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MANAGE_DEVICE_POLICY_PROFILE_INTERACTION:kotlin.String` can set this restriction using the DevicePolicyManager APIs mentioned below.

Key for user restrictions.

Type: Boolean

 Value: "no_cross_profile_copy_paste"

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#addUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#clearUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/os/UserManager#getUserRestrictions()`

### DISALLOW_DATA_ROAMING

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DISALLOW_DATA_ROAMING: String
```

Specifies if a user is not allowed to use cellular data when roaming.

This restriction can only be set by a device owner, a profile owner on the primary user or a profile owner of an organization-owned managed profile on the parent profile. When it is set by a device owner, it applies globally. When it is set by a profile owner on the primary user or by a profile owner of an organization-owned managed profile on the parent profile, it disables the primary user from using cellular data when roaming.

Holders of the permission `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MANAGE_DEVICE_POLICY_MOBILE_NETWORK:kotlin.String` can set this restriction using the DevicePolicyManager APIs mentioned below.

The default value is `false`.

 Value: "no_data_roaming"

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#addUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#clearUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/os/UserManager#getUserRestrictions()`

### DISALLOW_DEBUGGING_FEATURES

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DISALLOW_DEBUGGING_FEATURES: String
```

Specifies if a user is disallowed from enabling or accessing debugging features.

A device owner and a profile owner can set this restriction. When it is set by a device owner, a profile owner on the primary user or by a profile owner of an organization-owned managed profile on the parent profile, it disables debugging features altogether, including USB debugging. When set on a managed profile or a secondary user, it blocks debugging for that user only, including starting activities, making service calls, accessing content providers, sending broadcasts, installing/uninstalling packages, clearing user data, etc.

Holders of the permission `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MANAGE_DEVICE_POLICY_DEBUGGING_FEATURES:kotlin.String` can set this restriction using the DevicePolicyManager APIs mentioned below.

Default is `true` for newly created work profile on or after the 2025-04 security patch level. Otherwise, the default is `false`.

Key for user restrictions.

Type: Boolean

 Value: "no_debugging_features"

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#addUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#clearUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/os/UserManager#getUserRestrictions()`

### DISALLOW_FACTORY_RESET

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DISALLOW_FACTORY_RESET: String
```

Specifies if a user is disallowed from factory resetting from Settings. This can only be set by device owners and profile owners on an admin user. The default value is `false`.

This restriction has no effect on non-admin users since they cannot factory reset the device.

Holders of the permission `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MANAGE_DEVICE_POLICY_FACTORY_RESET:kotlin.String` can set this restriction using the DevicePolicyManager APIs mentioned below.

Key for user restrictions.

Type: Boolean

 Value: "no_factory_reset"

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#addUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#clearUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/os/UserManager#getUserRestrictions()`

### DISALLOW_FUN

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DISALLOW_FUN: String
```

Specifies if the user is not allowed to have fun. In some cases, the device owner may wish to prevent the user from experiencing amusement or joy while using the device. The default value is `false`.

Holders of the permission `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MANAGE_DEVICE_POLICY_FUN:kotlin.String` can set this restriction using the DevicePolicyManager APIs mentioned below.

Key for user restrictions.

Type: Boolean

 Value: "no_fun"

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#addUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#clearUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/os/UserManager#getUserRestrictions()`

### DISALLOW_GRANT_ADMIN

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DISALLOW_GRANT_ADMIN: String
```

Restricts a user's ability to possess or grant admin privileges.

When set to `true`, this prevents the user from:

- Becoming an admin
- Giving other users admin privileges

This restriction is only effective in environments where multiple admins are allowed.

Key for user restrictions. Type: Boolean. Default: `false`.

 Value: "no_grant_admin"

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#addUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#clearUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/os/UserManager#getUserRestrictions()`

### DISALLOW_INSTALL_APPS

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DISALLOW_INSTALL_APPS: String
```

Specifies if a user is disallowed from installing applications. This user restriction also prevents device owners and profile owners installing apps. The default value is `false`.

Holders of the permission `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MANAGE_DEVICE_POLICY_APPS_CONTROL:kotlin.String` can set this restriction using the DevicePolicyManager APIs mentioned below.

Key for user restrictions.

Type: Boolean

 Value: "no_install_apps"

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#addUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#clearUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/os/UserManager#getUserRestrictions()`

### DISALLOW_INSTALL_UNKNOWN_SOURCES

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DISALLOW_INSTALL_UNKNOWN_SOURCES: String
```

Specifies if a user is disallowed from enabling the "Unknown Sources" setting, that allows installation of apps from unknown sources. Unknown sources exclude adb and special apps such as trusted app stores. The default value is `false`.

Holders of the permission `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MANAGE_DEVICE_POLICY_INSTALL_UNKNOWN_SOURCES:kotlin.String` can set this restriction using the DevicePolicyManager APIs mentioned below.

Note: This restriction does not apply to installations initiated or performed by registered app stores or the installation of registered app stores themselves. To also restrict installations of registered app stores and from registered app stores, use `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_INSTALL_UNKNOWN_SOURCES_INCLUDING_REGISTERED_APP_STORES:kotlin.String`.

Key for user restrictions.

Type: Boolean

 Value: "no_install_unknown_sources"

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#addUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#clearUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/os/UserManager#getUserRestrictions()`

### DISALLOW_INSTALL_UNKNOWN_SOURCES_GLOBALLY

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DISALLOW_INSTALL_UNKNOWN_SOURCES_GLOBALLY: String
```

This restriction is a device-wide version of `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_INSTALL_UNKNOWN_SOURCES:kotlin.String`. Specifies if all users on the device are disallowed from enabling the "Unknown Sources" setting, that allows installation of apps from unknown sources. This restriction can be enabled by the profile owner, in which case all accounts and profiles will be affected.

Holders of the permission `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MANAGE_DEVICE_POLICY_INSTALL_UNKNOWN_SOURCES:kotlin.String` can set this restriction using the DevicePolicyManager APIs mentioned below.

Note: This restriction does not apply to installations initiated or performed by registered app stores or the installation of registered app stores themselves. To also restrict installations of registered app stores and from registered app stores, use `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_INSTALL_UNKNOWN_SOURCES_INCLUDING_REGISTERED_APP_STORES:kotlin.String`. The default value is `false`.

Key for user restrictions.

Type: Boolean

 Value: "no_install_unknown_sources_globally"

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#addUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#clearUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/os/UserManager#getUserRestrictions()`

### DISALLOW_INSTALL_UNKNOWN_SOURCES_INCLUDING_REGISTERED_APP_STORES

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DISALLOW_INSTALL_UNKNOWN_SOURCES_INCLUDING_REGISTERED_APP_STORES: String
```

User restriction to disallow installing apps from unknown sources, including registered app stores.

When this restriction is set, the user cannot install apps from any source other than privileged installers that are explicitly allowed as trusted sources. This supersedes `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_INSTALL_UNKNOWN_SOURCES:kotlin.String` by also blocking installations initiated by or from registered app stores (holders of `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#INSTALL_PACKAGES_AS_REGISTERED_APP_STORE:kotlin.String`), and installations of registered app stores themselves.

Key for user restrictions.

Type: Boolean

 Value: "no_install_unknown_sources_including_registered_app_stores"

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#addUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#clearUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/os/UserManager#getUserRestrictions()`

### DISALLOW_MICROPHONE_TOGGLE

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DISALLOW_MICROPHONE_TOGGLE: String
```

Specifies whether the microphone toggle is available to the user. If this restriction is set, the user will not be able to block microphone access via the system toggle. If microphone access is blocked when the restriction is added, it will be automatically re-enabled. This restriction can only be set by a device owner.

The default value is `false`.

 Value: "disallow_microphone_toggle"

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/SensorPrivacyManager.html#`
- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#addUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#clearUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/os/UserManager#getUserRestrictions()`

### DISALLOW_MODIFY_ACCOUNTS

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DISALLOW_MODIFY_ACCOUNTS: String
```

Specifies if a user is disallowed from adding and removing accounts, unless they are android.accounts.AccountManager#addAccountExplicitly added by Authenticator. The default value is `false`.

From `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES#N:kotlin.Int` a profile or device owner app can still use `https://developer.android.com/reference/kotlin/android/accounts/AccountManager.html#` APIs to add or remove accounts when account management is disallowed.

Holders of the permission `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MANAGE_DEVICE_POLICY_ACCOUNT_MANAGEMENT:kotlin.String` can set this restriction using the DevicePolicyManager APIs mentioned below.

Key for user restrictions.

Type: Boolean

 Value: "no_modify_accounts"

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#addUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#clearUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/os/UserManager#getUserRestrictions()`

### DISALLOW_MOUNT_PHYSICAL_MEDIA

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DISALLOW_MOUNT_PHYSICAL_MEDIA: String
```

Specifies if a user is disallowed from mounting physical external media.

This restriction can only be set by a device owner, a profile owner on the primary user or a profile owner of an organization-owned managed profile on the parent profile. When it is set by a device owner, it applies globally. When it is set by a profile owner on the primary user or by a profile owner of an organization-owned managed profile on the parent profile, it disables the primary user from mounting physical external media.

Holders of the permission `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MANAGE_DEVICE_POLICY_PHYSICAL_MEDIA:kotlin.String` can set this restriction using the DevicePolicyManager APIs mentioned below.

The default value is `false`.

Key for user restrictions.

Type: Boolean

 Value: "no_physical_media"

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#addUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#clearUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/os/UserManager#getUserRestrictions()`

### DISALLOW_NEAR_FIELD_COMMUNICATION_RADIO

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DISALLOW_NEAR_FIELD_COMMUNICATION_RADIO: String
```

This user restriction specifies if Near-field communication is disallowed on the device. If Near-field communication is disallowed it cannot be turned on via Settings.

This restriction can only be set by a device owner or a profile owner of an organization-owned managed profile on the parent profile. In both cases, the restriction applies globally on the device and will turn off the Near-field communication radio if it's currently on and prevent the radio from being turned on in the future.

Near-field communication (NFC) is a radio technology that allows two devices (like your phone and a payments terminal) to communicate with each other when they're close together.

Default is `false`.

Key for user restrictions.

Type: Boolean

 Value: "no_near_field_communication_radio"

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#addUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#clearUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/os/UserManager#getUserRestrictions()`

### DISALLOW_NETWORK_RESET

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DISALLOW_NETWORK_RESET: String
```

Specifies if a user is disallowed from resetting network settings from Settings. This can only be set by device owners and profile owners on the main user. The default value is `false`.

This restriction has no effect on non-Admin users since they cannot reset the network settings of the device.

Holders of the permission `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MANAGE_DEVICE_POLICY_MOBILE_NETWORK:kotlin.String` can set this restriction using the DevicePolicyManager APIs mentioned below.

Key for user restrictions.

Type: Boolean

 Value: "no_network_reset"

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#addUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#clearUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/os/UserManager#getUserRestrictions()`

### DISALLOW_OUTGOING_BEAM

Added in [API level 22](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DISALLOW_OUTGOING_BEAM: String
```

Specifies if the user is not allowed to use NFC to beam out data from apps. The default value is `false`.

Holders of the permission `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MANAGE_DEVICE_POLICY_NEARBY_COMMUNICATION:kotlin.String` can set this restriction using the DevicePolicyManager APIs mentioned below.

Key for user restrictions.

Type: Boolean

 Value: "no_outgoing_beam"

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#addUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#clearUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/os/UserManager#getUserRestrictions()`

### DISALLOW_OUTGOING_CALLS

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DISALLOW_OUTGOING_CALLS: String
```

Specifies that the user is not allowed to make outgoing phone calls. Emergency calls are still permitted.

A device owner and a profile owner can set this restriction, although the restriction has no effect in a managed profile. When it is set by a device owner, a profile owner on the primary user or by a profile owner of an organization-owned managed profile on the parent profile, it disallows the primary user from making outgoing phone calls.

Holders of the permission `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MANAGE_DEVICE_POLICY_CALLS:kotlin.String` can set this restriction using the DevicePolicyManager APIs mentioned below.

The default value is `false`.

Key for user restrictions.

Type: Boolean

 Value: "no_outgoing_calls"

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#addUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#clearUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/os/UserManager#getUserRestrictions()`

### DISALLOW_PRINTING

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DISALLOW_PRINTING: String
```

Specifies whether the user is allowed to print. This restriction can be set by device or profile owner.

Holders of the permission `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MANAGE_DEVICE_POLICY_PRINTING:kotlin.String` can set this restriction using the DevicePolicyManager APIs mentioned below. The default value is `false`.

 Value: "no_printing"

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#addUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#clearUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/os/UserManager#getUserRestrictions()`

### DISALLOW_REMOVE_MANAGED_PROFILE

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DISALLOW_REMOVE_MANAGED_PROFILE: String
```

**Deprecated:** *As the ability to have a managed profile on a fully-managed device has been removed from the platform, this restriction will be silently ignored when applied by the device owner. When the device is provisioned with a managed profile on an organization-owned device, the managed profile could not be removed anyway.*

Specifies if managed profiles of this user can be removed, other than by its profile owner. The default value is `false`.

This restriction has no effect on managed profiles, and this restriction does not block the removal of private profiles of this user.

Key for user restrictions.

Type: Boolean

 Value: "no_remove_managed_profile"

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#addUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#clearUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/os/UserManager#getUserRestrictions()`

### DISALLOW_REMOVE_USER

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DISALLOW_REMOVE_USER: String
```

When set on the admin user this specifies if the user can remove secondary users. Managed profiles and private profiles can still be removed even if this is set on the admin user. When set on a non-admin secondary user, this specifies if the user can remove itself. This restriction has no effect when set on managed profiles. The default value is `false`.

Holders of the permission `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MANAGE_DEVICE_POLICY_MODIFY_USERS:kotlin.String` can set this restriction using the DevicePolicyManager APIs mentioned below.

Key for user restrictions.

Type: Boolean

 Value: "no_remove_user"

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#addUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#clearUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/os/UserManager#getUserRestrictions()`

### DISALLOW_SAFE_BOOT

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DISALLOW_SAFE_BOOT: String
```

Specifies if the user is not allowed to reboot the device into safe boot mode.

This restriction can only be set by a device owner, a profile owner on the primary user or a profile owner of an organization-owned managed profile on the parent profile. When it is set by a device owner, it applies globally. When it is set by a profile owner on the primary user or by a profile owner of an organization-owned managed profile on the parent profile, it disables the primary user from rebooting the device into safe boot mode.

Holders of the permission `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MANAGE_DEVICE_POLICY_SAFE_BOOT:kotlin.String` can set this restriction using the DevicePolicyManager APIs mentioned below.

The default value is `false`.

Key for user restrictions.

Type: Boolean

 Value: "no_safe_boot"

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#addUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#clearUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/os/UserManager#getUserRestrictions()`

### DISALLOW_SET_USER_ICON

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DISALLOW_SET_USER_ICON: String
```

Specifies if a user is not allowed to change their icon. Device owner and profile owner can set this restriction. When it is set by device owner, only the target user will be affected. The default value is `false`.

Holders of the permission `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MANAGE_DEVICE_POLICY_MODIFY_USERS:kotlin.String` can set this restriction using the DevicePolicyManager APIs mentioned below.

Key for user restrictions.

Type: Boolean

 Value: "no_set_user_icon"

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#addUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#clearUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/os/UserManager#getUserRestrictions()`

### DISALLOW_SET_WALLPAPER

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DISALLOW_SET_WALLPAPER: String
```

User restriction to disallow setting a wallpaper. Profile owner and device owner are able to set wallpaper regardless of this restriction. The default value is `false`.

Holders of the permission `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MANAGE_DEVICE_POLICY_WALLPAPER:kotlin.String` can set this restriction using the DevicePolicyManager APIs mentioned below.

Key for user restrictions.

Type: Boolean

 Value: "no_set_wallpaper"

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#addUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#clearUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/os/UserManager#getUserRestrictions()`

### DISALLOW_SHARE_INTO_MANAGED_PROFILE

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DISALLOW_SHARE_INTO_MANAGED_PROFILE: String
```

Specifies whether the user can share file / picture / data from the primary user into the managed profile, either by sending them from the primary side, or by picking up data within an app in the managed profile.

When a managed profile is created, the system allows the user to send data from the primary side to the profile by setting up certain default cross profile intent filters. If this is undesired, this restriction can be set to disallow it. Note that this restriction will not block any sharing allowed by explicit `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#addCrossProfileIntentFilter(android.content.ComponentName,%20android.content.IntentFilter,%20kotlin.Int)` calls by the profile owner.

This restriction is only meaningful when set by profile owner. When it is set by device owner, it does not have any effect.

Holders of the permission `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MANAGE_DEVICE_POLICY_PROFILE_INTERACTION:kotlin.String` can set this restriction using the DevicePolicyManager APIs mentioned below.

The default value is `false`.

 Value: "no_sharing_into_profile"

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#addUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#clearUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/os/UserManager#getUserRestrictions()`

### DISALLOW_SHARE_LOCATION

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DISALLOW_SHARE_LOCATION: String
```

Specifies if a user is disallowed from turning on location sharing.

In a managed profile, location sharing by default reflects the primary user's setting, but can be overridden and forced off by setting this restriction to true in the managed profile.

A device owner and a profile owner can set this restriction. When it is set by a device owner, a profile owner on the primary user or by a profile owner of an organization-owned managed profile on the parent profile, it prevents the primary user from turning on location sharing.

Holders of the permission `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MANAGE_DEVICE_POLICY_LOCATION:kotlin.String` can set this restriction using the DevicePolicyManager APIs mentioned below.

The default value is `false`.

Key for user restrictions.

Type: Boolean

 Value: "no_share_location"

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#addUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#clearUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/os/UserManager#getUserRestrictions()`

### DISALLOW_SHARING_ADMIN_CONFIGURED_WIFI

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DISALLOW_SHARING_ADMIN_CONFIGURED_WIFI: String
```

Specifies if users are disallowed from sharing Wi-Fi for admin configured networks.

Device owner and profile owner can set this restriction. When it is set by any of these owners, it prevents all users from sharing Wi-Fi for networks configured by these owners. Other networks not configured by these owners are not affected.

Holders of the permission `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MANAGE_DEVICE_POLICY_WIFI:kotlin.String` can set this restriction using the DevicePolicyManager APIs mentioned below.

The default value is `false`.

Key for user restrictions.

Type: Boolean

 Value: "no_sharing_admin_configured_wifi"

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#addUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#clearUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/os/UserManager#getUserRestrictions()`

### DISALLOW_SIM_GLOBALLY

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DISALLOW_SIM_GLOBALLY: String
```

This user restriction specifies if the user is able to add embedded SIMs to the device.

This restriction blocks the download of embedded SIMs.

This restriction can only be set by a device owner or a profile owner of an organization-owned managed profile. In both cases, the restriction applies globally on the device.

Holders of the permission `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MANAGE_DEVICE_POLICY_MOBILE_NETWORK:kotlin.String` can set this restriction using the DevicePolicyManager APIs mentioned below.

Default is `false`.

Key for user restrictions.

Type: Boolean

 Value: "no_sim_globally"

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#addUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#clearUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/os/UserManager#getUserRestrictions()`

### DISALLOW_SMS

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DISALLOW_SMS: String
```

Specifies that the user is not allowed to send or receive SMS messages.

This restriction can only be set by a device owner, a profile owner on the primary user or a profile owner of an organization-owned managed profile on the parent profile. When it is set by a device owner, it applies globally. When it is set by a profile owner on the primary user or by a profile owner of an organization-owned managed profile on the parent profile, it disables the primary user from sending or receiving SMS messages.

Holders of the permission `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MANAGE_DEVICE_POLICY_SMS:kotlin.String` can set this restriction using the DevicePolicyManager APIs mentioned below.

The default value is `false`.

Key for user restrictions.

Type: Boolean

 Value: "no_sms"

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#addUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#clearUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/os/UserManager#getUserRestrictions()`

### DISALLOW_SYSTEM_ERROR_DIALOGS

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DISALLOW_SYSTEM_ERROR_DIALOGS: String
```

Specifies that system error dialogs for crashed or unresponsive apps should not be shown. In this case, the system will force-stop the app as if the user chooses the "close app" option on the UI. A feedback report isn't collected as there is no way for the user to provide explicit consent. The default value is `false`.

When this user restriction is set by device owners, it's applied to all users. When set by the profile owner of the primary user or a secondary user, the restriction affects only the calling user. This user restriction has no effect on managed profiles.

Holders of the permission `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MANAGE_DEVICE_POLICY_SYSTEM_DIALOGS:kotlin.String` can set this restriction using the DevicePolicyManager APIs mentioned below.

Key for user restrictions.

Type: Boolean

 Value: "no_system_error_dialogs"

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#addUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#clearUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/os/UserManager#getUserRestrictions()`

### DISALLOW_TASK_CONTINUITY_HANDOFF

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DISALLOW_TASK_CONTINUITY_HANDOFF: String
```

Specifies if the user is not allowed to handoff tasks to other devices.

This policy may be set by a device owner or a profile owner. When set by a device owner, no applications will be able to send data to other devices for Handoff, nor will the current device exchange task metadata for other devices. When it is set by a profile owner of an organization-owned managed profile or the parent profile, applications running in the personal user will be disallowed from performing Handoff and excluded from appearing in Handoff metadata exchanges

The default value is `false`.

Key for user restrictions.

Type: Boolean

 Value: "no_task_continuity_handoff"

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#addUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#clearUserRestriction(android.content.ComponentName,%20kotlin.String)`

### DISALLOW_THREAD_NETWORK

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DISALLOW_THREAD_NETWORK: String
```

This user restriction specifies if Thread network is disallowed on the device. If Thread network is disallowed it cannot be turned on via Settings.

This restriction can only be set by a device owner or a profile owner of an organization-owned managed profile on the parent profile. In both cases, the restriction applies globally on the device and will turn off the Thread network radio if it's currently on and prevent the radio from being turned on in the future.

[Thread](https://www.threadgroup.org) is a low-power and low-latency wireless mesh networking protocol built on IPv6.

Default is `false`.

Key for user restrictions.

Type: Boolean

 Value: "no_thread_network"

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#addUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#clearUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/os/UserManager#getUserRestrictions()`

### DISALLOW_ULTRA_WIDEBAND_RADIO

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DISALLOW_ULTRA_WIDEBAND_RADIO: String
```

This user restriction specifies if Ultra-wideband is disallowed on the device. If Ultra-wideband is disallowed it cannot be turned on via Settings.

Ultra-wideband (UWB) is a radio technology that can use a very low energy level for short-range, high-bandwidth communications over a large portion of the radio spectrum.

This restriction can only be set by a device owner or a profile owner of an organization-owned managed profile on the parent profile. In both cases, the restriction applies globally on the device and will turn off the ultra-wideband radio if it's currently on and prevent the radio from being turned on in the future.

Holders of the permission `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MANAGE_DEVICE_POLICY_NEARBY_COMMUNICATION:kotlin.String` can set this restriction using the DevicePolicyManager APIs mentioned below.

Default is `false`.

Key for user restrictions.

Type: Boolean

 Value: "no_ultra_wideband_radio"

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#addUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#clearUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/os/UserManager#getUserRestrictions()`

### DISALLOW_UNIFIED_PASSWORD

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DISALLOW_UNIFIED_PASSWORD: String
```

Specifies that the managed profile is not allowed to have unified lock screen challenge with the profile parent.

To ensure that there is a separate work profile password, IT admins have to:

1. Enforce `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_UNIFIED_PASSWORD:kotlin.String`
2. Verify that `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#isUsingUnifiedPassword(android.content.ComponentName)` returns false. This indicates that there is now a separate work profile password configured and the set up is completed.
3. In case `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#isUsingUnifiedPassword(android.content.ComponentName)` returns true, invoke `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#ACTION_SET_NEW_PASSWORD:kotlin.String` intent and then verify again `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#isUsingUnifiedPassword(android.content.ComponentName)`.

<br />

Can be set by profile owners. It only has effect on managed profiles when set by managed profile owner. Has no effect on non-managed profiles or users.

Holders of the permission `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MANAGE_DEVICE_POLICY_LOCK_CREDENTIALS:kotlin.String` can set this restriction using the `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#` APIs mentioned below.

Key for user restrictions.

Type: Boolean

 Value: "no_unified_password"

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#addUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#clearUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/os/UserManager#getUserRestrictions()`

### DISALLOW_UNINSTALL_APPS

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DISALLOW_UNINSTALL_APPS: String
```

Specifies if a user is disallowed from uninstalling applications. The default value is `false`.

Holders of the permission `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MANAGE_DEVICE_POLICY_APPS_CONTROL:kotlin.String` can set this restriction using the DevicePolicyManager APIs mentioned below.

Key for user restrictions.

Type: Boolean

 Value: "no_uninstall_apps"

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#addUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#clearUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/os/UserManager#getUserRestrictions()`

### DISALLOW_UNMUTE_MICROPHONE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DISALLOW_UNMUTE_MICROPHONE: String
```

Specifies if a user is disallowed from adjusting microphone volume. If set, the microphone will be muted.

A device owner and a profile owner can set this restriction, although the restriction has no effect in a managed profile. When it is set by a device owner, it applies globally. When it is set by a profile owner on the primary user or by a profile owner of an organization-owned managed profile on the parent profile, it will disallow the primary user from adjusting the microphone volume.

Holders of the permission `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MANAGE_DEVICE_POLICY_MICROPHONE:kotlin.String` can set this restriction using the DevicePolicyManager APIs mentioned below.

The default value is `false`.

Key for user restrictions.

Type: Boolean

 Value: "no_unmute_microphone"

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#addUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#clearUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/os/UserManager#getUserRestrictions()`

### DISALLOW_USB_FILE_TRANSFER

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DISALLOW_USB_FILE_TRANSFER: String
```

Specifies if a user is disallowed from transferring files over USB.

This restriction can only be set by a [device owner](https://developers.google.com/android/work/terminology#device_owner_do) or a [profile owner](https://developers.google.com/android/work/terminology#profile_owner_po) on the primary user's profile or a profile owner of an organization-owned [managed profile](https://developers.google.com/android/work/terminology#managed_profile) on the parent profile. When it is set by a device owner, it applies globally. When it is set by a profile owner on the primary user or by a profile owner of an organization-owned managed profile on the parent profile, it disables the primary user from transferring files over USB. No other user on the device is able to use file transfer over USB because the UI for file transfer is always associated with the primary user.

Holders of the permission `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MANAGE_DEVICE_POLICY_USB_FILE_TRANSFER:kotlin.String` can set this restriction using the DevicePolicyManager APIs mentioned below.

The default value is `false`.

Key for user restrictions.

Type: Boolean

 Value: "no_usb_file_transfer"

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#addUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#clearUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/os/UserManager#getUserRestrictions()`

### DISALLOW_USER_SWITCH

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DISALLOW_USER_SWITCH: String
```

Specifies if user switching is blocked on the current user.

This restriction can only be set by the device owner, it will be applied to all users. Device owner can still switch user via `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#switchUser(android.content.ComponentName,%20android.os.UserHandle)` when this restriction is set.

Holders of the permission `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MANAGE_DEVICE_POLICY_MODIFY_USERS:kotlin.String` can set this restriction using the DevicePolicyManager APIs mentioned below.

The default value is `false`.

 Value: "no_user_switch"

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#addUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#clearUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/os/UserManager#getUserRestrictions()`

### DISALLOW_WIFI_DIRECT

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DISALLOW_WIFI_DIRECT: String
```

Specifies if a user is disallowed from using Wi-Fi Direct.

This restriction can only be set by a device owner, a profile owner of an organization-owned managed profile on the parent profile. When it is set by any of these owners, it prevents all users from using Wi-Fi Direct.

Holders of the permission `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MANAGE_DEVICE_POLICY_WIFI:kotlin.String` can set this restriction using the DevicePolicyManager APIs mentioned below.

The default value is `false`.

Key for user restrictions.

Type: Boolean

 Value: "no_wifi_direct"

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#addUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#clearUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/os/UserManager#getUserRestrictions()`

### DISALLOW_WIFI_TETHERING

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DISALLOW_WIFI_TETHERING: String
```

Specifies if a user is disallowed from using Wi-Fi tethering.

This restriction does not limit the user's ability to modify or connect to regular Wi-Fi networks, which is separately controlled by `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_CONFIG_WIFI:kotlin.String`.

This restriction can only be set by a device owner, a profile owner of an organization-owned managed profile on the parent profile. When it is set by any of these owners, it prevents all users from using Wi-Fi tethering. Other forms of tethering are not affected.

Holders of the permission `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MANAGE_DEVICE_POLICY_WIFI:kotlin.String` can set this restriction using the DevicePolicyManager APIs mentioned below. This user restriction disables only Wi-Fi tethering. Use `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_CONFIG_TETHERING:kotlin.String` to limit all forms of tethering. When `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_CONFIG_TETHERING:kotlin.String` is set, this user restriction becomes obsolete.

The default value is `false`.

Key for user restrictions.

Type: Boolean

 Value: "no_wifi_tethering"

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#addUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#clearUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/os/UserManager#getUserRestrictions()`

### ENSURE_VERIFY_APPS

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ENSURE_VERIFY_APPS: String
```

Specifies if a user is disallowed from disabling application verification. The default value is `false`.

In Android 8.0 ([API level 26](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES#O:kotlin.Int)) and higher, this is a global user restriction. If a device owner or profile owner sets this restriction, the system enforces app verification across all users on the device. Running in earlier Android versions, this restriction affects only the profile that sets it.

Holders of the permission `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MANAGE_DEVICE_POLICY_INSTALL_UNKNOWN_SOURCES:kotlin.String` can set this restriction using the DevicePolicyManager APIs mentioned below.

Key for user restrictions.

Type: Boolean

 Value: "ensure_verify_apps"

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#addUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#clearUserRestriction(android.content.ComponentName,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/os/UserManager#getUserRestrictions()`

### KEY_RESTRICTIONS_PENDING

Added in [API level 22](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_RESTRICTIONS_PENDING: String
```

Application restriction key that is used to indicate the pending arrival of real restrictions for the app.

Applications that support restrictions should check for the presence of this key. A `true` value indicates that restrictions may be applied in the near future but are not available yet. It is the responsibility of any management application that sets this flag to update it when the final restrictions are enforced.

Key for application restrictions.

Type: Boolean

 Value: "restrictions_pending"

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#setApplicationRestrictions(android.content.ComponentName,%20kotlin.String,%20android.os.Bundle)`
- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#getApplicationRestrictions(android.content.ComponentName,%20kotlin.String)`

### QUIET_MODE_DISABLE_ONLY_IF_CREDENTIAL_NOT_REQUIRED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val QUIET_MODE_DISABLE_ONLY_IF_CREDENTIAL_NOT_REQUIRED: Int
```

Flag passed to #requestQuietModeEnabled to request disabling quiet mode only if there is no need to confirm the user credentials. If credentials are required to disable quiet mode, #requestQuietModeEnabled will do nothing and return `false`.

 Value: 1

### USER_CREATION_FAILED_NOT_PERMITTED

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val USER_CREATION_FAILED_NOT_PERMITTED: Int
```

Error result indicating that this user is not allowed to add other users on this device. This is a result code returned from the activity created by the intent `https://developer.android.com/reference/kotlin/android/os/UserManager#createUserCreationIntent(kotlin.String,%20kotlin.String,%20kotlin.String,%20android.os.PersistableBundle)`.

 Value: 1

### USER_CREATION_FAILED_NO_MORE_USERS

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val USER_CREATION_FAILED_NO_MORE_USERS: Int
```

Error result indicating that no more users can be created on this device. This is a result code returned from the activity created by the intent `https://developer.android.com/reference/kotlin/android/os/UserManager#createUserCreationIntent(kotlin.String,%20kotlin.String,%20kotlin.String,%20android.os.PersistableBundle)`.

 Value: 2

### USER_OPERATION_ERROR_CURRENT_USER

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val USER_OPERATION_ERROR_CURRENT_USER: Int
```

Indicates user operation failed because the target user is in the foreground.

 Value: 4

### USER_OPERATION_ERROR_LOW_STORAGE

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val USER_OPERATION_ERROR_LOW_STORAGE: Int
```

Indicates user operation failed because device has low data storage.

 Value: 5

### USER_OPERATION_ERROR_MANAGED_PROFILE

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val USER_OPERATION_ERROR_MANAGED_PROFILE: Int
```

Indicates user operation failed because target user is a managed profile.

 Value: 2

### USER_OPERATION_ERROR_MAX_RUNNING_USERS

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val USER_OPERATION_ERROR_MAX_RUNNING_USERS: Int
```

Indicates user operation failed because maximum running user limit has been reached.

 Value: 3

### USER_OPERATION_ERROR_MAX_USERS

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val USER_OPERATION_ERROR_MAX_USERS: Int
```

Indicates user operation failed because a relevant maximum user limit has been reached.

This could include the situation in which limit is 0, such as if a particular type of user is not enabled or is ineligible to be added to the requested parent.

 Value: 6

### USER_OPERATION_ERROR_UNKNOWN

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val USER_OPERATION_ERROR_UNKNOWN: Int
```

Indicates user operation failed for unknown reason.

 Value: 1

### USER_OPERATION_SUCCESS

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val USER_OPERATION_SUCCESS: Int
```

Indicates user operation is successful.

 Value: 0

### USER_TYPE_PROFILE_CLONE

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val USER_TYPE_PROFILE_CLONE: String
```

User type representing a clone profile. Clone profile is a user profile type used to run a second instance of an otherwise single user App (eg, messengers). Currently only the main user (which is the first full user set up on the device, usually the system user) can have a clone profile.

 Value: "android.os.usertype.profile.CLONE"

### USER_TYPE_PROFILE_MANAGED

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val USER_TYPE_PROFILE_MANAGED: String
```

User type representing a managed profile, which is a profile that is to be managed by a device policy controller (DPC). The intended purpose is for work profiles, which are managed by a corporate entity.

 Value: "android.os.usertype.profile.MANAGED"

### USER_TYPE_PROFILE_PRIVATE

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val USER_TYPE_PROFILE_PRIVATE: String
```

User type representing a private profile. Private profile is a user profile that can be used as an alternative user-space to install and use sensitive apps. UI surfaces can adopt an alternative strategy to show apps belonging to this profile, in line with their sensitive nature.

 Value: "android.os.usertype.profile.PRIVATE"

## Public methods

### createUserCreationIntent

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun createUserCreationIntent(
    userName: String?, 
    accountName: String?, 
    accountType: String?, 
    accountOptions: PersistableBundle?
): Intent!
```

Returns an intent to create a user for the provided name and account name. The name and account name will be used when the setup process for the new user is started.

The intent should be launched using startActivityForResult and the return result will indicate if the user consented to adding a new user and if the operation succeeded. Any errors in creating the user will be returned in the result code. If the user cancels the request, the return result will be `https://developer.android.com/reference/kotlin/android/app/Activity.html#RESULT_CANCELED:kotlin.Int`. On success, the result code will be `https://developer.android.com/reference/kotlin/android/app/Activity.html#RESULT_OK:kotlin.Int`.

Use `https://developer.android.com/reference/kotlin/android/os/UserManager#supportsMultipleUsers()` to first check if the device supports this operation at all.

The new user is created but not initialized. After switching into the user for the first time, the preferred user name and account information are used by the setup process for that user. This API should only be called if the current user is an `https://developer.android.com/reference/kotlin/android/os/UserManager#isAdminUser()` user, as otherwise the returned intent will not be able to create a user.

| Parameters ||
|---|---|
| `userName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: Optional name to assign to the user. Character limit is 100. This value may be `null`. |
| `accountName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: Optional account name that will be used by the setup wizard to initialize the user. Character limit is 500. This value may be `null`. |
| `accountType` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: Optional account type for the account to be created. This is required if the account name is specified. Character limit is 500. This value may be `null`. |
| --- | --- |
| `accountOptions` | [PersistableBundle](https://developer.android.com/reference/kotlin/android/os/PersistableBundle)?: Optional bundle of data to be passed in during account creation in the new user via `https://developer.android.com/reference/kotlin/android/accounts/AccountManager.html#addAccount(kotlin.String,%20kotlin.String,%20kotlin.Array,%20android.os.Bundle,%20android.app.Activity,%20android.accounts.AccountManagerCallback,%20android.os.Handler)`. Character limit is 1000. This value may be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/Intent.html#!` | An Intent that can be launched from an Activity. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/os/UserManager#USER_CREATION_FAILED_NOT_PERMITTED:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/os/UserManager#USER_CREATION_FAILED_NO_MORE_USERS:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/os/UserManager#supportsMultipleUsers()`

### getApplicationRestrictions

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getApplicationRestrictions(packageName: String!): Bundle!
```

Returns a `https://developer.android.com/reference/kotlin/android/os/Bundle` containing any saved application restrictions for the context user, for the given package name. Only an application with this package name can call this method.

The returned `https://developer.android.com/reference/kotlin/android/os/Bundle` consists of key-value pairs, as defined by the application, where the types of values may be:

- `boolean`
- `int`
- `String` or `String[]`
- From `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES#M:kotlin.Int`, `Bundle` or `Bundle[]`

NOTE: The method performs disk I/O and shouldn't be called on the main thread

Starting from Android version `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES#UPSIDE_DOWN_CAKE:kotlin.Int`, it is possible for there to be multiple managing apps on the device with the ability to set app restrictions, e.g. an Enterprise Device Policy Controller (DPC) and a Supervision admin. This method will always return the app restrictions set by the DPC, if the DPC has set one. Beginning from SDK level 36.1, if the DPC has not set any app restriction while other managing apps have set some, this method will return app restrictions set by one of those managing apps. There is no guarantee on which managing apps app restriction will be returned. To retrieve restrictions set by all managing apps, use `https://developer.android.com/reference/kotlin/android/content/RestrictionsManager.html#getApplicationRestrictionsPerAdmin()` instead. 
This method may take several seconds to complete, so it should only be called from a worker thread.

| Parameters ||
|---|---|
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the package name of the calling application |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/os/Bundle!` | a `https://developer.android.com/reference/kotlin/android/os/Bundle` with the restrictions for that package, or an empty `https://developer.android.com/reference/kotlin/android/os/Bundle` if there are no saved restrictions. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/os/UserManager#KEY_RESTRICTIONS_PENDING:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#getApplicationRestrictions(android.content.ComponentName,%20kotlin.String)`

### getSerialNumberForUser

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getSerialNumberForUser(user: UserHandle!): Long
```

Return the serial number for a user. This is a device-unique number assigned to that user; if the user is deleted and then a new user created, the new users will not be given the same serial number.

| Parameters ||
|---|---|
| `user` | [UserHandle](https://developer.android.com/reference/kotlin/android/os/UserHandle)!: The user whose serial number is to be retrieved. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | The serial number of the given user; returns -1 if the given UserHandle does not exist. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/os/UserManager#getUserForSerialNumber(kotlin.Long)`

### getUserCount

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getUserCount(): Int
```

Return the number of users currently created on the device. 
Requires android.Manifest.permission.MANAGE_USERS or android.Manifest.permission.CREATE_USERS

### getUserCreationTime

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getUserCreationTime(userHandle: UserHandle!): Long
```

Returns creation time of the given user. The given user must be the calling user or a profile associated with it.

| Parameters ||
|---|---|
| `userHandle` | [UserHandle](https://developer.android.com/reference/kotlin/android/os/UserHandle)!: user handle of the calling user or a profile associated with the calling user. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | creation time in milliseconds since Epoch time. |

### getUserForSerialNumber

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getUserForSerialNumber(serialNumber: Long): UserHandle!
```

Return the user associated with a serial number previously returned by `https://developer.android.com/reference/kotlin/android/os/UserManager#getSerialNumberForUser(android.os.UserHandle)`.

| Parameters ||
|---|---|
| `serialNumber` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): The serial number of the user that is being retrieved. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/os/UserHandle!` | Return the user associated with the serial number, or null if there is not one. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/os/UserManager#getSerialNumberForUser(android.os.UserHandle)`

### getUserName

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getUserName(): String
```

Returns the user name of the context user. This call is only available to applications on the system image. 
Requires android.Manifest.permission.MANAGE_USERS or android.Manifest.permission.CREATE_USERS or android.Manifest.permission.QUERY_USERS or `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#GET_ACCOUNTS_PRIVILEGED:kotlin.String`

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | the user name. This value cannot be `null`. |

### getUserProfiles

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getUserProfiles(): MutableList<UserHandle!>!
```

Returns a list of the users that are associated with the context user, including the user itself. This includes the user, its profiles, its parent, and its parent's other profiles, as applicable.

Note that this includes all profile types (not including Restricted profiles).

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/os/UserHandle!>!` | A non-empty list of UserHandles associated with the context user. |

### getUserRestrictions

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getUserRestrictions(): Bundle!
```

Returns the user-wide restrictions imposed on the context user.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/os/Bundle!` | a Bundle containing all the restrictions. |

### getUserRestrictions

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getUserRestrictions(userHandle: UserHandle!): Bundle!
```

Returns the user-wide restrictions imposed on the user specified by `userHandle`.

| Parameters ||
|---|---|
| `userHandle` | [UserHandle](https://developer.android.com/reference/kotlin/android/os/UserHandle)!: the UserHandle of the user for whom to retrieve the restrictions. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/os/Bundle!` | a Bundle containing all the restrictions. Requires `android.permission.MANAGE_USERS` or `android.permission.INTERACT_ACROSS_USERS`, otherwise specified `https://developer.android.com/reference/kotlin/android/os/UserHandle` must be the calling user or a profile associated with it. |

### hasUserRestriction

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun hasUserRestriction(restrictionKey: String!): Boolean
```

Returns whether the context user has been disallowed from performing certain actions or setting certain settings.

| Parameters ||
|---|---|
| `restrictionKey` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The string key representing the restriction. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/os/UserManager#ALLOW_PARENT_PROFILE_APP_LINKING:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_ADD_MANAGED_PROFILE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_ADD_PRIVATE_PROFILE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_ADD_USER:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_ADD_WIFI_CONFIG:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_ADJUST_VOLUME:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_AIRPLANE_MODE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_AMBIENT_DISPLAY:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_APPS_CONTROL:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_ASSIST_CONTENT:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_AUTOFILL:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_BLUETOOTH:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_BLUETOOTH_SHARING:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_CAMERA_TOGGLE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_CELLULAR_2G:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_CHANGE_NEAR_FIELD_COMMUNICATION_RADIO:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_CHANGE_WIFI_STATE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_CONFIG_BLUETOOTH:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_CONFIG_BRIGHTNESS:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_CONFIG_CELL_BROADCASTS:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_CONFIG_CREDENTIALS:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_CONFIG_DATE_TIME:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_CONFIG_DEFAULT_APPS:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_CONFIG_LOCALE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_CONFIG_LOCATION:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_CONFIG_MOBILE_NETWORKS:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_CONFIG_PRIVATE_DNS:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_CONFIG_SCREEN_TIMEOUT:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_CONFIG_TETHERING:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_CONFIG_VPN:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_CONFIG_WIFI:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_CONTENT_CAPTURE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_CONTENT_SUGGESTIONS:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_CREATE_WINDOWS:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_CROSS_PROFILE_COPY_PASTE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_DATA_ROAMING:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_DEBUGGING_FEATURES:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_FACTORY_RESET:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_FUN:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_GRANT_ADMIN:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_TASK_CONTINUITY_HANDOFF:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_INSTALL_APPS:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_INSTALL_UNKNOWN_SOURCES:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_INSTALL_UNKNOWN_SOURCES_GLOBALLY:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_INSTALL_UNKNOWN_SOURCES_INCLUDING_REGISTERED_APP_STORES:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_MICROPHONE_TOGGLE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_MODIFY_ACCOUNTS:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_MOUNT_PHYSICAL_MEDIA:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_NEAR_FIELD_COMMUNICATION_RADIO:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_NETWORK_RESET:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_OUTGOING_BEAM:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_OUTGOING_CALLS:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_PRINTING:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_REMOVE_MANAGED_PROFILE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_REMOVE_USER:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_SAFE_BOOT:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_SET_USER_ICON:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_SET_WALLPAPER:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_SHARE_INTO_MANAGED_PROFILE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_SHARE_LOCATION:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_SHARING_ADMIN_CONFIGURED_WIFI:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_SIM_GLOBALLY:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_SMS:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_SYSTEM_ERROR_DIALOGS:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_THREAD_NETWORK:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_ULTRA_WIDEBAND_RADIO:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_UNIFIED_PASSWORD:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_UNINSTALL_APPS:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_UNMUTE_MICROPHONE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_USB_FILE_TRANSFER:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_USER_SWITCH:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_WIFI_DIRECT:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager#DISALLOW_WIFI_TETHERING:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager#ENSURE_VERIFY_APPS:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager#KEY_RESTRICTIONS_PENDING:kotlin.String` |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the context user has the given restriction, `false` otherwise. |

### isAdminUser

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isAdminUser(): Boolean
```

Used to check if the context user is an admin user. An admin user may be allowed to modify or configure certain settings that aren't available to non-admin users, create and delete additional users, etc. There can be more than one admin users.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | whether the context user is an admin user. |

### isDemoUser

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isDemoUser(): Boolean
```

Checks if the context user is a demo user. When running in a demo user, apps can be more helpful to the user, or explain their features in more detail.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | whether the context user is a demo user. |

### isHeadlessSystemUserMode

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun isHeadlessSystemUserMode(): Boolean
```

Checks whether the device is running in a headless system user mode.

Headless system user mode means the `https://developer.android.com/reference/kotlin/android/os/UserManager#isSystemUser()` runs system services and some system UI, but it is not associated with any real person and additional users must be created to be associated with real persons.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | whether the device is running in a headless system user mode. |

### isManagedProfile

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isManagedProfile(): Boolean
```

Checks if the context user is a managed profile. Note that this applies specifically to *managed* profiles. For profiles in general, use `https://developer.android.com/reference/kotlin/android/os/UserManager#isProfile()` instead.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | whether the context user is a managed profile. |

### isProfile

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isProfile(): Boolean
```

Checks if the context user is running in a profile. A profile is a user that typically has its own separate data but shares its UI with some parent user. For example, a `https://developer.android.com/reference/kotlin/android/os/UserManager#isManagedProfile()` is a type of profile.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | whether the context user is in a profile. |

### isQuietModeEnabled

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isQuietModeEnabled(userHandle: UserHandle!): Boolean
```

Returns whether the given profile is in quiet mode or not.

| Parameters ||
|---|---|
| `userHandle` | [UserHandle](https://developer.android.com/reference/kotlin/android/os/UserHandle)!: The user handle of the profile to be queried. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the profile is in quiet mode, false otherwise. |

### isSystemUser

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isSystemUser(): Boolean
```

Used to check if the context user is the system user. The system user is the initial user that is implicitly created on first boot and hosts most of the system services.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | whether the context user is the system user. |

### isUserAGoat

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isUserAGoat(): Boolean
```

Used to determine whether the user making this call is subject to teleportations.

As of `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES#LOLLIPOP:kotlin.Int`, this method can now automatically identify goats using advanced goat recognition technology.

As of `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES#R:kotlin.Int`, this method always returns `false` in order to protect goat privacy.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Returns whether the user making this call is a goat. |

### isUserForeground

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isUserForeground(): Boolean
```

Checks if the context user is running in the foreground.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | whether the context user is running in the foreground. |

### isUserRunning

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isUserRunning(user: UserHandle!): Boolean
```

Return whether the given user is actively running. This means that the user is in the "started" state, not "stopped" -- it is currently allowed to run code through scheduled alarms, receiving broadcasts, etc. A started user may be either the current foreground user or a background user; the result here does not distinguish between the two.

Note prior to Android Nougat MR1 (SDK version \<= 24; `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES#N:kotlin.Int`, this API required a system permission in order to check other profile's status. Since Android Nougat MR1 (SDK version \>= 25; `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES#N_MR1:kotlin.Int`), the restriction has been relaxed, and now it'll accept any `https://developer.android.com/reference/kotlin/android/os/UserHandle` within the same profile group as the caller.

| Parameters ||
|---|---|
| `user` | [UserHandle](https://developer.android.com/reference/kotlin/android/os/UserHandle)!: The user to retrieve the running state for. |

### isUserRunningOrStopping

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isUserRunningOrStopping(user: UserHandle!): Boolean
```

Return whether the given user is actively running *or* stopping. This is like `https://developer.android.com/reference/kotlin/android/os/UserManager#isUserRunning(android.os.UserHandle)`, but will also return true if the user had been running but is in the process of being stopped (but is not yet fully stopped, and still running some code).

Note prior to Android Nougat MR1 (SDK version \<= 24; `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES#N:kotlin.Int`, this API required a system permission in order to check other profile's status. Since Android Nougat MR1 (SDK version \>= 25; `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES#N_MR1:kotlin.Int`), the restriction has been relaxed, and now it'll accept any `https://developer.android.com/reference/kotlin/android/os/UserHandle` within the same profile group as the caller.

| Parameters ||
|---|---|
| `user` | [UserHandle](https://developer.android.com/reference/kotlin/android/os/UserHandle)!: The user to retrieve the running state for. |

### isUserUnlocked

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isUserUnlocked(): Boolean
```

Return whether the context user is running in an "unlocked" state.

On devices with direct boot, a user is unlocked only after they've entered their credentials (such as a lock pattern or PIN). On devices without direct boot, a user is unlocked as soon as it starts.

When a user is locked, only device-protected data storage is available. When a user is unlocked, both device-protected and credential-protected private app data storage is available.
**See Also**

- `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_USER_UNLOCKED:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/content/Context.html#createDeviceProtectedStorageContext()`

### isUserUnlocked

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isUserUnlocked(user: UserHandle!): Boolean
```

Return whether the given user is running in an "unlocked" state.

On devices with direct boot, a user is unlocked only after they've entered their credentials (such as a lock pattern or PIN). On devices without direct boot, a user is unlocked as soon as it starts.

When a user is locked, only device-protected data storage is available. When a user is unlocked, both device-protected and credential-protected private app data storage is available.

Requires `android.permission.MANAGE_USERS` or `android.permission.INTERACT_ACROSS_USERS`, otherwise specified `https://developer.android.com/reference/kotlin/android/os/UserHandle` must be the calling user or a profile associated with it.

| Parameters ||
|---|---|
| `user` | [UserHandle](https://developer.android.com/reference/kotlin/android/os/UserHandle)!: to retrieve the unlocked state for. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_USER_UNLOCKED:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/content/Context.html#createDeviceProtectedStorageContext()`

### requestQuietModeEnabled

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun requestQuietModeEnabled(
    enableQuietMode: Boolean, 
    userHandle: UserHandle
): Boolean
```

Enables or disables quiet mode for a profile. If quiet mode is enabled, apps in the profile don't run, generate notifications, or consume data or battery.

If a user's credential is needed to turn off quiet mode, a confirm credential screen will be shown to the user.

The change may not happen instantly, however apps can listen for `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_MANAGED_PROFILE_AVAILABLE:kotlin.String` and `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_MANAGED_PROFILE_UNAVAILABLE:kotlin.String` broadcasts in order to be notified of the change of the quiet mode for managed profile. Apps can listen to generic broadcasts `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_PROFILE_AVAILABLE:kotlin.String` and `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_PROFILE_UNAVAILABLE:kotlin.String` to be notified of the change in quiet mode for any profiles. Apps can also check the current state of quiet mode by calling `https://developer.android.com/reference/kotlin/android/os/UserManager#isQuietModeEnabled(android.os.UserHandle)`.

The caller must either be the foreground default launcher or have one of these permissions: `MANAGE_USERS` or `MODIFY_QUIET_MODE`.

| Parameters ||
|---|---|
| `enableQuietMode` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): whether quiet mode should be enabled or disabled |
| `userHandle` | [UserHandle](https://developer.android.com/reference/kotlin/android/os/UserHandle): user handle of the profile. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `false` if user's credential is needed in order to turn off quiet mode, `true` otherwise |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if `userHandle` is not a profile |
| `java.lang.SecurityException` | if the caller is invalid |

**See Also**

- `https://developer.android.com/reference/kotlin/android/os/UserManager#isQuietModeEnabled(android.os.UserHandle)`

### requestQuietModeEnabled

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun requestQuietModeEnabled(
    enableQuietMode: Boolean, 
    userHandle: UserHandle, 
    flags: Int
): Boolean
```

Perform the same operation as `https://developer.android.com/reference/kotlin/android/os/UserManager#requestQuietModeEnabled(kotlin.Boolean,%20android.os.UserHandle)`, but with a flag to tweak the behavior of the request.

| Parameters ||
|---|---|
| `enableQuietMode` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): whether quiet mode should be enabled or disabled |
| `userHandle` | [UserHandle](https://developer.android.com/reference/kotlin/android/os/UserHandle): user handle of the profile. This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Can be 0 or `https://developer.android.com/reference/kotlin/android/os/UserManager#QUIET_MODE_DISABLE_ONLY_IF_CREDENTIAL_NOT_REQUIRED:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/UserManager#QUIET_MODE_DISABLE_ONLY_IF_CREDENTIAL_NOT_REQUIRED:kotlin.Int` |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `false` if user's credential is needed in order to turn off quiet mode, `true` otherwise |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if `userHandle` is not a managed profile |
| `java.lang.SecurityException` | if the caller is invalid |

**See Also**

- `https://developer.android.com/reference/kotlin/android/os/UserManager#isQuietModeEnabled(android.os.UserHandle)`

### setRestrictionsChallenge

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setRestrictionsChallenge(newPin: String!): Boolean
```

**Deprecated:** *The restrictions PIN functionality is no longer provided by the system. This method is preserved for backwards compatibility reasons and always returns false.*

Sets a new challenge PIN for restrictions. This is only for use by pre-installed apps and requires the MANAGE_USERS permission.

| Parameters ||
|---|---|
| `newPin` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the PIN to use for challenge dialogs. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Returns true if the challenge PIN was set successfully. |

### setUserRestriction

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setUserRestriction(
    key: String!, 
    value: Boolean
): Unit
```

**Deprecated:** *use `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#addUserRestriction(android.content.ComponentName,%20kotlin.String)` or `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#clearUserRestriction(android.content.ComponentName,%20kotlin.String)` instead.*

Sets the value of a specific restriction on the context user. Requires the MANAGE_USERS permission. 
Requires android.Manifest.permission.MANAGE_USERS

| Parameters ||
|---|---|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the key of the restriction |
| `value` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): the value for the restriction |

### setUserRestrictions

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setUserRestrictions(restrictions: Bundle!): Unit
```

**Deprecated:** *Deprecated in Java.*

This will no longer work. Device owners and profile owners should use `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#addUserRestriction(android.content.ComponentName,%20kotlin.String)` instead.

### setUserRestrictions

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setUserRestrictions(
    restrictions: Bundle!, 
    userHandle: UserHandle!
): Unit
```

**Deprecated:** *Deprecated in Java.*

This will no longer work. Device owners and profile owners should use `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#addUserRestriction(android.content.ComponentName,%20kotlin.String)` instead.

### supportsMultipleUsers

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun supportsMultipleUsers(): Boolean
```

Returns whether this device supports multiple switchable users with their own login and customizable space.

Note that, even if false, multiple users might still be possible, as long as no login UI is required; e.g., profiles might still be supported, as they do not require a login UI.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | whether the device supports multiple switchable users. |
