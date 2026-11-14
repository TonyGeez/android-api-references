# ViewSwitcher.ViewFactory

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ViewFactory

Kotlin | [Java](https://developer.android.com/reference/android/widget/ViewSwitcher.ViewFactory "View this page in Java") 

```
interface ViewFactory
```

| [android.widget.ViewSwitcher.ViewFactory](https://developer.android.com/reference/kotlin/android/widget/ViewSwitcher.ViewFactory#) |

Creates views in a ViewSwitcher.

## Summary

| Public methods ||
|------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [View](https://developer.android.com/reference/kotlin/android/view/View.html#)! | [makeView](https://developer.android.com/reference/kotlin/android/widget/ViewSwitcher.ViewFactory#makeView())`()` Creates a new [android.view.View](https://developer.android.com/reference/kotlin/android/view/View.html#) to be added in a [android.widget.ViewSwitcher](https://developer.android.com/reference/kotlin/android/widget/ViewSwitcher). |

## Public methods

### makeView

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun makeView(): View!
```

Creates a new [android.view.View](https://developer.android.com/reference/kotlin/android/view/View.html#) to be added in a [android.widget.ViewSwitcher](https://developer.android.com/reference/kotlin/android/widget/ViewSwitcher).

| Return ||
|---------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [View](https://developer.android.com/reference/kotlin/android/view/View.html#)! | a [android.view.View](https://developer.android.com/reference/kotlin/android/view/View.html#) |
