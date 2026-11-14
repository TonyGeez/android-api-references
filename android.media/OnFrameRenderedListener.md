# MediaCodec.OnFrameRenderedListener

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnFrameRenderedListener

Kotlin| [Java](../android/media/MediaCodec.OnFrameRenderedListener.md) 
| --- | --- |

```
interface OnFrameRenderedListener
```

| [android.media.MediaCodec.OnFrameRenderedListener](../android/media/MediaCodec.OnFrameRenderedListener.md) |

Listener to be called when an output frame has rendered on the output surface

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onFrameRendered](../android/media/MediaCodec.OnFrameRenderedListener.md))`(`codec:` ` [MediaCodec](MediaCodec.md)`, `presentationTimeUs:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `nanoTime:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Called when an output frame has rendered on the output surface. |

## Public methods

### onFrameRendered

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onFrameRendered(
    codec: MediaCodec, 
    presentationTimeUs: Long, 
    nanoTime: Long
): Unit
```

Called when an output frame has rendered on the output surface.

**Note:** This callback is for informational purposes only: to get precise render timing samples, and can be significantly delayed and batched. Starting with Android [android.os.Build.VERSION_CODES#UPSIDE_DOWN_CAKE](../android/os/Build.VERSION_CODES.md), a callback will always be received for each rendered frame providing the MediaCodec is still in the executing state when the callback is dispatched. Prior to Android [android.os.Build.VERSION_CODES#UPSIDE_DOWN_CAKE](../android/os/Build.VERSION_CODES.md), some frames may have been rendered even if there was no callback generated.

| Parameters ||
|----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `codec` | [MediaCodec](MediaCodec.md):the MediaCodec instance This value cannot be`null`. |
| `presentationTimeUs` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the presentation time (media time) of the frame rendered. This is usually the same as specified in [queueInputBuffer](MediaCodec.md)); however, some codecs may alter the media time by applying some time-based transformation, such as frame rate conversion. In that case, presentation time corresponds to the actual output frame rendered. |
| `nanoTime` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The system time when the frame was rendered. |
| --- | --- |

**See Also**

- [java.lang.System#nanoTime](../java.lang/System.md))
