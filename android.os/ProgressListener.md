# FileUtils.ProgressListener

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ProgressListener

Kotlin| [Java](../android/os/FileUtils.ProgressListener.md) 
| --- | --- |

```
interface ProgressListener
```

| [android.os.FileUtils.ProgressListener](../android/os/FileUtils.ProgressListener.md) |

Listener that is called periodically as progress is made.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onProgress](../android/os/FileUtils.ProgressListener.md))`(`progress:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` <br /> |

## Public methods

### onProgress

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onProgress(progress: Long): Unit
```
