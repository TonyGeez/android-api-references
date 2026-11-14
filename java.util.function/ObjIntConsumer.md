# ObjIntConsumer

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ObjIntConsumer

```
@FunctionalInterface interface ObjIntConsumer<T : Any!>
```

| [java.util.function.ObjIntConsumer](https://developer.android.com/reference/kotlin/java/util/function/ObjIntConsumer#) |

Represents an operation that accepts an object-valued and a `int`-valued argument, and returns no result. This is the `(reference, int)` specialization of [BiConsumer](https://developer.android.com/reference/kotlin/java/util/function/BiConsumer). Unlike most other functional interfaces, `ObjIntConsumer` is expected to operate via side-effects.

This is a [functional interface](https://developer.android.com/reference/kotlin/java/util/function/package-summary) whose functional method is [accept(java.lang.Object,int)](https://developer.android.com/reference/kotlin/java/util/function/ObjIntConsumer#accept(java.util.function.ObjIntConsumer.T,%20kotlin.Int)).

## Summary

| Public methods ||
|---------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [accept](https://developer.android.com/reference/kotlin/java/util/function/ObjIntConsumer#accept(java.util.function.ObjIntConsumer.T,%20kotlin.Int))`(`t:` `T`, `value:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Performs this operation on the given arguments. |

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
