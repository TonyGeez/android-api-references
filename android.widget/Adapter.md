# Adapter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Adapter

Kotlin | [Java](Adapter.md) 
| --- | --- |

```
interface Adapter
```

| [android.widget.Adapter](Adapter.md) |

| Known Direct Subclasses [ListAdapter](ListAdapter.md), [SpinnerAdapter](SpinnerAdapter.md) |------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [ListAdapter](ListAdapter.md) | Extended [Adapter](Adapter.md) that is the bridge between a [ListView](ListView.md) and the data that backs the list. | | [SpinnerAdapter](SpinnerAdapter.md) | Extended [Adapter](Adapter.md) that is the bridge between a [android.widget.Spinner](Spinner.md) and its data. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [ArrayAdapter](ArrayAdapter.md), [ArrayAdapter](ArrayAdapter.md), [ArrayAdapter](ArrayAdapter.md), [BaseAdapter](BaseAdapter.md), [BaseAdapter](BaseAdapter.md), [CursorAdapter](CursorAdapter.md), [CursorAdapter](CursorAdapter.md), [CursorAdapter](CursorAdapter.md), [HeaderViewListAdapter](HeaderViewListAdapter.md), [ResourceCursorAdapter](ResourceCursorAdapter.md), [ResourceCursorAdapter](ResourceCursorAdapter.md), [ResourceCursorAdapter](ResourceCursorAdapter.md), and 8 others. |--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [ArrayAdapter](ArrayAdapter.md) | You can use this adapter to provide views for an [AdapterView](AdapterView.md), Returns a view for each object in a collection of data objects you provide, and can be used with list-based user interface widgets such as [ListView](ListView.md) or [Spinner](Spinner.md). | | [ArrayAdapter](ArrayAdapter.md) | You can use this adapter to provide views for an [AdapterView](AdapterView.md), Returns a view for each object in a collection of data objects you provide, and can be used with list-based user interface widgets such as [ListView](ListView.md) or [Spinner](Spinner.md). | | [ArrayAdapter](ArrayAdapter.md) | You can use this adapter to provide views for an [AdapterView](AdapterView.md), Returns a view for each object in a collection of data objects you provide, and can be used with list-based user interface widgets such as [ListView](ListView.md) or [Spinner](Spinner.md). | | [BaseAdapter](BaseAdapter.md) | Common base class of common implementation for an [Adapter](Adapter.md) that can be used in both [ListView](ListView.md) (by implementing the specialized [ListAdapter](ListAdapter.md) interface) and [Spinner](Spinner.md) (by implementing the specialized [SpinnerAdapter](SpinnerAdapter.md) interface). | | [BaseAdapter](BaseAdapter.md) | Common base class of common implementation for an [Adapter](Adapter.md) that can be used in both [ListView](ListView.md) (by implementing the specialized [ListAdapter](ListAdapter.md) interface) and [Spinner](Spinner.md) (by implementing the specialized [SpinnerAdapter](SpinnerAdapter.md) interface). | | [CursorAdapter](CursorAdapter.md) | Adapter that exposes data from a [Cursor](../android.database/Cursor.md) to a [ListView](ListView.md) widget. | | [CursorAdapter](CursorAdapter.md) | Adapter that exposes data from a [Cursor](../android.database/Cursor.md) to a [ListView](ListView.md) widget. | | [CursorAdapter](CursorAdapter.md) | Adapter that exposes data from a [Cursor](../android.database/Cursor.md) to a [ListView](ListView.md) widget. | | [HeaderViewListAdapter](HeaderViewListAdapter.md) | ListAdapter used when a ListView has header views. | | [ResourceCursorAdapter](ResourceCursorAdapter.md) | An easy adapter that creates views defined in an XML file. | | [ResourceCursorAdapter](ResourceCursorAdapter.md) | An easy adapter that creates views defined in an XML file. | | [ResourceCursorAdapter](ResourceCursorAdapter.md) | An easy adapter that creates views defined in an XML file. | | [SimpleAdapter](SimpleAdapter.md) | An easy adapter to map static data to views defined in an XML file. | | [SimpleAdapter](SimpleAdapter.md) | An easy adapter to map static data to views defined in an XML file. | | [SimpleAdapter](SimpleAdapter.md) | An easy adapter to map static data to views defined in an XML file. | | [SimpleCursorAdapter](SimpleCursorAdapter.md) | An easy adapter to map columns from a cursor to TextViews or ImageViews defined in an XML file. | | [SimpleCursorAdapter](SimpleCursorAdapter.md) | An easy adapter to map columns from a cursor to TextViews or ImageViews defined in an XML file. | | [SimpleCursorAdapter](SimpleCursorAdapter.md) | An easy adapter to map columns from a cursor to TextViews or ImageViews defined in an XML file. | | [ThemedSpinnerAdapter](ThemedSpinnerAdapter.md) | An extension of SpinnerAdapter that is capable of inflating drop-down views against a different theme than normal views. | | [WrapperListAdapter](WrapperListAdapter.md) | List adapter that wraps another list adapter. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

An Adapter object acts as a bridge between an [AdapterView](AdapterView.md) and the underlying data for that view. The Adapter provides access to the data items. The Adapter is also responsible for making a [android.view.View](../android.view/View.md) for each item in the data set.

## Summary

| Constants ||
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [IGNORE_ITEM_VIEW_TYPE](Adapter.md) An item view type that causes the [AdapterView](AdapterView.md) to ignore the item view. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [NO_SELECTION](Adapter.md) <br /> |

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!\>? | [getAutofillOptions](Adapter.md))`()` Gets a string representation of the adapter data that can help [android.service.autofill.AutofillService](../android.service.autofill/AutofillService.md) autofill the view backed by the adapter. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getCount](Adapter.md))`()` How many items are in the data set represented by this Adapter. |
| abstract [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getItem](Adapter.md))`(`position:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Get the data item associated with the specified position in the data set. |
| --- | --- |
| abstract [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getItemId](Adapter.md))`(`position:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Get the row id associated with the specified position in the list. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getItemViewType](Adapter.md))`(`position:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Get the type of View that will be created by [getView](Adapter.md)) for the specified item. |
| abstract [View](../android.view/View.md)! | [getView](Adapter.md))`(`position:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `convertView:` ` [View](../android.view/View.md)!`, `parent:` ` [ViewGroup](../android.view/ViewGroup.md)!`)` Get a View that displays the data at the specified position in the data set. |
| --- | --- |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getViewTypeCount](Adapter.md))`()` Returns the number of types of Views that will be created by [getView](Adapter.md)). |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasStableIds](Adapter.md))`()` Indicates whether the item ids are stable across changes to the underlying data. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEmpty](Adapter.md))`()` <br /> |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerDataSetObserver](Adapter.md))`(`observer:` ` [DataSetObserver](../android.database/DataSetObserver.md)!`)` Register an observer that is called when changes happen to the data used by this adapter. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unregisterDataSetObserver](Adapter.md))`(`observer:` ` [DataSetObserver](../android.database/DataSetObserver.md)!`)` Unregister an observer that has previously been registered with this adapter via [registerDataSetObserver](Adapter.md)). |

## Constants

### IGNORE_ITEM_VIEW_TYPE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val IGNORE_ITEM_VIEW_TYPE: Int
```

An item view type that causes the [AdapterView](AdapterView.md) to ignore the item view. For example, this can be used if the client does not want a particular view to be given for conversion in [getView(int,android.view.View,android.view.ViewGroup)](Adapter.md)). 

 Value: -1

**See Also**

- [#getItemViewType(int)](Adapter.md))
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

Gets a string representation of the adapter data that can help [android.service.autofill.AutofillService](../android.service.autofill/AutofillService.md) autofill the view backed by the adapter.

It should only be set (i.e., non-`null` if the values do not represent PII (Personally Identifiable Information - sensitive data such as email addresses, credit card numbers, passwords, etc...). For example, it's ok to return a list of month names, but not a list of usernames. A good rule of thumb is that if the adapter data comes from static resources, such data is not PII - see [android.view.ViewStructure#setDataIsSensitive(boolean)](../android.view/ViewStructure.md)) for more info.

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

Get the type of View that will be created by [getView](Adapter.md)) for the specified item.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `position` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The position of the item within the adapter's data set whose view type we want. |

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | An integer representing the type of View. Two views should share the same type if one can be converted to the other in [getView](Adapter.md)). Note: Integers must be in the range 0 to [getViewTypeCount](Adapter.md)) - 1. [IGNORE_ITEM_VIEW_TYPE](Adapter.md) can also be returned. |

**See Also**

- [#IGNORE_ITEM_VIEW_TYPE](Adapter.md) 

### getView

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getView(
    position: Int, 
    convertView: View!, 
    parent: ViewGroup!
): View!
```

Get a View that displays the data at the specified position in the data set. You can either create a View manually or inflate it from an XML layout file. When the View is inflated, the parent View (GridView, ListView...) will apply default layout parameters unless you use [android.view.LayoutInflater#inflate(int, android.view.ViewGroup, boolean)](../android.view/LayoutInflater.md)) to specify a root view and to prevent attachment to the root.

| Parameters ||
|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `position` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The position of the item within the adapter's data set of the item whose view we want. |
| `convertView` | [View](../android.view/View.md)!: The old view to reuse, if possible. Note: You should check that this view is non-null and of an appropriate type before using. If it is not possible to convert this view to display the correct data, this method can create a new view. Heterogeneous lists can specify their number of view types, so that this View is always of the right type (see [getViewTypeCount()](Adapter.md)) and [getItemViewType(int)](Adapter.md))). |
| `parent` | [ViewGroup](../android.view/ViewGroup.md)!: The parent that this view will eventually be attached to |
| --- | --- |

| Return ||
|---------------------------------------------------------------------------------|-------------------------------------------------------------|
| [View](../android.view/View.md)! | A View corresponding to the data at the specified position. |

### getViewTypeCount

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getViewTypeCount(): Int
```

Returns the number of types of Views that will be created by [getView](Adapter.md)). Each type represents a set of views that can be converted in [getView](Adapter.md)). If the adapter always returns the same type of View for all items, this method should return 1.

This method will only be called when the adapter is set on the [AdapterView](AdapterView.md).

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
| `observer` | [DataSetObserver](../android.database/DataSetObserver.md)!: the object that gets notified when the data set changes. |

### unregisterDataSetObserver

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun unregisterDataSetObserver(observer: DataSetObserver!): Unit
```

Unregister an observer that has previously been registered with this adapter via [registerDataSetObserver](Adapter.md)).

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------|
| `observer` | [DataSetObserver](../android.database/DataSetObserver.md)!: the object to unregister. |
