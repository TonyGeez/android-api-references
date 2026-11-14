# MemoryFile

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MemoryFile

Kotlin| [Java](MemoryFile.md) 
| --- | --- |

```
open class MemoryFile
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.os.MemoryFile](MemoryFile.md) |

MemoryFile is a wrapper for [SharedMemory](SharedMemory.md) which can optionally be set to purgeable. Applications should generally prefer to use [SharedMemory](SharedMemory.md) which offers more flexible access \& control over the shared memory region than MemoryFile does. Purgeable files may have their contents reclaimed by the kernel in low memory conditions (only if allowPurging is set to true). After a file is purged, attempts to read or write the file will cause an IOException to be thrown.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [MemoryFile](MemoryFile.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `length:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Allocates a new ashmem region. |

| Public methods ||
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [allowPurging](MemoryFile.md))`(`allowPurging:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Enables or disables purging of the memory file. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](MemoryFile.md))`()` Closes the memory file. |
| open [InputStream](../java.io/InputStream.md)! | [getInputStream](MemoryFile.md))`()` Creates a new InputStream for reading from the memory file. |
| --- | --- |
| open [OutputStream](../java.io/OutputStream.md)! | [getOutputStream](MemoryFile.md))`()` Creates a new OutputStream for writing to the memory file. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isPurgingAllowed](MemoryFile.md))`()` Is memory file purging enabled? |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [length](MemoryFile.md))`()` Returns the length of the memory file. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [readBytes](MemoryFile.md))`(`buffer:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `srcOffset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `destOffset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `count:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Reads bytes from the memory file. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeBytes](MemoryFile.md))`(`buffer:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `srcOffset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `destOffset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `count:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Write bytes to the memory file. |

## Public constructors

### MemoryFile

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
MemoryFile(
    name: String!, 
    length: Int)
```

Allocates a new ashmem region. The region is initially not purgable.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:optional name for the file (can be null). |
| `length` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):of the memory file in bytes, must be positive. |

| Exceptions ||
|-----------------------|------------------------------------------|
| `java.io.IOException` | if the memory file could not be created. |

## Public methods

### allowPurging

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 27](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun allowPurging(allowPurging: Boolean): Boolean
```

**Deprecated:** *Purgable is considered generally fragile and hard to use safely. Applications are recommend to instead use [android.content.ComponentCallbacks2#onTrimMemory(int)](../android.content/ComponentCallbacks2.md))to react to memory events and release shared memory regions as appropriate.*

Enables or disables purging of the memory file.

| Parameters ||
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `allowPurging` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):true if the operating system can purge the contents of the file in low memory situations |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | previous value of allowPurging |

### close

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun close(): Unit
```

Closes the memory file. If there are no other open references to the memory file, it will be deleted. 

### getInputStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getInputStream(): InputStream!
```

Creates a new InputStream for reading from the memory file.

| Return ||
|------------------------------------------------------------------------------------------|-------------|
| [InputStream](../java.io/InputStream.md)! | InputStream |

### getOutputStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getOutputStream(): OutputStream!
```

Creates a new OutputStream for writing to the memory file.

| Return ||
|--------------------------------------------------------------------------------------------|--------------|
| [OutputStream](../java.io/OutputStream.md)! | OutputStream |

### isPurgingAllowed

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 27](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isPurgingAllowed(): Boolean
```

**Deprecated:** *Purgable is considered generally fragile and hard to use safely. Applications are recommend to instead use [android.content.ComponentCallbacks2#onTrimMemory(int)](../android.content/ComponentCallbacks2.md))to react to memory events and release shared memory regions as appropriate.*

Is memory file purging enabled?

| Return ||
|------------------------------------------------------------------------------------|---------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the file may be purged. |

### length

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun length(): Int
```

Returns the length of the memory file.

| Return ||
|----------------------------------------------------------------------------|--------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | file length. |

### readBytes

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun readBytes(
    buffer: ByteArray!, 
    srcOffset: Int, 
    destOffset: Int, 
    count: Int
): Int
```

Reads bytes from the memory file. Will throw an IOException if the file has been purged.

| Parameters ||
|--------------|----------------------------------------------------------------------------------------------------------------------------|
| `buffer` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:byte array to read bytes into. |
| `srcOffset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):offset into the memory file to read from. |
| `destOffset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):offset into the byte array buffer to read into. |
| --- | --- |
| `count` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):number of bytes to read. |

| Return ||
|----------------------------------------------------------------------------|-----------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | number of bytes read. |

| Exceptions ||
|-----------------------|----------------------------------------------------|
| `java.io.IOException` | if the memory file has been purged or deactivated. |

### writeBytes

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun writeBytes(
    buffer: ByteArray!, 
    srcOffset: Int, 
    destOffset: Int, 
    count: Int
): Unit
```

Write bytes to the memory file. Will throw an IOException if the file has been purged.

| Parameters ||
|--------------|-----------------------------------------------------------------------------------------------------------------------------|
| `buffer` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:byte array to write bytes from. |
| `srcOffset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):offset into the byte array buffer to write from. |
| `destOffset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):offset into the memory file to write to. |
| --- | --- |
| `count` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):number of bytes to write. |

| Exceptions ||
|-----------------------|----------------------------------------------------|
| `java.io.IOException` | if the memory file has been purged or deactivated. |
