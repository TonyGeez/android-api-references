# EntityIterator

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# EntityIterator

Kotlin| [Java](EntityIterator.md) 
| --- | --- |

```
interface EntityIterator : MutableIterator<Entity!>
```

| [android.content.EntityIterator](EntityIterator.md) |

A specialization of [Iterator](../java.util/Iterator.md) that allows iterating over a collection of [Entity](Entity.md) objects. In addition to the iteration functionality it also allows resetting the iterator back to the beginning and provides for an explicit [close()](EntityIterator.md))method to indicate that the iterator is no longer needed and that its resources can be released.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](EntityIterator.md))`()` Indicates that this iterator is no longer needed and that any associated resources may be released (such as a SQLite cursor). |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [reset](EntityIterator.md))`()` Reset the iterator back to the beginning. |

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
