# LongToDoubleFunction

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# LongToDoubleFunction

```
@FunctionalInterface interface LongToDoubleFunction
```

| [java.util.function.LongToDoubleFunction](../java/util/function/LongToDoubleFunction.md) |

Represents a function that accepts a long-valued argument and produces a double-valued result. This is the`long`-to-`double`primitive specialization for [Function](../java/util/function/Function.md).

This is a [functional interface](../java/util/function/_package.md) whose functional method is [applyAsDouble(long)](../java/util/function/LongToDoubleFunction.md)).

## Summary

| Public methods ||
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [applyAsDouble](../java/util/function/LongToDoubleFunction.md))`(`value:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Applies this function to the given argument. |

## Public methods

### applyAsDouble

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun applyAsDouble(value: Long): Double
```

Applies this function to the given argument.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------|
| `value` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the function argument |

| Return ||
|----------------------------------------------------------------------------------|---------------------|
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | the function result |
