Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BiConsumer

```
@FunctionalInterface interface BiConsumer<T : Any!, U : Any!>
```

| [java.util.function.BiConsumer](../java/util/function/BiConsumer.md) |

Represents an operation that accepts two input arguments and returns no result. This is the two-arity specialization of `https://developer.android.com/reference/kotlin/java/util/function/Consumer`. Unlike most other functional interfaces, `BiConsumer` is expected to operate via side-effects.

This is a [functional interface](../java/util/function/_package.md) whose functional method is `https://developer.android.com/reference/kotlin/java/util/function/BiConsumer#accept(java.util.function.BiConsumer.T,%20java.util.function.BiConsumer.U)`.

## Summary

| Public methods ||
|---|---|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/util/function/BiConsumer#accept(java.util.function.BiConsumer.T,%20java.util.function.BiConsumer.U)(t: T, u: U)` Performs this operation on the given arguments. |
| open [BiConsumer](../java/util/function/BiConsumer.md)\<T, U\>! | `https://developer.android.com/reference/kotlin/java/util/function/BiConsumer#andThen(java.util.function.BiConsumer)(after: https://developer.android.com/reference/kotlin/java/util/function/BiConsumer#<in T, in U>!)` Returns a composed `BiConsumer` that performs, in sequence, this operation followed by the `after` operation. |

## Public methods

### accept

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun accept(
    t: T, 
    u: U
): Unit
```

Performs this operation on the given arguments.

| Parameters ||
|---|---|
| `t` | T: the first input argument |
| `u` | U: the second input argument |

### andThen

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun andThen(after: BiConsumer<in T, in U>!): BiConsumer<T, U>!
```

Returns a composed `BiConsumer` that performs, in sequence, this operation followed by the `after` operation. If performing either operation throws an exception, it is relayed to the caller of the composed operation. If performing this operation throws an exception, the `after` operation will not be performed.

| Parameters ||
|---|---|
| `after` | [BiConsumer](../java/util/function/BiConsumer.md)\<in T, in U\>!: the operation to perform after this operation |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/function/BiConsumer#<T, U>!` | a composed `BiConsumer` that performs in sequence this operation followed by the `after` operation |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if `after` is null |
