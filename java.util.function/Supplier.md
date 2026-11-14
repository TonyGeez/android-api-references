# Supplier

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Supplier

```
@FunctionalInterface interface Supplier<T : Any!>
```

| [java.util.function.Supplier](https://developer.android.com/reference/kotlin/java/util/function/Supplier#) |

| Known Direct Subclasses [ServiceLoader.Provider](https://developer.android.com/reference/kotlin/java/util/ServiceLoader.Provider.html#) |-----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------| | [ServiceLoader.Provider](https://developer.android.com/reference/kotlin/java/util/ServiceLoader.Provider.html#) | Represents a service provider located by`ServiceLoader`. | |
| --- | --- | --- | --- | --- | --- | --- |

Represents a supplier of results.

There is no requirement that a new or distinct result be returned each time the supplier is invoked.

This is a [functional interface](https://developer.android.com/reference/kotlin/java/util/function/package-summary) whose functional method is [get()](https://developer.android.com/reference/kotlin/java/util/function/Supplier#get()).

## Summary

| Public methods ||
|-----------|------------------------------------------------------------------------------------------------------------|
| abstractT | [get](https://developer.android.com/reference/kotlin/java/util/function/Supplier#get())`()` Gets a result. |

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
