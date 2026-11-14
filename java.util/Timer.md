# Timer

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Timer

```
open class Timer
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.util.Timer](https://developer.android.com/reference/kotlin/java/util/Timer#) |

A facility for threads to schedule tasks for future execution in a background thread. Tasks may be scheduled for one-time execution, or for repeated execution at regular intervals.

Corresponding to each`Timer`object is a single background thread that is used to execute all of the timer's tasks, sequentially. Timer tasks should complete quickly. If a timer task takes excessive time to complete, it "hogs" the timer's task execution thread. This can, in turn, delay the execution of subsequent tasks, which may "bunch up" and execute in rapid succession when (and if) the offending task finally completes.

After the last live reference to a`Timer`object goes away*and* all outstanding tasks have completed execution, the timer's task execution thread terminates gracefully (and becomes subject to garbage collection). However, this can take arbitrarily long to occur. By default, the task execution thread does not run as a*daemon thread* , so it is capable of keeping an application from terminating. If a caller wants to terminate a timer's task execution thread rapidly, the caller should invoke the timer's`cancel`method.

If the timer's task execution thread terminates unexpectedly, for example, because its`stop`method is invoked, any further attempt to schedule a task on the timer will result in an`IllegalStateException`, as if the timer's`cancel`method had been invoked.

This class is thread-safe: multiple threads can share a single`Timer`object without the need for external synchronization.

This class does*not* offer real-time guarantees: it schedules tasks using the`Object.wait(long)`method.

Java 5.0 introduced the`java.util.concurrent`package and one of the concurrency utilities therein is the which is a thread pool for repeatedly executing tasks at a given rate or delay. It is effectively a more versatile replacement for the`Timer`/`TimerTask`combination, as it allows multiple service threads, accepts various time units, and doesn't require subclassing`TimerTask`(just implement`Runnable`). Configuring`ScheduledThreadPoolExecutor`with one thread makes it equivalent to`Timer`.

Implementation note: This class scales to large numbers of concurrently scheduled tasks (thousands should present no problem). Internally, it uses a binary heap to represent its task queue, so the cost to schedule a task is O(log n), where n is the number of concurrently scheduled tasks.

Implementation note: All constructors start a timer thread.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [Timer](https://developer.android.com/reference/kotlin/java/util/Timer#Timer())`()` Creates a new timer. |
| [Timer](https://developer.android.com/reference/kotlin/java/util/Timer#Timer(kotlin.Boolean))`(`isDaemon:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Creates a new timer whose associated thread may be specified to [run as a daemon](https://developer.android.com/reference/kotlin/java/lang/Thread.html#setDaemon(kotlin.Boolean)). |
| [Timer](https://developer.android.com/reference/kotlin/java/util/Timer#Timer(kotlin.String))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Creates a new timer whose associated thread has the specified name. |
| [Timer](https://developer.android.com/reference/kotlin/java/util/Timer#Timer(kotlin.String,%20kotlin.Boolean))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `isDaemon:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Creates a new timer whose associated thread has the specified name, and may be specified to [run as a daemon](https://developer.android.com/reference/kotlin/java/lang/Thread.html#setDaemon(kotlin.Boolean)). |

| Public methods ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [cancel](https://developer.android.com/reference/kotlin/java/util/Timer#cancel())`()` Terminates this timer, discarding any currently scheduled tasks. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [purge](https://developer.android.com/reference/kotlin/java/util/Timer#purge())`()` Removes all cancelled tasks from this timer's task queue. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [schedule](https://developer.android.com/reference/kotlin/java/util/Timer#schedule(java.util.TimerTask,%20java.util.Date))`(`task:` ` [TimerTask](https://developer.android.com/reference/kotlin/java/util/TimerTask)!`, `time:` ` [Date](https://developer.android.com/reference/kotlin/java/util/Date)!`)` Schedules the specified task for execution at the specified time. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [schedule](https://developer.android.com/reference/kotlin/java/util/Timer#schedule(java.util.TimerTask,%20java.util.Date,%20kotlin.Long))`(`task:` ` [TimerTask](https://developer.android.com/reference/kotlin/java/util/TimerTask)!`, `firstTime:` ` [Date](https://developer.android.com/reference/kotlin/java/util/Date)!`, `period:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Schedules the specified task for repeated*fixed-delay execution*, beginning at the specified time. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [schedule](https://developer.android.com/reference/kotlin/java/util/Timer#schedule(java.util.TimerTask,%20kotlin.Long))`(`task:` ` [TimerTask](https://developer.android.com/reference/kotlin/java/util/TimerTask)!`, `delay:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Schedules the specified task for execution after the specified delay. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [schedule](https://developer.android.com/reference/kotlin/java/util/Timer#schedule(java.util.TimerTask,%20kotlin.Long,%20kotlin.Long))`(`task:` ` [TimerTask](https://developer.android.com/reference/kotlin/java/util/TimerTask)!`, `delay:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `period:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Schedules the specified task for repeated*fixed-delay execution*, beginning after the specified delay. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [scheduleAtFixedRate](https://developer.android.com/reference/kotlin/java/util/Timer#scheduleAtFixedRate(java.util.TimerTask,%20java.util.Date,%20kotlin.Long))`(`task:` ` [TimerTask](https://developer.android.com/reference/kotlin/java/util/TimerTask)!`, `firstTime:` ` [Date](https://developer.android.com/reference/kotlin/java/util/Date)!`, `period:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Schedules the specified task for repeated*fixed-rate execution*, beginning at the specified time. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [scheduleAtFixedRate](https://developer.android.com/reference/kotlin/java/util/Timer#scheduleAtFixedRate(java.util.TimerTask,%20kotlin.Long,%20kotlin.Long))`(`task:` ` [TimerTask](https://developer.android.com/reference/kotlin/java/util/TimerTask)!`, `delay:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `period:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Schedules the specified task for repeated*fixed-rate execution*, beginning after the specified delay. |

## Public constructors

### Timer

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Timer()
```

Creates a new timer. The associated thread does*not* [run as a daemon](https://developer.android.com/reference/kotlin/java/lang/Thread.html#setDaemon(kotlin.Boolean)). 

### Timer

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Timer(isDaemon: Boolean)
```

Creates a new timer whose associated thread may be specified to [run as a daemon](https://developer.android.com/reference/kotlin/java/lang/Thread.html#setDaemon(kotlin.Boolean)). A daemon thread is called for if the timer will be used to schedule repeating "maintenance activities", which must be performed as long as the application is running, but should not prolong the lifetime of the application.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------|
| `isDaemon` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):true if the associated thread should run as a daemon. |

### Timer

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Timer(name: String!)
```

Creates a new timer whose associated thread has the specified name. The associated thread does*not* [run as a daemon](https://developer.android.com/reference/kotlin/java/lang/Thread.html#setDaemon(kotlin.Boolean)).

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the associated thread |

| Exceptions ||
|----------------------------------|-----------------|
| `java.lang.NullPointerException` | if`name`is null |

### Timer

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Timer(
    name: String!, 
    isDaemon: Boolean)
```

Creates a new timer whose associated thread has the specified name, and may be specified to [run as a daemon](https://developer.android.com/reference/kotlin/java/lang/Thread.html#setDaemon(kotlin.Boolean)).

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the associated thread |
| `isDaemon` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):true if the associated thread should run as a daemon |

| Exceptions ||
|----------------------------------|-----------------|
| `java.lang.NullPointerException` | if`name`is null |

## Public methods

### cancel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun cancel(): Unit
```

Terminates this timer, discarding any currently scheduled tasks. Does not interfere with a currently executing task (if it exists). Once a timer has been terminated, its execution thread terminates gracefully, and no more tasks may be scheduled on it.

Note that calling this method from within the run method of a timer task that was invoked by this timer absolutely guarantees that the ongoing task execution is the last task execution that will ever be performed by this timer.

This method may be called repeatedly; the second and subsequent calls have no effect. 

### purge

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun purge(): Int
```

Removes all cancelled tasks from this timer's task queue.*Calling this method has no effect on the behavior of the timer*, but eliminates the references to the cancelled tasks from the queue. If there are no external references to these tasks, they become eligible for garbage collection.

Most programs will have no need to call this method. It is designed for use by the rare application that cancels a large number of tasks. Calling this method trades time for space: the runtime of the method may be proportional to n + c log n, where n is the number of tasks in the queue and c is the number of cancelled tasks.

Note that it is permissible to call this method from within a task scheduled on this timer.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of tasks removed from the queue. |

### schedule

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun schedule(
    task: TimerTask!, 
    time: Date!
): Unit
```

Schedules the specified task for execution at the specified time. If the time is in the past, the task is scheduled for immediate execution.

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------|
| `task` | [TimerTask](https://developer.android.com/reference/kotlin/java/util/TimerTask)!:task to be scheduled. |
| `time` | [Date](https://developer.android.com/reference/kotlin/java/util/Date)!:time at which task is to be executed. |

| Exceptions ||
|--------------------------------------|----------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if`time.getTime()`is negative. |
| `java.lang.IllegalStateException` | if task was already scheduled or cancelled, timer was cancelled, or timer thread terminated. |
| `java.lang.NullPointerException` | if`task`or`time`is null |
| --- | --- |

### schedule

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun schedule(
    task: TimerTask!, 
    firstTime: Date!, 
    period: Long
): Unit
```

Schedules the specified task for repeated*fixed-delay execution*, beginning at the specified time. Subsequent executions take place at approximately regular intervals, separated by the specified period.

In fixed-delay execution, each execution is scheduled relative to the actual execution time of the previous execution. If an execution is delayed for any reason (such as garbage collection or other background activity), subsequent executions will be delayed as well. In the long run, the frequency of execution will generally be slightly lower than the reciprocal of the specified period (assuming the system clock underlying`Object.wait(long)`is accurate). As a consequence of the above, if the scheduled first time is in the past, it is scheduled for immediate execution.

Fixed-delay execution is appropriate for recurring activities that require "smoothness." In other words, it is appropriate for activities where it is more important to keep the frequency accurate in the short run than in the long run. This includes most animation tasks, such as blinking a cursor at regular intervals. It also includes tasks wherein regular activity is performed in response to human input, such as automatically repeating a character as long as a key is held down.

| Parameters ||
|-------------|---------------------------------------------------------------------------------------------------------------------------------------|
| `task` | [TimerTask](https://developer.android.com/reference/kotlin/java/util/TimerTask)!:task to be scheduled. |
| `firstTime` | [Date](https://developer.android.com/reference/kotlin/java/util/Date)!:First time at which task is to be executed. |
| `period` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):time in milliseconds between successive task executions. |
| --- | --- |

| Exceptions ||
|--------------------------------------|----------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if`firstTime.getTime() < 0`, or`period <= 0` |
| `java.lang.IllegalStateException` | if task was already scheduled or cancelled, timer was cancelled, or timer thread terminated. |
| `java.lang.NullPointerException` | if`task`or`firstTime`is null |
| --- | --- |

### schedule

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun schedule(
    task: TimerTask!, 
    delay: Long
): Unit
```

Schedules the specified task for execution after the specified delay.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------------------|
| `task` | [TimerTask](https://developer.android.com/reference/kotlin/java/util/TimerTask)!:task to be scheduled. |
| `delay` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):delay in milliseconds before task is to be executed. |

| Exceptions ||
|--------------------------------------|----------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if`delay`is negative, or`delay + System.currentTimeMillis()`is negative. |
| `java.lang.IllegalStateException` | if task was already scheduled or cancelled, timer was cancelled, or timer thread terminated. |
| `java.lang.NullPointerException` | if`task`is null |
| --- | --- |

### schedule

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun schedule(
    task: TimerTask!, 
    delay: Long, 
    period: Long
): Unit
```

Schedules the specified task for repeated*fixed-delay execution*, beginning after the specified delay. Subsequent executions take place at approximately regular intervals separated by the specified period.

In fixed-delay execution, each execution is scheduled relative to the actual execution time of the previous execution. If an execution is delayed for any reason (such as garbage collection or other background activity), subsequent executions will be delayed as well. In the long run, the frequency of execution will generally be slightly lower than the reciprocal of the specified period (assuming the system clock underlying`Object.wait(long)`is accurate).

Fixed-delay execution is appropriate for recurring activities that require "smoothness." In other words, it is appropriate for activities where it is more important to keep the frequency accurate in the short run than in the long run. This includes most animation tasks, such as blinking a cursor at regular intervals. It also includes tasks wherein regular activity is performed in response to human input, such as automatically repeating a character as long as a key is held down.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------|
| `task` | [TimerTask](https://developer.android.com/reference/kotlin/java/util/TimerTask)!:task to be scheduled. |
| `delay` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):delay in milliseconds before task is to be executed. |
| `period` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):time in milliseconds between successive task executions. |
| --- | --- |

| Exceptions ||
|--------------------------------------|----------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if`delay < 0`, or`delay + System.currentTimeMillis() < 0`, or`period <= 0` |
| `java.lang.IllegalStateException` | if task was already scheduled or cancelled, timer was cancelled, or timer thread terminated. |
| `java.lang.NullPointerException` | if`task`is null |
| --- | --- |

### scheduleAtFixedRate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun scheduleAtFixedRate(
    task: TimerTask!, 
    firstTime: Date!, 
    period: Long
): Unit
```

Schedules the specified task for repeated*fixed-rate execution*, beginning at the specified time. Subsequent executions take place at approximately regular intervals, separated by the specified period.

In fixed-rate execution, each execution is scheduled relative to the scheduled execution time of the initial execution. If an execution is delayed for any reason (such as garbage collection or other background activity), two or more executions will occur in rapid succession to "catch up." In the long run, the frequency of execution will be exactly the reciprocal of the specified period (assuming the system clock underlying`Object.wait(long)`is accurate). As a consequence of the above, if the scheduled first time is in the past, then any "missed" executions will be scheduled for immediate "catch up" execution.

Fixed-rate execution is appropriate for recurring activities that are sensitive to*absolute*time, such as ringing a chime every hour on the hour, or running scheduled maintenance every day at a particular time. It is also appropriate for recurring activities where the total time to perform a fixed number of executions is important, such as a countdown timer that ticks once every second for ten seconds. Finally, fixed-rate execution is appropriate for scheduling multiple repeating timer tasks that must remain synchronized with respect to one another.

| Parameters ||
|-------------|---------------------------------------------------------------------------------------------------------------------------------------|
| `task` | [TimerTask](https://developer.android.com/reference/kotlin/java/util/TimerTask)!:task to be scheduled. |
| `firstTime` | [Date](https://developer.android.com/reference/kotlin/java/util/Date)!:First time at which task is to be executed. |
| `period` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):time in milliseconds between successive task executions. |
| --- | --- |

| Exceptions ||
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if`firstTime.getTime() < 0`or`period <= 0` |
| `java.lang.IllegalStateException` | if task was already scheduled or cancelled, timer was cancelled, or timer thread terminated. |
| `java.lang.NullPointerException` | if`task`or`firstTime`is null Since API level 31: If the app is frozen by the Android cached apps freezer before the fixed rate task is done or canceled, the task may run many times immediately when the app unfreezes, just as if a single execution of the command had taken the duration of the frozen period to execute. Since API level 36: If any execution of this task takes longer than its period, then the subsequent execution will be scheduled for the most recent missed period. Additionally, since there may be at most one "catch up" task and never two or more "catch up" tasks happening in rapid succession, if the scheduled first time is multiple periods in the past, then only one "catch up" task will be scheduled for immediate execution. |
| --- | --- |

### scheduleAtFixedRate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun scheduleAtFixedRate(
    task: TimerTask!, 
    delay: Long, 
    period: Long
): Unit
```

Schedules the specified task for repeated*fixed-rate execution*, beginning after the specified delay. Subsequent executions take place at approximately regular intervals, separated by the specified period.

In fixed-rate execution, each execution is scheduled relative to the scheduled execution time of the initial execution. If an execution is delayed for any reason (such as garbage collection or other background activity), two or more executions will occur in rapid succession to "catch up." In the long run, the frequency of execution will be exactly the reciprocal of the specified period (assuming the system clock underlying`Object.wait(long)`is accurate).

Fixed-rate execution is appropriate for recurring activities that are sensitive to*absolute*time, such as ringing a chime every hour on the hour, or running scheduled maintenance every day at a particular time. It is also appropriate for recurring activities where the total time to perform a fixed number of executions is important, such as a countdown timer that ticks once every second for ten seconds. Finally, fixed-rate execution is appropriate for scheduling multiple repeating timer tasks that must remain synchronized with respect to one another.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------|
| `task` | [TimerTask](https://developer.android.com/reference/kotlin/java/util/TimerTask)!:task to be scheduled. |
| `delay` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):delay in milliseconds before task is to be executed. |
| `period` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):time in milliseconds between successive task executions. |
| --- | --- |

| Exceptions ||
|--------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if`delay < 0`, or`delay + System.currentTimeMillis() < 0`, or`period <= 0` |
| `java.lang.IllegalStateException` | if task was already scheduled or cancelled, timer was cancelled, or timer thread terminated. |
| `java.lang.NullPointerException` | if`task`is null Since API level 31: If the app is frozen by the Android cached apps freezer before the fixed rate task is done or canceled, the task may run many times immediately when the app unfreezes, just as if a single execution of the command had taken the duration of the frozen period to execute. Since API level 36: If any execution of this task takes longer than its period, then the subsequent execution will be scheduled for the most recent missed period. |
| --- | --- |
