# SoundPool.OnLoadCompleteListener

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnLoadCompleteListener

Kotlin| [Java](https://developer.android.com/reference/android/media/SoundPool.OnLoadCompleteListener "View this page in Java") 
| --- | --- |

```
interface OnLoadCompleteListener
```

| [android.media.SoundPool.OnLoadCompleteListener](https://developer.android.com/reference/kotlin/android/media/SoundPool.OnLoadCompleteListener#) |

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onLoadComplete](https://developer.android.com/reference/kotlin/android/media/SoundPool.OnLoadCompleteListener#onLoadComplete(android.media.SoundPool,%20kotlin.Int,%20kotlin.Int))`(`soundPool:` ` [SoundPool](https://developer.android.com/reference/kotlin/android/media/SoundPool)!`, `sampleId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `status:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called when a sound has completed loading. |

## Public methods

### onLoadComplete

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onLoadComplete(
    soundPool: SoundPool!, 
    sampleId: Int, 
    status: Int
): Unit
```

Called when a sound has completed loading.

| Parameters ||
|-------------|------------------------------------------------------------------------------------------------------------------------------|
| `soundPool` | [SoundPool](https://developer.android.com/reference/kotlin/android/media/SoundPool)!:SoundPool object from the load() method |
| `sampleId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the sample ID of the sound loaded. |
| `status` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the status of the load operation (0 = success) |
| --- | --- |
