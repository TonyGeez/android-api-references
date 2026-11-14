# android.content

# android.content

Kotlin | [Java](https://developer.android.com/reference/android/content/package-summary "View this page in Java")
| --- | --- |

## Interfaces

| [OnPrimaryClipChangedListener](https://developer.android.com/reference/kotlin/android/content/ClipboardManager.OnPrimaryClipChangedListener) | Defines a listener callback that is invoked when the primary clip on the clipboard changes. |
| --- | --- |
| [ComponentCallbacks](https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks) | The set of callback APIs that are common to all application components ([android.app.Activity](https://developer.android.com/reference/kotlin/android/app/Activity.html#), [android.app.Service](https://developer.android.com/reference/kotlin/android/app/Service.html#), [ContentProvider](https://developer.android.com/reference/kotlin/android/content/ContentProvider), and [android.app.Application](https://developer.android.com/reference/kotlin/android/app/Application.html#)). |
| [ComponentCallbacks2](https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2) | Callbacks for app state transitions that can be used to improve background memory management. |
| [PipeDataWriter](https://developer.android.com/reference/kotlin/android/content/ContentProvider.PipeDataWriter) | Interface to write a stream of data to a pipe. |
| --- | --- |
| [DialogInterface](https://developer.android.com/reference/kotlin/android/content/DialogInterface) | Interface that defines a dialog-type class that can be shown, dismissed, or canceled, and may have buttons that can be clicked. |
| [EntityIterator](https://developer.android.com/reference/kotlin/android/content/EntityIterator) | A specialization of [Iterator](https://developer.android.com/reference/kotlin/java/util/Iterator.html#) that allows iterating over a collection of [Entity](https://developer.android.com/reference/kotlin/android/content/Entity) objects. |
| [OnFinished](https://developer.android.com/reference/kotlin/android/content/IntentSender.OnFinished) | Callback interface for discovering when a send operation has completed. |
| --- | --- |
| [OnLoadCanceledListener](https://developer.android.com/reference/kotlin/android/content/Loader.OnLoadCanceledListener) | Interface that is implemented to discover when a Loader has been canceled before it finished loading its data. |
| [OnLoadCompleteListener](https://developer.android.com/reference/kotlin/android/content/Loader.OnLoadCompleteListener) | Interface that is implemented to discover when a Loader has finished loading its data. |
| [ServiceConnection](https://developer.android.com/reference/kotlin/android/content/ServiceConnection) | Interface for monitoring the state of an application service. |
| --- | --- |
| [SharedPreferences](https://developer.android.com/reference/kotlin/android/content/SharedPreferences) | Interface for accessing and modifying preference data returned by [android.content.Context#getSharedPreferences](https://developer.android.com/reference/kotlin/android/content/Context#getSharedPreferences(kotlin.String,%20kotlin.Int)). |
| [SyncStatusObserver](https://developer.android.com/reference/kotlin/android/content/SyncStatusObserver) | <br /> |

## Classes

| [AbstractThreadedSyncAdapter](https://developer.android.com/reference/kotlin/android/content/AbstractThreadedSyncAdapter) | An abstract implementation of a SyncAdapter that spawns a thread to invoke a sync operation. |
| --- | --- |
| [AsyncQueryHandler](https://developer.android.com/reference/kotlin/android/content/AsyncQueryHandler) | A helper class to help make handling asynchronous [ContentResolver](https://developer.android.com/reference/kotlin/android/content/ContentResolver) queries easier. |
| [AsyncTaskLoader](https://developer.android.com/reference/kotlin/android/content/AsyncTaskLoader) | Abstract Loader that provides an [AsyncTask](https://developer.android.com/reference/kotlin/android/os/AsyncTask.html#) to do the work. |
| [AttributionSource](https://developer.android.com/reference/kotlin/android/content/AttributionSource) | This class represents a source to which access to permission protected data should be attributed. |
| --- | --- |
| [BroadcastReceiver](https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver) | Base class for code that receives and handles broadcast intents sent by [android.content.Context#sendBroadcast(Intent)](https://developer.android.com/reference/kotlin/android/content/Context#sendBroadcast(android.content.Intent)). |
| [ClipboardManager](https://developer.android.com/reference/kotlin/android/content/ClipboardManager) | Interface to the clipboard service, for placing and retrieving text in the global clipboard. |
| [ClipData](https://developer.android.com/reference/kotlin/android/content/ClipData) | Representation of a clipped data on the clipboard. |
| --- | --- |
| [ClipDescription](https://developer.android.com/reference/kotlin/android/content/ClipDescription) | Meta-data describing the contents of a [ClipData](https://developer.android.com/reference/kotlin/android/content/ClipData). |
| [ComponentName](https://developer.android.com/reference/kotlin/android/content/ComponentName) | Identifier for a specific application component ([android.app.Activity](https://developer.android.com/reference/kotlin/android/app/Activity.html#), [android.app.Service](https://developer.android.com/reference/kotlin/android/app/Service.html#), [android.content.BroadcastReceiver](https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver), or [android.content.ContentProvider](https://developer.android.com/reference/kotlin/android/content/ContentProvider)) that is available. |
| [ContentProvider](https://developer.android.com/reference/kotlin/android/content/ContentProvider) | Content providers are one of the primary building blocks of Android applications, providing content to applications. |
| --- | --- |
| [ContentProviderClient](https://developer.android.com/reference/kotlin/android/content/ContentProviderClient) | The public interface object used to interact with a specific [ContentProvider](https://developer.android.com/reference/kotlin/android/content/ContentProvider). |
| [ContentProviderOperation](https://developer.android.com/reference/kotlin/android/content/ContentProviderOperation) | Represents a single operation to be performed as part of a batch of operations. |
| [ContentProviderResult](https://developer.android.com/reference/kotlin/android/content/ContentProviderResult) | Contains the result of the application of a [ContentProviderOperation](https://developer.android.com/reference/kotlin/android/content/ContentProviderOperation). |
| --- | --- |
| [ContentQueryMap](https://developer.android.com/reference/kotlin/android/content/ContentQueryMap) | Caches the contents of a cursor into a Map of String-\>ContentValues and optionally keeps the cache fresh by registering for updates on the content backing the cursor. |
| [ContentResolver](https://developer.android.com/reference/kotlin/android/content/ContentResolver) | This class provides applications access to the content model. |
| [ContentUris](https://developer.android.com/reference/kotlin/android/content/ContentUris) | Utility methods useful for working with [android.net.Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#) objects that use the "content" (content://) scheme. |
| --- | --- |
| [ContentValues](https://developer.android.com/reference/kotlin/android/content/ContentValues) | This class is used to store a set of values that the [ContentResolver](https://developer.android.com/reference/kotlin/android/content/ContentResolver) can process. |
| [Context](https://developer.android.com/reference/kotlin/android/content/Context) | Interface to global information about an application environment. |
| [ContextParams](https://developer.android.com/reference/kotlin/android/content/ContextParams) | This class represents rules around how a context being created via [Context.createContext](https://developer.android.com/reference/kotlin/android/content/Context#createContext(android.content.ContextParams)) should behave. |
| --- | --- |
| [ContextWrapper](https://developer.android.com/reference/kotlin/android/content/ContextWrapper) | Proxying implementation of Context that simply delegates all of its calls to another Context. |
| [CursorLoader](https://developer.android.com/reference/kotlin/android/content/CursorLoader) | A loader that queries the [ContentResolver](https://developer.android.com/reference/kotlin/android/content/ContentResolver) and returns a [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#). |
| [Entity](https://developer.android.com/reference/kotlin/android/content/Entity) | A representation of a item using ContentValues. |
| --- | --- |
| [Intent](https://developer.android.com/reference/kotlin/android/content/Intent) | An intent is an abstract description of an operation to be performed. |
| [IntentFilter](https://developer.android.com/reference/kotlin/android/content/IntentFilter) | Structured description of Intent values to be matched. |
| [IntentSender](https://developer.android.com/reference/kotlin/android/content/IntentSender) | A description of an Intent and target action to perform with it. |
| --- | --- |
| [Loader](https://developer.android.com/reference/kotlin/android/content/Loader) | A class that performs asynchronous loading of data. |
| [LocusId](https://developer.android.com/reference/kotlin/android/content/LocusId) | An identifier for an unique state (locus) in the application. |
| [MutableContextWrapper](https://developer.android.com/reference/kotlin/android/content/MutableContextWrapper) | Special version of [ContextWrapper](https://developer.android.com/reference/kotlin/android/content/ContextWrapper) that allows the base context to be modified after it is initially set. |
| --- | --- |
| [PeriodicSync](https://developer.android.com/reference/kotlin/android/content/PeriodicSync) | Value type that contains information about a periodic sync. |
| [QuickViewConstants](https://developer.android.com/reference/kotlin/android/content/QuickViewConstants) | Constants for [Intent.ACTION_QUICK_VIEW](https://developer.android.com/reference/kotlin/android/content/Intent#ACTION_QUICK_VIEW:kotlin.String). |
| [RestrictionEntry](https://developer.android.com/reference/kotlin/android/content/RestrictionEntry) | Applications can expose restrictions for a restricted user on a multiuser device. |
| --- | --- |
| [RestrictionsManager](https://developer.android.com/reference/kotlin/android/content/RestrictionsManager) | Provides a mechanism for apps to query restrictions imposed by an entity that manages the user. |
| [SearchRecentSuggestionsProvider](https://developer.android.com/reference/kotlin/android/content/SearchRecentSuggestionsProvider) | This superclass can be used to create a simple search suggestions provider for your application. |
| [SyncAdapterType](https://developer.android.com/reference/kotlin/android/content/SyncAdapterType) | Value type that represents a SyncAdapterType. |
| --- | --- |
| [SyncContext](https://developer.android.com/reference/kotlin/android/content/SyncContext) | <br /> |
| [SyncInfo](https://developer.android.com/reference/kotlin/android/content/SyncInfo) | Information about the sync operation that is currently underway. |
| [SyncRequest](https://developer.android.com/reference/kotlin/android/content/SyncRequest) | Convenience class to construct sync requests. |
| --- | --- |
| [SyncResult](https://developer.android.com/reference/kotlin/android/content/SyncResult) | This class is used to communicate the results of a sync operation to the SyncManager. |
| [SyncStats](https://developer.android.com/reference/kotlin/android/content/SyncStats) | Used to record various statistics about the result of a sync operation. |
| [UriMatcher](https://developer.android.com/reference/kotlin/android/content/UriMatcher) | Utility class to aid in matching URIs in content providers. |
| --- | --- |
| [UriPermission](https://developer.android.com/reference/kotlin/android/content/UriPermission) | Description of a single Uri permission grant. |
| [UriRelativeFilter](https://developer.android.com/reference/kotlin/android/content/UriRelativeFilter) | A filter for matching Intent URI Data as part of a [UriRelativeFilterGroup](https://developer.android.com/reference/kotlin/android/content/UriRelativeFilterGroup). |
| [UriRelativeFilterGroup](https://developer.android.com/reference/kotlin/android/content/UriRelativeFilterGroup) | An intent data matching group based on a URI's relative reference which includes the path, query and fragment. |
| --- | --- |

## Exceptions

| [ActivityNotFoundException](https://developer.android.com/reference/kotlin/android/content/ActivityNotFoundException) | This exception is thrown when a call to android. |
| --- | --- |
| [OperationApplicationException](https://developer.android.com/reference/kotlin/android/content/OperationApplicationException) | Thrown when an application of a [ContentProviderOperation](https://developer.android.com/reference/kotlin/android/content/ContentProviderOperation) fails due the specified constraints. |
| [ReceiverCallNotAllowedException](https://developer.android.com/reference/kotlin/android/content/ReceiverCallNotAllowedException) | This exception is thrown from android. |
