# ObjLongConsumer

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ObjLongConsumer

```
@FunctionalInterface interface ObjLongConsumer<T : Any!>
```

| [java.util.function.ObjLongConsumer](ObjLongConsumer.md) |

Represents an operation that accepts an object-valued and a`long`-valued argument, and returns no result. This is the`(reference, long)`specialization of [BiConsumer](BiConsumer.md). Unlike most other functional interfaces,`ObjLongConsumer`is expected to operate via side-effects.

This is a [functional interface](_package.md) whose functional method is [accept(java.lang.Object,long)](ObjLongConsumer.md)).

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [accept](ObjLongConsumer.md))`(`t:` `T`, `value:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Performs this operation on the given arguments. |

## Public methods

### accept

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun accept(
    t: T, 
    value: Long
): Unit
```

Performs this operation on the given arguments.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------|
| `t` | T:the first input argument |
| `value` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the second input argument |
