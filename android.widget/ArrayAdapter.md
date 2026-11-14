# ArrayAdapter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ArrayAdapter

Kotlin| [Java](../android/widget/ArrayAdapter.md) 
| --- | --- |

```
open class ArrayAdapter<T : Any!> : BaseAdapter, Filterable, ThemedSpinnerAdapter
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.widget.BaseAdapter](../android/widget/BaseAdapter.md) ||
| | ↳ | [android.widget.ArrayAdapter](../android/widget/ArrayAdapter.md) |

You can use this adapter to provide views for an [AdapterView](../android/widget/AdapterView.md), Returns a view for each object in a collection of data objects you provide, and can be used with list-based user interface widgets such as [ListView](../android/widget/ListView.md) or [Spinner](../android/widget/Spinner.md).

By default, the array adapter creates a view by calling [Object.toString()](../java/lang/Object.md))on each data object in the collection you provide, and places the result in a TextView. You may also customize what type of view is used for the data object in the collection. To customize what type of view is used for the data object, override [getView(int,android.view.View,android.view.ViewGroup)](../android/widget/ArrayAdapter.md))and inflate a view resource.

For an example of using an array adapter with a ListView, see the [Adapter Views](https://developer.android.com/guide/topics/ui/declaring-layout.html#AdapterViews) guide.

For an example of using an array adapter with a Spinner, see the [Spinners](https://developer.android.com/guide/topics/ui/controls/spinner.html) guide.

**Note:** If you are considering using array adapter with a ListView, consider using androidx.recyclerview.widget.RecyclerView instead. RecyclerView offers similar features with better performance and more flexibility than ListView provides. See the [Recycler View](https://developer.android.com/guide/topics/ui/layout/recyclerview.html) guide.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ArrayAdapter](../android/widget/ArrayAdapter.md))`(`context:` ` [Context](../android/content/Context.md)`, `resource:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Constructor |
| [ArrayAdapter](../android/widget/ArrayAdapter.md))`(`context:` ` [Context](../android/content/Context.md)`, `resource:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `textViewResourceId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Constructor |
| [ArrayAdapter](../android/widget/ArrayAdapter.md))`(`context:` ` [Context](../android/content/Context.md)`, `resource:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `textViewResourceId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `objects:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)<T>`)` Constructor |
| [ArrayAdapter](../android/widget/ArrayAdapter.md))`(`context:` ` [Context](../android/content/Context.md)`, `resource:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `textViewResourceId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `objects:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)<T>`)` Constructor. |
| [ArrayAdapter](../android/widget/ArrayAdapter.md))`(`context:` ` [Context](../android/content/Context.md)`, `resource:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `objects:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)<T>`)` Constructor |
| [ArrayAdapter](../android/widget/ArrayAdapter.md))`(`context:` ` [Context](../android/content/Context.md)`, `resource:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `objects:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)<T>`)` Constructor. |

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [add](../android/widget/ArrayAdapter.md))`(`object:` `T?`)` Adds the specified object at the end of the array. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addAll](../android/widget/ArrayAdapter.md))`(`collection:` ` [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)<out` `T>`)` Adds the specified Collection at the end of the array. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addAll](../android/widget/ArrayAdapter.md))`(`vararg` `items:` `T`)` Adds the specified items at the end of the array. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clear](../android/widget/ArrayAdapter.md))`()` Remove all elements from the list. |
| openstatic [ArrayAdapter](../android/widget/ArrayAdapter.md)\< [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!\> | [createFromResource](../android/widget/ArrayAdapter.md))`(`context:` ` [Context](../android/content/Context.md)`, `textArrayResId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `textViewResId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a new ArrayAdapter from external resources. |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!\>? | [getAutofillOptions](../android/widget/ArrayAdapter.md))`()` Gets a string representation of the adapter data that can help [android.service.autofill.AutofillService](../android/service/autofill/AutofillService.md) autofill the view backed by the adapter. |
| --- | --- |
| open [Context](../android/content/Context.md) | [getContext](../android/widget/ArrayAdapter.md))`()` Returns the context associated with this array adapter. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getCount](../android/widget/ArrayAdapter.md))`()` <br /> |
| open [View](../android/view/View.md)! | [getDropDownView](../android/widget/ArrayAdapter.md))`(`position:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `convertView:` ` [View](../android/view/View.md)?`, `parent:` ` [ViewGroup](../android/view/ViewGroup.md)`)` Gets a [android.view.View](../android/view/View.md) that displays in the drop down popup the data at the specified position in the data set. |
| --- | --- |
| open [Resources.Theme](../android/content/res/Resources.Theme.md)? | [getDropDownViewTheme](../android/widget/ArrayAdapter.md))`()` Returns the value previously set by a call to [setDropDownViewTheme(android.content.res.Resources.Theme)](../android/widget/ThemedSpinnerAdapter.md)). |
| open [Filter](../android/widget/Filter.md) | [getFilter](../android/widget/ArrayAdapter.md))`()` Returns a filter that can be used to constrain data with a filtering pattern. |
| openT? | [getItem](../android/widget/ArrayAdapter.md))`(`position:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Get the data item associated with the specified position in the data set. |
| --- | --- |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getItemId](../android/widget/ArrayAdapter.md))`(`position:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPosition](../android/widget/ArrayAdapter.md))`(`item:` `T?`)` Returns the position of the specified item in the array. |
| open [View](../android/view/View.md) | [getView](../android/widget/ArrayAdapter.md))`(`position:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `convertView:` ` [View](../android/view/View.md)?`, `parent:` ` [ViewGroup](../android/view/ViewGroup.md)`)` Get a View that displays the data at the specified position in the data set. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [insert](../android/widget/ArrayAdapter.md))`(`object:` `T?`, `index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Inserts the specified object at the specified index in the array. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [notifyDataSetChanged](../android/widget/ArrayAdapter.md))`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [remove](../android/widget/ArrayAdapter.md))`(`object:` `T?`)` Removes the specified object from the array. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDropDownViewResource](../android/widget/ArrayAdapter.md))`(`resource:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the layout resource to create the drop down views. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDropDownViewTheme](../android/widget/ArrayAdapter.md))`(`theme:` ` [Resources.Theme](../android/content/res/Resources.Theme.md)?`)` Sets the [Resources.Theme](../android/content/res/Resources.Theme.md) against which drop-down views are inflated. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setNotifyOnChange](../android/widget/ArrayAdapter.md))`(`notifyOnChange:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Control whether methods that change the list ([add](../android/widget/ArrayAdapter.md)), [addAll(java.util.Collection)](../android/widget/ArrayAdapter.md)),[addAll(java.lang.Object[])](https://developer.android.com/reference/kotlin/android/widget/ArrayAdapter#addAll(android.widget.ArrayAdapter.T)), [insert](../android/widget/ArrayAdapter.md)), [remove](../android/widget/ArrayAdapter.md)), [clear](../android/widget/ArrayAdapter.md)), [sort(java.util.Comparator)](../android/widget/ArrayAdapter.md))) automatically call [notifyDataSetChanged](../android/widget/ArrayAdapter.md)). |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [sort](../android/widget/ArrayAdapter.md))`(`comparator:` ` [Comparator](../java/util/Comparator.md)<in` `T>`)` Sorts the content of this adapter using the specified comparator. |

| Inherited functions ||
|---|---|
| From class [BaseAdapter](../android/widget/BaseAdapter.md) |------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [areAllItemsEnabled](../android/widget/BaseAdapter.md))`()` <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getItemViewType](../android/widget/BaseAdapter.md))`(`position:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getViewTypeCount](../android/widget/BaseAdapter.md))`()` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasStableIds](../android/widget/BaseAdapter.md))`()` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEmpty](../android/widget/BaseAdapter.md))`()` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEnabled](../android/widget/BaseAdapter.md))`(`position:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [notifyDataSetInvalidated](../android/widget/BaseAdapter.md))`()` <br /> Notifies the attached observers that the underlying data is no longer valid or available. Once invoked this adapter is no longer valid and should not report further data set changes. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerDataSetObserver](../android/widget/BaseAdapter.md))`(`observer:` ` [DataSetObserver](../android/database/DataSetObserver.md)!`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAutofillOptions](../android/widget/BaseAdapter.md))`(`vararg` `options:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` <br /> Sets the value returned by [getAutofillOptions()](../android/widget/BaseAdapter.md)) <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unregisterDataSetObserver](../android/widget/BaseAdapter.md))`(`observer:` ` [DataSetObserver](../android/database/DataSetObserver.md)!`)` <br /> | ||

## Public constructors

### ArrayAdapter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ArrayAdapter(
    context: Context, 
    resource: Int)
```

Constructor

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android/content/Context.md):The current context. This value cannot be`null`. |
| `resource` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The resource ID for a layout file containing a TextView to use when instantiating views. |

### ArrayAdapter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ArrayAdapter(
    context: Context, 
    resource: Int, 
    textViewResourceId: Int)
```

Constructor

| Parameters ||
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android/content/Context.md):The current context. This value cannot be`null`. |
| `resource` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The resource ID for a layout file containing a layout to use when instantiating views. |
| `textViewResourceId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The id of the TextView within the layout resource to be populated |
| --- | --- |

### ArrayAdapter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ArrayAdapter(
    context: Context, 
    resource: Int, 
    textViewResourceId: Int, 
    objects: MutableList<T>)
```

Constructor

| Parameters ||
|----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android/content/Context.md):The current context. This value cannot be`null`. |
| `resource` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The resource ID for a layout file containing a layout to use when instantiating views. |
| `textViewResourceId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The id of the TextView within the layout resource to be populated |
| --- | --- |
| `objects` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\<T\>:The objects to represent in the ListView. This value cannot be`null`. |

### ArrayAdapter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ArrayAdapter(
    context: Context, 
    resource: Int, 
    textViewResourceId: Int, 
    objects: Array<T>)
```

Constructor. This constructor will result in the underlying data collection being immutable, so methods such as [clear()](../android/widget/ArrayAdapter.md))will throw an exception.

| Parameters ||
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android/content/Context.md):The current context. This value cannot be`null`. |
| `resource` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The resource ID for a layout file containing a layout to use when instantiating views. |
| `textViewResourceId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The id of the TextView within the layout resource to be populated |
| --- | --- |
| `objects` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\<T\>:The objects to represent in the ListView. This value cannot be`null`. |

### ArrayAdapter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ArrayAdapter(
    context: Context, 
    resource: Int, 
    objects: MutableList<T>)
```

Constructor

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android/content/Context.md):The current context. This value cannot be`null`. |
| `resource` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The resource ID for a layout file containing a TextView to use when instantiating views. |
| `objects` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\<T\>:The objects to represent in the ListView. This value cannot be`null`. |
| --- | --- |

### ArrayAdapter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ArrayAdapter(
    context: Context, 
    resource: Int, 
    objects: Array<T>)
```

Constructor. This constructor will result in the underlying data collection being immutable, so methods such as [clear()](../android/widget/ArrayAdapter.md))will throw an exception.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android/content/Context.md):The current context. This value cannot be`null`. |
| `resource` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The resource ID for a layout file containing a TextView to use when instantiating views. |
| `objects` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\<T\>:The objects to represent in the ListView. This value cannot be`null`. |
| --- | --- |

## Public methods

### add

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun add(object: T?): Unit
```

Adds the specified object at the end of the array.

| Parameters ||
|----------|------------------------------------------------------------------------|
| `object` | T?:The object to add at the end of the array. This value may be`null`. |

| Exceptions ||
|-------------------------------------------|------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the underlying data collection is immutable |

### addAll

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun addAll(collection: MutableCollection<out T>): Unit
```

Adds the specified Collection at the end of the array.

| Parameters ||
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `collection` | [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\<outT\>:The Collection to add at the end of the array. This value cannot be`null`. |

| Exceptions ||
|-------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the addAll operation is not supported by this list |
| `java.lang.ClassCastException` | if the class of an element of the specified collection prevents it from being added to this list |
| `java.lang.NullPointerException` | if the specified collection contains one or more null elements and this list does not permit null elements, or if the specified collection is null |
| --- | --- |
| `java.lang.IllegalArgumentException` | if some property of an element of the specified collection prevents it from being added to this list |

### addAll

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun addAll(vararg items: T): Unit
```

Adds the specified items at the end of the array.

| Parameters ||
|---------|---------------------------------------------|
| `items` | T:The items to add at the end of the array. |

| Exceptions ||
|-------------------------------------------|------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the underlying data collection is immutable |

### clear

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun clear(): Unit
```

Remove all elements from the list.

| Exceptions ||
|-------------------------------------------|------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the underlying data collection is immutable |

### createFromResource

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun createFromResource(
    context: Context, 
    textArrayResId: Int, 
    textViewResId: Int
): ArrayAdapter<CharSequence!>
```

Creates a new ArrayAdapter from external resources. The content of the array is obtained through [android.content.res.Resources#getTextArray(int)](../android/content/res/Resources.md)).

| Parameters ||
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android/content/Context.md):The application's environment. This value cannot be`null`. |
| `textArrayResId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The identifier of the array to use as the data source. |
| `textViewResId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The identifier of the layout used to create views. |
| --- | --- |

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| [ArrayAdapter](../android/widget/ArrayAdapter.md)< [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!> | An ArrayAdapter. This value cannot be`null`. |

### getAutofillOptions

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getAutofillOptions(): Array<CharSequence!>?
```

Gets a string representation of the adapter data that can help [android.service.autofill.AutofillService](../android/service/autofill/AutofillService.md) autofill the view backed by the adapter.

It should only be set (i.e., non-`null`if the values do not represent PII (Personally Identifiable Information - sensitive data such as email addresses, credit card numbers, passwords, etc...). For example, it's ok to return a list of month names, but not a list of usernames. A good rule of thumb is that if the adapter data comes from static resources, such data is not PII - see [android.view.ViewStructure#setDataIsSensitive(boolean)](../android/view/ViewStructure.md))for more info.

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!>? | values from the string array used by [createFromResource(android.content.Context,int,int)](../android/widget/ArrayAdapter.md)), or`null`if object was created otherwsie or if contents were dynamically changed after creation. |

### getContext

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getContext(): Context
```

Returns the context associated with this array adapter. The context is used to create views from the resource passed to the constructor.

| Return ||
|-----------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [Context](../android/content/Context.md) | The Context associated with this adapter. This value cannot be`null`. |

### getCount

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getCount(): Int
```

| Return ||
|----------------------------------------------------------------------------|-----------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Count of items. |

### getDropDownView

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDropDownView(
    position: Int, 
    convertView: View?, 
    parent: ViewGroup
): View!
```

Gets a [android.view.View](../android/view/View.md) that displays in the drop down popup the data at the specified position in the data set.

| Parameters ||
|---------------|----------------------------------------------------------------------------------------------------------------------|
| `position` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):index of the item whose view we want. |
| `convertView` | [View](../android/view/View.md)?:This value may be`null`. |
| `parent` | [ViewGroup](../android/view/ViewGroup.md):This value cannot be`null`. |
| --- | --- |

| Return ||
|---------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [View](../android/view/View.md)! | a [android.view.View](../android/view/View.md) corresponding to the data at the specified position. |

### getDropDownViewTheme

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDropDownViewTheme(): Resources.Theme?
```

Returns the value previously set by a call to [setDropDownViewTheme(android.content.res.Resources.Theme)](../android/widget/ThemedSpinnerAdapter.md)).

| Return ||
|--------------------------------------------------------------------------------------------------------------|--------------------------|
| [Resources.Theme](../android/content/res/Resources.Theme.md)? | This value may be`null`. |

### getFilter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getFilter(): Filter
```

Returns a filter that can be used to constrain data with a filtering pattern.

This method is usually implemented by [android.widget.Adapter](../android/widget/Adapter.md) classes.

| Return ||
|--------------------------------------------------------------------------------|-----------------------------|
| [Filter](../android/widget/Filter.md) | This value cannot be`null`. |

### getItem

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getItem(position: Int): T?
```

Get the data item associated with the specified position in the data set.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| `position` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Position of the item whose data we want within the adapter's data set. |

| Return ||
|----|--------------------------|
| T? | This value may be`null`. |

### getItemId

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getItemId(position: Int): Long
```

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| `position` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The position of the item within the adapter's data set whose row id we want. |

| Return ||
|------------------------------------------------------------------------------|-----------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | The id of the item at the specified position. |

### getPosition

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPosition(item: T?): Int
```

Returns the position of the specified item in the array.

| Parameters ||
|--------|-------------------------------------------------------------------|
| `item` | T?:The item to retrieve the position of. This value may be`null`. |

| Return ||
|----------------------------------------------------------------------------|-------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The position of the specified item. |

### getView

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getView(
    position: Int, 
    convertView: View?, 
    parent: ViewGroup
): View
```

Get a View that displays the data at the specified position in the data set. You can either create a View manually or inflate it from an XML layout file. When the View is inflated, the parent View (GridView, ListView...) will apply default layout parameters unless you use [android.view.LayoutInflater#inflate(int, android.view.ViewGroup, boolean)](../android/view/LayoutInflater.md))to specify a root view and to prevent attachment to the root.

| Parameters ||
|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `position` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The position of the item within the adapter's data set of the item whose view we want. |
| `convertView` | [View](../android/view/View.md)?:This value may be`null`. |
| `parent` | [ViewGroup](../android/view/ViewGroup.md):This value cannot be`null`. |
| --- | --- |

| Return ||
|--------------------------------------------------------------------------------|-----------------------------|
| [View](../android/view/View.md) | This value cannot be`null`. |

### insert

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun insert(
    object: T?, 
    index: Int
): Unit
```

Inserts the specified object at the specified index in the array.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------|
| `object` | T?:The object to insert into the array. This value may be`null`. |
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The index at which the object must be inserted. |

| Exceptions ||
|-------------------------------------------|------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the underlying data collection is immutable |

### notifyDataSetChanged

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun notifyDataSetChanged(): Unit
```  

### remove

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun remove(object: T?): Unit
```

Removes the specified object from the array.

| Parameters ||
|----------|---------------------------------------------------|
| `object` | T?:The object to remove. This value may be`null`. |

| Exceptions ||
|-------------------------------------------|------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the underlying data collection is immutable |

### setDropDownViewResource

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setDropDownViewResource(resource: Int): Unit
```

Sets the layout resource to create the drop down views.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------|
| `resource` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the layout resource defining the drop down views |

**See Also**

- [#getDropDownView(int, android.view.View, android.view.ViewGroup)](../android/widget/ArrayAdapter.md)) 

### setDropDownViewTheme

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setDropDownViewTheme(theme: Resources.Theme?): Unit
```

Sets the [Resources.Theme](../android/content/res/Resources.Theme.md) against which drop-down views are inflated.

By default, drop-down views are inflated against the theme of the [Context](../android/content/Context.md) passed to the adapter's constructor.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `theme` | [Resources.Theme](../android/content/res/Resources.Theme.md)?:the theme against which to inflate drop-down views or`null`to use the theme from the adapter's context |

**See Also**

- [#getDropDownView(int, View, ViewGroup)](../android/widget/ArrayAdapter.md)) 

### setNotifyOnChange

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setNotifyOnChange(notifyOnChange: Boolean): Unit
```

Control whether methods that change the list ([add](../android/widget/ArrayAdapter.md)), [addAll(java.util.Collection)](../android/widget/ArrayAdapter.md)),[addAll(java.lang.Object[])](https://developer.android.com/reference/kotlin/android/widget/ArrayAdapter#addAll(android.widget.ArrayAdapter.T)), [insert](../android/widget/ArrayAdapter.md)), [remove](../android/widget/ArrayAdapter.md)), [clear](../android/widget/ArrayAdapter.md)), [sort(java.util.Comparator)](../android/widget/ArrayAdapter.md))) automatically call [notifyDataSetChanged](../android/widget/ArrayAdapter.md)). If set to false, caller must manually call notifyDataSetChanged() to have the changes reflected in the attached view. The default is true, and calling notifyDataSetChanged() resets the flag to true.

| Parameters ||
|------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `notifyOnChange` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):if true, modifications to the list will automatically call [notifyDataSetChanged](../android/widget/ArrayAdapter.md)) |

### sort

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun sort(comparator: Comparator<in T>): Unit
```

Sorts the content of this adapter using the specified comparator.

| Parameters ||
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `comparator` | [Comparator](../java/util/Comparator.md)\<inT\>:The comparator used to sort the objects contained in this adapter. This value cannot be`null`. |
