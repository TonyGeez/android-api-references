# VibratorManager

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# VibratorManager

Kotlin | [Java](../android/os/VibratorManager.md) 
| --- | --- |

```
abstract class VibratorManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.os.VibratorManager](../android/os/VibratorManager.md) |

Provides access to all vibrators from the device, as well as the ability to run them in a synchronized fashion.

If your process exits, any vibration you started will stop.

## Summary

| Public methods ||
|------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [cancel](../android/os/VibratorManager.md))`()` Turn all the vibrators off. |
| abstract [Vibrator](../android/os/Vibrator.md) | [getDefaultVibrator](../android/os/VibratorManager.md))`()` Returns the default Vibrator for the device. |
| abstract [Vibrator](../android/os/Vibrator.md) | [getVibrator](../android/os/VibratorManager.md))`(`vibratorId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Retrieve a single vibrator by id. |
| --- | --- |
| abstract [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html) | [getVibratorIds](../android/os/VibratorManager.md))`()` List all available vibrator ids, returning a possible empty list. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [vibrate](../android/os/VibratorManager.md))`(`effect:` ` [CombinedVibration](../android/os/CombinedVibration.md)`)` Vibrate with a given combination of effects. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [vibrate](../android/os/VibratorManager.md))`(`effect:` ` [CombinedVibration](../android/os/CombinedVibration.md)`, `attributes:` ` [VibrationAttributes](../android/os/VibrationAttributes.md)?`)` Vibrate with a given combination of effects. |
| --- | --- |

## Public methods

### cancel

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun cancel(): Unit
```

Turn all the vibrators off. 
Requires [android.Manifest.permission#VIBRATE](../android/Manifest.permission.md) 

### getDefaultVibrator

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getDefaultVibrator(): Vibrator
```

Returns the default Vibrator for the device.

| Return ||
|--------------------------------------------------------------------------------|------------------------------|
| [Vibrator](../android/os/Vibrator.md) | This value cannot be `null`. |

### getVibrator

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getVibrator(vibratorId: Int): Vibrator
```

Retrieve a single vibrator by id.

| Parameters ||
|--------------|---------------------------------------------------------------------------------------------------------------------|
| `vibratorId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The id of the vibrator to be retrieved. |

| Return ||
|--------------------------------------------------------------------------------|---------------------------------------------------|
| [Vibrator](../android/os/Vibrator.md) | The vibrator with given `vibratorId`, never null. |

### getVibratorIds

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getVibratorIds(): IntArray
```

List all available vibrator ids, returning a possible empty list.

| Return ||
|---------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html) | An array containing the ids of the vibrators available on the device. This value cannot be `null`. |

### vibrate

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun vibrate(effect: CombinedVibration): Unit
```

Vibrate with a given combination of effects.

Pass in a [CombinedVibration](../android/os/CombinedVibration.md) representing a combination of [VibrationEffects](../android/os/VibrationEffect.md) to be played on one or more vibrators.

The app should be in foreground for the vibration to happen.

Requires [android.Manifest.permission#VIBRATE](../android/Manifest.permission.md)

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `effect` | [CombinedVibration](../android/os/CombinedVibration.md): a combination of effects to be performed by one or more vibrators. This value cannot be `null`. |

### vibrate

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun vibrate(
    effect: CombinedVibration, 
    attributes: VibrationAttributes?
): Unit
```

Vibrate with a given combination of effects.

Pass in a [CombinedVibration](../android/os/CombinedVibration.md) representing a combination of [VibrationEffect](../android/os/VibrationEffect.md) to be played on one or more vibrators.

The app should be in foreground for the vibration to happen. Background apps should specify a ringtone, notification or alarm usage in order to vibrate.

Requires [android.Manifest.permission#VIBRATE](../android/Manifest.permission.md)

| Parameters ||
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `effect` | [CombinedVibration](../android/os/CombinedVibration.md): a combination of effects to be performed by one or more vibrators. This value cannot be `null`. |
| `attributes` | [VibrationAttributes](../android/os/VibrationAttributes.md)?: [VibrationAttributes](../android/os/VibrationAttributes.md) corresponding to the vibration. For example, specify [VibrationAttributes.USAGE_ALARM](../android/os/VibrationAttributes.md) for alarm vibrations or [VibrationAttributes.USAGE_RINGTONE](../android/os/VibrationAttributes.md) for vibrations associated with incoming calls. This value may be `null`. |
