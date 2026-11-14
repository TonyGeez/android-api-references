# Observable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Observable

```
open class Observable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [java.util.Observable](https://developer.android.com/reference/kotlin/java/util/Observable#) |

| Known Direct Subclasses [ContentQueryMap](https://developer.android.com/reference/kotlin/android/content/ContentQueryMap.html#) |---------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [ContentQueryMap](https://developer.android.com/reference/kotlin/android/content/ContentQueryMap.html#) | Caches the contents of a cursor into a Map of String-\>ContentValues and optionally keeps the cache fresh by registering for updates on the content backing the cursor. | |

| **This class was deprecated in API level 33.**
|
| This class and the [Observer](https://developer.android.com/reference/kotlin/java/util/Observer) interface have been deprecated. The event model supported by`Observer`and`Observable`is quite limited, the order of notifications delivered by`Observable`is unspecified, and state changes are not in one-for-one correspondence with notifications. For a richer event model, consider using the [java.beans](https://developer.android.com/reference/kotlin/java/beans/package-summary.html) package. For reliable and ordered messaging among threads, consider using one of the concurrent data structures in the [java.util.concurrent](https://developer.android.com/reference/kotlin/java/util/concurrent/package-summary) package. For reactive streams style programming, see the [java.util.concurrent.Flow](https://developer.android.com/reference/kotlin/java/util/concurrent/Flow) API.

This class represents an observable object, or "data" in the model-view paradigm. It can be subclassed to represent an object that the application wants to have observed.

An observable object can have one or more observers. An observer may be any object that implements interface`Observer`. After an observable instance changes, an application calling the`Observable`'s`notifyObservers`method causes all of its observers to be notified of the change by a call to their`update`method.

The order in which notifications will be delivered is unspecified. The default implementation provided in the Observable class will notify Observers in the order in which they registered interest, but subclasses may change this order, use no guaranteed order, deliver notifications on separate threads, or may guarantee that their subclass follows this order, as they choose.

Note that this notification mechanism has nothing to do with threads and is completely separate from the`wait`and`notify`mechanism of class`Object`.

When an observable object is newly created, its set of observers is empty. Two observers are considered the same if and only if the`equals`method returns true for them.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [Observable](https://developer.android.com/reference/kotlin/java/util/Observable#Observable())`()` Construct an Observable with zero Observers. |

| Public methods ||
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addObserver](https://developer.android.com/reference/kotlin/java/util/Observable#addObserver(java.util.Observer))`(`o:` ` [Observer](https://developer.android.com/reference/kotlin/java/util/Observer)!`)` Adds an observer to the set of observers for this object, provided that it is not the same as some observer already in the set. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [countObservers](https://developer.android.com/reference/kotlin/java/util/Observable#countObservers())`()` Returns the number of observers of this`Observable`object. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [deleteObserver](https://developer.android.com/reference/kotlin/java/util/Observable#deleteObserver(java.util.Observer))`(`o:` ` [Observer](https://developer.android.com/reference/kotlin/java/util/Observer)!`)` Deletes an observer from the set of observers of this object. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [deleteObservers](https://developer.android.com/reference/kotlin/java/util/Observable#deleteObservers())`()` Clears the observer list so that this object no longer has any observers. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasChanged](https://developer.android.com/reference/kotlin/java/util/Observable#hasChanged())`()` Tests if this object has changed. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [notifyObservers](https://developer.android.com/reference/kotlin/java/util/Observable#notifyObservers())`()` If this object has changed, as indicated by the`hasChanged`method, then notify all of its observers and then call the`clearChanged`method to indicate that this object has no longer changed. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [notifyObservers](https://developer.android.com/reference/kotlin/java/util/Observable#notifyObservers(kotlin.Any))`(`arg:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` If this object has changed, as indicated by the`hasChanged`method, then notify all of its observers and then call the`clearChanged`method to indicate that this object has no longer changed. |

| Protected methods ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clearChanged](https://developer.android.com/reference/kotlin/java/util/Observable#clearChanged())`()` Indicates that this object has no longer changed, or that it has already notified all of its observers of its most recent change, so that the`hasChanged`method will now return`false`. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setChanged](https://developer.android.com/reference/kotlin/java/util/Observable#setChanged())`()` Marks this`Observable`object as having been changed; the`hasChanged`method will now return`true`. |

## Public constructors

### Observable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Observable()
```

Construct an Observable with zero Observers.

## Public methods

### addObserver

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun addObserver(o: Observer!): Unit
```

**Deprecated:** *Deprecated in Java.*

Adds an observer to the set of observers for this object, provided that it is not the same as some observer already in the set. The order in which notifications will be delivered to multiple observers is not specified. See the class comment.

| Parameters ||
|-----|---------------------------------------------------------------------------------------------------------|
| `o` | [Observer](https://developer.android.com/reference/kotlin/java/util/Observer)!:an observer to be added. |

| Exceptions ||
|----------------------------------|-----------------------------|
| `java.lang.NullPointerException` | if the parameter o is null. |

### countObservers

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun countObservers(): Int
```

**Deprecated:** *Deprecated in Java.*

Returns the number of observers of this`Observable`object.

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of observers of this object. |

### deleteObserver

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun deleteObserver(o: Observer!): Unit
```

**Deprecated:** *Deprecated in Java.*

Deletes an observer from the set of observers of this object. Passing`null`to this method will have no effect.

| Parameters ||
|-----|------------------------------------------------------------------------------------------------------------|
| `o` | [Observer](https://developer.android.com/reference/kotlin/java/util/Observer)!:the observer to be deleted. |

### deleteObservers

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun deleteObservers(): Unit
```

**Deprecated:** *Deprecated in Java.*

Clears the observer list so that this object no longer has any observers. 

### hasChanged

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hasChanged(): Boolean
```

**Deprecated:** *Deprecated in Java.*

Tests if this object has changed.

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if and only if the`setChanged`method has been called more recently than the`clearChanged`method on this object;`false`otherwise. |

**See Also**

- [java.util.Observable#clearChanged()](https://developer.android.com/reference/kotlin/java/util/Observable#clearChanged())
- [java.util.Observable#setChanged()](https://developer.android.com/reference/kotlin/java/util/Observable#setChanged()) 

### notifyObservers

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun notifyObservers(): Unit
```

**Deprecated:** *Deprecated in Java.*

If this object has changed, as indicated by the`hasChanged`method, then notify all of its observers and then call the`clearChanged`method to indicate that this object has no longer changed.

Each observer has its`update`method called with two arguments: this observable object and`null`. In other words, this method is equivalent to:
`notifyObservers(null)` 
**See Also**

- [java.util.Observable#clearChanged()](https://developer.android.com/reference/kotlin/java/util/Observable#clearChanged())
- [java.util.Observable#hasChanged()](https://developer.android.com/reference/kotlin/java/util/Observable#hasChanged())
- [java.util.Observer#update(java.util.Observable, java.lang.Object)](https://developer.android.com/reference/kotlin/java/util/Observer#update(java.util.Observable,%20kotlin.Any)) 

### notifyObservers

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun notifyObservers(arg: Any!): Unit
```

**Deprecated:** *Deprecated in Java.*

If this object has changed, as indicated by the`hasChanged`method, then notify all of its observers and then call the`clearChanged`method to indicate that this object has no longer changed.

Each observer has its`update`method called with two arguments: this observable object and the`arg`argument.

| Parameters ||
|-------|-----------------------------------------------------------------------------------------|
| `arg` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:any object. |

**See Also**

- [java.util.Observable#clearChanged()](https://developer.android.com/reference/kotlin/java/util/Observable#clearChanged())
- [java.util.Observable#hasChanged()](https://developer.android.com/reference/kotlin/java/util/Observable#hasChanged())
- [java.util.Observer#update(java.util.Observable, java.lang.Object)](https://developer.android.com/reference/kotlin/java/util/Observer#update(java.util.Observable,%20kotlin.Any))

## Protected methods

### clearChanged

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun clearChanged(): Unit
```

**Deprecated:** *Deprecated in Java.*

Indicates that this object has no longer changed, or that it has already notified all of its observers of its most recent change, so that the`hasChanged`method will now return`false`. This method is called automatically by the`notifyObservers`methods. 
**See Also**

- [java.util.Observable#notifyObservers()](https://developer.android.com/reference/kotlin/java/util/Observable#notifyObservers())
- [java.util.Observable#notifyObservers(java.lang.Object)](https://developer.android.com/reference/kotlin/java/util/Observable#notifyObservers(kotlin.Any)) 

### setChanged

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun setChanged(): Unit
```

**Deprecated:** *Deprecated in Java.*

Marks this`Observable`object as having been changed; the`hasChanged`method will now return`true`.
