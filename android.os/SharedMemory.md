# SharedMemory

Added in [API level 27](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SharedMemory

Kotlin| [Java](SharedMemory.md) 
| --- | --- |

```
class SharedMemory : Closeable, Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.os.SharedMemory](SharedMemory.md) |

SharedMemory enables the creation, mapping, and protection control over anonymous shared memory.

## Summary

| Inherited constants ||
|---|---|
| From class [Parcelable](Parcelable.md) |----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](Parcelable.md) <br /> Descriptor bit used with [describeContents()](Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](Parcelable.md) <br /> Flag for use with [writeToParcel](Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](SharedMemory.md))`()` Close the backing [FileDescriptor](../java.io/FileDescriptor.md) of this SharedMemory instance. |
| static [SharedMemory](SharedMemory.md) | [create](SharedMemory.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `size:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates an anonymous SharedMemory instance with the provided debug name and size. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](SharedMemory.md))`()` <br /> |
| --- | --- |
| static [SharedMemory](SharedMemory.md) | [fromFileDescriptor](SharedMemory.md))`(`fd:` ` [ParcelFileDescriptor](ParcelFileDescriptor.md)`)` Creates an instance from existing shared memory passed as [ParcelFileDescriptor](ParcelFileDescriptor.md). |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSize](SharedMemory.md))`()` <br /> |
| [ByteBuffer](../java.nio/ByteBuffer.md) | [map](SharedMemory.md))`(`prot:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `length:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates an mmap of the SharedMemory with the specified prot, offset, and length. |
| --- | --- |
| [ByteBuffer](../java.nio/ByteBuffer.md) | [mapReadOnly](SharedMemory.md))`()` Creates a read-only mapping of the entire shared memory region. |
| [ByteBuffer](../java.nio/ByteBuffer.md) | [mapReadWrite](SharedMemory.md))`()` Creates a read/write mapping of the entire shared memory region. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [setProtect](SharedMemory.md))`(`prot:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the protection on the shared memory to the combination specified in prot, which is either a bitwise-or'd combination of [android.system.OsConstants#PROT_READ](../android.system/OsConstants.md), [android.system.OsConstants#PROT_WRITE](../android.system/OsConstants.md), [android.system.OsConstants#PROT_EXEC](../android.system/OsConstants.md) from [android.system.OsConstants](../android.system/OsConstants.md), or [android.system.OsConstants#PROT_NONE](../android.system/OsConstants.md), to remove all further access. |
| --- | --- |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unmap](SharedMemory.md))`(`buffer:` ` [ByteBuffer](../java.nio/ByteBuffer.md)`)` Unmaps a buffer previously returned by [map(int,int,int)](SharedMemory.md)). |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](SharedMemory.md))`(`dest:` ` [Parcel](Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |

| Properties ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [SharedMemory](SharedMemory.md)!\> | [CREATOR](SharedMemory.md) <br /> |

## Public methods

### close

Added in [API level 27](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun close(): Unit
```

Close the backing [FileDescriptor](../java.io/FileDescriptor.md) of this SharedMemory instance. Note that all open mappings of the shared memory will remain valid and may continue to be used. The shared memory will not be freed until all file descriptor handles are closed and all memory mappings are unmapped.

| Exceptions ||
|-----------------------|-----------------------------------|
| `java.lang.Exception` | if this resource cannot be closed |
| `java.io.IOException` | if an I/O error occurs |

### create

Added in [API level 27](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun create(
    name: String?, 
    size: Int
): SharedMemory
```

Creates an anonymous SharedMemory instance with the provided debug name and size. The name is only used for debugging purposes and can help identify what the shared memory is used for when inspecting memory maps for the processes that have mapped this SharedMemory instance.

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:The debug name to use for this SharedMemory instance. This can be null, however a debug name is recommended to help identify memory usage when using tools such as lsof or examining /proc/\[pid\]/maps |
| `size` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The size of the shared memory to create. Must be greater than 0. |

| Return ||
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [SharedMemory](SharedMemory.md) | A SharedMemory instance of the requested size This value cannot be`null`. |

| Exceptions ||
|---------------------------------|------------------------------------|
| `android.system.ErrnoException` | if the requested allocation fails. |

### describeContents

Added in [API level 27](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](Parcelable.md) |

### fromFileDescriptor

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun fromFileDescriptor(fd: ParcelFileDescriptor): SharedMemory
```

Creates an instance from existing shared memory passed as [ParcelFileDescriptor](ParcelFileDescriptor.md).

The`fd`should be a shared memory created from`SharedMemory or ASharedMemory`. This can be useful when shared memory is passed as file descriptor through JNI or binder service implemented in cpp.

Note that newly created`SharedMemory`takes ownership of passed`fd`and the original`fd`becomes detached (Check [ParcelFileDescriptor.detachFd()](ParcelFileDescriptor.md))). If the caller wants to use the file descriptor after the call, the caller should duplicate the file descriptor (Check [ParcelFileDescriptor.dup()](ParcelFileDescriptor.md))) and pass the duped version instead.

| Parameters ||
|------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `fd` | [ParcelFileDescriptor](ParcelFileDescriptor.md):File descriptor of shared memory passed as [ParcelFileDescriptor](ParcelFileDescriptor.md). This value cannot be`null`. |

| Return ||
|-----------------------------------------------------------------------------------------|-----------------------------|
| [SharedMemory](SharedMemory.md) | This value cannot be`null`. |

### getSize

Added in [API level 27](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSize(): Int
```

| Return ||
|----------------------------------------------------------------------------|--------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The size of the SharedMemory region. |

### map

Added in [API level 27](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun map(
    prot: Int, 
    offset: Int, 
    length: Int
): ByteBuffer
```

Creates an mmap of the SharedMemory with the specified prot, offset, and length. This will always produce a new ByteBuffer window to the backing shared memory region. Every call to map() may be paired with a call to [unmap(java.nio.ByteBuffer)](SharedMemory.md))when the ByteBuffer returned by map() is no longer needed.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `prot` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):A bitwise-or'd combination of PROT_READ, PROT_WRITE, PROT_EXEC, or PROT_NONE. |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The offset into the shared memory to begin mapping. Must be \>= 0 and less than getSize(). |
| `length` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The length of the region to map. Must be \> 0 and offset + length must not exceed getSize(). |
| --- | --- |

| Return ||
|----------------------------------------------------------------------------------------|---------------------------------------------------|
| [ByteBuffer](../java.nio/ByteBuffer.md) | A ByteBuffer mapping. This value cannot be`null`. |

| Exceptions ||
|---------------------------------|--------------------------|
| `android.system.ErrnoException` | if the mmap call failed. |

### mapReadOnly

Added in [API level 27](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun mapReadOnly(): ByteBuffer
```

Creates a read-only mapping of the entire shared memory region. This requires the the protection level of the shared memory is at least PROT_READ or the map will fail. Use [map(int,int,int)](SharedMemory.md))to have more control over the mapping if desired. This is equivalent to map(OsConstants.PROT_READ, 0, getSize())

| Return ||
|----------------------------------------------------------------------------------------|--------------------------------------------------|
| [ByteBuffer](../java.nio/ByteBuffer.md) | A ByteBuffer mapping This value cannot be`null`. |

| Exceptions ||
|---------------------------------|--------------------------|
| `android.system.ErrnoException` | if the mmap call failed. |

### mapReadWrite

Added in [API level 27](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun mapReadWrite(): ByteBuffer
```

Creates a read/write mapping of the entire shared memory region. This requires the the protection level of the shared memory is at least PROT_READ|PROT_WRITE or the map will fail. Use [map(int,int,int)](SharedMemory.md))to have more control over the mapping if desired. This is equivalent to map(OsConstants.PROT_READ | OsConstants.PROT_WRITE, 0, getSize())
| --- | --- | --- |

| Return ||
|----------------------------------------------------------------------------------------|--------------------------------------------------|
| [ByteBuffer](../java.nio/ByteBuffer.md) | A ByteBuffer mapping This value cannot be`null`. |

| Exceptions ||
|---------------------------------|--------------------------|
| `android.system.ErrnoException` | if the mmap call failed. |

### setProtect

Added in [API level 27](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setProtect(prot: Int): Boolean
```

Sets the protection on the shared memory to the combination specified in prot, which is either a bitwise-or'd combination of [android.system.OsConstants#PROT_READ](../android.system/OsConstants.md), [android.system.OsConstants#PROT_WRITE](../android.system/OsConstants.md), [android.system.OsConstants#PROT_EXEC](../android.system/OsConstants.md) from [android.system.OsConstants](../android.system/OsConstants.md), or [android.system.OsConstants#PROT_NONE](../android.system/OsConstants.md), to remove all further access. Note that protection can only ever be removed, not added. By default shared memory is created with protection set to PROT_READ | PROT_WRITE | PROT_EXEC. The protection passed here also only applies to any mappings created after calling this method. Existing mmaps of the shared memory retain whatever protection they had when they were created. A common usage of this is to share a read-only copy of the data with something else. To do that first create the read/write mapping with PROT_READ | PROT_WRITE, then call setProtect(PROT_READ) to remove write capability, then send the SharedMemory to another process. That process will only be able to mmap with PROT_READ.
| --- | --- | --- | --- |

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `prot` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Any bitwise-or'ed combination of [android.system.OsConstants#PROT_READ](../android.system/OsConstants.md), [android.system.OsConstants#PROT_WRITE](../android.system/OsConstants.md), and [android.system.OsConstants#PROT_EXEC](../android.system/OsConstants.md); or [android.system.OsConstants#PROT_NONE](../android.system/OsConstants.md) |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | Whether or not the requested protection was applied. Returns true on success, false if the requested protection was broader than the existing protection. |

### unmap

Added in [API level 27](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun unmap(buffer: ByteBuffer): Unit
```

Unmaps a buffer previously returned by [map(int,int,int)](SharedMemory.md)). This will immediately release the backing memory of the ByteBuffer, invalidating all references to it. Only call this method if there are no duplicates of the ByteBuffer in use and don't access the ByteBuffer after calling this method.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------|
| `buffer` | [ByteBuffer](../java.nio/ByteBuffer.md):The buffer to unmap This value cannot be`null`. |

### writeToParcel

Added in [API level 27](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

Flatten this object in to a Parcel.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Parcel](Parcel.md):This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](Parcelable.md). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 27](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<SharedMemory!>
```
