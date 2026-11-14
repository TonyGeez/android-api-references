# ResourceCursorAdapter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ResourceCursorAdapter

Kotlin | [Java](https://developer.android.com/reference/android/widget/ResourceCursorAdapter "View this page in Java") 

```
abstract class ResourceCursorAdapter : CursorAdapter
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| ↳ | [android.widget.BaseAdapter](https://developer.android.com/reference/kotlin/android/widget/BaseAdapter) |||
| | ↳ | [android.widget.CursorAdapter](https://developer.android.com/reference/kotlin/android/widget/CursorAdapter) ||
| | | ↳ | [android.widget.ResourceCursorAdapter](https://developer.android.com/reference/kotlin/android/widget/ResourceCursorAdapter#) |

| Known Direct Subclasses [SimpleCursorAdapter](https://developer.android.com/reference/kotlin/android/widget/SimpleCursorAdapter) |----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------| | [SimpleCursorAdapter](https://developer.android.com/reference/kotlin/android/widget/SimpleCursorAdapter) | An easy adapter to map columns from a cursor to TextViews or ImageViews defined in an XML file. | |

An easy adapter that creates views defined in an XML file. You can specify the XML file that defines the appearance of the views.

## Summary

| Inherited constants ||
|---|---|
| From class [CursorAdapter](https://developer.android.com/reference/kotlin/android/widget/CursorAdapter) |----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FLAG_AUTO_REQUERY](https://developer.android.com/reference/kotlin/android/widget/CursorAdapter#FLAG_AUTO_REQUERY:kotlin.Int) If set the adapter will call requery() on the cursor whenever a content change notification is delivered. Implies [FLAG_REGISTER_CONTENT_OBSERVER](https://developer.android.com/reference/kotlin/android/widget/CursorAdapter#FLAG_REGISTER_CONTENT_OBSERVER:kotlin.Int). <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FLAG_REGISTER_CONTENT_OBSERVER](https://developer.android.com/reference/kotlin/android/widget/CursorAdapter#FLAG_REGISTER_CONTENT_OBSERVER:kotlin.Int) If set the adapter will register a content observer on the cursor and will call [onContentChanged()](https://developer.android.com/reference/kotlin/android/widget/CursorAdapter#onContentChanged()) when a notification comes in. Be careful when using this flag: you will need to unset the current Cursor from the adapter to avoid leaks due to its registered observers. This flag is not needed when using a CursorAdapter with a [android.content.CursorLoader](https://developer.android.com/reference/kotlin/android/content/CursorLoader.html#). <br /> | ||

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ResourceCursorAdapter](https://developer.android.com/reference/kotlin/android/widget/ResourceCursorAdapter#ResourceCursorAdapter(android.content.Context,%20kotlin.Int,%20android.database.Cursor))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`, `layout:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `c:` ` [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#)!`)` Constructor the enables auto-requery. |
| [ResourceCursorAdapter](https://developer.android.com/reference/kotlin/android/widget/ResourceCursorAdapter#ResourceCursorAdapter(android.content.Context,%20kotlin.Int,%20android.database.Cursor,%20kotlin.Boolean))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`, `layout:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `c:` ` [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#)!`, `autoRequery:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Constructor with default behavior as per [CursorAdapter.CursorAdapter(Context, Cursor, boolean)](https://developer.android.com/reference/kotlin/android/widget/CursorAdapter#CursorAdapter(android.content.Context,%20android.database.Cursor,%20kotlin.Boolean)); it is recommended you not use this, but instead [ResourceCursorAdapter(android.content.Context,int,android.database.Cursor,int)](https://developer.android.com/reference/kotlin/android/widget/ResourceCursorAdapter#ResourceCursorAdapter(android.content.Context,%20kotlin.Int,%20android.database.Cursor,%20kotlin.Int)). |
| [ResourceCursorAdapter](https://developer.android.com/reference/kotlin/android/widget/ResourceCursorAdapter#ResourceCursorAdapter(android.content.Context,%20kotlin.Int,%20android.database.Cursor,%20kotlin.Int))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`, `layout:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `c:` ` [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#)!`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Standard constructor. |

| Public methods ||
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [View](https://developer.android.com/reference/kotlin/android/view/View.html#)! | [newDropDownView](https://developer.android.com/reference/kotlin/android/widget/ResourceCursorAdapter#newDropDownView(android.content.Context,%20android.database.Cursor,%20android.view.ViewGroup))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`, `cursor:` ` [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#)!`, `parent:` ` [ViewGroup](https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#)!`)` <br /> |
| open [View](https://developer.android.com/reference/kotlin/android/view/View.html#)! | [newView](https://developer.android.com/reference/kotlin/android/widget/ResourceCursorAdapter#newView(android.content.Context,%20android.database.Cursor,%20android.view.ViewGroup))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`, `cursor:` ` [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#)!`, `parent:` ` [ViewGroup](https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#)!`)` Inflates view(s) from the specified XML file. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDropDownViewResource](https://developer.android.com/reference/kotlin/android/widget/ResourceCursorAdapter#setDropDownViewResource(kotlin.Int))`(`dropDownLayout:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the layout resource of the drop down views. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDropDownViewTheme](https://developer.android.com/reference/kotlin/android/widget/ResourceCursorAdapter#setDropDownViewTheme(android.content.res.Resources.Theme))`(`theme:` ` [Resources.Theme](https://developer.android.com/reference/kotlin/android/content/res/Resources.Theme.html#)?`)` Sets the [android.content.res.Resources.Theme](https://developer.android.com/reference/kotlin/android/content/res/Resources.Theme.html#) against which drop-down views are inflated. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setViewResource](https://developer.android.com/reference/kotlin/android/widget/ResourceCursorAdapter#setViewResource(kotlin.Int))`(`layout:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the layout resource of the item views. |

| Inherited functions ||
|---|---|
| From class [BaseAdapter](https://developer.android.com/reference/kotlin/android/widget/BaseAdapter) |---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [areAllItemsEnabled](https://developer.android.com/reference/kotlin/android/widget/BaseAdapter#areAllItemsEnabled())`()` <br /> | | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!>? | [getAutofillOptions](https://developer.android.com/reference/kotlin/android/widget/BaseAdapter#getAutofillOptions())`()` <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getItemViewType](https://developer.android.com/reference/kotlin/android/widget/BaseAdapter#getItemViewType(kotlin.Int))`(`position:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getViewTypeCount](https://developer.android.com/reference/kotlin/android/widget/BaseAdapter#getViewTypeCount())`()` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEmpty](https://developer.android.com/reference/kotlin/android/widget/BaseAdapter#isEmpty())`()` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEnabled](https://developer.android.com/reference/kotlin/android/widget/BaseAdapter#isEnabled(kotlin.Int))`(`position:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [notifyDataSetChanged](https://developer.android.com/reference/kotlin/android/widget/BaseAdapter#notifyDataSetChanged())`()` Notifies the attached observers that the underlying data has been changed and any View reflecting the data set should refresh itself. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [notifyDataSetInvalidated](https://developer.android.com/reference/kotlin/android/widget/BaseAdapter#notifyDataSetInvalidated())`()` Notifies the attached observers that the underlying data is no longer valid or available. Once invoked this adapter is no longer valid and should not report further data set changes. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerDataSetObserver](https://developer.android.com/reference/kotlin/android/widget/BaseAdapter#registerDataSetObserver(android.database.DataSetObserver))`(`observer:` ` [DataSetObserver](https://developer.android.com/reference/kotlin/android/database/DataSetObserver.html#)!`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAutofillOptions](https://developer.android.com/reference/kotlin/android/widget/BaseAdapter#setAutofillOptions(kotlin.CharSequence))`(`vararg` `options:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` Sets the value returned by [getAutofillOptions()](https://developer.android.com/reference/kotlin/android/widget/BaseAdapter#getAutofillOptions()) <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unregisterDataSetObserver](https://developer.android.com/reference/kotlin/android/widget/BaseAdapter#unregisterDataSetObserver(android.database.DataSetObserver))`(`observer:` ` [DataSetObserver](https://developer.android.com/reference/kotlin/android/database/DataSetObserver.html#)!`)` <br /> | ||
| From class [CursorAdapter](https://developer.android.com/reference/kotlin/android/widget/CursorAdapter) |--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [bindView](https://developer.android.com/reference/kotlin/android/widget/CursorAdapter#bindView(android.view.View,%20android.content.Context,%20android.database.Cursor))`(`view:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!`, `context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`, `cursor:` ` [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#)!`)` Bind an existing view to the data pointed to by cursor <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [changeCursor](https://developer.android.com/reference/kotlin/android/widget/CursorAdapter#changeCursor(android.database.Cursor))`(`cursor:` ` [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#)!`)` Change the underlying cursor to a new cursor. If there is an existing cursor it will be closed. <br /> | | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | [convertToString](https://developer.android.com/reference/kotlin/android/widget/CursorAdapter#convertToString(android.database.Cursor))`(`cursor:` ` [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#)!`)` Converts the cursor into a CharSequence. Subclasses should override this method to convert their results. The default implementation returns an empty String for null values or the default String representation of the value. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getCount](https://developer.android.com/reference/kotlin/android/widget/CursorAdapter#getCount())`()` <br /> | | [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#)! | [getCursor](https://developer.android.com/reference/kotlin/android/widget/CursorAdapter#getCursor())`()` Returns the cursor. <br /> | | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)! | [getDropDownView](https://developer.android.com/reference/kotlin/android/widget/CursorAdapter#getDropDownView(kotlin.Int,%20android.view.View,%20android.view.ViewGroup))`(`position:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `convertView:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!`, `parent:` ` [ViewGroup](https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#)!`)` <br /> | | [Resources.Theme](https://developer.android.com/reference/kotlin/android/content/res/Resources.Theme.html#)? | [getDropDownViewTheme](https://developer.android.com/reference/kotlin/android/widget/CursorAdapter#getDropDownViewTheme())`()` <br /> | | [Filter](https://developer.android.com/reference/kotlin/android/widget/Filter)! | [getFilter](https://developer.android.com/reference/kotlin/android/widget/CursorAdapter#getFilter())`()` <br /> | | [FilterQueryProvider](https://developer.android.com/reference/kotlin/android/widget/FilterQueryProvider)! | [getFilterQueryProvider](https://developer.android.com/reference/kotlin/android/widget/CursorAdapter#getFilterQueryProvider())`()` Returns the query filter provider used for filtering. When the provider is null, no filtering occurs. <br /> | | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getItem](https://developer.android.com/reference/kotlin/android/widget/CursorAdapter#getItem(kotlin.Int))`(`position:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> | | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getItemId](https://developer.android.com/reference/kotlin/android/widget/CursorAdapter#getItemId(kotlin.Int))`(`position:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> | | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)! | [getView](https://developer.android.com/reference/kotlin/android/widget/CursorAdapter#getView(kotlin.Int,%20android.view.View,%20android.view.ViewGroup))`(`position:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `convertView:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!`, `parent:` ` [ViewGroup](https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#)!`)` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasStableIds](https://developer.android.com/reference/kotlin/android/widget/CursorAdapter#hasStableIds())`()` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [init](https://developer.android.com/reference/kotlin/android/widget/CursorAdapter#init(android.content.Context,%20android.database.Cursor,%20kotlin.Boolean))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`, `c:` ` [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#)!`, `autoRequery:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onContentChanged](https://developer.android.com/reference/kotlin/android/widget/CursorAdapter#onContentChanged())`()` Called when the [ContentObserver](https://developer.android.com/reference/kotlin/android/database/ContentObserver.html#) on the cursor receives a change notification. The default implementation provides the auto-requery logic, but may be overridden by sub classes. <br /> | | [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#)! | [runQueryOnBackgroundThread](https://developer.android.com/reference/kotlin/android/widget/CursorAdapter#runQueryOnBackgroundThread(kotlin.CharSequence))`(`constraint:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` Runs a query with the specified constraint. This query is requested by the filter attached to this adapter. The query is provided by a [android.widget.FilterQueryProvider](https://developer.android.com/reference/kotlin/android/widget/FilterQueryProvider). If no provider is specified, the current cursor is not filtered and returned. After this method returns the resulting cursor is passed to [changeCursor(android.database.Cursor)](https://developer.android.com/reference/kotlin/android/widget/CursorAdapter#changeCursor(android.database.Cursor)) and the previous cursor is closed. This method is always executed on a background thread, not on the application's main thread (or UI thread.) Contract: when constraint is null or empty, the original results, prior to any filtering, must be returned. This method may take several seconds to complete, so it should only be called from a worker thread. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFilterQueryProvider](https://developer.android.com/reference/kotlin/android/widget/CursorAdapter#setFilterQueryProvider(android.widget.FilterQueryProvider))`(`filterQueryProvider:` ` [FilterQueryProvider](https://developer.android.com/reference/kotlin/android/widget/FilterQueryProvider)!`)` Sets the query filter provider used to filter the current Cursor. The provider's [android.widget.FilterQueryProvider#runQuery(CharSequence)](https://developer.android.com/reference/kotlin/android/widget/FilterQueryProvider#runQuery(kotlin.CharSequence)) method is invoked when filtering is requested by a client of this adapter. <br /> | | [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#)! | [swapCursor](https://developer.android.com/reference/kotlin/android/widget/CursorAdapter#swapCursor(android.database.Cursor))`(`newCursor:` ` [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#)!`)` Swap in a new Cursor, returning the old Cursor. Unlike [changeCursor(android.database.Cursor)](https://developer.android.com/reference/kotlin/android/widget/CursorAdapter#changeCursor(android.database.Cursor)), the returned old Cursor is *not* closed. <br /> | ||

## Public constructors

### ResourceCursorAdapter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ResourceCursorAdapter(
    context: Context!, 
    layout: Int, 
    c: Cursor!)
```

**Deprecated:** *This option is discouraged, as it results in Cursor queries being performed on the application's UI thread and thus can cause poor responsiveness or even Application Not Responding errors. As an alternative, use [android.app.LoaderManager](https://developer.android.com/reference/kotlin/android/app/LoaderManager.html#) with a [android.content.CursorLoader](https://developer.android.com/reference/kotlin/android/content/CursorLoader.html#).*

Constructor the enables auto-requery.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!: The context where the ListView associated with this adapter is running |
| `layout` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): resource identifier of a layout file that defines the views for this list item. Unless you override them later, this will define both the item views and the drop down views. |

### ResourceCursorAdapter

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ResourceCursorAdapter(
    context: Context!, 
    layout: Int, 
    c: Cursor!, 
    autoRequery: Boolean)
```

Constructor with default behavior as per [CursorAdapter.CursorAdapter(Context, Cursor, boolean)](https://developer.android.com/reference/kotlin/android/widget/CursorAdapter#CursorAdapter(android.content.Context,%20android.database.Cursor,%20kotlin.Boolean)); it is recommended you not use this, but instead [ResourceCursorAdapter(android.content.Context,int,android.database.Cursor,int)](https://developer.android.com/reference/kotlin/android/widget/ResourceCursorAdapter#ResourceCursorAdapter(android.content.Context,%20kotlin.Int,%20android.database.Cursor,%20kotlin.Int)). When using this constructor, [FLAG_REGISTER_CONTENT_OBSERVER](https://developer.android.com/reference/kotlin/android/widget/CursorAdapter#FLAG_REGISTER_CONTENT_OBSERVER:kotlin.Int) will always be set.

| Parameters ||
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!: The context where the ListView associated with this adapter is running |
| `layout` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): resource identifier of a layout file that defines the views for this list item. Unless you override them later, this will define both the item views and the drop down views. |
| `c` | [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#)!: The cursor from which to get the data. |
| `autoRequery` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): If true the adapter will call requery() on the cursor whenever it changes so the most recent data is always displayed. Using true here is discouraged. |

### ResourceCursorAdapter

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ResourceCursorAdapter(
    context: Context!, 
    layout: Int, 
    c: Cursor!, 
    flags: Int)
```

Standard constructor.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!: The context where the ListView associated with this adapter is running |
| `layout` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Resource identifier of a layout file that defines the views for this list item. Unless you override them later, this will define both the item views and the drop down views. |
| `c` | [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#)!: The cursor from which to get the data. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Flags used to determine the behavior of the adapter, as per [CursorAdapter.CursorAdapter(Context, Cursor, int)](https://developer.android.com/reference/kotlin/android/widget/CursorAdapter#CursorAdapter(android.content.Context,%20android.database.Cursor,%20kotlin.Int)). |

## Public methods

### newDropDownView

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun newDropDownView(
    context: Context!, 
    cursor: Cursor!, 
    parent: ViewGroup!
): View!
```

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!: Interface to application's global information |
| `cursor` | [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#)!: The cursor from which to get the data. The cursor is already moved to the correct position. |
| `parent` | [ViewGroup](https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#)!: The parent to which the new view is attached to |

| Return ||
|---------------------------------------------------------------------------------|-------------------------|
| [View](https://developer.android.com/reference/kotlin/android/view/View.html#)! | the newly created view. |

### newView

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun newView(
    context: Context!, 
    cursor: Cursor!, 
    parent: ViewGroup!
): View!
```

Inflates view(s) from the specified XML file.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!: Interface to application's global information |
| `cursor` | [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#)!: The cursor from which to get the data. The cursor is already moved to the correct position. |
| `parent` | [ViewGroup](https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#)!: The parent to which the new view is attached to |

| Return ||
|---------------------------------------------------------------------------------|-------------------------|
| [View](https://developer.android.com/reference/kotlin/android/view/View.html#)! | the newly created view. |

**See Also**

- [android.widget.CursorAdapter#newView(android.content.Context,
* android.database.Cursor, ViewGroup)](https://developer.android.com/reference/kotlin/android/widget/CursorAdapter#newView(android.content.Context,%20android.database.Cursor,%20android.view.ViewGroup)) 

### setDropDownViewResource

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setDropDownViewResource(dropDownLayout: Int): Unit
```

Sets the layout resource of the drop down views.

| Parameters ||
|------------------|---------------------------------------------------------------------------------------------------------------------------------|
| `dropDownLayout` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the layout resources used to create drop down views |

### setDropDownViewTheme

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setDropDownViewTheme(theme: Resources.Theme?): Unit
```

Sets the [android.content.res.Resources.Theme](https://developer.android.com/reference/kotlin/android/content/res/Resources.Theme.html#) against which drop-down views are inflated.

By default, drop-down views are inflated against the theme of the [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#) passed to the adapter's constructor.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `theme` | [Resources.Theme](https://developer.android.com/reference/kotlin/android/content/res/Resources.Theme.html#)?: the theme against which to inflate drop-down views or `null` to use the theme from the adapter's context |

**See Also**

- [#newDropDownView(Context, Cursor, ViewGroup)](https://developer.android.com/reference/kotlin/android/widget/ResourceCursorAdapter#newDropDownView(android.content.Context,%20android.database.Cursor,%20android.view.ViewGroup)) 

### setViewResource

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setViewResource(layout: Int): Unit
```

Sets the layout resource of the item views.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------|
| `layout` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the layout resources used to create item views |
