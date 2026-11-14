# ToDoubleFunction

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ToDoubleFunction

```
@FunctionalInterface interface ToDoubleFunction<T : Any!>
```

| [java.util.function.ToDoubleFunction](https://developer.android.com/reference/kotlin/java/util/function/ToDoubleFunction#) |

Represents a function that produces a double-valued result. This is the`double`-producing primitive specialization for [Function](https://developer.android.com/reference/kotlin/java/util/function/Function).

This is a [functional interface](https://developer.android.com/reference/kotlin/java/util/function/package-summary) whose functional method is [applyAsDouble(java.lang.Object)](https://developer.android.com/reference/kotlin/java/util/function/ToDoubleFunction#applyAsDouble(java.util.function.ToDoubleFunction.T)).

## Summary

| Public methods ||
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [applyAsDouble](https://developer.android.com/reference/kotlin/java/util/function/ToDoubleFunction#applyAsDouble(java.util.function.ToDoubleFunction.T))`(`value:` `T`)` Applies this function to the given argument. |

## Public methods

### applyAsDouble

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun applyAsDouble(value: T): Double
```

Applies this function to the given argument.

| Parameters ||
|---------|-------------------------|
| `value` | T:the function argument |

| Return ||
|----------------------------------------------------------------------------------|---------------------|
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | the function result |
