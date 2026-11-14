# SimpleCursorAdapter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SimpleCursorAdapter

Kotlin| [Java](https://developer.android.com/reference/android/widget/SimpleCursorAdapter "View this page in Java") 

```
open class SimpleCursorAdapter : ResourceCursorAdapter
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| ↳ | [android.widget.BaseAdapter](https://developer.android.com/reference/kotlin/android/widget/BaseAdapter) ||||
| | ↳ | [android.widget.CursorAdapter](https://developer.android.com/reference/kotlin/android/widget/CursorAdapter) |||
| | | ↳ | [android.widget.ResourceCursorAdapter](https://developer.android.com/reference/kotlin/android/widget/ResourceCursorAdapter) ||
| | | | ↳ | [android.widget.SimpleCursorAdapter](https://developer.android.com/reference/kotlin/android/widget/SimpleCursorAdapter#) |

An easy adapter to map columns from a cursor to TextViews or ImageViews defined in an XML file. You can specify which columns you want, which views you want to display the columns, and the XML file that defines the appearance of these views. Binding occurs in two phases. First, if a [android.widget.SimpleCursorAdapter.ViewBinder](https://developer.android.com/reference/kotlin/android/widget/SimpleCursorAdapter.ViewBinder) is available, [ViewBinder.setViewValue(android.view.View, android.database.Cursor, int)](https://developer.android.com/reference/kotlin/android/widget/SimpleCursorAdapter.ViewBinder#setViewValue(android.view.View,%20android.database.Cursor,%20kotlin.Int))is invoked. If the returned value is true, binding has occured. If the returned value is false and the view to bind is a TextView, [setViewText(android.widget.TextView,java.lang.String)](https://developer.android.com/reference/kotlin/android/widget/SimpleCursorAdapter#setViewText(android.widget.TextView,%20kotlin.String))is invoked. If the returned value is false and the view to bind is an ImageView, [setViewImage(android.widget.ImageView,java.lang.String)](https://developer.android.com/reference/kotlin/android/widget/SimpleCursorAdapter#setViewImage(android.widget.ImageView,%20kotlin.String))is invoked. If no appropriate binding can be found, an [IllegalStateException](https://developer.android.com/reference/kotlin/java/lang/IllegalStateException.html#) is thrown. If this adapter is used with filtering, for instance in an [android.widget.AutoCompleteTextView](https://developer.android.com/reference/kotlin/android/widget/AutoCompleteTextView), you can use the [android.widget.SimpleCursorAdapter.CursorToStringConverter](https://developer.android.com/reference/kotlin/android/widget/SimpleCursorAdapter.CursorToStringConverter) and the [android.widget.FilterQueryProvider](https://developer.android.com/reference/kotlin/android/widget/FilterQueryProvider) interfaces to get control over the filtering process. You can refer to [convertToString(android.database.Cursor)](https://developer.android.com/reference/kotlin/android/widget/SimpleCursorAdapter#convertToString(android.database.Cursor))and [runQueryOnBackgroundThread(java.lang.CharSequence)](https://developer.android.com/reference/kotlin/android/widget/CursorAdapter#runQueryOnBackgroundThread(kotlin.CharSequence))for more information.

## Summary

| Nested classes ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [CursorToStringConverter](https://developer.android.com/reference/kotlin/android/widget/SimpleCursorAdapter.CursorToStringConverter) This class can be used by external clients of SimpleCursorAdapter to define how the Cursor should be converted to a String. |
| abstract | [ViewBinder](https://developer.android.com/reference/kotlin/android/widget/SimpleCursorAdapter.ViewBinder) This class can be used by external clients of SimpleCursorAdapter to bind values fom the Cursor to views. |

| Inherited constants ||
|---|---|
| From class [CursorAdapter](https://developer.android.com/reference/kotlin/android/widget/CursorAdapter) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FLAG_AUTO_REQUERY](https://developer.android.com/reference/kotlin/android/widget/CursorAdapter#FLAG_AUTO_REQUERY:kotlin.Int) <br /> If set the adapter will call requery() on the cursor whenever a content change notification is delivered. Implies [FLAG_REGISTER_CONTENT_OBSERVER](https://developer.android.com/reference/kotlin/android/widget/CursorAdapter#FLAG_REGISTER_CONTENT_OBSERVER:kotlin.Int). <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FLAG_REGISTER_CONTENT_OBSERVER](https://developer.android.com/reference/kotlin/android/widget/CursorAdapter#FLAG_REGISTER_CONTENT_OBSERVER:kotlin.Int) <br /> If set the adapter will register a content observer on the cursor and will call [onContentChanged()](https://developer.android.com/reference/kotlin/android/widget/CursorAdapter#onContentChanged())when a notification comes in. Be careful when using this flag: you will need to unset the current Cursor from the adapter to avoid leaks due to its registered observers. This flag is not needed when using a CursorAdapter with a [android.content.CursorLoader](https://developer.android.com/reference/kotlin/android/content/CursorLoader.html#). <br /> | ||

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SimpleCursorAdapter](https://developer.android.com/reference/kotlin/android/widget/SimpleCursorAdapter#SimpleCursorAdapter(android.content.Context,%20kotlin.Int,%20android.database.Cursor,%20kotlin.Array,%20kotlin.IntArray))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`, `layout:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `c:` ` [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#)!`, `from:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`, `to:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!`)` Constructor the enables auto-requery. |
| [SimpleCursorAdapter](https://developer.android.com/reference/kotlin/android/widget/SimpleCursorAdapter#SimpleCursorAdapter(android.content.Context,%20kotlin.Int,%20android.database.Cursor,%20kotlin.Array,%20kotlin.IntArray,%20kotlin.Int))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`, `layout:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `c:` ` [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#)!`, `from:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`, `to:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Standard constructor. |

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [bindView](https://developer.android.com/reference/kotlin/android/widget/SimpleCursorAdapter#bindView(android.view.View,%20android.content.Context,%20android.database.Cursor))`(`view:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!`, `context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`, `cursor:` ` [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#)!`)` Binds all of the field names passed into the "to" parameter of the constructor with their corresponding cursor columns as specified in the "from" parameter. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [changeCursorAndColumns](https://developer.android.com/reference/kotlin/android/widget/SimpleCursorAdapter#changeCursorAndColumns(android.database.Cursor,%20kotlin.Array,%20kotlin.IntArray))`(`c:` ` [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#)!`, `from:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`, `to:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!`)` Change the cursor and change the column-to-view mappings at the same time. |
| open [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | [convertToString](https://developer.android.com/reference/kotlin/android/widget/SimpleCursorAdapter#convertToString(android.database.Cursor))`(`cursor:` ` [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#)!`)` Returns a CharSequence representation of the specified Cursor as defined by the current CursorToStringConverter. |
| open [SimpleCursorAdapter.CursorToStringConverter](https://developer.android.com/reference/kotlin/android/widget/SimpleCursorAdapter.CursorToStringConverter)! | [getCursorToStringConverter](https://developer.android.com/reference/kotlin/android/widget/SimpleCursorAdapter#getCursorToStringConverter())`()` Returns the converter used to convert the filtering Cursor into a String. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getStringConversionColumn](https://developer.android.com/reference/kotlin/android/widget/SimpleCursorAdapter#getStringConversionColumn())`()` Return the index of the column used to get a String representation of the Cursor. |
| open [SimpleCursorAdapter.ViewBinder](https://developer.android.com/reference/kotlin/android/widget/SimpleCursorAdapter.ViewBinder)! | [getViewBinder](https://developer.android.com/reference/kotlin/android/widget/SimpleCursorAdapter#getViewBinder())`()` Returns the [ViewBinder](https://developer.android.com/reference/kotlin/android/widget/SimpleCursorAdapter.ViewBinder) used to bind data to views. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setCursorToStringConverter](https://developer.android.com/reference/kotlin/android/widget/SimpleCursorAdapter#setCursorToStringConverter(android.widget.SimpleCursorAdapter.CursorToStringConverter))`(`cursorToStringConverter:` ` [SimpleCursorAdapter.CursorToStringConverter](https://developer.android.com/reference/kotlin/android/widget/SimpleCursorAdapter.CursorToStringConverter)!`)` Sets the converter used to convert the filtering Cursor into a String. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setStringConversionColumn](https://developer.android.com/reference/kotlin/android/widget/SimpleCursorAdapter#setStringConversionColumn(kotlin.Int))`(`stringConversionColumn:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Defines the index of the column in the Cursor used to get a String representation of that Cursor. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setViewBinder](https://developer.android.com/reference/kotlin/android/widget/SimpleCursorAdapter#setViewBinder(android.widget.SimpleCursorAdapter.ViewBinder))`(`viewBinder:` ` [SimpleCursorAdapter.ViewBinder](https://developer.android.com/reference/kotlin/android/widget/SimpleCursorAdapter.ViewBinder)!`)` Sets the binder used to bind data to views. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setViewImage](https://developer.android.com/reference/kotlin/android/widget/SimpleCursorAdapter#setViewImage(android.widget.ImageView,%20kotlin.String))`(`v:` ` [ImageView](https://developer.android.com/reference/kotlin/android/widget/ImageView)!`, `value:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Called by bindView() to set the image for an ImageView but only if there is no existing ViewBinder or if the existing ViewBinder cannot handle binding to an ImageView. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setViewText](https://developer.android.com/reference/kotlin/android/widget/SimpleCursorAdapter#setViewText(android.widget.TextView,%20kotlin.String))`(`v:` ` [TextView](https://developer.android.com/reference/kotlin/android/widget/TextView)!`, `text:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Called by bindView() to set the text for a TextView but only if there is no existing ViewBinder or if the existing ViewBinder cannot handle binding to a TextView. |
| open [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#)! | [swapCursor](https://developer.android.com/reference/kotlin/android/widget/SimpleCursorAdapter#swapCursor(android.database.Cursor))`(`c:` ` [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#)!`)` <br /> |

| Inherited functions ||
|---|---|
| From class [BaseAdapter](https://developer.android.com/reference/kotlin/android/widget/BaseAdapter) |---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [areAllItemsEnabled](https://developer.android.com/reference/kotlin/android/widget/BaseAdapter#areAllItemsEnabled())`()` <br /> | | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!>? | [getAutofillOptions](https://developer.android.com/reference/kotlin/android/widget/BaseAdapter#getAutofillOptions())`()` <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getItemViewType](https://developer.android.com/reference/kotlin/android/widget/BaseAdapter#getItemViewType(kotlin.Int))`(`position:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getViewTypeCount](https://developer.android.com/reference/kotlin/android/widget/BaseAdapter#getViewTypeCount())`()` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEmpty](https://developer.android.com/reference/kotlin/android/widget/BaseAdapter#isEmpty())`()` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEnabled](https://developer.android.com/reference/kotlin/android/widget/BaseAdapter#isEnabled(kotlin.Int))`(`position:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [notifyDataSetChanged](https://developer.android.com/reference/kotlin/android/widget/BaseAdapter#notifyDataSetChanged())`()` <br /> Notifies the attached observers that the underlying data has been changed and any View reflecting the data set should refresh itself. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [notifyDataSetInvalidated](https://developer.android.com/reference/kotlin/android/widget/BaseAdapter#notifyDataSetInvalidated())`()` <br /> Notifies the attached observers that the underlying data is no longer valid or available. Once invoked this adapter is no longer valid and should not report further data set changes. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerDataSetObserver](https://developer.android.com/reference/kotlin/android/widget/BaseAdapter#registerDataSetObserver(android.database.DataSetObserver))`(`observer:` ` [DataSetObserver](https://developer.android.com/reference/kotlin/android/database/DataSetObserver.html#)!`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAutofillOptions](https://developer.android.com/reference/kotlin/android/widget/BaseAdapter#setAutofillOptions(kotlin.CharSequence))`(`vararg` `options:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` <br /> Sets the value returned by [getAutofillOptions()](https://developer.android.com/reference/kotlin/android/widget/BaseAdapter#getAutofillOptions()) <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unregisterDataSetObserver](https://developer.android.com/reference/kotlin/android/widget/BaseAdapter#unregisterDataSetObserver(android.database.DataSetObserver))`(`observer:` ` [DataSetObserver](https://developer.android.com/reference/kotlin/android/database/DataSetObserver.html#)!`)` <br /> | ||
| From class [CursorAdapter](https://developer.android.com/reference/kotlin/android/widget/CursorAdapter) |--------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [bindView](https://developer.android.com/reference/kotlin/android/widget/CursorAdapter#bindView(android.view.View,%20android.content.Context,%20android.database.Cursor))`(`view:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!`, `context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`, `cursor:` ` [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#)!`)` <br /> Bind an existing view to the data pointed to by cursor <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [changeCursor](https://developer.android.com/reference/kotlin/android/widget/CursorAdapter#changeCursor(android.database.Cursor))`(`cursor:` ` [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#)!`)` <br /> Change the underlying cursor to a new cursor. If there is an existing cursor it will be closed. <br /> | | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | [convertToString](https://developer.android.com/reference/kotlin/android/widget/CursorAdapter#convertToString(android.database.Cursor))`(`cursor:` ` [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#)!`)` <br /> Converts the cursor into a CharSequence. Subclasses should override this method to convert their results. The default implementation returns an empty String for null values or the default String representation of the value. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getCount](https://developer.android.com/reference/kotlin/android/widget/CursorAdapter#getCount())`()` <br /> | | [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#)! | [getCursor](https://developer.android.com/reference/kotlin/android/widget/CursorAdapter#getCursor())`()` <br /> Returns the cursor. <br /> | | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)! | [getDropDownView](https://developer.android.com/reference/kotlin/android/widget/CursorAdapter#getDropDownView(kotlin.Int,%20android.view.View,%20android.view.ViewGroup))`(`position:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `convertView:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!`, `parent:` ` [ViewGroup](https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#)!`)` <br /> | | [Resources.Theme](https://developer.android.com/reference/kotlin/android/content/res/Resources.Theme.html#)? | [getDropDownViewTheme](https://developer.android.com/reference/kotlin/android/widget/CursorAdapter#getDropDownViewTheme())`()` <br /> | | [Filter](https://developer.android.com/reference/kotlin/android/widget/Filter)! | [getFilter](https://developer.android.com/reference/kotlin/android/widget/CursorAdapter#getFilter())`()` <br /> | | [FilterQueryProvider](https://developer.android.com/reference/kotlin/android/widget/FilterQueryProvider)! | [getFilterQueryProvider](https://developer.android.com/reference/kotlin/android/widget/CursorAdapter#getFilterQueryProvider())`()` <br /> Returns the query filter provider used for filtering. When the provider is null, no filtering occurs. <br /> | | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getItem](https://developer.android.com/reference/kotlin/android/widget/CursorAdapter#getItem(kotlin.Int))`(`position:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> | | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getItemId](https://developer.android.com/reference/kotlin/android/widget/CursorAdapter#getItemId(kotlin.Int))`(`position:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> | | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)! | [getView](https://developer.android.com/reference/kotlin/android/widget/CursorAdapter#getView(kotlin.Int,%20android.view.View,%20android.view.ViewGroup))`(`position:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `convertView:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!`, `parent:` ` [ViewGroup](https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#)!`)` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasStableIds](https://developer.android.com/reference/kotlin/android/widget/CursorAdapter#hasStableIds())`()` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [init](https://developer.android.com/reference/kotlin/android/widget/CursorAdapter#init(android.content.Context,%20android.database.Cursor,%20kotlin.Boolean))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`, `c:` ` [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#)!`, `autoRequery:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onContentChanged](https://developer.android.com/reference/kotlin/android/widget/CursorAdapter#onContentChanged())`()` <br /> Called when the [ContentObserver](https://developer.android.com/reference/kotlin/android/database/ContentObserver.html#) on the cursor receives a change notification. The default implementation provides the auto-requery logic, but may be overridden by sub classes. <br /> | | [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#)! | [runQueryOnBackgroundThread](https://developer.android.com/reference/kotlin/android/widget/CursorAdapter#runQueryOnBackgroundThread(kotlin.CharSequence))`(`constraint:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` <br /> Runs a query with the specified constraint. This query is requested by the filter attached to this adapter. The query is provided by a [android.widget.FilterQueryProvider](https://developer.android.com/reference/kotlin/android/widget/FilterQueryProvider). If no provider is specified, the current cursor is not filtered and returned. After this method returns the resulting cursor is passed to [changeCursor(android.database.Cursor)](https://developer.android.com/reference/kotlin/android/widget/CursorAdapter#changeCursor(android.database.Cursor))and the previous cursor is closed. This method is always executed on a background thread, not on the application's main thread (or UI thread.) Contract: when constraint is null or empty, the original results, prior to any filtering, must be returned. This method may take several seconds to complete, so it should only be called from a worker thread. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFilterQueryProvider](https://developer.android.com/reference/kotlin/android/widget/CursorAdapter#setFilterQueryProvider(android.widget.FilterQueryProvider))`(`filterQueryProvider:` ` [FilterQueryProvider](https://developer.android.com/reference/kotlin/android/widget/FilterQueryProvider)!`)` <br /> Sets the query filter provider used to filter the current Cursor. The provider's [android.widget.FilterQueryProvider#runQuery(CharSequence)](https://developer.android.com/reference/kotlin/android/widget/FilterQueryProvider#runQuery(kotlin.CharSequence))method is invoked when filtering is requested by a client of this adapter. <br /> | | [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#)! | [swapCursor](https://developer.android.com/reference/kotlin/android/widget/CursorAdapter#swapCursor(android.database.Cursor))`(`newCursor:` ` [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#)!`)` <br /> Swap in a new Cursor, returning the old Cursor. Unlike [changeCursor(android.database.Cursor)](https://developer.android.com/reference/kotlin/android/widget/CursorAdapter#changeCursor(android.database.Cursor)), the returned old Cursor is*not*closed. <br /> | ||
| From class [ResourceCursorAdapter](https://developer.android.com/reference/kotlin/android/widget/ResourceCursorAdapter) |---------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)! | [newDropDownView](https://developer.android.com/reference/kotlin/android/widget/ResourceCursorAdapter#newDropDownView(android.content.Context,%20android.database.Cursor,%20android.view.ViewGroup))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`, `cursor:` ` [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#)!`, `parent:` ` [ViewGroup](https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#)!`)` <br /> | | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)! | [newView](https://developer.android.com/reference/kotlin/android/widget/ResourceCursorAdapter#newView(android.content.Context,%20android.database.Cursor,%20android.view.ViewGroup))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`, `cursor:` ` [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#)!`, `parent:` ` [ViewGroup](https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#)!`)` <br /> Inflates view(s) from the specified XML file. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDropDownViewResource](https://developer.android.com/reference/kotlin/android/widget/ResourceCursorAdapter#setDropDownViewResource(kotlin.Int))`(`dropDownLayout:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Sets the layout resource of the drop down views. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDropDownViewTheme](https://developer.android.com/reference/kotlin/android/widget/ResourceCursorAdapter#setDropDownViewTheme(android.content.res.Resources.Theme))`(`theme:` ` [Resources.Theme](https://developer.android.com/reference/kotlin/android/content/res/Resources.Theme.html#)?`)` <br /> Sets the [android.content.res.Resources.Theme](https://developer.android.com/reference/kotlin/android/content/res/Resources.Theme.html#) against which drop-down views are inflated. By default, drop-down views are inflated against the theme of the [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#) passed to the adapter's constructor. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setViewResource](https://developer.android.com/reference/kotlin/android/widget/ResourceCursorAdapter#setViewResource(kotlin.Int))`(`layout:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Sets the layout resource of the item views. <br /> | ||

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

**Deprecated:** *This option is discouraged, as it results in Cursor queries being performed on the application's UI thread and thus can cause poor responsiveness or even Application Not Responding errors. As an alternative, use [android.app.LoaderManager](https://developer.android.com/reference/kotlin/android/app/LoaderManager.html#) with a [android.content.CursorLoader](https://developer.android.com/reference/kotlin/android/content/CursorLoader.html#).*

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
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!:The context where the ListView associated with this SimpleListItemFactory is running |
| `layout` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):resource identifier of a layout file that defines the views for this list item. The layout file should include at least those named views defined in "to" |
| `c` | [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#)!:The database cursor. Can be null if the cursor is not available yet. |
| `from` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!:A list of column names representing the data to bind to the UI. Can be null if the cursor is not available yet. |
| `to` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!:The views that should display column in the "from" parameter. These should all be TextViews. The first N views in this list are given the values of the first N columns in the from parameter. Can be null if the cursor is not available yet. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Flags used to determine the behavior of the adapter, as per [CursorAdapter.CursorAdapter(Context, Cursor, int)](https://developer.android.com/reference/kotlin/android/widget/CursorAdapter#CursorAdapter(android.content.Context,%20android.database.Cursor,%20kotlin.Int)). |

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

Binds all of the field names passed into the "to" parameter of the constructor with their corresponding cursor columns as specified in the "from" parameter. Binding occurs in two phases. First, if a [android.widget.SimpleCursorAdapter.ViewBinder](https://developer.android.com/reference/kotlin/android/widget/SimpleCursorAdapter.ViewBinder) is available, [ViewBinder.setViewValue(android.view.View, android.database.Cursor, int)](https://developer.android.com/reference/kotlin/android/widget/SimpleCursorAdapter.ViewBinder#setViewValue(android.view.View,%20android.database.Cursor,%20kotlin.Int))is invoked. If the returned value is true, binding has occured. If the returned value is false and the view to bind is a TextView, [setViewText(android.widget.TextView,java.lang.String)](https://developer.android.com/reference/kotlin/android/widget/SimpleCursorAdapter#setViewText(android.widget.TextView,%20kotlin.String))is invoked. If the returned value is false and the view to bind is an ImageView, [setViewImage(android.widget.ImageView,java.lang.String)](https://developer.android.com/reference/kotlin/android/widget/SimpleCursorAdapter#setViewImage(android.widget.ImageView,%20kotlin.String))is invoked. If no appropriate binding can be found, an [IllegalStateException](https://developer.android.com/reference/kotlin/java/lang/IllegalStateException.html#) is thrown.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `view` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!:Existing view, returned earlier by newView |
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!:Interface to application's global information |
| `cursor` | [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#)!:The cursor from which to get the data. The cursor is already moved to the correct position. |

| Exceptions ||
|-----------------------------------|-------------------------|
| `java.lang.IllegalStateException` | if binding cannot occur |

**See Also**

- [android.widget.CursorAdapter#bindView(android.view.View,
 * android.content.Context, android.database.Cursor)](https://developer.android.com/reference/kotlin/android/widget/CursorAdapter#bindView(android.view.View,%20android.content.Context,%20android.database.Cursor))
- <https://developer.android.com/reference/kotlin/android/widget/SimpleCursorAdapter#getViewBinder()>
- <https://developer.android.com/reference/kotlin/android/widget/SimpleCursorAdapter#setViewBinder(android.widget.SimpleCursorAdapter.ViewBinder)>
- [#setViewImage(ImageView, String)](https://developer.android.com/reference/kotlin/android/widget/SimpleCursorAdapter#setViewImage(android.widget.ImageView,%20kotlin.String))
- [#setViewText(TextView, String)](https://developer.android.com/reference/kotlin/android/widget/SimpleCursorAdapter#setViewText(android.widget.TextView,%20kotlin.String)) 

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
| `c` | [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#)!:The database cursor. Can be null if the cursor is not available yet. |
| `from` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!:A list of column names representing the data to bind to the UI. Can be null if the cursor is not available yet. |
| `to` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!:The views that should display column in the "from" parameter. These should all be TextViews. The first N views in this list are given the values of the first N columns in the from parameter. Can be null if the cursor is not available yet. |

### convertToString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun convertToString(cursor: Cursor!): CharSequence!
```

Returns a CharSequence representation of the specified Cursor as defined by the current CursorToStringConverter. If no CursorToStringConverter has been set, the String conversion column is used instead. If the conversion column is -1, the returned String is empty if the cursor is null or Cursor.toString().

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------|
| `cursor` | [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#)!:the Cursor to convert to a CharSequence |

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
| [SimpleCursorAdapter.CursorToStringConverter](https://developer.android.com/reference/kotlin/android/widget/SimpleCursorAdapter.CursorToStringConverter)! | null if the converter does not exist or an instance of [android.widget.SimpleCursorAdapter.CursorToStringConverter](https://developer.android.com/reference/kotlin/android/widget/SimpleCursorAdapter.CursorToStringConverter) |

**See Also**

- <https://developer.android.com/reference/kotlin/android/widget/SimpleCursorAdapter#setCursorToStringConverter(android.widget.SimpleCursorAdapter.CursorToStringConverter)>
- <https://developer.android.com/reference/kotlin/android/widget/SimpleCursorAdapter#getStringConversionColumn()>
- [#setStringConversionColumn(int)](https://developer.android.com/reference/kotlin/android/widget/SimpleCursorAdapter#setStringConversionColumn(kotlin.Int))
- [android.widget.CursorAdapter#convertToString(android.database.Cursor)](https://developer.android.com/reference/kotlin/android/widget/CursorAdapter#convertToString(android.database.Cursor)) 

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

- [android.widget.CursorAdapter#convertToString(android.database.Cursor)](https://developer.android.com/reference/kotlin/android/widget/CursorAdapter#convertToString(android.database.Cursor))
- [#setStringConversionColumn(int)](https://developer.android.com/reference/kotlin/android/widget/SimpleCursorAdapter#setStringConversionColumn(kotlin.Int))
- <https://developer.android.com/reference/kotlin/android/widget/SimpleCursorAdapter#setCursorToStringConverter(android.widget.SimpleCursorAdapter.CursorToStringConverter)>
- <https://developer.android.com/reference/kotlin/android/widget/SimpleCursorAdapter#getCursorToStringConverter()> 

### getViewBinder

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getViewBinder(): SimpleCursorAdapter.ViewBinder!
```

Returns the [ViewBinder](https://developer.android.com/reference/kotlin/android/widget/SimpleCursorAdapter.ViewBinder) used to bind data to views.

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------|
| [SimpleCursorAdapter.ViewBinder](https://developer.android.com/reference/kotlin/android/widget/SimpleCursorAdapter.ViewBinder)! | a ViewBinder or null if the binder does not exist |

**See Also**

- [#bindView(android.view.View, android.content.Context, android.database.Cursor)](https://developer.android.com/reference/kotlin/android/widget/SimpleCursorAdapter#bindView(android.view.View,%20android.content.Context,%20android.database.Cursor))
- <https://developer.android.com/reference/kotlin/android/widget/SimpleCursorAdapter#setViewBinder(android.widget.SimpleCursorAdapter.ViewBinder)> 

### setCursorToStringConverter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setCursorToStringConverter(cursorToStringConverter: SimpleCursorAdapter.CursorToStringConverter!): Unit
```

Sets the converter used to convert the filtering Cursor into a String.

| Parameters ||
|---------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `cursorToStringConverter` | [SimpleCursorAdapter.CursorToStringConverter](https://developer.android.com/reference/kotlin/android/widget/SimpleCursorAdapter.CursorToStringConverter)!:the Cursor to String converter, or null to remove the converter |

**See Also**

- <https://developer.android.com/reference/kotlin/android/widget/SimpleCursorAdapter#setCursorToStringConverter(android.widget.SimpleCursorAdapter.CursorToStringConverter)>
- <https://developer.android.com/reference/kotlin/android/widget/SimpleCursorAdapter#getStringConversionColumn()>
- [#setStringConversionColumn(int)](https://developer.android.com/reference/kotlin/android/widget/SimpleCursorAdapter#setStringConversionColumn(kotlin.Int))
- [android.widget.CursorAdapter#convertToString(android.database.Cursor)](https://developer.android.com/reference/kotlin/android/widget/CursorAdapter#convertToString(android.database.Cursor)) 

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

- [android.widget.CursorAdapter#convertToString(android.database.Cursor)](https://developer.android.com/reference/kotlin/android/widget/CursorAdapter#convertToString(android.database.Cursor))
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
| `viewBinder` | [SimpleCursorAdapter.ViewBinder](https://developer.android.com/reference/kotlin/android/widget/SimpleCursorAdapter.ViewBinder)!:the binder used to bind data to views, can be null to remove the existing binder |

**See Also**

- [#bindView(android.view.View, android.content.Context, android.database.Cursor)](https://developer.android.com/reference/kotlin/android/widget/SimpleCursorAdapter#bindView(android.view.View,%20android.content.Context,%20android.database.Cursor))
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
| `v` | [ImageView](https://developer.android.com/reference/kotlin/android/widget/ImageView)!:ImageView to receive an image |
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
| `v` | [TextView](https://developer.android.com/reference/kotlin/android/widget/TextView)!:TextView to receive text |
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
| [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#)! | Returns the previously set Cursor, or null if there was not one. If the given new Cursor is the same instance is the previously set Cursor, null is also returned. |
