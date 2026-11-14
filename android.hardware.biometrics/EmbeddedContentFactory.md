Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# EmbeddedContentFactory

```
interface EmbeddedContentFactory
```

| [android.hardware.biometrics.EmbeddedBiometricPrompt.EmbeddedContentFactory](https://developer.android.com/reference/kotlin/android/hardware/biometrics/EmbeddedBiometricPrompt.EmbeddedContentFactory#) |

A factory that produces the custom embedded content view for the biometric prompt. This allows the view to be inflated with the correct display metrics.

## Summary

| Public methods ||
|---|---|
| abstract [View](https://developer.android.com/reference/kotlin/android/view/View.html#) | `https://developer.android.com/reference/kotlin/android/hardware/biometrics/EmbeddedBiometricPrompt.EmbeddedContentFactory#createView(android.content.Context)(context: https://developer.android.com/reference/kotlin/android/content/Context.html#)` <br /> |

## Public methods

### createView

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun createView(context: Context): View
```

| Parameters ||
|---|---|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#): The `https://developer.android.com/reference/kotlin/android/content/Context.html#` to use for creating or inflating the view. This context has the correct density for the host display. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/View.html#` | The `https://developer.android.com/reference/kotlin/android/view/View.html#` to be shown in the biometric prompt. This value cannot be `null`. |
