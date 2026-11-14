# Thread.UncaughtExceptionHandler

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# UncaughtExceptionHandler

```
@FunctionalInterface interface UncaughtExceptionHandler
```

| [java.lang.Thread.UncaughtExceptionHandler](../java/lang/Thread.UncaughtExceptionHandler.md) |

| Known Direct Subclasses [ThreadGroup](../java/lang/ThreadGroup.md) |-------------------------------------------------------------------------------------|---------------------------------------------| | [ThreadGroup](../java/lang/ThreadGroup.md) | A thread group represents a set of threads. | |
| --- | --- | --- | --- | --- | --- | --- |

Interface for handlers invoked when a`Thread`abruptly terminates due to an uncaught exception.

When a thread is about to terminate due to an uncaught exception the Java Virtual Machine will query the thread for its`UncaughtExceptionHandler`using [getUncaughtExceptionHandler](../java/lang/Thread.md))and will invoke the handler's`uncaughtException`method, passing the thread and the exception as arguments. If a thread has not had its`UncaughtExceptionHandler`explicitly set, then its`ThreadGroup`object acts as its`UncaughtExceptionHandler`. If the`ThreadGroup`object has no special requirements for dealing with the exception, it can forward the invocation to the [default uncaught exception handler](../java/lang/Thread.md)).

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [uncaughtException](../java/lang/Thread.UncaughtExceptionHandler.md))`(`t:` ` [Thread](../java/lang/Thread.md)`, `e:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)`)` Method invoked when the given thread terminates due to the given uncaught exception. |

## Public methods

### uncaughtException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun uncaughtException(
    t: Thread, 
    e: Throwable
): Unit
```

Method invoked when the given thread terminates due to the given uncaught exception.

Any exception thrown by this method will be ignored by the Java Virtual Machine.

| Parameters ||
|-----|------------------------------------------------------------------------------------------------------|
| `t` | [Thread](../java/lang/Thread.md):the thread |
| `e` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html):the exception |
