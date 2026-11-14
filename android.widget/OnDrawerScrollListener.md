# SlidingDrawer.OnDrawerScrollListener

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnDrawerScrollListener

Kotlin| [Java](../android/widget/SlidingDrawer.OnDrawerScrollListener.md) 
| --- | --- |

```
interface OnDrawerScrollListener
```

| [android.widget.SlidingDrawer.OnDrawerScrollListener](../android/widget/SlidingDrawer.OnDrawerScrollListener.md) |

| **This interface was deprecated in API level 29.**
|
| Deprecated in Java.

Callback invoked when the drawer is scrolled.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onScrollEnded](../android/widget/SlidingDrawer.OnDrawerScrollListener.md))`()` Invoked when the user stops dragging/flinging the drawer's handle. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onScrollStarted](../android/widget/SlidingDrawer.OnDrawerScrollListener.md))`()` Invoked when the user starts dragging/flinging the drawer's handle. |

## Public methods

### onScrollEnded

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onScrollEnded(): Unit
```

**Deprecated:** *Deprecated in Java.*

Invoked when the user stops dragging/flinging the drawer's handle. 

### onScrollStarted

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onScrollStarted(): Unit
```

**Deprecated:** *Deprecated in Java.*

Invoked when the user starts dragging/flinging the drawer's handle.
