# ContentProviderClient

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ContentProviderClient

Kotlin| [Java](https://developer.android.com/reference/android/content/ContentProviderClient "View this page in Java") 

```
open class ContentProviderClient : AutoCloseable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.content.ContentProviderClient](https://developer.android.com/reference/kotlin/android/content/ContentProviderClient#) |

The public interface object used to interact with a specific [ContentProvider](https://developer.android.com/reference/kotlin/android/content/ContentProvider).

Instances can be obtained by calling android.content.ContentResolver#acquireContentProviderClient or android.content.ContentResolver#acquireUnstableContentProviderClient. Instances must be released using [close()](https://developer.android.com/reference/kotlin/android/content/ContentProviderClient#close())in order to indicate to the system that the underlying [ContentProvider](https://developer.android.com/reference/kotlin/android/content/ContentProvider) is no longer needed and can be killed to free up resources.

Note that you should generally create a new ContentProviderClient instance for each thread that will be performing operations. Unlike [ContentResolver](https://developer.android.com/reference/kotlin/android/content/ContentResolver), the methods here such as #query and #openFile are not thread safe -- you must not call [close()](https://developer.android.com/reference/kotlin/android/content/ContentProviderClient#close())on the ContentProviderClient those calls are made from until you are finished with the data they have returned.

## Summary

| Public methods ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [ContentProviderResult](https://developer.android.com/reference/kotlin/android/content/ContentProviderResult)!\> | [applyBatch](https://developer.android.com/reference/kotlin/android/content/ContentProviderClient#applyBatch(kotlin.String,%20java.util.ArrayList))`(`authority:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `operations:` ` [ArrayList](https://developer.android.com/reference/kotlin/java/util/ArrayList.html#)< [ContentProviderOperation](https://developer.android.com/reference/kotlin/android/content/ContentProviderOperation)!>`)` See android. |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [ContentProviderResult](https://developer.android.com/reference/kotlin/android/content/ContentProviderResult)!\> | [applyBatch](https://developer.android.com/reference/kotlin/android/content/ContentProviderClient#applyBatch(java.util.ArrayList))`(`operations:` ` [ArrayList](https://developer.android.com/reference/kotlin/java/util/ArrayList.html#)< [ContentProviderOperation](https://developer.android.com/reference/kotlin/android/content/ContentProviderOperation)!>`)` See android. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [bulkInsert](https://developer.android.com/reference/kotlin/android/content/ContentProviderClient#bulkInsert(android.net.Uri,%20kotlin.Array))`(`url:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)`, `initialValues:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [ContentValues](https://developer.android.com/reference/kotlin/android/content/ContentValues)!>`)` See [ContentProvider.bulkInsert](https://developer.android.com/reference/kotlin/android/content/ContentProvider#bulkInsert(android.net.Uri,%20kotlin.Array)) |
| open [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)? | [call](https://developer.android.com/reference/kotlin/android/content/ContentProviderClient#call(kotlin.String,%20kotlin.String,%20android.os.Bundle))`(`method:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `arg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `extras:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)?`)` See [ContentProvider.call(String, String, Bundle)](https://developer.android.com/reference/kotlin/android/content/ContentProvider#call(kotlin.String,%20kotlin.String,%20android.os.Bundle)) |
| open [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)? | [call](https://developer.android.com/reference/kotlin/android/content/ContentProviderClient#call(kotlin.String,%20kotlin.String,%20kotlin.String,%20android.os.Bundle))`(`authority:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `method:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `arg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `extras:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)?`)` See [ContentProvider.call(String, String, Bundle)](https://developer.android.com/reference/kotlin/android/content/ContentProvider#call(kotlin.String,%20kotlin.String,%20android.os.Bundle)) |
| [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)? | [canonicalize](https://developer.android.com/reference/kotlin/android/content/ContentProviderClient#canonicalize(android.net.Uri))`(`url:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)`)` See [ContentProvider.canonicalize](https://developer.android.com/reference/kotlin/android/content/ContentProvider#canonicalize(android.net.Uri)) |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](https://developer.android.com/reference/kotlin/android/content/ContentProviderClient#close())`()` Closes this client connection, indicating to the system that the underlying [ContentProvider](https://developer.android.com/reference/kotlin/android/content/ContentProvider) is no longer needed. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [delete](https://developer.android.com/reference/kotlin/android/content/ContentProviderClient#delete(android.net.Uri,%20android.os.Bundle))`(`url:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)`, `extras:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)?`)` See android. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [delete](https://developer.android.com/reference/kotlin/android/content/ContentProviderClient#delete(android.net.Uri,%20kotlin.String,%20kotlin.Array))`(`url:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)`, `selection:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `selectionArgs:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>?`)` See android. |
| open [ContentProvider](https://developer.android.com/reference/kotlin/android/content/ContentProvider)? | [getLocalContentProvider](https://developer.android.com/reference/kotlin/android/content/ContentProviderClient#getLocalContentProvider())`()` Get a reference to the [ContentProvider](https://developer.android.com/reference/kotlin/android/content/ContentProvider) that is associated with this client. |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>? | [getStreamTypes](https://developer.android.com/reference/kotlin/android/content/ContentProviderClient#getStreamTypes(android.net.Uri,%20kotlin.String))`(`url:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)`, `mimeTypeFilter:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` See [ContentProvider.getStreamTypes](https://developer.android.com/reference/kotlin/android/content/ContentProvider#getStreamTypes(android.net.Uri,%20kotlin.String)) |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getType](https://developer.android.com/reference/kotlin/android/content/ContentProviderClient#getType(android.net.Uri))`(`url:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)`)` See [ContentProvider.getType](https://developer.android.com/reference/kotlin/android/content/ContentProvider#getType(android.net.Uri)) |
| open [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)? | [insert](https://developer.android.com/reference/kotlin/android/content/ContentProviderClient#insert(android.net.Uri,%20android.content.ContentValues))`(`url:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)`, `initialValues:` ` [ContentValues](https://developer.android.com/reference/kotlin/android/content/ContentValues)?`)` See android. |
| open [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)? | [insert](https://developer.android.com/reference/kotlin/android/content/ContentProviderClient#insert(android.net.Uri,%20android.content.ContentValues,%20android.os.Bundle))`(`url:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)`, `initialValues:` ` [ContentValues](https://developer.android.com/reference/kotlin/android/content/ContentValues)?`, `extras:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)?`)` See android. |
| open [AssetFileDescriptor](https://developer.android.com/reference/kotlin/android/content/res/AssetFileDescriptor)? | [openAssetFile](https://developer.android.com/reference/kotlin/android/content/ContentProviderClient#openAssetFile(android.net.Uri,%20kotlin.String))`(`url:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)`, `mode:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` See android. |
| open [AssetFileDescriptor](https://developer.android.com/reference/kotlin/android/content/res/AssetFileDescriptor)? | [openAssetFile](https://developer.android.com/reference/kotlin/android/content/ContentProviderClient#openAssetFile(android.net.Uri,%20kotlin.String,%20android.os.CancellationSignal))`(`url:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)`, `mode:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `signal:` ` [CancellationSignal](https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#)?`)` See android. |
| open [ParcelFileDescriptor](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#)? | [openFile](https://developer.android.com/reference/kotlin/android/content/ContentProviderClient#openFile(android.net.Uri,%20kotlin.String))`(`url:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)`, `mode:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` See android. |
| open [ParcelFileDescriptor](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#)? | [openFile](https://developer.android.com/reference/kotlin/android/content/ContentProviderClient#openFile(android.net.Uri,%20kotlin.String,%20android.os.CancellationSignal))`(`url:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)`, `mode:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `signal:` ` [CancellationSignal](https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#)?`)` See android. |
| [AssetFileDescriptor](https://developer.android.com/reference/kotlin/android/content/res/AssetFileDescriptor)? | [openTypedAssetFile](https://developer.android.com/reference/kotlin/android/content/ContentProviderClient#openTypedAssetFile(android.net.Uri,%20kotlin.String,%20android.os.Bundle,%20android.os.CancellationSignal))`(`uri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)`, `mimeTypeFilter:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `opts:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)?`, `signal:` ` [CancellationSignal](https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#)?`)` <br /> |
| [AssetFileDescriptor](https://developer.android.com/reference/kotlin/android/content/res/AssetFileDescriptor)? | [openTypedAssetFileDescriptor](https://developer.android.com/reference/kotlin/android/content/ContentProviderClient#openTypedAssetFileDescriptor(android.net.Uri,%20kotlin.String,%20android.os.Bundle))`(`uri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)`, `mimeType:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `opts:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)?`)` See android. |
| [AssetFileDescriptor](https://developer.android.com/reference/kotlin/android/content/res/AssetFileDescriptor)? | [openTypedAssetFileDescriptor](https://developer.android.com/reference/kotlin/android/content/ContentProviderClient#openTypedAssetFileDescriptor(android.net.Uri,%20kotlin.String,%20android.os.Bundle,%20android.os.CancellationSignal))`(`uri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)`, `mimeType:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `opts:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)?`, `signal:` ` [CancellationSignal](https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#)?`)` See android. |
| open [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#)? | [query](https://developer.android.com/reference/kotlin/android/content/ContentProviderClient#query(android.net.Uri,%20kotlin.Array,%20android.os.Bundle,%20android.os.CancellationSignal))`(`uri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)`, `projection:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>?`, `queryArgs:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!`, `cancellationSignal:` ` [CancellationSignal](https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#)?`)` See android. |
| open [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#)? | [query](https://developer.android.com/reference/kotlin/android/content/ContentProviderClient#query(android.net.Uri,%20kotlin.Array,%20kotlin.String,%20kotlin.Array,%20kotlin.String))`(`url:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)`, `projection:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>?`, `selection:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `selectionArgs:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>?`, `sortOrder:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` See android. |
| open [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#)? | [query](https://developer.android.com/reference/kotlin/android/content/ContentProviderClient#query(android.net.Uri,%20kotlin.Array,%20kotlin.String,%20kotlin.Array,%20kotlin.String,%20android.os.CancellationSignal))`(`uri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)`, `projection:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>?`, `selection:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `selectionArgs:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>?`, `sortOrder:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `cancellationSignal:` ` [CancellationSignal](https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#)?`)` See android. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [refresh](https://developer.android.com/reference/kotlin/android/content/ContentProviderClient#refresh(android.net.Uri,%20android.os.Bundle,%20android.os.CancellationSignal))`(`url:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)!`, `extras:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)?`, `cancellationSignal:` ` [CancellationSignal](https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#)?`)` See [ContentProvider.refresh](https://developer.android.com/reference/kotlin/android/content/ContentProvider#refresh(android.net.Uri,%20android.os.Bundle,%20android.os.CancellationSignal)) |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [release](https://developer.android.com/reference/kotlin/android/content/ContentProviderClient#release())`()` <br /> |
| [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)? | [uncanonicalize](https://developer.android.com/reference/kotlin/android/content/ContentProviderClient#uncanonicalize(android.net.Uri))`(`url:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)`)` See [ContentProvider.uncanonicalize](https://developer.android.com/reference/kotlin/android/content/ContentProvider#uncanonicalize(android.net.Uri)) |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [update](https://developer.android.com/reference/kotlin/android/content/ContentProviderClient#update(android.net.Uri,%20android.content.ContentValues,%20android.os.Bundle))`(`url:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)`, `values:` ` [ContentValues](https://developer.android.com/reference/kotlin/android/content/ContentValues)?`, `extras:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)?`)` See android. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [update](https://developer.android.com/reference/kotlin/android/content/ContentProviderClient#update(android.net.Uri,%20android.content.ContentValues,%20kotlin.String,%20kotlin.Array))`(`url:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)`, `values:` ` [ContentValues](https://developer.android.com/reference/kotlin/android/content/ContentValues)?`, `selection:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `selectionArgs:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>?`)` See android. |

| Protected methods ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finalize](https://developer.android.com/reference/kotlin/android/content/ContentProviderClient#finalize())`()` <br /> |

## Public methods

### applyBatch

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun applyBatch(
    authority: String, 
    operations: ArrayList<ContentProviderOperation!>
): Array<ContentProviderResult!>
```

See android.content.ContentProvider#applyBatch

| Parameters ||
|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `authority` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):This value cannot be`null`. |
| `operations` | [ArrayList](https://developer.android.com/reference/kotlin/java/util/ArrayList.html#)\< [ContentProviderOperation](https://developer.android.com/reference/kotlin/android/content/ContentProviderOperation)!\>:This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [ContentProviderResult](https://developer.android.com/reference/kotlin/android/content/ContentProviderResult)!> | This value cannot be`null`. |

### applyBatch

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun applyBatch(operations: ArrayList<ContentProviderOperation!>): Array<ContentProviderResult!>
```

See android.content.ContentProvider#applyBatch

| Parameters ||
|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `operations` | [ArrayList](https://developer.android.com/reference/kotlin/java/util/ArrayList.html#)\< [ContentProviderOperation](https://developer.android.com/reference/kotlin/android/content/ContentProviderOperation)!\>:This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [ContentProviderResult](https://developer.android.com/reference/kotlin/android/content/ContentProviderResult)!> | This value cannot be`null`. |

### bulkInsert

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun bulkInsert(
    url: Uri, 
    initialValues: Array<ContentValues!>
): Int
```

See [ContentProvider.bulkInsert](https://developer.android.com/reference/kotlin/android/content/ContentProvider#bulkInsert(android.net.Uri,%20kotlin.Array))

| Parameters ||
|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `url` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#):This value cannot be`null`. |
| `initialValues` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [ContentValues](https://developer.android.com/reference/kotlin/android/content/ContentValues)!\>:This value cannot be`null`. |

### call

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun call(
    method: String, 
    arg: String?, 
    extras: Bundle?
): Bundle?
```

See [ContentProvider.call(String, String, Bundle)](https://developer.android.com/reference/kotlin/android/content/ContentProvider#call(kotlin.String,%20kotlin.String,%20android.os.Bundle))

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

See [ContentProvider.call(String, String, Bundle)](https://developer.android.com/reference/kotlin/android/content/ContentProvider#call(kotlin.String,%20kotlin.String,%20android.os.Bundle))

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------------------|
| `authority` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):This value cannot be`null`. |
| `method` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):This value cannot be`null`. |
| `arg` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:This value may be`null`. |
| `extras` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)?:This value may be`null`. |

| Return ||
|-----------------------------------------------------------------------------------|--------------------------|
| [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)? | This value may be`null`. |

### canonicalize

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun canonicalize(url: Uri): Uri?
```

See [ContentProvider.canonicalize](https://developer.android.com/reference/kotlin/android/content/ContentProvider#canonicalize(android.net.Uri))

| Parameters ||
|-------|---------------------------------------------------------------------------------------------------------|
| `url` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#):This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------|--------------------------|
| [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)? | This value may be`null`. |

### close

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun close(): Unit
```

Closes this client connection, indicating to the system that the underlying [ContentProvider](https://developer.android.com/reference/kotlin/android/content/ContentProvider) is no longer needed.

| Exceptions ||
|-----------------------|-----------------------------------|
| `java.lang.Exception` | if this resource cannot be closed |

### delete

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun delete(
    url: Uri, 
    extras: Bundle?
): Int
```

See android.content.ContentProvider#delete

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------|
| `url` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#):This value cannot be`null`. |
| `extras` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)?:This value may be`null`. |

### delete

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun delete(
    url: Uri, 
    selection: String?, 
    selectionArgs: Array<String!>?
): Int
```

See android.content.ContentProvider#delete

| Parameters ||
|-----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `url` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#):This value cannot be`null`. |
| `selection` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:This value may be`null`. |
| `selectionArgs` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>?:This value may be`null`. |

### getLocalContentProvider

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getLocalContentProvider(): ContentProvider?
```

Get a reference to the [ContentProvider](https://developer.android.com/reference/kotlin/android/content/ContentProvider) that is associated with this client. If the [ContentProvider](https://developer.android.com/reference/kotlin/android/content/ContentProvider) is running in a different process then null will be returned. This can be used if you know you are running in the same process as a provider, and want to get direct access to its implementation details.

| Return ||
|----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ContentProvider](https://developer.android.com/reference/kotlin/android/content/ContentProvider)? | If the associated [ContentProvider](https://developer.android.com/reference/kotlin/android/content/ContentProvider) is local, returns it. Otherwise returns null. |

### getStreamTypes

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getStreamTypes(
    url: Uri, 
    mimeTypeFilter: String
): Array<String!>?
```

See [ContentProvider.getStreamTypes](https://developer.android.com/reference/kotlin/android/content/ContentProvider#getStreamTypes(android.net.Uri,%20kotlin.String))

| Parameters ||
|------------------|--------------------------------------------------------------------------------------------------------------|
| `url` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#):This value cannot be`null`. |
| `mimeTypeFilter` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):This value cannot be`null`. |

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>? | This value may be`null`. |

### getType

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getType(url: Uri): String?
```

See [ContentProvider.getType](https://developer.android.com/reference/kotlin/android/content/ContentProvider#getType(android.net.Uri))

| Parameters ||
|-------|---------------------------------------------------------------------------------------------------------|
| `url` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#):This value cannot be`null`. |

| Return ||
|-----------------------------------------------------------------------------------|--------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | This value may be`null`. |

### insert

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun insert(
    url: Uri, 
    initialValues: ContentValues?
): Uri?
```

See android.content.ContentProvider#insert

| Parameters ||
|-----------------|-------------------------------------------------------------------------------------------------------------------------|
| `url` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#):This value cannot be`null`. |
| `initialValues` | [ContentValues](https://developer.android.com/reference/kotlin/android/content/ContentValues)?:This value may be`null`. |

| Return ||
|------------------------------------------------------------------------------|--------------------------|
| [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)? | This value may be`null`. |

### insert

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun insert(
    url: Uri, 
    initialValues: ContentValues?, 
    extras: Bundle?
): Uri?
```

See android.content.ContentProvider#insert

| Parameters ||
|-----------------|-------------------------------------------------------------------------------------------------------------------------|
| `url` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#):This value cannot be`null`. |
| `initialValues` | [ContentValues](https://developer.android.com/reference/kotlin/android/content/ContentValues)?:This value may be`null`. |
| `extras` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)?:This value may be`null`. |

| Return ||
|------------------------------------------------------------------------------|--------------------------|
| [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)? | This value may be`null`. |

### openAssetFile

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun openAssetFile(
    url: Uri, 
    mode: String
): AssetFileDescriptor?
```

See android.content.ContentProvider#openAssetFile. Note that this*does not*take care of non-content: URIs such as file:. It is strongly recommended you use the android.content.ContentResolver#openAssetFileDescriptor API instead.

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------|
| `url` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#):This value cannot be`null`. |
| `mode` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):This value cannot be`null`. |

| Return ||
|----------------------------------------------------------------------------------------------------------------|--------------------------|
| [AssetFileDescriptor](https://developer.android.com/reference/kotlin/android/content/res/AssetFileDescriptor)? | This value may be`null`. |

### openAssetFile

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun openAssetFile(
    url: Uri, 
    mode: String, 
    signal: CancellationSignal?
): AssetFileDescriptor?
```

See android.content.ContentProvider#openAssetFile. Note that this*does not*take care of non-content: URIs such as file:. It is strongly recommended you use the android.content.ContentResolver#openAssetFileDescriptor API instead.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------|
| `url` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#):This value cannot be`null`. |
| `mode` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):This value cannot be`null`. |
| `signal` | [CancellationSignal](https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#)?:This value may be`null`. |

| Return ||
|----------------------------------------------------------------------------------------------------------------|--------------------------|
| [AssetFileDescriptor](https://developer.android.com/reference/kotlin/android/content/res/AssetFileDescriptor)? | This value may be`null`. |

### openFile

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun openFile(
    url: Uri, 
    mode: String
): ParcelFileDescriptor?
```

See android.content.ContentProvider#openFile. Note that this*does not*take care of non-content: URIs such as file:. It is strongly recommended you use the android.content.ContentResolver#openFileDescriptor API instead.

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------|
| `url` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#):This value cannot be`null`. |
| `mode` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):This value cannot be`null`. |

| Return ||
|---------------------------------------------------------------------------------------------------------------|--------------------------|
| [ParcelFileDescriptor](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#)? | This value may be`null`. |

### openFile

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun openFile(
    url: Uri, 
    mode: String, 
    signal: CancellationSignal?
): ParcelFileDescriptor?
```

See android.content.ContentProvider#openFile. Note that this*does not*take care of non-content: URIs such as file:. It is strongly recommended you use the android.content.ContentResolver#openFileDescriptor API instead.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------|
| `url` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#):This value cannot be`null`. |
| `mode` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):This value cannot be`null`. |
| `signal` | [CancellationSignal](https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#)?:This value may be`null`. |

| Return ||
|---------------------------------------------------------------------------------------------------------------|--------------------------|
| [ParcelFileDescriptor](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#)? | This value may be`null`. |

### openTypedAssetFile

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun openTypedAssetFile(
    uri: Uri, 
    mimeTypeFilter: String, 
    opts: Bundle?, 
    signal: CancellationSignal?
): AssetFileDescriptor?
```

| Parameters ||
|------------------|------------------------------------------------------------------------------------------------------------------------------------|
| `uri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#):This value cannot be`null`. |
| `mimeTypeFilter` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):This value cannot be`null`. |
| `opts` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)?:This value may be`null`. |
| `signal` | [CancellationSignal](https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#)?:This value may be`null`. |

| Return ||
|----------------------------------------------------------------------------------------------------------------|--------------------------|
| [AssetFileDescriptor](https://developer.android.com/reference/kotlin/android/content/res/AssetFileDescriptor)? | This value may be`null`. |

### openTypedAssetFileDescriptor

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun openTypedAssetFileDescriptor(
    uri: Uri, 
    mimeType: String, 
    opts: Bundle?
): AssetFileDescriptor?
```

See android.content.ContentProvider#openTypedAssetFile

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------|
| `uri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#):This value cannot be`null`. |
| `mimeType` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):This value cannot be`null`. |
| `opts` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)?:This value may be`null`. |

| Return ||
|----------------------------------------------------------------------------------------------------------------|--------------------------|
| [AssetFileDescriptor](https://developer.android.com/reference/kotlin/android/content/res/AssetFileDescriptor)? | This value may be`null`. |

### openTypedAssetFileDescriptor

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun openTypedAssetFileDescriptor(
    uri: Uri, 
    mimeType: String, 
    opts: Bundle?, 
    signal: CancellationSignal?
): AssetFileDescriptor?
```

See android.content.ContentProvider#openTypedAssetFile

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------|
| `uri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#):This value cannot be`null`. |
| `mimeType` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):This value cannot be`null`. |
| `opts` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)?:This value may be`null`. |
| `signal` | [CancellationSignal](https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#)?:This value may be`null`. |

| Return ||
|----------------------------------------------------------------------------------------------------------------|--------------------------|
| [AssetFileDescriptor](https://developer.android.com/reference/kotlin/android/content/res/AssetFileDescriptor)? | This value may be`null`. |

### query

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun query(
    uri: Uri, 
    projection: Array<String!>?, 
    queryArgs: Bundle!, 
    cancellationSignal: CancellationSignal?
): Cursor?
```

See android.content.ContentProvider#query

| Parameters ||
|----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `uri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#):This value cannot be`null`. |
| `projection` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>?:This value may be`null`. |
| `cancellationSignal` | [CancellationSignal](https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#)?:This value may be`null`. |

| Return ||
|-----------------------------------------------------------------------------------------|--------------------------|
| [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#)? | This value may be`null`. |

### query

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun query(
    url: Uri, 
    projection: Array<String!>?, 
    selection: String?, 
    selectionArgs: Array<String!>?, 
    sortOrder: String?
): Cursor?
```

See android.content.ContentProvider#query

| Parameters ||
|-----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `url` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#):This value cannot be`null`. |
| `projection` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>?:This value may be`null`. |
| `selection` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:This value may be`null`. |
| `selectionArgs` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>?:This value may be`null`. |
| `sortOrder` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:This value may be`null`. |

| Return ||
|-----------------------------------------------------------------------------------------|--------------------------|
| [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#)? | This value may be`null`. |

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

See android.content.ContentProvider#query

| Parameters ||
|----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `uri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#):This value cannot be`null`. |
| `projection` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>?:This value may be`null`. |
| `selection` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:This value may be`null`. |
| `selectionArgs` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>?:This value may be`null`. |
| `sortOrder` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:This value may be`null`. |
| `cancellationSignal` | [CancellationSignal](https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#)?:This value may be`null`. |

| Return ||
|-----------------------------------------------------------------------------------------|--------------------------|
| [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#)? | This value may be`null`. |

### refresh

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun refresh(
    url: Uri!, 
    extras: Bundle?, 
    cancellationSignal: CancellationSignal?
): Boolean
```

See [ContentProvider.refresh](https://developer.android.com/reference/kotlin/android/content/ContentProvider#refresh(android.net.Uri,%20android.os.Bundle,%20android.os.CancellationSignal))

| Parameters ||
|----------------------|------------------------------------------------------------------------------------------------------------------------------------|
| `extras` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)?:This value may be`null`. |
| `cancellationSignal` | [CancellationSignal](https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#)?:This value may be`null`. |

### release

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun release(): Boolean
```

**Deprecated:** *replaced by [close()](https://developer.android.com/reference/kotlin/android/content/ContentProviderClient#close()).* 

### uncanonicalize

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun uncanonicalize(url: Uri): Uri?
```

See [ContentProvider.uncanonicalize](https://developer.android.com/reference/kotlin/android/content/ContentProvider#uncanonicalize(android.net.Uri))

| Parameters ||
|-------|---------------------------------------------------------------------------------------------------------|
| `url` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#):This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------|--------------------------|
| [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)? | This value may be`null`. |

### update

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun update(
    url: Uri, 
    values: ContentValues?, 
    extras: Bundle?
): Int
```

See android.content.ContentProvider#update

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------|
| `url` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#):This value cannot be`null`. |
| `values` | [ContentValues](https://developer.android.com/reference/kotlin/android/content/ContentValues)?:This value may be`null`. |
| `extras` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)?:This value may be`null`. |

### update

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun update(
    url: Uri, 
    values: ContentValues?, 
    selection: String?, 
    selectionArgs: Array<String!>?
): Int
```

See android.content.ContentProvider#update

| Parameters ||
|-----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `url` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#):This value cannot be`null`. |
| `values` | [ContentValues](https://developer.android.com/reference/kotlin/android/content/ContentValues)?:This value may be`null`. |
| `selection` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:This value may be`null`. |
| `selectionArgs` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>?:This value may be`null`. |

## Protected methods

### finalize

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun finalize(): Unit
```

| Exceptions ||
|-----------------------|-------------------------------------|
| `java.lang.Throwable` | the`Exception`raised by this method |
