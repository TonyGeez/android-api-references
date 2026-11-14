# AssetFileDescriptor

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AssetFileDescriptor

Kotlin| [Java](https://developer.android.com/reference/android/content/res/AssetFileDescriptor "View this page in Java") 

```
open class AssetFileDescriptor : Closeable, Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.content.res.AssetFileDescriptor](https://developer.android.com/reference/kotlin/android/content/res/AssetFileDescriptor#) |

File descriptor of an entry in the AssetManager. This provides your own opened FileDescriptor that can be used to read the data, as well as the offset and length of that entry's data in the file.

## Summary

| Nested classes ||
|------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open | [AutoCloseInputStream](https://developer.android.com/reference/kotlin/android/content/res/AssetFileDescriptor.AutoCloseInputStream) An InputStream you can create on a ParcelFileDescriptor, which will take care of calling android. |
| open | [AutoCloseOutputStream](https://developer.android.com/reference/kotlin/android/content/res/AssetFileDescriptor.AutoCloseOutputStream) An OutputStream you can create on a ParcelFileDescriptor, which will take care of calling android. |

| Constants ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [UNKNOWN_LENGTH](https://developer.android.com/reference/kotlin/android/content/res/AssetFileDescriptor#UNKNOWN_LENGTH:kotlin.Long) Length used with [AssetFileDescriptor(android.os.ParcelFileDescriptor,long,long)](https://developer.android.com/reference/kotlin/android/content/res/AssetFileDescriptor#AssetFileDescriptor(android.os.ParcelFileDescriptor,%20kotlin.Long,%20kotlin.Long))and [getDeclaredLength](https://developer.android.com/reference/kotlin/android/content/res/AssetFileDescriptor#getDeclaredLength())when a length has not been declared. |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [AssetFileDescriptor](https://developer.android.com/reference/kotlin/android/content/res/AssetFileDescriptor#AssetFileDescriptor(android.os.ParcelFileDescriptor,%20kotlin.Long,%20kotlin.Long))`(`fd:` ` [ParcelFileDescriptor](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#)!`, `startOffset:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `length:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Create a new AssetFileDescriptor from the given values. |
| [AssetFileDescriptor](https://developer.android.com/reference/kotlin/android/content/res/AssetFileDescriptor#AssetFileDescriptor(android.os.ParcelFileDescriptor,%20kotlin.Long,%20kotlin.Long,%20android.os.Bundle))`(`fd:` ` [ParcelFileDescriptor](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#)!`, `startOffset:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `length:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `extras:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!`)` Create a new AssetFileDescriptor from the given values. |

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](https://developer.android.com/reference/kotlin/android/content/res/AssetFileDescriptor#close())`()` Convenience for calling`getParcelFileDescriptor().close()`. |
| open [FileInputStream](https://developer.android.com/reference/kotlin/java/io/FileInputStream.html#)! | [createInputStream](https://developer.android.com/reference/kotlin/android/content/res/AssetFileDescriptor#createInputStream())`()` Create and return a new auto-close input stream for this asset. |
| open [FileOutputStream](https://developer.android.com/reference/kotlin/java/io/FileOutputStream.html#)! | [createOutputStream](https://developer.android.com/reference/kotlin/android/content/res/AssetFileDescriptor#createOutputStream())`()` Create and return a new auto-close output stream for this asset. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/content/res/AssetFileDescriptor#describeContents())`()` <br /> |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getDeclaredLength](https://developer.android.com/reference/kotlin/android/content/res/AssetFileDescriptor#getDeclaredLength())`()` Return the actual number of bytes that were declared when the AssetFileDescriptor was constructed. |
| open [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)! | [getExtras](https://developer.android.com/reference/kotlin/android/content/res/AssetFileDescriptor#getExtras())`()` Returns any additional details that can be used to interpret the underlying file descriptor. |
| open [FileDescriptor](https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#)! | [getFileDescriptor](https://developer.android.com/reference/kotlin/android/content/res/AssetFileDescriptor#getFileDescriptor())`()` Returns the FileDescriptor that can be used to read the data in the file. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getLength](https://developer.android.com/reference/kotlin/android/content/res/AssetFileDescriptor#getLength())`()` Returns the total number of bytes of this asset entry's data. |
| open [ParcelFileDescriptor](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#)! | [getParcelFileDescriptor](https://developer.android.com/reference/kotlin/android/content/res/AssetFileDescriptor#getParcelFileDescriptor())`()` The AssetFileDescriptor contains its own ParcelFileDescriptor, which in addition to the normal FileDescriptor object also allows you to close the descriptor when you are done with it. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getStartOffset](https://developer.android.com/reference/kotlin/android/content/res/AssetFileDescriptor#getStartOffset())`()` Returns the byte offset where this asset entry's data starts. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/content/res/AssetFileDescriptor#toString())`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/content/res/AssetFileDescriptor#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`out:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Properties ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [AssetFileDescriptor](https://developer.android.com/reference/kotlin/android/content/res/AssetFileDescriptor#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/content/res/AssetFileDescriptor#CREATOR:android.os.Parcelable.Creator) <br /> |

## Constants

### UNKNOWN_LENGTH

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val UNKNOWN_LENGTH: Long
```

Length used with [AssetFileDescriptor(android.os.ParcelFileDescriptor,long,long)](https://developer.android.com/reference/kotlin/android/content/res/AssetFileDescriptor#AssetFileDescriptor(android.os.ParcelFileDescriptor,%20kotlin.Long,%20kotlin.Long))and [getDeclaredLength](https://developer.android.com/reference/kotlin/android/content/res/AssetFileDescriptor#getDeclaredLength())when a length has not been declared. This means the data extends to the end of the file. 

 Value: -1L

## Public constructors

### AssetFileDescriptor

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
AssetFileDescriptor(
    fd: ParcelFileDescriptor!, 
    startOffset: Long, 
    length: Long)
```

Create a new AssetFileDescriptor from the given values.

| Parameters ||
|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `fd` | [ParcelFileDescriptor](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#)!:The underlying file descriptor. |
| `startOffset` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The location within the file that the asset starts. This must be 0 if length is UNKNOWN_LENGTH. |
| `length` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The number of bytes of the asset, or [UNKNOWN_LENGTH](https://developer.android.com/reference/kotlin/android/content/res/AssetFileDescriptor#UNKNOWN_LENGTH:kotlin.Long) if it extends to the end of the file. |

### AssetFileDescriptor

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
AssetFileDescriptor(
    fd: ParcelFileDescriptor!, 
    startOffset: Long, 
    length: Long, 
    extras: Bundle!)
```

Create a new AssetFileDescriptor from the given values.

| Parameters ||
|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `fd` | [ParcelFileDescriptor](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#)!:The underlying file descriptor. |
| `startOffset` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The location within the file that the asset starts. This must be 0 if length is UNKNOWN_LENGTH. |
| `length` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The number of bytes of the asset, or [UNKNOWN_LENGTH](https://developer.android.com/reference/kotlin/android/content/res/AssetFileDescriptor#UNKNOWN_LENGTH:kotlin.Long) if it extends to the end of the file. |
| `extras` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!:additional details that can be used to interpret the underlying file descriptor. May be null. |

## Public methods

### close

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun close(): Unit
```

Convenience for calling`getParcelFileDescriptor().close()`.

| Exceptions ||
|-----------------------|-----------------------------------|
| `java.lang.Exception` | if this resource cannot be closed |
| `java.io.IOException` | if an I/O error occurs |

### createInputStream

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun createInputStream(): FileInputStream!
```

Create and return a new auto-close input stream for this asset. This will either return a full asset [AutoCloseInputStream](https://developer.android.com/reference/kotlin/android/content/res/AssetFileDescriptor.AutoCloseInputStream), or an underlying [ParcelFileDescriptor.AutoCloseInputStream](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.AutoCloseInputStream.html#) depending on whether the the object represents a complete file or sub-section of a file. You should only call this once for a particular asset. 

### createOutputStream

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun createOutputStream(): FileOutputStream!
```

Create and return a new auto-close output stream for this asset. This will either return a full asset [AutoCloseOutputStream](https://developer.android.com/reference/kotlin/android/content/res/AssetFileDescriptor.AutoCloseOutputStream), or an underlying [ParcelFileDescriptor.AutoCloseOutputStream](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.AutoCloseOutputStream.html#) depending on whether the the object represents a complete file or sub-section of a file. You should only call this once for a particular asset. 

### describeContents

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### getDeclaredLength

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDeclaredLength(): Long
```

Return the actual number of bytes that were declared when the AssetFileDescriptor was constructed. Will be [UNKNOWN_LENGTH](https://developer.android.com/reference/kotlin/android/content/res/AssetFileDescriptor#UNKNOWN_LENGTH:kotlin.Long) if the length was not declared, meaning data should be read to the end of the file. 
**See Also**

- <https://developer.android.com/reference/kotlin/android/content/res/AssetFileDescriptor#getDeclaredLength()> 

### getExtras

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getExtras(): Bundle!
```

Returns any additional details that can be used to interpret the underlying file descriptor. May be null. 

### getFileDescriptor

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getFileDescriptor(): FileDescriptor!
```

Returns the FileDescriptor that can be used to read the data in the file. 

### getLength

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getLength(): Long
```

Returns the total number of bytes of this asset entry's data. May be [UNKNOWN_LENGTH](https://developer.android.com/reference/kotlin/android/content/res/AssetFileDescriptor#UNKNOWN_LENGTH:kotlin.Long) if the asset extends to the end of the file. If the AssetFileDescriptor was constructed with [UNKNOWN_LENGTH](https://developer.android.com/reference/kotlin/android/content/res/AssetFileDescriptor#UNKNOWN_LENGTH:kotlin.Long), this will use [ParcelFileDescriptor.getStatSize()](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#getStatSize())to find the total size of the file, returning that number if found or [UNKNOWN_LENGTH](https://developer.android.com/reference/kotlin/android/content/res/AssetFileDescriptor#UNKNOWN_LENGTH:kotlin.Long) if it could not be determined. 
**See Also**

- <https://developer.android.com/reference/kotlin/android/content/res/AssetFileDescriptor#getDeclaredLength()> 

### getParcelFileDescriptor

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getParcelFileDescriptor(): ParcelFileDescriptor!
```

The AssetFileDescriptor contains its own ParcelFileDescriptor, which in addition to the normal FileDescriptor object also allows you to close the descriptor when you are done with it. 

### getStartOffset

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getStartOffset(): Long
```

Returns the byte offset where this asset entry's data starts. 

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

### writeToParcel

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun writeToParcel(
    out: Parcel, 
    flags: Int
): Unit
```

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<AssetFileDescriptor!>
```
