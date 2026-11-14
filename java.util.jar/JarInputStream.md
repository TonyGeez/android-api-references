Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# JarInputStream

```
open class JarInputStream : ZipInputStream
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||||
| --- | --- | --- | --- | --- | --- |
| ↳ | [java.io.InputStream](../java.io/InputStream.md) |||||
| | ↳ | [java.io.FilterInputStream](../java.io/FilterInputStream.md) ||||
| | | ↳ | [java.util.zip.InflaterInputStream](../java.util.zip/InflaterInputStream.md) |||
| --- | --- | --- | --- | --- | --- |
| | | | ↳ | [java.util.zip.ZipInputStream](../java.util.zip/ZipInputStream.md) ||
| | | | | ↳ | [java.util.jar.JarInputStream](JarInputStream.md) |

The `JarInputStream` class is used to read the contents of a JAR file from any input stream. It extends the class `java.util.zip.ZipInputStream` with support for reading an optional `Manifest` entry. The `Manifest` can be used to store meta-information about the JAR file and its entries.

## Summary

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/java/util/zip/ZipInputStream.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipInputStream.html#CENATT:kotlin.Int` Central directory (CEN) header internal file attributes field offset. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipInputStream.html#CENATX:kotlin.Int` Central directory (CEN) header external file attributes field offset. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipInputStream.html#CENCOM:kotlin.Int` Central directory (CEN) header comment length field offset. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipInputStream.html#CENCRC:kotlin.Int` Central directory (CEN) header uncompressed file crc-32 value field offset. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipInputStream.html#CENDSK:kotlin.Int` Central directory (CEN) header disk number start field offset. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipInputStream.html#CENEXT:kotlin.Int` Central directory (CEN) header extra field length field offset. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipInputStream.html#CENFLG:kotlin.Int` Central directory (CEN) header encrypt, decrypt flags field offset. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipInputStream.html#CENHDR:kotlin.Int` Central directory (CEN) header size in bytes (including signature). <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipInputStream.html#CENHOW:kotlin.Int` Central directory (CEN) header compression method field offset. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipInputStream.html#CENLEN:kotlin.Int` Central directory (CEN) header uncompressed size field offset. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipInputStream.html#CENNAM:kotlin.Int` Central directory (CEN) header filename length field offset. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipInputStream.html#CENOFF:kotlin.Int` Central directory (CEN) header LOC header offset field offset. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipInputStream.html#CENSIG:kotlin.Long` Central directory (CEN) header signature. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipInputStream.html#CENSIZ:kotlin.Int` Central directory (CEN) header compressed size field offset. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipInputStream.html#CENTIM:kotlin.Int` Central directory (CEN) header modification time field offset. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipInputStream.html#CENVEM:kotlin.Int` Central directory (CEN) header version made by field offset. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipInputStream.html#CENVER:kotlin.Int` Central directory (CEN) header version needed to extract field offset. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipInputStream.html#ENDCOM:kotlin.Int` End of central directory (END) header zip file comment length field offset. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipInputStream.html#ENDHDR:kotlin.Int` End of central directory (END) header size in bytes (including signature). <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipInputStream.html#ENDOFF:kotlin.Int` End of central directory (END) header offset for the first CEN header field offset. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipInputStream.html#ENDSIG:kotlin.Long` End of central directory (END) header signature. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipInputStream.html#ENDSIZ:kotlin.Int` End of central directory (END) header central directory size in bytes field offset. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipInputStream.html#ENDSUB:kotlin.Int` End of central directory (END) header number of entries on this disk field offset. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipInputStream.html#ENDTOT:kotlin.Int` End of central directory (END) header total number of entries field offset. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipInputStream.html#EXTCRC:kotlin.Int` Extra local (EXT) header uncompressed file crc-32 value field offset. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipInputStream.html#EXTHDR:kotlin.Int` Extra local (EXT) header size in bytes (including signature). <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipInputStream.html#EXTLEN:kotlin.Int` Extra local (EXT) header uncompressed size field offset. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipInputStream.html#EXTSIG:kotlin.Long` Extra local (EXT) header signature. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipInputStream.html#EXTSIZ:kotlin.Int` Extra local (EXT) header compressed size field offset. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipInputStream.html#LOCCRC:kotlin.Int` Local file (LOC) header uncompressed file crc-32 value field offset. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipInputStream.html#LOCEXT:kotlin.Int` Local file (LOC) header extra field length field offset. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipInputStream.html#LOCFLG:kotlin.Int` Local file (LOC) header general purpose bit flag field offset. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipInputStream.html#LOCHDR:kotlin.Int` Local file (LOC) header size in bytes (including signature). <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipInputStream.html#LOCHOW:kotlin.Int` Local file (LOC) header compression method field offset. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipInputStream.html#LOCLEN:kotlin.Int` Local file (LOC) header uncompressed size field offset. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipInputStream.html#LOCNAM:kotlin.Int` Local file (LOC) header filename length field offset. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipInputStream.html#LOCSIG:kotlin.Long` Local file (LOC) header signature. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipInputStream.html#LOCSIZ:kotlin.Int` Local file (LOC) header compressed size field offset. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipInputStream.html#LOCTIM:kotlin.Int` Local file (LOC) header modification time field offset. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipInputStream.html#LOCVER:kotlin.Int` Local file (LOC) header version needed to extract field offset. <br /> | ||

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/jar/JarInputStream#JarInputStream(java.io.InputStream)(in: https://developer.android.com/reference/kotlin/java/io/InputStream.html#!)` Creates a new `JarInputStream` and reads the optional manifest. |
| `https://developer.android.com/reference/kotlin/java/util/jar/JarInputStream#JarInputStream(java.io.InputStream,%20kotlin.Boolean)(in: https://developer.android.com/reference/kotlin/java/io/InputStream.html#!, verify: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Creates a new `JarInputStream` and reads the optional manifest. |

| Public methods ||
|---|---|
| open [Manifest](Manifest.md)! | `https://developer.android.com/reference/kotlin/java/util/jar/JarInputStream#getManifest()()` Returns the `Manifest` for this JAR file, or `null` if none. |
| open [ZipEntry](../java.util.zip/ZipEntry.md)! | `https://developer.android.com/reference/kotlin/java/util/jar/JarInputStream#getNextEntry()()` Reads the next ZIP file entry and positions the stream at the beginning of the entry data. |
| open [JarEntry](JarEntry.md)! | `https://developer.android.com/reference/kotlin/java/util/jar/JarInputStream#getNextJarEntry()()` Reads the next JAR file entry and positions the stream at the beginning of the entry data. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/util/jar/JarInputStream#read(kotlin.ByteArray,%20kotlin.Int,%20kotlin.Int)(b: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html!, off: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, len: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Reads from the current JAR file entry into an array of bytes. |

| Protected methods ||
|---|---|
| open [ZipEntry](../java.util.zip/ZipEntry.md)! | `https://developer.android.com/reference/kotlin/java/util/jar/JarInputStream#createZipEntry(kotlin.String)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Creates a new `JarEntry` (`ZipEntry`) for the specified JAR file entry name. |

| Inherited functions ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/java/util/zip/ZipInputStream.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipInputStream.html#available()()` Returns 0 after EOF has reached for the current entry data, otherwise always return 1. Programs should not count on this method to return the actual number of bytes that could be read without blocking. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipInputStream.html#close()()` Closes this input stream and releases any system resources associated with the stream. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipInputStream.html#closeEntry()()` Closes the current ZIP entry and positions the stream for reading the next entry. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipInputStream.html#skip(kotlin.Long)(n: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Skips specified number of bytes in the current ZIP entry. <br /> | ||
| From class `https://developer.android.com/reference/kotlin/java/util/zip/InflaterInputStream.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/InflaterInputStream.html#fill()()` Fills input buffer with more data to decompress. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/InflaterInputStream.html#mark(kotlin.Int)(readlimit: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Marks the current position in this input stream. The `mark` method of `InflaterInputStream` does nothing. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/InflaterInputStream.html#markSupported()()` Tests if this input stream supports the `mark` and `reset` methods. The `markSupported` method of `InflaterInputStream` returns `false`. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/InflaterInputStream.html#read()()` Reads a byte of uncompressed data. This method will block until enough input is available for decompression. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/InflaterInputStream.html#reset()()` Repositions this stream to the position at the time the `mark` method was last called on this input stream. The method `reset` for class `InflaterInputStream` does nothing except throw an `IOException`. <br /> | ||
| From class `https://developer.android.com/reference/kotlin/java/io/InputStream.html#` |---|---| | `https://developer.android.com/reference/kotlin/java/io/InputStream.html#!` | `https://developer.android.com/reference/kotlin/java/io/InputStream.html#nullInputStream()()` Returns a new `InputStream` that reads no bytes. The returned stream is initially open. The stream is closed by calling the `close()` method. Subsequent calls to `close()` have no effect. While the stream is open, the `available()`, `read()`, `read(byte[])`, `read(byte[], int, int)`, `readAllBytes()`, `readNBytes(byte[], int, int)`, `readNBytes(int)`, `skip(long)`, `skipNBytes(long)`, and `transferTo()` methods all behave as if end of stream has been reached. After the stream has been closed, these methods all throw `IOException`. The `markSupported()` method returns `false`. The `mark()` method does nothing, and the `reset()` method throws `IOException`. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html!` | `https://developer.android.com/reference/kotlin/java/io/InputStream.html#readAllBytes()()` Reads all remaining bytes from the input stream. This method blocks until all remaining bytes have been read and end of stream is detected, or an exception is thrown. This method does not close the input stream. When this stream reaches end of stream, further invocations of this method will return an empty byte array. Note that this method is intended for simple cases where it is convenient to read all bytes into a byte array. It is not intended for reading input streams with large amounts of data. The behavior for the case where the input stream is *asynchronously closed*, or the thread interrupted during the read, is highly input stream specific, and therefore not specified. If an I/O error occurs reading from the input stream, then it may do so after some, but not all, bytes have been read. Consequently the input stream may not be at end of stream and may be in an inconsistent state. It is strongly recommended that the stream be promptly closed if an I/O error occurs. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/io/InputStream.html#readNBytes(kotlin.ByteArray,%20kotlin.Int,%20kotlin.Int)(b: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html!, off: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, len: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Reads the requested number of bytes from the input stream into the given byte array. This method blocks until `len` bytes of input data have been read, end of stream is detected, or an exception is thrown. The number of bytes actually read, possibly zero, is returned. This method does not close the input stream. In the case where end of stream is reached before `len` bytes have been read, then the actual number of bytes read will be returned. When this stream reaches end of stream, further invocations of this method will return zero. If `len` is zero, then no bytes are read and `0` is returned; otherwise, there is an attempt to read up to `len` bytes. The first byte read is stored into element `b[off]`, the next one in to `b[off+1]`, and so on. The number of bytes read is, at most, equal to `len`. Let *k* be the number of bytes actually read; these bytes will be stored in elements `b[off]` through `b[off+`*k* `-1]`, leaving elements `b[off+`*k* `]` through `b[off+len-1]` unaffected. The behavior for the case where the input stream is *asynchronously closed*, or the thread interrupted during the read, is highly input stream specific, and therefore not specified. If an I/O error occurs reading from the input stream, then it may do so after some, but not all, bytes of `b` have been updated with data from the input stream. Consequently the input stream and `b` may be in an inconsistent state. It is strongly recommended that the stream be promptly closed if an I/O error occurs. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html!` | `https://developer.android.com/reference/kotlin/java/io/InputStream.html#readNBytes(kotlin.Int)(len: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Reads up to a specified number of bytes from the input stream. This method blocks until the requested number of bytes has been read, end of stream is detected, or an exception is thrown. This method does not close the input stream. The length of the returned array equals the number of bytes read from the stream. If `len` is zero, then no bytes are read and an empty byte array is returned. Otherwise, up to `len` bytes are read from the stream. Fewer than `len` bytes may be read if end of stream is encountered. When this stream reaches end of stream, further invocations of this method will return an empty byte array. Note that this method is intended for simple cases where it is convenient to read the specified number of bytes into a byte array. The total amount of memory allocated by this method is proportional to the number of bytes read from the stream which is bounded by `len`. Therefore, the method may be safely called with very large values of `len` provided sufficient memory is available. The behavior for the case where the input stream is *asynchronously closed*, or the thread interrupted during the read, is highly input stream specific, and therefore not specified. If an I/O error occurs reading from the input stream, then it may do so after some, but not all, bytes have been read. Consequently the input stream may not be at end of stream and may be in an inconsistent state. It is strongly recommended that the stream be promptly closed if an I/O error occurs. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/java/io/InputStream.html#skipNBytes(kotlin.Long)(n: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Skips over and discards exactly `n` bytes of data from this input stream. If `n` is zero, then no bytes are skipped. If `n` is negative, then no bytes are skipped. Subclasses may handle the negative value differently. This method blocks until the requested number of bytes has been skipped, end of file is reached, or an exception is thrown. If end of stream is reached before the stream is at the desired position, then an `EOFException` is thrown. If an I/O error occurs, then the input stream may be in an inconsistent state. It is strongly recommended that the stream be promptly closed if an I/O error occurs. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | `https://developer.android.com/reference/kotlin/java/io/InputStream.html#transferTo(java.io.OutputStream)(out: https://developer.android.com/reference/kotlin/java/io/OutputStream.html#!)` Reads all bytes from this input stream and writes the bytes to the given output stream in the order that they are read. On return, this input stream will be at end of stream. This method does not close either stream. This method may block indefinitely reading from the input stream, or writing to the output stream. The behavior for the case where the input and/or output stream is *asynchronously closed*, or the thread interrupted during the transfer, is highly input and output stream specific, and therefore not specified. If an I/O error occurs reading from the input stream or writing to the output stream, then it may do so after some bytes have been read or written. Consequently the input stream may not be at end of stream and one, or both, streams may be in an inconsistent state. It is strongly recommended that both streams be promptly closed if an I/O error occurs. <br /> | ||
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| From class `https://developer.android.com/reference/kotlin/java/io/FilterInputStream.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/io/FilterInputStream.html#read(kotlin.ByteArray)(b: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html!)` Reads up to `b.length` bytes of data from this input stream into an array of bytes. This method blocks until some input is available. This method simply performs the call `read(b, 0, b.length)` and returns the result. It is important that it does *not* do `in.read(b)` instead; certain subclasses of `FilterInputStream` depend on the implementation strategy actually used. <br /> | ||

| Inherited properties ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/java/util/zip/InflaterInputStream.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html!` | `https://developer.android.com/reference/kotlin/java/util/zip/InflaterInputStream.html#buf:kotlin.ByteArray` Input buffer for decompression. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/InflaterInputStream.html#closed:kotlin.Boolean` Indicates whether the #close() method has been called, internal use only. <br /> | | `https://developer.android.com/reference/kotlin/java/util/zip/Inflater.html#!` | `https://developer.android.com/reference/kotlin/java/util/zip/InflaterInputStream.html#inf:java.util.zip.Inflater` Decompressor for this stream. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/InflaterInputStream.html#len:kotlin.Int` Length of input buffer. <br /> | ||
| From class `https://developer.android.com/reference/kotlin/java/io/FilterInputStream.html#` |---|---| | `https://developer.android.com/reference/kotlin/java/io/InputStream.html#!` | `https://developer.android.com/reference/kotlin/java/io/FilterInputStream.html#in:java.io.InputStream` The input stream to be filtered. <br /> | ||

## Public constructors

### JarInputStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
JarInputStream(in: InputStream!)
```

Creates a new `JarInputStream` and reads the optional manifest. If a manifest is present, also attempts to verify the signatures if the JarInputStream is signed.

| Parameters ||
|---|---|
| `in` | [InputStream](../java.io/InputStream.md)!: the actual input stream |

| Exceptions ||
|---|---|
| `java.io.IOException` | if an I/O error has occurred |

### JarInputStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
JarInputStream(
    in: InputStream!, 
    verify: Boolean)
```

Creates a new `JarInputStream` and reads the optional manifest. If a manifest is present and verify is true, also attempts to verify the signatures if the JarInputStream is signed.

| Parameters ||
|---|---|
| `in` | [InputStream](../java.io/InputStream.md)!: the actual input stream |
| `verify` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): whether or not to verify the JarInputStream if it is signed. |

| Exceptions ||
|---|---|
| `java.io.IOException` | if an I/O error has occurred |

## Public methods

### getManifest

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getManifest(): Manifest!
```

Returns the `Manifest` for this JAR file, or `null` if none.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/jar/Manifest!` | the `Manifest` for this JAR file, or `null` if none. |

### getNextEntry

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getNextEntry(): ZipEntry!
```

Reads the next ZIP file entry and positions the stream at the beginning of the entry data. If verification has been enabled, any invalid signature detected while positioning the stream for the next entry will result in an exception.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/zip/ZipEntry.html#!` | the next ZIP file entry, or null if there are no more entries |

| Exceptions ||
|---|---|
| `java.io.IOException` | if an I/O error has occurred |
| `java.util.zip.ZipException` | if a ZIP file error has occurred |
| `java.lang.SecurityException` | if any of the jar file entries are incorrectly signed. |
| --- | --- |

### getNextJarEntry

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getNextJarEntry(): JarEntry!
```

Reads the next JAR file entry and positions the stream at the beginning of the entry data. If verification has been enabled, any invalid signature detected while positioning the stream for the next entry will result in an exception.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/jar/JarEntry!` | the next JAR file entry, or null if there are no more entries |

| Exceptions ||
|---|---|
| `java.io.IOException` | if an I/O error has occurred |
| `java.lang.SecurityException` | if any of the jar file entries are incorrectly signed. |
| `java.util.zip.ZipException` | if a ZIP file error has occurred |
| --- | --- |

### read

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun read(
    b: ByteArray!, 
    off: Int, 
    len: Int
): Int
```

Reads from the current JAR file entry into an array of bytes. If `len` is not zero, the method blocks until some input is available; otherwise, no bytes are read and `0` is returned. If verification has been enabled, any invalid signature on the current entry will be reported at some point before the end of the entry is reached.

| Parameters ||
|---|---|
| `b` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!: the buffer into which the data is read |
| `off` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the start offset in the destination array `b` |
| `len` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the maximum number of bytes to read |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the actual number of bytes read, or -1 if the end of the entry is reached |

| Exceptions ||
|---|---|
| `java.io.IOException` | if an I/O error has occurred |
| `java.lang.IndexOutOfBoundsException` | If `off` is negative, `len` is negative, or `len` is greater than `b.length - off` |
| `java.lang.NullPointerException` | If `b` is `null`. |
| --- | --- |
| `java.util.zip.ZipException` | if a ZIP file error has occurred |
| `java.lang.SecurityException` | if any of the jar file entries are incorrectly signed. |

## Protected methods

### createZipEntry

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun createZipEntry(name: String!): ZipEntry!
```

Creates a new `JarEntry` (`ZipEntry`) for the specified JAR file entry name. The manifest attributes of the specified JAR file entry name will be copied to the new `JarEntry`.

| Parameters ||
|---|---|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the name of the JAR/ZIP file entry |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/zip/ZipEntry.html#!` | the `JarEntry` object just created |
