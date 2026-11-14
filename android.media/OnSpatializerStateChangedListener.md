# Spatializer.OnSpatializerStateChangedListener

Added in [API level 32](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnSpatializerStateChangedListener

Kotlin| [Java](https://developer.android.com/reference/android/media/Spatializer.OnSpatializerStateChangedListener "View this page in Java") 

```
interface OnSpatializerStateChangedListener
```

| [android.media.Spatializer.OnSpatializerStateChangedListener](https://developer.android.com/reference/kotlin/android/media/Spatializer.OnSpatializerStateChangedListener#) |

An interface to be notified of changes to the state of the spatializer effect.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onSpatializerAvailableChanged](https://developer.android.com/reference/kotlin/android/media/Spatializer.OnSpatializerStateChangedListener#onSpatializerAvailableChanged(android.media.Spatializer,%20kotlin.Boolean))`(`spat:` ` [Spatializer](https://developer.android.com/reference/kotlin/android/media/Spatializer)`, `available:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Called when the availability of the spatializer effect changes |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onSpatializerEnabledChanged](https://developer.android.com/reference/kotlin/android/media/Spatializer.OnSpatializerStateChangedListener#onSpatializerEnabledChanged(android.media.Spatializer,%20kotlin.Boolean))`(`spat:` ` [Spatializer](https://developer.android.com/reference/kotlin/android/media/Spatializer)`, `enabled:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Called when the enabled state of the spatializer effect changes |

## Public methods

### onSpatializerAvailableChanged

Added in [API level 32](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onSpatializerAvailableChanged(
    spat: Spatializer, 
    available: Boolean
): Unit
```

Called when the availability of the spatializer effect changes

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `spat` | [Spatializer](https://developer.android.com/reference/kotlin/android/media/Spatializer):the`Spatializer`instance whose state changed This value cannot be`null`. |
| `available` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):`true`if the spatializer effect is available and capable of processing the audio for the current configuration of the device,`false`otherwise. |

**See Also**

- [#isAvailable()](https://developer.android.com/reference/kotlin/android/media/Spatializer#isAvailable()) 

### onSpatializerEnabledChanged

Added in [API level 32](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onSpatializerEnabledChanged(
    spat: Spatializer, 
    enabled: Boolean
): Unit
```

Called when the enabled state of the spatializer effect changes

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `spat` | [Spatializer](https://developer.android.com/reference/kotlin/android/media/Spatializer):the`Spatializer`instance whose state changed This value cannot be`null`. |
| `enabled` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):`true`if the spatializer effect is enabled on the device,`false`otherwise |

**See Also**

- [#isEnabled()](https://developer.android.com/reference/kotlin/android/media/Spatializer#isEnabled())
