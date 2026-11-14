Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ActivityOptions

```
open class ActivityOptions
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.app.ActivityOptions](https://developer.android.com/reference/kotlin/android/app/ActivityOptions#) |

Helper class for building an options Bundle that can be used with `https://developer.android.com/reference/kotlin/android/content/Context.html#startActivity(android.content.Intent,%20android.os.Bundle)` and related methods.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/app/ActivityOptions.LaunchCookie` An opaque token used to track and identify a specific activity launch request. |

| Constants ||
|---|---|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/ActivityOptions#EXTRA_USAGE_TIME_REPORT:kotlin.String` A long in the extras delivered by `https://developer.android.com/reference/kotlin/android/app/ActivityOptions#requestUsageTimeReport(android.app.PendingIntent)` that contains the total time (in ms) the user spent in the app flow. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/ActivityOptions#EXTRA_USAGE_TIME_REPORT_PACKAGES:kotlin.String` A Bundle in the extras delivered by `https://developer.android.com/reference/kotlin/android/app/ActivityOptions#requestUsageTimeReport(android.app.PendingIntent)` that contains detailed information about the time spent in each package associated with the app; each key is a package name, whose value is a long containing the time (in ms). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/ActivityOptions#MODE_BACKGROUND_ACTIVITY_START_ALLOWED:kotlin.Int` Grants the `https://developer.android.com/reference/kotlin/android/app/PendingIntent` background activity start privileges. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/ActivityOptions#MODE_BACKGROUND_ACTIVITY_START_ALLOW_ALWAYS:kotlin.Int` Grants the `https://developer.android.com/reference/kotlin/android/app/PendingIntent` all background activity start privileges, including those normally reserved for privileged contexts (e.g., companion apps or those with the |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/ActivityOptions#MODE_BACKGROUND_ACTIVITY_START_ALLOW_IF_VISIBLE:kotlin.Int` Grants the `https://developer.android.com/reference/kotlin/android/app/PendingIntent` background activity start privileges only when the app has a visible window (i.e., is visible to the user). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/ActivityOptions#MODE_BACKGROUND_ACTIVITY_START_DENIED:kotlin.Int` Denies the `https://developer.android.com/reference/kotlin/android/app/PendingIntent` any background activity start privileges. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/ActivityOptions#MODE_BACKGROUND_ACTIVITY_START_SYSTEM_DEFINED:kotlin.Int` The system determines whether to grant background activity start privileges. |

| Public methods ||
|---|---|
| open [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)? | `https://developer.android.com/reference/kotlin/android/app/ActivityOptions#getLaunchBounds()()` Returns the bounds that should be used to launch the activity. |
| open [ActivityOptions.LaunchCookie](https://developer.android.com/reference/kotlin/android/app/ActivityOptions.LaunchCookie)? | `https://developer.android.com/reference/kotlin/android/app/ActivityOptions#getLaunchCookie()()` Gets the launch cookie associated with these options, if set. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/ActivityOptions#getLaunchDisplayId()()` Gets the id of the display where activity should be launched. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/app/ActivityOptions#getLockTaskMode()()` Gets whether the activity is to be launched into LockTask mode. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/ActivityOptions#getPendingIntentBackgroundActivityStartMode()()` Get the mode for allowing or denying the senders privileges to start background activities to the PendingIntent. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/ActivityOptions#getPendingIntentCreatorBackgroundActivityStartMode()()` Returns the mode to start background activities granted by the creator of the `https://developer.android.com/reference/kotlin/android/app/PendingIntent`. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/ActivityOptions#getSplashScreenStyle()()` Gets the style can be used for cold-launching an activity. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/app/ActivityOptions#isAllowPassThroughOnTouchOutside()()` Returns whether the source activity allows the overlaying activities from the to-be-launched app to pass through touch events to it when touches fall outside the content window. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/app/ActivityOptions#isMovableTaskRequired()()` Gets whether a task in which the activity will be launched is required to be movable right after launch using the `https://developer.android.com/reference/kotlin/android/app/ActivityManager.AppTask#moveTaskTo(android.app.TaskLocation,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)` method. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/app/ActivityOptions#isPendingIntentBackgroundActivityLaunchAllowed()()` Get PendingIntent activity is allowed to be started in the background if the caller can start background activities. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/app/ActivityOptions#isShareIdentityEnabled()()` Returns whether the launching app has opted-in to sharing its identity with the launched activity. |
| open static [ActivityOptions](https://developer.android.com/reference/kotlin/android/app/ActivityOptions#)! | `https://developer.android.com/reference/kotlin/android/app/ActivityOptions#makeBasic()()` Create a basic ActivityOptions that has no special animation associated with it. |
| open static [ActivityOptions](https://developer.android.com/reference/kotlin/android/app/ActivityOptions#)! | `https://developer.android.com/reference/kotlin/android/app/ActivityOptions#makeClipRevealAnimation(android.view.View,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)(source: https://developer.android.com/reference/kotlin/android/view/View.html#!, startX: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, startY: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, width: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, height: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Create an ActivityOptions specifying an animation where the new activity is revealed from a small originating area of the screen to its final full representation. |
| open static [ActivityOptions](https://developer.android.com/reference/kotlin/android/app/ActivityOptions#)! | `https://developer.android.com/reference/kotlin/android/app/ActivityOptions#makeCustomAnimation(android.content.Context,%20kotlin.Int,%20kotlin.Int)(context: https://developer.android.com/reference/kotlin/android/content/Context.html#!, enterResId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, exitResId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Create an ActivityOptions specifying a custom animation to run when the activity is displayed. |
| open static [ActivityOptions](https://developer.android.com/reference/kotlin/android/app/ActivityOptions#) | `https://developer.android.com/reference/kotlin/android/app/ActivityOptions#makeCustomAnimation(android.content.Context,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)(context: https://developer.android.com/reference/kotlin/android/content/Context.html#, enterResId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, exitResId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, backgroundColor: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Create an ActivityOptions specifying a custom animation to run when the activity is displayed. |
| open static [ActivityOptions](https://developer.android.com/reference/kotlin/android/app/ActivityOptions#) | `https://developer.android.com/reference/kotlin/android/app/ActivityOptions#makeLaunchIntoPip(android.app.PictureInPictureParams)(pictureInPictureParams: https://developer.android.com/reference/kotlin/android/app/PictureInPictureParams)` Creates an `https://developer.android.com/reference/kotlin/android/app/ActivityOptions#` instance that launch into picture-in-picture. |
| open static [ActivityOptions](https://developer.android.com/reference/kotlin/android/app/ActivityOptions#)! | `https://developer.android.com/reference/kotlin/android/app/ActivityOptions#makeScaleUpAnimation(android.view.View,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)(source: https://developer.android.com/reference/kotlin/android/view/View.html#!, startX: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, startY: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, width: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, height: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Create an ActivityOptions specifying an animation where the new activity is scaled from a small originating area of the screen to its final full representation. |
| open static [ActivityOptions](https://developer.android.com/reference/kotlin/android/app/ActivityOptions#)! | `https://developer.android.com/reference/kotlin/android/app/ActivityOptions#makeSceneTransitionAnimation(android.app.Activity,%20android.util.Pair)(activity: https://developer.android.com/reference/kotlin/android/app/Activity!, vararg sharedElements: https://developer.android.com/reference/kotlin/android/util/Pair.html#<https://developer.android.com/reference/kotlin/android/view/View.html#!, https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!)` Create an ActivityOptions to transition between Activities using cross-Activity scene animations. |
| open static [ActivityOptions](https://developer.android.com/reference/kotlin/android/app/ActivityOptions#)! | `https://developer.android.com/reference/kotlin/android/app/ActivityOptions#makeSceneTransitionAnimation(android.app.Activity,%20android.view.View,%20kotlin.String)(activity: https://developer.android.com/reference/kotlin/android/app/Activity!, sharedElement: https://developer.android.com/reference/kotlin/android/view/View.html#!, sharedElementName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Create an ActivityOptions to transition between Activities using cross-Activity scene animations. |
| open static [ActivityOptions](https://developer.android.com/reference/kotlin/android/app/ActivityOptions#)! | `https://developer.android.com/reference/kotlin/android/app/ActivityOptions#makeTaskLaunchBehind()()` If set along with Intent. |
| open static [ActivityOptions](https://developer.android.com/reference/kotlin/android/app/ActivityOptions#)! | `https://developer.android.com/reference/kotlin/android/app/ActivityOptions#makeThumbnailScaleUpAnimation(android.view.View,%20android.graphics.Bitmap,%20kotlin.Int,%20kotlin.Int)(source: https://developer.android.com/reference/kotlin/android/view/View.html#!, thumbnail: https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#!, startX: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, startY: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Create an ActivityOptions specifying an animation where a thumbnail is scaled from a given position to the new activity window that is being started. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/ActivityOptions#requestUsageTimeReport(android.app.PendingIntent)(receiver: https://developer.android.com/reference/kotlin/android/app/PendingIntent!)` Ask the system track that time the user spends in the app being launched, and report it back once done. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/ActivityOptions#setAllowPassThroughOnTouchOutside(kotlin.Boolean)(allowed: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Sets whether the source activity allows the overlaying activities from the to-be-launched app to pass through touch events to it when touches fall outside the content window. |
| open [ActivityOptions](https://developer.android.com/reference/kotlin/android/app/ActivityOptions#)! | `https://developer.android.com/reference/kotlin/android/app/ActivityOptions#setAppVerificationBundle(android.os.Bundle)(bundle: https://developer.android.com/reference/kotlin/android/os/Bundle.html#!)` Set the `https://developer.android.com/reference/kotlin/android/os/Bundle.html#` that is provided to the app installer for additional verification if the call to android. |
| open [ActivityOptions](https://developer.android.com/reference/kotlin/android/app/ActivityOptions#)! | `https://developer.android.com/reference/kotlin/android/app/ActivityOptions#setLaunchBounds(android.graphics.Rect)(screenSpacePixelRect: https://developer.android.com/reference/kotlin/android/graphics/Rect.html#?)` Sets the bounds (window size and position) that the activity should be launched in. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/ActivityOptions#setLaunchCookie(android.app.ActivityOptions.LaunchCookie)(launchCookie: https://developer.android.com/reference/kotlin/android/app/ActivityOptions.LaunchCookie?)` Sets a launch cookie to track the `https://developer.android.com/reference/kotlin/android/app/Activity` and task launched as a result of these options. |
| open [ActivityOptions](https://developer.android.com/reference/kotlin/android/app/ActivityOptions#)! | `https://developer.android.com/reference/kotlin/android/app/ActivityOptions#setLaunchDisplayId(kotlin.Int)(launchDisplayId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Sets the id of the display where the activity should be launched. |
| open [ActivityOptions](https://developer.android.com/reference/kotlin/android/app/ActivityOptions#)! | `https://developer.android.com/reference/kotlin/android/app/ActivityOptions#setLockTaskEnabled(kotlin.Boolean)(lockTaskMode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Sets whether the activity is to be launched into LockTask mode. |
| open [ActivityOptions](https://developer.android.com/reference/kotlin/android/app/ActivityOptions#) | `https://developer.android.com/reference/kotlin/android/app/ActivityOptions#setMovableTaskRequired(kotlin.Boolean)(movableTaskRequired: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Sets whether a task in which the activity will be launched is required to be movable right after launch using the `https://developer.android.com/reference/kotlin/android/app/ActivityManager.AppTask#moveTaskTo(android.app.TaskLocation,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)` method. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/ActivityOptions#setPendingIntentBackgroundActivityLaunchAllowed(kotlin.Boolean)(allowed: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Set PendingIntent activity is allowed to be started in the background if the caller can start background activities. |
| open [ActivityOptions](https://developer.android.com/reference/kotlin/android/app/ActivityOptions#) | `https://developer.android.com/reference/kotlin/android/app/ActivityOptions#setPendingIntentBackgroundActivityStartMode(kotlin.Int)(state: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Sets the mode for allowing or denying the senders privileges to start background activities to the PendingIntent. |
| open [ActivityOptions](https://developer.android.com/reference/kotlin/android/app/ActivityOptions#) | `https://developer.android.com/reference/kotlin/android/app/ActivityOptions#setPendingIntentCreatorBackgroundActivityStartMode(kotlin.Int)(mode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Allow a `https://developer.android.com/reference/kotlin/android/app/PendingIntent` to use the privilege of its creator to start background activities. |
| open [ActivityOptions](https://developer.android.com/reference/kotlin/android/app/ActivityOptions#) | `https://developer.android.com/reference/kotlin/android/app/ActivityOptions#setShareIdentityEnabled(kotlin.Boolean)(shareIdentity: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Sets whether the identity of the launching app should be shared with the activity. |
| open [ActivityOptions](https://developer.android.com/reference/kotlin/android/app/ActivityOptions#) | `https://developer.android.com/reference/kotlin/android/app/ActivityOptions#setSplashScreenStyle(kotlin.Int)(style: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Sets the preferred splash screen style of the opening activities. |
| open [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)! | `https://developer.android.com/reference/kotlin/android/app/ActivityOptions#toBundle()()` Returns the created options as a Bundle, which can be passed to `https://developer.android.com/reference/kotlin/android/content/Context.html#startActivity(android.content.Intent,%20android.os.Bundle)` and related methods. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/ActivityOptions#toString()()` Returns a string representation of the object. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/ActivityOptions#update(android.app.ActivityOptions)(otherOptions: https://developer.android.com/reference/kotlin/android/app/ActivityOptions#!)` Update the current values in this ActivityOptions from those supplied in otherOptions. |

## Constants

### EXTRA_USAGE_TIME_REPORT

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_USAGE_TIME_REPORT: String
```

A long in the extras delivered by `https://developer.android.com/reference/kotlin/android/app/ActivityOptions#requestUsageTimeReport(android.app.PendingIntent)` that contains the total time (in ms) the user spent in the app flow.

 Value: "android.activity.usage_time"

### EXTRA_USAGE_TIME_REPORT_PACKAGES

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_USAGE_TIME_REPORT_PACKAGES: String
```

A Bundle in the extras delivered by `https://developer.android.com/reference/kotlin/android/app/ActivityOptions#requestUsageTimeReport(android.app.PendingIntent)` that contains detailed information about the time spent in each package associated with the app; each key is a package name, whose value is a long containing the time (in ms).

 Value: "android.usage_time_packages"

### MODE_BACKGROUND_ACTIVITY_START_ALLOWED

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MODE_BACKGROUND_ACTIVITY_START_ALLOWED: Int
```

**Deprecated:** *Use `https://developer.android.com/reference/kotlin/android/app/ActivityOptions#MODE_BACKGROUND_ACTIVITY_START_ALLOW_IF_VISIBLE:kotlin.Int` to allow starts only when the app is visible or `https://developer.android.com/reference/kotlin/android/app/ActivityOptions#MODE_BACKGROUND_ACTIVITY_START_ALLOW_ALWAYS:kotlin.Int` to allow starts at any time (see [Restrictions on starting activities from the background](https://developer.android.com/guide/components/activities/background-starts)).*

Grants the `https://developer.android.com/reference/kotlin/android/app/PendingIntent` background activity start privileges. This behaves the same as `https://developer.android.com/reference/kotlin/android/app/ActivityOptions#MODE_BACKGROUND_ACTIVITY_START_ALLOW_ALWAYS:kotlin.Int`, except it does not grant background activity launch permissions based on the privileged permission `START_ACTIVITIES_FROM_BACKGROUND`.

 Value: 1

### MODE_BACKGROUND_ACTIVITY_START_ALLOW_ALWAYS

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MODE_BACKGROUND_ACTIVITY_START_ALLOW_ALWAYS: Int
```

Grants the `https://developer.android.com/reference/kotlin/android/app/PendingIntent` all background activity start privileges, including those normally reserved for privileged contexts (e.g., companion apps or those with the `START_ACTIVITIES_FROM_BACKGROUND` permission).

**Caution:** This mode should be used sparingly. Most apps should use `https://developer.android.com/reference/kotlin/android/app/ActivityOptions#MODE_BACKGROUND_ACTIVITY_START_ALLOW_IF_VISIBLE:kotlin.Int` instead, relying on notifications or foreground services for background interactions to minimize user disruption. However, this mode is necessary for specific use cases, such as companion apps responding to prompts from a connected device.

For more information on background activity start restrictions, see: [Restrictions on starting activities from the background](https://developer.android.com/guide/components/activities/background-starts)

 Value: 3

### MODE_BACKGROUND_ACTIVITY_START_ALLOW_IF_VISIBLE

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MODE_BACKGROUND_ACTIVITY_START_ALLOW_IF_VISIBLE: Int
```

Grants the `https://developer.android.com/reference/kotlin/android/app/PendingIntent` background activity start privileges only when the app has a visible window (i.e., is visible to the user). This is the recommended mode for most apps to minimize disruption to the user experience.

For more information on background activity start restrictions, see: [Restrictions on starting activities from the background](https://developer.android.com/guide/components/activities/background-starts)

 Value: 4

### MODE_BACKGROUND_ACTIVITY_START_DENIED

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MODE_BACKGROUND_ACTIVITY_START_DENIED: Int
```

Denies the `https://developer.android.com/reference/kotlin/android/app/PendingIntent` any background activity start privileges.

 Value: 2

### MODE_BACKGROUND_ACTIVITY_START_SYSTEM_DEFINED

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MODE_BACKGROUND_ACTIVITY_START_SYSTEM_DEFINED: Int
```

The system determines whether to grant background activity start privileges. This is the default behavior if no explicit mode is specified.

 Value: 0

## Public methods

### getLaunchBounds

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getLaunchBounds(): Rect?
```

Returns the bounds that should be used to launch the activity.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/Rect.html#?` | Bounds used to launch the activity. This value may be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/ActivityOptions#setLaunchBounds(android.graphics.Rect)`

### getLaunchCookie

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getLaunchCookie(): ActivityOptions.LaunchCookie?
```

Gets the launch cookie associated with these options, if set.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/app/ActivityOptions.LaunchCookie?` | The launch tracking cookie if set, or `null` otherwise. |

### getLaunchDisplayId

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getLaunchDisplayId(): Int
```

Gets the id of the display where activity should be launched.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The id of the display where activity should be launched, `https://developer.android.com/reference/kotlin/android/view/Display.html#INVALID_DISPLAY:kotlin.Int` if not set. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/ActivityOptions#setLaunchDisplayId(kotlin.Int)`

### getLockTaskMode

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getLockTaskMode(): Boolean
```

Gets whether the activity is to be launched into LockTask mode.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the activity is to be launched into LockTask mode. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/Activity#startLockTask()`
- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager#setLockTaskPackages(android.content.ComponentName,%20kotlin.Array)`

### getPendingIntentBackgroundActivityStartMode

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getPendingIntentBackgroundActivityStartMode(): Int
```

Get the mode for allowing or denying the senders privileges to start background activities to the PendingIntent.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is one of the following: - `https://developer.android.com/reference/kotlin/android/app/ActivityOptions#MODE_BACKGROUND_ACTIVITY_START_SYSTEM_DEFINED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/ActivityOptions#MODE_BACKGROUND_ACTIVITY_START_ALLOWED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/ActivityOptions#MODE_BACKGROUND_ACTIVITY_START_DENIED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/ActivityOptions#MODE_BACKGROUND_ACTIVITY_START_ALLOW_ALWAYS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/ActivityOptions#MODE_BACKGROUND_ACTIVITY_START_ALLOW_IF_VISIBLE:kotlin.Int` |

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/ActivityOptions#setPendingIntentBackgroundActivityStartMode(kotlin.Int)`

### getPendingIntentCreatorBackgroundActivityStartMode

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getPendingIntentCreatorBackgroundActivityStartMode(): Int
```

Returns the mode to start background activities granted by the creator of the `https://developer.android.com/reference/kotlin/android/app/PendingIntent`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the mode currently set. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/app/ActivityOptions#MODE_BACKGROUND_ACTIVITY_START_SYSTEM_DEFINED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/ActivityOptions#MODE_BACKGROUND_ACTIVITY_START_ALLOWED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/ActivityOptions#MODE_BACKGROUND_ACTIVITY_START_DENIED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/ActivityOptions#MODE_BACKGROUND_ACTIVITY_START_ALLOW_ALWAYS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/ActivityOptions#MODE_BACKGROUND_ACTIVITY_START_ALLOW_IF_VISIBLE:kotlin.Int` |

### getSplashScreenStyle

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getSplashScreenStyle(): Int
```

Gets the style can be used for cold-launching an activity.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is one of the following: - `https://developer.android.com/reference/kotlin/android/window/SplashScreen.html#SPLASH_SCREEN_STYLE_SOLID_COLOR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/window/SplashScreen.html#SPLASH_SCREEN_STYLE_ICON:kotlin.Int` |

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/ActivityOptions#setSplashScreenStyle(kotlin.Int)`

### isAllowPassThroughOnTouchOutside

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isAllowPassThroughOnTouchOutside(): Boolean
```

Returns whether the source activity allows the overlaying activities from the to-be-launched app to pass through touch events to it when touches fall outside the content window.
**See Also**

- `https://developer.android.com/reference/kotlin/android/app/ActivityOptions#setAllowPassThroughOnTouchOutside(kotlin.Boolean)`

### isMovableTaskRequired

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isMovableTaskRequired(): Boolean
```

Gets whether a task in which the activity will be launched is required to be movable right after launch using the `https://developer.android.com/reference/kotlin/android/app/ActivityManager.AppTask#moveTaskTo(android.app.TaskLocation,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)` method.
**See Also**

- `https://developer.android.com/reference/kotlin/android/app/ActivityOptions#setMovableTaskRequired(kotlin.Boolean)`

### isPendingIntentBackgroundActivityLaunchAllowed

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isPendingIntentBackgroundActivityLaunchAllowed(): Boolean
```

**Deprecated:** *use `https://developer.android.com/reference/kotlin/android/app/ActivityOptions#getPendingIntentBackgroundActivityStartMode()` since for apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#UPSIDE_DOWN_CAKE:kotlin.Int` or higher this value might not match the actual behavior if the value was not explicitly set.*

Get PendingIntent activity is allowed to be started in the background if the caller can start background activities.

### isShareIdentityEnabled

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isShareIdentityEnabled(): Boolean
```

Returns whether the launching app has opted-in to sharing its identity with the launched activity.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the launching app has opted-in to sharing its identity |

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/ActivityOptions#setShareIdentityEnabled(kotlin.Boolean)`
- `https://developer.android.com/reference/kotlin/android/app/Activity#getLaunchedFromUid()`
- `https://developer.android.com/reference/kotlin/android/app/Activity#getLaunchedFromPackage()`

### makeBasic

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun makeBasic(): ActivityOptions!
```

Create a basic ActivityOptions that has no special animation associated with it. Other options can still be set.

### makeClipRevealAnimation

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun makeClipRevealAnimation(
    source: View!, 
    startX: Int, 
    startY: Int, 
    width: Int, 
    height: Int
): ActivityOptions!
```

Create an ActivityOptions specifying an animation where the new activity is revealed from a small originating area of the screen to its final full representation.

| Parameters ||
|---|---|
| `source` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!: The View that the new activity is animating from. This defines the coordinate space for startX and startY. |
| `startX` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The x starting location of the new activity, relative to source. |
| `startY` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The y starting location of the activity, relative to source. |
| `width` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The initial width of the new activity. |
| `height` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The initial height of the new activity. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/app/ActivityOptions#!` | Returns a new ActivityOptions object that you can use to supply these options as the options Bundle when starting an activity. |

### makeCustomAnimation

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun makeCustomAnimation(
    context: Context!, 
    enterResId: Int, 
    exitResId: Int
): ActivityOptions!
```

Create an ActivityOptions specifying a custom animation to run when the activity is displayed.

| Parameters ||
|---|---|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!: Who is defining this. This is the application that the animation resources will be loaded from. |
| `enterResId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): A resource ID of the animation resource to use for the incoming activity. Use 0 for no animation. |
| `exitResId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): A resource ID of the animation resource to use for the outgoing activity. Use 0 for no animation. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/app/ActivityOptions#!` | Returns a new ActivityOptions object that you can use to supply these options as the options Bundle when starting an activity. |

### makeCustomAnimation

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun makeCustomAnimation(
    context: Context, 
    enterResId: Int, 
    exitResId: Int, 
    backgroundColor: Int
): ActivityOptions
```

Create an ActivityOptions specifying a custom animation to run when the activity is displayed.

| Parameters ||
|---|---|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#): Who is defining this. This is the application that the animation resources will be loaded from. This value cannot be `null`. |
| `enterResId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): A resource ID of the animation resource to use for the incoming activity. Use 0 for no animation. |
| `exitResId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): A resource ID of the animation resource to use for the outgoing activity. Use 0 for no animation. |
| `backgroundColor` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The background color to use for the background during the animation if the animation requires a background. Set to 0 to not override the default color. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/app/ActivityOptions#` | Returns a new ActivityOptions object that you can use to supply these options as the options Bundle when starting an activity. This value cannot be `null`. |

### makeLaunchIntoPip

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun makeLaunchIntoPip(pictureInPictureParams: PictureInPictureParams): ActivityOptions
```

Creates an `https://developer.android.com/reference/kotlin/android/app/ActivityOptions#` instance that launch into picture-in-picture. This is normally used by a Host activity to start another activity that will directly enter picture-in-picture upon its creation.

| Parameters ||
|---|---|
| `pictureInPictureParams` | [PictureInPictureParams](https://developer.android.com/reference/kotlin/android/app/PictureInPictureParams): `https://developer.android.com/reference/kotlin/android/app/PictureInPictureParams` for launching the Activity to picture-in-picture mode. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/app/ActivityOptions#` | This value cannot be `null`. |

### makeScaleUpAnimation

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun makeScaleUpAnimation(
    source: View!, 
    startX: Int, 
    startY: Int, 
    width: Int, 
    height: Int
): ActivityOptions!
```

Create an ActivityOptions specifying an animation where the new activity is scaled from a small originating area of the screen to its final full representation.

If the Intent this is being used with has not set its `https://developer.android.com/reference/kotlin/android/content/Intent.html#setSourceBounds(android.graphics.Rect)`, those bounds will be filled in for you based on the initial bounds passed in here.

| Parameters ||
|---|---|
| `source` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!: The View that the new activity is animating from. This defines the coordinate space for startX and startY. |
| `startX` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The x starting location of the new activity, relative to source. |
| `startY` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The y starting location of the activity, relative to source. |
| `width` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The initial width of the new activity. |
| `height` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The initial height of the new activity. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/app/ActivityOptions#!` | Returns a new ActivityOptions object that you can use to supply these options as the options Bundle when starting an activity. |

### makeSceneTransitionAnimation

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
@SafeVarargs open static fun makeSceneTransitionAnimation(
    activity: Activity!, 
    vararg sharedElements: Pair<View!, String!>!
): ActivityOptions!
```

Create an ActivityOptions to transition between Activities using cross-Activity scene animations. This method carries the position of multiple shared elements to the started Activity. The position of the first element in sharedElements will be used as the epicenter for the exit Transition. The position of the associated shared element in the launched Activity will be the epicenter of its entering Transition.

This requires `https://developer.android.com/reference/kotlin/android/view/Window.html#FEATURE_ACTIVITY_TRANSITIONS:kotlin.Int` to be enabled on the calling Activity to cause an exit transition. The same must be in the called Activity to get an entering transition.

| Parameters ||
|---|---|
| `activity` | [Activity](https://developer.android.com/reference/kotlin/android/app/Activity)!: The Activity whose window contains the shared elements. |
| `sharedElements` | [Pair](https://developer.android.com/reference/kotlin/android/util/Pair.html#)\< [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!, [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!: The names of the shared elements to transfer to the called Activity and their associated Views. The Views must each have a unique shared element name. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/app/ActivityOptions#!` | Returns a new ActivityOptions object that you can use to supply these options as the options Bundle when starting an activity. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/transition/Transition.html#setEpicenterCallback(android.transition.Transition.EpicenterCallback)`

### makeSceneTransitionAnimation

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun makeSceneTransitionAnimation(
    activity: Activity!, 
    sharedElement: View!, 
    sharedElementName: String!
): ActivityOptions!
```

Create an ActivityOptions to transition between Activities using cross-Activity scene animations. This method carries the position of one shared element to the started Activity. The position of `sharedElement` will be used as the epicenter for the exit Transition. The position of the shared element in the launched Activity will be the epicenter of its entering Transition.

This requires `https://developer.android.com/reference/kotlin/android/view/Window.html#FEATURE_ACTIVITY_TRANSITIONS:kotlin.Int` to be enabled on the calling Activity to cause an exit transition. The same must be in the called Activity to get an entering transition.

| Parameters ||
|---|---|
| `activity` | [Activity](https://developer.android.com/reference/kotlin/android/app/Activity)!: The Activity whose window contains the shared elements. |
| `sharedElement` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!: The View to transition to the started Activity. |
| `sharedElementName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The shared element name as used in the target Activity. This must not be null. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/app/ActivityOptions#!` | Returns a new ActivityOptions object that you can use to supply these options as the options Bundle when starting an activity. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/transition/Transition.html#setEpicenterCallback(android.transition.Transition.EpicenterCallback)`

### makeTaskLaunchBehind

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun makeTaskLaunchBehind(): ActivityOptions!
```

**Deprecated:** *This method is deprecated because starting an Activity behind the current task lacks transparency and violates user expectations. **Alternative:** Start the target Activity, then immediately call `https://developer.android.com/reference/kotlin/android/app/ActivityManager.AppTask#moveToFront()` on the **caller's task** to restore its foreground focus.*

If set along with Intent.FLAG_ACTIVITY_NEW_DOCUMENT then the task being launched will not be presented to the user but will instead be only available through the recents task list. In addition, the new task wil be affiliated with the launching activity's task. Affiliated tasks are grouped together in the recents task list.

This behavior is not supported for activities with `https://developer.android.com/reference/kotlin/android/R.styleable.html#AndroidManifestActivity_launchMode:kotlin.Int` values of `singleInstance` or `singleTask`.

### makeThumbnailScaleUpAnimation

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun makeThumbnailScaleUpAnimation(
    source: View!, 
    thumbnail: Bitmap!, 
    startX: Int, 
    startY: Int
): ActivityOptions!
```

Create an ActivityOptions specifying an animation where a thumbnail is scaled from a given position to the new activity window that is being started.

If the Intent this is being used with has not set its `https://developer.android.com/reference/kotlin/android/content/Intent.html#setSourceBounds(android.graphics.Rect)`, those bounds will be filled in for you based on the initial thumbnail location and size provided here.

| Parameters ||
|---|---|
| `source` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!: The View that this thumbnail is animating from. This defines the coordinate space for startX and startY. |
| `thumbnail` | [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#)!: The bitmap that will be shown as the initial thumbnail of the animation. |
| `startX` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The x starting location of the bitmap, relative to source. |
| `startY` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The y starting location of the bitmap, relative to source. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/app/ActivityOptions#!` | Returns a new ActivityOptions object that you can use to supply these options as the options Bundle when starting an activity. |

### requestUsageTimeReport

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun requestUsageTimeReport(receiver: PendingIntent!): Unit
```

Ask the system track that time the user spends in the app being launched, and report it back once done. The report will be sent to the given receiver, with the extras `https://developer.android.com/reference/kotlin/android/app/ActivityOptions#EXTRA_USAGE_TIME_REPORT:kotlin.String` and `https://developer.android.com/reference/kotlin/android/app/ActivityOptions#EXTRA_USAGE_TIME_REPORT_PACKAGES:kotlin.String` filled in.

The time interval tracked is from launching this activity until the user leaves that activity's flow. They are considered to stay in the flow as long as new activities are being launched or returned to from the original flow, even if this crosses package or task boundaries. For example, if the originator starts an activity to view an image, and while there the user selects to share, which launches their email app in a new task, and they complete the share, the time during that entire operation will be included until they finally hit back from the original image viewer activity.

The user is considered to complete a flow once they switch to another activity that is not part of the tracked flow. This may happen, for example, by using the notification shade, launcher, or recents to launch or switch to another app. Simply going in to these navigation elements does not break the flow (although the launcher and recents stops time tracking of the session); it is the act of going somewhere else that completes the tracking.

| Parameters ||
|---|---|
| `receiver` | [PendingIntent](https://developer.android.com/reference/kotlin/android/app/PendingIntent)!: A broadcast receiver that willl receive the report. |

### setAllowPassThroughOnTouchOutside

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setAllowPassThroughOnTouchOutside(allowed: Boolean): Unit
```

Sets whether the source activity allows the overlaying activities from the to-be-launched app to pass through touch events to it when touches fall outside the content window.

By default, touches that fall on a translucent non-touchable area of an overlaying activity window may be blocked from passing through to the activity below (source activity), unless the overlaying activity is from the same UID as the source activity. The source activity may use this method to opt in and allow the overlaying activities from the to-be-launched app to pass through touches to itself. The source activity needs to ensure that it trusts the overlaying activity and its content is not vulnerable to UI redressing attacks. The flag is ignored if the context calling `https://developer.android.com/reference/kotlin/android/content/Context.html#startActivity(android.content.Intent,%20android.os.Bundle)` is not an activity.

Apps with target SDK 36 and above that depend on cross-uid pass-through touches must opt in to ensure that pass-through touches work correctly.

For backward compatibility, apps with target SDK 35 and below may still receive pass-through touches without opt-in if the cross-uid activity is launched by the source activity.

### setAppVerificationBundle

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setAppVerificationBundle(bundle: Bundle!): ActivityOptions!
```

Set the `https://developer.android.com/reference/kotlin/android/os/Bundle.html#` that is provided to the app installer for additional verification if the call to android.content.Context#startActivity results in an app being installed. This Bundle is not provided to any other app besides the installer.

### setLaunchBounds

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setLaunchBounds(screenSpacePixelRect: Rect?): ActivityOptions!
```

Sets the bounds (window size and position) that the activity should be launched in. Rect position should be provided in pixels and in screen coordinates.

**NOTE:** This value is ignored on devices that don't have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_FREEFORM_WINDOW_MANAGEMENT:kotlin.String` or `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_PICTURE_IN_PICTURE:kotlin.String` enabled, and on displays that don't support freeform and PiP windows.

| Parameters ||
|---|---|
| `screenSpacePixelRect` | [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)?: launch bounds. This value may be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/app/ActivityOptions#!` | `this` `https://developer.android.com/reference/kotlin/android/app/ActivityOptions#` instance |

### setLaunchCookie

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setLaunchCookie(launchCookie: ActivityOptions.LaunchCookie?): Unit
```

Sets a launch cookie to track the `https://developer.android.com/reference/kotlin/android/app/Activity` and task launched as a result of these options.

If the launched activity is a trampoline that starts another activity immediately, the cookie will be transferred to the next activity.

| Parameters ||
|---|---|
| `launchCookie` | [ActivityOptions.LaunchCookie](https://developer.android.com/reference/kotlin/android/app/ActivityOptions.LaunchCookie)?: the unique cookie to associate with this launch, or `null` to clear |

### setLaunchDisplayId

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setLaunchDisplayId(launchDisplayId: Int): ActivityOptions!
```

Sets the id of the display where the activity should be launched. An app can launch activities on public displays or displays where the app already has activities. Otherwise, trying to launch on a display for which `https://developer.android.com/reference/kotlin/android/app/ActivityManager#isActivityStartAllowedOnDisplay(android.content.Context,%20kotlin.Int,%20android.content.Intent)` returns `false` (such as a private display or providing an invalid display id) will result in an exception.

Setting launch display id will be ignored on devices that don't have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_ACTIVITIES_ON_SECONDARY_DISPLAYS:kotlin.String`.

| Parameters ||
|---|---|
| `launchDisplayId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The id of the display where the activity should be launched. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/app/ActivityOptions#!` | `this` `https://developer.android.com/reference/kotlin/android/app/ActivityOptions#` instance. |

### setLockTaskEnabled

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setLockTaskEnabled(lockTaskMode: Boolean): ActivityOptions!
```

Sets whether the activity is to be launched into LockTask mode. Use this option to start an activity in LockTask mode. Note that only apps permitted by `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager` can run in LockTask mode. Therefore, if `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager#isLockTaskPermitted(kotlin.String)` returns `false` for the package of the target activity, a `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#` will be thrown during `https://developer.android.com/reference/kotlin/android/content/Context.html#startActivity(android.content.Intent,%20android.os.Bundle)`. This method doesn't affect activities that are already running --- relaunch the activity to run in lock task mode. Defaults to `false` if not set.

| Parameters ||
|---|---|
| `lockTaskMode` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): `true` if the activity is to be launched into LockTask mode. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/app/ActivityOptions#!` | `this` `https://developer.android.com/reference/kotlin/android/app/ActivityOptions#` instance. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/Activity#startLockTask()`
- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager#setLockTaskPackages(android.content.ComponentName,%20kotlin.Array)`

### setMovableTaskRequired

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setMovableTaskRequired(movableTaskRequired: Boolean): ActivityOptions
```

Sets whether a task in which the activity will be launched is required to be movable right after launch using the `https://developer.android.com/reference/kotlin/android/app/ActivityManager.AppTask#moveTaskTo(android.app.TaskLocation,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)` method. If the system cannot guarantee this, the android.content.Context#startActivity call will throw an `https://developer.android.com/reference/kotlin/android/app/InfeasibleActivityOptionsException`.

Defaults to `false`, if not set.

This option will cause the android.content.Context#startActivity call to throw an `https://developer.android.com/reference/kotlin/android/app/InfeasibleActivityOptionsException` if the activity is not launched in a new task. For more information about how the host task of a new activity is determined, see the [guide on task management](https://developer.android.com/guide/components/activities/tasks-and-back-stack#ManagingTasks). 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#REPOSITION_SELF_WINDOWS:kotlin.String`

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/app/ActivityOptions#` | This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/ActivityManager.AppTask#moveTaskTo(android.app.TaskLocation,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)`

### setPendingIntentBackgroundActivityLaunchAllowed

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setPendingIntentBackgroundActivityLaunchAllowed(allowed: Boolean): Unit
```

**Deprecated:** *use #setPendingIntentBackgroundActivityStartMode(int) to set the full range of states*

Set PendingIntent activity is allowed to be started in the background if the caller can start background activities.

### setPendingIntentBackgroundActivityStartMode

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setPendingIntentBackgroundActivityStartMode(state: Int): ActivityOptions
```

Sets the mode for allowing or denying the senders privileges to start background activities to the PendingIntent. This is typically used in when executing `https://developer.android.com/reference/kotlin/android/app/PendingIntent#send(android.content.Context,%20kotlin.Int,%20android.content.Intent,%20android.app.PendingIntent.OnFinished,%20android.os.Handler,%20kotlin.String,%20android.os.Bundle)` or similar methods. A privileged sender of a PendingIntent should only grant `https://developer.android.com/reference/kotlin/android/app/ActivityOptions#MODE_BACKGROUND_ACTIVITY_START_ALLOWED:kotlin.Int` if the PendingIntent is from a trusted source and/or executed on behalf the user.

| Parameters ||
|---|---|
| `state` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Value is one of the following: - `https://developer.android.com/reference/kotlin/android/app/ActivityOptions#MODE_BACKGROUND_ACTIVITY_START_SYSTEM_DEFINED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/ActivityOptions#MODE_BACKGROUND_ACTIVITY_START_ALLOWED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/ActivityOptions#MODE_BACKGROUND_ACTIVITY_START_DENIED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/ActivityOptions#MODE_BACKGROUND_ACTIVITY_START_ALLOW_ALWAYS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/ActivityOptions#MODE_BACKGROUND_ACTIVITY_START_ALLOW_IF_VISIBLE:kotlin.Int` |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/app/ActivityOptions#` | This value cannot be `null`. |

### setPendingIntentCreatorBackgroundActivityStartMode

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setPendingIntentCreatorBackgroundActivityStartMode(mode: Int): ActivityOptions
```

Allow a `https://developer.android.com/reference/kotlin/android/app/PendingIntent` to use the privilege of its creator to start background activities.

| Parameters ||
|---|---|
| `mode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the mode being set. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/app/ActivityOptions#MODE_BACKGROUND_ACTIVITY_START_SYSTEM_DEFINED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/ActivityOptions#MODE_BACKGROUND_ACTIVITY_START_ALLOWED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/ActivityOptions#MODE_BACKGROUND_ACTIVITY_START_DENIED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/ActivityOptions#MODE_BACKGROUND_ACTIVITY_START_ALLOW_ALWAYS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/ActivityOptions#MODE_BACKGROUND_ACTIVITY_START_ALLOW_IF_VISIBLE:kotlin.Int` |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/app/ActivityOptions#` | This value cannot be `null`. |

### setShareIdentityEnabled

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setShareIdentityEnabled(shareIdentity: Boolean): ActivityOptions
```

Sets whether the identity of the launching app should be shared with the activity.

Use this option when starting an activity that needs to know the identity of the launching app; with this set to `true`, the activity will have access to the launching app's package name and uid.

Defaults to `false` if not set.

Note, even if the launching app does not explicitly enable sharing of its identity, if the activity is started with `Activity#startActivityForResult`, then `https://developer.android.com/reference/kotlin/android/app/Activity#getCallingPackage()` will still return the launching app's package name to allow validation of the result's recipient. Also, an activity running within a package signed by the same key used to sign the platform (some system apps such as Settings will be signed with the platform's key) will have access to the launching app's identity.

| Parameters ||
|---|---|
| `shareIdentity` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): whether the launching app's identity should be shared with the activity |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/app/ActivityOptions#` | `this` `https://developer.android.com/reference/kotlin/android/app/ActivityOptions#` instance. This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/Activity#getLaunchedFromPackage()`
- `https://developer.android.com/reference/kotlin/android/app/Activity#getLaunchedFromUid()`

### setSplashScreenStyle

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setSplashScreenStyle(style: Int): ActivityOptions
```

Sets the preferred splash screen style of the opening activities. This only applies if the Activity or Process is not yet created.

| Parameters ||
|---|---|
| `style` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Can be either `https://developer.android.com/reference/kotlin/android/window/SplashScreen.html#SPLASH_SCREEN_STYLE_ICON:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/window/SplashScreen.html#SPLASH_SCREEN_STYLE_SOLID_COLOR:kotlin.Int` Value is one of the following: - `https://developer.android.com/reference/kotlin/android/window/SplashScreen.html#SPLASH_SCREEN_STYLE_SOLID_COLOR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/window/SplashScreen.html#SPLASH_SCREEN_STYLE_ICON:kotlin.Int` |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/app/ActivityOptions#` | This value cannot be `null`. |

### toBundle

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun toBundle(): Bundle!
```

Returns the created options as a Bundle, which can be passed to `https://developer.android.com/reference/kotlin/android/content/Context.html#startActivity(android.content.Intent,%20android.os.Bundle)` and related methods. Note that the returned Bundle is still owned by the ActivityOptions object; you must not modify it, but can supply it to the startActivity methods that take an options Bundle.

### toString

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun toString(): String
```

Returns a string representation of the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the object. |

### update

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun update(otherOptions: ActivityOptions!): Unit
```

Update the current values in this ActivityOptions from those supplied in otherOptions. Any values defined in otherOptions replace those in the base options.
