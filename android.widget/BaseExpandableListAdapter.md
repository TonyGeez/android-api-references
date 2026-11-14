# BaseExpandableListAdapter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BaseExpandableListAdapter

Kotlin| [Java](https://developer.android.com/reference/android/widget/BaseExpandableListAdapter "View this page in Java") 
| --- | --- |

```
abstract class BaseExpandableListAdapter : ExpandableListAdapter, HeterogeneousExpandableList
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.widget.BaseExpandableListAdapter](https://developer.android.com/reference/kotlin/android/widget/BaseExpandableListAdapter#) |

| Known Direct Subclasses [CursorTreeAdapter](https://developer.android.com/reference/kotlin/android/widget/CursorTreeAdapter), [SimpleExpandableListAdapter](https://developer.android.com/reference/kotlin/android/widget/SimpleExpandableListAdapter) |--------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [CursorTreeAdapter](https://developer.android.com/reference/kotlin/android/widget/CursorTreeAdapter) | An adapter that exposes data from a series of [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#) s to an [ExpandableListView](https://developer.android.com/reference/kotlin/android/widget/ExpandableListView) widget. | | [SimpleExpandableListAdapter](https://developer.android.com/reference/kotlin/android/widget/SimpleExpandableListAdapter) | An easy adapter to map static data to group and child views defined in an XML file. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [ResourceCursorTreeAdapter](https://developer.android.com/reference/kotlin/android/widget/ResourceCursorTreeAdapter), [SimpleCursorTreeAdapter](https://developer.android.com/reference/kotlin/android/widget/SimpleCursorTreeAdapter) |----------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------| | [ResourceCursorTreeAdapter](https://developer.android.com/reference/kotlin/android/widget/ResourceCursorTreeAdapter) | A fairly simple ExpandableListAdapter that creates views defined in an XML file. | | [SimpleCursorTreeAdapter](https://developer.android.com/reference/kotlin/android/widget/SimpleCursorTreeAdapter) | An easy adapter to map columns from a cursor to TextViews or ImageViews defined in an XML file. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Base class for a [ExpandableListAdapter](https://developer.android.com/reference/kotlin/android/widget/ExpandableListAdapter) used to provide data and Views from some data to an expandable list view.

Adapters inheriting this class should verify that the base implementations of [getCombinedChildId(long,long)](https://developer.android.com/reference/kotlin/android/widget/BaseExpandableListAdapter#getCombinedChildId(kotlin.Long,%20kotlin.Long))and [getCombinedGroupId(long)](https://developer.android.com/reference/kotlin/android/widget/BaseExpandableListAdapter#getCombinedGroupId(kotlin.Long))are correct in generating unique IDs from the group/children IDs.

<br />

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [BaseExpandableListAdapter](https://developer.android.com/reference/kotlin/android/widget/BaseExpandableListAdapter#BaseExpandableListAdapter())`()` <br /> |

| Public methods ||
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [areAllItemsEnabled](https://developer.android.com/reference/kotlin/android/widget/BaseExpandableListAdapter#areAllItemsEnabled())`()` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getChildType](https://developer.android.com/reference/kotlin/android/widget/BaseExpandableListAdapter#getChildType(kotlin.Int,%20kotlin.Int))`(`groupPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `childPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Get the type of child View that will be created by [android.widget.ExpandableListAdapter#getChildView(int, int, boolean, View, ViewGroup)](https://developer.android.com/reference/kotlin/android/widget/ExpandableListAdapter#getChildView(kotlin.Int,%20kotlin.Int,%20kotlin.Boolean,%20android.view.View,%20android.view.ViewGroup))for the specified child item. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getChildTypeCount](https://developer.android.com/reference/kotlin/android/widget/BaseExpandableListAdapter#getChildTypeCount())`()` Returns the number of types of child Views that will be created by [android.widget.ExpandableListAdapter#getChildView(int, int, boolean, View, ViewGroup)](https://developer.android.com/reference/kotlin/android/widget/ExpandableListAdapter#getChildView(kotlin.Int,%20kotlin.Int,%20kotlin.Boolean,%20android.view.View,%20android.view.ViewGroup)). |
| --- | --- |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getCombinedChildId](https://developer.android.com/reference/kotlin/android/widget/BaseExpandableListAdapter#getCombinedChildId(kotlin.Long,%20kotlin.Long))`(`groupId:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `childId:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Override this method if you foresee a clash in IDs based on this scheme: |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getCombinedGroupId](https://developer.android.com/reference/kotlin/android/widget/BaseExpandableListAdapter#getCombinedGroupId(kotlin.Long))`(`groupId:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Override this method if you foresee a clash in IDs based on this scheme: |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getGroupType](https://developer.android.com/reference/kotlin/android/widget/BaseExpandableListAdapter#getGroupType(kotlin.Int))`(`groupPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Get the type of group View that will be created by [android.widget.ExpandableListAdapter#getGroupView(int, boolean, View, ViewGroup)](https://developer.android.com/reference/kotlin/android/widget/ExpandableListAdapter#getGroupView(kotlin.Int,%20kotlin.Boolean,%20android.view.View,%20android.view.ViewGroup)). |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getGroupTypeCount](https://developer.android.com/reference/kotlin/android/widget/BaseExpandableListAdapter#getGroupTypeCount())`()` Returns the number of types of group Views that will be created by [android.widget.ExpandableListAdapter#getGroupView(int, boolean, View, ViewGroup)](https://developer.android.com/reference/kotlin/android/widget/ExpandableListAdapter#getGroupView(kotlin.Int,%20kotlin.Boolean,%20android.view.View,%20android.view.ViewGroup)). |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEmpty](https://developer.android.com/reference/kotlin/android/widget/BaseExpandableListAdapter#isEmpty())`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [notifyDataSetChanged](https://developer.android.com/reference/kotlin/android/widget/BaseExpandableListAdapter#notifyDataSetChanged())`()` <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [notifyDataSetInvalidated](https://developer.android.com/reference/kotlin/android/widget/BaseExpandableListAdapter#notifyDataSetInvalidated())`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onGroupCollapsed](https://developer.android.com/reference/kotlin/android/widget/BaseExpandableListAdapter#onGroupCollapsed(kotlin.Int))`(`groupPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onGroupExpanded](https://developer.android.com/reference/kotlin/android/widget/BaseExpandableListAdapter#onGroupExpanded(kotlin.Int))`(`groupPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerDataSetObserver](https://developer.android.com/reference/kotlin/android/widget/BaseExpandableListAdapter#registerDataSetObserver(android.database.DataSetObserver))`(`observer:` ` [DataSetObserver](https://developer.android.com/reference/kotlin/android/database/DataSetObserver.html#)!`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unregisterDataSetObserver](https://developer.android.com/reference/kotlin/android/widget/BaseExpandableListAdapter#unregisterDataSetObserver(android.database.DataSetObserver))`(`observer:` ` [DataSetObserver](https://developer.android.com/reference/kotlin/android/database/DataSetObserver.html#)!`)` <br /> |

| Inherited functions ||
|---|---|
| From class [ExpandableListAdapter](https://developer.android.com/reference/kotlin/android/widget/ExpandableListAdapter) |------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getChild](https://developer.android.com/reference/kotlin/android/widget/ExpandableListAdapter#getChild(kotlin.Int,%20kotlin.Int))`(`groupPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `childPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Gets the data associated with the given child within the given group. <br /> | | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getChildId](https://developer.android.com/reference/kotlin/android/widget/ExpandableListAdapter#getChildId(kotlin.Int,%20kotlin.Int))`(`groupPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `childPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Gets the ID for the given child within the given group. This ID must be unique across all children within the group. The combined ID (see [getCombinedChildId(long,long)](https://developer.android.com/reference/kotlin/android/widget/ExpandableListAdapter#getCombinedChildId(kotlin.Long,%20kotlin.Long))) must be unique across ALL items (groups and all children). <br /> | | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)! | [getChildView](https://developer.android.com/reference/kotlin/android/widget/ExpandableListAdapter#getChildView(kotlin.Int,%20kotlin.Int,%20kotlin.Boolean,%20android.view.View,%20android.view.ViewGroup))`(`groupPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `childPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `isLastChild:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `convertView:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!`, `parent:` ` [ViewGroup](https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#)!`)` <br /> Gets a View that displays the data for the given child within the given group. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getChildrenCount](https://developer.android.com/reference/kotlin/android/widget/ExpandableListAdapter#getChildrenCount(kotlin.Int))`(`groupPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Gets the number of children in a specified group. <br /> | | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getGroup](https://developer.android.com/reference/kotlin/android/widget/ExpandableListAdapter#getGroup(kotlin.Int))`(`groupPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Gets the data associated with the given group. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getGroupCount](https://developer.android.com/reference/kotlin/android/widget/ExpandableListAdapter#getGroupCount())`()` <br /> Gets the number of groups. <br /> | | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getGroupId](https://developer.android.com/reference/kotlin/android/widget/ExpandableListAdapter#getGroupId(kotlin.Int))`(`groupPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Gets the ID for the group at the given position. This group ID must be unique across groups. The combined ID (see [getCombinedGroupId(long)](https://developer.android.com/reference/kotlin/android/widget/ExpandableListAdapter#getCombinedGroupId(kotlin.Long))) must be unique across ALL items (groups and all children). <br /> | | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)! | [getGroupView](https://developer.android.com/reference/kotlin/android/widget/ExpandableListAdapter#getGroupView(kotlin.Int,%20kotlin.Boolean,%20android.view.View,%20android.view.ViewGroup))`(`groupPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `isExpanded:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `convertView:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!`, `parent:` ` [ViewGroup](https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#)!`)` <br /> Gets a View that displays the given group. This View is only for the group--the Views for the group's children will be fetched using [getChildView(int,int,boolean,android.view.View,android.view.ViewGroup)](https://developer.android.com/reference/kotlin/android/widget/ExpandableListAdapter#getChildView(kotlin.Int,%20kotlin.Int,%20kotlin.Boolean,%20android.view.View,%20android.view.ViewGroup)). <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasStableIds](https://developer.android.com/reference/kotlin/android/widget/ExpandableListAdapter#hasStableIds())`()` <br /> Indicates whether the child and group IDs are stable across changes to the underlying data. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isChildSelectable](https://developer.android.com/reference/kotlin/android/widget/ExpandableListAdapter#isChildSelectable(kotlin.Int,%20kotlin.Int))`(`groupPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `childPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Whether the child at the specified position is selectable. <br /> | ||

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

Get the type of child View that will be created by [android.widget.ExpandableListAdapter#getChildView(int, int, boolean, View, ViewGroup)](https://developer.android.com/reference/kotlin/android/widget/ExpandableListAdapter#getChildView(kotlin.Int,%20kotlin.Int,%20kotlin.Boolean,%20android.view.View,%20android.view.ViewGroup))for the specified child item.

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

Returns the number of types of child Views that will be created by [android.widget.ExpandableListAdapter#getChildView(int, int, boolean, View, ViewGroup)](https://developer.android.com/reference/kotlin/android/widget/ExpandableListAdapter#getChildView(kotlin.Int,%20kotlin.Int,%20kotlin.Boolean,%20android.view.View,%20android.view.ViewGroup)). Each type represents a set of views that can be converted in [android.widget.ExpandableListAdapter#getChildView(int, int, boolean, View, ViewGroup)](https://developer.android.com/reference/kotlin/android/widget/ExpandableListAdapter#getChildView(kotlin.Int,%20kotlin.Int,%20kotlin.Boolean,%20android.view.View,%20android.view.ViewGroup)), for any group. If the adapter always returns the same type of View for all child items, this method should return 1.
This method will only be called when the adapter is set on the [AdapterView](https://developer.android.com/reference/kotlin/android/widget/AdapterView).

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
- bit 32-63: Lower 32 bits of the childId.Gets an ID for a child that is unique across any item (either group or child) that is in this list. Expandable lists require each item (group or child) to have a unique ID among all children and groups in the list. This method is responsible for returning that unique ID given a child's ID and its group's ID. Furthermore, if [hasStableIds()](https://developer.android.com/reference/kotlin/android/widget/ExpandableListAdapter#hasStableIds())is true, the returned ID must be stable as well.

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
- bit 32-63: Lower 32 bits of the childId.Gets an ID for a group that is unique across any item (either group or child) that is in this list. Expandable lists require each item (group or child) to have a unique ID among all children and groups in the list. This method is responsible for returning that unique ID given a group's ID. Furthermore, if [hasStableIds()](https://developer.android.com/reference/kotlin/android/widget/ExpandableListAdapter#hasStableIds())is true, the returned ID must be stable as well.

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

Get the type of group View that will be created by [android.widget.ExpandableListAdapter#getGroupView(int, boolean, View, ViewGroup)](https://developer.android.com/reference/kotlin/android/widget/ExpandableListAdapter#getGroupView(kotlin.Int,%20kotlin.Boolean,%20android.view.View,%20android.view.ViewGroup)). for the specified group item.

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

Returns the number of types of group Views that will be created by [android.widget.ExpandableListAdapter#getGroupView(int, boolean, View, ViewGroup)](https://developer.android.com/reference/kotlin/android/widget/ExpandableListAdapter#getGroupView(kotlin.Int,%20kotlin.Boolean,%20android.view.View,%20android.view.ViewGroup)). Each type represents a set of views that can be converted in [android.widget.ExpandableListAdapter#getGroupView(int, boolean, View, ViewGroup)](https://developer.android.com/reference/kotlin/android/widget/ExpandableListAdapter#getGroupView(kotlin.Int,%20kotlin.Boolean,%20android.view.View,%20android.view.ViewGroup)). If the adapter always returns the same type of View for all group items, this method should return 1.
This method will only be called when the adapter is set on the [AdapterView](https://developer.android.com/reference/kotlin/android/widget/AdapterView).

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

- [android.database.DataSetObservable#notifyChanged()](https://developer.android.com/reference/kotlin/android/database/DataSetObservable.html#notifyChanged()) 

### notifyDataSetInvalidated

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun notifyDataSetInvalidated(): Unit
```  
**See Also**

- [android.database.DataSetObservable#notifyInvalidated()](https://developer.android.com/reference/kotlin/android/database/DataSetObservable.html#notifyInvalidated()) 

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
