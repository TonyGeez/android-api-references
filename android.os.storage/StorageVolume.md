# StorageVolume

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# StorageVolume

Kotlin| [Java](../android/os/storage/StorageVolume.md) 
| --- | --- |

```
class StorageVolume : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.os.storage.StorageVolume](../android/os/storage/StorageVolume.md) |

Information about a shared/external storage volume for a specific user.

A device always has one (and one only) primary storage volume, but it could have extra volumes, like SD cards and USB drives. This object represents the logical view of a storage volume for a specific user: different users might have different views for the same physical volume (for example, if the volume is a built-in emulated storage).

The storage volume is not necessarily mounted, applications should use [getState()](../android/os/storage/StorageVolume.md))to verify its state.

Applications willing to read or write to this storage volume needs to get a permission from the user first, which can be achieved in the following ways:

- To get access to standard directories (like the [Environment.DIRECTORY_PICTURES](../android/os/Environment.md)), they can use the [createAccessIntent(java.lang.String)](../android/os/storage/StorageVolume.md)). This is the recommend way, since it provides a simpler API and narrows the access to the given directory (and its descendants).
- To get access to any directory (and its descendants), they can use the Storage Access Framework APIs (such as [Intent.ACTION_OPEN_DOCUMENT](../android/content/Intent.md) and [Intent.ACTION_OPEN_DOCUMENT_TREE](../android/content/Intent.md), although these APIs do not guarantee the user will select this specific volume.
- To get read and write access to the primary storage volume, applications can declare the [android.Manifest.permission#READ_EXTERNAL_STORAGE](../android/Manifest.permission.md) and [android.Manifest.permission#WRITE_EXTERNAL_STORAGE](../android/Manifest.permission.md) permissions respectively, with the latter including the former. This approach is discouraged, since users may be hesitant to grant broad access to all files contained on a storage device.

It can be obtained through [StorageManager.getStorageVolumes()](../android/os/storage/StorageManager.md))and [StorageManager.getPrimaryStorageVolume()](../android/os/storage/StorageManager.md))and also as an extra in some broadcasts (see [EXTRA_STORAGE_VOLUME](../android/os/storage/StorageVolume.md)).

See [Environment.getExternalStorageDirectory()](../android/os/Environment.md))for more info about shared/external storage semantics.

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_STORAGE_VOLUME](../android/os/storage/StorageVolume.md) Name of the [Parcelable](../android/os/Parcelable.md) extra in the [Intent.ACTION_MEDIA_REMOVED](../android/content/Intent.md), [Intent.ACTION_MEDIA_UNMOUNTED](../android/content/Intent.md), [Intent.ACTION_MEDIA_CHECKING](../android/content/Intent.md), [Intent.ACTION_MEDIA_NOFS](../android/content/Intent.md), [Intent.ACTION_MEDIA_MOUNTED](../android/content/Intent.md), [Intent.ACTION_MEDIA_SHARED](../android/content/Intent.md), [Intent.ACTION_MEDIA_BAD_REMOVAL](../android/content/Intent.md), [Intent.ACTION_MEDIA_UNMOUNTABLE](../android/content/Intent.md), and [Intent.ACTION_MEDIA_EJECT](../android/content/Intent.md) broadcast that contains a [StorageVolume](../android/os/storage/StorageVolume.md). |

| Inherited constants ||
|---|---|
| From class [Parcelable](../android/os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android/os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android/os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Intent](../android/content/Intent.md)? | [createAccessIntent](../android/os/storage/StorageVolume.md))`(`directoryName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Builds an intent to give access to a standard storage directory or entire volume after obtaining the user's approval. |
| [Intent](../android/content/Intent.md) | [createOpenDocumentTreeIntent](../android/os/storage/StorageVolume.md))`()` Builds an [Intent.ACTION_OPEN_DOCUMENT_TREE](../android/content/Intent.md) to allow the user to grant access to any directory subtree (or entire volume) from the [android.provider.DocumentsProvider](../android/provider/DocumentsProvider.md) s available on the device. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](../android/os/storage/StorageVolume.md))`()` <br /> |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](../android/os/storage/StorageVolume.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Indicates whether some other object is "equal to" this one. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getDescription](../android/os/storage/StorageVolume.md))`(`context:` ` [Context](../android/content/Context.md)!`)` Returns a user-visible description of the volume. |
| [File](../java/io/File.md)? | [getDirectory](../android/os/storage/StorageVolume.md))`()` Returns the directory where this volume is currently mounted. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getMediaStoreVolumeName](../android/os/storage/StorageVolume.md))`()` Return the volume name that can be used to interact with this storage device through [MediaStore](../android/provider/MediaStore.md). |
| [UserHandle](../android/os/UserHandle.md) | [getOwner](../android/os/storage/StorageVolume.md))`()` Returns the user that owns this volume |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getState](../android/os/storage/StorageVolume.md))`()` Returns the current state of the volume. |
| --- | --- |
| [UUID](../java/util/UUID.md)? | [getStorageUuid](../android/os/storage/StorageVolume.md))`()` Gets the converted volume UUID. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getUuid](../android/os/storage/StorageVolume.md))`()` Gets the volume UUID, if any. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](../android/os/storage/StorageVolume.md))`()` <br /> |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEmulated](../android/os/storage/StorageVolume.md))`()` Returns true if the volume is emulated. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isPrimary](../android/os/storage/StorageVolume.md))`()` Returns true if the volume is the primary shared/external storage, which is the volume backed by [Environment.getExternalStorageDirectory()](../android/os/Environment.md)). |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isRemovable](../android/os/storage/StorageVolume.md))`()` Returns true if the volume is removable. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../android/os/storage/StorageVolume.md))`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](../android/os/storage/StorageVolume.md))`(`parcel:` ` [Parcel](../android/os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Properties ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [StorageVolume](../android/os/storage/StorageVolume.md)!\> | [CREATOR](../android/os/storage/StorageVolume.md) <br /> |

## Constants

### EXTRA_STORAGE_VOLUME

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_STORAGE_VOLUME: String
```

Name of the [Parcelable](../android/os/Parcelable.md) extra in the [Intent.ACTION_MEDIA_REMOVED](../android/content/Intent.md), [Intent.ACTION_MEDIA_UNMOUNTED](../android/content/Intent.md), [Intent.ACTION_MEDIA_CHECKING](../android/content/Intent.md), [Intent.ACTION_MEDIA_NOFS](../android/content/Intent.md), [Intent.ACTION_MEDIA_MOUNTED](../android/content/Intent.md), [Intent.ACTION_MEDIA_SHARED](../android/content/Intent.md), [Intent.ACTION_MEDIA_BAD_REMOVAL](../android/content/Intent.md), [Intent.ACTION_MEDIA_UNMOUNTABLE](../android/content/Intent.md), and [Intent.ACTION_MEDIA_EJECT](../android/content/Intent.md) broadcast that contains a [StorageVolume](../android/os/storage/StorageVolume.md). 

 Value: "android.os.storage.extra.STORAGE_VOLUME"

## Public methods

### createAccessIntent

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun createAccessIntent(directoryName: String!): Intent?
```

**Deprecated:** *Callers should migrate to using [Intent.ACTION_OPEN_DOCUMENT_TREE](../android/content/Intent.md) instead. Launching this [Intent](../android/content/Intent.md) on devices running [android.os.Build.VERSION_CODES#Q](../android/os/Build.VERSION_CODES.md) or higher, will immediately finish with a result code of [android.app.Activity#RESULT_CANCELED](../android/app/Activity.md).*

Builds an intent to give access to a standard storage directory or entire volume after obtaining the user's approval.

When invoked, the system will ask the user to grant access to the requested directory (and its descendants). The result of the request will be returned to the activity through the`onActivityResult`method.

To gain access to descendants (child, grandchild, etc) documents, use [DocumentsContract.buildDocumentUriUsingTree(Uri, String)](../android/provider/DocumentsContract.md)), or [DocumentsContract.buildChildDocumentsUriUsingTree(Uri, String)](../android/provider/DocumentsContract.md))with the returned URI.

If your application only needs to store internal data, consider using [Context.getExternalFilesDirs](../android/content/Context.md)), [Context.getExternalCacheDirs()](../android/content/Context.md)), or [Context.getExternalMediaDirs()](../android/content/Context.md)), which require no permissions to read or write.

Access to the entire volume is only available for non-primary volumes (for the primary volume, apps can use the [android.Manifest.permission#READ_EXTERNAL_STORAGE](../android/Manifest.permission.md) and [android.Manifest.permission#WRITE_EXTERNAL_STORAGE](../android/Manifest.permission.md) permissions) and should be used with caution, since users are more likely to deny access when asked for entire volume access rather than specific directories.

| Parameters ||
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `directoryName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:must be one of [Environment.DIRECTORY_MUSIC](../android/os/Environment.md), [Environment.DIRECTORY_PODCASTS](../android/os/Environment.md), [Environment.DIRECTORY_RINGTONES](../android/os/Environment.md), [Environment.DIRECTORY_ALARMS](../android/os/Environment.md), [Environment.DIRECTORY_NOTIFICATIONS](../android/os/Environment.md), [Environment.DIRECTORY_PICTURES](../android/os/Environment.md), [Environment.DIRECTORY_MOVIES](../android/os/Environment.md), [Environment.DIRECTORY_DOWNLOADS](../android/os/Environment.md), [Environment.DIRECTORY_DCIM](../android/os/Environment.md), or [Environment.DIRECTORY_DOCUMENTS](../android/os/Environment.md), or`null`to request access to the entire volume. |

| Return ||
|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [Intent](../android/content/Intent.md)? | intent to request access, or`null`if the requested directory is invalid for that volume. |

**See Also**

- [android.provider.DocumentsContract](../android/provider/DocumentsContract.md) 

### createOpenDocumentTreeIntent

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun createOpenDocumentTreeIntent(): Intent
```

Builds an [Intent.ACTION_OPEN_DOCUMENT_TREE](../android/content/Intent.md) to allow the user to grant access to any directory subtree (or entire volume) from the [android.provider.DocumentsProvider](../android/provider/DocumentsProvider.md) s available on the device. The initial location of the document navigation will be the root of this [StorageVolume](../android/os/storage/StorageVolume.md). Note that the returned [Intent](../android/content/Intent.md) simply suggests that the user picks this [StorageVolume](../android/os/storage/StorageVolume.md) by default, but the user may select a different location. Callers must respect the user's chosen location, even if it is different from the originally requested location.

| Return ||
|---------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Intent](../android/content/Intent.md) | intent to [Intent.ACTION_OPEN_DOCUMENT_TREE](../android/content/Intent.md) initially showing the contents of this [StorageVolume](../android/os/storage/StorageVolume.md) This value cannot be`null`. |

**See Also**

- [android.content.Intent#ACTION_OPEN_DOCUMENT_TREE](../android/content/Intent.md) 

### describeContents

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) |

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

Direct filesystem access via this path has significant emulation overhead, and apps are instead strongly encouraged to interact with media on storage volumes via the [MediaStore](../android/provider/MediaStore.md) APIs.

This directory does not give apps any additional access beyond what they already have via [MediaStore](../android/provider/MediaStore.md).

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [File](../java/io/File.md)? | directory where this volume is mounted, or`null`if the volume is not currently mounted. |

### getMediaStoreVolumeName

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMediaStoreVolumeName(): String?
```

Return the volume name that can be used to interact with this storage device through [MediaStore](../android/provider/MediaStore.md).

| Return ||
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | opaque volume name, or`null`if this volume is not indexed by [MediaStore](../android/provider/MediaStore.md). |

**See Also**

- [android.provider.MediaStore.Audio.Media#getContentUri(String)](../android/provider/MediaStore.Audio.Media.md))
- [android.provider.MediaStore.Video.Media#getContentUri(String)](../android/provider/MediaStore.Video.Media.md))
- [android.provider.MediaStore.Images.Media#getContentUri(String)](../android/provider/MediaStore.Images.Media.md)) 

### getOwner

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getOwner(): UserHandle
```

Returns the user that owns this volume

| Return ||
|------------------------------------------------------------------------------------------|-----------------------------|
| [UserHandle](../android/os/UserHandle.md) | This value cannot be`null`. |

### getState

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getState(): String!
```

Returns the current state of the volume.

| Return ||
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | one of [Environment.MEDIA_UNKNOWN](../android/os/Environment.md), [Environment.MEDIA_REMOVED](../android/os/Environment.md), [Environment.MEDIA_UNMOUNTED](../android/os/Environment.md), [Environment.MEDIA_CHECKING](../android/os/Environment.md), [Environment.MEDIA_NOFS](../android/os/Environment.md), [Environment.MEDIA_MOUNTED](../android/os/Environment.md), [Environment.MEDIA_MOUNTED_READ_ONLY](../android/os/Environment.md), [Environment.MEDIA_SHARED](../android/os/Environment.md), [Environment.MEDIA_BAD_REMOVAL](../android/os/Environment.md), or [Environment.MEDIA_UNMOUNTABLE](../android/os/Environment.md). |

### getStorageUuid

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getStorageUuid(): UUID?
```

Gets the converted volume UUID. If a valid UUID is returned, it is compatible with other APIs that make use of [UUID](../java/util/UUID.md) like android.os.storage.StorageManager#allocateBytes and [android.content.pm.ApplicationInfo#storageUuid](../android/content/pm/ApplicationInfo.md)

| Return ||
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [UUID](../java/util/UUID.md)? | the UUID for the volume or`null`for "portable" storage devices which haven't been adopted. |

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

Returns true if the volume is the primary shared/external storage, which is the volume backed by [Environment.getExternalStorageDirectory()](../android/os/Environment.md)). 

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
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<StorageVolume!>
```
