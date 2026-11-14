# LongFunction

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# LongFunction

```
@FunctionalInterface interface LongFunction<R : Any!>
```

| [java.util.function.LongFunction](LongFunction.md) |

Represents a function that accepts a long-valued argument and produces a result. This is the`long`-consuming primitive specialization for [Function](Function.md).

This is a [functional interface](_package.md) whose functional method is [apply(long)](LongFunction.md)).

## Summary

| Public methods ||
|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstractR | [apply](LongFunction.md))`(`value:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Applies this function to the given argument. |

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
