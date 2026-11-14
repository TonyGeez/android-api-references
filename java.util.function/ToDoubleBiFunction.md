# ToDoubleBiFunction

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ToDoubleBiFunction

```
@FunctionalInterface interface ToDoubleBiFunction<T : Any!, U : Any!>
```

| [java.util.function.ToDoubleBiFunction](ToDoubleBiFunction.md) |

Represents a function that accepts two arguments and produces a double-valued result. This is the`double`-producing primitive specialization for [BiFunction](BiFunction.md).

This is a [functional interface](_package.md) whose functional method is [applyAsDouble(java.lang.Object,java.lang.Object)](ToDoubleBiFunction.md)).

## Summary

| Public methods ||
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [applyAsDouble](ToDoubleBiFunction.md))`(`t:` `T`, `u:` `U`)` Applies this function to the given arguments. |

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
