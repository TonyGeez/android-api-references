# Exchanger

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Exchanger

```
open class Exchanger<V : Any!>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.util.concurrent.Exchanger](Exchanger.md) |

A synchronization point at which threads can pair and swap elements within pairs. Each thread presents some object on entry to the #exchange method, matches with a partner thread, and receives its partner's object on return. An Exchanger may be viewed as a bidirectional form of a [SynchronousQueue](SynchronousQueue.md). Exchangers may be useful in applications such as genetic algorithms and pipeline designs.

**Sample Usage:** Here are the highlights of a class that uses an`Exchanger`to swap buffers between threads so that the thread filling the buffer gets a freshly emptied one when it needs it, handing off the filled one to the thread emptying the buffer. 

```kotlin
<code>class FillAndEmpty {
    Exchanger&lt;DataBuffer&gt; exchanger = new Exchanger&lt;&gt;();
    DataBuffer initialEmptyBuffer = ...; // a made-up type
    DataBuffer initialFullBuffer = ...;
 
    class FillingLoop implements Runnable {
      public void run() {
        DataBuffer currentBuffer = initialEmptyBuffer;
        try {
          while (currentBuffer != null) {
            addToBuffer(currentBuffer);
            if (currentBuffer.isFull())
              currentBuffer = exchanger.exchange(currentBuffer);
          }
        } catch (InterruptedException ex) { ... handle ...}
      }
    }
 
    class EmptyingLoop implements Runnable {
      public void run() {
        DataBuffer currentBuffer = initialFullBuffer;
        try {
          while (currentBuffer != null) {
            takeFromBuffer(currentBuffer);
            if (currentBuffer.isEmpty())
              currentBuffer = exchanger.exchange(currentBuffer);
          }
        } catch (InterruptedException ex) { ... handle ...}
      }
    }
 
    void start() {
      new Thread(new FillingLoop()).start();
      new Thread(new EmptyingLoop()).start();
    }
  }</code>
```

Memory consistency effects: For each pair of threads that successfully exchange objects via an`Exchanger`, actions prior to the`exchange()`in each thread [*happen-before*](_package.md) those subsequent to a return from the corresponding`exchange()`in the other thread.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------|---|
| [Exchanger](Exchanger.md))`()` Creates a new Exchanger. |

| Public methods ||
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openV | [exchange](Exchanger.md))`(`x:` `V`)` Waits for another thread to arrive at this exchange point (unless the current thread is [interrupted](../java.lang/Thread.md))), and then transfers the given object to it, receiving its object in return. |
| openV | [exchange](Exchanger.md))`(`x:` `V`, `timeout:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `unit:` ` [TimeUnit](TimeUnit.md)!`)` Waits for another thread to arrive at this exchange point (unless the current thread is [interrupted](../java.lang/Thread.md))or the specified waiting time elapses), and then transfers the given object to it, receiving its object in return. |

## Public constructors

### Exchanger

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Exchanger()
```

Creates a new Exchanger.

## Public methods

### exchange

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun exchange(x: V): V
```

Waits for another thread to arrive at this exchange point (unless the current thread is [interrupted](../java.lang/Thread.md))), and then transfers the given object to it, receiving its object in return.

If another thread is already waiting at the exchange point then it is resumed for thread scheduling purposes and receives the object passed in by the current thread. The current thread returns immediately, receiving the object passed to the exchange by that other thread.

If no other thread is already waiting at the exchange then the current thread is disabled for thread scheduling purposes and lies dormant until one of two things happens:

- Some other thread enters the exchange; or
- Some other thread [interrupts](../java.lang/Thread.md))the current thread.

If the current thread:

- has its interrupted status set on entry to this method; or
- is [interrupted](../java.lang/Thread.md))while waiting for the exchange,

then [InterruptedException](../java.lang/InterruptedException.md) is thrown and the current thread's interrupted status is cleared.

| Parameters ||
|-----|--------------------------|
| `x` | V:the object to exchange |

| Return ||
|---|-----------------------------------------|
| V | the object provided by the other thread |

| Exceptions ||
|----------------------------------|-----------------------------------------------------|
| `java.lang.InterruptedException` | if the current thread was interrupted while waiting |

### exchange

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun exchange(
    x: V, 
    timeout: Long, 
    unit: TimeUnit!
): V
```

Waits for another thread to arrive at this exchange point (unless the current thread is [interrupted](../java.lang/Thread.md))or the specified waiting time elapses), and then transfers the given object to it, receiving its object in return.

If another thread is already waiting at the exchange point then it is resumed for thread scheduling purposes and receives the object passed in by the current thread. The current thread returns immediately, receiving the object passed to the exchange by that other thread.

If no other thread is already waiting at the exchange then the current thread is disabled for thread scheduling purposes and lies dormant until one of three things happens:

- Some other thread enters the exchange; or
- Some other thread [interrupts](../java.lang/Thread.md))the current thread; or
- The specified waiting time elapses.

If the current thread:

- has its interrupted status set on entry to this method; or
- is [interrupted](../java.lang/Thread.md))while waiting for the exchange,

then [InterruptedException](../java.lang/InterruptedException.md) is thrown and the current thread's interrupted status is cleared.

If the specified waiting time elapses then [TimeoutException](TimeoutException.md) is thrown. If the time is less than or equal to zero, the method will not wait at all.

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------------------|
| `x` | V:the object to exchange |
| `timeout` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the maximum time to wait |
| `unit` | [TimeUnit](TimeUnit.md)!:the time unit of the`timeout`argument |
| --- | --- |

| Return ||
|---|-----------------------------------------|
| V | the object provided by the other thread |

| Exceptions ||
|-----------------------------------------|---------------------------------------------------------------------------------|
| `java.lang.InterruptedException` | if the current thread was interrupted while waiting |
| `java.util.concurrent.TimeoutException` | if the specified waiting time elapses before another thread enters the exchange |
