Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BiConsumer

```
@FunctionalInterface interface BiConsumer<T : Any!, U : Any!>
```

| [java.util.function.BiConsumer](BiConsumer.md) |

Represents an operation that accepts two input arguments and returns no result. This is the two-arity specialization of Consumer. Unlike most other functional interfaces, `BiConsumer` is expected to operate via side-effects.

This is a [functional interface](_package.md) whose functional method is accept.

## Summary

| Public methods ||
|---|---|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | accept Performs this operation on the given arguments. |
| open [BiConsumer](BiConsumer.md)\<T, U\>! | andThen Returns a composed `BiConsumer` that performs, in sequence, this operation followed by the `after` operation. |

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
| `after` | [BiConsumer](BiConsumer.md)\<in T, in U\>!: the operation to perform after this operation |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/function/BiConsumer#<T, U>!` | a composed `BiConsumer` that performs in sequence this operation followed by the `after` operation |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if `after` is null |
