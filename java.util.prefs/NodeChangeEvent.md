# NodeChangeEvent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# NodeChangeEvent

```
open class NodeChangeEvent : EventObject
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [java.util.EventObject](../java/util/EventObject.md) ||
| | ↳ | [java.util.prefs.NodeChangeEvent](../java/util/prefs/NodeChangeEvent.md) |

An event emitted by a Preferences node to indicate that a child of that node has been added or removed.

Note, that although NodeChangeEvent inherits Serializable interface from java.util.EventObject, it is not intended to be Serializable. Appropriate serialization methods are implemented to throw NotSerializableException.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [NodeChangeEvent](../java/util/prefs/NodeChangeEvent.md))`(`parent:` ` [Preferences](../java/util/prefs/Preferences.md)!`, `child:` ` [Preferences](../java/util/prefs/Preferences.md)!`)` Constructs a new`NodeChangeEvent`instance. |

| Public methods ||
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Preferences](../java/util/prefs/Preferences.md)! | [getChild](../java/util/prefs/NodeChangeEvent.md))`()` Returns the node that was added or removed. |
| open [Preferences](../java/util/prefs/Preferences.md)! | [getParent](../java/util/prefs/NodeChangeEvent.md))`()` Returns the parent of the node that was added or removed. |

| Inherited functions ||
|---|---|
| From class [EventObject](../java/util/EventObject.md) |----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getSource](../java/util/EventObject.md))`()` <br /> The object on which the Event initially occurred. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../java/util/EventObject.md))`()` <br /> Returns a String representation of this EventObject. <br /> | ||

| Inherited properties ||
|---|---|
| From class [EventObject](../java/util/EventObject.md) |-----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [source](../java/util/EventObject.md) <br /> The object on which the Event initially occurred. <br /> | ||

## Public constructors

### NodeChangeEvent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
NodeChangeEvent(
    parent: Preferences!, 
    child: Preferences!)
```

Constructs a new`NodeChangeEvent`instance.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------|
| `parent` | [Preferences](../java/util/prefs/Preferences.md)!:The parent of the node that was added or removed. |
| `child` | [Preferences](../java/util/prefs/Preferences.md)!:The node that was added or removed. |

## Public methods

### getChild

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getChild(): Preferences!
```

Returns the node that was added or removed.

| Return ||
|--------------------------------------------------------------------------------------------|-------------------------------------|
| [Preferences](../java/util/prefs/Preferences.md)! | The node that was added or removed. |

### getParent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getParent(): Preferences!
```

Returns the parent of the node that was added or removed.

| Return ||
|--------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| [Preferences](../java/util/prefs/Preferences.md)! | The parent Preferences node whose child was added or removed |
