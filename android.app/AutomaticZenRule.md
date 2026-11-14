# AutomaticZenRule

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AutomaticZenRule

Kotlin| [Java](../android/app/AutomaticZenRule.md) 
| --- | --- |

```
class AutomaticZenRule : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.app.AutomaticZenRule](../android/app/AutomaticZenRule.md) |

Rule instance information for a zen (aka DND or Attention Management) mode.

## Summary

| Nested classes ||
|---|-------------------------------------------------------------------------------------------------------|
| | [Builder](../android/app/AutomaticZenRule.Builder.md) <br /> |

| Constants ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_BEDTIME](../android/app/AutomaticZenRule.md) The type for rules triggered by bedtime/sleeping, like time of day, or snore detection. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_DRIVING](../android/app/AutomaticZenRule.md) The type for rules triggered by driving detection, like Bluetooth connections or vehicle sounds. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_IMMERSIVE](../android/app/AutomaticZenRule.md) The type for rules triggered by the user entering an immersive activity, like opening an app using [WindowInsetsController.hide(int)](../android/view/WindowInsetsController.md)). |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_MANAGED](../android/app/AutomaticZenRule.md) The type for rules created and managed by a device owner. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_OTHER](../android/app/AutomaticZenRule.md) Rule is of a known type, but not one of the specific types. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_SCHEDULE_CALENDAR](../android/app/AutomaticZenRule.md) The type for rules triggered by calendar events. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_SCHEDULE_TIME](../android/app/AutomaticZenRule.md) The type for rules triggered according to a time-based schedule. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_THEATER](../android/app/AutomaticZenRule.md) The type for rules that have a [ZenPolicy](../android/service/notification/ZenPolicy.md) that implies that the device should not make sound and potentially hide some visual effects; may be triggered when entering a location where silence is requested, like a theater. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_UNKNOWN](../android/app/AutomaticZenRule.md) Rule is of an unknown type. |
| --- | --- |

| Inherited constants ||
|---|---|
| From class [Parcelable](../android/os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android/os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android/os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [AutomaticZenRule](../android/app/AutomaticZenRule.md))`(`source:` ` [Parcel](../android/os/Parcel.md)!`)` <br /> |
| [AutomaticZenRule](../android/app/AutomaticZenRule.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `owner:` ` [ComponentName](../android/content/ComponentName.md)?`, `configurationActivity:` ` [ComponentName](../android/content/ComponentName.md)?`, `conditionId:` ` [Uri](../android/net/Uri.md)`, `policy:` ` [ZenPolicy](../android/service/notification/ZenPolicy.md)?`, `interruptionFilter:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `enabled:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Creates an automatic zen rule. |
| [AutomaticZenRule](../android/app/AutomaticZenRule.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `owner:` ` [ComponentName](../android/content/ComponentName.md)!`, `conditionId:` ` [Uri](../android/net/Uri.md)!`, `interruptionFilter:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `enabled:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Creates an automatic zen rule. |

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](../android/app/AutomaticZenRule.md))`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](../android/app/AutomaticZenRule.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Indicates whether some other object is "equal to" this one. |
| [Uri](../android/net/Uri.md)! | [getConditionId](../android/app/AutomaticZenRule.md))`()` Returns the representation of the state that causes this rule to become active. |
| --- | --- |
| [ComponentName](../android/content/ComponentName.md)? | [getConfigurationActivity](../android/app/AutomaticZenRule.md))`()` Returns the [ComponentName](../android/content/ComponentName.md) of the activity that shows configuration options for this rule. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getCreationTime](../android/app/AutomaticZenRule.md))`()` Returns the time this rule was created, represented as milliseconds since the epoch. |
| [ZenDeviceEffects](../android/service/notification/ZenDeviceEffects.md)? | [getDeviceEffects](../android/app/AutomaticZenRule.md))`()` Gets the [ZenDeviceEffects](../android/service/notification/ZenDeviceEffects.md) of this rule. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getIconResId](../android/app/AutomaticZenRule.md))`()` Gets the resource id of the drawable icon for this rule. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getInterruptionFilter](../android/app/AutomaticZenRule.md))`()` Returns the interruption filter that is applied when this rule is active. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getName](../android/app/AutomaticZenRule.md))`()` Returns the name of this rule. |
| --- | --- |
| [ComponentName](../android/content/ComponentName.md)! | [getOwner](../android/app/AutomaticZenRule.md))`()` Returns the [ComponentName](../android/content/ComponentName.md) of the condition provider service that owns this rule. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getTriggerDescription](../android/app/AutomaticZenRule.md))`()` Gets the user visible description of when this rule is active (see [Condition.STATE_TRUE](../android/service/notification/Condition.md)). |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getType](../android/app/AutomaticZenRule.md))`()` Gets the type of the rule. |
| --- | --- |
| [ZenPolicy](../android/service/notification/ZenPolicy.md)? | [getZenPolicy](../android/app/AutomaticZenRule.md))`()` Gets the [ZenPolicy](../android/service/notification/ZenPolicy.md) applied if [getInterruptionFilter()](../android/app/AutomaticZenRule.md))is [NotificationManager.INTERRUPTION_FILTER_PRIORITY](../android/app/NotificationManager.md). |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](../android/app/AutomaticZenRule.md))`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEnabled](../android/app/AutomaticZenRule.md))`()` Returns whether this rule is enabled. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isManualInvocationAllowed](../android/app/AutomaticZenRule.md))`()` Gets whether this rule can be manually activated by the user even when the triggering condition for the rule is not met. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setConditionId](../android/app/AutomaticZenRule.md))`(`conditionId:` ` [Uri](../android/net/Uri.md)!`)` Sets the representation of the state that causes this rule to become active. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setConfigurationActivity](../android/app/AutomaticZenRule.md))`(`componentName:` ` [ComponentName](../android/content/ComponentName.md)?`)` Sets the configuration activity - an activity that handles [NotificationManager.ACTION_AUTOMATIC_ZEN_RULE](../android/app/NotificationManager.md) that shows the user more information about this rule and/or allows them to configure it. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDeviceEffects](../android/app/AutomaticZenRule.md))`(`deviceEffects:` ` [ZenDeviceEffects](../android/service/notification/ZenDeviceEffects.md)?`)` Sets the [ZenDeviceEffects](../android/service/notification/ZenDeviceEffects.md) associated to this rule. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setEnabled](../android/app/AutomaticZenRule.md))`(`enabled:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Enables this rule. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setInterruptionFilter](../android/app/AutomaticZenRule.md))`(`interruptionFilter:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the interruption filter that is applied when this rule is active. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setName](../android/app/AutomaticZenRule.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Sets the name of this rule. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setZenPolicy](../android/app/AutomaticZenRule.md))`(`zenPolicy:` ` [ZenPolicy](../android/service/notification/ZenPolicy.md)?`)` Sets the [ZenPolicy](../android/service/notification/ZenPolicy.md) applied if [getInterruptionFilter()](../android/app/AutomaticZenRule.md))is [NotificationManager.INTERRUPTION_FILTER_PRIORITY](../android/app/NotificationManager.md). |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../android/app/AutomaticZenRule.md))`()` <br /> |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](../android/app/AutomaticZenRule.md))`(`dest:` ` [Parcel](../android/os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Properties ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [AutomaticZenRule](../android/app/AutomaticZenRule.md)!\> | [CREATOR](../android/app/AutomaticZenRule.md) <br /> |

## Constants

### TYPE_BEDTIME

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_BEDTIME: Int
```

The type for rules triggered by bedtime/sleeping, like time of day, or snore detection.

Only the 'Wellbeing' app may own rules of this type. 

 Value: 3

### TYPE_DRIVING

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_DRIVING: Int
```

The type for rules triggered by driving detection, like Bluetooth connections or vehicle sounds. 

 Value: 4

### TYPE_IMMERSIVE

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_IMMERSIVE: Int
```

The type for rules triggered by the user entering an immersive activity, like opening an app using [WindowInsetsController.hide(int)](../android/view/WindowInsetsController.md)). 

 Value: 5

### TYPE_MANAGED

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_MANAGED: Int
```

The type for rules created and managed by a device owner. These rules may not be fully editable by the device user.

Only a 'Device Owner' app may own rules of this type. 

 Value: 7

### TYPE_OTHER

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_OTHER: Int
```

Rule is of a known type, but not one of the specific types. 

 Value: 0

### TYPE_SCHEDULE_CALENDAR

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_SCHEDULE_CALENDAR: Int
```

The type for rules triggered by calendar events. 

 Value: 2

### TYPE_SCHEDULE_TIME

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_SCHEDULE_TIME: Int
```

The type for rules triggered according to a time-based schedule. 

 Value: 1

### TYPE_THEATER

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_THEATER: Int
```

The type for rules that have a [ZenPolicy](../android/service/notification/ZenPolicy.md) that implies that the device should not make sound and potentially hide some visual effects; may be triggered when entering a location where silence is requested, like a theater. 

 Value: 6

### TYPE_UNKNOWN

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_UNKNOWN: Int
```

Rule is of an unknown type. This is the default value if not provided by the owning app, and the value returned if the true type was added in an API level higher than the calling app's targetSdk. 

 Value: -1

## Public constructors

### AutomaticZenRule

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
AutomaticZenRule(source: Parcel!)
```  

### AutomaticZenRule

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
AutomaticZenRule(
    name: String, 
    owner: ComponentName?, 
    configurationActivity: ComponentName?, 
    conditionId: Uri, 
    policy: ZenPolicy?, 
    interruptionFilter: Int, 
    enabled: Boolean)
```

Creates an automatic zen rule.

Note: Prefer [AutomaticZenRule.Builder](../android/app/AutomaticZenRule.Builder.md) to construct an [AutomaticZenRule](../android/app/AutomaticZenRule.md).

| Parameters ||
|-------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The name of the rule. This value cannot be`null`. |
| `owner` | [ComponentName](../android/content/ComponentName.md)?:The Condition Provider service that owns this rule. This can be null if you're using [NotificationManager.setAutomaticZenRuleState(String, Condition)](../android/app/NotificationManager.md))instead of [android.service.notification.ConditionProviderService](../android/service/notification/ConditionProviderService.md). |
| `configurationActivity` | [ComponentName](../android/content/ComponentName.md)?:An activity that handles [NotificationManager.ACTION_AUTOMATIC_ZEN_RULE](../android/app/NotificationManager.md) that shows the user more information about this rule and/or allows them to configure it. This is required if you are not using a [android.service.notification.ConditionProviderService](../android/service/notification/ConditionProviderService.md). If you are, it overrides the information specified in your manifest. This value may be`null`. |
| --- | --- |
| `conditionId` | [Uri](../android/net/Uri.md):A representation of the state that should cause your app to apply the given interruption filter. This value cannot be`null`. |
| `interruptionFilter` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The interruption filter defines which notifications are allowed to interrupt the user (e.g. via sound \& vibration) while this rule is active. |
| `policy` | [ZenPolicy](../android/service/notification/ZenPolicy.md)?:The policy defines which notifications are allowed to interrupt the user while this rule is active. This overrides the global policy while this rule is action ([Condition.STATE_TRUE](../android/service/notification/Condition.md)). This value may be`null`. |
| --- | --- |
| `enabled` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):Whether the rule is enabled. |

### AutomaticZenRule

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
AutomaticZenRule(
    name: String!, 
    owner: ComponentName!, 
    conditionId: Uri!, 
    interruptionFilter: Int, 
    enabled: Boolean)
```

**Deprecated:** *Use [AutomaticZenRule.Builder](../android/app/AutomaticZenRule.Builder.md) to construct an [AutomaticZenRule](../android/app/AutomaticZenRule.md).*

Creates an automatic zen rule.

| Parameters ||
|----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The name of the rule. |
| `owner` | [ComponentName](../android/content/ComponentName.md)!:The Condition Provider service that owns this rule. |
| `interruptionFilter` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The interruption filter defines which notifications are allowed to interrupt the user (e.g. via sound \& vibration) while this rule is active. |
| --- | --- |
| `enabled` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):Whether the rule is enabled. |

## Public methods

### describeContents

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) |

### equals

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

Indicates whether some other object is "equal to" this one.

The`equals`method implements an equivalence relation on non-null object references:

- It is*reflexive* : for any non-null reference value`x`,`x.equals(x)`should return`true`.
- It is*symmetric* : for any non-null reference values`x`and`y`,`x.equals(y)`should return`true`if and only if`y.equals(x)`returns`true`.
- It is*transitive* : for any non-null reference values`x`,`y`, and`z`, if`x.equals(y)`returns`true`and`y.equals(z)`returns`true`, then`x.equals(z)`should return`true`.
- It is*consistent* : for any non-null reference values`x`and`y`, multiple invocations of`x.equals(y)`consistently return`true`or consistently return`false`, provided no information used in`equals`comparisons on the objects is modified.
- For any non-null reference value`x`,`x.equals(null)`should return`false`.

An equivalence relation partitions the elements it operates on into*equivalence classes*; all the members of an equivalence class are equal to each other. Members of an equivalence class are substitutable for each other, at least for some purposes.

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |
| `o` | This value may be`null`. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

### getConditionId

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getConditionId(): Uri!
```

Returns the representation of the state that causes this rule to become active. 

### getConfigurationActivity

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getConfigurationActivity(): ComponentName?
```

Returns the [ComponentName](../android/content/ComponentName.md) of the activity that shows configuration options for this rule.

| Return ||
|------------------------------------------------------------------------------------------------------|--------------------------|
| [ComponentName](../android/content/ComponentName.md)? | This value may be`null`. |

### getCreationTime

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCreationTime(): Long
```

Returns the time this rule was created, represented as milliseconds since the epoch. 

### getDeviceEffects

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDeviceEffects(): ZenDeviceEffects?
```

Gets the [ZenDeviceEffects](../android/service/notification/ZenDeviceEffects.md) of this rule.

| Return ||
|-------------------------------------------------------------------------------------------------------------------------|--------------------------|
| [ZenDeviceEffects](../android/service/notification/ZenDeviceEffects.md)? | This value may be`null`. |

### getIconResId

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getIconResId(): Int
```

Gets the resource id of the drawable icon for this rule. 

### getInterruptionFilter

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getInterruptionFilter(): Int
```

Returns the interruption filter that is applied when this rule is active. 

### getName

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getName(): String!
```

Returns the name of this rule. 

### getOwner

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getOwner(): ComponentName!
```

Returns the [ComponentName](../android/content/ComponentName.md) of the condition provider service that owns this rule. 

### getTriggerDescription

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTriggerDescription(): String?
```

Gets the user visible description of when this rule is active (see [Condition.STATE_TRUE](../android/service/notification/Condition.md)).

| Return ||
|-----------------------------------------------------------------------------------|--------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | This value may be`null`. |

### getType

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getType(): Int
```

Gets the type of the rule.

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.app.AutomaticZenRule#TYPE_UNKNOWN](../android/app/AutomaticZenRule.md), [android.app.AutomaticZenRule#TYPE_OTHER](../android/app/AutomaticZenRule.md), [android.app.AutomaticZenRule#TYPE_SCHEDULE_TIME](../android/app/AutomaticZenRule.md), [android.app.AutomaticZenRule#TYPE_SCHEDULE_CALENDAR](../android/app/AutomaticZenRule.md), [android.app.AutomaticZenRule#TYPE_BEDTIME](../android/app/AutomaticZenRule.md), [android.app.AutomaticZenRule#TYPE_DRIVING](../android/app/AutomaticZenRule.md), [android.app.AutomaticZenRule#TYPE_IMMERSIVE](../android/app/AutomaticZenRule.md), [android.app.AutomaticZenRule#TYPE_THEATER](../android/app/AutomaticZenRule.md), or [android.app.AutomaticZenRule#TYPE_MANAGED](../android/app/AutomaticZenRule.md) |

### getZenPolicy

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getZenPolicy(): ZenPolicy?
```

Gets the [ZenPolicy](../android/service/notification/ZenPolicy.md) applied if [getInterruptionFilter()](../android/app/AutomaticZenRule.md))is [NotificationManager.INTERRUPTION_FILTER_PRIORITY](../android/app/NotificationManager.md).

| Return ||
|-----------------------------------------------------------------------------------------------------------|--------------------------|
| [ZenPolicy](../android/service/notification/ZenPolicy.md)? | This value may be`null`. |

### hashCode

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### isEnabled

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isEnabled(): Boolean
```

Returns whether this rule is enabled. 

### isManualInvocationAllowed

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isManualInvocationAllowed(): Boolean
```

Gets whether this rule can be manually activated by the user even when the triggering condition for the rule is not met. 

### setConditionId

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setConditionId(conditionId: Uri!): Unit
```

Sets the representation of the state that causes this rule to become active. 

### setConfigurationActivity

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setConfigurationActivity(componentName: ComponentName?): Unit
```

Sets the configuration activity - an activity that handles [NotificationManager.ACTION_AUTOMATIC_ZEN_RULE](../android/app/NotificationManager.md) that shows the user more information about this rule and/or allows them to configure it. This is required to be non-null for rules that are not backed by a [android.service.notification.ConditionProviderService](../android/service/notification/ConditionProviderService.md).

This is exclusive with the`owner`supplied in the constructor; rules where a configuration activity is set will not use the [android.service.notification.ConditionProviderService](../android/service/notification/ConditionProviderService.md) supplied there to determine whether the rule should be active.

| Parameters ||
|-----------------|-------------------------------------------------------------------------------------------------------------------------------|
| `componentName` | [ComponentName](../android/content/ComponentName.md)?:This value may be`null`. |

### setDeviceEffects

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setDeviceEffects(deviceEffects: ZenDeviceEffects?): Unit
```

Sets the [ZenDeviceEffects](../android/service/notification/ZenDeviceEffects.md) associated to this rule. Device effects specify changes to the device behavior that should apply while the rule is active, but are not directly related to suppressing notifications (for example: disabling always-on display).

When updating an existing rule via [NotificationManager.updateAutomaticZenRule](../android/app/NotificationManager.md)), a`null`value here means the previous set of effects is retained.

| Parameters ||
|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| `deviceEffects` | [ZenDeviceEffects](../android/service/notification/ZenDeviceEffects.md)?:This value may be`null`. |

### setEnabled

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setEnabled(enabled: Boolean): Unit
```

Enables this rule. 

### setInterruptionFilter

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setInterruptionFilter(interruptionFilter: Int): Unit
```

Sets the interruption filter that is applied when this rule is active.

- When [NotificationManager.INTERRUPTION_FILTER_PRIORITY](../android/app/NotificationManager.md), the rule will use the [ZenPolicy](../android/service/notification/ZenPolicy.md) supplied to [setZenPolicy](../android/app/AutomaticZenRule.md))(or a default one).
- When [NotificationManager.INTERRUPTION_FILTER_ALARMS](../android/app/NotificationManager.md) or [NotificationManager.INTERRUPTION_FILTER_NONE](../android/app/NotificationManager.md), the rule will use a fixed [ZenPolicy](../android/service/notification/ZenPolicy.md) matching the filter.
- When [NotificationManager.INTERRUPTION_FILTER_ALL](../android/app/NotificationManager.md), the rule will not block notifications, but can still have [ZenDeviceEffects](../android/service/notification/ZenDeviceEffects.md).

<br />

| Parameters ||
|----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `interruptionFilter` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The do not disturb mode to enter when this rule is active. Value is [android.app.NotificationManager#INTERRUPTION_FILTER_NONE](../android/app/NotificationManager.md), [android.app.NotificationManager#INTERRUPTION_FILTER_PRIORITY](../android/app/NotificationManager.md), [android.app.NotificationManager#INTERRUPTION_FILTER_ALARMS](../android/app/NotificationManager.md), [android.app.NotificationManager#INTERRUPTION_FILTER_ALL](../android/app/NotificationManager.md), or [android.app.NotificationManager#INTERRUPTION_FILTER_UNKNOWN](../android/app/NotificationManager.md) |

### setName

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setName(name: String!): Unit
```

Sets the name of this rule. 

### setZenPolicy

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setZenPolicy(zenPolicy: ZenPolicy?): Unit
```

Sets the [ZenPolicy](../android/service/notification/ZenPolicy.md) applied if [getInterruptionFilter()](../android/app/AutomaticZenRule.md))is [NotificationManager.INTERRUPTION_FILTER_PRIORITY](../android/app/NotificationManager.md).

When updating an existing rule via [NotificationManager.updateAutomaticZenRule](../android/app/NotificationManager.md)), a`null`value here means the previous policy is retained.

| Parameters ||
|-------------|------------------------------------------------------------------------------------------------------------------------------------|
| `zenPolicy` | [ZenPolicy](../android/service/notification/ZenPolicy.md)?:This value may be`null`. |

### toString

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

### writeToParcel

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Parcel](../android/os/Parcel.md):The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<AutomaticZenRule!>
```
