# MtpStorageInfo

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MtpStorageInfo

Kotlin| [Java](https://developer.android.com/reference/android/mtp/MtpStorageInfo "View this page in Java") 

```
class MtpStorageInfo
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.mtp.MtpStorageInfo](https://developer.android.com/reference/kotlin/android/mtp/MtpStorageInfo#) |

This class encapsulates information about a storage unit on an MTP device. This corresponds to the StorageInfo Dataset described in section 5.2.2 of the MTP specification.

## Summary

| Public methods ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getDescription](https://developer.android.com/reference/kotlin/android/mtp/MtpStorageInfo#getDescription())`()` Returns the description string for the storage unit. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getFreeSpace](https://developer.android.com/reference/kotlin/android/mtp/MtpStorageInfo#getFreeSpace())`()` Returns the amount of free space in the storage unit in bytes |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getMaxCapacity](https://developer.android.com/reference/kotlin/android/mtp/MtpStorageInfo#getMaxCapacity())`()` Returns the maximum storage capacity for the storage unit in bytes |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getStorageId](https://developer.android.com/reference/kotlin/android/mtp/MtpStorageInfo#getStorageId())`()` Returns the storage ID for the storage unit. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getVolumeIdentifier](https://developer.android.com/reference/kotlin/android/mtp/MtpStorageInfo#getVolumeIdentifier())`()` Returns the volume identifier for the storage unit |

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
