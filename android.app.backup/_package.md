# android.app.backup

# android.app.backup

Kotlin| [Java](https://developer.android.com/reference/android/app/backup/package-summary "View this page in Java")
| --- | --- |

## Interfaces

| [BackupHelper](https://developer.android.com/reference/kotlin/android/app/backup/BackupHelper) | Defines the calling interface that [BackupAgentHelper](https://developer.android.com/reference/kotlin/android/app/backup/BackupAgentHelper) uses when dispatching backup and restore operations to the installed helpers. |
| --- | --- |

## Classes

| [BackupAgent](https://developer.android.com/reference/kotlin/android/app/backup/BackupAgent) | Provides the central interface between an application and Android's data backup infrastructure. |
| --- | --- |
| [BackupAgentHelper](https://developer.android.com/reference/kotlin/android/app/backup/BackupAgentHelper) | A convenient [BackupAgent](https://developer.android.com/reference/kotlin/android/app/backup/BackupAgent) wrapper class that automatically manages heterogeneous data sets within the backup data, each identified by a unique key prefix. |
| [BackupDataInput](https://developer.android.com/reference/kotlin/android/app/backup/BackupDataInput) | Provides the structured interface through which a [BackupAgent](https://developer.android.com/reference/kotlin/android/app/backup/BackupAgent) reads information from the backup data set, via its [onRestore()](https://developer.android.com/reference/kotlin/android/app/backup/BackupAgent#onRestore(android.app.backup.BackupDataInput,%20kotlin.Int,%20android.os.ParcelFileDescriptor))method. |
| [BackupDataInputStream](https://developer.android.com/reference/kotlin/android/app/backup/BackupDataInputStream) | Provides an [java.io.InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)-like interface for accessing an entity's data during a restore operation. |
| --- | --- |
| [BackupDataOutput](https://developer.android.com/reference/kotlin/android/app/backup/BackupDataOutput) | Provides the structured interface through which a [BackupAgent](https://developer.android.com/reference/kotlin/android/app/backup/BackupAgent) commits information to the backup data set, via its [onBackup()](https://developer.android.com/reference/kotlin/android/app/backup/BackupAgent#onBackup(android.os.ParcelFileDescriptor,%20android.app.backup.BackupDataOutput,%20android.os.ParcelFileDescriptor))method. |
| [BackupManager](https://developer.android.com/reference/kotlin/android/app/backup/BackupManager) | The interface through which an application interacts with the Android backup service to request backup and restore operations. |
| [FileBackupHelper](https://developer.android.com/reference/kotlin/android/app/backup/FileBackupHelper) | A helper class that can be used in conjunction with [android.app.backup.BackupAgentHelper](https://developer.android.com/reference/kotlin/android/app/backup/BackupAgentHelper) to manage the backup of a set of files. |
| --- | --- |
| [FullBackupDataOutput](https://developer.android.com/reference/kotlin/android/app/backup/FullBackupDataOutput) | Provides the interface through which a [BackupAgent](https://developer.android.com/reference/kotlin/android/app/backup/BackupAgent) writes entire files to a full backup data set, via its [BackupAgent.onFullBackup(FullBackupDataOutput)](https://developer.android.com/reference/kotlin/android/app/backup/BackupAgent#onFullBackup(android.app.backup.FullBackupDataOutput))method. |
| [FullRestoreDataInput](https://developer.android.com/reference/kotlin/android/app/backup/FullRestoreDataInput) | Provides the interface through which a [BackupAgent](https://developer.android.com/reference/kotlin/android/app/backup/BackupAgent) reads entire files from a full backup data set, via its [BackupAgent.onRestoreFile(FullRestoreDataInput)](https://developer.android.com/reference/kotlin/android/app/backup/BackupAgent#onRestoreFile(android.app.backup.FullRestoreDataInput))method. |
| [RestoreObserver](https://developer.android.com/reference/kotlin/android/app/backup/RestoreObserver) | Callback class for receiving progress reports during a restore operation. |
| --- | --- |
| [SharedPreferencesBackupHelper](https://developer.android.com/reference/kotlin/android/app/backup/SharedPreferencesBackupHelper) | A helper class that can be used in conjunction with [android.app.backup.BackupAgentHelper](https://developer.android.com/reference/kotlin/android/app/backup/BackupAgentHelper) to manage the backup of [android.content.SharedPreferences](https://developer.android.com/reference/kotlin/android/content/SharedPreferences.html#). |
