# DataSetObservable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DataSetObservable

Kotlin| [Java](https://developer.android.com/reference/android/database/DataSetObservable "View this page in Java") 

```
open class DataSetObservable : Observable<DataSetObserver!>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| ↳ | [android.database.Observable](https://developer.android.com/reference/kotlin/android/database/Observable)\< [android.database.DataSetObserver](https://developer.android.com/reference/kotlin/android/database/DataSetObserver)\> ||
| | ↳ | [android.database.DataSetObservable](https://developer.android.com/reference/kotlin/android/database/DataSetObservable#) |

A specialization of [Observable](https://developer.android.com/reference/kotlin/android/database/Observable) for [DataSetObserver](https://developer.android.com/reference/kotlin/android/database/DataSetObserver) that provides methods for sending notifications to a list of [DataSetObserver](https://developer.android.com/reference/kotlin/android/database/DataSetObserver) objects.

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------|---|
| [DataSetObservable](https://developer.android.com/reference/kotlin/android/database/DataSetObservable#DataSetObservable())`()` <br /> |

| Public methods ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [notifyChanged](https://developer.android.com/reference/kotlin/android/database/DataSetObservable#notifyChanged())`()` Invokes [DataSetObserver.onChanged](https://developer.android.com/reference/kotlin/android/database/DataSetObserver#onChanged())on each observer. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [notifyInvalidated](https://developer.android.com/reference/kotlin/android/database/DataSetObservable#notifyInvalidated())`()` Invokes [DataSetObserver.onInvalidated](https://developer.android.com/reference/kotlin/android/database/DataSetObserver#onInvalidated())on each observer. |

| Inherited functions ||
|---|---|
| From class [Observable](https://developer.android.com/reference/kotlin/android/database/Observable) |------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerObserver](https://developer.android.com/reference/kotlin/android/database/Observable#registerObserver(android.database.Observable.T))`(`observer:` `T`)` <br /> Adds an observer to the list. The observer cannot be null and it must not already be registered. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unregisterAll](https://developer.android.com/reference/kotlin/android/database/Observable#unregisterAll())`()` <br /> Remove all registered observers. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unregisterObserver](https://developer.android.com/reference/kotlin/android/database/Observable#unregisterObserver(android.database.Observable.T))`(`observer:` `T`)` <br /> Removes a previously registered observer. The observer must not be null and it must already have been registered. <br /> | ||

| Inherited properties ||
|---|---|
| From class [Observable](https://developer.android.com/reference/kotlin/android/database/Observable) |-------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [ArrayList](https://developer.android.com/reference/kotlin/java/util/ArrayList.html#)<T>! | [mObservers](https://developer.android.com/reference/kotlin/android/database/Observable#mObservers:java.util.ArrayList) <br /> The list of observers. An observer can be in the list at most once and will never be null. <br /> | ||

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

Invokes [DataSetObserver.onChanged](https://developer.android.com/reference/kotlin/android/database/DataSetObserver#onChanged())on each observer. Called when the contents of the data set have changed. The recipient will obtain the new contents the next time it queries the data set. 

### notifyInvalidated

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun notifyInvalidated(): Unit
```

Invokes [DataSetObserver.onInvalidated](https://developer.android.com/reference/kotlin/android/database/DataSetObserver#onInvalidated())on each observer. Called when the data set is no longer valid and cannot be queried again, such as when the data set has been closed.
