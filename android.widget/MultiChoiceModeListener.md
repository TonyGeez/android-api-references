# AbsListView.MultiChoiceModeListener

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MultiChoiceModeListener

Kotlin | [Java](https://developer.android.com/reference/android/widget/AbsListView.MultiChoiceModeListener "View this page in Java") 

```
interface MultiChoiceModeListener : ActionMode.Callback
```

| [android.widget.AbsListView.MultiChoiceModeListener](https://developer.android.com/reference/kotlin/android/widget/AbsListView.MultiChoiceModeListener#) |

A MultiChoiceModeListener receives events for [AbsListView.CHOICE_MODE_MULTIPLE_MODAL](https://developer.android.com/reference/kotlin/android/widget/AbsListView#CHOICE_MODE_MULTIPLE_MODAL:kotlin.Int). It acts as the [ActionMode.Callback](https://developer.android.com/reference/kotlin/android/view/ActionMode.Callback.html#) for the selection mode and also receives [onItemCheckedStateChanged(android.view.ActionMode,int,long,boolean)](https://developer.android.com/reference/kotlin/android/widget/AbsListView.MultiChoiceModeListener#onItemCheckedStateChanged(android.view.ActionMode,%20kotlin.Int,%20kotlin.Long,%20kotlin.Boolean)) events when the user selects and deselects list items.

## Summary

| Public methods ||
|---------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onItemCheckedStateChanged](https://developer.android.com/reference/kotlin/android/widget/AbsListView.MultiChoiceModeListener#onItemCheckedStateChanged(android.view.ActionMode,%20kotlin.Int,%20kotlin.Long,%20kotlin.Boolean))`(`mode:` ` [ActionMode](https://developer.android.com/reference/kotlin/android/view/ActionMode.html#)!`, `position:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `id:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `checked:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Called when an item is checked or unchecked during selection mode. |

| Inherited functions ||
|---|---|
| From class [Callback](https://developer.android.com/reference/kotlin/android/view/ActionMode.Callback.html#) |------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onActionItemClicked](https://developer.android.com/reference/kotlin/android/view/ActionMode.Callback.html#onActionItemClicked(android.view.ActionMode,%20android.view.MenuItem))`(`mode:` ` [ActionMode](https://developer.android.com/reference/kotlin/android/view/ActionMode.html#)!`, `item:` ` [MenuItem](https://developer.android.com/reference/kotlin/android/view/MenuItem.html#)!`)` Called to report a user click on an action button. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onCreateActionMode](https://developer.android.com/reference/kotlin/android/view/ActionMode.Callback.html#onCreateActionMode(android.view.ActionMode,%20android.view.Menu))`(`mode:` ` [ActionMode](https://developer.android.com/reference/kotlin/android/view/ActionMode.html#)!`, `menu:` ` [Menu](https://developer.android.com/reference/kotlin/android/view/Menu.html#)!`)` Called when action mode is first created. The menu supplied will be used to generate action buttons for the action mode. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onDestroyActionMode](https://developer.android.com/reference/kotlin/android/view/ActionMode.Callback.html#onDestroyActionMode(android.view.ActionMode))`(`mode:` ` [ActionMode](https://developer.android.com/reference/kotlin/android/view/ActionMode.html#)!`)` Called when an action mode is about to be exited and destroyed. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onPrepareActionMode](https://developer.android.com/reference/kotlin/android/view/ActionMode.Callback.html#onPrepareActionMode(android.view.ActionMode,%20android.view.Menu))`(`mode:` ` [ActionMode](https://developer.android.com/reference/kotlin/android/view/ActionMode.html#)!`, `menu:` ` [Menu](https://developer.android.com/reference/kotlin/android/view/Menu.html#)!`)` Called to refresh an action mode's action menu whenever it is invalidated. <br /> | ||

## Public methods

### onItemCheckedStateChanged

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onItemCheckedStateChanged(
    mode: ActionMode!, 
    position: Int, 
    id: Long, 
    checked: Boolean
): Unit
```

Called when an item is checked or unchecked during selection mode.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `mode` | [ActionMode](https://developer.android.com/reference/kotlin/android/view/ActionMode.html#)!: The [ActionMode](https://developer.android.com/reference/kotlin/android/view/ActionMode.html#) providing the selection mode |
| `position` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Adapter position of the item that was checked or unchecked |
| `id` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): Adapter ID of the item that was checked or unchecked |
| `checked` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): `true` if the item is now checked, `false` if the item is now unchecked. |
