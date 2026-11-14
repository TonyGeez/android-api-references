Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# StorageStats

Kotlin | [Java](StorageStats.md)
| --- | --- |

```
class StorageStats : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.app.usage.StorageStats](StorageStats.md) |

Storage statistics for a UID, package, or `https://developer.android.com/reference/kotlin/android/os/UserHandle.html#` on a single storage volume.

## Summary

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/usage/StorageStats#APP_DATA_TYPE_FILE_TYPE_APK:kotlin.Int` Represents all . |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/usage/StorageStats#APP_DATA_TYPE_FILE_TYPE_CURRENT_PROFILE:kotlin.Int` Represents current profile of application. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/usage/StorageStats#APP_DATA_TYPE_FILE_TYPE_DEXOPT_ARTIFACT:kotlin.Int` Represents all nonstale dexopt and runtime artifacts of application. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/usage/StorageStats#APP_DATA_TYPE_FILE_TYPE_DM:kotlin.Int` Represents all . |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/usage/StorageStats#APP_DATA_TYPE_FILE_TYPE_REFERENCE_PROFILE:kotlin.Int` Represents reference profile of application. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/usage/StorageStats#APP_DATA_TYPE_LIB:kotlin.Int` Represents lib/ in application code path. |
| --- | --- |

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` Descriptor bit used with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()`: indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` Flag for use with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/usage/StorageStats#describeContents()()` Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/app/usage/StorageStats#getAppBytes()()` Return the size of app. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/app/usage/StorageStats#getAppBytesByDataType(kotlin.Int)(dataType: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Return the size of the specified data type. |
| --- | --- |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/app/usage/StorageStats#getCacheBytes()()` Return the size of all cached data. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/app/usage/StorageStats#getDataBytes()()` Return the size of all data. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/app/usage/StorageStats#getExternalCacheBytes()()` Return the size of all cached data in the primary external/shared storage. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/usage/StorageStats#writeToParcel(android.os.Parcel,%20kotlin.Int)(dest: https://developer.android.com/reference/kotlin/android/os/Parcel.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Flatten this object in to a Parcel. |

| Properties ||
|---|---|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [StorageStats](StorageStats.md)!\> | `https://developer.android.com/reference/kotlin/android/app/usage/StorageStats#CREATOR:android.os.Parcelable.Creator` <br /> |

## Constants

### APP_DATA_TYPE_FILE_TYPE_APK

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val APP_DATA_TYPE_FILE_TYPE_APK: Int
```

Represents all .apk files in application code path. Can be used as an input to `https://developer.android.com/reference/kotlin/android/app/usage/StorageStats#getAppBytesByDataType(kotlin.Int)` to get the sum of sizes for files of this type.

 Value: 3

### APP_DATA_TYPE_FILE_TYPE_CURRENT_PROFILE

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val APP_DATA_TYPE_FILE_TYPE_CURRENT_PROFILE: Int
```

Represents current profile of application. Current profiles may or may not be used during the next profile-guided dexopt. Can be used as an input to `https://developer.android.com/reference/kotlin/android/app/usage/StorageStats#getAppBytesByDataType(kotlin.Int)` to get the size of files of this type. This size fluctuates regularly, it goes up when the user uses more and more classes/methods and comes down when a deamon merges this into the ref profile and does profile-guided dexopt.

 Value: 2

### APP_DATA_TYPE_FILE_TYPE_DEXOPT_ARTIFACT

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val APP_DATA_TYPE_FILE_TYPE_DEXOPT_ARTIFACT: Int
```

Represents all nonstale dexopt and runtime artifacts of application. This includes AOT-compiled code and other data that can speed up app execution. For more detailed information, read the [JIT compiler](https://source.android.com/docs/core/runtime/jit-compiler#flow) guide. Dexopt artifacts become stale when one of their dependencies has changed. They may be cleaned up or replaced by ART Services at any time. For a preload app, this type includes dexopt artifacts on readonly partitions if they are up-to-date. Can be used as an input to `https://developer.android.com/reference/kotlin/android/app/usage/StorageStats#getAppBytesByDataType(kotlin.Int)` to get the sum of sizes for files of this type. The sum might include the size of data that is part of appBytes, dataBytes or cacheBytes.

 Value: 0

### APP_DATA_TYPE_FILE_TYPE_DM

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val APP_DATA_TYPE_FILE_TYPE_DM: Int
```

Represents all .dm files in application code path. Can be used as an input to `https://developer.android.com/reference/kotlin/android/app/usage/StorageStats#getAppBytesByDataType(kotlin.Int)` to get the sum of sizes for files of this type.

 Value: 4

### APP_DATA_TYPE_FILE_TYPE_REFERENCE_PROFILE

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val APP_DATA_TYPE_FILE_TYPE_REFERENCE_PROFILE: Int
```

Represents reference profile of application. Reference profiles are the ones used during the last profile-guided dexopt. If the last dexopt wasn't profile-guided, then these profiles were not used. Can be used as an input to `https://developer.android.com/reference/kotlin/android/app/usage/StorageStats#getAppBytesByDataType(kotlin.Int)` to get the size of files of this type.

 Value: 1

### APP_DATA_TYPE_LIB

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val APP_DATA_TYPE_LIB: Int
```

Represents lib/ in application code path. Can be used as an input to `https://developer.android.com/reference/kotlin/android/app/usage/StorageStats#getAppBytesByDataType(kotlin.Int)` to get the size of lib/ directory.

 Value: 5

## Public methods

### describeContents

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### getAppBytes

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getAppBytes(): Long
```

Return the size of app. This includes `APK` files, optimized compiler output, and unpacked native libraries.

If the primary external/shared storage is hosted on this storage device, then this includes files stored under `https://developer.android.com/reference/kotlin/android/content/Context.html#getObbDir()`.

Code is shared between all users on a multiuser device. 
Value is a non-negative number of bytes.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | Value is a non-negative number of bytes. |

### getAppBytesByDataType

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getAppBytesByDataType(dataType: Int): Long
```

Return the size of the specified data type. This includes files stored under application code path.

If there is more than one package inside a uid, the return represents the aggregated stats when query StorageStat for package or uid. The data is not collected and the return defaults to 0 when query StorageStats for user.

Data is isolated for each user on a multiuser device.

| Parameters ||
|---|---|
| `dataType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Value is one of the following: - `https://developer.android.com/reference/kotlin/android/app/usage/StorageStats#APP_DATA_TYPE_FILE_TYPE_DEXOPT_ARTIFACT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/usage/StorageStats#APP_DATA_TYPE_FILE_TYPE_REFERENCE_PROFILE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/usage/StorageStats#APP_DATA_TYPE_FILE_TYPE_CURRENT_PROFILE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/usage/StorageStats#APP_DATA_TYPE_FILE_TYPE_APK:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/usage/StorageStats#APP_DATA_TYPE_FILE_TYPE_DM:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/usage/StorageStats#APP_DATA_TYPE_LIB:kotlin.Int` |

### getCacheBytes

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getCacheBytes(): Long
```

Return the size of all cached data. This includes files stored under `https://developer.android.com/reference/kotlin/android/content/Context.html#getCacheDir()` and `https://developer.android.com/reference/kotlin/android/content/Context.html#getCodeCacheDir()`.

If the primary external/shared storage is hosted on this storage device, then this includes files stored under `https://developer.android.com/reference/kotlin/android/content/Context.html#getExternalCacheDir()`.

Cached data is isolated for each user on a multiuser device. 
Value is a non-negative number of bytes.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | Value is a non-negative number of bytes. |

### getDataBytes

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getDataBytes(): Long
```

Return the size of all data. This includes files stored under `https://developer.android.com/reference/kotlin/android/content/Context.html#getDataDir()`, `https://developer.android.com/reference/kotlin/android/content/Context.html#getCacheDir()`, `https://developer.android.com/reference/kotlin/android/content/Context.html#getCodeCacheDir()`.

If the primary external/shared storage is hosted on this storage device, then this includes files stored under `https://developer.android.com/reference/kotlin/android/content/Context.html#getExternalFilesDir(kotlin.String)`, `https://developer.android.com/reference/kotlin/android/content/Context.html#getExternalCacheDir()`, and `https://developer.android.com/reference/kotlin/android/content/Context.html#getExternalMediaDirs()`.

Data is isolated for each user on a multiuser device. 
Value is a non-negative number of bytes.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | Value is a non-negative number of bytes. |

### getExternalCacheBytes

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getExternalCacheBytes(): Long
```

Return the size of all cached data in the primary external/shared storage. This includes files stored under `https://developer.android.com/reference/kotlin/android/content/Context.html#getExternalCacheDir()`.

Cached data is isolated for each user on a multiuser device. 
Value is a non-negative number of bytes.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | Value is a non-negative number of bytes. |

### writeToParcel

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

Flatten this object in to a Parcel.

| Parameters ||
|---|---|
| `dest` | [Parcel](../android.os/Parcel.md): The Parcel in which the object should be written. This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` |

## Properties

### CREATOR

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<StorageStats!>
```
