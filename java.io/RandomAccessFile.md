Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RandomAccessFile

```
open class RandomAccessFile : Closeable, DataInput, DataOutput
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [java.io.RandomAccessFile](https://developer.android.com/reference/kotlin/java/io/RandomAccessFile#) |

Instances of this class support both reading and writing to a random access file. A random access file behaves like a large array of bytes stored in the file system. There is a kind of cursor, or index into the implied array, called the *file pointer* ; input operations read bytes starting at the file pointer and advance the file pointer past the bytes read. If the random access file is created in read/write mode, then output operations are also available; output operations write bytes starting at the file pointer and advance the file pointer past the bytes written. Output operations that write past the current end of the implied array cause the array to be extended. The file pointer can be read by the `getFilePointer` method and set by the `seek` method.

It is generally true of all the reading routines in this class that if end-of-file is reached before the desired number of bytes has been read, an `EOFException` (which is a kind of `IOException`) is thrown. If any byte cannot be read for any reason other than end-of-file, an `IOException` other than `EOFException` is thrown. In particular, an `IOException` may be thrown if the stream has been closed.

## Summary

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/io/RandomAccessFile#RandomAccessFile(java.io.File,%20kotlin.String)(file: https://developer.android.com/reference/kotlin/java/io/File!, mode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Creates a random access file stream to read from, and optionally to write to, the file specified by the `https://developer.android.com/reference/kotlin/java/io/File` argument. |
| `https://developer.android.com/reference/kotlin/java/io/RandomAccessFile#RandomAccessFile(kotlin.String,%20kotlin.String)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, mode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Creates a random access file stream to read from, and optionally to write to, a file with the specified name. |

| Public methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/io/RandomAccessFile#close()()` Closes this random access file stream and releases any system resources associated with the stream. |
| [FileChannel](https://developer.android.com/reference/kotlin/java/nio/channels/FileChannel.html#)! | `https://developer.android.com/reference/kotlin/java/io/RandomAccessFile#getChannel()()` Returns the unique `https://developer.android.com/reference/kotlin/java/nio/channels/FileChannel.html#` object associated with this file. |
| [FileDescriptor](https://developer.android.com/reference/kotlin/java/io/FileDescriptor)! | `https://developer.android.com/reference/kotlin/java/io/RandomAccessFile#getFD()()` Returns the opaque file descriptor object associated with this stream. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/java/io/RandomAccessFile#getFilePointer()()` Returns the current offset in this file. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/java/io/RandomAccessFile#length()()` Returns the length of this file. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/io/RandomAccessFile#read()()` Reads a byte of data from this file. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/io/RandomAccessFile#read(kotlin.ByteArray)(b: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html!)` Reads up to `b.length` bytes of data from this file into an array of bytes. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/io/RandomAccessFile#read(kotlin.ByteArray,%20kotlin.Int,%20kotlin.Int)(b: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html!, off: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, len: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Reads up to `len` bytes of data from this file into an array of bytes. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/io/RandomAccessFile#readBoolean()()` Reads a `boolean` from this file. |
| [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | `https://developer.android.com/reference/kotlin/java/io/RandomAccessFile#readByte()()` Reads a signed eight-bit value from this file. |
| [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | `https://developer.android.com/reference/kotlin/java/io/RandomAccessFile#readChar()()` Reads a character from this file. |
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | `https://developer.android.com/reference/kotlin/java/io/RandomAccessFile#readDouble()()` Reads a `double` from this file. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/java/io/RandomAccessFile#readFloat()()` Reads a `float` from this file. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/io/RandomAccessFile#readFully(kotlin.ByteArray)(b: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html!)` Reads `b.length` bytes from this file into the byte array, starting at the current file pointer. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/io/RandomAccessFile#readFully(kotlin.ByteArray,%20kotlin.Int,%20kotlin.Int)(b: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html!, off: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, len: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Reads exactly `len` bytes from this file into the byte array, starting at the current file pointer. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/io/RandomAccessFile#readInt()()` Reads a signed 32-bit integer from this file. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/java/io/RandomAccessFile#readLine()()` Reads the next line of text from this file. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/java/io/RandomAccessFile#readLong()()` Reads a signed 64-bit integer from this file. |
| [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | `https://developer.android.com/reference/kotlin/java/io/RandomAccessFile#readShort()()` Reads a signed 16-bit number from this file. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/java/io/RandomAccessFile#readUTF()()` Reads in a string from this file. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/io/RandomAccessFile#readUnsignedByte()()` Reads an unsigned eight-bit number from this file. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/io/RandomAccessFile#readUnsignedShort()()` Reads an unsigned 16-bit number from this file. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/io/RandomAccessFile#seek(kotlin.Long)(pos: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Sets the file-pointer offset, measured from the beginning of this file, at which the next read or write occurs. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/io/RandomAccessFile#setLength(kotlin.Long)(newLength: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Sets the length of this file. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/io/RandomAccessFile#skipBytes(kotlin.Int)(n: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Attempts to skip over `n` bytes of input discarding the skipped bytes. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/io/RandomAccessFile#write(kotlin.ByteArray)(b: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html!)` Writes `b.length` bytes from the specified byte array to this file, starting at the current file pointer. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/io/RandomAccessFile#write(kotlin.ByteArray,%20kotlin.Int,%20kotlin.Int)(b: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html!, off: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, len: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Writes `len` bytes from the specified byte array starting at offset `off` to this file. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/io/RandomAccessFile#write(kotlin.Int)(b: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Writes the specified byte to this file. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/io/RandomAccessFile#writeBoolean(kotlin.Boolean)(v: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Writes a `boolean` to the file as a one-byte value. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/io/RandomAccessFile#writeByte(kotlin.Int)(v: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Writes a `byte` to the file as a one-byte value. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/io/RandomAccessFile#writeBytes(kotlin.String)(s: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Writes the string to the file as a sequence of bytes. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/io/RandomAccessFile#writeChar(kotlin.Int)(v: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Writes a `char` to the file as a two-byte value, high byte first. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/io/RandomAccessFile#writeChars(kotlin.String)(s: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Writes a string to the file as a sequence of characters. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/io/RandomAccessFile#writeDouble(kotlin.Double)(v: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)` Converts the double argument to a `long` using the `doubleToLongBits` method in class `Double`, and then writes that `long` value to the file as an eight-byte quantity, high byte first. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/io/RandomAccessFile#writeFloat(kotlin.Float)(v: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` Converts the float argument to an `int` using the `floatToIntBits` method in class `Float`, and then writes that `int` value to the file as a four-byte quantity, high byte first. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/io/RandomAccessFile#writeInt(kotlin.Int)(v: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Writes an `int` to the file as four bytes, high byte first. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/io/RandomAccessFile#writeLong(kotlin.Long)(v: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Writes a `long` to the file as eight bytes, high byte first. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/io/RandomAccessFile#writeShort(kotlin.Int)(v: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Writes a `short` to the file as two bytes, high byte first. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/io/RandomAccessFile#writeUTF(kotlin.String)(str: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Writes a string to the file using [modified UTF-8](https://developer.android.com/reference/kotlin/java/io/DataInput#modified-utf-8) encoding in a machine-independent manner. |

| Protected methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/io/RandomAccessFile#finalize()()` Called by the garbage collector on an object when garbage collection determines that there are no more references to the object. |

## Public constructors

### RandomAccessFile

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
RandomAccessFile(
    file: File!, 
    mode: String!)
```

Creates a random access file stream to read from, and optionally to write to, the file specified by the `https://developer.android.com/reference/kotlin/java/io/File` argument. A new `https://developer.android.com/reference/kotlin/java/io/FileDescriptor` object is created to represent this file connection.

The mode argument specifies the access mode in which the file is to be opened. The permitted values and their meanings are:

| Value | Meaning |
|---|---|
| "r" | Open for reading only. Invoking any of the write methods of the resulting object will cause an `https://developer.android.com/reference/kotlin/java/io/IOException` to be thrown. |
| "rw" | Open for reading and writing. If the file does not already exist then an attempt will be made to create it. |
| "rws" | Open for reading and writing, as with "rw", and also require that every update to the file's content or metadata be written synchronously to the underlying storage device. |
| "rwd" | Open for reading and writing, as with "rw", and also require that every update to the file's content be written synchronously to the underlying storage device. |

The "rws" and "rwd" modes work much like the `https://developer.android.com/reference/kotlin/java/nio/channels/FileChannel.html#force(kotlin.Boolean)` method of the `https://developer.android.com/reference/kotlin/java/nio/channels/FileChannel.html#` class, passing arguments of true and false, respectively, except that they always apply to every I/O operation and are therefore often more efficient. If the file resides on a local storage device then when an invocation of a method of this class returns it is guaranteed that all changes made to the file by that invocation will have been written to that device. This is useful for ensuring that critical information is not lost in the event of a system crash. If the file does not reside on a local device then no such guarantee is made.

The "rwd" mode can be used to reduce the number of I/O operations performed. Using "rwd" only requires updates to the file's content to be written to storage; using "rws" requires updates to both the file's content and its metadata to be written, which generally requires at least one more low-level I/O operation.

If there is a security manager, its `checkRead` method is called with the pathname of the `file` argument as its argument to see if read access to the file is allowed. If the mode allows writing, the security manager's `checkWrite` method is also called with the path argument to see if write access to the file is allowed.

| Parameters ||
|---|---|
| `file` | [File](https://developer.android.com/reference/kotlin/java/io/File)!: the file object |
| `mode` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the access mode, as described [above](https://developer.android.com/reference/kotlin/java/io/RandomAccessFile#mode) |

| Exceptions ||
|---|---|
| `java.io.FileNotFoundException` | if the mode is "r" but the given file object does not denote an existing regular file, or if the mode begins with "rw" but the given file object does not denote an existing, writable regular file and a new regular file of that name cannot be created, or if some other error occurs while opening or creating the file |
| `java.lang.IllegalArgumentException` | if the mode argument is not equal to one of "r", "rw", "rws", or "rwd" |
| `java.lang.SecurityException` | if a security manager exists and its `checkRead` method denies read access to the file or the mode is "rw" and the security manager's `checkWrite` method denies write access to the file |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#checkRead(kotlin.String)`
- `https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#checkWrite(kotlin.String)`
- `https://developer.android.com/reference/kotlin/java/nio/channels/FileChannel.html#force(kotlin.Boolean)`

### RandomAccessFile

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
RandomAccessFile(
    name: String!, 
    mode: String!)
```

Creates a random access file stream to read from, and optionally to write to, a file with the specified name. A new `https://developer.android.com/reference/kotlin/java/io/FileDescriptor` object is created to represent the connection to the file.

The mode argument specifies the access mode with which the file is to be opened. The permitted values and their meanings are as specified for the [RandomAccessFile(File,String)](https://developer.android.com/reference/kotlin/java/io/RandomAccessFile#mode) constructor.

If there is a security manager, its `checkRead` method is called with the `name` argument as its argument to see if read access to the file is allowed. If the mode allows writing, the security manager's `checkWrite` method is also called with the `name` argument as its argument to see if write access to the file is allowed.

| Parameters ||
|---|---|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the system-dependent filename |
| `mode` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the access [mode](https://developer.android.com/reference/kotlin/java/io/RandomAccessFile#mode) |

| Exceptions ||
|---|---|
| `java.io.FileNotFoundException` | if the mode is "r" but the given string does not denote an existing regular file, or if the mode begins with "rw" but the given string does not denote an existing, writable regular file and a new regular file of that name cannot be created, or if some other error occurs while opening or creating the file |
| `java.lang.IllegalArgumentException` | if the mode argument is not equal to one of "r", "rw", "rws", or "rwd" |
| `java.lang.SecurityException` | if a security manager exists and its `checkRead` method denies read access to the file or the mode is "rw" and the security manager's `checkWrite` method denies write access to the file |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#`
- `https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#checkRead(kotlin.String)`
- `https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#checkWrite(kotlin.String)`

## Public methods

### close

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun close(): Unit
```

Closes this random access file stream and releases any system resources associated with the stream. A closed random access file cannot perform input or output operations and cannot be reopened.

If this file has an associated channel then the channel is closed as well.

| Exceptions ||
|---|---|
| `java.lang.Exception` | if this resource cannot be closed |
| `java.io.IOException` | if an I/O error occurs. |

### getChannel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getChannel(): FileChannel!
```

Returns the unique `https://developer.android.com/reference/kotlin/java/nio/channels/FileChannel.html#` object associated with this file.

The `https://developer.android.com/reference/kotlin/java/nio/channels/FileChannel.html#position()` of the returned channel will always be equal to this object's file-pointer offset as returned by the `https://developer.android.com/reference/kotlin/java/io/RandomAccessFile#getFilePointer()` method. Changing this object's file-pointer offset, whether explicitly or by reading or writing bytes, will change the position of the channel, and vice versa. Changing the file's length via this object will change the length seen via the file channel, and vice versa.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/nio/channels/FileChannel.html#!` | the file channel associated with this file |

### getFD

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getFD(): FileDescriptor!
```

Returns the opaque file descriptor object associated with this stream.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/io/FileDescriptor!` | the file descriptor object associated with this stream. |

| Exceptions ||
|---|---|
| `java.io.IOException` | if an I/O error occurs. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/io/FileDescriptor`

### getFilePointer

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getFilePointer(): Long
```

Returns the current offset in this file.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the offset from the beginning of the file, in bytes, at which the next read or write occurs. |

| Exceptions ||
|---|---|
| `java.io.IOException` | if an I/O error occurs. |

### length

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun length(): Long
```

Returns the length of this file.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the length of this file, measured in bytes. |

| Exceptions ||
|---|---|
| `java.io.IOException` | if an I/O error occurs. |

### read

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun read(): Int
```

Reads a byte of data from this file. The byte is returned as an integer in the range 0 to 255 (`0x00-0x0ff`). This method blocks if no input is yet available.

Although `RandomAccessFile` is not a subclass of `InputStream`, this method behaves in exactly the same way as the `https://developer.android.com/reference/kotlin/java/io/InputStream#read()` method of `InputStream`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the next byte of data, or `-1` if the end of the file has been reached. |

| Exceptions ||
|---|---|
| `java.io.IOException` | if an I/O error occurs. Not thrown if end-of-file has been reached. |

### read

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun read(b: ByteArray!): Int
```

Reads up to `b.length` bytes of data from this file into an array of bytes. This method blocks until at least one byte of input is available.

Although `RandomAccessFile` is not a subclass of `InputStream`, this method behaves in exactly the same way as the `https://developer.android.com/reference/kotlin/java/io/InputStream#read(kotlin.ByteArray)` method of `InputStream`.

| Parameters ||
|---|---|
| `b` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!: the buffer into which the data is read. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the total number of bytes read into the buffer, or `-1` if there is no more data because the end of this file has been reached. |

| Exceptions ||
|---|---|
| `java.io.IOException` | If the first byte cannot be read for any reason other than end of file, or if the random access file has been closed, or if some other I/O error occurs. |
| `java.lang.NullPointerException` | If `b` is `null`. |

### read

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun read(
    b: ByteArray!, 
    off: Int, 
    len: Int
): Int
```

Reads up to `len` bytes of data from this file into an array of bytes. This method blocks until at least one byte of input is available.

Although `RandomAccessFile` is not a subclass of `InputStream`, this method behaves in exactly the same way as the `https://developer.android.com/reference/kotlin/java/io/InputStream#read(kotlin.ByteArray,%20kotlin.Int,%20kotlin.Int)` method of `InputStream`.

| Parameters ||
|---|---|
| `b` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!: the buffer into which the data is read. |
| `off` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the start offset in array `b` at which the data is written. |
| `len` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the maximum number of bytes read. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the total number of bytes read into the buffer, or `-1` if there is no more data because the end of the file has been reached. |

| Exceptions ||
|---|---|
| `java.io.IOException` | If the first byte cannot be read for any reason other than end of file, or if the random access file has been closed, or if some other I/O error occurs. |
| `java.lang.IndexOutOfBoundsException` | If `off` is negative, `len` is negative, or `len` is greater than `b.length - off` |
| `java.lang.NullPointerException` | If `b` is `null`. |

### readBoolean

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun readBoolean(): Boolean
```

Reads a `boolean` from this file. This method reads a single byte from the file, starting at the current file pointer. A value of `0` represents `false`. Any other value represents `true`. This method blocks until the byte is read, the end of the stream is detected, or an exception is thrown.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | the `boolean` value read. |

| Exceptions ||
|---|---|
| `java.io.EOFException` | if this file has reached the end. |
| `java.io.IOException` | if an I/O error occurs. |

### readByte

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun readByte(): Byte
```

Reads a signed eight-bit value from this file. This method reads a byte from the file, starting from the current file pointer. If the byte read is `b`, where `0 <= b <= 255`, then the result is:

```kotlin
(byte)(b)
  
```

<br />

This method blocks until the byte is read, the end of the stream is detected, or an exception is thrown.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html` | the next byte of this file as a signed eight-bit `byte`. |

| Exceptions ||
|---|---|
| `java.io.EOFException` | if this file has reached the end. |
| `java.io.IOException` | if an I/O error occurs. |

### readChar

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun readChar(): Char
```

Reads a character from this file. This method reads two bytes from the file, starting at the current file pointer. If the bytes read, in order, are `b1` and `b2`, where `0 <= b1, b2 <= 255`, then the result is equal to:

```kotlin
(char)((b1 << 8) | b2)
  
```

<br />

This method blocks until the two bytes are read, the end of the stream is detected, or an exception is thrown.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html` | the next two bytes of this file, interpreted as a `char`. |

| Exceptions ||
|---|---|
| `java.io.EOFException` | if this file reaches the end before reading two bytes. |
| `java.io.IOException` | if an I/O error occurs. |

### readDouble

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun readDouble(): Double
```

Reads a `double` from this file. This method reads a `long` value, starting at the current file pointer, as if by the `readLong` method and then converts that `long` to a `double` using the `longBitsToDouble` method in class `Double`.

This method blocks until the eight bytes are read, the end of the stream is detected, or an exception is thrown.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html` | the next eight bytes of this file, interpreted as a `double`. |

| Exceptions ||
|---|---|
| `java.io.EOFException` | if this file reaches the end before reading eight bytes. |
| `java.io.IOException` | if an I/O error occurs. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/io/RandomAccessFile#readLong()`
- `https://developer.android.com/reference/kotlin/java/lang/Double.html#longBitsToDouble(kotlin.Long)`

### readFloat

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun readFloat(): Float
```

Reads a `float` from this file. This method reads an `int` value, starting at the current file pointer, as if by the `readInt` method and then converts that `int` to a `float` using the `intBitsToFloat` method in class `Float`.

This method blocks until the four bytes are read, the end of the stream is detected, or an exception is thrown.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | the next four bytes of this file, interpreted as a `float`. |

| Exceptions ||
|---|---|
| `java.io.EOFException` | if this file reaches the end before reading four bytes. |
| `java.io.IOException` | if an I/O error occurs. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/io/RandomAccessFile#readInt()`
- `https://developer.android.com/reference/kotlin/java/lang/Float.html#intBitsToFloat(kotlin.Int)`

### readFully

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun readFully(b: ByteArray!): Unit
```

Reads `b.length` bytes from this file into the byte array, starting at the current file pointer. This method reads repeatedly from the file until the requested number of bytes are read. This method blocks until the requested number of bytes are read, the end of the stream is detected, or an exception is thrown.

| Parameters ||
|---|---|
| `b` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!: the buffer into which the data is read. |

| Exceptions ||
|---|---|
| `java.io.EOFException` | if this file reaches the end before reading all the bytes. |
| `java.io.IOException` | if an I/O error occurs. |
| `java.lang.NullPointerException` | if `b` is `null`. |

### readFully

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun readFully(
    b: ByteArray!, 
    off: Int, 
    len: Int
): Unit
```

Reads exactly `len` bytes from this file into the byte array, starting at the current file pointer. This method reads repeatedly from the file until the requested number of bytes are read. This method blocks until the requested number of bytes are read, the end of the stream is detected, or an exception is thrown.

| Parameters ||
|---|---|
| `b` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!: the buffer into which the data is read. |
| `off` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the start offset of the data. |
| `len` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the number of bytes to read. |

| Exceptions ||
|---|---|
| `java.io.EOFException` | if this file reaches the end before reading all the bytes. |
| `java.io.IOException` | if an I/O error occurs. |
| `java.lang.IndexOutOfBoundsException` | if `off` is negative, `len` is negative, or `len` is greater than `b.length - off`. |
| `java.lang.NullPointerException` | if `b` is `null`. |

### readInt

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun readInt(): Int
```

Reads a signed 32-bit integer from this file. This method reads 4 bytes from the file, starting at the current file pointer. If the bytes read, in order, are `b1`, `b2`, `b3`, and `b4`, where `0 <= b1, b2, b3, b4 <= 255`, then the result is equal to:

```kotlin
(b1 << 24) | (b2 << 16) + (b3 << 8) + b4
  
```

<br />

This method blocks until the four bytes are read, the end of the stream is detected, or an exception is thrown.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the next four bytes of this file, interpreted as an `int`. |

| Exceptions ||
|---|---|
| `java.io.EOFException` | if this file reaches the end before reading four bytes. |
| `java.io.IOException` | if an I/O error occurs. |

### readLine

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun readLine(): String!
```

Reads the next line of text from this file. This method successively reads bytes from the file, starting at the current file pointer, until it reaches a line terminator or the end of the file. Each byte is converted into a character by taking the byte's value for the lower eight bits of the character and setting the high eight bits of the character to zero. This method does not, therefore, support the full Unicode character set.

A line of text is terminated by a carriage-return character (`'\u005Cr'`), a newline character (`'\u005Cn'`), a carriage-return character immediately followed by a newline character, or the end of the file. Line-terminating characters are discarded and are not included as part of the string returned.

This method blocks until a newline character is read, a carriage return and the byte following it are read (to see if it is a newline), the end of the file is reached, or an exception is thrown.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | the next line of text from this file, or null if end of file is encountered before even one byte is read. |

| Exceptions ||
|---|---|
| `java.io.IOException` | if an I/O error occurs. |

### readLong

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun readLong(): Long
```

Reads a signed 64-bit integer from this file. This method reads eight bytes from the file, starting at the current file pointer. If the bytes read, in order, are `b1`, `b2`, `b3`, `b4`, `b5`, `b6`, `b7`, and `b8,` where:

```kotlin
0 <= b1, b2, b3, b4, b5, b6, b7, b8 <=255,
  
```

<br />

then the result is equal to:

```kotlin
((long)b1 << 56) + ((long)b2 << 48)
      + ((long)b3 << 40) + ((long)b4 << 32)
      + ((long)b5 << 24) + ((long)b6 << 16)
      + ((long)b7 << 8) + b8
  
```

This method blocks until the eight bytes are read, the end of the stream is detected, or an exception is thrown.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the next eight bytes of this file, interpreted as a `long`. |

| Exceptions ||
|---|---|
| `java.io.EOFException` | if this file reaches the end before reading eight bytes. |
| `java.io.IOException` | if an I/O error occurs. |

### readShort

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun readShort(): Short
```

Reads a signed 16-bit number from this file. The method reads two bytes from this file, starting at the current file pointer. If the two bytes read, in order, are `b1` and `b2`, where each of the two values is between `0` and `255`, inclusive, then the result is equal to:

```kotlin
(short)((b1 << 8) | b2)
  
```

<br />

This method blocks until the two bytes are read, the end of the stream is detected, or an exception is thrown.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html` | the next two bytes of this file, interpreted as a signed 16-bit number. |

| Exceptions ||
|---|---|
| `java.io.EOFException` | if this file reaches the end before reading two bytes. |
| `java.io.IOException` | if an I/O error occurs. |

### readUTF

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun readUTF(): String!
```

Reads in a string from this file. The string has been encoded using a [modified UTF-8](https://developer.android.com/reference/kotlin/java/io/DataInput#modified-utf-8) format.

The first two bytes are read, starting from the current file pointer, as if by `readUnsignedShort`. This value gives the number of following bytes that are in the encoded string, not the length of the resulting string. The following bytes are then interpreted as bytes encoding characters in the modified UTF-8 format and are converted into characters.

This method blocks until all the bytes are read, the end of the stream is detected, or an exception is thrown.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | a Unicode string. |

| Exceptions ||
|---|---|
| `java.io.EOFException` | if this file reaches the end before reading all the bytes. |
| `java.io.IOException` | if an I/O error occurs. |
| `java.io.UTFDataFormatException` | if the bytes do not represent valid modified UTF-8 encoding of a Unicode string. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/io/RandomAccessFile#readUnsignedShort()`

### readUnsignedByte

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun readUnsignedByte(): Int
```

Reads an unsigned eight-bit number from this file. This method reads a byte from this file, starting at the current file pointer, and returns that byte.

This method blocks until the byte is read, the end of the stream is detected, or an exception is thrown.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the next byte of this file, interpreted as an unsigned eight-bit number. |

| Exceptions ||
|---|---|
| `java.io.EOFException` | if this file has reached the end. |
| `java.io.IOException` | if an I/O error occurs. |

### readUnsignedShort

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun readUnsignedShort(): Int
```

Reads an unsigned 16-bit number from this file. This method reads two bytes from the file, starting at the current file pointer. If the bytes read, in order, are `b1` and `b2`, where `0 <= b1, b2 <= 255`, then the result is equal to:

```kotlin
(b1 << 8) | b2
  
```

<br />

This method blocks until the two bytes are read, the end of the stream is detected, or an exception is thrown.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the next two bytes of this file, interpreted as an unsigned 16-bit integer. |

| Exceptions ||
|---|---|
| `java.io.EOFException` | if this file reaches the end before reading two bytes. |
| `java.io.IOException` | if an I/O error occurs. |

### seek

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun seek(pos: Long): Unit
```

Sets the file-pointer offset, measured from the beginning of this file, at which the next read or write occurs. The offset may be set beyond the end of the file. Setting the offset beyond the end of the file does not change the file length. The file length will change only by writing after the offset has been set beyond the end of the file.

| Parameters ||
|---|---|
| `pos` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the offset position, measured in bytes from the beginning of the file, at which to set the file pointer. |

| Exceptions ||
|---|---|
| `java.io.IOException` | if `pos` is less than `0` or if an I/O error occurs. |

### setLength

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setLength(newLength: Long): Unit
```

Sets the length of this file.

If the present length of the file as returned by the `length` method is greater than the `newLength` argument then the file will be truncated. In this case, if the file offset as returned by the `getFilePointer` method is greater than `newLength` then after this method returns the offset will be equal to `newLength`.

If the present length of the file as returned by the `length` method is smaller than the `newLength` argument then the file will be extended. In this case, the contents of the extended portion of the file are not defined.

| Parameters ||
|---|---|
| `newLength` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): The desired length of the file |

| Exceptions ||
|---|---|
| `java.io.IOException` | If an I/O error occurs |

### skipBytes

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun skipBytes(n: Int): Int
```

Attempts to skip over `n` bytes of input discarding the skipped bytes.

This method may skip over some smaller number of bytes, possibly zero. This may result from any of a number of conditions; reaching end of file before `n` bytes have been skipped is only one possibility. This method never throws an `EOFException`. The actual number of bytes skipped is returned. If `n` is negative, no bytes are skipped.

| Parameters ||
|---|---|
| `n` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the number of bytes to be skipped. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the actual number of bytes skipped. |

| Exceptions ||
|---|---|
| `java.io.IOException` | if an I/O error occurs. |

### write

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun write(b: ByteArray!): Unit
```

Writes `b.length` bytes from the specified byte array to this file, starting at the current file pointer.

| Parameters ||
|---|---|
| `b` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!: the data. |

| Exceptions ||
|---|---|
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

Writes `len` bytes from the specified byte array starting at offset `off` to this file.

| Parameters ||
|---|---|
| `b` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!: the data. |
| `off` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the start offset in the data. |
| `len` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the number of bytes to write. |

| Exceptions ||
|---|---|
| `java.io.IOException` | if an I/O error occurs. |

### write

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun write(b: Int): Unit
```

Writes the specified byte to this file. The write starts at the current file pointer.

| Parameters ||
|---|---|
| `b` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the `byte` to be written. |

| Exceptions ||
|---|---|
| `java.io.IOException` | if an I/O error occurs. |

### writeBoolean

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeBoolean(v: Boolean): Unit
```

Writes a `boolean` to the file as a one-byte value. The value `true` is written out as the value `(byte)1`; the value `false` is written out as the value `(byte)0`. The write starts at the current position of the file pointer.

| Parameters ||
|---|---|
| `v` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): a `boolean` value to be written. |

| Exceptions ||
|---|---|
| `java.io.IOException` | if an I/O error occurs. |

### writeByte

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeByte(v: Int): Unit
```

Writes a `byte` to the file as a one-byte value. The write starts at the current position of the file pointer.

| Parameters ||
|---|---|
| `v` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): a `byte` value to be written. |

| Exceptions ||
|---|---|
| `java.io.IOException` | if an I/O error occurs. |

### writeBytes

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeBytes(s: String!): Unit
```

Writes the string to the file as a sequence of bytes. Each character in the string is written out, in sequence, by discarding its high eight bits. The write starts at the current position of the file pointer.

| Parameters ||
|---|---|
| `s` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: a string of bytes to be written. |

| Exceptions ||
|---|---|
| `java.io.IOException` | if an I/O error occurs. |

### writeChar

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeChar(v: Int): Unit
```

Writes a `char` to the file as a two-byte value, high byte first. The write starts at the current position of the file pointer.

| Parameters ||
|---|---|
| `v` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): a `char` value to be written. |

| Exceptions ||
|---|---|
| `java.io.IOException` | if an I/O error occurs. |

### writeChars

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeChars(s: String!): Unit
```

Writes a string to the file as a sequence of characters. Each character is written to the data output stream as if by the `writeChar` method. The write starts at the current position of the file pointer.

| Parameters ||
|---|---|
| `s` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: a `String` value to be written. |

| Exceptions ||
|---|---|
| `java.io.IOException` | if an I/O error occurs. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/io/RandomAccessFile#writeChar(kotlin.Int)`

### writeDouble

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeDouble(v: Double): Unit
```

Converts the double argument to a `long` using the `doubleToLongBits` method in class `Double`, and then writes that `long` value to the file as an eight-byte quantity, high byte first. The write starts at the current position of the file pointer.

| Parameters ||
|---|---|
| `v` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html): a `double` value to be written. |

| Exceptions ||
|---|---|
| `java.io.IOException` | if an I/O error occurs. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/Double.html#doubleToLongBits(kotlin.Double)`

### writeFloat

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeFloat(v: Float): Unit
```

Converts the float argument to an `int` using the `floatToIntBits` method in class `Float`, and then writes that `int` value to the file as a four-byte quantity, high byte first. The write starts at the current position of the file pointer.

| Parameters ||
|---|---|
| `v` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): a `float` value to be written. |

| Exceptions ||
|---|---|
| `java.io.IOException` | if an I/O error occurs. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/Float.html#floatToIntBits(kotlin.Float)`

### writeInt

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeInt(v: Int): Unit
```

Writes an `int` to the file as four bytes, high byte first. The write starts at the current position of the file pointer.

| Parameters ||
|---|---|
| `v` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): an `int` to be written. |

| Exceptions ||
|---|---|
| `java.io.IOException` | if an I/O error occurs. |

### writeLong

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeLong(v: Long): Unit
```

Writes a `long` to the file as eight bytes, high byte first. The write starts at the current position of the file pointer.

| Parameters ||
|---|---|
| `v` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): a `long` to be written. |

| Exceptions ||
|---|---|
| `java.io.IOException` | if an I/O error occurs. |

### writeShort

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeShort(v: Int): Unit
```

Writes a `short` to the file as two bytes, high byte first. The write starts at the current position of the file pointer.

| Parameters ||
|---|---|
| `v` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): a `short` to be written. |

| Exceptions ||
|---|---|
| `java.io.IOException` | if an I/O error occurs. |

### writeUTF

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeUTF(str: String!): Unit
```

Writes a string to the file using [modified UTF-8](https://developer.android.com/reference/kotlin/java/io/DataInput#modified-utf-8) encoding in a machine-independent manner.

First, two bytes are written to the file, starting at the current file pointer, as if by the `writeShort` method giving the number of bytes to follow. This value is the number of bytes actually written out, not the length of the string. Following the length, each character of the string is output, in sequence, using the modified UTF-8 encoding for each character.

| Parameters ||
|---|---|
| `s` | the string value to be written. |
| `str` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: a string to be written. |

| Exceptions ||
|---|---|
| `java.io.IOException` | if an I/O error occurs. |

## Protected methods

### finalize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun finalize(): Unit
```

Called by the garbage collector on an object when garbage collection determines that there are no more references to the object. A subclass overrides the `finalize` method to dispose of system resources or to perform other cleanup.

The general contract of `finalize` is that it is invoked if and when the Java virtual machine has determined that there is no longer any means by which this object can be accessed by any thread that has not yet died, except as a result of an action taken by the finalization of some other object or class which is ready to be finalized. The `finalize` method may take any action, including making this object available again to other threads; the usual purpose of `finalize`, however, is to perform cleanup actions before the object is irrevocably discarded. For example, the finalize method for an object that represents an input/output connection might perform explicit I/O transactions to break the connection before the object is permanently discarded.

The `finalize` method of class `Object` performs no special action; it simply returns normally. Subclasses of `Object` may override this definition.

The Java programming language does not guarantee which thread will invoke the `finalize` method for any given object. It is guaranteed, however, that the thread that invokes finalize will not be holding any user-visible synchronization locks when finalize is invoked. If an uncaught exception is thrown by the finalize method, the exception is ignored and finalization of that object terminates.

After the `finalize` method has been invoked for an object, no further action is taken until the Java virtual machine has again determined that there is no longer any means by which this object can be accessed by any thread that has not yet died, including possible actions by other objects or classes which are ready to be finalized, at which point the object may be discarded.

The `finalize` method is never invoked more than once by a Java virtual machine for any given object.

Any exception thrown by the `finalize` method causes the finalization of this object to be halted, but is otherwise ignored.

| Exceptions ||
|---|---|
| `java.lang.Throwable` | the `Exception` raised by this method |
