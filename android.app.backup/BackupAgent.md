Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BackupAgent

```
abstract class BackupAgent : ContextWrapper
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [android.content.Context](../android.content/Context.md) |||
| | ↳ | [android.content.ContextWrapper](../android.content/ContextWrapper.md) ||
| | | ↳ | [android.app.backup.BackupAgent](BackupAgent.md) |
| --- | --- | --- | --- |

Known Direct Subclasses [BackupAgentHelper](BackupAgentHelper.md) [BackupAgentHelper](BackupAgentHelper.md) A convenient BackupAgent wrapper class that automatically manages heterogeneous data sets within the backup data, each identified by a unique key prefix.

Provides the central interface between an application and Android's data backup infrastructure. An application that wishes to participate in the backup and restore mechanism will declare a subclass of BackupAgent, implement the onBackup and onRestore methods, and provide the name of its backup agent class in its `AndroidManifest.xml` file via the ` https://developer.android.com/guide/topics/manifest/application-element.html` tag's `android:backupAgent` attribute.

<br />

> [!NOTE]
>
> ### Developer Guides
>
> For more information about using BackupAgent, read the [Data Backup](https://developer.android.com/guide/topics/data/backup.html) developer guide.

### Basic Operation

When the application makes changes to data that it wishes to keep backed up, it should call the dataChanged method. This notifies the Android Backup Manager that the application needs an opportunity to update its backup image. The Backup Manager, in turn, schedules a backup pass to be performed at an opportune time.

Restore operations are typically performed only when applications are first installed on a device. At that time, the operating system checks to see whether there is a previously-saved data set available for the application being installed, and if so, begins an immediate restore pass to deliver the backup data as part of the installation process.

When a backup or restore pass is run, the application's process is launched (if not already running), the manifest-declared backup agent class (in the `android:backupAgent` attribute) is instantiated within that process, and the agent's onCreate method is invoked. This prepares the agent instance to run the actual backup or restore logic. At this point the agent's onBackup or onRestore method will be invoked as appropriate for the operation being performed.

A backup data set consists of one or more "entities," flattened binary data records that are each identified with a key string unique within the data set. Adding a record to the active data set or updating an existing record is done by simply writing new entity data under the desired key. Deleting an entity from the data set is done by writing an entity under that key with header specifying a negative data size, and no actual entity data.

**Helper Classes**

An extensible agent based on convenient helper classes is available in BackupAgentHelper. That class is particularly suited to handling of simple file or `https://developer.android.com/reference/kotlin/android/content/SharedPreferences.html#` backup and restore.

**Threading**

The constructor, as well as onCreate and onDestroy lifecycle callbacks run on the main thread (UI thread) of the application that implements the BackupAgent. The data-handling callbacks: onBackup, onFullBackup, onRestore, onRestoreFile, onRestoreFinished, and onQuotaExceeded run on binder pool threads.

## Summary

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/backup/BackupAgent#FLAG_CLIENT_SIDE_ENCRYPTION_ENABLED:kotlin.Int` Transport flag indicating that the transport has client-side encryption enabled. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/backup/BackupAgent#FLAG_CROSS_PLATFORM_DATA_TRANSFER_IOS:kotlin.Int` Transport flag indicating that the transport is used for a cross-platform transfer to or from iOS. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/backup/BackupAgent#FLAG_DEVICE_TO_DEVICE_TRANSFER:kotlin.Int` Transport flag indicating that the transport is used for a device-to-device transfer. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/backup/BackupAgent#TYPE_DIRECTORY:kotlin.Int` During a full restore, indicates that the file system object being restored is a directory. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/backup/BackupAgent#TYPE_FILE:kotlin.Int` During a full restore, indicates that the file system object being restored is an ordinary file. |

Inherited constants From class `https://developer.android.com/reference/kotlin/android/content/Context.html#` `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#ACCESSIBILITY_SERVICE:kotlin.String`

Use with getSystemService to retrieve a `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityManager.html#` for giving the user feedback for UI events through the registered event listeners.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#ACCOUNT_SERVICE:kotlin.String`

Use with getSystemService to retrieve a `https://developer.android.com/reference/kotlin/android/accounts/AccountManager.html#` for receiving intents at a time of your choosing.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#ACTIVITY_SERVICE:kotlin.String`

Use with getSystemService to retrieve a `https://developer.android.com/reference/kotlin/android/app/ActivityManager.html#` for interacting with the global system state.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#ADVANCED_PROTECTION_SERVICE:kotlin.String`

Use with getSystemService to retrieve an `https://developer.android.com/reference/kotlin/android/security/advancedprotection/AdvancedProtectionManager.html#`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#ALARM_SERVICE:kotlin.String`

Use with getSystemService to retrieve a `https://developer.android.com/reference/kotlin/android/app/AlarmManager.html#` for receiving intents at a time of your choosing.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#APPWIDGET_SERVICE:kotlin.String`

Use with getSystemService to retrieve a `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager.html#` for accessing AppWidgets.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#APP_FUNCTION_SERVICE:kotlin.String`

Use with getSystemService to retrieve an `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionManager.html#` for executing app functions.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#APP_INTERACTION_SERVICE:kotlin.String`

Use with getSystemService to retrieve an `https://developer.android.com/reference/kotlin/android/app/AppInteractionManager.html#` for managing app interactions.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#APP_OPS_SERVICE:kotlin.String`

Use with getSystemService to retrieve a `https://developer.android.com/reference/kotlin/android/app/AppOpsManager.html#` for tracking application operations on the device.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#APP_SEARCH_SERVICE:kotlin.String`

Use with getSystemService to retrieve an `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchManager.html#` for indexing and querying app data managed by the system.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#AUDIO_SERVICE:kotlin.String`

Use with getSystemService to retrieve a `https://developer.android.com/reference/kotlin/android/media/AudioManager.html#` for handling management of volume, ringer modes and audio routing.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#AUTHENTICATION_POLICY_SERVICE:kotlin.String`

Use with getSystemService to retrieve an `https://developer.android.com/reference/kotlin/android/security/authenticationpolicy/AuthenticationPolicyManager.html#`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#AUTOFILL_SERVICE:kotlin.String`

Use with getSystemService to retrieve an `https://developer.android.com/reference/kotlin/android/view/autofill/AutofillManager.html#`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#BATTERY_SERVICE:kotlin.String`

Use with getSystemService to retrieve a `https://developer.android.com/reference/kotlin/android/os/BatteryManager.html#` for managing battery state.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#BIND_ABOVE_CLIENT:kotlin.Int`

Flag for #bindService: indicates that the client application binding to this service considers the service to be more important than the app itself. When set, the platform will try to have the out of memory killer kill the app before it kills the service it is bound to, though this is not guaranteed to be the case.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#BIND_ADJUST_WITH_ACTIVITY:kotlin.Int`

Flag for #bindService: If binding from an activity, allow the target service's process importance to be raised based on whether the activity is visible to the user, regardless whether another flag is used to reduce the amount that the client process's overall importance is used to impact it.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#BIND_ALLOW_ACTIVITY_STARTS:kotlin.Int`

Flag for #bindService: If binding from an app that is visible, the bound service is allowed to start an activity from background. This was the default behavior before SDK version `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#UPSIDE_DOWN_CAKE:kotlin.Int`. Since then, the default behavior changed to disallow the bound service to start a background activity even if the app bound to it is in foreground, unless this flag is specified when binding.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#BIND_ALLOW_OOM_MANAGEMENT:kotlin.Int`

Flag for #bindService: allow the process hosting the bound service to go through its normal memory management. It will be treated more like a running service, allowing the system to (temporarily) expunge the process if low on memory or for some other whim it may have, and being more aggressive about making it a candidate to be killed (and restarted) if running for a long time.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#BIND_AUTO_CREATE:kotlin.Int`

Flag for #bindService: automatically create the service as long as the binding exists. Note that while this will create the service, its onStartCommand method will still only be called due to an explicit call to startService. Even without that, though, this still provides you with access to the service object while the service is created.

Note that prior to `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#ICE_CREAM_SANDWICH:kotlin.Int`, not supplying this flag would also impact how important the system consider's the target service's process to be. When set, the only way for it to be raised was by binding from a service in which case it will only be important when that activity is in the foreground. Now to achieve this behavior you must explicitly supply the new flag `https://developer.android.com/reference/kotlin/android/content/Context.html#BIND_ADJUST_WITH_ACTIVITY:kotlin.Int`. For compatibility, old applications that don't specify `https://developer.android.com/reference/kotlin/android/content/Context.html#BIND_AUTO_CREATE:kotlin.Int` will automatically have the flags `https://developer.android.com/reference/kotlin/android/content/Context.html#BIND_WAIVE_PRIORITY:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/content/Context.html#BIND_ADJUST_WITH_ACTIVITY:kotlin.Int` set for them in order to achieve the same result.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#BIND_DEBUG_UNBIND:kotlin.Int`

Flag for #bindService: include debugging help for mismatched calls to unbind. When this flag is set, the callstack of the following unbindService call is retained, to be printed if a later incorrect unbind call is made. Note that doing this requires retaining information about the binding that was made for the lifetime of the app, resulting in a leak -- this should only be used for debugging.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#BIND_EXTERNAL_SERVICE:kotlin.Int`

Flag for #bindService: The service being bound is an `https://developer.android.com/reference/kotlin/android/R.attr.html#isolatedProcess:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/R.attr.html#externalService:kotlin.Int` service. This binds the service into the calling application's package, rather than the package in which the service is declared.

When using this flag, the code for the service being bound will execute under the calling application's package name and user ID. Because the service must be an isolated process, it will not have direct access to the application's data, though. The purpose of this flag is to allow applications to provide services that are attributed to the app using the service, rather than the application providing the service.
*This flag is NOT compatible with `https://developer.android.com/reference/kotlin/android/content/Context.BindServiceFlags.html#`. If you need to use `https://developer.android.com/reference/kotlin/android/content/Context.BindServiceFlags.html#`, you must use `https://developer.android.com/reference/kotlin/android/content/Context.html#BIND_EXTERNAL_SERVICE_LONG:kotlin.Long` instead.*

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#BIND_EXTERNAL_SERVICE_LONG:kotlin.Long`

Works in the same way as `https://developer.android.com/reference/kotlin/android/content/Context.html#BIND_EXTERNAL_SERVICE:kotlin.Int`, but it's defined as a `long` value that is compatible to `https://developer.android.com/reference/kotlin/android/content/Context.BindServiceFlags.html#`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#BIND_IMPORTANT:kotlin.Int`

Flag for #bindService: this service is very important to the client, so should be brought to the foreground process level when the client is. Normally a process can only be raised to the visibility level by a client, even if that client is in the foreground.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#BIND_INCLUDE_CAPABILITIES:kotlin.Int`

Flag for #bindService: If binding from an app that has specific capabilities due to its foreground state such as an activity or foreground service, then this flag will allow the bound app to get the same capabilities, as long as it has the required permissions as well. If binding from a top app and its target SDK version is at or above `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int`, the app needs to explicitly use BIND_INCLUDE_CAPABILITIES flag to pass all capabilities to the service so the other app can have while-in-use access such as location, camera, microphone from background. If binding from a top app and its target SDK version is below `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int`, BIND_INCLUDE_CAPABILITIES is implicit.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#BIND_NOT_FOREGROUND:kotlin.Int`

Flag for #bindService: don't allow this binding to raise the target service's process to the foreground scheduling priority. It will still be raised to at least the same memory priority as the client (so that its process will not be killable in any situation where the client is not killable), but for CPU scheduling purposes it may be left in the background. This only has an impact in the situation where the binding client is a foreground process and the target service is in a background process.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#BIND_NOT_PERCEPTIBLE:kotlin.Int`

Flag for #bindService: If binding from an app that is visible or user-perceptible, lower the target service's importance to below the perceptible level. This allows the system to (temporarily) expunge the bound process from memory to make room for more important user-perceptible processes.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#BIND_PACKAGE_ISOLATED_PROCESS:kotlin.Int`

Flag for #bindIsolatedService: Bind the service into a shared isolated process, but only with other isolated services from the same package that declare the same process name.

Specifying this flag allows multiple isolated services defined in the same package to be running in a single shared isolated process. This shared isolated process must be specified since this flag will not work with the default application process.

This flag is different from `https://developer.android.com/reference/kotlin/android/content/Context.html#BIND_SHARED_ISOLATED_PROCESS:kotlin.Int` since it only allows binding services from the same package in the same shared isolated process. This also means the shared package isolated process is global, and not scoped to each potential calling app.

The shared isolated process instance is identified by the "android:process" attribute defined by the service. This flag cannot be used without this attribute set.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#BIND_SHARED_ISOLATED_PROCESS:kotlin.Int`

Flag for #bindIsolatedService: Bind the service into a shared isolated process. Specifying this flag allows multiple isolated services to be running in a single shared isolated process. The shared isolated process instance is identified by the instanceName parameter in bindIsolatedService. Subsequent calls to #bindIsolatedService with the same instanceName will cause the isolated service to be co-located in the same shared isolated process. Note that the shared isolated process is scoped to the calling app; once created, only the calling app can bind additional isolated services into the shared process. However, the services themselves can come from different APKs and therefore different vendors. Only services that set the `https://developer.android.com/reference/kotlin/android/R.attr.html#allowSharedIsolatedProcess:kotlin.Int` attribute to `true` are allowed to be bound into a shared isolated process.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#BIND_WAIVE_PRIORITY:kotlin.Int`

Flag for #bindService: don't impact the scheduling or memory management priority of the target service's hosting process. Allows the service's process to be managed on the background LRU list just like a regular application process in the background.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#BIOMETRIC_SERVICE:kotlin.String`

Use with getSystemService to retrieve a `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricManager.html#` for handling biometric and PIN/pattern/password authentication.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#BLOB_STORE_SERVICE:kotlin.String`

Use with getSystemService to retrieve a `https://developer.android.com/reference/kotlin/android/app/blob/BlobStoreManager.html#` for contributing and accessing data blobs from the blob store maintained by the system.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#BLUETOOTH_SERVICE:kotlin.String`

Use with getSystemService to retrieve a `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothManager.html#` for using Bluetooth.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#BUGREPORT_SERVICE:kotlin.String`

Service to capture a bugreport.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#CAMERA_SERVICE:kotlin.String`

Use with getSystemService to retrieve a `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraManager.html#` for interacting with camera devices.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#CAPTIONING_SERVICE:kotlin.String`

Use with getSystemService to retrieve a `https://developer.android.com/reference/kotlin/android/view/accessibility/CaptioningManager.html#` for obtaining captioning properties and listening for changes in captioning preferences.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#CARRIER_CONFIG_SERVICE:kotlin.String`

Use with getSystemService to retrieve a `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager.html#` for reading carrier configuration values.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#CHOOSER_SERVICE:kotlin.String`

Use with getSystemService to retrieve a `https://developer.android.com/reference/kotlin/android/service/chooser/ChooserManager.html#`.

**Note:** This service is not available on Wear OS, Android TV, or Android Auto devices. On these form factors, calls to `getSystemService` for this service will return `null`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#CLIPBOARD_SERVICE:kotlin.String`

Use with getSystemService to retrieve a `https://developer.android.com/reference/kotlin/android/content/ClipboardManager.html#` for accessing and modifying the contents of the global clipboard.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#COMPANION_DEVICE_SERVICE:kotlin.String`

Use with getSystemService to retrieve a `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager.html#` for managing companion devices

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#CONNECTIVITY_DIAGNOSTICS_SERVICE:kotlin.String`

Use with getSystemService to retrieve a `https://developer.android.com/reference/kotlin/android/net/ConnectivityDiagnosticsManager.html#` for performing network connectivity diagnostics as well as receiving network connectivity information from the system.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#CONNECTIVITY_SERVICE:kotlin.String`

Use with getSystemService to retrieve a `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager.html#` for handling management of network connections.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#CONSUMER_IR_SERVICE:kotlin.String`

Use with getSystemService to retrieve a `https://developer.android.com/reference/kotlin/android/hardware/ConsumerIrManager.html#` for transmitting infrared signals from the device.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#CONTACT_KEYS_SERVICE:kotlin.String`

Use with getSystemService to retrieve a `https://developer.android.com/reference/kotlin/android/provider/E2eeContactKeysManager.html#` to managing contact keys.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#CONTENT_RESTRICTION_SERVICE:kotlin.String`

Use with getSystemService to retrieve a `https://developer.android.com/reference/kotlin/android/app/contentsafety/ContentSafetyManager.html#`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#CONTEXT_IGNORE_SECURITY:kotlin.Int`

Flag for use with createPackageContext: ignore any security restrictions on the Context being requested, allowing it to always be loaded. For use with `https://developer.android.com/reference/kotlin/android/content/Context.html#CONTEXT_INCLUDE_CODE:kotlin.Int` to allow code to be loaded into a process even when it isn't safe to do so. Use with extreme care!

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#CONTEXT_INCLUDE_CODE:kotlin.Int`

Flag for use with createPackageContext: include the application code with the context. This means loading code into the caller's process, so that getClassLoader can be used to instantiate the application's classes. Setting this flags imposes security restrictions on what application context you can access; if the requested application can not be safely loaded into your process, java.lang.SecurityException will be thrown. If this flag is not set, there will be no restrictions on the packages that can be loaded, but getClassLoader will always return the default system class loader.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#CONTEXT_RESTRICTED:kotlin.Int`

Flag for use with createPackageContext: a restricted context may disable specific features. For instance, a View associated with a restricted context would ignore particular XML attributes.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#CREDENTIAL_SERVICE:kotlin.String`

Use with getSystemService to retrieve a `https://developer.android.com/reference/kotlin/android/credentials/CredentialManager.html#` to authenticate a user to your app.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#CROSS_PROFILE_APPS_SERVICE:kotlin.String`

Use with getSystemService to retrieve a `https://developer.android.com/reference/kotlin/android/content/pm/CrossProfileApps.html#` for cross profile operations.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#DEVICE_ID_DEFAULT:kotlin.Int`

The default device ID, which is the ID of the primary (non-virtual) device.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#DEVICE_ID_INVALID:kotlin.Int`

Invalid device ID.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#DEVICE_LOCK_SERVICE:kotlin.String`

Use with getSystemService to retrieve a `https://developer.android.com/reference/kotlin/android/devicelock/DeviceLockManager.html#`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#DEVICE_POLICY_SERVICE:kotlin.String`

Use with getSystemService to retrieve a `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#` for working with global device policy management.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#DISPLAY_HASH_SERVICE:kotlin.String`

Use with getSystemService to access `https://developer.android.com/reference/kotlin/android/view/displayhash/DisplayHashManager.html#` to handle display hashes.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#DISPLAY_SERVICE:kotlin.String`

Use with getSystemService to retrieve a `https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager.html#` for interacting with display devices.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#DOMAIN_VERIFICATION_SERVICE:kotlin.String`

Use with getSystemService to access `https://developer.android.com/reference/kotlin/android/content/pm/verify/domain/DomainVerificationManager.html#` to retrieve approval and user state for declared web domains.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#DOWNLOAD_SERVICE:kotlin.String`

Use with getSystemService to retrieve a `https://developer.android.com/reference/kotlin/android/app/DownloadManager.html#` for requesting HTTP downloads.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#DROPBOX_SERVICE:kotlin.String`

Use with getSystemService to retrieve a `https://developer.android.com/reference/kotlin/android/os/DropBoxManager.html#` instance for recording diagnostic logs.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#EUICC_SERVICE:kotlin.String`

Use with getSystemService to retrieve a `https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager.html#` to manage the device eUICC (embedded SIM).

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#FILE_INTEGRITY_SERVICE:kotlin.String`

Use with getSystemService to retrieve an `https://developer.android.com/reference/kotlin/android/security/FileIntegrityManager.html#`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#FILE_SERVICE:kotlin.String`

Use with getSystemService to retrieve a `https://developer.android.com/reference/kotlin/android/os/storage/FileManager.html#` for handling file operations.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#GAME_SERVICE:kotlin.String`

Use with getSystemService to retrieve a `https://developer.android.com/reference/kotlin/android/app/GameManager.html#`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#GRAMMATICAL_INFLECTION_SERVICE:kotlin.String`

Use with getSystemService to retrieve a `https://developer.android.com/reference/kotlin/android/app/GrammaticalInflectionManager.html#`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#HARDWARE_PROPERTIES_SERVICE:kotlin.String`

Use with getSystemService to retrieve a `https://developer.android.com/reference/kotlin/android/os/HardwarePropertiesManager.html#` for accessing the hardware properties service.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#HEALTHCONNECT_SERVICE:kotlin.String`

Use with getSystemService to retrieve a `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#HID_SERVICE:kotlin.String`

Use with getSystemService to retrieve a `https://developer.android.com/reference/kotlin/android/hardware/hid/HidManager.html#` for interacting with HID devices.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#INPUT_METHOD_SERVICE:kotlin.String`

Use with getSystemService to retrieve a `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager.html#` for accessing input methods.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#INPUT_SERVICE:kotlin.String`

Use with getSystemService to retrieve a `https://developer.android.com/reference/kotlin/android/hardware/input/InputManager.html#` for interacting with input devices.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#IPSEC_SERVICE:kotlin.String`

Use with getSystemService to retrieve a `https://developer.android.com/reference/kotlin/android/net/IpSecManager.html#` for encrypting Sockets or Networks with IPSec.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#JOB_SCHEDULER_SERVICE:kotlin.String`

Use with getSystemService to retrieve a `https://developer.android.com/reference/kotlin/android/app/job/JobScheduler.html#` instance for managing occasional background tasks.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#KEYCHAIN_SERVICE:kotlin.String`

Use with getSystemService to retrieve a `https://developer.android.com/reference/kotlin/android/security/KeyChainManager.html#` for managing KeyChain certificates and grants.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#KEYGUARD_SERVICE:kotlin.String`

Use with getSystemService to retrieve a `https://developer.android.com/reference/kotlin/android/app/KeyguardManager.html#` for controlling keyguard.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#KEYSTORE_SERVICE:kotlin.String`

Use with getSystemService to retrieve a `https://developer.android.com/reference/kotlin/android/security/keystore/KeyStoreManager.html#` for accessing [Android Keystore](../privacy-and-security/keystore.md) functions.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#LAUNCHER_APPS_SERVICE:kotlin.String`

Use with getSystemService to retrieve a `https://developer.android.com/reference/kotlin/android/content/pm/LauncherApps.html#` for querying and monitoring launchable apps across profiles of a user.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#LAYOUT_INFLATER_SERVICE:kotlin.String`

Use with getSystemService to retrieve a `https://developer.android.com/reference/kotlin/android/view/LayoutInflater.html#` for inflating layout resources in this context.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#LOCALE_SERVICE:kotlin.String`

Use with getSystemService to retrieve a `https://developer.android.com/reference/kotlin/android/app/LocaleManager.html#`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#LOCATION_SERVICE:kotlin.String`

Use with getSystemService to retrieve a `https://developer.android.com/reference/kotlin/android/location/LocationManager.html#` for controlling location updates.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#MEDIA_COMMUNICATION_SERVICE:kotlin.String`

Use with getSystemService to retrieve a `https://developer.android.com/reference/kotlin/android/media/MediaCommunicationManager.html#` for managing `https://developer.android.com/reference/kotlin/android/media/MediaSession2.html#`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#MEDIA_METRICS_SERVICE:kotlin.String`

Use with getSystemService to retrieve a `https://developer.android.com/reference/kotlin/android/media/metrics/MediaMetricsManager.html#` for interacting with media metrics on the device.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#MEDIA_PROJECTION_SERVICE:kotlin.String`

Use with getSystemService to retrieve a `https://developer.android.com/reference/kotlin/android/media/projection/MediaProjectionManager.html#` instance for managing media projection sessions.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#MEDIA_QUALITY_SERVICE:kotlin.String`

Use with getSystemService to retrieve a `https://developer.android.com/reference/kotlin/android/media/quality/MediaQualityManager.html#` for standardize picture and audio API parameters.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#MEDIA_ROUTER_SERVICE:kotlin.String`

Use with #getSystemService to retrieve a `https://developer.android.com/reference/kotlin/android/media/MediaRouter.html#` for controlling and managing routing of media.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#MEDIA_SESSION_SERVICE:kotlin.String`

Use with getSystemService to retrieve a `https://developer.android.com/reference/kotlin/android/media/session/MediaSessionManager.html#` for managing media Sessions.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#MEMORY_BUDGET_SERVICE:kotlin.String`

Use with getSystemService to retrieve a `https://developer.android.com/reference/kotlin/android/app/MemoryBudgetManager.html#` for monitoring memory budgets.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#MIDI_SERVICE:kotlin.String`

Use with getSystemService to retrieve a `https://developer.android.com/reference/kotlin/android/media/midi/MidiManager.html#` for accessing the MIDI service.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#MODE_APPEND:kotlin.Int`

File creation mode: for use with openFileOutput, if the file already exists then write data to the end of the existing file instead of erasing it.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#MODE_ENABLE_WRITE_AHEAD_LOGGING:kotlin.Int`

Database open flag: when set, the database is opened with write-ahead logging enabled by default.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#MODE_MULTI_PROCESS:kotlin.Int`

SharedPreference loading flag: when set, the file on disk will be checked for modification even if the shared preferences instance is already loaded in this process. This behavior is sometimes desired in cases where the application has multiple processes, all writing to the same SharedPreferences file. Generally there are better forms of communication between processes, though.

This was the legacy (but undocumented) behavior in and before Gingerbread (Android 2.3) and this flag is implied when targeting such releases. For applications targeting SDK versions *greater than* Android 2.3, this flag must be explicitly set if desired.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#MODE_NO_LOCALIZED_COLLATORS:kotlin.Int`

Database open flag: when set, the database is opened without support for localized collators.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#MODE_PRIVATE:kotlin.Int`

File creation mode: the default mode, where the created file can only be accessed by the calling application (or all applications sharing the same user ID).

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#MODE_WORLD_READABLE:kotlin.Int`

File creation mode: allow all other applications to have read access to the created file.

Starting from `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#N:kotlin.Int`, attempting to use this mode throws a `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#MODE_WORLD_WRITEABLE:kotlin.Int`

File creation mode: allow all other applications to have write access to the created file.

Starting from `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#N:kotlin.Int`, attempting to use this mode will throw a `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#MULTISENSORY_MANAGER_SERVICE:kotlin.String`

Use with getSystemService to retrieve the service that plays multisensory feedback.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#NETWORK_STATS_SERVICE:kotlin.String`

Use with getSystemService to retrieve a `https://developer.android.com/reference/kotlin/android/app/usage/NetworkStatsManager.html#` for querying network usage stats.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#NFC_SERVICE:kotlin.String`

Use with getSystemService to retrieve a `https://developer.android.com/reference/kotlin/android/nfc/NfcManager.html#` for using NFC.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#NOTIFICATION_SERVICE:kotlin.String`

Use with getSystemService to retrieve a `https://developer.android.com/reference/kotlin/android/app/NotificationManager.html#` for informing the user of background events.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#NPU_SERVICE:kotlin.String`

Use with getSystemService to retrieve a BackupAgent.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#NSD_SERVICE:kotlin.String`

Use with getSystemService to retrieve a `https://developer.android.com/reference/kotlin/android/net/nsd/NsdManager.html#` for handling management of network service discovery

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#OVERLAY_SERVICE:kotlin.String`

Use with getSystemService to retrieve a `https://developer.android.com/reference/kotlin/android/content/om/OverlayManager.html#` for managing overlay packages.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#PCC_SANDBOX_SERVICE:kotlin.String`

Use with getSystemService to retrieve a `https://developer.android.com/reference/kotlin/android/app/privatecompute/PccSandboxManager.html#`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#PEOPLE_SERVICE:kotlin.String`

Use with getSystemService to access a `https://developer.android.com/reference/kotlin/android/app/people/PeopleManager.html#` to interact with your published conversations.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#PERFORMANCE_HINT_SERVICE:kotlin.String`

Use with getSystemService to retrieve a `https://developer.android.com/reference/kotlin/android/os/PerformanceHintManager.html#` for accessing the performance hinting service.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#PERSISTENT_DATA_BLOCK_SERVICE:kotlin.String`

Use with getSystemService to retrieve a `https://developer.android.com/reference/kotlin/android/service/persistentdata/PersistentDataBlockManager.html#` instance for interacting with a storage device that lives across factory resets.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#POWER_SERVICE:kotlin.String`

Use with getSystemService to retrieve a `https://developer.android.com/reference/kotlin/android/os/PowerManager.html#` for controlling power management, including "wake locks," which let you keep the device on while you're running long tasks.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#PRINT_SERVICE:kotlin.String`

`https://developer.android.com/reference/kotlin/android/print/PrintManager.html#` for printing and managing printers and print tasks.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#PROFILING_SERVICE:kotlin.String`

Use with getSystemService to retrieve an `https://developer.android.com/reference/kotlin/android/os/ProfilingManager.html#`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#RECEIVER_EXPORTED:kotlin.Int`

Flag for #registerReceiver: The receiver can receive broadcasts from other Apps. Has the same behavior as marking a statically registered receiver with "exported=true"

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#RECEIVER_NOT_EXPORTED:kotlin.Int`

Flag for #registerReceiver: The receiver cannot receive broadcasts from other Apps. Has the same behavior as marking a statically registered receiver with "exported=false"

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#RECEIVER_VISIBLE_TO_INSTANT_APPS:kotlin.Int`

Flag for #registerReceiver: The receiver can receive broadcasts from Instant Apps.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#RESTRICTIONS_SERVICE:kotlin.String`

Use with getSystemService to retrieve a `https://developer.android.com/reference/kotlin/android/content/RestrictionsManager.html#` for retrieving application restrictions and requesting permissions for restricted operations.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#ROLE_SERVICE:kotlin.String`

Use with getSystemService to retrieve a `https://developer.android.com/reference/kotlin/android/app/role/RoleManager.html#` for managing roles.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#SATELLITE_SERVICE:kotlin.String`

Use with getSystemService to retrieve a `https://developer.android.com/reference/kotlin/android/telephony/satellite/SatelliteManager.html#` for accessing satellite functionality.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#SEARCH_SERVICE:kotlin.String`

Use with getSystemService to retrieve a `https://developer.android.com/reference/kotlin/android/app/SearchManager.html#` for handling searches.

`https://developer.android.com/reference/kotlin/android/content/res/Configuration.html#UI_MODE_TYPE_WATCH:kotlin.Int` does not support `https://developer.android.com/reference/kotlin/android/app/SearchManager.html#`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#SECURITY_STATE_SERVICE:kotlin.String`

Use with getSystemService to retrieve a `https://developer.android.com/reference/kotlin/android/os/SecurityStateManager.html#` for accessing the security state manager service.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#SENSOR_SERVICE:kotlin.String`

Use with getSystemService to retrieve a `https://developer.android.com/reference/kotlin/android/hardware/SensorManager.html#` for accessing sensors.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#SERIAL_SERVICE:kotlin.String`

Use with getSystemService to retrieve a `https://developer.android.com/reference/kotlin/android/hardware/serial/SerialManager.html#` for access to serial ports.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#SHORTCUT_SERVICE:kotlin.String`

Use with getSystemService to retrieve a `https://developer.android.com/reference/kotlin/android/content/pm/ShortcutManager.html#` for accessing the launcher shortcut service.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#STATUS_BAR_SERVICE:kotlin.String`

Use with getSystemService to retrieve a `https://developer.android.com/reference/kotlin/android/app/StatusBarManager.html#` for interacting with the status bar and quick settings.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#STORAGE_SERVICE:kotlin.String`

Use with getSystemService to retrieve a `https://developer.android.com/reference/kotlin/android/os/storage/StorageManager.html#` for accessing system storage functions.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#STORAGE_STATS_SERVICE:kotlin.String`

Use with getSystemService to retrieve a `https://developer.android.com/reference/kotlin/android/app/usage/StorageStatsManager.html#` for accessing system storage statistics.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#SYSTEM_HEALTH_SERVICE:kotlin.String`

Use with getSystemService to retrieve a `https://developer.android.com/reference/kotlin/android/os/health/SystemHealthManager.html#` for accessing system health (battery, power, memory, etc) metrics.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#TELECOM_SERVICE:kotlin.String`

Use with getSystemService to retrieve a `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager.html#` to manage telecom-related features of the device.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#TELEPHONY_IMS_SERVICE:kotlin.String`

Use with getSystemService to retrieve an `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsManager.html#`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#TELEPHONY_PHONE_NUMBER_SERVICE:kotlin.String`

Use with getSystemService to retrieve a `https://developer.android.com/reference/kotlin/android/telephony/PhoneNumberManager.html#` for parsing phone numbers.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#TELEPHONY_SERVICE:kotlin.String`

Use with getSystemService to retrieve a `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager.html#` for handling management the telephony features of the device.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#TELEPHONY_SUBSCRIPTION_SERVICE:kotlin.String`

Use with getSystemService to retrieve a `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager.html#` for handling management the telephony subscriptions of the device.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#TETHERING_SERVICE:kotlin.String`

Use with getSystemService to retrieve a `https://developer.android.com/reference/kotlin/android/net/TetheringManager.html#` for managing tethering functions.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#TEXT_CLASSIFICATION_SERVICE:kotlin.String`

Use with getSystemService to retrieve a `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassificationManager.html#` for text classification services.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#TEXT_SERVICES_MANAGER_SERVICE:kotlin.String`

Use with getSystemService to retrieve a `https://developer.android.com/reference/kotlin/android/view/textservice/TextServicesManager.html#` for accessing text services.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#TIME_MANAGER_SERVICE:kotlin.String`

Use with getSystemService to retrieve a `https://developer.android.com/reference/kotlin/android/app/time/TimeManager.html#`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#TV_AD_SERVICE:kotlin.String`

Use with getSystemService to retrieve a `https://developer.android.com/reference/kotlin/android/media/tv/ad/TvAdManager.html#` for interacting with TV client-side advertisement services on the device.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#TV_INPUT_SERVICE:kotlin.String`

Use with getSystemService to retrieve a `https://developer.android.com/reference/kotlin/android/media/tv/TvInputManager.html#` for interacting with TV inputs on the device.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#TV_INTERACTIVE_APP_SERVICE:kotlin.String`

Use with getSystemService to retrieve a `https://developer.android.com/reference/kotlin/android/media/tv/interactive/TvInteractiveAppManager.html#` for interacting with TV interactive applications on the device.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#UI_MODE_SERVICE:kotlin.String`

Use with getSystemService to retrieve a `https://developer.android.com/reference/kotlin/android/app/UiModeManager.html#` for controlling UI modes.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#USAGE_STATS_SERVICE:kotlin.String`

Use with getSystemService to retrieve a `https://developer.android.com/reference/kotlin/android/app/usage/UsageStatsManager.html#` for querying device usage stats.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#USB_SERVICE:kotlin.String`

Use with getSystemService to retrieve a `https://developer.android.com/reference/kotlin/android/hardware/usb/UsbManager.html#` for access to USB devices (as a USB host) and for controlling this device's behavior as a USB device.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#USER_SERVICE:kotlin.String`

Use with getSystemService to retrieve a `https://developer.android.com/reference/kotlin/android/os/UserManager.html#` for managing users on devices that support multiple users.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#VIBRATOR_MANAGER_SERVICE:kotlin.String`

Use with getSystemService to retrieve a `https://developer.android.com/reference/kotlin/android/os/VibratorManager.html#` for accessing the device vibrators, interacting with individual ones and playing synchronized effects on multiple vibrators.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#VIBRATOR_SERVICE:kotlin.String`

Use with getSystemService to retrieve a `https://developer.android.com/reference/kotlin/android/os/Vibrator.html#` for interacting with the vibration hardware.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#VIRTUAL_DEVICE_SERVICE:kotlin.String`

Use with getSystemService to retrieve a `https://developer.android.com/reference/kotlin/android/companion/virtual/VirtualDeviceManager.html#` for managing virtual devices. On devices without `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_COMPANION_DEVICE_SETUP:kotlin.String` system feature the getSystemService will return `null`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#VPN_MANAGEMENT_SERVICE:kotlin.String`

Use with getSystemService to retrieve a `https://developer.android.com/reference/kotlin/android/net/VpnManager.html#` to manage profiles for the platform built-in VPN.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#WALLPAPER_SERVICE:kotlin.String`

Use with getSystemService to retrieve a com.android.server.WallpaperService for accessing wallpapers.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#WEB_APP_SERVICE:kotlin.String`

Use with getSystemService to retrieve a `https://developer.android.com/reference/kotlin/android/content/pm/webapp/WebAppManager.html#`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#WIFI_AWARE_SERVICE:kotlin.String`

Use with getSystemService to retrieve a `https://developer.android.com/reference/kotlin/android/net/wifi/aware/WifiAwareManager.html#` for handling management of Wi-Fi Aware.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#WIFI_P2P_SERVICE:kotlin.String`

Use with getSystemService to retrieve a `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.html#` for handling management of Wi-Fi peer-to-peer connections.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#WIFI_RTT_RANGING_SERVICE:kotlin.String`

Use with getSystemService to retrieve a `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/WifiRttManager.html#` for ranging devices with wifi.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#WIFI_SERVICE:kotlin.String`

Use with getSystemService to retrieve a `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager.html#` for handling management of Wi-Fi access.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#WINDOW_SERVICE:kotlin.String`

Use with getSystemService to retrieve a `https://developer.android.com/reference/kotlin/android/view/WindowManager.html#` for accessing the system's window manager.

<br />

| Public constructors ||
|---|---|
| BackupAgent <br /> |

| Public methods ||
|---|---|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | fullBackupFile Write an entire file as part of a full-backup operation. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onBackup The application is being asked to write any data changed since the last time it performed a backup operation. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onCreate Provided as a convenience for agent implementations that need an opportunity to do one-time initialization before the actual backup or restore operation is begun. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onDestroy Provided as a convenience for agent implementations that need to do some sort of shutdown process after backup or restore is completed. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | onEstimateFullBackupBytes Estimate how much data in bytes a full backup will deliver. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onFullBackup The application is having its entire file system contents backed up. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onQuotaExceeded Notification that the application's current backup operation causes it to exceed the maximum size permitted by the transport. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onRestore The application is being restored from backup and should replace any existing data with the contents of the backup. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onRestore New version of onRestore that handles a long app version code. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onRestoreFile Handle the data delivered via the given file descriptor during a full restore operation. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onRestoreFile Handle the data delivered via the given file descriptor during a full restore operation. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onRestoreFinished The application's restore operation has completed. |
| --- | --- |

Inherited functions From class `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#` `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` attachBaseContext

Set the base context for this ContextWrapper. All calls will then be delegated to the base context. Throws IllegalStateException if a base context has already been set.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` bindIsolatedService

Variation of #bindService that, in the specific case of isolated services, allows the caller to generate multiple instances of a service from a single component declaration. In other words, you can use this to bind to a service that has specified `https://developer.android.com/reference/kotlin/android/R.attr.html#isolatedProcess:kotlin.Int` and, in addition to the existing behavior of running in an isolated process, you can also through the arguments here have the system bring up multiple concurrent processes hosting their own instances of that service. The instanceName you provide here identifies the different instances, and you can use updateServiceGroup to tell the system how it should manage each of these instances.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` bindService

See bindService Call of to obtain a BindServiceFlags object.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` bindService

See bindService Call of to obtain a BindServiceFlags object.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` bindService

Connects to an application service, creating it if needed. This defines a dependency between your application and the service. The given conn will receive the service object when it is created and be told if it dies and restarts. The service will be considered required by the system only for as long as the calling context exists. For example, if this Context is an Activity that is stopped, the service will not be required to continue running until the Activity is resumed.

If the service does not support binding, it may return `null` from its onBind method. If it does, then the ServiceConnection's onNullBinding method will be invoked instead of onServiceConnected.

**Note:** This method *cannot* be called from a `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#` component. A pattern you can use to communicate from a BroadcastReceiver to a Service is to call startService with the arguments containing the command to be sent, with the service calling its stopSelf method when done executing that command. See the API demo App/Service/Service Start Arguments Controller for an illustration of this. It is okay, however, to use this method from a BroadcastReceiver that has been registered with #registerReceiver, since the lifetime of this BroadcastReceiver is tied to another object (the one that registered it).

This method only accepts a int type flag, to pass in a long type flag, call bindService instead.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` bindService

Same as bindService with executor to control ServiceConnection callbacks.

This method only accepts a 32 bits flag, to pass in a 64 bits flag, call bindService instead.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` bindServiceAsUser

See bindServiceAsUser Call of to obtain a BindServiceFlags object.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` bindServiceAsUser

Binds to a service in the given `user` in the same manner as #bindService.

Requires that one of the following conditions are met:

- caller has `android.Manifest.permission.INTERACT_ACROSS_USERS_FULL`
- caller has `android.Manifest.permission.INTERACT_ACROSS_USERS` and is the same package as the `service` (determined by its component's package) and the Android version is at least `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#TIRAMISU:kotlin.Int`
- caller has `android.Manifest.permission.INTERACT_ACROSS_USERS` and is in same profile group as the given `user`
- caller has `android.Manifest.permission.INTERACT_ACROSS_PROFILES` and is in same profile group as the given `user` and is the same package as the `service`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` checkCallingOrSelfPermission

Determine whether the calling process of an IPC *or you* have been granted a particular permission. This is the same as checkCallingPermission, except it grants your own permissions if you are not currently processing an IPC. Use with care!

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` checkCallingOrSelfUriPermission

Determine whether the calling process of an IPC *or you* has been granted permission to access a specific URI. This is the same as checkCallingUriPermission, except it grants your own permissions if you are not currently processing an IPC. Use with care!

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html` checkCallingOrSelfUriPermissions

Determine whether the calling process of an IPC *or you* has been granted permission to access a list of URIs. This is the same as checkCallingUriPermission, except it grants your own permissions if you are not currently processing an IPC. Use with care!

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` checkCallingPermission

Determine whether the calling process of an IPC you are handling has been granted a particular permission. This is basically the same as calling checkPermission with the pid and uid returned by getCallingPid and getCallingUid. One important difference is that if you are not currently processing an IPC, this function will always fail. This is done to protect against accidentally leaking permissions; you can use checkCallingOrSelfPermission to avoid this protection.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` checkCallingUriPermission

Determine whether the calling process and uid has been granted permission to access a specific URI. This is basically the same as calling checkUriPermission with the pid and uid returned by getCallingPid and getCallingUid. One important difference is that if you are not currently processing an IPC, this function will always fail.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html` checkCallingUriPermissions

Determine whether the calling process and uid has been granted permission to access a list of URIs. This is basically the same as calling checkUriPermissions with the pid and uid returned by getCallingPid and getCallingUid. One important difference is that if you are not currently processing an IPC, this function will always fail.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` checkContentUriPermissionFull

Determine whether a particular process and uid has been granted permission to access a specific content URI.

Unlike checkUriPermission, this method checks for general access to the URI's content provider, as well as explicitly granted permissions.

Note, this check will throw an `https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#` for non-content URIs.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` checkPermission

Determine whether the given permission is allowed for a particular process and user ID running in the system.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` checkSelfPermission

Determine whether *you* have been granted a particular permission.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` checkUriPermission

Determine whether a particular process and uid has been granted permission to access a specific URI. This only checks for permissions that have been explicitly granted -- if the given process/uid has more general access to the URI's content provider then this check will always fail.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` checkUriPermission

Check both a Uri and normal permission. This allows you to perform both checkPermission and #checkUriPermission in one call.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html` checkUriPermissions

Determine whether a particular process and uid has been granted permission to access a list of URIs. This only checks for permissions that have been explicitly granted -- if the given process/uid has more general access to the URI's content provider then this check will always fail. **Note:** On SDK Version `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int`, calling this method from a secondary-user's context will incorrectly return `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#PERMISSION_DENIED:kotlin.Int` for all {code uris}.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` clearWallpaper

<br />

`https://developer.android.com/reference/kotlin/android/content/Context.html#` createAttributionContext

Return a new Context object for the current Context but attribute to a different tag. In complex apps attribution tagging can be used to distinguish between separate logical parts.

<br />

`https://developer.android.com/reference/kotlin/android/content/Context.html#!` createConfigurationContext

Return a new Context object for the current Context but whose resources are adjusted to match the given Configuration. Each call to this method returns a new instance of a Context object; Context objects are not shared, however common state (ClassLoader, other Resources for the same configuration) may be so the Context itself can be fairly lightweight.

<br />

`https://developer.android.com/reference/kotlin/android/content/Context.html#` createContext

Creates a context with specific properties and behaviors.

<br />

`https://developer.android.com/reference/kotlin/android/content/Context.html#!` createContextForSplit

Return a new Context object for the given split name. The new Context has a ClassLoader and Resources object that can access the split's and all of its dependencies' code/resources. Each call to this method returns a new instance of a Context object; Context objects are not shared, however common state (ClassLoader, other Resources for the same split) may be so the Context itself can be fairly lightweight.

<br />

`https://developer.android.com/reference/kotlin/android/content/Context.html#` createDeviceContext

Returns a new `Context` object from the current context but with device association given by the `deviceId`. Each call to this method returns a new instance of a context object. Context objects are not shared; however, common state (such as the `https://developer.android.com/reference/kotlin/java/lang/ClassLoader.html#` and other resources for the same configuration) can be shared, so the `Context` itself is lightweight.

Applications that run on virtual devices may use this method to access the default device capabilities and functionality (by passing `https://developer.android.com/reference/kotlin/android/content/Context.html#DEVICE_ID_DEFAULT:kotlin.Int`. Similarly, applications running on the default device may access the functionality of virtual devices.

Note that the newly created instance will be associated with the same display as the parent Context, regardless of the device ID passed here.

<br />

`https://developer.android.com/reference/kotlin/android/content/Context.html#!` createDeviceProtectedStorageContext

Return a new Context object for the current Context but whose storage APIs are backed by device-protected storage.

On devices with direct boot, data stored in this location is encrypted with a key tied to the physical device, and it can be accessed immediately after the device has booted successfully, both *before and after* the user has authenticated with their credentials (such as a lock pattern or PIN).

Because device-protected data is available without user authentication, you should carefully limit the data you store using this Context. For example, storing sensitive authentication tokens or passwords in the device-protected area is strongly discouraged.

If the underlying device does not have the ability to store device-protected and credential-protected data using different keys, then both storage areas will become available at the same time. They remain as two distinct storage locations on disk, and only the window of availability changes.

Each call to this method returns a new instance of a Context object; Context objects are not shared, however common state (ClassLoader, other Resources for the same configuration) may be so the Context itself can be fairly lightweight.

<br />

`https://developer.android.com/reference/kotlin/android/content/Context.html#!` createDisplayContext

Returns a new `Context` object from the current context but with resources adjusted to match the metrics of `display`. Each call to this method returns a new instance of a context object. Context objects are not shared; however, common state (such as the `https://developer.android.com/reference/kotlin/java/lang/ClassLoader.html#` and other resources for the same configuration) can be shared, so the `Context` itself is lightweight.

**Note:** This `Context` is **not** expected to be updated with new configuration if the underlying display configuration changes and the cached `Resources` it returns could be stale. It is suggested to use `https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager.DisplayListener.html#` to listen for changes and re-create an instance if necessary.

This `Context` is **not** a UI context, do not use it to access UI components or obtain a `https://developer.android.com/reference/kotlin/android/view/WindowManager.html#` instance.

To obtain an instance of `https://developer.android.com/reference/kotlin/android/view/WindowManager.html#` configured to show windows on the given display, call createWindowContext on the returned display context, then call getSystemService or getSystemService on the returned window context.

<br />

`https://developer.android.com/reference/kotlin/android/content/Context.html#!` createPackageContext

Return a new Context object for the given application name. This Context is the same as what the named application gets when it is launched, containing the same resources and class loader. Each call to this method returns a new instance of a Context object; Context objects are not shared, however they share common state (Resources, ClassLoader, etc) so the Context instance itself is fairly lightweight.

Throws `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.NameNotFoundException.html#` if there is no application with the given package name.

Throws `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#` if the Context requested can not be loaded into the caller's process for security reasons (see `https://developer.android.com/reference/kotlin/android/content/Context.html#CONTEXT_INCLUDE_CODE:kotlin.Int` for more information}.

<br />

`https://developer.android.com/reference/kotlin/android/content/Context.html#` createWindowContext

Creates a `Context` for a non-`https://developer.android.com/reference/kotlin/android/app/Activity.html#` window on the given `https://developer.android.com/reference/kotlin/android/view/Display.html#`.

Similar to createWindowContext, but the `display` is passed in, instead of implicitly using the getDisplay.

<br />

`https://developer.android.com/reference/kotlin/android/content/Context.html#` createWindowContext

Creates a Context for a non-activity window.

A window context is a context that can be used to add non-activity windows, such as `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#TYPE_APPLICATION_OVERLAY:kotlin.Int`. A window context must be created from a context that has an associated `https://developer.android.com/reference/kotlin/android/view/Display.html#`, such as `https://developer.android.com/reference/kotlin/android/app/Activity.html#` or a context created with createDisplayContext.

The window context is created with the appropriate `https://developer.android.com/reference/kotlin/android/content/res/Configuration.html#` for the area of the display that the windows created with it can occupy; it must be used when `https://developer.android.com/reference/kotlin/android/view/LayoutInflater.html#` views, such that they can be inflated with proper `https://developer.android.com/reference/kotlin/android/content/res/Resources.html#`. Below is a sample code to **add an application overlay window on the primary display:**

```kotlin
...
  final DisplayManager dm = anyContext.getSystemService(DisplayManager.class);
  final Display primaryDisplay = dm.getDisplay(DEFAULT_DISPLAY);
  final Context windowContext = anyContext.createDisplayContext(primaryDisplay)
          .createWindowContext(TYPE_APPLICATION_OVERLAY, null);
  final View overlayView = Inflater.from(windowContext).inflate(someLayoutXml, null);
 
  // WindowManager.LayoutParams initialization
  ...
  // The types used in addView and createWindowContext must match.
  mParams.type = TYPE_APPLICATION_OVERLAY;
  ...
 
  windowContext.getSystemService(WindowManager.class).addView(overlayView, mParams);
  
```

This context's configuration and resources are adjusted to an area of the display where the windows with provided type will be added. **Note that all windows associated with the same context will have an affinity and can only be moved together between different displays or areas on a display.** If there is a need to add different window types, or non-associated windows, separate Contexts should be used.

Creating a window context is an expensive operation. Misuse of this API may lead to a huge performance drop. The best practice is to use the same window context when possible. An approach is to create one window context with specific window type and display and use it everywhere it's needed.

After `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int`, window context provides the capability to receive configuration changes for existing token by overriding the `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#token:android.os.IBinder` of the `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#` passed in addView. This is useful when an application needs to attach its window to an existing activity for window token sharing use-case.

Note that the window context in `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int` didn't have this capability. This is a no-op for the window context in `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int`.
Below is sample code to **attach an existing token to a window context:**

```kotlin
final DisplayManager dm = anyContext.getSystemService(DisplayManager.class);
  final Display primaryDisplay = dm.getDisplay(DEFAULT_DISPLAY);
  final Context windowContext = anyContext.createWindowContext(primaryDisplay,
          TYPE_APPLICATION, null);
 
  // Get an existing token.
  final IBinder existingToken = activity.getWindow().getAttributes().token;
 
  // The types used in addView() and createWindowContext() must match.
  final WindowManager.LayoutParams params = new WindowManager.LayoutParams(TYPE_APPLICATION);
  params.token = existingToken;
 
  // After WindowManager#addView(), the server side will extract the provided token from
  // LayoutParams#token (existingToken in the sample code), and switch to propagate
  // configuration changes from the node associated with the provided token.
  windowContext.getSystemService(WindowManager.class).addView(overlayView, mParams);
  
```

After `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int`, window context provides the capability to listen to its `https://developer.android.com/reference/kotlin/android/content/res/Configuration.html#` changes by calling registerComponentCallbacks, while other kinds of `https://developer.android.com/reference/kotlin/android/content/Context.html#` will register the `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks.html#` to getApplicationContext. Note that window context only propagate onConfigurationChanged callback. onLowMemory or other callbacks in `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#` won't be invoked.

Note that using `https://developer.android.com/reference/kotlin/android/app/Application.html#` or `https://developer.android.com/reference/kotlin/android/app/Service.html#` context for UI-related queries may result in layout or continuity issues on devices with variable screen sizes (e.g. foldables) or in multi-window modes, since these non-UI contexts may not reflect the `https://developer.android.com/reference/kotlin/android/content/res/Configuration.html#` changes for the visual container.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!` databaseList

Returns an array of strings naming the private databases associated with this Context's application package.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` deleteDatabase

Delete an existing private SQLiteDatabase associated with this Context's application package.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` deleteFile

Delete the given private file associated with this Context's application package.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` deleteSharedPreferences

Delete an existing shared preferences file.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` enforceCallingOrSelfPermission

If neither you nor the calling process of an IPC you are handling has been granted a particular permission, throw a `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#`. This is the same as enforceCallingPermission, except it grants your own permissions if you are not currently processing an IPC. Use with care!

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` enforceCallingOrSelfUriPermission

If the calling process of an IPC *or you* has not been granted permission to access a specific URI, throw `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#`. This is the same as enforceCallingUriPermission, except it grants your own permissions if you are not currently processing an IPC. Use with care!

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` enforceCallingPermission

If the calling process of an IPC you are handling has not been granted a particular permission, throw a `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#`. This is basically the same as calling enforcePermission with the pid and uid returned by getCallingPid and getCallingUid. One important difference is that if you are not currently processing an IPC, this function will always throw the SecurityException. This is done to protect against accidentally leaking permissions; you can use enforceCallingOrSelfPermission to avoid this protection.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` enforceCallingUriPermission

If the calling process and uid has not been granted permission to access a specific URI, throw `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#`. This is basically the same as calling enforceUriPermission with the pid and uid returned by getCallingPid and getCallingUid. One important difference is that if you are not currently processing an IPC, this function will always throw a SecurityException.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` enforcePermission

If the given permission is not allowed for a particular process and user ID running in the system, throw a `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` enforceUriPermission

If a particular process and uid has not been granted permission to access a specific URI, throw `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#`. This only checks for permissions that have been explicitly granted -- if the given process/uid has more general access to the URI's content provider then this check will always fail.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` enforceUriPermission

Enforce both a Uri and normal permission. This allows you to perform both enforcePermission and #enforceUriPermission in one call.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!` fileList

Returns an array of strings naming the private files associated with this Context's application package.

<br />

`https://developer.android.com/reference/kotlin/android/content/Context.html#!` getApplicationContext

Return the context of the single, global Application object of the current process. This generally should only be used if you need a Context whose lifecycle is separate from the current context, that is tied to the lifetime of the process rather than the current component.

Consider for example how this interacts with registerReceiver:

- If used from an Activity context, the receiver is being registered within that activity. This means that you are expected to unregister before the activity is done being destroyed; in fact if you do not do so, the framework will clean up your leaked registration as it removes the activity and log an error. Thus, if you use the Activity context to register a receiver that is static (global to the process, not associated with an Activity instance) then that registration will be removed on you at whatever point the activity you used is destroyed.

- If used from the Context returned here, the receiver is being registered with the global state associated with your application. Thus it will never be unregistered for you. This is necessary if the receiver is associated with static data, not a particular component. However using the ApplicationContext elsewhere can easily lead to serious leaks if you forget to unregister, unbind, etc.

<br />

`https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo.html#!` getApplicationInfo

Return the full application info for this context's package.

<br />

`https://developer.android.com/reference/kotlin/android/content/res/AssetManager.html#!` getAssets

Returns an AssetManager instance for the application's package.

**Note:** Implementations of this method should return an AssetManager instance that is consistent with the Resources instance returned by getResources. For example, they should share the same `https://developer.android.com/reference/kotlin/android/content/res/Configuration.html#` object.

<br />

`https://developer.android.com/reference/kotlin/android/content/AttributionSource.html#` getAttributionSource

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?` getAttributionTag

Attribution can be used in complex apps to logically separate parts of the app. E.g. a blogging app might also have a instant messaging app built in. In this case two separate tags can for used each sub-feature.

<br />

`https://developer.android.com/reference/kotlin/android/content/Context.html#!` getBaseContext

<br />

`https://developer.android.com/reference/kotlin/java/io/File.html#!` getCacheDir

Returns the absolute path to the application specific cache directory on the filesystem.

The system will automatically delete files in this directory as disk space is needed elsewhere on the device. The system will always delete older files first, as reported by lastModified. If desired, you can exert more control over how files are deleted using setCacheBehaviorGroup and setCacheBehaviorTombstone.

Apps are strongly encouraged to keep their usage of cache space below the quota returned by getCacheQuotaBytes. If your app goes above this quota, your cached files will be some of the first to be deleted when additional disk space is needed. Conversely, if your app stays under this quota, your cached files will be some of the last to be deleted when additional disk space is needed.

Note that your cache quota will change over time depending on how frequently the user interacts with your app, and depending on how much system-wide disk space is used.

The returned path may change over time if the calling app is moved to an adopted storage device, so only relative paths should be persisted.

Apps require no extra permissions to read or write to the returned path, since this path lives in their private storage.

<br />

`https://developer.android.com/reference/kotlin/java/lang/ClassLoader.html#!` getClassLoader

Return a class loader you can use to retrieve classes in this package.

<br />

`https://developer.android.com/reference/kotlin/java/io/File.html#!` getCodeCacheDir

Returns the absolute path to the application specific cache directory on the filesystem designed for storing cached code.

The system will delete any files stored in this location both when your specific application is upgraded, and when the entire platform is upgraded.

This location is optimal for storing compiled or optimized code generated by your application at runtime.

The returned path may change over time if the calling app is moved to an adopted storage device, so only relative paths should be persisted.

Apps require no extra permissions to read or write to the returned path, since this path lives in their private storage.

<br />

`https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#!` getContentResolver

Return a ContentResolver instance for your application's package.

<br />

`https://developer.android.com/reference/kotlin/java/io/File.html#!` getDataDir

Returns the absolute path to the directory on the filesystem where all private files belonging to this app are stored. Apps should not use this path directly; they should instead use getFilesDir, getCacheDir, getDir, or other storage APIs on this class.

The returned path may change over time if the calling app is moved to an adopted storage device, so only relative paths should be persisted.

No additional permissions are required for the calling app to read or write files under the returned path.

<br />

`https://developer.android.com/reference/kotlin/java/io/File.html#!` getDatabasePath

Returns the absolute path on the filesystem where a database created with #openOrCreateDatabase is stored.

The returned path may change over time if the calling app is moved to an adopted storage device, so only relative paths should be persisted.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` getDeviceId

Gets the device ID this context is associated with. Applications can use this method to determine whether they are running on a virtual device and identify that device. The device ID of the host device is `https://developer.android.com/reference/kotlin/android/content/Context.html#DEVICE_ID_DEFAULT:kotlin.Int`

If the underlying device ID is changed by the system, for example, when an `https://developer.android.com/reference/kotlin/android/app/Activity.html#` is moved to a different virtual device, applications can register to listen to changes by calling registerDeviceIdChangeListener.

This method will only return a reliable value for this instance if it was created with createDeviceContext, or if this instance is a UI or Display Context. Contexts created with createDeviceContext will have an explicit device association, which will never change, even if the underlying device is closed or is removed. UI Contexts and Display Contexts are already associated with a display, so if the device association is not explicitly given, getDeviceId will return the ID of the device associated with the associated display. The system can assign an arbitrary device id value for Contexts not logically associated with a device.

<br />

`https://developer.android.com/reference/kotlin/java/io/File.html#!` getDir

Retrieve, creating if needed, a new directory in which the application can place its own custom data files. You can use the returned File object to create and access files in this directory. Note that files created through a File object will only be accessible by your own application; you can only set the mode of the entire directory, not of individual files.

The returned path may change over time if the calling app is moved to an adopted storage device, so only relative paths should be persisted.

Apps require no extra permissions to read or write to the returned path, since this path lives in their private storage.

<br />

`https://developer.android.com/reference/kotlin/android/view/Display.html#!` getDisplay

Get the display this context is associated with. Applications should use this method with `https://developer.android.com/reference/kotlin/android/app/Activity.html#` or a context associated with a `https://developer.android.com/reference/kotlin/android/view/Display.html#` via createDisplayContext to get a display object associated with a Context, or getDisplay to get a display object by id.

<br />

`https://developer.android.com/reference/kotlin/java/io/File.html#?` getExternalCacheDir

Returns absolute path to application-specific directory on the primary shared/external storage device where the application can place cache files it owns. These files are internal to the application, and not typically visible to the user as media.

This is like getCacheDir in that these files will be deleted when the application is uninstalled, however there are some important differences:

- The platform does not always monitor the space available in shared storage, and thus may not automatically delete these files. Apps should always manage the maximum space used in this location. Currently the only time files here will be deleted by the platform is when running on `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#JELLY_BEAN_MR1:kotlin.Int` or later and isExternalStorageEmulated returns true.
- Shared storage may not always be available, since removable media can be ejected by the user. Media state can be checked using getExternalStorageState.
- There is no security enforced with these files. For example, any application holding `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#WRITE_EXTERNAL_STORAGE:kotlin.String` can write to these files.

If a shared storage device is emulated (as determined by isExternalStorageEmulated), its contents are backed by a private user data partition, which means there is little benefit to storing data here instead of the private directory returned by getCacheDir.

Starting in `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#KITKAT:kotlin.Int`, no permissions are required to read or write to the returned path; it's always accessible to the calling app. This only applies to paths generated for package name of the calling application. To access paths belonging to other packages, `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#WRITE_EXTERNAL_STORAGE:kotlin.String` and/or `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_EXTERNAL_STORAGE:kotlin.String` are required.

On devices with multiple users (as described by `https://developer.android.com/reference/kotlin/android/os/UserManager.html#`), each user has their own isolated shared storage. Applications only have access to the shared storage for the user they're running as.

The returned path may change over time if different shared storage media is inserted, so only relative paths should be persisted.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/java/io/File.html#!>!` getExternalCacheDirs

Returns absolute paths to application-specific directories on all shared/external storage devices where the application can place cache files it owns. These files are internal to the application, and not typically visible to the user as media.

This is like getCacheDir in that these files will be deleted when the application is uninstalled, however there are some important differences:

- The platform does not always monitor the space available in shared storage, and thus may not automatically delete these files. Apps should always manage the maximum space used in this location. Currently the only time files here will be deleted by the platform is when running on `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#JELLY_BEAN_MR1:kotlin.Int` or later and isExternalStorageEmulated returns true.
- Shared storage may not always be available, since removable media can be ejected by the user. Media state can be checked using getExternalStorageState.
- There is no security enforced with these files. For example, any application holding `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#WRITE_EXTERNAL_STORAGE:kotlin.String` can write to these files.

If a shared storage device is emulated (as determined by isExternalStorageEmulated), its contents are backed by a private user data partition, which means there is little benefit to storing data here instead of the private directory returned by getCacheDir.

Shared storage devices returned here are considered a stable part of the device, including physical media slots under a protective cover. The returned paths do not include transient devices, such as USB flash drives connected to handheld devices.

An application may store data on any or all of the returned devices. For example, an app may choose to store large files on the device with the most available space, as measured by `https://developer.android.com/reference/kotlin/android/os/StatFs.html#`.

No additional permissions are required for the calling app to read or write files under the returned path. Write access outside of these paths on secondary external storage devices is not available.

The returned paths may change over time if different shared storage media is inserted, so only relative paths should be persisted.

<br />

`https://developer.android.com/reference/kotlin/java/io/File.html#?` getExternalFilesDir

Returns the absolute path to the directory on the primary shared/external storage device where the application can place persistent files it owns. These files are internal to the applications, and not typically visible to the user as media.

This is like getFilesDir in that these files will be deleted when the application is uninstalled, however there are some important differences:

- Shared storage may not always be available, since removable media can be ejected by the user. Media state can be checked using getExternalStorageState.
- There is no security enforced with these files. For example, any application holding `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#WRITE_EXTERNAL_STORAGE:kotlin.String` can write to these files.

If a shared storage device is emulated (as determined by isExternalStorageEmulated), its contents are backed by a private user data partition, which means there is little benefit to storing data here instead of the private directories returned by getFilesDir, etc.

Starting in `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#KITKAT:kotlin.Int`, no permissions are required to read or write to the returned path; it's always accessible to the calling app. This only applies to paths generated for package name of the calling application. To access paths belonging to other packages, `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#WRITE_EXTERNAL_STORAGE:kotlin.String` and/or `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_EXTERNAL_STORAGE:kotlin.String` are required.

On devices with multiple users (as described by `https://developer.android.com/reference/kotlin/android/os/UserManager.html#`), each user has their own isolated shared storage. Applications only have access to the shared storage for the user they're running as.

The returned path may change over time if different shared storage media is inserted, so only relative paths should be persisted.

Here is an example of typical code to manipulate a file in an application's shared storage:

If you supply a non-null type to this function, the returned file will be a path to a sub-directory of the given type. Though these files are not automatically scanned by the media scanner, you can explicitly add them to the media database with scanFile. Note that this is not the same as getExternalStoragePublicDirectory, which provides directories of media shared by all applications. The directories returned here are owned by the application, and their contents will be removed when the application is uninstalled. Unlike getExternalStoragePublicDirectory, the directory returned here will be automatically created for you.

Here is an example of typical code to manipulate a picture in an application's shared storage and add it to the media database:

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/java/io/File.html#!>!` getExternalFilesDirs

Returns absolute paths to application-specific directories on all shared/external storage devices where the application can place persistent files it owns. These files are internal to the application, and not typically visible to the user as media.

This is like getFilesDir in that these files will be deleted when the application is uninstalled, however there are some important differences:

- Shared storage may not always be available, since removable media can be ejected by the user. Media state can be checked using getExternalStorageState.
- There is no security enforced with these files. For example, any application holding `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#WRITE_EXTERNAL_STORAGE:kotlin.String` can write to these files.

If a shared storage device is emulated (as determined by isExternalStorageEmulated), its contents are backed by a private user data partition, which means there is little benefit to storing data here instead of the private directories returned by getFilesDir, etc.

Shared storage devices returned here are considered a stable part of the device, including physical media slots under a protective cover. The returned paths do not include transient devices, such as USB flash drives connected to handheld devices.

An application may store data on any or all of the returned devices. For example, an app may choose to store large files on the device with the most available space, as measured by `https://developer.android.com/reference/kotlin/android/os/StatFs.html#`.

No additional permissions are required for the calling app to read or write files under the returned path. Write access outside of these paths on secondary external storage devices is not available.

The returned path may change over time if different shared storage media is inserted, so only relative paths should be persisted.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/java/io/File.html#!>!` getExternalMediaDirs

Returns absolute paths to application-specific directories on all shared/external storage devices where the application can place media files. These files are scanned and made available to other apps through `https://developer.android.com/reference/kotlin/android/provider/MediaStore.html#`.

This is like getExternalFilesDirs in that these files will be deleted when the application is uninstalled, however there are some important differences:

- Shared storage may not always be available, since removable media can be ejected by the user. Media state can be checked using getExternalStorageState.
- There is no security enforced with these files. For example, any application holding `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#WRITE_EXTERNAL_STORAGE:kotlin.String` can write to these files.

Shared storage devices returned here are considered a stable part of the device, including physical media slots under a protective cover. The returned paths do not include transient devices, such as USB flash drives connected to handheld devices.

An application may store data on any or all of the returned devices. For example, an app may choose to store large files on the device with the most available space, as measured by `https://developer.android.com/reference/kotlin/android/os/StatFs.html#`.

No additional permissions are required for the calling app to read or write files under the returned path. Write access outside of these paths on secondary external storage devices is not available.

The returned paths may change over time if different shared storage media is inserted, so only relative paths should be persisted.

<br />

`https://developer.android.com/reference/kotlin/java/io/File.html#!` getFileStreamPath

Returns the absolute path on the filesystem where a file created with openFileOutput is stored.

The returned path may change over time if the calling app is moved to an adopted storage device, so only relative paths should be persisted.

<br />

`https://developer.android.com/reference/kotlin/java/io/File.html#!` getFilesDir

Returns the absolute path to the directory on the filesystem where files created with openFileOutput are stored.

The returned path may change over time if the calling app is moved to an adopted storage device, so only relative paths should be persisted.

No additional permissions are required for the calling app to read or write files under the returned path.

<br />

`https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#!` getMainExecutor

Return an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that will run enqueued tasks on the main thread associated with this context. This is the thread used to dispatch calls to application components (activities, services, etc).

<br />

`https://developer.android.com/reference/kotlin/android/os/Looper.html#!` getMainLooper

Return the Looper for the main thread of the current process. This is the thread used to dispatch calls to application components (activities, services, etc).

By definition, this method returns the same result as would be obtained by calling getMainLooper.

<br />

`https://developer.android.com/reference/kotlin/java/io/File.html#!` getNoBackupFilesDir

Returns the absolute path to the directory on the filesystem similar to getFilesDir. The difference is that files placed under this directory will be excluded from automatic backup to remote storage. See BackupAgent for a full discussion of the automatic backup mechanism in Android.

The returned path may change over time if the calling app is moved to an adopted storage device, so only relative paths should be persisted.

No additional permissions are required for the calling app to read or write files under the returned path.

<br />

`https://developer.android.com/reference/kotlin/java/io/File.html#!` getObbDir

Return the primary shared/external storage directory where this application's OBB files (if there are any) can be found. Note if the application does not have any OBB files, this directory may not exist.

This is like getFilesDir in that these files will be deleted when the application is uninstalled, however there are some important differences:

- Shared storage may not always be available, since removable media can be ejected by the user. Media state can be checked using getExternalStorageState.
- There is no security enforced with these files. For example, any application holding `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#WRITE_EXTERNAL_STORAGE:kotlin.String` can write to these files.

Starting in `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#KITKAT:kotlin.Int`, no permissions are required to read or write to the path that this method returns. However, starting from `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#M:kotlin.Int`, to read the OBB expansion files, you must declare the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_EXTERNAL_STORAGE:kotlin.String` permission in the app manifest and ask for permission at runtime as follows:

`<uses-permission android:name="android.permission.READ_EXTERNAL_STORAGE" android:maxSdkVersion="23" />`

Starting from `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#N:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_EXTERNAL_STORAGE:kotlin.String` permission is not required, so don't ask for this permission at runtime. To handle both cases, your app must first try to read the OBB file, and if it fails, you must request `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_EXTERNAL_STORAGE:kotlin.String` permission at runtime.

The following code snippet shows how to do this:

```kotlin
File obb = new File(obb_filename);
  boolean open_failed = false;
 
  try {
      BufferedReader br = new BufferedReader(new FileReader(obb));
      open_failed = false;
      ReadObbFile(br);
  } catch (IOException e) {
      open_failed = true;
  }
 
  if (open_failed) {
      // request READ_EXTERNAL_STORAGE permission before reading OBB file
      ReadObbFileWithPermission();
  }
  
```
On devices with multiple users (as described by `https://developer.android.com/reference/kotlin/android/os/UserManager.html#`), multiple users may share the same OBB storage location. Applications should ensure that multiple instances running under different users don't interfere with each other.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/java/io/File.html#!>!` getObbDirs

Returns absolute paths to application-specific directories on all shared/external storage devices where the application's OBB files (if there are any) can be found. Note if the application does not have any OBB files, these directories may not exist.

This is like getFilesDir in that these files will be deleted when the application is uninstalled, however there are some important differences:

- Shared storage may not always be available, since removable media can be ejected by the user. Media state can be checked using getExternalStorageState.
- There is no security enforced with these files. For example, any application holding `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#WRITE_EXTERNAL_STORAGE:kotlin.String` can write to these files.

Shared storage devices returned here are considered a stable part of the device, including physical media slots under a protective cover. The returned paths do not include transient devices, such as USB flash drives connected to handheld devices.

An application may store data on any or all of the returned devices. For example, an app may choose to store large files on the device with the most available space, as measured by `https://developer.android.com/reference/kotlin/android/os/StatFs.html#`.

No additional permissions are required for the calling app to read or write files under the returned path. Write access outside of these paths on secondary external storage devices is not available.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` getOpPackageName

Return the package name that should be used for `https://developer.android.com/reference/kotlin/android/app/AppOpsManager.html#` calls from this context, so that app ops manager's uid verification will work with the name.

This is not generally intended for third party application developers.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` getPackageCodePath

Return the full path to this context's primary Android package. The Android package is a ZIP file which contains application's primary code and assets.

Note: this is not generally useful for applications, since they should not be directly accessing the file system.

<br />

`https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#!` getPackageManager

Return PackageManager instance to find global package information.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` getPackageName

Return the name of this application's package.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` getPackageResourcePath

Return the full path to this context's primary Android package. The Android package is a ZIP file which contains the application's primary resources.

Note: this is not generally useful for applications, since they should not be directly accessing the file system.

<br />

`https://developer.android.com/reference/kotlin/android/content/ContextParams.html#?` getParams

Return the set of parameters which this Context was created with, if it was created via createContext.

<br />

`https://developer.android.com/reference/kotlin/android/content/res/Resources.html#!` getResources

Returns a Resources instance for the application's package.

**Note:** Implementations of this method should return a Resources instance that is consistent with the AssetManager instance returned by getAssets. For example, they should share the same `https://developer.android.com/reference/kotlin/android/content/res/Configuration.html#` object.

<br />

`https://developer.android.com/reference/kotlin/android/content/SharedPreferences.html#!` getSharedPreferences

Retrieve and hold the contents of the preferences file 'name', returning a SharedPreferences through which you can retrieve and modify its values. Only one instance of the SharedPreferences object is returned to any callers for the same name, meaning they will see each other's edits as soon as they are made.

This method is thread-safe.

If the preferences directory does not already exist, it will be created when this method is called.

If a preferences file by this name does not exist, it will be created when you retrieve an editor (edit) and then commit changes (commit or apply).

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!` getSystemService

Return the handle to a system-level service by name. The class of the returned object varies by the requested name. Currently available names are:

`https://developer.android.com/reference/kotlin/android/content/Context.html#WINDOW_SERVICE:kotlin.String` ("window")
: The top-level window manager in which you can place custom windows. The returned object is a `https://developer.android.com/reference/kotlin/android/view/WindowManager.html#`. Must only be obtained from a visual context such as Activity or a Context created with createWindowContext, which are adjusted to the configuration and visual bounds of an area on screen.

`https://developer.android.com/reference/kotlin/android/content/Context.html#LAYOUT_INFLATER_SERVICE:kotlin.String` ("layout_inflater")
: A `https://developer.android.com/reference/kotlin/android/view/LayoutInflater.html#` for inflating layout resources in this context. Must only be obtained from a visual context such as Activity or a Context created with createWindowContext, which are adjusted to the configuration and visual bounds of an area on screen.

`https://developer.android.com/reference/kotlin/android/content/Context.html#ACTIVITY_SERVICE:kotlin.String` ("activity")
: A `https://developer.android.com/reference/kotlin/android/app/ActivityManager.html#` for interacting with the global activity state of the system.

`https://developer.android.com/reference/kotlin/android/content/Context.html#WALLPAPER_SERVICE:kotlin.String` ("wallpaper")
: A `https://developer.android.com/reference/kotlin/android/service/wallpaper/WallpaperService.html#` for accessing wallpapers in this context. Must only be obtained from a visual context such as Activity or a Context created with createWindowContext, which are adjusted to the configuration and visual bounds of an area on screen.

`https://developer.android.com/reference/kotlin/android/content/Context.html#POWER_SERVICE:kotlin.String` ("power")
: A `https://developer.android.com/reference/kotlin/android/os/PowerManager.html#` for controlling power management.

`https://developer.android.com/reference/kotlin/android/content/Context.html#ALARM_SERVICE:kotlin.String` ("alarm")
: A `https://developer.android.com/reference/kotlin/android/app/AlarmManager.html#` for receiving intents at the time of your choosing.

`https://developer.android.com/reference/kotlin/android/content/Context.html#NOTIFICATION_SERVICE:kotlin.String` ("notification")
: A `https://developer.android.com/reference/kotlin/android/app/NotificationManager.html#` for informing the user of background events.

`https://developer.android.com/reference/kotlin/android/content/Context.html#KEYGUARD_SERVICE:kotlin.String` ("keyguard")
: A `https://developer.android.com/reference/kotlin/android/app/KeyguardManager.html#` for controlling keyguard.

`https://developer.android.com/reference/kotlin/android/content/Context.html#LOCATION_SERVICE:kotlin.String` ("location")
: A `https://developer.android.com/reference/kotlin/android/location/LocationManager.html#` for controlling location (e.g., GPS) updates.

`https://developer.android.com/reference/kotlin/android/content/Context.html#SEARCH_SERVICE:kotlin.String` ("search")
: A `https://developer.android.com/reference/kotlin/android/app/SearchManager.html#` for handling search.

`https://developer.android.com/reference/kotlin/android/content/Context.html#VIBRATOR_MANAGER_SERVICE:kotlin.String` ("vibrator_manager")
: A `https://developer.android.com/reference/kotlin/android/os/VibratorManager.html#` for accessing the device vibrators, interacting with individual ones and playing synchronized effects on multiple vibrators.

`https://developer.android.com/reference/kotlin/android/content/Context.html#MULTISENSORY_MANAGER_SERVICE:kotlin.String` ("multisensory_manager")
: A `https://developer.android.com/reference/kotlin/android/os/multisensory/MultisensoryManager.html#` for delivering audio-haptic feedback in the Multisensory Design System

`https://developer.android.com/reference/kotlin/android/content/Context.html#VIBRATOR_SERVICE:kotlin.String` ("vibrator")
: A `https://developer.android.com/reference/kotlin/android/os/Vibrator.html#` for interacting with the vibrator hardware.

`https://developer.android.com/reference/kotlin/android/content/Context.html#CONNECTIVITY_SERVICE:kotlin.String` ("connectivity")
: A `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager.html#` for handling management of network connections.

`https://developer.android.com/reference/kotlin/android/content/Context.html#IPSEC_SERVICE:kotlin.String` ("ipsec")
: A `https://developer.android.com/reference/kotlin/android/net/IpSecManager.html#` for managing IPSec on sockets and networks.

`https://developer.android.com/reference/kotlin/android/content/Context.html#WIFI_SERVICE:kotlin.String` ("wifi")
: A `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager.html#` for management of Wi-Fi connectivity. On releases before Android 7, it should only be obtained from an application context, and not from any other derived context to avoid memory leaks within the calling process.

`https://developer.android.com/reference/kotlin/android/content/Context.html#WIFI_AWARE_SERVICE:kotlin.String` ("wifiaware")
: A `https://developer.android.com/reference/kotlin/android/net/wifi/aware/WifiAwareManager.html#` for management of Wi-Fi Aware discovery and connectivity.

`https://developer.android.com/reference/kotlin/android/content/Context.html#WIFI_P2P_SERVICE:kotlin.String` ("wifip2p")
: A `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.html#` for management of Wi-Fi Direct connectivity.

`https://developer.android.com/reference/kotlin/android/content/Context.html#INPUT_METHOD_SERVICE:kotlin.String` ("input_method")
: An `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager.html#` for management of input methods.

`https://developer.android.com/reference/kotlin/android/content/Context.html#UI_MODE_SERVICE:kotlin.String` ("uimode")
: An `https://developer.android.com/reference/kotlin/android/app/UiModeManager.html#` for controlling UI modes.

`https://developer.android.com/reference/kotlin/android/content/Context.html#DOWNLOAD_SERVICE:kotlin.String` ("download")
: A `https://developer.android.com/reference/kotlin/android/app/DownloadManager.html#` for requesting HTTP downloads

`https://developer.android.com/reference/kotlin/android/content/Context.html#BATTERY_SERVICE:kotlin.String` ("batterymanager")
: A `https://developer.android.com/reference/kotlin/android/os/BatteryManager.html#` for managing battery state

`https://developer.android.com/reference/kotlin/android/content/Context.html#JOB_SCHEDULER_SERVICE:kotlin.String` ("taskmanager")
: A `https://developer.android.com/reference/kotlin/android/app/job/JobScheduler.html#` for managing scheduled tasks

`https://developer.android.com/reference/kotlin/android/content/Context.html#NETWORK_STATS_SERVICE:kotlin.String` ("netstats")
: A `https://developer.android.com/reference/kotlin/android/app/usage/NetworkStatsManager.html#` for querying network usage statistics.

`https://developer.android.com/reference/kotlin/android/content/Context.html#HARDWARE_PROPERTIES_SERVICE:kotlin.String` ("hardware_properties")
: A `https://developer.android.com/reference/kotlin/android/os/HardwarePropertiesManager.html#` for accessing hardware properties.

`https://developer.android.com/reference/kotlin/android/content/Context.html#DOMAIN_VERIFICATION_SERVICE:kotlin.String` ("domain_verification")
: A `https://developer.android.com/reference/kotlin/android/content/pm/verify/domain/DomainVerificationManager.html#` for accessing web domain approval state.

`https://developer.android.com/reference/kotlin/android/content/Context.html#DISPLAY_HASH_SERVICE:kotlin.String` ("display_hash")
: A `https://developer.android.com/reference/kotlin/android/view/displayhash/DisplayHashManager.html#` for management of display hashes.

`https://developer.android.com/reference/kotlin/android/content/Context.html#AUTHENTICATION_POLICY_SERVICE:kotlin.String` ("authentication_policy")
: A `https://developer.android.com/reference/kotlin/android/security/authenticationpolicy/AuthenticationPolicyManager.html#` for managing authentication related policies on the device.

<br />

Note: System services obtained via this API may be closely associated with the Context in which they are obtained from. In general, do not share the service objects between various different contexts (Activities, Applications, Services, Providers, etc.)

Note: Instant apps, for which isInstantApp returns true, don't have access to the following system services: `https://developer.android.com/reference/kotlin/android/content/Context.html#DEVICE_POLICY_SERVICE:kotlin.String`, #FINGERPRINT_SERVICE, `https://developer.android.com/reference/kotlin/android/content/Context.html#KEYGUARD_SERVICE:kotlin.String`, `https://developer.android.com/reference/kotlin/android/content/Context.html#SHORTCUT_SERVICE:kotlin.String`, `https://developer.android.com/reference/kotlin/android/content/Context.html#USB_SERVICE:kotlin.String`, `https://developer.android.com/reference/kotlin/android/content/Context.html#WALLPAPER_SERVICE:kotlin.String`, `https://developer.android.com/reference/kotlin/android/content/Context.html#WIFI_P2P_SERVICE:kotlin.String`, `https://developer.android.com/reference/kotlin/android/content/Context.html#WIFI_SERVICE:kotlin.String`, `https://developer.android.com/reference/kotlin/android/content/Context.html#WIFI_AWARE_SERVICE:kotlin.String`. For these services this method will return `null`. Generally, if you are running as an instant app you should always check whether the result of this method is `null`.

Note: When implementing this method, keep in mind that new services can be added on newer Android releases, so if you're looking for just the explicit names mentioned above, make sure to return `null` when you don't recognize the name --- if you throw a `https://developer.android.com/reference/kotlin/java/lang/RuntimeException.html#` exception instead, your app might break on new Android releases.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?` getSystemServiceName

Gets the name of the system-level service that is represented by the specified class.

<br />

`https://developer.android.com/reference/kotlin/android/content/res/Resources.Theme.html#!` getTheme

Return the Theme object associated with this Context.

<br />

`https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#!` getWallpaper

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` getWallpaperDesiredMinimumHeight

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` getWallpaperDesiredMinimumWidth

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` grantUriPermission

Grant permission to access a specific Uri to another package, regardless of whether that package has general permission to access the Uri's content provider. This can be used to grant specific, temporary permissions, typically in response to user interaction (such as the user opening an attachment that you would like someone else to display).

Normally you should use `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_GRANT_READ_URI_PERMISSION:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_GRANT_WRITE_URI_PERMISSION:kotlin.Int` with the Intent being used to start an activity instead of this function directly. If you use this function directly, you should be sure to call #revokeUriPermission when the target should no longer be allowed to access it.

To succeed, the content provider owning the Uri must have set the `https://developer.android.com/reference/kotlin/android/R.styleable.html#AndroidManifestProvider_grantUriPermissions:kotlin.Int` attribute in its manifest or included the `https://developer.android.com/reference/kotlin/android/R.styleable.html#AndroidManifestGrantUriPermission:kotlin.IntArray` tag.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` isDeviceProtectedStorage

Indicates if the storage APIs of this Context are backed by device-protected storage.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` isRestricted

Indicates whether this Context is restricted.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` isUiContext

Returns `true` if the context is a UI context which can access UI components such as `https://developer.android.com/reference/kotlin/android/view/WindowManager.html#`, `https://developer.android.com/reference/kotlin/android/view/LayoutInflater.html#` or `https://developer.android.com/reference/kotlin/android/app/WallpaperManager.html#`. Accessing UI components from non-UI contexts throws `https://developer.android.com/reference/kotlin/android/os/strictmode/Violation.html#` if detectIncorrectContextUse is enabled.

Examples of UI contexts are an `https://developer.android.com/reference/kotlin/android/app/Activity.html#`, a context created from createWindowContext or `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService.html#`

Note that even if it is allowed programmatically, it is not suggested to override this method to bypass `https://developer.android.com/reference/kotlin/android/os/strictmode/IncorrectContextUseViolation.html#` verification.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` moveDatabaseFrom

Move an existing database file from the given source storage context to this context. This is typically used to migrate data between storage locations after an upgrade, such as migrating to device protected storage.

The database must be closed before being moved.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` moveSharedPreferencesFrom

Move an existing shared preferences file from the given source storage context to this context. This is typically used to migrate data between storage locations after an upgrade, such as moving to device protected storage.

<br />

`https://developer.android.com/reference/kotlin/java/io/FileInputStream.html#!` openFileInput

Open a private file associated with this Context's application package for reading.

<br />

`https://developer.android.com/reference/kotlin/java/io/FileOutputStream.html#!` openFileOutput

Open a private file associated with this Context's application package for writing. Creates the file if it doesn't already exist.

No additional permissions are required for the calling app to read or write the returned file.

<br />

`https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase.html#!` openOrCreateDatabase

Open a new private SQLiteDatabase associated with this Context's application package. Create the database file if it doesn't exist.

<br />

`https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase.html#!` openOrCreateDatabase

Open a new private SQLiteDatabase associated with this Context's application package. Creates the database file if it doesn't exist.

Accepts input param: a concrete instance of `https://developer.android.com/reference/kotlin/android/database/DatabaseErrorHandler.html#` to be used to handle corruption when sqlite reports database corruption.

<br />

`https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#!` peekWallpaper

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` rebindService

Rebind an application service with updated bind service flags

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` registerComponentCallbacks

Add a new `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks.html#` to the base application of the Context, which will be called at the same times as the ComponentCallbacks methods of activities and other components are called. Note that you *must* be sure to use unregisterComponentCallbacks when appropriate in the future; this will not be removed for you.

After `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#TIRAMISU:kotlin.Int`, the `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks.html#` will be registered to getBaseContext, and can be only used after attachBaseContext. Users can still call to `getApplicationContext().registerComponentCallbacks(ComponentCallbacks)` to add `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks.html#` to the base application.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` registerDeviceIdChangeListener

Adds a new device ID changed listener to the `Context`, which will be called when the device association is changed by the system.

The callback can be called when an app is moved to a different device and the `Context` is not explicitly associated with a specific device.

When an application receives a device id update callback, this Context is guaranteed to also have an updated display ID(if any) and `https://developer.android.com/reference/kotlin/android/content/res/Configuration.html#`.

<br />

<br />

`https://developer.android.com/reference/kotlin/android/content/Intent.html#?` registerReceiver

Register a BroadcastReceiver to be run in the main activity thread. The receiver will be called with any broadcast Intent that matches filter, in the main application thread.

The system may broadcast Intents that are "sticky" -- these stay around after the broadcast has finished, to be sent to any later registrations. If your IntentFilter matches one of these sticky Intents, that Intent will be returned by this function **and** sent to your receiver as if it had just been broadcast.

There may be multiple sticky Intents that match filter, in which case each of these will be sent to receiver. In this case, only one of these can be returned directly by the function; which of these that is returned is arbitrarily decided by the system.

If you know the Intent you are registering for is sticky, you can supply null for your receiver. In this case, no receiver is registered -- the function simply returns the sticky Intent that matches filter. In the case of multiple matches, the same rules as described above apply.

See `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#` for more information on Intent broadcasts.

As of `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#UPSIDE_DOWN_CAKE:kotlin.Int`, the system can [place context-registered broadcasts in a queue while the app is in the](https://developer.android.com/develop/background-work/background-tasks/broadcasts#android-14) [cached state](https://developer.android.com/guide/components/activities/process-lifecycle). When the app leaves the cached state, such as returning to the foreground, the system delivers any queued broadcasts. Multiple instances of certain broadcasts might be merged into one broadcast.

As of `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#ICE_CREAM_SANDWICH:kotlin.Int`, receivers registered with this method will correctly respect the setPackage specified for an Intent being broadcast. Prior to that, it would be ignored and delivered to all matching registered receivers. Be careful if using this for security.

For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#UPSIDE_DOWN_CAKE:kotlin.Int`, either `https://developer.android.com/reference/kotlin/android/content/Context.html#RECEIVER_EXPORTED:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/content/Context.html#RECEIVER_NOT_EXPORTED:kotlin.Int` must be specified if the receiver is not being registered for [system broadcasts](https://developer.android.com/guide/components/broadcasts#system-broadcasts) or a `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#` will be thrown. See registerReceiver to register a receiver with flags.

Note: this method *cannot be called from a `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#` component;* that is, from a BroadcastReceiver that is declared in an application's manifest. It is okay, however, to call this method from another BroadcastReceiver that has itself been registered at run time with #registerReceiver, since the lifetime of such a registered BroadcastReceiver is tied to the object that registered it.

<br />

`https://developer.android.com/reference/kotlin/android/content/Intent.html#?` registerReceiver

Register to receive intent broadcasts, with the receiver optionally being exposed to Instant Apps. See registerReceiver for more information. By default Instant Apps cannot interact with receivers in other applications, this allows you to expose a receiver that Instant Apps can interact with.

See `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#` for more information on Intent broadcasts.

As of `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#UPSIDE_DOWN_CAKE:kotlin.Int`, the system can [place context-registered broadcasts in a queue while the app is in the](https://developer.android.com/develop/background-work/background-tasks/broadcasts#android-14) [cached state](https://developer.android.com/guide/components/activities/process-lifecycle). When the app leaves the cached state, such as returning to the foreground, the system delivers any queued broadcasts. Multiple instances of certain broadcasts might be merged into one broadcast.

As of `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#ICE_CREAM_SANDWICH:kotlin.Int`, receivers registered with this method will correctly respect the setPackage specified for an Intent being broadcast. Prior to that, it would be ignored and delivered to all matching registered receivers. Be careful if using this for security.

<br />

`https://developer.android.com/reference/kotlin/android/content/Intent.html#?` registerReceiver

Register to receive intent broadcasts, to run in the context of scheduler. See registerReceiver for more information. This allows you to enforce permissions on who can broadcast intents to your receiver, or have the receiver run in a different thread than the main application thread.

See `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#` for more information on Intent broadcasts.

As of `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#UPSIDE_DOWN_CAKE:kotlin.Int`, the system can [place context-registered broadcasts in a queue while the app is in the](https://developer.android.com/develop/background-work/background-tasks/broadcasts#android-14) [cached state](https://developer.android.com/guide/components/activities/process-lifecycle). When the app leaves the cached state, such as returning to the foreground, the system delivers any queued broadcasts. Multiple instances of certain broadcasts might be merged into one broadcast.

As of `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#ICE_CREAM_SANDWICH:kotlin.Int`, receivers registered with this method will correctly respect the setPackage specified for an Intent being broadcast. Prior to that, it would be ignored and delivered to all matching registered receivers. Be careful if using this for security.

For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#UPSIDE_DOWN_CAKE:kotlin.Int`, either `https://developer.android.com/reference/kotlin/android/content/Context.html#RECEIVER_EXPORTED:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/content/Context.html#RECEIVER_NOT_EXPORTED:kotlin.Int` must be specified if the receiver is not being registered for [system broadcasts](https://developer.android.com/guide/components/broadcasts#system-broadcasts) or a `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#` will be thrown. See registerReceiver to register a receiver with flags.

<br />

`https://developer.android.com/reference/kotlin/android/content/Intent.html#?` registerReceiver

Register to receive intent broadcasts, to run in the context of scheduler. See registerReceiver and registerReceiver for more information.

See `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#` for more information on Intent broadcasts.

As of `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#UPSIDE_DOWN_CAKE:kotlin.Int`, the system can [place context-registered broadcasts in a queue while the app is in the](https://developer.android.com/develop/background-work/background-tasks/broadcasts#android-14) [cached state](https://developer.android.com/guide/components/activities/process-lifecycle). When the app leaves the cached state, such as returning to the foreground, the system delivers any queued broadcasts. Multiple instances of certain broadcasts might be merged into one broadcast.

As of `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#ICE_CREAM_SANDWICH:kotlin.Int`, receivers registered with this method will correctly respect the setPackage specified for an Intent being broadcast. Prior to that, it would be ignored and delivered to all matching registered receivers. Be careful if using this for security.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` removeStickyBroadcast

Remove the data previously sent with #sendStickyBroadcast, so that it is as if the sticky broadcast had never happened. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BROADCAST_STICKY:kotlin.String`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` removeStickyBroadcastAsUser

Version of removeStickyBroadcast that allows you to specify the user the broadcast will be sent to. This is not available to applications that are not pre-installed on the system image.

You must hold the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BROADCAST_STICKY:kotlin.String` permission in order to use this API. If you do not hold that permission, `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#` will be thrown. 
Requires android.Manifest.permission.INTERACT_ACROSS_USERS and `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BROADCAST_STICKY:kotlin.String`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` revokeSelfPermissionsOnKill

Triggers the revocation of one or more permissions for the calling package. A package is only able to revoke runtime permissions. If a permission is not currently granted, it is ignored and will not get revoked (even if later granted by the user). Ultimately, you should never make assumptions about a permission status as users may grant or revoke them at any time.

Background permissions which have no corresponding foreground permission still granted once the revocation is effective will also be revoked.

The revocation happens asynchronously and kills all processes running in the calling UID. It will be triggered once it is safe to do so. In particular, it will not be triggered as long as the package remains in the foreground, or has any active manifest components (e.g. when another app is accessing a content provider in the package).

If you want to revoke the permissions right away, you could call `System.exit()` in `Handler.postDelayed` with a delay to allow completion of async IPC, But `System.exit()` could affect other apps that are accessing your app at the moment. For example, apps accessing a content provider in your app will all crash.

Note that the settings UI shows a permission group as granted as long as at least one permission in the group is granted. If you want the user to observe the revocation in the settings, you should revoke every permission in the target group. To learn the current list of permissions in a group, you may use getGroupOfPlatformPermission and getPlatformPermissionsForGroup. This list of permissions may evolve over time, so it is recommended to check whether it contains any permission you wish to retain before trying to revoke an entire group.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` revokeUriPermission

Remove all permissions to access a particular content provider Uri that were previously added with grantUriPermission or *any other* mechanism. The given Uri will match all previously granted Uris that are the same or a sub-path of the given Uri. That is, revoking "content://foo/target" will revoke both "content://foo/target" and "content://foo/target/sub", but not "content://foo". It will not remove any prefix grants that exist at a higher level.

Prior to `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#LOLLIPOP:kotlin.Int`, if you did not have regular permission access to a Uri, but had received access to it through a specific Uri permission grant, you could not revoke that grant with this function and a `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#` would be thrown. As of `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#LOLLIPOP:kotlin.Int`, this function will not throw a security exception, but will remove whatever permission grants to the Uri had been given to the app (or none).

Unlike revokeUriPermission, this method impacts all permission grants matching the given Uri, for any package they had been granted to, through any mechanism this had happened (such as indirectly through the clipboard, activity launch, service start, etc). That means this can be potentially dangerous to use, as it can revoke grants that another app could be strongly expecting to stick around.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` revokeUriPermission

Remove permissions to access a particular content provider Uri that were previously added with grantUriPermission for a specific target package. The given Uri will match all previously granted Uris that are the same or a sub-path of the given Uri. That is, revoking "content://foo/target" will revoke both "content://foo/target" and "content://foo/target/sub", but not "content://foo". It will not remove any prefix grants that exist at a higher level.

Unlike revokeUriPermission, this method will *only* revoke permissions that had been explicitly granted through grantUriPermission and only for the package specified. Any matching grants that have happened through other mechanisms (clipboard, activity launching, service starting, etc) will not be removed.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` sendBroadcast

Broadcast the given intent to all interested BroadcastReceivers. This call is asynchronous; it returns immediately, and you will continue executing while the receivers are run. No results are propagated from receivers and receivers can not abort the broadcast. If you want to allow receivers to propagate results or abort the broadcast, you must send an ordered broadcast using sendOrderedBroadcast.

See `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#` for more information on Intent broadcasts.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` sendBroadcast

Broadcast the given intent to all interested BroadcastReceivers, allowing an optional required permission to be enforced. This call is asynchronous; it returns immediately, and you will continue executing while the receivers are run. No results are propagated from receivers and receivers can not abort the broadcast. If you want to allow receivers to propagate results or abort the broadcast, you must send an ordered broadcast using sendOrderedBroadcast.

See `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#` for more information on Intent broadcasts.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` sendBroadcast

Broadcast the given intent to all interested BroadcastReceivers, allowing an optional required permission to be enforced. This call is asynchronous; it returns immediately, and you will continue executing while the receivers are run. No results are propagated from receivers and receivers can not abort the broadcast. If you want to allow receivers to propagate results or abort the broadcast, you must send an ordered broadcast using sendOrderedBroadcast.

See `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#` for more information on Intent broadcasts.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` sendBroadcastAsUser

Version of sendBroadcast that allows you to specify the user the broadcast will be sent to. This is not available to applications that are not pre-installed on the system image. 
Requires android.Manifest.permission.INTERACT_ACROSS_USERS

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` sendBroadcastAsUser

Version of sendBroadcast that allows you to specify the user the broadcast will be sent to. This is not available to applications that are not pre-installed on the system image. 
Requires android.Manifest.permission.INTERACT_ACROSS_USERS

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` sendOrderedBroadcast

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` sendOrderedBroadcast

Broadcast the given intent to all interested BroadcastReceivers, delivering them one at a time to allow more preferred receivers to consume the broadcast before it is delivered to less preferred receivers. This call is asynchronous; it returns immediately, and you will continue executing while the receivers are run.

See `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#` for more information on Intent broadcasts.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` sendOrderedBroadcast

Version of sendBroadcast that allows you to receive data back from the broadcast. This is accomplished by supplying your own BroadcastReceiver when calling, which will be treated as a final receiver at the end of the broadcast -- its onReceive method will be called with the result values collected from the other receivers. The broadcast will be serialized in the same way as calling sendOrderedBroadcast.

Like sendBroadcast, this method is asynchronous; it will return before resultReceiver.onReceive() is called.

See `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#` for more information on Intent broadcasts.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` sendOrderedBroadcast

Broadcast the given intent to all interested BroadcastReceivers, delivering them one at a time to allow more preferred receivers to consume the broadcast before it is delivered to less preferred receivers. This call is asynchronous; it returns immediately, and you will continue executing while the receivers are run.

See `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#` for more information on Intent broadcasts.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` sendOrderedBroadcast

Version of sendBroadcast that allows you to receive data back from the broadcast. This is accomplished by supplying your own BroadcastReceiver when calling, which will be treated as a final receiver at the end of the broadcast -- its onReceive method will be called with the result values collected from the other receivers. The broadcast will be serialized in the same way as calling sendOrderedBroadcast.

Like sendBroadcast, this method is asynchronous; it will return before resultReceiver.onReceive() is called.

See `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#` for more information on Intent broadcasts.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` sendOrderedBroadcast

Version of sendOrderedBroadcast that allows you to specify the App Op to enforce restrictions on which receivers the broadcast will be sent to.

See `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#` for more information on Intent broadcasts.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` sendOrderedBroadcastAsUser

Version of sendOrderedBroadcast that allows you to specify the user the broadcast will be sent to. This is not available to applications that are not pre-installed on the system image.

See `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#` for more information on Intent broadcasts. 
Requires android.Manifest.permission.INTERACT_ACROSS_USERS

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` sendStickyBroadcast

Perform a sendBroadcast that is "sticky," meaning the Intent you are sending stays around after the broadcast is complete, so that others can quickly retrieve that data through the return value of registerReceiver. In all other ways, this behaves the same as sendBroadcast. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BROADCAST_STICKY:kotlin.String`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` sendStickyBroadcast

Perform a sendBroadcast that is "sticky," meaning the Intent you are sending stays around after the broadcast is complete, so that others can quickly retrieve that data through the return value of registerReceiver. In all other ways, this behaves the same as sendBroadcast.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` sendStickyBroadcastAsUser

Version of sendStickyBroadcast that allows you to specify the user the broadcast will be sent to. This is not available to applications that are not pre-installed on the system image. 
Requires android.Manifest.permission.INTERACT_ACROSS_USERS and `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BROADCAST_STICKY:kotlin.String`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` sendStickyOrderedBroadcast

Version of #sendStickyBroadcast that allows you to receive data back from the broadcast. This is accomplished by supplying your own BroadcastReceiver when calling, which will be treated as a final receiver at the end of the broadcast -- its onReceive method will be called with the result values collected from the other receivers. The broadcast will be serialized in the same way as calling sendOrderedBroadcast.

Like sendBroadcast, this method is asynchronous; it will return before resultReceiver.onReceive() is called. Note that the sticky data stored is only the data you initially supply to the broadcast, not the result of any changes made by the receivers.

See `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#` for more information on Intent broadcasts. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BROADCAST_STICKY:kotlin.String`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` sendStickyOrderedBroadcastAsUser

Version of sendStickyOrderedBroadcast that allows you to specify the user the broadcast will be sent to. This is not available to applications that are not pre-installed on the system image.

See `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#` for more information on Intent broadcasts. 
Requires android.Manifest.permission.INTERACT_ACROSS_USERS and `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BROADCAST_STICKY:kotlin.String`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setTheme

Set the base theme for this context. Note that this should be called before any views are instantiated in the Context (for example before calling android.app.Activity#setContentView or android.view.LayoutInflater#inflate).

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setWallpaper

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` setWallpaper

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` shouldShowRequestPermissionRationale

Gets whether you should show UI with rationale before requesting a permission. If the permission does not exist on this SDK level or is not visible to this app, the method will return `false`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` startActivities

Same as startActivities with no options specified.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` startActivities

Launch multiple new activities. This is generally the same as calling startActivity for the first Intent in the array, that activity during its creation calling startActivity for the second entry, etc. Note that unlike that approach, generally none of the activities except the last in the array will be created at this point, but rather will be created when the user first visits them (due to pressing back from the activity on top).

This method throws `https://developer.android.com/reference/kotlin/android/content/ActivityNotFoundException.html#` if there was no Activity found for *any* given Intent. In this case the state of the activity stack is undefined (some Intents in the list may be on it, some not), so you probably want to avoid such situations.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` startActivity

Same as startActivity with no options specified.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` startActivity

Launch a new activity. You will not receive any information about when the activity exits.

Note that if this method is being called from outside of an `https://developer.android.com/reference/kotlin/android/app/Activity.html#` Context, then the Intent must include the `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_ACTIVITY_NEW_TASK:kotlin.Int` launch flag. This is because, without being started from an existing Activity, there is no existing task in which to place the new activity and thus it needs to be placed in its own separate task.

This method throws `https://developer.android.com/reference/kotlin/android/content/ActivityNotFoundException.html#` if there was no Activity found to run the given Intent.

<br />

`https://developer.android.com/reference/kotlin/android/content/ComponentName.html#?` startForegroundService

Similar to startService, but with an implicit promise that the Service will call startForeground once it begins running. The service is given an amount of time comparable to the ANR interval to do this, otherwise the system will automatically crash the process, in which case an internal exception `ForegroundServiceDidNotStartInTimeException` is logged on logcat on devices running SDK Version `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or later. On older Android versions, an internal exception `RemoteServiceException` is logged instead, with a corresponding message.

Unlike the ordinary startService, this method can be used at any time, regardless of whether the app hosting the service is in a foreground state.

**Note:** Beginning with SDK Version `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int`, apps targeting SDK Version `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or higher are not allowed to start foreground services from the background. See [Behavior changes: Apps targeting Android 12](../about/versions/12/behavior-changes-12.md) for more details.

<br />

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` startInstrumentation

Start executing an `https://developer.android.com/reference/kotlin/android/app/Instrumentation.html#` class. The given Instrumentation component will be run by killing its target application (if currently running), starting the target process, instantiating the instrumentation component, and then letting it drive the application.

This function is not synchronous -- it returns as soon as the instrumentation has started and while it is running.

Instrumentation is normally only allowed to run against a package that is either unsigned or signed with a signature that the the instrumentation package is also signed with (ensuring the target trusts the instrumentation).

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` startIntentSender

Same as startIntentSender with no options specified.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` startIntentSender

Like startActivity, but taking a IntentSender to start. If the IntentSender is for an activity, that activity will be started as if you had called the regular startActivity here; otherwise, its associated action will be executed (such as sending a broadcast) as if you had called android.content.IntentSender#sendIntent on it.

<br />

`https://developer.android.com/reference/kotlin/android/content/ComponentName.html#?` startService

Request that a given application service be started. The Intent should either contain the complete class name of a specific service implementation to start, or a specific package name to target. If the Intent is less specified, it logs a warning about this. In this case any of the multiple matching services may be used. If this service is not already running, it will be instantiated and started (creating a process for it if needed); if it is running then it remains running.

Every call to this method will result in a corresponding call to the target service's onStartCommand method, with the intent given here. This provides a convenient way to submit jobs to a service without having to bind and call on to its interface.

Using startService() overrides the default service lifetime that is managed by #bindService: it requires the service to remain running until stopService is called, regardless of whether any clients are connected to it. Note that calls to startService() do not nest: no matter how many times you call startService(), a single call to stopService will stop it.

The system attempts to keep running services around as much as possible. The only time they should be stopped is if the current foreground application is using so many resources that the service needs to be killed. If any errors happen in the service's process, it will automatically be restarted.

This function will throw `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#` if you do not have permission to start the given service.

**Note:** Each call to startService() results in significant work done by the system to manage service lifecycle surrounding the processing of the intent, which can take multiple milliseconds of CPU time. Due to this cost, startService() should not be used for frequent intent delivery to a service, and only for scheduling significant work. Use #bindService for high frequency calls.
Beginning with SDK Version `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#O:kotlin.Int`, apps targeting SDK Version `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#O:kotlin.Int` or higher are not allowed to start background services from the background. See [Background Execution Limits](../about/versions/oreo/background.md) for more details.

**Note:** Beginning with SDK Version `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int`, apps targeting SDK Version `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or higher are not allowed to start foreground services from the background. See [Behavior changes: Apps targeting Android 12](../about/versions/12/behavior-changes-12.md) for more details.

<br />

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` stopService

Request that a given application service be stopped. If the service is not running, nothing happens. Otherwise it is stopped. Note that calls to startService() are not counted -- this stops the service no matter how many times it was started.

If the service is running as a foreground service when it is stopped, its associated notification will be removed. To avoid this, apps can use stopForeground to decouple the notification from the service's lifecycle before stopping it.

Note that if a stopped service still has `https://developer.android.com/reference/kotlin/android/content/ServiceConnection.html#` objects bound to it with the `https://developer.android.com/reference/kotlin/android/content/Context.html#BIND_AUTO_CREATE:kotlin.Int` set, it will not be destroyed until all of these bindings are removed. See the `https://developer.android.com/reference/kotlin/android/app/Service.html#` documentation for more details on a service's lifecycle.

This function will throw `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#` if you do not have permission to stop the given service.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` unbindService

Disconnect from an application service. You will no longer receive calls as the service is restarted, and the service is now allowed to stop at any time.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` unregisterComponentCallbacks

Remove a `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks.html#` object that was previously registered with registerComponentCallbacks.

After `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#TIRAMISU:kotlin.Int`, the `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks.html#` will be unregistered to getBaseContext, and can be only used after attachBaseContext

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` unregisterDeviceIdChangeListener

Removes a device ID changed listener from the Context. It's a no-op if the listener is not already registered.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` unregisterReceiver

Unregister a previously registered BroadcastReceiver. *All* filters that have been registered for this BroadcastReceiver will be removed.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` updateServiceBindings

Perform a batch update of existing bindings. Existing bindings can be rebound with an updated set of flags, or unbound. Only flags returned from getUpdateableFlags may be added or removed.

This API behaves as if the rebindService and unbindService API are called in the same order as the params are iterated.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` updateServiceGroup

For a service previously bound with #bindService or a related method, change how the system manages that service's process in relation to other processes. This doesn't modify the original bind flags that were passed in when binding, but adjusts how the process will be managed in some cases based on those flags. Currently only works on isolated processes (will be ignored for non-isolated processes).

Note that this call does not take immediate effect, but will be applied the next time the impacted process is adjusted for some other reason. Typically you would call this before then calling a new #bindIsolatedService on the service of interest, with that binding causing the process to be shuffled accordingly.

<br />

From class `https://developer.android.com/reference/kotlin/android/content/Context.html#` `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` bindIsolatedService

See bindIsolatedService Call of to obtain a BindServiceFlags object.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` getColor

Returns a color associated with a particular resource ID and styled for the current theme.

<br />

`https://developer.android.com/reference/kotlin/android/content/res/ColorStateList.html#` getColorStateList

Returns a color state list associated with a particular resource ID and styled for the current theme.

<br />

`https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#?` getDrawable

Returns a drawable object associated with a particular resource ID and styled for the current theme.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` getString

Returns a localized string from the application's package's default string table.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` getString

Returns a localized formatted string from the application's package's default string table, substituting the format arguments as defined in `https://developer.android.com/reference/kotlin/java/util/Formatter.html#` and java.lang.String#format.

<br />

`T` getSystemService

Return the handle to a system-level service by class.

Currently available classes are: `https://developer.android.com/reference/kotlin/android/view/WindowManager.html#`, `https://developer.android.com/reference/kotlin/android/view/LayoutInflater.html#`, `https://developer.android.com/reference/kotlin/android/app/ActivityManager.html#`, `https://developer.android.com/reference/kotlin/android/os/PowerManager.html#`, `https://developer.android.com/reference/kotlin/android/app/AlarmManager.html#`, `https://developer.android.com/reference/kotlin/android/app/NotificationManager.html#`, `https://developer.android.com/reference/kotlin/android/app/KeyguardManager.html#`, `https://developer.android.com/reference/kotlin/android/location/LocationManager.html#`, `https://developer.android.com/reference/kotlin/android/app/SearchManager.html#`, `https://developer.android.com/reference/kotlin/android/os/Vibrator.html#`, `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager.html#`, `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager.html#`, `https://developer.android.com/reference/kotlin/android/media/AudioManager.html#`, `https://developer.android.com/reference/kotlin/android/media/MediaRouter.html#`, `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager.html#`, `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager.html#`, `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager.html#`, `https://developer.android.com/reference/kotlin/android/app/UiModeManager.html#`, `https://developer.android.com/reference/kotlin/android/app/DownloadManager.html#`, `https://developer.android.com/reference/kotlin/android/os/BatteryManager.html#`, `https://developer.android.com/reference/kotlin/android/app/job/JobScheduler.html#`, `https://developer.android.com/reference/kotlin/android/app/usage/NetworkStatsManager.html#`, `https://developer.android.com/reference/kotlin/android/content/pm/verify/domain/DomainVerificationManager.html#`, `https://developer.android.com/reference/kotlin/android/view/displayhash/DisplayHashManager.html#` `https://developer.android.com/reference/kotlin/android/security/authenticationpolicy/AuthenticationPolicyManager.html#`.

Note: System services obtained via this API may be closely associated with the Context in which they are obtained from. In general, do not share the service objects between various different contexts (Activities, Applications, Services, Providers, etc.)

Note: Instant apps, for which isInstantApp returns true, don't have access to the following system services: `https://developer.android.com/reference/kotlin/android/content/Context.html#DEVICE_POLICY_SERVICE:kotlin.String`, #FINGERPRINT_SERVICE, `https://developer.android.com/reference/kotlin/android/content/Context.html#KEYGUARD_SERVICE:kotlin.String`, `https://developer.android.com/reference/kotlin/android/content/Context.html#SHORTCUT_SERVICE:kotlin.String`, `https://developer.android.com/reference/kotlin/android/content/Context.html#USB_SERVICE:kotlin.String`, `https://developer.android.com/reference/kotlin/android/content/Context.html#WALLPAPER_SERVICE:kotlin.String`, `https://developer.android.com/reference/kotlin/android/content/Context.html#WIFI_P2P_SERVICE:kotlin.String`, `https://developer.android.com/reference/kotlin/android/content/Context.html#WIFI_SERVICE:kotlin.String`, `https://developer.android.com/reference/kotlin/android/content/Context.html#WIFI_AWARE_SERVICE:kotlin.String`. For these services this method will return `null`. Generally, if you are running as an instant app you should always check whether the result of this method is `null`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html` getText

Return a localized, styled CharSequence from the application's package's default string table.

<br />

`https://developer.android.com/reference/kotlin/android/content/Context.BindServiceFlags.html#` getUpdateableFlags

Gets the list of bind flags that may be updated (i.e. added or removed) for an existing connection. Includes:

- `https://developer.android.com/reference/kotlin/android/content/Context.html#BIND_NOT_FOREGROUND:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/content/Context.html#BIND_ABOVE_CLIENT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/content/Context.html#BIND_ALLOW_OOM_MANAGEMENT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/content/Context.html#BIND_WAIVE_PRIORITY:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/content/Context.html#BIND_IMPORTANT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/content/Context.html#BIND_ADJUST_WITH_ACTIVITY:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/content/Context.html#BIND_NOT_PERCEPTIBLE:kotlin.Int`

<br />

<br />

`https://developer.android.com/reference/kotlin/android/content/res/TypedArray.html#` obtainStyledAttributes

Retrieve styled attribute information in this Context's theme. See obtainStyledAttributes for more information.

<br />

`https://developer.android.com/reference/kotlin/android/content/res/TypedArray.html#` obtainStyledAttributes

Retrieve styled attribute information in this Context's theme. See obtainStyledAttributes for more information.

<br />

`https://developer.android.com/reference/kotlin/android/content/res/TypedArray.html#` obtainStyledAttributes

Retrieve styled attribute information in this Context's theme. See obtainStyledAttributes for more information.

<br />

`https://developer.android.com/reference/kotlin/android/content/res/TypedArray.html#` obtainStyledAttributes

Retrieve styled attribute information in this Context's theme. See obtainStyledAttributes for more information.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` revokeSelfPermissionOnKill

Triggers the asynchronous revocation of a runtime permission. If the permission is not currently granted, nothing happens (even if later granted by the user).

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` sendBroadcastWithMultiplePermissions

Broadcast the given intent to all interested BroadcastReceivers, allowing an array of required permissions to be enforced. This call is asynchronous; it returns immediately, and you will continue executing while the receivers are run. No results are propagated from receivers and receivers can not abort the broadcast. If you want to allow receivers to propagate results or abort the broadcast, you must send an ordered broadcast using sendOrderedBroadcast.

See `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#` for more information on Intent broadcasts.

<br />

## Constants

### FLAG_CLIENT_SIDE_ENCRYPTION_ENABLED

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_CLIENT_SIDE_ENCRYPTION_ENABLED: Int
```

Transport flag indicating that the transport has client-side encryption enabled. i.e., the user's backup has been encrypted with a key known only to the device, and not to the remote storage solution. Even if an attacker had root access to the remote storage provider they should not be able to decrypt the user's backup data.

 Value: 1

### FLAG_CROSS_PLATFORM_DATA_TRANSFER_IOS

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_CROSS_PLATFORM_DATA_TRANSFER_IOS: Int
```

Transport flag indicating that the transport is used for a cross-platform transfer to or from iOS. The user's backup data is sent directly to another device over e.g. USB or WiFi.

 Value: 8

### FLAG_DEVICE_TO_DEVICE_TRANSFER

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_DEVICE_TO_DEVICE_TRANSFER: Int
```

Transport flag indicating that the transport is used for a device-to-device transfer. There is no third party or intermediate storage. The user's backup data is sent directly to another device over e.g., USB or WiFi.

 Value: 2

### TYPE_DIRECTORY

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_DIRECTORY: Int
```

During a full restore, indicates that the file system object being restored is a directory.

 Value: 2

### TYPE_FILE

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_FILE: Int
```

During a full restore, indicates that the file system object being restored is an ordinary file.

 Value: 1

## Public constructors

### BackupAgent

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
BackupAgent()
```

## Public methods

### fullBackupFile

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun fullBackupFile(
    file: File!, 
    output: FullBackupDataOutput!
): Unit
```

Write an entire file as part of a full-backup operation. The file's contents will be delivered to the backup destination along with the metadata necessary to place it with the proper location and permissions on the device where the data is restored.

Attempting to back up files in directories that are ignored by the backup system will have no effect. For example, if the app calls this method with a file inside the getNoBackupFilesDir directory, it will be ignored. See onFullBackup for details on what directories are excluded from backups.

| Parameters ||
|---|---|
| `file` | [File](../java.io/File.md)!: The file to be backed up. The file must exist and be readable by the caller. |
| `output` | [FullBackupDataOutput](FullBackupDataOutput.md)!: The destination to which the backed-up file data will be sent. |

### onBackup

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun onBackup(
    oldState: ParcelFileDescriptor!, 
    data: BackupDataOutput!, 
    newState: ParcelFileDescriptor!
): Unit
```

The application is being asked to write any data changed since the last time it performed a backup operation. The state data recorded during the last backup pass is provided in the `oldState` file descriptor. If `oldState` is `null`, no old state is available and the application should perform a full backup. In both cases, a representation of the final backup state after this pass should be written to the file pointed to by the file descriptor wrapped in `newState`.

Each entity written to the BackupDataOutput `data` stream will be transmitted over the current backup transport and stored in the remote data set under the key supplied as part of the entity. Writing an entity with a negative data size instructs the transport to delete whatever entity currently exists under that key from the remote data set.

| Parameters ||
|---|---|
| `oldState` | [ParcelFileDescriptor](../android.os/ParcelFileDescriptor.md)!: An open, read-only ParcelFileDescriptor pointing to the last backup state provided by the application. May be `null`, in which case no prior state is being provided and the application should perform a full backup. |
| `data` | [BackupDataOutput](BackupDataOutput.md)!: A structured wrapper around an open, read/write file descriptor pointing to the backup data destination. Typically the application will use backup helper classes to write to this file. |
| `newState` | [ParcelFileDescriptor](../android.os/ParcelFileDescriptor.md)!: An open, read/write ParcelFileDescriptor pointing to an empty file. The application should record the final backup state here after writing the requested data to the `data` output stream. |
| --- | --- |

### onCreate

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onCreate(): Unit
```

Provided as a convenience for agent implementations that need an opportunity to do one-time initialization before the actual backup or restore operation is begun.

### onDestroy

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onDestroy(): Unit
```

Provided as a convenience for agent implementations that need to do some sort of shutdown process after backup or restore is completed.

Agents do not need to override this method.

### onEstimateFullBackupBytes

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onEstimateFullBackupBytes(
    quotaBytes: Long, 
    transportFlags: Int
): Long
```

Estimate how much data in bytes a full backup will deliver. This is used during the preflight check to make sure the size doesn't exceed the backup quota.

By default, the backup size is measured by calling onFullBackup and looking at the size of the backup it produces while discarding the data. This method can be overridden to provide an alternative, more efficient estimation if necessary. 
Value is a non-negative number of bytes.

| Parameters ||
|---|---|
| `quotaBytes` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): The maximum data size that the transport currently permits this application to store as a backup. |
| `transportFlags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): flags with additional information about the backup transport. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | estimated size of the full backup. If the returned size is negative, the backup agent will fallback to using onFullBackup to measure the size. Value is a non-negative number of bytes. |

### onFullBackup

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onFullBackup(data: FullBackupDataOutput!): Unit
```

The application is having its entire file system contents backed up. `data` points to the backup destination, and the app has the opportunity to choose which files are to be stored. To commit a file as part of the backup, call the fullBackupFile helper method. After all file data is written to the output, the agent returns from this method and the backup operation concludes.

Certain parts of the app's data are never backed up even if the app explicitly sends them to the output:

- The contents of the getCacheDir directory
- The contents of the getCodeCacheDir directory
- The contents of the getNoBackupFilesDir directory
- The contents of the app's shared library directory

The default implementation of this method backs up the entirety of the application's "owned" file system trees to the output other than the few exceptions listed above. Apps only need to override this method if they need to impose special limitations on which files are being stored beyond the control that getNoBackupFilesDir offers. Alternatively they can provide an xml resource to specify what data to include or exclude.

| Parameters ||
|---|---|
| `data` | [FullBackupDataOutput](FullBackupDataOutput.md)!: A structured wrapper pointing to the backup destination. |

| Exceptions ||
|---|---|
| `java.io.IOException` | |

**See Also**

- getNoBackupFilesDir
- fullBackupFile
- onRestoreFile

### onQuotaExceeded

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onQuotaExceeded(
    backupDataBytes: Long, 
    quotaBytes: Long
): Unit
```

Notification that the application's current backup operation causes it to exceed the maximum size permitted by the transport. The ongoing backup operation is halted and rolled back: any data that had been stored by a previous backup operation is still intact. Typically the quota-exceeded state will be detected before any data is actually transmitted over the network.

The `quotaBytes` value is the total data size currently permitted for this application. If desired, the application can use this as a hint for determining how much data to store. For example, a messaging application might choose to store only the newest messages, dropping enough older content to stay under the quota.

Note that the maximum quota for the application can change over time. In particular, in the future the quota may grow. Applications that adapt to the quota when deciding what data to store should be aware of this and implement their data storage mechanisms in a way that can take advantage of additional quota.

| Parameters ||
|---|---|
| `backupDataBytes` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): The amount of data measured while initializing the backup operation, if the total exceeds the app's alloted quota. If initial measurement suggested that the data would fit but then too much data was actually submitted as part of the operation, then this value is the amount of data that had been streamed into the transport at the time the quota was reached. |
| `quotaBytes` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): The maximum data size that the transport currently permits this application to store as a backup. |

### onRestore

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun onRestore(
    data: BackupDataInput!, 
    appVersionCode: Int, 
    newState: ParcelFileDescriptor!
): Unit
```

The application is being restored from backup and should replace any existing data with the contents of the backup. The backup data is provided through the `data` parameter. Once the restore is finished, the application should write a representation of the final state to the `newState` file descriptor.

The application is responsible for properly erasing its old data and replacing it with the data supplied to this method. No "clear user data" operation will be performed automatically by the operating system. The exception to this is in the case of a failed restore attempt: if onRestore() throws an exception, the OS will assume that the application's data may now be in an incoherent state, and will clear it before proceeding.

| Parameters ||
|---|---|
| `data` | [BackupDataInput](BackupDataInput.md)!: A structured wrapper around an open, read-only file descriptor pointing to a full snapshot of the application's data. The application should consume every entity represented in this data stream. |
| `appVersionCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The value of the [`android:versionCode`](https://developer.android.com/guide/topics/manifest/manifest-element.html#vcode) manifest attribute, from the application that backed up this particular data set. This makes it possible for an application's agent to distinguish among any possible older data versions when asked to perform the restore operation. |
| `newState` | [ParcelFileDescriptor](../android.os/ParcelFileDescriptor.md)!: An open, read/write ParcelFileDescriptor pointing to an empty file. The application should record the final backup state here after restoring its data from the `data` stream. When a full-backup dataset is being restored, this will be `null`. |
| --- | --- |

### onRestore

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onRestore(
    data: BackupDataInput!, 
    appVersionCode: Long, 
    newState: ParcelFileDescriptor!
): Unit
```

New version of onRestore that handles a long app version code. Default implementation casts the version code to an int and calls onRestore.

### onRestoreFile

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onRestoreFile(data: FullRestoreDataInput): Unit
```

Handle the data delivered via the given file descriptor during a full restore operation. The agent is given the path to the file's original location as well as its size and metadata.

The file descriptor can only be read for `size` bytes; attempting to read more data has undefined behavior.

The default implementation creates the destination file/directory and populates it with the data from the file descriptor, then sets the file's access mode and modification time to match the restore arguments.

| Parameters ||
|---|---|
| `data` | [FullRestoreDataInput](FullRestoreDataInput.md): A structured wrapper containing the details of the file that's being restored and additional metadata from the backup. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.io.IOException` | |

### onRestoreFile

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onRestoreFile(
    data: ParcelFileDescriptor!, 
    size: Long, 
    destination: File!, 
    type: Int, 
    mode: Long, 
    mtime: Long
): Unit
```

Handle the data delivered via the given file descriptor during a full restore operation. The agent is given the path to the file's original location as well as its size and metadata.

The file descriptor can only be read for `size` bytes; attempting to read more data has undefined behavior.

The default implementation creates the destination file/directory and populates it with the data from the file descriptor, then sets the file's access mode and modification time to match the restore arguments.

| Parameters ||
|---|---|
| `data` | [ParcelFileDescriptor](../android.os/ParcelFileDescriptor.md)!: A read-only file descriptor from which the agent can read `size` bytes of file data. |
| `size` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): The number of bytes of file content to be restored to the given destination. If the file system object being restored is a directory, `size` will be zero. |
| `destination` | [File](../java.io/File.md)!: The File on disk to be restored with the given data. |
| --- | --- |
| `type` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The kind of file system object being restored. This will be either `https://developer.android.com/reference/kotlin/android/app/backup/BackupAgent#TYPE_FILE:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/app/backup/BackupAgent#TYPE_DIRECTORY:kotlin.Int`. |
| `mode` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): The access mode to be assigned to the destination after its data is written. This is in the standard format used by `chmod()`. |
| `mtime` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): The modification time of the file when it was backed up, suitable to be assigned to the file after its data is written. |
| --- | --- |

| Exceptions ||
|---|---|
| `java.io.IOException` | |

### onRestoreFinished

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onRestoreFinished(): Unit
```

The application's restore operation has completed. This method is called after all available data has been delivered to the application for restore (via either the onRestore or onRestoreFile callbacks). This provides the app with a stable end-of-restore opportunity to perform any appropriate post-processing on the data that was just delivered.
**See Also**

- onRestore
- onRestoreFile
