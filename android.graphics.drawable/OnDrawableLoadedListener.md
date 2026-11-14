# Icon.OnDrawableLoadedListener

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnDrawableLoadedListener

Kotlin| [Java](https://developer.android.com/reference/android/graphics/drawable/Icon.OnDrawableLoadedListener "View this page in Java") 

```
interface OnDrawableLoadedListener
```

| [android.graphics.drawable.Icon.OnDrawableLoadedListener](https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon.OnDrawableLoadedListener#) |

Implement this interface to receive a callback when [loadDrawableAsync](https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon#loadDrawableAsync(android.content.Context,%20android.graphics.drawable.Icon.OnDrawableLoadedListener,%20android.os.Handler))is finished and your Drawable is ready.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onDrawableLoaded](https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon.OnDrawableLoadedListener#onDrawableLoaded(android.graphics.drawable.Drawable))`(`d:` ` [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable)!`)` <br /> |

## Public methods

### onDrawableLoaded

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onDrawableLoaded(d: Drawable!): Unit
```
