# EventObject

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# EventObject

```
open class EventObject : Serializable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [java.util.EventObject](https://developer.android.com/reference/kotlin/java/util/EventObject#) |

| Known Direct Subclasses [ConnectionEvent](https://developer.android.com/reference/kotlin/javax/sql/ConnectionEvent.html#), [HandshakeCompletedEvent](https://developer.android.com/reference/kotlin/javax/net/ssl/HandshakeCompletedEvent.html#), [NodeChangeEvent](https://developer.android.com/reference/kotlin/java/util/prefs/NodeChangeEvent), [PreferenceChangeEvent](https://developer.android.com/reference/kotlin/java/util/prefs/PreferenceChangeEvent), [PropertyChangeEvent](https://developer.android.com/reference/kotlin/java/beans/PropertyChangeEvent.html#), [RowSetEvent](https://developer.android.com/reference/kotlin/javax/sql/RowSetEvent.html#), [SSLSessionBindingEvent](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSessionBindingEvent.html#), [StatementEvent](https://developer.android.com/reference/kotlin/javax/sql/StatementEvent.html#) |-----------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------| | [ConnectionEvent](https://developer.android.com/reference/kotlin/javax/sql/ConnectionEvent.html#) | An`Event`object that provides information about the source of a connection-related event. | | [HandshakeCompletedEvent](https://developer.android.com/reference/kotlin/javax/net/ssl/HandshakeCompletedEvent.html#) | This event indicates that an SSL handshake completed on a given SSL connection. | | [NodeChangeEvent](https://developer.android.com/reference/kotlin/java/util/prefs/NodeChangeEvent) | An event emitted by a Preferences node to indicate that a child of that node has been added or removed. | | [PreferenceChangeEvent](https://developer.android.com/reference/kotlin/java/util/prefs/PreferenceChangeEvent) | An event emitted by a Preferences node to indicate that a preference has been added, removed or has had its value changed. | | [PropertyChangeEvent](https://developer.android.com/reference/kotlin/java/beans/PropertyChangeEvent.html#) | A "PropertyChange" event gets delivered whenever a bean changes a "bound" or "constrained" property. | | [RowSetEvent](https://developer.android.com/reference/kotlin/javax/sql/RowSetEvent.html#) | An`Event`object generated when an event occurs to a`RowSet`object. | | [SSLSessionBindingEvent](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSessionBindingEvent.html#) | This event is propagated to a SSLSessionBindingListener. | | [StatementEvent](https://developer.android.com/reference/kotlin/javax/sql/StatementEvent.html#) | A`StatementEvent`is sent to all`StatementEventListener`s which were registered with a`PooledConnection`. | |

| Known Indirect Subclasses [IndexedPropertyChangeEvent](https://developer.android.com/reference/kotlin/java/beans/IndexedPropertyChangeEvent.html#) |--------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------| | [IndexedPropertyChangeEvent](https://developer.android.com/reference/kotlin/java/beans/IndexedPropertyChangeEvent.html#) | An "IndexedPropertyChange" event gets delivered whenever a component that conforms to the JavaBeans™ specification (a "bean") changes a bound indexed property. | |

The root class from which all event state objects shall be derived.

All Events are constructed with a reference to the object, the "source", that is logically deemed to be the object upon which the Event in question initially occurred upon.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [EventObject](https://developer.android.com/reference/kotlin/java/util/EventObject#EventObject(kotlin.Any))`(`source:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Constructs a prototypical Event. |

| Public methods ||
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getSource](https://developer.android.com/reference/kotlin/java/util/EventObject#getSource())`()` The object on which the Event initially occurred. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/java/util/EventObject#toString())`()` Returns a String representation of this EventObject. |

| Properties ||
|-----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [source](https://developer.android.com/reference/kotlin/java/util/EventObject#source:kotlin.Any) The object on which the Event initially occurred. |

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
