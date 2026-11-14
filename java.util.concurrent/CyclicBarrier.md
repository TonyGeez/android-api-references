# CyclicBarrier

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CyclicBarrier

```
open class CyclicBarrier
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [java.util.concurrent.CyclicBarrier](https://developer.android.com/reference/kotlin/java/util/concurrent/CyclicBarrier#) |

A synchronization aid that allows a set of threads to all wait for each other to reach a common barrier point. CyclicBarriers are useful in programs involving a fixed sized party of threads that must occasionally wait for each other. The barrier is called*cyclic*because it can be re-used after the waiting threads are released.

A`CyclicBarrier`supports an optional [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#) command that is run once per barrier point, after the last thread in the party arrives, but before any threads are released. This*barrier action*is useful for updating shared-state before any of the parties continue.

**Sample usage:**Here is an example of using a barrier in a parallel decomposition design: 

```kotlin
<code>class Solver {
    final int N;
    final float[][] data;
    final CyclicBarrier barrier;
 
    class Worker implements Runnable {
      int myRow;
      Worker(int row) { myRow = row; }
      public void run() {
        while (!done()) {
          processRow(myRow);
 
          try {
            barrier.await();
          } catch (InterruptedException ex) {
            return;
          } catch (BrokenBarrierException ex) {
            return;
          }
        }
      }
    }
 
    public Solver(float[][] matrix) {
      data = matrix;
      N = matrix.length;
      Runnable barrierAction = () -&gt; mergeRows(...);
      barrier = new CyclicBarrier(N, barrierAction);
 
      List&lt;Thread&gt; threads = new ArrayList&lt;&gt;(N);
      for (int i = 0; i &lt; N; i++) {
        Thread thread = new Thread(new Worker(i));
        threads.add(thread);
        thread.start();
      }
 
      // wait until done
      for (Thread thread : threads)
        try {
          thread.join();
        } catch (InterruptedException ex) { }
    }
  }</code>
```
Here, each worker thread processes a row of the matrix, then waits at the barrier until all rows have been processed. When all rows are processed the supplied [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#) barrier action is executed and merges the rows. If the merger determines that a solution has been found then`done()`will return`true`and each worker will terminate.

If the barrier action does not rely on the parties being suspended when it is executed, then any of the threads in the party could execute that action when it is released. To facilitate this, each invocation of #await returns the arrival index of that thread at the barrier. You can then choose which thread should execute the barrier action, for example: 

```kotlin
<code>if (barrier.await() == 0) {
    // log the completion of this iteration
  }</code>
```

The`CyclicBarrier`uses an all-or-none breakage model for failed synchronization attempts: If a thread leaves a barrier point prematurely because of interruption, failure, or timeout, all other threads waiting at that barrier point will also leave abnormally via [BrokenBarrierException](https://developer.android.com/reference/kotlin/java/util/concurrent/BrokenBarrierException)(or [InterruptedException](https://developer.android.com/reference/kotlin/java/lang/InterruptedException.html#) if they too were interrupted at about the same time).

Memory consistency effects: Actions in a thread prior to calling`await()` [*happen-before*](https://developer.android.com/reference/kotlin/java/util/concurrent/package-summary#MemoryVisibility) actions that are part of the barrier action, which in turn*happen-before* actions following a successful return from the corresponding`await()`in other threads.

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [CyclicBarrier](https://developer.android.com/reference/kotlin/java/util/concurrent/CyclicBarrier#CyclicBarrier(kotlin.Int))`(`parties:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a new`CyclicBarrier`that will trip when the given number of parties (threads) are waiting upon it, and does not perform a predefined action when the barrier is tripped. |
| [CyclicBarrier](https://developer.android.com/reference/kotlin/java/util/concurrent/CyclicBarrier#CyclicBarrier(kotlin.Int,%20java.lang.Runnable))`(`parties:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `barrierAction:` ` [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#)!`)` Creates a new`CyclicBarrier`that will trip when the given number of parties (threads) are waiting upon it, and which will execute the given barrier action when the barrier is tripped, performed by the last thread entering the barrier. |

| Public methods ||
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [await](https://developer.android.com/reference/kotlin/java/util/concurrent/CyclicBarrier#await())`()` Waits until all [parties](https://developer.android.com/reference/kotlin/java/util/concurrent/CyclicBarrier#getParties())have invoked`await`on this barrier. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [await](https://developer.android.com/reference/kotlin/java/util/concurrent/CyclicBarrier#await(kotlin.Long,%20java.util.concurrent.TimeUnit))`(`timeout:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `unit:` ` [TimeUnit](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit)!`)` Waits until all [parties](https://developer.android.com/reference/kotlin/java/util/concurrent/CyclicBarrier#getParties())have invoked`await`on this barrier, or the specified waiting time elapses. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getNumberWaiting](https://developer.android.com/reference/kotlin/java/util/concurrent/CyclicBarrier#getNumberWaiting())`()` Returns the number of parties currently waiting at the barrier. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getParties](https://developer.android.com/reference/kotlin/java/util/concurrent/CyclicBarrier#getParties())`()` Returns the number of parties required to trip this barrier. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isBroken](https://developer.android.com/reference/kotlin/java/util/concurrent/CyclicBarrier#isBroken())`()` Queries if this barrier is in a broken state. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [reset](https://developer.android.com/reference/kotlin/java/util/concurrent/CyclicBarrier#reset())`()` Resets the barrier to its initial state. |

## Public constructors

### CyclicBarrier

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
CyclicBarrier(parties: Int)
```

Creates a new`CyclicBarrier`that will trip when the given number of parties (threads) are waiting upon it, and does not perform a predefined action when the barrier is tripped.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| `parties` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of threads that must invoke #await before the barrier is tripped |

| Exceptions ||
|--------------------------------------|---------------------------|
| `java.lang.IllegalArgumentException` | if`parties`is less than 1 |

### CyclicBarrier

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
CyclicBarrier(
    parties: Int, 
    barrierAction: Runnable!)
```

Creates a new`CyclicBarrier`that will trip when the given number of parties (threads) are waiting upon it, and which will execute the given barrier action when the barrier is tripped, performed by the last thread entering the barrier.

| Parameters ||
|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `parties` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of threads that must invoke #await before the barrier is tripped |
| `barrierAction` | [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#)!:the command to execute when the barrier is tripped, or`null`if there is no action |

| Exceptions ||
|--------------------------------------|---------------------------|
| `java.lang.IllegalArgumentException` | if`parties`is less than 1 |

## Public methods

### await

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun await(): Int
```

Waits until all [parties](https://developer.android.com/reference/kotlin/java/util/concurrent/CyclicBarrier#getParties())have invoked`await`on this barrier.

If the current thread is not the last to arrive then it is disabled for thread scheduling purposes and lies dormant until one of the following things happens:

- The last thread arrives; or
- Some other thread [interrupts](https://developer.android.com/reference/kotlin/java/lang/Thread.html#interrupt())the current thread; or
- Some other thread [interrupts](https://developer.android.com/reference/kotlin/java/lang/Thread.html#interrupt())one of the other waiting threads; or
- Some other thread times out while waiting for barrier; or
- Some other thread invokes [reset](https://developer.android.com/reference/kotlin/java/util/concurrent/CyclicBarrier#reset())on this barrier.

If the current thread:

- has its interrupted status set on entry to this method; or
- is [interrupted](https://developer.android.com/reference/kotlin/java/lang/Thread.html#interrupt())while waiting

then [InterruptedException](https://developer.android.com/reference/kotlin/java/lang/InterruptedException.html#) is thrown and the current thread's interrupted status is cleared.

If the barrier is [reset](https://developer.android.com/reference/kotlin/java/util/concurrent/CyclicBarrier#reset())while any thread is waiting, or if the barrier [is broken](https://developer.android.com/reference/kotlin/java/util/concurrent/CyclicBarrier#isBroken())when`await`is invoked, or while any thread is waiting, then [BrokenBarrierException](https://developer.android.com/reference/kotlin/java/util/concurrent/BrokenBarrierException) is thrown.

If any thread is [interrupted](https://developer.android.com/reference/kotlin/java/lang/Thread.html#interrupt())while waiting, then all other waiting threads will throw [BrokenBarrierException](https://developer.android.com/reference/kotlin/java/util/concurrent/BrokenBarrierException) and the barrier is placed in the broken state.

If the current thread is the last thread to arrive, and a non-null barrier action was supplied in the constructor, then the current thread runs the action before allowing the other threads to continue. If an exception occurs during the barrier action then that exception will be propagated in the current thread and the barrier is placed in the broken state.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the arrival index of the current thread, where index`getParties() - 1`indicates the first to arrive and zero indicates the last to arrive |

| Exceptions ||
|-----------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.InterruptedException` | if the current thread was interrupted while waiting |
| `java.util.concurrent.BrokenBarrierException` | if*another* thread was interrupted or timed out while the current thread was waiting, or the barrier was reset, or the barrier was broken when`await`was called, or the barrier action (if present) failed due to an exception |

### await

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun await(
    timeout: Long, 
    unit: TimeUnit!
): Int
```

Waits until all [parties](https://developer.android.com/reference/kotlin/java/util/concurrent/CyclicBarrier#getParties())have invoked`await`on this barrier, or the specified waiting time elapses.

If the current thread is not the last to arrive then it is disabled for thread scheduling purposes and lies dormant until one of the following things happens:

- The last thread arrives; or
- The specified timeout elapses; or
- Some other thread [interrupts](https://developer.android.com/reference/kotlin/java/lang/Thread.html#interrupt())the current thread; or
- Some other thread [interrupts](https://developer.android.com/reference/kotlin/java/lang/Thread.html#interrupt())one of the other waiting threads; or
- Some other thread times out while waiting for barrier; or
- Some other thread invokes [reset](https://developer.android.com/reference/kotlin/java/util/concurrent/CyclicBarrier#reset())on this barrier.

If the current thread:

- has its interrupted status set on entry to this method; or
- is [interrupted](https://developer.android.com/reference/kotlin/java/lang/Thread.html#interrupt())while waiting

then [InterruptedException](https://developer.android.com/reference/kotlin/java/lang/InterruptedException.html#) is thrown and the current thread's interrupted status is cleared.

If the specified waiting time elapses then [TimeoutException](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeoutException) is thrown. If the time is less than or equal to zero, the method will not wait at all.

If the barrier is [reset](https://developer.android.com/reference/kotlin/java/util/concurrent/CyclicBarrier#reset())while any thread is waiting, or if the barrier [is broken](https://developer.android.com/reference/kotlin/java/util/concurrent/CyclicBarrier#isBroken())when`await`is invoked, or while any thread is waiting, then [BrokenBarrierException](https://developer.android.com/reference/kotlin/java/util/concurrent/BrokenBarrierException) is thrown.

If any thread is [interrupted](https://developer.android.com/reference/kotlin/java/lang/Thread.html#interrupt())while waiting, then all other waiting threads will throw [BrokenBarrierException](https://developer.android.com/reference/kotlin/java/util/concurrent/BrokenBarrierException) and the barrier is placed in the broken state.

If the current thread is the last thread to arrive, and a non-null barrier action was supplied in the constructor, then the current thread runs the action before allowing the other threads to continue. If an exception occurs during the barrier action then that exception will be propagated in the current thread and the barrier is placed in the broken state.

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------------------------|
| `timeout` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the time to wait for the barrier |
| `unit` | [TimeUnit](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit)!:the time unit of the timeout parameter |

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the arrival index of the current thread, where index`getParties() - 1`indicates the first to arrive and zero indicates the last to arrive |

| Exceptions ||
|-----------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.InterruptedException` | if the current thread was interrupted while waiting |
| `java.util.concurrent.TimeoutException` | if the specified timeout elapses. In this case the barrier will be broken. |
| `java.util.concurrent.BrokenBarrierException` | if*another* thread was interrupted or timed out while the current thread was waiting, or the barrier was reset, or the barrier was broken when`await`was called, or the barrier action (if present) failed due to an exception |

### getNumberWaiting

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getNumberWaiting(): Int
```

Returns the number of parties currently waiting at the barrier. This method is primarily useful for debugging and assertions.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of parties currently blocked in #await |

### getParties

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getParties(): Int
```

Returns the number of parties required to trip this barrier.

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of parties required to trip this barrier |

### isBroken

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isBroken(): Boolean
```

Queries if this barrier is in a broken state.

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if one or more parties broke out of this barrier due to interruption or timeout since construction or the last reset, or a barrier action failed due to an exception;`false`otherwise. |

### reset

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun reset(): Unit
```

Resets the barrier to its initial state. If any parties are currently waiting at the barrier, they will return with a [BrokenBarrierException](https://developer.android.com/reference/kotlin/java/util/concurrent/BrokenBarrierException). Note that resets*after*a breakage has occurred for other reasons can be complicated to carry out; threads need to re-synchronize in some other way, and choose one to perform the reset. It may be preferable to instead create a new barrier for subsequent use.
