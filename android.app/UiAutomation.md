# UiAutomation

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# UiAutomation

Kotlin| [Java](../android/app/UiAutomation.md) 
| --- | --- |

```
class UiAutomation
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.app.UiAutomation](../android/app/UiAutomation.md) |

Class for interacting with the device's UI by simulation user actions and introspection of the screen content. It relies on the platform accessibility APIs to introspect the screen and to perform some actions on the remote view tree. It also allows injecting of arbitrary raw input events simulating user interaction with keyboards and touch devices. One can think of a UiAutomation as a special type of [android.accessibilityservice.AccessibilityService](../android/accessibilityservice/AccessibilityService.md) which does not provide hooks for the service life cycle and exposes other APIs that are useful for UI test automation.

The APIs exposed by this class are low-level to maximize flexibility when developing UI test automation tools and libraries. Generally, a UiAutomation client should be using a higher-level library or implement high-level functions. For example, performing a tap on the screen requires construction and injecting of a touch down and up events which have to be delivered to the system by a call to [injectInputEvent(android.view.InputEvent,boolean)](../android/app/UiAutomation.md)).

The APIs exposed by this class operate across applications enabling a client to write tests that cover use cases spanning over multiple applications. For example, going to the settings application to change a setting and then interacting with another application whose behavior depends on that setting.

## Summary

| Nested classes ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [AccessibilityEventFilter](../android/app/UiAutomation.AccessibilityEventFilter.md) Listener for filtering accessibility events. |
| abstract | [OnAccessibilityEventListener](../android/app/UiAutomation.OnAccessibilityEventListener.md) Listener for observing the [AccessibilityEvent](../android/view/accessibility/AccessibilityEvent.md) stream. |

| Constants ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FLAG_DONT_SUPPRESS_ACCESSIBILITY_SERVICES](../android/app/UiAutomation.md) UiAutomation suppresses accessibility services by default. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FLAG_DONT_USE_ACCESSIBILITY](../android/app/UiAutomation.md) UiAutomation uses the accessibility subsystem by default. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ROTATION_FREEZE_0](../android/app/UiAutomation.md) Rotation constant: Freeze rotation to 0 degrees (natural orientation) |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ROTATION_FREEZE_180](../android/app/UiAutomation.md) Rotation constant: Freeze rotation to 180 degrees . |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ROTATION_FREEZE_270](../android/app/UiAutomation.md) Rotation constant: Freeze rotation to 270 degrees . |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ROTATION_FREEZE_90](../android/app/UiAutomation.md) Rotation constant: Freeze rotation to 90 degrees . |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ROTATION_FREEZE_CURRENT](../android/app/UiAutomation.md) Rotation constant: Freeze rotation to its current state. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ROTATION_UNFREEZE](../android/app/UiAutomation.md) Rotation constant: Unfreeze rotation (rotating the device changes its rotation state). |

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [adoptShellPermissionIdentity](../android/app/UiAutomation.md))`()` Adopt the permission identity of the shell UID for all permissions. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [adoptShellPermissionIdentity](../android/app/UiAutomation.md))`(`vararg` `permissions:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Adopt the permission identity of the shell UID only for the provided permissions. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [clearCache](../android/app/UiAutomation.md))`()` Clears the accessibility cache. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clearWindowAnimationFrameStats](../android/app/UiAutomation.md))`()` Clears the window animation rendering statistics. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [clearWindowContentFrameStats](../android/app/UiAutomation.md))`(`windowId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Clears the frame statistics for the content of a given window. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [dropShellPermissionIdentity](../android/app/UiAutomation.md))`()` Drop the shell permission identity adopted by a previous call to [adoptShellPermissionIdentity()](../android/app/UiAutomation.md)). |
| --- | --- |
| [AccessibilityEvent](../android/view/accessibility/AccessibilityEvent.md)! | [executeAndWaitForEvent](../android/app/UiAutomation.md))`(`command:` ` [Runnable](../java/lang/Runnable.md)!`, `filter:` ` [UiAutomation.AccessibilityEventFilter](../android/app/UiAutomation.AccessibilityEventFilter.md)!`, `timeoutMillis:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Executes a command and waits for a specific accessibility event up to a given wait timeout. |
| [ParcelFileDescriptor](../android/os/ParcelFileDescriptor.md)! | [executeShellCommand](../android/app/UiAutomation.md))`(`command:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Executes a shell command. |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [ParcelFileDescriptor](../android/os/ParcelFileDescriptor.md)!\> | [executeShellCommandRw](../android/app/UiAutomation.md))`(`command:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Executes a shell command. |
| --- | --- |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [ParcelFileDescriptor](../android/os/ParcelFileDescriptor.md)!\> | [executeShellCommandRwe](../android/app/UiAutomation.md))`(`command:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Executes a shell command. |
| [AccessibilityNodeInfo](../android/view/accessibility/AccessibilityNodeInfo.md)! | [findFocus](../android/app/UiAutomation.md))`(`focus:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Find the view that has the specified focus type. |
| [AccessibilityNodeInfo](../android/view/accessibility/AccessibilityNodeInfo.md)! | [getRootInActiveWindow](../android/app/UiAutomation.md))`()` Gets the root [AccessibilityNodeInfo](../android/view/accessibility/AccessibilityNodeInfo.md) in the active window. |
| --- | --- |
| [AccessibilityServiceInfo](../android/accessibilityservice/AccessibilityServiceInfo.md)! | [getServiceInfo](../android/app/UiAutomation.md))`()` Gets the an [AccessibilityServiceInfo](../android/accessibilityservice/AccessibilityServiceInfo.md) describing this UiAutomation. |
| [WindowAnimationFrameStats](../android/view/WindowAnimationFrameStats.md)! | [getWindowAnimationFrameStats](../android/app/UiAutomation.md))`()` Gets the window animation frame statistics. |
| [WindowContentFrameStats](../android/view/WindowContentFrameStats.md)! | [getWindowContentFrameStats](../android/app/UiAutomation.md))`(`windowId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Gets the frame statistics for a given window. |
| --- | --- |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [AccessibilityWindowInfo](../android/view/accessibility/AccessibilityWindowInfo.md)!\>! | [getWindows](../android/app/UiAutomation.md))`()` Gets the windows on the screen associated with the [UiAutomation](../android/app/UiAutomation.md) context (usually the [default display).](../android/view/Display.md) |
| [SparseArray](../android/util/SparseArray.md)\< [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [AccessibilityWindowInfo](../android/view/accessibility/AccessibilityWindowInfo.md)!\>!\> | [getWindowsOnAllDisplays](../android/app/UiAutomation.md))`()` Gets the windows on the screen of all displays. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [grantRuntimePermission](../android/app/UiAutomation.md))`(`packageName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `permission:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Grants a runtime permission to a package. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [grantRuntimePermissionAsUser](../android/app/UiAutomation.md))`(`packageName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `permission:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `userHandle:` ` [UserHandle](../android/os/UserHandle.md)!`)` Grants a runtime permission to a package for a user. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [injectInputEvent](../android/app/UiAutomation.md))`(`event:` ` [InputEvent](../android/view/InputEvent.md)!`, `sync:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` A method for injecting an arbitrary input event. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [performGlobalAction](../android/app/UiAutomation.md))`(`action:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Performs a global action. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [revokeRuntimePermission](../android/app/UiAutomation.md))`(`packageName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `permission:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Revokes a runtime permission from a package. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [revokeRuntimePermissionAsUser](../android/app/UiAutomation.md))`(`packageName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `permission:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `userHandle:` ` [UserHandle](../android/os/UserHandle.md)!`)` Revokes a runtime permission from a package. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAnimationScale](../android/app/UiAutomation.md))`(`scale:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Sets the system settings values that control the scaling factor for animations. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOnAccessibilityEventListener](../android/app/UiAutomation.md))`(`listener:` ` [UiAutomation.OnAccessibilityEventListener](../android/app/UiAutomation.OnAccessibilityEventListener.md)!`)` Sets a callback for observing the stream of [AccessibilityEvent](../android/view/accessibility/AccessibilityEvent.md) s. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [setRotation](../android/app/UiAutomation.md))`(`rotation:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the device rotation. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setRunAsMonkey](../android/app/UiAutomation.md))`(`enable:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets whether this UiAutomation to run in a "monkey" mode. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setServiceInfo](../android/app/UiAutomation.md))`(`info:` ` [AccessibilityServiceInfo](../android/accessibilityservice/AccessibilityServiceInfo.md)!`)` Sets the [AccessibilityServiceInfo](../android/accessibilityservice/AccessibilityServiceInfo.md) that describes how this UiAutomation will be handled by the platform accessibility layer. |
| [Bitmap](../android/graphics/Bitmap.md)! | [takeScreenshot](../android/app/UiAutomation.md))`()` Takes a screenshot. |
| [Bitmap](../android/graphics/Bitmap.md)? | [takeScreenshot](../android/app/UiAutomation.md))`(`window:` ` [Window](../android/view/Window.md)`)` Used to capture a screenshot of a Window. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../android/app/UiAutomation.md))`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [waitForIdle](../android/app/UiAutomation.md))`(`idleTimeoutMillis:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `globalTimeoutMillis:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Waits for the accessibility event stream to become idle, which is not to have received an accessibility event within`idleTimeoutMillis`. |

## Constants

### FLAG_DONT_SUPPRESS_ACCESSIBILITY_SERVICES

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FLAG_DONT_SUPPRESS_ACCESSIBILITY_SERVICES: Int
```

UiAutomation suppresses accessibility services by default. This flag specifies that existing accessibility services should continue to run, and that new ones may start. This flag is set when obtaining the UiAutomation from [Instrumentation.getUiAutomation(int)](../android/app/Instrumentation.md)). 

 Value: 1

### FLAG_DONT_USE_ACCESSIBILITY

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FLAG_DONT_USE_ACCESSIBILITY: Int
```

UiAutomation uses the accessibility subsystem by default. This flag provides an option to eliminate the overhead of engaging the accessibility subsystem for tests that do not need to interact with the user interface. Setting this flag disables methods that rely on accessibility. This flag is set when obtaining the UiAutomation from [Instrumentation.getUiAutomation(int)](../android/app/Instrumentation.md)). 

 Value: 2

### ROTATION_FREEZE_0

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ROTATION_FREEZE_0: Int
```

Rotation constant: Freeze rotation to 0 degrees (natural orientation) 

 Value: 0

### ROTATION_FREEZE_180

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ROTATION_FREEZE_180: Int
```

Rotation constant: Freeze rotation to 180 degrees . 

 Value: 2

### ROTATION_FREEZE_270

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ROTATION_FREEZE_270: Int
```

Rotation constant: Freeze rotation to 270 degrees . 

 Value: 3

### ROTATION_FREEZE_90

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ROTATION_FREEZE_90: Int
```

Rotation constant: Freeze rotation to 90 degrees . 

 Value: 1

### ROTATION_FREEZE_CURRENT

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ROTATION_FREEZE_CURRENT: Int
```

Rotation constant: Freeze rotation to its current state. 

 Value: -1

### ROTATION_UNFREEZE

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ROTATION_UNFREEZE: Int
```

Rotation constant: Unfreeze rotation (rotating the device changes its rotation state). 

 Value: -2

## Public methods

### adoptShellPermissionIdentity

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun adoptShellPermissionIdentity(): Unit
```

Adopt the permission identity of the shell UID for all permissions. This allows you to call APIs protected permissions which normal apps cannot hold but are granted to the shell UID. If you already adopted all shell permissions by calling this method or [adoptShellPermissionIdentity(java.lang.String...)](../android/app/UiAutomation.md))a subsequent call will replace any previous adoption. Note that your permission state becomes that of the shell UID and it is not a combination of your and the shell UID permissions.

**Note:Calling this method adopts all shell permissions and overrides any subset of adopted permissions via [adoptShellPermissionIdentity(java.lang.String...)](../android/app/UiAutomation.md)).** 
**See Also**

- [#adoptShellPermissionIdentity(String...)](../android/app/UiAutomation.md))
- <https://developer.android.com/reference/kotlin/android/app/UiAutomation#dropShellPermissionIdentity()> 

### adoptShellPermissionIdentity

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun adoptShellPermissionIdentity(vararg permissions: String!): Unit
```

Adopt the permission identity of the shell UID only for the provided permissions. This allows you to call APIs protected permissions which normal apps cannot hold but are granted to the shell UID. If you already adopted shell permissions by calling this method, or [adoptShellPermissionIdentity()](../android/app/UiAutomation.md))a subsequent call will replace any previous adoption.

**Note:This method behave differently from [adoptShellPermissionIdentity()](../android/app/UiAutomation.md)). Only the listed permissions will use the shell identity and other permissions will still check against the original UID**

| Parameters ||
|---------------|----------------------------------------------------------------------------------------------------------------------------------|
| `permissions` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The permissions to adopt or`null`to adopt all. |

**See Also**

- <https://developer.android.com/reference/kotlin/android/app/UiAutomation#adoptShellPermissionIdentity()>
- <https://developer.android.com/reference/kotlin/android/app/UiAutomation#dropShellPermissionIdentity()> 

### clearCache

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun clearCache(): Boolean
```

Clears the accessibility cache.

| Return ||
|------------------------------------------------------------------------------------|--------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the cache was cleared |

**See Also**

- [android.accessibilityservice.AccessibilityService#clearCache()](../android/accessibilityservice/AccessibilityService.md)) 

### clearWindowAnimationFrameStats

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun clearWindowAnimationFrameStats(): Unit
```

**Deprecated:** *animation-frames are no-longer used. Use Shared [FrameTimeline](https://perfetto.dev/docs/data-sources/frametimeline) jank metrics instead.*

Clears the window animation rendering statistics. These statistics contain information about the most recently rendered window animation frames, i.e. for window transition animations. 
**See Also**

- [android.view.WindowAnimationFrameStats](../android/view/WindowAnimationFrameStats.md)
- <https://developer.android.com/reference/kotlin/android/app/UiAutomation#getWindowAnimationFrameStats()>
- [android.R.styleable#WindowAnimation](../android/R.styleable.md) 

### clearWindowContentFrameStats

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun clearWindowContentFrameStats(windowId: Int): Boolean
```

Clears the frame statistics for the content of a given window. These statistics contain information about the most recently rendered content frames.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------|
| `windowId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The window id. |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | Whether the window is present and its frame statistics were cleared. |

| Exceptions ||
|-----------------------------------|----------------------------------------------------------------------|
| `java.lang.IllegalStateException` | If the connection to the accessibility subsystem is not established. |

**See Also**

- [android.view.WindowContentFrameStats](../android/view/WindowContentFrameStats.md)
- [#getWindowContentFrameStats(int)](../android/app/UiAutomation.md))
- <https://developer.android.com/reference/kotlin/android/app/UiAutomation#getWindows()>
- [android.view.accessibility.AccessibilityWindowInfo#getId()](../android/view/accessibility/AccessibilityWindowInfo.md)) 

### dropShellPermissionIdentity

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun dropShellPermissionIdentity(): Unit
```

Drop the shell permission identity adopted by a previous call to [adoptShellPermissionIdentity()](../android/app/UiAutomation.md)). If you did not adopt the shell permission identity this method would be a no-op. 
**See Also**

- <https://developer.android.com/reference/kotlin/android/app/UiAutomation#adoptShellPermissionIdentity()> 

### executeAndWaitForEvent

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun executeAndWaitForEvent(
    command: Runnable!, 
    filter: UiAutomation.AccessibilityEventFilter!, 
    timeoutMillis: Long
): AccessibilityEvent!
```

Executes a command and waits for a specific accessibility event up to a given wait timeout. To detect a sequence of events one can implement a filter that keeps track of seen events of the expected sequence and returns true after the last event of that sequence is received.

**Note:**It is caller's responsibility to recycle the returned event.

| Parameters ||
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `command` | [Runnable](../java/lang/Runnable.md)!:The command to execute. |
| `filter` | [UiAutomation.AccessibilityEventFilter](../android/app/UiAutomation.AccessibilityEventFilter.md)!:Filter that recognizes the expected event. |
| `timeoutMillis` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The wait timeout in milliseconds. |
| --- | --- |

| Exceptions ||
|-----------------------------------------|----------------------------------------------------------------------|
| `java.util.concurrent.TimeoutException` | If the expected event is not received within the timeout. |
| `java.lang.IllegalStateException` | If the connection to the accessibility subsystem is not established. |

### executeShellCommand

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun executeShellCommand(command: String!): ParcelFileDescriptor!
```

Executes a shell command. This method returns a file descriptor that points to the standard output stream. The command execution is similar to running "adb shell " from a host connected to the device.

**Note:**It is your responsibility to close the returned file descriptor once you are done reading.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------|
| `command` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The command to execute. |

| Return ||
|---------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| [ParcelFileDescriptor](../android/os/ParcelFileDescriptor.md)! | A file descriptor to the standard output stream. |

**See Also**

- <https://developer.android.com/reference/kotlin/android/app/UiAutomation#adoptShellPermissionIdentity()> 

### executeShellCommandRw

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun executeShellCommandRw(command: String): Array<ParcelFileDescriptor!>
```

Executes a shell command. This method returns two file descriptors, one that points to the standard output stream (element at index 0), and one that points to the standard input stream (element at index 1). The command execution is similar to running "adb shell " from a host connected to the device.

**Note:**It is your responsibility to close the returned file descriptors once you are done reading/writing.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------|
| `command` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The command to execute. This value cannot be`null`. |

| Return ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [ParcelFileDescriptor](../android/os/ParcelFileDescriptor.md)!> | File descriptors (out, in) to the standard output/input streams. This value cannot be`null`. |

### executeShellCommandRwe

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun executeShellCommandRwe(command: String): Array<ParcelFileDescriptor!>
```

Executes a shell command. This method returns three file descriptors, one that points to the standard output stream (element at index 0), one that points to the standard input stream (element at index 1), and one points to standard error stream (element at index 2). The command execution is similar to running "adb shell " from a host connected to the device.

**Note:**It is your responsibility to close the returned file descriptors once you are done reading/writing.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------|
| `command` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The command to execute. This value cannot be`null`. |

| Return ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [ParcelFileDescriptor](../android/os/ParcelFileDescriptor.md)!> | File descriptors (out, in, err) to the standard output/input/error streams. This value cannot be`null`. |

### findFocus

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun findFocus(focus: Int): AccessibilityNodeInfo!
```

Find the view that has the specified focus type. The search is performed across all windows.

**Note:** In order to access the windows you have to opt-in to retrieve the interactive windows by setting the [AccessibilityServiceInfo.FLAG_RETRIEVE_INTERACTIVE_WINDOWS](../android/accessibilityservice/AccessibilityServiceInfo.md) flag. Otherwise, the search will be performed only in the active window.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `focus` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The focus to find. One of [AccessibilityNodeInfo.FOCUS_INPUT](../android/view/accessibility/AccessibilityNodeInfo.md) or [AccessibilityNodeInfo.FOCUS_ACCESSIBILITY](../android/view/accessibility/AccessibilityNodeInfo.md). |

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------|
| [AccessibilityNodeInfo](../android/view/accessibility/AccessibilityNodeInfo.md)! | The node info of the focused view or null. |

| Exceptions ||
|-----------------------------------|----------------------------------------------------------------------|
| `java.lang.IllegalStateException` | If the connection to the accessibility subsystem is not established. |

**See Also**

- [android.view.accessibility.AccessibilityNodeInfo#FOCUS_INPUT](../android/view/accessibility/AccessibilityNodeInfo.md)
- [android.view.accessibility.AccessibilityNodeInfo#FOCUS_ACCESSIBILITY](../android/view/accessibility/AccessibilityNodeInfo.md) 

### getRootInActiveWindow

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getRootInActiveWindow(): AccessibilityNodeInfo!
```

Gets the root [AccessibilityNodeInfo](../android/view/accessibility/AccessibilityNodeInfo.md) in the active window.

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------|----------------|
| [AccessibilityNodeInfo](../android/view/accessibility/AccessibilityNodeInfo.md)! | The root info. |

| Exceptions ||
|-----------------------------------|----------------------------------------------------------------------|
| `java.lang.IllegalStateException` | If the connection to the accessibility subsystem is not established. |

### getServiceInfo

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getServiceInfo(): AccessibilityServiceInfo!
```

Gets the an [AccessibilityServiceInfo](../android/accessibilityservice/AccessibilityServiceInfo.md) describing this UiAutomation. This method is useful if one wants to change some of the dynamically configurable properties at runtime.

| Return ||
|-----------------------------------------------------------------------------------------------------------------------------------------|---------------------------------|
| [AccessibilityServiceInfo](../android/accessibilityservice/AccessibilityServiceInfo.md)! | The accessibility service info. |

| Exceptions ||
|-----------------------------------|----------------------------------------------------------------------|
| `java.lang.IllegalStateException` | If the connection to the accessibility subsystem is not established. |

**See Also**

- [android.accessibilityservice.AccessibilityServiceInfo](../android/accessibilityservice/AccessibilityServiceInfo.md) 

### getWindowAnimationFrameStats

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getWindowAnimationFrameStats(): WindowAnimationFrameStats!
```

**Deprecated:** *animation-frames are no-longer used.*

Gets the window animation frame statistics. These statistics contain information about the most recently rendered window animation frames, i.e. for window transition animations.

A typical usage requires clearing the window animation frame statistics via [clearWindowAnimationFrameStats()](../android/app/UiAutomation.md))followed by an interaction that causes a window transition which uses a window animation and finally getting the window animation frame statistics by calling this method. 

```kotlin
// Start with a clean slate.
  uiAutimation.clearWindowAnimationFrameStats();
 
  // Do stuff to trigger a window transition.
 
  // Get the frame statistics.
  WindowAnimationFrameStats stats = uiAutomation.getWindowAnimationFrameStats();
  
```

| Return ||
|---------------------------------------------------------------------------------------------------------------------------|----------------------------------------|
| [WindowAnimationFrameStats](../android/view/WindowAnimationFrameStats.md)! | The window animation frame statistics. |

**See Also**

- [android.view.WindowAnimationFrameStats](../android/view/WindowAnimationFrameStats.md)
- <https://developer.android.com/reference/kotlin/android/app/UiAutomation#clearWindowAnimationFrameStats()>
- [android.R.styleable#WindowAnimation](../android/R.styleable.md) 

### getWindowContentFrameStats

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getWindowContentFrameStats(windowId: Int): WindowContentFrameStats!
```

Gets the frame statistics for a given window. These statistics contain information about the most recently rendered content frames.

A typical usage requires clearing the window frame statistics via [clearWindowContentFrameStats(int)](../android/app/UiAutomation.md))followed by an interaction with the UI and finally getting the window frame statistics via calling this method. 

```kotlin
// Assume we have at least one window.
  final int windowId = getWindows().get(0).getId();
 
  // Start with a clean slate.
  uiAutimation.clearWindowContentFrameStats(windowId);
 
  // Do stuff with the UI.
 
  // Get the frame statistics.
  WindowContentFrameStats stats = uiAutomation.getWindowContentFrameStats(windowId);
  
```

| Parameters ||
|------------|-------------------------------------------------------------------------------------------|
| `windowId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The window id. |

| Return ||
|-----------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [WindowContentFrameStats](../android/view/WindowContentFrameStats.md)! | The window frame statistics, or null if the window is not present. |

| Exceptions ||
|-----------------------------------|----------------------------------------------------------------------|
| `java.lang.IllegalStateException` | If the connection to the accessibility subsystem is not established. |

**See Also**

- [android.view.WindowContentFrameStats](../android/view/WindowContentFrameStats.md)
- [#clearWindowContentFrameStats(int)](../android/app/UiAutomation.md))
- <https://developer.android.com/reference/kotlin/android/app/UiAutomation#getWindows()>
- [android.view.accessibility.AccessibilityWindowInfo#getId()](../android/view/accessibility/AccessibilityWindowInfo.md)) 

### getWindows

```
fun getWindows(): MutableList<AccessibilityWindowInfo!>!
```

Gets the windows on the screen associated with the [UiAutomation](../android/app/UiAutomation.md) context (usually the [default display).](../android/view/Display.md) 

### getWindowsOnAllDisplays

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getWindowsOnAllDisplays(): SparseArray<MutableList<AccessibilityWindowInfo!>!>
```

Gets the windows on the screen of all displays. This method returns only the windows that a sighted user can interact with, as opposed to all windows. For example, if there is a modal dialog shown and the user cannot touch anything behind it, then only the modal window will be reported (assuming it is the top one). For convenience the returned windows are ordered in a descending layer order, which is the windows that are higher in the Z-order are reported first.

**Note:** In order to access the windows you have to opt-in to retrieve the interactive windows by setting the [AccessibilityServiceInfo.FLAG_RETRIEVE_INTERACTIVE_WINDOWS](../android/accessibilityservice/AccessibilityServiceInfo.md) flag.

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [SparseArray](../android/util/SparseArray.md)< [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [AccessibilityWindowInfo](../android/view/accessibility/AccessibilityWindowInfo.md)!>!> | The windows of all displays if there are windows and the service is can retrieve them, otherwise an empty list. The key of SparseArray is display ID. This value cannot be`null`. |

| Exceptions ||
|-----------------------------------|----------------------------------------------------------------------|
| `java.lang.IllegalStateException` | If the connection to the accessibility subsystem is not established. |

### grantRuntimePermission

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun grantRuntimePermission(
    packageName: String!, 
    permission: String!
): Unit
```

Grants a runtime permission to a package.

| Parameters ||
|---------------|------------------------------------------------------------------------------------------------------------------|
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The package to which to grant. |
| `permission` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The permission to grant. |

| Exceptions ||
|-------------------------------|------------------------------------|
| `java.lang.SecurityException` | if unable to grant the permission. |

### grantRuntimePermissionAsUser

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun grantRuntimePermissionAsUser(
    packageName: String!, 
    permission: String!, 
    userHandle: UserHandle!
): Unit
```

Grants a runtime permission to a package for a user.

| Parameters ||
|---------------|------------------------------------------------------------------------------------------------------------------|
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The package to which to grant. |
| `permission` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The permission to grant. |

| Exceptions ||
|-------------------------------|------------------------------------|
| `java.lang.SecurityException` | if unable to grant the permission. |

### injectInputEvent

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun injectInputEvent(
    event: InputEvent!, 
    sync: Boolean
): Boolean
```

A method for injecting an arbitrary input event. This method waits for all window container animations and surface operations to complete.

**Note:**It is caller's responsibility to recycle the event.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------|
| `event` | [InputEvent](../android/view/InputEvent.md)!:the event to inject |
| `sync` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):whether to inject the event synchronously |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if event injection succeeded |

### performGlobalAction

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun performGlobalAction(action: Int): Boolean
```

Performs a global action. Such an action can be performed at any moment regardless of the current application or user location in that application. For example going back, going home, opening recents, etc.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------|
| `action` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The action to perform. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | Whether the action was successfully performed. |

| Exceptions ||
|-----------------------------------|----------------------------------------------------------------------|
| `java.lang.IllegalStateException` | If the connection to the accessibility subsystem is not established. |

**See Also**

- [android.accessibilityservice.AccessibilityService#GLOBAL_ACTION_BACK](../android/accessibilityservice/AccessibilityService.md)
- [android.accessibilityservice.AccessibilityService#GLOBAL_ACTION_HOME](../android/accessibilityservice/AccessibilityService.md)
- [android.accessibilityservice.AccessibilityService#GLOBAL_ACTION_NOTIFICATIONS](../android/accessibilityservice/AccessibilityService.md)
- [android.accessibilityservice.AccessibilityService#GLOBAL_ACTION_RECENTS](../android/accessibilityservice/AccessibilityService.md) 

### revokeRuntimePermission

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun revokeRuntimePermission(
    packageName: String!, 
    permission: String!
): Unit
```

Revokes a runtime permission from a package.

| Parameters ||
|---------------|------------------------------------------------------------------------------------------------------------------|
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The package to which to grant. |
| `permission` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The permission to grant. |

| Exceptions ||
|-------------------------------|-------------------------------------|
| `java.lang.SecurityException` | if unable to revoke the permission. |

### revokeRuntimePermissionAsUser

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun revokeRuntimePermissionAsUser(
    packageName: String!, 
    permission: String!, 
    userHandle: UserHandle!
): Unit
```

Revokes a runtime permission from a package.

| Parameters ||
|---------------|------------------------------------------------------------------------------------------------------------------|
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The package to which to grant. |
| `permission` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The permission to grant. |

| Exceptions ||
|-------------------------------|-------------------------------------|
| `java.lang.SecurityException` | if unable to revoke the permission. |

### setAnimationScale

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setAnimationScale(scale: Float): Unit
```

Sets the system settings values that control the scaling factor for animations. The scale controls the animation playback speed for animations that respect these settings. Animations that do not respect the settings values will not be affected by this function. A lower scale value results in a faster speed. A value of`0`disables animations entirely. When animations are disabled services receive window change events more quickly which can reduce the potential by confusion by reducing the time during which windows are in transition.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------|
| `scale` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The scaling factor for all animations. |

**See Also**

- [android.view.accessibility.AccessibilityEvent#TYPE_WINDOWS_CHANGED](../android/view/accessibility/AccessibilityEvent.md)
- [android.view.accessibility.AccessibilityEvent#TYPE_WINDOW_STATE_CHANGED](../android/view/accessibility/AccessibilityEvent.md)
- [android.provider.Settings.Global#WINDOW_ANIMATION_SCALE](../android/provider/Settings.Global.md)
- [android.provider.Settings.Global#TRANSITION_ANIMATION_SCALE](../android/provider/Settings.Global.md)
- [android.provider.Settings.Global#ANIMATOR_DURATION_SCALE](../android/provider/Settings.Global.md) 

### setOnAccessibilityEventListener

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setOnAccessibilityEventListener(listener: UiAutomation.OnAccessibilityEventListener!): Unit
```

Sets a callback for observing the stream of [AccessibilityEvent](../android/view/accessibility/AccessibilityEvent.md) s. The callbacks are delivered on the main application thread.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [UiAutomation.OnAccessibilityEventListener](../android/app/UiAutomation.OnAccessibilityEventListener.md)!:The callback. |

| Exceptions ||
|-----------------------------------|----------------------------------------------------------------------|
| `java.lang.IllegalStateException` | If the connection to the accessibility subsystem is not established. |

### setRotation

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setRotation(rotation: Int): Boolean
```

Sets the device rotation. A client can freeze the rotation in desired state or freeze the rotation to its current state or unfreeze the rotation (rotating the device changes its rotation state).

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------|
| `rotation` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The desired rotation. |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | Whether the rotation was set successfully. |

**See Also**

- [#ROTATION_FREEZE_0](../android/app/UiAutomation.md)
- [#ROTATION_FREEZE_90](../android/app/UiAutomation.md)
- [#ROTATION_FREEZE_180](../android/app/UiAutomation.md)
- [#ROTATION_FREEZE_270](../android/app/UiAutomation.md)
- [#ROTATION_FREEZE_CURRENT](../android/app/UiAutomation.md)
- [#ROTATION_UNFREEZE](../android/app/UiAutomation.md) 

### setRunAsMonkey

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setRunAsMonkey(enable: Boolean): Unit
```

Sets whether this UiAutomation to run in a "monkey" mode. Applications can query whether they are executed in a "monkey" mode, i.e. run by a test framework, and avoid doing potentially undesirable actions such as calling 911 or posting on public forums etc.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------|
| `enable` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):whether to run in a "monkey" mode or not. Default is not. |

**See Also**

- [android.app.ActivityManager#isUserAMonkey()](../android/app/ActivityManager.md)) 

### setServiceInfo

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setServiceInfo(info: AccessibilityServiceInfo!): Unit
```

Sets the [AccessibilityServiceInfo](../android/accessibilityservice/AccessibilityServiceInfo.md) that describes how this UiAutomation will be handled by the platform accessibility layer.

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| `info` | [AccessibilityServiceInfo](../android/accessibilityservice/AccessibilityServiceInfo.md)!:The info. |

| Exceptions ||
|-----------------------------------|----------------------------------------------------------------------|
| `java.lang.IllegalStateException` | If the connection to the accessibility subsystem is not established. |

**See Also**

- [android.accessibilityservice.AccessibilityServiceInfo](../android/accessibilityservice/AccessibilityServiceInfo.md) 

### takeScreenshot

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun takeScreenshot(): Bitmap!
```

Takes a screenshot.

| Return ||
|-----------------------------------------------------------------------------------------|---------------------------------------------------|
| [Bitmap](../android/graphics/Bitmap.md)! | The screenshot bitmap on success, null otherwise. |

### takeScreenshot

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun takeScreenshot(window: Window): Bitmap?
```

Used to capture a screenshot of a Window. This can return null in the following cases: 1. Window content hasn't been layed out. 2. Window doesn't have a valid SurfaceControl 3. An error occurred in SurfaceFlinger when trying to take the screenshot.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| `window` | [Window](../android/view/Window.md):Window to take a screenshot of This value cannot be`null`. |

| Return ||
|-----------------------------------------------------------------------------------------|---------------------------------------------------|
| [Bitmap](../android/graphics/Bitmap.md)? | The screenshot bitmap on success, null otherwise. |

### toString

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

### waitForIdle

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun waitForIdle(
    idleTimeoutMillis: Long, 
    globalTimeoutMillis: Long
): Unit
```

Waits for the accessibility event stream to become idle, which is not to have received an accessibility event within`idleTimeoutMillis`. The total time spent to wait for an idle accessibility event stream is bounded by the`globalTimeoutMillis`.

| Parameters ||
|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `idleTimeoutMillis` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The timeout in milliseconds between two events to consider the device idle. |
| `globalTimeoutMillis` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The maximal global timeout in milliseconds in which to wait for an idle state. |

| Exceptions ||
|-----------------------------------------|----------------------------------------------------------------------|
| `java.util.concurrent.TimeoutException` | If no idle state was detected within`globalTimeoutMillis.` |
| `java.lang.IllegalStateException` | If the connection to the accessibility subsystem is not established. |
