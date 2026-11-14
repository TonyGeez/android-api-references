# RangingManager

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RangingManager

Kotlin| [Java](../android/ranging/RangingManager.md) 
| --- | --- |

```
class RangingManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.ranging.RangingManager](../android/ranging/RangingManager.md) |

This class provides a way to perform ranging operations such as querying the device's capabilities and determining the distance and angle between the local device and a remote device.

To get a [RangingManager](../android/ranging/RangingManager.md), call the`Context.getSystemService(RangingManager.class)`. 
Restricted for SDK Runtime environment in API level 36.

## Summary

| Nested classes ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [RangingCapabilitiesCallback](../android/ranging/RangingManager.RangingCapabilitiesCallback.md) Callback interface to receive the availabilities and capabilities of all the ranging technology supported by the device. |

| Constants ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BLE_CS](../android/ranging/RangingManager.md) Bluetooth Channel Sounding (BT-CS) technology. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BLE_RSSI](../android/ranging/RangingManager.md) Bluetooth Low Energy (BLE) RSSI-based ranging technology. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [UWB](../android/ranging/RangingManager.md) Ultra-Wideband (UWB) technology. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [WIFI_NAN_RTT](../android/ranging/RangingManager.md) WiFi Round Trip Time (WiFi-RTT) technology. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [WIFI_STA_RTT](../android/ranging/RangingManager.md) WiFi Round Trip Time (WiFi-RTT 8011MC) technology. |

| Public methods ||
|--------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [RangingSession](../android/ranging/RangingSession.md)? | [createRangingSession](../android/ranging/RangingManager.md))`(`executor:` ` [Executor](../java/util/concurrent/Executor.md)`, `callback:` ` [RangingSession.Callback](../android/ranging/RangingSession.Callback.md)`)` Creates a new ranging session. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerCapabilitiesCallback](../android/ranging/RangingManager.md))`(`executor:` ` [Executor](../java/util/concurrent/Executor.md)`, `callback:` ` [RangingManager.RangingCapabilitiesCallback](../android/ranging/RangingManager.RangingCapabilitiesCallback.md)`)` Registers a callback to receive ranging capabilities updates. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unregisterCapabilitiesCallback](../android/ranging/RangingManager.md))`(`callback:` ` [RangingManager.RangingCapabilitiesCallback](../android/ranging/RangingManager.RangingCapabilitiesCallback.md)`)` Unregisters a previously registered ranging capabilities callback. |
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

This method returns a [RangingSession](../android/ranging/RangingSession.md) instance, which can be used to initiate, manage, and stop ranging operations. The provided [RangingSession.Callback](../android/ranging/RangingSession.Callback.md) will be used to receive session-related events, such as session start, stop, and ranging updates.

It is recommended to provide an appropriate [Executor](../java/util/concurrent/Executor.md) to ensure that callback events are handled on a suitable thread.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `callback` | [RangingSession.Callback](../android/ranging/RangingSession.Callback.md):the [RangingSession.Callback](../android/ranging/RangingSession.Callback.md) to handle session-related events. Must not be`null`. |
| `executor` | [Executor](../java/util/concurrent/Executor.md):the [Executor](../java/util/concurrent/Executor.md) on which the callback will be invoked. Must not be`null`. |

| Return ||
|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [RangingSession](../android/ranging/RangingSession.md)? | the [RangingSession](../android/ranging/RangingSession.md) instance if the session was successfully created, or`null`if the session could not be created. |

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
| `executor` | [Executor](../java/util/concurrent/Executor.md):The [Executor](../java/util/concurrent/Executor.md) on which the callback will be executed. Must not be null. Callback and listener events are dispatched through this [Executor](../java/util/concurrent/Executor.md), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](../android/content/Context.md)). Otherwise, provide an [Executor](../java/util/concurrent/Executor.md) that dispatches to an appropriate thread. |
| `callback` | [RangingManager.RangingCapabilitiesCallback](../android/ranging/RangingManager.RangingCapabilitiesCallback.md):The [RangingCapabilitiesCallback](../android/ranging/RangingManager.RangingCapabilitiesCallback.md) that will handle the capabilities updates. Must not be null. |

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
| `callback` | [RangingManager.RangingCapabilitiesCallback](../android/ranging/RangingManager.RangingCapabilitiesCallback.md):The [RangingCapabilitiesCallback](../android/ranging/RangingManager.RangingCapabilitiesCallback.md) to be unregistered. Must not be null. |

| Return ||
|------------------------------------------------------------------------------|-----------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | This value cannot be`null`. |

| Exceptions ||
|----------------------------------|--------------------------|
| `java.lang.NullPointerException` | if the`callback`is null. |
