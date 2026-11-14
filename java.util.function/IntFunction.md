# IntFunction

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# IntFunction

```
@FunctionalInterface interface IntFunction<R : Any!>
```

| [java.util.function.IntFunction](../java/util/function/IntFunction.md) |

Represents a function that accepts an int-valued argument and produces a result. This is the`int`-consuming primitive specialization for [Function](../java/util/function/Function.md).

This is a [functional interface](../java/util/function/_package.md) whose functional method is [apply(int)](../java/util/function/IntFunction.md)).

## Summary

| Public methods ||
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstractR | [apply](../java/util/function/IntFunction.md))`(`value:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Applies this function to the given argument. |

## Public methods

### apply

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun apply(value: Int): R
```

Applies this function to the given argument.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------|
| `value` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the function argument |

| Return ||
|---|---------------------|
| R | the function result |
