# SliceProvider

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SliceProvider

Kotlin| [Java](https://developer.android.com/reference/android/app/slice/SliceProvider "View this page in Java") 
| --- | --- |

```
abstract class SliceProvider : ContentProvider
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.content.ContentProvider](https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#) ||
| | ↳ | [android.app.slice.SliceProvider](https://developer.android.com/reference/kotlin/android/app/slice/SliceProvider#) |

| **This class was deprecated in API level 35.**
|
| Slice framework has been deprecated, it will not receive any updates from android.os.Build.VANILLA_ICE_CREAM and forward. If you are looking for a framework that sends displayable data from one app to another, consider using [android.app.appsearch.AppSearchManager](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchManager.html#).

A SliceProvider allows an app to provide content to be displayed in system spaces. This content is templated and can contain actions, and the behavior of how it is surfaced is specific to the system surface.

Slices are not currently live content. They are bound once and shown to the user. If the content changes due to a callback from user interaction, then [ContentResolver.notifyChange(Uri, ContentObserver)](https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#notifyChange(android.net.Uri,%20android.database.ContentObserver))should be used to notify the system.

The provider needs to be declared in the manifest to provide the authority for the app. The authority for most slices is expected to match the package of the application. 

```kotlin
<provider
      android:name="com.example.mypkg.MySliceProvider"
      android:authorities="com.example.mypkg" />
  
```

Slices can be identified by a Uri or by an Intent. To link an Intent with a slice, the provider must have an [IntentFilter](https://developer.android.com/reference/kotlin/android/content/IntentFilter.html#) matching the slice intent. When a slice is being requested via an intent, [onMapIntentToUri(android.content.Intent)](https://developer.android.com/reference/kotlin/android/app/slice/SliceProvider#onMapIntentToUri(android.content.Intent))can be called and is expected to return an appropriate Uri representing the slice. 

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
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SLICE_TYPE](https://developer.android.com/reference/kotlin/android/app/slice/SliceProvider#SLICE_TYPE:kotlin.String) This is the Android platform's MIME type for a URI containing a slice implemented through [SliceProvider](https://developer.android.com/reference/kotlin/android/app/slice/SliceProvider#). |

| Inherited constants ||
|---|---|
| From class [ComponentCallbacks2](https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#) |----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TRIM_MEMORY_BACKGROUND](https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#TRIM_MEMORY_BACKGROUND:kotlin.Int) <br /> Level for [onTrimMemory(int)](https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#onTrimMemory(kotlin.Int)): the process has gone on to the LRU list. This is a good opportunity to clean up resources that can efficiently and quickly be re-built if the user returns to the app. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TRIM_MEMORY_COMPLETE](https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#TRIM_MEMORY_COMPLETE:kotlin.Int) <br /> Level for [onTrimMemory(int)](https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#onTrimMemory(kotlin.Int)): the process is nearing the end of the background LRU list, and if more memory isn't found soon it will be killed. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TRIM_MEMORY_MODERATE](https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#TRIM_MEMORY_MODERATE:kotlin.Int) <br /> Level for [onTrimMemory(int)](https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#onTrimMemory(kotlin.Int)): the process is around the middle of the background LRU list; freeing memory can help the system keep other processes running later in the list for better overall performance. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TRIM_MEMORY_RUNNING_CRITICAL](https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#TRIM_MEMORY_RUNNING_CRITICAL:kotlin.Int) <br /> Level for [onTrimMemory(int)](https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#onTrimMemory(kotlin.Int)): the process is not an expendable background process, but the device is running extremely low on memory and is about to not be able to keep any background processes running. Your running process should free up as many non-critical resources as it can to allow that memory to be used elsewhere. The next thing that will happen after this is [onLowMemory()](https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks.html#onLowMemory())called to report that nothing at all can be kept in the background, a situation that can start to notably impact the user. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TRIM_MEMORY_RUNNING_LOW](https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#TRIM_MEMORY_RUNNING_LOW:kotlin.Int) <br /> Level for [onTrimMemory(int)](https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#onTrimMemory(kotlin.Int)): the process is not an expendable background process, but the device is running low on memory. Your running process should free up unneeded resources to allow that memory to be used elsewhere. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TRIM_MEMORY_RUNNING_MODERATE](https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#TRIM_MEMORY_RUNNING_MODERATE:kotlin.Int) <br /> Level for [onTrimMemory(int)](https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#onTrimMemory(kotlin.Int)): the process is not an expendable background process, but the device is running moderately low on memory. Your running process may want to release some unneeded resources for use elsewhere. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TRIM_MEMORY_UI_HIDDEN](https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#TRIM_MEMORY_UI_HIDDEN:kotlin.Int) <br /> Level for [onTrimMemory(int)](https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#onTrimMemory(kotlin.Int)): the process had been showing a user interface, and is no longer doing so. Large allocations with the UI should be released at this point to allow memory to be better managed. <br /> | ||

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SliceProvider](https://developer.android.com/reference/kotlin/android/app/slice/SliceProvider#SliceProvider())`()` <br /> |
| [SliceProvider](https://developer.android.com/reference/kotlin/android/app/slice/SliceProvider#SliceProvider(kotlin.String))`(`vararg` `autoGrantPermissions:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` A version of constructing a SliceProvider that allows autogranting slice permissions to apps that hold specific platform permissions. |

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [attachInfo](https://developer.android.com/reference/kotlin/android/app/slice/SliceProvider#attachInfo(android.content.Context,%20android.content.pm.ProviderInfo))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`, `info:` ` [ProviderInfo](https://developer.android.com/reference/kotlin/android/content/pm/ProviderInfo.html#)!`)` <br /> |
| open [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)? | [call](https://developer.android.com/reference/kotlin/android/app/slice/SliceProvider#call(kotlin.String,%20kotlin.String,%20android.os.Bundle))`(`method:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `arg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `extras:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)?`)` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [delete](https://developer.android.com/reference/kotlin/android/app/slice/SliceProvider#delete(android.net.Uri,%20kotlin.String,%20kotlin.Array))`(`uri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)`, `selection:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `selectionArgs:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>?`)` <br /> |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getType](https://developer.android.com/reference/kotlin/android/app/slice/SliceProvider#getType(android.net.Uri))`(`uri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)`)` <br /> |
| [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)? | [insert](https://developer.android.com/reference/kotlin/android/app/slice/SliceProvider#insert(android.net.Uri,%20android.content.ContentValues))`(`uri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)`, `values:` ` [ContentValues](https://developer.android.com/reference/kotlin/android/content/ContentValues.html#)?`)` <br /> |
| open [Slice](https://developer.android.com/reference/kotlin/android/app/slice/Slice)! | [onBindSlice](https://developer.android.com/reference/kotlin/android/app/slice/SliceProvider#onBindSlice(android.net.Uri,%20kotlin.collections.MutableSet))`(`sliceUri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)!`, `supportedSpecs:` ` [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [SliceSpec](https://developer.android.com/reference/kotlin/android/app/slice/SliceSpec)!>!`)` Implemented to create a slice. |
| --- | --- |
| open [PendingIntent](https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#) | [onCreatePermissionRequest](https://developer.android.com/reference/kotlin/android/app/slice/SliceProvider#onCreatePermissionRequest(android.net.Uri))`(`sliceUri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)!`)` Called when an app requests a slice it does not have write permission to the uri for. |
| open [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\< [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)!\> | [onGetSliceDescendants](https://developer.android.com/reference/kotlin/android/app/slice/SliceProvider#onGetSliceDescendants(android.net.Uri))`(`uri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)`)` Obtains a list of slices that are descendants of the specified Uri. |
| open [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#) | [onMapIntentToUri](https://developer.android.com/reference/kotlin/android/app/slice/SliceProvider#onMapIntentToUri(android.content.Intent))`(`intent:` ` [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#)!`)` This method must be overridden if an [IntentFilter](https://developer.android.com/reference/kotlin/android/content/IntentFilter.html#) is specified on the SliceProvider. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onSlicePinned](https://developer.android.com/reference/kotlin/android/app/slice/SliceProvider#onSlicePinned(android.net.Uri))`(`sliceUri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)!`)` Called to inform an app that a slice has been pinned. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onSliceUnpinned](https://developer.android.com/reference/kotlin/android/app/slice/SliceProvider#onSliceUnpinned(android.net.Uri))`(`sliceUri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)!`)` Called to inform an app that a slices is no longer pinned. |
| [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#)? | [query](https://developer.android.com/reference/kotlin/android/app/slice/SliceProvider#query(android.net.Uri,%20kotlin.Array,%20android.os.Bundle,%20android.os.CancellationSignal))`(`uri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)`, `projection:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>?`, `queryArgs:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)?`, `cancellationSignal:` ` [CancellationSignal](https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#)?`)` <br /> |
| --- | --- |
| [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#)? | [query](https://developer.android.com/reference/kotlin/android/app/slice/SliceProvider#query(android.net.Uri,%20kotlin.Array,%20kotlin.String,%20kotlin.Array,%20kotlin.String))`(`uri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)`, `projection:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>?`, `selection:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `selectionArgs:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>?`, `sortOrder:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` <br /> |
| [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#)? | [query](https://developer.android.com/reference/kotlin/android/app/slice/SliceProvider#query(android.net.Uri,%20kotlin.Array,%20kotlin.String,%20kotlin.Array,%20kotlin.String,%20android.os.CancellationSignal))`(`uri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)`, `projection:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>?`, `selection:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `selectionArgs:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>?`, `sortOrder:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `cancellationSignal:` ` [CancellationSignal](https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#)?`)` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [update](https://developer.android.com/reference/kotlin/android/app/slice/SliceProvider#update(android.net.Uri,%20android.content.ContentValues,%20kotlin.String,%20kotlin.Array))`(`uri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)`, `values:` ` [ContentValues](https://developer.android.com/reference/kotlin/android/content/ContentValues.html#)?`, `selection:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `selectionArgs:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>?`)` <br /> |
| --- | --- |

| Inherited functions ||
|---|---|
| From class [ContentProvider](https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#) |------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [ContentProviderResult](https://developer.android.com/reference/kotlin/android/content/ContentProviderResult.html#)!> | [applyBatch](https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#applyBatch(kotlin.String,%20java.util.ArrayList))`(`authority:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `operations:` ` [ArrayList](https://developer.android.com/reference/kotlin/java/util/ArrayList.html#)< [ContentProviderOperation](https://developer.android.com/reference/kotlin/android/content/ContentProviderOperation.html#)!>`)` <br /> Override this to handle requests to perform a batch of operations, or the default implementation will iterate over the operations and call [ContentProviderOperation.apply](https://developer.android.com/reference/kotlin/android/content/ContentProviderOperation.html#apply(android.content.ContentProvider,%20kotlin.Array,%20kotlin.Int))on each of them. If all calls to [ContentProviderOperation.apply](https://developer.android.com/reference/kotlin/android/content/ContentProviderOperation.html#apply(android.content.ContentProvider,%20kotlin.Array,%20kotlin.Int))succeed then a [ContentProviderResult](https://developer.android.com/reference/kotlin/android/content/ContentProviderResult.html#) array with as many elements as there were operations will be returned. If any of the calls fail, it is up to the implementation how many of the others take effect. This method can be called from multiple threads, as described in [Processes and Threads](https://developer.android.com/guide/topics/fundamentals/processes-and-threads.html#Threads). <br /> | | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [ContentProviderResult](https://developer.android.com/reference/kotlin/android/content/ContentProviderResult.html#)!> | [applyBatch](https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#applyBatch(java.util.ArrayList))`(`operations:` ` [ArrayList](https://developer.android.com/reference/kotlin/java/util/ArrayList.html#)< [ContentProviderOperation](https://developer.android.com/reference/kotlin/android/content/ContentProviderOperation.html#)!>`)` <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [bulkInsert](https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#bulkInsert(android.net.Uri,%20kotlin.Array))`(`uri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)`, `values:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [ContentValues](https://developer.android.com/reference/kotlin/android/content/ContentValues.html#)!>`)` <br /> Override this to handle requests to insert a set of new rows, or the default implementation will iterate over the values and call #insert on each of them. As a courtesy, call [notifyChange()](https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#notifyChange(android.net.Uri,%20android.database.ContentObserver))after inserting. This method can be called from multiple threads, as described in [Processes and Threads](https://developer.android.com/guide/topics/fundamentals/processes-and-threads.html#Threads). <br /> | | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)? | [call](https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#call(kotlin.String,%20kotlin.String,%20kotlin.String,%20android.os.Bundle))`(`authority:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `method:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `arg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `extras:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)?`)` <br /> Call a provider-defined method. This can be used to implement interfaces that are cheaper and/or unnatural for a table-like model. **WARNING:** The framework does no permission checking on this entry into the content provider besides the basic ability for the application to get access to the provider at all. For example, it has no idea whether the call being executed may read or write data in the provider, so can't enforce those individual permissions. Any implementation of this method**must**do its own permission checks on incoming calls to make sure they are allowed. <br /> | | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)? | [canonicalize](https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#canonicalize(android.net.Uri))`(`url:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)`)` <br /> Implement this to support canonicalization of URIs that refer to your content provider. A canonical URI is one that can be transported across devices, backup/restore, and other contexts, and still be able to refer to the same data item. Typically this is implemented by adding query params to the URI allowing the content provider to verify that an incoming canonical URI references the same data as it was originally intended for and, if it doesn't, to find that data (if it exists) in the current environment. For example, if the content provider holds people and a normal URI in it is created with a row index into that people database, the cananical representation may have an additional query param at the end which specifies the name of the person it is intended for. Later calls into the provider with that URI will look up the row of that URI's base index and, if it doesn't match or its entry's name doesn't match the name in the query param, perform a query on its database to find the correct row to operate on. If you implement support for canonical URIs,**all** incoming calls with URIs (including this one) must perform this verification and recovery of any canonical URIs they receive. In addition, you must also implement [uncanonicalize](https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#uncanonicalize(android.net.Uri))to strip the canonicalization of any of these URIs. The default implementation of this method returns null, indicating that canonical URIs are not supported. <br /> | | [ContentProvider.CallingIdentity](https://developer.android.com/reference/kotlin/android/content/ContentProvider.CallingIdentity.html#) | [clearCallingIdentity](https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#clearCallingIdentity())`()` <br /> Reset the identity of the incoming IPC on the current thread. Internally this calls [Binder.clearCallingIdentity()](https://developer.android.com/reference/kotlin/android/os/Binder.html#clearCallingIdentity())and also clears any value stored in [getCallingPackage()](https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#getCallingPackage()). <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [delete](https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#delete(android.net.Uri,%20android.os.Bundle))`(`uri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)`, `extras:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)?`)` <br /> Implement this to handle requests to delete one or more rows. The implementation should apply the selection clause when performing deletion, allowing the operation to affect multiple rows in a directory. As a courtesy, call [notifyChange()](https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#notifyChange(android.net.Uri,%20android.database.ContentObserver))after deleting. This method can be called from multiple threads, as described in [Processes and Threads](https://developer.android.com/guide/topics/fundamentals/processes-and-threads.html#Threads). The implementation is responsible for parsing out a row ID at the end of the URI, if a specific row is being deleted. That is, the client would pass in`content://contacts/people/22`and the implementation is responsible for parsing the record number (22) when creating a SQL statement. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [dump](https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#dump(java.io.FileDescriptor,%20java.io.PrintWriter,%20kotlin.Array))`(`fd:` ` [FileDescriptor](https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#)!`, `writer:` ` [PrintWriter](https://developer.android.com/reference/kotlin/java/io/PrintWriter.html#)!`, `args:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`)` <br /> Print the Provider's state into the given stream. This gets invoked if you run "adb shell dumpsys activity provider \<provider_component_name\>". <br /> | | [AttributionSource](https://developer.android.com/reference/kotlin/android/content/AttributionSource.html#)? | [getCallingAttributionSource](https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#getCallingAttributionSource())`()` <br /> Gets the attribution source of the calling app. If you want to attribute the data access to the calling app you can create an attribution context via [android.content.Context#createContext(ContextParams)](https://developer.android.com/reference/kotlin/android/content/Context.html#createContext(android.content.ContextParams))and passing this identity to [ContextParams.Builder.setNextAttributionSource(](https://developer.android.com/reference/kotlin/android/content/ContextParams.Builder.html#setNextAttributionSource(android.content.AttributionSource)). <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getCallingAttributionTag](https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#getCallingAttributionTag())`()` <br /> Return the attribution tag of the caller that initiated the request being processed on the current thread. Returns`null`if not currently processing a request of the request is for the default attribution. This will always return`null`when processing [getTypeAnonymous(android.net.Uri)](https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#getTypeAnonymous(android.net.Uri))requests For [getType(android.net.Uri)](https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#getType(android.net.Uri))requests, this will be only available for cases, where the caller can be identified. See [getTypeAnonymous(android.net.Uri)](https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#getTypeAnonymous(android.net.Uri)) <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getCallingPackage](https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#getCallingPackage())`()` <br /> Return the package name of the caller that initiated the request being processed on the current thread. The returned package will have been verified to belong to the calling UID. Returns`null`if not currently processing a request. This will always return`null`when processing [getTypeAnonymous(android.net.Uri)](https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#getTypeAnonymous(android.net.Uri))requests For [getType(android.net.Uri)](https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#getType(android.net.Uri))requests, this will be only available for cases, where the caller can be identified. See [getTypeAnonymous(android.net.Uri)](https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#getTypeAnonymous(android.net.Uri)) <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getCallingPackageUnchecked](https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#getCallingPackageUnchecked())`()` <br /> Return the package name of the caller that initiated the request being processed on the current thread. The returned package will have*not* been verified to belong to the calling UID. Returns`null`if not currently processing a request. This will always return`null`when processing [getTypeAnonymous(android.net.Uri)](https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#getTypeAnonymous(android.net.Uri))requests For [getType(android.net.Uri)](https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#getType(android.net.Uri))requests, this will be only available for cases, where the caller can be identified. See [getTypeAnonymous(android.net.Uri)](https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#getTypeAnonymous(android.net.Uri)) <br /> | | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)? | [getContext](https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#getContext())`()` <br /> Retrieves the Context this provider is running in. Only available once [onCreate](https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#onCreate())has been called -- this will return`null`in the constructor. <br /> | | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [PathPermission](https://developer.android.com/reference/kotlin/android/content/pm/PathPermission.html#)!>? | [getPathPermissions](https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#getPathPermissions())`()` <br /> Return the path-based permissions required for read and/or write access to this content provider. This method can be called from multiple threads, as described in [Processes and Threads](https://developer.android.com/guide/topics/fundamentals/processes-and-threads.html#Threads). <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getReadPermission](https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#getReadPermission())`()` <br /> Return the name of the permission required for read-only access to this content provider. This method can be called from multiple threads, as described in [Processes and Threads](https://developer.android.com/guide/topics/fundamentals/processes-and-threads.html#Threads). <br /> | | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>? | [getStreamTypes](https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#getStreamTypes(android.net.Uri,%20kotlin.String))`(`uri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)`, `mimeTypeFilter:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` <br /> Called by a client to determine the types of data streams that this content provider supports for the given URI. The default implementation returns`null`, meaning no types. If your content provider stores data of a particular type, return that MIME type if it matches the given mimeTypeFilter. If it can perform type conversions, return an array of all supported MIME types that match mimeTypeFilter. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getTypeAnonymous](https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#getTypeAnonymous(android.net.Uri))`(`uri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)`)` <br /> Implement this to handle requests for MIME type of URIs, that does not need to reveal any internal information which should be protected by any permission. If your mime type reveals details that should be protected, then you should protect those by implementing those in [getType](https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#getType(android.net.Uri)), and in this function, only return types of URIs which can be obtained by anyone without any access. Implementing ths function will make sure [getType](https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#getType(android.net.Uri))is protected by readPermission. This function by default works as the [getType](https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#getType(android.net.Uri)) <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getWritePermission](https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#getWritePermission())`()` <br /> Return the name of the permission required for read/write access to this content provider. This method can be called from multiple threads, as described in [Processes and Threads](https://developer.android.com/guide/topics/fundamentals/processes-and-threads.html#Threads). <br /> | | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)? | [insert](https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#insert(android.net.Uri,%20android.content.ContentValues,%20android.os.Bundle))`(`uri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)`, `values:` ` [ContentValues](https://developer.android.com/reference/kotlin/android/content/ContentValues.html#)?`, `extras:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)?`)` <br /> Implement this to handle requests to insert a new row. As a courtesy, call [notifyChange()](https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#notifyChange(android.net.Uri,%20android.database.ContentObserver))after inserting. This method can be called from multiple threads, as described in [Processes and Threads](https://developer.android.com/guide/topics/fundamentals/processes-and-threads.html#Threads). <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isTemporary](https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#isTemporary())`()` <br /> Returns true if this instance is a temporary content provider. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onCallingPackageChanged](https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#onCallingPackageChanged())`()` <br /> Called whenever the value of [getCallingPackage()](https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#getCallingPackage())changes, giving the provider an opportunity to invalidate any security related caching it may be performing. This typically happens when a [ContentProvider](https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#) makes a nested call back into itself when already processing a call from a remote process. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onConfigurationChanged](https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#onConfigurationChanged(android.content.res.Configuration))`(`newConfig:` ` [Configuration](https://developer.android.com/reference/kotlin/android/content/res/Configuration.html#)`)` <br /> Called by the system when the device configuration changes while your component is running. Note that, unlike activities, other components are never restarted when a configuration changes: they must always deal with the results of the change, such as by re-retrieving resources. At the time that this function has been called, your Resources object will have been updated to return resource values matching the new configuration. For more information, read [Handling Runtime Changes](https://developer.android.com/guide/topics/resources/runtime-changes.html). This method is always called on the application main thread, and must not perform lengthy operations. The default content provider implementation does nothing. Override this method to take appropriate action. (Content providers do not usually care about things like screen orientation, but may want to know about locale changes.) <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onCreate](https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#onCreate())`()` <br /> Implement this to initialize your content provider on startup. This method is called for all registered content providers on the application main thread at application launch time. It must not perform lengthy operations, or application startup will be delayed. You should defer nontrivial initialization (such as opening, upgrading, and scanning databases) until the content provider is used (via #query, #insert, etc). Deferred initialization keeps application startup fast, avoids unnecessary work if the provider turns out not to be needed, and stops database errors (such as a full disk) from halting application launch. If you use SQLite, [android.database.sqlite.SQLiteOpenHelper](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteOpenHelper.html#) is a helpful utility class that makes it easy to manage databases, and will automatically defer opening until first use. If you do use SQLiteOpenHelper, make sure to avoid calling [android.database.sqlite.SQLiteOpenHelper#getReadableDatabase](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteOpenHelper.html#getReadableDatabase())or [android.database.sqlite.SQLiteOpenHelper#getWritableDatabase](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteOpenHelper.html#getWritableDatabase())from this method. (Instead, override [android.database.sqlite.SQLiteOpenHelper#onOpen](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteOpenHelper.html#onOpen(android.database.sqlite.SQLiteDatabase))to initialize the database when it is first opened.) <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onLowMemory](https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#onLowMemory())`()` <br /> This is called when the overall system is running low on memory, and actively running processes should trim their memory usage. While the exact point at which this will be called is not defined, generally it will happen when all background process have been killed. That is, before reaching the point of killing processes hosting service and foreground UI that we would like to avoid killing. This method is always called on the application main thread, and must not perform lengthy operations. The default content provider implementation does nothing. Subclasses may override this method to take appropriate action. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onTrimMemory](https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#onTrimMemory(kotlin.Int))`(`level:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> | | [AssetFileDescriptor](https://developer.android.com/reference/kotlin/android/content/res/AssetFileDescriptor.html#)? | [openAssetFile](https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#openAssetFile(android.net.Uri,%20kotlin.String))`(`uri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)`, `mode:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` <br /> This is like #openFile, but can be implemented by providers that need to be able to return sub-sections of files, often assets inside of their .apk. This method can be called from multiple threads, as described in [Processes and Threads](https://developer.android.com/guide/topics/fundamentals/processes-and-threads.html#Threads). If you implement this, your clients must be able to deal with such file slices, either directly with android.content.ContentResolver#openAssetFileDescriptor, or by using the higher-level [ContentResolver.openInputStream](https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#openInputStream(android.net.Uri))or android.content.ContentResolver#openOutputStream methods. The returned AssetFileDescriptor can be a pipe or socket pair to enable streaming of data. If you are implementing this to return a full file, you should create the AssetFileDescriptor with [AssetFileDescriptor.UNKNOWN_LENGTH](https://developer.android.com/reference/kotlin/android/content/res/AssetFileDescriptor.html#UNKNOWN_LENGTH:kotlin.Long) to be compatible with applications that cannot handle sub-sections of files. For use in Intents, you will want to implement [getType](https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#getType(android.net.Uri))to return the appropriate MIME type for the data returned here with the same URI. This will allow intent resolution to automatically determine the data MIME type and select the appropriate matching targets as part of its operation. For better interoperability with other applications, it is recommended that for any URIs that can be opened, you also support queries on them containing at least the columns specified by [android.provider.OpenableColumns](https://developer.android.com/reference/kotlin/android/provider/OpenableColumns.html#). <br /> | | [AssetFileDescriptor](https://developer.android.com/reference/kotlin/android/content/res/AssetFileDescriptor.html#)? | [openAssetFile](https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#openAssetFile(android.net.Uri,%20kotlin.String,%20android.os.CancellationSignal))`(`uri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)`, `mode:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `signal:` ` [CancellationSignal](https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#)?`)` <br /> This is like #openFile, but can be implemented by providers that need to be able to return sub-sections of files, often assets inside of their .apk. This method can be called from multiple threads, as described in [Processes and Threads](https://developer.android.com/guide/topics/fundamentals/processes-and-threads.html#Threads). If you implement this, your clients must be able to deal with such file slices, either directly with android.content.ContentResolver#openAssetFileDescriptor, or by using the higher-level [ContentResolver.openInputStream](https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#openInputStream(android.net.Uri))or android.content.ContentResolver#openOutputStream methods. The returned AssetFileDescriptor can be a pipe or socket pair to enable streaming of data. If you are implementing this to return a full file, you should create the AssetFileDescriptor with [AssetFileDescriptor.UNKNOWN_LENGTH](https://developer.android.com/reference/kotlin/android/content/res/AssetFileDescriptor.html#UNKNOWN_LENGTH:kotlin.Long) to be compatible with applications that cannot handle sub-sections of files. For use in Intents, you will want to implement [getType](https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#getType(android.net.Uri))to return the appropriate MIME type for the data returned here with the same URI. This will allow intent resolution to automatically determine the data MIME type and select the appropriate matching targets as part of its operation. For better interoperability with other applications, it is recommended that for any URIs that can be opened, you also support queries on them containing at least the columns specified by [android.provider.OpenableColumns](https://developer.android.com/reference/kotlin/android/provider/OpenableColumns.html#). <br /> | | [ParcelFileDescriptor](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#)? | [openFile](https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#openFile(android.net.Uri,%20kotlin.String))`(`uri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)`, `mode:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` <br /> Override this to handle requests to open a file blob. The default implementation always throws [FileNotFoundException](https://developer.android.com/reference/kotlin/java/io/FileNotFoundException.html#). This method can be called from multiple threads, as described in [Processes and Threads](https://developer.android.com/guide/topics/fundamentals/processes-and-threads.html#Threads). This method returns a ParcelFileDescriptor, which is returned directly to the caller. This way large data (such as images and documents) can be returned without copying the content. The returned ParcelFileDescriptor is owned by the caller, so it is their responsibility to close it when done. That is, the implementation of this method should create a new ParcelFileDescriptor for each call. If opened with the exclusive "r" or "w" modes, the returned ParcelFileDescriptor can be a pipe or socket pair to enable streaming of data. Opening with the "rw" or "rwt" modes implies a file on disk that supports seeking. If you need to detect when the returned ParcelFileDescriptor has been closed, or if the remote process has crashed or encountered some other error, you can use [ParcelFileDescriptor.open(File, int,](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#open(java.io.File,%20kotlin.Int,%20android.os.Handler,%20android.os.ParcelFileDescriptor.OnCloseListener)), [ParcelFileDescriptor.createReliablePipe()](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#createReliablePipe()), or [ParcelFileDescriptor.createReliableSocketPair()](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#createReliableSocketPair()). If you need to return a large file that isn't backed by a real file on disk, such as a file on a network share or cloud storage service, consider using [StorageManager.openProxyFileDescriptor(int, android.os.ProxyFileDescriptorCallback, android.os.Handler)](https://developer.android.com/reference/kotlin/android/os/storage/StorageManager.html#openProxyFileDescriptor(kotlin.Int,%20android.os.ProxyFileDescriptorCallback,%20android.os.Handler))which will let you to stream the content on-demand. For use in Intents, you will want to implement [getType](https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#getType(android.net.Uri))to return the appropriate MIME type for the data returned here with the same URI. This will allow intent resolution to automatically determine the data MIME type and select the appropriate matching targets as part of its operation. For better interoperability with other applications, it is recommended that for any URIs that can be opened, you also support queries on them containing at least the columns specified by [android.provider.OpenableColumns](https://developer.android.com/reference/kotlin/android/provider/OpenableColumns.html#). You may also want to support other common columns if you have additional meta-data to supply, such as [android.provider.MediaStore.MediaColumns#DATE_ADDED](https://developer.android.com/reference/kotlin/android/provider/MediaStore.MediaColumns.html#DATE_ADDED:kotlin.String) in [android.provider.MediaStore.MediaColumns](https://developer.android.com/reference/kotlin/android/provider/MediaStore.MediaColumns.html#). <br /> | | [ParcelFileDescriptor](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#)? | [openFile](https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#openFile(android.net.Uri,%20kotlin.String,%20android.os.CancellationSignal))`(`uri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)`, `mode:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `signal:` ` [CancellationSignal](https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#)?`)` <br /> Override this to handle requests to open a file blob. The default implementation always throws [FileNotFoundException](https://developer.android.com/reference/kotlin/java/io/FileNotFoundException.html#). This method can be called from multiple threads, as described in [Processes and Threads](https://developer.android.com/guide/topics/fundamentals/processes-and-threads.html#Threads). This method returns a ParcelFileDescriptor, which is returned directly to the caller. This way large data (such as images and documents) can be returned without copying the content. The returned ParcelFileDescriptor is owned by the caller, so it is their responsibility to close it when done. That is, the implementation of this method should create a new ParcelFileDescriptor for each call. If opened with the exclusive "r" or "w" modes, the returned ParcelFileDescriptor can be a pipe or socket pair to enable streaming of data. Opening with the "rw" or "rwt" modes implies a file on disk that supports seeking. If you need to detect when the returned ParcelFileDescriptor has been closed, or if the remote process has crashed or encountered some other error, you can use [ParcelFileDescriptor.open(File, int,](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#open(java.io.File,%20kotlin.Int,%20android.os.Handler,%20android.os.ParcelFileDescriptor.OnCloseListener)), [ParcelFileDescriptor.createReliablePipe()](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#createReliablePipe()), or [ParcelFileDescriptor.createReliableSocketPair()](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#createReliableSocketPair()). For use in Intents, you will want to implement [getType](https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#getType(android.net.Uri))to return the appropriate MIME type for the data returned here with the same URI. This will allow intent resolution to automatically determine the data MIME type and select the appropriate matching targets as part of its operation. For better interoperability with other applications, it is recommended that for any URIs that can be opened, you also support queries on them containing at least the columns specified by [android.provider.OpenableColumns](https://developer.android.com/reference/kotlin/android/provider/OpenableColumns.html#). You may also want to support other common columns if you have additional meta-data to supply, such as [android.provider.MediaStore.MediaColumns#DATE_ADDED](https://developer.android.com/reference/kotlin/android/provider/MediaStore.MediaColumns.html#DATE_ADDED:kotlin.String) in [android.provider.MediaStore.MediaColumns](https://developer.android.com/reference/kotlin/android/provider/MediaStore.MediaColumns.html#). <br /> | | [ParcelFileDescriptor](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#) | [openFileHelper](https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#openFileHelper(android.net.Uri,%20kotlin.String))`(`uri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)`, `mode:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` <br /> Convenience for subclasses that wish to implement #openFile by looking up a column named "_data" at the given URI. <br /> | | [ParcelFileDescriptor](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#) | [openPipeHelper](https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#openPipeHelper(android.net.Uri,%20kotlin.String,%20android.os.Bundle,%20android.content.ContentProvider.openPipeHelper.T,%20android.content.ContentProvider.PipeDataWriter))`(`uri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)`, `mimeType:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `opts:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)?`, `args:` `T?`, `func:` ` [ContentProvider.PipeDataWriter](https://developer.android.com/reference/kotlin/android/content/ContentProvider.PipeDataWriter.html#)<T>`)` <br /> A helper function for implementing #openTypedAssetFile, for creating a data pipe and background thread allowing you to stream generated data back to the client. This function returns a new ParcelFileDescriptor that should be returned to the caller (the caller is responsible for closing it). <br /> | | [AssetFileDescriptor](https://developer.android.com/reference/kotlin/android/content/res/AssetFileDescriptor.html#)? | [openTypedAssetFile](https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#openTypedAssetFile(android.net.Uri,%20kotlin.String,%20android.os.Bundle))`(`uri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)`, `mimeTypeFilter:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `opts:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)?`)` <br /> Called by a client to open a read-only stream containing data of a particular MIME type. This is like [openAssetFile(android.net.Uri,java.lang.String)](https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#openAssetFile(android.net.Uri,%20kotlin.String)), except the file can only be read-only and the content provider may perform data conversions to generate data of the desired type. The default implementation compares the given mimeType against the result of [getType(android.net.Uri)](https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#getType(android.net.Uri))and, if they match, simply calls [openAssetFile(android.net.Uri,java.lang.String)](https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#openAssetFile(android.net.Uri,%20kotlin.String)). See [ClipData](https://developer.android.com/reference/kotlin/android/content/ClipData.html#) for examples of the use and implementation of this method. The returned AssetFileDescriptor can be a pipe or socket pair to enable streaming of data. For better interoperability with other applications, it is recommended that for any URIs that can be opened, you also support queries on them containing at least the columns specified by [android.provider.OpenableColumns](https://developer.android.com/reference/kotlin/android/provider/OpenableColumns.html#). You may also want to support other common columns if you have additional meta-data to supply, such as [android.provider.MediaStore.MediaColumns#DATE_ADDED](https://developer.android.com/reference/kotlin/android/provider/MediaStore.MediaColumns.html#DATE_ADDED:kotlin.String) in [android.provider.MediaStore.MediaColumns](https://developer.android.com/reference/kotlin/android/provider/MediaStore.MediaColumns.html#). <br /> | | [AssetFileDescriptor](https://developer.android.com/reference/kotlin/android/content/res/AssetFileDescriptor.html#)? | [openTypedAssetFile](https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#openTypedAssetFile(android.net.Uri,%20kotlin.String,%20android.os.Bundle,%20android.os.CancellationSignal))`(`uri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)`, `mimeTypeFilter:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `opts:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)?`, `signal:` ` [CancellationSignal](https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#)?`)` <br /> Called by a client to open a read-only stream containing data of a particular MIME type. This is like [openAssetFile(android.net.Uri,java.lang.String)](https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#openAssetFile(android.net.Uri,%20kotlin.String)), except the file can only be read-only and the content provider may perform data conversions to generate data of the desired type. The default implementation compares the given mimeType against the result of [getType(android.net.Uri)](https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#getType(android.net.Uri))and, if they match, simply calls [openAssetFile(android.net.Uri,java.lang.String)](https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#openAssetFile(android.net.Uri,%20kotlin.String)). See [ClipData](https://developer.android.com/reference/kotlin/android/content/ClipData.html#) for examples of the use and implementation of this method. The returned AssetFileDescriptor can be a pipe or socket pair to enable streaming of data. For better interoperability with other applications, it is recommended that for any URIs that can be opened, you also support queries on them containing at least the columns specified by [android.provider.OpenableColumns](https://developer.android.com/reference/kotlin/android/provider/OpenableColumns.html#). You may also want to support other common columns if you have additional meta-data to supply, such as [android.provider.MediaStore.MediaColumns#DATE_ADDED](https://developer.android.com/reference/kotlin/android/provider/MediaStore.MediaColumns.html#DATE_ADDED:kotlin.String) in [android.provider.MediaStore.MediaColumns](https://developer.android.com/reference/kotlin/android/provider/MediaStore.MediaColumns.html#). <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [refresh](https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#refresh(android.net.Uri,%20android.os.Bundle,%20android.os.CancellationSignal))`(`uri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)!`, `extras:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)?`, `cancellationSignal:` ` [CancellationSignal](https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#)?`)` <br /> Implement this to support refresh of content identified by`uri`. By default, this method returns false; providers who wish to implement this should return true to signal the client that the provider has tried refreshing with its own implementation. This allows clients to request an explicit refresh of content identified by`uri`. Client code should only invoke this method when there is a strong indication (such as a user initiated pull to refresh gesture) that the content is stale. Remember to send [ContentResolver.notifyChange(Uri, android.database.ContentObserver)](https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#notifyChange(android.net.Uri,%20android.database.ContentObserver))notifications when content changes. <br /> | | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#) | [requireContext](https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#requireContext())`()` <br /> Retrieves a Non-Nullable Context this provider is running in, this is intended to be called after [onCreate](https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#onCreate()). When called before context was created, an IllegalStateException will be thrown. Note A provider must be declared in the manifest and created automatically by the system, and context is only available after [onCreate](https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#onCreate())is called. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [restoreCallingIdentity](https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#restoreCallingIdentity(android.content.ContentProvider.CallingIdentity))`(`identity:` ` [ContentProvider.CallingIdentity](https://developer.android.com/reference/kotlin/android/content/ContentProvider.CallingIdentity.html#)`)` <br /> Restore the identity of the incoming IPC on the current thread back to a previously identity that was returned by [clearCallingIdentity](https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#clearCallingIdentity()). Internally this calls [Binder.restoreCallingIdentity(long)](https://developer.android.com/reference/kotlin/android/os/Binder.html#restoreCallingIdentity(kotlin.Long))and also restores any value stored in [getCallingPackage()](https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#getCallingPackage()). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPathPermissions](https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#setPathPermissions(kotlin.Array))`(`permissions:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [PathPermission](https://developer.android.com/reference/kotlin/android/content/pm/PathPermission.html#)!>?`)` <br /> Change the path-based permission required to read and/or write data in the content provider. This is normally set for you from its manifest information when the provider is first created. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setReadPermission](https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#setReadPermission(kotlin.String))`(`permission:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` <br /> Change the permission required to read data from the content provider. This is normally set for you from its manifest information when the provider is first created. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setWritePermission](https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#setWritePermission(kotlin.String))`(`permission:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` <br /> Change the permission required to read and write data in the content provider. This is normally set for you from its manifest information when the provider is first created. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [shutdown](https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#shutdown())`()` <br /> Implement this to shut down the ContentProvider instance. You can then invoke this method in unit tests. Android normally handles ContentProvider startup and shutdown automatically. You do not need to start up or shut down a ContentProvider. When you invoke a test method on a ContentProvider, however, a ContentProvider instance is started and keeps running after the test finishes, even if a succeeding test instantiates another ContentProvider. A conflict develops because the two instances are usually running against the same underlying data source (for example, an sqlite database). Implementing shutDown() avoids this conflict by providing a way to terminate the ContentProvider. This method can also prevent memory leaks from multiple instantiations of the ContentProvider, and it can ensure unit test isolation by allowing you to completely clean up the test fixture before moving on to the next test. <br /> | | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)? | [uncanonicalize](https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#uncanonicalize(android.net.Uri))`(`url:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)`)` <br /> Remove canonicalization from canonical URIs previously returned by [canonicalize](https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#canonicalize(android.net.Uri)). For example, if your implementation is to add a query param to canonicalize a URI, this method can simply trip any query params on the URI. The default implementation always returns the same url that was passed in. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [update](https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#update(android.net.Uri,%20android.content.ContentValues,%20android.os.Bundle))`(`uri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)`, `values:` ` [ContentValues](https://developer.android.com/reference/kotlin/android/content/ContentValues.html#)?`, `extras:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)?`)` <br /> Implement this to handle requests to update one or more rows. The implementation should update all rows matching the selection to set the columns according to the provided values map. As a courtesy, call [notifyChange()](https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#notifyChange(android.net.Uri,%20android.database.ContentObserver))after updating. This method can be called from multiple threads, as described in [Processes and Threads](https://developer.android.com/guide/topics/fundamentals/processes-and-threads.html#Threads). <br /> | ||
| From class [ComponentCallbacks](https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks.html#) |------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onConfigurationChanged](https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks.html#onConfigurationChanged(android.content.res.Configuration))`(`newConfig:` ` [Configuration](https://developer.android.com/reference/kotlin/android/content/res/Configuration.html#)`)` <br /> Called by the system when the device configuration changes while your component is running. Note that, unlike activities, other components are never restarted when a configuration changes: they must always deal with the results of the change, such as by re-retrieving resources. At the time that this function has been called, your Resources object will have been updated to return resource values matching the new configuration. For more information, read [Handling Runtime Changes](https://developer.android.com/guide/topics/resources/runtime-changes.html). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onLowMemory](https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks.html#onLowMemory())`()` <br /> This is called when the overall system is running low on memory, and actively running processes should trim their memory usage. While the exact point at which this will be called is not defined, generally it will happen when all background process have been killed. That is, before reaching the point of killing processes hosting service and foreground UI that we would like to avoid killing. <br /> | ||

## Constants

### SLICE_TYPE

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SLICE_TYPE: String
```

**Deprecated:** *Deprecated in Java.*

This is the Android platform's MIME type for a URI containing a slice implemented through [SliceProvider](https://developer.android.com/reference/kotlin/android/app/slice/SliceProvider#). 

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
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!:The context this provider is running in |
| `info` | [ProviderInfo](https://developer.android.com/reference/kotlin/android/content/pm/ProviderInfo.html#)!:Registered information about this content provider |

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
| `extras` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)?:This value may be`null`. |
| --- | --- |

| Return ||
|-----------------------------------------------------------------------------------|--------------------------|
| [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)? | This value may be`null`. |

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
| `uri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#):The full URI to query, including a row ID (if a specific record is requested). This value cannot be`null`. |
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
| `uri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#):the URI to query. This value cannot be`null`. |

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
| `uri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#):The content:// URI of the insertion request. This value cannot be`null`. |
| `values` | [ContentValues](https://developer.android.com/reference/kotlin/android/content/ContentValues.html#)?:A set of column_name/value pairs to add to the database. This value may be`null`. |

| Return ||
|------------------------------------------------------------------------------|---------------------------------------------------------------|
| [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)? | The URI for the newly inserted item. This value may be`null`. |

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

onBindSlice should return as quickly as possible so that the UI tied to this slice can be responsive. No network or other IO will be allowed during onBindSlice. Any loading that needs to be done should happen in the background with a call to [ContentResolver.notifyChange(Uri, ContentObserver)](https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#notifyChange(android.net.Uri,%20android.database.ContentObserver))when the app is ready to provide the complete data in onBindSlice.

The slice returned should have a spec that is compatible with one of the supported specs.

| Parameters ||
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `sliceUri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)!:Uri to bind. |
| `supportedSpecs` | [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [SliceSpec](https://developer.android.com/reference/kotlin/android/app/slice/SliceSpec)!\>!:List of supported specs. |

**See Also**

- [android.app.slice.Slice](https://developer.android.com/reference/kotlin/android/app/slice/Slice)
- [android.app.slice.Slice#HINT_PARTIAL](https://developer.android.com/reference/kotlin/android/app/slice/Slice#HINT_PARTIAL:kotlin.String) 

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
| `sliceUri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)!:the Uri of the slice attempting to be bound. |

| Return ||
|-------------------------------------------------------------------------------------------------|-----------------------------|
| [PendingIntent](https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#) | This value cannot be`null`. |

**See Also**

- [#getCallingPackage()](https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#getCallingPackage()) 

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
| `uri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#):The uri to look for descendants under. This value cannot be`null`. |

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)< [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)!> | All slices within the space. This value cannot be`null`. |

**See Also**

- [android.app.slice.SliceManager#getSliceDescendants(Uri)](https://developer.android.com/reference/kotlin/android/app/slice/SliceManager#getSliceDescendants(android.net.Uri)) 

### onMapIntentToUri

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onMapIntentToUri(intent: Intent!): Uri
```

**Deprecated:** *Deprecated in Java.*

This method must be overridden if an [IntentFilter](https://developer.android.com/reference/kotlin/android/content/IntentFilter.html#) is specified on the SliceProvider. In that case, this method can be called and is expected to return a non-null Uri representing a slice. Otherwise this will throw [UnsupportedOperationException](https://developer.android.com/reference/kotlin/java/lang/UnsupportedOperationException.html#). Any intent filter added to a slice provider should also contain [SliceManager.CATEGORY_SLICE](https://developer.android.com/reference/kotlin/android/app/slice/SliceManager#CATEGORY_SLICE:kotlin.String), because otherwise it will not be detected by [SliceManager.mapIntentToUri(Intent)](https://developer.android.com/reference/kotlin/android/app/slice/SliceManager#mapIntentToUri(android.content.Intent)).

| Return ||
|-----------------------------------------------------------------------------|-----------------------------------------------------------------|
| [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#) | Uri representing the slice associated with the provided intent. |

**See Also**

- [android.app.slice.Slice](https://developer.android.com/reference/kotlin/android/app/slice/Slice)
- [android.app.slice.SliceManager#mapIntentToUri(Intent)](https://developer.android.com/reference/kotlin/android/app/slice/SliceManager#mapIntentToUri(android.content.Intent)) 

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
| `sliceUri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)!:The uri of the slice being unpinned. |

**See Also**

- [#onSliceUnpinned(Uri)](https://developer.android.com/reference/kotlin/android/app/slice/SliceProvider#onSliceUnpinned(android.net.Uri)) 

### onSliceUnpinned

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onSliceUnpinned(sliceUri: Uri!): Unit
```

**Deprecated:** *Deprecated in Java.*

Called to inform an app that a slices is no longer pinned.

This means that no other apps on the device care about updates to this slice anymore and therefore it is not important to be updated. Any syncs or jobs related to this slice should be cancelled. 
**See Also**

- [#onSlicePinned(Uri)](https://developer.android.com/reference/kotlin/android/app/slice/SliceProvider#onSlicePinned(android.net.Uri)) 

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
| `uri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#):The URI to query. This will be the full URI sent by the client. This value cannot be`null`. |
| `projection` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>?:The list of columns to put into the cursor. If`null`provide a default set of columns. |
| `queryArgs` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)?:A Bundle containing additional information necessary for the operation. Arguments may include SQL style arguments, such as [ContentResolver.QUERY_ARG_SQL_LIMIT](https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#QUERY_ARG_SQL_LIMIT:kotlin.String), but note that the documentation for each individual provider will indicate which arguments they support. This value may be`null`. |
| --- | --- |
| `cancellationSignal` | [CancellationSignal](https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#)?:A signal to cancel the operation in progress, or`null`. |

| Return ||
|-----------------------------------------------------------------------------------------|--------------------|
| [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#)? | a Cursor or`null`. |

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
| `uri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#):The URI to query. This will be the full URI sent by the client; if the client is requesting a specific record, the URI will end in a record number that the implementation should parse and add to a WHERE or HAVING clause, specifying that _id value. This value cannot be`null`. |
| `projection` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>?:The list of columns to put into the cursor. If`null`all columns are included. |
| `selection` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:A selection criteria to apply when filtering rows. If`null`then all rows are included. |
| --- | --- |
| `selectionArgs` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>?:You may include ?s in selection, which will be replaced by the values from selectionArgs, in order that they appear in the selection. The values will be bound as Strings. This value may be`null`. |
| `sortOrder` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:How the rows in the cursor should be sorted. If`null`then the provider is free to define the sort order. |

| Return ||
|-----------------------------------------------------------------------------------------|--------------------|
| [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#)? | a Cursor or`null`. |

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
| `uri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#):The URI to query. This will be the full URI sent by the client; if the client is requesting a specific record, the URI will end in a record number that the implementation should parse and add to a WHERE or HAVING clause, specifying that _id value. This value cannot be`null`. |
| `projection` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>?:The list of columns to put into the cursor. If`null`all columns are included. |
| `selection` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:A selection criteria to apply when filtering rows. If`null`then all rows are included. |
| --- | --- |
| `selectionArgs` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>?:You may include ?s in selection, which will be replaced by the values from selectionArgs, in order that they appear in the selection. The values will be bound as Strings. This value may be`null`. |
| `sortOrder` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:How the rows in the cursor should be sorted. If`null`then the provider is free to define the sort order. |
| `cancellationSignal` | [CancellationSignal](https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#)?:A signal to cancel the operation in progress, or`null`if none. If the operation is canceled, then [android.os.OperationCanceledException](https://developer.android.com/reference/kotlin/android/os/OperationCanceledException.html#) will be thrown when the query is executed. |
| --- | --- |

| Return ||
|-----------------------------------------------------------------------------------------|--------------------|
| [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#)? | a Cursor or`null`. |

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
| `uri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#):The URI to query. This can potentially have a record ID if this is an update request for a specific record. This value cannot be`null`. |
| `values` | [ContentValues](https://developer.android.com/reference/kotlin/android/content/ContentValues.html#)?:A set of column_name/value pairs to update in the database. This value may be`null`. |
| `selection` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:An optional filter to match rows to update. This value may be`null`. |
| --- | --- |
| `selectionArgs` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>?:This value may be`null`. |

| Return ||
|----------------------------------------------------------------------------|------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of rows affected. |
