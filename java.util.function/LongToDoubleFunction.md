# LongToDoubleFunction

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# LongToDoubleFunction

```
@FunctionalInterface interface LongToDoubleFunction
```

| [java.util.function.LongToDoubleFunction](https://developer.android.com/reference/kotlin/java/util/function/LongToDoubleFunction#) |

Represents a function that accepts a long-valued argument and produces a double-valued result. This is the`long`-to-`double`primitive specialization for [Function](https://developer.android.com/reference/kotlin/java/util/function/Function).

This is a [functional interface](https://developer.android.com/reference/kotlin/java/util/function/package-summary) whose functional method is [applyAsDouble(long)](https://developer.android.com/reference/kotlin/java/util/function/LongToDoubleFunction#applyAsDouble(kotlin.Long)).

## Summary

| Public methods ||
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [applyAsDouble](https://developer.android.com/reference/kotlin/java/util/function/LongToDoubleFunction#applyAsDouble(kotlin.Long))`(`value:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Applies this function to the given argument. |

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
