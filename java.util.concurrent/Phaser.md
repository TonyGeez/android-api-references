# Phaser

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Phaser

```
open class Phaser
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.util.concurrent.Phaser](../java/util/concurrent/Phaser.md) |

A reusable synchronization barrier, similar in functionality to [CyclicBarrier](../java/util/concurrent/CyclicBarrier.md) and [CountDownLatch](../java/util/concurrent/CountDownLatch.md) but supporting more flexible usage.

**Registration.** Unlike the case for other barriers, the number of parties*registered* to synchronize on a phaser may vary over time. Tasks may be registered at any time (using methods [register](../java/util/concurrent/Phaser.md)), [bulkRegister](../java/util/concurrent/Phaser.md)), or forms of constructors establishing initial numbers of parties), and optionally deregistered upon any arrival (using [arriveAndDeregister](../java/util/concurrent/Phaser.md))). As is the case with most basic synchronization constructs, registration and deregistration affect only internal counts; they do not establish any further internal bookkeeping, so tasks cannot query whether they are registered. (However, you can introduce such bookkeeping by subclassing this class.)

**Synchronization.** Like a`CyclicBarrier`, a`Phaser`may be repeatedly awaited. Method [arriveAndAwaitAdvance](../java/util/concurrent/Phaser.md))has effect analogous to java.util.concurrent.CyclicBarrier#await. Each generation of a phaser has an associated phase number. The phase number starts at zero, and advances when all parties arrive at the phaser, wrapping around to zero after reaching`Integer.MAX_VALUE`. The use of phase numbers enables independent control of actions upon arrival at a phaser and upon awaiting others, via two kinds of methods that may be invoked by any registered party:

- **Arrival.** Methods [arrive](../java/util/concurrent/Phaser.md))and [arriveAndDeregister](../java/util/concurrent/Phaser.md))record arrival. These methods do not block, but return an associated*arrival phase number* ; that is, the phase number of the phaser to which the arrival applied. When the final party for a given phase arrives, an optional action is performed and the phase advances. These actions are performed by the party triggering a phase advance, and are arranged by overriding method [onAdvance(int,int)](../java/util/concurrent/Phaser.md)), which also controls termination. Overriding this method is similar to, but more flexible than, providing a barrier action to a`CyclicBarrier`.
- **Waiting.** Method [awaitAdvance](../java/util/concurrent/Phaser.md))requires an argument indicating an arrival phase number, and returns when the phaser advances to (or is already at) a different phase. Unlike similar constructions using`CyclicBarrier`, method`awaitAdvance`continues to wait even if the waiting thread is interrupted. Interruptible and timeout versions are also available, but exceptions encountered while tasks wait interruptibly or with timeout do not change the state of the phaser. If necessary, you can perform any associated recovery within handlers of those exceptions, often after invoking`forceTermination`. Phasers may also be used by tasks executing in a [ForkJoinPool](../java/util/concurrent/ForkJoinPool.md). Progress is ensured if the pool's parallelism level can accommodate the maximum number of simultaneously blocked parties.

**Termination.** A phaser may enter a*termination* state, that may be checked using method [isTerminated](../java/util/concurrent/Phaser.md)). Upon termination, all synchronization methods immediately return without waiting for advance, as indicated by a negative return value. Similarly, attempts to register upon termination have no effect. Termination is triggered when an invocation of`onAdvance`returns`true`. The default implementation returns`true`if a deregistration has caused the number of registered parties to become zero. As illustrated below, when phasers control actions with a fixed number of iterations, it is often convenient to override this method to cause termination when the current phase number reaches a threshold. Method [forceTermination](../java/util/concurrent/Phaser.md))is also available to abruptly release waiting threads and allow them to terminate.

**Tiering.** Phasers may be*tiered*(i.e., constructed in tree structures) to reduce contention. Phasers with large numbers of parties that would otherwise experience heavy synchronization contention costs may instead be set up so that groups of sub-phasers share a common parent. This may greatly increase throughput even though it incurs greater per-operation overhead.

In a tree of tiered phasers, registration and deregistration of child phasers with their parent are managed automatically. Whenever the number of registered parties of a child phaser becomes non-zero (as established in the [Phaser(java.util.concurrent.Phaser,int)](../java/util/concurrent/Phaser.md))constructor, [register](../java/util/concurrent/Phaser.md)), or [bulkRegister](../java/util/concurrent/Phaser.md))), the child phaser is registered with its parent. Whenever the number of registered parties becomes zero as the result of an invocation of [arriveAndDeregister](../java/util/concurrent/Phaser.md)), the child phaser is deregistered from its parent.

**Monitoring.** While synchronization methods may be invoked only by registered parties, the current state of a phaser may be monitored by any caller. At any given moment there are [getRegisteredParties](../java/util/concurrent/Phaser.md))parties in total, of which [getArrivedParties](../java/util/concurrent/Phaser.md))have arrived at the current phase ([getPhase](../java/util/concurrent/Phaser.md))). When the remaining ([getUnarrivedParties](../java/util/concurrent/Phaser.md))) parties arrive, the phase advances. The values returned by these methods may reflect transient states and so are not in general useful for synchronization control. Method [toString](../java/util/concurrent/Phaser.md))returns snapshots of these state queries in a form convenient for informal monitoring.

Memory consistency effects: Actions prior to any form of arrive method [*happen-before*](../java/util/concurrent/_package.md) a corresponding phase advance and onAdvance actions (if present), which in turn*happen-before*actions following the phase advance.

**Sample usages:**

A`Phaser`may be used instead of a`CountDownLatch`to control a one-shot action serving a variable number of parties. The typical idiom is for the method setting this up to first register, then start all the actions, then deregister, as in: 

```kotlin
<code>void runTasks(List&lt;Runnable&gt; tasks) {
    Phaser startingGate = new Phaser(1); // "1" to register self
    // create and start threads
    for (Runnable task : tasks) {
      startingGate.register();
      new Thread(() -&gt; {
        startingGate.arriveAndAwaitAdvance();
        task.run();
      }).start();
    }
 
    // deregister self to allow threads to proceed
    startingGate.arriveAndDeregister();
  }</code>
```

One way to cause a set of threads to repeatedly perform actions for a given number of iterations is to override`onAdvance`: 

```kotlin
<code>void startTasks(List&lt;Runnable&gt; tasks, int iterations) {
    Phaser phaser = new Phaser() {
      protected boolean onAdvance(int phase, int registeredParties) {
        return phase &gt;= iterations - 1 || registeredParties == 0;
      }
    };
    phaser.register();
    for (Runnable task : tasks) {
      phaser.register();
      new Thread(() -&gt; {
        do {
          task.run();
          phaser.arriveAndAwaitAdvance();
        } while (!phaser.isTerminated());
      }).start();
    }
    // allow threads to proceed; don't wait for them
    phaser.arriveAndDeregister();
  }</code>
```
If the main task must later await termination, it may re-register and then execute a similar loop: 

```kotlin
<code>// ...
    phaser.register();
    while (!phaser.isTerminated())
      phaser.arriveAndAwaitAdvance();</code>
```

Related constructions may be used to await particular phase numbers in contexts where you are sure that the phase will never wrap around`Integer.MAX_VALUE`. For example: 

```kotlin
<code>void awaitPhase(Phaser phaser, int phase) {
    int p = phaser.register(); // assumes caller not already registered
    while (p &lt; phase) {
      if (phaser.isTerminated())
        // ... deal with unexpected termination
      else
        p = phaser.arriveAndAwaitAdvance();
    }
    phaser.arriveAndDeregister();
  }</code>
```

To create a set of`n`tasks using a tree of phasers, you could use code of the following form, assuming a Task class with a constructor accepting a`Phaser`that it registers with upon construction. After invocation of`build(new Task[n], 0, n, new Phaser())`, these tasks could then be started, for example by submitting to a pool: 

```kotlin
<code>void build(Task[] tasks, int lo, int hi, Phaser ph) {
    if (hi - lo &gt; TASKS_PER_PHASER) {
      for (int i = lo; i &lt; hi; i += TASKS_PER_PHASER) {
        int j = Math.min(i + TASKS_PER_PHASER, hi);
        build(tasks, i, j, new Phaser(ph));
      }
    } else {
      for (int i = lo; i &lt; hi; ++i)
        tasks[i] = new Task(ph);
        // assumes new Task(ph) performs ph.register()
    }
  }</code>
```
The best value of`TASKS_PER_PHASER`depends mainly on expected synchronization rates. A value as low as four may be appropriate for extremely small per-phase task bodies (thus high rates), or up to hundreds for extremely large ones.

**Implementation notes:** This implementation restricts the maximum number of parties to 65535. Attempts to register additional parties result in`IllegalStateException`. However, you can and should create tiered phasers to accommodate arbitrarily large sets of participants.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [Phaser](../java/util/concurrent/Phaser.md))`()` Creates a new phaser with no initially registered parties, no parent, and initial phase number 0. |
| [Phaser](../java/util/concurrent/Phaser.md))`(`parties:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a new phaser with the given number of registered unarrived parties, no parent, and initial phase number 0. |
| [Phaser](../java/util/concurrent/Phaser.md))`(`parent:` ` [Phaser](../java/util/concurrent/Phaser.md)!`)` Equivalent to [Phaser(parent, 0)](../java/util/concurrent/Phaser.md)). |
| [Phaser](../java/util/concurrent/Phaser.md))`(`parent:` ` [Phaser](../java/util/concurrent/Phaser.md)!`, `parties:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a new phaser with the given parent and number of registered unarrived parties. |

| Public methods ||
|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [arrive](../java/util/concurrent/Phaser.md))`()` Arrives at this phaser, without waiting for others to arrive. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [arriveAndAwaitAdvance](../java/util/concurrent/Phaser.md))`()` Arrives at this phaser and awaits others. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [arriveAndDeregister](../java/util/concurrent/Phaser.md))`()` Arrives at this phaser and deregisters from it without waiting for others to arrive. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [awaitAdvance](../java/util/concurrent/Phaser.md))`(`phase:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Awaits the phase of this phaser to advance from the given phase value, returning immediately if the current phase is not equal to the given phase value or this phaser is terminated. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [awaitAdvanceInterruptibly](../java/util/concurrent/Phaser.md))`(`phase:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Awaits the phase of this phaser to advance from the given phase value, throwing`InterruptedException`if interrupted while waiting, or returning immediately if the current phase is not equal to the given phase value or this phaser is terminated. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [awaitAdvanceInterruptibly](../java/util/concurrent/Phaser.md))`(`phase:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `timeout:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `unit:` ` [TimeUnit](../java/util/concurrent/TimeUnit.md)!`)` Awaits the phase of this phaser to advance from the given phase value or the given timeout to elapse, throwing`InterruptedException`if interrupted while waiting, or returning immediately if the current phase is not equal to the given phase value or this phaser is terminated. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [bulkRegister](../java/util/concurrent/Phaser.md))`(`parties:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Adds the given number of new unarrived parties to this phaser. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [forceTermination](../java/util/concurrent/Phaser.md))`()` Forces this phaser to enter termination state. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getArrivedParties](../java/util/concurrent/Phaser.md))`()` Returns the number of registered parties that have arrived at the current phase of this phaser. |
| --- | --- |
| open [Phaser](../java/util/concurrent/Phaser.md)! | [getParent](../java/util/concurrent/Phaser.md))`()` Returns the parent of this phaser, or`null`if none. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPhase](../java/util/concurrent/Phaser.md))`()` Returns the current phase number. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getRegisteredParties](../java/util/concurrent/Phaser.md))`()` Returns the number of parties registered at this phaser. |
| --- | --- |
| open [Phaser](../java/util/concurrent/Phaser.md)! | [getRoot](../java/util/concurrent/Phaser.md))`()` Returns the root ancestor of this phaser, which is the same as this phaser if it has no parent. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getUnarrivedParties](../java/util/concurrent/Phaser.md))`()` Returns the number of registered parties that have not yet arrived at the current phase of this phaser. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isTerminated](../java/util/concurrent/Phaser.md))`()` Returns`true`if this phaser has been terminated. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [register](../java/util/concurrent/Phaser.md))`()` Adds a new unarrived party to this phaser. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../java/util/concurrent/Phaser.md))`()` Returns a string identifying this phaser, as well as its state. |

| Protected methods ||
|----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onAdvance](../java/util/concurrent/Phaser.md))`(`phase:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `registeredParties:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Overridable method to perform an action upon impending phase advance, and to control termination. |

## Public constructors

### Phaser

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Phaser()
```

Creates a new phaser with no initially registered parties, no parent, and initial phase number 0. Any thread using this phaser will need to first register for it. 

### Phaser

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Phaser(parties: Int)
```

Creates a new phaser with the given number of registered unarrived parties, no parent, and initial phase number 0.

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------------------------------|
| `parties` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of parties required to advance to the next phase |

| Exceptions ||
|--------------------------------------|-----------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if parties less than zero or greater than the maximum number of parties supported |

### Phaser

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Phaser(parent: Phaser!)
```

Equivalent to [Phaser(parent, 0)](../java/util/concurrent/Phaser.md)).

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------|
| `parent` | [Phaser](../java/util/concurrent/Phaser.md)!:the parent phaser |

### Phaser

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Phaser(
    parent: Phaser!, 
    parties: Int)
```

Creates a new phaser with the given parent and number of registered unarrived parties. When the given parent is non-null and the given number of parties is greater than zero, this child phaser is registered with its parent.

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------------------------------|
| `parent` | [Phaser](../java/util/concurrent/Phaser.md)!:the parent phaser |
| `parties` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of parties required to advance to the next phase |

| Exceptions ||
|--------------------------------------|-----------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if parties less than zero or greater than the maximum number of parties supported |

## Public methods

### arrive

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun arrive(): Int
```

Arrives at this phaser, without waiting for others to arrive.

It is a usage error for an unregistered party to invoke this method. However, this error may result in an`IllegalStateException`only upon some subsequent operation on this phaser, if ever.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the arrival phase number, or a negative value if terminated |

| Exceptions ||
|-----------------------------------|-----------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | if not terminated and the number of unarrived parties would become negative |

### arriveAndAwaitAdvance

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun arriveAndAwaitAdvance(): Int
```

Arrives at this phaser and awaits others. Equivalent in effect to`awaitAdvance(arrive())`. If you need to await with interruption or timeout, you can arrange this with an analogous construction using one of the other forms of the`awaitAdvance`method. If instead you need to deregister upon arrival, use`awaitAdvance(arriveAndDeregister())`.

It is a usage error for an unregistered party to invoke this method. However, this error may result in an`IllegalStateException`only upon some subsequent operation on this phaser, if ever.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the arrival phase number, or the (negative) [current phase](../java/util/concurrent/Phaser.md))if terminated |

| Exceptions ||
|-----------------------------------|-----------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | if not terminated and the number of unarrived parties would become negative |

### arriveAndDeregister

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun arriveAndDeregister(): Int
```

Arrives at this phaser and deregisters from it without waiting for others to arrive. Deregistration reduces the number of parties required to advance in future phases. If this phaser has a parent, and deregistration causes this phaser to have zero parties, this phaser is also deregistered from its parent.

It is a usage error for an unregistered party to invoke this method. However, this error may result in an`IllegalStateException`only upon some subsequent operation on this phaser, if ever.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the arrival phase number, or a negative value if terminated |

| Exceptions ||
|-----------------------------------|-------------------------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | if not terminated and the number of registered or unarrived parties would become negative |

### awaitAdvance

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun awaitAdvance(phase: Int): Int
```

Awaits the phase of this phaser to advance from the given phase value, returning immediately if the current phase is not equal to the given phase value or this phaser is terminated.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `phase` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):an arrival phase number, or negative value if terminated; this argument is normally the value returned by a previous call to`arrive`or`arriveAndDeregister`. |

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the next arrival phase number, or the argument if it is negative, or the (negative) [current phase](../java/util/concurrent/Phaser.md))if terminated |

### awaitAdvanceInterruptibly

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun awaitAdvanceInterruptibly(phase: Int): Int
```

Awaits the phase of this phaser to advance from the given phase value, throwing`InterruptedException`if interrupted while waiting, or returning immediately if the current phase is not equal to the given phase value or this phaser is terminated.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `phase` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):an arrival phase number, or negative value if terminated; this argument is normally the value returned by a previous call to`arrive`or`arriveAndDeregister`. |

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the next arrival phase number, or the argument if it is negative, or the (negative) [current phase](../java/util/concurrent/Phaser.md))if terminated |

| Exceptions ||
|----------------------------------|-------------------------------------|
| `java.lang.InterruptedException` | if thread interrupted while waiting |

### awaitAdvanceInterruptibly

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun awaitAdvanceInterruptibly(
    phase: Int, 
    timeout: Long, 
    unit: TimeUnit!
): Int
```

Awaits the phase of this phaser to advance from the given phase value or the given timeout to elapse, throwing`InterruptedException`if interrupted while waiting, or returning immediately if the current phase is not equal to the given phase value or this phaser is terminated.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `phase` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):an arrival phase number, or negative value if terminated; this argument is normally the value returned by a previous call to`arrive`or`arriveAndDeregister`. |
| `timeout` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):how long to wait before giving up, in units of`unit` |
| `unit` | [TimeUnit](../java/util/concurrent/TimeUnit.md)!:a`TimeUnit`determining how to interpret the`timeout`parameter |
| --- | --- |

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the next arrival phase number, or the argument if it is negative, or the (negative) [current phase](../java/util/concurrent/Phaser.md))if terminated |

| Exceptions ||
|-----------------------------------------|-------------------------------------|
| `java.lang.InterruptedException` | if thread interrupted while waiting |
| `java.util.concurrent.TimeoutException` | if timed out while waiting |

### bulkRegister

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun bulkRegister(parties: Int): Int
```

Adds the given number of new unarrived parties to this phaser. If an ongoing invocation of [onAdvance](../java/util/concurrent/Phaser.md))is in progress, this method may await its completion before returning. If this phaser has a parent, and the given number of parties is greater than zero, and this phaser previously had no registered parties, this child phaser is also registered with its parent. If this phaser is terminated, the attempt to register has no effect, and a negative value is returned.

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| `parties` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of additional parties required to advance to the next phase |

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the arrival phase number to which this registration applied. If this value is negative, then this phaser has terminated, in which case registration has no effect. |

| Exceptions ||
|--------------------------------------|-----------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | if attempting to register more than the maximum supported number of parties |
| `java.lang.IllegalArgumentException` | if`parties < 0` |

### forceTermination

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun forceTermination(): Unit
```

Forces this phaser to enter termination state. Counts of registered parties are unaffected. If this phaser is a member of a tiered set of phasers, then all of the phasers in the set are terminated. If this phaser is already terminated, this method has no effect. This method may be useful for coordinating recovery after one or more tasks encounter unexpected exceptions. 

### getArrivedParties

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getArrivedParties(): Int
```

Returns the number of registered parties that have arrived at the current phase of this phaser. If this phaser has terminated, the returned value is meaningless and arbitrary.

| Return ||
|----------------------------------------------------------------------------|-------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of arrived parties |

### getParent

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getParent(): Phaser!
```

Returns the parent of this phaser, or`null`if none.

| Return ||
|----------------------------------------------------------------------------------------|--------------------------------------------|
| [Phaser](../java/util/concurrent/Phaser.md)! | the parent of this phaser, or`null`if none |

### getPhase

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPhase(): Int
```

Returns the current phase number. The maximum phase number is`Integer.MAX_VALUE`, after which it restarts at zero. Upon termination, the phase number is negative, in which case the prevailing phase prior to termination may be obtained via`getPhase() + Integer.MIN_VALUE`.

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the phase number, or a negative value if terminated |

### getRegisteredParties

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getRegisteredParties(): Int
```

Returns the number of parties registered at this phaser.

| Return ||
|----------------------------------------------------------------------------|-----------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of parties |

### getRoot

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getRoot(): Phaser!
```

Returns the root ancestor of this phaser, which is the same as this phaser if it has no parent.

| Return ||
|----------------------------------------------------------------------------------------|----------------------------------|
| [Phaser](../java/util/concurrent/Phaser.md)! | the root ancestor of this phaser |

### getUnarrivedParties

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getUnarrivedParties(): Int
```

Returns the number of registered parties that have not yet arrived at the current phase of this phaser. If this phaser has terminated, the returned value is meaningless and arbitrary.

| Return ||
|----------------------------------------------------------------------------|---------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of unarrived parties |

### isTerminated

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isTerminated(): Boolean
```

Returns`true`if this phaser has been terminated.

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this phaser has been terminated |

### register

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun register(): Int
```

Adds a new unarrived party to this phaser. If an ongoing invocation of [onAdvance](../java/util/concurrent/Phaser.md))is in progress, this method may await its completion before returning. If this phaser has a parent, and this phaser previously had no registered parties, this child phaser is also registered with its parent. If this phaser is terminated, the attempt to register has no effect, and a negative value is returned.

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the arrival phase number to which this registration applied. If this value is negative, then this phaser has terminated, in which case registration has no effect. |

| Exceptions ||
|-----------------------------------|-----------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | if attempting to register more than the maximum supported number of parties |

### toString

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

Returns a string identifying this phaser, as well as its state. The state, in brackets, includes the String`"phase = "`followed by the phase number,`"parties = "`followed by the number of registered parties, and`"arrived = "`followed by the number of arrived parties.

| Return ||
|----------------------------------------------------------------------------------|--------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string identifying this phaser, as well as its state |

## Protected methods

### onAdvance

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun onAdvance(
    phase: Int, 
    registeredParties: Int
): Boolean
```

Overridable method to perform an action upon impending phase advance, and to control termination. This method is invoked upon arrival of the party advancing this phaser (when all other waiting parties are dormant). If this method returns`true`, this phaser will be set to a final termination state upon advance, and subsequent calls to [isTerminated](../java/util/concurrent/Phaser.md))will return true. Any (unchecked) Exception or Error thrown by an invocation of this method is propagated to the party attempting to advance this phaser, in which case no advance occurs.

The arguments to this method provide the state of the phaser prevailing for the current transition. The effects of invoking arrival, registration, and waiting methods on this phaser from within`onAdvance`are unspecified and should not be relied on.

If this phaser is a member of a tiered set of phasers, then`onAdvance`is invoked only for its root phaser on each advance.

To support the most common use cases, the default implementation of this method returns`true`when the number of registered parties has become zero as the result of a party invoking`arriveAndDeregister`. You can disable this behavior, thus enabling continuation upon future registrations, by overriding this method to always return`false`: 

```kotlin
<code>Phaser phaser = new Phaser() {
    protected boolean onAdvance(int phase, int parties) { return false; }
  };</code>
```

| Parameters ||
|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `phase` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the current phase number on entry to this method, before this phaser is advanced |
| `registeredParties` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the current number of registered parties |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this phaser should terminate |
