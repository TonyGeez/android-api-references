# LockSupport

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# LockSupport

```
open class LockSupport
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [java.util.concurrent.locks.LockSupport](https://developer.android.com/reference/kotlin/java/util/concurrent/locks/LockSupport#) |

Basic thread blocking primitives for creating locks and other synchronization classes.

This class associates, with each thread that uses it, a permit (in the sense of the [Semaphore](https://developer.android.com/reference/kotlin/java/util/concurrent/Semaphore.html#) class). A call to`park`will return immediately if the permit is available, consuming it in the process; otherwise it*may* block. A call to`unpark`makes the permit available, if it was not already available. (Unlike with Semaphores though, permits do not accumulate. There is at most one.) Reliable usage requires the use of volatile (or atomic) variables to control when to park or unpark. Orderings of calls to these methods are maintained with respect to volatile variable accesses, but not necessarily non-volatile variable accesses.

Methods`park`and`unpark`provide efficient means of blocking and unblocking threads that do not encounter the problems that cause the deprecated methods`Thread.suspend`and`Thread.resume`to be unusable for such purposes: Races between one thread invoking`park`and another thread trying to`unpark`it will preserve liveness, due to the permit. Additionally,`park`will return if the caller's thread was interrupted, and timeout versions are supported. The`park`method may also return at any other time, for "no reason", so in general must be invoked within a loop that rechecks conditions upon return. In this sense`park`serves as an optimization of a "busy wait" that does not waste as much time spinning, but must be paired with an`unpark`to be effective.

The three forms of`park`each also support a`blocker`object parameter. This object is recorded while the thread is blocked to permit monitoring and diagnostic tools to identify the reasons that threads are blocked. (Such tools may access blockers using method [getBlocker(java.lang.Thread)](https://developer.android.com/reference/kotlin/java/util/concurrent/locks/LockSupport#getBlocker(java.lang.Thread)).) The use of these forms rather than the original forms without this parameter is strongly encouraged. The normal argument to supply as a`blocker`within a lock implementation is`this`.

These methods are designed to be used as tools for creating higher-level synchronization utilities, and are not in themselves useful for most concurrency control applications. The`park`method is designed for use only in constructions of the form: 

```kotlin
<code>while (!canProceed()) {
    // ensure request to unpark is visible to other threads
    ...
    LockSupport.park(this);
  }</code>
```
where no actions by the thread publishing a request to unpark, prior to the call to`park`, entail locking or blocking. Because only one permit is associated with each thread, any intermediary uses of`park`, including implicitly via class loading, could lead to an unresponsive thread (a "lost unpark").

**Sample Usage.**Here is a sketch of a first-in-first-out non-reentrant lock class: 

```kotlin
<code>class FIFOMutex {
    private final AtomicBoolean locked = new AtomicBoolean(false);
    private final Queue&lt;Thread&gt; waiters
      = new ConcurrentLinkedQueue&lt;&gt;();
 
    public void lock() {
      boolean wasInterrupted = false;
      // publish current thread for unparkers
      waiters.add(Thread.currentThread());
 
      // Block while not first in queue or cannot acquire lock
      while (waiters.peek() != Thread.currentThread() ||
             !locked.compareAndSet(false, true)) {
        LockSupport.park(this);
        // ignore interrupts while waiting
        if (Thread.interrupted())
          wasInterrupted = true;
      }
 
      waiters.remove();
      // ensure correct interrupt status on return
      if (wasInterrupted)
        Thread.currentThread().interrupt();
    }
 
    public void unlock() {
      locked.set(false);
      LockSupport.unpark(waiters.peek());
    }
 
    static {
      // Reduce the risk of "lost unpark" due to classloading
      Class&lt;?&gt; ensureLoaded = LockSupport.class;
    }
  }</code>
```

## Summary

| Public methods ||
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getBlocker](https://developer.android.com/reference/kotlin/java/util/concurrent/locks/LockSupport#getBlocker(java.lang.Thread))`(`t:` ` [Thread](https://developer.android.com/reference/kotlin/java/lang/Thread.html#)!`)` Returns the blocker object supplied to the most recent invocation of a park method that has not yet unblocked, or null if not blocked. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [park](https://developer.android.com/reference/kotlin/java/util/concurrent/locks/LockSupport#park())`()` Disables the current thread for thread scheduling purposes unless the permit is available. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [park](https://developer.android.com/reference/kotlin/java/util/concurrent/locks/LockSupport#park(kotlin.Any))`(`blocker:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Disables the current thread for thread scheduling purposes unless the permit is available. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [parkNanos](https://developer.android.com/reference/kotlin/java/util/concurrent/locks/LockSupport#parkNanos(kotlin.Any,%20kotlin.Long))`(`blocker:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`, `nanos:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Disables the current thread for thread scheduling purposes, for up to the specified waiting time, unless the permit is available. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [parkNanos](https://developer.android.com/reference/kotlin/java/util/concurrent/locks/LockSupport#parkNanos(kotlin.Long))`(`nanos:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Disables the current thread for thread scheduling purposes, for up to the specified waiting time, unless the permit is available. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [parkUntil](https://developer.android.com/reference/kotlin/java/util/concurrent/locks/LockSupport#parkUntil(kotlin.Any,%20kotlin.Long))`(`blocker:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`, `deadline:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Disables the current thread for thread scheduling purposes, until the specified deadline, unless the permit is available. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [parkUntil](https://developer.android.com/reference/kotlin/java/util/concurrent/locks/LockSupport#parkUntil(kotlin.Long))`(`deadline:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Disables the current thread for thread scheduling purposes, until the specified deadline, unless the permit is available. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setCurrentBlocker](https://developer.android.com/reference/kotlin/java/util/concurrent/locks/LockSupport#setCurrentBlocker(kotlin.Any))`(`blocker:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Sets the object to be returned by invocations of [getBlocker](https://developer.android.com/reference/kotlin/java/util/concurrent/locks/LockSupport#getBlocker(java.lang.Thread))for the current thread. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unpark](https://developer.android.com/reference/kotlin/java/util/concurrent/locks/LockSupport#unpark(java.lang.Thread))`(`thread:` ` [Thread](https://developer.android.com/reference/kotlin/java/lang/Thread.html#)!`)` Makes available the permit for the given thread, if it was not already available. |

## Public methods

### getBlocker

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getBlocker(t: Thread!): Any!
```

Returns the blocker object supplied to the most recent invocation of a park method that has not yet unblocked, or null if not blocked. The value returned is just a momentary snapshot -- the thread may have since unblocked or blocked on a different blocker object.

| Parameters ||
|-----|---------------------------------------------------------------------------------------------|
| `t` | [Thread](https://developer.android.com/reference/kotlin/java/lang/Thread.html#)!:the thread |

| Return ||
|-----------------------------------------------------------------------------|-------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | the blocker |

| Exceptions ||
|----------------------------------|---------------------|
| `java.lang.NullPointerException` | if argument is null |

### park

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun park(): Unit
```

Disables the current thread for thread scheduling purposes unless the permit is available.

If the permit is available then it is consumed and the call returns immediately; otherwise the current thread becomes disabled for thread scheduling purposes and lies dormant until one of three things happens:

- Some other thread invokes [unpark](https://developer.android.com/reference/kotlin/java/util/concurrent/locks/LockSupport#unpark(java.lang.Thread))with the current thread as the target; or
- Some other thread [interrupts](https://developer.android.com/reference/kotlin/java/lang/Thread.html#interrupt())the current thread; or
- The call spuriously (that is, for no reason) returns.

This method does*not*report which of these caused the method to return. Callers should re-check the conditions which caused the thread to park in the first place. Callers may also determine, for example, the interrupt status of the thread upon return. 

### park

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun park(blocker: Any!): Unit
```

Disables the current thread for thread scheduling purposes unless the permit is available.

If the permit is available then it is consumed and the call returns immediately; otherwise the current thread becomes disabled for thread scheduling purposes and lies dormant until one of three things happens:

- Some other thread invokes [unpark](https://developer.android.com/reference/kotlin/java/util/concurrent/locks/LockSupport#unpark(java.lang.Thread))with the current thread as the target; or
- Some other thread [interrupts](https://developer.android.com/reference/kotlin/java/lang/Thread.html#interrupt())the current thread; or
- The call spuriously (that is, for no reason) returns.

This method does*not*report which of these caused the method to return. Callers should re-check the conditions which caused the thread to park in the first place. Callers may also determine, for example, the interrupt status of the thread upon return.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------|
| `blocker` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:the synchronization object responsible for this thread parking |

### parkNanos

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun parkNanos(
    blocker: Any!, 
    nanos: Long
): Unit
```

Disables the current thread for thread scheduling purposes, for up to the specified waiting time, unless the permit is available.

If the specified waiting time is zero or negative, the method does nothing. Otherwise, if the permit is available then it is consumed and the call returns immediately; otherwise the current thread becomes disabled for thread scheduling purposes and lies dormant until one of four things happens:

- Some other thread invokes [unpark](https://developer.android.com/reference/kotlin/java/util/concurrent/locks/LockSupport#unpark(java.lang.Thread))with the current thread as the target; or
- Some other thread [interrupts](https://developer.android.com/reference/kotlin/java/lang/Thread.html#interrupt())the current thread; or
- The specified waiting time elapses; or
- The call spuriously (that is, for no reason) returns.

This method does*not*report which of these caused the method to return. Callers should re-check the conditions which caused the thread to park in the first place. Callers may also determine, for example, the interrupt status of the thread, or the elapsed time upon return.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------|
| `blocker` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:the synchronization object responsible for this thread parking |
| `nanos` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the maximum number of nanoseconds to wait |

### parkNanos

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun parkNanos(nanos: Long): Unit
```

Disables the current thread for thread scheduling purposes, for up to the specified waiting time, unless the permit is available.

If the specified waiting time is zero or negative, the method does nothing. Otherwise, if the permit is available then it is consumed and the call returns immediately; otherwise the current thread becomes disabled for thread scheduling purposes and lies dormant until one of four things happens:

- Some other thread invokes [unpark](https://developer.android.com/reference/kotlin/java/util/concurrent/locks/LockSupport#unpark(java.lang.Thread))with the current thread as the target; or
- Some other thread [interrupts](https://developer.android.com/reference/kotlin/java/lang/Thread.html#interrupt())the current thread; or
- The specified waiting time elapses; or
- The call spuriously (that is, for no reason) returns.

This method does*not*report which of these caused the method to return. Callers should re-check the conditions which caused the thread to park in the first place. Callers may also determine, for example, the interrupt status of the thread, or the elapsed time upon return.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------|
| `nanos` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the maximum number of nanoseconds to wait |

### parkUntil

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun parkUntil(
    blocker: Any!, 
    deadline: Long
): Unit
```

Disables the current thread for thread scheduling purposes, until the specified deadline, unless the permit is available.

If the permit is available then it is consumed and the call returns immediately; otherwise the current thread becomes disabled for thread scheduling purposes and lies dormant until one of four things happens:

- Some other thread invokes [unpark](https://developer.android.com/reference/kotlin/java/util/concurrent/locks/LockSupport#unpark(java.lang.Thread))with the current thread as the target; or
- Some other thread [interrupts](https://developer.android.com/reference/kotlin/java/lang/Thread.html#interrupt())the current thread; or
- The specified deadline passes; or
- The call spuriously (that is, for no reason) returns.

This method does*not*report which of these caused the method to return. Callers should re-check the conditions which caused the thread to park in the first place. Callers may also determine, for example, the interrupt status of the thread, or the current time upon return.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| `blocker` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:the synchronization object responsible for this thread parking |
| `deadline` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the absolute time, in milliseconds from the Epoch, to wait until |

### parkUntil

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun parkUntil(deadline: Long): Unit
```

Disables the current thread for thread scheduling purposes, until the specified deadline, unless the permit is available.

If the permit is available then it is consumed and the call returns immediately; otherwise the current thread becomes disabled for thread scheduling purposes and lies dormant until one of four things happens:

- Some other thread invokes [unpark](https://developer.android.com/reference/kotlin/java/util/concurrent/locks/LockSupport#unpark(java.lang.Thread))with the current thread as the target; or
- Some other thread [interrupts](https://developer.android.com/reference/kotlin/java/lang/Thread.html#interrupt())the current thread; or
- The specified deadline passes; or
- The call spuriously (that is, for no reason) returns.

This method does*not*report which of these caused the method to return. Callers should re-check the conditions which caused the thread to park in the first place. Callers may also determine, for example, the interrupt status of the thread, or the current time upon return.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| `deadline` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the absolute time, in milliseconds from the Epoch, to wait until |

### setCurrentBlocker

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun setCurrentBlocker(blocker: Any!): Unit
```

Sets the object to be returned by invocations of [getBlocker](https://developer.android.com/reference/kotlin/java/util/concurrent/locks/LockSupport#getBlocker(java.lang.Thread))for the current thread. This method may be used before invoking the no-argument version of [park()](https://developer.android.com/reference/kotlin/java/util/concurrent/locks/LockSupport#park())from non-public objects, allowing more helpful diagnostics, or retaining compatibility with previous implementations of blocking methods. Previous values of the blocker are not automatically restored after blocking. To obtain the effects of`park(b`}, use`setCurrentBlocker(b); park(); setCurrentBlocker(null);`

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------|
| `blocker` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:the blocker object |

### unpark

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun unpark(thread: Thread!): Unit
```

Makes available the permit for the given thread, if it was not already available. If the thread was blocked on`park`then it will unblock. Otherwise, its next call to`park`is guaranteed not to block. This operation is not guaranteed to have any effect at all if the given thread has not been started.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `thread` | [Thread](https://developer.android.com/reference/kotlin/java/lang/Thread.html#)!:the thread to unpark, or`null`, in which case this operation has no effect |
