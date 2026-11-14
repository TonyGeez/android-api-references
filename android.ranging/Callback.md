# RangingSession.Callback

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Callback

Kotlin| [Java](../android/ranging/RangingSession.Callback.md) 
| --- | --- |

```
interface Callback
```

| [android.ranging.RangingSession.Callback](../android/ranging/RangingSession.Callback.md) |

Callback interface for receiving ranging session events.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [REASON_LOCAL_REQUEST](../android/ranging/RangingSession.Callback.md) Indicates that the session was closed because [AutoCloseable.close()](../java/lang/AutoCloseable.md))or [RangingSession.stop()](../android/ranging/RangingSession.md))was called. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [REASON_NO_PEERS_FOUND](../android/ranging/RangingSession.Callback.md) Indicates that the session was closed because none of the specified peers were found. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [REASON_REMOTE_REQUEST](../android/ranging/RangingSession.Callback.md) Indicates that the session was closed at the request of a remote peer. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [REASON_SYSTEM_POLICY](../android/ranging/RangingSession.Callback.md) Indicates that the local system policy forced the session to close, such as power management policy, airplane mode etc. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [REASON_UNKNOWN](../android/ranging/RangingSession.Callback.md) Indicates that the session was closed due to an unknown reason. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [REASON_UNSUPPORTED](../android/ranging/RangingSession.Callback.md) Indicates that the session closed because the provided session parameters were not supported. |
| --- | --- |

| Public methods ||
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onClosed](../android/ranging/RangingSession.Callback.md))`(`reason:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called when the ranging session has closed. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onOpenFailed](../android/ranging/RangingSession.Callback.md))`(`reason:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called when the ranging session failed to open. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onOpened](../android/ranging/RangingSession.Callback.md))`()` Called when the ranging session opens successfully. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onResults](../android/ranging/RangingSession.Callback.md))`(`peer:` ` [RangingDevice](../android/ranging/RangingDevice.md)`, `data:` ` [RangingData](../android/ranging/RangingData.md)`)` Called when ranging data has been received from a peer. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onStarted](../android/ranging/RangingSession.Callback.md))`(`peer:` ` [RangingDevice](../android/ranging/RangingDevice.md)`, `technology:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called when ranging has started with a particular peer using a particular technology during an ongoing session. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onStopped](../android/ranging/RangingSession.Callback.md))`(`peer:` ` [RangingDevice](../android/ranging/RangingDevice.md)`, `technology:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called when ranging has stopped with a particular peer using a particular technology during an ongoing session. |
| --- | --- |

## Constants

### REASON_LOCAL_REQUEST

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val REASON_LOCAL_REQUEST: Int
```

Indicates that the session was closed because [AutoCloseable.close()](../java/lang/AutoCloseable.md))or [RangingSession.stop()](../android/ranging/RangingSession.md))was called. 

 Value: 1

### REASON_NO_PEERS_FOUND

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val REASON_NO_PEERS_FOUND: Int
```

Indicates that the session was closed because none of the specified peers were found. 

 Value: 5

### REASON_REMOTE_REQUEST

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val REASON_REMOTE_REQUEST: Int
```

Indicates that the session was closed at the request of a remote peer. 

 Value: 2

### REASON_SYSTEM_POLICY

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val REASON_SYSTEM_POLICY: Int
```

Indicates that the local system policy forced the session to close, such as power management policy, airplane mode etc. 

 Value: 4

### REASON_UNKNOWN

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val REASON_UNKNOWN: Int
```

Indicates that the session was closed due to an unknown reason. 

 Value: 0

### REASON_UNSUPPORTED

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val REASON_UNSUPPORTED: Int
```

Indicates that the session closed because the provided session parameters were not supported. 

 Value: 3

## Public methods

### onClosed

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onClosed(reason: Int): Unit
```

Called when the ranging session has closed.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `reason` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the reason why the session was closed, limited to values defined by android.ranging.RangingSession.Callback.Reason. Value is [android.ranging.RangingSession.Callback#REASON_UNKNOWN](../android/ranging/RangingSession.Callback.md), [android.ranging.RangingSession.Callback#REASON_LOCAL_REQUEST](../android/ranging/RangingSession.Callback.md), [android.ranging.RangingSession.Callback#REASON_REMOTE_REQUEST](../android/ranging/RangingSession.Callback.md), [android.ranging.RangingSession.Callback#REASON_UNSUPPORTED](../android/ranging/RangingSession.Callback.md), [android.ranging.RangingSession.Callback#REASON_SYSTEM_POLICY](../android/ranging/RangingSession.Callback.md), or [android.ranging.RangingSession.Callback#REASON_NO_PEERS_FOUND](../android/ranging/RangingSession.Callback.md) |

### onOpenFailed

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onOpenFailed(reason: Int): Unit
```

Called when the ranging session failed to open.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `reason` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the reason for the failure, limited to values defined by android.ranging.RangingSession.Callback.Reason. Value is [android.ranging.RangingSession.Callback#REASON_UNKNOWN](../android/ranging/RangingSession.Callback.md), [android.ranging.RangingSession.Callback#REASON_LOCAL_REQUEST](../android/ranging/RangingSession.Callback.md), [android.ranging.RangingSession.Callback#REASON_REMOTE_REQUEST](../android/ranging/RangingSession.Callback.md), [android.ranging.RangingSession.Callback#REASON_UNSUPPORTED](../android/ranging/RangingSession.Callback.md), [android.ranging.RangingSession.Callback#REASON_SYSTEM_POLICY](../android/ranging/RangingSession.Callback.md), or [android.ranging.RangingSession.Callback#REASON_NO_PEERS_FOUND](../android/ranging/RangingSession.Callback.md) |

### onOpened

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onOpened(): Unit
```

Called when the ranging session opens successfully. 

### onResults

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onResults(
    peer: RangingDevice, 
    data: RangingData
): Unit
```

Called when ranging data has been received from a peer.

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `peer` | [RangingDevice](../android/ranging/RangingDevice.md): [RangingDevice](../android/ranging/RangingDevice.md) the peer from which ranging data was received. This value cannot be`null`. |
| `data` | [RangingData](../android/ranging/RangingData.md): [RangingData](../android/ranging/RangingData.md) the received. This value cannot be`null`. |

### onStarted

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onStarted(
    peer: RangingDevice, 
    technology: Int
): Unit
```

Called when ranging has started with a particular peer using a particular technology during an ongoing session.

| Parameters ||
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `peer` | [RangingDevice](../android/ranging/RangingDevice.md): [RangingDevice](../android/ranging/RangingDevice.md) the peer with which ranging has started. This value cannot be`null`. |
| `technology` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):android.ranging.RangingManager.RangingTechnology the ranging technology that started. Value is [android.ranging.RangingManager#UWB](../android/ranging/RangingManager.md), [android.ranging.RangingManager#BLE_CS](../android/ranging/RangingManager.md), [android.ranging.RangingManager#WIFI_NAN_RTT](../android/ranging/RangingManager.md), [android.ranging.RangingManager#BLE_RSSI](../android/ranging/RangingManager.md), or [android.ranging.RangingManager#WIFI_STA_RTT](../android/ranging/RangingManager.md) |

### onStopped

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onStopped(
    peer: RangingDevice, 
    technology: Int
): Unit
```

Called when ranging has stopped with a particular peer using a particular technology during an ongoing session.

| Parameters ||
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `peer` | [RangingDevice](../android/ranging/RangingDevice.md): [RangingDevice](../android/ranging/RangingDevice.md) the peer with which ranging has stopped. This value cannot be`null`. |
| `technology` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):android.ranging.RangingManager.RangingTechnology the ranging technology that stopped. Value is [android.ranging.RangingManager#UWB](../android/ranging/RangingManager.md), [android.ranging.RangingManager#BLE_CS](../android/ranging/RangingManager.md), [android.ranging.RangingManager#WIFI_NAN_RTT](../android/ranging/RangingManager.md), [android.ranging.RangingManager#BLE_RSSI](../android/ranging/RangingManager.md), or [android.ranging.RangingManager#WIFI_STA_RTT](../android/ranging/RangingManager.md) |
