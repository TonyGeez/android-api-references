Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# UnaryOperator

```
@FunctionalInterface interface UnaryOperator<T : Any!> : Function<T, T>
```

| [java.util.function.UnaryOperator](../java/util/function/UnaryOperator.md) |

Represents an operation on a single operand that produces a result of the same type as its operand. This is a specialization of `Function` for the case where the operand and result are of the same type.

This is a [functional interface](../java/util/function/_package.md) whose functional method is `https://developer.android.com/reference/kotlin/java/util/function/Function#apply(java.util.function.Function.T)`.

## Summary

| Public methods ||
|---|---|
| open static [UnaryOperator](../java/util/function/UnaryOperator.md)\<T\>! | `https://developer.android.com/reference/kotlin/java/util/function/UnaryOperator#identity()()` Returns a unary operator that always returns its input argument. |

| Inherited functions ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/java/util/function/Function` |---|---| | `https://developer.android.com/reference/kotlin/java/util/function/Function<T, V>!` | `https://developer.android.com/reference/kotlin/java/util/function/Function#andThen(java.util.function.Function)(after: https://developer.android.com/reference/kotlin/java/util/function/Function<in R, out V>!)` Returns a composed function that first applies this function to its input, and then applies the `after` function to the result. If evaluation of either function throws an exception, it is relayed to the caller of the composed function. <br /> | | `R` | `https://developer.android.com/reference/kotlin/java/util/function/Function#apply(java.util.function.Function.T)(t: T)` Applies this function to the given argument. <br /> | | `https://developer.android.com/reference/kotlin/java/util/function/Function<V, R>!` | `https://developer.android.com/reference/kotlin/java/util/function/Function#compose(java.util.function.Function)(before: https://developer.android.com/reference/kotlin/java/util/function/Function<in V, out T>!)` Returns a composed function that first applies the `before` function to its input, and then applies this function to the result. If evaluation of either function throws an exception, it is relayed to the caller of the composed function. <br /> | ||

## Public methods

### identity

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun <T : Any!> identity(): UnaryOperator<T>!
```

Returns a unary operator that always returns its input argument.

| Parameters ||
|---|---|
| `<T>` | the type of the input and output of the operator |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/function/UnaryOperator#<T>!` | a unary operator that always returns its input argument |
