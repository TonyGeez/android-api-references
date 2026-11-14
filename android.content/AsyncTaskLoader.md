Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AsyncTaskLoader

Kotlin | [Java](AsyncTaskLoader.md)
| --- | --- |

```
abstract class AsyncTaskLoader<D : Any!> : Loader<D>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.content.Loader](Loader.md)\<D\> ||
| | ↳ | [android.content.AsyncTaskLoader](AsyncTaskLoader.md) |

| Known Direct Subclasses [CursorLoader](CursorLoader.md) |---|---| | [CursorLoader](CursorLoader.md) | A loader that queries the ContentResolver and returns a `https://developer.android.com/reference/kotlin/android/database/Cursor.html#`. | |
| --- | --- | --- | --- | --- | --- | --- |

| **This class was deprecated in API level 28.**
|
| Use the [Support Library](https://developer.android.com/tools/extras/support-library.html) androidx.loader.content.AsyncTaskLoader

Abstract Loader that provides an `https://developer.android.com/reference/kotlin/android/os/AsyncTask.html#` to do the work. See Loader and `https://developer.android.com/reference/kotlin/android/app/LoaderManager.html#` for more details.

Here is an example implementation of an AsyncTaskLoader subclass that loads the currently installed applications from the package manager. This implementation takes care of retrieving the application labels and sorting its result set from them, monitoring for changes to the installed applications, and rebuilding the list when a change in configuration requires this (such as a locale change).

An example implementation of a fragment that uses the above loader to show the currently installed applications in a list is below.

## Summary

| Public constructors ||
|---|---|
| AsyncTaskLoader <br /> |

| Public methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | cancelLoadInBackground Called on the main thread to abort a load in progress. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | dump Print the Loader's state into the given stream. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isLoadInBackgroundCanceled Returns true if the current invocation of loadInBackground is being canceled. |
| --- | --- |
| abstract D | loadInBackground Called on a worker thread to perform the actual load and to return the result of the load operation. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onCanceled Called if the task was canceled before it was completed. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setUpdateThrottle Set amount to throttle updates by. |
| --- | --- |

| Protected methods ||
|---|---|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | onCancelLoad Subclasses must implement this to take care of requests to cancelLoad. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onForceLoad Subclasses must implement this to take care of requests to forceLoad. |
| open D | onLoadInBackground Calls loadInBackground. |
| --- | --- |

| Inherited functions ||
|---|---|
| From class Loader |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | abandon This function will normally be called for you automatically by `https://developer.android.com/reference/kotlin/android/app/LoaderManager.html#` when restarting a Loader. When using a Loader with `https://developer.android.com/reference/kotlin/android/app/LoaderManager.html#`, you *must not* call this method yourself, or you will conflict with its management of the Loader. Tell the Loader that it is being abandoned. This is called prior to reset to have it retain its current data but not report any new data. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | cancelLoad Attempt to cancel the current load task. Must be called on the main thread of the process. Cancellation is not an immediate operation, since the load is performed in a background thread. If there is currently a load in progress, this method requests that the load be canceled, and notes this is the case; once the background thread has completed its work its remaining state will be cleared. If another load request comes in during this time, it will be held until the canceled load is complete. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | commitContentChanged Commit that you have actually fully processed a content change that was returned by takeContentChanged. This is for use with rollbackContentChanged to handle situations where a load is cancelled. Call this when you have completely processed a load without it being cancelled. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | dataToString For debugging, converts an instance of the Loader's data class to a string that can be printed. Must handle a null data. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | deliverCancellation Informs the registered `https://developer.android.com/reference/kotlin/android/content/Loader.OnLoadCanceledListener` that the load has been canceled. Should only be called by subclasses. Must be called from the process's main thread. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | deliverResult Sends the result of the load to the registered listener. Should only be called by subclasses. Must be called from the process's main thread. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | forceLoad Force an asynchronous load. Unlike startLoading this will ignore a previously loaded data set and load a new one. This simply calls through to the implementation's onForceLoad. You generally should only call this when the loader is started -- that is, isStarted returns true. Must be called from the process's main thread. <br /> | | `https://developer.android.com/reference/kotlin/android/content/Context!` | getContext <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | getId <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | isAbandoned Return whether this loader has been abandoned. In this state, the loader *must not* report any new data, and *must* keep its last reported data valid until it is finally reset. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | isReset Return whether this load has been reset. That is, either the loader has not yet been started for the first time, or its reset has been called. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | isStarted Return whether this load has been started. That is, its startLoading has been called and no calls to stopLoading or reset have yet been made. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | onAbandon Subclasses implement this to take care of being abandoned. This is an optional intermediate state prior to onReset -- it means that the client is no longer interested in any new data from the loader, so the loader must not report any further updates. However, the loader *must* keep its last reported data valid until the final onReset happens. You can retrieve the current abandoned state with isAbandoned. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | onContentChanged Called when `https://developer.android.com/reference/kotlin/android/content/Loader.ForceLoadContentObserver` detects a change. The default implementation checks to see if the loader is currently started; if so, it simply calls forceLoad; otherwise, it sets a flag so that takeContentChanged returns true. Must be called from the process's main thread. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | onReset Subclasses must implement this to take care of resetting their loader, as per reset. This is not called by clients directly, but as a result of a call to reset. This will always be called from the process's main thread. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | onStartLoading Subclasses must implement this to take care of loading their data, as per startLoading. This is not called by clients directly, but as a result of a call to startLoading. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | onStopLoading Subclasses must implement this to take care of stopping their loader, as per stopLoading. This is not called by clients directly, but as a result of a call to stopLoading. This will always be called from the process's main thread. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | registerListener Registers a class that will receive callbacks when a load is complete. The callback will be called on the process's main thread so it's safe to pass the results to widgets. Must be called from the process's main thread. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | registerOnLoadCanceledListener Registers a listener that will receive callbacks when a load is canceled. The callback will be called on the process's main thread so it's safe to pass the results to widgets. Must be called from the process's main thread. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | reset This function will normally be called for you automatically by `https://developer.android.com/reference/kotlin/android/app/LoaderManager.html#` when destroying a Loader. When using a Loader with `https://developer.android.com/reference/kotlin/android/app/LoaderManager.html#`, you *must not* call this method yourself, or you will conflict with its management of the Loader. Resets the state of the Loader. The Loader should at this point free all of its resources, since it may never be called again; however, its startLoading may later be called at which point it must be able to start running again. This updates the Loader's internal state so that isStarted and isReset will return the correct values, and then calls the implementation's onReset. Must be called from the process's main thread. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | rollbackContentChanged Report that you have abandoned the processing of a content change that was returned by takeContentChanged and would like to rollback to the state where there is again a pending content change. This is to handle the case where a data load due to a content change has been canceled before its data was delivered back to the loader. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | startLoading This function will normally be called for you automatically by `https://developer.android.com/reference/kotlin/android/app/LoaderManager.html#` when the associated fragment/activity is being started. When using a Loader with `https://developer.android.com/reference/kotlin/android/app/LoaderManager.html#`, you *must not* call this method yourself, or you will conflict with its management of the Loader. Starts an asynchronous load of the Loader's data. When the result is ready the callbacks will be called on the process's main thread. If a previous load has been completed and is still valid the result may be passed to the callbacks immediately. The loader will monitor the source of the data set and may deliver future callbacks if the source changes. Calling stopLoading will stop the delivery of callbacks. This updates the Loader's internal state so that isStarted and isReset will return the correct values, and then calls the implementation's onStartLoading. Must be called from the process's main thread. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | stopLoading This function will normally be called for you automatically by `https://developer.android.com/reference/kotlin/android/app/LoaderManager.html#` when the associated fragment/activity is being stopped. When using a Loader with `https://developer.android.com/reference/kotlin/android/app/LoaderManager.html#`, you *must not* call this method yourself, or you will conflict with its management of the Loader. Stops delivery of updates until the next time startLoading is called. Implementations should *not* invalidate their data at this point -- clients are still free to use the last data the loader reported. They will, however, typically stop reporting new data if the data changes; they can still monitor for changes, but must not report them to the client until and if startLoading is later called. This updates the Loader's internal state so that isStarted will return the correct value, and then calls the implementation's onStopLoading. Must be called from the process's main thread. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | takeContentChanged Take the current flag indicating whether the loader's content had changed while it was stopped. If it had, true is returned and the flag is cleared. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | toString Returns a string representation of the object. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | unregisterListener Remove a listener that was previously added with registerListener. Must be called from the process's main thread. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | unregisterOnLoadCanceledListener Unregisters a listener that was previously added with registerOnLoadCanceledListener. Must be called from the process's main thread. <br /> | ||

## Public constructors

### AsyncTaskLoader

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
AsyncTaskLoader(context: Context!)
```

## Public methods

### cancelLoadInBackground

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun cancelLoadInBackground(): Unit
```

**Deprecated:** *Deprecated in Java.*

Called on the main thread to abort a load in progress. Override this method to abort the current invocation of loadInBackground that is running in the background on a worker thread. This method should do nothing if loadInBackground has not started running or if it has already finished.
**See Also**

- loadInBackground

### dump

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun dump(
    prefix: String!, 
    fd: FileDescriptor!, 
    writer: PrintWriter!, 
    args: Array<String!>!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Print the Loader's state into the given stream.

| Parameters ||
|---|---|
| `prefix` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: Text to print at the front of each line. |
| `fd` | [FileDescriptor](../java.io/FileDescriptor.md)!: The raw file descriptor that the dump is being sent to. |
| `writer` | [PrintWriter](../java.io/PrintWriter.md)!: A PrintWriter to which the dump is to be set. |
| --- | --- |
| `args` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!: Additional arguments to the dump request. |

### isLoadInBackgroundCanceled

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isLoadInBackgroundCanceled(): Boolean
```

**Deprecated:** *Deprecated in Java.*

Returns true if the current invocation of loadInBackground is being canceled.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the current invocation of loadInBackground is being canceled. |

**See Also**

- loadInBackground

### loadInBackground

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun loadInBackground(): D
```

**Deprecated:** *Deprecated in Java.*

Called on a worker thread to perform the actual load and to return the result of the load operation. Implementations should not deliver the result directly, but should return them from this method, which will eventually end up calling deliverResult on the UI thread. If implementations need to process the results on the UI thread they may override deliverResult and do so there. To support cancellation, this method should periodically check the value of isLoadInBackgroundCanceled and terminate when it returns true. Subclasses may also override cancelLoadInBackground to interrupt the load directly instead of polling isLoadInBackgroundCanceled. When the load is canceled, this method may either return normally or throw `https://developer.android.com/reference/kotlin/android/os/OperationCanceledException.html#`. In either case, the Loader will call onCanceled to perform post-cancellation cleanup and to dispose of the result object, if any.

| Return ||
|---|---|
| `D` | The result of the load operation. |

| Exceptions ||
|---|---|
| `android.os.OperationCanceledException` | if the load is canceled during execution. |

**See Also**

- isLoadInBackgroundCanceled
- cancelLoadInBackground
- onCanceled

### onCanceled

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onCanceled(data: D): Unit
```

**Deprecated:** *Deprecated in Java.*

Called if the task was canceled before it was completed. Gives the class a chance to clean up post-cancellation and to properly dispose of the result.

| Parameters ||
|---|---|
| `data` | D: The value that was returned by loadInBackground, or null if the task threw `https://developer.android.com/reference/kotlin/android/os/OperationCanceledException.html#`. |

### setUpdateThrottle

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setUpdateThrottle(delayMS: Long): Unit
```

**Deprecated:** *Deprecated in Java.*

Set amount to throttle updates by. This is the minimum time from when the last loadInBackground call has completed until a new load is scheduled.

| Parameters ||
|---|---|
| `delayMS` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): Amount of delay, in milliseconds. |

## Protected methods

### onCancelLoad

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun onCancelLoad(): Boolean
```

**Deprecated:** *Deprecated in Java.*

Subclasses must implement this to take care of requests to cancelLoad. This will always be called from the process's main thread.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Returns false if the task could not be canceled, typically because it has already completed normally, or because startLoading hasn't been called; returns true otherwise. When true is returned, the task is still running and the `https://developer.android.com/reference/kotlin/android/content/Loader.OnLoadCanceledListener` will be called when the task completes. |

### onForceLoad

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun onForceLoad(): Unit
```

**Deprecated:** *Deprecated in Java.*

Subclasses must implement this to take care of requests to forceLoad. This will always be called from the process's main thread.

### onLoadInBackground

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun onLoadInBackground(): D
```

**Deprecated:** *Deprecated in Java.*

Calls loadInBackground. This method is reserved for use by the loader framework. Subclasses should override loadInBackground instead of this method.

| Return ||
|---|---|
| `D` | The result of the load operation. |

| Exceptions ||
|---|---|
| `android.os.OperationCanceledException` | if the load is canceled during execution. |

**See Also**

- loadInBackground
