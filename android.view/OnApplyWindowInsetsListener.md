# View.OnApplyWindowInsetsListener

Added in [API level 20](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnApplyWindowInsetsListener

Kotlin| [Java](https://developer.android.com/reference/android/view/View.OnApplyWindowInsetsListener "View this page in Java") 

```
interface OnApplyWindowInsetsListener
```

| [android.view.View.OnApplyWindowInsetsListener](https://developer.android.com/reference/kotlin/android/view/View.OnApplyWindowInsetsListener#) |

Listener for applying window insets on a view in a custom way.

Apps may choose to implement this interface if they want to apply custom policy to the way that window insets are treated for a view. If an OnApplyWindowInsetsListener is set, its [onApplyWindowInsets](https://developer.android.com/reference/kotlin/android/view/View.OnApplyWindowInsetsListener#onApplyWindowInsets(android.view.View,%20android.view.WindowInsets))method will be called instead of the View's own [onApplyWindowInsets](https://developer.android.com/reference/kotlin/android/view/View#onApplyWindowInsets(android.view.WindowInsets))method. The listener may optionally call the parameter View's`onApplyWindowInsets`method to apply the View's normal behavior as part of its own.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [WindowInsets](https://developer.android.com/reference/kotlin/android/view/WindowInsets) | [onApplyWindowInsets](https://developer.android.com/reference/kotlin/android/view/View.OnApplyWindowInsetsListener#onApplyWindowInsets(android.view.View,%20android.view.WindowInsets))`(`v:` ` [View](https://developer.android.com/reference/kotlin/android/view/View)`, `insets:` ` [WindowInsets](https://developer.android.com/reference/kotlin/android/view/WindowInsets)`)` When [set](https://developer.android.com/reference/kotlin/android/view/View#setOnApplyWindowInsetsListener(android.view.View.OnApplyWindowInsetsListener))on a View, this listener method will be called instead of the view's own [onApplyWindowInsets](https://developer.android.com/reference/kotlin/android/view/View#onApplyWindowInsets(android.view.WindowInsets))method. |

## Public methods

### onApplyWindowInsets

Added in [API level 20](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onApplyWindowInsets(
    v: View, 
    insets: WindowInsets
): WindowInsets
```

When [set](https://developer.android.com/reference/kotlin/android/view/View#setOnApplyWindowInsetsListener(android.view.View.OnApplyWindowInsetsListener))on a View, this listener method will be called instead of the view's own [onApplyWindowInsets](https://developer.android.com/reference/kotlin/android/view/View#onApplyWindowInsets(android.view.WindowInsets))method.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------|
| `v` | [View](https://developer.android.com/reference/kotlin/android/view/View):The view applying window insets This value cannot be`null`. |
| `insets` | [WindowInsets](https://developer.android.com/reference/kotlin/android/view/WindowInsets):The insets to apply This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [WindowInsets](https://developer.android.com/reference/kotlin/android/view/WindowInsets) | The insets supplied, minus any insets that were consumed This value cannot be`null`. |
