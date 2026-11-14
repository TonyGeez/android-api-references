# DoubleFunction

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DoubleFunction

```
@FunctionalInterface interface DoubleFunction<R : Any!>
```

| [java.util.function.DoubleFunction](https://developer.android.com/reference/kotlin/java/util/function/DoubleFunction#) |

Represents a function that accepts a double-valued argument and produces a result. This is the`double`-consuming primitive specialization for [Function](https://developer.android.com/reference/kotlin/java/util/function/Function).

This is a [functional interface](https://developer.android.com/reference/kotlin/java/util/function/package-summary) whose functional method is [apply(double)](https://developer.android.com/reference/kotlin/java/util/function/DoubleFunction#apply(kotlin.Double)).

## Summary

| Public methods ||
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstractR | [apply](https://developer.android.com/reference/kotlin/java/util/function/DoubleFunction#apply(kotlin.Double))`(`value:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`)` Applies this function to the given argument. |

## Public methods

### apply

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun apply(value: Double): R
```

Applies this function to the given argument.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------|
| `value` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html):the function argument |

| Return ||
|---|---------------------|
| R | the function result |
