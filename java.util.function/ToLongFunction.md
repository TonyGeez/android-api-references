# ToLongFunction

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ToLongFunction

```
@FunctionalInterface interface ToLongFunction<T : Any!>
```

| [java.util.function.ToLongFunction](https://developer.android.com/reference/kotlin/java/util/function/ToLongFunction#) |

Represents a function that produces a long-valued result. This is the`long`-producing primitive specialization for [Function](https://developer.android.com/reference/kotlin/java/util/function/Function).

This is a [functional interface](https://developer.android.com/reference/kotlin/java/util/function/package-summary) whose functional method is [applyAsLong(java.lang.Object)](https://developer.android.com/reference/kotlin/java/util/function/ToLongFunction#applyAsLong(java.util.function.ToLongFunction.T)).

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [applyAsLong](https://developer.android.com/reference/kotlin/java/util/function/ToLongFunction#applyAsLong(java.util.function.ToLongFunction.T))`(`value:` `T`)` Applies this function to the given argument. |

## Public methods

### applyAsLong

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun applyAsLong(value: T): Long
```

Applies this function to the given argument.

| Parameters ||
|---------|-------------------------|
| `value` | T:the function argument |

| Return ||
|------------------------------------------------------------------------------|---------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the function result |
