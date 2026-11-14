# StorageStatsManager

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# StorageStatsManager

Kotlin| [Java](../android/app/usage/StorageStatsManager.md) 
| --- | --- |

```
open class StorageStatsManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.app.usage.StorageStatsManager](../android/app/usage/StorageStatsManager.md) |

Access to detailed storage statistics. This provides a summary of how apps, users, and external/shared storage is utilizing disk space.

Note: no permissions are required when calling these APIs for your own package or UID. However, requesting details for any other package requires the`android.Manifest.permission#PACKAGE_USAGE_STATS`permission, which is a system-level permission that will not be granted to normal apps. Declaring that permission expresses your intention to use this API and an end user can then choose to grant this permission through the Settings application.

## Summary

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getFreeBytes](../android/app/usage/StorageStatsManager.md))`(`storageUuid:` ` [UUID](../java/util/UUID.md)`)` Return the free space on the requested storage volume. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getTotalBytes](../android/app/usage/StorageStatsManager.md))`(`storageUuid:` ` [UUID](../java/util/UUID.md)`)` Return the total size of the underlying physical media that is hosting this storage volume. |
| open [ExternalStorageStats](../android/app/usage/ExternalStorageStats.md) | [queryExternalStatsForUser](../android/app/usage/StorageStatsManager.md))`(`storageUuid:` ` [UUID](../java/util/UUID.md)`, `user:` ` [UserHandle](../android/os/UserHandle.md)`)` Return shared/external storage statistics for a specific [UserHandle](../android/os/UserHandle.md) on the requested storage volume. |
| --- | --- |
| open [StorageStats](../android/app/usage/StorageStats.md) | [queryStatsForPackage](../android/app/usage/StorageStatsManager.md))`(`storageUuid:` ` [UUID](../java/util/UUID.md)`, `packageName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `user:` ` [UserHandle](../android/os/UserHandle.md)`)` Return storage statistics for a specific package on the requested storage volume. |
| open [StorageStats](../android/app/usage/StorageStats.md) | [queryStatsForUid](../android/app/usage/StorageStatsManager.md))`(`storageUuid:` ` [UUID](../java/util/UUID.md)`, `uid:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return storage statistics for a specific UID on the requested storage volume. |
| open [StorageStats](../android/app/usage/StorageStats.md) | [queryStatsForUser](../android/app/usage/StorageStatsManager.md))`(`storageUuid:` ` [UUID](../java/util/UUID.md)`, `user:` ` [UserHandle](../android/os/UserHandle.md)`)` Return storage statistics for a specific [UserHandle](../android/os/UserHandle.md) on the requested storage volume. |
| --- | --- |

## Public methods

### getFreeBytes

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getFreeBytes(storageUuid: UUID): Long
```

Return the free space on the requested storage volume.

This value is best suited for visual display to end users, since it's designed to reflect both unused space*and*and cached space that could be reclaimed by the system.

Apps making logical decisions about disk space should always use [StorageManager.getAllocatableBytes(UUID)](../android/os/storage/StorageManager.md))instead of this value. 
This method may take several seconds to complete, so it should only be called from a worker thread. 
Value is a non-negative number of bytes.

| Parameters ||
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `storageUuid` | [UUID](../java/util/UUID.md):the UUID of the storage volume you're interested in, such as [StorageManager.UUID_DEFAULT](../android/os/storage/StorageManager.md). This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------|------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | Value is a non-negative number of bytes. |

| Exceptions ||
|-----------------------|----------------------------------------|
| `java.io.IOException` | when the storage device isn't present. |

### getTotalBytes

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getTotalBytes(storageUuid: UUID): Long
```

Return the total size of the underlying physical media that is hosting this storage volume.

This value is best suited for visual display to end users, since it's designed to reflect the total storage size advertised in a retail environment.

Apps making logical decisions about disk space should always use [File.getTotalSpace()](../java/io/File.md))instead of this value. 
This method may take several seconds to complete, so it should only be called from a worker thread. 
Value is a non-negative number of bytes.

| Parameters ||
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `storageUuid` | [UUID](../java/util/UUID.md):the UUID of the storage volume you're interested in, such as [StorageManager.UUID_DEFAULT](../android/os/storage/StorageManager.md). This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------|------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | Value is a non-negative number of bytes. |

| Exceptions ||
|-----------------------|----------------------------------------|
| `java.io.IOException` | when the storage device isn't present. |

### queryExternalStatsForUser

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun queryExternalStatsForUser(
    storageUuid: UUID, 
    user: UserHandle
): ExternalStorageStats
```

Return shared/external storage statistics for a specific [UserHandle](../android/os/UserHandle.md) on the requested storage volume.

Note: this API requires the`android.Manifest.permission#PACKAGE_USAGE_STATS`permission, which is a system-level permission that will not be granted to normal apps. Declaring that permission expresses your intention to use this API and an end user can then choose to grant this permission through the Settings application.

This method may take several seconds to complete, so it should only be called from a worker thread.

| Parameters ||
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `storageUuid` | [UUID](../java/util/UUID.md):the UUID of the storage volume you're interested in, such as [StorageManager.UUID_DEFAULT](../android/os/storage/StorageManager.md). This value cannot be`null`. |
| `user` | [UserHandle](../android/os/UserHandle.md):This value cannot be`null`. |

| Return ||
|---------------------------------------------------------------------------------------------------------------|-----------------------------|
| [ExternalStorageStats](../android/app/usage/ExternalStorageStats.md) | This value cannot be`null`. |

| Exceptions ||
|-----------------------|----------------------------------------|
| `java.io.IOException` | when the storage device isn't present. |

**See Also**

- [android.os.Process#myUserHandle()](../android/os/Process.md)) 

### queryStatsForPackage

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun queryStatsForPackage(
    storageUuid: UUID, 
    packageName: String, 
    user: UserHandle
): StorageStats
```

Return storage statistics for a specific package on the requested storage volume.

Note: no permissions are required when calling this API for your own package. However, requesting details for any other package requires the`android.Manifest.permission#PACKAGE_USAGE_STATS`permission, which is a system-level permission that will not be granted to normal apps. Declaring that permission expresses your intention to use this API and an end user can then choose to grant this permission through the Settings application.

Note: if the requested package uses the`android:sharedUserId`manifest feature, this call will be forced into a slower manual calculation path. If possible, consider always using [queryStatsForUid(java.util.UUID,int)](../android/app/usage/StorageStatsManager.md)), which is typically faster.

This method may take several seconds to complete, so it should only be called from a worker thread.

| Parameters ||
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `storageUuid` | [UUID](../java/util/UUID.md):the UUID of the storage volume you're interested in, such as [StorageManager.UUID_DEFAULT](../android/os/storage/StorageManager.md). This value cannot be`null`. |
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):the package name you're interested in. This value cannot be`null`. |
| `user` | [UserHandle](../android/os/UserHandle.md):the user you're interested in. This value cannot be`null`. |
| --- | --- |

| Return ||
|-----------------------------------------------------------------------------------------------|-----------------------------|
| [StorageStats](../android/app/usage/StorageStats.md) | This value cannot be`null`. |

| Exceptions ||
|-----------------------------------------------------------|-------------------------------------------------------------------------|
| `android.content.pm.PackageManager.NameNotFoundException` | when the requested package name isn't installed for the requested user. |
| `java.io.IOException` | when the storage device isn't present. |

**See Also**

- [android.content.pm.ApplicationInfo#storageUuid](../android/content/pm/ApplicationInfo.md)
- [android.content.pm.PackageInfo#packageName](../android/content/pm/PackageInfo.md) 

### queryStatsForUid

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun queryStatsForUid(
    storageUuid: UUID, 
    uid: Int
): StorageStats
```

Return storage statistics for a specific UID on the requested storage volume.

Note: no permissions are required when calling this API for your own UID. However, requesting details for any other UID requires the`android.Manifest.permission#PACKAGE_USAGE_STATS`permission, which is a system-level permission that will not be granted to normal apps. Declaring that permission expresses your intention to use this API and an end user can then choose to grant this permission through the Settings application.

This method may take several seconds to complete, so it should only be called from a worker thread.

| Parameters ||
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `storageUuid` | [UUID](../java/util/UUID.md):the UUID of the storage volume you're interested in, such as [StorageManager.UUID_DEFAULT](../android/os/storage/StorageManager.md). This value cannot be`null`. |
| `uid` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the UID you're interested in. |

| Return ||
|-----------------------------------------------------------------------------------------------|-----------------------------|
| [StorageStats](../android/app/usage/StorageStats.md) | This value cannot be`null`. |

| Exceptions ||
|-----------------------|----------------------------------------|
| `java.io.IOException` | when the storage device isn't present. |

**See Also**

- [android.content.pm.ApplicationInfo#storageUuid](../android/content/pm/ApplicationInfo.md)
- [android.content.pm.ApplicationInfo#uid](../android/content/pm/ApplicationInfo.md) 

### queryStatsForUser

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun queryStatsForUser(
    storageUuid: UUID, 
    user: UserHandle
): StorageStats
```

Return storage statistics for a specific [UserHandle](../android/os/UserHandle.md) on the requested storage volume.

Note: this API requires the`android.Manifest.permission#PACKAGE_USAGE_STATS`permission, which is a system-level permission that will not be granted to normal apps. Declaring that permission expresses your intention to use this API and an end user can then choose to grant this permission through the Settings application.

This method may take several seconds to complete, so it should only be called from a worker thread.

| Parameters ||
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `storageUuid` | [UUID](../java/util/UUID.md):the UUID of the storage volume you're interested in, such as [StorageManager.UUID_DEFAULT](../android/os/storage/StorageManager.md). This value cannot be`null`. |
| `user` | [UserHandle](../android/os/UserHandle.md):the user you're interested in. This value cannot be`null`. |

| Return ||
|-----------------------------------------------------------------------------------------------|-----------------------------|
| [StorageStats](../android/app/usage/StorageStats.md) | This value cannot be`null`. |

| Exceptions ||
|-----------------------|----------------------------------------|
| `java.io.IOException` | when the storage device isn't present. |

**See Also**

- [android.os.Process#myUserHandle()](../android/os/Process.md))
