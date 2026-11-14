# Loader

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Loader

Kotlin| [Java](https://developer.android.com/reference/android/content/Loader "View this page in Java") 
| --- | --- |

```
open class Loader<D : Any!>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.content.Loader](https://developer.android.com/reference/kotlin/android/content/Loader#) |

| Known Direct Subclasses [AsyncTaskLoader](https://developer.android.com/reference/kotlin/android/content/AsyncTaskLoader) |---------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------| | [AsyncTaskLoader](https://developer.android.com/reference/kotlin/android/content/AsyncTaskLoader) | Abstract Loader that provides an [AsyncTask](https://developer.android.com/reference/kotlin/android/os/AsyncTask.html#) to do the work. | |
| --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [CursorLoader](https://developer.android.com/reference/kotlin/android/content/CursorLoader) |---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [CursorLoader](https://developer.android.com/reference/kotlin/android/content/CursorLoader) | A loader that queries the [ContentResolver](https://developer.android.com/reference/kotlin/android/content/ContentResolver) and returns a [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#). | |
| --- | --- | --- | --- | --- | --- | --- |

| **This class was deprecated in API level 28.**
|
| Use the [Support Library](https://developer.android.com/tools/extras/support-library.html) androidx.loader.content.Loader

A class that performs asynchronous loading of data. While Loaders are active they should monitor the source of their data and deliver new results when the contents change. See [android.app.LoaderManager](https://developer.android.com/reference/kotlin/android/app/LoaderManager.html#) for more detail.

**Note on threading:** Clients of loaders should as a rule perform any calls on to a Loader from the main thread of their process (that is, the thread the Activity callbacks and other things occur on). Subclasses of Loader (such as [AsyncTaskLoader](https://developer.android.com/reference/kotlin/android/content/AsyncTaskLoader)) will often perform their work in a separate thread, but when delivering their results this too should be done on the main thread.

Subclasses generally must implement at least [onStartLoading()](https://developer.android.com/reference/kotlin/android/content/Loader#onStartLoading()), [onStopLoading()](https://developer.android.com/reference/kotlin/android/content/Loader#onStopLoading()), [onForceLoad()](https://developer.android.com/reference/kotlin/android/content/Loader#onForceLoad()), and [onReset()](https://developer.android.com/reference/kotlin/android/content/Loader#onReset()).

Most implementations should not derive directly from this class, but instead inherit from [AsyncTaskLoader](https://developer.android.com/reference/kotlin/android/content/AsyncTaskLoader).
|
| ### Developer Guides
|
| For more information about using loaders, read the [Loaders](https://developer.android.com/guide/components/loaders.html) developer guide.

## Summary

| Nested classes ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [ForceLoadContentObserver](https://developer.android.com/reference/kotlin/android/content/Loader.ForceLoadContentObserver) An implementation of a ContentObserver that takes care of connecting it to the Loader to have the loader re-load its data when the observer is told it has changed. |
| abstract | [OnLoadCanceledListener](https://developer.android.com/reference/kotlin/android/content/Loader.OnLoadCanceledListener) Interface that is implemented to discover when a Loader has been canceled before it finished loading its data. |
| abstract | [OnLoadCompleteListener](https://developer.android.com/reference/kotlin/android/content/Loader.OnLoadCompleteListener) Interface that is implemented to discover when a Loader has finished loading its data. |
| --- | --- |

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [Loader](https://developer.android.com/reference/kotlin/android/content/Loader#Loader(android.content.Context))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context)!`)` Stores away the application context associated with context. |

| Public methods ||
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [abandon](https://developer.android.com/reference/kotlin/android/content/Loader#abandon())`()` This function will normally be called for you automatically by [android.app.LoaderManager](https://developer.android.com/reference/kotlin/android/app/LoaderManager.html#) when restarting a Loader. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [cancelLoad](https://developer.android.com/reference/kotlin/android/content/Loader#cancelLoad())`()` Attempt to cancel the current load task. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [commitContentChanged](https://developer.android.com/reference/kotlin/android/content/Loader#commitContentChanged())`()` Commit that you have actually fully processed a content change that was returned by [takeContentChanged](https://developer.android.com/reference/kotlin/android/content/Loader#takeContentChanged()). |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [dataToString](https://developer.android.com/reference/kotlin/android/content/Loader#dataToString(android.content.Loader.ForceLoadContentObserver.D))`(`data:` `D`)` For debugging, converts an instance of the Loader's data class to a string that can be printed. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [deliverCancellation](https://developer.android.com/reference/kotlin/android/content/Loader#deliverCancellation())`()` Informs the registered [OnLoadCanceledListener](https://developer.android.com/reference/kotlin/android/content/Loader.OnLoadCanceledListener) that the load has been canceled. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [deliverResult](https://developer.android.com/reference/kotlin/android/content/Loader#deliverResult(android.content.Loader.ForceLoadContentObserver.D))`(`data:` `D`)` Sends the result of the load to the registered listener. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [dump](https://developer.android.com/reference/kotlin/android/content/Loader#dump(kotlin.String,%20java.io.FileDescriptor,%20java.io.PrintWriter,%20kotlin.Array))`(`prefix:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `fd:` ` [FileDescriptor](https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#)!`, `writer:` ` [PrintWriter](https://developer.android.com/reference/kotlin/java/io/PrintWriter.html#)!`, `args:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`)` Print the Loader's state into the given stream. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [forceLoad](https://developer.android.com/reference/kotlin/android/content/Loader#forceLoad())`()` Force an asynchronous load. |
| open [Context](https://developer.android.com/reference/kotlin/android/content/Context)! | [getContext](https://developer.android.com/reference/kotlin/android/content/Loader#getContext())`()` <br /> |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getId](https://developer.android.com/reference/kotlin/android/content/Loader#getId())`()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isAbandoned](https://developer.android.com/reference/kotlin/android/content/Loader#isAbandoned())`()` Return whether this loader has been abandoned. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isReset](https://developer.android.com/reference/kotlin/android/content/Loader#isReset())`()` Return whether this load has been reset. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isStarted](https://developer.android.com/reference/kotlin/android/content/Loader#isStarted())`()` Return whether this load has been started. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onContentChanged](https://developer.android.com/reference/kotlin/android/content/Loader#onContentChanged())`()` Called when [ForceLoadContentObserver](https://developer.android.com/reference/kotlin/android/content/Loader.ForceLoadContentObserver) detects a change. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerListener](https://developer.android.com/reference/kotlin/android/content/Loader#registerListener(kotlin.Int,%20android.content.Loader.OnLoadCompleteListener))`(`id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `listener:` ` [Loader.OnLoadCompleteListener](https://developer.android.com/reference/kotlin/android/content/Loader.OnLoadCompleteListener)<D>!`)` Registers a class that will receive callbacks when a load is complete. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerOnLoadCanceledListener](https://developer.android.com/reference/kotlin/android/content/Loader#registerOnLoadCanceledListener(android.content.Loader.OnLoadCanceledListener))`(`listener:` ` [Loader.OnLoadCanceledListener](https://developer.android.com/reference/kotlin/android/content/Loader.OnLoadCanceledListener)<D>!`)` Registers a listener that will receive callbacks when a load is canceled. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [reset](https://developer.android.com/reference/kotlin/android/content/Loader#reset())`()` This function will normally be called for you automatically by [android.app.LoaderManager](https://developer.android.com/reference/kotlin/android/app/LoaderManager.html#) when destroying a Loader. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [rollbackContentChanged](https://developer.android.com/reference/kotlin/android/content/Loader#rollbackContentChanged())`()` Report that you have abandoned the processing of a content change that was returned by [takeContentChanged()](https://developer.android.com/reference/kotlin/android/content/Loader#takeContentChanged())and would like to rollback to the state where there is again a pending content change. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [startLoading](https://developer.android.com/reference/kotlin/android/content/Loader#startLoading())`()` This function will normally be called for you automatically by [android.app.LoaderManager](https://developer.android.com/reference/kotlin/android/app/LoaderManager.html#) when the associated fragment/activity is being started. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [stopLoading](https://developer.android.com/reference/kotlin/android/content/Loader#stopLoading())`()` This function will normally be called for you automatically by [android.app.LoaderManager](https://developer.android.com/reference/kotlin/android/app/LoaderManager.html#) when the associated fragment/activity is being stopped. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [takeContentChanged](https://developer.android.com/reference/kotlin/android/content/Loader#takeContentChanged())`()` Take the current flag indicating whether the loader's content had changed while it was stopped. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/content/Loader#toString())`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unregisterListener](https://developer.android.com/reference/kotlin/android/content/Loader#unregisterListener(android.content.Loader.OnLoadCompleteListener))`(`listener:` ` [Loader.OnLoadCompleteListener](https://developer.android.com/reference/kotlin/android/content/Loader.OnLoadCompleteListener)<D>!`)` Remove a listener that was previously added with [registerListener](https://developer.android.com/reference/kotlin/android/content/Loader#registerListener(kotlin.Int,%20android.content.Loader.OnLoadCompleteListener)). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unregisterOnLoadCanceledListener](https://developer.android.com/reference/kotlin/android/content/Loader#unregisterOnLoadCanceledListener(android.content.Loader.OnLoadCanceledListener))`(`listener:` ` [Loader.OnLoadCanceledListener](https://developer.android.com/reference/kotlin/android/content/Loader.OnLoadCanceledListener)<D>!`)` Unregisters a listener that was previously added with [registerOnLoadCanceledListener](https://developer.android.com/reference/kotlin/android/content/Loader#registerOnLoadCanceledListener(android.content.Loader.OnLoadCanceledListener)). |
| --- | --- |

| Protected methods ||
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onAbandon](https://developer.android.com/reference/kotlin/android/content/Loader#onAbandon())`()` Subclasses implement this to take care of being abandoned. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onCancelLoad](https://developer.android.com/reference/kotlin/android/content/Loader#onCancelLoad())`()` Subclasses must implement this to take care of requests to [cancelLoad()](https://developer.android.com/reference/kotlin/android/content/Loader#cancelLoad()). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onForceLoad](https://developer.android.com/reference/kotlin/android/content/Loader#onForceLoad())`()` Subclasses must implement this to take care of requests to [forceLoad()](https://developer.android.com/reference/kotlin/android/content/Loader#forceLoad()). |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onReset](https://developer.android.com/reference/kotlin/android/content/Loader#onReset())`()` Subclasses must implement this to take care of resetting their loader, as per [reset()](https://developer.android.com/reference/kotlin/android/content/Loader#reset()). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onStartLoading](https://developer.android.com/reference/kotlin/android/content/Loader#onStartLoading())`()` Subclasses must implement this to take care of loading their data, as per [startLoading()](https://developer.android.com/reference/kotlin/android/content/Loader#startLoading()). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onStopLoading](https://developer.android.com/reference/kotlin/android/content/Loader#onStopLoading())`()` Subclasses must implement this to take care of stopping their loader, as per [stopLoading()](https://developer.android.com/reference/kotlin/android/content/Loader#stopLoading()). |
| --- | --- |

## Public constructors

### Loader

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Loader(context: Context!)
```

Stores away the application context associated with context. Since Loaders can be used across multiple activities it's dangerous to store the context directly; always use [getContext()](https://developer.android.com/reference/kotlin/android/content/Loader#getContext())to retrieve the Loader's Context, don't use the constructor argument directly. The Context returned by [getContext](https://developer.android.com/reference/kotlin/android/content/Loader#getContext())is safe to use across Activity instances.

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context)!:used to retrieve the application context. |

## Public methods

### abandon

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun abandon(): Unit
```

**Deprecated:** *Deprecated in Java.*

This function will normally be called for you automatically by [android.app.LoaderManager](https://developer.android.com/reference/kotlin/android/app/LoaderManager.html#) when restarting a Loader. When using a Loader with [android.app.LoaderManager](https://developer.android.com/reference/kotlin/android/app/LoaderManager.html#), you*must not* call this method yourself, or you will conflict with its management of the Loader. Tell the Loader that it is being abandoned. This is called prior to [reset](https://developer.android.com/reference/kotlin/android/content/Loader#reset())to have it retain its current data but not report any new data. 

### cancelLoad

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun cancelLoad(): Boolean
```

**Deprecated:** *Deprecated in Java.*

Attempt to cancel the current load task. Must be called on the main thread of the process.

Cancellation is not an immediate operation, since the load is performed in a background thread. If there is currently a load in progress, this method requests that the load be canceled, and notes this is the case; once the background thread has completed its work its remaining state will be cleared. If another load request comes in during this time, it will be held until the canceled load is complete.

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | Returns false if the task could not be canceled, typically because it has already completed normally, or because [startLoading()](https://developer.android.com/reference/kotlin/android/content/Loader#startLoading())hasn't been called; returns true otherwise. When true is returned, the task is still running and the [OnLoadCanceledListener](https://developer.android.com/reference/kotlin/android/content/Loader.OnLoadCanceledListener) will be called when the task completes. |

### commitContentChanged

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun commitContentChanged(): Unit
```

**Deprecated:** *Deprecated in Java.*

Commit that you have actually fully processed a content change that was returned by [takeContentChanged](https://developer.android.com/reference/kotlin/android/content/Loader#takeContentChanged()). This is for use with [rollbackContentChanged()](https://developer.android.com/reference/kotlin/android/content/Loader#rollbackContentChanged())to handle situations where a load is cancelled. Call this when you have completely processed a load without it being cancelled. 

### dataToString

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun dataToString(data: D): String!
```

**Deprecated:** *Deprecated in Java.*

For debugging, converts an instance of the Loader's data class to a string that can be printed. Must handle a null data. 

### deliverCancellation

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun deliverCancellation(): Unit
```

**Deprecated:** *Deprecated in Java.*

Informs the registered [OnLoadCanceledListener](https://developer.android.com/reference/kotlin/android/content/Loader.OnLoadCanceledListener) that the load has been canceled. Should only be called by subclasses. Must be called from the process's main thread. 

### deliverResult

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun deliverResult(data: D): Unit
```

**Deprecated:** *Deprecated in Java.*

Sends the result of the load to the registered listener. Should only be called by subclasses. Must be called from the process's main thread.

| Parameters ||
|--------|--------------------------|
| `data` | D:the result of the load |

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
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `prefix` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:Text to print at the front of each line. |
| `fd` | [FileDescriptor](https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#)!:The raw file descriptor that the dump is being sent to. |
| `writer` | [PrintWriter](https://developer.android.com/reference/kotlin/java/io/PrintWriter.html#)!:A PrintWriter to which the dump is to be set. |
| --- | --- |
| `args` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!:Additional arguments to the dump request. |

### forceLoad

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun forceLoad(): Unit
```

**Deprecated:** *Deprecated in Java.*

Force an asynchronous load. Unlike [startLoading()](https://developer.android.com/reference/kotlin/android/content/Loader#startLoading())this will ignore a previously loaded data set and load a new one. This simply calls through to the implementation's [onForceLoad()](https://developer.android.com/reference/kotlin/android/content/Loader#onForceLoad()). You generally should only call this when the loader is started -- that is, [isStarted()](https://developer.android.com/reference/kotlin/android/content/Loader#isStarted())returns true.

Must be called from the process's main thread. 

### getContext

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getContext(): Context!
```

**Deprecated:** *Deprecated in Java.*

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| [Context](https://developer.android.com/reference/kotlin/android/content/Context)! | an application context retrieved from the Context passed to the constructor. |

### getId

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getId(): Int
```

**Deprecated:** *Deprecated in Java.*

| Return ||
|----------------------------------------------------------------------------|-----------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the ID of this loader |

### isAbandoned

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isAbandoned(): Boolean
```

**Deprecated:** *Deprecated in Java.*

Return whether this loader has been abandoned. In this state, the loader*must not* report any new data, and*must*keep its last reported data valid until it is finally reset. 

### isReset

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isReset(): Boolean
```

**Deprecated:** *Deprecated in Java.*

Return whether this load has been reset. That is, either the loader has not yet been started for the first time, or its [reset()](https://developer.android.com/reference/kotlin/android/content/Loader#reset())has been called. 

### isStarted

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isStarted(): Boolean
```

**Deprecated:** *Deprecated in Java.*

Return whether this load has been started. That is, its [startLoading()](https://developer.android.com/reference/kotlin/android/content/Loader#startLoading())has been called and no calls to [stopLoading()](https://developer.android.com/reference/kotlin/android/content/Loader#stopLoading())or [reset()](https://developer.android.com/reference/kotlin/android/content/Loader#reset())have yet been made. 

### onContentChanged

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onContentChanged(): Unit
```

**Deprecated:** *Deprecated in Java.*

Called when [ForceLoadContentObserver](https://developer.android.com/reference/kotlin/android/content/Loader.ForceLoadContentObserver) detects a change. The default implementation checks to see if the loader is currently started; if so, it simply calls [forceLoad()](https://developer.android.com/reference/kotlin/android/content/Loader#forceLoad()); otherwise, it sets a flag so that [takeContentChanged()](https://developer.android.com/reference/kotlin/android/content/Loader#takeContentChanged())returns true.

Must be called from the process's main thread. 

### registerListener

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun registerListener(
    id: Int, 
    listener: Loader.OnLoadCompleteListener<D>!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Registers a class that will receive callbacks when a load is complete. The callback will be called on the process's main thread so it's safe to pass the results to widgets.

Must be called from the process's main thread. 

### registerOnLoadCanceledListener

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun registerOnLoadCanceledListener(listener: Loader.OnLoadCanceledListener<D>!): Unit
```

**Deprecated:** *Deprecated in Java.*

Registers a listener that will receive callbacks when a load is canceled. The callback will be called on the process's main thread so it's safe to pass the results to widgets. Must be called from the process's main thread.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [Loader.OnLoadCanceledListener](https://developer.android.com/reference/kotlin/android/content/Loader.OnLoadCanceledListener)\<D\>!:The listener to register. |

### reset

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun reset(): Unit
```

**Deprecated:** *Deprecated in Java.*

This function will normally be called for you automatically by [android.app.LoaderManager](https://developer.android.com/reference/kotlin/android/app/LoaderManager.html#) when destroying a Loader. When using a Loader with [android.app.LoaderManager](https://developer.android.com/reference/kotlin/android/app/LoaderManager.html#), you*must not* call this method yourself, or you will conflict with its management of the Loader. Resets the state of the Loader. The Loader should at this point free all of its resources, since it may never be called again; however, its [startLoading()](https://developer.android.com/reference/kotlin/android/content/Loader#startLoading())may later be called at which point it must be able to start running again.

This updates the Loader's internal state so that [isStarted()](https://developer.android.com/reference/kotlin/android/content/Loader#isStarted())and [isReset()](https://developer.android.com/reference/kotlin/android/content/Loader#isReset())will return the correct values, and then calls the implementation's [onReset()](https://developer.android.com/reference/kotlin/android/content/Loader#onReset()).

Must be called from the process's main thread. 

### rollbackContentChanged

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun rollbackContentChanged(): Unit
```

**Deprecated:** *Deprecated in Java.*

Report that you have abandoned the processing of a content change that was returned by [takeContentChanged()](https://developer.android.com/reference/kotlin/android/content/Loader#takeContentChanged())and would like to rollback to the state where there is again a pending content change. This is to handle the case where a data load due to a content change has been canceled before its data was delivered back to the loader. 

### startLoading

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun startLoading(): Unit
```

**Deprecated:** *Deprecated in Java.*

This function will normally be called for you automatically by [android.app.LoaderManager](https://developer.android.com/reference/kotlin/android/app/LoaderManager.html#) when the associated fragment/activity is being started. When using a Loader with [android.app.LoaderManager](https://developer.android.com/reference/kotlin/android/app/LoaderManager.html#), you*must not* call this method yourself, or you will conflict with its management of the Loader. Starts an asynchronous load of the Loader's data. When the result is ready the callbacks will be called on the process's main thread. If a previous load has been completed and is still valid the result may be passed to the callbacks immediately. The loader will monitor the source of the data set and may deliver future callbacks if the source changes. Calling [stopLoading](https://developer.android.com/reference/kotlin/android/content/Loader#stopLoading())will stop the delivery of callbacks.

This updates the Loader's internal state so that [isStarted()](https://developer.android.com/reference/kotlin/android/content/Loader#isStarted())and [isReset()](https://developer.android.com/reference/kotlin/android/content/Loader#isReset())will return the correct values, and then calls the implementation's [onStartLoading()](https://developer.android.com/reference/kotlin/android/content/Loader#onStartLoading()).

Must be called from the process's main thread. 

### stopLoading

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun stopLoading(): Unit
```

**Deprecated:** *Deprecated in Java.*

This function will normally be called for you automatically by [android.app.LoaderManager](https://developer.android.com/reference/kotlin/android/app/LoaderManager.html#) when the associated fragment/activity is being stopped. When using a Loader with [android.app.LoaderManager](https://developer.android.com/reference/kotlin/android/app/LoaderManager.html#), you*must not*call this method yourself, or you will conflict with its management of the Loader.

Stops delivery of updates until the next time [startLoading()](https://developer.android.com/reference/kotlin/android/content/Loader#startLoading())is called. Implementations should*not* invalidate their data at this point -- clients are still free to use the last data the loader reported. They will, however, typically stop reporting new data if the data changes; they can still monitor for changes, but must not report them to the client until and if [startLoading()](https://developer.android.com/reference/kotlin/android/content/Loader#startLoading())is later called.

This updates the Loader's internal state so that [isStarted()](https://developer.android.com/reference/kotlin/android/content/Loader#isStarted())will return the correct value, and then calls the implementation's [onStopLoading()](https://developer.android.com/reference/kotlin/android/content/Loader#onStopLoading()).

Must be called from the process's main thread. 

### takeContentChanged

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun takeContentChanged(): Boolean
```

**Deprecated:** *Deprecated in Java.*

Take the current flag indicating whether the loader's content had changed while it was stopped. If it had, true is returned and the flag is cleared. 

### toString

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

**Deprecated:** *Deprecated in Java.*

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

### unregisterListener

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun unregisterListener(listener: Loader.OnLoadCompleteListener<D>!): Unit
```

**Deprecated:** *Deprecated in Java.*

Remove a listener that was previously added with [registerListener](https://developer.android.com/reference/kotlin/android/content/Loader#registerListener(kotlin.Int,%20android.content.Loader.OnLoadCompleteListener)). Must be called from the process's main thread. 

### unregisterOnLoadCanceledListener

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun unregisterOnLoadCanceledListener(listener: Loader.OnLoadCanceledListener<D>!): Unit
```

**Deprecated:** *Deprecated in Java.*

Unregisters a listener that was previously added with [registerOnLoadCanceledListener](https://developer.android.com/reference/kotlin/android/content/Loader#registerOnLoadCanceledListener(android.content.Loader.OnLoadCanceledListener)). Must be called from the process's main thread.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [Loader.OnLoadCanceledListener](https://developer.android.com/reference/kotlin/android/content/Loader.OnLoadCanceledListener)\<D\>!:The listener to unregister. |

## Protected methods

### onAbandon

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun onAbandon(): Unit
```

**Deprecated:** *Deprecated in Java.*

Subclasses implement this to take care of being abandoned. This is an optional intermediate state prior to [onReset()](https://developer.android.com/reference/kotlin/android/content/Loader#onReset())-- it means that the client is no longer interested in any new data from the loader, so the loader must not report any further updates. However, the loader*must* keep its last reported data valid until the final [onReset()](https://developer.android.com/reference/kotlin/android/content/Loader#onReset())happens. You can retrieve the current abandoned state with [isAbandoned](https://developer.android.com/reference/kotlin/android/content/Loader#isAbandoned()). 

### onCancelLoad

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun onCancelLoad(): Boolean
```

**Deprecated:** *Deprecated in Java.*

Subclasses must implement this to take care of requests to [cancelLoad()](https://developer.android.com/reference/kotlin/android/content/Loader#cancelLoad()). This will always be called from the process's main thread.

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | Returns false if the task could not be canceled, typically because it has already completed normally, or because [startLoading()](https://developer.android.com/reference/kotlin/android/content/Loader#startLoading())hasn't been called; returns true otherwise. When true is returned, the task is still running and the [OnLoadCanceledListener](https://developer.android.com/reference/kotlin/android/content/Loader.OnLoadCanceledListener) will be called when the task completes. |

### onForceLoad

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun onForceLoad(): Unit
```

**Deprecated:** *Deprecated in Java.*

Subclasses must implement this to take care of requests to [forceLoad()](https://developer.android.com/reference/kotlin/android/content/Loader#forceLoad()). This will always be called from the process's main thread. 

### onReset

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun onReset(): Unit
```

**Deprecated:** *Deprecated in Java.*

Subclasses must implement this to take care of resetting their loader, as per [reset()](https://developer.android.com/reference/kotlin/android/content/Loader#reset()). This is not called by clients directly, but as a result of a call to [reset()](https://developer.android.com/reference/kotlin/android/content/Loader#reset()). This will always be called from the process's main thread. 

### onStartLoading

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun onStartLoading(): Unit
```

**Deprecated:** *Deprecated in Java.*

Subclasses must implement this to take care of loading their data, as per [startLoading()](https://developer.android.com/reference/kotlin/android/content/Loader#startLoading()). This is not called by clients directly, but as a result of a call to [startLoading()](https://developer.android.com/reference/kotlin/android/content/Loader#startLoading()). 

### onStopLoading

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun onStopLoading(): Unit
```

**Deprecated:** *Deprecated in Java.*

Subclasses must implement this to take care of stopping their loader, as per [stopLoading()](https://developer.android.com/reference/kotlin/android/content/Loader#stopLoading()). This is not called by clients directly, but as a result of a call to [stopLoading()](https://developer.android.com/reference/kotlin/android/content/Loader#stopLoading()). This will always be called from the process's main thread.
