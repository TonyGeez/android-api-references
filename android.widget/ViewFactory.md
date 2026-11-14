# ViewSwitcher.ViewFactory

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ViewFactory

Kotlin | [Java](../android/widget/ViewSwitcher.ViewFactory.md) 
| --- | --- |

```
interface ViewFactory
```

| [android.widget.ViewSwitcher.ViewFactory](../android/widget/ViewSwitcher.ViewFactory.md) |

Creates views in a ViewSwitcher.

## Summary

| Public methods ||
|------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [View](../android/view/View.md)! | [makeView](../android/widget/ViewSwitcher.ViewFactory.md))`()` Creates a new [android.view.View](../android/view/View.md) to be added in a [android.widget.ViewSwitcher](../android/widget/ViewSwitcher.md). |

## Public methods

### makeView

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun makeView(): View!
```

Creates a new [android.view.View](../android/view/View.md) to be added in a [android.widget.ViewSwitcher](../android/widget/ViewSwitcher.md).

| Return ||
|---------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [View](../android/view/View.md)! | a [android.view.View](../android/view/View.md) |
