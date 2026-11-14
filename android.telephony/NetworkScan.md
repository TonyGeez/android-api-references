# NetworkScan

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# NetworkScan

Kotlin| [Java](https://developer.android.com/reference/android/telephony/NetworkScan "View this page in Java") 

```
open class NetworkScan
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.telephony.NetworkScan](https://developer.android.com/reference/kotlin/android/telephony/NetworkScan#) |

The caller of android.telephony.TelephonyManager#requestNetworkScan(android.telephony.NetworkScanRequest,Executor,NetworkScanCallback) will receive an instance of [NetworkScan](https://developer.android.com/reference/kotlin/android/telephony/NetworkScan#), which contains a callback method [stopScan()](https://developer.android.com/reference/kotlin/android/telephony/NetworkScan#stopScan())for stopping the in-progress scan.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_INTERRUPTED](https://developer.android.com/reference/kotlin/android/telephony/NetworkScan#ERROR_INTERRUPTED:kotlin.Int) The scan has been interrupted by another scan with higher priority. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_INVALID_SCAN](https://developer.android.com/reference/kotlin/android/telephony/NetworkScan#ERROR_INVALID_SCAN:kotlin.Int) The parameters of the scan is invalid. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_INVALID_SCANID](https://developer.android.com/reference/kotlin/android/telephony/NetworkScan#ERROR_INVALID_SCANID:kotlin.Int) The scan ID is invalid. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_MODEM_ERROR](https://developer.android.com/reference/kotlin/android/telephony/NetworkScan#ERROR_MODEM_ERROR:kotlin.Int) The scan has failed due to some modem errors. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_MODEM_UNAVAILABLE](https://developer.android.com/reference/kotlin/android/telephony/NetworkScan#ERROR_MODEM_UNAVAILABLE:kotlin.Int) The modem can not perform the scan because it is doing something else. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_RADIO_INTERFACE_ERROR](https://developer.android.com/reference/kotlin/android/telephony/NetworkScan#ERROR_RADIO_INTERFACE_ERROR:kotlin.Int) The RIL returns nothing or exceptions. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_UNSUPPORTED](https://developer.android.com/reference/kotlin/android/telephony/NetworkScan#ERROR_UNSUPPORTED:kotlin.Int) The modem does not support the request scan. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SUCCESS](https://developer.android.com/reference/kotlin/android/telephony/NetworkScan#SUCCESS:kotlin.Int) The RIL has successfully performed the network scan. |

| Public methods ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [stopScan](https://developer.android.com/reference/kotlin/android/telephony/NetworkScan#stopScan())`()` Stops the network scan Use this method to stop an ongoing scan. |

## Constants

### ERROR_INTERRUPTED

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_INTERRUPTED: Int
```

The scan has been interrupted by another scan with higher priority. 

 Value: 10002

### ERROR_INVALID_SCAN

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_INVALID_SCAN: Int
```

The parameters of the scan is invalid. 

 Value: 2

### ERROR_INVALID_SCANID

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_INVALID_SCANID: Int
```

The scan ID is invalid. The user is either trying to stop a scan which does not exist or started by others. 

 Value: 10001

### ERROR_MODEM_ERROR

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_MODEM_ERROR: Int
```

The scan has failed due to some modem errors. 

 Value: 1

### ERROR_MODEM_UNAVAILABLE

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_MODEM_UNAVAILABLE: Int
```

The modem can not perform the scan because it is doing something else. 

 Value: 3

### ERROR_RADIO_INTERFACE_ERROR

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_RADIO_INTERFACE_ERROR: Int
```

The RIL returns nothing or exceptions. 

 Value: 10000

### ERROR_UNSUPPORTED

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_UNSUPPORTED: Int
```

The modem does not support the request scan. 

 Value: 4

### SUCCESS

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SUCCESS: Int
```

The RIL has successfully performed the network scan. 

 Value: 0

## Public methods

### stopScan

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun stopScan(): Unit
```

Stops the network scan Use this method to stop an ongoing scan. When user requests a new scan, a [NetworkScan](https://developer.android.com/reference/kotlin/android/telephony/NetworkScan#) object will be returned, and the user can stop the scan by calling this method.
