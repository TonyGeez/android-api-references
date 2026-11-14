# HeterogeneousExpandableList

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# HeterogeneousExpandableList

Kotlin| [Java](../android/widget/HeterogeneousExpandableList.md) 
| --- | --- |

```
interface HeterogeneousExpandableList
```

| [android.widget.HeterogeneousExpandableList](../android/widget/HeterogeneousExpandableList.md) |

| Known Direct Subclasses [BaseExpandableListAdapter](../android/widget/BaseExpandableListAdapter.md) |----------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [BaseExpandableListAdapter](../android/widget/BaseExpandableListAdapter.md) | Base class for a [ExpandableListAdapter](../android/widget/ExpandableListAdapter.md) used to provide data and Views from some data to an expandable list view. | |
| --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [CursorTreeAdapter](../android/widget/CursorTreeAdapter.md), [ResourceCursorTreeAdapter](../android/widget/ResourceCursorTreeAdapter.md), [SimpleCursorTreeAdapter](../android/widget/SimpleCursorTreeAdapter.md), [SimpleExpandableListAdapter](../android/widget/SimpleExpandableListAdapter.md) |--------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [CursorTreeAdapter](../android/widget/CursorTreeAdapter.md) | An adapter that exposes data from a series of [Cursor](../android/database/Cursor.md) s to an [ExpandableListView](../android/widget/ExpandableListView.md) widget. | | [ResourceCursorTreeAdapter](../android/widget/ResourceCursorTreeAdapter.md) | A fairly simple ExpandableListAdapter that creates views defined in an XML file. | | [SimpleCursorTreeAdapter](../android/widget/SimpleCursorTreeAdapter.md) | An easy adapter to map columns from a cursor to TextViews or ImageViews defined in an XML file. | | [SimpleExpandableListAdapter](../android/widget/SimpleExpandableListAdapter.md) | An easy adapter to map static data to group and child views defined in an XML file. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Additional methods that when implemented make an [ExpandableListAdapter](../android/widget/ExpandableListAdapter.md) take advantage of the [Adapter](../android/widget/Adapter.md) view type mechanism.

An [ExpandableListAdapter](../android/widget/ExpandableListAdapter.md) declares it has one view type for its group items and one view type for its child items. Although adapted for most [ExpandableListView](../android/widget/ExpandableListView.md) s, these values should be tuned for heterogeneous [ExpandableListView](../android/widget/ExpandableListView.md) s.
Lists that contain different types of group and/or child item views, should use an adapter that implements this interface. This way, the recycled views that will be provided to [android.widget.ExpandableListAdapter#getGroupView(int, boolean, View, ViewGroup)](../android/widget/ExpandableListAdapter.md))and [android.widget.ExpandableListAdapter#getChildView(int, int, boolean, View, ViewGroup)](../android/widget/ExpandableListAdapter.md))will be of the appropriate group or child type, resulting in a more efficient reuse of the previously created views.

## Summary

| Public methods ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getChildType](../android/widget/HeterogeneousExpandableList.md))`(`groupPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `childPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Get the type of child View that will be created by [android.widget.ExpandableListAdapter#getChildView(int, int, boolean, View, ViewGroup)](../android/widget/ExpandableListAdapter.md))for the specified child item. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getChildTypeCount](../android/widget/HeterogeneousExpandableList.md))`()` Returns the number of types of child Views that will be created by [android.widget.ExpandableListAdapter#getChildView(int, int, boolean, View, ViewGroup)](../android/widget/ExpandableListAdapter.md)). |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getGroupType](../android/widget/HeterogeneousExpandableList.md))`(`groupPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Get the type of group View that will be created by [android.widget.ExpandableListAdapter#getGroupView(int, boolean, View, ViewGroup)](../android/widget/ExpandableListAdapter.md)). |
| --- | --- |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getGroupTypeCount](../android/widget/HeterogeneousExpandableList.md))`()` Returns the number of types of group Views that will be created by [android.widget.ExpandableListAdapter#getGroupView(int, boolean, View, ViewGroup)](../android/widget/ExpandableListAdapter.md)). |

## Public methods

### getChildType

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getChildType(
    groupPosition: Int, 
    childPosition: Int
): Int
```

Get the type of child View that will be created by [android.widget.ExpandableListAdapter#getChildView(int, int, boolean, View, ViewGroup)](../android/widget/ExpandableListAdapter.md))for the specified child item.

| Parameters ||
|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| `groupPosition` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the position of the group that the child resides in |
| `childPosition` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the position of the child with respect to other children in the group |

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | An integer representing the type of child View. Two child views should share the same type if one can be converted to the other in [android.widget.ExpandableListAdapter#getChildView(int, int, boolean, View, ViewGroup)](../android/widget/ExpandableListAdapter.md))Note: Integers must be in the range 0 to [getChildTypeCount](../android/widget/HeterogeneousExpandableList.md))- 1. [android.widget.Adapter#IGNORE_ITEM_VIEW_TYPE](../android/widget/Adapter.md) can also be returned. |

**See Also**

- [android.widget.Adapter#IGNORE_ITEM_VIEW_TYPE](../android/widget/Adapter.md)
- <https://developer.android.com/reference/kotlin/android/widget/HeterogeneousExpandableList#getChildTypeCount()> 

### getChildTypeCount

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getChildTypeCount(): Int
```

Returns the number of types of child Views that will be created by [android.widget.ExpandableListAdapter#getChildView(int, int, boolean, View, ViewGroup)](../android/widget/ExpandableListAdapter.md)). Each type represents a set of views that can be converted in [android.widget.ExpandableListAdapter#getChildView(int, int, boolean, View, ViewGroup)](../android/widget/ExpandableListAdapter.md)), for any group. If the adapter always returns the same type of View for all child items, this method should return 1.
This method will only be called when the adapter is set on the [AdapterView](../android/widget/AdapterView.md).

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The total number of types of child Views that will be created by this adapter. |

**See Also**

- <https://developer.android.com/reference/kotlin/android/widget/HeterogeneousExpandableList#getGroupTypeCount()>
- [#getChildType(int, int)](../android/widget/HeterogeneousExpandableList.md)) 

### getGroupType

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getGroupType(groupPosition: Int): Int
```

Get the type of group View that will be created by [android.widget.ExpandableListAdapter#getGroupView(int, boolean, View, ViewGroup)](../android/widget/ExpandableListAdapter.md)). for the specified group item.

| Parameters ||
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| `groupPosition` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the position of the group for which the type should be returned. |

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | An integer representing the type of group View. Two group views should share the same type if one can be converted to the other in [android.widget.ExpandableListAdapter#getGroupView(int, boolean, View, ViewGroup)](../android/widget/ExpandableListAdapter.md)). Note: Integers must be in the range 0 to [getGroupTypeCount](../android/widget/HeterogeneousExpandableList.md))- 1. [android.widget.Adapter#IGNORE_ITEM_VIEW_TYPE](../android/widget/Adapter.md) can also be returned. |

**See Also**

- [android.widget.Adapter#IGNORE_ITEM_VIEW_TYPE](../android/widget/Adapter.md)
- <https://developer.android.com/reference/kotlin/android/widget/HeterogeneousExpandableList#getGroupTypeCount()> 

### getGroupTypeCount

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getGroupTypeCount(): Int
```

Returns the number of types of group Views that will be created by [android.widget.ExpandableListAdapter#getGroupView(int, boolean, View, ViewGroup)](../android/widget/ExpandableListAdapter.md)). Each type represents a set of views that can be converted in [android.widget.ExpandableListAdapter#getGroupView(int, boolean, View, ViewGroup)](../android/widget/ExpandableListAdapter.md)). If the adapter always returns the same type of View for all group items, this method should return 1.
This method will only be called when the adapter is set on the [AdapterView](../android/widget/AdapterView.md).

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The number of types of group Views that will be created by this adapter. |

**See Also**

- <https://developer.android.com/reference/kotlin/android/widget/HeterogeneousExpandableList#getChildTypeCount()>
- [#getGroupType(int)](../android/widget/HeterogeneousExpandableList.md))
