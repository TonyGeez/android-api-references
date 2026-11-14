# BackupHelper

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BackupHelper

Kotlin| [Java](https://developer.android.com/reference/android/app/backup/BackupHelper "View this page in Java") 

```
interface BackupHelper
```

| [android.app.backup.BackupHelper](https://developer.android.com/reference/kotlin/android/app/backup/BackupHelper#) |

| Known Direct Subclasses [FileBackupHelper](https://developer.android.com/reference/kotlin/android/app/backup/FileBackupHelper), [SharedPreferencesBackupHelper](https://developer.android.com/reference/kotlin/android/app/backup/SharedPreferencesBackupHelper) |----------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [FileBackupHelper](https://developer.android.com/reference/kotlin/android/app/backup/FileBackupHelper) | A helper class that can be used in conjunction with [android.app.backup.BackupAgentHelper](https://developer.android.com/reference/kotlin/android/app/backup/BackupAgentHelper) to manage the backup of a set of files. | | [SharedPreferencesBackupHelper](https://developer.android.com/reference/kotlin/android/app/backup/SharedPreferencesBackupHelper) | A helper class that can be used in conjunction with [android.app.backup.BackupAgentHelper](https://developer.android.com/reference/kotlin/android/app/backup/BackupAgentHelper) to manage the backup of [android.content.SharedPreferences](https://developer.android.com/reference/kotlin/android/content/SharedPreferences.html#). | |

Defines the calling interface that [BackupAgentHelper](https://developer.android.com/reference/kotlin/android/app/backup/BackupAgentHelper) uses when dispatching backup and restore operations to the installed helpers. Applications can define and install their own helpers as well as using those provided as part of the Android framework.

Although multiple helper objects may be installed simultaneously, each helper is responsible only for handling its own data, and will not see entities created by other components within the backup system. Invocations of multiple helpers are performed sequentially by the [BackupAgentHelper](https://developer.android.com/reference/kotlin/android/app/backup/BackupAgentHelper), with each helper given a chance to access its own saved state from within the state record produced during the previous backup operation.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [performBackup](https://developer.android.com/reference/kotlin/android/app/backup/BackupHelper#performBackup(android.os.ParcelFileDescriptor,%20android.app.backup.BackupDataOutput,%20android.os.ParcelFileDescriptor))`(`oldState:` ` [ParcelFileDescriptor](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#)!`, `data:` ` [BackupDataOutput](https://developer.android.com/reference/kotlin/android/app/backup/BackupDataOutput)!`, `newState:` ` [ParcelFileDescriptor](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#)!`)` Based on`oldState`, determine what application content needs to be backed up, write it to`data`, and fill in`newState`with the complete state as it exists now. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [restoreEntity](https://developer.android.com/reference/kotlin/android/app/backup/BackupHelper#restoreEntity(android.app.backup.BackupDataInputStream))`(`data:` ` [BackupDataInputStream](https://developer.android.com/reference/kotlin/android/app/backup/BackupDataInputStream)!`)` Called by [BackupAgentHelper](https://developer.android.com/reference/kotlin/android/app/backup/BackupAgentHelper) to restore a single entity from the restore data set. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeNewStateDescription](https://developer.android.com/reference/kotlin/android/app/backup/BackupHelper#writeNewStateDescription(android.os.ParcelFileDescriptor))`(`newState:` ` [ParcelFileDescriptor](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#)!`)` Called by [BackupAgentHelper](https://developer.android.com/reference/kotlin/android/app/backup/BackupAgentHelper) after a restore operation to write the backup state file corresponding to the data as processed by the helper. |

## Public methods

### performBackup

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun performBackup(
    oldState: ParcelFileDescriptor!, 
    data: BackupDataOutput!, 
    newState: ParcelFileDescriptor!
): Unit
```

Based on`oldState`, determine what application content needs to be backed up, write it to`data`, and fill in`newState`with the complete state as it exists now.

Implementing this method is much like implementing [onBackup()](https://developer.android.com/reference/kotlin/android/app/backup/BackupAgent#onBackup(android.os.ParcelFileDescriptor,%20android.app.backup.BackupDataOutput,%20android.os.ParcelFileDescriptor))--- the method parameters are the same. When this method is invoked the`oldState`descriptor points to the beginning of the state data written during this helper's previous backup operation, and the`newState`descriptor points to the file location at which the helper should write its new state after performing the backup operation.

**Note:** The helper should not close or seek either the`oldState`or the`newState`file descriptors. It is essential that when reading the helper's saved state from the`oldState`file, no extra content is consumed beyond what was stored by this helper. If more old state data is read, even accidentally, it will make it impossible for additional helpers that may be invoked after this one to properly reconstruct their prior state.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `oldState` | [ParcelFileDescriptor](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#)!:An open, read-only [android.os.ParcelFileDescriptor](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#) pointing to the last backup state provided by the application. May be`null`, in which case no prior state is being provided and the application should perform a full backup. |
| `data` | [BackupDataOutput](https://developer.android.com/reference/kotlin/android/app/backup/BackupDataOutput)!:An open, read/write [BackupDataOutput](https://developer.android.com/reference/kotlin/android/app/backup/BackupDataOutput) pointing to the backup data destination. Typically the application will use backup helper classes to write to this file. |
| `newState` | [ParcelFileDescriptor](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#)!:An open, read/write [android.os.ParcelFileDescriptor](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#) pointing to an empty file. The application should record the final backup state here after writing the requested data to the`data`output stream. |

### restoreEntity

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun restoreEntity(data: BackupDataInputStream!): Unit
```

Called by [BackupAgentHelper](https://developer.android.com/reference/kotlin/android/app/backup/BackupAgentHelper) to restore a single entity from the restore data set. This method will be called for each entity in the data set that belongs to this handler.

**Note:** Do not close the`data`stream. Do not read more than [size()](https://developer.android.com/reference/kotlin/android/app/backup/BackupDataInputStream#size())bytes from`data`.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `data` | [BackupDataInputStream](https://developer.android.com/reference/kotlin/android/app/backup/BackupDataInputStream)!:An open [BackupDataInputStream](https://developer.android.com/reference/kotlin/android/app/backup/BackupDataInputStream) from which the backup data can be read. |

### writeNewStateDescription

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun writeNewStateDescription(newState: ParcelFileDescriptor!): Unit
```

Called by [BackupAgentHelper](https://developer.android.com/reference/kotlin/android/app/backup/BackupAgentHelper) after a restore operation to write the backup state file corresponding to the data as processed by the helper. The data written here will be available to the helper during the next call to its [performBackup()](https://developer.android.com/reference/kotlin/android/app/backup/BackupHelper#performBackup(android.os.ParcelFileDescriptor,%20android.app.backup.BackupDataOutput,%20android.os.ParcelFileDescriptor))method.

This method will be called even if the handler's [restoreEntity()](https://developer.android.com/reference/kotlin/android/app/backup/BackupHelper#restoreEntity(android.app.backup.BackupDataInputStream))method was never invoked during the restore operation.

**Note:** The helper should not close or seek the`newState`file descriptor.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `newState` | [ParcelFileDescriptor](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#)!:A [android.os.ParcelFileDescriptor](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#) to which the new state will be written. |
