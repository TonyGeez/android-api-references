# DoubleFunction

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DoubleFunction

```
@FunctionalInterface interface DoubleFunction<R : Any!>
```

| [java.util.function.DoubleFunction](../java/util/function/DoubleFunction.md) |

Represents a function that accepts a double-valued argument and produces a result. This is the`double`-consuming primitive specialization for [Function](../java/util/function/Function.md).

This is a [functional interface](../java/util/function/_package.md) whose functional method is [apply(double)](../java/util/function/DoubleFunction.md)).

## Summary

| Public methods ||
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstractR | [apply](../java/util/function/DoubleFunction.md))`(`value:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`)` Applies this function to the given argument. |

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
