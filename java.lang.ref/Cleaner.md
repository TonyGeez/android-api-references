# Cleaner

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Cleaner

```
class Cleaner
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.lang.ref.Cleaner](Cleaner.md) |

`Cleaner`manages a set of object references and corresponding cleaning actions.

Cleaning actions are [registered](Cleaner.md))to run after the cleaner is notified that the object has become phantom reachable. The cleaner uses [PhantomReference](PhantomReference.md) and [ReferenceQueue](ReferenceQueue.md) to be notified when the [reachability](_package.md) changes.

Each cleaner operates independently, managing the pending cleaning actions and handling threading and termination when the cleaner is no longer in use. Registering an object reference and corresponding cleaning action returns a [Cleanable](../java/lang/ref/Cleaner.Cleanable.md). The most efficient use is to explicitly invoke the [clean](../java/lang/ref/Cleaner.Cleanable.md))method when the object is closed or no longer needed. The cleaning action is a [Runnable](../java.lang/Runnable.md) to be invoked at most once when the object has become phantom reachable unless it has already been explicitly cleaned. Note that the cleaning action must not refer to the object being registered. If so, the object will not become phantom reachable and the cleaning action will not be invoked automatically.

The execution of the cleaning action is performed by a thread associated with the cleaner. The thread runs until all registered cleaning actions have completed and the cleaner itself is reclaimed by the garbage collector.

The behavior of cleaners during [System.exit](../java.lang/System.md))is implementation specific. No guarantees are made relating to whether cleaning actions are invoked or not.

Unless otherwise noted, passing a`null`argument to a constructor or method in this class will cause a [NullPointerException](../java.lang/NullPointerException.md) to be thrown.

## Summary

| Nested classes ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [Cleanable](../java/lang/ref/Cleaner.Cleanable.md) `Cleanable`represents an object and a cleaning action registered in a`Cleaner`. |

| Public methods ||
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Cleaner](Cleaner.md)! | [create](Cleaner.md))`()` Returns a new`Cleaner`. |
| static [Cleaner](Cleaner.md)! | [create](Cleaner.md))`(`threadFactory:` ` [ThreadFactory](../java.util.concurrent/ThreadFactory.md)!`)` Returns a new`Cleaner`using a`Thread`from the`ThreadFactory`. |
| [Cleaner.Cleanable](../java/lang/ref/Cleaner.Cleanable.md)! | [register](Cleaner.md))`(`obj:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`, `action:` ` [Runnable](../java.lang/Runnable.md)!`)` Registers an object and a cleaning action to run when the object becomes phantom reachable. |
| --- | --- |

## Public methods

### create

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun create(): Cleaner!
```

Returns a new`Cleaner`.

The cleaner creates a [daemon thread](../java.lang/Thread.md))to process the phantom reachable objects and to invoke cleaning actions. The [context class loader](../java.lang/Thread.md))of the thread is set to the [system class loader](../java.lang/ClassLoader.md)). The thread has no permissions, enforced only if a [SecurityManager is set](../java.lang/System.md)).

All exceptions thrown by the cleaning actions in this thread are ignored.

The cleaner terminates when it is phantom reachable and all of the registered cleaning actions are complete.

| Return ||
|-----------------------------------------------------------------------------------|----------------|
| [Cleaner](Cleaner.md)! | a new`Cleaner` |

| Exceptions ||
|-------------------------------|---------------------------------------------------------------------|
| `java.lang.SecurityException` | if the current thread is not allowed to create or start the thread. |

### create

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun create(threadFactory: ThreadFactory!): Cleaner!
```

Returns a new`Cleaner`using a`Thread`from the`ThreadFactory`.

A thread from the thread factory's [newThread](../java.util.concurrent/ThreadFactory.md))method is set to be a [daemon thread](../java.lang/Thread.md))and started to process phantom reachable objects and invoke cleaning actions. On each call the [thread factory](../java.util.concurrent/ThreadFactory.md))must provide a Thread that is suitable for performing the cleaning actions.

The cleaner terminates when it is phantom reachable and all of the registered cleaning actions are complete.

| Parameters ||
|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `threadFactory` | [ThreadFactory](../java.util.concurrent/ThreadFactory.md)!:a`ThreadFactory`to return a new`Thread`to process cleaning actions |

| Return ||
|-----------------------------------------------------------------------------------|----------------|
| [Cleaner](Cleaner.md)! | a new`Cleaner` |

| Exceptions ||
|-----------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalThreadStateException` | if the thread from the thread factory was [not a new thread](../java/lang/Thread.State.md). |
| `java.lang.SecurityException` | if the current thread is not allowed to create or start the thread. |

### register

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun register(
    obj: Any!, 
    action: Runnable!
): Cleaner.Cleanable!
```

Registers an object and a cleaning action to run when the object becomes phantom reachable. Refer to the [API Note](Cleaner.md) above for cautions about the behavior of cleaning actions.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| `obj` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:the object to monitor |
| `action` | [Runnable](../java.lang/Runnable.md)!:a`Runnable`to invoke when the object becomes phantom reachable |

| Return ||
|------------------------------------------------------------------------------------------------------|----------------------|
| [Cleaner.Cleanable](../java/lang/ref/Cleaner.Cleanable.md)! | a`Cleanable`instance |
