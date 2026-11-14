# DoubleToLongFunction

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DoubleToLongFunction

```
@FunctionalInterface interface DoubleToLongFunction
```

| [java.util.function.DoubleToLongFunction](https://developer.android.com/reference/kotlin/java/util/function/DoubleToLongFunction#) |

Represents a function that accepts a double-valued argument and produces a long-valued result. This is the`double`-to-`long`primitive specialization for [Function](https://developer.android.com/reference/kotlin/java/util/function/Function).

This is a [functional interface](https://developer.android.com/reference/kotlin/java/util/function/package-summary) whose functional method is [applyAsLong(double)](https://developer.android.com/reference/kotlin/java/util/function/DoubleToLongFunction#applyAsLong(kotlin.Double)).

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [applyAsLong](https://developer.android.com/reference/kotlin/java/util/function/DoubleToLongFunction#applyAsLong(kotlin.Double))`(`value:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`)` Applies this function to the given argument. |

## Public methods

### applyAsLong

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun applyAsLong(value: Double): Long
```

Applies this function to the given argument.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------|
| `value` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html):the function argument |

| Return ||
|------------------------------------------------------------------------------|---------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the function result |
