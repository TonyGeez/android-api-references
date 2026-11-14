# HeaderViewListAdapter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# HeaderViewListAdapter

Kotlin| [Java](HeaderViewListAdapter.md) 
| --- | --- |

```
open class HeaderViewListAdapter : Filterable, WrapperListAdapter
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.widget.HeaderViewListAdapter](HeaderViewListAdapter.md) |

ListAdapter used when a ListView has header views. This ListAdapter wraps another one and also keeps track of the header views and their associated data objects.

This is intended as a base class; you will probably not need to use this class directly in your own code.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [HeaderViewListAdapter](HeaderViewListAdapter.md))`(`headerViewInfos:` ` [ArrayList](../java.util/ArrayList.md)< [ListView.FixedViewInfo](../android/widget/ListView.FixedViewInfo.md)!>!`, `footerViewInfos:` ` [ArrayList](../java.util/ArrayList.md)< [ListView.FixedViewInfo](../android/widget/ListView.FixedViewInfo.md)!>!`, `adapter:` ` [ListAdapter](ListAdapter.md)!`)` <br /> |

| Public methods ||
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [areAllItemsEnabled](HeaderViewListAdapter.md))`()` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getCount](HeaderViewListAdapter.md))`()` <br /> |
| open [Filter](Filter.md)! | [getFilter](HeaderViewListAdapter.md))`()` <br /> |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getFootersCount](HeaderViewListAdapter.md))`()` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getHeadersCount](HeaderViewListAdapter.md))`()` <br /> |
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getItem](HeaderViewListAdapter.md))`(`position:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getItemId](HeaderViewListAdapter.md))`(`position:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getItemViewType](HeaderViewListAdapter.md))`(`position:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [View](../android.view/View.md)! | [getView](HeaderViewListAdapter.md))`(`position:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `convertView:` ` [View](../android.view/View.md)!`, `parent:` ` [ViewGroup](../android.view/ViewGroup.md)!`)` <br /> |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getViewTypeCount](HeaderViewListAdapter.md))`()` <br /> |
| open [ListAdapter](ListAdapter.md)! | [getWrappedAdapter](HeaderViewListAdapter.md))`()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasStableIds](HeaderViewListAdapter.md))`()` <br /> |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEmpty](HeaderViewListAdapter.md))`()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEnabled](HeaderViewListAdapter.md))`(`position:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerDataSetObserver](HeaderViewListAdapter.md))`(`observer:` ` [DataSetObserver](../android.database/DataSetObserver.md)!`)` <br /> |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [removeFooter](HeaderViewListAdapter.md))`(`v:` ` [View](../android.view/View.md)!`)` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [removeHeader](HeaderViewListAdapter.md))`(`v:` ` [View](../android.view/View.md)!`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unregisterDataSetObserver](HeaderViewListAdapter.md))`(`observer:` ` [DataSetObserver](../android.database/DataSetObserver.md)!`)` <br /> |
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
| [Filter](Filter.md)! | a filter used to constrain data |

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
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | An integer representing the type of View. Two views should share the same type if one can be converted to the other in [getView](Adapter.md)). Note: Integers must be in the range 0 to [getViewTypeCount](Adapter.md))- 1. [IGNORE_ITEM_VIEW_TYPE](Adapter.md) can also be returned. |

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
| [ListAdapter](ListAdapter.md)! | The [android.widget.ListAdapter](ListAdapter.md) wrapped by this adapter. |

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
| `observer` | [DataSetObserver](../android.database/DataSetObserver.md)!:the object that gets notified when the data set changes. |

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
| `observer` | [DataSetObserver](../android.database/DataSetObserver.md)!:the object to unregister. |
