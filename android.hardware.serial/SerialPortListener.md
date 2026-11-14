Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SerialPortListener

```
interface SerialPortListener
```

| [android.hardware.serial.SerialPortListener](SerialPortListener.md) |

Listener to monitor serial port connections and disconnections.

## Summary

| Public methods ||
|---|---|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/serial/SerialPortListener#onSerialPortConnected(android.hardware.serial.SerialPort)(port: https://developer.android.com/reference/kotlin/android/hardware/serial/SerialPort)` Called when a supported serial port is connected. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/serial/SerialPortListener#onSerialPortDisconnected(android.hardware.serial.SerialPort)(port: https://developer.android.com/reference/kotlin/android/hardware/serial/SerialPort)` Called when a supported serial port is disconnected. |

## Public methods

### onSerialPortConnected

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun onSerialPortConnected(port: SerialPort): Unit
```

Called when a supported serial port is connected.

| Parameters ||
|---|---|
| `port` | [SerialPort](SerialPort.md): This value cannot be `null`. |

### onSerialPortDisconnected

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun onSerialPortDisconnected(port: SerialPort): Unit
```

Called when a supported serial port is disconnected.

| Parameters ||
|---|---|
| `port` | [SerialPort](SerialPort.md): This value cannot be `null`. |
