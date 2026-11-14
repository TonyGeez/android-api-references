Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SystemOnBackInvokedCallbacks

Kotlin | [Java](SystemOnBackInvokedCallbacks.md)
| --- | --- |

```
class SystemOnBackInvokedCallbacks
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.window.SystemOnBackInvokedCallbacks](SystemOnBackInvokedCallbacks.md) |

Utility class providing OnBackInvokedCallbacks to override the default behavior when system back is invoked. e.g. finish

By registering these callbacks with the OnBackInvokedDispatcher, the system can trigger specific behaviors and play corresponding ahead-of-time animations when the back gesture is invoked.

For example, to trigger the moveTaskToBack behavior:

```kotlin
OnBackInvokedDispatcher dispatcher = activity.getOnBackInvokedDispatcher();
    dispatcher.registerOnBackInvokedCallback(
        OnBackInvokedDispatcher.PRIORITY_DEFAULT,
        SystemOnBackInvokedCallbacks.moveTaskToBackCallback(activity));
  
```

## Summary

| Public methods ||
|---|---|
| static [OnBackInvokedCallback](OnBackInvokedCallback.md) | finishAndRemoveTaskCallback Get a callback to triggers finishAndRemoveTask on the associated `https://developer.android.com/reference/kotlin/android/app/Activity.html#`. |
| static [OnBackInvokedCallback](OnBackInvokedCallback.md) | moveTaskToBackCallback Get a callback to triggers moveTaskToBack on the associated `https://developer.android.com/reference/kotlin/android/app/Activity.html#`, moving the task containing the activity to the background. |

## Public methods

### finishAndRemoveTaskCallback

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun finishAndRemoveTaskCallback(activity: Activity): OnBackInvokedCallback
```

Get a callback to triggers finishAndRemoveTask on the associated `https://developer.android.com/reference/kotlin/android/app/Activity.html#`. If the activity is the root activity of its task, the entire task will be removed from the recents task. The activity will be finished in all cases. The system will play the corresponding transition animation.

| Parameters ||
|---|---|
| `activity` | [Activity](../android.app/Activity.md): The associated `https://developer.android.com/reference/kotlin/android/app/Activity.html#` This value cannot be `null`. |

| Return ||
|---|---|
| OnBackInvokedCallback | This value cannot be `null`. |

**See Also**

- finishAndRemoveTask

### moveTaskToBackCallback

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun moveTaskToBackCallback(activity: Activity): OnBackInvokedCallback
```

Get a callback to triggers moveTaskToBack on the associated `https://developer.android.com/reference/kotlin/android/app/Activity.html#`, moving the task containing the activity to the background. The system will play the corresponding transition animation, regardless of whether the activity is the root activity of the task.

| Parameters ||
|---|---|
| `activity` | [Activity](../android.app/Activity.md): The associated `https://developer.android.com/reference/kotlin/android/app/Activity.html#` This value cannot be `null`. |

| Return ||
|---|---|
| OnBackInvokedCallback | This value cannot be `null`. |

**See Also**

- moveTaskToBack
