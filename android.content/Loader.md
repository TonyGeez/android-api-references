# Loader

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Loader

Kotlin| [Java](Loader.md) 
| --- | --- |

```
open class Loader<D : Any!>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.content.Loader](Loader.md) |

| Known Direct Subclasses [AsyncTaskLoader](AsyncTaskLoader.md) |---------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------| | [AsyncTaskLoader](AsyncTaskLoader.md) | Abstract Loader that provides an [AsyncTask](../android.os/AsyncTask.md) to do the work. | |
| --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [CursorLoader](CursorLoader.md) |---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [CursorLoader](CursorLoader.md) | A loader that queries the [ContentResolver](ContentResolver.md) and returns a [Cursor](../android.database/Cursor.md). | |
| --- | --- | --- | --- | --- | --- | --- |

| **This class was deprecated in API level 28.**
|
| Use the [Support Library](https://developer.android.com/tools/extras/support-library.html) androidx.loader.content.Loader

A class that performs asynchronous loading of data. While Loaders are active they should monitor the source of their data and deliver new results when the contents change. See [android.app.LoaderManager](../android.app/LoaderManager.md) for more detail.

**Note on threading:** Clients of loaders should as a rule perform any calls on to a Loader from the main thread of their process (that is, the thread the Activity callbacks and other things occur on). Subclasses of Loader (such as [AsyncTaskLoader](AsyncTaskLoader.md)) will often perform their work in a separate thread, but when delivering their results this too should be done on the main thread.

Subclasses generally must implement at least [onStartLoading()](Loader.md)), [onStopLoading()](Loader.md)), [onForceLoad()](Loader.md)), and [onReset()](Loader.md)).

Most implementations should not derive directly from this class, but instead inherit from [AsyncTaskLoader](AsyncTaskLoader.md).
|
| ### Developer Guides
|
| For more information about using loaders, read the [Loaders](https://developer.android.com/guide/components/loaders.html) developer guide.

## Summary

| Nested classes ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [ForceLoadContentObserver](../android/content/Loader.ForceLoadContentObserver.md) An implementation of a ContentObserver that takes care of connecting it to the Loader to have the loader re-load its data when the observer is told it has changed. |
| abstract | [OnLoadCanceledListener](../android/content/Loader.OnLoadCanceledListener.md) Interface that is implemented to discover when a Loader has been canceled before it finished loading its data. |
| abstract | [OnLoadCompleteListener](../android/content/Loader.OnLoadCompleteListener.md) Interface that is implemented to discover when a Loader has finished loading its data. |
| --- | --- |

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [Loader](Loader.md))`(`context:` ` [Context](Context.md)!`)` Stores away the application context associated with context. |

| Public methods ||
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [abandon](Loader.md))`()` This function will normally be called for you automatically by [android.app.LoaderManager](../android.app/LoaderManager.md) when restarting a Loader. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [cancelLoad](Loader.md))`()` Attempt to cancel the current load task. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [commitContentChanged](Loader.md))`()` Commit that you have actually fully processed a content change that was returned by [takeContentChanged](Loader.md)). |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [dataToString](Loader.md))`(`data:` `D`)` For debugging, converts an instance of the Loader's data class to a string that can be printed. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [deliverCancellation](Loader.md))`()` Informs the registered [OnLoadCanceledListener](../android/content/Loader.OnLoadCanceledListener.md) that the load has been canceled. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [deliverResult](Loader.md))`(`data:` `D`)` Sends the result of the load to the registered listener. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [dump](Loader.md))`(`prefix:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `fd:` ` [FileDescriptor](../java.io/FileDescriptor.md)!`, `writer:` ` [PrintWriter](../java.io/PrintWriter.md)!`, `args:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`)` Print the Loader's state into the given stream. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [forceLoad](Loader.md))`()` Force an asynchronous load. |
| open [Context](Context.md)! | [getContext](Loader.md))`()` <br /> |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getId](Loader.md))`()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isAbandoned](Loader.md))`()` Return whether this loader has been abandoned. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isReset](Loader.md))`()` Return whether this load has been reset. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isStarted](Loader.md))`()` Return whether this load has been started. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onContentChanged](Loader.md))`()` Called when [ForceLoadContentObserver](../android/content/Loader.ForceLoadContentObserver.md) detects a change. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerListener](Loader.md))`(`id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `listener:` ` [Loader.OnLoadCompleteListener](../android/content/Loader.OnLoadCompleteListener.md)<D>!`)` Registers a class that will receive callbacks when a load is complete. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerOnLoadCanceledListener](Loader.md))`(`listener:` ` [Loader.OnLoadCanceledListener](../android/content/Loader.OnLoadCanceledListener.md)<D>!`)` Registers a listener that will receive callbacks when a load is canceled. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [reset](Loader.md))`()` This function will normally be called for you automatically by [android.app.LoaderManager](../android.app/LoaderManager.md) when destroying a Loader. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [rollbackContentChanged](Loader.md))`()` Report that you have abandoned the processing of a content change that was returned by [takeContentChanged()](Loader.md))and would like to rollback to the state where there is again a pending content change. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [startLoading](Loader.md))`()` This function will normally be called for you automatically by [android.app.LoaderManager](../android.app/LoaderManager.md) when the associated fragment/activity is being started. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [stopLoading](Loader.md))`()` This function will normally be called for you automatically by [android.app.LoaderManager](../android.app/LoaderManager.md) when the associated fragment/activity is being stopped. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [takeContentChanged](Loader.md))`()` Take the current flag indicating whether the loader's content had changed while it was stopped. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](Loader.md))`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unregisterListener](Loader.md))`(`listener:` ` [Loader.OnLoadCompleteListener](../android/content/Loader.OnLoadCompleteListener.md)<D>!`)` Remove a listener that was previously added with [registerListener](Loader.md)). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unregisterOnLoadCanceledListener](Loader.md))`(`listener:` ` [Loader.OnLoadCanceledListener](../android/content/Loader.OnLoadCanceledListener.md)<D>!`)` Unregisters a listener that was previously added with [registerOnLoadCanceledListener](Loader.md)). |
| --- | --- |

| Protected methods ||
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onAbandon](Loader.md))`()` Subclasses implement this to take care of being abandoned. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onCancelLoad](Loader.md))`()` Subclasses must implement this to take care of requests to [cancelLoad()](Loader.md)). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onForceLoad](Loader.md))`()` Subclasses must implement this to take care of requests to [forceLoad()](Loader.md)). |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onReset](Loader.md))`()` Subclasses must implement this to take care of resetting their loader, as per [reset()](Loader.md)). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onStartLoading](Loader.md))`()` Subclasses must implement this to take care of loading their data, as per [startLoading()](Loader.md)). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onStopLoading](Loader.md))`()` Subclasses must implement this to take care of stopping their loader, as per [stopLoading()](Loader.md)). |
| --- | --- |

## Public constructors

### Loader

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Loader(context: Context!)
```

Stores away the application context associated with context. Since Loaders can be used across multiple activities it's dangerous to store the context directly; always use [getContext()](Loader.md))to retrieve the Loader's Context, don't use the constructor argument directly. The Context returned by [getContext](Loader.md))is safe to use across Activity instances.

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](Context.md)!:used to retrieve the application context. |

## Public methods

### abandon

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun abandon(): Unit
```

**Deprecated:** *Deprecated in Java.*

This function will normally be called for you automatically by [android.app.LoaderManager](../android.app/LoaderManager.md) when restarting a Loader. When using a Loader with [android.app.LoaderManager](../android.app/LoaderManager.md), you*must not* call this method yourself, or you will conflict with its management of the Loader. Tell the Loader that it is being abandoned. This is called prior to [reset](Loader.md))to have it retain its current data but not report any new data. 

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
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | Returns false if the task could not be canceled, typically because it has already completed normally, or because [startLoading()](Loader.md))hasn't been called; returns true otherwise. When true is returned, the task is still running and the [OnLoadCanceledListener](../android/content/Loader.OnLoadCanceledListener.md) will be called when the task completes. |

### commitContentChanged

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun commitContentChanged(): Unit
```

**Deprecated:** *Deprecated in Java.*

Commit that you have actually fully processed a content change that was returned by [takeContentChanged](Loader.md)). This is for use with [rollbackContentChanged()](Loader.md))to handle situations where a load is cancelled. Call this when you have completely processed a load without it being cancelled. 

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

Informs the registered [OnLoadCanceledListener](../android/content/Loader.OnLoadCanceledListener.md) that the load has been canceled. Should only be called by subclasses. Must be called from the process's main thread. 

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
| `fd` | [FileDescriptor](../java.io/FileDescriptor.md)!:The raw file descriptor that the dump is being sent to. |
| `writer` | [PrintWriter](../java.io/PrintWriter.md)!:A PrintWriter to which the dump is to be set. |
| --- | --- |
| `args` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!:Additional arguments to the dump request. |

### forceLoad

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun forceLoad(): Unit
```

**Deprecated:** *Deprecated in Java.*

Force an asynchronous load. Unlike [startLoading()](Loader.md))this will ignore a previously loaded data set and load a new one. This simply calls through to the implementation's [onForceLoad()](Loader.md)). You generally should only call this when the loader is started -- that is, [isStarted()](Loader.md))returns true.

Must be called from the process's main thread. 

### getContext

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getContext(): Context!
```

**Deprecated:** *Deprecated in Java.*

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| [Context](Context.md)! | an application context retrieved from the Context passed to the constructor. |

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

Return whether this load has been reset. That is, either the loader has not yet been started for the first time, or its [reset()](Loader.md))has been called. 

### isStarted

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isStarted(): Boolean
```

**Deprecated:** *Deprecated in Java.*

Return whether this load has been started. That is, its [startLoading()](Loader.md))has been called and no calls to [stopLoading()](Loader.md))or [reset()](Loader.md))have yet been made. 

### onContentChanged

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onContentChanged(): Unit
```

**Deprecated:** *Deprecated in Java.*

Called when [ForceLoadContentObserver](../android/content/Loader.ForceLoadContentObserver.md) detects a change. The default implementation checks to see if the loader is currently started; if so, it simply calls [forceLoad()](Loader.md)); otherwise, it sets a flag so that [takeContentChanged()](Loader.md))returns true.

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
| `listener` | [Loader.OnLoadCanceledListener](../android/content/Loader.OnLoadCanceledListener.md)\<D\>!:The listener to register. |

### reset

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun reset(): Unit
```

**Deprecated:** *Deprecated in Java.*

This function will normally be called for you automatically by [android.app.LoaderManager](../android.app/LoaderManager.md) when destroying a Loader. When using a Loader with [android.app.LoaderManager](../android.app/LoaderManager.md), you*must not* call this method yourself, or you will conflict with its management of the Loader. Resets the state of the Loader. The Loader should at this point free all of its resources, since it may never be called again; however, its [startLoading()](Loader.md))may later be called at which point it must be able to start running again.

This updates the Loader's internal state so that [isStarted()](Loader.md))and [isReset()](Loader.md))will return the correct values, and then calls the implementation's [onReset()](Loader.md)).

Must be called from the process's main thread. 

### rollbackContentChanged

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun rollbackContentChanged(): Unit
```

**Deprecated:** *Deprecated in Java.*

Report that you have abandoned the processing of a content change that was returned by [takeContentChanged()](Loader.md))and would like to rollback to the state where there is again a pending content change. This is to handle the case where a data load due to a content change has been canceled before its data was delivered back to the loader. 

### startLoading

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun startLoading(): Unit
```

**Deprecated:** *Deprecated in Java.*

This function will normally be called for you automatically by [android.app.LoaderManager](../android.app/LoaderManager.md) when the associated fragment/activity is being started. When using a Loader with [android.app.LoaderManager](../android.app/LoaderManager.md), you*must not* call this method yourself, or you will conflict with its management of the Loader. Starts an asynchronous load of the Loader's data. When the result is ready the callbacks will be called on the process's main thread. If a previous load has been completed and is still valid the result may be passed to the callbacks immediately. The loader will monitor the source of the data set and may deliver future callbacks if the source changes. Calling [stopLoading](Loader.md))will stop the delivery of callbacks.

This updates the Loader's internal state so that [isStarted()](Loader.md))and [isReset()](Loader.md))will return the correct values, and then calls the implementation's [onStartLoading()](Loader.md)).

Must be called from the process's main thread. 

### stopLoading

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun stopLoading(): Unit
```

**Deprecated:** *Deprecated in Java.*

This function will normally be called for you automatically by [android.app.LoaderManager](../android.app/LoaderManager.md) when the associated fragment/activity is being stopped. When using a Loader with [android.app.LoaderManager](../android.app/LoaderManager.md), you*must not*call this method yourself, or you will conflict with its management of the Loader.

Stops delivery of updates until the next time [startLoading()](Loader.md))is called. Implementations should*not* invalidate their data at this point -- clients are still free to use the last data the loader reported. They will, however, typically stop reporting new data if the data changes; they can still monitor for changes, but must not report them to the client until and if [startLoading()](Loader.md))is later called.

This updates the Loader's internal state so that [isStarted()](Loader.md))will return the correct value, and then calls the implementation's [onStopLoading()](Loader.md)).

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

Remove a listener that was previously added with [registerListener](Loader.md)). Must be called from the process's main thread. 

### unregisterOnLoadCanceledListener

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun unregisterOnLoadCanceledListener(listener: Loader.OnLoadCanceledListener<D>!): Unit
```

**Deprecated:** *Deprecated in Java.*

Unregisters a listener that was previously added with [registerOnLoadCanceledListener](Loader.md)). Must be called from the process's main thread.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [Loader.OnLoadCanceledListener](../android/content/Loader.OnLoadCanceledListener.md)\<D\>!:The listener to unregister. |

## Protected methods

### onAbandon

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun onAbandon(): Unit
```

**Deprecated:** *Deprecated in Java.*

Subclasses implement this to take care of being abandoned. This is an optional intermediate state prior to [onReset()](Loader.md))-- it means that the client is no longer interested in any new data from the loader, so the loader must not report any further updates. However, the loader*must* keep its last reported data valid until the final [onReset()](Loader.md))happens. You can retrieve the current abandoned state with [isAbandoned](Loader.md)). 

### onCancelLoad

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun onCancelLoad(): Boolean
```

**Deprecated:** *Deprecated in Java.*

Subclasses must implement this to take care of requests to [cancelLoad()](Loader.md)). This will always be called from the process's main thread.

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | Returns false if the task could not be canceled, typically because it has already completed normally, or because [startLoading()](Loader.md))hasn't been called; returns true otherwise. When true is returned, the task is still running and the [OnLoadCanceledListener](../android/content/Loader.OnLoadCanceledListener.md) will be called when the task completes. |

### onForceLoad

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun onForceLoad(): Unit
```

**Deprecated:** *Deprecated in Java.*

Subclasses must implement this to take care of requests to [forceLoad()](Loader.md)). This will always be called from the process's main thread. 

### onReset

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun onReset(): Unit
```

**Deprecated:** *Deprecated in Java.*

Subclasses must implement this to take care of resetting their loader, as per [reset()](Loader.md)). This is not called by clients directly, but as a result of a call to [reset()](Loader.md)). This will always be called from the process's main thread. 

### onStartLoading

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun onStartLoading(): Unit
```

**Deprecated:** *Deprecated in Java.*

Subclasses must implement this to take care of loading their data, as per [startLoading()](Loader.md)). This is not called by clients directly, but as a result of a call to [startLoading()](Loader.md)). 

### onStopLoading

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun onStopLoading(): Unit
```

**Deprecated:** *Deprecated in Java.*

Subclasses must implement this to take care of stopping their loader, as per [stopLoading()](Loader.md)). This is not called by clients directly, but as a result of a call to [stopLoading()](Loader.md)). This will always be called from the process's main thread.
