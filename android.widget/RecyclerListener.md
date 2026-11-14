# AbsListView.RecyclerListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RecyclerListener

Kotlin| [Java](https://developer.android.com/reference/android/widget/AbsListView.RecyclerListener "View this page in Java") 
| --- | --- |

```
interface RecyclerListener
```

| [android.widget.AbsListView.RecyclerListener](https://developer.android.com/reference/kotlin/android/widget/AbsListView.RecyclerListener#) |

A RecyclerListener is used to receive a notification whenever a View is placed inside the RecycleBin's scrap heap. This listener is used to free resources associated to Views placed in the RecycleBin.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onMovedToScrapHeap](https://developer.android.com/reference/kotlin/android/widget/AbsListView.RecyclerListener#onMovedToScrapHeap(android.view.View))`(`view:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!`)` Indicates that the specified View was moved into the recycler's scrap heap. |

## Public methods

### onMovedToScrapHeap

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onMovedToScrapHeap(view: View!): Unit
```

Indicates that the specified View was moved into the recycler's scrap heap. The view is not displayed on screen any more and any expensive resource associated with the view should be discarded.

| Parameters ||
|--------|----------------------------------------------------------------------------------|
| `view` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!: |
