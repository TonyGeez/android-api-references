# ResourceCursorAdapter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ResourceCursorAdapter

Kotlin | [Java](../android/widget/ResourceCursorAdapter.md) 
| --- | --- |

```
abstract class ResourceCursorAdapter : CursorAdapter
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [android.widget.BaseAdapter](../android/widget/BaseAdapter.md) |||
| | ↳ | [android.widget.CursorAdapter](../android/widget/CursorAdapter.md) ||
| | | ↳ | [android.widget.ResourceCursorAdapter](../android/widget/ResourceCursorAdapter.md) |
| --- | --- | --- | --- |

| Known Direct Subclasses [SimpleCursorAdapter](../android/widget/SimpleCursorAdapter.md) |----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------| | [SimpleCursorAdapter](../android/widget/SimpleCursorAdapter.md) | An easy adapter to map columns from a cursor to TextViews or ImageViews defined in an XML file. | |
| --- | --- | --- | --- | --- | --- | --- |

An easy adapter that creates views defined in an XML file. You can specify the XML file that defines the appearance of the views.

## Summary

| Inherited constants ||
|---|---|
| From class [CursorAdapter](../android/widget/CursorAdapter.md) |----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FLAG_AUTO_REQUERY](../android/widget/CursorAdapter.md) If set the adapter will call requery() on the cursor whenever a content change notification is delivered. Implies [FLAG_REGISTER_CONTENT_OBSERVER](../android/widget/CursorAdapter.md). <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FLAG_REGISTER_CONTENT_OBSERVER](../android/widget/CursorAdapter.md) If set the adapter will register a content observer on the cursor and will call [onContentChanged()](../android/widget/CursorAdapter.md)) when a notification comes in. Be careful when using this flag: you will need to unset the current Cursor from the adapter to avoid leaks due to its registered observers. This flag is not needed when using a CursorAdapter with a [android.content.CursorLoader](../android/content/CursorLoader.md). <br /> | ||

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ResourceCursorAdapter](../android/widget/ResourceCursorAdapter.md))`(`context:` ` [Context](../android/content/Context.md)!`, `layout:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `c:` ` [Cursor](../android/database/Cursor.md)!`)` Constructor the enables auto-requery. |
| [ResourceCursorAdapter](../android/widget/ResourceCursorAdapter.md))`(`context:` ` [Context](../android/content/Context.md)!`, `layout:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `c:` ` [Cursor](../android/database/Cursor.md)!`, `autoRequery:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Constructor with default behavior as per [CursorAdapter.CursorAdapter(Context, Cursor, boolean)](../android/widget/CursorAdapter.md)); it is recommended you not use this, but instead [ResourceCursorAdapter(android.content.Context,int,android.database.Cursor,int)](../android/widget/ResourceCursorAdapter.md)). |
| [ResourceCursorAdapter](../android/widget/ResourceCursorAdapter.md))`(`context:` ` [Context](../android/content/Context.md)!`, `layout:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `c:` ` [Cursor](../android/database/Cursor.md)!`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Standard constructor. |

| Public methods ||
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [View](../android/view/View.md)! | [newDropDownView](../android/widget/ResourceCursorAdapter.md))`(`context:` ` [Context](../android/content/Context.md)!`, `cursor:` ` [Cursor](../android/database/Cursor.md)!`, `parent:` ` [ViewGroup](../android/view/ViewGroup.md)!`)` <br /> |
| open [View](../android/view/View.md)! | [newView](../android/widget/ResourceCursorAdapter.md))`(`context:` ` [Context](../android/content/Context.md)!`, `cursor:` ` [Cursor](../android/database/Cursor.md)!`, `parent:` ` [ViewGroup](../android/view/ViewGroup.md)!`)` Inflates view(s) from the specified XML file. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDropDownViewResource](../android/widget/ResourceCursorAdapter.md))`(`dropDownLayout:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the layout resource of the drop down views. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDropDownViewTheme](../android/widget/ResourceCursorAdapter.md))`(`theme:` ` [Resources.Theme](../android/content/res/Resources.Theme.md)?`)` Sets the [android.content.res.Resources.Theme](../android/content/res/Resources.Theme.md) against which drop-down views are inflated. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setViewResource](../android/widget/ResourceCursorAdapter.md))`(`layout:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the layout resource of the item views. |

| Inherited functions ||
|---|---|
| From class [BaseAdapter](../android/widget/BaseAdapter.md) |---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [areAllItemsEnabled](../android/widget/BaseAdapter.md))`()` <br /> | | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!>? | [getAutofillOptions](../android/widget/BaseAdapter.md))`()` <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getItemViewType](../android/widget/BaseAdapter.md))`(`position:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getViewTypeCount](../android/widget/BaseAdapter.md))`()` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEmpty](../android/widget/BaseAdapter.md))`()` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEnabled](../android/widget/BaseAdapter.md))`(`position:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [notifyDataSetChanged](../android/widget/BaseAdapter.md))`()` Notifies the attached observers that the underlying data has been changed and any View reflecting the data set should refresh itself. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [notifyDataSetInvalidated](../android/widget/BaseAdapter.md))`()` Notifies the attached observers that the underlying data is no longer valid or available. Once invoked this adapter is no longer valid and should not report further data set changes. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerDataSetObserver](../android/widget/BaseAdapter.md))`(`observer:` ` [DataSetObserver](../android/database/DataSetObserver.md)!`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAutofillOptions](../android/widget/BaseAdapter.md))`(`vararg` `options:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` Sets the value returned by [getAutofillOptions()](../android/widget/BaseAdapter.md)) <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unregisterDataSetObserver](../android/widget/BaseAdapter.md))`(`observer:` ` [DataSetObserver](../android/database/DataSetObserver.md)!`)` <br /> | ||
| From class [CursorAdapter](../android/widget/CursorAdapter.md) |--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [bindView](../android/widget/CursorAdapter.md))`(`view:` ` [View](../android/view/View.md)!`, `context:` ` [Context](../android/content/Context.md)!`, `cursor:` ` [Cursor](../android/database/Cursor.md)!`)` Bind an existing view to the data pointed to by cursor <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [changeCursor](../android/widget/CursorAdapter.md))`(`cursor:` ` [Cursor](../android/database/Cursor.md)!`)` Change the underlying cursor to a new cursor. If there is an existing cursor it will be closed. <br /> | | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | [convertToString](../android/widget/CursorAdapter.md))`(`cursor:` ` [Cursor](../android/database/Cursor.md)!`)` Converts the cursor into a CharSequence. Subclasses should override this method to convert their results. The default implementation returns an empty String for null values or the default String representation of the value. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getCount](../android/widget/CursorAdapter.md))`()` <br /> | | [Cursor](../android/database/Cursor.md)! | [getCursor](../android/widget/CursorAdapter.md))`()` Returns the cursor. <br /> | | [View](../android/view/View.md)! | [getDropDownView](../android/widget/CursorAdapter.md))`(`position:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `convertView:` ` [View](../android/view/View.md)!`, `parent:` ` [ViewGroup](../android/view/ViewGroup.md)!`)` <br /> | | [Resources.Theme](../android/content/res/Resources.Theme.md)? | [getDropDownViewTheme](../android/widget/CursorAdapter.md))`()` <br /> | | [Filter](../android/widget/Filter.md)! | [getFilter](../android/widget/CursorAdapter.md))`()` <br /> | | [FilterQueryProvider](../android/widget/FilterQueryProvider.md)! | [getFilterQueryProvider](../android/widget/CursorAdapter.md))`()` Returns the query filter provider used for filtering. When the provider is null, no filtering occurs. <br /> | | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getItem](../android/widget/CursorAdapter.md))`(`position:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> | | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getItemId](../android/widget/CursorAdapter.md))`(`position:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> | | [View](../android/view/View.md)! | [getView](../android/widget/CursorAdapter.md))`(`position:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `convertView:` ` [View](../android/view/View.md)!`, `parent:` ` [ViewGroup](../android/view/ViewGroup.md)!`)` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasStableIds](../android/widget/CursorAdapter.md))`()` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [init](../android/widget/CursorAdapter.md))`(`context:` ` [Context](../android/content/Context.md)!`, `c:` ` [Cursor](../android/database/Cursor.md)!`, `autoRequery:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onContentChanged](../android/widget/CursorAdapter.md))`()` Called when the [ContentObserver](../android/database/ContentObserver.md) on the cursor receives a change notification. The default implementation provides the auto-requery logic, but may be overridden by sub classes. <br /> | | [Cursor](../android/database/Cursor.md)! | [runQueryOnBackgroundThread](../android/widget/CursorAdapter.md))`(`constraint:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` Runs a query with the specified constraint. This query is requested by the filter attached to this adapter. The query is provided by a [android.widget.FilterQueryProvider](../android/widget/FilterQueryProvider.md). If no provider is specified, the current cursor is not filtered and returned. After this method returns the resulting cursor is passed to [changeCursor(android.database.Cursor)](../android/widget/CursorAdapter.md)) and the previous cursor is closed. This method is always executed on a background thread, not on the application's main thread (or UI thread.) Contract: when constraint is null or empty, the original results, prior to any filtering, must be returned. This method may take several seconds to complete, so it should only be called from a worker thread. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFilterQueryProvider](../android/widget/CursorAdapter.md))`(`filterQueryProvider:` ` [FilterQueryProvider](../android/widget/FilterQueryProvider.md)!`)` Sets the query filter provider used to filter the current Cursor. The provider's [android.widget.FilterQueryProvider#runQuery(CharSequence)](../android/widget/FilterQueryProvider.md)) method is invoked when filtering is requested by a client of this adapter. <br /> | | [Cursor](../android/database/Cursor.md)! | [swapCursor](../android/widget/CursorAdapter.md))`(`newCursor:` ` [Cursor](../android/database/Cursor.md)!`)` Swap in a new Cursor, returning the old Cursor. Unlike [changeCursor(android.database.Cursor)](../android/widget/CursorAdapter.md)), the returned old Cursor is *not* closed. <br /> | ||

## Public constructors

### ResourceCursorAdapter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ResourceCursorAdapter(
    context: Context!, 
    layout: Int, 
    c: Cursor!)
```

**Deprecated:** *This option is discouraged, as it results in Cursor queries being performed on the application's UI thread and thus can cause poor responsiveness or even Application Not Responding errors. As an alternative, use [android.app.LoaderManager](../android/app/LoaderManager.md) with a [android.content.CursorLoader](../android/content/CursorLoader.md).*

Constructor the enables auto-requery.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android/content/Context.md)!: The context where the ListView associated with this adapter is running |
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

Constructor with default behavior as per [CursorAdapter.CursorAdapter(Context, Cursor, boolean)](../android/widget/CursorAdapter.md)); it is recommended you not use this, but instead [ResourceCursorAdapter(android.content.Context,int,android.database.Cursor,int)](../android/widget/ResourceCursorAdapter.md)). When using this constructor, [FLAG_REGISTER_CONTENT_OBSERVER](../android/widget/CursorAdapter.md) will always be set.

| Parameters ||
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android/content/Context.md)!: The context where the ListView associated with this adapter is running |
| `layout` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): resource identifier of a layout file that defines the views for this list item. Unless you override them later, this will define both the item views and the drop down views. |
| `c` | [Cursor](../android/database/Cursor.md)!: The cursor from which to get the data. |
| --- | --- |
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
| `context` | [Context](../android/content/Context.md)!: The context where the ListView associated with this adapter is running |
| `layout` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Resource identifier of a layout file that defines the views for this list item. Unless you override them later, this will define both the item views and the drop down views. |
| `c` | [Cursor](../android/database/Cursor.md)!: The cursor from which to get the data. |
| --- | --- |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Flags used to determine the behavior of the adapter, as per [CursorAdapter.CursorAdapter(Context, Cursor, int)](../android/widget/CursorAdapter.md)). |

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
| `context` | [Context](../android/content/Context.md)!: Interface to application's global information |
| `cursor` | [Cursor](../android/database/Cursor.md)!: The cursor from which to get the data. The cursor is already moved to the correct position. |
| `parent` | [ViewGroup](../android/view/ViewGroup.md)!: The parent to which the new view is attached to |
| --- | --- |

| Return ||
|---------------------------------------------------------------------------------|-------------------------|
| [View](../android/view/View.md)! | the newly created view. |

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
| `context` | [Context](../android/content/Context.md)!: Interface to application's global information |
| `cursor` | [Cursor](../android/database/Cursor.md)!: The cursor from which to get the data. The cursor is already moved to the correct position. |
| `parent` | [ViewGroup](../android/view/ViewGroup.md)!: The parent to which the new view is attached to |
| --- | --- |

| Return ||
|---------------------------------------------------------------------------------|-------------------------|
| [View](../android/view/View.md)! | the newly created view. |

**See Also**

- [android.widget.CursorAdapter#newView(android.content.Context,
* android.database.Cursor, ViewGroup)](../android/widget/CursorAdapter.md)) 

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

Sets the [android.content.res.Resources.Theme](../android/content/res/Resources.Theme.md) against which drop-down views are inflated.

By default, drop-down views are inflated against the theme of the [Context](../android/content/Context.md) passed to the adapter's constructor.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `theme` | [Resources.Theme](../android/content/res/Resources.Theme.md)?: the theme against which to inflate drop-down views or `null` to use the theme from the adapter's context |

**See Also**

- [#newDropDownView(Context, Cursor, ViewGroup)](../android/widget/ResourceCursorAdapter.md)) 

### setViewResource

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setViewResource(layout: Int): Unit
```

Sets the layout resource of the item views.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------|
| `layout` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the layout resources used to create item views |
