# HeterogeneousExpandableList

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# HeterogeneousExpandableList

Kotlin| [Java](https://developer.android.com/reference/android/widget/HeterogeneousExpandableList "View this page in Java") 

```
interface HeterogeneousExpandableList
```

| [android.widget.HeterogeneousExpandableList](https://developer.android.com/reference/kotlin/android/widget/HeterogeneousExpandableList#) |

| Known Direct Subclasses [BaseExpandableListAdapter](https://developer.android.com/reference/kotlin/android/widget/BaseExpandableListAdapter) |----------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [BaseExpandableListAdapter](https://developer.android.com/reference/kotlin/android/widget/BaseExpandableListAdapter) | Base class for a [ExpandableListAdapter](https://developer.android.com/reference/kotlin/android/widget/ExpandableListAdapter) used to provide data and Views from some data to an expandable list view. | |

| Known Indirect Subclasses [CursorTreeAdapter](https://developer.android.com/reference/kotlin/android/widget/CursorTreeAdapter), [ResourceCursorTreeAdapter](https://developer.android.com/reference/kotlin/android/widget/ResourceCursorTreeAdapter), [SimpleCursorTreeAdapter](https://developer.android.com/reference/kotlin/android/widget/SimpleCursorTreeAdapter), [SimpleExpandableListAdapter](https://developer.android.com/reference/kotlin/android/widget/SimpleExpandableListAdapter) |--------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [CursorTreeAdapter](https://developer.android.com/reference/kotlin/android/widget/CursorTreeAdapter) | An adapter that exposes data from a series of [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#) s to an [ExpandableListView](https://developer.android.com/reference/kotlin/android/widget/ExpandableListView) widget. | | [ResourceCursorTreeAdapter](https://developer.android.com/reference/kotlin/android/widget/ResourceCursorTreeAdapter) | A fairly simple ExpandableListAdapter that creates views defined in an XML file. | | [SimpleCursorTreeAdapter](https://developer.android.com/reference/kotlin/android/widget/SimpleCursorTreeAdapter) | An easy adapter to map columns from a cursor to TextViews or ImageViews defined in an XML file. | | [SimpleExpandableListAdapter](https://developer.android.com/reference/kotlin/android/widget/SimpleExpandableListAdapter) | An easy adapter to map static data to group and child views defined in an XML file. | |

Additional methods that when implemented make an [ExpandableListAdapter](https://developer.android.com/reference/kotlin/android/widget/ExpandableListAdapter) take advantage of the [Adapter](https://developer.android.com/reference/kotlin/android/widget/Adapter) view type mechanism.

An [ExpandableListAdapter](https://developer.android.com/reference/kotlin/android/widget/ExpandableListAdapter) declares it has one view type for its group items and one view type for its child items. Although adapted for most [ExpandableListView](https://developer.android.com/reference/kotlin/android/widget/ExpandableListView) s, these values should be tuned for heterogeneous [ExpandableListView](https://developer.android.com/reference/kotlin/android/widget/ExpandableListView) s.
Lists that contain different types of group and/or child item views, should use an adapter that implements this interface. This way, the recycled views that will be provided to [android.widget.ExpandableListAdapter#getGroupView(int, boolean, View, ViewGroup)](https://developer.android.com/reference/kotlin/android/widget/ExpandableListAdapter#getGroupView(kotlin.Int,%20kotlin.Boolean,%20android.view.View,%20android.view.ViewGroup))and [android.widget.ExpandableListAdapter#getChildView(int, int, boolean, View, ViewGroup)](https://developer.android.com/reference/kotlin/android/widget/ExpandableListAdapter#getChildView(kotlin.Int,%20kotlin.Int,%20kotlin.Boolean,%20android.view.View,%20android.view.ViewGroup))will be of the appropriate group or child type, resulting in a more efficient reuse of the previously created views.

## Summary

| Public methods ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getChildType](https://developer.android.com/reference/kotlin/android/widget/HeterogeneousExpandableList#getChildType(kotlin.Int,%20kotlin.Int))`(`groupPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `childPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Get the type of child View that will be created by [android.widget.ExpandableListAdapter#getChildView(int, int, boolean, View, ViewGroup)](https://developer.android.com/reference/kotlin/android/widget/ExpandableListAdapter#getChildView(kotlin.Int,%20kotlin.Int,%20kotlin.Boolean,%20android.view.View,%20android.view.ViewGroup))for the specified child item. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getChildTypeCount](https://developer.android.com/reference/kotlin/android/widget/HeterogeneousExpandableList#getChildTypeCount())`()` Returns the number of types of child Views that will be created by [android.widget.ExpandableListAdapter#getChildView(int, int, boolean, View, ViewGroup)](https://developer.android.com/reference/kotlin/android/widget/ExpandableListAdapter#getChildView(kotlin.Int,%20kotlin.Int,%20kotlin.Boolean,%20android.view.View,%20android.view.ViewGroup)). |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getGroupType](https://developer.android.com/reference/kotlin/android/widget/HeterogeneousExpandableList#getGroupType(kotlin.Int))`(`groupPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Get the type of group View that will be created by [android.widget.ExpandableListAdapter#getGroupView(int, boolean, View, ViewGroup)](https://developer.android.com/reference/kotlin/android/widget/ExpandableListAdapter#getGroupView(kotlin.Int,%20kotlin.Boolean,%20android.view.View,%20android.view.ViewGroup)). |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getGroupTypeCount](https://developer.android.com/reference/kotlin/android/widget/HeterogeneousExpandableList#getGroupTypeCount())`()` Returns the number of types of group Views that will be created by [android.widget.ExpandableListAdapter#getGroupView(int, boolean, View, ViewGroup)](https://developer.android.com/reference/kotlin/android/widget/ExpandableListAdapter#getGroupView(kotlin.Int,%20kotlin.Boolean,%20android.view.View,%20android.view.ViewGroup)). |

## Public methods

### getChildType

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getChildType(
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
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | An integer representing the type of child View. Two child views should share the same type if one can be converted to the other in [android.widget.ExpandableListAdapter#getChildView(int, int, boolean, View, ViewGroup)](https://developer.android.com/reference/kotlin/android/widget/ExpandableListAdapter#getChildView(kotlin.Int,%20kotlin.Int,%20kotlin.Boolean,%20android.view.View,%20android.view.ViewGroup))Note: Integers must be in the range 0 to [getChildTypeCount](https://developer.android.com/reference/kotlin/android/widget/HeterogeneousExpandableList#getChildTypeCount())- 1. [android.widget.Adapter#IGNORE_ITEM_VIEW_TYPE](https://developer.android.com/reference/kotlin/android/widget/Adapter#IGNORE_ITEM_VIEW_TYPE:kotlin.Int) can also be returned. |

**See Also**

- [android.widget.Adapter#IGNORE_ITEM_VIEW_TYPE](https://developer.android.com/reference/kotlin/android/widget/Adapter#IGNORE_ITEM_VIEW_TYPE:kotlin.Int)
- <https://developer.android.com/reference/kotlin/android/widget/HeterogeneousExpandableList#getChildTypeCount()> 

### getChildTypeCount

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getChildTypeCount(): Int
```

Returns the number of types of child Views that will be created by [android.widget.ExpandableListAdapter#getChildView(int, int, boolean, View, ViewGroup)](https://developer.android.com/reference/kotlin/android/widget/ExpandableListAdapter#getChildView(kotlin.Int,%20kotlin.Int,%20kotlin.Boolean,%20android.view.View,%20android.view.ViewGroup)). Each type represents a set of views that can be converted in [android.widget.ExpandableListAdapter#getChildView(int, int, boolean, View, ViewGroup)](https://developer.android.com/reference/kotlin/android/widget/ExpandableListAdapter#getChildView(kotlin.Int,%20kotlin.Int,%20kotlin.Boolean,%20android.view.View,%20android.view.ViewGroup)), for any group. If the adapter always returns the same type of View for all child items, this method should return 1.
This method will only be called when the adapter is set on the [AdapterView](https://developer.android.com/reference/kotlin/android/widget/AdapterView).

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The total number of types of child Views that will be created by this adapter. |

**See Also**

- <https://developer.android.com/reference/kotlin/android/widget/HeterogeneousExpandableList#getGroupTypeCount()>
- [#getChildType(int, int)](https://developer.android.com/reference/kotlin/android/widget/HeterogeneousExpandableList#getChildType(kotlin.Int,%20kotlin.Int)) 

### getGroupType

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getGroupType(groupPosition: Int): Int
```

Get the type of group View that will be created by [android.widget.ExpandableListAdapter#getGroupView(int, boolean, View, ViewGroup)](https://developer.android.com/reference/kotlin/android/widget/ExpandableListAdapter#getGroupView(kotlin.Int,%20kotlin.Boolean,%20android.view.View,%20android.view.ViewGroup)). for the specified group item.

| Parameters ||
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| `groupPosition` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the position of the group for which the type should be returned. |

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | An integer representing the type of group View. Two group views should share the same type if one can be converted to the other in [android.widget.ExpandableListAdapter#getGroupView(int, boolean, View, ViewGroup)](https://developer.android.com/reference/kotlin/android/widget/ExpandableListAdapter#getGroupView(kotlin.Int,%20kotlin.Boolean,%20android.view.View,%20android.view.ViewGroup)). Note: Integers must be in the range 0 to [getGroupTypeCount](https://developer.android.com/reference/kotlin/android/widget/HeterogeneousExpandableList#getGroupTypeCount())- 1. [android.widget.Adapter#IGNORE_ITEM_VIEW_TYPE](https://developer.android.com/reference/kotlin/android/widget/Adapter#IGNORE_ITEM_VIEW_TYPE:kotlin.Int) can also be returned. |

**See Also**

- [android.widget.Adapter#IGNORE_ITEM_VIEW_TYPE](https://developer.android.com/reference/kotlin/android/widget/Adapter#IGNORE_ITEM_VIEW_TYPE:kotlin.Int)
- <https://developer.android.com/reference/kotlin/android/widget/HeterogeneousExpandableList#getGroupTypeCount()> 

### getGroupTypeCount

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getGroupTypeCount(): Int
```

Returns the number of types of group Views that will be created by [android.widget.ExpandableListAdapter#getGroupView(int, boolean, View, ViewGroup)](https://developer.android.com/reference/kotlin/android/widget/ExpandableListAdapter#getGroupView(kotlin.Int,%20kotlin.Boolean,%20android.view.View,%20android.view.ViewGroup)). Each type represents a set of views that can be converted in [android.widget.ExpandableListAdapter#getGroupView(int, boolean, View, ViewGroup)](https://developer.android.com/reference/kotlin/android/widget/ExpandableListAdapter#getGroupView(kotlin.Int,%20kotlin.Boolean,%20android.view.View,%20android.view.ViewGroup)). If the adapter always returns the same type of View for all group items, this method should return 1.
This method will only be called when the adapter is set on the [AdapterView](https://developer.android.com/reference/kotlin/android/widget/AdapterView).

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The number of types of group Views that will be created by this adapter. |

**See Also**

- <https://developer.android.com/reference/kotlin/android/widget/HeterogeneousExpandableList#getChildTypeCount()>
- [#getGroupType(int)](https://developer.android.com/reference/kotlin/android/widget/HeterogeneousExpandableList#getGroupType(kotlin.Int))
