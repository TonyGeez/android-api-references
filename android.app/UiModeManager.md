# UiModeManager

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# UiModeManager

Kotlin| [Java](UiModeManager.md) 
| --- | --- |

```
open class UiModeManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.app.UiModeManager](UiModeManager.md) |

This class provides access to the system uimode services. These services allow applications to control UI modes of the device. It provides functionality to disable the car mode and it gives access to the night mode settings.

These facilities are built on top of the underlying [android.content.Intent#ACTION_DOCK_EVENT](../android.content/Intent.md) broadcasts that are sent when the user physical places the device into and out of a dock. When that happens, the UiModeManager switches the system [android.content.res.Configuration](../android.content.res/Configuration.md) to the appropriate UI mode, sends broadcasts about the mode switch, and starts the corresponding mode activity if appropriate. See the broadcasts [ACTION_ENTER_CAR_MODE](UiModeManager.md) and [ACTION_ENTER_DESK_MODE](UiModeManager.md) for more information.

In addition, the user may manually switch the system to car mode without physically being in a dock. While in car mode -- whether by manual action from the user or being physically placed in a dock -- a notification is displayed allowing the user to exit dock mode. Thus the dock mode represented here may be different than the current state of the underlying dock event broadcast.

## Summary

| Nested classes ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [ContrastChangeListener](../android/app/UiModeManager.ContrastChangeListener.md) Listener for the UI contrast. |

| Constants ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DISABLE_CAR_MODE_GO_HOME](UiModeManager.md) Flag for use with [disableCarMode(int)](UiModeManager.md)): go to the normal home activity as part of the disable. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ENABLE_CAR_MODE_ALLOW_SLEEP](UiModeManager.md) Flag for use with [enableCarMode(int)](UiModeManager.md)): allow sleep mode while in car mode. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ENABLE_CAR_MODE_GO_CAR_HOME](UiModeManager.md) Flag for use with [enableCarMode(int)](UiModeManager.md)): go to the car home activity as part of the enable. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MODE_NIGHT_AUTO](UiModeManager.md) Constant for [setNightMode(int)](UiModeManager.md))and [getNightMode()](UiModeManager.md)): automatically switch night mode on and off based on the time. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MODE_NIGHT_CUSTOM](UiModeManager.md) Constant for [setNightMode(int)](UiModeManager.md))and [getNightMode()](UiModeManager.md)): automatically switch night mode on and off based on the time. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MODE_NIGHT_NO](UiModeManager.md) Constant for [setNightMode(int)](UiModeManager.md))and [getNightMode()](UiModeManager.md)): never run in night mode. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MODE_NIGHT_YES](UiModeManager.md) Constant for [setNightMode(int)](UiModeManager.md))and [getNightMode()](UiModeManager.md)): always run in night mode. |

| Public methods ||
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addContrastChangeListener](UiModeManager.md))`(`executor:` ` [Executor](../java.util.concurrent/Executor.md)`, `listener:` ` [UiModeManager.ContrastChangeListener](../android/app/UiModeManager.ContrastChangeListener.md)`)` Registers a [ContrastChangeListener](../android/app/UiModeManager.ContrastChangeListener.md) for the user. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [disableCarMode](UiModeManager.md))`(`flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Turn off special mode if currently in car mode. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [enableCarMode](UiModeManager.md))`(`flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Force device into car mode, like it had been placed in the car dock. |
| --- | --- |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getContrast](UiModeManager.md))`()` Returns the color contrast for the user. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getCurrentModeType](UiModeManager.md))`()` Return the current running mode type. |
| open [LocalTime](../java.time/LocalTime.md) | [getCustomNightModeEnd](UiModeManager.md))`()` Returns the time of the day Dark theme deactivates |
| --- | --- |
| open [LocalTime](../java.time/LocalTime.md) | [getCustomNightModeStart](UiModeManager.md))`()` Returns the time of the day Dark theme activates |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getNightMode](UiModeManager.md))`()` Returns the currently configured night mode. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeContrastChangeListener](UiModeManager.md))`(`listener:` ` [UiModeManager.ContrastChangeListener](../android/app/UiModeManager.ContrastChangeListener.md)`)` Unregisters a [ContrastChangeListener](../android/app/UiModeManager.ContrastChangeListener.md) for the user. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setApplicationNightMode](UiModeManager.md))`(`mode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets and persist the night mode for this application. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setCustomNightModeEnd](UiModeManager.md))`(`time:` ` [LocalTime](../java.time/LocalTime.md)`)` Sets the time of the day Dark theme deactivates |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setCustomNightModeStart](UiModeManager.md))`(`time:` ` [LocalTime](../java.time/LocalTime.md)`)` Sets the time of the day Dark theme activates |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setNightMode](UiModeManager.md))`(`mode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the system-wide night mode. |

| Properties ||
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [ACTION_ENTER_CAR_MODE](UiModeManager.md) Broadcast sent when the device's UI has switched to car mode, either by being placed in a car dock or explicit action of the user. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [ACTION_ENTER_DESK_MODE](UiModeManager.md) Broadcast sent when the device's UI has switched to desk mode, by being placed in a desk dock. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [ACTION_EXIT_CAR_MODE](UiModeManager.md) Broadcast sent when the device's UI has switch away from car mode back to normal mode. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [ACTION_EXIT_DESK_MODE](UiModeManager.md) Broadcast sent when the device's UI has switched away from desk mode back to normal mode. |

## Constants

### DISABLE_CAR_MODE_GO_HOME

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DISABLE_CAR_MODE_GO_HOME: Int
```

Flag for use with [disableCarMode(int)](UiModeManager.md)): go to the normal home activity as part of the disable. Disabling this way ensures a clean transition between the current activity (in car mode) and the original home activity (which was typically last running without being in car mode). 

 Value: 1

### ENABLE_CAR_MODE_ALLOW_SLEEP

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ENABLE_CAR_MODE_ALLOW_SLEEP: Int
```

Flag for use with [enableCarMode(int)](UiModeManager.md)): allow sleep mode while in car mode. By default, when this flag is not set, the system may hold a full wake lock to keep the screen turned on and prevent the system from entering sleep mode while in car mode. Setting this flag disables such behavior and the system may enter sleep mode if there is no other user activity and no other wake lock held. Setting this flag can be relevant for a car dock application that does not require the screen kept on. 

 Value: 2

### ENABLE_CAR_MODE_GO_CAR_HOME

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ENABLE_CAR_MODE_GO_CAR_HOME: Int
```

Flag for use with [enableCarMode(int)](UiModeManager.md)): go to the car home activity as part of the enable. Enabling this way ensures a clean transition between the current activity (in non-car-mode) and the car home activity that will serve as home while in car mode. This will switch to the car home activity even if we are already in car mode. 

 Value: 1

### MODE_NIGHT_AUTO

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MODE_NIGHT_AUTO: Int
```

Constant for [setNightMode(int)](UiModeManager.md))and [getNightMode()](UiModeManager.md)): automatically switch night mode on and off based on the time. 

 Value: 0

### MODE_NIGHT_CUSTOM

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MODE_NIGHT_CUSTOM: Int
```

Constant for [setNightMode(int)](UiModeManager.md))and [getNightMode()](UiModeManager.md)): automatically switch night mode on and off based on the time. 

 Value: 3

### MODE_NIGHT_NO

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MODE_NIGHT_NO: Int
```

Constant for [setNightMode(int)](UiModeManager.md))and [getNightMode()](UiModeManager.md)): never run in night mode. 

 Value: 1

### MODE_NIGHT_YES

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MODE_NIGHT_YES: Int
```

Constant for [setNightMode(int)](UiModeManager.md))and [getNightMode()](UiModeManager.md)): always run in night mode. 

 Value: 2

## Public methods

### addContrastChangeListener

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun addContrastChangeListener(
    executor: Executor, 
    listener: UiModeManager.ContrastChangeListener
): Unit
```

Registers a [ContrastChangeListener](../android/app/UiModeManager.ContrastChangeListener.md) for the user.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `executor` | [Executor](../java.util.concurrent/Executor.md):The executor on which the listener should be called back. This value cannot be`null`. Callback and listener events are dispatched through this [Executor](../java.util.concurrent/Executor.md), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](../android.content/Context.md)). Otherwise, provide an [Executor](../java.util.concurrent/Executor.md) that dispatches to an appropriate thread. |
| `listener` | [UiModeManager.ContrastChangeListener](../android/app/UiModeManager.ContrastChangeListener.md):The listener. This value cannot be`null`. |

### disableCarMode

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun disableCarMode(flags: Int): Unit
```

Turn off special mode if currently in car mode.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):One of the disable car mode flags. Value is [android.app.UiModeManager#DISABLE_CAR_MODE_GO_HOME](UiModeManager.md) |

### enableCarMode

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun enableCarMode(flags: Int): Unit
```

Force device into car mode, like it had been placed in the car dock. This will cause the device to switch to the car home UI as part of the mode switch.

| Parameters ||
|---------|---------------------------------------------------------------------------------------|
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Must be 0. |

### getContrast

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getContrast(): Float
```

Returns the color contrast for the user.

**Note:**You need to query this only if your application is doing its own rendering and does not rely on the material rendering pipeline.

| Return ||
|--------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | The color contrast, float in \[-1, 1\] where - 0 corresponds to the default contrast - -1 corresponds to the minimum contrast - 1 corresponds to the maximum contrast Value is between -1.0f and 1.0f inclusive |

### getCurrentModeType

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getCurrentModeType(): Int
```

Return the current running mode type. May be one of [Configuration.UI_MODE_TYPE_NORMAL](../android.content.res/Configuration.md), [Configuration.UI_MODE_TYPE_DESK](../android.content.res/Configuration.md), [Configuration.UI_MODE_TYPE_CAR](../android.content.res/Configuration.md), [Configuration.UI_MODE_TYPE_TELEVISION](../android.content.res/Configuration.md), [Configuration.UI_MODE_TYPE_APPLIANCE](../android.content.res/Configuration.md), [Configuration.UI_MODE_TYPE_WATCH](../android.content.res/Configuration.md), or [Configuration.UI_MODE_TYPE_VR_HEADSET](../android.content.res/Configuration.md). 

### getCustomNightModeEnd

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getCustomNightModeEnd(): LocalTime
```

Returns the time of the day Dark theme deactivates

When night mode is [MODE_NIGHT_CUSTOM](UiModeManager.md), the system uses this time set to deactivate it automatically.

| Return ||
|---------------------------------------------------------------------------------------|-----------------------------|
| [LocalTime](../java.time/LocalTime.md) | This value cannot be`null`. |

### getCustomNightModeStart

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getCustomNightModeStart(): LocalTime
```

Returns the time of the day Dark theme activates

When night mode is [MODE_NIGHT_CUSTOM](UiModeManager.md), the system uses this time set to activate it automatically.

| Return ||
|---------------------------------------------------------------------------------------|-----------------------------|
| [LocalTime](../java.time/LocalTime.md) | This value cannot be`null`. |

### getNightMode

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getNightMode(): Int
```

Returns the currently configured night mode.

May be one of:

- [MODE_NIGHT_NO](UiModeManager.md)
- [MODE_NIGHT_YES](UiModeManager.md)
- [MODE_NIGHT_AUTO](UiModeManager.md)
- [MODE_NIGHT_CUSTOM](UiModeManager.md)
- `-1`on error

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the current night mode, or`-1`on error Value is [android.app.UiModeManager#MODE_NIGHT_AUTO](UiModeManager.md), [android.app.UiModeManager#MODE_NIGHT_CUSTOM](UiModeManager.md), [android.app.UiModeManager#MODE_NIGHT_NO](UiModeManager.md), or [android.app.UiModeManager#MODE_NIGHT_YES](UiModeManager.md) |

**See Also**

- [#setNightMode(int)](UiModeManager.md)) 

### removeContrastChangeListener

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun removeContrastChangeListener(listener: UiModeManager.ContrastChangeListener): Unit
```

Unregisters a [ContrastChangeListener](../android/app/UiModeManager.ContrastChangeListener.md) for the user. If the listener was not registered, does nothing and returns.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [UiModeManager.ContrastChangeListener](../android/app/UiModeManager.ContrastChangeListener.md):The listener to unregister. This value cannot be`null`. |

### setApplicationNightMode

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setApplicationNightMode(mode: Int): Unit
```

Sets and persist the night mode for this application.

The mode can be one of:

- * [MODE_NIGHT_NO](UiModeManager.md)* sets the device into`notnight`mode
- * [MODE_NIGHT_YES](UiModeManager.md)* sets the device into`night`mode
- * [MODE_NIGHT_CUSTOM](UiModeManager.md)* automatically switches between`night`and`notnight`based on the custom time set (or default)
- * [MODE_NIGHT_AUTO](UiModeManager.md)* automatically switches between`night`and`notnight`based on the device's current location and certain other sensors

Changes to night mode take effect locally and will result in a configuration change (and potentially an Activity lifecycle event) being applied to this application. The mode is persisted for this application until it is either modified by the application, the user clears the data for the application, or this application is uninstalled.

Developers interested in a non-persistent app-local implementation of night mode should consider using androidx.appcompat.app.AppCompatDelegate#setDefaultNightMode(int) to manage the -night qualifier locally.

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `mode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the night mode to set Value is [android.app.UiModeManager#MODE_NIGHT_AUTO](UiModeManager.md), [android.app.UiModeManager#MODE_NIGHT_CUSTOM](UiModeManager.md), [android.app.UiModeManager#MODE_NIGHT_NO](UiModeManager.md), or [android.app.UiModeManager#MODE_NIGHT_YES](UiModeManager.md) |

**See Also**

- [#setNightMode(int)](UiModeManager.md)) 

### setCustomNightModeEnd

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setCustomNightModeEnd(time: LocalTime): Unit
```

Sets the time of the day Dark theme deactivates

When night mode is [MODE_NIGHT_CUSTOM](UiModeManager.md), the system uses this time set to deactivate it automatically.

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `time` | [LocalTime](../java.time/LocalTime.md):The time of the day Dark theme should deactivate This value cannot be`null`. |

### setCustomNightModeStart

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setCustomNightModeStart(time: LocalTime): Unit
```

Sets the time of the day Dark theme activates

When night mode is [MODE_NIGHT_CUSTOM](UiModeManager.md), the system uses this time set to activate it automatically

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `time` | [LocalTime](../java.time/LocalTime.md):The time of the day Dark theme should activate This value cannot be`null`. |

### setNightMode

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setNightMode(mode: Int): Unit
```

Sets the system-wide night mode.

The mode can be one of:

- * [MODE_NIGHT_NO](UiModeManager.md)* sets the device into`notnight`mode
- * [MODE_NIGHT_YES](UiModeManager.md)* sets the device into`night`mode
- * [MODE_NIGHT_CUSTOM](UiModeManager.md)* automatically switches between`night`and`notnight`based on the custom time set (or default)
- * [MODE_NIGHT_AUTO](UiModeManager.md)* automatically switches between`night`and`notnight`based on the device's current location and certain other sensors

**Note:** On API 22 and below, changes to the night mode are only effective when the [car](../android.content.res/Configuration.md) or [desk](../android.content.res/Configuration.md) mode is enabled on a device. On API 23 through API 28, changes to night mode are always effective.

Starting in API 29, when the device is in car mode and this method is called, night mode will change, but the new setting is not persisted and the previously persisted setting will be restored when the device exits car mode.

Changes to night mode take effect globally and will result in a configuration change (and potentially an Activity lifecycle event) being applied to all running apps. Developers interested in an app-local implementation of night mode should consider using [setApplicationNightMode(int)](UiModeManager.md))to set and persist the -night qualifier locally or androidx.appcompat.app.AppCompatDelegate#setDefaultNightMode(int) for the backward compatible implementation.

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `mode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the night mode to set Value is [android.app.UiModeManager#MODE_NIGHT_AUTO](UiModeManager.md), [android.app.UiModeManager#MODE_NIGHT_CUSTOM](UiModeManager.md), [android.app.UiModeManager#MODE_NIGHT_NO](UiModeManager.md), or [android.app.UiModeManager#MODE_NIGHT_YES](UiModeManager.md) |

**See Also**

- <https://developer.android.com/reference/kotlin/android/app/UiModeManager#getNightMode()>
- [#setApplicationNightMode(int)](UiModeManager.md))

## Properties

### ACTION_ENTER_CAR_MODE

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static var ACTION_ENTER_CAR_MODE: String!
```

Broadcast sent when the device's UI has switched to car mode, either by being placed in a car dock or explicit action of the user. After sending the broadcast, the system will start the intent [android.content.Intent#ACTION_MAIN](../android.content/Intent.md) with category [android.content.Intent#CATEGORY_CAR_DOCK](../android.content/Intent.md) to display the car UI, which typically what an application would implement to provide their own interface. However, applications can also monitor this Intent in order to be informed of mode changes or prevent the normal car UI from being displayed by setting the result of the broadcast to [Activity.RESULT_CANCELED](Activity.md).

This intent is broadcast when [getCurrentModeType()](UiModeManager.md))transitions to [Configuration.UI_MODE_TYPE_CAR](../android.content.res/Configuration.md) from some other ui mode. 

### ACTION_ENTER_DESK_MODE

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static var ACTION_ENTER_DESK_MODE: String!
```

Broadcast sent when the device's UI has switched to desk mode, by being placed in a desk dock. After sending the broadcast, the system will start the intent [android.content.Intent#ACTION_MAIN](../android.content/Intent.md) with category [android.content.Intent#CATEGORY_DESK_DOCK](../android.content/Intent.md) to display the desk UI, which typically what an application would implement to provide their own interface. However, applications can also monitor this Intent in order to be informed of mode changes or prevent the normal desk UI from being displayed by setting the result of the broadcast to [Activity.RESULT_CANCELED](Activity.md). 

### ACTION_EXIT_CAR_MODE

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static var ACTION_EXIT_CAR_MODE: String!
```

Broadcast sent when the device's UI has switch away from car mode back to normal mode. Typically used by a car mode app, to dismiss itself when the user exits car mode.

This intent is broadcast when [getCurrentModeType()](UiModeManager.md))transitions from [Configuration.UI_MODE_TYPE_CAR](../android.content.res/Configuration.md) to some other ui mode. 

### ACTION_EXIT_DESK_MODE

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static var ACTION_EXIT_DESK_MODE: String!
```

Broadcast sent when the device's UI has switched away from desk mode back to normal mode. Typically used by a desk mode app, to dismiss itself when the user exits desk mode.
