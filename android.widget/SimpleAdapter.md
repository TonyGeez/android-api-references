# SimpleAdapter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SimpleAdapter

Kotlin | [Java](https://developer.android.com/reference/android/widget/SimpleAdapter "View this page in Java") 

```
open class SimpleAdapter : BaseAdapter, Filterable, ThemedSpinnerAdapter
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| ↳ | [android.widget.BaseAdapter](https://developer.android.com/reference/kotlin/android/widget/BaseAdapter) ||
| | ↳ | [android.widget.SimpleAdapter](https://developer.android.com/reference/kotlin/android/widget/SimpleAdapter#) |

An easy adapter to map static data to views defined in an XML file. You can specify the data backing the list as an ArrayList of Maps. Each entry in the ArrayList corresponds to one row in the list. The Maps contain the data for each row. You also specify an XML file that defines the views used to display the row, and a mapping from keys in the Map to specific views. Binding data to views occurs in two phases. First, if a [android.widget.SimpleAdapter.ViewBinder](https://developer.android.com/reference/kotlin/android/widget/SimpleAdapter.ViewBinder) is available, [ViewBinder.setViewValue(android.view.View, Object, String)](https://developer.android.com/reference/kotlin/android/widget/SimpleAdapter.ViewBinder#setViewValue(android.view.View,%20kotlin.Any,%20kotlin.String)) is invoked. If the returned value is true, binding has occurred. If the returned value is false, the following views are then tried in order:

- A view that implements Checkable (e.g. CheckBox). The expected bind value is a boolean.
- TextView. The expected bind value is a string and [setViewText(android.widget.TextView,java.lang.String)](https://developer.android.com/reference/kotlin/android/widget/SimpleAdapter#setViewText(android.widget.TextView,%20kotlin.String)) is invoked.
- ImageView. The expected bind value is a resource id or a string and [setViewImage(android.widget.ImageView,int)](https://developer.android.com/reference/kotlin/android/widget/SimpleAdapter#setViewImage(android.widget.ImageView,%20kotlin.Int)) or [setViewImage(android.widget.ImageView,java.lang.String)](https://developer.android.com/reference/kotlin/android/widget/SimpleAdapter#setViewImage(android.widget.ImageView,%20kotlin.String)) is invoked.

If no appropriate binding can be found, an [IllegalStateException](https://developer.android.com/reference/kotlin/java/lang/IllegalStateException.html#) is thrown.

<br />

## Summary

| Nested classes ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [ViewBinder](https://developer.android.com/reference/kotlin/android/widget/SimpleAdapter.ViewBinder) This class can be used by external clients of SimpleAdapter to bind values to views. |

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SimpleAdapter](https://developer.android.com/reference/kotlin/android/widget/SimpleAdapter#SimpleAdapter(android.content.Context,%20kotlin.collections.MutableList,%20kotlin.Int,%20kotlin.Array,%20kotlin.IntArray))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`, `data:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)<out` ` [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!,` `*>!>!`, `resource:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `from:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`, `to:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!`)` Constructor |

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getCount](https://developer.android.com/reference/kotlin/android/widget/SimpleAdapter#getCount())`()` <br /> |
| open [View](https://developer.android.com/reference/kotlin/android/view/View.html#)! | [getDropDownView](https://developer.android.com/reference/kotlin/android/widget/SimpleAdapter#getDropDownView(kotlin.Int,%20android.view.View,%20android.view.ViewGroup))`(`position:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `convertView:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!`, `parent:` ` [ViewGroup](https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#)!`)` <br /> |
| open [Resources.Theme](https://developer.android.com/reference/kotlin/android/content/res/Resources.Theme.html#)? | [getDropDownViewTheme](https://developer.android.com/reference/kotlin/android/widget/SimpleAdapter#getDropDownViewTheme())`()` <br /> |
| open [Filter](https://developer.android.com/reference/kotlin/android/widget/Filter)! | [getFilter](https://developer.android.com/reference/kotlin/android/widget/SimpleAdapter#getFilter())`()` <br /> |
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getItem](https://developer.android.com/reference/kotlin/android/widget/SimpleAdapter#getItem(kotlin.Int))`(`position:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getItemId](https://developer.android.com/reference/kotlin/android/widget/SimpleAdapter#getItemId(kotlin.Int))`(`position:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [View](https://developer.android.com/reference/kotlin/android/view/View.html#)! | [getView](https://developer.android.com/reference/kotlin/android/widget/SimpleAdapter#getView(kotlin.Int,%20android.view.View,%20android.view.ViewGroup))`(`position:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `convertView:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!`, `parent:` ` [ViewGroup](https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#)!`)` <br /> |
| open [SimpleAdapter.ViewBinder](https://developer.android.com/reference/kotlin/android/widget/SimpleAdapter.ViewBinder)! | [getViewBinder](https://developer.android.com/reference/kotlin/android/widget/SimpleAdapter#getViewBinder())`()` Returns the [ViewBinder](https://developer.android.com/reference/kotlin/android/widget/SimpleAdapter.ViewBinder) used to bind data to views. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDropDownViewResource](https://developer.android.com/reference/kotlin/android/widget/SimpleAdapter#setDropDownViewResource(kotlin.Int))`(`resource:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the layout resource to create the drop down views. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDropDownViewTheme](https://developer.android.com/reference/kotlin/android/widget/SimpleAdapter#setDropDownViewTheme(android.content.res.Resources.Theme))`(`theme:` ` [Resources.Theme](https://developer.android.com/reference/kotlin/android/content/res/Resources.Theme.html#)?`)` Sets the [android.content.res.Resources.Theme](https://developer.android.com/reference/kotlin/android/content/res/Resources.Theme.html#) against which drop-down views are inflated. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setViewBinder](https://developer.android.com/reference/kotlin/android/widget/SimpleAdapter#setViewBinder(android.widget.SimpleAdapter.ViewBinder))`(`viewBinder:` ` [SimpleAdapter.ViewBinder](https://developer.android.com/reference/kotlin/android/widget/SimpleAdapter.ViewBinder)!`)` Sets the binder used to bind data to views. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setViewImage](https://developer.android.com/reference/kotlin/android/widget/SimpleAdapter#setViewImage(android.widget.ImageView,%20kotlin.Int))`(`v:` ` [ImageView](https://developer.android.com/reference/kotlin/android/widget/ImageView)!`, `value:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called by bindView() to set the image for an ImageView but only if there is no existing ViewBinder or if the existing ViewBinder cannot handle binding to an ImageView. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setViewImage](https://developer.android.com/reference/kotlin/android/widget/SimpleAdapter#setViewImage(android.widget.ImageView,%20kotlin.String))`(`v:` ` [ImageView](https://developer.android.com/reference/kotlin/android/widget/ImageView)!`, `value:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Called by bindView() to set the image for an ImageView but only if there is no existing ViewBinder or if the existing ViewBinder cannot handle binding to an ImageView. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setViewText](https://developer.android.com/reference/kotlin/android/widget/SimpleAdapter#setViewText(android.widget.TextView,%20kotlin.String))`(`v:` ` [TextView](https://developer.android.com/reference/kotlin/android/widget/TextView)!`, `text:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Called by bindView() to set the text for a TextView but only if there is no existing ViewBinder or if the existing ViewBinder cannot handle binding to a TextView. |

| Inherited functions ||
|---|---|
| From class [BaseAdapter](https://developer.android.com/reference/kotlin/android/widget/BaseAdapter) |---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [areAllItemsEnabled](https://developer.android.com/reference/kotlin/android/widget/BaseAdapter#areAllItemsEnabled())`()` <br /> | | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!>? | [getAutofillOptions](https://developer.android.com/reference/kotlin/android/widget/BaseAdapter#getAutofillOptions())`()` <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getItemViewType](https://developer.android.com/reference/kotlin/android/widget/BaseAdapter#getItemViewType(kotlin.Int))`(`position:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getViewTypeCount](https://developer.android.com/reference/kotlin/android/widget/BaseAdapter#getViewTypeCount())`()` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasStableIds](https://developer.android.com/reference/kotlin/android/widget/BaseAdapter#hasStableIds())`()` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEmpty](https://developer.android.com/reference/kotlin/android/widget/BaseAdapter#isEmpty())`()` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEnabled](https://developer.android.com/reference/kotlin/android/widget/BaseAdapter#isEnabled(kotlin.Int))`(`position:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [notifyDataSetChanged](https://developer.android.com/reference/kotlin/android/widget/BaseAdapter#notifyDataSetChanged())`()` Notifies the attached observers that the underlying data has been changed and any View reflecting the data set should refresh itself. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [notifyDataSetInvalidated](https://developer.android.com/reference/kotlin/android/widget/BaseAdapter#notifyDataSetInvalidated())`()` Notifies the attached observers that the underlying data is no longer valid or available. Once invoked this adapter is no longer valid and should not report further data set changes. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerDataSetObserver](https://developer.android.com/reference/kotlin/android/widget/BaseAdapter#registerDataSetObserver(android.database.DataSetObserver))`(`observer:` ` [DataSetObserver](https://developer.android.com/reference/kotlin/android/database/DataSetObserver.html#)!`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAutofillOptions](https://developer.android.com/reference/kotlin/android/widget/BaseAdapter#setAutofillOptions(kotlin.CharSequence))`(`vararg` `options:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` Sets the value returned by [getAutofillOptions()](https://developer.android.com/reference/kotlin/android/widget/BaseAdapter#getAutofillOptions()) <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unregisterDataSetObserver](https://developer.android.com/reference/kotlin/android/widget/BaseAdapter#unregisterDataSetObserver(android.database.DataSetObserver))`(`observer:` ` [DataSetObserver](https://developer.android.com/reference/kotlin/android/database/DataSetObserver.html#)!`)` <br /> | ||

## Public constructors

### SimpleAdapter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SimpleAdapter(
    context: Context!, 
    data: MutableList<out MutableMap<String!, *>!>!, 
    resource: Int, 
    from: Array<String!>!, 
    to: IntArray!)
```

Constructor

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!: The context where the View associated with this SimpleAdapter is running |
| `data` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\<out [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, \*\>!\>!: A List of Maps. Each entry in the List corresponds to one row in the list. The Maps contain the data for each row, and should include all the entries specified in "from" |
| `resource` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Resource identifier of a view layout that defines the views for this list item. The layout file should include at least those named views defined in "to" |
| `from` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!: A list of column names that will be added to the Map associated with each item. |
| `to` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!: The views that should display column in the "from" parameter. These should all be TextViews. The first N views in this list are given the values of the first N columns in the from parameter. |

## Public methods

### getCount

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getCount(): Int
```

| Return ||
|----------------------------------------------------------------------------|-----------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Count of items. |

**See Also**

- [android.widget.Adapter#getCount()](https://developer.android.com/reference/kotlin/android/widget/Adapter#getCount()) 

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
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `position` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): index of the item whose view we want. |
| `convertView` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!: the old view to reuse, if possible. Note: You should check that this view is non-null and of an appropriate type before using. If it is not possible to convert this view to display the correct data, this method can create a new view. |
| `parent` | [ViewGroup](https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#)!: the parent that this view will eventually be attached to |

| Return ||
|---------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| [View](https://developer.android.com/reference/kotlin/android/view/View.html#)! | a [android.view.View](https://developer.android.com/reference/kotlin/android/view/View.html#) corresponding to the data at the specified position. |

### getDropDownViewTheme

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDropDownViewTheme(): Resources.Theme?
```

| Return ||
|--------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Resources.Theme](https://developer.android.com/reference/kotlin/android/content/res/Resources.Theme.html#)? | the [Resources.Theme](https://developer.android.com/reference/kotlin/android/content/res/Resources.Theme.html#) against which drop-down views are inflated, or `null` if one has not been explicitly set |

### getFilter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getFilter(): Filter!
```

| Return ||
|---------------------------------------------------------------------------------|---------------------------------|
| [Filter](https://developer.android.com/reference/kotlin/android/widget/Filter)! | a filter used to constrain data |

### getItem

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getItem(position: Int): Any!
```

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| `position` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Position of the item whose data we want within the adapter's data set. |

| Return ||
|-----------------------------------------------------------------------------|-------------------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | The data at the specified position. |

**See Also**

- [android.widget.Adapter#getItem(int)](https://developer.android.com/reference/kotlin/android/widget/Adapter#getItem(kotlin.Int)) 

### getItemId

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getItemId(position: Int): Long
```

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `position` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The position of the item within the adapter's data set whose row id we want. |

| Return ||
|------------------------------------------------------------------------------|-----------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | The id of the item at the specified position. |

**See Also**

- [android.widget.Adapter#getItemId(int)](https://developer.android.com/reference/kotlin/android/widget/Adapter#getItemId(kotlin.Int)) 

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
|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `position` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The position of the item within the adapter's data set of the item whose view we want. |
| `convertView` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!: The old view to reuse, if possible. Note: You should check that this view is non-null and of an appropriate type before using. If it is not possible to convert this view to display the correct data, this method can create a new view. Heterogeneous lists can specify their number of view types, so that this View is always of the right type (see [getViewTypeCount()](https://developer.android.com/reference/kotlin/android/widget/Adapter#getViewTypeCount()) and [getItemViewType(int)](https://developer.android.com/reference/kotlin/android/widget/Adapter#getItemViewType(kotlin.Int))). |
| `parent` | [ViewGroup](https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#)!: The parent that this view will eventually be attached to |

| Return ||
|---------------------------------------------------------------------------------|-------------------------------------------------------------|
| [View](https://developer.android.com/reference/kotlin/android/view/View.html#)! | A View corresponding to the data at the specified position. |

**See Also**

- [android.widget.Adapter#getView(int, View, ViewGroup)](https://developer.android.com/reference/kotlin/android/widget/Adapter#getView(kotlin.Int,%20android.view.View,%20android.view.ViewGroup)) 

### getViewBinder

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getViewBinder(): SimpleAdapter.ViewBinder!
```

Returns the [ViewBinder](https://developer.android.com/reference/kotlin/android/widget/SimpleAdapter.ViewBinder) used to bind data to views.

| Return ||
|---------------------------------------------------------------------------------------------------------------------|---------------------------------------------------|
| [SimpleAdapter.ViewBinder](https://developer.android.com/reference/kotlin/android/widget/SimpleAdapter.ViewBinder)! | a ViewBinder or null if the binder does not exist |

**See Also**

- <https://developer.android.com/reference/kotlin/android/widget/SimpleAdapter#setViewBinder(android.widget.SimpleAdapter.ViewBinder)> 

### setDropDownViewResource

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setDropDownViewResource(resource: Int): Unit
```

Sets the layout resource to create the drop down views.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------|
| `resource` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the layout resource defining the drop down views |

**See Also**

- [#getDropDownView(int, android.view.View, android.view.ViewGroup)](https://developer.android.com/reference/kotlin/android/widget/SimpleAdapter#getDropDownView(kotlin.Int,%20android.view.View,%20android.view.ViewGroup)) 

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

- [#getDropDownView(int, View, ViewGroup)](https://developer.android.com/reference/kotlin/android/widget/SimpleAdapter#getDropDownView(kotlin.Int,%20android.view.View,%20android.view.ViewGroup)) 

### setViewBinder

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setViewBinder(viewBinder: SimpleAdapter.ViewBinder!): Unit
```

Sets the binder used to bind data to views.

| Parameters ||
|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `viewBinder` | [SimpleAdapter.ViewBinder](https://developer.android.com/reference/kotlin/android/widget/SimpleAdapter.ViewBinder)!: the binder used to bind data to views, can be null to remove the existing binder |

**See Also**

- <https://developer.android.com/reference/kotlin/android/widget/SimpleAdapter#getViewBinder()> 

### setViewImage

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setViewImage(
    v: ImageView!, 
    value: Int
): Unit
```

Called by bindView() to set the image for an ImageView but only if there is no existing ViewBinder or if the existing ViewBinder cannot handle binding to an ImageView. This method is called instead of [setViewImage(android.widget.ImageView,java.lang.String)](https://developer.android.com/reference/kotlin/android/widget/SimpleAdapter#setViewImage(android.widget.ImageView,%20kotlin.String)) if the supplied data is an int or Integer.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------|
| `v` | [ImageView](https://developer.android.com/reference/kotlin/android/widget/ImageView)!: ImageView to receive an image |
| `value` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the value retrieved from the data set |

**See Also**

- [#setViewImage(ImageView, String)](https://developer.android.com/reference/kotlin/android/widget/SimpleAdapter#setViewImage(android.widget.ImageView,%20kotlin.String)) 

### setViewImage

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setViewImage(
    v: ImageView!, 
    value: String!
): Unit
```

Called by bindView() to set the image for an ImageView but only if there is no existing ViewBinder or if the existing ViewBinder cannot handle binding to an ImageView. By default, the value will be treated as an image resource. If the value cannot be used as an image resource, the value is used as an image Uri. This method is called instead of [setViewImage(android.widget.ImageView,int)](https://developer.android.com/reference/kotlin/android/widget/SimpleAdapter#setViewImage(android.widget.ImageView,%20kotlin.Int)) if the supplied data is not an int or Integer.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------|
| `v` | [ImageView](https://developer.android.com/reference/kotlin/android/widget/ImageView)!: ImageView to receive an image |
| `value` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the value retrieved from the data set |

**See Also**

- [#setViewImage(ImageView, int)](https://developer.android.com/reference/kotlin/android/widget/SimpleAdapter#setViewImage(android.widget.ImageView,%20kotlin.Int)) 

### setViewText

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setViewText(
    v: TextView!, 
    text: String!
): Unit
```

Called by bindView() to set the text for a TextView but only if there is no existing ViewBinder or if the existing ViewBinder cannot handle binding to a TextView.

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------------------------|
| `v` | [TextView](https://developer.android.com/reference/kotlin/android/widget/TextView)!: TextView to receive text |
| `text` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the text to be set for the TextView |
