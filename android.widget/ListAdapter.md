# ListAdapter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ListAdapter

Kotlin| [Java](ListAdapter.md) 
| --- | --- |

```
interface ListAdapter : Adapter
```

| [android.widget.ListAdapter](ListAdapter.md) |

| Known Direct Subclasses [BaseAdapter](BaseAdapter.md), [WrapperListAdapter](WrapperListAdapter.md) |--------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [BaseAdapter](BaseAdapter.md) | Common base class of common implementation for an [Adapter](Adapter.md) that can be used in both [ListView](ListView.md)(by implementing the specialized [ListAdapter](ListAdapter.md) interface) and [Spinner](Spinner.md)(by implementing the specialized [SpinnerAdapter](SpinnerAdapter.md) interface). | | [WrapperListAdapter](WrapperListAdapter.md) | List adapter that wraps another list adapter. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [ArrayAdapter](ArrayAdapter.md), [CursorAdapter](CursorAdapter.md), [HeaderViewListAdapter](HeaderViewListAdapter.md), [ResourceCursorAdapter](ResourceCursorAdapter.md), [SimpleAdapter](SimpleAdapter.md), [SimpleCursorAdapter](SimpleCursorAdapter.md) |--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [ArrayAdapter](ArrayAdapter.md) | You can use this adapter to provide views for an [AdapterView](AdapterView.md), Returns a view for each object in a collection of data objects you provide, and can be used with list-based user interface widgets such as [ListView](ListView.md) or [Spinner](Spinner.md). | | [CursorAdapter](CursorAdapter.md) | Adapter that exposes data from a [Cursor](../android.database/Cursor.md) to a [ListView](ListView.md) widget. | | [HeaderViewListAdapter](HeaderViewListAdapter.md) | ListAdapter used when a ListView has header views. | | [ResourceCursorAdapter](ResourceCursorAdapter.md) | An easy adapter that creates views defined in an XML file. | | [SimpleAdapter](SimpleAdapter.md) | An easy adapter to map static data to views defined in an XML file. | | [SimpleCursorAdapter](SimpleCursorAdapter.md) | An easy adapter to map columns from a cursor to TextViews or ImageViews defined in an XML file. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Extended [Adapter](Adapter.md) that is the bridge between a [ListView](ListView.md) and the data that backs the list. Frequently that data comes from a Cursor, but that is not required. The ListView can display any data provided that it is wrapped in a ListAdapter.

## Summary

| Inherited constants ||
|---|---|
| From class [Adapter](Adapter.md) |----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [IGNORE_ITEM_VIEW_TYPE](Adapter.md) <br /> An item view type that causes the [AdapterView](AdapterView.md) to ignore the item view. For example, this can be used if the client does not want a particular view to be given for conversion in [getView(int,android.view.View,android.view.ViewGroup)](Adapter.md)). <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [NO_SELECTION](Adapter.md) <br /> | ||

| Public methods ||
|--------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [areAllItemsEnabled](ListAdapter.md))`()` Indicates whether all the items in this adapter are enabled. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEnabled](ListAdapter.md))`(`position:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns true if the item at the specified position is not a separator. |

| Inherited functions ||
|---|---|
| From class [Adapter](Adapter.md) |---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!>? | [getAutofillOptions](Adapter.md))`()` <br /> Gets a string representation of the adapter data that can help [android.service.autofill.AutofillService](../android.service.autofill/AutofillService.md) autofill the view backed by the adapter. It should only be set (i.e., non-`null`if the values do not represent PII (Personally Identifiable Information - sensitive data such as email addresses, credit card numbers, passwords, etc...). For example, it's ok to return a list of month names, but not a list of usernames. A good rule of thumb is that if the adapter data comes from static resources, such data is not PII - see [android.view.ViewStructure#setDataIsSensitive(boolean)](../android.view/ViewStructure.md))for more info. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getCount](Adapter.md))`()` <br /> How many items are in the data set represented by this Adapter. <br /> | | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getItem](Adapter.md))`(`position:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Get the data item associated with the specified position in the data set. <br /> | | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getItemId](Adapter.md))`(`position:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Get the row id associated with the specified position in the list. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getItemViewType](Adapter.md))`(`position:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Get the type of View that will be created by [getView](Adapter.md))for the specified item. <br /> | | [View](../android.view/View.md)! | [getView](Adapter.md))`(`position:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `convertView:` ` [View](../android.view/View.md)!`, `parent:` ` [ViewGroup](../android.view/ViewGroup.md)!`)` <br /> Get a View that displays the data at the specified position in the data set. You can either create a View manually or inflate it from an XML layout file. When the View is inflated, the parent View (GridView, ListView...) will apply default layout parameters unless you use [android.view.LayoutInflater#inflate(int, android.view.ViewGroup, boolean)](../android.view/LayoutInflater.md))to specify a root view and to prevent attachment to the root. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getViewTypeCount](Adapter.md))`()` <br /> Returns the number of types of Views that will be created by [getView](Adapter.md)). Each type represents a set of views that can be converted in [getView](Adapter.md)). If the adapter always returns the same type of View for all items, this method should return 1. This method will only be called when the adapter is set on the [AdapterView](AdapterView.md). <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasStableIds](Adapter.md))`()` <br /> Indicates whether the item ids are stable across changes to the underlying data. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEmpty](Adapter.md))`()` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerDataSetObserver](Adapter.md))`(`observer:` ` [DataSetObserver](../android.database/DataSetObserver.md)!`)` <br /> Register an observer that is called when changes happen to the data used by this adapter. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unregisterDataSetObserver](Adapter.md))`(`observer:` ` [DataSetObserver](../android.database/DataSetObserver.md)!`)` <br /> Unregister an observer that has previously been registered with this adapter via [registerDataSetObserver](Adapter.md)). <br /> | ||

## Public methods

### areAllItemsEnabled

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun areAllItemsEnabled(): Boolean
```

Indicates whether all the items in this adapter are enabled. If the value returned by this method changes over time, there is no guarantee it will take effect. If true, it means all items are selectable and clickable (there is no separator.)

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if all items are enabled, false otherwise. |

**See Also**

- [#isEnabled(int)](ListAdapter.md)) 

### isEnabled

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isEnabled(position: Int): Boolean
```

Returns true if the item at the specified position is not a separator. (A separator is a non-selectable, non-clickable item). The result is unspecified if position is invalid. An [ArrayIndexOutOfBoundsException](../java.lang/ArrayIndexOutOfBoundsException.md) should be thrown in that case for fast failure.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------|
| `position` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Index of the item |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if the item is not a separator |

**See Also**

- <https://developer.android.com/reference/kotlin/android/widget/ListAdapter#areAllItemsEnabled()>
