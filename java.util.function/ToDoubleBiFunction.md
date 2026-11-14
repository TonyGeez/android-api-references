# ToDoubleBiFunction

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ToDoubleBiFunction

```
@FunctionalInterface interface ToDoubleBiFunction<T : Any!, U : Any!>
```

| [java.util.function.ToDoubleBiFunction](https://developer.android.com/reference/kotlin/java/util/function/ToDoubleBiFunction#) |

Represents a function that accepts two arguments and produces a double-valued result. This is the`double`-producing primitive specialization for [BiFunction](https://developer.android.com/reference/kotlin/java/util/function/BiFunction).

This is a [functional interface](https://developer.android.com/reference/kotlin/java/util/function/package-summary) whose functional method is [applyAsDouble(java.lang.Object,java.lang.Object)](https://developer.android.com/reference/kotlin/java/util/function/ToDoubleBiFunction#applyAsDouble(java.util.function.ToDoubleBiFunction.T,%20java.util.function.ToDoubleBiFunction.U)).

## Summary

| Public methods ||
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [applyAsDouble](https://developer.android.com/reference/kotlin/java/util/function/ToDoubleBiFunction#applyAsDouble(java.util.function.ToDoubleBiFunction.T,%20java.util.function.ToDoubleBiFunction.U))`(`t:` `T`, `u:` `U`)` Applies this function to the given arguments. |

## Public methods

### applyAsDouble

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun applyAsDouble(
    t: T, 
    u: U
): Double
```

Applies this function to the given arguments.

| Parameters ||
|-----|--------------------------------|
| `t` | T:the first function argument |
| `u` | U:the second function argument |

| Return ||
|----------------------------------------------------------------------------------|---------------------|
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | the function result |
