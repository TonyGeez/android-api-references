# EntityIterator

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# EntityIterator

Kotlin| [Java](../android/content/EntityIterator.md) 
| --- | --- |

```
interface EntityIterator : MutableIterator<Entity!>
```

| [android.content.EntityIterator](../android/content/EntityIterator.md) |

A specialization of [Iterator](../java/util/Iterator.md) that allows iterating over a collection of [Entity](../android/content/Entity.md) objects. In addition to the iteration functionality it also allows resetting the iterator back to the beginning and provides for an explicit [close()](../android/content/EntityIterator.md))method to indicate that the iterator is no longer needed and that its resources can be released.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](../android/content/EntityIterator.md))`()` Indicates that this iterator is no longer needed and that any associated resources may be released (such as a SQLite cursor). |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [reset](../android/content/EntityIterator.md))`()` Reset the iterator back to the beginning. |

## Public methods

### close

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun close(): Unit
```

Indicates that this iterator is no longer needed and that any associated resources may be released (such as a SQLite cursor). 

### reset

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun reset(): Unit
```

Reset the iterator back to the beginning.
