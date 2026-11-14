# PropertyChangeEvent

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PropertyChangeEvent

```
open class PropertyChangeEvent : EventObject
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| ↳ | [java.util.EventObject](https://developer.android.com/reference/kotlin/java/util/EventObject.html#) ||
| | ↳ | [java.beans.PropertyChangeEvent](https://developer.android.com/reference/kotlin/java/beans/PropertyChangeEvent#) |

| Known Direct Subclasses [IndexedPropertyChangeEvent](https://developer.android.com/reference/kotlin/java/beans/IndexedPropertyChangeEvent) |--------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------| | [IndexedPropertyChangeEvent](https://developer.android.com/reference/kotlin/java/beans/IndexedPropertyChangeEvent) | An "IndexedPropertyChange" event gets delivered whenever a component that conforms to the JavaBeans™ specification (a "bean") changes a bound indexed property. | |

A "PropertyChange" event gets delivered whenever a bean changes a "bound" or "constrained" property. A PropertyChangeEvent object is sent as an argument to the PropertyChangeListener and VetoableChangeListener methods.

Normally PropertyChangeEvents are accompanied by the name and the old and new value of the changed property. If the new value is a primitive type (such as int or boolean) it must be wrapped as the corresponding java.lang.\* Object type (such as Integer or Boolean).

Null values may be provided for the old and the new values if their true values are not known.

An event source may send a null object as the name to indicate that an arbitrary set of if its properties have changed. In this case the old and new values should also be null.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [PropertyChangeEvent](https://developer.android.com/reference/kotlin/java/beans/PropertyChangeEvent#PropertyChangeEvent(kotlin.Any,%20kotlin.String,%20kotlin.Any,%20kotlin.Any))`(`source:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`, `propertyName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `oldValue:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`, `newValue:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Constructs a new `PropertyChangeEvent`. |

| Public methods ||
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getNewValue](https://developer.android.com/reference/kotlin/java/beans/PropertyChangeEvent#getNewValue())`()` Gets the new value for the property, expressed as an Object. |
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getOldValue](https://developer.android.com/reference/kotlin/java/beans/PropertyChangeEvent#getOldValue())`()` Gets the old value for the property, expressed as an Object. |
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getPropagationId](https://developer.android.com/reference/kotlin/java/beans/PropertyChangeEvent#getPropagationId())`()` The "propagationId" field is reserved for future use. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getPropertyName](https://developer.android.com/reference/kotlin/java/beans/PropertyChangeEvent#getPropertyName())`()` Gets the programmatic name of the property that was changed. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPropagationId](https://developer.android.com/reference/kotlin/java/beans/PropertyChangeEvent#setPropagationId(kotlin.Any))`(`propagationId:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Sets the propagationId object for the event. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/java/beans/PropertyChangeEvent#toString())`()` Returns a string representation of the object. |

| Inherited functions ||
|---|---|
| From class [EventObject](https://developer.android.com/reference/kotlin/java/util/EventObject.html#) |-----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getSource](https://developer.android.com/reference/kotlin/java/util/EventObject.html#getSource())`()` The object on which the Event initially occurred. <br /> | ||

| Inherited properties ||
|---|---|
| From class [EventObject](https://developer.android.com/reference/kotlin/java/util/EventObject.html#) |-----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [source](https://developer.android.com/reference/kotlin/java/util/EventObject.html#source:kotlin.Any) The object on which the Event initially occurred. <br /> | ||

## Public constructors

### PropertyChangeEvent

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
PropertyChangeEvent(
    source: Any!, 
    propertyName: String!, 
    oldValue: Any!, 
    newValue: Any!)
```

Constructs a new `PropertyChangeEvent`.

| Parameters ||
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| `source` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!: the bean that fired the event |
| `propertyName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the programmatic name of the property that was changed |
| `oldValue` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!: the old value of the property |
| `newValue` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!: the new value of the property |

| Exceptions ||
|--------------------------------------|-----------------------|
| `java.lang.IllegalArgumentException` | if `source` is `null` |

## Public methods

### getNewValue

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getNewValue(): Any!
```

Gets the new value for the property, expressed as an Object.

| Return ||
|-----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | The new value for the property, expressed as an Object. May be null if multiple properties have changed. |

### getOldValue

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getOldValue(): Any!
```

Gets the old value for the property, expressed as an Object.

| Return ||
|-----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | The old value for the property, expressed as an Object. May be null if multiple properties have changed. |

### getPropagationId

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPropagationId(): Any!
```

The "propagationId" field is reserved for future use. In Beans 1.0 the sole requirement is that if a listener catches a PropertyChangeEvent and then fires a PropertyChangeEvent of its own, then it should make sure that it propagates the propagationId field from its incoming event to its outgoing event.

| Return ||
|-----------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | the propagationId object associated with a bound/constrained property update. |

### getPropertyName

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPropertyName(): String!
```

Gets the programmatic name of the property that was changed.

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | The programmatic name of the property that was changed. May be null if multiple properties have changed. |

### setPropagationId

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setPropagationId(propagationId: Any!): Unit
```

Sets the propagationId object for the event.

| Parameters ||
|-----------------|----------------------------------------------------------------------------------------------------------------------|
| `propagationId` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!: The propagationId object for the event. |

### toString

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

Returns a string representation of the object.

| Return ||
|----------------------------------------------------------------------------------|---------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object |
