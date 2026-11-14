# BooleanSupplier

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BooleanSupplier

```
@FunctionalInterface interface BooleanSupplier
```

| [java.util.function.BooleanSupplier](../java/util/function/BooleanSupplier.md) |

Represents a supplier of`boolean`-valued results. This is the`boolean`-producing primitive specialization of [Supplier](../java/util/function/Supplier.md).

There is no requirement that a new or distinct result be returned each time the supplier is invoked.

This is a [functional interface](../java/util/function/_package.md) whose functional method is [getAsBoolean()](../java/util/function/BooleanSupplier.md)).

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getAsBoolean](../java/util/function/BooleanSupplier.md))`()` Gets a result. |

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
