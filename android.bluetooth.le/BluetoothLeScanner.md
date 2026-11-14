Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BluetoothLeScanner

```
class BluetoothLeScanner
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.bluetooth.le.BluetoothLeScanner](https://developer.android.com/reference/kotlin/android/bluetooth/le/BluetoothLeScanner#) |

This class provides methods to perform scan related operations for Bluetooth LE devices. An application can scan for a particular type of Bluetooth LE devices using `https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanFilter`. It can also request different types of callbacks for delivering the result.

Use `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter.html#getBluetoothLeScanner()` to get an instance of `https://developer.android.com/reference/kotlin/android/bluetooth/le/BluetoothLeScanner#`.

## Summary

| Constants ||
|---|---|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/le/BluetoothLeScanner#EXTRA_CALLBACK_TYPE:kotlin.String` Optional extra indicating the callback type, which will be one of CALLBACK_TYPE_\* constants in `https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanSettings`. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/le/BluetoothLeScanner#EXTRA_ERROR_CODE:kotlin.String` Optional extra indicating the error code, if any. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/le/BluetoothLeScanner#EXTRA_LIST_SCAN_RESULT:kotlin.String` Extra containing a list of ScanResults. |
| --- | --- |

| Public methods ||
|---|---|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/le/BluetoothLeScanner#flushPendingScanResults(android.bluetooth.le.ScanCallback)(callback: https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanCallback!)` Flush pending batch scan results stored in Bluetooth controller. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/le/BluetoothLeScanner#startScan(android.bluetooth.le.ScanCallback)(callback: https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanCallback)` Start Bluetooth LE scan with default parameters and no filters. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/le/BluetoothLeScanner#startScan(kotlin.collections.MutableList,%20android.bluetooth.le.ScanSettings,%20android.app.PendingIntent)(filters: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanFilter!>?, settings: https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanSettings?, callbackIntent: https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#)` Start Bluetooth LE scan using a `https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#`. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/le/BluetoothLeScanner#startScan(kotlin.collections.MutableList,%20android.bluetooth.le.ScanSettings,%20android.bluetooth.le.ScanCallback)(filters: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanFilter!>?, settings: https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanSettings, callback: https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanCallback)` Start Bluetooth LE scan. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/le/BluetoothLeScanner#stopScan(android.app.PendingIntent)(callbackIntent: https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#!)` Stops an ongoing Bluetooth LE scan started using a PendingIntent. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/le/BluetoothLeScanner#stopScan(android.bluetooth.le.ScanCallback)(callback: https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanCallback!)` Stops an ongoing Bluetooth LE scan. |
| --- | --- |

## Constants

### EXTRA_CALLBACK_TYPE

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_CALLBACK_TYPE: String
```

Optional extra indicating the callback type, which will be one of CALLBACK_TYPE_\* constants in `https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanSettings`.

 Value: "android.bluetooth.le.extra.CALLBACK_TYPE"

**See Also**

- `https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanCallback#onScanResult(kotlin.Int,%20android.bluetooth.le.ScanResult)`

### EXTRA_ERROR_CODE

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_ERROR_CODE: String
```

Optional extra indicating the error code, if any. The error code will be one of the SCAN_FAILED_\* codes in `https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanCallback`.

 Value: "android.bluetooth.le.extra.ERROR_CODE"

### EXTRA_LIST_SCAN_RESULT

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_LIST_SCAN_RESULT: String
```

Extra containing a list of ScanResults. It can have one or more results if there was no error. In case of error, `https://developer.android.com/reference/kotlin/android/bluetooth/le/BluetoothLeScanner#EXTRA_ERROR_CODE:kotlin.String` will contain the error code and this extra will not be available.

 Value: "android.bluetooth.le.extra.LIST_SCAN_RESULT"

## Public methods

### flushPendingScanResults

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun flushPendingScanResults(callback: ScanCallback!): Unit
```

Flush pending batch scan results stored in Bluetooth controller. This will return Bluetooth LE scan results batched on bluetooth controller. Returns immediately, batch scan results data will be delivered through the `callback`. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int` or lower, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_ADMIN:kotlin.String` permission which can be gained with a simple `<uses-permission>` manifest tag. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or or higher, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_SCAN:kotlin.String` permission which can be gained with `https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)`. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_SCAN:kotlin.String`

| Parameters ||
|---|---|
| `callback` | [ScanCallback](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanCallback)!: Callback of the Bluetooth LE Scan, it has to be the same instance as the one used to start scan. |

### startScan

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun startScan(callback: ScanCallback): Unit
```

Start Bluetooth LE scan with default parameters and no filters. The scan results will be delivered through `callback`. For unfiltered scans, scanning is stopped on screen off to save power. Scanning is resumed when screen is turned on again. To avoid this, use `https://developer.android.com/reference/kotlin/android/bluetooth/le/BluetoothLeScanner#startScan(kotlin.collections.MutableList,%20android.bluetooth.le.ScanSettings,%20android.bluetooth.le.ScanCallback)` with desired `https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanFilter`.

An app must have `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_COARSE_LOCATION:kotlin.String` permission in order to get results. An App targeting Android Q or later must have `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String` permission in order to get results.

This method requires the calling app to have the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_SCAN:kotlin.String` permission. Additionally, an app must have the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_PRIVILEGED:kotlin.String` if it is used for BLE scan only mode (when the adapter state is not `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter.html#STATE_ON:kotlin.Int`). 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int` or lower, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_ADMIN:kotlin.String` permission which can be gained with a simple `<uses-permission>` manifest tag. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or or higher, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_SCAN:kotlin.String` permission which can be gained with `https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)`. 
In addition, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String` permission. For apps targeting Build.VERSION_CODES#S or higher, an alternative is a strong assertion that you will never derive the physical location of the device, made by declaring `usesPermissionFlags="neverForLocation"` on the relevant `<uses-permission>` manifest tag. However, this assertion may restrict the types of Bluetooth devices you can interact with.

| Parameters ||
|---|---|
| `callback` | [ScanCallback](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanCallback): Callback used to deliver scan results. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | If `callback` is null. |

### startScan

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun startScan(
    filters: MutableList<ScanFilter!>?, 
    settings: ScanSettings?, 
    callbackIntent: PendingIntent
): Int
```

Start Bluetooth LE scan using a `https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#`. The scan results will be delivered via the PendingIntent. Use this method of scanning if your process is not always running and it should be started when scan results are available.

An app must have `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_COARSE_LOCATION:kotlin.String` permission in order to get results. An App targeting Android Q or later must have `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String` permission in order to get results.

When the PendingIntent is delivered, the Intent passed to the receiver or activity will contain one or more of the extras `https://developer.android.com/reference/kotlin/android/bluetooth/le/BluetoothLeScanner#EXTRA_CALLBACK_TYPE:kotlin.String`, `https://developer.android.com/reference/kotlin/android/bluetooth/le/BluetoothLeScanner#EXTRA_ERROR_CODE:kotlin.String` and `https://developer.android.com/reference/kotlin/android/bluetooth/le/BluetoothLeScanner#EXTRA_LIST_SCAN_RESULT:kotlin.String` to indicate the result of the scan.

This method requires the calling app to have the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_SCAN:kotlin.String` permission. Additionally, an app must have the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_PRIVILEGED:kotlin.String` if any of the following is true:

- it is used for BLE scan only mode (when the adapter state is not `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter.html#STATE_ON:kotlin.Int`).
- the `https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanSettings` uses android.bluetooth.le.ScanSettings#SCAN_MODE_AMBIENT_DISCOVERY.
- the `https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanSettings` uses batched scanning (`https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanSettings#getReportDelayMillis()` \> 0) with android.bluetooth.le.ScanSettings#SCAN_RESULT_TYPE_ABBREVIATED.
- a `https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanFilter` has a device address set, and either the address type is not `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice.html#ADDRESS_TYPE_PUBLIC:kotlin.Int` or the IRK is not null.

. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int` or lower, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_ADMIN:kotlin.String` permission which can be gained with a simple `<uses-permission>` manifest tag. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or or higher, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_SCAN:kotlin.String` permission which can be gained with `https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)`. 
In addition, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String` permission. For apps targeting Build.VERSION_CODES#S or higher, an alternative is a strong assertion that you will never derive the physical location of the device, made by declaring `usesPermissionFlags="neverForLocation"` on the relevant `<uses-permission>` manifest tag. However, this assertion may restrict the types of Bluetooth devices you can interact with.

| Parameters ||
|---|---|
| `filters` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [ScanFilter](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanFilter)!\>?: Optional list of ScanFilters for finding exact BLE devices. This value may be `null`. |
| `settings` | [ScanSettings](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanSettings)?: Optional settings for the scan. This value may be `null`. |
| `callbackIntent` | [PendingIntent](https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#): The PendingIntent to deliver the result to. This value cannot be `null`. |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Returns 0 for success or an error code from `https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanCallback` if the scan request could not be sent. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/bluetooth/le/BluetoothLeScanner#stopScan(android.app.PendingIntent)`

### startScan

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun startScan(
    filters: MutableList<ScanFilter!>?, 
    settings: ScanSettings, 
    callback: ScanCallback
): Unit
```

Start Bluetooth LE scan. The scan results will be delivered through `callback`. For unfiltered scans, scanning is stopped on screen off to save power. Scanning is resumed when screen is turned on again. To avoid this, do filtered scanning by using proper `https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanFilter`

An app must have `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_COARSE_LOCATION:kotlin.String` permission in order to get results. An App targeting Android Q or later must have `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String` permission in order to get results.

This method requires the calling app to have the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_SCAN:kotlin.String` permission. Additionally, an app must have the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_PRIVILEGED:kotlin.String` if any of the following is true:

- it is used for BLE scan only mode (when the adapter state is not `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter.html#STATE_ON:kotlin.Int`).
- the `https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanSettings` uses android.bluetooth.le.ScanSettings#SCAN_MODE_AMBIENT_DISCOVERY.
- the `https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanSettings` uses batched scanning (`https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanSettings#getReportDelayMillis()` \> 0) with android.bluetooth.le.ScanSettings#SCAN_RESULT_TYPE_ABBREVIATED.
- a `https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanFilter` has a device address set, and either the address type is not `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice.html#ADDRESS_TYPE_PUBLIC:kotlin.Int` or the IRK is not null.

. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int` or lower, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_ADMIN:kotlin.String` permission which can be gained with a simple `<uses-permission>` manifest tag. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or or higher, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_SCAN:kotlin.String` permission which can be gained with `https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)`. 
In addition, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String` permission. For apps targeting Build.VERSION_CODES#S or higher, an alternative is a strong assertion that you will never derive the physical location of the device, made by declaring `usesPermissionFlags="neverForLocation"` on the relevant `<uses-permission>` manifest tag. However, this assertion may restrict the types of Bluetooth devices you can interact with.

| Parameters ||
|---|---|
| `filters` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [ScanFilter](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanFilter)!\>?: `https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanFilter`s for finding exact BLE devices. This value may be `null`. |
| `settings` | [ScanSettings](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanSettings): Settings for the scan. This value cannot be `null`. |
| `callback` | [ScanCallback](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanCallback): Callback used to deliver scan results. This value cannot be `null`. |
| --- | --- |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | If `settings` or `callback` is null. |

### stopScan

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun stopScan(callbackIntent: PendingIntent!): Unit
```

Stops an ongoing Bluetooth LE scan started using a PendingIntent. When creating the PendingIntent parameter, please do not use the FLAG_CANCEL_CURRENT flag. Otherwise, the stop scan may have no effect. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int` or lower, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_ADMIN:kotlin.String` permission which can be gained with a simple `<uses-permission>` manifest tag. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or or higher, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_SCAN:kotlin.String` permission which can be gained with `https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)`. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_SCAN:kotlin.String`

| Parameters ||
|---|---|
| `callbackIntent` | [PendingIntent](https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#)!: The PendingIntent that was used to start the scan. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/bluetooth/le/BluetoothLeScanner#startScan(kotlin.collections.MutableList,%20android.bluetooth.le.ScanSettings,%20android.app.PendingIntent)`

### stopScan

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun stopScan(callback: ScanCallback!): Unit
```

Stops an ongoing Bluetooth LE scan. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int` or lower, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_ADMIN:kotlin.String` permission which can be gained with a simple `<uses-permission>` manifest tag. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or or higher, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_SCAN:kotlin.String` permission which can be gained with `https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)`. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_SCAN:kotlin.String`
