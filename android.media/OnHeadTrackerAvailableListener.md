# Spatializer.OnHeadTrackerAvailableListener

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnHeadTrackerAvailableListener

Kotlin| [Java](https://developer.android.com/reference/android/media/Spatializer.OnHeadTrackerAvailableListener "View this page in Java") 

```
interface OnHeadTrackerAvailableListener
```

| [android.media.Spatializer.OnHeadTrackerAvailableListener](https://developer.android.com/reference/kotlin/android/media/Spatializer.OnHeadTrackerAvailableListener#) |

Interface to be notified of changes to the availability of a head tracker on the audio device to be used by the spatializer effect.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onHeadTrackerAvailableChanged](https://developer.android.com/reference/kotlin/android/media/Spatializer.OnHeadTrackerAvailableListener#onHeadTrackerAvailableChanged(android.media.Spatializer,%20kotlin.Boolean))`(`spatializer:` ` [Spatializer](https://developer.android.com/reference/kotlin/android/media/Spatializer)`, `available:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Called when the availability of the head tracker changed. |

## Public methods

### onHeadTrackerAvailableChanged

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onHeadTrackerAvailableChanged(
    spatializer: Spatializer, 
    available: Boolean
): Unit
```

Called when the availability of the head tracker changed.

| Parameters ||
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `spatializer` | [Spatializer](https://developer.android.com/reference/kotlin/android/media/Spatializer):the`Spatializer`instance for which the head tracker availability was updated This value cannot be`null`. |
| `available` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):true if the audio device that would output audio processed by the`Spatializer`has a head tracker associated with it, false otherwise. |
