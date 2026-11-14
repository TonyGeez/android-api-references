# CountDownLatch

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CountDownLatch

```
open class CountDownLatch
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.util.concurrent.CountDownLatch](CountDownLatch.md) |

A synchronization aid that allows one or more threads to wait until a set of operations being performed in other threads completes.

A`CountDownLatch`is initialized with a given*count* . The #await methods block until the current count reaches zero due to invocations of the [countDown](CountDownLatch.md))method, after which all waiting threads are released and any subsequent invocations of #await return immediately. This is a one-shot phenomenon -- the count cannot be reset. If you need a version that resets the count, consider using a [CyclicBarrier](CyclicBarrier.md).

A`CountDownLatch`is a versatile synchronization tool and can be used for a number of purposes. A`CountDownLatch`initialized with a count of one serves as a simple on/off latch, or gate: all threads invoking #await wait at the gate until it is opened by a thread invoking [countDown](CountDownLatch.md)). A`CountDownLatch`initialized to*N* can be used to make one thread wait until*N*threads have completed some action, or some action has been completed N times.

A useful property of a`CountDownLatch`is that it doesn't require that threads calling`countDown`wait for the count to reach zero before proceeding, it simply prevents any thread from proceeding past an #await until all threads could pass.

**Sample usage:**Here is a pair of classes in which a group of worker threads use two countdown latches:

- The first is a start signal that prevents any worker from proceeding until the driver is ready for them to proceed;
- The second is a completion signal that allows the driver to wait until all workers have completed.

```kotlin
<code>class Driver { // ...
    void main() throws InterruptedException {
      CountDownLatch startSignal = new CountDownLatch(1);
      CountDownLatch doneSignal = new CountDownLatch(N);
 
      for (int i = 0; i &lt; N; ++i) // create and start threads
        new Thread(new Worker(startSignal, doneSignal)).start();
 
      doSomethingElse();            // don't let run yet
      startSignal.countDown();      // let all threads proceed
      doSomethingElse();
      doneSignal.await();           // wait for all to finish
    }
  }
 
  class Worker implements Runnable {
    private final CountDownLatch startSignal;
    private final CountDownLatch doneSignal;
    Worker(CountDownLatch startSignal, CountDownLatch doneSignal) {
      this.startSignal = startSignal;
      this.doneSignal = doneSignal;
    }
    public void run() {
      try {
        startSignal.await();
        doWork();
        doneSignal.countDown();
      } catch (InterruptedException ex) {} // return;
    }
 
    void doWork() { ... }
  }</code>
```

Another typical usage would be to divide a problem into N parts, describe each part with a Runnable that executes that portion and counts down on the latch, and queue all the Runnables to an Executor. When all sub-parts are complete, the coordinating thread will be able to pass through await. (When threads must repeatedly count down in this way, instead use a [CyclicBarrier](CyclicBarrier.md).) 

```kotlin
<code>class Driver2 { // ...
    void main() throws InterruptedException {
      CountDownLatch doneSignal = new CountDownLatch(N);
      Executor e = ...;
 
      for (int i = 0; i &lt; N; ++i) // create and start threads
        e.execute(new WorkerRunnable(doneSignal, i));
 
      doneSignal.await();           // wait for all to finish
    }
  }
 
  class WorkerRunnable implements Runnable {
    private final CountDownLatch doneSignal;
    private final int i;
    WorkerRunnable(CountDownLatch doneSignal, int i) {
      this.doneSignal = doneSignal;
      this.i = i;
    }
    public void run() {
      doWork();
      doneSignal.countDown();
    }
 
    void doWork() { ... }
  }</code>
```

Memory consistency effects: Until the count reaches zero, actions in a thread prior to calling`countDown()` [*happen-before*](_package.md) actions following a successful return from a corresponding`await()`in another thread.

## Summary

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [CountDownLatch](CountDownLatch.md))`(`count:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Constructs a`CountDownLatch`initialized with the given count. |

| Public methods ||
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [await](CountDownLatch.md))`()` Causes the current thread to wait until the latch has counted down to zero, unless the thread is [interrupted](../java.lang/Thread.md)). |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [await](CountDownLatch.md))`(`timeout:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `unit:` ` [TimeUnit](TimeUnit.md)!`)` Causes the current thread to wait until the latch has counted down to zero, unless the thread is [interrupted](../java.lang/Thread.md)), or the specified waiting time elapses. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [countDown](CountDownLatch.md))`()` Decrements the count of the latch, releasing all waiting threads if the count reaches zero. |
| --- | --- |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getCount](CountDownLatch.md))`()` Returns the current count. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](CountDownLatch.md))`()` Returns a string identifying this latch, as well as its state. |

## Public constructors

### CountDownLatch

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
CountDownLatch(count: Int)
```

Constructs a`CountDownLatch`initialized with the given count.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `count` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of times [countDown](CountDownLatch.md))must be invoked before threads can pass through #await |

| Exceptions ||
|--------------------------------------|----------------------|
| `java.lang.IllegalArgumentException` | if`count`is negative |

## Public methods

### await

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun await(): Unit
```

Causes the current thread to wait until the latch has counted down to zero, unless the thread is [interrupted](../java.lang/Thread.md)).

If the current count is zero then this method returns immediately.

If the current count is greater than zero then the current thread becomes disabled for thread scheduling purposes and lies dormant until one of two things happen:

- The count reaches zero due to invocations of the [countDown](CountDownLatch.md))method; or
- Some other thread [interrupts](../java.lang/Thread.md))the current thread.

If the current thread:

- has its interrupted status set on entry to this method; or
- is [interrupted](../java.lang/Thread.md))while waiting,

then [InterruptedException](../java.lang/InterruptedException.md) is thrown and the current thread's interrupted status is cleared.

| Exceptions ||
|----------------------------------|----------------------------------------------------|
| `java.lang.InterruptedException` | if the current thread is interrupted while waiting |

### await

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun await(
    timeout: Long, 
    unit: TimeUnit!
): Boolean
```

Causes the current thread to wait until the latch has counted down to zero, unless the thread is [interrupted](../java.lang/Thread.md)), or the specified waiting time elapses.

If the current count is zero then this method returns immediately with the value`true`.

If the current count is greater than zero then the current thread becomes disabled for thread scheduling purposes and lies dormant until one of three things happen:

- The count reaches zero due to invocations of the [countDown](CountDownLatch.md))method; or
- Some other thread [interrupts](../java.lang/Thread.md))the current thread; or
- The specified waiting time elapses.

If the count reaches zero then the method returns with the value`true`.

If the current thread:

- has its interrupted status set on entry to this method; or
- is [interrupted](../java.lang/Thread.md))while waiting,

then [InterruptedException](../java.lang/InterruptedException.md) is thrown and the current thread's interrupted status is cleared.

If the specified waiting time elapses then the value`false`is returned. If the time is less than or equal to zero, the method will not wait at all.

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------------------|
| `timeout` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the maximum time to wait |
| `unit` | [TimeUnit](TimeUnit.md)!:the time unit of the`timeout`argument |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the count reached zero and`false`if the waiting time elapsed before the count reached zero |

| Exceptions ||
|----------------------------------|----------------------------------------------------|
| `java.lang.InterruptedException` | if the current thread is interrupted while waiting |

### countDown

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun countDown(): Unit
```

Decrements the count of the latch, releasing all waiting threads if the count reaches zero.

If the current count is greater than zero then it is decremented. If the new count is zero then all waiting threads are re-enabled for thread scheduling purposes.

If the current count equals zero then nothing happens. 

### getCount

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getCount(): Long
```

Returns the current count.

This method is typically used for debugging and testing purposes.

| Return ||
|------------------------------------------------------------------------------|-------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the current count |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

Returns a string identifying this latch, as well as its state. The state, in brackets, includes the String`"Count ="`followed by the current count.

| Return ||
|----------------------------------------------------------------------------------|-------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string identifying this latch, as well as its state |
