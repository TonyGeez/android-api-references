# LongFunction

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# LongFunction

```
@FunctionalInterface interface LongFunction<R : Any!>
```

| [java.util.function.LongFunction](https://developer.android.com/reference/kotlin/java/util/function/LongFunction#) |

Represents a function that accepts a long-valued argument and produces a result. This is the`long`-consuming primitive specialization for [Function](https://developer.android.com/reference/kotlin/java/util/function/Function).

This is a [functional interface](https://developer.android.com/reference/kotlin/java/util/function/package-summary) whose functional method is [apply(long)](https://developer.android.com/reference/kotlin/java/util/function/LongFunction#apply(kotlin.Long)).

## Summary

| Public methods ||
|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstractR | [apply](https://developer.android.com/reference/kotlin/java/util/function/LongFunction#apply(kotlin.Long))`(`value:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Applies this function to the given argument. |

## Public methods

### apply

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun apply(value: Long): R
```

Applies this function to the given argument.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------|
| `value` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the function argument |

| Return ||
|---|---------------------|
| R | the function result |
