# StorageManager

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# StorageManager

Kotlin| [Java](../android/os/storage/StorageManager.md) 
| --- | --- |

```
open class StorageManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.os.storage.StorageManager](../android/os/storage/StorageManager.md) |

StorageManager is the interface to the systems storage service. The storage manager handles storage-related items such as Opaque Binary Blobs (OBBs).

OBBs contain a filesystem that maybe be encrypted on disk and mounted on-demand from an application. OBBs are a good way of providing large amounts of binary assets without packaging them into APKs as they may be multiple gigabytes in size. However, due to their size, they're most likely stored in a shared storage pool accessible from all programs. The system does not guarantee the security of the OBB file itself: if any program modifies the OBB, there is no guarantee that a read from that OBB will produce the expected output.

## Summary

| Nested classes ||
|------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open | [StorageVolumeCallback](../android/os/storage/StorageManager.StorageVolumeCallback.md) Callback that delivers [StorageVolume](../android/os/storage/StorageVolume.md) related events. |

| Constants ||
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ACTION_CLEAR_APP_CACHE](../android/os/storage/StorageManager.md) Activity Action: Allows the user to free up space by clearing app external cache directories. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ACTION_MANAGE_STORAGE](../android/os/storage/StorageManager.md) Activity Action: Allows the user to manage their storage. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_REQUESTED_BYTES](../android/os/storage/StorageManager.md) Extra used to indicate the total size (in bytes) that an application is interested in allocating. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_UUID](../android/os/storage/StorageManager.md) Extra [UUID](../java/util/UUID.md) used to indicate the storage volume where an application is interested in allocating or managing disk space. |

| Public methods ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [allocateBytes](../android/os/storage/StorageManager.md))`(`fd:` ` [FileDescriptor](../java/io/FileDescriptor.md)!`, `bytes:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Allocate the requested number of bytes for your application to use in the given open file. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [allocateBytes](../android/os/storage/StorageManager.md))`(`storageUuid:` ` [UUID](../java/util/UUID.md)`, `bytes:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Allocate the requested number of bytes for your application to use on the given storage volume. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getAllocatableBytes](../android/os/storage/StorageManager.md))`(`storageUuid:` ` [UUID](../java/util/UUID.md)`)` Return the maximum number of new bytes that your app can allocate for itself on the given storage volume. |
| --- | --- |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getCacheQuotaBytes](../android/os/storage/StorageManager.md))`(`storageUuid:` ` [UUID](../java/util/UUID.md)`)` Return quota size in bytes for all cached data belonging to the calling app on the given storage volume. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getCacheSizeBytes](../android/os/storage/StorageManager.md))`(`storageUuid:` ` [UUID](../java/util/UUID.md)`)` Return total size in bytes of all cached data belonging to the calling app on the given storage volume. |
| open [PendingIntent](../android/app/PendingIntent.md)? | [getManageSpaceActivityIntent](../android/os/storage/StorageManager.md))`(`packageName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `requestCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns a [PendingIntent](../android/app/PendingIntent.md) that can be used by Apps with [android.Manifest.permission#MANAGE_EXTERNAL_STORAGE](../android/Manifest.permission.md) permission to launch the manageSpaceActivity for any App that implements it, irrespective of its exported status. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getMountedObbPath](../android/os/storage/StorageManager.md))`(`rawPath:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Check the mounted path of an Opaque Binary Blob (OBB) file. |
| open [StorageVolume](../android/os/storage/StorageVolume.md) | [getPrimaryStorageVolume](../android/os/storage/StorageManager.md))`()` Return the primary shared/external storage volume available to the current user. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [StorageVolume](../android/os/storage/StorageVolume.md)!\> | [getRecentStorageVolumes](../android/os/storage/StorageManager.md))`()` Return the list of shared/external storage volumes both currently and recently available to the calling user. |
| --- | --- |
| open [StorageVolume](../android/os/storage/StorageVolume.md) | [getStorageVolume](../android/os/storage/StorageManager.md))`(`uri:` ` [Uri](../android/net/Uri.md)`)` Return the [StorageVolume](../android/os/storage/StorageVolume.md) that contains the given [MediaStore](../android/provider/MediaStore.md) item. |
| open [StorageVolume](../android/os/storage/StorageVolume.md)? | [getStorageVolume](../android/os/storage/StorageManager.md))`(`file:` ` [File](../java/io/File.md)`)` Return the [StorageVolume](../android/os/storage/StorageVolume.md) that contains the given file, or`null`if none. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [StorageVolume](../android/os/storage/StorageVolume.md)!\> | [getStorageVolumes](../android/os/storage/StorageManager.md))`()` Return the list of shared/external storage volumes currently available to the calling user. |
| --- | --- |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [StorageVolume](../android/os/storage/StorageVolume.md)!\> | [getStorageVolumesIncludingSharedProfiles](../android/os/storage/StorageManager.md))`()` Return the list of shared/external storage volumes currently available to the calling user and the user it shares media with. |
| open [UUID](../java/util/UUID.md) | [getUuidForPath](../android/os/storage/StorageManager.md))`(`path:` ` [File](../java/io/File.md)`)` Return a UUID identifying the storage volume that hosts the given filesystem path. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isAllocationSupported](../android/os/storage/StorageManager.md))`(`fd:` ` [FileDescriptor](../java/io/FileDescriptor.md)`)` Test if the given file descriptor supports allocation of disk space using [allocateBytes(java.io.FileDescriptor,long)](../android/os/storage/StorageManager.md)). |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isCacheBehaviorGroup](../android/os/storage/StorageManager.md))`(`path:` ` [File](../java/io/File.md)!`)` Read the current value set by [setCacheBehaviorGroup(java.io.File,boolean)](../android/os/storage/StorageManager.md)). |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isCacheBehaviorTombstone](../android/os/storage/StorageManager.md))`(`path:` ` [File](../java/io/File.md)!`)` Read the current value set by [setCacheBehaviorTombstone(java.io.File,boolean)](../android/os/storage/StorageManager.md)). |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isCheckpointSupported](../android/os/storage/StorageManager.md))`()` Check whether the device supports filesystem checkpoint. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEncrypted](../android/os/storage/StorageManager.md))`(`file:` ` [File](../java/io/File.md)!`)` Return if data stored at or under the given path will be encrypted while at rest. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isObbMounted](../android/os/storage/StorageManager.md))`(`rawPath:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Check whether an Opaque Binary Blob (OBB) is mounted or not. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [mountObb](../android/os/storage/StorageManager.md))`(`rawPath:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `key:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `listener:` ` [OnObbStateChangeListener](../android/os/storage/OnObbStateChangeListener.md)!`)` Mount an Opaque Binary Blob (OBB) file. |
| --- | --- |
| open [ParcelFileDescriptor](../android/os/ParcelFileDescriptor.md) | [openProxyFileDescriptor](../android/os/storage/StorageManager.md))`(`mode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `callback:` ` [ProxyFileDescriptorCallback](../android/os/ProxyFileDescriptorCallback.md)!`, `handler:` ` [Handler](../android/os/Handler.md)!`)` Opens a seekable [ParcelFileDescriptor](../android/os/ParcelFileDescriptor.md) that proxies all low-level I/O requests back to the given [ProxyFileDescriptorCallback](../android/os/ProxyFileDescriptorCallback.md). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerStorageVolumeCallback](../android/os/storage/StorageManager.md))`(`executor:` ` [Executor](../java/util/concurrent/Executor.md)`, `callback:` ` [StorageManager.StorageVolumeCallback](../android/os/storage/StorageManager.StorageVolumeCallback.md)`)` Registers the given callback to listen for [StorageVolume](../android/os/storage/StorageVolume.md) changes. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setCacheBehaviorGroup](../android/os/storage/StorageManager.md))`(`path:` ` [File](../java/io/File.md)!`, `group:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Enable or disable special cache behavior that treats this directory and its contents as an entire group. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setCacheBehaviorTombstone](../android/os/storage/StorageManager.md))`(`path:` ` [File](../java/io/File.md)!`, `tombstone:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Enable or disable special cache behavior that leaves deleted cache files intact as tombstones. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [unmountObb](../android/os/storage/StorageManager.md))`(`rawPath:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `force:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `listener:` ` [OnObbStateChangeListener](../android/os/storage/OnObbStateChangeListener.md)!`)` Unmount an Opaque Binary Blob (OBB) file asynchronously. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unregisterStorageVolumeCallback](../android/os/storage/StorageManager.md))`(`callback:` ` [StorageManager.StorageVolumeCallback](../android/os/storage/StorageManager.StorageVolumeCallback.md)`)` Unregisters the given callback from listening for [StorageVolume](../android/os/storage/StorageVolume.md) changes. |
| --- | --- |

| Properties ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [UUID](../java/util/UUID.md)! | [UUID_DEFAULT](../android/os/storage/StorageManager.md) UUID representing the default internal storage of this device which provides [Environment.getDataDirectory()](../android/os/Environment.md)). |

## Constants

### ACTION_CLEAR_APP_CACHE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACTION_CLEAR_APP_CACHE: String
```

Activity Action: Allows the user to free up space by clearing app external cache directories. The intent doesn't automatically clear cache, but shows a dialog and lets the user decide.

This intent should be launched using [Activity.startActivityForResult(Intent, int)](../android/app/Activity.md))so that the user knows which app is requesting to clear cache. The returned result will be: [Activity.RESULT_OK](../android/app/Activity.md) if the activity was launched and all cache was cleared, [OsConstants.EIO](../android/system/OsConstants.md) if an error occurred while clearing the cache or [Activity.RESULT_CANCELED](../android/app/Activity.md) otherwise. 
Requires [android.Manifest.permission#MANAGE_EXTERNAL_STORAGE](../android/Manifest.permission.md) 

 Value: "android.os.storage.action.CLEAR_APP_CACHE"

### ACTION_MANAGE_STORAGE

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACTION_MANAGE_STORAGE: String
```

Activity Action: Allows the user to manage their storage. This activity provides the ability to free up space on the device by deleting data such as apps.

If the sending application has a specific storage device or allocation size in mind, they can optionally define [EXTRA_UUID](../android/os/storage/StorageManager.md) or [EXTRA_REQUESTED_BYTES](../android/os/storage/StorageManager.md), respectively.

This intent should be launched using [Activity.startActivityForResult(Intent, int)](../android/app/Activity.md))so that the user knows which app is requesting the storage space. The returned result will be [Activity.RESULT_OK](../android/app/Activity.md) if the requested space was made available, or [Activity.RESULT_CANCELED](../android/app/Activity.md) otherwise. 

 Value: "android.os.storage.action.MANAGE_STORAGE"

### EXTRA_REQUESTED_BYTES

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_REQUESTED_BYTES: String
```

Extra used to indicate the total size (in bytes) that an application is interested in allocating.

When defined, the management UI will help guide the user to free up enough disk space to reach this requested value. 

 Value: "android.os.storage.extra.REQUESTED_BYTES"

**See Also**

- [#ACTION_MANAGE_STORAGE](../android/os/storage/StorageManager.md) 

### EXTRA_UUID

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_UUID: String
```

Extra [UUID](../java/util/UUID.md) used to indicate the storage volume where an application is interested in allocating or managing disk space. 

 Value: "android.os.storage.extra.UUID"

**See Also**

- [#ACTION_MANAGE_STORAGE](../android/os/storage/StorageManager.md)
- [#UUID_DEFAULT](../android/os/storage/StorageManager.md)
- [#getUuidForPath(File)](../android/os/storage/StorageManager.md))
- [android.content.Intent#putExtra(String, java.io.Serializable)](../android/content/Intent.md))

## Public methods

### allocateBytes

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun allocateBytes(
    fd: FileDescriptor!, 
    bytes: Long
): Unit
```

Allocate the requested number of bytes for your application to use in the given open file. This will cause the system to delete any cached files necessary to satisfy your request.

Attempts to allocate disk space beyond the value returned by [getAllocatableBytes(java.util.UUID)](../android/os/storage/StorageManager.md))will fail.

This method guarantees that bytes have been allocated to the opened file, otherwise it will throw if fast allocation is not possible. Fast allocation is typically only supported in private app data directories, and on shared/external storage devices which are emulated.

If you're progressively allocating an unbounded amount of storage space (such as when recording a video) you should avoid calling this method more than once every 60 seconds. 
This method may take several seconds to complete, so it should only be called from a worker thread.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `fd` | [FileDescriptor](../java/io/FileDescriptor.md)!:the open file that you'd like to allocate disk space for. |
| `bytes` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the number of bytes to allocate. This is the desired final size of the open file. If the open file is smaller than this requested size, it will be extended without modifying any existing contents. If the open file is larger than this requested size, it will be truncated. Value is a non-negative number of bytes. |

| Exceptions ||
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | when the storage device isn't present, or when it doesn't support allocating space, or if the device had trouble allocating the requested space. |

**See Also**

- [#isAllocationSupported(FileDescriptor)](../android/os/storage/StorageManager.md))
- [android.os.Environment#isExternalStorageEmulated(File)](../android/os/Environment.md)) 

### allocateBytes

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun allocateBytes(
    storageUuid: UUID, 
    bytes: Long
): Unit
```

Allocate the requested number of bytes for your application to use on the given storage volume. This will cause the system to delete any cached files necessary to satisfy your request.

Attempts to allocate disk space beyond the value returned by [getAllocatableBytes(java.util.UUID)](../android/os/storage/StorageManager.md))will fail.

Since multiple apps can be running simultaneously, this method may be subject to race conditions. If possible, consider using [allocateBytes(java.io.FileDescriptor,long)](../android/os/storage/StorageManager.md))which will guarantee that bytes are allocated to an opened file.

If you're progressively allocating an unbounded amount of storage space (such as when recording a video) you should avoid calling this method more than once every 60 seconds. 
This method may take several seconds to complete, so it should only be called from a worker thread.

| Parameters ||
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `storageUuid` | [UUID](../java/util/UUID.md):the UUID of the storage volume where you'd like to allocate disk space. The UUID for a specific path can be obtained using [getUuidForPath(java.io.File)](../android/os/storage/StorageManager.md)). This value cannot be`null`. |
| `bytes` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the number of bytes to allocate. Value is a non-negative number of bytes. |

| Exceptions ||
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | when the storage device isn't present, or when it doesn't support allocating space, or if the device had trouble allocating the requested space. |

**See Also**

- [#getAllocatableBytes(UUID)](../android/os/storage/StorageManager.md)) 

### getAllocatableBytes

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getAllocatableBytes(storageUuid: UUID): Long
```

Return the maximum number of new bytes that your app can allocate for itself on the given storage volume. This value is typically larger than [File.getUsableSpace()](../java/io/File.md)), since the system may be willing to delete cached files to satisfy an allocation request. You can then allocate space for yourself using [allocateBytes(java.util.UUID,long)](../android/os/storage/StorageManager.md))or [allocateBytes(java.io.FileDescriptor,long)](../android/os/storage/StorageManager.md)).

This method is best used as a pre-flight check, such as deciding if there is enough space to store an entire music album before you allocate space for each audio file in the album. Attempts to allocate disk space beyond the returned value will fail.

If the returned value is not large enough for the data you'd like to persist, you can launch [ACTION_MANAGE_STORAGE](../android/os/storage/StorageManager.md) with the [EXTRA_UUID](../android/os/storage/StorageManager.md) and [EXTRA_REQUESTED_BYTES](../android/os/storage/StorageManager.md) options to help involve the user in freeing up disk space.

If you're progressively allocating an unbounded amount of storage space (such as when recording a video) you should avoid calling this method more than once every 30 seconds.

Note: if your app uses the`android:sharedUserId`manifest feature, then allocatable space for all packages in your shared UID is tracked together as a single unit.

This method may take several seconds to complete, so it should only be called from a worker thread. 
Value is a non-negative number of bytes.

| Parameters ||
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `storageUuid` | [UUID](../java/util/UUID.md):the UUID of the storage volume where you're considering allocating disk space, since allocatable space can vary widely depending on the underlying storage device. The UUID for a specific path can be obtained using [getUuidForPath(java.io.File)](../android/os/storage/StorageManager.md)). This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the maximum number of new bytes that the calling app can allocate using [allocateBytes(java.util.UUID,long)](../android/os/storage/StorageManager.md))or [allocateBytes(java.io.FileDescriptor,long)](../android/os/storage/StorageManager.md)). Value is a non-negative number of bytes. |

| Exceptions ||
|-----------------------|-------------------------------------------------------------------------------------|
| `java.io.IOException` | when the storage device isn't present, or when it doesn't support allocating space. |

### getCacheQuotaBytes

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getCacheQuotaBytes(storageUuid: UUID): Long
```

Return quota size in bytes for all cached data belonging to the calling app on the given storage volume.

If your app goes above this quota, your cached files will be some of the first to be deleted when additional disk space is needed. Conversely, if your app stays under this quota, your cached files will be some of the last to be deleted when additional disk space is needed.

This quota will change over time depending on how frequently the user interacts with your app, and depending on how much system-wide disk space is used.

Note: if your app uses the`android:sharedUserId`manifest feature, then cached data for all packages in your shared UID is tracked together as a single unit.

This method may take several seconds to complete, so it should only be called from a worker thread. 
Value is a non-negative number of bytes.

| Parameters ||
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `storageUuid` | [UUID](../java/util/UUID.md):the UUID of the storage volume that you're interested in. The UUID for a specific path can be obtained using [getUuidForPath(java.io.File)](../android/os/storage/StorageManager.md)). This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------|------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | Value is a non-negative number of bytes. |

| Exceptions ||
|-----------------------|---------------------------------------------------------------------------------|
| `java.io.IOException` | when the storage device isn't present, or when it doesn't support cache quotas. |

**See Also**

- [#getCacheSizeBytes(UUID)](../android/os/storage/StorageManager.md)) 

### getCacheSizeBytes

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getCacheSizeBytes(storageUuid: UUID): Long
```

Return total size in bytes of all cached data belonging to the calling app on the given storage volume.

Cached data tracked by this method always includes [Context.getCacheDir()](../android/content/Context.md))and [Context.getCodeCacheDir()](../android/content/Context.md)), and it also includes [Context.getExternalCacheDir()](../android/content/Context.md))if the primary shared/external storage is hosted on the same storage device as your private data.

Note: if your app uses the`android:sharedUserId`manifest feature, then cached data for all packages in your shared UID is tracked together as a single unit.

This method may take several seconds to complete, so it should only be called from a worker thread. 
Value is a non-negative number of bytes.

| Parameters ||
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `storageUuid` | [UUID](../java/util/UUID.md):the UUID of the storage volume that you're interested in. The UUID for a specific path can be obtained using [getUuidForPath(java.io.File)](../android/os/storage/StorageManager.md)). This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------|------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | Value is a non-negative number of bytes. |

| Exceptions ||
|-----------------------|---------------------------------------------------------------------------------|
| `java.io.IOException` | when the storage device isn't present, or when it doesn't support cache quotas. |

**See Also**

- [#getCacheQuotaBytes(UUID)](../android/os/storage/StorageManager.md)) 

### getManageSpaceActivityIntent

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getManageSpaceActivityIntent(
    packageName: String, 
    requestCode: Int
): PendingIntent?
```

Returns a [PendingIntent](../android/app/PendingIntent.md) that can be used by Apps with [android.Manifest.permission#MANAGE_EXTERNAL_STORAGE](../android/Manifest.permission.md) permission to launch the manageSpaceActivity for any App that implements it, irrespective of its exported status.

Caller has the responsibility of supplying a valid packageName which has manageSpaceActivity implemented. 
Requires [android.Manifest.permission#MANAGE_EXTERNAL_STORAGE](../android/Manifest.permission.md)

| Parameters ||
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):package name for the App for which manageSpaceActivity is to be launched This value cannot be`null`. |
| `requestCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):for launching the activity |

| Return ||
|--------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [PendingIntent](../android/app/PendingIntent.md)? | PendingIntent to launch the manageSpaceActivity if successful, null if the packageName doesn't have a manageSpaceActivity. |

| Exceptions ||
|--------------------------------------|-------------------------------------|
| `java.lang.IllegalArgumentException` | an invalid packageName is supplied. |

### getMountedObbPath

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getMountedObbPath(rawPath: String!): String!
```

Check the mounted path of an Opaque Binary Blob (OBB) file. This will give you the path to where you can obtain access to the internals of the OBB.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------|
| `rawPath` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:path to OBB image |

| Return ||
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | absolute path to mounted OBB image data or`null`if not mounted or exception encountered trying to read status |

### getPrimaryStorageVolume

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPrimaryStorageVolume(): StorageVolume
```

Return the primary shared/external storage volume available to the current user. This volume is the same storage device returned by [Environment.getExternalStorageDirectory()](../android/os/Environment.md))and [Context.getExternalFilesDir(String)](../android/content/Context.md)).

| Return ||
|--------------------------------------------------------------------------------------------------|-----------------------------|
| [StorageVolume](../android/os/storage/StorageVolume.md) | This value cannot be`null`. |

### getRecentStorageVolumes

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getRecentStorageVolumes(): MutableList<StorageVolume!>
```

Return the list of shared/external storage volumes both currently and recently available to the calling user.

Recently available storage volumes are likely to reappear in the future, so apps are encouraged to preserve any indexed metadata related to these volumes to optimize user experiences.

| Return ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [StorageVolume](../android/os/storage/StorageVolume.md)!> | This value cannot be`null`. |

### getStorageVolume

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getStorageVolume(uri: Uri): StorageVolume
```

Return the [StorageVolume](../android/os/storage/StorageVolume.md) that contains the given [MediaStore](../android/provider/MediaStore.md) item.

| Parameters ||
|-------|---------------------------------------------------------------------------------------------------------|
| `uri` | [Uri](../android/net/Uri.md):This value cannot be`null`. |

| Return ||
|--------------------------------------------------------------------------------------------------|-----------------------------|
| [StorageVolume](../android/os/storage/StorageVolume.md) | This value cannot be`null`. |

### getStorageVolume

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getStorageVolume(file: File): StorageVolume?
```

Return the [StorageVolume](../android/os/storage/StorageVolume.md) that contains the given file, or`null`if none.

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------|
| `file` | [File](../java/io/File.md):This value cannot be`null`. |

### getStorageVolumes

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getStorageVolumes(): MutableList<StorageVolume!>
```

Return the list of shared/external storage volumes currently available to the calling user.

These storage volumes are actively attached to the device, but may be in any mount state, as returned by [StorageVolume.getState()](../android/os/storage/StorageVolume.md)). Returns both the primary shared storage device and any attached external volumes, including SD cards and USB drives.

| Return ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [StorageVolume](../android/os/storage/StorageVolume.md)!> | This value cannot be`null`. |

### getStorageVolumesIncludingSharedProfiles

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getStorageVolumesIncludingSharedProfiles(): MutableList<StorageVolume!>
```

Return the list of shared/external storage volumes currently available to the calling user and the user it shares media with. Please refer to [multi-user support](https://source.android.com/compatibility/12/android-12-cdd#95_multi-user_support) for more details.

This is similar to [StorageManager.getStorageVolumes()](../android/os/storage/StorageManager.md))except that the result also includes the volumes belonging to any user it shares media with 
Requires [android.Manifest.permission#MANAGE_EXTERNAL_STORAGE](../android/Manifest.permission.md)

| Return ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [StorageVolume](../android/os/storage/StorageVolume.md)!> | This value cannot be`null`. |

### getUuidForPath

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getUuidForPath(path: File): UUID
```

Return a UUID identifying the storage volume that hosts the given filesystem path.

If this path is hosted by the default internal storage of the device at [Environment.getDataDirectory()](../android/os/Environment.md)), the returned value will be [UUID_DEFAULT](../android/os/storage/StorageManager.md).

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------|
| `path` | [File](../java/io/File.md):This value cannot be`null`. |

| Return ||
|-----------------------------------------------------------------------------|-----------------------------|
| [UUID](../java/util/UUID.md) | This value cannot be`null`. |

| Exceptions ||
|-----------------------|-----------------------------------------------------------------------------------------------------|
| `java.io.IOException` | when the storage device hosting the given path isn't present, or when it doesn't have a valid UUID. |

### isAllocationSupported

Added in [API level 27](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isAllocationSupported(fd: FileDescriptor): Boolean
```

Test if the given file descriptor supports allocation of disk space using [allocateBytes(java.io.FileDescriptor,long)](../android/os/storage/StorageManager.md)).

| Parameters ||
|------|---------------------------------------------------------------------------------------------------------------------------|
| `fd` | [FileDescriptor](../java/io/FileDescriptor.md):This value cannot be`null`. |

### isCacheBehaviorGroup

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isCacheBehaviorGroup(path: File!): Boolean
```

Read the current value set by [setCacheBehaviorGroup(java.io.File,boolean)](../android/os/storage/StorageManager.md)). 

### isCacheBehaviorTombstone

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isCacheBehaviorTombstone(path: File!): Boolean
```

Read the current value set by [setCacheBehaviorTombstone(java.io.File,boolean)](../android/os/storage/StorageManager.md)). 

### isCheckpointSupported

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isCheckpointSupported(): Boolean
```

Check whether the device supports filesystem checkpoint.

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the device supports filesystem checkpoint, false otherwise. |

### isEncrypted

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isEncrypted(file: File!): Boolean
```

Return if data stored at or under the given path will be encrypted while at rest. This can help apps avoid the overhead of double-encrypting data. 

### isObbMounted

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isObbMounted(rawPath: String!): Boolean
```

Check whether an Opaque Binary Blob (OBB) is mounted or not.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------|
| `rawPath` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:path to OBB image |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if OBB is mounted; false if not mounted or on error |

### mountObb

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun mountObb(
    rawPath: String!, 
    key: String!, 
    listener: OnObbStateChangeListener!
): Boolean
```

Mount an Opaque Binary Blob (OBB) file.

The OBB will remain mounted for as long as the StorageManager reference is held by the application. As soon as this reference is lost, the OBBs in use will be unmounted. The [OnObbStateChangeListener](../android/os/storage/OnObbStateChangeListener.md) registered with this call will receive the success or failure of this operation.

*Note:*you can only mount OBB files for which the OBB tag on the file matches a package ID that is owned by the calling program's UID. That is, shared UID applications can attempt to mount any other application's OBB that shares its UID.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `rawPath` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the path to the OBB file |
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:must be`null`. Previously, some Android device implementations accepted a non-`null`key to mount an encrypted OBB file. However, this never worked reliably and is no longer supported. |
| `listener` | [OnObbStateChangeListener](../android/os/storage/OnObbStateChangeListener.md)!:will receive the success or failure of the operation |
| --- | --- |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | whether the mount call was successfully queued or not |

### openProxyFileDescriptor

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun openProxyFileDescriptor(
    mode: Int, 
    callback: ProxyFileDescriptorCallback!, 
    handler: Handler!
): ParcelFileDescriptor
```

Opens a seekable [ParcelFileDescriptor](../android/os/ParcelFileDescriptor.md) that proxies all low-level I/O requests back to the given [ProxyFileDescriptorCallback](../android/os/ProxyFileDescriptorCallback.md).

This can be useful when you want to provide quick access to a large file that isn't backed by a real file on disk, such as a file on a network share, cloud storage service, etc. As an example, you could respond to a [ContentResolver.openFileDescriptor(android.net.Uri, String)](../android/content/ContentResolver.md))request by returning a [ParcelFileDescriptor](../android/os/ParcelFileDescriptor.md) created with this method, and then stream the content on-demand as requested.

Another useful example might be where you have an encrypted file that you're willing to decrypt on-demand, but where you want to avoid persisting the cleartext version.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `mode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The desired access mode, must be one of [ParcelFileDescriptor.MODE_READ_ONLY](../android/os/ParcelFileDescriptor.md), [ParcelFileDescriptor.MODE_WRITE_ONLY](../android/os/ParcelFileDescriptor.md), or [ParcelFileDescriptor.MODE_READ_WRITE](../android/os/ParcelFileDescriptor.md) |
| `callback` | [ProxyFileDescriptorCallback](../android/os/ProxyFileDescriptorCallback.md)!:Callback to process file operation requests issued on returned file descriptor. |
| `handler` | [Handler](../android/os/Handler.md)!:Handler that invokes callback methods. |
| --- | --- |

| Return ||
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| [ParcelFileDescriptor](../android/os/ParcelFileDescriptor.md) | Seekable ParcelFileDescriptor. This value cannot be`null`. |

### registerStorageVolumeCallback

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun registerStorageVolumeCallback(
    executor: Executor, 
    callback: StorageManager.StorageVolumeCallback
): Unit
```

Registers the given callback to listen for [StorageVolume](../android/os/storage/StorageVolume.md) changes.

For example, this can be used to detect when a volume changes to the [Environment.MEDIA_MOUNTED](../android/os/Environment.md) or [Environment.MEDIA_UNMOUNTED](../android/os/Environment.md) states.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `executor` | [Executor](../java/util/concurrent/Executor.md):Callback and listener events are dispatched through this [Executor](../java/util/concurrent/Executor.md), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](../android/content/Context.md)). Otherwise, provide an [Executor](../java/util/concurrent/Executor.md) that dispatches to an appropriate thread. This value cannot be`null`. |
| `callback` | [StorageManager.StorageVolumeCallback](../android/os/storage/StorageManager.StorageVolumeCallback.md):This value cannot be`null`. |

**See Also**

- [android.os.storage.StorageManager#unregisterStorageVolumeCallback](../android/os/storage/StorageManager.md)) 

### setCacheBehaviorGroup

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setCacheBehaviorGroup(
    path: File!, 
    group: Boolean
): Unit
```

Enable or disable special cache behavior that treats this directory and its contents as an entire group.

When enabled and this directory is considered for automatic deletion by the OS, all contained files will either be deleted together, or not at all. This is useful when you have a directory that contains several related metadata files that depend on each other, such as movie file and a subtitle file.

When enabled, the*newest* [File.lastModified()](../java/io/File.md))value of any contained files is considered the modified time of the entire directory.

This behavior can only be set on a directory, and it applies recursively to all contained files and directories. 

### setCacheBehaviorTombstone

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setCacheBehaviorTombstone(
    path: File!, 
    tombstone: Boolean
): Unit
```

Enable or disable special cache behavior that leaves deleted cache files intact as tombstones.

When enabled and a file contained in this directory is automatically deleted by the OS, the file will be truncated to have a length of 0 bytes instead of being fully deleted. This is useful if you need to distinguish between a file that was deleted versus one that never existed.

This behavior can only be set on a directory, and it applies recursively to all contained files and directories.

Note: this behavior is ignored completely if the user explicitly requests that all cached data be cleared. 

### unmountObb

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun unmountObb(
    rawPath: String!, 
    force: Boolean, 
    listener: OnObbStateChangeListener!
): Boolean
```

Unmount an Opaque Binary Blob (OBB) file asynchronously. If the`force`flag is true, it will kill any application needed to unmount the given OBB (even the calling application).

The [OnObbStateChangeListener](../android/os/storage/OnObbStateChangeListener.md) registered with this call will receive the success or failure of this operation.

*Note:*you can only mount OBB files for which the OBB tag on the file matches a package ID that is owned by the calling program's UID. That is, shared UID applications can obtain access to any other application's OBB that shares its UID.

<br />

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `rawPath` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:path to the OBB file |
| `force` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):whether to kill any programs using this in order to unmount it |
| `listener` | [OnObbStateChangeListener](../android/os/storage/OnObbStateChangeListener.md)!:will receive the success or failure of the operation |
| --- | --- |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | whether the unmount call was successfully queued or not |

### unregisterStorageVolumeCallback

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun unregisterStorageVolumeCallback(callback: StorageManager.StorageVolumeCallback): Unit
```

Unregisters the given callback from listening for [StorageVolume](../android/os/storage/StorageVolume.md) changes.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `callback` | [StorageManager.StorageVolumeCallback](../android/os/storage/StorageManager.StorageVolumeCallback.md):This value cannot be`null`. |

**See Also**

- [android.os.storage.StorageManager#registerStorageVolumeCallback](../android/os/storage/StorageManager.md))

## Properties

### UUID_DEFAULT

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val UUID_DEFAULT: UUID!
```

UUID representing the default internal storage of this device which provides [Environment.getDataDirectory()](../android/os/Environment.md)).

This value is constant across all devices and it will never change, and thus it cannot be used to uniquely identify a particular physical device. 
**See Also**

- [#getUuidForPath(File)](../android/os/storage/StorageManager.md))
- [android.content.pm.ApplicationInfo#storageUuid](../android/content/pm/ApplicationInfo.md)
