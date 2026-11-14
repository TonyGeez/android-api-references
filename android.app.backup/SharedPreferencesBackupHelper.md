# SharedPreferencesBackupHelper

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SharedPreferencesBackupHelper

Kotlin | [Java](https://developer.android.com/reference/android/app/backup/SharedPreferencesBackupHelper "View this page in Java") 

```
open class SharedPreferencesBackupHelper : BackupHelper
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.app.backup.SharedPreferencesBackupHelper](https://developer.android.com/reference/kotlin/android/app/backup/SharedPreferencesBackupHelper#) |

A helper class that can be used in conjunction with [android.app.backup.BackupAgentHelper](https://developer.android.com/reference/kotlin/android/app/backup/BackupAgentHelper) to manage the backup of [android.content.SharedPreferences](https://developer.android.com/reference/kotlin/android/content/SharedPreferences.html#). Whenever a backup is performed, it will back up all named shared preferences that have changed since the last backup operation.

To use this class, the application's backup agent class should extend [android.app.backup.BackupAgentHelper](https://developer.android.com/reference/kotlin/android/app/backup/BackupAgentHelper). Then, in the agent's [BackupAgent.onCreate()](https://developer.android.com/reference/kotlin/android/app/backup/BackupAgent#onCreate()) method, an instance of this class should be allocated and installed as a backup/restore handler within the BackupAgentHelper framework. For example, an agent supporting backup and restore for an application with two groups of [android.content.SharedPreferences](https://developer.android.com/reference/kotlin/android/content/SharedPreferences.html#) data might look something like this: 

```kotlin
import android.app.backup.BackupAgentHelper;
  import android.app.backup.SharedPreferencesBackupHelper;
 
  public class MyBackupAgent extends BackupAgentHelper {
      // The names of the SharedPreferences groups that the application maintains.  These
      // are the same strings that are passed to <code><a docref="android.content.Context$getSharedPreferences(kotlin.String, kotlin.Int)">Context.getSharedPreferences(String, int)</a></code>.
      static final String PREFS_DISPLAY = "displayprefs";
      static final String PREFS_SCORES = "highscores";
 
      // An arbitrary string used within the BackupAgentHelper implementation to
      // identify the SharedPreferenceBackupHelper's data.
      static final String MY_PREFS_BACKUP_KEY = "myprefs";
 
      // Allocate a helper and install it.
      public void onCreate() {
          SharedPreferencesBackupHelper helper =
                  new SharedPreferencesBackupHelper(this, PREFS_DISPLAY, PREFS_SCORES);
          addHelper(MY_PREFS_BACKUP_KEY, helper);
      }
  }
```

No further implementation is needed; the [BackupAgentHelper](https://developer.android.com/reference/kotlin/android/app/backup/BackupAgentHelper) mechanism automatically dispatches the [BackupAgent.onBackup()](https://developer.android.com/reference/kotlin/android/app/backup/BackupAgent#onBackup(android.os.ParcelFileDescriptor,%20android.app.backup.BackupDataOutput,%20android.os.ParcelFileDescriptor)) and [BackupAgent.onRestore()](https://developer.android.com/reference/kotlin/android/app/backup/BackupAgent#onRestore(android.app.backup.BackupDataInput,%20kotlin.Int,%20android.os.ParcelFileDescriptor)) callbacks to the SharedPreferencesBackupHelper as appropriate.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SharedPreferencesBackupHelper](https://developer.android.com/reference/kotlin/android/app/backup/SharedPreferencesBackupHelper#SharedPreferencesBackupHelper(android.content.Context,%20kotlin.String))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`, `vararg` `prefGroups:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Construct a helper for backing up and restoring the [android.content.SharedPreferences](https://developer.android.com/reference/kotlin/android/content/SharedPreferences.html#) under the given names. |

| Public methods ||
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [performBackup](https://developer.android.com/reference/kotlin/android/app/backup/SharedPreferencesBackupHelper#performBackup(android.os.ParcelFileDescriptor,%20android.app.backup.BackupDataOutput,%20android.os.ParcelFileDescriptor))`(`oldState:` ` [ParcelFileDescriptor](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#)!`, `data:` ` [BackupDataOutput](https://developer.android.com/reference/kotlin/android/app/backup/BackupDataOutput)!`, `newState:` ` [ParcelFileDescriptor](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#)!`)` Backs up the configured [android.content.SharedPreferences](https://developer.android.com/reference/kotlin/android/content/SharedPreferences.html#) groups. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [restoreEntity](https://developer.android.com/reference/kotlin/android/app/backup/SharedPreferencesBackupHelper#restoreEntity(android.app.backup.BackupDataInputStream))`(`data:` ` [BackupDataInputStream](https://developer.android.com/reference/kotlin/android/app/backup/BackupDataInputStream)!`)` Restores one entity from the restore data stream to its proper shared preferences file store. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeNewStateDescription](https://developer.android.com/reference/kotlin/android/app/backup/SharedPreferencesBackupHelper#writeNewStateDescription(android.os.ParcelFileDescriptor))`(`fd:` ` [ParcelFileDescriptor](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#)!`)` <br /> |

## Public constructors

### SharedPreferencesBackupHelper

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SharedPreferencesBackupHelper(
    context: Context!, 
    vararg prefGroups: String!)
```

Construct a helper for backing up and restoring the [android.content.SharedPreferences](https://developer.android.com/reference/kotlin/android/content/SharedPreferences.html#) under the given names.

| Parameters ||
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!: The application [android.content.Context](https://developer.android.com/reference/kotlin/android/content/Context.html#) |
| `prefGroups` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The names of each [android.content.SharedPreferences](https://developer.android.com/reference/kotlin/android/content/SharedPreferences.html#) file to back up |

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

Backs up the configured [android.content.SharedPreferences](https://developer.android.com/reference/kotlin/android/content/SharedPreferences.html#) groups.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `oldState` | [ParcelFileDescriptor](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#)!: An open, read-only [android.os.ParcelFileDescriptor](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#) pointing to the last backup state provided by the application. May be `null`, in which case no prior state is being provided and the application should perform a full backup. |
| `data` | [BackupDataOutput](https://developer.android.com/reference/kotlin/android/app/backup/BackupDataOutput)!: An open, read/write [BackupDataOutput](https://developer.android.com/reference/kotlin/android/app/backup/BackupDataOutput) pointing to the backup data destination. Typically the application will use backup helper classes to write to this file. |
| `newState` | [ParcelFileDescriptor](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#)!: An open, read/write [android.os.ParcelFileDescriptor](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#) pointing to an empty file. The application should record the final backup state here after writing the requested data to the `data` output stream. |

### restoreEntity

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun restoreEntity(data: BackupDataInputStream!): Unit
```

Restores one entity from the restore data stream to its proper shared preferences file store.

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `data` | [BackupDataInputStream](https://developer.android.com/reference/kotlin/android/app/backup/BackupDataInputStream)!: An open [BackupDataInputStream](https://developer.android.com/reference/kotlin/android/app/backup/BackupDataInputStream) from which the backup data can be read. |

### writeNewStateDescription

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun writeNewStateDescription(fd: ParcelFileDescriptor!): Unit
```

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `newState` | A [android.os.ParcelFileDescriptor](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#) to which the new state will be written. |
