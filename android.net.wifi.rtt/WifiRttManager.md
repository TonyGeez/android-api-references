# WifiRttManager

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# WifiRttManager

Kotlin| [Java](../android/net/wifi/rtt/WifiRttManager.md) 
| --- | --- |

```
open class WifiRttManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.net.wifi.rtt.WifiRttManager](../android/net/wifi/rtt/WifiRttManager.md) |

This class provides the primary API for measuring distance (range) to other devices using the IEEE 802.11mc Wi-Fi Round Trip Time (RTT) technology.

The devices which can be ranged include:
- Access Points (APs)
- Wi-Fi Aware peersRanging requests are triggered using [startRanging(android.net.wifi.rtt.RangingRequest,java.util.concurrent.Executor,android.net.wifi.rtt.RangingResultCallback)](../android/net/wifi/rtt/WifiRttManager.md)). Results (in case of successful operation) are returned in the [RangingResultCallback.onRangingResults(List)](../android/net/wifi/rtt/RangingResultCallback.md))callback.

 Wi-Fi RTT may not be usable at some points, e.g. when Wi-Fi is disabled. To validate that the functionality is available use the [isAvailable()](../android/net/wifi/rtt/WifiRttManager.md))function. To track changes in RTT usability register for the [ACTION_WIFI_RTT_STATE_CHANGED](../android/net/wifi/rtt/WifiRttManager.md) broadcast. Note that this broadcast is not sticky - you should register for it and then check the above API to avoid a race condition. 
 Restricted for SDK Runtime environment in API level 34.

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ACTION_WIFI_RTT_STATE_CHANGED](../android/net/wifi/rtt/WifiRttManager.md) Broadcast intent action to indicate that the state of Wi-Fi RTT availability has changed. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [CHARACTERISTICS_KEY_BOOLEAN_LCI](../android/net/wifi/rtt/WifiRttManager.md) Bundle key to access if getting the Location Configuration Information(LCI) from responder is supported. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [CHARACTERISTICS_KEY_BOOLEAN_LCR](../android/net/wifi/rtt/WifiRttManager.md) Bundle key to access if getting the Location Civic Report(LCR) from responder is supported. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [CHARACTERISTICS_KEY_BOOLEAN_NTB_INITIATOR](../android/net/wifi/rtt/WifiRttManager.md) Bundle key to access if device supports to be a IEEE 802. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [CHARACTERISTICS_KEY_BOOLEAN_ONE_SIDED_RTT](../android/net/wifi/rtt/WifiRttManager.md) Bundle key to access if one-sided Wi-Fi RTT is supported. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [CHARACTERISTICS_KEY_BOOLEAN_RANGING_FRAME_PROTECTION_SUPPORTED](../android/net/wifi/rtt/WifiRttManager.md) Bundle key to access if device supports ranging frame protection. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [CHARACTERISTICS_KEY_BOOLEAN_SECURE_HE_LTF_SUPPORTED](../android/net/wifi/rtt/WifiRttManager.md) Bundle key to access if device supports secure HE-LTF (High Efficiency Long Training Field). |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [CHARACTERISTICS_KEY_BOOLEAN_STA_RESPONDER](../android/net/wifi/rtt/WifiRttManager.md) Bundle key to access if device supports to be a responder in station mode |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [CHARACTERISTICS_KEY_INT_MAX_SUPPORTED_SECURE_HE_LTF_PROTO_VERSION](../android/net/wifi/rtt/WifiRttManager.md) Bundle key to access the maximum supported secure HE-LTF protocol version. |
| --- | --- |

| Public methods ||
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Bundle](../android/os/Bundle.md) | [getRttCharacteristics](../android/net/wifi/rtt/WifiRttManager.md))`()` Returns a Bundle which represents the characteristics of the Wi-Fi RTT interface: a set of parameters which specify feature support. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isAvailable](../android/net/wifi/rtt/WifiRttManager.md))`()` Returns the current status of RTT API: whether or not RTT is available. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [startRanging](../android/net/wifi/rtt/WifiRttManager.md))`(`request:` ` [RangingRequest](../android/net/wifi/rtt/RangingRequest.md)`, `executor:` ` [Executor](../java/util/concurrent/Executor.md)`, `callback:` ` [RangingResultCallback](../android/net/wifi/rtt/RangingResultCallback.md)`)` Initiate a request to range to a set of devices specified in the [RangingRequest](../android/net/wifi/rtt/RangingRequest.md). |
| --- | --- |

## Constants

### ACTION_WIFI_RTT_STATE_CHANGED

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACTION_WIFI_RTT_STATE_CHANGED: String
```

Broadcast intent action to indicate that the state of Wi-Fi RTT availability has changed. Use the [isAvailable()](../android/net/wifi/rtt/WifiRttManager.md))to query the current status. This broadcast is**not** sticky, use the [isAvailable()](../android/net/wifi/rtt/WifiRttManager.md))API after registering the broadcast to check the current state of Wi-Fi RTT.

Note: The broadcast is only delivered to registered receivers - no manifest registered components will be launched. 

 Value: "android.net.wifi.rtt.action.WIFI_RTT_STATE_CHANGED"

### CHARACTERISTICS_KEY_BOOLEAN_LCI

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CHARACTERISTICS_KEY_BOOLEAN_LCI: String
```

Bundle key to access if getting the Location Configuration Information(LCI) from responder is supported. 

 Value: "key_lci"

**See Also**

- [android.net.wifi.rtt.ResponderLocation](../android/net/wifi/rtt/ResponderLocation.md) 

### CHARACTERISTICS_KEY_BOOLEAN_LCR

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CHARACTERISTICS_KEY_BOOLEAN_LCR: String
```

Bundle key to access if getting the Location Civic Report(LCR) from responder is supported. 

 Value: "key_lcr"

**See Also**

- [android.net.wifi.rtt.ResponderLocation](../android/net/wifi/rtt/ResponderLocation.md) 

### CHARACTERISTICS_KEY_BOOLEAN_NTB_INITIATOR

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CHARACTERISTICS_KEY_BOOLEAN_NTB_INITIATOR: String
```

Bundle key to access if device supports to be a IEEE 802.11az non-trigger based initiator 

 Value: "key_ntb_initiator"

### CHARACTERISTICS_KEY_BOOLEAN_ONE_SIDED_RTT

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CHARACTERISTICS_KEY_BOOLEAN_ONE_SIDED_RTT: String
```

Bundle key to access if one-sided Wi-Fi RTT is supported. When it is not supported, only two-sided RTT can be performed, which requires responder supports IEEE 802.11mc and this can be determined by the method [ScanResult.is80211mcResponder()](../android/net/wifi/ScanResult.md)) 

 Value: "key_one_sided_rtt"

### CHARACTERISTICS_KEY_BOOLEAN_RANGING_FRAME_PROTECTION_SUPPORTED

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CHARACTERISTICS_KEY_BOOLEAN_RANGING_FRAME_PROTECTION_SUPPORTED: String
```

Bundle key to access if device supports ranging frame protection. IEEE 802.11az introduces Protected Management Frames for FTM (Fine Timing Measurement), adding a layer of encryption and integrity protection to these frames. 

 Value: "key_rnm_mfp_supported"

### CHARACTERISTICS_KEY_BOOLEAN_SECURE_HE_LTF_SUPPORTED

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CHARACTERISTICS_KEY_BOOLEAN_SECURE_HE_LTF_SUPPORTED: String
```

Bundle key to access if device supports secure HE-LTF (High Efficiency Long Training Field). Secure HE-LTF is a critical security enhancement in the IEEE 802.11az standard that aims to protect ranging measurements from spoofing and manipulation. 

 Value: "key_secure_he_ltf_supported"

### CHARACTERISTICS_KEY_BOOLEAN_STA_RESPONDER

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CHARACTERISTICS_KEY_BOOLEAN_STA_RESPONDER: String
```

Bundle key to access if device supports to be a responder in station mode 

 Value: "key_sta_responder"

### CHARACTERISTICS_KEY_INT_MAX_SUPPORTED_SECURE_HE_LTF_PROTO_VERSION

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CHARACTERISTICS_KEY_INT_MAX_SUPPORTED_SECURE_HE_LTF_PROTO_VERSION: String
```

Bundle key to access the maximum supported secure HE-LTF protocol version. 

 Value: "key_max_supported_secure_he_ltf_proto_ver"

## Public methods

### getRttCharacteristics

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getRttCharacteristics(): Bundle
```

Returns a Bundle which represents the characteristics of the Wi-Fi RTT interface: a set of parameters which specify feature support. Each parameter can be accessed by the specified Bundle key, one of the`CHARACTERISTICS_KEY_*`value.

May return an empty Bundle if the Wi-Fi RTT service is not initialized. 
Requires [android.Manifest.permission#ACCESS_WIFI_STATE](../android/Manifest.permission.md)

| Return ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [Bundle](../android/os/Bundle.md) | A Bundle specifying feature support of RTT. This value cannot be`null`. |

### isAvailable

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isAvailable(): Boolean
```

Returns the current status of RTT API: whether or not RTT is available. To track changes in the state of RTT API register for the [ACTION_WIFI_RTT_STATE_CHANGED](../android/net/wifi/rtt/WifiRttManager.md) broadcast.

Note: availability of RTT does not mean that the app can use the API. The app's permissions and platform Location Mode are validated at run-time.

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | A boolean indicating whether the app can use the RTT API at this time (true) or not (false). |

### startRanging

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun startRanging(
    request: RangingRequest, 
    executor: Executor, 
    callback: RangingResultCallback
): Unit
```

Initiate a request to range to a set of devices specified in the [RangingRequest](../android/net/wifi/rtt/RangingRequest.md). Results will be returned in the [RangingResultCallback](../android/net/wifi/rtt/RangingResultCallback.md) set of callbacks.

Ranging request with only Wifi Aware peers can be performed with either [android.Manifest.permission#NEARBY_WIFI_DEVICES](../android/Manifest.permission.md) with android:usesPermissionFlags="neverForLocation", or [android.Manifest.permission#ACCESS_FINE_LOCATION](../android/Manifest.permission.md). All other types of ranging requests require [android.Manifest.permission#ACCESS_FINE_LOCATION](../android/Manifest.permission.md). 
Requires [android.Manifest.permission#ACCESS_FINE_LOCATION](../android/Manifest.permission.md) and [android.Manifest.permission#CHANGE_WIFI_STATE](../android/Manifest.permission.md) and [android.Manifest.permission#ACCESS_WIFI_STATE](../android/Manifest.permission.md) and [android.Manifest.permission#NEARBY_WIFI_DEVICES](../android/Manifest.permission.md)

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `request` | [RangingRequest](../android/net/wifi/rtt/RangingRequest.md):A request specifying a set of devices whose distance measurements are requested. This value cannot be`null`. |
| `executor` | [Executor](../java/util/concurrent/Executor.md):The Executor on which to run the callback. This value cannot be`null`. Callback and listener events are dispatched through this [Executor](../java/util/concurrent/Executor.md), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](../android/content/Context.md)). Otherwise, provide an [Executor](../java/util/concurrent/Executor.md) that dispatches to an appropriate thread. |
| `callback` | [RangingResultCallback](../android/net/wifi/rtt/RangingResultCallback.md):A callback for the result of the ranging request. This value cannot be`null`. |
| --- | --- |
