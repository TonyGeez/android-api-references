# BluetoothAdapter.LeScanCallback

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# LeScanCallback

Kotlin| [Java](https://developer.android.com/reference/android/bluetooth/BluetoothAdapter.LeScanCallback "View this page in Java") 

```
interface LeScanCallback
```

| [android.bluetooth.BluetoothAdapter.LeScanCallback](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter.LeScanCallback#) |

Callback interface used to deliver LE scan results.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onLeScan](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter.LeScanCallback#onLeScan(android.bluetooth.BluetoothDevice,%20kotlin.Int,%20kotlin.ByteArray))`(`device:` ` [BluetoothDevice](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice)!`, `rssi:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `scanRecord:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Callback reporting an LE device found during a device scan initiated by the android. |

## Public methods

### onLeScan

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onLeScan(
    device: BluetoothDevice!, 
    rssi: Int, 
    scanRecord: ByteArray!
): Unit
```

Callback reporting an LE device found during a device scan initiated by the android.bluetooth.BluetoothAdapter#startLeScan function.

| Parameters ||
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `device` | [BluetoothDevice](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice)!:Identifies the remote device |
| `rssi` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The RSSI value for the remote device as reported by the Bluetooth hardware. 0 if no RSSI value is available. |
| `scanRecord` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:The content of the advertisement record offered by the remote device. |
