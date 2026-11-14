# SharedPreferencesBackupHelper

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SharedPreferencesBackupHelper

Kotlin | [Java](../android/app/backup/SharedPreferencesBackupHelper.md) 
| --- | --- |

```
open class SharedPreferencesBackupHelper : BackupHelper
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.app.backup.SharedPreferencesBackupHelper](../android/app/backup/SharedPreferencesBackupHelper.md) |

A helper class that can be used in conjunction with [android.app.backup.BackupAgentHelper](../android/app/backup/BackupAgentHelper.md) to manage the backup of [android.content.SharedPreferences](../android/content/SharedPreferences.md). Whenever a backup is performed, it will back up all named shared preferences that have changed since the last backup operation.

To use this class, the application's backup agent class should extend [android.app.backup.BackupAgentHelper](../android/app/backup/BackupAgentHelper.md). Then, in the agent's [BackupAgent.onCreate()](../android/app/backup/BackupAgent.md)) method, an instance of this class should be allocated and installed as a backup/restore handler within the BackupAgentHelper framework. For example, an agent supporting backup and restore for an application with two groups of [android.content.SharedPreferences](../android/content/SharedPreferences.md) data might look something like this: 

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

No further implementation is needed; the [BackupAgentHelper](../android/app/backup/BackupAgentHelper.md) mechanism automatically dispatches the [BackupAgent.onBackup()](../android/app/backup/BackupAgent.md)) and [BackupAgent.onRestore()](../android/app/backup/BackupAgent.md)) callbacks to the SharedPreferencesBackupHelper as appropriate.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SharedPreferencesBackupHelper](../android/app/backup/SharedPreferencesBackupHelper.md))`(`context:` ` [Context](../android/content/Context.md)!`, `vararg` `prefGroups:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Construct a helper for backing up and restoring the [android.content.SharedPreferences](../android/content/SharedPreferences.md) under the given names. |

| Public methods ||
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [performBackup](../android/app/backup/SharedPreferencesBackupHelper.md))`(`oldState:` ` [ParcelFileDescriptor](../android/os/ParcelFileDescriptor.md)!`, `data:` ` [BackupDataOutput](../android/app/backup/BackupDataOutput.md)!`, `newState:` ` [ParcelFileDescriptor](../android/os/ParcelFileDescriptor.md)!`)` Backs up the configured [android.content.SharedPreferences](../android/content/SharedPreferences.md) groups. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [restoreEntity](../android/app/backup/SharedPreferencesBackupHelper.md))`(`data:` ` [BackupDataInputStream](../android/app/backup/BackupDataInputStream.md)!`)` Restores one entity from the restore data stream to its proper shared preferences file store. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeNewStateDescription](../android/app/backup/SharedPreferencesBackupHelper.md))`(`fd:` ` [ParcelFileDescriptor](../android/os/ParcelFileDescriptor.md)!`)` <br /> |
| --- | --- |

## Public constructors

### SharedPreferencesBackupHelper

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SharedPreferencesBackupHelper(
    context: Context!, 
    vararg prefGroups: String!)
```

Construct a helper for backing up and restoring the [android.content.SharedPreferences](../android/content/SharedPreferences.md) under the given names.

| Parameters ||
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android/content/Context.md)!: The application [android.content.Context](../android/content/Context.md) |
| `prefGroups` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The names of each [android.content.SharedPreferences](../android/content/SharedPreferences.md) file to back up |

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

Backs up the configured [android.content.SharedPreferences](../android/content/SharedPreferences.md) groups.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `oldState` | [ParcelFileDescriptor](../android/os/ParcelFileDescriptor.md)!: An open, read-only [android.os.ParcelFileDescriptor](../android/os/ParcelFileDescriptor.md) pointing to the last backup state provided by the application. May be `null`, in which case no prior state is being provided and the application should perform a full backup. |
| `data` | [BackupDataOutput](../android/app/backup/BackupDataOutput.md)!: An open, read/write [BackupDataOutput](../android/app/backup/BackupDataOutput.md) pointing to the backup data destination. Typically the application will use backup helper classes to write to this file. |
| `newState` | [ParcelFileDescriptor](../android/os/ParcelFileDescriptor.md)!: An open, read/write [android.os.ParcelFileDescriptor](../android/os/ParcelFileDescriptor.md) pointing to an empty file. The application should record the final backup state here after writing the requested data to the `data` output stream. |
| --- | --- |

### restoreEntity

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun restoreEntity(data: BackupDataInputStream!): Unit
```

Restores one entity from the restore data stream to its proper shared preferences file store.

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `data` | [BackupDataInputStream](../android/app/backup/BackupDataInputStream.md)!: An open [BackupDataInputStream](../android/app/backup/BackupDataInputStream.md) from which the backup data can be read. |

### writeNewStateDescription

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun writeNewStateDescription(fd: ParcelFileDescriptor!): Unit
```

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `newState` | A [android.os.ParcelFileDescriptor](../android/os/ParcelFileDescriptor.md) to which the new state will be written. |
