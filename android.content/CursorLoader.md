# CursorLoader

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CursorLoader

Kotlin| [Java](CursorLoader.md) 
| --- | --- |

```
open class CursorLoader : AsyncTaskLoader<Cursor!>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [android.content.Loader](Loader.md)\<D\> |||
| | ↳ | [android.content.AsyncTaskLoader](AsyncTaskLoader.md)\< [android.database.Cursor](../android.database/Cursor.md)\> ||
| | | ↳ | [android.content.CursorLoader](CursorLoader.md) |
| --- | --- | --- | --- |

| **This class was deprecated in API level 28.**
|
| Use the [Support Library](https://developer.android.com/tools/extras/support-library.html) androidx.loader.content.CursorLoader

A loader that queries the [ContentResolver](ContentResolver.md) and returns a [Cursor](../android.database/Cursor.md). This class implements the [Loader](Loader.md) protocol in a standard way for querying cursors, building on [AsyncTaskLoader](AsyncTaskLoader.md) to perform the cursor query on a background thread so that it does not block the application's UI.

A CursorLoader must be built with the full information for the query to perform, either through the[CursorLoader(android.content.Context,android.net.Uri,java.lang.String[],java.lang.String,java.lang.String[],java.lang.String)](https://developer.android.com/reference/kotlin/android/content/CursorLoader#CursorLoader(android.content.Context,%20android.net.Uri,%20kotlin.Array,%20kotlin.String,%20kotlin.Array,%20kotlin.String))or creating an empty instance with [CursorLoader(android.content.Context)](CursorLoader.md))and filling in the desired parameters with [setUri(android.net.Uri)](CursorLoader.md)), [setSelection(java.lang.String)](CursorLoader.md)),[setSelectionArgs(java.lang.String[])](https://developer.android.com/reference/kotlin/android/content/CursorLoader#setSelectionArgs(kotlin.Array)), [setSortOrder(java.lang.String)](CursorLoader.md)), and[setProjection(java.lang.String[])](https://developer.android.com/reference/kotlin/android/content/CursorLoader#setProjection(kotlin.Array)).

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [CursorLoader](CursorLoader.md))`(`context:` ` [Context](Context.md)!`)` Creates an empty unspecified CursorLoader. |
| [CursorLoader](CursorLoader.md))`(`context:` ` [Context](Context.md)!`, `uri:` ` [Uri](../android.net/Uri.md)!`, `projection:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`, `selection:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `selectionArgs:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`, `sortOrder:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Creates a fully-specified CursorLoader. |

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [cancelLoadInBackground](CursorLoader.md))`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [deliverResult](CursorLoader.md))`(`cursor:` ` [Cursor](../android.database/Cursor.md)!`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [dump](CursorLoader.md))`(`prefix:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `fd:` ` [FileDescriptor](../java.io/FileDescriptor.md)!`, `writer:` ` [PrintWriter](../java.io/PrintWriter.md)!`, `args:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`)` <br /> |
| --- | --- |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [getProjection](CursorLoader.md))`()` <br /> |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getSelection](CursorLoader.md))`()` <br /> |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [getSelectionArgs](CursorLoader.md))`()` <br /> |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getSortOrder](CursorLoader.md))`()` <br /> |
| open [Uri](../android.net/Uri.md)! | [getUri](CursorLoader.md))`()` <br /> |
| open [Cursor](../android.database/Cursor.md)! | [loadInBackground](CursorLoader.md))`()` <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onCanceled](CursorLoader.md))`(`cursor:` ` [Cursor](../android.database/Cursor.md)!`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setProjection](CursorLoader.md))`(`projection:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSelection](CursorLoader.md))`(`selection:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSelectionArgs](CursorLoader.md))`(`selectionArgs:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSortOrder](CursorLoader.md))`(`sortOrder:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setUri](CursorLoader.md))`(`uri:` ` [Uri](../android.net/Uri.md)!`)` <br /> |
| --- | --- |

| Protected methods ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onReset](CursorLoader.md))`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onStartLoading](CursorLoader.md))`()` Starts an asynchronous load of the data. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onStopLoading](CursorLoader.md))`()` Must be called from the UI thread |
| --- | --- |

| Inherited functions ||
|---|---|
| From class [Loader](Loader.md) |------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [abandon](Loader.md))`()` <br /> This function will normally be called for you automatically by [android.app.LoaderManager](../android.app/LoaderManager.md) when restarting a Loader. When using a Loader with [android.app.LoaderManager](../android.app/LoaderManager.md), you*must not* call this method yourself, or you will conflict with its management of the Loader. Tell the Loader that it is being abandoned. This is called prior to [reset](Loader.md))to have it retain its current data but not report any new data. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [cancelLoad](Loader.md))`()` <br /> Attempt to cancel the current load task. Must be called on the main thread of the process. Cancellation is not an immediate operation, since the load is performed in a background thread. If there is currently a load in progress, this method requests that the load be canceled, and notes this is the case; once the background thread has completed its work its remaining state will be cleared. If another load request comes in during this time, it will be held until the canceled load is complete. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [commitContentChanged](Loader.md))`()` <br /> Commit that you have actually fully processed a content change that was returned by [takeContentChanged](Loader.md)). This is for use with [rollbackContentChanged()](Loader.md))to handle situations where a load is cancelled. Call this when you have completely processed a load without it being cancelled. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [dataToString](Loader.md))`(`data:` `D`)` <br /> For debugging, converts an instance of the Loader's data class to a string that can be printed. Must handle a null data. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [deliverCancellation](Loader.md))`()` <br /> Informs the registered [OnLoadCanceledListener](../android/content/Loader.OnLoadCanceledListener.md) that the load has been canceled. Should only be called by subclasses. Must be called from the process's main thread. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [deliverResult](Loader.md))`(`data:` `D`)` <br /> Sends the result of the load to the registered listener. Should only be called by subclasses. Must be called from the process's main thread. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [forceLoad](Loader.md))`()` <br /> Force an asynchronous load. Unlike [startLoading()](Loader.md))this will ignore a previously loaded data set and load a new one. This simply calls through to the implementation's [onForceLoad()](Loader.md)). You generally should only call this when the loader is started -- that is, [isStarted()](Loader.md))returns true. Must be called from the process's main thread. <br /> | | [Context](Context.md)! | [getContext](Loader.md))`()` <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getId](Loader.md))`()` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isAbandoned](Loader.md))`()` <br /> Return whether this loader has been abandoned. In this state, the loader*must not* report any new data, and*must*keep its last reported data valid until it is finally reset. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isReset](Loader.md))`()` <br /> Return whether this load has been reset. That is, either the loader has not yet been started for the first time, or its [reset()](Loader.md))has been called. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isStarted](Loader.md))`()` <br /> Return whether this load has been started. That is, its [startLoading()](Loader.md))has been called and no calls to [stopLoading()](Loader.md))or [reset()](Loader.md))have yet been made. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onAbandon](Loader.md))`()` <br /> Subclasses implement this to take care of being abandoned. This is an optional intermediate state prior to [onReset()](Loader.md))-- it means that the client is no longer interested in any new data from the loader, so the loader must not report any further updates. However, the loader*must* keep its last reported data valid until the final [onReset()](Loader.md))happens. You can retrieve the current abandoned state with [isAbandoned](Loader.md)). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onContentChanged](Loader.md))`()` <br /> Called when [ForceLoadContentObserver](../android/content/Loader.ForceLoadContentObserver.md) detects a change. The default implementation checks to see if the loader is currently started; if so, it simply calls [forceLoad()](Loader.md)); otherwise, it sets a flag so that [takeContentChanged()](Loader.md))returns true. Must be called from the process's main thread. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onReset](Loader.md))`()` <br /> Subclasses must implement this to take care of resetting their loader, as per [reset()](Loader.md)). This is not called by clients directly, but as a result of a call to [reset()](Loader.md)). This will always be called from the process's main thread. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onStartLoading](Loader.md))`()` <br /> Subclasses must implement this to take care of loading their data, as per [startLoading()](Loader.md)). This is not called by clients directly, but as a result of a call to [startLoading()](Loader.md)). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onStopLoading](Loader.md))`()` <br /> Subclasses must implement this to take care of stopping their loader, as per [stopLoading()](Loader.md)). This is not called by clients directly, but as a result of a call to [stopLoading()](Loader.md)). This will always be called from the process's main thread. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerListener](Loader.md))`(`id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `listener:` ` [Loader.OnLoadCompleteListener](../android/content/Loader.OnLoadCompleteListener.md)<D>!`)` <br /> Registers a class that will receive callbacks when a load is complete. The callback will be called on the process's main thread so it's safe to pass the results to widgets. Must be called from the process's main thread. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerOnLoadCanceledListener](Loader.md))`(`listener:` ` [Loader.OnLoadCanceledListener](../android/content/Loader.OnLoadCanceledListener.md)<D>!`)` <br /> Registers a listener that will receive callbacks when a load is canceled. The callback will be called on the process's main thread so it's safe to pass the results to widgets. Must be called from the process's main thread. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [reset](Loader.md))`()` <br /> This function will normally be called for you automatically by [android.app.LoaderManager](../android.app/LoaderManager.md) when destroying a Loader. When using a Loader with [android.app.LoaderManager](../android.app/LoaderManager.md), you*must not* call this method yourself, or you will conflict with its management of the Loader. Resets the state of the Loader. The Loader should at this point free all of its resources, since it may never be called again; however, its [startLoading()](Loader.md))may later be called at which point it must be able to start running again. This updates the Loader's internal state so that [isStarted()](Loader.md))and [isReset()](Loader.md))will return the correct values, and then calls the implementation's [onReset()](Loader.md)). Must be called from the process's main thread. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [rollbackContentChanged](Loader.md))`()` <br /> Report that you have abandoned the processing of a content change that was returned by [takeContentChanged()](Loader.md))and would like to rollback to the state where there is again a pending content change. This is to handle the case where a data load due to a content change has been canceled before its data was delivered back to the loader. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [startLoading](Loader.md))`()` <br /> This function will normally be called for you automatically by [android.app.LoaderManager](../android.app/LoaderManager.md) when the associated fragment/activity is being started. When using a Loader with [android.app.LoaderManager](../android.app/LoaderManager.md), you*must not* call this method yourself, or you will conflict with its management of the Loader. Starts an asynchronous load of the Loader's data. When the result is ready the callbacks will be called on the process's main thread. If a previous load has been completed and is still valid the result may be passed to the callbacks immediately. The loader will monitor the source of the data set and may deliver future callbacks if the source changes. Calling [stopLoading](Loader.md))will stop the delivery of callbacks. This updates the Loader's internal state so that [isStarted()](Loader.md))and [isReset()](Loader.md))will return the correct values, and then calls the implementation's [onStartLoading()](Loader.md)). Must be called from the process's main thread. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [stopLoading](Loader.md))`()` <br /> This function will normally be called for you automatically by [android.app.LoaderManager](../android.app/LoaderManager.md) when the associated fragment/activity is being stopped. When using a Loader with [android.app.LoaderManager](../android.app/LoaderManager.md), you*must not*call this method yourself, or you will conflict with its management of the Loader. Stops delivery of updates until the next time [startLoading()](Loader.md))is called. Implementations should*not* invalidate their data at this point -- clients are still free to use the last data the loader reported. They will, however, typically stop reporting new data if the data changes; they can still monitor for changes, but must not report them to the client until and if [startLoading()](Loader.md))is later called. This updates the Loader's internal state so that [isStarted()](Loader.md))will return the correct value, and then calls the implementation's [onStopLoading()](Loader.md)). Must be called from the process's main thread. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [takeContentChanged](Loader.md))`()` <br /> Take the current flag indicating whether the loader's content had changed while it was stopped. If it had, true is returned and the flag is cleared. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](Loader.md))`()` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unregisterListener](Loader.md))`(`listener:` ` [Loader.OnLoadCompleteListener](../android/content/Loader.OnLoadCompleteListener.md)<D>!`)` <br /> Remove a listener that was previously added with [registerListener](Loader.md)). Must be called from the process's main thread. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unregisterOnLoadCanceledListener](Loader.md))`(`listener:` ` [Loader.OnLoadCanceledListener](../android/content/Loader.OnLoadCanceledListener.md)<D>!`)` <br /> Unregisters a listener that was previously added with [registerOnLoadCanceledListener](Loader.md)). Must be called from the process's main thread. <br /> | ||
| From class [AsyncTaskLoader](AsyncTaskLoader.md) |------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isLoadInBackgroundCanceled](AsyncTaskLoader.md))`()` <br /> Returns true if the current invocation of [loadInBackground](AsyncTaskLoader.md))is being canceled. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onCancelLoad](AsyncTaskLoader.md))`()` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onForceLoad](AsyncTaskLoader.md))`()` <br /> | | D | [onLoadInBackground](AsyncTaskLoader.md))`()` <br /> Calls [loadInBackground()](AsyncTaskLoader.md)). This method is reserved for use by the loader framework. Subclasses should override [loadInBackground](AsyncTaskLoader.md))instead of this method. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setUpdateThrottle](AsyncTaskLoader.md))`(`delayMS:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` <br /> Set amount to throttle updates by. This is the minimum time from when the last [loadInBackground()](AsyncTaskLoader.md))call has completed until a new load is scheduled. <br /> | ||

## Public constructors

### CursorLoader

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
CursorLoader(context: Context!)
```

Creates an empty unspecified CursorLoader. You must follow this with calls to [setUri(android.net.Uri)](CursorLoader.md)), [setSelection(java.lang.String)](CursorLoader.md)), etc to specify the query to perform. 

### CursorLoader

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
CursorLoader(
    context: Context!, 
    uri: Uri!, 
    projection: Array<String!>!, 
    selection: String!, 
    selectionArgs: Array<String!>!, 
    sortOrder: String!)
```

Creates a fully-specified CursorLoader. See [ContentResolver.query()](ContentResolver.md))for documentation on the meaning of the parameters. These will be passed as-is to that call.

## Public methods

### cancelLoadInBackground

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun cancelLoadInBackground(): Unit
```

**Deprecated:** *Deprecated in Java.* 

### deliverResult

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun deliverResult(cursor: Cursor!): Unit
```

**Deprecated:** *Deprecated in Java.*

| Parameters ||
|--------|------------------------|
| `data` | the result of the load |

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

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `prefix` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:Text to print at the front of each line. |
| `fd` | [FileDescriptor](../java.io/FileDescriptor.md)!:The raw file descriptor that the dump is being sent to. |
| `writer` | [PrintWriter](../java.io/PrintWriter.md)!:A PrintWriter to which the dump is to be set. |
| --- | --- |
| `args` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!:Additional arguments to the dump request. |

### getProjection

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getProjection(): Array<String!>!
```

**Deprecated:** *Deprecated in Java.* 

### getSelection

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSelection(): String!
```

**Deprecated:** *Deprecated in Java.* 

### getSelectionArgs

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSelectionArgs(): Array<String!>!
```

**Deprecated:** *Deprecated in Java.* 

### getSortOrder

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSortOrder(): String!
```

**Deprecated:** *Deprecated in Java.* 

### getUri

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getUri(): Uri!
```

**Deprecated:** *Deprecated in Java.* 

### loadInBackground

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun loadInBackground(): Cursor!
```

**Deprecated:** *Deprecated in Java.*

| Return ||
|-----------------------------------------------------------------------------------------|-----------------------------------|
| [Cursor](../android.database/Cursor.md)! | The result of the load operation. |

| Exceptions ||
|-----------------------------------------|-------------------------------------------|
| `android.os.OperationCanceledException` | if the load is canceled during execution. |

### onCanceled

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onCanceled(cursor: Cursor!): Unit
```

**Deprecated:** *Deprecated in Java.*

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `data` | The value that was returned by [loadInBackground](AsyncTaskLoader.md)), or null if the task threw [OperationCanceledException](../android.os/OperationCanceledException.md). |

### setProjection

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setProjection(projection: Array<String!>!): Unit
```

**Deprecated:** *Deprecated in Java.* 

### setSelection

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setSelection(selection: String!): Unit
```

**Deprecated:** *Deprecated in Java.* 

### setSelectionArgs

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setSelectionArgs(selectionArgs: Array<String!>!): Unit
```

**Deprecated:** *Deprecated in Java.* 

### setSortOrder

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setSortOrder(sortOrder: String!): Unit
```

**Deprecated:** *Deprecated in Java.* 

### setUri

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setUri(uri: Uri!): Unit
```

**Deprecated:** *Deprecated in Java.*

## Protected methods

### onReset

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun onReset(): Unit
```

**Deprecated:** *Deprecated in Java.* 

### onStartLoading

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun onStartLoading(): Unit
```

**Deprecated:** *Deprecated in Java.*

Starts an asynchronous load of the data. When the result is ready the callbacks will be called on the UI thread. If a previous load has been completed and is still valid the result may be passed to the callbacks immediately. Must be called from the UI thread 

### onStopLoading

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun onStopLoading(): Unit
```

**Deprecated:** *Deprecated in Java.*

Must be called from the UI thread
