# ToDoubleFunction

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ToDoubleFunction

```
@FunctionalInterface interface ToDoubleFunction<T : Any!>
```

| [java.util.function.ToDoubleFunction](ToDoubleFunction.md) |

Represents a function that produces a double-valued result. This is the`double`-producing primitive specialization for [Function](Function.md).

This is a [functional interface](_package.md) whose functional method is [applyAsDouble(java.lang.Object)](ToDoubleFunction.md)).

## Summary

| Public methods ||
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [applyAsDouble](ToDoubleFunction.md))`(`value:` `T`)` Applies this function to the given argument. |

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
