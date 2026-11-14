# FileUtils.ProgressListener

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ProgressListener

Kotlin| [Java](https://developer.android.com/reference/android/os/FileUtils.ProgressListener "View this page in Java") 

```
interface ProgressListener
```

| [android.os.FileUtils.ProgressListener](https://developer.android.com/reference/kotlin/android/os/FileUtils.ProgressListener#) |

Listener that is called periodically as progress is made.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onProgress](https://developer.android.com/reference/kotlin/android/os/FileUtils.ProgressListener#onProgress(kotlin.Long))`(`progress:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` <br /> |

## Public methods

### onProgress

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onProgress(progress: Long): Unit
```
