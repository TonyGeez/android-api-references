Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# StatusBarManager

```
open class StatusBarManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.app.StatusBarManager](StatusBarManager.md) |

Allows an app to control the status bar.

## Summary

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/StatusBarManager#SHOW_POWER_MENU_RESULT_DISABLED:kotlin.Int` Result returned in a callback when a call to showPowerMenu cannot be completed due to the Power Menu being currently disabled. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/StatusBarManager#SHOW_POWER_MENU_RESULT_SHOWING:kotlin.Int` Result returned in a callback when a call to showPowerMenu has succeeded and the Power Menu is currently showing. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/StatusBarManager#SHOW_POWER_MENU_RESULT_UNKNOWN:kotlin.Int` Unknwown result of calling showPowerMenu. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/StatusBarManager#TILE_ADD_REQUEST_ERROR_APP_NOT_IN_FOREGROUND:kotlin.Int` Indicates that the requesting application is not in the foreground. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/StatusBarManager#TILE_ADD_REQUEST_ERROR_BAD_COMPONENT:kotlin.Int` Indicates that the component does not match an enabled exported `https://developer.android.com/reference/kotlin/android/service/quicksettings/TileService.html#` for the current user. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/StatusBarManager#TILE_ADD_REQUEST_ERROR_MISMATCHED_PACKAGE:kotlin.Int` Indicates that this package does not match that of the `https://developer.android.com/reference/kotlin/android/service/quicksettings/TileService.html#`. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/StatusBarManager#TILE_ADD_REQUEST_ERROR_NOT_CURRENT_USER:kotlin.Int` Indicates that the user is not the current user. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/StatusBarManager#TILE_ADD_REQUEST_ERROR_NO_STATUS_BAR_SERVICE:kotlin.Int` The request could not be processed because no fulfilling service was found. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/StatusBarManager#TILE_ADD_REQUEST_ERROR_REQUEST_IN_PROGRESS:kotlin.Int` Indicates that there's a request in progress for this package. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/StatusBarManager#TILE_ADD_REQUEST_RESULT_TILE_ADDED:kotlin.Int` Response indicating that the tile was added. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/StatusBarManager#TILE_ADD_REQUEST_RESULT_TILE_ALREADY_ADDED:kotlin.Int` Response indicating that the tile was already added and the user was not prompted. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/StatusBarManager#TILE_ADD_REQUEST_RESULT_TILE_NOT_ADDED:kotlin.Int` Response indicating that the tile was not added. |
| --- | --- |

| Public methods ||
|---|---|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | canLaunchCaptureContentActivityForNote Checks whether the supplied activity can startActivityForResult a system activity that captures content on the screen to take a screenshot. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | requestAddTileService Request to the user to add a `https://developer.android.com/reference/kotlin/android/service/quicksettings/TileService.html#` to the set of current QS tiles. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | showPowerMenu Request to show the Power Menu. |
| --- | --- |

## Constants

### SHOW_POWER_MENU_RESULT_DISABLED

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SHOW_POWER_MENU_RESULT_DISABLED: Int
```

Result returned in a callback when a call to showPowerMenu cannot be completed due to the Power Menu being currently disabled.

 Value: 1

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager#LOCK_TASK_FEATURE_GLOBAL_ACTIONS:kotlin.Int`

### SHOW_POWER_MENU_RESULT_SHOWING

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SHOW_POWER_MENU_RESULT_SHOWING: Int
```

Result returned in a callback when a call to showPowerMenu has succeeded and the Power Menu is currently showing.

 Value: 0

### SHOW_POWER_MENU_RESULT_UNKNOWN

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SHOW_POWER_MENU_RESULT_UNKNOWN: Int
```

Unknwown result of calling showPowerMenu. Used for compatibility purposes.

 Value: -1

### TILE_ADD_REQUEST_ERROR_APP_NOT_IN_FOREGROUND

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TILE_ADD_REQUEST_ERROR_APP_NOT_IN_FOREGROUND: Int
```

Indicates that the requesting application is not in the foreground.

 Value: 1004

### TILE_ADD_REQUEST_ERROR_BAD_COMPONENT

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TILE_ADD_REQUEST_ERROR_BAD_COMPONENT: Int
```

Indicates that the component does not match an enabled exported `https://developer.android.com/reference/kotlin/android/service/quicksettings/TileService.html#` for the current user.

 Value: 1002

### TILE_ADD_REQUEST_ERROR_MISMATCHED_PACKAGE

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TILE_ADD_REQUEST_ERROR_MISMATCHED_PACKAGE: Int
```

Indicates that this package does not match that of the `https://developer.android.com/reference/kotlin/android/service/quicksettings/TileService.html#`.

 Value: 1000

### TILE_ADD_REQUEST_ERROR_NOT_CURRENT_USER

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TILE_ADD_REQUEST_ERROR_NOT_CURRENT_USER: Int
```

Indicates that the user is not the current user.

 Value: 1003

### TILE_ADD_REQUEST_ERROR_NO_STATUS_BAR_SERVICE

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TILE_ADD_REQUEST_ERROR_NO_STATUS_BAR_SERVICE: Int
```

The request could not be processed because no fulfilling service was found. This could be a temporary issue (for example, SystemUI has crashed).

 Value: 1005

### TILE_ADD_REQUEST_ERROR_REQUEST_IN_PROGRESS

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TILE_ADD_REQUEST_ERROR_REQUEST_IN_PROGRESS: Int
```

Indicates that there's a request in progress for this package.

 Value: 1001

### TILE_ADD_REQUEST_RESULT_TILE_ADDED

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TILE_ADD_REQUEST_RESULT_TILE_ADDED: Int
```

Response indicating that the tile was added.

 Value: 2

### TILE_ADD_REQUEST_RESULT_TILE_ALREADY_ADDED

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TILE_ADD_REQUEST_RESULT_TILE_ALREADY_ADDED: Int
```

Response indicating that the tile was already added and the user was not prompted.

 Value: 1

### TILE_ADD_REQUEST_RESULT_TILE_NOT_ADDED

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TILE_ADD_REQUEST_RESULT_TILE_NOT_ADDED: Int
```

Response indicating that the tile was not added.

 Value: 0

## Public methods

### canLaunchCaptureContentActivityForNote

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun canLaunchCaptureContentActivityForNote(activity: Activity): Boolean
```

Checks whether the supplied activity can startActivityForResult a system activity that captures content on the screen to take a screenshot.

Note: The result should not be cached.

The system activity displays an editing tool that allows user to edit the screenshot, save it on device, and return the edited screenshot as `https://developer.android.com/reference/kotlin/android/net/Uri.html#` to the calling activity. User interaction is required to return the edited screenshot to the calling activity.

When `true`, callers can use startActivityForResult to start start the content capture activity using `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_LAUNCH_CAPTURE_CONTENT_ACTIVITY_FOR_NOTE:kotlin.String`. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#LAUNCH_CAPTURE_CONTENT_ACTIVITY_FOR_NOTE:kotlin.String`

| Parameters ||
|---|---|
| `activity` | [Activity](Activity.md): Calling activity. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the activity supports launching the capture content activity for note. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_LAUNCH_CAPTURE_CONTENT_ACTIVITY_FOR_NOTE:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#LAUNCH_CAPTURE_CONTENT_ACTIVITY_FOR_NOTE:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/app/role/RoleManager#ROLE_NOTES:kotlin.String`

### requestAddTileService

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun requestAddTileService(
    tileServiceComponentName: ComponentName, 
    tileLabel: CharSequence, 
    icon: Icon, 
    resultExecutor: Executor, 
    resultCallback: Consumer<Int!>
): Unit
```

Request to the user to add a `https://developer.android.com/reference/kotlin/android/service/quicksettings/TileService.html#` to the set of current QS tiles.

Calling this will prompt the user to decide whether they want to add the shown `https://developer.android.com/reference/kotlin/android/service/quicksettings/TileService.html#` to their current tiles. The user can deny the request and the system can stop processing requests for a given `https://developer.android.com/reference/kotlin/android/content/ComponentName.html#` after a number of requests.

The request will show to the user information about the tile:

- Application name
- Label for the tile
- Icon for the tile

The user for which this will be added is determined from the `https://developer.android.com/reference/kotlin/android/content/Context.html#` used to retrieve this service, and must match the current user. The requesting application must be in the foreground (`https://developer.android.com/reference/kotlin/android/app/ActivityManager.RunningAppProcessInfo#IMPORTANCE_FOREGROUND:kotlin.Int` and the `https://developer.android.com/reference/kotlin/android/service/quicksettings/TileService.html#` must be exported. Note: the system can choose to auto-deny a request if the user has denied that specific request (user, ComponentName) enough times before.

| Parameters ||
|---|---|
| `tileServiceComponentName` | [ComponentName](../android.content/ComponentName.md): `https://developer.android.com/reference/kotlin/android/content/ComponentName.html#` of the `https://developer.android.com/reference/kotlin/android/service/quicksettings/TileService.html#` for the request. This value cannot be `null`. |
| `tileLabel` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html): label of the tile to show to the user. This value cannot be `null`. |
| `icon` | [Icon](../android.graphics.drawable/Icon.md): icon to use in the tile shown to the user. This value cannot be `null`. |
| --- | --- |
| `resultExecutor` | [Executor](../java.util.concurrent/Executor.md): an executor to run the callback on. This value cannot be `null`. |
| `resultCallback` | [Consumer](../java.util.function/Consumer.md)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\>: callback to indicate the result of the request. This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/service/quicksettings/TileService.html#`

### showPowerMenu

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun showPowerMenu(
    executor: Executor, 
    receiver: OutcomeReceiver<Int!, Throwable!>
): Unit
```

Request to show the Power Menu.

The Power Menu is the dialog that contains options like Power off, Restart, etc. Also known as Global Actions

Showing this dialog may be restricted by the system, for example by DevicePolicyManager, if `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager#LOCK_TASK_FEATURE_GLOBAL_ACTIONS:kotlin.Int` is set.

The `receiver` will indicate when the Power Menu is visible (if possible) in its result, or whether the Power Menu is currently disabled. If the Power Menu is currently visible when the request is made, `https://developer.android.com/reference/kotlin/android/app/StatusBarManager#SHOW_POWER_MENU_RESULT_SHOWING:kotlin.Int` will be returned through the callback immediately.

Alternatively, if the request could not be completed due to an error, it will be returned with onError. This error can be `https://developer.android.com/reference/kotlin/java/util/concurrent/TimeoutException.html#` if the request times out after a few seconds without a response, or a different `https://developer.android.com/reference/kotlin/java/lang/Exception.html#`. In these error cases, it usually means that there's an underlying issue with the system and retrying will not succeed.

This callback can be reused for multiple requests. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#SHOW_POWER_MENU:kotlin.String` or `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#SHOW_POWER_MENU_PRIVILEGED:kotlin.String`

| Parameters ||
|---|---|
| `executor` | [Executor](../java.util.concurrent/Executor.md): an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` in which the methods of `callback` will be called. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use getMainExecutor. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `receiver` | [OutcomeReceiver](../android.os/OutcomeReceiver.md)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!, [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!\>: will call back with the result of the request, or a possible error. This value cannot be `null`. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/app/StatusBarManager#SHOW_POWER_MENU_RESULT_UNKNOWN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/StatusBarManager#SHOW_POWER_MENU_RESULT_SHOWING:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/StatusBarManager#SHOW_POWER_MENU_RESULT_DISABLED:kotlin.Int` |
