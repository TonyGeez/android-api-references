# LongToIntFunction

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# LongToIntFunction

```
@FunctionalInterface interface LongToIntFunction
```

| [java.util.function.LongToIntFunction](LongToIntFunction.md) |

Represents a function that accepts a long-valued argument and produces an int-valued result. This is the`long`-to-`int`primitive specialization for [Function](Function.md).

This is a [functional interface](_package.md) whose functional method is [applyAsInt(long)](LongToIntFunction.md)).

## Summary

| Public methods ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [applyAsInt](LongToIntFunction.md))`(`value:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Applies this function to the given argument. |

## Public methods

### applyAsInt

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun applyAsInt(value: Long): Int
```

Applies this function to the given argument.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------|
| `value` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the function argument |

| Return ||
|----------------------------------------------------------------------------|---------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the function result |
