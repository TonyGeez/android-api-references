# RecoverySystem

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RecoverySystem

Kotlin| [Java](../android/os/RecoverySystem.md) 
| --- | --- |

```
open class RecoverySystem
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.os.RecoverySystem](../android/os/RecoverySystem.md) |

RecoverySystem contains methods for interacting with the Android recovery system (the separate partition that can be used to install system updates, wipe user data, etc.)

## Summary

| Nested classes ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [ProgressListener](../android/os/RecoverySystem.ProgressListener.md) Interface definition for a callback to be invoked regularly as verification proceeds. |

| Public methods ||
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [installPackage](../android/os/RecoverySystem.md))`(`context:` ` [Context](../android/content/Context.md)!`, `packageFile:` ` [File](../java/io/File.md)!`)` Reboots the device in order to install the given update package. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [rebootWipeCache](../android/os/RecoverySystem.md))`(`context:` ` [Context](../android/content/Context.md)!`)` Reboot into the recovery system to wipe the /cache partition. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [rebootWipeUserData](../android/os/RecoverySystem.md))`(`context:` ` [Context](../android/content/Context.md)!`)` Reboots the device and wipes the user data and cache partitions. |
| --- | --- |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [verifyPackage](../android/os/RecoverySystem.md))`(`packageFile:` ` [File](../java/io/File.md)!`, `listener:` ` [RecoverySystem.ProgressListener](../android/os/RecoverySystem.ProgressListener.md)!`, `deviceCertsZipFile:` ` [File](../java/io/File.md)!`)` Verify the cryptographic signature of a system update package before installing it. |

## Public methods

### installPackage

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun installPackage(
    context: Context!, 
    packageFile: File!
): Unit
```

Reboots the device in order to install the given update package. Requires the [android.Manifest.permission#REBOOT](../android/Manifest.permission.md) permission. 
Requires android.Manifest.permission.RECOVERY

| Parameters ||
|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android/content/Context.md)!:the Context to use |
| `packageFile` | [File](../java/io/File.md)!:the update package to install. Must be on a partition mountable by recovery. (The set of partitions known to recovery may vary from device to device. Generally, /cache and /data are safe.) |

| Exceptions ||
|-----------------------|----------------------------------------------------------------------------|
| `java.io.IOException` | if writing the recovery command file fails, or if the reboot itself fails. |

### rebootWipeCache

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun rebootWipeCache(context: Context!): Unit
```

Reboot into the recovery system to wipe the /cache partition.

| Exceptions ||
|-----------------------|--------------------------|
| `java.io.IOException` | if something goes wrong. |

### rebootWipeUserData

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun rebootWipeUserData(context: Context!): Unit
```

Reboots the device and wipes the user data and cache partitions. This is sometimes called a "factory reset", which is something of a misnomer because the system partition is not restored to its factory state. Requires the [android.Manifest.permission#REBOOT](../android/Manifest.permission.md) permission.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android/content/Context.md)!:the Context to use |

| Exceptions ||
|-------------------------------|----------------------------------------------------------------------------|
| `java.io.IOException` | if writing the recovery command file fails, or if the reboot itself fails. |
| `java.lang.SecurityException` | if the current user is not allowed to wipe data. |

### verifyPackage

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun verifyPackage(
    packageFile: File!, 
    listener: RecoverySystem.ProgressListener!, 
    deviceCertsZipFile: File!
): Unit
```

Verify the cryptographic signature of a system update package before installing it. Note that the package is also verified separately by the installer once the device is rebooted into the recovery system. This function will return only if the package was successfully verified; otherwise it will throw an exception. Verification of a package can take significant time, so this function should not be called from a UI thread. Interrupting the thread while this function is in progress will result in a SecurityException being thrown (and the thread's interrupt flag will be cleared).

| Parameters ||
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `packageFile` | [File](../java/io/File.md)!:the package to be verified |
| `listener` | [RecoverySystem.ProgressListener](../android/os/RecoverySystem.ProgressListener.md)!:an object to receive periodic progress updates as verification proceeds. May be null. |
| `deviceCertsZipFile` | [File](../java/io/File.md)!:the zip file of certificates whose public keys we will accept. Verification succeeds if the package is signed by the private key corresponding to any public key in this file. May be null to use the system default file (currently "/system/etc/security/otacerts.zip"). |
| --- | --- |

| Exceptions ||
|------------------------------------------|--------------------------------------------------------------|
| `java.io.IOException` | if there were any errors reading the package or certs files. |
| `java.security.GeneralSecurityException` | if verification failed |
