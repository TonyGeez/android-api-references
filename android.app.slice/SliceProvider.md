# SliceProvider

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SliceProvider

Kotlin| [Java](../android/app/slice/SliceProvider.md) 
| --- | --- |

```
abstract class SliceProvider : ContentProvider
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.content.ContentProvider](../android/content/ContentProvider.md) ||
| | ↳ | [android.app.slice.SliceProvider](../android/app/slice/SliceProvider.md) |

| **This class was deprecated in API level 35.**
|
| Slice framework has been deprecated, it will not receive any updates from android.os.Build.VANILLA_ICE_CREAM and forward. If you are looking for a framework that sends displayable data from one app to another, consider using [android.app.appsearch.AppSearchManager](../android/app/appsearch/AppSearchManager.md).

A SliceProvider allows an app to provide content to be displayed in system spaces. This content is templated and can contain actions, and the behavior of how it is surfaced is specific to the system surface.

Slices are not currently live content. They are bound once and shown to the user. If the content changes due to a callback from user interaction, then [ContentResolver.notifyChange(Uri, ContentObserver)](../android/content/ContentResolver.md))should be used to notify the system.

The provider needs to be declared in the manifest to provide the authority for the app. The authority for most slices is expected to match the package of the application. 

```kotlin
<provider
      android:name="com.example.mypkg.MySliceProvider"
      android:authorities="com.example.mypkg" />
  
```

Slices can be identified by a Uri or by an Intent. To link an Intent with a slice, the provider must have an [IntentFilter](../android/content/IntentFilter.md) matching the slice intent. When a slice is being requested via an intent, [onMapIntentToUri(android.content.Intent)](../android/app/slice/SliceProvider.md))can be called and is expected to return an appropriate Uri representing the slice. 

```kotlin
<provider
      android:name="com.example.mypkg.MySliceProvider"
      android:authorities="com.example.mypkg">
      <intent-filter>
          <action android:name="com.example.mypkg.intent.action.MY_SLICE_INTENT" />
          <category android:name="android.app.slice.category.SLICE" />
      </intent-filter>
  </provider>
  
```

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SLICE_TYPE](../android/app/slice/SliceProvider.md) This is the Android platform's MIME type for a URI containing a slice implemented through [SliceProvider](../android/app/slice/SliceProvider.md). |

| Inherited constants ||
|---|---|
| From class [ComponentCallbacks2](../android/content/ComponentCallbacks2.md) |----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TRIM_MEMORY_BACKGROUND](../android/content/ComponentCallbacks2.md) <br /> Level for [onTrimMemory(int)](../android/content/ComponentCallbacks2.md)): the process has gone on to the LRU list. This is a good opportunity to clean up resources that can efficiently and quickly be re-built if the user returns to the app. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TRIM_MEMORY_COMPLETE](../android/content/ComponentCallbacks2.md) <br /> Level for [onTrimMemory(int)](../android/content/ComponentCallbacks2.md)): the process is nearing the end of the background LRU list, and if more memory isn't found soon it will be killed. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TRIM_MEMORY_MODERATE](../android/content/ComponentCallbacks2.md) <br /> Level for [onTrimMemory(int)](../android/content/ComponentCallbacks2.md)): the process is around the middle of the background LRU list; freeing memory can help the system keep other processes running later in the list for better overall performance. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TRIM_MEMORY_RUNNING_CRITICAL](../android/content/ComponentCallbacks2.md) <br /> Level for [onTrimMemory(int)](../android/content/ComponentCallbacks2.md)): the process is not an expendable background process, but the device is running extremely low on memory and is about to not be able to keep any background processes running. Your running process should free up as many non-critical resources as it can to allow that memory to be used elsewhere. The next thing that will happen after this is [onLowMemory()](../android/content/ComponentCallbacks.md))called to report that nothing at all can be kept in the background, a situation that can start to notably impact the user. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TRIM_MEMORY_RUNNING_LOW](../android/content/ComponentCallbacks2.md) <br /> Level for [onTrimMemory(int)](../android/content/ComponentCallbacks2.md)): the process is not an expendable background process, but the device is running low on memory. Your running process should free up unneeded resources to allow that memory to be used elsewhere. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TRIM_MEMORY_RUNNING_MODERATE](../android/content/ComponentCallbacks2.md) <br /> Level for [onTrimMemory(int)](../android/content/ComponentCallbacks2.md)): the process is not an expendable background process, but the device is running moderately low on memory. Your running process may want to release some unneeded resources for use elsewhere. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TRIM_MEMORY_UI_HIDDEN](../android/content/ComponentCallbacks2.md) <br /> Level for [onTrimMemory(int)](../android/content/ComponentCallbacks2.md)): the process had been showing a user interface, and is no longer doing so. Large allocations with the UI should be released at this point to allow memory to be better managed. <br /> | ||

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SliceProvider](../android/app/slice/SliceProvider.md))`()` <br /> |
| [SliceProvider](../android/app/slice/SliceProvider.md))`(`vararg` `autoGrantPermissions:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` A version of constructing a SliceProvider that allows autogranting slice permissions to apps that hold specific platform permissions. |

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [attachInfo](../android/app/slice/SliceProvider.md))`(`context:` ` [Context](../android/content/Context.md)!`, `info:` ` [ProviderInfo](../android/content/pm/ProviderInfo.md)!`)` <br /> |
| open [Bundle](../android/os/Bundle.md)? | [call](../android/app/slice/SliceProvider.md))`(`method:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `arg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `extras:` ` [Bundle](../android/os/Bundle.md)?`)` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [delete](../android/app/slice/SliceProvider.md))`(`uri:` ` [Uri](../android/net/Uri.md)`, `selection:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `selectionArgs:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>?`)` <br /> |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getType](../android/app/slice/SliceProvider.md))`(`uri:` ` [Uri](../android/net/Uri.md)`)` <br /> |
| [Uri](../android/net/Uri.md)? | [insert](../android/app/slice/SliceProvider.md))`(`uri:` ` [Uri](../android/net/Uri.md)`, `values:` ` [ContentValues](../android/content/ContentValues.md)?`)` <br /> |
| open [Slice](../android/app/slice/Slice.md)! | [onBindSlice](../android/app/slice/SliceProvider.md))`(`sliceUri:` ` [Uri](../android/net/Uri.md)!`, `supportedSpecs:` ` [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [SliceSpec](../android/app/slice/SliceSpec.md)!>!`)` Implemented to create a slice. |
| --- | --- |
| open [PendingIntent](../android/app/PendingIntent.md) | [onCreatePermissionRequest](../android/app/slice/SliceProvider.md))`(`sliceUri:` ` [Uri](../android/net/Uri.md)!`)` Called when an app requests a slice it does not have write permission to the uri for. |
| open [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\< [Uri](../android/net/Uri.md)!\> | [onGetSliceDescendants](../android/app/slice/SliceProvider.md))`(`uri:` ` [Uri](../android/net/Uri.md)`)` Obtains a list of slices that are descendants of the specified Uri. |
| open [Uri](../android/net/Uri.md) | [onMapIntentToUri](../android/app/slice/SliceProvider.md))`(`intent:` ` [Intent](../android/content/Intent.md)!`)` This method must be overridden if an [IntentFilter](../android/content/IntentFilter.md) is specified on the SliceProvider. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onSlicePinned](../android/app/slice/SliceProvider.md))`(`sliceUri:` ` [Uri](../android/net/Uri.md)!`)` Called to inform an app that a slice has been pinned. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onSliceUnpinned](../android/app/slice/SliceProvider.md))`(`sliceUri:` ` [Uri](../android/net/Uri.md)!`)` Called to inform an app that a slices is no longer pinned. |
| [Cursor](../android/database/Cursor.md)? | [query](../android/app/slice/SliceProvider.md))`(`uri:` ` [Uri](../android/net/Uri.md)`, `projection:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>?`, `queryArgs:` ` [Bundle](../android/os/Bundle.md)?`, `cancellationSignal:` ` [CancellationSignal](../android/os/CancellationSignal.md)?`)` <br /> |
| --- | --- |
| [Cursor](../android/database/Cursor.md)? | [query](../android/app/slice/SliceProvider.md))`(`uri:` ` [Uri](../android/net/Uri.md)`, `projection:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>?`, `selection:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `selectionArgs:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>?`, `sortOrder:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` <br /> |
| [Cursor](../android/database/Cursor.md)? | [query](../android/app/slice/SliceProvider.md))`(`uri:` ` [Uri](../android/net/Uri.md)`, `projection:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>?`, `selection:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `selectionArgs:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>?`, `sortOrder:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `cancellationSignal:` ` [CancellationSignal](../android/os/CancellationSignal.md)?`)` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [update](../android/app/slice/SliceProvider.md))`(`uri:` ` [Uri](../android/net/Uri.md)`, `values:` ` [ContentValues](../android/content/ContentValues.md)?`, `selection:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `selectionArgs:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>?`)` <br /> |
| --- | --- |

| Inherited functions ||
|---|---|
| From class [ContentProvider](../android/content/ContentProvider.md) |------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [ContentProviderResult](../android/content/ContentProviderResult.md)!> | [applyBatch](../android/content/ContentProvider.md))`(`authority:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `operations:` ` [ArrayList](../java/util/ArrayList.md)< [ContentProviderOperation](../android/content/ContentProviderOperation.md)!>`)` <br /> Override this to handle requests to perform a batch of operations, or the default implementation will iterate over the operations and call [ContentProviderOperation.apply](../android/content/ContentProviderOperation.md))on each of them. If all calls to [ContentProviderOperation.apply](../android/content/ContentProviderOperation.md))succeed then a [ContentProviderResult](../android/content/ContentProviderResult.md) array with as many elements as there were operations will be returned. If any of the calls fail, it is up to the implementation how many of the others take effect. This method can be called from multiple threads, as described in [Processes and Threads](https://developer.android.com/guide/topics/fundamentals/processes-and-threads.html#Threads). <br /> | | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [ContentProviderResult](../android/content/ContentProviderResult.md)!> | [applyBatch](../android/content/ContentProvider.md))`(`operations:` ` [ArrayList](../java/util/ArrayList.md)< [ContentProviderOperation](../android/content/ContentProviderOperation.md)!>`)` <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [bulkInsert](../android/content/ContentProvider.md))`(`uri:` ` [Uri](../android/net/Uri.md)`, `values:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [ContentValues](../android/content/ContentValues.md)!>`)` <br /> Override this to handle requests to insert a set of new rows, or the default implementation will iterate over the values and call #insert on each of them. As a courtesy, call [notifyChange()](../android/content/ContentResolver.md))after inserting. This method can be called from multiple threads, as described in [Processes and Threads](https://developer.android.com/guide/topics/fundamentals/processes-and-threads.html#Threads). <br /> | | [Bundle](../android/os/Bundle.md)? | [call](../android/content/ContentProvider.md))`(`authority:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `method:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `arg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `extras:` ` [Bundle](../android/os/Bundle.md)?`)` <br /> Call a provider-defined method. This can be used to implement interfaces that are cheaper and/or unnatural for a table-like model. **WARNING:** The framework does no permission checking on this entry into the content provider besides the basic ability for the application to get access to the provider at all. For example, it has no idea whether the call being executed may read or write data in the provider, so can't enforce those individual permissions. Any implementation of this method**must**do its own permission checks on incoming calls to make sure they are allowed. <br /> | | [Uri](../android/net/Uri.md)? | [canonicalize](../android/content/ContentProvider.md))`(`url:` ` [Uri](../android/net/Uri.md)`)` <br /> Implement this to support canonicalization of URIs that refer to your content provider. A canonical URI is one that can be transported across devices, backup/restore, and other contexts, and still be able to refer to the same data item. Typically this is implemented by adding query params to the URI allowing the content provider to verify that an incoming canonical URI references the same data as it was originally intended for and, if it doesn't, to find that data (if it exists) in the current environment. For example, if the content provider holds people and a normal URI in it is created with a row index into that people database, the cananical representation may have an additional query param at the end which specifies the name of the person it is intended for. Later calls into the provider with that URI will look up the row of that URI's base index and, if it doesn't match or its entry's name doesn't match the name in the query param, perform a query on its database to find the correct row to operate on. If you implement support for canonical URIs,**all** incoming calls with URIs (including this one) must perform this verification and recovery of any canonical URIs they receive. In addition, you must also implement [uncanonicalize](../android/content/ContentProvider.md))to strip the canonicalization of any of these URIs. The default implementation of this method returns null, indicating that canonical URIs are not supported. <br /> | | [ContentProvider.CallingIdentity](../android/content/ContentProvider.CallingIdentity.md) | [clearCallingIdentity](../android/content/ContentProvider.md))`()` <br /> Reset the identity of the incoming IPC on the current thread. Internally this calls [Binder.clearCallingIdentity()](../android/os/Binder.md))and also clears any value stored in [getCallingPackage()](../android/content/ContentProvider.md)). <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [delete](../android/content/ContentProvider.md))`(`uri:` ` [Uri](../android/net/Uri.md)`, `extras:` ` [Bundle](../android/os/Bundle.md)?`)` <br /> Implement this to handle requests to delete one or more rows. The implementation should apply the selection clause when performing deletion, allowing the operation to affect multiple rows in a directory. As a courtesy, call [notifyChange()](../android/content/ContentResolver.md))after deleting. This method can be called from multiple threads, as described in [Processes and Threads](https://developer.android.com/guide/topics/fundamentals/processes-and-threads.html#Threads). The implementation is responsible for parsing out a row ID at the end of the URI, if a specific row is being deleted. That is, the client would pass in`content://contacts/people/22`and the implementation is responsible for parsing the record number (22) when creating a SQL statement. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [dump](../android/content/ContentProvider.md))`(`fd:` ` [FileDescriptor](../java/io/FileDescriptor.md)!`, `writer:` ` [PrintWriter](../java/io/PrintWriter.md)!`, `args:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`)` <br /> Print the Provider's state into the given stream. This gets invoked if you run "adb shell dumpsys activity provider \<provider_component_name\>". <br /> | | [AttributionSource](../android/content/AttributionSource.md)? | [getCallingAttributionSource](../android/content/ContentProvider.md))`()` <br /> Gets the attribution source of the calling app. If you want to attribute the data access to the calling app you can create an attribution context via [android.content.Context#createContext(ContextParams)](../android/content/Context.md))and passing this identity to [ContextParams.Builder.setNextAttributionSource(](../android/content/ContextParams.Builder.md)). <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getCallingAttributionTag](../android/content/ContentProvider.md))`()` <br /> Return the attribution tag of the caller that initiated the request being processed on the current thread. Returns`null`if not currently processing a request of the request is for the default attribution. This will always return`null`when processing [getTypeAnonymous(android.net.Uri)](../android/content/ContentProvider.md))requests For [getType(android.net.Uri)](../android/content/ContentProvider.md))requests, this will be only available for cases, where the caller can be identified. See [getTypeAnonymous(android.net.Uri)](../android/content/ContentProvider.md)) <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getCallingPackage](../android/content/ContentProvider.md))`()` <br /> Return the package name of the caller that initiated the request being processed on the current thread. The returned package will have been verified to belong to the calling UID. Returns`null`if not currently processing a request. This will always return`null`when processing [getTypeAnonymous(android.net.Uri)](../android/content/ContentProvider.md))requests For [getType(android.net.Uri)](../android/content/ContentProvider.md))requests, this will be only available for cases, where the caller can be identified. See [getTypeAnonymous(android.net.Uri)](../android/content/ContentProvider.md)) <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getCallingPackageUnchecked](../android/content/ContentProvider.md))`()` <br /> Return the package name of the caller that initiated the request being processed on the current thread. The returned package will have*not* been verified to belong to the calling UID. Returns`null`if not currently processing a request. This will always return`null`when processing [getTypeAnonymous(android.net.Uri)](../android/content/ContentProvider.md))requests For [getType(android.net.Uri)](../android/content/ContentProvider.md))requests, this will be only available for cases, where the caller can be identified. See [getTypeAnonymous(android.net.Uri)](../android/content/ContentProvider.md)) <br /> | | [Context](../android/content/Context.md)? | [getContext](../android/content/ContentProvider.md))`()` <br /> Retrieves the Context this provider is running in. Only available once [onCreate](../android/content/ContentProvider.md))has been called -- this will return`null`in the constructor. <br /> | | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [PathPermission](../android/content/pm/PathPermission.md)!>? | [getPathPermissions](../android/content/ContentProvider.md))`()` <br /> Return the path-based permissions required for read and/or write access to this content provider. This method can be called from multiple threads, as described in [Processes and Threads](https://developer.android.com/guide/topics/fundamentals/processes-and-threads.html#Threads). <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getReadPermission](../android/content/ContentProvider.md))`()` <br /> Return the name of the permission required for read-only access to this content provider. This method can be called from multiple threads, as described in [Processes and Threads](https://developer.android.com/guide/topics/fundamentals/processes-and-threads.html#Threads). <br /> | | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>? | [getStreamTypes](../android/content/ContentProvider.md))`(`uri:` ` [Uri](../android/net/Uri.md)`, `mimeTypeFilter:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` <br /> Called by a client to determine the types of data streams that this content provider supports for the given URI. The default implementation returns`null`, meaning no types. If your content provider stores data of a particular type, return that MIME type if it matches the given mimeTypeFilter. If it can perform type conversions, return an array of all supported MIME types that match mimeTypeFilter. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getTypeAnonymous](../android/content/ContentProvider.md))`(`uri:` ` [Uri](../android/net/Uri.md)`)` <br /> Implement this to handle requests for MIME type of URIs, that does not need to reveal any internal information which should be protected by any permission. If your mime type reveals details that should be protected, then you should protect those by implementing those in [getType](../android/content/ContentProvider.md)), and in this function, only return types of URIs which can be obtained by anyone without any access. Implementing ths function will make sure [getType](../android/content/ContentProvider.md))is protected by readPermission. This function by default works as the [getType](../android/content/ContentProvider.md)) <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getWritePermission](../android/content/ContentProvider.md))`()` <br /> Return the name of the permission required for read/write access to this content provider. This method can be called from multiple threads, as described in [Processes and Threads](https://developer.android.com/guide/topics/fundamentals/processes-and-threads.html#Threads). <br /> | | [Uri](../android/net/Uri.md)? | [insert](../android/content/ContentProvider.md))`(`uri:` ` [Uri](../android/net/Uri.md)`, `values:` ` [ContentValues](../android/content/ContentValues.md)?`, `extras:` ` [Bundle](../android/os/Bundle.md)?`)` <br /> Implement this to handle requests to insert a new row. As a courtesy, call [notifyChange()](../android/content/ContentResolver.md))after inserting. This method can be called from multiple threads, as described in [Processes and Threads](https://developer.android.com/guide/topics/fundamentals/processes-and-threads.html#Threads). <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isTemporary](../android/content/ContentProvider.md))`()` <br /> Returns true if this instance is a temporary content provider. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onCallingPackageChanged](../android/content/ContentProvider.md))`()` <br /> Called whenever the value of [getCallingPackage()](../android/content/ContentProvider.md))changes, giving the provider an opportunity to invalidate any security related caching it may be performing. This typically happens when a [ContentProvider](../android/content/ContentProvider.md) makes a nested call back into itself when already processing a call from a remote process. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onConfigurationChanged](../android/content/ContentProvider.md))`(`newConfig:` ` [Configuration](../android/content/res/Configuration.md)`)` <br /> Called by the system when the device configuration changes while your component is running. Note that, unlike activities, other components are never restarted when a configuration changes: they must always deal with the results of the change, such as by re-retrieving resources. At the time that this function has been called, your Resources object will have been updated to return resource values matching the new configuration. For more information, read [Handling Runtime Changes](https://developer.android.com/guide/topics/resources/runtime-changes.html). This method is always called on the application main thread, and must not perform lengthy operations. The default content provider implementation does nothing. Override this method to take appropriate action. (Content providers do not usually care about things like screen orientation, but may want to know about locale changes.) <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onCreate](../android/content/ContentProvider.md))`()` <br /> Implement this to initialize your content provider on startup. This method is called for all registered content providers on the application main thread at application launch time. It must not perform lengthy operations, or application startup will be delayed. You should defer nontrivial initialization (such as opening, upgrading, and scanning databases) until the content provider is used (via #query, #insert, etc). Deferred initialization keeps application startup fast, avoids unnecessary work if the provider turns out not to be needed, and stops database errors (such as a full disk) from halting application launch. If you use SQLite, [android.database.sqlite.SQLiteOpenHelper](../android/database/sqlite/SQLiteOpenHelper.md) is a helpful utility class that makes it easy to manage databases, and will automatically defer opening until first use. If you do use SQLiteOpenHelper, make sure to avoid calling [android.database.sqlite.SQLiteOpenHelper#getReadableDatabase](../android/database/sqlite/SQLiteOpenHelper.md))or [android.database.sqlite.SQLiteOpenHelper#getWritableDatabase](../android/database/sqlite/SQLiteOpenHelper.md))from this method. (Instead, override [android.database.sqlite.SQLiteOpenHelper#onOpen](../android/database/sqlite/SQLiteOpenHelper.md))to initialize the database when it is first opened.) <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onLowMemory](../android/content/ContentProvider.md))`()` <br /> This is called when the overall system is running low on memory, and actively running processes should trim their memory usage. While the exact point at which this will be called is not defined, generally it will happen when all background process have been killed. That is, before reaching the point of killing processes hosting service and foreground UI that we would like to avoid killing. This method is always called on the application main thread, and must not perform lengthy operations. The default content provider implementation does nothing. Subclasses may override this method to take appropriate action. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onTrimMemory](../android/content/ContentProvider.md))`(`level:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> | | [AssetFileDescriptor](../android/content/res/AssetFileDescriptor.md)? | [openAssetFile](../android/content/ContentProvider.md))`(`uri:` ` [Uri](../android/net/Uri.md)`, `mode:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` <br /> This is like #openFile, but can be implemented by providers that need to be able to return sub-sections of files, often assets inside of their .apk. This method can be called from multiple threads, as described in [Processes and Threads](https://developer.android.com/guide/topics/fundamentals/processes-and-threads.html#Threads). If you implement this, your clients must be able to deal with such file slices, either directly with android.content.ContentResolver#openAssetFileDescriptor, or by using the higher-level [ContentResolver.openInputStream](../android/content/ContentResolver.md))or android.content.ContentResolver#openOutputStream methods. The returned AssetFileDescriptor can be a pipe or socket pair to enable streaming of data. If you are implementing this to return a full file, you should create the AssetFileDescriptor with [AssetFileDescriptor.UNKNOWN_LENGTH](../android/content/res/AssetFileDescriptor.md) to be compatible with applications that cannot handle sub-sections of files. For use in Intents, you will want to implement [getType](../android/content/ContentProvider.md))to return the appropriate MIME type for the data returned here with the same URI. This will allow intent resolution to automatically determine the data MIME type and select the appropriate matching targets as part of its operation. For better interoperability with other applications, it is recommended that for any URIs that can be opened, you also support queries on them containing at least the columns specified by [android.provider.OpenableColumns](../android/provider/OpenableColumns.md). <br /> | | [AssetFileDescriptor](../android/content/res/AssetFileDescriptor.md)? | [openAssetFile](../android/content/ContentProvider.md))`(`uri:` ` [Uri](../android/net/Uri.md)`, `mode:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `signal:` ` [CancellationSignal](../android/os/CancellationSignal.md)?`)` <br /> This is like #openFile, but can be implemented by providers that need to be able to return sub-sections of files, often assets inside of their .apk. This method can be called from multiple threads, as described in [Processes and Threads](https://developer.android.com/guide/topics/fundamentals/processes-and-threads.html#Threads). If you implement this, your clients must be able to deal with such file slices, either directly with android.content.ContentResolver#openAssetFileDescriptor, or by using the higher-level [ContentResolver.openInputStream](../android/content/ContentResolver.md))or android.content.ContentResolver#openOutputStream methods. The returned AssetFileDescriptor can be a pipe or socket pair to enable streaming of data. If you are implementing this to return a full file, you should create the AssetFileDescriptor with [AssetFileDescriptor.UNKNOWN_LENGTH](../android/content/res/AssetFileDescriptor.md) to be compatible with applications that cannot handle sub-sections of files. For use in Intents, you will want to implement [getType](../android/content/ContentProvider.md))to return the appropriate MIME type for the data returned here with the same URI. This will allow intent resolution to automatically determine the data MIME type and select the appropriate matching targets as part of its operation. For better interoperability with other applications, it is recommended that for any URIs that can be opened, you also support queries on them containing at least the columns specified by [android.provider.OpenableColumns](../android/provider/OpenableColumns.md). <br /> | | [ParcelFileDescriptor](../android/os/ParcelFileDescriptor.md)? | [openFile](../android/content/ContentProvider.md))`(`uri:` ` [Uri](../android/net/Uri.md)`, `mode:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` <br /> Override this to handle requests to open a file blob. The default implementation always throws [FileNotFoundException](../java/io/FileNotFoundException.md). This method can be called from multiple threads, as described in [Processes and Threads](https://developer.android.com/guide/topics/fundamentals/processes-and-threads.html#Threads). This method returns a ParcelFileDescriptor, which is returned directly to the caller. This way large data (such as images and documents) can be returned without copying the content. The returned ParcelFileDescriptor is owned by the caller, so it is their responsibility to close it when done. That is, the implementation of this method should create a new ParcelFileDescriptor for each call. If opened with the exclusive "r" or "w" modes, the returned ParcelFileDescriptor can be a pipe or socket pair to enable streaming of data. Opening with the "rw" or "rwt" modes implies a file on disk that supports seeking. If you need to detect when the returned ParcelFileDescriptor has been closed, or if the remote process has crashed or encountered some other error, you can use [ParcelFileDescriptor.open(File, int,](../android/os/ParcelFileDescriptor.md)), [ParcelFileDescriptor.createReliablePipe()](../android/os/ParcelFileDescriptor.md)), or [ParcelFileDescriptor.createReliableSocketPair()](../android/os/ParcelFileDescriptor.md)). If you need to return a large file that isn't backed by a real file on disk, such as a file on a network share or cloud storage service, consider using [StorageManager.openProxyFileDescriptor(int, android.os.ProxyFileDescriptorCallback, android.os.Handler)](../android/os/storage/StorageManager.md))which will let you to stream the content on-demand. For use in Intents, you will want to implement [getType](../android/content/ContentProvider.md))to return the appropriate MIME type for the data returned here with the same URI. This will allow intent resolution to automatically determine the data MIME type and select the appropriate matching targets as part of its operation. For better interoperability with other applications, it is recommended that for any URIs that can be opened, you also support queries on them containing at least the columns specified by [android.provider.OpenableColumns](../android/provider/OpenableColumns.md). You may also want to support other common columns if you have additional meta-data to supply, such as [android.provider.MediaStore.MediaColumns#DATE_ADDED](../android/provider/MediaStore.MediaColumns.md) in [android.provider.MediaStore.MediaColumns](../android/provider/MediaStore.MediaColumns.md). <br /> | | [ParcelFileDescriptor](../android/os/ParcelFileDescriptor.md)? | [openFile](../android/content/ContentProvider.md))`(`uri:` ` [Uri](../android/net/Uri.md)`, `mode:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `signal:` ` [CancellationSignal](../android/os/CancellationSignal.md)?`)` <br /> Override this to handle requests to open a file blob. The default implementation always throws [FileNotFoundException](../java/io/FileNotFoundException.md). This method can be called from multiple threads, as described in [Processes and Threads](https://developer.android.com/guide/topics/fundamentals/processes-and-threads.html#Threads). This method returns a ParcelFileDescriptor, which is returned directly to the caller. This way large data (such as images and documents) can be returned without copying the content. The returned ParcelFileDescriptor is owned by the caller, so it is their responsibility to close it when done. That is, the implementation of this method should create a new ParcelFileDescriptor for each call. If opened with the exclusive "r" or "w" modes, the returned ParcelFileDescriptor can be a pipe or socket pair to enable streaming of data. Opening with the "rw" or "rwt" modes implies a file on disk that supports seeking. If you need to detect when the returned ParcelFileDescriptor has been closed, or if the remote process has crashed or encountered some other error, you can use [ParcelFileDescriptor.open(File, int,](../android/os/ParcelFileDescriptor.md)), [ParcelFileDescriptor.createReliablePipe()](../android/os/ParcelFileDescriptor.md)), or [ParcelFileDescriptor.createReliableSocketPair()](../android/os/ParcelFileDescriptor.md)). For use in Intents, you will want to implement [getType](../android/content/ContentProvider.md))to return the appropriate MIME type for the data returned here with the same URI. This will allow intent resolution to automatically determine the data MIME type and select the appropriate matching targets as part of its operation. For better interoperability with other applications, it is recommended that for any URIs that can be opened, you also support queries on them containing at least the columns specified by [android.provider.OpenableColumns](../android/provider/OpenableColumns.md). You may also want to support other common columns if you have additional meta-data to supply, such as [android.provider.MediaStore.MediaColumns#DATE_ADDED](../android/provider/MediaStore.MediaColumns.md) in [android.provider.MediaStore.MediaColumns](../android/provider/MediaStore.MediaColumns.md). <br /> | | [ParcelFileDescriptor](../android/os/ParcelFileDescriptor.md) | [openFileHelper](../android/content/ContentProvider.md))`(`uri:` ` [Uri](../android/net/Uri.md)`, `mode:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` <br /> Convenience for subclasses that wish to implement #openFile by looking up a column named "_data" at the given URI. <br /> | | [ParcelFileDescriptor](../android/os/ParcelFileDescriptor.md) | [openPipeHelper](../android/content/ContentProvider.md))`(`uri:` ` [Uri](../android/net/Uri.md)`, `mimeType:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `opts:` ` [Bundle](../android/os/Bundle.md)?`, `args:` `T?`, `func:` ` [ContentProvider.PipeDataWriter](../android/content/ContentProvider.PipeDataWriter.md)<T>`)` <br /> A helper function for implementing #openTypedAssetFile, for creating a data pipe and background thread allowing you to stream generated data back to the client. This function returns a new ParcelFileDescriptor that should be returned to the caller (the caller is responsible for closing it). <br /> | | [AssetFileDescriptor](../android/content/res/AssetFileDescriptor.md)? | [openTypedAssetFile](../android/content/ContentProvider.md))`(`uri:` ` [Uri](../android/net/Uri.md)`, `mimeTypeFilter:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `opts:` ` [Bundle](../android/os/Bundle.md)?`)` <br /> Called by a client to open a read-only stream containing data of a particular MIME type. This is like [openAssetFile(android.net.Uri,java.lang.String)](../android/content/ContentProvider.md)), except the file can only be read-only and the content provider may perform data conversions to generate data of the desired type. The default implementation compares the given mimeType against the result of [getType(android.net.Uri)](../android/content/ContentProvider.md))and, if they match, simply calls [openAssetFile(android.net.Uri,java.lang.String)](../android/content/ContentProvider.md)). See [ClipData](../android/content/ClipData.md) for examples of the use and implementation of this method. The returned AssetFileDescriptor can be a pipe or socket pair to enable streaming of data. For better interoperability with other applications, it is recommended that for any URIs that can be opened, you also support queries on them containing at least the columns specified by [android.provider.OpenableColumns](../android/provider/OpenableColumns.md). You may also want to support other common columns if you have additional meta-data to supply, such as [android.provider.MediaStore.MediaColumns#DATE_ADDED](../android/provider/MediaStore.MediaColumns.md) in [android.provider.MediaStore.MediaColumns](../android/provider/MediaStore.MediaColumns.md). <br /> | | [AssetFileDescriptor](../android/content/res/AssetFileDescriptor.md)? | [openTypedAssetFile](../android/content/ContentProvider.md))`(`uri:` ` [Uri](../android/net/Uri.md)`, `mimeTypeFilter:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `opts:` ` [Bundle](../android/os/Bundle.md)?`, `signal:` ` [CancellationSignal](../android/os/CancellationSignal.md)?`)` <br /> Called by a client to open a read-only stream containing data of a particular MIME type. This is like [openAssetFile(android.net.Uri,java.lang.String)](../android/content/ContentProvider.md)), except the file can only be read-only and the content provider may perform data conversions to generate data of the desired type. The default implementation compares the given mimeType against the result of [getType(android.net.Uri)](../android/content/ContentProvider.md))and, if they match, simply calls [openAssetFile(android.net.Uri,java.lang.String)](../android/content/ContentProvider.md)). See [ClipData](../android/content/ClipData.md) for examples of the use and implementation of this method. The returned AssetFileDescriptor can be a pipe or socket pair to enable streaming of data. For better interoperability with other applications, it is recommended that for any URIs that can be opened, you also support queries on them containing at least the columns specified by [android.provider.OpenableColumns](../android/provider/OpenableColumns.md). You may also want to support other common columns if you have additional meta-data to supply, such as [android.provider.MediaStore.MediaColumns#DATE_ADDED](../android/provider/MediaStore.MediaColumns.md) in [android.provider.MediaStore.MediaColumns](../android/provider/MediaStore.MediaColumns.md). <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [refresh](../android/content/ContentProvider.md))`(`uri:` ` [Uri](../android/net/Uri.md)!`, `extras:` ` [Bundle](../android/os/Bundle.md)?`, `cancellationSignal:` ` [CancellationSignal](../android/os/CancellationSignal.md)?`)` <br /> Implement this to support refresh of content identified by`uri`. By default, this method returns false; providers who wish to implement this should return true to signal the client that the provider has tried refreshing with its own implementation. This allows clients to request an explicit refresh of content identified by`uri`. Client code should only invoke this method when there is a strong indication (such as a user initiated pull to refresh gesture) that the content is stale. Remember to send [ContentResolver.notifyChange(Uri, android.database.ContentObserver)](../android/content/ContentResolver.md))notifications when content changes. <br /> | | [Context](../android/content/Context.md) | [requireContext](../android/content/ContentProvider.md))`()` <br /> Retrieves a Non-Nullable Context this provider is running in, this is intended to be called after [onCreate](../android/content/ContentProvider.md)). When called before context was created, an IllegalStateException will be thrown. Note A provider must be declared in the manifest and created automatically by the system, and context is only available after [onCreate](../android/content/ContentProvider.md))is called. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [restoreCallingIdentity](../android/content/ContentProvider.md))`(`identity:` ` [ContentProvider.CallingIdentity](../android/content/ContentProvider.CallingIdentity.md)`)` <br /> Restore the identity of the incoming IPC on the current thread back to a previously identity that was returned by [clearCallingIdentity](../android/content/ContentProvider.md)). Internally this calls [Binder.restoreCallingIdentity(long)](../android/os/Binder.md))and also restores any value stored in [getCallingPackage()](../android/content/ContentProvider.md)). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPathPermissions](../android/content/ContentProvider.md))`(`permissions:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [PathPermission](../android/content/pm/PathPermission.md)!>?`)` <br /> Change the path-based permission required to read and/or write data in the content provider. This is normally set for you from its manifest information when the provider is first created. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setReadPermission](../android/content/ContentProvider.md))`(`permission:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` <br /> Change the permission required to read data from the content provider. This is normally set for you from its manifest information when the provider is first created. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setWritePermission](../android/content/ContentProvider.md))`(`permission:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` <br /> Change the permission required to read and write data in the content provider. This is normally set for you from its manifest information when the provider is first created. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [shutdown](../android/content/ContentProvider.md))`()` <br /> Implement this to shut down the ContentProvider instance. You can then invoke this method in unit tests. Android normally handles ContentProvider startup and shutdown automatically. You do not need to start up or shut down a ContentProvider. When you invoke a test method on a ContentProvider, however, a ContentProvider instance is started and keeps running after the test finishes, even if a succeeding test instantiates another ContentProvider. A conflict develops because the two instances are usually running against the same underlying data source (for example, an sqlite database). Implementing shutDown() avoids this conflict by providing a way to terminate the ContentProvider. This method can also prevent memory leaks from multiple instantiations of the ContentProvider, and it can ensure unit test isolation by allowing you to completely clean up the test fixture before moving on to the next test. <br /> | | [Uri](../android/net/Uri.md)? | [uncanonicalize](../android/content/ContentProvider.md))`(`url:` ` [Uri](../android/net/Uri.md)`)` <br /> Remove canonicalization from canonical URIs previously returned by [canonicalize](../android/content/ContentProvider.md)). For example, if your implementation is to add a query param to canonicalize a URI, this method can simply trip any query params on the URI. The default implementation always returns the same url that was passed in. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [update](../android/content/ContentProvider.md))`(`uri:` ` [Uri](../android/net/Uri.md)`, `values:` ` [ContentValues](../android/content/ContentValues.md)?`, `extras:` ` [Bundle](../android/os/Bundle.md)?`)` <br /> Implement this to handle requests to update one or more rows. The implementation should update all rows matching the selection to set the columns according to the provided values map. As a courtesy, call [notifyChange()](../android/content/ContentResolver.md))after updating. This method can be called from multiple threads, as described in [Processes and Threads](https://developer.android.com/guide/topics/fundamentals/processes-and-threads.html#Threads). <br /> | ||
| From class [ComponentCallbacks](../android/content/ComponentCallbacks.md) |------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onConfigurationChanged](../android/content/ComponentCallbacks.md))`(`newConfig:` ` [Configuration](../android/content/res/Configuration.md)`)` <br /> Called by the system when the device configuration changes while your component is running. Note that, unlike activities, other components are never restarted when a configuration changes: they must always deal with the results of the change, such as by re-retrieving resources. At the time that this function has been called, your Resources object will have been updated to return resource values matching the new configuration. For more information, read [Handling Runtime Changes](https://developer.android.com/guide/topics/resources/runtime-changes.html). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onLowMemory](../android/content/ComponentCallbacks.md))`()` <br /> This is called when the overall system is running low on memory, and actively running processes should trim their memory usage. While the exact point at which this will be called is not defined, generally it will happen when all background process have been killed. That is, before reaching the point of killing processes hosting service and foreground UI that we would like to avoid killing. <br /> | ||

## Constants

### SLICE_TYPE

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SLICE_TYPE: String
```

**Deprecated:** *Deprecated in Java.*

This is the Android platform's MIME type for a URI containing a slice implemented through [SliceProvider](../android/app/slice/SliceProvider.md). 

 Value: "vnd.android.slice"

## Public constructors

### SliceProvider

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SliceProvider()
```  

### SliceProvider

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SliceProvider(vararg autoGrantPermissions: String!)
```

A version of constructing a SliceProvider that allows autogranting slice permissions to apps that hold specific platform permissions.

When an app tries to bind a slice from this provider that it does not have access to, This provider will check if the caller holds permissions to any of the autoGrantPermissions specified, if they do they will be granted persisted uri access to all slices of this provider.

| Parameters ||
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `autoGrantPermissions` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:List of permissions that holders are auto-granted access to slices. This value cannot be`null`. |

## Public methods

### attachInfo

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun attachInfo(
    context: Context!, 
    info: ProviderInfo!
): Unit
```

**Deprecated:** *Deprecated in Java.*

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android/content/Context.md)!:The context this provider is running in |
| `info` | [ProviderInfo](../android/content/pm/ProviderInfo.md)!:Registered information about this content provider |

### call

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun call(
    method: String, 
    arg: String?, 
    extras: Bundle?
): Bundle?
```

**Deprecated:** *Deprecated in Java.*

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------|
| `method` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):This value cannot be`null`. |
| `arg` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:This value may be`null`. |
| `extras` | [Bundle](../android/os/Bundle.md)?:This value may be`null`. |
| --- | --- |

| Return ||
|-----------------------------------------------------------------------------------|--------------------------|
| [Bundle](../android/os/Bundle.md)? | This value may be`null`. |

### delete

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun delete(
    uri: Uri, 
    selection: String?, 
    selectionArgs: Array<String!>?
): Int
```

**Deprecated:** *Deprecated in Java.*

| Parameters ||
|-----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `uri` | [Uri](../android/net/Uri.md):The full URI to query, including a row ID (if a specific record is requested). This value cannot be`null`. |
| `selection` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:An optional restriction to apply to rows when deleting. This value may be`null`. |
| `selectionArgs` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>?:This value may be`null`. |
| --- | --- |

| Return ||
|----------------------------------------------------------------------------|------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The number of rows affected. |

| Exceptions ||
|---------------------------------|---|
| `android.database.SQLException` | |

### getType

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getType(uri: Uri): String?
```

**Deprecated:** *Deprecated in Java.*

| Parameters ||
|-------|---------------------------------------------------------------------------------------------------------------------------|
| `uri` | [Uri](../android/net/Uri.md):the URI to query. This value cannot be`null`. |

| Return ||
|-----------------------------------------------------------------------------------|--------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | a MIME type string, or`null`if there is no type. |

### insert

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun insert(
    uri: Uri, 
    values: ContentValues?
): Uri?
```

**Deprecated:** *Deprecated in Java.*

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `uri` | [Uri](../android/net/Uri.md):The content:// URI of the insertion request. This value cannot be`null`. |
| `values` | [ContentValues](../android/content/ContentValues.md)?:A set of column_name/value pairs to add to the database. This value may be`null`. |

| Return ||
|------------------------------------------------------------------------------|---------------------------------------------------------------|
| [Uri](../android/net/Uri.md)? | The URI for the newly inserted item. This value may be`null`. |

### onBindSlice

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onBindSlice(
    sliceUri: Uri!, 
    supportedSpecs: MutableSet<SliceSpec!>!
): Slice!
```

**Deprecated:** *Deprecated in Java.*

Implemented to create a slice.

onBindSlice should return as quickly as possible so that the UI tied to this slice can be responsive. No network or other IO will be allowed during onBindSlice. Any loading that needs to be done should happen in the background with a call to [ContentResolver.notifyChange(Uri, ContentObserver)](../android/content/ContentResolver.md))when the app is ready to provide the complete data in onBindSlice.

The slice returned should have a spec that is compatible with one of the supported specs.

| Parameters ||
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `sliceUri` | [Uri](../android/net/Uri.md)!:Uri to bind. |
| `supportedSpecs` | [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [SliceSpec](../android/app/slice/SliceSpec.md)!\>!:List of supported specs. |

**See Also**

- [android.app.slice.Slice](../android/app/slice/Slice.md)
- [android.app.slice.Slice#HINT_PARTIAL](../android/app/slice/Slice.md) 

### onCreatePermissionRequest

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onCreatePermissionRequest(sliceUri: Uri!): PendingIntent
```

**Deprecated:** *Deprecated in Java.*

Called when an app requests a slice it does not have write permission to the uri for.

The return value will be the action on a slice that prompts the user that the calling app wants to show slices from this app. The default implementation launches a dialog that allows the user to grant access to this slice. Apps that do not want to allow this user grant, can override this and instead launch their own dialog with different behavior.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------|
| `sliceUri` | [Uri](../android/net/Uri.md)!:the Uri of the slice attempting to be bound. |

| Return ||
|-------------------------------------------------------------------------------------------------|-----------------------------|
| [PendingIntent](../android/app/PendingIntent.md) | This value cannot be`null`. |

**See Also**

- [#getCallingPackage()](../android/content/ContentProvider.md)) 

### onGetSliceDescendants

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onGetSliceDescendants(uri: Uri): MutableCollection<Uri!>
```

**Deprecated:** *Deprecated in Java.*

Obtains a list of slices that are descendants of the specified Uri.

Implementing this is optional for a SliceProvider, but does provide a good discovery mechanism for finding slice Uris.

| Parameters ||
|-------|------------------------------------------------------------------------------------------------------------------------------------------------|
| `uri` | [Uri](../android/net/Uri.md):The uri to look for descendants under. This value cannot be`null`. |

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)< [Uri](../android/net/Uri.md)!> | All slices within the space. This value cannot be`null`. |

**See Also**

- [android.app.slice.SliceManager#getSliceDescendants(Uri)](../android/app/slice/SliceManager.md)) 

### onMapIntentToUri

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onMapIntentToUri(intent: Intent!): Uri
```

**Deprecated:** *Deprecated in Java.*

This method must be overridden if an [IntentFilter](../android/content/IntentFilter.md) is specified on the SliceProvider. In that case, this method can be called and is expected to return a non-null Uri representing a slice. Otherwise this will throw [UnsupportedOperationException](../java/lang/UnsupportedOperationException.md). Any intent filter added to a slice provider should also contain [SliceManager.CATEGORY_SLICE](../android/app/slice/SliceManager.md), because otherwise it will not be detected by [SliceManager.mapIntentToUri(Intent)](../android/app/slice/SliceManager.md)).

| Return ||
|-----------------------------------------------------------------------------|-----------------------------------------------------------------|
| [Uri](../android/net/Uri.md) | Uri representing the slice associated with the provided intent. |

**See Also**

- [android.app.slice.Slice](../android/app/slice/Slice.md)
- [android.app.slice.SliceManager#mapIntentToUri(Intent)](../android/app/slice/SliceManager.md)) 

### onSlicePinned

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onSlicePinned(sliceUri: Uri!): Unit
```

**Deprecated:** *Deprecated in Java.*

Called to inform an app that a slice has been pinned.

Pinning is a way that slice hosts use to notify apps of which slices they care about updates for. When a slice is pinned the content is expected to be relatively fresh and kept up to date.

Being pinned does not provide any escalated privileges for the slice provider. So apps should do things such as turn on syncing or schedule a job in response to a onSlicePinned.

Pinned state is not persisted through a reboot, and apps can expect a new call to onSlicePinned for any slices that should remain pinned after a reboot occurs.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------|
| `sliceUri` | [Uri](../android/net/Uri.md)!:The uri of the slice being unpinned. |

**See Also**

- [#onSliceUnpinned(Uri)](../android/app/slice/SliceProvider.md)) 

### onSliceUnpinned

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onSliceUnpinned(sliceUri: Uri!): Unit
```

**Deprecated:** *Deprecated in Java.*

Called to inform an app that a slices is no longer pinned.

This means that no other apps on the device care about updates to this slice anymore and therefore it is not important to be updated. Any syncs or jobs related to this slice should be cancelled. 
**See Also**

- [#onSlicePinned(Uri)](../android/app/slice/SliceProvider.md)) 

### query

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun query(
    uri: Uri, 
    projection: Array<String!>?, 
    queryArgs: Bundle?, 
    cancellationSignal: CancellationSignal?
): Cursor?
```

**Deprecated:** *Deprecated in Java.*

| Parameters ||
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `uri` | [Uri](../android/net/Uri.md):The URI to query. This will be the full URI sent by the client. This value cannot be`null`. |
| `projection` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>?:The list of columns to put into the cursor. If`null`provide a default set of columns. |
| `queryArgs` | [Bundle](../android/os/Bundle.md)?:A Bundle containing additional information necessary for the operation. Arguments may include SQL style arguments, such as [ContentResolver.QUERY_ARG_SQL_LIMIT](../android/content/ContentResolver.md), but note that the documentation for each individual provider will indicate which arguments they support. This value may be`null`. |
| --- | --- |
| `cancellationSignal` | [CancellationSignal](../android/os/CancellationSignal.md)?:A signal to cancel the operation in progress, or`null`. |

| Return ||
|-----------------------------------------------------------------------------------------|--------------------|
| [Cursor](../android/database/Cursor.md)? | a Cursor or`null`. |

### query

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun query(
    uri: Uri, 
    projection: Array<String!>?, 
    selection: String?, 
    selectionArgs: Array<String!>?, 
    sortOrder: String?
): Cursor?
```

**Deprecated:** *Deprecated in Java.*

| Parameters ||
|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `uri` | [Uri](../android/net/Uri.md):The URI to query. This will be the full URI sent by the client; if the client is requesting a specific record, the URI will end in a record number that the implementation should parse and add to a WHERE or HAVING clause, specifying that _id value. This value cannot be`null`. |
| `projection` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>?:The list of columns to put into the cursor. If`null`all columns are included. |
| `selection` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:A selection criteria to apply when filtering rows. If`null`then all rows are included. |
| --- | --- |
| `selectionArgs` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>?:You may include ?s in selection, which will be replaced by the values from selectionArgs, in order that they appear in the selection. The values will be bound as Strings. This value may be`null`. |
| `sortOrder` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:How the rows in the cursor should be sorted. If`null`then the provider is free to define the sort order. |

| Return ||
|-----------------------------------------------------------------------------------------|--------------------|
| [Cursor](../android/database/Cursor.md)? | a Cursor or`null`. |

### query

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun query(
    uri: Uri, 
    projection: Array<String!>?, 
    selection: String?, 
    selectionArgs: Array<String!>?, 
    sortOrder: String?, 
    cancellationSignal: CancellationSignal?
): Cursor?
```

**Deprecated:** *Deprecated in Java.*

| Parameters ||
|----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `uri` | [Uri](../android/net/Uri.md):The URI to query. This will be the full URI sent by the client; if the client is requesting a specific record, the URI will end in a record number that the implementation should parse and add to a WHERE or HAVING clause, specifying that _id value. This value cannot be`null`. |
| `projection` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>?:The list of columns to put into the cursor. If`null`all columns are included. |
| `selection` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:A selection criteria to apply when filtering rows. If`null`then all rows are included. |
| --- | --- |
| `selectionArgs` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>?:You may include ?s in selection, which will be replaced by the values from selectionArgs, in order that they appear in the selection. The values will be bound as Strings. This value may be`null`. |
| `sortOrder` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:How the rows in the cursor should be sorted. If`null`then the provider is free to define the sort order. |
| `cancellationSignal` | [CancellationSignal](../android/os/CancellationSignal.md)?:A signal to cancel the operation in progress, or`null`if none. If the operation is canceled, then [android.os.OperationCanceledException](../android/os/OperationCanceledException.md) will be thrown when the query is executed. |
| --- | --- |

| Return ||
|-----------------------------------------------------------------------------------------|--------------------|
| [Cursor](../android/database/Cursor.md)? | a Cursor or`null`. |

### update

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun update(
    uri: Uri, 
    values: ContentValues?, 
    selection: String?, 
    selectionArgs: Array<String!>?
): Int
```

**Deprecated:** *Deprecated in Java.*

| Parameters ||
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `uri` | [Uri](../android/net/Uri.md):The URI to query. This can potentially have a record ID if this is an update request for a specific record. This value cannot be`null`. |
| `values` | [ContentValues](../android/content/ContentValues.md)?:A set of column_name/value pairs to update in the database. This value may be`null`. |
| `selection` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:An optional filter to match rows to update. This value may be`null`. |
| --- | --- |
| `selectionArgs` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>?:This value may be`null`. |

| Return ||
|----------------------------------------------------------------------------|------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of rows affected. |
