# Supplier

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Supplier

```
@FunctionalInterface interface Supplier<T : Any!>
```

| [java.util.function.Supplier](../java/util/function/Supplier.md) |

| Known Direct Subclasses [ServiceLoader.Provider](../java/util/ServiceLoader.Provider.md) |-----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------| | [ServiceLoader.Provider](../java/util/ServiceLoader.Provider.md) | Represents a service provider located by`ServiceLoader`. | |
| --- | --- | --- | --- | --- | --- | --- |

Represents a supplier of results.

There is no requirement that a new or distinct result be returned each time the supplier is invoked.

This is a [functional interface](../java/util/function/_package.md) whose functional method is [get()](../java/util/function/Supplier.md)).

## Summary

| Public methods ||
|-----------|------------------------------------------------------------------------------------------------------------|
| abstractT | [get](../java/util/function/Supplier.md))`()` Gets a result. |

## Public methods

### get

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun get(): T
```

Gets a result.

| Return ||
|---|----------|
| T | a result |
