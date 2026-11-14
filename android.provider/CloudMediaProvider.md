Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [R Extensions 3](https://developer.android.com/sdkExtensions)

# CloudMediaProvider

```
abstract class CloudMediaProvider : ContentProvider
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.content.ContentProvider](https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#) ||
| | ↳ | [android.provider.CloudMediaProvider](https://developer.android.com/reference/kotlin/android/provider/CloudMediaProvider#) |

Base class for a cloud media provider. A cloud media provider offers read-only access to durable media files, specifically photos and videos stored on a local disk, or files in a cloud storage service. To create a cloud media provider, extend this class, implement the abstract methods, and add it to your manifest like this:

```kotlin
<manifest>
     ...
     <application>
         ...
         <provider
             android:name="com.example.MyCloudProvider"
             android:authorities="com.example.mycloudprovider"
             android:exported="true"
             android:permission="com.android.providers.media.permission.MANAGE_CLOUD_MEDIA_PROVIDERS"
             <intent-filter>
                 <action android:name="android.content.action.CLOUD_MEDIA_PROVIDER" />
             </intent-filter>
         </provider>
         ...
     </application>
 </manifest>
```

<br />

When defining your provider, you must protect it with the `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProviderContract#MANAGE_CLOUD_MEDIA_PROVIDERS_PERMISSION:kotlin.String`, which is a permission only the system can obtain, trying to define an unprotected `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProvider#` will result in a `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#`.

Applications cannot use a cloud media provider directly; they must go through `https://developer.android.com/reference/kotlin/android/provider/MediaStore#ACTION_PICK_IMAGES:kotlin.String` which requires a user to actively navigate and select media items. When a user selects a media item through that UI, the system issues narrow URI permission grants to the requesting application.

### Media items

A media item must be an openable stream (with a specific MIME type). Media items can belong to zero or more albums. Albums cannot contain other albums.

Each item under a provider is uniquely referenced by its media or album id, which must not change which must be unique across all collection IDs as returned by `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProvider#onGetMediaCollectionInfo(android.os.Bundle)`.

## Summary

| Nested classes ||
|---|---|
| abstract | `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProvider.CloudMediaSurfaceController` Manages rendering the preview of media items on given instances of `https://developer.android.com/reference/kotlin/android/view/Surface.html#`. |
| | `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProvider.CloudMediaSurfaceStateChangedCallback` This class is used by `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProvider#` to send `https://developer.android.com/reference/kotlin/android/view/Surface.html#` state updates to picker launched via `https://developer.android.com/reference/kotlin/android/provider/MediaStore#ACTION_PICK_IMAGES:kotlin.String`. |

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#TRIM_MEMORY_BACKGROUND:kotlin.Int` Level for `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#onTrimMemory(kotlin.Int)`: the process has gone on to the LRU list. This is a good opportunity to clean up resources that can efficiently and quickly be re-built if the user returns to the app. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#TRIM_MEMORY_COMPLETE:kotlin.Int` Level for `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#onTrimMemory(kotlin.Int)`: the process is nearing the end of the background LRU list, and if more memory isn't found soon it will be killed. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#TRIM_MEMORY_MODERATE:kotlin.Int` Level for `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#onTrimMemory(kotlin.Int)`: the process is around the middle of the background LRU list; freeing memory can help the system keep other processes running later in the list for better overall performance. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#TRIM_MEMORY_RUNNING_CRITICAL:kotlin.Int` Level for `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#onTrimMemory(kotlin.Int)`: the process is not an expendable background process, but the device is running extremely low on memory and is about to not be able to keep any background processes running. Your running process should free up as many non-critical resources as it can to allow that memory to be used elsewhere. The next thing that will happen after this is `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks.html#onLowMemory()` called to report that nothing at all can be kept in the background, a situation that can start to notably impact the user. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#TRIM_MEMORY_RUNNING_LOW:kotlin.Int` Level for `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#onTrimMemory(kotlin.Int)`: the process is not an expendable background process, but the device is running low on memory. Your running process should free up unneeded resources to allow that memory to be used elsewhere. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#TRIM_MEMORY_RUNNING_MODERATE:kotlin.Int` Level for `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#onTrimMemory(kotlin.Int)`: the process is not an expendable background process, but the device is running moderately low on memory. Your running process may want to release some unneeded resources for use elsewhere. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#TRIM_MEMORY_UI_HIDDEN:kotlin.Int` Level for `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#onTrimMemory(kotlin.Int)`: the process had been showing a user interface, and is no longer doing so. Large allocations with the UI should be released at this point to allow memory to be better managed. <br /> | ||

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProvider#CloudMediaProvider()()` <br /> |

| Public methods ||
|---|---|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProvider#attachInfo(android.content.Context,%20android.content.pm.ProviderInfo)(context: https://developer.android.com/reference/kotlin/android/content/Context.html#, info: https://developer.android.com/reference/kotlin/android/content/pm/ProviderInfo.html#)` Implementation is provided by the parent class. |
| [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#) | `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProvider#call(kotlin.String,%20kotlin.String,%20android.os.Bundle)(method: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, arg: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, extras: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?)` Implementation is provided by the parent class. |
| [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#) | `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProvider#canonicalize(android.net.Uri)(uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#)` Implementation is provided by the parent class. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProvider#delete(android.net.Uri,%20kotlin.String,%20kotlin.Array)(uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#, selection: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, selectionArgs: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>?)` Implementation is provided by the parent class. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProvider#getType(android.net.Uri)(uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#)` Implementation is provided by the parent class. |
| [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#) | `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProvider#insert(android.net.Uri,%20android.content.ContentValues)(uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#, values: https://developer.android.com/reference/kotlin/android/content/ContentValues.html#!)` Implementation is provided by the parent class. |
| --- | --- |
| open [CloudMediaProvider.CloudMediaSurfaceController](https://developer.android.com/reference/kotlin/android/provider/CloudMediaProvider.CloudMediaSurfaceController)? | `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProvider#onCreateCloudMediaSurfaceController(android.os.Bundle,%20android.provider.CloudMediaProvider.CloudMediaSurfaceStateChangedCallback)(config: https://developer.android.com/reference/kotlin/android/os/Bundle.html#, callback: https://developer.android.com/reference/kotlin/android/provider/CloudMediaProvider.CloudMediaSurfaceStateChangedCallback)` Returns a `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProvider.CloudMediaSurfaceController` used for rendering the preview of media items, or null if preview rendering is not supported. |
| open [CloudMediaProviderContract.Capabilities](https://developer.android.com/reference/kotlin/android/provider/CloudMediaProviderContract.Capabilities) | `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProvider#onGetCapabilities()()` Returns the `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProviderContract.Capabilities` of this CloudMediaProvider. |
| abstract [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#) | `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProvider#onGetMediaCollectionInfo(android.os.Bundle)(extras: https://developer.android.com/reference/kotlin/android/os/Bundle.html#)` Returns metadata about the media collection itself. |
| --- | --- |
| abstract [ParcelFileDescriptor](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#) | `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProvider#onOpenMedia(kotlin.String,%20android.os.Bundle,%20android.os.CancellationSignal)(mediaId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, extras: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?, signal: https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#?)` Returns the full size media item identified by `mediaId`. |
| abstract [AssetFileDescriptor](https://developer.android.com/reference/kotlin/android/content/res/AssetFileDescriptor.html#) | `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProvider#onOpenPreview(kotlin.String,%20android.graphics.Point,%20android.os.Bundle,%20android.os.CancellationSignal)(mediaId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, size: https://developer.android.com/reference/kotlin/android/graphics/Point.html#, extras: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?, signal: https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#?)` Returns a thumbnail of `size` for a media item identified by `mediaId` |
| open [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#) | `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProvider#onQueryAlbums(android.os.Bundle)(extras: https://developer.android.com/reference/kotlin/android/os/Bundle.html#)` Returns a cursor representing all album items in the media collection optionally filtered by `extras` and sorted in reverse chronological order of `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProviderContract.AlbumColumns#DATE_TAKEN_MILLIS:kotlin.String`, i. |
| --- | --- |
| abstract [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#) | `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProvider#onQueryDeletedMedia(android.os.Bundle)(extras: https://developer.android.com/reference/kotlin/android/os/Bundle.html#)` Returns a `https://developer.android.com/reference/kotlin/android/database/Cursor.html#` representing all deleted media items in the entire media collection within the current provider version as returned by `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProvider#onGetMediaCollectionInfo(android.os.Bundle)`. |
| abstract [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#) | `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProvider#onQueryMedia(android.os.Bundle)(extras: https://developer.android.com/reference/kotlin/android/os/Bundle.html#)` Returns a cursor representing all media items in the media collection optionally filtered by `extras` and sorted in reverse chronological order of `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProviderContract.MediaColumns#DATE_TAKEN_MILLIS:kotlin.String`, i. |
| open [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#) | `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProvider#onQueryMediaCategories(kotlin.String,%20android.os.Bundle,%20android.os.CancellationSignal)(parentCategoryId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, extras: https://developer.android.com/reference/kotlin/android/os/Bundle.html#, cancellationSignal: https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#?)` Queries for the available MediaCategories under the given `parentCategoryId`, filtered by `extras`. |
| --- | --- |
| open [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#) | `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProvider#onQueryMediaInMediaSet(kotlin.String,%20android.os.Bundle,%20android.os.CancellationSignal)(mediaSetId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, extras: https://developer.android.com/reference/kotlin/android/os/Bundle.html#, cancellationSignal: https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#?)` Queries for the available media items under a given `mediaSetId`, filtered by `extras`. |
| open [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#) | `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProvider#onQueryMediaSets(kotlin.String,%20android.os.Bundle,%20android.os.CancellationSignal)(mediaCategoryId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, extras: https://developer.android.com/reference/kotlin/android/os/Bundle.html#, cancellationSignal: https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#?)` Queries for the available MediaSets under a given `mediaCategoryId`, filtered by `extras`. |
| open [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#) | `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProvider#onQuerySearchSuggestions(kotlin.String,%20android.os.Bundle,%20android.os.CancellationSignal)(prefixText: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, extras: https://developer.android.com/reference/kotlin/android/os/Bundle.html#, cancellationSignal: https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#?)` Queries for the available SearchSuggestions based on a `prefixText`, filtered by `extras`. |
| --- | --- |
| open [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#) | `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProvider#onSearchMedia(kotlin.String,%20android.os.Bundle,%20android.os.CancellationSignal)(searchText: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, extras: https://developer.android.com/reference/kotlin/android/os/Bundle.html#, cancellationSignal: https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#?)` Searches media items based on entered search text, managed by `extras` and returns a cursor of `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProviderContract.MediaColumns` based on the match. |
| open [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#) | `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProvider#onSearchMedia(kotlin.String,%20kotlin.String,%20android.os.Bundle,%20android.os.CancellationSignal)(suggestedMediaSetId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, fallbackSearchText: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, extras: https://developer.android.com/reference/kotlin/android/os/Bundle.html#, cancellationSignal: https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#?)` Searches media items based on a selected suggestion, managed by `extras` and returns a cursor of `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProviderContract.MediaColumns` based on the match. |
| [ParcelFileDescriptor](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#) | `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProvider#openFile(android.net.Uri,%20kotlin.String)(uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#, mode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Implementation is provided by the parent class. |
| --- | --- |
| [ParcelFileDescriptor](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#) | `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProvider#openFile(android.net.Uri,%20kotlin.String,%20android.os.CancellationSignal)(uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#, mode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, signal: https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#?)` Implementation is provided by the parent class. |
| [AssetFileDescriptor](https://developer.android.com/reference/kotlin/android/content/res/AssetFileDescriptor.html#) | `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProvider#openTypedAssetFile(android.net.Uri,%20kotlin.String,%20android.os.Bundle)(uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#, mimeTypeFilter: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, opts: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?)` Implementation is provided by the parent class. |
| [AssetFileDescriptor](https://developer.android.com/reference/kotlin/android/content/res/AssetFileDescriptor.html#) | `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProvider#openTypedAssetFile(android.net.Uri,%20kotlin.String,%20android.os.Bundle,%20android.os.CancellationSignal)(uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#, mimeTypeFilter: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, opts: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?, signal: https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#?)` Implementation is provided by the parent class. |
| --- | --- |
| [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#) | `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProvider#query(android.net.Uri,%20kotlin.Array,%20android.os.Bundle,%20android.os.CancellationSignal)(uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#, projection: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>?, queryArgs: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?, cancellationSignal: https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#?)` Implementation is provided by the parent class. |
| [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#) | `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProvider#query(android.net.Uri,%20kotlin.Array,%20kotlin.String,%20kotlin.Array,%20kotlin.String)(uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#, projection: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>?, selection: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, selectionArgs: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>?, sortOrder: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?)` Implementation is provided by the parent class. |
| [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#) | `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProvider#query(android.net.Uri,%20kotlin.Array,%20kotlin.String,%20kotlin.Array,%20kotlin.String,%20android.os.CancellationSignal)(uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#, projection: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>?, selection: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, selectionArgs: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>?, sortOrder: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, cancellationSignal: https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#?)` Implementation is provided by the parent class. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProvider#update(android.net.Uri,%20android.content.ContentValues,%20kotlin.String,%20kotlin.Array)(uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#, values: https://developer.android.com/reference/kotlin/android/content/ContentValues.html#!, selection: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, selectionArgs: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>?)` Implementation is provided by the parent class. |

| Inherited functions ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/android/content/ContentProviderResult.html#!>` | `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#applyBatch(kotlin.String,%20java.util.ArrayList)(authority: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, operations: https://developer.android.com/reference/kotlin/java/util/ArrayList.html#<https://developer.android.com/reference/kotlin/android/content/ContentProviderOperation.html#!>)` Override this to handle requests to perform a batch of operations, or the default implementation will iterate over the operations and call `https://developer.android.com/reference/kotlin/android/content/ContentProviderOperation.html#apply(android.content.ContentProvider,%20kotlin.Array,%20kotlin.Int)` on each of them. If all calls to `https://developer.android.com/reference/kotlin/android/content/ContentProviderOperation.html#apply(android.content.ContentProvider,%20kotlin.Array,%20kotlin.Int)` succeed then a `https://developer.android.com/reference/kotlin/android/content/ContentProviderResult.html#` array with as many elements as there were operations will be returned. If any of the calls fail, it is up to the implementation how many of the others take effect. This method can be called from multiple threads, as described in [Processes and Threads](https://developer.android.com/guide/topics/fundamentals/processes-and-threads.html#Threads). <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/android/content/ContentProviderResult.html#!>` | `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#applyBatch(java.util.ArrayList)(operations: https://developer.android.com/reference/kotlin/java/util/ArrayList.html#<https://developer.android.com/reference/kotlin/android/content/ContentProviderOperation.html#!>)` <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#bulkInsert(android.net.Uri,%20kotlin.Array)(uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#, values: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/android/content/ContentValues.html#!>)` Override this to handle requests to insert a set of new rows, or the default implementation will iterate over the values and call #insert on each of them. As a courtesy, call `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#notifyChange(android.net.Uri,%20android.database.ContentObserver)` after inserting. This method can be called from multiple threads, as described in [Processes and Threads](https://developer.android.com/guide/topics/fundamentals/processes-and-threads.html#Threads). <br /> | | `https://developer.android.com/reference/kotlin/android/os/Bundle.html#?` | `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#call(kotlin.String,%20kotlin.String,%20kotlin.String,%20android.os.Bundle)(authority: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, method: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, arg: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, extras: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?)` Call a provider-defined method. This can be used to implement interfaces that are cheaper and/or unnatural for a table-like model. **WARNING:** The framework does no permission checking on this entry into the content provider besides the basic ability for the application to get access to the provider at all. For example, it has no idea whether the call being executed may read or write data in the provider, so can't enforce those individual permissions. Any implementation of this method **must** do its own permission checks on incoming calls to make sure they are allowed. <br /> | | `https://developer.android.com/reference/kotlin/android/content/ContentProvider.CallingIdentity.html#` | `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#clearCallingIdentity()()` Reset the identity of the incoming IPC on the current thread. Internally this calls `https://developer.android.com/reference/kotlin/android/os/Binder.html#clearCallingIdentity()` and also clears any value stored in `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#getCallingPackage()`. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#delete(android.net.Uri,%20android.os.Bundle)(uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#, extras: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?)` Implement this to handle requests to delete one or more rows. The implementation should apply the selection clause when performing deletion, allowing the operation to affect multiple rows in a directory. As a courtesy, call `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#notifyChange(android.net.Uri,%20android.database.ContentObserver)` after deleting. This method can be called from multiple threads, as described in [Processes and Threads](https://developer.android.com/guide/topics/fundamentals/processes-and-threads.html#Threads). The implementation is responsible for parsing out a row ID at the end of the URI, if a specific row is being deleted. That is, the client would pass in `content://contacts/people/22` and the implementation is responsible for parsing the record number (22) when creating a SQL statement. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#dump(java.io.FileDescriptor,%20java.io.PrintWriter,%20kotlin.Array)(fd: https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#!, writer: https://developer.android.com/reference/kotlin/java/io/PrintWriter.html#!, args: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!)` Print the Provider's state into the given stream. This gets invoked if you run "adb shell dumpsys activity provider \<provider_component_name\>". <br /> | | `https://developer.android.com/reference/kotlin/android/content/AttributionSource.html#?` | `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#getCallingAttributionSource()()` Gets the attribution source of the calling app. If you want to attribute the data access to the calling app you can create an attribution context via `https://developer.android.com/reference/kotlin/android/content/Context.html#createContext(android.content.ContextParams)` and passing this identity to `https://developer.android.com/reference/kotlin/android/content/ContextParams.Builder.html#setNextAttributionSource(android.content.AttributionSource)`. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?` | `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#getCallingAttributionTag()()` Return the attribution tag of the caller that initiated the request being processed on the current thread. Returns `null` if not currently processing a request of the request is for the default attribution. This will always return `null` when processing `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#getTypeAnonymous(android.net.Uri)` requests For `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#getType(android.net.Uri)` requests, this will be only available for cases, where the caller can be identified. See `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#getTypeAnonymous(android.net.Uri)` <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?` | `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#getCallingPackage()()` Return the package name of the caller that initiated the request being processed on the current thread. The returned package will have been verified to belong to the calling UID. Returns `null` if not currently processing a request. This will always return `null` when processing `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#getTypeAnonymous(android.net.Uri)` requests For `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#getType(android.net.Uri)` requests, this will be only available for cases, where the caller can be identified. See `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#getTypeAnonymous(android.net.Uri)` <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?` | `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#getCallingPackageUnchecked()()` Return the package name of the caller that initiated the request being processed on the current thread. The returned package will have *not* been verified to belong to the calling UID. Returns `null` if not currently processing a request. This will always return `null` when processing `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#getTypeAnonymous(android.net.Uri)` requests For `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#getType(android.net.Uri)` requests, this will be only available for cases, where the caller can be identified. See `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#getTypeAnonymous(android.net.Uri)` <br /> | | `https://developer.android.com/reference/kotlin/android/content/Context.html#?` | `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#getContext()()` Retrieves the Context this provider is running in. Only available once `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#onCreate()` has been called -- this will return `null` in the constructor. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/android/content/pm/PathPermission.html#!>?` | `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#getPathPermissions()()` Return the path-based permissions required for read and/or write access to this content provider. This method can be called from multiple threads, as described in [Processes and Threads](https://developer.android.com/guide/topics/fundamentals/processes-and-threads.html#Threads). <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?` | `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#getReadPermission()()` Return the name of the permission required for read-only access to this content provider. This method can be called from multiple threads, as described in [Processes and Threads](https://developer.android.com/guide/topics/fundamentals/processes-and-threads.html#Threads). <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>?` | `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#getStreamTypes(android.net.Uri,%20kotlin.String)(uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#, mimeTypeFilter: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Called by a client to determine the types of data streams that this content provider supports for the given URI. The default implementation returns `null`, meaning no types. If your content provider stores data of a particular type, return that MIME type if it matches the given mimeTypeFilter. If it can perform type conversions, return an array of all supported MIME types that match mimeTypeFilter. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?` | `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#getTypeAnonymous(android.net.Uri)(uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#)` Implement this to handle requests for MIME type of URIs, that does not need to reveal any internal information which should be protected by any permission. If your mime type reveals details that should be protected, then you should protect those by implementing those in `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#getType(android.net.Uri)`, and in this function, only return types of URIs which can be obtained by anyone without any access. Implementing ths function will make sure `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#getType(android.net.Uri)` is protected by readPermission. This function by default works as the `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#getType(android.net.Uri)` <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?` | `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#getWritePermission()()` Return the name of the permission required for read/write access to this content provider. This method can be called from multiple threads, as described in [Processes and Threads](https://developer.android.com/guide/topics/fundamentals/processes-and-threads.html#Threads). <br /> | | `https://developer.android.com/reference/kotlin/android/net/Uri.html#?` | `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#insert(android.net.Uri,%20android.content.ContentValues,%20android.os.Bundle)(uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#, values: https://developer.android.com/reference/kotlin/android/content/ContentValues.html#?, extras: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?)` Implement this to handle requests to insert a new row. As a courtesy, call `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#notifyChange(android.net.Uri,%20android.database.ContentObserver)` after inserting. This method can be called from multiple threads, as described in [Processes and Threads](https://developer.android.com/guide/topics/fundamentals/processes-and-threads.html#Threads). <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#isTemporary()()` Returns true if this instance is a temporary content provider. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#onCallingPackageChanged()()` Called whenever the value of `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#getCallingPackage()` changes, giving the provider an opportunity to invalidate any security related caching it may be performing. This typically happens when a `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#` makes a nested call back into itself when already processing a call from a remote process. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#onConfigurationChanged(android.content.res.Configuration)(newConfig: https://developer.android.com/reference/kotlin/android/content/res/Configuration.html#)` Called by the system when the device configuration changes while your component is running. Note that, unlike activities, other components are never restarted when a configuration changes: they must always deal with the results of the change, such as by re-retrieving resources. At the time that this function has been called, your Resources object will have been updated to return resource values matching the new configuration. For more information, read [Handling Runtime Changes](https://developer.android.com/guide/topics/resources/runtime-changes.html). This method is always called on the application main thread, and must not perform lengthy operations. The default content provider implementation does nothing. Override this method to take appropriate action. (Content providers do not usually care about things like screen orientation, but may want to know about locale changes.) <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#onCreate()()` Implement this to initialize your content provider on startup. This method is called for all registered content providers on the application main thread at application launch time. It must not perform lengthy operations, or application startup will be delayed. You should defer nontrivial initialization (such as opening, upgrading, and scanning databases) until the content provider is used (via #query, #insert, etc). Deferred initialization keeps application startup fast, avoids unnecessary work if the provider turns out not to be needed, and stops database errors (such as a full disk) from halting application launch. If you use SQLite, `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteOpenHelper.html#` is a helpful utility class that makes it easy to manage databases, and will automatically defer opening until first use. If you do use SQLiteOpenHelper, make sure to avoid calling `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteOpenHelper.html#getReadableDatabase()` or `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteOpenHelper.html#getWritableDatabase()` from this method. (Instead, override `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteOpenHelper.html#onOpen(android.database.sqlite.SQLiteDatabase)` to initialize the database when it is first opened.) <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#onLowMemory()()` This is called when the overall system is running low on memory, and actively running processes should trim their memory usage. While the exact point at which this will be called is not defined, generally it will happen when all background process have been killed. That is, before reaching the point of killing processes hosting service and foreground UI that we would like to avoid killing. This method is always called on the application main thread, and must not perform lengthy operations. The default content provider implementation does nothing. Subclasses may override this method to take appropriate action. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#onTrimMemory(kotlin.Int)(level: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Called when the operating system has determined that it is a good time for a process to trim unneeded memory from its process. You should never compare to exact values of the level, since new intermediate values may be added -- you will typically want to compare if the value is greater or equal to a level you are interested in. To retrieve the processes current trim level at any point, you can use `https://developer.android.com/reference/kotlin/android/app/ActivityManager.html#getMyMemoryState(android.app.ActivityManager.RunningAppProcessInfo)`. <br /> | | `https://developer.android.com/reference/kotlin/android/content/res/AssetFileDescriptor.html#?` | `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#openAssetFile(android.net.Uri,%20kotlin.String)(uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#, mode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` This is like #openFile, but can be implemented by providers that need to be able to return sub-sections of files, often assets inside of their .apk. This method can be called from multiple threads, as described in [Processes and Threads](https://developer.android.com/guide/topics/fundamentals/processes-and-threads.html#Threads). If you implement this, your clients must be able to deal with such file slices, either directly with android.content.ContentResolver#openAssetFileDescriptor, or by using the higher-level `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#openInputStream(android.net.Uri)` or android.content.ContentResolver#openOutputStream methods. The returned AssetFileDescriptor can be a pipe or socket pair to enable streaming of data. If you are implementing this to return a full file, you should create the AssetFileDescriptor with `https://developer.android.com/reference/kotlin/android/content/res/AssetFileDescriptor.html#UNKNOWN_LENGTH:kotlin.Long` to be compatible with applications that cannot handle sub-sections of files. For use in Intents, you will want to implement `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#getType(android.net.Uri)` to return the appropriate MIME type for the data returned here with the same URI. This will allow intent resolution to automatically determine the data MIME type and select the appropriate matching targets as part of its operation. For better interoperability with other applications, it is recommended that for any URIs that can be opened, you also support queries on them containing at least the columns specified by `https://developer.android.com/reference/kotlin/android/provider/OpenableColumns`. <br /> | | `https://developer.android.com/reference/kotlin/android/content/res/AssetFileDescriptor.html#?` | `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#openAssetFile(android.net.Uri,%20kotlin.String,%20android.os.CancellationSignal)(uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#, mode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, signal: https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#?)` This is like #openFile, but can be implemented by providers that need to be able to return sub-sections of files, often assets inside of their .apk. This method can be called from multiple threads, as described in [Processes and Threads](https://developer.android.com/guide/topics/fundamentals/processes-and-threads.html#Threads). If you implement this, your clients must be able to deal with such file slices, either directly with android.content.ContentResolver#openAssetFileDescriptor, or by using the higher-level `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#openInputStream(android.net.Uri)` or android.content.ContentResolver#openOutputStream methods. The returned AssetFileDescriptor can be a pipe or socket pair to enable streaming of data. If you are implementing this to return a full file, you should create the AssetFileDescriptor with `https://developer.android.com/reference/kotlin/android/content/res/AssetFileDescriptor.html#UNKNOWN_LENGTH:kotlin.Long` to be compatible with applications that cannot handle sub-sections of files. For use in Intents, you will want to implement `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#getType(android.net.Uri)` to return the appropriate MIME type for the data returned here with the same URI. This will allow intent resolution to automatically determine the data MIME type and select the appropriate matching targets as part of its operation. For better interoperability with other applications, it is recommended that for any URIs that can be opened, you also support queries on them containing at least the columns specified by `https://developer.android.com/reference/kotlin/android/provider/OpenableColumns`. <br /> | | `https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#` | `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#openFileHelper(android.net.Uri,%20kotlin.String)(uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#, mode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Convenience for subclasses that wish to implement #openFile by looking up a column named "_data" at the given URI. <br /> | | `https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#` | `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#openPipeHelper(android.net.Uri,%20kotlin.String,%20android.os.Bundle,%20android.content.ContentProvider.openPipeHelper.T,%20android.content.ContentProvider.PipeDataWriter)(uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#, mimeType: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, opts: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?, args: T?, func: https://developer.android.com/reference/kotlin/android/content/ContentProvider.PipeDataWriter.html#<T>)` A helper function for implementing #openTypedAssetFile, for creating a data pipe and background thread allowing you to stream generated data back to the client. This function returns a new ParcelFileDescriptor that should be returned to the caller (the caller is responsible for closing it). <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#refresh(android.net.Uri,%20android.os.Bundle,%20android.os.CancellationSignal)(uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#!, extras: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?, cancellationSignal: https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#?)` Implement this to support refresh of content identified by `uri`. By default, this method returns false; providers who wish to implement this should return true to signal the client that the provider has tried refreshing with its own implementation. This allows clients to request an explicit refresh of content identified by `uri`. Client code should only invoke this method when there is a strong indication (such as a user initiated pull to refresh gesture) that the content is stale. Remember to send `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#notifyChange(android.net.Uri,%20android.database.ContentObserver)` notifications when content changes. <br /> | | `https://developer.android.com/reference/kotlin/android/content/Context.html#` | `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#requireContext()()` Retrieves a Non-Nullable Context this provider is running in, this is intended to be called after `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#onCreate()`. When called before context was created, an IllegalStateException will be thrown. Note A provider must be declared in the manifest and created automatically by the system, and context is only available after `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#onCreate()` is called. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#restoreCallingIdentity(android.content.ContentProvider.CallingIdentity)(identity: https://developer.android.com/reference/kotlin/android/content/ContentProvider.CallingIdentity.html#)` Restore the identity of the incoming IPC on the current thread back to a previously identity that was returned by `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#clearCallingIdentity()`. Internally this calls `https://developer.android.com/reference/kotlin/android/os/Binder.html#restoreCallingIdentity(kotlin.Long)` and also restores any value stored in `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#getCallingPackage()`. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#setPathPermissions(kotlin.Array)(permissions: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/android/content/pm/PathPermission.html#!>?)` Change the path-based permission required to read and/or write data in the content provider. This is normally set for you from its manifest information when the provider is first created. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#setReadPermission(kotlin.String)(permission: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?)` Change the permission required to read data from the content provider. This is normally set for you from its manifest information when the provider is first created. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#setWritePermission(kotlin.String)(permission: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?)` Change the permission required to read and write data in the content provider. This is normally set for you from its manifest information when the provider is first created. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#shutdown()()` Implement this to shut down the ContentProvider instance. You can then invoke this method in unit tests. Android normally handles ContentProvider startup and shutdown automatically. You do not need to start up or shut down a ContentProvider. When you invoke a test method on a ContentProvider, however, a ContentProvider instance is started and keeps running after the test finishes, even if a succeeding test instantiates another ContentProvider. A conflict develops because the two instances are usually running against the same underlying data source (for example, an sqlite database). Implementing shutDown() avoids this conflict by providing a way to terminate the ContentProvider. This method can also prevent memory leaks from multiple instantiations of the ContentProvider, and it can ensure unit test isolation by allowing you to completely clean up the test fixture before moving on to the next test. <br /> | | `https://developer.android.com/reference/kotlin/android/net/Uri.html#?` | `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#uncanonicalize(android.net.Uri)(url: https://developer.android.com/reference/kotlin/android/net/Uri.html#)` Remove canonicalization from canonical URIs previously returned by `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#canonicalize(android.net.Uri)`. For example, if your implementation is to add a query param to canonicalize a URI, this method can simply trip any query params on the URI. The default implementation always returns the same url that was passed in. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#update(android.net.Uri,%20android.content.ContentValues,%20android.os.Bundle)(uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#, values: https://developer.android.com/reference/kotlin/android/content/ContentValues.html#?, extras: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?)` Implement this to handle requests to update one or more rows. The implementation should update all rows matching the selection to set the columns according to the provided values map. As a courtesy, call `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#notifyChange(android.net.Uri,%20android.database.ContentObserver)` after updating. This method can be called from multiple threads, as described in [Processes and Threads](https://developer.android.com/guide/topics/fundamentals/processes-and-threads.html#Threads). <br /> | ||
| From class `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks.html#onConfigurationChanged(android.content.res.Configuration)(newConfig: https://developer.android.com/reference/kotlin/android/content/res/Configuration.html#)` Called by the system when the device configuration changes while your component is running. Note that, unlike activities, other components are never restarted when a configuration changes: they must always deal with the results of the change, such as by re-retrieving resources. At the time that this function has been called, your Resources object will have been updated to return resource values matching the new configuration. For more information, read [Handling Runtime Changes](https://developer.android.com/guide/topics/resources/runtime-changes.html). <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks.html#onLowMemory()()` This is called when the overall system is running low on memory, and actively running processes should trim their memory usage. While the exact point at which this will be called is not defined, generally it will happen when all background process have been killed. That is, before reaching the point of killing processes hosting service and foreground UI that we would like to avoid killing. <br /> | ||

## Public constructors

### CloudMediaProvider

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [R Extensions 3](https://developer.android.com/sdkExtensions)

```
CloudMediaProvider()
```

## Public methods

### attachInfo

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun attachInfo(
    context: Context, 
    info: ProviderInfo
): Unit
```

Implementation is provided by the parent class. Cannot be overridden.

| Parameters ||
|---|---|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#): This value cannot be `null`. |
| `info` | [ProviderInfo](https://developer.android.com/reference/kotlin/android/content/pm/ProviderInfo.html#): This value cannot be `null`. |

### call

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun call(
    method: String, 
    arg: String?, 
    extras: Bundle?
): Bundle
```

Implementation is provided by the parent class. Cannot be overridden.

| Parameters ||
|---|---|
| `method` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |
| `arg` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: This value may be `null`. |
| `extras` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)?: This value may be `null`. |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/os/Bundle.html#` | This value cannot be `null`. |

### canonicalize

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun canonicalize(uri: Uri): Uri
```

Implementation is provided by the parent class. Throws by default, and cannot be overridden.

| Parameters ||
|---|---|
| `url` | The Uri to canonicalize. This value cannot be `null`. |
| `uri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#): This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/net/Uri.html#` | This value cannot be `null`. |

### delete

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun delete(
    uri: Uri, 
    selection: String?, 
    selectionArgs: Array<String!>?
): Int
```

Implementation is provided by the parent class. Throws by default, and cannot be overridden.

| Parameters ||
|---|---|
| `uri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#): This value cannot be `null`. |
| `selection` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: This value may be `null`. |
| `selectionArgs` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>?: This value may be `null`. |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The number of rows affected. |

| Exceptions ||
|---|---|
| `android.database.SQLException` | |

### getType

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getType(uri: Uri): String
```

Implementation is provided by the parent class. Throws by default, and cannot be overridden.

| Parameters ||
|---|---|
| `uri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#): This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | This value cannot be `null`. |

### insert

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun insert(
    uri: Uri, 
    values: ContentValues!
): Uri
```

Implementation is provided by the parent class. Throws by default, and cannot be overridden.

| Parameters ||
|---|---|
| `uri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#): This value cannot be `null`. |
| `values` | [ContentValues](https://developer.android.com/reference/kotlin/android/content/ContentValues.html#)!: This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/net/Uri.html#` | This value cannot be `null`. |

### onCreateCloudMediaSurfaceController

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [R Extensions 3](https://developer.android.com/sdkExtensions)

```
open fun onCreateCloudMediaSurfaceController(
    config: Bundle, 
    callback: CloudMediaProvider.CloudMediaSurfaceStateChangedCallback
): CloudMediaProvider.CloudMediaSurfaceController?
```

Returns a `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProvider.CloudMediaSurfaceController` used for rendering the preview of media items, or null if preview rendering is not supported.

| Parameters ||
|---|---|
| `config` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#): containing configuration parameters for `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProvider.CloudMediaSurfaceController` - `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProviderContract#EXTRA_LOOPING_PLAYBACK_ENABLED:kotlin.String` - `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProviderContract#EXTRA_SURFACE_CONTROLLER_AUDIO_MUTE_ENABLED:kotlin.String` . This value cannot be `null`. |
| `callback` | [CloudMediaProvider.CloudMediaSurfaceStateChangedCallback](https://developer.android.com/reference/kotlin/android/provider/CloudMediaProvider.CloudMediaSurfaceStateChangedCallback): `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProvider.CloudMediaSurfaceStateChangedCallback` to send state updates for `https://developer.android.com/reference/kotlin/android/view/Surface.html#` to picker launched via `https://developer.android.com/reference/kotlin/android/provider/MediaStore#ACTION_PICK_IMAGES:kotlin.String` This value cannot be `null`. |

### onGetCapabilities

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [R Extensions 16](https://developer.android.com/sdkExtensions)

```
open fun onGetCapabilities(): CloudMediaProviderContract.Capabilities
```

Returns the `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProviderContract.Capabilities` of this CloudMediaProvider. This object is used to determine which APIs can be safely invoked during runtime. If not overridden the default capabilities are used. IMPORTANT: This method is performance critical and should avoid long running or expensive operations.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProviderContract.Capabilities` | This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProviderContract.Capabilities`

### onGetMediaCollectionInfo

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [R Extensions 3](https://developer.android.com/sdkExtensions)

```
abstract fun onGetMediaCollectionInfo(extras: Bundle): Bundle
```

Returns metadata about the media collection itself.

This is useful for the OS to determine if its cache of media items in the collection is still valid and if a full or incremental sync is required with `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProvider#onQueryMedia(android.os.Bundle)`.

This method might be called by the OS frequently and is performance critical, hence it should avoid long running operations.

If the provider handled any filters in `extras`, it must add the key to the `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#EXTRA_HONORED_ARGS:kotlin.String` as part of the returned `https://developer.android.com/reference/kotlin/android/os/Bundle.html#`. Consistent failures to return valid media collection info may result in changing the active cloud media provider serving the photopicker.

| Parameters ||
|---|---|
| `extras` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#): containing keys to filter result: - `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProviderContract#EXTRA_ALBUM_ID:kotlin.String` . This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/os/Bundle.html#` | `https://developer.android.com/reference/kotlin/android/os/Bundle.html#` containing `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProviderContract.MediaCollectionInfo` - `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProviderContract.MediaCollectionInfo#MEDIA_COLLECTION_ID:kotlin.String` - `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProviderContract.MediaCollectionInfo#LAST_MEDIA_SYNC_GENERATION:kotlin.String` - `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProviderContract.MediaCollectionInfo#ACCOUNT_NAME:kotlin.String` - `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProviderContract.MediaCollectionInfo#ACCOUNT_CONFIGURATION_INTENT:kotlin.String` . This value cannot be `null`. |

### onOpenMedia

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [R Extensions 3](https://developer.android.com/sdkExtensions)

```
abstract fun onOpenMedia(
    mediaId: String, 
    extras: Bundle?, 
    signal: CancellationSignal?
): ParcelFileDescriptor
```

Returns the full size media item identified by `mediaId`.

If you block while downloading content, you should periodically check `https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#isCanceled()` to abort abandoned open requests.

| Parameters ||
|---|---|
| `mediaId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the media item to return. This value cannot be `null`. |
| `extras` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)?: to modify the way the fd is opened, there's none at the moment, but some might be implemented in the future. This value may be `null`. |
| `signal` | [CancellationSignal](https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#)?: used by the OS to signal if the request should be cancelled. This value may be `null`. |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#` | read-only file descriptor for accessing the media file. This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProvider#onOpenPreview(kotlin.String,%20android.graphics.Point,%20android.os.Bundle,%20android.os.CancellationSignal)`

### onOpenPreview

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [R Extensions 3](https://developer.android.com/sdkExtensions)

```
abstract fun onOpenPreview(
    mediaId: String, 
    size: Point, 
    extras: Bundle?, 
    signal: CancellationSignal?
): AssetFileDescriptor
```

Returns a thumbnail of `size` for a media item identified by `mediaId`

The cloud media provider should strictly return thumbnail in the original `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProviderContract.MediaColumns#MIME_TYPE:kotlin.String` of the item.

This is expected to be a much lower resolution version than the item returned by `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProvider#onOpenMedia(kotlin.String,%20android.os.Bundle,%20android.os.CancellationSignal)`.

If you block while downloading content, you should periodically check `https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#isCanceled()` to abort abandoned open requests.

| Parameters ||
|---|---|
| `mediaId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the media item to return. This value cannot be `null`. |
| `size` | [Point](https://developer.android.com/reference/kotlin/android/graphics/Point.html#): the dimensions of the thumbnail to return. The returned file descriptor doesn't have to match the `size` precisely because the OS will adjust the dimensions before usage. Implementations can return close approximations especially if the approximation is already locally on the device and doesn't require downloading from the cloud. This value cannot be `null`. |
| `extras` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)?: to modify the way the fd is opened, e.g. for video files we may request a thumbnail image instead of a video with `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProviderContract#EXTRA_PREVIEW_THUMBNAIL:kotlin.String`. In the absence of this extra, this method must return a descriptor representing the actual media file, otherwise it should return the thumbnail. Failure in returning the same may cause unexpected media preview behaviour in the photopicker. This value may be `null`. |
| --- | --- |
| `signal` | [CancellationSignal](https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#)?: used by the OS to signal if the request should be cancelled. This value may be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/res/AssetFileDescriptor.html#` | read-only file descriptor for accessing the thumbnail for the media file. This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProvider#onOpenMedia(kotlin.String,%20android.os.Bundle,%20android.os.CancellationSignal)`
- `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProviderContract#EXTRA_PREVIEW_THUMBNAIL:kotlin.String`

### onQueryAlbums

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [R Extensions 3](https://developer.android.com/sdkExtensions)

```
open fun onQueryAlbums(extras: Bundle): Cursor
```

Returns a cursor representing all album items in the media collection optionally filtered by `extras` and sorted in reverse chronological order of `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProviderContract.AlbumColumns#DATE_TAKEN_MILLIS:kotlin.String`, i.e. most recent items first.

The cloud media provider must set the `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProviderContract#EXTRA_MEDIA_COLLECTION_ID:kotlin.String` as part of the returned `https://developer.android.com/reference/kotlin/android/database/Cursor.html#setExtras(android.os.Bundle)` `https://developer.android.com/reference/kotlin/android/os/Bundle.html#`. Not setting this is an error and invalidates the returned `https://developer.android.com/reference/kotlin/android/database/Cursor.html#`.

If the provider handled any filters in `extras`, it must add the key to the `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#EXTRA_HONORED_ARGS:kotlin.String` as part of the returned `https://developer.android.com/reference/kotlin/android/database/Cursor.html#setExtras(android.os.Bundle)` `https://developer.android.com/reference/kotlin/android/os/Bundle.html#`.

| Parameters ||
|---|---|
| `extras` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#): containing keys to filter album items: - `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProviderContract#EXTRA_SYNC_GENERATION:kotlin.String` - `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProviderContract#EXTRA_PAGE_TOKEN:kotlin.String` - `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProviderContract#EXTRA_PAGE_SIZE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_MIME_TYPES:kotlin.String` . This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/database/Cursor.html#` | cursor representing album items containing all `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProviderContract.AlbumColumns` columns. This value cannot be `null`. |

### onQueryDeletedMedia

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [R Extensions 3](https://developer.android.com/sdkExtensions)

```
abstract fun onQueryDeletedMedia(extras: Bundle): Cursor
```

Returns a `https://developer.android.com/reference/kotlin/android/database/Cursor.html#` representing all deleted media items in the entire media collection within the current provider version as returned by `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProvider#onGetMediaCollectionInfo(android.os.Bundle)`. These items can be optionally filtered by `extras`.

The cloud media provider must set the `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProviderContract#EXTRA_MEDIA_COLLECTION_ID:kotlin.String` as part of the returned `https://developer.android.com/reference/kotlin/android/database/Cursor.html#setExtras(android.os.Bundle)` `https://developer.android.com/reference/kotlin/android/os/Bundle.html#`. Not setting this is an error and invalidates the returned `https://developer.android.com/reference/kotlin/android/database/Cursor.html#`.

If the provider handled any filters in `extras`, it must add the key to the `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#EXTRA_HONORED_ARGS:kotlin.String` as part of the returned `https://developer.android.com/reference/kotlin/android/database/Cursor.html#setExtras(android.os.Bundle)` `https://developer.android.com/reference/kotlin/android/os/Bundle.html#`.

| Parameters ||
|---|---|
| `extras` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#): containing keys to filter deleted media items: - `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProviderContract#EXTRA_SYNC_GENERATION:kotlin.String` - `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProviderContract#EXTRA_PAGE_TOKEN:kotlin.String` . This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/database/Cursor.html#` | cursor representing deleted media items containing just the `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProviderContract.MediaColumns#ID:kotlin.String` column. This value cannot be `null`. |

### onQueryMedia

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [R Extensions 3](https://developer.android.com/sdkExtensions)

```
abstract fun onQueryMedia(extras: Bundle): Cursor
```

Returns a cursor representing all media items in the media collection optionally filtered by `extras` and sorted in reverse chronological order of `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProviderContract.MediaColumns#DATE_TAKEN_MILLIS:kotlin.String`, i.e. most recent items first.

The cloud media provider must set the `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProviderContract#EXTRA_MEDIA_COLLECTION_ID:kotlin.String` as part of the returned `https://developer.android.com/reference/kotlin/android/database/Cursor.html#setExtras(android.os.Bundle)` `https://developer.android.com/reference/kotlin/android/os/Bundle.html#`. Not setting this is an error and invalidates the returned `https://developer.android.com/reference/kotlin/android/database/Cursor.html#`.

If the cloud media provider handled any filters in `extras`, it must add the key to the `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#EXTRA_HONORED_ARGS:kotlin.String` as part of the returned `https://developer.android.com/reference/kotlin/android/database/Cursor.html#setExtras(android.os.Bundle)` `https://developer.android.com/reference/kotlin/android/os/Bundle.html#`.

| Parameters ||
|---|---|
| `extras` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#): containing keys to filter media items: - `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProviderContract#EXTRA_SYNC_GENERATION:kotlin.String` - `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProviderContract#EXTRA_PAGE_TOKEN:kotlin.String` - `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProviderContract#EXTRA_ALBUM_ID:kotlin.String` - `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProviderContract#EXTRA_PAGE_SIZE:kotlin.String` . This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/database/Cursor.html#` | cursor representing media items containing all `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProviderContract.MediaColumns` columns. This value cannot be `null`. |

### onQueryMediaCategories

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [R Extensions 16](https://developer.android.com/sdkExtensions)

```
open fun onQueryMediaCategories(
    parentCategoryId: String?, 
    extras: Bundle, 
    cancellationSignal: CancellationSignal?
): Cursor
```

Queries for the available MediaCategories under the given `parentCategoryId`, filtered by `extras`. The columns of MediaCategories are in the class `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProviderContract.MediaCategoryColumns`.

When `parentCategoryId` is null, this returns the root categories.

The order in which media categories are sorted in the cursor will be retained when displaying results to the user.

The cloud media provider must set the `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProviderContract#EXTRA_MEDIA_COLLECTION_ID:kotlin.String` as part of the returned cursor by using `https://developer.android.com/reference/kotlin/android/database/Cursor.html#setExtras(android.os.Bundle)`. Not setting this is an error and invalidates the returned `https://developer.android.com/reference/kotlin/android/database/Cursor.html#`, meaning photo picker will not use the cursor for any operation.

`extras` may contain some key-value pairs which should be used to filter the results. If the provider handled any filters in `extras`, it must add the key to the `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#EXTRA_HONORED_ARGS:kotlin.String` as part of the returned cursor by using `https://developer.android.com/reference/kotlin/android/database/Cursor.html#setExtras(android.os.Bundle)`. If not honored, photo picker will assume the result of the query is without the extra being used. Note: Currently this function does not pass any params in `extras`.

| Parameters ||
|---|---|
| `parentCategoryId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: the ID of the parent category to filter media categories. This value may be `null`. |
| `extras` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#): containing keys to filter media categories: - `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_MIME_TYPES:kotlin.String` . This value cannot be `null`. |
| `cancellationSignal` | [CancellationSignal](https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#)?: `https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#` to check if request has been cancelled. This value may be `null`. |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/database/Cursor.html#` | cursor with `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProviderContract.MediaCategoryColumns` columns |

### onQueryMediaInMediaSet

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [R Extensions 16](https://developer.android.com/sdkExtensions)

```
open fun onQueryMediaInMediaSet(
    mediaSetId: String, 
    extras: Bundle, 
    cancellationSignal: CancellationSignal?
): Cursor
```

Queries for the available media items under a given `mediaSetId`, filtered by `extras`. The columns of Media are in the class `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProviderContract.MediaColumns`. `mediaSetId` is the ID given as part of `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProviderContract.MediaSetColumns#ID:kotlin.String`

The order in which media items are sorted in the cursor will be retained when displaying results to the user.

The cloud media provider must set the `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProviderContract#EXTRA_MEDIA_COLLECTION_ID:kotlin.String` as part of the returned `https://developer.android.com/reference/kotlin/android/database/Cursor.html#` by using `https://developer.android.com/reference/kotlin/android/database/Cursor.html#setExtras(android.os.Bundle)`. Not setting this is an error and invalidates the returned `https://developer.android.com/reference/kotlin/android/database/Cursor.html#`, meaning photo picker will not use the cursor for any operation.

`extras` may contain some key-value pairs which should be used to prepare the results. If the provider handled any filters in `extras`, it must add the key to the `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#EXTRA_HONORED_ARGS:kotlin.String` as part of the returned cursor by using `https://developer.android.com/reference/kotlin/android/database/Cursor.html#setExtras(android.os.Bundle)`. If not honored, photo picker will assume the result of the query is without the extra being used.

If the cloud media provider supports pagination, they can set `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProviderContract#EXTRA_PAGE_TOKEN:kotlin.String` as the next page token, as part of the returned cursor by using `https://developer.android.com/reference/kotlin/android/database/Cursor.html#setExtras(android.os.Bundle)`. If a token is set, the OS will pass it as a key-value pair in `extras` when querying for media for subsequent pages. The provider can keep returning pagination tokens in the returned cursor by using `https://developer.android.com/reference/kotlin/android/database/Cursor.html#setExtras(android.os.Bundle)` until the last page at which point it should not set a token in the returned cursor.

| Parameters ||
|---|---|
| `mediaSetId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the ID of the media set to filter media items. This value cannot be `null`. |
| `extras` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#): containing keys to filter media items: - `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProviderContract#EXTRA_PAGE_TOKEN:kotlin.String` - `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProviderContract#EXTRA_PAGE_SIZE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProviderContract#EXTRA_SORT_ORDER:kotlin.String` - `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_MIME_TYPES:kotlin.String` . This value cannot be `null`. |
| `cancellationSignal` | [CancellationSignal](https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#)?: `https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#` to check if request has been cancelled. This value may be `null`. |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/database/Cursor.html#` | cursor representing `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProviderContract.MediaColumns` columns. This value cannot be `null`. |

### onQueryMediaSets

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [R Extensions 16](https://developer.android.com/sdkExtensions)

```
open fun onQueryMediaSets(
    mediaCategoryId: String, 
    extras: Bundle, 
    cancellationSignal: CancellationSignal?
): Cursor
```

Queries for the available MediaSets under a given `mediaCategoryId`, filtered by `extras`. The columns of MediaSet are in the class `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProviderContract.MediaSetColumns`.

This returns MediaSets directly inside the given MediaCategoryId. If the passed mediaCategoryId has some more nested mediaCategories, the mediaSets inside the nested mediaCategories must not be returned in this response.

The order in which media sets are sorted in the cursor will be retained when displaying results to the user.

The cloud media provider must set the `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProviderContract#EXTRA_MEDIA_COLLECTION_ID:kotlin.String` as part of the returned cursor by using `https://developer.android.com/reference/kotlin/android/database/Cursor.html#setExtras(android.os.Bundle)` . Not setting this is an error and invalidates the returned `https://developer.android.com/reference/kotlin/android/database/Cursor.html#`, meaning photo picker will not use the cursor for any operation.

`extras` may contain some key-value pairs which should be used to prepare the results. If the provider handled any filters in `extras`, it must add the key to the `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#EXTRA_HONORED_ARGS:kotlin.String` as part of the returned cursor by using `https://developer.android.com/reference/kotlin/android/database/Cursor.html#setExtras(android.os.Bundle)`. If not honored, photo picker will assume the result of the query is without the extra being used.

If the cloud media provider supports pagination, they can set `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProviderContract#EXTRA_PAGE_TOKEN:kotlin.String` as the next page token, as part of the returned cursor by using `https://developer.android.com/reference/kotlin/android/database/Cursor.html#setExtras(android.os.Bundle)`. If a token is set, the OS will pass it as a key-value pair in `extras` when querying for query media sets for subsequent pages. The provider can keep returning pagination tokens in the returned cursor by using `https://developer.android.com/reference/kotlin/android/database/Cursor.html#setExtras(android.os.Bundle)` until the last page at which point it should not set a token in the returned cursor.

| Parameters ||
|---|---|
| `mediaCategoryId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the ID of the media category to filter media sets. This value cannot be `null`. |
| `extras` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#): containing keys to filter media sets: - `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProviderContract#EXTRA_PAGE_TOKEN:kotlin.String` - `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProviderContract#EXTRA_PAGE_SIZE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_MIME_TYPES:kotlin.String` . This value cannot be `null`. |
| `cancellationSignal` | [CancellationSignal](https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#)?: `https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#` to check if request has been cancelled. This value may be `null`. |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/database/Cursor.html#` | cursor representing `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProviderContract.MediaSetColumns` columns. This value cannot be `null`. |

### onQuerySearchSuggestions

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [R Extensions 16](https://developer.android.com/sdkExtensions)

```
open fun onQuerySearchSuggestions(
    prefixText: String, 
    extras: Bundle, 
    cancellationSignal: CancellationSignal?
): Cursor
```

Queries for the available SearchSuggestions based on a `prefixText`, filtered by `extras`. The columns of SearchSuggestions are in the class `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProviderContract.SearchSuggestionColumns`

If the user has not started typing, this is considered as zero state suggestion. In this case `prefixText` will be empty string.

The order in which suggestions are sorted in the cursor will be retained when displaying results to the user.

The cloud media provider must set the `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProviderContract#EXTRA_MEDIA_COLLECTION_ID:kotlin.String` as part of the returned cursor by using `https://developer.android.com/reference/kotlin/android/database/Cursor.html#setExtras(android.os.Bundle)` . Not setting this is an error and invalidates the returned `https://developer.android.com/reference/kotlin/android/database/Cursor.html#`, meaning photo picker will not use the cursor for any operation.

`extras` may contain some key-value pairs which should be used to prepare the results. If the provider handled any params in `extras`, it must add the key to the `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#EXTRA_HONORED_ARGS:kotlin.String` as part of the returned cursor by using `https://developer.android.com/reference/kotlin/android/database/Cursor.html#setExtras(android.os.Bundle)`. If not honored, photo picker will assume the result of the query is without the extra being used. Note: Currently this function does not pass any key-value params in `extras`.

Results may not be displayed if it takes longer than 300 milliseconds to get a response from the cloud media provider.

| Parameters ||
|---|---|
| `prefixText` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the prefix text to filter search suggestions. This value cannot be `null`. |
| `extras` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#): containing keys to filter search suggestions. - `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProviderContract#EXTRA_PAGE_SIZE:kotlin.String` . This value cannot be `null`. |
| `cancellationSignal` | [CancellationSignal](https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#)?: `https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#` to check if request has been cancelled. This value may be `null`. |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/database/Cursor.html#` | cursor representing search suggestions containing all `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProviderContract.SearchSuggestionColumns` columns. This value cannot be `null`. |

### onSearchMedia

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [R Extensions 16](https://developer.android.com/sdkExtensions)

```
open fun onSearchMedia(
    searchText: String, 
    extras: Bundle, 
    cancellationSignal: CancellationSignal?
): Cursor
```

Searches media items based on entered search text, managed by `extras` and returns a cursor of `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProviderContract.MediaColumns` based on the match.

The cloud media provider must set the `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProviderContract#EXTRA_MEDIA_COLLECTION_ID:kotlin.String` as part of the returned cursor by using `https://developer.android.com/reference/kotlin/android/database/Cursor.html#setExtras(android.os.Bundle)` . Not setting this is an error and invalidates the returned `https://developer.android.com/reference/kotlin/android/database/Cursor.html#`, meaning photo picker will not use the cursor for any operation.

`extras` may contain some key-value pairs which should be used to prepare the results. If the provider handled any params in `extras`, it must add the key to the `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#EXTRA_HONORED_ARGS:kotlin.String` as part of the returned cursor by using `https://developer.android.com/reference/kotlin/android/database/Cursor.html#setExtras(android.os.Bundle)`. If not honored, photo picker will assume the result of the query is without the extra being used.

An example user journey:

1. User enters the search prompt.
2. Using `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProvider#onQuerySearchSuggestions(kotlin.String,%20android.os.Bundle,%20android.os.CancellationSignal)`, photo picker display suggestions as the user keeps typing.
3. User types completely and then enters search, Photo picker calls: `onSearchMedia(searchText, extras)`

If the cloud media provider supports pagination, they can set `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProviderContract#EXTRA_PAGE_TOKEN:kotlin.String` as the next page token, as part of the returned cursor by using `https://developer.android.com/reference/kotlin/android/database/Cursor.html#setExtras(android.os.Bundle)`. If a token is set, the OS will pass it as a key value pair in `extras` when querying for search media for subsequent pages. The provider can keep returning pagination tokens in the returned cursor by using `https://developer.android.com/reference/kotlin/android/database/Cursor.html#setExtras(android.os.Bundle)` until the last page at which point it should not set a token in the returned cursor.

Results may not be displayed if it takes longer than 3 seconds to get a paged response from the cloud media provider.

| Parameters ||
|---|---|
| `searchText` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): search text to be used. This value cannot be `null`. |
| `extras` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#): containing keys to manage the search results: - `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProviderContract#EXTRA_PAGE_TOKEN:kotlin.String` - `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProviderContract#EXTRA_PAGE_SIZE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProviderContract#EXTRA_SORT_ORDER:kotlin.String` - `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_MIME_TYPES:kotlin.String` . This value cannot be `null`. |
| `cancellationSignal` | [CancellationSignal](https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#)?: `https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#` to check if request has been cancelled. This value may be `null`. |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/database/Cursor.html#` | cursor of `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProviderContract.MediaColumns` based on the match. This value cannot be `null`. |

### onSearchMedia

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [R Extensions 16](https://developer.android.com/sdkExtensions)

```
open fun onSearchMedia(
    suggestedMediaSetId: String, 
    fallbackSearchText: String?, 
    extras: Bundle, 
    cancellationSignal: CancellationSignal?
): Cursor
```

Searches media items based on a selected suggestion, managed by `extras` and returns a cursor of `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProviderContract.MediaColumns` based on the match.

The cloud media provider must set the `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProviderContract#EXTRA_MEDIA_COLLECTION_ID:kotlin.String` as part of the returned cursor by using `https://developer.android.com/reference/kotlin/android/database/Cursor.html#setExtras(android.os.Bundle)` . Not setting this is an error and invalidates the returned `https://developer.android.com/reference/kotlin/android/database/Cursor.html#`, meaning photo picker will not use the cursor for any operation.

`extras` may contain some key-value pairs which should be used to prepare the results. If the provider handled any params in `extras`, it must add the key to the `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#EXTRA_HONORED_ARGS:kotlin.String` as part of the returned cursor by using `https://developer.android.com/reference/kotlin/android/database/Cursor.html#setExtras(android.os.Bundle)`. If not honored, photo picker will assume the result of the query is without the extra being used.

An example user journey:

1. User enters the search prompt.
2. Using `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProvider#onQuerySearchSuggestions(kotlin.String,%20android.os.Bundle,%20android.os.CancellationSignal)`, photo picker display suggestions as the user keeps typing.
3. User selects a suggestion, Photo picker calls: `onSearchMedia(suggestedMediaSetId, fallbackSearchText, extras)` with the `suggestedMediaSetId` corresponding to the user chosen suggestion. `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProviderContract.SearchSuggestionColumns#MEDIA_SET_ID:kotlin.String`

If the cloud media provider supports pagination, they can set `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProviderContract#EXTRA_PAGE_TOKEN:kotlin.String` as the next page token, as part of the returned cursor by using `https://developer.android.com/reference/kotlin/android/database/Cursor.html#setExtras(android.os.Bundle)`. If a token is set, the OS will pass it as a key value pair in `extras` when querying for search media for subsequent pages. The provider can keep returning pagination tokens in the returned cursor by using `https://developer.android.com/reference/kotlin/android/database/Cursor.html#setExtras(android.os.Bundle)` until the last page at which point it should not set a token in the returned cursor

Results may not be displayed if it takes longer than 3 seconds to get a paged response from the cloud media provider.

| Parameters ||
|---|---|
| `suggestedMediaSetId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the media set ID of the suggestion that the user wants to search. This value cannot be `null`. |
| `fallbackSearchText` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: optional search text to be used when `suggestedMediaSetId` is not useful. This value may be `null`. |
| `extras` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#): containing keys to manage the search results: - `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProviderContract#EXTRA_PAGE_TOKEN:kotlin.String` - `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProviderContract#EXTRA_PAGE_SIZE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProviderContract#EXTRA_SORT_ORDER:kotlin.String` - `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_MIME_TYPES:kotlin.String` . This value cannot be `null`. |
| --- | --- |
| `cancellationSignal` | [CancellationSignal](https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#)?: `https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#` to check if request has been cancelled. This value may be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/database/Cursor.html#` | cursor of `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProviderContract.MediaColumns` based on the match. This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProviderContract.SearchSuggestionColumns#MEDIA_SET_ID:kotlin.String`

### openFile

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun openFile(
    uri: Uri, 
    mode: String
): ParcelFileDescriptor
```

Implementation is provided by the parent class. Cannot be overridden.

| Parameters ||
|---|---|
| `uri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#): This value cannot be `null`. |
| `mode` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#` | This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.io.FileNotFoundException` | Throws FileNotFoundException if there is no file associated with the given URI or the mode is invalid. |
| `java.lang.SecurityException` | Throws SecurityException if the caller does not have permission to access the file. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProvider#onOpenMedia(kotlin.String,%20android.os.Bundle,%20android.os.CancellationSignal)`

### openFile

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun openFile(
    uri: Uri, 
    mode: String, 
    signal: CancellationSignal?
): ParcelFileDescriptor
```

Implementation is provided by the parent class. Cannot be overridden.

| Parameters ||
|---|---|
| `uri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#): This value cannot be `null`. |
| `mode` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |
| `signal` | [CancellationSignal](https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#)?: This value may be `null`. |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#` | This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.io.FileNotFoundException` | Throws FileNotFoundException if there is no file associated with the given URI or the mode is invalid. |
| `java.lang.SecurityException` | Throws SecurityException if the caller does not have permission to access the file. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProvider#onOpenMedia(kotlin.String,%20android.os.Bundle,%20android.os.CancellationSignal)`

### openTypedAssetFile

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun openTypedAssetFile(
    uri: Uri, 
    mimeTypeFilter: String, 
    opts: Bundle?
): AssetFileDescriptor
```

Implementation is provided by the parent class. Cannot be overridden.

| Parameters ||
|---|---|
| `uri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#): This value cannot be `null`. |
| `mimeTypeFilter` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |
| `opts` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)?: This value may be `null`. |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/res/AssetFileDescriptor.html#` | This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.io.FileNotFoundException` | Throws FileNotFoundException if there is no file associated with the given URI or the mode is invalid. |
| `java.lang.IllegalArgumentException` | Throws IllegalArgumentException if the content provider does not support the requested MIME type. |
| `java.lang.SecurityException` | Throws SecurityException if the caller does not have permission to access the data. |
| --- | --- |

**See Also**

- `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProvider#onOpenPreview(kotlin.String,%20android.graphics.Point,%20android.os.Bundle,%20android.os.CancellationSignal)`
- `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProvider#onOpenMedia(kotlin.String,%20android.os.Bundle,%20android.os.CancellationSignal)`

### openTypedAssetFile

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun openTypedAssetFile(
    uri: Uri, 
    mimeTypeFilter: String, 
    opts: Bundle?, 
    signal: CancellationSignal?
): AssetFileDescriptor
```

Implementation is provided by the parent class. Cannot be overridden.

| Parameters ||
|---|---|
| `uri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#): This value cannot be `null`. |
| `mimeTypeFilter` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |
| `opts` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)?: This value may be `null`. |
| --- | --- |
| `signal` | [CancellationSignal](https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#)?: This value may be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/res/AssetFileDescriptor.html#` | This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.io.FileNotFoundException` | Throws FileNotFoundException if there is no file associated with the given URI or the mode is invalid. |
| `java.lang.IllegalArgumentException` | Throws IllegalArgumentException if the content provider does not support the requested MIME type. |
| `java.lang.SecurityException` | Throws SecurityException if the caller does not have permission to access the data. |
| --- | --- |

**See Also**

- `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProvider#onOpenPreview(kotlin.String,%20android.graphics.Point,%20android.os.Bundle,%20android.os.CancellationSignal)`
- `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProvider#onOpenMedia(kotlin.String,%20android.os.Bundle,%20android.os.CancellationSignal)`

### query

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun query(
    uri: Uri, 
    projection: Array<String!>?, 
    queryArgs: Bundle?, 
    cancellationSignal: CancellationSignal?
): Cursor
```

Implementation is provided by the parent class. Cannot be overridden.

| Parameters ||
|---|---|
| `uri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#): This value cannot be `null`. |
| `projection` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>?: This value may be `null`. |
| `queryArgs` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)?: This value may be `null`. |
| --- | --- |
| `cancellationSignal` | [CancellationSignal](https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#)?: This value may be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/database/Cursor.html#` | This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProvider#onQueryMedia(android.os.Bundle)`
- `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProvider#onQueryDeletedMedia(android.os.Bundle)`
- `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProvider#onQueryAlbums(android.os.Bundle)`

### query

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun query(
    uri: Uri, 
    projection: Array<String!>?, 
    selection: String?, 
    selectionArgs: Array<String!>?, 
    sortOrder: String?
): Cursor
```

Implementation is provided by the parent class. Throws by default, and cannot be overridden.

| Parameters ||
|---|---|
| `uri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#): This value cannot be `null`. |
| `projection` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>?: This value may be `null`. |
| `selection` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: This value may be `null`. |
| --- | --- |
| `selectionArgs` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>?: This value may be `null`. |
| `sortOrder` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: This value may be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/database/Cursor.html#` | This value cannot be `null`. |

### query

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun query(
    uri: Uri, 
    projection: Array<String!>?, 
    selection: String?, 
    selectionArgs: Array<String!>?, 
    sortOrder: String?, 
    cancellationSignal: CancellationSignal?
): Cursor
```

Implementation is provided by the parent class. Throws by default, and cannot be overridden.

| Parameters ||
|---|---|
| `uri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#): This value cannot be `null`. |
| `projection` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>?: This value may be `null`. |
| `selection` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: This value may be `null`. |
| --- | --- |
| `selectionArgs` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>?: This value may be `null`. |
| `sortOrder` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: This value may be `null`. |
| `cancellationSignal` | [CancellationSignal](https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#)?: This value may be `null`. |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/database/Cursor.html#` | This value cannot be `null`. |

### update

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun update(
    uri: Uri, 
    values: ContentValues!, 
    selection: String?, 
    selectionArgs: Array<String!>?
): Int
```

Implementation is provided by the parent class. Throws by default, and cannot be overridden.

| Parameters ||
|---|---|
| `uri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#): This value cannot be `null`. |
| `values` | [ContentValues](https://developer.android.com/reference/kotlin/android/content/ContentValues.html#)!: This value cannot be `null`. |
| `selection` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: This value may be `null`. |
| --- | --- |
| `selectionArgs` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>?: This value may be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the number of rows affected. |
