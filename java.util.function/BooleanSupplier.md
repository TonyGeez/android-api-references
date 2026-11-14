# BooleanSupplier

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BooleanSupplier

```
@FunctionalInterface interface BooleanSupplier
```

| [java.util.function.BooleanSupplier](https://developer.android.com/reference/kotlin/java/util/function/BooleanSupplier#) |

Represents a supplier of`boolean`-valued results. This is the`boolean`-producing primitive specialization of [Supplier](https://developer.android.com/reference/kotlin/java/util/function/Supplier).

There is no requirement that a new or distinct result be returned each time the supplier is invoked.

This is a [functional interface](https://developer.android.com/reference/kotlin/java/util/function/package-summary) whose functional method is [getAsBoolean()](https://developer.android.com/reference/kotlin/java/util/function/BooleanSupplier#getAsBoolean()).

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getAsBoolean](https://developer.android.com/reference/kotlin/java/util/function/BooleanSupplier#getAsBoolean())`()` Gets a result. |

## Public methods

### getAsBoolean

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getAsBoolean(): Boolean
```

Gets a result.

| Return ||
|------------------------------------------------------------------------------------|----------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | a result |
