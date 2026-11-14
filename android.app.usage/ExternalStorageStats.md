# ExternalStorageStats

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ExternalStorageStats

Kotlin| [Java](https://developer.android.com/reference/android/app/usage/ExternalStorageStats "View this page in Java") 
| --- | --- |

```
class ExternalStorageStats : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.app.usage.ExternalStorageStats](https://developer.android.com/reference/kotlin/android/app/usage/ExternalStorageStats#) |

Shared/external storage statistics for a [UserHandle](https://developer.android.com/reference/kotlin/android/os/UserHandle.html#) on a single storage volume.

## Summary

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/app/usage/ExternalStorageStats#describeContents())`()` <br /> |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getAppBytes](https://developer.android.com/reference/kotlin/android/app/usage/ExternalStorageStats#getAppBytes())`()` Return the total bytes used by app files in the shared/external storage hosted on this volume. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getAudioBytes](https://developer.android.com/reference/kotlin/android/app/usage/ExternalStorageStats#getAudioBytes())`()` Return the total bytes used by all audio files in the shared/external storage hosted on this volume. |
| --- | --- |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getImageBytes](https://developer.android.com/reference/kotlin/android/app/usage/ExternalStorageStats#getImageBytes())`()` Return the total bytes used by all image files in the shared/external storage hosted on this volume. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getTotalBytes](https://developer.android.com/reference/kotlin/android/app/usage/ExternalStorageStats#getTotalBytes())`()` Return the total bytes used by all files in the shared/external storage hosted on this volume. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getVideoBytes](https://developer.android.com/reference/kotlin/android/app/usage/ExternalStorageStats#getVideoBytes())`()` Return the total bytes used by all video files in the shared/external storage hosted on this volume. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/app/usage/ExternalStorageStats#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Properties ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [ExternalStorageStats](https://developer.android.com/reference/kotlin/android/app/usage/ExternalStorageStats#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/app/usage/ExternalStorageStats#CREATOR:android.os.Parcelable.Creator) <br /> |

## Public methods

### describeContents

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### getAppBytes

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAppBytes(): Long
```

Return the total bytes used by app files in the shared/external storage hosted on this volume.

This data is already accounted against individual apps as returned through [StorageStats](https://developer.android.com/reference/kotlin/android/app/usage/StorageStats).

This value only includes data which is isolated for each user on a multiuser device. 
Value is a non-negative number of bytes.

| Return ||
|------------------------------------------------------------------------------|------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | Value is a non-negative number of bytes. |

### getAudioBytes

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAudioBytes(): Long
```

Return the total bytes used by all audio files in the shared/external storage hosted on this volume.

This value only includes data which is isolated for each user on a multiuser device. This value does not include any app files which are all accounted under [getAppBytes()](https://developer.android.com/reference/kotlin/android/app/usage/ExternalStorageStats#getAppBytes()). 
Value is a non-negative number of bytes.

| Return ||
|------------------------------------------------------------------------------|------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | Value is a non-negative number of bytes. |

### getImageBytes

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getImageBytes(): Long
```

Return the total bytes used by all image files in the shared/external storage hosted on this volume.

This value only includes data which is isolated for each user on a multiuser device. This value does not include any app files which are all accounted under [getAppBytes()](https://developer.android.com/reference/kotlin/android/app/usage/ExternalStorageStats#getAppBytes()). 
Value is a non-negative number of bytes.

| Return ||
|------------------------------------------------------------------------------|------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | Value is a non-negative number of bytes. |

### getTotalBytes

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTotalBytes(): Long
```

Return the total bytes used by all files in the shared/external storage hosted on this volume.

This value only includes data which is isolated for each user on a multiuser device. Any OBB data shared between users is not accounted in this value. 
Value is a non-negative number of bytes.

| Return ||
|------------------------------------------------------------------------------|------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | Value is a non-negative number of bytes. |

### getVideoBytes

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getVideoBytes(): Long
```

Return the total bytes used by all video files in the shared/external storage hosted on this volume.

This value only includes data which is isolated for each user on a multiuser device. This value does not include any app files which are all accounted under [getAppBytes()](https://developer.android.com/reference/kotlin/android/app/usage/ExternalStorageStats#getAppBytes()). 
Value is a non-negative number of bytes.

| Return ||
|------------------------------------------------------------------------------|------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | Value is a non-negative number of bytes. |

### writeToParcel

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#):The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<ExternalStorageStats!>
```
