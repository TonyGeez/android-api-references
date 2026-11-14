# Thread

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Thread

```
open class Thread : Runnable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.lang.Thread](Thread.md) |

| Known Direct Subclasses [ForkJoinWorkerThread](../java.util.concurrent/ForkJoinWorkerThread.md), [HandlerThread](../android.os/HandlerThread.md) |------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [ForkJoinWorkerThread](../java.util.concurrent/ForkJoinWorkerThread.md) | A thread managed by a [ForkJoinPool](../java.util.concurrent/ForkJoinPool.md), which executes [ForkJoinTask](../java.util.concurrent/ForkJoinTask.md) s. | | [HandlerThread](../android.os/HandlerThread.md) | A [Thread](Thread.md) that has a [Looper](../android.os/Looper.md). | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

A*thread*is a thread of execution in a program. The Java Virtual Machine allows an application to have multiple threads of execution running concurrently.

Every thread has a priority. Threads with higher priority are executed in preference to threads with lower priority. Each thread may or may not also be marked as a daemon. When code running in some thread creates a new`Thread`object, the new thread has its priority initially set equal to the priority of the creating thread, and is a daemon thread if and only if the creating thread is a daemon.

When a Java Virtual Machine starts up, there is usually a single non-daemon thread (which typically calls the method named`main`of some designated class). The Java Virtual Machine continues to execute threads until either of the following occurs:

- The`exit`method of class`Runtime`has been called and the security manager has permitted the exit operation to take place.
- All threads that are not daemon threads have died, either by returning from the call to the`run`method or by throwing an exception that propagates beyond the`run`method.

There are two ways to create a new thread of execution. One is to declare a class to be a subclass of`Thread`. This subclass should override the`run`method of class`Thread`. An instance of the subclass can then be allocated and started. For example, a thread that computes primes larger than a stated value could be written as follows: 

```kotlin
class PrimeThread extends Thread {
          long minPrime;
          PrimeThread(long minPrime) {
              this.minPrime = minPrime;
          }
 
          public void run() {
              // compute primes larger than minPrime
               . . .
          }
      }
  
```

The following code would then create a thread and start it running: 

```kotlin
PrimeThread p = new PrimeThread(143);
      p.start();
  
```

The other way to create a thread is to declare a class that implements the`Runnable`interface. That class then implements the`run`method. An instance of the class can then be allocated, passed as an argument when creating`Thread`, and started. The same example in this other style looks like the following: 

```kotlin
class PrimeRun implements Runnable {
          long minPrime;
          PrimeRun(long minPrime) {
              this.minPrime = minPrime;
          }
 
          public void run() {
              // compute primes larger than minPrime
               . . .
          }
      }
  
```

The following code would then create a thread and start it running: 

```kotlin
PrimeRun p = new PrimeRun(143);
      new Thread(p).start();
  
```

Every thread has a name for identification purposes. More than one thread may have the same name. If a name is not specified when a thread is created, a new name is generated for it.

Unless otherwise noted, passing a`null`argument to a constructor or method in this class will cause a [NullPointerException](NullPointerException.md) to be thrown.

## Summary

| Nested classes ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [State](../java/lang/Thread.State.md) A thread state. |
| abstract | [UncaughtExceptionHandler](../java/lang/Thread.UncaughtExceptionHandler.md) Interface for handlers invoked when a`Thread`abruptly terminates due to an uncaught exception. |

| Constants ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MAX_PRIORITY](Thread.md) The maximum priority that a thread can have. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MIN_PRIORITY](Thread.md) The minimum priority that a thread can have. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [NORM_PRIORITY](Thread.md) The default priority that is assigned to a thread. |
| --- | --- |

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [Thread](Thread.md))`()` Allocates a new`Thread`object. |
| [Thread](Thread.md))`(`target:` ` [Runnable](Runnable.md)?`)` Allocates a new`Thread`object. |
| [Thread](Thread.md))`(`target:` ` [Runnable](Runnable.md)?`, `name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Allocates a new`Thread`object. |
| [Thread](Thread.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Allocates a new`Thread`object. |
| [Thread](Thread.md))`(`group:` ` [ThreadGroup](ThreadGroup.md)?`, `target:` ` [Runnable](Runnable.md)?`)` Allocates a new`Thread`object. |
| [Thread](Thread.md))`(`group:` ` [ThreadGroup](ThreadGroup.md)?`, `target:` ` [Runnable](Runnable.md)?`, `name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Allocates a new`Thread`object so that it has`target`as its run object, has the specified`name`as its name, and belongs to the thread group referred to by`group`. |
| [Thread](Thread.md))`(`group:` ` [ThreadGroup](ThreadGroup.md)?`, `target:` ` [Runnable](Runnable.md)?`, `name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `stackSize:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Allocates a new`Thread`object so that it has`target`as its run object, has the specified`name`as its name, and belongs to the thread group referred to by`group`, and has the specified*stack size*. |
| [Thread](Thread.md))`(`group:` ` [ThreadGroup](ThreadGroup.md)?`, `target:` ` [Runnable](Runnable.md)?`, `name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `stackSize:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `inheritThreadLocals:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Allocates a new`Thread`object so that it has`target`as its run object, has the specified`name`as its name, belongs to the thread group referred to by`group`, has the specified`stackSize`, and inherits initial values for [inheritable thread-local](InheritableThreadLocal.md) variables if`inheritThreadLocals`is`true`. |
| [Thread](Thread.md))`(`group:` ` [ThreadGroup](ThreadGroup.md)?`, `name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Allocates a new`Thread`object. |

| Public methods ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [activeCount](Thread.md))`()` Returns an estimate of the number of active threads in the current thread's [thread group](ThreadGroup.md) and its subgroups. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [checkAccess](Thread.md))`()` Determines if the currently running thread has permission to modify this thread. |
| openstatic [Thread](Thread.md) | [currentThread](Thread.md))`()` Returns a reference to the currently executing thread object. |
| --- | --- |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [dumpStack](Thread.md))`()` Prints a stack trace of the current thread to the standard error stream. |
| openstatic [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [enumerate](Thread.md))`(`tarray:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Thread](Thread.md)!>!`)` Copies into the specified array every active thread in the current thread's thread group and its subgroups. |
| openstatic [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [Thread](Thread.md)!, [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [StackTraceElement](StackTraceElement.md)!\>!\> | [getAllStackTraces](Thread.md))`()` Returns a map of stack traces for all live threads. |
| --- | --- |
| open [ClassLoader](ClassLoader.md)? | [getContextClassLoader](Thread.md))`()` Returns the context`ClassLoader`for this thread. |
| openstatic [Thread.UncaughtExceptionHandler](../java/lang/Thread.UncaughtExceptionHandler.md)? | [getDefaultUncaughtExceptionHandler](Thread.md))`()` Returns the default handler invoked when a thread abruptly terminates due to an uncaught exception. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getId](Thread.md))`()` Returns the identifier of this Thread. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getName](Thread.md))`()` Returns this thread's name. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPriority](Thread.md))`()` Returns this thread's priority. |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [StackTraceElement](StackTraceElement.md)!\> | [getStackTrace](Thread.md))`()` Returns an array of stack trace elements representing the stack dump of this thread. |
| --- | --- |
| open [Thread.State](../java/lang/Thread.State.md) | [getState](Thread.md))`()` Returns the state of this thread. |
| [ThreadGroup](ThreadGroup.md)? | [getThreadGroup](Thread.md))`()` Returns the thread group to which this thread belongs. |
| open [Thread.UncaughtExceptionHandler](../java/lang/Thread.UncaughtExceptionHandler.md)? | [getUncaughtExceptionHandler](Thread.md))`()` Returns the handler invoked when this thread abruptly terminates due to an uncaught exception. |
| --- | --- |
| openstatic [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [holdsLock](Thread.md))`(`obj:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)`)` Returns`true`if and only if the current thread holds the monitor lock on the specified object. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [interrupt](Thread.md))`()` Interrupts this thread. |
| openstatic [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [interrupted](Thread.md))`()` Tests whether the current thread has been interrupted. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isAlive](Thread.md))`()` Tests if this thread is alive. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isDaemon](Thread.md))`()` Tests if this thread is a daemon thread. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isInterrupted](Thread.md))`()` Tests whether this thread has been interrupted. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isVirtual](Thread.md))`()` Returns`true`if this thread is a virtual thread. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [join](Thread.md))`()` Waits for this thread to die. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [join](Thread.md))`(`millis:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Waits at most`millis`milliseconds for this thread to die. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [join](Thread.md))`(`millis:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `nanos:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Waits at most`millis`milliseconds plus`nanos`nanoseconds for this thread to die. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onSpinWait](Thread.md))`()` Indicates that the caller is momentarily unable to progress, until the occurrence of one or more actions on the part of other activities. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [run](Thread.md))`()` If this thread was constructed using a separate`Runnable`run object, then that`Runnable`object's`run`method is called; otherwise, this method does nothing and returns. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setContextClassLoader](Thread.md))`(`cl:` ` [ClassLoader](ClassLoader.md)?`)` Sets the context ClassLoader for this Thread. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDaemon](Thread.md))`(`on:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Marks this thread as either a [daemon](Thread.md))thread or a user thread. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDefaultUncaughtExceptionHandler](Thread.md))`(`eh:` ` [Thread.UncaughtExceptionHandler](../java/lang/Thread.UncaughtExceptionHandler.md)?`)` Set the default handler invoked when a thread abruptly terminates due to an uncaught exception, and no other handler has been defined for that thread. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setName](Thread.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Changes the name of this thread to be equal to the argument`name`. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPriority](Thread.md))`(`newPriority:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Changes the priority of this thread. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setUncaughtExceptionHandler](Thread.md))`(`eh:` ` [Thread.UncaughtExceptionHandler](../java/lang/Thread.UncaughtExceptionHandler.md)?`)` Set the handler invoked when this thread abruptly terminates due to an uncaught exception. |
| --- | --- |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [sleep](Thread.md))`(`millis:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Causes the currently executing thread to sleep (temporarily cease execution) for the specified number of milliseconds, subject to the precision and accuracy of system timers and schedulers. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [sleep](Thread.md))`(`millis:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `nanos:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Causes the currently executing thread to sleep (temporarily cease execution) for the specified number of milliseconds plus the specified number of nanoseconds, subject to the precision and accuracy of system timers and schedulers. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [start](Thread.md))`()` Causes this thread to begin execution; the Java Virtual Machine calls the`run`method of this thread. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [stop](Thread.md))`()` Throws`UnsupportedOperationException`. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [threadId](Thread.md))`()` Returns the identifier of this Thread. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](Thread.md))`()` Returns a string representation of this thread, including the thread's name, priority, and thread group. |
| --- | --- |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [yield](Thread.md))`()` A hint to the scheduler that the current thread is willing to yield its current use of a processor. |

| Protected methods ||
|--------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | [clone](Thread.md))`()` Throws CloneNotSupportedException as a Thread can not be meaningfully cloned. |

## Constants

### MAX_PRIORITY

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MAX_PRIORITY: Int
```

The maximum priority that a thread can have. 

 Value: 10

### MIN_PRIORITY

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MIN_PRIORITY: Int
```

The minimum priority that a thread can have. 

 Value: 1

### NORM_PRIORITY

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NORM_PRIORITY: Int
```

The default priority that is assigned to a thread. 

 Value: 5

## Public constructors

### Thread

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Thread()
```

Allocates a new`Thread`object. This constructor has the same effect as [Thread](Thread.md))`(null, null, gname)`, where`gname`is a newly generated name. Automatically generated names are of the form`"Thread-"+`*n* , where*n*is an integer. 

### Thread

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Thread(target: Runnable?)
```

Allocates a new`Thread`object. This constructor has the same effect as [Thread](Thread.md))`(null, target, gname)`, where`gname`is a newly generated name. Automatically generated names are of the form`"Thread-"+`*n* , where*n*is an integer.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `target` | [Runnable](Runnable.md)?:the object whose`run`method is invoked when this thread is started. If`null`, this classes`run`method does nothing. |

### Thread

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Thread(
    target: Runnable?, 
    name: String)
```

Allocates a new`Thread`object. This constructor has the same effect as [Thread](Thread.md))`(null, target, name)`.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `target` | [Runnable](Runnable.md)?:the object whose`run`method is invoked when this thread is started. If`null`, this thread's run method is invoked. |
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):the name of the new thread |

### Thread

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Thread(name: String)
```

Allocates a new`Thread`object. This constructor has the same effect as [Thread](Thread.md))`(null, null, name)`.

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):the name of the new thread |

### Thread

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Thread(
    group: ThreadGroup?, 
    target: Runnable?)
```

Allocates a new`Thread`object. This constructor has the same effect as [Thread](Thread.md))`(group, target, gname)`,where`gname`is a newly generated name. Automatically generated names are of the form`"Thread-"+`*n* , where*n*is an integer.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `group` | [ThreadGroup](ThreadGroup.md)?:the thread group. If`null`and there is a security manager, the group is determined by [SecurityManager.getThreadGroup()](SecurityManager.md)). If there is not a security manager or`SecurityManager.getThreadGroup()`returns`null`, the group is set to the current thread's thread group. |
| `target` | [Runnable](Runnable.md)?:the object whose`run`method is invoked when this thread is started. If`null`, this thread's run method is invoked. |

| Exceptions ||
|-------------------------------|----------------------------------------------------------------------------|
| `java.lang.SecurityException` | if the current thread cannot create a thread in the specified thread group |

### Thread

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Thread(
    group: ThreadGroup?, 
    target: Runnable?, 
    name: String)
```

Allocates a new`Thread`object so that it has`target`as its run object, has the specified`name`as its name, and belongs to the thread group referred to by`group`.

If there is a security manager, its [checkAccess](SecurityManager.md))method is invoked with the ThreadGroup as its argument.

In addition, its`checkPermission`method is invoked with the`RuntimePermission("enableContextClassLoaderOverride")`permission when invoked directly or indirectly by the constructor of a subclass which overrides the`getContextClassLoader`or`setContextClassLoader`methods.

The priority of the newly created thread is set equal to the priority of the thread creating it, that is, the currently running thread. The method [setPriority](Thread.md))may be used to change the priority to a new value.

The newly created thread is initially marked as being a daemon thread if and only if the thread creating it is currently marked as a daemon thread. The method [setDaemon](Thread.md))may be used to change whether or not a thread is a daemon.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `group` | [ThreadGroup](ThreadGroup.md)?:the thread group. If`null`and there is a security manager, the group is determined by [SecurityManager.getThreadGroup()](SecurityManager.md)). If there is not a security manager or`SecurityManager.getThreadGroup()`returns`null`, the group is set to the current thread's thread group. |
| `target` | [Runnable](Runnable.md)?:the object whose`run`method is invoked when this thread is started. If`null`, this thread's run method is invoked. |
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):the name of the new thread |
| --- | --- |

| Exceptions ||
|-------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.SecurityException` | if the current thread cannot create a thread in the specified thread group or cannot override the context class loader methods. |

### Thread

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Thread(
    group: ThreadGroup?, 
    target: Runnable?, 
    name: String, 
    stackSize: Long)
```

Allocates a new`Thread`object so that it has`target`as its run object, has the specified`name`as its name, and belongs to the thread group referred to by`group`, and has the specified*stack size*.

This constructor is identical to [Thread(java.lang.ThreadGroup,java.lang.Runnable,java.lang.String)](Thread.md))with the exception of the fact that it allows the thread stack size to be specified. The stack size is the approximate number of bytes of address space that the virtual machine is to allocate for this thread's stack.**The effect of the`stackSize`parameter, if any, is highly platform dependent.**

On some platforms, specifying a higher value for the`stackSize`parameter may allow a thread to achieve greater recursion depth before throwing a [StackOverflowError](StackOverflowError.md). Similarly, specifying a lower value may allow a greater number of threads to exist concurrently without throwing an [OutOfMemoryError](OutOfMemoryError.md)(or other internal error). The details of the relationship between the value of the`stackSize`parameter and the maximum recursion depth and concurrency level are platform-dependent.**On some platforms, the value of the`stackSize`parameter may have no effect whatsoever.**

The virtual machine is free to treat the`stackSize`parameter as a suggestion. If the specified value is unreasonably low for the platform, the virtual machine may instead use some platform-specific minimum value; if the specified value is unreasonably high, the virtual machine may instead use some platform-specific maximum. Likewise, the virtual machine is free to round the specified value up or down as it sees fit (or to ignore it completely).

Specifying a value of zero for the`stackSize`parameter will cause this constructor to behave exactly like the`Thread(ThreadGroup, Runnable, String)`constructor.

*Due to the platform-dependent nature of the behavior of this constructor, extreme care should be exercised in its use. The thread stack size necessary to perform a given computation will likely vary from one JRE implementation to another. In light of this variation, careful tuning of the stack size parameter may be required, and the tuning may need to be repeated for each JRE implementation on which an application is to run.*

Implementation note: Java platform implementers are encouraged to document their implementation's behavior with respect to the`stackSize`parameter.

| Parameters ||
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `group` | [ThreadGroup](ThreadGroup.md)?:the thread group. If`null`and there is a security manager, the group is determined by [SecurityManager.getThreadGroup()](SecurityManager.md)). If there is not a security manager or`SecurityManager.getThreadGroup()`returns`null`, the group is set to the current thread's thread group. |
| `target` | [Runnable](Runnable.md)?:the object whose`run`method is invoked when this thread is started. If`null`, this thread's run method is invoked. |
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):the name of the new thread |
| --- | --- |
| `stackSize` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the desired stack size for the new thread, or zero to indicate that this parameter is to be ignored. |

| Exceptions ||
|-------------------------------|----------------------------------------------------------------------------|
| `java.lang.SecurityException` | if the current thread cannot create a thread in the specified thread group |

### Thread

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Thread(
    group: ThreadGroup?, 
    target: Runnable?, 
    name: String, 
    stackSize: Long, 
    inheritThreadLocals: Boolean)
```

Allocates a new`Thread`object so that it has`target`as its run object, has the specified`name`as its name, belongs to the thread group referred to by`group`, has the specified`stackSize`, and inherits initial values for [inheritable thread-local](InheritableThreadLocal.md) variables if`inheritThreadLocals`is`true`.

This constructor is identical to [Thread(java.lang.ThreadGroup,java.lang.Runnable,java.lang.String,long)](Thread.md))with the added ability to suppress, or not, the inheriting of initial values for inheritable thread-local variables from the constructing thread. This allows for finer grain control over inheritable thread-locals. Care must be taken when passing a value of`false`for`inheritThreadLocals`, as it may lead to unexpected behavior if the new thread executes code that expects a specific thread-local value to be inherited.

Specifying a value of`true`for the`inheritThreadLocals`parameter will cause this constructor to behave exactly like the`Thread(ThreadGroup, Runnable, String, long)`constructor.

| Parameters ||
|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `group` | [ThreadGroup](ThreadGroup.md)?:the thread group. If`null`and there is a security manager, the group is determined by [SecurityManager.getThreadGroup()](SecurityManager.md)). If there is not a security manager or`SecurityManager.getThreadGroup()`returns`null`, the group is set to the current thread's thread group. |
| `target` | [Runnable](Runnable.md)?:the object whose`run`method is invoked when this thread is started. If`null`, this thread's run method is invoked. |
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):the name of the new thread |
| --- | --- |
| `stackSize` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the desired stack size for the new thread, or zero to indicate that this parameter is to be ignored |
| `inheritThreadLocals` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):if`true`, inherit initial values for inheritable thread-locals from the constructing thread, otherwise no initial values are inherited |

| Exceptions ||
|-------------------------------|----------------------------------------------------------------------------|
| `java.lang.SecurityException` | if the current thread cannot create a thread in the specified thread group |

### Thread

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Thread(
    group: ThreadGroup?, 
    name: String)
```

Allocates a new`Thread`object. This constructor has the same effect as [Thread](Thread.md))`(group, null, name)`.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `group` | [ThreadGroup](ThreadGroup.md)?:the thread group. If`null`and there is a security manager, the group is determined by [SecurityManager.getThreadGroup()](SecurityManager.md)). If there is not a security manager or`SecurityManager.getThreadGroup()`returns`null`, the group is set to the current thread's thread group. |
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):the name of the new thread |

| Exceptions ||
|-------------------------------|----------------------------------------------------------------------------|
| `java.lang.SecurityException` | if the current thread cannot create a thread in the specified thread group |

## Public methods

### activeCount

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun activeCount(): Int
```

Returns an estimate of the number of active threads in the current thread's [thread group](ThreadGroup.md) and its subgroups. Recursively iterates over all subgroups in the current thread's thread group.

The value returned is only an estimate because the number of threads may change dynamically while this method traverses internal data structures, and might be affected by the presence of certain system threads. This method is intended primarily for debugging and monitoring purposes.

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | an estimate of the number of active threads in the current thread's thread group and in any other thread group that has the current thread's thread group as an ancestor |

### checkAccess

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun checkAccess(): Unit
```

**Deprecated:** *This method is only useful in conjunction with [the Security Manager](SecurityManager.md), which is deprecated and subject to removal in a future release. Consequently, this method is also deprecated and subject to removal. There is no replacement for the Security Manager or this method.*

Determines if the currently running thread has permission to modify this thread.

If there is a security manager, its`checkAccess`method is called with this thread as its argument. This may result in throwing a`SecurityException`.

| Exceptions ||
|-------------------------------|-------------------------------------------------------------|
| `java.lang.SecurityException` | if the current thread is not allowed to access this thread. |

**See Also**

- [java.lang.SecurityManager#checkAccess(Thread)](SecurityManager.md)) 

### currentThread

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun currentThread(): Thread
```

Returns a reference to the currently executing thread object.

| Return ||
|----------------------------------------------------------------------------|---------------------------------|
| [Thread](Thread.md) | the currently executing thread. |

### dumpStack

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun dumpStack(): Unit
```

Prints a stack trace of the current thread to the standard error stream. This method is used only for debugging. 
**See Also**

- [java.lang.Throwable#printStackTrace()](Throwable.md)) 

### enumerate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun enumerate(tarray: Array<Thread!>!): Int
```

Copies into the specified array every active thread in the current thread's thread group and its subgroups. This method simply invokes the[java.lang.ThreadGroup#enumerate(Thread[])](https://developer.android.com/reference/kotlin/java/lang/ThreadGroup#enumerate(kotlin.Array))method of the current thread's thread group.

An application might use the [activeCount](Thread.md))method to get an estimate of how big the array should be, however*if the array is too short to hold all the threads, the extra threads are silently ignored.* If it is critical to obtain every active thread in the current thread's thread group and its subgroups, the invoker should verify that the returned int value is strictly less than the length of`tarray`.

Due to the inherent race condition in this method, it is recommended that the method only be used for debugging and monitoring purposes.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `tarray` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Thread](Thread.md)!\>!:an array into which to put the list of threads |

| Return ||
|----------------------------------------------------------------------------|------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of threads put into the array |

| Exceptions ||
|-------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.SecurityException` | if [java.lang.ThreadGroup#checkAccess](ThreadGroup.md))determines that the current thread cannot access its thread group |

### getAllStackTraces

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getAllStackTraces(): MutableMap<Thread!, Array<StackTraceElement!>!>
```

Returns a map of stack traces for all live threads. The map keys are threads and each map value is an array of`StackTraceElement`that represents the stack dump of the corresponding`Thread`. The returned stack traces are in the format specified for the [getStackTrace](Thread.md))method.

The threads may be executing while this method is called. The stack trace of each thread only represents a snapshot and each stack trace may be obtained at different time. A zero-length array will be returned in the map value if the virtual machine has no stack trace information about a thread.

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)< [Thread](Thread.md)!,` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [StackTraceElement](StackTraceElement.md)!>!> | a`Map`from`Thread`to an array of`StackTraceElement`that represents the stack trace of the corresponding thread. |

**See Also**

- [#getStackTrace](Thread.md))
- [java.lang.RuntimePermission](RuntimePermission.md)
- [java.lang.Throwable#getStackTrace](Throwable.md)) 

### getContextClassLoader

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getContextClassLoader(): ClassLoader?
```

Returns the context`ClassLoader`for this thread. The context`ClassLoader`is provided by the creator of the thread for use by code running in this thread when loading classes and resources. If not [set](Thread.md)), the default is the`ClassLoader`context of the parent thread. The context`ClassLoader`of the primordial thread is typically set to the class loader used to load the application.

| Return ||
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [ClassLoader](ClassLoader.md)? | the context`ClassLoader`for this thread, or`null`indicating the system class loader (or, failing that, the bootstrap class loader) |

| Exceptions ||
|-------------------------------|----------------------------------------------------------|
| `java.lang.SecurityException` | if the current thread cannot get the context ClassLoader |

### getDefaultUncaughtExceptionHandler

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getDefaultUncaughtExceptionHandler(): Thread.UncaughtExceptionHandler?
```

Returns the default handler invoked when a thread abruptly terminates due to an uncaught exception. If the returned value is`null`, there is no default.

| Return ||
|------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| [Thread.UncaughtExceptionHandler](../java/lang/Thread.UncaughtExceptionHandler.md)? | the default uncaught exception handler for all threads |

**See Also**

- [#setDefaultUncaughtExceptionHandler](Thread.md)) 

### getId

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getId(): Long
```

**Deprecated:** *This method is not final and may be overridden to return a value that is not the thread ID. Use [threadId()](Thread.md))instead.*

Returns the identifier of this Thread. The thread ID is a positive`long`number generated when this thread was created. The thread ID is unique and remains unchanged during its lifetime. When a thread is terminated, this thread ID may be reused.

| Return ||
|------------------------------------------------------------------------------|-------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | this thread's ID. |

### getName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getName(): String
```

Returns this thread's name.

| Return ||
|----------------------------------------------------------------------------------|---------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | this thread's name. |

**See Also**

- [#setName(String)](Thread.md)) 

### getPriority

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPriority(): Int
```

Returns this thread's priority.

| Return ||
|----------------------------------------------------------------------------|-------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | this thread's priority. |

**See Also**

- [#setPriority](Thread.md)) 

### getStackTrace

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getStackTrace(): Array<StackTraceElement!>
```

Returns an array of stack trace elements representing the stack dump of this thread. This method will return a zero-length array if this thread has not started, has started but has not yet been scheduled to run by the system, or has terminated. If the returned array is of non-zero length then the first element of the array represents the top of the stack, which is the most recent method invocation in the sequence. The last element of the array represents the bottom of the stack, which is the least recent method invocation in the sequence.

If there is a security manager, and this thread is not the current thread, then the security manager's`checkPermission`method is called with a`RuntimePermission("getStackTrace")`permission to see if it's ok to get the stack trace.

Some virtual machines may, under some circumstances, omit one or more stack frames from the stack trace. In the extreme case, a virtual machine that has no stack trace information concerning this thread is permitted to return a zero-length array from this method.

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [StackTraceElement](StackTraceElement.md)!> | an array of`StackTraceElement`, each represents one stack frame. |

| Exceptions ||
|-------------------------------|--------------------------------------------------------------------------------------------------------------|
| `java.lang.SecurityException` | if a security manager exists and its`checkPermission`method doesn't allow getting the stack trace of thread. |

**See Also**

- [java.lang.RuntimePermission](RuntimePermission.md)
- [java.lang.Throwable#getStackTrace](Throwable.md)) 

### getState

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getState(): Thread.State
```

Returns the state of this thread. This method is designed for use in monitoring of the system state, not for synchronization control.

| Return ||
|---------------------------------------------------------------------------------------|----------------------|
| [Thread.State](../java/lang/Thread.State.md) | this thread's state. |

### getThreadGroup

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getThreadGroup(): ThreadGroup?
```

Returns the thread group to which this thread belongs. This method returns null if this thread has died (been stopped).

| Return ||
|--------------------------------------------------------------------------------------|-----------------------------|
| [ThreadGroup](ThreadGroup.md)? | this thread's thread group. |

### getUncaughtExceptionHandler

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getUncaughtExceptionHandler(): Thread.UncaughtExceptionHandler?
```

Returns the handler invoked when this thread abruptly terminates due to an uncaught exception. If this thread has not had an uncaught exception handler explicitly set then this thread's`ThreadGroup`object is returned, unless this thread has terminated, in which case`null`is returned.

| Return ||
|------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| [Thread.UncaughtExceptionHandler](../java/lang/Thread.UncaughtExceptionHandler.md)? | the uncaught exception handler for this thread |

### holdsLock

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun holdsLock(obj: Any): Boolean
```

Returns`true`if and only if the current thread holds the monitor lock on the specified object.

This method is designed to allow a program to assert that the current thread already holds a specified lock: 

```kotlin
assert Thread.holdsLock(obj);
  
```

| Parameters ||
|-------|-----------------------------------------------------------------------------------------------------------------------|
| `obj` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html):the object on which to test lock ownership |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the current thread holds the monitor lock on the specified object. |

| Exceptions ||
|----------------------------------|-----------------|
| `java.lang.NullPointerException` | if obj is`null` |

### interrupt

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun interrupt(): Unit
```

Interrupts this thread.

Unless the current thread is interrupting itself, which is always permitted, the [checkAccess](Thread.md))method of this thread is invoked, which may cause a [SecurityException](SecurityException.md) to be thrown.

If this thread is blocked in an invocation of the [wait()](Object.md)), [wait(long)](Object.md)), or [wait(long, int)](Object.md))methods of the [Object](Object.md) class, or of the [join()](Thread.md)), [join(long)](Thread.md)), [join(long,int)](Thread.md)), [sleep(long)](Thread.md)), or [sleep(long,int)](Thread.md))methods of this class, then its interrupt status will be cleared and it will receive an [InterruptedException](InterruptedException.md).

If this thread is blocked in an I/O operation upon an then the channel will be closed, the thread's interrupt status will be set, and the thread will receive a .

If this thread is blocked in a [java.nio.channels.Selector](../java.nio.channels/Selector.md) then the thread's interrupt status will be set and it will return immediately from the selection operation, possibly with a non-zero value, just as if the selector's [wakeup](../java.nio.channels/Selector.md))method were invoked.

If none of the previous conditions hold then this thread's interrupt status will be set.

Interrupting a thread that is not alive need not have any effect.

| Exceptions ||
|-------------------------------|-------------------------------------------------|
| `java.lang.SecurityException` | if the current thread cannot modify this thread |

### interrupted

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun interrupted(): Boolean
```

Tests whether the current thread has been interrupted. The*interrupted status*of the thread is cleared by this method. In other words, if this method were to be called twice in succession, the second call would return false (unless the current thread were interrupted again, after the first call had cleared its interrupted status and before the second call had examined it).

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the current thread has been interrupted;`false`otherwise. |

**See Also**

- <https://developer.android.com/reference/kotlin/java/lang/Thread#isInterrupted()> 

### isAlive

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isAlive(): Boolean
```

Tests if this thread is alive. A thread is alive if it has been started and has not yet terminated.

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this thread is alive;`false`otherwise. |

### isDaemon

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isDaemon(): Boolean
```

Tests if this thread is a daemon thread.

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this thread is a daemon thread;`false`otherwise. |

**See Also**

- [#setDaemon(boolean)](Thread.md)) 

### isInterrupted

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isInterrupted(): Boolean
```

Tests whether this thread has been interrupted. The*interrupted status*of the thread is unaffected by this method.

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this thread has been interrupted;`false`otherwise. |

**See Also**

- <https://developer.android.com/reference/kotlin/java/lang/Thread#interrupted()> 

### isVirtual

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isVirtual(): Boolean
```

Returns`true`if this thread is a virtual thread. A virtual thread is scheduled by the Java virtual machine rather than the operating system.

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this thread is a virtual thread This method always returns false because virtual thread isn't implemented on Android yet. This method is only useful for cross-platform libraries. |

### join

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun join(): Unit
```

Waits for this thread to die.

An invocation of this method behaves in exactly the same way as the invocation
[join](Thread.md))`(0)`

| Exceptions ||
|----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.InterruptedException` | if any thread has interrupted the current thread. The*interrupted status*of the current thread is cleared when this exception is thrown. |

### join

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun join(millis: Long): Unit
```

Waits at most`millis`milliseconds for this thread to die. A timeout of`0`means to wait forever.

This implementation uses a loop of`this.wait`calls conditioned on`this.isAlive`. As a thread terminates the`this.notifyAll`method is invoked. It is recommended that applications not use`wait`,`notify`, or`notifyAll`on`Thread`instances.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------|
| `millis` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the time to wait in milliseconds |

| Exceptions ||
|--------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the value of`millis`is negative |
| `java.lang.InterruptedException` | if any thread has interrupted the current thread. The*interrupted status*of the current thread is cleared when this exception is thrown. |

### join

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun join(
    millis: Long, 
    nanos: Int
): Unit
```

Waits at most`millis`milliseconds plus`nanos`nanoseconds for this thread to die. If both arguments are`0`, it means to wait forever.

This implementation uses a loop of`this.wait`calls conditioned on`this.isAlive`. As a thread terminates the`this.notifyAll`method is invoked. It is recommended that applications not use`wait`,`notify`, or`notifyAll`on`Thread`instances.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------|
| `millis` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the time to wait in milliseconds |
| `nanos` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):`0-999999`additional nanoseconds to wait |

| Exceptions ||
|--------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the value of`millis`is negative, or the value of`nanos`is not in the range`0-999999` |
| `java.lang.InterruptedException` | if any thread has interrupted the current thread. The*interrupted status*of the current thread is cleared when this exception is thrown. |

### onSpinWait

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun onSpinWait(): Unit
```

Indicates that the caller is momentarily unable to progress, until the occurrence of one or more actions on the part of other activities. By invoking this method within each iteration of a spin-wait loop construct, the calling thread indicates to the runtime that it is busy-waiting. The runtime may take action to improve the performance of invoking spin-wait loop constructions. 

### run

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun run(): Unit
```

If this thread was constructed using a separate`Runnable`run object, then that`Runnable`object's`run`method is called; otherwise, this method does nothing and returns.

Subclasses of`Thread`should override this method. 
**See Also**

- <https://developer.android.com/reference/kotlin/java/lang/Thread#start()>
- <https://developer.android.com/reference/kotlin/java/lang/Thread#stop()>
- [#Thread(ThreadGroup, Runnable, String)](Thread.md)) 

### setContextClassLoader

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setContextClassLoader(cl: ClassLoader?): Unit
```

Sets the context ClassLoader for this Thread. The context ClassLoader can be set when a thread is created, and allows the creator of the thread to provide the appropriate class loader, through`getContextClassLoader`, to code running in the thread when loading classes and resources.

If a security manager is present, its [checkPermission](SecurityManager.md))method is invoked with a [RuntimePermission](RuntimePermission.md)`("setContextClassLoader")`permission to see if setting the context ClassLoader is permitted.

| Parameters ||
|------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `cl` | [ClassLoader](ClassLoader.md)?:the context ClassLoader for this Thread, or null indicating the system class loader (or, failing that, the bootstrap class loader) |

| Exceptions ||
|-------------------------------|----------------------------------------------------------|
| `java.lang.SecurityException` | if the current thread cannot set the context ClassLoader |

### setDaemon

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setDaemon(on: Boolean): Unit
```

Marks this thread as either a [daemon](Thread.md))thread or a user thread. The Java Virtual Machine exits when the only threads running are all daemon threads.

This method must be invoked before the thread is started.

| Parameters ||
|------|-----------------------------------------------------------------------------------------------------------------------------------|
| `on` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):if`true`, marks this thread as a daemon thread |

| Exceptions ||
|-----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalThreadStateException` | if this thread is [alive](Thread.md)) |
| `java.lang.SecurityException` | if [checkAccess](Thread.md))determines that the current thread cannot modify this thread |

### setDefaultUncaughtExceptionHandler

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun setDefaultUncaughtExceptionHandler(eh: Thread.UncaughtExceptionHandler?): Unit
```

Set the default handler invoked when a thread abruptly terminates due to an uncaught exception, and no other handler has been defined for that thread.

Uncaught exception handling is controlled first by the thread, then by the thread's [ThreadGroup](ThreadGroup.md) object and finally by the default uncaught exception handler. If the thread does not have an explicit uncaught exception handler set, and the thread's thread group (including parent thread groups) does not specialize its`uncaughtException`method, then the default handler's`uncaughtException`method will be invoked.

By setting the default uncaught exception handler, an application can change the way in which uncaught exceptions are handled (such as logging to a specific device, or file) for those threads that would already accept whatever "default" behavior the system provided.

Note that the default uncaught exception handler should not usually defer to the thread's`ThreadGroup`object, as that could cause infinite recursion.

| Parameters ||
|------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `eh` | [Thread.UncaughtExceptionHandler](../java/lang/Thread.UncaughtExceptionHandler.md)?:the object to use as the default uncaught exception handler. If`null`then there is no default handler. |

**See Also**

- [#setUncaughtExceptionHandler](Thread.md))
- [#getUncaughtExceptionHandler](Thread.md))
- [java.lang.ThreadGroup#uncaughtException](ThreadGroup.md)) 

### setName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setName(name: String): Unit
```

Changes the name of this thread to be equal to the argument`name`.

First the`checkAccess`method of this thread is called with no arguments. This may result in throwing a`SecurityException`.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):the new name for this thread. |

| Exceptions ||
|-------------------------------|--------------------------------------------------|
| `java.lang.SecurityException` | if the current thread cannot modify this thread. |

**See Also**

- [#getName](Thread.md))
- <https://developer.android.com/reference/kotlin/java/lang/Thread#checkAccess()> 

### setPriority

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setPriority(newPriority: Int): Unit
```

Changes the priority of this thread.

First the`checkAccess`method of this thread is called with no arguments. This may result in throwing a`SecurityException`.

Otherwise, the priority of this thread is set to the smaller of the specified`newPriority`and the maximum permitted priority of the thread's thread group.

| Parameters ||
|---------------|-----------------------------------------------------------------------------------------------------------|
| `newPriority` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):priority to set this thread to |

| Exceptions ||
|--------------------------------------|--------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | If the priority is not in the range`MIN_PRIORITY`to`MAX_PRIORITY`. |
| `java.lang.SecurityException` | if the current thread cannot modify this thread. |

**See Also**

- [#getPriority](Thread.md))
- <https://developer.android.com/reference/kotlin/java/lang/Thread#checkAccess()>
- <https://developer.android.com/reference/kotlin/java/lang/Thread#getThreadGroup()>
- [#MAX_PRIORITY](Thread.md)
- [#MIN_PRIORITY](Thread.md)
- [java.lang.ThreadGroup#getMaxPriority()](ThreadGroup.md)) 

### setUncaughtExceptionHandler

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setUncaughtExceptionHandler(eh: Thread.UncaughtExceptionHandler?): Unit
```

Set the handler invoked when this thread abruptly terminates due to an uncaught exception.

A thread can take full control of how it responds to uncaught exceptions by having its uncaught exception handler explicitly set. If no such handler is set then the thread's`ThreadGroup`object acts as its handler.

| Parameters ||
|------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `eh` | [Thread.UncaughtExceptionHandler](../java/lang/Thread.UncaughtExceptionHandler.md)?:the object to use as this thread's uncaught exception handler. If`null`then this thread has no explicit handler. |

| Exceptions ||
|-------------------------------|-------------------------------------------------------------|
| `java.lang.SecurityException` | if the current thread is not allowed to modify this thread. |

**See Also**

- [#setDefaultUncaughtExceptionHandler](Thread.md))
- [java.lang.ThreadGroup#uncaughtException](ThreadGroup.md)) 

### sleep

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun sleep(millis: Long): Unit
```

Causes the currently executing thread to sleep (temporarily cease execution) for the specified number of milliseconds, subject to the precision and accuracy of system timers and schedulers. The thread does not lose ownership of any monitors.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------|
| `millis` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the length of time to sleep in milliseconds |

| Exceptions ||
|--------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the value of`millis`is negative |
| `java.lang.InterruptedException` | if any thread has interrupted the current thread. The*interrupted status*of the current thread is cleared when this exception is thrown. |

### sleep

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun sleep(
    millis: Long, 
    nanos: Int
): Unit
```

Causes the currently executing thread to sleep (temporarily cease execution) for the specified number of milliseconds plus the specified number of nanoseconds, subject to the precision and accuracy of system timers and schedulers. The thread does not lose ownership of any monitors.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------|
| `millis` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the length of time to sleep in milliseconds |
| `nanos` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):`0-999999`additional nanoseconds to sleep |

| Exceptions ||
|--------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the value of`millis`is negative, or the value of`nanos`is not in the range`0-999999` |
| `java.lang.InterruptedException` | if any thread has interrupted the current thread. The*interrupted status*of the current thread is cleared when this exception is thrown. |

### start

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun start(): Unit
```

Causes this thread to begin execution; the Java Virtual Machine calls the`run`method of this thread.

The result is that two threads are running concurrently: the current thread (which returns from the call to the`start`method) and the other thread (which executes its`run`method).

It is never legal to start a thread more than once. In particular, a thread may not be restarted once it has completed execution.

**WARNING:** Do not override this method, because the runtime may treat this method`final`in the future, because it works closely with the runtime.

| Exceptions ||
|-----------------------------------------|------------------------------------|
| `java.lang.IllegalThreadStateException` | if the thread was already started. |

**See Also**

- <https://developer.android.com/reference/kotlin/java/lang/Thread#run()>
- <https://developer.android.com/reference/kotlin/java/lang/Thread#stop()> 

### stop

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun stop(): Unit
```

**Deprecated:** *This method was originally designed to force a thread to stop and throw a`ThreadDeath`as an exception. It was inherently unsafe. Stopping a thread with Thread.stop causes it to unlock all of the monitors that it has locked (as a natural consequence of the unchecked`ThreadDeath`exception propagating up the stack). If any of the objects previously protected by these monitors were in an inconsistent state, the damaged objects become visible to other threads, potentially resulting in arbitrary behavior. Many uses of`stop`should be replaced by code that simply modifies some variable to indicate that the target thread should stop running. The target thread should check this variable regularly, and return from its run method in an orderly fashion if the variable indicates that it is to stop running. If the target thread waits for long periods (on a condition variable, for example), the`interrupt`method should be used to interrupt the wait. For more information, see [Why are Thread.stop, Thread.suspend and Thread.resume Deprecated?](https://docs.oracle.com/javase/8/docs/technotes/guides/concurrency/threadPrimitiveDeprecation.html).*

Throws`UnsupportedOperationException`. 

### threadId

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun threadId(): Long
```

Returns the identifier of this Thread. The thread ID is a positive`long`number generated when this thread was created. The thread ID is unique and remains unchanged during its lifetime.

| Return ||
|------------------------------------------------------------------------------|------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | this thread's ID |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

Returns a string representation of this thread, including the thread's name, priority, and thread group.

| Return ||
|----------------------------------------------------------------------------------|-----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of this thread. |

### yield

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun yield(): Unit
```

A hint to the scheduler that the current thread is willing to yield its current use of a processor. The scheduler is free to ignore this hint.

Yield is a heuristic attempt to improve relative progression between threads that would otherwise over-utilise a CPU. Its use should be combined with detailed profiling and benchmarking to ensure that it actually has the desired effect.

It is rarely appropriate to use this method. It may be useful for debugging or testing purposes, where it may help to reproduce bugs due to race conditions. It may also be useful when designing concurrency control constructs such as the ones in the [java.util.concurrent.locks](../java.util.concurrent.locks/_package.md) package.

## Protected methods

### clone

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun clone(): Any
```

Throws CloneNotSupportedException as a Thread can not be meaningfully cloned. Construct a new Thread instead.

| Return ||
|----------------------------------------------------------------------------|---------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | a clone of this instance. |

| Exceptions ||
|----------------------------------------|--------|
| `java.lang.CloneNotSupportedException` | always |
