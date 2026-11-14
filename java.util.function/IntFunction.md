# IntFunction

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# IntFunction

```
@FunctionalInterface interface IntFunction<R : Any!>
```

| [java.util.function.IntFunction](https://developer.android.com/reference/kotlin/java/util/function/IntFunction#) |

Represents a function that accepts an int-valued argument and produces a result. This is the`int`-consuming primitive specialization for [Function](https://developer.android.com/reference/kotlin/java/util/function/Function).

This is a [functional interface](https://developer.android.com/reference/kotlin/java/util/function/package-summary) whose functional method is [apply(int)](https://developer.android.com/reference/kotlin/java/util/function/IntFunction#apply(kotlin.Int)).

## Summary

| Public methods ||
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstractR | [apply](https://developer.android.com/reference/kotlin/java/util/function/IntFunction#apply(kotlin.Int))`(`value:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Applies this function to the given argument. |

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
