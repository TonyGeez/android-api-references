# DataSetObservable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DataSetObservable

Kotlin| [Java](../android/database/DataSetObservable.md) 
| --- | --- |

```
open class DataSetObservable : Observable<DataSetObserver!>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.database.Observable](../android/database/Observable.md)\< [android.database.DataSetObserver](../android/database/DataSetObserver.md)\> ||
| | ↳ | [android.database.DataSetObservable](../android/database/DataSetObservable.md) |

A specialization of [Observable](../android/database/Observable.md) for [DataSetObserver](../android/database/DataSetObserver.md) that provides methods for sending notifications to a list of [DataSetObserver](../android/database/DataSetObserver.md) objects.

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------|---|
| [DataSetObservable](../android/database/DataSetObservable.md))`()` <br /> |

| Public methods ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [notifyChanged](../android/database/DataSetObservable.md))`()` Invokes [DataSetObserver.onChanged](../android/database/DataSetObserver.md))on each observer. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [notifyInvalidated](../android/database/DataSetObservable.md))`()` Invokes [DataSetObserver.onInvalidated](../android/database/DataSetObserver.md))on each observer. |

| Inherited functions ||
|---|---|
| From class [Observable](../android/database/Observable.md) |------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerObserver](../android/database/Observable.md))`(`observer:` `T`)` <br /> Adds an observer to the list. The observer cannot be null and it must not already be registered. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unregisterAll](../android/database/Observable.md))`()` <br /> Remove all registered observers. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unregisterObserver](../android/database/Observable.md))`(`observer:` `T`)` <br /> Removes a previously registered observer. The observer must not be null and it must already have been registered. <br /> | ||

| Inherited properties ||
|---|---|
| From class [Observable](../android/database/Observable.md) |-------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [ArrayList](../java/util/ArrayList.md)<T>! | [mObservers](../android/database/Observable.md) <br /> The list of observers. An observer can be in the list at most once and will never be null. <br /> | ||

## Public constructors

### DataSetObservable

```
DataSetObservable()
```

## Public methods

### notifyChanged

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun notifyChanged(): Unit
```

Invokes [DataSetObserver.onChanged](../android/database/DataSetObserver.md))on each observer. Called when the contents of the data set have changed. The recipient will obtain the new contents the next time it queries the data set. 

### notifyInvalidated

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun notifyInvalidated(): Unit
```

Invokes [DataSetObserver.onInvalidated](../android/database/DataSetObserver.md))on each observer. Called when the data set is no longer valid and cannot be queried again, such as when the data set has been closed.
