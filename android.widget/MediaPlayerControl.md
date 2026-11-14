# MediaController.MediaPlayerControl

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MediaPlayerControl

Kotlin| [Java](../android/widget/MediaController.MediaPlayerControl.md) 
| --- | --- |

```
interface MediaPlayerControl
```

| [android.widget.MediaController.MediaPlayerControl](../android/widget/MediaController.MediaPlayerControl.md) |

| Known Direct Subclasses [VideoView](../android/widget/VideoView.md) |--------------------------------------------------------------------------------------|------------------------| | [VideoView](../android/widget/VideoView.md) | Displays a video file. | |
| --- | --- | --- | --- | --- | --- | --- |

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [canPause](../android/widget/MediaController.MediaPlayerControl.md))`()` <br /> |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [canSeekBackward](../android/widget/MediaController.MediaPlayerControl.md))`()` <br /> |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [canSeekForward](../android/widget/MediaController.MediaPlayerControl.md))`()` <br /> |
| --- | --- |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getAudioSessionId](../android/widget/MediaController.MediaPlayerControl.md))`()` Get the audio session id for the player used by this VideoView. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getBufferPercentage](../android/widget/MediaController.MediaPlayerControl.md))`()` <br /> |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getCurrentPosition](../android/widget/MediaController.MediaPlayerControl.md))`()` <br /> |
| --- | --- |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDuration](../android/widget/MediaController.MediaPlayerControl.md))`()` <br /> |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isPlaying](../android/widget/MediaController.MediaPlayerControl.md))`()` <br /> |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [pause](../android/widget/MediaController.MediaPlayerControl.md))`()` <br /> |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [seekTo](../android/widget/MediaController.MediaPlayerControl.md))`(`pos:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [start](../android/widget/MediaController.MediaPlayerControl.md))`()` <br /> |

## Public methods

### canPause

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun canPause(): Boolean
```  

### canSeekBackward

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun canSeekBackward(): Boolean
```  

### canSeekForward

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun canSeekForward(): Boolean
```  

### getAudioSessionId

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getAudioSessionId(): Int
```

Get the audio session id for the player used by this VideoView. This can be used to apply audio effects to the audio track of a video.

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The audio session, or 0 if there was an error. |

### getBufferPercentage

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getBufferPercentage(): Int
```  

### getCurrentPosition

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getCurrentPosition(): Int
```  

### getDuration

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getDuration(): Int
```  

### isPlaying

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isPlaying(): Boolean
```  

### pause

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun pause(): Unit
```  

### seekTo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun seekTo(pos: Int): Unit
```  

### start

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun start(): Unit
```
