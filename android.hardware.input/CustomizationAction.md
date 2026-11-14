Added in [API level 37.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CustomizationAction

```
abstract class CustomizationAction
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.hardware.input.CustomizationAction](CustomizationAction.md) |

| Known Direct Subclasses [AppCustomizationAction](AppCustomizationAction.md), [SimpleCustomizationAction](SimpleCustomizationAction.md), [UriCustomizationAction](UriCustomizationAction.md) |---|---| | [AppCustomizationAction](AppCustomizationAction.md) | Represents an action that launches or sends an intent to a specific application component in response to a peripheral input customization trigger. | | [SimpleCustomizationAction](SimpleCustomizationAction.md) | Represents predefined simple actions, such as Volume up/down, Screenshot, etc. | | [UriCustomizationAction](UriCustomizationAction.md) | Represents an action that requires an accompanying URI to execute. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Represents an action that can be associated with a peripheral customization trigger.

This is an abstract class that serves as the base for all customization actions, such as SimpleCustomizationAction, AppCustomizationAction and UriCustomizationAction.

## Summary
