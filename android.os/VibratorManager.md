# VibratorManager

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# VibratorManager

Kotlin | [Java](https://developer.android.com/reference/android/os/VibratorManager "View this page in Java") 

```
abstract class VibratorManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.os.VibratorManager](https://developer.android.com/reference/kotlin/android/os/VibratorManager#) |

Provides access to all vibrators from the device, as well as the ability to run them in a synchronized fashion.

If your process exits, any vibration you started will stop.

## Summary

| Public methods ||
|------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [cancel](https://developer.android.com/reference/kotlin/android/os/VibratorManager#cancel())`()` Turn all the vibrators off. |
| abstract [Vibrator](https://developer.android.com/reference/kotlin/android/os/Vibrator) | [getDefaultVibrator](https://developer.android.com/reference/kotlin/android/os/VibratorManager#getDefaultVibrator())`()` Returns the default Vibrator for the device. |
| abstract [Vibrator](https://developer.android.com/reference/kotlin/android/os/Vibrator) | [getVibrator](https://developer.android.com/reference/kotlin/android/os/VibratorManager#getVibrator(kotlin.Int))`(`vibratorId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Retrieve a single vibrator by id. |
| abstract [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html) | [getVibratorIds](https://developer.android.com/reference/kotlin/android/os/VibratorManager#getVibratorIds())`()` List all available vibrator ids, returning a possible empty list. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [vibrate](https://developer.android.com/reference/kotlin/android/os/VibratorManager#vibrate(android.os.CombinedVibration))`(`effect:` ` [CombinedVibration](https://developer.android.com/reference/kotlin/android/os/CombinedVibration)`)` Vibrate with a given combination of effects. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [vibrate](https://developer.android.com/reference/kotlin/android/os/VibratorManager#vibrate(android.os.CombinedVibration,%20android.os.VibrationAttributes))`(`effect:` ` [CombinedVibration](https://developer.android.com/reference/kotlin/android/os/CombinedVibration)`, `attributes:` ` [VibrationAttributes](https://developer.android.com/reference/kotlin/android/os/VibrationAttributes)?`)` Vibrate with a given combination of effects. |

## Public methods

### cancel

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun cancel(): Unit
```

Turn all the vibrators off. 
Requires [android.Manifest.permission#VIBRATE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#VIBRATE:kotlin.String) 

### getDefaultVibrator

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getDefaultVibrator(): Vibrator
```

Returns the default Vibrator for the device.

| Return ||
|--------------------------------------------------------------------------------|------------------------------|
| [Vibrator](https://developer.android.com/reference/kotlin/android/os/Vibrator) | This value cannot be `null`. |

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
| [Vibrator](https://developer.android.com/reference/kotlin/android/os/Vibrator) | The vibrator with given `vibratorId`, never null. |

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

Pass in a [CombinedVibration](https://developer.android.com/reference/kotlin/android/os/CombinedVibration) representing a combination of [VibrationEffects](https://developer.android.com/reference/kotlin/android/os/VibrationEffect) to be played on one or more vibrators.

The app should be in foreground for the vibration to happen.

Requires [android.Manifest.permission#VIBRATE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#VIBRATE:kotlin.String)

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `effect` | [CombinedVibration](https://developer.android.com/reference/kotlin/android/os/CombinedVibration): a combination of effects to be performed by one or more vibrators. This value cannot be `null`. |

### vibrate

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun vibrate(
    effect: CombinedVibration, 
    attributes: VibrationAttributes?
): Unit
```

Vibrate with a given combination of effects.

Pass in a [CombinedVibration](https://developer.android.com/reference/kotlin/android/os/CombinedVibration) representing a combination of [VibrationEffect](https://developer.android.com/reference/kotlin/android/os/VibrationEffect) to be played on one or more vibrators.

The app should be in foreground for the vibration to happen. Background apps should specify a ringtone, notification or alarm usage in order to vibrate.

Requires [android.Manifest.permission#VIBRATE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#VIBRATE:kotlin.String)

| Parameters ||
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `effect` | [CombinedVibration](https://developer.android.com/reference/kotlin/android/os/CombinedVibration): a combination of effects to be performed by one or more vibrators. This value cannot be `null`. |
| `attributes` | [VibrationAttributes](https://developer.android.com/reference/kotlin/android/os/VibrationAttributes)?: [VibrationAttributes](https://developer.android.com/reference/kotlin/android/os/VibrationAttributes) corresponding to the vibration. For example, specify [VibrationAttributes.USAGE_ALARM](https://developer.android.com/reference/kotlin/android/os/VibrationAttributes#USAGE_ALARM:kotlin.Int) for alarm vibrations or [VibrationAttributes.USAGE_RINGTONE](https://developer.android.com/reference/kotlin/android/os/VibrationAttributes#USAGE_RINGTONE:kotlin.Int) for vibrations associated with incoming calls. This value may be `null`. |
