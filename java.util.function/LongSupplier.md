# LongSupplier

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# LongSupplier

```
@FunctionalInterface interface LongSupplier
```

| [java.util.function.LongSupplier](../java/util/function/LongSupplier.md) |

Represents a supplier of`long`-valued results. This is the`long`-producing primitive specialization of [Supplier](../java/util/function/Supplier.md).

There is no requirement that a distinct result be returned each time the supplier is invoked.

This is a [functional interface](../java/util/function/_package.md) whose functional method is [getAsLong()](../java/util/function/LongSupplier.md)).

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| abstract [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getAsLong](../java/util/function/LongSupplier.md))`()` Gets a result. |

## Public methods

### getAsLong

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getAsLong(): Long
```

Gets a result.

| Return ||
|------------------------------------------------------------------------------|----------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | a result |
