# ExpandableListView.OnGroupClickListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnGroupClickListener

Kotlin| [Java](../android/widget/ExpandableListView.OnGroupClickListener.md) 
| --- | --- |

```
interface OnGroupClickListener
```

| [android.widget.ExpandableListView.OnGroupClickListener](../android/widget/ExpandableListView.OnGroupClickListener.md) |

Interface definition for a callback to be invoked when a group in this expandable list has been clicked.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onGroupClick](../android/widget/ExpandableListView.OnGroupClickListener.md))`(`parent:` ` [ExpandableListView](ExpandableListView.md)!`, `v:` ` [View](../android.view/View.md)!`, `groupPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `id:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Callback method to be invoked when a group in this expandable list has been clicked. |

## Public methods

### onGroupClick

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onGroupClick(
    parent: ExpandableListView!, 
    v: View!, 
    groupPosition: Int, 
    id: Long
): Boolean
```

Callback method to be invoked when a group in this expandable list has been clicked.

| Parameters ||
|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `parent` | [ExpandableListView](ExpandableListView.md)!:The ExpandableListConnector where the click happened |
| `v` | [View](../android.view/View.md)!:The view within the expandable list/ListView that was clicked |
| `groupPosition` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The group position that was clicked |
| --- | --- |
| `id` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The row id of the group that was clicked |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if the click was handled |
