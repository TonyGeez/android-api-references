Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MockContentProvider

```
open class MockContentProvider : ContentProvider
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.content.ContentProvider](../android/content/ContentProvider.md) ||
| | ↳ | [android.test.mock.MockContentProvider](../android/test/mock/MockContentProvider.md) |

Mock implementation of ContentProvider. All methods are non-functional and throw `https://developer.android.com/reference/kotlin/java/lang/UnsupportedOperationException.html#`. Tests can extend this class to implement behavior needed for tests.

## Summary

Inherited constants From class `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#` `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#TRIM_MEMORY_BACKGROUND:kotlin.Int`

Level for `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#onTrimMemory(kotlin.Int)`: the process has gone on to the LRU list. This is a good opportunity to clean up resources that can efficiently and quickly be re-built if the user returns to the app.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#TRIM_MEMORY_COMPLETE:kotlin.Int`

Level for `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#onTrimMemory(kotlin.Int)`: the process is nearing the end of the background LRU list, and if more memory isn't found soon it will be killed.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#TRIM_MEMORY_MODERATE:kotlin.Int`

Level for `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#onTrimMemory(kotlin.Int)`: the process is around the middle of the background LRU list; freeing memory can help the system keep other processes running later in the list for better overall performance.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#TRIM_MEMORY_RUNNING_CRITICAL:kotlin.Int`

Level for `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#onTrimMemory(kotlin.Int)`: the process is not an expendable background process, but the device is running extremely low on memory and is about to not be able to keep any background processes running. Your running process should free up as many non-critical resources as it can to allow that memory to be used elsewhere. The next thing that will happen after this is `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks.html#onLowMemory()` called to report that nothing at all can be kept in the background, a situation that can start to notably impact the user.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#TRIM_MEMORY_RUNNING_LOW:kotlin.Int`

Level for `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#onTrimMemory(kotlin.Int)`: the process is not an expendable background process, but the device is running low on memory. Your running process should free up unneeded resources to allow that memory to be used elsewhere.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#TRIM_MEMORY_RUNNING_MODERATE:kotlin.Int`

Level for `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#onTrimMemory(kotlin.Int)`: the process is not an expendable background process, but the device is running moderately low on memory. Your running process may want to release some unneeded resources for use elsewhere.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#TRIM_MEMORY_UI_HIDDEN:kotlin.Int`

Level for `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#onTrimMemory(kotlin.Int)`: the process had been showing a user interface, and is no longer doing so. Large allocations with the UI should be released at this point to allow memory to be better managed.

<br />

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/test/mock/MockContentProvider#MockContentProvider(android.content.Context)(context: https://developer.android.com/reference/kotlin/android/content/Context.html#!)` A constructor accepting a Context instance, which is supposed to be the subclasss of `https://developer.android.com/reference/kotlin/android/test/mock/MockContext`. |
| `https://developer.android.com/reference/kotlin/android/test/mock/MockContentProvider#MockContentProvider(android.content.Context,%20kotlin.String,%20kotlin.String,%20kotlin.Array)(context: https://developer.android.com/reference/kotlin/android/content/Context.html#!, readPermission: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, writePermission: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, pathPermissions: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/android/content/pm/PathPermission.html#!>!)` A constructor which initialize four member variables which `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#` have internally. |

| Protected constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/test/mock/MockContentProvider#MockContentProvider()()` A constructor using `https://developer.android.com/reference/kotlin/android/test/mock/MockContext` instance as a Context in it. |

| Public methods ||
|---|---|
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [ContentProviderResult](../android/content/ContentProviderResult.md)!\> | `https://developer.android.com/reference/kotlin/android/test/mock/MockContentProvider#applyBatch(java.util.ArrayList)(operations: https://developer.android.com/reference/kotlin/java/util/ArrayList.html#<https://developer.android.com/reference/kotlin/android/content/ContentProviderOperation.html#!>)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/test/mock/MockContentProvider#attachInfo(android.content.Context,%20android.content.pm.ProviderInfo)(context: https://developer.android.com/reference/kotlin/android/content/Context.html#!, info: https://developer.android.com/reference/kotlin/android/content/pm/ProviderInfo.html#!)` After being instantiated, this is called to tell the content provider about itself. |
| open static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/test/mock/MockContentProvider#attachInfoForTesting(android.content.ContentProvider,%20android.content.Context,%20android.content.pm.ProviderInfo)(provider: https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#!, context: https://developer.android.com/reference/kotlin/android/content/Context.html#!, providerInfo: https://developer.android.com/reference/kotlin/android/content/pm/ProviderInfo.html#!)` Like `https://developer.android.com/reference/kotlin/android/test/mock/MockContentProvider#attachInfo(android.content.Context,%20android.content.pm.ProviderInfo)`, but for use when directly instantiating the provider for testing. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/test/mock/MockContentProvider#bulkInsert(android.net.Uri,%20kotlin.Array)(uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#, values: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/android/content/ContentValues.html#!>)` If you're reluctant to implement this manually, please just call super. |
| open [Bundle](../android/os/Bundle.md)? | `https://developer.android.com/reference/kotlin/android/test/mock/MockContentProvider#call(kotlin.String,%20kotlin.String,%20android.os.Bundle)(method: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, request: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, args: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?)` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/test/mock/MockContentProvider#delete(android.net.Uri,%20kotlin.String,%20kotlin.Array)(uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#, selection: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, selectionArgs: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>?)` Implement this to handle requests to delete one or more rows. |
| --- | --- |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>? | `https://developer.android.com/reference/kotlin/android/test/mock/MockContentProvider#getStreamTypes(android.net.Uri,%20kotlin.String)(url: https://developer.android.com/reference/kotlin/android/net/Uri.html#, mimeTypeFilter: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Called by a client to determine the types of data streams that this content provider supports for the given URI. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | `https://developer.android.com/reference/kotlin/android/test/mock/MockContentProvider#getType(android.net.Uri)(uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#)` Implement this to handle requests for the MIME type of the data at the given URI. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | `https://developer.android.com/reference/kotlin/android/test/mock/MockContentProvider#getTypeAnonymous(android.net.Uri)(uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#)` Implement this to handle requests for MIME type of URIs, that does not need to reveal any internal information which should be protected by any permission. |
| --- | --- |
| open [Uri](../android/net/Uri.md)? | `https://developer.android.com/reference/kotlin/android/test/mock/MockContentProvider#insert(android.net.Uri,%20android.content.ContentValues)(uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#, values: https://developer.android.com/reference/kotlin/android/content/ContentValues.html#?)` Implement this to handle requests to insert a new row. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/test/mock/MockContentProvider#onCreate()()` Implement this to initialize your content provider on startup. |
| open [AssetFileDescriptor](../android/content/res/AssetFileDescriptor.md)? | `https://developer.android.com/reference/kotlin/android/test/mock/MockContentProvider#openTypedAssetFile(android.net.Uri,%20kotlin.String,%20android.os.Bundle)(url: https://developer.android.com/reference/kotlin/android/net/Uri.html#, mimeType: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, opts: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?)` Called by a client to open a read-only stream containing data of a particular MIME type. |
| --- | --- |
| open [Cursor](../android/database/Cursor.md)? | `https://developer.android.com/reference/kotlin/android/test/mock/MockContentProvider#query(android.net.Uri,%20kotlin.Array,%20kotlin.String,%20kotlin.Array,%20kotlin.String)(uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#, projection: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>?, selection: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, selectionArgs: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>?, sortOrder: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?)` Implement this to handle query requests from clients. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/test/mock/MockContentProvider#update(android.net.Uri,%20android.content.ContentValues,%20kotlin.String,%20kotlin.Array)(uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#, values: https://developer.android.com/reference/kotlin/android/content/ContentValues.html#?, selection: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, selectionArgs: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>?)` Implement this to handle requests to update one or more rows. |

Inherited functions From class `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#` `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/android/content/ContentProviderResult.html#!>` `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#applyBatch(kotlin.String,%20java.util.ArrayList)(authority: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, operations: https://developer.android.com/reference/kotlin/java/util/ArrayList.html#<https://developer.android.com/reference/kotlin/android/content/ContentProviderOperation.html#!>)`

Override this to handle requests to perform a batch of operations, or the default implementation will iterate over the operations and call `https://developer.android.com/reference/kotlin/android/content/ContentProviderOperation.html#apply(android.content.ContentProvider,%20kotlin.Array,%20kotlin.Int)` on each of them. If all calls to `https://developer.android.com/reference/kotlin/android/content/ContentProviderOperation.html#apply(android.content.ContentProvider,%20kotlin.Array,%20kotlin.Int)` succeed then a `https://developer.android.com/reference/kotlin/android/content/ContentProviderResult.html#` array with as many elements as there were operations will be returned. If any of the calls fail, it is up to the implementation how many of the others take effect. This method can be called from multiple threads, as described in [Processes and Threads](https://developer.android.com/guide/topics/fundamentals/processes-and-threads.html#Threads).

<br />

`https://developer.android.com/reference/kotlin/android/os/Bundle.html#?` `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#call(kotlin.String,%20kotlin.String,%20kotlin.String,%20android.os.Bundle)(authority: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, method: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, arg: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, extras: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?)`

Call a provider-defined method. This can be used to implement interfaces that are cheaper and/or unnatural for a table-like model.

**WARNING:** The framework does no permission checking on this entry into the content provider besides the basic ability for the application to get access to the provider at all. For example, it has no idea whether the call being executed may read or write data in the provider, so can't enforce those individual permissions. Any implementation of this method **must** do its own permission checks on incoming calls to make sure they are allowed.

<br />

`https://developer.android.com/reference/kotlin/android/net/Uri.html#?` `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#canonicalize(android.net.Uri)(url: https://developer.android.com/reference/kotlin/android/net/Uri.html#)`

Implement this to support canonicalization of URIs that refer to your content provider. A canonical URI is one that can be transported across devices, backup/restore, and other contexts, and still be able to refer to the same data item. Typically this is implemented by adding query params to the URI allowing the content provider to verify that an incoming canonical URI references the same data as it was originally intended for and, if it doesn't, to find that data (if it exists) in the current environment.

For example, if the content provider holds people and a normal URI in it is created with a row index into that people database, the cananical representation may have an additional query param at the end which specifies the name of the person it is intended for. Later calls into the provider with that URI will look up the row of that URI's base index and, if it doesn't match or its entry's name doesn't match the name in the query param, perform a query on its database to find the correct row to operate on.

If you implement support for canonical URIs, **all** incoming calls with URIs (including this one) must perform this verification and recovery of any canonical URIs they receive. In addition, you must also implement `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#uncanonicalize(android.net.Uri)` to strip the canonicalization of any of these URIs.

The default implementation of this method returns null, indicating that canonical URIs are not supported.

<br />

`https://developer.android.com/reference/kotlin/android/content/ContentProvider.CallingIdentity.html#` `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#clearCallingIdentity()()`

Reset the identity of the incoming IPC on the current thread.

Internally this calls `https://developer.android.com/reference/kotlin/android/os/Binder.html#clearCallingIdentity()` and also clears any value stored in `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#getCallingPackage()`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#delete(android.net.Uri,%20android.os.Bundle)(uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#, extras: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?)`

Implement this to handle requests to delete one or more rows. The implementation should apply the selection clause when performing deletion, allowing the operation to affect multiple rows in a directory. As a courtesy, call `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#notifyChange(android.net.Uri,%20android.database.ContentObserver)` after deleting. This method can be called from multiple threads, as described in [Processes and Threads](https://developer.android.com/guide/topics/fundamentals/processes-and-threads.html#Threads).

The implementation is responsible for parsing out a row ID at the end of the URI, if a specific row is being deleted. That is, the client would pass in `content://contacts/people/22` and the implementation is responsible for parsing the record number (22) when creating a SQL statement.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#dump(java.io.FileDescriptor,%20java.io.PrintWriter,%20kotlin.Array)(fd: https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#!, writer: https://developer.android.com/reference/kotlin/java/io/PrintWriter.html#!, args: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!)`

Print the Provider's state into the given stream. This gets invoked if you run "adb shell dumpsys activity provider \<provider_component_name\>".

<br />

`https://developer.android.com/reference/kotlin/android/content/AttributionSource.html#?` `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#getCallingAttributionSource()()`

Gets the attribution source of the calling app. If you want to attribute the data access to the calling app you can create an attribution context via `https://developer.android.com/reference/kotlin/android/content/Context.html#createContext(android.content.ContextParams)` and passing this identity to `https://developer.android.com/reference/kotlin/android/content/ContextParams.Builder.html#setNextAttributionSource(android.content.AttributionSource)`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?` `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#getCallingAttributionTag()()`

Return the attribution tag of the caller that initiated the request being processed on the current thread. Returns `null` if not currently processing a request of the request is for the default attribution.

This will always return `null` when processing `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#getTypeAnonymous(android.net.Uri)` requests For `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#getType(android.net.Uri)` requests, this will be only available for cases, where the caller can be identified. See `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#getTypeAnonymous(android.net.Uri)`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?` `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#getCallingPackage()()`

Return the package name of the caller that initiated the request being processed on the current thread. The returned package will have been verified to belong to the calling UID. Returns `null` if not currently processing a request.

This will always return `null` when processing `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#getTypeAnonymous(android.net.Uri)` requests For `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#getType(android.net.Uri)` requests, this will be only available for cases, where the caller can be identified. See `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#getTypeAnonymous(android.net.Uri)`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?` `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#getCallingPackageUnchecked()()`

Return the package name of the caller that initiated the request being processed on the current thread. The returned package will have *not* been verified to belong to the calling UID. Returns `null` if not currently processing a request.

This will always return `null` when processing `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#getTypeAnonymous(android.net.Uri)` requests For `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#getType(android.net.Uri)` requests, this will be only available for cases, where the caller can be identified. See `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#getTypeAnonymous(android.net.Uri)`

<br />

`https://developer.android.com/reference/kotlin/android/content/Context.html#?` `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#getContext()()`

Retrieves the Context this provider is running in. Only available once `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#onCreate()` has been called -- this will return `null` in the constructor.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/android/content/pm/PathPermission.html#!>?` `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#getPathPermissions()()`

Return the path-based permissions required for read and/or write access to this content provider. This method can be called from multiple threads, as described in [Processes and Threads](https://developer.android.com/guide/topics/fundamentals/processes-and-threads.html#Threads).

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?` `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#getReadPermission()()`

Return the name of the permission required for read-only access to this content provider. This method can be called from multiple threads, as described in [Processes and Threads](https://developer.android.com/guide/topics/fundamentals/processes-and-threads.html#Threads).

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?` `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#getWritePermission()()`

Return the name of the permission required for read/write access to this content provider. This method can be called from multiple threads, as described in [Processes and Threads](https://developer.android.com/guide/topics/fundamentals/processes-and-threads.html#Threads).

<br />

`https://developer.android.com/reference/kotlin/android/net/Uri.html#?` `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#insert(android.net.Uri,%20android.content.ContentValues,%20android.os.Bundle)(uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#, values: https://developer.android.com/reference/kotlin/android/content/ContentValues.html#?, extras: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?)`

Implement this to handle requests to insert a new row. As a courtesy, call `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#notifyChange(android.net.Uri,%20android.database.ContentObserver)` after inserting. This method can be called from multiple threads, as described in [Processes and Threads](https://developer.android.com/guide/topics/fundamentals/processes-and-threads.html#Threads).

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#isTemporary()()`

Returns true if this instance is a temporary content provider.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#onCallingPackageChanged()()`

Called whenever the value of `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#getCallingPackage()` changes, giving the provider an opportunity to invalidate any security related caching it may be performing.

This typically happens when a `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#` makes a nested call back into itself when already processing a call from a remote process.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#onConfigurationChanged(android.content.res.Configuration)(newConfig: https://developer.android.com/reference/kotlin/android/content/res/Configuration.html#)`

Called by the system when the device configuration changes while your component is running. Note that, unlike activities, other components are never restarted when a configuration changes: they must always deal with the results of the change, such as by re-retrieving resources.

At the time that this function has been called, your Resources object will have been updated to return resource values matching the new configuration.

For more information, read [Handling Runtime Changes](https://developer.android.com/guide/topics/resources/runtime-changes.html). This method is always called on the application main thread, and must not perform lengthy operations.

The default content provider implementation does nothing. Override this method to take appropriate action. (Content providers do not usually care about things like screen orientation, but may want to know about locale changes.)

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#onLowMemory()()`

This is called when the overall system is running low on memory, and actively running processes should trim their memory usage. While the exact point at which this will be called is not defined, generally it will happen when all background process have been killed. That is, before reaching the point of killing processes hosting service and foreground UI that we would like to avoid killing. This method is always called on the application main thread, and must not perform lengthy operations.

The default content provider implementation does nothing. Subclasses may override this method to take appropriate action.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#onTrimMemory(kotlin.Int)(level: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Called when the operating system has determined that it is a good time for a process to trim unneeded memory from its process. You should never compare to exact values of the level, since new intermediate values may be added -- you will typically want to compare if the value is greater or equal to a level you are interested in.

To retrieve the processes current trim level at any point, you can use `https://developer.android.com/reference/kotlin/android/app/ActivityManager.html#getMyMemoryState(android.app.ActivityManager.RunningAppProcessInfo)`.

<br />

`https://developer.android.com/reference/kotlin/android/content/res/AssetFileDescriptor.html#?` `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#openAssetFile(android.net.Uri,%20kotlin.String)(uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#, mode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`

This is like #openFile, but can be implemented by providers that need to be able to return sub-sections of files, often assets inside of their .apk. This method can be called from multiple threads, as described in [Processes and Threads](https://developer.android.com/guide/topics/fundamentals/processes-and-threads.html#Threads).

If you implement this, your clients must be able to deal with such file slices, either directly with android.content.ContentResolver#openAssetFileDescriptor, or by using the higher-level `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#openInputStream(android.net.Uri)` or android.content.ContentResolver#openOutputStream methods.

The returned AssetFileDescriptor can be a pipe or socket pair to enable streaming of data.

If you are implementing this to return a full file, you should create the AssetFileDescriptor with `https://developer.android.com/reference/kotlin/android/content/res/AssetFileDescriptor.html#UNKNOWN_LENGTH:kotlin.Long` to be compatible with applications that cannot handle sub-sections of files.

For use in Intents, you will want to implement `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#getType(android.net.Uri)` to return the appropriate MIME type for the data returned here with the same URI. This will allow intent resolution to automatically determine the data MIME type and select the appropriate matching targets as part of its operation.

For better interoperability with other applications, it is recommended that for any URIs that can be opened, you also support queries on them containing at least the columns specified by `https://developer.android.com/reference/kotlin/android/provider/OpenableColumns.html#`.

<br />

`https://developer.android.com/reference/kotlin/android/content/res/AssetFileDescriptor.html#?` `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#openAssetFile(android.net.Uri,%20kotlin.String,%20android.os.CancellationSignal)(uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#, mode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, signal: https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#?)`

This is like #openFile, but can be implemented by providers that need to be able to return sub-sections of files, often assets inside of their .apk. This method can be called from multiple threads, as described in [Processes and Threads](https://developer.android.com/guide/topics/fundamentals/processes-and-threads.html#Threads).

If you implement this, your clients must be able to deal with such file slices, either directly with android.content.ContentResolver#openAssetFileDescriptor, or by using the higher-level `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#openInputStream(android.net.Uri)` or android.content.ContentResolver#openOutputStream methods.

The returned AssetFileDescriptor can be a pipe or socket pair to enable streaming of data.

If you are implementing this to return a full file, you should create the AssetFileDescriptor with `https://developer.android.com/reference/kotlin/android/content/res/AssetFileDescriptor.html#UNKNOWN_LENGTH:kotlin.Long` to be compatible with applications that cannot handle sub-sections of files.

For use in Intents, you will want to implement `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#getType(android.net.Uri)` to return the appropriate MIME type for the data returned here with the same URI. This will allow intent resolution to automatically determine the data MIME type and select the appropriate matching targets as part of its operation.

For better interoperability with other applications, it is recommended that for any URIs that can be opened, you also support queries on them containing at least the columns specified by `https://developer.android.com/reference/kotlin/android/provider/OpenableColumns.html#`.

<br />

`https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#?` `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#openFile(android.net.Uri,%20kotlin.String)(uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#, mode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`

Override this to handle requests to open a file blob. The default implementation always throws `https://developer.android.com/reference/kotlin/java/io/FileNotFoundException.html#`. This method can be called from multiple threads, as described in [Processes and Threads](https://developer.android.com/guide/topics/fundamentals/processes-and-threads.html#Threads).

This method returns a ParcelFileDescriptor, which is returned directly to the caller. This way large data (such as images and documents) can be returned without copying the content.

The returned ParcelFileDescriptor is owned by the caller, so it is their responsibility to close it when done. That is, the implementation of this method should create a new ParcelFileDescriptor for each call.

If opened with the exclusive "r" or "w" modes, the returned ParcelFileDescriptor can be a pipe or socket pair to enable streaming of data. Opening with the "rw" or "rwt" modes implies a file on disk that supports seeking.

If you need to detect when the returned ParcelFileDescriptor has been closed, or if the remote process has crashed or encountered some other error, you can use `https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#open(java.io.File,%20kotlin.Int,%20android.os.Handler,%20android.os.ParcelFileDescriptor.OnCloseListener)`, `https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#createReliablePipe()`, or `https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#createReliableSocketPair()`.

If you need to return a large file that isn't backed by a real file on disk, such as a file on a network share or cloud storage service, consider using `https://developer.android.com/reference/kotlin/android/os/storage/StorageManager.html#openProxyFileDescriptor(kotlin.Int,%20android.os.ProxyFileDescriptorCallback,%20android.os.Handler)` which will let you to stream the content on-demand.

For use in Intents, you will want to implement `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#getType(android.net.Uri)` to return the appropriate MIME type for the data returned here with the same URI. This will allow intent resolution to automatically determine the data MIME type and select the appropriate matching targets as part of its operation.

For better interoperability with other applications, it is recommended that for any URIs that can be opened, you also support queries on them containing at least the columns specified by `https://developer.android.com/reference/kotlin/android/provider/OpenableColumns.html#`. You may also want to support other common columns if you have additional meta-data to supply, such as `https://developer.android.com/reference/kotlin/android/provider/MediaStore.MediaColumns.html#DATE_ADDED:kotlin.String` in `https://developer.android.com/reference/kotlin/android/provider/MediaStore.MediaColumns.html#`.

<br />

`https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#?` `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#openFile(android.net.Uri,%20kotlin.String,%20android.os.CancellationSignal)(uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#, mode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, signal: https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#?)`

Override this to handle requests to open a file blob. The default implementation always throws `https://developer.android.com/reference/kotlin/java/io/FileNotFoundException.html#`. This method can be called from multiple threads, as described in [Processes and Threads](https://developer.android.com/guide/topics/fundamentals/processes-and-threads.html#Threads).

This method returns a ParcelFileDescriptor, which is returned directly to the caller. This way large data (such as images and documents) can be returned without copying the content.

The returned ParcelFileDescriptor is owned by the caller, so it is their responsibility to close it when done. That is, the implementation of this method should create a new ParcelFileDescriptor for each call.

If opened with the exclusive "r" or "w" modes, the returned ParcelFileDescriptor can be a pipe or socket pair to enable streaming of data. Opening with the "rw" or "rwt" modes implies a file on disk that supports seeking.

If you need to detect when the returned ParcelFileDescriptor has been closed, or if the remote process has crashed or encountered some other error, you can use `https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#open(java.io.File,%20kotlin.Int,%20android.os.Handler,%20android.os.ParcelFileDescriptor.OnCloseListener)`, `https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#createReliablePipe()`, or `https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#createReliableSocketPair()`.

For use in Intents, you will want to implement `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#getType(android.net.Uri)` to return the appropriate MIME type for the data returned here with the same URI. This will allow intent resolution to automatically determine the data MIME type and select the appropriate matching targets as part of its operation.

For better interoperability with other applications, it is recommended that for any URIs that can be opened, you also support queries on them containing at least the columns specified by `https://developer.android.com/reference/kotlin/android/provider/OpenableColumns.html#`. You may also want to support other common columns if you have additional meta-data to supply, such as `https://developer.android.com/reference/kotlin/android/provider/MediaStore.MediaColumns.html#DATE_ADDED:kotlin.String` in `https://developer.android.com/reference/kotlin/android/provider/MediaStore.MediaColumns.html#`.

<br />

`https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#` `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#openFileHelper(android.net.Uri,%20kotlin.String)(uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#, mode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`

Convenience for subclasses that wish to implement #openFile by looking up a column named "_data" at the given URI.

<br />

`https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#` `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#openPipeHelper(android.net.Uri,%20kotlin.String,%20android.os.Bundle,%20android.content.ContentProvider.openPipeHelper.T,%20android.content.ContentProvider.PipeDataWriter)(uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#, mimeType: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, opts: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?, args: T?, func: https://developer.android.com/reference/kotlin/android/content/ContentProvider.PipeDataWriter.html#<T>)`

A helper function for implementing #openTypedAssetFile, for creating a data pipe and background thread allowing you to stream generated data back to the client. This function returns a new ParcelFileDescriptor that should be returned to the caller (the caller is responsible for closing it).

<br />

`https://developer.android.com/reference/kotlin/android/content/res/AssetFileDescriptor.html#?` `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#openTypedAssetFile(android.net.Uri,%20kotlin.String,%20android.os.Bundle,%20android.os.CancellationSignal)(uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#, mimeTypeFilter: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, opts: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?, signal: https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#?)`

Called by a client to open a read-only stream containing data of a particular MIME type. This is like `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#openAssetFile(android.net.Uri,%20kotlin.String)`, except the file can only be read-only and the content provider may perform data conversions to generate data of the desired type.

The default implementation compares the given mimeType against the result of `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#getType(android.net.Uri)` and, if they match, simply calls `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#openAssetFile(android.net.Uri,%20kotlin.String)`.

See `https://developer.android.com/reference/kotlin/android/content/ClipData.html#` for examples of the use and implementation of this method.

The returned AssetFileDescriptor can be a pipe or socket pair to enable streaming of data.

For better interoperability with other applications, it is recommended that for any URIs that can be opened, you also support queries on them containing at least the columns specified by `https://developer.android.com/reference/kotlin/android/provider/OpenableColumns.html#`. You may also want to support other common columns if you have additional meta-data to supply, such as `https://developer.android.com/reference/kotlin/android/provider/MediaStore.MediaColumns.html#DATE_ADDED:kotlin.String` in `https://developer.android.com/reference/kotlin/android/provider/MediaStore.MediaColumns.html#`.

<br />

`https://developer.android.com/reference/kotlin/android/database/Cursor.html#?` `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#query(android.net.Uri,%20kotlin.Array,%20android.os.Bundle,%20android.os.CancellationSignal)(uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#, projection: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>?, queryArgs: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?, cancellationSignal: https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#?)`

Implement this to handle query requests where the arguments are packed into a `https://developer.android.com/reference/kotlin/android/os/Bundle.html#`. Arguments may include traditional SQL style query arguments. When present these should be handled according to the contract established in `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#query(android.net.Uri,%20kotlin.Array,%20kotlin.String,%20kotlin.Array,%20kotlin.String,%20android.os.CancellationSignal)`.

Traditional SQL arguments can be found in the bundle using the following keys:
- `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#QUERY_ARG_SQL_SELECTION:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#QUERY_ARG_SQL_SELECTION_ARGS:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#QUERY_ARG_SQL_SORT_ORDER:kotlin.String`

 This method can be called from multiple threads, as described in [Processes and Threads](https://developer.android.com/guide/topics/fundamentals/processes-and-threads.html#Threads).

 Example client call:

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

 See `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#query(android.net.Uri,%20kotlin.Array,%20kotlin.String,%20kotlin.Array,%20kotlin.String,%20android.os.CancellationSignal)` for implementation details.

`https://developer.android.com/reference/kotlin/android/database/Cursor.html#?` `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#query(android.net.Uri,%20kotlin.Array,%20kotlin.String,%20kotlin.Array,%20kotlin.String,%20android.os.CancellationSignal)(uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#, projection: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>?, selection: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, selectionArgs: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>?, sortOrder: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, cancellationSignal: https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#?)`

Implement this to handle query requests from clients with support for cancellation.

Apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#O:kotlin.Int` or higher should override `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#query(android.net.Uri,%20kotlin.Array,%20android.os.Bundle,%20android.os.CancellationSignal)` instead of this method.

This method can be called from multiple threads, as described in [Processes and Threads](https://developer.android.com/guide/topics/fundamentals/processes-and-threads.html#Threads).

Example client call:

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

If you implement this method then you must also implement the version of `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#query(android.net.Uri,%20kotlin.Array,%20kotlin.String,%20kotlin.Array,%20kotlin.String)` that does not take a cancellation signal to ensure correct operation on older versions of the Android Framework in which the cancellation signal overload was not available.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#refresh(android.net.Uri,%20android.os.Bundle,%20android.os.CancellationSignal)(uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#!, extras: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?, cancellationSignal: https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#?)`

Implement this to support refresh of content identified by `uri`. By default, this method returns false; providers who wish to implement this should return true to signal the client that the provider has tried refreshing with its own implementation.

This allows clients to request an explicit refresh of content identified by `uri`.

Client code should only invoke this method when there is a strong indication (such as a user initiated pull to refresh gesture) that the content is stale.

Remember to send `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#notifyChange(android.net.Uri,%20android.database.ContentObserver)` notifications when content changes.

<br />

`https://developer.android.com/reference/kotlin/android/content/Context.html#` `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#requireContext()()`

Retrieves a Non-Nullable Context this provider is running in, this is intended to be called after `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#onCreate()`. When called before context was created, an IllegalStateException will be thrown.

Note A provider must be declared in the manifest and created automatically by the system, and context is only available after `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#onCreate()` is called.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#restoreCallingIdentity(android.content.ContentProvider.CallingIdentity)(identity: https://developer.android.com/reference/kotlin/android/content/ContentProvider.CallingIdentity.html#)`

Restore the identity of the incoming IPC on the current thread back to a previously identity that was returned by `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#clearCallingIdentity()`.

Internally this calls `https://developer.android.com/reference/kotlin/android/os/Binder.html#restoreCallingIdentity(kotlin.Long)` and also restores any value stored in `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#getCallingPackage()`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#setPathPermissions(kotlin.Array)(permissions: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/android/content/pm/PathPermission.html#!>?)`

Change the path-based permission required to read and/or write data in the content provider. This is normally set for you from its manifest information when the provider is first created.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#setReadPermission(kotlin.String)(permission: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?)`

Change the permission required to read data from the content provider. This is normally set for you from its manifest information when the provider is first created.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#setWritePermission(kotlin.String)(permission: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?)`

Change the permission required to read and write data in the content provider. This is normally set for you from its manifest information when the provider is first created.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#shutdown()()`

Implement this to shut down the ContentProvider instance. You can then invoke this method in unit tests.

Android normally handles ContentProvider startup and shutdown automatically. You do not need to start up or shut down a ContentProvider. When you invoke a test method on a ContentProvider, however, a ContentProvider instance is started and keeps running after the test finishes, even if a succeeding test instantiates another ContentProvider. A conflict develops because the two instances are usually running against the same underlying data source (for example, an sqlite database).

Implementing shutDown() avoids this conflict by providing a way to terminate the ContentProvider. This method can also prevent memory leaks from multiple instantiations of the ContentProvider, and it can ensure unit test isolation by allowing you to completely clean up the test fixture before moving on to the next test.

<br />

`https://developer.android.com/reference/kotlin/android/net/Uri.html#?` `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#uncanonicalize(android.net.Uri)(url: https://developer.android.com/reference/kotlin/android/net/Uri.html#)`

Remove canonicalization from canonical URIs previously returned by `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#canonicalize(android.net.Uri)`. For example, if your implementation is to add a query param to canonicalize a URI, this method can simply trip any query params on the URI. The default implementation always returns the same url that was passed in.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#update(android.net.Uri,%20android.content.ContentValues,%20android.os.Bundle)(uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#, values: https://developer.android.com/reference/kotlin/android/content/ContentValues.html#?, extras: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?)`

Implement this to handle requests to update one or more rows. The implementation should update all rows matching the selection to set the columns according to the provided values map. As a courtesy, call `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#notifyChange(android.net.Uri,%20android.database.ContentObserver)` after updating. This method can be called from multiple threads, as described in [Processes and Threads](https://developer.android.com/guide/topics/fundamentals/processes-and-threads.html#Threads).

<br />

From class `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks.html#` `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks.html#onConfigurationChanged(android.content.res.Configuration)(newConfig: https://developer.android.com/reference/kotlin/android/content/res/Configuration.html#)`

Called by the system when the device configuration changes while your component is running. Note that, unlike activities, other components are never restarted when a configuration changes: they must always deal with the results of the change, such as by re-retrieving resources.

At the time that this function has been called, your Resources object will have been updated to return resource values matching the new configuration.

For more information, read [Handling Runtime Changes](https://developer.android.com/guide/topics/resources/runtime-changes.html).

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks.html#onLowMemory()()`

This is called when the overall system is running low on memory, and actively running processes should trim their memory usage. While the exact point at which this will be called is not defined, generally it will happen when all background process have been killed. That is, before reaching the point of killing processes hosting service and foreground UI that we would like to avoid killing.

<br />

## Public constructors

### MockContentProvider

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
MockContentProvider(context: Context!)
```

A constructor accepting a Context instance, which is supposed to be the subclasss of `https://developer.android.com/reference/kotlin/android/test/mock/MockContext`.

### MockContentProvider

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
MockContentProvider(
    context: Context!, 
    readPermission: String!, 
    writePermission: String!, 
    pathPermissions: Array<PathPermission!>!)
```

A constructor which initialize four member variables which `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#` have internally.

| Parameters ||
|---|---|
| `context` | [Context](../android/content/Context.md)!: A Context object which should be some mock instance (like the instance of `https://developer.android.com/reference/kotlin/android/test/mock/MockContext`). |
| `readPermission` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The read permision you want this instance should have in the test, which is available via `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#getReadPermission()`. |
| `writePermission` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The write permission you want this instance should have in the test, which is available via `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#getWritePermission()`. |
| --- | --- |
| `pathPermissions` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [PathPermission](../android/content/pm/PathPermission.md)!\>!: The PathPermissions you want this instance should have in the test, which is available via `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#getPathPermissions()`. |

## Protected constructors

### MockContentProvider

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected MockContentProvider()
```

A constructor using `https://developer.android.com/reference/kotlin/android/test/mock/MockContext` instance as a Context in it.

## Public methods

### applyBatch

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun applyBatch(operations: ArrayList<ContentProviderOperation!>): Array<ContentProviderResult!>
```

| Parameters ||
|---|---|
| `operations` | [ArrayList](../java/util/ArrayList.md)\< [ContentProviderOperation](../android/content/ContentProviderOperation.md)!\>: This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/android/content/ContentProviderResult.html#!>` | This value cannot be `null`. |

### attachInfo

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun attachInfo(
    context: Context!, 
    info: ProviderInfo!
): Unit
```

After being instantiated, this is called to tell the content provider about itself.

| Parameters ||
|---|---|
| `context` | [Context](../android/content/Context.md)!: The context this provider is running in |
| `info` | [ProviderInfo](../android/content/pm/ProviderInfo.md)!: Registered information about this content provider |

### attachInfoForTesting

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun attachInfoForTesting(
    provider: ContentProvider!, 
    context: Context!, 
    providerInfo: ProviderInfo!
): Unit
```

**Deprecated:** *Use a mocking framework like [Mockito](https://github.com/mockito/mockito). New tests should be written using the [Android Testing Support Library](https://developer.android.com/tools/testing-support-library/index.html).*

Like `https://developer.android.com/reference/kotlin/android/test/mock/MockContentProvider#attachInfo(android.content.Context,%20android.content.pm.ProviderInfo)`, but for use when directly instantiating the provider for testing.

Provided for use by `android.test.ProviderTestCase2` and `android.test.RenamingDelegatingContext`.

### bulkInsert

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun bulkInsert(
    uri: Uri, 
    values: Array<ContentValues!>
): Int
```

If you're reluctant to implement this manually, please just call super.bulkInsert().

| Parameters ||
|---|---|
| `uri` | [Uri](../android/net/Uri.md): The content:// URI of the insertion request. This value cannot be `null`. |
| `values` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [ContentValues](../android/content/ContentValues.md)!\>: An array of sets of column_name/value pairs to add to the database. This must not be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The number of values that were inserted. |

### call

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun call(
    method: String, 
    request: String?, 
    args: Bundle?
): Bundle?
```

| Parameters ||
|---|---|
| `method` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |
| `arg` | This value may be `null`. |
| `extras` | This value may be `null`. |
| --- | --- |
| `request` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: This value may be `null`. |
| `args` | [Bundle](../android/os/Bundle.md)?: This value may be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/os/Bundle.html#?` | This value may be `null`. |

### delete

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun delete(
    uri: Uri, 
    selection: String?, 
    selectionArgs: Array<String!>?
): Int
```

Implement this to handle requests to delete one or more rows. The implementation should apply the selection clause when performing deletion, allowing the operation to affect multiple rows in a directory. As a courtesy, call `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#notifyChange(android.net.Uri,%20android.database.ContentObserver)` after deleting. This method can be called from multiple threads, as described in [Processes and Threads](https://developer.android.com/guide/topics/fundamentals/processes-and-threads.html#Threads).

The implementation is responsible for parsing out a row ID at the end of the URI, if a specific row is being deleted. That is, the client would pass in `content://contacts/people/22` and the implementation is responsible for parsing the record number (22) when creating a SQL statement.

| Parameters ||
|---|---|
| `uri` | [Uri](../android/net/Uri.md): The full URI to query, including a row ID (if a specific record is requested). This value cannot be `null`. |
| `selection` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: An optional restriction to apply to rows when deleting. This value may be `null`. |
| `selectionArgs` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>?: This value may be `null`. |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The number of rows affected. |

| Exceptions ||
|---|---|
| `android.database.SQLException` | |

### getStreamTypes

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getStreamTypes(
    url: Uri, 
    mimeTypeFilter: String
): Array<String!>?
```

Called by a client to determine the types of data streams that this content provider supports for the given URI. The default implementation returns `null`, meaning no types. If your content provider stores data of a particular type, return that MIME type if it matches the given mimeTypeFilter. If it can perform type conversions, return an array of all supported MIME types that match mimeTypeFilter.

| Parameters ||
|---|---|
| `uri` | The data in the content provider being queried. This value cannot be `null`. |
| `mimeTypeFilter` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The type of data the client desires. May be a pattern, such as \*/\* to retrieve all possible data types. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>?` | Returns `null` if there are no possible data streams for the given mimeTypeFilter. Otherwise returns an array of all available concrete MIME types. |

### getType

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getType(uri: Uri): String?
```

Implement this to handle requests for the MIME type of the data at the given URI. The returned MIME type should start with `vnd.android.cursor.item` for a single record, or `vnd.android.cursor.dir/` for multiple items. This method can be called from multiple threads, as described in [Processes and Threads](https://developer.android.com/guide/topics/fundamentals/processes-and-threads.html#Threads).

Note that by default there are no permissions needed for an application to access this information; if your content provider requires read and/or write permissions, or is not exported, all applications can still call this method regardless of their access permissions.

If your mime type reveals details that should be protected, then you should protect this method by implementing `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#getTypeAnonymous(android.net.Uri)`. Implementing `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#getTypeAnonymous(android.net.Uri)` ensures your `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#getType(android.net.Uri)` can be only accessed by caller's having associated readPermission for the URI.

| Parameters ||
|---|---|
| `uri` | [Uri](../android/net/Uri.md): the URI to query. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?` | a MIME type string, or `null` if there is no type. |

### getTypeAnonymous

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getTypeAnonymous(uri: Uri): String?
```

Implement this to handle requests for MIME type of URIs, that does not need to reveal any internal information which should be protected by any permission.

If your mime type reveals details that should be protected, then you should protect those by implementing those in `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#getType(android.net.Uri)`, and in this function, only return types of URIs which can be obtained by anyone without any access. Implementing ths function will make sure `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#getType(android.net.Uri)` is protected by readPermission. This function by default works as the `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#getType(android.net.Uri)`

| Parameters ||
|---|---|
| `uri` | [Uri](../android/net/Uri.md): the URI to query. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?` | a MIME type string, or `null` if type needs to be protected. |

### insert

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun insert(
    uri: Uri, 
    values: ContentValues?
): Uri?
```

Implement this to handle requests to insert a new row. As a courtesy, call `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#notifyChange(android.net.Uri,%20android.database.ContentObserver)` after inserting. This method can be called from multiple threads, as described in [Processes and Threads](https://developer.android.com/guide/topics/fundamentals/processes-and-threads.html#Threads).

| Parameters ||
|---|---|
| `uri` | [Uri](../android/net/Uri.md): The content:// URI of the insertion request. This value cannot be `null`. |
| `values` | [ContentValues](../android/content/ContentValues.md)?: A set of column_name/value pairs to add to the database. This value may be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/net/Uri.html#?` | The URI for the newly inserted item. This value may be `null`. |

### onCreate

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onCreate(): Boolean
```

Implement this to initialize your content provider on startup. This method is called for all registered content providers on the application main thread at application launch time. It must not perform lengthy operations, or application startup will be delayed.

You should defer nontrivial initialization (such as opening, upgrading, and scanning databases) until the content provider is used (via #query, #insert, etc). Deferred initialization keeps application startup fast, avoids unnecessary work if the provider turns out not to be needed, and stops database errors (such as a full disk) from halting application launch.

If you use SQLite, `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteOpenHelper.html#` is a helpful utility class that makes it easy to manage databases, and will automatically defer opening until first use. If you do use SQLiteOpenHelper, make sure to avoid calling `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteOpenHelper.html#getReadableDatabase()` or `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteOpenHelper.html#getWritableDatabase()` from this method. (Instead, override `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteOpenHelper.html#onOpen(android.database.sqlite.SQLiteDatabase)` to initialize the database when it is first opened.)

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the provider was successfully loaded, false otherwise |

### openTypedAssetFile

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun openTypedAssetFile(
    url: Uri, 
    mimeType: String, 
    opts: Bundle?
): AssetFileDescriptor?
```

Called by a client to open a read-only stream containing data of a particular MIME type. This is like `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#openAssetFile(android.net.Uri,%20kotlin.String)`, except the file can only be read-only and the content provider may perform data conversions to generate data of the desired type.

The default implementation compares the given mimeType against the result of `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#getType(android.net.Uri)` and, if they match, simply calls `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#openAssetFile(android.net.Uri,%20kotlin.String)`.

See `https://developer.android.com/reference/kotlin/android/content/ClipData.html#` for examples of the use and implementation of this method.

The returned AssetFileDescriptor can be a pipe or socket pair to enable streaming of data.

For better interoperability with other applications, it is recommended that for any URIs that can be opened, you also support queries on them containing at least the columns specified by `https://developer.android.com/reference/kotlin/android/provider/OpenableColumns.html#`. You may also want to support other common columns if you have additional meta-data to supply, such as `https://developer.android.com/reference/kotlin/android/provider/MediaStore.MediaColumns.html#DATE_ADDED:kotlin.String` in `https://developer.android.com/reference/kotlin/android/provider/MediaStore.MediaColumns.html#`.

| Parameters ||
|---|---|
| `uri` | The data in the content provider being queried. This value cannot be `null`. |
| `mimeTypeFilter` | The type of data the client desires. May be a pattern, such as \*/\*, if the caller does not have specific type requirements; in this case the content provider will pick its best type matching the pattern. This value cannot be `null`. |
| `opts` | [Bundle](../android/os/Bundle.md)?: Additional options from the client. The definitions of these are specific to the content provider being called. This value may be `null`. |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/res/AssetFileDescriptor.html#?` | Returns a new AssetFileDescriptor from which the client can read data of the desired type. This value may be `null`. |

| Exceptions ||
|---|---|
| `java.io.FileNotFoundException` | Throws FileNotFoundException if there is no file associated with the given URI or the mode is invalid. |
| `java.lang.IllegalArgumentException` | Throws IllegalArgumentException if the content provider does not support the requested MIME type. |
| `java.lang.SecurityException` | Throws SecurityException if the caller does not have permission to access the data. |
| --- | --- |

### query

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun query(
    uri: Uri, 
    projection: Array<String!>?, 
    selection: String?, 
    selectionArgs: Array<String!>?, 
    sortOrder: String?
): Cursor?
```

Implement this to handle query requests from clients.

Apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#O:kotlin.Int` or higher should override `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#query(android.net.Uri,%20kotlin.Array,%20android.os.Bundle,%20android.os.CancellationSignal)` and provide a stub implementation of this method.

This method can be called from multiple threads, as described in [Processes and Threads](https://developer.android.com/guide/topics/fundamentals/processes-and-threads.html#Threads).

Example client call:

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
|---|---|
| `uri` | [Uri](../android/net/Uri.md): The URI to query. This will be the full URI sent by the client; if the client is requesting a specific record, the URI will end in a record number that the implementation should parse and add to a WHERE or HAVING clause, specifying that _id value. This value cannot be `null`. |
| `projection` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>?: The list of columns to put into the cursor. If `null` all columns are included. |
| `selection` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: A selection criteria to apply when filtering rows. If `null` then all rows are included. |
| --- | --- |
| `selectionArgs` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>?: You may include ?s in selection, which will be replaced by the values from selectionArgs, in order that they appear in the selection. The values will be bound as Strings. This value may be `null`. |
| `sortOrder` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: How the rows in the cursor should be sorted. If `null` then the provider is free to define the sort order. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/database/Cursor.html#?` | a Cursor or `null`. |

### update

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun update(
    uri: Uri, 
    values: ContentValues?, 
    selection: String?, 
    selectionArgs: Array<String!>?
): Int
```

Implement this to handle requests to update one or more rows. The implementation should update all rows matching the selection to set the columns according to the provided values map. As a courtesy, call `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#notifyChange(android.net.Uri,%20android.database.ContentObserver)` after updating. This method can be called from multiple threads, as described in [Processes and Threads](https://developer.android.com/guide/topics/fundamentals/processes-and-threads.html#Threads).

| Parameters ||
|---|---|
| `uri` | [Uri](../android/net/Uri.md): The URI to query. This can potentially have a record ID if this is an update request for a specific record. This value cannot be `null`. |
| `values` | [ContentValues](../android/content/ContentValues.md)?: A set of column_name/value pairs to update in the database. This value may be `null`. |
| `selection` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: An optional filter to match rows to update. This value may be `null`. |
| --- | --- |
| `selectionArgs` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>?: This value may be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the number of rows affected. |
