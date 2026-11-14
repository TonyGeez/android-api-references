Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DocumentsProvider

```
abstract class DocumentsProvider : ContentProvider
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.content.ContentProvider](../android.content/ContentProvider.md) ||
| | ↳ | [android.provider.DocumentsProvider](DocumentsProvider.md) |

Base class for a document provider. A document provider offers read and write access to durable files, such as files stored on a local disk, or files in a cloud storage service. To create a document provider, extend this class, implement the abstract methods, and add it to your manifest like this:

```kotlin
<manifest>
     ...
     <application>
         ...
         <provider
             android:name="com.example.MyCloudProvider"
             android:authorities="com.example.mycloudprovider"
             android:exported="true"
             android:grantUriPermissions="true"
             android:permission="android.permission.MANAGE_DOCUMENTS"
             android:enabled="@bool/isAtLeastKitKat">
             <intent-filter>
                 <action android:name="android.content.action.DOCUMENTS_PROVIDER" />
             </intent-filter>
         </provider>
         ...
     </application>
 </manifest>
```

<br />

When defining your provider, you must protect it with `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MANAGE_DOCUMENTS:kotlin.String`, which is a permission only the system can obtain. Applications cannot use a documents provider directly; they must go through `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_OPEN_DOCUMENT:kotlin.String` or `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_CREATE_DOCUMENT:kotlin.String` which requires a user to actively navigate and select documents. When a user selects documents through that UI, the system issues narrow URI permission grants to the requesting application.

### Documents

A document can be either an openable stream (with a specific MIME type), or a directory containing additional documents (with the `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract.Document#MIME_TYPE_DIR:kotlin.String` MIME type). Each directory represents the top of a subtree containing zero or more documents, which can recursively contain even more documents and directories.

Each document can have different capabilities, as described by `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract.Document#COLUMN_FLAGS:kotlin.String`. For example, if a document can be represented as a thumbnail, your provider can set `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract.Document#FLAG_SUPPORTS_THUMBNAIL:kotlin.Int` and implement `https://developer.android.com/reference/kotlin/android/provider/DocumentsProvider#openDocumentThumbnail(kotlin.String,%20android.graphics.Point,%20android.os.CancellationSignal)` to return that thumbnail.

Each document under a provider is uniquely referenced by its `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract.Document#COLUMN_DOCUMENT_ID:kotlin.String`, which must not change once returned. A single document can be included in multiple directories when responding to `https://developer.android.com/reference/kotlin/android/provider/DocumentsProvider#queryChildDocuments(kotlin.String,%20kotlin.Array,%20kotlin.String)`. For example, a provider might surface a single photo in multiple locations: once in a directory of geographic locations, and again in a directory of dates.

### Roots

All documents are surfaced through one or more "roots." Each root represents the top of a document tree that a user can navigate. For example, a root could represent an account or a physical storage device. Similar to documents, each root can have capabilities expressed through `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract.Root#COLUMN_FLAGS:kotlin.String`.

## Summary

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#TRIM_MEMORY_BACKGROUND:kotlin.Int` Level for `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#onTrimMemory(kotlin.Int)`: the process has gone on to the LRU list. This is a good opportunity to clean up resources that can efficiently and quickly be re-built if the user returns to the app. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#TRIM_MEMORY_COMPLETE:kotlin.Int` Level for `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#onTrimMemory(kotlin.Int)`: the process is nearing the end of the background LRU list, and if more memory isn't found soon it will be killed. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#TRIM_MEMORY_MODERATE:kotlin.Int` Level for `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#onTrimMemory(kotlin.Int)`: the process is around the middle of the background LRU list; freeing memory can help the system keep other processes running later in the list for better overall performance. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#TRIM_MEMORY_RUNNING_CRITICAL:kotlin.Int` Level for `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#onTrimMemory(kotlin.Int)`: the process is not an expendable background process, but the device is running extremely low on memory and is about to not be able to keep any background processes running. Your running process should free up as many non-critical resources as it can to allow that memory to be used elsewhere. The next thing that will happen after this is `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks.html#onLowMemory()` called to report that nothing at all can be kept in the background, a situation that can start to notably impact the user. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#TRIM_MEMORY_RUNNING_LOW:kotlin.Int` Level for `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#onTrimMemory(kotlin.Int)`: the process is not an expendable background process, but the device is running low on memory. Your running process should free up unneeded resources to allow that memory to be used elsewhere. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#TRIM_MEMORY_RUNNING_MODERATE:kotlin.Int` Level for `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#onTrimMemory(kotlin.Int)`: the process is not an expendable background process, but the device is running moderately low on memory. Your running process may want to release some unneeded resources for use elsewhere. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#TRIM_MEMORY_UI_HIDDEN:kotlin.Int` Level for `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#onTrimMemory(kotlin.Int)`: the process had been showing a user interface, and is no longer doing so. Large allocations with the UI should be released at this point to allow memory to be better managed. <br /> | ||

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/provider/DocumentsProvider#DocumentsProvider()()` <br /> |

| Public methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/provider/DocumentsProvider#attachInfo(android.content.Context,%20android.content.pm.ProviderInfo)(context: https://developer.android.com/reference/kotlin/android/content/Context.html#!, info: https://developer.android.com/reference/kotlin/android/content/pm/ProviderInfo.html#!)` Implementation is provided by the parent class. |
| open [Bundle](../android.os/Bundle.md)? | `https://developer.android.com/reference/kotlin/android/provider/DocumentsProvider#call(kotlin.String,%20kotlin.String,%20android.os.Bundle)(method: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, arg: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, extras: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?)` Implementation is provided by the parent class. |
| open [Uri](../android.net/Uri.md)? | `https://developer.android.com/reference/kotlin/android/provider/DocumentsProvider#canonicalize(android.net.Uri)(uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#)` Implementation is provided by the parent class. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/provider/DocumentsProvider#copyDocument(kotlin.String,%20kotlin.String)(sourceDocumentId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, targetParentDocumentId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Copy the requested document or a document tree. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/provider/DocumentsProvider#createDocument(kotlin.String,%20kotlin.String,%20kotlin.String)(parentDocumentId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, mimeType: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, displayName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Create a new document and return its newly generated `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract.Document#COLUMN_DOCUMENT_ID:kotlin.String`. |
| open [IntentSender](../android.content/IntentSender.md)! | `https://developer.android.com/reference/kotlin/android/provider/DocumentsProvider#createWebLinkIntent(kotlin.String,%20android.os.Bundle)(documentId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, options: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?)` Creates an intent sender for a web link, if the document is web linkable. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/provider/DocumentsProvider#delete(android.net.Uri,%20kotlin.String,%20kotlin.Array)(uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#, selection: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, selectionArgs: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>?)` Implementation is provided by the parent class. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/provider/DocumentsProvider#deleteDocument(kotlin.String)(documentId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Delete the requested document. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/provider/DocumentsProvider#ejectRoot(kotlin.String)(rootId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Ejects the root. |
| --- | --- |
| open [DocumentsContract.Path](../android/provider/DocumentsContract.Path.md)! | `https://developer.android.com/reference/kotlin/android/provider/DocumentsProvider#findDocumentPath(kotlin.String,%20kotlin.String)(parentDocumentId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, childDocumentId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Finds the canonical path for the requested document. |
| open [Bundle](../android.os/Bundle.md)? | `https://developer.android.com/reference/kotlin/android/provider/DocumentsProvider#getDocumentMetadata(kotlin.String)(documentId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Returns metadata associated with the document. |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | `https://developer.android.com/reference/kotlin/android/provider/DocumentsProvider#getDocumentStreamTypes(kotlin.String,%20kotlin.String)(documentId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, mimeTypeFilter: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Return a list of streamable MIME types matching the filter, which can be passed to `https://developer.android.com/reference/kotlin/android/provider/DocumentsProvider#openTypedDocument(kotlin.String,%20kotlin.String,%20android.os.Bundle,%20android.os.CancellationSignal)`. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/provider/DocumentsProvider#getDocumentType(kotlin.String)(documentId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Return concrete MIME type of the requested document. |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>? | `https://developer.android.com/reference/kotlin/android/provider/DocumentsProvider#getStreamTypes(android.net.Uri,%20kotlin.String)(uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#, mimeTypeFilter: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Called by a client to determine the types of data streams that this content provider support for the given URI. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | `https://developer.android.com/reference/kotlin/android/provider/DocumentsProvider#getType(android.net.Uri)(uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#)` Implementation is provided by the parent class. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | `https://developer.android.com/reference/kotlin/android/provider/DocumentsProvider#getTypeAnonymous(android.net.Uri)(uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#)` An unrestricted version of getType, which does not reveal sensitive information |
| [Uri](../android.net/Uri.md)? | `https://developer.android.com/reference/kotlin/android/provider/DocumentsProvider#insert(android.net.Uri,%20android.content.ContentValues)(uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#, values: https://developer.android.com/reference/kotlin/android/content/ContentValues.html#?)` Implementation is provided by the parent class. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/provider/DocumentsProvider#isChildDocument(kotlin.String,%20kotlin.String)(parentDocumentId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, documentId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Test if a document is descendant (child, grandchild, etc) from the given parent. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/provider/DocumentsProvider#moveDocument(kotlin.String,%20kotlin.String,%20kotlin.String)(sourceDocumentId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, sourceParentDocumentId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, targetParentDocumentId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Move the requested document or a document tree. |
| [AssetFileDescriptor](../android.content.res/AssetFileDescriptor.md)? | `https://developer.android.com/reference/kotlin/android/provider/DocumentsProvider#openAssetFile(android.net.Uri,%20kotlin.String)(uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#, mode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Implementation is provided by the parent class. |
| [AssetFileDescriptor](../android.content.res/AssetFileDescriptor.md)? | `https://developer.android.com/reference/kotlin/android/provider/DocumentsProvider#openAssetFile(android.net.Uri,%20kotlin.String,%20android.os.CancellationSignal)(uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#, mode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, signal: https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#?)` Implementation is provided by the parent class. |
| --- | --- |
| abstract [ParcelFileDescriptor](../android.os/ParcelFileDescriptor.md)! | `https://developer.android.com/reference/kotlin/android/provider/DocumentsProvider#openDocument(kotlin.String,%20kotlin.String,%20android.os.CancellationSignal)(documentId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, mode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, signal: https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#?)` Open and return the requested document. |
| open [AssetFileDescriptor](../android.content.res/AssetFileDescriptor.md)! | `https://developer.android.com/reference/kotlin/android/provider/DocumentsProvider#openDocumentThumbnail(kotlin.String,%20android.graphics.Point,%20android.os.CancellationSignal)(documentId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, sizeHint: https://developer.android.com/reference/kotlin/android/graphics/Point.html#!, signal: https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#!)` Open and return a thumbnail of the requested document. |
| [ParcelFileDescriptor](../android.os/ParcelFileDescriptor.md)? | `https://developer.android.com/reference/kotlin/android/provider/DocumentsProvider#openFile(android.net.Uri,%20kotlin.String)(uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#, mode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Implementation is provided by the parent class. |
| --- | --- |
| [ParcelFileDescriptor](../android.os/ParcelFileDescriptor.md)? | `https://developer.android.com/reference/kotlin/android/provider/DocumentsProvider#openFile(android.net.Uri,%20kotlin.String,%20android.os.CancellationSignal)(uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#, mode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, signal: https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#?)` Implementation is provided by the parent class. |
| [AssetFileDescriptor](../android.content.res/AssetFileDescriptor.md)? | `https://developer.android.com/reference/kotlin/android/provider/DocumentsProvider#openTypedAssetFile(android.net.Uri,%20kotlin.String,%20android.os.Bundle)(uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#, mimeTypeFilter: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, opts: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?)` Implementation is provided by the parent class. |
| [AssetFileDescriptor](../android.content.res/AssetFileDescriptor.md)? | `https://developer.android.com/reference/kotlin/android/provider/DocumentsProvider#openTypedAssetFile(android.net.Uri,%20kotlin.String,%20android.os.Bundle,%20android.os.CancellationSignal)(uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#, mimeTypeFilter: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, opts: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?, signal: https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#?)` Implementation is provided by the parent class. |
| --- | --- |
| open [AssetFileDescriptor](../android.content.res/AssetFileDescriptor.md)! | `https://developer.android.com/reference/kotlin/android/provider/DocumentsProvider#openTypedDocument(kotlin.String,%20kotlin.String,%20android.os.Bundle,%20android.os.CancellationSignal)(documentId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, mimeTypeFilter: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, opts: https://developer.android.com/reference/kotlin/android/os/Bundle.html#!, signal: https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#!)` Open and return the document in a format matching the specified MIME type filter. |
| [Cursor](../android.database/Cursor.md)? | `https://developer.android.com/reference/kotlin/android/provider/DocumentsProvider#query(android.net.Uri,%20kotlin.Array,%20android.os.Bundle,%20android.os.CancellationSignal)(uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#, projection: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>?, queryArgs: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?, cancellationSignal: https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#?)` Implementation is provided by the parent class. |
| [Cursor](../android.database/Cursor.md)? | `https://developer.android.com/reference/kotlin/android/provider/DocumentsProvider#query(android.net.Uri,%20kotlin.Array,%20kotlin.String,%20kotlin.Array,%20kotlin.String)(uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#, projection: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>?, selection: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, selectionArgs: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>?, sortOrder: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?)` Implement this to handle query requests from clients. |
| --- | --- |
| open [Cursor](../android.database/Cursor.md)? | `https://developer.android.com/reference/kotlin/android/provider/DocumentsProvider#query(android.net.Uri,%20kotlin.Array,%20kotlin.String,%20kotlin.Array,%20kotlin.String,%20android.os.CancellationSignal)(uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#, projection: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>?, selection: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, selectionArgs: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>?, sortOrder: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, cancellationSignal: https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#?)` WARNING: Sub-classes should not override this method. |
| open [Cursor](../android.database/Cursor.md)! | `https://developer.android.com/reference/kotlin/android/provider/DocumentsProvider#queryChildDocuments(kotlin.String,%20kotlin.Array,%20android.os.Bundle)(parentDocumentId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, projection: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>?, queryArgs: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?)` Override this method to return the children documents contained in the requested directory. |
| abstract [Cursor](../android.database/Cursor.md)! | `https://developer.android.com/reference/kotlin/android/provider/DocumentsProvider#queryChildDocuments(kotlin.String,%20kotlin.Array,%20kotlin.String)(parentDocumentId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, projection: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!, sortOrder: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Return the children documents contained in the requested directory. |
| --- | --- |
| abstract [Cursor](../android.database/Cursor.md)! | `https://developer.android.com/reference/kotlin/android/provider/DocumentsProvider#queryDocument(kotlin.String,%20kotlin.Array)(documentId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, projection: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!)` Return metadata for the single requested document. |
| open [Cursor](../android.database/Cursor.md)! | `https://developer.android.com/reference/kotlin/android/provider/DocumentsProvider#queryRecentDocuments(kotlin.String,%20kotlin.Array)(rootId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, projection: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!)` Return recently modified documents under the requested root. |
| open [Cursor](../android.database/Cursor.md)? | `https://developer.android.com/reference/kotlin/android/provider/DocumentsProvider#queryRecentDocuments(kotlin.String,%20kotlin.Array,%20android.os.Bundle,%20android.os.CancellationSignal)(rootId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, projection: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>?, queryArgs: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?, signal: https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#?)` Return recently modified documents under the requested root. |
| --- | --- |
| abstract [Cursor](../android.database/Cursor.md)! | `https://developer.android.com/reference/kotlin/android/provider/DocumentsProvider#queryRoots(kotlin.Array)(projection: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!)` Return all roots currently provided. |
| open [Cursor](../android.database/Cursor.md)! | `https://developer.android.com/reference/kotlin/android/provider/DocumentsProvider#querySearchDocuments(kotlin.String,%20kotlin.String,%20kotlin.Array)(rootId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, query: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, projection: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!)` Return documents that match the given query under the requested root. |
| open [Cursor](../android.database/Cursor.md)? | `https://developer.android.com/reference/kotlin/android/provider/DocumentsProvider#querySearchDocuments(kotlin.String,%20kotlin.String,%20kotlin.Array,%20android.os.CancellationSignal)(parentDocumentId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, query: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, projection: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>?, signal: https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#?)` Return documents that match the given query under the requested directory. |
| --- | --- |
| open [Cursor](../android.database/Cursor.md)? | `https://developer.android.com/reference/kotlin/android/provider/DocumentsProvider#querySearchDocuments(kotlin.String,%20kotlin.Array,%20android.os.Bundle)(rootId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, projection: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>?, queryArgs: https://developer.android.com/reference/kotlin/android/os/Bundle.html#)` Return documents that match the given query under the requested root. |
| open [Cursor](../android.database/Cursor.md)? | `https://developer.android.com/reference/kotlin/android/provider/DocumentsProvider#querySearchDocuments(kotlin.String,%20kotlin.Array,%20android.os.Bundle,%20android.os.CancellationSignal)(parentDocumentId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, projection: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>?, queryArgs: https://developer.android.com/reference/kotlin/android/os/Bundle.html#, signal: https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#?)` Return documents that match the given query under the requested directory. |
| open [Cursor](../android.database/Cursor.md)? | `https://developer.android.com/reference/kotlin/android/provider/DocumentsProvider#queryTrashDocuments(kotlin.String,%20kotlin.Array,%20android.os.Bundle,%20android.os.CancellationSignal)(rootId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, projection: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>?, queryArgs: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?, signal: https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#?)` <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/provider/DocumentsProvider#removeDocument(kotlin.String,%20kotlin.String)(documentId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, parentDocumentId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Removes the requested document or a document tree. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/provider/DocumentsProvider#renameDocument(kotlin.String,%20kotlin.String)(documentId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, displayName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Rename an existing document. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | `https://developer.android.com/reference/kotlin/android/provider/DocumentsProvider#restoreDocumentFromTrash(kotlin.String,%20kotlin.String)(documentId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, targetParentDocumentId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?)` Restore the specified trash document. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/provider/DocumentsProvider#revokeDocumentPermission(kotlin.String)(documentId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Revoke any active permission grants for the given `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract.Document#COLUMN_DOCUMENT_ID:kotlin.String`, usually called when a document becomes invalid. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | `https://developer.android.com/reference/kotlin/android/provider/DocumentsProvider#trashDocument(kotlin.String)(documentId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Trash the requested document. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/provider/DocumentsProvider#update(android.net.Uri,%20android.content.ContentValues,%20kotlin.String,%20kotlin.Array)(uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#, values: https://developer.android.com/reference/kotlin/android/content/ContentValues.html#?, selection: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, selectionArgs: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>?)` Implementation is provided by the parent class. |
| --- | --- |

| Inherited functions ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/android/content/ContentProviderResult.html#!>` | `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#applyBatch(kotlin.String,%20java.util.ArrayList)(authority: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, operations: https://developer.android.com/reference/kotlin/java/util/ArrayList.html#<https://developer.android.com/reference/kotlin/android/content/ContentProviderOperation.html#!>)` Override this to handle requests to perform a batch of operations, or the default implementation will iterate over the operations and call `https://developer.android.com/reference/kotlin/android/content/ContentProviderOperation.html#apply(android.content.ContentProvider,%20kotlin.Array,%20kotlin.Int)` on each of them. If all calls to `https://developer.android.com/reference/kotlin/android/content/ContentProviderOperation.html#apply(android.content.ContentProvider,%20kotlin.Array,%20kotlin.Int)` succeed then a `https://developer.android.com/reference/kotlin/android/content/ContentProviderResult.html#` array with as many elements as there were operations will be returned. If any of the calls fail, it is up to the implementation how many of the others take effect. This method can be called from multiple threads, as described in [Processes and Threads](https://developer.android.com/guide/topics/fundamentals/processes-and-threads.html#Threads). <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/android/content/ContentProviderResult.html#!>` | `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#applyBatch(java.util.ArrayList)(operations: https://developer.android.com/reference/kotlin/java/util/ArrayList.html#<https://developer.android.com/reference/kotlin/android/content/ContentProviderOperation.html#!>)` <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#bulkInsert(android.net.Uri,%20kotlin.Array)(uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#, values: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/android/content/ContentValues.html#!>)` Override this to handle requests to insert a set of new rows, or the default implementation will iterate over the values and call #insert on each of them. As a courtesy, call `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#notifyChange(android.net.Uri,%20android.database.ContentObserver)` after inserting. This method can be called from multiple threads, as described in [Processes and Threads](https://developer.android.com/guide/topics/fundamentals/processes-and-threads.html#Threads). <br /> | | `https://developer.android.com/reference/kotlin/android/os/Bundle.html#?` | `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#call(kotlin.String,%20kotlin.String,%20kotlin.String,%20android.os.Bundle)(authority: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, method: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, arg: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, extras: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?)` Call a provider-defined method. This can be used to implement interfaces that are cheaper and/or unnatural for a table-like model. **WARNING:** The framework does no permission checking on this entry into the content provider besides the basic ability for the application to get access to the provider at all. For example, it has no idea whether the call being executed may read or write data in the provider, so can't enforce those individual permissions. Any implementation of this method **must** do its own permission checks on incoming calls to make sure they are allowed. <br /> | | `https://developer.android.com/reference/kotlin/android/content/ContentProvider.CallingIdentity.html#` | `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#clearCallingIdentity()()` Reset the identity of the incoming IPC on the current thread. Internally this calls `https://developer.android.com/reference/kotlin/android/os/Binder.html#clearCallingIdentity()` and also clears any value stored in `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#getCallingPackage()`. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#delete(android.net.Uri,%20android.os.Bundle)(uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#, extras: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?)` Implement this to handle requests to delete one or more rows. The implementation should apply the selection clause when performing deletion, allowing the operation to affect multiple rows in a directory. As a courtesy, call `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#notifyChange(android.net.Uri,%20android.database.ContentObserver)` after deleting. This method can be called from multiple threads, as described in [Processes and Threads](https://developer.android.com/guide/topics/fundamentals/processes-and-threads.html#Threads). The implementation is responsible for parsing out a row ID at the end of the URI, if a specific row is being deleted. That is, the client would pass in `content://contacts/people/22` and the implementation is responsible for parsing the record number (22) when creating a SQL statement. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#dump(java.io.FileDescriptor,%20java.io.PrintWriter,%20kotlin.Array)(fd: https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#!, writer: https://developer.android.com/reference/kotlin/java/io/PrintWriter.html#!, args: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!)` Print the Provider's state into the given stream. This gets invoked if you run "adb shell dumpsys activity provider \<provider_component_name\>". <br /> | | `https://developer.android.com/reference/kotlin/android/content/AttributionSource.html#?` | `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#getCallingAttributionSource()()` Gets the attribution source of the calling app. If you want to attribute the data access to the calling app you can create an attribution context via `https://developer.android.com/reference/kotlin/android/content/Context.html#createContext(android.content.ContextParams)` and passing this identity to `https://developer.android.com/reference/kotlin/android/content/ContextParams.Builder.html#setNextAttributionSource(android.content.AttributionSource)`. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?` | `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#getCallingAttributionTag()()` Return the attribution tag of the caller that initiated the request being processed on the current thread. Returns `null` if not currently processing a request of the request is for the default attribution. This will always return `null` when processing `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#getTypeAnonymous(android.net.Uri)` requests For `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#getType(android.net.Uri)` requests, this will be only available for cases, where the caller can be identified. See `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#getTypeAnonymous(android.net.Uri)` <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?` | `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#getCallingPackage()()` Return the package name of the caller that initiated the request being processed on the current thread. The returned package will have been verified to belong to the calling UID. Returns `null` if not currently processing a request. This will always return `null` when processing `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#getTypeAnonymous(android.net.Uri)` requests For `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#getType(android.net.Uri)` requests, this will be only available for cases, where the caller can be identified. See `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#getTypeAnonymous(android.net.Uri)` <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?` | `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#getCallingPackageUnchecked()()` Return the package name of the caller that initiated the request being processed on the current thread. The returned package will have *not* been verified to belong to the calling UID. Returns `null` if not currently processing a request. This will always return `null` when processing `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#getTypeAnonymous(android.net.Uri)` requests For `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#getType(android.net.Uri)` requests, this will be only available for cases, where the caller can be identified. See `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#getTypeAnonymous(android.net.Uri)` <br /> | | `https://developer.android.com/reference/kotlin/android/content/Context.html#?` | `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#getContext()()` Retrieves the Context this provider is running in. Only available once `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#onCreate()` has been called -- this will return `null` in the constructor. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/android/content/pm/PathPermission.html#!>?` | `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#getPathPermissions()()` Return the path-based permissions required for read and/or write access to this content provider. This method can be called from multiple threads, as described in [Processes and Threads](https://developer.android.com/guide/topics/fundamentals/processes-and-threads.html#Threads). <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?` | `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#getReadPermission()()` Return the name of the permission required for read-only access to this content provider. This method can be called from multiple threads, as described in [Processes and Threads](https://developer.android.com/guide/topics/fundamentals/processes-and-threads.html#Threads). <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?` | `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#getWritePermission()()` Return the name of the permission required for read/write access to this content provider. This method can be called from multiple threads, as described in [Processes and Threads](https://developer.android.com/guide/topics/fundamentals/processes-and-threads.html#Threads). <br /> | | `https://developer.android.com/reference/kotlin/android/net/Uri.html#?` | `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#insert(android.net.Uri,%20android.content.ContentValues,%20android.os.Bundle)(uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#, values: https://developer.android.com/reference/kotlin/android/content/ContentValues.html#?, extras: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?)` Implement this to handle requests to insert a new row. As a courtesy, call `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#notifyChange(android.net.Uri,%20android.database.ContentObserver)` after inserting. This method can be called from multiple threads, as described in [Processes and Threads](https://developer.android.com/guide/topics/fundamentals/processes-and-threads.html#Threads). <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#isTemporary()()` Returns true if this instance is a temporary content provider. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#onCallingPackageChanged()()` Called whenever the value of `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#getCallingPackage()` changes, giving the provider an opportunity to invalidate any security related caching it may be performing. This typically happens when a `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#` makes a nested call back into itself when already processing a call from a remote process. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#onConfigurationChanged(android.content.res.Configuration)(newConfig: https://developer.android.com/reference/kotlin/android/content/res/Configuration.html#)` Called by the system when the device configuration changes while your component is running. Note that, unlike activities, other components are never restarted when a configuration changes: they must always deal with the results of the change, such as by re-retrieving resources. At the time that this function has been called, your Resources object will have been updated to return resource values matching the new configuration. For more information, read [Handling Runtime Changes](https://developer.android.com/guide/topics/resources/runtime-changes.html). This method is always called on the application main thread, and must not perform lengthy operations. The default content provider implementation does nothing. Override this method to take appropriate action. (Content providers do not usually care about things like screen orientation, but may want to know about locale changes.) <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#onCreate()()` Implement this to initialize your content provider on startup. This method is called for all registered content providers on the application main thread at application launch time. It must not perform lengthy operations, or application startup will be delayed. You should defer nontrivial initialization (such as opening, upgrading, and scanning databases) until the content provider is used (via #query, #insert, etc). Deferred initialization keeps application startup fast, avoids unnecessary work if the provider turns out not to be needed, and stops database errors (such as a full disk) from halting application launch. If you use SQLite, `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteOpenHelper.html#` is a helpful utility class that makes it easy to manage databases, and will automatically defer opening until first use. If you do use SQLiteOpenHelper, make sure to avoid calling `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteOpenHelper.html#getReadableDatabase()` or `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteOpenHelper.html#getWritableDatabase()` from this method. (Instead, override `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteOpenHelper.html#onOpen(android.database.sqlite.SQLiteDatabase)` to initialize the database when it is first opened.) <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#onLowMemory()()` This is called when the overall system is running low on memory, and actively running processes should trim their memory usage. While the exact point at which this will be called is not defined, generally it will happen when all background process have been killed. That is, before reaching the point of killing processes hosting service and foreground UI that we would like to avoid killing. This method is always called on the application main thread, and must not perform lengthy operations. The default content provider implementation does nothing. Subclasses may override this method to take appropriate action. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#onTrimMemory(kotlin.Int)(level: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Called when the operating system has determined that it is a good time for a process to trim unneeded memory from its process. You should never compare to exact values of the level, since new intermediate values may be added -- you will typically want to compare if the value is greater or equal to a level you are interested in. To retrieve the processes current trim level at any point, you can use `https://developer.android.com/reference/kotlin/android/app/ActivityManager.html#getMyMemoryState(android.app.ActivityManager.RunningAppProcessInfo)`. <br /> | | `https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#` | `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#openFileHelper(android.net.Uri,%20kotlin.String)(uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#, mode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Convenience for subclasses that wish to implement #openFile by looking up a column named "_data" at the given URI. <br /> | | `https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#` | `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#openPipeHelper(android.net.Uri,%20kotlin.String,%20android.os.Bundle,%20android.content.ContentProvider.openPipeHelper.T,%20android.content.ContentProvider.PipeDataWriter)(uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#, mimeType: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, opts: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?, args: T?, func: https://developer.android.com/reference/kotlin/android/content/ContentProvider.PipeDataWriter.html#<T>)` A helper function for implementing #openTypedAssetFile, for creating a data pipe and background thread allowing you to stream generated data back to the client. This function returns a new ParcelFileDescriptor that should be returned to the caller (the caller is responsible for closing it). <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#refresh(android.net.Uri,%20android.os.Bundle,%20android.os.CancellationSignal)(uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#!, extras: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?, cancellationSignal: https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#?)` Implement this to support refresh of content identified by `uri`. By default, this method returns false; providers who wish to implement this should return true to signal the client that the provider has tried refreshing with its own implementation. This allows clients to request an explicit refresh of content identified by `uri`. Client code should only invoke this method when there is a strong indication (such as a user initiated pull to refresh gesture) that the content is stale. Remember to send `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#notifyChange(android.net.Uri,%20android.database.ContentObserver)` notifications when content changes. <br /> | | `https://developer.android.com/reference/kotlin/android/content/Context.html#` | `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#requireContext()()` Retrieves a Non-Nullable Context this provider is running in, this is intended to be called after `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#onCreate()`. When called before context was created, an IllegalStateException will be thrown. Note A provider must be declared in the manifest and created automatically by the system, and context is only available after `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#onCreate()` is called. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#restoreCallingIdentity(android.content.ContentProvider.CallingIdentity)(identity: https://developer.android.com/reference/kotlin/android/content/ContentProvider.CallingIdentity.html#)` Restore the identity of the incoming IPC on the current thread back to a previously identity that was returned by `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#clearCallingIdentity()`. Internally this calls `https://developer.android.com/reference/kotlin/android/os/Binder.html#restoreCallingIdentity(kotlin.Long)` and also restores any value stored in `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#getCallingPackage()`. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#setPathPermissions(kotlin.Array)(permissions: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/android/content/pm/PathPermission.html#!>?)` Change the path-based permission required to read and/or write data in the content provider. This is normally set for you from its manifest information when the provider is first created. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#setReadPermission(kotlin.String)(permission: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?)` Change the permission required to read data from the content provider. This is normally set for you from its manifest information when the provider is first created. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#setWritePermission(kotlin.String)(permission: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?)` Change the permission required to read and write data in the content provider. This is normally set for you from its manifest information when the provider is first created. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#shutdown()()` Implement this to shut down the ContentProvider instance. You can then invoke this method in unit tests. Android normally handles ContentProvider startup and shutdown automatically. You do not need to start up or shut down a ContentProvider. When you invoke a test method on a ContentProvider, however, a ContentProvider instance is started and keeps running after the test finishes, even if a succeeding test instantiates another ContentProvider. A conflict develops because the two instances are usually running against the same underlying data source (for example, an sqlite database). Implementing shutDown() avoids this conflict by providing a way to terminate the ContentProvider. This method can also prevent memory leaks from multiple instantiations of the ContentProvider, and it can ensure unit test isolation by allowing you to completely clean up the test fixture before moving on to the next test. <br /> | | `https://developer.android.com/reference/kotlin/android/net/Uri.html#?` | `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#uncanonicalize(android.net.Uri)(url: https://developer.android.com/reference/kotlin/android/net/Uri.html#)` Remove canonicalization from canonical URIs previously returned by `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#canonicalize(android.net.Uri)`. For example, if your implementation is to add a query param to canonicalize a URI, this method can simply trip any query params on the URI. The default implementation always returns the same url that was passed in. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#update(android.net.Uri,%20android.content.ContentValues,%20android.os.Bundle)(uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#, values: https://developer.android.com/reference/kotlin/android/content/ContentValues.html#?, extras: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?)` Implement this to handle requests to update one or more rows. The implementation should update all rows matching the selection to set the columns according to the provided values map. As a courtesy, call `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#notifyChange(android.net.Uri,%20android.database.ContentObserver)` after updating. This method can be called from multiple threads, as described in [Processes and Threads](https://developer.android.com/guide/topics/fundamentals/processes-and-threads.html#Threads). <br /> | ||
| From class `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks.html#onConfigurationChanged(android.content.res.Configuration)(newConfig: https://developer.android.com/reference/kotlin/android/content/res/Configuration.html#)` Called by the system when the device configuration changes while your component is running. Note that, unlike activities, other components are never restarted when a configuration changes: they must always deal with the results of the change, such as by re-retrieving resources. At the time that this function has been called, your Resources object will have been updated to return resource values matching the new configuration. For more information, read [Handling Runtime Changes](https://developer.android.com/guide/topics/resources/runtime-changes.html). <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks.html#onLowMemory()()` This is called when the overall system is running low on memory, and actively running processes should trim their memory usage. While the exact point at which this will be called is not defined, generally it will happen when all background process have been killed. That is, before reaching the point of killing processes hosting service and foreground UI that we would like to avoid killing. <br /> | ||

## Public constructors

### DocumentsProvider

```
DocumentsProvider()
```

## Public methods

### attachInfo

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun attachInfo(
    context: Context!, 
    info: ProviderInfo!
): Unit
```

Implementation is provided by the parent class.

| Parameters ||
|---|---|
| `context` | [Context](../android.content/Context.md)!: The context this provider is running in |
| `info` | [ProviderInfo](../android.content.pm/ProviderInfo.md)!: Registered information about this content provider |

### call

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun call(
    method: String, 
    arg: String?, 
    extras: Bundle?
): Bundle?
```

Implementation is provided by the parent class. Can be overridden to provide additional functionality, but subclasses *must* always call the superclass. If the superclass returns `null`, the subclass may implement custom behavior. 
If you override this method you *must* call through to the superclass implementation.

| Parameters ||
|---|---|
| `method` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |
| `arg` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: This value may be `null`. |
| `extras` | [Bundle](../android.os/Bundle.md)?: This value may be `null`. |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/os/Bundle.html#?` | This value may be `null`. |

### canonicalize

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun canonicalize(uri: Uri): Uri?
```

Implementation is provided by the parent class. Can be overridden to provide additional functionality, but subclasses *must* always call the superclass. If the superclass returns `null`, the subclass may implement custom behavior.

This is typically used to resolve a subtree URI into a concrete document reference, issuing a narrower single-document URI permission grant along the way. 
If you override this method you *must* call through to the superclass implementation.

| Parameters ||
|---|---|
| `url` | The Uri to canonicalize. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/net/Uri.html#?` | Return the canonical representation of url, or null if canonicalization of that Uri is not supported. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract#buildDocumentUriUsingTree(android.net.Uri,%20kotlin.String)`

### copyDocument

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun copyDocument(
    sourceDocumentId: String!, 
    targetParentDocumentId: String!
): String!
```

Copy the requested document or a document tree.

Copies a document including all child documents to another location within the same document provider. Upon completion returns the document id of the copied document at the target destination. `null` must never be returned.

| Parameters ||
|---|---|
| `sourceDocumentId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the document to copy. |
| `targetParentDocumentId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the target document to be copied into as a child. |

| Exceptions ||
|---|---|
| `android.app.AuthenticationRequiredException` | If authentication is required from the user (such as login credentials), but it is not guaranteed that the client will handle this properly. |

### createDocument

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun createDocument(
    parentDocumentId: String!, 
    mimeType: String!, 
    displayName: String!
): String!
```

Create a new document and return its newly generated `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract.Document#COLUMN_DOCUMENT_ID:kotlin.String`. You must allocate a new `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract.Document#COLUMN_DOCUMENT_ID:kotlin.String` to represent the document, which must not change once returned.

| Parameters ||
|---|---|
| `parentDocumentId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the parent directory to create the new document under. |
| `mimeType` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the concrete MIME type associated with the new document. If the MIME type is not supported, the provider must throw. |
| `displayName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the display name of the new document. The provider may alter this name to meet any internal constraints, such as avoiding conflicting names. |
| --- | --- |

| Exceptions ||
|---|---|
| `android.app.AuthenticationRequiredException` | If authentication is required from the user (such as login credentials), but it is not guaranteed that the client will handle this properly. |

### createWebLinkIntent

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun createWebLinkIntent(
    documentId: String!, 
    options: Bundle?
): IntentSender!
```

Creates an intent sender for a web link, if the document is web linkable.

`https://developer.android.com/reference/kotlin/android/app/AuthenticationRequiredException.html#` can be thrown if user does not have sufficient permission for the linked document. Before any new permissions are granted for the linked document, a visible UI must be shown, so the user can explicitly confirm whether the permission grants are expected. The user must be able to cancel the operation.

Options passed as an argument may include a list of recipients, such as email addresses. The provider should reflect these options if possible, but it's acceptable to ignore them. In either case, confirmation UI must be shown before any new permission grants are granted.

It is all right to generate a web link without granting new permissions, if opening the link would result in a page for requesting permission access. If it's impossible then the operation must fail by throwing an exception.

| Parameters ||
|---|---|
| `documentId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the document to create a web link intent for. |
| `options` | [Bundle](../android.os/Bundle.md)?: additional information, such as list of recipients. Optional. This value may be `null`. |

| Exceptions ||
|---|---|
| `android.app.AuthenticationRequiredException` | If authentication is required from the user (such as login credentials), but it is not guaranteed that the client will handle this properly. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract.Document#FLAG_WEB_LINKABLE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#getIntentSender()`

### delete

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

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
| `uri` | [Uri](../android.net/Uri.md): The full URI to query, including a row ID (if a specific record is requested). This value cannot be `null`. |
| `selection` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: An optional restriction to apply to rows when deleting. This value may be `null`. |
| `selectionArgs` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>?: This value may be `null`. |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The number of rows affected. |

| Exceptions ||
|---|---|
| `android.database.SQLException` | |

**See Also**

- `https://developer.android.com/reference/kotlin/android/provider/DocumentsProvider#deleteDocument(kotlin.String)`

### deleteDocument

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun deleteDocument(documentId: String!): Unit
```

Delete the requested document.

Upon returning, any URI permission grants for the given document will be revoked. If additional documents were deleted as a side effect of this call (such as documents inside a directory) the implementor is responsible for revoking those permissions using `https://developer.android.com/reference/kotlin/android/provider/DocumentsProvider#revokeDocumentPermission(kotlin.String)`.

| Parameters ||
|---|---|
| `documentId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the document to delete. |

| Exceptions ||
|---|---|
| `android.app.AuthenticationRequiredException` | If authentication is required from the user (such as login credentials), but it is not guaranteed that the client will handle this properly. |

### ejectRoot

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun ejectRoot(rootId: String!): Unit
```

Ejects the root. Throws `https://developer.android.com/reference/kotlin/java/lang/IllegalStateException.html#` if ejection failed.

| Parameters ||
|---|---|
| `rootId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the root to be ejected. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract.Root#FLAG_SUPPORTS_EJECT:kotlin.Int`

### findDocumentPath

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun findDocumentPath(
    parentDocumentId: String?, 
    childDocumentId: String!
): DocumentsContract.Path!
```

Finds the canonical path for the requested document. The path must start from the parent document if parentDocumentId is not null or the root document if parentDocumentId is null. If there are more than one path to this document, return the most typical one. Include both the parent document or root document and the requested document in the returned path.

This API assumes that document ID has enough info to infer the root. Different roots should use different document ID to refer to the same document.

| Parameters ||
|---|---|
| `parentDocumentId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: the document from which the path starts if not null, or null to indicate a path from the root is requested. |
| `childDocumentId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the document which path is requested. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract.Path!` | the path of the requested document. If parentDocumentId is null returned root ID must not be null. If parentDocumentId is not null returned root ID must be null. |

| Exceptions ||
|---|---|
| `android.app.AuthenticationRequiredException` | If authentication is required from the user (such as login credentials), but it is not guaranteed that the client will handle this properly. |

### getDocumentMetadata

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getDocumentMetadata(documentId: String): Bundle?
```

Returns metadata associated with the document. The type of metadata returned is specific to the document type. For example the data returned for an image file will likely consist primarily or solely of EXIF metadata.

The returned `https://developer.android.com/reference/kotlin/android/os/Bundle.html#` will contain zero or more entries depending on the type of data supported by the document provider.

1. A `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract#METADATA_TYPES:kotlin.String` containing a `String[]` value. The string array identifies the type or types of metadata returned. Each value in the can be used to access a `https://developer.android.com/reference/kotlin/android/os/Bundle.html#` of data containing that type of data.
2. An entry each for each type of returned metadata. Each set of metadata is itself represented as a bundle and accessible via a string key naming the type of data.

| Parameters ||
|---|---|
| `documentId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): get the metadata of the document. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/os/Bundle.html#?` | a Bundle of Bundles. This value may be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract#getDocumentMetadata(android.content.ContentResolver,%20android.net.Uri)`

### getDocumentStreamTypes

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getDocumentStreamTypes(
    documentId: String!, 
    mimeTypeFilter: String!
): Array<String!>!
```

Return a list of streamable MIME types matching the filter, which can be passed to `https://developer.android.com/reference/kotlin/android/provider/DocumentsProvider#openTypedDocument(kotlin.String,%20kotlin.String,%20android.os.Bundle,%20android.os.CancellationSignal)`.

The default implementation returns a MIME type provided by `https://developer.android.com/reference/kotlin/android/provider/DocumentsProvider#queryDocument(kotlin.String,%20kotlin.Array)` as long as it matches the filter and the document does not have the `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract.Document#FLAG_VIRTUAL_DOCUMENT:kotlin.Int` flag set.

Virtual documents must have at least one streamable format.
**See Also**

- `https://developer.android.com/reference/kotlin/android/provider/DocumentsProvider#getStreamTypes(android.net.Uri,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/provider/DocumentsProvider#openTypedDocument(kotlin.String,%20kotlin.String,%20android.os.Bundle,%20android.os.CancellationSignal)`

### getDocumentType

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getDocumentType(documentId: String!): String!
```

Return concrete MIME type of the requested document. Must match the value of `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract.Document#COLUMN_MIME_TYPE:kotlin.String` for this document. The default implementation queries `https://developer.android.com/reference/kotlin/android/provider/DocumentsProvider#queryDocument(kotlin.String,%20kotlin.Array)`, so providers may choose to override this as an optimization.

<br />

| Exceptions ||
|---|---|
| `android.app.AuthenticationRequiredException` | If authentication is required from the user (such as login credentials), but it is not guaranteed that the client will handle this properly. |

### getStreamTypes

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getStreamTypes(
    uri: Uri, 
    mimeTypeFilter: String
): Array<String!>?
```

Called by a client to determine the types of data streams that this content provider support for the given URI.

Overriding this method is deprecated. Override `https://developer.android.com/reference/kotlin/android/provider/DocumentsProvider#openTypedDocument(kotlin.String,%20kotlin.String,%20android.os.Bundle,%20android.os.CancellationSignal)` instead.

| Parameters ||
|---|---|
| `uri` | [Uri](../android.net/Uri.md): The data in the content provider being queried. This value cannot be `null`. |
| `mimeTypeFilter` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The type of data the client desires. May be a pattern, such as \*/\* to retrieve all possible data types. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>?` | Returns `null` if there are no possible data streams for the given mimeTypeFilter. Otherwise returns an array of all available concrete MIME types. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/provider/DocumentsProvider#getDocumentStreamTypes(kotlin.String,%20kotlin.String)`

### getType

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getType(uri: Uri): String?
```

Implementation is provided by the parent class. Cannot be overridden.

| Parameters ||
|---|---|
| `uri` | [Uri](../android.net/Uri.md): the URI to query. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?` | a MIME type string, or `null` if there is no type. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/provider/DocumentsProvider#getDocumentType(kotlin.String)`

### getTypeAnonymous

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getTypeAnonymous(uri: Uri): String?
```

An unrestricted version of getType, which does not reveal sensitive information

| Parameters ||
|---|---|
| `uri` | [Uri](../android.net/Uri.md): This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?` | This value may be `null`. |

### insert

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun insert(
    uri: Uri, 
    values: ContentValues?
): Uri?
```

Implementation is provided by the parent class. Throws by default, and cannot be overridden.

| Parameters ||
|---|---|
| `uri` | [Uri](../android.net/Uri.md): The content:// URI of the insertion request. This value cannot be `null`. |
| `values` | [ContentValues](../android.content/ContentValues.md)?: A set of column_name/value pairs to add to the database. This value may be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/net/Uri.html#?` | The URI for the newly inserted item. This value may be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/provider/DocumentsProvider#createDocument(kotlin.String,%20kotlin.String,%20kotlin.String)`

### isChildDocument

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isChildDocument(
    parentDocumentId: String!, 
    documentId: String!
): Boolean
```

Test if a document is descendant (child, grandchild, etc) from the given parent. For example, providers must implement this to support `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_OPEN_DOCUMENT_TREE:kotlin.String`. You should avoid making network requests to keep this request fast.

| Parameters ||
|---|---|
| `parentDocumentId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: parent to verify against. |
| `documentId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: child to verify. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | if given document is a descendant of the given parent. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract.Root#FLAG_SUPPORTS_IS_CHILD:kotlin.Int`

### moveDocument

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun moveDocument(
    sourceDocumentId: String!, 
    sourceParentDocumentId: String!, 
    targetParentDocumentId: String!
): String!
```

Move the requested document or a document tree.

Moves a document including all child documents to another location within the same document provider. Upon completion returns the document id of the copied document at the target destination. `null` must never be returned.

It's the responsibility of the provider to revoke grants if the document is no longer accessible using `sourceDocumentId`.

| Parameters ||
|---|---|
| `sourceDocumentId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the document to move. |
| `sourceParentDocumentId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the parent of the document to move. |
| `targetParentDocumentId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the target document to be a new parent of the source document. |
| --- | --- |

| Exceptions ||
|---|---|
| `android.app.AuthenticationRequiredException` | If authentication is required from the user (such as login credentials), but it is not guaranteed that the client will handle this properly. |

### openAssetFile

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun openAssetFile(
    uri: Uri, 
    mode: String
): AssetFileDescriptor?
```

Implementation is provided by the parent class. Cannot be overridden.

| Parameters ||
|---|---|
| `uri` | [Uri](../android.net/Uri.md): The URI whose file is to be opened. This value cannot be `null`. |
| `mode` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The string representation of the file mode. Can be "r", "w", "wt", "wa", "rw" or "rwt". Please note the exact implementation of these may differ for each Provider implementation - for example, "w" may or may not truncate. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/res/AssetFileDescriptor.html#?` | Returns a new AssetFileDescriptor which you can use to access the file. This value may be `null`. |

| Exceptions ||
|---|---|
| `java.io.FileNotFoundException` | Throws FileNotFoundException if there is no file associated with the given URI or the mode is invalid. |
| `java.lang.SecurityException` | Throws SecurityException if the caller does not have permission to access the file. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/provider/DocumentsProvider#openDocument(kotlin.String,%20kotlin.String,%20android.os.CancellationSignal)`

### openAssetFile

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun openAssetFile(
    uri: Uri, 
    mode: String, 
    signal: CancellationSignal?
): AssetFileDescriptor?
```

Implementation is provided by the parent class. Cannot be overridden.

| Parameters ||
|---|---|
| `uri` | [Uri](../android.net/Uri.md): The URI whose file is to be opened. This value cannot be `null`. |
| `mode` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The string representation of the file mode. Can be "r", "w", "wt", "wa", "rw" or "rwt". Please note the exact implementation of these may differ for each Provider implementation - for example, "w" may or may not truncate. This value cannot be `null`. |
| `signal` | [CancellationSignal](../android.os/CancellationSignal.md)?: A signal to cancel the operation in progress, or `null` if none. For example, if you are downloading a file from the network to service a "rw" mode request, you should periodically call `https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#throwIfCanceled()` to check whether the client has canceled the request and abort the download. |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/res/AssetFileDescriptor.html#?` | Returns a new AssetFileDescriptor which you can use to access the file. This value may be `null`. |

| Exceptions ||
|---|---|
| `java.io.FileNotFoundException` | Throws FileNotFoundException if there is no file associated with the given URI or the mode is invalid. |
| `java.lang.SecurityException` | Throws SecurityException if the caller does not have permission to access the file. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/provider/DocumentsProvider#openDocument(kotlin.String,%20kotlin.String,%20android.os.CancellationSignal)`

### openDocument

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun openDocument(
    documentId: String!, 
    mode: String!, 
    signal: CancellationSignal?
): ParcelFileDescriptor!
```

Open and return the requested document.

Your provider should return a reliable `https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#` to detect when the remote caller has finished reading or writing the document.

Mode "r" should always be supported. Provider should throw `https://developer.android.com/reference/kotlin/java/lang/UnsupportedOperationException.html#` if the passing mode is not supported. You may return a pipe or socket pair if the mode is exclusively "r" or "w", but complex modes like "rw" imply a normal file on disk that supports seeking.

If you block while downloading content, you should periodically check `https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#isCanceled()` to abort abandoned open requests.

| Parameters ||
|---|---|
| `documentId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the document to return. |
| `mode` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the mode to open with, such as 'r', 'w', or 'rw'. |
| `signal` | [CancellationSignal](../android.os/CancellationSignal.md)?: used by the caller to signal if the request should be cancelled. May be null. |
| --- | --- |

| Exceptions ||
|---|---|
| `android.app.AuthenticationRequiredException` | If authentication is required from the user (such as login credentials), but it is not guaranteed that the client will handle this properly. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#createReliablePipe()`
- `https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#createReliableSocketPair()`
- `https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#parseMode(kotlin.String)`

### openDocumentThumbnail

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun openDocumentThumbnail(
    documentId: String!, 
    sizeHint: Point!, 
    signal: CancellationSignal!
): AssetFileDescriptor!
```

Open and return a thumbnail of the requested document.

A provider should return a thumbnail closely matching the hinted size, attempting to serve from a local cache if possible. A provider should never return images more than double the hinted size.

If you perform expensive operations to download or generate a thumbnail, you should periodically check `https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#isCanceled()` to abort abandoned thumbnail requests.

| Parameters ||
|---|---|
| `documentId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the document to return. |
| `sizeHint` | [Point](../android.graphics/Point.md)!: hint of the optimal thumbnail dimensions. |
| `signal` | [CancellationSignal](../android.os/CancellationSignal.md)!: used by the caller to signal if the request should be cancelled. May be null. |
| --- | --- |

| Exceptions ||
|---|---|
| `android.app.AuthenticationRequiredException` | If authentication is required from the user (such as login credentials), but it is not guaranteed that the client will handle this properly. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract.Document#FLAG_SUPPORTS_THUMBNAIL:kotlin.Int`

### openFile

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun openFile(
    uri: Uri, 
    mode: String
): ParcelFileDescriptor?
```

Implementation is provided by the parent class. Cannot be overridden.

| Parameters ||
|---|---|
| `uri` | [Uri](../android.net/Uri.md): The URI whose file is to be opened. This value cannot be `null`. |
| `mode` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The string representation of the file mode. Can be "r", "w", "wt", "wa", "rw" or "rwt". Please note the exact implementation of these may differ for each Provider implementation - for example, "w" may or may not truncate. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#?` | Returns a new ParcelFileDescriptor which you can use to access the file. This value may be `null`. |

| Exceptions ||
|---|---|
| `java.io.FileNotFoundException` | Throws FileNotFoundException if there is no file associated with the given URI or the mode is invalid. |
| `java.lang.SecurityException` | Throws SecurityException if the caller does not have permission to access the file. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/provider/DocumentsProvider#openDocument(kotlin.String,%20kotlin.String,%20android.os.CancellationSignal)`

### openFile

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun openFile(
    uri: Uri, 
    mode: String, 
    signal: CancellationSignal?
): ParcelFileDescriptor?
```

Implementation is provided by the parent class. Cannot be overridden.

| Parameters ||
|---|---|
| `uri` | [Uri](../android.net/Uri.md): The URI whose file is to be opened. This value cannot be `null`. |
| `mode` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The string representation of the file mode. Can be "r", "w", "wt", "wa", "rw" or "rwt". Please note the exact implementation of these may differ for each Provider implementation - for example, "w" may or may not truncate. This value cannot be `null`. |
| `signal` | [CancellationSignal](../android.os/CancellationSignal.md)?: A signal to cancel the operation in progress, or `null` if none. For example, if you are downloading a file from the network to service a "rw" mode request, you should periodically call `https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#throwIfCanceled()` to check whether the client has canceled the request and abort the download. |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#?` | Returns a new ParcelFileDescriptor which you can use to access the file. This value may be `null`. |

| Exceptions ||
|---|---|
| `java.io.FileNotFoundException` | Throws FileNotFoundException if there is no file associated with the given URI or the mode is invalid. |
| `java.lang.SecurityException` | Throws SecurityException if the caller does not have permission to access the file. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/provider/DocumentsProvider#openDocument(kotlin.String,%20kotlin.String,%20android.os.CancellationSignal)`

### openTypedAssetFile

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun openTypedAssetFile(
    uri: Uri, 
    mimeTypeFilter: String, 
    opts: Bundle?
): AssetFileDescriptor?
```

Implementation is provided by the parent class. Cannot be overridden.

| Parameters ||
|---|---|
| `uri` | [Uri](../android.net/Uri.md): The data in the content provider being queried. This value cannot be `null`. |
| `mimeTypeFilter` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The type of data the client desires. May be a pattern, such as \*/\*, if the caller does not have specific type requirements; in this case the content provider will pick its best type matching the pattern. This value cannot be `null`. |
| `opts` | [Bundle](../android.os/Bundle.md)?: Additional options from the client. The definitions of these are specific to the content provider being called. This value may be `null`. |
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

**See Also**

- `https://developer.android.com/reference/kotlin/android/provider/DocumentsProvider#openDocumentThumbnail(kotlin.String,%20android.graphics.Point,%20android.os.CancellationSignal)`
- `https://developer.android.com/reference/kotlin/android/provider/DocumentsProvider#openTypedDocument(kotlin.String,%20kotlin.String,%20android.os.Bundle,%20android.os.CancellationSignal)`
- `https://developer.android.com/reference/kotlin/android/provider/DocumentsProvider#getDocumentStreamTypes(kotlin.String,%20kotlin.String)`

### openTypedAssetFile

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun openTypedAssetFile(
    uri: Uri, 
    mimeTypeFilter: String, 
    opts: Bundle?, 
    signal: CancellationSignal?
): AssetFileDescriptor?
```

Implementation is provided by the parent class. Cannot be overridden.

| Parameters ||
|---|---|
| `uri` | [Uri](../android.net/Uri.md): The data in the content provider being queried. This value cannot be `null`. |
| `mimeTypeFilter` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The type of data the client desires. May be a pattern, such as \*/\*, if the caller does not have specific type requirements; in this case the content provider will pick its best type matching the pattern. This value cannot be `null`. |
| `opts` | [Bundle](../android.os/Bundle.md)?: Additional options from the client. The definitions of these are specific to the content provider being called. This value may be `null`. |
| --- | --- |
| `signal` | [CancellationSignal](../android.os/CancellationSignal.md)?: A signal to cancel the operation in progress, or `null` if none. For example, if you are downloading a file from the network to service a "rw" mode request, you should periodically call `https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#throwIfCanceled()` to check whether the client has canceled the request and abort the download. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/res/AssetFileDescriptor.html#?` | Returns a new AssetFileDescriptor from which the client can read data of the desired type. This value may be `null`. |

| Exceptions ||
|---|---|
| `java.io.FileNotFoundException` | Throws FileNotFoundException if there is no file associated with the given URI or the mode is invalid. |
| `java.lang.IllegalArgumentException` | Throws IllegalArgumentException if the content provider does not support the requested MIME type. |
| `java.lang.SecurityException` | Throws SecurityException if the caller does not have permission to access the data. |
| --- | --- |

**See Also**

- `https://developer.android.com/reference/kotlin/android/provider/DocumentsProvider#openDocumentThumbnail(kotlin.String,%20android.graphics.Point,%20android.os.CancellationSignal)`
- `https://developer.android.com/reference/kotlin/android/provider/DocumentsProvider#openTypedDocument(kotlin.String,%20kotlin.String,%20android.os.Bundle,%20android.os.CancellationSignal)`
- `https://developer.android.com/reference/kotlin/android/provider/DocumentsProvider#getDocumentStreamTypes(kotlin.String,%20kotlin.String)`

### openTypedDocument

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun openTypedDocument(
    documentId: String!, 
    mimeTypeFilter: String!, 
    opts: Bundle!, 
    signal: CancellationSignal!
): AssetFileDescriptor!
```

Open and return the document in a format matching the specified MIME type filter.

A provider may perform a conversion if the documents's MIME type is not matching the specified MIME type filter.

Virtual documents must have at least one streamable format.

| Parameters ||
|---|---|
| `documentId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the document to return. |
| `mimeTypeFilter` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the MIME type filter for the requested format. May be \*\\/\*, which matches any MIME type. |
| `opts` | [Bundle](../android.os/Bundle.md)!: extra options from the client. Specific to the content provider. |
| --- | --- |
| `signal` | [CancellationSignal](../android.os/CancellationSignal.md)!: used by the caller to signal if the request should be cancelled. May be null. |

| Exceptions ||
|---|---|
| `android.app.AuthenticationRequiredException` | If authentication is required from the user (such as login credentials), but it is not guaranteed that the client will handle this properly. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/provider/DocumentsProvider#getDocumentStreamTypes(kotlin.String,%20kotlin.String)`

### query

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun query(
    uri: Uri, 
    projection: Array<String!>?, 
    queryArgs: Bundle?, 
    cancellationSignal: CancellationSignal?
): Cursor?
```

Implementation is provided by the parent class. Cannot be overridden.

| Parameters ||
|---|---|
| `uri` | [Uri](../android.net/Uri.md): The URI to query. This will be the full URI sent by the client. This value cannot be `null`. |
| `projection` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>?: The list of columns to put into the cursor. If `null` provide a default set of columns. |
| `queryArgs` | [Bundle](../android.os/Bundle.md)?: A Bundle containing additional information necessary for the operation. Arguments may include SQL style arguments, such as `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#QUERY_ARG_SQL_LIMIT:kotlin.String`, but note that the documentation for each individual provider will indicate which arguments they support. This value may be `null`. |
| --- | --- |
| `cancellationSignal` | [CancellationSignal](../android.os/CancellationSignal.md)?: A signal to cancel the operation in progress, or `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/database/Cursor.html#?` | a Cursor or `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/provider/DocumentsProvider#queryRoots(kotlin.Array)`
- `https://developer.android.com/reference/kotlin/android/provider/DocumentsProvider#queryRecentDocuments(kotlin.String,%20kotlin.Array,%20android.os.Bundle,%20android.os.CancellationSignal)`
- `https://developer.android.com/reference/kotlin/android/provider/DocumentsProvider#queryDocument(kotlin.String,%20kotlin.Array)`
- `https://developer.android.com/reference/kotlin/android/provider/DocumentsProvider#queryChildDocuments(kotlin.String,%20kotlin.Array,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/provider/DocumentsProvider#querySearchDocuments(kotlin.String,%20kotlin.Array,%20android.os.Bundle)`

### query

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun query(
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
| `uri` | [Uri](../android.net/Uri.md): The URI to query. This will be the full URI sent by the client; if the client is requesting a specific record, the URI will end in a record number that the implementation should parse and add to a WHERE or HAVING clause, specifying that _id value. This value cannot be `null`. |
| `projection` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>?: The list of columns to put into the cursor. If `null` all columns are included. |
| `selection` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: A selection criteria to apply when filtering rows. If `null` then all rows are included. |
| --- | --- |
| `selectionArgs` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>?: You may include ?s in selection, which will be replaced by the values from selectionArgs, in order that they appear in the selection. The values will be bound as Strings. This value may be `null`. |
| `sortOrder` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: How the rows in the cursor should be sorted. If `null` then the provider is free to define the sort order. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/database/Cursor.html#?` | a Cursor or `null`. |

### query

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

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

WARNING: Sub-classes should not override this method. This method is non-final solely for the purposes of backwards compatibility.

| Parameters ||
|---|---|
| `uri` | [Uri](../android.net/Uri.md): The URI to query. This will be the full URI sent by the client; if the client is requesting a specific record, the URI will end in a record number that the implementation should parse and add to a WHERE or HAVING clause, specifying that _id value. This value cannot be `null`. |
| `projection` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>?: The list of columns to put into the cursor. If `null` all columns are included. |
| `selection` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: A selection criteria to apply when filtering rows. If `null` then all rows are included. |
| --- | --- |
| `selectionArgs` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>?: You may include ?s in selection, which will be replaced by the values from selectionArgs, in order that they appear in the selection. The values will be bound as Strings. This value may be `null`. |
| `sortOrder` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: How the rows in the cursor should be sorted. If `null` then the provider is free to define the sort order. |
| `cancellationSignal` | [CancellationSignal](../android.os/CancellationSignal.md)?: A signal to cancel the operation in progress, or `null` if none. If the operation is canceled, then `https://developer.android.com/reference/kotlin/android/os/OperationCanceledException.html#` will be thrown when the query is executed. |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/database/Cursor.html#?` | a Cursor or `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/provider/DocumentsProvider#queryChildDocuments(kotlin.String,%20kotlin.Array,%20android.os.Bundle)`
- `https://developer.android.com/reference/kotlin/android/provider/DocumentsProvider#queryDocument(kotlin.String,%20kotlin.Array)`
- `https://developer.android.com/reference/kotlin/android/provider/DocumentsProvider#queryRecentDocuments(kotlin.String,%20kotlin.Array)`
- `https://developer.android.com/reference/kotlin/android/provider/DocumentsProvider#queryRoots(kotlin.Array)`
- `https://developer.android.com/reference/kotlin/android/provider/DocumentsProvider#querySearchDocuments(kotlin.String,%20kotlin.Array,%20android.os.Bundle)`

### queryChildDocuments

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun queryChildDocuments(
    parentDocumentId: String!, 
    projection: Array<String!>?, 
    queryArgs: Bundle?
): Cursor!
```

Override this method to return the children documents contained in the requested directory. This must return immediate descendants only.

If your provider is cloud-based, and you have data cached locally, you may return the local data immediately, setting `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract#EXTRA_LOADING:kotlin.String` on Cursor extras to indicate that you are still fetching additional data. Then, when the network data is available, you can send a change notification to trigger a requery and return the complete contents. To return a Cursor with extras, you need to extend and override `https://developer.android.com/reference/kotlin/android/database/Cursor.html#getExtras()`.

To support change notifications, you must `https://developer.android.com/reference/kotlin/android/database/Cursor.html#setNotificationUri(android.content.ContentResolver,%20android.net.Uri)` with a relevant Uri, such as `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract#buildChildDocumentsUri(kotlin.String,%20kotlin.String)`. Then you can call `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#notifyChange(android.net.Uri,%20android.database.ContentObserver,%20kotlin.Boolean)` with that Uri to send change notifications.

| Parameters ||
|---|---|
| `parentDocumentId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the directory to return children for. |
| `projection` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>?: list of `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract.Document` columns to put into the cursor. If `null` all supported columns should be included. |
| `queryArgs` | [Bundle](../android.os/Bundle.md)?: Bundle containing sorting information or other argument useful to the provider. If no sorting information is available, default sorting will be used, which may be unordered. See `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#QUERY_ARG_SORT_COLUMNS:kotlin.String` for details. This value may be `null`. |
| --- | --- |

| Exceptions ||
|---|---|
| `android.app.AuthenticationRequiredException` | If authentication is required from the user (such as login credentials), but it is not guaranteed that the client will handle this properly. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract#EXTRA_LOADING:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract#EXTRA_INFO:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract#EXTRA_ERROR:kotlin.String`

### queryChildDocuments

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun queryChildDocuments(
    parentDocumentId: String!, 
    projection: Array<String!>!, 
    sortOrder: String!
): Cursor!
```

Return the children documents contained in the requested directory. This must only return immediate descendants, as additional queries will be issued to recursively explore the tree.

Apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#O:kotlin.Int` or higher should override `https://developer.android.com/reference/kotlin/android/provider/DocumentsProvider#queryChildDocuments(kotlin.String,%20kotlin.Array,%20android.os.Bundle)`.

If your provider is cloud-based, and you have some data cached or pinned locally, you may return the local data immediately, setting `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract#EXTRA_LOADING:kotlin.String` on the Cursor to indicate that you are still fetching additional data. Then, when the network data is available, you can send a change notification to trigger a requery and return the complete contents. To return a Cursor with extras, you need to extend and override `https://developer.android.com/reference/kotlin/android/database/Cursor.html#getExtras()`.

To support change notifications, you must `https://developer.android.com/reference/kotlin/android/database/Cursor.html#setNotificationUri(android.content.ContentResolver,%20android.net.Uri)` with a relevant Uri, such as `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract#buildChildDocumentsUri(kotlin.String,%20kotlin.String)`. Then you can call `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#notifyChange(android.net.Uri,%20android.database.ContentObserver,%20kotlin.Boolean)` with that Uri to send change notifications.

| Parameters ||
|---|---|
| `parentDocumentId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the directory to return children for. |
| `projection` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!: list of `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract.Document` columns to put into the cursor. If `null` all supported columns should be included. |
| `sortOrder` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: how to order the rows, formatted as an SQL `ORDER BY` clause (excluding the ORDER BY itself). Passing `null` will use the default sort order, which may be unordered. This ordering is a hint that can be used to prioritize how data is fetched from the network, but UI may always enforce a specific ordering. |
| --- | --- |

| Exceptions ||
|---|---|
| `android.app.AuthenticationRequiredException` | If authentication is required from the user (such as login credentials), but it is not guaranteed that the client will handle this properly. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract#EXTRA_LOADING:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract#EXTRA_INFO:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract#EXTRA_ERROR:kotlin.String`

### queryDocument

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun queryDocument(
    documentId: String!, 
    projection: Array<String!>!
): Cursor!
```

Return metadata for the single requested document. You should avoid making network requests to keep this request fast.

| Parameters ||
|---|---|
| `documentId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the document to return. |
| `projection` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!: list of `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract.Document` columns to put into the cursor. If `null` all supported columns should be included. |

| Exceptions ||
|---|---|
| `android.app.AuthenticationRequiredException` | If authentication is required from the user (such as login credentials), but it is not guaranteed that the client will handle this properly. |

### queryRecentDocuments

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun queryRecentDocuments(
    rootId: String!, 
    projection: Array<String!>!
): Cursor!
```

Return recently modified documents under the requested root. This will only be called for roots that advertise `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract.Root#FLAG_SUPPORTS_RECENTS:kotlin.Int`. The returned documents should be sorted by `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract.Document#COLUMN_LAST_MODIFIED:kotlin.String` in descending order, and limited to only return the 64 most recently modified documents.

Recent documents do not support change notifications.

| Parameters ||
|---|---|
| `projection` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!: list of `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract.Document` columns to put into the cursor. If `null` all supported columns should be included. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract#EXTRA_LOADING:kotlin.String`

### queryRecentDocuments

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun queryRecentDocuments(
    rootId: String, 
    projection: Array<String!>?, 
    queryArgs: Bundle?, 
    signal: CancellationSignal?
): Cursor?
```

Return recently modified documents under the requested root. This will only be called for roots that advertise `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract.Root#FLAG_SUPPORTS_RECENTS:kotlin.Int`. The returned documents should be sorted by `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract.Document#COLUMN_LAST_MODIFIED:kotlin.String` in descending order of the most recently modified documents.

If this method is overriden by the concrete DocumentsProvider and `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#QUERY_ARG_LIMIT:kotlin.String` is specified with a nonnegative int under queryArgs, the result will be limited by that number and `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#QUERY_ARG_LIMIT:kotlin.String` will be specified under `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#EXTRA_HONORED_ARGS:kotlin.String`. Otherwise, a default 64 limit will be used and no QUERY_ARG\* will be specified under `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#EXTRA_HONORED_ARGS:kotlin.String`.

Recent documents do not support change notifications.

| Parameters ||
|---|---|
| `rootId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |
| `projection` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>?: list of `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract.Document` columns to put into the cursor. If `null` all supported columns should be included. |
| `queryArgs` | [Bundle](../android.os/Bundle.md)?: the extra query arguments. This value may be `null`. |
| --- | --- |
| `signal` | [CancellationSignal](../android.os/CancellationSignal.md)?: used by the caller to signal if the request should be cancelled. May be null. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/database/Cursor.html#?` | This value may be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract#EXTRA_LOADING:kotlin.String`

### queryRoots

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun queryRoots(projection: Array<String!>!): Cursor!
```

Return all roots currently provided. To display to users, you must define at least one root. You should avoid making network requests to keep this request fast.

Each root is defined by the metadata columns described in `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract.Root`, including `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract.Root#COLUMN_DOCUMENT_ID:kotlin.String` which points to a directory representing a tree of documents to display under that root.

If this set of roots changes, you must call `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#notifyChange(android.net.Uri,%20android.database.ContentObserver,%20kotlin.Boolean)` with `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract#buildRootsUri(kotlin.String)` to notify the system.

<br />

| Parameters ||
|---|---|
| `projection` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!: list of `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract.Root` columns to put into the cursor. If `null` all supported columns should be included. |

### querySearchDocuments

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun querySearchDocuments(
    rootId: String!, 
    query: String!, 
    projection: Array<String!>!
): Cursor!
```

Return documents that match the given query under the requested root. The returned documents should be sorted by relevance in descending order. How documents are matched against the query string is an implementation detail left to each provider, but it's suggested that at least `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract.Document#COLUMN_DISPLAY_NAME:kotlin.String` be matched in a case-insensitive fashion.

If your provider is cloud-based, and you have some data cached or pinned locally, you may return the local data immediately, setting `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract#EXTRA_LOADING:kotlin.String` on the Cursor to indicate that you are still fetching additional data. Then, when the network data is available, you can send a change notification to trigger a requery and return the complete contents.

To support change notifications, you must `https://developer.android.com/reference/kotlin/android/database/Cursor.html#setNotificationUri(android.content.ContentResolver,%20android.net.Uri)` with a relevant Uri, such as `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract#buildSearchDocumentsUri(kotlin.String,%20kotlin.String,%20kotlin.String)`. Then you can call `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#notifyChange(android.net.Uri,%20android.database.ContentObserver,%20kotlin.Boolean)` with that Uri to send change notifications.

| Parameters ||
|---|---|
| `rootId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the root to search under. |
| `query` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: string to match documents against. |
| `projection` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!: list of `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract.Document` columns to put into the cursor. If `null` all supported columns should be included. |
| --- | --- |

| Exceptions ||
|---|---|
| `android.app.AuthenticationRequiredException` | If authentication is required from the user (such as login credentials), but it is not guaranteed that the client will handle this properly. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract#EXTRA_LOADING:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract#EXTRA_INFO:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract#EXTRA_ERROR:kotlin.String`

### querySearchDocuments

Added in [API level 37.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun querySearchDocuments(
    parentDocumentId: String, 
    query: String, 
    projection: Array<String!>?, 
    signal: CancellationSignal?
): Cursor?
```

Return documents that match the given query under the requested directory. The returned documents should be sorted by relevance in descending order. How documents are matched against the query string is an implementation detail left to each provider, but it's suggested that at least `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract.Document#COLUMN_DISPLAY_NAME:kotlin.String` be matched in a case-insensitive fashion.

If your provider is cloud-based, and you have some data cached or pinned locally, you may return the local data immediately, setting `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract#EXTRA_LOADING:kotlin.String` on the Cursor to indicate that you are still fetching additional data. Then, when the network data is available, you can send a change notification to trigger a requery and return the complete contents.

To support change notifications, you must `https://developer.android.com/reference/kotlin/android/database/Cursor.html#setNotificationUri(android.content.ContentResolver,%20android.net.Uri)` with a relevant Uri, such as `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract#buildSearchDocumentsUri(android.net.Uri,%20kotlin.String)`. Then you can call `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#notifyChange(android.net.Uri,%20android.database.ContentObserver,%20kotlin.Boolean)` with that Uri to send change notifications.

| Parameters ||
|---|---|
| `parentDocumentId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the directory to search under. This value cannot be `null`. |
| `query` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): string to match documents against. This value cannot be `null`. |
| `projection` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>?: list of `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract.Document` columns to put into the cursor. If `null` all supported columns should be included. |
| --- | --- |
| `signal` | [CancellationSignal](../android.os/CancellationSignal.md)?: used by the caller to signal if the request should be cancelled. May be null. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/database/Cursor.html#?` | This value may be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract#buildSearchDocumentsUri(android.net.Uri,%20kotlin.String)`

### querySearchDocuments

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun querySearchDocuments(
    rootId: String, 
    projection: Array<String!>?, 
    queryArgs: Bundle
): Cursor?
```

Return documents that match the given query under the requested root. The returned documents should be sorted by relevance in descending order. How documents are matched against the query string is an implementation detail left to each provider, but it's suggested that at least `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract.Document#COLUMN_DISPLAY_NAME:kotlin.String` be matched in a case-insensitive fashion.

This method is called for root-level searches. It requires the root to advertise `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract.Root#FLAG_SUPPORTS_SEARCH:kotlin.Int`.

If your provider is cloud-based, and you have some data cached or pinned locally, you may return the local data immediately, setting `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract#EXTRA_LOADING:kotlin.String` on the Cursor to indicate that you are still fetching additional data. Then, when the network data is available, you can send a change notification to trigger a requery and return the complete contents.

To support change notifications, you must `https://developer.android.com/reference/kotlin/android/database/Cursor.html#setNotificationUri(android.content.ContentResolver,%20android.net.Uri)` with a relevant Uri, such as `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract#buildSearchDocumentsUri(kotlin.String,%20kotlin.String,%20kotlin.String)`. Then you can call `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#notifyChange(android.net.Uri,%20android.database.ContentObserver,%20kotlin.Boolean)` with that Uri to send change notifications.

| Parameters ||
|---|---|
| `rootId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the root to search under. This value cannot be `null`. |
| `projection` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>?: list of `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract.Document` columns to put into the cursor. If `null` all supported columns should be included. |
| `queryArgs` | [Bundle](../android.os/Bundle.md): the query arguments. `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract#QUERY_ARG_EXCLUDE_MEDIA:kotlin.String`, `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract#QUERY_ARG_DISPLAY_NAME:kotlin.String`, `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract#QUERY_ARG_MIME_TYPES:kotlin.String`, `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract#QUERY_ARG_FILE_SIZE_OVER:kotlin.String`, `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract#QUERY_ARG_LAST_MODIFIED_AFTER:kotlin.String`. This value cannot be `null`. |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/database/Cursor.html#?` | cursor containing search result. Include `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#EXTRA_HONORED_ARGS:kotlin.String` in `https://developer.android.com/reference/kotlin/android/database/Cursor.html#` extras `https://developer.android.com/reference/kotlin/android/os/Bundle.html#` when any QUERY_ARG_\* value was honored during the preparation of the results. This value may be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract.Root#COLUMN_QUERY_ARGS:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#EXTRA_HONORED_ARGS:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract#EXTRA_LOADING:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract#EXTRA_INFO:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract#EXTRA_ERROR:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract.Root#FLAG_SUPPORTS_SEARCH:kotlin.Int`

### querySearchDocuments

Added in [API level 37.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun querySearchDocuments(
    parentDocumentId: String, 
    projection: Array<String!>?, 
    queryArgs: Bundle, 
    signal: CancellationSignal?
): Cursor?
```

Return documents that match the given query under the requested directory. The returned documents should be sorted by relevance in descending order. How documents are matched against the query string is an implementation detail left to each provider, but it's suggested that at least `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract.Document#COLUMN_DISPLAY_NAME:kotlin.String` be matched in a case-insensitive fashion.

This method is called for subtree-level searches. It requires the specific directory to advertise `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract.Document#FLAG_SUPPORTS_SUBTREE_SEARCH:kotlin.Int`.

If your provider is cloud-based, and you have some data cached or pinned locally, you may return the local data immediately, setting `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract#EXTRA_LOADING:kotlin.String` on the Cursor to indicate that you are still fetching additional data. Then, when the network data is available, you can send a change notification to trigger a requery and return the complete contents.

To support change notifications, you must `https://developer.android.com/reference/kotlin/android/database/Cursor.html#setNotificationUri(android.content.ContentResolver,%20android.net.Uri)` with a relevant Uri, such as `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract#buildSearchDocumentsUri(android.net.Uri,%20kotlin.String)`. Then you can call `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#notifyChange(android.net.Uri,%20android.database.ContentObserver,%20kotlin.Boolean)` with that Uri to send change notifications.

| Parameters ||
|---|---|
| `parentDocumentId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the directory to search under. This value cannot be `null`. |
| `projection` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>?: list of `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract.Document` columns to put into the cursor. If `null` all supported columns should be included. |
| `queryArgs` | [Bundle](../android.os/Bundle.md): the query arguments. `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract#QUERY_ARG_EXCLUDE_MEDIA:kotlin.String`, `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract#QUERY_ARG_DISPLAY_NAME:kotlin.String`, `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract#QUERY_ARG_MIME_TYPES:kotlin.String`, `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract#QUERY_ARG_FILE_SIZE_OVER:kotlin.String`, `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract#QUERY_ARG_LAST_MODIFIED_AFTER:kotlin.String`. This value cannot be `null`. |
| --- | --- |
| `signal` | [CancellationSignal](../android.os/CancellationSignal.md)?: used by the caller to signal if the request should be cancelled. May be null. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/database/Cursor.html#?` | cursor containing search result. Include `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#EXTRA_HONORED_ARGS:kotlin.String` in `https://developer.android.com/reference/kotlin/android/database/Cursor.html#` extras `https://developer.android.com/reference/kotlin/android/os/Bundle.html#` when any QUERY_ARG_\* value was honored during the preparation of the results. This value may be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract.Root#COLUMN_QUERY_ARGS:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#EXTRA_HONORED_ARGS:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract#EXTRA_LOADING:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract#EXTRA_INFO:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract#EXTRA_ERROR:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract.Document#FLAG_SUPPORTS_SUBTREE_SEARCH:kotlin.Int`

### queryTrashDocuments

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun queryTrashDocuments(
    rootId: String, 
    projection: Array<String!>?, 
    queryArgs: Bundle?, 
    signal: CancellationSignal?
): Cursor?
```

| Parameters ||
|---|---|
| `rootId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the root to return trash items for. This value cannot be `null`. |
| `projection` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>?: list of `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract.Document` columns to put into the cursor. If `null` all supported columns should be included. |
| `queryArgs` | [Bundle](../android.os/Bundle.md)?: the extra query arguments. This value may be `null`. |
| --- | --- |
| `signal` | [CancellationSignal](../android.os/CancellationSignal.md)?: used by the caller to signal if the request should be cancelled. May be null. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/database/Cursor.html#?` | a cursor of trashed documents. This will be called for each provider (for local just externalstorage provider) and combine the results. This value may be `null`. |

| Exceptions ||
|---|---|
| `android.app.AuthenticationRequiredException` | If authentication is required from the user (such as login credentials), but it is not guaranteed that the client will handle this properly. |

### removeDocument

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun removeDocument(
    documentId: String!, 
    parentDocumentId: String!
): Unit
```

Removes the requested document or a document tree.

In contrast to `https://developer.android.com/reference/kotlin/android/provider/DocumentsProvider#deleteDocument(kotlin.String)` it requires specifying the parent. This method is especially useful if the document can be in multiple parents.

It's the responsibility of the provider to revoke grants if the document is removed from the last parent, and effectively the document is deleted.

| Parameters ||
|---|---|
| `documentId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the document to remove. |
| `parentDocumentId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the parent of the document to move. |

| Exceptions ||
|---|---|
| `android.app.AuthenticationRequiredException` | If authentication is required from the user (such as login credentials), but it is not guaranteed that the client will handle this properly. |

### renameDocument

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun renameDocument(
    documentId: String!, 
    displayName: String!
): String!
```

Rename an existing document.

If a different `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract.Document#COLUMN_DOCUMENT_ID:kotlin.String` must be used to represent the renamed document, generate and return it. Any outstanding URI permission grants will be updated to point at the new document. If the original `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract.Document#COLUMN_DOCUMENT_ID:kotlin.String` is still valid after the rename, return `null`.

| Parameters ||
|---|---|
| `documentId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the document to rename. |
| `displayName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the updated display name of the document. The provider may alter this name to meet any internal constraints, such as avoiding conflicting names. |

| Exceptions ||
|---|---|
| `android.app.AuthenticationRequiredException` | If authentication is required from the user (such as login credentials), but it is not guaranteed that the client will handle this properly. |

### restoreDocumentFromTrash

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun restoreDocumentFromTrash(
    documentId: String, 
    targetParentDocumentId: String?
): String?
```

Restore the specified trash document.

Upon restoring a document, the document will be restored from trash to the specified target parent document.

| Parameters ||
|---|---|
| `documentId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the document to restore. This value cannot be `null`. |
| `targetParentDocumentId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: the target location to restore the document to. If `null`, the restore path will be obtained from the `documentId` |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?` | the document id of the restored document or return `null` in case of failure. |

| Exceptions ||
|---|---|
| `android.app.AuthenticationRequiredException` | If authentication is required from the user (such as login credentials), but it is not guaranteed that the client will handle this properly. |

### revokeDocumentPermission

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun revokeDocumentPermission(documentId: String!): Unit
```

Revoke any active permission grants for the given `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract.Document#COLUMN_DOCUMENT_ID:kotlin.String`, usually called when a document becomes invalid. Follows the same semantics as `https://developer.android.com/reference/kotlin/android/content/Context.html#revokeUriPermission(android.net.Uri,%20kotlin.Int)`.

### trashDocument

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun trashDocument(documentId: String): String?
```

Trash the requested document.

Upon trashing a document, the document will be marked as trashed. It will not be accessible other then trash page until `https://developer.android.com/reference/kotlin/android/provider/DocumentsProvider#restoreDocumentFromTrash(kotlin.String,%20kotlin.String)`. Any URI permission grants for the given document will be revoked.

| Parameters ||
|---|---|
| `documentId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the document to trash. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?` | the document id of the trashed document or return `null` in case of failure. |

| Exceptions ||
|---|---|
| `android.app.AuthenticationRequiredException` | If authentication is required from the user (such as login credentials), but it is not guaranteed that the client will handle this properly. |

### update

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun update(
    uri: Uri, 
    values: ContentValues?, 
    selection: String?, 
    selectionArgs: Array<String!>?
): Int
```

Implementation is provided by the parent class. Throws by default, and cannot be overridden.

| Parameters ||
|---|---|
| `uri` | [Uri](../android.net/Uri.md): The URI to query. This can potentially have a record ID if this is an update request for a specific record. This value cannot be `null`. |
| `values` | [ContentValues](../android.content/ContentValues.md)?: A set of column_name/value pairs to update in the database. This value may be `null`. |
| `selection` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: An optional filter to match rows to update. This value may be `null`. |
| --- | --- |
| `selectionArgs` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>?: This value may be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the number of rows affected. |
