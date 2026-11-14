# ExpandableListView.OnChildClickListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnChildClickListener

Kotlin| [Java](../android/widget/ExpandableListView.OnChildClickListener.md) 
| --- | --- |

```
interface OnChildClickListener
```

| [android.widget.ExpandableListView.OnChildClickListener](../android/widget/ExpandableListView.OnChildClickListener.md) |

| Known Direct Subclasses [ExpandableListActivity](../android.app/ExpandableListActivity.md) |-------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [ExpandableListActivity](../android.app/ExpandableListActivity.md) | An activity that displays an expandable list of items by binding to a data source implementing the ExpandableListAdapter, and exposes event handlers when the user selects an item. | |
| --- | --- | --- | --- | --- | --- | --- |

Interface definition for a callback to be invoked when a child in this expandable list has been clicked.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onChildClick](../android/widget/ExpandableListView.OnChildClickListener.md))`(`parent:` ` [ExpandableListView](ExpandableListView.md)!`, `v:` ` [View](../android.view/View.md)!`, `groupPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `childPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `id:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Callback method to be invoked when a child in this expandable list has been clicked. |

## Public methods

### onChildClick

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onChildClick(
    parent: ExpandableListView!, 
    v: View!, 
    groupPosition: Int, 
    childPosition: Int, 
    id: Long
): Boolean
```

Callback method to be invoked when a child in this expandable list has been clicked.

| Parameters ||
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| `parent` | [ExpandableListView](ExpandableListView.md)!:The ExpandableListView where the click happened |
| `v` | [View](../android.view/View.md)!:The view within the expandable list/ListView that was clicked |
| `groupPosition` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The group position that contains the child that was clicked |
| --- | --- |
| `childPosition` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The child position within the group |
| `id` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The row id of the child that was clicked |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if the click was handled |
