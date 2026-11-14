# MtpStorageInfo

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MtpStorageInfo

Kotlin| [Java](../android/mtp/MtpStorageInfo.md) 
| --- | --- |

```
class MtpStorageInfo
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.mtp.MtpStorageInfo](../android/mtp/MtpStorageInfo.md) |

This class encapsulates information about a storage unit on an MTP device. This corresponds to the StorageInfo Dataset described in section 5.2.2 of the MTP specification.

## Summary

| Public methods ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getDescription](../android/mtp/MtpStorageInfo.md))`()` Returns the description string for the storage unit. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getFreeSpace](../android/mtp/MtpStorageInfo.md))`()` Returns the amount of free space in the storage unit in bytes |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getMaxCapacity](../android/mtp/MtpStorageInfo.md))`()` Returns the maximum storage capacity for the storage unit in bytes |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getStorageId](../android/mtp/MtpStorageInfo.md))`()` Returns the storage ID for the storage unit. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getVolumeIdentifier](../android/mtp/MtpStorageInfo.md))`()` Returns the volume identifier for the storage unit |

## Public methods

### getDescription

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDescription(): String
```

Returns the description string for the storage unit. This is typically displayed to the user in the user interface on the MTP host.

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | the storage unit description This value cannot be`null`. |

### getFreeSpace

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getFreeSpace(): Long
```

Returns the amount of free space in the storage unit in bytes

| Return ||
|------------------------------------------------------------------------------|--------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the amount of free space |

### getMaxCapacity

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMaxCapacity(): Long
```

Returns the maximum storage capacity for the storage unit in bytes

| Return ||
|------------------------------------------------------------------------------|----------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the maximum capacity |

### getStorageId

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getStorageId(): Int
```

Returns the storage ID for the storage unit. The storage ID uniquely identifies the storage unit on the MTP device.

| Return ||
|----------------------------------------------------------------------------|----------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the storage ID |

### getVolumeIdentifier

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getVolumeIdentifier(): String
```

Returns the volume identifier for the storage unit

| Return ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | the storage volume identifier This value cannot be`null`. |
