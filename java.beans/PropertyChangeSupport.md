# PropertyChangeSupport

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PropertyChangeSupport

```
open class PropertyChangeSupport : Serializable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [java.beans.PropertyChangeSupport](https://developer.android.com/reference/kotlin/java/beans/PropertyChangeSupport#) |

This is a utility class that can be used by beans that support bound properties. It manages a list of listeners and dispatches [PropertyChangeEvent](https://developer.android.com/reference/kotlin/java/beans/PropertyChangeEvent) s to them. You can use an instance of this class as a member field of your bean and delegate these types of work to it. The [PropertyChangeListener](https://developer.android.com/reference/kotlin/java/beans/PropertyChangeListener) can be registered for all properties or for a property specified by name.

Here is an example of`PropertyChangeSupport`usage that follows the rules and recommendations laid out in the JavaBeans™ specification: 

```kotlin
public class MyBean {
      private final PropertyChangeSupport pcs = new PropertyChangeSupport(this);
 
      public void addPropertyChangeListener(PropertyChangeListener listener) {
          this.pcs.addPropertyChangeListener(listener);
      }
 
      public void removePropertyChangeListener(PropertyChangeListener listener) {
          this.pcs.removePropertyChangeListener(listener);
      }
 
      private String value;
 
      public String getValue() {
          return this.value;
      }
 
      public void setValue(String newValue) {
          String oldValue = this.value;
          this.value = newValue;
          this.pcs.firePropertyChange("value", oldValue, newValue);
      }
 
      [...]
  }
  
```

A`PropertyChangeSupport`instance is thread-safe.

This class is serializable. When it is serialized it will save (and restore) any listeners that are themselves serializable. Any non-serializable listeners will be skipped during serialization.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [PropertyChangeSupport](https://developer.android.com/reference/kotlin/java/beans/PropertyChangeSupport#PropertyChangeSupport(kotlin.Any))`(`sourceBean:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Constructs a`PropertyChangeSupport`object. |

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addPropertyChangeListener](https://developer.android.com/reference/kotlin/java/beans/PropertyChangeSupport#addPropertyChangeListener(java.beans.PropertyChangeListener))`(`listener:` ` [PropertyChangeListener](https://developer.android.com/reference/kotlin/java/beans/PropertyChangeListener)!`)` Add a PropertyChangeListener to the listener list. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addPropertyChangeListener](https://developer.android.com/reference/kotlin/java/beans/PropertyChangeSupport#addPropertyChangeListener(kotlin.String,%20java.beans.PropertyChangeListener))`(`propertyName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `listener:` ` [PropertyChangeListener](https://developer.android.com/reference/kotlin/java/beans/PropertyChangeListener)!`)` Add a PropertyChangeListener for a specific property. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [fireIndexedPropertyChange](https://developer.android.com/reference/kotlin/java/beans/PropertyChangeSupport#fireIndexedPropertyChange(kotlin.String,%20kotlin.Int,%20kotlin.Boolean,%20kotlin.Boolean))`(`propertyName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `oldValue:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `newValue:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Reports a boolean bound indexed property update to listeners that have been registered to track updates of all properties or a property with the specified name. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [fireIndexedPropertyChange](https://developer.android.com/reference/kotlin/java/beans/PropertyChangeSupport#fireIndexedPropertyChange(kotlin.String,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`propertyName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `oldValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `newValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Reports an integer bound indexed property update to listeners that have been registered to track updates of all properties or a property with the specified name. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [fireIndexedPropertyChange](https://developer.android.com/reference/kotlin/java/beans/PropertyChangeSupport#fireIndexedPropertyChange(kotlin.String,%20kotlin.Int,%20kotlin.Any,%20kotlin.Any))`(`propertyName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `oldValue:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`, `newValue:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Reports a bound indexed property update to listeners that have been registered to track updates of all properties or a property with the specified name. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [firePropertyChange](https://developer.android.com/reference/kotlin/java/beans/PropertyChangeSupport#firePropertyChange(java.beans.PropertyChangeEvent))`(`event:` ` [PropertyChangeEvent](https://developer.android.com/reference/kotlin/java/beans/PropertyChangeEvent)!`)` Fires a property change event to listeners that have been registered to track updates of all properties or a property with the specified name. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [firePropertyChange](https://developer.android.com/reference/kotlin/java/beans/PropertyChangeSupport#firePropertyChange(kotlin.String,%20kotlin.Boolean,%20kotlin.Boolean))`(`propertyName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `oldValue:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `newValue:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Reports a boolean bound property update to listeners that have been registered to track updates of all properties or a property with the specified name. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [firePropertyChange](https://developer.android.com/reference/kotlin/java/beans/PropertyChangeSupport#firePropertyChange(kotlin.String,%20kotlin.Int,%20kotlin.Int))`(`propertyName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `oldValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `newValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Reports an integer bound property update to listeners that have been registered to track updates of all properties or a property with the specified name. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [firePropertyChange](https://developer.android.com/reference/kotlin/java/beans/PropertyChangeSupport#firePropertyChange(kotlin.String,%20kotlin.Any,%20kotlin.Any))`(`propertyName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `oldValue:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`, `newValue:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Reports a bound property update to listeners that have been registered to track updates of all properties or a property with the specified name. |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [PropertyChangeListener](https://developer.android.com/reference/kotlin/java/beans/PropertyChangeListener)!\>! | [getPropertyChangeListeners](https://developer.android.com/reference/kotlin/java/beans/PropertyChangeSupport#getPropertyChangeListeners())`()` Returns an array of all the listeners that were added to the PropertyChangeSupport object with addPropertyChangeListener(). |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [PropertyChangeListener](https://developer.android.com/reference/kotlin/java/beans/PropertyChangeListener)!\>! | [getPropertyChangeListeners](https://developer.android.com/reference/kotlin/java/beans/PropertyChangeSupport#getPropertyChangeListeners(kotlin.String))`(`propertyName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns an array of all the listeners which have been associated with the named property. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasListeners](https://developer.android.com/reference/kotlin/java/beans/PropertyChangeSupport#hasListeners(kotlin.String))`(`propertyName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Check if there are any listeners for a specific property, including those registered on all properties. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removePropertyChangeListener](https://developer.android.com/reference/kotlin/java/beans/PropertyChangeSupport#removePropertyChangeListener(java.beans.PropertyChangeListener))`(`listener:` ` [PropertyChangeListener](https://developer.android.com/reference/kotlin/java/beans/PropertyChangeListener)!`)` Remove a PropertyChangeListener from the listener list. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removePropertyChangeListener](https://developer.android.com/reference/kotlin/java/beans/PropertyChangeSupport#removePropertyChangeListener(kotlin.String,%20java.beans.PropertyChangeListener))`(`propertyName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `listener:` ` [PropertyChangeListener](https://developer.android.com/reference/kotlin/java/beans/PropertyChangeListener)!`)` Remove a PropertyChangeListener for a specific property. |

## Public constructors

### PropertyChangeSupport

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
PropertyChangeSupport(sourceBean: Any!)
```

Constructs a`PropertyChangeSupport`object.

| Parameters ||
|--------------|--------------------------------------------------------------------------------------------------------------------------------|
| `sourceBean` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:The bean to be given as the source for any events. |

## Public methods

### addPropertyChangeListener

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun addPropertyChangeListener(listener: PropertyChangeListener!): Unit
```

Add a PropertyChangeListener to the listener list. The listener is registered for all properties. The same listener object may be added more than once, and will be called as many times as it is added. If`listener`is null, no exception is thrown and no action is taken.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [PropertyChangeListener](https://developer.android.com/reference/kotlin/java/beans/PropertyChangeListener)!:The PropertyChangeListener to be added |

### addPropertyChangeListener

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun addPropertyChangeListener(
    propertyName: String!, 
    listener: PropertyChangeListener!
): Unit
```

Add a PropertyChangeListener for a specific property. The listener will be invoked only when a call on firePropertyChange names that specific property. The same listener object may be added more than once. For each property, the listener will be invoked the number of times it was added for that property. If`propertyName`or`listener`is null, no exception is thrown and no action is taken.

| Parameters ||
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| `propertyName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The name of the property to listen on. |
| `listener` | [PropertyChangeListener](https://developer.android.com/reference/kotlin/java/beans/PropertyChangeListener)!:The PropertyChangeListener to be added |

### fireIndexedPropertyChange

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun fireIndexedPropertyChange(
    propertyName: String!, 
    index: Int, 
    oldValue: Boolean, 
    newValue: Boolean
): Unit
```

Reports a boolean bound indexed property update to listeners that have been registered to track updates of all properties or a property with the specified name.

No event is fired if old and new values are equal.

This is merely a convenience wrapper around the more general [fireIndexedPropertyChange(java.lang.String,int,java.lang.Object,java.lang.Object)](https://developer.android.com/reference/kotlin/java/beans/PropertyChangeSupport#fireIndexedPropertyChange(kotlin.String,%20kotlin.Int,%20kotlin.Any,%20kotlin.Any))method.

| Parameters ||
|----------------|------------------------------------------------------------------------------------------------------------------------------------------|
| `propertyName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the programmatic name of the property that was changed |
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index of the property element that was changed |
| `oldValue` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):the old value of the property |
| `newValue` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):the new value of the property |

### fireIndexedPropertyChange

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun fireIndexedPropertyChange(
    propertyName: String!, 
    index: Int, 
    oldValue: Int, 
    newValue: Int
): Unit
```

Reports an integer bound indexed property update to listeners that have been registered to track updates of all properties or a property with the specified name.

No event is fired if old and new values are equal.

This is merely a convenience wrapper around the more general [fireIndexedPropertyChange(java.lang.String,int,java.lang.Object,java.lang.Object)](https://developer.android.com/reference/kotlin/java/beans/PropertyChangeSupport#fireIndexedPropertyChange(kotlin.String,%20kotlin.Int,%20kotlin.Any,%20kotlin.Any))method.

| Parameters ||
|----------------|------------------------------------------------------------------------------------------------------------------------------------------|
| `propertyName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the programmatic name of the property that was changed |
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index of the property element that was changed |
| `oldValue` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the old value of the property |
| `newValue` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the new value of the property |

### fireIndexedPropertyChange

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun fireIndexedPropertyChange(
    propertyName: String!, 
    index: Int, 
    oldValue: Any!, 
    newValue: Any!
): Unit
```

Reports a bound indexed property update to listeners that have been registered to track updates of all properties or a property with the specified name.

No event is fired if old and new values are equal and non-null.

This is merely a convenience wrapper around the more general [firePropertyChange(java.beans.PropertyChangeEvent)](https://developer.android.com/reference/kotlin/java/beans/PropertyChangeSupport#firePropertyChange(java.beans.PropertyChangeEvent))method.

| Parameters ||
|----------------|------------------------------------------------------------------------------------------------------------------------------------------|
| `propertyName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the programmatic name of the property that was changed |
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index of the property element that was changed |
| `oldValue` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:the old value of the property |
| `newValue` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:the new value of the property |

### firePropertyChange

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun firePropertyChange(event: PropertyChangeEvent!): Unit
```

Fires a property change event to listeners that have been registered to track updates of all properties or a property with the specified name.

No event is fired if the given event's old and new values are equal and non-null.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------------------------|
| `event` | [PropertyChangeEvent](https://developer.android.com/reference/kotlin/java/beans/PropertyChangeEvent)!:the`PropertyChangeEvent`to be fired |

### firePropertyChange

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun firePropertyChange(
    propertyName: String!, 
    oldValue: Boolean, 
    newValue: Boolean
): Unit
```

Reports a boolean bound property update to listeners that have been registered to track updates of all properties or a property with the specified name.

No event is fired if old and new values are equal.

This is merely a convenience wrapper around the more general [firePropertyChange(java.lang.String,java.lang.Object,java.lang.Object)](https://developer.android.com/reference/kotlin/java/beans/PropertyChangeSupport#firePropertyChange(kotlin.String,%20kotlin.Any,%20kotlin.Any))method.

| Parameters ||
|----------------|------------------------------------------------------------------------------------------------------------------------------------------|
| `propertyName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the programmatic name of the property that was changed |
| `oldValue` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):the old value of the property |
| `newValue` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):the new value of the property |

### firePropertyChange

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun firePropertyChange(
    propertyName: String!, 
    oldValue: Int, 
    newValue: Int
): Unit
```

Reports an integer bound property update to listeners that have been registered to track updates of all properties or a property with the specified name.

No event is fired if old and new values are equal.

This is merely a convenience wrapper around the more general [firePropertyChange(java.lang.String,java.lang.Object,java.lang.Object)](https://developer.android.com/reference/kotlin/java/beans/PropertyChangeSupport#firePropertyChange(kotlin.String,%20kotlin.Any,%20kotlin.Any))method.

| Parameters ||
|----------------|------------------------------------------------------------------------------------------------------------------------------------------|
| `propertyName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the programmatic name of the property that was changed |
| `oldValue` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the old value of the property |
| `newValue` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the new value of the property |

### firePropertyChange

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun firePropertyChange(
    propertyName: String!, 
    oldValue: Any!, 
    newValue: Any!
): Unit
```

Reports a bound property update to listeners that have been registered to track updates of all properties or a property with the specified name.

No event is fired if old and new values are equal and non-null.

This is merely a convenience wrapper around the more general [firePropertyChange(java.beans.PropertyChangeEvent)](https://developer.android.com/reference/kotlin/java/beans/PropertyChangeSupport#firePropertyChange(java.beans.PropertyChangeEvent))method.

| Parameters ||
|----------------|------------------------------------------------------------------------------------------------------------------------------------------|
| `propertyName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the programmatic name of the property that was changed |
| `oldValue` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:the old value of the property |
| `newValue` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:the new value of the property |

### getPropertyChangeListeners

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPropertyChangeListeners(): Array<PropertyChangeListener!>!
```

Returns an array of all the listeners that were added to the PropertyChangeSupport object with addPropertyChangeListener().

If some listeners have been added with a named property, then the returned array will be a mixture of PropertyChangeListeners and`PropertyChangeListenerProxy`s. If the calling method is interested in distinguishing the listeners then it must test each element to see if it's a`PropertyChangeListenerProxy`, perform the cast, and examine the parameter. 

```kotlin
<code>PropertyChangeListener[] listeners = bean.getPropertyChangeListeners();
  for (int i = 0; i &lt; listeners.length; i++) {
    if (listeners[i] instanceof PropertyChangeListenerProxy) {
      PropertyChangeListenerProxy proxy =
                     (PropertyChangeListenerProxy)listeners[i];
      if (proxy.getPropertyName().equals("foo")) {
        // proxy is a PropertyChangeListener which was associated
        // with the property named "foo"
      }
    }
  }
  </code>
```

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [PropertyChangeListener](https://developer.android.com/reference/kotlin/java/beans/PropertyChangeListener)!>! | all of the`PropertyChangeListeners`added or an empty array if no listeners have been added |

**See Also**

- [java.beans.PropertyChangeListenerProxy](https://developer.android.com/reference/kotlin/java/beans/PropertyChangeListenerProxy) 

### getPropertyChangeListeners

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPropertyChangeListeners(propertyName: String!): Array<PropertyChangeListener!>!
```

Returns an array of all the listeners which have been associated with the named property.

| Parameters ||
|----------------|------------------------------------------------------------------------------------------------------------------------------|
| `propertyName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The name of the property being listened to |

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [PropertyChangeListener](https://developer.android.com/reference/kotlin/java/beans/PropertyChangeListener)!>! | all of the`PropertyChangeListeners`associated with the named property. If no such listeners have been added, or if`propertyName`is null, an empty array is returned. |

### hasListeners

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hasListeners(propertyName: String!): Boolean
```

Check if there are any listeners for a specific property, including those registered on all properties. If`propertyName`is null, only check for listeners registered on all properties.

| Parameters ||
|----------------|------------------------------------------------------------------------------------------------------|
| `propertyName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the property name. |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if there are one or more listeners for the given property |

### removePropertyChangeListener

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun removePropertyChangeListener(listener: PropertyChangeListener!): Unit
```

Remove a PropertyChangeListener from the listener list. This removes a PropertyChangeListener that was registered for all properties. If`listener`was added more than once to the same event source, it will be notified one less time after being removed. If`listener`is null, or was never added, no exception is thrown and no action is taken.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [PropertyChangeListener](https://developer.android.com/reference/kotlin/java/beans/PropertyChangeListener)!:The PropertyChangeListener to be removed |

### removePropertyChangeListener

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun removePropertyChangeListener(
    propertyName: String!, 
    listener: PropertyChangeListener!
): Unit
```

Remove a PropertyChangeListener for a specific property. If`listener`was added more than once to the same event source for the specified property, it will be notified one less time after being removed. If`propertyName`is null, no exception is thrown and no action is taken. If`listener`is null, or was never added for the specified property, no exception is thrown and no action is taken.

| Parameters ||
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `propertyName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The name of the property that was listened on. |
| `listener` | [PropertyChangeListener](https://developer.android.com/reference/kotlin/java/beans/PropertyChangeListener)!:The PropertyChangeListener to be removed |
