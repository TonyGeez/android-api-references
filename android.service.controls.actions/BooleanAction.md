# BooleanAction

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BooleanAction

Kotlin| [Java](BooleanAction.md) 
| --- | --- |

```
class BooleanAction : ControlAction
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.service.controls.actions.ControlAction](ControlAction.md) ||
| | ↳ | [android.service.controls.actions.BooleanAction](BooleanAction.md) |

Action sent by user toggling a [Control](../android.service.controls/Control.md) between checked/unchecked. This action is available when the [Control](../android.service.controls/Control.md) was constructed with either a [ToggleTemplate](../android.service.controls.templates/ToggleTemplate.md) or a [ToggleRangeTemplate](../android.service.controls.templates/ToggleRangeTemplate.md).

## Summary

| Inherited constants ||
|---|---|
| From class [ControlAction](ControlAction.md) |----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RESPONSE_CHALLENGE_ACK](ControlAction.md) <br /> Response code for the`consumer`in [ControlsProviderService.performControlAction](../android.service.controls/ControlsProviderService.md))indicating that in order for the action to be performed, acknowledgment from the user is required. Any non-empty string returned from [getChallengeValue](ControlAction.md))shall be treated as a positive acknowledgment. Value is [android.service.controls.actions.ControlAction#RESPONSE_UNKNOWN](ControlAction.md), [android.service.controls.actions.ControlAction#RESPONSE_OK](ControlAction.md), [android.service.controls.actions.ControlAction#RESPONSE_FAIL](ControlAction.md), [android.service.controls.actions.ControlAction#RESPONSE_CHALLENGE_ACK](ControlAction.md), [android.service.controls.actions.ControlAction#RESPONSE_CHALLENGE_PIN](ControlAction.md), or [android.service.controls.actions.ControlAction#RESPONSE_CHALLENGE_PASSPHRASE](ControlAction.md) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RESPONSE_CHALLENGE_PASSPHRASE](ControlAction.md) <br /> Response code for the`consumer`in [ControlsProviderService.performControlAction](../android.service.controls/ControlsProviderService.md))indicating that in order for the action to be performed, an alphanumeric passphrase is required. Value is [android.service.controls.actions.ControlAction#RESPONSE_UNKNOWN](ControlAction.md), [android.service.controls.actions.ControlAction#RESPONSE_OK](ControlAction.md), [android.service.controls.actions.ControlAction#RESPONSE_FAIL](ControlAction.md), [android.service.controls.actions.ControlAction#RESPONSE_CHALLENGE_ACK](ControlAction.md), [android.service.controls.actions.ControlAction#RESPONSE_CHALLENGE_PIN](ControlAction.md), or [android.service.controls.actions.ControlAction#RESPONSE_CHALLENGE_PASSPHRASE](ControlAction.md) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RESPONSE_CHALLENGE_PIN](ControlAction.md) <br /> Response code for the`consumer`in [ControlsProviderService.performControlAction](../android.service.controls/ControlsProviderService.md))indicating that in order for the action to be performed, a PIN is required. Value is [android.service.controls.actions.ControlAction#RESPONSE_UNKNOWN](ControlAction.md), [android.service.controls.actions.ControlAction#RESPONSE_OK](ControlAction.md), [android.service.controls.actions.ControlAction#RESPONSE_FAIL](ControlAction.md), [android.service.controls.actions.ControlAction#RESPONSE_CHALLENGE_ACK](ControlAction.md), [android.service.controls.actions.ControlAction#RESPONSE_CHALLENGE_PIN](ControlAction.md), or [android.service.controls.actions.ControlAction#RESPONSE_CHALLENGE_PASSPHRASE](ControlAction.md) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RESPONSE_FAIL](ControlAction.md) <br /> Response code for the`consumer`in [ControlsProviderService.performControlAction](../android.service.controls/ControlsProviderService.md))indicating that the action has failed. Value is [android.service.controls.actions.ControlAction#RESPONSE_UNKNOWN](ControlAction.md), [android.service.controls.actions.ControlAction#RESPONSE_OK](ControlAction.md), [android.service.controls.actions.ControlAction#RESPONSE_FAIL](ControlAction.md), [android.service.controls.actions.ControlAction#RESPONSE_CHALLENGE_ACK](ControlAction.md), [android.service.controls.actions.ControlAction#RESPONSE_CHALLENGE_PIN](ControlAction.md), or [android.service.controls.actions.ControlAction#RESPONSE_CHALLENGE_PASSPHRASE](ControlAction.md) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RESPONSE_OK](ControlAction.md) <br /> Response code for the`consumer`in [ControlsProviderService.performControlAction](../android.service.controls/ControlsProviderService.md))indicating that the action has been performed. The action may still fail later and the state may not change. Value is [android.service.controls.actions.ControlAction#RESPONSE_UNKNOWN](ControlAction.md), [android.service.controls.actions.ControlAction#RESPONSE_OK](ControlAction.md), [android.service.controls.actions.ControlAction#RESPONSE_FAIL](ControlAction.md), [android.service.controls.actions.ControlAction#RESPONSE_CHALLENGE_ACK](ControlAction.md), [android.service.controls.actions.ControlAction#RESPONSE_CHALLENGE_PIN](ControlAction.md), or [android.service.controls.actions.ControlAction#RESPONSE_CHALLENGE_PASSPHRASE](ControlAction.md) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RESPONSE_UNKNOWN](ControlAction.md) <br /> Value is [android.service.controls.actions.ControlAction#RESPONSE_UNKNOWN](ControlAction.md), [android.service.controls.actions.ControlAction#RESPONSE_OK](ControlAction.md), [android.service.controls.actions.ControlAction#RESPONSE_FAIL](ControlAction.md), [android.service.controls.actions.ControlAction#RESPONSE_CHALLENGE_ACK](ControlAction.md), [android.service.controls.actions.ControlAction#RESPONSE_CHALLENGE_PIN](ControlAction.md), or [android.service.controls.actions.ControlAction#RESPONSE_CHALLENGE_PASSPHRASE](ControlAction.md) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_BOOLEAN](ControlAction.md) <br /> The identifier of [BooleanAction](BooleanAction.md). Value is [android.service.controls.actions.ControlAction#TYPE_ERROR](ControlAction.md), [android.service.controls.actions.ControlAction#TYPE_BOOLEAN](ControlAction.md), [android.service.controls.actions.ControlAction#TYPE_FLOAT](ControlAction.md), [android.service.controls.actions.ControlAction#TYPE_MODE](ControlAction.md), or [android.service.controls.actions.ControlAction#TYPE_COMMAND](ControlAction.md) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_COMMAND](ControlAction.md) <br /> The identifier of [CommandAction](CommandAction.md). Value is [android.service.controls.actions.ControlAction#TYPE_ERROR](ControlAction.md), [android.service.controls.actions.ControlAction#TYPE_BOOLEAN](ControlAction.md), [android.service.controls.actions.ControlAction#TYPE_FLOAT](ControlAction.md), [android.service.controls.actions.ControlAction#TYPE_MODE](ControlAction.md), or [android.service.controls.actions.ControlAction#TYPE_COMMAND](ControlAction.md) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_ERROR](ControlAction.md) <br /> The identifier of the action returned by [getErrorAction](ControlAction.md)). Value is [android.service.controls.actions.ControlAction#TYPE_ERROR](ControlAction.md), [android.service.controls.actions.ControlAction#TYPE_BOOLEAN](ControlAction.md), [android.service.controls.actions.ControlAction#TYPE_FLOAT](ControlAction.md), [android.service.controls.actions.ControlAction#TYPE_MODE](ControlAction.md), or [android.service.controls.actions.ControlAction#TYPE_COMMAND](ControlAction.md) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_FLOAT](ControlAction.md) <br /> The identifier of [FloatAction](FloatAction.md). Value is [android.service.controls.actions.ControlAction#TYPE_ERROR](ControlAction.md), [android.service.controls.actions.ControlAction#TYPE_BOOLEAN](ControlAction.md), [android.service.controls.actions.ControlAction#TYPE_FLOAT](ControlAction.md), [android.service.controls.actions.ControlAction#TYPE_MODE](ControlAction.md), or [android.service.controls.actions.ControlAction#TYPE_COMMAND](ControlAction.md) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_MODE](ControlAction.md) <br /> The identifier of [ModeAction](ModeAction.md). Value is [android.service.controls.actions.ControlAction#TYPE_ERROR](ControlAction.md), [android.service.controls.actions.ControlAction#TYPE_BOOLEAN](ControlAction.md), [android.service.controls.actions.ControlAction#TYPE_FLOAT](ControlAction.md), [android.service.controls.actions.ControlAction#TYPE_MODE](ControlAction.md), or [android.service.controls.actions.ControlAction#TYPE_COMMAND](ControlAction.md) <br /> | ||

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [BooleanAction](BooleanAction.md))`(`templateId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `newState:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> |
| [BooleanAction](BooleanAction.md))`(`templateId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `newState:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `challengeValue:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` <br /> |

| Public methods ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getActionType](BooleanAction.md))`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getNewState](BooleanAction.md))`()` The new state set for the button in the corresponding [ToggleTemplate](../android.service.controls.templates/ToggleTemplate.md). |

| Inherited functions ||
|---|---|
| From class [ControlAction](ControlAction.md) |----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getChallengeValue](ControlAction.md))`()` <br /> The challenge value used to authenticate certain actions, if available. <br /> | | [ControlAction](ControlAction.md) | [getErrorAction](ControlAction.md))`()` <br /> Returns a singleton [ControlAction](ControlAction.md) used for indicating an error in unparceling. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getTemplateId](ControlAction.md))`()` <br /> The identifier of the [ControlTemplate](../android.service.controls.templates/ControlTemplate.md) that originated this action <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isValidResponse](ControlAction.md))`(`response:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> | ||

## Public constructors

### BooleanAction

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
BooleanAction(
    templateId: String, 
    newState: Boolean)
```

| Parameters ||
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `templateId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):the identifier of the [ToggleTemplate](../android.service.controls.templates/ToggleTemplate.md) that produced this action. This value cannot be`null`. |
| `newState` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):new value for the state displayed by the [ToggleTemplate](../android.service.controls.templates/ToggleTemplate.md). |

### BooleanAction

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
BooleanAction(
    templateId: String, 
    newState: Boolean, 
    challengeValue: String?)
```

| Parameters ||
|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `templateId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):the identifier of the template that originated this action. This value cannot be`null`. |
| `newState` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):new value for the state displayed by the template. |
| `challengeValue` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:a value sent by the user along with the action to authenticate.null is sent when no authentication is needed or has not been requested. |
| --- | --- |

## Public methods

### getActionType

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getActionType(): Int
```

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ControlAction.TYPE_BOOLEAN](ControlAction.md) |

### getNewState

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getNewState(): Boolean
```

The new state set for the button in the corresponding [ToggleTemplate](../android.service.controls.templates/ToggleTemplate.md).

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the button was toggled from unchecked to checked. |
