# EasyConnectStatusCallback

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# EasyConnectStatusCallback

Kotlin| [Java](https://developer.android.com/reference/android/net/wifi/EasyConnectStatusCallback "View this page in Java") 

```
abstract class EasyConnectStatusCallback
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.net.wifi.EasyConnectStatusCallback](https://developer.android.com/reference/kotlin/android/net/wifi/EasyConnectStatusCallback#) |

Easy Connect (DPP) Status Callback. Use this callback to get status updates (success, failure, progress) from the Easy Connect operations.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EASY_CONNECT_EVENT_FAILURE_AUTHENTICATION](https://developer.android.com/reference/kotlin/android/net/wifi/EasyConnectStatusCallback#EASY_CONNECT_EVENT_FAILURE_AUTHENTICATION:kotlin.Int) Easy Connect Failure event: Bootstrapping/Authentication initialization process failure. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EASY_CONNECT_EVENT_FAILURE_BUSY](https://developer.android.com/reference/kotlin/android/net/wifi/EasyConnectStatusCallback#EASY_CONNECT_EVENT_FAILURE_BUSY:kotlin.Int) Easy Connect Failure event: Easy Connect request while in another Easy Connect exchange. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EASY_CONNECT_EVENT_FAILURE_CANNOT_FIND_NETWORK](https://developer.android.com/reference/kotlin/android/net/wifi/EasyConnectStatusCallback#EASY_CONNECT_EVENT_FAILURE_CANNOT_FIND_NETWORK:kotlin.Int) Easy Connect R2 Failure event: Enrollee cannot find the network. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EASY_CONNECT_EVENT_FAILURE_CONFIGURATION](https://developer.android.com/reference/kotlin/android/net/wifi/EasyConnectStatusCallback#EASY_CONNECT_EVENT_FAILURE_CONFIGURATION:kotlin.Int) Easy Connect Failure event: Configuration process has failed due to malformed message. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EASY_CONNECT_EVENT_FAILURE_ENROLLEE_AUTHENTICATION](https://developer.android.com/reference/kotlin/android/net/wifi/EasyConnectStatusCallback#EASY_CONNECT_EVENT_FAILURE_ENROLLEE_AUTHENTICATION:kotlin.Int) Easy Connect R2 Failure event: Enrollee failed to authenticate with the network. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EASY_CONNECT_EVENT_FAILURE_ENROLLEE_FAILED_TO_SCAN_NETWORK_CHANNEL](https://developer.android.com/reference/kotlin/android/net/wifi/EasyConnectStatusCallback#EASY_CONNECT_EVENT_FAILURE_ENROLLEE_FAILED_TO_SCAN_NETWORK_CHANNEL:kotlin.Int) Easy Connect Failure event: Enrollee didn't scan the network's operating channel. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EASY_CONNECT_EVENT_FAILURE_ENROLLEE_REJECTED_CONFIGURATION](https://developer.android.com/reference/kotlin/android/net/wifi/EasyConnectStatusCallback#EASY_CONNECT_EVENT_FAILURE_ENROLLEE_REJECTED_CONFIGURATION:kotlin.Int) Easy Connect R2 Failure event: Enrollee rejected the configuration. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EASY_CONNECT_EVENT_FAILURE_GENERIC](https://developer.android.com/reference/kotlin/android/net/wifi/EasyConnectStatusCallback#EASY_CONNECT_EVENT_FAILURE_GENERIC:kotlin.Int) Easy Connect Failure event: General protocol failure. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EASY_CONNECT_EVENT_FAILURE_INVALID_NETWORK](https://developer.android.com/reference/kotlin/android/net/wifi/EasyConnectStatusCallback#EASY_CONNECT_EVENT_FAILURE_INVALID_NETWORK:kotlin.Int) Easy Connect Failure event: Invalid network provided to Easy Connect configurator. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EASY_CONNECT_EVENT_FAILURE_INVALID_URI](https://developer.android.com/reference/kotlin/android/net/wifi/EasyConnectStatusCallback#EASY_CONNECT_EVENT_FAILURE_INVALID_URI:kotlin.Int) Easy Connect Failure event: Scanned QR code is either not a Easy Connect URI, or the Easy Connect URI has errors. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EASY_CONNECT_EVENT_FAILURE_NOT_COMPATIBLE](https://developer.android.com/reference/kotlin/android/net/wifi/EasyConnectStatusCallback#EASY_CONNECT_EVENT_FAILURE_NOT_COMPATIBLE:kotlin.Int) Easy Connect Failure event: Both devices are implementing the same role and are incompatible. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EASY_CONNECT_EVENT_FAILURE_NOT_SUPPORTED](https://developer.android.com/reference/kotlin/android/net/wifi/EasyConnectStatusCallback#EASY_CONNECT_EVENT_FAILURE_NOT_SUPPORTED:kotlin.Int) Easy Connect Failure event: Feature or option is not supported. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EASY_CONNECT_EVENT_FAILURE_TIMEOUT](https://developer.android.com/reference/kotlin/android/net/wifi/EasyConnectStatusCallback#EASY_CONNECT_EVENT_FAILURE_TIMEOUT:kotlin.Int) Easy Connect Failure event: No response from the peer. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EASY_CONNECT_EVENT_FAILURE_URI_GENERATION](https://developer.android.com/reference/kotlin/android/net/wifi/EasyConnectStatusCallback#EASY_CONNECT_EVENT_FAILURE_URI_GENERATION:kotlin.Int) Easy Connect Failure event: System failed to generate DPP URI. |

## Constants

### EASY_CONNECT_EVENT_FAILURE_AUTHENTICATION

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EASY_CONNECT_EVENT_FAILURE_AUTHENTICATION: Int
```

Easy Connect Failure event: Bootstrapping/Authentication initialization process failure. 

 Value: -2

### EASY_CONNECT_EVENT_FAILURE_BUSY

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EASY_CONNECT_EVENT_FAILURE_BUSY: Int
```

Easy Connect Failure event: Easy Connect request while in another Easy Connect exchange. 

 Value: -5

### EASY_CONNECT_EVENT_FAILURE_CANNOT_FIND_NETWORK

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EASY_CONNECT_EVENT_FAILURE_CANNOT_FIND_NETWORK: Int
```

Easy Connect R2 Failure event: Enrollee cannot find the network. 

 Value: -10

### EASY_CONNECT_EVENT_FAILURE_CONFIGURATION

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EASY_CONNECT_EVENT_FAILURE_CONFIGURATION: Int
```

Easy Connect Failure event: Configuration process has failed due to malformed message. 

 Value: -4

### EASY_CONNECT_EVENT_FAILURE_ENROLLEE_AUTHENTICATION

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EASY_CONNECT_EVENT_FAILURE_ENROLLEE_AUTHENTICATION: Int
```

Easy Connect R2 Failure event: Enrollee failed to authenticate with the network. 

 Value: -11

### EASY_CONNECT_EVENT_FAILURE_ENROLLEE_FAILED_TO_SCAN_NETWORK_CHANNEL

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EASY_CONNECT_EVENT_FAILURE_ENROLLEE_FAILED_TO_SCAN_NETWORK_CHANNEL: Int
```

Easy Connect Failure event: Enrollee didn't scan the network's operating channel. This error is generated when framework finds that Network's operating channel is not included in the list of channels the Enrollee scanned in attempting to discover the network prior to connection. 

 Value: -14

### EASY_CONNECT_EVENT_FAILURE_ENROLLEE_REJECTED_CONFIGURATION

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EASY_CONNECT_EVENT_FAILURE_ENROLLEE_REJECTED_CONFIGURATION: Int
```

Easy Connect R2 Failure event: Enrollee rejected the configuration. 

 Value: -12

### EASY_CONNECT_EVENT_FAILURE_GENERIC

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EASY_CONNECT_EVENT_FAILURE_GENERIC: Int
```

Easy Connect Failure event: General protocol failure. 

 Value: -7

### EASY_CONNECT_EVENT_FAILURE_INVALID_NETWORK

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EASY_CONNECT_EVENT_FAILURE_INVALID_NETWORK: Int
```

Easy Connect Failure event: Invalid network provided to Easy Connect configurator. Network must either be WPA3-Personal (SAE) or WPA2-Personal (PSK). 

 Value: -9

### EASY_CONNECT_EVENT_FAILURE_INVALID_URI

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EASY_CONNECT_EVENT_FAILURE_INVALID_URI: Int
```

Easy Connect Failure event: Scanned QR code is either not a Easy Connect URI, or the Easy Connect URI has errors. 

 Value: -1

### EASY_CONNECT_EVENT_FAILURE_NOT_COMPATIBLE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EASY_CONNECT_EVENT_FAILURE_NOT_COMPATIBLE: Int
```

Easy Connect Failure event: Both devices are implementing the same role and are incompatible. 

 Value: -3

### EASY_CONNECT_EVENT_FAILURE_NOT_SUPPORTED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EASY_CONNECT_EVENT_FAILURE_NOT_SUPPORTED: Int
```

Easy Connect Failure event: Feature or option is not supported. 

 Value: -8

### EASY_CONNECT_EVENT_FAILURE_TIMEOUT

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EASY_CONNECT_EVENT_FAILURE_TIMEOUT: Int
```

Easy Connect Failure event: No response from the peer. 

 Value: -6

### EASY_CONNECT_EVENT_FAILURE_URI_GENERATION

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EASY_CONNECT_EVENT_FAILURE_URI_GENERATION: Int
```

Easy Connect Failure event: System failed to generate DPP URI. 

 Value: -13
