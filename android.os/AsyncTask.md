Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AsyncTask

```
abstract class AsyncTask<Params : Any!, Progress : Any!, Result : Any!>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.os.AsyncTask](https://developer.android.com/reference/kotlin/android/os/AsyncTask#) |

> [!CAUTION]
> **This class was deprecated in API level 30.**
>
> Use the standard `java.util.concurrent` or [Kotlin concurrency utilities](https://developer.android.com/topic/libraries/architecture/coroutines) instead.

AsyncTask was intended to enable proper and easy use of the UI thread. However, the most common use case was for integrating into UI, and that would cause Context leaks, missed callbacks, or crashes on configuration changes. It also has inconsistent behavior on different versions of the platform, swallows exceptions from `doInBackground`, and does not provide much utility over using `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`s directly.

AsyncTask is designed to be a helper class around `https://developer.android.com/reference/kotlin/java/lang/Thread.html#` and `https://developer.android.com/reference/kotlin/android/os/Handler` and does not constitute a generic threading framework. AsyncTasks should ideally be used for short operations (a few seconds at the most.) If you need to keep threads running for long periods of time, it is highly recommended you use the various APIs provided by the `java.util.concurrent` package such as `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, `https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadPoolExecutor.html#` and `https://developer.android.com/reference/kotlin/java/util/concurrent/FutureTask.html#`.

An asynchronous task is defined by a computation that runs on a background thread and whose result is published on the UI thread. An asynchronous task is defined by 3 generic types, called `Params`, `Progress` and `Result`, and 4 steps, called `onPreExecute`, `doInBackground`, `onProgressUpdate` and `onPostExecute`.

> [!NOTE]
>
> ### Developer Guides
>
> For more information about using tasks and threads, read the [Processes and Threads](https://developer.android.com/guide/components/processes-and-threads.html) developer guide.

## Usage

AsyncTask must be subclassed to be used. The subclass will override at least one method (`https://developer.android.com/reference/kotlin/android/os/AsyncTask#doInBackground(android.os.AsyncTask.Params)`), and most often will override a second one (`https://developer.android.com/reference/kotlin/android/os/AsyncTask#onPostExecute(android.os.AsyncTask.Result)`.)

Here is an example of subclassing:

```kotlin
private class DownloadFilesTask extends AsyncTask<URL, Integer, Long> {
      protected Long doInBackground(URL... urls) {
          int count = urls.length;
          long totalSize = 0;
          for (int i = 0; i < count; i++) {
              totalSize += Downloader.downloadFile(urls[i]);
              publishProgress((int) ((i / (float) count) * 100));
              // Escape early if cancel() is called
              if (isCancelled()) break;
          }
          return totalSize;
      }
 
      protected void onProgressUpdate(Integer... progress) {
          setProgressPercent(progress[0]);
      }
 
      protected void onPostExecute(Long result) {
          showDialog("Downloaded " + result + " bytes");
      }
  }
  
```

Once created, a task is executed very simply:

```kotlin
new DownloadFilesTask().execute(url1, url2, url3);
  
```

## AsyncTask's generic types

The three types used by an asynchronous task are the following:

1. `Params`, the type of the parameters sent to the task upon execution.
2. `Progress`, the type of the progress units published during the background computation.
3. `Result`, the type of the result of the background computation.

Not all types are always used by an asynchronous task. To mark a type as unused, simply use the type `https://developer.android.com/reference/kotlin/java/lang/Void.html#`:

```kotlin
private class MyTask extends AsyncTask<Void, Void, Void> { ... }
  
```

## The 4 steps

When an asynchronous task is executed, the task goes through 4 steps:

1. `https://developer.android.com/reference/kotlin/android/os/AsyncTask#onPreExecute()`, invoked on the UI thread before the task is executed. This step is normally used to setup the task, for instance by showing a progress bar in the user interface.
2. `https://developer.android.com/reference/kotlin/android/os/AsyncTask#doInBackground(android.os.AsyncTask.Params)`, invoked on the background thread immediately after `https://developer.android.com/reference/kotlin/android/os/AsyncTask#onPreExecute()` finishes executing. This step is used to perform background computation that can take a long time. The parameters of the asynchronous task are passed to this step. The result of the computation must be returned by this step and will be passed back to the last step. This step can also use `https://developer.android.com/reference/kotlin/android/os/AsyncTask#publishProgress(android.os.AsyncTask.Progress)` to publish one or more units of progress. These values are published on the UI thread, in the `https://developer.android.com/reference/kotlin/android/os/AsyncTask#onProgressUpdate(android.os.AsyncTask.Progress)` step.
3. `https://developer.android.com/reference/kotlin/android/os/AsyncTask#onProgressUpdate(android.os.AsyncTask.Progress)`, invoked on the UI thread after a call to `https://developer.android.com/reference/kotlin/android/os/AsyncTask#publishProgress(android.os.AsyncTask.Progress)`. The timing of the execution is undefined. This method is used to display any form of progress in the user interface while the background computation is still executing. For instance, it can be used to animate a progress bar or show logs in a text field.
4. `https://developer.android.com/reference/kotlin/android/os/AsyncTask#onPostExecute(android.os.AsyncTask.Result)`, invoked on the UI thread after the background computation finishes. The result of the background computation is passed to this step as a parameter.

## Cancelling a task

A task can be cancelled at any time by invoking `https://developer.android.com/reference/kotlin/android/os/AsyncTask#cancel(kotlin.Boolean)`. Invoking this method will cause subsequent calls to `https://developer.android.com/reference/kotlin/android/os/AsyncTask#isCancelled()` to return true. After invoking this method, `https://developer.android.com/reference/kotlin/android/os/AsyncTask#onCancelled(android.os.AsyncTask.Result)`, instead of `https://developer.android.com/reference/kotlin/android/os/AsyncTask#onPostExecute(android.os.AsyncTask.Result)` will be invoked after `https://developer.android.com/reference/kotlin/android/os/AsyncTask#doInBackground(android.os.AsyncTask.Params)` returns. To ensure that a task is cancelled as quickly as possible, you should always check the return value of `https://developer.android.com/reference/kotlin/android/os/AsyncTask#isCancelled()` periodically from `https://developer.android.com/reference/kotlin/android/os/AsyncTask#doInBackground(android.os.AsyncTask.Params)`, if possible (inside a loop for instance.)

## Threading rules

There are a few threading rules that must be followed for this class to work properly:

- The AsyncTask class must be loaded on the UI thread. This is done automatically as of `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES#JELLY_BEAN:kotlin.Int`.
- The task instance must be created on the UI thread.
- execute must be invoked on the UI thread.
- Do not call `https://developer.android.com/reference/kotlin/android/os/AsyncTask#onPreExecute()`, `https://developer.android.com/reference/kotlin/android/os/AsyncTask#onPostExecute(android.os.AsyncTask.Result)`, `https://developer.android.com/reference/kotlin/android/os/AsyncTask#doInBackground(android.os.AsyncTask.Params)`, `https://developer.android.com/reference/kotlin/android/os/AsyncTask#onProgressUpdate(android.os.AsyncTask.Progress)` manually.
- The task can be executed only once (an exception will be thrown if a second execution is attempted.)

## Memory observability

AsyncTask guarantees that all callback calls are synchronized to ensure the following without explicit synchronizations.

- The memory effects of `https://developer.android.com/reference/kotlin/android/os/AsyncTask#onPreExecute()`, and anything else executed before the call to #execute, including the construction of the AsyncTask object, are visible to `https://developer.android.com/reference/kotlin/android/os/AsyncTask#doInBackground(android.os.AsyncTask.Params)`.
- The memory effects of `https://developer.android.com/reference/kotlin/android/os/AsyncTask#doInBackground(android.os.AsyncTask.Params)` are visible to `https://developer.android.com/reference/kotlin/android/os/AsyncTask#onPostExecute(android.os.AsyncTask.Result)`.
- Any memory effects of `https://developer.android.com/reference/kotlin/android/os/AsyncTask#doInBackground(android.os.AsyncTask.Params)` preceding a call to `https://developer.android.com/reference/kotlin/android/os/AsyncTask#publishProgress(android.os.AsyncTask.Progress)` are visible to the corresponding `https://developer.android.com/reference/kotlin/android/os/AsyncTask#onProgressUpdate(android.os.AsyncTask.Progress)` call. (But `https://developer.android.com/reference/kotlin/android/os/AsyncTask#doInBackground(android.os.AsyncTask.Params)` continues to run, and care needs to be taken that later updates in `https://developer.android.com/reference/kotlin/android/os/AsyncTask#doInBackground(android.os.AsyncTask.Params)` do not interfere with an in-progress `https://developer.android.com/reference/kotlin/android/os/AsyncTask#onProgressUpdate(android.os.AsyncTask.Progress)` call.)
- Any memory effects preceding a call to `https://developer.android.com/reference/kotlin/android/os/AsyncTask#cancel(kotlin.Boolean)` are visible after a call to `https://developer.android.com/reference/kotlin/android/os/AsyncTask#isCancelled()` that returns true as a result, or during and after a resulting call to #onCancelled.

## Order of execution

When first introduced, AsyncTasks were executed serially on a single background thread. Starting with `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES#DONUT:kotlin.Int`, this was changed to a pool of threads allowing multiple tasks to operate in parallel. Starting with `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES#HONEYCOMB:kotlin.Int`, tasks are executed on a single thread to avoid common application errors caused by parallel execution.

If you truly want parallel execution, you can invoke `https://developer.android.com/reference/kotlin/android/os/AsyncTask#executeOnExecutor(java.util.concurrent.Executor,%20android.os.AsyncTask.Params)` with `https://developer.android.com/reference/kotlin/android/os/AsyncTask#THREAD_POOL_EXECUTOR:java.util.concurrent.Executor`.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/os/AsyncTask.Status` Indicates the current status of the task. |

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/os/AsyncTask#AsyncTask()()` Creates a new asynchronous task. |

| Public methods ||
|---|---|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/os/AsyncTask#cancel(kotlin.Boolean)(mayInterruptIfRunning: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Attempts to cancel execution of this task. |
| [AsyncTask](https://developer.android.com/reference/kotlin/android/os/AsyncTask#)\<Params, Progress, Result\>! | `https://developer.android.com/reference/kotlin/android/os/AsyncTask#execute(android.os.AsyncTask.Params)(vararg params: Params)` Executes the task with the specified parameters. |
| open static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/os/AsyncTask#execute(java.lang.Runnable)(runnable: https://developer.android.com/reference/kotlin/java/lang/Runnable.html#!)` Convenience version of `https://developer.android.com/reference/kotlin/android/os/AsyncTask#execute(android.os.AsyncTask.Params)` for use with a simple Runnable object. |
| [AsyncTask](https://developer.android.com/reference/kotlin/android/os/AsyncTask#)\<Params, Progress, Result\>! | `https://developer.android.com/reference/kotlin/android/os/AsyncTask#executeOnExecutor(java.util.concurrent.Executor,%20android.os.AsyncTask.Params)(exec: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#!, vararg params: Params)` Executes the task with the specified parameters. |
| Result | `https://developer.android.com/reference/kotlin/android/os/AsyncTask#get()()` Waits if necessary for the computation to complete, and then retrieves its result. |
| Result | `https://developer.android.com/reference/kotlin/android/os/AsyncTask#get(kotlin.Long,%20java.util.concurrent.TimeUnit)(timeout: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html, unit: https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit.html#!)` Waits if necessary for at most the given time for the computation to complete, and then retrieves its result. |
| [AsyncTask.Status](https://developer.android.com/reference/kotlin/android/os/AsyncTask.Status)! | `https://developer.android.com/reference/kotlin/android/os/AsyncTask#getStatus()()` Returns the current status of this task. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/os/AsyncTask#isCancelled()()` Returns true if this task was cancelled before it completed normally. |

| Protected methods ||
|---|---|
| abstract Result | `https://developer.android.com/reference/kotlin/android/os/AsyncTask#doInBackground(android.os.AsyncTask.Params)(vararg params: Params)` Override this method to perform a computation on a background thread. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/os/AsyncTask#onCancelled()()` Applications should preferably override `https://developer.android.com/reference/kotlin/android/os/AsyncTask#onCancelled(android.os.AsyncTask.Result)`. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/os/AsyncTask#onCancelled(android.os.AsyncTask.Result)(result: Result)` Runs on the UI thread after `https://developer.android.com/reference/kotlin/android/os/AsyncTask#cancel(kotlin.Boolean)` is invoked and `https://developer.android.com/reference/kotlin/android/os/AsyncTask#doInBackground(android.os.AsyncTask.Params)` has finished. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/os/AsyncTask#onPostExecute(android.os.AsyncTask.Result)(result: Result)` Runs on the UI thread after `https://developer.android.com/reference/kotlin/android/os/AsyncTask#doInBackground(android.os.AsyncTask.Params)`. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/os/AsyncTask#onPreExecute()()` Runs on the UI thread before `https://developer.android.com/reference/kotlin/android/os/AsyncTask#doInBackground(android.os.AsyncTask.Params)`. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/os/AsyncTask#onProgressUpdate(android.os.AsyncTask.Progress)(vararg values: Progress)` Runs on the UI thread after `https://developer.android.com/reference/kotlin/android/os/AsyncTask#publishProgress(android.os.AsyncTask.Progress)` is invoked. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/os/AsyncTask#publishProgress(android.os.AsyncTask.Progress)(vararg values: Progress)` This method can be invoked from `https://developer.android.com/reference/kotlin/android/os/AsyncTask#doInBackground(android.os.AsyncTask.Params)` to publish updates on the UI thread while the background computation is still running. |

| Properties ||
|---|---|
| static [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#)! | `https://developer.android.com/reference/kotlin/android/os/AsyncTask#SERIAL_EXECUTOR:java.util.concurrent.Executor` An `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that executes tasks one at a time in serial order. |
| static [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#)! | `https://developer.android.com/reference/kotlin/android/os/AsyncTask#THREAD_POOL_EXECUTOR:java.util.concurrent.Executor` An `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that can be used to execute tasks in parallel. |

## Public constructors

### AsyncTask

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
AsyncTask()
```

Creates a new asynchronous task. This constructor must be invoked on the UI thread.

## Public methods

### cancel

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun cancel(mayInterruptIfRunning: Boolean): Boolean
```

**Deprecated:** *Deprecated in Java.*

Attempts to cancel execution of this task. This attempt will fail if the task has already completed, already been cancelled, or could not be cancelled for some other reason. If successful, and this task has not started when cancel is called, this task should never run. If the task has already started, then the mayInterruptIfRunning parameter determines whether the thread executing this task should be interrupted in an attempt to stop the task.

Calling this method will result in `https://developer.android.com/reference/kotlin/android/os/AsyncTask#onCancelled(android.os.AsyncTask.Result)` being invoked on the UI thread after `https://developer.android.com/reference/kotlin/android/os/AsyncTask#doInBackground(android.os.AsyncTask.Params)` returns. Calling this method guarantees that onPostExecute(Object) is never subsequently invoked, even if cancel returns false, but `https://developer.android.com/reference/kotlin/android/os/AsyncTask#onPostExecute(android.os.AsyncTask.Result)` has not yet run. To finish the task as early as possible, check `https://developer.android.com/reference/kotlin/android/os/AsyncTask#isCancelled()` periodically from `https://developer.android.com/reference/kotlin/android/os/AsyncTask#doInBackground(android.os.AsyncTask.Params)`.

This only requests cancellation. It never waits for a running background task to terminate, even if mayInterruptIfRunning is true.

| Parameters ||
|---|---|
| `mayInterruptIfRunning` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): true if the thread executing this task should be interrupted; otherwise, in-progress tasks are allowed to complete. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | false if the task could not be cancelled, typically because it has already completed normally; true otherwise |

**See Also**

- `https://developer.android.com/reference/kotlin/android/os/AsyncTask#isCancelled()`
- `https://developer.android.com/reference/kotlin/android/os/AsyncTask#onCancelled(android.os.AsyncTask.Result)`

### execute

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun execute(vararg params: Params): AsyncTask<Params, Progress, Result>!
```

**Deprecated:** *Deprecated in Java.*

Executes the task with the specified parameters. The task returns itself (this) so that the caller can keep a reference to it.

Note: this function schedules the task on a queue for a single background thread or pool of threads depending on the platform version. When first introduced, AsyncTasks were executed serially on a single background thread. Starting with `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES#DONUT:kotlin.Int`, this was changed to a pool of threads allowing multiple tasks to operate in parallel. Starting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES#HONEYCOMB:kotlin.Int`, tasks are back to being executed on a single thread to avoid common application errors caused by parallel execution. If you truly want parallel execution, you can use the `https://developer.android.com/reference/kotlin/android/os/AsyncTask#executeOnExecutor(java.util.concurrent.Executor,%20android.os.AsyncTask.Params)` version of this method with `https://developer.android.com/reference/kotlin/android/os/AsyncTask#THREAD_POOL_EXECUTOR:java.util.concurrent.Executor`; however, see commentary there for warnings on its use.

This method must be invoked on the UI thread. 
This method must be called from the main thread of your app.

| Parameters ||
|---|---|
| `params` | Params: The parameters of the task. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/os/AsyncTask#<Params, Progress, Result>!` | This instance of AsyncTask. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | If `https://developer.android.com/reference/kotlin/android/os/AsyncTask#getStatus()` returns either `https://developer.android.com/reference/kotlin/android/os/AsyncTask.Status` or `https://developer.android.com/reference/kotlin/android/os/AsyncTask.Status`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/os/AsyncTask#executeOnExecutor(java.util.concurrent.Executor,%20android.os.AsyncTask.Params)`
- `https://developer.android.com/reference/kotlin/android/os/AsyncTask#execute(java.lang.Runnable)`

### execute

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun execute(runnable: Runnable!): Unit
```

**Deprecated:** *Deprecated in Java.*

Convenience version of `https://developer.android.com/reference/kotlin/android/os/AsyncTask#execute(android.os.AsyncTask.Params)` for use with a simple Runnable object. See `https://developer.android.com/reference/kotlin/android/os/AsyncTask#execute(android.os.AsyncTask.Params)` for more information on the order of execution. 
This method must be called from the main thread of your app.
**See Also**

- `https://developer.android.com/reference/kotlin/android/os/AsyncTask#execute(android.os.AsyncTask.Params)`
- `https://developer.android.com/reference/kotlin/android/os/AsyncTask#executeOnExecutor(java.util.concurrent.Executor,%20android.os.AsyncTask.Params)`

### executeOnExecutor

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun executeOnExecutor(
    exec: Executor!, 
    vararg params: Params
): AsyncTask<Params, Progress, Result>!
```

**Deprecated:** *Deprecated in Java.*

Executes the task with the specified parameters. The task returns itself (this) so that the caller can keep a reference to it.

This method is typically used with `https://developer.android.com/reference/kotlin/android/os/AsyncTask#THREAD_POOL_EXECUTOR:java.util.concurrent.Executor` to allow multiple tasks to run in parallel on a pool of threads managed by AsyncTask, however you can also use your own `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` for custom behavior.

*Warning:* Allowing multiple tasks to run in parallel from a thread pool is generally *not* what one wants, because the order of their operation is not defined. For example, if these tasks are used to modify any state in common (such as writing a file due to a button click), there are no guarantees on the order of the modifications. Without careful work it is possible in rare cases for the newer version of the data to be over-written by an older one, leading to obscure data loss and stability issues. Such changes are best executed in serial; to guarantee such work is serialized regardless of platform version you can use this function with `https://developer.android.com/reference/kotlin/android/os/AsyncTask#SERIAL_EXECUTOR:java.util.concurrent.Executor`.

This method must be invoked on the UI thread. 
This method must be called from the main thread of your app.

| Parameters ||
|---|---|
| `exec` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#)!: The executor to use. `https://developer.android.com/reference/kotlin/android/os/AsyncTask#THREAD_POOL_EXECUTOR:java.util.concurrent.Executor` is available as a convenient process-wide thread pool for tasks that are loosely coupled. |
| `params` | Params: The parameters of the task. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/os/AsyncTask#<Params, Progress, Result>!` | This instance of AsyncTask. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | If `https://developer.android.com/reference/kotlin/android/os/AsyncTask#getStatus()` returns either `https://developer.android.com/reference/kotlin/android/os/AsyncTask.Status` or `https://developer.android.com/reference/kotlin/android/os/AsyncTask.Status`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/os/AsyncTask#execute(android.os.AsyncTask.Params)`

### get

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun get(): Result
```

**Deprecated:** *Deprecated in Java.*

Waits if necessary for the computation to complete, and then retrieves its result.

| Return ||
|---|---|
| `Result` | The computed result. |

| Exceptions ||
|---|---|
| `java.lang.InterruptedException` | If the current thread was interrupted while waiting. |
| `java.util.concurrent.CancellationException` | If the computation was cancelled. |
| `java.util.concurrent.ExecutionException` | If the computation threw an exception. |

### get

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun get(
    timeout: Long, 
    unit: TimeUnit!
): Result
```

**Deprecated:** *Deprecated in Java.*

Waits if necessary for at most the given time for the computation to complete, and then retrieves its result.

| Parameters ||
|---|---|
| `timeout` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): Time to wait before cancelling the operation. |
| `unit` | [TimeUnit](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit.html#)!: The time unit for the timeout. |

| Return ||
|---|---|
| `Result` | The computed result. |

| Exceptions ||
|---|---|
| `java.lang.InterruptedException` | If the current thread was interrupted while waiting. |
| `java.util.concurrent.CancellationException` | If the computation was cancelled. |
| `java.util.concurrent.ExecutionException` | If the computation threw an exception. |
| `java.util.concurrent.TimeoutException` | If the wait timed out. |

### getStatus

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getStatus(): AsyncTask.Status!
```

**Deprecated:** *Deprecated in Java.*

Returns the current status of this task.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/os/AsyncTask.Status!` | The current status. |

### isCancelled

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isCancelled(): Boolean
```

**Deprecated:** *Deprecated in Java.*

Returns true if this task was cancelled before it completed normally. If you are calling `https://developer.android.com/reference/kotlin/android/os/AsyncTask#cancel(kotlin.Boolean)` on the task, the value returned by this method should be checked periodically from `https://developer.android.com/reference/kotlin/android/os/AsyncTask#doInBackground(android.os.AsyncTask.Params)` to end the task as soon as possible.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if task was cancelled before it completed |

**See Also**

- `https://developer.android.com/reference/kotlin/android/os/AsyncTask#cancel(kotlin.Boolean)`

## Protected methods

### doInBackground

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected abstract fun doInBackground(vararg params: Params): Result
```

**Deprecated:** *Deprecated in Java.*

Override this method to perform a computation on a background thread. The specified parameters are the parameters passed to #execute by the caller of this task. This will normally run on a background thread. But to better support testing frameworks, it is recommended that this also tolerates direct execution on the foreground thread, as part of the #execute call. This method can call `https://developer.android.com/reference/kotlin/android/os/AsyncTask#publishProgress(android.os.AsyncTask.Progress)` to publish updates on the UI thread. 
This method may take several seconds to complete, so it should only be called from a worker thread.

| Parameters ||
|---|---|
| `params` | Params: The parameters of the task. |

| Return ||
|---|---|
| `Result` | A result, defined by the subclass of this task. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/os/AsyncTask#onPreExecute()`
- `https://developer.android.com/reference/kotlin/android/os/AsyncTask#onPostExecute(android.os.AsyncTask.Result)`
- `https://developer.android.com/reference/kotlin/android/os/AsyncTask#publishProgress(android.os.AsyncTask.Progress)`

### onCancelled

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun onCancelled(): Unit
```

**Deprecated:** *Deprecated in Java.*

Applications should preferably override `https://developer.android.com/reference/kotlin/android/os/AsyncTask#onCancelled(android.os.AsyncTask.Result)`. This method is invoked by the default implementation of `https://developer.android.com/reference/kotlin/android/os/AsyncTask#onCancelled(android.os.AsyncTask.Result)`. The default version does nothing.

Runs on the UI thread after `https://developer.android.com/reference/kotlin/android/os/AsyncTask#cancel(kotlin.Boolean)` is invoked and `https://developer.android.com/reference/kotlin/android/os/AsyncTask#doInBackground(android.os.AsyncTask.Params)` has finished.
. 
This method must be called from the main thread of your app. **See Also**

- `https://developer.android.com/reference/kotlin/android/os/AsyncTask#onCancelled(android.os.AsyncTask.Result)`
- `https://developer.android.com/reference/kotlin/android/os/AsyncTask#cancel(kotlin.Boolean)`
- `https://developer.android.com/reference/kotlin/android/os/AsyncTask#isCancelled()`

### onCancelled

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun onCancelled(result: Result): Unit
```

**Deprecated:** *Deprecated in Java.*

Runs on the UI thread after `https://developer.android.com/reference/kotlin/android/os/AsyncTask#cancel(kotlin.Boolean)` is invoked and `https://developer.android.com/reference/kotlin/android/os/AsyncTask#doInBackground(android.os.AsyncTask.Params)` has finished.

The default implementation simply invokes `https://developer.android.com/reference/kotlin/android/os/AsyncTask#onCancelled()` and ignores the result. If you write your own implementation, do not call `super.onCancelled(result)`.
. 
This method must be called from the main thread of your app.

| Parameters ||
|---|---|
| `result` | Result: The result, if any, computed in `https://developer.android.com/reference/kotlin/android/os/AsyncTask#doInBackground(android.os.AsyncTask.Params)`, can be null |

**See Also**

- `https://developer.android.com/reference/kotlin/android/os/AsyncTask#cancel(kotlin.Boolean)`
- `https://developer.android.com/reference/kotlin/android/os/AsyncTask#isCancelled()`

### onPostExecute

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun onPostExecute(result: Result): Unit
```

**Deprecated:** *Deprecated in Java.*

Runs on the UI thread after `https://developer.android.com/reference/kotlin/android/os/AsyncTask#doInBackground(android.os.AsyncTask.Params)`. The specified result is the value returned by `https://developer.android.com/reference/kotlin/android/os/AsyncTask#doInBackground(android.os.AsyncTask.Params)`. To better support testing frameworks, it is recommended that this be written to tolerate direct execution as part of the execute() call. The default version does nothing.

This method won't be invoked if the task was cancelled.
. 
This method must be called from the main thread of your app.

| Parameters ||
|---|---|
| `result` | Result: The result of the operation computed by `https://developer.android.com/reference/kotlin/android/os/AsyncTask#doInBackground(android.os.AsyncTask.Params)`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/os/AsyncTask#onPreExecute()`
- `https://developer.android.com/reference/kotlin/android/os/AsyncTask#doInBackground(android.os.AsyncTask.Params)`
- `https://developer.android.com/reference/kotlin/android/os/AsyncTask#onCancelled(android.os.AsyncTask.Result)`

### onPreExecute

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun onPreExecute(): Unit
```

**Deprecated:** *Deprecated in Java.*

Runs on the UI thread before `https://developer.android.com/reference/kotlin/android/os/AsyncTask#doInBackground(android.os.AsyncTask.Params)`. Invoked directly by #execute or `https://developer.android.com/reference/kotlin/android/os/AsyncTask#executeOnExecutor(java.util.concurrent.Executor,%20android.os.AsyncTask.Params)`. The default version does nothing. 
This method must be called from the main thread of your app.
**See Also**

- `https://developer.android.com/reference/kotlin/android/os/AsyncTask#onPostExecute(android.os.AsyncTask.Result)`
- `https://developer.android.com/reference/kotlin/android/os/AsyncTask#doInBackground(android.os.AsyncTask.Params)`

### onProgressUpdate

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun onProgressUpdate(vararg values: Progress): Unit
```

**Deprecated:** *Deprecated in Java.*

Runs on the UI thread after `https://developer.android.com/reference/kotlin/android/os/AsyncTask#publishProgress(android.os.AsyncTask.Progress)` is invoked. The specified values are the values passed to `https://developer.android.com/reference/kotlin/android/os/AsyncTask#publishProgress(android.os.AsyncTask.Progress)`. The default version does nothing. 
This method must be called from the main thread of your app.

| Parameters ||
|---|---|
| `values` | Progress: The values indicating progress. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/os/AsyncTask#publishProgress(android.os.AsyncTask.Progress)`
- `https://developer.android.com/reference/kotlin/android/os/AsyncTask#doInBackground(android.os.AsyncTask.Params)`

### publishProgress

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected fun publishProgress(vararg values: Progress): Unit
```

**Deprecated:** *Deprecated in Java.*

This method can be invoked from `https://developer.android.com/reference/kotlin/android/os/AsyncTask#doInBackground(android.os.AsyncTask.Params)` to publish updates on the UI thread while the background computation is still running. Each call to this method will trigger the execution of `https://developer.android.com/reference/kotlin/android/os/AsyncTask#onProgressUpdate(android.os.AsyncTask.Progress)` on the UI thread. `https://developer.android.com/reference/kotlin/android/os/AsyncTask#onProgressUpdate(android.os.AsyncTask.Progress)` will not be called if the task has been canceled. 
This method may take several seconds to complete, so it should only be called from a worker thread.

| Parameters ||
|---|---|
| `values` | Progress: The progress values to update the UI with. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/os/AsyncTask#onProgressUpdate(android.os.AsyncTask.Progress)`
- `https://developer.android.com/reference/kotlin/android/os/AsyncTask#doInBackground(android.os.AsyncTask.Params)`

## Properties

### SERIAL_EXECUTOR

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SERIAL_EXECUTOR: Executor!
```

**Deprecated:** *Globally serializing tasks results in excessive queuing for unrelated operations.*

An `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that executes tasks one at a time in serial order. This serialization is global to a particular process.

### THREAD_POOL_EXECUTOR

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val THREAD_POOL_EXECUTOR: Executor!
```

**Deprecated:** *Using a single thread pool for a general purpose results in suboptimal behavior for different tasks. Small, CPU-bound tasks benefit from a bounded pool and queueing, and long-running blocking tasks, such as network operations, benefit from many threads. Use or create an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` configured for your use case.*

An `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that can be used to execute tasks in parallel.
