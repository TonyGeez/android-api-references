# RemoteViewsService.RemoteViewsFactory

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RemoteViewsFactory

Kotlin| [Java](https://developer.android.com/reference/android/widget/RemoteViewsService.RemoteViewsFactory "View this page in Java") 
| --- | --- |

```
interface RemoteViewsFactory
```

| [android.widget.RemoteViewsService.RemoteViewsFactory](https://developer.android.com/reference/kotlin/android/widget/RemoteViewsService.RemoteViewsFactory#) |

An interface for an adapter between a remote collection view (ListView, GridView, etc) and the underlying data for that view. The implementor is responsible for making a RemoteView for each item in the data set. This interface is a thin wrapper around [Adapter](https://developer.android.com/reference/kotlin/android/widget/Adapter).

## Summary

| Public methods ||
|---------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getCount](https://developer.android.com/reference/kotlin/android/widget/RemoteViewsService.RemoteViewsFactory#getCount())`()` See [Adapter.getCount()](https://developer.android.com/reference/kotlin/android/widget/Adapter#getCount()) |
| abstract [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getItemId](https://developer.android.com/reference/kotlin/android/widget/RemoteViewsService.RemoteViewsFactory#getItemId(kotlin.Int))`(`position:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` See [Adapter.getItemId(int)](https://developer.android.com/reference/kotlin/android/widget/Adapter#getItemId(kotlin.Int)). |
| abstract [RemoteViews](https://developer.android.com/reference/kotlin/android/widget/RemoteViews)! | [getLoadingView](https://developer.android.com/reference/kotlin/android/widget/RemoteViewsService.RemoteViewsFactory#getLoadingView())`()` This allows for the use of a custom loading view which appears between the time that [getViewAt(int)](https://developer.android.com/reference/kotlin/android/widget/RemoteViewsService.RemoteViewsFactory#getViewAt(kotlin.Int))is called and returns. |
| --- | --- |
| abstract [RemoteViews](https://developer.android.com/reference/kotlin/android/widget/RemoteViews)! | [getViewAt](https://developer.android.com/reference/kotlin/android/widget/RemoteViewsService.RemoteViewsFactory#getViewAt(kotlin.Int))`(`position:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` See [Adapter.getView(int, android.view.View, android.view.ViewGroup)](https://developer.android.com/reference/kotlin/android/widget/Adapter#getView(kotlin.Int,%20android.view.View,%20android.view.ViewGroup)). |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getViewTypeCount](https://developer.android.com/reference/kotlin/android/widget/RemoteViewsService.RemoteViewsFactory#getViewTypeCount())`()` See [Adapter.getViewTypeCount()](https://developer.android.com/reference/kotlin/android/widget/Adapter#getViewTypeCount()). |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasStableIds](https://developer.android.com/reference/kotlin/android/widget/RemoteViewsService.RemoteViewsFactory#hasStableIds())`()` See [Adapter.hasStableIds()](https://developer.android.com/reference/kotlin/android/widget/Adapter#hasStableIds()). |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onCreate](https://developer.android.com/reference/kotlin/android/widget/RemoteViewsService.RemoteViewsFactory#onCreate())`()` Called when your factory is first constructed. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onDataSetChanged](https://developer.android.com/reference/kotlin/android/widget/RemoteViewsService.RemoteViewsFactory#onDataSetChanged())`()` Called when notifyDataSetChanged() is triggered on the remote adapter. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onDestroy](https://developer.android.com/reference/kotlin/android/widget/RemoteViewsService.RemoteViewsFactory#onDestroy())`()` Called when the last RemoteViewsAdapter that is associated with this factory is unbound. |
| --- | --- |

## Public methods

### getCount

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getCount(): Int
```

See [Adapter.getCount()](https://developer.android.com/reference/kotlin/android/widget/Adapter#getCount())

| Return ||
|----------------------------------------------------------------------------|-----------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Count of items. |

### getItemId

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getItemId(position: Int): Long
```

See [Adapter.getItemId(int)](https://developer.android.com/reference/kotlin/android/widget/Adapter#getItemId(kotlin.Int)).

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| `position` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The position of the item within the data set whose row id we want. |

| Return ||
|------------------------------------------------------------------------------|-----------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | The id of the item at the specified position. |

### getLoadingView

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getLoadingView(): RemoteViews!
```

This allows for the use of a custom loading view which appears between the time that [getViewAt(int)](https://developer.android.com/reference/kotlin/android/widget/RemoteViewsService.RemoteViewsFactory#getViewAt(kotlin.Int))is called and returns. If null is returned, a default loading view will be used.

| Return ||
|-------------------------------------------------------------------------------------------|--------------------------------------------------------|
| [RemoteViews](https://developer.android.com/reference/kotlin/android/widget/RemoteViews)! | The RemoteViews representing the desired loading view. |

### getViewAt

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getViewAt(position: Int): RemoteViews!
```

See [Adapter.getView(int, android.view.View, android.view.ViewGroup)](https://developer.android.com/reference/kotlin/android/widget/Adapter#getView(kotlin.Int,%20android.view.View,%20android.view.ViewGroup)). Note: expensive tasks can be safely performed synchronously within this method, and a loading view will be displayed in the interim. See [getLoadingView()](https://developer.android.com/reference/kotlin/android/widget/RemoteViewsService.RemoteViewsFactory#getLoadingView()).

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `position` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The position of the item within the Factory's data set of the item whose view we want. |

| Return ||
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [RemoteViews](https://developer.android.com/reference/kotlin/android/widget/RemoteViews)! | A RemoteViews object corresponding to the data at the specified position. |

### getViewTypeCount

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getViewTypeCount(): Int
```

See [Adapter.getViewTypeCount()](https://developer.android.com/reference/kotlin/android/widget/Adapter#getViewTypeCount()).

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The number of types of Views that will be returned by this factory. |

### hasStableIds

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun hasStableIds(): Boolean
```

See [Adapter.hasStableIds()](https://developer.android.com/reference/kotlin/android/widget/Adapter#hasStableIds()).

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if the same id always refers to the same object. |

### onCreate

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onCreate(): Unit
```

Called when your factory is first constructed. The same factory may be shared across multiple RemoteViewAdapters depending on the intent passed. 

### onDataSetChanged

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onDataSetChanged(): Unit
```

Called when notifyDataSetChanged() is triggered on the remote adapter. This allows a RemoteViewsFactory to respond to data changes by updating any internal references. Note: expensive tasks can be safely performed synchronously within this method. In the interim, the old data will be displayed within the widget. 
**See Also**

- [android.appwidget.AppWidgetManager#notifyAppWidgetViewDataChanged(int[], int)](https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager.html#notifyAppWidgetViewDataChanged(kotlin.IntArray,%20kotlin.Int)) 

### onDestroy

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onDestroy(): Unit
```

Called when the last RemoteViewsAdapter that is associated with this factory is unbound.
