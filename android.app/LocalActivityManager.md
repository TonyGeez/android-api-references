# LocalActivityManager

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 13](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# LocalActivityManager

Kotlin| [Java](https://developer.android.com/reference/android/app/LocalActivityManager "View this page in Java") 

```
open class LocalActivityManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.app.LocalActivityManager](https://developer.android.com/reference/kotlin/android/app/LocalActivityManager#) |

| **This class was deprecated in API level 13.**
|
| Use the new [Fragment](https://developer.android.com/reference/kotlin/android/app/Fragment) and [FragmentManager](https://developer.android.com/reference/kotlin/android/app/FragmentManager) APIs instead; these are also available on older platforms through the Android compatibility package.

Helper class for managing multiple running embedded activities in the same process. This class is not normally used directly, but rather created for you as part of the [android.app.ActivityGroup](https://developer.android.com/reference/kotlin/android/app/ActivityGroup) implementation.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [LocalActivityManager](https://developer.android.com/reference/kotlin/android/app/LocalActivityManager#LocalActivityManager(android.app.Activity,%20kotlin.Boolean))`(`parent:` ` [Activity](https://developer.android.com/reference/kotlin/android/app/Activity)!`, `singleMode:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Create a new LocalActivityManager for holding activities running within the given parent. |

| Public methods ||
|-----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Window](https://developer.android.com/reference/kotlin/android/view/Window.html#)! | [destroyActivity](https://developer.android.com/reference/kotlin/android/app/LocalActivityManager#destroyActivity(kotlin.String,%20kotlin.Boolean))`(`id:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `finish:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Destroy the activity associated with a particular id. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [dispatchCreate](https://developer.android.com/reference/kotlin/android/app/LocalActivityManager#dispatchCreate(android.os.Bundle))`(`state:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!`)` Restore a state that was previously returned by [saveInstanceState](https://developer.android.com/reference/kotlin/android/app/LocalActivityManager#saveInstanceState()). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [dispatchDestroy](https://developer.android.com/reference/kotlin/android/app/LocalActivityManager#dispatchDestroy(kotlin.Boolean))`(`finishing:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Called by the container activity in its [Activity.onDestroy](https://developer.android.com/reference/kotlin/android/app/Activity#onDestroy())so that LocalActivityManager can perform the corresponding action on the activities it holds. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [dispatchPause](https://developer.android.com/reference/kotlin/android/app/LocalActivityManager#dispatchPause(kotlin.Boolean))`(`finishing:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Called by the container activity in its [Activity.onPause](https://developer.android.com/reference/kotlin/android/app/Activity#onPause())so that LocalActivityManager can perform the corresponding action on the activities it holds. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [dispatchResume](https://developer.android.com/reference/kotlin/android/app/LocalActivityManager#dispatchResume())`()` Called by the container activity in its [Activity.onResume](https://developer.android.com/reference/kotlin/android/app/Activity#onResume())so that LocalActivityManager can perform the corresponding action on the activities it holds. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [dispatchStop](https://developer.android.com/reference/kotlin/android/app/LocalActivityManager#dispatchStop())`()` Called by the container activity in its [Activity.onStop](https://developer.android.com/reference/kotlin/android/app/Activity#onStop())so that LocalActivityManager can perform the corresponding action on the activities it holds. |
| open [Activity](https://developer.android.com/reference/kotlin/android/app/Activity)! | [getActivity](https://developer.android.com/reference/kotlin/android/app/LocalActivityManager#getActivity(kotlin.String))`(`id:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Return the Activity object associated with a string ID. |
| open [Activity](https://developer.android.com/reference/kotlin/android/app/Activity)! | [getCurrentActivity](https://developer.android.com/reference/kotlin/android/app/LocalActivityManager#getCurrentActivity())`()` Retrieve the Activity that is currently running. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getCurrentId](https://developer.android.com/reference/kotlin/android/app/LocalActivityManager#getCurrentId())`()` Retrieve the ID of the activity that is currently running. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeAllActivities](https://developer.android.com/reference/kotlin/android/app/LocalActivityManager#removeAllActivities())`()` Remove all activities from this LocalActivityManager, performing an [Activity.onDestroy](https://developer.android.com/reference/kotlin/android/app/Activity#onDestroy())on any that are currently instantiated. |
| open [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)! | [saveInstanceState](https://developer.android.com/reference/kotlin/android/app/LocalActivityManager#saveInstanceState())`()` Retrieve the state of all activities known by the group. |
| open [Window](https://developer.android.com/reference/kotlin/android/view/Window.html#)! | [startActivity](https://developer.android.com/reference/kotlin/android/app/LocalActivityManager#startActivity(kotlin.String,%20android.content.Intent))`(`id:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `intent:` ` [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#)!`)` Start a new activity running in the group. |

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
| `parent` | [Activity](https://developer.android.com/reference/kotlin/android/app/Activity)!:the host of the embedded activities |
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
| [Window](https://developer.android.com/reference/kotlin/android/view/Window.html#)! | Returns the window that was used to display the activity, or null if there was none. |

### dispatchCreate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun dispatchCreate(state: Bundle!): Unit
```

**Deprecated:** *Deprecated in Java.*

Restore a state that was previously returned by [saveInstanceState](https://developer.android.com/reference/kotlin/android/app/LocalActivityManager#saveInstanceState()). This adds to the activity group information about all activity IDs that had previously been saved, even if they have not been started yet, so if the user later navigates to them the correct state will be restored.

Note: This does**not**change the current running activity, or start whatever activity was previously running when the state was saved. That is up to the client to do, in whatever way it thinks is best.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------|
| `state` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!:a previously saved state; does nothing if this is null |

**See Also**

- [#saveInstanceState](https://developer.android.com/reference/kotlin/android/app/LocalActivityManager#saveInstanceState()) 

### dispatchDestroy

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun dispatchDestroy(finishing: Boolean): Unit
```

**Deprecated:** *Deprecated in Java.*

Called by the container activity in its [Activity.onDestroy](https://developer.android.com/reference/kotlin/android/app/Activity#onDestroy())so that LocalActivityManager can perform the corresponding action on the activities it holds. 
**See Also**

- [android.app.Activity#onDestroy](https://developer.android.com/reference/kotlin/android/app/Activity#onDestroy()) 

### dispatchPause

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun dispatchPause(finishing: Boolean): Unit
```

**Deprecated:** *Deprecated in Java.*

Called by the container activity in its [Activity.onPause](https://developer.android.com/reference/kotlin/android/app/Activity#onPause())so that LocalActivityManager can perform the corresponding action on the activities it holds.

| Parameters ||
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `finishing` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):set to true if the parent activity has been finished; this can be determined by calling Activity.isFinishing() |

**See Also**

- [android.app.Activity#onPause](https://developer.android.com/reference/kotlin/android/app/Activity#onPause())
- [android.app.Activity#isFinishing](https://developer.android.com/reference/kotlin/android/app/Activity#isFinishing()) 

### dispatchResume

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun dispatchResume(): Unit
```

**Deprecated:** *Deprecated in Java.*

Called by the container activity in its [Activity.onResume](https://developer.android.com/reference/kotlin/android/app/Activity#onResume())so that LocalActivityManager can perform the corresponding action on the activities it holds. 
**See Also**

- [android.app.Activity#onResume](https://developer.android.com/reference/kotlin/android/app/Activity#onResume()) 

### dispatchStop

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun dispatchStop(): Unit
```

**Deprecated:** *Deprecated in Java.*

Called by the container activity in its [Activity.onStop](https://developer.android.com/reference/kotlin/android/app/Activity#onStop())so that LocalActivityManager can perform the corresponding action on the activities it holds. 
**See Also**

- [android.app.Activity#onStop](https://developer.android.com/reference/kotlin/android/app/Activity#onStop()) 

### getActivity

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getActivity(id: String!): Activity!
```

**Deprecated:** *Deprecated in Java.*

Return the Activity object associated with a string ID.

| Return ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [Activity](https://developer.android.com/reference/kotlin/android/app/Activity)! | the associated Activity object, or null if the id is unknown or its activity is not currently instantiated |

**See Also**

- [#startActivity](https://developer.android.com/reference/kotlin/android/app/LocalActivityManager#startActivity(kotlin.String,%20android.content.Intent)) 

### getCurrentActivity

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getCurrentActivity(): Activity!
```

**Deprecated:** *Deprecated in Java.*

Retrieve the Activity that is currently running.

| Return ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [Activity](https://developer.android.com/reference/kotlin/android/app/Activity)! | the currently running (resumed) Activity, or null if there is not one |

**See Also**

- [#startActivity](https://developer.android.com/reference/kotlin/android/app/LocalActivityManager#startActivity(kotlin.String,%20android.content.Intent))
- [#getCurrentId](https://developer.android.com/reference/kotlin/android/app/LocalActivityManager#getCurrentId()) 

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

- [#startActivity](https://developer.android.com/reference/kotlin/android/app/LocalActivityManager#startActivity(kotlin.String,%20android.content.Intent))
- [#getCurrentActivity](https://developer.android.com/reference/kotlin/android/app/LocalActivityManager#getCurrentActivity()) 

### removeAllActivities

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun removeAllActivities(): Unit
```

**Deprecated:** *Deprecated in Java.*

Remove all activities from this LocalActivityManager, performing an [Activity.onDestroy](https://developer.android.com/reference/kotlin/android/app/Activity#onDestroy())on any that are currently instantiated. 

### saveInstanceState

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun saveInstanceState(): Bundle!
```

**Deprecated:** *Deprecated in Java.*

Retrieve the state of all activities known by the group. For activities that have previously run and are now stopped or finished, the last saved state is used. For the current running activity, its android.app.Activity#onSaveInstanceState is called to retrieve its current state.

| Return ||
|-----------------------------------------------------------------------------------|------------------------------------------------------------------|
| [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)! | a Bundle holding the newly created state of all known activities |

**See Also**

- [#dispatchCreate](https://developer.android.com/reference/kotlin/android/app/LocalActivityManager#dispatchCreate(android.os.Bundle)) 

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
- If the current activity uses a non-multiple launch mode (such as singleTop), or the Intent has the [Intent.FLAG_ACTIVITY_SINGLE_TOP](https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_ACTIVITY_SINGLE_TOP:kotlin.Int) flag set, then the current activity will remain running and its [Activity.onNewIntent()](https://developer.android.com/reference/kotlin/android/app/Activity#onNewIntent(android.content.Intent))method called.
- If the new Intent is the same (excluding extras) as the previous one, and the new Intent does not have the [Intent.FLAG_ACTIVITY_CLEAR_TOP](https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_ACTIVITY_CLEAR_TOP:kotlin.Int) set, then the current activity will remain running as-is.
- Otherwise, the current activity will be finished and a new one started.

If the given Intent can not be resolved to an available Activity, this method throws [android.content.ActivityNotFoundException](https://developer.android.com/reference/kotlin/android/content/ActivityNotFoundException.html#).

Warning: There is an issue where, if the Intent does not include an explicit component, we can restore the state for a different activity class than was previously running when the state was saved (if the set of available activities changes between those points).

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------|
| `id` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:Unique identifier of the activity to be started |
| `intent` | [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#)!:The Intent describing the activity to be started |

| Return ||
|-------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Window](https://developer.android.com/reference/kotlin/android/view/Window.html#)! | Returns the window of the activity. The caller needs to take care of adding this window to a view hierarchy, and likewise dealing with removing the old window if the activity has changed. |

| Exceptions ||
|---------------------------------------------|---|
| `android.content.ActivityNotFoundException` | |
