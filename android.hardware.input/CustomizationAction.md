Added in [API level 37.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CustomizationAction

```
abstract class CustomizationAction
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.hardware.input.CustomizationAction](https://developer.android.com/reference/kotlin/android/hardware/input/CustomizationAction#) |

| Known Direct Subclasses [AppCustomizationAction](https://developer.android.com/reference/kotlin/android/hardware/input/AppCustomizationAction), [SimpleCustomizationAction](https://developer.android.com/reference/kotlin/android/hardware/input/SimpleCustomizationAction), [UriCustomizationAction](https://developer.android.com/reference/kotlin/android/hardware/input/UriCustomizationAction) |---|---| | [AppCustomizationAction](https://developer.android.com/reference/kotlin/android/hardware/input/AppCustomizationAction) | Represents an action that launches or sends an intent to a specific application component in response to a peripheral input customization trigger. | | [SimpleCustomizationAction](https://developer.android.com/reference/kotlin/android/hardware/input/SimpleCustomizationAction) | Represents predefined simple actions, such as Volume up/down, Screenshot, etc. | | [UriCustomizationAction](https://developer.android.com/reference/kotlin/android/hardware/input/UriCustomizationAction) | Represents an action that requires an accompanying URI to execute. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Represents an action that can be associated with a peripheral customization trigger.

This is an abstract class that serves as the base for all customization actions, such as `https://developer.android.com/reference/kotlin/android/hardware/input/SimpleCustomizationAction`, `https://developer.android.com/reference/kotlin/android/hardware/input/AppCustomizationAction` and `https://developer.android.com/reference/kotlin/android/hardware/input/UriCustomizationAction`.

## Summary
