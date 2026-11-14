# Iterable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Iterable

```
interface Iterable<T : Any!>
```

| [java.lang.Iterable](https://developer.android.com/reference/kotlin/java/lang/Iterable#) |

Implementing this interface allows an object to be the target of the enhanced`for`statement (sometimes called the "for-each loop" statement).

## Summary

| Public methods ||
|------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [forEach](https://developer.android.com/reference/kotlin/java/lang/Iterable#forEach(java.util.function.Consumer))`(`action:` ` [Consumer](https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#)<in` `T>`)` Performs the given action for each element of the`Iterable`until all elements have been processed or the action throws an exception. |
| abstract [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)\<T\> | [iterator](https://developer.android.com/reference/kotlin/java/lang/Iterable#iterator())`()` Returns an iterator over elements of type`T`. |
| open [Spliterator](https://developer.android.com/reference/kotlin/java/util/Spliterator.html#)\<T\> | [spliterator](https://developer.android.com/reference/kotlin/java/lang/Iterable#spliterator())`()` Creates a [Spliterator](https://developer.android.com/reference/kotlin/java/util/Spliterator.html#) over the elements described by this`Iterable`. |

## Public methods

### forEach

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun forEach(action: Consumer<in T>): Unit
```

Performs the given action for each element of the`Iterable`until all elements have been processed or the action throws an exception. Actions are performed in the order of iteration, if that order is specified. Exceptions thrown by the action are relayed to the caller.

The behavior of this method is unspecified if the action performs side-effects that modify the underlying source of elements, unless an overriding class has specified a concurrent modification policy.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| `action` | [Consumer](https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#)\<inT\>:The action to be performed for each element |

| Exceptions ||
|----------------------------------|---------------------------------|
| `java.lang.NullPointerException` | if the specified action is null |

### iterator

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun iterator(): MutableIterator<T>
```

Returns an iterator over elements of type`T`.

| Return ||
|--------------------------------------------------------------------------------------------------------------------|--------------|
| [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)<T> | an Iterator. |

### spliterator

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun spliterator(): Spliterator<T>
```

Creates a [Spliterator](https://developer.android.com/reference/kotlin/java/util/Spliterator.html#) over the elements described by this`Iterable`.

| Return ||
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| [Spliterator](https://developer.android.com/reference/kotlin/java/util/Spliterator.html#)<T> | a`Spliterator`over the elements described by this`Iterable`. |
