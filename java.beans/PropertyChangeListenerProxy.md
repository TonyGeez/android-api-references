# PropertyChangeListenerProxy

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PropertyChangeListenerProxy

```
open class PropertyChangeListenerProxy : EventListenerProxy<PropertyChangeListener!>, PropertyChangeListener
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [java.util.EventListenerProxy](../java/util/EventListenerProxy.md)\< [java.beans.PropertyChangeListener](../java/beans/PropertyChangeListener.md)\> ||
| | ↳ | [java.beans.PropertyChangeListenerProxy](../java/beans/PropertyChangeListenerProxy.md) |

A class which extends the`EventListenerProxy`specifically for adding a`PropertyChangeListener`with a "bound" property. Instances of this class can be added as`PropertyChangeListener`s to a bean which supports firing property change events.

If the object has a`getPropertyChangeListeners`method then the array returned could be a mixture of`PropertyChangeListener`and`PropertyChangeListenerProxy`objects.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [PropertyChangeListenerProxy](../java/beans/PropertyChangeListenerProxy.md))`(`propertyName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `listener:` ` [PropertyChangeListener](../java/beans/PropertyChangeListener.md)!`)` Constructor which binds the`PropertyChangeListener`to a specific property. |

| Public methods ||
|---------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getPropertyName](../java/beans/PropertyChangeListenerProxy.md))`()` Returns the name of the named property associated with the listener. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [propertyChange](../java/beans/PropertyChangeListenerProxy.md))`(`event:` ` [PropertyChangeEvent](../java/beans/PropertyChangeEvent.md)!`)` Forwards the property change event to the listener delegate. |

| Inherited functions ||
|---|---|
| From class [EventListenerProxy](../java/util/EventListenerProxy.md) |---|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | T | [getListener](../java/util/EventListenerProxy.md))`()` <br /> Returns the listener associated with the proxy. <br /> | ||

## Public constructors

### PropertyChangeListenerProxy

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
PropertyChangeListenerProxy(
    propertyName: String!, 
    listener: PropertyChangeListener!)
```

Constructor which binds the`PropertyChangeListener`to a specific property.

| Parameters ||
|----------------|---------------------------------------------------------------------------------------------------------------------------------|
| `propertyName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the property to listen on |
| `listener` | [PropertyChangeListener](../java/beans/PropertyChangeListener.md)!:the listener object |

## Public methods

### getPropertyName

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPropertyName(): String!
```

Returns the name of the named property associated with the listener.

| Return ||
|-----------------------------------------------------------------------------------|-------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the name of the named property associated with the listener |

### propertyChange

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun propertyChange(event: PropertyChangeEvent!): Unit
```

Forwards the property change event to the listener delegate.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------|
| `evt` | A PropertyChangeEvent object describing the event source and the property that has changed. |
| `event` | [PropertyChangeEvent](../java/beans/PropertyChangeEvent.md)!:the property change event |
