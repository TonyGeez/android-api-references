# android.app.backup

# android.app.backup

Kotlin| [Java](_package.md)
| --- | --- |

## Interfaces

| [BackupHelper](BackupHelper.md) | Defines the calling interface that [BackupAgentHelper](BackupAgentHelper.md) uses when dispatching backup and restore operations to the installed helpers. |
| --- | --- |

## Classes

| [BackupAgent](BackupAgent.md) | Provides the central interface between an application and Android's data backup infrastructure. |
| --- | --- |
| [BackupAgentHelper](BackupAgentHelper.md) | A convenient [BackupAgent](BackupAgent.md) wrapper class that automatically manages heterogeneous data sets within the backup data, each identified by a unique key prefix. |
| [BackupDataInput](BackupDataInput.md) | Provides the structured interface through which a [BackupAgent](BackupAgent.md) reads information from the backup data set, via its [onRestore()](BackupAgent.md))method. |
| [BackupDataInputStream](BackupDataInputStream.md) | Provides an [java.io.InputStream](../java.io/InputStream.md)-like interface for accessing an entity's data during a restore operation. |
| --- | --- |
| [BackupDataOutput](BackupDataOutput.md) | Provides the structured interface through which a [BackupAgent](BackupAgent.md) commits information to the backup data set, via its [onBackup()](BackupAgent.md))method. |
| [BackupManager](BackupManager.md) | The interface through which an application interacts with the Android backup service to request backup and restore operations. |
| [FileBackupHelper](FileBackupHelper.md) | A helper class that can be used in conjunction with [android.app.backup.BackupAgentHelper](BackupAgentHelper.md) to manage the backup of a set of files. |
| --- | --- |
| [FullBackupDataOutput](FullBackupDataOutput.md) | Provides the interface through which a [BackupAgent](BackupAgent.md) writes entire files to a full backup data set, via its [BackupAgent.onFullBackup(FullBackupDataOutput)](BackupAgent.md))method. |
| [FullRestoreDataInput](FullRestoreDataInput.md) | Provides the interface through which a [BackupAgent](BackupAgent.md) reads entire files from a full backup data set, via its [BackupAgent.onRestoreFile(FullRestoreDataInput)](BackupAgent.md))method. |
| [RestoreObserver](RestoreObserver.md) | Callback class for receiving progress reports during a restore operation. |
| --- | --- |
| [SharedPreferencesBackupHelper](SharedPreferencesBackupHelper.md) | A helper class that can be used in conjunction with [android.app.backup.BackupAgentHelper](BackupAgentHelper.md) to manage the backup of [android.content.SharedPreferences](../android.content/SharedPreferences.md). |
