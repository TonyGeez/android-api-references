# MediaCodec.OnFirstTunnelFrameReadyListener

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnFirstTunnelFrameReadyListener

Kotlin| [Java](../android/media/MediaCodec.OnFirstTunnelFrameReadyListener.md) 
| --- | --- |

```
interface OnFirstTunnelFrameReadyListener
```

| [android.media.MediaCodec.OnFirstTunnelFrameReadyListener](../android/media/MediaCodec.OnFirstTunnelFrameReadyListener.md) |

Listener to be called when the first output frame has been decoded and is ready to be rendered for a codec configured for tunnel mode with`KEY_AUDIO_SESSION_ID`.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onFirstTunnelFrameReady](../android/media/MediaCodec.OnFirstTunnelFrameReadyListener.md))`(`codec:` ` [MediaCodec](MediaCodec.md)`)` Called when the first output frame has been decoded and is ready to be rendered. |

## Public methods

### onFirstTunnelFrameReady

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onFirstTunnelFrameReady(codec: MediaCodec): Unit
```

Called when the first output frame has been decoded and is ready to be rendered.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------|
| `codec` | [MediaCodec](MediaCodec.md):This value cannot be`null`. |
