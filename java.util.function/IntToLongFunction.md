# IntToLongFunction

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# IntToLongFunction

```
@FunctionalInterface interface IntToLongFunction
```

| [java.util.function.IntToLongFunction](https://developer.android.com/reference/kotlin/java/util/function/IntToLongFunction#) |

Represents a function that accepts an int-valued argument and produces a long-valued result. This is the`int`-to-`long`primitive specialization for [Function](https://developer.android.com/reference/kotlin/java/util/function/Function).

This is a [functional interface](https://developer.android.com/reference/kotlin/java/util/function/package-summary) whose functional method is [applyAsLong(int)](https://developer.android.com/reference/kotlin/java/util/function/IntToLongFunction#applyAsLong(kotlin.Int)).

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [applyAsLong](https://developer.android.com/reference/kotlin/java/util/function/IntToLongFunction#applyAsLong(kotlin.Int))`(`value:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Applies this function to the given argument. |

## Public methods

### applyAsLong

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun applyAsLong(value: Int): Long
```

Applies this function to the given argument.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------|
| `value` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the function argument |

| Return ||
|------------------------------------------------------------------------------|---------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the function result |
