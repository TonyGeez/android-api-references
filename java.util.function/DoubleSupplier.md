# DoubleSupplier

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DoubleSupplier

```
@FunctionalInterface interface DoubleSupplier
```

| [java.util.function.DoubleSupplier](DoubleSupplier.md) |

Represents a supplier of`double`-valued results. This is the`double`-producing primitive specialization of [Supplier](Supplier.md).

There is no requirement that a distinct result be returned each time the supplier is invoked.

This is a [functional interface](_package.md) whose functional method is [getAsDouble()](DoubleSupplier.md)).

## Summary

| Public methods ||
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| abstract [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [getAsDouble](DoubleSupplier.md))`()` Gets a result. |

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
