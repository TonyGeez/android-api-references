# ViewTreeObserver.OnGlobalLayoutListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnGlobalLayoutListener

Kotlin| [Java](../android/view/ViewTreeObserver.OnGlobalLayoutListener.md) 
| --- | --- |

```
interface OnGlobalLayoutListener
```

| [android.view.ViewTreeObserver.OnGlobalLayoutListener](../android/view/ViewTreeObserver.OnGlobalLayoutListener.md) |

| Known Direct Subclasses [AbsListView](../android.widget/AbsListView.md), [NativeActivity](../android.app/NativeActivity.md) |---------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------| | [AbsListView](../android.widget/AbsListView.md) | Base class that can be used to implement virtualized lists of items. | | [NativeActivity](../android.app/NativeActivity.md) | Convenience for implementing an activity that will be implemented purely in native code. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [ExpandableListView](../android.widget/ExpandableListView.md), [GridView](../android.widget/GridView.md), [ListView](../android.widget/ListView.md) |--------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------| | [ExpandableListView](../android.widget/ExpandableListView.md) | A view that shows items in a vertically scrolling two-level list. | | [GridView](../android.widget/GridView.md) | A view that shows items in two-dimensional scrolling grid. | | [ListView](../android.widget/ListView.md) | Displays a vertically-scrollable collection of views, where each view is positioned immediately below the previous view in the list. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Interface definition for a callback to be invoked when the global layout state or the visibility of views within the view tree changes.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onGlobalLayout](../android/view/ViewTreeObserver.OnGlobalLayoutListener.md))`()` Callback method to be invoked when the global layout state or the visibility of views within the view tree changes |

## Public methods

### onGlobalLayout

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onGlobalLayout(): Unit
```

Callback method to be invoked when the global layout state or the visibility of views within the view tree changes
