# PreferenceChangeEvent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PreferenceChangeEvent

```
open class PreferenceChangeEvent : EventObject
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [java.util.EventObject](../java/util/EventObject.md) ||
| | ↳ | [java.util.prefs.PreferenceChangeEvent](../java/util/prefs/PreferenceChangeEvent.md) |

An event emitted by a Preferences node to indicate that a preference has been added, removed or has had its value changed.

Note, that although PreferenceChangeEvent inherits Serializable interface from EventObject, it is not intended to be Serializable. Appropriate serialization methods are implemented to throw NotSerializableException.

## Summary

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [PreferenceChangeEvent](../java/util/prefs/PreferenceChangeEvent.md))`(`node:` ` [Preferences](../java/util/prefs/Preferences.md)!`, `key:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `newValue:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a new`PreferenceChangeEvent`instance. |

| Public methods ||
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getKey](../java/util/prefs/PreferenceChangeEvent.md))`()` Returns the key of the preference that was changed. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getNewValue](../java/util/prefs/PreferenceChangeEvent.md))`()` Returns the new value for the preference. |
| open [Preferences](../java/util/prefs/Preferences.md)! | [getNode](../java/util/prefs/PreferenceChangeEvent.md))`()` Returns the preference node that emitted the event. |
| --- | --- |

| Inherited functions ||
|---|---|
| From class [EventObject](../java/util/EventObject.md) |----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getSource](../java/util/EventObject.md))`()` <br /> The object on which the Event initially occurred. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../java/util/EventObject.md))`()` <br /> Returns a String representation of this EventObject. <br /> | ||

| Inherited properties ||
|---|---|
| From class [EventObject](../java/util/EventObject.md) |-----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [source](../java/util/EventObject.md) <br /> The object on which the Event initially occurred. <br /> | ||

## Public constructors

### PreferenceChangeEvent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
PreferenceChangeEvent(
    node: Preferences!, 
    key: String!, 
    newValue: String!)
```

Constructs a new`PreferenceChangeEvent`instance.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `node` | [Preferences](../java/util/prefs/Preferences.md)!:The Preferences node that emitted the event. |
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The key of the preference that was changed. |
| `newValue` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The new value of the preference, or null if the preference is being removed. |
| --- | --- |

## Public methods

### getKey

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getKey(): String!
```

Returns the key of the preference that was changed.

| Return ||
|-----------------------------------------------------------------------------------|---------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | The key of the preference that was changed. |

### getNewValue

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getNewValue(): String!
```

Returns the new value for the preference.

| Return ||
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | The new value for the preference, or null if the preference was removed. |

### getNode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getNode(): Preferences!
```

Returns the preference node that emitted the event.

| Return ||
|--------------------------------------------------------------------------------------------|---------------------------------------------|
| [Preferences](../java/util/prefs/Preferences.md)! | The preference node that emitted the event. |
