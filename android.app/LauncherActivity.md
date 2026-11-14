Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# LauncherActivity

```
abstract class LauncherActivity : ListActivity
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||||
| --- | --- | --- | --- | --- | --- | --- |
| ↳ | [android.content.Context](../android/content/Context.md) ||||||
| | ↳ | [android.content.ContextWrapper](../android/content/ContextWrapper.md) |||||
| | | ↳ | [android.view.ContextThemeWrapper](../android/view/ContextThemeWrapper.md) ||||
| --- | --- | --- | --- | --- | --- | --- |
| | | | ↳ | [android.app.Activity](../android/app/Activity.md) |||
| | | | | ↳ | [android.app.ListActivity](../android/app/ListActivity.md) ||
| | | | | | ↳ | [android.app.LauncherActivity](../android/app/LauncherActivity.md) |
| --- | --- | --- | --- | --- | --- | --- |

> [!CAUTION]
> **This class was deprecated in API level 30.**
>
> Applications can implement this UI themselves using androidx.recyclerview.widget.RecyclerView and `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#queryIntentActivities(android.content.Intent,%20kotlin.Int)`

Displays a list of all activities which can be performed for a given intent. Launches when clicked.

## Summary

| Nested classes ||
|---|---|
| open | `https://developer.android.com/reference/kotlin/android/app/LauncherActivity.IconResizer` Utility class to resize icons to match default icon size. |
| open | `https://developer.android.com/reference/kotlin/android/app/LauncherActivity.ListItem` An item in the list |

Inherited constants From class `https://developer.android.com/reference/kotlin/android/content/Context.html#` `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#ACCESSIBILITY_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityManager.html#` for giving the user feedback for UI events through the registered event listeners.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#ACCOUNT_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/accounts/AccountManager.html#` for receiving intents at a time of your choosing.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#ACTIVITY_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/app/ActivityManager` for interacting with the global system state.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#ADVANCED_PROTECTION_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve an `https://developer.android.com/reference/kotlin/android/security/advancedprotection/AdvancedProtectionManager.html#`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#ALARM_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/app/AlarmManager` for receiving intents at a time of your choosing.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#APPWIDGET_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager.html#` for accessing AppWidgets.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#APP_FUNCTION_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve an `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionManager` for executing app functions.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#APP_INTERACTION_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve an `https://developer.android.com/reference/kotlin/android/app/AppInteractionManager` for managing app interactions.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#APP_OPS_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/app/AppOpsManager` for tracking application operations on the device.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#APP_SEARCH_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve an `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchManager` for indexing and querying app data managed by the system.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#AUDIO_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/media/AudioManager.html#` for handling management of volume, ringer modes and audio routing.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#AUTHENTICATION_POLICY_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve an `https://developer.android.com/reference/kotlin/android/security/authenticationpolicy/AuthenticationPolicyManager.html#`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#AUTOFILL_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve an `https://developer.android.com/reference/kotlin/android/view/autofill/AutofillManager.html#`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#BATTERY_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/os/BatteryManager.html#` for managing battery state.

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

Flag for #bindService: automatically create the service as long as the binding exists. Note that while this will create the service, its `https://developer.android.com/reference/kotlin/android/app/Service#onStartCommand(android.content.Intent,%20kotlin.Int,%20kotlin.Int)` method will still only be called due to an explicit call to `https://developer.android.com/reference/kotlin/android/content/Context.html#startService(android.content.Intent)`. Even without that, though, this still provides you with access to the service object while the service is created.

Note that prior to `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#ICE_CREAM_SANDWICH:kotlin.Int`, not supplying this flag would also impact how important the system consider's the target service's process to be. When set, the only way for it to be raised was by binding from a service in which case it will only be important when that activity is in the foreground. Now to achieve this behavior you must explicitly supply the new flag `https://developer.android.com/reference/kotlin/android/content/Context.html#BIND_ADJUST_WITH_ACTIVITY:kotlin.Int`. For compatibility, old applications that don't specify `https://developer.android.com/reference/kotlin/android/content/Context.html#BIND_AUTO_CREATE:kotlin.Int` will automatically have the flags `https://developer.android.com/reference/kotlin/android/content/Context.html#BIND_WAIVE_PRIORITY:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/content/Context.html#BIND_ADJUST_WITH_ACTIVITY:kotlin.Int` set for them in order to achieve the same result.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#BIND_DEBUG_UNBIND:kotlin.Int`

Flag for #bindService: include debugging help for mismatched calls to unbind. When this flag is set, the callstack of the following `https://developer.android.com/reference/kotlin/android/content/Context.html#unbindService(android.content.ServiceConnection)` call is retained, to be printed if a later incorrect unbind call is made. Note that doing this requires retaining information about the binding that was made for the lifetime of the app, resulting in a leak -- this should only be used for debugging.

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

Flag for #bindIsolatedService: Bind the service into a shared isolated process. Specifying this flag allows multiple isolated services to be running in a single shared isolated process. The shared isolated process instance is identified by the instanceName parameter in `https://developer.android.com/reference/kotlin/android/content/Context.html#bindIsolatedService(android.content.Intent,%20kotlin.Int,%20kotlin.String,%20java.util.concurrent.Executor,%20android.content.ServiceConnection)`. Subsequent calls to #bindIsolatedService with the same instanceName will cause the isolated service to be co-located in the same shared isolated process. Note that the shared isolated process is scoped to the calling app; once created, only the calling app can bind additional isolated services into the shared process. However, the services themselves can come from different APKs and therefore different vendors. Only services that set the `https://developer.android.com/reference/kotlin/android/R.attr.html#allowSharedIsolatedProcess:kotlin.Int` attribute to `true` are allowed to be bound into a shared isolated process.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#BIND_WAIVE_PRIORITY:kotlin.Int`

Flag for #bindService: don't impact the scheduling or memory management priority of the target service's hosting process. Allows the service's process to be managed on the background LRU list just like a regular application process in the background.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#BIOMETRIC_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricManager.html#` for handling biometric and PIN/pattern/password authentication.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#BLOB_STORE_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/app/blob/BlobStoreManager` for contributing and accessing data blobs from the blob store maintained by the system.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#BLUETOOTH_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothManager.html#` for using Bluetooth.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#BUGREPORT_SERVICE:kotlin.String`

Service to capture a bugreport.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#CAMERA_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraManager.html#` for interacting with camera devices.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#CAPTIONING_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/view/accessibility/CaptioningManager.html#` for obtaining captioning properties and listening for changes in captioning preferences.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#CARRIER_CONFIG_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager.html#` for reading carrier configuration values.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#CHOOSER_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/service/chooser/ChooserManager.html#`.

**Note:** This service is not available on Wear OS, Android TV, or Android Auto devices. On these form factors, calls to `getSystemService` for this service will return `null`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#CLIPBOARD_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/content/ClipboardManager.html#` for accessing and modifying the contents of the global clipboard.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#COMPANION_DEVICE_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager.html#` for managing companion devices

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#CONNECTIVITY_DIAGNOSTICS_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/net/ConnectivityDiagnosticsManager.html#` for performing network connectivity diagnostics as well as receiving network connectivity information from the system.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#CONNECTIVITY_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager.html#` for handling management of network connections.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#CONSUMER_IR_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/hardware/ConsumerIrManager.html#` for transmitting infrared signals from the device.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#CONTACT_KEYS_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/provider/E2eeContactKeysManager.html#` to managing contact keys.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#CONTENT_RESTRICTION_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/app/contentsafety/ContentSafetyManager`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#CONTEXT_IGNORE_SECURITY:kotlin.Int`

Flag for use with `https://developer.android.com/reference/kotlin/android/content/Context.html#createPackageContext(kotlin.String,%20kotlin.Int)`: ignore any security restrictions on the Context being requested, allowing it to always be loaded. For use with `https://developer.android.com/reference/kotlin/android/content/Context.html#CONTEXT_INCLUDE_CODE:kotlin.Int` to allow code to be loaded into a process even when it isn't safe to do so. Use with extreme care!

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#CONTEXT_INCLUDE_CODE:kotlin.Int`

Flag for use with `https://developer.android.com/reference/kotlin/android/content/Context.html#createPackageContext(kotlin.String,%20kotlin.Int)`: include the application code with the context. This means loading code into the caller's process, so that `https://developer.android.com/reference/kotlin/android/content/Context.html#getClassLoader()` can be used to instantiate the application's classes. Setting this flags imposes security restrictions on what application context you can access; if the requested application can not be safely loaded into your process, java.lang.SecurityException will be thrown. If this flag is not set, there will be no restrictions on the packages that can be loaded, but `https://developer.android.com/reference/kotlin/android/content/Context.html#getClassLoader()` will always return the default system class loader.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#CONTEXT_RESTRICTED:kotlin.Int`

Flag for use with `https://developer.android.com/reference/kotlin/android/content/Context.html#createPackageContext(kotlin.String,%20kotlin.Int)`: a restricted context may disable specific features. For instance, a View associated with a restricted context would ignore particular XML attributes.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#CREDENTIAL_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/credentials/CredentialManager.html#` to authenticate a user to your app.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#CROSS_PROFILE_APPS_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/content/pm/CrossProfileApps.html#` for cross profile operations.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#DEVICE_ID_DEFAULT:kotlin.Int`

The default device ID, which is the ID of the primary (non-virtual) device.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#DEVICE_ID_INVALID:kotlin.Int`

Invalid device ID.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#DEVICE_LOCK_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/devicelock/DeviceLockManager.html#`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#DEVICE_POLICY_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager` for working with global device policy management.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#DISPLAY_HASH_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to access `https://developer.android.com/reference/kotlin/android/view/displayhash/DisplayHashManager.html#` to handle display hashes.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#DISPLAY_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager.html#` for interacting with display devices.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#DOMAIN_VERIFICATION_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to access `https://developer.android.com/reference/kotlin/android/content/pm/verify/domain/DomainVerificationManager.html#` to retrieve approval and user state for declared web domains.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#DOWNLOAD_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/app/DownloadManager` for requesting HTTP downloads.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#DROPBOX_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/os/DropBoxManager.html#` instance for recording diagnostic logs.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#EUICC_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager.html#` to manage the device eUICC (embedded SIM).

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#FILE_INTEGRITY_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve an `https://developer.android.com/reference/kotlin/android/security/FileIntegrityManager.html#`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#FILE_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/os/storage/FileManager.html#` for handling file operations.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#GAME_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/app/GameManager`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#GRAMMATICAL_INFLECTION_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/app/GrammaticalInflectionManager`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#HARDWARE_PROPERTIES_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/os/HardwarePropertiesManager.html#` for accessing the hardware properties service.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#HEALTHCONNECT_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#HID_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/hardware/hid/HidManager.html#` for interacting with HID devices.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#INPUT_METHOD_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager.html#` for accessing input methods.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#INPUT_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/hardware/input/InputManager.html#` for interacting with input devices.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#IPSEC_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/net/IpSecManager.html#` for encrypting Sockets or Networks with IPSec.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#JOB_SCHEDULER_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/app/job/JobScheduler` instance for managing occasional background tasks.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#KEYCHAIN_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/security/KeyChainManager.html#` for managing KeyChain certificates and grants.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#KEYGUARD_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/app/KeyguardManager` for controlling keyguard.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#KEYSTORE_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/security/keystore/KeyStoreManager.html#` for accessing [Android Keystore](../privacy-and-security/keystore.md) functions.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#LAUNCHER_APPS_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/content/pm/LauncherApps.html#` for querying and monitoring launchable apps across profiles of a user.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#LAYOUT_INFLATER_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/view/LayoutInflater.html#` for inflating layout resources in this context.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#LOCALE_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/app/LocaleManager`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#LOCATION_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/location/LocationManager.html#` for controlling location updates.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#MEDIA_COMMUNICATION_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/media/MediaCommunicationManager.html#` for managing `https://developer.android.com/reference/kotlin/android/media/MediaSession2.html#`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#MEDIA_METRICS_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/media/metrics/MediaMetricsManager.html#` for interacting with media metrics on the device.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#MEDIA_PROJECTION_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/media/projection/MediaProjectionManager.html#` instance for managing media projection sessions.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#MEDIA_QUALITY_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/media/quality/MediaQualityManager.html#` for standardize picture and audio API parameters.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#MEDIA_ROUTER_SERVICE:kotlin.String`

Use with #getSystemService to retrieve a `https://developer.android.com/reference/kotlin/android/media/MediaRouter.html#` for controlling and managing routing of media.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#MEDIA_SESSION_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/media/session/MediaSessionManager.html#` for managing media Sessions.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#MEMORY_BUDGET_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/app/MemoryBudgetManager` for monitoring memory budgets.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#MIDI_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/media/midi/MidiManager.html#` for accessing the MIDI service.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#MODE_APPEND:kotlin.Int`

File creation mode: for use with `https://developer.android.com/reference/kotlin/android/content/Context.html#openFileOutput(kotlin.String,%20kotlin.Int)`, if the file already exists then write data to the end of the existing file instead of erasing it.

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

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve the service that plays multisensory feedback.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#NETWORK_STATS_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/app/usage/NetworkStatsManager` for querying network usage stats.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#NFC_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/nfc/NfcManager.html#` for using NFC.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#NOTIFICATION_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/app/NotificationManager` for informing the user of background events.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#NPU_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/app/LauncherActivity#`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#NSD_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/net/nsd/NsdManager.html#` for handling management of network service discovery

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#OVERLAY_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/content/om/OverlayManager.html#` for managing overlay packages.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#PCC_SANDBOX_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/app/privatecompute/PccSandboxManager`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#PEOPLE_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to access a `https://developer.android.com/reference/kotlin/android/app/people/PeopleManager` to interact with your published conversations.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#PERFORMANCE_HINT_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/os/PerformanceHintManager.html#` for accessing the performance hinting service.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#PERSISTENT_DATA_BLOCK_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/service/persistentdata/PersistentDataBlockManager.html#` instance for interacting with a storage device that lives across factory resets.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#POWER_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/os/PowerManager.html#` for controlling power management, including "wake locks," which let you keep the device on while you're running long tasks.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#PRINT_SERVICE:kotlin.String`

`https://developer.android.com/reference/kotlin/android/print/PrintManager.html#` for printing and managing printers and print tasks.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#PROFILING_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve an `https://developer.android.com/reference/kotlin/android/os/ProfilingManager.html#`.

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

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/content/RestrictionsManager.html#` for retrieving application restrictions and requesting permissions for restricted operations.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#ROLE_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/app/role/RoleManager` for managing roles.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#SATELLITE_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/telephony/satellite/SatelliteManager.html#` for accessing satellite functionality.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#SEARCH_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/app/SearchManager` for handling searches.

`https://developer.android.com/reference/kotlin/android/content/res/Configuration.html#UI_MODE_TYPE_WATCH:kotlin.Int` does not support `https://developer.android.com/reference/kotlin/android/app/SearchManager`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#SECURITY_STATE_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/os/SecurityStateManager.html#` for accessing the security state manager service.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#SENSOR_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/hardware/SensorManager.html#` for accessing sensors.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#SERIAL_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/hardware/serial/SerialManager.html#` for access to serial ports.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#SHORTCUT_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/content/pm/ShortcutManager.html#` for accessing the launcher shortcut service.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#STATUS_BAR_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/app/StatusBarManager` for interacting with the status bar and quick settings.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#STORAGE_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/os/storage/StorageManager.html#` for accessing system storage functions.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#STORAGE_STATS_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/app/usage/StorageStatsManager` for accessing system storage statistics.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#SYSTEM_HEALTH_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/os/health/SystemHealthManager.html#` for accessing system health (battery, power, memory, etc) metrics.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#TELECOM_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager.html#` to manage telecom-related features of the device.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#TELEPHONY_IMS_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve an `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsManager.html#`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#TELEPHONY_PHONE_NUMBER_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/telephony/PhoneNumberManager.html#` for parsing phone numbers.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#TELEPHONY_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager.html#` for handling management the telephony features of the device.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#TELEPHONY_SUBSCRIPTION_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager.html#` for handling management the telephony subscriptions of the device.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#TETHERING_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/net/TetheringManager.html#` for managing tethering functions.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#TEXT_CLASSIFICATION_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassificationManager.html#` for text classification services.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#TEXT_SERVICES_MANAGER_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/view/textservice/TextServicesManager.html#` for accessing text services.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#TIME_MANAGER_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/app/time/TimeManager`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#TV_AD_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/media/tv/ad/TvAdManager.html#` for interacting with TV client-side advertisement services on the device.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#TV_INPUT_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/media/tv/TvInputManager.html#` for interacting with TV inputs on the device.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#TV_INTERACTIVE_APP_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/media/tv/interactive/TvInteractiveAppManager.html#` for interacting with TV interactive applications on the device.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#UI_MODE_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/app/UiModeManager` for controlling UI modes.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#USAGE_STATS_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/app/usage/UsageStatsManager` for querying device usage stats.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#USB_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/hardware/usb/UsbManager.html#` for access to USB devices (as a USB host) and for controlling this device's behavior as a USB device.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#USER_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/os/UserManager.html#` for managing users on devices that support multiple users.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#VIBRATOR_MANAGER_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/os/VibratorManager.html#` for accessing the device vibrators, interacting with individual ones and playing synchronized effects on multiple vibrators.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#VIBRATOR_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/os/Vibrator.html#` for interacting with the vibration hardware.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#VIRTUAL_DEVICE_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/companion/virtual/VirtualDeviceManager.html#` for managing virtual devices. On devices without `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_COMPANION_DEVICE_SETUP:kotlin.String` system feature the `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` will return `null`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#VPN_MANAGEMENT_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/net/VpnManager.html#` to manage profiles for the platform built-in VPN.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#WALLPAPER_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a com.android.server.WallpaperService for accessing wallpapers.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#WEB_APP_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/content/pm/webapp/WebAppManager.html#`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#WIFI_AWARE_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/net/wifi/aware/WifiAwareManager.html#` for handling management of Wi-Fi Aware.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#WIFI_P2P_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.html#` for handling management of Wi-Fi peer-to-peer connections.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#WIFI_RTT_RANGING_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/WifiRttManager.html#` for ranging devices with wifi.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#WIFI_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager.html#` for handling management of Wi-Fi access.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#WINDOW_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/view/WindowManager.html#` for accessing the system's window manager.

<br />

From class `https://developer.android.com/reference/kotlin/android/app/Activity` `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#DEFAULT_KEYS_DIALER:kotlin.Int`

Use with `https://developer.android.com/reference/kotlin/android/app/Activity#setDefaultKeyMode(kotlin.Int)` to launch the dialer during default key handling.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#DEFAULT_KEYS_DISABLE:kotlin.Int`

Use with `https://developer.android.com/reference/kotlin/android/app/Activity#setDefaultKeyMode(kotlin.Int)` to turn off default handling of keys.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#DEFAULT_KEYS_SEARCH_GLOBAL:kotlin.Int`

Use with `https://developer.android.com/reference/kotlin/android/app/Activity#setDefaultKeyMode(kotlin.Int)` to specify that unhandled keystrokes will start a global search (typically web search, but some platforms may define alternate methods for global search)

See `https://developer.android.com/reference/kotlin/android/app/SearchManager` for more details.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#DEFAULT_KEYS_SEARCH_LOCAL:kotlin.Int`

Use with `https://developer.android.com/reference/kotlin/android/app/Activity#setDefaultKeyMode(kotlin.Int)` to specify that unhandled keystrokes will start an application-defined search. (If the application or activity does not actually define a search, the keys will be ignored.)

See `https://developer.android.com/reference/kotlin/android/app/SearchManager` for more details.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#DEFAULT_KEYS_SHORTCUT:kotlin.Int`

Use with `https://developer.android.com/reference/kotlin/android/app/Activity#setDefaultKeyMode(kotlin.Int)` to execute a menu shortcut in default key handling.

That is, the user does not need to hold down the menu key to execute menu shortcuts.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#FULLSCREEN_MODE_REQUEST_ENTER:kotlin.Int`

Request type of `https://developer.android.com/reference/kotlin/android/app/Activity#requestFullscreenMode(kotlin.Int,%20android.os.OutcomeReceiver)`, to request enter fullscreen mode from multi-window mode.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#FULLSCREEN_MODE_REQUEST_EXIT:kotlin.Int`

Request type of `https://developer.android.com/reference/kotlin/android/app/Activity#requestFullscreenMode(kotlin.Int,%20android.os.OutcomeReceiver)`, to request exiting the requested fullscreen mode and restore to the previous multi-window mode.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#OVERRIDE_TRANSITION_CLOSE:kotlin.Int`

Request type of `https://developer.android.com/reference/kotlin/android/app/Activity#overrideActivityTransition(kotlin.Int,%20kotlin.Int,%20kotlin.Int)` or `https://developer.android.com/reference/kotlin/android/app/Activity#overrideActivityTransition(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)`, to override the closing transition.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#OVERRIDE_TRANSITION_OPEN:kotlin.Int`

Request type of `https://developer.android.com/reference/kotlin/android/app/Activity#overrideActivityTransition(kotlin.Int,%20kotlin.Int,%20kotlin.Int)` or `https://developer.android.com/reference/kotlin/android/app/Activity#overrideActivityTransition(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)`, to override the opening transition.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#RESULT_CANCELED:kotlin.Int`

Standard activity result: operation canceled.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#RESULT_FIRST_USER:kotlin.Int`

Start of user-defined activity results.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#RESULT_OK:kotlin.Int`

Standard activity result: operation succeeded.

<br />

From class `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#` `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#TRIM_MEMORY_BACKGROUND:kotlin.Int`

Level for `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#onTrimMemory(kotlin.Int)`: the process has gone on to the LRU list. This is a good opportunity to clean up resources that can efficiently and quickly be re-built if the user returns to the app.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#TRIM_MEMORY_COMPLETE:kotlin.Int`

Level for `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#onTrimMemory(kotlin.Int)`: the process is nearing the end of the background LRU list, and if more memory isn't found soon it will be killed.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#TRIM_MEMORY_MODERATE:kotlin.Int`

Level for `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#onTrimMemory(kotlin.Int)`: the process is around the middle of the background LRU list; freeing memory can help the system keep other processes running later in the list for better overall performance.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#TRIM_MEMORY_RUNNING_CRITICAL:kotlin.Int`

Level for `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#onTrimMemory(kotlin.Int)`: the process is not an expendable background process, but the device is running extremely low on memory and is about to not be able to keep any background processes running. Your running process should free up as many non-critical resources as it can to allow that memory to be used elsewhere. The next thing that will happen after this is `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks.html#onLowMemory()` called to report that nothing at all can be kept in the background, a situation that can start to notably impact the user.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#TRIM_MEMORY_RUNNING_LOW:kotlin.Int`

Level for `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#onTrimMemory(kotlin.Int)`: the process is not an expendable background process, but the device is running low on memory. Your running process should free up unneeded resources to allow that memory to be used elsewhere.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#TRIM_MEMORY_RUNNING_MODERATE:kotlin.Int`

Level for `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#onTrimMemory(kotlin.Int)`: the process is not an expendable background process, but the device is running moderately low on memory. Your running process may want to release some unneeded resources for use elsewhere.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#TRIM_MEMORY_UI_HIDDEN:kotlin.Int`

Level for `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#onTrimMemory(kotlin.Int)`: the process had been showing a user interface, and is no longer doing so. Large allocations with the UI should be released at this point to allow memory to be better managed.

<br />

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/app/LauncherActivity#LauncherActivity()()` <br /> |

| Public methods ||
|---|---|
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [LauncherActivity.ListItem](../android/app/LauncherActivity.ListItem.md)!\>! | `https://developer.android.com/reference/kotlin/android/app/LauncherActivity#makeListItems()()` Perform the query to determine which results to show and return a list of them. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/LauncherActivity#setTitle(kotlin.Int)(titleId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Change the title associated with this activity. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/LauncherActivity#setTitle(kotlin.CharSequence)(title: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!)` Change the title associated with this activity. |
| --- | --- |

| Protected methods ||
|---|---|
| open [Intent](../android/content/Intent.md)! | `https://developer.android.com/reference/kotlin/android/app/LauncherActivity#getTargetIntent()()` Get the base intent to use when running `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#queryIntentActivities(android.content.Intent,%20kotlin.Int)`. |
| open [Intent](../android/content/Intent.md)! | `https://developer.android.com/reference/kotlin/android/app/LauncherActivity#intentForPosition(kotlin.Int)(position: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Return the actual Intent for a specific position in our `https://developer.android.com/reference/kotlin/android/widget/ListView.html#`. |
| open [LauncherActivity.ListItem](../android/app/LauncherActivity.ListItem.md)! | `https://developer.android.com/reference/kotlin/android/app/LauncherActivity#itemForPosition(kotlin.Int)(position: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Return the `https://developer.android.com/reference/kotlin/android/app/LauncherActivity.ListItem` for a specific position in our `https://developer.android.com/reference/kotlin/android/widget/ListView.html#`. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/LauncherActivity#onCreate(android.os.Bundle)(icicle: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?)` Called when the activity is starting. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/LauncherActivity#onListItemClick(android.widget.ListView,%20android.view.View,%20kotlin.Int,%20kotlin.Long)(l: https://developer.android.com/reference/kotlin/android/widget/ListView.html#!, v: https://developer.android.com/reference/kotlin/android/view/View.html#!, position: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, id: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` This method will be called when an item in the list is selected. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [ResolveInfo](../android/content/pm/ResolveInfo.md)!\>! | `https://developer.android.com/reference/kotlin/android/app/LauncherActivity#onQueryPackageManager(android.content.Intent)(queryIntent: https://developer.android.com/reference/kotlin/android/content/Intent.html#!)` Perform query on package manager for list items. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/LauncherActivity#onSetContentView()()` Override to call setContentView() with your own content view to customize the list layout. |

Inherited functions From class `https://developer.android.com/reference/kotlin/android/app/Activity` `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#addContentView(android.view.View,%20android.view.ViewGroup.LayoutParams)(view: https://developer.android.com/reference/kotlin/android/view/View.html#!, params: https://developer.android.com/reference/kotlin/android/view/ViewGroup.LayoutParams.html#!)`

Add an additional content view to the activity. Added after any existing ones in the activity -- existing views are NOT removed.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#attachBaseContext(android.content.Context)(newBase: https://developer.android.com/reference/kotlin/android/content/Context.html#!)`

Set the base context for this ContextWrapper. All calls will then be delegated to the base context. Throws IllegalStateException if a base context has already been set.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#clearOverrideActivityTransition(kotlin.Int)(overrideType: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Clears the animations which are set from #overrideActivityTransition.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#closeContextMenu()()`

Programmatically closes the most recently opened context menu, if showing.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#closeOptionsMenu()()`

Progammatically closes the options menu. If the options menu is already closed, this method does nothing.

<br />

`https://developer.android.com/reference/kotlin/android/app/PendingIntent!` `https://developer.android.com/reference/kotlin/android/app/Activity#createPendingResult(kotlin.Int,%20android.content.Intent,%20kotlin.Int)(requestCode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, data: https://developer.android.com/reference/kotlin/android/content/Intent.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Create a new PendingIntent object which you can hand to others for them to use to send result data back to your #onActivityResult callback. The created object will be either one-shot (becoming invalid after a result is sent back) or multiple (allowing any number of results to be sent through it).

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#dismissDialog(kotlin.Int)(id: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Dismiss a dialog that was previously shown via `https://developer.android.com/reference/kotlin/android/app/Activity#showDialog(kotlin.Int)`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#dismissKeyboardShortcutsHelper()()`

Dismiss the Keyboard Shortcuts screen.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#dispatchGenericMotionEvent(android.view.MotionEvent)(ev: https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#!)`

Called to process generic motion events. You can override this to intercept all generic motion events before they are dispatched to the window. Be sure to call this implementation for generic motion events that should be handled normally.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#dispatchKeyEvent(android.view.KeyEvent)(event: https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#!)`

Called to process key events. You can override this to intercept all key events before they are dispatched to the window. Be sure to call this implementation for key events that should be handled normally.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#dispatchKeyShortcutEvent(android.view.KeyEvent)(event: https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#!)`

Called to process a key shortcut event. You can override this to intercept all key shortcut events before they are dispatched to the window. Be sure to call this implementation for key shortcut events that should be handled normally.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#dispatchPopulateAccessibilityEvent(android.view.accessibility.AccessibilityEvent)(event: https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent.html#!)`

Called to process population of `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent.html#`s.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#dispatchTouchEvent(android.view.MotionEvent)(ev: https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#!)`

Called to process touch screen events. You can override this to intercept all touch screen events before they are dispatched to the window. Be sure to call this implementation for touch screen events that should be handled normally.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#dispatchTrackballEvent(android.view.MotionEvent)(ev: https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#!)`

Called to process trackball events. You can override this to intercept all trackball events before they are dispatched to the window. Be sure to call this implementation for trackball events that should be handled normally.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#dump(kotlin.String,%20java.io.FileDescriptor,%20java.io.PrintWriter,%20kotlin.Array)(prefix: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, fd: https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#?, writer: https://developer.android.com/reference/kotlin/java/io/PrintWriter.html#, args: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>?)`

Print the Activity's state into the given stream. This gets invoked if you run `adb shell dumpsys activity <activity_component_name>`.

This method won't be called if the app targets `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#TIRAMISU:kotlin.Int` or later if the dump request starts with one of the following arguments:

- --autofill
- --contentcapture
- --translation
- --list-dumpables
- --dump-dumpable

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#enterPictureInPictureMode()()`

Puts the activity in picture-in-picture mode if possible in the current system state. Any prior calls to `https://developer.android.com/reference/kotlin/android/app/Activity#setPictureInPictureParams(android.app.PictureInPictureParams)` will still apply when entering picture-in-picture through this call.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#enterPictureInPictureMode(android.app.PictureInPictureParams)(params: https://developer.android.com/reference/kotlin/android/app/PictureInPictureParams)`

Puts the activity in picture-in-picture mode if possible in the current system state. The set parameters in `params` will be combined with the parameters from prior calls to `https://developer.android.com/reference/kotlin/android/app/Activity#setPictureInPictureParams(android.app.PictureInPictureParams)`. The system may disallow entering picture-in-picture in various cases, including when the activity is not visible, if the screen is locked or if the user has an activity pinned.

By default, system calculates the dimension of picture-in-picture window based on the given `params`. See [Picture-in-picture Support](https://developer.android.com/guide/topics/ui/picture-in-picture) on how to override this behavior.

<br />

`T` `https://developer.android.com/reference/kotlin/android/app/Activity#findViewById(kotlin.Int)(id: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Finds a view that was identified by the `android:id` XML attribute that was processed in #onCreate.

**Note:** In most cases -- depending on compiler support -- the resulting view is automatically cast to the target class type. If the target class type is unconstrained, an explicit cast may be necessary.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#finish()()`

Call this when your activity is done and should be closed. The ActivityResult is propagated back to whoever launched you via onActivityResult().

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#finishActivity(kotlin.Int)(requestCode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Force finish another activity that you had previously started with #startActivityForResult.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#finishActivityFromChild(android.app.Activity,%20kotlin.Int)(child: https://developer.android.com/reference/kotlin/android/app/Activity, requestCode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

This is called when a child activity of this one calls its finishActivity().

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#finishAffinity()()`

Finish this activity as well as all activities immediately below it in the current task that have the same affinity. This is typically used when an application can be launched on to another task (such as from an ACTION_VIEW of a content type it understands) and the user has used the up navigation to switch out of the current task and in to its own task. In this case, if the user has navigated down into any other activities of the second application, all of those should be removed from the original task as part of the task switch.

Note that this finish does *not* allow you to deliver results to the previous activity, and an exception will be thrown if you are trying to do so.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#finishAfterTransition()()`

Reverses the Activity Scene entry Transition and triggers the calling Activity to reverse its exit Transition. When the exit Transition completes, `https://developer.android.com/reference/kotlin/android/app/Activity#finish()` is called. If no entry Transition was used, finish() is called immediately and the Activity exit Transition is run.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#finishAndRemoveTask()()`

Call this when your activity is done and should be closed and the task should be completely removed as a part of finishing the root activity of the task.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#finishFromChild(android.app.Activity)(child: https://developer.android.com/reference/kotlin/android/app/Activity!)`

This is called when a child activity of this one calls its `https://developer.android.com/reference/kotlin/android/app/Activity#finish()` method. The default implementation simply calls finish() on this activity (the parent), finishing the entire group.

<br />

`https://developer.android.com/reference/kotlin/android/app/ActionBar?` `https://developer.android.com/reference/kotlin/android/app/Activity#getActionBar()()`

Retrieve a reference to this activity's ActionBar.

<br />

`https://developer.android.com/reference/kotlin/android/app/Application!` `https://developer.android.com/reference/kotlin/android/app/Activity#getApplication()()`

Return the application that owns this activity.

<br />

`https://developer.android.com/reference/kotlin/android/app/ComponentCaller?` `https://developer.android.com/reference/kotlin/android/app/Activity#getCaller()()`

Returns the ComponentCaller instance of the app that started this activity.

To keep the ComponentCaller instance for future use, call `https://developer.android.com/reference/kotlin/android/app/Activity#setIntent(android.content.Intent,%20android.app.ComponentCaller)`, and use this method to retrieve it.

Note that in #onNewIntent, this method will return the original ComponentCaller. You can use `https://developer.android.com/reference/kotlin/android/app/Activity#setIntent(android.content.Intent,%20android.app.ComponentCaller)` to update it to the new ComponentCaller.

<br />

`https://developer.android.com/reference/kotlin/android/content/ComponentName.html#?` `https://developer.android.com/reference/kotlin/android/app/Activity#getCallingActivity()()`

Return the name of the activity that invoked this activity. This is who the data in #setResult will be sent to. You can use this information to validate that the recipient is allowed to receive the data.

Note: if the calling activity is not expecting a result (that is it did not use the #startActivityForResult form that includes a request code), then the calling package will be null.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?` `https://developer.android.com/reference/kotlin/android/app/Activity#getCallingPackage()()`

Return the name of the package that invoked this activity. This is who the data in #setResult will be sent to. You can use this information to validate that the recipient is allowed to receive the data.

Note: if the calling activity is not expecting a result (that is it did not use the #startActivityForResult form that includes a request code), then the calling package will be null.

Note: prior to `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#JELLY_BEAN_MR2:kotlin.Int`, the result from this method was unstable. If the process hosting the calling package was no longer running, it would return null instead of the proper package name. You can use `https://developer.android.com/reference/kotlin/android/app/Activity#getCallingActivity()` and retrieve the package name from that instead.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#getChangingConfigurations()()`

If this activity is being destroyed because it can not handle a configuration parameter being changed (and thus its `https://developer.android.com/reference/kotlin/android/app/Activity#onConfigurationChanged(android.content.res.Configuration)` method is *not* being called), then you can use this method to discover the set of changes that have occurred while in the process of being destroyed. Note that there is no guarantee that these will be accurate (other changes could have happened at any time), so you should only use this as an optimization hint.

<br />

`https://developer.android.com/reference/kotlin/android/content/ComponentName.html#!` `https://developer.android.com/reference/kotlin/android/app/Activity#getComponentName()()`

Returns the complete component name of this activity.

<br />

`https://developer.android.com/reference/kotlin/android/transition/Scene.html#!` `https://developer.android.com/reference/kotlin/android/app/Activity#getContentScene()()`

Retrieve the `https://developer.android.com/reference/kotlin/android/transition/Scene.html#` representing this window's current content. Requires `https://developer.android.com/reference/kotlin/android/view/Window.html#FEATURE_CONTENT_TRANSITIONS:kotlin.Int`.

This method will return null if the current content is not represented by a Scene.

<br />

`https://developer.android.com/reference/kotlin/android/transition/TransitionManager.html#!` `https://developer.android.com/reference/kotlin/android/app/Activity#getContentTransitionManager()()`

Retrieve the `https://developer.android.com/reference/kotlin/android/transition/TransitionManager.html#` responsible for default transitions in this window. Requires `https://developer.android.com/reference/kotlin/android/view/Window.html#FEATURE_CONTENT_TRANSITIONS:kotlin.Int`.

This method will return non-null after content has been initialized (e.g. by using #setContentView) if `https://developer.android.com/reference/kotlin/android/view/Window.html#FEATURE_CONTENT_TRANSITIONS:kotlin.Int` has been granted.

<br />

`https://developer.android.com/reference/kotlin/android/app/ComponentCaller` `https://developer.android.com/reference/kotlin/android/app/Activity#getCurrentCaller()()`

Returns the ComponentCaller instance of the app that re-launched this activity with a new intent via #onNewIntent or #onActivityResult.

Note that this method only works within the #onNewIntent and #onActivityResult methods. If you call this method outside #onNewIntent and #onActivityResult, it will throw an `https://developer.android.com/reference/kotlin/java/lang/IllegalStateException.html#`.

You can also retrieve the caller if you override `https://developer.android.com/reference/kotlin/android/app/Activity#onNewIntent(android.content.Intent,%20android.app.ComponentCaller)` or `https://developer.android.com/reference/kotlin/android/app/Activity#onActivityResult(kotlin.Int,%20kotlin.Int,%20android.content.Intent,%20android.app.ComponentCaller)`.

To keep the ComponentCaller instance for future use, call `https://developer.android.com/reference/kotlin/android/app/Activity#setIntent(android.content.Intent,%20android.app.ComponentCaller)`, and use `https://developer.android.com/reference/kotlin/android/app/Activity#getCaller()` to retrieve it.

<br />

`https://developer.android.com/reference/kotlin/android/view/View.html#?` `https://developer.android.com/reference/kotlin/android/app/Activity#getCurrentFocus()()`

Calls `https://developer.android.com/reference/kotlin/android/view/Window.html#getCurrentFocus()` on the Window of this Activity to return the currently focused view.

<br />

`https://developer.android.com/reference/kotlin/android/app/FragmentManager!` `https://developer.android.com/reference/kotlin/android/app/Activity#getFragmentManager()()`

Return the FragmentManager for interacting with fragments associated with this activity.

<br />

`https://developer.android.com/reference/kotlin/android/app/ComponentCaller` `https://developer.android.com/reference/kotlin/android/app/Activity#getInitialCaller()()`

Returns the ComponentCaller instance of the app that initially launched this activity.

Note that calls to #onNewIntent and #setIntent have no effect on the returned value of this method.

<br />

`https://developer.android.com/reference/kotlin/android/content/Intent.html#!` `https://developer.android.com/reference/kotlin/android/app/Activity#getIntent()()`

Returns the intent that started this activity.

To keep the Intent instance for future use, call `https://developer.android.com/reference/kotlin/android/app/Activity#setIntent(android.content.Intent)`, and use this method to retrieve it.

Note that in #onNewIntent, this method will return the original Intent. You can use `https://developer.android.com/reference/kotlin/android/app/Activity#setIntent(android.content.Intent)` to update it to the new Intent.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?` `https://developer.android.com/reference/kotlin/android/app/Activity#getLastNonConfigurationInstance()()`

Retrieve the non-configuration instance data that was previously returned by `https://developer.android.com/reference/kotlin/android/app/Activity#onRetainNonConfigurationInstance()`. This will be available from the initial #onCreate and `https://developer.android.com/reference/kotlin/android/app/Activity#onStart()` calls to the new instance, allowing you to extract any useful dynamic state from the previous instance.

Note that the data you retrieve here should *only* be used as an optimization for handling configuration changes. You should always be able to handle getting a null pointer back, and an activity must still be able to restore itself to its previous state (through the normal `https://developer.android.com/reference/kotlin/android/app/Activity#onSaveInstanceState(android.os.Bundle)` mechanism) even if this function returns null.

**Note:** For most cases you should use the `https://developer.android.com/reference/kotlin/android/app/Fragment` API `https://developer.android.com/reference/kotlin/android/app/Fragment#setRetainInstance(kotlin.Boolean)` instead; this is also available on older platforms through the Android support libraries.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?` `https://developer.android.com/reference/kotlin/android/app/Activity#getLaunchedFromPackage()()`

Returns the package name of the app that initially launched this activity.

In order to receive the launching app's package name, at least one of the following has to be met:

- The app must call `https://developer.android.com/reference/kotlin/android/app/ActivityOptions#setShareIdentityEnabled(kotlin.Boolean)` with a value of `true` and launch this activity with the resulting `ActivityOptions`.
- The launched activity has the same uid as the launching app.
- The launched activity is running in a package that is signed with the same key used to sign the platform (typically only system packages such as Settings will meet this requirement).
- Starting in `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#CINNAMON_BUN:kotlin.Int`, the activity was launched directly with `https://developer.android.com/reference/kotlin/android/app/Activity#startActivityForResult(android.content.Intent,%20kotlin.Int)`.

. These are the same requirements for `https://developer.android.com/reference/kotlin/android/app/Activity#getLaunchedFromUid()`; if any of these are met, then these methods can be used to obtain the uid and package name of the launching app. If none are met, then `null` is returned.

Note, if an activity is launched via `https://developer.android.com/reference/kotlin/android/app/Activity#startActivityForResult(android.content.Intent,%20kotlin.Int)` but the launch is intercepted and forwarded by an intermediate app using `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_ACTIVITY_FORWARD_RESULT:kotlin.Int`, the identity of the intermediate app will not be implicitly shared. In this forwarding scenario, the intermediate app must explicitly opt-in using `https://developer.android.com/reference/kotlin/android/app/ActivityOptions#setShareIdentityEnabled(kotlin.Boolean)`.

Prior to `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#CINNAMON_BUN:kotlin.Int`, the launching app's identity was not implicitly shared for any result-based launches and could only be retrieved via `https://developer.android.com/reference/kotlin/android/app/Activity#getCallingPackage()`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#getLaunchedFromUid()()`

Returns the uid of the app that initially launched this activity.

In order to receive the launching app's uid, at least one of the following has to be met:

- The app must call `https://developer.android.com/reference/kotlin/android/app/ActivityOptions#setShareIdentityEnabled(kotlin.Boolean)` with a value of `true` and launch this activity with the resulting `ActivityOptions`.
- The launched activity has the same uid as the launching app.
- The launched activity is running in a package that is signed with the same key used to sign the platform (typically only system packages such as Settings will meet this requirement).
- Starting in `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#CINNAMON_BUN:kotlin.Int`, the activity was launched directly with `https://developer.android.com/reference/kotlin/android/app/Activity#startActivityForResult(android.content.Intent,%20kotlin.Int)`.

. These are the same requirements for `https://developer.android.com/reference/kotlin/android/app/Activity#getLaunchedFromPackage()`; if any of these are met, then these methods can be used to obtain the uid and package name of the launching app. If none are met, then `https://developer.android.com/reference/kotlin/android/os/Process.html#INVALID_UID:kotlin.Int` is returned.

Note, if an activity is launched via `https://developer.android.com/reference/kotlin/android/app/Activity#startActivityForResult(android.content.Intent,%20kotlin.Int)` but the launch is intercepted and forwarded by an intermediate app using `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_ACTIVITY_FORWARD_RESULT:kotlin.Int`, the identity of the intermediate app will not be implicitly shared. In this forwarding scenario, the intermediate app must explicitly opt-in using `https://developer.android.com/reference/kotlin/android/app/ActivityOptions#setShareIdentityEnabled(kotlin.Boolean)`.

Prior to `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#CINNAMON_BUN:kotlin.Int`, the launching app's identity was not implicitly shared for any result-based launches and could only be retrieved via `https://developer.android.com/reference/kotlin/android/app/Activity#getCallingPackage()`

<br />

`https://developer.android.com/reference/kotlin/android/view/LayoutInflater.html#` `https://developer.android.com/reference/kotlin/android/app/Activity#getLayoutInflater()()`

Convenience for calling `https://developer.android.com/reference/kotlin/android/view/Window.html#getLayoutInflater()`.

<br />

`https://developer.android.com/reference/kotlin/android/app/LoaderManager!` `https://developer.android.com/reference/kotlin/android/app/Activity#getLoaderManager()()`

Return the LoaderManager for this activity, creating it if needed.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#getLocalClassName()()`

Returns class name for this activity with the package prefix removed. This is the default name used to read and write settings.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#getMaxNumPictureInPictureActions()()`

Return the number of actions that will be displayed in the picture-in-picture UI when the user interacts with the activity currently in picture-in-picture mode. This number may change if the global configuration changes (ie. if the device is plugged into an external display), but will always be at least three.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#getMaxNumPictureInPictureOverlayActions()()`

Returns the maximum number of overlay actions that will be displayed in the picture-in-picture window.

Any overlay actions set via `https://developer.android.com/reference/kotlin/android/app/PictureInPictureParams.Builder#setOverlayActions(kotlin.collections.MutableList,%20android.app.RemoteAction)` that exceed this number will not be shown.

<br />

`https://developer.android.com/reference/kotlin/android/media/session/MediaController.html#!` `https://developer.android.com/reference/kotlin/android/app/Activity#getMediaController()()`

Gets the controller which should be receiving media key and volume events while this activity is in the foreground.

<br />

`https://developer.android.com/reference/kotlin/android/view/MenuInflater.html#` `https://developer.android.com/reference/kotlin/android/app/Activity#getMenuInflater()()`

Returns a `https://developer.android.com/reference/kotlin/android/view/MenuInflater.html#` with this context.

<br />

`https://developer.android.com/reference/kotlin/android/window/OnBackInvokedDispatcher.html#` `https://developer.android.com/reference/kotlin/android/app/Activity#getOnBackInvokedDispatcher()()`

Returns the `https://developer.android.com/reference/kotlin/android/window/OnBackInvokedDispatcher.html#` instance associated with the window that this activity is attached to.

<br />

`https://developer.android.com/reference/kotlin/android/app/Activity!` `https://developer.android.com/reference/kotlin/android/app/Activity#getParent()()`

Returns the parent `https://developer.android.com/reference/kotlin/android/app/Activity` if this is a child `https://developer.android.com/reference/kotlin/android/app/Activity` of an `https://developer.android.com/reference/kotlin/android/app/ActivityGroup`.

<br />

`https://developer.android.com/reference/kotlin/android/content/Intent.html#?` `https://developer.android.com/reference/kotlin/android/app/Activity#getParentActivityIntent()()`

Obtain an `https://developer.android.com/reference/kotlin/android/content/Intent.html#` that will launch an explicit target activity specified by this activity's logical parent. The logical parent is named in the application's manifest by the `https://developer.android.com/reference/kotlin/android/R.attr.html#parentActivityName:kotlin.Int` attribute. Activity subclasses may override this method to modify the Intent returned by super.getParentActivityIntent() or to implement a different mechanism of retrieving the parent intent entirely.

<br />

`https://developer.android.com/reference/kotlin/android/content/SharedPreferences.html#!` `https://developer.android.com/reference/kotlin/android/app/Activity#getPreferences(kotlin.Int)(mode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Retrieve a `https://developer.android.com/reference/kotlin/android/content/SharedPreferences.html#` object for accessing preferences that are private to this activity. This simply calls the underlying `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#getSharedPreferences(kotlin.String,%20kotlin.Int)` method by passing in this activity's class name as the preferences name.

<br />

`https://developer.android.com/reference/kotlin/android/net/Uri.html#?` `https://developer.android.com/reference/kotlin/android/app/Activity#getReferrer()()`

Return information about who launched this activity. If the launching Intent contains an `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_REFERRER:kotlin.String`, that will be returned as-is; otherwise, if known, an `https://developer.android.com/reference/kotlin/android/content/Intent.html#URI_ANDROID_APP_SCHEME:kotlin.Int` referrer URI containing the package name that started the Intent will be returned. This may return null if no referrer can be identified -- it is neither explicitly specified, nor is it known which application package was involved.

If called while inside the handling of #onNewIntent, this function will return the referrer that submitted that new intent to the activity only after `https://developer.android.com/reference/kotlin/android/app/Activity#setIntent(android.content.Intent)` is called with the provided intent.

Note that this is *not* a security feature -- you can not trust the referrer information, applications can spoof it.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#getRequestedOrientation()()`

Returns the current requested orientation of the activity, which is either the orientation requested in the app manifest or the last orientation given to `https://developer.android.com/reference/kotlin/android/app/Activity#setRequestedOrientation(kotlin.Int)`. **Note:**

- To improve the layout of apps on form factors with smallest width \>= 600dp, the system ignores calls to this method for apps that target Android 16 (API level 36) or higher.
- Device manufacturers can configure devices to ignore calls to this method to improve the layout of orientation-restricted apps.
- On devices with Android 16 (API level 36) or higher installed, virtual device owners (select trusted and privileged apps) can optimize app layout on displays they manage by ignoring calls to this method. See also [Companion app streaming](https://source.android.com/docs/core/permissions/app-streaming).

See [Device compatibility mode](https://developer.android.com/guide/practices/device-compatibility-mode).

<br />

<br />

`https://developer.android.com/reference/kotlin/android/view/SearchEvent.html#!` `https://developer.android.com/reference/kotlin/android/app/Activity#getSearchEvent()()`

During the onSearchRequested() callbacks, this function will return the `https://developer.android.com/reference/kotlin/android/view/SearchEvent.html#` that triggered the callback, if it exists.

<br />

`https://developer.android.com/reference/kotlin/android/window/SplashScreen.html#` `https://developer.android.com/reference/kotlin/android/app/Activity#getSplashScreen()()`

Get the interface that activity use to talk to the splash screen.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!` `https://developer.android.com/reference/kotlin/android/app/Activity#getSystemService(kotlin.String)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`

Return the handle to a system-level service by name. The class of the returned object varies by the requested name. Currently available names are:

`https://developer.android.com/reference/kotlin/android/content/Context.html#WINDOW_SERVICE:kotlin.String` ("window")
: The top-level window manager in which you can place custom windows. The returned object is a `https://developer.android.com/reference/kotlin/android/view/WindowManager.html#`. Must only be obtained from a visual context such as Activity or a Context created with `https://developer.android.com/reference/kotlin/android/content/Context.html#createWindowContext(kotlin.Int,%20android.os.Bundle)`, which are adjusted to the configuration and visual bounds of an area on screen.

`https://developer.android.com/reference/kotlin/android/content/Context.html#LAYOUT_INFLATER_SERVICE:kotlin.String` ("layout_inflater")
: A `https://developer.android.com/reference/kotlin/android/view/LayoutInflater.html#` for inflating layout resources in this context. Must only be obtained from a visual context such as Activity or a Context created with `https://developer.android.com/reference/kotlin/android/content/Context.html#createWindowContext(kotlin.Int,%20android.os.Bundle)`, which are adjusted to the configuration and visual bounds of an area on screen.

`https://developer.android.com/reference/kotlin/android/content/Context.html#ACTIVITY_SERVICE:kotlin.String` ("activity")
: A `https://developer.android.com/reference/kotlin/android/app/ActivityManager` for interacting with the global activity state of the system.

`https://developer.android.com/reference/kotlin/android/content/Context.html#WALLPAPER_SERVICE:kotlin.String` ("wallpaper")
: A `https://developer.android.com/reference/kotlin/android/service/wallpaper/WallpaperService.html#` for accessing wallpapers in this context. Must only be obtained from a visual context such as Activity or a Context created with `https://developer.android.com/reference/kotlin/android/content/Context.html#createWindowContext(kotlin.Int,%20android.os.Bundle)`, which are adjusted to the configuration and visual bounds of an area on screen.

`https://developer.android.com/reference/kotlin/android/content/Context.html#POWER_SERVICE:kotlin.String` ("power")
: A `https://developer.android.com/reference/kotlin/android/os/PowerManager.html#` for controlling power management.

`https://developer.android.com/reference/kotlin/android/content/Context.html#ALARM_SERVICE:kotlin.String` ("alarm")
: A `https://developer.android.com/reference/kotlin/android/app/AlarmManager` for receiving intents at the time of your choosing.

`https://developer.android.com/reference/kotlin/android/content/Context.html#NOTIFICATION_SERVICE:kotlin.String` ("notification")
: A `https://developer.android.com/reference/kotlin/android/app/NotificationManager` for informing the user of background events.

`https://developer.android.com/reference/kotlin/android/content/Context.html#KEYGUARD_SERVICE:kotlin.String` ("keyguard")
: A `https://developer.android.com/reference/kotlin/android/app/KeyguardManager` for controlling keyguard.

`https://developer.android.com/reference/kotlin/android/content/Context.html#LOCATION_SERVICE:kotlin.String` ("location")
: A `https://developer.android.com/reference/kotlin/android/location/LocationManager.html#` for controlling location (e.g., GPS) updates.

`https://developer.android.com/reference/kotlin/android/content/Context.html#SEARCH_SERVICE:kotlin.String` ("search")
: A `https://developer.android.com/reference/kotlin/android/app/SearchManager` for handling search.

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
: An `https://developer.android.com/reference/kotlin/android/app/UiModeManager` for controlling UI modes.

`https://developer.android.com/reference/kotlin/android/content/Context.html#DOWNLOAD_SERVICE:kotlin.String` ("download")
: A `https://developer.android.com/reference/kotlin/android/app/DownloadManager` for requesting HTTP downloads

`https://developer.android.com/reference/kotlin/android/content/Context.html#BATTERY_SERVICE:kotlin.String` ("batterymanager")
: A `https://developer.android.com/reference/kotlin/android/os/BatteryManager.html#` for managing battery state

`https://developer.android.com/reference/kotlin/android/content/Context.html#JOB_SCHEDULER_SERVICE:kotlin.String` ("taskmanager")
: A `https://developer.android.com/reference/kotlin/android/app/job/JobScheduler` for managing scheduled tasks

`https://developer.android.com/reference/kotlin/android/content/Context.html#NETWORK_STATS_SERVICE:kotlin.String` ("netstats")
: A `https://developer.android.com/reference/kotlin/android/app/usage/NetworkStatsManager` for querying network usage statistics.

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

Note: Instant apps, for which `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#isInstantApp()` returns true, don't have access to the following system services: `https://developer.android.com/reference/kotlin/android/content/Context.html#DEVICE_POLICY_SERVICE:kotlin.String`, #FINGERPRINT_SERVICE, `https://developer.android.com/reference/kotlin/android/content/Context.html#KEYGUARD_SERVICE:kotlin.String`, `https://developer.android.com/reference/kotlin/android/content/Context.html#SHORTCUT_SERVICE:kotlin.String`, `https://developer.android.com/reference/kotlin/android/content/Context.html#USB_SERVICE:kotlin.String`, `https://developer.android.com/reference/kotlin/android/content/Context.html#WALLPAPER_SERVICE:kotlin.String`, `https://developer.android.com/reference/kotlin/android/content/Context.html#WIFI_P2P_SERVICE:kotlin.String`, `https://developer.android.com/reference/kotlin/android/content/Context.html#WIFI_SERVICE:kotlin.String`, `https://developer.android.com/reference/kotlin/android/content/Context.html#WIFI_AWARE_SERVICE:kotlin.String`. For these services this method will return `null`. Generally, if you are running as an instant app you should always check whether the result of this method is `null`.

Note: When implementing this method, keep in mind that new services can be added on newer Android releases, so if you're looking for just the explicit names mentioned above, make sure to return `null` when you don't recognize the name --- if you throw a `https://developer.android.com/reference/kotlin/java/lang/RuntimeException.html#` exception instead, your app might break on new Android releases.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#getTaskId()()`

Return the identifier of the task this activity is in. This identifier will remain the same for the lifetime of the activity.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!` `https://developer.android.com/reference/kotlin/android/app/Activity#getTitle()()`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#getTitleColor()()`

<br />

`https://developer.android.com/reference/kotlin/android/app/VoiceInteractor!` `https://developer.android.com/reference/kotlin/android/app/Activity#getVoiceInteractor()()`

Retrieve the active `https://developer.android.com/reference/kotlin/android/app/VoiceInteractor` that the user is going through to interact with this activity.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#getVolumeControlStream()()`

Gets the suggested audio stream whose volume should be changed by the hardware volume controls.

<br />

`https://developer.android.com/reference/kotlin/android/view/Window.html#!` `https://developer.android.com/reference/kotlin/android/app/Activity#getWindow()()`

Retrieve the current `https://developer.android.com/reference/kotlin/android/view/Window.html#` for the activity. This can be used to directly access parts of the Window API that are not available through Activity/Screen.

<br />

`https://developer.android.com/reference/kotlin/android/view/WindowManager.html#!` `https://developer.android.com/reference/kotlin/android/app/Activity#getWindowManager()()`

Retrieve the window manager for showing custom windows.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#hasWindowFocus()()`

Returns true if this activity's *main* window currently has window focus. Note that this is not the same as the view itself having focus.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#invalidateOptionsMenu()()`

Declare that the options menu has changed, so should be recreated. The `https://developer.android.com/reference/kotlin/android/app/Activity#onCreateOptionsMenu(android.view.Menu)` method will be called the next time it needs to be displayed.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#isActivityTransitionRunning()()`

Returns whether there are any activity transitions currently running on this activity. A return value of `true` can mean that either an enter or exit transition is running, including whether the background of the activity is animating as a part of that transition.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#isChangingConfigurations()()`

Check to see whether this activity is in the process of being destroyed in order to be recreated with a new configuration.

This is often used in `https://developer.android.com/reference/kotlin/android/app/Activity#onStop()` to determine whether the state needs to be cleaned up or will be passed on to the next instance of the activity via `https://developer.android.com/reference/kotlin/android/app/Activity#onRetainNonConfigurationInstance()`. However, if the activity has already been in the background as stopped, and then gets recreated with different configuration, there won't be another `https://developer.android.com/reference/kotlin/android/app/Activity#onPause()` or `https://developer.android.com/reference/kotlin/android/app/Activity#onStop()` with this API returning `true`.

For example, if an activity that is not handling size configuration change is first minimized, and then get rotated with the display, it should first receive `https://developer.android.com/reference/kotlin/android/app/Activity#onPause()` and `https://developer.android.com/reference/kotlin/android/app/Activity#onStop()` with this API returning `false`, and then receive `https://developer.android.com/reference/kotlin/android/app/Activity#onDestroy()` with this API returning `true`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#isChild()()`

Whether this is a child `https://developer.android.com/reference/kotlin/android/app/Activity` of an `https://developer.android.com/reference/kotlin/android/app/ActivityGroup`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#isDestroyed()()`

Returns true if the final `https://developer.android.com/reference/kotlin/android/app/Activity#onDestroy()` call has been made on the Activity, so this instance is now dead.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#isFinishing()()`

Check to see whether this activity is in the process of finishing, either because you called `https://developer.android.com/reference/kotlin/android/app/Activity#finish()` on it or someone else has requested that it finished.

This is often used in `https://developer.android.com/reference/kotlin/android/app/Activity#onPause()` to determine whether the activity is simply pausing or completely finishing. However, if the finish request is made after the activity has already been paused/stopped, there won't be another `https://developer.android.com/reference/kotlin/android/app/Activity#onPause()` or `https://developer.android.com/reference/kotlin/android/app/Activity#onStop()` with this API returning `true`.

For example, if an activity is first minimized, and then gets killed in background, it should first receive `https://developer.android.com/reference/kotlin/android/app/Activity#onPause()` and `https://developer.android.com/reference/kotlin/android/app/Activity#onStop()` with this API returning `false`, and then receive `https://developer.android.com/reference/kotlin/android/app/Activity#onDestroy()` with this API returning `true`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#isHandoffEnabled()()`

Returns if Handoff has been enabled for this Activity. See `https://developer.android.com/reference/kotlin/android/app/Activity#setHandoffEnabled(kotlin.Boolean,%20android.app.HandoffActivityParams)` to change if Handoff is enabled on this Activity. When Handoff is enabled, the user may request this Activity to be sent to other devices that they owe. The system will request data from this Activity to recreate it on the other device. TODO (b/412338142): Add link to onHandoffActivityDataRequested once method is added.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#isImmersive()()`

Bit indicating that this activity is "immersive" and should not be interrupted by notifications if possible. This value is initially set by the manifest property `android:immersive` but may be changed at runtime by `https://developer.android.com/reference/kotlin/android/app/Activity#setImmersive(kotlin.Boolean)`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#isInMultiWindowMode()()`

Returns true if the activity is currently in multi-window mode.

See [Support multi-window mode](https://developer.android.com/develop/ui/compose/layouts/adaptive/support-multi-window-mode) for recommendations on how to handle different multi-window scenarios such as split-screen.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#isInPictureInPictureMode()()`

Returns true if the activity is currently in picture-in-picture mode.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#isLaunchedFromBubble()()`

Indicates whether this activity is launched from a bubble. A bubble is a floating shortcut on the screen that expands to show an activity. If your activity can be used normally or as a bubble, you might use this method to check if the activity is bubbled to modify any behaviour that might be different between the normal activity and the bubbled activity. For example, if you normally cancel the notification associated with the activity when you open the activity, you might not want to do that when you're bubbled as that would remove the bubble. **Note:** This method will return `false` for app Bubbles. See https://developer.android.com/develop/ui/compose/layouts/adaptive/support-bubbles and only applicable to chat bubbles.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#isLocalVoiceInteractionSupported()()`

Queries whether the currently enabled voice interaction service supports returning a voice interactor for use by the activity. This is valid only for the duration of the activity.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#isTaskRoot()()`

Return whether this activity is the root of a task. The root is the first activity in a task.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#isVoiceInteraction()()`

Check whether this activity is running as part of a voice interaction with the user. If true, it should perform its interaction with the user through the `https://developer.android.com/reference/kotlin/android/app/VoiceInteractor` returned by `https://developer.android.com/reference/kotlin/android/app/Activity#getVoiceInteractor()`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#isVoiceInteractionRoot()()`

Like `https://developer.android.com/reference/kotlin/android/app/Activity#isVoiceInteraction()`, but only returns `true` if this is also the root of a voice interaction. That is, returns `true` if this activity was directly started by the voice interaction service as the initiation of a voice interaction. Otherwise, for example if it was started by another activity while under voice interaction, returns `false`. If the activity `https://developer.android.com/reference/kotlin/android/R.styleable.html#AndroidManifestActivity_launchMode:kotlin.Int` is `singleTask`, it forces the activity to launch in a new task, separate from the one that started it. Therefore, there is no longer a relationship between them, and `https://developer.android.com/reference/kotlin/android/app/Activity#isVoiceInteractionRoot()` return `false` in this case.

<br />

`https://developer.android.com/reference/kotlin/android/database/Cursor.html#!` `https://developer.android.com/reference/kotlin/android/app/Activity#managedQuery(android.net.Uri,%20kotlin.Array,%20kotlin.String,%20kotlin.Array,%20kotlin.String)(uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#!, projection: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!, selection: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, selectionArgs: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!, sortOrder: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)`

Wrapper around `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#query(android.net.Uri,%20kotlin.Array,%20kotlin.String,%20kotlin.Array,%20kotlin.String)` that gives the resulting `https://developer.android.com/reference/kotlin/android/database/Cursor.html#` to call `https://developer.android.com/reference/kotlin/android/app/Activity#startManagingCursor(android.database.Cursor)` so that the activity will manage its lifecycle for you. *If you are targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#HONEYCOMB:kotlin.Int` or later, consider instead using `https://developer.android.com/reference/kotlin/android/app/LoaderManager` instead, available via `https://developer.android.com/reference/kotlin/android/app/Activity#getLoaderManager()`.*

**Warning:** Do not call android.database.Cursor#close() on a cursor obtained using this method, because the activity will do that for you at the appropriate time. However, if you call `https://developer.android.com/reference/kotlin/android/app/Activity#stopManagingCursor(android.database.Cursor)` on a cursor from a managed query, the system *will not* automatically close the cursor and, in that case, you must call android.database.Cursor#close().

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#moveTaskToBack(kotlin.Boolean)(nonRoot: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`

Move the task containing this activity to the back of the activity stack. The activity's order within the task is unchanged.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#navigateUpTo(android.content.Intent)(upIntent: https://developer.android.com/reference/kotlin/android/content/Intent.html#!)`

Navigate from this activity to the activity specified by upIntent, finishing this activity in the process. If the activity indicated by upIntent already exists in the task's history, this activity and all others before the indicated activity in the history stack will be finished.

If the indicated activity does not appear in the history stack, this will finish each activity in this task until the root activity of the task is reached, resulting in an "in-app home" behavior. This can be useful in apps with a complex navigation hierarchy when an activity may be reached by a path not passing through a canonical parent activity.

This method should be used when performing up navigation from within the same task as the destination. If up navigation should cross tasks in some cases, see `https://developer.android.com/reference/kotlin/android/app/Activity#shouldUpRecreateTask(android.content.Intent)`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#navigateUpToFromChild(android.app.Activity,%20android.content.Intent)(child: https://developer.android.com/reference/kotlin/android/app/Activity!, upIntent: https://developer.android.com/reference/kotlin/android/content/Intent.html#!)`

This is called when a child activity of this one calls its `https://developer.android.com/reference/kotlin/android/app/Activity#navigateUpTo(android.content.Intent)` method. The default implementation simply calls navigateUpTo(upIntent) on this activity (the parent).

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#onActionModeFinished(android.view.ActionMode)(mode: https://developer.android.com/reference/kotlin/android/view/ActionMode.html#!)`

Notifies the activity that an action mode has finished. Activity subclasses overriding this method should call the superclass implementation. 
If you override this method you *must* call through to the superclass implementation.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#onActionModeStarted(android.view.ActionMode)(mode: https://developer.android.com/reference/kotlin/android/view/ActionMode.html#!)`

Notifies the Activity that an action mode has been started. Activity subclasses overriding this method should call the superclass implementation. 
If you override this method you *must* call through to the superclass implementation.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#onActivityReenter(kotlin.Int,%20android.content.Intent)(resultCode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, data: https://developer.android.com/reference/kotlin/android/content/Intent.html#!)`

Called when an activity you launched with an activity transition exposes this Activity through a returning activity transition, giving you the resultCode and any additional data from it. This method will only be called if the activity set a result code other than `https://developer.android.com/reference/kotlin/android/app/Activity#RESULT_CANCELED:kotlin.Int` and it supports activity transitions with `https://developer.android.com/reference/kotlin/android/view/Window.html#FEATURE_ACTIVITY_TRANSITIONS:kotlin.Int`.

The purpose of this function is to let the called Activity send a hint about its state so that this underlying Activity can prepare to be exposed. A call to this method does not guarantee that the called Activity has or will be exiting soon. It only indicates that it will expose this Activity's Window and it has some data to pass to prepare it.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#onActivityResult(kotlin.Int,%20kotlin.Int,%20android.content.Intent)(requestCode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, resultCode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, data: https://developer.android.com/reference/kotlin/android/content/Intent.html#!)`

Called when an activity you launched exits, giving you the requestCode you started it with, the resultCode it returned, and any additional data from it. The resultCode will be `https://developer.android.com/reference/kotlin/android/app/Activity#RESULT_CANCELED:kotlin.Int` if the activity explicitly returned that, didn't return any result, or crashed during its operation.

An activity can never receive a result in the resumed state. You can count on `https://developer.android.com/reference/kotlin/android/app/Activity#onResume()` being called after this method, though not necessarily immediately after. If the activity was resumed, it will be paused and the result will be delivered, followed by `https://developer.android.com/reference/kotlin/android/app/Activity#onResume()`. If the activity wasn't in the resumed state, then the result will be delivered, with `https://developer.android.com/reference/kotlin/android/app/Activity#onResume()` called sometime later when the activity becomes active again.

This method is never invoked if your activity sets `https://developer.android.com/reference/kotlin/android/R.styleable.html#AndroidManifestActivity_noHistory:kotlin.Int` to `true`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#onActivityResult(kotlin.Int,%20kotlin.Int,%20android.content.Intent,%20android.app.ComponentCaller)(requestCode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, resultCode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, data: https://developer.android.com/reference/kotlin/android/content/Intent.html#?, caller: https://developer.android.com/reference/kotlin/android/app/ComponentCaller)`

Same as `https://developer.android.com/reference/kotlin/android/app/Activity#onActivityResult(kotlin.Int,%20kotlin.Int,%20android.content.Intent)`, but with an extra parameter for the ComponentCaller instance associated with the app that sent the result.

If you want to retrieve the caller without overriding this method, call `https://developer.android.com/reference/kotlin/android/app/Activity#getCurrentCaller()` inside your existing `https://developer.android.com/reference/kotlin/android/app/Activity#onActivityResult(kotlin.Int,%20kotlin.Int,%20android.content.Intent)`.

Note that you should only override one #onActivityResult method.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#onApplyThemeResource(android.content.res.Resources.Theme,%20kotlin.Int,%20kotlin.Boolean)(theme: https://developer.android.com/reference/kotlin/android/content/res/Resources.Theme.html#!, resid: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, first: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`

Called by #setTheme and #getTheme to apply a theme resource to the current Theme object. May be overridden to change the default (simple) behavior. This method will not be called in multiple threads simultaneously.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#onAttachFragment(android.app.Fragment)(fragment: https://developer.android.com/reference/kotlin/android/app/Fragment!)`

Called when a Fragment is being attached to this activity, immediately after the call to its android.app.Fragment#onAttach method and before `https://developer.android.com/reference/kotlin/android/app/Fragment#onCreate(android.os.Bundle)`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#onAttachedToWindow()()`

Called when the main window associated with the activity has been attached to the window manager. See `https://developer.android.com/reference/kotlin/android/view/View.html#onAttachedToWindow()` for more information.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#onBackPressed()()`

Called when the activity has detected the user's press of the back key. The default implementation depends on the platform version:

- On platform versions prior to `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int`, it finishes the current activity, but you can override this to do whatever you want.
- Starting with platform version `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int`, for activities that are the root activity of the task and also declare an `https://developer.android.com/reference/kotlin/android/content/IntentFilter.html#` with `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_MAIN:kotlin.String` and `https://developer.android.com/reference/kotlin/android/content/Intent.html#CATEGORY_LAUNCHER:kotlin.String` in the manifest, the current activity and its task will be moved to the back of the activity stack instead of being finished. Other activities will simply be finished.
- If you target version `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` and override this method, we strongly recommend to call through to the superclass implementation after you finish handling navigation within the app.
- If you target version `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#TIRAMISU:kotlin.Int` or later, you should not use this method but register an `https://developer.android.com/reference/kotlin/android/window/OnBackInvokedCallback.html#` on an `https://developer.android.com/reference/kotlin/android/window/OnBackInvokedDispatcher.html#` that you can retrieve using `https://developer.android.com/reference/kotlin/android/app/Activity#getOnBackInvokedDispatcher()`. You should also set `android:enableOnBackInvokedCallback="true"` in the application manifest.

 Alternatively, you can use `androidx.activity.ComponentActivity#getOnBackPressedDispatcher()` for backward compatibility.

<br />

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#onChildTitleChanged(android.app.Activity,%20kotlin.CharSequence)(childActivity: https://developer.android.com/reference/kotlin/android/app/Activity!, title: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!)`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#onConfigurationChanged(android.content.res.Configuration)(newConfig: https://developer.android.com/reference/kotlin/android/content/res/Configuration.html#)`

Called by the system when the device configuration changes while your activity is running. Note that this will only be called if you have selected configurations you would like to handle with the `https://developer.android.com/reference/kotlin/android/R.attr.html#configChanges:kotlin.Int` attribute in your manifest. If any configuration change occurs that is not selected to be reported by that attribute, then instead of reporting it the system will stop and restart the activity (to have it launched with the new configuration). The only exception is if a size-based configuration is not large enough to be considered significant, in which case the system will not recreate the activity and will instead call this method. For details on this see the documentation on [size-based config change](https://developer.android.com/guide/topics/resources/runtime-changes.html).

At the time that this function has been called, your Resources object will have been updated to return resource values matching the new configuration.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#onContextItemSelected(android.view.MenuItem)(item: https://developer.android.com/reference/kotlin/android/view/MenuItem.html#)`

This hook is called whenever an item in a context menu is selected. The default implementation simply returns false to have the normal processing happen (calling the item's Runnable or sending a message to its Handler as appropriate). You can use this method for any items for which you would like to do processing without those other facilities.

Use `https://developer.android.com/reference/kotlin/android/view/MenuItem.html#getMenuInfo()` to get extra information set by the View that added this menu item.

Derived classes should call through to the base class for it to perform the default menu handling.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#onContextMenuClosed(android.view.Menu)(menu: https://developer.android.com/reference/kotlin/android/view/Menu.html#)`

This hook is called whenever the context menu is being closed (either by the user canceling the menu with the back/menu button, or when an item is selected).

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#onCreate(android.os.Bundle)(savedInstanceState: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?)`

Called when the activity is starting. This is where most initialization should go: calling `https://developer.android.com/reference/kotlin/android/app/Activity#setContentView(kotlin.Int)` to inflate the activity's UI, using `https://developer.android.com/reference/kotlin/android/app/Activity#findViewById(kotlin.Int)` to programmatically interact with widgets in the UI, calling `https://developer.android.com/reference/kotlin/android/app/Activity#managedQuery(android.net.Uri,%20kotlin.Array,%20kotlin.String,%20kotlin.Array,%20kotlin.String)` to retrieve cursors for data being displayed, etc.

You can call `https://developer.android.com/reference/kotlin/android/app/Activity#finish()` from within this function, in which case onDestroy() will be immediately called after #onCreate without any of the rest of the activity lifecycle (`https://developer.android.com/reference/kotlin/android/app/Activity#onStart()`, `https://developer.android.com/reference/kotlin/android/app/Activity#onResume()`, `https://developer.android.com/reference/kotlin/android/app/Activity#onPause()`, etc.) executing.

*Derived classes must call through to the super class's implementation of this method. If they do not, an exception will be thrown.*
. 
This method must be called from the main thread of your app. 
If you override this method you *must* call through to the superclass implementation.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#onCreate(android.os.Bundle,%20android.os.PersistableBundle)(savedInstanceState: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?, persistentState: https://developer.android.com/reference/kotlin/android/os/PersistableBundle.html#?)`

Same as `https://developer.android.com/reference/kotlin/android/app/Activity#onCreate(android.os.Bundle)` but called for those activities created with the attribute `https://developer.android.com/reference/kotlin/android/R.attr.html#persistableMode:kotlin.Int` set to `persistAcrossReboots`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#onCreateContextMenu(android.view.ContextMenu,%20android.view.View,%20android.view.ContextMenu.ContextMenuInfo)(menu: https://developer.android.com/reference/kotlin/android/view/ContextMenu.html#!, v: https://developer.android.com/reference/kotlin/android/view/View.html#!, menuInfo: https://developer.android.com/reference/kotlin/android/view/ContextMenu.ContextMenuInfo.html#!)`

Called when a context menu for the `view` is about to be shown. Unlike `https://developer.android.com/reference/kotlin/android/app/Activity#onCreateOptionsMenu(android.view.Menu)`, this will be called every time the context menu is about to be shown and should be populated for the view (or item inside the view for `https://developer.android.com/reference/kotlin/android/widget/AdapterView.html#` subclasses, this can be found in the `menuInfo`)).

Use `https://developer.android.com/reference/kotlin/android/app/Activity#onContextItemSelected(android.view.MenuItem)` to know when an item has been selected.

It is not safe to hold onto the context menu after this method returns.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html?` `https://developer.android.com/reference/kotlin/android/app/Activity#onCreateDescription()()`

Generate a new description for this activity. This method is called before stopping the activity and can, if desired, return some textual description of its current state to be displayed to the user.

The default implementation returns null, which will cause you to inherit the description from the previous activity. If all activities return null, generally the label of the top activity will be used as the description.

<br />

`https://developer.android.com/reference/kotlin/android/app/Dialog!` `https://developer.android.com/reference/kotlin/android/app/Activity#onCreateDialog(kotlin.Int)(id: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

<br />

`https://developer.android.com/reference/kotlin/android/app/Dialog?` `https://developer.android.com/reference/kotlin/android/app/Activity#onCreateDialog(kotlin.Int,%20android.os.Bundle)(id: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, args: https://developer.android.com/reference/kotlin/android/os/Bundle.html#!)`

Callback for creating dialogs that are managed (saved and restored) for you by the activity. The default implementation calls through to `https://developer.android.com/reference/kotlin/android/app/Activity#onCreateDialog(kotlin.Int)` for compatibility. *If you are targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#HONEYCOMB:kotlin.Int` or later, consider instead using a `https://developer.android.com/reference/kotlin/android/app/DialogFragment` instead.*

If you use `https://developer.android.com/reference/kotlin/android/app/Activity#showDialog(kotlin.Int)`, the activity will call through to this method the first time, and hang onto it thereafter. Any dialog that is created by this method will automatically be saved and restored for you, including whether it is showing.

If you would like the activity to manage saving and restoring dialogs for you, you should override this method and handle any ids that are passed to #showDialog.

If you would like an opportunity to prepare your dialog before it is shown, override `https://developer.android.com/reference/kotlin/android/app/Activity#onPrepareDialog(kotlin.Int,%20android.app.Dialog,%20android.os.Bundle)`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#onCreateNavigateUpTaskStack(android.app.TaskStackBuilder)(builder: https://developer.android.com/reference/kotlin/android/app/TaskStackBuilder!)`

Define the synthetic task stack that will be generated during Up navigation from a different task.

The default implementation of this method adds the parent chain of this activity as specified in the manifest to the supplied `https://developer.android.com/reference/kotlin/android/app/TaskStackBuilder`. Applications may choose to override this method to construct the desired task stack in a different way.

This method will be invoked by the default implementation of `https://developer.android.com/reference/kotlin/android/app/Activity#onNavigateUp()` if `https://developer.android.com/reference/kotlin/android/app/Activity#shouldUpRecreateTask(android.content.Intent)` returns true when supplied with the intent returned by `https://developer.android.com/reference/kotlin/android/app/Activity#getParentActivityIntent()`.

Applications that wish to supply extra Intent parameters to the parent stack defined by the manifest should override `https://developer.android.com/reference/kotlin/android/app/Activity#onPrepareNavigateUpTaskStack(android.app.TaskStackBuilder)`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#onCreateOptionsMenu(android.view.Menu)(menu: https://developer.android.com/reference/kotlin/android/view/Menu.html#!)`

Initialize the contents of the Activity's standard options menu. You should place your menu items in to menu.

This is only called once, the first time the options menu is displayed. To update the menu every time it is displayed, see `https://developer.android.com/reference/kotlin/android/app/Activity#onPrepareOptionsMenu(android.view.Menu)`.

The default implementation populates the menu with standard system menu items. These are placed in the `https://developer.android.com/reference/kotlin/android/view/Menu.html#CATEGORY_SYSTEM:kotlin.Int` group so that they will be correctly ordered with application-defined menu items. Deriving classes should always call through to the base implementation.

You can safely hold on to menu (and any items created from it), making modifications to it as desired, until the next time onCreateOptionsMenu() is called.

When you add items to the menu, you can implement the Activity's `https://developer.android.com/reference/kotlin/android/app/Activity#onOptionsItemSelected(android.view.MenuItem)` method to handle them there.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#onCreatePanelMenu(kotlin.Int,%20android.view.Menu)(featureId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, menu: https://developer.android.com/reference/kotlin/android/view/Menu.html#)`

Default implementation of `https://developer.android.com/reference/kotlin/android/view/Window.Callback.html#onCreatePanelMenu(kotlin.Int,%20android.view.Menu)` for activities. This calls through to the new `https://developer.android.com/reference/kotlin/android/app/Activity#onCreateOptionsMenu(android.view.Menu)` method for the `https://developer.android.com/reference/kotlin/android/view/Window.html#FEATURE_OPTIONS_PANEL:kotlin.Int` panel, so that subclasses of Activity don't need to deal with feature codes.

<br />

`https://developer.android.com/reference/kotlin/android/view/View.html#?` `https://developer.android.com/reference/kotlin/android/app/Activity#onCreatePanelView(kotlin.Int)(featureId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Default implementation of `https://developer.android.com/reference/kotlin/android/view/Window.Callback.html#onCreatePanelView(kotlin.Int)` for activities. This simply returns null so that all panel sub-windows will have the default menu behavior.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#onCreateThumbnail(android.graphics.Bitmap,%20android.graphics.Canvas)(outBitmap: https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#!, canvas: https://developer.android.com/reference/kotlin/android/graphics/Canvas.html#!)`

<br />

`https://developer.android.com/reference/kotlin/android/view/View.html#?` `https://developer.android.com/reference/kotlin/android/app/Activity#onCreateView(android.view.View,%20kotlin.String,%20android.content.Context,%20android.util.AttributeSet)(parent: https://developer.android.com/reference/kotlin/android/view/View.html#?, name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, context: https://developer.android.com/reference/kotlin/android/content/Context.html#, attrs: https://developer.android.com/reference/kotlin/android/util/AttributeSet.html#)`

Standard implementation of `https://developer.android.com/reference/kotlin/android/view/LayoutInflater.Factory2.html#onCreateView(android.view.View,%20kotlin.String,%20android.content.Context,%20android.util.AttributeSet)` used when inflating with the LayoutInflater returned by #getSystemService. This implementation handles tags to embed fragments inside of the activity.

<br />

`https://developer.android.com/reference/kotlin/android/view/View.html#?` `https://developer.android.com/reference/kotlin/android/app/Activity#onCreateView(kotlin.String,%20android.content.Context,%20android.util.AttributeSet)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, context: https://developer.android.com/reference/kotlin/android/content/Context.html#, attrs: https://developer.android.com/reference/kotlin/android/util/AttributeSet.html#)`

Standard implementation of `https://developer.android.com/reference/kotlin/android/view/LayoutInflater.Factory.html#onCreateView(kotlin.String,%20android.content.Context,%20android.util.AttributeSet)` used when inflating with the LayoutInflater returned by #getSystemService. This implementation does nothing and is for pre-`https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#HONEYCOMB:kotlin.Int` apps. Newer apps should use `https://developer.android.com/reference/kotlin/android/app/Activity#onCreateView(android.view.View,%20kotlin.String,%20android.content.Context,%20android.util.AttributeSet)`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#onDetachedFromWindow()()`

Called when the main window associated with the activity has been detached from the window manager. See `https://developer.android.com/reference/kotlin/android/view/View.html#onDetachedFromWindow()` for more information.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#onEnterAnimationComplete()()`

Activities cannot draw during the period that their windows are animating in. In order to know when it is safe to begin drawing they can override this method which will be called when the entering animation has completed.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#onGenericMotionEvent(android.view.MotionEvent)(event: https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#!)`

Called when a generic motion event was not handled by any of the views inside of the activity.

Generic motion events describe joystick movements, hover events from mouse or stylus devices, trackpad touches, scroll wheel movements and other motion events not handled by `https://developer.android.com/reference/kotlin/android/app/Activity#onTouchEvent(android.view.MotionEvent)` or `https://developer.android.com/reference/kotlin/android/app/Activity#onTrackballEvent(android.view.MotionEvent)`. The `https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#getSource()` of the motion event specifies the class of input that was received. Implementations of this method must examine the bits in the source before processing the event.

Generic motion events with source class `https://developer.android.com/reference/kotlin/android/view/InputDevice.html#SOURCE_CLASS_POINTER:kotlin.Int` are delivered to the view under the pointer. All other generic motion events are delivered to the focused view.

See `https://developer.android.com/reference/kotlin/android/view/View.html#onGenericMotionEvent(android.view.MotionEvent)` for an example of how to handle this event.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#onGetDirectActions(android.os.CancellationSignal,%20java.util.function.Consumer)(cancellationSignal: https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#, callback: https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/app/DirectAction!>!>)`

Returns the list of direct actions supported by the app.

You should return the list of actions that could be executed in the current context, which is in the current state of the app. If the actions that could be executed by the app changes you should report that via calling `https://developer.android.com/reference/kotlin/android/app/VoiceInteractor#notifyDirectActionsChanged()`.

To get the voice interactor you need to call `https://developer.android.com/reference/kotlin/android/app/Activity#getVoiceInteractor()` which would return non `null` only if there is an ongoing voice interaction session. You can also detect when the voice interactor is no longer valid because the voice interaction session that is backing is finished by calling `https://developer.android.com/reference/kotlin/android/app/VoiceInteractor#registerOnDestroyedCallback(java.util.concurrent.Executor,%20java.lang.Runnable)`.

This method will be called only after `https://developer.android.com/reference/kotlin/android/app/Activity#onStart()` and before `https://developer.android.com/reference/kotlin/android/app/Activity#onStop()`.

You should pass to the callback the currently supported direct actions which cannot be `null` or contain `null` elements.

You should return the action list as soon as possible to ensure the consumer, for example the assistant, is as responsive as possible which would improve user experience of your app.

<br />

`https://developer.android.com/reference/kotlin/android/app/HandoffActivityData?` `https://developer.android.com/reference/kotlin/android/app/Activity#onHandoffActivityDataRequested(android.app.HandoffActivityDataRequestInfo)(requestInfo: https://developer.android.com/reference/kotlin/android/app/HandoffActivityDataRequestInfo)`

Retrieves `https://developer.android.com/reference/kotlin/android/app/HandoffActivityData` representing this activity, allowing it to be recreated on another device owned by the user. The system automatically handles calling #onHandoffActivityDataRequested. This will only be called if `https://developer.android.com/reference/kotlin/android/app/Activity#isHandoffEnabled()` is `true` for this activity. If `https://developer.android.com/reference/kotlin/android/app/Activity#isHandoffEnabled()` is `true`, the activity is expected to return a non-null value. Returning `null` will present an error to the user indicating Handoff unexpectedly failed. If the current activity is in the foreground on the current device, the app's icon representing this activity will be shown on other nearby devices owned by the user. If the user selects this icon, the system will call this method to retrieve the data needed to recreate this activity on another device. When this activity is stopped, the system will call this method to retrieve `https://developer.android.com/reference/kotlin/android/app/HandoffActivityData` for caching. This allows the user to hand this activity off to another device even if it is not currently running. In these situations, `https://developer.android.com/reference/kotlin/android/app/HandoffActivityDataRequestInfo#isActiveRequest()` will be `false`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#onKeyDown(kotlin.Int,%20android.view.KeyEvent)(keyCode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, event: https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#!)`

Called when a key was pressed down and not handled by any of the views inside of the activity. So, for example, key presses while the cursor is inside a TextView will not trigger the event (unless it is a navigation to another object) because TextView handles its own key presses.

If the focused view didn't want this event, this method is called.

The default implementation takes care of `https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#KEYCODE_BACK:kotlin.Int` by calling `https://developer.android.com/reference/kotlin/android/app/Activity#onBackPressed()`, though the behavior varies based on the application compatibility mode: for `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#ECLAIR:kotlin.Int` or later applications, it will set up the dispatch to call `https://developer.android.com/reference/kotlin/android/app/Activity#onKeyUp(kotlin.Int,%20android.view.KeyEvent)` where the action will be performed; for earlier applications, it will perform the action immediately in on-down, as those versions of the platform behaved. This implementation will also take care of `https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#KEYCODE_ESCAPE:kotlin.Int` by finishing the activity if it would be closed by touching outside of it.

Other additional default key handling may be performed if configured with `https://developer.android.com/reference/kotlin/android/app/Activity#setDefaultKeyMode(kotlin.Int)`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#onKeyLongPress(kotlin.Int,%20android.view.KeyEvent)(keyCode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, event: https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#!)`

Default implementation of `https://developer.android.com/reference/kotlin/android/view/KeyEvent.Callback.html#onKeyLongPress(kotlin.Int,%20android.view.KeyEvent)`: always returns false (doesn't handle the event). To receive this callback, you must return true from onKeyDown for the current event stream.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#onKeyMultiple(kotlin.Int,%20kotlin.Int,%20android.view.KeyEvent)(keyCode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, repeatCount: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, event: https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#!)`

Default implementation of `https://developer.android.com/reference/kotlin/android/view/KeyEvent.Callback.html#onKeyMultiple(kotlin.Int,%20kotlin.Int,%20android.view.KeyEvent)`: always returns false (doesn't handle the event).

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#onKeyShortcut(kotlin.Int,%20android.view.KeyEvent)(keyCode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, event: https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#!)`

Called when a key shortcut event is not handled by any of the views in the Activity. Override this method to implement global key shortcuts for the Activity. Key shortcuts can also be implemented by setting the `https://developer.android.com/reference/kotlin/android/view/MenuItem.html#setShortcut(kotlin.Char,%20kotlin.Char)` property of menu items.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#onKeyUp(kotlin.Int,%20android.view.KeyEvent)(keyCode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, event: https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#!)`

Called when a key was released and not handled by any of the views inside of the activity. So, for example, key presses while the cursor is inside a TextView will not trigger the event (unless it is a navigation to another object) because TextView handles its own key presses.

The default implementation handles KEYCODE_BACK to stop the activity and go back.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#onLocalVoiceInteractionStarted()()`

Callback to indicate that `https://developer.android.com/reference/kotlin/android/app/Activity#startLocalVoiceInteraction(android.os.Bundle)` has resulted in a voice interaction session being started. You can now retrieve a voice interactor using `https://developer.android.com/reference/kotlin/android/app/Activity#getVoiceInteractor()`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#onLocalVoiceInteractionStopped()()`

Callback to indicate that the local voice interaction has stopped either because it was requested through a call to `https://developer.android.com/reference/kotlin/android/app/Activity#stopLocalVoiceInteraction()` or because it was canceled by the user. The previously acquired `https://developer.android.com/reference/kotlin/android/app/VoiceInteractor` is no longer valid after this.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#onLowMemory()()`

This is called when the overall system is running low on memory, and actively running processes should trim their memory usage. While the exact point at which this will be called is not defined, generally it will happen when all background process have been killed. That is, before reaching the point of killing processes hosting service and foreground UI that we would like to avoid killing.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#onMenuItemSelected(kotlin.Int,%20android.view.MenuItem)(featureId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, item: https://developer.android.com/reference/kotlin/android/view/MenuItem.html#)`

Default implementation of `https://developer.android.com/reference/kotlin/android/view/Window.Callback.html#onMenuItemSelected(kotlin.Int,%20android.view.MenuItem)` for activities. This calls through to the new `https://developer.android.com/reference/kotlin/android/app/Activity#onOptionsItemSelected(android.view.MenuItem)` method for the `https://developer.android.com/reference/kotlin/android/view/Window.html#FEATURE_OPTIONS_PANEL:kotlin.Int` panel, so that subclasses of Activity don't need to deal with feature codes.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#onMenuOpened(kotlin.Int,%20android.view.Menu)(featureId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, menu: https://developer.android.com/reference/kotlin/android/view/Menu.html#)`

Called when a panel's menu is opened by the user. This may also be called when the menu is changing from one type to another (for example, from the icon menu to the expanded menu).

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#onMultiWindowModeChanged(kotlin.Boolean)(isInMultiWindowMode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`

Called by the system when the activity changes from fullscreen mode to multi-window mode and visa-versa.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#onMultiWindowModeChanged(kotlin.Boolean,%20android.content.res.Configuration)(isInMultiWindowMode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html, newConfig: https://developer.android.com/reference/kotlin/android/content/res/Configuration.html#!)`

Called by the system when the activity changes from fullscreen mode to multi-window mode and visa-versa. This method provides the same configuration that will be sent in the following `https://developer.android.com/reference/kotlin/android/app/Activity#onConfigurationChanged(android.content.res.Configuration)` call after the activity enters this mode.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#onNavigateUp()()`

This method is called whenever the user chooses to navigate Up within your application's activity hierarchy from the action bar.

If the attribute `https://developer.android.com/reference/kotlin/android/R.attr.html#parentActivityName:kotlin.Int` was specified in the manifest for this activity or an activity-alias to it, default Up navigation will be handled automatically. If any activity along the parent chain requires extra Intent arguments, the Activity subclass should override the method `https://developer.android.com/reference/kotlin/android/app/Activity#onPrepareNavigateUpTaskStack(android.app.TaskStackBuilder)` to supply those arguments.

See [Tasks and Back Stack](https://developer.android.com/guide/components/tasks-and-back-stack.html) from the developer guide and [Navigation](https://developer.android.com/design/patterns/navigation.html) from the design guide for more information about navigating within your app.

See the `https://developer.android.com/reference/kotlin/android/app/TaskStackBuilder` class and the Activity methods `https://developer.android.com/reference/kotlin/android/app/Activity#getParentActivityIntent()`, `https://developer.android.com/reference/kotlin/android/app/Activity#shouldUpRecreateTask(android.content.Intent)`, and `https://developer.android.com/reference/kotlin/android/app/Activity#navigateUpTo(android.content.Intent)` for help implementing custom Up navigation. The AppNavigation sample application in the Android SDK is also available for reference.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#onNavigateUpFromChild(android.app.Activity)(child: https://developer.android.com/reference/kotlin/android/app/Activity!)`

This is called when a child activity of this one attempts to navigate up. The default implementation simply calls onNavigateUp() on this activity (the parent).

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#onNewIntent(android.content.Intent)(intent: https://developer.android.com/reference/kotlin/android/content/Intent.html#!)`

This is called for activities that set launchMode to "singleTop" in their package, or if a client used the `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_ACTIVITY_SINGLE_TOP:kotlin.Int` flag when calling #startActivity. In either case, when the activity is re-launched while at the top of the activity stack instead of a new instance of the activity being started, onNewIntent() will be called on the existing instance with the Intent that was used to re-launch it.

An activity can never receive a new intent in the resumed state. You can count on `https://developer.android.com/reference/kotlin/android/app/Activity#onResume()` being called after this method, though not necessarily immediately after the completion of this callback. If the activity was resumed, it will be paused and new intent will be delivered, followed by `https://developer.android.com/reference/kotlin/android/app/Activity#onResume()`. If the activity wasn't in the resumed state, then new intent can be delivered immediately, with `https://developer.android.com/reference/kotlin/android/app/Activity#onResume()` called sometime later when activity becomes active again.

Note that `https://developer.android.com/reference/kotlin/android/app/Activity#getIntent()` still returns the original Intent. You can use `https://developer.android.com/reference/kotlin/android/app/Activity#setIntent(android.content.Intent)` to update it to this new Intent.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#onNewIntent(android.content.Intent,%20android.app.ComponentCaller)(intent: https://developer.android.com/reference/kotlin/android/content/Intent.html#, caller: https://developer.android.com/reference/kotlin/android/app/ComponentCaller)`

Same as `https://developer.android.com/reference/kotlin/android/app/Activity#onNewIntent(android.content.Intent)`, but with an extra parameter for the ComponentCaller instance associated with the app that sent the intent.

If you want to retrieve the caller without overriding this method, call `https://developer.android.com/reference/kotlin/android/app/Activity#getCurrentCaller()` inside your existing `https://developer.android.com/reference/kotlin/android/app/Activity#onNewIntent(android.content.Intent)`.

Note that you should only override one #onNewIntent method.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#onOptionsItemSelected(android.view.MenuItem)(item: https://developer.android.com/reference/kotlin/android/view/MenuItem.html#)`

This hook is called whenever an item in your options menu is selected. The default implementation simply returns false to have the normal processing happen (calling the item's Runnable or sending a message to its Handler as appropriate). You can use this method for any items for which you would like to do processing without those other facilities.

Derived classes should call through to the base class for it to perform the default menu handling.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#onOptionsMenuClosed(android.view.Menu)(menu: https://developer.android.com/reference/kotlin/android/view/Menu.html#!)`

This hook is called whenever the options menu is being closed (either by the user canceling the menu with the back/menu button, or when an item is selected).

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#onPanelClosed(kotlin.Int,%20android.view.Menu)(featureId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, menu: https://developer.android.com/reference/kotlin/android/view/Menu.html#)`

Default implementation of `https://developer.android.com/reference/kotlin/android/view/Window.Callback.html#onPanelClosed(kotlin.Int,%20android.view.Menu)` for activities. This calls through to `https://developer.android.com/reference/kotlin/android/app/Activity#onOptionsMenuClosed(android.view.Menu)` method for the `https://developer.android.com/reference/kotlin/android/view/Window.html#FEATURE_OPTIONS_PANEL:kotlin.Int` panel, so that subclasses of Activity don't need to deal with feature codes. For context menus (`https://developer.android.com/reference/kotlin/android/view/Window.html#FEATURE_CONTEXT_MENU:kotlin.Int`), the `https://developer.android.com/reference/kotlin/android/app/Activity#onContextMenuClosed(android.view.Menu)` will be called.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#onPause()()`

Called as part of the activity lifecycle when the user no longer actively interacts with the activity, but it is still visible on screen. The counterpart to `https://developer.android.com/reference/kotlin/android/app/Activity#onResume()`

When activity B is launched in front of activity A, this callback will be invoked on A. B will not be created until A's `https://developer.android.com/reference/kotlin/android/app/Activity#onPause()` returns, so be sure to not do anything lengthy here.

This callback is mostly used for saving any persistent state the activity is editing, to present a "edit in place" model to the user and making sure nothing is lost if there are not enough resources to start the new activity without first killing this one. This is also a good place to stop things that consume a noticeable amount of CPU in order to make the switch to the next activity as fast as possible.

On platform versions prior to `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#Q:kotlin.Int` this is also a good place to try to close exclusive-access devices or to release access to singleton resources. Starting with `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#Q:kotlin.Int` there can be multiple resumed activities in the system at the same time, so `https://developer.android.com/reference/kotlin/android/app/Activity#onTopResumedActivityChanged(kotlin.Boolean)` should be used for that purpose instead.

If an activity is launched on top, after receiving this call you will usually receive a following call to `https://developer.android.com/reference/kotlin/android/app/Activity#onStop()` (after the next activity has been resumed and displayed above). However in some cases there will be a direct call back to `https://developer.android.com/reference/kotlin/android/app/Activity#onResume()` without going through the stopped state. An activity can also rest in paused state in some cases when in multi-window mode, still visible to user.

*Derived classes must call through to the super class's implementation of this method. If they do not, an exception will be thrown.*
. 
If you override this method you *must* call through to the superclass implementation.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#onPerformDirectAction(kotlin.String,%20android.os.Bundle,%20android.os.CancellationSignal,%20java.util.function.Consumer)(actionId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, arguments: https://developer.android.com/reference/kotlin/android/os/Bundle.html#, cancellationSignal: https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#, resultListener: https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#<https://developer.android.com/reference/kotlin/android/os/Bundle.html#!>)`

This is called to perform an action previously defined by the app. Apps also have access to `https://developer.android.com/reference/kotlin/android/app/Activity#getVoiceInteractor()` to follow up on the action.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#onPictureInPictureModeChanged(kotlin.Boolean)(isInPictureInPictureMode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`

Called by the system when the activity changes to and from picture-in-picture mode.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#onPictureInPictureModeChanged(kotlin.Boolean,%20android.content.res.Configuration)(isInPictureInPictureMode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html, newConfig: https://developer.android.com/reference/kotlin/android/content/res/Configuration.html#!)`

Called by the system when the activity changes to and from picture-in-picture mode. This method provides the same configuration that will be sent in the following `https://developer.android.com/reference/kotlin/android/app/Activity#onConfigurationChanged(android.content.res.Configuration)` call after the activity enters this mode.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#onPictureInPictureRequested()()`

This method is called by the system in various cases where picture in picture mode should be entered if supported.

It is up to the app developer to choose whether to call `https://developer.android.com/reference/kotlin/android/app/Activity#enterPictureInPictureMode(android.app.PictureInPictureParams)` at this time. For example, the system will call this method when the activity is being put into the background, so the app developer might want to switch an activity into PIP mode instead.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#onPictureInPictureUiStateChanged(android.app.PictureInPictureUiState)(pipState: https://developer.android.com/reference/kotlin/android/app/PictureInPictureUiState)`

Called by the system when the activity is in PiP and has state changes. Compare to `https://developer.android.com/reference/kotlin/android/app/Activity#onPictureInPictureModeChanged(kotlin.Boolean,%20android.content.res.Configuration)`, which is only called when PiP mode changes (meaning, enters or exits PiP), this can be called at any time while the activity is in PiP mode. Therefore, all invocation can only happen after `https://developer.android.com/reference/kotlin/android/app/Activity#onPictureInPictureModeChanged(kotlin.Boolean,%20android.content.res.Configuration)` is called with true, and before `https://developer.android.com/reference/kotlin/android/app/Activity#onPictureInPictureModeChanged(kotlin.Boolean,%20android.content.res.Configuration)` is called with false. You would not need to worry about cases where this is called and the activity is not in Picture-In-Picture mode. For managing cases where the activity enters/exits Picture-in-Picture (e.g. resources clean-up on exit), use `https://developer.android.com/reference/kotlin/android/app/Activity#onPictureInPictureModeChanged(kotlin.Boolean,%20android.content.res.Configuration)`. The default state is everything declared in `https://developer.android.com/reference/kotlin/android/app/PictureInPictureUiState` is false, such as `https://developer.android.com/reference/kotlin/android/app/PictureInPictureUiState#isStashed()`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#onPostCreate(android.os.Bundle)(savedInstanceState: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?)`

Called when activity start-up is complete (after `https://developer.android.com/reference/kotlin/android/app/Activity#onStart()` and #onRestoreInstanceState have been called). Applications will generally not implement this method; it is intended for system classes to do final initialization after application code has run.

*Derived classes must call through to the super class's implementation of this method. If they do not, an exception will be thrown.*
. 
If you override this method you *must* call through to the superclass implementation.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#onPostCreate(android.os.Bundle,%20android.os.PersistableBundle)(savedInstanceState: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?, persistentState: https://developer.android.com/reference/kotlin/android/os/PersistableBundle.html#?)`

This is the same as `https://developer.android.com/reference/kotlin/android/app/Activity#onPostCreate(android.os.Bundle)` but is called for activities created with the attribute `https://developer.android.com/reference/kotlin/android/R.attr.html#persistableMode:kotlin.Int` set to `persistAcrossReboots`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#onPostResume()()`

Called when activity resume is complete (after `https://developer.android.com/reference/kotlin/android/app/Activity#onResume()` has been called). Applications will generally not implement this method; it is intended for system classes to do final setup after application resume code has run.

*Derived classes must call through to the super class's implementation of this method. If they do not, an exception will be thrown.*
. 
If you override this method you *must* call through to the superclass implementation.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#onPrepareDialog(kotlin.Int,%20android.app.Dialog)(id: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, dialog: https://developer.android.com/reference/kotlin/android/app/Dialog!)`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#onPrepareDialog(kotlin.Int,%20android.app.Dialog,%20android.os.Bundle)(id: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, dialog: https://developer.android.com/reference/kotlin/android/app/Dialog!, args: https://developer.android.com/reference/kotlin/android/os/Bundle.html#!)`

Provides an opportunity to prepare a managed dialog before it is being shown. The default implementation calls through to `https://developer.android.com/reference/kotlin/android/app/Activity#onPrepareDialog(kotlin.Int,%20android.app.Dialog)` for compatibility.

Override this if you need to update a managed dialog based on the state of the application each time it is shown. For example, a time picker dialog might want to be updated with the current time. You should call through to the superclass's implementation. The default implementation will set this Activity as the owner activity on the Dialog.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#onPrepareNavigateUpTaskStack(android.app.TaskStackBuilder)(builder: https://developer.android.com/reference/kotlin/android/app/TaskStackBuilder!)`

Prepare the synthetic task stack that will be generated during Up navigation from a different task.

This method receives the `https://developer.android.com/reference/kotlin/android/app/TaskStackBuilder` with the constructed series of Intents as generated by `https://developer.android.com/reference/kotlin/android/app/Activity#onCreateNavigateUpTaskStack(android.app.TaskStackBuilder)`. If any extra data should be added to these intents before launching the new task, the application should override this method and add that data here.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#onPrepareOptionsMenu(android.view.Menu)(menu: https://developer.android.com/reference/kotlin/android/view/Menu.html#!)`

Prepare the Screen's standard options menu to be displayed. This is called right before the menu is shown, every time it is shown. You can use this method to efficiently enable/disable items or otherwise dynamically modify the contents.

The default implementation updates the system menu items based on the activity's state. Deriving classes should always call through to the base class implementation.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#onPreparePanel(kotlin.Int,%20android.view.View,%20android.view.Menu)(featureId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, view: https://developer.android.com/reference/kotlin/android/view/View.html#?, menu: https://developer.android.com/reference/kotlin/android/view/Menu.html#)`

Default implementation of `https://developer.android.com/reference/kotlin/android/view/Window.Callback.html#onPreparePanel(kotlin.Int,%20android.view.View,%20android.view.Menu)` for activities. This calls through to the new `https://developer.android.com/reference/kotlin/android/app/Activity#onPrepareOptionsMenu(android.view.Menu)` method for the `https://developer.android.com/reference/kotlin/android/view/Window.html#FEATURE_OPTIONS_PANEL:kotlin.Int` panel, so that subclasses of Activity don't need to deal with feature codes.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#onProvideAssistContent(android.app.assist.AssistContent)(outContent: https://developer.android.com/reference/kotlin/android/app/assist/AssistContent!)`

This is called when the user is requesting an assist, to provide references to content related to the current activity. Before being called, the `outContent` Intent is filled with the base Intent of the activity (the Intent returned by `https://developer.android.com/reference/kotlin/android/app/Activity#getIntent()`). The Intent's extras are stripped of any types that are not valid for `https://developer.android.com/reference/kotlin/android/os/PersistableBundle.html#` or non-framework Parcelables, and the flags `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_GRANT_WRITE_URI_PERMISSION:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_GRANT_PERSISTABLE_URI_PERMISSION:kotlin.Int` are cleared from the Intent.

Custom implementation may adjust the content intent to better reflect the top-level context of the activity, and fill in its ClipData with additional content of interest that the user is currently viewing. For example, an image gallery application that has launched in to an activity allowing the user to swipe through pictures should modify the intent to reference the current image they are looking it; such an application when showing a list of pictures should add a ClipData that has references to all of the pictures currently visible on screen.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#onProvideAssistData(android.os.Bundle)(data: https://developer.android.com/reference/kotlin/android/os/Bundle.html#!)`

This is called when the user is requesting an assist, to build a full `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_ASSIST:kotlin.String` Intent with all of the context of the current application. You can override this method to place into the bundle anything you would like to appear in the `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_ASSIST_CONTEXT:kotlin.String` part of the assist Intent.

This function will be called after any global assist callbacks that had been registered with `https://developer.android.com/reference/kotlin/android/app/Application#registerOnProvideAssistDataListener(android.app.Application.OnProvideAssistDataListener)`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#onProvideKeyboardShortcuts(kotlin.collections.MutableList,%20android.view.Menu,%20kotlin.Int)(data: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/view/KeyboardShortcutGroup.html#!>!, menu: https://developer.android.com/reference/kotlin/android/view/Menu.html#?, deviceId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Called when Keyboard Shortcuts are requested for the current window.

<br />

`https://developer.android.com/reference/kotlin/android/net/Uri.html#!` `https://developer.android.com/reference/kotlin/android/app/Activity#onProvideReferrer()()`

Override to generate the desired referrer for the content currently being shown by the app. The default implementation returns null, meaning the referrer will simply be the android-app: of the package name of this activity. Return a non-null Uri to have that supplied as the `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_REFERRER:kotlin.String` of any activities started from it.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#onRequestPermissionsResult(kotlin.Int,%20kotlin.Array,%20kotlin.IntArray)(requestCode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, permissions: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>, grantResults: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)`

Callback for the result from requesting permissions. This method is invoked for every call on #requestPermissions

**Note:** It is possible that the permissions request interaction with the user is interrupted. In this case you will receive empty permissions and results arrays which should be treated as a cancellation.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#onRequestPermissionsResult(kotlin.Int,%20kotlin.Array,%20kotlin.IntArray,%20kotlin.Int)(requestCode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, permissions: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>, grantResults: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html, deviceId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Callback for the result from requesting permissions. This method is invoked for every call on #requestPermissions.

**Note:** It is possible that the permissions request interaction with the user is interrupted. In this case you will receive empty permissions and results arrays which should be treated as a cancellation.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#onRestart()()`

Called after `https://developer.android.com/reference/kotlin/android/app/Activity#onStop()` when the current activity is being re-displayed to the user (the user has navigated back to it). It will be followed by `https://developer.android.com/reference/kotlin/android/app/Activity#onStart()` and then `https://developer.android.com/reference/kotlin/android/app/Activity#onResume()`

For activities that are using raw `https://developer.android.com/reference/kotlin/android/database/Cursor.html#` objects (instead of creating them through `https://developer.android.com/reference/kotlin/android/app/Activity#managedQuery(android.net.Uri,%20kotlin.Array,%20kotlin.String,%20kotlin.Array,%20kotlin.String)`, this is usually the place where the cursor should be requeried (because you had deactivated it in `https://developer.android.com/reference/kotlin/android/app/Activity#onStop()`.

*Derived classes must call through to the super class's implementation of this method. If they do not, an exception will be thrown.*
. 
If you override this method you *must* call through to the superclass implementation.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#onRestoreInstanceState(android.os.Bundle,%20android.os.PersistableBundle)(savedInstanceState: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?, persistentState: https://developer.android.com/reference/kotlin/android/os/PersistableBundle.html#?)`

This is the same as `https://developer.android.com/reference/kotlin/android/app/Activity#onRestoreInstanceState(android.os.Bundle)` but is called for activities created with the attribute `https://developer.android.com/reference/kotlin/android/R.attr.html#persistableMode:kotlin.Int` set to `persistAcrossReboots`. The `https://developer.android.com/reference/kotlin/android/os/PersistableBundle.html#` passed came from the restored PersistableBundle first saved in `https://developer.android.com/reference/kotlin/android/app/Activity#onSaveInstanceState(android.os.Bundle,%20android.os.PersistableBundle)`.

This method is called between `https://developer.android.com/reference/kotlin/android/app/Activity#onStart()` and #onPostCreate.

If this method is called `https://developer.android.com/reference/kotlin/android/app/Activity#onRestoreInstanceState(android.os.Bundle)` will not be called.

At least one of `savedInstanceState` or `persistentState` will not be null.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#onResume()()`

Called after #onRestoreInstanceState, `https://developer.android.com/reference/kotlin/android/app/Activity#onRestart()`, or `https://developer.android.com/reference/kotlin/android/app/Activity#onPause()`. This is usually a hint for your activity to start interacting with the user, which is a good indicator that the activity became active and ready to receive input. This sometimes could also be a transit state toward another resting state. For instance, an activity may be relaunched to `https://developer.android.com/reference/kotlin/android/app/Activity#onPause()` due to configuration changes and the activity was visible, but wasn't the top-most activity of an activity task. `https://developer.android.com/reference/kotlin/android/app/Activity#onResume()` is guaranteed to be called before `https://developer.android.com/reference/kotlin/android/app/Activity#onPause()` in this case which honors the activity lifecycle policy and the activity eventually rests in `https://developer.android.com/reference/kotlin/android/app/Activity#onPause()`

On platform versions prior to `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#Q:kotlin.Int` this is also a good place to try to open exclusive-access devices or to get access to singleton resources. Starting with `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#Q:kotlin.Int` there can be multiple resumed activities in the system simultaneously, so `https://developer.android.com/reference/kotlin/android/app/Activity#onTopResumedActivityChanged(kotlin.Boolean)` should be used for that purpose instead.

*Derived classes must call through to the super class's implementation of this method. If they do not, an exception will be thrown.*
. 
If you override this method you *must* call through to the superclass implementation.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!` `https://developer.android.com/reference/kotlin/android/app/Activity#onRetainNonConfigurationInstance()()`

Called by the system, as part of destroying an activity due to a configuration change, when it is known that a new instance will immediately be created for the new configuration. You can return any object you like here, including the activity instance itself, which can later be retrieved by calling `https://developer.android.com/reference/kotlin/android/app/Activity#getLastNonConfigurationInstance()` in the new activity instance. *If you are targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#HONEYCOMB:kotlin.Int` or later, consider instead using a `https://developer.android.com/reference/kotlin/android/app/Fragment` with `https://developer.android.com/reference/kotlin/android/app/Fragment#setRetainInstance(kotlin.Boolean)`.*

This function is called purely as an optimization, and you must not rely on it being called. When it is called, a number of guarantees will be made to help optimize configuration switching:

- The function will be called between `https://developer.android.com/reference/kotlin/android/app/Activity#onStop()` and `https://developer.android.com/reference/kotlin/android/app/Activity#onDestroy()`.
- A new instance of the activity will *always* be immediately created after this one's `https://developer.android.com/reference/kotlin/android/app/Activity#onDestroy()` is called. In particular, *no* messages will be dispatched during this time (when the returned object does not have an activity to be associated with).
- The object you return here will *always* be available from the `https://developer.android.com/reference/kotlin/android/app/Activity#getLastNonConfigurationInstance()` method of the following activity instance as described there.

These guarantees are designed so that an activity can use this API to propagate extensive state from the old to new activity instance, from loaded bitmaps, to network connections, to evenly actively running threads. Note that you should *not* propagate any data that may change based on the configuration, including any data loaded from resources such as strings, layouts, or drawables.

The guarantee of no message handling during the switch to the next activity simplifies use with active objects. For example if your retained state is an `https://developer.android.com/reference/kotlin/android/os/AsyncTask.html#` you are guaranteed that its call back functions (like `https://developer.android.com/reference/kotlin/android/os/AsyncTask.html#onPostExecute(android.os.AsyncTask.Result)`) will not be called from the call here until you execute the next instance's `https://developer.android.com/reference/kotlin/android/app/Activity#onCreate(android.os.Bundle)`. (Note however that there is of course no such guarantee for `https://developer.android.com/reference/kotlin/android/os/AsyncTask.html#doInBackground(android.os.AsyncTask.Params)` since that is running in a separate thread.)

**Note:** For most cases you should use the `https://developer.android.com/reference/kotlin/android/app/Fragment` API `https://developer.android.com/reference/kotlin/android/app/Fragment#setRetainInstance(kotlin.Boolean)` instead; this is also available on older platforms through the Android support libraries.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#onSaveInstanceState(android.os.Bundle)(outState: https://developer.android.com/reference/kotlin/android/os/Bundle.html#)`

Called to retrieve per-instance state from an activity before being killed so that the state can be restored in #onCreate or #onRestoreInstanceState (the `https://developer.android.com/reference/kotlin/android/os/Bundle.html#` populated by this method will be passed to both).

This method is called before an activity may be killed so that when it comes back some time in the future it can restore its state. For example, if activity B is launched in front of activity A, and at some point activity A is killed to reclaim resources, activity A will have a chance to save the current state of its user interface via this method so that when the user returns to activity A, the state of the user interface can be restored via #onCreate or #onRestoreInstanceState.

Do not confuse this method with activity lifecycle callbacks such as `https://developer.android.com/reference/kotlin/android/app/Activity#onPause()`, which is always called when the user no longer actively interacts with an activity, or `https://developer.android.com/reference/kotlin/android/app/Activity#onStop()` which is called when activity becomes invisible. One example of when `https://developer.android.com/reference/kotlin/android/app/Activity#onPause()` and `https://developer.android.com/reference/kotlin/android/app/Activity#onStop()` is called and not this method is when a user navigates back from activity B to activity A: there is no need to call #onSaveInstanceState on B because that particular instance will never be restored, so the system avoids calling it. An example when `https://developer.android.com/reference/kotlin/android/app/Activity#onPause()` is called and not #onSaveInstanceState is when activity B is launched in front of activity A: the system may avoid calling #onSaveInstanceState on activity A if it isn't killed during the lifetime of B since the state of the user interface of A will stay intact.

The default implementation takes care of most of the UI per-instance state for you by calling `https://developer.android.com/reference/kotlin/android/view/View.html#onSaveInstanceState()` on each view in the hierarchy that has an id, and by saving the id of the currently focused view (all of which is restored by the default implementation of #onRestoreInstanceState). If you override this method to save additional information not captured by each individual view, you will likely want to call through to the default implementation, otherwise be prepared to save all of the state of each view yourself.

If called, this method will occur after `https://developer.android.com/reference/kotlin/android/app/Activity#onStop()` for applications targeting platforms starting with `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#P:kotlin.Int`. For applications targeting earlier platform versions this method will occur before `https://developer.android.com/reference/kotlin/android/app/Activity#onStop()` and there are no guarantees about whether it will occur before or after `https://developer.android.com/reference/kotlin/android/app/Activity#onPause()`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#onSaveInstanceState(android.os.Bundle,%20android.os.PersistableBundle)(outState: https://developer.android.com/reference/kotlin/android/os/Bundle.html#, outPersistentState: https://developer.android.com/reference/kotlin/android/os/PersistableBundle.html#)`

This is the same as #onSaveInstanceState but is called for activities created with the attribute `https://developer.android.com/reference/kotlin/android/R.attr.html#persistableMode:kotlin.Int` set to `persistAcrossReboots`. The `https://developer.android.com/reference/kotlin/android/os/PersistableBundle.html#` passed in will be saved and presented in `https://developer.android.com/reference/kotlin/android/app/Activity#onCreate(android.os.Bundle,%20android.os.PersistableBundle)` the first time that this activity is restarted following the next device reboot or after an update.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#onSearchRequested()()`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#onSearchRequested(android.view.SearchEvent)(searchEvent: https://developer.android.com/reference/kotlin/android/view/SearchEvent.html#?)`

This hook is called when the user signals the desire to start a search.

You can use this function as a simple way to launch the search UI, in response to a menu item, search button, or other widgets within your activity. Unless overridden, calling this function is the same as calling `https://developer.android.com/reference/kotlin/android/app/Activity#startSearch(kotlin.String,%20kotlin.Boolean,%20android.os.Bundle,%20kotlin.Boolean)`, which launches search for the current activity as specified in its manifest, see `https://developer.android.com/reference/kotlin/android/app/SearchManager`.

You can override this function to force global search, e.g. in response to a dedicated search key, or to block search entirely (by simply returning false).

Note: when running in a `https://developer.android.com/reference/kotlin/android/content/res/Configuration.html#UI_MODE_TYPE_TELEVISION:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/content/res/Configuration.html#UI_MODE_TYPE_WATCH:kotlin.Int`, the default implementation changes to simply return false and you must supply your own custom implementation if you want to support search.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#onStart()()`

Called after #onCreate --- or after `https://developer.android.com/reference/kotlin/android/app/Activity#onRestart()` when the activity had been stopped, but is now again being displayed to the user. It will usually be followed by `https://developer.android.com/reference/kotlin/android/app/Activity#onResume()`. This is a good place to begin drawing visual elements, running animations, etc.

You can call `https://developer.android.com/reference/kotlin/android/app/Activity#finish()` from within this function, in which case `https://developer.android.com/reference/kotlin/android/app/Activity#onStop()` will be immediately called after `https://developer.android.com/reference/kotlin/android/app/Activity#onStart()` without the lifecycle transitions in-between (`https://developer.android.com/reference/kotlin/android/app/Activity#onResume()`, `https://developer.android.com/reference/kotlin/android/app/Activity#onPause()`, etc.) executing.

*Derived classes must call through to the super class's implementation of this method. If they do not, an exception will be thrown.*
. 
If you override this method you *must* call through to the superclass implementation.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#onStateNotSaved()()`

Called when an `https://developer.android.com/reference/kotlin/android/app/Activity#onResume()` is coming up, prior to other pre-resume callbacks such as #onNewIntent and #onActivityResult. This is primarily intended to give the activity a hint that its state is no longer saved -- it will generally be called after #onSaveInstanceState and prior to the activity being resumed/started again.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#onStop()()`

Called when you are no longer visible to the user. You will next receive either `https://developer.android.com/reference/kotlin/android/app/Activity#onRestart()`, `https://developer.android.com/reference/kotlin/android/app/Activity#onDestroy()`, or nothing, depending on later user activity. This is a good place to stop refreshing UI, running animations and other visual things.

*Derived classes must call through to the super class's implementation of this method. If they do not, an exception will be thrown.*
. 
If you override this method you *must* call through to the superclass implementation.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#onTitleChanged(kotlin.CharSequence,%20kotlin.Int)(title: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!, color: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#onTopResumedActivityChanged(kotlin.Boolean)(isTopResumedActivity: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`

Called when activity gets or loses the top resumed position in the system.

Starting with `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#Q:kotlin.Int` multiple activities can be resumed at the same time in multi-window and multi-display modes. This callback should be used instead of `https://developer.android.com/reference/kotlin/android/app/Activity#onResume()` as an indication that the activity can try to open exclusive-access devices like camera.

It will always be delivered after the activity was resumed and before it is paused. In some cases it might be skipped and activity can go straight from `https://developer.android.com/reference/kotlin/android/app/Activity#onResume()` to `https://developer.android.com/reference/kotlin/android/app/Activity#onPause()` without receiving the top resumed state.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#onTouchEvent(android.view.MotionEvent)(event: https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#!)`

Called when a touch screen event was not handled by any of the views inside of the activity. This is most useful to process touch events that happen outside of your window bounds, where there is no view to receive it.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#onTrackballEvent(android.view.MotionEvent)(event: https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#!)`

Called when the trackball was moved and not handled by any of the views inside of the activity. So, for example, if the trackball moves while focus is on a button, you will receive a call here because buttons do not normally do anything with trackball events. The call here happens *before* trackball movements are converted to DPAD key events, which then get sent back to the view hierarchy, and will be processed at the point for things like focus navigation.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#onTrimMemory(kotlin.Int)(level: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Called when the operating system has determined that it is a good time for a process to trim unneeded memory from its process. You should never compare to exact values of the level, since new intermediate values may be added -- you will typically want to compare if the value is greater or equal to a level you are interested in.

To retrieve the processes current trim level at any point, you can use `https://developer.android.com/reference/kotlin/android/app/ActivityManager#getMyMemoryState(android.app.ActivityManager.RunningAppProcessInfo)`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#onUserInteraction()()`

Called whenever a key, touch, or trackball event is dispatched to the activity. Implement this method if you wish to know that the user has interacted with the device in some way while your activity is running. This callback and `https://developer.android.com/reference/kotlin/android/app/Activity#onUserLeaveHint()` are intended to help activities manage status bar notifications intelligently; specifically, for helping activities determine the proper time to cancel a notification.

All calls to your activity's `https://developer.android.com/reference/kotlin/android/app/Activity#onUserLeaveHint()` callback will be accompanied by calls to `https://developer.android.com/reference/kotlin/android/app/Activity#onUserInteraction()`. This ensures that your activity will be told of relevant user activity such as pulling down the notification pane and touching an item there.

Note that this callback will be invoked for the touch down action that begins a touch gesture, but may not be invoked for the touch-moved and touch-up actions that follow.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#onUserLeaveHint()()`

Called as part of the activity lifecycle when an activity is about to go into the background as the result of user choice. For example, when the user presses the Home key, `https://developer.android.com/reference/kotlin/android/app/Activity#onUserLeaveHint()` will be called, but when an incoming phone call causes the in-call Activity to be automatically brought to the foreground, `https://developer.android.com/reference/kotlin/android/app/Activity#onUserLeaveHint()` will not be called on the activity being interrupted. In cases when it is invoked, this method is called right before the activity's `https://developer.android.com/reference/kotlin/android/app/Activity#onPause()` callback.

This callback and `https://developer.android.com/reference/kotlin/android/app/Activity#onUserInteraction()` are intended to help activities manage status bar notifications intelligently; specifically, for helping activities determine the proper time to cancel a notification.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#onVisibleBehindCanceled()()`

Called when a translucent activity over this activity is becoming opaque or another activity is being launched. Activities that override this method must call `super.onVisibleBehindCanceled()` or a SuperNotCalledException will be thrown.

When this method is called the activity has 500 msec to release any resources it may be using while visible in the background. If the activity has not returned from this method in 500 msec the system will destroy the activity and kill the process in order to recover the resources for another process. Otherwise `https://developer.android.com/reference/kotlin/android/app/Activity#onStop()` will be called following return. 
If you override this method you *must* call through to the superclass implementation.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#onWindowAttributesChanged(android.view.WindowManager.LayoutParams)(params: https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#!)`

This is called whenever the current window attributes change.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#onWindowFocusChanged(kotlin.Boolean)(hasFocus: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`

Called when the current `https://developer.android.com/reference/kotlin/android/view/Window.html#` of the activity gains or loses focus. This is the best indicator of whether this activity is the entity with which the user actively interacts. The default implementation clears the key tracking state, so should always be called.

Note that this provides information about global focus state, which is managed independently of activity lifecycle. As such, while focus changes will generally have some relation to lifecycle changes (an activity that is stopped will not generally get window focus), you should not rely on any particular order between the callbacks here and those in the other lifecycle methods such as `https://developer.android.com/reference/kotlin/android/app/Activity#onResume()`.

As a general rule, however, a foreground activity will have window focus... unless it has displayed other dialogs or popups that take input focus, in which case the activity itself will not have focus when the other windows have it. Likewise, the system may display system-level windows (such as the status bar notification panel or a system alert) which will temporarily take window input focus without pausing the foreground activity.

Starting with `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#Q:kotlin.Int` there can be multiple resumed activities at the same time in multi-window mode, so resumed state does not guarantee window focus even if there are no overlays above.

If the intent is to know when an activity is the topmost active, the one the user interacted with last among all activities but not including non-activity windows like dialogs and popups, then `https://developer.android.com/reference/kotlin/android/app/Activity#onTopResumedActivityChanged(kotlin.Boolean)` should be used. On platform versions prior to `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#Q:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/app/Activity#onResume()` is the best indicator.

<br />

`https://developer.android.com/reference/kotlin/android/view/ActionMode.html#?` `https://developer.android.com/reference/kotlin/android/app/Activity#onWindowStartingActionMode(android.view.ActionMode.Callback)(callback: https://developer.android.com/reference/kotlin/android/view/ActionMode.Callback.html#!)`

Give the Activity a chance to control the UI for an action mode requested by the system.

Note: If you are looking for a notification callback that an action mode has been started for this activity, see `https://developer.android.com/reference/kotlin/android/app/Activity#onActionModeStarted(android.view.ActionMode)`.

<br />

`https://developer.android.com/reference/kotlin/android/view/ActionMode.html#?` `https://developer.android.com/reference/kotlin/android/app/Activity#onWindowStartingActionMode(android.view.ActionMode.Callback,%20kotlin.Int)(callback: https://developer.android.com/reference/kotlin/android/view/ActionMode.Callback.html#!, type: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Called when an action mode is being started for this window. Gives the callback an opportunity to handle the action mode in its own unique and beautiful way. If this method returns null the system can choose a way to present the mode or choose not to start the mode at all.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#openContextMenu(android.view.View)(view: https://developer.android.com/reference/kotlin/android/view/View.html#!)`

Programmatically opens the context menu for a particular `view`. The `view` should have been added via `https://developer.android.com/reference/kotlin/android/app/Activity#registerForContextMenu(android.view.View)`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#openOptionsMenu()()`

Programmatically opens the options menu. If the options menu is already open, this method does nothing.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#overrideActivityTransition(kotlin.Int,%20kotlin.Int,%20kotlin.Int)(overrideType: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, enterAnim: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, exitAnim: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Customizes the animation for activity transitions.

This method provides a robust way to override transition animations at runtime and can be called at any point in the activity's lifecycle. It is particularly useful for handling predictive back animations, for which `https://developer.android.com/reference/kotlin/android/app/Activity#overridePendingTransition(kotlin.Int,%20kotlin.Int)` is not suitable.

The specified animations will be applied only when this activity is at the top of the task stack during the transition. For example, to customize the opening animation for an Activity B started from Activity A, call this method in B's `onCreate` with `overrideType = OVERRIDE_TRANSITION_OPEN`. To customize the closing animation when returning from B to A, call this method in B with `overrideType = OVERRIDE_TRANSITION_CLOSE`.

**Animation Precedence:**

- Animations set by `https://developer.android.com/reference/kotlin/android/app/Activity#overridePendingTransition(kotlin.Int,%20kotlin.Int)` have the highest priority.
- Animations set by this method have higher priority than those defined by `https://developer.android.com/reference/kotlin/android/view/Window.html#setWindowAnimations(kotlin.Int)`.

**Predictive Back Animation:**

When predictive back is enabled (see `enableOnBackInvokedCallback` in the manifest), the system may control the preview phase of the back animation. The custom transition defined by `enterAnim` and `exitAnim` is then applied only after the back gesture is committed.

**Limitations:**

- This method, along with `https://developer.android.com/reference/kotlin/android/app/Activity#overridePendingTransition(kotlin.Int,%20kotlin.Int)` and `https://developer.android.com/reference/kotlin/android/view/Window.html#setWindowAnimations(kotlin.Int)`, is ignored if the activity is started with `https://developer.android.com/reference/kotlin/android/app/ActivityOptions#makeSceneTransitionAnimation(android.app.Activity,%20android.util.Pair)`.
- As of Android 11, this method cannot be used to customize cross-task transitions.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#overrideActivityTransition(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)(overrideType: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, enterAnim: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, exitAnim: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, backgroundColor: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Customizes the animation and background color for activity transitions.

This method provides a robust way to override transition animations at runtime and can be called at any point in the activity's lifecycle. It is particularly useful for handling predictive back animations, for which `https://developer.android.com/reference/kotlin/android/app/Activity#overridePendingTransition(kotlin.Int,%20kotlin.Int)` is not suitable.

The specified animations will be applied only when this activity is at the top of the task stack during the transition. For example, to customize the opening animation for an Activity B started from Activity A, call this method in B's `onCreate` with `overrideType = OVERRIDE_TRANSITION_OPEN`. To customize the closing animation when returning from B to A, call this method in B with `overrideType = OVERRIDE_TRANSITION_CLOSE`.

**Animation Precedence:**

- Animations set by `https://developer.android.com/reference/kotlin/android/app/Activity#overridePendingTransition(kotlin.Int,%20kotlin.Int)` have the highest priority.
- Animations set by this method have higher priority than those defined by `https://developer.android.com/reference/kotlin/android/view/Window.html#setWindowAnimations(kotlin.Int)`.

**Predictive Back Animation:**

When predictive back is enabled (see `enableOnBackInvokedCallback` in the manifest), the system may control the preview phase of the back animation. The custom transition defined by `enterAnim` and `exitAnim` is then applied only after the back gesture is committed.

**Limitations:**

- This method, along with `https://developer.android.com/reference/kotlin/android/app/Activity#overridePendingTransition(kotlin.Int,%20kotlin.Int)` and `https://developer.android.com/reference/kotlin/android/view/Window.html#setWindowAnimations(kotlin.Int)`, is ignored if the activity is started with `https://developer.android.com/reference/kotlin/android/app/ActivityOptions#makeSceneTransitionAnimation(android.app.Activity,%20android.util.Pair)`.
- As of Android 11, this method cannot be used to customize cross-task transitions.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#overridePendingTransition(kotlin.Int,%20kotlin.Int)(enterAnim: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, exitAnim: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Call immediately after one of the flavors of #startActivity(android.content.Intent) or `https://developer.android.com/reference/kotlin/android/app/Activity#finish()` to specify an explicit transition animation to perform next.

As of `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#JELLY_BEAN:kotlin.Int` an alternative to using this with starting activities is to supply the desired animation information through a `https://developer.android.com/reference/kotlin/android/app/ActivityOptions` bundle to #startActivity(android.content.Intent,android.os.Bundle) or a related function. This allows you to specify a custom animation even when starting an activity from outside the context of the current top activity.

Af of `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` application can only specify a transition animation when the transition happens within the same task. System default animation is used for cross-task transition animations.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#overridePendingTransition(kotlin.Int,%20kotlin.Int,%20kotlin.Int)(enterAnim: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, exitAnim: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, backgroundColor: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Call immediately after one of the flavors of #startActivity(android.content.Intent) or `https://developer.android.com/reference/kotlin/android/app/Activity#finish()` to specify an explicit transition animation to perform next.

As of `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#JELLY_BEAN:kotlin.Int` an alternative to using this with starting activities is to supply the desired animation information through a `https://developer.android.com/reference/kotlin/android/app/ActivityOptions` bundle to #startActivity(android.content.Intent,android.os.Bundle) or a related function. This allows you to specify a custom animation even when starting an activity from outside the context of the current top activity.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#postponeEnterTransition()()`

Postpone the entering activity transition when Activity was started with `https://developer.android.com/reference/kotlin/android/app/ActivityOptions#makeSceneTransitionAnimation(android.app.Activity,%20android.util.Pair)`.

This method gives the Activity the ability to delay starting the entering and shared element transitions until all data is loaded. Until then, the Activity won't draw into its window, leaving the window transparent. This may also cause the returning animation to be delayed until data is ready. This method should be called in `https://developer.android.com/reference/kotlin/android/app/Activity#onCreate(android.os.Bundle)` or in `https://developer.android.com/reference/kotlin/android/app/Activity#onActivityReenter(kotlin.Int,%20android.content.Intent)`. `https://developer.android.com/reference/kotlin/android/app/Activity#startPostponedEnterTransition()` must be called to allow the Activity to start the transitions. If the Activity did not use `https://developer.android.com/reference/kotlin/android/app/ActivityOptions#makeSceneTransitionAnimation(android.app.Activity,%20android.util.Pair)`, then this method does nothing.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#recreate()()`

Cause this Activity to be recreated with a new instance. This results in essentially the same flow as when the Activity is created due to a configuration change -- the current instance will go through its lifecycle to `https://developer.android.com/reference/kotlin/android/app/Activity#onDestroy()` and a new instance then created after it.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#registerActivityLifecycleCallbacks(android.app.Application.ActivityLifecycleCallbacks)(callback: https://developer.android.com/reference/kotlin/android/app/Application.ActivityLifecycleCallbacks)`

Register an `https://developer.android.com/reference/kotlin/android/app/Application.ActivityLifecycleCallbacks` instance that receives lifecycle callbacks for only this Activity.

In relation to any `https://developer.android.com/reference/kotlin/android/app/Application#registerActivityLifecycleCallbacks(android.app.Application.ActivityLifecycleCallbacks)`, the callbacks registered here will always occur nested within those callbacks. This means:

- Pre events will first be sent to Application registered callbacks, then to callbacks registered here.
- `https://developer.android.com/reference/kotlin/android/app/Application.ActivityLifecycleCallbacks#onActivityCreated(android.app.Activity,%20android.os.Bundle)`, `https://developer.android.com/reference/kotlin/android/app/Application.ActivityLifecycleCallbacks#onActivityStarted(android.app.Activity)`, and `https://developer.android.com/reference/kotlin/android/app/Application.ActivityLifecycleCallbacks#onActivityResumed(android.app.Activity)` will be sent first to Application registered callbacks, then to callbacks registered here. For all other events, callbacks registered here will be sent first.
- Post events will first be sent to callbacks registered here, then to Application registered callbacks.

If multiple callbacks are registered here, they receive events in a first in (up through `https://developer.android.com/reference/kotlin/android/app/Application.ActivityLifecycleCallbacks#onActivityPostResumed(android.app.Activity)`, last out ordering.

It is strongly recommended to register this in the constructor of your Activity to ensure you get all available callbacks. As this callback is associated with only this Activity, it is not usually necessary to `https://developer.android.com/reference/kotlin/android/app/Activity#unregisterActivityLifecycleCallbacks(android.app.Application.ActivityLifecycleCallbacks)` it unless you specifically do not want to receive further lifecycle callbacks.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#registerComponentCallbacks(android.content.ComponentCallbacks)(callback: https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks.html#!)`

Add a new `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks.html#` to the base application of the Context, which will be called at the same times as the ComponentCallbacks methods of activities and other components are called. Note that you *must* be sure to use `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#unregisterComponentCallbacks(android.content.ComponentCallbacks)` when appropriate in the future; this will not be removed for you.

After `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#TIRAMISU:kotlin.Int`, the `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks.html#` will be registered to `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#getBaseContext()`, and can be only used after `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#attachBaseContext(android.content.Context)`. Users can still call to `getApplicationContext().registerComponentCallbacks(ComponentCallbacks)` to add `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks.html#` to the base application.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#registerForContextMenu(android.view.View)(view: https://developer.android.com/reference/kotlin/android/view/View.html#!)`

Registers a context menu to be shown for the given view (multiple views can show the context menu). This method will set the `https://developer.android.com/reference/kotlin/android/view/View.OnCreateContextMenuListener.html#` on the view to this activity, so `https://developer.android.com/reference/kotlin/android/app/Activity#onCreateContextMenu(android.view.ContextMenu,%20android.view.View,%20android.view.ContextMenu.ContextMenuInfo)` will be called when it is time to show the context menu.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#registerScreenCaptureCallback(java.util.concurrent.Executor,%20android.app.Activity.ScreenCaptureCallback)(executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, callback: https://developer.android.com/reference/kotlin/android/app/Activity.ScreenCaptureCallback)`

Registers a screen capture callback for this activity. The callback will be triggered when a screen capture of this activity is attempted. This callback will be executed on the thread of the passed `executor`. For details, see `https://developer.android.com/reference/kotlin/android/app/Activity.ScreenCaptureCallback#onScreenCaptured()`. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#DETECT_SCREEN_CAPTURE:kotlin.String`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#releaseInstance()()`

Ask that the local app instance of this activity be released to free up its memory. This is asking for the activity to be destroyed, but does **not** finish the activity -- a new instance of the activity will later be re-created if needed due to the user navigating back to it.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#removeDialog(kotlin.Int)(id: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Removes any internal references to a dialog managed by this Activity. If the dialog is showing, it will dismiss it as part of the clean up.

This can be useful if you know that you will never show a dialog again and want to avoid the overhead of saving and restoring it in the future.

As of `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#GINGERBREAD:kotlin.Int`, this function will not throw an exception if you try to remove an ID that does not currently have an associated dialog.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#reportFullyDrawn()()`

Report to the system that your app is now fully drawn, for diagnostic and optimization purposes. The system may adjust optimizations to prioritize work that happens before reportFullyDrawn is called, to improve app startup. Misrepresenting the startup window by calling reportFullyDrawn too late or too early may decrease application and startup performance.

This is also used to help instrument application launch times, so that the app can report when it is fully in a usable state; without this, the only thing the system itself can determine is the point at which the activity's window is *first* drawn and displayed. To participate in app launch time measurement, you should always call this method after first launch (when `https://developer.android.com/reference/kotlin/android/app/Activity#onCreate(android.os.Bundle)` is called), at the point where you have entirely drawn your UI and populated with all of the significant data. You can safely call this method any time after first launch as well, in which case it will simply be ignored.

If this method is called before the activity's window is *first* drawn and displayed as measured by the system, the reported time here will be shifted to the system measured time.

<br />

`https://developer.android.com/reference/kotlin/android/view/DragAndDropPermissions.html#!` `https://developer.android.com/reference/kotlin/android/app/Activity#requestDragAndDropPermissions(android.view.DragEvent)(event: https://developer.android.com/reference/kotlin/android/view/DragEvent.html#!)`

Create `https://developer.android.com/reference/kotlin/android/view/DragAndDropPermissions.html#` object bound to this activity and controlling the access permissions for content URIs associated with the `https://developer.android.com/reference/kotlin/android/view/DragEvent.html#`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#requestFullscreenMode(kotlin.Int,%20android.os.OutcomeReceiver)(request: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, approvalCallback: https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#<https://developer.android.com/reference/kotlin/java/lang/Void.html#!, https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html!>?)`

Request to put the activity into fullscreen. The requester must be pinned or the top-most activity of the focused display which can be verified using `https://developer.android.com/reference/kotlin/android/app/Activity#onTopResumedActivityChanged(kotlin.Boolean)`. The request should also be a response to a user input. When getting fullscreen and receiving corresponding `https://developer.android.com/reference/kotlin/android/app/Activity#onConfigurationChanged(android.content.res.Configuration)` and `https://developer.android.com/reference/kotlin/android/app/Activity#onMultiWindowModeChanged(kotlin.Boolean,%20android.content.res.Configuration)`, the activity should relayout itself and the system bars' visibilities can be controlled as usual fullscreen apps. Calling it again with the exit request can restore the activity to the previous status. This will only happen when it got into fullscreen through this API.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#requestOpenInBrowserEducation()()`

Requests to show the "Open in browser" education. "Open in browser" is a feature within the app header that allows users to switch from an app to the web. The feature is made available when an application is opened by a user clicking a link or when a link is provided by an application. Links can be provided by calling `https://developer.android.com/reference/kotlin/android/app/assist/AssistContent#setSessionTransferUri(android.net.Uri)` or `https://developer.android.com/reference/kotlin/android/app/assist/AssistContent#setWebUri(android.net.Uri)`.

This method should be utilized when an activity wants to nudge the user to switch to the web application in cases where the web may provide the user with a better experience. Note that this method does not guarantee that the education will be shown.

The number of times that the "Open in browser" education can be triggered by this method is limited per application, and, when shown, the education appears above the app's content. For these reasons, developers should use this method sparingly when it is least disruptive to the user to show the education and when it is optimal to switch the user to a browser session. Before requesting to show the education, developers should assert that they have set a link that can be used by the "Open in browser" feature through either `https://developer.android.com/reference/kotlin/android/app/assist/AssistContent#setSessionTransferUri(android.net.Uri)` or `https://developer.android.com/reference/kotlin/android/app/assist/AssistContent#setWebUri(android.net.Uri)` so that users are navigated to a relevant page if they choose to switch to the browser. If a URI is not set using either method, "Open in browser" will utilize a generic link if available which will direct users to the homepage of the site associated with the app. The generic link is provided for a limited number of applications by the system and cannot be edited by developers. If none of these options contains a valid URI, the user will not be provided with the option to switch to the browser and the education will not be shown if requested.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#requestPermissions(kotlin.Array,%20kotlin.Int)(permissions: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>, requestCode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Requests permissions to be granted to this application. These permissions must be requested in your manifest, they should not be granted to your app, and they should have protection level `https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo.html#PROTECTION_DANGEROUS:kotlin.Int`, regardless whether they are declared by the platform or a third-party app.

Normal permissions `https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo.html#PROTECTION_NORMAL:kotlin.Int` are granted at install time if requested in the manifest. Signature permissions `https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo.html#PROTECTION_SIGNATURE:kotlin.Int` are granted at install time if requested in the manifest and the signature of your app matches the signature of the app declaring the permissions.

Call #shouldShowRequestPermissionRationale before calling this API to check if the system recommends to show a rationale UI before asking for a permission.

If your app does not have the requested permissions the user will be presented with UI for accepting them. After the user has accepted or rejected the requested permissions you will receive a callback on #onRequestPermissionsResult reporting whether the permissions were granted or not.

Note that requesting a permission does not guarantee it will be granted and your app should be able to run without having this permission.

This method may start an activity allowing the user to choose which permissions to grant and which to reject. Hence, you should be prepared that your activity may be paused and resumed. Further, granting some permissions may require a restart of you application. In such a case, the system will recreate the activity stack before delivering the result to #onRequestPermissionsResult.

When checking whether you have a permission you should use `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#checkSelfPermission(kotlin.String)`.

You cannot request a permission if your activity sets `https://developer.android.com/reference/kotlin/android/R.styleable.html#AndroidManifestActivity_noHistory:kotlin.Int` to `true` because in this case the activity would not receive result callbacks including #onRequestPermissionsResult.

The [permissions samples](https://github.com/android/platform-samples/tree/main/samples/privacy/permissions) repo demonstrates how to use this method to request permissions at run time.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#requestPermissions(kotlin.Array,%20kotlin.Int,%20kotlin.Int)(permissions: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>, requestCode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, deviceId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Requests permissions to be granted to this application. These permissions must be requested in your manifest, they should not be granted to your app, and they should have protection level `https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo.html#PROTECTION_DANGEROUS:kotlin.Int`, regardless whether they are declared by the platform or a third-party app.

Normal permissions `https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo.html#PROTECTION_NORMAL:kotlin.Int` are granted at install time if requested in the manifest. Signature permissions `https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo.html#PROTECTION_SIGNATURE:kotlin.Int` are granted at install time if requested in the manifest and the signature of your app matches the signature of the app declaring the permissions.

Call #shouldShowRequestPermissionRationale before calling this API to check if the system recommends to show a rationale UI before asking for a permission.

If your app does not have the requested permissions the user will be presented with UI for accepting them. After the user has accepted or rejected the requested permissions you will receive a callback on #onRequestPermissionsResult reporting whether the permissions were granted or not.

Note that requesting a permission does not guarantee it will be granted and your app should be able to run without having this permission.

This method may start an activity allowing the user to choose which permissions to grant and which to reject. Hence, you should be prepared that your activity may be paused and resumed. Further, granting some permissions may require a restart of you application. In such a case, the system will recreate the activity stack before delivering the result to #onRequestPermissionsResult.

When checking whether you have a permission you should use `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#checkSelfPermission(kotlin.String)`.

You cannot request a permission if your activity sets `https://developer.android.com/reference/kotlin/android/R.styleable.html#AndroidManifestActivity_noHistory:kotlin.Int` to `true` because in this case the activity would not receive result callbacks including #onRequestPermissionsResult.

The [permissions samples](https://github.com/android/platform-samples/tree/main/samples/privacy/permissions) repo demonstrates how to use this method to request permissions at run time.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#requestShowKeyboardShortcuts()()`

Request the Keyboard Shortcuts screen to show up. This will trigger `https://developer.android.com/reference/kotlin/android/app/Activity#onProvideKeyboardShortcuts(kotlin.collections.MutableList,%20android.view.Menu,%20kotlin.Int)` to retrieve the shortcuts for the foreground activity.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#requestVisibleBehind(kotlin.Boolean)(visible: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`

Activities that want to remain visible behind a translucent activity above them must call this method anytime between the start of `https://developer.android.com/reference/kotlin/android/app/Activity#onResume()` and the return from `https://developer.android.com/reference/kotlin/android/app/Activity#onPause()`. If this call is successful then the activity will remain visible after `https://developer.android.com/reference/kotlin/android/app/Activity#onPause()` is called, and is allowed to continue playing media in the background.

The actions of this call are reset each time that this activity is brought to the front. That is, every time `https://developer.android.com/reference/kotlin/android/app/Activity#onResume()` is called the activity will be assumed to not have requested visible behind. Therefore, if you want this activity to continue to be visible in the background you must call this method again.

Only fullscreen opaque activities may make this call. I.e. this call is a nop for dialog and translucent activities.

Under all circumstances, the activity must stop playing and release resources prior to or within a call to `https://developer.android.com/reference/kotlin/android/app/Activity#onVisibleBehindCanceled()` or if this call returns false.

False will be returned any time this method is called between the return of onPause and the next call to onResume.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#requestWindowFeature(kotlin.Int)(featureId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Enable extended window features. This is a convenience for calling `https://developer.android.com/reference/kotlin/android/view/Window.html#requestFeature(kotlin.Int)`.

<br />

`T` `https://developer.android.com/reference/kotlin/android/app/Activity#requireViewById(kotlin.Int)(id: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Finds a view that was identified by the `android:id` XML attribute that was processed in #onCreate, or throws an IllegalArgumentException if the ID is invalid, or there is no matching view in the hierarchy.

**Note:** In most cases -- depending on compiler support -- the resulting view is automatically cast to the target class type. If the target class type is unconstrained, an explicit cast may be necessary.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#runOnUiThread(java.lang.Runnable)(action: https://developer.android.com/reference/kotlin/java/lang/Runnable.html#!)`

Runs the specified action on the UI thread. If the current thread is the UI thread, then the action is executed immediately. If the current thread is not the UI thread, the action is posted to the event queue of the UI thread.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#setActionBar(android.widget.Toolbar)(toolbar: https://developer.android.com/reference/kotlin/android/widget/Toolbar.html#?)`

Set a `https://developer.android.com/reference/kotlin/android/widget/Toolbar.html#` to act as the `https://developer.android.com/reference/kotlin/android/app/ActionBar` for this Activity window.

When set to a non-null value the `https://developer.android.com/reference/kotlin/android/app/Activity#getActionBar()` method will return an `https://developer.android.com/reference/kotlin/android/app/ActionBar` object that can be used to control the given toolbar as if it were a traditional window decor action bar. The toolbar's menu will be populated with the Activity's options menu and the navigation button will be wired through the standard `https://developer.android.com/reference/kotlin/android/R.id.html#home:kotlin.Int` menu select action.

In order to use a Toolbar within the Activity's window content the application must not request the window feature `https://developer.android.com/reference/kotlin/android/view/Window.html#FEATURE_ACTION_BAR:kotlin.Int`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#setAllowCrossUidActivitySwitchFromBelow(kotlin.Boolean)(allowed: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`

Specifies whether the activities below this one in the task can also start other activities or finish the task.

Starting from Target SDK Level `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#VANILLA_ICE_CREAM:kotlin.Int`, apps may be blocked from starting new activities or finishing their task unless the top activity of such task belong to the same UID for security reasons.

Setting this flag to `true` will allow the launching app to ignore the restriction if this activity is on top. Apps matching the UID of this activity are always exempt.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#setContentTransitionManager(android.transition.TransitionManager)(tm: https://developer.android.com/reference/kotlin/android/transition/TransitionManager.html#!)`

Set the `https://developer.android.com/reference/kotlin/android/transition/TransitionManager.html#` to use for default transitions in this window. Requires `https://developer.android.com/reference/kotlin/android/view/Window.html#FEATURE_CONTENT_TRANSITIONS:kotlin.Int`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#setContentView(android.view.View)(view: https://developer.android.com/reference/kotlin/android/view/View.html#!)`

Set the activity content to an explicit view. This view is placed directly into the activity's view hierarchy. It can itself be a complex view hierarchy. When calling this method, the layout parameters of the specified view are ignored. Both the width and the height of the view are set by default to `https://developer.android.com/reference/kotlin/android/view/ViewGroup.LayoutParams.html#MATCH_PARENT:kotlin.Int`. To use your own layout parameters, invoke `https://developer.android.com/reference/kotlin/android/app/Activity#setContentView(android.view.View,%20android.view.ViewGroup.LayoutParams)` instead.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#setContentView(android.view.View,%20android.view.ViewGroup.LayoutParams)(view: https://developer.android.com/reference/kotlin/android/view/View.html#!, params: https://developer.android.com/reference/kotlin/android/view/ViewGroup.LayoutParams.html#!)`

Set the activity content to an explicit view. This view is placed directly into the activity's view hierarchy. It can itself be a complex view hierarchy.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#setContentView(kotlin.Int)(layoutResID: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Set the activity content from a layout resource. The resource will be inflated, adding all top-level views to the activity.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#setDefaultKeyMode(kotlin.Int)(mode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Select the default key handling for this activity. This controls what will happen to key events that are not otherwise handled. The default mode (`https://developer.android.com/reference/kotlin/android/app/Activity#DEFAULT_KEYS_DISABLE:kotlin.Int`) will simply drop them on the floor. Other modes allow you to launch the dialer (`https://developer.android.com/reference/kotlin/android/app/Activity#DEFAULT_KEYS_DIALER:kotlin.Int`), execute a shortcut in your options menu without requiring the menu key be held down (`https://developer.android.com/reference/kotlin/android/app/Activity#DEFAULT_KEYS_SHORTCUT:kotlin.Int`), or launch a search (`https://developer.android.com/reference/kotlin/android/app/Activity#DEFAULT_KEYS_SEARCH_LOCAL:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/app/Activity#DEFAULT_KEYS_SEARCH_GLOBAL:kotlin.Int`).

Note that the mode selected here does not impact the default handling of system keys, such as the "back" and "menu" keys, and your activity and its views always get a first chance to receive and handle all application keys.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#setEnterSharedElementCallback(android.app.SharedElementCallback)(callback: https://developer.android.com/reference/kotlin/android/app/SharedElementCallback!)`

When `https://developer.android.com/reference/kotlin/android/app/ActivityOptions#makeSceneTransitionAnimation(android.app.Activity,%20android.view.View,%20kotlin.String)` was used to start an Activity, callback will be called to handle shared elements on the *launched* Activity. This requires `https://developer.android.com/reference/kotlin/android/view/Window.html#FEATURE_ACTIVITY_TRANSITIONS:kotlin.Int`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#setExitSharedElementCallback(android.app.SharedElementCallback)(callback: https://developer.android.com/reference/kotlin/android/app/SharedElementCallback!)`

When `https://developer.android.com/reference/kotlin/android/app/ActivityOptions#makeSceneTransitionAnimation(android.app.Activity,%20android.view.View,%20kotlin.String)` was used to start an Activity, callback will be called to handle shared elements on the *launching* Activity. Most calls will only come when returning from the started Activity. This requires `https://developer.android.com/reference/kotlin/android/view/Window.html#FEATURE_ACTIVITY_TRANSITIONS:kotlin.Int`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#setFeatureDrawable(kotlin.Int,%20android.graphics.drawable.Drawable)(featureId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, drawable: https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#!)`

Convenience for calling `https://developer.android.com/reference/kotlin/android/view/Window.html#setFeatureDrawable(kotlin.Int,%20android.graphics.drawable.Drawable)`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#setFeatureDrawableAlpha(kotlin.Int,%20kotlin.Int)(featureId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, alpha: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Convenience for calling `https://developer.android.com/reference/kotlin/android/view/Window.html#setFeatureDrawableAlpha(kotlin.Int,%20kotlin.Int)`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#setFeatureDrawableResource(kotlin.Int,%20kotlin.Int)(featureId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, resId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Convenience for calling `https://developer.android.com/reference/kotlin/android/view/Window.html#setFeatureDrawableResource(kotlin.Int,%20kotlin.Int)`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#setFeatureDrawableUri(kotlin.Int,%20android.net.Uri)(featureId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#!)`

Convenience for calling `https://developer.android.com/reference/kotlin/android/view/Window.html#setFeatureDrawableUri(kotlin.Int,%20android.net.Uri)`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#setFinishOnTouchOutside(kotlin.Boolean)(finish: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`

Sets whether this activity is finished when touched outside its window's bounds.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#setHandoffEnabled(kotlin.Boolean,%20android.app.HandoffActivityParams)(handoffEnabled: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html, handoffActivityParams: https://developer.android.com/reference/kotlin/android/app/HandoffActivityParams?)`

Sets if Handoff is enabled for this Activity. See `https://developer.android.com/reference/kotlin/android/app/Activity#isHandoffEnabled()` to get if Handoff is currently enabled on this Activity. If Handoff is enabled, this Activity will only be eligible to be handed off to other devices if it is the topmost Activity in its Task. Callers may specify optional parameters to specify when Handoff is appropriate for the current activity. See `https://developer.android.com/reference/kotlin/android/app/HandoffActivityParams` for more details.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#setImmersive(kotlin.Boolean)(i: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`

Adjust the current immersive mode setting. Note that changing this value will have no effect on the activity's `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#` structure; that is, if `android:immersive` is set to `true` in the application's manifest entry for this activity, the `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#flags:kotlin.Int` member will always have its `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#FLAG_IMMERSIVE:kotlin.Int` bit set.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#setInheritShowWhenLocked(kotlin.Boolean)(inheritShowWhenLocked: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`

Specifies whether this `https://developer.android.com/reference/kotlin/android/app/Activity` should be shown on top of the lock screen whenever the lockscreen is up and this activity has another activity behind it with the showWhenLock attribute set. That is, this activity is only visible on the lock screen if there is another activity with the showWhenLock attribute visible at the same time on the lock screen. A use case for this is permission dialogs, that should only be visible on the lock screen if their requesting activity is also visible. This value can be set as a manifest attribute using android.R.attr#inheritShowWhenLocked.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#setIntent(android.content.Intent)(newIntent: https://developer.android.com/reference/kotlin/android/content/Intent.html#!)`

Changes the intent returned by `https://developer.android.com/reference/kotlin/android/app/Activity#getIntent()`. This holds a reference to the given intent; it does not copy it. Often used in conjunction with `https://developer.android.com/reference/kotlin/android/app/Activity#onNewIntent(android.content.Intent)`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#setIntent(android.content.Intent,%20android.app.ComponentCaller)(newIntent: https://developer.android.com/reference/kotlin/android/content/Intent.html#?, newCaller: https://developer.android.com/reference/kotlin/android/app/ComponentCaller?)`

Changes the intent returned by `https://developer.android.com/reference/kotlin/android/app/Activity#getIntent()`, and ComponentCaller returned by `https://developer.android.com/reference/kotlin/android/app/Activity#getCaller()`. This holds references to the given intent, and ComponentCaller; it does not copy them. Often used in conjunction with `https://developer.android.com/reference/kotlin/android/app/Activity#onNewIntent(android.content.Intent)`. To retrieve the caller from `https://developer.android.com/reference/kotlin/android/app/Activity#onNewIntent(android.content.Intent)`, use `https://developer.android.com/reference/kotlin/android/app/Activity#getCurrentCaller()`, otherwise override `https://developer.android.com/reference/kotlin/android/app/Activity#onNewIntent(android.content.Intent,%20android.app.ComponentCaller)`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#setLocusContext(android.content.LocusId,%20android.os.Bundle)(locusId: https://developer.android.com/reference/kotlin/android/content/LocusId.html#?, bundle: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?)`

Sets the `https://developer.android.com/reference/kotlin/android/content/LocusId.html#` for this activity. The locus id helps identify different instances of the same `Activity` class.

For example, a locus id based on a specific conversation could be set on a conversation app's chat `Activity`. The system can then use this locus id along with app's contents to provide ranking signals in various UI surfaces including sharing, notifications, shortcuts and so on.

It is recommended to set the same locus id in the shortcut's locus id using `https://developer.android.com/reference/kotlin/android/content/pm/ShortcutInfo.Builder.html#setLocusId(android.content.LocusId)` so that the system can learn appropriate ranking signals linking the activity's locus id with the matching shortcut.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#setMediaController(android.media.session.MediaController)(controller: https://developer.android.com/reference/kotlin/android/media/session/MediaController.html#!)`

Sets a `https://developer.android.com/reference/kotlin/android/media/session/MediaController.html#` to send media keys and volume changes to.

The controller will be tied to the window of this Activity. Media key and volume events which are received while the Activity is in the foreground will be forwarded to the controller and used to invoke transport controls or adjust the volume. This may be used instead of or in addition to `https://developer.android.com/reference/kotlin/android/app/Activity#setVolumeControlStream(kotlin.Int)` to affect a specific session instead of a specific stream.

It is not guaranteed that the hardware volume controls will always change this session's volume (for example, if a call is in progress, its stream's volume may be changed instead). To reset back to the default use null as the controller.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#setPictureInPictureParams(android.app.PictureInPictureParams)(params: https://developer.android.com/reference/kotlin/android/app/PictureInPictureParams)`

Updates the properties of the picture-in-picture activity, or sets it to be used later when `https://developer.android.com/reference/kotlin/android/app/Activity#enterPictureInPictureMode()` is called.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#setProgress(kotlin.Int)(progress: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Sets the progress for the progress bars in the title.

In order for the progress bar to be shown, the feature must be requested via `https://developer.android.com/reference/kotlin/android/app/Activity#requestWindowFeature(kotlin.Int)`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#setProgressBarIndeterminate(kotlin.Boolean)(indeterminate: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`

Sets whether the horizontal progress bar in the title should be indeterminate (the circular is always indeterminate).

In order for the progress bar to be shown, the feature must be requested via `https://developer.android.com/reference/kotlin/android/app/Activity#requestWindowFeature(kotlin.Int)`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#setProgressBarIndeterminateVisibility(kotlin.Boolean)(visible: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`

Sets the visibility of the indeterminate progress bar in the title.

In order for the progress bar to be shown, the feature must be requested via `https://developer.android.com/reference/kotlin/android/app/Activity#requestWindowFeature(kotlin.Int)`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#setProgressBarVisibility(kotlin.Boolean)(visible: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`

Sets the visibility of the progress bar in the title.

In order for the progress bar to be shown, the feature must be requested via `https://developer.android.com/reference/kotlin/android/app/Activity#requestWindowFeature(kotlin.Int)`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#setRecentsScreenshotEnabled(kotlin.Boolean)(enabled: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`

If set to false, this indicates to the system that it should never take a screenshot of the activity to be used as a representation in recents screen. By default, this value is `true`.

Note that the system may use the window background of the theme instead to represent the window when it is not running.

Also note that in comparison to `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#FLAG_SECURE:kotlin.Int`, this only affects the behavior when the activity's screenshot would be used as a representation when the activity is not in a started state, i.e. in Overview. The system may still take screenshots of the activity in other contexts; for example, when the user takes a screenshot of the entire screen, or when the active `https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionService.html#` requests a screenshot via `https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession.html#SHOW_WITH_SCREENSHOT:kotlin.Int`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#setRequestedOrientation(kotlin.Int)(requestedOrientation: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Change the desired orientation of this activity. If the activity is currently in the foreground or otherwise impacting the screen orientation, the screen is immediately changed (possibly causing the activity to be restarted). Otherwise, the new orientation is used the next time the activity is visible. **Note:**

- To improve the layout of apps on form factors with smallest width \>= 600dp, the system ignores calls to this method for apps that target Android 16 (API level 36) or higher.
- Device manufacturers can configure devices to ignore calls to this method to improve the layout of orientation-restricted apps.
- On devices with Android 16 (API level 36) or higher installed, virtual device owners (select trusted and privileged apps) can optimize app layout on displays they manage by ignoring calls to this method. See also [Companion app streaming](https://source.android.com/docs/core/permissions/app-streaming).

See [Device compatibility mode](https://developer.android.com/guide/practices/device-compatibility-mode).

<br />

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#setResult(kotlin.Int)(resultCode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Call this to set the result that your activity will return to its caller.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#setResult(kotlin.Int,%20android.content.Intent)(resultCode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, data: https://developer.android.com/reference/kotlin/android/content/Intent.html#!)`

Call this to set the result that your activity will return to its caller.

As of `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#GINGERBREAD:kotlin.Int`, the Intent you supply here can have `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_GRANT_READ_URI_PERMISSION:kotlin.Int` and/or `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_GRANT_WRITE_URI_PERMISSION:kotlin.Int` set. This will grant the Activity receiving the result access to the specific URIs in the Intent. Access will remain until the Activity has finished (it will remain across the hosting process being killed and other temporary destruction) and will be added to any existing set of URI permissions it already holds.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#setSecondaryProgress(kotlin.Int)(secondaryProgress: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Sets the secondary progress for the progress bar in the title. This progress is drawn between the primary progress (set via `https://developer.android.com/reference/kotlin/android/app/Activity#setProgress(kotlin.Int)` and the background. It can be ideal for media scenarios such as showing the buffering progress while the default progress shows the play progress.

In order for the progress bar to be shown, the feature must be requested via `https://developer.android.com/reference/kotlin/android/app/Activity#requestWindowFeature(kotlin.Int)`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#setShouldDockBigOverlays(kotlin.Boolean)(shouldDockBigOverlays: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`

Specifies a preference to dock big overlays like the expanded picture-in-picture on TV (see `https://developer.android.com/reference/kotlin/android/app/PictureInPictureParams.Builder#setExpandedAspectRatio(android.util.Rational)`). Docking puts the big overlay side-by-side next to this activity, so that both windows are fully visible to the user.

If unspecified, whether the overlay window will be docked or not, will be defined by the system.

If specified, the system will try to respect the preference, but it may be overridden by a user preference.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#setShowWhenLocked(kotlin.Boolean)(showWhenLocked: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`

Specifies whether an `https://developer.android.com/reference/kotlin/android/app/Activity` should be shown on top of the lock screen whenever the lockscreen is up and the activity is resumed. Normally an activity will be transitioned to the stopped state if it is started while the lockscreen is up, but with this flag set the activity will remain in the resumed state visible on-top of the lock screen. This value can be set as a manifest attribute using `https://developer.android.com/reference/kotlin/android/R.attr.html#showWhenLocked:kotlin.Int`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#setTaskDescription(android.app.ActivityManager.TaskDescription)(taskDescription: https://developer.android.com/reference/kotlin/android/app/ActivityManager.TaskDescription!)`

Sets information describing the task with this activity for presentation inside the Recents System UI. When `https://developer.android.com/reference/kotlin/android/app/ActivityManager#getRecentTasks(kotlin.Int,%20kotlin.Int)` is called, the activities of each task are traversed in order from the topmost activity to the bottommost. The traversal continues for each property until a suitable value is found. For each task the taskDescription will be returned in `https://developer.android.com/reference/kotlin/android/app/ActivityManager.TaskDescription`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#setTheme(kotlin.Int)(resid: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Set the base theme for this context. Note that this should be called before any views are instantiated in the Context (for example before calling android.app.Activity#setContentView or android.view.LayoutInflater#inflate).

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#setTitle(kotlin.Int)(titleId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Change the title associated with this activity. If this is a top-level activity, the title for its window will change. If it is an embedded activity, the parent can do whatever it wants with it.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#setTitle(kotlin.CharSequence)(title: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!)`

Change the title associated with this activity. If this is a top-level activity, the title for its window will change. If it is an embedded activity, the parent can do whatever it wants with it.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#setTitleColor(kotlin.Int)(textColor: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Change the color of the title associated with this activity.

This method is deprecated starting in API Level 11 and replaced by action bar styles. For information on styling the Action Bar, read the [Action Bar](https://developer.android.com/ guide/topics/ui/actionbar.html) developer guide.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#setTranslucent(kotlin.Boolean)(translucent: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`

Convert an activity, which particularly with `https://developer.android.com/reference/kotlin/android/R.attr.html#windowIsTranslucent:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/R.attr.html#windowIsFloating:kotlin.Int` attribute, to a fullscreen opaque activity, or convert it from opaque back to translucent.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#setTurnScreenOn(kotlin.Boolean)(turnScreenOn: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`

Specifies whether the screen should be turned on when the `https://developer.android.com/reference/kotlin/android/app/Activity` is resumed. Normally an activity will be transitioned to the stopped state if it is started while the screen if off, but with this flag set the activity will cause the screen to turn on if the activity will be visible and resumed due to the screen coming on. The screen will not be turned on if the activity won't be visible after the screen is turned on. This flag is normally used in conjunction with the `https://developer.android.com/reference/kotlin/android/R.attr.html#showWhenLocked:kotlin.Int` flag to make sure the activity is visible after the screen is turned on when the lockscreen is up. In addition, if this flag is set and the activity calls `https://developer.android.com/reference/kotlin/android/app/KeyguardManager#requestDismissKeyguard(android.app.Activity,%20android.app.KeyguardManager.KeyguardDismissCallback)` the screen will turn on.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#setVisible(kotlin.Boolean)(visible: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`

Control whether this activity's main window is visible. This is intended only for the special case of an activity that is not going to show a UI itself, but can't just finish prior to onResume() because it needs to wait for a service binding or such. Setting this to false allows you to prevent your UI from being shown during that time.

The default value for this is taken from the `https://developer.android.com/reference/kotlin/android/R.attr.html#windowNoDisplay:kotlin.Int` attribute of the activity's theme.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#setVolumeControlStream(kotlin.Int)(streamType: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Suggests an audio stream whose volume should be changed by the hardware volume controls.

The suggested audio stream will be tied to the window of this Activity. Volume requests which are received while the Activity is in the foreground will affect this stream.

It is not guaranteed that the hardware volume controls will always change this stream's volume (for example, if a call is in progress, its stream's volume may be changed instead). To reset back to the default, use `https://developer.android.com/reference/kotlin/android/media/AudioManager.html#USE_DEFAULT_STREAM_TYPE:kotlin.Int`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#setVrModeEnabled(kotlin.Boolean,%20android.content.ComponentName)(enabled: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html, requestedComponent: https://developer.android.com/reference/kotlin/android/content/ComponentName.html#)`

Enable or disable virtual reality (VR) mode for this Activity.

VR mode is a hint to Android system to switch to a mode optimized for VR applications while this Activity has user focus.

It is recommended that applications additionally declare `https://developer.android.com/reference/kotlin/android/R.attr.html#enableVrMode:kotlin.Int` in their manifest to allow for smooth activity transitions when switching between VR activities.

If the requested `https://developer.android.com/reference/kotlin/android/service/vr/VrListenerService.html#` component is not available, VR mode will not be started. Developers can handle this case as follows:

```kotlin
String servicePackage = "com.whatever.app";
  String serviceClass = "com.whatever.app.MyVrListenerService";
 
  // Name of the component of the VrListenerService to start.
  ComponentName serviceComponent = new ComponentName(servicePackage, serviceClass);
 
  try {
     setVrModeEnabled(true, myComponentName);
  } catch (PackageManager.NameNotFoundException e) {
         List<ApplicationInfo> installed = getPackageManager().getInstalledApplications(0);
         boolean isInstalled = false;
         for (ApplicationInfo app : installed) {
             if (app.packageName.equals(servicePackage)) {
                 isInstalled = true;
                 break;
             }
         }
         if (isInstalled) {
             // Package is installed, but not enabled in Settings.  Let user enable it.
             startActivity(new Intent(Settings.ACTION_VR_LISTENER_SETTINGS));
         } else {
             // Package is not installed.  Send an intent to download this.
             sentIntentToLaunchAppStore(servicePackage);
         }
  }
  
```

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#shouldDockBigOverlays()()`

Returns whether big overlays should be docked next to the activity as set by `https://developer.android.com/reference/kotlin/android/app/Activity#setShouldDockBigOverlays(kotlin.Boolean)`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#shouldShowRequestPermissionRationale(kotlin.String)(permission: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`

Gets whether you should show UI with rationale before requesting a permission.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#shouldShowRequestPermissionRationale(kotlin.String,%20kotlin.Int)(permission: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, deviceId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Gets whether you should show UI with rationale before requesting a permission.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#shouldUpRecreateTask(android.content.Intent)(targetIntent: https://developer.android.com/reference/kotlin/android/content/Intent.html#!)`

Returns true if the app should recreate the task when navigating 'up' from this activity by using targetIntent.

If this method returns false the app can trivially call `https://developer.android.com/reference/kotlin/android/app/Activity#navigateUpTo(android.content.Intent)` using the same parameters to correctly perform up navigation. If this method returns false, the app should synthesize a new task stack by using `https://developer.android.com/reference/kotlin/android/app/TaskStackBuilder` or another similar mechanism to perform up navigation.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#showAssist(android.os.Bundle)(args: https://developer.android.com/reference/kotlin/android/os/Bundle.html#!)`

Ask to have the current assistant shown to the user. This only works if the calling activity is the current foreground activity. It is the same as calling `https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionService.html#showSession(android.os.Bundle,%20kotlin.Int)` and requesting all of the possible context. The receiver will always see `https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession.html#SHOW_SOURCE_APPLICATION:kotlin.Int` set.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#showDialog(kotlin.Int)(id: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Simple version of `https://developer.android.com/reference/kotlin/android/app/Activity#showDialog(kotlin.Int,%20android.os.Bundle)` that does not take any arguments. Simply calls `https://developer.android.com/reference/kotlin/android/app/Activity#showDialog(kotlin.Int,%20android.os.Bundle)` with null arguments.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#showDialog(kotlin.Int,%20android.os.Bundle)(id: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, args: https://developer.android.com/reference/kotlin/android/os/Bundle.html#!)`

Show a dialog managed by this activity. A call to `https://developer.android.com/reference/kotlin/android/app/Activity#onCreateDialog(kotlin.Int,%20android.os.Bundle)` will be made with the same id the first time this is called for a given id. From thereafter, the dialog will be automatically saved and restored. *If you are targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#HONEYCOMB:kotlin.Int` or later, consider instead using a `https://developer.android.com/reference/kotlin/android/app/DialogFragment` instead.*

Each time a dialog is shown, `https://developer.android.com/reference/kotlin/android/app/Activity#onPrepareDialog(kotlin.Int,%20android.app.Dialog,%20android.os.Bundle)` will be made to provide an opportunity to do any timely preparation.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#showLockTaskEscapeMessage()()`

Shows the user the system defined message for telling the user how to exit lock task mode. The task containing this activity must be in lock task mode at the time of this call for the message to be displayed.

<br />

`https://developer.android.com/reference/kotlin/android/view/ActionMode.html#?` `https://developer.android.com/reference/kotlin/android/app/Activity#startActionMode(android.view.ActionMode.Callback)(callback: https://developer.android.com/reference/kotlin/android/view/ActionMode.Callback.html#!)`

Start an action mode of the default type `https://developer.android.com/reference/kotlin/android/view/ActionMode.html#TYPE_PRIMARY:kotlin.Int`.

<br />

`https://developer.android.com/reference/kotlin/android/view/ActionMode.html#?` `https://developer.android.com/reference/kotlin/android/app/Activity#startActionMode(android.view.ActionMode.Callback,%20kotlin.Int)(callback: https://developer.android.com/reference/kotlin/android/view/ActionMode.Callback.html#!, type: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Start an action mode of the given type.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#startActivities(kotlin.Array)(intents: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/android/content/Intent.html#!>!)`

Same as #startActivities(android.content.Intent\[\],android.os.Bundle) with no options specified.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#startActivities(kotlin.Array,%20android.os.Bundle)(intents: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/android/content/Intent.html#!>!, options: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?)`

Launch a new activity. You will not receive any information about when the activity exits. This implementation overrides the base version, providing information about the activity performing the launch. Because of this additional information, the `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_ACTIVITY_NEW_TASK:kotlin.Int` launch flag is not required; if not specified, the new activity will be added to the task of the caller.

This method throws `https://developer.android.com/reference/kotlin/android/content/ActivityNotFoundException.html#` if there was no Activity found to run the given Intent.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#startActivity(android.content.Intent)(intent: https://developer.android.com/reference/kotlin/android/content/Intent.html#!)`

Same as #startActivity(android.content.Intent,android.os.Bundle) with no options specified.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#startActivity(android.content.Intent,%20android.os.Bundle)(intent: https://developer.android.com/reference/kotlin/android/content/Intent.html#!, options: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?)`

Launch a new activity. You will not receive any information about when the activity exits. This implementation overrides the base version, providing information about the activity performing the launch. Because of this additional information, the `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_ACTIVITY_NEW_TASK:kotlin.Int` launch flag is not required; if not specified, the new activity will be added to the task of the caller.

This method throws `https://developer.android.com/reference/kotlin/android/content/ActivityNotFoundException.html#` if there was no Activity found to run the given Intent.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#startActivityForResult(android.content.Intent,%20kotlin.Int)(intent: https://developer.android.com/reference/kotlin/android/content/Intent.html#!, requestCode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Same as calling `https://developer.android.com/reference/kotlin/android/app/Activity#startActivityForResult(android.content.Intent,%20kotlin.Int,%20android.os.Bundle)` with no options.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#startActivityForResult(android.content.Intent,%20kotlin.Int,%20android.os.Bundle)(intent: https://developer.android.com/reference/kotlin/android/content/Intent.html#!, requestCode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, options: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?)`

Launch an activity for which you would like a result when it finished. When this activity exits, your onActivityResult() method will be called with the given requestCode. Using a negative requestCode is the same as calling #startActivity (the activity is not launched as a sub-activity).

Note that this method should only be used with Intent protocols that are defined to return a result. In other protocols (such as `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_MAIN:kotlin.String` or `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_VIEW:kotlin.String`), you may not get the result when you expect. For example, if the activity you are launching uses `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_ACTIVITY_NEW_TASK:kotlin.Int`, it will not run in your task and thus you will immediately receive a cancel result.

As a special case, if you call startActivityForResult() with a requestCode \>= 0 during the initial onCreate(Bundle savedInstanceState)/onResume() of your activity, then your window will not be displayed until a result is returned back from the started activity. This is to avoid visible flickering when redirecting to another activity.

This method throws `https://developer.android.com/reference/kotlin/android/content/ActivityNotFoundException.html#` if there was no Activity found to run the given Intent.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#startActivityFromChild(android.app.Activity,%20android.content.Intent,%20kotlin.Int)(child: https://developer.android.com/reference/kotlin/android/app/Activity, intent: https://developer.android.com/reference/kotlin/android/content/Intent.html#!, requestCode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Same as calling `https://developer.android.com/reference/kotlin/android/app/Activity#startActivityFromChild(android.app.Activity,%20android.content.Intent,%20kotlin.Int,%20android.os.Bundle)` with no options.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#startActivityFromChild(android.app.Activity,%20android.content.Intent,%20kotlin.Int,%20android.os.Bundle)(child: https://developer.android.com/reference/kotlin/android/app/Activity, intent: https://developer.android.com/reference/kotlin/android/content/Intent.html#!, requestCode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, options: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?)`

This is called when a child activity of this one calls its #startActivity or #startActivityForResult method.

This method throws `https://developer.android.com/reference/kotlin/android/content/ActivityNotFoundException.html#` if there was no Activity found to run the given Intent.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#startActivityFromFragment(android.app.Fragment,%20android.content.Intent,%20kotlin.Int)(fragment: https://developer.android.com/reference/kotlin/android/app/Fragment, intent: https://developer.android.com/reference/kotlin/android/content/Intent.html#!, requestCode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Same as calling `https://developer.android.com/reference/kotlin/android/app/Activity#startActivityFromFragment(android.app.Fragment,%20android.content.Intent,%20kotlin.Int,%20android.os.Bundle)` with no options.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#startActivityFromFragment(android.app.Fragment,%20android.content.Intent,%20kotlin.Int,%20android.os.Bundle)(fragment: https://developer.android.com/reference/kotlin/android/app/Fragment, intent: https://developer.android.com/reference/kotlin/android/content/Intent.html#!, requestCode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, options: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?)`

This is called when a Fragment in this activity calls its android.app.Fragment#startActivity or android.app.Fragment#startActivityForResult method.

This method throws `https://developer.android.com/reference/kotlin/android/content/ActivityNotFoundException.html#` if there was no Activity found to run the given Intent.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#startActivityIfNeeded(android.content.Intent,%20kotlin.Int)(intent: https://developer.android.com/reference/kotlin/android/content/Intent.html#, requestCode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Same as calling `https://developer.android.com/reference/kotlin/android/app/Activity#startActivityIfNeeded(android.content.Intent,%20kotlin.Int,%20android.os.Bundle)` with no options.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#startActivityIfNeeded(android.content.Intent,%20kotlin.Int,%20android.os.Bundle)(intent: https://developer.android.com/reference/kotlin/android/content/Intent.html#, requestCode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, options: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?)`

A special variation to launch an activity only if a new activity instance is needed to handle the given Intent. In other words, this is just like `https://developer.android.com/reference/kotlin/android/app/Activity#startActivityForResult(android.content.Intent,%20kotlin.Int)` except: if you are using the `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_ACTIVITY_SINGLE_TOP:kotlin.Int` flag, or singleTask or singleTop `https://developer.android.com/reference/kotlin/android/R.styleable.html#AndroidManifestActivity_launchMode:kotlin.Int`, and the activity that handles intent is the same as your currently running activity, then a new instance is not needed. In this case, instead of the normal behavior of calling #onNewIntent this function will return and you can handle the Intent yourself.

This function can only be called from a top-level activity; if it is called from a child activity, a runtime exception will be thrown.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#startIntentSender(android.content.IntentSender,%20android.content.Intent,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)(intent: https://developer.android.com/reference/kotlin/android/content/IntentSender.html#!, fillInIntent: https://developer.android.com/reference/kotlin/android/content/Intent.html#?, flagsMask: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, flagsValues: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, extraFlags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Same as calling #startIntentSender(android.content.IntentSender,android.content.Intent,int,int,int,android.os.Bundle) with no options.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#startIntentSender(android.content.IntentSender,%20android.content.Intent,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20android.os.Bundle)(intent: https://developer.android.com/reference/kotlin/android/content/IntentSender.html#!, fillInIntent: https://developer.android.com/reference/kotlin/android/content/Intent.html#?, flagsMask: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, flagsValues: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, extraFlags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, options: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?)`

Like #startActivity(android.content.Intent,android.os.Bundle), but taking a IntentSender to start; see `https://developer.android.com/reference/kotlin/android/app/Activity#startIntentSenderForResult(android.content.IntentSender,%20kotlin.Int,%20android.content.Intent,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20android.os.Bundle)` for more information.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#startIntentSenderForResult(android.content.IntentSender,%20kotlin.Int,%20android.content.Intent,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)(intent: https://developer.android.com/reference/kotlin/android/content/IntentSender.html#!, requestCode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, fillInIntent: https://developer.android.com/reference/kotlin/android/content/Intent.html#?, flagsMask: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, flagsValues: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, extraFlags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Same as calling `https://developer.android.com/reference/kotlin/android/app/Activity#startIntentSenderForResult(android.content.IntentSender,%20kotlin.Int,%20android.content.Intent,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20android.os.Bundle)` with no options.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#startIntentSenderForResult(android.content.IntentSender,%20kotlin.Int,%20android.content.Intent,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20android.os.Bundle)(intent: https://developer.android.com/reference/kotlin/android/content/IntentSender.html#!, requestCode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, fillInIntent: https://developer.android.com/reference/kotlin/android/content/Intent.html#?, flagsMask: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, flagsValues: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, extraFlags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, options: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?)`

Like `https://developer.android.com/reference/kotlin/android/app/Activity#startActivityForResult(android.content.Intent,%20kotlin.Int)`, but allowing you to use a IntentSender to describe the activity to be started. If the IntentSender is for an activity, that activity will be started as if you had called the regular `https://developer.android.com/reference/kotlin/android/app/Activity#startActivityForResult(android.content.Intent,%20kotlin.Int)` here; otherwise, its associated action will be executed (such as sending a broadcast) as if you had called android.content.IntentSender#sendIntent on it.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#startIntentSenderFromChild(android.app.Activity,%20android.content.IntentSender,%20kotlin.Int,%20android.content.Intent,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)(child: https://developer.android.com/reference/kotlin/android/app/Activity!, intent: https://developer.android.com/reference/kotlin/android/content/IntentSender.html#!, requestCode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, fillInIntent: https://developer.android.com/reference/kotlin/android/content/Intent.html#!, flagsMask: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, flagsValues: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, extraFlags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Same as calling `https://developer.android.com/reference/kotlin/android/app/Activity#startIntentSenderFromChild(android.app.Activity,%20android.content.IntentSender,%20kotlin.Int,%20android.content.Intent,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20android.os.Bundle)` with no options.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#startIntentSenderFromChild(android.app.Activity,%20android.content.IntentSender,%20kotlin.Int,%20android.content.Intent,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20android.os.Bundle)(child: https://developer.android.com/reference/kotlin/android/app/Activity!, intent: https://developer.android.com/reference/kotlin/android/content/IntentSender.html#!, requestCode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, fillInIntent: https://developer.android.com/reference/kotlin/android/content/Intent.html#!, flagsMask: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, flagsValues: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, extraFlags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, options: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?)`

Like `https://developer.android.com/reference/kotlin/android/app/Activity#startActivityFromChild(android.app.Activity,%20android.content.Intent,%20kotlin.Int)`, but taking a IntentSender; see `https://developer.android.com/reference/kotlin/android/app/Activity#startIntentSenderForResult(android.content.IntentSender,%20kotlin.Int,%20android.content.Intent,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)` for more information.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#startLocalVoiceInteraction(android.os.Bundle)(privateOptions: https://developer.android.com/reference/kotlin/android/os/Bundle.html#!)`

Starts a local voice interaction session. When ready, `https://developer.android.com/reference/kotlin/android/app/Activity#onLocalVoiceInteractionStarted()` is called. You can pass a bundle of private options to the registered voice interaction service.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#startLockTask()()`

Request to put this activity in a mode where the user is locked to a restricted set of applications.

If `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager#isLockTaskPermitted(kotlin.String)` returns `true` for this component, the current task will be launched directly into LockTask mode. Only apps allowlisted by `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager#setLockTaskPackages(android.content.ComponentName,%20kotlin.Array)` can be launched while LockTask mode is active. The user will not be able to leave this mode until this activity calls `https://developer.android.com/reference/kotlin/android/app/Activity#stopLockTask()`. Calling this method while the device is already in LockTask mode has no effect.

Otherwise, the current task will be launched into screen pinning mode. In this case, the system will prompt the user with a dialog requesting permission to use this mode. The user can exit at any time through instructions shown on the request dialog. Calling `https://developer.android.com/reference/kotlin/android/app/Activity#stopLockTask()` will also terminate this mode.

**Note:** this method can only be called when the activity is foreground. That is, between `https://developer.android.com/reference/kotlin/android/app/Activity#onResume()` and `https://developer.android.com/reference/kotlin/android/app/Activity#onPause()`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#startManagingCursor(android.database.Cursor)(c: https://developer.android.com/reference/kotlin/android/database/Cursor.html#!)`

This method allows the activity to take care of managing the given `https://developer.android.com/reference/kotlin/android/database/Cursor.html#`'s lifecycle for you based on the activity's lifecycle. That is, when the activity is stopped it will automatically call `https://developer.android.com/reference/kotlin/android/database/Cursor.html#deactivate()` on the given Cursor, and when it is later restarted it will call `https://developer.android.com/reference/kotlin/android/database/Cursor.html#requery()` for you. When the activity is destroyed, all managed Cursors will be closed automatically. *If you are targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#HONEYCOMB:kotlin.Int` or later, consider instead using `https://developer.android.com/reference/kotlin/android/app/LoaderManager` instead, available via `https://developer.android.com/reference/kotlin/android/app/Activity#getLoaderManager()`.*

**Warning:** Do not call android.database.Cursor#close() on cursor obtained from `https://developer.android.com/reference/kotlin/android/app/Activity#managedQuery(android.net.Uri,%20kotlin.Array,%20kotlin.String,%20kotlin.Array,%20kotlin.String)`, because the activity will do that for you at the appropriate time. However, if you call `https://developer.android.com/reference/kotlin/android/app/Activity#stopManagingCursor(android.database.Cursor)` on a cursor from a managed query, the system *will not* automatically close the cursor and, in that case, you must call android.database.Cursor#close().

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#startNextMatchingActivity(android.content.Intent)(intent: https://developer.android.com/reference/kotlin/android/content/Intent.html#)`

Same as calling `https://developer.android.com/reference/kotlin/android/app/Activity#startNextMatchingActivity(android.content.Intent,%20android.os.Bundle)` with no options.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#startNextMatchingActivity(android.content.Intent,%20android.os.Bundle)(intent: https://developer.android.com/reference/kotlin/android/content/Intent.html#, options: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?)`

Special version of starting an activity, for use when you are replacing other activity components. You can use this to hand the Intent off to the next Activity that can handle it. You typically call this in #onCreate with the Intent returned by `https://developer.android.com/reference/kotlin/android/app/Activity#getIntent()`. Note: For security reasons, the caller identity propagated to the next activity will reflect this intermediary app's identity unless it shares the same UID as the original caller. The receiving activity should validate the immediate caller rather than assuming the original intent sender is preserved.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#startPostponedEnterTransition()()`

Begin postponed transitions after `https://developer.android.com/reference/kotlin/android/app/Activity#postponeEnterTransition()` was called. If postponeEnterTransition() was called, you must call startPostponedEnterTransition() to have your Activity start drawing.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#startSearch(kotlin.String,%20kotlin.Boolean,%20android.os.Bundle,%20kotlin.Boolean)(initialQuery: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, selectInitialQuery: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html, appSearchData: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?, globalSearch: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`

This hook is called to launch the search UI.

It is typically called from onSearchRequested(), either directly from Activity.onSearchRequested() or from an overridden version in any given Activity. If your goal is simply to activate search, it is preferred to call onSearchRequested(), which may have been overridden elsewhere in your Activity. If your goal is to inject specific data such as context data, it is preferred to *override* onSearchRequested(), so that any callers to it will benefit from the override.

Note: when running in a `https://developer.android.com/reference/kotlin/android/content/res/Configuration.html#UI_MODE_TYPE_WATCH:kotlin.Int`, use of this API is not supported.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#stopLocalVoiceInteraction()()`

Request to terminate the current voice interaction that was previously started using `https://developer.android.com/reference/kotlin/android/app/Activity#startLocalVoiceInteraction(android.os.Bundle)`. When the interaction is terminated, `https://developer.android.com/reference/kotlin/android/app/Activity#onLocalVoiceInteractionStopped()` will be called.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#stopLockTask()()`

Stop the current task from being locked.

Called to end the LockTask or screen pinning mode started by `https://developer.android.com/reference/kotlin/android/app/Activity#startLockTask()`. This can only be called by activities that have called `https://developer.android.com/reference/kotlin/android/app/Activity#startLockTask()` previously.

**Note:** If the device is in LockTask mode that is not initially started by this activity, then calling this method will not terminate the LockTask mode, but only finish its own task. The device will remain in LockTask mode, until the activity which started the LockTask mode calls this method, or until its allowlist authorization is revoked by `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager#setLockTaskPackages(android.content.ComponentName,%20kotlin.Array)`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#stopManagingCursor(android.database.Cursor)(c: https://developer.android.com/reference/kotlin/android/database/Cursor.html#!)`

Given a Cursor that was previously given to `https://developer.android.com/reference/kotlin/android/app/Activity#startManagingCursor(android.database.Cursor)`, stop the activity's management of that cursor.

**Warning:** After calling this method on a cursor from a managed query, the system *will not* automatically close the cursor and you must call android.database.Cursor#close().

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#takeKeyEvents(kotlin.Boolean)(get: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`

Request that key events come to this activity. Use this if your activity has no views with focus, but the activity still wants a chance to process key events.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#triggerSearch(kotlin.String,%20android.os.Bundle)(query: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, appSearchData: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?)`

Similar to `https://developer.android.com/reference/kotlin/android/app/Activity#startSearch(kotlin.String,%20kotlin.Boolean,%20android.os.Bundle,%20kotlin.Boolean)`, but actually fires off the search query after invoking the search dialog. Made available for testing purposes.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#unregisterActivityLifecycleCallbacks(android.app.Application.ActivityLifecycleCallbacks)(callback: https://developer.android.com/reference/kotlin/android/app/Application.ActivityLifecycleCallbacks)`

Unregister an `https://developer.android.com/reference/kotlin/android/app/Application.ActivityLifecycleCallbacks` previously registered with `https://developer.android.com/reference/kotlin/android/app/Activity#registerActivityLifecycleCallbacks(android.app.Application.ActivityLifecycleCallbacks)`. It will not receive any further callbacks.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#unregisterComponentCallbacks(android.content.ComponentCallbacks)(callback: https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks.html#!)`

Remove a `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks.html#` object that was previously registered with `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#registerComponentCallbacks(android.content.ComponentCallbacks)`.

After `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#TIRAMISU:kotlin.Int`, the `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks.html#` will be unregistered to `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#getBaseContext()`, and can be only used after `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#attachBaseContext(android.content.Context)`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#unregisterForContextMenu(android.view.View)(view: https://developer.android.com/reference/kotlin/android/view/View.html#!)`

Prevents a context menu to be shown for the given view. This method will remove the `https://developer.android.com/reference/kotlin/android/view/View.OnCreateContextMenuListener.html#` on the view.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Activity#unregisterScreenCaptureCallback(android.app.Activity.ScreenCaptureCallback)(callback: https://developer.android.com/reference/kotlin/android/app/Activity.ScreenCaptureCallback)`

Unregisters a screen capture callback for this surface. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#DETECT_SCREEN_CAPTURE:kotlin.String`

<br />

From class `https://developer.android.com/reference/kotlin/android/view/ContextThemeWrapper.html#` `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/ContextThemeWrapper.html#applyOverrideConfiguration(android.content.res.Configuration)(overrideConfiguration: https://developer.android.com/reference/kotlin/android/content/res/Configuration.html#!)`

Call to set an "override configuration" on this context -- this is a configuration that replies one or more values of the standard configuration that is applied to the context. See `https://developer.android.com/reference/kotlin/android/content/Context.html#createConfigurationContext(android.content.res.Configuration)` for more information.

This method can only be called once, and must be called before any calls to #getResources() or #getAssets() are made.

<br />

`https://developer.android.com/reference/kotlin/android/content/res/AssetManager.html#!` `https://developer.android.com/reference/kotlin/android/view/ContextThemeWrapper.html#getAssets()()`

Returns an AssetManager instance for the application's package.

**Note:** Implementations of this method should return an AssetManager instance that is consistent with the Resources instance returned by `https://developer.android.com/reference/kotlin/android/content/Context.html#getResources()`. For example, they should share the same `https://developer.android.com/reference/kotlin/android/content/res/Configuration.html#` object.

<br />

`https://developer.android.com/reference/kotlin/android/content/res/Resources.html#!` `https://developer.android.com/reference/kotlin/android/view/ContextThemeWrapper.html#getResources()()`

Returns a Resources instance for the application's package.

**Note:** Implementations of this method should return a Resources instance that is consistent with the AssetManager instance returned by `https://developer.android.com/reference/kotlin/android/content/Context.html#getAssets()`. For example, they should share the same `https://developer.android.com/reference/kotlin/android/content/res/Configuration.html#` object.

<br />

`https://developer.android.com/reference/kotlin/android/content/res/Resources.Theme.html#!` `https://developer.android.com/reference/kotlin/android/view/ContextThemeWrapper.html#getTheme()()`

Return the Theme object associated with this Context.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/ContextThemeWrapper.html#setTheme(android.content.res.Resources.Theme)(theme: https://developer.android.com/reference/kotlin/android/content/res/Resources.Theme.html#?)`

Set the configure the current theme. If null is provided then the default Theme is returned on the next call to #getTheme()

<br />

From class `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#` `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#bindIsolatedService(android.content.Intent,%20kotlin.Int,%20kotlin.String,%20java.util.concurrent.Executor,%20android.content.ServiceConnection)(service: https://developer.android.com/reference/kotlin/android/content/Intent.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, instanceName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, conn: https://developer.android.com/reference/kotlin/android/content/ServiceConnection.html#)`

Variation of #bindService that, in the specific case of isolated services, allows the caller to generate multiple instances of a service from a single component declaration. In other words, you can use this to bind to a service that has specified `https://developer.android.com/reference/kotlin/android/R.attr.html#isolatedProcess:kotlin.Int` and, in addition to the existing behavior of running in an isolated process, you can also through the arguments here have the system bring up multiple concurrent processes hosting their own instances of that service. The instanceName you provide here identifies the different instances, and you can use `https://developer.android.com/reference/kotlin/android/content/Context.html#updateServiceGroup(android.content.ServiceConnection,%20kotlin.Int,%20kotlin.Int)` to tell the system how it should manage each of these instances.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#bindService(android.content.Intent,%20android.content.Context.BindServiceFlags,%20java.util.concurrent.Executor,%20android.content.ServiceConnection)(service: https://developer.android.com/reference/kotlin/android/content/Intent.html#, flags: https://developer.android.com/reference/kotlin/android/content/Context.BindServiceFlags.html#, executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, conn: https://developer.android.com/reference/kotlin/android/content/ServiceConnection.html#)`

See `https://developer.android.com/reference/kotlin/android/content/Context.html#bindService(android.content.Intent,%20kotlin.Int,%20java.util.concurrent.Executor,%20android.content.ServiceConnection)` Call `https://developer.android.com/reference/kotlin/android/content/Context.BindServiceFlags.html#of(kotlin.Long)` to obtain a BindServiceFlags object.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#bindService(android.content.Intent,%20android.content.ServiceConnection,%20android.content.Context.BindServiceFlags)(service: https://developer.android.com/reference/kotlin/android/content/Intent.html#, conn: https://developer.android.com/reference/kotlin/android/content/ServiceConnection.html#, flags: https://developer.android.com/reference/kotlin/android/content/Context.BindServiceFlags.html#)`

See `https://developer.android.com/reference/kotlin/android/content/Context.html#bindService(android.content.Intent,%20android.content.ServiceConnection,%20kotlin.Int)` Call `https://developer.android.com/reference/kotlin/android/content/Context.BindServiceFlags.html#of(kotlin.Long)` to obtain a BindServiceFlags object.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#bindService(android.content.Intent,%20android.content.ServiceConnection,%20kotlin.Int)(service: https://developer.android.com/reference/kotlin/android/content/Intent.html#, conn: https://developer.android.com/reference/kotlin/android/content/ServiceConnection.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Connects to an application service, creating it if needed. This defines a dependency between your application and the service. The given conn will receive the service object when it is created and be told if it dies and restarts. The service will be considered required by the system only for as long as the calling context exists. For example, if this Context is an Activity that is stopped, the service will not be required to continue running until the Activity is resumed.

If the service does not support binding, it may return `null` from its `https://developer.android.com/reference/kotlin/android/app/Service#onBind(android.content.Intent)` method. If it does, then the ServiceConnection's `https://developer.android.com/reference/kotlin/android/content/ServiceConnection.html#onNullBinding(android.content.ComponentName)` method will be invoked instead of `https://developer.android.com/reference/kotlin/android/content/ServiceConnection.html#onServiceConnected(android.content.ComponentName,%20android.os.IBinder)`.

**Note:** This method *cannot* be called from a `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#` component. A pattern you can use to communicate from a BroadcastReceiver to a Service is to call `https://developer.android.com/reference/kotlin/android/content/Context.html#startService(android.content.Intent)` with the arguments containing the command to be sent, with the service calling its `https://developer.android.com/reference/kotlin/android/app/Service#stopSelf(kotlin.Int)` method when done executing that command. See the API demo App/Service/Service Start Arguments Controller for an illustration of this. It is okay, however, to use this method from a BroadcastReceiver that has been registered with #registerReceiver, since the lifetime of this BroadcastReceiver is tied to another object (the one that registered it).

This method only accepts a int type flag, to pass in a long type flag, call `https://developer.android.com/reference/kotlin/android/content/Context.html#bindService(android.content.Intent,%20android.content.ServiceConnection,%20android.content.Context.BindServiceFlags)` instead.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#bindService(android.content.Intent,%20kotlin.Int,%20java.util.concurrent.Executor,%20android.content.ServiceConnection)(service: https://developer.android.com/reference/kotlin/android/content/Intent.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, conn: https://developer.android.com/reference/kotlin/android/content/ServiceConnection.html#)`

Same as `https://developer.android.com/reference/kotlin/android/content/Context.html#bindService(android.content.Intent,%20android.content.ServiceConnection,%20kotlin.Int)` with executor to control ServiceConnection callbacks.

This method only accepts a 32 bits flag, to pass in a 64 bits flag, call `https://developer.android.com/reference/kotlin/android/content/Context.html#bindService(android.content.Intent,%20android.content.Context.BindServiceFlags,%20java.util.concurrent.Executor,%20android.content.ServiceConnection)` instead.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#bindServiceAsUser(android.content.Intent,%20android.content.ServiceConnection,%20android.content.Context.BindServiceFlags,%20android.os.UserHandle)(service: https://developer.android.com/reference/kotlin/android/content/Intent.html#, conn: https://developer.android.com/reference/kotlin/android/content/ServiceConnection.html#, flags: https://developer.android.com/reference/kotlin/android/content/Context.BindServiceFlags.html#, user: https://developer.android.com/reference/kotlin/android/os/UserHandle.html#)`

See `https://developer.android.com/reference/kotlin/android/content/Context.html#bindServiceAsUser(android.content.Intent,%20android.content.ServiceConnection,%20kotlin.Int,%20android.os.UserHandle)` Call `https://developer.android.com/reference/kotlin/android/content/Context.BindServiceFlags.html#of(kotlin.Long)` to obtain a BindServiceFlags object.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#bindServiceAsUser(android.content.Intent,%20android.content.ServiceConnection,%20kotlin.Int,%20android.os.UserHandle)(service: https://developer.android.com/reference/kotlin/android/content/Intent.html#, conn: https://developer.android.com/reference/kotlin/android/content/ServiceConnection.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, user: https://developer.android.com/reference/kotlin/android/os/UserHandle.html#)`

Binds to a service in the given `user` in the same manner as #bindService.

Requires that one of the following conditions are met:

- caller has `android.Manifest.permission.INTERACT_ACROSS_USERS_FULL`
- caller has `android.Manifest.permission.INTERACT_ACROSS_USERS` and is the same package as the `service` (determined by its component's package) and the Android version is at least `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#TIRAMISU:kotlin.Int`
- caller has `android.Manifest.permission.INTERACT_ACROSS_USERS` and is in same profile group as the given `user`
- caller has `android.Manifest.permission.INTERACT_ACROSS_PROFILES` and is in same profile group as the given `user` and is the same package as the `service`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#checkCallingOrSelfPermission(kotlin.String)(permission: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`

Determine whether the calling process of an IPC *or you* have been granted a particular permission. This is the same as `https://developer.android.com/reference/kotlin/android/content/Context.html#checkCallingPermission(kotlin.String)`, except it grants your own permissions if you are not currently processing an IPC. Use with care!

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#checkCallingOrSelfUriPermission(android.net.Uri,%20kotlin.Int)(uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#!, modeFlags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Determine whether the calling process of an IPC *or you* has been granted permission to access a specific URI. This is the same as `https://developer.android.com/reference/kotlin/android/content/Context.html#checkCallingUriPermission(android.net.Uri,%20kotlin.Int)`, except it grants your own permissions if you are not currently processing an IPC. Use with care!

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#checkCallingOrSelfUriPermissions(kotlin.collections.MutableList,%20kotlin.Int)(uris: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/net/Uri.html#!>, modeFlags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Determine whether the calling process of an IPC *or you* has been granted permission to access a list of URIs. This is the same as `https://developer.android.com/reference/kotlin/android/content/Context.html#checkCallingUriPermission(android.net.Uri,%20kotlin.Int)`, except it grants your own permissions if you are not currently processing an IPC. Use with care!

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#checkCallingPermission(kotlin.String)(permission: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`

Determine whether the calling process of an IPC you are handling has been granted a particular permission. This is basically the same as calling `https://developer.android.com/reference/kotlin/android/content/Context.html#checkPermission(kotlin.String,%20kotlin.Int,%20kotlin.Int)` with the pid and uid returned by `https://developer.android.com/reference/kotlin/android/os/Binder.html#getCallingPid()` and `https://developer.android.com/reference/kotlin/android/os/Binder.html#getCallingUid()`. One important difference is that if you are not currently processing an IPC, this function will always fail. This is done to protect against accidentally leaking permissions; you can use `https://developer.android.com/reference/kotlin/android/content/Context.html#checkCallingOrSelfPermission(kotlin.String)` to avoid this protection.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#checkCallingUriPermission(android.net.Uri,%20kotlin.Int)(uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#!, modeFlags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Determine whether the calling process and uid has been granted permission to access a specific URI. This is basically the same as calling `https://developer.android.com/reference/kotlin/android/content/Context.html#checkUriPermission(android.net.Uri,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)` with the pid and uid returned by `https://developer.android.com/reference/kotlin/android/os/Binder.html#getCallingPid()` and `https://developer.android.com/reference/kotlin/android/os/Binder.html#getCallingUid()`. One important difference is that if you are not currently processing an IPC, this function will always fail.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#checkCallingUriPermissions(kotlin.collections.MutableList,%20kotlin.Int)(uris: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/net/Uri.html#!>, modeFlags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Determine whether the calling process and uid has been granted permission to access a list of URIs. This is basically the same as calling `https://developer.android.com/reference/kotlin/android/content/Context.html#checkUriPermissions(kotlin.collections.MutableList,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)` with the pid and uid returned by `https://developer.android.com/reference/kotlin/android/os/Binder.html#getCallingPid()` and `https://developer.android.com/reference/kotlin/android/os/Binder.html#getCallingUid()`. One important difference is that if you are not currently processing an IPC, this function will always fail.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#checkContentUriPermissionFull(android.net.Uri,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)(uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#, pid: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, uid: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, modeFlags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Determine whether a particular process and uid has been granted permission to access a specific content URI.

Unlike `https://developer.android.com/reference/kotlin/android/content/Context.html#checkUriPermission(android.net.Uri,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)`, this method checks for general access to the URI's content provider, as well as explicitly granted permissions.

Note, this check will throw an `https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#` for non-content URIs.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#checkPermission(kotlin.String,%20kotlin.Int,%20kotlin.Int)(permission: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, pid: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, uid: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Determine whether the given permission is allowed for a particular process and user ID running in the system.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#checkSelfPermission(kotlin.String)(permission: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`

Determine whether *you* have been granted a particular permission.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#checkUriPermission(android.net.Uri,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)(uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#!, pid: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, uid: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, modeFlags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Determine whether a particular process and uid has been granted permission to access a specific URI. This only checks for permissions that have been explicitly granted -- if the given process/uid has more general access to the URI's content provider then this check will always fail.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#checkUriPermission(android.net.Uri,%20kotlin.String,%20kotlin.String,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)(uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#?, readPermission: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, writePermission: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, pid: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, uid: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, modeFlags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Check both a Uri and normal permission. This allows you to perform both `https://developer.android.com/reference/kotlin/android/content/Context.html#checkPermission(kotlin.String,%20kotlin.Int,%20kotlin.Int)` and #checkUriPermission in one call.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#checkUriPermissions(kotlin.collections.MutableList,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)(uris: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/net/Uri.html#!>, pid: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, uid: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, modeFlags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Determine whether a particular process and uid has been granted permission to access a list of URIs. This only checks for permissions that have been explicitly granted -- if the given process/uid has more general access to the URI's content provider then this check will always fail. **Note:** On SDK Version `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int`, calling this method from a secondary-user's context will incorrectly return `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#PERMISSION_DENIED:kotlin.Int` for all {code uris}.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#clearWallpaper()()`

<br />

`https://developer.android.com/reference/kotlin/android/content/Context.html#` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#createAttributionContext(kotlin.String)(attributionTag: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?)`

Return a new Context object for the current Context but attribute to a different tag. In complex apps attribution tagging can be used to distinguish between separate logical parts.

<br />

`https://developer.android.com/reference/kotlin/android/content/Context.html#!` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#createConfigurationContext(android.content.res.Configuration)(overrideConfiguration: https://developer.android.com/reference/kotlin/android/content/res/Configuration.html#)`

Return a new Context object for the current Context but whose resources are adjusted to match the given Configuration. Each call to this method returns a new instance of a Context object; Context objects are not shared, however common state (ClassLoader, other Resources for the same configuration) may be so the Context itself can be fairly lightweight.

<br />

`https://developer.android.com/reference/kotlin/android/content/Context.html#` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#createContext(android.content.ContextParams)(contextParams: https://developer.android.com/reference/kotlin/android/content/ContextParams.html#)`

Creates a context with specific properties and behaviors.

<br />

`https://developer.android.com/reference/kotlin/android/content/Context.html#!` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#createContextForSplit(kotlin.String)(splitName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)`

Return a new Context object for the given split name. The new Context has a ClassLoader and Resources object that can access the split's and all of its dependencies' code/resources. Each call to this method returns a new instance of a Context object; Context objects are not shared, however common state (ClassLoader, other Resources for the same split) may be so the Context itself can be fairly lightweight.

<br />

`https://developer.android.com/reference/kotlin/android/content/Context.html#` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#createDeviceContext(kotlin.Int)(deviceId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Returns a new `Context` object from the current context but with device association given by the `deviceId`. Each call to this method returns a new instance of a context object. Context objects are not shared; however, common state (such as the `https://developer.android.com/reference/kotlin/java/lang/ClassLoader.html#` and other resources for the same configuration) can be shared, so the `Context` itself is lightweight.

Applications that run on virtual devices may use this method to access the default device capabilities and functionality (by passing `https://developer.android.com/reference/kotlin/android/content/Context.html#DEVICE_ID_DEFAULT:kotlin.Int`. Similarly, applications running on the default device may access the functionality of virtual devices.

Note that the newly created instance will be associated with the same display as the parent Context, regardless of the device ID passed here.

<br />

`https://developer.android.com/reference/kotlin/android/content/Context.html#!` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#createDeviceProtectedStorageContext()()`

Return a new Context object for the current Context but whose storage APIs are backed by device-protected storage.

On devices with direct boot, data stored in this location is encrypted with a key tied to the physical device, and it can be accessed immediately after the device has booted successfully, both *before and after* the user has authenticated with their credentials (such as a lock pattern or PIN).

Because device-protected data is available without user authentication, you should carefully limit the data you store using this Context. For example, storing sensitive authentication tokens or passwords in the device-protected area is strongly discouraged.

If the underlying device does not have the ability to store device-protected and credential-protected data using different keys, then both storage areas will become available at the same time. They remain as two distinct storage locations on disk, and only the window of availability changes.

Each call to this method returns a new instance of a Context object; Context objects are not shared, however common state (ClassLoader, other Resources for the same configuration) may be so the Context itself can be fairly lightweight.

<br />

`https://developer.android.com/reference/kotlin/android/content/Context.html#!` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#createDisplayContext(android.view.Display)(display: https://developer.android.com/reference/kotlin/android/view/Display.html#)`

Returns a new `Context` object from the current context but with resources adjusted to match the metrics of `display`. Each call to this method returns a new instance of a context object. Context objects are not shared; however, common state (such as the `https://developer.android.com/reference/kotlin/java/lang/ClassLoader.html#` and other resources for the same configuration) can be shared, so the `Context` itself is lightweight.

**Note:** This `Context` is **not** expected to be updated with new configuration if the underlying display configuration changes and the cached `Resources` it returns could be stale. It is suggested to use `https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager.DisplayListener.html#` to listen for changes and re-create an instance if necessary.

This `Context` is **not** a UI context, do not use it to access UI components or obtain a `https://developer.android.com/reference/kotlin/android/view/WindowManager.html#` instance.

To obtain an instance of `https://developer.android.com/reference/kotlin/android/view/WindowManager.html#` configured to show windows on the given display, call `https://developer.android.com/reference/kotlin/android/content/Context.html#createWindowContext(kotlin.Int,%20android.os.Bundle)` on the returned display context, then call `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` or `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(java.lang.Class)` on the returned window context.

<br />

`https://developer.android.com/reference/kotlin/android/content/Context.html#!` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#createPackageContext(kotlin.String,%20kotlin.Int)(packageName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Return a new Context object for the given application name. This Context is the same as what the named application gets when it is launched, containing the same resources and class loader. Each call to this method returns a new instance of a Context object; Context objects are not shared, however they share common state (Resources, ClassLoader, etc) so the Context instance itself is fairly lightweight.

Throws `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.NameNotFoundException.html#` if there is no application with the given package name.

Throws `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#` if the Context requested can not be loaded into the caller's process for security reasons (see `https://developer.android.com/reference/kotlin/android/content/Context.html#CONTEXT_INCLUDE_CODE:kotlin.Int` for more information}.

<br />

`https://developer.android.com/reference/kotlin/android/content/Context.html#` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#createWindowContext(android.view.Display,%20kotlin.Int,%20android.os.Bundle)(display: https://developer.android.com/reference/kotlin/android/view/Display.html#, type: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, options: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?)`

Creates a `Context` for a non-`https://developer.android.com/reference/kotlin/android/app/Activity` window on the given `https://developer.android.com/reference/kotlin/android/view/Display.html#`.

Similar to `https://developer.android.com/reference/kotlin/android/content/Context.html#createWindowContext(kotlin.Int,%20android.os.Bundle)`, but the `display` is passed in, instead of implicitly using the `https://developer.android.com/reference/kotlin/android/content/Context.html#getDisplay()`.

<br />

`https://developer.android.com/reference/kotlin/android/content/Context.html#` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#createWindowContext(kotlin.Int,%20android.os.Bundle)(type: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, options: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?)`

Creates a Context for a non-activity window.

A window context is a context that can be used to add non-activity windows, such as `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#TYPE_APPLICATION_OVERLAY:kotlin.Int`. A window context must be created from a context that has an associated `https://developer.android.com/reference/kotlin/android/view/Display.html#`, such as `https://developer.android.com/reference/kotlin/android/app/Activity` or a context created with `https://developer.android.com/reference/kotlin/android/content/Context.html#createDisplayContext(android.view.Display)`.

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

After `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int`, window context provides the capability to receive configuration changes for existing token by overriding the `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#token:android.os.IBinder` of the `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#` passed in `https://developer.android.com/reference/kotlin/android/view/ViewManager.html#addView(android.view.View,%20android.view.ViewGroup.LayoutParams)`. This is useful when an application needs to attach its window to an existing activity for window token sharing use-case.

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

After `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int`, window context provides the capability to listen to its `https://developer.android.com/reference/kotlin/android/content/res/Configuration.html#` changes by calling `https://developer.android.com/reference/kotlin/android/content/Context.html#registerComponentCallbacks(android.content.ComponentCallbacks)`, while other kinds of `https://developer.android.com/reference/kotlin/android/content/Context.html#` will register the `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks.html#` to `https://developer.android.com/reference/kotlin/android/content/Context.html#getApplicationContext()`. Note that window context only propagate `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks.html#onConfigurationChanged(android.content.res.Configuration)` callback. `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks.html#onLowMemory()` or other callbacks in `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#` won't be invoked.

Note that using `https://developer.android.com/reference/kotlin/android/app/Application` or `https://developer.android.com/reference/kotlin/android/app/Service` context for UI-related queries may result in layout or continuity issues on devices with variable screen sizes (e.g. foldables) or in multi-window modes, since these non-UI contexts may not reflect the `https://developer.android.com/reference/kotlin/android/content/res/Configuration.html#` changes for the visual container.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#databaseList()()`

Returns an array of strings naming the private databases associated with this Context's application package.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#deleteDatabase(kotlin.String)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)`

Delete an existing private SQLiteDatabase associated with this Context's application package.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#deleteFile(kotlin.String)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)`

Delete the given private file associated with this Context's application package.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#deleteSharedPreferences(kotlin.String)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)`

Delete an existing shared preferences file.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#enforceCallingOrSelfPermission(kotlin.String,%20kotlin.String)(permission: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, message: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?)`

If neither you nor the calling process of an IPC you are handling has been granted a particular permission, throw a `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#`. This is the same as `https://developer.android.com/reference/kotlin/android/content/Context.html#enforceCallingPermission(kotlin.String,%20kotlin.String)`, except it grants your own permissions if you are not currently processing an IPC. Use with care!

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#enforceCallingOrSelfUriPermission(android.net.Uri,%20kotlin.Int,%20kotlin.String)(uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#!, modeFlags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, message: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)`

If the calling process of an IPC *or you* has not been granted permission to access a specific URI, throw `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#`. This is the same as `https://developer.android.com/reference/kotlin/android/content/Context.html#enforceCallingUriPermission(android.net.Uri,%20kotlin.Int,%20kotlin.String)`, except it grants your own permissions if you are not currently processing an IPC. Use with care!

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#enforceCallingPermission(kotlin.String,%20kotlin.String)(permission: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, message: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?)`

If the calling process of an IPC you are handling has not been granted a particular permission, throw a `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#`. This is basically the same as calling `https://developer.android.com/reference/kotlin/android/content/Context.html#enforcePermission(kotlin.String,%20kotlin.Int,%20kotlin.Int,%20kotlin.String)` with the pid and uid returned by `https://developer.android.com/reference/kotlin/android/os/Binder.html#getCallingPid()` and `https://developer.android.com/reference/kotlin/android/os/Binder.html#getCallingUid()`. One important difference is that if you are not currently processing an IPC, this function will always throw the SecurityException. This is done to protect against accidentally leaking permissions; you can use `https://developer.android.com/reference/kotlin/android/content/Context.html#enforceCallingOrSelfPermission(kotlin.String,%20kotlin.String)` to avoid this protection.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#enforceCallingUriPermission(android.net.Uri,%20kotlin.Int,%20kotlin.String)(uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#!, modeFlags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, message: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)`

If the calling process and uid has not been granted permission to access a specific URI, throw `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#`. This is basically the same as calling `https://developer.android.com/reference/kotlin/android/content/Context.html#enforceUriPermission(android.net.Uri,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.String)` with the pid and uid returned by `https://developer.android.com/reference/kotlin/android/os/Binder.html#getCallingPid()` and `https://developer.android.com/reference/kotlin/android/os/Binder.html#getCallingUid()`. One important difference is that if you are not currently processing an IPC, this function will always throw a SecurityException.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#enforcePermission(kotlin.String,%20kotlin.Int,%20kotlin.Int,%20kotlin.String)(permission: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, pid: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, uid: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, message: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?)`

If the given permission is not allowed for a particular process and user ID running in the system, throw a `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#enforceUriPermission(android.net.Uri,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.String)(uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#!, pid: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, uid: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, modeFlags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, message: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)`

If a particular process and uid has not been granted permission to access a specific URI, throw `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#`. This only checks for permissions that have been explicitly granted -- if the given process/uid has more general access to the URI's content provider then this check will always fail.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#enforceUriPermission(android.net.Uri,%20kotlin.String,%20kotlin.String,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.String)(uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#?, readPermission: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, writePermission: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, pid: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, uid: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, modeFlags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, message: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?)`

Enforce both a Uri and normal permission. This allows you to perform both `https://developer.android.com/reference/kotlin/android/content/Context.html#enforcePermission(kotlin.String,%20kotlin.Int,%20kotlin.Int,%20kotlin.String)` and #enforceUriPermission in one call.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#fileList()()`

Returns an array of strings naming the private files associated with this Context's application package.

<br />

`https://developer.android.com/reference/kotlin/android/content/Context.html#!` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#getApplicationContext()()`

Return the context of the single, global Application object of the current process. This generally should only be used if you need a Context whose lifecycle is separate from the current context, that is tied to the lifetime of the process rather than the current component.

Consider for example how this interacts with `https://developer.android.com/reference/kotlin/android/content/Context.html#registerReceiver(android.content.BroadcastReceiver,%20android.content.IntentFilter)`:

- If used from an Activity context, the receiver is being registered within that activity. This means that you are expected to unregister before the activity is done being destroyed; in fact if you do not do so, the framework will clean up your leaked registration as it removes the activity and log an error. Thus, if you use the Activity context to register a receiver that is static (global to the process, not associated with an Activity instance) then that registration will be removed on you at whatever point the activity you used is destroyed.

- If used from the Context returned here, the receiver is being registered with the global state associated with your application. Thus it will never be unregistered for you. This is necessary if the receiver is associated with static data, not a particular component. However using the ApplicationContext elsewhere can easily lead to serious leaks if you forget to unregister, unbind, etc.

<br />

`https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo.html#!` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#getApplicationInfo()()`

Return the full application info for this context's package.

<br />

`https://developer.android.com/reference/kotlin/android/content/AttributionSource.html#` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#getAttributionSource()()`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#getAttributionTag()()`

Attribution can be used in complex apps to logically separate parts of the app. E.g. a blogging app might also have a instant messaging app built in. In this case two separate tags can for used each sub-feature.

<br />

`https://developer.android.com/reference/kotlin/android/content/Context.html#!` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#getBaseContext()()`

<br />

`https://developer.android.com/reference/kotlin/java/io/File.html#!` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#getCacheDir()()`

Returns the absolute path to the application specific cache directory on the filesystem.

The system will automatically delete files in this directory as disk space is needed elsewhere on the device. The system will always delete older files first, as reported by `https://developer.android.com/reference/kotlin/java/io/File.html#lastModified()`. If desired, you can exert more control over how files are deleted using `https://developer.android.com/reference/kotlin/android/os/storage/StorageManager.html#setCacheBehaviorGroup(java.io.File,%20kotlin.Boolean)` and `https://developer.android.com/reference/kotlin/android/os/storage/StorageManager.html#setCacheBehaviorTombstone(java.io.File,%20kotlin.Boolean)`.

Apps are strongly encouraged to keep their usage of cache space below the quota returned by `https://developer.android.com/reference/kotlin/android/os/storage/StorageManager.html#getCacheQuotaBytes(java.util.UUID)`. If your app goes above this quota, your cached files will be some of the first to be deleted when additional disk space is needed. Conversely, if your app stays under this quota, your cached files will be some of the last to be deleted when additional disk space is needed.

Note that your cache quota will change over time depending on how frequently the user interacts with your app, and depending on how much system-wide disk space is used.

The returned path may change over time if the calling app is moved to an adopted storage device, so only relative paths should be persisted.

Apps require no extra permissions to read or write to the returned path, since this path lives in their private storage.

<br />

`https://developer.android.com/reference/kotlin/java/lang/ClassLoader.html#!` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#getClassLoader()()`

Return a class loader you can use to retrieve classes in this package.

<br />

`https://developer.android.com/reference/kotlin/java/io/File.html#!` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#getCodeCacheDir()()`

Returns the absolute path to the application specific cache directory on the filesystem designed for storing cached code.

The system will delete any files stored in this location both when your specific application is upgraded, and when the entire platform is upgraded.

This location is optimal for storing compiled or optimized code generated by your application at runtime.

The returned path may change over time if the calling app is moved to an adopted storage device, so only relative paths should be persisted.

Apps require no extra permissions to read or write to the returned path, since this path lives in their private storage.

<br />

`https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#!` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#getContentResolver()()`

Return a ContentResolver instance for your application's package.

<br />

`https://developer.android.com/reference/kotlin/java/io/File.html#!` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#getDataDir()()`

Returns the absolute path to the directory on the filesystem where all private files belonging to this app are stored. Apps should not use this path directly; they should instead use `https://developer.android.com/reference/kotlin/android/content/Context.html#getFilesDir()`, `https://developer.android.com/reference/kotlin/android/content/Context.html#getCacheDir()`, `https://developer.android.com/reference/kotlin/android/content/Context.html#getDir(kotlin.String,%20kotlin.Int)`, or other storage APIs on this class.

The returned path may change over time if the calling app is moved to an adopted storage device, so only relative paths should be persisted.

No additional permissions are required for the calling app to read or write files under the returned path.

<br />

`https://developer.android.com/reference/kotlin/java/io/File.html#!` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#getDatabasePath(kotlin.String)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)`

Returns the absolute path on the filesystem where a database created with #openOrCreateDatabase is stored.

The returned path may change over time if the calling app is moved to an adopted storage device, so only relative paths should be persisted.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#getDeviceId()()`

Gets the device ID this context is associated with. Applications can use this method to determine whether they are running on a virtual device and identify that device. The device ID of the host device is `https://developer.android.com/reference/kotlin/android/content/Context.html#DEVICE_ID_DEFAULT:kotlin.Int`

If the underlying device ID is changed by the system, for example, when an `https://developer.android.com/reference/kotlin/android/app/Activity` is moved to a different virtual device, applications can register to listen to changes by calling `https://developer.android.com/reference/kotlin/android/content/Context.html#registerDeviceIdChangeListener(java.util.concurrent.Executor,%20java.util.function.IntConsumer)`.

This method will only return a reliable value for this instance if it was created with `https://developer.android.com/reference/kotlin/android/content/Context.html#createDeviceContext(kotlin.Int)`, or if this instance is a UI or Display Context. Contexts created with `https://developer.android.com/reference/kotlin/android/content/Context.html#createDeviceContext(kotlin.Int)` will have an explicit device association, which will never change, even if the underlying device is closed or is removed. UI Contexts and Display Contexts are already associated with a display, so if the device association is not explicitly given, `https://developer.android.com/reference/kotlin/android/content/Context.html#getDeviceId()` will return the ID of the device associated with the associated display. The system can assign an arbitrary device id value for Contexts not logically associated with a device.

<br />

`https://developer.android.com/reference/kotlin/java/io/File.html#!` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#getDir(kotlin.String,%20kotlin.Int)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, mode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Retrieve, creating if needed, a new directory in which the application can place its own custom data files. You can use the returned File object to create and access files in this directory. Note that files created through a File object will only be accessible by your own application; you can only set the mode of the entire directory, not of individual files.

The returned path may change over time if the calling app is moved to an adopted storage device, so only relative paths should be persisted.

Apps require no extra permissions to read or write to the returned path, since this path lives in their private storage.

<br />

`https://developer.android.com/reference/kotlin/android/view/Display.html#!` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#getDisplay()()`

Get the display this context is associated with. Applications should use this method with `https://developer.android.com/reference/kotlin/android/app/Activity` or a context associated with a `https://developer.android.com/reference/kotlin/android/view/Display.html#` via `https://developer.android.com/reference/kotlin/android/content/Context.html#createDisplayContext(android.view.Display)` to get a display object associated with a Context, or `https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager.html#getDisplay(kotlin.Int)` to get a display object by id.

<br />

`https://developer.android.com/reference/kotlin/java/io/File.html#?` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#getExternalCacheDir()()`

Returns absolute path to application-specific directory on the primary shared/external storage device where the application can place cache files it owns. These files are internal to the application, and not typically visible to the user as media.

This is like `https://developer.android.com/reference/kotlin/android/content/Context.html#getCacheDir()` in that these files will be deleted when the application is uninstalled, however there are some important differences:

- The platform does not always monitor the space available in shared storage, and thus may not automatically delete these files. Apps should always manage the maximum space used in this location. Currently the only time files here will be deleted by the platform is when running on `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#JELLY_BEAN_MR1:kotlin.Int` or later and `https://developer.android.com/reference/kotlin/android/os/Environment.html#isExternalStorageEmulated(java.io.File)` returns true.
- Shared storage may not always be available, since removable media can be ejected by the user. Media state can be checked using `https://developer.android.com/reference/kotlin/android/os/Environment.html#getExternalStorageState(java.io.File)`.
- There is no security enforced with these files. For example, any application holding `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#WRITE_EXTERNAL_STORAGE:kotlin.String` can write to these files.

If a shared storage device is emulated (as determined by `https://developer.android.com/reference/kotlin/android/os/Environment.html#isExternalStorageEmulated(java.io.File)`), its contents are backed by a private user data partition, which means there is little benefit to storing data here instead of the private directory returned by `https://developer.android.com/reference/kotlin/android/content/Context.html#getCacheDir()`.

Starting in `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#KITKAT:kotlin.Int`, no permissions are required to read or write to the returned path; it's always accessible to the calling app. This only applies to paths generated for package name of the calling application. To access paths belonging to other packages, `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#WRITE_EXTERNAL_STORAGE:kotlin.String` and/or `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_EXTERNAL_STORAGE:kotlin.String` are required.

On devices with multiple users (as described by `https://developer.android.com/reference/kotlin/android/os/UserManager.html#`), each user has their own isolated shared storage. Applications only have access to the shared storage for the user they're running as.

The returned path may change over time if different shared storage media is inserted, so only relative paths should be persisted.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/java/io/File.html#!>!` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#getExternalCacheDirs()()`

Returns absolute paths to application-specific directories on all shared/external storage devices where the application can place cache files it owns. These files are internal to the application, and not typically visible to the user as media.

This is like `https://developer.android.com/reference/kotlin/android/content/Context.html#getCacheDir()` in that these files will be deleted when the application is uninstalled, however there are some important differences:

- The platform does not always monitor the space available in shared storage, and thus may not automatically delete these files. Apps should always manage the maximum space used in this location. Currently the only time files here will be deleted by the platform is when running on `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#JELLY_BEAN_MR1:kotlin.Int` or later and `https://developer.android.com/reference/kotlin/android/os/Environment.html#isExternalStorageEmulated(java.io.File)` returns true.
- Shared storage may not always be available, since removable media can be ejected by the user. Media state can be checked using `https://developer.android.com/reference/kotlin/android/os/Environment.html#getExternalStorageState(java.io.File)`.
- There is no security enforced with these files. For example, any application holding `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#WRITE_EXTERNAL_STORAGE:kotlin.String` can write to these files.

If a shared storage device is emulated (as determined by `https://developer.android.com/reference/kotlin/android/os/Environment.html#isExternalStorageEmulated(java.io.File)`), its contents are backed by a private user data partition, which means there is little benefit to storing data here instead of the private directory returned by `https://developer.android.com/reference/kotlin/android/content/Context.html#getCacheDir()`.

Shared storage devices returned here are considered a stable part of the device, including physical media slots under a protective cover. The returned paths do not include transient devices, such as USB flash drives connected to handheld devices.

An application may store data on any or all of the returned devices. For example, an app may choose to store large files on the device with the most available space, as measured by `https://developer.android.com/reference/kotlin/android/os/StatFs.html#`.

No additional permissions are required for the calling app to read or write files under the returned path. Write access outside of these paths on secondary external storage devices is not available.

The returned paths may change over time if different shared storage media is inserted, so only relative paths should be persisted.

<br />

`https://developer.android.com/reference/kotlin/java/io/File.html#?` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#getExternalFilesDir(kotlin.String)(type: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?)`

Returns the absolute path to the directory on the primary shared/external storage device where the application can place persistent files it owns. These files are internal to the applications, and not typically visible to the user as media.

This is like `https://developer.android.com/reference/kotlin/android/content/Context.html#getFilesDir()` in that these files will be deleted when the application is uninstalled, however there are some important differences:

- Shared storage may not always be available, since removable media can be ejected by the user. Media state can be checked using `https://developer.android.com/reference/kotlin/android/os/Environment.html#getExternalStorageState(java.io.File)`.
- There is no security enforced with these files. For example, any application holding `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#WRITE_EXTERNAL_STORAGE:kotlin.String` can write to these files.

If a shared storage device is emulated (as determined by `https://developer.android.com/reference/kotlin/android/os/Environment.html#isExternalStorageEmulated(java.io.File)`), its contents are backed by a private user data partition, which means there is little benefit to storing data here instead of the private directories returned by `https://developer.android.com/reference/kotlin/android/content/Context.html#getFilesDir()`, etc.

Starting in `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#KITKAT:kotlin.Int`, no permissions are required to read or write to the returned path; it's always accessible to the calling app. This only applies to paths generated for package name of the calling application. To access paths belonging to other packages, `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#WRITE_EXTERNAL_STORAGE:kotlin.String` and/or `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_EXTERNAL_STORAGE:kotlin.String` are required.

On devices with multiple users (as described by `https://developer.android.com/reference/kotlin/android/os/UserManager.html#`), each user has their own isolated shared storage. Applications only have access to the shared storage for the user they're running as.

The returned path may change over time if different shared storage media is inserted, so only relative paths should be persisted.

Here is an example of typical code to manipulate a file in an application's shared storage:

If you supply a non-null type to this function, the returned file will be a path to a sub-directory of the given type. Though these files are not automatically scanned by the media scanner, you can explicitly add them to the media database with `https://developer.android.com/reference/kotlin/android/media/MediaScannerConnection.html#scanFile(android.content.Context,%20kotlin.Array,%20kotlin.Array,%20android.media.MediaScannerConnection.OnScanCompletedListener)`. Note that this is not the same as `https://developer.android.com/reference/kotlin/android/os/Environment.html#getExternalStoragePublicDirectory(kotlin.String)`, which provides directories of media shared by all applications. The directories returned here are owned by the application, and their contents will be removed when the application is uninstalled. Unlike `https://developer.android.com/reference/kotlin/android/os/Environment.html#getExternalStoragePublicDirectory(kotlin.String)`, the directory returned here will be automatically created for you.

Here is an example of typical code to manipulate a picture in an application's shared storage and add it to the media database:

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/java/io/File.html#!>!` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#getExternalFilesDirs(kotlin.String)(type: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)`

Returns absolute paths to application-specific directories on all shared/external storage devices where the application can place persistent files it owns. These files are internal to the application, and not typically visible to the user as media.

This is like `https://developer.android.com/reference/kotlin/android/content/Context.html#getFilesDir()` in that these files will be deleted when the application is uninstalled, however there are some important differences:

- Shared storage may not always be available, since removable media can be ejected by the user. Media state can be checked using `https://developer.android.com/reference/kotlin/android/os/Environment.html#getExternalStorageState(java.io.File)`.
- There is no security enforced with these files. For example, any application holding `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#WRITE_EXTERNAL_STORAGE:kotlin.String` can write to these files.

If a shared storage device is emulated (as determined by `https://developer.android.com/reference/kotlin/android/os/Environment.html#isExternalStorageEmulated(java.io.File)`), its contents are backed by a private user data partition, which means there is little benefit to storing data here instead of the private directories returned by `https://developer.android.com/reference/kotlin/android/content/Context.html#getFilesDir()`, etc.

Shared storage devices returned here are considered a stable part of the device, including physical media slots under a protective cover. The returned paths do not include transient devices, such as USB flash drives connected to handheld devices.

An application may store data on any or all of the returned devices. For example, an app may choose to store large files on the device with the most available space, as measured by `https://developer.android.com/reference/kotlin/android/os/StatFs.html#`.

No additional permissions are required for the calling app to read or write files under the returned path. Write access outside of these paths on secondary external storage devices is not available.

The returned path may change over time if different shared storage media is inserted, so only relative paths should be persisted.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/java/io/File.html#!>!` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#getExternalMediaDirs()()`

Returns absolute paths to application-specific directories on all shared/external storage devices where the application can place media files. These files are scanned and made available to other apps through `https://developer.android.com/reference/kotlin/android/provider/MediaStore.html#`.

This is like `https://developer.android.com/reference/kotlin/android/content/Context.html#getExternalFilesDirs(kotlin.String)` in that these files will be deleted when the application is uninstalled, however there are some important differences:

- Shared storage may not always be available, since removable media can be ejected by the user. Media state can be checked using `https://developer.android.com/reference/kotlin/android/os/Environment.html#getExternalStorageState(java.io.File)`.
- There is no security enforced with these files. For example, any application holding `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#WRITE_EXTERNAL_STORAGE:kotlin.String` can write to these files.

Shared storage devices returned here are considered a stable part of the device, including physical media slots under a protective cover. The returned paths do not include transient devices, such as USB flash drives connected to handheld devices.

An application may store data on any or all of the returned devices. For example, an app may choose to store large files on the device with the most available space, as measured by `https://developer.android.com/reference/kotlin/android/os/StatFs.html#`.

No additional permissions are required for the calling app to read or write files under the returned path. Write access outside of these paths on secondary external storage devices is not available.

The returned paths may change over time if different shared storage media is inserted, so only relative paths should be persisted.

<br />

`https://developer.android.com/reference/kotlin/java/io/File.html#!` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#getFileStreamPath(kotlin.String)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)`

Returns the absolute path on the filesystem where a file created with `https://developer.android.com/reference/kotlin/android/content/Context.html#openFileOutput(kotlin.String,%20kotlin.Int)` is stored.

The returned path may change over time if the calling app is moved to an adopted storage device, so only relative paths should be persisted.

<br />

`https://developer.android.com/reference/kotlin/java/io/File.html#!` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#getFilesDir()()`

Returns the absolute path to the directory on the filesystem where files created with `https://developer.android.com/reference/kotlin/android/content/Context.html#openFileOutput(kotlin.String,%20kotlin.Int)` are stored.

The returned path may change over time if the calling app is moved to an adopted storage device, so only relative paths should be persisted.

No additional permissions are required for the calling app to read or write files under the returned path.

<br />

`https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#!` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#getMainExecutor()()`

Return an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that will run enqueued tasks on the main thread associated with this context. This is the thread used to dispatch calls to application components (activities, services, etc).

<br />

`https://developer.android.com/reference/kotlin/android/os/Looper.html#!` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#getMainLooper()()`

Return the Looper for the main thread of the current process. This is the thread used to dispatch calls to application components (activities, services, etc).

By definition, this method returns the same result as would be obtained by calling `https://developer.android.com/reference/kotlin/android/os/Looper.html#getMainLooper()`.

<br />

`https://developer.android.com/reference/kotlin/java/io/File.html#!` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#getNoBackupFilesDir()()`

Returns the absolute path to the directory on the filesystem similar to `https://developer.android.com/reference/kotlin/android/content/Context.html#getFilesDir()`. The difference is that files placed under this directory will be excluded from automatic backup to remote storage. See `https://developer.android.com/reference/kotlin/android/app/backup/BackupAgent` for a full discussion of the automatic backup mechanism in Android.

The returned path may change over time if the calling app is moved to an adopted storage device, so only relative paths should be persisted.

No additional permissions are required for the calling app to read or write files under the returned path.

<br />

`https://developer.android.com/reference/kotlin/java/io/File.html#!` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#getObbDir()()`

Return the primary shared/external storage directory where this application's OBB files (if there are any) can be found. Note if the application does not have any OBB files, this directory may not exist.

This is like `https://developer.android.com/reference/kotlin/android/content/Context.html#getFilesDir()` in that these files will be deleted when the application is uninstalled, however there are some important differences:

- Shared storage may not always be available, since removable media can be ejected by the user. Media state can be checked using `https://developer.android.com/reference/kotlin/android/os/Environment.html#getExternalStorageState(java.io.File)`.
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

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/java/io/File.html#!>!` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#getObbDirs()()`

Returns absolute paths to application-specific directories on all shared/external storage devices where the application's OBB files (if there are any) can be found. Note if the application does not have any OBB files, these directories may not exist.

This is like `https://developer.android.com/reference/kotlin/android/content/Context.html#getFilesDir()` in that these files will be deleted when the application is uninstalled, however there are some important differences:

- Shared storage may not always be available, since removable media can be ejected by the user. Media state can be checked using `https://developer.android.com/reference/kotlin/android/os/Environment.html#getExternalStorageState(java.io.File)`.
- There is no security enforced with these files. For example, any application holding `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#WRITE_EXTERNAL_STORAGE:kotlin.String` can write to these files.

Shared storage devices returned here are considered a stable part of the device, including physical media slots under a protective cover. The returned paths do not include transient devices, such as USB flash drives connected to handheld devices.

An application may store data on any or all of the returned devices. For example, an app may choose to store large files on the device with the most available space, as measured by `https://developer.android.com/reference/kotlin/android/os/StatFs.html#`.

No additional permissions are required for the calling app to read or write files under the returned path. Write access outside of these paths on secondary external storage devices is not available.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#getOpPackageName()()`

Return the package name that should be used for `https://developer.android.com/reference/kotlin/android/app/AppOpsManager` calls from this context, so that app ops manager's uid verification will work with the name.

This is not generally intended for third party application developers.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#getPackageCodePath()()`

Return the full path to this context's primary Android package. The Android package is a ZIP file which contains application's primary code and assets.

Note: this is not generally useful for applications, since they should not be directly accessing the file system.

<br />

`https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#!` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#getPackageManager()()`

Return PackageManager instance to find global package information.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#getPackageName()()`

Return the name of this application's package.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#getPackageResourcePath()()`

Return the full path to this context's primary Android package. The Android package is a ZIP file which contains the application's primary resources.

Note: this is not generally useful for applications, since they should not be directly accessing the file system.

<br />

`https://developer.android.com/reference/kotlin/android/content/ContextParams.html#?` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#getParams()()`

Return the set of parameters which this Context was created with, if it was created via `https://developer.android.com/reference/kotlin/android/content/Context.html#createContext(android.content.ContextParams)`.

<br />

`https://developer.android.com/reference/kotlin/android/content/SharedPreferences.html#!` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#getSharedPreferences(kotlin.String,%20kotlin.Int)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, mode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Retrieve and hold the contents of the preferences file 'name', returning a SharedPreferences through which you can retrieve and modify its values. Only one instance of the SharedPreferences object is returned to any callers for the same name, meaning they will see each other's edits as soon as they are made.

This method is thread-safe.

If the preferences directory does not already exist, it will be created when this method is called.

If a preferences file by this name does not exist, it will be created when you retrieve an editor (`https://developer.android.com/reference/kotlin/android/content/SharedPreferences.html#edit()`) and then commit changes (`https://developer.android.com/reference/kotlin/android/content/SharedPreferences.Editor.html#commit()` or `https://developer.android.com/reference/kotlin/android/content/SharedPreferences.Editor.html#apply()`).

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#getSystemServiceName(java.lang.Class)(serviceClass: https://developer.android.com/reference/kotlin/java/lang/Class.html#<*>)`

Gets the name of the system-level service that is represented by the specified class.

<br />

`https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#!` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#getWallpaper()()`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#getWallpaperDesiredMinimumHeight()()`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#getWallpaperDesiredMinimumWidth()()`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#grantUriPermission(kotlin.String,%20android.net.Uri,%20kotlin.Int)(toPackage: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#!, modeFlags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Grant permission to access a specific Uri to another package, regardless of whether that package has general permission to access the Uri's content provider. This can be used to grant specific, temporary permissions, typically in response to user interaction (such as the user opening an attachment that you would like someone else to display).

Normally you should use `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_GRANT_READ_URI_PERMISSION:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_GRANT_WRITE_URI_PERMISSION:kotlin.Int` with the Intent being used to start an activity instead of this function directly. If you use this function directly, you should be sure to call #revokeUriPermission when the target should no longer be allowed to access it.

To succeed, the content provider owning the Uri must have set the `https://developer.android.com/reference/kotlin/android/R.styleable.html#AndroidManifestProvider_grantUriPermissions:kotlin.Int` attribute in its manifest or included the `https://developer.android.com/reference/kotlin/android/R.styleable.html#AndroidManifestGrantUriPermission:kotlin.IntArray` tag.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#isDeviceProtectedStorage()()`

Indicates if the storage APIs of this Context are backed by device-protected storage.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#isRestricted()()`

Indicates whether this Context is restricted.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#isUiContext()()`

Returns `true` if the context is a UI context which can access UI components such as `https://developer.android.com/reference/kotlin/android/view/WindowManager.html#`, `https://developer.android.com/reference/kotlin/android/view/LayoutInflater.html#` or `https://developer.android.com/reference/kotlin/android/app/WallpaperManager`. Accessing UI components from non-UI contexts throws `https://developer.android.com/reference/kotlin/android/os/strictmode/Violation.html#` if `https://developer.android.com/reference/kotlin/android/os/StrictMode.VmPolicy.Builder.html#detectIncorrectContextUse()` is enabled.

Examples of UI contexts are an `https://developer.android.com/reference/kotlin/android/app/Activity`, a context created from `https://developer.android.com/reference/kotlin/android/content/Context.html#createWindowContext(kotlin.Int,%20android.os.Bundle)` or `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService.html#`

Note that even if it is allowed programmatically, it is not suggested to override this method to bypass `https://developer.android.com/reference/kotlin/android/os/strictmode/IncorrectContextUseViolation.html#` verification.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#moveDatabaseFrom(android.content.Context,%20kotlin.String)(sourceContext: https://developer.android.com/reference/kotlin/android/content/Context.html#!, name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)`

Move an existing database file from the given source storage context to this context. This is typically used to migrate data between storage locations after an upgrade, such as migrating to device protected storage.

The database must be closed before being moved.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#moveSharedPreferencesFrom(android.content.Context,%20kotlin.String)(sourceContext: https://developer.android.com/reference/kotlin/android/content/Context.html#!, name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)`

Move an existing shared preferences file from the given source storage context to this context. This is typically used to migrate data between storage locations after an upgrade, such as moving to device protected storage.

<br />

`https://developer.android.com/reference/kotlin/java/io/FileInputStream.html#!` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#openFileInput(kotlin.String)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)`

Open a private file associated with this Context's application package for reading.

<br />

`https://developer.android.com/reference/kotlin/java/io/FileOutputStream.html#!` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#openFileOutput(kotlin.String,%20kotlin.Int)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, mode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Open a private file associated with this Context's application package for writing. Creates the file if it doesn't already exist.

No additional permissions are required for the calling app to read or write the returned file.

<br />

`https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase.html#!` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#openOrCreateDatabase(kotlin.String,%20kotlin.Int,%20android.database.sqlite.SQLiteDatabase.CursorFactory)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, mode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, factory: https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase.CursorFactory.html#!)`

Open a new private SQLiteDatabase associated with this Context's application package. Create the database file if it doesn't exist.

<br />

`https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase.html#!` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#openOrCreateDatabase(kotlin.String,%20kotlin.Int,%20android.database.sqlite.SQLiteDatabase.CursorFactory,%20android.database.DatabaseErrorHandler)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, mode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, factory: https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase.CursorFactory.html#!, errorHandler: https://developer.android.com/reference/kotlin/android/database/DatabaseErrorHandler.html#?)`

Open a new private SQLiteDatabase associated with this Context's application package. Creates the database file if it doesn't exist.

Accepts input param: a concrete instance of `https://developer.android.com/reference/kotlin/android/database/DatabaseErrorHandler.html#` to be used to handle corruption when sqlite reports database corruption.

<br />

`https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#!` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#peekWallpaper()()`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#rebindService(android.content.ServiceConnection,%20android.content.Context.BindServiceFlags)(conn: https://developer.android.com/reference/kotlin/android/content/ServiceConnection.html#, flags: https://developer.android.com/reference/kotlin/android/content/Context.BindServiceFlags.html#)`

Rebind an application service with updated bind service flags

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#registerComponentCallbacks(android.content.ComponentCallbacks)(callback: https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks.html#!)`

Add a new `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks.html#` to the base application of the Context, which will be called at the same times as the ComponentCallbacks methods of activities and other components are called. Note that you *must* be sure to use `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#unregisterComponentCallbacks(android.content.ComponentCallbacks)` when appropriate in the future; this will not be removed for you.

After `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#TIRAMISU:kotlin.Int`, the `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks.html#` will be registered to `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#getBaseContext()`, and can be only used after `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#attachBaseContext(android.content.Context)`. Users can still call to `getApplicationContext().registerComponentCallbacks(ComponentCallbacks)` to add `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks.html#` to the base application.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#registerDeviceIdChangeListener(java.util.concurrent.Executor,%20java.util.function.IntConsumer)(executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, listener: https://developer.android.com/reference/kotlin/java/util/function/IntConsumer.html#)`

Adds a new device ID changed listener to the `Context`, which will be called when the device association is changed by the system.

The callback can be called when an app is moved to a different device and the `Context` is not explicitly associated with a specific device.

When an application receives a device id update callback, this Context is guaranteed to also have an updated display ID(if any) and `https://developer.android.com/reference/kotlin/android/content/res/Configuration.html#`.

<br />

<br />

`https://developer.android.com/reference/kotlin/android/content/Intent.html#?` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#registerReceiver(android.content.BroadcastReceiver,%20android.content.IntentFilter)(receiver: https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#?, filter: https://developer.android.com/reference/kotlin/android/content/IntentFilter.html#!)`

Register a BroadcastReceiver to be run in the main activity thread. The receiver will be called with any broadcast Intent that matches filter, in the main application thread.

The system may broadcast Intents that are "sticky" -- these stay around after the broadcast has finished, to be sent to any later registrations. If your IntentFilter matches one of these sticky Intents, that Intent will be returned by this function **and** sent to your receiver as if it had just been broadcast.

There may be multiple sticky Intents that match filter, in which case each of these will be sent to receiver. In this case, only one of these can be returned directly by the function; which of these that is returned is arbitrarily decided by the system.

If you know the Intent you are registering for is sticky, you can supply null for your receiver. In this case, no receiver is registered -- the function simply returns the sticky Intent that matches filter. In the case of multiple matches, the same rules as described above apply.

See `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#` for more information on Intent broadcasts.

As of `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#UPSIDE_DOWN_CAKE:kotlin.Int`, the system can [place context-registered broadcasts in a queue while the app is in the](https://developer.android.com/develop/background-work/background-tasks/broadcasts#android-14) [cached state](https://developer.android.com/guide/components/activities/process-lifecycle). When the app leaves the cached state, such as returning to the foreground, the system delivers any queued broadcasts. Multiple instances of certain broadcasts might be merged into one broadcast.

As of `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#ICE_CREAM_SANDWICH:kotlin.Int`, receivers registered with this method will correctly respect the `https://developer.android.com/reference/kotlin/android/content/Intent.html#setPackage(kotlin.String)` specified for an Intent being broadcast. Prior to that, it would be ignored and delivered to all matching registered receivers. Be careful if using this for security.

For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#UPSIDE_DOWN_CAKE:kotlin.Int`, either `https://developer.android.com/reference/kotlin/android/content/Context.html#RECEIVER_EXPORTED:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/content/Context.html#RECEIVER_NOT_EXPORTED:kotlin.Int` must be specified if the receiver is not being registered for [system broadcasts](https://developer.android.com/guide/components/broadcasts#system-broadcasts) or a `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#` will be thrown. See `https://developer.android.com/reference/kotlin/android/content/Context.html#registerReceiver(android.content.BroadcastReceiver,%20android.content.IntentFilter,%20kotlin.Int)` to register a receiver with flags.

Note: this method *cannot be called from a `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#` component;* that is, from a BroadcastReceiver that is declared in an application's manifest. It is okay, however, to call this method from another BroadcastReceiver that has itself been registered at run time with #registerReceiver, since the lifetime of such a registered BroadcastReceiver is tied to the object that registered it.

<br />

`https://developer.android.com/reference/kotlin/android/content/Intent.html#?` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#registerReceiver(android.content.BroadcastReceiver,%20android.content.IntentFilter,%20kotlin.Int)(receiver: https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#?, filter: https://developer.android.com/reference/kotlin/android/content/IntentFilter.html#!, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Register to receive intent broadcasts, with the receiver optionally being exposed to Instant Apps. See `https://developer.android.com/reference/kotlin/android/content/Context.html#registerReceiver(android.content.BroadcastReceiver,%20android.content.IntentFilter)` for more information. By default Instant Apps cannot interact with receivers in other applications, this allows you to expose a receiver that Instant Apps can interact with.

See `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#` for more information on Intent broadcasts.

As of `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#UPSIDE_DOWN_CAKE:kotlin.Int`, the system can [place context-registered broadcasts in a queue while the app is in the](https://developer.android.com/develop/background-work/background-tasks/broadcasts#android-14) [cached state](https://developer.android.com/guide/components/activities/process-lifecycle). When the app leaves the cached state, such as returning to the foreground, the system delivers any queued broadcasts. Multiple instances of certain broadcasts might be merged into one broadcast.

As of `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#ICE_CREAM_SANDWICH:kotlin.Int`, receivers registered with this method will correctly respect the `https://developer.android.com/reference/kotlin/android/content/Intent.html#setPackage(kotlin.String)` specified for an Intent being broadcast. Prior to that, it would be ignored and delivered to all matching registered receivers. Be careful if using this for security.

<br />

`https://developer.android.com/reference/kotlin/android/content/Intent.html#?` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#registerReceiver(android.content.BroadcastReceiver,%20android.content.IntentFilter,%20kotlin.String,%20android.os.Handler)(receiver: https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#?, filter: https://developer.android.com/reference/kotlin/android/content/IntentFilter.html#!, broadcastPermission: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, scheduler: https://developer.android.com/reference/kotlin/android/os/Handler.html#?)`

Register to receive intent broadcasts, to run in the context of scheduler. See `https://developer.android.com/reference/kotlin/android/content/Context.html#registerReceiver(android.content.BroadcastReceiver,%20android.content.IntentFilter)` for more information. This allows you to enforce permissions on who can broadcast intents to your receiver, or have the receiver run in a different thread than the main application thread.

See `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#` for more information on Intent broadcasts.

As of `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#UPSIDE_DOWN_CAKE:kotlin.Int`, the system can [place context-registered broadcasts in a queue while the app is in the](https://developer.android.com/develop/background-work/background-tasks/broadcasts#android-14) [cached state](https://developer.android.com/guide/components/activities/process-lifecycle). When the app leaves the cached state, such as returning to the foreground, the system delivers any queued broadcasts. Multiple instances of certain broadcasts might be merged into one broadcast.

As of `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#ICE_CREAM_SANDWICH:kotlin.Int`, receivers registered with this method will correctly respect the `https://developer.android.com/reference/kotlin/android/content/Intent.html#setPackage(kotlin.String)` specified for an Intent being broadcast. Prior to that, it would be ignored and delivered to all matching registered receivers. Be careful if using this for security.

For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#UPSIDE_DOWN_CAKE:kotlin.Int`, either `https://developer.android.com/reference/kotlin/android/content/Context.html#RECEIVER_EXPORTED:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/content/Context.html#RECEIVER_NOT_EXPORTED:kotlin.Int` must be specified if the receiver is not being registered for [system broadcasts](https://developer.android.com/guide/components/broadcasts#system-broadcasts) or a `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#` will be thrown. See `https://developer.android.com/reference/kotlin/android/content/Context.html#registerReceiver(android.content.BroadcastReceiver,%20android.content.IntentFilter,%20kotlin.String,%20android.os.Handler,%20kotlin.Int)` to register a receiver with flags.

<br />

`https://developer.android.com/reference/kotlin/android/content/Intent.html#?` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#registerReceiver(android.content.BroadcastReceiver,%20android.content.IntentFilter,%20kotlin.String,%20android.os.Handler,%20kotlin.Int)(receiver: https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#?, filter: https://developer.android.com/reference/kotlin/android/content/IntentFilter.html#!, broadcastPermission: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, scheduler: https://developer.android.com/reference/kotlin/android/os/Handler.html#?, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Register to receive intent broadcasts, to run in the context of scheduler. See `https://developer.android.com/reference/kotlin/android/content/Context.html#registerReceiver(android.content.BroadcastReceiver,%20android.content.IntentFilter,%20kotlin.Int)` and `https://developer.android.com/reference/kotlin/android/content/Context.html#registerReceiver(android.content.BroadcastReceiver,%20android.content.IntentFilter,%20kotlin.String,%20android.os.Handler)` for more information.

See `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#` for more information on Intent broadcasts.

As of `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#UPSIDE_DOWN_CAKE:kotlin.Int`, the system can [place context-registered broadcasts in a queue while the app is in the](https://developer.android.com/develop/background-work/background-tasks/broadcasts#android-14) [cached state](https://developer.android.com/guide/components/activities/process-lifecycle). When the app leaves the cached state, such as returning to the foreground, the system delivers any queued broadcasts. Multiple instances of certain broadcasts might be merged into one broadcast.

As of `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#ICE_CREAM_SANDWICH:kotlin.Int`, receivers registered with this method will correctly respect the `https://developer.android.com/reference/kotlin/android/content/Intent.html#setPackage(kotlin.String)` specified for an Intent being broadcast. Prior to that, it would be ignored and delivered to all matching registered receivers. Be careful if using this for security.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#removeStickyBroadcast(android.content.Intent)(intent: https://developer.android.com/reference/kotlin/android/content/Intent.html#!)`

Remove the data previously sent with #sendStickyBroadcast, so that it is as if the sticky broadcast had never happened. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BROADCAST_STICKY:kotlin.String`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#removeStickyBroadcastAsUser(android.content.Intent,%20android.os.UserHandle)(intent: https://developer.android.com/reference/kotlin/android/content/Intent.html#!, user: https://developer.android.com/reference/kotlin/android/os/UserHandle.html#!)`

Version of `https://developer.android.com/reference/kotlin/android/content/Context.html#removeStickyBroadcast(android.content.Intent)` that allows you to specify the user the broadcast will be sent to. This is not available to applications that are not pre-installed on the system image.

You must hold the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BROADCAST_STICKY:kotlin.String` permission in order to use this API. If you do not hold that permission, `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#` will be thrown. 
Requires android.Manifest.permission.INTERACT_ACROSS_USERS and `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BROADCAST_STICKY:kotlin.String`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#revokeSelfPermissionsOnKill(kotlin.collections.MutableCollection)(permissions: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>)`

Triggers the revocation of one or more permissions for the calling package. A package is only able to revoke runtime permissions. If a permission is not currently granted, it is ignored and will not get revoked (even if later granted by the user). Ultimately, you should never make assumptions about a permission status as users may grant or revoke them at any time.

Background permissions which have no corresponding foreground permission still granted once the revocation is effective will also be revoked.

The revocation happens asynchronously and kills all processes running in the calling UID. It will be triggered once it is safe to do so. In particular, it will not be triggered as long as the package remains in the foreground, or has any active manifest components (e.g. when another app is accessing a content provider in the package).

If you want to revoke the permissions right away, you could call `System.exit()` in `Handler.postDelayed` with a delay to allow completion of async IPC, But `System.exit()` could affect other apps that are accessing your app at the moment. For example, apps accessing a content provider in your app will all crash.

Note that the settings UI shows a permission group as granted as long as at least one permission in the group is granted. If you want the user to observe the revocation in the settings, you should revoke every permission in the target group. To learn the current list of permissions in a group, you may use `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getGroupOfPlatformPermission(kotlin.String,%20java.util.concurrent.Executor,%20java.util.function.Consumer)` and `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getPlatformPermissionsForGroup(kotlin.String,%20java.util.concurrent.Executor,%20java.util.function.Consumer)`. This list of permissions may evolve over time, so it is recommended to check whether it contains any permission you wish to retain before trying to revoke an entire group.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#revokeUriPermission(android.net.Uri,%20kotlin.Int)(uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#!, modeFlags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Remove all permissions to access a particular content provider Uri that were previously added with `https://developer.android.com/reference/kotlin/android/content/Context.html#grantUriPermission(kotlin.String,%20android.net.Uri,%20kotlin.Int)` or *any other* mechanism. The given Uri will match all previously granted Uris that are the same or a sub-path of the given Uri. That is, revoking "content://foo/target" will revoke both "content://foo/target" and "content://foo/target/sub", but not "content://foo". It will not remove any prefix grants that exist at a higher level.

Prior to `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#LOLLIPOP:kotlin.Int`, if you did not have regular permission access to a Uri, but had received access to it through a specific Uri permission grant, you could not revoke that grant with this function and a `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#` would be thrown. As of `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#LOLLIPOP:kotlin.Int`, this function will not throw a security exception, but will remove whatever permission grants to the Uri had been given to the app (or none).

Unlike `https://developer.android.com/reference/kotlin/android/content/Context.html#revokeUriPermission(kotlin.String,%20android.net.Uri,%20kotlin.Int)`, this method impacts all permission grants matching the given Uri, for any package they had been granted to, through any mechanism this had happened (such as indirectly through the clipboard, activity launch, service start, etc). That means this can be potentially dangerous to use, as it can revoke grants that another app could be strongly expecting to stick around.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#revokeUriPermission(kotlin.String,%20android.net.Uri,%20kotlin.Int)(targetPackage: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#!, modeFlags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Remove permissions to access a particular content provider Uri that were previously added with `https://developer.android.com/reference/kotlin/android/content/Context.html#grantUriPermission(kotlin.String,%20android.net.Uri,%20kotlin.Int)` for a specific target package. The given Uri will match all previously granted Uris that are the same or a sub-path of the given Uri. That is, revoking "content://foo/target" will revoke both "content://foo/target" and "content://foo/target/sub", but not "content://foo". It will not remove any prefix grants that exist at a higher level.

Unlike `https://developer.android.com/reference/kotlin/android/content/Context.html#revokeUriPermission(android.net.Uri,%20kotlin.Int)`, this method will *only* revoke permissions that had been explicitly granted through `https://developer.android.com/reference/kotlin/android/content/Context.html#grantUriPermission(kotlin.String,%20android.net.Uri,%20kotlin.Int)` and only for the package specified. Any matching grants that have happened through other mechanisms (clipboard, activity launching, service starting, etc) will not be removed.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#sendBroadcast(android.content.Intent)(intent: https://developer.android.com/reference/kotlin/android/content/Intent.html#!)`

Broadcast the given intent to all interested BroadcastReceivers. This call is asynchronous; it returns immediately, and you will continue executing while the receivers are run. No results are propagated from receivers and receivers can not abort the broadcast. If you want to allow receivers to propagate results or abort the broadcast, you must send an ordered broadcast using `https://developer.android.com/reference/kotlin/android/content/Context.html#sendOrderedBroadcast(android.content.Intent,%20kotlin.String)`.

See `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#` for more information on Intent broadcasts.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#sendBroadcast(android.content.Intent,%20kotlin.String)(intent: https://developer.android.com/reference/kotlin/android/content/Intent.html#!, receiverPermission: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?)`

Broadcast the given intent to all interested BroadcastReceivers, allowing an optional required permission to be enforced. This call is asynchronous; it returns immediately, and you will continue executing while the receivers are run. No results are propagated from receivers and receivers can not abort the broadcast. If you want to allow receivers to propagate results or abort the broadcast, you must send an ordered broadcast using `https://developer.android.com/reference/kotlin/android/content/Context.html#sendOrderedBroadcast(android.content.Intent,%20kotlin.String)`.

See `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#` for more information on Intent broadcasts.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#sendBroadcast(android.content.Intent,%20kotlin.String,%20android.os.Bundle)(intent: https://developer.android.com/reference/kotlin/android/content/Intent.html#, receiverPermission: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, options: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?)`

Broadcast the given intent to all interested BroadcastReceivers, allowing an optional required permission to be enforced. This call is asynchronous; it returns immediately, and you will continue executing while the receivers are run. No results are propagated from receivers and receivers can not abort the broadcast. If you want to allow receivers to propagate results or abort the broadcast, you must send an ordered broadcast using `https://developer.android.com/reference/kotlin/android/content/Context.html#sendOrderedBroadcast(android.content.Intent,%20kotlin.String)`.

See `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#` for more information on Intent broadcasts.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#sendBroadcastAsUser(android.content.Intent,%20android.os.UserHandle)(intent: https://developer.android.com/reference/kotlin/android/content/Intent.html#!, user: https://developer.android.com/reference/kotlin/android/os/UserHandle.html#!)`

Version of `https://developer.android.com/reference/kotlin/android/content/Context.html#sendBroadcast(android.content.Intent)` that allows you to specify the user the broadcast will be sent to. This is not available to applications that are not pre-installed on the system image. 
Requires android.Manifest.permission.INTERACT_ACROSS_USERS

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#sendBroadcastAsUser(android.content.Intent,%20android.os.UserHandle,%20kotlin.String)(intent: https://developer.android.com/reference/kotlin/android/content/Intent.html#!, user: https://developer.android.com/reference/kotlin/android/os/UserHandle.html#!, receiverPermission: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?)`

Version of `https://developer.android.com/reference/kotlin/android/content/Context.html#sendBroadcast(android.content.Intent,%20kotlin.String)` that allows you to specify the user the broadcast will be sent to. This is not available to applications that are not pre-installed on the system image. 
Requires android.Manifest.permission.INTERACT_ACROSS_USERS

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#sendOrderedBroadcast(android.content.Intent,%20kotlin.Int,%20kotlin.String,%20kotlin.String,%20android.content.BroadcastReceiver,%20android.os.Handler,%20kotlin.String,%20android.os.Bundle,%20android.os.Bundle)(intent: https://developer.android.com/reference/kotlin/android/content/Intent.html#, initialCode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, receiverPermission: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, receiverAppOp: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, resultReceiver: https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#?, scheduler: https://developer.android.com/reference/kotlin/android/os/Handler.html#?, initialData: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, initialExtras: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?, options: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?)`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#sendOrderedBroadcast(android.content.Intent,%20kotlin.String)(intent: https://developer.android.com/reference/kotlin/android/content/Intent.html#!, receiverPermission: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?)`

Broadcast the given intent to all interested BroadcastReceivers, delivering them one at a time to allow more preferred receivers to consume the broadcast before it is delivered to less preferred receivers. This call is asynchronous; it returns immediately, and you will continue executing while the receivers are run.

See `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#` for more information on Intent broadcasts.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#sendOrderedBroadcast(android.content.Intent,%20kotlin.String,%20android.content.BroadcastReceiver,%20android.os.Handler,%20kotlin.Int,%20kotlin.String,%20android.os.Bundle)(intent: https://developer.android.com/reference/kotlin/android/content/Intent.html#, receiverPermission: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, resultReceiver: https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#?, scheduler: https://developer.android.com/reference/kotlin/android/os/Handler.html#?, initialCode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, initialData: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, initialExtras: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?)`

Version of `https://developer.android.com/reference/kotlin/android/content/Context.html#sendBroadcast(android.content.Intent)` that allows you to receive data back from the broadcast. This is accomplished by supplying your own BroadcastReceiver when calling, which will be treated as a final receiver at the end of the broadcast -- its `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#onReceive(android.content.Context,%20android.content.Intent)` method will be called with the result values collected from the other receivers. The broadcast will be serialized in the same way as calling `https://developer.android.com/reference/kotlin/android/content/Context.html#sendOrderedBroadcast(android.content.Intent,%20kotlin.String)`.

Like `https://developer.android.com/reference/kotlin/android/content/Context.html#sendBroadcast(android.content.Intent)`, this method is asynchronous; it will return before resultReceiver.onReceive() is called.

See `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#` for more information on Intent broadcasts.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#sendOrderedBroadcast(android.content.Intent,%20kotlin.String,%20android.os.Bundle)(intent: https://developer.android.com/reference/kotlin/android/content/Intent.html#, receiverPermission: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, options: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?)`

Broadcast the given intent to all interested BroadcastReceivers, delivering them one at a time to allow more preferred receivers to consume the broadcast before it is delivered to less preferred receivers. This call is asynchronous; it returns immediately, and you will continue executing while the receivers are run.

See `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#` for more information on Intent broadcasts.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#sendOrderedBroadcast(android.content.Intent,%20kotlin.String,%20android.os.Bundle,%20android.content.BroadcastReceiver,%20android.os.Handler,%20kotlin.Int,%20kotlin.String,%20android.os.Bundle)(intent: https://developer.android.com/reference/kotlin/android/content/Intent.html#, receiverPermission: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, options: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?, resultReceiver: https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#?, scheduler: https://developer.android.com/reference/kotlin/android/os/Handler.html#?, initialCode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, initialData: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, initialExtras: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?)`

Version of `https://developer.android.com/reference/kotlin/android/content/Context.html#sendBroadcast(android.content.Intent)` that allows you to receive data back from the broadcast. This is accomplished by supplying your own BroadcastReceiver when calling, which will be treated as a final receiver at the end of the broadcast -- its `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#onReceive(android.content.Context,%20android.content.Intent)` method will be called with the result values collected from the other receivers. The broadcast will be serialized in the same way as calling `https://developer.android.com/reference/kotlin/android/content/Context.html#sendOrderedBroadcast(android.content.Intent,%20kotlin.String)`.

Like `https://developer.android.com/reference/kotlin/android/content/Context.html#sendBroadcast(android.content.Intent)`, this method is asynchronous; it will return before resultReceiver.onReceive() is called.

See `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#` for more information on Intent broadcasts.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#sendOrderedBroadcast(android.content.Intent,%20kotlin.String,%20kotlin.String,%20android.content.BroadcastReceiver,%20android.os.Handler,%20kotlin.Int,%20kotlin.String,%20android.os.Bundle)(intent: https://developer.android.com/reference/kotlin/android/content/Intent.html#, receiverPermission: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, receiverAppOp: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, resultReceiver: https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#?, scheduler: https://developer.android.com/reference/kotlin/android/os/Handler.html#?, initialCode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, initialData: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, initialExtras: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?)`

Version of `https://developer.android.com/reference/kotlin/android/content/Context.html#sendOrderedBroadcast(android.content.Intent,%20kotlin.String,%20android.content.BroadcastReceiver,%20android.os.Handler,%20kotlin.Int,%20kotlin.String,%20android.os.Bundle)` that allows you to specify the App Op to enforce restrictions on which receivers the broadcast will be sent to.

See `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#` for more information on Intent broadcasts.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#sendOrderedBroadcastAsUser(android.content.Intent,%20android.os.UserHandle,%20kotlin.String,%20android.content.BroadcastReceiver,%20android.os.Handler,%20kotlin.Int,%20kotlin.String,%20android.os.Bundle)(intent: https://developer.android.com/reference/kotlin/android/content/Intent.html#!, user: https://developer.android.com/reference/kotlin/android/os/UserHandle.html#!, receiverPermission: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, resultReceiver: https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#?, scheduler: https://developer.android.com/reference/kotlin/android/os/Handler.html#?, initialCode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, initialData: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, initialExtras: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?)`

Version of `https://developer.android.com/reference/kotlin/android/content/Context.html#sendOrderedBroadcast(android.content.Intent,%20kotlin.String,%20android.content.BroadcastReceiver,%20android.os.Handler,%20kotlin.Int,%20kotlin.String,%20android.os.Bundle)` that allows you to specify the user the broadcast will be sent to. This is not available to applications that are not pre-installed on the system image.

See `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#` for more information on Intent broadcasts. 
Requires android.Manifest.permission.INTERACT_ACROSS_USERS

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#sendStickyBroadcast(android.content.Intent)(intent: https://developer.android.com/reference/kotlin/android/content/Intent.html#!)`

Perform a `https://developer.android.com/reference/kotlin/android/content/Context.html#sendBroadcast(android.content.Intent)` that is "sticky," meaning the Intent you are sending stays around after the broadcast is complete, so that others can quickly retrieve that data through the return value of `https://developer.android.com/reference/kotlin/android/content/Context.html#registerReceiver(android.content.BroadcastReceiver,%20android.content.IntentFilter)`. In all other ways, this behaves the same as `https://developer.android.com/reference/kotlin/android/content/Context.html#sendBroadcast(android.content.Intent)`. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BROADCAST_STICKY:kotlin.String`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#sendStickyBroadcast(android.content.Intent,%20android.os.Bundle)(intent: https://developer.android.com/reference/kotlin/android/content/Intent.html#, options: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?)`

Perform a `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#sendBroadcast(android.content.Intent)` that is "sticky," meaning the Intent you are sending stays around after the broadcast is complete, so that others can quickly retrieve that data through the return value of `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#registerReceiver(android.content.BroadcastReceiver,%20android.content.IntentFilter)`. In all other ways, this behaves the same as `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#sendBroadcast(android.content.Intent)`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#sendStickyBroadcastAsUser(android.content.Intent,%20android.os.UserHandle)(intent: https://developer.android.com/reference/kotlin/android/content/Intent.html#!, user: https://developer.android.com/reference/kotlin/android/os/UserHandle.html#!)`

Version of `https://developer.android.com/reference/kotlin/android/content/Context.html#sendStickyBroadcast(android.content.Intent)` that allows you to specify the user the broadcast will be sent to. This is not available to applications that are not pre-installed on the system image. 
Requires android.Manifest.permission.INTERACT_ACROSS_USERS and `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BROADCAST_STICKY:kotlin.String`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#sendStickyOrderedBroadcast(android.content.Intent,%20android.content.BroadcastReceiver,%20android.os.Handler,%20kotlin.Int,%20kotlin.String,%20android.os.Bundle)(intent: https://developer.android.com/reference/kotlin/android/content/Intent.html#!, resultReceiver: https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#?, scheduler: https://developer.android.com/reference/kotlin/android/os/Handler.html#?, initialCode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, initialData: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, initialExtras: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?)`

Version of #sendStickyBroadcast that allows you to receive data back from the broadcast. This is accomplished by supplying your own BroadcastReceiver when calling, which will be treated as a final receiver at the end of the broadcast -- its `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#onReceive(android.content.Context,%20android.content.Intent)` method will be called with the result values collected from the other receivers. The broadcast will be serialized in the same way as calling `https://developer.android.com/reference/kotlin/android/content/Context.html#sendOrderedBroadcast(android.content.Intent,%20kotlin.String)`.

Like `https://developer.android.com/reference/kotlin/android/content/Context.html#sendBroadcast(android.content.Intent)`, this method is asynchronous; it will return before resultReceiver.onReceive() is called. Note that the sticky data stored is only the data you initially supply to the broadcast, not the result of any changes made by the receivers.

See `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#` for more information on Intent broadcasts. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BROADCAST_STICKY:kotlin.String`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#sendStickyOrderedBroadcastAsUser(android.content.Intent,%20android.os.UserHandle,%20android.content.BroadcastReceiver,%20android.os.Handler,%20kotlin.Int,%20kotlin.String,%20android.os.Bundle)(intent: https://developer.android.com/reference/kotlin/android/content/Intent.html#!, user: https://developer.android.com/reference/kotlin/android/os/UserHandle.html#!, resultReceiver: https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#?, scheduler: https://developer.android.com/reference/kotlin/android/os/Handler.html#?, initialCode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, initialData: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, initialExtras: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?)`

Version of `https://developer.android.com/reference/kotlin/android/content/Context.html#sendStickyOrderedBroadcast(android.content.Intent,%20android.content.BroadcastReceiver,%20android.os.Handler,%20kotlin.Int,%20kotlin.String,%20android.os.Bundle)` that allows you to specify the user the broadcast will be sent to. This is not available to applications that are not pre-installed on the system image.

See `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#` for more information on Intent broadcasts. 
Requires android.Manifest.permission.INTERACT_ACROSS_USERS and `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BROADCAST_STICKY:kotlin.String`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#setWallpaper(android.graphics.Bitmap)(bitmap: https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#!)`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#setWallpaper(java.io.InputStream)(data: https://developer.android.com/reference/kotlin/java/io/InputStream.html#!)`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#shouldShowRequestPermissionRationale(kotlin.String)(permission: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`

Gets whether you should show UI with rationale before requesting a permission. If the permission does not exist on this SDK level or is not visible to this app, the method will return `false`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#startActivities(kotlin.Array)(intents: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/android/content/Intent.html#!>!)`

Same as `https://developer.android.com/reference/kotlin/android/content/Context.html#startActivities(kotlin.Array,%20android.os.Bundle)` with no options specified.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#startActivities(kotlin.Array,%20android.os.Bundle)(intents: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/android/content/Intent.html#!>!, options: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?)`

Launch multiple new activities. This is generally the same as calling `https://developer.android.com/reference/kotlin/android/content/Context.html#startActivity(android.content.Intent)` for the first Intent in the array, that activity during its creation calling `https://developer.android.com/reference/kotlin/android/content/Context.html#startActivity(android.content.Intent)` for the second entry, etc. Note that unlike that approach, generally none of the activities except the last in the array will be created at this point, but rather will be created when the user first visits them (due to pressing back from the activity on top).

This method throws `https://developer.android.com/reference/kotlin/android/content/ActivityNotFoundException.html#` if there was no Activity found for *any* given Intent. In this case the state of the activity stack is undefined (some Intents in the list may be on it, some not), so you probably want to avoid such situations.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#startActivity(android.content.Intent)(intent: https://developer.android.com/reference/kotlin/android/content/Intent.html#!)`

Same as `https://developer.android.com/reference/kotlin/android/content/Context.html#startActivity(android.content.Intent,%20android.os.Bundle)` with no options specified.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#startActivity(android.content.Intent,%20android.os.Bundle)(intent: https://developer.android.com/reference/kotlin/android/content/Intent.html#!, options: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?)`

Launch a new activity. You will not receive any information about when the activity exits.

Note that if this method is being called from outside of an `https://developer.android.com/reference/kotlin/android/app/Activity` Context, then the Intent must include the `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_ACTIVITY_NEW_TASK:kotlin.Int` launch flag. This is because, without being started from an existing Activity, there is no existing task in which to place the new activity and thus it needs to be placed in its own separate task.

This method throws `https://developer.android.com/reference/kotlin/android/content/ActivityNotFoundException.html#` if there was no Activity found to run the given Intent.

<br />

`https://developer.android.com/reference/kotlin/android/content/ComponentName.html#?` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#startForegroundService(android.content.Intent)(service: https://developer.android.com/reference/kotlin/android/content/Intent.html#!)`

Similar to `https://developer.android.com/reference/kotlin/android/content/Context.html#startService(android.content.Intent)`, but with an implicit promise that the Service will call `https://developer.android.com/reference/kotlin/android/app/Service#startForeground(kotlin.Int,%20android.app.Notification)` once it begins running. The service is given an amount of time comparable to the ANR interval to do this, otherwise the system will automatically crash the process, in which case an internal exception `ForegroundServiceDidNotStartInTimeException` is logged on logcat on devices running SDK Version `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or later. On older Android versions, an internal exception `RemoteServiceException` is logged instead, with a corresponding message.

Unlike the ordinary `https://developer.android.com/reference/kotlin/android/content/Context.html#startService(android.content.Intent)`, this method can be used at any time, regardless of whether the app hosting the service is in a foreground state.

**Note:** Beginning with SDK Version `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int`, apps targeting SDK Version `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or higher are not allowed to start foreground services from the background. See [Behavior changes: Apps targeting Android 12](../about/versions/12/behavior-changes-12.md) for more details.

<br />

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#startInstrumentation(android.content.ComponentName,%20kotlin.String,%20android.os.Bundle)(className: https://developer.android.com/reference/kotlin/android/content/ComponentName.html#, profileFile: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, arguments: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?)`

Start executing an `https://developer.android.com/reference/kotlin/android/app/Instrumentation` class. The given Instrumentation component will be run by killing its target application (if currently running), starting the target process, instantiating the instrumentation component, and then letting it drive the application.

This function is not synchronous -- it returns as soon as the instrumentation has started and while it is running.

Instrumentation is normally only allowed to run against a package that is either unsigned or signed with a signature that the the instrumentation package is also signed with (ensuring the target trusts the instrumentation).

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#startIntentSender(android.content.IntentSender,%20android.content.Intent,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)(intent: https://developer.android.com/reference/kotlin/android/content/IntentSender.html#!, fillInIntent: https://developer.android.com/reference/kotlin/android/content/Intent.html#?, flagsMask: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, flagsValues: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, extraFlags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Same as `https://developer.android.com/reference/kotlin/android/content/Context.html#startIntentSender(android.content.IntentSender,%20android.content.Intent,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20android.os.Bundle)` with no options specified.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#startIntentSender(android.content.IntentSender,%20android.content.Intent,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20android.os.Bundle)(intent: https://developer.android.com/reference/kotlin/android/content/IntentSender.html#!, fillInIntent: https://developer.android.com/reference/kotlin/android/content/Intent.html#?, flagsMask: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, flagsValues: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, extraFlags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, options: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?)`

Like `https://developer.android.com/reference/kotlin/android/content/Context.html#startActivity(android.content.Intent,%20android.os.Bundle)`, but taking a IntentSender to start. If the IntentSender is for an activity, that activity will be started as if you had called the regular `https://developer.android.com/reference/kotlin/android/content/Context.html#startActivity(android.content.Intent)` here; otherwise, its associated action will be executed (such as sending a broadcast) as if you had called android.content.IntentSender#sendIntent on it.

<br />

`https://developer.android.com/reference/kotlin/android/content/ComponentName.html#?` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#startService(android.content.Intent)(service: https://developer.android.com/reference/kotlin/android/content/Intent.html#!)`

Request that a given application service be started. The Intent should either contain the complete class name of a specific service implementation to start, or a specific package name to target. If the Intent is less specified, it logs a warning about this. In this case any of the multiple matching services may be used. If this service is not already running, it will be instantiated and started (creating a process for it if needed); if it is running then it remains running.

Every call to this method will result in a corresponding call to the target service's `https://developer.android.com/reference/kotlin/android/app/Service#onStartCommand(android.content.Intent,%20kotlin.Int,%20kotlin.Int)` method, with the intent given here. This provides a convenient way to submit jobs to a service without having to bind and call on to its interface.

Using startService() overrides the default service lifetime that is managed by #bindService: it requires the service to remain running until `https://developer.android.com/reference/kotlin/android/content/Context.html#stopService(android.content.Intent)` is called, regardless of whether any clients are connected to it. Note that calls to startService() do not nest: no matter how many times you call startService(), a single call to `https://developer.android.com/reference/kotlin/android/content/Context.html#stopService(android.content.Intent)` will stop it.

The system attempts to keep running services around as much as possible. The only time they should be stopped is if the current foreground application is using so many resources that the service needs to be killed. If any errors happen in the service's process, it will automatically be restarted.

This function will throw `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#` if you do not have permission to start the given service.

**Note:** Each call to startService() results in significant work done by the system to manage service lifecycle surrounding the processing of the intent, which can take multiple milliseconds of CPU time. Due to this cost, startService() should not be used for frequent intent delivery to a service, and only for scheduling significant work. Use #bindService for high frequency calls.
Beginning with SDK Version `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#O:kotlin.Int`, apps targeting SDK Version `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#O:kotlin.Int` or higher are not allowed to start background services from the background. See [Background Execution Limits](../about/versions/oreo/background.md) for more details.

**Note:** Beginning with SDK Version `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int`, apps targeting SDK Version `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or higher are not allowed to start foreground services from the background. See [Behavior changes: Apps targeting Android 12](../about/versions/12/behavior-changes-12.md) for more details.

<br />

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#stopService(android.content.Intent)(name: https://developer.android.com/reference/kotlin/android/content/Intent.html#!)`

Request that a given application service be stopped. If the service is not running, nothing happens. Otherwise it is stopped. Note that calls to startService() are not counted -- this stops the service no matter how many times it was started.

If the service is running as a foreground service when it is stopped, its associated notification will be removed. To avoid this, apps can use `https://developer.android.com/reference/kotlin/android/app/Service#stopForeground(kotlin.Int)` to decouple the notification from the service's lifecycle before stopping it.

Note that if a stopped service still has `https://developer.android.com/reference/kotlin/android/content/ServiceConnection.html#` objects bound to it with the `https://developer.android.com/reference/kotlin/android/content/Context.html#BIND_AUTO_CREATE:kotlin.Int` set, it will not be destroyed until all of these bindings are removed. See the `https://developer.android.com/reference/kotlin/android/app/Service` documentation for more details on a service's lifecycle.

This function will throw `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#` if you do not have permission to stop the given service.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#unbindService(android.content.ServiceConnection)(conn: https://developer.android.com/reference/kotlin/android/content/ServiceConnection.html#)`

Disconnect from an application service. You will no longer receive calls as the service is restarted, and the service is now allowed to stop at any time.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#unregisterComponentCallbacks(android.content.ComponentCallbacks)(callback: https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks.html#!)`

Remove a `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks.html#` object that was previously registered with `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#registerComponentCallbacks(android.content.ComponentCallbacks)`.

After `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#TIRAMISU:kotlin.Int`, the `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks.html#` will be unregistered to `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#getBaseContext()`, and can be only used after `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#attachBaseContext(android.content.Context)`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#unregisterDeviceIdChangeListener(java.util.function.IntConsumer)(listener: https://developer.android.com/reference/kotlin/java/util/function/IntConsumer.html#)`

Removes a device ID changed listener from the Context. It's a no-op if the listener is not already registered.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#unregisterReceiver(android.content.BroadcastReceiver)(receiver: https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#!)`

Unregister a previously registered BroadcastReceiver. *All* filters that have been registered for this BroadcastReceiver will be removed.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#updateServiceBindings(kotlin.collections.MutableCollection)(params: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html<https://developer.android.com/reference/kotlin/android/content/Context.UpdateBindingParams.html#!>)`

Perform a batch update of existing bindings. Existing bindings can be rebound with an updated set of flags, or unbound. Only flags returned from `https://developer.android.com/reference/kotlin/android/content/Context.html#getUpdateableFlags()` may be added or removed.

This API behaves as if the `https://developer.android.com/reference/kotlin/android/content/Context.html#rebindService(android.content.ServiceConnection,%20android.content.Context.BindServiceFlags)` and `https://developer.android.com/reference/kotlin/android/content/Context.html#unbindService(android.content.ServiceConnection)` API are called in the same order as the params are iterated.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#updateServiceGroup(android.content.ServiceConnection,%20kotlin.Int,%20kotlin.Int)(conn: https://developer.android.com/reference/kotlin/android/content/ServiceConnection.html#, group: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, importance: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

For a service previously bound with #bindService or a related method, change how the system manages that service's process in relation to other processes. This doesn't modify the original bind flags that were passed in when binding, but adjusts how the process will be managed in some cases based on those flags. Currently only works on isolated processes (will be ignored for non-isolated processes).

Note that this call does not take immediate effect, but will be applied the next time the impacted process is adjusted for some other reason. Typically you would call this before then calling a new #bindIsolatedService on the service of interest, with that binding causing the process to be shuffled accordingly.

<br />

From class `https://developer.android.com/reference/kotlin/android/content/Context.html#` `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#bindIsolatedService(android.content.Intent,%20android.content.Context.BindServiceFlags,%20kotlin.String,%20java.util.concurrent.Executor,%20android.content.ServiceConnection)(service: https://developer.android.com/reference/kotlin/android/content/Intent.html#, flags: https://developer.android.com/reference/kotlin/android/content/Context.BindServiceFlags.html#, instanceName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, conn: https://developer.android.com/reference/kotlin/android/content/ServiceConnection.html#)`

See `https://developer.android.com/reference/kotlin/android/content/Context.html#bindIsolatedService(android.content.Intent,%20kotlin.Int,%20kotlin.String,%20java.util.concurrent.Executor,%20android.content.ServiceConnection)` Call `https://developer.android.com/reference/kotlin/android/content/Context.BindServiceFlags.html#of(kotlin.Long)` to obtain a BindServiceFlags object.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#getColor(kotlin.Int)(id: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Returns a color associated with a particular resource ID and styled for the current theme.

<br />

`https://developer.android.com/reference/kotlin/android/content/res/ColorStateList.html#` `https://developer.android.com/reference/kotlin/android/content/Context.html#getColorStateList(kotlin.Int)(id: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Returns a color state list associated with a particular resource ID and styled for the current theme.

<br />

`https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#?` `https://developer.android.com/reference/kotlin/android/content/Context.html#getDrawable(kotlin.Int)(id: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Returns a drawable object associated with a particular resource ID and styled for the current theme.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#getString(kotlin.Int)(resId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Returns a localized string from the application's package's default string table.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#getString(kotlin.Int,%20kotlin.Any)(resId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, vararg formatArgs: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!)`

Returns a localized formatted string from the application's package's default string table, substituting the format arguments as defined in `https://developer.android.com/reference/kotlin/java/util/Formatter.html#` and java.lang.String#format.

<br />

`T` `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(java.lang.Class)(serviceClass: https://developer.android.com/reference/kotlin/java/lang/Class.html#<T>)`

Return the handle to a system-level service by class.

Currently available classes are: `https://developer.android.com/reference/kotlin/android/view/WindowManager.html#`, `https://developer.android.com/reference/kotlin/android/view/LayoutInflater.html#`, `https://developer.android.com/reference/kotlin/android/app/ActivityManager`, `https://developer.android.com/reference/kotlin/android/os/PowerManager.html#`, `https://developer.android.com/reference/kotlin/android/app/AlarmManager`, `https://developer.android.com/reference/kotlin/android/app/NotificationManager`, `https://developer.android.com/reference/kotlin/android/app/KeyguardManager`, `https://developer.android.com/reference/kotlin/android/location/LocationManager.html#`, `https://developer.android.com/reference/kotlin/android/app/SearchManager`, `https://developer.android.com/reference/kotlin/android/os/Vibrator.html#`, `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager.html#`, `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager.html#`, `https://developer.android.com/reference/kotlin/android/media/AudioManager.html#`, `https://developer.android.com/reference/kotlin/android/media/MediaRouter.html#`, `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager.html#`, `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager.html#`, `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager.html#`, `https://developer.android.com/reference/kotlin/android/app/UiModeManager`, `https://developer.android.com/reference/kotlin/android/app/DownloadManager`, `https://developer.android.com/reference/kotlin/android/os/BatteryManager.html#`, `https://developer.android.com/reference/kotlin/android/app/job/JobScheduler`, `https://developer.android.com/reference/kotlin/android/app/usage/NetworkStatsManager`, `https://developer.android.com/reference/kotlin/android/content/pm/verify/domain/DomainVerificationManager.html#`, `https://developer.android.com/reference/kotlin/android/view/displayhash/DisplayHashManager.html#` `https://developer.android.com/reference/kotlin/android/security/authenticationpolicy/AuthenticationPolicyManager.html#`.

Note: System services obtained via this API may be closely associated with the Context in which they are obtained from. In general, do not share the service objects between various different contexts (Activities, Applications, Services, Providers, etc.)

Note: Instant apps, for which `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#isInstantApp()` returns true, don't have access to the following system services: `https://developer.android.com/reference/kotlin/android/content/Context.html#DEVICE_POLICY_SERVICE:kotlin.String`, #FINGERPRINT_SERVICE, `https://developer.android.com/reference/kotlin/android/content/Context.html#KEYGUARD_SERVICE:kotlin.String`, `https://developer.android.com/reference/kotlin/android/content/Context.html#SHORTCUT_SERVICE:kotlin.String`, `https://developer.android.com/reference/kotlin/android/content/Context.html#USB_SERVICE:kotlin.String`, `https://developer.android.com/reference/kotlin/android/content/Context.html#WALLPAPER_SERVICE:kotlin.String`, `https://developer.android.com/reference/kotlin/android/content/Context.html#WIFI_P2P_SERVICE:kotlin.String`, `https://developer.android.com/reference/kotlin/android/content/Context.html#WIFI_SERVICE:kotlin.String`, `https://developer.android.com/reference/kotlin/android/content/Context.html#WIFI_AWARE_SERVICE:kotlin.String`. For these services this method will return `null`. Generally, if you are running as an instant app you should always check whether the result of this method is `null`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#getText(kotlin.Int)(resId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Return a localized, styled CharSequence from the application's package's default string table.

<br />

`https://developer.android.com/reference/kotlin/android/content/Context.BindServiceFlags.html#` `https://developer.android.com/reference/kotlin/android/content/Context.html#getUpdateableFlags()()`

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

`https://developer.android.com/reference/kotlin/android/content/res/TypedArray.html#` `https://developer.android.com/reference/kotlin/android/content/Context.html#obtainStyledAttributes(android.util.AttributeSet,%20kotlin.IntArray)(set: https://developer.android.com/reference/kotlin/android/util/AttributeSet.html#?, attrs: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)`

Retrieve styled attribute information in this Context's theme. See `https://developer.android.com/reference/kotlin/android/content/res/Resources.Theme.html#obtainStyledAttributes(android.util.AttributeSet,%20kotlin.IntArray,%20kotlin.Int,%20kotlin.Int)` for more information.

<br />

`https://developer.android.com/reference/kotlin/android/content/res/TypedArray.html#` `https://developer.android.com/reference/kotlin/android/content/Context.html#obtainStyledAttributes(android.util.AttributeSet,%20kotlin.IntArray,%20kotlin.Int,%20kotlin.Int)(set: https://developer.android.com/reference/kotlin/android/util/AttributeSet.html#?, attrs: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html, defStyleAttr: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, defStyleRes: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Retrieve styled attribute information in this Context's theme. See `https://developer.android.com/reference/kotlin/android/content/res/Resources.Theme.html#obtainStyledAttributes(android.util.AttributeSet,%20kotlin.IntArray,%20kotlin.Int,%20kotlin.Int)` for more information.

<br />

`https://developer.android.com/reference/kotlin/android/content/res/TypedArray.html#` `https://developer.android.com/reference/kotlin/android/content/Context.html#obtainStyledAttributes(kotlin.Int,%20kotlin.IntArray)(resid: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, attrs: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)`

Retrieve styled attribute information in this Context's theme. See `https://developer.android.com/reference/kotlin/android/content/res/Resources.Theme.html#obtainStyledAttributes(kotlin.Int,%20kotlin.IntArray)` for more information.

<br />

`https://developer.android.com/reference/kotlin/android/content/res/TypedArray.html#` `https://developer.android.com/reference/kotlin/android/content/Context.html#obtainStyledAttributes(kotlin.IntArray)(attrs: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)`

Retrieve styled attribute information in this Context's theme. See `https://developer.android.com/reference/kotlin/android/content/res/Resources.Theme.html#obtainStyledAttributes(kotlin.IntArray)` for more information.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#revokeSelfPermissionOnKill(kotlin.String)(permName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`

Triggers the asynchronous revocation of a runtime permission. If the permission is not currently granted, nothing happens (even if later granted by the user).

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#sendBroadcastWithMultiplePermissions(android.content.Intent,%20kotlin.Array)(intent: https://developer.android.com/reference/kotlin/android/content/Intent.html#, receiverPermissions: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>)`

Broadcast the given intent to all interested BroadcastReceivers, allowing an array of required permissions to be enforced. This call is asynchronous; it returns immediately, and you will continue executing while the receivers are run. No results are propagated from receivers and receivers can not abort the broadcast. If you want to allow receivers to propagate results or abort the broadcast, you must send an ordered broadcast using `https://developer.android.com/reference/kotlin/android/content/Context.html#sendOrderedBroadcast(android.content.Intent,%20kotlin.String)`.

See `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#` for more information on Intent broadcasts.

<br />

From class `https://developer.android.com/reference/kotlin/android/app/ListActivity` `https://developer.android.com/reference/kotlin/android/widget/ListAdapter.html#!` `https://developer.android.com/reference/kotlin/android/app/ListActivity#getListAdapter()()`

Get the ListAdapter associated with this activity's ListView.

<br />

`https://developer.android.com/reference/kotlin/android/widget/ListView.html#!` `https://developer.android.com/reference/kotlin/android/app/ListActivity#getListView()()`

Get the activity's list view widget.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` `https://developer.android.com/reference/kotlin/android/app/ListActivity#getSelectedItemId()()`

Get the cursor row ID of the currently selected list item.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/app/ListActivity#getSelectedItemPosition()()`

Get the position of the currently selected list item.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/ListActivity#onContentChanged()()`

Updates the screen state (current list and other views) when the content changes.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/ListActivity#onDestroy()()`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/ListActivity#onRestoreInstanceState(android.os.Bundle)(state: https://developer.android.com/reference/kotlin/android/os/Bundle.html#)`

Ensures the list view has been created before Activity restores all of the view states.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/ListActivity#setListAdapter(android.widget.ListAdapter)(adapter: https://developer.android.com/reference/kotlin/android/widget/ListAdapter.html#!)`

Provide the cursor for the list view.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/ListActivity#setSelection(kotlin.Int)(position: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Set the currently selected list item to the specified position with the adapter's data

<br />

From class `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks.html#` `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks.html#onConfigurationChanged(android.content.res.Configuration)(newConfig: https://developer.android.com/reference/kotlin/android/content/res/Configuration.html#)`

Called by the system when the device configuration changes while your component is running. Note that, unlike activities, other components are never restarted when a configuration changes: they must always deal with the results of the change, such as by re-retrieving resources.

At the time that this function has been called, your Resources object will have been updated to return resource values matching the new configuration.

For more information, read [Handling Runtime Changes](https://developer.android.com/guide/topics/resources/runtime-changes.html).

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks.html#onLowMemory()()`

This is called when the overall system is running low on memory, and actively running processes should trim their memory usage. While the exact point at which this will be called is not defined, generally it will happen when all background process have been killed. That is, before reaching the point of killing processes hosting service and foreground UI that we would like to avoid killing.

<br />

From class `https://developer.android.com/reference/kotlin/android/view/Window.Callback.html#` `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/Window.Callback.html#onPointerCaptureChanged(kotlin.Boolean)(hasCapture: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`

Called when pointer capture is enabled or disabled for the current window.

<br />

Inherited properties From class `https://developer.android.com/reference/kotlin/android/app/Activity` `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html!` `https://developer.android.com/reference/kotlin/android/app/Activity#FOCUSED_STATE_SET:kotlin.IntArray`

<br />

## Public constructors

### LauncherActivity

```
LauncherActivity()
```

## Public methods

### makeListItems

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun makeListItems(): MutableList<LauncherActivity.ListItem!>!
```

**Deprecated:** *Deprecated in Java.*

Perform the query to determine which results to show and return a list of them.

### setTitle

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setTitle(titleId: Int): Unit
```

**Deprecated:** *Deprecated in Java.*

Change the title associated with this activity. If this is a top-level activity, the title for its window will change. If it is an embedded activity, the parent can do whatever it wants with it.

### setTitle

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setTitle(title: CharSequence!): Unit
```

**Deprecated:** *Deprecated in Java.*

Change the title associated with this activity. If this is a top-level activity, the title for its window will change. If it is an embedded activity, the parent can do whatever it wants with it.

## Protected methods

### getTargetIntent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun getTargetIntent(): Intent!
```

**Deprecated:** *Deprecated in Java.*

Get the base intent to use when running `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#queryIntentActivities(android.content.Intent,%20kotlin.Int)`.

### intentForPosition

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun intentForPosition(position: Int): Intent!
```

**Deprecated:** *Deprecated in Java.*

Return the actual Intent for a specific position in our `https://developer.android.com/reference/kotlin/android/widget/ListView.html#`.

| Parameters ||
|---|---|
| `position` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The item whose Intent to return |

### itemForPosition

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun itemForPosition(position: Int): LauncherActivity.ListItem!
```

**Deprecated:** *Deprecated in Java.*

Return the `https://developer.android.com/reference/kotlin/android/app/LauncherActivity.ListItem` for a specific position in our `https://developer.android.com/reference/kotlin/android/widget/ListView.html#`.

| Parameters ||
|---|---|
| `position` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The item to return |

### onCreate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun onCreate(icicle: Bundle?): Unit
```

**Deprecated:** *Deprecated in Java.*

Called when the activity is starting. This is where most initialization should go: calling `https://developer.android.com/reference/kotlin/android/app/Activity#setContentView(kotlin.Int)` to inflate the activity's UI, using `https://developer.android.com/reference/kotlin/android/app/Activity#findViewById(kotlin.Int)` to programmatically interact with widgets in the UI, calling `https://developer.android.com/reference/kotlin/android/app/Activity#managedQuery(android.net.Uri,%20kotlin.Array,%20kotlin.String,%20kotlin.Array,%20kotlin.String)` to retrieve cursors for data being displayed, etc.

You can call `https://developer.android.com/reference/kotlin/android/app/Activity#finish()` from within this function, in which case onDestroy() will be immediately called after #onCreate without any of the rest of the activity lifecycle (`https://developer.android.com/reference/kotlin/android/app/Activity#onStart()`, `https://developer.android.com/reference/kotlin/android/app/Activity#onResume()`, `https://developer.android.com/reference/kotlin/android/app/Activity#onPause()`, etc.) executing.

*Derived classes must call through to the super class's implementation of this method. If they do not, an exception will be thrown.*
. 
This method must be called from the main thread of your app. 
If you override this method you *must* call through to the superclass implementation.

| Parameters ||
|---|---|
| `savedInstanceState` | If the activity is being re-initialized after previously being shut down then this Bundle contains the data it most recently supplied in #onSaveInstanceState. ***Note: Otherwise it is null.*** |

### onListItemClick

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun onListItemClick(
    l: ListView!, 
    v: View!, 
    position: Int, 
    id: Long
): Unit
```

**Deprecated:** *Deprecated in Java.*

This method will be called when an item in the list is selected. Subclasses should override. Subclasses can call getListView().getItemAtPosition(position) if they need to access the data associated with the selected item.

| Parameters ||
|---|---|
| `l` | [ListView](../android/widget/ListView.md)!: The ListView where the click happened |
| `v` | [View](../android/view/View.md)!: The view that was clicked within the ListView |
| `position` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The position of the view in the list |
| --- | --- |
| `id` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): The row id of the item that was clicked |

### onQueryPackageManager

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun onQueryPackageManager(queryIntent: Intent!): MutableList<ResolveInfo!>!
```

**Deprecated:** *Deprecated in Java.*

Perform query on package manager for list items. The default implementation queries for activities.

### onSetContentView

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun onSetContentView(): Unit
```

**Deprecated:** *Deprecated in Java.*

Override to call setContentView() with your own content view to customize the list layout.
