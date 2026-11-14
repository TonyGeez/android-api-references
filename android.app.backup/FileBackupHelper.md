# FileBackupHelper

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# FileBackupHelper

Kotlin| [Java](https://developer.android.com/reference/android/app/backup/FileBackupHelper "View this page in Java") 
| --- | --- |

```
open class FileBackupHelper : BackupHelper
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.app.backup.FileBackupHelper](https://developer.android.com/reference/kotlin/android/app/backup/FileBackupHelper#) |

A helper class that can be used in conjunction with [android.app.backup.BackupAgentHelper](https://developer.android.com/reference/kotlin/android/app/backup/BackupAgentHelper) to manage the backup of a set of files. Whenever backup is performed, all files changed since the last backup will be saved in their entirety. When backup first occurs, every file in the list provided to [FileBackupHelper](https://developer.android.com/reference/kotlin/android/app/backup/FileBackupHelper#FileBackupHelper(android.content.Context,%20kotlin.String))will be backed up.

During restore, if the helper encounters data for a file that was not specified when the FileBackupHelper object was constructed, that data will be ignored.

**Note:**This should be used only with small configuration files, not large binary files.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [FileBackupHelper](https://developer.android.com/reference/kotlin/android/app/backup/FileBackupHelper#FileBackupHelper(android.content.Context,%20kotlin.String))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`, `vararg` `files:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Construct a helper to manage backup/restore of entire files within the application's data directory hierarchy. |

| Public methods ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [performBackup](https://developer.android.com/reference/kotlin/android/app/backup/FileBackupHelper#performBackup(android.os.ParcelFileDescriptor,%20android.app.backup.BackupDataOutput,%20android.os.ParcelFileDescriptor))`(`oldState:` ` [ParcelFileDescriptor](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#)!`, `data:` ` [BackupDataOutput](https://developer.android.com/reference/kotlin/android/app/backup/BackupDataOutput)!`, `newState:` ` [ParcelFileDescriptor](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#)!`)` Based on`oldState`, determine which of the files from the application's data directory need to be backed up, write them to the data stream, and fill in`newState`with the state as it exists now. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [restoreEntity](https://developer.android.com/reference/kotlin/android/app/backup/FileBackupHelper#restoreEntity(android.app.backup.BackupDataInputStream))`(`data:` ` [BackupDataInputStream](https://developer.android.com/reference/kotlin/android/app/backup/BackupDataInputStream)!`)` Restore one record \[representing a single file\] from the restore dataset. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeNewStateDescription](https://developer.android.com/reference/kotlin/android/app/backup/FileBackupHelper#writeNewStateDescription(android.os.ParcelFileDescriptor))`(`fd:` ` [ParcelFileDescriptor](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#)!`)` <br /> |
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
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!:The backup agent's Context object |
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

This should only be called directly from within the [BackupAgentHelper](https://developer.android.com/reference/kotlin/android/app/backup/BackupAgentHelper) implementation. See [android.app.backup.BackupAgent#onBackup(ParcelFileDescriptor, BackupDataOutput, ParcelFileDescriptor)](https://developer.android.com/reference/kotlin/android/app/backup/BackupAgent#onBackup(android.os.ParcelFileDescriptor,%20android.app.backup.BackupDataOutput,%20android.os.ParcelFileDescriptor))for a description of parameter meanings.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `oldState` | [ParcelFileDescriptor](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#)!:An open, read-only [android.os.ParcelFileDescriptor](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#) pointing to the last backup state provided by the application. May be`null`, in which case no prior state is being provided and the application should perform a full backup. |
| `data` | [BackupDataOutput](https://developer.android.com/reference/kotlin/android/app/backup/BackupDataOutput)!:An open, read/write [BackupDataOutput](https://developer.android.com/reference/kotlin/android/app/backup/BackupDataOutput) pointing to the backup data destination. Typically the application will use backup helper classes to write to this file. |
| `newState` | [ParcelFileDescriptor](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#)!:An open, read/write [android.os.ParcelFileDescriptor](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#) pointing to an empty file. The application should record the final backup state here after writing the requested data to the`data`output stream. |
| --- | --- |

### restoreEntity

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun restoreEntity(data: BackupDataInputStream!): Unit
```

Restore one record \[representing a single file\] from the restore dataset.

This should only be called directly from within the [BackupAgentHelper](https://developer.android.com/reference/kotlin/android/app/backup/BackupAgentHelper) implementation.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `data` | [BackupDataInputStream](https://developer.android.com/reference/kotlin/android/app/backup/BackupDataInputStream)!:An open [BackupDataInputStream](https://developer.android.com/reference/kotlin/android/app/backup/BackupDataInputStream) from which the backup data can be read. |

### writeNewStateDescription

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun writeNewStateDescription(fd: ParcelFileDescriptor!): Unit
```

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `newState` | A [android.os.ParcelFileDescriptor](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#) to which the new state will be written. |
