# BaseAdapter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BaseAdapter

Kotlin| [Java](https://developer.android.com/reference/android/widget/BaseAdapter "View this page in Java") 
| --- | --- |

```
abstract class BaseAdapter : ListAdapter, SpinnerAdapter
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.widget.BaseAdapter](https://developer.android.com/reference/kotlin/android/widget/BaseAdapter#) |

| Known Direct Subclasses [ArrayAdapter](https://developer.android.com/reference/kotlin/android/widget/ArrayAdapter), [CursorAdapter](https://developer.android.com/reference/kotlin/android/widget/CursorAdapter), [SimpleAdapter](https://developer.android.com/reference/kotlin/android/widget/SimpleAdapter) |----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [ArrayAdapter](https://developer.android.com/reference/kotlin/android/widget/ArrayAdapter) | You can use this adapter to provide views for an [AdapterView](https://developer.android.com/reference/kotlin/android/widget/AdapterView), Returns a view for each object in a collection of data objects you provide, and can be used with list-based user interface widgets such as [ListView](https://developer.android.com/reference/kotlin/android/widget/ListView) or [Spinner](https://developer.android.com/reference/kotlin/android/widget/Spinner). | | [CursorAdapter](https://developer.android.com/reference/kotlin/android/widget/CursorAdapter) | Adapter that exposes data from a [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#) to a [ListView](https://developer.android.com/reference/kotlin/android/widget/ListView) widget. | | [SimpleAdapter](https://developer.android.com/reference/kotlin/android/widget/SimpleAdapter) | An easy adapter to map static data to views defined in an XML file. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [ResourceCursorAdapter](https://developer.android.com/reference/kotlin/android/widget/ResourceCursorAdapter), [SimpleCursorAdapter](https://developer.android.com/reference/kotlin/android/widget/SimpleCursorAdapter) |--------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------| | [ResourceCursorAdapter](https://developer.android.com/reference/kotlin/android/widget/ResourceCursorAdapter) | An easy adapter that creates views defined in an XML file. | | [SimpleCursorAdapter](https://developer.android.com/reference/kotlin/android/widget/SimpleCursorAdapter) | An easy adapter to map columns from a cursor to TextViews or ImageViews defined in an XML file. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Common base class of common implementation for an [Adapter](https://developer.android.com/reference/kotlin/android/widget/Adapter) that can be used in both [ListView](https://developer.android.com/reference/kotlin/android/widget/ListView)(by implementing the specialized [ListAdapter](https://developer.android.com/reference/kotlin/android/widget/ListAdapter) interface) and [Spinner](https://developer.android.com/reference/kotlin/android/widget/Spinner)(by implementing the specialized [SpinnerAdapter](https://developer.android.com/reference/kotlin/android/widget/SpinnerAdapter) interface).

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------|---|
| [BaseAdapter](https://developer.android.com/reference/kotlin/android/widget/BaseAdapter#BaseAdapter())`()` <br /> |

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [areAllItemsEnabled](https://developer.android.com/reference/kotlin/android/widget/BaseAdapter#areAllItemsEnabled())`()` <br /> |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!\>? | [getAutofillOptions](https://developer.android.com/reference/kotlin/android/widget/BaseAdapter#getAutofillOptions())`()` <br /> |
| open [View](https://developer.android.com/reference/kotlin/android/view/View.html#)! | [getDropDownView](https://developer.android.com/reference/kotlin/android/widget/BaseAdapter#getDropDownView(kotlin.Int,%20android.view.View,%20android.view.ViewGroup))`(`position:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `convertView:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!`, `parent:` ` [ViewGroup](https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#)!`)` <br /> |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getItemViewType](https://developer.android.com/reference/kotlin/android/widget/BaseAdapter#getItemViewType(kotlin.Int))`(`position:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getViewTypeCount](https://developer.android.com/reference/kotlin/android/widget/BaseAdapter#getViewTypeCount())`()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasStableIds](https://developer.android.com/reference/kotlin/android/widget/BaseAdapter#hasStableIds())`()` <br /> |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEmpty](https://developer.android.com/reference/kotlin/android/widget/BaseAdapter#isEmpty())`()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEnabled](https://developer.android.com/reference/kotlin/android/widget/BaseAdapter#isEnabled(kotlin.Int))`(`position:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [notifyDataSetChanged](https://developer.android.com/reference/kotlin/android/widget/BaseAdapter#notifyDataSetChanged())`()` Notifies the attached observers that the underlying data has been changed and any View reflecting the data set should refresh itself. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [notifyDataSetInvalidated](https://developer.android.com/reference/kotlin/android/widget/BaseAdapter#notifyDataSetInvalidated())`()` Notifies the attached observers that the underlying data is no longer valid or available. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerDataSetObserver](https://developer.android.com/reference/kotlin/android/widget/BaseAdapter#registerDataSetObserver(android.database.DataSetObserver))`(`observer:` ` [DataSetObserver](https://developer.android.com/reference/kotlin/android/database/DataSetObserver.html#)!`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAutofillOptions](https://developer.android.com/reference/kotlin/android/widget/BaseAdapter#setAutofillOptions(kotlin.CharSequence))`(`vararg` `options:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` Sets the value returned by [getAutofillOptions()](https://developer.android.com/reference/kotlin/android/widget/BaseAdapter#getAutofillOptions()) |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unregisterDataSetObserver](https://developer.android.com/reference/kotlin/android/widget/BaseAdapter#unregisterDataSetObserver(android.database.DataSetObserver))`(`observer:` ` [DataSetObserver](https://developer.android.com/reference/kotlin/android/database/DataSetObserver.html#)!`)` <br /> |

## Public constructors

### BaseAdapter

```
BaseAdapter()
```

## Public methods

### areAllItemsEnabled

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun areAllItemsEnabled(): Boolean
```

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if all items are enabled, false otherwise. |

### getAutofillOptions

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getAutofillOptions(): Array<CharSequence!>?
```

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!>? | `null`by default, unless implementations override it. |

### getDropDownView

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDropDownView(
    position: Int, 
    convertView: View!, 
    parent: ViewGroup!
): View!
```

| Parameters ||
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `position` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):index of the item whose view we want. |
| `convertView` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!:the old view to reuse, if possible. Note: You should check that this view is non-null and of an appropriate type before using. If it is not possible to convert this view to display the correct data, this method can create a new view. |
| `parent` | [ViewGroup](https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#)!:the parent that this view will eventually be attached to |
| --- | --- |

| Return ||
|---------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [View](https://developer.android.com/reference/kotlin/android/view/View.html#)! | a [android.view.View](https://developer.android.com/reference/kotlin/android/view/View.html#) corresponding to the data at the specified position. |

### getItemViewType

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getItemViewType(position: Int): Int
```

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `position` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The position of the item within the adapter's data set whose view type we want. |

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | An integer representing the type of View. Two views should share the same type if one can be converted to the other in [getView](https://developer.android.com/reference/kotlin/android/widget/Adapter#getView(kotlin.Int,%20android.view.View,%20android.view.ViewGroup)). Note: Integers must be in the range 0 to [getViewTypeCount](https://developer.android.com/reference/kotlin/android/widget/Adapter#getViewTypeCount())- 1. [IGNORE_ITEM_VIEW_TYPE](https://developer.android.com/reference/kotlin/android/widget/Adapter#IGNORE_ITEM_VIEW_TYPE:kotlin.Int) can also be returned. |

### getViewTypeCount

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getViewTypeCount(): Int
```

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The number of types of Views that will be created by this adapter |

### hasStableIds

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hasStableIds(): Boolean
```

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if the same id always refers to the same object. |

### isEmpty

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isEmpty(): Boolean
```

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if this adapter doesn't contain any data. This is used to determine whether the empty view should be displayed. A typical implementation will return getCount() == 0 but since getCount() includes the headers and footers, specialized adapters might want a different behavior. |

### isEnabled

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isEnabled(position: Int): Boolean
```

| Parameters ||
|------------|----------------------------------------------------------------------------------------------|
| `position` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Index of the item |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if the item is not a separator |

### notifyDataSetChanged

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun notifyDataSetChanged(): Unit
```

Notifies the attached observers that the underlying data has been changed and any View reflecting the data set should refresh itself. 

### notifyDataSetInvalidated

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun notifyDataSetInvalidated(): Unit
```

Notifies the attached observers that the underlying data is no longer valid or available. Once invoked this adapter is no longer valid and should not report further data set changes. 

### registerDataSetObserver

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun registerDataSetObserver(observer: DataSetObserver!): Unit
```

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `observer` | [DataSetObserver](https://developer.android.com/reference/kotlin/android/database/DataSetObserver.html#)!:the object that gets notified when the data set changes. |

### setAutofillOptions

Added in [API level 27](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setAutofillOptions(vararg options: CharSequence!): Unit
```

Sets the value returned by [getAutofillOptions()](https://developer.android.com/reference/kotlin/android/widget/BaseAdapter#getAutofillOptions())

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------------|
| `options` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:This value may be`null`. |

### unregisterDataSetObserver

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun unregisterDataSetObserver(observer: DataSetObserver!): Unit
```

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------|
| `observer` | [DataSetObserver](https://developer.android.com/reference/kotlin/android/database/DataSetObserver.html#)!:the object to unregister. |
