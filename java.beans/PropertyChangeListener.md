# PropertyChangeListener

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PropertyChangeListener

```
interface PropertyChangeListener : EventListener
```

| [java.beans.PropertyChangeListener](https://developer.android.com/reference/kotlin/java/beans/PropertyChangeListener#) |

| Known Direct Subclasses [PropertyChangeListenerProxy](https://developer.android.com/reference/kotlin/java/beans/PropertyChangeListenerProxy) |----------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------| | [PropertyChangeListenerProxy](https://developer.android.com/reference/kotlin/java/beans/PropertyChangeListenerProxy) | A class which extends the`EventListenerProxy`specifically for adding a`PropertyChangeListener`with a "bound" property. | |

A "PropertyChange" event gets fired whenever a bean changes a "bound" property. You can register a PropertyChangeListener with a source bean so as to be notified of any bound property updates.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [propertyChange](https://developer.android.com/reference/kotlin/java/beans/PropertyChangeListener#propertyChange(java.beans.PropertyChangeEvent))`(`evt:` ` [PropertyChangeEvent](https://developer.android.com/reference/kotlin/java/beans/PropertyChangeEvent)!`)` This method gets called when a bound property is changed. |

## Public methods

### propertyChange

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun propertyChange(evt: PropertyChangeEvent!): Unit
```

This method gets called when a bound property is changed.

| Parameters ||
|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `evt` | [PropertyChangeEvent](https://developer.android.com/reference/kotlin/java/beans/PropertyChangeEvent)!:A PropertyChangeEvent object describing the event source and the property that has changed. |
