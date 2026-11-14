Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# VibrationEffectInflater

```
class VibrationEffectInflater
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.view.VibrationEffectInflater](VibrationEffectInflater.md) |

Instantiates `https://developer.android.com/reference/kotlin/android/os/VibrationEffect.html#` objects from Android XML resources.

## Summary

| Public methods ||
|---|---|
| static [VibrationEffectInflater](VibrationEffectInflater.md) | from Obtains the VibrationEffectInflater associated with the given context. |
| [VibrationEffect](../android.os/VibrationEffect.md) | inflate Inflates a `https://developer.android.com/reference/kotlin/android/os/VibrationEffect.html#` from an Android XML resource containing a vibration pattern (e.g., stored inside |

## Public methods

### from

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun from(context: Context): VibrationEffectInflater
```

Obtains the VibrationEffectInflater associated with the given context.

| Parameters ||
|---|---|
| `context` | [Context](../android.content/Context.md): The context to access resources. This value cannot be `null`. |

| Return ||
|---|---|
| VibrationEffectInflater | The VibrationEffectInflater instance. This value cannot be `null`. |

### inflate

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun inflate(resId: Int): VibrationEffect
```

Inflates a `https://developer.android.com/reference/kotlin/android/os/VibrationEffect.html#` from an Android XML resource containing a vibration pattern (e.g., stored inside `res/xml/`).

For dynamic vibration patterns, see parseFromXml.

| Parameters ||
|---|---|
| `resId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The resource ID containing the vibration XML pattern. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/os/VibrationEffect.html#` | Parsed `https://developer.android.com/reference/kotlin/android/os/VibrationEffect.html#`. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `android.view.InflateException` | If there's an inflation error. |
