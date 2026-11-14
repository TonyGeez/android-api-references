# BaseAdapter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BaseAdapter

Kotlin| [Java](BaseAdapter.md) 
| --- | --- |

```
abstract class BaseAdapter : ListAdapter, SpinnerAdapter
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.widget.BaseAdapter](BaseAdapter.md) |

| Known Direct Subclasses [ArrayAdapter](ArrayAdapter.md), [CursorAdapter](CursorAdapter.md), [SimpleAdapter](SimpleAdapter.md) |----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [ArrayAdapter](ArrayAdapter.md) | You can use this adapter to provide views for an [AdapterView](AdapterView.md), Returns a view for each object in a collection of data objects you provide, and can be used with list-based user interface widgets such as [ListView](ListView.md) or [Spinner](Spinner.md). | | [CursorAdapter](CursorAdapter.md) | Adapter that exposes data from a [Cursor](../android.database/Cursor.md) to a [ListView](ListView.md) widget. | | [SimpleAdapter](SimpleAdapter.md) | An easy adapter to map static data to views defined in an XML file. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [ResourceCursorAdapter](ResourceCursorAdapter.md), [SimpleCursorAdapter](SimpleCursorAdapter.md) |--------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------| | [ResourceCursorAdapter](ResourceCursorAdapter.md) | An easy adapter that creates views defined in an XML file. | | [SimpleCursorAdapter](SimpleCursorAdapter.md) | An easy adapter to map columns from a cursor to TextViews or ImageViews defined in an XML file. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Common base class of common implementation for an [Adapter](Adapter.md) that can be used in both [ListView](ListView.md)(by implementing the specialized [ListAdapter](ListAdapter.md) interface) and [Spinner](Spinner.md)(by implementing the specialized [SpinnerAdapter](SpinnerAdapter.md) interface).

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------|---|
| [BaseAdapter](BaseAdapter.md))`()` <br /> |

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [areAllItemsEnabled](BaseAdapter.md))`()` <br /> |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!\>? | [getAutofillOptions](BaseAdapter.md))`()` <br /> |
| open [View](../android.view/View.md)! | [getDropDownView](BaseAdapter.md))`(`position:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `convertView:` ` [View](../android.view/View.md)!`, `parent:` ` [ViewGroup](../android.view/ViewGroup.md)!`)` <br /> |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getItemViewType](BaseAdapter.md))`(`position:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getViewTypeCount](BaseAdapter.md))`()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasStableIds](BaseAdapter.md))`()` <br /> |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEmpty](BaseAdapter.md))`()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEnabled](BaseAdapter.md))`(`position:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [notifyDataSetChanged](BaseAdapter.md))`()` Notifies the attached observers that the underlying data has been changed and any View reflecting the data set should refresh itself. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [notifyDataSetInvalidated](BaseAdapter.md))`()` Notifies the attached observers that the underlying data is no longer valid or available. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerDataSetObserver](BaseAdapter.md))`(`observer:` ` [DataSetObserver](../android.database/DataSetObserver.md)!`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAutofillOptions](BaseAdapter.md))`(`vararg` `options:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` Sets the value returned by [getAutofillOptions()](BaseAdapter.md)) |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unregisterDataSetObserver](BaseAdapter.md))`(`observer:` ` [DataSetObserver](../android.database/DataSetObserver.md)!`)` <br /> |

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
| `convertView` | [View](../android.view/View.md)!:the old view to reuse, if possible. Note: You should check that this view is non-null and of an appropriate type before using. If it is not possible to convert this view to display the correct data, this method can create a new view. |
| `parent` | [ViewGroup](../android.view/ViewGroup.md)!:the parent that this view will eventually be attached to |
| --- | --- |

| Return ||
|---------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [View](../android.view/View.md)! | a [android.view.View](../android.view/View.md) corresponding to the data at the specified position. |

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
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | An integer representing the type of View. Two views should share the same type if one can be converted to the other in [getView](Adapter.md)). Note: Integers must be in the range 0 to [getViewTypeCount](Adapter.md))- 1. [IGNORE_ITEM_VIEW_TYPE](Adapter.md) can also be returned. |

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
| `observer` | [DataSetObserver](../android.database/DataSetObserver.md)!:the object that gets notified when the data set changes. |

### setAutofillOptions

Added in [API level 27](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setAutofillOptions(vararg options: CharSequence!): Unit
```

Sets the value returned by [getAutofillOptions()](BaseAdapter.md))

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
| `observer` | [DataSetObserver](../android.database/DataSetObserver.md)!:the object to unregister. |
