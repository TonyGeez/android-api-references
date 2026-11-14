# RangingManager

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RangingManager

Kotlin| [Java](https://developer.android.com/reference/android/ranging/RangingManager "View this page in Java") 
| --- | --- |

```
class RangingManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.ranging.RangingManager](https://developer.android.com/reference/kotlin/android/ranging/RangingManager#) |

This class provides a way to perform ranging operations such as querying the device's capabilities and determining the distance and angle between the local device and a remote device.

To get a [RangingManager](https://developer.android.com/reference/kotlin/android/ranging/RangingManager#), call the`Context.getSystemService(RangingManager.class)`. 
Restricted for SDK Runtime environment in API level 36.

## Summary

| Nested classes ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [RangingCapabilitiesCallback](https://developer.android.com/reference/kotlin/android/ranging/RangingManager.RangingCapabilitiesCallback) Callback interface to receive the availabilities and capabilities of all the ranging technology supported by the device. |

| Constants ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BLE_CS](https://developer.android.com/reference/kotlin/android/ranging/RangingManager#BLE_CS:kotlin.Int) Bluetooth Channel Sounding (BT-CS) technology. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BLE_RSSI](https://developer.android.com/reference/kotlin/android/ranging/RangingManager#BLE_RSSI:kotlin.Int) Bluetooth Low Energy (BLE) RSSI-based ranging technology. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [UWB](https://developer.android.com/reference/kotlin/android/ranging/RangingManager#UWB:kotlin.Int) Ultra-Wideband (UWB) technology. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [WIFI_NAN_RTT](https://developer.android.com/reference/kotlin/android/ranging/RangingManager#WIFI_NAN_RTT:kotlin.Int) WiFi Round Trip Time (WiFi-RTT) technology. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [WIFI_STA_RTT](https://developer.android.com/reference/kotlin/android/ranging/RangingManager#WIFI_STA_RTT:kotlin.Int) WiFi Round Trip Time (WiFi-RTT 8011MC) technology. |

| Public methods ||
|--------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [RangingSession](https://developer.android.com/reference/kotlin/android/ranging/RangingSession)? | [createRangingSession](https://developer.android.com/reference/kotlin/android/ranging/RangingManager#createRangingSession(java.util.concurrent.Executor,%20android.ranging.RangingSession.Callback))`(`executor:` ` [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#)`, `callback:` ` [RangingSession.Callback](https://developer.android.com/reference/kotlin/android/ranging/RangingSession.Callback)`)` Creates a new ranging session. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerCapabilitiesCallback](https://developer.android.com/reference/kotlin/android/ranging/RangingManager#registerCapabilitiesCallback(java.util.concurrent.Executor,%20android.ranging.RangingManager.RangingCapabilitiesCallback))`(`executor:` ` [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#)`, `callback:` ` [RangingManager.RangingCapabilitiesCallback](https://developer.android.com/reference/kotlin/android/ranging/RangingManager.RangingCapabilitiesCallback)`)` Registers a callback to receive ranging capabilities updates. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unregisterCapabilitiesCallback](https://developer.android.com/reference/kotlin/android/ranging/RangingManager#unregisterCapabilitiesCallback(android.ranging.RangingManager.RangingCapabilitiesCallback))`(`callback:` ` [RangingManager.RangingCapabilitiesCallback](https://developer.android.com/reference/kotlin/android/ranging/RangingManager.RangingCapabilitiesCallback)`)` Unregisters a previously registered ranging capabilities callback. |
| --- | --- |

## Constants

### BLE_CS

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BLE_CS: Int
```

Bluetooth Channel Sounding (BT-CS) technology. 

 Value: 1

### BLE_RSSI

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BLE_RSSI: Int
```

Bluetooth Low Energy (BLE) RSSI-based ranging technology. 

 Value: 3

### UWB

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val UWB: Int
```

Ultra-Wideband (UWB) technology. 

 Value: 0

### WIFI_NAN_RTT

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val WIFI_NAN_RTT: Int
```

WiFi Round Trip Time (WiFi-RTT) technology. 

 Value: 2

### WIFI_STA_RTT

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val WIFI_STA_RTT: Int
```

WiFi Round Trip Time (WiFi-RTT 8011MC) technology. 

 Value: 4

## Public methods

### createRangingSession

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun createRangingSession(
    executor: Executor, 
    callback: RangingSession.Callback
): RangingSession?
```

Creates a new ranging session. A ranging session enables the application to perform ranging operations using available technologies such as UWB (Ultra-Wideband) or WiFi RTT (Round Trip Time).

This method returns a [RangingSession](https://developer.android.com/reference/kotlin/android/ranging/RangingSession) instance, which can be used to initiate, manage, and stop ranging operations. The provided [RangingSession.Callback](https://developer.android.com/reference/kotlin/android/ranging/RangingSession.Callback) will be used to receive session-related events, such as session start, stop, and ranging updates.

It is recommended to provide an appropriate [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#) to ensure that callback events are handled on a suitable thread.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `callback` | [RangingSession.Callback](https://developer.android.com/reference/kotlin/android/ranging/RangingSession.Callback):the [RangingSession.Callback](https://developer.android.com/reference/kotlin/android/ranging/RangingSession.Callback) to handle session-related events. Must not be`null`. |
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#):the [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#) on which the callback will be invoked. Must not be`null`. |

| Return ||
|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [RangingSession](https://developer.android.com/reference/kotlin/android/ranging/RangingSession)? | the [RangingSession](https://developer.android.com/reference/kotlin/android/ranging/RangingSession) instance if the session was successfully created, or`null`if the session could not be created. |

| Exceptions ||
|----------------------------------|-----------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if`callback`or`executor`is null. |
| `java.lang.SecurityException` | if the calling app does not have the necessary permissions to create a ranging session. |

### registerCapabilitiesCallback

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun registerCapabilitiesCallback(
    executor: Executor, 
    callback: RangingManager.RangingCapabilitiesCallback
): Unit
```

Registers a callback to receive ranging capabilities updates.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#):The [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#) on which the callback will be executed. Must not be null. Callback and listener events are dispatched through this [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()). Otherwise, provide an [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#) that dispatches to an appropriate thread. |
| `callback` | [RangingManager.RangingCapabilitiesCallback](https://developer.android.com/reference/kotlin/android/ranging/RangingManager.RangingCapabilitiesCallback):The [RangingCapabilitiesCallback](https://developer.android.com/reference/kotlin/android/ranging/RangingManager.RangingCapabilitiesCallback) that will handle the capabilities updates. Must not be null. |

| Return ||
|------------------------------------------------------------------------------|-----------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | This value cannot be`null`. |

| Exceptions ||
|----------------------------------|--------------------------------------|
| `java.lang.NullPointerException` | if the`executor`or`callback`is null. |

### unregisterCapabilitiesCallback

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun unregisterCapabilitiesCallback(callback: RangingManager.RangingCapabilitiesCallback): Unit
```

Unregisters a previously registered ranging capabilities callback.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `callback` | [RangingManager.RangingCapabilitiesCallback](https://developer.android.com/reference/kotlin/android/ranging/RangingManager.RangingCapabilitiesCallback):The [RangingCapabilitiesCallback](https://developer.android.com/reference/kotlin/android/ranging/RangingManager.RangingCapabilitiesCallback) to be unregistered. Must not be null. |

| Return ||
|------------------------------------------------------------------------------|-----------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | This value cannot be`null`. |

| Exceptions ||
|----------------------------------|--------------------------|
| `java.lang.NullPointerException` | if the`callback`is null. |
