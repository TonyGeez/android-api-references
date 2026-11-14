# IntSupplier

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# IntSupplier

```
@FunctionalInterface interface IntSupplier
```

| [java.util.function.IntSupplier](../java/util/function/IntSupplier.md) |

Represents a supplier of`int`-valued results. This is the`int`-producing primitive specialization of [Supplier](../java/util/function/Supplier.md).

There is no requirement that a distinct result be returned each time the supplier is invoked.

This is a [functional interface](../java/util/function/_package.md) whose functional method is [getAsInt()](../java/util/function/IntSupplier.md)).

## Summary

| Public methods ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getAsInt](../java/util/function/IntSupplier.md))`()` Gets a result. |

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
