# ViewTreeObserver.OnTouchModeChangeListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnTouchModeChangeListener

Kotlin| [Java](https://developer.android.com/reference/android/view/ViewTreeObserver.OnTouchModeChangeListener "View this page in Java") 

```
interface OnTouchModeChangeListener
```

| [android.view.ViewTreeObserver.OnTouchModeChangeListener](https://developer.android.com/reference/kotlin/android/view/ViewTreeObserver.OnTouchModeChangeListener#) |

| Known Direct Subclasses [AbsListView](https://developer.android.com/reference/kotlin/android/widget/AbsListView.html#), [TabHost](https://developer.android.com/reference/kotlin/android/widget/TabHost.html#) |------------------------------------------------------------------------------------------------|----------------------------------------------------------------------| | [AbsListView](https://developer.android.com/reference/kotlin/android/widget/AbsListView.html#) | Base class that can be used to implement virtualized lists of items. | | [TabHost](https://developer.android.com/reference/kotlin/android/widget/TabHost.html#) | Container for a tabbed window view. | |

| Known Indirect Subclasses [ExpandableListView](https://developer.android.com/reference/kotlin/android/widget/ExpandableListView.html#), [GridView](https://developer.android.com/reference/kotlin/android/widget/GridView.html#), [ListView](https://developer.android.com/reference/kotlin/android/widget/ListView.html#) |--------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------| | [ExpandableListView](https://developer.android.com/reference/kotlin/android/widget/ExpandableListView.html#) | A view that shows items in a vertically scrolling two-level list. | | [GridView](https://developer.android.com/reference/kotlin/android/widget/GridView.html#) | A view that shows items in two-dimensional scrolling grid. | | [ListView](https://developer.android.com/reference/kotlin/android/widget/ListView.html#) | Displays a vertically-scrollable collection of views, where each view is positioned immediately below the previous view in the list. | |

Interface definition for a callback to be invoked when the touch mode changes.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onTouchModeChanged](https://developer.android.com/reference/kotlin/android/view/ViewTreeObserver.OnTouchModeChangeListener#onTouchModeChanged(kotlin.Boolean))`(`isInTouchMode:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Callback method to be invoked when the touch mode changes. |

## Public methods

### onTouchModeChanged

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onTouchModeChanged(isInTouchMode: Boolean): Unit
```

Callback method to be invoked when the touch mode changes.

| Parameters ||
|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `isInTouchMode` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):True if the view hierarchy is now in touch mode, false otherwise. |
