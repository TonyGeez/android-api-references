# ActionMode.Callback

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Callback

Kotlin| [Java](https://developer.android.com/reference/android/view/ActionMode.Callback "View this page in Java") 

```
interface Callback
```

| [android.view.ActionMode.Callback](https://developer.android.com/reference/kotlin/android/view/ActionMode.Callback#) |

| Known Direct Subclasses [AbsListView.MultiChoiceModeListener](https://developer.android.com/reference/kotlin/android/widget/AbsListView.MultiChoiceModeListener.html#), [ActionMode.Callback2](https://developer.android.com/reference/kotlin/android/view/ActionMode.Callback2) |------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [AbsListView.MultiChoiceModeListener](https://developer.android.com/reference/kotlin/android/widget/AbsListView.MultiChoiceModeListener.html#) | A MultiChoiceModeListener receives events for [AbsListView.CHOICE_MODE_MULTIPLE_MODAL](https://developer.android.com/reference/kotlin/android/widget/AbsListView.html#CHOICE_MODE_MULTIPLE_MODAL:kotlin.Int). | | [ActionMode.Callback2](https://developer.android.com/reference/kotlin/android/view/ActionMode.Callback2) | Extension of [ActionMode.Callback](https://developer.android.com/reference/kotlin/android/view/ActionMode.Callback#) to provide content rect information. | |

Callback interface for action modes. Supplied to [View.startActionMode(Callback)](https://developer.android.com/reference/kotlin/android/view/View#startActionMode(android.view.ActionMode.Callback)), a Callback configures and handles events raised by a user's interaction with an action mode.

An action mode's lifecycle is as follows:

- [Callback.onCreateActionMode(ActionMode, Menu)](https://developer.android.com/reference/kotlin/android/view/ActionMode.Callback#onCreateActionMode(android.view.ActionMode,%20android.view.Menu))once on initial creation
- [Callback.onPrepareActionMode(ActionMode, Menu)](https://developer.android.com/reference/kotlin/android/view/ActionMode.Callback#onPrepareActionMode(android.view.ActionMode,%20android.view.Menu))after creation and any time the [ActionMode](https://developer.android.com/reference/kotlin/android/view/ActionMode) is invalidated
- [Callback.onActionItemClicked(ActionMode, MenuItem)](https://developer.android.com/reference/kotlin/android/view/ActionMode.Callback#onActionItemClicked(android.view.ActionMode,%20android.view.MenuItem))any time a contextual action button is clicked
- [Callback.onDestroyActionMode(ActionMode)](https://developer.android.com/reference/kotlin/android/view/ActionMode.Callback#onDestroyActionMode(android.view.ActionMode))when the action mode is closed

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onActionItemClicked](https://developer.android.com/reference/kotlin/android/view/ActionMode.Callback#onActionItemClicked(android.view.ActionMode,%20android.view.MenuItem))`(`mode:` ` [ActionMode](https://developer.android.com/reference/kotlin/android/view/ActionMode)!`, `item:` ` [MenuItem](https://developer.android.com/reference/kotlin/android/view/MenuItem)!`)` Called to report a user click on an action button. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onCreateActionMode](https://developer.android.com/reference/kotlin/android/view/ActionMode.Callback#onCreateActionMode(android.view.ActionMode,%20android.view.Menu))`(`mode:` ` [ActionMode](https://developer.android.com/reference/kotlin/android/view/ActionMode)!`, `menu:` ` [Menu](https://developer.android.com/reference/kotlin/android/view/Menu)!`)` Called when action mode is first created. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onDestroyActionMode](https://developer.android.com/reference/kotlin/android/view/ActionMode.Callback#onDestroyActionMode(android.view.ActionMode))`(`mode:` ` [ActionMode](https://developer.android.com/reference/kotlin/android/view/ActionMode)!`)` Called when an action mode is about to be exited and destroyed. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onPrepareActionMode](https://developer.android.com/reference/kotlin/android/view/ActionMode.Callback#onPrepareActionMode(android.view.ActionMode,%20android.view.Menu))`(`mode:` ` [ActionMode](https://developer.android.com/reference/kotlin/android/view/ActionMode)!`, `menu:` ` [Menu](https://developer.android.com/reference/kotlin/android/view/Menu)!`)` Called to refresh an action mode's action menu whenever it is invalidated. |

## Public methods

### onActionItemClicked

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onActionItemClicked(
    mode: ActionMode!, 
    item: MenuItem!
): Boolean
```

Called to report a user click on an action button.

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------|
| `mode` | [ActionMode](https://developer.android.com/reference/kotlin/android/view/ActionMode)!:The current ActionMode |
| `item` | [MenuItem](https://developer.android.com/reference/kotlin/android/view/MenuItem)!:The item that was clicked |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if this callback handled the event, false if the standard MenuItem invocation should continue. |

### onCreateActionMode

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onCreateActionMode(
    mode: ActionMode!, 
    menu: Menu!
): Boolean
```

Called when action mode is first created. The menu supplied will be used to generate action buttons for the action mode.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------|
| `mode` | [ActionMode](https://developer.android.com/reference/kotlin/android/view/ActionMode)!:ActionMode being created |
| `menu` | [Menu](https://developer.android.com/reference/kotlin/android/view/Menu)!:Menu used to populate action buttons |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the action mode should be created, false if entering this mode should be aborted. |

### onDestroyActionMode

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onDestroyActionMode(mode: ActionMode!): Unit
```

Called when an action mode is about to be exited and destroyed.

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------------------------------|
| `mode` | [ActionMode](https://developer.android.com/reference/kotlin/android/view/ActionMode)!:The current ActionMode being destroyed |

### onPrepareActionMode

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onPrepareActionMode(
    mode: ActionMode!, 
    menu: Menu!
): Boolean
```

Called to refresh an action mode's action menu whenever it is invalidated.

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------------|
| `mode` | [ActionMode](https://developer.android.com/reference/kotlin/android/view/ActionMode)!:ActionMode being prepared |
| `menu` | [Menu](https://developer.android.com/reference/kotlin/android/view/Menu)!:Menu used to populate action buttons |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the menu or action mode was updated, false otherwise. |
