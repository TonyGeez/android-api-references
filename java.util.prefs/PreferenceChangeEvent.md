# PreferenceChangeEvent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PreferenceChangeEvent

```
open class PreferenceChangeEvent : EventObject
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| ↳ | [java.util.EventObject](https://developer.android.com/reference/kotlin/java/util/EventObject.html#) ||
| | ↳ | [java.util.prefs.PreferenceChangeEvent](https://developer.android.com/reference/kotlin/java/util/prefs/PreferenceChangeEvent#) |

An event emitted by a Preferences node to indicate that a preference has been added, removed or has had its value changed.

Note, that although PreferenceChangeEvent inherits Serializable interface from EventObject, it is not intended to be Serializable. Appropriate serialization methods are implemented to throw NotSerializableException.

## Summary

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [PreferenceChangeEvent](https://developer.android.com/reference/kotlin/java/util/prefs/PreferenceChangeEvent#PreferenceChangeEvent(java.util.prefs.Preferences,%20kotlin.String,%20kotlin.String))`(`node:` ` [Preferences](https://developer.android.com/reference/kotlin/java/util/prefs/Preferences)!`, `key:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `newValue:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a new`PreferenceChangeEvent`instance. |

| Public methods ||
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getKey](https://developer.android.com/reference/kotlin/java/util/prefs/PreferenceChangeEvent#getKey())`()` Returns the key of the preference that was changed. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getNewValue](https://developer.android.com/reference/kotlin/java/util/prefs/PreferenceChangeEvent#getNewValue())`()` Returns the new value for the preference. |
| open [Preferences](https://developer.android.com/reference/kotlin/java/util/prefs/Preferences)! | [getNode](https://developer.android.com/reference/kotlin/java/util/prefs/PreferenceChangeEvent#getNode())`()` Returns the preference node that emitted the event. |

| Inherited functions ||
|---|---|
| From class [EventObject](https://developer.android.com/reference/kotlin/java/util/EventObject.html#) |----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getSource](https://developer.android.com/reference/kotlin/java/util/EventObject.html#getSource())`()` <br /> The object on which the Event initially occurred. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/java/util/EventObject.html#toString())`()` <br /> Returns a String representation of this EventObject. <br /> | ||

| Inherited properties ||
|---|---|
| From class [EventObject](https://developer.android.com/reference/kotlin/java/util/EventObject.html#) |-----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [source](https://developer.android.com/reference/kotlin/java/util/EventObject.html#source:kotlin.Any) <br /> The object on which the Event initially occurred. <br /> | ||

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
| `node` | [Preferences](https://developer.android.com/reference/kotlin/java/util/prefs/Preferences)!:The Preferences node that emitted the event. |
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The key of the preference that was changed. |
| `newValue` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The new value of the preference, or null if the preference is being removed. |

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
| [Preferences](https://developer.android.com/reference/kotlin/java/util/prefs/Preferences)! | The preference node that emitted the event. |
