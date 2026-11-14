Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ByteBuffer

```
abstract class ByteBuffer : Buffer, Comparable<ByteBuffer!>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [java.nio.Buffer](Buffer.md) ||
| | ↳ | [java.nio.ByteBuffer](ByteBuffer.md) |

| Known Direct Subclasses [MappedByteBuffer](MappedByteBuffer.md) |---|---| | [MappedByteBuffer](MappedByteBuffer.md) | A direct byte buffer whose content is a memory-mapped region of a file. | |
| --- | --- | --- | --- | --- | --- | --- |

A byte buffer.

This class defines six categories of operations upon byte buffers:

- Absolute and relative get and put methods that read and write single bytes;
- Absolute and relative get methods that transfer contiguous sequences of bytes from this buffer into an array;
- Absolute and relative put methods that transfer contiguous sequences of bytes from a byte array or some other byte buffer into this buffer;
- Absolute and relative getChar and putChar methods that read and write values of other primitive types, translating them to and from sequences of bytes in a particular byte order;
- Methods for creating * [view buffers](ByteBuffer.md)*, which allow a byte buffer to be viewed as a buffer containing values of some other primitive type; and
- A method for compact a byte buffer.

Byte buffers can be created either by allocate, which allocates space for the buffer's content, or by wrap an existing byte array {#if\[char\]?or string} into a buffer.

## Direct *vs.* non-direct buffers

A byte buffer is either *direct* or *non-direct*. Given a direct byte buffer, the Java virtual machine will make a best effort to perform native I/O operations directly upon it. That is, it will attempt to avoid copying the buffer's content to (or from) an intermediate buffer before (or after) each invocation of one of the underlying operating system's native I/O operations.

A direct byte buffer may be created by invoking the allocateDirect factory method of this class. The buffers returned by this method typically have somewhat higher allocation and deallocation costs than non-direct buffers. The contents of direct buffers may reside outside of the normal garbage-collected heap, and so their impact upon the memory footprint of an application might not be obvious. It is therefore recommended that direct buffers be allocated primarily for large, long-lived buffers that are subject to the underlying system's native I/O operations. In general it is best to allocate direct buffers only when they yield a measurable gain in program performance.

A direct byte buffer may also be created by map a region of a file directly into memory. An implementation of the Java platform may optionally support the creation of direct byte buffers from native code via JNI. If an instance of one of these kinds of buffers refers to an inaccessible region of memory then an attempt to access that region will not change the buffer's content and will cause an unspecified exception to be thrown either at the time of the access or at some later time.

Whether a byte buffer is direct or non-direct may be determined by invoking its isDirect method. This method is provided so that explicit buffer management can be done in performance-critical code.

## Access to binary data

This class defines methods for reading and writing values of all other primitive types, except `boolean`. Primitive values are translated to (or from) sequences of bytes according to the buffer's current byte order, which may be retrieved and modified via the #order methods. Specific byte orders are represented by instances of the ByteOrder class. The initial order of a byte buffer is always `https://developer.android.com/reference/kotlin/java/nio/ByteOrder#BIG_ENDIAN:java.nio.ByteOrder`.

For access to heterogeneous binary data, that is, sequences of values of different types, this class defines a family of absolute and relative *get* and *put* methods for each type. For 32-bit floating-point values, for example, this class defines:

```kotlin
float  <code><a docref="java.nio.ByteBuffer$getFloat()">#getFloat()</a></code>float  <code><a docref="java.nio.ByteBuffer$getFloat(kotlin.Int)">getFloat(int index)</a></code>void  <code><a docref="java.nio.ByteBuffer$putFloat(kotlin.Float)">putFloat(float f)</a></code>void  <code><a docref="java.nio.ByteBuffer$putFloat(kotlin.Int, kotlin.Float)">putFloat(int index, float f)</a></code>
```

Corresponding methods are defined for the types `char, short, int, long`, and `double`. The index parameters of the absolute *get* and *put* methods are in terms of bytes rather than of the type being read or written.

For access to homogeneous binary data, that is, sequences of values of the same type, this class defines methods that can create *views* of a given byte buffer. A *view buffer* is simply another buffer whose content is backed by the byte buffer. Changes to the byte buffer's content will be visible in the view buffer, and vice versa; the two buffers' position, limit, and mark values are independent. The asFloatBuffer method, for example, creates an instance of the FloatBuffer class that is backed by the byte buffer upon which the method is invoked. Corresponding view-creation methods are defined for the types `char, short, int, long`, and `double`.

View buffers have three important advantages over the families of type-specific *get* and *put* methods described above:

- A view buffer is indexed not in terms of bytes but rather in terms of the type-specific size of its values;
- A view buffer provides relative bulk *get* and *put* methods that can transfer contiguous sequences of values between a buffer and an array or some other buffer of the same type; and
- A view buffer is potentially much more efficient because it will be direct if, and only if, its backing byte buffer is direct.

The byte order of a view buffer is fixed to be that of its byte buffer at the time that the view is created.

## Invocation chaining

Methods in this class that do not otherwise have a value to return are specified to return the buffer upon which they are invoked. This allows method invocations to be chained. The sequence of statements

```kotlin
bb.putInt(0xCAFEBABE);
  bb.putShort(3);
  bb.putShort(45);
```
can, for example, be replaced by the single statement

```kotlin
bb.putInt(0xCAFEBABE).putShort(3).putShort(45);
```

## Summary

| Public methods ||
|---|---|
| [ByteBuffer](ByteBuffer.md) | alignedSlice Creates a new byte buffer whose content is a shared and aligned subsequence of this buffer's content. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | alignmentOffset Returns the memory address, pointing to the byte at the given index, modulo the given unit size. |
| open static [ByteBuffer](ByteBuffer.md) | allocate Allocates a new byte buffer. |
| --- | --- |
| open static [ByteBuffer](ByteBuffer.md) | allocateDirect Allocates a new direct byte buffer. |
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html) | array Returns the byte array that backs this buffer *(optional operation)*. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | arrayOffset Returns the offset within this buffer's backing array of the first element of the buffer *(optional operation)*. |
| --- | --- |
| abstract [CharBuffer](CharBuffer.md) | asCharBuffer Creates a view of this byte buffer as a char buffer. |
| abstract [DoubleBuffer](DoubleBuffer.md) | asDoubleBuffer Creates a view of this byte buffer as a double buffer. |
| abstract [FloatBuffer](FloatBuffer.md) | asFloatBuffer Creates a view of this byte buffer as a float buffer. |
| --- | --- |
| abstract [IntBuffer](IntBuffer.md) | asIntBuffer Creates a view of this byte buffer as an int buffer. |
| abstract [LongBuffer](LongBuffer.md) | asLongBuffer Creates a view of this byte buffer as a long buffer. |
| abstract [ByteBuffer](ByteBuffer.md) | asReadOnlyBuffer Creates a new, read-only byte buffer that shares this buffer's content. |
| --- | --- |
| abstract [ShortBuffer](ShortBuffer.md) | asShortBuffer Creates a view of this byte buffer as a short buffer. |
| open [Buffer](Buffer.md) | clear Clears this buffer. |
| abstract [ByteBuffer](ByteBuffer.md) | compact Compacts this buffer *(optional operation)*. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | compareTo Compares this buffer to another. |
| abstract [ByteBuffer](ByteBuffer.md) | duplicate Creates a new byte buffer that shares this buffer's content. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | equals Tells whether or not this buffer is equal to another object. |
| --- | --- |
| open [Buffer](Buffer.md) | flip Flips this buffer. |
| abstract [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | get Relative *get* method. |
| open [ByteBuffer](ByteBuffer.md) | get Relative bulk *get* method. |
| --- | --- |
| open [ByteBuffer](ByteBuffer.md) | get Relative bulk *get* method. |
| abstract [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | get Absolute *get* method. |
| open [ByteBuffer](ByteBuffer.md) | get Absolute bulk *get* method. |
| --- | --- |
| open [ByteBuffer](ByteBuffer.md) | get Absolute bulk *get* method. |
| abstract [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | getChar Relative *get* method for reading a char value. |
| abstract [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | getChar Absolute *get* method for reading a char value. |
| --- | --- |
| abstract [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | getDouble Relative *get* method for reading a double value. |
| abstract [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | getDouble Absolute *get* method for reading a double value. |
| abstract [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | getFloat Relative *get* method for reading a float value. |
| --- | --- |
| abstract [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | getFloat Absolute *get* method for reading a float value. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getInt Relative *get* method for reading an int value. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getInt Absolute *get* method for reading an int value. |
| --- | --- |
| abstract [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | getLong Relative *get* method for reading a long value. |
| abstract [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | getLong Absolute *get* method for reading a long value. |
| abstract [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | getShort Relative *get* method for reading a short value. |
| --- | --- |
| abstract [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | getShort Absolute *get* method for reading a short value. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | hasArray Tells whether or not this buffer is backed by an accessible byte array. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | hashCode Returns the current hash code of this buffer. |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isDirect Tells whether or not this byte buffer is direct. |
| open [Buffer](Buffer.md) | limit Sets this buffer's limit. |
| open [Buffer](Buffer.md) | mark Sets this buffer's mark at its position. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | mismatch Finds and returns the relative index of the first mismatch between this buffer and a given buffer. |
| [ByteOrder](ByteOrder.md) | order Retrieves this buffer's byte order. |
| [ByteBuffer](ByteBuffer.md) | order Modifies this buffer's byte order. |
| --- | --- |
| open [Buffer](Buffer.md) | position Sets this buffer's position. |
| abstract [ByteBuffer](ByteBuffer.md) | put Relative *put* method *(optional operation)*. |
| [ByteBuffer](ByteBuffer.md) | put Relative bulk *put* method *(optional operation)*. |
| --- | --- |
| open [ByteBuffer](ByteBuffer.md) | put Relative bulk *put* method *(optional operation)*. |
| abstract [ByteBuffer](ByteBuffer.md) | put Absolute *put* method *(optional operation)*. |
| open [ByteBuffer](ByteBuffer.md) | put Absolute bulk *put* method *(optional operation)*. |
| --- | --- |
| open [ByteBuffer](ByteBuffer.md) | put Absolute bulk *put* method *(optional operation)*. |
| open [ByteBuffer](ByteBuffer.md) | put Absolute bulk *put* method *(optional operation)*. |
| open [ByteBuffer](ByteBuffer.md) | put Relative bulk *put* method *(optional operation)*. |
| --- | --- |
| abstract [ByteBuffer](ByteBuffer.md) | putChar Relative *put* method for writing a char value *(optional operation)*. |
| abstract [ByteBuffer](ByteBuffer.md) | putChar Absolute *put* method for writing a char value *(optional operation)*. |
| abstract [ByteBuffer](ByteBuffer.md) | putDouble Relative *put* method for writing a double value *(optional operation)*. |
| --- | --- |
| abstract [ByteBuffer](ByteBuffer.md) | putDouble Absolute *put* method for writing a double value *(optional operation)*. |
| abstract [ByteBuffer](ByteBuffer.md) | putFloat Relative *put* method for writing a float value *(optional operation)*. |
| abstract [ByteBuffer](ByteBuffer.md) | putFloat Absolute *put* method for writing a float value *(optional operation)*. |
| --- | --- |
| abstract [ByteBuffer](ByteBuffer.md) | putInt Relative *put* method for writing an int value *(optional operation)*. |
| abstract [ByteBuffer](ByteBuffer.md) | putInt Absolute *put* method for writing an int value *(optional operation)*. |
| abstract [ByteBuffer](ByteBuffer.md) | putLong Absolute *put* method for writing a long value *(optional operation)*. |
| --- | --- |
| abstract [ByteBuffer](ByteBuffer.md) | putLong Relative *put* method for writing a long value *(optional operation)*. |
| abstract [ByteBuffer](ByteBuffer.md) | putShort Absolute *put* method for writing a short value *(optional operation)*. |
| abstract [ByteBuffer](ByteBuffer.md) | putShort Relative *put* method for writing a short value *(optional operation)*. |
| --- | --- |
| open [Buffer](Buffer.md) | reset Resets this buffer's position to the previously-marked position. |
| open [Buffer](Buffer.md) | rewind Rewinds this buffer. |
| abstract [ByteBuffer](ByteBuffer.md) | slice Creates a new byte buffer whose content is a shared subsequence of this buffer's content. |
| --- | --- |
| abstract [ByteBuffer](ByteBuffer.md) | slice Creates a new byte buffer whose content is a shared subsequence of this buffer's content. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | toString Returns a string summarizing the state of this buffer. |
| open static [ByteBuffer](ByteBuffer.md) | wrap Wraps a byte array into a buffer. |
| --- | --- |
| open static [ByteBuffer](ByteBuffer.md) | wrap Wraps a byte array into a buffer. |

| Inherited functions ||
|---|---|
| From class Buffer |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | capacity Returns this buffer's capacity. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | hasRemaining Tells whether there are any elements between the current position and the limit. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | isReadOnly Tells whether or not this buffer is read-only. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | limit Returns this buffer's limit. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | position Returns this buffer's position. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | remaining Returns the number of elements between the current position and the limit. <br /> | ||

## Public methods

### alignedSlice

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun alignedSlice(unitSize: Int): ByteBuffer
```

Creates a new byte buffer whose content is a shared and aligned subsequence of this buffer's content.

The content of the new buffer will start at this buffer's current position rounded up to the index of the nearest aligned byte for the given unit size, and end at this buffer's limit rounded down to the index of the nearest aligned byte for the given unit size. If rounding results in out-of-bound values then the new buffer's capacity and limit will be zero. If rounding is within bounds the following expressions will be true for a new buffer `nb` and unit size `unitSize`:

```kotlin
<code>nb.alignmentOffset(0, unitSize) == 0
  nb.alignmentOffset(nb.limit(), unitSize) == 0
  </code>
```

Changes to this buffer's content will be visible in the new buffer, and vice versa; the two buffers' position, limit, and mark values will be independent.

The new buffer's position will be zero, its capacity and its limit will be the number of bytes remaining in this buffer or fewer subject to alignment, its mark will be undefined, and its byte order will be `https://developer.android.com/reference/kotlin/java/nio/ByteOrder#BIG_ENDIAN:java.nio.ByteOrder`. The new buffer will be direct if, and only if, this buffer is direct, and it will be read-only if, and only if, this buffer is read-only.

| Parameters ||
|---|---|
| `unitSize` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The unit size in bytes, must be a power of `2` |

| Return ||
|---|---|
| ByteBuffer | The new byte buffer |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | If the unit size not a power of `2` |
| `java.lang.UnsupportedOperationException` | If the native platform does not guarantee stable aligned slices for the given unit size when managing the memory regions of buffers of the same kind as this buffer (direct or non-direct). For example, if garbage collection would result in the moving of a memory region covered by a non-direct buffer from one location to another and both locations have different alignment characteristics. |

**See Also**

- alignmentOffset
- slice

### alignmentOffset

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun alignmentOffset(
    index: Int, 
    unitSize: Int
): Int
```

Returns the memory address, pointing to the byte at the given index, modulo the given unit size.

The return value is non-negative in the range of `0` (inclusive) up to `unitSize` (exclusive), with zero indicating that the address of the byte at the index is aligned for the unit size, and a positive value that the address is misaligned for the unit size. If the address of the byte at the index is misaligned, the return value represents how much the index should be adjusted to locate a byte at an aligned address. Specifically, the index should either be decremented by the return value if the latter is not greater than `index`, or be incremented by the unit size minus the return value. Therefore given

```kotlin
int value = alignmentOffset(index, unitSize)
```
then the identities

```kotlin
alignmentOffset(index - value, unitSize) == 0, value ≤ index
```
and

```kotlin
alignmentOffset(index + (unitSize - value), unitSize) == 0
```
must hold.

| Parameters ||
|---|---|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The index to query for alignment offset, must be non-negative, no upper bounds check is performed |
| `unitSize` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The unit size in bytes, must be a power of `2` |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The indexed byte's memory address modulo the unit size |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | If the index is negative or the unit size is not a power of `2` |
| `java.lang.UnsupportedOperationException` | If the native platform does not guarantee stable alignment offset values for the given unit size when managing the memory regions of buffers of the same kind as this buffer (direct or non-direct). For example, if garbage collection would result in the moving of a memory region covered by a non-direct buffer from one location to another and both locations have different alignment characteristics. |

**See Also**

- alignedSlice

### allocate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun allocate(capacity: Int): ByteBuffer
```

Allocates a new byte buffer.

The new buffer's position will be zero, its limit will be its capacity, its mark will be undefined, each of its elements will be initialized to zero, and its byte order will be `https://developer.android.com/reference/kotlin/java/nio/ByteOrder#BIG_ENDIAN:java.nio.ByteOrder`. It will have a array, and its arrayOffset will be zero.

| Parameters ||
|---|---|
| `capacity` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The new buffer's capacity, in bytes |

| Return ||
|---|---|
| ByteBuffer | The new byte buffer |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | If the `capacity` is a negative integer |

### allocateDirect

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun allocateDirect(capacity: Int): ByteBuffer
```

Allocates a new direct byte buffer.

The new buffer's position will be zero, its limit will be its capacity, its mark will be undefined, each of its elements will be initialized to zero, and its byte order will be `https://developer.android.com/reference/kotlin/java/nio/ByteOrder#BIG_ENDIAN:java.nio.ByteOrder`. Whether or not it has a hasArray is unspecified.

| Parameters ||
|---|---|
| `capacity` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The new buffer's capacity, in bytes |

| Return ||
|---|---|
| ByteBuffer | The new byte buffer |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | If the `capacity` is a negative integer |

### array

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun array(): ByteArray
```

Returns the byte array that backs this buffer *(optional operation)*.

Modifications to this buffer's content will cause the returned array's content to be modified, and vice versa.

Invoke the hasArray method before invoking this method in order to ensure that this buffer has an accessible backing array.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html` | The array that backs this buffer |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | If this buffer is not backed by an accessible array |
| `java.nio.ReadOnlyBufferException` | If this buffer is backed by an array but is read-only |

### arrayOffset

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun arrayOffset(): Int
```

Returns the offset within this buffer's backing array of the first element of the buffer *(optional operation)*.

If this buffer is backed by an array then buffer position *p* corresponds to array index *p* + `arrayOffset()`.

Invoke the hasArray method before invoking this method in order to ensure that this buffer has an accessible backing array.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The offset within this buffer's array of the first element of the buffer |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | If this buffer is not backed by an accessible array |
| `java.nio.ReadOnlyBufferException` | If this buffer is backed by an array but is read-only |

### asCharBuffer

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun asCharBuffer(): CharBuffer
```

Creates a view of this byte buffer as a char buffer.

The content of the new buffer will start at this buffer's current position. Changes to this buffer's content will be visible in the new buffer, and vice versa; the two buffers' position, limit, and mark values will be independent.

The new buffer's position will be zero, its capacity and its limit will be the number of bytes remaining in this buffer divided by two, its mark will be undefined, and its byte order will be that of the byte buffer at the moment the view is created. The new buffer will be direct if, and only if, this buffer is direct, and it will be read-only if, and only if, this buffer is read-only.

| Return ||
|---|---|
| CharBuffer | A new char buffer |

### asDoubleBuffer

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun asDoubleBuffer(): DoubleBuffer
```

Creates a view of this byte buffer as a double buffer.

The content of the new buffer will start at this buffer's current position. Changes to this buffer's content will be visible in the new buffer, and vice versa; the two buffers' position, limit, and mark values will be independent.

The new buffer's position will be zero, its capacity and its limit will be the number of bytes remaining in this buffer divided by eight, its mark will be undefined, and its byte order will be that of the byte buffer at the moment the view is created. The new buffer will be direct if, and only if, this buffer is direct, and it will be read-only if, and only if, this buffer is read-only.

| Return ||
|---|---|
| DoubleBuffer | A new double buffer |

### asFloatBuffer

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun asFloatBuffer(): FloatBuffer
```

Creates a view of this byte buffer as a float buffer.

The content of the new buffer will start at this buffer's current position. Changes to this buffer's content will be visible in the new buffer, and vice versa; the two buffers' position, limit, and mark values will be independent.

The new buffer's position will be zero, its capacity and its limit will be the number of bytes remaining in this buffer divided by four, its mark will be undefined, and its byte order will be that of the byte buffer at the moment the view is created. The new buffer will be direct if, and only if, this buffer is direct, and it will be read-only if, and only if, this buffer is read-only.

| Return ||
|---|---|
| FloatBuffer | A new float buffer |

### asIntBuffer

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun asIntBuffer(): IntBuffer
```

Creates a view of this byte buffer as an int buffer.

The content of the new buffer will start at this buffer's current position. Changes to this buffer's content will be visible in the new buffer, and vice versa; the two buffers' position, limit, and mark values will be independent.

The new buffer's position will be zero, its capacity and its limit will be the number of bytes remaining in this buffer divided by four, its mark will be undefined, and its byte order will be that of the byte buffer at the moment the view is created. The new buffer will be direct if, and only if, this buffer is direct, and it will be read-only if, and only if, this buffer is read-only.

| Return ||
|---|---|
| IntBuffer | A new int buffer |

### asLongBuffer

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun asLongBuffer(): LongBuffer
```

Creates a view of this byte buffer as a long buffer.

The content of the new buffer will start at this buffer's current position. Changes to this buffer's content will be visible in the new buffer, and vice versa; the two buffers' position, limit, and mark values will be independent.

The new buffer's position will be zero, its capacity and its limit will be the number of bytes remaining in this buffer divided by eight, its mark will be undefined, and its byte order will be that of the byte buffer at the moment the view is created. The new buffer will be direct if, and only if, this buffer is direct, and it will be read-only if, and only if, this buffer is read-only.

| Return ||
|---|---|
| LongBuffer | A new long buffer |

### asReadOnlyBuffer

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun asReadOnlyBuffer(): ByteBuffer
```

Creates a new, read-only byte buffer that shares this buffer's content.

The content of the new buffer will be that of this buffer. Changes to this buffer's content will be visible in the new buffer; the new buffer itself, however, will be read-only and will not allow the shared content to be modified. The two buffers' position, limit, and mark values will be independent.

The new buffer's capacity, limit, position, and mark values will be identical to those of this buffer, and its byte order will be `https://developer.android.com/reference/kotlin/java/nio/ByteOrder#BIG_ENDIAN:java.nio.ByteOrder`.

If this buffer is itself read-only then this method behaves in exactly the same way as the duplicate method.

| Return ||
|---|---|
| ByteBuffer | The new, read-only byte buffer |

### asShortBuffer

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun asShortBuffer(): ShortBuffer
```

Creates a view of this byte buffer as a short buffer.

The content of the new buffer will start at this buffer's current position. Changes to this buffer's content will be visible in the new buffer, and vice versa; the two buffers' position, limit, and mark values will be independent.

The new buffer's position will be zero, its capacity and its limit will be the number of bytes remaining in this buffer divided by two, its mark will be undefined, and its byte order will be that of the byte buffer at the moment the view is created. The new buffer will be direct if, and only if, this buffer is direct, and it will be read-only if, and only if, this buffer is read-only.

| Return ||
|---|---|
| ShortBuffer | A new short buffer |

### clear

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun clear(): Buffer
```

Clears this buffer. The position is set to zero, the limit is set to the capacity, and the mark is discarded.

Invoke this method before using a sequence of channel-read or *put* operations to fill this buffer. For example:

```kotlin
buf.clear();     // Prepare buffer for reading
  in.read(buf);    // Read data
```

This method does not actually erase the data in the buffer, but it is named as if it did because it will most often be used in situations in which that might as well be the case.

| Return ||
|---|---|
| Buffer | This buffer |

### compact

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun compact(): ByteBuffer
```

Compacts this buffer *(optional operation)*.

The bytes between the buffer's current position and its limit, if any, are copied to the beginning of the buffer. That is, the byte at index *p* = `position()` is copied to index zero, the byte at index *p* + 1 is copied to index one, and so forth until the byte at index `limit()` - 1 is copied to index *n* = `limit()` - `1` - *p* . The buffer's position is then set to *n+1* and its limit is set to its capacity. The mark, if defined, is discarded.

The buffer's position is set to the number of bytes copied, rather than to zero, so that an invocation of this method can be followed immediately by an invocation of another relative *put* method.

Invoke this method after writing data from a buffer in case the write was incomplete. The following loop, for example, copies bytes from one channel to another via the buffer `buf`:

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
|---|---|
| ByteBuffer | This buffer |

| Exceptions ||
|---|---|
| `java.nio.ReadOnlyBufferException` | If this buffer is read-only |

### compareTo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun compareTo(other: ByteBuffer): Int
```

Compares this buffer to another.

Two byte buffers are compared by comparing their sequences of remaining elements lexicographically, without regard to the starting position of each sequence within its corresponding buffer. Pairs of `byte` elements are compared as if by invoking compare.

A byte buffer is not comparable to any other type of object.

| Parameters ||
|---|---|
| `o` | the object to be compared. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | A negative integer, zero, or a positive integer as this buffer is less than, equal to, or greater than the given buffer |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the specified object's type prevents it from being compared to this object. |
| `java.lang.NullPointerException` | if the specified object is null |

### duplicate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun duplicate(): ByteBuffer
```

Creates a new byte buffer that shares this buffer's content.

The content of the new buffer will be that of this buffer. Changes to this buffer's content will be visible in the new buffer, and vice versa; the two buffers' position, limit, and mark values will be independent.

The new buffer's capacity, limit, position, and mark values will be identical to those of this buffer, and its byte order will be `https://developer.android.com/reference/kotlin/java/nio/ByteOrder#BIG_ENDIAN:java.nio.ByteOrder`. The new buffer will be direct if, and only if, this buffer is direct, and it will be read-only if, and only if, this buffer is read-only.

| Return ||
|---|---|
| ByteBuffer | The new byte buffer |

### equals

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun equals(other: Any?): Boolean
```

Tells whether or not this buffer is equal to another object.

Two byte buffers are equal if, and only if,

1. They have the same element type,
2. They have the same number of remaining elements, and
3. The two sequences of remaining elements, considered independently of their starting positions, are pointwise equal.

A byte buffer is not equal to any other type of object.

| Parameters ||
|---|---|
| `obj` | the reference object with which to compare. |
| `ob` | The object to which this buffer is to be compared |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if, and only if, this buffer is equal to the given object |

### flip

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun flip(): Buffer
```

Flips this buffer. The limit is set to the current position and then the position is set to zero. If the mark is defined then it is discarded.

After a sequence of channel-read or *put* operations, invoke this method to prepare for a sequence of channel-write or relative *get* operations. For example:

```kotlin
buf.put(magic);    // Prepend header
  in.read(buf);      // Read data into rest of buffer
  buf.flip();        // Flip buffer
  out.write(buf);    // Write header + data to channel
```

This method is often used in conjunction with the compact method when transferring data from one place to another.

| Return ||
|---|---|
| Buffer | This buffer |

### get

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun get(): Byte
```

Relative *get* method. Reads the byte at this buffer's current position, and then increments the position.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html` | The byte at the buffer's current position |

| Exceptions ||
|---|---|
| `java.nio.BufferUnderflowException` | If the buffer's current position is not smaller than its limit |

### get

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun get(dst: ByteArray): ByteBuffer
```

Relative bulk *get* method.

This method transfers bytes from this buffer into the given destination array. An invocation of this method of the form `src.get(a)` behaves in exactly the same way as the invocation

```kotlin
src.get(a, 0, a.length) 
```

| Parameters ||
|---|---|
| `dst` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html): The destination array |

| Return ||
|---|---|
| ByteBuffer | This buffer |

| Exceptions ||
|---|---|
| `java.nio.BufferUnderflowException` | If there are fewer than `length` bytes remaining in this buffer |

### get

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun get(
    dst: ByteArray, 
    offset: Int, 
    length: Int
): ByteBuffer
```

Relative bulk *get* method.

This method transfers bytes from this buffer into the given destination array. If there are fewer bytes remaining in the buffer than are required to satisfy the request, that is, if `length` `>` `remaining()`, then no bytes are transferred and a BufferUnderflowException is thrown.

Otherwise, this method copies `length` bytes from this buffer into the given array, starting at the current position of this buffer and at the given offset in the array. The position of this buffer is then incremented by `length`.

In other words, an invocation of this method of the form `src.get(dst, off, len)` has exactly the same effect as the loop

```kotlin
<code>for (int i = off; i &lt; off + len; i++)
          dst[i] = src.get();
  </code>
```
except that it first checks that there are sufficient bytes in this buffer and it is potentially much more efficient.

| Parameters ||
|---|---|
| `dst` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html): The array into which bytes are to be written |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The offset within the array of the first byte to be written; must be non-negative and no larger than `dst.length` |
| `length` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The maximum number of bytes to be written to the given array; must be non-negative and no larger than `dst.length - offset` |
| --- | --- |

| Return ||
|---|---|
| ByteBuffer | This buffer |

| Exceptions ||
|---|---|
| `java.lang.IndexOutOfBoundsException` | If the preconditions on the `offset` and `length` parameters do not hold |
| `java.nio.BufferUnderflowException` | If there are fewer than `length` bytes remaining in this buffer |

### get

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun get(index: Int): Byte
```

Absolute *get* method. Reads the byte at the given index.

| Parameters ||
|---|---|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The index from which the byte will be read |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html` | The byte at the given index |

| Exceptions ||
|---|---|
| `java.lang.IndexOutOfBoundsException` | If `index` is negative or not smaller than the buffer's limit |

### get

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun get(
    index: Int, 
    dst: ByteArray
): ByteBuffer
```

Absolute bulk *get* method.

This method transfers bytes from this buffer into the given destination array. The position of this buffer is unchanged. An invocation of this method of the form `src.get(index, dst)` behaves in exactly the same way as the invocation:

```kotlin
src.get(index, dst, 0, dst.length) 
```

| Parameters ||
|---|---|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The index in this buffer from which the first byte will be read; must be non-negative and less than `limit()` |
| `dst` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html): The destination array |

| Return ||
|---|---|
| ByteBuffer | This buffer |

| Exceptions ||
|---|---|
| `java.lang.IndexOutOfBoundsException` | If `index` is negative, not smaller than `limit()`, or `limit() - index < dst.length` |

### get

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun get(
    index: Int, 
    dst: ByteArray, 
    offset: Int, 
    length: Int
): ByteBuffer
```

Absolute bulk *get* method.

This method transfers `length` bytes from this buffer into the given array, starting at the given index in this buffer and at the given offset in the array. The position of this buffer is unchanged.

An invocation of this method of the form `src.get(index, dst, offset, length)` has exactly the same effect as the following loop except that it first checks the consistency of the supplied parameters and it is potentially much more efficient:

```kotlin
<code>for (int i = offset, j = index; i &lt; offset + length; i++, j++)
          dst[i] = src.get(j);
  </code>
```

| Parameters ||
|---|---|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The index in this buffer from which the first byte will be read; must be non-negative and less than `limit()` |
| `dst` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html): The destination array |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The offset within the array of the first byte to be written; must be non-negative and less than `dst.length` |
| --- | --- |
| `length` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The number of bytes to be written to the given array; must be non-negative and no larger than the smaller of `limit() - index` and `dst.length - offset` |

| Return ||
|---|---|
| ByteBuffer | This buffer |

| Exceptions ||
|---|---|
| `java.lang.IndexOutOfBoundsException` | If the preconditions on the `index`, `offset`, and `length` parameters do not hold |

### getChar

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getChar(): Char
```

Relative *get* method for reading a char value.

Reads the next two bytes at this buffer's current position, composing them into a char value according to the current byte order, and then increments the position by two.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html` | The char value at the buffer's current position |

| Exceptions ||
|---|---|
| `java.nio.BufferUnderflowException` | If there are fewer than two bytes remaining in this buffer |

### getChar

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getChar(index: Int): Char
```

Absolute *get* method for reading a char value.

Reads two bytes at the given index, composing them into a char value according to the current byte order.

| Parameters ||
|---|---|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The index from which the bytes will be read |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html` | The char value at the given index |

| Exceptions ||
|---|---|
| `java.lang.IndexOutOfBoundsException` | If `index` is negative or not smaller than the buffer's limit, minus one |

### getDouble

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getDouble(): Double
```

Relative *get* method for reading a double value.

Reads the next eight bytes at this buffer's current position, composing them into a double value according to the current byte order, and then increments the position by eight.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html` | The double value at the buffer's current position |

| Exceptions ||
|---|---|
| `java.nio.BufferUnderflowException` | If there are fewer than eight bytes remaining in this buffer |

### getDouble

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getDouble(index: Int): Double
```

Absolute *get* method for reading a double value.

Reads eight bytes at the given index, composing them into a double value according to the current byte order.

| Parameters ||
|---|---|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The index from which the bytes will be read |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html` | The double value at the given index |

| Exceptions ||
|---|---|
| `java.lang.IndexOutOfBoundsException` | If `index` is negative or not smaller than the buffer's limit, minus seven |

### getFloat

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getFloat(): Float
```

Relative *get* method for reading a float value.

Reads the next four bytes at this buffer's current position, composing them into a float value according to the current byte order, and then increments the position by four.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | The float value at the buffer's current position |

| Exceptions ||
|---|---|
| `java.nio.BufferUnderflowException` | If there are fewer than four bytes remaining in this buffer |

### getFloat

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getFloat(index: Int): Float
```

Absolute *get* method for reading a float value.

Reads four bytes at the given index, composing them into a float value according to the current byte order.

| Parameters ||
|---|---|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The index from which the bytes will be read |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | The float value at the given index |

| Exceptions ||
|---|---|
| `java.lang.IndexOutOfBoundsException` | If `index` is negative or not smaller than the buffer's limit, minus three |

### getInt

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getInt(): Int
```

Relative *get* method for reading an int value.

Reads the next four bytes at this buffer's current position, composing them into an int value according to the current byte order, and then increments the position by four.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The int value at the buffer's current position |

| Exceptions ||
|---|---|
| `java.nio.BufferUnderflowException` | If there are fewer than four bytes remaining in this buffer |

### getInt

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getInt(index: Int): Int
```

Absolute *get* method for reading an int value.

Reads four bytes at the given index, composing them into a int value according to the current byte order.

| Parameters ||
|---|---|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The index from which the bytes will be read |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The int value at the given index |

| Exceptions ||
|---|---|
| `java.lang.IndexOutOfBoundsException` | If `index` is negative or not smaller than the buffer's limit, minus three |

### getLong

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getLong(): Long
```

Relative *get* method for reading a long value.

Reads the next eight bytes at this buffer's current position, composing them into a long value according to the current byte order, and then increments the position by eight.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | The long value at the buffer's current position |

| Exceptions ||
|---|---|
| `java.nio.BufferUnderflowException` | If there are fewer than eight bytes remaining in this buffer |

### getLong

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getLong(index: Int): Long
```

Absolute *get* method for reading a long value.

Reads eight bytes at the given index, composing them into a long value according to the current byte order.

| Parameters ||
|---|---|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The index from which the bytes will be read |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | The long value at the given index |

| Exceptions ||
|---|---|
| `java.lang.IndexOutOfBoundsException` | If `index` is negative or not smaller than the buffer's limit, minus seven |

### getShort

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getShort(): Short
```

Relative *get* method for reading a short value.

Reads the next two bytes at this buffer's current position, composing them into a short value according to the current byte order, and then increments the position by two.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html` | The short value at the buffer's current position |

| Exceptions ||
|---|---|
| `java.nio.BufferUnderflowException` | If there are fewer than two bytes remaining in this buffer |

### getShort

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getShort(index: Int): Short
```

Absolute *get* method for reading a short value.

Reads two bytes at the given index, composing them into a short value according to the current byte order.

| Parameters ||
|---|---|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The index from which the bytes will be read |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html` | The short value at the given index |

| Exceptions ||
|---|---|
| `java.lang.IndexOutOfBoundsException` | If `index` is negative or not smaller than the buffer's limit, minus one |

### hasArray

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hasArray(): Boolean
```

Tells whether or not this buffer is backed by an accessible byte array.

If this method returns `true` then the array and arrayOffset methods may safely be invoked.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if, and only if, this buffer is backed by an array and is not read-only |

### hashCode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun hashCode(): Int
```

Returns the current hash code of this buffer.

The hash code of a byte buffer depends only upon its remaining elements; that is, upon the elements from `position()` up to, and including, the element at `limit()` - `1`.

Because buffer hash codes are content-dependent, it is inadvisable to use buffers as keys in hash maps or similar data structures unless it is known that their contents will not change.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The current hash code of this buffer |

### isDirect

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun isDirect(): Boolean
```

Tells whether or not this byte buffer is direct.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if, and only if, this buffer is direct |

### limit

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun limit(newLimit: Int): Buffer
```

Sets this buffer's limit. If the position is larger than the new limit then it is set to the new limit. If the mark is defined and larger than the new limit then it is discarded.

| Parameters ||
|---|---|
| `newLimit` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The new limit value; must be non-negative and no larger than this buffer's capacity |

| Return ||
|---|---|
| Buffer | This buffer |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | If the preconditions on `newLimit` do not hold |

### mark

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun mark(): Buffer
```

Sets this buffer's mark at its position.

| Return ||
|---|---|
| Buffer | This buffer |

### mismatch

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun mismatch(that: ByteBuffer): Int
```

Finds and returns the relative index of the first mismatch between this buffer and a given buffer. The index is relative to the position of each buffer and will be in the range of 0 (inclusive) up to the smaller of the remaining elements in each buffer (exclusive).

If the two buffers share a common prefix then the returned index is the length of the common prefix and it follows that there is a mismatch between the two buffers at that index within the respective buffers. If one buffer is a proper prefix of the other then the returned index is the smaller of the remaining elements in each buffer, and it follows that the index is only valid for the buffer with the larger number of remaining elements. Otherwise, there is no mismatch.

| Parameters ||
|---|---|
| `that` | [ByteBuffer](ByteBuffer.md): The byte buffer to be tested for a mismatch with this buffer |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The relative index of the first mismatch between this and the given buffer, otherwise -1 if no mismatch. |

### order

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun order(): ByteOrder
```

Retrieves this buffer's byte order.

The byte order is used when reading or writing multibyte values, and when creating buffers that are views of this byte buffer. The order of a newly-created byte buffer is always `https://developer.android.com/reference/kotlin/java/nio/ByteOrder#BIG_ENDIAN:java.nio.ByteOrder`.

| Return ||
|---|---|
| ByteOrder | This buffer's byte order |

### order

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun order(bo: ByteOrder): ByteBuffer
```

Modifies this buffer's byte order.

| Parameters ||
|---|---|
| `bo` | [ByteOrder](ByteOrder.md): The new byte order, either `https://developer.android.com/reference/kotlin/java/nio/ByteOrder#BIG_ENDIAN:java.nio.ByteOrder` or `https://developer.android.com/reference/kotlin/java/nio/ByteOrder#LITTLE_ENDIAN:java.nio.ByteOrder` |

| Return ||
|---|---|
| ByteBuffer | This buffer |

### position

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun position(newPosition: Int): Buffer
```

Sets this buffer's position. If the mark is defined and larger than the new position then it is discarded.

| Parameters ||
|---|---|
| `newPosition` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The new position value; must be non-negative and no larger than the current limit |

| Return ||
|---|---|
| Buffer | This buffer |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | If the preconditions on `newPosition` do not hold |

### put

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun put(b: Byte): ByteBuffer
```

Relative *put* method *(optional operation)*.

Writes the given byte into this buffer at the current position, and then increments the position.

| Parameters ||
|---|---|
| `b` | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html): The byte to be written |

| Return ||
|---|---|
| ByteBuffer | This buffer |

| Exceptions ||
|---|---|
| `java.nio.BufferOverflowException` | If this buffer's current position is not smaller than its limit |
| `java.nio.ReadOnlyBufferException` | If this buffer is read-only |

### put

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun put(src: ByteArray): ByteBuffer
```

Relative bulk *put* method *(optional operation)*.

This method transfers the entire content of the given source byte array into this buffer. An invocation of this method of the form `dst.put(a)` behaves in exactly the same way as the invocation

```kotlin
dst.put(a, 0, a.length) 
```

| Parameters ||
|---|---|
| `src` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html): The source array |

| Return ||
|---|---|
| ByteBuffer | This buffer |

| Exceptions ||
|---|---|
| `java.nio.BufferOverflowException` | If there is insufficient space in this buffer |
| `java.nio.ReadOnlyBufferException` | If this buffer is read-only |

### put

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun put(
    src: ByteArray, 
    offset: Int, 
    length: Int
): ByteBuffer
```

Relative bulk *put* method *(optional operation)*.

This method transfers bytes into this buffer from the given source array. If there are more bytes to be copied from the array than remain in this buffer, that is, if `length` `>` `remaining()`, then no bytes are transferred and a BufferOverflowException is thrown.

Otherwise, this method copies `length` bytes from the given array into this buffer, starting at the given offset in the array and at the current position of this buffer. The position of this buffer is then incremented by `length`.

In other words, an invocation of this method of the form `dst.put(src, off, len)` has exactly the same effect as the loop

```kotlin
<code>for (int i = off; i &lt; off + len; i++)
          dst.put(src[i]);
  </code>
```
except that it first checks that there is sufficient space in this buffer and it is potentially much more efficient.

| Parameters ||
|---|---|
| `src` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html): The array from which bytes are to be read |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The offset within the array of the first byte to be read; must be non-negative and no larger than `src.length` |
| `length` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The number of bytes to be read from the given array; must be non-negative and no larger than `src.length - offset` |
| --- | --- |

| Return ||
|---|---|
| ByteBuffer | This buffer |

| Exceptions ||
|---|---|
| `java.lang.IndexOutOfBoundsException` | If the preconditions on the `offset` and `length` parameters do not hold |
| `java.nio.BufferOverflowException` | If there is insufficient space in this buffer |
| `java.nio.ReadOnlyBufferException` | If this buffer is read-only |
| --- | --- |

### put

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun put(
    index: Int, 
    b: Byte
): ByteBuffer
```

Absolute *put* method *(optional operation)*.

Writes the given byte into this buffer at the given index.

| Parameters ||
|---|---|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The index at which the byte will be written |
| `b` | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html): The byte value to be written |

| Return ||
|---|---|
| ByteBuffer | This buffer |

| Exceptions ||
|---|---|
| `java.lang.IndexOutOfBoundsException` | If `index` is negative or not smaller than the buffer's limit |
| `java.nio.ReadOnlyBufferException` | If this buffer is read-only |

### put

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun put(
    index: Int, 
    src: ByteArray
): ByteBuffer
```

Absolute bulk *put* method *(optional operation)*.

This method copies bytes into this buffer from the given source array. The position of this buffer is unchanged. An invocation of this method of the form `dst.put(index, src)` behaves in exactly the same way as the invocation:

```kotlin
dst.put(index, src, 0, src.length); 
```

| Parameters ||
|---|---|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The index in this buffer at which the first byte will be written; must be non-negative and less than `limit()` |
| `src` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html): The array from which bytes are to be read |

| Return ||
|---|---|
| ByteBuffer | This buffer |

| Exceptions ||
|---|---|
| `java.lang.IndexOutOfBoundsException` | If `index` is negative, not smaller than `limit()`, or `limit() - index < src.length` |
| `java.nio.ReadOnlyBufferException` | If this buffer is read-only |

### put

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun put(
    index: Int, 
    src: ByteArray, 
    offset: Int, 
    length: Int
): ByteBuffer
```

Absolute bulk *put* method *(optional operation)*.

This method transfers `length` bytes from the given array, starting at the given offset in the array and at the given index in this buffer. The position of this buffer is unchanged.

An invocation of this method of the form `dst.put(index, src, offset, length)` has exactly the same effect as the following loop except that it first checks the consistency of the supplied parameters and it is potentially much more efficient:

```kotlin
<code>for (int i = offset, j = index; i &lt; offset + length; i++, j++)
          dst.put(j, src[i]);
  </code>
```

| Parameters ||
|---|---|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The index in this buffer at which the first byte will be written; must be non-negative and less than `limit()` |
| `src` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html): The array from which bytes are to be read |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The offset within the array of the first byte to be read; must be non-negative and less than `src.length` |
| --- | --- |
| `length` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The number of bytes to be read from the given array; must be non-negative and no larger than the smaller of `limit() - index` and `src.length - offset` |

| Return ||
|---|---|
| ByteBuffer | This buffer |

| Exceptions ||
|---|---|
| `java.lang.IndexOutOfBoundsException` | If the preconditions on the `index`, `offset`, and `length` parameters do not hold |
| `java.nio.ReadOnlyBufferException` | If this buffer is read-only |

### put

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun put(
    index: Int, 
    src: ByteBuffer, 
    offset: Int, 
    length: Int
): ByteBuffer
```

Absolute bulk *put* method *(optional operation)*.

This method transfers `length` bytes into this buffer from the given source buffer, starting at the given `offset` in the source buffer and the given `index` in this buffer. The positions of both buffers are unchanged.

In other words, an invocation of this method of the form `dst.put(index, src, offset, length)` has exactly the same effect as the loop

```kotlin
<code>for (int i = offset, j = index; i &lt; offset + length; i++, j++)
      dst.put(j, src.get(i));
  </code>
```
except that it first checks the consistency of the supplied parameters and it is potentially much more efficient. If this buffer and the source buffer share the same backing array or memory, then the result will be as if the source elements were first copied to an intermediate location before being written into this buffer.

| Parameters ||
|---|---|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The index in this buffer at which the first byte will be written; must be non-negative and less than `limit()` |
| `src` | [ByteBuffer](ByteBuffer.md): The buffer from which bytes are to be read |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The index within the source buffer of the first byte to be read; must be non-negative and less than `src.limit()` |
| --- | --- |
| `length` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The number of bytes to be read from the given buffer; must be non-negative and no larger than the smaller of `limit() - index` and `src.limit() - offset` |

| Return ||
|---|---|
| ByteBuffer | This buffer |

| Exceptions ||
|---|---|
| `java.lang.IndexOutOfBoundsException` | If the preconditions on the `index`, `offset`, and `length` parameters do not hold |
| `java.nio.ReadOnlyBufferException` | If this buffer is read-only |

### put

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun put(src: ByteBuffer): ByteBuffer
```

Relative bulk *put* method *(optional operation)*.

This method transfers the bytes remaining in the given source buffer into this buffer. If there are more bytes remaining in the source buffer than in this buffer, that is, if `src.remaining()` `>` `remaining()`, then no bytes are transferred and a BufferOverflowException is thrown.

Otherwise, this method copies *n* = `src.remaining()` bytes from the given buffer into this buffer, starting at each buffer's current position. The positions of both buffers are then incremented by *n*.

In other words, an invocation of this method of the form `dst.put(src)` has exactly the same effect as the loop

```kotlin
while (src.hasRemaining())
          dst.put(src.get()); 
```
except that it first checks that there is sufficient space in this buffer and it is potentially much more efficient. If this buffer and the source buffer share the same backing array or memory, then the result will be as if the source elements were first copied to an intermediate location before being written into this buffer.

| Parameters ||
|---|---|
| `src` | [ByteBuffer](ByteBuffer.md): The source buffer from which bytes are to be read; must not be this buffer |

| Return ||
|---|---|
| ByteBuffer | This buffer |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | If the source buffer is this buffer |
| `java.nio.BufferOverflowException` | If there is insufficient space in this buffer for the remaining bytes in the source buffer |
| `java.nio.ReadOnlyBufferException` | If this buffer is read-only |
| --- | --- |

### putChar

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun putChar(value: Char): ByteBuffer
```

Relative *put* method for writing a char value *(optional operation)*.

Writes two bytes containing the given char value, in the current byte order, into this buffer at the current position, and then increments the position by two.

| Parameters ||
|---|---|
| `value` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html): The char value to be written |

| Return ||
|---|---|
| ByteBuffer | This buffer |

| Exceptions ||
|---|---|
| `java.nio.BufferOverflowException` | If there are fewer than two bytes remaining in this buffer |
| `java.nio.ReadOnlyBufferException` | If this buffer is read-only |

### putChar

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun putChar(
    index: Int, 
    value: Char
): ByteBuffer
```

Absolute *put* method for writing a char value *(optional operation)*.

Writes two bytes containing the given char value, in the current byte order, into this buffer at the given index.

| Parameters ||
|---|---|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The index at which the bytes will be written |
| `value` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html): The char value to be written |

| Return ||
|---|---|
| ByteBuffer | This buffer |

| Exceptions ||
|---|---|
| `java.lang.IndexOutOfBoundsException` | If `index` is negative or not smaller than the buffer's limit, minus one |
| `java.nio.ReadOnlyBufferException` | If this buffer is read-only |

### putDouble

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun putDouble(value: Double): ByteBuffer
```

Relative *put* method for writing a double value *(optional operation)*.

Writes eight bytes containing the given double value, in the current byte order, into this buffer at the current position, and then increments the position by eight.

| Parameters ||
|---|---|
| `value` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html): The double value to be written |

| Return ||
|---|---|
| ByteBuffer | This buffer |

| Exceptions ||
|---|---|
| `java.nio.BufferOverflowException` | If there are fewer than eight bytes remaining in this buffer |
| `java.nio.ReadOnlyBufferException` | If this buffer is read-only |

### putDouble

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun putDouble(
    index: Int, 
    value: Double
): ByteBuffer
```

Absolute *put* method for writing a double value *(optional operation)*.

Writes eight bytes containing the given double value, in the current byte order, into this buffer at the given index.

| Parameters ||
|---|---|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The index at which the bytes will be written |
| `value` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html): The double value to be written |

| Return ||
|---|---|
| ByteBuffer | This buffer |

| Exceptions ||
|---|---|
| `java.lang.IndexOutOfBoundsException` | If `index` is negative or not smaller than the buffer's limit, minus seven |
| `java.nio.ReadOnlyBufferException` | If this buffer is read-only |

### putFloat

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun putFloat(value: Float): ByteBuffer
```

Relative *put* method for writing a float value *(optional operation)*.

Writes four bytes containing the given float value, in the current byte order, into this buffer at the current position, and then increments the position by four.

| Parameters ||
|---|---|
| `value` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The float value to be written |

| Return ||
|---|---|
| ByteBuffer | This buffer |

| Exceptions ||
|---|---|
| `java.nio.BufferOverflowException` | If there are fewer than four bytes remaining in this buffer |
| `java.nio.ReadOnlyBufferException` | If this buffer is read-only |

### putFloat

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun putFloat(
    index: Int, 
    value: Float
): ByteBuffer
```

Absolute *put* method for writing a float value *(optional operation)*.

Writes four bytes containing the given float value, in the current byte order, into this buffer at the given index.

| Parameters ||
|---|---|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The index at which the bytes will be written |
| `value` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The float value to be written |

| Return ||
|---|---|
| ByteBuffer | This buffer |

| Exceptions ||
|---|---|
| `java.lang.IndexOutOfBoundsException` | If `index` is negative or not smaller than the buffer's limit, minus three |
| `java.nio.ReadOnlyBufferException` | If this buffer is read-only |

### putInt

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun putInt(value: Int): ByteBuffer
```

Relative *put* method for writing an int value *(optional operation)*.

Writes four bytes containing the given int value, in the current byte order, into this buffer at the current position, and then increments the position by four.

| Parameters ||
|---|---|
| `value` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The int value to be written |

| Return ||
|---|---|
| ByteBuffer | This buffer |

| Exceptions ||
|---|---|
| `java.nio.BufferOverflowException` | If there are fewer than four bytes remaining in this buffer |
| `java.nio.ReadOnlyBufferException` | If this buffer is read-only |

### putInt

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun putInt(
    index: Int, 
    value: Int
): ByteBuffer
```

Absolute *put* method for writing an int value *(optional operation)*.

Writes four bytes containing the given int value, in the current byte order, into this buffer at the given index.

| Parameters ||
|---|---|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The index at which the bytes will be written |
| `value` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The int value to be written |

| Return ||
|---|---|
| ByteBuffer | This buffer |

| Exceptions ||
|---|---|
| `java.lang.IndexOutOfBoundsException` | If `index` is negative or not smaller than the buffer's limit, minus three |
| `java.nio.ReadOnlyBufferException` | If this buffer is read-only |

### putLong

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun putLong(
    index: Int, 
    value: Long
): ByteBuffer
```

Absolute *put* method for writing a long value *(optional operation)*.

Writes eight bytes containing the given long value, in the current byte order, into this buffer at the given index.

| Parameters ||
|---|---|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The index at which the bytes will be written |
| `value` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): The long value to be written |

| Return ||
|---|---|
| ByteBuffer | This buffer |

| Exceptions ||
|---|---|
| `java.lang.IndexOutOfBoundsException` | If `index` is negative or not smaller than the buffer's limit, minus seven |
| `java.nio.ReadOnlyBufferException` | If this buffer is read-only |

### putLong

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun putLong(value: Long): ByteBuffer
```

Relative *put* method for writing a long value *(optional operation)*.

Writes eight bytes containing the given long value, in the current byte order, into this buffer at the current position, and then increments the position by eight.

| Parameters ||
|---|---|
| `value` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): The long value to be written |

| Return ||
|---|---|
| ByteBuffer | This buffer |

| Exceptions ||
|---|---|
| `java.nio.BufferOverflowException` | If there are fewer than eight bytes remaining in this buffer |
| `java.nio.ReadOnlyBufferException` | If this buffer is read-only |

### putShort

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun putShort(
    index: Int, 
    value: Short
): ByteBuffer
```

Absolute *put* method for writing a short value *(optional operation)*.

Writes two bytes containing the given short value, in the current byte order, into this buffer at the given index.

| Parameters ||
|---|---|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The index at which the bytes will be written |
| `value` | [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html): The short value to be written |

| Return ||
|---|---|
| ByteBuffer | This buffer |

| Exceptions ||
|---|---|
| `java.lang.IndexOutOfBoundsException` | If `index` is negative or not smaller than the buffer's limit, minus one |
| `java.nio.ReadOnlyBufferException` | If this buffer is read-only |

### putShort

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun putShort(value: Short): ByteBuffer
```

Relative *put* method for writing a short value *(optional operation)*.

Writes two bytes containing the given short value, in the current byte order, into this buffer at the current position, and then increments the position by two.

| Parameters ||
|---|---|
| `value` | [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html): The short value to be written |

| Return ||
|---|---|
| ByteBuffer | This buffer |

| Exceptions ||
|---|---|
| `java.nio.BufferOverflowException` | If there are fewer than two bytes remaining in this buffer |
| `java.nio.ReadOnlyBufferException` | If this buffer is read-only |

### reset

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun reset(): Buffer
```

Resets this buffer's position to the previously-marked position.

Invoking this method neither changes nor discards the mark's value.

| Return ||
|---|---|
| Buffer | This buffer |

| Exceptions ||
|---|---|
| `java.nio.InvalidMarkException` | If the mark has not been set |

### rewind

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun rewind(): Buffer
```

Rewinds this buffer. The position is set to zero and the mark is discarded.

Invoke this method before a sequence of channel-write or *get* operations, assuming that the limit has already been set appropriately. For example:

```kotlin
out.write(buf);    // Write remaining data
  buf.rewind();      // Rewind buffer
  buf.get(array);    // Copy data into array
```

| Return ||
|---|---|
| Buffer | This buffer |

### slice

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun slice(): ByteBuffer
```

Creates a new byte buffer whose content is a shared subsequence of this buffer's content.

The content of the new buffer will start at this buffer's current position. Changes to this buffer's content will be visible in the new buffer, and vice versa; the two buffers' position, limit, and mark values will be independent.

The new buffer's position will be zero, its capacity and its limit will be the number of bytes remaining in this buffer, its mark will be undefined, and its byte order will be `https://developer.android.com/reference/kotlin/java/nio/ByteOrder#BIG_ENDIAN:java.nio.ByteOrder`. The new buffer will be direct if, and only if, this buffer is direct, and it will be read-only if, and only if, this buffer is read-only.

| Return ||
|---|---|
| ByteBuffer | The new byte buffer |

**See Also**

- alignedSlice

### slice

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun slice(
    index: Int, 
    length: Int
): ByteBuffer
```

Creates a new byte buffer whose content is a shared subsequence of this buffer's content.

The content of the new buffer will start at position `index` in this buffer, and will contain `length` elements. Changes to this buffer's content will be visible in the new buffer, and vice versa; the two buffers' position, limit, and mark values will be independent.

The new buffer's position will be zero, its capacity and its limit will be `length`, its mark will be undefined, and its byte order will be `https://developer.android.com/reference/kotlin/java/nio/ByteOrder#BIG_ENDIAN:java.nio.ByteOrder`. The new buffer will be direct if, and only if, this buffer is direct, and it will be read-only if, and only if, this buffer is read-only.

| Parameters ||
|---|---|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The position in this buffer at which the content of the new buffer will start; must be non-negative and no larger than limit |
| `length` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The number of elements the new buffer will contain; must be non-negative and no larger than `limit() - index` |

| Return ||
|---|---|
| ByteBuffer | The new buffer |

| Exceptions ||
|---|---|
| `java.lang.IndexOutOfBoundsException` | If `index` is negative or greater than `limit()`, `length` is negative, or `length > limit() - index` |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun toString(): String
```

Returns a string summarizing the state of this buffer.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | A summary string |

### wrap

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun wrap(array: ByteArray): ByteBuffer
```

Wraps a byte array into a buffer.

The new buffer will be backed by the given byte array; that is, modifications to the buffer will cause the array to be modified and vice versa. The new buffer's capacity and limit will be `array.length`, its position will be zero, its mark will be undefined, and its byte order will be `https://developer.android.com/reference/kotlin/java/nio/ByteOrder#BIG_ENDIAN:java.nio.ByteOrder`. Its array will be the given array, and its arrayOffset will be zero.

| Parameters ||
|---|---|
| `array` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html): The array that will back this buffer |

| Return ||
|---|---|
| ByteBuffer | The new byte buffer |

### wrap

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun wrap(
    array: ByteArray, 
    offset: Int, 
    length: Int
): ByteBuffer
```

Wraps a byte array into a buffer.

The new buffer will be backed by the given byte array; that is, modifications to the buffer will cause the array to be modified and vice versa. The new buffer's capacity will be `array.length`, its position will be `offset`, its limit will be `offset + length`, its mark will be undefined, and its byte order will be `https://developer.android.com/reference/kotlin/java/nio/ByteOrder#BIG_ENDIAN:java.nio.ByteOrder`. Its array will be the given array, and its arrayOffset will be zero.

| Parameters ||
|---|---|
| `array` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html): The array that will back the new buffer |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The offset of the subarray to be used; must be non-negative and no larger than `array.length`. The new buffer's position will be set to this value. |
| `length` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The length of the subarray to be used; must be non-negative and no larger than `array.length - offset`. The new buffer's limit will be set to `offset + length`. |
| --- | --- |

| Return ||
|---|---|
| ByteBuffer | The new byte buffer |

| Exceptions ||
|---|---|
| `java.lang.IndexOutOfBoundsException` | If the preconditions on the `offset` and `length` parameters do not hold |
