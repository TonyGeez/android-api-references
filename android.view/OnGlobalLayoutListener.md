# ViewTreeObserver.OnGlobalLayoutListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnGlobalLayoutListener

Kotlin| [Java](https://developer.android.com/reference/android/view/ViewTreeObserver.OnGlobalLayoutListener "View this page in Java") 
| --- | --- |

```
interface OnGlobalLayoutListener
```

| [android.view.ViewTreeObserver.OnGlobalLayoutListener](https://developer.android.com/reference/kotlin/android/view/ViewTreeObserver.OnGlobalLayoutListener#) |

| Known Direct Subclasses [AbsListView](https://developer.android.com/reference/kotlin/android/widget/AbsListView.html#), [NativeActivity](https://developer.android.com/reference/kotlin/android/app/NativeActivity.html#) |---------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------| | [AbsListView](https://developer.android.com/reference/kotlin/android/widget/AbsListView.html#) | Base class that can be used to implement virtualized lists of items. | | [NativeActivity](https://developer.android.com/reference/kotlin/android/app/NativeActivity.html#) | Convenience for implementing an activity that will be implemented purely in native code. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [ExpandableListView](https://developer.android.com/reference/kotlin/android/widget/ExpandableListView.html#), [GridView](https://developer.android.com/reference/kotlin/android/widget/GridView.html#), [ListView](https://developer.android.com/reference/kotlin/android/widget/ListView.html#) |--------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------| | [ExpandableListView](https://developer.android.com/reference/kotlin/android/widget/ExpandableListView.html#) | A view that shows items in a vertically scrolling two-level list. | | [GridView](https://developer.android.com/reference/kotlin/android/widget/GridView.html#) | A view that shows items in two-dimensional scrolling grid. | | [ListView](https://developer.android.com/reference/kotlin/android/widget/ListView.html#) | Displays a vertically-scrollable collection of views, where each view is positioned immediately below the previous view in the list. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Interface definition for a callback to be invoked when the global layout state or the visibility of views within the view tree changes.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onGlobalLayout](https://developer.android.com/reference/kotlin/android/view/ViewTreeObserver.OnGlobalLayoutListener#onGlobalLayout())`()` Callback method to be invoked when the global layout state or the visibility of views within the view tree changes |

## Public methods

### onGlobalLayout

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onGlobalLayout(): Unit
```

Callback method to be invoked when the global layout state or the visibility of views within the view tree changes
