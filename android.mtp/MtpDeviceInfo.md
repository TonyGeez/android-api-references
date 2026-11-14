# MtpDeviceInfo

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MtpDeviceInfo

Kotlin| [Java](https://developer.android.com/reference/android/mtp/MtpDeviceInfo "View this page in Java") 
| --- | --- |

```
open class MtpDeviceInfo
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.mtp.MtpDeviceInfo](https://developer.android.com/reference/kotlin/android/mtp/MtpDeviceInfo#) |

This class encapsulates information about an MTP device. This corresponds to the DeviceInfo Dataset described in section 5.1.1 of the MTP specification.

## Summary

| Public methods ||
|----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html) | [getEventsSupported](https://developer.android.com/reference/kotlin/android/mtp/MtpDeviceInfo#getEventsSupported())`()` Returns event code supported by the device. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getManufacturer](https://developer.android.com/reference/kotlin/android/mtp/MtpDeviceInfo#getManufacturer())`()` Returns the manufacturer's name for the MTP device |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getModel](https://developer.android.com/reference/kotlin/android/mtp/MtpDeviceInfo#getModel())`()` Returns the model name for the MTP device |
| --- | --- |
| [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html) | [getOperationsSupported](https://developer.android.com/reference/kotlin/android/mtp/MtpDeviceInfo#getOperationsSupported())`()` Returns operation code supported by the device. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getSerialNumber](https://developer.android.com/reference/kotlin/android/mtp/MtpDeviceInfo#getSerialNumber())`()` Returns the unique serial number for the MTP device |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getVersion](https://developer.android.com/reference/kotlin/android/mtp/MtpDeviceInfo#getVersion())`()` Returns the version string the MTP device |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEventSupported](https://developer.android.com/reference/kotlin/android/mtp/MtpDeviceInfo#isEventSupported(kotlin.Int))`(`code:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns if the given event is supported by the device or not. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isOperationSupported](https://developer.android.com/reference/kotlin/android/mtp/MtpDeviceInfo#isOperationSupported(kotlin.Int))`(`code:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns if the given operation is supported by the device or not. |

## Public methods

### getEventsSupported

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getEventsSupported(): IntArray
```

Returns event code supported by the device.

| Return ||
|---------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html) | supported event code. Can be null if device does not provide the property. |

**See Also**

- [android.mtp.MtpEvent#EVENT_UNDEFINED](https://developer.android.com/reference/kotlin/android/mtp/MtpEvent#EVENT_UNDEFINED:kotlin.Int)
- [android.mtp.MtpEvent#EVENT_CANCEL_TRANSACTION](https://developer.android.com/reference/kotlin/android/mtp/MtpEvent#EVENT_CANCEL_TRANSACTION:kotlin.Int)
- [android.mtp.MtpEvent#EVENT_OBJECT_ADDED](https://developer.android.com/reference/kotlin/android/mtp/MtpEvent#EVENT_OBJECT_ADDED:kotlin.Int)
- [android.mtp.MtpEvent#EVENT_OBJECT_REMOVED](https://developer.android.com/reference/kotlin/android/mtp/MtpEvent#EVENT_OBJECT_REMOVED:kotlin.Int)
- [android.mtp.MtpEvent#EVENT_STORE_ADDED](https://developer.android.com/reference/kotlin/android/mtp/MtpEvent#EVENT_STORE_ADDED:kotlin.Int)
- [android.mtp.MtpEvent#EVENT_STORE_REMOVED](https://developer.android.com/reference/kotlin/android/mtp/MtpEvent#EVENT_STORE_REMOVED:kotlin.Int)
- [android.mtp.MtpEvent#EVENT_DEVICE_PROP_CHANGED](https://developer.android.com/reference/kotlin/android/mtp/MtpEvent#EVENT_DEVICE_PROP_CHANGED:kotlin.Int)
- [android.mtp.MtpEvent#EVENT_OBJECT_INFO_CHANGED](https://developer.android.com/reference/kotlin/android/mtp/MtpEvent#EVENT_OBJECT_INFO_CHANGED:kotlin.Int)
- [android.mtp.MtpEvent#EVENT_DEVICE_INFO_CHANGED](https://developer.android.com/reference/kotlin/android/mtp/MtpEvent#EVENT_DEVICE_INFO_CHANGED:kotlin.Int)
- [android.mtp.MtpEvent#EVENT_REQUEST_OBJECT_TRANSFER](https://developer.android.com/reference/kotlin/android/mtp/MtpEvent#EVENT_REQUEST_OBJECT_TRANSFER:kotlin.Int)
- [android.mtp.MtpEvent#EVENT_STORE_FULL](https://developer.android.com/reference/kotlin/android/mtp/MtpEvent#EVENT_STORE_FULL:kotlin.Int)
- [android.mtp.MtpEvent#EVENT_DEVICE_RESET](https://developer.android.com/reference/kotlin/android/mtp/MtpEvent#EVENT_DEVICE_RESET:kotlin.Int)
- [android.mtp.MtpEvent#EVENT_STORAGE_INFO_CHANGED](https://developer.android.com/reference/kotlin/android/mtp/MtpEvent#EVENT_STORAGE_INFO_CHANGED:kotlin.Int)
- [android.mtp.MtpEvent#EVENT_CAPTURE_COMPLETE](https://developer.android.com/reference/kotlin/android/mtp/MtpEvent#EVENT_CAPTURE_COMPLETE:kotlin.Int)
- [android.mtp.MtpEvent#EVENT_UNREPORTED_STATUS](https://developer.android.com/reference/kotlin/android/mtp/MtpEvent#EVENT_UNREPORTED_STATUS:kotlin.Int)
- [android.mtp.MtpEvent#EVENT_OBJECT_PROP_CHANGED](https://developer.android.com/reference/kotlin/android/mtp/MtpEvent#EVENT_OBJECT_PROP_CHANGED:kotlin.Int)
- [android.mtp.MtpEvent#EVENT_OBJECT_PROP_DESC_CHANGED](https://developer.android.com/reference/kotlin/android/mtp/MtpEvent#EVENT_OBJECT_PROP_DESC_CHANGED:kotlin.Int)
- [android.mtp.MtpEvent#EVENT_OBJECT_REFERENCES_CHANGED](https://developer.android.com/reference/kotlin/android/mtp/MtpEvent#EVENT_OBJECT_REFERENCES_CHANGED:kotlin.Int) 

### getManufacturer

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getManufacturer(): String
```

Returns the manufacturer's name for the MTP device

| Return ||
|----------------------------------------------------------------------------------|---------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | the manufacturer name This value cannot be`null`. |

### getModel

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getModel(): String
```

Returns the model name for the MTP device

| Return ||
|----------------------------------------------------------------------------------|--------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | the model name This value cannot be`null`. |

### getOperationsSupported

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getOperationsSupported(): IntArray
```

Returns operation code supported by the device.

| Return ||
|---------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html) | supported operation code. Can be null if device does not provide the property. |

**See Also**

- [android.mtp.MtpConstants#OPERATION_GET_DEVICE_INFO](https://developer.android.com/reference/kotlin/android/mtp/MtpConstants#OPERATION_GET_DEVICE_INFO:kotlin.Int)
- [android.mtp.MtpConstants#OPERATION_OPEN_SESSION](https://developer.android.com/reference/kotlin/android/mtp/MtpConstants#OPERATION_OPEN_SESSION:kotlin.Int)
- [android.mtp.MtpConstants#OPERATION_CLOSE_SESSION](https://developer.android.com/reference/kotlin/android/mtp/MtpConstants#OPERATION_CLOSE_SESSION:kotlin.Int)
- [android.mtp.MtpConstants#OPERATION_GET_STORAGE_I_DS](https://developer.android.com/reference/kotlin/android/mtp/MtpConstants#OPERATION_GET_STORAGE_I_DS:kotlin.Int)
- [android.mtp.MtpConstants#OPERATION_GET_STORAGE_INFO](https://developer.android.com/reference/kotlin/android/mtp/MtpConstants#OPERATION_GET_STORAGE_INFO:kotlin.Int)
- [android.mtp.MtpConstants#OPERATION_GET_NUM_OBJECTS](https://developer.android.com/reference/kotlin/android/mtp/MtpConstants#OPERATION_GET_NUM_OBJECTS:kotlin.Int)
- [android.mtp.MtpConstants#OPERATION_GET_OBJECT_HANDLES](https://developer.android.com/reference/kotlin/android/mtp/MtpConstants#OPERATION_GET_OBJECT_HANDLES:kotlin.Int)
- [android.mtp.MtpConstants#OPERATION_GET_OBJECT_INFO](https://developer.android.com/reference/kotlin/android/mtp/MtpConstants#OPERATION_GET_OBJECT_INFO:kotlin.Int)
- [android.mtp.MtpConstants#OPERATION_GET_OBJECT](https://developer.android.com/reference/kotlin/android/mtp/MtpConstants#OPERATION_GET_OBJECT:kotlin.Int)
- [android.mtp.MtpConstants#OPERATION_GET_THUMB](https://developer.android.com/reference/kotlin/android/mtp/MtpConstants#OPERATION_GET_THUMB:kotlin.Int)
- [android.mtp.MtpConstants#OPERATION_DELETE_OBJECT](https://developer.android.com/reference/kotlin/android/mtp/MtpConstants#OPERATION_DELETE_OBJECT:kotlin.Int)
- [android.mtp.MtpConstants#OPERATION_SEND_OBJECT_INFO](https://developer.android.com/reference/kotlin/android/mtp/MtpConstants#OPERATION_SEND_OBJECT_INFO:kotlin.Int)
- [android.mtp.MtpConstants#OPERATION_SEND_OBJECT](https://developer.android.com/reference/kotlin/android/mtp/MtpConstants#OPERATION_SEND_OBJECT:kotlin.Int)
- [android.mtp.MtpConstants#OPERATION_INITIATE_CAPTURE](https://developer.android.com/reference/kotlin/android/mtp/MtpConstants#OPERATION_INITIATE_CAPTURE:kotlin.Int)
- [android.mtp.MtpConstants#OPERATION_FORMAT_STORE](https://developer.android.com/reference/kotlin/android/mtp/MtpConstants#OPERATION_FORMAT_STORE:kotlin.Int)
- [android.mtp.MtpConstants#OPERATION_RESET_DEVICE](https://developer.android.com/reference/kotlin/android/mtp/MtpConstants#OPERATION_RESET_DEVICE:kotlin.Int)
- [android.mtp.MtpConstants#OPERATION_SELF_TEST](https://developer.android.com/reference/kotlin/android/mtp/MtpConstants#OPERATION_SELF_TEST:kotlin.Int)
- [android.mtp.MtpConstants#OPERATION_SET_OBJECT_PROTECTION](https://developer.android.com/reference/kotlin/android/mtp/MtpConstants#OPERATION_SET_OBJECT_PROTECTION:kotlin.Int)
- [android.mtp.MtpConstants#OPERATION_POWER_DOWN](https://developer.android.com/reference/kotlin/android/mtp/MtpConstants#OPERATION_POWER_DOWN:kotlin.Int)
- [android.mtp.MtpConstants#OPERATION_GET_DEVICE_PROP_DESC](https://developer.android.com/reference/kotlin/android/mtp/MtpConstants#OPERATION_GET_DEVICE_PROP_DESC:kotlin.Int)
- [android.mtp.MtpConstants#OPERATION_GET_DEVICE_PROP_VALUE](https://developer.android.com/reference/kotlin/android/mtp/MtpConstants#OPERATION_GET_DEVICE_PROP_VALUE:kotlin.Int)
- [android.mtp.MtpConstants#OPERATION_SET_DEVICE_PROP_VALUE](https://developer.android.com/reference/kotlin/android/mtp/MtpConstants#OPERATION_SET_DEVICE_PROP_VALUE:kotlin.Int)
- [android.mtp.MtpConstants#OPERATION_RESET_DEVICE_PROP_VALUE](https://developer.android.com/reference/kotlin/android/mtp/MtpConstants#OPERATION_RESET_DEVICE_PROP_VALUE:kotlin.Int)
- [android.mtp.MtpConstants#OPERATION_TERMINATE_OPEN_CAPTURE](https://developer.android.com/reference/kotlin/android/mtp/MtpConstants#OPERATION_TERMINATE_OPEN_CAPTURE:kotlin.Int)
- [android.mtp.MtpConstants#OPERATION_MOVE_OBJECT](https://developer.android.com/reference/kotlin/android/mtp/MtpConstants#OPERATION_MOVE_OBJECT:kotlin.Int)
- [android.mtp.MtpConstants#OPERATION_COPY_OBJECT](https://developer.android.com/reference/kotlin/android/mtp/MtpConstants#OPERATION_COPY_OBJECT:kotlin.Int)
- [android.mtp.MtpConstants#OPERATION_GET_PARTIAL_OBJECT](https://developer.android.com/reference/kotlin/android/mtp/MtpConstants#OPERATION_GET_PARTIAL_OBJECT:kotlin.Int)
- [android.mtp.MtpConstants#OPERATION_INITIATE_OPEN_CAPTURE](https://developer.android.com/reference/kotlin/android/mtp/MtpConstants#OPERATION_INITIATE_OPEN_CAPTURE:kotlin.Int)
- [android.mtp.MtpConstants#OPERATION_GET_OBJECT_PROPS_SUPPORTED](https://developer.android.com/reference/kotlin/android/mtp/MtpConstants#OPERATION_GET_OBJECT_PROPS_SUPPORTED:kotlin.Int)
- [android.mtp.MtpConstants#OPERATION_GET_OBJECT_PROP_DESC](https://developer.android.com/reference/kotlin/android/mtp/MtpConstants#OPERATION_GET_OBJECT_PROP_DESC:kotlin.Int)
- [android.mtp.MtpConstants#OPERATION_GET_OBJECT_PROP_VALUE](https://developer.android.com/reference/kotlin/android/mtp/MtpConstants#OPERATION_GET_OBJECT_PROP_VALUE:kotlin.Int)
- [android.mtp.MtpConstants#OPERATION_SET_OBJECT_PROP_VALUE](https://developer.android.com/reference/kotlin/android/mtp/MtpConstants#OPERATION_SET_OBJECT_PROP_VALUE:kotlin.Int)
- [android.mtp.MtpConstants#OPERATION_GET_OBJECT_REFERENCES](https://developer.android.com/reference/kotlin/android/mtp/MtpConstants#OPERATION_GET_OBJECT_REFERENCES:kotlin.Int)
- [android.mtp.MtpConstants#OPERATION_SET_OBJECT_REFERENCES](https://developer.android.com/reference/kotlin/android/mtp/MtpConstants#OPERATION_SET_OBJECT_REFERENCES:kotlin.Int)
- [android.mtp.MtpConstants#OPERATION_SKIP](https://developer.android.com/reference/kotlin/android/mtp/MtpConstants#OPERATION_SKIP:kotlin.Int) 

### getSerialNumber

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSerialNumber(): String
```

Returns the unique serial number for the MTP device

| Return ||
|----------------------------------------------------------------------------------|-----------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | the serial number This value cannot be`null`. |

### getVersion

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getVersion(): String
```

Returns the version string the MTP device

| Return ||
|----------------------------------------------------------------------------------|------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | the device version This value cannot be`null`. |

### isEventSupported

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isEventSupported(code: Int): Boolean
```

Returns if the given event is supported by the device or not.

| Parameters ||
|--------|----------------------------------------------------------------------------------------|
| `code` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Event code. |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | If the given event is supported by the device or not. |

### isOperationSupported

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isOperationSupported(code: Int): Boolean
```

Returns if the given operation is supported by the device or not.

| Parameters ||
|--------|--------------------------------------------------------------------------------------------|
| `code` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Operation code. |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | If the given operation is supported by the device or not. |
