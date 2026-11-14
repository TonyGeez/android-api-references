# AbsListView.OnScrollListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnScrollListener

Kotlin| [Java](../android/widget/AbsListView.OnScrollListener.md) 
| --- | --- |

```
interface OnScrollListener
```

| [android.widget.AbsListView.OnScrollListener](../android/widget/AbsListView.OnScrollListener.md) |

Interface definition for a callback to be invoked when the list or grid has been scrolled.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SCROLL_STATE_FLING](../android/widget/AbsListView.OnScrollListener.md) The user had previously been scrolling using touch and had performed a fling. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SCROLL_STATE_IDLE](../android/widget/AbsListView.OnScrollListener.md) The view is not scrolling. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SCROLL_STATE_TOUCH_SCROLL](../android/widget/AbsListView.OnScrollListener.md) The user is scrolling using touch, and their finger is still on the screen |
| --- | --- |

| Public methods ||
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onScroll](../android/widget/AbsListView.OnScrollListener.md))`(`view:` ` [AbsListView](AbsListView.md)!`, `firstVisibleItem:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `visibleItemCount:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `totalItemCount:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Callback method to be invoked when the list or grid has been scrolled. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onScrollStateChanged](../android/widget/AbsListView.OnScrollListener.md))`(`view:` ` [AbsListView](AbsListView.md)!`, `scrollState:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Callback method to be invoked while the list view or grid view is being scrolled. |

## Constants

### SCROLL_STATE_FLING

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SCROLL_STATE_FLING: Int
```

The user had previously been scrolling using touch and had performed a fling. The animation is now coasting to a stop 

 Value: 2

### SCROLL_STATE_IDLE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SCROLL_STATE_IDLE: Int
```

The view is not scrolling. Note navigating the list using the trackball counts as being in the idle state since these transitions are not animated. 

 Value: 0

### SCROLL_STATE_TOUCH_SCROLL

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SCROLL_STATE_TOUCH_SCROLL: Int
```

The user is scrolling using touch, and their finger is still on the screen 

 Value: 1

## Public methods

### onScroll

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onScroll(
    view: AbsListView!, 
    firstVisibleItem: Int, 
    visibleItemCount: Int, 
    totalItemCount: Int
): Unit
```

Callback method to be invoked when the list or grid has been scrolled. This will be called after the scroll has completed

| Parameters ||
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| `view` | [AbsListView](AbsListView.md)!:The view whose scroll state is being reported |
| `firstVisibleItem` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index of the first visible cell (ignore if visibleItemCount == 0) |
| `visibleItemCount` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of visible cells |
| --- | --- |
| `totalItemCount` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of items in the list adapter |

### onScrollStateChanged

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onScrollStateChanged(
    view: AbsListView!, 
    scrollState: Int
): Unit
```

Callback method to be invoked while the list view or grid view is being scrolled. If the view is being scrolled, this method will be called before the next frame of the scroll is rendered. In particular, it will be called before any calls to [Adapter.getView(int, View, ViewGroup)](Adapter.md)).

| Parameters ||
|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `view` | [AbsListView](AbsListView.md)!:The view whose scroll state is being reported |
| `scrollState` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The current scroll state. One of [SCROLL_STATE_TOUCH_SCROLL](../android/widget/AbsListView.OnScrollListener.md) or [SCROLL_STATE_IDLE](../android/widget/AbsListView.OnScrollListener.md). |
