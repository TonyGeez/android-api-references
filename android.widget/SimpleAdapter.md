# SimpleAdapter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SimpleAdapter

Kotlin | [Java](../android/widget/SimpleAdapter.md) 
| --- | --- |

```
open class SimpleAdapter : BaseAdapter, Filterable, ThemedSpinnerAdapter
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.widget.BaseAdapter](../android/widget/BaseAdapter.md) ||
| | ↳ | [android.widget.SimpleAdapter](../android/widget/SimpleAdapter.md) |

An easy adapter to map static data to views defined in an XML file. You can specify the data backing the list as an ArrayList of Maps. Each entry in the ArrayList corresponds to one row in the list. The Maps contain the data for each row. You also specify an XML file that defines the views used to display the row, and a mapping from keys in the Map to specific views. Binding data to views occurs in two phases. First, if a [android.widget.SimpleAdapter.ViewBinder](../android/widget/SimpleAdapter.ViewBinder.md) is available, [ViewBinder.setViewValue(android.view.View, Object, String)](../android/widget/SimpleAdapter.ViewBinder.md)) is invoked. If the returned value is true, binding has occurred. If the returned value is false, the following views are then tried in order:

- A view that implements Checkable (e.g. CheckBox). The expected bind value is a boolean.
- TextView. The expected bind value is a string and [setViewText(android.widget.TextView,java.lang.String)](../android/widget/SimpleAdapter.md)) is invoked.
- ImageView. The expected bind value is a resource id or a string and [setViewImage(android.widget.ImageView,int)](../android/widget/SimpleAdapter.md)) or [setViewImage(android.widget.ImageView,java.lang.String)](../android/widget/SimpleAdapter.md)) is invoked.

If no appropriate binding can be found, an [IllegalStateException](../java/lang/IllegalStateException.md) is thrown.

<br />

## Summary

| Nested classes ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [ViewBinder](../android/widget/SimpleAdapter.ViewBinder.md) This class can be used by external clients of SimpleAdapter to bind values to views. |

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SimpleAdapter](../android/widget/SimpleAdapter.md))`(`context:` ` [Context](../android/content/Context.md)!`, `data:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)<out` ` [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!,` `*>!>!`, `resource:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `from:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`, `to:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!`)` Constructor |

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getCount](../android/widget/SimpleAdapter.md))`()` <br /> |
| open [View](../android/view/View.md)! | [getDropDownView](../android/widget/SimpleAdapter.md))`(`position:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `convertView:` ` [View](../android/view/View.md)!`, `parent:` ` [ViewGroup](../android/view/ViewGroup.md)!`)` <br /> |
| open [Resources.Theme](../android/content/res/Resources.Theme.md)? | [getDropDownViewTheme](../android/widget/SimpleAdapter.md))`()` <br /> |
| --- | --- |
| open [Filter](../android/widget/Filter.md)! | [getFilter](../android/widget/SimpleAdapter.md))`()` <br /> |
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getItem](../android/widget/SimpleAdapter.md))`(`position:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getItemId](../android/widget/SimpleAdapter.md))`(`position:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |
| open [View](../android/view/View.md)! | [getView](../android/widget/SimpleAdapter.md))`(`position:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `convertView:` ` [View](../android/view/View.md)!`, `parent:` ` [ViewGroup](../android/view/ViewGroup.md)!`)` <br /> |
| open [SimpleAdapter.ViewBinder](../android/widget/SimpleAdapter.ViewBinder.md)! | [getViewBinder](../android/widget/SimpleAdapter.md))`()` Returns the [ViewBinder](../android/widget/SimpleAdapter.ViewBinder.md) used to bind data to views. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDropDownViewResource](../android/widget/SimpleAdapter.md))`(`resource:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the layout resource to create the drop down views. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDropDownViewTheme](../android/widget/SimpleAdapter.md))`(`theme:` ` [Resources.Theme](../android/content/res/Resources.Theme.md)?`)` Sets the [android.content.res.Resources.Theme](../android/content/res/Resources.Theme.md) against which drop-down views are inflated. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setViewBinder](../android/widget/SimpleAdapter.md))`(`viewBinder:` ` [SimpleAdapter.ViewBinder](../android/widget/SimpleAdapter.ViewBinder.md)!`)` Sets the binder used to bind data to views. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setViewImage](../android/widget/SimpleAdapter.md))`(`v:` ` [ImageView](../android/widget/ImageView.md)!`, `value:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called by bindView() to set the image for an ImageView but only if there is no existing ViewBinder or if the existing ViewBinder cannot handle binding to an ImageView. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setViewImage](../android/widget/SimpleAdapter.md))`(`v:` ` [ImageView](../android/widget/ImageView.md)!`, `value:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Called by bindView() to set the image for an ImageView but only if there is no existing ViewBinder or if the existing ViewBinder cannot handle binding to an ImageView. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setViewText](../android/widget/SimpleAdapter.md))`(`v:` ` [TextView](../android/widget/TextView.md)!`, `text:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Called by bindView() to set the text for a TextView but only if there is no existing ViewBinder or if the existing ViewBinder cannot handle binding to a TextView. |

| Inherited functions ||
|---|---|
| From class [BaseAdapter](../android/widget/BaseAdapter.md) |---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [areAllItemsEnabled](../android/widget/BaseAdapter.md))`()` <br /> | | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!>? | [getAutofillOptions](../android/widget/BaseAdapter.md))`()` <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getItemViewType](../android/widget/BaseAdapter.md))`(`position:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getViewTypeCount](../android/widget/BaseAdapter.md))`()` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasStableIds](../android/widget/BaseAdapter.md))`()` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEmpty](../android/widget/BaseAdapter.md))`()` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEnabled](../android/widget/BaseAdapter.md))`(`position:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [notifyDataSetChanged](../android/widget/BaseAdapter.md))`()` Notifies the attached observers that the underlying data has been changed and any View reflecting the data set should refresh itself. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [notifyDataSetInvalidated](../android/widget/BaseAdapter.md))`()` Notifies the attached observers that the underlying data is no longer valid or available. Once invoked this adapter is no longer valid and should not report further data set changes. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerDataSetObserver](../android/widget/BaseAdapter.md))`(`observer:` ` [DataSetObserver](../android/database/DataSetObserver.md)!`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAutofillOptions](../android/widget/BaseAdapter.md))`(`vararg` `options:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` Sets the value returned by [getAutofillOptions()](../android/widget/BaseAdapter.md)) <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unregisterDataSetObserver](../android/widget/BaseAdapter.md))`(`observer:` ` [DataSetObserver](../android/database/DataSetObserver.md)!`)` <br /> | ||

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
| `context` | [Context](../android/content/Context.md)!: The context where the View associated with this SimpleAdapter is running |
| `data` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\<out [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, \*\>!\>!: A List of Maps. Each entry in the List corresponds to one row in the list. The Maps contain the data for each row, and should include all the entries specified in "from" |
| `resource` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Resource identifier of a view layout that defines the views for this list item. The layout file should include at least those named views defined in "to" |
| --- | --- |
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

- [android.widget.Adapter#getCount()](../android/widget/Adapter.md)) 

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
| `convertView` | [View](../android/view/View.md)!: the old view to reuse, if possible. Note: You should check that this view is non-null and of an appropriate type before using. If it is not possible to convert this view to display the correct data, this method can create a new view. |
| `parent` | [ViewGroup](../android/view/ViewGroup.md)!: the parent that this view will eventually be attached to |
| --- | --- |

| Return ||
|---------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| [View](../android/view/View.md)! | a [android.view.View](../android/view/View.md) corresponding to the data at the specified position. |

### getDropDownViewTheme

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDropDownViewTheme(): Resources.Theme?
```

| Return ||
|--------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Resources.Theme](../android/content/res/Resources.Theme.md)? | the [Resources.Theme](../android/content/res/Resources.Theme.md) against which drop-down views are inflated, or `null` if one has not been explicitly set |

### getFilter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getFilter(): Filter!
```

| Return ||
|---------------------------------------------------------------------------------|---------------------------------|
| [Filter](../android/widget/Filter.md)! | a filter used to constrain data |

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

- [android.widget.Adapter#getItem(int)](../android/widget/Adapter.md)) 

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

- [android.widget.Adapter#getItemId(int)](../android/widget/Adapter.md)) 

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
| `convertView` | [View](../android/view/View.md)!: The old view to reuse, if possible. Note: You should check that this view is non-null and of an appropriate type before using. If it is not possible to convert this view to display the correct data, this method can create a new view. Heterogeneous lists can specify their number of view types, so that this View is always of the right type (see [getViewTypeCount()](../android/widget/Adapter.md)) and [getItemViewType(int)](../android/widget/Adapter.md))). |
| `parent` | [ViewGroup](../android/view/ViewGroup.md)!: The parent that this view will eventually be attached to |
| --- | --- |

| Return ||
|---------------------------------------------------------------------------------|-------------------------------------------------------------|
| [View](../android/view/View.md)! | A View corresponding to the data at the specified position. |

**See Also**

- [android.widget.Adapter#getView(int, View, ViewGroup)](../android/widget/Adapter.md)) 

### getViewBinder

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getViewBinder(): SimpleAdapter.ViewBinder!
```

Returns the [ViewBinder](../android/widget/SimpleAdapter.ViewBinder.md) used to bind data to views.

| Return ||
|---------------------------------------------------------------------------------------------------------------------|---------------------------------------------------|
| [SimpleAdapter.ViewBinder](../android/widget/SimpleAdapter.ViewBinder.md)! | a ViewBinder or null if the binder does not exist |

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

- [#getDropDownView(int, android.view.View, android.view.ViewGroup)](../android/widget/SimpleAdapter.md)) 

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

- [#getDropDownView(int, View, ViewGroup)](../android/widget/SimpleAdapter.md)) 

### setViewBinder

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setViewBinder(viewBinder: SimpleAdapter.ViewBinder!): Unit
```

Sets the binder used to bind data to views.

| Parameters ||
|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `viewBinder` | [SimpleAdapter.ViewBinder](../android/widget/SimpleAdapter.ViewBinder.md)!: the binder used to bind data to views, can be null to remove the existing binder |

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

Called by bindView() to set the image for an ImageView but only if there is no existing ViewBinder or if the existing ViewBinder cannot handle binding to an ImageView. This method is called instead of [setViewImage(android.widget.ImageView,java.lang.String)](../android/widget/SimpleAdapter.md)) if the supplied data is an int or Integer.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------|
| `v` | [ImageView](../android/widget/ImageView.md)!: ImageView to receive an image |
| `value` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the value retrieved from the data set |

**See Also**

- [#setViewImage(ImageView, String)](../android/widget/SimpleAdapter.md)) 

### setViewImage

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setViewImage(
    v: ImageView!, 
    value: String!
): Unit
```

Called by bindView() to set the image for an ImageView but only if there is no existing ViewBinder or if the existing ViewBinder cannot handle binding to an ImageView. By default, the value will be treated as an image resource. If the value cannot be used as an image resource, the value is used as an image Uri. This method is called instead of [setViewImage(android.widget.ImageView,int)](../android/widget/SimpleAdapter.md)) if the supplied data is not an int or Integer.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------|
| `v` | [ImageView](../android/widget/ImageView.md)!: ImageView to receive an image |
| `value` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the value retrieved from the data set |

**See Also**

- [#setViewImage(ImageView, int)](../android/widget/SimpleAdapter.md)) 

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
| `v` | [TextView](../android/widget/TextView.md)!: TextView to receive text |
| `text` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the text to be set for the TextView |
