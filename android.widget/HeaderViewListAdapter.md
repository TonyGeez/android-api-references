# HeaderViewListAdapter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# HeaderViewListAdapter

Kotlin| [Java](https://developer.android.com/reference/android/widget/HeaderViewListAdapter "View this page in Java") 
| --- | --- |

```
open class HeaderViewListAdapter : Filterable, WrapperListAdapter
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.widget.HeaderViewListAdapter](https://developer.android.com/reference/kotlin/android/widget/HeaderViewListAdapter#) |

ListAdapter used when a ListView has header views. This ListAdapter wraps another one and also keeps track of the header views and their associated data objects.

This is intended as a base class; you will probably not need to use this class directly in your own code.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [HeaderViewListAdapter](https://developer.android.com/reference/kotlin/android/widget/HeaderViewListAdapter#HeaderViewListAdapter(java.util.ArrayList,%20java.util.ArrayList,%20android.widget.ListAdapter))`(`headerViewInfos:` ` [ArrayList](https://developer.android.com/reference/kotlin/java/util/ArrayList.html#)< [ListView.FixedViewInfo](https://developer.android.com/reference/kotlin/android/widget/ListView.FixedViewInfo)!>!`, `footerViewInfos:` ` [ArrayList](https://developer.android.com/reference/kotlin/java/util/ArrayList.html#)< [ListView.FixedViewInfo](https://developer.android.com/reference/kotlin/android/widget/ListView.FixedViewInfo)!>!`, `adapter:` ` [ListAdapter](https://developer.android.com/reference/kotlin/android/widget/ListAdapter)!`)` <br /> |

| Public methods ||
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [areAllItemsEnabled](https://developer.android.com/reference/kotlin/android/widget/HeaderViewListAdapter#areAllItemsEnabled())`()` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getCount](https://developer.android.com/reference/kotlin/android/widget/HeaderViewListAdapter#getCount())`()` <br /> |
| open [Filter](https://developer.android.com/reference/kotlin/android/widget/Filter)! | [getFilter](https://developer.android.com/reference/kotlin/android/widget/HeaderViewListAdapter#getFilter())`()` <br /> |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getFootersCount](https://developer.android.com/reference/kotlin/android/widget/HeaderViewListAdapter#getFootersCount())`()` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getHeadersCount](https://developer.android.com/reference/kotlin/android/widget/HeaderViewListAdapter#getHeadersCount())`()` <br /> |
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getItem](https://developer.android.com/reference/kotlin/android/widget/HeaderViewListAdapter#getItem(kotlin.Int))`(`position:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getItemId](https://developer.android.com/reference/kotlin/android/widget/HeaderViewListAdapter#getItemId(kotlin.Int))`(`position:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getItemViewType](https://developer.android.com/reference/kotlin/android/widget/HeaderViewListAdapter#getItemViewType(kotlin.Int))`(`position:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [View](https://developer.android.com/reference/kotlin/android/view/View.html#)! | [getView](https://developer.android.com/reference/kotlin/android/widget/HeaderViewListAdapter#getView(kotlin.Int,%20android.view.View,%20android.view.ViewGroup))`(`position:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `convertView:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!`, `parent:` ` [ViewGroup](https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#)!`)` <br /> |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getViewTypeCount](https://developer.android.com/reference/kotlin/android/widget/HeaderViewListAdapter#getViewTypeCount())`()` <br /> |
| open [ListAdapter](https://developer.android.com/reference/kotlin/android/widget/ListAdapter)! | [getWrappedAdapter](https://developer.android.com/reference/kotlin/android/widget/HeaderViewListAdapter#getWrappedAdapter())`()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasStableIds](https://developer.android.com/reference/kotlin/android/widget/HeaderViewListAdapter#hasStableIds())`()` <br /> |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEmpty](https://developer.android.com/reference/kotlin/android/widget/HeaderViewListAdapter#isEmpty())`()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEnabled](https://developer.android.com/reference/kotlin/android/widget/HeaderViewListAdapter#isEnabled(kotlin.Int))`(`position:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerDataSetObserver](https://developer.android.com/reference/kotlin/android/widget/HeaderViewListAdapter#registerDataSetObserver(android.database.DataSetObserver))`(`observer:` ` [DataSetObserver](https://developer.android.com/reference/kotlin/android/database/DataSetObserver.html#)!`)` <br /> |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [removeFooter](https://developer.android.com/reference/kotlin/android/widget/HeaderViewListAdapter#removeFooter(android.view.View))`(`v:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!`)` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [removeHeader](https://developer.android.com/reference/kotlin/android/widget/HeaderViewListAdapter#removeHeader(android.view.View))`(`v:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unregisterDataSetObserver](https://developer.android.com/reference/kotlin/android/widget/HeaderViewListAdapter#unregisterDataSetObserver(android.database.DataSetObserver))`(`observer:` ` [DataSetObserver](https://developer.android.com/reference/kotlin/android/database/DataSetObserver.html#)!`)` <br /> |
| --- | --- |

## Public constructors

### HeaderViewListAdapter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
HeaderViewListAdapter(
    headerViewInfos: ArrayList<ListView.FixedViewInfo!>!, 
    footerViewInfos: ArrayList<ListView.FixedViewInfo!>!, 
    adapter: ListAdapter!)
```

## Public methods

### areAllItemsEnabled

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun areAllItemsEnabled(): Boolean
```

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if all items are enabled, false otherwise. |

### getCount

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getCount(): Int
```

| Return ||
|----------------------------------------------------------------------------|-----------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Count of items. |

### getFilter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getFilter(): Filter!
```

| Return ||
|---------------------------------------------------------------------------------|---------------------------------|
| [Filter](https://developer.android.com/reference/kotlin/android/widget/Filter)! | a filter used to constrain data |

### getFootersCount

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getFootersCount(): Int
```  

### getHeadersCount

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getHeadersCount(): Int
```  

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

### getItemViewType

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getItemViewType(position: Int): Int
```

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `position` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The position of the item within the adapter's data set whose view type we want. |

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | An integer representing the type of View. Two views should share the same type if one can be converted to the other in [getView](https://developer.android.com/reference/kotlin/android/widget/Adapter#getView(kotlin.Int,%20android.view.View,%20android.view.ViewGroup)). Note: Integers must be in the range 0 to [getViewTypeCount](https://developer.android.com/reference/kotlin/android/widget/Adapter#getViewTypeCount())- 1. [IGNORE_ITEM_VIEW_TYPE](https://developer.android.com/reference/kotlin/android/widget/Adapter#IGNORE_ITEM_VIEW_TYPE:kotlin.Int) can also be returned. |

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
| --- | --- |

| Return ||
|---------------------------------------------------------------------------------|-------------------------------------------------------------|
| [View](https://developer.android.com/reference/kotlin/android/view/View.html#)! | A View corresponding to the data at the specified position. |

### getViewTypeCount

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getViewTypeCount(): Int
```

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The number of types of Views that will be created by this adapter |

### getWrappedAdapter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getWrappedAdapter(): ListAdapter!
```

| Return ||
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [ListAdapter](https://developer.android.com/reference/kotlin/android/widget/ListAdapter)! | The [android.widget.ListAdapter](https://developer.android.com/reference/kotlin/android/widget/ListAdapter) wrapped by this adapter. |

### hasStableIds

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hasStableIds(): Boolean
```

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if the same id always refers to the same object. |

### isEmpty

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isEmpty(): Boolean
```

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if this adapter doesn't contain any data. This is used to determine whether the empty view should be displayed. A typical implementation will return getCount() == 0 but since getCount() includes the headers and footers, specialized adapters might want a different behavior. |

### isEnabled

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isEnabled(position: Int): Boolean
```

| Parameters ||
|------------|----------------------------------------------------------------------------------------------|
| `position` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Index of the item |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if the item is not a separator |

### registerDataSetObserver

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun registerDataSetObserver(observer: DataSetObserver!): Unit
```

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `observer` | [DataSetObserver](https://developer.android.com/reference/kotlin/android/database/DataSetObserver.html#)!:the object that gets notified when the data set changes. |

### removeFooter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun removeFooter(v: View!): Boolean
```  

### removeHeader

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun removeHeader(v: View!): Boolean
```  

### unregisterDataSetObserver

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun unregisterDataSetObserver(observer: DataSetObserver!): Unit
```

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------|
| `observer` | [DataSetObserver](https://developer.android.com/reference/kotlin/android/database/DataSetObserver.html#)!:the object to unregister. |
