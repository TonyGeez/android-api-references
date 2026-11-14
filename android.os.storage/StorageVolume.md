# StorageVolume

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# StorageVolume

Kotlin| [Java](https://developer.android.com/reference/android/os/storage/StorageVolume "View this page in Java") 

```
class StorageVolume : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.os.storage.StorageVolume](https://developer.android.com/reference/kotlin/android/os/storage/StorageVolume#) |

Information about a shared/external storage volume for a specific user.

A device always has one (and one only) primary storage volume, but it could have extra volumes, like SD cards and USB drives. This object represents the logical view of a storage volume for a specific user: different users might have different views for the same physical volume (for example, if the volume is a built-in emulated storage).

The storage volume is not necessarily mounted, applications should use [getState()](https://developer.android.com/reference/kotlin/android/os/storage/StorageVolume#getState())to verify its state.

Applications willing to read or write to this storage volume needs to get a permission from the user first, which can be achieved in the following ways:

- To get access to standard directories (like the [Environment.DIRECTORY_PICTURES](https://developer.android.com/reference/kotlin/android/os/Environment.html#DIRECTORY_PICTURES:kotlin.String)), they can use the [createAccessIntent(java.lang.String)](https://developer.android.com/reference/kotlin/android/os/storage/StorageVolume#createAccessIntent(kotlin.String)). This is the recommend way, since it provides a simpler API and narrows the access to the given directory (and its descendants).
- To get access to any directory (and its descendants), they can use the Storage Access Framework APIs (such as [Intent.ACTION_OPEN_DOCUMENT](https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_OPEN_DOCUMENT:kotlin.String) and [Intent.ACTION_OPEN_DOCUMENT_TREE](https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_OPEN_DOCUMENT_TREE:kotlin.String), although these APIs do not guarantee the user will select this specific volume.
- To get read and write access to the primary storage volume, applications can declare the [android.Manifest.permission#READ_EXTERNAL_STORAGE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_EXTERNAL_STORAGE:kotlin.String) and [android.Manifest.permission#WRITE_EXTERNAL_STORAGE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#WRITE_EXTERNAL_STORAGE:kotlin.String) permissions respectively, with the latter including the former. This approach is discouraged, since users may be hesitant to grant broad access to all files contained on a storage device.

It can be obtained through [StorageManager.getStorageVolumes()](https://developer.android.com/reference/kotlin/android/os/storage/StorageManager#getStorageVolumes())and [StorageManager.getPrimaryStorageVolume()](https://developer.android.com/reference/kotlin/android/os/storage/StorageManager#getPrimaryStorageVolume())and also as an extra in some broadcasts (see [EXTRA_STORAGE_VOLUME](https://developer.android.com/reference/kotlin/android/os/storage/StorageVolume#EXTRA_STORAGE_VOLUME:kotlin.String)).

See [Environment.getExternalStorageDirectory()](https://developer.android.com/reference/kotlin/android/os/Environment.html#getExternalStorageDirectory())for more info about shared/external storage semantics.

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_STORAGE_VOLUME](https://developer.android.com/reference/kotlin/android/os/storage/StorageVolume#EXTRA_STORAGE_VOLUME:kotlin.String) Name of the [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) extra in the [Intent.ACTION_MEDIA_REMOVED](https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_MEDIA_REMOVED:kotlin.String), [Intent.ACTION_MEDIA_UNMOUNTED](https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_MEDIA_UNMOUNTED:kotlin.String), [Intent.ACTION_MEDIA_CHECKING](https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_MEDIA_CHECKING:kotlin.String), [Intent.ACTION_MEDIA_NOFS](https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_MEDIA_NOFS:kotlin.String), [Intent.ACTION_MEDIA_MOUNTED](https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_MEDIA_MOUNTED:kotlin.String), [Intent.ACTION_MEDIA_SHARED](https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_MEDIA_SHARED:kotlin.String), [Intent.ACTION_MEDIA_BAD_REMOVAL](https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_MEDIA_BAD_REMOVAL:kotlin.String), [Intent.ACTION_MEDIA_UNMOUNTABLE](https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_MEDIA_UNMOUNTABLE:kotlin.String), and [Intent.ACTION_MEDIA_EJECT](https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_MEDIA_EJECT:kotlin.String) broadcast that contains a [StorageVolume](https://developer.android.com/reference/kotlin/android/os/storage/StorageVolume#). |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#)? | [createAccessIntent](https://developer.android.com/reference/kotlin/android/os/storage/StorageVolume#createAccessIntent(kotlin.String))`(`directoryName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Builds an intent to give access to a standard storage directory or entire volume after obtaining the user's approval. |
| [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#) | [createOpenDocumentTreeIntent](https://developer.android.com/reference/kotlin/android/os/storage/StorageVolume#createOpenDocumentTreeIntent())`()` Builds an [Intent.ACTION_OPEN_DOCUMENT_TREE](https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_OPEN_DOCUMENT_TREE:kotlin.String) to allow the user to grant access to any directory subtree (or entire volume) from the [android.provider.DocumentsProvider](https://developer.android.com/reference/kotlin/android/provider/DocumentsProvider.html#) s available on the device. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/os/storage/StorageVolume#describeContents())`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/os/storage/StorageVolume#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Indicates whether some other object is "equal to" this one. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getDescription](https://developer.android.com/reference/kotlin/android/os/storage/StorageVolume#getDescription(android.content.Context))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`)` Returns a user-visible description of the volume. |
| [File](https://developer.android.com/reference/kotlin/java/io/File.html#)? | [getDirectory](https://developer.android.com/reference/kotlin/android/os/storage/StorageVolume#getDirectory())`()` Returns the directory where this volume is currently mounted. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getMediaStoreVolumeName](https://developer.android.com/reference/kotlin/android/os/storage/StorageVolume#getMediaStoreVolumeName())`()` Return the volume name that can be used to interact with this storage device through [MediaStore](https://developer.android.com/reference/kotlin/android/provider/MediaStore.html#). |
| [UserHandle](https://developer.android.com/reference/kotlin/android/os/UserHandle.html#) | [getOwner](https://developer.android.com/reference/kotlin/android/os/storage/StorageVolume#getOwner())`()` Returns the user that owns this volume |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getState](https://developer.android.com/reference/kotlin/android/os/storage/StorageVolume#getState())`()` Returns the current state of the volume. |
| [UUID](https://developer.android.com/reference/kotlin/java/util/UUID.html#)? | [getStorageUuid](https://developer.android.com/reference/kotlin/android/os/storage/StorageVolume#getStorageUuid())`()` Gets the converted volume UUID. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getUuid](https://developer.android.com/reference/kotlin/android/os/storage/StorageVolume#getUuid())`()` Gets the volume UUID, if any. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/os/storage/StorageVolume#hashCode())`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEmulated](https://developer.android.com/reference/kotlin/android/os/storage/StorageVolume#isEmulated())`()` Returns true if the volume is emulated. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isPrimary](https://developer.android.com/reference/kotlin/android/os/storage/StorageVolume#isPrimary())`()` Returns true if the volume is the primary shared/external storage, which is the volume backed by [Environment.getExternalStorageDirectory()](https://developer.android.com/reference/kotlin/android/os/Environment.html#getExternalStorageDirectory()). |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isRemovable](https://developer.android.com/reference/kotlin/android/os/storage/StorageVolume#isRemovable())`()` Returns true if the volume is removable. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/os/storage/StorageVolume#toString())`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/os/storage/StorageVolume#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`parcel:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Properties ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [StorageVolume](https://developer.android.com/reference/kotlin/android/os/storage/StorageVolume#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/os/storage/StorageVolume#CREATOR:android.os.Parcelable.Creator) <br /> |

## Constants

### EXTRA_STORAGE_VOLUME

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_STORAGE_VOLUME: String
```

Name of the [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) extra in the [Intent.ACTION_MEDIA_REMOVED](https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_MEDIA_REMOVED:kotlin.String), [Intent.ACTION_MEDIA_UNMOUNTED](https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_MEDIA_UNMOUNTED:kotlin.String), [Intent.ACTION_MEDIA_CHECKING](https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_MEDIA_CHECKING:kotlin.String), [Intent.ACTION_MEDIA_NOFS](https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_MEDIA_NOFS:kotlin.String), [Intent.ACTION_MEDIA_MOUNTED](https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_MEDIA_MOUNTED:kotlin.String), [Intent.ACTION_MEDIA_SHARED](https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_MEDIA_SHARED:kotlin.String), [Intent.ACTION_MEDIA_BAD_REMOVAL](https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_MEDIA_BAD_REMOVAL:kotlin.String), [Intent.ACTION_MEDIA_UNMOUNTABLE](https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_MEDIA_UNMOUNTABLE:kotlin.String), and [Intent.ACTION_MEDIA_EJECT](https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_MEDIA_EJECT:kotlin.String) broadcast that contains a [StorageVolume](https://developer.android.com/reference/kotlin/android/os/storage/StorageVolume#). 

 Value: "android.os.storage.extra.STORAGE_VOLUME"

## Public methods

### createAccessIntent

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun createAccessIntent(directoryName: String!): Intent?
```

**Deprecated:** *Callers should migrate to using [Intent.ACTION_OPEN_DOCUMENT_TREE](https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_OPEN_DOCUMENT_TREE:kotlin.String) instead. Launching this [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#) on devices running [android.os.Build.VERSION_CODES#Q](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#Q:kotlin.Int) or higher, will immediately finish with a result code of [android.app.Activity#RESULT_CANCELED](https://developer.android.com/reference/kotlin/android/app/Activity.html#RESULT_CANCELED:kotlin.Int).*

Builds an intent to give access to a standard storage directory or entire volume after obtaining the user's approval.

When invoked, the system will ask the user to grant access to the requested directory (and its descendants). The result of the request will be returned to the activity through the`onActivityResult`method.

To gain access to descendants (child, grandchild, etc) documents, use [DocumentsContract.buildDocumentUriUsingTree(Uri, String)](https://developer.android.com/reference/kotlin/android/provider/DocumentsContract.html#buildDocumentUriUsingTree(android.net.Uri,%20kotlin.String)), or [DocumentsContract.buildChildDocumentsUriUsingTree(Uri, String)](https://developer.android.com/reference/kotlin/android/provider/DocumentsContract.html#buildChildDocumentsUriUsingTree(android.net.Uri,%20kotlin.String))with the returned URI.

If your application only needs to store internal data, consider using [Context.getExternalFilesDirs](https://developer.android.com/reference/kotlin/android/content/Context.html#getExternalFilesDirs(kotlin.String)), [Context.getExternalCacheDirs()](https://developer.android.com/reference/kotlin/android/content/Context.html#getExternalCacheDirs()), or [Context.getExternalMediaDirs()](https://developer.android.com/reference/kotlin/android/content/Context.html#getExternalMediaDirs()), which require no permissions to read or write.

Access to the entire volume is only available for non-primary volumes (for the primary volume, apps can use the [android.Manifest.permission#READ_EXTERNAL_STORAGE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_EXTERNAL_STORAGE:kotlin.String) and [android.Manifest.permission#WRITE_EXTERNAL_STORAGE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#WRITE_EXTERNAL_STORAGE:kotlin.String) permissions) and should be used with caution, since users are more likely to deny access when asked for entire volume access rather than specific directories.

| Parameters ||
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `directoryName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:must be one of [Environment.DIRECTORY_MUSIC](https://developer.android.com/reference/kotlin/android/os/Environment.html#DIRECTORY_MUSIC:kotlin.String), [Environment.DIRECTORY_PODCASTS](https://developer.android.com/reference/kotlin/android/os/Environment.html#DIRECTORY_PODCASTS:kotlin.String), [Environment.DIRECTORY_RINGTONES](https://developer.android.com/reference/kotlin/android/os/Environment.html#DIRECTORY_RINGTONES:kotlin.String), [Environment.DIRECTORY_ALARMS](https://developer.android.com/reference/kotlin/android/os/Environment.html#DIRECTORY_ALARMS:kotlin.String), [Environment.DIRECTORY_NOTIFICATIONS](https://developer.android.com/reference/kotlin/android/os/Environment.html#DIRECTORY_NOTIFICATIONS:kotlin.String), [Environment.DIRECTORY_PICTURES](https://developer.android.com/reference/kotlin/android/os/Environment.html#DIRECTORY_PICTURES:kotlin.String), [Environment.DIRECTORY_MOVIES](https://developer.android.com/reference/kotlin/android/os/Environment.html#DIRECTORY_MOVIES:kotlin.String), [Environment.DIRECTORY_DOWNLOADS](https://developer.android.com/reference/kotlin/android/os/Environment.html#DIRECTORY_DOWNLOADS:kotlin.String), [Environment.DIRECTORY_DCIM](https://developer.android.com/reference/kotlin/android/os/Environment.html#DIRECTORY_DCIM:kotlin.String), or [Environment.DIRECTORY_DOCUMENTS](https://developer.android.com/reference/kotlin/android/os/Environment.html#DIRECTORY_DOCUMENTS:kotlin.String), or`null`to request access to the entire volume. |

| Return ||
|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#)? | intent to request access, or`null`if the requested directory is invalid for that volume. |

**See Also**

- [android.provider.DocumentsContract](https://developer.android.com/reference/kotlin/android/provider/DocumentsContract.html#) 

### createOpenDocumentTreeIntent

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun createOpenDocumentTreeIntent(): Intent
```

Builds an [Intent.ACTION_OPEN_DOCUMENT_TREE](https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_OPEN_DOCUMENT_TREE:kotlin.String) to allow the user to grant access to any directory subtree (or entire volume) from the [android.provider.DocumentsProvider](https://developer.android.com/reference/kotlin/android/provider/DocumentsProvider.html#) s available on the device. The initial location of the document navigation will be the root of this [StorageVolume](https://developer.android.com/reference/kotlin/android/os/storage/StorageVolume#). Note that the returned [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#) simply suggests that the user picks this [StorageVolume](https://developer.android.com/reference/kotlin/android/os/storage/StorageVolume#) by default, but the user may select a different location. Callers must respect the user's chosen location, even if it is different from the originally requested location.

| Return ||
|---------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#) | intent to [Intent.ACTION_OPEN_DOCUMENT_TREE](https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_OPEN_DOCUMENT_TREE:kotlin.String) initially showing the contents of this [StorageVolume](https://developer.android.com/reference/kotlin/android/os/storage/StorageVolume#) This value cannot be`null`. |

**See Also**

- [android.content.Intent#ACTION_OPEN_DOCUMENT_TREE](https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_OPEN_DOCUMENT_TREE:kotlin.String) 

### describeContents

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### equals

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

Indicates whether some other object is "equal to" this one.

The`equals`method implements an equivalence relation on non-null object references:

- It is*reflexive* : for any non-null reference value`x`,`x.equals(x)`should return`true`.
- It is*symmetric* : for any non-null reference values`x`and`y`,`x.equals(y)`should return`true`if and only if`y.equals(x)`returns`true`.
- It is*transitive* : for any non-null reference values`x`,`y`, and`z`, if`x.equals(y)`returns`true`and`y.equals(z)`returns`true`, then`x.equals(z)`should return`true`.
- It is*consistent* : for any non-null reference values`x`and`y`, multiple invocations of`x.equals(y)`consistently return`true`or consistently return`false`, provided no information used in`equals`comparisons on the objects is modified.
- For any non-null reference value`x`,`x.equals(null)`should return`false`.

An equivalence relation partitions the elements it operates on into*equivalence classes*; all the members of an equivalence class are equal to each other. Members of an equivalence class are substitutable for each other, at least for some purposes.

| Parameters ||
|-------|--------------------------|
| `obj` | This value may be`null`. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

### getDescription

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDescription(context: Context!): String!
```

Returns a user-visible description of the volume.

| Return ||
|-----------------------------------------------------------------------------------|------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the volume description |

### getDirectory

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDirectory(): File?
```

Returns the directory where this volume is currently mounted.

Direct filesystem access via this path has significant emulation overhead, and apps are instead strongly encouraged to interact with media on storage volumes via the [MediaStore](https://developer.android.com/reference/kotlin/android/provider/MediaStore.html#) APIs.

This directory does not give apps any additional access beyond what they already have via [MediaStore](https://developer.android.com/reference/kotlin/android/provider/MediaStore.html#).

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [File](https://developer.android.com/reference/kotlin/java/io/File.html#)? | directory where this volume is mounted, or`null`if the volume is not currently mounted. |

### getMediaStoreVolumeName

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMediaStoreVolumeName(): String?
```

Return the volume name that can be used to interact with this storage device through [MediaStore](https://developer.android.com/reference/kotlin/android/provider/MediaStore.html#).

| Return ||
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | opaque volume name, or`null`if this volume is not indexed by [MediaStore](https://developer.android.com/reference/kotlin/android/provider/MediaStore.html#). |

**See Also**

- [android.provider.MediaStore.Audio.Media#getContentUri(String)](https://developer.android.com/reference/kotlin/android/provider/MediaStore.Audio.Media.html#getContentUri(kotlin.String))
- [android.provider.MediaStore.Video.Media#getContentUri(String)](https://developer.android.com/reference/kotlin/android/provider/MediaStore.Video.Media.html#getContentUri(kotlin.String))
- [android.provider.MediaStore.Images.Media#getContentUri(String)](https://developer.android.com/reference/kotlin/android/provider/MediaStore.Images.Media.html#getContentUri(kotlin.String)) 

### getOwner

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getOwner(): UserHandle
```

Returns the user that owns this volume

| Return ||
|------------------------------------------------------------------------------------------|-----------------------------|
| [UserHandle](https://developer.android.com/reference/kotlin/android/os/UserHandle.html#) | This value cannot be`null`. |

### getState

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getState(): String!
```

Returns the current state of the volume.

| Return ||
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | one of [Environment.MEDIA_UNKNOWN](https://developer.android.com/reference/kotlin/android/os/Environment.html#MEDIA_UNKNOWN:kotlin.String), [Environment.MEDIA_REMOVED](https://developer.android.com/reference/kotlin/android/os/Environment.html#MEDIA_REMOVED:kotlin.String), [Environment.MEDIA_UNMOUNTED](https://developer.android.com/reference/kotlin/android/os/Environment.html#MEDIA_UNMOUNTED:kotlin.String), [Environment.MEDIA_CHECKING](https://developer.android.com/reference/kotlin/android/os/Environment.html#MEDIA_CHECKING:kotlin.String), [Environment.MEDIA_NOFS](https://developer.android.com/reference/kotlin/android/os/Environment.html#MEDIA_NOFS:kotlin.String), [Environment.MEDIA_MOUNTED](https://developer.android.com/reference/kotlin/android/os/Environment.html#MEDIA_MOUNTED:kotlin.String), [Environment.MEDIA_MOUNTED_READ_ONLY](https://developer.android.com/reference/kotlin/android/os/Environment.html#MEDIA_MOUNTED_READ_ONLY:kotlin.String), [Environment.MEDIA_SHARED](https://developer.android.com/reference/kotlin/android/os/Environment.html#MEDIA_SHARED:kotlin.String), [Environment.MEDIA_BAD_REMOVAL](https://developer.android.com/reference/kotlin/android/os/Environment.html#MEDIA_BAD_REMOVAL:kotlin.String), or [Environment.MEDIA_UNMOUNTABLE](https://developer.android.com/reference/kotlin/android/os/Environment.html#MEDIA_UNMOUNTABLE:kotlin.String). |

### getStorageUuid

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getStorageUuid(): UUID?
```

Gets the converted volume UUID. If a valid UUID is returned, it is compatible with other APIs that make use of [UUID](https://developer.android.com/reference/kotlin/java/util/UUID.html#) like android.os.storage.StorageManager#allocateBytes and [android.content.pm.ApplicationInfo#storageUuid](https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo.html#storageUuid:java.util.UUID)

| Return ||
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [UUID](https://developer.android.com/reference/kotlin/java/util/UUID.html#)? | the UUID for the volume or`null`for "portable" storage devices which haven't been adopted. |

**See Also**

### getUuid

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getUuid(): String?
```

Gets the volume UUID, if any.

| Return ||
|-----------------------------------------------------------------------------------|--------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | This value may be`null`. |

### hashCode

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### isEmulated

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isEmulated(): Boolean
```

Returns true if the volume is emulated.

| Return ||
|------------------------------------------------------------------------------------|-------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | is emulated |

### isPrimary

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isPrimary(): Boolean
```

Returns true if the volume is the primary shared/external storage, which is the volume backed by [Environment.getExternalStorageDirectory()](https://developer.android.com/reference/kotlin/android/os/Environment.html#getExternalStorageDirectory()). 

### isRemovable

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isRemovable(): Boolean
```

Returns true if the volume is removable.

| Return ||
|------------------------------------------------------------------------------------|--------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | is removable |

### toString

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

### writeToParcel

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun writeToParcel(
    parcel: Parcel, 
    flags: Int
): Unit
```

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<StorageVolume!>
```
