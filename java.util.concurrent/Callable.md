# Callable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Callable

```
@FunctionalInterface interface Callable<V : Any!>
```

| [java.util.concurrent.Callable](../java/util/concurrent/Callable.md) |

A task that returns a result and may throw an exception. Implementors define a single method with no arguments called`call`.

The`Callable`interface is similar to , in that both are designed for classes whose instances are potentially executed by another thread. A`Runnable`, however, does not return a result and cannot throw a checked exception.

The [Executors](../java/util/concurrent/Executors.md) class contains utility methods to convert from other common forms to`Callable`classes.

## Summary

| Public methods ||
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstractV | [call](../java/util/concurrent/Callable.md))`()` Computes a result, or throws an exception if unable to do so. |

## Public methods

### call

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun call(): V
```

Computes a result, or throws an exception if unable to do so.

| Return ||
|---|-----------------|
| V | computed result |

| Exceptions ||
|-----------------------|-------------------------------|
| `java.lang.Exception` | if unable to compute a result |
