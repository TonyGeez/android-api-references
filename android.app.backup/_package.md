# android.app.backup

# android.app.backup

Kotlin| [Java](../android/app/backup/_package.md)
| --- | --- |

## Interfaces

| [BackupHelper](../android/app/backup/BackupHelper.md) | Defines the calling interface that [BackupAgentHelper](../android/app/backup/BackupAgentHelper.md) uses when dispatching backup and restore operations to the installed helpers. |
| --- | --- |

## Classes

| [BackupAgent](../android/app/backup/BackupAgent.md) | Provides the central interface between an application and Android's data backup infrastructure. |
| --- | --- |
| [BackupAgentHelper](../android/app/backup/BackupAgentHelper.md) | A convenient [BackupAgent](../android/app/backup/BackupAgent.md) wrapper class that automatically manages heterogeneous data sets within the backup data, each identified by a unique key prefix. |
| [BackupDataInput](../android/app/backup/BackupDataInput.md) | Provides the structured interface through which a [BackupAgent](../android/app/backup/BackupAgent.md) reads information from the backup data set, via its [onRestore()](../android/app/backup/BackupAgent.md))method. |
| [BackupDataInputStream](../android/app/backup/BackupDataInputStream.md) | Provides an [java.io.InputStream](../java/io/InputStream.md)-like interface for accessing an entity's data during a restore operation. |
| --- | --- |
| [BackupDataOutput](../android/app/backup/BackupDataOutput.md) | Provides the structured interface through which a [BackupAgent](../android/app/backup/BackupAgent.md) commits information to the backup data set, via its [onBackup()](../android/app/backup/BackupAgent.md))method. |
| [BackupManager](../android/app/backup/BackupManager.md) | The interface through which an application interacts with the Android backup service to request backup and restore operations. |
| [FileBackupHelper](../android/app/backup/FileBackupHelper.md) | A helper class that can be used in conjunction with [android.app.backup.BackupAgentHelper](../android/app/backup/BackupAgentHelper.md) to manage the backup of a set of files. |
| --- | --- |
| [FullBackupDataOutput](../android/app/backup/FullBackupDataOutput.md) | Provides the interface through which a [BackupAgent](../android/app/backup/BackupAgent.md) writes entire files to a full backup data set, via its [BackupAgent.onFullBackup(FullBackupDataOutput)](../android/app/backup/BackupAgent.md))method. |
| [FullRestoreDataInput](../android/app/backup/FullRestoreDataInput.md) | Provides the interface through which a [BackupAgent](../android/app/backup/BackupAgent.md) reads entire files from a full backup data set, via its [BackupAgent.onRestoreFile(FullRestoreDataInput)](../android/app/backup/BackupAgent.md))method. |
| [RestoreObserver](../android/app/backup/RestoreObserver.md) | Callback class for receiving progress reports during a restore operation. |
| --- | --- |
| [SharedPreferencesBackupHelper](../android/app/backup/SharedPreferencesBackupHelper.md) | A helper class that can be used in conjunction with [android.app.backup.BackupAgentHelper](../android/app/backup/BackupAgentHelper.md) to manage the backup of [android.content.SharedPreferences](../android/content/SharedPreferences.md). |
