# IntSupplier

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# IntSupplier

```
@FunctionalInterface interface IntSupplier
```

| [java.util.function.IntSupplier](https://developer.android.com/reference/kotlin/java/util/function/IntSupplier#) |

Represents a supplier of`int`-valued results. This is the`int`-producing primitive specialization of [Supplier](https://developer.android.com/reference/kotlin/java/util/function/Supplier).

There is no requirement that a distinct result be returned each time the supplier is invoked.

This is a [functional interface](https://developer.android.com/reference/kotlin/java/util/function/package-summary) whose functional method is [getAsInt()](https://developer.android.com/reference/kotlin/java/util/function/IntSupplier#getAsInt()).

## Summary

| Public methods ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getAsInt](https://developer.android.com/reference/kotlin/java/util/function/IntSupplier#getAsInt())`()` Gets a result. |

## Public methods

### getAsInt

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getAsInt(): Int
```

Gets a result.

| Return ||
|----------------------------------------------------------------------------|----------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a result |
