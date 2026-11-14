# InlineContentView.SurfaceControlCallback

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SurfaceControlCallback

Kotlin| [Java](../android/widget/inline/InlineContentView.SurfaceControlCallback.md) 
| --- | --- |

```
interface SurfaceControlCallback
```

| [android.widget.inline.InlineContentView.SurfaceControlCallback](../android/widget/inline/InlineContentView.SurfaceControlCallback.md) |

Callback for observing the lifecycle of the surface control that manipulates the backing secure embedded UI surface.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onCreated](../android/widget/inline/InlineContentView.SurfaceControlCallback.md))`(`surfaceControl:` ` [SurfaceControl](../android/view/SurfaceControl.md)`)` Called when the backing surface is being created. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onDestroyed](../android/widget/inline/InlineContentView.SurfaceControlCallback.md))`(`surfaceControl:` ` [SurfaceControl](../android/view/SurfaceControl.md)`)` Called when the backing surface is being destroyed. |

## Public methods

### onCreated

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onCreated(surfaceControl: SurfaceControl): Unit
```

Called when the backing surface is being created.

| Parameters ||
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `surfaceControl` | [SurfaceControl](../android/view/SurfaceControl.md):The surface control to manipulate the surface. This value cannot be`null`. |

### onDestroyed

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onDestroyed(surfaceControl: SurfaceControl): Unit
```

Called when the backing surface is being destroyed.

| Parameters ||
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `surfaceControl` | [SurfaceControl](../android/view/SurfaceControl.md):The surface control to manipulate the surface. This value cannot be`null`. |
