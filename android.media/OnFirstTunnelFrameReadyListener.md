# MediaCodec.OnFirstTunnelFrameReadyListener

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnFirstTunnelFrameReadyListener

Kotlin| [Java](https://developer.android.com/reference/android/media/MediaCodec.OnFirstTunnelFrameReadyListener "View this page in Java") 

```
interface OnFirstTunnelFrameReadyListener
```

| [android.media.MediaCodec.OnFirstTunnelFrameReadyListener](https://developer.android.com/reference/kotlin/android/media/MediaCodec.OnFirstTunnelFrameReadyListener#) |

Listener to be called when the first output frame has been decoded and is ready to be rendered for a codec configured for tunnel mode with`KEY_AUDIO_SESSION_ID`.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onFirstTunnelFrameReady](https://developer.android.com/reference/kotlin/android/media/MediaCodec.OnFirstTunnelFrameReadyListener#onFirstTunnelFrameReady(android.media.MediaCodec))`(`codec:` ` [MediaCodec](https://developer.android.com/reference/kotlin/android/media/MediaCodec)`)` Called when the first output frame has been decoded and is ready to be rendered. |

## Public methods

### onFirstTunnelFrameReady

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onFirstTunnelFrameReady(codec: MediaCodec): Unit
```

Called when the first output frame has been decoded and is ready to be rendered.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------|
| `codec` | [MediaCodec](https://developer.android.com/reference/kotlin/android/media/MediaCodec):This value cannot be`null`. |
