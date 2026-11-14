# ZipInputStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ZipInputStream

```
open class ZipInputStream : InflaterInputStream
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [java.io.InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#) ||||
| | ↳ | [java.io.FilterInputStream](https://developer.android.com/reference/kotlin/java/io/FilterInputStream.html#) |||
| | | ↳ | [java.util.zip.InflaterInputStream](https://developer.android.com/reference/kotlin/java/util/zip/InflaterInputStream) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [java.util.zip.ZipInputStream](https://developer.android.com/reference/kotlin/java/util/zip/ZipInputStream#) |

| Known Direct Subclasses [JarInputStream](https://developer.android.com/reference/kotlin/java/util/jar/JarInputStream.html#) |-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------| | [JarInputStream](https://developer.android.com/reference/kotlin/java/util/jar/JarInputStream.html#) | The `JarInputStream` class is used to read the contents of a JAR file from any input stream. | |
| --- | --- | --- | --- | --- | --- | --- |

This class implements an input stream filter for reading files in the ZIP file format. Includes support for both compressed and uncompressed entries.

## Summary

| Constants ||
|-------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CENATT](https://developer.android.com/reference/kotlin/java/util/zip/ZipInputStream#CENATT:kotlin.Int) Central directory (CEN) header internal file attributes field offset. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CENATX](https://developer.android.com/reference/kotlin/java/util/zip/ZipInputStream#CENATX:kotlin.Int) Central directory (CEN) header external file attributes field offset. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CENCOM](https://developer.android.com/reference/kotlin/java/util/zip/ZipInputStream#CENCOM:kotlin.Int) Central directory (CEN) header comment length field offset. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CENCRC](https://developer.android.com/reference/kotlin/java/util/zip/ZipInputStream#CENCRC:kotlin.Int) Central directory (CEN) header uncompressed file crc-32 value field offset. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CENDSK](https://developer.android.com/reference/kotlin/java/util/zip/ZipInputStream#CENDSK:kotlin.Int) Central directory (CEN) header disk number start field offset. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CENEXT](https://developer.android.com/reference/kotlin/java/util/zip/ZipInputStream#CENEXT:kotlin.Int) Central directory (CEN) header extra field length field offset. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CENFLG](https://developer.android.com/reference/kotlin/java/util/zip/ZipInputStream#CENFLG:kotlin.Int) Central directory (CEN) header encrypt, decrypt flags field offset. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CENHDR](https://developer.android.com/reference/kotlin/java/util/zip/ZipInputStream#CENHDR:kotlin.Int) Central directory (CEN) header size in bytes (including signature). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CENHOW](https://developer.android.com/reference/kotlin/java/util/zip/ZipInputStream#CENHOW:kotlin.Int) Central directory (CEN) header compression method field offset. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CENLEN](https://developer.android.com/reference/kotlin/java/util/zip/ZipInputStream#CENLEN:kotlin.Int) Central directory (CEN) header uncompressed size field offset. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CENNAM](https://developer.android.com/reference/kotlin/java/util/zip/ZipInputStream#CENNAM:kotlin.Int) Central directory (CEN) header filename length field offset. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CENOFF](https://developer.android.com/reference/kotlin/java/util/zip/ZipInputStream#CENOFF:kotlin.Int) Central directory (CEN) header LOC header offset field offset. |
| --- | --- |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [CENSIG](https://developer.android.com/reference/kotlin/java/util/zip/ZipInputStream#CENSIG:kotlin.Long) Central directory (CEN) header signature. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CENSIZ](https://developer.android.com/reference/kotlin/java/util/zip/ZipInputStream#CENSIZ:kotlin.Int) Central directory (CEN) header compressed size field offset. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CENTIM](https://developer.android.com/reference/kotlin/java/util/zip/ZipInputStream#CENTIM:kotlin.Int) Central directory (CEN) header modification time field offset. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CENVEM](https://developer.android.com/reference/kotlin/java/util/zip/ZipInputStream#CENVEM:kotlin.Int) Central directory (CEN) header version made by field offset. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CENVER](https://developer.android.com/reference/kotlin/java/util/zip/ZipInputStream#CENVER:kotlin.Int) Central directory (CEN) header version needed to extract field offset. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ENDCOM](https://developer.android.com/reference/kotlin/java/util/zip/ZipInputStream#ENDCOM:kotlin.Int) End of central directory (END) header zip file comment length field offset. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ENDHDR](https://developer.android.com/reference/kotlin/java/util/zip/ZipInputStream#ENDHDR:kotlin.Int) End of central directory (END) header size in bytes (including signature). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ENDOFF](https://developer.android.com/reference/kotlin/java/util/zip/ZipInputStream#ENDOFF:kotlin.Int) End of central directory (END) header offset for the first CEN header field offset. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [ENDSIG](https://developer.android.com/reference/kotlin/java/util/zip/ZipInputStream#ENDSIG:kotlin.Long) End of central directory (END) header signature. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ENDSIZ](https://developer.android.com/reference/kotlin/java/util/zip/ZipInputStream#ENDSIZ:kotlin.Int) End of central directory (END) header central directory size in bytes field offset. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ENDSUB](https://developer.android.com/reference/kotlin/java/util/zip/ZipInputStream#ENDSUB:kotlin.Int) End of central directory (END) header number of entries on this disk field offset. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ENDTOT](https://developer.android.com/reference/kotlin/java/util/zip/ZipInputStream#ENDTOT:kotlin.Int) End of central directory (END) header total number of entries field offset. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EXTCRC](https://developer.android.com/reference/kotlin/java/util/zip/ZipInputStream#EXTCRC:kotlin.Int) Extra local (EXT) header uncompressed file crc-32 value field offset. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EXTHDR](https://developer.android.com/reference/kotlin/java/util/zip/ZipInputStream#EXTHDR:kotlin.Int) Extra local (EXT) header size in bytes (including signature). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EXTLEN](https://developer.android.com/reference/kotlin/java/util/zip/ZipInputStream#EXTLEN:kotlin.Int) Extra local (EXT) header uncompressed size field offset. |
| --- | --- |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [EXTSIG](https://developer.android.com/reference/kotlin/java/util/zip/ZipInputStream#EXTSIG:kotlin.Long) Extra local (EXT) header signature. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EXTSIZ](https://developer.android.com/reference/kotlin/java/util/zip/ZipInputStream#EXTSIZ:kotlin.Int) Extra local (EXT) header compressed size field offset. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LOCCRC](https://developer.android.com/reference/kotlin/java/util/zip/ZipInputStream#LOCCRC:kotlin.Int) Local file (LOC) header uncompressed file crc-32 value field offset. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LOCEXT](https://developer.android.com/reference/kotlin/java/util/zip/ZipInputStream#LOCEXT:kotlin.Int) Local file (LOC) header extra field length field offset. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LOCFLG](https://developer.android.com/reference/kotlin/java/util/zip/ZipInputStream#LOCFLG:kotlin.Int) Local file (LOC) header general purpose bit flag field offset. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LOCHDR](https://developer.android.com/reference/kotlin/java/util/zip/ZipInputStream#LOCHDR:kotlin.Int) Local file (LOC) header size in bytes (including signature). |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LOCHOW](https://developer.android.com/reference/kotlin/java/util/zip/ZipInputStream#LOCHOW:kotlin.Int) Local file (LOC) header compression method field offset. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LOCLEN](https://developer.android.com/reference/kotlin/java/util/zip/ZipInputStream#LOCLEN:kotlin.Int) Local file (LOC) header uncompressed size field offset. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LOCNAM](https://developer.android.com/reference/kotlin/java/util/zip/ZipInputStream#LOCNAM:kotlin.Int) Local file (LOC) header filename length field offset. |
| --- | --- |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [LOCSIG](https://developer.android.com/reference/kotlin/java/util/zip/ZipInputStream#LOCSIG:kotlin.Long) Local file (LOC) header signature. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LOCSIZ](https://developer.android.com/reference/kotlin/java/util/zip/ZipInputStream#LOCSIZ:kotlin.Int) Local file (LOC) header compressed size field offset. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LOCTIM](https://developer.android.com/reference/kotlin/java/util/zip/ZipInputStream#LOCTIM:kotlin.Int) Local file (LOC) header modification time field offset. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LOCVER](https://developer.android.com/reference/kotlin/java/util/zip/ZipInputStream#LOCVER:kotlin.Int) Local file (LOC) header version needed to extract field offset. |

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ZipInputStream](https://developer.android.com/reference/kotlin/java/util/zip/ZipInputStream#ZipInputStream(java.io.InputStream))`(`in:` ` [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)!`)` Creates a new ZIP input stream. |
| [ZipInputStream](https://developer.android.com/reference/kotlin/java/util/zip/ZipInputStream#ZipInputStream(java.io.InputStream,%20java.nio.charset.Charset))`(`in:` ` [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)!`, `charset:` ` [Charset](https://developer.android.com/reference/kotlin/java/nio/charset/Charset.html#)!`)` Creates a new ZIP input stream. |

| Public methods ||
|-----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [available](https://developer.android.com/reference/kotlin/java/util/zip/ZipInputStream#available())`()` Returns 0 after EOF has reached for the current entry data, otherwise always return 1. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](https://developer.android.com/reference/kotlin/java/util/zip/ZipInputStream#close())`()` Closes this input stream and releases any system resources associated with the stream. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [closeEntry](https://developer.android.com/reference/kotlin/java/util/zip/ZipInputStream#closeEntry())`()` Closes the current ZIP entry and positions the stream for reading the next entry. |
| --- | --- |
| open [ZipEntry](https://developer.android.com/reference/kotlin/java/util/zip/ZipEntry)! | [getNextEntry](https://developer.android.com/reference/kotlin/java/util/zip/ZipInputStream#getNextEntry())`()` Reads the next ZIP file entry and positions the stream at the beginning of the entry data. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [read](https://developer.android.com/reference/kotlin/java/util/zip/ZipInputStream#read(kotlin.ByteArray,%20kotlin.Int,%20kotlin.Int))`(`b:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `off:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `len:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Reads from the current ZIP entry into an array of bytes. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [skip](https://developer.android.com/reference/kotlin/java/util/zip/ZipInputStream#skip(kotlin.Long))`(`n:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Skips specified number of bytes in the current ZIP entry. |
| --- | --- |

| Protected methods ||
|-----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [ZipEntry](https://developer.android.com/reference/kotlin/java/util/zip/ZipEntry)! | [createZipEntry](https://developer.android.com/reference/kotlin/java/util/zip/ZipInputStream#createZipEntry(kotlin.String))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Creates a new `ZipEntry` object for the specified entry name. |

| Inherited functions ||
|---|---|
| From class [InflaterInputStream](https://developer.android.com/reference/kotlin/java/util/zip/InflaterInputStream) |------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [fill](https://developer.android.com/reference/kotlin/java/util/zip/InflaterInputStream#fill())`()` Fills input buffer with more data to decompress. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [mark](https://developer.android.com/reference/kotlin/java/util/zip/InflaterInputStream#mark(kotlin.Int))`(`readlimit:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Marks the current position in this input stream. The `mark` method of `InflaterInputStream` does nothing. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [markSupported](https://developer.android.com/reference/kotlin/java/util/zip/InflaterInputStream#markSupported())`()` Tests if this input stream supports the `mark` and `reset` methods. The `markSupported` method of `InflaterInputStream` returns `false`. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [read](https://developer.android.com/reference/kotlin/java/util/zip/InflaterInputStream#read())`()` Reads a byte of uncompressed data. This method will block until enough input is available for decompression. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [reset](https://developer.android.com/reference/kotlin/java/util/zip/InflaterInputStream#reset())`()` Repositions this stream to the position at the time the `mark` method was last called on this input stream. The method `reset` for class `InflaterInputStream` does nothing except throw an `IOException`. <br /> | ||
| From class [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#) |------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)! | [nullInputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#nullInputStream())`()` Returns a new `InputStream` that reads no bytes. The returned stream is initially open. The stream is closed by calling the `close()` method. Subsequent calls to `close()` have no effect. While the stream is open, the `available()`, `read()`, `read(byte[])`, `read(byte[], int, int)`, `readAllBytes()`, `readNBytes(byte[], int, int)`, `readNBytes(int)`, `skip(long)`, `skipNBytes(long)`, and `transferTo()` methods all behave as if end of stream has been reached. After the stream has been closed, these methods all throw `IOException`. The `markSupported()` method returns `false`. The `mark()` method does nothing, and the `reset()` method throws `IOException`. <br /> | | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [readAllBytes](https://developer.android.com/reference/kotlin/java/io/InputStream.html#readAllBytes())`()` Reads all remaining bytes from the input stream. This method blocks until all remaining bytes have been read and end of stream is detected, or an exception is thrown. This method does not close the input stream. When this stream reaches end of stream, further invocations of this method will return an empty byte array. Note that this method is intended for simple cases where it is convenient to read all bytes into a byte array. It is not intended for reading input streams with large amounts of data. The behavior for the case where the input stream is *asynchronously closed*, or the thread interrupted during the read, is highly input stream specific, and therefore not specified. If an I/O error occurs reading from the input stream, then it may do so after some, but not all, bytes have been read. Consequently the input stream may not be at end of stream and may be in an inconsistent state. It is strongly recommended that the stream be promptly closed if an I/O error occurs. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [readNBytes](https://developer.android.com/reference/kotlin/java/io/InputStream.html#readNBytes(kotlin.ByteArray,%20kotlin.Int,%20kotlin.Int))`(`b:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `off:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `len:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Reads the requested number of bytes from the input stream into the given byte array. This method blocks until `len` bytes of input data have been read, end of stream is detected, or an exception is thrown. The number of bytes actually read, possibly zero, is returned. This method does not close the input stream. In the case where end of stream is reached before `len` bytes have been read, then the actual number of bytes read will be returned. When this stream reaches end of stream, further invocations of this method will return zero. If `len` is zero, then no bytes are read and `0` is returned; otherwise, there is an attempt to read up to `len` bytes. The first byte read is stored into element `b[off]`, the next one in to `b[off+1]`, and so on. The number of bytes read is, at most, equal to `len`. Let *k* be the number of bytes actually read; these bytes will be stored in elements `b[off]` through `b[off+`*k* `-1]`, leaving elements `b[off+`*k* `]` through `b[off+len-1]` unaffected. The behavior for the case where the input stream is *asynchronously closed*, or the thread interrupted during the read, is highly input stream specific, and therefore not specified. If an I/O error occurs reading from the input stream, then it may do so after some, but not all, bytes of `b` have been updated with data from the input stream. Consequently the input stream and `b` may be in an inconsistent state. It is strongly recommended that the stream be promptly closed if an I/O error occurs. <br /> | | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [readNBytes](https://developer.android.com/reference/kotlin/java/io/InputStream.html#readNBytes(kotlin.Int))`(`len:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Reads up to a specified number of bytes from the input stream. This method blocks until the requested number of bytes has been read, end of stream is detected, or an exception is thrown. This method does not close the input stream. The length of the returned array equals the number of bytes read from the stream. If `len` is zero, then no bytes are read and an empty byte array is returned. Otherwise, up to `len` bytes are read from the stream. Fewer than `len` bytes may be read if end of stream is encountered. When this stream reaches end of stream, further invocations of this method will return an empty byte array. Note that this method is intended for simple cases where it is convenient to read the specified number of bytes into a byte array. The total amount of memory allocated by this method is proportional to the number of bytes read from the stream which is bounded by `len`. Therefore, the method may be safely called with very large values of `len` provided sufficient memory is available. The behavior for the case where the input stream is *asynchronously closed*, or the thread interrupted during the read, is highly input stream specific, and therefore not specified. If an I/O error occurs reading from the input stream, then it may do so after some, but not all, bytes have been read. Consequently the input stream may not be at end of stream and may be in an inconsistent state. It is strongly recommended that the stream be promptly closed if an I/O error occurs. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [skipNBytes](https://developer.android.com/reference/kotlin/java/io/InputStream.html#skipNBytes(kotlin.Long))`(`n:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Skips over and discards exactly `n` bytes of data from this input stream. If `n` is zero, then no bytes are skipped. If `n` is negative, then no bytes are skipped. Subclasses may handle the negative value differently. This method blocks until the requested number of bytes has been skipped, end of file is reached, or an exception is thrown. If end of stream is reached before the stream is at the desired position, then an `EOFException` is thrown. If an I/O error occurs, then the input stream may be in an inconsistent state. It is strongly recommended that the stream be promptly closed if an I/O error occurs. <br /> | | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [transferTo](https://developer.android.com/reference/kotlin/java/io/InputStream.html#transferTo(java.io.OutputStream))`(`out:` ` [OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream.html#)!`)` Reads all bytes from this input stream and writes the bytes to the given output stream in the order that they are read. On return, this input stream will be at end of stream. This method does not close either stream. This method may block indefinitely reading from the input stream, or writing to the output stream. The behavior for the case where the input and/or output stream is *asynchronously closed*, or the thread interrupted during the transfer, is highly input and output stream specific, and therefore not specified. If an I/O error occurs reading from the input stream or writing to the output stream, then it may do so after some bytes have been read or written. Consequently the input stream may not be at end of stream and one, or both, streams may be in an inconsistent state. It is strongly recommended that both streams be promptly closed if an I/O error occurs. <br /> | ||
| From class [FilterInputStream](https://developer.android.com/reference/kotlin/java/io/FilterInputStream.html#) |----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [read](https://developer.android.com/reference/kotlin/java/io/FilterInputStream.html#read(kotlin.ByteArray))`(`b:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Reads up to `b.length` bytes of data from this input stream into an array of bytes. This method blocks until some input is available. This method simply performs the call `read(b, 0, b.length)` and returns the result. It is important that it does *not* do `in.read(b)` instead; certain subclasses of `FilterInputStream` depend on the implementation strategy actually used. <br /> | ||
| --- | --- | --- | --- | --- | --- | --- | --- |

| Inherited properties ||
|---|---|
| From class [InflaterInputStream](https://developer.android.com/reference/kotlin/java/util/zip/InflaterInputStream) |------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [buf](https://developer.android.com/reference/kotlin/java/util/zip/InflaterInputStream#buf:kotlin.ByteArray) Input buffer for decompression. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [closed](https://developer.android.com/reference/kotlin/java/util/zip/InflaterInputStream#closed:kotlin.Boolean) Indicates whether the #close() method has been called, internal use only. <br /> | | [Inflater](https://developer.android.com/reference/kotlin/java/util/zip/Inflater)! | [inf](https://developer.android.com/reference/kotlin/java/util/zip/InflaterInputStream#inf:java.util.zip.Inflater) Decompressor for this stream. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [len](https://developer.android.com/reference/kotlin/java/util/zip/InflaterInputStream#len:kotlin.Int) Length of input buffer. <br /> | ||
| From class [FilterInputStream](https://developer.android.com/reference/kotlin/java/io/FilterInputStream.html#) |------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------| | [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)! | [in](https://developer.android.com/reference/kotlin/java/io/FilterInputStream.html#in:java.io.InputStream) The input stream to be filtered. <br /> | ||

## Constants

### CENATT

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CENATT: Int
```

Central directory (CEN) header internal file attributes field offset. 

 Value: 36

### CENATX

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CENATX: Int
```

Central directory (CEN) header external file attributes field offset. 

 Value: 38

### CENCOM

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CENCOM: Int
```

Central directory (CEN) header comment length field offset. 

 Value: 32

### CENCRC

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CENCRC: Int
```

Central directory (CEN) header uncompressed file crc-32 value field offset. 

 Value: 16

### CENDSK

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CENDSK: Int
```

Central directory (CEN) header disk number start field offset. 

 Value: 34

### CENEXT

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CENEXT: Int
```

Central directory (CEN) header extra field length field offset. 

 Value: 30

### CENFLG

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CENFLG: Int
```

Central directory (CEN) header encrypt, decrypt flags field offset. 

 Value: 8

### CENHDR

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CENHDR: Int
```

Central directory (CEN) header size in bytes (including signature). 

 Value: 46

### CENHOW

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CENHOW: Int
```

Central directory (CEN) header compression method field offset. 

 Value: 10

### CENLEN

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CENLEN: Int
```

Central directory (CEN) header uncompressed size field offset. 

 Value: 24

### CENNAM

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CENNAM: Int
```

Central directory (CEN) header filename length field offset. 

 Value: 28

### CENOFF

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CENOFF: Int
```

Central directory (CEN) header LOC header offset field offset. 

 Value: 42

### CENSIG

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CENSIG: Long
```

Central directory (CEN) header signature. 

 Value: 33639248L

### CENSIZ

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CENSIZ: Int
```

Central directory (CEN) header compressed size field offset. 

 Value: 20

### CENTIM

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CENTIM: Int
```

Central directory (CEN) header modification time field offset. 

 Value: 12

### CENVEM

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CENVEM: Int
```

Central directory (CEN) header version made by field offset. 

 Value: 4

### CENVER

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CENVER: Int
```

Central directory (CEN) header version needed to extract field offset. 

 Value: 6

### ENDCOM

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ENDCOM: Int
```

End of central directory (END) header zip file comment length field offset. 

 Value: 20

### ENDHDR

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ENDHDR: Int
```

End of central directory (END) header size in bytes (including signature). 

 Value: 22

### ENDOFF

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ENDOFF: Int
```

End of central directory (END) header offset for the first CEN header field offset. 

 Value: 16

### ENDSIG

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ENDSIG: Long
```

End of central directory (END) header signature. 

 Value: 101010256L

### ENDSIZ

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ENDSIZ: Int
```

End of central directory (END) header central directory size in bytes field offset. 

 Value: 12

### ENDSUB

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ENDSUB: Int
```

End of central directory (END) header number of entries on this disk field offset. 

 Value: 8

### ENDTOT

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ENDTOT: Int
```

End of central directory (END) header total number of entries field offset. 

 Value: 10

### EXTCRC

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTCRC: Int
```

Extra local (EXT) header uncompressed file crc-32 value field offset. 

 Value: 4

### EXTHDR

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTHDR: Int
```

Extra local (EXT) header size in bytes (including signature). 

 Value: 16

### EXTLEN

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTLEN: Int
```

Extra local (EXT) header uncompressed size field offset. 

 Value: 12

### EXTSIG

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTSIG: Long
```

Extra local (EXT) header signature. 

 Value: 134695760L

### EXTSIZ

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTSIZ: Int
```

Extra local (EXT) header compressed size field offset. 

 Value: 8

### LOCCRC

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LOCCRC: Int
```

Local file (LOC) header uncompressed file crc-32 value field offset. 

 Value: 14

### LOCEXT

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LOCEXT: Int
```

Local file (LOC) header extra field length field offset. 

 Value: 28

### LOCFLG

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LOCFLG: Int
```

Local file (LOC) header general purpose bit flag field offset. 

 Value: 6

### LOCHDR

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LOCHDR: Int
```

Local file (LOC) header size in bytes (including signature). 

 Value: 30

### LOCHOW

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LOCHOW: Int
```

Local file (LOC) header compression method field offset. 

 Value: 8

### LOCLEN

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LOCLEN: Int
```

Local file (LOC) header uncompressed size field offset. 

 Value: 22

### LOCNAM

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LOCNAM: Int
```

Local file (LOC) header filename length field offset. 

 Value: 26

### LOCSIG

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LOCSIG: Long
```

Local file (LOC) header signature. 

 Value: 67324752L

### LOCSIZ

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LOCSIZ: Int
```

Local file (LOC) header compressed size field offset. 

 Value: 18

### LOCTIM

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LOCTIM: Int
```

Local file (LOC) header modification time field offset. 

 Value: 10

### LOCVER

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LOCVER: Int
```

Local file (LOC) header version needed to extract field offset. 

 Value: 4

## Public constructors

### ZipInputStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ZipInputStream(in: InputStream!)
```

Creates a new ZIP input stream.

The UTF-8 [charset](https://developer.android.com/reference/kotlin/java/nio/charset/Charset.html#) is used to decode the entry names.

| Parameters ||
|------|-------------------------------------------------------------------------------------------------------------------|
| `in` | [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)!: the actual input stream |

### ZipInputStream

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ZipInputStream(
    in: InputStream!, 
    charset: Charset!)
```

Creates a new ZIP input stream.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `in` | [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)!: the actual input stream |
| `charset` | [Charset](https://developer.android.com/reference/kotlin/java/nio/charset/Charset.html#)!: The [charset](https://developer.android.com/reference/kotlin/java/nio/charset/Charset.html#) to be used to decode the ZIP entry name (ignored if the [language encoding bit](https://developer.android.com/reference/kotlin/java/util/zip/package-summary#lang_encoding) of the ZIP entry's general purpose bit flag is set). |

## Public methods

### available

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun available(): Int
```

Returns 0 after EOF has reached for the current entry data, otherwise always return 1.

Programs should not count on this method to return the actual number of bytes that could be read without blocking.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | 1 before EOF and 0 after EOF has reached for current entry. |

| Exceptions ||
|-----------------------|-------------------------|
| `java.io.IOException` | if an I/O error occurs. |

### close

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun close(): Unit
```

Closes this input stream and releases any system resources associated with the stream.

| Exceptions ||
|-----------------------|-----------------------------------|
| `java.lang.Exception` | if this resource cannot be closed |
| `java.io.IOException` | if an I/O error has occurred |

### closeEntry

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun closeEntry(): Unit
```

Closes the current ZIP entry and positions the stream for reading the next entry.

| Exceptions ||
|------------------------------|----------------------------------|
| `java.util.zip.ZipException` | if a ZIP file error has occurred |
| `java.io.IOException` | if an I/O error has occurred |

### getNextEntry

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getNextEntry(): ZipEntry!
```

Reads the next ZIP file entry and positions the stream at the beginning of the entry data.

If the app targets Android U or above, zip file entry names containing ".." or starting with "/" passed here will throw a [ZipException](https://developer.android.com/reference/kotlin/java/util/zip/ZipException). For more details, see [dalvik.system.ZipPathValidator](https://developer.android.com/reference/kotlin/dalvik/system/ZipPathValidator.html#).

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [ZipEntry](https://developer.android.com/reference/kotlin/java/util/zip/ZipEntry)! | the next ZIP file entry, or null if there are no more entries |

| Exceptions ||
|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.util.zip.ZipException` | if (1) a ZIP file error has occurred or (2) `targetSdkVersion >= BUILD.VERSION_CODES.UPSIDE_DOWN_CAKE` and (the `name` argument contains ".." or starts with "/"). |
| `java.io.IOException` | if an I/O error has occurred |

### read

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun read(
    b: ByteArray!, 
    off: Int, 
    len: Int
): Int
```

Reads from the current ZIP entry into an array of bytes. If `len` is not zero, the method blocks until some input is available; otherwise, no bytes are read and `0` is returned.

| Parameters ||
|-------|----------------------------------------------------------------------------------------------------------------------------------|
| `b` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!: the buffer into which the data is read |
| `off` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the start offset in the destination array `b` |
| `len` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the maximum number of bytes read |
| --- | --- |

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the actual number of bytes read, or -1 if the end of the entry is reached |

| Exceptions ||
|---------------------------------------|------------------------------------------------------------------------------------|
| `java.io.IOException` | if an I/O error has occurred |
| `java.lang.NullPointerException` | if `b` is `null`. |
| `java.lang.IndexOutOfBoundsException` | if `off` is negative, `len` is negative, or `len` is greater than `b.length - off` |
| --- | --- |
| `java.util.zip.ZipException` | if a ZIP file error has occurred |

### skip

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun skip(n: Long): Long
```

Skips specified number of bytes in the current ZIP entry.

| Parameters ||
|-----|-----------------------------------------------------------------------------------------------------------|
| `n` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the number of bytes to skip |

| Return ||
|------------------------------------------------------------------------------|------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the actual number of bytes skipped |

| Exceptions ||
|--------------------------------------|----------------------------------|
| `java.io.IOException` | if an I/O error has occurred |
| `java.lang.IllegalArgumentException` | if `n < 0` |
| `java.util.zip.ZipException` | if a ZIP file error has occurred |
| --- | --- |

## Protected methods

### createZipEntry

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun createZipEntry(name: String!): ZipEntry!
```

Creates a new `ZipEntry` object for the specified entry name.

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the ZIP file entry name |

| Return ||
|------------------------------------------------------------------------------------|---------------------------|
| [ZipEntry](https://developer.android.com/reference/kotlin/java/util/zip/ZipEntry)! | the ZipEntry just created |
