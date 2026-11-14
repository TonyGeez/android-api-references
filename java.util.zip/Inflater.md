# Inflater

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Inflater

```
open class Inflater
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [java.util.zip.Inflater](https://developer.android.com/reference/kotlin/java/util/zip/Inflater#) |

This class provides support for general purpose decompression using the popular ZLIB compression library. The ZLIB compression library was initially developed as part of the PNG graphics standard and is not protected by patents. It is fully described in the specifications at the [java.util.zip package description](https://developer.android.com/reference/kotlin/java/util/zip/package-summary#package-description).

This class inflates sequences of ZLIB compressed bytes. The input byte sequence is provided in either byte array or byte buffer, via one of the`setInput()`methods. The output byte sequence is written to the output byte array or byte buffer passed to the`deflate()`methods.

The following code fragment demonstrates a trivial compression and decompression of a string using`Deflater`and`Inflater`. 

```kotlin
try {
      // Encode a String into bytes
      String inputString = "blahblahblah\u20AC\u20AC";
      byte[] input = inputString.getBytes("UTF-8");
 
      // Compress the bytes
      byte[] output = new byte[100];
      Deflater compresser = new Deflater();
      compresser.setInput(input);
      compresser.finish();
      int compressedDataLength = compresser.deflate(output);
 
      // Decompress the bytes
      Inflater decompresser = new Inflater();
      decompresser.setInput(output, 0, compressedDataLength);
      byte[] result = new byte[100];
      int resultLength = decompresser.inflate(result);
      decompresser.end();
 
      // Decode the bytes into a String
      String outputString = new String(result, 0, resultLength, "UTF-8");
  } catch (java.io.UnsupportedEncodingException ex) {
      // handle
  } catch (java.util.zip.DataFormatException ex) {
      // handle
  }
  
```

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [Inflater](https://developer.android.com/reference/kotlin/java/util/zip/Inflater#Inflater())`()` Creates a new decompressor. |
| [Inflater](https://developer.android.com/reference/kotlin/java/util/zip/Inflater#Inflater(kotlin.Boolean))`(`nowrap:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Creates a new decompressor. |

| Public methods ||
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [end](https://developer.android.com/reference/kotlin/java/util/zip/Inflater#end())`()` Closes the decompressor and discards any unprocessed input. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [finished](https://developer.android.com/reference/kotlin/java/util/zip/Inflater#finished())`()` Returns true if the end of the compressed data stream has been reached. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getAdler](https://developer.android.com/reference/kotlin/java/util/zip/Inflater#getAdler())`()` Returns the ADLER-32 value of the uncompressed data. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getBytesRead](https://developer.android.com/reference/kotlin/java/util/zip/Inflater#getBytesRead())`()` Returns the total number of compressed bytes input so far. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getBytesWritten](https://developer.android.com/reference/kotlin/java/util/zip/Inflater#getBytesWritten())`()` Returns the total number of uncompressed bytes output so far. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getRemaining](https://developer.android.com/reference/kotlin/java/util/zip/Inflater#getRemaining())`()` Returns the total number of bytes remaining in the input buffer. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getTotalIn](https://developer.android.com/reference/kotlin/java/util/zip/Inflater#getTotalIn())`()` Returns the total number of compressed bytes input so far. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getTotalOut](https://developer.android.com/reference/kotlin/java/util/zip/Inflater#getTotalOut())`()` Returns the total number of uncompressed bytes output so far. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [inflate](https://developer.android.com/reference/kotlin/java/util/zip/Inflater#inflate(kotlin.ByteArray))`(`output:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Uncompresses bytes into specified buffer. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [inflate](https://developer.android.com/reference/kotlin/java/util/zip/Inflater#inflate(kotlin.ByteArray,%20kotlin.Int,%20kotlin.Int))`(`output:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `off:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `len:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Uncompresses bytes into specified buffer. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [inflate](https://developer.android.com/reference/kotlin/java/util/zip/Inflater#inflate(java.nio.ByteBuffer))`(`output:` ` [ByteBuffer](https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#)!`)` Uncompresses bytes into specified buffer. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [needsDictionary](https://developer.android.com/reference/kotlin/java/util/zip/Inflater#needsDictionary())`()` Returns true if a preset dictionary is needed for decompression. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [needsInput](https://developer.android.com/reference/kotlin/java/util/zip/Inflater#needsInput())`()` Returns true if no data remains in the input buffer. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [reset](https://developer.android.com/reference/kotlin/java/util/zip/Inflater#reset())`()` Resets inflater so that a new set of input data can be processed. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDictionary](https://developer.android.com/reference/kotlin/java/util/zip/Inflater#setDictionary(kotlin.ByteArray))`(`dictionary:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Sets the preset dictionary to the given array of bytes. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDictionary](https://developer.android.com/reference/kotlin/java/util/zip/Inflater#setDictionary(kotlin.ByteArray,%20kotlin.Int,%20kotlin.Int))`(`dictionary:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `off:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `len:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the preset dictionary to the given array of bytes. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDictionary](https://developer.android.com/reference/kotlin/java/util/zip/Inflater#setDictionary(java.nio.ByteBuffer))`(`dictionary:` ` [ByteBuffer](https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#)!`)` Sets the preset dictionary to the bytes in the given buffer. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setInput](https://developer.android.com/reference/kotlin/java/util/zip/Inflater#setInput(kotlin.ByteArray))`(`input:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Sets input data for decompression. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setInput](https://developer.android.com/reference/kotlin/java/util/zip/Inflater#setInput(kotlin.ByteArray,%20kotlin.Int,%20kotlin.Int))`(`input:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `off:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `len:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets input data for decompression. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setInput](https://developer.android.com/reference/kotlin/java/util/zip/Inflater#setInput(java.nio.ByteBuffer))`(`input:` ` [ByteBuffer](https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#)!`)` Sets input data for decompression. |

## Public constructors

### Inflater

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Inflater()
```

Creates a new decompressor. 

### Inflater

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Inflater(nowrap: Boolean)
```

Creates a new decompressor. If the parameter 'nowrap' is true then the ZLIB header and checksum fields will not be used. This provides compatibility with the compression format used by both GZIP and PKZIP.

Note: When using the 'nowrap' option it is also necessary to provide an extra "dummy" byte as input. This is required by the ZLIB native library in order to support certain optimizations.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------|
| `nowrap` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):if true then support GZIP compatible compression |

## Public methods

### end

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun end(): Unit
```

Closes the decompressor and discards any unprocessed input. This method should be called when the decompressor is no longer being used. Once this method is called, the behavior of the Inflater object is undefined. 

### finished

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun finished(): Boolean
```

Returns true if the end of the compressed data stream has been reached.

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the end of the compressed data stream has been reached |

### getAdler

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getAdler(): Int
```

Returns the ADLER-32 value of the uncompressed data.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the ADLER-32 value of the uncompressed data |

### getBytesRead

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getBytesRead(): Long
```

Returns the total number of compressed bytes input so far.

| Return ||
|------------------------------------------------------------------------------|------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the total (non-negative) number of compressed bytes input so far |

### getBytesWritten

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getBytesWritten(): Long
```

Returns the total number of uncompressed bytes output so far.

| Return ||
|------------------------------------------------------------------------------|---------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the total (non-negative) number of uncompressed bytes output so far |

### getRemaining

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getRemaining(): Int
```

Returns the total number of bytes remaining in the input buffer. This can be used to find out what bytes still remain in the input buffer after decompression has finished.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the total number of bytes remaining in the input buffer |

### getTotalIn

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getTotalIn(): Int
```

Returns the total number of compressed bytes input so far.

Since the number of bytes may be greater than Integer.MAX_VALUE, the [getBytesRead()](https://developer.android.com/reference/kotlin/java/util/zip/Inflater#getBytesRead())method is now the preferred means of obtaining this information.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the total number of compressed bytes input so far |

### getTotalOut

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getTotalOut(): Int
```

Returns the total number of uncompressed bytes output so far.

Since the number of bytes may be greater than Integer.MAX_VALUE, the [getBytesWritten()](https://developer.android.com/reference/kotlin/java/util/zip/Inflater#getBytesWritten())method is now the preferred means of obtaining this information.

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the total number of uncompressed bytes output so far |

### inflate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun inflate(output: ByteArray!): Int
```

Uncompresses bytes into specified buffer. Returns actual number of bytes uncompressed. A return value of 0 indicates that needsInput() or needsDictionary() should be called in order to determine if more input data or a preset dictionary is required. In the latter case, getAdler() can be used to get the Adler-32 value of the dictionary required.

The [remaining byte count](https://developer.android.com/reference/kotlin/java/util/zip/Inflater#getRemaining())will be reduced by the number of consumed input bytes. If the [setInput(java.nio.ByteBuffer)](https://developer.android.com/reference/kotlin/java/util/zip/Inflater#setInput(java.nio.ByteBuffer))method was called to provide a buffer for input, the input buffer's position will be advanced the number of consumed bytes.

These byte totals, as well as the [total bytes read](https://developer.android.com/reference/kotlin/java/util/zip/Inflater#getBytesRead())and the [total bytes written](https://developer.android.com/reference/kotlin/java/util/zip/Inflater#getBytesWritten())values, will be updated even in the event that a [DataFormatException](https://developer.android.com/reference/kotlin/java/util/zip/DataFormatException) is thrown to reflect the amount of data consumed and produced before the exception occurred.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------|
| `output` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the buffer for the uncompressed data |

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the actual number of uncompressed bytes |

| Exceptions ||
|-------------------------------------|------------------------------------------|
| `java.util.zip.DataFormatException` | if the compressed data format is invalid |

**See Also**

- [java.util.zip.Inflater#needsInput](https://developer.android.com/reference/kotlin/java/util/zip/Inflater#needsInput())
- [java.util.zip.Inflater#needsDictionary](https://developer.android.com/reference/kotlin/java/util/zip/Inflater#needsDictionary()) 

### inflate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun inflate(
    output: ByteArray!, 
    off: Int, 
    len: Int
): Int
```

Uncompresses bytes into specified buffer. Returns actual number of bytes uncompressed. A return value of 0 indicates that needsInput() or needsDictionary() should be called in order to determine if more input data or a preset dictionary is required. In the latter case, getAdler() can be used to get the Adler-32 value of the dictionary required.

If the [setInput(java.nio.ByteBuffer)](https://developer.android.com/reference/kotlin/java/util/zip/Inflater#setInput(java.nio.ByteBuffer))method was called to provide a buffer for input, the input buffer's position will be advanced by the number of bytes consumed by this operation, even in the event that a [DataFormatException](https://developer.android.com/reference/kotlin/java/util/zip/DataFormatException) is thrown.

The [remaining byte count](https://developer.android.com/reference/kotlin/java/util/zip/Inflater#getRemaining())will be reduced by the number of consumed input bytes. If the [setInput(java.nio.ByteBuffer)](https://developer.android.com/reference/kotlin/java/util/zip/Inflater#setInput(java.nio.ByteBuffer))method was called to provide a buffer for input, the input buffer's position will be advanced the number of consumed bytes.

These byte totals, as well as the [total bytes read](https://developer.android.com/reference/kotlin/java/util/zip/Inflater#getBytesRead())and the [total bytes written](https://developer.android.com/reference/kotlin/java/util/zip/Inflater#getBytesWritten())values, will be updated even in the event that a [DataFormatException](https://developer.android.com/reference/kotlin/java/util/zip/DataFormatException) is thrown to reflect the amount of data consumed and produced before the exception occurred.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------|
| `output` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the buffer for the uncompressed data |
| `off` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the start offset of the data |
| `len` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the maximum number of uncompressed bytes |

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the actual number of uncompressed bytes |

| Exceptions ||
|-------------------------------------|------------------------------------------|
| `java.util.zip.DataFormatException` | if the compressed data format is invalid |

**See Also**

- [java.util.zip.Inflater#needsInput](https://developer.android.com/reference/kotlin/java/util/zip/Inflater#needsInput())
- [java.util.zip.Inflater#needsDictionary](https://developer.android.com/reference/kotlin/java/util/zip/Inflater#needsDictionary()) 

### inflate

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun inflate(output: ByteBuffer!): Int
```

Uncompresses bytes into specified buffer. Returns actual number of bytes uncompressed. A return value of 0 indicates that needsInput() or needsDictionary() should be called in order to determine if more input data or a preset dictionary is required. In the latter case, getAdler() can be used to get the Adler-32 value of the dictionary required.

On success, the position of the given`output`byte buffer will be advanced by as many bytes as were produced by the operation, which is equal to the number returned by this method. Note that the position of the`output`buffer will be advanced even in the event that a [DataFormatException](https://developer.android.com/reference/kotlin/java/util/zip/DataFormatException) is thrown.

The [remaining byte count](https://developer.android.com/reference/kotlin/java/util/zip/Inflater#getRemaining())will be reduced by the number of consumed input bytes. If the [setInput(java.nio.ByteBuffer)](https://developer.android.com/reference/kotlin/java/util/zip/Inflater#setInput(java.nio.ByteBuffer))method was called to provide a buffer for input, the input buffer's position will be advanced the number of consumed bytes.

These byte totals, as well as the [total bytes read](https://developer.android.com/reference/kotlin/java/util/zip/Inflater#getBytesRead())and the [total bytes written](https://developer.android.com/reference/kotlin/java/util/zip/Inflater#getBytesWritten())values, will be updated even in the event that a [DataFormatException](https://developer.android.com/reference/kotlin/java/util/zip/DataFormatException) is thrown to reflect the amount of data consumed and produced before the exception occurred.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------|
| `output` | [ByteBuffer](https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#)!:the buffer for the uncompressed data |

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the actual number of uncompressed bytes |

| Exceptions ||
|-------------------------------------|------------------------------------------|
| `java.util.zip.DataFormatException` | if the compressed data format is invalid |
| `java.nio.ReadOnlyBufferException` | if the given output buffer is read-only |

**See Also**

- [java.util.zip.Inflater#needsInput](https://developer.android.com/reference/kotlin/java/util/zip/Inflater#needsInput())
- [java.util.zip.Inflater#needsDictionary](https://developer.android.com/reference/kotlin/java/util/zip/Inflater#needsDictionary()) 

### needsDictionary

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun needsDictionary(): Boolean
```

Returns true if a preset dictionary is needed for decompression.

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if a preset dictionary is needed for decompression |

**See Also**

### needsInput

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun needsInput(): Boolean
```

Returns true if no data remains in the input buffer. This can be used to determine if one of the`setInput()`methods should be called in order to provide more input.

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if no data remains in the input buffer |

### reset

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun reset(): Unit
```

Resets inflater so that a new set of input data can be processed. 

### setDictionary

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setDictionary(dictionary: ByteArray!): Unit
```

Sets the preset dictionary to the given array of bytes. Should be called when inflate() returns 0 and needsDictionary() returns true indicating that a preset dictionary is required. The method getAdler() can be used to get the Adler-32 value of the dictionary needed.

| Parameters ||
|--------------|--------------------------------------------------------------------------------------------------------------------|
| `dictionary` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the dictionary data bytes |

**See Also**

- [java.util.zip.Inflater#needsDictionary](https://developer.android.com/reference/kotlin/java/util/zip/Inflater#needsDictionary())
- [java.util.zip.Inflater#getAdler](https://developer.android.com/reference/kotlin/java/util/zip/Inflater#getAdler()) 

### setDictionary

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setDictionary(
    dictionary: ByteArray!, 
    off: Int, 
    len: Int
): Unit
```

Sets the preset dictionary to the given array of bytes. Should be called when inflate() returns 0 and needsDictionary() returns true indicating that a preset dictionary is required. The method getAdler() can be used to get the Adler-32 value of the dictionary needed.

| Parameters ||
|--------------|--------------------------------------------------------------------------------------------------------------------|
| `dictionary` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the dictionary data bytes |
| `off` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the start offset of the data |
| `len` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the length of the data |

**See Also**

- [java.util.zip.Inflater#needsDictionary](https://developer.android.com/reference/kotlin/java/util/zip/Inflater#needsDictionary())
- [java.util.zip.Inflater#getAdler](https://developer.android.com/reference/kotlin/java/util/zip/Inflater#getAdler()) 

### setDictionary

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setDictionary(dictionary: ByteBuffer!): Unit
```

Sets the preset dictionary to the bytes in the given buffer. Should be called when inflate() returns 0 and needsDictionary() returns true indicating that a preset dictionary is required. The method getAdler() can be used to get the Adler-32 value of the dictionary needed.

The bytes in given byte buffer will be fully consumed by this method. On return, its position will equal its limit.

| Parameters ||
|--------------|-------------------------------------------------------------------------------------------------------------------|
| `dictionary` | [ByteBuffer](https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#)!:the dictionary data bytes |

**See Also**

- [java.util.zip.Inflater#needsDictionary](https://developer.android.com/reference/kotlin/java/util/zip/Inflater#needsDictionary())
- [java.util.zip.Inflater#getAdler](https://developer.android.com/reference/kotlin/java/util/zip/Inflater#getAdler()) 

### setInput

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setInput(input: ByteArray!): Unit
```

Sets input data for decompression.

One of the`setInput()`methods should be called whenever`needsInput()`returns true indicating that more input data is required.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------|
| `input` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the input data bytes |

**See Also**

- [java.util.zip.Inflater#needsInput](https://developer.android.com/reference/kotlin/java/util/zip/Inflater#needsInput()) 

### setInput

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setInput(
    input: ByteArray!, 
    off: Int, 
    len: Int
): Unit
```

Sets input data for decompression.

One of the`setInput()`methods should be called whenever`needsInput()`returns true indicating that more input data is required.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------|
| `input` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the input data bytes |
| `off` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the start offset of the input data |
| `len` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the length of the input data |

**See Also**

- [java.util.zip.Inflater#needsInput](https://developer.android.com/reference/kotlin/java/util/zip/Inflater#needsInput()) 

### setInput

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setInput(input: ByteBuffer!): Unit
```

Sets input data for decompression.

One of the`setInput()`methods should be called whenever`needsInput()`returns true indicating that more input data is required.

The given buffer's position will be advanced as inflate operations are performed, up to the buffer's limit. The input buffer may be modified (refilled) between inflate operations; doing so is equivalent to creating a new buffer and setting it with this method.

Modifying the input buffer's contents, position, or limit concurrently with an inflate operation will result in undefined behavior, which may include incorrect operation results or operation failure.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------|
| `input` | [ByteBuffer](https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#)!:the input data bytes |

**See Also**

- [java.util.zip.Inflater#needsInput](https://developer.android.com/reference/kotlin/java/util/zip/Inflater#needsInput())
