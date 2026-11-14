# EventListenerProxy

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# EventListenerProxy

```
abstract class EventListenerProxy<T : EventListener!> : EventListener
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.util.EventListenerProxy](EventListenerProxy.md) |

| Known Direct Subclasses [PropertyChangeListenerProxy](../java.beans/PropertyChangeListenerProxy.md) |----------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------| | [PropertyChangeListenerProxy](../java.beans/PropertyChangeListenerProxy.md) | A class which extends the`EventListenerProxy`specifically for adding a`PropertyChangeListener`with a "bound" property. | |
| --- | --- | --- | --- | --- | --- | --- |

An abstract wrapper class for an`EventListener`class which associates a set of additional parameters with the listener. Subclasses must provide the storage and accessor methods for the additional arguments or parameters.

For example, a bean which supports named properties would have a two argument method signature for adding a`PropertyChangeListener`for a property: 

```kotlin
public void addPropertyChangeListener(String propertyName,
                                        PropertyChangeListener listener)
  
```
If the bean also implemented the zero argument get listener method: 

```kotlin
public PropertyChangeListener[] getPropertyChangeListeners()
  
```
then the array may contain inner`PropertyChangeListeners`which are also`PropertyChangeListenerProxy`objects.

If the calling method is interested in retrieving the named property then it would have to test the element to see if it is a proxy class.

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [EventListenerProxy](EventListenerProxy.md))`(`listener:` `T`)` Creates a proxy for the specified listener. |

| Public methods ||
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openT | [getListener](EventListenerProxy.md))`()` Returns the listener associated with the proxy. |

## Public constructors

### EventListenerProxy

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
EventListenerProxy(listener: T)
```

Creates a proxy for the specified listener.

| Parameters ||
|------------|-----------------------|
| `listener` | T:the listener object |

## Public methods

### getListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getListener(): T
```

Returns the listener associated with the proxy.

| Return ||
|---|----------------------------------------|
| T | the listener associated with the proxy |
