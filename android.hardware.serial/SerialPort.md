Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SerialPort

```
class SerialPort
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.hardware.serial.SerialPort](https://developer.android.com/reference/kotlin/android/hardware/serial/SerialPort#) |

A class representing a Serial port.

## Summary

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/serial/SerialPort#INVALID_ID:kotlin.Int` Value returned by `https://developer.android.com/reference/kotlin/android/hardware/serial/SerialPort#getVendorId()` and `https://developer.android.com/reference/kotlin/android/hardware/serial/SerialPort#getProductId()` if this serial port isn't a USB device. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/serial/SerialPort#OPEN_FLAG_DATA_SYNC:kotlin.Int` For use with `https://developer.android.com/reference/kotlin/android/hardware/serial/SerialPort#requestOpen(kotlin.Int,%20kotlin.Boolean,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)`: write operations on the file will complete according to the requirements of synchronized I/O data integrity completion (while file metadata may not be synchronized). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/serial/SerialPort#OPEN_FLAG_NONBLOCK:kotlin.Int` For use with `https://developer.android.com/reference/kotlin/android/hardware/serial/SerialPort#requestOpen(kotlin.Int,%20kotlin.Boolean,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)`: when possible, the file is opened in nonblocking mode. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/serial/SerialPort#OPEN_FLAG_READ_ONLY:kotlin.Int` For use with `https://developer.android.com/reference/kotlin/android/hardware/serial/SerialPort#requestOpen(kotlin.Int,%20kotlin.Boolean,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)`: open for reading only. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/serial/SerialPort#OPEN_FLAG_READ_WRITE:kotlin.Int` For use with `https://developer.android.com/reference/kotlin/android/hardware/serial/SerialPort#requestOpen(kotlin.Int,%20kotlin.Boolean,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)`: open for reading and writing. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/serial/SerialPort#OPEN_FLAG_SYNC:kotlin.Int` For use with `https://developer.android.com/reference/kotlin/android/hardware/serial/SerialPort#requestOpen(kotlin.Int,%20kotlin.Boolean,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)`: write operations on the file will complete according to the requirements of synchronized I/O file integrity completion (by contrast with the synchronized I/O data integrity completion provided by FLAG_DATA_SYNC). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/serial/SerialPort#OPEN_FLAG_WRITE_ONLY:kotlin.Int` For use with `https://developer.android.com/reference/kotlin/android/hardware/serial/SerialPort#requestOpen(kotlin.Int,%20kotlin.Boolean,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)`: open for writing only. |

| Public methods ||
|---|---|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/serial/SerialPort#getName()()` Get the device name. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/serial/SerialPort#getProductId()()` Return the product ID of this serial port if it is a USB device. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/serial/SerialPort#getVendorId()()` Return the vendor ID of this serial port if it is a USB device. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/serial/SerialPort#requestOpen(kotlin.Int,%20kotlin.Boolean,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)(flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, exclusive: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html, executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, receiver: https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#<https://developer.android.com/reference/kotlin/android/hardware/serial/SerialPortResponse!, https://developer.android.com/reference/kotlin/java/lang/Exception.html#!>)` Request to open the port. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/serial/SerialPort#toString()()` Returns a string representation of the object. |

## Constants

### INVALID_ID

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val INVALID_ID: Int
```

Value returned by `https://developer.android.com/reference/kotlin/android/hardware/serial/SerialPort#getVendorId()` and `https://developer.android.com/reference/kotlin/android/hardware/serial/SerialPort#getProductId()` if this serial port isn't a USB device.

 Value: -1

### OPEN_FLAG_DATA_SYNC

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val OPEN_FLAG_DATA_SYNC: Int
```

For use with `https://developer.android.com/reference/kotlin/android/hardware/serial/SerialPort#requestOpen(kotlin.Int,%20kotlin.Boolean,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)`: write operations on the file will complete according to the requirements of synchronized I/O data integrity completion (while file metadata may not be synchronized).

 Value: 4096

### OPEN_FLAG_NONBLOCK

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val OPEN_FLAG_NONBLOCK: Int
```

For use with `https://developer.android.com/reference/kotlin/android/hardware/serial/SerialPort#requestOpen(kotlin.Int,%20kotlin.Boolean,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)`: when possible, the file is opened in nonblocking mode.

 Value: 2048

### OPEN_FLAG_READ_ONLY

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val OPEN_FLAG_READ_ONLY: Int
```

For use with `https://developer.android.com/reference/kotlin/android/hardware/serial/SerialPort#requestOpen(kotlin.Int,%20kotlin.Boolean,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)`: open for reading only.

 Value: 0

### OPEN_FLAG_READ_WRITE

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val OPEN_FLAG_READ_WRITE: Int
```

For use with `https://developer.android.com/reference/kotlin/android/hardware/serial/SerialPort#requestOpen(kotlin.Int,%20kotlin.Boolean,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)`: open for reading and writing.

 Value: 2

### OPEN_FLAG_SYNC

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val OPEN_FLAG_SYNC: Int
```

For use with `https://developer.android.com/reference/kotlin/android/hardware/serial/SerialPort#requestOpen(kotlin.Int,%20kotlin.Boolean,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)`: write operations on the file will complete according to the requirements of synchronized I/O file integrity completion (by contrast with the synchronized I/O data integrity completion provided by FLAG_DATA_SYNC).

 Value: 1048576

### OPEN_FLAG_WRITE_ONLY

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val OPEN_FLAG_WRITE_ONLY: Int
```

For use with `https://developer.android.com/reference/kotlin/android/hardware/serial/SerialPort#requestOpen(kotlin.Int,%20kotlin.Boolean,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)`: open for writing only.

 Value: 1

## Public methods

### getName

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getName(): String
```

Get the device name. It is the dev node name under /dev, e.g. ttyUSB0, ttyACM1.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | This value cannot be `null`. |

### getProductId

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getProductId(): Int
```

Return the product ID of this serial port if it is a USB device. Otherwise, it returns `https://developer.android.com/reference/kotlin/android/hardware/serial/SerialPort#INVALID_ID:kotlin.Int`.

### getVendorId

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getVendorId(): Int
```

Return the vendor ID of this serial port if it is a USB device. Otherwise, it returns `https://developer.android.com/reference/kotlin/android/hardware/serial/SerialPort#INVALID_ID:kotlin.Int`.

### requestOpen

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun requestOpen(
    flags: Int, 
    exclusive: Boolean, 
    executor: Executor, 
    receiver: OutcomeReceiver<SerialPortResponse!, Exception!>
): Unit
```

Request to open the port.

Exceptions passed to `receiver` may be

- `https://developer.android.com/reference/kotlin/java/lang/IllegalStateException.html#` if the port is not found.
- `https://developer.android.com/reference/kotlin/java/io/IOException.html#` if the port cannot be opened.
- `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#` if the user rejects the open request.

| Parameters ||
|---|---|
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): open flags that define read/write mode and other options. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/hardware/serial/SerialPort#OPEN_FLAG_READ_ONLY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/serial/SerialPort#OPEN_FLAG_WRITE_ONLY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/serial/SerialPort#OPEN_FLAG_READ_WRITE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/serial/SerialPort#OPEN_FLAG_NONBLOCK:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/serial/SerialPort#OPEN_FLAG_DATA_SYNC:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/serial/SerialPort#OPEN_FLAG_SYNC:kotlin.Int` |
| `exclusive` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): whether to request exclusive access to the port, preventing other processes from opening it. |
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#): the executor used to run receiver. This value cannot be `null`. |
| `receiver` | [OutcomeReceiver](https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#)\< [SerialPortResponse](https://developer.android.com/reference/kotlin/android/hardware/serial/SerialPortResponse)!, [Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#)!\>: the outcome receiver. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the set of flags is not correct. |
| `java.lang.NullPointerException` | if any parameters are `null`. |

### toString

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toString(): String
```

Returns a string representation of the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the object. |
