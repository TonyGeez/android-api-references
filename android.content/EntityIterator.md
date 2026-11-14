# EntityIterator

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# EntityIterator

Kotlin| [Java](https://developer.android.com/reference/android/content/EntityIterator "View this page in Java") 

```
interface EntityIterator : MutableIterator<Entity!>
```

| [android.content.EntityIterator](https://developer.android.com/reference/kotlin/android/content/EntityIterator#) |

A specialization of [Iterator](https://developer.android.com/reference/kotlin/java/util/Iterator.html#) that allows iterating over a collection of [Entity](https://developer.android.com/reference/kotlin/android/content/Entity) objects. In addition to the iteration functionality it also allows resetting the iterator back to the beginning and provides for an explicit [close()](https://developer.android.com/reference/kotlin/android/content/EntityIterator#close())method to indicate that the iterator is no longer needed and that its resources can be released.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](https://developer.android.com/reference/kotlin/android/content/EntityIterator#close())`()` Indicates that this iterator is no longer needed and that any associated resources may be released (such as a SQLite cursor). |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [reset](https://developer.android.com/reference/kotlin/android/content/EntityIterator#reset())`()` Reset the iterator back to the beginning. |

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
