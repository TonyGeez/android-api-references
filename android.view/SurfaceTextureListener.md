# TextureView.SurfaceTextureListener

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SurfaceTextureListener

Kotlin | [Java](../android/view/TextureView.SurfaceTextureListener.md) 
| --- | --- |

```
interface SurfaceTextureListener
```

| [android.view.TextureView.SurfaceTextureListener](../android/view/TextureView.SurfaceTextureListener.md) |

This listener can be used to be notified when the surface texture associated with this texture view is available.

## Summary

| Public methods ||
|---------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onSurfaceTextureAvailable](../android/view/TextureView.SurfaceTextureListener.md))`(`surface:` ` [SurfaceTexture](../android.graphics/SurfaceTexture.md)`, `width:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `height:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Invoked when a [TextureView](TextureView.md)'s SurfaceTexture is ready for use. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onSurfaceTextureDestroyed](../android/view/TextureView.SurfaceTextureListener.md))`(`surface:` ` [SurfaceTexture](../android.graphics/SurfaceTexture.md)`)` Invoked when the specified [SurfaceTexture](../android.graphics/SurfaceTexture.md) is about to be destroyed. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onSurfaceTextureSizeChanged](../android/view/TextureView.SurfaceTextureListener.md))`(`surface:` ` [SurfaceTexture](../android.graphics/SurfaceTexture.md)`, `width:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `height:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Invoked when the [SurfaceTexture](../android.graphics/SurfaceTexture.md)'s buffers size changed. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onSurfaceTextureUpdated](../android/view/TextureView.SurfaceTextureListener.md))`(`surface:` ` [SurfaceTexture](../android.graphics/SurfaceTexture.md)`)` Invoked when the specified [SurfaceTexture](../android.graphics/SurfaceTexture.md) is updated through [SurfaceTexture.updateTexImage()](../android.graphics/SurfaceTexture.md)). |

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

Invoked when a [TextureView](TextureView.md)'s SurfaceTexture is ready for use.

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `surface` | [SurfaceTexture](../android.graphics/SurfaceTexture.md): The surface returned by [android.view.TextureView#getSurfaceTexture()](TextureView.md)) This value cannot be `null`. |
| `width` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The width of the surface |
| `height` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The height of the surface |
| --- | --- |

### onSurfaceTextureDestroyed

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onSurfaceTextureDestroyed(surface: SurfaceTexture): Boolean
```

Invoked when the specified [SurfaceTexture](../android.graphics/SurfaceTexture.md) is about to be destroyed. If returns true, no rendering should happen inside the surface texture after this method is invoked. If returns false, the client needs to call [SurfaceTexture.release()](../android.graphics/SurfaceTexture.md)). Most applications should return true.

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `surface` | [SurfaceTexture](../android.graphics/SurfaceTexture.md): The surface about to be destroyed This value cannot be `null`. |

### onSurfaceTextureSizeChanged

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onSurfaceTextureSizeChanged(
    surface: SurfaceTexture, 
    width: Int, 
    height: Int
): Unit
```

Invoked when the [SurfaceTexture](../android.graphics/SurfaceTexture.md)'s buffers size changed.

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `surface` | [SurfaceTexture](../android.graphics/SurfaceTexture.md): The surface returned by [android.view.TextureView#getSurfaceTexture()](TextureView.md)) This value cannot be `null`. |
| `width` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The new width of the surface |
| `height` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The new height of the surface |
| --- | --- |

### onSurfaceTextureUpdated

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onSurfaceTextureUpdated(surface: SurfaceTexture): Unit
```

Invoked when the specified [SurfaceTexture](../android.graphics/SurfaceTexture.md) is updated through [SurfaceTexture.updateTexImage()](../android.graphics/SurfaceTexture.md)).

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `surface` | [SurfaceTexture](../android.graphics/SurfaceTexture.md): The surface just updated This value cannot be `null`. |
