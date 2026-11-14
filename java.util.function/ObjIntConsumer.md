# ObjIntConsumer

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ObjIntConsumer

```
@FunctionalInterface interface ObjIntConsumer<T : Any!>
```

| [java.util.function.ObjIntConsumer](ObjIntConsumer.md) |

Represents an operation that accepts an object-valued and a `int`-valued argument, and returns no result. This is the `(reference, int)` specialization of [BiConsumer](BiConsumer.md). Unlike most other functional interfaces, `ObjIntConsumer` is expected to operate via side-effects.

This is a [functional interface](_package.md) whose functional method is [accept(java.lang.Object,int)](ObjIntConsumer.md)).

## Summary

| Public methods ||
|---------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [accept](ObjIntConsumer.md))`(`t:` `T`, `value:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Performs this operation on the given arguments. |

## Public methods

### accept

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun accept(
    t: T, 
    value: Int
): Unit
```

Performs this operation on the given arguments.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------|
| `t` | T: the first input argument |
| `value` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the second input argument |
