# Runnable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Runnable

```
@FunctionalInterface interface Runnable
```

| [java.lang.Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable#) |

| Known Direct Subclasses [AnimationDrawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimationDrawable.html#), [CookieSyncManager](https://developer.android.com/reference/kotlin/android/webkit/CookieSyncManager.html#), [RenderScript.RSErrorHandler](https://developer.android.com/reference/kotlin/android/renderscript/RenderScript.RSErrorHandler.html#), [RenderScript.RSMessageHandler](https://developer.android.com/reference/kotlin/android/renderscript/RenderScript.RSMessageHandler.html#), [RunnableFuture](https://developer.android.com/reference/kotlin/java/util/concurrent/RunnableFuture.html#), [Thread](https://developer.android.com/reference/kotlin/java/lang/Thread), [TimerTask](https://developer.android.com/reference/kotlin/java/util/TimerTask.html#) |------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [AnimationDrawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimationDrawable.html#) | An object used to create frame-by-frame animations, defined by a series of Drawable objects, which can be used as a View object's background. | | [CookieSyncManager](https://developer.android.com/reference/kotlin/android/webkit/CookieSyncManager.html#) | The CookieSyncManager is used to synchronize the browser cookie store between RAM and permanent storage. | | [RenderScript.RSErrorHandler](https://developer.android.com/reference/kotlin/android/renderscript/RenderScript.RSErrorHandler.html#) | The runtime error handler base class. | | [RenderScript.RSMessageHandler](https://developer.android.com/reference/kotlin/android/renderscript/RenderScript.RSMessageHandler.html#) | The base class from which an application should derive in order to receive RS messages from scripts. | | [RunnableFuture](https://developer.android.com/reference/kotlin/java/util/concurrent/RunnableFuture.html#) | A [Future](https://developer.android.com/reference/kotlin/java/util/concurrent/Future.html#) that is [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable#). | | [Thread](https://developer.android.com/reference/kotlin/java/lang/Thread) | A*thread*is a thread of execution in a program. | | [TimerTask](https://developer.android.com/reference/kotlin/java/util/TimerTask.html#) | A task that can be scheduled for one-time or repeated execution by a [Timer](https://developer.android.com/reference/kotlin/java/util/Timer.html#). | |

| Known Indirect Subclasses [ForkJoinWorkerThread](https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinWorkerThread.html#), [FutureTask](https://developer.android.com/reference/kotlin/java/util/concurrent/FutureTask.html#), [HandlerThread](https://developer.android.com/reference/kotlin/android/os/HandlerThread.html#), [RunnableScheduledFuture](https://developer.android.com/reference/kotlin/java/util/concurrent/RunnableScheduledFuture.html#) |------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [ForkJoinWorkerThread](https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinWorkerThread.html#) | A thread managed by a [ForkJoinPool](https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinPool.html#), which executes [ForkJoinTask](https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinTask.html#) s. | | [FutureTask](https://developer.android.com/reference/kotlin/java/util/concurrent/FutureTask.html#) | A cancellable asynchronous computation. | | [HandlerThread](https://developer.android.com/reference/kotlin/android/os/HandlerThread.html#) | A [Thread](https://developer.android.com/reference/kotlin/java/lang/Thread) that has a [Looper](https://developer.android.com/reference/kotlin/android/os/Looper.html#). | | [RunnableScheduledFuture](https://developer.android.com/reference/kotlin/java/util/concurrent/RunnableScheduledFuture.html#) | A [ScheduledFuture](https://developer.android.com/reference/kotlin/java/util/concurrent/ScheduledFuture.html#) that is [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable#). | |

The`Runnable`interface should be implemented by any class whose instances are intended to be executed by a thread. The class must define a method of no arguments called`run`.

This interface is designed to provide a common protocol for objects that wish to execute code while they are active. For example,`Runnable`is implemented by class`Thread`. Being active simply means that a thread has been started and has not yet been stopped.

In addition,`Runnable`provides the means for a class to be active while not subclassing`Thread`. A class that implements`Runnable`can run without subclassing`Thread`by instantiating a`Thread`instance and passing itself in as the target. In most cases, the`Runnable`interface should be used if you are only planning to override the`run()`method and no other`Thread`methods. This is important because classes should not be subclassed unless the programmer intends on modifying or enhancing the fundamental behavior of the class.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [run](https://developer.android.com/reference/kotlin/java/lang/Runnable#run())`()` When an object implementing interface`Runnable`is used to create a thread, starting the thread causes the object's`run`method to be called in that separately executing thread. |

## Public methods

### run

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun run(): Unit
```

When an object implementing interface`Runnable`is used to create a thread, starting the thread causes the object's`run`method to be called in that separately executing thread.

The general contract of the method`run`is that it may take any action whatsoever. 
**See Also**

- [java.lang.Thread#run()](https://developer.android.com/reference/kotlin/java/lang/Thread#run())
