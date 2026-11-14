Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ActivityInfo

```
open class ActivityInfo : ComponentInfo, Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [android.content.pm.PackageItemInfo](../android/content/pm/PackageItemInfo.md) |||
| | ↳ | [android.content.pm.ComponentInfo](../android/content/pm/ComponentInfo.md) ||
| | | ↳ | [android.content.pm.ActivityInfo](../android/content/pm/ActivityInfo.md) |
| --- | --- | --- | --- |

Information you can retrieve about a particular application activity or receiver. This corresponds to information collected from the AndroidManifest.xml's \<activity\> and \<receiver\> tags.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.WindowLayout` Contains information about position and size of the activity on the display. |

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#COLOR_MODE_DEFAULT:kotlin.Int` Value for `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#colorMode:kotlin.Int` indicating that the activity should use the default color mode (sRGB, low dynamic range). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#COLOR_MODE_HDR:kotlin.Int` Value of `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#colorMode:kotlin.Int` indicating that the activity should use a high dynamic range if the presentation display supports it. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#COLOR_MODE_WIDE_COLOR_GAMUT:kotlin.Int` Value of `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#colorMode:kotlin.Int` indicating that the activity should use a wide color gamut if the presentation display supports it. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#CONFIG_ASSETS_PATHS:kotlin.Int` Bit in `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#configChanges:kotlin.Int` that indicates that the activity can itself handle asset path changes. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#CONFIG_COLOR_MODE:kotlin.Int` Bit in `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#configChanges:kotlin.Int` that indicates that the activity can itself handle the change to the display color gamut or dynamic range. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#CONFIG_DENSITY:kotlin.Int` Bit in `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#configChanges:kotlin.Int` that indicates that the activity can itself handle density changes. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#CONFIG_FONT_SCALE:kotlin.Int` Bit in `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#configChanges:kotlin.Int` that indicates that the activity can itself handle changes to the font scaling factor. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#CONFIG_FONT_WEIGHT_ADJUSTMENT:kotlin.Int` Bit in `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#configChanges:kotlin.Int` that indicates that the activity can itself handle changes to font weight. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#CONFIG_GRAMMATICAL_GENDER:kotlin.Int` Bit in `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#configChanges:kotlin.Int` that indicates that the activity can itself handle the change to gender. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#CONFIG_KEYBOARD:kotlin.Int` Bit in `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#configChanges:kotlin.Int` that indicates that the activity can itself handle changes to the keyboard type. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#CONFIG_KEYBOARD_HIDDEN:kotlin.Int` Bit in `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#configChanges:kotlin.Int` that indicates that the activity can itself handle changes to the keyboard or navigation being hidden/exposed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#CONFIG_LAYOUT_DIRECTION:kotlin.Int` Bit in `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#configChanges:kotlin.Int` that indicates that the activity can itself handle the change to layout direction. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#CONFIG_LOCALE:kotlin.Int` Bit in `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#configChanges:kotlin.Int` that indicates that the activity can itself handle changes to the locale. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#CONFIG_MCC:kotlin.Int` Bit in `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#configChanges:kotlin.Int` that indicates that the activity can itself handle changes to the IMSI MCC. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#CONFIG_MNC:kotlin.Int` Bit in `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#configChanges:kotlin.Int` that indicates that the activity can itself handle changes to the IMSI MNC. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#CONFIG_NAVIGATION:kotlin.Int` Bit in `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#configChanges:kotlin.Int` that indicates that the activity can itself handle changes to the navigation type. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#CONFIG_ORIENTATION:kotlin.Int` Bit in `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#configChanges:kotlin.Int` that indicates that the activity can itself handle changes to the screen orientation. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#CONFIG_RESOURCES_UNUSED:kotlin.Int` This is probably not the constant you want, the resources compiler supports a less dangerous version of it, 'allKnown', that only suppresses all currently existing configuration change restarts depending on your target SDK rather than whatever the latest SDK supports, allowing the application to work with resources on future Platform versions. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#CONFIG_SCREEN_LAYOUT:kotlin.Int` Bit in `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#configChanges:kotlin.Int` that indicates that the activity can itself handle changes to the screen layout. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#CONFIG_SCREEN_SIZE:kotlin.Int` Bit in `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#configChanges:kotlin.Int` that indicates that the activity can itself handle the screen size. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#CONFIG_SMALLEST_SCREEN_SIZE:kotlin.Int` Bit in `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#configChanges:kotlin.Int` that indicates that the activity can itself handle the smallest screen size. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#CONFIG_TOUCHSCREEN:kotlin.Int` Bit in `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#configChanges:kotlin.Int` that indicates that the activity can itself handle changes to the touchscreen type. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#CONFIG_UI_MODE:kotlin.Int` Bit in `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#configChanges:kotlin.Int` that indicates that the activity can itself handle the ui mode. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#DOCUMENT_LAUNCH_ALWAYS:kotlin.Int` Constant corresponding to `always` in the `https://developer.android.com/reference/kotlin/android/R.attr.html#documentLaunchMode:kotlin.Int` attribute. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#DOCUMENT_LAUNCH_INTO_EXISTING:kotlin.Int` Constant corresponding to `intoExisting` in the `https://developer.android.com/reference/kotlin/android/R.attr.html#documentLaunchMode:kotlin.Int` attribute. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#DOCUMENT_LAUNCH_NEVER:kotlin.Int` Constant corresponding to `never` in the `https://developer.android.com/reference/kotlin/android/R.attr.html#documentLaunchMode:kotlin.Int` attribute. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#DOCUMENT_LAUNCH_NONE:kotlin.Int` Constant corresponding to `none` in the `https://developer.android.com/reference/kotlin/android/R.attr.html#documentLaunchMode:kotlin.Int` attribute. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#FLAG_ALLOW_TASK_REPARENTING:kotlin.Int` Bit in `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#flags:kotlin.Int` that indicates that the activity can be moved between tasks based on its task affinity. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#FLAG_ALLOW_UNTRUSTED_ACTIVITY_EMBEDDING:kotlin.Int` Bit in `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#flags:kotlin.Int`: If set, indicates that the activity can be embedded by untrusted hosts. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#FLAG_ALWAYS_RETAIN_TASK_STATE:kotlin.Int` Bit in `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#flags:kotlin.Int` indicating that, when the activity is the root of a task, that task's stack should never be cleared when it is relaunched from home. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#FLAG_AUTO_REMOVE_FROM_RECENTS:kotlin.Int` Bit in `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#flags:kotlin.Int` indicating that tasks started with this activity are to be removed from the recent list of tasks when the last activity in the task is finished. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#FLAG_CLEAR_TASK_ON_LAUNCH:kotlin.Int` Bit in `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#flags:kotlin.Int` indicating that, when the activity is the root of a task, that task's stack should be cleared each time the user re-launches it from home. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#FLAG_ENABLE_VR_MODE:kotlin.Int` Bit in `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#flags:kotlin.Int` indicating that this activity should be run with VR mode enabled. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#FLAG_EXCLUDE_FROM_RECENTS:kotlin.Int` Bit in `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#flags:kotlin.Int` that indicates that the activity should not appear in the list of recently launched activities. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#FLAG_FINISH_ON_CLOSE_SYSTEM_DIALOGS:kotlin.Int` Bit in `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#flags:kotlin.Int` indicating that, when a request to close system windows happens, this activity is finished. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#FLAG_FINISH_ON_TASK_LAUNCH:kotlin.Int` Bit in `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#flags:kotlin.Int` indicating that, when the activity's task is relaunched from home, this activity should be finished. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#FLAG_HARDWARE_ACCELERATED:kotlin.Int` Value for `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#flags:kotlin.Int`: true when the application's rendering should be hardware accelerated. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#FLAG_IMMERSIVE:kotlin.Int` Bit in `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#flags:kotlin.Int` corresponding to an immersive activity that wishes not to be interrupted by notifications. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#FLAG_MULTIPROCESS:kotlin.Int` Bit in `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#flags:kotlin.Int` indicating whether this activity is able to run in multiple processes. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#FLAG_NO_HISTORY:kotlin.Int` Bit in `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#flags:kotlin.Int` indicating that, when the user navigates away from an activity, it should be finished. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#FLAG_PREFER_MINIMAL_POST_PROCESSING:kotlin.Int` Bit in `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#flags:kotlin.Int` indicating whether the display should preferably be switched to a minimal post processing mode. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#FLAG_RELINQUISH_TASK_IDENTITY:kotlin.Int` Bit in `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#flags:kotlin.Int`: If set, a task rooted at this activity will have its baseIntent replaced by the activity immediately above this. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#FLAG_RESUME_WHILE_PAUSING:kotlin.Int` Bit in `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#flags:kotlin.Int` indicating that this activity can start is creation/resume while the previous activity is still pausing. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#FLAG_SINGLE_USER:kotlin.Int` Bit in `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#flags:kotlin.Int`: If set, a single instance of the receiver will run for all users on the device. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#FLAG_STATE_NOT_NEEDED:kotlin.Int` Bit in `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#flags:kotlin.Int` indicating that the activity's state is not required to be saved, so that if there is a failure the activity will not be removed from the activity stack. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#LAUNCH_MULTIPLE:kotlin.Int` Constant corresponding to `standard` in the `https://developer.android.com/reference/kotlin/android/R.attr.html#launchMode:kotlin.Int` attribute. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#LAUNCH_SINGLE_INSTANCE:kotlin.Int` Constant corresponding to `singleInstance` in the `https://developer.android.com/reference/kotlin/android/R.attr.html#launchMode:kotlin.Int` attribute. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#LAUNCH_SINGLE_INSTANCE_PER_TASK:kotlin.Int` Constant corresponding to `singleInstancePerTask` in the `https://developer.android.com/reference/kotlin/android/R.attr.html#launchMode:kotlin.Int` attribute. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#LAUNCH_SINGLE_TASK:kotlin.Int` Constant corresponding to `singleTask` in the `https://developer.android.com/reference/kotlin/android/R.attr.html#launchMode:kotlin.Int` attribute. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#LAUNCH_SINGLE_TOP:kotlin.Int` Constant corresponding to `singleTop` in the `https://developer.android.com/reference/kotlin/android/R.attr.html#launchMode:kotlin.Int` attribute. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#PERSIST_ACROSS_REBOOTS:kotlin.Int` Constant corresponding to `persistAcrossReboots` in the `https://developer.android.com/reference/kotlin/android/R.attr.html#persistableMode:kotlin.Int` attribute. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#PERSIST_NEVER:kotlin.Int` Constant corresponding to `doNotPersist` in the `https://developer.android.com/reference/kotlin/android/R.attr.html#persistableMode:kotlin.Int` attribute. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#PERSIST_ROOT_ONLY:kotlin.Int` Constant corresponding to `persistRootOnly` in the `https://developer.android.com/reference/kotlin/android/R.attr.html#persistableMode:kotlin.Int` attribute. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#SCREEN_ORIENTATION_BEHIND:kotlin.Int` Constant corresponding to `behind` in the `https://developer.android.com/reference/kotlin/android/R.attr.html#screenOrientation:kotlin.Int` attribute. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#SCREEN_ORIENTATION_FULL_SENSOR:kotlin.Int` Constant corresponding to `fullSensor` in the `https://developer.android.com/reference/kotlin/android/R.attr.html#screenOrientation:kotlin.Int` attribute. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#SCREEN_ORIENTATION_FULL_USER:kotlin.Int` Constant corresponding to `fullUser` in the `https://developer.android.com/reference/kotlin/android/R.attr.html#screenOrientation:kotlin.Int` attribute. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#SCREEN_ORIENTATION_LANDSCAPE:kotlin.Int` Constant corresponding to `landscape` in the `https://developer.android.com/reference/kotlin/android/R.attr.html#screenOrientation:kotlin.Int` attribute. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#SCREEN_ORIENTATION_LOCKED:kotlin.Int` Constant corresponding to `locked` in the `https://developer.android.com/reference/kotlin/android/R.attr.html#screenOrientation:kotlin.Int` attribute. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#SCREEN_ORIENTATION_NOSENSOR:kotlin.Int` Constant corresponding to `nosensor` in the `https://developer.android.com/reference/kotlin/android/R.attr.html#screenOrientation:kotlin.Int` attribute. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#SCREEN_ORIENTATION_PORTRAIT:kotlin.Int` Constant corresponding to `portrait` in the `https://developer.android.com/reference/kotlin/android/R.attr.html#screenOrientation:kotlin.Int` attribute. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#SCREEN_ORIENTATION_REVERSE_LANDSCAPE:kotlin.Int` Constant corresponding to `reverseLandscape` in the `https://developer.android.com/reference/kotlin/android/R.attr.html#screenOrientation:kotlin.Int` attribute. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#SCREEN_ORIENTATION_REVERSE_PORTRAIT:kotlin.Int` Constant corresponding to `reversePortrait` in the `https://developer.android.com/reference/kotlin/android/R.attr.html#screenOrientation:kotlin.Int` attribute. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#SCREEN_ORIENTATION_SENSOR:kotlin.Int` Constant corresponding to `sensor` in the `https://developer.android.com/reference/kotlin/android/R.attr.html#screenOrientation:kotlin.Int` attribute. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#SCREEN_ORIENTATION_SENSOR_LANDSCAPE:kotlin.Int` Constant corresponding to `sensorLandscape` in the `https://developer.android.com/reference/kotlin/android/R.attr.html#screenOrientation:kotlin.Int` attribute. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#SCREEN_ORIENTATION_SENSOR_PORTRAIT:kotlin.Int` Constant corresponding to `sensorPortrait` in the `https://developer.android.com/reference/kotlin/android/R.attr.html#screenOrientation:kotlin.Int` attribute. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#SCREEN_ORIENTATION_UNSPECIFIED:kotlin.Int` Constant corresponding to `unspecified` in the `https://developer.android.com/reference/kotlin/android/R.attr.html#screenOrientation:kotlin.Int` attribute. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#SCREEN_ORIENTATION_USER:kotlin.Int` Constant corresponding to `user` in the `https://developer.android.com/reference/kotlin/android/R.attr.html#screenOrientation:kotlin.Int` attribute. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#SCREEN_ORIENTATION_USER_LANDSCAPE:kotlin.Int` Constant corresponding to `userLandscape` in the `https://developer.android.com/reference/kotlin/android/R.attr.html#screenOrientation:kotlin.Int` attribute. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#SCREEN_ORIENTATION_USER_PORTRAIT:kotlin.Int` Constant corresponding to `userPortrait` in the `https://developer.android.com/reference/kotlin/android/R.attr.html#screenOrientation:kotlin.Int` attribute. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#UIOPTION_SPLIT_ACTION_BAR_WHEN_NARROW:kotlin.Int` Flag for use with `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#uiOptions:kotlin.Int`. |

Inherited constants From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int`

Descriptor bit used with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()`: indicates that the Parcelable object's flattened representation includes a file descriptor.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`

Flag for use with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point.

<br />

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#ActivityInfo()()` <br /> |
| `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#ActivityInfo(android.content.pm.ActivityInfo)(orig: https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#!)` <br /> |

| Public methods ||
|---|---|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#describeContents()()` Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#dump(android.util.Printer,%20kotlin.String)(pw: https://developer.android.com/reference/kotlin/android/util/Printer.html#!, prefix: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` <br /> |
| open [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#getKnownActivityEmbeddingCerts()()` Gets the trusted host certificate digests of apps that are allowed to embed this activity. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#getThemeResource()()` Return the theme resource identifier to use for this activity. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#toString()()` Returns a string representation of the object. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#writeToParcel(android.os.Parcel,%20kotlin.Int)(dest: https://developer.android.com/reference/kotlin/android/os/Parcel.html#, parcelableFlags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` <br /> |
| --- | --- |

Inherited functions From class `https://developer.android.com/reference/kotlin/android/content/pm/ComponentInfo` `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/ComponentInfo#dumpBack(android.util.Printer,%20kotlin.String)(pw: https://developer.android.com/reference/kotlin/android/util/Printer.html#!, prefix: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/ComponentInfo#dumpFront(android.util.Printer,%20kotlin.String)(pw: https://developer.android.com/reference/kotlin/android/util/Printer.html#!, prefix: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/ComponentInfo#getBannerResource()()`

Return the banner resource identifier to use for this component. If the component defines a banner, that is used; else, the application banner is used.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/ComponentInfo#getIconResource()()`

Return the icon resource identifier to use for this component. If the component defines an icon, that is used; else, the application icon is used.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/ComponentInfo#getLogoResource()()`

Return the logo resource identifier to use for this component. If the component defines a logo, that is used; else, the application logo is used.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/ComponentInfo#isEnabled()()`

Return whether this component and its enclosing application are enabled.

<br />

From class `https://developer.android.com/reference/kotlin/android/content/pm/PackageItemInfo` `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#!` `https://developer.android.com/reference/kotlin/android/content/pm/PackageItemInfo#loadBanner(android.content.pm.PackageManager)(pm: https://developer.android.com/reference/kotlin/android/content/pm/PackageManager!)`

Retrieve the current graphical banner associated with this item. This will call back on the given PackageManager to load the banner from the application.

The returned drawable is subject to the same size capping limits as described in `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#getApplicationIcon(android.content.pm.ApplicationInfo)`.

<br />

`https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#!` `https://developer.android.com/reference/kotlin/android/content/pm/PackageItemInfo#loadIcon(android.content.pm.PackageManager)(pm: https://developer.android.com/reference/kotlin/android/content/pm/PackageManager!)`

Retrieve the current graphical icon associated with this item. This will call back on the given PackageManager to load the icon from the application.

The returned drawable is subject to the same size capping limits as described in `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#getApplicationIcon(android.content.pm.ApplicationInfo)`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageItemInfo#loadLabel(android.content.pm.PackageManager)(pm: https://developer.android.com/reference/kotlin/android/content/pm/PackageManager)`

Retrieve the current textual label associated with this item. This will call back on the given PackageManager to load the label from the application.

<br />

`https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#!` `https://developer.android.com/reference/kotlin/android/content/pm/PackageItemInfo#loadLogo(android.content.pm.PackageManager)(pm: https://developer.android.com/reference/kotlin/android/content/pm/PackageManager!)`

Retrieve the current graphical logo associated with this item. This will call back on the given PackageManager to load the logo from the application.

The returned drawable is subject to the same size capping limits as described in `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#getApplicationIcon(android.content.pm.ApplicationInfo)`.

<br />

`https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#!` `https://developer.android.com/reference/kotlin/android/content/pm/PackageItemInfo#loadUnbadgedIcon(android.content.pm.PackageManager)(pm: https://developer.android.com/reference/kotlin/android/content/pm/PackageManager!)`

Retrieve the current graphical icon associated with this item without the addition of a work badge if applicable. This will call back on the given PackageManager to load the icon from the application.

The returned drawable is subject to the same size capping limits as described in `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#getApplicationIcon(android.content.pm.ApplicationInfo)`.

<br />

`https://developer.android.com/reference/kotlin/android/content/res/XmlResourceParser.html#!` `https://developer.android.com/reference/kotlin/android/content/pm/PackageItemInfo#loadXmlMetaData(android.content.pm.PackageManager,%20kotlin.String)(pm: https://developer.android.com/reference/kotlin/android/content/pm/PackageManager!, name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)`

Load an XML resource attached to the meta-data of this item. This will retrieved the name meta-data entry, and if defined call back on the given PackageManager to load its XML file from the application.

<br />

| Properties ||
|---|---|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [ActivityInfo](../android/content/pm/ActivityInfo.md)!\> | `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#CREATOR:android.os.Parcelable.Creator` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#colorMode:kotlin.Int` The color mode requested by this activity. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#configChanges:kotlin.Int` Bit mask of kinds of configuration changes that this activity can handle itself (without being restarted by the system). |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#documentLaunchMode:kotlin.Int` The document launch mode style requested by the activity. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#flags:kotlin.Int` Options that have been set in the activity declaration in the manifest. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#launchMode:kotlin.Int` The launch mode style requested by the activity. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#maxRecents:kotlin.Int` The maximum number of tasks rooted at this activity that can be in the recent task list. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#parentActivityName:kotlin.String` If defined, the activity named here is the logical parent of this activity. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#permission:kotlin.String` Optional name of a permission required to be able to access this Activity. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#persistableMode:kotlin.Int` Value indicating how this activity is to be persisted across reboots for restoring in the Recents list. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#requiredDisplayCategory:kotlin.String` Specifies the required display category of the activity. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#screenOrientation:kotlin.Int` The preferred screen orientation this activity would like to run in. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#softInputMode:kotlin.Int` The desired soft input mode for this activity's main window. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#targetActivity:kotlin.String` If this is an activity alias, this is the real activity class to run for it. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#taskAffinity:kotlin.String` The affinity this activity has for another task in the system. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#theme:kotlin.Int` A style resource identifier (in the package's resources) of this activity's theme. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#uiOptions:kotlin.Int` The desired extra UI options for this activity and its main window. |
| [ActivityInfo.WindowLayout](../android/content/pm/ActivityInfo.WindowLayout.md)! | `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#windowLayout:android.content.pm.ActivityInfo.WindowLayout` Information about desired position and size of activity on the display when it is first started. |
| --- | --- |

Inherited properties From class `https://developer.android.com/reference/kotlin/android/content/pm/ComponentInfo` `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo!` `https://developer.android.com/reference/kotlin/android/content/pm/ComponentInfo#applicationInfo:android.content.pm.ApplicationInfo`

Global information about the application/package this component is a part of.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!` `https://developer.android.com/reference/kotlin/android/content/pm/ComponentInfo#attributionTags:kotlin.Array`

Set of attribution tags that should be automatically applied to this component.

When this component represents an `https://developer.android.com/reference/kotlin/android/app/Activity.html#`, `https://developer.android.com/reference/kotlin/android/app/Service.html#`, `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#` or `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#`, each instance will be automatically configured with `https://developer.android.com/reference/kotlin/android/content/Context.html#createAttributionContext(kotlin.String)` using the first attribution tag contained here.

Additionally, when this component represents a `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#` and the sender of a broadcast requires the receiver to hold one or more specific permissions, those permission checks will be performed using each of the attributions tags contained here.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/ComponentInfo#descriptionRes:kotlin.Int`

A string resource identifier (in the package's resources) containing a user-readable description of the component. From the "description" attribute or, if not set, 0.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/ComponentInfo#directBootAware:kotlin.Boolean`

Indicates if this component is aware of direct boot lifecycle, and can be safely run before the user has entered their credentials (such as a lock pattern or PIN).

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/ComponentInfo#enabled:kotlin.Boolean`

Indicates whether or not this component may be instantiated. Note that this value can be overridden by the one in its parent `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/ComponentInfo#exported:kotlin.Boolean`

Set to true if this component is available for use by other applications. Comes from `https://developer.android.com/reference/kotlin/android/R.attr.html#exported:kotlin.Int` of the \<activity\>, \<receiver\>, \<service\>, or \<provider\> tag.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` `https://developer.android.com/reference/kotlin/android/content/pm/ComponentInfo#processName:kotlin.String`

The name of the process this component should run in. From the "android:process" attribute or, if not set, the same as applicationInfo.processName.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` `https://developer.android.com/reference/kotlin/android/content/pm/ComponentInfo#splitName:kotlin.String`

The name of the split in which this component is declared. Null if the component was declared in the base APK.

<br />

From class `https://developer.android.com/reference/kotlin/android/content/pm/PackageItemInfo` `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageItemInfo#banner:kotlin.Int`

A drawable resource identifier (in the package's resources) of this component's banner. From the "banner" attribute or, if not set, 0.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageItemInfo#icon:kotlin.Int`

A drawable resource identifier (in the package's resources) of this component's icon. From the "icon" attribute or, if not set, 0.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageItemInfo#isArchived:kotlin.Boolean`

Whether the package is currently in an archived state.

Packages can be archived through `https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#requestArchive(kotlin.String,%20android.content.IntentSender)` and do not have any APKs stored on the device, but do keep the data directory.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageItemInfo#labelRes:kotlin.Int`

A string resource identifier (in the package's resources) of this component's label. From the "label" attribute or, if not set, 0.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageItemInfo#logo:kotlin.Int`

A drawable resource identifier (in the package's resources) of this component's logo. Logos may be larger/wider than icons and are displayed by certain UI elements in place of a name or name/icon combination. From the "logo" attribute or, if not set, 0.

<br />

`https://developer.android.com/reference/kotlin/android/os/Bundle.html#!` `https://developer.android.com/reference/kotlin/android/content/pm/PackageItemInfo#metaData:android.os.Bundle`

Additional meta-data associated with this component. This field will only be filled in if you set the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#GET_META_DATA:kotlin.Int` flag when requesting the info.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` `https://developer.android.com/reference/kotlin/android/content/pm/PackageItemInfo#name:kotlin.String`

Public name of this item. From the "android:name" attribute.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!` `https://developer.android.com/reference/kotlin/android/content/pm/PackageItemInfo#nonLocalizedLabel:kotlin.CharSequence`

The string provided in the AndroidManifest file, if any. You probably don't want to use this. You probably want `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#getApplicationLabel(android.content.pm.ApplicationInfo)`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` `https://developer.android.com/reference/kotlin/android/content/pm/PackageItemInfo#packageName:kotlin.String`

Name of the package that this item is in.

<br />

## Constants

### COLOR_MODE_DEFAULT

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val COLOR_MODE_DEFAULT: Int
```

Value for `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#colorMode:kotlin.Int` indicating that the activity should use the default color mode (sRGB, low dynamic range).

 Value: 0

**See Also**

- `https://developer.android.com/reference/kotlin/android/R.attr.html#colorMode:kotlin.Int`

### COLOR_MODE_HDR

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val COLOR_MODE_HDR: Int
```

Value of `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#colorMode:kotlin.Int` indicating that the activity should use a high dynamic range if the presentation display supports it.

Note: This does not impact SurfaceViews or SurfaceControls, as those have their own independent HDR support.

**Important:** Although this value was added in API 26, it is strongly recommended to avoid using it until API 34 which is when HDR support for the UI toolkit was officially added.

 Value: 2

**See Also**

- `https://developer.android.com/reference/kotlin/android/R.attr.html#colorMode:kotlin.Int`

### COLOR_MODE_WIDE_COLOR_GAMUT

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val COLOR_MODE_WIDE_COLOR_GAMUT: Int
```

Value of `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#colorMode:kotlin.Int` indicating that the activity should use a wide color gamut if the presentation display supports it.

 Value: 1

**See Also**

- `https://developer.android.com/reference/kotlin/android/R.attr.html#colorMode:kotlin.Int`

### CONFIG_ASSETS_PATHS

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONFIG_ASSETS_PATHS: Int
```

Bit in `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#configChanges:kotlin.Int` that indicates that the activity can itself handle asset path changes. Set from the `https://developer.android.com/reference/kotlin/android/R.attr.html#configChanges:kotlin.Int` attribute. This is not a core resource configuration, but a higher-level value, so its constant starts at the high bits.

 Value: -2147483648

### CONFIG_COLOR_MODE

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONFIG_COLOR_MODE: Int
```

Bit in `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#configChanges:kotlin.Int` that indicates that the activity can itself handle the change to the display color gamut or dynamic range. Set from the `https://developer.android.com/reference/kotlin/android/R.attr.html#configChanges:kotlin.Int` attribute.

 Value: 16384

### CONFIG_DENSITY

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONFIG_DENSITY: Int
```

Bit in `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#configChanges:kotlin.Int` that indicates that the activity can itself handle density changes. Set from the `https://developer.android.com/reference/kotlin/android/R.attr.html#configChanges:kotlin.Int` attribute.

 Value: 4096

### CONFIG_FONT_SCALE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONFIG_FONT_SCALE: Int
```

Bit in `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#configChanges:kotlin.Int` that indicates that the activity can itself handle changes to the font scaling factor. Set from the `https://developer.android.com/reference/kotlin/android/R.attr.html#configChanges:kotlin.Int` attribute. This is not a core resource configuration, but a higher-level value, so its constant starts at the high bits.

 Value: 1073741824

### CONFIG_FONT_WEIGHT_ADJUSTMENT

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONFIG_FONT_WEIGHT_ADJUSTMENT: Int
```

Bit in `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#configChanges:kotlin.Int` that indicates that the activity can itself handle changes to font weight. Set from the `https://developer.android.com/reference/kotlin/android/R.attr.html#configChanges:kotlin.Int` attribute. This is not a core resource configuration, but a higher-level value, so its constant starts at the high bits.

 Value: 268435456

### CONFIG_GRAMMATICAL_GENDER

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONFIG_GRAMMATICAL_GENDER: Int
```

Bit in `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#configChanges:kotlin.Int` that indicates that the activity can itself handle the change to gender. Set from the `https://developer.android.com/reference/kotlin/android/R.attr.html#configChanges:kotlin.Int` attribute.

 Value: 32768

### CONFIG_KEYBOARD

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONFIG_KEYBOARD: Int
```

Bit in `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#configChanges:kotlin.Int` that indicates that the activity can itself handle changes to the keyboard type. Set from the `https://developer.android.com/reference/kotlin/android/R.attr.html#configChanges:kotlin.Int` attribute.

 Value: 16

### CONFIG_KEYBOARD_HIDDEN

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONFIG_KEYBOARD_HIDDEN: Int
```

Bit in `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#configChanges:kotlin.Int` that indicates that the activity can itself handle changes to the keyboard or navigation being hidden/exposed. Note that inspite of the name, this applies to the changes to any hidden states: keyboard or navigation. Set from the `https://developer.android.com/reference/kotlin/android/R.attr.html#configChanges:kotlin.Int` attribute.

 Value: 32

### CONFIG_LAYOUT_DIRECTION

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONFIG_LAYOUT_DIRECTION: Int
```

Bit in `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#configChanges:kotlin.Int` that indicates that the activity can itself handle the change to layout direction. Set from the `https://developer.android.com/reference/kotlin/android/R.attr.html#configChanges:kotlin.Int` attribute.

 Value: 8192

### CONFIG_LOCALE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONFIG_LOCALE: Int
```

Bit in `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#configChanges:kotlin.Int` that indicates that the activity can itself handle changes to the locale. Set from the `https://developer.android.com/reference/kotlin/android/R.attr.html#configChanges:kotlin.Int` attribute.

 Value: 4

### CONFIG_MCC

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONFIG_MCC: Int
```

Bit in `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#configChanges:kotlin.Int` that indicates that the activity can itself handle changes to the IMSI MCC. Set from the `https://developer.android.com/reference/kotlin/android/R.attr.html#configChanges:kotlin.Int` attribute.

 Value: 1

### CONFIG_MNC

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONFIG_MNC: Int
```

Bit in `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#configChanges:kotlin.Int` that indicates that the activity can itself handle changes to the IMSI MNC. Set from the `https://developer.android.com/reference/kotlin/android/R.attr.html#configChanges:kotlin.Int` attribute.

 Value: 2

### CONFIG_NAVIGATION

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONFIG_NAVIGATION: Int
```

Bit in `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#configChanges:kotlin.Int` that indicates that the activity can itself handle changes to the navigation type. Set from the `https://developer.android.com/reference/kotlin/android/R.attr.html#configChanges:kotlin.Int` attribute.

 Value: 64

### CONFIG_ORIENTATION

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONFIG_ORIENTATION: Int
```

Bit in `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#configChanges:kotlin.Int` that indicates that the activity can itself handle changes to the screen orientation. Set from the `https://developer.android.com/reference/kotlin/android/R.attr.html#configChanges:kotlin.Int` attribute.

 Value: 128

### CONFIG_RESOURCES_UNUSED

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONFIG_RESOURCES_UNUSED: Int
```

This is probably not the constant you want, the resources compiler supports a less dangerous version of it, 'allKnown', that only suppresses all currently existing configuration change restarts depending on your target SDK rather than whatever the latest SDK supports, allowing the application to work with resources on future Platform versions.

Bit in `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#configChanges:kotlin.Int` that indicates that the activity doesn't use Android Resources at all and doesn't need to be restarted on any configuration changes. This bit disables all restarts for configuration dimensions available in the current target SDK as well as dimensions introduced in future SDKs. Use it only if the activity doesn't need anything from its resources, and doesn't depend on any libraries that may provide resources and need to respond to configuration changes. When set, `https://developer.android.com/reference/kotlin/android/app/Activity.html#onConfigurationChanged(android.content.res.Configuration)` will be called instead of a restart, and it's up to the implementation to ensure that no stale resource values remain loaded anywhere in the code.

This overrides all other bits, and this is recommended to be used individually.

This is not a core resource configuration, but a higher-level value, so its constant starts at the high bits.

 Value: 134217728

### CONFIG_SCREEN_LAYOUT

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONFIG_SCREEN_LAYOUT: Int
```

Bit in `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#configChanges:kotlin.Int` that indicates that the activity can itself handle changes to the screen layout. Set from the `https://developer.android.com/reference/kotlin/android/R.attr.html#configChanges:kotlin.Int` attribute.

 Value: 256

### CONFIG_SCREEN_SIZE

Added in [API level 13](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONFIG_SCREEN_SIZE: Int
```

Bit in `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#configChanges:kotlin.Int` that indicates that the activity can itself handle the screen size. Set from the `https://developer.android.com/reference/kotlin/android/R.attr.html#configChanges:kotlin.Int` attribute. This will be set by default for applications that target an earlier version than `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#HONEYCOMB_MR2:kotlin.Int`... **however** , you will not see the bit set here becomes some applications incorrectly compare `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#configChanges:kotlin.Int` against an absolute value rather than correctly masking out the bits they are interested in. Please don't do that, thanks.

 Value: 1024

### CONFIG_SMALLEST_SCREEN_SIZE

Added in [API level 13](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONFIG_SMALLEST_SCREEN_SIZE: Int
```

Bit in `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#configChanges:kotlin.Int` that indicates that the activity can itself handle the smallest screen size. Set from the `https://developer.android.com/reference/kotlin/android/R.attr.html#configChanges:kotlin.Int` attribute. This will be set by default for applications that target an earlier version than `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#HONEYCOMB_MR2:kotlin.Int`... **however** , you will not see the bit set here becomes some applications incorrectly compare `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#configChanges:kotlin.Int` against an absolute value rather than correctly masking out the bits they are interested in. Please don't do that, thanks.

 Value: 2048

### CONFIG_TOUCHSCREEN

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONFIG_TOUCHSCREEN: Int
```

Bit in `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#configChanges:kotlin.Int` that indicates that the activity can itself handle changes to the touchscreen type. Set from the `https://developer.android.com/reference/kotlin/android/R.attr.html#configChanges:kotlin.Int` attribute.

 Value: 8

### CONFIG_UI_MODE

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONFIG_UI_MODE: Int
```

Bit in `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#configChanges:kotlin.Int` that indicates that the activity can itself handle the ui mode. Set from the `https://developer.android.com/reference/kotlin/android/R.attr.html#configChanges:kotlin.Int` attribute.

 Value: 512

### DOCUMENT_LAUNCH_ALWAYS

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DOCUMENT_LAUNCH_ALWAYS: Int
```

Constant corresponding to `always` in the `https://developer.android.com/reference/kotlin/android/R.attr.html#documentLaunchMode:kotlin.Int` attribute.

 Value: 2

### DOCUMENT_LAUNCH_INTO_EXISTING

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DOCUMENT_LAUNCH_INTO_EXISTING: Int
```

Constant corresponding to `intoExisting` in the `https://developer.android.com/reference/kotlin/android/R.attr.html#documentLaunchMode:kotlin.Int` attribute.

 Value: 1

### DOCUMENT_LAUNCH_NEVER

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DOCUMENT_LAUNCH_NEVER: Int
```

Constant corresponding to `never` in the `https://developer.android.com/reference/kotlin/android/R.attr.html#documentLaunchMode:kotlin.Int` attribute.

 Value: 3

### DOCUMENT_LAUNCH_NONE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DOCUMENT_LAUNCH_NONE: Int
```

Constant corresponding to `none` in the `https://developer.android.com/reference/kotlin/android/R.attr.html#documentLaunchMode:kotlin.Int` attribute.

 Value: 0

### FLAG_ALLOW_TASK_REPARENTING

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_ALLOW_TASK_REPARENTING: Int
```

Bit in `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#flags:kotlin.Int` that indicates that the activity can be moved between tasks based on its task affinity. Set from the `https://developer.android.com/reference/kotlin/android/R.attr.html#allowTaskReparenting:kotlin.Int` attribute.

 Value: 64

### FLAG_ALLOW_UNTRUSTED_ACTIVITY_EMBEDDING

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_ALLOW_UNTRUSTED_ACTIVITY_EMBEDDING: Int
```

Bit in `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#flags:kotlin.Int`: If set, indicates that the activity can be embedded by untrusted hosts. In this case the interactions with and visibility of the embedded activity may be limited. Set from the `https://developer.android.com/reference/kotlin/android/R.attr.html#allowUntrustedActivityEmbedding:kotlin.Int` attribute.

 Value: 268435456

### FLAG_ALWAYS_RETAIN_TASK_STATE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_ALWAYS_RETAIN_TASK_STATE: Int
```

Bit in `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#flags:kotlin.Int` indicating that, when the activity is the root of a task, that task's stack should never be cleared when it is relaunched from home. Set from the `https://developer.android.com/reference/kotlin/android/R.attr.html#alwaysRetainTaskState:kotlin.Int` attribute.

 Value: 8

### FLAG_AUTO_REMOVE_FROM_RECENTS

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_AUTO_REMOVE_FROM_RECENTS: Int
```

Bit in `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#flags:kotlin.Int` indicating that tasks started with this activity are to be removed from the recent list of tasks when the last activity in the task is finished. Corresponds to `https://developer.android.com/reference/kotlin/android/R.attr.html#autoRemoveFromRecents:kotlin.Int`

 Value: 8192

### FLAG_CLEAR_TASK_ON_LAUNCH

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_CLEAR_TASK_ON_LAUNCH: Int
```

Bit in `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#flags:kotlin.Int` indicating that, when the activity is the root of a task, that task's stack should be cleared each time the user re-launches it from home. As a result, the user will always return to the original activity at the top of the task. This flag only applies to activities that are used to start the root of a new task. Set from the `https://developer.android.com/reference/kotlin/android/R.attr.html#clearTaskOnLaunch:kotlin.Int` attribute.

 Value: 4

### FLAG_ENABLE_VR_MODE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_ENABLE_VR_MODE: Int
```

Bit in `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#flags:kotlin.Int` indicating that this activity should be run with VR mode enabled.

 Value: 32768

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/Activity.html#setVrModeEnabled(kotlin.Boolean,%20android.content.ComponentName)`

### FLAG_EXCLUDE_FROM_RECENTS

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_EXCLUDE_FROM_RECENTS: Int
```

Bit in `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#flags:kotlin.Int` that indicates that the activity should not appear in the list of recently launched activities. Set from the `https://developer.android.com/reference/kotlin/android/R.attr.html#excludeFromRecents:kotlin.Int` attribute.

 Value: 32

### FLAG_FINISH_ON_CLOSE_SYSTEM_DIALOGS

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_FINISH_ON_CLOSE_SYSTEM_DIALOGS: Int
```

Bit in `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#flags:kotlin.Int` indicating that, when a request to close system windows happens, this activity is finished. Set from the `https://developer.android.com/reference/kotlin/android/R.attr.html#finishOnCloseSystemDialogs:kotlin.Int` attribute.

 Value: 256

### FLAG_FINISH_ON_TASK_LAUNCH

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_FINISH_ON_TASK_LAUNCH: Int
```

Bit in `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#flags:kotlin.Int` indicating that, when the activity's task is relaunched from home, this activity should be finished. Set from the `https://developer.android.com/reference/kotlin/android/R.attr.html#finishOnTaskLaunch:kotlin.Int` attribute.

 Value: 2

### FLAG_HARDWARE_ACCELERATED

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_HARDWARE_ACCELERATED: Int
```

Value for `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#flags:kotlin.Int`: true when the application's rendering should be hardware accelerated.

 Value: 512

### FLAG_IMMERSIVE

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_IMMERSIVE: Int
```

Bit in `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#flags:kotlin.Int` corresponding to an immersive activity that wishes not to be interrupted by notifications. Applications that hide the system notification bar with `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#FLAG_FULLSCREEN:kotlin.Int` may still be interrupted by high-priority notifications; for example, an incoming phone call may use `https://developer.android.com/reference/kotlin/android/app/Notification.html#fullScreenIntent:android.app.PendingIntent` to present a full-screen in-call activity to the user, pausing the current activity as a side-effect. An activity with `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#FLAG_IMMERSIVE:kotlin.Int` set, however, will not be interrupted; the notification may be shown in some other way (such as a small floating "toast" window). Note that this flag will always reflect the Activity's `android:immersive` manifest definition, even if the Activity's immersive state is changed at runtime via `https://developer.android.com/reference/kotlin/android/app/Activity.html#setImmersive(kotlin.Boolean)`.

 Value: 2048

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/Notification.html#FLAG_HIGH_PRIORITY:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/app/Activity.html#setImmersive(kotlin.Boolean)`

### FLAG_MULTIPROCESS

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_MULTIPROCESS: Int
```

Bit in `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#flags:kotlin.Int` indicating whether this activity is able to run in multiple processes. If true, the system may instantiate it in the some process as the process starting it in order to conserve resources. If false, the default, it always runs in `https://developer.android.com/reference/kotlin/android/content/pm/ComponentInfo#processName:kotlin.String`. Set from the `https://developer.android.com/reference/kotlin/android/R.attr.html#multiprocess:kotlin.Int` attribute.

 Value: 1

### FLAG_NO_HISTORY

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_NO_HISTORY: Int
```

Bit in `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#flags:kotlin.Int` indicating that, when the user navigates away from an activity, it should be finished. Set from the `https://developer.android.com/reference/kotlin/android/R.attr.html#noHistory:kotlin.Int` attribute.

 Value: 128

### FLAG_PREFER_MINIMAL_POST_PROCESSING

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_PREFER_MINIMAL_POST_PROCESSING: Int
```

Bit in `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#flags:kotlin.Int` indicating whether the display should preferably be switched to a minimal post processing mode. See `https://developer.android.com/reference/kotlin/android/R.attr.html#preferMinimalPostProcessing:kotlin.Int`

 Value: 33554432

### FLAG_RELINQUISH_TASK_IDENTITY

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_RELINQUISH_TASK_IDENTITY: Int
```

Bit in `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#flags:kotlin.Int`: If set, a task rooted at this activity will have its baseIntent replaced by the activity immediately above this. Each activity may further relinquish its identity to the activity above it using this flag. Set from the `https://developer.android.com/reference/kotlin/android/R.attr.html#relinquishTaskIdentity:kotlin.Int` attribute.

 Value: 4096

### FLAG_RESUME_WHILE_PAUSING

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_RESUME_WHILE_PAUSING: Int
```

Bit in `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#flags:kotlin.Int` indicating that this activity can start is creation/resume while the previous activity is still pausing. Corresponds to `https://developer.android.com/reference/kotlin/android/R.attr.html#resumeWhilePausing:kotlin.Int`

 Value: 16384

### FLAG_SINGLE_USER

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_SINGLE_USER: Int
```

Bit in `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#flags:kotlin.Int`: If set, a single instance of the receiver will run for all users on the device. Set from the `https://developer.android.com/reference/kotlin/android/R.attr.html#singleUser:kotlin.Int` attribute. Note that this flag is only relevant for ActivityInfo structures that are describing receiver components; it is not applied to activities.

 Value: 1073741824

### FLAG_STATE_NOT_NEEDED

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_STATE_NOT_NEEDED: Int
```

Bit in `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#flags:kotlin.Int` indicating that the activity's state is not required to be saved, so that if there is a failure the activity will not be removed from the activity stack. Set from the `https://developer.android.com/reference/kotlin/android/R.attr.html#stateNotNeeded:kotlin.Int` attribute.

 Value: 16

### LAUNCH_MULTIPLE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LAUNCH_MULTIPLE: Int
```

Constant corresponding to `standard` in the `https://developer.android.com/reference/kotlin/android/R.attr.html#launchMode:kotlin.Int` attribute.

 Value: 0

### LAUNCH_SINGLE_INSTANCE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LAUNCH_SINGLE_INSTANCE: Int
```

Constant corresponding to `singleInstance` in the `https://developer.android.com/reference/kotlin/android/R.attr.html#launchMode:kotlin.Int` attribute.

 Value: 3

### LAUNCH_SINGLE_INSTANCE_PER_TASK

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LAUNCH_SINGLE_INSTANCE_PER_TASK: Int
```

Constant corresponding to `singleInstancePerTask` in the `https://developer.android.com/reference/kotlin/android/R.attr.html#launchMode:kotlin.Int` attribute.

 Value: 4

### LAUNCH_SINGLE_TASK

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LAUNCH_SINGLE_TASK: Int
```

Constant corresponding to `singleTask` in the `https://developer.android.com/reference/kotlin/android/R.attr.html#launchMode:kotlin.Int` attribute.

 Value: 2

### LAUNCH_SINGLE_TOP

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LAUNCH_SINGLE_TOP: Int
```

Constant corresponding to `singleTop` in the `https://developer.android.com/reference/kotlin/android/R.attr.html#launchMode:kotlin.Int` attribute.

 Value: 1

### PERSIST_ACROSS_REBOOTS

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PERSIST_ACROSS_REBOOTS: Int
```

Constant corresponding to `persistAcrossReboots` in the `https://developer.android.com/reference/kotlin/android/R.attr.html#persistableMode:kotlin.Int` attribute.

 Value: 2

### PERSIST_NEVER

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PERSIST_NEVER: Int
```

Constant corresponding to `doNotPersist` in the `https://developer.android.com/reference/kotlin/android/R.attr.html#persistableMode:kotlin.Int` attribute.

 Value: 1

### PERSIST_ROOT_ONLY

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PERSIST_ROOT_ONLY: Int
```

Constant corresponding to `persistRootOnly` in the `https://developer.android.com/reference/kotlin/android/R.attr.html#persistableMode:kotlin.Int` attribute.

 Value: 0

### SCREEN_ORIENTATION_BEHIND

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SCREEN_ORIENTATION_BEHIND: Int
```

Constant corresponding to `behind` in the `https://developer.android.com/reference/kotlin/android/R.attr.html#screenOrientation:kotlin.Int` attribute.

 Value: 3

### SCREEN_ORIENTATION_FULL_SENSOR

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SCREEN_ORIENTATION_FULL_SENSOR: Int
```

Constant corresponding to `fullSensor` in the `https://developer.android.com/reference/kotlin/android/R.attr.html#screenOrientation:kotlin.Int` attribute.

 Value: 10

### SCREEN_ORIENTATION_FULL_USER

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SCREEN_ORIENTATION_FULL_USER: Int
```

Constant corresponding to `fullUser` in the `https://developer.android.com/reference/kotlin/android/R.attr.html#screenOrientation:kotlin.Int` attribute.

 Value: 13

### SCREEN_ORIENTATION_LANDSCAPE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SCREEN_ORIENTATION_LANDSCAPE: Int
```

Constant corresponding to `landscape` in the `https://developer.android.com/reference/kotlin/android/R.attr.html#screenOrientation:kotlin.Int` attribute.

 Value: 0

### SCREEN_ORIENTATION_LOCKED

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SCREEN_ORIENTATION_LOCKED: Int
```

Constant corresponding to `locked` in the `https://developer.android.com/reference/kotlin/android/R.attr.html#screenOrientation:kotlin.Int` attribute.

 Value: 14

### SCREEN_ORIENTATION_NOSENSOR

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SCREEN_ORIENTATION_NOSENSOR: Int
```

Constant corresponding to `nosensor` in the `https://developer.android.com/reference/kotlin/android/R.attr.html#screenOrientation:kotlin.Int` attribute.

 Value: 5

### SCREEN_ORIENTATION_PORTRAIT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SCREEN_ORIENTATION_PORTRAIT: Int
```

Constant corresponding to `portrait` in the `https://developer.android.com/reference/kotlin/android/R.attr.html#screenOrientation:kotlin.Int` attribute.

 Value: 1

### SCREEN_ORIENTATION_REVERSE_LANDSCAPE

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SCREEN_ORIENTATION_REVERSE_LANDSCAPE: Int
```

Constant corresponding to `reverseLandscape` in the `https://developer.android.com/reference/kotlin/android/R.attr.html#screenOrientation:kotlin.Int` attribute.

 Value: 8

### SCREEN_ORIENTATION_REVERSE_PORTRAIT

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SCREEN_ORIENTATION_REVERSE_PORTRAIT: Int
```

Constant corresponding to `reversePortrait` in the `https://developer.android.com/reference/kotlin/android/R.attr.html#screenOrientation:kotlin.Int` attribute.

 Value: 9

### SCREEN_ORIENTATION_SENSOR

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SCREEN_ORIENTATION_SENSOR: Int
```

Constant corresponding to `sensor` in the `https://developer.android.com/reference/kotlin/android/R.attr.html#screenOrientation:kotlin.Int` attribute.

 Value: 4

### SCREEN_ORIENTATION_SENSOR_LANDSCAPE

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SCREEN_ORIENTATION_SENSOR_LANDSCAPE: Int
```

Constant corresponding to `sensorLandscape` in the `https://developer.android.com/reference/kotlin/android/R.attr.html#screenOrientation:kotlin.Int` attribute.

 Value: 6

### SCREEN_ORIENTATION_SENSOR_PORTRAIT

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SCREEN_ORIENTATION_SENSOR_PORTRAIT: Int
```

Constant corresponding to `sensorPortrait` in the `https://developer.android.com/reference/kotlin/android/R.attr.html#screenOrientation:kotlin.Int` attribute.

 Value: 7

### SCREEN_ORIENTATION_UNSPECIFIED

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SCREEN_ORIENTATION_UNSPECIFIED: Int
```

Constant corresponding to `unspecified` in the `https://developer.android.com/reference/kotlin/android/R.attr.html#screenOrientation:kotlin.Int` attribute.

 Value: -1

### SCREEN_ORIENTATION_USER

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SCREEN_ORIENTATION_USER: Int
```

Constant corresponding to `user` in the `https://developer.android.com/reference/kotlin/android/R.attr.html#screenOrientation:kotlin.Int` attribute.

 Value: 2

### SCREEN_ORIENTATION_USER_LANDSCAPE

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SCREEN_ORIENTATION_USER_LANDSCAPE: Int
```

Constant corresponding to `userLandscape` in the `https://developer.android.com/reference/kotlin/android/R.attr.html#screenOrientation:kotlin.Int` attribute.

 Value: 11

### SCREEN_ORIENTATION_USER_PORTRAIT

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SCREEN_ORIENTATION_USER_PORTRAIT: Int
```

Constant corresponding to `userPortrait` in the `https://developer.android.com/reference/kotlin/android/R.attr.html#screenOrientation:kotlin.Int` attribute.

 Value: 12

### UIOPTION_SPLIT_ACTION_BAR_WHEN_NARROW

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val UIOPTION_SPLIT_ACTION_BAR_WHEN_NARROW: Int
```

Flag for use with `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#uiOptions:kotlin.Int`. Indicates that the action bar should put all action items in a separate bar when the screen is narrow.

This value corresponds to "splitActionBarWhenNarrow" for the `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#uiOptions:kotlin.Int` XML attribute.

 Value: 1

## Public constructors

### ActivityInfo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
ActivityInfo()
```

### ActivityInfo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
ActivityInfo(orig: ActivityInfo!)
```

## Public methods

### describeContents

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### dump

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun dump(
    pw: Printer!, 
    prefix: String!
): Unit
```

### getKnownActivityEmbeddingCerts

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getKnownActivityEmbeddingCerts(): MutableSet<String!>
```

Gets the trusted host certificate digests of apps that are allowed to embed this activity. The digests are computed using the SHA-256 digest algorithm.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>` | This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/R.attr.html#knownActivityEmbeddingCerts:kotlin.Int`

### getThemeResource

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getThemeResource(): Int
```

Return the theme resource identifier to use for this activity. If the activity defines a theme, that is used; else, the application theme is used.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The theme associated with this activity. |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun toString(): String
```

Returns a string representation of the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the object. |

### writeToParcel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun writeToParcel(
    dest: Parcel, 
    parcelableFlags: Int
): Unit
```

| Parameters ||
|---|---|
| `dest` | [Parcel](../android/os/Parcel.md): The Parcel in which the object should be written. This value cannot be `null`. |
| `flags` | Additional flags about how the object should be written. May be 0 or `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` |

## Properties

### CREATOR

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<ActivityInfo!>
```

### colorMode

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var colorMode: Int
```

The color mode requested by this activity. The target display may not be able to honor the request. 
Value is one of the following:

- `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#COLOR_MODE_DEFAULT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#COLOR_MODE_WIDE_COLOR_GAMUT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#COLOR_MODE_HDR:kotlin.Int`

<br />

### configChanges

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var configChanges: Int
```

Bit mask of kinds of configuration changes that this activity can handle itself (without being restarted by the system). Contains any combination of `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#CONFIG_FONT_SCALE:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#CONFIG_MCC:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#CONFIG_MNC:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#CONFIG_LOCALE:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#CONFIG_TOUCHSCREEN:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#CONFIG_KEYBOARD:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#CONFIG_NAVIGATION:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#CONFIG_ORIENTATION:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#CONFIG_SCREEN_LAYOUT:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#CONFIG_DENSITY:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#CONFIG_LAYOUT_DIRECTION:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#CONFIG_COLOR_MODE:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#CONFIG_GRAMMATICAL_GENDER:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#CONFIG_ASSETS_PATHS:kotlin.Int`, and `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#CONFIG_RESOURCES_UNUSED:kotlin.Int`. Set from the `https://developer.android.com/reference/kotlin/android/R.attr.html#configChanges:kotlin.Int` attribute.

### documentLaunchMode

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var documentLaunchMode: Int
```

The document launch mode style requested by the activity. From the `https://developer.android.com/reference/kotlin/android/R.attr.html#documentLaunchMode:kotlin.Int` attribute, one of `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#DOCUMENT_LAUNCH_NONE:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#DOCUMENT_LAUNCH_INTO_EXISTING:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#DOCUMENT_LAUNCH_ALWAYS:kotlin.Int`.

Modes DOCUMENT_LAUNCH_ALWAYS and DOCUMENT_LAUNCH_INTO_EXISTING are equivalent to `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_ACTIVITY_NEW_DOCUMENT:kotlin.Int` with and without `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_ACTIVITY_MULTIPLE_TASK:kotlin.Int` respectively.

### flags

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var flags: Int
```

Options that have been set in the activity declaration in the manifest. These include: `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#FLAG_MULTIPROCESS:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#FLAG_FINISH_ON_TASK_LAUNCH:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#FLAG_CLEAR_TASK_ON_LAUNCH:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#FLAG_ALWAYS_RETAIN_TASK_STATE:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#FLAG_STATE_NOT_NEEDED:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#FLAG_EXCLUDE_FROM_RECENTS:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#FLAG_ALLOW_TASK_REPARENTING:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#FLAG_NO_HISTORY:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#FLAG_FINISH_ON_CLOSE_SYSTEM_DIALOGS:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#FLAG_HARDWARE_ACCELERATED:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#FLAG_SINGLE_USER:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#FLAG_ALLOW_UNTRUSTED_ACTIVITY_EMBEDDING:kotlin.Int`.

### launchMode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var launchMode: Int
```

The launch mode style requested by the activity. From the `https://developer.android.com/reference/kotlin/android/R.attr.html#launchMode:kotlin.Int` attribute. 
Value is one of the following:

- `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#LAUNCH_MULTIPLE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#LAUNCH_SINGLE_TOP:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#LAUNCH_SINGLE_TASK:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#LAUNCH_SINGLE_INSTANCE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#LAUNCH_SINGLE_INSTANCE_PER_TASK:kotlin.Int`

<br />

### maxRecents

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var maxRecents: Int
```

The maximum number of tasks rooted at this activity that can be in the recent task list. Refer to `https://developer.android.com/reference/kotlin/android/R.attr.html#maxRecents:kotlin.Int`.

### parentActivityName

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var parentActivityName: String!
```

If defined, the activity named here is the logical parent of this activity.

### permission

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var permission: String!
```

Optional name of a permission required to be able to access this Activity. From the "permission" attribute.

### persistableMode

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var persistableMode: Int
```

Value indicating how this activity is to be persisted across reboots for restoring in the Recents list. `https://developer.android.com/reference/kotlin/android/R.attr.html#persistableMode:kotlin.Int`

### requiredDisplayCategory

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var requiredDisplayCategory: String?
```

Specifies the required display category of the activity. Set from the `https://developer.android.com/reference/kotlin/android/R.attr.html#requiredDisplayCategory:kotlin.Int` attribute. Upon creation, a display can specify which display categories it supports and one of the category must be present in the `<activity>` element to allow this activity to run. The default value is `null`, which indicates the activity does not have a required display category and thus can only run on a display that didn't specify any display categories. Each activity can only specify one required category but a display can support multiple display categories.

This field should be formatted as a Java-language-style free form string(for example, com.google.automotive_entertainment), which may contain uppercase or lowercase letters ('A' through 'Z'), numbers, and underscores ('_') but may only start with letters.

### screenOrientation

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var screenOrientation: Int
```

The preferred screen orientation this activity would like to run in. From the `https://developer.android.com/reference/kotlin/android/R.attr.html#screenOrientation:kotlin.Int` attribute, one of `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#SCREEN_ORIENTATION_UNSPECIFIED:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#SCREEN_ORIENTATION_LANDSCAPE:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#SCREEN_ORIENTATION_PORTRAIT:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#SCREEN_ORIENTATION_USER:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#SCREEN_ORIENTATION_BEHIND:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#SCREEN_ORIENTATION_SENSOR:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#SCREEN_ORIENTATION_NOSENSOR:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#SCREEN_ORIENTATION_SENSOR_LANDSCAPE:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#SCREEN_ORIENTATION_SENSOR_PORTRAIT:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#SCREEN_ORIENTATION_REVERSE_LANDSCAPE:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#SCREEN_ORIENTATION_REVERSE_PORTRAIT:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#SCREEN_ORIENTATION_FULL_SENSOR:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#SCREEN_ORIENTATION_USER_LANDSCAPE:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#SCREEN_ORIENTATION_USER_PORTRAIT:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#SCREEN_ORIENTATION_FULL_USER:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#SCREEN_ORIENTATION_LOCKED:kotlin.Int`,. 
Value is one of the following:

- `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#SCREEN_ORIENTATION_UNSPECIFIED:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#SCREEN_ORIENTATION_LANDSCAPE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#SCREEN_ORIENTATION_PORTRAIT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#SCREEN_ORIENTATION_USER:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#SCREEN_ORIENTATION_BEHIND:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#SCREEN_ORIENTATION_SENSOR:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#SCREEN_ORIENTATION_NOSENSOR:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#SCREEN_ORIENTATION_SENSOR_LANDSCAPE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#SCREEN_ORIENTATION_SENSOR_PORTRAIT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#SCREEN_ORIENTATION_REVERSE_LANDSCAPE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#SCREEN_ORIENTATION_REVERSE_PORTRAIT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#SCREEN_ORIENTATION_FULL_SENSOR:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#SCREEN_ORIENTATION_USER_LANDSCAPE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#SCREEN_ORIENTATION_USER_PORTRAIT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#SCREEN_ORIENTATION_FULL_USER:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#SCREEN_ORIENTATION_LOCKED:kotlin.Int`

<br />

### softInputMode

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var softInputMode: Int
```

The desired soft input mode for this activity's main window. Set from the `https://developer.android.com/reference/kotlin/android/R.attr.html#windowSoftInputMode:kotlin.Int` attribute in the activity's manifest. May be any of the same values allowed for `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#softInputMode:kotlin.Int`. If 0 (unspecified), the mode from the theme will be used. 
Value is either `0` or a combination of the following:

- `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#SOFT_INPUT_STATE_UNSPECIFIED:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#SOFT_INPUT_STATE_UNCHANGED:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#SOFT_INPUT_STATE_HIDDEN:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#SOFT_INPUT_STATE_ALWAYS_HIDDEN:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#SOFT_INPUT_STATE_VISIBLE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#SOFT_INPUT_STATE_ALWAYS_VISIBLE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#SOFT_INPUT_ADJUST_UNSPECIFIED:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#SOFT_INPUT_ADJUST_RESIZE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#SOFT_INPUT_ADJUST_PAN:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#SOFT_INPUT_ADJUST_NOTHING:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#SOFT_INPUT_IS_FORWARD_NAVIGATION:kotlin.Int`

<br />

### targetActivity

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var targetActivity: String!
```

If this is an activity alias, this is the real activity class to run for it. Otherwise, this is null.

### taskAffinity

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var taskAffinity: String!
```

The affinity this activity has for another task in the system. The string here is the name of the task, often the package name of the overall package. If null, the activity has no affinity. Set from the `https://developer.android.com/reference/kotlin/android/R.attr.html#taskAffinity:kotlin.Int` attribute.

### theme

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var theme: Int
```

A style resource identifier (in the package's resources) of this activity's theme. From the "theme" attribute or, if not set, 0.

### uiOptions

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var uiOptions: Int
```

The desired extra UI options for this activity and its main window. Set from the `https://developer.android.com/reference/kotlin/android/R.attr.html#uiOptions:kotlin.Int` attribute in the activity's manifest.

### windowLayout

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var windowLayout: ActivityInfo.WindowLayout!
```

Information about desired position and size of activity on the display when it is first started.
