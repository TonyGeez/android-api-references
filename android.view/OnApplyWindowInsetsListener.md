# View.OnApplyWindowInsetsListener

Added in [API level 20](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnApplyWindowInsetsListener

Kotlin| [Java](../android/view/View.OnApplyWindowInsetsListener.md) 
| --- | --- |

```
interface OnApplyWindowInsetsListener
```

| [android.view.View.OnApplyWindowInsetsListener](../android/view/View.OnApplyWindowInsetsListener.md) |

Listener for applying window insets on a view in a custom way.

Apps may choose to implement this interface if they want to apply custom policy to the way that window insets are treated for a view. If an OnApplyWindowInsetsListener is set, its [onApplyWindowInsets](../android/view/View.OnApplyWindowInsetsListener.md))method will be called instead of the View's own [onApplyWindowInsets](../android/view/View.md))method. The listener may optionally call the parameter View's`onApplyWindowInsets`method to apply the View's normal behavior as part of its own.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [WindowInsets](../android/view/WindowInsets.md) | [onApplyWindowInsets](../android/view/View.OnApplyWindowInsetsListener.md))`(`v:` ` [View](../android/view/View.md)`, `insets:` ` [WindowInsets](../android/view/WindowInsets.md)`)` When [set](../android/view/View.md))on a View, this listener method will be called instead of the view's own [onApplyWindowInsets](../android/view/View.md))method. |

## Public methods

### onApplyWindowInsets

Added in [API level 20](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onApplyWindowInsets(
    v: View, 
    insets: WindowInsets
): WindowInsets
```

When [set](../android/view/View.md))on a View, this listener method will be called instead of the view's own [onApplyWindowInsets](../android/view/View.md))method.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------|
| `v` | [View](../android/view/View.md):The view applying window insets This value cannot be`null`. |
| `insets` | [WindowInsets](../android/view/WindowInsets.md):The insets to apply This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [WindowInsets](../android/view/WindowInsets.md) | The insets supplied, minus any insets that were consumed This value cannot be`null`. |
