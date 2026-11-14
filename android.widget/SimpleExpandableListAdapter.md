# SimpleExpandableListAdapter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SimpleExpandableListAdapter

Kotlin| [Java](../android/widget/SimpleExpandableListAdapter.md) 
| --- | --- |

```
open class SimpleExpandableListAdapter : BaseExpandableListAdapter
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.widget.BaseExpandableListAdapter](../android/widget/BaseExpandableListAdapter.md) ||
| | ↳ | [android.widget.SimpleExpandableListAdapter](../android/widget/SimpleExpandableListAdapter.md) |

An easy adapter to map static data to group and child views defined in an XML file. You can separately specify the data backing the group as a List of Maps. Each entry in the ArrayList corresponds to one group in the expandable list. The Maps contain the data for each row. You also specify an XML file that defines the views used to display a group, and a mapping from keys in the Map to specific views. This process is similar for a child, except it is one-level deeper so the data backing is specified as a List\>, where the first List corresponds to the group of the child, the second List corresponds to the position of the child within the group, and finally the Map holds the data for that particular child.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SimpleExpandableListAdapter](../android/widget/SimpleExpandableListAdapter.md))`(`context:` ` [Context](../android/content/Context.md)!`, `groupData:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)<out` ` [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!,` `*>!>!`, `expandedGroupLayout:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `collapsedGroupLayout:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `groupFrom:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`, `groupTo:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!`, `childData:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)<out` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)<out` ` [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!,` `*>!>!>!`, `childLayout:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `lastChildLayout:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `childFrom:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`, `childTo:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!`)` Constructor |
| [SimpleExpandableListAdapter](../android/widget/SimpleExpandableListAdapter.md))`(`context:` ` [Context](../android/content/Context.md)!`, `groupData:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)<out` ` [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!,` `*>!>!`, `expandedGroupLayout:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `collapsedGroupLayout:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `groupFrom:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`, `groupTo:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!`, `childData:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)<out` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)<out` ` [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!,` `*>!>!>!`, `childLayout:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `childFrom:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`, `childTo:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!`)` Constructor |
| [SimpleExpandableListAdapter](../android/widget/SimpleExpandableListAdapter.md))`(`context:` ` [Context](../android/content/Context.md)!`, `groupData:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)<out` ` [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!,` `*>!>!`, `groupLayout:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `groupFrom:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`, `groupTo:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!`, `childData:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)<out` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)<out` ` [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!,` `*>!>!>!`, `childLayout:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `childFrom:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`, `childTo:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!`)` Constructor |

| Public methods ||
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getChild](../android/widget/SimpleExpandableListAdapter.md))`(`groupPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `childPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getChildId](../android/widget/SimpleExpandableListAdapter.md))`(`groupPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `childPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [View](../android/view/View.md)! | [getChildView](../android/widget/SimpleExpandableListAdapter.md))`(`groupPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `childPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `isLastChild:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `convertView:` ` [View](../android/view/View.md)!`, `parent:` ` [ViewGroup](../android/view/ViewGroup.md)!`)` <br /> |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getChildrenCount](../android/widget/SimpleExpandableListAdapter.md))`(`groupPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getGroup](../android/widget/SimpleExpandableListAdapter.md))`(`groupPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getGroupCount](../android/widget/SimpleExpandableListAdapter.md))`()` <br /> |
| --- | --- |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getGroupId](../android/widget/SimpleExpandableListAdapter.md))`(`groupPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [View](../android/view/View.md)! | [getGroupView](../android/widget/SimpleExpandableListAdapter.md))`(`groupPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `isExpanded:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `convertView:` ` [View](../android/view/View.md)!`, `parent:` ` [ViewGroup](../android/view/ViewGroup.md)!`)` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasStableIds](../android/widget/SimpleExpandableListAdapter.md))`()` <br /> |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isChildSelectable](../android/widget/SimpleExpandableListAdapter.md))`(`groupPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `childPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [View](../android/view/View.md)! | [newChildView](../android/widget/SimpleExpandableListAdapter.md))`(`isLastChild:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `parent:` ` [ViewGroup](../android/view/ViewGroup.md)!`)` Instantiates a new View for a child. |
| open [View](../android/view/View.md)! | [newGroupView](../android/widget/SimpleExpandableListAdapter.md))`(`isExpanded:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `parent:` ` [ViewGroup](../android/view/ViewGroup.md)!`)` Instantiates a new View for a group. |
| --- | --- |

| Inherited functions ||
|---|---|
| From class [BaseExpandableListAdapter](../android/widget/BaseExpandableListAdapter.md) |------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [areAllItemsEnabled](../android/widget/BaseExpandableListAdapter.md))`()` <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getChildType](../android/widget/BaseExpandableListAdapter.md))`(`groupPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `childPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Get the type of child View that will be created by [android.widget.ExpandableListAdapter#getChildView(int, int, boolean, View, ViewGroup)](../android/widget/ExpandableListAdapter.md))for the specified child item. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getChildTypeCount](../android/widget/BaseExpandableListAdapter.md))`()` <br /> Returns the number of types of child Views that will be created by [android.widget.ExpandableListAdapter#getChildView(int, int, boolean, View, ViewGroup)](../android/widget/ExpandableListAdapter.md)). Each type represents a set of views that can be converted in [android.widget.ExpandableListAdapter#getChildView(int, int, boolean, View, ViewGroup)](../android/widget/ExpandableListAdapter.md)), for any group. If the adapter always returns the same type of View for all child items, this method should return 1. This method will only be called when the adapter is set on the [AdapterView](../android/widget/AdapterView.md). <br /> | | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getCombinedChildId](../android/widget/BaseExpandableListAdapter.md))`(`groupId:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `childId:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` <br /> Override this method if you foresee a clash in IDs based on this scheme: Base implementation returns a long: - bit 0: Whether this ID points to a child (unset) or group (set), so for this method this bit will be 1. - bit 1-31: Lower 31 bits of the groupId - bit 32-63: Lower 32 bits of the childId.Gets an ID for a child that is unique across any item (either group or child) that is in this list. Expandable lists require each item (group or child) to have a unique ID among all children and groups in the list. This method is responsible for returning that unique ID given a child's ID and its group's ID. Furthermore, if [hasStableIds()](../android/widget/ExpandableListAdapter.md))is true, the returned ID must be stable as well. | | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getCombinedGroupId](../android/widget/BaseExpandableListAdapter.md))`(`groupId:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` <br /> Override this method if you foresee a clash in IDs based on this scheme: Base implementation returns a long: - bit 0: Whether this ID points to a child (unset) or group (set), so for this method this bit will be 0. - bit 1-31: Lower 31 bits of the groupId - bit 32-63: Lower 32 bits of the childId.Gets an ID for a group that is unique across any item (either group or child) that is in this list. Expandable lists require each item (group or child) to have a unique ID among all children and groups in the list. This method is responsible for returning that unique ID given a group's ID. Furthermore, if [hasStableIds()](../android/widget/ExpandableListAdapter.md))is true, the returned ID must be stable as well. | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getGroupType](../android/widget/BaseExpandableListAdapter.md))`(`groupPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Get the type of group View that will be created by [android.widget.ExpandableListAdapter#getGroupView(int, boolean, View, ViewGroup)](../android/widget/ExpandableListAdapter.md)). for the specified group item. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getGroupTypeCount](../android/widget/BaseExpandableListAdapter.md))`()` <br /> Returns the number of types of group Views that will be created by [android.widget.ExpandableListAdapter#getGroupView(int, boolean, View, ViewGroup)](../android/widget/ExpandableListAdapter.md)). Each type represents a set of views that can be converted in [android.widget.ExpandableListAdapter#getGroupView(int, boolean, View, ViewGroup)](../android/widget/ExpandableListAdapter.md)). If the adapter always returns the same type of View for all group items, this method should return 1. This method will only be called when the adapter is set on the [AdapterView](../android/widget/AdapterView.md). <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEmpty](../android/widget/BaseExpandableListAdapter.md))`()` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [notifyDataSetChanged](../android/widget/BaseExpandableListAdapter.md))`()` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [notifyDataSetInvalidated](../android/widget/BaseExpandableListAdapter.md))`()` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onGroupCollapsed](../android/widget/BaseExpandableListAdapter.md))`(`groupPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onGroupExpanded](../android/widget/BaseExpandableListAdapter.md))`(`groupPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerDataSetObserver](../android/widget/BaseExpandableListAdapter.md))`(`observer:` ` [DataSetObserver](../android/database/DataSetObserver.md)!`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unregisterDataSetObserver](../android/widget/BaseExpandableListAdapter.md))`(`observer:` ` [DataSetObserver](../android/database/DataSetObserver.md)!`)` <br /> | ||
| From class [ExpandableListAdapter](../android/widget/ExpandableListAdapter.md) |------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getChild](../android/widget/ExpandableListAdapter.md))`(`groupPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `childPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Gets the data associated with the given child within the given group. <br /> | | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getChildId](../android/widget/ExpandableListAdapter.md))`(`groupPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `childPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Gets the ID for the given child within the given group. This ID must be unique across all children within the group. The combined ID (see [getCombinedChildId(long,long)](../android/widget/ExpandableListAdapter.md))) must be unique across ALL items (groups and all children). <br /> | | [View](../android/view/View.md)! | [getChildView](../android/widget/ExpandableListAdapter.md))`(`groupPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `childPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `isLastChild:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `convertView:` ` [View](../android/view/View.md)!`, `parent:` ` [ViewGroup](../android/view/ViewGroup.md)!`)` <br /> Gets a View that displays the data for the given child within the given group. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getChildrenCount](../android/widget/ExpandableListAdapter.md))`(`groupPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Gets the number of children in a specified group. <br /> | | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getGroup](../android/widget/ExpandableListAdapter.md))`(`groupPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Gets the data associated with the given group. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getGroupCount](../android/widget/ExpandableListAdapter.md))`()` <br /> Gets the number of groups. <br /> | | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getGroupId](../android/widget/ExpandableListAdapter.md))`(`groupPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Gets the ID for the group at the given position. This group ID must be unique across groups. The combined ID (see [getCombinedGroupId(long)](../android/widget/ExpandableListAdapter.md))) must be unique across ALL items (groups and all children). <br /> | | [View](../android/view/View.md)! | [getGroupView](../android/widget/ExpandableListAdapter.md))`(`groupPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `isExpanded:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `convertView:` ` [View](../android/view/View.md)!`, `parent:` ` [ViewGroup](../android/view/ViewGroup.md)!`)` <br /> Gets a View that displays the given group. This View is only for the group--the Views for the group's children will be fetched using [getChildView(int,int,boolean,android.view.View,android.view.ViewGroup)](../android/widget/ExpandableListAdapter.md)). <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasStableIds](../android/widget/ExpandableListAdapter.md))`()` <br /> Indicates whether the child and group IDs are stable across changes to the underlying data. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isChildSelectable](../android/widget/ExpandableListAdapter.md))`(`groupPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `childPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Whether the child at the specified position is selectable. <br /> | ||

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
| `context` | [Context](../android/content/Context.md)!:The context where the [ExpandableListView](../android/widget/ExpandableListView.md) associated with this [SimpleExpandableListAdapter](../android/widget/SimpleExpandableListAdapter.md) is running |
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
| `context` | [Context](../android/content/Context.md)!:The context where the [ExpandableListView](../android/widget/ExpandableListView.md) associated with this [SimpleExpandableListAdapter](../android/widget/SimpleExpandableListAdapter.md) is running |
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
| `context` | [Context](../android/content/Context.md)!:The context where the [ExpandableListView](../android/widget/ExpandableListView.md) associated with this [SimpleExpandableListAdapter](../android/widget/SimpleExpandableListAdapter.md) is running |
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
| `convertView` | [View](../android/view/View.md)!:the old view to reuse, if possible. You should check that this view is non-null and of an appropriate type before using. If it is not possible to convert this view to display the correct data, this method can create a new view. It is not guaranteed that the convertView will have been previously created by [getChildView(int,int,boolean,android.view.View,android.view.ViewGroup)](../android/widget/ExpandableListAdapter.md)). |
| `parent` | [ViewGroup](../android/view/ViewGroup.md)!:the parent that this view will eventually be attached to |

| Return ||
|---------------------------------------------------------------------------------|---------------------------------------------------------------|
| [View](../android/view/View.md)! | the View corresponding to the child at the specified position |

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
| `convertView` | [View](../android/view/View.md)!:the old view to reuse, if possible. You should check that this view is non-null and of an appropriate type before using. If it is not possible to convert this view to display the correct data, this method can create a new view. It is not guaranteed that the convertView will have been previously created by [getGroupView(int,boolean,android.view.View,android.view.ViewGroup)](../android/widget/ExpandableListAdapter.md)). |
| --- | --- |
| `parent` | [ViewGroup](../android/view/ViewGroup.md)!:the parent that this view will eventually be attached to |

| Return ||
|---------------------------------------------------------------------------------|---------------------------------------------------------------|
| [View](../android/view/View.md)! | the View corresponding to the group at the specified position |

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
| `parent` | [ViewGroup](../android/view/ViewGroup.md)!:The eventual parent of this new View. |

| Return ||
|---------------------------------------------------------------------------------|------------------|
| [View](../android/view/View.md)! | A new child View |

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
| `parent` | [ViewGroup](../android/view/ViewGroup.md)!:The eventual parent of this new View. |

| Return ||
|---------------------------------------------------------------------------------|------------------|
| [View](../android/view/View.md)! | A new group View |
