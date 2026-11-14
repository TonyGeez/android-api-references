# MtpEvent

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MtpEvent

Kotlin| [Java](https://developer.android.com/reference/android/mtp/MtpEvent "View this page in Java") 
| --- | --- |

```
open class MtpEvent
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.mtp.MtpEvent](https://developer.android.com/reference/kotlin/android/mtp/MtpEvent#) |

This class encapsulates information about a MTP event. This corresponds to the events described in appendix G of the MTP specification.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EVENT_CANCEL_TRANSACTION](https://developer.android.com/reference/kotlin/android/mtp/MtpEvent#EVENT_CANCEL_TRANSACTION:kotlin.Int) Event code for CANCEL_TRANSACTION event |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EVENT_CAPTURE_COMPLETE](https://developer.android.com/reference/kotlin/android/mtp/MtpEvent#EVENT_CAPTURE_COMPLETE:kotlin.Int) Event code for CAPTURE_COMPLETE event |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EVENT_DEVICE_INFO_CHANGED](https://developer.android.com/reference/kotlin/android/mtp/MtpEvent#EVENT_DEVICE_INFO_CHANGED:kotlin.Int) Event code for DEVICE_INFO_CHANGED event |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EVENT_DEVICE_PROP_CHANGED](https://developer.android.com/reference/kotlin/android/mtp/MtpEvent#EVENT_DEVICE_PROP_CHANGED:kotlin.Int) Event code for DEVICE_PROP_CHANGED event |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EVENT_DEVICE_RESET](https://developer.android.com/reference/kotlin/android/mtp/MtpEvent#EVENT_DEVICE_RESET:kotlin.Int) Event code for DEVICE_RESET event |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EVENT_OBJECT_ADDED](https://developer.android.com/reference/kotlin/android/mtp/MtpEvent#EVENT_OBJECT_ADDED:kotlin.Int) Event code for OBJECT_ADDED event |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EVENT_OBJECT_INFO_CHANGED](https://developer.android.com/reference/kotlin/android/mtp/MtpEvent#EVENT_OBJECT_INFO_CHANGED:kotlin.Int) Event code for OBJECT_INFO_CHANGED event |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EVENT_OBJECT_PROP_CHANGED](https://developer.android.com/reference/kotlin/android/mtp/MtpEvent#EVENT_OBJECT_PROP_CHANGED:kotlin.Int) Event code for OBJECT_PROP_CHANGED event |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EVENT_OBJECT_PROP_DESC_CHANGED](https://developer.android.com/reference/kotlin/android/mtp/MtpEvent#EVENT_OBJECT_PROP_DESC_CHANGED:kotlin.Int) Event code for OBJECT_PROP_DESC_CHANGED event |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EVENT_OBJECT_REFERENCES_CHANGED](https://developer.android.com/reference/kotlin/android/mtp/MtpEvent#EVENT_OBJECT_REFERENCES_CHANGED:kotlin.Int) Event code for OBJECT_REFERENCES_CHANGED event |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EVENT_OBJECT_REMOVED](https://developer.android.com/reference/kotlin/android/mtp/MtpEvent#EVENT_OBJECT_REMOVED:kotlin.Int) Event code for OBJECT_REMOVED event |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EVENT_REQUEST_OBJECT_TRANSFER](https://developer.android.com/reference/kotlin/android/mtp/MtpEvent#EVENT_REQUEST_OBJECT_TRANSFER:kotlin.Int) Event code for REQUEST_OBJECT_TRANSFER event |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EVENT_STORAGE_INFO_CHANGED](https://developer.android.com/reference/kotlin/android/mtp/MtpEvent#EVENT_STORAGE_INFO_CHANGED:kotlin.Int) Event code for STORAGE_INFO_CHANGED event |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EVENT_STORE_ADDED](https://developer.android.com/reference/kotlin/android/mtp/MtpEvent#EVENT_STORE_ADDED:kotlin.Int) Event code for STORE_ADDED event |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EVENT_STORE_FULL](https://developer.android.com/reference/kotlin/android/mtp/MtpEvent#EVENT_STORE_FULL:kotlin.Int) Event code for STORE_FULL event |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EVENT_STORE_REMOVED](https://developer.android.com/reference/kotlin/android/mtp/MtpEvent#EVENT_STORE_REMOVED:kotlin.Int) Event code for STORE_REMOVED event |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EVENT_UNDEFINED](https://developer.android.com/reference/kotlin/android/mtp/MtpEvent#EVENT_UNDEFINED:kotlin.Int) Event code for UNDEFINED event |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EVENT_UNREPORTED_STATUS](https://developer.android.com/reference/kotlin/android/mtp/MtpEvent#EVENT_UNREPORTED_STATUS:kotlin.Int) Event code for UNREPORTED_STATUS event |
| --- | --- |

| Public methods ||
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDevicePropCode](https://developer.android.com/reference/kotlin/android/mtp/MtpEvent#getDevicePropCode())`()` Obtains devicePropCode event parameter. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getEventCode](https://developer.android.com/reference/kotlin/android/mtp/MtpEvent#getEventCode())`()` Returns event code of MTP event. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getObjectFormatCode](https://developer.android.com/reference/kotlin/android/mtp/MtpEvent#getObjectFormatCode())`()` Obtains objectFormatCode event parameter. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getObjectHandle](https://developer.android.com/reference/kotlin/android/mtp/MtpEvent#getObjectHandle())`()` Obtains objectHandle event parameter. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getObjectPropCode](https://developer.android.com/reference/kotlin/android/mtp/MtpEvent#getObjectPropCode())`()` Obtains objectPropCode event parameter. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getParameter1](https://developer.android.com/reference/kotlin/android/mtp/MtpEvent#getParameter1())`()` Obtains the first event parameter. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getParameter2](https://developer.android.com/reference/kotlin/android/mtp/MtpEvent#getParameter2())`()` Obtains the second event parameter. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getParameter3](https://developer.android.com/reference/kotlin/android/mtp/MtpEvent#getParameter3())`()` Obtains the third event parameter. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getStorageId](https://developer.android.com/reference/kotlin/android/mtp/MtpEvent#getStorageId())`()` Obtains storageID event parameter. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getTransactionId](https://developer.android.com/reference/kotlin/android/mtp/MtpEvent#getTransactionId())`()` Obtains transactionID event parameter. |

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

- [#EVENT_DEVICE_PROP_CHANGED](https://developer.android.com/reference/kotlin/android/mtp/MtpEvent#EVENT_DEVICE_PROP_CHANGED:kotlin.Int) 

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

- [#EVENT_OBJECT_PROP_DESC_CHANGED](https://developer.android.com/reference/kotlin/android/mtp/MtpEvent#EVENT_OBJECT_PROP_DESC_CHANGED:kotlin.Int) 

### getObjectHandle

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getObjectHandle(): Int
```

Obtains objectHandle event parameter. 
**See Also**

- [#EVENT_OBJECT_ADDED](https://developer.android.com/reference/kotlin/android/mtp/MtpEvent#EVENT_OBJECT_ADDED:kotlin.Int)
- [#EVENT_OBJECT_REMOVED](https://developer.android.com/reference/kotlin/android/mtp/MtpEvent#EVENT_OBJECT_REMOVED:kotlin.Int)
- [#EVENT_OBJECT_INFO_CHANGED](https://developer.android.com/reference/kotlin/android/mtp/MtpEvent#EVENT_OBJECT_INFO_CHANGED:kotlin.Int)
- [#EVENT_REQUEST_OBJECT_TRANSFER](https://developer.android.com/reference/kotlin/android/mtp/MtpEvent#EVENT_REQUEST_OBJECT_TRANSFER:kotlin.Int)
- [#EVENT_OBJECT_PROP_CHANGED](https://developer.android.com/reference/kotlin/android/mtp/MtpEvent#EVENT_OBJECT_PROP_CHANGED:kotlin.Int)
- [#EVENT_OBJECT_REFERENCES_CHANGED](https://developer.android.com/reference/kotlin/android/mtp/MtpEvent#EVENT_OBJECT_REFERENCES_CHANGED:kotlin.Int) 

### getObjectPropCode

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getObjectPropCode(): Int
```

Obtains objectPropCode event parameter. 
**See Also**

- [#EVENT_OBJECT_PROP_CHANGED](https://developer.android.com/reference/kotlin/android/mtp/MtpEvent#EVENT_OBJECT_PROP_CHANGED:kotlin.Int)
- [#EVENT_OBJECT_PROP_DESC_CHANGED](https://developer.android.com/reference/kotlin/android/mtp/MtpEvent#EVENT_OBJECT_PROP_DESC_CHANGED:kotlin.Int) 

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

- [#EVENT_STORE_ADDED](https://developer.android.com/reference/kotlin/android/mtp/MtpEvent#EVENT_STORE_ADDED:kotlin.Int)
- [#EVENT_STORE_REMOVED](https://developer.android.com/reference/kotlin/android/mtp/MtpEvent#EVENT_STORE_REMOVED:kotlin.Int)
- [#EVENT_STORE_FULL](https://developer.android.com/reference/kotlin/android/mtp/MtpEvent#EVENT_STORE_FULL:kotlin.Int)
- [#EVENT_STORAGE_INFO_CHANGED](https://developer.android.com/reference/kotlin/android/mtp/MtpEvent#EVENT_STORAGE_INFO_CHANGED:kotlin.Int) 

### getTransactionId

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getTransactionId(): Int
```

Obtains transactionID event parameter. 
**See Also**

- [#EVENT_CAPTURE_COMPLETE](https://developer.android.com/reference/kotlin/android/mtp/MtpEvent#EVENT_CAPTURE_COMPLETE:kotlin.Int)
