# EventObject

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# EventObject

```
open class EventObject : Serializable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.util.EventObject](../java/util/EventObject.md) |

| Known Direct Subclasses [ConnectionEvent](../javax/sql/ConnectionEvent.md), [HandshakeCompletedEvent](../javax/net/ssl/HandshakeCompletedEvent.md), [NodeChangeEvent](../java/util/prefs/NodeChangeEvent.md), [PreferenceChangeEvent](../java/util/prefs/PreferenceChangeEvent.md), [PropertyChangeEvent](../java/beans/PropertyChangeEvent.md), [RowSetEvent](../javax/sql/RowSetEvent.md), [SSLSessionBindingEvent](../javax/net/ssl/SSLSessionBindingEvent.md), [StatementEvent](../javax/sql/StatementEvent.md) |-----------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------| | [ConnectionEvent](../javax/sql/ConnectionEvent.md) | An`Event`object that provides information about the source of a connection-related event. | | [HandshakeCompletedEvent](../javax/net/ssl/HandshakeCompletedEvent.md) | This event indicates that an SSL handshake completed on a given SSL connection. | | [NodeChangeEvent](../java/util/prefs/NodeChangeEvent.md) | An event emitted by a Preferences node to indicate that a child of that node has been added or removed. | | [PreferenceChangeEvent](../java/util/prefs/PreferenceChangeEvent.md) | An event emitted by a Preferences node to indicate that a preference has been added, removed or has had its value changed. | | [PropertyChangeEvent](../java/beans/PropertyChangeEvent.md) | A "PropertyChange" event gets delivered whenever a bean changes a "bound" or "constrained" property. | | [RowSetEvent](../javax/sql/RowSetEvent.md) | An`Event`object generated when an event occurs to a`RowSet`object. | | [SSLSessionBindingEvent](../javax/net/ssl/SSLSessionBindingEvent.md) | This event is propagated to a SSLSessionBindingListener. | | [StatementEvent](../javax/sql/StatementEvent.md) | A`StatementEvent`is sent to all`StatementEventListener`s which were registered with a`PooledConnection`. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [IndexedPropertyChangeEvent](../java/beans/IndexedPropertyChangeEvent.md) |--------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------| | [IndexedPropertyChangeEvent](../java/beans/IndexedPropertyChangeEvent.md) | An "IndexedPropertyChange" event gets delivered whenever a component that conforms to the JavaBeans™ specification (a "bean") changes a bound indexed property. | |
| --- | --- | --- | --- | --- | --- | --- |

The root class from which all event state objects shall be derived.

All Events are constructed with a reference to the object, the "source", that is logically deemed to be the object upon which the Event in question initially occurred upon.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [EventObject](../java/util/EventObject.md))`(`source:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Constructs a prototypical Event. |

| Public methods ||
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getSource](../java/util/EventObject.md))`()` The object on which the Event initially occurred. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../java/util/EventObject.md))`()` Returns a String representation of this EventObject. |

| Properties ||
|-----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [source](../java/util/EventObject.md) The object on which the Event initially occurred. |

## Public constructors

### EventObject

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
EventObject(source: Any!)
```

Constructs a prototypical Event.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------|
| `source` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:the object on which the Event initially occurred |

| Exceptions ||
|--------------------------------------|-------------------|
| `java.lang.IllegalArgumentException` | if source is null |

## Public methods

### getSource

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSource(): Any!
```

The object on which the Event initially occurred.

| Return ||
|-----------------------------------------------------------------------------|--------------------------------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | the object on which the Event initially occurred |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

Returns a String representation of this EventObject.

| Return ||
|----------------------------------------------------------------------------------|---------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a String representation of this EventObject |

## Properties

### source

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected var source: Any!
```

The object on which the Event initially occurred.
