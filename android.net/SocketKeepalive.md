# SocketKeepalive

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SocketKeepalive

Kotlin| [Java](../android/net/SocketKeepalive.md) 
| --- | --- |

```
abstract class SocketKeepalive : AutoCloseable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.net.SocketKeepalive](../android/net/SocketKeepalive.md) |

Allows applications to request that the system periodically send specific packets on their behalf, using hardware offload to save battery power. To request that the system send keepalives, call one of the methods that return a [SocketKeepalive](../android/net/SocketKeepalive.md) object, such as [ConnectivityManager.createSocketKeepalive](../android/net/ConnectivityManager.md)), passing in a non-null callback. If the [SocketKeepalive](../android/net/SocketKeepalive.md) is successfully started, the callback's`onStarted`method will be called. If an error occurs,`onError`will be called, specifying one of the`ERROR_*`constants in this class. To stop an existing keepalive, call [SocketKeepalive.stop](../android/net/SocketKeepalive.md)). The system will call [SocketKeepalive.Callback.onStopped](../android/net/SocketKeepalive.Callback.md))if the operation was successful or [SocketKeepalive.Callback.onError](../android/net/SocketKeepalive.Callback.md))if an error occurred. For cellular, the device MUST support at least 1 keepalive slot. For WiFi, the device SHOULD support keepalive offload. If it does not, it MUST reply with [SocketKeepalive.Callback.onError](../android/net/SocketKeepalive.Callback.md))with`ERROR_UNSUPPORTED`to any keepalive offload request. If it does, it MUST support at least 3 concurrent keepalive slots.

## Summary

| Nested classes ||
|------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open | [Callback](../android/net/SocketKeepalive.Callback.md) The callback which app can use to learn the status changes of [SocketKeepalive](../android/net/SocketKeepalive.md). |

| Constants ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_HARDWARE_ERROR](../android/net/SocketKeepalive.md) There was a hardware error. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_INSUFFICIENT_RESOURCES](../android/net/SocketKeepalive.md) Resources are insufficient (e.g. all hardware slots are in use). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_INVALID_INTERVAL](../android/net/SocketKeepalive.md) The interval is invalid (e.g. too short). |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_INVALID_IP_ADDRESS](../android/net/SocketKeepalive.md) The invalid IP addresses. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_INVALID_LENGTH](../android/net/SocketKeepalive.md) The length is invalid (e.g. too long). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_INVALID_NETWORK](../android/net/SocketKeepalive.md) The invalid network. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_INVALID_PORT](../android/net/SocketKeepalive.md) The port is invalid. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_INVALID_SOCKET](../android/net/SocketKeepalive.md) The socket is invalid. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_SOCKET_NOT_IDLE](../android/net/SocketKeepalive.md) The socket is not idle. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_UNSUPPORTED](../android/net/SocketKeepalive.md) The request is unsupported. |

| Public methods ||
|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](../android/net/SocketKeepalive.md))`()` Deactivate this [SocketKeepalive](../android/net/SocketKeepalive.md) and free allocated resources. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [start](../android/net/SocketKeepalive.md))`(`intervalSec:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Request that keepalive be started with the given`intervalSec`. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [stop](../android/net/SocketKeepalive.md))`()` Requests that keepalive be stopped. |
| --- | --- |

## Constants

### ERROR_HARDWARE_ERROR

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_HARDWARE_ERROR: Int
```

There was a hardware error. 

 Value: -31

### ERROR_INSUFFICIENT_RESOURCES

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_INSUFFICIENT_RESOURCES: Int
```

Resources are insufficient (e.g. all hardware slots are in use). 

 Value: -32

### ERROR_INVALID_INTERVAL

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_INVALID_INTERVAL: Int
```

The interval is invalid (e.g. too short). 

 Value: -24

### ERROR_INVALID_IP_ADDRESS

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_INVALID_IP_ADDRESS: Int
```

The invalid IP addresses. Indicates the specified IP addresses are invalid. For example, the specified source IP address is not configured on the specified`Network`. 

 Value: -21

### ERROR_INVALID_LENGTH

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_INVALID_LENGTH: Int
```

The length is invalid (e.g. too long). 

 Value: -23

### ERROR_INVALID_NETWORK

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_INVALID_NETWORK: Int
```

The invalid network. It indicates the specified`Network`is not connected. 

 Value: -20

### ERROR_INVALID_PORT

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_INVALID_PORT: Int
```

The port is invalid. 

 Value: -22

### ERROR_INVALID_SOCKET

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_INVALID_SOCKET: Int
```

The socket is invalid. 

 Value: -25

### ERROR_SOCKET_NOT_IDLE

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_SOCKET_NOT_IDLE: Int
```

The socket is not idle. 

 Value: -26

### ERROR_UNSUPPORTED

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_UNSUPPORTED: Int
```

The request is unsupported. 

 Value: -30

## Public methods

### close

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun close(): Unit
```

Deactivate this [SocketKeepalive](../android/net/SocketKeepalive.md) and free allocated resources. The instance won't be usable again if`close()`is called.

| Exceptions ||
|-----------------------|-----------------------------------|
| `java.lang.Exception` | if this resource cannot be closed |

### start

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun start(intervalSec: Int): Unit
```

Request that keepalive be started with the given`intervalSec`. See [SocketKeepalive](../android/net/SocketKeepalive.md). If the remote binder dies, or the binder call throws an exception when invoking start or stop of the [SocketKeepalive](../android/net/SocketKeepalive.md), a [RuntimeException](../java/lang/RuntimeException.md) caused by a [RemoteException](../android/os/RemoteException.md) will be thrown into the [Executor](../java/util/concurrent/Executor.md). This is typically not important to catch because the remote party is the system, so if it is not in shape to communicate through binder the system is going down anyway. If the caller still cares, it can use a custom [Executor](../java/util/concurrent/Executor.md) to catch the [RuntimeException](../java/lang/RuntimeException.md).

| Parameters ||
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `intervalSec` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The target interval in seconds between keepalive packet transmissions. The interval should be between 10 seconds and 3600 seconds, otherwise [ERROR_INVALID_INTERVAL](../android/net/SocketKeepalive.md) will be returned. Value is between android.net.SocketKeepalive#MIN_INTERVAL_SEC and android.net.SocketKeepalive#MAX_INTERVAL_SEC inclusive |

### stop

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun stop(): Unit
```

Requests that keepalive be stopped. The application must wait for [Callback.onStopped](../android/net/SocketKeepalive.Callback.md))before using the object. See [SocketKeepalive](../android/net/SocketKeepalive.md).
