# ContentProvider

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ContentProvider

Kotlin| [Java](https://developer.android.com/reference/android/content/ContentProvider "View this page in Java") 

```
abstract class ContentProvider : ComponentCallbacks2
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.content.ContentProvider](https://developer.android.com/reference/kotlin/android/content/ContentProvider#) |

| Known Direct Subclasses [CloudMediaProvider](https://developer.android.com/reference/kotlin/android/provider/CloudMediaProvider.html#), [DocumentsProvider](https://developer.android.com/reference/kotlin/android/provider/DocumentsProvider.html#), [MockContentProvider](https://developer.android.com/reference/kotlin/android/test/mock/MockContentProvider.html#), [SearchRecentSuggestionsProvider](https://developer.android.com/reference/kotlin/android/content/SearchRecentSuggestionsProvider), [SliceProvider](https://developer.android.com/reference/kotlin/android/app/slice/SliceProvider.html#) |-----------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------| | [CloudMediaProvider](https://developer.android.com/reference/kotlin/android/provider/CloudMediaProvider.html#) | Base class for a cloud media provider. | | [DocumentsProvider](https://developer.android.com/reference/kotlin/android/provider/DocumentsProvider.html#) | Base class for a document provider. | | [MockContentProvider](https://developer.android.com/reference/kotlin/android/test/mock/MockContentProvider.html#) | Mock implementation of ContentProvider. | | [SearchRecentSuggestionsProvider](https://developer.android.com/reference/kotlin/android/content/SearchRecentSuggestionsProvider) | This superclass can be used to create a simple search suggestions provider for your application. | | [SliceProvider](https://developer.android.com/reference/kotlin/android/app/slice/SliceProvider.html#) | A SliceProvider allows an app to provide content to be displayed in system spaces. | |

Content providers are one of the primary building blocks of Android applications, providing content to applications. They encapsulate data and provide it to applications through the single [ContentResolver](https://developer.android.com/reference/kotlin/android/content/ContentResolver) interface. A content provider is only required if you need to share data between multiple applications. For example, the contacts data is used by multiple applications and must be stored in a content provider. If you don't need to share data amongst multiple applications you can use a database directly via [android.database.sqlite.SQLiteDatabase](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase.html#).

When a request is made via a [ContentResolver](https://developer.android.com/reference/kotlin/android/content/ContentResolver) the system inspects the authority of the given URI and passes the request to the content provider registered with the authority. The content provider can interpret the rest of the URI however it wants. The [UriMatcher](https://developer.android.com/reference/kotlin/android/content/UriMatcher) class is helpful for parsing URIs.

The primary methods that need to be implemented are:

- [onCreate](https://developer.android.com/reference/kotlin/android/content/ContentProvider#onCreate())which is called to initialize the provider
- query which returns data to the caller
- insert which inserts new data into the content provider
- update which updates existing data in the content provider
- delete which deletes data from the content provider
- [getType](https://developer.android.com/reference/kotlin/android/content/ContentProvider#getType(android.net.Uri))which returns the MIME type of data in the content provider

<br />

Data access methods (such as #insert and #update) may be called from many threads at once, and must be thread-safe. Other methods (such as [onCreate](https://developer.android.com/reference/kotlin/android/content/ContentProvider#onCreate())) are only called from the application main thread, and must avoid performing lengthy operations. See the method descriptions for their expected thread behavior.

Requests to [ContentResolver](https://developer.android.com/reference/kotlin/android/content/ContentResolver) are automatically forwarded to the appropriate ContentProvider instance, so subclasses don't have to worry about the details of cross-process calls.
|
| ### Developer Guides
|
| For more information about using content providers, read the [Content Providers](https://developer.android.com/guide/topics/providers/content-providers.html) developer guide.

## Summary

| Nested classes ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [CallingIdentity](https://developer.android.com/reference/kotlin/android/content/ContentProvider.CallingIdentity) Opaque token representing the identity of an incoming IPC. |
| abstract | [PipeDataWriter](https://developer.android.com/reference/kotlin/android/content/ContentProvider.PipeDataWriter) Interface to write a stream of data to a pipe. |

| Inherited constants ||
|---|---|
| From class [ComponentCallbacks2](https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2) |----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TRIM_MEMORY_BACKGROUND](https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2#TRIM_MEMORY_BACKGROUND:kotlin.Int) <br /> Level for [onTrimMemory(int)](https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2#onTrimMemory(kotlin.Int)): the process has gone on to the LRU list. This is a good opportunity to clean up resources that can efficiently and quickly be re-built if the user returns to the app. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TRIM_MEMORY_COMPLETE](https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2#TRIM_MEMORY_COMPLETE:kotlin.Int) <br /> Level for [onTrimMemory(int)](https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2#onTrimMemory(kotlin.Int)): the process is nearing the end of the background LRU list, and if more memory isn't found soon it will be killed. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TRIM_MEMORY_MODERATE](https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2#TRIM_MEMORY_MODERATE:kotlin.Int) <br /> Level for [onTrimMemory(int)](https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2#onTrimMemory(kotlin.Int)): the process is around the middle of the background LRU list; freeing memory can help the system keep other processes running later in the list for better overall performance. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TRIM_MEMORY_RUNNING_CRITICAL](https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2#TRIM_MEMORY_RUNNING_CRITICAL:kotlin.Int) <br /> Level for [onTrimMemory(int)](https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2#onTrimMemory(kotlin.Int)): the process is not an expendable background process, but the device is running extremely low on memory and is about to not be able to keep any background processes running. Your running process should free up as many non-critical resources as it can to allow that memory to be used elsewhere. The next thing that will happen after this is [onLowMemory()](https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks#onLowMemory())called to report that nothing at all can be kept in the background, a situation that can start to notably impact the user. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TRIM_MEMORY_RUNNING_LOW](https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2#TRIM_MEMORY_RUNNING_LOW:kotlin.Int) <br /> Level for [onTrimMemory(int)](https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2#onTrimMemory(kotlin.Int)): the process is not an expendable background process, but the device is running low on memory. Your running process should free up unneeded resources to allow that memory to be used elsewhere. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TRIM_MEMORY_RUNNING_MODERATE](https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2#TRIM_MEMORY_RUNNING_MODERATE:kotlin.Int) <br /> Level for [onTrimMemory(int)](https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2#onTrimMemory(kotlin.Int)): the process is not an expendable background process, but the device is running moderately low on memory. Your running process may want to release some unneeded resources for use elsewhere. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TRIM_MEMORY_UI_HIDDEN](https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2#TRIM_MEMORY_UI_HIDDEN:kotlin.Int) <br /> Level for [onTrimMemory(int)](https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2#onTrimMemory(kotlin.Int)): the process had been showing a user interface, and is no longer doing so. Large allocations with the UI should be released at this point to allow memory to be better managed. <br /> | ||

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ContentProvider](https://developer.android.com/reference/kotlin/android/content/ContentProvider#ContentProvider())`()` Construct a ContentProvider instance. |

| Public methods ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [ContentProviderResult](https://developer.android.com/reference/kotlin/android/content/ContentProviderResult)!\> | [applyBatch](https://developer.android.com/reference/kotlin/android/content/ContentProvider#applyBatch(kotlin.String,%20java.util.ArrayList))`(`authority:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `operations:` ` [ArrayList](https://developer.android.com/reference/kotlin/java/util/ArrayList.html#)< [ContentProviderOperation](https://developer.android.com/reference/kotlin/android/content/ContentProviderOperation)!>`)` Override this to handle requests to perform a batch of operations, or the default implementation will iterate over the operations and call [ContentProviderOperation.apply](https://developer.android.com/reference/kotlin/android/content/ContentProviderOperation#apply(android.content.ContentProvider,%20kotlin.Array,%20kotlin.Int))on each of them. |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [ContentProviderResult](https://developer.android.com/reference/kotlin/android/content/ContentProviderResult)!\> | [applyBatch](https://developer.android.com/reference/kotlin/android/content/ContentProvider#applyBatch(java.util.ArrayList))`(`operations:` ` [ArrayList](https://developer.android.com/reference/kotlin/java/util/ArrayList.html#)< [ContentProviderOperation](https://developer.android.com/reference/kotlin/android/content/ContentProviderOperation)!>`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [attachInfo](https://developer.android.com/reference/kotlin/android/content/ContentProvider#attachInfo(android.content.Context,%20android.content.pm.ProviderInfo))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context)!`, `info:` ` [ProviderInfo](https://developer.android.com/reference/kotlin/android/content/pm/ProviderInfo)!`)` After being instantiated, this is called to tell the content provider about itself. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [bulkInsert](https://developer.android.com/reference/kotlin/android/content/ContentProvider#bulkInsert(android.net.Uri,%20kotlin.Array))`(`uri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)`, `values:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [ContentValues](https://developer.android.com/reference/kotlin/android/content/ContentValues)!>`)` Override this to handle requests to insert a set of new rows, or the default implementation will iterate over the values and call #insert on each of them. |
| open [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)? | [call](https://developer.android.com/reference/kotlin/android/content/ContentProvider#call(kotlin.String,%20kotlin.String,%20android.os.Bundle))`(`method:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `arg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `extras:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)?`)` <br /> |
| open [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)? | [call](https://developer.android.com/reference/kotlin/android/content/ContentProvider#call(kotlin.String,%20kotlin.String,%20kotlin.String,%20android.os.Bundle))`(`authority:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `method:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `arg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `extras:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)?`)` Call a provider-defined method. |
| open [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)? | [canonicalize](https://developer.android.com/reference/kotlin/android/content/ContentProvider#canonicalize(android.net.Uri))`(`url:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)`)` Implement this to support canonicalization of URIs that refer to your content provider. |
| [ContentProvider.CallingIdentity](https://developer.android.com/reference/kotlin/android/content/ContentProvider.CallingIdentity) | [clearCallingIdentity](https://developer.android.com/reference/kotlin/android/content/ContentProvider#clearCallingIdentity())`()` Reset the identity of the incoming IPC on the current thread. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [delete](https://developer.android.com/reference/kotlin/android/content/ContentProvider#delete(android.net.Uri,%20android.os.Bundle))`(`uri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)`, `extras:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)?`)` Implement this to handle requests to delete one or more rows. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [delete](https://developer.android.com/reference/kotlin/android/content/ContentProvider#delete(android.net.Uri,%20kotlin.String,%20kotlin.Array))`(`uri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)`, `selection:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `selectionArgs:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>?`)` Implement this to handle requests to delete one or more rows. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [dump](https://developer.android.com/reference/kotlin/android/content/ContentProvider#dump(java.io.FileDescriptor,%20java.io.PrintWriter,%20kotlin.Array))`(`fd:` ` [FileDescriptor](https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#)!`, `writer:` ` [PrintWriter](https://developer.android.com/reference/kotlin/java/io/PrintWriter.html#)!`, `args:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`)` Print the Provider's state into the given stream. |
| [AttributionSource](https://developer.android.com/reference/kotlin/android/content/AttributionSource)? | [getCallingAttributionSource](https://developer.android.com/reference/kotlin/android/content/ContentProvider#getCallingAttributionSource())`()` Gets the attribution source of the calling app. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getCallingAttributionTag](https://developer.android.com/reference/kotlin/android/content/ContentProvider#getCallingAttributionTag())`()` Return the attribution tag of the caller that initiated the request being processed on the current thread. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getCallingPackage](https://developer.android.com/reference/kotlin/android/content/ContentProvider#getCallingPackage())`()` Return the package name of the caller that initiated the request being processed on the current thread. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getCallingPackageUnchecked](https://developer.android.com/reference/kotlin/android/content/ContentProvider#getCallingPackageUnchecked())`()` Return the package name of the caller that initiated the request being processed on the current thread. |
| [Context](https://developer.android.com/reference/kotlin/android/content/Context)? | [getContext](https://developer.android.com/reference/kotlin/android/content/ContentProvider#getContext())`()` Retrieves the Context this provider is running in. |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [PathPermission](https://developer.android.com/reference/kotlin/android/content/pm/PathPermission)!\>? | [getPathPermissions](https://developer.android.com/reference/kotlin/android/content/ContentProvider#getPathPermissions())`()` Return the path-based permissions required for read and/or write access to this content provider. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getReadPermission](https://developer.android.com/reference/kotlin/android/content/ContentProvider#getReadPermission())`()` Return the name of the permission required for read-only access to this content provider. |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>? | [getStreamTypes](https://developer.android.com/reference/kotlin/android/content/ContentProvider#getStreamTypes(android.net.Uri,%20kotlin.String))`(`uri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)`, `mimeTypeFilter:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Called by a client to determine the types of data streams that this content provider supports for the given URI. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getType](https://developer.android.com/reference/kotlin/android/content/ContentProvider#getType(android.net.Uri))`(`uri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)`)` Implement this to handle requests for the MIME type of the data at the given URI. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getTypeAnonymous](https://developer.android.com/reference/kotlin/android/content/ContentProvider#getTypeAnonymous(android.net.Uri))`(`uri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)`)` Implement this to handle requests for MIME type of URIs, that does not need to reveal any internal information which should be protected by any permission. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getWritePermission](https://developer.android.com/reference/kotlin/android/content/ContentProvider#getWritePermission())`()` Return the name of the permission required for read/write access to this content provider. |
| abstract [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)? | [insert](https://developer.android.com/reference/kotlin/android/content/ContentProvider#insert(android.net.Uri,%20android.content.ContentValues))`(`uri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)`, `values:` ` [ContentValues](https://developer.android.com/reference/kotlin/android/content/ContentValues)?`)` Implement this to handle requests to insert a new row. |
| open [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)? | [insert](https://developer.android.com/reference/kotlin/android/content/ContentProvider#insert(android.net.Uri,%20android.content.ContentValues,%20android.os.Bundle))`(`uri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)`, `values:` ` [ContentValues](https://developer.android.com/reference/kotlin/android/content/ContentValues)?`, `extras:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)?`)` Implement this to handle requests to insert a new row. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onCallingPackageChanged](https://developer.android.com/reference/kotlin/android/content/ContentProvider#onCallingPackageChanged())`()` Called whenever the value of [getCallingPackage()](https://developer.android.com/reference/kotlin/android/content/ContentProvider#getCallingPackage())changes, giving the provider an opportunity to invalidate any security related caching it may be performing. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onConfigurationChanged](https://developer.android.com/reference/kotlin/android/content/ContentProvider#onConfigurationChanged(android.content.res.Configuration))`(`newConfig:` ` [Configuration](https://developer.android.com/reference/kotlin/android/content/res/Configuration)`)` Called by the system when the device configuration changes while your component is running. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onCreate](https://developer.android.com/reference/kotlin/android/content/ContentProvider#onCreate())`()` Implement this to initialize your content provider on startup. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onLowMemory](https://developer.android.com/reference/kotlin/android/content/ContentProvider#onLowMemory())`()` This is called when the overall system is running low on memory, and actively running processes should trim their memory usage. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onTrimMemory](https://developer.android.com/reference/kotlin/android/content/ContentProvider#onTrimMemory(kotlin.Int))`(`level:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [AssetFileDescriptor](https://developer.android.com/reference/kotlin/android/content/res/AssetFileDescriptor)? | [openAssetFile](https://developer.android.com/reference/kotlin/android/content/ContentProvider#openAssetFile(android.net.Uri,%20kotlin.String))`(`uri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)`, `mode:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` This is like #openFile, but can be implemented by providers that need to be able to return sub-sections of files, often assets inside of their . |
| open [AssetFileDescriptor](https://developer.android.com/reference/kotlin/android/content/res/AssetFileDescriptor)? | [openAssetFile](https://developer.android.com/reference/kotlin/android/content/ContentProvider#openAssetFile(android.net.Uri,%20kotlin.String,%20android.os.CancellationSignal))`(`uri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)`, `mode:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `signal:` ` [CancellationSignal](https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#)?`)` This is like #openFile, but can be implemented by providers that need to be able to return sub-sections of files, often assets inside of their . |
| open [ParcelFileDescriptor](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#)? | [openFile](https://developer.android.com/reference/kotlin/android/content/ContentProvider#openFile(android.net.Uri,%20kotlin.String))`(`uri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)`, `mode:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Override this to handle requests to open a file blob. |
| open [ParcelFileDescriptor](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#)? | [openFile](https://developer.android.com/reference/kotlin/android/content/ContentProvider#openFile(android.net.Uri,%20kotlin.String,%20android.os.CancellationSignal))`(`uri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)`, `mode:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `signal:` ` [CancellationSignal](https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#)?`)` Override this to handle requests to open a file blob. |
| open [ParcelFileDescriptor](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#) | [openPipeHelper](https://developer.android.com/reference/kotlin/android/content/ContentProvider#openPipeHelper(android.net.Uri,%20kotlin.String,%20android.os.Bundle,%20android.content.ContentProvider.openPipeHelper.T,%20android.content.ContentProvider.PipeDataWriter))`(`uri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)`, `mimeType:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `opts:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)?`, `args:` `T?`, `func:` ` [ContentProvider.PipeDataWriter](https://developer.android.com/reference/kotlin/android/content/ContentProvider.PipeDataWriter)<T>`)` A helper function for implementing #openTypedAssetFile, for creating a data pipe and background thread allowing you to stream generated data back to the client. |
| open [AssetFileDescriptor](https://developer.android.com/reference/kotlin/android/content/res/AssetFileDescriptor)? | [openTypedAssetFile](https://developer.android.com/reference/kotlin/android/content/ContentProvider#openTypedAssetFile(android.net.Uri,%20kotlin.String,%20android.os.Bundle))`(`uri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)`, `mimeTypeFilter:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `opts:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)?`)` Called by a client to open a read-only stream containing data of a particular MIME type. |
| open [AssetFileDescriptor](https://developer.android.com/reference/kotlin/android/content/res/AssetFileDescriptor)? | [openTypedAssetFile](https://developer.android.com/reference/kotlin/android/content/ContentProvider#openTypedAssetFile(android.net.Uri,%20kotlin.String,%20android.os.Bundle,%20android.os.CancellationSignal))`(`uri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)`, `mimeTypeFilter:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `opts:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)?`, `signal:` ` [CancellationSignal](https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#)?`)` Called by a client to open a read-only stream containing data of a particular MIME type. |
| open [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#)? | [query](https://developer.android.com/reference/kotlin/android/content/ContentProvider#query(android.net.Uri,%20kotlin.Array,%20android.os.Bundle,%20android.os.CancellationSignal))`(`uri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)`, `projection:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>?`, `queryArgs:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)?`, `cancellationSignal:` ` [CancellationSignal](https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#)?`)` Implement this to handle query requests where the arguments are packed into a [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#). |
| abstract [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#)? | [query](https://developer.android.com/reference/kotlin/android/content/ContentProvider#query(android.net.Uri,%20kotlin.Array,%20kotlin.String,%20kotlin.Array,%20kotlin.String))`(`uri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)`, `projection:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>?`, `selection:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `selectionArgs:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>?`, `sortOrder:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` Implement this to handle query requests from clients. |
| open [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#)? | [query](https://developer.android.com/reference/kotlin/android/content/ContentProvider#query(android.net.Uri,%20kotlin.Array,%20kotlin.String,%20kotlin.Array,%20kotlin.String,%20android.os.CancellationSignal))`(`uri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)`, `projection:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>?`, `selection:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `selectionArgs:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>?`, `sortOrder:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `cancellationSignal:` ` [CancellationSignal](https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#)?`)` Implement this to handle query requests from clients with support for cancellation. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [refresh](https://developer.android.com/reference/kotlin/android/content/ContentProvider#refresh(android.net.Uri,%20android.os.Bundle,%20android.os.CancellationSignal))`(`uri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)!`, `extras:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)?`, `cancellationSignal:` ` [CancellationSignal](https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#)?`)` Implement this to support refresh of content identified by`uri`. |
| [Context](https://developer.android.com/reference/kotlin/android/content/Context) | [requireContext](https://developer.android.com/reference/kotlin/android/content/ContentProvider#requireContext())`()` Retrieves a Non-Nullable Context this provider is running in, this is intended to be called after [onCreate](https://developer.android.com/reference/kotlin/android/content/ContentProvider#onCreate()). |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [restoreCallingIdentity](https://developer.android.com/reference/kotlin/android/content/ContentProvider#restoreCallingIdentity(android.content.ContentProvider.CallingIdentity))`(`identity:` ` [ContentProvider.CallingIdentity](https://developer.android.com/reference/kotlin/android/content/ContentProvider.CallingIdentity)`)` Restore the identity of the incoming IPC on the current thread back to a previously identity that was returned by [clearCallingIdentity](https://developer.android.com/reference/kotlin/android/content/ContentProvider#clearCallingIdentity()). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [shutdown](https://developer.android.com/reference/kotlin/android/content/ContentProvider#shutdown())`()` Implement this to shut down the ContentProvider instance. |
| open [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)? | [uncanonicalize](https://developer.android.com/reference/kotlin/android/content/ContentProvider#uncanonicalize(android.net.Uri))`(`url:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)`)` Remove canonicalization from canonical URIs previously returned by [canonicalize](https://developer.android.com/reference/kotlin/android/content/ContentProvider#canonicalize(android.net.Uri)). |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [update](https://developer.android.com/reference/kotlin/android/content/ContentProvider#update(android.net.Uri,%20android.content.ContentValues,%20android.os.Bundle))`(`uri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)`, `values:` ` [ContentValues](https://developer.android.com/reference/kotlin/android/content/ContentValues)?`, `extras:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)?`)` Implement this to handle requests to update one or more rows. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [update](https://developer.android.com/reference/kotlin/android/content/ContentProvider#update(android.net.Uri,%20android.content.ContentValues,%20kotlin.String,%20kotlin.Array))`(`uri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)`, `values:` ` [ContentValues](https://developer.android.com/reference/kotlin/android/content/ContentValues)?`, `selection:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `selectionArgs:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>?`)` Implement this to handle requests to update one or more rows. |

| Protected methods ||
|--------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isTemporary](https://developer.android.com/reference/kotlin/android/content/ContentProvider#isTemporary())`()` Returns true if this instance is a temporary content provider. |
| [ParcelFileDescriptor](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#) | [openFileHelper](https://developer.android.com/reference/kotlin/android/content/ContentProvider#openFileHelper(android.net.Uri,%20kotlin.String))`(`uri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)`, `mode:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Convenience for subclasses that wish to implement #openFile by looking up a column named "_data" at the given URI. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPathPermissions](https://developer.android.com/reference/kotlin/android/content/ContentProvider#setPathPermissions(kotlin.Array))`(`permissions:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [PathPermission](https://developer.android.com/reference/kotlin/android/content/pm/PathPermission)!>?`)` Change the path-based permission required to read and/or write data in the content provider. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setReadPermission](https://developer.android.com/reference/kotlin/android/content/ContentProvider#setReadPermission(kotlin.String))`(`permission:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` Change the permission required to read data from the content provider. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setWritePermission](https://developer.android.com/reference/kotlin/android/content/ContentProvider#setWritePermission(kotlin.String))`(`permission:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` Change the permission required to read and write data in the content provider. |

| Inherited functions ||
|---|---|
| From class [ComponentCallbacks](https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks) |------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onConfigurationChanged](https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks#onConfigurationChanged(android.content.res.Configuration))`(`newConfig:` ` [Configuration](https://developer.android.com/reference/kotlin/android/content/res/Configuration)`)` <br /> Called by the system when the device configuration changes while your component is running. Note that, unlike activities, other components are never restarted when a configuration changes: they must always deal with the results of the change, such as by re-retrieving resources. At the time that this function has been called, your Resources object will have been updated to return resource values matching the new configuration. For more information, read [Handling Runtime Changes](https://developer.android.com/guide/topics/resources/runtime-changes.html). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onLowMemory](https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks#onLowMemory())`()` <br /> This is called when the overall system is running low on memory, and actively running processes should trim their memory usage. While the exact point at which this will be called is not defined, generally it will happen when all background process have been killed. That is, before reaching the point of killing processes hosting service and foreground UI that we would like to avoid killing. <br /> | ||

## Public constructors

### ContentProvider

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ContentProvider()
```

Construct a ContentProvider instance. Content providers must be [declared in the manifest](https://developer.android.com/guide/topics/manifest/provider-element.html), accessed with [ContentResolver](https://developer.android.com/reference/kotlin/android/content/ContentResolver), and created automatically by the system, so applications usually do not create ContentProvider instances directly.

At construction time, the object is uninitialized, and most fields and methods are unavailable. Subclasses should initialize themselves in [onCreate](https://developer.android.com/reference/kotlin/android/content/ContentProvider#onCreate()), not the constructor.

Content providers are created on the application main thread at application launch time. The constructor must not perform lengthy operations, or application startup will be delayed.

## Public methods

### applyBatch

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun applyBatch(
    authority: String, 
    operations: ArrayList<ContentProviderOperation!>
): Array<ContentProviderResult!>
```

Override this to handle requests to perform a batch of operations, or the default implementation will iterate over the operations and call [ContentProviderOperation.apply](https://developer.android.com/reference/kotlin/android/content/ContentProviderOperation#apply(android.content.ContentProvider,%20kotlin.Array,%20kotlin.Int))on each of them. If all calls to [ContentProviderOperation.apply](https://developer.android.com/reference/kotlin/android/content/ContentProviderOperation#apply(android.content.ContentProvider,%20kotlin.Array,%20kotlin.Int))succeed then a [ContentProviderResult](https://developer.android.com/reference/kotlin/android/content/ContentProviderResult) array with as many elements as there were operations will be returned. If any of the calls fail, it is up to the implementation how many of the others take effect. This method can be called from multiple threads, as described in [Processes and Threads](https://developer.android.com/guide/topics/fundamentals/processes-and-threads.html#Threads).

| Parameters ||
|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `operations` | [ArrayList](https://developer.android.com/reference/kotlin/java/util/ArrayList.html#)\< [ContentProviderOperation](https://developer.android.com/reference/kotlin/android/content/ContentProviderOperation)!\>:the operations to apply This value cannot be`null`. |
| `authority` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [ContentProviderResult](https://developer.android.com/reference/kotlin/android/content/ContentProviderResult)!> | the results of the applications This value cannot be`null`. |

| Exceptions ||
|-------------------------------------------------|--------------------------------|
| `android.content.OperationApplicationException` | thrown if any operation fails. |

**See Also**

- [android.content.ContentProviderOperation#apply](https://developer.android.com/reference/kotlin/android/content/ContentProviderOperation#apply(android.content.ContentProvider,%20kotlin.Array,%20kotlin.Int)) 

### applyBatch

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun applyBatch(operations: ArrayList<ContentProviderOperation!>): Array<ContentProviderResult!>
```

| Parameters ||
|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `operations` | [ArrayList](https://developer.android.com/reference/kotlin/java/util/ArrayList.html#)\< [ContentProviderOperation](https://developer.android.com/reference/kotlin/android/content/ContentProviderOperation)!\>:This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [ContentProviderResult](https://developer.android.com/reference/kotlin/android/content/ContentProviderResult)!> | This value cannot be`null`. |

### attachInfo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun attachInfo(
    context: Context!, 
    info: ProviderInfo!
): Unit
```

After being instantiated, this is called to tell the content provider about itself.

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context)!:The context this provider is running in |
| `info` | [ProviderInfo](https://developer.android.com/reference/kotlin/android/content/pm/ProviderInfo)!:Registered information about this content provider |

### bulkInsert

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun bulkInsert(
    uri: Uri, 
    values: Array<ContentValues!>
): Int
```

Override this to handle requests to insert a set of new rows, or the default implementation will iterate over the values and call #insert on each of them. As a courtesy, call [notifyChange()](https://developer.android.com/reference/kotlin/android/content/ContentResolver#notifyChange(android.net.Uri,%20android.database.ContentObserver))after inserting. This method can be called from multiple threads, as described in [Processes and Threads](https://developer.android.com/guide/topics/fundamentals/processes-and-threads.html#Threads).

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `uri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#):The content:// URI of the insertion request. This value cannot be`null`. |
| `values` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [ContentValues](https://developer.android.com/reference/kotlin/android/content/ContentValues)!\>:An array of sets of column_name/value pairs to add to the database. This must not be`null`. |

| Return ||
|----------------------------------------------------------------------------|------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The number of values that were inserted. |

### call

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun call(
    method: String, 
    arg: String?, 
    extras: Bundle?
): Bundle?
```

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------|
| `method` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):This value cannot be`null`. |
| `arg` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:This value may be`null`. |
| `extras` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)?:This value may be`null`. |

| Return ||
|-----------------------------------------------------------------------------------|--------------------------|
| [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)? | This value may be`null`. |

### call

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun call(
    authority: String, 
    method: String, 
    arg: String?, 
    extras: Bundle?
): Bundle?
```

Call a provider-defined method. This can be used to implement interfaces that are cheaper and/or unnatural for a table-like model.

**WARNING:** The framework does no permission checking on this entry into the content provider besides the basic ability for the application to get access to the provider at all. For example, it has no idea whether the call being executed may read or write data in the provider, so can't enforce those individual permissions. Any implementation of this method**must**do its own permission checks on incoming calls to make sure they are allowed.

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| `method` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):method name to call. Opaque to framework, but should not be`null`. |
| `arg` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:provider-defined String argument. May be`null`. |
| `extras` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)?:provider-defined Bundle argument. May be`null`. |
| `authority` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):This value cannot be`null`. |

| Return ||
|-----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)? | provider-defined return value. May be`null`, which is also the default for providers which don't implement any call methods. |

### canonicalize

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun canonicalize(url: Uri): Uri?
```

Implement this to support canonicalization of URIs that refer to your content provider. A canonical URI is one that can be transported across devices, backup/restore, and other contexts, and still be able to refer to the same data item. Typically this is implemented by adding query params to the URI allowing the content provider to verify that an incoming canonical URI references the same data as it was originally intended for and, if it doesn't, to find that data (if it exists) in the current environment.

For example, if the content provider holds people and a normal URI in it is created with a row index into that people database, the cananical representation may have an additional query param at the end which specifies the name of the person it is intended for. Later calls into the provider with that URI will look up the row of that URI's base index and, if it doesn't match or its entry's name doesn't match the name in the query param, perform a query on its database to find the correct row to operate on.

If you implement support for canonical URIs,**all** incoming calls with URIs (including this one) must perform this verification and recovery of any canonical URIs they receive. In addition, you must also implement [uncanonicalize](https://developer.android.com/reference/kotlin/android/content/ContentProvider#uncanonicalize(android.net.Uri))to strip the canonicalization of any of these URIs.

The default implementation of this method returns null, indicating that canonical URIs are not supported.

| Parameters ||
|-------|----------------------------------------------------------------------------------------------------------------------------------|
| `url` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#):The Uri to canonicalize. This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)? | Return the canonical representation of url, or null if canonicalization of that Uri is not supported. |

### clearCallingIdentity

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun clearCallingIdentity(): ContentProvider.CallingIdentity
```

Reset the identity of the incoming IPC on the current thread.

Internally this calls [Binder.clearCallingIdentity()](https://developer.android.com/reference/kotlin/android/os/Binder.html#clearCallingIdentity())and also clears any value stored in [getCallingPackage()](https://developer.android.com/reference/kotlin/android/content/ContentProvider#getCallingPackage()).

| Return ||
|-----------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ContentProvider.CallingIdentity](https://developer.android.com/reference/kotlin/android/content/ContentProvider.CallingIdentity) | Returns an opaque token that can be used to restore the original calling identity by passing it to [restoreCallingIdentity](https://developer.android.com/reference/kotlin/android/content/ContentProvider#restoreCallingIdentity(android.content.ContentProvider.CallingIdentity)). This value cannot be`null`. |

### delete

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun delete(
    uri: Uri, 
    extras: Bundle?
): Int
```

Implement this to handle requests to delete one or more rows. The implementation should apply the selection clause when performing deletion, allowing the operation to affect multiple rows in a directory. As a courtesy, call [notifyChange()](https://developer.android.com/reference/kotlin/android/content/ContentResolver#notifyChange(android.net.Uri,%20android.database.ContentObserver))after deleting. This method can be called from multiple threads, as described in [Processes and Threads](https://developer.android.com/guide/topics/fundamentals/processes-and-threads.html#Threads).

The implementation is responsible for parsing out a row ID at the end of the URI, if a specific row is being deleted. That is, the client would pass in`content://contacts/people/22`and the implementation is responsible for parsing the record number (22) when creating a SQL statement.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `uri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#):The full URI to query, including a row ID (if a specific record is requested). This value cannot be`null`. |
| `extras` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)?:A Bundle containing additional information necessary for the operation. Arguments may include SQL style arguments, such as [ContentResolver.QUERY_ARG_SQL_LIMIT](https://developer.android.com/reference/kotlin/android/content/ContentResolver#QUERY_ARG_SQL_LIMIT:kotlin.String), but note that the documentation for each individual provider will indicate which arguments they support. This value may be`null`. |

| Exceptions ||
|--------------------------------------|------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the provider doesn't support one of the requested Bundle arguments. |
| `android.database.SQLException` | |

### delete

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun delete(
    uri: Uri, 
    selection: String?, 
    selectionArgs: Array<String!>?
): Int
```

Implement this to handle requests to delete one or more rows. The implementation should apply the selection clause when performing deletion, allowing the operation to affect multiple rows in a directory. As a courtesy, call [notifyChange()](https://developer.android.com/reference/kotlin/android/content/ContentResolver#notifyChange(android.net.Uri,%20android.database.ContentObserver))after deleting. This method can be called from multiple threads, as described in [Processes and Threads](https://developer.android.com/guide/topics/fundamentals/processes-and-threads.html#Threads).

The implementation is responsible for parsing out a row ID at the end of the URI, if a specific row is being deleted. That is, the client would pass in`content://contacts/people/22`and the implementation is responsible for parsing the record number (22) when creating a SQL statement.

| Parameters ||
|-----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `uri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#):The full URI to query, including a row ID (if a specific record is requested). This value cannot be`null`. |
| `selection` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:An optional restriction to apply to rows when deleting. This value may be`null`. |
| `selectionArgs` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>?:This value may be`null`. |

| Return ||
|----------------------------------------------------------------------------|------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The number of rows affected. |

| Exceptions ||
|---------------------------------|---|
| `android.database.SQLException` | |

### dump

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun dump(
    fd: FileDescriptor!, 
    writer: PrintWriter!, 
    args: Array<String!>!
): Unit
```

Print the Provider's state into the given stream. This gets invoked if you run "adb shell dumpsys activity provider \<provider_component_name\>".

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `fd` | [FileDescriptor](https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#)!:The raw file descriptor that the dump is being sent to. |
| `writer` | [PrintWriter](https://developer.android.com/reference/kotlin/java/io/PrintWriter.html#)!:The PrintWriter to which you should dump your state. This will be closed for you after you return. |
| `args` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!:additional arguments to the dump request. |

### getCallingAttributionSource

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCallingAttributionSource(): AttributionSource?
```

Gets the attribution source of the calling app. If you want to attribute the data access to the calling app you can create an attribution context via [android.content.Context#createContext(ContextParams)](https://developer.android.com/reference/kotlin/android/content/Context#createContext(android.content.ContextParams))and passing this identity to [ContextParams.Builder.setNextAttributionSource(](https://developer.android.com/reference/kotlin/android/content/ContextParams.Builder#setNextAttributionSource(android.content.AttributionSource)).

| Return ||
|--------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| [AttributionSource](https://developer.android.com/reference/kotlin/android/content/AttributionSource)? | The identity of the caller for permission purposes. This value may be`null`. |

**See Also**

- [android.content.ContextParams.Builder#setNextAttributionSource(AttributionSource)](https://developer.android.com/reference/kotlin/android/content/ContextParams.Builder#setNextAttributionSource(android.content.AttributionSource))
- [android.content.AttributionSource](https://developer.android.com/reference/kotlin/android/content/AttributionSource) 

### getCallingAttributionTag

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCallingAttributionTag(): String?
```

Return the attribution tag of the caller that initiated the request being processed on the current thread. Returns`null`if not currently processing a request of the request is for the default attribution.

This will always return`null`when processing [getTypeAnonymous(android.net.Uri)](https://developer.android.com/reference/kotlin/android/content/ContentProvider#getTypeAnonymous(android.net.Uri))requests For [getType(android.net.Uri)](https://developer.android.com/reference/kotlin/android/content/ContentProvider#getType(android.net.Uri))requests, this will be only available for cases, where the caller can be identified. See [getTypeAnonymous(android.net.Uri)](https://developer.android.com/reference/kotlin/android/content/ContentProvider#getTypeAnonymous(android.net.Uri)) 
**See Also**

- [#getCallingPackage](https://developer.android.com/reference/kotlin/android/content/ContentProvider#getCallingPackage()) 

### getCallingPackage

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCallingPackage(): String?
```

Return the package name of the caller that initiated the request being processed on the current thread. The returned package will have been verified to belong to the calling UID. Returns`null`if not currently processing a request.

This will always return`null`when processing [getTypeAnonymous(android.net.Uri)](https://developer.android.com/reference/kotlin/android/content/ContentProvider#getTypeAnonymous(android.net.Uri))requests For [getType(android.net.Uri)](https://developer.android.com/reference/kotlin/android/content/ContentProvider#getType(android.net.Uri))requests, this will be only available for cases, where the caller can be identified. See [getTypeAnonymous(android.net.Uri)](https://developer.android.com/reference/kotlin/android/content/ContentProvider#getTypeAnonymous(android.net.Uri))

| Exceptions ||
|-------------------------------|-----------------------------------------------------------|
| `java.lang.SecurityException` | if the calling package doesn't belong to the calling UID. |

**See Also**

- [android.os.Binder#getCallingUid()](https://developer.android.com/reference/kotlin/android/os/Binder.html#getCallingUid())
- [android.content.Context#grantUriPermission(String, Uri, int)](https://developer.android.com/reference/kotlin/android/content/Context#grantUriPermission(kotlin.String,%20android.net.Uri,%20kotlin.Int)) 

### getCallingPackageUnchecked

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCallingPackageUnchecked(): String?
```

Return the package name of the caller that initiated the request being processed on the current thread. The returned package will have*not* been verified to belong to the calling UID. Returns`null`if not currently processing a request.

This will always return`null`when processing [getTypeAnonymous(android.net.Uri)](https://developer.android.com/reference/kotlin/android/content/ContentProvider#getTypeAnonymous(android.net.Uri))requests For [getType(android.net.Uri)](https://developer.android.com/reference/kotlin/android/content/ContentProvider#getType(android.net.Uri))requests, this will be only available for cases, where the caller can be identified. See [getTypeAnonymous(android.net.Uri)](https://developer.android.com/reference/kotlin/android/content/ContentProvider#getTypeAnonymous(android.net.Uri)) 
**See Also**

- [android.os.Binder#getCallingUid()](https://developer.android.com/reference/kotlin/android/os/Binder.html#getCallingUid())
- [android.content.Context#grantUriPermission(String, Uri, int)](https://developer.android.com/reference/kotlin/android/content/Context#grantUriPermission(kotlin.String,%20android.net.Uri,%20kotlin.Int)) 

### getContext

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getContext(): Context?
```

Retrieves the Context this provider is running in. Only available once [onCreate](https://developer.android.com/reference/kotlin/android/content/ContentProvider#onCreate())has been called -- this will return`null`in the constructor. 

### getPathPermissions

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPathPermissions(): Array<PathPermission!>?
```

Return the path-based permissions required for read and/or write access to this content provider. This method can be called from multiple threads, as described in [Processes and Threads](https://developer.android.com/guide/topics/fundamentals/processes-and-threads.html#Threads).

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [PathPermission](https://developer.android.com/reference/kotlin/android/content/pm/PathPermission)!>? | This value may be`null`. |

### getReadPermission

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getReadPermission(): String?
```

Return the name of the permission required for read-only access to this content provider. This method can be called from multiple threads, as described in [Processes and Threads](https://developer.android.com/guide/topics/fundamentals/processes-and-threads.html#Threads).

| Return ||
|-----------------------------------------------------------------------------------|--------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | This value may be`null`. |

### getStreamTypes

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getStreamTypes(
    uri: Uri, 
    mimeTypeFilter: String
): Array<String!>?
```

Called by a client to determine the types of data streams that this content provider supports for the given URI. The default implementation returns`null`, meaning no types. If your content provider stores data of a particular type, return that MIME type if it matches the given mimeTypeFilter. If it can perform type conversions, return an array of all supported MIME types that match mimeTypeFilter.

| Parameters ||
|------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `uri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#):The data in the content provider being queried. This value cannot be`null`. |
| `mimeTypeFilter` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The type of data the client desires. May be a pattern, such as \*/\* to retrieve all possible data types. This value cannot be`null`. |

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>? | Returns`null`if there are no possible data streams for the given mimeTypeFilter. Otherwise returns an array of all available concrete MIME types. |

**See Also**

- [#getType(Uri)](https://developer.android.com/reference/kotlin/android/content/ContentProvider#getType(android.net.Uri))
- [#openTypedAssetFile(Uri, String, Bundle)](https://developer.android.com/reference/kotlin/android/content/ContentProvider#openTypedAssetFile(android.net.Uri,%20kotlin.String,%20android.os.Bundle))
- [android.content.ClipDescription#compareMimeTypes(String, String)](https://developer.android.com/reference/kotlin/android/content/ClipDescription#compareMimeTypes(kotlin.String,%20kotlin.String)) 

### getType

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getType(uri: Uri): String?
```

Implement this to handle requests for the MIME type of the data at the given URI. The returned MIME type should start with`vnd.android.cursor.item`for a single record, or`vnd.android.cursor.dir/`for multiple items. This method can be called from multiple threads, as described in [Processes and Threads](https://developer.android.com/guide/topics/fundamentals/processes-and-threads.html#Threads).

Note that by default there are no permissions needed for an application to access this information; if your content provider requires read and/or write permissions, or is not exported, all applications can still call this method regardless of their access permissions.

If your mime type reveals details that should be protected, then you should protect this method by implementing [getTypeAnonymous](https://developer.android.com/reference/kotlin/android/content/ContentProvider#getTypeAnonymous(android.net.Uri)). Implementing [getTypeAnonymous](https://developer.android.com/reference/kotlin/android/content/ContentProvider#getTypeAnonymous(android.net.Uri))ensures your [getType](https://developer.android.com/reference/kotlin/android/content/ContentProvider#getType(android.net.Uri))can be only accessed by caller's having associated readPermission for the URI.

| Parameters ||
|-------|---------------------------------------------------------------------------------------------------------------------------|
| `uri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#):the URI to query. This value cannot be`null`. |

| Return ||
|-----------------------------------------------------------------------------------|--------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | a MIME type string, or`null`if there is no type. |

### getTypeAnonymous

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getTypeAnonymous(uri: Uri): String?
```

Implement this to handle requests for MIME type of URIs, that does not need to reveal any internal information which should be protected by any permission.

If your mime type reveals details that should be protected, then you should protect those by implementing those in [getType](https://developer.android.com/reference/kotlin/android/content/ContentProvider#getType(android.net.Uri)), and in this function, only return types of URIs which can be obtained by anyone without any access. Implementing ths function will make sure [getType](https://developer.android.com/reference/kotlin/android/content/ContentProvider#getType(android.net.Uri))is protected by readPermission. This function by default works as the [getType](https://developer.android.com/reference/kotlin/android/content/ContentProvider#getType(android.net.Uri))

| Parameters ||
|-------|---------------------------------------------------------------------------------------------------------------------------|
| `uri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#):the URI to query. This value cannot be`null`. |

| Return ||
|-----------------------------------------------------------------------------------|------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | a MIME type string, or`null`if type needs to be protected. |

### getWritePermission

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getWritePermission(): String?
```

Return the name of the permission required for read/write access to this content provider. This method can be called from multiple threads, as described in [Processes and Threads](https://developer.android.com/guide/topics/fundamentals/processes-and-threads.html#Threads).

| Return ||
|-----------------------------------------------------------------------------------|--------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | This value may be`null`. |

### insert

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun insert(
    uri: Uri, 
    values: ContentValues?
): Uri?
```

Implement this to handle requests to insert a new row. As a courtesy, call [notifyChange()](https://developer.android.com/reference/kotlin/android/content/ContentResolver#notifyChange(android.net.Uri,%20android.database.ContentObserver))after inserting. This method can be called from multiple threads, as described in [Processes and Threads](https://developer.android.com/guide/topics/fundamentals/processes-and-threads.html#Threads).

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `uri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#):The content:// URI of the insertion request. This value cannot be`null`. |
| `values` | [ContentValues](https://developer.android.com/reference/kotlin/android/content/ContentValues)?:A set of column_name/value pairs to add to the database. This value may be`null`. |

| Return ||
|------------------------------------------------------------------------------|---------------------------------------------------------------|
| [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)? | The URI for the newly inserted item. This value may be`null`. |

### insert

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun insert(
    uri: Uri, 
    values: ContentValues?, 
    extras: Bundle?
): Uri?
```

Implement this to handle requests to insert a new row. As a courtesy, call [notifyChange()](https://developer.android.com/reference/kotlin/android/content/ContentResolver#notifyChange(android.net.Uri,%20android.database.ContentObserver))after inserting. This method can be called from multiple threads, as described in [Processes and Threads](https://developer.android.com/guide/topics/fundamentals/processes-and-threads.html#Threads).

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `uri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#):The content:// URI of the insertion request. This value cannot be`null`. |
| `values` | [ContentValues](https://developer.android.com/reference/kotlin/android/content/ContentValues)?:A set of column_name/value pairs to add to the database. This value may be`null`. |
| `extras` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)?:A Bundle containing additional information necessary for the operation. Arguments may include SQL style arguments, such as [ContentResolver.QUERY_ARG_SQL_LIMIT](https://developer.android.com/reference/kotlin/android/content/ContentResolver#QUERY_ARG_SQL_LIMIT:kotlin.String), but note that the documentation for each individual provider will indicate which arguments they support. This value may be`null`. |

| Return ||
|------------------------------------------------------------------------------|---------------------------------------------------------------|
| [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)? | The URI for the newly inserted item. This value may be`null`. |

| Exceptions ||
|--------------------------------------|------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the provider doesn't support one of the requested Bundle arguments. |

### onCallingPackageChanged

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onCallingPackageChanged(): Unit
```

Called whenever the value of [getCallingPackage()](https://developer.android.com/reference/kotlin/android/content/ContentProvider#getCallingPackage())changes, giving the provider an opportunity to invalidate any security related caching it may be performing.

This typically happens when a [ContentProvider](https://developer.android.com/reference/kotlin/android/content/ContentProvider#) makes a nested call back into itself when already processing a call from a remote process. 

### onConfigurationChanged

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onConfigurationChanged(newConfig: Configuration): Unit
```

Called by the system when the device configuration changes while your component is running. Note that, unlike activities, other components are never restarted when a configuration changes: they must always deal with the results of the change, such as by re-retrieving resources.

At the time that this function has been called, your Resources object will have been updated to return resource values matching the new configuration.

For more information, read [Handling Runtime Changes](https://developer.android.com/guide/topics/resources/runtime-changes.html). This method is always called on the application main thread, and must not perform lengthy operations.

The default content provider implementation does nothing. Override this method to take appropriate action. (Content providers do not usually care about things like screen orientation, but may want to know about locale changes.)

| Parameters ||
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `newConfig` | [Configuration](https://developer.android.com/reference/kotlin/android/content/res/Configuration):The new device configuration. This value cannot be`null`. |

### onCreate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onCreate(): Boolean
```

Implement this to initialize your content provider on startup. This method is called for all registered content providers on the application main thread at application launch time. It must not perform lengthy operations, or application startup will be delayed.

You should defer nontrivial initialization (such as opening, upgrading, and scanning databases) until the content provider is used (via #query, #insert, etc). Deferred initialization keeps application startup fast, avoids unnecessary work if the provider turns out not to be needed, and stops database errors (such as a full disk) from halting application launch.

If you use SQLite, [android.database.sqlite.SQLiteOpenHelper](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteOpenHelper.html#) is a helpful utility class that makes it easy to manage databases, and will automatically defer opening until first use. If you do use SQLiteOpenHelper, make sure to avoid calling [android.database.sqlite.SQLiteOpenHelper#getReadableDatabase](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteOpenHelper.html#getReadableDatabase())or [android.database.sqlite.SQLiteOpenHelper#getWritableDatabase](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteOpenHelper.html#getWritableDatabase())from this method. (Instead, override [android.database.sqlite.SQLiteOpenHelper#onOpen](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteOpenHelper.html#onOpen(android.database.sqlite.SQLiteDatabase))to initialize the database when it is first opened.)

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the provider was successfully loaded, false otherwise |

### onLowMemory

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onLowMemory(): Unit
```

This is called when the overall system is running low on memory, and actively running processes should trim their memory usage. While the exact point at which this will be called is not defined, generally it will happen when all background process have been killed. That is, before reaching the point of killing processes hosting service and foreground UI that we would like to avoid killing. This method is always called on the application main thread, and must not perform lengthy operations.

The default content provider implementation does nothing. Subclasses may override this method to take appropriate action. 

### onTrimMemory

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onTrimMemory(level: Int): Unit
```

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `level` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The context of the trim, giving a hint of the amount of trimming the application may like to perform. Value is [android.content.ComponentCallbacks2#TRIM_MEMORY_COMPLETE](https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2#TRIM_MEMORY_COMPLETE:kotlin.Int), [android.content.ComponentCallbacks2#TRIM_MEMORY_MODERATE](https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2#TRIM_MEMORY_MODERATE:kotlin.Int), [android.content.ComponentCallbacks2#TRIM_MEMORY_BACKGROUND](https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2#TRIM_MEMORY_BACKGROUND:kotlin.Int), [android.content.ComponentCallbacks2#TRIM_MEMORY_UI_HIDDEN](https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2#TRIM_MEMORY_UI_HIDDEN:kotlin.Int), [android.content.ComponentCallbacks2#TRIM_MEMORY_RUNNING_CRITICAL](https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2#TRIM_MEMORY_RUNNING_CRITICAL:kotlin.Int), [android.content.ComponentCallbacks2#TRIM_MEMORY_RUNNING_LOW](https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2#TRIM_MEMORY_RUNNING_LOW:kotlin.Int), or [android.content.ComponentCallbacks2#TRIM_MEMORY_RUNNING_MODERATE](https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2#TRIM_MEMORY_RUNNING_MODERATE:kotlin.Int) |

### openAssetFile

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun openAssetFile(
    uri: Uri, 
    mode: String
): AssetFileDescriptor?
```

This is like #openFile, but can be implemented by providers that need to be able to return sub-sections of files, often assets inside of their .apk. This method can be called from multiple threads, as described in [Processes and Threads](https://developer.android.com/guide/topics/fundamentals/processes-and-threads.html#Threads).

If you implement this, your clients must be able to deal with such file slices, either directly with android.content.ContentResolver#openAssetFileDescriptor, or by using the higher-level [ContentResolver.openInputStream](https://developer.android.com/reference/kotlin/android/content/ContentResolver#openInputStream(android.net.Uri))or android.content.ContentResolver#openOutputStream methods.

The returned AssetFileDescriptor can be a pipe or socket pair to enable streaming of data.

If you are implementing this to return a full file, you should create the AssetFileDescriptor with [AssetFileDescriptor.UNKNOWN_LENGTH](https://developer.android.com/reference/kotlin/android/content/res/AssetFileDescriptor#UNKNOWN_LENGTH:kotlin.Long) to be compatible with applications that cannot handle sub-sections of files.

For use in Intents, you will want to implement [getType](https://developer.android.com/reference/kotlin/android/content/ContentProvider#getType(android.net.Uri))to return the appropriate MIME type for the data returned here with the same URI. This will allow intent resolution to automatically determine the data MIME type and select the appropriate matching targets as part of its operation.

For better interoperability with other applications, it is recommended that for any URIs that can be opened, you also support queries on them containing at least the columns specified by [android.provider.OpenableColumns](https://developer.android.com/reference/kotlin/android/provider/OpenableColumns.html#).

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `uri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#):The URI whose file is to be opened. This value cannot be`null`. |
| `mode` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The string representation of the file mode. Can be "r", "w", "wt", "wa", "rw" or "rwt". Please note the exact implementation of these may differ for each Provider implementation - for example, "w" may or may not truncate. This value cannot be`null`. |

| Return ||
|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [AssetFileDescriptor](https://developer.android.com/reference/kotlin/android/content/res/AssetFileDescriptor)? | Returns a new AssetFileDescriptor which you can use to access the file. This value may be`null`. |

| Exceptions ||
|---------------------------------|--------------------------------------------------------------------------------------------------------|
| `java.io.FileNotFoundException` | Throws FileNotFoundException if there is no file associated with the given URI or the mode is invalid. |
| `java.lang.SecurityException` | Throws SecurityException if the caller does not have permission to access the file. |

**See Also**

- [#openFile(Uri, String)](https://developer.android.com/reference/kotlin/android/content/ContentProvider#openFile(android.net.Uri,%20kotlin.String))
- [#openFileHelper(Uri, String)](https://developer.android.com/reference/kotlin/android/content/ContentProvider#openFileHelper(android.net.Uri,%20kotlin.String))
- <https://developer.android.com/reference/kotlin/android/content/ContentProvider#getType(android.net.Uri)> 

### openAssetFile

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun openAssetFile(
    uri: Uri, 
    mode: String, 
    signal: CancellationSignal?
): AssetFileDescriptor?
```

This is like #openFile, but can be implemented by providers that need to be able to return sub-sections of files, often assets inside of their .apk. This method can be called from multiple threads, as described in [Processes and Threads](https://developer.android.com/guide/topics/fundamentals/processes-and-threads.html#Threads).

If you implement this, your clients must be able to deal with such file slices, either directly with android.content.ContentResolver#openAssetFileDescriptor, or by using the higher-level [ContentResolver.openInputStream](https://developer.android.com/reference/kotlin/android/content/ContentResolver#openInputStream(android.net.Uri))or android.content.ContentResolver#openOutputStream methods.

The returned AssetFileDescriptor can be a pipe or socket pair to enable streaming of data.

If you are implementing this to return a full file, you should create the AssetFileDescriptor with [AssetFileDescriptor.UNKNOWN_LENGTH](https://developer.android.com/reference/kotlin/android/content/res/AssetFileDescriptor#UNKNOWN_LENGTH:kotlin.Long) to be compatible with applications that cannot handle sub-sections of files.

For use in Intents, you will want to implement [getType](https://developer.android.com/reference/kotlin/android/content/ContentProvider#getType(android.net.Uri))to return the appropriate MIME type for the data returned here with the same URI. This will allow intent resolution to automatically determine the data MIME type and select the appropriate matching targets as part of its operation.

For better interoperability with other applications, it is recommended that for any URIs that can be opened, you also support queries on them containing at least the columns specified by [android.provider.OpenableColumns](https://developer.android.com/reference/kotlin/android/provider/OpenableColumns.html#).

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `uri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#):The URI whose file is to be opened. This value cannot be`null`. |
| `mode` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The string representation of the file mode. Can be "r", "w", "wt", "wa", "rw" or "rwt". Please note the exact implementation of these may differ for each Provider implementation - for example, "w" may or may not truncate. This value cannot be`null`. |
| `signal` | [CancellationSignal](https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#)?:A signal to cancel the operation in progress, or`null`if none. For example, if you are downloading a file from the network to service a "rw" mode request, you should periodically call [CancellationSignal.throwIfCanceled()](https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#throwIfCanceled())to check whether the client has canceled the request and abort the download. |

| Return ||
|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [AssetFileDescriptor](https://developer.android.com/reference/kotlin/android/content/res/AssetFileDescriptor)? | Returns a new AssetFileDescriptor which you can use to access the file. This value may be`null`. |

| Exceptions ||
|---------------------------------|--------------------------------------------------------------------------------------------------------|
| `java.io.FileNotFoundException` | Throws FileNotFoundException if there is no file associated with the given URI or the mode is invalid. |
| `java.lang.SecurityException` | Throws SecurityException if the caller does not have permission to access the file. |

**See Also**

- [#openFile(Uri, String)](https://developer.android.com/reference/kotlin/android/content/ContentProvider#openFile(android.net.Uri,%20kotlin.String))
- [#openFileHelper(Uri, String)](https://developer.android.com/reference/kotlin/android/content/ContentProvider#openFileHelper(android.net.Uri,%20kotlin.String))
- <https://developer.android.com/reference/kotlin/android/content/ContentProvider#getType(android.net.Uri)> 

### openFile

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun openFile(
    uri: Uri, 
    mode: String
): ParcelFileDescriptor?
```

Override this to handle requests to open a file blob. The default implementation always throws [FileNotFoundException](https://developer.android.com/reference/kotlin/java/io/FileNotFoundException.html#). This method can be called from multiple threads, as described in [Processes and Threads](https://developer.android.com/guide/topics/fundamentals/processes-and-threads.html#Threads).

This method returns a ParcelFileDescriptor, which is returned directly to the caller. This way large data (such as images and documents) can be returned without copying the content.

The returned ParcelFileDescriptor is owned by the caller, so it is their responsibility to close it when done. That is, the implementation of this method should create a new ParcelFileDescriptor for each call.

If opened with the exclusive "r" or "w" modes, the returned ParcelFileDescriptor can be a pipe or socket pair to enable streaming of data. Opening with the "rw" or "rwt" modes implies a file on disk that supports seeking.

If you need to detect when the returned ParcelFileDescriptor has been closed, or if the remote process has crashed or encountered some other error, you can use [ParcelFileDescriptor.open(File, int,](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#open(java.io.File,%20kotlin.Int,%20android.os.Handler,%20android.os.ParcelFileDescriptor.OnCloseListener)), [ParcelFileDescriptor.createReliablePipe()](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#createReliablePipe()), or [ParcelFileDescriptor.createReliableSocketPair()](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#createReliableSocketPair()).

If you need to return a large file that isn't backed by a real file on disk, such as a file on a network share or cloud storage service, consider using [StorageManager.openProxyFileDescriptor(int, android.os.ProxyFileDescriptorCallback, android.os.Handler)](https://developer.android.com/reference/kotlin/android/os/storage/StorageManager.html#openProxyFileDescriptor(kotlin.Int,%20android.os.ProxyFileDescriptorCallback,%20android.os.Handler))which will let you to stream the content on-demand.

For use in Intents, you will want to implement [getType](https://developer.android.com/reference/kotlin/android/content/ContentProvider#getType(android.net.Uri))to return the appropriate MIME type for the data returned here with the same URI. This will allow intent resolution to automatically determine the data MIME type and select the appropriate matching targets as part of its operation.

For better interoperability with other applications, it is recommended that for any URIs that can be opened, you also support queries on them containing at least the columns specified by [android.provider.OpenableColumns](https://developer.android.com/reference/kotlin/android/provider/OpenableColumns.html#). You may also want to support other common columns if you have additional meta-data to supply, such as [android.provider.MediaStore.MediaColumns#DATE_ADDED](https://developer.android.com/reference/kotlin/android/provider/MediaStore.MediaColumns.html#DATE_ADDED:kotlin.String) in [android.provider.MediaStore.MediaColumns](https://developer.android.com/reference/kotlin/android/provider/MediaStore.MediaColumns.html#).

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `uri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#):The URI whose file is to be opened. This value cannot be`null`. |
| `mode` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The string representation of the file mode. Can be "r", "w", "wt", "wa", "rw" or "rwt". Please note the exact implementation of these may differ for each Provider implementation - for example, "w" may or may not truncate. This value cannot be`null`. |

| Return ||
|---------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [ParcelFileDescriptor](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#)? | Returns a new ParcelFileDescriptor which you can use to access the file. This value may be`null`. |

| Exceptions ||
|---------------------------------|--------------------------------------------------------------------------------------------------------|
| `java.io.FileNotFoundException` | Throws FileNotFoundException if there is no file associated with the given URI or the mode is invalid. |
| `java.lang.SecurityException` | Throws SecurityException if the caller does not have permission to access the file. |

**See Also**

- [#openAssetFile(Uri, String)](https://developer.android.com/reference/kotlin/android/content/ContentProvider#openAssetFile(android.net.Uri,%20kotlin.String))
- [#openFileHelper(Uri, String)](https://developer.android.com/reference/kotlin/android/content/ContentProvider#openFileHelper(android.net.Uri,%20kotlin.String))
- <https://developer.android.com/reference/kotlin/android/content/ContentProvider#getType(android.net.Uri)>
- [android.os.ParcelFileDescriptor#parseMode(String)](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#parseMode(kotlin.String)) 

### openFile

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun openFile(
    uri: Uri, 
    mode: String, 
    signal: CancellationSignal?
): ParcelFileDescriptor?
```

Override this to handle requests to open a file blob. The default implementation always throws [FileNotFoundException](https://developer.android.com/reference/kotlin/java/io/FileNotFoundException.html#). This method can be called from multiple threads, as described in [Processes and Threads](https://developer.android.com/guide/topics/fundamentals/processes-and-threads.html#Threads).

This method returns a ParcelFileDescriptor, which is returned directly to the caller. This way large data (such as images and documents) can be returned without copying the content.

The returned ParcelFileDescriptor is owned by the caller, so it is their responsibility to close it when done. That is, the implementation of this method should create a new ParcelFileDescriptor for each call.

If opened with the exclusive "r" or "w" modes, the returned ParcelFileDescriptor can be a pipe or socket pair to enable streaming of data. Opening with the "rw" or "rwt" modes implies a file on disk that supports seeking.

If you need to detect when the returned ParcelFileDescriptor has been closed, or if the remote process has crashed or encountered some other error, you can use [ParcelFileDescriptor.open(File, int,](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#open(java.io.File,%20kotlin.Int,%20android.os.Handler,%20android.os.ParcelFileDescriptor.OnCloseListener)), [ParcelFileDescriptor.createReliablePipe()](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#createReliablePipe()), or [ParcelFileDescriptor.createReliableSocketPair()](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#createReliableSocketPair()).

For use in Intents, you will want to implement [getType](https://developer.android.com/reference/kotlin/android/content/ContentProvider#getType(android.net.Uri))to return the appropriate MIME type for the data returned here with the same URI. This will allow intent resolution to automatically determine the data MIME type and select the appropriate matching targets as part of its operation.

For better interoperability with other applications, it is recommended that for any URIs that can be opened, you also support queries on them containing at least the columns specified by [android.provider.OpenableColumns](https://developer.android.com/reference/kotlin/android/provider/OpenableColumns.html#). You may also want to support other common columns if you have additional meta-data to supply, such as [android.provider.MediaStore.MediaColumns#DATE_ADDED](https://developer.android.com/reference/kotlin/android/provider/MediaStore.MediaColumns.html#DATE_ADDED:kotlin.String) in [android.provider.MediaStore.MediaColumns](https://developer.android.com/reference/kotlin/android/provider/MediaStore.MediaColumns.html#).

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `uri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#):The URI whose file is to be opened. This value cannot be`null`. |
| `mode` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The string representation of the file mode. Can be "r", "w", "wt", "wa", "rw" or "rwt". Please note the exact implementation of these may differ for each Provider implementation - for example, "w" may or may not truncate. This value cannot be`null`. |
| `signal` | [CancellationSignal](https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#)?:A signal to cancel the operation in progress, or`null`if none. For example, if you are downloading a file from the network to service a "rw" mode request, you should periodically call [CancellationSignal.throwIfCanceled()](https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#throwIfCanceled())to check whether the client has canceled the request and abort the download. |

| Return ||
|---------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [ParcelFileDescriptor](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#)? | Returns a new ParcelFileDescriptor which you can use to access the file. This value may be`null`. |

| Exceptions ||
|---------------------------------|--------------------------------------------------------------------------------------------------------|
| `java.io.FileNotFoundException` | Throws FileNotFoundException if there is no file associated with the given URI or the mode is invalid. |
| `java.lang.SecurityException` | Throws SecurityException if the caller does not have permission to access the file. |

**See Also**

- [#openAssetFile(Uri, String)](https://developer.android.com/reference/kotlin/android/content/ContentProvider#openAssetFile(android.net.Uri,%20kotlin.String))
- [#openFileHelper(Uri, String)](https://developer.android.com/reference/kotlin/android/content/ContentProvider#openFileHelper(android.net.Uri,%20kotlin.String))
- <https://developer.android.com/reference/kotlin/android/content/ContentProvider#getType(android.net.Uri)>
- [android.os.ParcelFileDescriptor#parseMode(String)](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#parseMode(kotlin.String)) 

### openPipeHelper

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun <T : Any!> openPipeHelper(
    uri: Uri, 
    mimeType: String, 
    opts: Bundle?, 
    args: T?, 
    func: ContentProvider.PipeDataWriter<T>
): ParcelFileDescriptor
```

A helper function for implementing #openTypedAssetFile, for creating a data pipe and background thread allowing you to stream generated data back to the client. This function returns a new ParcelFileDescriptor that should be returned to the caller (the caller is responsible for closing it).

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `uri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#):The URI whose data is to be written. This value cannot be`null`. |
| `mimeType` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The desired type of data to be written. This value cannot be`null`. |
| `opts` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)?:Options supplied by caller. This value may be`null`. |
| `args` | T?:Your own custom arguments. This value may be`null`. |
| `func` | [ContentProvider.PipeDataWriter](https://developer.android.com/reference/kotlin/android/content/ContentProvider.PipeDataWriter)\<T\>:Interface implementing the function that will actually stream the data. This value cannot be`null`. |

| Return ||
|--------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ParcelFileDescriptor](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#) | Returns a new ParcelFileDescriptor holding the read side of the pipe. This should be returned to the caller for reading; the caller is responsible for closing it when done. This value cannot be`null`. |

### openTypedAssetFile

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun openTypedAssetFile(
    uri: Uri, 
    mimeTypeFilter: String, 
    opts: Bundle?
): AssetFileDescriptor?
```

Called by a client to open a read-only stream containing data of a particular MIME type. This is like [openAssetFile(android.net.Uri,java.lang.String)](https://developer.android.com/reference/kotlin/android/content/ContentProvider#openAssetFile(android.net.Uri,%20kotlin.String)), except the file can only be read-only and the content provider may perform data conversions to generate data of the desired type.

The default implementation compares the given mimeType against the result of [getType(android.net.Uri)](https://developer.android.com/reference/kotlin/android/content/ContentProvider#getType(android.net.Uri))and, if they match, simply calls [openAssetFile(android.net.Uri,java.lang.String)](https://developer.android.com/reference/kotlin/android/content/ContentProvider#openAssetFile(android.net.Uri,%20kotlin.String)).

See [ClipData](https://developer.android.com/reference/kotlin/android/content/ClipData) for examples of the use and implementation of this method.

The returned AssetFileDescriptor can be a pipe or socket pair to enable streaming of data.

For better interoperability with other applications, it is recommended that for any URIs that can be opened, you also support queries on them containing at least the columns specified by [android.provider.OpenableColumns](https://developer.android.com/reference/kotlin/android/provider/OpenableColumns.html#). You may also want to support other common columns if you have additional meta-data to supply, such as [android.provider.MediaStore.MediaColumns#DATE_ADDED](https://developer.android.com/reference/kotlin/android/provider/MediaStore.MediaColumns.html#DATE_ADDED:kotlin.String) in [android.provider.MediaStore.MediaColumns](https://developer.android.com/reference/kotlin/android/provider/MediaStore.MediaColumns.html#).

| Parameters ||
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `uri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#):The data in the content provider being queried. This value cannot be`null`. |
| `mimeTypeFilter` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The type of data the client desires. May be a pattern, such as \*/\*, if the caller does not have specific type requirements; in this case the content provider will pick its best type matching the pattern. This value cannot be`null`. |
| `opts` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)?:Additional options from the client. The definitions of these are specific to the content provider being called. This value may be`null`. |

| Return ||
|----------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [AssetFileDescriptor](https://developer.android.com/reference/kotlin/android/content/res/AssetFileDescriptor)? | Returns a new AssetFileDescriptor from which the client can read data of the desired type. This value may be`null`. |

| Exceptions ||
|--------------------------------------|--------------------------------------------------------------------------------------------------------|
| `java.io.FileNotFoundException` | Throws FileNotFoundException if there is no file associated with the given URI or the mode is invalid. |
| `java.lang.SecurityException` | Throws SecurityException if the caller does not have permission to access the data. |
| `java.lang.IllegalArgumentException` | Throws IllegalArgumentException if the content provider does not support the requested MIME type. |

**See Also**

- [#getStreamTypes(Uri, String)](https://developer.android.com/reference/kotlin/android/content/ContentProvider#getStreamTypes(android.net.Uri,%20kotlin.String))
- [#openAssetFile(Uri, String)](https://developer.android.com/reference/kotlin/android/content/ContentProvider#openAssetFile(android.net.Uri,%20kotlin.String))
- [android.content.ClipDescription#compareMimeTypes(String, String)](https://developer.android.com/reference/kotlin/android/content/ClipDescription#compareMimeTypes(kotlin.String,%20kotlin.String)) 

### openTypedAssetFile

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun openTypedAssetFile(
    uri: Uri, 
    mimeTypeFilter: String, 
    opts: Bundle?, 
    signal: CancellationSignal?
): AssetFileDescriptor?
```

Called by a client to open a read-only stream containing data of a particular MIME type. This is like [openAssetFile(android.net.Uri,java.lang.String)](https://developer.android.com/reference/kotlin/android/content/ContentProvider#openAssetFile(android.net.Uri,%20kotlin.String)), except the file can only be read-only and the content provider may perform data conversions to generate data of the desired type.

The default implementation compares the given mimeType against the result of [getType(android.net.Uri)](https://developer.android.com/reference/kotlin/android/content/ContentProvider#getType(android.net.Uri))and, if they match, simply calls [openAssetFile(android.net.Uri,java.lang.String)](https://developer.android.com/reference/kotlin/android/content/ContentProvider#openAssetFile(android.net.Uri,%20kotlin.String)).

See [ClipData](https://developer.android.com/reference/kotlin/android/content/ClipData) for examples of the use and implementation of this method.

The returned AssetFileDescriptor can be a pipe or socket pair to enable streaming of data.

For better interoperability with other applications, it is recommended that for any URIs that can be opened, you also support queries on them containing at least the columns specified by [android.provider.OpenableColumns](https://developer.android.com/reference/kotlin/android/provider/OpenableColumns.html#). You may also want to support other common columns if you have additional meta-data to supply, such as [android.provider.MediaStore.MediaColumns#DATE_ADDED](https://developer.android.com/reference/kotlin/android/provider/MediaStore.MediaColumns.html#DATE_ADDED:kotlin.String) in [android.provider.MediaStore.MediaColumns](https://developer.android.com/reference/kotlin/android/provider/MediaStore.MediaColumns.html#).

| Parameters ||
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `uri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#):The data in the content provider being queried. This value cannot be`null`. |
| `mimeTypeFilter` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The type of data the client desires. May be a pattern, such as \*/\*, if the caller does not have specific type requirements; in this case the content provider will pick its best type matching the pattern. This value cannot be`null`. |
| `opts` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)?:Additional options from the client. The definitions of these are specific to the content provider being called. This value may be`null`. |
| `signal` | [CancellationSignal](https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#)?:A signal to cancel the operation in progress, or`null`if none. For example, if you are downloading a file from the network to service a "rw" mode request, you should periodically call [CancellationSignal.throwIfCanceled()](https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#throwIfCanceled())to check whether the client has canceled the request and abort the download. |

| Return ||
|----------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [AssetFileDescriptor](https://developer.android.com/reference/kotlin/android/content/res/AssetFileDescriptor)? | Returns a new AssetFileDescriptor from which the client can read data of the desired type. This value may be`null`. |

| Exceptions ||
|--------------------------------------|--------------------------------------------------------------------------------------------------------|
| `java.io.FileNotFoundException` | Throws FileNotFoundException if there is no file associated with the given URI or the mode is invalid. |
| `java.lang.SecurityException` | Throws SecurityException if the caller does not have permission to access the data. |
| `java.lang.IllegalArgumentException` | Throws IllegalArgumentException if the content provider does not support the requested MIME type. |

**See Also**

- [#getStreamTypes(Uri, String)](https://developer.android.com/reference/kotlin/android/content/ContentProvider#getStreamTypes(android.net.Uri,%20kotlin.String))
- [#openAssetFile(Uri, String)](https://developer.android.com/reference/kotlin/android/content/ContentProvider#openAssetFile(android.net.Uri,%20kotlin.String))
- [android.content.ClipDescription#compareMimeTypes(String, String)](https://developer.android.com/reference/kotlin/android/content/ClipDescription#compareMimeTypes(kotlin.String,%20kotlin.String)) 

### query

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun query(
    uri: Uri, 
    projection: Array<String!>?, 
    queryArgs: Bundle?, 
    cancellationSignal: CancellationSignal?
): Cursor?
```

Implement this to handle query requests where the arguments are packed into a [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#). Arguments may include traditional SQL style query arguments. When present these should be handled according to the contract established in[query(android.net.Uri,java.lang.String[],java.lang.String,java.lang.String[],java.lang.String,android.os.CancellationSignal)](https://developer.android.com/reference/kotlin/android/content/ContentProvider#query(android.net.Uri,%20kotlin.Array,%20kotlin.String,%20kotlin.Array,%20kotlin.String,%20android.os.CancellationSignal)).

Traditional SQL arguments can be found in the bundle using the following keys:
- [android.content.ContentResolver#QUERY_ARG_SQL_SELECTION](https://developer.android.com/reference/kotlin/android/content/ContentResolver#QUERY_ARG_SQL_SELECTION:kotlin.String)
- [android.content.ContentResolver#QUERY_ARG_SQL_SELECTION_ARGS](https://developer.android.com/reference/kotlin/android/content/ContentResolver#QUERY_ARG_SQL_SELECTION_ARGS:kotlin.String)
- [android.content.ContentResolver#QUERY_ARG_SQL_SORT_ORDER](https://developer.android.com/reference/kotlin/android/content/ContentResolver#QUERY_ARG_SQL_SORT_ORDER:kotlin.String)

 This method can be called from multiple threads, as described in [Processes and Threads](https://developer.android.com/guide/topics/fundamentals/processes-and-threads.html#Threads).

 Example client call:

 <br />

  ```kotlin
  // Request 20 records starting at row index 30.
   Bundle queryArgs = new Bundle();
   queryArgs.putInt(ContentResolver.QUERY_ARG_OFFSET, 30);
   queryArgs.putInt(ContentResolver.QUERY_ARG_LIMIT, 20);
   
   Cursor cursor = getContentResolver().query(
           contentUri,    // Content Uri is specific to individual content providers.
           projection,    // String[] describing which columns to return.
           queryArgs,     // Query arguments.
           null);         // Cancellation signal.
  ```
 Example implementation:

 <br />

  ```kotlin
  int recordsetSize = 0x1000;  // Actual value is implementation specific.
   queryArgs = queryArgs != null ? queryArgs : Bundle.EMPTY;  // ensure queryArgs is non-null
   
   int offset = queryArgs.getInt(ContentResolver.QUERY_ARG_OFFSET, 0);
   int limit = queryArgs.getInt(ContentResolver.QUERY_ARG_LIMIT, Integer.MIN_VALUE);
   
   MatrixCursor c = new MatrixCursor(PROJECTION, limit);
   
   // Calculate the number of items to include in the cursor.
   int numItems = MathUtils.constrain(recordsetSize - offset, 0, limit);
   
   // Build the paged result set....
   for (int i = offset; i < offset + numItems; i++) {
       // populate row from your data.
   }
   
   Bundle extras = new Bundle();
   c.setExtras(extras);
   
   // Any QUERY_ARG_* key may be included if honored.
   // In an actual implementation, include only keys that are both present in queryArgs
   // and reflected in the Cursor output. For example, if QUERY_ARG_OFFSET were included
   // in queryArgs, but was ignored because it contained an invalid value (like --273),
   // then QUERY_ARG_OFFSET should be omitted.
   extras.putStringArray(ContentResolver.EXTRA_HONORED_ARGS, new String[] {
       ContentResolver.QUERY_ARG_OFFSET,
       ContentResolver.QUERY_ARG_LIMIT
   });
   
   extras.putInt(ContentResolver.EXTRA_TOTAL_COUNT, recordsetSize);
   
   cursor.setNotificationUri(getContext().getContentResolver(), uri);
   
   return cursor;
  ```

 See[query(android.net.Uri,java.lang.String[],java.lang.String,java.lang.String[],java.lang.String,android.os.CancellationSignal)](https://developer.android.com/reference/kotlin/android/content/ContentProvider#query(android.net.Uri,%20kotlin.Array,%20kotlin.String,%20kotlin.Array,%20kotlin.String,%20android.os.CancellationSignal))for implementation details.

| Parameters ||
|----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `uri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#):The URI to query. This will be the full URI sent by the client. This value cannot be`null`. |
| `projection` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>?:The list of columns to put into the cursor. If`null`provide a default set of columns. |
| `queryArgs` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)?:A Bundle containing additional information necessary for the operation. Arguments may include SQL style arguments, such as [ContentResolver.QUERY_ARG_SQL_LIMIT](https://developer.android.com/reference/kotlin/android/content/ContentResolver#QUERY_ARG_SQL_LIMIT:kotlin.String), but note that the documentation for each individual provider will indicate which arguments they support. This value may be`null`. |
| `cancellationSignal` | [CancellationSignal](https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#)?:A signal to cancel the operation in progress, or`null`. |

| Return ||
|-----------------------------------------------------------------------------------------|--------------------|
| [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#)? | a Cursor or`null`. |

### query

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun query(
    uri: Uri, 
    projection: Array<String!>?, 
    selection: String?, 
    selectionArgs: Array<String!>?, 
    sortOrder: String?
): Cursor?
```

Implement this to handle query requests from clients.

Apps targeting [android.os.Build.VERSION_CODES#O](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#O:kotlin.Int) or higher should override[query(android.net.Uri,java.lang.String[],android.os.Bundle,android.os.CancellationSignal)](https://developer.android.com/reference/kotlin/android/content/ContentProvider#query(android.net.Uri,%20kotlin.Array,%20android.os.Bundle,%20android.os.CancellationSignal))and provide a stub implementation of this method.

This method can be called from multiple threads, as described in [Processes and Threads](https://developer.android.com/guide/topics/fundamentals/processes-and-threads.html#Threads).

Example client call:

<br />

```kotlin
// Request a specific record.
  Cursor managedCursor = managedQuery(
         ContentUris.withAppendedId(Contacts.People.CONTENT_URI, 2),
         projection,    // Which columns to return.
         null,          // WHERE clause.
         null,          // WHERE clause value substitution
         People.NAME + " ASC");   // Sort order.
```
Example implementation:

<br />

```kotlin
// SQLiteQueryBuilder is a helper class that creates the
 // proper SQL syntax for us.
 SQLiteQueryBuilder qBuilder = new SQLiteQueryBuilder();
 
 // Guard against SQL injection attacks
 qBuilder.setStrict(true);
 qBuilder.setProjectionMap(MAP_OF_QUERYABLE_COLUMNS);
 qBuilder.setStrictColumns(true);
 qBuilder.setStrictGrammar(true);
 
 // Set the table we're querying.
 qBuilder.setTables(DATABASE_TABLE_NAME);
 
 // If the query ends in a specific record number, we're
 // being asked for a specific record, so set the
 // WHERE clause in our query.
 if((URI_MATCHER.match(uri)) == SPECIFIC_MESSAGE){
     qBuilder.appendWhere("_id=" + uri.getPathLeafId());
 }
 
 // Make the query.
 Cursor c = qBuilder.query(mDb,
         projection,
         selection,
         selectionArgs,
         groupBy,
         having,
         sortOrder);
 c.setNotificationUri(getContext().getContentResolver(), uri);
 return c;
```

| Parameters ||
|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `uri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#):The URI to query. This will be the full URI sent by the client; if the client is requesting a specific record, the URI will end in a record number that the implementation should parse and add to a WHERE or HAVING clause, specifying that _id value. This value cannot be`null`. |
| `projection` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>?:The list of columns to put into the cursor. If`null`all columns are included. |
| `selection` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:A selection criteria to apply when filtering rows. If`null`then all rows are included. |
| `selectionArgs` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>?:You may include ?s in selection, which will be replaced by the values from selectionArgs, in order that they appear in the selection. The values will be bound as Strings. This value may be`null`. |
| `sortOrder` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:How the rows in the cursor should be sorted. If`null`then the provider is free to define the sort order. |

| Return ||
|-----------------------------------------------------------------------------------------|--------------------|
| [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#)? | a Cursor or`null`. |

### query

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun query(
    uri: Uri, 
    projection: Array<String!>?, 
    selection: String?, 
    selectionArgs: Array<String!>?, 
    sortOrder: String?, 
    cancellationSignal: CancellationSignal?
): Cursor?
```

Implement this to handle query requests from clients with support for cancellation.

Apps targeting [android.os.Build.VERSION_CODES#O](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#O:kotlin.Int) or higher should override[query(android.net.Uri,java.lang.String[],android.os.Bundle,android.os.CancellationSignal)](https://developer.android.com/reference/kotlin/android/content/ContentProvider#query(android.net.Uri,%20kotlin.Array,%20android.os.Bundle,%20android.os.CancellationSignal))instead of this method.

This method can be called from multiple threads, as described in [Processes and Threads](https://developer.android.com/guide/topics/fundamentals/processes-and-threads.html#Threads).

Example client call:

<br />

```kotlin
// Request a specific record.
  Cursor managedCursor = managedQuery(
         ContentUris.withAppendedId(Contacts.People.CONTENT_URI, 2),
         projection,    // Which columns to return.
         null,          // WHERE clause.
         null,          // WHERE clause value substitution
         People.NAME + " ASC");   // Sort order.
```
Example implementation:

<br />

```kotlin
// SQLiteQueryBuilder is a helper class that creates the
 // proper SQL syntax for us.
 SQLiteQueryBuilder qBuilder = new SQLiteQueryBuilder();
 
 // Guard against SQL injection attacks
 qBuilder.setStrict(true);
 qBuilder.setProjectionMap(MAP_OF_QUERYABLE_COLUMNS);
 qBuilder.setStrictColumns(true);
 qBuilder.setStrictGrammar(true);
 
 // Set the table we're querying.
 qBuilder.setTables(DATABASE_TABLE_NAME);
 
 // If the query ends in a specific record number, we're
 // being asked for a specific record, so set the
 // WHERE clause in our query.
 if((URI_MATCHER.match(uri)) == SPECIFIC_MESSAGE){
     qBuilder.appendWhere("_id=" + uri.getPathLeafId());
 }
 
 // Make the query.
 Cursor c = qBuilder.query(mDb,
         projection,
         selection,
         selectionArgs,
         groupBy,
         having,
         sortOrder);
 c.setNotificationUri(getContext().getContentResolver(), uri);
 return c;
```

If you implement this method then you must also implement the version of[query(android.net.Uri,java.lang.String[],java.lang.String,java.lang.String[],java.lang.String)](https://developer.android.com/reference/kotlin/android/content/ContentProvider#query(android.net.Uri,%20kotlin.Array,%20kotlin.String,%20kotlin.Array,%20kotlin.String))that does not take a cancellation signal to ensure correct operation on older versions of the Android Framework in which the cancellation signal overload was not available.

| Parameters ||
|----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `uri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#):The URI to query. This will be the full URI sent by the client; if the client is requesting a specific record, the URI will end in a record number that the implementation should parse and add to a WHERE or HAVING clause, specifying that _id value. This value cannot be`null`. |
| `projection` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>?:The list of columns to put into the cursor. If`null`all columns are included. |
| `selection` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:A selection criteria to apply when filtering rows. If`null`then all rows are included. |
| `selectionArgs` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>?:You may include ?s in selection, which will be replaced by the values from selectionArgs, in order that they appear in the selection. The values will be bound as Strings. This value may be`null`. |
| `sortOrder` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:How the rows in the cursor should be sorted. If`null`then the provider is free to define the sort order. |
| `cancellationSignal` | [CancellationSignal](https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#)?:A signal to cancel the operation in progress, or`null`if none. If the operation is canceled, then [android.os.OperationCanceledException](https://developer.android.com/reference/kotlin/android/os/OperationCanceledException.html#) will be thrown when the query is executed. |

| Return ||
|-----------------------------------------------------------------------------------------|--------------------|
| [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#)? | a Cursor or`null`. |

### refresh

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun refresh(
    uri: Uri!, 
    extras: Bundle?, 
    cancellationSignal: CancellationSignal?
): Boolean
```

Implement this to support refresh of content identified by`uri`. By default, this method returns false; providers who wish to implement this should return true to signal the client that the provider has tried refreshing with its own implementation.

This allows clients to request an explicit refresh of content identified by`uri`.

Client code should only invoke this method when there is a strong indication (such as a user initiated pull to refresh gesture) that the content is stale.

Remember to send [ContentResolver.notifyChange(Uri, android.database.ContentObserver)](https://developer.android.com/reference/kotlin/android/content/ContentResolver#notifyChange(android.net.Uri,%20android.database.ContentObserver))notifications when content changes.

| Parameters ||
|----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `uri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)!:The Uri identifying the data to refresh. |
| `extras` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)?:Additional options from the client. The definitions of these are specific to the content provider being called. This value may be`null`. |
| `cancellationSignal` | [CancellationSignal](https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#)?:A signal to cancel the operation in progress, or`null`if none. For example, if you called refresh on a particular uri, you should call [CancellationSignal.throwIfCanceled()](https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#throwIfCanceled())to check whether the client has canceled the refresh request. |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the provider actually tried refreshing. |

### requireContext

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun requireContext(): Context
```

Retrieves a Non-Nullable Context this provider is running in, this is intended to be called after [onCreate](https://developer.android.com/reference/kotlin/android/content/ContentProvider#onCreate()). When called before context was created, an IllegalStateException will be thrown.

Note A provider must be declared in the manifest and created automatically by the system, and context is only available after [onCreate](https://developer.android.com/reference/kotlin/android/content/ContentProvider#onCreate())is called.

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------|
| [Context](https://developer.android.com/reference/kotlin/android/content/Context) | This value cannot be`null`. |

### restoreCallingIdentity

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun restoreCallingIdentity(identity: ContentProvider.CallingIdentity): Unit
```

Restore the identity of the incoming IPC on the current thread back to a previously identity that was returned by [clearCallingIdentity](https://developer.android.com/reference/kotlin/android/content/ContentProvider#clearCallingIdentity()).

Internally this calls [Binder.restoreCallingIdentity(long)](https://developer.android.com/reference/kotlin/android/os/Binder.html#restoreCallingIdentity(kotlin.Long))and also restores any value stored in [getCallingPackage()](https://developer.android.com/reference/kotlin/android/content/ContentProvider#getCallingPackage()).

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `identity` | [ContentProvider.CallingIdentity](https://developer.android.com/reference/kotlin/android/content/ContentProvider.CallingIdentity):This value cannot be`null`. |

### shutdown

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun shutdown(): Unit
```

Implement this to shut down the ContentProvider instance. You can then invoke this method in unit tests.

Android normally handles ContentProvider startup and shutdown automatically. You do not need to start up or shut down a ContentProvider. When you invoke a test method on a ContentProvider, however, a ContentProvider instance is started and keeps running after the test finishes, even if a succeeding test instantiates another ContentProvider. A conflict develops because the two instances are usually running against the same underlying data source (for example, an sqlite database).

Implementing shutDown() avoids this conflict by providing a way to terminate the ContentProvider. This method can also prevent memory leaks from multiple instantiations of the ContentProvider, and it can ensure unit test isolation by allowing you to completely clean up the test fixture before moving on to the next test. 

### uncanonicalize

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun uncanonicalize(url: Uri): Uri?
```

Remove canonicalization from canonical URIs previously returned by [canonicalize](https://developer.android.com/reference/kotlin/android/content/ContentProvider#canonicalize(android.net.Uri)). For example, if your implementation is to add a query param to canonicalize a URI, this method can simply trip any query params on the URI. The default implementation always returns the same url that was passed in.

| Parameters ||
|-------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `url` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#):The Uri to remove any canonicalization from. This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)? | Return the non-canonical representation of url, return the url as-is if there is nothing to do, or return null if the data identified by the canonical representation can not be found in the current environment. |

### update

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun update(
    uri: Uri, 
    values: ContentValues?, 
    extras: Bundle?
): Int
```

Implement this to handle requests to update one or more rows. The implementation should update all rows matching the selection to set the columns according to the provided values map. As a courtesy, call [notifyChange()](https://developer.android.com/reference/kotlin/android/content/ContentResolver#notifyChange(android.net.Uri,%20android.database.ContentObserver))after updating. This method can be called from multiple threads, as described in [Processes and Threads](https://developer.android.com/guide/topics/fundamentals/processes-and-threads.html#Threads).

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `uri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#):The URI to query. This can potentially have a record ID if this is an update request for a specific record. This value cannot be`null`. |
| `values` | [ContentValues](https://developer.android.com/reference/kotlin/android/content/ContentValues)?:A set of column_name/value pairs to update in the database. This value may be`null`. |
| `extras` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)?:A Bundle containing additional information necessary for the operation. Arguments may include SQL style arguments, such as [ContentResolver.QUERY_ARG_SQL_LIMIT](https://developer.android.com/reference/kotlin/android/content/ContentResolver#QUERY_ARG_SQL_LIMIT:kotlin.String), but note that the documentation for each individual provider will indicate which arguments they support. This value may be`null`. |

| Return ||
|----------------------------------------------------------------------------|------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of rows affected. |

| Exceptions ||
|--------------------------------------|------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the provider doesn't support one of the requested Bundle arguments. |

### update

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun update(
    uri: Uri, 
    values: ContentValues?, 
    selection: String?, 
    selectionArgs: Array<String!>?
): Int
```

Implement this to handle requests to update one or more rows. The implementation should update all rows matching the selection to set the columns according to the provided values map. As a courtesy, call [notifyChange()](https://developer.android.com/reference/kotlin/android/content/ContentResolver#notifyChange(android.net.Uri,%20android.database.ContentObserver))after updating. This method can be called from multiple threads, as described in [Processes and Threads](https://developer.android.com/guide/topics/fundamentals/processes-and-threads.html#Threads).

| Parameters ||
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `uri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#):The URI to query. This can potentially have a record ID if this is an update request for a specific record. This value cannot be`null`. |
| `values` | [ContentValues](https://developer.android.com/reference/kotlin/android/content/ContentValues)?:A set of column_name/value pairs to update in the database. This value may be`null`. |
| `selection` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:An optional filter to match rows to update. This value may be`null`. |
| `selectionArgs` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>?:This value may be`null`. |

| Return ||
|----------------------------------------------------------------------------|------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of rows affected. |

## Protected methods

### isTemporary

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun isTemporary(): Boolean
```

Returns true if this instance is a temporary content provider.

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if this instance is a temporary content provider |

### openFileHelper

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected fun openFileHelper(
    uri: Uri, 
    mode: String
): ParcelFileDescriptor
```

Convenience for subclasses that wish to implement #openFile by looking up a column named "_data" at the given URI.

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `uri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#):The URI to be opened. This value cannot be`null`. |
| `mode` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The string representation of the file mode. Can be "r", "w", "wt", "wa", "rw" or "rwt". Please note the exact implementation of these may differ for each Provider implementation - for example, "w" may or may not truncate. This value cannot be`null`. |

| Return ||
|--------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [ParcelFileDescriptor](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#) | Returns a new ParcelFileDescriptor that can be used by the client to access the file. This value cannot be`null`. |

### setPathPermissions

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected fun setPathPermissions(permissions: Array<PathPermission!>?): Unit
```

Change the path-based permission required to read and/or write data in the content provider. This is normally set for you from its manifest information when the provider is first created.

| Parameters ||
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `permissions` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [PathPermission](https://developer.android.com/reference/kotlin/android/content/pm/PathPermission)!\>?:Array of path permission descriptions. This value may be`null`. |

### setReadPermission

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected fun setReadPermission(permission: String?): Unit
```

Change the permission required to read data from the content provider. This is normally set for you from its manifest information when the provider is first created.

| Parameters ||
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `permission` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:Name of the permission required for read-only access. This value may be`null`. |

### setWritePermission

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected fun setWritePermission(permission: String?): Unit
```

Change the permission required to read and write data in the content provider. This is normally set for you from its manifest information when the provider is first created.

| Parameters ||
|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `permission` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:Name of the permission required for read/write access. This value may be`null`. |
