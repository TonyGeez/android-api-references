# Adapter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Adapter

Kotlin | [Java](https://developer.android.com/reference/android/widget/Adapter "View this page in Java") 

```
interface Adapter
```

| [android.widget.Adapter](https://developer.android.com/reference/kotlin/android/widget/Adapter#) |

| Known Direct Subclasses [ListAdapter](https://developer.android.com/reference/kotlin/android/widget/ListAdapter), [SpinnerAdapter](https://developer.android.com/reference/kotlin/android/widget/SpinnerAdapter) |------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [ListAdapter](https://developer.android.com/reference/kotlin/android/widget/ListAdapter) | Extended [Adapter](https://developer.android.com/reference/kotlin/android/widget/Adapter#) that is the bridge between a [ListView](https://developer.android.com/reference/kotlin/android/widget/ListView) and the data that backs the list. | | [SpinnerAdapter](https://developer.android.com/reference/kotlin/android/widget/SpinnerAdapter) | Extended [Adapter](https://developer.android.com/reference/kotlin/android/widget/Adapter#) that is the bridge between a [android.widget.Spinner](https://developer.android.com/reference/kotlin/android/widget/Spinner) and its data. | |

| Known Indirect Subclasses [ArrayAdapter](https://developer.android.com/reference/kotlin/android/widget/ArrayAdapter), [ArrayAdapter](https://developer.android.com/reference/kotlin/android/widget/ArrayAdapter), [ArrayAdapter](https://developer.android.com/reference/kotlin/android/widget/ArrayAdapter), [BaseAdapter](https://developer.android.com/reference/kotlin/android/widget/BaseAdapter), [BaseAdapter](https://developer.android.com/reference/kotlin/android/widget/BaseAdapter), [CursorAdapter](https://developer.android.com/reference/kotlin/android/widget/CursorAdapter), [CursorAdapter](https://developer.android.com/reference/kotlin/android/widget/CursorAdapter), [CursorAdapter](https://developer.android.com/reference/kotlin/android/widget/CursorAdapter), [HeaderViewListAdapter](https://developer.android.com/reference/kotlin/android/widget/HeaderViewListAdapter), [ResourceCursorAdapter](https://developer.android.com/reference/kotlin/android/widget/ResourceCursorAdapter), [ResourceCursorAdapter](https://developer.android.com/reference/kotlin/android/widget/ResourceCursorAdapter), [ResourceCursorAdapter](https://developer.android.com/reference/kotlin/android/widget/ResourceCursorAdapter), and 8 others. |--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [ArrayAdapter](https://developer.android.com/reference/kotlin/android/widget/ArrayAdapter) | You can use this adapter to provide views for an [AdapterView](https://developer.android.com/reference/kotlin/android/widget/AdapterView), Returns a view for each object in a collection of data objects you provide, and can be used with list-based user interface widgets such as [ListView](https://developer.android.com/reference/kotlin/android/widget/ListView) or [Spinner](https://developer.android.com/reference/kotlin/android/widget/Spinner). | | [ArrayAdapter](https://developer.android.com/reference/kotlin/android/widget/ArrayAdapter) | You can use this adapter to provide views for an [AdapterView](https://developer.android.com/reference/kotlin/android/widget/AdapterView), Returns a view for each object in a collection of data objects you provide, and can be used with list-based user interface widgets such as [ListView](https://developer.android.com/reference/kotlin/android/widget/ListView) or [Spinner](https://developer.android.com/reference/kotlin/android/widget/Spinner). | | [ArrayAdapter](https://developer.android.com/reference/kotlin/android/widget/ArrayAdapter) | You can use this adapter to provide views for an [AdapterView](https://developer.android.com/reference/kotlin/android/widget/AdapterView), Returns a view for each object in a collection of data objects you provide, and can be used with list-based user interface widgets such as [ListView](https://developer.android.com/reference/kotlin/android/widget/ListView) or [Spinner](https://developer.android.com/reference/kotlin/android/widget/Spinner). | | [BaseAdapter](https://developer.android.com/reference/kotlin/android/widget/BaseAdapter) | Common base class of common implementation for an [Adapter](https://developer.android.com/reference/kotlin/android/widget/Adapter#) that can be used in both [ListView](https://developer.android.com/reference/kotlin/android/widget/ListView) (by implementing the specialized [ListAdapter](https://developer.android.com/reference/kotlin/android/widget/ListAdapter) interface) and [Spinner](https://developer.android.com/reference/kotlin/android/widget/Spinner) (by implementing the specialized [SpinnerAdapter](https://developer.android.com/reference/kotlin/android/widget/SpinnerAdapter) interface). | | [BaseAdapter](https://developer.android.com/reference/kotlin/android/widget/BaseAdapter) | Common base class of common implementation for an [Adapter](https://developer.android.com/reference/kotlin/android/widget/Adapter#) that can be used in both [ListView](https://developer.android.com/reference/kotlin/android/widget/ListView) (by implementing the specialized [ListAdapter](https://developer.android.com/reference/kotlin/android/widget/ListAdapter) interface) and [Spinner](https://developer.android.com/reference/kotlin/android/widget/Spinner) (by implementing the specialized [SpinnerAdapter](https://developer.android.com/reference/kotlin/android/widget/SpinnerAdapter) interface). | | [CursorAdapter](https://developer.android.com/reference/kotlin/android/widget/CursorAdapter) | Adapter that exposes data from a [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#) to a [ListView](https://developer.android.com/reference/kotlin/android/widget/ListView) widget. | | [CursorAdapter](https://developer.android.com/reference/kotlin/android/widget/CursorAdapter) | Adapter that exposes data from a [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#) to a [ListView](https://developer.android.com/reference/kotlin/android/widget/ListView) widget. | | [CursorAdapter](https://developer.android.com/reference/kotlin/android/widget/CursorAdapter) | Adapter that exposes data from a [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#) to a [ListView](https://developer.android.com/reference/kotlin/android/widget/ListView) widget. | | [HeaderViewListAdapter](https://developer.android.com/reference/kotlin/android/widget/HeaderViewListAdapter) | ListAdapter used when a ListView has header views. | | [ResourceCursorAdapter](https://developer.android.com/reference/kotlin/android/widget/ResourceCursorAdapter) | An easy adapter that creates views defined in an XML file. | | [ResourceCursorAdapter](https://developer.android.com/reference/kotlin/android/widget/ResourceCursorAdapter) | An easy adapter that creates views defined in an XML file. | | [ResourceCursorAdapter](https://developer.android.com/reference/kotlin/android/widget/ResourceCursorAdapter) | An easy adapter that creates views defined in an XML file. | | [SimpleAdapter](https://developer.android.com/reference/kotlin/android/widget/SimpleAdapter) | An easy adapter to map static data to views defined in an XML file. | | [SimpleAdapter](https://developer.android.com/reference/kotlin/android/widget/SimpleAdapter) | An easy adapter to map static data to views defined in an XML file. | | [SimpleAdapter](https://developer.android.com/reference/kotlin/android/widget/SimpleAdapter) | An easy adapter to map static data to views defined in an XML file. | | [SimpleCursorAdapter](https://developer.android.com/reference/kotlin/android/widget/SimpleCursorAdapter) | An easy adapter to map columns from a cursor to TextViews or ImageViews defined in an XML file. | | [SimpleCursorAdapter](https://developer.android.com/reference/kotlin/android/widget/SimpleCursorAdapter) | An easy adapter to map columns from a cursor to TextViews or ImageViews defined in an XML file. | | [SimpleCursorAdapter](https://developer.android.com/reference/kotlin/android/widget/SimpleCursorAdapter) | An easy adapter to map columns from a cursor to TextViews or ImageViews defined in an XML file. | | [ThemedSpinnerAdapter](https://developer.android.com/reference/kotlin/android/widget/ThemedSpinnerAdapter) | An extension of SpinnerAdapter that is capable of inflating drop-down views against a different theme than normal views. | | [WrapperListAdapter](https://developer.android.com/reference/kotlin/android/widget/WrapperListAdapter) | List adapter that wraps another list adapter. | |

An Adapter object acts as a bridge between an [AdapterView](https://developer.android.com/reference/kotlin/android/widget/AdapterView) and the underlying data for that view. The Adapter provides access to the data items. The Adapter is also responsible for making a [android.view.View](https://developer.android.com/reference/kotlin/android/view/View.html#) for each item in the data set.

## Summary

| Constants ||
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [IGNORE_ITEM_VIEW_TYPE](https://developer.android.com/reference/kotlin/android/widget/Adapter#IGNORE_ITEM_VIEW_TYPE:kotlin.Int) An item view type that causes the [AdapterView](https://developer.android.com/reference/kotlin/android/widget/AdapterView) to ignore the item view. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [NO_SELECTION](https://developer.android.com/reference/kotlin/android/widget/Adapter#NO_SELECTION:kotlin.Int) <br /> |

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!\>? | [getAutofillOptions](https://developer.android.com/reference/kotlin/android/widget/Adapter#getAutofillOptions())`()` Gets a string representation of the adapter data that can help [android.service.autofill.AutofillService](https://developer.android.com/reference/kotlin/android/service/autofill/AutofillService.html#) autofill the view backed by the adapter. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getCount](https://developer.android.com/reference/kotlin/android/widget/Adapter#getCount())`()` How many items are in the data set represented by this Adapter. |
| abstract [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getItem](https://developer.android.com/reference/kotlin/android/widget/Adapter#getItem(kotlin.Int))`(`position:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Get the data item associated with the specified position in the data set. |
| abstract [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getItemId](https://developer.android.com/reference/kotlin/android/widget/Adapter#getItemId(kotlin.Int))`(`position:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Get the row id associated with the specified position in the list. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getItemViewType](https://developer.android.com/reference/kotlin/android/widget/Adapter#getItemViewType(kotlin.Int))`(`position:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Get the type of View that will be created by [getView](https://developer.android.com/reference/kotlin/android/widget/Adapter#getView(kotlin.Int,%20android.view.View,%20android.view.ViewGroup)) for the specified item. |
| abstract [View](https://developer.android.com/reference/kotlin/android/view/View.html#)! | [getView](https://developer.android.com/reference/kotlin/android/widget/Adapter#getView(kotlin.Int,%20android.view.View,%20android.view.ViewGroup))`(`position:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `convertView:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!`, `parent:` ` [ViewGroup](https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#)!`)` Get a View that displays the data at the specified position in the data set. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getViewTypeCount](https://developer.android.com/reference/kotlin/android/widget/Adapter#getViewTypeCount())`()` Returns the number of types of Views that will be created by [getView](https://developer.android.com/reference/kotlin/android/widget/Adapter#getView(kotlin.Int,%20android.view.View,%20android.view.ViewGroup)). |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasStableIds](https://developer.android.com/reference/kotlin/android/widget/Adapter#hasStableIds())`()` Indicates whether the item ids are stable across changes to the underlying data. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEmpty](https://developer.android.com/reference/kotlin/android/widget/Adapter#isEmpty())`()` <br /> |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerDataSetObserver](https://developer.android.com/reference/kotlin/android/widget/Adapter#registerDataSetObserver(android.database.DataSetObserver))`(`observer:` ` [DataSetObserver](https://developer.android.com/reference/kotlin/android/database/DataSetObserver.html#)!`)` Register an observer that is called when changes happen to the data used by this adapter. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unregisterDataSetObserver](https://developer.android.com/reference/kotlin/android/widget/Adapter#unregisterDataSetObserver(android.database.DataSetObserver))`(`observer:` ` [DataSetObserver](https://developer.android.com/reference/kotlin/android/database/DataSetObserver.html#)!`)` Unregister an observer that has previously been registered with this adapter via [registerDataSetObserver](https://developer.android.com/reference/kotlin/android/widget/Adapter#registerDataSetObserver(android.database.DataSetObserver)). |

## Constants

### IGNORE_ITEM_VIEW_TYPE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val IGNORE_ITEM_VIEW_TYPE: Int
```

An item view type that causes the [AdapterView](https://developer.android.com/reference/kotlin/android/widget/AdapterView) to ignore the item view. For example, this can be used if the client does not want a particular view to be given for conversion in [getView(int,android.view.View,android.view.ViewGroup)](https://developer.android.com/reference/kotlin/android/widget/Adapter#getView(kotlin.Int,%20android.view.View,%20android.view.ViewGroup)). 

 Value: -1

**See Also**

- [#getItemViewType(int)](https://developer.android.com/reference/kotlin/android/widget/Adapter#getItemViewType(kotlin.Int))
- <https://developer.android.com/reference/kotlin/android/widget/Adapter#getViewTypeCount()> 

### NO_SELECTION

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NO_SELECTION: Int
```  

 Value: -2147483648

## Public methods

### getAutofillOptions

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getAutofillOptions(): Array<CharSequence!>?
```

Gets a string representation of the adapter data that can help [android.service.autofill.AutofillService](https://developer.android.com/reference/kotlin/android/service/autofill/AutofillService.html#) autofill the view backed by the adapter.

It should only be set (i.e., non-`null` if the values do not represent PII (Personally Identifiable Information - sensitive data such as email addresses, credit card numbers, passwords, etc...). For example, it's ok to return a list of month names, but not a list of usernames. A good rule of thumb is that if the adapter data comes from static resources, such data is not PII - see [android.view.ViewStructure#setDataIsSensitive(boolean)](https://developer.android.com/reference/kotlin/android/view/ViewStructure.html#setDataIsSensitive(kotlin.Boolean)) for more info.

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!>? | `null` by default, unless implementations override it. |

### getCount

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getCount(): Int
```

How many items are in the data set represented by this Adapter.

| Return ||
|----------------------------------------------------------------------------|-----------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Count of items. |

### getItem

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getItem(position: Int): Any!
```

Get the data item associated with the specified position in the data set.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| `position` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Position of the item whose data we want within the adapter's data set. |

| Return ||
|-----------------------------------------------------------------------------|-------------------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | The data at the specified position. |

### getItemId

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getItemId(position: Int): Long
```

Get the row id associated with the specified position in the list.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `position` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The position of the item within the adapter's data set whose row id we want. |

| Return ||
|------------------------------------------------------------------------------|-----------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | The id of the item at the specified position. |

### getItemViewType

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getItemViewType(position: Int): Int
```

Get the type of View that will be created by [getView](https://developer.android.com/reference/kotlin/android/widget/Adapter#getView(kotlin.Int,%20android.view.View,%20android.view.ViewGroup)) for the specified item.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `position` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The position of the item within the adapter's data set whose view type we want. |

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | An integer representing the type of View. Two views should share the same type if one can be converted to the other in [getView](https://developer.android.com/reference/kotlin/android/widget/Adapter#getView(kotlin.Int,%20android.view.View,%20android.view.ViewGroup)). Note: Integers must be in the range 0 to [getViewTypeCount](https://developer.android.com/reference/kotlin/android/widget/Adapter#getViewTypeCount()) - 1. [IGNORE_ITEM_VIEW_TYPE](https://developer.android.com/reference/kotlin/android/widget/Adapter#IGNORE_ITEM_VIEW_TYPE:kotlin.Int) can also be returned. |

**See Also**

- [#IGNORE_ITEM_VIEW_TYPE](https://developer.android.com/reference/kotlin/android/widget/Adapter#IGNORE_ITEM_VIEW_TYPE:kotlin.Int) 

### getView

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getView(
    position: Int, 
    convertView: View!, 
    parent: ViewGroup!
): View!
```

Get a View that displays the data at the specified position in the data set. You can either create a View manually or inflate it from an XML layout file. When the View is inflated, the parent View (GridView, ListView...) will apply default layout parameters unless you use [android.view.LayoutInflater#inflate(int, android.view.ViewGroup, boolean)](https://developer.android.com/reference/kotlin/android/view/LayoutInflater.html#inflate(kotlin.Int,%20android.view.ViewGroup,%20kotlin.Boolean)) to specify a root view and to prevent attachment to the root.

| Parameters ||
|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `position` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The position of the item within the adapter's data set of the item whose view we want. |
| `convertView` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!: The old view to reuse, if possible. Note: You should check that this view is non-null and of an appropriate type before using. If it is not possible to convert this view to display the correct data, this method can create a new view. Heterogeneous lists can specify their number of view types, so that this View is always of the right type (see [getViewTypeCount()](https://developer.android.com/reference/kotlin/android/widget/Adapter#getViewTypeCount()) and [getItemViewType(int)](https://developer.android.com/reference/kotlin/android/widget/Adapter#getItemViewType(kotlin.Int))). |
| `parent` | [ViewGroup](https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#)!: The parent that this view will eventually be attached to |

| Return ||
|---------------------------------------------------------------------------------|-------------------------------------------------------------|
| [View](https://developer.android.com/reference/kotlin/android/view/View.html#)! | A View corresponding to the data at the specified position. |

### getViewTypeCount

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getViewTypeCount(): Int
```

Returns the number of types of Views that will be created by [getView](https://developer.android.com/reference/kotlin/android/widget/Adapter#getView(kotlin.Int,%20android.view.View,%20android.view.ViewGroup)). Each type represents a set of views that can be converted in [getView](https://developer.android.com/reference/kotlin/android/widget/Adapter#getView(kotlin.Int,%20android.view.View,%20android.view.ViewGroup)). If the adapter always returns the same type of View for all items, this method should return 1.

This method will only be called when the adapter is set on the [AdapterView](https://developer.android.com/reference/kotlin/android/widget/AdapterView).

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The number of types of Views that will be created by this adapter |

### hasStableIds

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun hasStableIds(): Boolean
```

Indicates whether the item ids are stable across changes to the underlying data.

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if the same id always refers to the same object. |

### isEmpty

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isEmpty(): Boolean
```

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if this adapter doesn't contain any data. This is used to determine whether the empty view should be displayed. A typical implementation will return getCount() == 0 but since getCount() includes the headers and footers, specialized adapters might want a different behavior. |

### registerDataSetObserver

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun registerDataSetObserver(observer: DataSetObserver!): Unit
```

Register an observer that is called when changes happen to the data used by this adapter.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `observer` | [DataSetObserver](https://developer.android.com/reference/kotlin/android/database/DataSetObserver.html#)!: the object that gets notified when the data set changes. |

### unregisterDataSetObserver

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun unregisterDataSetObserver(observer: DataSetObserver!): Unit
```

Unregister an observer that has previously been registered with this adapter via [registerDataSetObserver](https://developer.android.com/reference/kotlin/android/widget/Adapter#registerDataSetObserver(android.database.DataSetObserver)).

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------|
| `observer` | [DataSetObserver](https://developer.android.com/reference/kotlin/android/database/DataSetObserver.html#)!: the object to unregister. |
