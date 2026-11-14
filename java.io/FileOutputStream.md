# FileOutputStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# FileOutputStream

```
open class FileOutputStream : OutputStream
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [java.io.OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream) ||
| | ↳ | [java.io.FileOutputStream](https://developer.android.com/reference/kotlin/java/io/FileOutputStream#) |

| Known Direct Subclasses [ParcelFileDescriptor.AutoCloseOutputStream](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.AutoCloseOutputStream.html#) |----------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------| | [ParcelFileDescriptor.AutoCloseOutputStream](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.AutoCloseOutputStream.html#) | An OutputStream you can create on a ParcelFileDescriptor, which will take care of calling android. | |
| --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [AssetFileDescriptor.AutoCloseOutputStream](https://developer.android.com/reference/kotlin/android/content/res/AssetFileDescriptor.AutoCloseOutputStream.html#) |-----------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------| | [AssetFileDescriptor.AutoCloseOutputStream](https://developer.android.com/reference/kotlin/android/content/res/AssetFileDescriptor.AutoCloseOutputStream.html#) | An OutputStream you can create on a ParcelFileDescriptor, which will take care of calling android. | |
| --- | --- | --- | --- | --- | --- | --- |

A file output stream is an output stream for writing data to a`File`or to a`FileDescriptor`. Whether or not a file is available or may be created depends upon the underlying platform. Some platforms, in particular, allow a file to be opened for writing by only one`FileOutputStream`(or other file-writing object) at a time. In such situations the constructors in this class will fail if the file involved is already open.

`FileOutputStream`is meant for writing streams of raw bytes such as image data. For writing streams of characters, consider using`FileWriter`.

## Summary

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [FileOutputStream](https://developer.android.com/reference/kotlin/java/io/FileOutputStream#FileOutputStream(java.io.File))`(`file:` ` [File](https://developer.android.com/reference/kotlin/java/io/File)!`)` Creates a file output stream to write to the file represented by the specified`File`object. |
| [FileOutputStream](https://developer.android.com/reference/kotlin/java/io/FileOutputStream#FileOutputStream(java.io.File,%20kotlin.Boolean))`(`file:` ` [File](https://developer.android.com/reference/kotlin/java/io/File)!`, `append:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Creates a file output stream to write to the file represented by the specified`File`object. |
| [FileOutputStream](https://developer.android.com/reference/kotlin/java/io/FileOutputStream#FileOutputStream(java.io.FileDescriptor))`(`fdObj:` ` [FileDescriptor](https://developer.android.com/reference/kotlin/java/io/FileDescriptor)!`)` Creates a file output stream to write to the specified file descriptor, which represents an existing connection to an actual file in the file system. |
| [FileOutputStream](https://developer.android.com/reference/kotlin/java/io/FileOutputStream#FileOutputStream(kotlin.String))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Creates a file output stream to write to the file with the specified name. |
| [FileOutputStream](https://developer.android.com/reference/kotlin/java/io/FileOutputStream#FileOutputStream(kotlin.String,%20kotlin.Boolean))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `append:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Creates a file output stream to write to the file with the specified name. |

| Public methods ||
|--------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](https://developer.android.com/reference/kotlin/java/io/FileOutputStream#close())`()` Closes this file output stream and releases any system resources associated with this stream. |
| open [FileChannel](https://developer.android.com/reference/kotlin/java/nio/channels/FileChannel.html#)! | [getChannel](https://developer.android.com/reference/kotlin/java/io/FileOutputStream#getChannel())`()` Returns the unique [FileChannel](https://developer.android.com/reference/kotlin/java/nio/channels/FileChannel.html#) object associated with this file output stream. |
| [FileDescriptor](https://developer.android.com/reference/kotlin/java/io/FileDescriptor)! | [getFD](https://developer.android.com/reference/kotlin/java/io/FileOutputStream#getFD())`()` Returns the file descriptor associated with this stream. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [write](https://developer.android.com/reference/kotlin/java/io/FileOutputStream#write(kotlin.ByteArray))`(`b:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Writes`b.length`bytes from the specified byte array to this file output stream. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [write](https://developer.android.com/reference/kotlin/java/io/FileOutputStream#write(kotlin.ByteArray,%20kotlin.Int,%20kotlin.Int))`(`b:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `off:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `len:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Writes`len`bytes from the specified byte array starting at offset`off`to this file output stream. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [write](https://developer.android.com/reference/kotlin/java/io/FileOutputStream#write(kotlin.Int))`(`b:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Writes the specified byte to this file output stream. |
| --- | --- |

| Protected methods ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finalize](https://developer.android.com/reference/kotlin/java/io/FileOutputStream#finalize())`()` Cleans up the connection to the file, and ensures that the`close`method of this file output stream is called when there are no more references to this stream. |

| Inherited functions ||
|---|---|
| From class [OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream) |--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [flush](https://developer.android.com/reference/kotlin/java/io/OutputStream#flush())`()` <br /> Flushes this output stream and forces any buffered output bytes to be written out. The general contract of`flush`is that calling it is an indication that, if any bytes previously written have been buffered by the implementation of the output stream, such bytes should immediately be written to their intended destination. If the intended destination of this stream is an abstraction provided by the underlying operating system, for example a file, then flushing the stream guarantees only that bytes previously written to the stream are passed to the operating system for writing; it does not guarantee that they are actually written to a physical device such as a disk drive. The`flush`method of`OutputStream`does nothing. <br /> | | [OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream)! | [nullOutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream#nullOutputStream())`()` <br /> Returns a new`OutputStream`which discards all bytes. The returned stream is initially open. The stream is closed by calling the`close()`method. Subsequent calls to`close()`have no effect. While the stream is open, the`write(int)`,`write(byte[])`, and`write(byte[], int, int)`methods do nothing. After the stream has been closed, these methods all throw`IOException`. The`flush()`method does nothing. <br /> | ||

## Public constructors

### FileOutputStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
FileOutputStream(file: File!)
```

Creates a file output stream to write to the file represented by the specified`File`object. A new`FileDescriptor`object is created to represent this file connection.

First, if there is a security manager, its`checkWrite`method is called with the path represented by the`file`argument as its argument.

If the file exists but is a directory rather than a regular file, does not exist but cannot be created, or cannot be opened for any other reason then a`FileNotFoundException`is thrown.

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------|
| `file` | [File](https://developer.android.com/reference/kotlin/java/io/File)!:the file to be opened for writing. |

| Exceptions ||
|---------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.io.FileNotFoundException` | if the file exists but is a directory rather than a regular file, does not exist but cannot be created, or cannot be opened for any other reason |
| `java.lang.SecurityException` | if a security manager exists and its`checkWrite`method denies write access to the file. |

**See Also**

- [java.io.File#getPath()](https://developer.android.com/reference/kotlin/java/io/File#getPath())
- [java.lang.SecurityException](https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#)
- [java.lang.SecurityManager#checkWrite(java.lang.String)](https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#checkWrite(kotlin.String)) 

### FileOutputStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
FileOutputStream(
    file: File!, 
    append: Boolean)
```

Creates a file output stream to write to the file represented by the specified`File`object. If the second argument is`true`, then bytes will be written to the end of the file rather than the beginning. A new`FileDescriptor`object is created to represent this file connection.

First, if there is a security manager, its`checkWrite`method is called with the path represented by the`file`argument as its argument.

If the file exists but is a directory rather than a regular file, does not exist but cannot be created, or cannot be opened for any other reason then a`FileNotFoundException`is thrown.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `file` | [File](https://developer.android.com/reference/kotlin/java/io/File)!:the file to be opened for writing. |
| `append` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):if`true`, then bytes will be written to the end of the file rather than the beginning |

| Exceptions ||
|---------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.io.FileNotFoundException` | if the file exists but is a directory rather than a regular file, does not exist but cannot be created, or cannot be opened for any other reason |
| `java.lang.SecurityException` | if a security manager exists and its`checkWrite`method denies write access to the file. |

**See Also**

- [java.io.File#getPath()](https://developer.android.com/reference/kotlin/java/io/File#getPath())
- [java.lang.SecurityException](https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#)
- [java.lang.SecurityManager#checkWrite(java.lang.String)](https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#checkWrite(kotlin.String)) 

### FileOutputStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
FileOutputStream(fdObj: FileDescriptor!)
```

Creates a file output stream to write to the specified file descriptor, which represents an existing connection to an actual file in the file system.

First, if there is a security manager, its`checkWrite`method is called with the file descriptor`fdObj`argument as its argument.

If`fdObj`is null then a`NullPointerException`is thrown.

This constructor does not throw an exception if`fdObj`is [invalid](https://developer.android.com/reference/kotlin/java/io/FileDescriptor#valid()). However, if the methods are invoked on the resulting stream to attempt I/O on the stream, an`IOException`is thrown.

Android-specific warning: #close() method doesn't close the`fdObj`provided, because this object doesn't own the file descriptor, but the caller does. The caller can call [android.system.Os#close(FileDescriptor)](https://developer.android.com/reference/kotlin/android/system/Os.html#close(java.io.FileDescriptor))to close the fd.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------|
| `fdObj` | [FileDescriptor](https://developer.android.com/reference/kotlin/java/io/FileDescriptor)!:the file descriptor to be opened for writing |

| Exceptions ||
|-------------------------------|---------------------------------------------------------------------------------------------------|
| `java.lang.SecurityException` | if a security manager exists and its`checkWrite`method denies write access to the file descriptor |

**See Also**

- [java.lang.SecurityManager#checkWrite(java.io.FileDescriptor)](https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#checkWrite(java.io.FileDescriptor)) 

### FileOutputStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
FileOutputStream(name: String!)
```

Creates a file output stream to write to the file with the specified name. A new`FileDescriptor`object is created to represent this file connection.

First, if there is a security manager, its`checkWrite`method is called with`name`as its argument.

If the file exists but is a directory rather than a regular file, does not exist but cannot be created, or cannot be opened for any other reason then a`FileNotFoundException`is thrown.

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the system-dependent filename |

| Exceptions ||
|---------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.io.FileNotFoundException` | if the file exists but is a directory rather than a regular file, does not exist but cannot be created, or cannot be opened for any other reason |
| `java.lang.SecurityException` | if a security manager exists and its`checkWrite`method denies write access to the file. |

**See Also**

- [java.lang.SecurityManager#checkWrite(java.lang.String)](https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#checkWrite(kotlin.String)) 

### FileOutputStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
FileOutputStream(
    name: String!, 
    append: Boolean)
```

Creates a file output stream to write to the file with the specified name. If the second argument is`true`, then bytes will be written to the end of the file rather than the beginning. A new`FileDescriptor`object is created to represent this file connection.

First, if there is a security manager, its`checkWrite`method is called with`name`as its argument.

If the file exists but is a directory rather than a regular file, does not exist but cannot be created, or cannot be opened for any other reason then a`FileNotFoundException`is thrown.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the system-dependent file name |
| `append` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):if`true`, then bytes will be written to the end of the file rather than the beginning |

| Exceptions ||
|---------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.io.FileNotFoundException` | if the file exists but is a directory rather than a regular file, does not exist but cannot be created, or cannot be opened for any other reason. |
| `java.lang.SecurityException` | if a security manager exists and its`checkWrite`method denies write access to the file. |

**See Also**

- [java.lang.SecurityManager#checkWrite(java.lang.String)](https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#checkWrite(kotlin.String))

## Public methods

### close

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun close(): Unit
```

Closes this file output stream and releases any system resources associated with this stream. This file output stream may no longer be used for writing bytes.

If this stream has an associated channel then the channel is closed as well.

| Exceptions ||
|-----------------------|-----------------------------------|
| `java.lang.Exception` | if this resource cannot be closed |
| `java.io.IOException` | if an I/O error occurs. |

### getChannel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getChannel(): FileChannel!
```

Returns the unique [FileChannel](https://developer.android.com/reference/kotlin/java/nio/channels/FileChannel.html#) object associated with this file output stream.

The initial [position](https://developer.android.com/reference/kotlin/java/nio/channels/FileChannel.html#position())of the returned channel will be equal to the number of bytes written to the file so far unless this stream is in append mode, in which case it will be equal to the size of the file. Writing bytes to this stream will increment the channel's position accordingly. Changing the channel's position, either explicitly or by writing, will change this stream's file position.

| Return ||
|----------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| [FileChannel](https://developer.android.com/reference/kotlin/java/nio/channels/FileChannel.html#)! | the file channel associated with this file output stream |

### getFD

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getFD(): FileDescriptor!
```

Returns the file descriptor associated with this stream.

| Return ||
|------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [FileDescriptor](https://developer.android.com/reference/kotlin/java/io/FileDescriptor)! | the`FileDescriptor`object that represents the connection to the file in the file system being used by this`FileOutputStream`object. |

| Exceptions ||
|-----------------------|-------------------------|
| `java.io.IOException` | if an I/O error occurs. |

**See Also**

- [java.io.FileDescriptor](https://developer.android.com/reference/kotlin/java/io/FileDescriptor) 

### write

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun write(b: ByteArray!): Unit
```

Writes`b.length`bytes from the specified byte array to this file output stream.

| Parameters ||
|-----|----------------------------------------------------------------------------------------------------|
| `b` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the data. |

| Exceptions ||
|-----------------------|-------------------------|
| `java.io.IOException` | if an I/O error occurs. |

### write

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun write(
    b: ByteArray!, 
    off: Int, 
    len: Int
): Unit
```

Writes`len`bytes from the specified byte array starting at offset`off`to this file output stream.

| Parameters ||
|-------|----------------------------------------------------------------------------------------------------------|
| `b` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the data. |
| `off` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the start offset in the data. |
| `len` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of bytes to write. |
| --- | --- |

| Exceptions ||
|-----------------------|-------------------------|
| `java.io.IOException` | if an I/O error occurs. |

### write

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun write(b: Int): Unit
```

Writes the specified byte to this file output stream. Implements the`write`method of`OutputStream`.

| Parameters ||
|-----|----------------------------------------------------------------------------------------------------|
| `b` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the byte to be written. |

| Exceptions ||
|-----------------------|-------------------------|
| `java.io.IOException` | if an I/O error occurs. |

## Protected methods

### finalize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun finalize(): Unit
```

Cleans up the connection to the file, and ensures that the`close`method of this file output stream is called when there are no more references to this stream.

| Exceptions ||
|-----------------------|-------------------------------------|
| `java.lang.Throwable` | the`Exception`raised by this method |
| `java.io.IOException` | if an I/O error occurs. |

**See Also**
