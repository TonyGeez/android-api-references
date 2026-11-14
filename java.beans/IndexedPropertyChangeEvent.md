# IndexedPropertyChangeEvent

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# IndexedPropertyChangeEvent

```
open class IndexedPropertyChangeEvent : PropertyChangeEvent
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [java.util.EventObject](https://developer.android.com/reference/kotlin/java/util/EventObject.html#) |||
| | ↳ | [java.beans.PropertyChangeEvent](https://developer.android.com/reference/kotlin/java/beans/PropertyChangeEvent) ||
| | | ↳ | [java.beans.IndexedPropertyChangeEvent](https://developer.android.com/reference/kotlin/java/beans/IndexedPropertyChangeEvent#) |
| --- | --- | --- | --- |

An "IndexedPropertyChange" event gets delivered whenever a component that conforms to the JavaBeans™ specification (a "bean") changes a bound indexed property. This class is an extension of`PropertyChangeEvent`but contains the index of the property that has changed.

Null values may be provided for the old and the new values if their true values are not known.

An event source may send a null object as the name to indicate that an arbitrary set of if its properties have changed. In this case the old and new values should also be null.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [IndexedPropertyChangeEvent](https://developer.android.com/reference/kotlin/java/beans/IndexedPropertyChangeEvent#IndexedPropertyChangeEvent(kotlin.Any,%20kotlin.String,%20kotlin.Any,%20kotlin.Any,%20kotlin.Int))`(`source:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`, `propertyName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `oldValue:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`, `newValue:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`, `index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Constructs a new`IndexedPropertyChangeEvent`object. |

| Public methods ||
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getIndex](https://developer.android.com/reference/kotlin/java/beans/IndexedPropertyChangeEvent#getIndex())`()` Gets the index of the property that was changed. |

| Inherited functions ||
|---|---|
| From class [PropertyChangeEvent](https://developer.android.com/reference/kotlin/java/beans/PropertyChangeEvent) |-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getNewValue](https://developer.android.com/reference/kotlin/java/beans/PropertyChangeEvent#getNewValue())`()` <br /> Gets the new value for the property, expressed as an Object. <br /> | | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getOldValue](https://developer.android.com/reference/kotlin/java/beans/PropertyChangeEvent#getOldValue())`()` <br /> Gets the old value for the property, expressed as an Object. <br /> | | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getPropagationId](https://developer.android.com/reference/kotlin/java/beans/PropertyChangeEvent#getPropagationId())`()` <br /> The "propagationId" field is reserved for future use. In Beans 1.0 the sole requirement is that if a listener catches a PropertyChangeEvent and then fires a PropertyChangeEvent of its own, then it should make sure that it propagates the propagationId field from its incoming event to its outgoing event. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getPropertyName](https://developer.android.com/reference/kotlin/java/beans/PropertyChangeEvent#getPropertyName())`()` <br /> Gets the programmatic name of the property that was changed. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPropagationId](https://developer.android.com/reference/kotlin/java/beans/PropertyChangeEvent#setPropagationId(kotlin.Any))`(`propagationId:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` <br /> Sets the propagationId object for the event. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/java/beans/PropertyChangeEvent#toString())`()` <br /> Returns a string representation of the object. <br /> | ||
| From class [EventObject](https://developer.android.com/reference/kotlin/java/util/EventObject.html#) |-----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getSource](https://developer.android.com/reference/kotlin/java/util/EventObject.html#getSource())`()` <br /> The object on which the Event initially occurred. <br /> | ||

| Inherited properties ||
|---|---|
| From class [EventObject](https://developer.android.com/reference/kotlin/java/util/EventObject.html#) |-----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [source](https://developer.android.com/reference/kotlin/java/util/EventObject.html#source:kotlin.Any) <br /> The object on which the Event initially occurred. <br /> | ||

## Public constructors

### IndexedPropertyChangeEvent

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
IndexedPropertyChangeEvent(
    source: Any!, 
    propertyName: String!, 
    oldValue: Any!, 
    newValue: Any!, 
    index: Int)
```

Constructs a new`IndexedPropertyChangeEvent`object.

| Parameters ||
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| `source` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:The bean that fired the event. |
| `propertyName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The programmatic name of the property that was changed. |
| `oldValue` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:The old value of the property. |
| --- | --- |
| `newValue` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:The new value of the property. |
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):index of the property element that was changed. |

## Public methods

### getIndex

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getIndex(): Int
```

Gets the index of the property that was changed.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The index specifying the property element that was changed. |
