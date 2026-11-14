Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SystemOnBackInvokedCallbacks

Kotlin | [Java](https://developer.android.com/reference/android/window/SystemOnBackInvokedCallbacks "View this page in Java")

```
class SystemOnBackInvokedCallbacks
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.window.SystemOnBackInvokedCallbacks](https://developer.android.com/reference/kotlin/android/window/SystemOnBackInvokedCallbacks#) |

Utility class providing `https://developer.android.com/reference/kotlin/android/window/OnBackInvokedCallback`s to override the default behavior when system back is invoked. e.g. `https://developer.android.com/reference/kotlin/android/app/Activity.html#finish()`

By registering these callbacks with the `https://developer.android.com/reference/kotlin/android/window/OnBackInvokedDispatcher`, the system can trigger specific behaviors and play corresponding ahead-of-time animations when the back gesture is invoked.

For example, to trigger the `https://developer.android.com/reference/kotlin/android/app/Activity.html#moveTaskToBack(kotlin.Boolean)` behavior:

```kotlin
OnBackInvokedDispatcher dispatcher = activity.getOnBackInvokedDispatcher();
    dispatcher.registerOnBackInvokedCallback(
        OnBackInvokedDispatcher.PRIORITY_DEFAULT,
        SystemOnBackInvokedCallbacks.moveTaskToBackCallback(activity));
  
```

## Summary

| Public methods ||
|---|---|
| static [OnBackInvokedCallback](https://developer.android.com/reference/kotlin/android/window/OnBackInvokedCallback) | `https://developer.android.com/reference/kotlin/android/window/SystemOnBackInvokedCallbacks#finishAndRemoveTaskCallback(android.app.Activity)(activity: https://developer.android.com/reference/kotlin/android/app/Activity.html#)` Get a callback to triggers `https://developer.android.com/reference/kotlin/android/app/Activity.html#finishAndRemoveTask()` on the associated `https://developer.android.com/reference/kotlin/android/app/Activity.html#`. |
| static [OnBackInvokedCallback](https://developer.android.com/reference/kotlin/android/window/OnBackInvokedCallback) | `https://developer.android.com/reference/kotlin/android/window/SystemOnBackInvokedCallbacks#moveTaskToBackCallback(android.app.Activity)(activity: https://developer.android.com/reference/kotlin/android/app/Activity.html#)` Get a callback to triggers `https://developer.android.com/reference/kotlin/android/app/Activity.html#moveTaskToBack(kotlin.Boolean)` on the associated `https://developer.android.com/reference/kotlin/android/app/Activity.html#`, moving the task containing the activity to the background. |

## Public methods

### finishAndRemoveTaskCallback

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun finishAndRemoveTaskCallback(activity: Activity): OnBackInvokedCallback
```

Get a callback to triggers `https://developer.android.com/reference/kotlin/android/app/Activity.html#finishAndRemoveTask()` on the associated `https://developer.android.com/reference/kotlin/android/app/Activity.html#`. If the activity is the root activity of its task, the entire task will be removed from the recents task. The activity will be finished in all cases. The system will play the corresponding transition animation.

| Parameters ||
|---|---|
| `activity` | [Activity](https://developer.android.com/reference/kotlin/android/app/Activity.html#): The associated `https://developer.android.com/reference/kotlin/android/app/Activity.html#` This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/window/OnBackInvokedCallback` | This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/Activity.html#finishAndRemoveTask()`

### moveTaskToBackCallback

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun moveTaskToBackCallback(activity: Activity): OnBackInvokedCallback
```

Get a callback to triggers `https://developer.android.com/reference/kotlin/android/app/Activity.html#moveTaskToBack(kotlin.Boolean)` on the associated `https://developer.android.com/reference/kotlin/android/app/Activity.html#`, moving the task containing the activity to the background. The system will play the corresponding transition animation, regardless of whether the activity is the root activity of the task.

| Parameters ||
|---|---|
| `activity` | [Activity](https://developer.android.com/reference/kotlin/android/app/Activity.html#): The associated `https://developer.android.com/reference/kotlin/android/app/Activity.html#` This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/window/OnBackInvokedCallback` | This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/Activity.html#moveTaskToBack(kotlin.Boolean)`
