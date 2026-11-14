Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ContentObservable

Kotlin | [Java](ContentObservable.md)
| --- | --- |

```
open class ContentObservable : Observable<ContentObserver!>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.database.Observable](Observable.md)\< [android.database.ContentObserver](ContentObserver.md)\> ||
| | ↳ | [android.database.ContentObservable](ContentObservable.md) |

A specialization of Observable for ContentObserver that provides methods for sending notifications to a list of ContentObserver objects.

## Summary

| Public constructors ||
|---|---|
| ContentObservable <br /> |

| Public methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | dispatchChange Invokes dispatchChange on each observer. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | dispatchChange Invokes dispatchChange on each observer. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | notifyChange Invokes android. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | registerObserver Adds an observer to the list. |

| Inherited functions ||
|---|---|
| From class Observable |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | unregisterAll Remove all registered observers. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | unregisterObserver Removes a previously registered observer. The observer must not be null and it must already have been registered. <br /> | ||

| Inherited properties ||
|---|---|
| From class Observable |---|---| | `https://developer.android.com/reference/kotlin/java/util/ArrayList.html#<T>!` | `https://developer.android.com/reference/kotlin/android/database/Observable#mObservers:java.util.ArrayList` The list of observers. An observer can be in the list at most once and will never be null. <br /> | ||

## Public constructors

### ContentObservable

```
ContentObservable()
```

## Public methods

### dispatchChange

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun dispatchChange(selfChange: Boolean): Unit
```

**Deprecated:** *Use dispatchChange instead.*

Invokes dispatchChange on each observer.

If `selfChange` is true, only delivers the notification to the observer if it has indicated that it wants to receive self-change notifications by implementing deliverSelfNotifications to return true.

| Parameters ||
|---|---|
| `selfChange` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): True if this is a self-change notification. |

### dispatchChange

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun dispatchChange(
    selfChange: Boolean, 
    uri: Uri!
): Unit
```

Invokes dispatchChange on each observer. Includes the changed content Uri when available.

If `selfChange` is true, only delivers the notification to the observer if it has indicated that it wants to receive self-change notifications by implementing deliverSelfNotifications to return true.

| Parameters ||
|---|---|
| `selfChange` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): True if this is a self-change notification. |
| `uri` | [Uri](../android.net/Uri.md)!: The Uri of the changed content, or null if unknown. |

### notifyChange

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun notifyChange(selfChange: Boolean): Unit
```

**Deprecated:** *Use #dispatchChange instead.*

Invokes android.database.ContentObserver#onChange on each observer.

| Parameters ||
|---|---|
| `selfChange` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): True if this is a self-change notification. |

### registerObserver

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun registerObserver(observer: ContentObserver!): Unit
```

Adds an observer to the list. The observer cannot be null and it must not already be registered.

| Parameters ||
|---|---|
| `observer` | [ContentObserver](ContentObserver.md)!: the observer to register |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | the observer is null |
| `java.lang.IllegalStateException` | the observer is already registered |
