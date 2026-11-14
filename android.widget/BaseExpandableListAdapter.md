# BaseExpandableListAdapter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BaseExpandableListAdapter

Kotlin| [Java](BaseExpandableListAdapter.md) 
| --- | --- |

```
abstract class BaseExpandableListAdapter : ExpandableListAdapter, HeterogeneousExpandableList
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.widget.BaseExpandableListAdapter](BaseExpandableListAdapter.md) |

| Known Direct Subclasses [CursorTreeAdapter](CursorTreeAdapter.md), [SimpleExpandableListAdapter](SimpleExpandableListAdapter.md) |--------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [CursorTreeAdapter](CursorTreeAdapter.md) | An adapter that exposes data from a series of [Cursor](../android.database/Cursor.md) s to an [ExpandableListView](ExpandableListView.md) widget. | | [SimpleExpandableListAdapter](SimpleExpandableListAdapter.md) | An easy adapter to map static data to group and child views defined in an XML file. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [ResourceCursorTreeAdapter](ResourceCursorTreeAdapter.md), [SimpleCursorTreeAdapter](SimpleCursorTreeAdapter.md) |----------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------| | [ResourceCursorTreeAdapter](ResourceCursorTreeAdapter.md) | A fairly simple ExpandableListAdapter that creates views defined in an XML file. | | [SimpleCursorTreeAdapter](SimpleCursorTreeAdapter.md) | An easy adapter to map columns from a cursor to TextViews or ImageViews defined in an XML file. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Base class for a [ExpandableListAdapter](ExpandableListAdapter.md) used to provide data and Views from some data to an expandable list view.

Adapters inheriting this class should verify that the base implementations of [getCombinedChildId(long,long)](BaseExpandableListAdapter.md))and [getCombinedGroupId(long)](BaseExpandableListAdapter.md))are correct in generating unique IDs from the group/children IDs.

<br />

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [BaseExpandableListAdapter](BaseExpandableListAdapter.md))`()` <br /> |

| Public methods ||
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [areAllItemsEnabled](BaseExpandableListAdapter.md))`()` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getChildType](BaseExpandableListAdapter.md))`(`groupPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `childPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Get the type of child View that will be created by [android.widget.ExpandableListAdapter#getChildView(int, int, boolean, View, ViewGroup)](ExpandableListAdapter.md))for the specified child item. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getChildTypeCount](BaseExpandableListAdapter.md))`()` Returns the number of types of child Views that will be created by [android.widget.ExpandableListAdapter#getChildView(int, int, boolean, View, ViewGroup)](ExpandableListAdapter.md)). |
| --- | --- |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getCombinedChildId](BaseExpandableListAdapter.md))`(`groupId:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `childId:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Override this method if you foresee a clash in IDs based on this scheme: |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getCombinedGroupId](BaseExpandableListAdapter.md))`(`groupId:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Override this method if you foresee a clash in IDs based on this scheme: |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getGroupType](BaseExpandableListAdapter.md))`(`groupPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Get the type of group View that will be created by [android.widget.ExpandableListAdapter#getGroupView(int, boolean, View, ViewGroup)](ExpandableListAdapter.md)). |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getGroupTypeCount](BaseExpandableListAdapter.md))`()` Returns the number of types of group Views that will be created by [android.widget.ExpandableListAdapter#getGroupView(int, boolean, View, ViewGroup)](ExpandableListAdapter.md)). |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEmpty](BaseExpandableListAdapter.md))`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [notifyDataSetChanged](BaseExpandableListAdapter.md))`()` <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [notifyDataSetInvalidated](BaseExpandableListAdapter.md))`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onGroupCollapsed](BaseExpandableListAdapter.md))`(`groupPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onGroupExpanded](BaseExpandableListAdapter.md))`(`groupPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerDataSetObserver](BaseExpandableListAdapter.md))`(`observer:` ` [DataSetObserver](../android.database/DataSetObserver.md)!`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unregisterDataSetObserver](BaseExpandableListAdapter.md))`(`observer:` ` [DataSetObserver](../android.database/DataSetObserver.md)!`)` <br /> |

| Inherited functions ||
|---|---|
| From class [ExpandableListAdapter](ExpandableListAdapter.md) |------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getChild](ExpandableListAdapter.md))`(`groupPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `childPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Gets the data associated with the given child within the given group. <br /> | | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getChildId](ExpandableListAdapter.md))`(`groupPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `childPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Gets the ID for the given child within the given group. This ID must be unique across all children within the group. The combined ID (see [getCombinedChildId(long,long)](ExpandableListAdapter.md))) must be unique across ALL items (groups and all children). <br /> | | [View](../android.view/View.md)! | [getChildView](ExpandableListAdapter.md))`(`groupPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `childPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `isLastChild:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `convertView:` ` [View](../android.view/View.md)!`, `parent:` ` [ViewGroup](../android.view/ViewGroup.md)!`)` <br /> Gets a View that displays the data for the given child within the given group. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getChildrenCount](ExpandableListAdapter.md))`(`groupPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Gets the number of children in a specified group. <br /> | | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getGroup](ExpandableListAdapter.md))`(`groupPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Gets the data associated with the given group. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getGroupCount](ExpandableListAdapter.md))`()` <br /> Gets the number of groups. <br /> | | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getGroupId](ExpandableListAdapter.md))`(`groupPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Gets the ID for the group at the given position. This group ID must be unique across groups. The combined ID (see [getCombinedGroupId(long)](ExpandableListAdapter.md))) must be unique across ALL items (groups and all children). <br /> | | [View](../android.view/View.md)! | [getGroupView](ExpandableListAdapter.md))`(`groupPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `isExpanded:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `convertView:` ` [View](../android.view/View.md)!`, `parent:` ` [ViewGroup](../android.view/ViewGroup.md)!`)` <br /> Gets a View that displays the given group. This View is only for the group--the Views for the group's children will be fetched using [getChildView(int,int,boolean,android.view.View,android.view.ViewGroup)](ExpandableListAdapter.md)). <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasStableIds](ExpandableListAdapter.md))`()` <br /> Indicates whether the child and group IDs are stable across changes to the underlying data. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isChildSelectable](ExpandableListAdapter.md))`(`groupPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `childPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Whether the child at the specified position is selectable. <br /> | ||

## Public constructors

### BaseExpandableListAdapter

```
BaseExpandableListAdapter()
```

## Public methods

### areAllItemsEnabled

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun areAllItemsEnabled(): Boolean
```  

### getChildType

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getChildType(
    groupPosition: Int, 
    childPosition: Int
): Int
```

Get the type of child View that will be created by [android.widget.ExpandableListAdapter#getChildView(int, int, boolean, View, ViewGroup)](ExpandableListAdapter.md))for the specified child item.

| Parameters ||
|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| `groupPosition` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the position of the group that the child resides in |
| `childPosition` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the position of the child with respect to other children in the group |

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | 0 for any group or child position, since only one child type count is declared. |

### getChildTypeCount

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getChildTypeCount(): Int
```

Returns the number of types of child Views that will be created by [android.widget.ExpandableListAdapter#getChildView(int, int, boolean, View, ViewGroup)](ExpandableListAdapter.md)). Each type represents a set of views that can be converted in [android.widget.ExpandableListAdapter#getChildView(int, int, boolean, View, ViewGroup)](ExpandableListAdapter.md)), for any group. If the adapter always returns the same type of View for all child items, this method should return 1.
This method will only be called when the adapter is set on the [AdapterView](AdapterView.md).

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | 1 as a default value in BaseExpandableListAdapter. |

### getCombinedChildId

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getCombinedChildId(
    groupId: Long, 
    childId: Long
): Long
```

Override this method if you foresee a clash in IDs based on this scheme:

Base implementation returns a long:
- bit 0: Whether this ID points to a child (unset) or group (set), so for this method this bit will be 1.
- bit 1-31: Lower 31 bits of the groupId
- bit 32-63: Lower 32 bits of the childId.Gets an ID for a child that is unique across any item (either group or child) that is in this list. Expandable lists require each item (group or child) to have a unique ID among all children and groups in the list. This method is responsible for returning that unique ID given a child's ID and its group's ID. Furthermore, if [hasStableIds()](ExpandableListAdapter.md))is true, the returned ID must be stable as well.

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------------------|
| `groupId` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The ID of the group that contains this child. |
| `childId` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The ID of the child. |

| Return ||
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | The unique (and possibly stable) ID of the child across all groups and children in this list. |

### getCombinedGroupId

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getCombinedGroupId(groupId: Long): Long
```

Override this method if you foresee a clash in IDs based on this scheme:

Base implementation returns a long:
- bit 0: Whether this ID points to a child (unset) or group (set), so for this method this bit will be 0.
- bit 1-31: Lower 31 bits of the groupId
- bit 32-63: Lower 32 bits of the childId.Gets an ID for a group that is unique across any item (either group or child) that is in this list. Expandable lists require each item (group or child) to have a unique ID among all children and groups in the list. This method is responsible for returning that unique ID given a group's ID. Furthermore, if [hasStableIds()](ExpandableListAdapter.md))is true, the returned ID must be stable as well.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------|
| `groupId` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The ID of the group |

| Return ||
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | The unique (and possibly stable) ID of the group across all groups and children in this list. |

### getGroupType

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getGroupType(groupPosition: Int): Int
```

Get the type of group View that will be created by [android.widget.ExpandableListAdapter#getGroupView(int, boolean, View, ViewGroup)](ExpandableListAdapter.md)). for the specified group item.

| Parameters ||
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| `groupPosition` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the position of the group for which the type should be returned. |

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | 0 for any groupPosition, since only one group type count is declared. |

### getGroupTypeCount

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getGroupTypeCount(): Int
```

Returns the number of types of group Views that will be created by [android.widget.ExpandableListAdapter#getGroupView(int, boolean, View, ViewGroup)](ExpandableListAdapter.md)). Each type represents a set of views that can be converted in [android.widget.ExpandableListAdapter#getGroupView(int, boolean, View, ViewGroup)](ExpandableListAdapter.md)). If the adapter always returns the same type of View for all group items, this method should return 1.
This method will only be called when the adapter is set on the [AdapterView](AdapterView.md).

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | 1 as a default value in BaseExpandableListAdapter. |

### isEmpty

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isEmpty(): Boolean
```  

### notifyDataSetChanged

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun notifyDataSetChanged(): Unit
```  
**See Also**

- [android.database.DataSetObservable#notifyChanged()](../android.database/DataSetObservable.md)) 

### notifyDataSetInvalidated

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun notifyDataSetInvalidated(): Unit
```  
**See Also**

- [android.database.DataSetObservable#notifyInvalidated()](../android.database/DataSetObservable.md)) 

### onGroupCollapsed

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onGroupCollapsed(groupPosition: Int): Unit
```

| Parameters ||
|-----------------|-------------------------------------------------------------------------------------------------------|
| `groupPosition` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The group being collapsed. |

### onGroupExpanded

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onGroupExpanded(groupPosition: Int): Unit
```

| Parameters ||
|-----------------|------------------------------------------------------------------------------------------------------|
| `groupPosition` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The group being expanded. |

### registerDataSetObserver

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun registerDataSetObserver(observer: DataSetObserver!): Unit
```  

### unregisterDataSetObserver

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun unregisterDataSetObserver(observer: DataSetObserver!): Unit
```
