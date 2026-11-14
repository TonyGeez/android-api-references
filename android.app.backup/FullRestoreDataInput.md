# FullRestoreDataInput

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# FullRestoreDataInput

Kotlin| [Java](FullRestoreDataInput.md) 
| --- | --- |

```
open class FullRestoreDataInput
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.app.backup.FullRestoreDataInput](FullRestoreDataInput.md) |

Provides the interface through which a [BackupAgent](BackupAgent.md) reads entire files from a full backup data set, via its [BackupAgent.onRestoreFile(FullRestoreDataInput)](BackupAgent.md))method.

## Summary

| Public methods ||
|------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getAppVersionCode](FullRestoreDataInput.md))`()` The version code of the app that created the backup. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getContentVersion](FullRestoreDataInput.md))`()` Content version set by the source device during a cross-platform transfer. |
| open [ParcelFileDescriptor](../android.os/ParcelFileDescriptor.md) | [getData](FullRestoreDataInput.md))`()` Read-only file descriptor containing the file data. |
| --- | --- |
| open [File](../java.io/File.md) | [getDestination](FullRestoreDataInput.md))`()` The file on disk to be restored with the given data. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getMode](FullRestoreDataInput.md))`()` The access mode to be assigned to the destination after its data is written. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getModificationTimeSeconds](FullRestoreDataInput.md))`()` A timestamp in the standard Unix epoch that represents the last modification time of the file when it was backed up, suitable to be assigned to the file after its data is written. |
| --- | --- |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getSize](FullRestoreDataInput.md))`()` Size of the file in bytes. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getTransportFlags](FullRestoreDataInput.md))`()` Flags with additional information about the transport. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getType](FullRestoreDataInput.md))`()` The kind of file system object being restored. |
| --- | --- |

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
| [ParcelFileDescriptor](../android.os/ParcelFileDescriptor.md) | This value cannot be`null`. |

### getDestination

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDestination(): File
```

The file on disk to be restored with the given data.

| Return ||
|---------------------------------------------------------------------------|-----------------------------|
| [File](../java.io/File.md) | This value cannot be`null`. |

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

Flags with additional information about the transport. The transport flags that can be set are defined in [BackupAgent](BackupAgent.md).

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is either`0`or a combination of [android.app.backup.BackupAgent#FLAG_CLIENT_SIDE_ENCRYPTION_ENABLED](BackupAgent.md), [android.app.backup.BackupAgent#FLAG_DEVICE_TO_DEVICE_TRANSFER](BackupAgent.md), android.app.backup.BackupAgent.FLAG_FAKE_CLIENT_SIDE_ENCRYPTION_ENABLED, and [android.app.backup.BackupAgent#FLAG_CROSS_PLATFORM_DATA_TRANSFER_IOS](BackupAgent.md) |

### getType

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getType(): Int
```

The kind of file system object being restored. This will be either [android.app.backup.BackupAgent#TYPE_FILE](BackupAgent.md) or [BackupAgent.TYPE_DIRECTORY](BackupAgent.md).

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is android.app.backup.BackupAgent.TYPE_EOF, [android.app.backup.BackupAgent#TYPE_FILE](BackupAgent.md), [android.app.backup.BackupAgent#TYPE_DIRECTORY](BackupAgent.md), or android.app.backup.BackupAgent.TYPE_SYMLINK |
