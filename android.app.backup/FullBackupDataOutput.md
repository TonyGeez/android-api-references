# FullBackupDataOutput

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# FullBackupDataOutput

Kotlin| [Java](../android/app/backup/FullBackupDataOutput.md) 
| --- | --- |

```
open class FullBackupDataOutput
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.app.backup.FullBackupDataOutput](../android/app/backup/FullBackupDataOutput.md) |

Provides the interface through which a [BackupAgent](../android/app/backup/BackupAgent.md) writes entire files to a full backup data set, via its [BackupAgent.onFullBackup(FullBackupDataOutput)](../android/app/backup/BackupAgent.md))method.

## Summary

| Public methods ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getQuota](../android/app/backup/FullBackupDataOutput.md))`()` Returns the quota in bytes for the application's current backup operation. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getTransportFlags](../android/app/backup/FullBackupDataOutput.md))`()` Returns flags with additional information about the backup transport. |

## Public methods

### getQuota

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getQuota(): Long
```

Returns the quota in bytes for the application's current backup operation. The value can vary for each operation. 
**See Also**

- [android.app.backup.BackupDataOutput#getQuota()](../android/app/backup/BackupDataOutput.md)) 

### getTransportFlags

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getTransportFlags(): Int
```

Returns flags with additional information about the backup transport. For supported flags see [android.app.backup.BackupAgent](../android/app/backup/BackupAgent.md) 
**See Also**

- [android.app.backup.BackupDataOutput#getTransportFlags()](../android/app/backup/BackupDataOutput.md))
