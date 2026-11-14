# Observable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Observable

Kotlin| [Java](Observable.md) 
| --- | --- |

```
abstract class Observable<T : Any!>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.database.Observable](Observable.md) |

| Known Direct Subclasses [ContentObservable](ContentObservable.md), [DataSetObservable](DataSetObservable.md) |--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [ContentObservable](ContentObservable.md) | A specialization of [Observable](Observable.md) for [ContentObserver](ContentObserver.md) that provides methods for sending notifications to a list of [ContentObserver](ContentObserver.md) objects. | | [DataSetObservable](DataSetObservable.md) | A specialization of [Observable](Observable.md) for [DataSetObserver](DataSetObserver.md) that provides methods for sending notifications to a list of [DataSetObserver](DataSetObserver.md) objects. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Provides methods for registering or unregistering arbitrary observers in an [ArrayList](../java.util/ArrayList.md). This abstract class is intended to be subclassed and specialized to maintain a registry of observers of specific types and dispatch notifications to them.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------|---|
| [Observable](Observable.md))`()` <br /> |

| Public methods ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerObserver](Observable.md))`(`observer:` `T`)` Adds an observer to the list. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unregisterAll](Observable.md))`()` Remove all registered observers. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unregisterObserver](Observable.md))`(`observer:` `T`)` Removes a previously registered observer. |
| --- | --- |

| Properties ||
|---------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| [ArrayList](../java.util/ArrayList.md)\<T\>! | [mObservers](Observable.md) The list of observers. |

## Public constructors

### Observable

```
Observable()
```

## Public methods

### registerObserver

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun registerObserver(observer: T): Unit
```

Adds an observer to the list. The observer cannot be null and it must not already be registered.

| Parameters ||
|------------|----------------------------|
| `observer` | T:the observer to register |

| Exceptions ||
|--------------------------------------|------------------------------------|
| `java.lang.IllegalArgumentException` | the observer is null |
| `java.lang.IllegalStateException` | the observer is already registered |

### unregisterAll

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun unregisterAll(): Unit
```

Remove all registered observers. 

### unregisterObserver

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun unregisterObserver(observer: T): Unit
```

Removes a previously registered observer. The observer must not be null and it must already have been registered.

| Parameters ||
|------------|------------------------------|
| `observer` | T:the observer to unregister |

| Exceptions ||
|--------------------------------------|------------------------------------|
| `java.lang.IllegalArgumentException` | the observer is null |
| `java.lang.IllegalStateException` | the observer is not yet registered |

## Properties

### mObservers

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected val mObservers: ArrayList<T>!
```

The list of observers. An observer can be in the list at most once and will never be null.
