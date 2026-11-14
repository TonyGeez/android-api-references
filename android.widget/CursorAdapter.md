# CursorAdapter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CursorAdapter

Kotlin| [Java](https://developer.android.com/reference/android/widget/CursorAdapter "View this page in Java") 

```
abstract class CursorAdapter : BaseAdapter, Filterable, ThemedSpinnerAdapter
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| ↳ | [android.widget.BaseAdapter](https://developer.android.com/reference/kotlin/android/widget/BaseAdapter) ||
| | ↳ | [android.widget.CursorAdapter](https://developer.android.com/reference/kotlin/android/widget/CursorAdapter#) |

| Known Direct Subclasses [ResourceCursorAdapter](https://developer.android.com/reference/kotlin/android/widget/ResourceCursorAdapter) |--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------| | [ResourceCursorAdapter](https://developer.android.com/reference/kotlin/android/widget/ResourceCursorAdapter) | An easy adapter that creates views defined in an XML file. | |

| Known Indirect Subclasses [SimpleCursorAdapter](https://developer.android.com/reference/kotlin/android/widget/SimpleCursorAdapter) |----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------| | [SimpleCursorAdapter](https://developer.android.com/reference/kotlin/android/widget/SimpleCursorAdapter) | An easy adapter to map columns from a cursor to TextViews or ImageViews defined in an XML file. | |

Adapter that exposes data from a [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#) to a [ListView](https://developer.android.com/reference/kotlin/android/widget/ListView) widget.

The Cursor must include a column named "_id" or this class will not work. Additionally, using [android.database.MergeCursor](https://developer.android.com/reference/kotlin/android/database/MergeCursor.html#) with this class will not work if the merged Cursors have overlapping values in their "_id" columns.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FLAG_AUTO_REQUERY](https://developer.android.com/reference/kotlin/android/widget/CursorAdapter#FLAG_AUTO_REQUERY:kotlin.Int) If set the adapter will call requery() on the cursor whenever a content change notification is delivered. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FLAG_REGISTER_CONTENT_OBSERVER](https://developer.android.com/reference/kotlin/android/widget/CursorAdapter#FLAG_REGISTER_CONTENT_OBSERVER:kotlin.Int) If set the adapter will register a content observer on the cursor and will call [onContentChanged()](https://developer.android.com/reference/kotlin/android/widget/CursorAdapter#onContentChanged())when a notification comes in. |

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [CursorAdapter](https://developer.android.com/reference/kotlin/android/widget/CursorAdapter#CursorAdapter(android.content.Context,%20android.database.Cursor))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`, `c:` ` [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#)!`)` Constructor that always enables auto-requery. |
| [CursorAdapter](https://developer.android.com/reference/kotlin/android/widget/CursorAdapter#CursorAdapter(android.content.Context,%20android.database.Cursor,%20kotlin.Boolean))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`, `c:` ` [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#)!`, `autoRequery:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Constructor that allows control over auto-requery. |
| [CursorAdapter](https://developer.android.com/reference/kotlin/android/widget/CursorAdapter#CursorAdapter(android.content.Context,%20android.database.Cursor,%20kotlin.Int))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`, `c:` ` [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#)!`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Recommended constructor. |

| Public methods ||
|------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [bindView](https://developer.android.com/reference/kotlin/android/widget/CursorAdapter#bindView(android.view.View,%20android.content.Context,%20android.database.Cursor))`(`view:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!`, `context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`, `cursor:` ` [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#)!`)` Bind an existing view to the data pointed to by cursor |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [changeCursor](https://developer.android.com/reference/kotlin/android/widget/CursorAdapter#changeCursor(android.database.Cursor))`(`cursor:` ` [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#)!`)` Change the underlying cursor to a new cursor. |
| open [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | [convertToString](https://developer.android.com/reference/kotlin/android/widget/CursorAdapter#convertToString(android.database.Cursor))`(`cursor:` ` [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#)!`)` Converts the cursor into a CharSequence. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getCount](https://developer.android.com/reference/kotlin/android/widget/CursorAdapter#getCount())`()` <br /> |
| open [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#)! | [getCursor](https://developer.android.com/reference/kotlin/android/widget/CursorAdapter#getCursor())`()` Returns the cursor. |
| open [View](https://developer.android.com/reference/kotlin/android/view/View.html#)! | [getDropDownView](https://developer.android.com/reference/kotlin/android/widget/CursorAdapter#getDropDownView(kotlin.Int,%20android.view.View,%20android.view.ViewGroup))`(`position:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `convertView:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!`, `parent:` ` [ViewGroup](https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#)!`)` <br /> |
| open [Resources.Theme](https://developer.android.com/reference/kotlin/android/content/res/Resources.Theme.html#)? | [getDropDownViewTheme](https://developer.android.com/reference/kotlin/android/widget/CursorAdapter#getDropDownViewTheme())`()` <br /> |
| open [Filter](https://developer.android.com/reference/kotlin/android/widget/Filter)! | [getFilter](https://developer.android.com/reference/kotlin/android/widget/CursorAdapter#getFilter())`()` <br /> |
| open [FilterQueryProvider](https://developer.android.com/reference/kotlin/android/widget/FilterQueryProvider)! | [getFilterQueryProvider](https://developer.android.com/reference/kotlin/android/widget/CursorAdapter#getFilterQueryProvider())`()` Returns the query filter provider used for filtering. |
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getItem](https://developer.android.com/reference/kotlin/android/widget/CursorAdapter#getItem(kotlin.Int))`(`position:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getItemId](https://developer.android.com/reference/kotlin/android/widget/CursorAdapter#getItemId(kotlin.Int))`(`position:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [View](https://developer.android.com/reference/kotlin/android/view/View.html#)! | [getView](https://developer.android.com/reference/kotlin/android/widget/CursorAdapter#getView(kotlin.Int,%20android.view.View,%20android.view.ViewGroup))`(`position:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `convertView:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!`, `parent:` ` [ViewGroup](https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#)!`)` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasStableIds](https://developer.android.com/reference/kotlin/android/widget/CursorAdapter#hasStableIds())`()` <br /> |
| open [View](https://developer.android.com/reference/kotlin/android/view/View.html#)! | [newDropDownView](https://developer.android.com/reference/kotlin/android/widget/CursorAdapter#newDropDownView(android.content.Context,%20android.database.Cursor,%20android.view.ViewGroup))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`, `cursor:` ` [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#)!`, `parent:` ` [ViewGroup](https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#)!`)` Makes a new drop down view to hold the data pointed to by cursor. |
| abstract [View](https://developer.android.com/reference/kotlin/android/view/View.html#)! | [newView](https://developer.android.com/reference/kotlin/android/widget/CursorAdapter#newView(android.content.Context,%20android.database.Cursor,%20android.view.ViewGroup))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`, `cursor:` ` [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#)!`, `parent:` ` [ViewGroup](https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#)!`)` Makes a new view to hold the data pointed to by cursor. |
| open [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#)! | [runQueryOnBackgroundThread](https://developer.android.com/reference/kotlin/android/widget/CursorAdapter#runQueryOnBackgroundThread(kotlin.CharSequence))`(`constraint:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` Runs a query with the specified constraint. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDropDownViewTheme](https://developer.android.com/reference/kotlin/android/widget/CursorAdapter#setDropDownViewTheme(android.content.res.Resources.Theme))`(`theme:` ` [Resources.Theme](https://developer.android.com/reference/kotlin/android/content/res/Resources.Theme.html#)?`)` Sets the [Resources.Theme](https://developer.android.com/reference/kotlin/android/content/res/Resources.Theme.html#) against which drop-down views are inflated. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFilterQueryProvider](https://developer.android.com/reference/kotlin/android/widget/CursorAdapter#setFilterQueryProvider(android.widget.FilterQueryProvider))`(`filterQueryProvider:` ` [FilterQueryProvider](https://developer.android.com/reference/kotlin/android/widget/FilterQueryProvider)!`)` Sets the query filter provider used to filter the current Cursor. |
| open [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#)! | [swapCursor](https://developer.android.com/reference/kotlin/android/widget/CursorAdapter#swapCursor(android.database.Cursor))`(`newCursor:` ` [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#)!`)` Swap in a new Cursor, returning the old Cursor. |

| Protected methods ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [init](https://developer.android.com/reference/kotlin/android/widget/CursorAdapter#init(android.content.Context,%20android.database.Cursor,%20kotlin.Boolean))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`, `c:` ` [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#)!`, `autoRequery:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onContentChanged](https://developer.android.com/reference/kotlin/android/widget/CursorAdapter#onContentChanged())`()` Called when the [ContentObserver](https://developer.android.com/reference/kotlin/android/database/ContentObserver.html#) on the cursor receives a change notification. |

| Inherited functions ||
|---|---|
| From class [BaseAdapter](https://developer.android.com/reference/kotlin/android/widget/BaseAdapter) |---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [areAllItemsEnabled](https://developer.android.com/reference/kotlin/android/widget/BaseAdapter#areAllItemsEnabled())`()` <br /> | | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!>? | [getAutofillOptions](https://developer.android.com/reference/kotlin/android/widget/BaseAdapter#getAutofillOptions())`()` <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getItemViewType](https://developer.android.com/reference/kotlin/android/widget/BaseAdapter#getItemViewType(kotlin.Int))`(`position:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getViewTypeCount](https://developer.android.com/reference/kotlin/android/widget/BaseAdapter#getViewTypeCount())`()` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEmpty](https://developer.android.com/reference/kotlin/android/widget/BaseAdapter#isEmpty())`()` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEnabled](https://developer.android.com/reference/kotlin/android/widget/BaseAdapter#isEnabled(kotlin.Int))`(`position:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [notifyDataSetChanged](https://developer.android.com/reference/kotlin/android/widget/BaseAdapter#notifyDataSetChanged())`()` <br /> Notifies the attached observers that the underlying data has been changed and any View reflecting the data set should refresh itself. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [notifyDataSetInvalidated](https://developer.android.com/reference/kotlin/android/widget/BaseAdapter#notifyDataSetInvalidated())`()` <br /> Notifies the attached observers that the underlying data is no longer valid or available. Once invoked this adapter is no longer valid and should not report further data set changes. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerDataSetObserver](https://developer.android.com/reference/kotlin/android/widget/BaseAdapter#registerDataSetObserver(android.database.DataSetObserver))`(`observer:` ` [DataSetObserver](https://developer.android.com/reference/kotlin/android/database/DataSetObserver.html#)!`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAutofillOptions](https://developer.android.com/reference/kotlin/android/widget/BaseAdapter#setAutofillOptions(kotlin.CharSequence))`(`vararg` `options:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` <br /> Sets the value returned by [getAutofillOptions()](https://developer.android.com/reference/kotlin/android/widget/BaseAdapter#getAutofillOptions()) <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unregisterDataSetObserver](https://developer.android.com/reference/kotlin/android/widget/BaseAdapter#unregisterDataSetObserver(android.database.DataSetObserver))`(`observer:` ` [DataSetObserver](https://developer.android.com/reference/kotlin/android/database/DataSetObserver.html#)!`)` <br /> | ||

## Constants

### FLAG_AUTO_REQUERY

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FLAG_AUTO_REQUERY: Int
```

**Deprecated:** *This option is discouraged, as it results in Cursor queries being performed on the application's UI thread and thus can cause poor responsiveness or even Application Not Responding errors. As an alternative, use [android.app.LoaderManager](https://developer.android.com/reference/kotlin/android/app/LoaderManager.html#) with a [android.content.CursorLoader](https://developer.android.com/reference/kotlin/android/content/CursorLoader.html#).*

If set the adapter will call requery() on the cursor whenever a content change notification is delivered. Implies [FLAG_REGISTER_CONTENT_OBSERVER](https://developer.android.com/reference/kotlin/android/widget/CursorAdapter#FLAG_REGISTER_CONTENT_OBSERVER:kotlin.Int). 

 Value: 1

### FLAG_REGISTER_CONTENT_OBSERVER

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FLAG_REGISTER_CONTENT_OBSERVER: Int
```

If set the adapter will register a content observer on the cursor and will call [onContentChanged()](https://developer.android.com/reference/kotlin/android/widget/CursorAdapter#onContentChanged())when a notification comes in. Be careful when using this flag: you will need to unset the current Cursor from the adapter to avoid leaks due to its registered observers. This flag is not needed when using a CursorAdapter with a [android.content.CursorLoader](https://developer.android.com/reference/kotlin/android/content/CursorLoader.html#). 

 Value: 2

## Public constructors

### CursorAdapter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
CursorAdapter(
    context: Context!, 
    c: Cursor!)
```

**Deprecated:** *This option is discouraged, as it results in Cursor queries being performed on the application's UI thread and thus can cause poor responsiveness or even Application Not Responding errors. As an alternative, use [android.app.LoaderManager](https://developer.android.com/reference/kotlin/android/app/LoaderManager.html#) with a [android.content.CursorLoader](https://developer.android.com/reference/kotlin/android/content/CursorLoader.html#).*

Constructor that always enables auto-requery.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------|
| `c` | [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#)!:The cursor from which to get the data. |
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!:The context |

### CursorAdapter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
CursorAdapter(
    context: Context!, 
    c: Cursor!, 
    autoRequery: Boolean)
```

Constructor that allows control over auto-requery. It is recommended you not use this, but instead [CursorAdapter(android.content.Context,android.database.Cursor,int)](https://developer.android.com/reference/kotlin/android/widget/CursorAdapter#CursorAdapter(android.content.Context,%20android.database.Cursor,%20kotlin.Int)). When using this constructor, [FLAG_REGISTER_CONTENT_OBSERVER](https://developer.android.com/reference/kotlin/android/widget/CursorAdapter#FLAG_REGISTER_CONTENT_OBSERVER:kotlin.Int) will always be set.

| Parameters ||
|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `c` | [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#)!:The cursor from which to get the data. |
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!:The context |
| `autoRequery` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):If true the adapter will call requery() on the cursor whenever it changes so the most recent data is always displayed. Using true here is discouraged. |

### CursorAdapter

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
CursorAdapter(
    context: Context!, 
    c: Cursor!, 
    flags: Int)
```

Recommended constructor.

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `c` | [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#)!:The cursor from which to get the data. |
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!:The context |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Flags used to determine the behavior of the adapter; may be any combination of [FLAG_AUTO_REQUERY](https://developer.android.com/reference/kotlin/android/widget/CursorAdapter#FLAG_AUTO_REQUERY:kotlin.Int) and [FLAG_REGISTER_CONTENT_OBSERVER](https://developer.android.com/reference/kotlin/android/widget/CursorAdapter#FLAG_REGISTER_CONTENT_OBSERVER:kotlin.Int). |

## Public methods

### bindView

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun bindView(
    view: View!, 
    context: Context!, 
    cursor: Cursor!
): Unit
```

Bind an existing view to the data pointed to by cursor

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `view` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!:Existing view, returned earlier by newView |
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!:Interface to application's global information |
| `cursor` | [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#)!:The cursor from which to get the data. The cursor is already moved to the correct position. |

### changeCursor

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun changeCursor(cursor: Cursor!): Unit
```

Change the underlying cursor to a new cursor. If there is an existing cursor it will be closed.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------|
| `cursor` | [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#)!:The new cursor to be used |

### convertToString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun convertToString(cursor: Cursor!): CharSequence!
```

Converts the cursor into a CharSequence. Subclasses should override this method to convert their results. The default implementation returns an empty String for null values or the default String representation of the value.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------|
| `cursor` | [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#)!:the cursor to convert to a CharSequence |

| Return ||
|------------------------------------------------------------------------------------------------|---------------------------------------|
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | a CharSequence representing the value |

### getCount

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getCount(): Int
```

| Return ||
|----------------------------------------------------------------------------|-----------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Count of items. |

**See Also**

- [android.widget.ListAdapter#getCount()](https://developer.android.com/reference/kotlin/android/widget/Adapter#getCount()) 

### getCursor

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getCursor(): Cursor!
```

Returns the cursor.

| Return ||
|-----------------------------------------------------------------------------------------|-------------|
| [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#)! | the cursor. |

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

| Return ||
|---------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [View](https://developer.android.com/reference/kotlin/android/view/View.html#)! | a [android.view.View](https://developer.android.com/reference/kotlin/android/view/View.html#) corresponding to the data at the specified position. |

### getDropDownViewTheme

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDropDownViewTheme(): Resources.Theme?
```

| Return ||
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Resources.Theme](https://developer.android.com/reference/kotlin/android/content/res/Resources.Theme.html#)? | the [Resources.Theme](https://developer.android.com/reference/kotlin/android/content/res/Resources.Theme.html#) against which drop-down views are inflated, or`null`if one has not been explicitly set |

### getFilter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getFilter(): Filter!
```

| Return ||
|---------------------------------------------------------------------------------|---------------------------------|
| [Filter](https://developer.android.com/reference/kotlin/android/widget/Filter)! | a filter used to constrain data |

### getFilterQueryProvider

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getFilterQueryProvider(): FilterQueryProvider!
```

Returns the query filter provider used for filtering. When the provider is null, no filtering occurs.

| Return ||
|-----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| [FilterQueryProvider](https://developer.android.com/reference/kotlin/android/widget/FilterQueryProvider)! | the current filter query provider or null if it does not exist |

**See Also**

- <https://developer.android.com/reference/kotlin/android/widget/CursorAdapter#setFilterQueryProvider(android.widget.FilterQueryProvider)>
- [#runQueryOnBackgroundThread(CharSequence)](https://developer.android.com/reference/kotlin/android/widget/CursorAdapter#runQueryOnBackgroundThread(kotlin.CharSequence)) 

### getItem

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getItem(position: Int): Any!
```

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| `position` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Position of the item whose data we want within the adapter's data set. |

| Return ||
|-----------------------------------------------------------------------------|-------------------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | The data at the specified position. |

**See Also**

- [android.widget.ListAdapter#getItem(int)](https://developer.android.com/reference/kotlin/android/widget/Adapter#getItem(kotlin.Int)) 

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

**See Also**

- [android.widget.ListAdapter#getItemId(int)](https://developer.android.com/reference/kotlin/android/widget/Adapter#getItemId(kotlin.Int)) 

### getView

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getView(
    position: Int, 
    convertView: View!, 
    parent: ViewGroup!
): View!
```

| Parameters ||
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `position` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The position of the item within the adapter's data set of the item whose view we want. |
| `convertView` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!:The old view to reuse, if possible. Note: You should check that this view is non-null and of an appropriate type before using. If it is not possible to convert this view to display the correct data, this method can create a new view. Heterogeneous lists can specify their number of view types, so that this View is always of the right type (see [getViewTypeCount()](https://developer.android.com/reference/kotlin/android/widget/Adapter#getViewTypeCount())and [getItemViewType(int)](https://developer.android.com/reference/kotlin/android/widget/Adapter#getItemViewType(kotlin.Int))). |
| `parent` | [ViewGroup](https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#)!:The parent that this view will eventually be attached to |

| Return ||
|---------------------------------------------------------------------------------|-------------------------------------------------------------|
| [View](https://developer.android.com/reference/kotlin/android/view/View.html#)! | A View corresponding to the data at the specified position. |

**See Also**

- [android.widget.ListAdapter#getView(int, View, ViewGroup)](https://developer.android.com/reference/kotlin/android/widget/Adapter#getView(kotlin.Int,%20android.view.View,%20android.view.ViewGroup)) 

### hasStableIds

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hasStableIds(): Boolean
```

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if the same id always refers to the same object. |

### newDropDownView

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun newDropDownView(
    context: Context!, 
    cursor: Cursor!, 
    parent: ViewGroup!
): View!
```

Makes a new drop down view to hold the data pointed to by cursor.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!:Interface to application's global information |
| `cursor` | [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#)!:The cursor from which to get the data. The cursor is already moved to the correct position. |
| `parent` | [ViewGroup](https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#)!:The parent to which the new view is attached to |

| Return ||
|---------------------------------------------------------------------------------|-------------------------|
| [View](https://developer.android.com/reference/kotlin/android/view/View.html#)! | the newly created view. |

### newView

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun newView(
    context: Context!, 
    cursor: Cursor!, 
    parent: ViewGroup!
): View!
```

Makes a new view to hold the data pointed to by cursor.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!:Interface to application's global information |
| `cursor` | [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#)!:The cursor from which to get the data. The cursor is already moved to the correct position. |
| `parent` | [ViewGroup](https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#)!:The parent to which the new view is attached to |

| Return ||
|---------------------------------------------------------------------------------|-------------------------|
| [View](https://developer.android.com/reference/kotlin/android/view/View.html#)! | the newly created view. |

### runQueryOnBackgroundThread

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun runQueryOnBackgroundThread(constraint: CharSequence!): Cursor!
```

Runs a query with the specified constraint. This query is requested by the filter attached to this adapter. The query is provided by a [android.widget.FilterQueryProvider](https://developer.android.com/reference/kotlin/android/widget/FilterQueryProvider). If no provider is specified, the current cursor is not filtered and returned. After this method returns the resulting cursor is passed to [changeCursor(android.database.Cursor)](https://developer.android.com/reference/kotlin/android/widget/CursorAdapter#changeCursor(android.database.Cursor))and the previous cursor is closed. This method is always executed on a background thread, not on the application's main thread (or UI thread.) Contract: when constraint is null or empty, the original results, prior to any filtering, must be returned. 
This method may take several seconds to complete, so it should only be called from a worker thread.

| Parameters ||
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| `constraint` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:the constraint with which the query must be filtered |

| Return ||
|-----------------------------------------------------------------------------------------|----------------------------------------------------|
| [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#)! | a Cursor representing the results of the new query |

**See Also**

- <https://developer.android.com/reference/kotlin/android/widget/CursorAdapter#getFilter()>
- <https://developer.android.com/reference/kotlin/android/widget/CursorAdapter#getFilterQueryProvider()>
- <https://developer.android.com/reference/kotlin/android/widget/CursorAdapter#setFilterQueryProvider(android.widget.FilterQueryProvider)> 

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

- [#newDropDownView(Context, Cursor, ViewGroup)](https://developer.android.com/reference/kotlin/android/widget/CursorAdapter#newDropDownView(android.content.Context,%20android.database.Cursor,%20android.view.ViewGroup)) 

### setFilterQueryProvider

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setFilterQueryProvider(filterQueryProvider: FilterQueryProvider!): Unit
```

Sets the query filter provider used to filter the current Cursor. The provider's [android.widget.FilterQueryProvider#runQuery(CharSequence)](https://developer.android.com/reference/kotlin/android/widget/FilterQueryProvider#runQuery(kotlin.CharSequence))method is invoked when filtering is requested by a client of this adapter.

| Parameters ||
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `filterQueryProvider` | [FilterQueryProvider](https://developer.android.com/reference/kotlin/android/widget/FilterQueryProvider)!:the filter query provider or null to remove it |

**See Also**

- <https://developer.android.com/reference/kotlin/android/widget/CursorAdapter#getFilterQueryProvider()>
- [#runQueryOnBackgroundThread(CharSequence)](https://developer.android.com/reference/kotlin/android/widget/CursorAdapter#runQueryOnBackgroundThread(kotlin.CharSequence)) 

### swapCursor

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun swapCursor(newCursor: Cursor!): Cursor!
```

Swap in a new Cursor, returning the old Cursor. Unlike [changeCursor(android.database.Cursor)](https://developer.android.com/reference/kotlin/android/widget/CursorAdapter#changeCursor(android.database.Cursor)), the returned old Cursor is*not*closed.

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------------------------|
| `newCursor` | [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#)!:The new cursor to be used. |

| Return ||
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#)! | Returns the previously set Cursor, or null if there was not one. If the given new Cursor is the same instance is the previously set Cursor, null is also returned. |

## Protected methods

### init

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun init(
    context: Context!, 
    c: Cursor!, 
    autoRequery: Boolean
): Unit
```

**Deprecated:** *Don't use this, use the normal constructor. This will be removed in the future.* 

### onContentChanged

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun onContentChanged(): Unit
```

Called when the [ContentObserver](https://developer.android.com/reference/kotlin/android/database/ContentObserver.html#) on the cursor receives a change notification. The default implementation provides the auto-requery logic, but may be overridden by sub classes. 
**See Also**

- [android.database.ContentObserver#onChange(boolean)](https://developer.android.com/reference/kotlin/android/database/ContentObserver.html#onChange(kotlin.Boolean))
