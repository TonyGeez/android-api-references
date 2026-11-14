# SimpleCursorAdapter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SimpleCursorAdapter

Kotlin| [Java](SimpleCursorAdapter.md) 
| --- | --- |

```
open class SimpleCursorAdapter : ResourceCursorAdapter
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [android.widget.BaseAdapter](BaseAdapter.md) ||||
| | ↳ | [android.widget.CursorAdapter](CursorAdapter.md) |||
| | | ↳ | [android.widget.ResourceCursorAdapter](ResourceCursorAdapter.md) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [android.widget.SimpleCursorAdapter](SimpleCursorAdapter.md) |

An easy adapter to map columns from a cursor to TextViews or ImageViews defined in an XML file. You can specify which columns you want, which views you want to display the columns, and the XML file that defines the appearance of these views. Binding occurs in two phases. First, if a [android.widget.SimpleCursorAdapter.ViewBinder](../android/widget/SimpleCursorAdapter.ViewBinder.md) is available, [ViewBinder.setViewValue(android.view.View, android.database.Cursor, int)](../android/widget/SimpleCursorAdapter.ViewBinder.md))is invoked. If the returned value is true, binding has occured. If the returned value is false and the view to bind is a TextView, [setViewText(android.widget.TextView,java.lang.String)](SimpleCursorAdapter.md))is invoked. If the returned value is false and the view to bind is an ImageView, [setViewImage(android.widget.ImageView,java.lang.String)](SimpleCursorAdapter.md))is invoked. If no appropriate binding can be found, an [IllegalStateException](../java.lang/IllegalStateException.md) is thrown. If this adapter is used with filtering, for instance in an [android.widget.AutoCompleteTextView](AutoCompleteTextView.md), you can use the [android.widget.SimpleCursorAdapter.CursorToStringConverter](../android/widget/SimpleCursorAdapter.CursorToStringConverter.md) and the [android.widget.FilterQueryProvider](FilterQueryProvider.md) interfaces to get control over the filtering process. You can refer to [convertToString(android.database.Cursor)](SimpleCursorAdapter.md))and [runQueryOnBackgroundThread(java.lang.CharSequence)](CursorAdapter.md))for more information.

## Summary

| Nested classes ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [CursorToStringConverter](../android/widget/SimpleCursorAdapter.CursorToStringConverter.md) This class can be used by external clients of SimpleCursorAdapter to define how the Cursor should be converted to a String. |
| abstract | [ViewBinder](../android/widget/SimpleCursorAdapter.ViewBinder.md) This class can be used by external clients of SimpleCursorAdapter to bind values fom the Cursor to views. |

| Inherited constants ||
|---|---|
| From class [CursorAdapter](CursorAdapter.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FLAG_AUTO_REQUERY](CursorAdapter.md) <br /> If set the adapter will call requery() on the cursor whenever a content change notification is delivered. Implies [FLAG_REGISTER_CONTENT_OBSERVER](CursorAdapter.md). <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FLAG_REGISTER_CONTENT_OBSERVER](CursorAdapter.md) <br /> If set the adapter will register a content observer on the cursor and will call [onContentChanged()](CursorAdapter.md))when a notification comes in. Be careful when using this flag: you will need to unset the current Cursor from the adapter to avoid leaks due to its registered observers. This flag is not needed when using a CursorAdapter with a [android.content.CursorLoader](../android.content/CursorLoader.md). <br /> | ||

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SimpleCursorAdapter](SimpleCursorAdapter.md))`(`context:` ` [Context](../android.content/Context.md)!`, `layout:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `c:` ` [Cursor](../android.database/Cursor.md)!`, `from:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`, `to:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!`)` Constructor the enables auto-requery. |
| [SimpleCursorAdapter](SimpleCursorAdapter.md))`(`context:` ` [Context](../android.content/Context.md)!`, `layout:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `c:` ` [Cursor](../android.database/Cursor.md)!`, `from:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`, `to:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Standard constructor. |

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [bindView](SimpleCursorAdapter.md))`(`view:` ` [View](../android.view/View.md)!`, `context:` ` [Context](../android.content/Context.md)!`, `cursor:` ` [Cursor](../android.database/Cursor.md)!`)` Binds all of the field names passed into the "to" parameter of the constructor with their corresponding cursor columns as specified in the "from" parameter. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [changeCursorAndColumns](SimpleCursorAdapter.md))`(`c:` ` [Cursor](../android.database/Cursor.md)!`, `from:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`, `to:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!`)` Change the cursor and change the column-to-view mappings at the same time. |
| open [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | [convertToString](SimpleCursorAdapter.md))`(`cursor:` ` [Cursor](../android.database/Cursor.md)!`)` Returns a CharSequence representation of the specified Cursor as defined by the current CursorToStringConverter. |
| --- | --- |
| open [SimpleCursorAdapter.CursorToStringConverter](../android/widget/SimpleCursorAdapter.CursorToStringConverter.md)! | [getCursorToStringConverter](SimpleCursorAdapter.md))`()` Returns the converter used to convert the filtering Cursor into a String. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getStringConversionColumn](SimpleCursorAdapter.md))`()` Return the index of the column used to get a String representation of the Cursor. |
| open [SimpleCursorAdapter.ViewBinder](../android/widget/SimpleCursorAdapter.ViewBinder.md)! | [getViewBinder](SimpleCursorAdapter.md))`()` Returns the [ViewBinder](../android/widget/SimpleCursorAdapter.ViewBinder.md) used to bind data to views. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setCursorToStringConverter](SimpleCursorAdapter.md))`(`cursorToStringConverter:` ` [SimpleCursorAdapter.CursorToStringConverter](../android/widget/SimpleCursorAdapter.CursorToStringConverter.md)!`)` Sets the converter used to convert the filtering Cursor into a String. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setStringConversionColumn](SimpleCursorAdapter.md))`(`stringConversionColumn:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Defines the index of the column in the Cursor used to get a String representation of that Cursor. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setViewBinder](SimpleCursorAdapter.md))`(`viewBinder:` ` [SimpleCursorAdapter.ViewBinder](../android/widget/SimpleCursorAdapter.ViewBinder.md)!`)` Sets the binder used to bind data to views. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setViewImage](SimpleCursorAdapter.md))`(`v:` ` [ImageView](ImageView.md)!`, `value:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Called by bindView() to set the image for an ImageView but only if there is no existing ViewBinder or if the existing ViewBinder cannot handle binding to an ImageView. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setViewText](SimpleCursorAdapter.md))`(`v:` ` [TextView](TextView.md)!`, `text:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Called by bindView() to set the text for a TextView but only if there is no existing ViewBinder or if the existing ViewBinder cannot handle binding to a TextView. |
| open [Cursor](../android.database/Cursor.md)! | [swapCursor](SimpleCursorAdapter.md))`(`c:` ` [Cursor](../android.database/Cursor.md)!`)` <br /> |
| --- | --- |

| Inherited functions ||
|---|---|
| From class [BaseAdapter](BaseAdapter.md) |---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [areAllItemsEnabled](BaseAdapter.md))`()` <br /> | | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!>? | [getAutofillOptions](BaseAdapter.md))`()` <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getItemViewType](BaseAdapter.md))`(`position:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getViewTypeCount](BaseAdapter.md))`()` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEmpty](BaseAdapter.md))`()` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEnabled](BaseAdapter.md))`(`position:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [notifyDataSetChanged](BaseAdapter.md))`()` <br /> Notifies the attached observers that the underlying data has been changed and any View reflecting the data set should refresh itself. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [notifyDataSetInvalidated](BaseAdapter.md))`()` <br /> Notifies the attached observers that the underlying data is no longer valid or available. Once invoked this adapter is no longer valid and should not report further data set changes. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerDataSetObserver](BaseAdapter.md))`(`observer:` ` [DataSetObserver](../android.database/DataSetObserver.md)!`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAutofillOptions](BaseAdapter.md))`(`vararg` `options:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` <br /> Sets the value returned by [getAutofillOptions()](BaseAdapter.md)) <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unregisterDataSetObserver](BaseAdapter.md))`(`observer:` ` [DataSetObserver](../android.database/DataSetObserver.md)!`)` <br /> | ||
| From class [CursorAdapter](CursorAdapter.md) |--------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [bindView](CursorAdapter.md))`(`view:` ` [View](../android.view/View.md)!`, `context:` ` [Context](../android.content/Context.md)!`, `cursor:` ` [Cursor](../android.database/Cursor.md)!`)` <br /> Bind an existing view to the data pointed to by cursor <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [changeCursor](CursorAdapter.md))`(`cursor:` ` [Cursor](../android.database/Cursor.md)!`)` <br /> Change the underlying cursor to a new cursor. If there is an existing cursor it will be closed. <br /> | | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | [convertToString](CursorAdapter.md))`(`cursor:` ` [Cursor](../android.database/Cursor.md)!`)` <br /> Converts the cursor into a CharSequence. Subclasses should override this method to convert their results. The default implementation returns an empty String for null values or the default String representation of the value. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getCount](CursorAdapter.md))`()` <br /> | | [Cursor](../android.database/Cursor.md)! | [getCursor](CursorAdapter.md))`()` <br /> Returns the cursor. <br /> | | [View](../android.view/View.md)! | [getDropDownView](CursorAdapter.md))`(`position:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `convertView:` ` [View](../android.view/View.md)!`, `parent:` ` [ViewGroup](../android.view/ViewGroup.md)!`)` <br /> | | [Resources.Theme](../android/content/res/Resources.Theme.md)? | [getDropDownViewTheme](CursorAdapter.md))`()` <br /> | | [Filter](Filter.md)! | [getFilter](CursorAdapter.md))`()` <br /> | | [FilterQueryProvider](FilterQueryProvider.md)! | [getFilterQueryProvider](CursorAdapter.md))`()` <br /> Returns the query filter provider used for filtering. When the provider is null, no filtering occurs. <br /> | | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getItem](CursorAdapter.md))`(`position:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> | | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getItemId](CursorAdapter.md))`(`position:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> | | [View](../android.view/View.md)! | [getView](CursorAdapter.md))`(`position:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `convertView:` ` [View](../android.view/View.md)!`, `parent:` ` [ViewGroup](../android.view/ViewGroup.md)!`)` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasStableIds](CursorAdapter.md))`()` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [init](CursorAdapter.md))`(`context:` ` [Context](../android.content/Context.md)!`, `c:` ` [Cursor](../android.database/Cursor.md)!`, `autoRequery:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onContentChanged](CursorAdapter.md))`()` <br /> Called when the [ContentObserver](../android.database/ContentObserver.md) on the cursor receives a change notification. The default implementation provides the auto-requery logic, but may be overridden by sub classes. <br /> | | [Cursor](../android.database/Cursor.md)! | [runQueryOnBackgroundThread](CursorAdapter.md))`(`constraint:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` <br /> Runs a query with the specified constraint. This query is requested by the filter attached to this adapter. The query is provided by a [android.widget.FilterQueryProvider](FilterQueryProvider.md). If no provider is specified, the current cursor is not filtered and returned. After this method returns the resulting cursor is passed to [changeCursor(android.database.Cursor)](CursorAdapter.md))and the previous cursor is closed. This method is always executed on a background thread, not on the application's main thread (or UI thread.) Contract: when constraint is null or empty, the original results, prior to any filtering, must be returned. This method may take several seconds to complete, so it should only be called from a worker thread. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFilterQueryProvider](CursorAdapter.md))`(`filterQueryProvider:` ` [FilterQueryProvider](FilterQueryProvider.md)!`)` <br /> Sets the query filter provider used to filter the current Cursor. The provider's [android.widget.FilterQueryProvider#runQuery(CharSequence)](FilterQueryProvider.md))method is invoked when filtering is requested by a client of this adapter. <br /> | | [Cursor](../android.database/Cursor.md)! | [swapCursor](CursorAdapter.md))`(`newCursor:` ` [Cursor](../android.database/Cursor.md)!`)` <br /> Swap in a new Cursor, returning the old Cursor. Unlike [changeCursor(android.database.Cursor)](CursorAdapter.md)), the returned old Cursor is*not*closed. <br /> | ||
| From class [ResourceCursorAdapter](ResourceCursorAdapter.md) |---------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [View](../android.view/View.md)! | [newDropDownView](ResourceCursorAdapter.md))`(`context:` ` [Context](../android.content/Context.md)!`, `cursor:` ` [Cursor](../android.database/Cursor.md)!`, `parent:` ` [ViewGroup](../android.view/ViewGroup.md)!`)` <br /> | | [View](../android.view/View.md)! | [newView](ResourceCursorAdapter.md))`(`context:` ` [Context](../android.content/Context.md)!`, `cursor:` ` [Cursor](../android.database/Cursor.md)!`, `parent:` ` [ViewGroup](../android.view/ViewGroup.md)!`)` <br /> Inflates view(s) from the specified XML file. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDropDownViewResource](ResourceCursorAdapter.md))`(`dropDownLayout:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Sets the layout resource of the drop down views. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDropDownViewTheme](ResourceCursorAdapter.md))`(`theme:` ` [Resources.Theme](../android/content/res/Resources.Theme.md)?`)` <br /> Sets the [android.content.res.Resources.Theme](../android/content/res/Resources.Theme.md) against which drop-down views are inflated. By default, drop-down views are inflated against the theme of the [Context](../android.content/Context.md) passed to the adapter's constructor. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setViewResource](ResourceCursorAdapter.md))`(`layout:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Sets the layout resource of the item views. <br /> | ||
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

## Public constructors

### SimpleCursorAdapter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SimpleCursorAdapter(
    context: Context!, 
    layout: Int, 
    c: Cursor!, 
    from: Array<String!>!, 
    to: IntArray!)
```

**Deprecated:** *This option is discouraged, as it results in Cursor queries being performed on the application's UI thread and thus can cause poor responsiveness or even Application Not Responding errors. As an alternative, use [android.app.LoaderManager](../android.app/LoaderManager.md) with a [android.content.CursorLoader](../android.content/CursorLoader.md).*

Constructor the enables auto-requery. 

### SimpleCursorAdapter

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SimpleCursorAdapter(
    context: Context!, 
    layout: Int, 
    c: Cursor!, 
    from: Array<String!>!, 
    to: IntArray!, 
    flags: Int)
```

Standard constructor.

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android.content/Context.md)!:The context where the ListView associated with this SimpleListItemFactory is running |
| `layout` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):resource identifier of a layout file that defines the views for this list item. The layout file should include at least those named views defined in "to" |
| `c` | [Cursor](../android.database/Cursor.md)!:The database cursor. Can be null if the cursor is not available yet. |
| --- | --- |
| `from` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!:A list of column names representing the data to bind to the UI. Can be null if the cursor is not available yet. |
| `to` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!:The views that should display column in the "from" parameter. These should all be TextViews. The first N views in this list are given the values of the first N columns in the from parameter. Can be null if the cursor is not available yet. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Flags used to determine the behavior of the adapter, as per [CursorAdapter.CursorAdapter(Context, Cursor, int)](CursorAdapter.md)). |
| --- | --- |

## Public methods

### bindView

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun bindView(
    view: View!, 
    context: Context!, 
    cursor: Cursor!
): Unit
```

Binds all of the field names passed into the "to" parameter of the constructor with their corresponding cursor columns as specified in the "from" parameter. Binding occurs in two phases. First, if a [android.widget.SimpleCursorAdapter.ViewBinder](../android/widget/SimpleCursorAdapter.ViewBinder.md) is available, [ViewBinder.setViewValue(android.view.View, android.database.Cursor, int)](../android/widget/SimpleCursorAdapter.ViewBinder.md))is invoked. If the returned value is true, binding has occured. If the returned value is false and the view to bind is a TextView, [setViewText(android.widget.TextView,java.lang.String)](SimpleCursorAdapter.md))is invoked. If the returned value is false and the view to bind is an ImageView, [setViewImage(android.widget.ImageView,java.lang.String)](SimpleCursorAdapter.md))is invoked. If no appropriate binding can be found, an [IllegalStateException](../java.lang/IllegalStateException.md) is thrown.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `view` | [View](../android.view/View.md)!:Existing view, returned earlier by newView |
| `context` | [Context](../android.content/Context.md)!:Interface to application's global information |
| `cursor` | [Cursor](../android.database/Cursor.md)!:The cursor from which to get the data. The cursor is already moved to the correct position. |
| --- | --- |

| Exceptions ||
|-----------------------------------|-------------------------|
| `java.lang.IllegalStateException` | if binding cannot occur |

**See Also**

- [android.widget.CursorAdapter#bindView(android.view.View,
 * android.content.Context, android.database.Cursor)](CursorAdapter.md))
- <https://developer.android.com/reference/kotlin/android/widget/SimpleCursorAdapter#getViewBinder()>
- <https://developer.android.com/reference/kotlin/android/widget/SimpleCursorAdapter#setViewBinder(android.widget.SimpleCursorAdapter.ViewBinder)>
- [#setViewImage(ImageView, String)](SimpleCursorAdapter.md))
- [#setViewText(TextView, String)](SimpleCursorAdapter.md)) 

### changeCursorAndColumns

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun changeCursorAndColumns(
    c: Cursor!, 
    from: Array<String!>!, 
    to: IntArray!
): Unit
```

Change the cursor and change the column-to-view mappings at the same time.

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `c` | [Cursor](../android.database/Cursor.md)!:The database cursor. Can be null if the cursor is not available yet. |
| `from` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!:A list of column names representing the data to bind to the UI. Can be null if the cursor is not available yet. |
| `to` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!:The views that should display column in the "from" parameter. These should all be TextViews. The first N views in this list are given the values of the first N columns in the from parameter. Can be null if the cursor is not available yet. |
| --- | --- |

### convertToString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun convertToString(cursor: Cursor!): CharSequence!
```

Returns a CharSequence representation of the specified Cursor as defined by the current CursorToStringConverter. If no CursorToStringConverter has been set, the String conversion column is used instead. If the conversion column is -1, the returned String is empty if the cursor is null or Cursor.toString().

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------|
| `cursor` | [Cursor](../android.database/Cursor.md)!:the Cursor to convert to a CharSequence |

| Return ||
|------------------------------------------------------------------------------------------------|-------------------------------------------------|
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | a non-null CharSequence representing the cursor |

### getCursorToStringConverter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getCursorToStringConverter(): SimpleCursorAdapter.CursorToStringConverter!
```

Returns the converter used to convert the filtering Cursor into a String.

| Return ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [SimpleCursorAdapter.CursorToStringConverter](../android/widget/SimpleCursorAdapter.CursorToStringConverter.md)! | null if the converter does not exist or an instance of [android.widget.SimpleCursorAdapter.CursorToStringConverter](../android/widget/SimpleCursorAdapter.CursorToStringConverter.md) |

**See Also**

- <https://developer.android.com/reference/kotlin/android/widget/SimpleCursorAdapter#setCursorToStringConverter(android.widget.SimpleCursorAdapter.CursorToStringConverter)>
- <https://developer.android.com/reference/kotlin/android/widget/SimpleCursorAdapter#getStringConversionColumn()>
- [#setStringConversionColumn(int)](SimpleCursorAdapter.md))
- [android.widget.CursorAdapter#convertToString(android.database.Cursor)](CursorAdapter.md)) 

### getStringConversionColumn

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getStringConversionColumn(): Int
```

Return the index of the column used to get a String representation of the Cursor.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a valid index in the current Cursor or -1 |

**See Also**

- [android.widget.CursorAdapter#convertToString(android.database.Cursor)](CursorAdapter.md))
- [#setStringConversionColumn(int)](SimpleCursorAdapter.md))
- <https://developer.android.com/reference/kotlin/android/widget/SimpleCursorAdapter#setCursorToStringConverter(android.widget.SimpleCursorAdapter.CursorToStringConverter)>
- <https://developer.android.com/reference/kotlin/android/widget/SimpleCursorAdapter#getCursorToStringConverter()> 

### getViewBinder

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getViewBinder(): SimpleCursorAdapter.ViewBinder!
```

Returns the [ViewBinder](../android/widget/SimpleCursorAdapter.ViewBinder.md) used to bind data to views.

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------|
| [SimpleCursorAdapter.ViewBinder](../android/widget/SimpleCursorAdapter.ViewBinder.md)! | a ViewBinder or null if the binder does not exist |

**See Also**

- [#bindView(android.view.View, android.content.Context, android.database.Cursor)](SimpleCursorAdapter.md))
- <https://developer.android.com/reference/kotlin/android/widget/SimpleCursorAdapter#setViewBinder(android.widget.SimpleCursorAdapter.ViewBinder)> 

### setCursorToStringConverter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setCursorToStringConverter(cursorToStringConverter: SimpleCursorAdapter.CursorToStringConverter!): Unit
```

Sets the converter used to convert the filtering Cursor into a String.

| Parameters ||
|---------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `cursorToStringConverter` | [SimpleCursorAdapter.CursorToStringConverter](../android/widget/SimpleCursorAdapter.CursorToStringConverter.md)!:the Cursor to String converter, or null to remove the converter |

**See Also**

- <https://developer.android.com/reference/kotlin/android/widget/SimpleCursorAdapter#setCursorToStringConverter(android.widget.SimpleCursorAdapter.CursorToStringConverter)>
- <https://developer.android.com/reference/kotlin/android/widget/SimpleCursorAdapter#getStringConversionColumn()>
- [#setStringConversionColumn(int)](SimpleCursorAdapter.md))
- [android.widget.CursorAdapter#convertToString(android.database.Cursor)](CursorAdapter.md)) 

### setStringConversionColumn

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setStringConversionColumn(stringConversionColumn: Int): Unit
```

Defines the index of the column in the Cursor used to get a String representation of that Cursor. The column is used to convert the Cursor to a String only when the current CursorToStringConverter is null.

| Parameters ||
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `stringConversionColumn` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):a valid index in the current Cursor or -1 to use the default conversion mechanism |

**See Also**

- [android.widget.CursorAdapter#convertToString(android.database.Cursor)](CursorAdapter.md))
- <https://developer.android.com/reference/kotlin/android/widget/SimpleCursorAdapter#getStringConversionColumn()>
- <https://developer.android.com/reference/kotlin/android/widget/SimpleCursorAdapter#setCursorToStringConverter(android.widget.SimpleCursorAdapter.CursorToStringConverter)>
- <https://developer.android.com/reference/kotlin/android/widget/SimpleCursorAdapter#getCursorToStringConverter()> 

### setViewBinder

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setViewBinder(viewBinder: SimpleCursorAdapter.ViewBinder!): Unit
```

Sets the binder used to bind data to views.

| Parameters ||
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `viewBinder` | [SimpleCursorAdapter.ViewBinder](../android/widget/SimpleCursorAdapter.ViewBinder.md)!:the binder used to bind data to views, can be null to remove the existing binder |

**See Also**

- [#bindView(android.view.View, android.content.Context, android.database.Cursor)](SimpleCursorAdapter.md))
- <https://developer.android.com/reference/kotlin/android/widget/SimpleCursorAdapter#getViewBinder()> 

### setViewImage

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setViewImage(
    v: ImageView!, 
    value: String!
): Unit
```

Called by bindView() to set the image for an ImageView but only if there is no existing ViewBinder or if the existing ViewBinder cannot handle binding to an ImageView. By default, the value will be treated as an image resource. If the value cannot be used as an image resource, the value is used as an image Uri. Intended to be overridden by Adapters that need to filter strings retrieved from the database.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------|
| `v` | [ImageView](ImageView.md)!:ImageView to receive an image |
| `value` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the value retrieved from the cursor |

### setViewText

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setViewText(
    v: TextView!, 
    text: String!
): Unit
```

Called by bindView() to set the text for a TextView but only if there is no existing ViewBinder or if the existing ViewBinder cannot handle binding to a TextView. Intended to be overridden by Adapters that need to filter strings retrieved from the database.

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------------------|
| `v` | [TextView](TextView.md)!:TextView to receive text |
| `text` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the text to be set for the TextView |

### swapCursor

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun swapCursor(c: Cursor!): Cursor!
```

| Parameters ||
|-------------|----------------------------|
| `newCursor` | The new cursor to be used. |

| Return ||
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Cursor](../android.database/Cursor.md)! | Returns the previously set Cursor, or null if there was not one. If the given new Cursor is the same instance is the previously set Cursor, null is also returned. |
