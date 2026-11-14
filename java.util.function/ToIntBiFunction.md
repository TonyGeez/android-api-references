# ToIntBiFunction

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ToIntBiFunction

```
@FunctionalInterface interface ToIntBiFunction<T : Any!, U : Any!>
```

| [java.util.function.ToIntBiFunction](ToIntBiFunction.md) |

Represents a function that accepts two arguments and produces an int-valued result. This is the`int`-producing primitive specialization for [BiFunction](BiFunction.md).

This is a [functional interface](_package.md) whose functional method is [applyAsInt(java.lang.Object,java.lang.Object)](ToIntBiFunction.md)).

## Summary

| Public methods ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [applyAsInt](ToIntBiFunction.md))`(`t:` `T`, `u:` `U`)` Applies this function to the given arguments. |

## Public methods

### applyAsInt

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun applyAsInt(
    t: T, 
    u: U
): Int
```

Applies this function to the given arguments.

| Parameters ||
|-----|--------------------------------|
| `t` | T:the first function argument |
| `u` | U:the second function argument |

| Return ||
|----------------------------------------------------------------------------|---------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the function result |
