Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DocumentsContract

```
class DocumentsContract
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.provider.DocumentsContract](https://developer.android.com/reference/kotlin/android/provider/DocumentsContract#) |

Defines the contract between a documents provider and the platform.

To create a document provider, extend `https://developer.android.com/reference/kotlin/android/provider/DocumentsProvider`, which provides a foundational implementation of this contract.

All client apps must hold a valid URI permission grant to access documents, typically issued when a user makes a selection through `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_OPEN_DOCUMENT:kotlin.String`, `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_CREATE_DOCUMENT:kotlin.String`, or `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_OPEN_DOCUMENT_TREE:kotlin.String`.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract.Document` Constants related to a document, including `https://developer.android.com/reference/kotlin/android/database/Cursor.html#` column names and flags. |
| | `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract.Path` Holds a path from a document to a particular document under it. |
| | `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract.Root` Constants related to a root of documents, including `https://developer.android.com/reference/kotlin/android/database/Cursor.html#` column names and flags. |

| Constants ||
|---|---|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract#ACTION_DOCUMENT_SETTINGS:kotlin.String` Action of intent issued by DocumentsUI when user wishes to open/configure/manage a particular document in the provider application. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract#CATEGORY_APPROVED_DOCUMENT_HANDLER:kotlin.String` Intent category to filter for activities that can handle document intents. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract#EXTRA_ERROR:kotlin.String` Optional string included in a directory `https://developer.android.com/reference/kotlin/android/database/Cursor.html#getExtras()` providing an error message that should be shown to a user. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract#EXTRA_EXCLUDE_SELF:kotlin.String` Set this in a DocumentsUI intent to cause a package's own roots to be excluded from the roots list. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract#EXTRA_INFO:kotlin.String` Optional string included in a directory `https://developer.android.com/reference/kotlin/android/database/Cursor.html#getExtras()` providing an informational message that should be shown to a user. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract#EXTRA_INITIAL_URI:kotlin.String` Sets the desired initial location visible to user when file chooser is shown. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract#EXTRA_LOADING:kotlin.String` Optional boolean flag included in a directory `https://developer.android.com/reference/kotlin/android/database/Cursor.html#getExtras()` indicating that a document provider is still loading data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract#EXTRA_ORIENTATION:kotlin.String` An extra number of degrees that an image should be rotated during the decode process to be presented correctly. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract#EXTRA_PROMPT:kotlin.String` Overrides the default prompt text in DocumentsUI when set in an intent. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract#METADATA_EXIF:kotlin.String` Get Exif information using DocumentsContract#getDocumentMetadata. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract#METADATA_TREE_COUNT:kotlin.String` Get total count of all documents currently stored under the given directory tree. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract#METADATA_TREE_SIZE:kotlin.String` Get total size of all documents currently stored under the given directory tree. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract#METADATA_TYPES:kotlin.String` Get string array identifies the type or types of metadata returned using DocumentsContract#getDocumentMetadata. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract#PROVIDER_INTERFACE:kotlin.String` Intent action used to identify `https://developer.android.com/reference/kotlin/android/provider/DocumentsProvider` instances. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract#QUERY_ARG_DISPLAY_NAME:kotlin.String` Key for `https://developer.android.com/reference/kotlin/android/provider/DocumentsProvider` to query display name is matched. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract#QUERY_ARG_EXCLUDE_MEDIA:kotlin.String` Key for `https://developer.android.com/reference/kotlin/android/provider/DocumentsProvider` to decide whether the files that have been added to MediaStore should be excluded. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract#QUERY_ARG_FILE_SIZE_OVER:kotlin.String` Key for `https://developer.android.com/reference/kotlin/android/provider/DocumentsProvider` to query the file size in bytes is larger than the value. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract#QUERY_ARG_LAST_MODIFIED_AFTER:kotlin.String` Key for `https://developer.android.com/reference/kotlin/android/provider/DocumentsProvider` to query the last modified time is newer than the value. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract#QUERY_ARG_MIME_TYPES:kotlin.String` Key for `https://developer.android.com/reference/kotlin/android/provider/DocumentsProvider` to query mime types is matched. |

| Public methods ||
|---|---|
| static [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)! | `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract#buildChildDocumentsUri(kotlin.String,%20kotlin.String)(authority: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, parentDocumentId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Build URI representing the children of the target directory in a document provider. |
| static [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)! | `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract#buildChildDocumentsUriUsingTree(android.net.Uri,%20kotlin.String)(treeUri: https://developer.android.com/reference/kotlin/android/net/Uri.html#!, parentDocumentId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Build URI representing the children of the target directory in a document provider. |
| static [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)! | `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract#buildDocumentUri(kotlin.String,%20kotlin.String)(authority: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, documentId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Build URI representing the target `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract.Document#COLUMN_DOCUMENT_ID:kotlin.String` in a document provider. |
| static [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)! | `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract#buildDocumentUriUsingTree(android.net.Uri,%20kotlin.String)(treeUri: https://developer.android.com/reference/kotlin/android/net/Uri.html#!, documentId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Build URI representing the target `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract.Document#COLUMN_DOCUMENT_ID:kotlin.String` in a document provider. |
| static [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)! | `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract#buildRecentDocumentsUri(kotlin.String,%20kotlin.String)(authority: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, rootId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Build URI representing the recently modified documents of a specific root in a document provider. |
| static [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)! | `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract#buildRootUri(kotlin.String,%20kotlin.String)(authority: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, rootId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Build URI representing the given `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract.Root#COLUMN_ROOT_ID:kotlin.String` in a document provider. |
| static [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)! | `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract#buildRootsUri(kotlin.String)(authority: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Build URI representing the roots of a document provider. |
| static [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#) | `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract#buildSearchDocumentsUri(android.net.Uri,%20kotlin.String)(parentDocumentUri: https://developer.android.com/reference/kotlin/android/net/Uri.html#, query: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?)` Build URI representing a search for matching documents under a specific directory in a document provider. |
| static [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)! | `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract#buildSearchDocumentsUri(kotlin.String,%20kotlin.String,%20kotlin.String)(authority: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, rootId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, query: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Build URI representing a search for matching documents under a specific root in a document provider. |
| static [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#) | `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract#buildTrashDocumentsUri(kotlin.String,%20kotlin.String)(authority: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, rootId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Returns URI representing the query trash documents of a specific document provider. |
| static [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)! | `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract#buildTreeDocumentUri(kotlin.String,%20kotlin.String)(authority: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, documentId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Build URI representing access to descendant documents of the given `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract.Document#COLUMN_DOCUMENT_ID:kotlin.String`. |
| static [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)? | `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract#copyDocument(android.content.ContentResolver,%20android.net.Uri,%20android.net.Uri)(content: https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#, sourceDocumentUri: https://developer.android.com/reference/kotlin/android/net/Uri.html#, targetParentDocumentUri: https://developer.android.com/reference/kotlin/android/net/Uri.html#)` Copies the given document. |
| static [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)? | `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract#createDocument(android.content.ContentResolver,%20android.net.Uri,%20kotlin.String,%20kotlin.String)(content: https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#, parentDocumentUri: https://developer.android.com/reference/kotlin/android/net/Uri.html#, mimeType: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, displayName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Create a new document with given MIME type and display name. |
| static [IntentSender](https://developer.android.com/reference/kotlin/android/content/IntentSender.html#)? | `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract#createWebLinkIntent(android.content.ContentResolver,%20android.net.Uri,%20android.os.Bundle)(content: https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#, uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#, options: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?)` Creates an intent for obtaining a web link for the specified document. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract#deleteDocument(android.content.ContentResolver,%20android.net.Uri)(content: https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#, documentUri: https://developer.android.com/reference/kotlin/android/net/Uri.html#)` Delete the given document. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract#ejectRoot(android.content.ContentResolver,%20android.net.Uri)(content: https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#, rootUri: https://developer.android.com/reference/kotlin/android/net/Uri.html#)` Ejects the given root. |
| static [DocumentsContract.Path](https://developer.android.com/reference/kotlin/android/provider/DocumentsContract.Path)? | `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract#findDocumentPath(android.content.ContentResolver,%20android.net.Uri)(content: https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#, treeUri: https://developer.android.com/reference/kotlin/android/net/Uri.html#)` Finds the canonical path from the top of the document tree. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract#getDocumentId(android.net.Uri)(documentUri: https://developer.android.com/reference/kotlin/android/net/Uri.html#!)` Extract the `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract.Document#COLUMN_DOCUMENT_ID:kotlin.String` from the given URI. |
| static [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)? | `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract#getDocumentMetadata(android.content.ContentResolver,%20android.net.Uri)(content: https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#, documentUri: https://developer.android.com/reference/kotlin/android/net/Uri.html#)` Returns metadata associated with the document. |
| static [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#)? | `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract#getDocumentThumbnail(android.content.ContentResolver,%20android.net.Uri,%20android.graphics.Point,%20android.os.CancellationSignal)(content: https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#, documentUri: https://developer.android.com/reference/kotlin/android/net/Uri.html#, size: https://developer.android.com/reference/kotlin/android/graphics/Point.html#, signal: https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#?)` Return thumbnail representing the document at the given URI. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract#getRootId(android.net.Uri)(rootUri: https://developer.android.com/reference/kotlin/android/net/Uri.html#!)` Extract the `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract.Root#COLUMN_ROOT_ID:kotlin.String` from the given URI. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract#getSearchDocumentsQuery(android.net.Uri)(searchDocumentsUri: https://developer.android.com/reference/kotlin/android/net/Uri.html#!)` Extract the search query from a URI built by `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract#buildSearchDocumentsUri(kotlin.String,%20kotlin.String,%20kotlin.String)`. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract#getTreeDocumentId(android.net.Uri)(documentUri: https://developer.android.com/reference/kotlin/android/net/Uri.html#!)` Extract the via `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract.Document#COLUMN_DOCUMENT_ID:kotlin.String` from the given URI. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract#isChildDocument(android.content.ContentResolver,%20android.net.Uri,%20android.net.Uri)(content: https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#, parentDocumentUri: https://developer.android.com/reference/kotlin/android/net/Uri.html#, childDocumentUri: https://developer.android.com/reference/kotlin/android/net/Uri.html#)` Test if a document is descendant (child, grandchild, etc) from the given parent. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract#isDocumentUri(android.content.Context,%20android.net.Uri)(context: https://developer.android.com/reference/kotlin/android/content/Context.html#!, uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#?)` Test if the given URI represents a `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract.Document` backed by a `https://developer.android.com/reference/kotlin/android/provider/DocumentsProvider`. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract#isRootUri(android.content.Context,%20android.net.Uri)(context: https://developer.android.com/reference/kotlin/android/content/Context.html#, uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#?)` Test if the given URI represents specific root backed by `https://developer.android.com/reference/kotlin/android/provider/DocumentsProvider`. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract#isRootsUri(android.content.Context,%20android.net.Uri)(context: https://developer.android.com/reference/kotlin/android/content/Context.html#, uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#?)` Test if the given URI represents all roots of the authority backed by `https://developer.android.com/reference/kotlin/android/provider/DocumentsProvider`. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract#isTreeUri(android.net.Uri)(uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#!)` Test if the given URI represents a `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract.Document` tree. |
| static [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)? | `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract#moveDocument(android.content.ContentResolver,%20android.net.Uri,%20android.net.Uri,%20android.net.Uri)(content: https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#, sourceDocumentUri: https://developer.android.com/reference/kotlin/android/net/Uri.html#, sourceParentDocumentUri: https://developer.android.com/reference/kotlin/android/net/Uri.html#, targetParentDocumentUri: https://developer.android.com/reference/kotlin/android/net/Uri.html#)` Moves the given document under a new parent. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract#removeDocument(android.content.ContentResolver,%20android.net.Uri,%20android.net.Uri)(content: https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#, documentUri: https://developer.android.com/reference/kotlin/android/net/Uri.html#, parentDocumentUri: https://developer.android.com/reference/kotlin/android/net/Uri.html#)` Removes the given document from a parent directory. |
| static [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)? | `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract#renameDocument(android.content.ContentResolver,%20android.net.Uri,%20kotlin.String)(content: https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#, documentUri: https://developer.android.com/reference/kotlin/android/net/Uri.html#, displayName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Change the display name of an existing document. |
| static [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)? | `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract#restoreDocumentFromTrash(android.content.ContentResolver,%20android.net.Uri,%20android.net.Uri)(content: https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#, sourceDocumentUri: https://developer.android.com/reference/kotlin/android/net/Uri.html#, targetParentDocumentUri: https://developer.android.com/reference/kotlin/android/net/Uri.html#?)` Restores a document from the trash. |
| static [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)? | `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract#trashDocument(android.content.ContentResolver,%20android.net.Uri)(content: https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#, documentUri: https://developer.android.com/reference/kotlin/android/net/Uri.html#)` Trashes the given document. |

## Constants

### ACTION_DOCUMENT_SETTINGS

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_DOCUMENT_SETTINGS: String
```

Action of intent issued by DocumentsUI when user wishes to open/configure/manage a particular document in the provider application.

When issued, the intent will include the URI of the document as the intent data.

A provider wishing to provide support for this action should do two things.
- Add an `<intent-filter>` matching this action.
- When supplying information in android.provider.DocumentsProvider#queryChildDocuments, include `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract.Document#FLAG_SUPPORTS_SETTINGS:kotlin.Int` in the flags for each document that supports settings.

 Value: "android.provider.action.DOCUMENT_SETTINGS"

### CATEGORY_APPROVED_DOCUMENT_HANDLER

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CATEGORY_APPROVED_DOCUMENT_HANDLER: String
```

Intent category to filter for activities that can handle document intents.

Indicates that an approved activity can receive intents `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_SEND:kotlin.String` and/or `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_SEND_MULTIPLE:kotlin.String`. The activity's package must be allowlisted by the system file manager. The activity will appear in the system file manager as a menu item when acceptable files are selected. The activity must also define an \`android:label\` to be accepted as a menu item.

Optionally, the activity can declare the intent to be shown as an action button instead of a menu item in \`AndroidManifest.xml\`. It must include an \`android:icon\` and a meta-data entry \`android.approvedtarget.as_button\` with a value of \`true\`.

An example declaration:

```kotlin
<activity android:name=".ApprovedDocumentHandlerActivity"
          ...
    <intent-filter>
        <action android:name="android.intent.action.SEND" />
        <category android:name="android.provider.category.APPROVED_DOCUMENT_HANDLER" />
        <data android:mimeType="text/plain" />
    </intent-filter>
  </activity>
  
```

 Value: "android.provider.category.APPROVED_DOCUMENT_HANDLER"

### EXTRA_ERROR

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_ERROR: String
```

Optional string included in a directory `https://developer.android.com/reference/kotlin/android/database/Cursor.html#getExtras()` providing an error message that should be shown to a user. For example, a provider may wish to indicate that a network error occurred. The user may choose to retry, resulting in a new query.

 Value: "error"

### EXTRA_EXCLUDE_SELF

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_EXCLUDE_SELF: String
```

Set this in a DocumentsUI intent to cause a package's own roots to be excluded from the roots list.

 Value: "android.provider.extra.EXCLUDE_SELF"

### EXTRA_INFO

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_INFO: String
```

Optional string included in a directory `https://developer.android.com/reference/kotlin/android/database/Cursor.html#getExtras()` providing an informational message that should be shown to a user. For example, a provider may wish to indicate that not all documents are available.

 Value: "info"

### EXTRA_INITIAL_URI

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_INITIAL_URI: String
```

Sets the desired initial location visible to user when file chooser is shown.

Applicable to `https://developer.android.com/reference/kotlin/android/content/Intent.html#` with actions:

- `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_OPEN_DOCUMENT:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_CREATE_DOCUMENT:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_OPEN_DOCUMENT_TREE:kotlin.String`

Location should specify a document URI or a tree URI with document ID. If this URI identifies a non-directory, document navigator will attempt to use the parent of the document as the initial location.

The initial location is system specific if this extra is missing or document navigator failed to locate the desired initial location.

 Value: "android.provider.extra.INITIAL_URI"

### EXTRA_LOADING

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_LOADING: String
```

Optional boolean flag included in a directory `https://developer.android.com/reference/kotlin/android/database/Cursor.html#getExtras()` indicating that a document provider is still loading data. For example, a provider has returned some results, but is still waiting on an outstanding network request. The provider must send a content changed notification when loading is finished.

 Value: "loading"

**See Also**

- `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#notifyChange(android.net.Uri,%20android.database.ContentObserver,%20kotlin.Boolean)`

### EXTRA_ORIENTATION

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_ORIENTATION: String
```

An extra number of degrees that an image should be rotated during the decode process to be presented correctly.

 Value: "android.provider.extra.ORIENTATION"

**See Also**

- `https://developer.android.com/reference/kotlin/android/content/res/AssetFileDescriptor.html#getExtras()`
- `https://developer.android.com/reference/kotlin/android/provider/MediaStore.MediaColumns#ORIENTATION:kotlin.String`

### EXTRA_PROMPT

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_PROMPT: String
```

Overrides the default prompt text in DocumentsUI when set in an intent.

 Value: "android.provider.extra.PROMPT"

### METADATA_EXIF

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val METADATA_EXIF: String
```

Get Exif information using DocumentsContract#getDocumentMetadata.

 Value: "android:documentExif"

**See Also**

- `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract#getDocumentMetadata(android.content.ContentResolver,%20android.net.Uri)`

### METADATA_TREE_COUNT

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val METADATA_TREE_COUNT: String
```

Get total count of all documents currently stored under the given directory tree. Only valid for `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract.Document#MIME_TYPE_DIR:kotlin.String` documents.

 Value: "android:metadataTreeCount"

**See Also**

- `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract#getDocumentMetadata(android.content.ContentResolver,%20android.net.Uri)`

### METADATA_TREE_SIZE

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val METADATA_TREE_SIZE: String
```

Get total size of all documents currently stored under the given directory tree. Only valid for `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract.Document#MIME_TYPE_DIR:kotlin.String` documents.

 Value: "android:metadataTreeSize"

**See Also**

- `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract#getDocumentMetadata(android.content.ContentResolver,%20android.net.Uri)`

### METADATA_TYPES

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val METADATA_TYPES: String
```

Get string array identifies the type or types of metadata returned using DocumentsContract#getDocumentMetadata.

 Value: "android:documentMetadataTypes"

**See Also**

- `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract#getDocumentMetadata(android.content.ContentResolver,%20android.net.Uri)`

### PROVIDER_INTERFACE

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PROVIDER_INTERFACE: String
```

Intent action used to identify `https://developer.android.com/reference/kotlin/android/provider/DocumentsProvider` instances. This is used in the `<intent-filter>` of a `<provider>`.

 Value: "android.content.action.DOCUMENTS_PROVIDER"

### QUERY_ARG_DISPLAY_NAME

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val QUERY_ARG_DISPLAY_NAME: String
```

Key for `https://developer.android.com/reference/kotlin/android/provider/DocumentsProvider` to query display name is matched. The match of display name is partial matching and case-insensitive. Ex: The value is "o", the display name of the results will contain both "foo" and "Open".

 Value: "android:query-arg-display-name"

**See Also**

- `https://developer.android.com/reference/kotlin/android/provider/DocumentsProvider#querySearchDocuments(kotlin.String,%20kotlin.Array,%20android.os.Bundle)`

### QUERY_ARG_EXCLUDE_MEDIA

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val QUERY_ARG_EXCLUDE_MEDIA: String
```

Key for `https://developer.android.com/reference/kotlin/android/provider/DocumentsProvider` to decide whether the files that have been added to MediaStore should be excluded. If the value is true, exclude them. Otherwise, include them.

 Value: "android:query-arg-exclude-media"

**See Also**

- `https://developer.android.com/reference/kotlin/android/provider/DocumentsProvider#querySearchDocuments(kotlin.String,%20kotlin.Array,%20android.os.Bundle)`

### QUERY_ARG_FILE_SIZE_OVER

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val QUERY_ARG_FILE_SIZE_OVER: String
```

Key for `https://developer.android.com/reference/kotlin/android/provider/DocumentsProvider` to query the file size in bytes is larger than the value.

 Value: "android:query-arg-file-size-over"

**See Also**

- `https://developer.android.com/reference/kotlin/android/provider/DocumentsProvider#querySearchDocuments(kotlin.String,%20kotlin.Array,%20android.os.Bundle)`

### QUERY_ARG_LAST_MODIFIED_AFTER

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val QUERY_ARG_LAST_MODIFIED_AFTER: String
```

Key for `https://developer.android.com/reference/kotlin/android/provider/DocumentsProvider` to query the last modified time is newer than the value. The unit is in milliseconds since January 1, 1970 00:00:00.0 UTC.

 Value: "android:query-arg-last-modified-after"

**See Also**

- `https://developer.android.com/reference/kotlin/android/provider/DocumentsProvider#querySearchDocuments(kotlin.String,%20kotlin.Array,%20android.os.Bundle)`
- `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract.Document#COLUMN_LAST_MODIFIED:kotlin.String`

### QUERY_ARG_MIME_TYPES

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val QUERY_ARG_MIME_TYPES: String
```

Key for `https://developer.android.com/reference/kotlin/android/provider/DocumentsProvider` to query mime types is matched. The value is a string array, it can support different mime types. Each items will be treated as "OR" condition. Ex: {"image/\*" , "video/\*"}. The mime types of the results will contain both image type and video type.

 Value: "android:query-arg-mime-types"

**See Also**

- `https://developer.android.com/reference/kotlin/android/provider/DocumentsProvider#querySearchDocuments(kotlin.String,%20kotlin.Array,%20android.os.Bundle)`

## Public methods

### buildChildDocumentsUri

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun buildChildDocumentsUri(
    authority: String!, 
    parentDocumentId: String!
): Uri!
```

Build URI representing the children of the target directory in a document provider. When queried, a provider will return zero or more rows with columns defined by `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract.Document`.

| Parameters ||
|---|---|
| `parentDocumentId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the document to return children for, which must be a directory with MIME type of `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract.Document#MIME_TYPE_DIR:kotlin.String`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/provider/DocumentsProvider#queryChildDocuments(kotlin.String,%20kotlin.Array,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract#getDocumentId(android.net.Uri)`

### buildChildDocumentsUriUsingTree

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun buildChildDocumentsUriUsingTree(
    treeUri: Uri!, 
    parentDocumentId: String!
): Uri!
```

Build URI representing the children of the target directory in a document provider. When queried, a provider will return zero or more rows with columns defined by `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract.Document`.

However, instead of directly accessing the target directory, the returned URI will leverage access granted through a subtree URI, typically returned by `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_OPEN_DOCUMENT_TREE:kotlin.String`. The target directory must be a descendant (child, grandchild, etc) of the subtree.

This is typically used to access documents under a user-selected directory tree, since it doesn't require the user to separately confirm each new document access.

| Parameters ||
|---|---|
| `treeUri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)!: the subtree to leverage to gain access to the target document. The target directory must be a descendant of this subtree. |
| `parentDocumentId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the document to return children for, which the caller may not have direct access to, and which must be a directory with MIME type of `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract.Document#MIME_TYPE_DIR:kotlin.String`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_OPEN_DOCUMENT_TREE:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/provider/DocumentsProvider#isChildDocument(kotlin.String,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract#buildChildDocumentsUri(kotlin.String,%20kotlin.String)`

### buildDocumentUri

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun buildDocumentUri(
    authority: String!, 
    documentId: String!
): Uri!
```

Build URI representing the target `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract.Document#COLUMN_DOCUMENT_ID:kotlin.String` in a document provider. When queried, a provider will return a single row with columns defined by `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract.Document`.
**See Also**

- `https://developer.android.com/reference/kotlin/android/provider/DocumentsProvider#queryDocument(kotlin.String,%20kotlin.Array)`
- `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract#getDocumentId(android.net.Uri)`

### buildDocumentUriUsingTree

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun buildDocumentUriUsingTree(
    treeUri: Uri!, 
    documentId: String!
): Uri!
```

Build URI representing the target `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract.Document#COLUMN_DOCUMENT_ID:kotlin.String` in a document provider. When queried, a provider will return a single row with columns defined by `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract.Document`.

However, instead of directly accessing the target document, the returned URI will leverage access granted through a subtree URI, typically returned by `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_OPEN_DOCUMENT_TREE:kotlin.String`. The target document must be a descendant (child, grandchild, etc) of the subtree.

This is typically used to access documents under a user-selected directory tree, since it doesn't require the user to separately confirm each new document access.

| Parameters ||
|---|---|
| `treeUri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)!: the subtree to leverage to gain access to the target document. The target directory must be a descendant of this subtree. |
| `documentId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the target document, which the caller may not have direct access to. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_OPEN_DOCUMENT_TREE:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/provider/DocumentsProvider#isChildDocument(kotlin.String,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract#buildDocumentUri(kotlin.String,%20kotlin.String)`

### buildRecentDocumentsUri

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun buildRecentDocumentsUri(
    authority: String!, 
    rootId: String!
): Uri!
```

Build URI representing the recently modified documents of a specific root in a document provider. When queried, a provider will return zero or more rows with columns defined by `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract.Document`.
**See Also**

- `https://developer.android.com/reference/kotlin/android/provider/DocumentsProvider#queryRecentDocuments(kotlin.String,%20kotlin.Array)`
- `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract#getRootId(android.net.Uri)`

### buildRootUri

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun buildRootUri(
    authority: String!, 
    rootId: String!
): Uri!
```

Build URI representing the given `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract.Root#COLUMN_ROOT_ID:kotlin.String` in a document provider.
**See Also**

- `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract#getRootId(android.net.Uri)`

### buildRootsUri

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun buildRootsUri(authority: String!): Uri!
```

Build URI representing the roots of a document provider. When queried, a provider will return one or more rows with columns defined by `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract.Root`.
**See Also**

- `https://developer.android.com/reference/kotlin/android/provider/DocumentsProvider#queryRoots(kotlin.Array)`

### buildSearchDocumentsUri

Added in [API level 37.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun buildSearchDocumentsUri(
    parentDocumentUri: Uri, 
    query: String?
): Uri
```

Build URI representing a search for matching documents under a specific directory in a document provider. When queried, a provider will return zero or more rows with columns defined by `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract.Document`.

| Parameters ||
|---|---|
| `parentDocumentUri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#): the document that search results should be restricted to, which must be a directory with mime type of `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract.Document#MIME_TYPE_DIR:kotlin.String` and have `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract.Document#FLAG_SUPPORTS_SUBTREE_SEARCH:kotlin.Int` set. This value cannot be `null`. |
| `query` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: string to match documents against. This value may be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/net/Uri.html#` | This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/provider/DocumentsProvider#querySearchDocuments(kotlin.String,%20kotlin.Array,%20android.os.Bundle,%20android.os.CancellationSignal)`
- `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract#getDocumentId(android.net.Uri)`
- `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract#getSearchDocumentsQuery(android.net.Uri)`

### buildSearchDocumentsUri

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun buildSearchDocumentsUri(
    authority: String!, 
    rootId: String!, 
    query: String!
): Uri!
```

Build URI representing a search for matching documents under a specific root in a document provider. When queried, a provider will return zero or more rows with columns defined by `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract.Document`.
**See Also**

- `https://developer.android.com/reference/kotlin/android/provider/DocumentsProvider#querySearchDocuments(kotlin.String,%20kotlin.String,%20kotlin.Array)`
- `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract#getRootId(android.net.Uri)`
- `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract#getSearchDocumentsQuery(android.net.Uri)`

### buildTrashDocumentsUri

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun buildTrashDocumentsUri(
    authority: String, 
    rootId: String
): Uri
```

Returns URI representing the query trash documents of a specific document provider.

| Parameters ||
|---|---|
| `authority` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |
| `rootId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/net/Uri.html#` | This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/provider/DocumentsProvider#queryTrashDocuments(kotlin.String,%20kotlin.Array,%20android.os.Bundle,%20android.os.CancellationSignal)`
- `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract#getRootId(android.net.Uri)`

### buildTreeDocumentUri

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun buildTreeDocumentUri(
    authority: String!, 
    documentId: String!
): Uri!
```

Build URI representing access to descendant documents of the given `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract.Document#COLUMN_DOCUMENT_ID:kotlin.String`.
**See Also**

- `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract#getTreeDocumentId(android.net.Uri)`

### copyDocument

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun copyDocument(
    content: ContentResolver, 
    sourceDocumentUri: Uri, 
    targetParentDocumentUri: Uri
): Uri?
```

Copies the given document.

| Parameters ||
|---|---|
| `content` | [ContentResolver](https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#): This value cannot be `null`. |
| `sourceDocumentUri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#): document with `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract.Document#FLAG_SUPPORTS_COPY:kotlin.Int` This value cannot be `null`. |
| `targetParentDocumentUri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#): document which will become a parent of the source document's copy. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/net/Uri.html#?` | the copied document, or `null` if failed. |

### createDocument

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun createDocument(
    content: ContentResolver, 
    parentDocumentUri: Uri, 
    mimeType: String, 
    displayName: String
): Uri?
```

Create a new document with given MIME type and display name.

| Parameters ||
|---|---|
| `content` | [ContentResolver](https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#): This value cannot be `null`. |
| `parentDocumentUri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#): directory with `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract.Document#FLAG_DIR_SUPPORTS_CREATE:kotlin.Int` This value cannot be `null`. |
| `mimeType` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): MIME type of new document. This value cannot be `null`. |
| `displayName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): name of new document. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/net/Uri.html#?` | newly created document, or `null` if failed |

### createWebLinkIntent

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun createWebLinkIntent(
    content: ContentResolver, 
    uri: Uri, 
    options: Bundle?
): IntentSender?
```

Creates an intent for obtaining a web link for the specified document.

Note, that due to internal limitations, if there is already a web link intent created for the specified document but with different options, then it may be overridden.

Providers are required to show confirmation UI for all new permissions granted for the linked document.

If list of recipients is known, then it should be passed in options as `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_EMAIL:kotlin.String` as a list of email addresses. Note, that this is just a hint for the provider, which can ignore the list. In either case the provider is required to show a UI for letting the user confirm any new permission grants.

Note, that the entire `options` bundle will be sent to the provider backing the passed `uri`. Make sure that you trust the provider before passing any sensitive information.

Since this API may show a UI, it cannot be called from background.

In order to obtain the Web Link use code like this:

```kotlin
<code>
  void onSomethingHappened() {
    IntentSender sender = DocumentsContract.createWebLinkIntent(<i>...</i>);
    if (sender != null) {
      startIntentSenderForResult(
          sender,
          WEB_LINK_REQUEST_CODE,
          null, 0, 0, 0, null);
    }
  }
 
  <i>(...)</i>
 
  void onActivityResult(int requestCode, int resultCode, Intent data) {
    if (requestCode == WEB_LINK_REQUEST_CODE &amp;&amp; resultCode == RESULT_OK) {
      Uri weblinkUri = data.getData();
      <i>...</i>
    }
  }
  </code>
```

| Parameters ||
|---|---|
| `content` | [ContentResolver](https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#): This value cannot be `null`. |
| `uri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#): uri for the document to create a link to. This value cannot be `null`. |
| `options` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)?: Extra information for generating the link. This value may be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/IntentSender.html#?` | an intent sender to obtain the web link, or null if the document is not linkable, or creating the intent sender failed. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/provider/DocumentsProvider#createWebLinkIntent(kotlin.String,%20android.os.Bundle)`
- `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_EMAIL:kotlin.String`

### deleteDocument

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun deleteDocument(
    content: ContentResolver, 
    documentUri: Uri
): Boolean
```

Delete the given document.

| Parameters ||
|---|---|
| `content` | [ContentResolver](https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#): This value cannot be `null`. |
| `documentUri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#): document with `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract.Document#FLAG_SUPPORTS_DELETE:kotlin.Int` This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | if the document was deleted successfully. |

### ejectRoot

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun ejectRoot(
    content: ContentResolver, 
    rootUri: Uri
): Unit
```

Ejects the given root. It throws `https://developer.android.com/reference/kotlin/java/lang/IllegalStateException.html#` when ejection failed.

| Parameters ||
|---|---|
| `content` | [ContentResolver](https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#): This value cannot be `null`. |
| `rootUri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#): root with `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract.Root#FLAG_SUPPORTS_EJECT:kotlin.Int` to be ejected. This value cannot be `null`. |

### findDocumentPath

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun findDocumentPath(
    content: ContentResolver, 
    treeUri: Uri
): DocumentsContract.Path?
```

Finds the canonical path from the top of the document tree. The `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract.Path#getPath()` of the return value contains the document ID of all documents along the path from the top the document tree to the requested document, both inclusive. The `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract.Path#getRootId()` of the return value returns `null`.

| Parameters ||
|---|---|
| `content` | [ContentResolver](https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#): This value cannot be `null`. |
| `treeUri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#): treeUri of the document which path is requested. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract.Path?` | the path of the document, or `null` if failed. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/provider/DocumentsProvider#findDocumentPath(kotlin.String,%20kotlin.String)`

### getDocumentId

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getDocumentId(documentUri: Uri!): String!
```

Extract the `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract.Document#COLUMN_DOCUMENT_ID:kotlin.String` from the given URI.
**See Also**

- `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract#isDocumentUri(android.content.Context,%20android.net.Uri)`

### getDocumentMetadata

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getDocumentMetadata(
    content: ContentResolver, 
    documentUri: Uri
): Bundle?
```

Returns metadata associated with the document. The type of metadata returned is specific to the document type. For example the data returned for an image file will likely consist primarily or solely of EXIF metadata.

The returned `https://developer.android.com/reference/kotlin/android/os/Bundle.html#` will contain zero or more entries depending on the type of data supported by the document provider.

1. A `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract#METADATA_TYPES:kotlin.String` containing a `String[]` value. The string array identifies the type or types of metadata returned. Each value in the can be used to access a `https://developer.android.com/reference/kotlin/android/os/Bundle.html#` of data containing that type of data.
2. An entry each for each type of returned metadata. Each set of metadata is itself represented as a bundle and accessible via a string key naming the type of data.

Example:

<br />

```kotlin
<code>
      Bundle metadata = DocumentsContract.getDocumentMetadata(client, imageDocUri, tags);
      if (metadata.containsKey(DocumentsContract.METADATA_EXIF)) {
          Bundle exif = metadata.getBundle(DocumentsContract.METADATA_EXIF);
          int imageLength = exif.getInt(ExifInterface.TAG_IMAGE_LENGTH);
      }
  </code>
```

| Parameters ||
|---|---|
| `content` | [ContentResolver](https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#): This value cannot be `null`. |
| `documentUri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#): a Document URI. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/os/Bundle.html#?` | a Bundle of Bundles. This value may be `null`. |

### getDocumentThumbnail

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getDocumentThumbnail(
    content: ContentResolver, 
    documentUri: Uri, 
    size: Point, 
    signal: CancellationSignal?
): Bitmap?
```

Return thumbnail representing the document at the given URI. Callers are responsible for their own in-memory caching.

| Parameters ||
|---|---|
| `content` | [ContentResolver](https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#): This value cannot be `null`. |
| `documentUri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#): document to return thumbnail for, which must have `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract.Document#FLAG_SUPPORTS_THUMBNAIL:kotlin.Int` set. This value cannot be `null`. |
| `size` | [Point](https://developer.android.com/reference/kotlin/android/graphics/Point.html#): optimal thumbnail size desired. A provider may return a thumbnail of a different size, but never more than double the requested size. This value cannot be `null`. |
| `signal` | [CancellationSignal](https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#)?: signal used to indicate if caller is no longer interested in the thumbnail. This value may be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#?` | decoded thumbnail, or `null` if problem was encountered. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/provider/DocumentsProvider#openDocumentThumbnail(kotlin.String,%20android.graphics.Point,%20android.os.CancellationSignal)`

### getRootId

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getRootId(rootUri: Uri!): String!
```

Extract the `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract.Root#COLUMN_ROOT_ID:kotlin.String` from the given URI.

### getSearchDocumentsQuery

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getSearchDocumentsQuery(searchDocumentsUri: Uri!): String!
```

Extract the search query from a URI built by `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract#buildSearchDocumentsUri(kotlin.String,%20kotlin.String,%20kotlin.String)`.

### getTreeDocumentId

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getTreeDocumentId(documentUri: Uri!): String!
```

Extract the via `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract.Document#COLUMN_DOCUMENT_ID:kotlin.String` from the given URI.

### isChildDocument

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun isChildDocument(
    content: ContentResolver, 
    parentDocumentUri: Uri, 
    childDocumentUri: Uri
): Boolean
```

Test if a document is descendant (child, grandchild, etc) from the given parent.

| Parameters ||
|---|---|
| `content` | [ContentResolver](https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#): This value cannot be `null`. |
| `parentDocumentUri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#): parent to verify against. This value cannot be `null`. |
| `childDocumentUri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#): child to verify. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | if given document is a descendant of the given parent. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract.Root#FLAG_SUPPORTS_IS_CHILD:kotlin.Int`

### isDocumentUri

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun isDocumentUri(
    context: Context!, 
    uri: Uri?
): Boolean
```

Test if the given URI represents a `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract.Document` backed by a `https://developer.android.com/reference/kotlin/android/provider/DocumentsProvider`.

| Parameters ||
|---|---|
| `uri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)?: This value may be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract#buildDocumentUri(kotlin.String,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract#buildDocumentUriUsingTree(android.net.Uri,%20kotlin.String)`

### isRootUri

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun isRootUri(
    context: Context, 
    uri: Uri?
): Boolean
```

Test if the given URI represents specific root backed by `https://developer.android.com/reference/kotlin/android/provider/DocumentsProvider`.

| Parameters ||
|---|---|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#): This value cannot be `null`. |
| `uri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)?: This value may be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract#buildRootUri(kotlin.String,%20kotlin.String)`

### isRootsUri

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun isRootsUri(
    context: Context, 
    uri: Uri?
): Boolean
```

Test if the given URI represents all roots of the authority backed by `https://developer.android.com/reference/kotlin/android/provider/DocumentsProvider`.

| Parameters ||
|---|---|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#): This value cannot be `null`. |
| `uri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)?: This value may be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract#buildRootsUri(kotlin.String)`

### isTreeUri

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun isTreeUri(uri: Uri!): Boolean
```

Test if the given URI represents a `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract.Document` tree.
**See Also**

- `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract#buildTreeDocumentUri(kotlin.String,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract#getTreeDocumentId(android.net.Uri)`

### moveDocument

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun moveDocument(
    content: ContentResolver, 
    sourceDocumentUri: Uri, 
    sourceParentDocumentUri: Uri, 
    targetParentDocumentUri: Uri
): Uri?
```

Moves the given document under a new parent.

| Parameters ||
|---|---|
| `content` | [ContentResolver](https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#): This value cannot be `null`. |
| `sourceDocumentUri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#): document with `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract.Document#FLAG_SUPPORTS_MOVE:kotlin.Int` This value cannot be `null`. |
| `sourceParentDocumentUri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#): parent document of the document to move. This value cannot be `null`. |
| `targetParentDocumentUri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#): document which will become a new parent of the source document. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/net/Uri.html#?` | the moved document, or `null` if failed. |

### removeDocument

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun removeDocument(
    content: ContentResolver, 
    documentUri: Uri, 
    parentDocumentUri: Uri
): Boolean
```

Removes the given document from a parent directory.

In contrast to `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract#deleteDocument(android.content.ContentResolver,%20android.net.Uri)` it requires specifying the parent. This method is especially useful if the document can be in multiple parents.

| Parameters ||
|---|---|
| `content` | [ContentResolver](https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#): This value cannot be `null`. |
| `documentUri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#): document with `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract.Document#FLAG_SUPPORTS_REMOVE:kotlin.Int` This value cannot be `null`. |
| `parentDocumentUri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#): parent document of the document to remove. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the document was removed successfully. |

### renameDocument

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun renameDocument(
    content: ContentResolver, 
    documentUri: Uri, 
    displayName: String
): Uri?
```

Change the display name of an existing document.

If the underlying provider needs to create a new `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract.Document#COLUMN_DOCUMENT_ID:kotlin.String` to represent the updated display name, that new document is returned and the original document is no longer valid. Otherwise, the original document is returned.

| Parameters ||
|---|---|
| `content` | [ContentResolver](https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#): This value cannot be `null`. |
| `documentUri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#): document with `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract.Document#FLAG_SUPPORTS_RENAME:kotlin.Int` This value cannot be `null`. |
| `displayName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): updated name for document. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/net/Uri.html#?` | the existing or new document after the rename, or `null` if failed. |

### restoreDocumentFromTrash

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun restoreDocumentFromTrash(
    content: ContentResolver, 
    sourceDocumentUri: Uri, 
    targetParentDocumentUri: Uri?
): Uri?
```

Restores a document from the trash.

| Parameters ||
|---|---|
| `content` | [ContentResolver](https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#): This value cannot be `null`. |
| `sourceDocumentUri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#): trashed document to restore. This value cannot be `null`. |
| `targetParentDocumentUri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)?: parent document to restore the document to. This value may be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/net/Uri.html#?` | the restored document, or `null` if failed. |

| Exceptions ||
|---|---|
| `java.io.FileNotFoundException` | if the `sourceDocumentUri` does not exist or the `targetParentDocumentUri` does not exist. |
| `java.lang.IllegalStateException` | if the document cannot be restored (e.g., already restored, or original parent is invalid). |
| `java.lang.UnsupportedOperationException` | if the document provider does not support restoring. |

### trashDocument

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun trashDocument(
    content: ContentResolver, 
    documentUri: Uri
): Uri?
```

Trashes the given document.

| Parameters ||
|---|---|
| `content` | [ContentResolver](https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#): This value cannot be `null`. |
| `documentUri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#): document with `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract.Document#FLAG_SUPPORTS_TRASH:kotlin.Int` This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/net/Uri.html#?` | the trashed document, or `null` if failed. |

| Exceptions ||
|---|---|
| `java.io.FileNotFoundException` | if the documentUri does not exist. |
| `java.lang.IllegalArgumentException` | if the document does not support trashing. |
| `java.lang.UnsupportedOperationException` | if the document provider does not support trashing. |
