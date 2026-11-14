# ThemedSpinnerAdapter

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ThemedSpinnerAdapter

Kotlin| [Java](../android/widget/ThemedSpinnerAdapter.md) 
| --- | --- |

```
interface ThemedSpinnerAdapter : SpinnerAdapter
```

| [android.widget.ThemedSpinnerAdapter](../android/widget/ThemedSpinnerAdapter.md) |

| Known Direct Subclasses [ArrayAdapter](../android/widget/ArrayAdapter.md), [CursorAdapter](../android/widget/CursorAdapter.md), [SimpleAdapter](../android/widget/SimpleAdapter.md) |----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [ArrayAdapter](../android/widget/ArrayAdapter.md) | You can use this adapter to provide views for an [AdapterView](../android/widget/AdapterView.md), Returns a view for each object in a collection of data objects you provide, and can be used with list-based user interface widgets such as [ListView](../android/widget/ListView.md) or [Spinner](../android/widget/Spinner.md). | | [CursorAdapter](../android/widget/CursorAdapter.md) | Adapter that exposes data from a [Cursor](../android/database/Cursor.md) to a [ListView](../android/widget/ListView.md) widget. | | [SimpleAdapter](../android/widget/SimpleAdapter.md) | An easy adapter to map static data to views defined in an XML file. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [ResourceCursorAdapter](../android/widget/ResourceCursorAdapter.md), [SimpleCursorAdapter](../android/widget/SimpleCursorAdapter.md) |--------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------| | [ResourceCursorAdapter](../android/widget/ResourceCursorAdapter.md) | An easy adapter that creates views defined in an XML file. | | [SimpleCursorAdapter](../android/widget/SimpleCursorAdapter.md) | An easy adapter to map columns from a cursor to TextViews or ImageViews defined in an XML file. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

An extension of SpinnerAdapter that is capable of inflating drop-down views against a different theme than normal views.

Classes that implement this interface should use the theme provided to [setDropDownViewTheme(android.content.res.Resources.Theme)](../android/widget/ThemedSpinnerAdapter.md))when creating views in [SpinnerAdapter.getDropDownView(int, View, ViewGroup)](../android/widget/SpinnerAdapter.md)).

## Summary

| Inherited constants ||
|---|---|
| From class [Adapter](../android/widget/Adapter.md) |----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [IGNORE_ITEM_VIEW_TYPE](../android/widget/Adapter.md) <br /> An item view type that causes the [AdapterView](../android/widget/AdapterView.md) to ignore the item view. For example, this can be used if the client does not want a particular view to be given for conversion in [getView(int,android.view.View,android.view.ViewGroup)](../android/widget/Adapter.md)). <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [NO_SELECTION](../android/widget/Adapter.md) <br /> | ||

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Resources.Theme](../android/content/res/Resources.Theme.md)? | [getDropDownViewTheme](../android/widget/ThemedSpinnerAdapter.md))`()` Returns the value previously set by a call to [setDropDownViewTheme(android.content.res.Resources.Theme)](../android/widget/ThemedSpinnerAdapter.md)). |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDropDownViewTheme](../android/widget/ThemedSpinnerAdapter.md))`(`theme:` ` [Resources.Theme](../android/content/res/Resources.Theme.md)?`)` Sets the [Resources.Theme](../android/content/res/Resources.Theme.md) against which drop-down views are inflated. |

| Inherited functions ||
|---|---|
| From class [Adapter](../android/widget/Adapter.md) |---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!>? | [getAutofillOptions](../android/widget/Adapter.md))`()` <br /> Gets a string representation of the adapter data that can help [android.service.autofill.AutofillService](../android/service/autofill/AutofillService.md) autofill the view backed by the adapter. It should only be set (i.e., non-`null`if the values do not represent PII (Personally Identifiable Information - sensitive data such as email addresses, credit card numbers, passwords, etc...). For example, it's ok to return a list of month names, but not a list of usernames. A good rule of thumb is that if the adapter data comes from static resources, such data is not PII - see [android.view.ViewStructure#setDataIsSensitive(boolean)](../android/view/ViewStructure.md))for more info. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getCount](../android/widget/Adapter.md))`()` <br /> How many items are in the data set represented by this Adapter. <br /> | | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getItem](../android/widget/Adapter.md))`(`position:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Get the data item associated with the specified position in the data set. <br /> | | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getItemId](../android/widget/Adapter.md))`(`position:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Get the row id associated with the specified position in the list. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getItemViewType](../android/widget/Adapter.md))`(`position:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Get the type of View that will be created by [getView](../android/widget/Adapter.md))for the specified item. <br /> | | [View](../android/view/View.md)! | [getView](../android/widget/Adapter.md))`(`position:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `convertView:` ` [View](../android/view/View.md)!`, `parent:` ` [ViewGroup](../android/view/ViewGroup.md)!`)` <br /> Get a View that displays the data at the specified position in the data set. You can either create a View manually or inflate it from an XML layout file. When the View is inflated, the parent View (GridView, ListView...) will apply default layout parameters unless you use [android.view.LayoutInflater#inflate(int, android.view.ViewGroup, boolean)](../android/view/LayoutInflater.md))to specify a root view and to prevent attachment to the root. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getViewTypeCount](../android/widget/Adapter.md))`()` <br /> Returns the number of types of Views that will be created by [getView](../android/widget/Adapter.md)). Each type represents a set of views that can be converted in [getView](../android/widget/Adapter.md)). If the adapter always returns the same type of View for all items, this method should return 1. This method will only be called when the adapter is set on the [AdapterView](../android/widget/AdapterView.md). <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasStableIds](../android/widget/Adapter.md))`()` <br /> Indicates whether the item ids are stable across changes to the underlying data. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEmpty](../android/widget/Adapter.md))`()` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerDataSetObserver](../android/widget/Adapter.md))`(`observer:` ` [DataSetObserver](../android/database/DataSetObserver.md)!`)` <br /> Register an observer that is called when changes happen to the data used by this adapter. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unregisterDataSetObserver](../android/widget/Adapter.md))`(`observer:` ` [DataSetObserver](../android/database/DataSetObserver.md)!`)` <br /> Unregister an observer that has previously been registered with this adapter via [registerDataSetObserver](../android/widget/Adapter.md)). <br /> | ||
| From class [SpinnerAdapter](../android/widget/SpinnerAdapter.md) |---------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [View](../android/view/View.md)! | [getDropDownView](../android/widget/SpinnerAdapter.md))`(`position:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `convertView:` ` [View](../android/view/View.md)!`, `parent:` ` [ViewGroup](../android/view/ViewGroup.md)!`)` <br /> Gets a [android.view.View](../android/view/View.md) that displays in the drop down popup the data at the specified position in the data set. <br /> | ||

## Public methods

### getDropDownViewTheme

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getDropDownViewTheme(): Resources.Theme?
```

Returns the value previously set by a call to [setDropDownViewTheme(android.content.res.Resources.Theme)](../android/widget/ThemedSpinnerAdapter.md)).

| Return ||
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Resources.Theme](../android/content/res/Resources.Theme.md)? | the [Resources.Theme](../android/content/res/Resources.Theme.md) against which drop-down views are inflated, or`null`if one has not been explicitly set |

### setDropDownViewTheme

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setDropDownViewTheme(theme: Resources.Theme?): Unit
```

Sets the [Resources.Theme](../android/content/res/Resources.Theme.md) against which drop-down views are inflated.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `theme` | [Resources.Theme](../android/content/res/Resources.Theme.md)?:the context against which to inflate drop-down views, or`null`to use the default theme |

**See Also**

- [android.widget.SpinnerAdapter#getDropDownView(int, View, ViewGroup)](../android/widget/SpinnerAdapter.md))
