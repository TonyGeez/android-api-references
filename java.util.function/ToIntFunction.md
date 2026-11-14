# ToIntFunction

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ToIntFunction

```
@FunctionalInterface interface ToIntFunction<T : Any!>
```

| [java.util.function.ToIntFunction](https://developer.android.com/reference/kotlin/java/util/function/ToIntFunction#) |

Represents a function that produces an int-valued result. This is the`int`-producing primitive specialization for [Function](https://developer.android.com/reference/kotlin/java/util/function/Function).

This is a [functional interface](https://developer.android.com/reference/kotlin/java/util/function/package-summary) whose functional method is [applyAsInt(java.lang.Object)](https://developer.android.com/reference/kotlin/java/util/function/ToIntFunction#applyAsInt(java.util.function.ToIntFunction.T)).

## Summary

| Public methods ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [applyAsInt](https://developer.android.com/reference/kotlin/java/util/function/ToIntFunction#applyAsInt(java.util.function.ToIntFunction.T))`(`value:` `T`)` Applies this function to the given argument. |

## Public methods

### applyAsInt

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun applyAsInt(value: T): Int
```

Applies this function to the given argument.

| Parameters ||
|---------|-------------------------|
| `value` | T:the function argument |

| Return ||
|----------------------------------------------------------------------------|---------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the function result |
