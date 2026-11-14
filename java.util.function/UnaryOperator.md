Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# UnaryOperator

```
@FunctionalInterface interface UnaryOperator<T : Any!> : Function<T, T>
```

| [java.util.function.UnaryOperator](UnaryOperator.md) |

Represents an operation on a single operand that produces a result of the same type as its operand. This is a specialization of `Function` for the case where the operand and result are of the same type.

This is a [functional interface](_package.md) whose functional method is apply.

## Summary

| Public methods ||
|---|---|
| open static [UnaryOperator](UnaryOperator.md)\<T\>! | identity Returns a unary operator that always returns its input argument. |

| Inherited functions ||
|---|---|
| From class Function |---|---| | `https://developer.android.com/reference/kotlin/java/util/function/Function<T, V>!` | andThen Returns a composed function that first applies this function to its input, and then applies the `after` function to the result. If evaluation of either function throws an exception, it is relayed to the caller of the composed function. <br /> | | `R` | apply Applies this function to the given argument. <br /> | | `https://developer.android.com/reference/kotlin/java/util/function/Function<V, R>!` | compose Returns a composed function that first applies the `before` function to its input, and then applies this function to the result. If evaluation of either function throws an exception, it is relayed to the caller of the composed function. <br /> | ||

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
