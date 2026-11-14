# android.content

# android.content

Kotlin | [Java](../android/content/_package.md)
| --- | --- |

## Interfaces

| [OnPrimaryClipChangedListener](../android/content/ClipboardManager.OnPrimaryClipChangedListener.md) | Defines a listener callback that is invoked when the primary clip on the clipboard changes. |
| --- | --- |
| [ComponentCallbacks](../android/content/ComponentCallbacks.md) | The set of callback APIs that are common to all application components ([android.app.Activity](../android/app/Activity.md), [android.app.Service](../android/app/Service.md), [ContentProvider](../android/content/ContentProvider.md), and [android.app.Application](../android/app/Application.md)). |
| [ComponentCallbacks2](../android/content/ComponentCallbacks2.md) | Callbacks for app state transitions that can be used to improve background memory management. |
| [PipeDataWriter](../android/content/ContentProvider.PipeDataWriter.md) | Interface to write a stream of data to a pipe. |
| --- | --- |
| [DialogInterface](../android/content/DialogInterface.md) | Interface that defines a dialog-type class that can be shown, dismissed, or canceled, and may have buttons that can be clicked. |
| [EntityIterator](../android/content/EntityIterator.md) | A specialization of [Iterator](../java/util/Iterator.md) that allows iterating over a collection of [Entity](../android/content/Entity.md) objects. |
| [OnFinished](../android/content/IntentSender.OnFinished.md) | Callback interface for discovering when a send operation has completed. |
| --- | --- |
| [OnLoadCanceledListener](../android/content/Loader.OnLoadCanceledListener.md) | Interface that is implemented to discover when a Loader has been canceled before it finished loading its data. |
| [OnLoadCompleteListener](../android/content/Loader.OnLoadCompleteListener.md) | Interface that is implemented to discover when a Loader has finished loading its data. |
| [ServiceConnection](../android/content/ServiceConnection.md) | Interface for monitoring the state of an application service. |
| --- | --- |
| [SharedPreferences](../android/content/SharedPreferences.md) | Interface for accessing and modifying preference data returned by [android.content.Context#getSharedPreferences](../android/content/Context.md)). |
| [SyncStatusObserver](../android/content/SyncStatusObserver.md) | <br /> |

## Classes

| [AbstractThreadedSyncAdapter](../android/content/AbstractThreadedSyncAdapter.md) | An abstract implementation of a SyncAdapter that spawns a thread to invoke a sync operation. |
| --- | --- |
| [AsyncQueryHandler](../android/content/AsyncQueryHandler.md) | A helper class to help make handling asynchronous [ContentResolver](../android/content/ContentResolver.md) queries easier. |
| [AsyncTaskLoader](../android/content/AsyncTaskLoader.md) | Abstract Loader that provides an [AsyncTask](../android/os/AsyncTask.md) to do the work. |
| [AttributionSource](../android/content/AttributionSource.md) | This class represents a source to which access to permission protected data should be attributed. |
| --- | --- |
| [BroadcastReceiver](../android/content/BroadcastReceiver.md) | Base class for code that receives and handles broadcast intents sent by [android.content.Context#sendBroadcast(Intent)](../android/content/Context.md)). |
| [ClipboardManager](../android/content/ClipboardManager.md) | Interface to the clipboard service, for placing and retrieving text in the global clipboard. |
| [ClipData](../android/content/ClipData.md) | Representation of a clipped data on the clipboard. |
| --- | --- |
| [ClipDescription](../android/content/ClipDescription.md) | Meta-data describing the contents of a [ClipData](../android/content/ClipData.md). |
| [ComponentName](../android/content/ComponentName.md) | Identifier for a specific application component ([android.app.Activity](../android/app/Activity.md), [android.app.Service](../android/app/Service.md), [android.content.BroadcastReceiver](../android/content/BroadcastReceiver.md), or [android.content.ContentProvider](../android/content/ContentProvider.md)) that is available. |
| [ContentProvider](../android/content/ContentProvider.md) | Content providers are one of the primary building blocks of Android applications, providing content to applications. |
| --- | --- |
| [ContentProviderClient](../android/content/ContentProviderClient.md) | The public interface object used to interact with a specific [ContentProvider](../android/content/ContentProvider.md). |
| [ContentProviderOperation](../android/content/ContentProviderOperation.md) | Represents a single operation to be performed as part of a batch of operations. |
| [ContentProviderResult](../android/content/ContentProviderResult.md) | Contains the result of the application of a [ContentProviderOperation](../android/content/ContentProviderOperation.md). |
| --- | --- |
| [ContentQueryMap](../android/content/ContentQueryMap.md) | Caches the contents of a cursor into a Map of String-\>ContentValues and optionally keeps the cache fresh by registering for updates on the content backing the cursor. |
| [ContentResolver](../android/content/ContentResolver.md) | This class provides applications access to the content model. |
| [ContentUris](../android/content/ContentUris.md) | Utility methods useful for working with [android.net.Uri](../android/net/Uri.md) objects that use the "content" (content://) scheme. |
| --- | --- |
| [ContentValues](../android/content/ContentValues.md) | This class is used to store a set of values that the [ContentResolver](../android/content/ContentResolver.md) can process. |
| [Context](../android/content/Context.md) | Interface to global information about an application environment. |
| [ContextParams](../android/content/ContextParams.md) | This class represents rules around how a context being created via [Context.createContext](../android/content/Context.md)) should behave. |
| --- | --- |
| [ContextWrapper](../android/content/ContextWrapper.md) | Proxying implementation of Context that simply delegates all of its calls to another Context. |
| [CursorLoader](../android/content/CursorLoader.md) | A loader that queries the [ContentResolver](../android/content/ContentResolver.md) and returns a [Cursor](../android/database/Cursor.md). |
| [Entity](../android/content/Entity.md) | A representation of a item using ContentValues. |
| --- | --- |
| [Intent](../android/content/Intent.md) | An intent is an abstract description of an operation to be performed. |
| [IntentFilter](../android/content/IntentFilter.md) | Structured description of Intent values to be matched. |
| [IntentSender](../android/content/IntentSender.md) | A description of an Intent and target action to perform with it. |
| --- | --- |
| [Loader](../android/content/Loader.md) | A class that performs asynchronous loading of data. |
| [LocusId](../android/content/LocusId.md) | An identifier for an unique state (locus) in the application. |
| [MutableContextWrapper](../android/content/MutableContextWrapper.md) | Special version of [ContextWrapper](../android/content/ContextWrapper.md) that allows the base context to be modified after it is initially set. |
| --- | --- |
| [PeriodicSync](../android/content/PeriodicSync.md) | Value type that contains information about a periodic sync. |
| [QuickViewConstants](../android/content/QuickViewConstants.md) | Constants for [Intent.ACTION_QUICK_VIEW](../android/content/Intent.md). |
| [RestrictionEntry](../android/content/RestrictionEntry.md) | Applications can expose restrictions for a restricted user on a multiuser device. |
| --- | --- |
| [RestrictionsManager](../android/content/RestrictionsManager.md) | Provides a mechanism for apps to query restrictions imposed by an entity that manages the user. |
| [SearchRecentSuggestionsProvider](../android/content/SearchRecentSuggestionsProvider.md) | This superclass can be used to create a simple search suggestions provider for your application. |
| [SyncAdapterType](../android/content/SyncAdapterType.md) | Value type that represents a SyncAdapterType. |
| --- | --- |
| [SyncContext](../android/content/SyncContext.md) | <br /> |
| [SyncInfo](../android/content/SyncInfo.md) | Information about the sync operation that is currently underway. |
| [SyncRequest](../android/content/SyncRequest.md) | Convenience class to construct sync requests. |
| --- | --- |
| [SyncResult](../android/content/SyncResult.md) | This class is used to communicate the results of a sync operation to the SyncManager. |
| [SyncStats](../android/content/SyncStats.md) | Used to record various statistics about the result of a sync operation. |
| [UriMatcher](../android/content/UriMatcher.md) | Utility class to aid in matching URIs in content providers. |
| --- | --- |
| [UriPermission](../android/content/UriPermission.md) | Description of a single Uri permission grant. |
| [UriRelativeFilter](../android/content/UriRelativeFilter.md) | A filter for matching Intent URI Data as part of a [UriRelativeFilterGroup](../android/content/UriRelativeFilterGroup.md). |
| [UriRelativeFilterGroup](../android/content/UriRelativeFilterGroup.md) | An intent data matching group based on a URI's relative reference which includes the path, query and fragment. |
| --- | --- |

## Exceptions

| [ActivityNotFoundException](../android/content/ActivityNotFoundException.md) | This exception is thrown when a call to android. |
| --- | --- |
| [OperationApplicationException](../android/content/OperationApplicationException.md) | Thrown when an application of a [ContentProviderOperation](../android/content/ContentProviderOperation.md) fails due the specified constraints. |
| [ReceiverCallNotAllowedException](../android/content/ReceiverCallNotAllowedException.md) | This exception is thrown from android. |
