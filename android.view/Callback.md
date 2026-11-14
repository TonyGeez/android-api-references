# ActionMode.Callback

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Callback

Kotlin| [Java](../android/view/ActionMode.Callback.md) 
| --- | --- |

```
interface Callback
```

| [android.view.ActionMode.Callback](../android/view/ActionMode.Callback.md) |

| Known Direct Subclasses [AbsListView.MultiChoiceModeListener](../android/widget/AbsListView.MultiChoiceModeListener.md), [ActionMode.Callback2](../android/view/ActionMode.Callback2.md) |------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [AbsListView.MultiChoiceModeListener](../android/widget/AbsListView.MultiChoiceModeListener.md) | A MultiChoiceModeListener receives events for [AbsListView.CHOICE_MODE_MULTIPLE_MODAL](../android.widget/AbsListView.md). | | [ActionMode.Callback2](../android/view/ActionMode.Callback2.md) | Extension of [ActionMode.Callback](../android/view/ActionMode.Callback.md) to provide content rect information. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Callback interface for action modes. Supplied to [View.startActionMode(Callback)](View.md)), a Callback configures and handles events raised by a user's interaction with an action mode.

An action mode's lifecycle is as follows:

- [Callback.onCreateActionMode(ActionMode, Menu)](../android/view/ActionMode.Callback.md))once on initial creation
- [Callback.onPrepareActionMode(ActionMode, Menu)](../android/view/ActionMode.Callback.md))after creation and any time the [ActionMode](ActionMode.md) is invalidated
- [Callback.onActionItemClicked(ActionMode, MenuItem)](../android/view/ActionMode.Callback.md))any time a contextual action button is clicked
- [Callback.onDestroyActionMode(ActionMode)](../android/view/ActionMode.Callback.md))when the action mode is closed

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onActionItemClicked](../android/view/ActionMode.Callback.md))`(`mode:` ` [ActionMode](ActionMode.md)!`, `item:` ` [MenuItem](MenuItem.md)!`)` Called to report a user click on an action button. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onCreateActionMode](../android/view/ActionMode.Callback.md))`(`mode:` ` [ActionMode](ActionMode.md)!`, `menu:` ` [Menu](Menu.md)!`)` Called when action mode is first created. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onDestroyActionMode](../android/view/ActionMode.Callback.md))`(`mode:` ` [ActionMode](ActionMode.md)!`)` Called when an action mode is about to be exited and destroyed. |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onPrepareActionMode](../android/view/ActionMode.Callback.md))`(`mode:` ` [ActionMode](ActionMode.md)!`, `menu:` ` [Menu](Menu.md)!`)` Called to refresh an action mode's action menu whenever it is invalidated. |

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
| `mode` | [ActionMode](ActionMode.md)!:The current ActionMode |
| `item` | [MenuItem](MenuItem.md)!:The item that was clicked |

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
| `mode` | [ActionMode](ActionMode.md)!:ActionMode being created |
| `menu` | [Menu](Menu.md)!:Menu used to populate action buttons |

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
| `mode` | [ActionMode](ActionMode.md)!:The current ActionMode being destroyed |

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
| `mode` | [ActionMode](ActionMode.md)!:ActionMode being prepared |
| `menu` | [Menu](Menu.md)!:Menu used to populate action buttons |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the menu or action mode was updated, false otherwise. |
