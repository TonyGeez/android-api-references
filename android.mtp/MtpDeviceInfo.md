# MtpDeviceInfo

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MtpDeviceInfo

Kotlin| [Java](MtpDeviceInfo.md) 
| --- | --- |

```
open class MtpDeviceInfo
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.mtp.MtpDeviceInfo](MtpDeviceInfo.md) |

This class encapsulates information about an MTP device. This corresponds to the DeviceInfo Dataset described in section 5.1.1 of the MTP specification.

## Summary

| Public methods ||
|----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html) | [getEventsSupported](MtpDeviceInfo.md))`()` Returns event code supported by the device. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getManufacturer](MtpDeviceInfo.md))`()` Returns the manufacturer's name for the MTP device |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getModel](MtpDeviceInfo.md))`()` Returns the model name for the MTP device |
| --- | --- |
| [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html) | [getOperationsSupported](MtpDeviceInfo.md))`()` Returns operation code supported by the device. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getSerialNumber](MtpDeviceInfo.md))`()` Returns the unique serial number for the MTP device |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getVersion](MtpDeviceInfo.md))`()` Returns the version string the MTP device |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEventSupported](MtpDeviceInfo.md))`(`code:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns if the given event is supported by the device or not. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isOperationSupported](MtpDeviceInfo.md))`(`code:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns if the given operation is supported by the device or not. |

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

- [android.mtp.MtpEvent#EVENT_UNDEFINED](MtpEvent.md)
- [android.mtp.MtpEvent#EVENT_CANCEL_TRANSACTION](MtpEvent.md)
- [android.mtp.MtpEvent#EVENT_OBJECT_ADDED](MtpEvent.md)
- [android.mtp.MtpEvent#EVENT_OBJECT_REMOVED](MtpEvent.md)
- [android.mtp.MtpEvent#EVENT_STORE_ADDED](MtpEvent.md)
- [android.mtp.MtpEvent#EVENT_STORE_REMOVED](MtpEvent.md)
- [android.mtp.MtpEvent#EVENT_DEVICE_PROP_CHANGED](MtpEvent.md)
- [android.mtp.MtpEvent#EVENT_OBJECT_INFO_CHANGED](MtpEvent.md)
- [android.mtp.MtpEvent#EVENT_DEVICE_INFO_CHANGED](MtpEvent.md)
- [android.mtp.MtpEvent#EVENT_REQUEST_OBJECT_TRANSFER](MtpEvent.md)
- [android.mtp.MtpEvent#EVENT_STORE_FULL](MtpEvent.md)
- [android.mtp.MtpEvent#EVENT_DEVICE_RESET](MtpEvent.md)
- [android.mtp.MtpEvent#EVENT_STORAGE_INFO_CHANGED](MtpEvent.md)
- [android.mtp.MtpEvent#EVENT_CAPTURE_COMPLETE](MtpEvent.md)
- [android.mtp.MtpEvent#EVENT_UNREPORTED_STATUS](MtpEvent.md)
- [android.mtp.MtpEvent#EVENT_OBJECT_PROP_CHANGED](MtpEvent.md)
- [android.mtp.MtpEvent#EVENT_OBJECT_PROP_DESC_CHANGED](MtpEvent.md)
- [android.mtp.MtpEvent#EVENT_OBJECT_REFERENCES_CHANGED](MtpEvent.md) 

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

- [android.mtp.MtpConstants#OPERATION_GET_DEVICE_INFO](MtpConstants.md)
- [android.mtp.MtpConstants#OPERATION_OPEN_SESSION](MtpConstants.md)
- [android.mtp.MtpConstants#OPERATION_CLOSE_SESSION](MtpConstants.md)
- [android.mtp.MtpConstants#OPERATION_GET_STORAGE_I_DS](MtpConstants.md)
- [android.mtp.MtpConstants#OPERATION_GET_STORAGE_INFO](MtpConstants.md)
- [android.mtp.MtpConstants#OPERATION_GET_NUM_OBJECTS](MtpConstants.md)
- [android.mtp.MtpConstants#OPERATION_GET_OBJECT_HANDLES](MtpConstants.md)
- [android.mtp.MtpConstants#OPERATION_GET_OBJECT_INFO](MtpConstants.md)
- [android.mtp.MtpConstants#OPERATION_GET_OBJECT](MtpConstants.md)
- [android.mtp.MtpConstants#OPERATION_GET_THUMB](MtpConstants.md)
- [android.mtp.MtpConstants#OPERATION_DELETE_OBJECT](MtpConstants.md)
- [android.mtp.MtpConstants#OPERATION_SEND_OBJECT_INFO](MtpConstants.md)
- [android.mtp.MtpConstants#OPERATION_SEND_OBJECT](MtpConstants.md)
- [android.mtp.MtpConstants#OPERATION_INITIATE_CAPTURE](MtpConstants.md)
- [android.mtp.MtpConstants#OPERATION_FORMAT_STORE](MtpConstants.md)
- [android.mtp.MtpConstants#OPERATION_RESET_DEVICE](MtpConstants.md)
- [android.mtp.MtpConstants#OPERATION_SELF_TEST](MtpConstants.md)
- [android.mtp.MtpConstants#OPERATION_SET_OBJECT_PROTECTION](MtpConstants.md)
- [android.mtp.MtpConstants#OPERATION_POWER_DOWN](MtpConstants.md)
- [android.mtp.MtpConstants#OPERATION_GET_DEVICE_PROP_DESC](MtpConstants.md)
- [android.mtp.MtpConstants#OPERATION_GET_DEVICE_PROP_VALUE](MtpConstants.md)
- [android.mtp.MtpConstants#OPERATION_SET_DEVICE_PROP_VALUE](MtpConstants.md)
- [android.mtp.MtpConstants#OPERATION_RESET_DEVICE_PROP_VALUE](MtpConstants.md)
- [android.mtp.MtpConstants#OPERATION_TERMINATE_OPEN_CAPTURE](MtpConstants.md)
- [android.mtp.MtpConstants#OPERATION_MOVE_OBJECT](MtpConstants.md)
- [android.mtp.MtpConstants#OPERATION_COPY_OBJECT](MtpConstants.md)
- [android.mtp.MtpConstants#OPERATION_GET_PARTIAL_OBJECT](MtpConstants.md)
- [android.mtp.MtpConstants#OPERATION_INITIATE_OPEN_CAPTURE](MtpConstants.md)
- [android.mtp.MtpConstants#OPERATION_GET_OBJECT_PROPS_SUPPORTED](MtpConstants.md)
- [android.mtp.MtpConstants#OPERATION_GET_OBJECT_PROP_DESC](MtpConstants.md)
- [android.mtp.MtpConstants#OPERATION_GET_OBJECT_PROP_VALUE](MtpConstants.md)
- [android.mtp.MtpConstants#OPERATION_SET_OBJECT_PROP_VALUE](MtpConstants.md)
- [android.mtp.MtpConstants#OPERATION_GET_OBJECT_REFERENCES](MtpConstants.md)
- [android.mtp.MtpConstants#OPERATION_SET_OBJECT_REFERENCES](MtpConstants.md)
- [android.mtp.MtpConstants#OPERATION_SKIP](MtpConstants.md) 

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
