# Spatializer.OnSpatializerStateChangedListener

Added in [API level 32](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnSpatializerStateChangedListener

Kotlin| [Java](../android/media/Spatializer.OnSpatializerStateChangedListener.md) 
| --- | --- |

```
interface OnSpatializerStateChangedListener
```

| [android.media.Spatializer.OnSpatializerStateChangedListener](../android/media/Spatializer.OnSpatializerStateChangedListener.md) |

An interface to be notified of changes to the state of the spatializer effect.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onSpatializerAvailableChanged](../android/media/Spatializer.OnSpatializerStateChangedListener.md))`(`spat:` ` [Spatializer](../android/media/Spatializer.md)`, `available:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Called when the availability of the spatializer effect changes |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onSpatializerEnabledChanged](../android/media/Spatializer.OnSpatializerStateChangedListener.md))`(`spat:` ` [Spatializer](../android/media/Spatializer.md)`, `enabled:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Called when the enabled state of the spatializer effect changes |

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
| `spat` | [Spatializer](../android/media/Spatializer.md):the`Spatializer`instance whose state changed This value cannot be`null`. |
| `available` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):`true`if the spatializer effect is available and capable of processing the audio for the current configuration of the device,`false`otherwise. |

**See Also**

- [#isAvailable()](../android/media/Spatializer.md)) 

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
| `spat` | [Spatializer](../android/media/Spatializer.md):the`Spatializer`instance whose state changed This value cannot be`null`. |
| `enabled` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):`true`if the spatializer effect is enabled on the device,`false`otherwise |

**See Also**

- [#isEnabled()](../android/media/Spatializer.md))
