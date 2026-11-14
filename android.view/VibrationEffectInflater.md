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
| static [VibrationEffectInflater](VibrationEffectInflater.md) | `https://developer.android.com/reference/kotlin/android/view/VibrationEffectInflater#from(android.content.Context)(context: https://developer.android.com/reference/kotlin/android/content/Context.html#)` Obtains the `https://developer.android.com/reference/kotlin/android/view/VibrationEffectInflater#` associated with the given context. |
| [VibrationEffect](../android.os/VibrationEffect.md) | `https://developer.android.com/reference/kotlin/android/view/VibrationEffectInflater#inflate(kotlin.Int)(resId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Inflates a `https://developer.android.com/reference/kotlin/android/os/VibrationEffect.html#` from an Android XML resource containing a vibration pattern (e.g., stored inside |

## Public methods

### from

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun from(context: Context): VibrationEffectInflater
```

Obtains the `https://developer.android.com/reference/kotlin/android/view/VibrationEffectInflater#` associated with the given context.

| Parameters ||
|---|---|
| `context` | [Context](../android.content/Context.md): The context to access resources. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/VibrationEffectInflater#` | The `https://developer.android.com/reference/kotlin/android/view/VibrationEffectInflater#` instance. This value cannot be `null`. |

### inflate

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun inflate(resId: Int): VibrationEffect
```

Inflates a `https://developer.android.com/reference/kotlin/android/os/VibrationEffect.html#` from an Android XML resource containing a vibration pattern (e.g., stored inside `res/xml/`).

For dynamic vibration patterns, see `https://developer.android.com/reference/kotlin/android/os/VibrationEffect.html#parseFromXml(java.io.InputStream)`.

| Parameters ||
|---|---|
| `resId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The resource ID containing the vibration XML pattern. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/os/VibrationEffect.html#` | Parsed `https://developer.android.com/reference/kotlin/android/os/VibrationEffect.html#`. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `android.view.InflateException` | If there's an inflation error. |
