# MemoryFile

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MemoryFile

Kotlin| [Java](https://developer.android.com/reference/android/os/MemoryFile "View this page in Java") 

```
open class MemoryFile
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.os.MemoryFile](https://developer.android.com/reference/kotlin/android/os/MemoryFile#) |

MemoryFile is a wrapper for [SharedMemory](https://developer.android.com/reference/kotlin/android/os/SharedMemory) which can optionally be set to purgeable. Applications should generally prefer to use [SharedMemory](https://developer.android.com/reference/kotlin/android/os/SharedMemory) which offers more flexible access \& control over the shared memory region than MemoryFile does. Purgeable files may have their contents reclaimed by the kernel in low memory conditions (only if allowPurging is set to true). After a file is purged, attempts to read or write the file will cause an IOException to be thrown.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [MemoryFile](https://developer.android.com/reference/kotlin/android/os/MemoryFile#MemoryFile(kotlin.String,%20kotlin.Int))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `length:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Allocates a new ashmem region. |

| Public methods ||
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [allowPurging](https://developer.android.com/reference/kotlin/android/os/MemoryFile#allowPurging(kotlin.Boolean))`(`allowPurging:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Enables or disables purging of the memory file. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](https://developer.android.com/reference/kotlin/android/os/MemoryFile#close())`()` Closes the memory file. |
| open [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)! | [getInputStream](https://developer.android.com/reference/kotlin/android/os/MemoryFile#getInputStream())`()` Creates a new InputStream for reading from the memory file. |
| open [OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream.html#)! | [getOutputStream](https://developer.android.com/reference/kotlin/android/os/MemoryFile#getOutputStream())`()` Creates a new OutputStream for writing to the memory file. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isPurgingAllowed](https://developer.android.com/reference/kotlin/android/os/MemoryFile#isPurgingAllowed())`()` Is memory file purging enabled? |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [length](https://developer.android.com/reference/kotlin/android/os/MemoryFile#length())`()` Returns the length of the memory file. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [readBytes](https://developer.android.com/reference/kotlin/android/os/MemoryFile#readBytes(kotlin.ByteArray,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`buffer:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `srcOffset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `destOffset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `count:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Reads bytes from the memory file. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeBytes](https://developer.android.com/reference/kotlin/android/os/MemoryFile#writeBytes(kotlin.ByteArray,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`buffer:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `srcOffset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `destOffset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `count:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Write bytes to the memory file. |

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

**Deprecated:** *Purgable is considered generally fragile and hard to use safely. Applications are recommend to instead use [android.content.ComponentCallbacks2#onTrimMemory(int)](https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#onTrimMemory(kotlin.Int))to react to memory events and release shared memory regions as appropriate.*

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
| [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)! | InputStream |

### getOutputStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getOutputStream(): OutputStream!
```

Creates a new OutputStream for writing to the memory file.

| Return ||
|--------------------------------------------------------------------------------------------|--------------|
| [OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream.html#)! | OutputStream |

### isPurgingAllowed

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 27](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isPurgingAllowed(): Boolean
```

**Deprecated:** *Purgable is considered generally fragile and hard to use safely. Applications are recommend to instead use [android.content.ComponentCallbacks2#onTrimMemory(int)](https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#onTrimMemory(kotlin.Int))to react to memory events and release shared memory regions as appropriate.*

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
| `count` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):number of bytes to write. |

| Exceptions ||
|-----------------------|----------------------------------------------------|
| `java.io.IOException` | if the memory file has been purged or deactivated. |
