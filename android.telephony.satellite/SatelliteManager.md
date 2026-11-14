# SatelliteManager

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SatelliteManager

Kotlin| [Java](../android/telephony/satellite/SatelliteManager.md) 
| --- | --- |

```
class SatelliteManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.telephony.satellite.SatelliteManager](../android/telephony/satellite/SatelliteManager.md) |

Manages satellite states such as monitoring enabled state and operations such as provisioning, pointing, messaging, location sharing, etc.

To get the object, call [Context.getSystemService(String)](../android/content/Context.md))with [Context.SATELLITE_SERVICE](../android/content/Context.md).

SatelliteManager is intended for use on devices with feature android.content.pm.PackageManager#FEATURE_TELEPHONY_SATELLITE. On devices without the feature, the behavior is not reliable. 
Requires the PackageManager#FEATURE_TELEPHONY_SATELLITE feature which can be detected using [PackageManager.hasSystemFeature(String)](../android/content/pm/PackageManager.md)).

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [PROPERTY_SATELLITE_DATA_OPTIMIZED](../android/telephony/satellite/SatelliteManager.md) The applications that are optimized for low bandwidth satellite data should set this property to package name of the application in the manifest to indicate to platform about the same. |

| Public methods ||
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerStateChangeListener](../android/telephony/satellite/SatelliteManager.md))`(`executor:` ` [Executor](../java/util/concurrent/Executor.md)`, `listener:` ` [SatelliteStateChangeListener](../android/telephony/satellite/SatelliteStateChangeListener.md)`)` Registers a [SatelliteStateChangeListener](../android/telephony/satellite/SatelliteStateChangeListener.md) to receive callbacks when the satellite state may have changed. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unregisterStateChangeListener](../android/telephony/satellite/SatelliteManager.md))`(`listener:` ` [SatelliteStateChangeListener](../android/telephony/satellite/SatelliteStateChangeListener.md)`)` Unregisters the [SatelliteStateChangeListener](../android/telephony/satellite/SatelliteStateChangeListener.md) previously registered with [registerStateChangeListener(java.util.concurrent.Executor,android.telephony.satellite.SatelliteStateChangeListener)](../android/telephony/satellite/SatelliteManager.md)). |

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

Registers a [SatelliteStateChangeListener](../android/telephony/satellite/SatelliteStateChangeListener.md) to receive callbacks when the satellite state may have changed.

The callback method is immediately triggered with latest state on invoking this method if the state change has been notified before. 
Requires [android.Manifest.permission#READ_BASIC_PHONE_STATE](../android/Manifest.permission.md) or android.Manifest.permission.READ_PRIVILEGED_PHONE_STATE or [android.Manifest.permission#READ_PHONE_STATE](../android/Manifest.permission.md) or [carrier privileges](../android/telephony/TelephonyManager.md))

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `executor` | [Executor](../java/util/concurrent/Executor.md):The [Executor](../java/util/concurrent/Executor.md) where the`listener`will be invoked This value cannot be`null`. Callback and listener events are dispatched through this [Executor](../java/util/concurrent/Executor.md), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](../android/content/Context.md)). Otherwise, provide an [Executor](../java/util/concurrent/Executor.md) that dispatches to an appropriate thread. |
| `listener` | [SatelliteStateChangeListener](../android/telephony/satellite/SatelliteStateChangeListener.md):The listener to monitor the satellite state change This value cannot be`null`. |

**See Also**

- [android.telephony.satellite.SatelliteStateChangeListener](../android/telephony/satellite/SatelliteStateChangeListener.md)
- [android.telephony.TelephonyManager#hasCarrierPrivileges()](../android/telephony/TelephonyManager.md)) 

### unregisterStateChangeListener

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun unregisterStateChangeListener(listener: SatelliteStateChangeListener): Unit
```

Unregisters the [SatelliteStateChangeListener](../android/telephony/satellite/SatelliteStateChangeListener.md) previously registered with [registerStateChangeListener(java.util.concurrent.Executor,android.telephony.satellite.SatelliteStateChangeListener)](../android/telephony/satellite/SatelliteManager.md)).

It will be a no-op if the`listener`is not currently registered. 
Requires [android.Manifest.permission#READ_BASIC_PHONE_STATE](../android/Manifest.permission.md) or android.Manifest.permission.READ_PRIVILEGED_PHONE_STATE or [android.Manifest.permission#READ_PHONE_STATE](../android/Manifest.permission.md) or [carrier privileges](../android/telephony/TelephonyManager.md))

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [SatelliteStateChangeListener](../android/telephony/satellite/SatelliteStateChangeListener.md):The listener to unregister This value cannot be`null`. |

**See Also**

- [android.telephony.satellite.SatelliteStateChangeListener](../android/telephony/satellite/SatelliteStateChangeListener.md)
- [android.telephony.TelephonyManager#hasCarrierPrivileges()](../android/telephony/TelephonyManager.md))
