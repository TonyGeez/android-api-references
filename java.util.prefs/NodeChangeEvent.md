# NodeChangeEvent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# NodeChangeEvent

```
open class NodeChangeEvent : EventObject
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [java.util.EventObject](https://developer.android.com/reference/kotlin/java/util/EventObject.html#) ||
| | ↳ | [java.util.prefs.NodeChangeEvent](https://developer.android.com/reference/kotlin/java/util/prefs/NodeChangeEvent#) |

An event emitted by a Preferences node to indicate that a child of that node has been added or removed.

Note, that although NodeChangeEvent inherits Serializable interface from java.util.EventObject, it is not intended to be Serializable. Appropriate serialization methods are implemented to throw NotSerializableException.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [NodeChangeEvent](https://developer.android.com/reference/kotlin/java/util/prefs/NodeChangeEvent#NodeChangeEvent(java.util.prefs.Preferences,%20java.util.prefs.Preferences))`(`parent:` ` [Preferences](https://developer.android.com/reference/kotlin/java/util/prefs/Preferences)!`, `child:` ` [Preferences](https://developer.android.com/reference/kotlin/java/util/prefs/Preferences)!`)` Constructs a new`NodeChangeEvent`instance. |

| Public methods ||
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Preferences](https://developer.android.com/reference/kotlin/java/util/prefs/Preferences)! | [getChild](https://developer.android.com/reference/kotlin/java/util/prefs/NodeChangeEvent#getChild())`()` Returns the node that was added or removed. |
| open [Preferences](https://developer.android.com/reference/kotlin/java/util/prefs/Preferences)! | [getParent](https://developer.android.com/reference/kotlin/java/util/prefs/NodeChangeEvent#getParent())`()` Returns the parent of the node that was added or removed. |

| Inherited functions ||
|---|---|
| From class [EventObject](https://developer.android.com/reference/kotlin/java/util/EventObject.html#) |----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getSource](https://developer.android.com/reference/kotlin/java/util/EventObject.html#getSource())`()` <br /> The object on which the Event initially occurred. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/java/util/EventObject.html#toString())`()` <br /> Returns a String representation of this EventObject. <br /> | ||

| Inherited properties ||
|---|---|
| From class [EventObject](https://developer.android.com/reference/kotlin/java/util/EventObject.html#) |-----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [source](https://developer.android.com/reference/kotlin/java/util/EventObject.html#source:kotlin.Any) <br /> The object on which the Event initially occurred. <br /> | ||

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
| `parent` | [Preferences](https://developer.android.com/reference/kotlin/java/util/prefs/Preferences)!:The parent of the node that was added or removed. |
| `child` | [Preferences](https://developer.android.com/reference/kotlin/java/util/prefs/Preferences)!:The node that was added or removed. |

## Public methods

### getChild

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getChild(): Preferences!
```

Returns the node that was added or removed.

| Return ||
|--------------------------------------------------------------------------------------------|-------------------------------------|
| [Preferences](https://developer.android.com/reference/kotlin/java/util/prefs/Preferences)! | The node that was added or removed. |

### getParent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getParent(): Preferences!
```

Returns the parent of the node that was added or removed.

| Return ||
|--------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| [Preferences](https://developer.android.com/reference/kotlin/java/util/prefs/Preferences)! | The parent Preferences node whose child was added or removed |
