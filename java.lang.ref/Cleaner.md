# Cleaner

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Cleaner

```
class Cleaner
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.lang.ref.Cleaner](https://developer.android.com/reference/kotlin/java/lang/ref/Cleaner#) |

`Cleaner`manages a set of object references and corresponding cleaning actions.

Cleaning actions are [registered](https://developer.android.com/reference/kotlin/java/lang/ref/Cleaner#register(kotlin.Any,%20java.lang.Runnable))to run after the cleaner is notified that the object has become phantom reachable. The cleaner uses [PhantomReference](https://developer.android.com/reference/kotlin/java/lang/ref/PhantomReference) and [ReferenceQueue](https://developer.android.com/reference/kotlin/java/lang/ref/ReferenceQueue) to be notified when the [reachability](https://developer.android.com/reference/kotlin/java/lang/ref/package-summary#reachability) changes.

Each cleaner operates independently, managing the pending cleaning actions and handling threading and termination when the cleaner is no longer in use. Registering an object reference and corresponding cleaning action returns a [Cleanable](https://developer.android.com/reference/kotlin/java/lang/ref/Cleaner.Cleanable). The most efficient use is to explicitly invoke the [clean](https://developer.android.com/reference/kotlin/java/lang/ref/Cleaner.Cleanable#clean())method when the object is closed or no longer needed. The cleaning action is a [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#) to be invoked at most once when the object has become phantom reachable unless it has already been explicitly cleaned. Note that the cleaning action must not refer to the object being registered. If so, the object will not become phantom reachable and the cleaning action will not be invoked automatically.

The execution of the cleaning action is performed by a thread associated with the cleaner. The thread runs until all registered cleaning actions have completed and the cleaner itself is reclaimed by the garbage collector.

The behavior of cleaners during [System.exit](https://developer.android.com/reference/kotlin/java/lang/System.html#exit(kotlin.Int))is implementation specific. No guarantees are made relating to whether cleaning actions are invoked or not.

Unless otherwise noted, passing a`null`argument to a constructor or method in this class will cause a [NullPointerException](https://developer.android.com/reference/kotlin/java/lang/NullPointerException.html#) to be thrown.

## Summary

| Nested classes ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [Cleanable](https://developer.android.com/reference/kotlin/java/lang/ref/Cleaner.Cleanable) `Cleanable`represents an object and a cleaning action registered in a`Cleaner`. |

| Public methods ||
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Cleaner](https://developer.android.com/reference/kotlin/java/lang/ref/Cleaner#)! | [create](https://developer.android.com/reference/kotlin/java/lang/ref/Cleaner#create())`()` Returns a new`Cleaner`. |
| static [Cleaner](https://developer.android.com/reference/kotlin/java/lang/ref/Cleaner#)! | [create](https://developer.android.com/reference/kotlin/java/lang/ref/Cleaner#create(java.util.concurrent.ThreadFactory))`(`threadFactory:` ` [ThreadFactory](https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadFactory.html#)!`)` Returns a new`Cleaner`using a`Thread`from the`ThreadFactory`. |
| [Cleaner.Cleanable](https://developer.android.com/reference/kotlin/java/lang/ref/Cleaner.Cleanable)! | [register](https://developer.android.com/reference/kotlin/java/lang/ref/Cleaner#register(kotlin.Any,%20java.lang.Runnable))`(`obj:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`, `action:` ` [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#)!`)` Registers an object and a cleaning action to run when the object becomes phantom reachable. |
| --- | --- |

## Public methods

### create

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun create(): Cleaner!
```

Returns a new`Cleaner`.

The cleaner creates a [daemon thread](https://developer.android.com/reference/kotlin/java/lang/Thread.html#setDaemon(kotlin.Boolean))to process the phantom reachable objects and to invoke cleaning actions. The [context class loader](https://developer.android.com/reference/kotlin/java/lang/Thread.html#getContextClassLoader())of the thread is set to the [system class loader](https://developer.android.com/reference/kotlin/java/lang/ClassLoader.html#getSystemClassLoader()). The thread has no permissions, enforced only if a [SecurityManager is set](https://developer.android.com/reference/kotlin/java/lang/System.html#setSecurityManager(java.lang.SecurityManager)).

All exceptions thrown by the cleaning actions in this thread are ignored.

The cleaner terminates when it is phantom reachable and all of the registered cleaning actions are complete.

| Return ||
|-----------------------------------------------------------------------------------|----------------|
| [Cleaner](https://developer.android.com/reference/kotlin/java/lang/ref/Cleaner#)! | a new`Cleaner` |

| Exceptions ||
|-------------------------------|---------------------------------------------------------------------|
| `java.lang.SecurityException` | if the current thread is not allowed to create or start the thread. |

### create

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun create(threadFactory: ThreadFactory!): Cleaner!
```

Returns a new`Cleaner`using a`Thread`from the`ThreadFactory`.

A thread from the thread factory's [newThread](https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadFactory.html#newThread(java.lang.Runnable))method is set to be a [daemon thread](https://developer.android.com/reference/kotlin/java/lang/Thread.html#setDaemon(kotlin.Boolean))and started to process phantom reachable objects and invoke cleaning actions. On each call the [thread factory](https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadFactory.html#newThread(java.lang.Runnable))must provide a Thread that is suitable for performing the cleaning actions.

The cleaner terminates when it is phantom reachable and all of the registered cleaning actions are complete.

| Parameters ||
|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `threadFactory` | [ThreadFactory](https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadFactory.html#)!:a`ThreadFactory`to return a new`Thread`to process cleaning actions |

| Return ||
|-----------------------------------------------------------------------------------|----------------|
| [Cleaner](https://developer.android.com/reference/kotlin/java/lang/ref/Cleaner#)! | a new`Cleaner` |

| Exceptions ||
|-----------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalThreadStateException` | if the thread from the thread factory was [not a new thread](https://developer.android.com/reference/kotlin/java/lang/Thread.State.html#). |
| `java.lang.SecurityException` | if the current thread is not allowed to create or start the thread. |

### register

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun register(
    obj: Any!, 
    action: Runnable!
): Cleaner.Cleanable!
```

Registers an object and a cleaning action to run when the object becomes phantom reachable. Refer to the [API Note](https://developer.android.com/reference/kotlin/java/lang/ref/Cleaner#compatible-cleaners) above for cautions about the behavior of cleaning actions.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| `obj` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:the object to monitor |
| `action` | [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#)!:a`Runnable`to invoke when the object becomes phantom reachable |

| Return ||
|------------------------------------------------------------------------------------------------------|----------------------|
| [Cleaner.Cleanable](https://developer.android.com/reference/kotlin/java/lang/ref/Cleaner.Cleanable)! | a`Cleanable`instance |
