# ControlAction

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ControlAction

Kotlin| [Java](../android/service/controls/actions/ControlAction.md) 
| --- | --- |

```
abstract class ControlAction
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.service.controls.actions.ControlAction](../android/service/controls/actions/ControlAction.md) |

| Known Direct Subclasses [BooleanAction](../android/service/controls/actions/BooleanAction.md), [CommandAction](../android/service/controls/actions/CommandAction.md), [FloatAction](../android/service/controls/actions/FloatAction.md), [ModeAction](../android/service/controls/actions/ModeAction.md) |----------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [BooleanAction](../android/service/controls/actions/BooleanAction.md) | Action sent by user toggling a [Control](../android/service/controls/Control.md) between checked/unchecked. | | [CommandAction](../android/service/controls/actions/CommandAction.md) | A simple [ControlAction](../android/service/controls/actions/ControlAction.md) indicating that the user has interacted with a [Control](../android/service/controls/Control.md) created using a [StatelessTemplate](../android/service/controls/templates/StatelessTemplate.md). | | [FloatAction](../android/service/controls/actions/FloatAction.md) | Action sent by a [RangeTemplate](../android/service/controls/templates/RangeTemplate.md), [ToggleRangeTemplate](../android/service/controls/templates/ToggleRangeTemplate.md). | | [ModeAction](../android/service/controls/actions/ModeAction.md) | Action sent by the user to indicate a change of mode. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

An abstract action indicating a user interaction with a [Control](../android/service/controls/Control.md). In some cases, an action needs to be validated by the user, using a password, PIN or simple acknowledgment. For those cases, an optional (nullable) parameter can be passed to send the user input. This**challenge value** will be requested from the user and sent as part of a [ControlAction](../android/service/controls/actions/ControlAction.md) only if the service has responded to an action with one of:

- [RESPONSE_CHALLENGE_ACK](../android/service/controls/actions/ControlAction.md)
- [RESPONSE_CHALLENGE_PIN](../android/service/controls/actions/ControlAction.md)
- [RESPONSE_CHALLENGE_PASSPHRASE](../android/service/controls/actions/ControlAction.md)

<br />

## Summary

| Constants ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RESPONSE_CHALLENGE_ACK](../android/service/controls/actions/ControlAction.md) Response code for the`consumer`in [ControlsProviderService.performControlAction](../android/service/controls/ControlsProviderService.md))indicating that in order for the action to be performed, acknowledgment from the user is required. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RESPONSE_CHALLENGE_PASSPHRASE](../android/service/controls/actions/ControlAction.md) Response code for the`consumer`in [ControlsProviderService.performControlAction](../android/service/controls/ControlsProviderService.md))indicating that in order for the action to be performed, an alphanumeric passphrase is required. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RESPONSE_CHALLENGE_PIN](../android/service/controls/actions/ControlAction.md) Response code for the`consumer`in [ControlsProviderService.performControlAction](../android/service/controls/ControlsProviderService.md))indicating that in order for the action to be performed, a PIN is required. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RESPONSE_FAIL](../android/service/controls/actions/ControlAction.md) Response code for the`consumer`in [ControlsProviderService.performControlAction](../android/service/controls/ControlsProviderService.md))indicating that the action has failed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RESPONSE_OK](../android/service/controls/actions/ControlAction.md) Response code for the`consumer`in [ControlsProviderService.performControlAction](../android/service/controls/ControlsProviderService.md))indicating that the action has been performed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RESPONSE_UNKNOWN](../android/service/controls/actions/ControlAction.md) Value is [android.service.controls.actions.ControlAction#RESPONSE_UNKNOWN](../android/service/controls/actions/ControlAction.md), [android.service.controls.actions.ControlAction#RESPONSE_OK](../android/service/controls/actions/ControlAction.md), [android.service.controls.actions.ControlAction#RESPONSE_FAIL](../android/service/controls/actions/ControlAction.md), [android.service.controls.actions.ControlAction#RESPONSE_CHALLENGE_ACK](../android/service/controls/actions/ControlAction.md), [android.service.controls.actions.ControlAction#RESPONSE_CHALLENGE_PIN](../android/service/controls/actions/ControlAction.md), or [android.service.controls.actions.ControlAction#RESPONSE_CHALLENGE_PASSPHRASE](../android/service/controls/actions/ControlAction.md) |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_BOOLEAN](../android/service/controls/actions/ControlAction.md) The identifier of [BooleanAction](../android/service/controls/actions/BooleanAction.md). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_COMMAND](../android/service/controls/actions/ControlAction.md) The identifier of [CommandAction](../android/service/controls/actions/CommandAction.md). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_ERROR](../android/service/controls/actions/ControlAction.md) The identifier of the action returned by [getErrorAction](../android/service/controls/actions/ControlAction.md)). |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_FLOAT](../android/service/controls/actions/ControlAction.md) The identifier of [FloatAction](../android/service/controls/actions/FloatAction.md). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_MODE](../android/service/controls/actions/ControlAction.md) The identifier of [ModeAction](../android/service/controls/actions/ModeAction.md). |

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getActionType](../android/service/controls/actions/ControlAction.md))`()` The action type associated with this class. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getChallengeValue](../android/service/controls/actions/ControlAction.md))`()` The challenge value used to authenticate certain actions, if available. |
| openstatic [ControlAction](../android/service/controls/actions/ControlAction.md) | [getErrorAction](../android/service/controls/actions/ControlAction.md))`()` Returns a singleton [ControlAction](../android/service/controls/actions/ControlAction.md) used for indicating an error in unparceling. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getTemplateId](../android/service/controls/actions/ControlAction.md))`()` The identifier of the [ControlTemplate](../android/service/controls/templates/ControlTemplate.md) that originated this action |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isValidResponse](../android/service/controls/actions/ControlAction.md))`(`response:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

## Constants

### RESPONSE_CHALLENGE_ACK

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RESPONSE_CHALLENGE_ACK: Int
```

Response code for the`consumer`in [ControlsProviderService.performControlAction](../android/service/controls/ControlsProviderService.md))indicating that in order for the action to be performed, acknowledgment from the user is required. Any non-empty string returned from [getChallengeValue](../android/service/controls/actions/ControlAction.md))shall be treated as a positive acknowledgment. 
Value is [android.service.controls.actions.ControlAction#RESPONSE_UNKNOWN](../android/service/controls/actions/ControlAction.md), [android.service.controls.actions.ControlAction#RESPONSE_OK](../android/service/controls/actions/ControlAction.md), [android.service.controls.actions.ControlAction#RESPONSE_FAIL](../android/service/controls/actions/ControlAction.md), [android.service.controls.actions.ControlAction#RESPONSE_CHALLENGE_ACK](../android/service/controls/actions/ControlAction.md), [android.service.controls.actions.ControlAction#RESPONSE_CHALLENGE_PIN](../android/service/controls/actions/ControlAction.md), or [android.service.controls.actions.ControlAction#RESPONSE_CHALLENGE_PASSPHRASE](../android/service/controls/actions/ControlAction.md) 

 Value: 3

### RESPONSE_CHALLENGE_PASSPHRASE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RESPONSE_CHALLENGE_PASSPHRASE: Int
```

Response code for the`consumer`in [ControlsProviderService.performControlAction](../android/service/controls/ControlsProviderService.md))indicating that in order for the action to be performed, an alphanumeric passphrase is required. 
Value is [android.service.controls.actions.ControlAction#RESPONSE_UNKNOWN](../android/service/controls/actions/ControlAction.md), [android.service.controls.actions.ControlAction#RESPONSE_OK](../android/service/controls/actions/ControlAction.md), [android.service.controls.actions.ControlAction#RESPONSE_FAIL](../android/service/controls/actions/ControlAction.md), [android.service.controls.actions.ControlAction#RESPONSE_CHALLENGE_ACK](../android/service/controls/actions/ControlAction.md), [android.service.controls.actions.ControlAction#RESPONSE_CHALLENGE_PIN](../android/service/controls/actions/ControlAction.md), or [android.service.controls.actions.ControlAction#RESPONSE_CHALLENGE_PASSPHRASE](../android/service/controls/actions/ControlAction.md) 

 Value: 5

### RESPONSE_CHALLENGE_PIN

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RESPONSE_CHALLENGE_PIN: Int
```

Response code for the`consumer`in [ControlsProviderService.performControlAction](../android/service/controls/ControlsProviderService.md))indicating that in order for the action to be performed, a PIN is required. 
Value is [android.service.controls.actions.ControlAction#RESPONSE_UNKNOWN](../android/service/controls/actions/ControlAction.md), [android.service.controls.actions.ControlAction#RESPONSE_OK](../android/service/controls/actions/ControlAction.md), [android.service.controls.actions.ControlAction#RESPONSE_FAIL](../android/service/controls/actions/ControlAction.md), [android.service.controls.actions.ControlAction#RESPONSE_CHALLENGE_ACK](../android/service/controls/actions/ControlAction.md), [android.service.controls.actions.ControlAction#RESPONSE_CHALLENGE_PIN](../android/service/controls/actions/ControlAction.md), or [android.service.controls.actions.ControlAction#RESPONSE_CHALLENGE_PASSPHRASE](../android/service/controls/actions/ControlAction.md) 

 Value: 4

### RESPONSE_FAIL

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RESPONSE_FAIL: Int
```

Response code for the`consumer`in [ControlsProviderService.performControlAction](../android/service/controls/ControlsProviderService.md))indicating that the action has failed. 
Value is [android.service.controls.actions.ControlAction#RESPONSE_UNKNOWN](../android/service/controls/actions/ControlAction.md), [android.service.controls.actions.ControlAction#RESPONSE_OK](../android/service/controls/actions/ControlAction.md), [android.service.controls.actions.ControlAction#RESPONSE_FAIL](../android/service/controls/actions/ControlAction.md), [android.service.controls.actions.ControlAction#RESPONSE_CHALLENGE_ACK](../android/service/controls/actions/ControlAction.md), [android.service.controls.actions.ControlAction#RESPONSE_CHALLENGE_PIN](../android/service/controls/actions/ControlAction.md), or [android.service.controls.actions.ControlAction#RESPONSE_CHALLENGE_PASSPHRASE](../android/service/controls/actions/ControlAction.md) 

 Value: 2

### RESPONSE_OK

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RESPONSE_OK: Int
```

Response code for the`consumer`in [ControlsProviderService.performControlAction](../android/service/controls/ControlsProviderService.md))indicating that the action has been performed. The action may still fail later and the state may not change. 
Value is [android.service.controls.actions.ControlAction#RESPONSE_UNKNOWN](../android/service/controls/actions/ControlAction.md), [android.service.controls.actions.ControlAction#RESPONSE_OK](../android/service/controls/actions/ControlAction.md), [android.service.controls.actions.ControlAction#RESPONSE_FAIL](../android/service/controls/actions/ControlAction.md), [android.service.controls.actions.ControlAction#RESPONSE_CHALLENGE_ACK](../android/service/controls/actions/ControlAction.md), [android.service.controls.actions.ControlAction#RESPONSE_CHALLENGE_PIN](../android/service/controls/actions/ControlAction.md), or [android.service.controls.actions.ControlAction#RESPONSE_CHALLENGE_PASSPHRASE](../android/service/controls/actions/ControlAction.md) 

 Value: 1

### RESPONSE_UNKNOWN

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RESPONSE_UNKNOWN: Int
```

Value is [android.service.controls.actions.ControlAction#RESPONSE_UNKNOWN](../android/service/controls/actions/ControlAction.md), [android.service.controls.actions.ControlAction#RESPONSE_OK](../android/service/controls/actions/ControlAction.md), [android.service.controls.actions.ControlAction#RESPONSE_FAIL](../android/service/controls/actions/ControlAction.md), [android.service.controls.actions.ControlAction#RESPONSE_CHALLENGE_ACK](../android/service/controls/actions/ControlAction.md), [android.service.controls.actions.ControlAction#RESPONSE_CHALLENGE_PIN](../android/service/controls/actions/ControlAction.md), or [android.service.controls.actions.ControlAction#RESPONSE_CHALLENGE_PASSPHRASE](../android/service/controls/actions/ControlAction.md) 

 Value: 0

### TYPE_BOOLEAN

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_BOOLEAN: Int
```

The identifier of [BooleanAction](../android/service/controls/actions/BooleanAction.md). 
Value is [android.service.controls.actions.ControlAction#TYPE_ERROR](../android/service/controls/actions/ControlAction.md), [android.service.controls.actions.ControlAction#TYPE_BOOLEAN](../android/service/controls/actions/ControlAction.md), [android.service.controls.actions.ControlAction#TYPE_FLOAT](../android/service/controls/actions/ControlAction.md), [android.service.controls.actions.ControlAction#TYPE_MODE](../android/service/controls/actions/ControlAction.md), or [android.service.controls.actions.ControlAction#TYPE_COMMAND](../android/service/controls/actions/ControlAction.md) 

 Value: 1

### TYPE_COMMAND

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_COMMAND: Int
```

The identifier of [CommandAction](../android/service/controls/actions/CommandAction.md). 
Value is [android.service.controls.actions.ControlAction#TYPE_ERROR](../android/service/controls/actions/ControlAction.md), [android.service.controls.actions.ControlAction#TYPE_BOOLEAN](../android/service/controls/actions/ControlAction.md), [android.service.controls.actions.ControlAction#TYPE_FLOAT](../android/service/controls/actions/ControlAction.md), [android.service.controls.actions.ControlAction#TYPE_MODE](../android/service/controls/actions/ControlAction.md), or [android.service.controls.actions.ControlAction#TYPE_COMMAND](../android/service/controls/actions/ControlAction.md) 

 Value: 5

### TYPE_ERROR

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_ERROR: Int
```

The identifier of the action returned by [getErrorAction](../android/service/controls/actions/ControlAction.md)). 
Value is [android.service.controls.actions.ControlAction#TYPE_ERROR](../android/service/controls/actions/ControlAction.md), [android.service.controls.actions.ControlAction#TYPE_BOOLEAN](../android/service/controls/actions/ControlAction.md), [android.service.controls.actions.ControlAction#TYPE_FLOAT](../android/service/controls/actions/ControlAction.md), [android.service.controls.actions.ControlAction#TYPE_MODE](../android/service/controls/actions/ControlAction.md), or [android.service.controls.actions.ControlAction#TYPE_COMMAND](../android/service/controls/actions/ControlAction.md) 

 Value: -1

### TYPE_FLOAT

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_FLOAT: Int
```

The identifier of [FloatAction](../android/service/controls/actions/FloatAction.md). 
Value is [android.service.controls.actions.ControlAction#TYPE_ERROR](../android/service/controls/actions/ControlAction.md), [android.service.controls.actions.ControlAction#TYPE_BOOLEAN](../android/service/controls/actions/ControlAction.md), [android.service.controls.actions.ControlAction#TYPE_FLOAT](../android/service/controls/actions/ControlAction.md), [android.service.controls.actions.ControlAction#TYPE_MODE](../android/service/controls/actions/ControlAction.md), or [android.service.controls.actions.ControlAction#TYPE_COMMAND](../android/service/controls/actions/ControlAction.md) 

 Value: 2

### TYPE_MODE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_MODE: Int
```

The identifier of [ModeAction](../android/service/controls/actions/ModeAction.md). 
Value is [android.service.controls.actions.ControlAction#TYPE_ERROR](../android/service/controls/actions/ControlAction.md), [android.service.controls.actions.ControlAction#TYPE_BOOLEAN](../android/service/controls/actions/ControlAction.md), [android.service.controls.actions.ControlAction#TYPE_FLOAT](../android/service/controls/actions/ControlAction.md), [android.service.controls.actions.ControlAction#TYPE_MODE](../android/service/controls/actions/ControlAction.md), or [android.service.controls.actions.ControlAction#TYPE_COMMAND](../android/service/controls/actions/ControlAction.md) 

 Value: 4

## Public methods

### getActionType

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getActionType(): Int
```

The action type associated with this class.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.service.controls.actions.ControlAction#TYPE_ERROR](../android/service/controls/actions/ControlAction.md), [android.service.controls.actions.ControlAction#TYPE_BOOLEAN](../android/service/controls/actions/ControlAction.md), [android.service.controls.actions.ControlAction#TYPE_FLOAT](../android/service/controls/actions/ControlAction.md), [android.service.controls.actions.ControlAction#TYPE_MODE](../android/service/controls/actions/ControlAction.md), or [android.service.controls.actions.ControlAction#TYPE_COMMAND](../android/service/controls/actions/ControlAction.md) |

### getChallengeValue

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getChallengeValue(): String?
```

The challenge value used to authenticate certain actions, if available.

| Return ||
|-----------------------------------------------------------------------------------|--------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | This value may be`null`. |

### getErrorAction

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getErrorAction(): ControlAction
```

Returns a singleton [ControlAction](../android/service/controls/actions/ControlAction.md) used for indicating an error in unparceling.

| Return ||
|-----------------------------------------------------------------------------------------------------------------|-----------------------------|
| [ControlAction](../android/service/controls/actions/ControlAction.md) | This value cannot be`null`. |

### getTemplateId

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getTemplateId(): String
```

The identifier of the [ControlTemplate](../android/service/controls/templates/ControlTemplate.md) that originated this action

| Return ||
|----------------------------------------------------------------------------------|-----------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | This value cannot be`null`. |

### isValidResponse

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun isValidResponse(response: Int): Boolean
```

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `response` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is [android.service.controls.actions.ControlAction#RESPONSE_UNKNOWN](../android/service/controls/actions/ControlAction.md), [android.service.controls.actions.ControlAction#RESPONSE_OK](../android/service/controls/actions/ControlAction.md), [android.service.controls.actions.ControlAction#RESPONSE_FAIL](../android/service/controls/actions/ControlAction.md), [android.service.controls.actions.ControlAction#RESPONSE_CHALLENGE_ACK](../android/service/controls/actions/ControlAction.md), [android.service.controls.actions.ControlAction#RESPONSE_CHALLENGE_PIN](../android/service/controls/actions/ControlAction.md), or [android.service.controls.actions.ControlAction#RESPONSE_CHALLENGE_PASSPHRASE](../android/service/controls/actions/ControlAction.md) |
