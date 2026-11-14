# ControlAction

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ControlAction

Kotlin| [Java](https://developer.android.com/reference/android/service/controls/actions/ControlAction "View this page in Java") 

```
abstract class ControlAction
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.service.controls.actions.ControlAction](https://developer.android.com/reference/kotlin/android/service/controls/actions/ControlAction#) |

| Known Direct Subclasses [BooleanAction](https://developer.android.com/reference/kotlin/android/service/controls/actions/BooleanAction), [CommandAction](https://developer.android.com/reference/kotlin/android/service/controls/actions/CommandAction), [FloatAction](https://developer.android.com/reference/kotlin/android/service/controls/actions/FloatAction), [ModeAction](https://developer.android.com/reference/kotlin/android/service/controls/actions/ModeAction) |----------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [BooleanAction](https://developer.android.com/reference/kotlin/android/service/controls/actions/BooleanAction) | Action sent by user toggling a [Control](https://developer.android.com/reference/kotlin/android/service/controls/Control.html#) between checked/unchecked. | | [CommandAction](https://developer.android.com/reference/kotlin/android/service/controls/actions/CommandAction) | A simple [ControlAction](https://developer.android.com/reference/kotlin/android/service/controls/actions/ControlAction#) indicating that the user has interacted with a [Control](https://developer.android.com/reference/kotlin/android/service/controls/Control.html#) created using a [StatelessTemplate](https://developer.android.com/reference/kotlin/android/service/controls/templates/StatelessTemplate.html#). | | [FloatAction](https://developer.android.com/reference/kotlin/android/service/controls/actions/FloatAction) | Action sent by a [RangeTemplate](https://developer.android.com/reference/kotlin/android/service/controls/templates/RangeTemplate.html#), [ToggleRangeTemplate](https://developer.android.com/reference/kotlin/android/service/controls/templates/ToggleRangeTemplate.html#). | | [ModeAction](https://developer.android.com/reference/kotlin/android/service/controls/actions/ModeAction) | Action sent by the user to indicate a change of mode. | |

An abstract action indicating a user interaction with a [Control](https://developer.android.com/reference/kotlin/android/service/controls/Control.html#). In some cases, an action needs to be validated by the user, using a password, PIN or simple acknowledgment. For those cases, an optional (nullable) parameter can be passed to send the user input. This**challenge value** will be requested from the user and sent as part of a [ControlAction](https://developer.android.com/reference/kotlin/android/service/controls/actions/ControlAction#) only if the service has responded to an action with one of:

- [RESPONSE_CHALLENGE_ACK](https://developer.android.com/reference/kotlin/android/service/controls/actions/ControlAction#RESPONSE_CHALLENGE_ACK:kotlin.Int)
- [RESPONSE_CHALLENGE_PIN](https://developer.android.com/reference/kotlin/android/service/controls/actions/ControlAction#RESPONSE_CHALLENGE_PIN:kotlin.Int)
- [RESPONSE_CHALLENGE_PASSPHRASE](https://developer.android.com/reference/kotlin/android/service/controls/actions/ControlAction#RESPONSE_CHALLENGE_PASSPHRASE:kotlin.Int)

<br />

## Summary

| Constants ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RESPONSE_CHALLENGE_ACK](https://developer.android.com/reference/kotlin/android/service/controls/actions/ControlAction#RESPONSE_CHALLENGE_ACK:kotlin.Int) Response code for the`consumer`in [ControlsProviderService.performControlAction](https://developer.android.com/reference/kotlin/android/service/controls/ControlsProviderService.html#performControlAction(kotlin.String,%20android.service.controls.actions.ControlAction,%20java.util.function.Consumer))indicating that in order for the action to be performed, acknowledgment from the user is required. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RESPONSE_CHALLENGE_PASSPHRASE](https://developer.android.com/reference/kotlin/android/service/controls/actions/ControlAction#RESPONSE_CHALLENGE_PASSPHRASE:kotlin.Int) Response code for the`consumer`in [ControlsProviderService.performControlAction](https://developer.android.com/reference/kotlin/android/service/controls/ControlsProviderService.html#performControlAction(kotlin.String,%20android.service.controls.actions.ControlAction,%20java.util.function.Consumer))indicating that in order for the action to be performed, an alphanumeric passphrase is required. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RESPONSE_CHALLENGE_PIN](https://developer.android.com/reference/kotlin/android/service/controls/actions/ControlAction#RESPONSE_CHALLENGE_PIN:kotlin.Int) Response code for the`consumer`in [ControlsProviderService.performControlAction](https://developer.android.com/reference/kotlin/android/service/controls/ControlsProviderService.html#performControlAction(kotlin.String,%20android.service.controls.actions.ControlAction,%20java.util.function.Consumer))indicating that in order for the action to be performed, a PIN is required. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RESPONSE_FAIL](https://developer.android.com/reference/kotlin/android/service/controls/actions/ControlAction#RESPONSE_FAIL:kotlin.Int) Response code for the`consumer`in [ControlsProviderService.performControlAction](https://developer.android.com/reference/kotlin/android/service/controls/ControlsProviderService.html#performControlAction(kotlin.String,%20android.service.controls.actions.ControlAction,%20java.util.function.Consumer))indicating that the action has failed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RESPONSE_OK](https://developer.android.com/reference/kotlin/android/service/controls/actions/ControlAction#RESPONSE_OK:kotlin.Int) Response code for the`consumer`in [ControlsProviderService.performControlAction](https://developer.android.com/reference/kotlin/android/service/controls/ControlsProviderService.html#performControlAction(kotlin.String,%20android.service.controls.actions.ControlAction,%20java.util.function.Consumer))indicating that the action has been performed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RESPONSE_UNKNOWN](https://developer.android.com/reference/kotlin/android/service/controls/actions/ControlAction#RESPONSE_UNKNOWN:kotlin.Int) Value is [android.service.controls.actions.ControlAction#RESPONSE_UNKNOWN](https://developer.android.com/reference/kotlin/android/service/controls/actions/ControlAction#RESPONSE_UNKNOWN:kotlin.Int), [android.service.controls.actions.ControlAction#RESPONSE_OK](https://developer.android.com/reference/kotlin/android/service/controls/actions/ControlAction#RESPONSE_OK:kotlin.Int), [android.service.controls.actions.ControlAction#RESPONSE_FAIL](https://developer.android.com/reference/kotlin/android/service/controls/actions/ControlAction#RESPONSE_FAIL:kotlin.Int), [android.service.controls.actions.ControlAction#RESPONSE_CHALLENGE_ACK](https://developer.android.com/reference/kotlin/android/service/controls/actions/ControlAction#RESPONSE_CHALLENGE_ACK:kotlin.Int), [android.service.controls.actions.ControlAction#RESPONSE_CHALLENGE_PIN](https://developer.android.com/reference/kotlin/android/service/controls/actions/ControlAction#RESPONSE_CHALLENGE_PIN:kotlin.Int), or [android.service.controls.actions.ControlAction#RESPONSE_CHALLENGE_PASSPHRASE](https://developer.android.com/reference/kotlin/android/service/controls/actions/ControlAction#RESPONSE_CHALLENGE_PASSPHRASE:kotlin.Int) |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_BOOLEAN](https://developer.android.com/reference/kotlin/android/service/controls/actions/ControlAction#TYPE_BOOLEAN:kotlin.Int) The identifier of [BooleanAction](https://developer.android.com/reference/kotlin/android/service/controls/actions/BooleanAction). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_COMMAND](https://developer.android.com/reference/kotlin/android/service/controls/actions/ControlAction#TYPE_COMMAND:kotlin.Int) The identifier of [CommandAction](https://developer.android.com/reference/kotlin/android/service/controls/actions/CommandAction). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_ERROR](https://developer.android.com/reference/kotlin/android/service/controls/actions/ControlAction#TYPE_ERROR:kotlin.Int) The identifier of the action returned by [getErrorAction](https://developer.android.com/reference/kotlin/android/service/controls/actions/ControlAction#getErrorAction()). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_FLOAT](https://developer.android.com/reference/kotlin/android/service/controls/actions/ControlAction#TYPE_FLOAT:kotlin.Int) The identifier of [FloatAction](https://developer.android.com/reference/kotlin/android/service/controls/actions/FloatAction). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_MODE](https://developer.android.com/reference/kotlin/android/service/controls/actions/ControlAction#TYPE_MODE:kotlin.Int) The identifier of [ModeAction](https://developer.android.com/reference/kotlin/android/service/controls/actions/ModeAction). |

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getActionType](https://developer.android.com/reference/kotlin/android/service/controls/actions/ControlAction#getActionType())`()` The action type associated with this class. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getChallengeValue](https://developer.android.com/reference/kotlin/android/service/controls/actions/ControlAction#getChallengeValue())`()` The challenge value used to authenticate certain actions, if available. |
| openstatic [ControlAction](https://developer.android.com/reference/kotlin/android/service/controls/actions/ControlAction#) | [getErrorAction](https://developer.android.com/reference/kotlin/android/service/controls/actions/ControlAction#getErrorAction())`()` Returns a singleton [ControlAction](https://developer.android.com/reference/kotlin/android/service/controls/actions/ControlAction#) used for indicating an error in unparceling. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getTemplateId](https://developer.android.com/reference/kotlin/android/service/controls/actions/ControlAction#getTemplateId())`()` The identifier of the [ControlTemplate](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate.html#) that originated this action |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isValidResponse](https://developer.android.com/reference/kotlin/android/service/controls/actions/ControlAction#isValidResponse(kotlin.Int))`(`response:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

## Constants

### RESPONSE_CHALLENGE_ACK

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RESPONSE_CHALLENGE_ACK: Int
```

Response code for the`consumer`in [ControlsProviderService.performControlAction](https://developer.android.com/reference/kotlin/android/service/controls/ControlsProviderService.html#performControlAction(kotlin.String,%20android.service.controls.actions.ControlAction,%20java.util.function.Consumer))indicating that in order for the action to be performed, acknowledgment from the user is required. Any non-empty string returned from [getChallengeValue](https://developer.android.com/reference/kotlin/android/service/controls/actions/ControlAction#getChallengeValue())shall be treated as a positive acknowledgment. 
Value is [android.service.controls.actions.ControlAction#RESPONSE_UNKNOWN](https://developer.android.com/reference/kotlin/android/service/controls/actions/ControlAction#RESPONSE_UNKNOWN:kotlin.Int), [android.service.controls.actions.ControlAction#RESPONSE_OK](https://developer.android.com/reference/kotlin/android/service/controls/actions/ControlAction#RESPONSE_OK:kotlin.Int), [android.service.controls.actions.ControlAction#RESPONSE_FAIL](https://developer.android.com/reference/kotlin/android/service/controls/actions/ControlAction#RESPONSE_FAIL:kotlin.Int), [android.service.controls.actions.ControlAction#RESPONSE_CHALLENGE_ACK](https://developer.android.com/reference/kotlin/android/service/controls/actions/ControlAction#RESPONSE_CHALLENGE_ACK:kotlin.Int), [android.service.controls.actions.ControlAction#RESPONSE_CHALLENGE_PIN](https://developer.android.com/reference/kotlin/android/service/controls/actions/ControlAction#RESPONSE_CHALLENGE_PIN:kotlin.Int), or [android.service.controls.actions.ControlAction#RESPONSE_CHALLENGE_PASSPHRASE](https://developer.android.com/reference/kotlin/android/service/controls/actions/ControlAction#RESPONSE_CHALLENGE_PASSPHRASE:kotlin.Int) 

 Value: 3

### RESPONSE_CHALLENGE_PASSPHRASE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RESPONSE_CHALLENGE_PASSPHRASE: Int
```

Response code for the`consumer`in [ControlsProviderService.performControlAction](https://developer.android.com/reference/kotlin/android/service/controls/ControlsProviderService.html#performControlAction(kotlin.String,%20android.service.controls.actions.ControlAction,%20java.util.function.Consumer))indicating that in order for the action to be performed, an alphanumeric passphrase is required. 
Value is [android.service.controls.actions.ControlAction#RESPONSE_UNKNOWN](https://developer.android.com/reference/kotlin/android/service/controls/actions/ControlAction#RESPONSE_UNKNOWN:kotlin.Int), [android.service.controls.actions.ControlAction#RESPONSE_OK](https://developer.android.com/reference/kotlin/android/service/controls/actions/ControlAction#RESPONSE_OK:kotlin.Int), [android.service.controls.actions.ControlAction#RESPONSE_FAIL](https://developer.android.com/reference/kotlin/android/service/controls/actions/ControlAction#RESPONSE_FAIL:kotlin.Int), [android.service.controls.actions.ControlAction#RESPONSE_CHALLENGE_ACK](https://developer.android.com/reference/kotlin/android/service/controls/actions/ControlAction#RESPONSE_CHALLENGE_ACK:kotlin.Int), [android.service.controls.actions.ControlAction#RESPONSE_CHALLENGE_PIN](https://developer.android.com/reference/kotlin/android/service/controls/actions/ControlAction#RESPONSE_CHALLENGE_PIN:kotlin.Int), or [android.service.controls.actions.ControlAction#RESPONSE_CHALLENGE_PASSPHRASE](https://developer.android.com/reference/kotlin/android/service/controls/actions/ControlAction#RESPONSE_CHALLENGE_PASSPHRASE:kotlin.Int) 

 Value: 5

### RESPONSE_CHALLENGE_PIN

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RESPONSE_CHALLENGE_PIN: Int
```

Response code for the`consumer`in [ControlsProviderService.performControlAction](https://developer.android.com/reference/kotlin/android/service/controls/ControlsProviderService.html#performControlAction(kotlin.String,%20android.service.controls.actions.ControlAction,%20java.util.function.Consumer))indicating that in order for the action to be performed, a PIN is required. 
Value is [android.service.controls.actions.ControlAction#RESPONSE_UNKNOWN](https://developer.android.com/reference/kotlin/android/service/controls/actions/ControlAction#RESPONSE_UNKNOWN:kotlin.Int), [android.service.controls.actions.ControlAction#RESPONSE_OK](https://developer.android.com/reference/kotlin/android/service/controls/actions/ControlAction#RESPONSE_OK:kotlin.Int), [android.service.controls.actions.ControlAction#RESPONSE_FAIL](https://developer.android.com/reference/kotlin/android/service/controls/actions/ControlAction#RESPONSE_FAIL:kotlin.Int), [android.service.controls.actions.ControlAction#RESPONSE_CHALLENGE_ACK](https://developer.android.com/reference/kotlin/android/service/controls/actions/ControlAction#RESPONSE_CHALLENGE_ACK:kotlin.Int), [android.service.controls.actions.ControlAction#RESPONSE_CHALLENGE_PIN](https://developer.android.com/reference/kotlin/android/service/controls/actions/ControlAction#RESPONSE_CHALLENGE_PIN:kotlin.Int), or [android.service.controls.actions.ControlAction#RESPONSE_CHALLENGE_PASSPHRASE](https://developer.android.com/reference/kotlin/android/service/controls/actions/ControlAction#RESPONSE_CHALLENGE_PASSPHRASE:kotlin.Int) 

 Value: 4

### RESPONSE_FAIL

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RESPONSE_FAIL: Int
```

Response code for the`consumer`in [ControlsProviderService.performControlAction](https://developer.android.com/reference/kotlin/android/service/controls/ControlsProviderService.html#performControlAction(kotlin.String,%20android.service.controls.actions.ControlAction,%20java.util.function.Consumer))indicating that the action has failed. 
Value is [android.service.controls.actions.ControlAction#RESPONSE_UNKNOWN](https://developer.android.com/reference/kotlin/android/service/controls/actions/ControlAction#RESPONSE_UNKNOWN:kotlin.Int), [android.service.controls.actions.ControlAction#RESPONSE_OK](https://developer.android.com/reference/kotlin/android/service/controls/actions/ControlAction#RESPONSE_OK:kotlin.Int), [android.service.controls.actions.ControlAction#RESPONSE_FAIL](https://developer.android.com/reference/kotlin/android/service/controls/actions/ControlAction#RESPONSE_FAIL:kotlin.Int), [android.service.controls.actions.ControlAction#RESPONSE_CHALLENGE_ACK](https://developer.android.com/reference/kotlin/android/service/controls/actions/ControlAction#RESPONSE_CHALLENGE_ACK:kotlin.Int), [android.service.controls.actions.ControlAction#RESPONSE_CHALLENGE_PIN](https://developer.android.com/reference/kotlin/android/service/controls/actions/ControlAction#RESPONSE_CHALLENGE_PIN:kotlin.Int), or [android.service.controls.actions.ControlAction#RESPONSE_CHALLENGE_PASSPHRASE](https://developer.android.com/reference/kotlin/android/service/controls/actions/ControlAction#RESPONSE_CHALLENGE_PASSPHRASE:kotlin.Int) 

 Value: 2

### RESPONSE_OK

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RESPONSE_OK: Int
```

Response code for the`consumer`in [ControlsProviderService.performControlAction](https://developer.android.com/reference/kotlin/android/service/controls/ControlsProviderService.html#performControlAction(kotlin.String,%20android.service.controls.actions.ControlAction,%20java.util.function.Consumer))indicating that the action has been performed. The action may still fail later and the state may not change. 
Value is [android.service.controls.actions.ControlAction#RESPONSE_UNKNOWN](https://developer.android.com/reference/kotlin/android/service/controls/actions/ControlAction#RESPONSE_UNKNOWN:kotlin.Int), [android.service.controls.actions.ControlAction#RESPONSE_OK](https://developer.android.com/reference/kotlin/android/service/controls/actions/ControlAction#RESPONSE_OK:kotlin.Int), [android.service.controls.actions.ControlAction#RESPONSE_FAIL](https://developer.android.com/reference/kotlin/android/service/controls/actions/ControlAction#RESPONSE_FAIL:kotlin.Int), [android.service.controls.actions.ControlAction#RESPONSE_CHALLENGE_ACK](https://developer.android.com/reference/kotlin/android/service/controls/actions/ControlAction#RESPONSE_CHALLENGE_ACK:kotlin.Int), [android.service.controls.actions.ControlAction#RESPONSE_CHALLENGE_PIN](https://developer.android.com/reference/kotlin/android/service/controls/actions/ControlAction#RESPONSE_CHALLENGE_PIN:kotlin.Int), or [android.service.controls.actions.ControlAction#RESPONSE_CHALLENGE_PASSPHRASE](https://developer.android.com/reference/kotlin/android/service/controls/actions/ControlAction#RESPONSE_CHALLENGE_PASSPHRASE:kotlin.Int) 

 Value: 1

### RESPONSE_UNKNOWN

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RESPONSE_UNKNOWN: Int
```

Value is [android.service.controls.actions.ControlAction#RESPONSE_UNKNOWN](https://developer.android.com/reference/kotlin/android/service/controls/actions/ControlAction#RESPONSE_UNKNOWN:kotlin.Int), [android.service.controls.actions.ControlAction#RESPONSE_OK](https://developer.android.com/reference/kotlin/android/service/controls/actions/ControlAction#RESPONSE_OK:kotlin.Int), [android.service.controls.actions.ControlAction#RESPONSE_FAIL](https://developer.android.com/reference/kotlin/android/service/controls/actions/ControlAction#RESPONSE_FAIL:kotlin.Int), [android.service.controls.actions.ControlAction#RESPONSE_CHALLENGE_ACK](https://developer.android.com/reference/kotlin/android/service/controls/actions/ControlAction#RESPONSE_CHALLENGE_ACK:kotlin.Int), [android.service.controls.actions.ControlAction#RESPONSE_CHALLENGE_PIN](https://developer.android.com/reference/kotlin/android/service/controls/actions/ControlAction#RESPONSE_CHALLENGE_PIN:kotlin.Int), or [android.service.controls.actions.ControlAction#RESPONSE_CHALLENGE_PASSPHRASE](https://developer.android.com/reference/kotlin/android/service/controls/actions/ControlAction#RESPONSE_CHALLENGE_PASSPHRASE:kotlin.Int) 

 Value: 0

### TYPE_BOOLEAN

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_BOOLEAN: Int
```

The identifier of [BooleanAction](https://developer.android.com/reference/kotlin/android/service/controls/actions/BooleanAction). 
Value is [android.service.controls.actions.ControlAction#TYPE_ERROR](https://developer.android.com/reference/kotlin/android/service/controls/actions/ControlAction#TYPE_ERROR:kotlin.Int), [android.service.controls.actions.ControlAction#TYPE_BOOLEAN](https://developer.android.com/reference/kotlin/android/service/controls/actions/ControlAction#TYPE_BOOLEAN:kotlin.Int), [android.service.controls.actions.ControlAction#TYPE_FLOAT](https://developer.android.com/reference/kotlin/android/service/controls/actions/ControlAction#TYPE_FLOAT:kotlin.Int), [android.service.controls.actions.ControlAction#TYPE_MODE](https://developer.android.com/reference/kotlin/android/service/controls/actions/ControlAction#TYPE_MODE:kotlin.Int), or [android.service.controls.actions.ControlAction#TYPE_COMMAND](https://developer.android.com/reference/kotlin/android/service/controls/actions/ControlAction#TYPE_COMMAND:kotlin.Int) 

 Value: 1

### TYPE_COMMAND

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_COMMAND: Int
```

The identifier of [CommandAction](https://developer.android.com/reference/kotlin/android/service/controls/actions/CommandAction). 
Value is [android.service.controls.actions.ControlAction#TYPE_ERROR](https://developer.android.com/reference/kotlin/android/service/controls/actions/ControlAction#TYPE_ERROR:kotlin.Int), [android.service.controls.actions.ControlAction#TYPE_BOOLEAN](https://developer.android.com/reference/kotlin/android/service/controls/actions/ControlAction#TYPE_BOOLEAN:kotlin.Int), [android.service.controls.actions.ControlAction#TYPE_FLOAT](https://developer.android.com/reference/kotlin/android/service/controls/actions/ControlAction#TYPE_FLOAT:kotlin.Int), [android.service.controls.actions.ControlAction#TYPE_MODE](https://developer.android.com/reference/kotlin/android/service/controls/actions/ControlAction#TYPE_MODE:kotlin.Int), or [android.service.controls.actions.ControlAction#TYPE_COMMAND](https://developer.android.com/reference/kotlin/android/service/controls/actions/ControlAction#TYPE_COMMAND:kotlin.Int) 

 Value: 5

### TYPE_ERROR

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_ERROR: Int
```

The identifier of the action returned by [getErrorAction](https://developer.android.com/reference/kotlin/android/service/controls/actions/ControlAction#getErrorAction()). 
Value is [android.service.controls.actions.ControlAction#TYPE_ERROR](https://developer.android.com/reference/kotlin/android/service/controls/actions/ControlAction#TYPE_ERROR:kotlin.Int), [android.service.controls.actions.ControlAction#TYPE_BOOLEAN](https://developer.android.com/reference/kotlin/android/service/controls/actions/ControlAction#TYPE_BOOLEAN:kotlin.Int), [android.service.controls.actions.ControlAction#TYPE_FLOAT](https://developer.android.com/reference/kotlin/android/service/controls/actions/ControlAction#TYPE_FLOAT:kotlin.Int), [android.service.controls.actions.ControlAction#TYPE_MODE](https://developer.android.com/reference/kotlin/android/service/controls/actions/ControlAction#TYPE_MODE:kotlin.Int), or [android.service.controls.actions.ControlAction#TYPE_COMMAND](https://developer.android.com/reference/kotlin/android/service/controls/actions/ControlAction#TYPE_COMMAND:kotlin.Int) 

 Value: -1

### TYPE_FLOAT

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_FLOAT: Int
```

The identifier of [FloatAction](https://developer.android.com/reference/kotlin/android/service/controls/actions/FloatAction). 
Value is [android.service.controls.actions.ControlAction#TYPE_ERROR](https://developer.android.com/reference/kotlin/android/service/controls/actions/ControlAction#TYPE_ERROR:kotlin.Int), [android.service.controls.actions.ControlAction#TYPE_BOOLEAN](https://developer.android.com/reference/kotlin/android/service/controls/actions/ControlAction#TYPE_BOOLEAN:kotlin.Int), [android.service.controls.actions.ControlAction#TYPE_FLOAT](https://developer.android.com/reference/kotlin/android/service/controls/actions/ControlAction#TYPE_FLOAT:kotlin.Int), [android.service.controls.actions.ControlAction#TYPE_MODE](https://developer.android.com/reference/kotlin/android/service/controls/actions/ControlAction#TYPE_MODE:kotlin.Int), or [android.service.controls.actions.ControlAction#TYPE_COMMAND](https://developer.android.com/reference/kotlin/android/service/controls/actions/ControlAction#TYPE_COMMAND:kotlin.Int) 

 Value: 2

### TYPE_MODE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_MODE: Int
```

The identifier of [ModeAction](https://developer.android.com/reference/kotlin/android/service/controls/actions/ModeAction). 
Value is [android.service.controls.actions.ControlAction#TYPE_ERROR](https://developer.android.com/reference/kotlin/android/service/controls/actions/ControlAction#TYPE_ERROR:kotlin.Int), [android.service.controls.actions.ControlAction#TYPE_BOOLEAN](https://developer.android.com/reference/kotlin/android/service/controls/actions/ControlAction#TYPE_BOOLEAN:kotlin.Int), [android.service.controls.actions.ControlAction#TYPE_FLOAT](https://developer.android.com/reference/kotlin/android/service/controls/actions/ControlAction#TYPE_FLOAT:kotlin.Int), [android.service.controls.actions.ControlAction#TYPE_MODE](https://developer.android.com/reference/kotlin/android/service/controls/actions/ControlAction#TYPE_MODE:kotlin.Int), or [android.service.controls.actions.ControlAction#TYPE_COMMAND](https://developer.android.com/reference/kotlin/android/service/controls/actions/ControlAction#TYPE_COMMAND:kotlin.Int) 

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
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.service.controls.actions.ControlAction#TYPE_ERROR](https://developer.android.com/reference/kotlin/android/service/controls/actions/ControlAction#TYPE_ERROR:kotlin.Int), [android.service.controls.actions.ControlAction#TYPE_BOOLEAN](https://developer.android.com/reference/kotlin/android/service/controls/actions/ControlAction#TYPE_BOOLEAN:kotlin.Int), [android.service.controls.actions.ControlAction#TYPE_FLOAT](https://developer.android.com/reference/kotlin/android/service/controls/actions/ControlAction#TYPE_FLOAT:kotlin.Int), [android.service.controls.actions.ControlAction#TYPE_MODE](https://developer.android.com/reference/kotlin/android/service/controls/actions/ControlAction#TYPE_MODE:kotlin.Int), or [android.service.controls.actions.ControlAction#TYPE_COMMAND](https://developer.android.com/reference/kotlin/android/service/controls/actions/ControlAction#TYPE_COMMAND:kotlin.Int) |

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

Returns a singleton [ControlAction](https://developer.android.com/reference/kotlin/android/service/controls/actions/ControlAction#) used for indicating an error in unparceling.

| Return ||
|-----------------------------------------------------------------------------------------------------------------|-----------------------------|
| [ControlAction](https://developer.android.com/reference/kotlin/android/service/controls/actions/ControlAction#) | This value cannot be`null`. |

### getTemplateId

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getTemplateId(): String
```

The identifier of the [ControlTemplate](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate.html#) that originated this action

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
| `response` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is [android.service.controls.actions.ControlAction#RESPONSE_UNKNOWN](https://developer.android.com/reference/kotlin/android/service/controls/actions/ControlAction#RESPONSE_UNKNOWN:kotlin.Int), [android.service.controls.actions.ControlAction#RESPONSE_OK](https://developer.android.com/reference/kotlin/android/service/controls/actions/ControlAction#RESPONSE_OK:kotlin.Int), [android.service.controls.actions.ControlAction#RESPONSE_FAIL](https://developer.android.com/reference/kotlin/android/service/controls/actions/ControlAction#RESPONSE_FAIL:kotlin.Int), [android.service.controls.actions.ControlAction#RESPONSE_CHALLENGE_ACK](https://developer.android.com/reference/kotlin/android/service/controls/actions/ControlAction#RESPONSE_CHALLENGE_ACK:kotlin.Int), [android.service.controls.actions.ControlAction#RESPONSE_CHALLENGE_PIN](https://developer.android.com/reference/kotlin/android/service/controls/actions/ControlAction#RESPONSE_CHALLENGE_PIN:kotlin.Int), or [android.service.controls.actions.ControlAction#RESPONSE_CHALLENGE_PASSPHRASE](https://developer.android.com/reference/kotlin/android/service/controls/actions/ControlAction#RESPONSE_CHALLENGE_PASSPHRASE:kotlin.Int) |
