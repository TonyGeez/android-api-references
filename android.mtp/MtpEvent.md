# MtpEvent

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MtpEvent

Kotlin| [Java](../android/mtp/MtpEvent.md) 
| --- | --- |

```
open class MtpEvent
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.mtp.MtpEvent](../android/mtp/MtpEvent.md) |

This class encapsulates information about a MTP event. This corresponds to the events described in appendix G of the MTP specification.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EVENT_CANCEL_TRANSACTION](../android/mtp/MtpEvent.md) Event code for CANCEL_TRANSACTION event |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EVENT_CAPTURE_COMPLETE](../android/mtp/MtpEvent.md) Event code for CAPTURE_COMPLETE event |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EVENT_DEVICE_INFO_CHANGED](../android/mtp/MtpEvent.md) Event code for DEVICE_INFO_CHANGED event |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EVENT_DEVICE_PROP_CHANGED](../android/mtp/MtpEvent.md) Event code for DEVICE_PROP_CHANGED event |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EVENT_DEVICE_RESET](../android/mtp/MtpEvent.md) Event code for DEVICE_RESET event |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EVENT_OBJECT_ADDED](../android/mtp/MtpEvent.md) Event code for OBJECT_ADDED event |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EVENT_OBJECT_INFO_CHANGED](../android/mtp/MtpEvent.md) Event code for OBJECT_INFO_CHANGED event |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EVENT_OBJECT_PROP_CHANGED](../android/mtp/MtpEvent.md) Event code for OBJECT_PROP_CHANGED event |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EVENT_OBJECT_PROP_DESC_CHANGED](../android/mtp/MtpEvent.md) Event code for OBJECT_PROP_DESC_CHANGED event |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EVENT_OBJECT_REFERENCES_CHANGED](../android/mtp/MtpEvent.md) Event code for OBJECT_REFERENCES_CHANGED event |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EVENT_OBJECT_REMOVED](../android/mtp/MtpEvent.md) Event code for OBJECT_REMOVED event |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EVENT_REQUEST_OBJECT_TRANSFER](../android/mtp/MtpEvent.md) Event code for REQUEST_OBJECT_TRANSFER event |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EVENT_STORAGE_INFO_CHANGED](../android/mtp/MtpEvent.md) Event code for STORAGE_INFO_CHANGED event |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EVENT_STORE_ADDED](../android/mtp/MtpEvent.md) Event code for STORE_ADDED event |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EVENT_STORE_FULL](../android/mtp/MtpEvent.md) Event code for STORE_FULL event |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EVENT_STORE_REMOVED](../android/mtp/MtpEvent.md) Event code for STORE_REMOVED event |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EVENT_UNDEFINED](../android/mtp/MtpEvent.md) Event code for UNDEFINED event |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EVENT_UNREPORTED_STATUS](../android/mtp/MtpEvent.md) Event code for UNREPORTED_STATUS event |
| --- | --- |

| Public methods ||
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDevicePropCode](../android/mtp/MtpEvent.md))`()` Obtains devicePropCode event parameter. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getEventCode](../android/mtp/MtpEvent.md))`()` Returns event code of MTP event. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getObjectFormatCode](../android/mtp/MtpEvent.md))`()` Obtains objectFormatCode event parameter. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getObjectHandle](../android/mtp/MtpEvent.md))`()` Obtains objectHandle event parameter. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getObjectPropCode](../android/mtp/MtpEvent.md))`()` Obtains objectPropCode event parameter. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getParameter1](../android/mtp/MtpEvent.md))`()` Obtains the first event parameter. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getParameter2](../android/mtp/MtpEvent.md))`()` Obtains the second event parameter. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getParameter3](../android/mtp/MtpEvent.md))`()` Obtains the third event parameter. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getStorageId](../android/mtp/MtpEvent.md))`()` Obtains storageID event parameter. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getTransactionId](../android/mtp/MtpEvent.md))`()` Obtains transactionID event parameter. |

## Constants

### EVENT_CANCEL_TRANSACTION

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EVENT_CANCEL_TRANSACTION: Int
```

Event code for CANCEL_TRANSACTION event 

 Value: 16385

### EVENT_CAPTURE_COMPLETE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EVENT_CAPTURE_COMPLETE: Int
```

Event code for CAPTURE_COMPLETE event 

 Value: 16397

### EVENT_DEVICE_INFO_CHANGED

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EVENT_DEVICE_INFO_CHANGED: Int
```

Event code for DEVICE_INFO_CHANGED event 

 Value: 16392

### EVENT_DEVICE_PROP_CHANGED

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EVENT_DEVICE_PROP_CHANGED: Int
```

Event code for DEVICE_PROP_CHANGED event 

 Value: 16390

### EVENT_DEVICE_RESET

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EVENT_DEVICE_RESET: Int
```

Event code for DEVICE_RESET event 

 Value: 16395

### EVENT_OBJECT_ADDED

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EVENT_OBJECT_ADDED: Int
```

Event code for OBJECT_ADDED event 

 Value: 16386

### EVENT_OBJECT_INFO_CHANGED

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EVENT_OBJECT_INFO_CHANGED: Int
```

Event code for OBJECT_INFO_CHANGED event 

 Value: 16391

### EVENT_OBJECT_PROP_CHANGED

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EVENT_OBJECT_PROP_CHANGED: Int
```

Event code for OBJECT_PROP_CHANGED event 

 Value: 51201

### EVENT_OBJECT_PROP_DESC_CHANGED

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EVENT_OBJECT_PROP_DESC_CHANGED: Int
```

Event code for OBJECT_PROP_DESC_CHANGED event 

 Value: 51202

### EVENT_OBJECT_REFERENCES_CHANGED

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EVENT_OBJECT_REFERENCES_CHANGED: Int
```

Event code for OBJECT_REFERENCES_CHANGED event 

 Value: 51203

### EVENT_OBJECT_REMOVED

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EVENT_OBJECT_REMOVED: Int
```

Event code for OBJECT_REMOVED event 

 Value: 16387

### EVENT_REQUEST_OBJECT_TRANSFER

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EVENT_REQUEST_OBJECT_TRANSFER: Int
```

Event code for REQUEST_OBJECT_TRANSFER event 

 Value: 16393

### EVENT_STORAGE_INFO_CHANGED

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EVENT_STORAGE_INFO_CHANGED: Int
```

Event code for STORAGE_INFO_CHANGED event 

 Value: 16396

### EVENT_STORE_ADDED

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EVENT_STORE_ADDED: Int
```

Event code for STORE_ADDED event 

 Value: 16388

### EVENT_STORE_FULL

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EVENT_STORE_FULL: Int
```

Event code for STORE_FULL event 

 Value: 16394

### EVENT_STORE_REMOVED

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EVENT_STORE_REMOVED: Int
```

Event code for STORE_REMOVED event 

 Value: 16389

### EVENT_UNDEFINED

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EVENT_UNDEFINED: Int
```

Event code for UNDEFINED event 

 Value: 16384

### EVENT_UNREPORTED_STATUS

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EVENT_UNREPORTED_STATUS: Int
```

Event code for UNREPORTED_STATUS event 

 Value: 16398

## Public methods

### getDevicePropCode

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDevicePropCode(): Int
```

Obtains devicePropCode event parameter. 
**See Also**

- [#EVENT_DEVICE_PROP_CHANGED](../android/mtp/MtpEvent.md) 

### getEventCode

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getEventCode(): Int
```

Returns event code of MTP event. See the USB-IF MTP specification for the details of event constants.

| Return ||
|----------------------------------------------------------------------------|------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | event code |

### getObjectFormatCode

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getObjectFormatCode(): Int
```

Obtains objectFormatCode event parameter. 
**See Also**

- [#EVENT_OBJECT_PROP_DESC_CHANGED](../android/mtp/MtpEvent.md) 

### getObjectHandle

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getObjectHandle(): Int
```

Obtains objectHandle event parameter. 
**See Also**

- [#EVENT_OBJECT_ADDED](../android/mtp/MtpEvent.md)
- [#EVENT_OBJECT_REMOVED](../android/mtp/MtpEvent.md)
- [#EVENT_OBJECT_INFO_CHANGED](../android/mtp/MtpEvent.md)
- [#EVENT_REQUEST_OBJECT_TRANSFER](../android/mtp/MtpEvent.md)
- [#EVENT_OBJECT_PROP_CHANGED](../android/mtp/MtpEvent.md)
- [#EVENT_OBJECT_REFERENCES_CHANGED](../android/mtp/MtpEvent.md) 

### getObjectPropCode

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getObjectPropCode(): Int
```

Obtains objectPropCode event parameter. 
**See Also**

- [#EVENT_OBJECT_PROP_CHANGED](../android/mtp/MtpEvent.md)
- [#EVENT_OBJECT_PROP_DESC_CHANGED](../android/mtp/MtpEvent.md) 

### getParameter1

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getParameter1(): Int
```

Obtains the first event parameter. 

### getParameter2

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getParameter2(): Int
```

Obtains the second event parameter. 

### getParameter3

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getParameter3(): Int
```

Obtains the third event parameter. 

### getStorageId

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getStorageId(): Int
```

Obtains storageID event parameter. 
**See Also**

- [#EVENT_STORE_ADDED](../android/mtp/MtpEvent.md)
- [#EVENT_STORE_REMOVED](../android/mtp/MtpEvent.md)
- [#EVENT_STORE_FULL](../android/mtp/MtpEvent.md)
- [#EVENT_STORAGE_INFO_CHANGED](../android/mtp/MtpEvent.md) 

### getTransactionId

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getTransactionId(): Int
```

Obtains transactionID event parameter. 
**See Also**

- [#EVENT_CAPTURE_COMPLETE](../android/mtp/MtpEvent.md)
