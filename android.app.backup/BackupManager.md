# BackupManager

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BackupManager

Kotlin| [Java](../android/app/backup/BackupManager.md) 
| --- | --- |

```
open class BackupManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.app.backup.BackupManager](../android/app/backup/BackupManager.md) |

The interface through which an application interacts with the Android backup service to request backup and restore operations. Applications instantiate it using the constructor and issue calls through that instance.

When an application has made changes to data which should be backed up, a call to [dataChanged()](../android/app/backup/BackupManager.md))will notify the backup service. The system will then schedule a backup operation to occur in the near future. Repeated calls to [dataChanged()](../android/app/backup/BackupManager.md))have no further effect until the backup operation actually occurs.

A backup or restore operation for your application begins when the system launches the [android.app.backup.BackupAgent](../android/app/backup/BackupAgent.md) subclass you've declared in your manifest. See the documentation for [android.app.backup.BackupAgent](../android/app/backup/BackupAgent.md) for a detailed description of how the operation then proceeds.

Several attributes affecting the operation of the backup and restore mechanism can be set on the` ` [<application>](https://developer.android.com/guide/topics/manifest/application-element.html) tag in your application's AndroidManifest.xml file.
|
| ### Developer Guides
|
| For more information about using BackupManager, read the [Data Backup](https://developer.android.com/guide/topics/data/backup.html) developer guide.

## Summary

| XML attributes ||
|-----------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [`android:allowBackup`](../android/app/backup/BackupManager.md) | Whether to allow the application to participate in the backup and restore infrastructure. |
| [`android:backupAgent`](../android/app/backup/BackupManager.md) | The name of the class subclassing BackupAgent to manage backup and restore of the application's data on external storage. |
| [`android:killAfterRestore`](../android/app/backup/BackupManager.md) | Whether the application in question should be terminated after its settings have been restored during a full-system restore operation. |
| --- | --- |
| [`android:restoreAnyVersion`](../android/app/backup/BackupManager.md) | Indicate that the application is prepared to attempt a restore of any backed-up dataset, even if the backup is apparently from a newer version of the application than is currently installed on the device. |

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [BackupManager](../android/app/backup/BackupManager.md))`(`context:` ` [Context](../android/content/Context.md)!`)` Constructs a BackupManager object through which the application can communicate with the Android backup system. |

| Public methods ||
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [dataChanged](../android/app/backup/BackupManager.md))`()` Notifies the Android backup system that your application wishes to back up new changes to its data. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [dataChanged](../android/app/backup/BackupManager.md))`(`packageName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Convenience method for callers who need to indicate that some other package needs a backup pass. |
| open [UserHandle](../android/os/UserHandle.md)? | [getUserForAncestralSerialNumber](../android/app/backup/BackupManager.md))`(`ancestralSerialNumber:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns a [UserHandle](../android/os/UserHandle.md) for the user that has`ancestralSerialNumber`as the serial number of the its ancestral work profile or`null`if there is none. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [requestRestore](../android/app/backup/BackupManager.md))`(`observer:` ` [RestoreObserver](../android/app/backup/RestoreObserver.md)!`)` <br /> |

## XML attributes

### android:allowBackup

```
android:allowBackup
```
Whether to allow the application to participate in the backup and restore infrastructure. If this attribute is set to`false`, no backup or restore of the application will ever be performed, even by a full-system backup that would otherwise cause all application data to be saved via adb. The default value of this attribute is`true`.

May be a boolean value, such as "`true`" or "`false`". 

### android:backupAgent

```
android:backupAgent
```
The name of the class subclassing`BackupAgent`to manage backup and restore of the application's data on external storage.

May be a string value, using '\\\\;' to escape characters such as '\\\\n' or '\\\\uxxxx' for a unicode character; 

### android:killAfterRestore

```
android:killAfterRestore
```
Whether the application in question should be terminated after its settings have been restored during a full-system restore operation. Single-package restore operations will never cause the application to be shut down. Full-system restore operations typically only occur once, when the phone is first set up. Third-party applications will not usually need to use this attribute.

The default is`true`, which means that after the application has finished processing its data during a full-system restore, it will be terminated.

May be a boolean value, such as "`true`" or "`false`". 

### android:restoreAnyVersion

```
android:restoreAnyVersion
```
Indicate that the application is prepared to attempt a restore of any backed-up dataset, even if the backup is apparently from a newer version of the application than is currently installed on the device. Setting this attribute to`true`will permit the Backup Manager to attempt restore even when a version mismatch suggests that the data are incompatible.*Use with caution!*

The default value of this attribute is`false`.

May be a boolean value, such as "`true`" or "`false`".

## Public constructors

### BackupManager

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
BackupManager(context: Context!)
```

Constructs a BackupManager object through which the application can communicate with the Android backup system.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android/content/Context.md)!:The [android.content.Context](../android/content/Context.md) that was provided when one of your application's [Activities](../android/app/Activity.md) was created. |

## Public methods

### dataChanged

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun dataChanged(): Unit
```

Notifies the Android backup system that your application wishes to back up new changes to its data. A backup operation using your application's [android.app.backup.BackupAgent](../android/app/backup/BackupAgent.md) subclass will be scheduled when you call this method.

Note: This only works if your application is performing Key/Value backups. 

### dataChanged

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun dataChanged(packageName: String!): Unit
```

Convenience method for callers who need to indicate that some other package needs a backup pass. This can be useful in the case of groups of packages that share a uid.

This method requires that the application hold the "android.permission.BACKUP" permission if the package named in the argument does not run under the same uid as the caller.

| Parameters ||
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The package name identifying the application to back up. Note: Only works for packages performing Key/Value backups. |

### getUserForAncestralSerialNumber

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getUserForAncestralSerialNumber(ancestralSerialNumber: Long): UserHandle?
```

Returns a [UserHandle](../android/os/UserHandle.md) for the user that has`ancestralSerialNumber`as the serial number of the its ancestral work profile or`null`if there is none.

The ancestral serial number will have a corresponding [UserHandle](../android/os/UserHandle.md) if the device has a work profile that was restored from another work profile with serial number`ancestralSerialNumber`. 
**See Also**

- [android.os.UserManager#getSerialNumberForUser(UserHandle)](../android/os/UserManager.md)) 

### requestRestore

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun requestRestore(observer: RestoreObserver!): Int
```

**Deprecated:** *Applications shouldn't request a restore operation using this method. In Android P and later, this method is a no-op.*

*Restore the calling application from backup. The data will be restored from the current backup dataset if the application has stored data there, or from the dataset used during the last full device setup operation if the current backup dataset has no matching data. If no backup data exists for this application in either source, a non-zero value is returned.*
*If this method returns zero (meaning success), the OS attempts to retrieve a backed-up dataset from the remote transport, instantiate the application's backup agent, and pass the dataset to the agent's [onRestore()](../android/app/backup/BackupAgent.md))method.
Unlike other restore operations, this method doesn't terminate the application after the restore. The application continues running to receive the [RestoreObserver](../android/app/backup/RestoreObserver.md) callbacks on the`observer`argument. Full backups use an [Application](../android/app/Application.md) base class while key-value backups use the application subclass declared in the AndroidManifest.xml`<application>`tag.*

<br />

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `observer` | [RestoreObserver](../android/app/backup/RestoreObserver.md)!:The [RestoreObserver](../android/app/backup/RestoreObserver.md) to receive callbacks during the restore operation. This must not be null. |

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Zero on success; nonzero on error. |
