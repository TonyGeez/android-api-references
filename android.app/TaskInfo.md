Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TaskInfo

```
open class TaskInfo
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.app.TaskInfo](TaskInfo.md) |

Known Direct Subclasses [ActivityManager.RecentTaskInfo](../android/app/ActivityManager.RecentTaskInfo.md), [ActivityManager.RunningTaskInfo](../android/app/ActivityManager.RunningTaskInfo.md) [ActivityManager.RecentTaskInfo](../android/app/ActivityManager.RecentTaskInfo.md) Information you can retrieve about tasks that the user has most recently started or visited.
[ActivityManager.RunningTaskInfo](../android/app/ActivityManager.RunningTaskInfo.md) Information you can retrieve about a particular task that is currently "running" in the system.

Stores information about a particular Task.

## Summary

| Public methods ||
|---|---|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getDisplayId <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isVisible Whether this task is visible. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | toString Returns a string representation of the object. |
| --- | --- |

| Properties ||
|---|---|
| [ComponentName](../android.content/ComponentName.md)? | `https://developer.android.com/reference/kotlin/android/app/TaskInfo#baseActivity:android.content.ComponentName` The component of the first activity in the task, can be considered the "application" of this task. |
| [Intent](../android.content/Intent.md) | `https://developer.android.com/reference/kotlin/android/app/TaskInfo#baseIntent:android.content.Intent` The base intent of the task (generally the intent that launched the task). |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/app/TaskInfo#isRunning:kotlin.Boolean` Whether or not this task has any running activities. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/TaskInfo#numActivities:kotlin.Int` The number of activities in this task (including running). |
| [ComponentName](../android.content/ComponentName.md)? | `https://developer.android.com/reference/kotlin/android/app/TaskInfo#origActivity:android.content.ComponentName` The component of the target activity if this task was started from an activity alias. |
| [ActivityManager.TaskDescription](../android/app/ActivityManager.TaskDescription.md)? | `https://developer.android.com/reference/kotlin/android/app/TaskInfo#taskDescription:android.app.ActivityManager.TaskDescription` The recent activity values for the highest activity in the stack to have set the values. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/TaskInfo#taskId:kotlin.Int` The identifier for this task. |
| [ComponentName](../android.content/ComponentName.md)? | `https://developer.android.com/reference/kotlin/android/app/TaskInfo#topActivity:android.content.ComponentName` The component of the top activity in the task, currently showing to the user. |

## Public methods

### getDisplayId

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getDisplayId(): Int
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The id of the display this task is associated with. |

### isVisible

Added in [API level 32](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isVisible(): Boolean
```

Whether this task is visible.

### toString

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun toString(): String
```

Returns a string representation of the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the object. |

## Properties

### baseActivity

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var baseActivity: ComponentName?
```

The component of the first activity in the task, can be considered the "application" of this task.

### baseIntent

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var baseIntent: Intent
```

The base intent of the task (generally the intent that launched the task). This intent can be used to relaunch the task (if it is no longer running) or brought to the front if it is.

### isRunning

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var isRunning: Boolean
```

Whether or not this task has any running activities.

### numActivities

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var numActivities: Int
```

The number of activities in this task (including running).

### origActivity

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var origActivity: ComponentName?
```

The component of the target activity if this task was started from an activity alias. Otherwise, this is null.

### taskDescription

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var taskDescription: ActivityManager.TaskDescription?
```

The recent activity values for the highest activity in the stack to have set the values. setTaskDescription.

### taskId

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var taskId: Int
```

The identifier for this task.

### topActivity

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var topActivity: ComponentName?
```

The component of the top activity in the task, currently showing to the user.
