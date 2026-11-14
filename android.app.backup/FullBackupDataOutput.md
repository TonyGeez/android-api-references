# FullBackupDataOutput

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# FullBackupDataOutput

Kotlin| [Java](https://developer.android.com/reference/android/app/backup/FullBackupDataOutput "View this page in Java") 

```
open class FullBackupDataOutput
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.app.backup.FullBackupDataOutput](https://developer.android.com/reference/kotlin/android/app/backup/FullBackupDataOutput#) |

Provides the interface through which a [BackupAgent](https://developer.android.com/reference/kotlin/android/app/backup/BackupAgent) writes entire files to a full backup data set, via its [BackupAgent.onFullBackup(FullBackupDataOutput)](https://developer.android.com/reference/kotlin/android/app/backup/BackupAgent#onFullBackup(android.app.backup.FullBackupDataOutput))method.

## Summary

| Public methods ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getQuota](https://developer.android.com/reference/kotlin/android/app/backup/FullBackupDataOutput#getQuota())`()` Returns the quota in bytes for the application's current backup operation. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getTransportFlags](https://developer.android.com/reference/kotlin/android/app/backup/FullBackupDataOutput#getTransportFlags())`()` Returns flags with additional information about the backup transport. |

## Public methods

### getQuota

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getQuota(): Long
```

Returns the quota in bytes for the application's current backup operation. The value can vary for each operation. 
**See Also**

- [android.app.backup.BackupDataOutput#getQuota()](https://developer.android.com/reference/kotlin/android/app/backup/BackupDataOutput#getQuota()) 

### getTransportFlags

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getTransportFlags(): Int
```

Returns flags with additional information about the backup transport. For supported flags see [android.app.backup.BackupAgent](https://developer.android.com/reference/kotlin/android/app/backup/BackupAgent) 
**See Also**

- [android.app.backup.BackupDataOutput#getTransportFlags()](https://developer.android.com/reference/kotlin/android/app/backup/BackupDataOutput#getTransportFlags())
