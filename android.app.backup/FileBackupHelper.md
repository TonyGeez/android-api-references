# FileBackupHelper

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# FileBackupHelper

Kotlin| [Java](FileBackupHelper.md) 
| --- | --- |

```
open class FileBackupHelper : BackupHelper
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.app.backup.FileBackupHelper](FileBackupHelper.md) |

A helper class that can be used in conjunction with [android.app.backup.BackupAgentHelper](BackupAgentHelper.md) to manage the backup of a set of files. Whenever backup is performed, all files changed since the last backup will be saved in their entirety. When backup first occurs, every file in the list provided to [FileBackupHelper](FileBackupHelper.md))will be backed up.

During restore, if the helper encounters data for a file that was not specified when the FileBackupHelper object was constructed, that data will be ignored.

**Note:**This should be used only with small configuration files, not large binary files.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [FileBackupHelper](FileBackupHelper.md))`(`context:` ` [Context](../android.content/Context.md)!`, `vararg` `files:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Construct a helper to manage backup/restore of entire files within the application's data directory hierarchy. |

| Public methods ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [performBackup](FileBackupHelper.md))`(`oldState:` ` [ParcelFileDescriptor](../android.os/ParcelFileDescriptor.md)!`, `data:` ` [BackupDataOutput](BackupDataOutput.md)!`, `newState:` ` [ParcelFileDescriptor](../android.os/ParcelFileDescriptor.md)!`)` Based on`oldState`, determine which of the files from the application's data directory need to be backed up, write them to the data stream, and fill in`newState`with the state as it exists now. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [restoreEntity](FileBackupHelper.md))`(`data:` ` [BackupDataInputStream](BackupDataInputStream.md)!`)` Restore one record \[representing a single file\] from the restore dataset. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeNewStateDescription](FileBackupHelper.md))`(`fd:` ` [ParcelFileDescriptor](../android.os/ParcelFileDescriptor.md)!`)` <br /> |
| --- | --- |

## Public constructors

### FileBackupHelper

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
FileBackupHelper(
    context: Context!, 
    vararg files: String!)
```

Construct a helper to manage backup/restore of entire files within the application's data directory hierarchy.

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android.content/Context.md)!:The backup agent's Context object |
| `files` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:A list of the files to be backed up or restored. |

## Public methods

### performBackup

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun performBackup(
    oldState: ParcelFileDescriptor!, 
    data: BackupDataOutput!, 
    newState: ParcelFileDescriptor!
): Unit
```

Based on`oldState`, determine which of the files from the application's data directory need to be backed up, write them to the data stream, and fill in`newState`with the state as it exists now. When`oldState`is`null`, all the files will be backed up.

This should only be called directly from within the [BackupAgentHelper](BackupAgentHelper.md) implementation. See [android.app.backup.BackupAgent#onBackup(ParcelFileDescriptor, BackupDataOutput, ParcelFileDescriptor)](BackupAgent.md))for a description of parameter meanings.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `oldState` | [ParcelFileDescriptor](../android.os/ParcelFileDescriptor.md)!:An open, read-only [android.os.ParcelFileDescriptor](../android.os/ParcelFileDescriptor.md) pointing to the last backup state provided by the application. May be`null`, in which case no prior state is being provided and the application should perform a full backup. |
| `data` | [BackupDataOutput](BackupDataOutput.md)!:An open, read/write [BackupDataOutput](BackupDataOutput.md) pointing to the backup data destination. Typically the application will use backup helper classes to write to this file. |
| `newState` | [ParcelFileDescriptor](../android.os/ParcelFileDescriptor.md)!:An open, read/write [android.os.ParcelFileDescriptor](../android.os/ParcelFileDescriptor.md) pointing to an empty file. The application should record the final backup state here after writing the requested data to the`data`output stream. |
| --- | --- |

### restoreEntity

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun restoreEntity(data: BackupDataInputStream!): Unit
```

Restore one record \[representing a single file\] from the restore dataset.

This should only be called directly from within the [BackupAgentHelper](BackupAgentHelper.md) implementation.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `data` | [BackupDataInputStream](BackupDataInputStream.md)!:An open [BackupDataInputStream](BackupDataInputStream.md) from which the backup data can be read. |

### writeNewStateDescription

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun writeNewStateDescription(fd: ParcelFileDescriptor!): Unit
```

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `newState` | A [android.os.ParcelFileDescriptor](../android.os/ParcelFileDescriptor.md) to which the new state will be written. |
