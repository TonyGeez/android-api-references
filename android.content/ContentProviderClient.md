# ContentProviderClient

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ContentProviderClient

Kotlin| [Java](ContentProviderClient.md) 
| --- | --- |

```
open class ContentProviderClient : AutoCloseable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.content.ContentProviderClient](ContentProviderClient.md) |

The public interface object used to interact with a specific [ContentProvider](ContentProvider.md).

Instances can be obtained by calling android.content.ContentResolver#acquireContentProviderClient or android.content.ContentResolver#acquireUnstableContentProviderClient. Instances must be released using [close()](ContentProviderClient.md))in order to indicate to the system that the underlying [ContentProvider](ContentProvider.md) is no longer needed and can be killed to free up resources.

Note that you should generally create a new ContentProviderClient instance for each thread that will be performing operations. Unlike [ContentResolver](ContentResolver.md), the methods here such as #query and #openFile are not thread safe -- you must not call [close()](ContentProviderClient.md))on the ContentProviderClient those calls are made from until you are finished with the data they have returned.

## Summary

| Public methods ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [ContentProviderResult](ContentProviderResult.md)!\> | [applyBatch](ContentProviderClient.md))`(`authority:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `operations:` ` [ArrayList](../java.util/ArrayList.md)< [ContentProviderOperation](ContentProviderOperation.md)!>`)` See android. |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [ContentProviderResult](ContentProviderResult.md)!\> | [applyBatch](ContentProviderClient.md))`(`operations:` ` [ArrayList](../java.util/ArrayList.md)< [ContentProviderOperation](ContentProviderOperation.md)!>`)` See android. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [bulkInsert](ContentProviderClient.md))`(`url:` ` [Uri](../android.net/Uri.md)`, `initialValues:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [ContentValues](ContentValues.md)!>`)` See [ContentProvider.bulkInsert](ContentProvider.md)) |
| --- | --- |
| open [Bundle](../android.os/Bundle.md)? | [call](ContentProviderClient.md))`(`method:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `arg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `extras:` ` [Bundle](../android.os/Bundle.md)?`)` See [ContentProvider.call(String, String, Bundle)](ContentProvider.md)) |
| open [Bundle](../android.os/Bundle.md)? | [call](ContentProviderClient.md))`(`authority:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `method:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `arg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `extras:` ` [Bundle](../android.os/Bundle.md)?`)` See [ContentProvider.call(String, String, Bundle)](ContentProvider.md)) |
| [Uri](../android.net/Uri.md)? | [canonicalize](ContentProviderClient.md))`(`url:` ` [Uri](../android.net/Uri.md)`)` See [ContentProvider.canonicalize](ContentProvider.md)) |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](ContentProviderClient.md))`()` Closes this client connection, indicating to the system that the underlying [ContentProvider](ContentProvider.md) is no longer needed. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [delete](ContentProviderClient.md))`(`url:` ` [Uri](../android.net/Uri.md)`, `extras:` ` [Bundle](../android.os/Bundle.md)?`)` See android. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [delete](ContentProviderClient.md))`(`url:` ` [Uri](../android.net/Uri.md)`, `selection:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `selectionArgs:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>?`)` See android. |
| --- | --- |
| open [ContentProvider](ContentProvider.md)? | [getLocalContentProvider](ContentProviderClient.md))`()` Get a reference to the [ContentProvider](ContentProvider.md) that is associated with this client. |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>? | [getStreamTypes](ContentProviderClient.md))`(`url:` ` [Uri](../android.net/Uri.md)`, `mimeTypeFilter:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` See [ContentProvider.getStreamTypes](ContentProvider.md)) |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getType](ContentProviderClient.md))`(`url:` ` [Uri](../android.net/Uri.md)`)` See [ContentProvider.getType](ContentProvider.md)) |
| --- | --- |
| open [Uri](../android.net/Uri.md)? | [insert](ContentProviderClient.md))`(`url:` ` [Uri](../android.net/Uri.md)`, `initialValues:` ` [ContentValues](ContentValues.md)?`)` See android. |
| open [Uri](../android.net/Uri.md)? | [insert](ContentProviderClient.md))`(`url:` ` [Uri](../android.net/Uri.md)`, `initialValues:` ` [ContentValues](ContentValues.md)?`, `extras:` ` [Bundle](../android.os/Bundle.md)?`)` See android. |
| open [AssetFileDescriptor](../android.content.res/AssetFileDescriptor.md)? | [openAssetFile](ContentProviderClient.md))`(`url:` ` [Uri](../android.net/Uri.md)`, `mode:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` See android. |
| --- | --- |
| open [AssetFileDescriptor](../android.content.res/AssetFileDescriptor.md)? | [openAssetFile](ContentProviderClient.md))`(`url:` ` [Uri](../android.net/Uri.md)`, `mode:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `signal:` ` [CancellationSignal](../android.os/CancellationSignal.md)?`)` See android. |
| open [ParcelFileDescriptor](../android.os/ParcelFileDescriptor.md)? | [openFile](ContentProviderClient.md))`(`url:` ` [Uri](../android.net/Uri.md)`, `mode:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` See android. |
| open [ParcelFileDescriptor](../android.os/ParcelFileDescriptor.md)? | [openFile](ContentProviderClient.md))`(`url:` ` [Uri](../android.net/Uri.md)`, `mode:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `signal:` ` [CancellationSignal](../android.os/CancellationSignal.md)?`)` See android. |
| --- | --- |
| [AssetFileDescriptor](../android.content.res/AssetFileDescriptor.md)? | [openTypedAssetFile](ContentProviderClient.md))`(`uri:` ` [Uri](../android.net/Uri.md)`, `mimeTypeFilter:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `opts:` ` [Bundle](../android.os/Bundle.md)?`, `signal:` ` [CancellationSignal](../android.os/CancellationSignal.md)?`)` <br /> |
| [AssetFileDescriptor](../android.content.res/AssetFileDescriptor.md)? | [openTypedAssetFileDescriptor](ContentProviderClient.md))`(`uri:` ` [Uri](../android.net/Uri.md)`, `mimeType:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `opts:` ` [Bundle](../android.os/Bundle.md)?`)` See android. |
| [AssetFileDescriptor](../android.content.res/AssetFileDescriptor.md)? | [openTypedAssetFileDescriptor](ContentProviderClient.md))`(`uri:` ` [Uri](../android.net/Uri.md)`, `mimeType:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `opts:` ` [Bundle](../android.os/Bundle.md)?`, `signal:` ` [CancellationSignal](../android.os/CancellationSignal.md)?`)` See android. |
| --- | --- |
| open [Cursor](../android.database/Cursor.md)? | [query](ContentProviderClient.md))`(`uri:` ` [Uri](../android.net/Uri.md)`, `projection:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>?`, `queryArgs:` ` [Bundle](../android.os/Bundle.md)!`, `cancellationSignal:` ` [CancellationSignal](../android.os/CancellationSignal.md)?`)` See android. |
| open [Cursor](../android.database/Cursor.md)? | [query](ContentProviderClient.md))`(`url:` ` [Uri](../android.net/Uri.md)`, `projection:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>?`, `selection:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `selectionArgs:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>?`, `sortOrder:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` See android. |
| open [Cursor](../android.database/Cursor.md)? | [query](ContentProviderClient.md))`(`uri:` ` [Uri](../android.net/Uri.md)`, `projection:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>?`, `selection:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `selectionArgs:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>?`, `sortOrder:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `cancellationSignal:` ` [CancellationSignal](../android.os/CancellationSignal.md)?`)` See android. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [refresh](ContentProviderClient.md))`(`url:` ` [Uri](../android.net/Uri.md)!`, `extras:` ` [Bundle](../android.os/Bundle.md)?`, `cancellationSignal:` ` [CancellationSignal](../android.os/CancellationSignal.md)?`)` See [ContentProvider.refresh](ContentProvider.md)) |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [release](ContentProviderClient.md))`()` <br /> |
| [Uri](../android.net/Uri.md)? | [uncanonicalize](ContentProviderClient.md))`(`url:` ` [Uri](../android.net/Uri.md)`)` See [ContentProvider.uncanonicalize](ContentProvider.md)) |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [update](ContentProviderClient.md))`(`url:` ` [Uri](../android.net/Uri.md)`, `values:` ` [ContentValues](ContentValues.md)?`, `extras:` ` [Bundle](../android.os/Bundle.md)?`)` See android. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [update](ContentProviderClient.md))`(`url:` ` [Uri](../android.net/Uri.md)`, `values:` ` [ContentValues](ContentValues.md)?`, `selection:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `selectionArgs:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>?`)` See android. |

| Protected methods ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finalize](ContentProviderClient.md))`()` <br /> |

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
| `operations` | [ArrayList](../java.util/ArrayList.md)\< [ContentProviderOperation](ContentProviderOperation.md)!\>:This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [ContentProviderResult](ContentProviderResult.md)!> | This value cannot be`null`. |

### applyBatch

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun applyBatch(operations: ArrayList<ContentProviderOperation!>): Array<ContentProviderResult!>
```

See android.content.ContentProvider#applyBatch

| Parameters ||
|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `operations` | [ArrayList](../java.util/ArrayList.md)\< [ContentProviderOperation](ContentProviderOperation.md)!\>:This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [ContentProviderResult](ContentProviderResult.md)!> | This value cannot be`null`. |

### bulkInsert

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun bulkInsert(
    url: Uri, 
    initialValues: Array<ContentValues!>
): Int
```

See [ContentProvider.bulkInsert](ContentProvider.md))

| Parameters ||
|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `url` | [Uri](../android.net/Uri.md):This value cannot be`null`. |
| `initialValues` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [ContentValues](ContentValues.md)!\>:This value cannot be`null`. |

### call

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun call(
    method: String, 
    arg: String?, 
    extras: Bundle?
): Bundle?
```

See [ContentProvider.call(String, String, Bundle)](ContentProvider.md))

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------|
| `method` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):This value cannot be`null`. |
| `arg` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:This value may be`null`. |
| `extras` | [Bundle](../android.os/Bundle.md)?:This value may be`null`. |
| --- | --- |

| Return ||
|-----------------------------------------------------------------------------------|--------------------------|
| [Bundle](../android.os/Bundle.md)? | This value may be`null`. |

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

See [ContentProvider.call(String, String, Bundle)](ContentProvider.md))

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------------------|
| `authority` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):This value cannot be`null`. |
| `method` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):This value cannot be`null`. |
| `arg` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:This value may be`null`. |
| --- | --- |
| `extras` | [Bundle](../android.os/Bundle.md)?:This value may be`null`. |

| Return ||
|-----------------------------------------------------------------------------------|--------------------------|
| [Bundle](../android.os/Bundle.md)? | This value may be`null`. |

### canonicalize

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun canonicalize(url: Uri): Uri?
```

See [ContentProvider.canonicalize](ContentProvider.md))

| Parameters ||
|-------|---------------------------------------------------------------------------------------------------------|
| `url` | [Uri](../android.net/Uri.md):This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------|--------------------------|
| [Uri](../android.net/Uri.md)? | This value may be`null`. |

### close

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun close(): Unit
```

Closes this client connection, indicating to the system that the underlying [ContentProvider](ContentProvider.md) is no longer needed.

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
| `url` | [Uri](../android.net/Uri.md):This value cannot be`null`. |
| `extras` | [Bundle](../android.os/Bundle.md)?:This value may be`null`. |

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
| `url` | [Uri](../android.net/Uri.md):This value cannot be`null`. |
| `selection` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:This value may be`null`. |
| `selectionArgs` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>?:This value may be`null`. |
| --- | --- |

### getLocalContentProvider

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getLocalContentProvider(): ContentProvider?
```

Get a reference to the [ContentProvider](ContentProvider.md) that is associated with this client. If the [ContentProvider](ContentProvider.md) is running in a different process then null will be returned. This can be used if you know you are running in the same process as a provider, and want to get direct access to its implementation details.

| Return ||
|----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ContentProvider](ContentProvider.md)? | If the associated [ContentProvider](ContentProvider.md) is local, returns it. Otherwise returns null. |

### getStreamTypes

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getStreamTypes(
    url: Uri, 
    mimeTypeFilter: String
): Array<String!>?
```

See [ContentProvider.getStreamTypes](ContentProvider.md))

| Parameters ||
|------------------|--------------------------------------------------------------------------------------------------------------|
| `url` | [Uri](../android.net/Uri.md):This value cannot be`null`. |
| `mimeTypeFilter` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):This value cannot be`null`. |

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>? | This value may be`null`. |

### getType

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getType(url: Uri): String?
```

See [ContentProvider.getType](ContentProvider.md))

| Parameters ||
|-------|---------------------------------------------------------------------------------------------------------|
| `url` | [Uri](../android.net/Uri.md):This value cannot be`null`. |

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
| `url` | [Uri](../android.net/Uri.md):This value cannot be`null`. |
| `initialValues` | [ContentValues](ContentValues.md)?:This value may be`null`. |

| Return ||
|------------------------------------------------------------------------------|--------------------------|
| [Uri](../android.net/Uri.md)? | This value may be`null`. |

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
| `url` | [Uri](../android.net/Uri.md):This value cannot be`null`. |
| `initialValues` | [ContentValues](ContentValues.md)?:This value may be`null`. |
| `extras` | [Bundle](../android.os/Bundle.md)?:This value may be`null`. |
| --- | --- |

| Return ||
|------------------------------------------------------------------------------|--------------------------|
| [Uri](../android.net/Uri.md)? | This value may be`null`. |

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
| `url` | [Uri](../android.net/Uri.md):This value cannot be`null`. |
| `mode` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):This value cannot be`null`. |

| Return ||
|----------------------------------------------------------------------------------------------------------------|--------------------------|
| [AssetFileDescriptor](../android.content.res/AssetFileDescriptor.md)? | This value may be`null`. |

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
| `url` | [Uri](../android.net/Uri.md):This value cannot be`null`. |
| `mode` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):This value cannot be`null`. |
| `signal` | [CancellationSignal](../android.os/CancellationSignal.md)?:This value may be`null`. |
| --- | --- |

| Return ||
|----------------------------------------------------------------------------------------------------------------|--------------------------|
| [AssetFileDescriptor](../android.content.res/AssetFileDescriptor.md)? | This value may be`null`. |

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
| `url` | [Uri](../android.net/Uri.md):This value cannot be`null`. |
| `mode` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):This value cannot be`null`. |

| Return ||
|---------------------------------------------------------------------------------------------------------------|--------------------------|
| [ParcelFileDescriptor](../android.os/ParcelFileDescriptor.md)? | This value may be`null`. |

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
| `url` | [Uri](../android.net/Uri.md):This value cannot be`null`. |
| `mode` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):This value cannot be`null`. |
| `signal` | [CancellationSignal](../android.os/CancellationSignal.md)?:This value may be`null`. |
| --- | --- |

| Return ||
|---------------------------------------------------------------------------------------------------------------|--------------------------|
| [ParcelFileDescriptor](../android.os/ParcelFileDescriptor.md)? | This value may be`null`. |

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
| `uri` | [Uri](../android.net/Uri.md):This value cannot be`null`. |
| `mimeTypeFilter` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):This value cannot be`null`. |
| `opts` | [Bundle](../android.os/Bundle.md)?:This value may be`null`. |
| --- | --- |
| `signal` | [CancellationSignal](../android.os/CancellationSignal.md)?:This value may be`null`. |

| Return ||
|----------------------------------------------------------------------------------------------------------------|--------------------------|
| [AssetFileDescriptor](../android.content.res/AssetFileDescriptor.md)? | This value may be`null`. |

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
| `uri` | [Uri](../android.net/Uri.md):This value cannot be`null`. |
| `mimeType` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):This value cannot be`null`. |
| `opts` | [Bundle](../android.os/Bundle.md)?:This value may be`null`. |
| --- | --- |

| Return ||
|----------------------------------------------------------------------------------------------------------------|--------------------------|
| [AssetFileDescriptor](../android.content.res/AssetFileDescriptor.md)? | This value may be`null`. |

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
| `uri` | [Uri](../android.net/Uri.md):This value cannot be`null`. |
| `mimeType` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):This value cannot be`null`. |
| `opts` | [Bundle](../android.os/Bundle.md)?:This value may be`null`. |
| --- | --- |
| `signal` | [CancellationSignal](../android.os/CancellationSignal.md)?:This value may be`null`. |

| Return ||
|----------------------------------------------------------------------------------------------------------------|--------------------------|
| [AssetFileDescriptor](../android.content.res/AssetFileDescriptor.md)? | This value may be`null`. |

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
| `uri` | [Uri](../android.net/Uri.md):This value cannot be`null`. |
| `projection` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>?:This value may be`null`. |
| `cancellationSignal` | [CancellationSignal](../android.os/CancellationSignal.md)?:This value may be`null`. |
| --- | --- |

| Return ||
|-----------------------------------------------------------------------------------------|--------------------------|
| [Cursor](../android.database/Cursor.md)? | This value may be`null`. |

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
| `url` | [Uri](../android.net/Uri.md):This value cannot be`null`. |
| `projection` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>?:This value may be`null`. |
| `selection` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:This value may be`null`. |
| --- | --- |
| `selectionArgs` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>?:This value may be`null`. |
| `sortOrder` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:This value may be`null`. |

| Return ||
|-----------------------------------------------------------------------------------------|--------------------------|
| [Cursor](../android.database/Cursor.md)? | This value may be`null`. |

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
| `uri` | [Uri](../android.net/Uri.md):This value cannot be`null`. |
| `projection` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>?:This value may be`null`. |
| `selection` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:This value may be`null`. |
| --- | --- |
| `selectionArgs` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>?:This value may be`null`. |
| `sortOrder` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:This value may be`null`. |
| `cancellationSignal` | [CancellationSignal](../android.os/CancellationSignal.md)?:This value may be`null`. |
| --- | --- |

| Return ||
|-----------------------------------------------------------------------------------------|--------------------------|
| [Cursor](../android.database/Cursor.md)? | This value may be`null`. |

### refresh

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun refresh(
    url: Uri!, 
    extras: Bundle?, 
    cancellationSignal: CancellationSignal?
): Boolean
```

See [ContentProvider.refresh](ContentProvider.md))

| Parameters ||
|----------------------|------------------------------------------------------------------------------------------------------------------------------------|
| `extras` | [Bundle](../android.os/Bundle.md)?:This value may be`null`. |
| `cancellationSignal` | [CancellationSignal](../android.os/CancellationSignal.md)?:This value may be`null`. |

### release

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun release(): Boolean
```

**Deprecated:** *replaced by [close()](ContentProviderClient.md)).* 

### uncanonicalize

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun uncanonicalize(url: Uri): Uri?
```

See [ContentProvider.uncanonicalize](ContentProvider.md))

| Parameters ||
|-------|---------------------------------------------------------------------------------------------------------|
| `url` | [Uri](../android.net/Uri.md):This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------|--------------------------|
| [Uri](../android.net/Uri.md)? | This value may be`null`. |

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
| `url` | [Uri](../android.net/Uri.md):This value cannot be`null`. |
| `values` | [ContentValues](ContentValues.md)?:This value may be`null`. |
| `extras` | [Bundle](../android.os/Bundle.md)?:This value may be`null`. |
| --- | --- |

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
| `url` | [Uri](../android.net/Uri.md):This value cannot be`null`. |
| `values` | [ContentValues](ContentValues.md)?:This value may be`null`. |
| `selection` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:This value may be`null`. |
| --- | --- |
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
