# CursorAdapter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CursorAdapter

Kotlin| [Java](CursorAdapter.md) 
| --- | --- |

```
abstract class CursorAdapter : BaseAdapter, Filterable, ThemedSpinnerAdapter
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.widget.BaseAdapter](BaseAdapter.md) ||
| | ↳ | [android.widget.CursorAdapter](CursorAdapter.md) |

| Known Direct Subclasses [ResourceCursorAdapter](ResourceCursorAdapter.md) |--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------| | [ResourceCursorAdapter](ResourceCursorAdapter.md) | An easy adapter that creates views defined in an XML file. | |
| --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [SimpleCursorAdapter](SimpleCursorAdapter.md) |----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------| | [SimpleCursorAdapter](SimpleCursorAdapter.md) | An easy adapter to map columns from a cursor to TextViews or ImageViews defined in an XML file. | |
| --- | --- | --- | --- | --- | --- | --- |

Adapter that exposes data from a [Cursor](../android.database/Cursor.md) to a [ListView](ListView.md) widget.

The Cursor must include a column named "_id" or this class will not work. Additionally, using [android.database.MergeCursor](../android.database/MergeCursor.md) with this class will not work if the merged Cursors have overlapping values in their "_id" columns.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FLAG_AUTO_REQUERY](CursorAdapter.md) If set the adapter will call requery() on the cursor whenever a content change notification is delivered. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FLAG_REGISTER_CONTENT_OBSERVER](CursorAdapter.md) If set the adapter will register a content observer on the cursor and will call [onContentChanged()](CursorAdapter.md))when a notification comes in. |

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [CursorAdapter](CursorAdapter.md))`(`context:` ` [Context](../android.content/Context.md)!`, `c:` ` [Cursor](../android.database/Cursor.md)!`)` Constructor that always enables auto-requery. |
| [CursorAdapter](CursorAdapter.md))`(`context:` ` [Context](../android.content/Context.md)!`, `c:` ` [Cursor](../android.database/Cursor.md)!`, `autoRequery:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Constructor that allows control over auto-requery. |
| [CursorAdapter](CursorAdapter.md))`(`context:` ` [Context](../android.content/Context.md)!`, `c:` ` [Cursor](../android.database/Cursor.md)!`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Recommended constructor. |

| Public methods ||
|------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [bindView](CursorAdapter.md))`(`view:` ` [View](../android.view/View.md)!`, `context:` ` [Context](../android.content/Context.md)!`, `cursor:` ` [Cursor](../android.database/Cursor.md)!`)` Bind an existing view to the data pointed to by cursor |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [changeCursor](CursorAdapter.md))`(`cursor:` ` [Cursor](../android.database/Cursor.md)!`)` Change the underlying cursor to a new cursor. |
| open [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | [convertToString](CursorAdapter.md))`(`cursor:` ` [Cursor](../android.database/Cursor.md)!`)` Converts the cursor into a CharSequence. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getCount](CursorAdapter.md))`()` <br /> |
| open [Cursor](../android.database/Cursor.md)! | [getCursor](CursorAdapter.md))`()` Returns the cursor. |
| open [View](../android.view/View.md)! | [getDropDownView](CursorAdapter.md))`(`position:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `convertView:` ` [View](../android.view/View.md)!`, `parent:` ` [ViewGroup](../android.view/ViewGroup.md)!`)` <br /> |
| --- | --- |
| open [Resources.Theme](../android/content/res/Resources.Theme.md)? | [getDropDownViewTheme](CursorAdapter.md))`()` <br /> |
| open [Filter](Filter.md)! | [getFilter](CursorAdapter.md))`()` <br /> |
| open [FilterQueryProvider](FilterQueryProvider.md)! | [getFilterQueryProvider](CursorAdapter.md))`()` Returns the query filter provider used for filtering. |
| --- | --- |
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getItem](CursorAdapter.md))`(`position:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getItemId](CursorAdapter.md))`(`position:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [View](../android.view/View.md)! | [getView](CursorAdapter.md))`(`position:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `convertView:` ` [View](../android.view/View.md)!`, `parent:` ` [ViewGroup](../android.view/ViewGroup.md)!`)` <br /> |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasStableIds](CursorAdapter.md))`()` <br /> |
| open [View](../android.view/View.md)! | [newDropDownView](CursorAdapter.md))`(`context:` ` [Context](../android.content/Context.md)!`, `cursor:` ` [Cursor](../android.database/Cursor.md)!`, `parent:` ` [ViewGroup](../android.view/ViewGroup.md)!`)` Makes a new drop down view to hold the data pointed to by cursor. |
| abstract [View](../android.view/View.md)! | [newView](CursorAdapter.md))`(`context:` ` [Context](../android.content/Context.md)!`, `cursor:` ` [Cursor](../android.database/Cursor.md)!`, `parent:` ` [ViewGroup](../android.view/ViewGroup.md)!`)` Makes a new view to hold the data pointed to by cursor. |
| --- | --- |
| open [Cursor](../android.database/Cursor.md)! | [runQueryOnBackgroundThread](CursorAdapter.md))`(`constraint:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` Runs a query with the specified constraint. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDropDownViewTheme](CursorAdapter.md))`(`theme:` ` [Resources.Theme](../android/content/res/Resources.Theme.md)?`)` Sets the [Resources.Theme](../android/content/res/Resources.Theme.md) against which drop-down views are inflated. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFilterQueryProvider](CursorAdapter.md))`(`filterQueryProvider:` ` [FilterQueryProvider](FilterQueryProvider.md)!`)` Sets the query filter provider used to filter the current Cursor. |
| --- | --- |
| open [Cursor](../android.database/Cursor.md)! | [swapCursor](CursorAdapter.md))`(`newCursor:` ` [Cursor](../android.database/Cursor.md)!`)` Swap in a new Cursor, returning the old Cursor. |

| Protected methods ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [init](CursorAdapter.md))`(`context:` ` [Context](../android.content/Context.md)!`, `c:` ` [Cursor](../android.database/Cursor.md)!`, `autoRequery:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onContentChanged](CursorAdapter.md))`()` Called when the [ContentObserver](../android.database/ContentObserver.md) on the cursor receives a change notification. |

| Inherited functions ||
|---|---|
| From class [BaseAdapter](BaseAdapter.md) |---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [areAllItemsEnabled](BaseAdapter.md))`()` <br /> | | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!>? | [getAutofillOptions](BaseAdapter.md))`()` <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getItemViewType](BaseAdapter.md))`(`position:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getViewTypeCount](BaseAdapter.md))`()` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEmpty](BaseAdapter.md))`()` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEnabled](BaseAdapter.md))`(`position:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [notifyDataSetChanged](BaseAdapter.md))`()` <br /> Notifies the attached observers that the underlying data has been changed and any View reflecting the data set should refresh itself. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [notifyDataSetInvalidated](BaseAdapter.md))`()` <br /> Notifies the attached observers that the underlying data is no longer valid or available. Once invoked this adapter is no longer valid and should not report further data set changes. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerDataSetObserver](BaseAdapter.md))`(`observer:` ` [DataSetObserver](../android.database/DataSetObserver.md)!`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAutofillOptions](BaseAdapter.md))`(`vararg` `options:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` <br /> Sets the value returned by [getAutofillOptions()](BaseAdapter.md)) <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unregisterDataSetObserver](BaseAdapter.md))`(`observer:` ` [DataSetObserver](../android.database/DataSetObserver.md)!`)` <br /> | ||

## Constants

### FLAG_AUTO_REQUERY

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FLAG_AUTO_REQUERY: Int
```

**Deprecated:** *This option is discouraged, as it results in Cursor queries being performed on the application's UI thread and thus can cause poor responsiveness or even Application Not Responding errors. As an alternative, use [android.app.LoaderManager](../android.app/LoaderManager.md) with a [android.content.CursorLoader](../android.content/CursorLoader.md).*

If set the adapter will call requery() on the cursor whenever a content change notification is delivered. Implies [FLAG_REGISTER_CONTENT_OBSERVER](CursorAdapter.md). 

 Value: 1

### FLAG_REGISTER_CONTENT_OBSERVER

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FLAG_REGISTER_CONTENT_OBSERVER: Int
```

If set the adapter will register a content observer on the cursor and will call [onContentChanged()](CursorAdapter.md))when a notification comes in. Be careful when using this flag: you will need to unset the current Cursor from the adapter to avoid leaks due to its registered observers. This flag is not needed when using a CursorAdapter with a [android.content.CursorLoader](../android.content/CursorLoader.md). 

 Value: 2

## Public constructors

### CursorAdapter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
CursorAdapter(
    context: Context!, 
    c: Cursor!)
```

**Deprecated:** *This option is discouraged, as it results in Cursor queries being performed on the application's UI thread and thus can cause poor responsiveness or even Application Not Responding errors. As an alternative, use [android.app.LoaderManager](../android.app/LoaderManager.md) with a [android.content.CursorLoader](../android.content/CursorLoader.md).*

Constructor that always enables auto-requery.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------|
| `c` | [Cursor](../android.database/Cursor.md)!:The cursor from which to get the data. |
| `context` | [Context](../android.content/Context.md)!:The context |

### CursorAdapter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
CursorAdapter(
    context: Context!, 
    c: Cursor!, 
    autoRequery: Boolean)
```

Constructor that allows control over auto-requery. It is recommended you not use this, but instead [CursorAdapter(android.content.Context,android.database.Cursor,int)](CursorAdapter.md)). When using this constructor, [FLAG_REGISTER_CONTENT_OBSERVER](CursorAdapter.md) will always be set.

| Parameters ||
|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `c` | [Cursor](../android.database/Cursor.md)!:The cursor from which to get the data. |
| `context` | [Context](../android.content/Context.md)!:The context |
| `autoRequery` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):If true the adapter will call requery() on the cursor whenever it changes so the most recent data is always displayed. Using true here is discouraged. |
| --- | --- |

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
| `c` | [Cursor](../android.database/Cursor.md)!:The cursor from which to get the data. |
| `context` | [Context](../android.content/Context.md)!:The context |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Flags used to determine the behavior of the adapter; may be any combination of [FLAG_AUTO_REQUERY](CursorAdapter.md) and [FLAG_REGISTER_CONTENT_OBSERVER](CursorAdapter.md). |
| --- | --- |

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
| `view` | [View](../android.view/View.md)!:Existing view, returned earlier by newView |
| `context` | [Context](../android.content/Context.md)!:Interface to application's global information |
| `cursor` | [Cursor](../android.database/Cursor.md)!:The cursor from which to get the data. The cursor is already moved to the correct position. |
| --- | --- |

### changeCursor

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun changeCursor(cursor: Cursor!): Unit
```

Change the underlying cursor to a new cursor. If there is an existing cursor it will be closed.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------|
| `cursor` | [Cursor](../android.database/Cursor.md)!:The new cursor to be used |

### convertToString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun convertToString(cursor: Cursor!): CharSequence!
```

Converts the cursor into a CharSequence. Subclasses should override this method to convert their results. The default implementation returns an empty String for null values or the default String representation of the value.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------|
| `cursor` | [Cursor](../android.database/Cursor.md)!:the cursor to convert to a CharSequence |

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

- [android.widget.ListAdapter#getCount()](Adapter.md)) 

### getCursor

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getCursor(): Cursor!
```

Returns the cursor.

| Return ||
|-----------------------------------------------------------------------------------------|-------------|
| [Cursor](../android.database/Cursor.md)! | the cursor. |

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

### getDropDownViewTheme

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDropDownViewTheme(): Resources.Theme?
```

| Return ||
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Resources.Theme](../android/content/res/Resources.Theme.md)? | the [Resources.Theme](../android/content/res/Resources.Theme.md) against which drop-down views are inflated, or`null`if one has not been explicitly set |

### getFilter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getFilter(): Filter!
```

| Return ||
|---------------------------------------------------------------------------------|---------------------------------|
| [Filter](Filter.md)! | a filter used to constrain data |

### getFilterQueryProvider

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getFilterQueryProvider(): FilterQueryProvider!
```

Returns the query filter provider used for filtering. When the provider is null, no filtering occurs.

| Return ||
|-----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| [FilterQueryProvider](FilterQueryProvider.md)! | the current filter query provider or null if it does not exist |

**See Also**

- <https://developer.android.com/reference/kotlin/android/widget/CursorAdapter#setFilterQueryProvider(android.widget.FilterQueryProvider)>
- [#runQueryOnBackgroundThread(CharSequence)](CursorAdapter.md)) 

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

- [android.widget.ListAdapter#getItem(int)](Adapter.md)) 

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

- [android.widget.ListAdapter#getItemId(int)](Adapter.md)) 

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
| `convertView` | [View](../android.view/View.md)!:The old view to reuse, if possible. Note: You should check that this view is non-null and of an appropriate type before using. If it is not possible to convert this view to display the correct data, this method can create a new view. Heterogeneous lists can specify their number of view types, so that this View is always of the right type (see [getViewTypeCount()](Adapter.md))and [getItemViewType(int)](Adapter.md))). |
| `parent` | [ViewGroup](../android.view/ViewGroup.md)!:The parent that this view will eventually be attached to |
| --- | --- |

| Return ||
|---------------------------------------------------------------------------------|-------------------------------------------------------------|
| [View](../android.view/View.md)! | A View corresponding to the data at the specified position. |

**See Also**

- [android.widget.ListAdapter#getView(int, View, ViewGroup)](Adapter.md)) 

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
| `context` | [Context](../android.content/Context.md)!:Interface to application's global information |
| `cursor` | [Cursor](../android.database/Cursor.md)!:The cursor from which to get the data. The cursor is already moved to the correct position. |
| `parent` | [ViewGroup](../android.view/ViewGroup.md)!:The parent to which the new view is attached to |
| --- | --- |

| Return ||
|---------------------------------------------------------------------------------|-------------------------|
| [View](../android.view/View.md)! | the newly created view. |

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
| `context` | [Context](../android.content/Context.md)!:Interface to application's global information |
| `cursor` | [Cursor](../android.database/Cursor.md)!:The cursor from which to get the data. The cursor is already moved to the correct position. |
| `parent` | [ViewGroup](../android.view/ViewGroup.md)!:The parent to which the new view is attached to |
| --- | --- |

| Return ||
|---------------------------------------------------------------------------------|-------------------------|
| [View](../android.view/View.md)! | the newly created view. |

### runQueryOnBackgroundThread

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun runQueryOnBackgroundThread(constraint: CharSequence!): Cursor!
```

Runs a query with the specified constraint. This query is requested by the filter attached to this adapter. The query is provided by a [android.widget.FilterQueryProvider](FilterQueryProvider.md). If no provider is specified, the current cursor is not filtered and returned. After this method returns the resulting cursor is passed to [changeCursor(android.database.Cursor)](CursorAdapter.md))and the previous cursor is closed. This method is always executed on a background thread, not on the application's main thread (or UI thread.) Contract: when constraint is null or empty, the original results, prior to any filtering, must be returned. 
This method may take several seconds to complete, so it should only be called from a worker thread.

| Parameters ||
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| `constraint` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:the constraint with which the query must be filtered |

| Return ||
|-----------------------------------------------------------------------------------------|----------------------------------------------------|
| [Cursor](../android.database/Cursor.md)! | a Cursor representing the results of the new query |

**See Also**

- <https://developer.android.com/reference/kotlin/android/widget/CursorAdapter#getFilter()>
- <https://developer.android.com/reference/kotlin/android/widget/CursorAdapter#getFilterQueryProvider()>
- <https://developer.android.com/reference/kotlin/android/widget/CursorAdapter#setFilterQueryProvider(android.widget.FilterQueryProvider)> 

### setDropDownViewTheme

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setDropDownViewTheme(theme: Resources.Theme?): Unit
```

Sets the [Resources.Theme](../android/content/res/Resources.Theme.md) against which drop-down views are inflated.

By default, drop-down views are inflated against the theme of the [Context](../android.content/Context.md) passed to the adapter's constructor.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `theme` | [Resources.Theme](../android/content/res/Resources.Theme.md)?:the theme against which to inflate drop-down views or`null`to use the theme from the adapter's context |

**See Also**

- [#newDropDownView(Context, Cursor, ViewGroup)](CursorAdapter.md)) 

### setFilterQueryProvider

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setFilterQueryProvider(filterQueryProvider: FilterQueryProvider!): Unit
```

Sets the query filter provider used to filter the current Cursor. The provider's [android.widget.FilterQueryProvider#runQuery(CharSequence)](FilterQueryProvider.md))method is invoked when filtering is requested by a client of this adapter.

| Parameters ||
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `filterQueryProvider` | [FilterQueryProvider](FilterQueryProvider.md)!:the filter query provider or null to remove it |

**See Also**

- <https://developer.android.com/reference/kotlin/android/widget/CursorAdapter#getFilterQueryProvider()>
- [#runQueryOnBackgroundThread(CharSequence)](CursorAdapter.md)) 

### swapCursor

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun swapCursor(newCursor: Cursor!): Cursor!
```

Swap in a new Cursor, returning the old Cursor. Unlike [changeCursor(android.database.Cursor)](CursorAdapter.md)), the returned old Cursor is*not*closed.

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------------------------|
| `newCursor` | [Cursor](../android.database/Cursor.md)!:The new cursor to be used. |

| Return ||
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Cursor](../android.database/Cursor.md)! | Returns the previously set Cursor, or null if there was not one. If the given new Cursor is the same instance is the previously set Cursor, null is also returned. |

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

Called when the [ContentObserver](../android.database/ContentObserver.md) on the cursor receives a change notification. The default implementation provides the auto-requery logic, but may be overridden by sub classes. 
**See Also**

- [android.database.ContentObserver#onChange(boolean)](../android.database/ContentObserver.md))
