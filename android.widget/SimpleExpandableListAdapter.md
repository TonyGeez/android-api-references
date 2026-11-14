# SimpleExpandableListAdapter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SimpleExpandableListAdapter

Kotlin| [Java](https://developer.android.com/reference/android/widget/SimpleExpandableListAdapter "View this page in Java") 
| --- | --- |

```
open class SimpleExpandableListAdapter : BaseExpandableListAdapter
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.widget.BaseExpandableListAdapter](https://developer.android.com/reference/kotlin/android/widget/BaseExpandableListAdapter) ||
| | ↳ | [android.widget.SimpleExpandableListAdapter](https://developer.android.com/reference/kotlin/android/widget/SimpleExpandableListAdapter#) |

An easy adapter to map static data to group and child views defined in an XML file. You can separately specify the data backing the group as a List of Maps. Each entry in the ArrayList corresponds to one group in the expandable list. The Maps contain the data for each row. You also specify an XML file that defines the views used to display a group, and a mapping from keys in the Map to specific views. This process is similar for a child, except it is one-level deeper so the data backing is specified as a List\>, where the first List corresponds to the group of the child, the second List corresponds to the position of the child within the group, and finally the Map holds the data for that particular child.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SimpleExpandableListAdapter](https://developer.android.com/reference/kotlin/android/widget/SimpleExpandableListAdapter#SimpleExpandableListAdapter(android.content.Context,%20kotlin.collections.MutableList,%20kotlin.Int,%20kotlin.Int,%20kotlin.Array,%20kotlin.IntArray,%20kotlin.collections.MutableList,%20kotlin.Int,%20kotlin.Int,%20kotlin.Array,%20kotlin.IntArray))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`, `groupData:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)<out` ` [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!,` `*>!>!`, `expandedGroupLayout:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `collapsedGroupLayout:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `groupFrom:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`, `groupTo:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!`, `childData:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)<out` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)<out` ` [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!,` `*>!>!>!`, `childLayout:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `lastChildLayout:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `childFrom:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`, `childTo:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!`)` Constructor |
| [SimpleExpandableListAdapter](https://developer.android.com/reference/kotlin/android/widget/SimpleExpandableListAdapter#SimpleExpandableListAdapter(android.content.Context,%20kotlin.collections.MutableList,%20kotlin.Int,%20kotlin.Int,%20kotlin.Array,%20kotlin.IntArray,%20kotlin.collections.MutableList,%20kotlin.Int,%20kotlin.Array,%20kotlin.IntArray))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`, `groupData:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)<out` ` [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!,` `*>!>!`, `expandedGroupLayout:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `collapsedGroupLayout:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `groupFrom:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`, `groupTo:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!`, `childData:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)<out` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)<out` ` [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!,` `*>!>!>!`, `childLayout:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `childFrom:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`, `childTo:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!`)` Constructor |
| [SimpleExpandableListAdapter](https://developer.android.com/reference/kotlin/android/widget/SimpleExpandableListAdapter#SimpleExpandableListAdapter(android.content.Context,%20kotlin.collections.MutableList,%20kotlin.Int,%20kotlin.Array,%20kotlin.IntArray,%20kotlin.collections.MutableList,%20kotlin.Int,%20kotlin.Array,%20kotlin.IntArray))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`, `groupData:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)<out` ` [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!,` `*>!>!`, `groupLayout:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `groupFrom:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`, `groupTo:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!`, `childData:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)<out` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)<out` ` [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!,` `*>!>!>!`, `childLayout:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `childFrom:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`, `childTo:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!`)` Constructor |

| Public methods ||
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getChild](https://developer.android.com/reference/kotlin/android/widget/SimpleExpandableListAdapter#getChild(kotlin.Int,%20kotlin.Int))`(`groupPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `childPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getChildId](https://developer.android.com/reference/kotlin/android/widget/SimpleExpandableListAdapter#getChildId(kotlin.Int,%20kotlin.Int))`(`groupPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `childPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [View](https://developer.android.com/reference/kotlin/android/view/View.html#)! | [getChildView](https://developer.android.com/reference/kotlin/android/widget/SimpleExpandableListAdapter#getChildView(kotlin.Int,%20kotlin.Int,%20kotlin.Boolean,%20android.view.View,%20android.view.ViewGroup))`(`groupPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `childPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `isLastChild:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `convertView:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!`, `parent:` ` [ViewGroup](https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#)!`)` <br /> |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getChildrenCount](https://developer.android.com/reference/kotlin/android/widget/SimpleExpandableListAdapter#getChildrenCount(kotlin.Int))`(`groupPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getGroup](https://developer.android.com/reference/kotlin/android/widget/SimpleExpandableListAdapter#getGroup(kotlin.Int))`(`groupPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getGroupCount](https://developer.android.com/reference/kotlin/android/widget/SimpleExpandableListAdapter#getGroupCount())`()` <br /> |
| --- | --- |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getGroupId](https://developer.android.com/reference/kotlin/android/widget/SimpleExpandableListAdapter#getGroupId(kotlin.Int))`(`groupPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [View](https://developer.android.com/reference/kotlin/android/view/View.html#)! | [getGroupView](https://developer.android.com/reference/kotlin/android/widget/SimpleExpandableListAdapter#getGroupView(kotlin.Int,%20kotlin.Boolean,%20android.view.View,%20android.view.ViewGroup))`(`groupPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `isExpanded:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `convertView:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!`, `parent:` ` [ViewGroup](https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#)!`)` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasStableIds](https://developer.android.com/reference/kotlin/android/widget/SimpleExpandableListAdapter#hasStableIds())`()` <br /> |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isChildSelectable](https://developer.android.com/reference/kotlin/android/widget/SimpleExpandableListAdapter#isChildSelectable(kotlin.Int,%20kotlin.Int))`(`groupPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `childPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [View](https://developer.android.com/reference/kotlin/android/view/View.html#)! | [newChildView](https://developer.android.com/reference/kotlin/android/widget/SimpleExpandableListAdapter#newChildView(kotlin.Boolean,%20android.view.ViewGroup))`(`isLastChild:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `parent:` ` [ViewGroup](https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#)!`)` Instantiates a new View for a child. |
| open [View](https://developer.android.com/reference/kotlin/android/view/View.html#)! | [newGroupView](https://developer.android.com/reference/kotlin/android/widget/SimpleExpandableListAdapter#newGroupView(kotlin.Boolean,%20android.view.ViewGroup))`(`isExpanded:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `parent:` ` [ViewGroup](https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#)!`)` Instantiates a new View for a group. |
| --- | --- |

| Inherited functions ||
|---|---|
| From class [BaseExpandableListAdapter](https://developer.android.com/reference/kotlin/android/widget/BaseExpandableListAdapter) |------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [areAllItemsEnabled](https://developer.android.com/reference/kotlin/android/widget/BaseExpandableListAdapter#areAllItemsEnabled())`()` <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getChildType](https://developer.android.com/reference/kotlin/android/widget/BaseExpandableListAdapter#getChildType(kotlin.Int,%20kotlin.Int))`(`groupPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `childPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Get the type of child View that will be created by [android.widget.ExpandableListAdapter#getChildView(int, int, boolean, View, ViewGroup)](https://developer.android.com/reference/kotlin/android/widget/ExpandableListAdapter#getChildView(kotlin.Int,%20kotlin.Int,%20kotlin.Boolean,%20android.view.View,%20android.view.ViewGroup))for the specified child item. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getChildTypeCount](https://developer.android.com/reference/kotlin/android/widget/BaseExpandableListAdapter#getChildTypeCount())`()` <br /> Returns the number of types of child Views that will be created by [android.widget.ExpandableListAdapter#getChildView(int, int, boolean, View, ViewGroup)](https://developer.android.com/reference/kotlin/android/widget/ExpandableListAdapter#getChildView(kotlin.Int,%20kotlin.Int,%20kotlin.Boolean,%20android.view.View,%20android.view.ViewGroup)). Each type represents a set of views that can be converted in [android.widget.ExpandableListAdapter#getChildView(int, int, boolean, View, ViewGroup)](https://developer.android.com/reference/kotlin/android/widget/ExpandableListAdapter#getChildView(kotlin.Int,%20kotlin.Int,%20kotlin.Boolean,%20android.view.View,%20android.view.ViewGroup)), for any group. If the adapter always returns the same type of View for all child items, this method should return 1. This method will only be called when the adapter is set on the [AdapterView](https://developer.android.com/reference/kotlin/android/widget/AdapterView). <br /> | | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getCombinedChildId](https://developer.android.com/reference/kotlin/android/widget/BaseExpandableListAdapter#getCombinedChildId(kotlin.Long,%20kotlin.Long))`(`groupId:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `childId:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` <br /> Override this method if you foresee a clash in IDs based on this scheme: Base implementation returns a long: - bit 0: Whether this ID points to a child (unset) or group (set), so for this method this bit will be 1. - bit 1-31: Lower 31 bits of the groupId - bit 32-63: Lower 32 bits of the childId.Gets an ID for a child that is unique across any item (either group or child) that is in this list. Expandable lists require each item (group or child) to have a unique ID among all children and groups in the list. This method is responsible for returning that unique ID given a child's ID and its group's ID. Furthermore, if [hasStableIds()](https://developer.android.com/reference/kotlin/android/widget/ExpandableListAdapter#hasStableIds())is true, the returned ID must be stable as well. | | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getCombinedGroupId](https://developer.android.com/reference/kotlin/android/widget/BaseExpandableListAdapter#getCombinedGroupId(kotlin.Long))`(`groupId:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` <br /> Override this method if you foresee a clash in IDs based on this scheme: Base implementation returns a long: - bit 0: Whether this ID points to a child (unset) or group (set), so for this method this bit will be 0. - bit 1-31: Lower 31 bits of the groupId - bit 32-63: Lower 32 bits of the childId.Gets an ID for a group that is unique across any item (either group or child) that is in this list. Expandable lists require each item (group or child) to have a unique ID among all children and groups in the list. This method is responsible for returning that unique ID given a group's ID. Furthermore, if [hasStableIds()](https://developer.android.com/reference/kotlin/android/widget/ExpandableListAdapter#hasStableIds())is true, the returned ID must be stable as well. | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getGroupType](https://developer.android.com/reference/kotlin/android/widget/BaseExpandableListAdapter#getGroupType(kotlin.Int))`(`groupPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Get the type of group View that will be created by [android.widget.ExpandableListAdapter#getGroupView(int, boolean, View, ViewGroup)](https://developer.android.com/reference/kotlin/android/widget/ExpandableListAdapter#getGroupView(kotlin.Int,%20kotlin.Boolean,%20android.view.View,%20android.view.ViewGroup)). for the specified group item. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getGroupTypeCount](https://developer.android.com/reference/kotlin/android/widget/BaseExpandableListAdapter#getGroupTypeCount())`()` <br /> Returns the number of types of group Views that will be created by [android.widget.ExpandableListAdapter#getGroupView(int, boolean, View, ViewGroup)](https://developer.android.com/reference/kotlin/android/widget/ExpandableListAdapter#getGroupView(kotlin.Int,%20kotlin.Boolean,%20android.view.View,%20android.view.ViewGroup)). Each type represents a set of views that can be converted in [android.widget.ExpandableListAdapter#getGroupView(int, boolean, View, ViewGroup)](https://developer.android.com/reference/kotlin/android/widget/ExpandableListAdapter#getGroupView(kotlin.Int,%20kotlin.Boolean,%20android.view.View,%20android.view.ViewGroup)). If the adapter always returns the same type of View for all group items, this method should return 1. This method will only be called when the adapter is set on the [AdapterView](https://developer.android.com/reference/kotlin/android/widget/AdapterView). <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEmpty](https://developer.android.com/reference/kotlin/android/widget/BaseExpandableListAdapter#isEmpty())`()` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [notifyDataSetChanged](https://developer.android.com/reference/kotlin/android/widget/BaseExpandableListAdapter#notifyDataSetChanged())`()` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [notifyDataSetInvalidated](https://developer.android.com/reference/kotlin/android/widget/BaseExpandableListAdapter#notifyDataSetInvalidated())`()` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onGroupCollapsed](https://developer.android.com/reference/kotlin/android/widget/BaseExpandableListAdapter#onGroupCollapsed(kotlin.Int))`(`groupPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onGroupExpanded](https://developer.android.com/reference/kotlin/android/widget/BaseExpandableListAdapter#onGroupExpanded(kotlin.Int))`(`groupPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerDataSetObserver](https://developer.android.com/reference/kotlin/android/widget/BaseExpandableListAdapter#registerDataSetObserver(android.database.DataSetObserver))`(`observer:` ` [DataSetObserver](https://developer.android.com/reference/kotlin/android/database/DataSetObserver.html#)!`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unregisterDataSetObserver](https://developer.android.com/reference/kotlin/android/widget/BaseExpandableListAdapter#unregisterDataSetObserver(android.database.DataSetObserver))`(`observer:` ` [DataSetObserver](https://developer.android.com/reference/kotlin/android/database/DataSetObserver.html#)!`)` <br /> | ||
| From class [ExpandableListAdapter](https://developer.android.com/reference/kotlin/android/widget/ExpandableListAdapter) |------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getChild](https://developer.android.com/reference/kotlin/android/widget/ExpandableListAdapter#getChild(kotlin.Int,%20kotlin.Int))`(`groupPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `childPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Gets the data associated with the given child within the given group. <br /> | | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getChildId](https://developer.android.com/reference/kotlin/android/widget/ExpandableListAdapter#getChildId(kotlin.Int,%20kotlin.Int))`(`groupPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `childPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Gets the ID for the given child within the given group. This ID must be unique across all children within the group. The combined ID (see [getCombinedChildId(long,long)](https://developer.android.com/reference/kotlin/android/widget/ExpandableListAdapter#getCombinedChildId(kotlin.Long,%20kotlin.Long))) must be unique across ALL items (groups and all children). <br /> | | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)! | [getChildView](https://developer.android.com/reference/kotlin/android/widget/ExpandableListAdapter#getChildView(kotlin.Int,%20kotlin.Int,%20kotlin.Boolean,%20android.view.View,%20android.view.ViewGroup))`(`groupPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `childPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `isLastChild:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `convertView:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!`, `parent:` ` [ViewGroup](https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#)!`)` <br /> Gets a View that displays the data for the given child within the given group. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getChildrenCount](https://developer.android.com/reference/kotlin/android/widget/ExpandableListAdapter#getChildrenCount(kotlin.Int))`(`groupPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Gets the number of children in a specified group. <br /> | | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getGroup](https://developer.android.com/reference/kotlin/android/widget/ExpandableListAdapter#getGroup(kotlin.Int))`(`groupPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Gets the data associated with the given group. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getGroupCount](https://developer.android.com/reference/kotlin/android/widget/ExpandableListAdapter#getGroupCount())`()` <br /> Gets the number of groups. <br /> | | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getGroupId](https://developer.android.com/reference/kotlin/android/widget/ExpandableListAdapter#getGroupId(kotlin.Int))`(`groupPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Gets the ID for the group at the given position. This group ID must be unique across groups. The combined ID (see [getCombinedGroupId(long)](https://developer.android.com/reference/kotlin/android/widget/ExpandableListAdapter#getCombinedGroupId(kotlin.Long))) must be unique across ALL items (groups and all children). <br /> | | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)! | [getGroupView](https://developer.android.com/reference/kotlin/android/widget/ExpandableListAdapter#getGroupView(kotlin.Int,%20kotlin.Boolean,%20android.view.View,%20android.view.ViewGroup))`(`groupPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `isExpanded:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `convertView:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!`, `parent:` ` [ViewGroup](https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#)!`)` <br /> Gets a View that displays the given group. This View is only for the group--the Views for the group's children will be fetched using [getChildView(int,int,boolean,android.view.View,android.view.ViewGroup)](https://developer.android.com/reference/kotlin/android/widget/ExpandableListAdapter#getChildView(kotlin.Int,%20kotlin.Int,%20kotlin.Boolean,%20android.view.View,%20android.view.ViewGroup)). <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasStableIds](https://developer.android.com/reference/kotlin/android/widget/ExpandableListAdapter#hasStableIds())`()` <br /> Indicates whether the child and group IDs are stable across changes to the underlying data. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isChildSelectable](https://developer.android.com/reference/kotlin/android/widget/ExpandableListAdapter#isChildSelectable(kotlin.Int,%20kotlin.Int))`(`groupPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `childPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Whether the child at the specified position is selectable. <br /> | ||

## Public constructors

### SimpleExpandableListAdapter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SimpleExpandableListAdapter(
    context: Context!, 
    groupData: MutableList<out MutableMap<String!, *>!>!, 
    expandedGroupLayout: Int, 
    collapsedGroupLayout: Int, 
    groupFrom: Array<String!>!, 
    groupTo: IntArray!, 
    childData: MutableList<out MutableList<out MutableMap<String!, *>!>!>!, 
    childLayout: Int, 
    lastChildLayout: Int, 
    childFrom: Array<String!>!, 
    childTo: IntArray!)
```

Constructor

| Parameters ||
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!:The context where the [ExpandableListView](https://developer.android.com/reference/kotlin/android/widget/ExpandableListView) associated with this [SimpleExpandableListAdapter](https://developer.android.com/reference/kotlin/android/widget/SimpleExpandableListAdapter#) is running |
| `groupData` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\<out [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!,\*\>!\>!:A List of Maps. Each entry in the List corresponds to one group in the list. The Maps contain the data for each group, and should include all the entries specified in "groupFrom" |
| `groupFrom` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!:A list of keys that will be fetched from the Map associated with each group. |
| --- | --- |
| `groupTo` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!:The group views that should display column in the "groupFrom" parameter. These should all be TextViews. The first N views in this list are given the values of the first N columns in the groupFrom parameter. |
| `expandedGroupLayout` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):resource identifier of a view layout that defines the views for an expanded group. The layout file should include at least those named views defined in "groupTo" |
| `collapsedGroupLayout` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):resource identifier of a view layout that defines the views for a collapsed group. The layout file should include at least those named views defined in "groupTo" |
| --- | --- |
| `childData` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\<out [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\<out [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!,\*\>!\>!\>!:A List of List of Maps. Each entry in the outer List corresponds to a group (index by group position), each entry in the inner List corresponds to a child within the group (index by child position), and the Map corresponds to the data for a child (index by values in the childFrom array). The Map contains the data for each child, and should include all the entries specified in "childFrom" |
| `childFrom` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!:A list of keys that will be fetched from the Map associated with each child. |
| `childTo` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!:The child views that should display column in the "childFrom" parameter. These should all be TextViews. The first N views in this list are given the values of the first N columns in the childFrom parameter. |
| --- | --- |
| `childLayout` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):resource identifier of a view layout that defines the views for a child (unless it is the last child within a group, in which case the lastChildLayout is used). The layout file should include at least those named views defined in "childTo" |
| `lastChildLayout` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):resource identifier of a view layout that defines the views for the last child within each group. The layout file should include at least those named views defined in "childTo" |

### SimpleExpandableListAdapter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SimpleExpandableListAdapter(
    context: Context!, 
    groupData: MutableList<out MutableMap<String!, *>!>!, 
    expandedGroupLayout: Int, 
    collapsedGroupLayout: Int, 
    groupFrom: Array<String!>!, 
    groupTo: IntArray!, 
    childData: MutableList<out MutableList<out MutableMap<String!, *>!>!>!, 
    childLayout: Int, 
    childFrom: Array<String!>!, 
    childTo: IntArray!)
```

Constructor

| Parameters ||
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!:The context where the [ExpandableListView](https://developer.android.com/reference/kotlin/android/widget/ExpandableListView) associated with this [SimpleExpandableListAdapter](https://developer.android.com/reference/kotlin/android/widget/SimpleExpandableListAdapter#) is running |
| `groupData` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\<out [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!,\*\>!\>!:A List of Maps. Each entry in the List corresponds to one group in the list. The Maps contain the data for each group, and should include all the entries specified in "groupFrom" |
| `groupFrom` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!:A list of keys that will be fetched from the Map associated with each group. |
| --- | --- |
| `groupTo` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!:The group views that should display column in the "groupFrom" parameter. These should all be TextViews. The first N views in this list are given the values of the first N columns in the groupFrom parameter. |
| `expandedGroupLayout` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):resource identifier of a view layout that defines the views for an expanded group. The layout file should include at least those named views defined in "groupTo" |
| `collapsedGroupLayout` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):resource identifier of a view layout that defines the views for a collapsed group. The layout file should include at least those named views defined in "groupTo" |
| --- | --- |
| `childData` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\<out [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\<out [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!,\*\>!\>!\>!:A List of List of Maps. Each entry in the outer List corresponds to a group (index by group position), each entry in the inner List corresponds to a child within the group (index by child position), and the Map corresponds to the data for a child (index by values in the childFrom array). The Map contains the data for each child, and should include all the entries specified in "childFrom" |
| `childFrom` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!:A list of keys that will be fetched from the Map associated with each child. |
| `childTo` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!:The child views that should display column in the "childFrom" parameter. These should all be TextViews. The first N views in this list are given the values of the first N columns in the childFrom parameter. |
| --- | --- |
| `childLayout` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):resource identifier of a view layout that defines the views for a child. The layout file should include at least those named views defined in "childTo" |

### SimpleExpandableListAdapter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SimpleExpandableListAdapter(
    context: Context!, 
    groupData: MutableList<out MutableMap<String!, *>!>!, 
    groupLayout: Int, 
    groupFrom: Array<String!>!, 
    groupTo: IntArray!, 
    childData: MutableList<out MutableList<out MutableMap<String!, *>!>!>!, 
    childLayout: Int, 
    childFrom: Array<String!>!, 
    childTo: IntArray!)
```

Constructor

| Parameters ||
|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!:The context where the [ExpandableListView](https://developer.android.com/reference/kotlin/android/widget/ExpandableListView) associated with this [SimpleExpandableListAdapter](https://developer.android.com/reference/kotlin/android/widget/SimpleExpandableListAdapter#) is running |
| `groupData` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\<out [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!,\*\>!\>!:A List of Maps. Each entry in the List corresponds to one group in the list. The Maps contain the data for each group, and should include all the entries specified in "groupFrom" |
| `groupFrom` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!:A list of keys that will be fetched from the Map associated with each group. |
| --- | --- |
| `groupTo` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!:The group views that should display column in the "groupFrom" parameter. These should all be TextViews. The first N views in this list are given the values of the first N columns in the groupFrom parameter. |
| `groupLayout` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):resource identifier of a view layout that defines the views for a group. The layout file should include at least those named views defined in "groupTo" |
| `childData` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\<out [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\<out [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!,\*\>!\>!\>!:A List of List of Maps. Each entry in the outer List corresponds to a group (index by group position), each entry in the inner List corresponds to a child within the group (index by child position), and the Map corresponds to the data for a child (index by values in the childFrom array). The Map contains the data for each child, and should include all the entries specified in "childFrom" |
| --- | --- |
| `childFrom` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!:A list of keys that will be fetched from the Map associated with each child. |
| `childTo` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!:The child views that should display column in the "childFrom" parameter. These should all be TextViews. The first N views in this list are given the values of the first N columns in the childFrom parameter. |
| `childLayout` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):resource identifier of a view layout that defines the views for a child. The layout file should include at least those named views defined in "childTo" |
| --- | --- |

## Public methods

### getChild

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getChild(
    groupPosition: Int, 
    childPosition: Int
): Any!
```

| Parameters ||
|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| `groupPosition` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the position of the group that the child resides in |
| `childPosition` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the position of the child with respect to other children in the group |

| Return ||
|-----------------------------------------------------------------------------|-----------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | the data of the child |

### getChildId

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getChildId(
    groupPosition: Int, 
    childPosition: Int
): Long
```

| Parameters ||
|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| `groupPosition` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the position of the group that contains the child |
| `childPosition` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the position of the child within the group for which the ID is wanted |

| Return ||
|------------------------------------------------------------------------------|----------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the ID associated with the child |

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

| Parameters ||
|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `groupPosition` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the position of the group that contains the child |
| `childPosition` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the position of the child (for which the View is returned) within the group |
| `isLastChild` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):Whether the child is the last child within the group |
| --- | --- |
| `convertView` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!:the old view to reuse, if possible. You should check that this view is non-null and of an appropriate type before using. If it is not possible to convert this view to display the correct data, this method can create a new view. It is not guaranteed that the convertView will have been previously created by [getChildView(int,int,boolean,android.view.View,android.view.ViewGroup)](https://developer.android.com/reference/kotlin/android/widget/ExpandableListAdapter#getChildView(kotlin.Int,%20kotlin.Int,%20kotlin.Boolean,%20android.view.View,%20android.view.ViewGroup)). |
| `parent` | [ViewGroup](https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#)!:the parent that this view will eventually be attached to |

| Return ||
|---------------------------------------------------------------------------------|---------------------------------------------------------------|
| [View](https://developer.android.com/reference/kotlin/android/view/View.html#)! | the View corresponding to the child at the specified position |

### getChildrenCount

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getChildrenCount(groupPosition: Int): Int
```

| Parameters ||
|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `groupPosition` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the position of the group for which the children count should be returned |

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the children count in the specified group |

### getGroup

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getGroup(groupPosition: Int): Any!
```

| Parameters ||
|-----------------|------------------------------------------------------------------------------------------------------|
| `groupPosition` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the position of the group |

| Return ||
|-----------------------------------------------------------------------------|----------------------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | the data child for the specified group |

### getGroupCount

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getGroupCount(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of groups |

### getGroupId

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getGroupId(groupPosition: Int): Long
```

| Parameters ||
|-----------------|---------------------------------------------------------------------------------------------------------------------------------|
| `groupPosition` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the position of the group for which the ID is wanted |

| Return ||
|------------------------------------------------------------------------------|----------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the ID associated with the group |

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

| Parameters ||
|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `groupPosition` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the position of the group for which the View is returned |
| `isExpanded` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):whether the group is expanded or collapsed |
| `convertView` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!:the old view to reuse, if possible. You should check that this view is non-null and of an appropriate type before using. If it is not possible to convert this view to display the correct data, this method can create a new view. It is not guaranteed that the convertView will have been previously created by [getGroupView(int,boolean,android.view.View,android.view.ViewGroup)](https://developer.android.com/reference/kotlin/android/widget/ExpandableListAdapter#getGroupView(kotlin.Int,%20kotlin.Boolean,%20android.view.View,%20android.view.ViewGroup)). |
| --- | --- |
| `parent` | [ViewGroup](https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#)!:the parent that this view will eventually be attached to |

| Return ||
|---------------------------------------------------------------------------------|---------------------------------------------------------------|
| [View](https://developer.android.com/reference/kotlin/android/view/View.html#)! | the View corresponding to the group at the specified position |

### hasStableIds

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hasStableIds(): Boolean
```

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | whether or not the same ID always refers to the same object |

### isChildSelectable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isChildSelectable(
    groupPosition: Int, 
    childPosition: Int
): Boolean
```

| Parameters ||
|-----------------|------------------------------------------------------------------------------------------------------------------------------|
| `groupPosition` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the position of the group that contains the child |
| `childPosition` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the position of the child within the group |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | whether the child is selectable. |

### newChildView

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun newChildView(
    isLastChild: Boolean, 
    parent: ViewGroup!
): View!
```

Instantiates a new View for a child.

| Parameters ||
|---------------|------------------------------------------------------------------------------------------------------------------------------------------|
| `isLastChild` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):Whether the child is the last child within its group. |
| `parent` | [ViewGroup](https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#)!:The eventual parent of this new View. |

| Return ||
|---------------------------------------------------------------------------------|------------------|
| [View](https://developer.android.com/reference/kotlin/android/view/View.html#)! | A new child View |

### newGroupView

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun newGroupView(
    isExpanded: Boolean, 
    parent: ViewGroup!
): View!
```

Instantiates a new View for a group.

| Parameters ||
|--------------|---------------------------------------------------------------------------------------------------------------------------------|
| `isExpanded` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):Whether the group is currently expanded. |
| `parent` | [ViewGroup](https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#)!:The eventual parent of this new View. |

| Return ||
|---------------------------------------------------------------------------------|------------------|
| [View](https://developer.android.com/reference/kotlin/android/view/View.html#)! | A new group View |
