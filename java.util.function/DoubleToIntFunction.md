# DoubleToIntFunction

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DoubleToIntFunction

```
@FunctionalInterface interface DoubleToIntFunction
```

| [java.util.function.DoubleToIntFunction](DoubleToIntFunction.md) |

Represents a function that accepts a double-valued argument and produces an int-valued result. This is the`double`-to-`int`primitive specialization for [Function](Function.md).

This is a [functional interface](_package.md) whose functional method is [applyAsInt(double)](DoubleToIntFunction.md)).

## Summary

| Public methods ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [applyAsInt](DoubleToIntFunction.md))`(`value:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`)` Applies this function to the given argument. |

## Public methods

### applyAsInt

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun applyAsInt(value: Double): Int
```

Applies this function to the given argument.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------|
| `value` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html):the function argument |

| Return ||
|----------------------------------------------------------------------------|---------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the function result |
