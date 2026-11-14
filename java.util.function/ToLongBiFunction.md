Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ToLongBiFunction

```
@FunctionalInterface interface ToLongBiFunction<T : Any!, U : Any!>
```

| [java.util.function.ToLongBiFunction](https://developer.android.com/reference/kotlin/java/util/function/ToLongBiFunction#) |

Represents a function that accepts two arguments and produces a long-valued result. This is the `long`-producing primitive specialization for `https://developer.android.com/reference/kotlin/java/util/function/BiFunction`.

This is a [functional interface](https://developer.android.com/reference/kotlin/java/util/function/package-summary) whose functional method is `https://developer.android.com/reference/kotlin/java/util/function/ToLongBiFunction#applyAsLong(java.util.function.ToLongBiFunction.T,%20java.util.function.ToLongBiFunction.U)`.

## Summary

| Public methods ||
|---|---|
| abstract [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/java/util/function/ToLongBiFunction#applyAsLong(java.util.function.ToLongBiFunction.T,%20java.util.function.ToLongBiFunction.U)(t: T, u: U)` Applies this function to the given arguments. |

## Public methods

### applyAsLong

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun applyAsLong(
    t: T, 
    u: U
): Long
```

Applies this function to the given arguments.

| Parameters ||
|---|---|
| `t` | T: the first function argument |
| `u` | U: the second function argument |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the function result |
