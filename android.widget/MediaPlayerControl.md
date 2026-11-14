# MediaController.MediaPlayerControl

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MediaPlayerControl

Kotlin| [Java](https://developer.android.com/reference/android/widget/MediaController.MediaPlayerControl "View this page in Java") 

```
interface MediaPlayerControl
```

| [android.widget.MediaController.MediaPlayerControl](https://developer.android.com/reference/kotlin/android/widget/MediaController.MediaPlayerControl#) |

| Known Direct Subclasses [VideoView](https://developer.android.com/reference/kotlin/android/widget/VideoView) |--------------------------------------------------------------------------------------|------------------------| | [VideoView](https://developer.android.com/reference/kotlin/android/widget/VideoView) | Displays a video file. | |

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [canPause](https://developer.android.com/reference/kotlin/android/widget/MediaController.MediaPlayerControl#canPause())`()` <br /> |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [canSeekBackward](https://developer.android.com/reference/kotlin/android/widget/MediaController.MediaPlayerControl#canSeekBackward())`()` <br /> |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [canSeekForward](https://developer.android.com/reference/kotlin/android/widget/MediaController.MediaPlayerControl#canSeekForward())`()` <br /> |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getAudioSessionId](https://developer.android.com/reference/kotlin/android/widget/MediaController.MediaPlayerControl#getAudioSessionId())`()` Get the audio session id for the player used by this VideoView. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getBufferPercentage](https://developer.android.com/reference/kotlin/android/widget/MediaController.MediaPlayerControl#getBufferPercentage())`()` <br /> |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getCurrentPosition](https://developer.android.com/reference/kotlin/android/widget/MediaController.MediaPlayerControl#getCurrentPosition())`()` <br /> |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDuration](https://developer.android.com/reference/kotlin/android/widget/MediaController.MediaPlayerControl#getDuration())`()` <br /> |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isPlaying](https://developer.android.com/reference/kotlin/android/widget/MediaController.MediaPlayerControl#isPlaying())`()` <br /> |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [pause](https://developer.android.com/reference/kotlin/android/widget/MediaController.MediaPlayerControl#pause())`()` <br /> |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [seekTo](https://developer.android.com/reference/kotlin/android/widget/MediaController.MediaPlayerControl#seekTo(kotlin.Int))`(`pos:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [start](https://developer.android.com/reference/kotlin/android/widget/MediaController.MediaPlayerControl#start())`()` <br /> |

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
