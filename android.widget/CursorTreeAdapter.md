Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CursorTreeAdapter

Kotlin | [Java](https://developer.android.com/reference/android/widget/CursorTreeAdapter "View this page in Java")
| --- | --- |

```
abstract class CursorTreeAdapter : BaseExpandableListAdapter, Filterable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.widget.BaseExpandableListAdapter](https://developer.android.com/reference/kotlin/android/widget/BaseExpandableListAdapter) ||
| | ↳ | [android.widget.CursorTreeAdapter](https://developer.android.com/reference/kotlin/android/widget/CursorTreeAdapter#) |

| Known Direct Subclasses [ResourceCursorTreeAdapter](https://developer.android.com/reference/kotlin/android/widget/ResourceCursorTreeAdapter) |---|---| | [ResourceCursorTreeAdapter](https://developer.android.com/reference/kotlin/android/widget/ResourceCursorTreeAdapter) | A fairly simple ExpandableListAdapter that creates views defined in an XML file. | |
| --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [SimpleCursorTreeAdapter](https://developer.android.com/reference/kotlin/android/widget/SimpleCursorTreeAdapter) |---|---| | [SimpleCursorTreeAdapter](https://developer.android.com/reference/kotlin/android/widget/SimpleCursorTreeAdapter) | An easy adapter to map columns from a cursor to TextViews or ImageViews defined in an XML file. | |
| --- | --- | --- | --- | --- | --- | --- |

An adapter that exposes data from a series of `https://developer.android.com/reference/kotlin/android/database/Cursor.html#`s to an `https://developer.android.com/reference/kotlin/android/widget/ExpandableListView` widget. The top-level `https://developer.android.com/reference/kotlin/android/database/Cursor.html#` (that is given in the constructor) exposes the groups, while subsequent `https://developer.android.com/reference/kotlin/android/database/Cursor.html#`s returned from `https://developer.android.com/reference/kotlin/android/widget/CursorTreeAdapter#getChildrenCursor(android.database.Cursor)` expose children within a particular group. The Cursors must include a column named "_id" or this class will not work.

## Summary

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/widget/CursorTreeAdapter#CursorTreeAdapter(android.database.Cursor,%20android.content.Context)(cursor: https://developer.android.com/reference/kotlin/android/database/Cursor.html#!, context: https://developer.android.com/reference/kotlin/android/content/Context.html#!)` Constructor. |
| `https://developer.android.com/reference/kotlin/android/widget/CursorTreeAdapter#CursorTreeAdapter(android.database.Cursor,%20android.content.Context,%20kotlin.Boolean)(cursor: https://developer.android.com/reference/kotlin/android/database/Cursor.html#!, context: https://developer.android.com/reference/kotlin/android/content/Context.html#!, autoRequery: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Constructor. |

| Public methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/widget/CursorTreeAdapter#changeCursor(android.database.Cursor)(cursor: https://developer.android.com/reference/kotlin/android/database/Cursor.html#!)` <br /> |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/widget/CursorTreeAdapter#convertToString(android.database.Cursor)(cursor: https://developer.android.com/reference/kotlin/android/database/Cursor.html#!)` <br /> |
| open [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#)! | `https://developer.android.com/reference/kotlin/android/widget/CursorTreeAdapter#getChild(kotlin.Int,%20kotlin.Int)(groupPosition: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, childPosition: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Gets the data associated with the given child within the given group. |
| --- | --- |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/widget/CursorTreeAdapter#getChildId(kotlin.Int,%20kotlin.Int)(groupPosition: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, childPosition: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Gets the ID for the given child within the given group. |
| open [View](https://developer.android.com/reference/kotlin/android/view/View.html#)! | `https://developer.android.com/reference/kotlin/android/widget/CursorTreeAdapter#getChildView(kotlin.Int,%20kotlin.Int,%20kotlin.Boolean,%20android.view.View,%20android.view.ViewGroup)(groupPosition: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, childPosition: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, isLastChild: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html, convertView: https://developer.android.com/reference/kotlin/android/view/View.html#!, parent: https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#!)` Gets a View that displays the data for the given child within the given group. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/widget/CursorTreeAdapter#getChildrenCount(kotlin.Int)(groupPosition: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Gets the number of children in a specified group. |
| --- | --- |
| open [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#)! | `https://developer.android.com/reference/kotlin/android/widget/CursorTreeAdapter#getCursor()()` <br /> |
| open [Filter](https://developer.android.com/reference/kotlin/android/widget/Filter)! | `https://developer.android.com/reference/kotlin/android/widget/CursorTreeAdapter#getFilter()()` Returns a filter that can be used to constrain data with a filtering pattern. |
| open [FilterQueryProvider](https://developer.android.com/reference/kotlin/android/widget/FilterQueryProvider)! | `https://developer.android.com/reference/kotlin/android/widget/CursorTreeAdapter#getFilterQueryProvider()()` <br /> |
| --- | --- |
| open [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#)! | `https://developer.android.com/reference/kotlin/android/widget/CursorTreeAdapter#getGroup(kotlin.Int)(groupPosition: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Gets the data associated with the given group. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/widget/CursorTreeAdapter#getGroupCount()()` Gets the number of groups. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/widget/CursorTreeAdapter#getGroupId(kotlin.Int)(groupPosition: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Gets the ID for the group at the given position. |
| --- | --- |
| open [View](https://developer.android.com/reference/kotlin/android/view/View.html#)! | `https://developer.android.com/reference/kotlin/android/widget/CursorTreeAdapter#getGroupView(kotlin.Int,%20kotlin.Boolean,%20android.view.View,%20android.view.ViewGroup)(groupPosition: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, isExpanded: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html, convertView: https://developer.android.com/reference/kotlin/android/view/View.html#!, parent: https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#!)` Gets a View that displays the given group. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/widget/CursorTreeAdapter#hasStableIds()()` Indicates whether the child and group IDs are stable across changes to the underlying data. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/widget/CursorTreeAdapter#isChildSelectable(kotlin.Int,%20kotlin.Int)(groupPosition: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, childPosition: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Whether the child at the specified position is selectable. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/widget/CursorTreeAdapter#notifyDataSetChanged()()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/widget/CursorTreeAdapter#notifyDataSetChanged(kotlin.Boolean)(releaseCursors: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Notifies a data set change, but with the option of not releasing any cached cursors. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/widget/CursorTreeAdapter#notifyDataSetInvalidated()()` <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/widget/CursorTreeAdapter#onGroupCollapsed(kotlin.Int)(groupPosition: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Called when a group is collapsed. |
| open [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#)! | `https://developer.android.com/reference/kotlin/android/widget/CursorTreeAdapter#runQueryOnBackgroundThread(kotlin.CharSequence)(constraint: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/widget/CursorTreeAdapter#setChildrenCursor(kotlin.Int,%20android.database.Cursor)(groupPosition: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, childrenCursor: https://developer.android.com/reference/kotlin/android/database/Cursor.html#!)` Sets the children Cursor for a particular group. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/widget/CursorTreeAdapter#setFilterQueryProvider(android.widget.FilterQueryProvider)(filterQueryProvider: https://developer.android.com/reference/kotlin/android/widget/FilterQueryProvider!)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/widget/CursorTreeAdapter#setGroupCursor(android.database.Cursor)(cursor: https://developer.android.com/reference/kotlin/android/database/Cursor.html#!)` Sets the group Cursor. |

| Protected methods ||
|---|---|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/widget/CursorTreeAdapter#bindChildView(android.view.View,%20android.content.Context,%20android.database.Cursor,%20kotlin.Boolean)(view: https://developer.android.com/reference/kotlin/android/view/View.html#!, context: https://developer.android.com/reference/kotlin/android/content/Context.html#!, cursor: https://developer.android.com/reference/kotlin/android/database/Cursor.html#!, isLastChild: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Bind an existing view to the child data pointed to by cursor |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/widget/CursorTreeAdapter#bindGroupView(android.view.View,%20android.content.Context,%20android.database.Cursor,%20kotlin.Boolean)(view: https://developer.android.com/reference/kotlin/android/view/View.html#!, context: https://developer.android.com/reference/kotlin/android/content/Context.html#!, cursor: https://developer.android.com/reference/kotlin/android/database/Cursor.html#!, isExpanded: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Bind an existing view to the group data pointed to by cursor. |
| abstract [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#)! | `https://developer.android.com/reference/kotlin/android/widget/CursorTreeAdapter#getChildrenCursor(android.database.Cursor)(groupCursor: https://developer.android.com/reference/kotlin/android/database/Cursor.html#!)` Gets the Cursor for the children at the given group. |
| --- | --- |
| abstract [View](https://developer.android.com/reference/kotlin/android/view/View.html#)! | `https://developer.android.com/reference/kotlin/android/widget/CursorTreeAdapter#newChildView(android.content.Context,%20android.database.Cursor,%20kotlin.Boolean,%20android.view.ViewGroup)(context: https://developer.android.com/reference/kotlin/android/content/Context.html#!, cursor: https://developer.android.com/reference/kotlin/android/database/Cursor.html#!, isLastChild: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html, parent: https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#!)` Makes a new child view to hold the data pointed to by cursor. |
| abstract [View](https://developer.android.com/reference/kotlin/android/view/View.html#)! | `https://developer.android.com/reference/kotlin/android/widget/CursorTreeAdapter#newGroupView(android.content.Context,%20android.database.Cursor,%20kotlin.Boolean,%20android.view.ViewGroup)(context: https://developer.android.com/reference/kotlin/android/content/Context.html#!, cursor: https://developer.android.com/reference/kotlin/android/database/Cursor.html#!, isExpanded: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html, parent: https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#!)` Makes a new group view to hold the group data pointed to by cursor. |

| Inherited functions ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/widget/BaseExpandableListAdapter` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/widget/BaseExpandableListAdapter#areAllItemsEnabled()()` <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/widget/BaseExpandableListAdapter#getChildType(kotlin.Int,%20kotlin.Int)(groupPosition: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, childPosition: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Get the type of child View that will be created by `https://developer.android.com/reference/kotlin/android/widget/ExpandableListAdapter#getChildView(kotlin.Int,%20kotlin.Int,%20kotlin.Boolean,%20android.view.View,%20android.view.ViewGroup)` for the specified child item. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/widget/BaseExpandableListAdapter#getChildTypeCount()()` Returns the number of types of child Views that will be created by `https://developer.android.com/reference/kotlin/android/widget/ExpandableListAdapter#getChildView(kotlin.Int,%20kotlin.Int,%20kotlin.Boolean,%20android.view.View,%20android.view.ViewGroup)` . Each type represents a set of views that can be converted in `https://developer.android.com/reference/kotlin/android/widget/ExpandableListAdapter#getChildView(kotlin.Int,%20kotlin.Int,%20kotlin.Boolean,%20android.view.View,%20android.view.ViewGroup)` , for any group. If the adapter always returns the same type of View for all child items, this method should return 1. This method will only be called when the adapter is set on the `https://developer.android.com/reference/kotlin/android/widget/AdapterView`. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | `https://developer.android.com/reference/kotlin/android/widget/BaseExpandableListAdapter#getCombinedChildId(kotlin.Long,%20kotlin.Long)(groupId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html, childId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Override this method if you foresee a clash in IDs based on this scheme: Base implementation returns a long: - bit 0: Whether this ID points to a child (unset) or group (set), so for this method this bit will be 1. - bit 1-31: Lower 31 bits of the groupId - bit 32-63: Lower 32 bits of the childId. Gets an ID for a child that is unique across any item (either group or child) that is in this list. Expandable lists require each item (group or child) to have a unique ID among all children and groups in the list. This method is responsible for returning that unique ID given a child's ID and its group's ID. Furthermore, if `https://developer.android.com/reference/kotlin/android/widget/ExpandableListAdapter#hasStableIds()` is true, the returned ID must be stable as well. | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | `https://developer.android.com/reference/kotlin/android/widget/BaseExpandableListAdapter#getCombinedGroupId(kotlin.Long)(groupId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Override this method if you foresee a clash in IDs based on this scheme: Base implementation returns a long: - bit 0: Whether this ID points to a child (unset) or group (set), so for this method this bit will be 0. - bit 1-31: Lower 31 bits of the groupId - bit 32-63: Lower 32 bits of the childId. Gets an ID for a group that is unique across any item (either group or child) that is in this list. Expandable lists require each item (group or child) to have a unique ID among all children and groups in the list. This method is responsible for returning that unique ID given a group's ID. Furthermore, if `https://developer.android.com/reference/kotlin/android/widget/ExpandableListAdapter#hasStableIds()` is true, the returned ID must be stable as well. | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/widget/BaseExpandableListAdapter#getGroupType(kotlin.Int)(groupPosition: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Get the type of group View that will be created by `https://developer.android.com/reference/kotlin/android/widget/ExpandableListAdapter#getGroupView(kotlin.Int,%20kotlin.Boolean,%20android.view.View,%20android.view.ViewGroup)` . for the specified group item. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/widget/BaseExpandableListAdapter#getGroupTypeCount()()` Returns the number of types of group Views that will be created by `https://developer.android.com/reference/kotlin/android/widget/ExpandableListAdapter#getGroupView(kotlin.Int,%20kotlin.Boolean,%20android.view.View,%20android.view.ViewGroup)` . Each type represents a set of views that can be converted in `https://developer.android.com/reference/kotlin/android/widget/ExpandableListAdapter#getGroupView(kotlin.Int,%20kotlin.Boolean,%20android.view.View,%20android.view.ViewGroup)` . If the adapter always returns the same type of View for all group items, this method should return 1. This method will only be called when the adapter is set on the `https://developer.android.com/reference/kotlin/android/widget/AdapterView`. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/widget/BaseExpandableListAdapter#isEmpty()()` <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/widget/BaseExpandableListAdapter#onGroupExpanded(kotlin.Int)(groupPosition: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Called when a group is expanded. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/widget/BaseExpandableListAdapter#registerDataSetObserver(android.database.DataSetObserver)(observer: https://developer.android.com/reference/kotlin/android/database/DataSetObserver.html#!)` <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/widget/BaseExpandableListAdapter#unregisterDataSetObserver(android.database.DataSetObserver)(observer: https://developer.android.com/reference/kotlin/android/database/DataSetObserver.html#!)` <br /> | ||
| From class `https://developer.android.com/reference/kotlin/android/widget/ExpandableListAdapter` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!` | `https://developer.android.com/reference/kotlin/android/widget/ExpandableListAdapter#getChild(kotlin.Int,%20kotlin.Int)(groupPosition: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, childPosition: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Gets the data associated with the given child within the given group. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | `https://developer.android.com/reference/kotlin/android/widget/ExpandableListAdapter#getChildId(kotlin.Int,%20kotlin.Int)(groupPosition: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, childPosition: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Gets the ID for the given child within the given group. This ID must be unique across all children within the group. The combined ID (see `https://developer.android.com/reference/kotlin/android/widget/ExpandableListAdapter#getCombinedChildId(kotlin.Long,%20kotlin.Long)`) must be unique across ALL items (groups and all children). <br /> | | `https://developer.android.com/reference/kotlin/android/view/View.html#!` | `https://developer.android.com/reference/kotlin/android/widget/ExpandableListAdapter#getChildView(kotlin.Int,%20kotlin.Int,%20kotlin.Boolean,%20android.view.View,%20android.view.ViewGroup)(groupPosition: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, childPosition: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, isLastChild: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html, convertView: https://developer.android.com/reference/kotlin/android/view/View.html#!, parent: https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#!)` Gets a View that displays the data for the given child within the given group. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/widget/ExpandableListAdapter#getChildrenCount(kotlin.Int)(groupPosition: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Gets the number of children in a specified group. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!` | `https://developer.android.com/reference/kotlin/android/widget/ExpandableListAdapter#getGroup(kotlin.Int)(groupPosition: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Gets the data associated with the given group. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/widget/ExpandableListAdapter#getGroupCount()()` Gets the number of groups. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | `https://developer.android.com/reference/kotlin/android/widget/ExpandableListAdapter#getGroupId(kotlin.Int)(groupPosition: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Gets the ID for the group at the given position. This group ID must be unique across groups. The combined ID (see `https://developer.android.com/reference/kotlin/android/widget/ExpandableListAdapter#getCombinedGroupId(kotlin.Long)`) must be unique across ALL items (groups and all children). <br /> | | `https://developer.android.com/reference/kotlin/android/view/View.html#!` | `https://developer.android.com/reference/kotlin/android/widget/ExpandableListAdapter#getGroupView(kotlin.Int,%20kotlin.Boolean,%20android.view.View,%20android.view.ViewGroup)(groupPosition: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, isExpanded: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html, convertView: https://developer.android.com/reference/kotlin/android/view/View.html#!, parent: https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#!)` Gets a View that displays the given group. This View is only for the group--the Views for the group's children will be fetched using `https://developer.android.com/reference/kotlin/android/widget/ExpandableListAdapter#getChildView(kotlin.Int,%20kotlin.Int,%20kotlin.Boolean,%20android.view.View,%20android.view.ViewGroup)`. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/widget/ExpandableListAdapter#hasStableIds()()` Indicates whether the child and group IDs are stable across changes to the underlying data. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/widget/ExpandableListAdapter#isChildSelectable(kotlin.Int,%20kotlin.Int)(groupPosition: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, childPosition: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Whether the child at the specified position is selectable. <br /> | ||

## Public constructors

### CursorTreeAdapter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
CursorTreeAdapter(
    cursor: Cursor!, 
    context: Context!)
```

Constructor. The adapter will call `https://developer.android.com/reference/kotlin/android/database/Cursor.html#requery()` on the cursor whenever it changes so that the most recent data is always displayed.

| Parameters ||
|---|---|
| `cursor` | [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#)!: The cursor from which to get the data for the groups. |

### CursorTreeAdapter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
CursorTreeAdapter(
    cursor: Cursor!, 
    context: Context!, 
    autoRequery: Boolean)
```

Constructor.

| Parameters ||
|---|---|
| `cursor` | [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#)!: The cursor from which to get the data for the groups. |
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!: The context |
| `autoRequery` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): If true the adapter will call `https://developer.android.com/reference/kotlin/android/database/Cursor.html#requery()` on the cursor whenever it changes so the most recent data is always displayed. |
| --- | --- |

## Public methods

### changeCursor

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun changeCursor(cursor: Cursor!): Unit
```
**See Also**

- `https://developer.android.com/reference/kotlin/android/widget/CursorAdapter#changeCursor(android.database.Cursor)`

### convertToString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun convertToString(cursor: Cursor!): String!
```
**See Also**

- `https://developer.android.com/reference/kotlin/android/widget/CursorAdapter#convertToString(android.database.Cursor)`

### getChild

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getChild(
    groupPosition: Int, 
    childPosition: Int
): Cursor!
```

Gets the data associated with the given child within the given group.

| Parameters ||
|---|---|
| `groupPosition` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the position of the group that the child resides in |
| `childPosition` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the position of the child with respect to other children in the group |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/database/Cursor.html#!` | the data of the child |

### getChildId

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getChildId(
    groupPosition: Int, 
    childPosition: Int
): Long
```

Gets the ID for the given child within the given group. This ID must be unique across all children within the group. The combined ID (see `https://developer.android.com/reference/kotlin/android/widget/ExpandableListAdapter#getCombinedChildId(kotlin.Long,%20kotlin.Long)`) must be unique across ALL items (groups and all children).

| Parameters ||
|---|---|
| `groupPosition` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the position of the group that contains the child |
| `childPosition` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the position of the child within the group for which the ID is wanted |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the ID associated with the child |

### getChildView

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getChildView(
    groupPosition: Int, 
    childPosition: Int, 
    isLastChild: Boolean, 
    convertView: View!, 
    parent: ViewGroup!
): View!
```

Gets a View that displays the data for the given child within the given group.

| Parameters ||
|---|---|
| `groupPosition` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the position of the group that contains the child |
| `childPosition` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the position of the child (for which the View is returned) within the group |
| `isLastChild` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): Whether the child is the last child within the group |
| --- | --- |
| `convertView` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!: the old view to reuse, if possible. You should check that this view is non-null and of an appropriate type before using. If it is not possible to convert this view to display the correct data, this method can create a new view. It is not guaranteed that the convertView will have been previously created by `https://developer.android.com/reference/kotlin/android/widget/ExpandableListAdapter#getChildView(kotlin.Int,%20kotlin.Int,%20kotlin.Boolean,%20android.view.View,%20android.view.ViewGroup)`. |
| `parent` | [ViewGroup](https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#)!: the parent that this view will eventually be attached to |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/View.html#!` | the View corresponding to the child at the specified position |

### getChildrenCount

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getChildrenCount(groupPosition: Int): Int
```

Gets the number of children in a specified group.

| Parameters ||
|---|---|
| `groupPosition` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the position of the group for which the children count should be returned |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the children count in the specified group |

### getCursor

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getCursor(): Cursor!
```
**See Also**

- `https://developer.android.com/reference/kotlin/android/widget/CursorAdapter#getCursor()`

### getFilter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getFilter(): Filter!
```

Returns a filter that can be used to constrain data with a filtering pattern.

This method is usually implemented by `https://developer.android.com/reference/kotlin/android/widget/Adapter` classes.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/widget/Filter!` | a filter used to constrain data |

### getFilterQueryProvider

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getFilterQueryProvider(): FilterQueryProvider!
```
**See Also**

- `https://developer.android.com/reference/kotlin/android/widget/CursorAdapter#getFilterQueryProvider()`

### getGroup

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getGroup(groupPosition: Int): Cursor!
```

Gets the data associated with the given group.

| Parameters ||
|---|---|
| `groupPosition` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the position of the group |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/database/Cursor.html#!` | the data child for the specified group |

### getGroupCount

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getGroupCount(): Int
```

Gets the number of groups.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the number of groups |

### getGroupId

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getGroupId(groupPosition: Int): Long
```

Gets the ID for the group at the given position. This group ID must be unique across groups. The combined ID (see `https://developer.android.com/reference/kotlin/android/widget/ExpandableListAdapter#getCombinedGroupId(kotlin.Long)`) must be unique across ALL items (groups and all children).

| Parameters ||
|---|---|
| `groupPosition` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the position of the group for which the ID is wanted |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the ID associated with the group |

### getGroupView

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getGroupView(
    groupPosition: Int, 
    isExpanded: Boolean, 
    convertView: View!, 
    parent: ViewGroup!
): View!
```

Gets a View that displays the given group. This View is only for the group--the Views for the group's children will be fetched using `https://developer.android.com/reference/kotlin/android/widget/ExpandableListAdapter#getChildView(kotlin.Int,%20kotlin.Int,%20kotlin.Boolean,%20android.view.View,%20android.view.ViewGroup)`.

| Parameters ||
|---|---|
| `groupPosition` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the position of the group for which the View is returned |
| `isExpanded` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): whether the group is expanded or collapsed |
| `convertView` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!: the old view to reuse, if possible. You should check that this view is non-null and of an appropriate type before using. If it is not possible to convert this view to display the correct data, this method can create a new view. It is not guaranteed that the convertView will have been previously created by `https://developer.android.com/reference/kotlin/android/widget/ExpandableListAdapter#getGroupView(kotlin.Int,%20kotlin.Boolean,%20android.view.View,%20android.view.ViewGroup)`. |
| --- | --- |
| `parent` | [ViewGroup](https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#)!: the parent that this view will eventually be attached to |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/View.html#!` | the View corresponding to the group at the specified position |

### hasStableIds

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun hasStableIds(): Boolean
```

Indicates whether the child and group IDs are stable across changes to the underlying data.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | whether or not the same ID always refers to the same object |

### isChildSelectable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isChildSelectable(
    groupPosition: Int, 
    childPosition: Int
): Boolean
```

Whether the child at the specified position is selectable.

| Parameters ||
|---|---|
| `groupPosition` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the position of the group that contains the child |
| `childPosition` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the position of the child within the group |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | whether the child is selectable. |

### notifyDataSetChanged

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun notifyDataSetChanged(): Unit
```

### notifyDataSetChanged

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun notifyDataSetChanged(releaseCursors: Boolean): Unit
```

Notifies a data set change, but with the option of not releasing any cached cursors.

| Parameters ||
|---|---|
| `releaseCursors` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): Whether to release and deactivate any cached cursors. |

### notifyDataSetInvalidated

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun notifyDataSetInvalidated(): Unit
```

### onGroupCollapsed

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onGroupCollapsed(groupPosition: Int): Unit
```

Called when a group is collapsed.

| Parameters ||
|---|---|
| `groupPosition` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The group being collapsed. |

### runQueryOnBackgroundThread

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun runQueryOnBackgroundThread(constraint: CharSequence!): Cursor!
```
**See Also**

- `https://developer.android.com/reference/kotlin/android/widget/CursorAdapter#runQueryOnBackgroundThread(kotlin.CharSequence)`

### setChildrenCursor

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setChildrenCursor(
    groupPosition: Int, 
    childrenCursor: Cursor!
): Unit
```

Sets the children Cursor for a particular group. If there is an existing cursor it will be closed.

This is useful when asynchronously querying to prevent blocking the UI.

| Parameters ||
|---|---|
| `groupPosition` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The group whose children are being set via this Cursor. |
| `childrenCursor` | [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#)!: The Cursor that contains the children of the group. |

### setFilterQueryProvider

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setFilterQueryProvider(filterQueryProvider: FilterQueryProvider!): Unit
```
**See Also**

- `https://developer.android.com/reference/kotlin/android/widget/CursorAdapter#setFilterQueryProvider(android.widget.FilterQueryProvider)`

### setGroupCursor

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setGroupCursor(cursor: Cursor!): Unit
```

Sets the group Cursor.

| Parameters ||
|---|---|
| `cursor` | [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#)!: The Cursor to set for the group. If there is an existing cursor it will be closed. |

## Protected methods

### bindChildView

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected abstract fun bindChildView(
    view: View!, 
    context: Context!, 
    cursor: Cursor!, 
    isLastChild: Boolean
): Unit
```

Bind an existing view to the child data pointed to by cursor

| Parameters ||
|---|---|
| `view` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!: Existing view, returned earlier by newChildView |
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!: Interface to application's global information |
| `cursor` | [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#)!: The cursor from which to get the data. The cursor is already moved to the correct position. |
| --- | --- |
| `isLastChild` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): Whether the child is the last child within its group. |

### bindGroupView

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected abstract fun bindGroupView(
    view: View!, 
    context: Context!, 
    cursor: Cursor!, 
    isExpanded: Boolean
): Unit
```

Bind an existing view to the group data pointed to by cursor.

| Parameters ||
|---|---|
| `view` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!: Existing view, returned earlier by newGroupView. |
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!: Interface to application's global information |
| `cursor` | [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#)!: The cursor from which to get the data. The cursor is already moved to the correct position. |
| --- | --- |
| `isExpanded` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): Whether the group is expanded. |

### getChildrenCursor

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected abstract fun getChildrenCursor(groupCursor: Cursor!): Cursor!
```

Gets the Cursor for the children at the given group. Subclasses must implement this method to return the children data for a particular group.

If you want to asynchronously query a provider to prevent blocking the UI, it is possible to return null and at a later time call `https://developer.android.com/reference/kotlin/android/widget/CursorTreeAdapter#setChildrenCursor(kotlin.Int,%20android.database.Cursor)`.

It is your responsibility to manage this Cursor through the Activity lifecycle. It is a good idea to use `https://developer.android.com/reference/kotlin/android/app/Activity.html#managedQuery(android.net.Uri,%20kotlin.Array,%20kotlin.String,%20kotlin.Array,%20kotlin.String)` which will handle this for you. In some situations, the adapter will deactivate the Cursor on its own, but this will not always be the case, so please ensure the Cursor is properly managed.

| Parameters ||
|---|---|
| `groupCursor` | [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#)!: The cursor pointing to the group whose children cursor should be returned |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/database/Cursor.html#!` | The cursor for the children of a particular group, or null. |

### newChildView

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected abstract fun newChildView(
    context: Context!, 
    cursor: Cursor!, 
    isLastChild: Boolean, 
    parent: ViewGroup!
): View!
```

Makes a new child view to hold the data pointed to by cursor.

| Parameters ||
|---|---|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!: Interface to application's global information |
| `cursor` | [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#)!: The cursor from which to get the data. The cursor is already moved to the correct position. |
| `isLastChild` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): Whether the child is the last child within its group. |
| --- | --- |
| `parent` | [ViewGroup](https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#)!: The parent to which the new view is attached to |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/View.html#!` | the newly created view. |

### newGroupView

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected abstract fun newGroupView(
    context: Context!, 
    cursor: Cursor!, 
    isExpanded: Boolean, 
    parent: ViewGroup!
): View!
```

Makes a new group view to hold the group data pointed to by cursor.

| Parameters ||
|---|---|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!: Interface to application's global information |
| `cursor` | [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#)!: The group cursor from which to get the data. The cursor is already moved to the correct position. |
| `isExpanded` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): Whether the group is expanded. |
| --- | --- |
| `parent` | [ViewGroup](https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#)!: The parent to which the new view is attached to |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/View.html#!` | The newly created view. |
