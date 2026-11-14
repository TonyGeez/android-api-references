# InlineContentView.SurfaceControlCallback

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SurfaceControlCallback

Kotlin| [Java](https://developer.android.com/reference/android/widget/inline/InlineContentView.SurfaceControlCallback "View this page in Java") 
| --- | --- |

```
interface SurfaceControlCallback
```

| [android.widget.inline.InlineContentView.SurfaceControlCallback](https://developer.android.com/reference/kotlin/android/widget/inline/InlineContentView.SurfaceControlCallback#) |

Callback for observing the lifecycle of the surface control that manipulates the backing secure embedded UI surface.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onCreated](https://developer.android.com/reference/kotlin/android/widget/inline/InlineContentView.SurfaceControlCallback#onCreated(android.view.SurfaceControl))`(`surfaceControl:` ` [SurfaceControl](https://developer.android.com/reference/kotlin/android/view/SurfaceControl.html#)`)` Called when the backing surface is being created. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onDestroyed](https://developer.android.com/reference/kotlin/android/widget/inline/InlineContentView.SurfaceControlCallback#onDestroyed(android.view.SurfaceControl))`(`surfaceControl:` ` [SurfaceControl](https://developer.android.com/reference/kotlin/android/view/SurfaceControl.html#)`)` Called when the backing surface is being destroyed. |

## Public methods

### onCreated

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onCreated(surfaceControl: SurfaceControl): Unit
```

Called when the backing surface is being created.

| Parameters ||
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `surfaceControl` | [SurfaceControl](https://developer.android.com/reference/kotlin/android/view/SurfaceControl.html#):The surface control to manipulate the surface. This value cannot be`null`. |

### onDestroyed

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onDestroyed(surfaceControl: SurfaceControl): Unit
```

Called when the backing surface is being destroyed.

| Parameters ||
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `surfaceControl` | [SurfaceControl](https://developer.android.com/reference/kotlin/android/view/SurfaceControl.html#):The surface control to manipulate the surface. This value cannot be`null`. |
