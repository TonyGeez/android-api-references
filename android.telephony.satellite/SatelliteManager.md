# SatelliteManager

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SatelliteManager

Kotlin| [Java](https://developer.android.com/reference/android/telephony/satellite/SatelliteManager "View this page in Java") 
| --- | --- |

```
class SatelliteManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.telephony.satellite.SatelliteManager](https://developer.android.com/reference/kotlin/android/telephony/satellite/SatelliteManager#) |

Manages satellite states such as monitoring enabled state and operations such as provisioning, pointing, messaging, location sharing, etc.

To get the object, call [Context.getSystemService(String)](https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String))with [Context.SATELLITE_SERVICE](https://developer.android.com/reference/kotlin/android/content/Context.html#SATELLITE_SERVICE:kotlin.String).

SatelliteManager is intended for use on devices with feature android.content.pm.PackageManager#FEATURE_TELEPHONY_SATELLITE. On devices without the feature, the behavior is not reliable. 
Requires the PackageManager#FEATURE_TELEPHONY_SATELLITE feature which can be detected using [PackageManager.hasSystemFeature(String)](https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#hasSystemFeature(kotlin.String)).

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [PROPERTY_SATELLITE_DATA_OPTIMIZED](https://developer.android.com/reference/kotlin/android/telephony/satellite/SatelliteManager#PROPERTY_SATELLITE_DATA_OPTIMIZED:kotlin.String) The applications that are optimized for low bandwidth satellite data should set this property to package name of the application in the manifest to indicate to platform about the same. |

| Public methods ||
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerStateChangeListener](https://developer.android.com/reference/kotlin/android/telephony/satellite/SatelliteManager#registerStateChangeListener(java.util.concurrent.Executor,%20android.telephony.satellite.SatelliteStateChangeListener))`(`executor:` ` [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#)`, `listener:` ` [SatelliteStateChangeListener](https://developer.android.com/reference/kotlin/android/telephony/satellite/SatelliteStateChangeListener)`)` Registers a [SatelliteStateChangeListener](https://developer.android.com/reference/kotlin/android/telephony/satellite/SatelliteStateChangeListener) to receive callbacks when the satellite state may have changed. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unregisterStateChangeListener](https://developer.android.com/reference/kotlin/android/telephony/satellite/SatelliteManager#unregisterStateChangeListener(android.telephony.satellite.SatelliteStateChangeListener))`(`listener:` ` [SatelliteStateChangeListener](https://developer.android.com/reference/kotlin/android/telephony/satellite/SatelliteStateChangeListener)`)` Unregisters the [SatelliteStateChangeListener](https://developer.android.com/reference/kotlin/android/telephony/satellite/SatelliteStateChangeListener) previously registered with [registerStateChangeListener(java.util.concurrent.Executor,android.telephony.satellite.SatelliteStateChangeListener)](https://developer.android.com/reference/kotlin/android/telephony/satellite/SatelliteManager#registerStateChangeListener(java.util.concurrent.Executor,%20android.telephony.satellite.SatelliteStateChangeListener)). |

## Constants

### PROPERTY_SATELLITE_DATA_OPTIMIZED

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PROPERTY_SATELLITE_DATA_OPTIMIZED: String
```

The applications that are optimized for low bandwidth satellite data should set this property to package name of the application in the manifest to indicate to platform about the same.`<application> <meta-data android:name="android.telephony.PROPERTY_SATELLITE_DATA_OPTIMIZED" android:value=<package-name>/> </application> `

When this meta-data is set in application's manifest, satellite data optimized network is available for application to use. 

 Value: "android.telephony.PROPERTY_SATELLITE_DATA_OPTIMIZED"

## Public methods

### registerStateChangeListener

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun registerStateChangeListener(
    executor: Executor, 
    listener: SatelliteStateChangeListener
): Unit
```

Registers a [SatelliteStateChangeListener](https://developer.android.com/reference/kotlin/android/telephony/satellite/SatelliteStateChangeListener) to receive callbacks when the satellite state may have changed.

The callback method is immediately triggered with latest state on invoking this method if the state change has been notified before. 
Requires [android.Manifest.permission#READ_BASIC_PHONE_STATE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_BASIC_PHONE_STATE:kotlin.String) or android.Manifest.permission.READ_PRIVILEGED_PHONE_STATE or [android.Manifest.permission#READ_PHONE_STATE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PHONE_STATE:kotlin.String) or [carrier privileges](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager.html#hasCarrierPrivileges())

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#):The [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#) where the`listener`will be invoked This value cannot be`null`. Callback and listener events are dispatched through this [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()). Otherwise, provide an [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#) that dispatches to an appropriate thread. |
| `listener` | [SatelliteStateChangeListener](https://developer.android.com/reference/kotlin/android/telephony/satellite/SatelliteStateChangeListener):The listener to monitor the satellite state change This value cannot be`null`. |

**See Also**

- [android.telephony.satellite.SatelliteStateChangeListener](https://developer.android.com/reference/kotlin/android/telephony/satellite/SatelliteStateChangeListener)
- [android.telephony.TelephonyManager#hasCarrierPrivileges()](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager.html#hasCarrierPrivileges()) 

### unregisterStateChangeListener

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun unregisterStateChangeListener(listener: SatelliteStateChangeListener): Unit
```

Unregisters the [SatelliteStateChangeListener](https://developer.android.com/reference/kotlin/android/telephony/satellite/SatelliteStateChangeListener) previously registered with [registerStateChangeListener(java.util.concurrent.Executor,android.telephony.satellite.SatelliteStateChangeListener)](https://developer.android.com/reference/kotlin/android/telephony/satellite/SatelliteManager#registerStateChangeListener(java.util.concurrent.Executor,%20android.telephony.satellite.SatelliteStateChangeListener)).

It will be a no-op if the`listener`is not currently registered. 
Requires [android.Manifest.permission#READ_BASIC_PHONE_STATE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_BASIC_PHONE_STATE:kotlin.String) or android.Manifest.permission.READ_PRIVILEGED_PHONE_STATE or [android.Manifest.permission#READ_PHONE_STATE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PHONE_STATE:kotlin.String) or [carrier privileges](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager.html#hasCarrierPrivileges())

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [SatelliteStateChangeListener](https://developer.android.com/reference/kotlin/android/telephony/satellite/SatelliteStateChangeListener):The listener to unregister This value cannot be`null`. |

**See Also**

- [android.telephony.satellite.SatelliteStateChangeListener](https://developer.android.com/reference/kotlin/android/telephony/satellite/SatelliteStateChangeListener)
- [android.telephony.TelephonyManager#hasCarrierPrivileges()](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager.html#hasCarrierPrivileges())
