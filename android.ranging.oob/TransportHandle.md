# TransportHandle

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TransportHandle

Kotlin| [Java](https://developer.android.com/reference/android/ranging/oob/TransportHandle "View this page in Java") 
| --- | --- |

```
interface TransportHandle : AutoCloseable
```

| [android.ranging.oob.TransportHandle](https://developer.android.com/reference/kotlin/android/ranging/oob/TransportHandle#) |

TransportHandle is used as the Out-Of-Band (OOB) transport mechanism by ranging module. In cases where module is used in a non-raw ranging mode, the user shall provide an implementation of the TransportHandle, allowing ranging module to do the necessary OOB communication with a peer device using the provided transport handle. Some examples of OOB transport between two peer devices are:

- BLE GATT connection
- Wi-Fi MDNS link
- Internet

<br />

## Summary

| Nested classes ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [ReceiveCallback](https://developer.android.com/reference/kotlin/android/ranging/oob/TransportHandle.ReceiveCallback) TransportHandle callback. |

| Public methods ||
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerReceiveCallback](https://developer.android.com/reference/kotlin/android/ranging/oob/TransportHandle#registerReceiveCallback(java.util.concurrent.Executor,%20android.ranging.oob.TransportHandle.ReceiveCallback))`(`executor:` ` [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#)`, `callback:` ` [TransportHandle.ReceiveCallback](https://developer.android.com/reference/kotlin/android/ranging/oob/TransportHandle.ReceiveCallback)`)` Registers a callback to receive updates from the transport mechanism. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [sendData](https://developer.android.com/reference/kotlin/android/ranging/oob/TransportHandle#sendData(kotlin.ByteArray))`(`data:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)`)` Send data to the peer device via the implemented OOB transport. |

| Inherited functions ||
|---|---|
| From class [AutoCloseable](https://developer.android.com/reference/kotlin/java/lang/AutoCloseable.html#) |------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](https://developer.android.com/reference/kotlin/java/lang/AutoCloseable.html#close())`()` <br /> Closes this resource, relinquishing any underlying resources. This method is invoked automatically on objects managed by the`try`-with-resources statement. <br /> | ||

## Public methods

### registerReceiveCallback

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun registerReceiveCallback(
    executor: Executor, 
    callback: TransportHandle.ReceiveCallback
): Unit
```

Registers a callback to receive updates from the transport mechanism.

The callback should be used to notify information about the peer device including the data received from the peer device.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#):the [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#) on which the callback should be invoked. Must not be null. |
| `callback` | [TransportHandle.ReceiveCallback](https://developer.android.com/reference/kotlin/android/ranging/oob/TransportHandle.ReceiveCallback):the [ReceiveCallback](https://developer.android.com/reference/kotlin/android/ranging/oob/TransportHandle.ReceiveCallback) instance to receive updates. Must not be null. |

| Exceptions ||
|--------------------------------------|-----------------------------------------|
| `java.lang.IllegalArgumentException` | if either`executor`or`callback`is null. |

### sendData

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun sendData(data: ByteArray): Unit
```

Send data to the peer device via the implemented OOB transport.

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| `data` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html):the data to be sent to the peer device. Must not be null. |

| Exceptions ||
|--------------------------------------|-----------------------------------------|
| `java.lang.IllegalArgumentException` | if the provided data is null or invalid |
