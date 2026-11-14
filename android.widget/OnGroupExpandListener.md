# ExpandableListView.OnGroupExpandListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnGroupExpandListener

Kotlin| [Java](https://developer.android.com/reference/android/widget/ExpandableListView.OnGroupExpandListener "View this page in Java") 
| --- | --- |

```
interface OnGroupExpandListener
```

| [android.widget.ExpandableListView.OnGroupExpandListener](https://developer.android.com/reference/kotlin/android/widget/ExpandableListView.OnGroupExpandListener#) |

| Known Direct Subclasses [ExpandableListActivity](https://developer.android.com/reference/kotlin/android/app/ExpandableListActivity.html#) |-------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [ExpandableListActivity](https://developer.android.com/reference/kotlin/android/app/ExpandableListActivity.html#) | An activity that displays an expandable list of items by binding to a data source implementing the ExpandableListAdapter, and exposes event handlers when the user selects an item. | |
| --- | --- | --- | --- | --- | --- | --- |

Used for being notified when a group is expanded

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onGroupExpand](https://developer.android.com/reference/kotlin/android/widget/ExpandableListView.OnGroupExpandListener#onGroupExpand(kotlin.Int))`(`groupPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Callback method to be invoked when a group in this expandable list has been expanded. |

## Public methods

### onGroupExpand

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onGroupExpand(groupPosition: Int): Unit
```

Callback method to be invoked when a group in this expandable list has been expanded.

| Parameters ||
|-----------------|-----------------------------------------------------------------------------------------------------------------|
| `groupPosition` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The group position that was expanded |
