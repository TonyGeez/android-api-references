# ToIntFunction

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ToIntFunction

```
@FunctionalInterface interface ToIntFunction<T : Any!>
```

| [java.util.function.ToIntFunction](ToIntFunction.md) |

Represents a function that produces an int-valued result. This is the`int`-producing primitive specialization for [Function](Function.md).

This is a [functional interface](_package.md) whose functional method is [applyAsInt(java.lang.Object)](ToIntFunction.md)).

## Summary

| Public methods ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [applyAsInt](ToIntFunction.md))`(`value:` `T`)` Applies this function to the given argument. |

## Public methods

### applyAsInt

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun applyAsInt(value: T): Int
```

Applies this function to the given argument.

| Parameters ||
|---------|-------------------------|
| `value` | T:the function argument |

| Return ||
|----------------------------------------------------------------------------|---------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the function result |
