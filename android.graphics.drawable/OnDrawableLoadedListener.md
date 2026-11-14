# Icon.OnDrawableLoadedListener

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnDrawableLoadedListener

Kotlin| [Java](../android/graphics/drawable/Icon.OnDrawableLoadedListener.md) 
| --- | --- |

```
interface OnDrawableLoadedListener
```

| [android.graphics.drawable.Icon.OnDrawableLoadedListener](../android/graphics/drawable/Icon.OnDrawableLoadedListener.md) |

Implement this interface to receive a callback when [loadDrawableAsync](Icon.md))is finished and your Drawable is ready.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onDrawableLoaded](../android/graphics/drawable/Icon.OnDrawableLoadedListener.md))`(`d:` ` [Drawable](Drawable.md)!`)` <br /> |

## Public methods

### onDrawableLoaded

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onDrawableLoaded(d: Drawable!): Unit
```
