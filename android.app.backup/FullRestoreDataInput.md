# FullRestoreDataInput

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# FullRestoreDataInput

Kotlin| [Java](https://developer.android.com/reference/android/app/backup/FullRestoreDataInput "View this page in Java") 

```
open class FullRestoreDataInput
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.app.backup.FullRestoreDataInput](https://developer.android.com/reference/kotlin/android/app/backup/FullRestoreDataInput#) |

Provides the interface through which a [BackupAgent](https://developer.android.com/reference/kotlin/android/app/backup/BackupAgent) reads entire files from a full backup data set, via its [BackupAgent.onRestoreFile(FullRestoreDataInput)](https://developer.android.com/reference/kotlin/android/app/backup/BackupAgent#onRestoreFile(android.app.backup.FullRestoreDataInput))method.

## Summary

| Public methods ||
|------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getAppVersionCode](https://developer.android.com/reference/kotlin/android/app/backup/FullRestoreDataInput#getAppVersionCode())`()` The version code of the app that created the backup. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getContentVersion](https://developer.android.com/reference/kotlin/android/app/backup/FullRestoreDataInput#getContentVersion())`()` Content version set by the source device during a cross-platform transfer. |
| open [ParcelFileDescriptor](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#) | [getData](https://developer.android.com/reference/kotlin/android/app/backup/FullRestoreDataInput#getData())`()` Read-only file descriptor containing the file data. |
| open [File](https://developer.android.com/reference/kotlin/java/io/File.html#) | [getDestination](https://developer.android.com/reference/kotlin/android/app/backup/FullRestoreDataInput#getDestination())`()` The file on disk to be restored with the given data. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getMode](https://developer.android.com/reference/kotlin/android/app/backup/FullRestoreDataInput#getMode())`()` The access mode to be assigned to the destination after its data is written. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getModificationTimeSeconds](https://developer.android.com/reference/kotlin/android/app/backup/FullRestoreDataInput#getModificationTimeSeconds())`()` A timestamp in the standard Unix epoch that represents the last modification time of the file when it was backed up, suitable to be assigned to the file after its data is written. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getSize](https://developer.android.com/reference/kotlin/android/app/backup/FullRestoreDataInput#getSize())`()` Size of the file in bytes. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getTransportFlags](https://developer.android.com/reference/kotlin/android/app/backup/FullRestoreDataInput#getTransportFlags())`()` Flags with additional information about the transport. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getType](https://developer.android.com/reference/kotlin/android/app/backup/FullRestoreDataInput#getType())`()` The kind of file system object being restored. |

## Public methods

### getAppVersionCode

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getAppVersionCode(): Long
```

The version code of the app that created the backup. 

### getContentVersion

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getContentVersion(): String
```

Content version set by the source device during a cross-platform transfer. Empty string if the source device did not provide a content version.

| Return ||
|----------------------------------------------------------------------------------|-----------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | This value cannot be`null`. |

### getData

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getData(): ParcelFileDescriptor
```

Read-only file descriptor containing the file data.

| Return ||
|--------------------------------------------------------------------------------------------------------------|-----------------------------|
| [ParcelFileDescriptor](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#) | This value cannot be`null`. |

### getDestination

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDestination(): File
```

The file on disk to be restored with the given data.

| Return ||
|---------------------------------------------------------------------------|-----------------------------|
| [File](https://developer.android.com/reference/kotlin/java/io/File.html#) | This value cannot be`null`. |

### getMode

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getMode(): Long
```

The access mode to be assigned to the destination after its data is written. This is in the standard format used by`chmod()`. 

### getModificationTimeSeconds

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getModificationTimeSeconds(): Long
```

A timestamp in the standard Unix epoch that represents the last modification time of the file when it was backed up, suitable to be assigned to the file after its data is written. 
Value is a non-negative timestamp measured as the number of seconds since 1970-01-01T00:00:00Z.

| Return ||
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | Value is a non-negative timestamp measured as the number of seconds since 1970-01-01T00:00:00Z. |

### getSize

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSize(): Long
```

Size of the file in bytes. 

### getTransportFlags

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getTransportFlags(): Int
```

Flags with additional information about the transport. The transport flags that can be set are defined in [BackupAgent](https://developer.android.com/reference/kotlin/android/app/backup/BackupAgent).

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is either`0`or a combination of [android.app.backup.BackupAgent#FLAG_CLIENT_SIDE_ENCRYPTION_ENABLED](https://developer.android.com/reference/kotlin/android/app/backup/BackupAgent#FLAG_CLIENT_SIDE_ENCRYPTION_ENABLED:kotlin.Int), [android.app.backup.BackupAgent#FLAG_DEVICE_TO_DEVICE_TRANSFER](https://developer.android.com/reference/kotlin/android/app/backup/BackupAgent#FLAG_DEVICE_TO_DEVICE_TRANSFER:kotlin.Int), android.app.backup.BackupAgent.FLAG_FAKE_CLIENT_SIDE_ENCRYPTION_ENABLED, and [android.app.backup.BackupAgent#FLAG_CROSS_PLATFORM_DATA_TRANSFER_IOS](https://developer.android.com/reference/kotlin/android/app/backup/BackupAgent#FLAG_CROSS_PLATFORM_DATA_TRANSFER_IOS:kotlin.Int) |

### getType

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getType(): Int
```

The kind of file system object being restored. This will be either [android.app.backup.BackupAgent#TYPE_FILE](https://developer.android.com/reference/kotlin/android/app/backup/BackupAgent#TYPE_FILE:kotlin.Int) or [BackupAgent.TYPE_DIRECTORY](https://developer.android.com/reference/kotlin/android/app/backup/BackupAgent#TYPE_DIRECTORY:kotlin.Int).

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is android.app.backup.BackupAgent.TYPE_EOF, [android.app.backup.BackupAgent#TYPE_FILE](https://developer.android.com/reference/kotlin/android/app/backup/BackupAgent#TYPE_FILE:kotlin.Int), [android.app.backup.BackupAgent#TYPE_DIRECTORY](https://developer.android.com/reference/kotlin/android/app/backup/BackupAgent#TYPE_DIRECTORY:kotlin.Int), or android.app.backup.BackupAgent.TYPE_SYMLINK |
