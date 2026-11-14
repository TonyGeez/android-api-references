# DoubleSupplier

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DoubleSupplier

```
@FunctionalInterface interface DoubleSupplier
```

| [java.util.function.DoubleSupplier](https://developer.android.com/reference/kotlin/java/util/function/DoubleSupplier#) |

Represents a supplier of`double`-valued results. This is the`double`-producing primitive specialization of [Supplier](https://developer.android.com/reference/kotlin/java/util/function/Supplier).

There is no requirement that a distinct result be returned each time the supplier is invoked.

This is a [functional interface](https://developer.android.com/reference/kotlin/java/util/function/package-summary) whose functional method is [getAsDouble()](https://developer.android.com/reference/kotlin/java/util/function/DoubleSupplier#getAsDouble()).

## Summary

| Public methods ||
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| abstract [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [getAsDouble](https://developer.android.com/reference/kotlin/java/util/function/DoubleSupplier#getAsDouble())`()` Gets a result. |

## Public methods

### getAsDouble

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getAsDouble(): Double
```

Gets a result.

| Return ||
|----------------------------------------------------------------------------------|----------|
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | a result |
