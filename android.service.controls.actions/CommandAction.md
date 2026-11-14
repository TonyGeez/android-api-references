# CommandAction

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CommandAction

Kotlin| [Java](CommandAction.md) 
| --- | --- |

```
class CommandAction : ControlAction
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.service.controls.actions.ControlAction](ControlAction.md) ||
| | ↳ | [android.service.controls.actions.CommandAction](CommandAction.md) |

A simple [ControlAction](ControlAction.md) indicating that the user has interacted with a [Control](../android.service.controls/Control.md) created using a [StatelessTemplate](../android.service.controls.templates/StatelessTemplate.md).

## Summary

| Inherited constants ||
|---|---|
| From class [ControlAction](ControlAction.md) |----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RESPONSE_CHALLENGE_ACK](ControlAction.md) <br /> Response code for the`consumer`in [ControlsProviderService.performControlAction](../android.service.controls/ControlsProviderService.md))indicating that in order for the action to be performed, acknowledgment from the user is required. Any non-empty string returned from [getChallengeValue](ControlAction.md))shall be treated as a positive acknowledgment. Value is [android.service.controls.actions.ControlAction#RESPONSE_UNKNOWN](ControlAction.md), [android.service.controls.actions.ControlAction#RESPONSE_OK](ControlAction.md), [android.service.controls.actions.ControlAction#RESPONSE_FAIL](ControlAction.md), [android.service.controls.actions.ControlAction#RESPONSE_CHALLENGE_ACK](ControlAction.md), [android.service.controls.actions.ControlAction#RESPONSE_CHALLENGE_PIN](ControlAction.md), or [android.service.controls.actions.ControlAction#RESPONSE_CHALLENGE_PASSPHRASE](ControlAction.md) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RESPONSE_CHALLENGE_PASSPHRASE](ControlAction.md) <br /> Response code for the`consumer`in [ControlsProviderService.performControlAction](../android.service.controls/ControlsProviderService.md))indicating that in order for the action to be performed, an alphanumeric passphrase is required. Value is [android.service.controls.actions.ControlAction#RESPONSE_UNKNOWN](ControlAction.md), [android.service.controls.actions.ControlAction#RESPONSE_OK](ControlAction.md), [android.service.controls.actions.ControlAction#RESPONSE_FAIL](ControlAction.md), [android.service.controls.actions.ControlAction#RESPONSE_CHALLENGE_ACK](ControlAction.md), [android.service.controls.actions.ControlAction#RESPONSE_CHALLENGE_PIN](ControlAction.md), or [android.service.controls.actions.ControlAction#RESPONSE_CHALLENGE_PASSPHRASE](ControlAction.md) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RESPONSE_CHALLENGE_PIN](ControlAction.md) <br /> Response code for the`consumer`in [ControlsProviderService.performControlAction](../android.service.controls/ControlsProviderService.md))indicating that in order for the action to be performed, a PIN is required. Value is [android.service.controls.actions.ControlAction#RESPONSE_UNKNOWN](ControlAction.md), [android.service.controls.actions.ControlAction#RESPONSE_OK](ControlAction.md), [android.service.controls.actions.ControlAction#RESPONSE_FAIL](ControlAction.md), [android.service.controls.actions.ControlAction#RESPONSE_CHALLENGE_ACK](ControlAction.md), [android.service.controls.actions.ControlAction#RESPONSE_CHALLENGE_PIN](ControlAction.md), or [android.service.controls.actions.ControlAction#RESPONSE_CHALLENGE_PASSPHRASE](ControlAction.md) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RESPONSE_FAIL](ControlAction.md) <br /> Response code for the`consumer`in [ControlsProviderService.performControlAction](../android.service.controls/ControlsProviderService.md))indicating that the action has failed. Value is [android.service.controls.actions.ControlAction#RESPONSE_UNKNOWN](ControlAction.md), [android.service.controls.actions.ControlAction#RESPONSE_OK](ControlAction.md), [android.service.controls.actions.ControlAction#RESPONSE_FAIL](ControlAction.md), [android.service.controls.actions.ControlAction#RESPONSE_CHALLENGE_ACK](ControlAction.md), [android.service.controls.actions.ControlAction#RESPONSE_CHALLENGE_PIN](ControlAction.md), or [android.service.controls.actions.ControlAction#RESPONSE_CHALLENGE_PASSPHRASE](ControlAction.md) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RESPONSE_OK](ControlAction.md) <br /> Response code for the`consumer`in [ControlsProviderService.performControlAction](../android.service.controls/ControlsProviderService.md))indicating that the action has been performed. The action may still fail later and the state may not change. Value is [android.service.controls.actions.ControlAction#RESPONSE_UNKNOWN](ControlAction.md), [android.service.controls.actions.ControlAction#RESPONSE_OK](ControlAction.md), [android.service.controls.actions.ControlAction#RESPONSE_FAIL](ControlAction.md), [android.service.controls.actions.ControlAction#RESPONSE_CHALLENGE_ACK](ControlAction.md), [android.service.controls.actions.ControlAction#RESPONSE_CHALLENGE_PIN](ControlAction.md), or [android.service.controls.actions.ControlAction#RESPONSE_CHALLENGE_PASSPHRASE](ControlAction.md) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RESPONSE_UNKNOWN](ControlAction.md) <br /> Value is [android.service.controls.actions.ControlAction#RESPONSE_UNKNOWN](ControlAction.md), [android.service.controls.actions.ControlAction#RESPONSE_OK](ControlAction.md), [android.service.controls.actions.ControlAction#RESPONSE_FAIL](ControlAction.md), [android.service.controls.actions.ControlAction#RESPONSE_CHALLENGE_ACK](ControlAction.md), [android.service.controls.actions.ControlAction#RESPONSE_CHALLENGE_PIN](ControlAction.md), or [android.service.controls.actions.ControlAction#RESPONSE_CHALLENGE_PASSPHRASE](ControlAction.md) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_BOOLEAN](ControlAction.md) <br /> The identifier of [BooleanAction](BooleanAction.md). Value is [android.service.controls.actions.ControlAction#TYPE_ERROR](ControlAction.md), [android.service.controls.actions.ControlAction#TYPE_BOOLEAN](ControlAction.md), [android.service.controls.actions.ControlAction#TYPE_FLOAT](ControlAction.md), [android.service.controls.actions.ControlAction#TYPE_MODE](ControlAction.md), or [android.service.controls.actions.ControlAction#TYPE_COMMAND](ControlAction.md) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_COMMAND](ControlAction.md) <br /> The identifier of [CommandAction](CommandAction.md). Value is [android.service.controls.actions.ControlAction#TYPE_ERROR](ControlAction.md), [android.service.controls.actions.ControlAction#TYPE_BOOLEAN](ControlAction.md), [android.service.controls.actions.ControlAction#TYPE_FLOAT](ControlAction.md), [android.service.controls.actions.ControlAction#TYPE_MODE](ControlAction.md), or [android.service.controls.actions.ControlAction#TYPE_COMMAND](ControlAction.md) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_ERROR](ControlAction.md) <br /> The identifier of the action returned by [getErrorAction](ControlAction.md)). Value is [android.service.controls.actions.ControlAction#TYPE_ERROR](ControlAction.md), [android.service.controls.actions.ControlAction#TYPE_BOOLEAN](ControlAction.md), [android.service.controls.actions.ControlAction#TYPE_FLOAT](ControlAction.md), [android.service.controls.actions.ControlAction#TYPE_MODE](ControlAction.md), or [android.service.controls.actions.ControlAction#TYPE_COMMAND](ControlAction.md) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_FLOAT](ControlAction.md) <br /> The identifier of [FloatAction](FloatAction.md). Value is [android.service.controls.actions.ControlAction#TYPE_ERROR](ControlAction.md), [android.service.controls.actions.ControlAction#TYPE_BOOLEAN](ControlAction.md), [android.service.controls.actions.ControlAction#TYPE_FLOAT](ControlAction.md), [android.service.controls.actions.ControlAction#TYPE_MODE](ControlAction.md), or [android.service.controls.actions.ControlAction#TYPE_COMMAND](ControlAction.md) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_MODE](ControlAction.md) <br /> The identifier of [ModeAction](ModeAction.md). Value is [android.service.controls.actions.ControlAction#TYPE_ERROR](ControlAction.md), [android.service.controls.actions.ControlAction#TYPE_BOOLEAN](ControlAction.md), [android.service.controls.actions.ControlAction#TYPE_FLOAT](ControlAction.md), [android.service.controls.actions.ControlAction#TYPE_MODE](ControlAction.md), or [android.service.controls.actions.ControlAction#TYPE_COMMAND](ControlAction.md) <br /> | ||

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [CommandAction](CommandAction.md))`(`templateId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` <br /> |
| [CommandAction](CommandAction.md))`(`templateId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `challengeValue:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` <br /> |

| Public methods ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getActionType](CommandAction.md))`()` <br /> |

| Inherited functions ||
|---|---|
| From class [ControlAction](ControlAction.md) |----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getChallengeValue](ControlAction.md))`()` <br /> The challenge value used to authenticate certain actions, if available. <br /> | | [ControlAction](ControlAction.md) | [getErrorAction](ControlAction.md))`()` <br /> Returns a singleton [ControlAction](ControlAction.md) used for indicating an error in unparceling. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getTemplateId](ControlAction.md))`()` <br /> The identifier of the [ControlTemplate](../android.service.controls.templates/ControlTemplate.md) that originated this action <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isValidResponse](ControlAction.md))`(`response:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> | ||

## Public constructors

### CommandAction

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
CommandAction(templateId: String)
```

| Parameters ||
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `templateId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):the identifier of the [StatelessTemplate](../android.service.controls.templates/StatelessTemplate.md) that originated this action. This value cannot be`null`. |

### CommandAction

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
CommandAction(
    templateId: String, 
    challengeValue: String?)
```

| Parameters ||
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `templateId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):the identifier of the [StatelessTemplate](../android.service.controls.templates/StatelessTemplate.md) that originated this action. This value cannot be`null`. |
| `challengeValue` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:a value sent by the user along with the action to authenticate.null is sent when no authentication is needed or has not been requested. |

## Public methods

### getActionType

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getActionType(): Int
```

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ControlAction.TYPE_COMMAND](ControlAction.md) |
