# ThemedSpinnerAdapter

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ThemedSpinnerAdapter

Kotlin| [Java](ThemedSpinnerAdapter.md) 
| --- | --- |

```
interface ThemedSpinnerAdapter : SpinnerAdapter
```

| [android.widget.ThemedSpinnerAdapter](ThemedSpinnerAdapter.md) |

| Known Direct Subclasses [ArrayAdapter](ArrayAdapter.md), [CursorAdapter](CursorAdapter.md), [SimpleAdapter](SimpleAdapter.md) |----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [ArrayAdapter](ArrayAdapter.md) | You can use this adapter to provide views for an [AdapterView](AdapterView.md), Returns a view for each object in a collection of data objects you provide, and can be used with list-based user interface widgets such as [ListView](ListView.md) or [Spinner](Spinner.md). | | [CursorAdapter](CursorAdapter.md) | Adapter that exposes data from a [Cursor](../android.database/Cursor.md) to a [ListView](ListView.md) widget. | | [SimpleAdapter](SimpleAdapter.md) | An easy adapter to map static data to views defined in an XML file. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [ResourceCursorAdapter](ResourceCursorAdapter.md), [SimpleCursorAdapter](SimpleCursorAdapter.md) |--------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------| | [ResourceCursorAdapter](ResourceCursorAdapter.md) | An easy adapter that creates views defined in an XML file. | | [SimpleCursorAdapter](SimpleCursorAdapter.md) | An easy adapter to map columns from a cursor to TextViews or ImageViews defined in an XML file. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

An extension of SpinnerAdapter that is capable of inflating drop-down views against a different theme than normal views.

Classes that implement this interface should use the theme provided to [setDropDownViewTheme(android.content.res.Resources.Theme)](ThemedSpinnerAdapter.md))when creating views in [SpinnerAdapter.getDropDownView(int, View, ViewGroup)](SpinnerAdapter.md)).

## Summary

| Inherited constants ||
|---|---|
| From class [Adapter](Adapter.md) |----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [IGNORE_ITEM_VIEW_TYPE](Adapter.md) <br /> An item view type that causes the [AdapterView](AdapterView.md) to ignore the item view. For example, this can be used if the client does not want a particular view to be given for conversion in [getView(int,android.view.View,android.view.ViewGroup)](Adapter.md)). <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [NO_SELECTION](Adapter.md) <br /> | ||

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Resources.Theme](../android/content/res/Resources.Theme.md)? | [getDropDownViewTheme](ThemedSpinnerAdapter.md))`()` Returns the value previously set by a call to [setDropDownViewTheme(android.content.res.Resources.Theme)](ThemedSpinnerAdapter.md)). |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDropDownViewTheme](ThemedSpinnerAdapter.md))`(`theme:` ` [Resources.Theme](../android/content/res/Resources.Theme.md)?`)` Sets the [Resources.Theme](../android/content/res/Resources.Theme.md) against which drop-down views are inflated. |

| Inherited functions ||
|---|---|
| From class [Adapter](Adapter.md) |---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!>? | [getAutofillOptions](Adapter.md))`()` <br /> Gets a string representation of the adapter data that can help [android.service.autofill.AutofillService](../android.service.autofill/AutofillService.md) autofill the view backed by the adapter. It should only be set (i.e., non-`null`if the values do not represent PII (Personally Identifiable Information - sensitive data such as email addresses, credit card numbers, passwords, etc...). For example, it's ok to return a list of month names, but not a list of usernames. A good rule of thumb is that if the adapter data comes from static resources, such data is not PII - see [android.view.ViewStructure#setDataIsSensitive(boolean)](../android.view/ViewStructure.md))for more info. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getCount](Adapter.md))`()` <br /> How many items are in the data set represented by this Adapter. <br /> | | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getItem](Adapter.md))`(`position:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Get the data item associated with the specified position in the data set. <br /> | | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getItemId](Adapter.md))`(`position:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Get the row id associated with the specified position in the list. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getItemViewType](Adapter.md))`(`position:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Get the type of View that will be created by [getView](Adapter.md))for the specified item. <br /> | | [View](../android.view/View.md)! | [getView](Adapter.md))`(`position:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `convertView:` ` [View](../android.view/View.md)!`, `parent:` ` [ViewGroup](../android.view/ViewGroup.md)!`)` <br /> Get a View that displays the data at the specified position in the data set. You can either create a View manually or inflate it from an XML layout file. When the View is inflated, the parent View (GridView, ListView...) will apply default layout parameters unless you use [android.view.LayoutInflater#inflate(int, android.view.ViewGroup, boolean)](../android.view/LayoutInflater.md))to specify a root view and to prevent attachment to the root. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getViewTypeCount](Adapter.md))`()` <br /> Returns the number of types of Views that will be created by [getView](Adapter.md)). Each type represents a set of views that can be converted in [getView](Adapter.md)). If the adapter always returns the same type of View for all items, this method should return 1. This method will only be called when the adapter is set on the [AdapterView](AdapterView.md). <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasStableIds](Adapter.md))`()` <br /> Indicates whether the item ids are stable across changes to the underlying data. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEmpty](Adapter.md))`()` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerDataSetObserver](Adapter.md))`(`observer:` ` [DataSetObserver](../android.database/DataSetObserver.md)!`)` <br /> Register an observer that is called when changes happen to the data used by this adapter. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unregisterDataSetObserver](Adapter.md))`(`observer:` ` [DataSetObserver](../android.database/DataSetObserver.md)!`)` <br /> Unregister an observer that has previously been registered with this adapter via [registerDataSetObserver](Adapter.md)). <br /> | ||
| From class [SpinnerAdapter](SpinnerAdapter.md) |---------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [View](../android.view/View.md)! | [getDropDownView](SpinnerAdapter.md))`(`position:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `convertView:` ` [View](../android.view/View.md)!`, `parent:` ` [ViewGroup](../android.view/ViewGroup.md)!`)` <br /> Gets a [android.view.View](../android.view/View.md) that displays in the drop down popup the data at the specified position in the data set. <br /> | ||

## Public methods

### getDropDownViewTheme

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getDropDownViewTheme(): Resources.Theme?
```

Returns the value previously set by a call to [setDropDownViewTheme(android.content.res.Resources.Theme)](ThemedSpinnerAdapter.md)).

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

- [android.widget.SpinnerAdapter#getDropDownView(int, View, ViewGroup)](SpinnerAdapter.md))
