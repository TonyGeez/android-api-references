# ObjLongConsumer

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ObjLongConsumer

```
@FunctionalInterface interface ObjLongConsumer<T : Any!>
```

| [java.util.function.ObjLongConsumer](https://developer.android.com/reference/kotlin/java/util/function/ObjLongConsumer#) |

Represents an operation that accepts an object-valued and a`long`-valued argument, and returns no result. This is the`(reference, long)`specialization of [BiConsumer](https://developer.android.com/reference/kotlin/java/util/function/BiConsumer). Unlike most other functional interfaces,`ObjLongConsumer`is expected to operate via side-effects.

This is a [functional interface](https://developer.android.com/reference/kotlin/java/util/function/package-summary) whose functional method is [accept(java.lang.Object,long)](https://developer.android.com/reference/kotlin/java/util/function/ObjLongConsumer#accept(java.util.function.ObjLongConsumer.T,%20kotlin.Long)).

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [accept](https://developer.android.com/reference/kotlin/java/util/function/ObjLongConsumer#accept(java.util.function.ObjLongConsumer.T,%20kotlin.Long))`(`t:` `T`, `value:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Performs this operation on the given arguments. |

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
