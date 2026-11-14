# ObjDoubleConsumer

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ObjDoubleConsumer

```
@FunctionalInterface interface ObjDoubleConsumer<T : Any!>
```

| [java.util.function.ObjDoubleConsumer](https://developer.android.com/reference/kotlin/java/util/function/ObjDoubleConsumer#) |

Represents an operation that accepts an object-valued and a`double`-valued argument, and returns no result. This is the`(reference, double)`specialization of [BiConsumer](https://developer.android.com/reference/kotlin/java/util/function/BiConsumer). Unlike most other functional interfaces,`ObjDoubleConsumer`is expected to operate via side-effects.

This is a [functional interface](https://developer.android.com/reference/kotlin/java/util/function/package-summary) whose functional method is [accept(java.lang.Object,double)](https://developer.android.com/reference/kotlin/java/util/function/ObjDoubleConsumer#accept(java.util.function.ObjDoubleConsumer.T,%20kotlin.Double)).

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [accept](https://developer.android.com/reference/kotlin/java/util/function/ObjDoubleConsumer#accept(java.util.function.ObjDoubleConsumer.T,%20kotlin.Double))`(`t:` `T`, `value:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`)` Performs this operation on the given arguments. |

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
