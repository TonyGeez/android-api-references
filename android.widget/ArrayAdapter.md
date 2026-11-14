# ArrayAdapter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ArrayAdapter

Kotlin| [Java](https://developer.android.com/reference/android/widget/ArrayAdapter "View this page in Java") 

```
open class ArrayAdapter<T : Any!> : BaseAdapter, Filterable, ThemedSpinnerAdapter
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| ↳ | [android.widget.BaseAdapter](https://developer.android.com/reference/kotlin/android/widget/BaseAdapter) ||
| | ↳ | [android.widget.ArrayAdapter](https://developer.android.com/reference/kotlin/android/widget/ArrayAdapter#) |

You can use this adapter to provide views for an [AdapterView](https://developer.android.com/reference/kotlin/android/widget/AdapterView), Returns a view for each object in a collection of data objects you provide, and can be used with list-based user interface widgets such as [ListView](https://developer.android.com/reference/kotlin/android/widget/ListView) or [Spinner](https://developer.android.com/reference/kotlin/android/widget/Spinner).

By default, the array adapter creates a view by calling [Object.toString()](https://developer.android.com/reference/kotlin/java/lang/Object.html#toString())on each data object in the collection you provide, and places the result in a TextView. You may also customize what type of view is used for the data object in the collection. To customize what type of view is used for the data object, override [getView(int,android.view.View,android.view.ViewGroup)](https://developer.android.com/reference/kotlin/android/widget/ArrayAdapter#getView(kotlin.Int,%20android.view.View,%20android.view.ViewGroup))and inflate a view resource.

For an example of using an array adapter with a ListView, see the [Adapter Views](https://developer.android.com/guide/topics/ui/declaring-layout.html#AdapterViews) guide.

For an example of using an array adapter with a Spinner, see the [Spinners](https://developer.android.com/guide/topics/ui/controls/spinner.html) guide.

**Note:** If you are considering using array adapter with a ListView, consider using androidx.recyclerview.widget.RecyclerView instead. RecyclerView offers similar features with better performance and more flexibility than ListView provides. See the [Recycler View](https://developer.android.com/guide/topics/ui/layout/recyclerview.html) guide.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ArrayAdapter](https://developer.android.com/reference/kotlin/android/widget/ArrayAdapter#ArrayAdapter(android.content.Context,%20kotlin.Int))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)`, `resource:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Constructor |
| [ArrayAdapter](https://developer.android.com/reference/kotlin/android/widget/ArrayAdapter#ArrayAdapter(android.content.Context,%20kotlin.Int,%20kotlin.Int))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)`, `resource:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `textViewResourceId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Constructor |
| [ArrayAdapter](https://developer.android.com/reference/kotlin/android/widget/ArrayAdapter#ArrayAdapter(android.content.Context,%20kotlin.Int,%20kotlin.Int,%20kotlin.collections.MutableList))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)`, `resource:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `textViewResourceId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `objects:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)<T>`)` Constructor |
| [ArrayAdapter](https://developer.android.com/reference/kotlin/android/widget/ArrayAdapter#ArrayAdapter(android.content.Context,%20kotlin.Int,%20kotlin.Int,%20kotlin.Array))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)`, `resource:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `textViewResourceId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `objects:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)<T>`)` Constructor. |
| [ArrayAdapter](https://developer.android.com/reference/kotlin/android/widget/ArrayAdapter#ArrayAdapter(android.content.Context,%20kotlin.Int,%20kotlin.collections.MutableList))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)`, `resource:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `objects:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)<T>`)` Constructor |
| [ArrayAdapter](https://developer.android.com/reference/kotlin/android/widget/ArrayAdapter#ArrayAdapter(android.content.Context,%20kotlin.Int,%20kotlin.Array))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)`, `resource:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `objects:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)<T>`)` Constructor. |

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [add](https://developer.android.com/reference/kotlin/android/widget/ArrayAdapter#add(android.widget.ArrayAdapter.T))`(`object:` `T?`)` Adds the specified object at the end of the array. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addAll](https://developer.android.com/reference/kotlin/android/widget/ArrayAdapter#addAll(kotlin.collections.MutableCollection))`(`collection:` ` [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)<out` `T>`)` Adds the specified Collection at the end of the array. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addAll](https://developer.android.com/reference/kotlin/android/widget/ArrayAdapter#addAll(android.widget.ArrayAdapter.T))`(`vararg` `items:` `T`)` Adds the specified items at the end of the array. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clear](https://developer.android.com/reference/kotlin/android/widget/ArrayAdapter#clear())`()` Remove all elements from the list. |
| openstatic [ArrayAdapter](https://developer.android.com/reference/kotlin/android/widget/ArrayAdapter#)\< [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!\> | [createFromResource](https://developer.android.com/reference/kotlin/android/widget/ArrayAdapter#createFromResource(android.content.Context,%20kotlin.Int,%20kotlin.Int))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)`, `textArrayResId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `textViewResId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a new ArrayAdapter from external resources. |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!\>? | [getAutofillOptions](https://developer.android.com/reference/kotlin/android/widget/ArrayAdapter#getAutofillOptions())`()` Gets a string representation of the adapter data that can help [android.service.autofill.AutofillService](https://developer.android.com/reference/kotlin/android/service/autofill/AutofillService.html#) autofill the view backed by the adapter. |
| open [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#) | [getContext](https://developer.android.com/reference/kotlin/android/widget/ArrayAdapter#getContext())`()` Returns the context associated with this array adapter. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getCount](https://developer.android.com/reference/kotlin/android/widget/ArrayAdapter#getCount())`()` <br /> |
| open [View](https://developer.android.com/reference/kotlin/android/view/View.html#)! | [getDropDownView](https://developer.android.com/reference/kotlin/android/widget/ArrayAdapter#getDropDownView(kotlin.Int,%20android.view.View,%20android.view.ViewGroup))`(`position:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `convertView:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)?`, `parent:` ` [ViewGroup](https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#)`)` Gets a [android.view.View](https://developer.android.com/reference/kotlin/android/view/View.html#) that displays in the drop down popup the data at the specified position in the data set. |
| open [Resources.Theme](https://developer.android.com/reference/kotlin/android/content/res/Resources.Theme.html#)? | [getDropDownViewTheme](https://developer.android.com/reference/kotlin/android/widget/ArrayAdapter#getDropDownViewTheme())`()` Returns the value previously set by a call to [setDropDownViewTheme(android.content.res.Resources.Theme)](https://developer.android.com/reference/kotlin/android/widget/ThemedSpinnerAdapter#setDropDownViewTheme(android.content.res.Resources.Theme)). |
| open [Filter](https://developer.android.com/reference/kotlin/android/widget/Filter) | [getFilter](https://developer.android.com/reference/kotlin/android/widget/ArrayAdapter#getFilter())`()` Returns a filter that can be used to constrain data with a filtering pattern. |
| openT? | [getItem](https://developer.android.com/reference/kotlin/android/widget/ArrayAdapter#getItem(kotlin.Int))`(`position:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Get the data item associated with the specified position in the data set. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getItemId](https://developer.android.com/reference/kotlin/android/widget/ArrayAdapter#getItemId(kotlin.Int))`(`position:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPosition](https://developer.android.com/reference/kotlin/android/widget/ArrayAdapter#getPosition(android.widget.ArrayAdapter.T))`(`item:` `T?`)` Returns the position of the specified item in the array. |
| open [View](https://developer.android.com/reference/kotlin/android/view/View.html#) | [getView](https://developer.android.com/reference/kotlin/android/widget/ArrayAdapter#getView(kotlin.Int,%20android.view.View,%20android.view.ViewGroup))`(`position:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `convertView:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)?`, `parent:` ` [ViewGroup](https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#)`)` Get a View that displays the data at the specified position in the data set. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [insert](https://developer.android.com/reference/kotlin/android/widget/ArrayAdapter#insert(android.widget.ArrayAdapter.T,%20kotlin.Int))`(`object:` `T?`, `index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Inserts the specified object at the specified index in the array. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [notifyDataSetChanged](https://developer.android.com/reference/kotlin/android/widget/ArrayAdapter#notifyDataSetChanged())`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [remove](https://developer.android.com/reference/kotlin/android/widget/ArrayAdapter#remove(android.widget.ArrayAdapter.T))`(`object:` `T?`)` Removes the specified object from the array. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDropDownViewResource](https://developer.android.com/reference/kotlin/android/widget/ArrayAdapter#setDropDownViewResource(kotlin.Int))`(`resource:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the layout resource to create the drop down views. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDropDownViewTheme](https://developer.android.com/reference/kotlin/android/widget/ArrayAdapter#setDropDownViewTheme(android.content.res.Resources.Theme))`(`theme:` ` [Resources.Theme](https://developer.android.com/reference/kotlin/android/content/res/Resources.Theme.html#)?`)` Sets the [Resources.Theme](https://developer.android.com/reference/kotlin/android/content/res/Resources.Theme.html#) against which drop-down views are inflated. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setNotifyOnChange](https://developer.android.com/reference/kotlin/android/widget/ArrayAdapter#setNotifyOnChange(kotlin.Boolean))`(`notifyOnChange:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Control whether methods that change the list ([add](https://developer.android.com/reference/kotlin/android/widget/ArrayAdapter#add(android.widget.ArrayAdapter.T)), [addAll(java.util.Collection)](https://developer.android.com/reference/kotlin/android/widget/ArrayAdapter#addAll(kotlin.collections.MutableCollection)),[addAll(java.lang.Object[])](https://developer.android.com/reference/kotlin/android/widget/ArrayAdapter#addAll(android.widget.ArrayAdapter.T)), [insert](https://developer.android.com/reference/kotlin/android/widget/ArrayAdapter#insert(android.widget.ArrayAdapter.T,%20kotlin.Int)), [remove](https://developer.android.com/reference/kotlin/android/widget/ArrayAdapter#remove(android.widget.ArrayAdapter.T)), [clear](https://developer.android.com/reference/kotlin/android/widget/ArrayAdapter#clear()), [sort(java.util.Comparator)](https://developer.android.com/reference/kotlin/android/widget/ArrayAdapter#sort(java.util.Comparator))) automatically call [notifyDataSetChanged](https://developer.android.com/reference/kotlin/android/widget/ArrayAdapter#notifyDataSetChanged()). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [sort](https://developer.android.com/reference/kotlin/android/widget/ArrayAdapter#sort(java.util.Comparator))`(`comparator:` ` [Comparator](https://developer.android.com/reference/kotlin/java/util/Comparator.html#)<in` `T>`)` Sorts the content of this adapter using the specified comparator. |

| Inherited functions ||
|---|---|
| From class [BaseAdapter](https://developer.android.com/reference/kotlin/android/widget/BaseAdapter) |------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [areAllItemsEnabled](https://developer.android.com/reference/kotlin/android/widget/BaseAdapter#areAllItemsEnabled())`()` <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getItemViewType](https://developer.android.com/reference/kotlin/android/widget/BaseAdapter#getItemViewType(kotlin.Int))`(`position:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getViewTypeCount](https://developer.android.com/reference/kotlin/android/widget/BaseAdapter#getViewTypeCount())`()` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasStableIds](https://developer.android.com/reference/kotlin/android/widget/BaseAdapter#hasStableIds())`()` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEmpty](https://developer.android.com/reference/kotlin/android/widget/BaseAdapter#isEmpty())`()` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEnabled](https://developer.android.com/reference/kotlin/android/widget/BaseAdapter#isEnabled(kotlin.Int))`(`position:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [notifyDataSetInvalidated](https://developer.android.com/reference/kotlin/android/widget/BaseAdapter#notifyDataSetInvalidated())`()` <br /> Notifies the attached observers that the underlying data is no longer valid or available. Once invoked this adapter is no longer valid and should not report further data set changes. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerDataSetObserver](https://developer.android.com/reference/kotlin/android/widget/BaseAdapter#registerDataSetObserver(android.database.DataSetObserver))`(`observer:` ` [DataSetObserver](https://developer.android.com/reference/kotlin/android/database/DataSetObserver.html#)!`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAutofillOptions](https://developer.android.com/reference/kotlin/android/widget/BaseAdapter#setAutofillOptions(kotlin.CharSequence))`(`vararg` `options:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` <br /> Sets the value returned by [getAutofillOptions()](https://developer.android.com/reference/kotlin/android/widget/BaseAdapter#getAutofillOptions()) <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unregisterDataSetObserver](https://developer.android.com/reference/kotlin/android/widget/BaseAdapter#unregisterDataSetObserver(android.database.DataSetObserver))`(`observer:` ` [DataSetObserver](https://developer.android.com/reference/kotlin/android/database/DataSetObserver.html#)!`)` <br /> | ||

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
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#):The current context. This value cannot be`null`. |
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
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#):The current context. This value cannot be`null`. |
| `resource` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The resource ID for a layout file containing a layout to use when instantiating views. |
| `textViewResourceId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The id of the TextView within the layout resource to be populated |

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
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#):The current context. This value cannot be`null`. |
| `resource` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The resource ID for a layout file containing a layout to use when instantiating views. |
| `textViewResourceId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The id of the TextView within the layout resource to be populated |
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

Constructor. This constructor will result in the underlying data collection being immutable, so methods such as [clear()](https://developer.android.com/reference/kotlin/android/widget/ArrayAdapter#clear())will throw an exception.

| Parameters ||
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#):The current context. This value cannot be`null`. |
| `resource` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The resource ID for a layout file containing a layout to use when instantiating views. |
| `textViewResourceId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The id of the TextView within the layout resource to be populated |
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
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#):The current context. This value cannot be`null`. |
| `resource` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The resource ID for a layout file containing a TextView to use when instantiating views. |
| `objects` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\<T\>:The objects to represent in the ListView. This value cannot be`null`. |

### ArrayAdapter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ArrayAdapter(
    context: Context, 
    resource: Int, 
    objects: Array<T>)
```

Constructor. This constructor will result in the underlying data collection being immutable, so methods such as [clear()](https://developer.android.com/reference/kotlin/android/widget/ArrayAdapter#clear())will throw an exception.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#):The current context. This value cannot be`null`. |
| `resource` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The resource ID for a layout file containing a TextView to use when instantiating views. |
| `objects` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\<T\>:The objects to represent in the ListView. This value cannot be`null`. |

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

Creates a new ArrayAdapter from external resources. The content of the array is obtained through [android.content.res.Resources#getTextArray(int)](https://developer.android.com/reference/kotlin/android/content/res/Resources.html#getTextArray(kotlin.Int)).

| Parameters ||
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#):The application's environment. This value cannot be`null`. |
| `textArrayResId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The identifier of the array to use as the data source. |
| `textViewResId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The identifier of the layout used to create views. |

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| [ArrayAdapter](https://developer.android.com/reference/kotlin/android/widget/ArrayAdapter#)< [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!> | An ArrayAdapter. This value cannot be`null`. |

### getAutofillOptions

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getAutofillOptions(): Array<CharSequence!>?
```

Gets a string representation of the adapter data that can help [android.service.autofill.AutofillService](https://developer.android.com/reference/kotlin/android/service/autofill/AutofillService.html#) autofill the view backed by the adapter.

It should only be set (i.e., non-`null`if the values do not represent PII (Personally Identifiable Information - sensitive data such as email addresses, credit card numbers, passwords, etc...). For example, it's ok to return a list of month names, but not a list of usernames. A good rule of thumb is that if the adapter data comes from static resources, such data is not PII - see [android.view.ViewStructure#setDataIsSensitive(boolean)](https://developer.android.com/reference/kotlin/android/view/ViewStructure.html#setDataIsSensitive(kotlin.Boolean))for more info.

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!>? | values from the string array used by [createFromResource(android.content.Context,int,int)](https://developer.android.com/reference/kotlin/android/widget/ArrayAdapter#createFromResource(android.content.Context,%20kotlin.Int,%20kotlin.Int)), or`null`if object was created otherwsie or if contents were dynamically changed after creation. |

### getContext

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getContext(): Context
```

Returns the context associated with this array adapter. The context is used to create views from the resource passed to the constructor.

| Return ||
|-----------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#) | The Context associated with this adapter. This value cannot be`null`. |

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

Gets a [android.view.View](https://developer.android.com/reference/kotlin/android/view/View.html#) that displays in the drop down popup the data at the specified position in the data set.

| Parameters ||
|---------------|----------------------------------------------------------------------------------------------------------------------|
| `position` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):index of the item whose view we want. |
| `convertView` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)?:This value may be`null`. |
| `parent` | [ViewGroup](https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#):This value cannot be`null`. |

| Return ||
|---------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [View](https://developer.android.com/reference/kotlin/android/view/View.html#)! | a [android.view.View](https://developer.android.com/reference/kotlin/android/view/View.html#) corresponding to the data at the specified position. |

### getDropDownViewTheme

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDropDownViewTheme(): Resources.Theme?
```

Returns the value previously set by a call to [setDropDownViewTheme(android.content.res.Resources.Theme)](https://developer.android.com/reference/kotlin/android/widget/ThemedSpinnerAdapter#setDropDownViewTheme(android.content.res.Resources.Theme)).

| Return ||
|--------------------------------------------------------------------------------------------------------------|--------------------------|
| [Resources.Theme](https://developer.android.com/reference/kotlin/android/content/res/Resources.Theme.html#)? | This value may be`null`. |

### getFilter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getFilter(): Filter
```

Returns a filter that can be used to constrain data with a filtering pattern.

This method is usually implemented by [android.widget.Adapter](https://developer.android.com/reference/kotlin/android/widget/Adapter) classes.

| Return ||
|--------------------------------------------------------------------------------|-----------------------------|
| [Filter](https://developer.android.com/reference/kotlin/android/widget/Filter) | This value cannot be`null`. |

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

Get a View that displays the data at the specified position in the data set. You can either create a View manually or inflate it from an XML layout file. When the View is inflated, the parent View (GridView, ListView...) will apply default layout parameters unless you use [android.view.LayoutInflater#inflate(int, android.view.ViewGroup, boolean)](https://developer.android.com/reference/kotlin/android/view/LayoutInflater.html#inflate(kotlin.Int,%20android.view.ViewGroup,%20kotlin.Boolean))to specify a root view and to prevent attachment to the root.

| Parameters ||
|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `position` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The position of the item within the adapter's data set of the item whose view we want. |
| `convertView` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)?:This value may be`null`. |
| `parent` | [ViewGroup](https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#):This value cannot be`null`. |

| Return ||
|--------------------------------------------------------------------------------|-----------------------------|
| [View](https://developer.android.com/reference/kotlin/android/view/View.html#) | This value cannot be`null`. |

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

- [#getDropDownView(int, android.view.View, android.view.ViewGroup)](https://developer.android.com/reference/kotlin/android/widget/ArrayAdapter#getDropDownView(kotlin.Int,%20android.view.View,%20android.view.ViewGroup)) 

### setDropDownViewTheme

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setDropDownViewTheme(theme: Resources.Theme?): Unit
```

Sets the [Resources.Theme](https://developer.android.com/reference/kotlin/android/content/res/Resources.Theme.html#) against which drop-down views are inflated.

By default, drop-down views are inflated against the theme of the [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#) passed to the adapter's constructor.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `theme` | [Resources.Theme](https://developer.android.com/reference/kotlin/android/content/res/Resources.Theme.html#)?:the theme against which to inflate drop-down views or`null`to use the theme from the adapter's context |

**See Also**

- [#getDropDownView(int, View, ViewGroup)](https://developer.android.com/reference/kotlin/android/widget/ArrayAdapter#getDropDownView(kotlin.Int,%20android.view.View,%20android.view.ViewGroup)) 

### setNotifyOnChange

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setNotifyOnChange(notifyOnChange: Boolean): Unit
```

Control whether methods that change the list ([add](https://developer.android.com/reference/kotlin/android/widget/ArrayAdapter#add(android.widget.ArrayAdapter.T)), [addAll(java.util.Collection)](https://developer.android.com/reference/kotlin/android/widget/ArrayAdapter#addAll(kotlin.collections.MutableCollection)),[addAll(java.lang.Object[])](https://developer.android.com/reference/kotlin/android/widget/ArrayAdapter#addAll(android.widget.ArrayAdapter.T)), [insert](https://developer.android.com/reference/kotlin/android/widget/ArrayAdapter#insert(android.widget.ArrayAdapter.T,%20kotlin.Int)), [remove](https://developer.android.com/reference/kotlin/android/widget/ArrayAdapter#remove(android.widget.ArrayAdapter.T)), [clear](https://developer.android.com/reference/kotlin/android/widget/ArrayAdapter#clear()), [sort(java.util.Comparator)](https://developer.android.com/reference/kotlin/android/widget/ArrayAdapter#sort(java.util.Comparator))) automatically call [notifyDataSetChanged](https://developer.android.com/reference/kotlin/android/widget/ArrayAdapter#notifyDataSetChanged()). If set to false, caller must manually call notifyDataSetChanged() to have the changes reflected in the attached view. The default is true, and calling notifyDataSetChanged() resets the flag to true.

| Parameters ||
|------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `notifyOnChange` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):if true, modifications to the list will automatically call [notifyDataSetChanged](https://developer.android.com/reference/kotlin/android/widget/ArrayAdapter#notifyDataSetChanged()) |

### sort

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun sort(comparator: Comparator<in T>): Unit
```

Sorts the content of this adapter using the specified comparator.

| Parameters ||
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `comparator` | [Comparator](https://developer.android.com/reference/kotlin/java/util/Comparator.html#)\<inT\>:The comparator used to sort the objects contained in this adapter. This value cannot be`null`. |
