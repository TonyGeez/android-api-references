# ExpandableListAdapter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ExpandableListAdapter

Kotlin| [Java](ExpandableListAdapter.md) 
| --- | --- |

```
interface ExpandableListAdapter
```

| [android.widget.ExpandableListAdapter](ExpandableListAdapter.md) |

| Known Direct Subclasses [BaseExpandableListAdapter](BaseExpandableListAdapter.md) |----------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [BaseExpandableListAdapter](BaseExpandableListAdapter.md) | Base class for a [ExpandableListAdapter](ExpandableListAdapter.md) used to provide data and Views from some data to an expandable list view. | |
| --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [CursorTreeAdapter](CursorTreeAdapter.md), [ResourceCursorTreeAdapter](ResourceCursorTreeAdapter.md), [SimpleCursorTreeAdapter](SimpleCursorTreeAdapter.md), [SimpleExpandableListAdapter](SimpleExpandableListAdapter.md) |--------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [CursorTreeAdapter](CursorTreeAdapter.md) | An adapter that exposes data from a series of [Cursor](../android.database/Cursor.md) s to an [ExpandableListView](ExpandableListView.md) widget. | | [ResourceCursorTreeAdapter](ResourceCursorTreeAdapter.md) | A fairly simple ExpandableListAdapter that creates views defined in an XML file. | | [SimpleCursorTreeAdapter](SimpleCursorTreeAdapter.md) | An easy adapter to map columns from a cursor to TextViews or ImageViews defined in an XML file. | | [SimpleExpandableListAdapter](SimpleExpandableListAdapter.md) | An easy adapter to map static data to group and child views defined in an XML file. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

An adapter that links a [ExpandableListView](ExpandableListView.md) with the underlying data. The implementation of this interface will provide access to the data of the children (categorized by groups), and also instantiate [View](../android.view/View.md) s for children and groups.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [areAllItemsEnabled](ExpandableListAdapter.md))`()` <br /> |
| abstract [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getChild](ExpandableListAdapter.md))`(`groupPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `childPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Gets the data associated with the given child within the given group. |
| abstract [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getChildId](ExpandableListAdapter.md))`(`groupPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `childPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Gets the ID for the given child within the given group. |
| --- | --- |
| abstract [View](../android.view/View.md)! | [getChildView](ExpandableListAdapter.md))`(`groupPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `childPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `isLastChild:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `convertView:` ` [View](../android.view/View.md)!`, `parent:` ` [ViewGroup](../android.view/ViewGroup.md)!`)` Gets a View that displays the data for the given child within the given group. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getChildrenCount](ExpandableListAdapter.md))`(`groupPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Gets the number of children in a specified group. |
| abstract [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getCombinedChildId](ExpandableListAdapter.md))`(`groupId:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `childId:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Gets an ID for a child that is unique across any item (either group or child) that is in this list. |
| --- | --- |
| abstract [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getCombinedGroupId](ExpandableListAdapter.md))`(`groupId:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Gets an ID for a group that is unique across any item (either group or child) that is in this list. |
| abstract [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getGroup](ExpandableListAdapter.md))`(`groupPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Gets the data associated with the given group. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getGroupCount](ExpandableListAdapter.md))`()` Gets the number of groups. |
| --- | --- |
| abstract [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getGroupId](ExpandableListAdapter.md))`(`groupPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Gets the ID for the group at the given position. |
| abstract [View](../android.view/View.md)! | [getGroupView](ExpandableListAdapter.md))`(`groupPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `isExpanded:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `convertView:` ` [View](../android.view/View.md)!`, `parent:` ` [ViewGroup](../android.view/ViewGroup.md)!`)` Gets a View that displays the given group. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasStableIds](ExpandableListAdapter.md))`()` Indicates whether the child and group IDs are stable across changes to the underlying data. |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isChildSelectable](ExpandableListAdapter.md))`(`groupPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `childPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Whether the child at the specified position is selectable. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEmpty](ExpandableListAdapter.md))`()` <br /> |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onGroupCollapsed](ExpandableListAdapter.md))`(`groupPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called when a group is collapsed. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onGroupExpanded](ExpandableListAdapter.md))`(`groupPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called when a group is expanded. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerDataSetObserver](ExpandableListAdapter.md))`(`observer:` ` [DataSetObserver](../android.database/DataSetObserver.md)!`)` <br /> |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unregisterDataSetObserver](ExpandableListAdapter.md))`(`observer:` ` [DataSetObserver](../android.database/DataSetObserver.md)!`)` <br /> |
| --- | --- |

## Public methods

### areAllItemsEnabled

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun areAllItemsEnabled(): Boolean
```  
**See Also**

- [android.widget.ListAdapter#areAllItemsEnabled()](ListAdapter.md)) 

### getChild

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getChild(
    groupPosition: Int, 
    childPosition: Int
): Any!
```

Gets the data associated with the given child within the given group.

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
abstract fun getChildId(
    groupPosition: Int, 
    childPosition: Int
): Long
```

Gets the ID for the given child within the given group. This ID must be unique across all children within the group. The combined ID (see [getCombinedChildId(long,long)](ExpandableListAdapter.md))) must be unique across ALL items (groups and all children).

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
abstract fun getChildView(
    groupPosition: Int, 
    childPosition: Int, 
    isLastChild: Boolean, 
    convertView: View!, 
    parent: ViewGroup!
): View!
```

Gets a View that displays the data for the given child within the given group.

| Parameters ||
|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `groupPosition` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the position of the group that contains the child |
| `childPosition` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the position of the child (for which the View is returned) within the group |
| `isLastChild` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):Whether the child is the last child within the group |
| --- | --- |
| `convertView` | [View](../android.view/View.md)!:the old view to reuse, if possible. You should check that this view is non-null and of an appropriate type before using. If it is not possible to convert this view to display the correct data, this method can create a new view. It is not guaranteed that the convertView will have been previously created by [getChildView(int,int,boolean,android.view.View,android.view.ViewGroup)](ExpandableListAdapter.md)). |
| `parent` | [ViewGroup](../android.view/ViewGroup.md)!:the parent that this view will eventually be attached to |

| Return ||
|---------------------------------------------------------------------------------|---------------------------------------------------------------|
| [View](../android.view/View.md)! | the View corresponding to the child at the specified position |

### getChildrenCount

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getChildrenCount(groupPosition: Int): Int
```

Gets the number of children in a specified group.

| Parameters ||
|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `groupPosition` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the position of the group for which the children count should be returned |

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the children count in the specified group |

### getCombinedChildId

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getCombinedChildId(
    groupId: Long, 
    childId: Long
): Long
```

Gets an ID for a child that is unique across any item (either group or child) that is in this list. Expandable lists require each item (group or child) to have a unique ID among all children and groups in the list. This method is responsible for returning that unique ID given a child's ID and its group's ID. Furthermore, if [hasStableIds()](ExpandableListAdapter.md))is true, the returned ID must be stable as well.

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
abstract fun getCombinedGroupId(groupId: Long): Long
```

Gets an ID for a group that is unique across any item (either group or child) that is in this list. Expandable lists require each item (group or child) to have a unique ID among all children and groups in the list. This method is responsible for returning that unique ID given a group's ID. Furthermore, if [hasStableIds()](ExpandableListAdapter.md))is true, the returned ID must be stable as well.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------|
| `groupId` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The ID of the group |

| Return ||
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | The unique (and possibly stable) ID of the group across all groups and children in this list. |

### getGroup

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getGroup(groupPosition: Int): Any!
```

Gets the data associated with the given group.

| Parameters ||
|-----------------|------------------------------------------------------------------------------------------------------|
| `groupPosition` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the position of the group |

| Return ||
|-----------------------------------------------------------------------------|----------------------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | the data child for the specified group |

### getGroupCount

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getGroupCount(): Int
```

Gets the number of groups.

| Return ||
|----------------------------------------------------------------------------|----------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of groups |

### getGroupId

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getGroupId(groupPosition: Int): Long
```

Gets the ID for the group at the given position. This group ID must be unique across groups. The combined ID (see [getCombinedGroupId(long)](ExpandableListAdapter.md))) must be unique across ALL items (groups and all children).

| Parameters ||
|-----------------|---------------------------------------------------------------------------------------------------------------------------------|
| `groupPosition` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the position of the group for which the ID is wanted |

| Return ||
|------------------------------------------------------------------------------|----------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the ID associated with the group |

### getGroupView

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getGroupView(
    groupPosition: Int, 
    isExpanded: Boolean, 
    convertView: View!, 
    parent: ViewGroup!
): View!
```

Gets a View that displays the given group. This View is only for the group--the Views for the group's children will be fetched using [getChildView(int,int,boolean,android.view.View,android.view.ViewGroup)](ExpandableListAdapter.md)).

| Parameters ||
|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `groupPosition` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the position of the group for which the View is returned |
| `isExpanded` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):whether the group is expanded or collapsed |
| `convertView` | [View](../android.view/View.md)!:the old view to reuse, if possible. You should check that this view is non-null and of an appropriate type before using. If it is not possible to convert this view to display the correct data, this method can create a new view. It is not guaranteed that the convertView will have been previously created by [getGroupView(int,boolean,android.view.View,android.view.ViewGroup)](ExpandableListAdapter.md)). |
| --- | --- |
| `parent` | [ViewGroup](../android.view/ViewGroup.md)!:the parent that this view will eventually be attached to |

| Return ||
|---------------------------------------------------------------------------------|---------------------------------------------------------------|
| [View](../android.view/View.md)! | the View corresponding to the group at the specified position |

### hasStableIds

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun hasStableIds(): Boolean
```

Indicates whether the child and group IDs are stable across changes to the underlying data.

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | whether or not the same ID always refers to the same object |

**See Also**

- [android.widget.Adapter#hasStableIds()](Adapter.md)) 

### isChildSelectable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isChildSelectable(
    groupPosition: Int, 
    childPosition: Int
): Boolean
```

Whether the child at the specified position is selectable.

| Parameters ||
|-----------------|------------------------------------------------------------------------------------------------------------------------------|
| `groupPosition` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the position of the group that contains the child |
| `childPosition` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the position of the child within the group |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | whether the child is selectable. |

### isEmpty

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isEmpty(): Boolean
```  
**See Also**

- [android.widget.ListAdapter#isEmpty()](Adapter.md)) 

### onGroupCollapsed

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onGroupCollapsed(groupPosition: Int): Unit
```

Called when a group is collapsed.

| Parameters ||
|-----------------|-------------------------------------------------------------------------------------------------------|
| `groupPosition` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The group being collapsed. |

### onGroupExpanded

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onGroupExpanded(groupPosition: Int): Unit
```

Called when a group is expanded.

| Parameters ||
|-----------------|------------------------------------------------------------------------------------------------------|
| `groupPosition` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The group being expanded. |

### registerDataSetObserver

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun registerDataSetObserver(observer: DataSetObserver!): Unit
```  
**See Also**

- [android.widget.Adapter#registerDataSetObserver(DataSetObserver)](Adapter.md)) 

### unregisterDataSetObserver

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun unregisterDataSetObserver(observer: DataSetObserver!): Unit
```  
**See Also**

- [android.widget.Adapter#unregisterDataSetObserver(DataSetObserver)](Adapter.md))
