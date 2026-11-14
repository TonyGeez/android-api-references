Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SecurityLog

```
open class SecurityLog
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.app.admin.SecurityLog](../android/app/admin/SecurityLog.md) |

Definitions for working with security logs.

Device owner apps can control the logging with `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager#setSecurityLoggingEnabled(android.content.ComponentName,%20kotlin.Boolean)`. When security logs are enabled, device owner apps receive periodic callbacks from `https://developer.android.com/reference/kotlin/android/app/admin/DeviceAdminReceiver#onSecurityLogsAvailable(android.content.Context,%20android.content.Intent)`, at which time new batch of logs can be collected via `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager#retrieveSecurityLogs(android.content.ComponentName)`. `https://developer.android.com/reference/kotlin/android/app/admin/SecurityLog.SecurityEvent` describes the type and format of security logs being collected.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/app/admin/SecurityLog.SecurityEvent` A class representing a security event log entry. |

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/admin/SecurityLog#LEVEL_ERROR:kotlin.Int` Event severity level indicating that the event requires urgent admin action. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/admin/SecurityLog#LEVEL_INFO:kotlin.Int` Event severity level indicating that the event corresponds to normal workflow. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/admin/SecurityLog#LEVEL_WARNING:kotlin.Int` Event severity level indicating that the event may require admin attention. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/admin/SecurityLog#TAG_ADB_SHELL_CMD:kotlin.Int` Indicates that a shell command was issued over ADB via `adb shell <command>` The log entry contains a `String` payload containing the shell command, accessible via `https://developer.android.com/reference/kotlin/android/app/admin/SecurityLog.SecurityEvent#getData()`. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/admin/SecurityLog#TAG_ADB_SHELL_INTERACTIVE:kotlin.Int` Indicates that an ADB interactive shell was opened via "adb shell". |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/admin/SecurityLog#TAG_APP_PROCESS_START:kotlin.Int` Indicates that an app process was started. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/admin/SecurityLog#TAG_BACKUP_SERVICE_TOGGLED:kotlin.Int` Indicates that an admin has enabled or disabled backup service. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/admin/SecurityLog#TAG_BLUETOOTH_CONNECTION:kotlin.Int` Indicates that the device attempts to connect to a Bluetooth device. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/admin/SecurityLog#TAG_BLUETOOTH_DISCONNECTION:kotlin.Int` Indicates that the device disconnects from a connected Bluetooth device. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/admin/SecurityLog#TAG_CAMERA_POLICY_SET:kotlin.Int` Indicates that the admin has set policy to disable camera. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/admin/SecurityLog#TAG_CERT_AUTHORITY_INSTALLED:kotlin.Int` Indicates that a new root certificate has been installed into system's trusted credential storage. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/admin/SecurityLog#TAG_CERT_AUTHORITY_REMOVED:kotlin.Int` Indicates that a new root certificate has been removed from system's trusted credential storage. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/admin/SecurityLog#TAG_CERT_VALIDATION_FAILURE:kotlin.Int` Indicates a failure to validate X. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/admin/SecurityLog#TAG_CRYPTO_SELF_TEST_COMPLETED:kotlin.Int` Indicates that cryptographic functionality self test has completed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/admin/SecurityLog#TAG_KEYGUARD_DISABLED_FEATURES_SET:kotlin.Int` Indicates that an admin has set disabled keyguard features. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/admin/SecurityLog#TAG_KEYGUARD_DISMISSED:kotlin.Int` Indicates that keyguard has been dismissed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/admin/SecurityLog#TAG_KEYGUARD_DISMISS_AUTH_ATTEMPT:kotlin.Int` Indicates that there has been an authentication attempt to dismiss the keyguard. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/admin/SecurityLog#TAG_KEYGUARD_SECURED:kotlin.Int` Indicates that the device has been locked, either by the user or by a timeout. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/admin/SecurityLog#TAG_KEY_DESTRUCTION:kotlin.Int` Indicates that a cryptographic key was destroyed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/admin/SecurityLog#TAG_KEY_GENERATED:kotlin.Int` Indicates that a cryptographic key was generated. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/admin/SecurityLog#TAG_KEY_IMPORT:kotlin.Int` Indicates that a cryptographic key was imported. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/admin/SecurityLog#TAG_KEY_INTEGRITY_VIOLATION:kotlin.Int` Indicates a failed cryptographic key integrity check. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/admin/SecurityLog#TAG_LOGGING_STARTED:kotlin.Int` Indicates start-up of audit logging. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/admin/SecurityLog#TAG_LOGGING_STOPPED:kotlin.Int` Indicates shutdown of audit logging. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/admin/SecurityLog#TAG_LOG_BUFFER_SIZE_CRITICAL:kotlin.Int` Indicates that the audit log buffer has reached 90% of its capacity. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/admin/SecurityLog#TAG_MAX_PASSWORD_ATTEMPTS_SET:kotlin.Int` Indicates that an admin has set a maximum number of failed password attempts before wiping data. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/admin/SecurityLog#TAG_MAX_SCREEN_LOCK_TIMEOUT_SET:kotlin.Int` Indicates that an admin has set a maximum screen lock timeout. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/admin/SecurityLog#TAG_MEDIA_MOUNT:kotlin.Int` Indicates that removable media has been mounted on the device. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/admin/SecurityLog#TAG_MEDIA_UNMOUNT:kotlin.Int` Indicates that removable media was unmounted from the device. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/admin/SecurityLog#TAG_NFC_DISABLED:kotlin.Int` Indicates that NFC service is disabled. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/admin/SecurityLog#TAG_NFC_ENABLED:kotlin.Int` Indicates that NFC service is enabled. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/admin/SecurityLog#TAG_OS_SHUTDOWN:kotlin.Int` Indicates that the Android OS has shutdown. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/admin/SecurityLog#TAG_OS_STARTUP:kotlin.Int` Indicates that the Android OS has started. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/admin/SecurityLog#TAG_PACKAGE_INSTALLED:kotlin.Int` Indicates that a package is installed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/admin/SecurityLog#TAG_PACKAGE_UNINSTALLED:kotlin.Int` Indicates that a package is uninstalled. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/admin/SecurityLog#TAG_PACKAGE_UPDATED:kotlin.Int` Indicates that a package is updated. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/admin/SecurityLog#TAG_PASSWORD_CHANGED:kotlin.Int` Indicates that a user has just changed their lockscreen password. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/admin/SecurityLog#TAG_PASSWORD_COMPLEXITY_REQUIRED:kotlin.Int` Indicates that an admin has set a password complexity requirement, using the platform's pre-defined complexity levels. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/admin/SecurityLog#TAG_PASSWORD_COMPLEXITY_SET:kotlin.Int` Indicates that an admin has set a requirement for password complexity. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/admin/SecurityLog#TAG_PASSWORD_EXPIRATION_SET:kotlin.Int` Indicates that an admin has set a password expiration timeout. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/admin/SecurityLog#TAG_PASSWORD_HISTORY_LENGTH_SET:kotlin.Int` Indicates that an admin has set a password history length. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/admin/SecurityLog#TAG_REMOTE_LOCK:kotlin.Int` Indicates that an admin remotely locked the device or profile. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/admin/SecurityLog#TAG_SYNC_RECV_FILE:kotlin.Int` Indicates that a file was pulled from the device via the adb daemon, for example via `adb pull`. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/admin/SecurityLog#TAG_SYNC_SEND_FILE:kotlin.Int` Indicates that a file was pushed to the device via the adb daemon, for example via `adb push`. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/admin/SecurityLog#TAG_USER_RESTRICTION_ADDED:kotlin.Int` Indicates that an admin has set a user restriction. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/admin/SecurityLog#TAG_USER_RESTRICTION_REMOVED:kotlin.Int` Indicates that an admin has removed a user restriction. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/admin/SecurityLog#TAG_WIFI_CONNECTION:kotlin.Int` Indicates that an event occurred as the device attempted to connect to a managed WiFi network. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/admin/SecurityLog#TAG_WIFI_DISCONNECTION:kotlin.Int` Indicates that the device disconnects from a managed WiFi network. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/admin/SecurityLog#TAG_WIPE_FAILURE:kotlin.Int` Indicates a failure to wipe device or user data. |

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/app/admin/SecurityLog#SecurityLog()()` <br /> |

## Constants

### LEVEL_ERROR

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LEVEL_ERROR: Int
```

Event severity level indicating that the event requires urgent admin action.

 Value: 3

### LEVEL_INFO

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LEVEL_INFO: Int
```

Event severity level indicating that the event corresponds to normal workflow.

 Value: 1

### LEVEL_WARNING

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LEVEL_WARNING: Int
```

Event severity level indicating that the event may require admin attention.

 Value: 2

### TAG_ADB_SHELL_CMD

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TAG_ADB_SHELL_CMD: Int
```

Indicates that a shell command was issued over ADB via `adb shell <command>` The log entry contains a `String` payload containing the shell command, accessible via `https://developer.android.com/reference/kotlin/android/app/admin/SecurityLog.SecurityEvent#getData()`. If security logging is enabled on organization-owned managed profile devices, the shell command will be redacted to an empty string.

 Value: 210002

### TAG_ADB_SHELL_INTERACTIVE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TAG_ADB_SHELL_INTERACTIVE: Int
```

Indicates that an ADB interactive shell was opened via "adb shell". There is no extra payload in the log event.

 Value: 210001

### TAG_APP_PROCESS_START

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TAG_APP_PROCESS_START: Int
```

Indicates that an app process was started. The log entry contains the following information about the process encapsulated in an `https://developer.android.com/reference/kotlin/java/lang/Object.html#` array, accessible via `https://developer.android.com/reference/kotlin/android/app/admin/SecurityLog.SecurityEvent#getData()`:
- \[0\] process name (`String`)
- \[1\] exact start time in milliseconds according to `System.currentTimeMillis()` (`Long`)
- \[2\] app uid (`Integer`)
- \[3\] app pid (`Integer`)
- \[4\] seinfo tag (`String`)
- \[5\] SHA-256 hash of the base APK in hexadecimal (`String`) If security logging is enabled on organization-owned managed profile devices, only events happening inside the managed profile will be visible.

 Value: 210005

### TAG_BACKUP_SERVICE_TOGGLED

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TAG_BACKUP_SERVICE_TOGGLED: Int
```

Indicates that an admin has enabled or disabled backup service. The log entry contains the following information about the event encapsulated in an `https://developer.android.com/reference/kotlin/java/lang/Object.html#` array, accessible via `https://developer.android.com/reference/kotlin/android/app/admin/SecurityLog.SecurityEvent#getData()`:
- \[0\] admin package name (`String`)
- \[1\] admin user ID (`Integer`)
- \[2\] backup service state (`Integer`, 1 for enabled, 0 for disabled)

 Value: 210044

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager#setBackupServiceEnabled(android.content.ComponentName,%20kotlin.Boolean)`

### TAG_BLUETOOTH_CONNECTION

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TAG_BLUETOOTH_CONNECTION: Int
```

Indicates that the device attempts to connect to a Bluetooth device. The log entry contains the following information about the event, encapsulated in an `https://developer.android.com/reference/kotlin/java/lang/Object.html#` array and accessible via `https://developer.android.com/reference/kotlin/android/app/admin/SecurityLog.SecurityEvent#getData()`:
- \[0\] The MAC address of the Bluetooth device (`String`)
- \[1\] Whether the connection is successful (`Integer`, 1 if successful, 0 otherwise)
- \[2\] Optional human-readable failure reason, empty string if none (`String`)

 Value: 210039

### TAG_BLUETOOTH_DISCONNECTION

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TAG_BLUETOOTH_DISCONNECTION: Int
```

Indicates that the device disconnects from a connected Bluetooth device. The log entry contains the following information about the event, encapsulated in an `https://developer.android.com/reference/kotlin/java/lang/Object.html#` array and accessible via `https://developer.android.com/reference/kotlin/android/app/admin/SecurityLog.SecurityEvent#getData()`:
- \[0\] The MAC address of the connected Bluetooth device (`String`)
- \[1\] Optional human-readable disconnection reason, empty string if none (`String`)

 Value: 210040

### TAG_CAMERA_POLICY_SET

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TAG_CAMERA_POLICY_SET: Int
```

Indicates that the admin has set policy to disable camera. The log entry contains the following information about the event, encapsulated in an `https://developer.android.com/reference/kotlin/java/lang/Object.html#` array and accessible via `https://developer.android.com/reference/kotlin/android/app/admin/SecurityLog.SecurityEvent#getData()`:
- \[0\] admin package name (`String`)
- \[1\] admin user ID (`Integer`)
- \[2\] target user ID (`Integer`)
- \[3\] whether the camera is disabled or not (`Integer`, 1 if it's disabled, 0 if enabled)

 Value: 210034

### TAG_CERT_AUTHORITY_INSTALLED

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TAG_CERT_AUTHORITY_INSTALLED: Int
```

Indicates that a new root certificate has been installed into system's trusted credential storage. The log entry contains the following information about the event, encapsulated in an `https://developer.android.com/reference/kotlin/java/lang/Object.html#` array and accessible via `https://developer.android.com/reference/kotlin/android/app/admin/SecurityLog.SecurityEvent#getData()`:
- \[0\] result (`Integer`, 0 if operation failed, 1 if succeeded)
- \[1\] subject of the certificate (`String`).
- \[2\] which user the certificate is installed for (`Integer`), only available from version `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int`.

 If security logging is enabled on organization-owned managed profile devices, only events happening inside the managed profile will be visible.

 Value: 210029

### TAG_CERT_AUTHORITY_REMOVED

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TAG_CERT_AUTHORITY_REMOVED: Int
```

Indicates that a new root certificate has been removed from system's trusted credential storage. The log entry contains the following information about the event, encapsulated in an `https://developer.android.com/reference/kotlin/java/lang/Object.html#` array and accessible via `https://developer.android.com/reference/kotlin/android/app/admin/SecurityLog.SecurityEvent#getData()`:
- \[0\] result (`Integer`, 0 if operation failed, 1 if succeeded)
- \[1\] subject of the certificate (`String`).
- \[2\] which user the certificate is removed from (`Integer`), only available from version `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int`.

 If security logging is enabled on organization-owned managed profile devices, only events happening inside the managed profile will be visible.

 Value: 210030

### TAG_CERT_VALIDATION_FAILURE

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TAG_CERT_VALIDATION_FAILURE: Int
```

Indicates a failure to validate X.509v3 certificate. The log entry contains a `String` payload indicating the failure reason, accessible via `https://developer.android.com/reference/kotlin/android/app/admin/SecurityLog.SecurityEvent#getData()`.

 Value: 210033

### TAG_CRYPTO_SELF_TEST_COMPLETED

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TAG_CRYPTO_SELF_TEST_COMPLETED: Int
```

Indicates that cryptographic functionality self test has completed. The log entry contains an `Integer` payload, indicating the result of the test (0 if the test failed, 1 if succeeded) and accessible via `https://developer.android.com/reference/kotlin/android/app/admin/SecurityLog.SecurityEvent#getData()`.

 Value: 210031

### TAG_KEYGUARD_DISABLED_FEATURES_SET

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TAG_KEYGUARD_DISABLED_FEATURES_SET: Int
```

Indicates that an admin has set disabled keyguard features. The log entry contains the following information about the event encapsulated in an `https://developer.android.com/reference/kotlin/java/lang/Object.html#` array, accessible via `https://developer.android.com/reference/kotlin/android/app/admin/SecurityLog.SecurityEvent#getData()`:
- \[0\] admin package name (`String`)
- \[1\] admin user ID (`Integer`)
- \[2\] target user ID (`Integer`)
- \[3\] disabled keyguard feature mask (`Integer`).

 Value: 210021

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager#setKeyguardDisabledFeatures(android.content.ComponentName,%20kotlin.Int)`

### TAG_KEYGUARD_DISMISSED

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TAG_KEYGUARD_DISMISSED: Int
```

Indicates that keyguard has been dismissed. This event is only logged if the device has a secure keyguard. It is logged regardless of how keyguard is dismissed, including via PIN/pattern/password, biometrics or via a trust agent. There is no extra payload in the log event.

 Value: 210006

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/admin/SecurityLog#TAG_KEYGUARD_DISMISS_AUTH_ATTEMPT:kotlin.Int`

### TAG_KEYGUARD_DISMISS_AUTH_ATTEMPT

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TAG_KEYGUARD_DISMISS_AUTH_ATTEMPT: Int
```

Indicates that there has been an authentication attempt to dismiss the keyguard. The log entry contains the following information about the attempt encapsulated in an `https://developer.android.com/reference/kotlin/java/lang/Object.html#` array, accessible via `https://developer.android.com/reference/kotlin/android/app/admin/SecurityLog.SecurityEvent#getData()`:
- \[0\] attempt result (`Integer`, 1 for successful, 0 for unsuccessful)
- \[1\] strength of authentication method (`Integer`, 1 if strong authentication method was used, 0 otherwise)

 Value: 210007

### TAG_KEYGUARD_SECURED

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TAG_KEYGUARD_SECURED: Int
```

Indicates that the device has been locked, either by the user or by a timeout. There is no extra payload in the log event.

 Value: 210008

### TAG_KEY_DESTRUCTION

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TAG_KEY_DESTRUCTION: Int
```

Indicates that a cryptographic key was destroyed. The log entry contains the following information about the event, encapsulated in an `https://developer.android.com/reference/kotlin/java/lang/Object.html#` array and accessible via `https://developer.android.com/reference/kotlin/android/app/admin/SecurityLog.SecurityEvent#getData()`:

- \[0\] result (`Integer`, 0 if operation failed, 1 if succeeded)
- \[1\] alias of the key (`String`)
- \[2\] owner of the key (`Integer`):
 - If the top bit is clear, this is the requesting process uid.
 - If the top bit is set, this identifies an [SELinux label](https://source.android.com/docs/security/features/keystore#selinux-policy).

If security logging is enabled on organization-owned managed profile devices, only events happening inside the managed profile will be visible.

<br />

 Value: 210026

### TAG_KEY_GENERATED

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TAG_KEY_GENERATED: Int
```

Indicates that a cryptographic key was generated. The log entry contains the following information about the event, encapsulated in an `https://developer.android.com/reference/kotlin/java/lang/Object.html#` array and accessible via `https://developer.android.com/reference/kotlin/android/app/admin/SecurityLog.SecurityEvent#getData()`:

- \[0\] result (`Integer`, 0 if operation failed, 1 if succeeded)
- \[1\] alias of the key (`String`)
- \[2\] owner of the key (`Integer`):
 - If the top bit is clear, this is the requesting process uid.
 - If the top bit is set, this identifies an [SELinux label](https://source.android.com/docs/security/features/keystore#selinux-policy).

If security logging is enabled on organization-owned managed profile devices, only events happening inside the managed profile will be visible.

<br />

 Value: 210024

### TAG_KEY_IMPORT

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TAG_KEY_IMPORT: Int
```

Indicates that a cryptographic key was imported. The log entry contains the following information about the event, encapsulated in an `https://developer.android.com/reference/kotlin/java/lang/Object.html#` array and accessible via `https://developer.android.com/reference/kotlin/android/app/admin/SecurityLog.SecurityEvent#getData()`:

- \[0\] result (`Integer`, 0 if operation failed, 1 if succeeded)
- \[1\] alias of the key (`String`)
- \[2\] owner of the key (`Integer`):
 - If the top bit is clear, this is the requesting process uid.
 - If the top bit is set, this identifies an [SELinux label](https://source.android.com/docs/security/features/keystore#selinux-policy).

If security logging is enabled on organization-owned managed profile devices, only events happening inside the managed profile will be visible.

<br />

 Value: 210025

### TAG_KEY_INTEGRITY_VIOLATION

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TAG_KEY_INTEGRITY_VIOLATION: Int
```

Indicates a failed cryptographic key integrity check. The log entry contains the following information about the event, encapsulated in an `https://developer.android.com/reference/kotlin/java/lang/Object.html#` array and accessible via `https://developer.android.com/reference/kotlin/android/app/admin/SecurityLog.SecurityEvent#getData()`:

- \[0\] alias of the key (`String`)
- \[1\] owner of the key (`Integer`):
 - If the top bit is clear, this is the requesting process uid.
 - If the top bit is set, this identifies an [SELinux label](https://source.android.com/docs/security/features/keystore#selinux-policy).

If security logging is enabled on organization-owned managed profile devices, only events happening inside the managed profile will be visible.

<br />

 Value: 210032

### TAG_LOGGING_STARTED

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TAG_LOGGING_STARTED: Int
```

Indicates start-up of audit logging. There is no extra payload in the log event.

 Value: 210011

### TAG_LOGGING_STOPPED

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TAG_LOGGING_STOPPED: Int
```

Indicates shutdown of audit logging. There is no extra payload in the log event.

 Value: 210012

### TAG_LOG_BUFFER_SIZE_CRITICAL

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TAG_LOG_BUFFER_SIZE_CRITICAL: Int
```

Indicates that the audit log buffer has reached 90% of its capacity. There is no extra payload in the log event.

 Value: 210015

### TAG_MAX_PASSWORD_ATTEMPTS_SET

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TAG_MAX_PASSWORD_ATTEMPTS_SET: Int
```

Indicates that an admin has set a maximum number of failed password attempts before wiping data. The log entry contains the following information about the event encapsulated in an `https://developer.android.com/reference/kotlin/java/lang/Object.html#` array, accessible via `https://developer.android.com/reference/kotlin/android/app/admin/SecurityLog.SecurityEvent#getData()`:
- \[0\] admin package name (`String`)
- \[1\] admin user ID (`Integer`)
- \[2\] target user ID (`Integer`)
- \[3\] new maximum number of failed password attempts (`Integer`)

 Value: 210020

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager#setMaximumFailedPasswordsForWipe(android.content.ComponentName,%20kotlin.Int)`

### TAG_MAX_SCREEN_LOCK_TIMEOUT_SET

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TAG_MAX_SCREEN_LOCK_TIMEOUT_SET: Int
```

Indicates that an admin has set a maximum screen lock timeout. The log entry contains the following information about the event encapsulated in an `https://developer.android.com/reference/kotlin/java/lang/Object.html#` array, accessible via `https://developer.android.com/reference/kotlin/android/app/admin/SecurityLog.SecurityEvent#getData()`:
- \[0\] admin package name (`String`)
- \[1\] admin user ID (`Integer`)
- \[2\] target user ID (`Integer`)
- \[3\] new screen lock timeout in milliseconds (`Long`)

 Value: 210019

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager#setMaximumTimeToLock(android.content.ComponentName,%20kotlin.Long)`

### TAG_MEDIA_MOUNT

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TAG_MEDIA_MOUNT: Int
```

Indicates that removable media has been mounted on the device. The log entry contains the following information about the event, encapsulated in an `https://developer.android.com/reference/kotlin/java/lang/Object.html#` array and accessible via `https://developer.android.com/reference/kotlin/android/app/admin/SecurityLog.SecurityEvent#getData()`:
- \[0\] mount point (`String`)
- \[1\] volume label (`String`). Redacted to empty string on organization-owned managed profile devices.

 Value: 210013

### TAG_MEDIA_UNMOUNT

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TAG_MEDIA_UNMOUNT: Int
```

Indicates that removable media was unmounted from the device. The log entry contains the following information about the event, encapsulated in an `https://developer.android.com/reference/kotlin/java/lang/Object.html#` array and accessible via `https://developer.android.com/reference/kotlin/android/app/admin/SecurityLog.SecurityEvent#getData()`:
- \[0\] mount point (`String`)
- \[1\] volume label (`String`). Redacted to empty string on organization-owned managed profile devices.

 Value: 210014

### TAG_NFC_DISABLED

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TAG_NFC_DISABLED: Int
```

Indicates that NFC service is disabled. There is no extra payload in the log event.

 Value: 210046

### TAG_NFC_ENABLED

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TAG_NFC_ENABLED: Int
```

Indicates that NFC service is enabled. There is no extra payload in the log event.

 Value: 210045

### TAG_OS_SHUTDOWN

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TAG_OS_SHUTDOWN: Int
```

Indicates that the Android OS has shutdown. There is no extra payload in the log event.

 Value: 210010

### TAG_OS_STARTUP

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TAG_OS_STARTUP: Int
```

Indicates that the Android OS has started. The log entry contains the following information about the startup time software integrity check encapsulated in an `https://developer.android.com/reference/kotlin/java/lang/Object.html#` array, accessible via `https://developer.android.com/reference/kotlin/android/app/admin/SecurityLog.SecurityEvent#getData()`:
- \[0\] Verified Boot state (`String`)
- \[1\] dm-verity mode (`String`).

 Verified Boot state can be one of the following:
- `green` indicates that there is a full chain of trust extending from the bootloader to verified partitions including the bootloader, boot partition, and all verified partitions.
- `yellow` indicates that the boot partition has been verified using the embedded certificate and the signature is valid.
- `orange` indicates that the device may be freely modified. Device integrity is left to the user to verify out-of-band.

 dm-verity mode can be one of the following:
- `enforcing` indicates that the device will be restarted when corruption is detected.
- `eio` indicates that an I/O error will be returned for an attempt to read corrupted data blocks.
- `disabled` indicates that integrity check is disabled. For details see Verified Boot documentation.

 Value: 210009

### TAG_PACKAGE_INSTALLED

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TAG_PACKAGE_INSTALLED: Int
```

Indicates that a package is installed. The log entry contains the following information about the event, encapsulated in an `https://developer.android.com/reference/kotlin/java/lang/Object.html#` array and accessible via `https://developer.android.com/reference/kotlin/android/app/admin/SecurityLog.SecurityEvent#getData()`:
- \[0\] Name of the package being installed (`String`)
- \[1\] Package version code (`Long`)
- \[2\] UserId of the user that installed this package (`Integer`)

 Value: 210041

### TAG_PACKAGE_UNINSTALLED

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TAG_PACKAGE_UNINSTALLED: Int
```

Indicates that a package is uninstalled. The log entry contains the following information about the event, encapsulated in an `https://developer.android.com/reference/kotlin/java/lang/Object.html#` array and accessible via `https://developer.android.com/reference/kotlin/android/app/admin/SecurityLog.SecurityEvent#getData()`:
- \[0\] Name of the package being uninstalled (`String`)
- \[1\] Package version code (`Long`)
- \[2\] UserId of the user that uninstalled this package (`Integer`)

 Value: 210043

### TAG_PACKAGE_UPDATED

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TAG_PACKAGE_UPDATED: Int
```

Indicates that a package is updated. The log entry contains the following information about the event, encapsulated in an `https://developer.android.com/reference/kotlin/java/lang/Object.html#` array and accessible via `https://developer.android.com/reference/kotlin/android/app/admin/SecurityLog.SecurityEvent#getData()`:
- \[0\] Name of the package being updated (`String`)
- \[1\] Package version code (`Long`)
- \[2\] UserId of the user that updated this package (`Integer`)

 Value: 210042

### TAG_PASSWORD_CHANGED

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TAG_PASSWORD_CHANGED: Int
```

Indicates that a user has just changed their lockscreen password. The log entry contains the following information about the event, encapsulated in an `https://developer.android.com/reference/kotlin/java/lang/Object.html#` array and accessible via `https://developer.android.com/reference/kotlin/android/app/admin/SecurityLog.SecurityEvent#getData()`:
- \[0\] complexity for the new password (`Integer`)
- \[1\] target user ID (`Integer`)

 Password complexity levels are defined as in `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager#getPasswordComplexity()`

 Value: 210036

### TAG_PASSWORD_COMPLEXITY_REQUIRED

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TAG_PASSWORD_COMPLEXITY_REQUIRED: Int
```

Indicates that an admin has set a password complexity requirement, using the platform's pre-defined complexity levels. The log entry contains the following information about the event, encapsulated in an `https://developer.android.com/reference/kotlin/java/lang/Object.html#` array and accessible via `https://developer.android.com/reference/kotlin/android/app/admin/SecurityLog.SecurityEvent#getData()`:
- \[0\] admin package name (`String`)
- \[1\] admin user ID (`Integer`)
- \[2\] target user ID (`Integer`)
- \[3\] Password complexity (`Integer`)

 Value: 210035

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager#setRequiredPasswordComplexity(kotlin.Int)`

### TAG_PASSWORD_COMPLEXITY_SET

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TAG_PASSWORD_COMPLEXITY_SET: Int
```

Indicates that an admin has set a requirement for password complexity. The log entry contains the following information about the event, encapsulated in an `https://developer.android.com/reference/kotlin/java/lang/Object.html#` array and accessible via `https://developer.android.com/reference/kotlin/android/app/admin/SecurityLog.SecurityEvent#getData()`:
- \[0\] admin package name (`String`)
- \[1\] admin user ID (`Integer`)
- \[2\] target user ID (`Integer`)
- \[3\] minimum password length (`Integer`)
- \[4\] password quality constraint (`Integer`)
- \[5\] minimum number of letters (`Integer`)
- \[6\] minimum number of non-letters (`Integer`)
- \[7\] minimum number of digits (`Integer`)
- \[8\] minimum number of uppercase letters (`Integer`)
- \[9\] minimum number of lowercase letters (`Integer`)
- \[10\] minimum number of symbols (`Integer`)

 Value: 210017

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager#setPasswordMinimumLength(android.content.ComponentName,%20kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager#setPasswordQuality(android.content.ComponentName,%20kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager#setPasswordMinimumLetters(android.content.ComponentName,%20kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager#setPasswordMinimumNonLetter(android.content.ComponentName,%20kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager#setPasswordMinimumLowerCase(android.content.ComponentName,%20kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager#setPasswordMinimumUpperCase(android.content.ComponentName,%20kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager#setPasswordMinimumNumeric(android.content.ComponentName,%20kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager#setPasswordMinimumSymbols(android.content.ComponentName,%20kotlin.Int)`

### TAG_PASSWORD_EXPIRATION_SET

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TAG_PASSWORD_EXPIRATION_SET: Int
```

Indicates that an admin has set a password expiration timeout. The log entry contains the following information about the event, encapsulated in an `https://developer.android.com/reference/kotlin/java/lang/Object.html#` array and accessible via `https://developer.android.com/reference/kotlin/android/app/admin/SecurityLog.SecurityEvent#getData()`:
- \[0\] admin package name (`String`)
- \[1\] admin user ID (`Integer`)
- \[2\] target user ID (`Integer`)
- \[3\] new password expiration timeout in milliseconds (`Long`).

 Value: 210016

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager#setPasswordExpirationTimeout(android.content.ComponentName,%20kotlin.Long)`

### TAG_PASSWORD_HISTORY_LENGTH_SET

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TAG_PASSWORD_HISTORY_LENGTH_SET: Int
```

Indicates that an admin has set a password history length. The log entry contains the following information about the event encapsulated in an `https://developer.android.com/reference/kotlin/java/lang/Object.html#` array, accessible via `https://developer.android.com/reference/kotlin/android/app/admin/SecurityLog.SecurityEvent#getData()`:
- \[0\] admin package name (`String`)
- \[1\] admin user ID (`Integer`)
- \[2\] target user ID (`Integer`)
- \[3\] new password history length value (`Integer`)

 Value: 210018

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager#setPasswordHistoryLength(android.content.ComponentName,%20kotlin.Int)`

### TAG_REMOTE_LOCK

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TAG_REMOTE_LOCK: Int
```

Indicates that an admin remotely locked the device or profile. The log entry contains the following information about the event encapsulated in an `https://developer.android.com/reference/kotlin/java/lang/Object.html#` array, accessible via `https://developer.android.com/reference/kotlin/android/app/admin/SecurityLog.SecurityEvent#getData()`:
- \[0\] admin package name (`String`),
- \[1\] admin user ID (`Integer`).
- \[2\] target user ID (`Integer`)

 Value: 210022

### TAG_SYNC_RECV_FILE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TAG_SYNC_RECV_FILE: Int
```

Indicates that a file was pulled from the device via the adb daemon, for example via `adb pull`. The log entry contains a `String` payload containing the path of the pulled file on the device, accessible via `https://developer.android.com/reference/kotlin/android/app/admin/SecurityLog.SecurityEvent#getData()`.

 Value: 210003

### TAG_SYNC_SEND_FILE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TAG_SYNC_SEND_FILE: Int
```

Indicates that a file was pushed to the device via the adb daemon, for example via `adb push`. The log entry contains a `String` payload containing the destination path of the pushed file, accessible via `https://developer.android.com/reference/kotlin/android/app/admin/SecurityLog.SecurityEvent#getData()`.

 Value: 210004

### TAG_USER_RESTRICTION_ADDED

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TAG_USER_RESTRICTION_ADDED: Int
```

Indicates that an admin has set a user restriction. The log entry contains the following information about the event, encapsulated in an `https://developer.android.com/reference/kotlin/java/lang/Object.html#` array and accessible via `https://developer.android.com/reference/kotlin/android/app/admin/SecurityLog.SecurityEvent#getData()`:
- \[0\] admin package name (`String`)
- \[1\] admin user ID (`Integer`)
- \[2\] user restriction (`String`)

 Value: 210027

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager#addUserRestriction(android.content.ComponentName,%20kotlin.String)`

### TAG_USER_RESTRICTION_REMOVED

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TAG_USER_RESTRICTION_REMOVED: Int
```

Indicates that an admin has removed a user restriction. The log entry contains the following information about the event, encapsulated in an `https://developer.android.com/reference/kotlin/java/lang/Object.html#` array and accessible via `https://developer.android.com/reference/kotlin/android/app/admin/SecurityLog.SecurityEvent#getData()`:
- \[0\] admin package name (`String`)
- \[1\] admin user ID (`Integer`)
- \[2\] user restriction (`String`)

 Value: 210028

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager#clearUserRestriction(android.content.ComponentName,%20kotlin.String)`

### TAG_WIFI_CONNECTION

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TAG_WIFI_CONNECTION: Int
```

Indicates that an event occurred as the device attempted to connect to a managed WiFi network. The log entry contains the following information about the event, encapsulated in an `https://developer.android.com/reference/kotlin/java/lang/Object.html#` array and accessible via `https://developer.android.com/reference/kotlin/android/app/admin/SecurityLog.SecurityEvent#getData()`:
- \[0\] Last 2 octets of the network BSSID (`String`, in the form "xx:xx:xx:xx:AA:BB")
- \[1\] Type of event that occurred (`String`). Event types are CONNECTED, DISCONNECTED, ASSOCIATING, ASSOCIATED, EAP_METHOD_SELECTED, EAP_FAILURE, SSID_TEMP_DISABLED, and OPEN_SSL_FAILURE.
- \[2\] Optional human-readable failure reason, empty string if none (`String`)

 Value: 210037

### TAG_WIFI_DISCONNECTION

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TAG_WIFI_DISCONNECTION: Int
```

Indicates that the device disconnects from a managed WiFi network. The log entry contains the following information about the event, encapsulated in an `https://developer.android.com/reference/kotlin/java/lang/Object.html#` array and accessible via `https://developer.android.com/reference/kotlin/android/app/admin/SecurityLog.SecurityEvent#getData()`:
- \[0\] Last 2 octets of the network BSSID (`String`, in the form "xx:xx:xx:xx:AA:BB")
- \[1\] Optional human-readable disconnection reason, empty string if none (`String`)

 Value: 210038

### TAG_WIPE_FAILURE

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TAG_WIPE_FAILURE: Int
```

Indicates a failure to wipe device or user data. There is no extra payload in the log event.

 Value: 210023

## Public constructors

### SecurityLog

```
SecurityLog()
```
