Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AppOpsManager

```
open class AppOpsManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.app.AppOpsManager](AppOpsManager.md) |

App-ops are used for two purposes: Access control and tracking.

App-ops cover a wide variety of functionality from helping with runtime permissions access control and tracking to battery consumption tracking.

## Access control

App-ops can either be controlled for each uid or for each package. Which one is used depends on the API provider maintaining this app-op. For any security or privacy related app-op the provider needs to control the app-op for per uid as all security and privacy is based on uid in Android.

To control access the app-op can be set to a mode to:

`https://developer.android.com/reference/kotlin/android/app/AppOpsManager#MODE_DEFAULT:kotlin.Int`
: Default behavior, might differ from app-op or app-op

`https://developer.android.com/reference/kotlin/android/app/AppOpsManager#MODE_ALLOWED:kotlin.Int`
: Allow the access

`https://developer.android.com/reference/kotlin/android/app/AppOpsManager#MODE_IGNORED:kotlin.Int`
: Don't allow the access, i.e. don't perform the requested action or return no or placeholder data

`https://developer.android.com/reference/kotlin/android/app/AppOpsManager#MODE_ERRORED:kotlin.Int`
: Throw a `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#` on access. This can be suppressed by using a `...noThrow` method to check the mode

API providers need to check the mode returned by #noteOp if they are are allowing access to operations gated by the app-op. unsafeCheckOp should be used to check the mode if no access is granted. E.g. this can be used for displaying app-op state in the UI or when checking the state before later calling #noteOp anyway.

If an operation refers to a time span (e.g. a audio-recording session) the API provider should use #startOp and #finishOp instead of #noteOp.

### Runtime permissions and app-ops

Each platform defined runtime permission (beside background modifiers) has an associated app op which is used for tracking but also to allow for silent failures. I.e. if the runtime permission is denied the caller gets a `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#`, but if the permission is granted and the app-op is `https://developer.android.com/reference/kotlin/android/app/AppOpsManager#MODE_IGNORED:kotlin.Int` then the callers gets placeholder behavior, e.g. location callbacks would not happen.

### App-op permissions

App-ops permissions are platform defined permissions that can be overridden. The security check for app-op permissions should by `https://developer.android.com/reference/kotlin/android/app/AppOpsManager#MODE_DEFAULT:kotlin.Int` check the permission grant state. If the app-op state is set to `https://developer.android.com/reference/kotlin/android/app/AppOpsManager#MODE_ALLOWED:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/app/AppOpsManager#MODE_IGNORED:kotlin.Int` the app-op state should be checked instead of the permission grant state.

This functionality allows to grant access by default to apps fulfilling the requirements for a certain permission level. Still the behavior can be overridden when needed.

## Tracking

App-ops track many important events, including all accesses to runtime permission protected APIs. This is done by tracking when an app-op was #noteOp or #startOp. The tracked data can only be read by system components.

**Only #noteOp/#startOp are tracked; unsafeCheckOp is not tracked. Hence it is important to eventually call #noteOp or #startOp when providing access to protected operations or data.**

Some apps are forwarding access to other apps. E.g. an app might get the location from the system's location provider and then send the location further to a 3rd app. In this case the app passing on the data needs to call #noteProxyOp to signal the access proxying. This might also make sense inside of a single app if the access is forwarded between two parts of the tagged with different attribution tags.

An app can register an `https://developer.android.com/reference/kotlin/android/app/AppOpsManager.OnOpNotedCallback` to get informed about what accesses the system is tracking for it. As each runtime permission has an associated app-op this API is particularly useful for an app that want to find unexpected private data accesses.

## Summary

| Nested classes ||
|---|---|
| abstract | `https://developer.android.com/reference/kotlin/android/app/AppOpsManager.OnOpActiveChangedListener` Callback for notification of changes to operation active state. |
| abstract | `https://developer.android.com/reference/kotlin/android/app/AppOpsManager.OnOpChangedListener` Callback for notification of changes to operation state. |
| abstract | `https://developer.android.com/reference/kotlin/android/app/AppOpsManager.OnOpNotedCallback` Callback an app can #setOnOpNotedCallback to monitor the app-ops the system has tracked for it. |
| --- | --- |

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/AppOpsManager#MODE_ALLOWED:kotlin.Int` Result from #checkOp, #noteOp, #startOp: the given caller is allowed to perform the given operation. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/AppOpsManager#MODE_DEFAULT:kotlin.Int` Result from #checkOp, #noteOp, #startOp: the given caller should use its default security check. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/AppOpsManager#MODE_ERRORED:kotlin.Int` Result from #checkOpNoThrow, #noteOpNoThrow, #startOpNoThrow: the given caller is not allowed to perform the given operation, and this attempt should cause it to have a fatal error, typically a `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#`. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/AppOpsManager#MODE_FOREGROUND:kotlin.Int` Special mode that means "allow only when app is in foreground. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/AppOpsManager#MODE_IGNORED:kotlin.Int` Result from #checkOp, #noteOp, #startOp: the given caller is not allowed to perform the given operation, and this attempt should *silently fail* (it should not cause the app to crash). |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/AppOpsManager#OPSTR_ADD_VOICEMAIL:kotlin.String` Required to access phone state related information. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/AppOpsManager#OPSTR_ANSWER_PHONE_CALLS:kotlin.String` Answer incoming phone calls |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/AppOpsManager#OPSTR_BODY_SENSORS:kotlin.String` Access to body sensors such as heart rate, etc. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/AppOpsManager#OPSTR_CALL_PHONE:kotlin.String` Allows an application to initiate a phone call. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/AppOpsManager#OPSTR_CAMERA:kotlin.String` Required to be able to access the camera device. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/AppOpsManager#OPSTR_COARSE_LOCATION:kotlin.String` Access to coarse location information. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/AppOpsManager#OPSTR_FINE_LOCATION:kotlin.String` Access to fine location information. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/AppOpsManager#OPSTR_GET_USAGE_STATS:kotlin.String` Access to UsageStatsManager. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/AppOpsManager#OPSTR_MANAGE_CONTACTS:kotlin.String` Allows an application to manage the user's contacts data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/AppOpsManager#OPSTR_MOCK_LOCATION:kotlin.String` Inject mock location into the system. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/AppOpsManager#OPSTR_MONITOR_HIGH_POWER_LOCATION:kotlin.String` Continually monitoring location data with a relatively high power request. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/AppOpsManager#OPSTR_MONITOR_LOCATION:kotlin.String` Continually monitoring location data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/AppOpsManager#OPSTR_PICTURE_IN_PICTURE:kotlin.String` Access to picture-in-picture. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/AppOpsManager#OPSTR_PROCESS_OUTGOING_CALLS:kotlin.String` Access APIs for diverting outgoing calls |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/AppOpsManager#OPSTR_READ_CALENDAR:kotlin.String` Allows an application to read the user's calendar data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/AppOpsManager#OPSTR_READ_CALL_LOG:kotlin.String` Allows an application to read the user's call log. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/AppOpsManager#OPSTR_READ_CELL_BROADCASTS:kotlin.String` Read previously received cell broadcast messages. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/AppOpsManager#OPSTR_READ_CONTACTS:kotlin.String` Allows an application to read the user's contacts data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/AppOpsManager#OPSTR_READ_EXTERNAL_STORAGE:kotlin.String` Read external storage. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/AppOpsManager#OPSTR_READ_PHONE_NUMBERS:kotlin.String` <br /> |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/AppOpsManager#OPSTR_READ_PHONE_STATE:kotlin.String` Required to access phone state related information. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/AppOpsManager#OPSTR_READ_SMS:kotlin.String` Allows an application to read SMS messages. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/AppOpsManager#OPSTR_RECEIVE_MMS:kotlin.String` Allows an application to receive MMS messages. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/AppOpsManager#OPSTR_RECEIVE_SMS:kotlin.String` Allows an application to receive SMS messages. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/AppOpsManager#OPSTR_RECEIVE_WAP_PUSH:kotlin.String` Allows an application to receive WAP push messages. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/AppOpsManager#OPSTR_RECORD_AUDIO:kotlin.String` Required to be able to access the microphone device. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/AppOpsManager#OPSTR_SEND_SMS:kotlin.String` Allows an application to send SMS messages. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/AppOpsManager#OPSTR_SYSTEM_ALERT_WINDOW:kotlin.String` Required to draw on top of other apps. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/AppOpsManager#OPSTR_USE_FINGERPRINT:kotlin.String` Use the fingerprint API. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/AppOpsManager#OPSTR_USE_SIP:kotlin.String` Access APIs for SIP calling over VOIP or WiFi |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/AppOpsManager#OPSTR_WRITE_CALENDAR:kotlin.String` Allows an application to write to the user's calendar data. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/AppOpsManager#OPSTR_WRITE_CALL_LOG:kotlin.String` Allows an application to write to the user's call log. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/AppOpsManager#OPSTR_WRITE_CONTACTS:kotlin.String` Allows an application to write to the user's contacts data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/AppOpsManager#OPSTR_WRITE_EXTERNAL_STORAGE:kotlin.String` Write external storage. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/AppOpsManager#OPSTR_WRITE_SETTINGS:kotlin.String` Required to write/modify/update system settings. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/AppOpsManager#OP_NOTED_CALLBACK_FLAG_IGNORE_ASYNC:kotlin.Int` Ignores async op noted events. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/AppOpsManager#WATCH_FOREGROUND_CHANGES:kotlin.Int` Flag for startWatchingMode: Also get reports if the foreground state of an op's uid changes. |
| --- | --- |

| Public methods ||
|---|---|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | checkOp Check whether an application can perform an operation. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | checkOp Check whether an application can perform an operation. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | checkOpNoThrow Like checkOp but instead of throwing a `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#` it returns `https://developer.android.com/reference/kotlin/android/app/AppOpsManager#MODE_ERRORED:kotlin.Int`. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | checkOpNoThrow Like checkOp but instead of throwing a `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#` it returns `https://developer.android.com/reference/kotlin/android/app/AppOpsManager#MODE_ERRORED:kotlin.Int`. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | checkOpRawNoThrow Like checkOp but returns the *raw* mode associated with the op. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | checkPackage <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | finishOp <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | finishOp Report that an application is no longer performing an operation that had previously been started with startOp. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | finishProxyOp Report that an application is no longer performing an operation that had previously been started with startProxyOp. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isOpActive Checks whether the given op for a package is active, i. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | noteOp <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | noteOp Make note of an application performing an operation and check if the application is allowed to perform it. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | noteOpNoThrow <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | noteOpNoThrow Like noteOp but instead of throwing a `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#` it returns `https://developer.android.com/reference/kotlin/android/app/AppOpsManager#MODE_ERRORED:kotlin.Int`. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | noteProxyOp <br /> |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | noteProxyOp Make note of an application performing an operation on behalf of another application when handling an IPC. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | noteProxyOpNoThrow <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | noteProxyOpNoThrow <br /> |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | noteProxyOpNoThrow Like noteProxyOp but instead of throwing a `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#` it returns `https://developer.android.com/reference/kotlin/android/app/AppOpsManager#MODE_ERRORED:kotlin.Int`. |
| open static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | permissionToOp Gets the app-op name associated with a given permission. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setOnOpNotedCallback Set a new `https://developer.android.com/reference/kotlin/android/app/AppOpsManager.OnOpNotedCallback`. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setOnOpNotedCallback Set a new `https://developer.android.com/reference/kotlin/android/app/AppOpsManager.OnOpNotedCallback`. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | startOp <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | startOp Report that an application has started executing a long-running operation. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | startOpNoThrow <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | startOpNoThrow Like startOp but instead of throwing a `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#` it returns `https://developer.android.com/reference/kotlin/android/app/AppOpsManager#MODE_ERRORED:kotlin.Int`. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | startProxyOp Report that an application has started executing a long-running operation on behalf of another application when handling an IPC. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | startProxyOpNoThrow Like startProxyOp but instead of throwing a `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#` it returns `https://developer.android.com/reference/kotlin/android/app/AppOpsManager#MODE_ERRORED:kotlin.Int`. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | startWatchingActive Start watching for changes to the active state of app-ops. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | startWatchingMode Monitor for changes to the operating mode for the given op in the given app package. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | startWatchingMode Monitor for changes to the operating mode for the given op in the given app package. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | stopWatchingActive Stop watching for changes to the active state of an app-op. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | stopWatchingMode Stop monitoring that was previously started with #startWatchingMode. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | unsafeCheckOp Check whether an application might be able to perform an operation. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | unsafeCheckOpNoThrow Like unsafeCheckOp but instead of throwing a `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#` it returns `https://developer.android.com/reference/kotlin/android/app/AppOpsManager#MODE_ERRORED:kotlin.Int`. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | unsafeCheckOpRaw Like #checkOp but returns the *raw* mode associated with the op. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | unsafeCheckOpRawNoThrow Like #checkOp but returns the *raw* mode associated with the op. |

## Constants

### MODE_ALLOWED

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MODE_ALLOWED: Int
```

Result from #checkOp, #noteOp, #startOp: the given caller is allowed to perform the given operation.

 Value: 0

### MODE_DEFAULT

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MODE_DEFAULT: Int
```

Result from #checkOp, #noteOp, #startOp: the given caller should use its default security check. This mode is not normally used; it should only be used with appop permissions, and callers must explicitly check for it and deal with it.

 Value: 3

### MODE_ERRORED

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MODE_ERRORED: Int
```

Result from #checkOpNoThrow, #noteOpNoThrow, #startOpNoThrow: the given caller is not allowed to perform the given operation, and this attempt should cause it to have a fatal error, typically a `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#`.

 Value: 2

### MODE_FOREGROUND

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MODE_FOREGROUND: Int
```

Special mode that means "allow only when app is in foreground." This is **not** returned from unsafeCheckOp, #noteOp, #startOp. Rather, unsafeCheckOp will always return `https://developer.android.com/reference/kotlin/android/app/AppOpsManager#MODE_ALLOWED:kotlin.Int` (because it is always possible for it to be ultimately allowed, depending on the app's background state), and #noteOp and #startOp will return `https://developer.android.com/reference/kotlin/android/app/AppOpsManager#MODE_ALLOWED:kotlin.Int` when the app being checked is currently in the foreground, otherwise `https://developer.android.com/reference/kotlin/android/app/AppOpsManager#MODE_IGNORED:kotlin.Int`.

The only place you will this normally see this value is through unsafeCheckOpRaw, which returns the actual raw mode of the op. Note that because you can't know the current state of the app being checked (and it can change at any point), you can only treat the result here as an indication that it will vary between `https://developer.android.com/reference/kotlin/android/app/AppOpsManager#MODE_ALLOWED:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/app/AppOpsManager#MODE_IGNORED:kotlin.Int` depending on changes in the background state of the app. You thus must always use #noteOp or #startOp to do the actual check for access to the op.

 Value: 4

### MODE_IGNORED

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MODE_IGNORED: Int
```

Result from #checkOp, #noteOp, #startOp: the given caller is not allowed to perform the given operation, and this attempt should *silently fail* (it should not cause the app to crash).

 Value: 1

### OPSTR_ADD_VOICEMAIL

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val OPSTR_ADD_VOICEMAIL: String
```

Required to access phone state related information.

 Value: "android:add_voicemail"

### OPSTR_ANSWER_PHONE_CALLS

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val OPSTR_ANSWER_PHONE_CALLS: String
```

Answer incoming phone calls

 Value: "android:answer_phone_calls"

### OPSTR_BODY_SENSORS

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val OPSTR_BODY_SENSORS: String
```

Access to body sensors such as heart rate, etc.

 Value: "android:body_sensors"

### OPSTR_CALL_PHONE

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val OPSTR_CALL_PHONE: String
```

Allows an application to initiate a phone call.

 Value: "android:call_phone"

### OPSTR_CAMERA

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val OPSTR_CAMERA: String
```

Required to be able to access the camera device.

 Value: "android:camera"

### OPSTR_COARSE_LOCATION

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val OPSTR_COARSE_LOCATION: String
```

Access to coarse location information.

 Value: "android:coarse_location"

### OPSTR_FINE_LOCATION

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val OPSTR_FINE_LOCATION: String
```

Access to fine location information.

 Value: "android:fine_location"

### OPSTR_GET_USAGE_STATS

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val OPSTR_GET_USAGE_STATS: String
```

Access to UsageStatsManager.

 Value: "android:get_usage_stats"

### OPSTR_MANAGE_CONTACTS

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val OPSTR_MANAGE_CONTACTS: String
```

Allows an application to manage the user's contacts data.

 Value: "android:manage_contacts"

### OPSTR_MOCK_LOCATION

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val OPSTR_MOCK_LOCATION: String
```

Inject mock location into the system.

 Value: "android:mock_location"

### OPSTR_MONITOR_HIGH_POWER_LOCATION

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val OPSTR_MONITOR_HIGH_POWER_LOCATION: String
```

Continually monitoring location data with a relatively high power request.

 Value: "android:monitor_location_high_power"

### OPSTR_MONITOR_LOCATION

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val OPSTR_MONITOR_LOCATION: String
```

Continually monitoring location data.

 Value: "android:monitor_location"

### OPSTR_PICTURE_IN_PICTURE

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val OPSTR_PICTURE_IN_PICTURE: String
```

Access to picture-in-picture.

 Value: "android:picture_in_picture"

### OPSTR_PROCESS_OUTGOING_CALLS

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val OPSTR_PROCESS_OUTGOING_CALLS: String
```

Access APIs for diverting outgoing calls

 Value: "android:process_outgoing_calls"

### OPSTR_READ_CALENDAR

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val OPSTR_READ_CALENDAR: String
```

Allows an application to read the user's calendar data.

 Value: "android:read_calendar"

### OPSTR_READ_CALL_LOG

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val OPSTR_READ_CALL_LOG: String
```

Allows an application to read the user's call log.

 Value: "android:read_call_log"

### OPSTR_READ_CELL_BROADCASTS

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val OPSTR_READ_CELL_BROADCASTS: String
```

Read previously received cell broadcast messages.

 Value: "android:read_cell_broadcasts"

### OPSTR_READ_CONTACTS

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val OPSTR_READ_CONTACTS: String
```

Allows an application to read the user's contacts data.

 Value: "android:read_contacts"

### OPSTR_READ_EXTERNAL_STORAGE

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val OPSTR_READ_EXTERNAL_STORAGE: String
```

Read external storage.

 Value: "android:read_external_storage"

### OPSTR_READ_PHONE_NUMBERS

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val OPSTR_READ_PHONE_NUMBERS: String
```

 Value: "android:read_phone_numbers"

### OPSTR_READ_PHONE_STATE

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val OPSTR_READ_PHONE_STATE: String
```

Required to access phone state related information.

 Value: "android:read_phone_state"

### OPSTR_READ_SMS

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val OPSTR_READ_SMS: String
```

Allows an application to read SMS messages.

 Value: "android:read_sms"

### OPSTR_RECEIVE_MMS

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val OPSTR_RECEIVE_MMS: String
```

Allows an application to receive MMS messages.

 Value: "android:receive_mms"

### OPSTR_RECEIVE_SMS

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val OPSTR_RECEIVE_SMS: String
```

Allows an application to receive SMS messages.

 Value: "android:receive_sms"

### OPSTR_RECEIVE_WAP_PUSH

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val OPSTR_RECEIVE_WAP_PUSH: String
```

Allows an application to receive WAP push messages.

 Value: "android:receive_wap_push"

### OPSTR_RECORD_AUDIO

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val OPSTR_RECORD_AUDIO: String
```

Required to be able to access the microphone device.

 Value: "android:record_audio"

### OPSTR_SEND_SMS

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val OPSTR_SEND_SMS: String
```

Allows an application to send SMS messages.

 Value: "android:send_sms"

### OPSTR_SYSTEM_ALERT_WINDOW

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val OPSTR_SYSTEM_ALERT_WINDOW: String
```

Required to draw on top of other apps.

 Value: "android:system_alert_window"

### OPSTR_USE_FINGERPRINT

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val OPSTR_USE_FINGERPRINT: String
```

Use the fingerprint API.

 Value: "android:use_fingerprint"

### OPSTR_USE_SIP

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val OPSTR_USE_SIP: String
```

Access APIs for SIP calling over VOIP or WiFi

 Value: "android:use_sip"

### OPSTR_WRITE_CALENDAR

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val OPSTR_WRITE_CALENDAR: String
```

Allows an application to write to the user's calendar data.

 Value: "android:write_calendar"

### OPSTR_WRITE_CALL_LOG

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val OPSTR_WRITE_CALL_LOG: String
```

Allows an application to write to the user's call log.

 Value: "android:write_call_log"

### OPSTR_WRITE_CONTACTS

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val OPSTR_WRITE_CONTACTS: String
```

Allows an application to write to the user's contacts data.

 Value: "android:write_contacts"

### OPSTR_WRITE_EXTERNAL_STORAGE

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val OPSTR_WRITE_EXTERNAL_STORAGE: String
```

Write external storage.

 Value: "android:write_external_storage"

### OPSTR_WRITE_SETTINGS

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val OPSTR_WRITE_SETTINGS: String
```

Required to write/modify/update system settings.

 Value: "android:write_settings"

### OP_NOTED_CALLBACK_FLAG_IGNORE_ASYNC

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val OP_NOTED_CALLBACK_FLAG_IGNORE_ASYNC: Int
```

Ignores async op noted events.

 Value: 1

**See Also**

### WATCH_FOREGROUND_CHANGES

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val WATCH_FOREGROUND_CHANGES: Int
```

Flag for startWatchingMode: Also get reports if the foreground state of an op's uid changes. This only works when watching a particular op, not when watching a package.

 Value: 1

## Public methods

### checkOp

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun checkOp(
    op: String, 
    uid: Int, 
    packageName: String
): Int
```

Check whether an application can perform an operation.

For platform versions before `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#BAKLAVA:kotlin.Int`, this is *not* a security check; you must use noteOp or startOp for your actual security checks. This function can just be used for a quick check to see if an operation has been disabled for the application, as an early reject of some work.

For platform versions equal to or after `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#BAKLAVA:kotlin.Int`, it does the same security check as noteOp and startOp, and should be preferred to use.

This API does not modify the time stamp or other data about the operation.

| Parameters ||
|---|---|
| `op` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The operation to check. One of the OPSTR_\* constants. This value cannot be `null`. |
| `uid` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The uid of the application attempting to perform the operation. |
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The name of the application attempting to perform the operation. This value cannot be `null`. |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Returns `https://developer.android.com/reference/kotlin/android/app/AppOpsManager#MODE_ALLOWED:kotlin.Int` if the operation is allowed, or `https://developer.android.com/reference/kotlin/android/app/AppOpsManager#MODE_IGNORED:kotlin.Int` if it is not allowed and should be silently ignored (without causing the app to crash). |

| Exceptions ||
|---|---|
| `java.lang.SecurityException` | If the app has been configured to crash on this op. |

### checkOp

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun checkOp(
    op: String, 
    uid: Int, 
    packageName: String, 
    attributionTag: String?
): Int
```

Check whether an application can perform an operation. It does the same security check as noteOp and startOp, but does not modify the time stamp or other data about the operation.

| Parameters ||
|---|---|
| `op` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The operation to check. One of the OPSTR_\* constants. This value cannot be `null`. |
| `uid` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The uid of the application attempting to perform the operation. |
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The name of the application attempting to perform the operation. This value cannot be `null`. |
| --- | --- |
| `attributionTag` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: The createAttributionContext of the calling context or `null` for default attribution |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Returns `https://developer.android.com/reference/kotlin/android/app/AppOpsManager#MODE_ALLOWED:kotlin.Int` if the operation is allowed, or `https://developer.android.com/reference/kotlin/android/app/AppOpsManager#MODE_IGNORED:kotlin.Int` if it is not allowed and should be silently ignored (without causing the app to crash). |

| Exceptions ||
|---|---|
| `java.lang.SecurityException` | If the app has been configured to crash on this op. |

### checkOpNoThrow

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun checkOpNoThrow(
    op: String, 
    uid: Int, 
    packageName: String
): Int
```

Like checkOp but instead of throwing a `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#` it returns `https://developer.android.com/reference/kotlin/android/app/AppOpsManager#MODE_ERRORED:kotlin.Int`.

| Parameters ||
|---|---|
| `op` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |

### checkOpNoThrow

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun checkOpNoThrow(
    op: String, 
    uid: Int, 
    packageName: String, 
    attributionTag: String?
): Int
```

Like checkOp but instead of throwing a `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#` it returns `https://developer.android.com/reference/kotlin/android/app/AppOpsManager#MODE_ERRORED:kotlin.Int`.

| Parameters ||
|---|---|
| `op` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |
| `attributionTag` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: This value may be `null`. |
| --- | --- |

### checkOpRawNoThrow

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun checkOpRawNoThrow(
    op: String, 
    uid: Int, 
    packageName: String, 
    attributionTag: String?
): Int
```

Like checkOp but returns the *raw* mode associated with the op. Does not throw a security exception, does not translate `https://developer.android.com/reference/kotlin/android/app/AppOpsManager#MODE_FOREGROUND:kotlin.Int`.

| Parameters ||
|---|---|
| `op` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |
| `attributionTag` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: This value may be `null`. |
| --- | --- |

### checkPackage

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun checkPackage(
    uid: Int, 
    packageName: String
): Unit
```

**Deprecated:** *Use android.content.pm.PackageManager#getPackageUid instead*

| Parameters ||
|---|---|
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |

### finishOp

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun finishOp(
    op: String, 
    uid: Int, 
    packageName: String
): Unit
```

**Deprecated:** *Use finishOp instead*

| Parameters ||
|---|---|
| `op` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |

### finishOp

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun finishOp(
    op: String, 
    uid: Int, 
    packageName: String, 
    attributionTag: String?
): Unit
```

Report that an application is no longer performing an operation that had previously been started with startOp. There is no validation of input or result; the parameters supplied here must be the exact same ones previously passed in when starting the operation.

| Parameters ||
|---|---|
| `op` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |
| `attributionTag` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: This value may be `null`. |
| --- | --- |

### finishProxyOp

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun finishProxyOp(
    op: String, 
    proxiedUid: Int, 
    proxiedPackageName: String, 
    proxiedAttributionTag: String?
): Unit
```

Report that an application is no longer performing an operation that had previously been started with startProxyOp. There is no validation of input or result; the parameters supplied here must be the exact same ones previously passed in when starting the operation.

| Parameters ||
|---|---|
| `op` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The operation which was started. This value cannot be `null`. |
| `proxiedUid` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The proxied appp's UID |
| `proxiedPackageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The proxied appp's package name. This value cannot be `null`. |
| --- | --- |
| `proxiedAttributionTag` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: The proxied appp's attribution tag or `null` for default attribution |

### isOpActive

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isOpActive(
    op: String, 
    uid: Int, 
    packageName: String
): Boolean
```

Checks whether the given op for a package is active, i.e. did someone call #startOp without #finishOp yet.

If you don't hold the `android.Manifest.permission#WATCH_APPOPS` permission you can query only for your UID.

| Parameters ||
|---|---|
| `op` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |

**See Also**

- finishOp
- startOp

### noteOp

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun noteOp(
    op: String, 
    uid: Int, 
    packageName: String
): Int
```

**Deprecated:** *Use noteOp instead*

| Parameters ||
|---|---|
| `op` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |

### noteOp

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun noteOp(
    op: String, 
    uid: Int, 
    packageName: String?, 
    attributionTag: String?, 
    message: String?
): Int
```

Make note of an application performing an operation and check if the application is allowed to perform it.

If this is a check that is not preceding the protected operation, use unsafeCheckOp instead.

The identity of the package the app-op is noted for is specified by the `uid` and `packageName` parameters. If this is noted for a regular app both should be set and the package needs to be part of the uid. In the very rare case that an app-op is noted for an entity that does not have a package name, the package can be `null`. As it is possible that a single process contains more than one package the `packageName` should be getPackageName from the context of the caller of the API (in the app process) that eventually triggers this check. If this op is not noted for a running process the `packageName` cannot be read from the context, but it should be clear which package the note is for.

If the `uid` and `packageName` do not match this return `https://developer.android.com/reference/kotlin/android/app/AppOpsManager#MODE_IGNORED:kotlin.Int`.

Beside the access check this method also records the access. While the access check is based on `uid` and/or `packageName` the access recording is done based on the `packageName` and `attributionTag`. The `attributionTag` should be getAttributionTag from the same context the package name is read from. In the case the check is not related to an API call, the `attributionTag` should be `null`. Please note that e.g. registering a callback for later is still an API call and the code should store the attribution tag along the package name for being used in this method later.

The `message` parameter only needs to be set when this method is

not

called in a two-way binder call from the client. In this case the message is a free form text that is meant help the app developer determine what part of the app's code triggered the note. This message is passed back to the app in the onAsyncNoted callback. A good example of a useful message is including the identityHashCode of the listener that will receive data or the name of the manifest-receiver.

| Parameters ||
|---|---|
| `op` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The operation to note. One of the OPSTR_\* constants. This value cannot be `null`. |
| `uid` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The uid of the application attempting to perform the operation. |
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: The name of the application attempting to perform the operation. This value may be `null`. |
| --- | --- |
| `attributionTag` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: The createAttributionContext of the calling context or `null` for default attribution |
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: A message describing why the op was noted. This value may be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Returns `https://developer.android.com/reference/kotlin/android/app/AppOpsManager#MODE_ALLOWED:kotlin.Int` if the operation is allowed, or `https://developer.android.com/reference/kotlin/android/app/AppOpsManager#MODE_IGNORED:kotlin.Int` if it is not allowed and should be silently ignored (without causing the app to crash). |

| Exceptions ||
|---|---|
| `java.lang.SecurityException` | If the app has been configured to crash on this op. |

### noteOpNoThrow

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun noteOpNoThrow(
    op: String, 
    uid: Int, 
    packageName: String
): Int
```

**Deprecated:** *Use noteOpNoThrow instead*

| Parameters ||
|---|---|
| `op` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |

### noteOpNoThrow

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun noteOpNoThrow(
    op: String, 
    uid: Int, 
    packageName: String, 
    attributionTag: String?, 
    message: String?
): Int
```

Like noteOp but instead of throwing a `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#` it returns `https://developer.android.com/reference/kotlin/android/app/AppOpsManager#MODE_ERRORED:kotlin.Int`.

| Parameters ||
|---|---|
| `op` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |
| `attributionTag` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: This value may be `null`. |
| --- | --- |
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: This value may be `null`. |

**See Also**

- noteOp

### noteProxyOp

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun noteProxyOp(
    op: String, 
    proxiedPackageName: String
): Int
```

**Deprecated:** *Use noteProxyOp instead*

| Parameters ||
|---|---|
| `op` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |
| `proxiedPackageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |

### noteProxyOp

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun noteProxyOp(
    op: String, 
    proxiedPackageName: String?, 
    proxiedUid: Int, 
    proxiedAttributionTag: String?, 
    message: String?
): Int
```

Make note of an application performing an operation on behalf of another application when handling an IPC. This function will verify that the calling uid and proxied package name match, and if not, return `https://developer.android.com/reference/kotlin/android/app/AppOpsManager#MODE_IGNORED:kotlin.Int`. If this call succeeds, the last execution time of the operation for the proxied app and your app will be updated to the current time.

| Parameters ||
|---|---|
| `op` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The operation to note. One of the OPSTR_\* constants. This value cannot be `null`. |
| `proxiedPackageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: The name of the application calling into the proxy application. This value may be `null`. |
| `proxiedUid` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The uid of the proxied application |
| --- | --- |
| `proxiedAttributionTag` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: The proxied createAttributionContext or `null` for default attribution |
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: A message describing the reason the op was noted. This value may be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Returns `https://developer.android.com/reference/kotlin/android/app/AppOpsManager#MODE_ALLOWED:kotlin.Int` if the operation is allowed, or `https://developer.android.com/reference/kotlin/android/app/AppOpsManager#MODE_IGNORED:kotlin.Int` if it is not allowed and should be silently ignored (without causing the app to crash). |

| Exceptions ||
|---|---|
| `java.lang.SecurityException` | If the proxy or proxied app has been configured to crash on this op. |

### noteProxyOpNoThrow

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun noteProxyOpNoThrow(
    op: String, 
    proxiedPackageName: String
): Int
```

**Deprecated:** *Use noteProxyOpNoThrow instead*

| Parameters ||
|---|---|
| `op` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |
| `proxiedPackageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |

### noteProxyOpNoThrow

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun noteProxyOpNoThrow(
    op: String, 
    proxiedPackageName: String?, 
    proxiedUid: Int
): Int
```

**Deprecated:** *Use noteProxyOpNoThrow instead*

| Parameters ||
|---|---|
| `op` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |
| `proxiedPackageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: This value may be `null`. |

### noteProxyOpNoThrow

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun noteProxyOpNoThrow(
    op: String, 
    proxiedPackageName: String?, 
    proxiedUid: Int, 
    proxiedAttributionTag: String?, 
    message: String?
): Int
```

Like noteProxyOp but instead of throwing a `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#` it returns `https://developer.android.com/reference/kotlin/android/app/AppOpsManager#MODE_ERRORED:kotlin.Int`.

| Parameters ||
|---|---|
| `op` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |
| `proxiedPackageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: This value may be `null`. |
| `proxiedAttributionTag` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: This value may be `null`. |
| --- | --- |
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: This value may be `null`. |

**See Also**

- noteOpNoThrow

### permissionToOp

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun permissionToOp(permission: String): String?
```

Gets the app-op name associated with a given permission.

The app-op name is one of the public constants defined in this class such as `https://developer.android.com/reference/kotlin/android/app/AppOpsManager#OPSTR_COARSE_LOCATION:kotlin.String`. This API is intended to be used for mapping runtime permissions to the corresponding app-op.

| Parameters ||
|---|---|
| `permission` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The permission. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?` | The app-op associated with the permission or `null`. |

### setOnOpNotedCallback

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setOnOpNotedCallback(
    asyncExecutor: Executor?, 
    callback: AppOpsManager.OnOpNotedCallback?
): Unit
```

Set a new `https://developer.android.com/reference/kotlin/android/app/AppOpsManager.OnOpNotedCallback`.

There can only ever be one collector per process. If there currently is another callback set, this will fail.

Note that if an app has multiple processes registering for this callback, the system would fan out async op noted callbacks to each of the processes, resulting in the same data being delivered multiple times to an app, which is usually undesired. To avoid this, consider listening to async ops only in one process. See setOnOpNotedCallback for how to do this.

| Parameters ||
|---|---|
| `asyncExecutor` | [Executor](../java.util.concurrent/Executor.md)?: executor to execute onAsyncNoted on, `null` to unset. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use getMainExecutor. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `callback` | [AppOpsManager.OnOpNotedCallback](../android/app/AppOpsManager.OnOpNotedCallback.md)?: listener to set, `null` to unset |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | If another callback is already registered |

### setOnOpNotedCallback

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setOnOpNotedCallback(
    asyncExecutor: Executor?, 
    callback: AppOpsManager.OnOpNotedCallback?, 
    flags: Int
): Unit
```

Set a new `https://developer.android.com/reference/kotlin/android/app/AppOpsManager.OnOpNotedCallback`.

There can only ever be one collector per process. If there currently is another callback set, this will fail.

This API allows the caller to listen only to sync and self op noted events, and ignore async ops. This is useful in the scenario where an app has multiple processes. Consider an example where an app has two processes, A and B. The op noted events are as follows:

- op 1: process A, sync
- op 2: process A, async
- op 3: process B, sync
- op 4: process B, async Any process that listens to async op noted events gets events originating from across ALL processes (op 2 and op 4 in this example). So if both process A and B register as listeners, both of them get op 2 and 4 which is not ideal. To avoid duplicates, one of the two processes should set `https://developer.android.com/reference/kotlin/android/app/AppOpsManager#OP_NOTED_CALLBACK_FLAG_IGNORE_ASYNC:kotlin.Int`. For example process A sets `https://developer.android.com/reference/kotlin/android/app/AppOpsManager#OP_NOTED_CALLBACK_FLAG_IGNORE_ASYNC:kotlin.Int` and would then only get its own sync event (op 1). The other process would then listen to all types of events and get op 2, 3 and 4. Note that even with `https://developer.android.com/reference/kotlin/android/app/AppOpsManager#OP_NOTED_CALLBACK_FLAG_IGNORE_ASYNC:kotlin.Int`, onAsyncNoted may still be invoked. This happens for sync events that were collected before a callback is registered.

| Parameters ||
|---|---|
| `asyncExecutor` | [Executor](../java.util.concurrent/Executor.md)?: executor to execute onAsyncNoted on, `null` to unset. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use getMainExecutor. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `callback` | [AppOpsManager.OnOpNotedCallback](../android/app/AppOpsManager.OnOpNotedCallback.md)?: listener to set, `null` to unset |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): additional flags to modify the callback behavior, such as `https://developer.android.com/reference/kotlin/android/app/AppOpsManager#OP_NOTED_CALLBACK_FLAG_IGNORE_ASYNC:kotlin.Int` Value is either `0` or - `https://developer.android.com/reference/kotlin/android/app/AppOpsManager#OP_NOTED_CALLBACK_FLAG_IGNORE_ASYNC:kotlin.Int` |
| --- | --- |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | If another callback is already registered |

### startOp

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun startOp(
    op: String, 
    uid: Int, 
    packageName: String
): Int
```

**Deprecated:** *use startOp instead*

| Parameters ||
|---|---|
| `op` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |

### startOp

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun startOp(
    op: String, 
    uid: Int, 
    packageName: String?, 
    attributionTag: String?, 
    message: String?
): Int
```

Report that an application has started executing a long-running operation.

For more details how to determine the `callingPackageName`, `callingAttributionTag`, and `message`, please check the description in noteOp

| Parameters ||
|---|---|
| `op` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The operation to start. One of the OPSTR_\* constants. This value cannot be `null`. |
| `uid` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The user id of the application attempting to perform the operation. |
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: The name of the application attempting to perform the operation. This value may be `null`. |
| --- | --- |
| `attributionTag` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: The createAttributionContext or `null` for default attribution |
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: Description why op was started. This value may be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Returns `https://developer.android.com/reference/kotlin/android/app/AppOpsManager#MODE_ALLOWED:kotlin.Int` if the operation is allowed, or `https://developer.android.com/reference/kotlin/android/app/AppOpsManager#MODE_IGNORED:kotlin.Int` if it is not allowed and should be silently ignored (without causing the app to crash). |

| Exceptions ||
|---|---|
| `java.lang.SecurityException` | If the app has been configured to crash on this op or the package is not in the passed in UID. |

### startOpNoThrow

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun startOpNoThrow(
    op: String, 
    uid: Int, 
    packageName: String
): Int
```

**Deprecated:** *use startOpNoThrow instead*

| Parameters ||
|---|---|
| `op` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |

### startOpNoThrow

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun startOpNoThrow(
    op: String, 
    uid: Int, 
    packageName: String, 
    attributionTag: String?, 
    message: String?
): Int
```

Like startOp but instead of throwing a `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#` it returns `https://developer.android.com/reference/kotlin/android/app/AppOpsManager#MODE_ERRORED:kotlin.Int`.

| Parameters ||
|---|---|
| `op` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |
| `attributionTag` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: This value may be `null`. |
| --- | --- |
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: This value may be `null`. |

**See Also**

- startOp

### startProxyOp

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun startProxyOp(
    op: String, 
    proxiedUid: Int, 
    proxiedPackageName: String, 
    proxiedAttributionTag: String?, 
    message: String?
): Int
```

Report that an application has started executing a long-running operation on behalf of another application when handling an IPC. This function will verify that the calling uid and proxied package name match, and if not, return `https://developer.android.com/reference/kotlin/android/app/AppOpsManager#MODE_IGNORED:kotlin.Int`.

| Parameters ||
|---|---|
| `op` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The op to note. This value cannot be `null`. |
| `proxiedUid` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The uid to note the op for `null` |
| `proxiedPackageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The package name the uid belongs to. This value cannot be `null`. |
| --- | --- |
| `proxiedAttributionTag` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: The proxied createAttributionContext or `null` for default attribution |
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: A message describing the reason the op was noted. This value may be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Returns `https://developer.android.com/reference/kotlin/android/app/AppOpsManager#MODE_ALLOWED:kotlin.Int` if the operation is allowed, or `https://developer.android.com/reference/kotlin/android/app/AppOpsManager#MODE_IGNORED:kotlin.Int` if it is not allowed and should be silently ignored (without causing the app to crash). |

| Exceptions ||
|---|---|
| `java.lang.SecurityException` | If the proxy or proxied app has been configured to crash on this op. |

### startProxyOpNoThrow

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun startProxyOpNoThrow(
    op: String, 
    proxiedUid: Int, 
    proxiedPackageName: String, 
    proxiedAttributionTag: String?, 
    message: String?
): Int
```

Like startProxyOp but instead of throwing a `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#` it returns `https://developer.android.com/reference/kotlin/android/app/AppOpsManager#MODE_ERRORED:kotlin.Int`.

| Parameters ||
|---|---|
| `op` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |
| `proxiedPackageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |
| `proxiedAttributionTag` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: This value may be `null`. |
| --- | --- |
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: This value may be `null`. |

**See Also**

- startProxyOp

### startWatchingActive

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun startWatchingActive(
    ops: Array<String!>, 
    executor: Executor, 
    callback: AppOpsManager.OnOpActiveChangedListener
): Unit
```

Start watching for changes to the active state of app-ops. An app-op may be long running and it has a clear start and stop delimiters. If an op is being started or stopped by any package you will get a callback. To change the watched ops for a registered callback you need to unregister and register it again.

If you don't hold the `android.Manifest.permission#WATCH_APPOPS` permission you can watch changes only for your UID.

| Parameters ||
|---|---|
| `ops` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>: The operations to watch. This value cannot be `null`. |
| `executor` | [Executor](../java.util.concurrent/Executor.md): Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use getMainExecutor. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. This value cannot be `null`. |
| `callback` | [AppOpsManager.OnOpActiveChangedListener](../android/app/AppOpsManager.OnOpActiveChangedListener.md): Where to report changes. This value cannot be `null`. |
| --- | --- |

**See Also**

- stopWatchingActive

### startWatchingMode

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun startWatchingMode(
    op: String, 
    packageName: String?, 
    callback: AppOpsManager.OnOpChangedListener
): Unit
```

Monitor for changes to the operating mode for the given op in the given app package. You can watch op changes only for your UID.

| Parameters ||
|---|---|
| `op` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The operation to monitor, one of OPSTR_\*. This value cannot be `null`. |
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: The name of the application to monitor. This value may be `null`. |
| `callback` | [AppOpsManager.OnOpChangedListener](../android/app/AppOpsManager.OnOpChangedListener.md): Where to report changes. This value cannot be `null`. |
| --- | --- |

### startWatchingMode

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun startWatchingMode(
    op: String, 
    packageName: String?, 
    flags: Int, 
    callback: AppOpsManager.OnOpChangedListener
): Unit
```

Monitor for changes to the operating mode for the given op in the given app package. You can watch op changes only for your UID.

| Parameters ||
|---|---|
| `op` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The operation to monitor, one of OPSTR_\*. This value cannot be `null`. |
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: The name of the application to monitor. This value may be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Option flags: any combination of `https://developer.android.com/reference/kotlin/android/app/AppOpsManager#WATCH_FOREGROUND_CHANGES:kotlin.Int` or 0. |
| --- | --- |
| `callback` | [AppOpsManager.OnOpChangedListener](../android/app/AppOpsManager.OnOpChangedListener.md): Where to report changes. This value cannot be `null`. |

### stopWatchingActive

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun stopWatchingActive(callback: AppOpsManager.OnOpActiveChangedListener): Unit
```

Stop watching for changes to the active state of an app-op. An app-op may be long running and it has a clear start and stop delimiters. Unregistering a non-registered callback has no effect.

| Parameters ||
|---|---|
| `callback` | [AppOpsManager.OnOpActiveChangedListener](../android/app/AppOpsManager.OnOpActiveChangedListener.md): This value cannot be `null`. |

**See Also**

- startWatchingActive

### stopWatchingMode

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun stopWatchingMode(callback: AppOpsManager.OnOpChangedListener): Unit
```

Stop monitoring that was previously started with #startWatchingMode. All monitoring associated with this callback will be removed.

| Parameters ||
|---|---|
| `callback` | [AppOpsManager.OnOpChangedListener](../android/app/AppOpsManager.OnOpChangedListener.md): This value cannot be `null`. |

### unsafeCheckOp

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun unsafeCheckOp(
    op: String, 
    uid: Int, 
    packageName: String
): Int
```

**Deprecated:** *Use checkOp*

Check whether an application might be able to perform an operation.

For platform versions before `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#BAKLAVA:kotlin.Int`, this is *not* a security check; you must use noteOp or startOp for your actual security checks. This function can just be used for a quick check to see if an operation has been disabled for the application, as an early reject of some work.

For platform versions equal to or after `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#BAKLAVA:kotlin.Int`, this is no longer an unsafe check, and it does the same security check as noteOp and startOp. However, it's preferred to use checkOp, since the word "unsafe" in the name of this API is no longer accurate.

This API does not modify the time stamp or other data about the operation.

| Parameters ||
|---|---|
| `op` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The operation to check. One of the OPSTR_\* constants. This value cannot be `null`. |
| `uid` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The user id of the application attempting to perform the operation. |
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The name of the application attempting to perform the operation. This value cannot be `null`. |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Returns `https://developer.android.com/reference/kotlin/android/app/AppOpsManager#MODE_ALLOWED:kotlin.Int` if the operation is allowed, or `https://developer.android.com/reference/kotlin/android/app/AppOpsManager#MODE_IGNORED:kotlin.Int` if it is not allowed and should be silently ignored (without causing the app to crash). |

| Exceptions ||
|---|---|
| `java.lang.SecurityException` | If the app has been configured to crash on this op. |

### unsafeCheckOpNoThrow

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun unsafeCheckOpNoThrow(
    op: String, 
    uid: Int, 
    packageName: String
): Int
```

**Deprecated:** *Use checkOpNoThrow*

Like unsafeCheckOp but instead of throwing a `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#` it returns `https://developer.android.com/reference/kotlin/android/app/AppOpsManager#MODE_ERRORED:kotlin.Int`.

| Parameters ||
|---|---|
| `op` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |

### unsafeCheckOpRaw

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun unsafeCheckOpRaw(
    op: String, 
    uid: Int, 
    packageName: String
): Int
```

**Deprecated:** *Use checkOpRawNoThrow instead*

Like #checkOp but returns the *raw* mode associated with the op. Does not throw a security exception, does not translate `https://developer.android.com/reference/kotlin/android/app/AppOpsManager#MODE_FOREGROUND:kotlin.Int`.

| Parameters ||
|---|---|
| `op` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |

### unsafeCheckOpRawNoThrow

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun unsafeCheckOpRawNoThrow(
    op: String, 
    uid: Int, 
    packageName: String
): Int
```

**Deprecated:** *Use checkOpRawNoThrow instead*

Like #checkOp but returns the *raw* mode associated with the op. Does not throw a security exception, does not translate `https://developer.android.com/reference/kotlin/android/app/AppOpsManager#MODE_FOREGROUND:kotlin.Int`.

| Parameters ||
|---|---|
| `op` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |
