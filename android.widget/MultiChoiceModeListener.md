# AbsListView.MultiChoiceModeListener

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MultiChoiceModeListener

Kotlin | [Java](../android/widget/AbsListView.MultiChoiceModeListener.md) 
| --- | --- |

```
interface MultiChoiceModeListener : ActionMode.Callback
```

| [android.widget.AbsListView.MultiChoiceModeListener](../android/widget/AbsListView.MultiChoiceModeListener.md) |

A MultiChoiceModeListener receives events for [AbsListView.CHOICE_MODE_MULTIPLE_MODAL](../android/widget/AbsListView.md). It acts as the [ActionMode.Callback](../android/view/ActionMode.Callback.md) for the selection mode and also receives [onItemCheckedStateChanged(android.view.ActionMode,int,long,boolean)](../android/widget/AbsListView.MultiChoiceModeListener.md)) events when the user selects and deselects list items.

## Summary

| Public methods ||
|---------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onItemCheckedStateChanged](../android/widget/AbsListView.MultiChoiceModeListener.md))`(`mode:` ` [ActionMode](../android/view/ActionMode.md)!`, `position:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `id:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `checked:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Called when an item is checked or unchecked during selection mode. |

| Inherited functions ||
|---|---|
| From class [Callback](../android/view/ActionMode.Callback.md) |------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onActionItemClicked](../android/view/ActionMode.Callback.md))`(`mode:` ` [ActionMode](../android/view/ActionMode.md)!`, `item:` ` [MenuItem](../android/view/MenuItem.md)!`)` Called to report a user click on an action button. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onCreateActionMode](../android/view/ActionMode.Callback.md))`(`mode:` ` [ActionMode](../android/view/ActionMode.md)!`, `menu:` ` [Menu](../android/view/Menu.md)!`)` Called when action mode is first created. The menu supplied will be used to generate action buttons for the action mode. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onDestroyActionMode](../android/view/ActionMode.Callback.md))`(`mode:` ` [ActionMode](../android/view/ActionMode.md)!`)` Called when an action mode is about to be exited and destroyed. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onPrepareActionMode](../android/view/ActionMode.Callback.md))`(`mode:` ` [ActionMode](../android/view/ActionMode.md)!`, `menu:` ` [Menu](../android/view/Menu.md)!`)` Called to refresh an action mode's action menu whenever it is invalidated. <br /> | ||

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
| `mode` | [ActionMode](../android/view/ActionMode.md)!: The [ActionMode](../android/view/ActionMode.md) providing the selection mode |
| `position` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Adapter position of the item that was checked or unchecked |
| `id` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): Adapter ID of the item that was checked or unchecked |
| --- | --- |
| `checked` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): `true` if the item is now checked, `false` if the item is now unchecked. |
