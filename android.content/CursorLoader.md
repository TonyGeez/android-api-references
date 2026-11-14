# CursorLoader

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CursorLoader

Kotlin| [Java](https://developer.android.com/reference/android/content/CursorLoader "View this page in Java") 

```
open class CursorLoader : AsyncTaskLoader<Cursor!>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| ↳ | [android.content.Loader](https://developer.android.com/reference/kotlin/android/content/Loader)\<D\> |||
| | ↳ | [android.content.AsyncTaskLoader](https://developer.android.com/reference/kotlin/android/content/AsyncTaskLoader)\< [android.database.Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#)\> ||
| | | ↳ | [android.content.CursorLoader](https://developer.android.com/reference/kotlin/android/content/CursorLoader#) |

| **This class was deprecated in API level 28.**
|
| Use the [Support Library](https://developer.android.com/tools/extras/support-library.html) androidx.loader.content.CursorLoader

A loader that queries the [ContentResolver](https://developer.android.com/reference/kotlin/android/content/ContentResolver) and returns a [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#). This class implements the [Loader](https://developer.android.com/reference/kotlin/android/content/Loader) protocol in a standard way for querying cursors, building on [AsyncTaskLoader](https://developer.android.com/reference/kotlin/android/content/AsyncTaskLoader) to perform the cursor query on a background thread so that it does not block the application's UI.

A CursorLoader must be built with the full information for the query to perform, either through the[CursorLoader(android.content.Context,android.net.Uri,java.lang.String[],java.lang.String,java.lang.String[],java.lang.String)](https://developer.android.com/reference/kotlin/android/content/CursorLoader#CursorLoader(android.content.Context,%20android.net.Uri,%20kotlin.Array,%20kotlin.String,%20kotlin.Array,%20kotlin.String))or creating an empty instance with [CursorLoader(android.content.Context)](https://developer.android.com/reference/kotlin/android/content/CursorLoader#CursorLoader(android.content.Context))and filling in the desired parameters with [setUri(android.net.Uri)](https://developer.android.com/reference/kotlin/android/content/CursorLoader#setUri(android.net.Uri)), [setSelection(java.lang.String)](https://developer.android.com/reference/kotlin/android/content/CursorLoader#setSelection(kotlin.String)),[setSelectionArgs(java.lang.String[])](https://developer.android.com/reference/kotlin/android/content/CursorLoader#setSelectionArgs(kotlin.Array)), [setSortOrder(java.lang.String)](https://developer.android.com/reference/kotlin/android/content/CursorLoader#setSortOrder(kotlin.String)), and[setProjection(java.lang.String[])](https://developer.android.com/reference/kotlin/android/content/CursorLoader#setProjection(kotlin.Array)).

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [CursorLoader](https://developer.android.com/reference/kotlin/android/content/CursorLoader#CursorLoader(android.content.Context))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context)!`)` Creates an empty unspecified CursorLoader. |
| [CursorLoader](https://developer.android.com/reference/kotlin/android/content/CursorLoader#CursorLoader(android.content.Context,%20android.net.Uri,%20kotlin.Array,%20kotlin.String,%20kotlin.Array,%20kotlin.String))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context)!`, `uri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)!`, `projection:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`, `selection:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `selectionArgs:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`, `sortOrder:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Creates a fully-specified CursorLoader. |

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [cancelLoadInBackground](https://developer.android.com/reference/kotlin/android/content/CursorLoader#cancelLoadInBackground())`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [deliverResult](https://developer.android.com/reference/kotlin/android/content/CursorLoader#deliverResult(android.database.Cursor))`(`cursor:` ` [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#)!`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [dump](https://developer.android.com/reference/kotlin/android/content/CursorLoader#dump(kotlin.String,%20java.io.FileDescriptor,%20java.io.PrintWriter,%20kotlin.Array))`(`prefix:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `fd:` ` [FileDescriptor](https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#)!`, `writer:` ` [PrintWriter](https://developer.android.com/reference/kotlin/java/io/PrintWriter.html#)!`, `args:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`)` <br /> |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [getProjection](https://developer.android.com/reference/kotlin/android/content/CursorLoader#getProjection())`()` <br /> |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getSelection](https://developer.android.com/reference/kotlin/android/content/CursorLoader#getSelection())`()` <br /> |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [getSelectionArgs](https://developer.android.com/reference/kotlin/android/content/CursorLoader#getSelectionArgs())`()` <br /> |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getSortOrder](https://developer.android.com/reference/kotlin/android/content/CursorLoader#getSortOrder())`()` <br /> |
| open [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)! | [getUri](https://developer.android.com/reference/kotlin/android/content/CursorLoader#getUri())`()` <br /> |
| open [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#)! | [loadInBackground](https://developer.android.com/reference/kotlin/android/content/CursorLoader#loadInBackground())`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onCanceled](https://developer.android.com/reference/kotlin/android/content/CursorLoader#onCanceled(android.database.Cursor))`(`cursor:` ` [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#)!`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setProjection](https://developer.android.com/reference/kotlin/android/content/CursorLoader#setProjection(kotlin.Array))`(`projection:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSelection](https://developer.android.com/reference/kotlin/android/content/CursorLoader#setSelection(kotlin.String))`(`selection:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSelectionArgs](https://developer.android.com/reference/kotlin/android/content/CursorLoader#setSelectionArgs(kotlin.Array))`(`selectionArgs:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSortOrder](https://developer.android.com/reference/kotlin/android/content/CursorLoader#setSortOrder(kotlin.String))`(`sortOrder:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setUri](https://developer.android.com/reference/kotlin/android/content/CursorLoader#setUri(android.net.Uri))`(`uri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)!`)` <br /> |

| Protected methods ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onReset](https://developer.android.com/reference/kotlin/android/content/CursorLoader#onReset())`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onStartLoading](https://developer.android.com/reference/kotlin/android/content/CursorLoader#onStartLoading())`()` Starts an asynchronous load of the data. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onStopLoading](https://developer.android.com/reference/kotlin/android/content/CursorLoader#onStopLoading())`()` Must be called from the UI thread |

| Inherited functions ||
|---|---|
| From class [Loader](https://developer.android.com/reference/kotlin/android/content/Loader) |------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [abandon](https://developer.android.com/reference/kotlin/android/content/Loader#abandon())`()` <br /> This function will normally be called for you automatically by [android.app.LoaderManager](https://developer.android.com/reference/kotlin/android/app/LoaderManager.html#) when restarting a Loader. When using a Loader with [android.app.LoaderManager](https://developer.android.com/reference/kotlin/android/app/LoaderManager.html#), you*must not* call this method yourself, or you will conflict with its management of the Loader. Tell the Loader that it is being abandoned. This is called prior to [reset](https://developer.android.com/reference/kotlin/android/content/Loader#reset())to have it retain its current data but not report any new data. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [cancelLoad](https://developer.android.com/reference/kotlin/android/content/Loader#cancelLoad())`()` <br /> Attempt to cancel the current load task. Must be called on the main thread of the process. Cancellation is not an immediate operation, since the load is performed in a background thread. If there is currently a load in progress, this method requests that the load be canceled, and notes this is the case; once the background thread has completed its work its remaining state will be cleared. If another load request comes in during this time, it will be held until the canceled load is complete. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [commitContentChanged](https://developer.android.com/reference/kotlin/android/content/Loader#commitContentChanged())`()` <br /> Commit that you have actually fully processed a content change that was returned by [takeContentChanged](https://developer.android.com/reference/kotlin/android/content/Loader#takeContentChanged()). This is for use with [rollbackContentChanged()](https://developer.android.com/reference/kotlin/android/content/Loader#rollbackContentChanged())to handle situations where a load is cancelled. Call this when you have completely processed a load without it being cancelled. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [dataToString](https://developer.android.com/reference/kotlin/android/content/Loader#dataToString(android.content.Loader.ForceLoadContentObserver.D))`(`data:` `D`)` <br /> For debugging, converts an instance of the Loader's data class to a string that can be printed. Must handle a null data. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [deliverCancellation](https://developer.android.com/reference/kotlin/android/content/Loader#deliverCancellation())`()` <br /> Informs the registered [OnLoadCanceledListener](https://developer.android.com/reference/kotlin/android/content/Loader.OnLoadCanceledListener) that the load has been canceled. Should only be called by subclasses. Must be called from the process's main thread. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [deliverResult](https://developer.android.com/reference/kotlin/android/content/Loader#deliverResult(android.content.Loader.ForceLoadContentObserver.D))`(`data:` `D`)` <br /> Sends the result of the load to the registered listener. Should only be called by subclasses. Must be called from the process's main thread. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [forceLoad](https://developer.android.com/reference/kotlin/android/content/Loader#forceLoad())`()` <br /> Force an asynchronous load. Unlike [startLoading()](https://developer.android.com/reference/kotlin/android/content/Loader#startLoading())this will ignore a previously loaded data set and load a new one. This simply calls through to the implementation's [onForceLoad()](https://developer.android.com/reference/kotlin/android/content/Loader#onForceLoad()). You generally should only call this when the loader is started -- that is, [isStarted()](https://developer.android.com/reference/kotlin/android/content/Loader#isStarted())returns true. Must be called from the process's main thread. <br /> | | [Context](https://developer.android.com/reference/kotlin/android/content/Context)! | [getContext](https://developer.android.com/reference/kotlin/android/content/Loader#getContext())`()` <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getId](https://developer.android.com/reference/kotlin/android/content/Loader#getId())`()` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isAbandoned](https://developer.android.com/reference/kotlin/android/content/Loader#isAbandoned())`()` <br /> Return whether this loader has been abandoned. In this state, the loader*must not* report any new data, and*must*keep its last reported data valid until it is finally reset. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isReset](https://developer.android.com/reference/kotlin/android/content/Loader#isReset())`()` <br /> Return whether this load has been reset. That is, either the loader has not yet been started for the first time, or its [reset()](https://developer.android.com/reference/kotlin/android/content/Loader#reset())has been called. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isStarted](https://developer.android.com/reference/kotlin/android/content/Loader#isStarted())`()` <br /> Return whether this load has been started. That is, its [startLoading()](https://developer.android.com/reference/kotlin/android/content/Loader#startLoading())has been called and no calls to [stopLoading()](https://developer.android.com/reference/kotlin/android/content/Loader#stopLoading())or [reset()](https://developer.android.com/reference/kotlin/android/content/Loader#reset())have yet been made. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onAbandon](https://developer.android.com/reference/kotlin/android/content/Loader#onAbandon())`()` <br /> Subclasses implement this to take care of being abandoned. This is an optional intermediate state prior to [onReset()](https://developer.android.com/reference/kotlin/android/content/Loader#onReset())-- it means that the client is no longer interested in any new data from the loader, so the loader must not report any further updates. However, the loader*must* keep its last reported data valid until the final [onReset()](https://developer.android.com/reference/kotlin/android/content/Loader#onReset())happens. You can retrieve the current abandoned state with [isAbandoned](https://developer.android.com/reference/kotlin/android/content/Loader#isAbandoned()). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onContentChanged](https://developer.android.com/reference/kotlin/android/content/Loader#onContentChanged())`()` <br /> Called when [ForceLoadContentObserver](https://developer.android.com/reference/kotlin/android/content/Loader.ForceLoadContentObserver) detects a change. The default implementation checks to see if the loader is currently started; if so, it simply calls [forceLoad()](https://developer.android.com/reference/kotlin/android/content/Loader#forceLoad()); otherwise, it sets a flag so that [takeContentChanged()](https://developer.android.com/reference/kotlin/android/content/Loader#takeContentChanged())returns true. Must be called from the process's main thread. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onReset](https://developer.android.com/reference/kotlin/android/content/Loader#onReset())`()` <br /> Subclasses must implement this to take care of resetting their loader, as per [reset()](https://developer.android.com/reference/kotlin/android/content/Loader#reset()). This is not called by clients directly, but as a result of a call to [reset()](https://developer.android.com/reference/kotlin/android/content/Loader#reset()). This will always be called from the process's main thread. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onStartLoading](https://developer.android.com/reference/kotlin/android/content/Loader#onStartLoading())`()` <br /> Subclasses must implement this to take care of loading their data, as per [startLoading()](https://developer.android.com/reference/kotlin/android/content/Loader#startLoading()). This is not called by clients directly, but as a result of a call to [startLoading()](https://developer.android.com/reference/kotlin/android/content/Loader#startLoading()). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onStopLoading](https://developer.android.com/reference/kotlin/android/content/Loader#onStopLoading())`()` <br /> Subclasses must implement this to take care of stopping their loader, as per [stopLoading()](https://developer.android.com/reference/kotlin/android/content/Loader#stopLoading()). This is not called by clients directly, but as a result of a call to [stopLoading()](https://developer.android.com/reference/kotlin/android/content/Loader#stopLoading()). This will always be called from the process's main thread. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerListener](https://developer.android.com/reference/kotlin/android/content/Loader#registerListener(kotlin.Int,%20android.content.Loader.OnLoadCompleteListener))`(`id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `listener:` ` [Loader.OnLoadCompleteListener](https://developer.android.com/reference/kotlin/android/content/Loader.OnLoadCompleteListener)<D>!`)` <br /> Registers a class that will receive callbacks when a load is complete. The callback will be called on the process's main thread so it's safe to pass the results to widgets. Must be called from the process's main thread. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerOnLoadCanceledListener](https://developer.android.com/reference/kotlin/android/content/Loader#registerOnLoadCanceledListener(android.content.Loader.OnLoadCanceledListener))`(`listener:` ` [Loader.OnLoadCanceledListener](https://developer.android.com/reference/kotlin/android/content/Loader.OnLoadCanceledListener)<D>!`)` <br /> Registers a listener that will receive callbacks when a load is canceled. The callback will be called on the process's main thread so it's safe to pass the results to widgets. Must be called from the process's main thread. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [reset](https://developer.android.com/reference/kotlin/android/content/Loader#reset())`()` <br /> This function will normally be called for you automatically by [android.app.LoaderManager](https://developer.android.com/reference/kotlin/android/app/LoaderManager.html#) when destroying a Loader. When using a Loader with [android.app.LoaderManager](https://developer.android.com/reference/kotlin/android/app/LoaderManager.html#), you*must not* call this method yourself, or you will conflict with its management of the Loader. Resets the state of the Loader. The Loader should at this point free all of its resources, since it may never be called again; however, its [startLoading()](https://developer.android.com/reference/kotlin/android/content/Loader#startLoading())may later be called at which point it must be able to start running again. This updates the Loader's internal state so that [isStarted()](https://developer.android.com/reference/kotlin/android/content/Loader#isStarted())and [isReset()](https://developer.android.com/reference/kotlin/android/content/Loader#isReset())will return the correct values, and then calls the implementation's [onReset()](https://developer.android.com/reference/kotlin/android/content/Loader#onReset()). Must be called from the process's main thread. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [rollbackContentChanged](https://developer.android.com/reference/kotlin/android/content/Loader#rollbackContentChanged())`()` <br /> Report that you have abandoned the processing of a content change that was returned by [takeContentChanged()](https://developer.android.com/reference/kotlin/android/content/Loader#takeContentChanged())and would like to rollback to the state where there is again a pending content change. This is to handle the case where a data load due to a content change has been canceled before its data was delivered back to the loader. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [startLoading](https://developer.android.com/reference/kotlin/android/content/Loader#startLoading())`()` <br /> This function will normally be called for you automatically by [android.app.LoaderManager](https://developer.android.com/reference/kotlin/android/app/LoaderManager.html#) when the associated fragment/activity is being started. When using a Loader with [android.app.LoaderManager](https://developer.android.com/reference/kotlin/android/app/LoaderManager.html#), you*must not* call this method yourself, or you will conflict with its management of the Loader. Starts an asynchronous load of the Loader's data. When the result is ready the callbacks will be called on the process's main thread. If a previous load has been completed and is still valid the result may be passed to the callbacks immediately. The loader will monitor the source of the data set and may deliver future callbacks if the source changes. Calling [stopLoading](https://developer.android.com/reference/kotlin/android/content/Loader#stopLoading())will stop the delivery of callbacks. This updates the Loader's internal state so that [isStarted()](https://developer.android.com/reference/kotlin/android/content/Loader#isStarted())and [isReset()](https://developer.android.com/reference/kotlin/android/content/Loader#isReset())will return the correct values, and then calls the implementation's [onStartLoading()](https://developer.android.com/reference/kotlin/android/content/Loader#onStartLoading()). Must be called from the process's main thread. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [stopLoading](https://developer.android.com/reference/kotlin/android/content/Loader#stopLoading())`()` <br /> This function will normally be called for you automatically by [android.app.LoaderManager](https://developer.android.com/reference/kotlin/android/app/LoaderManager.html#) when the associated fragment/activity is being stopped. When using a Loader with [android.app.LoaderManager](https://developer.android.com/reference/kotlin/android/app/LoaderManager.html#), you*must not*call this method yourself, or you will conflict with its management of the Loader. Stops delivery of updates until the next time [startLoading()](https://developer.android.com/reference/kotlin/android/content/Loader#startLoading())is called. Implementations should*not* invalidate their data at this point -- clients are still free to use the last data the loader reported. They will, however, typically stop reporting new data if the data changes; they can still monitor for changes, but must not report them to the client until and if [startLoading()](https://developer.android.com/reference/kotlin/android/content/Loader#startLoading())is later called. This updates the Loader's internal state so that [isStarted()](https://developer.android.com/reference/kotlin/android/content/Loader#isStarted())will return the correct value, and then calls the implementation's [onStopLoading()](https://developer.android.com/reference/kotlin/android/content/Loader#onStopLoading()). Must be called from the process's main thread. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [takeContentChanged](https://developer.android.com/reference/kotlin/android/content/Loader#takeContentChanged())`()` <br /> Take the current flag indicating whether the loader's content had changed while it was stopped. If it had, true is returned and the flag is cleared. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/content/Loader#toString())`()` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unregisterListener](https://developer.android.com/reference/kotlin/android/content/Loader#unregisterListener(android.content.Loader.OnLoadCompleteListener))`(`listener:` ` [Loader.OnLoadCompleteListener](https://developer.android.com/reference/kotlin/android/content/Loader.OnLoadCompleteListener)<D>!`)` <br /> Remove a listener that was previously added with [registerListener](https://developer.android.com/reference/kotlin/android/content/Loader#registerListener(kotlin.Int,%20android.content.Loader.OnLoadCompleteListener)). Must be called from the process's main thread. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unregisterOnLoadCanceledListener](https://developer.android.com/reference/kotlin/android/content/Loader#unregisterOnLoadCanceledListener(android.content.Loader.OnLoadCanceledListener))`(`listener:` ` [Loader.OnLoadCanceledListener](https://developer.android.com/reference/kotlin/android/content/Loader.OnLoadCanceledListener)<D>!`)` <br /> Unregisters a listener that was previously added with [registerOnLoadCanceledListener](https://developer.android.com/reference/kotlin/android/content/Loader#registerOnLoadCanceledListener(android.content.Loader.OnLoadCanceledListener)). Must be called from the process's main thread. <br /> | ||
| From class [AsyncTaskLoader](https://developer.android.com/reference/kotlin/android/content/AsyncTaskLoader) |------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isLoadInBackgroundCanceled](https://developer.android.com/reference/kotlin/android/content/AsyncTaskLoader#isLoadInBackgroundCanceled())`()` <br /> Returns true if the current invocation of [loadInBackground](https://developer.android.com/reference/kotlin/android/content/AsyncTaskLoader#loadInBackground())is being canceled. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onCancelLoad](https://developer.android.com/reference/kotlin/android/content/AsyncTaskLoader#onCancelLoad())`()` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onForceLoad](https://developer.android.com/reference/kotlin/android/content/AsyncTaskLoader#onForceLoad())`()` <br /> | | D | [onLoadInBackground](https://developer.android.com/reference/kotlin/android/content/AsyncTaskLoader#onLoadInBackground())`()` <br /> Calls [loadInBackground()](https://developer.android.com/reference/kotlin/android/content/AsyncTaskLoader#loadInBackground()). This method is reserved for use by the loader framework. Subclasses should override [loadInBackground](https://developer.android.com/reference/kotlin/android/content/AsyncTaskLoader#loadInBackground())instead of this method. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setUpdateThrottle](https://developer.android.com/reference/kotlin/android/content/AsyncTaskLoader#setUpdateThrottle(kotlin.Long))`(`delayMS:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` <br /> Set amount to throttle updates by. This is the minimum time from when the last [loadInBackground()](https://developer.android.com/reference/kotlin/android/content/AsyncTaskLoader#loadInBackground())call has completed until a new load is scheduled. <br /> | ||

## Public constructors

### CursorLoader

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
CursorLoader(context: Context!)
```

Creates an empty unspecified CursorLoader. You must follow this with calls to [setUri(android.net.Uri)](https://developer.android.com/reference/kotlin/android/content/CursorLoader#setUri(android.net.Uri)), [setSelection(java.lang.String)](https://developer.android.com/reference/kotlin/android/content/CursorLoader#setSelection(kotlin.String)), etc to specify the query to perform. 

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

Creates a fully-specified CursorLoader. See [ContentResolver.query()](https://developer.android.com/reference/kotlin/android/content/ContentResolver#query(android.net.Uri,%20kotlin.Array,%20kotlin.String,%20kotlin.Array,%20kotlin.String))for documentation on the meaning of the parameters. These will be passed as-is to that call.

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
| `fd` | [FileDescriptor](https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#)!:The raw file descriptor that the dump is being sent to. |
| `writer` | [PrintWriter](https://developer.android.com/reference/kotlin/java/io/PrintWriter.html#)!:A PrintWriter to which the dump is to be set. |
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
| [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#)! | The result of the load operation. |

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
| `data` | The value that was returned by [loadInBackground](https://developer.android.com/reference/kotlin/android/content/AsyncTaskLoader#loadInBackground()), or null if the task threw [OperationCanceledException](https://developer.android.com/reference/kotlin/android/os/OperationCanceledException.html#). |

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
