# ResourceCursorTreeAdapter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ResourceCursorTreeAdapter

Kotlin| [Java](../android/widget/ResourceCursorTreeAdapter.md) 
| --- | --- |

```
abstract class ResourceCursorTreeAdapter : CursorTreeAdapter
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [android.widget.BaseExpandableListAdapter](../android/widget/BaseExpandableListAdapter.md) |||
| | ↳ | [android.widget.CursorTreeAdapter](../android/widget/CursorTreeAdapter.md) ||
| | | ↳ | [android.widget.ResourceCursorTreeAdapter](../android/widget/ResourceCursorTreeAdapter.md) |
| --- | --- | --- | --- |

| Known Direct Subclasses [SimpleCursorTreeAdapter](../android/widget/SimpleCursorTreeAdapter.md) |------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------| | [SimpleCursorTreeAdapter](../android/widget/SimpleCursorTreeAdapter.md) | An easy adapter to map columns from a cursor to TextViews or ImageViews defined in an XML file. | |
| --- | --- | --- | --- | --- | --- | --- |

A fairly simple ExpandableListAdapter that creates views defined in an XML file. You can specify the XML file that defines the appearance of the views.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ResourceCursorTreeAdapter](../android/widget/ResourceCursorTreeAdapter.md))`(`context:` ` [Context](../android/content/Context.md)!`, `cursor:` ` [Cursor](../android/database/Cursor.md)!`, `groupLayout:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `childLayout:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Constructor. |
| [ResourceCursorTreeAdapter](../android/widget/ResourceCursorTreeAdapter.md))`(`context:` ` [Context](../android/content/Context.md)!`, `cursor:` ` [Cursor](../android/database/Cursor.md)!`, `collapsedGroupLayout:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `expandedGroupLayout:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `childLayout:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Constructor. |
| [ResourceCursorTreeAdapter](../android/widget/ResourceCursorTreeAdapter.md))`(`context:` ` [Context](../android/content/Context.md)!`, `cursor:` ` [Cursor](../android/database/Cursor.md)!`, `collapsedGroupLayout:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `expandedGroupLayout:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `childLayout:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `lastChildLayout:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Constructor. |

| Public methods ||
|-------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [View](../android/view/View.md)! | [newChildView](../android/widget/ResourceCursorTreeAdapter.md))`(`context:` ` [Context](../android/content/Context.md)!`, `cursor:` ` [Cursor](../android/database/Cursor.md)!`, `isLastChild:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `parent:` ` [ViewGroup](../android/view/ViewGroup.md)!`)` <br /> |
| open [View](../android/view/View.md)! | [newGroupView](../android/widget/ResourceCursorTreeAdapter.md))`(`context:` ` [Context](../android/content/Context.md)!`, `cursor:` ` [Cursor](../android/database/Cursor.md)!`, `isExpanded:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `parent:` ` [ViewGroup](../android/view/ViewGroup.md)!`)` <br /> |

| Inherited functions ||
|---|---|
| From class [BaseExpandableListAdapter](../android/widget/BaseExpandableListAdapter.md) |------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [areAllItemsEnabled](../android/widget/BaseExpandableListAdapter.md))`()` <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getChildType](../android/widget/BaseExpandableListAdapter.md))`(`groupPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `childPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Get the type of child View that will be created by [android.widget.ExpandableListAdapter#getChildView(int, int, boolean, View, ViewGroup)](../android/widget/ExpandableListAdapter.md))for the specified child item. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getChildTypeCount](../android/widget/BaseExpandableListAdapter.md))`()` <br /> Returns the number of types of child Views that will be created by [android.widget.ExpandableListAdapter#getChildView(int, int, boolean, View, ViewGroup)](../android/widget/ExpandableListAdapter.md)). Each type represents a set of views that can be converted in [android.widget.ExpandableListAdapter#getChildView(int, int, boolean, View, ViewGroup)](../android/widget/ExpandableListAdapter.md)), for any group. If the adapter always returns the same type of View for all child items, this method should return 1. This method will only be called when the adapter is set on the [AdapterView](../android/widget/AdapterView.md). <br /> | | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getCombinedChildId](../android/widget/BaseExpandableListAdapter.md))`(`groupId:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `childId:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` <br /> Override this method if you foresee a clash in IDs based on this scheme: Base implementation returns a long: - bit 0: Whether this ID points to a child (unset) or group (set), so for this method this bit will be 1. - bit 1-31: Lower 31 bits of the groupId - bit 32-63: Lower 32 bits of the childId.Gets an ID for a child that is unique across any item (either group or child) that is in this list. Expandable lists require each item (group or child) to have a unique ID among all children and groups in the list. This method is responsible for returning that unique ID given a child's ID and its group's ID. Furthermore, if [hasStableIds()](../android/widget/ExpandableListAdapter.md))is true, the returned ID must be stable as well. | | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getCombinedGroupId](../android/widget/BaseExpandableListAdapter.md))`(`groupId:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` <br /> Override this method if you foresee a clash in IDs based on this scheme: Base implementation returns a long: - bit 0: Whether this ID points to a child (unset) or group (set), so for this method this bit will be 0. - bit 1-31: Lower 31 bits of the groupId - bit 32-63: Lower 32 bits of the childId.Gets an ID for a group that is unique across any item (either group or child) that is in this list. Expandable lists require each item (group or child) to have a unique ID among all children and groups in the list. This method is responsible for returning that unique ID given a group's ID. Furthermore, if [hasStableIds()](../android/widget/ExpandableListAdapter.md))is true, the returned ID must be stable as well. | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getGroupType](../android/widget/BaseExpandableListAdapter.md))`(`groupPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Get the type of group View that will be created by [android.widget.ExpandableListAdapter#getGroupView(int, boolean, View, ViewGroup)](../android/widget/ExpandableListAdapter.md)). for the specified group item. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getGroupTypeCount](../android/widget/BaseExpandableListAdapter.md))`()` <br /> Returns the number of types of group Views that will be created by [android.widget.ExpandableListAdapter#getGroupView(int, boolean, View, ViewGroup)](../android/widget/ExpandableListAdapter.md)). Each type represents a set of views that can be converted in [android.widget.ExpandableListAdapter#getGroupView(int, boolean, View, ViewGroup)](../android/widget/ExpandableListAdapter.md)). If the adapter always returns the same type of View for all group items, this method should return 1. This method will only be called when the adapter is set on the [AdapterView](../android/widget/AdapterView.md). <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEmpty](../android/widget/BaseExpandableListAdapter.md))`()` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onGroupExpanded](../android/widget/BaseExpandableListAdapter.md))`(`groupPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerDataSetObserver](../android/widget/BaseExpandableListAdapter.md))`(`observer:` ` [DataSetObserver](../android/database/DataSetObserver.md)!`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unregisterDataSetObserver](../android/widget/BaseExpandableListAdapter.md))`(`observer:` ` [DataSetObserver](../android/database/DataSetObserver.md)!`)` <br /> | ||
| From class [CursorTreeAdapter](../android/widget/CursorTreeAdapter.md) |-----------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [bindChildView](../android/widget/CursorTreeAdapter.md))`(`view:` ` [View](../android/view/View.md)!`, `context:` ` [Context](../android/content/Context.md)!`, `cursor:` ` [Cursor](../android/database/Cursor.md)!`, `isLastChild:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Bind an existing view to the child data pointed to by cursor <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [bindGroupView](../android/widget/CursorTreeAdapter.md))`(`view:` ` [View](../android/view/View.md)!`, `context:` ` [Context](../android/content/Context.md)!`, `cursor:` ` [Cursor](../android/database/Cursor.md)!`, `isExpanded:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Bind an existing view to the group data pointed to by cursor. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [changeCursor](../android/widget/CursorTreeAdapter.md))`(`cursor:` ` [Cursor](../android/database/Cursor.md)!`)` <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [convertToString](../android/widget/CursorTreeAdapter.md))`(`cursor:` ` [Cursor](../android/database/Cursor.md)!`)` <br /> | | [Cursor](../android/database/Cursor.md)! | [getChild](../android/widget/CursorTreeAdapter.md))`(`groupPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `childPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> | | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getChildId](../android/widget/CursorTreeAdapter.md))`(`groupPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `childPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> | | [View](../android/view/View.md)! | [getChildView](../android/widget/CursorTreeAdapter.md))`(`groupPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `childPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `isLastChild:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `convertView:` ` [View](../android/view/View.md)!`, `parent:` ` [ViewGroup](../android/view/ViewGroup.md)!`)` <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getChildrenCount](../android/widget/CursorTreeAdapter.md))`(`groupPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> | | [Cursor](../android/database/Cursor.md)! | [getChildrenCursor](../android/widget/CursorTreeAdapter.md))`(`groupCursor:` ` [Cursor](../android/database/Cursor.md)!`)` <br /> Gets the Cursor for the children at the given group. Subclasses must implement this method to return the children data for a particular group. If you want to asynchronously query a provider to prevent blocking the UI, it is possible to return null and at a later time call [setChildrenCursor(int,android.database.Cursor)](../android/widget/CursorTreeAdapter.md)). It is your responsibility to manage this Cursor through the Activity lifecycle. It is a good idea to use [Activity.managedQuery](../android/app/Activity.md))which will handle this for you. In some situations, the adapter will deactivate the Cursor on its own, but this will not always be the case, so please ensure the Cursor is properly managed. <br /> | | [Cursor](../android/database/Cursor.md)! | [getCursor](../android/widget/CursorTreeAdapter.md))`()` <br /> | | [Filter](../android/widget/Filter.md)! | [getFilter](../android/widget/CursorTreeAdapter.md))`()` <br /> | | [FilterQueryProvider](../android/widget/FilterQueryProvider.md)! | [getFilterQueryProvider](../android/widget/CursorTreeAdapter.md))`()` <br /> | | [Cursor](../android/database/Cursor.md)! | [getGroup](../android/widget/CursorTreeAdapter.md))`(`groupPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getGroupCount](../android/widget/CursorTreeAdapter.md))`()` <br /> | | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getGroupId](../android/widget/CursorTreeAdapter.md))`(`groupPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> | | [View](../android/view/View.md)! | [getGroupView](../android/widget/CursorTreeAdapter.md))`(`groupPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `isExpanded:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `convertView:` ` [View](../android/view/View.md)!`, `parent:` ` [ViewGroup](../android/view/ViewGroup.md)!`)` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasStableIds](../android/widget/CursorTreeAdapter.md))`()` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isChildSelectable](../android/widget/CursorTreeAdapter.md))`(`groupPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `childPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [notifyDataSetChanged](../android/widget/CursorTreeAdapter.md))`()` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [notifyDataSetChanged](../android/widget/CursorTreeAdapter.md))`(`releaseCursors:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Notifies a data set change, but with the option of not releasing any cached cursors. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [notifyDataSetInvalidated](../android/widget/CursorTreeAdapter.md))`()` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onGroupCollapsed](../android/widget/CursorTreeAdapter.md))`(`groupPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> | | [Cursor](../android/database/Cursor.md)! | [runQueryOnBackgroundThread](../android/widget/CursorTreeAdapter.md))`(`constraint:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setChildrenCursor](../android/widget/CursorTreeAdapter.md))`(`groupPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `childrenCursor:` ` [Cursor](../android/database/Cursor.md)!`)` <br /> Sets the children Cursor for a particular group. If there is an existing cursor it will be closed. This is useful when asynchronously querying to prevent blocking the UI. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFilterQueryProvider](../android/widget/CursorTreeAdapter.md))`(`filterQueryProvider:` ` [FilterQueryProvider](../android/widget/FilterQueryProvider.md)!`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setGroupCursor](../android/widget/CursorTreeAdapter.md))`(`cursor:` ` [Cursor](../android/database/Cursor.md)!`)` <br /> Sets the group Cursor. <br /> | ||
| From class [ExpandableListAdapter](../android/widget/ExpandableListAdapter.md) |------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getChild](../android/widget/ExpandableListAdapter.md))`(`groupPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `childPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Gets the data associated with the given child within the given group. <br /> | | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getChildId](../android/widget/ExpandableListAdapter.md))`(`groupPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `childPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Gets the ID for the given child within the given group. This ID must be unique across all children within the group. The combined ID (see [getCombinedChildId(long,long)](../android/widget/ExpandableListAdapter.md))) must be unique across ALL items (groups and all children). <br /> | | [View](../android/view/View.md)! | [getChildView](../android/widget/ExpandableListAdapter.md))`(`groupPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `childPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `isLastChild:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `convertView:` ` [View](../android/view/View.md)!`, `parent:` ` [ViewGroup](../android/view/ViewGroup.md)!`)` <br /> Gets a View that displays the data for the given child within the given group. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getChildrenCount](../android/widget/ExpandableListAdapter.md))`(`groupPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Gets the number of children in a specified group. <br /> | | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getGroup](../android/widget/ExpandableListAdapter.md))`(`groupPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Gets the data associated with the given group. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getGroupCount](../android/widget/ExpandableListAdapter.md))`()` <br /> Gets the number of groups. <br /> | | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getGroupId](../android/widget/ExpandableListAdapter.md))`(`groupPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Gets the ID for the group at the given position. This group ID must be unique across groups. The combined ID (see [getCombinedGroupId(long)](../android/widget/ExpandableListAdapter.md))) must be unique across ALL items (groups and all children). <br /> | | [View](../android/view/View.md)! | [getGroupView](../android/widget/ExpandableListAdapter.md))`(`groupPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `isExpanded:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `convertView:` ` [View](../android/view/View.md)!`, `parent:` ` [ViewGroup](../android/view/ViewGroup.md)!`)` <br /> Gets a View that displays the given group. This View is only for the group--the Views for the group's children will be fetched using [getChildView(int,int,boolean,android.view.View,android.view.ViewGroup)](../android/widget/ExpandableListAdapter.md)). <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasStableIds](../android/widget/ExpandableListAdapter.md))`()` <br /> Indicates whether the child and group IDs are stable across changes to the underlying data. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isChildSelectable](../android/widget/ExpandableListAdapter.md))`(`groupPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `childPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Whether the child at the specified position is selectable. <br /> | ||
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

## Public constructors

### ResourceCursorTreeAdapter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ResourceCursorTreeAdapter(
    context: Context!, 
    cursor: Cursor!, 
    groupLayout: Int, 
    childLayout: Int)
```

Constructor.

| Parameters ||
|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android/content/Context.md)!:The context where the ListView associated with this SimpleListItemFactory is running |
| `cursor` | [Cursor](../android/database/Cursor.md)!:The database cursor |
| `groupLayout` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):resource identifier of a layout file that defines the views for all groups. |
| --- | --- |
| `childLayout` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):resource identifier of a layout file that defines the views for all children. |

### ResourceCursorTreeAdapter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ResourceCursorTreeAdapter(
    context: Context!, 
    cursor: Cursor!, 
    collapsedGroupLayout: Int, 
    expandedGroupLayout: Int, 
    childLayout: Int)
```

Constructor.

| Parameters ||
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android/content/Context.md)!:The context where the ListView associated with this SimpleListItemFactory is running |
| `cursor` | [Cursor](../android/database/Cursor.md)!:The database cursor |
| `collapsedGroupLayout` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):resource identifier of a layout file that defines the views for collapsed groups. |
| --- | --- |
| `expandedGroupLayout` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):resource identifier of a layout file that defines the views for expanded groups. |
| `childLayout` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):resource identifier of a layout file that defines the views for all children. |

### ResourceCursorTreeAdapter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ResourceCursorTreeAdapter(
    context: Context!, 
    cursor: Cursor!, 
    collapsedGroupLayout: Int, 
    expandedGroupLayout: Int, 
    childLayout: Int, 
    lastChildLayout: Int)
```

Constructor.

| Parameters ||
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android/content/Context.md)!:The context where the ListView associated with this SimpleListItemFactory is running |
| `cursor` | [Cursor](../android/database/Cursor.md)!:The database cursor |
| `collapsedGroupLayout` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):resource identifier of a layout file that defines the views for collapsed groups. |
| --- | --- |
| `expandedGroupLayout` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):resource identifier of a layout file that defines the views for expanded groups. |
| `childLayout` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):resource identifier of a layout file that defines the views for all children but the last.. |
| `lastChildLayout` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):resource identifier of a layout file that defines the views for the last child of a group. |
| --- | --- |

## Public methods

### newChildView

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun newChildView(
    context: Context!, 
    cursor: Cursor!, 
    isLastChild: Boolean, 
    parent: ViewGroup!
): View!
```

| Parameters ||
|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android/content/Context.md)!:Interface to application's global information |
| `cursor` | [Cursor](../android/database/Cursor.md)!:The cursor from which to get the data. The cursor is already moved to the correct position. |
| `isLastChild` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):Whether the child is the last child within its group. |
| --- | --- |
| `parent` | [ViewGroup](../android/view/ViewGroup.md)!:The parent to which the new view is attached to |

| Return ||
|---------------------------------------------------------------------------------|-------------------------|
| [View](../android/view/View.md)! | the newly created view. |

### newGroupView

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun newGroupView(
    context: Context!, 
    cursor: Cursor!, 
    isExpanded: Boolean, 
    parent: ViewGroup!
): View!
```

| Parameters ||
|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android/content/Context.md)!:Interface to application's global information |
| `cursor` | [Cursor](../android/database/Cursor.md)!:The group cursor from which to get the data. The cursor is already moved to the correct position. |
| `isExpanded` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):Whether the group is expanded. |
| --- | --- |
| `parent` | [ViewGroup](../android/view/ViewGroup.md)!:The parent to which the new view is attached to |

| Return ||
|---------------------------------------------------------------------------------|-------------------------|
| [View](../android/view/View.md)! | The newly created view. |
