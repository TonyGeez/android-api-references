Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# WrapperListAdapter

Kotlin | [Java](WrapperListAdapter.md)
| --- | --- |

```
interface WrapperListAdapter : ListAdapter
```

| [android.widget.WrapperListAdapter](WrapperListAdapter.md) |

| Known Direct Subclasses [HeaderViewListAdapter](HeaderViewListAdapter.md) |---|---| | [HeaderViewListAdapter](HeaderViewListAdapter.md) | ListAdapter used when a ListView has header views. | |
| --- | --- | --- | --- | --- | --- | --- |

List adapter that wraps another list adapter. The wrapped adapter can be retrieved by calling `https://developer.android.com/reference/kotlin/android/widget/WrapperListAdapter#getWrappedAdapter()`.

## Summary

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/widget/Adapter` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/widget/Adapter#IGNORE_ITEM_VIEW_TYPE:kotlin.Int` An item view type that causes the `https://developer.android.com/reference/kotlin/android/widget/AdapterView` to ignore the item view. For example, this can be used if the client does not want a particular view to be given for conversion in `https://developer.android.com/reference/kotlin/android/widget/Adapter#getView(kotlin.Int,%20android.view.View,%20android.view.ViewGroup)`. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/widget/Adapter#NO_SELECTION:kotlin.Int` <br /> | ||

| Public methods ||
|---|---|
| abstract [ListAdapter](ListAdapter.md)! | `https://developer.android.com/reference/kotlin/android/widget/WrapperListAdapter#getWrappedAdapter()()` Returns the adapter wrapped by this list adapter. |

| Inherited functions ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/widget/ListAdapter` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/widget/ListAdapter#areAllItemsEnabled()()` Indicates whether all the items in this adapter are enabled. If the value returned by this method changes over time, there is no guarantee it will take effect. If true, it means all items are selectable and clickable (there is no separator.) <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/widget/ListAdapter#isEnabled(kotlin.Int)(position: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns true if the item at the specified position is not a separator. (A separator is a non-selectable, non-clickable item). The result is unspecified if position is invalid. An `https://developer.android.com/reference/kotlin/java/lang/ArrayIndexOutOfBoundsException.html#` should be thrown in that case for fast failure. <br /> | ||
| From class `https://developer.android.com/reference/kotlin/android/widget/Adapter` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!>?` | `https://developer.android.com/reference/kotlin/android/widget/Adapter#getAutofillOptions()()` Gets a string representation of the adapter data that can help `https://developer.android.com/reference/kotlin/android/service/autofill/AutofillService.html#` autofill the view backed by the adapter. It should only be set (i.e., non-`null` if the values do not represent PII (Personally Identifiable Information - sensitive data such as email addresses, credit card numbers, passwords, etc...). For example, it's ok to return a list of month names, but not a list of usernames. A good rule of thumb is that if the adapter data comes from static resources, such data is not PII - see `https://developer.android.com/reference/kotlin/android/view/ViewStructure.html#setDataIsSensitive(kotlin.Boolean)` for more info. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/widget/Adapter#getCount()()` How many items are in the data set represented by this Adapter. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!` | `https://developer.android.com/reference/kotlin/android/widget/Adapter#getItem(kotlin.Int)(position: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Get the data item associated with the specified position in the data set. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | `https://developer.android.com/reference/kotlin/android/widget/Adapter#getItemId(kotlin.Int)(position: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Get the row id associated with the specified position in the list. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/widget/Adapter#getItemViewType(kotlin.Int)(position: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Get the type of View that will be created by `https://developer.android.com/reference/kotlin/android/widget/Adapter#getView(kotlin.Int,%20android.view.View,%20android.view.ViewGroup)` for the specified item. <br /> | | `https://developer.android.com/reference/kotlin/android/view/View.html#!` | `https://developer.android.com/reference/kotlin/android/widget/Adapter#getView(kotlin.Int,%20android.view.View,%20android.view.ViewGroup)(position: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, convertView: https://developer.android.com/reference/kotlin/android/view/View.html#!, parent: https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#!)` Get a View that displays the data at the specified position in the data set. You can either create a View manually or inflate it from an XML layout file. When the View is inflated, the parent View (GridView, ListView...) will apply default layout parameters unless you use `https://developer.android.com/reference/kotlin/android/view/LayoutInflater.html#inflate(kotlin.Int,%20android.view.ViewGroup,%20kotlin.Boolean)` to specify a root view and to prevent attachment to the root. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/widget/Adapter#getViewTypeCount()()` Returns the number of types of Views that will be created by `https://developer.android.com/reference/kotlin/android/widget/Adapter#getView(kotlin.Int,%20android.view.View,%20android.view.ViewGroup)`. Each type represents a set of views that can be converted in `https://developer.android.com/reference/kotlin/android/widget/Adapter#getView(kotlin.Int,%20android.view.View,%20android.view.ViewGroup)`. If the adapter always returns the same type of View for all items, this method should return 1. This method will only be called when the adapter is set on the `https://developer.android.com/reference/kotlin/android/widget/AdapterView`. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/widget/Adapter#hasStableIds()()` Indicates whether the item ids are stable across changes to the underlying data. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/widget/Adapter#isEmpty()()` <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/widget/Adapter#registerDataSetObserver(android.database.DataSetObserver)(observer: https://developer.android.com/reference/kotlin/android/database/DataSetObserver.html#!)` Register an observer that is called when changes happen to the data used by this adapter. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/widget/Adapter#unregisterDataSetObserver(android.database.DataSetObserver)(observer: https://developer.android.com/reference/kotlin/android/database/DataSetObserver.html#!)` Unregister an observer that has previously been registered with this adapter via `https://developer.android.com/reference/kotlin/android/widget/Adapter#registerDataSetObserver(android.database.DataSetObserver)`. <br /> | ||

## Public methods

### getWrappedAdapter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getWrappedAdapter(): ListAdapter!
```

Returns the adapter wrapped by this list adapter.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/widget/ListAdapter!` | The `https://developer.android.com/reference/kotlin/android/widget/ListAdapter` wrapped by this adapter. |
