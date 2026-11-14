# TimerTask

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TimerTask

```
abstract class TimerTask : Runnable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.util.TimerTask](TimerTask.md) |

A task that can be scheduled for one-time or repeated execution by a [Timer](Timer.md).

A timer task is*not* reusable. Once a task has been scheduled for execution on a`Timer`or cancelled, subsequent attempts to schedule it for execution will throw`IllegalStateException`.

## Summary

| Protected constructors ||
|---------------------------------------------------------------------------------------------------------------------------|---|
| [TimerTask](TimerTask.md))`()` Creates a new timer task. |

| Public methods ||
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [cancel](TimerTask.md))`()` Cancels this timer task. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [run](TimerTask.md))`()` The action to be performed by this timer task. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [scheduledExecutionTime](TimerTask.md))`()` Returns the*scheduled* execution time of the most recent*actual*execution of this task. |
| --- | --- |

## Protected constructors

### TimerTask

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected TimerTask()
```

Creates a new timer task.

## Public methods

### cancel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun cancel(): Boolean
```

Cancels this timer task. If the task has been scheduled for one-time execution and has not yet run, or has not yet been scheduled, it will never run. If the task has been scheduled for repeated execution, it will never run again. (If the task is running when this call occurs, the task will run to completion, but will never run again.)

Note that calling this method from within the`run`method of a repeating timer task absolutely guarantees that the timer task will not run again.

This method may be called repeatedly; the second and subsequent calls have no effect.

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if this task is scheduled for one-time execution and has not yet run, or this task is scheduled for repeated execution. Returns false if the task was scheduled for one-time execution and has already run, or if the task was never scheduled, or if the task was already cancelled. (Loosely speaking, this method returns`true`if it prevents one or more scheduled executions from taking place.) |

### run

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun run(): Unit
```

The action to be performed by this timer task. 

### scheduledExecutionTime

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun scheduledExecutionTime(): Long
```

Returns the*scheduled* execution time of the most recent*actual*execution of this task. (If this method is invoked while task execution is in progress, the return value is the scheduled execution time of the ongoing task execution.)

This method is typically invoked from within a task's run method, to determine whether the current execution of the task is sufficiently timely to warrant performing the scheduled activity: 

```kotlin
<code>public void run() {
        if (System.currentTimeMillis() - scheduledExecutionTime() &gt;=
            MAX_TARDINESS)
                return;  // Too late; skip this execution.
        // Perform the task
    }
  </code>
```
This method is typically*not* used in conjunction with*fixed-delay execution* repeating tasks, as their scheduled execution times are allowed to drift over time, and so are not terribly significant.

| Return ||
|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the time at which the most recent execution of this task was scheduled to occur, in the format returned by Date.getTime(). The return value is undefined if the task has yet to commence its first execution. |

**See Also**

- [java.util.Date#getTime()](Date.md))
