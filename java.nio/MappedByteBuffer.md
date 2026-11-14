# MappedByteBuffer

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MappedByteBuffer

```
abstract class MappedByteBuffer : ByteBuffer
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [java.nio.Buffer](../java/nio/Buffer.md) |||
| | ↳ | [java.nio.ByteBuffer](../java/nio/ByteBuffer.md) ||
| | | ↳ | [java.nio.MappedByteBuffer](../java/nio/MappedByteBuffer.md) |
| --- | --- | --- | --- |

A direct byte buffer whose content is a memory-mapped region of a file.

Mapped byte buffers are created via the [FileChannel.map](../java/nio/channels/FileChannel.md))method. This class extends the [ByteBuffer](../java/nio/ByteBuffer.md) class with operations that are specific to memory-mapped file regions.

A mapped byte buffer and the file mapping that it represents remain valid until the buffer itself is garbage-collected.

The content of a mapped byte buffer can change at any time, for example if the content of the corresponding region of the mapped file is changed by this program or another. Whether or not such changes occur, and when they occur, is operating-system dependent and therefore unspecified.

All or part of a mapped byte buffer may become inaccessible at any time, for example if the mapped file is truncated. An attempt to access an inaccessible region of a mapped byte buffer will not change the buffer's content and will cause an unspecified exception to be thrown either at the time of the access or at some later time. It is therefore strongly recommended that appropriate precautions be taken to avoid the manipulation of a mapped file by this program, or by a concurrently running program, except to read or write the file's content.

Mapped byte buffers otherwise behave no differently than ordinary direct byte buffers.

## Summary

| Public methods ||
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Buffer](../java/nio/Buffer.md) | [clear](../java/nio/MappedByteBuffer.md))`()` Clears this buffer. |
| abstract [ByteBuffer](../java/nio/ByteBuffer.md) | [compact](../java/nio/MappedByteBuffer.md))`()` Compacts this buffer*(optional operation)*. |
| abstract [ByteBuffer](../java/nio/ByteBuffer.md) | [duplicate](../java/nio/MappedByteBuffer.md))`()` Creates a new byte buffer that shares this buffer's content. |
| --- | --- |
| [Buffer](../java/nio/Buffer.md) | [flip](../java/nio/MappedByteBuffer.md))`()` Flips this buffer. |
| [MappedByteBuffer](../java/nio/MappedByteBuffer.md)! | [force](../java/nio/MappedByteBuffer.md))`()` Forces any changes made to this buffer's content to be written to the storage device containing the mapped file. |
| [MappedByteBuffer](../java/nio/MappedByteBuffer.md)! | [force](../java/nio/MappedByteBuffer.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `length:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Forces any changes made to a region of this buffer's content to be written to the storage device containing the mapped file. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isLoaded](../java/nio/MappedByteBuffer.md))`()` Tells whether or not this buffer's content is resident in physical memory. |
| [Buffer](../java/nio/Buffer.md) | [limit](../java/nio/MappedByteBuffer.md))`(`newLimit:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets this buffer's limit. |
| [MappedByteBuffer](../java/nio/MappedByteBuffer.md)! | [load](../java/nio/MappedByteBuffer.md))`()` Loads this buffer's content into physical memory. |
| --- | --- |
| [Buffer](../java/nio/Buffer.md) | [mark](../java/nio/MappedByteBuffer.md))`()` Sets this buffer's mark at its position. |
| [Buffer](../java/nio/Buffer.md) | [position](../java/nio/MappedByteBuffer.md))`(`newPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets this buffer's position. |
| [Buffer](../java/nio/Buffer.md) | [reset](../java/nio/MappedByteBuffer.md))`()` Resets this buffer's position to the previously-marked position. |
| --- | --- |
| [Buffer](../java/nio/Buffer.md) | [rewind](../java/nio/MappedByteBuffer.md))`()` Rewinds this buffer. |
| abstract [ByteBuffer](../java/nio/ByteBuffer.md) | [slice](../java/nio/MappedByteBuffer.md))`()` Creates a new byte buffer whose content is a shared subsequence of this buffer's content. |
| abstract [MappedByteBuffer](../java/nio/MappedByteBuffer.md) | [slice](../java/nio/MappedByteBuffer.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `length:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a new byte buffer whose content is a shared subsequence of this buffer's content. |
| --- | --- |

| Inherited functions ||
|---|---|
| From class [ByteBuffer](../java/nio/ByteBuffer.md) |-----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [ByteBuffer](../java/nio/ByteBuffer.md) | [alignedSlice](../java/nio/ByteBuffer.md))`(`unitSize:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Creates a new byte buffer whose content is a shared and aligned subsequence of this buffer's content. The content of the new buffer will start at this buffer's current position rounded up to the index of the nearest aligned byte for the given unit size, and end at this buffer's limit rounded down to the index of the nearest aligned byte for the given unit size. If rounding results in out-of-bound values then the new buffer's capacity and limit will be zero. If rounding is within bounds the following expressions will be true for a new buffer`nb`and unit size`unitSize`: ```kotlin <code>nb.alignmentOffset(0, unitSize) == 0 nb.alignmentOffset(nb.limit(), unitSize) == 0 </code> ``` Changes to this buffer's content will be visible in the new buffer, and vice versa; the two buffers' position, limit, and mark values will be independent. The new buffer's position will be zero, its capacity and its limit will be the number of bytes remaining in this buffer or fewer subject to alignment, its mark will be undefined, and its byte order will be [BIG_ENDIAN](../java/nio/ByteOrder.md). The new buffer will be direct if, and only if, this buffer is direct, and it will be read-only if, and only if, this buffer is read-only. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [alignmentOffset](../java/nio/ByteBuffer.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `unitSize:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Returns the memory address, pointing to the byte at the given index, modulo the given unit size. The return value is non-negative in the range of`0`(inclusive) up to`unitSize`(exclusive), with zero indicating that the address of the byte at the index is aligned for the unit size, and a positive value that the address is misaligned for the unit size. If the address of the byte at the index is misaligned, the return value represents how much the index should be adjusted to locate a byte at an aligned address. Specifically, the index should either be decremented by the return value if the latter is not greater than`index`, or be incremented by the unit size minus the return value. Therefore given ```kotlin int value = alignmentOffset(index, unitSize) ``` then the identities ```kotlin alignmentOffset(index - value, unitSize) == 0, value ≤ index ``` and ```kotlin alignmentOffset(index + (unitSize - value), unitSize) == 0 ``` must hold. <br /> | | [ByteBuffer](../java/nio/ByteBuffer.md) | [allocate](../java/nio/ByteBuffer.md))`(`capacity:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Allocates a new byte buffer. The new buffer's position will be zero, its limit will be its capacity, its mark will be undefined, each of its elements will be initialized to zero, and its byte order will be [BIG_ENDIAN](../java/nio/ByteOrder.md). It will have a [backing array](../java/nio/ByteBuffer.md)), and its [array offset](../java/nio/ByteBuffer.md))will be zero. <br /> | | [ByteBuffer](../java/nio/ByteBuffer.md) | [allocateDirect](../java/nio/ByteBuffer.md))`(`capacity:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Allocates a new direct byte buffer. The new buffer's position will be zero, its limit will be its capacity, its mark will be undefined, each of its elements will be initialized to zero, and its byte order will be [BIG_ENDIAN](../java/nio/ByteOrder.md). Whether or not it has a [backing array](../java/nio/ByteBuffer.md))is unspecified. <br /> | | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html) | [array](../java/nio/ByteBuffer.md))`()` <br /> Returns the byte array that backs this buffer*(optional operation)*. Modifications to this buffer's content will cause the returned array's content to be modified, and vice versa. Invoke the [hasArray](../java/nio/ByteBuffer.md))method before invoking this method in order to ensure that this buffer has an accessible backing array. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [arrayOffset](../java/nio/ByteBuffer.md))`()` <br /> Returns the offset within this buffer's backing array of the first element of the buffer*(optional operation)*. If this buffer is backed by an array then buffer position*p* corresponds to array index*p* +`arrayOffset()`. Invoke the [hasArray](../java/nio/ByteBuffer.md))method before invoking this method in order to ensure that this buffer has an accessible backing array. <br /> | | [CharBuffer](../java/nio/CharBuffer.md) | [asCharBuffer](../java/nio/ByteBuffer.md))`()` <br /> Creates a view of this byte buffer as a char buffer. The content of the new buffer will start at this buffer's current position. Changes to this buffer's content will be visible in the new buffer, and vice versa; the two buffers' position, limit, and mark values will be independent. The new buffer's position will be zero, its capacity and its limit will be the number of bytes remaining in this buffer divided by two, its mark will be undefined, and its byte order will be that of the byte buffer at the moment the view is created. The new buffer will be direct if, and only if, this buffer is direct, and it will be read-only if, and only if, this buffer is read-only. <br /> | | [DoubleBuffer](../java/nio/DoubleBuffer.md) | [asDoubleBuffer](../java/nio/ByteBuffer.md))`()` <br /> Creates a view of this byte buffer as a double buffer. The content of the new buffer will start at this buffer's current position. Changes to this buffer's content will be visible in the new buffer, and vice versa; the two buffers' position, limit, and mark values will be independent. The new buffer's position will be zero, its capacity and its limit will be the number of bytes remaining in this buffer divided by eight, its mark will be undefined, and its byte order will be that of the byte buffer at the moment the view is created. The new buffer will be direct if, and only if, this buffer is direct, and it will be read-only if, and only if, this buffer is read-only. <br /> | | [FloatBuffer](../java/nio/FloatBuffer.md) | [asFloatBuffer](../java/nio/ByteBuffer.md))`()` <br /> Creates a view of this byte buffer as a float buffer. The content of the new buffer will start at this buffer's current position. Changes to this buffer's content will be visible in the new buffer, and vice versa; the two buffers' position, limit, and mark values will be independent. The new buffer's position will be zero, its capacity and its limit will be the number of bytes remaining in this buffer divided by four, its mark will be undefined, and its byte order will be that of the byte buffer at the moment the view is created. The new buffer will be direct if, and only if, this buffer is direct, and it will be read-only if, and only if, this buffer is read-only. <br /> | | [IntBuffer](../java/nio/IntBuffer.md) | [asIntBuffer](../java/nio/ByteBuffer.md))`()` <br /> Creates a view of this byte buffer as an int buffer. The content of the new buffer will start at this buffer's current position. Changes to this buffer's content will be visible in the new buffer, and vice versa; the two buffers' position, limit, and mark values will be independent. The new buffer's position will be zero, its capacity and its limit will be the number of bytes remaining in this buffer divided by four, its mark will be undefined, and its byte order will be that of the byte buffer at the moment the view is created. The new buffer will be direct if, and only if, this buffer is direct, and it will be read-only if, and only if, this buffer is read-only. <br /> | | [LongBuffer](../java/nio/LongBuffer.md) | [asLongBuffer](../java/nio/ByteBuffer.md))`()` <br /> Creates a view of this byte buffer as a long buffer. The content of the new buffer will start at this buffer's current position. Changes to this buffer's content will be visible in the new buffer, and vice versa; the two buffers' position, limit, and mark values will be independent. The new buffer's position will be zero, its capacity and its limit will be the number of bytes remaining in this buffer divided by eight, its mark will be undefined, and its byte order will be that of the byte buffer at the moment the view is created. The new buffer will be direct if, and only if, this buffer is direct, and it will be read-only if, and only if, this buffer is read-only. <br /> | | [ByteBuffer](../java/nio/ByteBuffer.md) | [asReadOnlyBuffer](../java/nio/ByteBuffer.md))`()` <br /> Creates a new, read-only byte buffer that shares this buffer's content. The content of the new buffer will be that of this buffer. Changes to this buffer's content will be visible in the new buffer; the new buffer itself, however, will be read-only and will not allow the shared content to be modified. The two buffers' position, limit, and mark values will be independent. The new buffer's capacity, limit, position, and mark values will be identical to those of this buffer, and its byte order will be [BIG_ENDIAN](../java/nio/ByteOrder.md). If this buffer is itself read-only then this method behaves in exactly the same way as the [duplicate](../java/nio/ByteBuffer.md))method. <br /> | | [ShortBuffer](../java/nio/ShortBuffer.md) | [asShortBuffer](../java/nio/ByteBuffer.md))`()` <br /> Creates a view of this byte buffer as a short buffer. The content of the new buffer will start at this buffer's current position. Changes to this buffer's content will be visible in the new buffer, and vice versa; the two buffers' position, limit, and mark values will be independent. The new buffer's position will be zero, its capacity and its limit will be the number of bytes remaining in this buffer divided by two, its mark will be undefined, and its byte order will be that of the byte buffer at the moment the view is created. The new buffer will be direct if, and only if, this buffer is direct, and it will be read-only if, and only if, this buffer is read-only. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [compareTo](../java/nio/ByteBuffer.md))`(`other:` ` [ByteBuffer](../java/nio/ByteBuffer.md)`)` <br /> Compares this buffer to another. Two byte buffers are compared by comparing their sequences of remaining elements lexicographically, without regard to the starting position of each sequence within its corresponding buffer. Pairs of`byte`elements are compared as if by invoking [Byte.compare(byte,byte)](../java/lang/Byte.md)). A byte buffer is not comparable to any other type of object. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](../java/nio/ByteBuffer.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> Tells whether or not this buffer is equal to another object. Two byte buffers are equal if, and only if, 1. They have the same element type, 2. They have the same number of remaining elements, and 3. The two sequences of remaining elements, considered independently of their starting positions, are pointwise equal. A byte buffer is not equal to any other type of object. <br /> | | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [get](../java/nio/ByteBuffer.md))`()` <br /> Relative*get*method. Reads the byte at this buffer's current position, and then increments the position. <br /> | | [ByteBuffer](../java/nio/ByteBuffer.md) | [get](../java/nio/ByteBuffer.md))`(`dst:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)`)` <br /> Relative bulk*get*method. This method transfers bytes from this buffer into the given destination array. An invocation of this method of the form`src.get(a)`behaves in exactly the same way as the invocation ```kotlin src.get(a, 0, a.length) ``` <br /> | | [ByteBuffer](../java/nio/ByteBuffer.md) | [get](../java/nio/ByteBuffer.md))`(`dst:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)`, `offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `length:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Relative bulk*get*method. This method transfers bytes from this buffer into the given destination array. If there are fewer bytes remaining in the buffer than are required to satisfy the request, that is, if`length``>``remaining()`, then no bytes are transferred and a [BufferUnderflowException](../java/nio/BufferUnderflowException.md) is thrown. Otherwise, this method copies`length`bytes from this buffer into the given array, starting at the current position of this buffer and at the given offset in the array. The position of this buffer is then incremented by`length`. In other words, an invocation of this method of the form`src.get(dst, off, len)`has exactly the same effect as the loop ```kotlin <code>for (int i = off; i &lt; off + len; i++) dst[i] = src.get(); </code> ``` except that it first checks that there are sufficient bytes in this buffer and it is potentially much more efficient. <br /> | | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [get](../java/nio/ByteBuffer.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Absolute*get*method. Reads the byte at the given index. <br /> | | [ByteBuffer](../java/nio/ByteBuffer.md) | [get](../java/nio/ByteBuffer.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `dst:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)`)` <br /> Absolute bulk*get*method. This method transfers bytes from this buffer into the given destination array. The position of this buffer is unchanged. An invocation of this method of the form`src.get(index, dst)`behaves in exactly the same way as the invocation: ```kotlin src.get(index, dst, 0, dst.length) ``` <br /> | | [ByteBuffer](../java/nio/ByteBuffer.md) | [get](../java/nio/ByteBuffer.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `dst:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)`, `offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `length:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Absolute bulk*get*method. This method transfers`length`bytes from this buffer into the given array, starting at the given index in this buffer and at the given offset in the array. The position of this buffer is unchanged. An invocation of this method of the form`src.get(index, dst, offset, length)`has exactly the same effect as the following loop except that it first checks the consistency of the supplied parameters and it is potentially much more efficient: ```kotlin <code>for (int i = offset, j = index; i &lt; offset + length; i++, j++) dst[i] = src.get(j); </code> ``` <br /> | | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | [getChar](../java/nio/ByteBuffer.md))`()` <br /> Relative*get*method for reading a char value. Reads the next two bytes at this buffer's current position, composing them into a char value according to the current byte order, and then increments the position by two. <br /> | | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | [getChar](../java/nio/ByteBuffer.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Absolute*get*method for reading a char value. Reads two bytes at the given index, composing them into a char value according to the current byte order. <br /> | | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [getDouble](../java/nio/ByteBuffer.md))`()` <br /> Relative*get*method for reading a double value. Reads the next eight bytes at this buffer's current position, composing them into a double value according to the current byte order, and then increments the position by eight. <br /> | | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [getDouble](../java/nio/ByteBuffer.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Absolute*get*method for reading a double value. Reads eight bytes at the given index, composing them into a double value according to the current byte order. <br /> | | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getFloat](../java/nio/ByteBuffer.md))`()` <br /> Relative*get*method for reading a float value. Reads the next four bytes at this buffer's current position, composing them into a float value according to the current byte order, and then increments the position by four. <br /> | | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getFloat](../java/nio/ByteBuffer.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Absolute*get*method for reading a float value. Reads four bytes at the given index, composing them into a float value according to the current byte order. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getInt](../java/nio/ByteBuffer.md))`()` <br /> Relative*get*method for reading an int value. Reads the next four bytes at this buffer's current position, composing them into an int value according to the current byte order, and then increments the position by four. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getInt](../java/nio/ByteBuffer.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Absolute*get*method for reading an int value. Reads four bytes at the given index, composing them into a int value according to the current byte order. <br /> | | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getLong](../java/nio/ByteBuffer.md))`()` <br /> Relative*get*method for reading a long value. Reads the next eight bytes at this buffer's current position, composing them into a long value according to the current byte order, and then increments the position by eight. <br /> | | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getLong](../java/nio/ByteBuffer.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Absolute*get*method for reading a long value. Reads eight bytes at the given index, composing them into a long value according to the current byte order. <br /> | | [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [getShort](../java/nio/ByteBuffer.md))`()` <br /> Relative*get*method for reading a short value. Reads the next two bytes at this buffer's current position, composing them into a short value according to the current byte order, and then increments the position by two. <br /> | | [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [getShort](../java/nio/ByteBuffer.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Absolute*get*method for reading a short value. Reads two bytes at the given index, composing them into a short value according to the current byte order. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasArray](../java/nio/ByteBuffer.md))`()` <br /> Tells whether or not this buffer is backed by an accessible byte array. If this method returns`true`then the [array](../java/nio/ByteBuffer.md))and [arrayOffset](../java/nio/ByteBuffer.md))methods may safely be invoked. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](../java/nio/ByteBuffer.md))`()` <br /> Returns the current hash code of this buffer. The hash code of a byte buffer depends only upon its remaining elements; that is, upon the elements from`position()`up to, and including, the element at`limit()`-`1`. Because buffer hash codes are content-dependent, it is inadvisable to use buffers as keys in hash maps or similar data structures unless it is known that their contents will not change. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isDirect](../java/nio/ByteBuffer.md))`()` <br /> Tells whether or not this byte buffer is direct. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [mismatch](../java/nio/ByteBuffer.md))`(`that:` ` [ByteBuffer](../java/nio/ByteBuffer.md)`)` <br /> Finds and returns the relative index of the first mismatch between this buffer and a given buffer. The index is relative to the [position](../java/nio/Buffer.md))of each buffer and will be in the range of 0 (inclusive) up to the smaller of the [remaining](../java/nio/Buffer.md))elements in each buffer (exclusive). If the two buffers share a common prefix then the returned index is the length of the common prefix and it follows that there is a mismatch between the two buffers at that index within the respective buffers. If one buffer is a proper prefix of the other then the returned index is the smaller of the remaining elements in each buffer, and it follows that the index is only valid for the buffer with the larger number of remaining elements. Otherwise, there is no mismatch. <br /> | | [ByteOrder](../java/nio/ByteOrder.md) | [order](../java/nio/ByteBuffer.md))`()` <br /> Retrieves this buffer's byte order. The byte order is used when reading or writing multibyte values, and when creating buffers that are views of this byte buffer. The order of a newly-created byte buffer is always [BIG_ENDIAN](../java/nio/ByteOrder.md). <br /> | | [ByteBuffer](../java/nio/ByteBuffer.md) | [order](../java/nio/ByteBuffer.md))`(`bo:` ` [ByteOrder](../java/nio/ByteOrder.md)`)` <br /> Modifies this buffer's byte order. <br /> | | [ByteBuffer](../java/nio/ByteBuffer.md) | [put](../java/nio/ByteBuffer.md))`(`b:` ` [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html)`)` <br /> Relative*put* method*(optional operation)*. Writes the given byte into this buffer at the current position, and then increments the position. <br /> | | [ByteBuffer](../java/nio/ByteBuffer.md) | [put](../java/nio/ByteBuffer.md))`(`src:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)`)` <br /> Relative bulk*put* method*(optional operation)*. This method transfers the entire content of the given source byte array into this buffer. An invocation of this method of the form`dst.put(a)`behaves in exactly the same way as the invocation ```kotlin dst.put(a, 0, a.length) ``` <br /> | | [ByteBuffer](../java/nio/ByteBuffer.md) | [put](../java/nio/ByteBuffer.md))`(`src:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)`, `offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `length:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Relative bulk*put* method*(optional operation)*. This method transfers bytes into this buffer from the given source array. If there are more bytes to be copied from the array than remain in this buffer, that is, if`length``>``remaining()`, then no bytes are transferred and a [BufferOverflowException](../java/nio/BufferOverflowException.md) is thrown. Otherwise, this method copies`length`bytes from the given array into this buffer, starting at the given offset in the array and at the current position of this buffer. The position of this buffer is then incremented by`length`. In other words, an invocation of this method of the form`dst.put(src, off, len)`has exactly the same effect as the loop ```kotlin <code>for (int i = off; i &lt; off + len; i++) dst.put(src[i]); </code> ``` except that it first checks that there is sufficient space in this buffer and it is potentially much more efficient. <br /> | | [ByteBuffer](../java/nio/ByteBuffer.md) | [put](../java/nio/ByteBuffer.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `b:` ` [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html)`)` <br /> Absolute*put* method*(optional operation)*. Writes the given byte into this buffer at the given index. <br /> | | [ByteBuffer](../java/nio/ByteBuffer.md) | [put](../java/nio/ByteBuffer.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `src:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)`)` <br /> Absolute bulk*put* method*(optional operation)*. This method copies bytes into this buffer from the given source array. The position of this buffer is unchanged. An invocation of this method of the form`dst.put(index, src)`behaves in exactly the same way as the invocation: ```kotlin dst.put(index, src, 0, src.length); ``` <br /> | | [ByteBuffer](../java/nio/ByteBuffer.md) | [put](../java/nio/ByteBuffer.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `src:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)`, `offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `length:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Absolute bulk*put* method*(optional operation)*. This method transfers`length`bytes from the given array, starting at the given offset in the array and at the given index in this buffer. The position of this buffer is unchanged. An invocation of this method of the form`dst.put(index, src, offset, length)`has exactly the same effect as the following loop except that it first checks the consistency of the supplied parameters and it is potentially much more efficient: ```kotlin <code>for (int i = offset, j = index; i &lt; offset + length; i++, j++) dst.put(j, src[i]); </code> ``` <br /> | | [ByteBuffer](../java/nio/ByteBuffer.md) | [put](../java/nio/ByteBuffer.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `src:` ` [ByteBuffer](../java/nio/ByteBuffer.md)`, `offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `length:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Absolute bulk*put* method*(optional operation)*. This method transfers`length`bytes into this buffer from the given source buffer, starting at the given`offset`in the source buffer and the given`index`in this buffer. The positions of both buffers are unchanged. In other words, an invocation of this method of the form`dst.put(index, src, offset, length)`has exactly the same effect as the loop ```kotlin <code>for (int i = offset, j = index; i &lt; offset + length; i++, j++) dst.put(j, src.get(i)); </code> ``` except that it first checks the consistency of the supplied parameters and it is potentially much more efficient. If this buffer and the source buffer share the same backing array or memory, then the result will be as if the source elements were first copied to an intermediate location before being written into this buffer. <br /> | | [ByteBuffer](../java/nio/ByteBuffer.md) | [put](../java/nio/ByteBuffer.md))`(`src:` ` [ByteBuffer](../java/nio/ByteBuffer.md)`)` <br /> Relative bulk*put* method*(optional operation)*. This method transfers the bytes remaining in the given source buffer into this buffer. If there are more bytes remaining in the source buffer than in this buffer, that is, if`src.remaining()``>``remaining()`, then no bytes are transferred and a [BufferOverflowException](../java/nio/BufferOverflowException.md) is thrown. Otherwise, this method copies*n* =`src.remaining()`bytes from the given buffer into this buffer, starting at each buffer's current position. The positions of both buffers are then incremented by*n*. In other words, an invocation of this method of the form`dst.put(src)`has exactly the same effect as the loop ```kotlin while (src.hasRemaining()) dst.put(src.get()); ``` except that it first checks that there is sufficient space in this buffer and it is potentially much more efficient. If this buffer and the source buffer share the same backing array or memory, then the result will be as if the source elements were first copied to an intermediate location before being written into this buffer. <br /> | | [ByteBuffer](../java/nio/ByteBuffer.md) | [putChar](../java/nio/ByteBuffer.md))`(`value:` ` [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)`)` <br /> Relative*put* method for writing a char value*(optional operation)*. Writes two bytes containing the given char value, in the current byte order, into this buffer at the current position, and then increments the position by two. <br /> | | [ByteBuffer](../java/nio/ByteBuffer.md) | [putChar](../java/nio/ByteBuffer.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `value:` ` [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)`)` <br /> Absolute*put* method for writing a char value*(optional operation)*. Writes two bytes containing the given char value, in the current byte order, into this buffer at the given index. <br /> | | [ByteBuffer](../java/nio/ByteBuffer.md) | [putDouble](../java/nio/ByteBuffer.md))`(`value:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`)` <br /> Relative*put* method for writing a double value*(optional operation)*. Writes eight bytes containing the given double value, in the current byte order, into this buffer at the current position, and then increments the position by eight. <br /> | | [ByteBuffer](../java/nio/ByteBuffer.md) | [putDouble](../java/nio/ByteBuffer.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `value:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`)` <br /> Absolute*put* method for writing a double value*(optional operation)*. Writes eight bytes containing the given double value, in the current byte order, into this buffer at the given index. <br /> | | [ByteBuffer](../java/nio/ByteBuffer.md) | [putFloat](../java/nio/ByteBuffer.md))`(`value:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` <br /> Relative*put* method for writing a float value*(optional operation)*. Writes four bytes containing the given float value, in the current byte order, into this buffer at the current position, and then increments the position by four. <br /> | | [ByteBuffer](../java/nio/ByteBuffer.md) | [putFloat](../java/nio/ByteBuffer.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `value:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` <br /> Absolute*put* method for writing a float value*(optional operation)*. Writes four bytes containing the given float value, in the current byte order, into this buffer at the given index. <br /> | | [ByteBuffer](../java/nio/ByteBuffer.md) | [putInt](../java/nio/ByteBuffer.md))`(`value:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Relative*put* method for writing an int value*(optional operation)*. Writes four bytes containing the given int value, in the current byte order, into this buffer at the current position, and then increments the position by four. <br /> | | [ByteBuffer](../java/nio/ByteBuffer.md) | [putInt](../java/nio/ByteBuffer.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `value:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Absolute*put* method for writing an int value*(optional operation)*. Writes four bytes containing the given int value, in the current byte order, into this buffer at the given index. <br /> | | [ByteBuffer](../java/nio/ByteBuffer.md) | [putLong](../java/nio/ByteBuffer.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `value:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` <br /> Absolute*put* method for writing a long value*(optional operation)*. Writes eight bytes containing the given long value, in the current byte order, into this buffer at the given index. <br /> | | [ByteBuffer](../java/nio/ByteBuffer.md) | [putLong](../java/nio/ByteBuffer.md))`(`value:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` <br /> Relative*put* method for writing a long value*(optional operation)*. Writes eight bytes containing the given long value, in the current byte order, into this buffer at the current position, and then increments the position by eight. <br /> | | [ByteBuffer](../java/nio/ByteBuffer.md) | [putShort](../java/nio/ByteBuffer.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `value:` ` [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html)`)` <br /> Absolute*put* method for writing a short value*(optional operation)*. Writes two bytes containing the given short value, in the current byte order, into this buffer at the given index. <br /> | | [ByteBuffer](../java/nio/ByteBuffer.md) | [putShort](../java/nio/ByteBuffer.md))`(`value:` ` [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html)`)` <br /> Relative*put* method for writing a short value*(optional operation)*. Writes two bytes containing the given short value, in the current byte order, into this buffer at the current position, and then increments the position by two. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../java/nio/ByteBuffer.md))`()` <br /> Returns a string summarizing the state of this buffer. <br /> | | [ByteBuffer](../java/nio/ByteBuffer.md) | [wrap](../java/nio/ByteBuffer.md))`(`array:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)`)` <br /> Wraps a byte array into a buffer. The new buffer will be backed by the given byte array; that is, modifications to the buffer will cause the array to be modified and vice versa. The new buffer's capacity and limit will be`array.length`, its position will be zero, its mark will be undefined, and its byte order will be [BIG_ENDIAN](../java/nio/ByteOrder.md). Its [backing array](../java/nio/ByteBuffer.md))will be the given array, and its [array offset](../java/nio/ByteBuffer.md))will be zero. <br /> | | [ByteBuffer](../java/nio/ByteBuffer.md) | [wrap](../java/nio/ByteBuffer.md))`(`array:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)`, `offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `length:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Wraps a byte array into a buffer. The new buffer will be backed by the given byte array; that is, modifications to the buffer will cause the array to be modified and vice versa. The new buffer's capacity will be`array.length`, its position will be`offset`, its limit will be`offset + length`, its mark will be undefined, and its byte order will be [BIG_ENDIAN](../java/nio/ByteOrder.md). Its [backing array](../java/nio/ByteBuffer.md))will be the given array, and its [array offset](../java/nio/ByteBuffer.md))will be zero. <br /> | ||
| From class [Buffer](../java/nio/Buffer.md) |------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [capacity](../java/nio/Buffer.md))`()` <br /> Returns this buffer's capacity. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasRemaining](../java/nio/Buffer.md))`()` <br /> Tells whether there are any elements between the current position and the limit. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isReadOnly](../java/nio/Buffer.md))`()` <br /> Tells whether or not this buffer is read-only. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [limit](../java/nio/Buffer.md))`()` <br /> Returns this buffer's limit. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [position](../java/nio/Buffer.md))`()` <br /> Returns this buffer's position. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [remaining](../java/nio/Buffer.md))`()` <br /> Returns the number of elements between the current position and the limit. <br /> | ||

## Public methods

### clear

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun clear(): Buffer
```

Clears this buffer. The position is set to zero, the limit is set to the capacity, and the mark is discarded.

Invoke this method before using a sequence of channel-read or*put*operations to fill this buffer. For example: 

```kotlin
buf.clear();     // Prepare buffer for reading
  in.read(buf);    // Read data
```

This method does not actually erase the data in the buffer, but it is named as if it did because it will most often be used in situations in which that might as well be the case.

| Return ||
|--------------------------------------------------------------------------|-------------|
| [Buffer](../java/nio/Buffer.md) | This buffer |

### compact

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun compact(): ByteBuffer
```

Compacts this buffer*(optional operation)*.

The bytes between the buffer's current position and its limit, if any, are copied to the beginning of the buffer. That is, the byte at index*p* =`position()`is copied to index zero, the byte at index*p* + 1 is copied to index one, and so forth until the byte at index`limit()`- 1 is copied to index*n* =`limit()`-`1`-*p* . The buffer's position is then set to*n+1*and its limit is set to its capacity. The mark, if defined, is discarded.

The buffer's position is set to the number of bytes copied, rather than to zero, so that an invocation of this method can be followed immediately by an invocation of another relative*put*method.

Invoke this method after writing data from a buffer in case the write was incomplete. The following loop, for example, copies bytes from one channel to another via the buffer`buf`: 

```kotlin
<code>buf.clear();          // Prepare buffer for use
    while (in.read(buf) &gt;= 0 || buf.position != 0) {
        buf.flip();
        out.write(buf);
        buf.compact();    // In case of partial write
    }
  </code>
```

| Return ||
|----------------------------------------------------------------------------------|-------------|
| [ByteBuffer](../java/nio/ByteBuffer.md) | This buffer |

| Exceptions ||
|------------------------------------|-----------------------------|
| `java.nio.ReadOnlyBufferException` | If this buffer is read-only |

### duplicate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun duplicate(): ByteBuffer
```

Creates a new byte buffer that shares this buffer's content.

The content of the new buffer will be that of this buffer. Changes to this buffer's content will be visible in the new buffer, and vice versa; the two buffers' position, limit, and mark values will be independent.

The new buffer's capacity, limit, position, and mark values will be identical to those of this buffer, and its byte order will be [BIG_ENDIAN](../java/nio/ByteOrder.md). The new buffer will be direct if, and only if, this buffer is direct, and it will be read-only if, and only if, this buffer is read-only.

| Return ||
|----------------------------------------------------------------------------------|---------------------|
| [ByteBuffer](../java/nio/ByteBuffer.md) | The new byte buffer |

### flip

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun flip(): Buffer
```

Flips this buffer. The limit is set to the current position and then the position is set to zero. If the mark is defined then it is discarded.

After a sequence of channel-read or*put* operations, invoke this method to prepare for a sequence of channel-write or relative*get*operations. For example: 

```kotlin
buf.put(magic);    // Prepend header
  in.read(buf);      // Read data into rest of buffer
  buf.flip();        // Flip buffer
  out.write(buf);    // Write header + data to channel
```

This method is often used in conjunction with the [compact](../java/nio/ByteBuffer.md))method when transferring data from one place to another.

| Return ||
|--------------------------------------------------------------------------|-------------|
| [Buffer](../java/nio/Buffer.md) | This buffer |

### force

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun force(): MappedByteBuffer!
```

Forces any changes made to this buffer's content to be written to the storage device containing the mapped file. The region starts at index zero in this buffer and is`capacity()`bytes.

If the file mapped into this buffer resides on a local storage device then when this method returns it is guaranteed that all changes made to the buffer since it was created, or since this method was last invoked, will have been written to that device.

If the file does not reside on a local device then no such guarantee is made.

If this buffer was not mapped in read/write mode ([java.nio.channels.FileChannel.MapMode#READ_WRITE](../java/nio/channels/FileChannel.MapMode.md)) then invoking this method may have no effect. In particular, the method has no effect for buffers mapped in read-only or private mapping modes. This method may or may not have an effect for implementation-specific mapping modes.

| Return ||
|------------------------------------------------------------------------------------------------|-------------|
| [MappedByteBuffer](../java/nio/MappedByteBuffer.md)! | This buffer |

| Exceptions ||
|--------------------------------|------------------------------------------------------------------------------------------------------|
| `java.io.UncheckedIOException` | If an I/O error occurs writing the buffer's content to the storage device containing the mapped file |

### force

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun force(
    index: Int, 
    length: Int
): MappedByteBuffer!
```

Forces any changes made to a region of this buffer's content to be written to the storage device containing the mapped file. The region starts at the given`index`in this buffer and is`length`bytes.

If the file mapped into this buffer resides on a local storage device then when this method returns it is guaranteed that all changes made to the selected region buffer since it was created, or since this method was last invoked, will have been written to that device. The force operation is free to write bytes that lie outside the specified region, for example to ensure that data blocks of some device-specific granularity are transferred in their entirety.

If the file does not reside on a local device then no such guarantee is made.

If this buffer was not mapped in read/write mode ([java.nio.channels.FileChannel.MapMode#READ_WRITE](../java/nio/channels/FileChannel.MapMode.md)) then invoking this method may have no effect. In particular, the method has no effect for buffers mapped in read-only or private mapping modes. This method may or may not have an effect for implementation-specific mapping modes.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The index of the first byte in the buffer region that is to be written back to storage; must be non-negative and less than`capacity()` |
| `length` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The length of the region in bytes; must be non-negative and no larger than`capacity() - index` |

| Return ||
|------------------------------------------------------------------------------------------------|-------------|
| [MappedByteBuffer](../java/nio/MappedByteBuffer.md)! | This buffer |

| Exceptions ||
|---------------------------------------|------------------------------------------------------------------------------------------------------|
| `java.lang.IndexOutOfBoundsException` | if the preconditions on the index and length do not hold. |
| `java.io.UncheckedIOException` | If an I/O error occurs writing the buffer's content to the storage device containing the mapped file |

### isLoaded

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isLoaded(): Boolean
```

Tells whether or not this buffer's content is resident in physical memory.

A return value of`true`implies that it is highly likely that all of the data in this buffer is resident in physical memory and may therefore be accessed without incurring any virtual-memory page faults or I/O operations. A return value of`false`does not necessarily imply that the buffer's content is not resident in physical memory.

The returned value is a hint, rather than a guarantee, because the underlying operating system may have paged out some of the buffer's data by the time that an invocation of this method returns.

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if it is likely that this buffer's content is resident in physical memory |

### limit

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun limit(newLimit: Int): Buffer
```

Sets this buffer's limit. If the position is larger than the new limit then it is set to the new limit. If the mark is defined and larger than the new limit then it is discarded.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `newLimit` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The new limit value; must be non-negative and no larger than this buffer's capacity |

| Return ||
|--------------------------------------------------------------------------|-------------|
| [Buffer](../java/nio/Buffer.md) | This buffer |

| Exceptions ||
|--------------------------------------|----------------------------------------------|
| `java.lang.IllegalArgumentException` | If the preconditions on`newLimit`do not hold |

### load

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun load(): MappedByteBuffer!
```

Loads this buffer's content into physical memory.

This method makes a best effort to ensure that, when it returns, this buffer's content is resident in physical memory. Invoking this method may cause some number of page faults and I/O operations to occur.

| Return ||
|------------------------------------------------------------------------------------------------|-------------|
| [MappedByteBuffer](../java/nio/MappedByteBuffer.md)! | This buffer |

### mark

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun mark(): Buffer
```

Sets this buffer's mark at its position.

| Return ||
|--------------------------------------------------------------------------|-------------|
| [Buffer](../java/nio/Buffer.md) | This buffer |

### position

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun position(newPosition: Int): Buffer
```

Sets this buffer's position. If the mark is defined and larger than the new position then it is discarded.

| Parameters ||
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `newPosition` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The new position value; must be non-negative and no larger than the current limit |

| Return ||
|--------------------------------------------------------------------------|-------------|
| [Buffer](../java/nio/Buffer.md) | This buffer |

| Exceptions ||
|--------------------------------------|-------------------------------------------------|
| `java.lang.IllegalArgumentException` | If the preconditions on`newPosition`do not hold |

### reset

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun reset(): Buffer
```

Resets this buffer's position to the previously-marked position.

Invoking this method neither changes nor discards the mark's value.

| Return ||
|--------------------------------------------------------------------------|-------------|
| [Buffer](../java/nio/Buffer.md) | This buffer |

| Exceptions ||
|---------------------------------|------------------------------|
| `java.nio.InvalidMarkException` | If the mark has not been set |

### rewind

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun rewind(): Buffer
```

Rewinds this buffer. The position is set to zero and the mark is discarded.

Invoke this method before a sequence of channel-write or*get*operations, assuming that the limit has already been set appropriately. For example: 

```kotlin
out.write(buf);    // Write remaining data
  buf.rewind();      // Rewind buffer
  buf.get(array);    // Copy data into array
```

| Return ||
|--------------------------------------------------------------------------|-------------|
| [Buffer](../java/nio/Buffer.md) | This buffer |

### slice

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun slice(): ByteBuffer
```

Creates a new byte buffer whose content is a shared subsequence of this buffer's content.

The content of the new buffer will start at this buffer's current position. Changes to this buffer's content will be visible in the new buffer, and vice versa; the two buffers' position, limit, and mark values will be independent.

The new buffer's position will be zero, its capacity and its limit will be the number of bytes remaining in this buffer, its mark will be undefined, and its byte order will be [BIG_ENDIAN](../java/nio/ByteOrder.md). The new buffer will be direct if, and only if, this buffer is direct, and it will be read-only if, and only if, this buffer is read-only.

Reading bytes into physical memory by invoking`load()`on the returned buffer, or writing bytes to the storage device by invoking`force()`on the returned buffer, will only act on the sub-range of this buffer that the returned buffer represents, namely`[position(),limit())`.

| Return ||
|----------------------------------------------------------------------------------|---------------------|
| [ByteBuffer](../java/nio/ByteBuffer.md) | The new byte buffer |

### slice

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun slice(
    index: Int, 
    length: Int
): MappedByteBuffer
```

Creates a new byte buffer whose content is a shared subsequence of this buffer's content.

The content of the new buffer will start at position`index`in this buffer, and will contain`length`elements. Changes to this buffer's content will be visible in the new buffer, and vice versa; the two buffers' position, limit, and mark values will be independent.

The new buffer's position will be zero, its capacity and its limit will be`length`, its mark will be undefined, and its byte order will be [BIG_ENDIAN](../java/nio/ByteOrder.md). The new buffer will be direct if, and only if, this buffer is direct, and it will be read-only if, and only if, this buffer is read-only.

Reading bytes into physical memory by invoking`load()`on the returned buffer, or writing bytes to the storage device by invoking`force()`on the returned buffer, will only act on the sub-range of this buffer that the returned buffer represents, namely`[index,index+length)`, where`index`and`length`are assumed to satisfy the preconditions.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The position in this buffer at which the content of the new buffer will start; must be non-negative and no larger than [limit()](../java/nio/Buffer.md)) |
| `length` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The number of elements the new buffer will contain; must be non-negative and no larger than`limit() - index` |

| Return ||
|-----------------------------------------------------------------------------------------------|----------------|
| [MappedByteBuffer](../java/nio/MappedByteBuffer.md) | The new buffer |

| Exceptions ||
|---------------------------------------|-------------------------------------------------------------------------------------------------|
| `java.lang.IndexOutOfBoundsException` | If`index`is negative or greater than`limit()`,`length`is negative, or`length > limit() - index` |
