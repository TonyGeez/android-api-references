Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DevicePolicyIdentifiers

```
class DevicePolicyIdentifiers
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.app.admin.DevicePolicyIdentifiers](../android/app/admin/DevicePolicyIdentifiers.md) |

Class containing identifiers for policy APIs in `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager`, for example they will be passed in `https://developer.android.com/reference/kotlin/android/app/admin/PolicyUpdateReceiver#onPolicySetResult(android.content.Context,%20kotlin.String,%20android.os.Bundle,%20android.app.admin.TargetUser,%20android.app.admin.PolicyUpdateResult)` and `https://developer.android.com/reference/kotlin/android/app/admin/PolicyUpdateReceiver#onPolicyChanged(android.content.Context,%20kotlin.String,%20android.os.Bundle,%20android.app.admin.TargetUser,%20android.app.admin.PolicyUpdateResult)` to communicate updates of a certain policy back to the admin.

## Summary

| Constants ||
|---|---|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyIdentifiers#ACCOUNT_MANAGEMENT_DISABLED_POLICY:kotlin.String` String identifier for `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager#setAccountManagementDisabled(android.content.ComponentName,%20kotlin.String,%20kotlin.Boolean)`. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyIdentifiers#APPLICATION_HIDDEN_POLICY:kotlin.String` String identifier for `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager#setApplicationHidden(android.content.ComponentName,%20kotlin.String,%20kotlin.Boolean)`. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyIdentifiers#APPLICATION_RESTRICTIONS_POLICY:kotlin.String` String identifier for `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager#setApplicationRestrictions(android.content.ComponentName,%20kotlin.String,%20android.os.Bundle)`. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyIdentifiers#APP_FUNCTIONS_POLICY:kotlin.String` String identifier for `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager#setAppFunctionsPolicy(kotlin.Int)`. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyIdentifiers#AUTO_TIMEZONE_POLICY:kotlin.String` String identifier for `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager#setAutoTimeZoneEnabled(android.content.ComponentName,%20kotlin.Boolean)`. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyIdentifiers#AUTO_TIME_POLICY:kotlin.String` String identifier for `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager#setAutoTimeEnabled(android.content.ComponentName,%20kotlin.Boolean)`. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyIdentifiers#BACKUP_SERVICE_POLICY:kotlin.String` String identifier for `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager#setBackupServiceEnabled(android.content.ComponentName,%20kotlin.Boolean)`. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyIdentifiers#CAMERA_DISABLED_POLICY:kotlin.String` String identifier for `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager#setCameraDisabled(android.content.ComponentName,%20kotlin.Boolean)`. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyIdentifiers#CONTENT_PROTECTION_POLICY:kotlin.String` String identifier for `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager#setContentProtectionPolicy(android.content.ComponentName,%20kotlin.Int)`. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyIdentifiers#CROSS_PROFILE_WIDGET_PROVIDER_POLICY:kotlin.String` String identifier for `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager#addCrossProfileWidgetProvider(android.content.ComponentName,%20kotlin.String)`. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyIdentifiers#KEYGUARD_DISABLED_FEATURES_POLICY:kotlin.String` String identifier for `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager#setKeyguardDisabledFeatures(android.content.ComponentName,%20kotlin.Int)`. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyIdentifiers#LOCK_TASK_POLICY:kotlin.String` String identifier for `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager#setLockTaskPackages(android.content.ComponentName,%20kotlin.Array)`. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyIdentifiers#MEMORY_TAGGING_POLICY:kotlin.String` String identifier for `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager#setMtePolicy(kotlin.Int)`. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyIdentifiers#PACKAGES_SUSPENDED_POLICY:kotlin.String` String identifier for `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager#setPackagesSuspended(android.content.ComponentName,%20kotlin.Array,%20kotlin.Boolean)`. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyIdentifiers#PACKAGE_UNINSTALL_BLOCKED_POLICY:kotlin.String` String identifier for `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager#setUninstallBlocked(android.content.ComponentName,%20kotlin.String,%20kotlin.Boolean)`. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyIdentifiers#PASSWORD_COMPLEXITY_POLICY:kotlin.String` String identifier for `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager#setRequiredPasswordComplexity(kotlin.Int)`. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyIdentifiers#PERMISSION_GRANT_POLICY:kotlin.String` String identifier for `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager#setPermissionGrantState(android.content.ComponentName,%20kotlin.String,%20kotlin.String,%20kotlin.Int)`. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyIdentifiers#PERSISTENT_PREFERRED_ACTIVITY_POLICY:kotlin.String` String identifier for `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager#addPersistentPreferredActivity(android.content.ComponentName,%20android.content.IntentFilter,%20android.content.ComponentName)`. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyIdentifiers#RESET_PASSWORD_TOKEN_POLICY:kotlin.String` String identifier for `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager#setResetPasswordToken(android.content.ComponentName,%20kotlin.ByteArray)`. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyIdentifiers#SECURITY_LOGGING_POLICY:kotlin.String` String identifier for `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager#setSecurityLoggingEnabled(android.content.ComponentName,%20kotlin.Boolean)`. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyIdentifiers#STATUS_BAR_DISABLED_POLICY:kotlin.String` String identifier for `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager#setStatusBarDisabled(android.content.ComponentName,%20kotlin.Boolean)`. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyIdentifiers#USB_DATA_SIGNALING_POLICY:kotlin.String` String identifier for `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager#setUsbDataSignalingEnabled(kotlin.Boolean)`. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyIdentifiers#USER_CONTROL_DISABLED_PACKAGES_POLICY:kotlin.String` String identifier for `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager#setUserControlDisabledPackages(android.content.ComponentName,%20kotlin.collections.MutableList)`. |

| Public methods ||
|---|---|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyIdentifiers#getIdentifierForUserRestriction(kotlin.String)(restriction: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Returns a string identifier for the provided user restrictions, see `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager#addUserRestriction(android.content.ComponentName,%20kotlin.String)` and `https://developer.android.com/reference/kotlin/android/os/UserManager.html#` for the list of available restrictions. |

## Constants

### ACCOUNT_MANAGEMENT_DISABLED_POLICY

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACCOUNT_MANAGEMENT_DISABLED_POLICY: String
```

String identifier for `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager#setAccountManagementDisabled(android.content.ComponentName,%20kotlin.String,%20kotlin.Boolean)`.

 Value: "accountManagementDisabled"

### APPLICATION_HIDDEN_POLICY

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val APPLICATION_HIDDEN_POLICY: String
```

String identifier for `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager#setApplicationHidden(android.content.ComponentName,%20kotlin.String,%20kotlin.Boolean)`.

 Value: "applicationHidden"

### APPLICATION_RESTRICTIONS_POLICY

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val APPLICATION_RESTRICTIONS_POLICY: String
```

String identifier for `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager#setApplicationRestrictions(android.content.ComponentName,%20kotlin.String,%20android.os.Bundle)`.

 Value: "applicationRestrictions"

### APP_FUNCTIONS_POLICY

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val APP_FUNCTIONS_POLICY: String
```

String identifier for `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager#setAppFunctionsPolicy(kotlin.Int)`.

 Value: "appFunctions"

### AUTO_TIMEZONE_POLICY

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AUTO_TIMEZONE_POLICY: String
```

String identifier for `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager#setAutoTimeZoneEnabled(android.content.ComponentName,%20kotlin.Boolean)`.

 Value: "autoTimezone"

### AUTO_TIME_POLICY

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AUTO_TIME_POLICY: String
```

String identifier for `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager#setAutoTimeEnabled(android.content.ComponentName,%20kotlin.Boolean)`.

 Value: "autoTime"

### BACKUP_SERVICE_POLICY

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val BACKUP_SERVICE_POLICY: String
```

String identifier for `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager#setBackupServiceEnabled(android.content.ComponentName,%20kotlin.Boolean)`.

 Value: "backupService"

### CAMERA_DISABLED_POLICY

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CAMERA_DISABLED_POLICY: String
```

String identifier for `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager#setCameraDisabled(android.content.ComponentName,%20kotlin.Boolean)`.

 Value: "cameraDisabled"

### CONTENT_PROTECTION_POLICY

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTENT_PROTECTION_POLICY: String
```

String identifier for `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager#setContentProtectionPolicy(android.content.ComponentName,%20kotlin.Int)`.

 Value: "contentProtection"

### CROSS_PROFILE_WIDGET_PROVIDER_POLICY

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CROSS_PROFILE_WIDGET_PROVIDER_POLICY: String
```

String identifier for `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager#addCrossProfileWidgetProvider(android.content.ComponentName,%20kotlin.String)`.

 Value: "crossProfileWidgetProvider"

### KEYGUARD_DISABLED_FEATURES_POLICY

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYGUARD_DISABLED_FEATURES_POLICY: String
```

String identifier for `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager#setKeyguardDisabledFeatures(android.content.ComponentName,%20kotlin.Int)`.

 Value: "keyguardDisabledFeatures"

### LOCK_TASK_POLICY

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LOCK_TASK_POLICY: String
```

String identifier for `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager#setLockTaskPackages(android.content.ComponentName,%20kotlin.Array)`.

 Value: "lockTask"

### MEMORY_TAGGING_POLICY

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MEMORY_TAGGING_POLICY: String
```

String identifier for `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager#setMtePolicy(kotlin.Int)`.

 Value: "memoryTagging"

### PACKAGES_SUSPENDED_POLICY

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PACKAGES_SUSPENDED_POLICY: String
```

String identifier for `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager#setPackagesSuspended(android.content.ComponentName,%20kotlin.Array,%20kotlin.Boolean)`.

 Value: "packagesSuspended"

### PACKAGE_UNINSTALL_BLOCKED_POLICY

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PACKAGE_UNINSTALL_BLOCKED_POLICY: String
```

String identifier for `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager#setUninstallBlocked(android.content.ComponentName,%20kotlin.String,%20kotlin.Boolean)`.

 Value: "packageUninstallBlocked"

### PASSWORD_COMPLEXITY_POLICY

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PASSWORD_COMPLEXITY_POLICY: String
```

String identifier for `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager#setRequiredPasswordComplexity(kotlin.Int)`.

 Value: "passwordComplexity"

### PERMISSION_GRANT_POLICY

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PERMISSION_GRANT_POLICY: String
```

String identifier for `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager#setPermissionGrantState(android.content.ComponentName,%20kotlin.String,%20kotlin.String,%20kotlin.Int)`.

 Value: "permissionGrant"

### PERSISTENT_PREFERRED_ACTIVITY_POLICY

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PERSISTENT_PREFERRED_ACTIVITY_POLICY: String
```

String identifier for `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager#addPersistentPreferredActivity(android.content.ComponentName,%20android.content.IntentFilter,%20android.content.ComponentName)`.

 Value: "persistentPreferredActivity"

### RESET_PASSWORD_TOKEN_POLICY

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESET_PASSWORD_TOKEN_POLICY: String
```

String identifier for `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager#setResetPasswordToken(android.content.ComponentName,%20kotlin.ByteArray)`.

 Value: "resetPasswordToken"

### SECURITY_LOGGING_POLICY

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SECURITY_LOGGING_POLICY: String
```

String identifier for `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager#setSecurityLoggingEnabled(android.content.ComponentName,%20kotlin.Boolean)`.

 Value: "securityLogging"

### STATUS_BAR_DISABLED_POLICY

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATUS_BAR_DISABLED_POLICY: String
```

String identifier for `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager#setStatusBarDisabled(android.content.ComponentName,%20kotlin.Boolean)`.

 Value: "statusBarDisabled"

### USB_DATA_SIGNALING_POLICY

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val USB_DATA_SIGNALING_POLICY: String
```

String identifier for `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager#setUsbDataSignalingEnabled(kotlin.Boolean)`.

 Value: "usbDataSignaling"

### USER_CONTROL_DISABLED_PACKAGES_POLICY

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val USER_CONTROL_DISABLED_PACKAGES_POLICY: String
```

String identifier for `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager#setUserControlDisabledPackages(android.content.ComponentName,%20kotlin.collections.MutableList)`.

 Value: "userControlDisabledPackages"

## Public methods

### getIdentifierForUserRestriction

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getIdentifierForUserRestriction(restriction: String): String
```

Returns a string identifier for the provided user restrictions, see `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager#addUserRestriction(android.content.ComponentName,%20kotlin.String)` and `https://developer.android.com/reference/kotlin/android/os/UserManager.html#` for the list of available restrictions.

| Parameters ||
|---|---|
| `restriction` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): Value is one of the following: - `https://developer.android.com/reference/kotlin/android/os/UserManager.html#ALLOW_PARENT_PROFILE_APP_LINKING:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager.html#DISALLOW_ADD_MANAGED_PROFILE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager.html#DISALLOW_ADD_PRIVATE_PROFILE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager.html#DISALLOW_ADD_USER:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager.html#DISALLOW_ADD_WIFI_CONFIG:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager.html#DISALLOW_ADJUST_VOLUME:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager.html#DISALLOW_AIRPLANE_MODE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager.html#DISALLOW_AMBIENT_DISPLAY:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager.html#DISALLOW_APPS_CONTROL:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager.html#DISALLOW_ASSIST_CONTENT:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager.html#DISALLOW_AUTOFILL:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager.html#DISALLOW_BLUETOOTH:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager.html#DISALLOW_BLUETOOTH_SHARING:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager.html#DISALLOW_CAMERA_TOGGLE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager.html#DISALLOW_CELLULAR_2G:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager.html#DISALLOW_CHANGE_NEAR_FIELD_COMMUNICATION_RADIO:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager.html#DISALLOW_CHANGE_WIFI_STATE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager.html#DISALLOW_CONFIG_BLUETOOTH:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager.html#DISALLOW_CONFIG_BRIGHTNESS:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager.html#DISALLOW_CONFIG_CELL_BROADCASTS:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager.html#DISALLOW_CONFIG_CREDENTIALS:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager.html#DISALLOW_CONFIG_DATE_TIME:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager.html#DISALLOW_CONFIG_DEFAULT_APPS:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager.html#DISALLOW_CONFIG_LOCALE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager.html#DISALLOW_CONFIG_LOCATION:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager.html#DISALLOW_CONFIG_MOBILE_NETWORKS:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager.html#DISALLOW_CONFIG_PRIVATE_DNS:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager.html#DISALLOW_CONFIG_SCREEN_TIMEOUT:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager.html#DISALLOW_CONFIG_TETHERING:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager.html#DISALLOW_CONFIG_VPN:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager.html#DISALLOW_CONFIG_WIFI:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager.html#DISALLOW_CONTENT_CAPTURE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager.html#DISALLOW_CONTENT_SUGGESTIONS:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager.html#DISALLOW_CREATE_WINDOWS:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager.html#DISALLOW_CROSS_PROFILE_COPY_PASTE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager.html#DISALLOW_DATA_ROAMING:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager.html#DISALLOW_DEBUGGING_FEATURES:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager.html#DISALLOW_FACTORY_RESET:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager.html#DISALLOW_FUN:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager.html#DISALLOW_GRANT_ADMIN:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager.html#DISALLOW_TASK_CONTINUITY_HANDOFF:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager.html#DISALLOW_INSTALL_APPS:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager.html#DISALLOW_INSTALL_UNKNOWN_SOURCES:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager.html#DISALLOW_INSTALL_UNKNOWN_SOURCES_GLOBALLY:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager.html#DISALLOW_INSTALL_UNKNOWN_SOURCES_INCLUDING_REGISTERED_APP_STORES:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager.html#DISALLOW_MICROPHONE_TOGGLE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager.html#DISALLOW_MODIFY_ACCOUNTS:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager.html#DISALLOW_MOUNT_PHYSICAL_MEDIA:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager.html#DISALLOW_NEAR_FIELD_COMMUNICATION_RADIO:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager.html#DISALLOW_NETWORK_RESET:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager.html#DISALLOW_OUTGOING_BEAM:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager.html#DISALLOW_OUTGOING_CALLS:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager.html#DISALLOW_PRINTING:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager.html#DISALLOW_REMOVE_MANAGED_PROFILE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager.html#DISALLOW_REMOVE_USER:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager.html#DISALLOW_SAFE_BOOT:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager.html#DISALLOW_SET_USER_ICON:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager.html#DISALLOW_SET_WALLPAPER:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager.html#DISALLOW_SHARE_INTO_MANAGED_PROFILE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager.html#DISALLOW_SHARE_LOCATION:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager.html#DISALLOW_SHARING_ADMIN_CONFIGURED_WIFI:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager.html#DISALLOW_SIM_GLOBALLY:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager.html#DISALLOW_SMS:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager.html#DISALLOW_SYSTEM_ERROR_DIALOGS:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager.html#DISALLOW_THREAD_NETWORK:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager.html#DISALLOW_ULTRA_WIDEBAND_RADIO:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager.html#DISALLOW_UNIFIED_PASSWORD:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager.html#DISALLOW_UNINSTALL_APPS:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager.html#DISALLOW_UNMUTE_MICROPHONE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager.html#DISALLOW_USB_FILE_TRANSFER:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager.html#DISALLOW_USER_SWITCH:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager.html#DISALLOW_WIFI_DIRECT:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager.html#DISALLOW_WIFI_TETHERING:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager.html#ENSURE_VERIFY_APPS:kotlin.String` - `https://developer.android.com/reference/kotlin/android/os/UserManager.html#KEY_RESTRICTIONS_PENDING:kotlin.String` . This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | This value cannot be `null`. |
