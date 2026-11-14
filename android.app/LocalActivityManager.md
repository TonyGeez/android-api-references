# LocalActivityManager

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 13](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# LocalActivityManager

Kotlin| [Java](../android/app/LocalActivityManager.md) 
| --- | --- |

```
open class LocalActivityManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.app.LocalActivityManager](../android/app/LocalActivityManager.md) |

| **This class was deprecated in API level 13.**
|
| Use the new [Fragment](../android/app/Fragment.md) and [FragmentManager](../android/app/FragmentManager.md) APIs instead; these are also available on older platforms through the Android compatibility package.

Helper class for managing multiple running embedded activities in the same process. This class is not normally used directly, but rather created for you as part of the [android.app.ActivityGroup](../android/app/ActivityGroup.md) implementation.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [LocalActivityManager](../android/app/LocalActivityManager.md))`(`parent:` ` [Activity](../android/app/Activity.md)!`, `singleMode:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Create a new LocalActivityManager for holding activities running within the given parent. |

| Public methods ||
|-----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Window](../android/view/Window.md)! | [destroyActivity](../android/app/LocalActivityManager.md))`(`id:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `finish:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Destroy the activity associated with a particular id. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [dispatchCreate](../android/app/LocalActivityManager.md))`(`state:` ` [Bundle](../android/os/Bundle.md)!`)` Restore a state that was previously returned by [saveInstanceState](../android/app/LocalActivityManager.md)). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [dispatchDestroy](../android/app/LocalActivityManager.md))`(`finishing:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Called by the container activity in its [Activity.onDestroy](../android/app/Activity.md))so that LocalActivityManager can perform the corresponding action on the activities it holds. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [dispatchPause](../android/app/LocalActivityManager.md))`(`finishing:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Called by the container activity in its [Activity.onPause](../android/app/Activity.md))so that LocalActivityManager can perform the corresponding action on the activities it holds. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [dispatchResume](../android/app/LocalActivityManager.md))`()` Called by the container activity in its [Activity.onResume](../android/app/Activity.md))so that LocalActivityManager can perform the corresponding action on the activities it holds. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [dispatchStop](../android/app/LocalActivityManager.md))`()` Called by the container activity in its [Activity.onStop](../android/app/Activity.md))so that LocalActivityManager can perform the corresponding action on the activities it holds. |
| --- | --- |
| open [Activity](../android/app/Activity.md)! | [getActivity](../android/app/LocalActivityManager.md))`(`id:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Return the Activity object associated with a string ID. |
| open [Activity](../android/app/Activity.md)! | [getCurrentActivity](../android/app/LocalActivityManager.md))`()` Retrieve the Activity that is currently running. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getCurrentId](../android/app/LocalActivityManager.md))`()` Retrieve the ID of the activity that is currently running. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeAllActivities](../android/app/LocalActivityManager.md))`()` Remove all activities from this LocalActivityManager, performing an [Activity.onDestroy](../android/app/Activity.md))on any that are currently instantiated. |
| open [Bundle](../android/os/Bundle.md)! | [saveInstanceState](../android/app/LocalActivityManager.md))`()` Retrieve the state of all activities known by the group. |
| open [Window](../android/view/Window.md)! | [startActivity](../android/app/LocalActivityManager.md))`(`id:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `intent:` ` [Intent](../android/content/Intent.md)!`)` Start a new activity running in the group. |
| --- | --- |

## Public constructors

### LocalActivityManager

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
LocalActivityManager(
    parent: Activity!, 
    singleMode: Boolean)
```

Create a new LocalActivityManager for holding activities running within the given parent.

| Parameters ||
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `parent` | [Activity](../android/app/Activity.md)!:the host of the embedded activities |
| `singleMode` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):True if the LocalActivityManger should keep a maximum of one activity resumed |

## Public methods

### destroyActivity

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun destroyActivity(
    id: String!, 
    finish: Boolean
): Window!
```

**Deprecated:** *Deprecated in Java.*

Destroy the activity associated with a particular id. This activity will go through the normal lifecycle events and fine onDestroy(), and then the id removed from the group.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `id` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:Unique identifier of the activity to be destroyed |
| `finish` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):If true, this activity will be finished, so its id and all state are removed from the group. |

| Return ||
|-------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [Window](../android/view/Window.md)! | Returns the window that was used to display the activity, or null if there was none. |

### dispatchCreate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun dispatchCreate(state: Bundle!): Unit
```

**Deprecated:** *Deprecated in Java.*

Restore a state that was previously returned by [saveInstanceState](../android/app/LocalActivityManager.md)). This adds to the activity group information about all activity IDs that had previously been saved, even if they have not been started yet, so if the user later navigates to them the correct state will be restored.

Note: This does**not**change the current running activity, or start whatever activity was previously running when the state was saved. That is up to the client to do, in whatever way it thinks is best.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------|
| `state` | [Bundle](../android/os/Bundle.md)!:a previously saved state; does nothing if this is null |

**See Also**

- [#saveInstanceState](../android/app/LocalActivityManager.md)) 

### dispatchDestroy

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun dispatchDestroy(finishing: Boolean): Unit
```

**Deprecated:** *Deprecated in Java.*

Called by the container activity in its [Activity.onDestroy](../android/app/Activity.md))so that LocalActivityManager can perform the corresponding action on the activities it holds. 
**See Also**

- [android.app.Activity#onDestroy](../android/app/Activity.md)) 

### dispatchPause

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun dispatchPause(finishing: Boolean): Unit
```

**Deprecated:** *Deprecated in Java.*

Called by the container activity in its [Activity.onPause](../android/app/Activity.md))so that LocalActivityManager can perform the corresponding action on the activities it holds.

| Parameters ||
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `finishing` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):set to true if the parent activity has been finished; this can be determined by calling Activity.isFinishing() |

**See Also**

- [android.app.Activity#onPause](../android/app/Activity.md))
- [android.app.Activity#isFinishing](../android/app/Activity.md)) 

### dispatchResume

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun dispatchResume(): Unit
```

**Deprecated:** *Deprecated in Java.*

Called by the container activity in its [Activity.onResume](../android/app/Activity.md))so that LocalActivityManager can perform the corresponding action on the activities it holds. 
**See Also**

- [android.app.Activity#onResume](../android/app/Activity.md)) 

### dispatchStop

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun dispatchStop(): Unit
```

**Deprecated:** *Deprecated in Java.*

Called by the container activity in its [Activity.onStop](../android/app/Activity.md))so that LocalActivityManager can perform the corresponding action on the activities it holds. 
**See Also**

- [android.app.Activity#onStop](../android/app/Activity.md)) 

### getActivity

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getActivity(id: String!): Activity!
```

**Deprecated:** *Deprecated in Java.*

Return the Activity object associated with a string ID.

| Return ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [Activity](../android/app/Activity.md)! | the associated Activity object, or null if the id is unknown or its activity is not currently instantiated |

**See Also**

- [#startActivity](../android/app/LocalActivityManager.md)) 

### getCurrentActivity

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getCurrentActivity(): Activity!
```

**Deprecated:** *Deprecated in Java.*

Retrieve the Activity that is currently running.

| Return ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [Activity](../android/app/Activity.md)! | the currently running (resumed) Activity, or null if there is not one |

**See Also**

- [#startActivity](../android/app/LocalActivityManager.md))
- [#getCurrentId](../android/app/LocalActivityManager.md)) 

### getCurrentId

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getCurrentId(): String!
```

**Deprecated:** *Deprecated in Java.*

Retrieve the ID of the activity that is currently running.

| Return ||
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the ID of the currently running (resumed) Activity, or null if there is not one |

**See Also**

- [#startActivity](../android/app/LocalActivityManager.md))
- [#getCurrentActivity](../android/app/LocalActivityManager.md)) 

### removeAllActivities

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun removeAllActivities(): Unit
```

**Deprecated:** *Deprecated in Java.*

Remove all activities from this LocalActivityManager, performing an [Activity.onDestroy](../android/app/Activity.md))on any that are currently instantiated. 

### saveInstanceState

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun saveInstanceState(): Bundle!
```

**Deprecated:** *Deprecated in Java.*

Retrieve the state of all activities known by the group. For activities that have previously run and are now stopped or finished, the last saved state is used. For the current running activity, its android.app.Activity#onSaveInstanceState is called to retrieve its current state.

| Return ||
|-----------------------------------------------------------------------------------|------------------------------------------------------------------|
| [Bundle](../android/os/Bundle.md)! | a Bundle holding the newly created state of all known activities |

**See Also**

- [#dispatchCreate](../android/app/LocalActivityManager.md)) 

### startActivity

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun startActivity(
    id: String!, 
    intent: Intent!
): Window!
```

**Deprecated:** *Deprecated in Java.*

Start a new activity running in the group. Every activity you start must have a unique string ID associated with it -- this is used to keep track of the activity, so that if you later call startActivity() again on it the same activity object will be retained.

When there had previously been an activity started under this id, it may either be destroyed and a new one started, or the current one re-used, based on these conditions, in order:

- If the Intent maps to a different activity component than is currently running, the current activity is finished and a new one started.
- If the current activity uses a non-multiple launch mode (such as singleTop), or the Intent has the [Intent.FLAG_ACTIVITY_SINGLE_TOP](../android/content/Intent.md) flag set, then the current activity will remain running and its [Activity.onNewIntent()](../android/app/Activity.md))method called.
- If the new Intent is the same (excluding extras) as the previous one, and the new Intent does not have the [Intent.FLAG_ACTIVITY_CLEAR_TOP](../android/content/Intent.md) set, then the current activity will remain running as-is.
- Otherwise, the current activity will be finished and a new one started.

If the given Intent can not be resolved to an available Activity, this method throws [android.content.ActivityNotFoundException](../android/content/ActivityNotFoundException.md).

Warning: There is an issue where, if the Intent does not include an explicit component, we can restore the state for a different activity class than was previously running when the state was saved (if the set of available activities changes between those points).

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------|
| `id` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:Unique identifier of the activity to be started |
| `intent` | [Intent](../android/content/Intent.md)!:The Intent describing the activity to be started |

| Return ||
|-------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Window](../android/view/Window.md)! | Returns the window of the activity. The caller needs to take care of adding this window to a view hierarchy, and likewise dealing with removing the old window if the activity has changed. |

| Exceptions ||
|---------------------------------------------|---|
| `android.content.ActivityNotFoundException` | |
