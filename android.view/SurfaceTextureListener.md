# TextureView.SurfaceTextureListener

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SurfaceTextureListener

Kotlin | [Java](https://developer.android.com/reference/android/view/TextureView.SurfaceTextureListener "View this page in Java") 
| --- | --- |

```
interface SurfaceTextureListener
```

| [android.view.TextureView.SurfaceTextureListener](https://developer.android.com/reference/kotlin/android/view/TextureView.SurfaceTextureListener#) |

This listener can be used to be notified when the surface texture associated with this texture view is available.

## Summary

| Public methods ||
|---------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onSurfaceTextureAvailable](https://developer.android.com/reference/kotlin/android/view/TextureView.SurfaceTextureListener#onSurfaceTextureAvailable(android.graphics.SurfaceTexture,%20kotlin.Int,%20kotlin.Int))`(`surface:` ` [SurfaceTexture](https://developer.android.com/reference/kotlin/android/graphics/SurfaceTexture.html#)`, `width:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `height:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Invoked when a [TextureView](https://developer.android.com/reference/kotlin/android/view/TextureView)'s SurfaceTexture is ready for use. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onSurfaceTextureDestroyed](https://developer.android.com/reference/kotlin/android/view/TextureView.SurfaceTextureListener#onSurfaceTextureDestroyed(android.graphics.SurfaceTexture))`(`surface:` ` [SurfaceTexture](https://developer.android.com/reference/kotlin/android/graphics/SurfaceTexture.html#)`)` Invoked when the specified [SurfaceTexture](https://developer.android.com/reference/kotlin/android/graphics/SurfaceTexture.html#) is about to be destroyed. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onSurfaceTextureSizeChanged](https://developer.android.com/reference/kotlin/android/view/TextureView.SurfaceTextureListener#onSurfaceTextureSizeChanged(android.graphics.SurfaceTexture,%20kotlin.Int,%20kotlin.Int))`(`surface:` ` [SurfaceTexture](https://developer.android.com/reference/kotlin/android/graphics/SurfaceTexture.html#)`, `width:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `height:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Invoked when the [SurfaceTexture](https://developer.android.com/reference/kotlin/android/graphics/SurfaceTexture.html#)'s buffers size changed. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onSurfaceTextureUpdated](https://developer.android.com/reference/kotlin/android/view/TextureView.SurfaceTextureListener#onSurfaceTextureUpdated(android.graphics.SurfaceTexture))`(`surface:` ` [SurfaceTexture](https://developer.android.com/reference/kotlin/android/graphics/SurfaceTexture.html#)`)` Invoked when the specified [SurfaceTexture](https://developer.android.com/reference/kotlin/android/graphics/SurfaceTexture.html#) is updated through [SurfaceTexture.updateTexImage()](https://developer.android.com/reference/kotlin/android/graphics/SurfaceTexture.html#updateTexImage()). |

## Public methods

### onSurfaceTextureAvailable

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onSurfaceTextureAvailable(
    surface: SurfaceTexture, 
    width: Int, 
    height: Int
): Unit
```

Invoked when a [TextureView](https://developer.android.com/reference/kotlin/android/view/TextureView)'s SurfaceTexture is ready for use.

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `surface` | [SurfaceTexture](https://developer.android.com/reference/kotlin/android/graphics/SurfaceTexture.html#): The surface returned by [android.view.TextureView#getSurfaceTexture()](https://developer.android.com/reference/kotlin/android/view/TextureView#getSurfaceTexture()) This value cannot be `null`. |
| `width` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The width of the surface |
| `height` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The height of the surface |
| --- | --- |

### onSurfaceTextureDestroyed

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onSurfaceTextureDestroyed(surface: SurfaceTexture): Boolean
```

Invoked when the specified [SurfaceTexture](https://developer.android.com/reference/kotlin/android/graphics/SurfaceTexture.html#) is about to be destroyed. If returns true, no rendering should happen inside the surface texture after this method is invoked. If returns false, the client needs to call [SurfaceTexture.release()](https://developer.android.com/reference/kotlin/android/graphics/SurfaceTexture.html#release()). Most applications should return true.

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `surface` | [SurfaceTexture](https://developer.android.com/reference/kotlin/android/graphics/SurfaceTexture.html#): The surface about to be destroyed This value cannot be `null`. |

### onSurfaceTextureSizeChanged

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onSurfaceTextureSizeChanged(
    surface: SurfaceTexture, 
    width: Int, 
    height: Int
): Unit
```

Invoked when the [SurfaceTexture](https://developer.android.com/reference/kotlin/android/graphics/SurfaceTexture.html#)'s buffers size changed.

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `surface` | [SurfaceTexture](https://developer.android.com/reference/kotlin/android/graphics/SurfaceTexture.html#): The surface returned by [android.view.TextureView#getSurfaceTexture()](https://developer.android.com/reference/kotlin/android/view/TextureView#getSurfaceTexture()) This value cannot be `null`. |
| `width` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The new width of the surface |
| `height` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The new height of the surface |
| --- | --- |

### onSurfaceTextureUpdated

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onSurfaceTextureUpdated(surface: SurfaceTexture): Unit
```

Invoked when the specified [SurfaceTexture](https://developer.android.com/reference/kotlin/android/graphics/SurfaceTexture.html#) is updated through [SurfaceTexture.updateTexImage()](https://developer.android.com/reference/kotlin/android/graphics/SurfaceTexture.html#updateTexImage()).

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `surface` | [SurfaceTexture](https://developer.android.com/reference/kotlin/android/graphics/SurfaceTexture.html#): The surface just updated This value cannot be `null`. |
