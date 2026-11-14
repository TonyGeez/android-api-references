# ProxyFileDescriptorCallback

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ProxyFileDescriptorCallback

Kotlin| [Java](https://developer.android.com/reference/android/os/ProxyFileDescriptorCallback "View this page in Java") 
| --- | --- |

```
abstract class ProxyFileDescriptorCallback
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.os.ProxyFileDescriptorCallback](https://developer.android.com/reference/kotlin/android/os/ProxyFileDescriptorCallback#) |

Callback that handles file system requests from ProxyFileDescriptor. All callback methods except for onRelease should throw [android.system.ErrnoException](https://developer.android.com/reference/kotlin/android/system/ErrnoException.html#) with proper errno on errors. See [errno(3)](http://man7.org/linux/man-pages/man3/errno.3.html) and [android.system.OsConstants](https://developer.android.com/reference/kotlin/android/system/OsConstants.html#). Typical errnos are

- [android.system.OsConstants#EIO](https://developer.android.com/reference/kotlin/android/system/OsConstants.html#EIO:kotlin.Int) for general I/O issues
- [android.system.OsConstants#ENOENT](https://developer.android.com/reference/kotlin/android/system/OsConstants.html#ENOENT:kotlin.Int) when the file is not found
- [android.system.OsConstants#EBADF](https://developer.android.com/reference/kotlin/android/system/OsConstants.html#EBADF:kotlin.Int) if the file doesn't allow read/write operations based on how it was opened. (For example, trying to write a file that was opened read-only.)
- [android.system.OsConstants#ENOSPC](https://developer.android.com/reference/kotlin/android/system/OsConstants.html#ENOSPC:kotlin.Int) if you cannot handle a write operation to space/quota limitations.

<br />

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ProxyFileDescriptorCallback](https://developer.android.com/reference/kotlin/android/os/ProxyFileDescriptorCallback#ProxyFileDescriptorCallback())`()` <br /> |

| Public methods ||
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onFsync](https://developer.android.com/reference/kotlin/android/os/ProxyFileDescriptorCallback#onFsync())`()` Ensures all the written data are stored in permanent storage device. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [onGetSize](https://developer.android.com/reference/kotlin/android/os/ProxyFileDescriptorCallback#onGetSize())`()` Returns size of bytes provided by the file descriptor. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [onRead](https://developer.android.com/reference/kotlin/android/os/ProxyFileDescriptorCallback#onRead(kotlin.Long,%20kotlin.Int,%20kotlin.ByteArray))`(`offset:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `size:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `data:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Provides bytes read from file descriptor. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onRelease](https://developer.android.com/reference/kotlin/android/os/ProxyFileDescriptorCallback#onRelease())`()` Invoked after the file is closed. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [onWrite](https://developer.android.com/reference/kotlin/android/os/ProxyFileDescriptorCallback#onWrite(kotlin.Long,%20kotlin.Int,%20kotlin.ByteArray))`(`offset:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `size:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `data:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Handles bytes written to file descriptor. |

## Public constructors

### ProxyFileDescriptorCallback

```
ProxyFileDescriptorCallback()
```

## Public methods

### onFsync

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onFsync(): Unit
```

Ensures all the written data are stored in permanent storage device. For example, if it has data stored in on memory cache, it needs to flush data to storage device.

| Exceptions ||
|---------------------------------|-------------------------------------------------------|
| `android.system.ErrnoException` | ErrnoException containing E constants in OsConstants. |

### onGetSize

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onGetSize(): Long
```

Returns size of bytes provided by the file descriptor.

| Return ||
|------------------------------------------------------------------------------|----------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | Size of bytes. |

| Exceptions ||
|---------------------------------|-------------------------------------------------------|
| `android.system.ErrnoException` | ErrnoException containing E constants in OsConstants. |

### onRead

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onRead(
    offset: Long, 
    size: Int, 
    data: ByteArray!
): Int
```

Provides bytes read from file descriptor. It needs to return exact requested size of bytes unless it reaches file end.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `offset` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):Offset in bytes from the file head specifying where to read bytes. If a seek operation is conducted on the file descriptor, then a read operation is requested, the offset refrects the proper position of requested bytes. |
| `size` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Size for read bytes. |
| `data` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:Byte array to store read bytes. |
| --- | --- |

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Size of bytes returned by the function. |

| Exceptions ||
|---------------------------------|-------------------------------------------------------|
| `android.system.ErrnoException` | ErrnoException containing E constants in OsConstants. |

### onRelease

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onRelease(): Unit
```

Invoked after the file is closed. 

### onWrite

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onWrite(
    offset: Long, 
    size: Int, 
    data: ByteArray!
): Int
```

Handles bytes written to file descriptor.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `offset` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):Offset in bytes from the file head specifying where to write bytes. If a seek operation is conducted on the file descriptor, then a write operation is requested, the offset refrects the proper position of requested bytes. |
| `size` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Size for write bytes. |
| `data` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:Byte array to be written to somewhere. |
| --- | --- |

| Return ||
|----------------------------------------------------------------------------|------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Size of bytes processed by the function. |

| Exceptions ||
|---------------------------------|-------------------------------------------------------|
| `android.system.ErrnoException` | ErrnoException containing E constants in OsConstants. |
