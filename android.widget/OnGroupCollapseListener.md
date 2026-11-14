# ExpandableListView.OnGroupCollapseListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnGroupCollapseListener

Kotlin| [Java](../android/widget/ExpandableListView.OnGroupCollapseListener.md) 
| --- | --- |

```
interface OnGroupCollapseListener
```

| [android.widget.ExpandableListView.OnGroupCollapseListener](../android/widget/ExpandableListView.OnGroupCollapseListener.md) |

| Known Direct Subclasses [ExpandableListActivity](../android/app/ExpandableListActivity.md) |-------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [ExpandableListActivity](../android/app/ExpandableListActivity.md) | An activity that displays an expandable list of items by binding to a data source implementing the ExpandableListAdapter, and exposes event handlers when the user selects an item. | |
| --- | --- | --- | --- | --- | --- | --- |

Used for being notified when a group is collapsed

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onGroupCollapse](../android/widget/ExpandableListView.OnGroupCollapseListener.md))`(`groupPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Callback method to be invoked when a group in this expandable list has been collapsed. |

## Public methods

### onGroupCollapse

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onGroupCollapse(groupPosition: Int): Unit
```

Callback method to be invoked when a group in this expandable list has been collapsed.

| Parameters ||
|-----------------|------------------------------------------------------------------------------------------------------------------|
| `groupPosition` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The group position that was collapsed |
