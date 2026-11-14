# SoundPool.OnLoadCompleteListener

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnLoadCompleteListener

Kotlin| [Java](../android/media/SoundPool.OnLoadCompleteListener.md) 
| --- | --- |

```
interface OnLoadCompleteListener
```

| [android.media.SoundPool.OnLoadCompleteListener](../android/media/SoundPool.OnLoadCompleteListener.md) |

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onLoadComplete](../android/media/SoundPool.OnLoadCompleteListener.md))`(`soundPool:` ` [SoundPool](../android/media/SoundPool.md)!`, `sampleId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `status:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called when a sound has completed loading. |

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
| `soundPool` | [SoundPool](../android/media/SoundPool.md)!:SoundPool object from the load() method |
| `sampleId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the sample ID of the sound loaded. |
| `status` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the status of the load operation (0 = success) |
| --- | --- |
