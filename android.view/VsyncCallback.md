Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# VsyncCallback

Kotlin | [Java](https://developer.android.com/reference/android/view/Choreographer.VsyncCallback "View this page in Java")

```
interface VsyncCallback
```

| [android.view.Choreographer.VsyncCallback](https://developer.android.com/reference/kotlin/android/view/Choreographer.VsyncCallback#) |

Implement this interface to receive a callback to start the next frame. The callback is invoked on the `https://developer.android.com/reference/kotlin/android/os/Looper.html#` thread to which the `https://developer.android.com/reference/kotlin/android/view/Choreographer` is attached. The callback payload contains information about multiple possible frames, allowing choice of the appropriate frame based on latency requirements.

## Summary

| Public methods ||
|---|---|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/Choreographer.VsyncCallback#onVsync(android.view.Choreographer.FrameData)(data: https://developer.android.com/reference/kotlin/android/view/Choreographer.FrameData)` Called when a new display frame is being rendered. |

## Public methods

### onVsync

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun onVsync(data: Choreographer.FrameData): Unit
```

Called when a new display frame is being rendered.

| Parameters ||
|---|---|
| `data` | [Choreographer.FrameData](https://developer.android.com/reference/kotlin/android/view/Choreographer.FrameData): The payload which includes frame information. Divide nanosecond values by `1000000` to convert it to the `https://developer.android.com/reference/kotlin/android/os/SystemClock.html#uptimeMillis()` time base. `data` is not valid outside of `onVsync` and should not be accessed outside the callback. This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/Choreographer.FrameCallback#doFrame(kotlin.Long)`
