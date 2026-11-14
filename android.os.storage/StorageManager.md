# StorageManager

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# StorageManager

Kotlin| [Java](https://developer.android.com/reference/android/os/storage/StorageManager "View this page in Java") 
| --- | --- |

```
open class StorageManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.os.storage.StorageManager](https://developer.android.com/reference/kotlin/android/os/storage/StorageManager#) |

StorageManager is the interface to the systems storage service. The storage manager handles storage-related items such as Opaque Binary Blobs (OBBs).

OBBs contain a filesystem that maybe be encrypted on disk and mounted on-demand from an application. OBBs are a good way of providing large amounts of binary assets without packaging them into APKs as they may be multiple gigabytes in size. However, due to their size, they're most likely stored in a shared storage pool accessible from all programs. The system does not guarantee the security of the OBB file itself: if any program modifies the OBB, there is no guarantee that a read from that OBB will produce the expected output.

## Summary

| Nested classes ||
|------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open | [StorageVolumeCallback](https://developer.android.com/reference/kotlin/android/os/storage/StorageManager.StorageVolumeCallback) Callback that delivers [StorageVolume](https://developer.android.com/reference/kotlin/android/os/storage/StorageVolume) related events. |

| Constants ||
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ACTION_CLEAR_APP_CACHE](https://developer.android.com/reference/kotlin/android/os/storage/StorageManager#ACTION_CLEAR_APP_CACHE:kotlin.String) Activity Action: Allows the user to free up space by clearing app external cache directories. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ACTION_MANAGE_STORAGE](https://developer.android.com/reference/kotlin/android/os/storage/StorageManager#ACTION_MANAGE_STORAGE:kotlin.String) Activity Action: Allows the user to manage their storage. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_REQUESTED_BYTES](https://developer.android.com/reference/kotlin/android/os/storage/StorageManager#EXTRA_REQUESTED_BYTES:kotlin.String) Extra used to indicate the total size (in bytes) that an application is interested in allocating. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_UUID](https://developer.android.com/reference/kotlin/android/os/storage/StorageManager#EXTRA_UUID:kotlin.String) Extra [UUID](https://developer.android.com/reference/kotlin/java/util/UUID.html#) used to indicate the storage volume where an application is interested in allocating or managing disk space. |

| Public methods ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [allocateBytes](https://developer.android.com/reference/kotlin/android/os/storage/StorageManager#allocateBytes(java.io.FileDescriptor,%20kotlin.Long))`(`fd:` ` [FileDescriptor](https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#)!`, `bytes:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Allocate the requested number of bytes for your application to use in the given open file. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [allocateBytes](https://developer.android.com/reference/kotlin/android/os/storage/StorageManager#allocateBytes(java.util.UUID,%20kotlin.Long))`(`storageUuid:` ` [UUID](https://developer.android.com/reference/kotlin/java/util/UUID.html#)`, `bytes:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Allocate the requested number of bytes for your application to use on the given storage volume. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getAllocatableBytes](https://developer.android.com/reference/kotlin/android/os/storage/StorageManager#getAllocatableBytes(java.util.UUID))`(`storageUuid:` ` [UUID](https://developer.android.com/reference/kotlin/java/util/UUID.html#)`)` Return the maximum number of new bytes that your app can allocate for itself on the given storage volume. |
| --- | --- |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getCacheQuotaBytes](https://developer.android.com/reference/kotlin/android/os/storage/StorageManager#getCacheQuotaBytes(java.util.UUID))`(`storageUuid:` ` [UUID](https://developer.android.com/reference/kotlin/java/util/UUID.html#)`)` Return quota size in bytes for all cached data belonging to the calling app on the given storage volume. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getCacheSizeBytes](https://developer.android.com/reference/kotlin/android/os/storage/StorageManager#getCacheSizeBytes(java.util.UUID))`(`storageUuid:` ` [UUID](https://developer.android.com/reference/kotlin/java/util/UUID.html#)`)` Return total size in bytes of all cached data belonging to the calling app on the given storage volume. |
| open [PendingIntent](https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#)? | [getManageSpaceActivityIntent](https://developer.android.com/reference/kotlin/android/os/storage/StorageManager#getManageSpaceActivityIntent(kotlin.String,%20kotlin.Int))`(`packageName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `requestCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns a [PendingIntent](https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#) that can be used by Apps with [android.Manifest.permission#MANAGE_EXTERNAL_STORAGE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MANAGE_EXTERNAL_STORAGE:kotlin.String) permission to launch the manageSpaceActivity for any App that implements it, irrespective of its exported status. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getMountedObbPath](https://developer.android.com/reference/kotlin/android/os/storage/StorageManager#getMountedObbPath(kotlin.String))`(`rawPath:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Check the mounted path of an Opaque Binary Blob (OBB) file. |
| open [StorageVolume](https://developer.android.com/reference/kotlin/android/os/storage/StorageVolume) | [getPrimaryStorageVolume](https://developer.android.com/reference/kotlin/android/os/storage/StorageManager#getPrimaryStorageVolume())`()` Return the primary shared/external storage volume available to the current user. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [StorageVolume](https://developer.android.com/reference/kotlin/android/os/storage/StorageVolume)!\> | [getRecentStorageVolumes](https://developer.android.com/reference/kotlin/android/os/storage/StorageManager#getRecentStorageVolumes())`()` Return the list of shared/external storage volumes both currently and recently available to the calling user. |
| --- | --- |
| open [StorageVolume](https://developer.android.com/reference/kotlin/android/os/storage/StorageVolume) | [getStorageVolume](https://developer.android.com/reference/kotlin/android/os/storage/StorageManager#getStorageVolume(android.net.Uri))`(`uri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)`)` Return the [StorageVolume](https://developer.android.com/reference/kotlin/android/os/storage/StorageVolume) that contains the given [MediaStore](https://developer.android.com/reference/kotlin/android/provider/MediaStore.html#) item. |
| open [StorageVolume](https://developer.android.com/reference/kotlin/android/os/storage/StorageVolume)? | [getStorageVolume](https://developer.android.com/reference/kotlin/android/os/storage/StorageManager#getStorageVolume(java.io.File))`(`file:` ` [File](https://developer.android.com/reference/kotlin/java/io/File.html#)`)` Return the [StorageVolume](https://developer.android.com/reference/kotlin/android/os/storage/StorageVolume) that contains the given file, or`null`if none. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [StorageVolume](https://developer.android.com/reference/kotlin/android/os/storage/StorageVolume)!\> | [getStorageVolumes](https://developer.android.com/reference/kotlin/android/os/storage/StorageManager#getStorageVolumes())`()` Return the list of shared/external storage volumes currently available to the calling user. |
| --- | --- |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [StorageVolume](https://developer.android.com/reference/kotlin/android/os/storage/StorageVolume)!\> | [getStorageVolumesIncludingSharedProfiles](https://developer.android.com/reference/kotlin/android/os/storage/StorageManager#getStorageVolumesIncludingSharedProfiles())`()` Return the list of shared/external storage volumes currently available to the calling user and the user it shares media with. |
| open [UUID](https://developer.android.com/reference/kotlin/java/util/UUID.html#) | [getUuidForPath](https://developer.android.com/reference/kotlin/android/os/storage/StorageManager#getUuidForPath(java.io.File))`(`path:` ` [File](https://developer.android.com/reference/kotlin/java/io/File.html#)`)` Return a UUID identifying the storage volume that hosts the given filesystem path. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isAllocationSupported](https://developer.android.com/reference/kotlin/android/os/storage/StorageManager#isAllocationSupported(java.io.FileDescriptor))`(`fd:` ` [FileDescriptor](https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#)`)` Test if the given file descriptor supports allocation of disk space using [allocateBytes(java.io.FileDescriptor,long)](https://developer.android.com/reference/kotlin/android/os/storage/StorageManager#allocateBytes(java.io.FileDescriptor,%20kotlin.Long)). |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isCacheBehaviorGroup](https://developer.android.com/reference/kotlin/android/os/storage/StorageManager#isCacheBehaviorGroup(java.io.File))`(`path:` ` [File](https://developer.android.com/reference/kotlin/java/io/File.html#)!`)` Read the current value set by [setCacheBehaviorGroup(java.io.File,boolean)](https://developer.android.com/reference/kotlin/android/os/storage/StorageManager#setCacheBehaviorGroup(java.io.File,%20kotlin.Boolean)). |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isCacheBehaviorTombstone](https://developer.android.com/reference/kotlin/android/os/storage/StorageManager#isCacheBehaviorTombstone(java.io.File))`(`path:` ` [File](https://developer.android.com/reference/kotlin/java/io/File.html#)!`)` Read the current value set by [setCacheBehaviorTombstone(java.io.File,boolean)](https://developer.android.com/reference/kotlin/android/os/storage/StorageManager#setCacheBehaviorTombstone(java.io.File,%20kotlin.Boolean)). |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isCheckpointSupported](https://developer.android.com/reference/kotlin/android/os/storage/StorageManager#isCheckpointSupported())`()` Check whether the device supports filesystem checkpoint. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEncrypted](https://developer.android.com/reference/kotlin/android/os/storage/StorageManager#isEncrypted(java.io.File))`(`file:` ` [File](https://developer.android.com/reference/kotlin/java/io/File.html#)!`)` Return if data stored at or under the given path will be encrypted while at rest. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isObbMounted](https://developer.android.com/reference/kotlin/android/os/storage/StorageManager#isObbMounted(kotlin.String))`(`rawPath:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Check whether an Opaque Binary Blob (OBB) is mounted or not. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [mountObb](https://developer.android.com/reference/kotlin/android/os/storage/StorageManager#mountObb(kotlin.String,%20kotlin.String,%20android.os.storage.OnObbStateChangeListener))`(`rawPath:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `key:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `listener:` ` [OnObbStateChangeListener](https://developer.android.com/reference/kotlin/android/os/storage/OnObbStateChangeListener)!`)` Mount an Opaque Binary Blob (OBB) file. |
| --- | --- |
| open [ParcelFileDescriptor](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#) | [openProxyFileDescriptor](https://developer.android.com/reference/kotlin/android/os/storage/StorageManager#openProxyFileDescriptor(kotlin.Int,%20android.os.ProxyFileDescriptorCallback,%20android.os.Handler))`(`mode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `callback:` ` [ProxyFileDescriptorCallback](https://developer.android.com/reference/kotlin/android/os/ProxyFileDescriptorCallback.html#)!`, `handler:` ` [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#)!`)` Opens a seekable [ParcelFileDescriptor](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#) that proxies all low-level I/O requests back to the given [ProxyFileDescriptorCallback](https://developer.android.com/reference/kotlin/android/os/ProxyFileDescriptorCallback.html#). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerStorageVolumeCallback](https://developer.android.com/reference/kotlin/android/os/storage/StorageManager#registerStorageVolumeCallback(java.util.concurrent.Executor,%20android.os.storage.StorageManager.StorageVolumeCallback))`(`executor:` ` [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#)`, `callback:` ` [StorageManager.StorageVolumeCallback](https://developer.android.com/reference/kotlin/android/os/storage/StorageManager.StorageVolumeCallback)`)` Registers the given callback to listen for [StorageVolume](https://developer.android.com/reference/kotlin/android/os/storage/StorageVolume) changes. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setCacheBehaviorGroup](https://developer.android.com/reference/kotlin/android/os/storage/StorageManager#setCacheBehaviorGroup(java.io.File,%20kotlin.Boolean))`(`path:` ` [File](https://developer.android.com/reference/kotlin/java/io/File.html#)!`, `group:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Enable or disable special cache behavior that treats this directory and its contents as an entire group. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setCacheBehaviorTombstone](https://developer.android.com/reference/kotlin/android/os/storage/StorageManager#setCacheBehaviorTombstone(java.io.File,%20kotlin.Boolean))`(`path:` ` [File](https://developer.android.com/reference/kotlin/java/io/File.html#)!`, `tombstone:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Enable or disable special cache behavior that leaves deleted cache files intact as tombstones. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [unmountObb](https://developer.android.com/reference/kotlin/android/os/storage/StorageManager#unmountObb(kotlin.String,%20kotlin.Boolean,%20android.os.storage.OnObbStateChangeListener))`(`rawPath:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `force:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `listener:` ` [OnObbStateChangeListener](https://developer.android.com/reference/kotlin/android/os/storage/OnObbStateChangeListener)!`)` Unmount an Opaque Binary Blob (OBB) file asynchronously. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unregisterStorageVolumeCallback](https://developer.android.com/reference/kotlin/android/os/storage/StorageManager#unregisterStorageVolumeCallback(android.os.storage.StorageManager.StorageVolumeCallback))`(`callback:` ` [StorageManager.StorageVolumeCallback](https://developer.android.com/reference/kotlin/android/os/storage/StorageManager.StorageVolumeCallback)`)` Unregisters the given callback from listening for [StorageVolume](https://developer.android.com/reference/kotlin/android/os/storage/StorageVolume) changes. |
| --- | --- |

| Properties ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [UUID](https://developer.android.com/reference/kotlin/java/util/UUID.html#)! | [UUID_DEFAULT](https://developer.android.com/reference/kotlin/android/os/storage/StorageManager#UUID_DEFAULT:java.util.UUID) UUID representing the default internal storage of this device which provides [Environment.getDataDirectory()](https://developer.android.com/reference/kotlin/android/os/Environment.html#getDataDirectory()). |

## Constants

### ACTION_CLEAR_APP_CACHE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACTION_CLEAR_APP_CACHE: String
```

Activity Action: Allows the user to free up space by clearing app external cache directories. The intent doesn't automatically clear cache, but shows a dialog and lets the user decide.

This intent should be launched using [Activity.startActivityForResult(Intent, int)](https://developer.android.com/reference/kotlin/android/app/Activity.html#startActivityForResult(android.content.Intent,%20kotlin.Int))so that the user knows which app is requesting to clear cache. The returned result will be: [Activity.RESULT_OK](https://developer.android.com/reference/kotlin/android/app/Activity.html#RESULT_OK:kotlin.Int) if the activity was launched and all cache was cleared, [OsConstants.EIO](https://developer.android.com/reference/kotlin/android/system/OsConstants.html#EIO:kotlin.Int) if an error occurred while clearing the cache or [Activity.RESULT_CANCELED](https://developer.android.com/reference/kotlin/android/app/Activity.html#RESULT_CANCELED:kotlin.Int) otherwise. 
Requires [android.Manifest.permission#MANAGE_EXTERNAL_STORAGE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MANAGE_EXTERNAL_STORAGE:kotlin.String) 

 Value: "android.os.storage.action.CLEAR_APP_CACHE"

### ACTION_MANAGE_STORAGE

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACTION_MANAGE_STORAGE: String
```

Activity Action: Allows the user to manage their storage. This activity provides the ability to free up space on the device by deleting data such as apps.

If the sending application has a specific storage device or allocation size in mind, they can optionally define [EXTRA_UUID](https://developer.android.com/reference/kotlin/android/os/storage/StorageManager#EXTRA_UUID:kotlin.String) or [EXTRA_REQUESTED_BYTES](https://developer.android.com/reference/kotlin/android/os/storage/StorageManager#EXTRA_REQUESTED_BYTES:kotlin.String), respectively.

This intent should be launched using [Activity.startActivityForResult(Intent, int)](https://developer.android.com/reference/kotlin/android/app/Activity.html#startActivityForResult(android.content.Intent,%20kotlin.Int))so that the user knows which app is requesting the storage space. The returned result will be [Activity.RESULT_OK](https://developer.android.com/reference/kotlin/android/app/Activity.html#RESULT_OK:kotlin.Int) if the requested space was made available, or [Activity.RESULT_CANCELED](https://developer.android.com/reference/kotlin/android/app/Activity.html#RESULT_CANCELED:kotlin.Int) otherwise. 

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

- [#ACTION_MANAGE_STORAGE](https://developer.android.com/reference/kotlin/android/os/storage/StorageManager#ACTION_MANAGE_STORAGE:kotlin.String) 

### EXTRA_UUID

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_UUID: String
```

Extra [UUID](https://developer.android.com/reference/kotlin/java/util/UUID.html#) used to indicate the storage volume where an application is interested in allocating or managing disk space. 

 Value: "android.os.storage.extra.UUID"

**See Also**

- [#ACTION_MANAGE_STORAGE](https://developer.android.com/reference/kotlin/android/os/storage/StorageManager#ACTION_MANAGE_STORAGE:kotlin.String)
- [#UUID_DEFAULT](https://developer.android.com/reference/kotlin/android/os/storage/StorageManager#UUID_DEFAULT:java.util.UUID)
- [#getUuidForPath(File)](https://developer.android.com/reference/kotlin/android/os/storage/StorageManager#getUuidForPath(java.io.File))
- [android.content.Intent#putExtra(String, java.io.Serializable)](https://developer.android.com/reference/kotlin/android/content/Intent.html#putExtra(kotlin.String,%20java.io.Serializable))

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

Attempts to allocate disk space beyond the value returned by [getAllocatableBytes(java.util.UUID)](https://developer.android.com/reference/kotlin/android/os/storage/StorageManager#getAllocatableBytes(java.util.UUID))will fail.

This method guarantees that bytes have been allocated to the opened file, otherwise it will throw if fast allocation is not possible. Fast allocation is typically only supported in private app data directories, and on shared/external storage devices which are emulated.

If you're progressively allocating an unbounded amount of storage space (such as when recording a video) you should avoid calling this method more than once every 60 seconds. 
This method may take several seconds to complete, so it should only be called from a worker thread.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `fd` | [FileDescriptor](https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#)!:the open file that you'd like to allocate disk space for. |
| `bytes` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the number of bytes to allocate. This is the desired final size of the open file. If the open file is smaller than this requested size, it will be extended without modifying any existing contents. If the open file is larger than this requested size, it will be truncated. Value is a non-negative number of bytes. |

| Exceptions ||
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | when the storage device isn't present, or when it doesn't support allocating space, or if the device had trouble allocating the requested space. |

**See Also**

- [#isAllocationSupported(FileDescriptor)](https://developer.android.com/reference/kotlin/android/os/storage/StorageManager#isAllocationSupported(java.io.FileDescriptor))
- [android.os.Environment#isExternalStorageEmulated(File)](https://developer.android.com/reference/kotlin/android/os/Environment.html#isExternalStorageEmulated(java.io.File)) 

### allocateBytes

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun allocateBytes(
    storageUuid: UUID, 
    bytes: Long
): Unit
```

Allocate the requested number of bytes for your application to use on the given storage volume. This will cause the system to delete any cached files necessary to satisfy your request.

Attempts to allocate disk space beyond the value returned by [getAllocatableBytes(java.util.UUID)](https://developer.android.com/reference/kotlin/android/os/storage/StorageManager#getAllocatableBytes(java.util.UUID))will fail.

Since multiple apps can be running simultaneously, this method may be subject to race conditions. If possible, consider using [allocateBytes(java.io.FileDescriptor,long)](https://developer.android.com/reference/kotlin/android/os/storage/StorageManager#allocateBytes(java.io.FileDescriptor,%20kotlin.Long))which will guarantee that bytes are allocated to an opened file.

If you're progressively allocating an unbounded amount of storage space (such as when recording a video) you should avoid calling this method more than once every 60 seconds. 
This method may take several seconds to complete, so it should only be called from a worker thread.

| Parameters ||
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `storageUuid` | [UUID](https://developer.android.com/reference/kotlin/java/util/UUID.html#):the UUID of the storage volume where you'd like to allocate disk space. The UUID for a specific path can be obtained using [getUuidForPath(java.io.File)](https://developer.android.com/reference/kotlin/android/os/storage/StorageManager#getUuidForPath(java.io.File)). This value cannot be`null`. |
| `bytes` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the number of bytes to allocate. Value is a non-negative number of bytes. |

| Exceptions ||
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | when the storage device isn't present, or when it doesn't support allocating space, or if the device had trouble allocating the requested space. |

**See Also**

- [#getAllocatableBytes(UUID)](https://developer.android.com/reference/kotlin/android/os/storage/StorageManager#getAllocatableBytes(java.util.UUID)) 

### getAllocatableBytes

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getAllocatableBytes(storageUuid: UUID): Long
```

Return the maximum number of new bytes that your app can allocate for itself on the given storage volume. This value is typically larger than [File.getUsableSpace()](https://developer.android.com/reference/kotlin/java/io/File.html#getUsableSpace()), since the system may be willing to delete cached files to satisfy an allocation request. You can then allocate space for yourself using [allocateBytes(java.util.UUID,long)](https://developer.android.com/reference/kotlin/android/os/storage/StorageManager#allocateBytes(java.util.UUID,%20kotlin.Long))or [allocateBytes(java.io.FileDescriptor,long)](https://developer.android.com/reference/kotlin/android/os/storage/StorageManager#allocateBytes(java.io.FileDescriptor,%20kotlin.Long)).

This method is best used as a pre-flight check, such as deciding if there is enough space to store an entire music album before you allocate space for each audio file in the album. Attempts to allocate disk space beyond the returned value will fail.

If the returned value is not large enough for the data you'd like to persist, you can launch [ACTION_MANAGE_STORAGE](https://developer.android.com/reference/kotlin/android/os/storage/StorageManager#ACTION_MANAGE_STORAGE:kotlin.String) with the [EXTRA_UUID](https://developer.android.com/reference/kotlin/android/os/storage/StorageManager#EXTRA_UUID:kotlin.String) and [EXTRA_REQUESTED_BYTES](https://developer.android.com/reference/kotlin/android/os/storage/StorageManager#EXTRA_REQUESTED_BYTES:kotlin.String) options to help involve the user in freeing up disk space.

If you're progressively allocating an unbounded amount of storage space (such as when recording a video) you should avoid calling this method more than once every 30 seconds.

Note: if your app uses the`android:sharedUserId`manifest feature, then allocatable space for all packages in your shared UID is tracked together as a single unit.

This method may take several seconds to complete, so it should only be called from a worker thread. 
Value is a non-negative number of bytes.

| Parameters ||
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `storageUuid` | [UUID](https://developer.android.com/reference/kotlin/java/util/UUID.html#):the UUID of the storage volume where you're considering allocating disk space, since allocatable space can vary widely depending on the underlying storage device. The UUID for a specific path can be obtained using [getUuidForPath(java.io.File)](https://developer.android.com/reference/kotlin/android/os/storage/StorageManager#getUuidForPath(java.io.File)). This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the maximum number of new bytes that the calling app can allocate using [allocateBytes(java.util.UUID,long)](https://developer.android.com/reference/kotlin/android/os/storage/StorageManager#allocateBytes(java.util.UUID,%20kotlin.Long))or [allocateBytes(java.io.FileDescriptor,long)](https://developer.android.com/reference/kotlin/android/os/storage/StorageManager#allocateBytes(java.io.FileDescriptor,%20kotlin.Long)). Value is a non-negative number of bytes. |

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
| `storageUuid` | [UUID](https://developer.android.com/reference/kotlin/java/util/UUID.html#):the UUID of the storage volume that you're interested in. The UUID for a specific path can be obtained using [getUuidForPath(java.io.File)](https://developer.android.com/reference/kotlin/android/os/storage/StorageManager#getUuidForPath(java.io.File)). This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------|------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | Value is a non-negative number of bytes. |

| Exceptions ||
|-----------------------|---------------------------------------------------------------------------------|
| `java.io.IOException` | when the storage device isn't present, or when it doesn't support cache quotas. |

**See Also**

- [#getCacheSizeBytes(UUID)](https://developer.android.com/reference/kotlin/android/os/storage/StorageManager#getCacheSizeBytes(java.util.UUID)) 

### getCacheSizeBytes

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getCacheSizeBytes(storageUuid: UUID): Long
```

Return total size in bytes of all cached data belonging to the calling app on the given storage volume.

Cached data tracked by this method always includes [Context.getCacheDir()](https://developer.android.com/reference/kotlin/android/content/Context.html#getCacheDir())and [Context.getCodeCacheDir()](https://developer.android.com/reference/kotlin/android/content/Context.html#getCodeCacheDir()), and it also includes [Context.getExternalCacheDir()](https://developer.android.com/reference/kotlin/android/content/Context.html#getExternalCacheDir())if the primary shared/external storage is hosted on the same storage device as your private data.

Note: if your app uses the`android:sharedUserId`manifest feature, then cached data for all packages in your shared UID is tracked together as a single unit.

This method may take several seconds to complete, so it should only be called from a worker thread. 
Value is a non-negative number of bytes.

| Parameters ||
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `storageUuid` | [UUID](https://developer.android.com/reference/kotlin/java/util/UUID.html#):the UUID of the storage volume that you're interested in. The UUID for a specific path can be obtained using [getUuidForPath(java.io.File)](https://developer.android.com/reference/kotlin/android/os/storage/StorageManager#getUuidForPath(java.io.File)). This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------|------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | Value is a non-negative number of bytes. |

| Exceptions ||
|-----------------------|---------------------------------------------------------------------------------|
| `java.io.IOException` | when the storage device isn't present, or when it doesn't support cache quotas. |

**See Also**

- [#getCacheQuotaBytes(UUID)](https://developer.android.com/reference/kotlin/android/os/storage/StorageManager#getCacheQuotaBytes(java.util.UUID)) 

### getManageSpaceActivityIntent

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getManageSpaceActivityIntent(
    packageName: String, 
    requestCode: Int
): PendingIntent?
```

Returns a [PendingIntent](https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#) that can be used by Apps with [android.Manifest.permission#MANAGE_EXTERNAL_STORAGE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MANAGE_EXTERNAL_STORAGE:kotlin.String) permission to launch the manageSpaceActivity for any App that implements it, irrespective of its exported status.

Caller has the responsibility of supplying a valid packageName which has manageSpaceActivity implemented. 
Requires [android.Manifest.permission#MANAGE_EXTERNAL_STORAGE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MANAGE_EXTERNAL_STORAGE:kotlin.String)

| Parameters ||
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):package name for the App for which manageSpaceActivity is to be launched This value cannot be`null`. |
| `requestCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):for launching the activity |

| Return ||
|--------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [PendingIntent](https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#)? | PendingIntent to launch the manageSpaceActivity if successful, null if the packageName doesn't have a manageSpaceActivity. |

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

Return the primary shared/external storage volume available to the current user. This volume is the same storage device returned by [Environment.getExternalStorageDirectory()](https://developer.android.com/reference/kotlin/android/os/Environment.html#getExternalStorageDirectory())and [Context.getExternalFilesDir(String)](https://developer.android.com/reference/kotlin/android/content/Context.html#getExternalFilesDir(kotlin.String)).

| Return ||
|--------------------------------------------------------------------------------------------------|-----------------------------|
| [StorageVolume](https://developer.android.com/reference/kotlin/android/os/storage/StorageVolume) | This value cannot be`null`. |

### getRecentStorageVolumes

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getRecentStorageVolumes(): MutableList<StorageVolume!>
```

Return the list of shared/external storage volumes both currently and recently available to the calling user.

Recently available storage volumes are likely to reappear in the future, so apps are encouraged to preserve any indexed metadata related to these volumes to optimize user experiences.

| Return ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [StorageVolume](https://developer.android.com/reference/kotlin/android/os/storage/StorageVolume)!> | This value cannot be`null`. |

### getStorageVolume

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getStorageVolume(uri: Uri): StorageVolume
```

Return the [StorageVolume](https://developer.android.com/reference/kotlin/android/os/storage/StorageVolume) that contains the given [MediaStore](https://developer.android.com/reference/kotlin/android/provider/MediaStore.html#) item.

| Parameters ||
|-------|---------------------------------------------------------------------------------------------------------|
| `uri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#):This value cannot be`null`. |

| Return ||
|--------------------------------------------------------------------------------------------------|-----------------------------|
| [StorageVolume](https://developer.android.com/reference/kotlin/android/os/storage/StorageVolume) | This value cannot be`null`. |

### getStorageVolume

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getStorageVolume(file: File): StorageVolume?
```

Return the [StorageVolume](https://developer.android.com/reference/kotlin/android/os/storage/StorageVolume) that contains the given file, or`null`if none.

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------|
| `file` | [File](https://developer.android.com/reference/kotlin/java/io/File.html#):This value cannot be`null`. |

### getStorageVolumes

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getStorageVolumes(): MutableList<StorageVolume!>
```

Return the list of shared/external storage volumes currently available to the calling user.

These storage volumes are actively attached to the device, but may be in any mount state, as returned by [StorageVolume.getState()](https://developer.android.com/reference/kotlin/android/os/storage/StorageVolume#getState()). Returns both the primary shared storage device and any attached external volumes, including SD cards and USB drives.

| Return ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [StorageVolume](https://developer.android.com/reference/kotlin/android/os/storage/StorageVolume)!> | This value cannot be`null`. |

### getStorageVolumesIncludingSharedProfiles

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getStorageVolumesIncludingSharedProfiles(): MutableList<StorageVolume!>
```

Return the list of shared/external storage volumes currently available to the calling user and the user it shares media with. Please refer to [multi-user support](https://source.android.com/compatibility/12/android-12-cdd#95_multi-user_support) for more details.

This is similar to [StorageManager.getStorageVolumes()](https://developer.android.com/reference/kotlin/android/os/storage/StorageManager#getStorageVolumes())except that the result also includes the volumes belonging to any user it shares media with 
Requires [android.Manifest.permission#MANAGE_EXTERNAL_STORAGE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MANAGE_EXTERNAL_STORAGE:kotlin.String)

| Return ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [StorageVolume](https://developer.android.com/reference/kotlin/android/os/storage/StorageVolume)!> | This value cannot be`null`. |

### getUuidForPath

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getUuidForPath(path: File): UUID
```

Return a UUID identifying the storage volume that hosts the given filesystem path.

If this path is hosted by the default internal storage of the device at [Environment.getDataDirectory()](https://developer.android.com/reference/kotlin/android/os/Environment.html#getDataDirectory()), the returned value will be [UUID_DEFAULT](https://developer.android.com/reference/kotlin/android/os/storage/StorageManager#UUID_DEFAULT:java.util.UUID).

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------|
| `path` | [File](https://developer.android.com/reference/kotlin/java/io/File.html#):This value cannot be`null`. |

| Return ||
|-----------------------------------------------------------------------------|-----------------------------|
| [UUID](https://developer.android.com/reference/kotlin/java/util/UUID.html#) | This value cannot be`null`. |

| Exceptions ||
|-----------------------|-----------------------------------------------------------------------------------------------------|
| `java.io.IOException` | when the storage device hosting the given path isn't present, or when it doesn't have a valid UUID. |

### isAllocationSupported

Added in [API level 27](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isAllocationSupported(fd: FileDescriptor): Boolean
```

Test if the given file descriptor supports allocation of disk space using [allocateBytes(java.io.FileDescriptor,long)](https://developer.android.com/reference/kotlin/android/os/storage/StorageManager#allocateBytes(java.io.FileDescriptor,%20kotlin.Long)).

| Parameters ||
|------|---------------------------------------------------------------------------------------------------------------------------|
| `fd` | [FileDescriptor](https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#):This value cannot be`null`. |

### isCacheBehaviorGroup

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isCacheBehaviorGroup(path: File!): Boolean
```

Read the current value set by [setCacheBehaviorGroup(java.io.File,boolean)](https://developer.android.com/reference/kotlin/android/os/storage/StorageManager#setCacheBehaviorGroup(java.io.File,%20kotlin.Boolean)). 

### isCacheBehaviorTombstone

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isCacheBehaviorTombstone(path: File!): Boolean
```

Read the current value set by [setCacheBehaviorTombstone(java.io.File,boolean)](https://developer.android.com/reference/kotlin/android/os/storage/StorageManager#setCacheBehaviorTombstone(java.io.File,%20kotlin.Boolean)). 

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

The OBB will remain mounted for as long as the StorageManager reference is held by the application. As soon as this reference is lost, the OBBs in use will be unmounted. The [OnObbStateChangeListener](https://developer.android.com/reference/kotlin/android/os/storage/OnObbStateChangeListener) registered with this call will receive the success or failure of this operation.

*Note:*you can only mount OBB files for which the OBB tag on the file matches a package ID that is owned by the calling program's UID. That is, shared UID applications can attempt to mount any other application's OBB that shares its UID.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `rawPath` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the path to the OBB file |
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:must be`null`. Previously, some Android device implementations accepted a non-`null`key to mount an encrypted OBB file. However, this never worked reliably and is no longer supported. |
| `listener` | [OnObbStateChangeListener](https://developer.android.com/reference/kotlin/android/os/storage/OnObbStateChangeListener)!:will receive the success or failure of the operation |
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

Opens a seekable [ParcelFileDescriptor](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#) that proxies all low-level I/O requests back to the given [ProxyFileDescriptorCallback](https://developer.android.com/reference/kotlin/android/os/ProxyFileDescriptorCallback.html#).

This can be useful when you want to provide quick access to a large file that isn't backed by a real file on disk, such as a file on a network share, cloud storage service, etc. As an example, you could respond to a [ContentResolver.openFileDescriptor(android.net.Uri, String)](https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#openFileDescriptor(android.net.Uri,%20kotlin.String))request by returning a [ParcelFileDescriptor](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#) created with this method, and then stream the content on-demand as requested.

Another useful example might be where you have an encrypted file that you're willing to decrypt on-demand, but where you want to avoid persisting the cleartext version.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `mode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The desired access mode, must be one of [ParcelFileDescriptor.MODE_READ_ONLY](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#MODE_READ_ONLY:kotlin.Int), [ParcelFileDescriptor.MODE_WRITE_ONLY](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#MODE_WRITE_ONLY:kotlin.Int), or [ParcelFileDescriptor.MODE_READ_WRITE](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#MODE_READ_WRITE:kotlin.Int) |
| `callback` | [ProxyFileDescriptorCallback](https://developer.android.com/reference/kotlin/android/os/ProxyFileDescriptorCallback.html#)!:Callback to process file operation requests issued on returned file descriptor. |
| `handler` | [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#)!:Handler that invokes callback methods. |
| --- | --- |

| Return ||
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| [ParcelFileDescriptor](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#) | Seekable ParcelFileDescriptor. This value cannot be`null`. |

### registerStorageVolumeCallback

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun registerStorageVolumeCallback(
    executor: Executor, 
    callback: StorageManager.StorageVolumeCallback
): Unit
```

Registers the given callback to listen for [StorageVolume](https://developer.android.com/reference/kotlin/android/os/storage/StorageVolume) changes.

For example, this can be used to detect when a volume changes to the [Environment.MEDIA_MOUNTED](https://developer.android.com/reference/kotlin/android/os/Environment.html#MEDIA_MOUNTED:kotlin.String) or [Environment.MEDIA_UNMOUNTED](https://developer.android.com/reference/kotlin/android/os/Environment.html#MEDIA_UNMOUNTED:kotlin.String) states.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#):Callback and listener events are dispatched through this [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()). Otherwise, provide an [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#) that dispatches to an appropriate thread. This value cannot be`null`. |
| `callback` | [StorageManager.StorageVolumeCallback](https://developer.android.com/reference/kotlin/android/os/storage/StorageManager.StorageVolumeCallback):This value cannot be`null`. |

**See Also**

- [android.os.storage.StorageManager#unregisterStorageVolumeCallback](https://developer.android.com/reference/kotlin/android/os/storage/StorageManager#unregisterStorageVolumeCallback(android.os.storage.StorageManager.StorageVolumeCallback)) 

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

When enabled, the*newest* [File.lastModified()](https://developer.android.com/reference/kotlin/java/io/File.html#lastModified())value of any contained files is considered the modified time of the entire directory.

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

The [OnObbStateChangeListener](https://developer.android.com/reference/kotlin/android/os/storage/OnObbStateChangeListener) registered with this call will receive the success or failure of this operation.

*Note:*you can only mount OBB files for which the OBB tag on the file matches a package ID that is owned by the calling program's UID. That is, shared UID applications can obtain access to any other application's OBB that shares its UID.

<br />

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `rawPath` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:path to the OBB file |
| `force` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):whether to kill any programs using this in order to unmount it |
| `listener` | [OnObbStateChangeListener](https://developer.android.com/reference/kotlin/android/os/storage/OnObbStateChangeListener)!:will receive the success or failure of the operation |
| --- | --- |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | whether the unmount call was successfully queued or not |

### unregisterStorageVolumeCallback

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun unregisterStorageVolumeCallback(callback: StorageManager.StorageVolumeCallback): Unit
```

Unregisters the given callback from listening for [StorageVolume](https://developer.android.com/reference/kotlin/android/os/storage/StorageVolume) changes.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `callback` | [StorageManager.StorageVolumeCallback](https://developer.android.com/reference/kotlin/android/os/storage/StorageManager.StorageVolumeCallback):This value cannot be`null`. |

**See Also**

- [android.os.storage.StorageManager#registerStorageVolumeCallback](https://developer.android.com/reference/kotlin/android/os/storage/StorageManager#registerStorageVolumeCallback(java.util.concurrent.Executor,%20android.os.storage.StorageManager.StorageVolumeCallback))

## Properties

### UUID_DEFAULT

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val UUID_DEFAULT: UUID!
```

UUID representing the default internal storage of this device which provides [Environment.getDataDirectory()](https://developer.android.com/reference/kotlin/android/os/Environment.html#getDataDirectory()).

This value is constant across all devices and it will never change, and thus it cannot be used to uniquely identify a particular physical device. 
**See Also**

- [#getUuidForPath(File)](https://developer.android.com/reference/kotlin/android/os/storage/StorageManager#getUuidForPath(java.io.File))
- [android.content.pm.ApplicationInfo#storageUuid](https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo.html#storageUuid:java.util.UUID)
