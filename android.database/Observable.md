# Observable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Observable

Kotlin| [Java](https://developer.android.com/reference/android/database/Observable "View this page in Java") 
| --- | --- |

```
abstract class Observable<T : Any!>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.database.Observable](https://developer.android.com/reference/kotlin/android/database/Observable#) |

| Known Direct Subclasses [ContentObservable](https://developer.android.com/reference/kotlin/android/database/ContentObservable), [DataSetObservable](https://developer.android.com/reference/kotlin/android/database/DataSetObservable) |--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [ContentObservable](https://developer.android.com/reference/kotlin/android/database/ContentObservable) | A specialization of [Observable](https://developer.android.com/reference/kotlin/android/database/Observable#) for [ContentObserver](https://developer.android.com/reference/kotlin/android/database/ContentObserver) that provides methods for sending notifications to a list of [ContentObserver](https://developer.android.com/reference/kotlin/android/database/ContentObserver) objects. | | [DataSetObservable](https://developer.android.com/reference/kotlin/android/database/DataSetObservable) | A specialization of [Observable](https://developer.android.com/reference/kotlin/android/database/Observable#) for [DataSetObserver](https://developer.android.com/reference/kotlin/android/database/DataSetObserver) that provides methods for sending notifications to a list of [DataSetObserver](https://developer.android.com/reference/kotlin/android/database/DataSetObserver) objects. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Provides methods for registering or unregistering arbitrary observers in an [ArrayList](https://developer.android.com/reference/kotlin/java/util/ArrayList.html#). This abstract class is intended to be subclassed and specialized to maintain a registry of observers of specific types and dispatch notifications to them.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------|---|
| [Observable](https://developer.android.com/reference/kotlin/android/database/Observable#Observable())`()` <br /> |

| Public methods ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerObserver](https://developer.android.com/reference/kotlin/android/database/Observable#registerObserver(android.database.Observable.T))`(`observer:` `T`)` Adds an observer to the list. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unregisterAll](https://developer.android.com/reference/kotlin/android/database/Observable#unregisterAll())`()` Remove all registered observers. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unregisterObserver](https://developer.android.com/reference/kotlin/android/database/Observable#unregisterObserver(android.database.Observable.T))`(`observer:` `T`)` Removes a previously registered observer. |
| --- | --- |

| Properties ||
|---------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| [ArrayList](https://developer.android.com/reference/kotlin/java/util/ArrayList.html#)\<T\>! | [mObservers](https://developer.android.com/reference/kotlin/android/database/Observable#mObservers:java.util.ArrayList) The list of observers. |

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
