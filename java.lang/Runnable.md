# Runnable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Runnable

```
@FunctionalInterface interface Runnable
```

| [java.lang.Runnable](../java/lang/Runnable.md) |

| Known Direct Subclasses [AnimationDrawable](../android/graphics/drawable/AnimationDrawable.md), [CookieSyncManager](../android/webkit/CookieSyncManager.md), [RenderScript.RSErrorHandler](../android/renderscript/RenderScript.RSErrorHandler.md), [RenderScript.RSMessageHandler](../android/renderscript/RenderScript.RSMessageHandler.md), [RunnableFuture](../java/util/concurrent/RunnableFuture.md), [Thread](../java/lang/Thread.md), [TimerTask](../java/util/TimerTask.md) |------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [AnimationDrawable](../android/graphics/drawable/AnimationDrawable.md) | An object used to create frame-by-frame animations, defined by a series of Drawable objects, which can be used as a View object's background. | | [CookieSyncManager](../android/webkit/CookieSyncManager.md) | The CookieSyncManager is used to synchronize the browser cookie store between RAM and permanent storage. | | [RenderScript.RSErrorHandler](../android/renderscript/RenderScript.RSErrorHandler.md) | The runtime error handler base class. | | [RenderScript.RSMessageHandler](../android/renderscript/RenderScript.RSMessageHandler.md) | The base class from which an application should derive in order to receive RS messages from scripts. | | [RunnableFuture](../java/util/concurrent/RunnableFuture.md) | A [Future](../java/util/concurrent/Future.md) that is [Runnable](../java/lang/Runnable.md). | | [Thread](../java/lang/Thread.md) | A*thread*is a thread of execution in a program. | | [TimerTask](../java/util/TimerTask.md) | A task that can be scheduled for one-time or repeated execution by a [Timer](../java/util/Timer.md). | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [ForkJoinWorkerThread](../java/util/concurrent/ForkJoinWorkerThread.md), [FutureTask](../java/util/concurrent/FutureTask.md), [HandlerThread](../android/os/HandlerThread.md), [RunnableScheduledFuture](../java/util/concurrent/RunnableScheduledFuture.md) |------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [ForkJoinWorkerThread](../java/util/concurrent/ForkJoinWorkerThread.md) | A thread managed by a [ForkJoinPool](../java/util/concurrent/ForkJoinPool.md), which executes [ForkJoinTask](../java/util/concurrent/ForkJoinTask.md) s. | | [FutureTask](../java/util/concurrent/FutureTask.md) | A cancellable asynchronous computation. | | [HandlerThread](../android/os/HandlerThread.md) | A [Thread](../java/lang/Thread.md) that has a [Looper](../android/os/Looper.md). | | [RunnableScheduledFuture](../java/util/concurrent/RunnableScheduledFuture.md) | A [ScheduledFuture](../java/util/concurrent/ScheduledFuture.md) that is [Runnable](../java/lang/Runnable.md). | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

The`Runnable`interface should be implemented by any class whose instances are intended to be executed by a thread. The class must define a method of no arguments called`run`.

This interface is designed to provide a common protocol for objects that wish to execute code while they are active. For example,`Runnable`is implemented by class`Thread`. Being active simply means that a thread has been started and has not yet been stopped.

In addition,`Runnable`provides the means for a class to be active while not subclassing`Thread`. A class that implements`Runnable`can run without subclassing`Thread`by instantiating a`Thread`instance and passing itself in as the target. In most cases, the`Runnable`interface should be used if you are only planning to override the`run()`method and no other`Thread`methods. This is important because classes should not be subclassed unless the programmer intends on modifying or enhancing the fundamental behavior of the class.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [run](../java/lang/Runnable.md))`()` When an object implementing interface`Runnable`is used to create a thread, starting the thread causes the object's`run`method to be called in that separately executing thread. |

## Public methods

### run

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun run(): Unit
```

When an object implementing interface`Runnable`is used to create a thread, starting the thread causes the object's`run`method to be called in that separately executing thread.

The general contract of the method`run`is that it may take any action whatsoever. 
**See Also**

- [java.lang.Thread#run()](../java/lang/Thread.md))
