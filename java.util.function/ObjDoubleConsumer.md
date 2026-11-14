# ObjDoubleConsumer

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ObjDoubleConsumer

```
@FunctionalInterface interface ObjDoubleConsumer<T : Any!>
```

| [java.util.function.ObjDoubleConsumer](../java/util/function/ObjDoubleConsumer.md) |

Represents an operation that accepts an object-valued and a`double`-valued argument, and returns no result. This is the`(reference, double)`specialization of [BiConsumer](../java/util/function/BiConsumer.md). Unlike most other functional interfaces,`ObjDoubleConsumer`is expected to operate via side-effects.

This is a [functional interface](../java/util/function/_package.md) whose functional method is [accept(java.lang.Object,double)](../java/util/function/ObjDoubleConsumer.md)).

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [accept](../java/util/function/ObjDoubleConsumer.md))`(`t:` `T`, `value:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`)` Performs this operation on the given arguments. |

## Public methods

### accept

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun accept(
    t: T, 
    value: Double
): Unit
```

Performs this operation on the given arguments.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------|
| `t` | T:the first input argument |
| `value` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html):the second input argument |
