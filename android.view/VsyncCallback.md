Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# VsyncCallback

Kotlin | [Java](../android/view/Choreographer.VsyncCallback.md)
| --- | --- |

```
interface VsyncCallback
```

| [android.view.Choreographer.VsyncCallback](../android/view/Choreographer.VsyncCallback.md) |

Implement this interface to receive a callback to start the next frame. The callback is invoked on the `https://developer.android.com/reference/kotlin/android/os/Looper.html#` thread to which the Choreographer is attached. The callback payload contains information about multiple possible frames, allowing choice of the appropriate frame based on latency requirements.

## Summary

| Public methods ||
|---|---|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onVsync Called when a new display frame is being rendered. |

## Public methods

### onVsync

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun onVsync(data: Choreographer.FrameData): Unit
```

Called when a new display frame is being rendered.

| Parameters ||
|---|---|
| `data` | [Choreographer.FrameData](../android/view/Choreographer.FrameData.md): The payload which includes frame information. Divide nanosecond values by `1000000` to convert it to the uptimeMillis time base. `data` is not valid outside of `onVsync` and should not be accessed outside the callback. This value cannot be `null`. |

**See Also**

- doFrame
