# ViewTreeObserver.OnTouchModeChangeListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnTouchModeChangeListener

Kotlin| [Java](../android/view/ViewTreeObserver.OnTouchModeChangeListener.md) 
| --- | --- |

```
interface OnTouchModeChangeListener
```

| [android.view.ViewTreeObserver.OnTouchModeChangeListener](../android/view/ViewTreeObserver.OnTouchModeChangeListener.md) |

| Known Direct Subclasses [AbsListView](../android/widget/AbsListView.md), [TabHost](../android/widget/TabHost.md) |------------------------------------------------------------------------------------------------|----------------------------------------------------------------------| | [AbsListView](../android/widget/AbsListView.md) | Base class that can be used to implement virtualized lists of items. | | [TabHost](../android/widget/TabHost.md) | Container for a tabbed window view. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [ExpandableListView](../android/widget/ExpandableListView.md), [GridView](../android/widget/GridView.md), [ListView](../android/widget/ListView.md) |--------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------| | [ExpandableListView](../android/widget/ExpandableListView.md) | A view that shows items in a vertically scrolling two-level list. | | [GridView](../android/widget/GridView.md) | A view that shows items in two-dimensional scrolling grid. | | [ListView](../android/widget/ListView.md) | Displays a vertically-scrollable collection of views, where each view is positioned immediately below the previous view in the list. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Interface definition for a callback to be invoked when the touch mode changes.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onTouchModeChanged](../android/view/ViewTreeObserver.OnTouchModeChangeListener.md))`(`isInTouchMode:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Callback method to be invoked when the touch mode changes. |

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
