# VibratorManager

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# VibratorManager

Kotlin | [Java](VibratorManager.md) 
| --- | --- |

```
abstract class VibratorManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.os.VibratorManager](VibratorManager.md) |

Provides access to all vibrators from the device, as well as the ability to run them in a synchronized fashion.

If your process exits, any vibration you started will stop.

## Summary

| Public methods ||
|------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [cancel](VibratorManager.md))`()` Turn all the vibrators off. |
| abstract [Vibrator](Vibrator.md) | [getDefaultVibrator](VibratorManager.md))`()` Returns the default Vibrator for the device. |
| abstract [Vibrator](Vibrator.md) | [getVibrator](VibratorManager.md))`(`vibratorId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Retrieve a single vibrator by id. |
| --- | --- |
| abstract [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html) | [getVibratorIds](VibratorManager.md))`()` List all available vibrator ids, returning a possible empty list. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [vibrate](VibratorManager.md))`(`effect:` ` [CombinedVibration](CombinedVibration.md)`)` Vibrate with a given combination of effects. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [vibrate](VibratorManager.md))`(`effect:` ` [CombinedVibration](CombinedVibration.md)`, `attributes:` ` [VibrationAttributes](VibrationAttributes.md)?`)` Vibrate with a given combination of effects. |
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
| [Vibrator](Vibrator.md) | This value cannot be `null`. |

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
| [Vibrator](Vibrator.md) | The vibrator with given `vibratorId`, never null. |

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

Pass in a [CombinedVibration](CombinedVibration.md) representing a combination of [VibrationEffects](VibrationEffect.md) to be played on one or more vibrators.

The app should be in foreground for the vibration to happen.

Requires [android.Manifest.permission#VIBRATE](../android/Manifest.permission.md)

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `effect` | [CombinedVibration](CombinedVibration.md): a combination of effects to be performed by one or more vibrators. This value cannot be `null`. |

### vibrate

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun vibrate(
    effect: CombinedVibration, 
    attributes: VibrationAttributes?
): Unit
```

Vibrate with a given combination of effects.

Pass in a [CombinedVibration](CombinedVibration.md) representing a combination of [VibrationEffect](VibrationEffect.md) to be played on one or more vibrators.

The app should be in foreground for the vibration to happen. Background apps should specify a ringtone, notification or alarm usage in order to vibrate.

Requires [android.Manifest.permission#VIBRATE](../android/Manifest.permission.md)

| Parameters ||
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `effect` | [CombinedVibration](CombinedVibration.md): a combination of effects to be performed by one or more vibrators. This value cannot be `null`. |
| `attributes` | [VibrationAttributes](VibrationAttributes.md)?: [VibrationAttributes](VibrationAttributes.md) corresponding to the vibration. For example, specify [VibrationAttributes.USAGE_ALARM](VibrationAttributes.md) for alarm vibrations or [VibrationAttributes.USAGE_RINGTONE](VibrationAttributes.md) for vibrations associated with incoming calls. This value may be `null`. |
