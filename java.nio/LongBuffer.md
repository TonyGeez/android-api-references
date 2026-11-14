# LongBuffer

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# LongBuffer

```
abstract class LongBuffer : Buffer, Comparable<LongBuffer!>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [java.nio.Buffer](Buffer.md) ||
| | ↳ | [java.nio.LongBuffer](LongBuffer.md) |

A long buffer.

This class defines four categories of operations upon long buffers:

- Absolute and relative [*get*](LongBuffer.md))and [*put*](LongBuffer.md))methods that read and write single longs;
- Absolute and relative [*bulk get*](LongBuffer.md))methods that transfer contiguous sequences of longs from this buffer into an array; and
- Absolute and relative [*bulk put*](LongBuffer.md))methods that transfer contiguous sequences of longs from a long array or some other long buffer into this buffer; and
- A method for [compacting](LongBuffer.md))a long buffer.

Long buffers can be created either by [*allocation*](LongBuffer.md)), which allocates space for the buffer's content, by [*wrapping*](LongBuffer.md))an existing long array into a buffer, or by creating a [*view*](ByteBuffer.md) of an existing byte buffer.

Like a byte buffer, a long buffer is either [*direct* or*non-direct*](ByteBuffer.md). A long buffer created via the`wrap`methods of this class will be non-direct. A long buffer created as a view of a byte buffer will be direct if, and only if, the byte buffer itself is direct. Whether or not a long buffer is direct may be determined by invoking the [isDirect](LongBuffer.md))method.

Methods in this class that do not otherwise have a value to return are specified to return the buffer upon which they are invoked. This allows method invocations to be chained.

## Summary

| Public methods ||
|----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [LongBuffer](LongBuffer.md)! | [allocate](LongBuffer.md))`(`capacity:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Allocates a new long buffer. |
| [LongArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html)! | [array](LongBuffer.md))`()` Returns the long array that backs this buffer*(optional operation)*. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [arrayOffset](LongBuffer.md))`()` Returns the offset within this buffer's backing array of the first element of the buffer*(optional operation)*. |
| --- | --- |
| abstract [LongBuffer](LongBuffer.md)! | [asReadOnlyBuffer](LongBuffer.md))`()` Creates a new, read-only long buffer that shares this buffer's content. |
| open [Buffer](Buffer.md)! | [clear](LongBuffer.md))`()` Clears this buffer. |
| abstract [LongBuffer](LongBuffer.md)! | [compact](LongBuffer.md))`()` Compacts this buffer*(optional operation)*. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [compareTo](LongBuffer.md))`(`other:` ` [LongBuffer](LongBuffer.md)!`)` Compares this buffer to another. |
| abstract [LongBuffer](LongBuffer.md)! | [duplicate](LongBuffer.md))`()` Creates a new long buffer that shares this buffer's content. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](LongBuffer.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Tells whether or not this buffer is equal to another object. |
| --- | --- |
| open [Buffer](Buffer.md)! | [flip](LongBuffer.md))`()` Flips this buffer. |
| abstract [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [get](LongBuffer.md))`()` Relative*get*method. |
| abstract [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [get](LongBuffer.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Absolute*get*method. |
| --- | --- |
| open [LongBuffer](LongBuffer.md)! | [get](LongBuffer.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `dst:` ` [LongArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html)!`)` Absolute bulk*get*method. |
| open [LongBuffer](LongBuffer.md)! | [get](LongBuffer.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `dst:` ` [LongArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html)!`, `offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `length:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Absolute bulk*get*method. |
| open [LongBuffer](LongBuffer.md)! | [get](LongBuffer.md))`(`dst:` ` [LongArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html)!`)` Relative bulk*get*method. |
| --- | --- |
| open [LongBuffer](LongBuffer.md)! | [get](LongBuffer.md))`(`dst:` ` [LongArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html)!`, `offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `length:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Relative bulk*get*method. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasArray](LongBuffer.md))`()` Tells whether or not this buffer is backed by an accessible long array. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](LongBuffer.md))`()` Returns the current hash code of this buffer. |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isDirect](LongBuffer.md))`()` Tells whether or not this long buffer is direct. |
| open [Buffer](Buffer.md)! | [limit](LongBuffer.md))`(`newLimit:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets this buffer's limit. |
| open [Buffer](Buffer.md)! | [mark](LongBuffer.md))`()` Sets this buffer's mark at its position. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [mismatch](LongBuffer.md))`(`that:` ` [LongBuffer](LongBuffer.md)!`)` Finds and returns the relative index of the first mismatch between this buffer and a given buffer. |
| abstract [ByteOrder](ByteOrder.md)! | [order](LongBuffer.md))`()` Retrieves this buffer's byte order. |
| open [Buffer](Buffer.md)! | [position](LongBuffer.md))`(`newPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets this buffer's position. |
| --- | --- |
| open [LongBuffer](LongBuffer.md)! | [put](LongBuffer.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `src:` ` [LongBuffer](LongBuffer.md)!`, `offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `length:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Absolute bulk*put* method*(optional operation)*. |
| abstract [LongBuffer](LongBuffer.md)! | [put](LongBuffer.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `l:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Absolute*put* method*(optional operation)*. |
| open [LongBuffer](LongBuffer.md)! | [put](LongBuffer.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `src:` ` [LongArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html)!`)` Absolute bulk*put* method*(optional operation)*. |
| --- | --- |
| open [LongBuffer](LongBuffer.md)! | [put](LongBuffer.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `src:` ` [LongArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html)!`, `offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `length:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Absolute bulk*put* method*(optional operation)*. |
| open [LongBuffer](LongBuffer.md)! | [put](LongBuffer.md))`(`src:` ` [LongBuffer](LongBuffer.md)!`)` Relative bulk*put* method*(optional operation)*. |
| abstract [LongBuffer](LongBuffer.md)! | [put](LongBuffer.md))`(`l:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Relative*put* method*(optional operation)*. |
| --- | --- |
| [LongBuffer](LongBuffer.md)! | [put](LongBuffer.md))`(`src:` ` [LongArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html)!`)` Relative bulk*put* method*(optional operation)*. |
| open [LongBuffer](LongBuffer.md)! | [put](LongBuffer.md))`(`src:` ` [LongArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html)!`, `offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `length:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Relative bulk*put* method*(optional operation)*. |
| open [Buffer](Buffer.md)! | [reset](LongBuffer.md))`()` Resets this buffer's position to the previously-marked position. |
| --- | --- |
| open [Buffer](Buffer.md)! | [rewind](LongBuffer.md))`()` Rewinds this buffer. |
| abstract [LongBuffer](LongBuffer.md)! | [slice](LongBuffer.md))`()` Creates a new long buffer whose content is a shared subsequence of this buffer's content. |
| abstract [LongBuffer](LongBuffer.md)! | [slice](LongBuffer.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `length:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a new long buffer whose content is a shared subsequence of this buffer's content. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](LongBuffer.md))`()` Returns a string summarizing the state of this buffer. |
| openstatic [LongBuffer](LongBuffer.md)! | [wrap](LongBuffer.md))`(`array:` ` [LongArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html)!`)` Wraps a long array into a buffer. |
| openstatic [LongBuffer](LongBuffer.md)! | [wrap](LongBuffer.md))`(`array:` ` [LongArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html)!`, `offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `length:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Wraps a long array into a buffer. |
| --- | --- |

| Inherited functions ||
|---|---|
| From class [Buffer](Buffer.md) |------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [capacity](Buffer.md))`()` <br /> Returns this buffer's capacity. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasRemaining](Buffer.md))`()` <br /> Tells whether there are any elements between the current position and the limit. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isReadOnly](Buffer.md))`()` <br /> Tells whether or not this buffer is read-only. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [limit](Buffer.md))`()` <br /> Returns this buffer's limit. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [position](Buffer.md))`()` <br /> Returns this buffer's position. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [remaining](Buffer.md))`()` <br /> Returns the number of elements between the current position and the limit. <br /> | ||

## Public methods

### allocate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun allocate(capacity: Int): LongBuffer!
```

Allocates a new long buffer.

The new buffer's position will be zero, its limit will be its capacity, its mark will be undefined, each of its elements will be initialized to zero, and its byte order will be the [native order](ByteOrder.md))of the underlying hardware. It will have a [backing array](LongBuffer.md)), and its [array offset](LongBuffer.md))will be zero.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------|
| `capacity` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The new buffer's capacity, in longs |

| Return ||
|------------------------------------------------------------------------------------|---------------------|
| [LongBuffer](LongBuffer.md)! | The new long buffer |

| Exceptions ||
|--------------------------------------|---------------------------------------|
| `java.lang.IllegalArgumentException` | If the`capacity`is a negative integer |

### array

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun array(): LongArray!
```

Returns the long array that backs this buffer*(optional operation)*.

Modifications to this buffer's content will cause the returned array's content to be modified, and vice versa.

Invoke the [hasArray](LongBuffer.md))method before invoking this method in order to ensure that this buffer has an accessible backing array.

| Return ||
|------------------------------------------------------------------------------------------|----------------------------------|
| [LongArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html)! | The array that backs this buffer |

| Exceptions ||
|-------------------------------------------|-------------------------------------------------------|
| `java.nio.ReadOnlyBufferException` | If this buffer is backed by an array but is read-only |
| `java.lang.UnsupportedOperationException` | If this buffer is not backed by an accessible array |

### arrayOffset

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun arrayOffset(): Int
```

Returns the offset within this buffer's backing array of the first element of the buffer*(optional operation)*.

If this buffer is backed by an array then buffer position*p* corresponds to array index*p* +`arrayOffset()`.

Invoke the [hasArray](LongBuffer.md))method before invoking this method in order to ensure that this buffer has an accessible backing array.

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The offset within this buffer's array of the first element of the buffer |

| Exceptions ||
|-------------------------------------------|-------------------------------------------------------|
| `java.nio.ReadOnlyBufferException` | If this buffer is backed by an array but is read-only |
| `java.lang.UnsupportedOperationException` | If this buffer is not backed by an accessible array |

### asReadOnlyBuffer

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun asReadOnlyBuffer(): LongBuffer!
```

Creates a new, read-only long buffer that shares this buffer's content.

The content of the new buffer will be that of this buffer. Changes to this buffer's content will be visible in the new buffer; the new buffer itself, however, will be read-only and will not allow the shared content to be modified. The two buffers' position, limit, and mark values will be independent.

The new buffer's capacity, limit, position, mark values, and byte order will be identical to those of this buffer.

If this buffer is itself read-only then this method behaves in exactly the same way as the [duplicate](LongBuffer.md))method.

| Return ||
|------------------------------------------------------------------------------------|--------------------------------|
| [LongBuffer](LongBuffer.md)! | The new, read-only long buffer |

### clear

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun clear(): Buffer!
```

Clears this buffer. The position is set to zero, the limit is set to the capacity, and the mark is discarded.

Invoke this method before using a sequence of channel-read or*put*operations to fill this buffer. For example: 

```kotlin
buf.clear();     // Prepare buffer for reading
  in.read(buf);    // Read data
```

This method does not actually erase the data in the buffer, but it is named as if it did because it will most often be used in situations in which that might as well be the case.

| Return ||
|---------------------------------------------------------------------------|-------------|
| [Buffer](Buffer.md)! | This buffer |

### compact

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun compact(): LongBuffer!
```

Compacts this buffer*(optional operation)*.

The longs between the buffer's current position and its limit, if any, are copied to the beginning of the buffer. That is, the long at index*p* =`position()`is copied to index zero, the long at index*p* + 1 is copied to index one, and so forth until the long at index`limit()`- 1 is copied to index*n* =`limit()`-`1`-*p* . The buffer's position is then set to*n+1*and its limit is set to its capacity. The mark, if defined, is discarded.

The buffer's position is set to the number of longs copied, rather than to zero, so that an invocation of this method can be followed immediately by an invocation of another relative*put*method.

| Return ||
|------------------------------------------------------------------------------------|-------------|
| [LongBuffer](LongBuffer.md)! | This buffer |

| Exceptions ||
|------------------------------------|-----------------------------|
| `java.nio.ReadOnlyBufferException` | If this buffer is read-only |

### compareTo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun compareTo(other: LongBuffer!): Int
```

Compares this buffer to another.

Two long buffers are compared by comparing their sequences of remaining elements lexicographically, without regard to the starting position of each sequence within its corresponding buffer. Pairs of`long`elements are compared as if by invoking [Long.compare(long,long)](../java.lang/Long.md)).

A long buffer is not comparable to any other type of object.

| Parameters ||
|-----|----------------------------|
| `o` | the object to be compared. |

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | A negative integer, zero, or a positive integer as this buffer is less than, equal to, or greater than the given buffer |

| Exceptions ||
|----------------------------------|--------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if the specified object is null |
| `java.lang.ClassCastException` | if the specified object's type prevents it from being compared to this object. |

### duplicate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun duplicate(): LongBuffer!
```

Creates a new long buffer that shares this buffer's content.

The content of the new buffer will be that of this buffer. Changes to this buffer's content will be visible in the new buffer, and vice versa; the two buffers' position, limit, and mark values will be independent.

The new buffer's capacity, limit, position, mark values, and byte order will be identical to those of this buffer. The new buffer will be direct if, and only if, this buffer is direct, and it will be read-only if, and only if, this buffer is read-only.

| Return ||
|------------------------------------------------------------------------------------|---------------------|
| [LongBuffer](LongBuffer.md)! | The new long buffer |

### equals

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun equals(other: Any?): Boolean
```

Tells whether or not this buffer is equal to another object.

Two long buffers are equal if, and only if,

1. They have the same element type,
2. They have the same number of remaining elements, and
3. The two sequences of remaining elements, considered independently of their starting positions, are pointwise equal.

A long buffer is not equal to any other type of object.

| Parameters ||
|-------|---------------------------------------------------|
| `obj` | the reference object with which to compare. |
| `ob` | The object to which this buffer is to be compared |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if, and only if, this buffer is equal to the given object |

### flip

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun flip(): Buffer!
```

Flips this buffer. The limit is set to the current position and then the position is set to zero. If the mark is defined then it is discarded.

After a sequence of channel-read or*put* operations, invoke this method to prepare for a sequence of channel-write or relative*get*operations. For example: 

```kotlin
buf.put(magic);    // Prepend header
  in.read(buf);      // Read data into rest of buffer
  buf.flip();        // Flip buffer
  out.write(buf);    // Write header + data to channel
```

This method is often used in conjunction with the [compact](ByteBuffer.md))method when transferring data from one place to another.

| Return ||
|---------------------------------------------------------------------------|-------------|
| [Buffer](Buffer.md)! | This buffer |

### get

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun get(): Long
```

Relative*get*method. Reads the long at this buffer's current position, and then increments the position.

| Return ||
|------------------------------------------------------------------------------|-------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | The long at the buffer's current position |

| Exceptions ||
|-------------------------------------|----------------------------------------------------------------|
| `java.nio.BufferUnderflowException` | If the buffer's current position is not smaller than its limit |

### get

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun get(index: Int): Long
```

Absolute*get*method. Reads the long at the given index.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The index from which the long will be read |

| Return ||
|------------------------------------------------------------------------------|-----------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | The long at the given index |

| Exceptions ||
|---------------------------------------|-------------------------------------------------------------|
| `java.lang.IndexOutOfBoundsException` | If`index`is negative or not smaller than the buffer's limit |

### get

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun get(
    index: Int, 
    dst: LongArray!
): LongBuffer!
```

Absolute bulk*get*method.

This method transfers longs from this buffer into the given destination array. The position of this buffer is unchanged. An invocation of this method of the form`src.get(index, dst)`behaves in exactly the same way as the invocation: 

```kotlin
src.get(index, dst, 0, dst.length) 
```

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The index in this buffer from which the first long will be read; must be non-negative and less than`limit()` |
| `dst` | [LongArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html)!:The destination array |

| Return ||
|------------------------------------------------------------------------------------|-------------|
| [LongBuffer](LongBuffer.md)! | This buffer |

| Exceptions ||
|---------------------------------------|-----------------------------------------------------------------------------------|
| `java.lang.IndexOutOfBoundsException` | If`index`is negative, not smaller than`limit()`, or`limit() - index < dst.length` |

### get

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun get(
    index: Int, 
    dst: LongArray!, 
    offset: Int, 
    length: Int
): LongBuffer!
```

Absolute bulk*get*method.

This method transfers`length`longs from this buffer into the given array, starting at the given index in this buffer and at the given offset in the array. The position of this buffer is unchanged.

An invocation of this method of the form`src.get(index, dst, offset, length)`has exactly the same effect as the following loop except that it first checks the consistency of the supplied parameters and it is potentially much more efficient: 

```kotlin
<code>for (int i = offset, j = index; i &lt; offset + length; i++, j++)
          dst[i] = src.get(j);
  </code>
```

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The index in this buffer from which the first long will be read; must be non-negative and less than`limit()` |
| `dst` | [LongArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html)!:The destination array |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The offset within the array of the first long to be written; must be non-negative and less than`dst.length` |
| --- | --- |
| `length` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The number of longs to be written to the given array; must be non-negative and no larger than the smaller of`limit() - index`and`dst.length - offset` |

| Return ||
|------------------------------------------------------------------------------------|-------------|
| [LongBuffer](LongBuffer.md)! | This buffer |

| Exceptions ||
|---------------------------------------|--------------------------------------------------------------------------------|
| `java.lang.IndexOutOfBoundsException` | If the preconditions on the`index`,`offset`, and`length`parameters do not hold |

### get

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun get(dst: LongArray!): LongBuffer!
```

Relative bulk*get*method.

This method transfers longs from this buffer into the given destination array. An invocation of this method of the form`src.get(a)`behaves in exactly the same way as the invocation 

```kotlin
src.get(a, 0, a.length) 
```

| Parameters ||
|-------|----------------------------------------------------------------------------------------------------------------|
| `dst` | [LongArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html)!:The destination array |

| Return ||
|------------------------------------------------------------------------------------|-------------|
| [LongBuffer](LongBuffer.md)! | This buffer |

| Exceptions ||
|-------------------------------------|---------------------------------------------------------------|
| `java.nio.BufferUnderflowException` | If there are fewer than`length`longs remaining in this buffer |

### get

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun get(
    dst: LongArray!, 
    offset: Int, 
    length: Int
): LongBuffer!
```

Relative bulk*get*method.

This method transfers longs from this buffer into the given destination array. If there are fewer longs remaining in the buffer than are required to satisfy the request, that is, if`length``>``remaining()`, then no longs are transferred and a [BufferUnderflowException](BufferUnderflowException.md) is thrown.

Otherwise, this method copies`length`longs from this buffer into the given array, starting at the current position of this buffer and at the given offset in the array. The position of this buffer is then incremented by`length`.

In other words, an invocation of this method of the form`src.get(dst, off, len)`has exactly the same effect as the loop 

```kotlin
<code>for (int i = off; i &lt; off + len; i++)
          dst[i] = src.get();
  </code>
```
except that it first checks that there are sufficient longs in this buffer and it is potentially much more efficient.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dst` | [LongArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html)!:The array into which longs are to be written |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The offset within the array of the first long to be written; must be non-negative and no larger than`dst.length` |
| `length` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The maximum number of longs to be written to the given array; must be non-negative and no larger than`dst.length - offset` |
| --- | --- |

| Return ||
|------------------------------------------------------------------------------------|-------------|
| [LongBuffer](LongBuffer.md)! | This buffer |

| Exceptions ||
|---------------------------------------|----------------------------------------------------------------------|
| `java.nio.BufferUnderflowException` | If there are fewer than`length`longs remaining in this buffer |
| `java.lang.IndexOutOfBoundsException` | If the preconditions on the`offset`and`length`parameters do not hold |

### hasArray

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hasArray(): Boolean
```

Tells whether or not this buffer is backed by an accessible long array.

If this method returns`true`then the [array](LongBuffer.md))and [arrayOffset](LongBuffer.md))methods may safely be invoked.

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if, and only if, this buffer is backed by an array and is not read-only |

### hashCode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hashCode(): Int
```

Returns the current hash code of this buffer.

The hash code of a long buffer depends only upon its remaining elements; that is, upon the elements from`position()`up to, and including, the element at`limit()`-`1`.

Because buffer hash codes are content-dependent, it is inadvisable to use buffers as keys in hash maps or similar data structures unless it is known that their contents will not change.

| Return ||
|----------------------------------------------------------------------------|--------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The current hash code of this buffer |

### isDirect

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isDirect(): Boolean
```

Tells whether or not this long buffer is direct.

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if, and only if, this buffer is direct |

### limit

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun limit(newLimit: Int): Buffer!
```

Sets this buffer's limit. If the position is larger than the new limit then it is set to the new limit. If the mark is defined and larger than the new limit then it is discarded.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `newLimit` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The new limit value; must be non-negative and no larger than this buffer's capacity |

| Return ||
|---------------------------------------------------------------------------|-------------|
| [Buffer](Buffer.md)! | This buffer |

| Exceptions ||
|--------------------------------------|----------------------------------------------|
| `java.lang.IllegalArgumentException` | If the preconditions on`newLimit`do not hold |

### mark

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun mark(): Buffer!
```

Sets this buffer's mark at its position.

| Return ||
|---------------------------------------------------------------------------|-------------|
| [Buffer](Buffer.md)! | This buffer |

### mismatch

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun mismatch(that: LongBuffer!): Int
```

Finds and returns the relative index of the first mismatch between this buffer and a given buffer. The index is relative to the [position](Buffer.md))of each buffer and will be in the range of 0 (inclusive) up to the smaller of the [remaining](Buffer.md))elements in each buffer (exclusive).

If the two buffers share a common prefix then the returned index is the length of the common prefix and it follows that there is a mismatch between the two buffers at that index within the respective buffers. If one buffer is a proper prefix of the other then the returned index is the smaller of the remaining elements in each buffer, and it follows that the index is only valid for the buffer with the larger number of remaining elements. Otherwise, there is no mismatch.

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| `that` | [LongBuffer](LongBuffer.md)!:The byte buffer to be tested for a mismatch with this buffer |

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The relative index of the first mismatch between this and the given buffer, otherwise -1 if no mismatch. |

### order

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun order(): ByteOrder!
```

Retrieves this buffer's byte order.

The byte order of a long buffer created by allocation or by wrapping an existing`long`array is the [native order](ByteOrder.md))of the underlying hardware. The byte order of a long buffer created as a [view](ByteBuffer.md) of a byte buffer is that of the byte buffer at the moment that the view is created.

| Return ||
|---------------------------------------------------------------------------------|--------------------------|
| [ByteOrder](ByteOrder.md)! | This buffer's byte order |

### position

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun position(newPosition: Int): Buffer!
```

Sets this buffer's position. If the mark is defined and larger than the new position then it is discarded.

| Parameters ||
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `newPosition` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The new position value; must be non-negative and no larger than the current limit |

| Return ||
|---------------------------------------------------------------------------|-------------|
| [Buffer](Buffer.md)! | This buffer |

| Exceptions ||
|--------------------------------------|-------------------------------------------------|
| `java.lang.IllegalArgumentException` | If the preconditions on`newPosition`do not hold |

### put

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun put(
    index: Int, 
    src: LongBuffer!, 
    offset: Int, 
    length: Int
): LongBuffer!
```

Absolute bulk*put* method*(optional operation)*.

This method transfers`length`longs into this buffer from the given source buffer, starting at the given`offset`in the source buffer and the given`index`in this buffer. The positions of both buffers are unchanged.

In other words, an invocation of this method of the form`dst.put(index, src, offset, length)`has exactly the same effect as the loop 

```kotlin
<code>for (int i = offset, j = index; i &lt; offset + length; i++, j++)
      dst.put(j, src.get(i));
  </code>
```
except that it first checks the consistency of the supplied parameters and it is potentially much more efficient. If this buffer and the source buffer share the same backing array or memory, then the result will be as if the source elements were first copied to an intermediate location before being written into this buffer.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The index in this buffer at which the first long will be written; must be non-negative and less than`limit()` |
| `src` | [LongBuffer](LongBuffer.md)!:The buffer from which longs are to be read |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The index within the source buffer of the first long to be read; must be non-negative and less than`src.limit()` |
| --- | --- |
| `length` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The number of longs to be read from the given buffer; must be non-negative and no larger than the smaller of`limit() - index`and`src.limit() - offset` |

| Return ||
|------------------------------------------------------------------------------------|-------------|
| [LongBuffer](LongBuffer.md)! | This buffer |

| Exceptions ||
|---------------------------------------|--------------------------------------------------------------------------------|
| `java.lang.IndexOutOfBoundsException` | If the preconditions on the`index`,`offset`, and`length`parameters do not hold |
| `java.nio.ReadOnlyBufferException` | If this buffer is read-only |

### put

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun put(
    index: Int, 
    l: Long
): LongBuffer!
```

Absolute*put* method*(optional operation)*.

Writes the given long into this buffer at the given index.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The index at which the long will be written |
| `l` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The long value to be written |

| Return ||
|------------------------------------------------------------------------------------|-------------|
| [LongBuffer](LongBuffer.md)! | This buffer |

| Exceptions ||
|---------------------------------------|-------------------------------------------------------------|
| `java.lang.IndexOutOfBoundsException` | If`index`is negative or not smaller than the buffer's limit |
| `java.nio.ReadOnlyBufferException` | If this buffer is read-only |

### put

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun put(
    index: Int, 
    src: LongArray!
): LongBuffer!
```

Absolute bulk*put* method*(optional operation)*.

This method copies longs into this buffer from the given source array. The position of this buffer is unchanged. An invocation of this method of the form`dst.put(index, src)`behaves in exactly the same way as the invocation: 

```kotlin
dst.put(index, src, 0, src.length); 
```

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The index in this buffer at which the first long will be written; must be non-negative and less than`limit()` |
| `src` | [LongArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html)!:The array from which longs are to be read |

| Return ||
|------------------------------------------------------------------------------------|-------------|
| [LongBuffer](LongBuffer.md)! | This buffer |

| Exceptions ||
|---------------------------------------|-----------------------------------------------------------------------------------|
| `java.lang.IndexOutOfBoundsException` | If`index`is negative, not smaller than`limit()`, or`limit() - index < src.length` |
| `java.nio.ReadOnlyBufferException` | If this buffer is read-only |

### put

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun put(
    index: Int, 
    src: LongArray!, 
    offset: Int, 
    length: Int
): LongBuffer!
```

Absolute bulk*put* method*(optional operation)*.

This method transfers`length`longs from the given array, starting at the given offset in the array and at the given index in this buffer. The position of this buffer is unchanged.

An invocation of this method of the form`dst.put(index, src, offset, length)`has exactly the same effect as the following loop except that it first checks the consistency of the supplied parameters and it is potentially much more efficient: 

```kotlin
<code>for (int i = offset, j = index; i &lt; offset + length; i++, j++)
          dst.put(j, src[i]);
  </code>
```

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The index in this buffer at which the first long will be written; must be non-negative and less than`limit()` |
| `src` | [LongArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html)!:The array from which longs are to be read |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The offset within the array of the first long to be read; must be non-negative and less than`src.length` |
| --- | --- |
| `length` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The number of longs to be read from the given array; must be non-negative and no larger than the smaller of`limit() - index`and`src.length - offset` |

| Return ||
|------------------------------------------------------------------------------------|-------------|
| [LongBuffer](LongBuffer.md)! | This buffer |

| Exceptions ||
|---------------------------------------|--------------------------------------------------------------------------------|
| `java.lang.IndexOutOfBoundsException` | If the preconditions on the`index`,`offset`, and`length`parameters do not hold |
| `java.nio.ReadOnlyBufferException` | If this buffer is read-only |

### put

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun put(src: LongBuffer!): LongBuffer!
```

Relative bulk*put* method*(optional operation)*.

This method transfers the longs remaining in the given source buffer into this buffer. If there are more longs remaining in the source buffer than in this buffer, that is, if`src.remaining()``>``remaining()`, then no longs are transferred and a [BufferOverflowException](BufferOverflowException.md) is thrown.

Otherwise, this method copies*n* =`src.remaining()`longs from the given buffer into this buffer, starting at each buffer's current position. The positions of both buffers are then incremented by*n*.

In other words, an invocation of this method of the form`dst.put(src)`has exactly the same effect as the loop 

```kotlin
while (src.hasRemaining())
          dst.put(src.get()); 
```
except that it first checks that there is sufficient space in this buffer and it is potentially much more efficient. If this buffer and the source buffer share the same backing array or memory, then the result will be as if the source elements were first copied to an intermediate location before being written into this buffer.

| Parameters ||
|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `src` | [LongBuffer](LongBuffer.md)!:The source buffer from which longs are to be read; must not be this buffer |

| Return ||
|------------------------------------------------------------------------------------|-------------|
| [LongBuffer](LongBuffer.md)! | This buffer |

| Exceptions ||
|--------------------------------------|--------------------------------------------------------------------------------------------|
| `java.nio.BufferOverflowException` | If there is insufficient space in this buffer for the remaining longs in the source buffer |
| `java.lang.IllegalArgumentException` | If the source buffer is this buffer |
| `java.nio.ReadOnlyBufferException` | If this buffer is read-only |
| --- | --- |

### put

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun put(l: Long): LongBuffer!
```

Relative*put* method*(optional operation)*.

Writes the given long into this buffer at the current position, and then increments the position.

| Parameters ||
|-----|-----------------------------------------------------------------------------------------------------|
| `l` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The long to be written |

| Return ||
|------------------------------------------------------------------------------------|-------------|
| [LongBuffer](LongBuffer.md)! | This buffer |

| Exceptions ||
|------------------------------------|-----------------------------------------------------------------|
| `java.nio.BufferOverflowException` | If this buffer's current position is not smaller than its limit |
| `java.nio.ReadOnlyBufferException` | If this buffer is read-only |

### put

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun put(src: LongArray!): LongBuffer!
```

Relative bulk*put* method*(optional operation)*.

This method transfers the entire content of the given source long array into this buffer. An invocation of this method of the form`dst.put(a)`behaves in exactly the same way as the invocation 

```kotlin
dst.put(a, 0, a.length) 
```

| Parameters ||
|-------|-----------------------------------------------------------------------------------------------------------|
| `src` | [LongArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html)!:The source array |

| Return ||
|------------------------------------------------------------------------------------|-------------|
| [LongBuffer](LongBuffer.md)! | This buffer |

| Exceptions ||
|------------------------------------|-----------------------------------------------|
| `java.nio.BufferOverflowException` | If there is insufficient space in this buffer |
| `java.nio.ReadOnlyBufferException` | If this buffer is read-only |

### put

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun put(
    src: LongArray!, 
    offset: Int, 
    length: Int
): LongBuffer!
```

Relative bulk*put* method*(optional operation)*.

This method transfers longs into this buffer from the given source array. If there are more longs to be copied from the array than remain in this buffer, that is, if`length``>``remaining()`, then no longs are transferred and a [BufferOverflowException](BufferOverflowException.md) is thrown.

Otherwise, this method copies`length`longs from the given array into this buffer, starting at the given offset in the array and at the current position of this buffer. The position of this buffer is then incremented by`length`.

In other words, an invocation of this method of the form`dst.put(src, off, len)`has exactly the same effect as the loop 

```kotlin
<code>for (int i = off; i &lt; off + len; i++)
          dst.put(src[i]);
  </code>
```
except that it first checks that there is sufficient space in this buffer and it is potentially much more efficient.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `src` | [LongArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html)!:The array from which longs are to be read |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The offset within the array of the first long to be read; must be non-negative and no larger than`src.length` |
| `length` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The number of longs to be read from the given array; must be non-negative and no larger than`src.length - offset` |
| --- | --- |

| Return ||
|------------------------------------------------------------------------------------|-------------|
| [LongBuffer](LongBuffer.md)! | This buffer |

| Exceptions ||
|---------------------------------------|----------------------------------------------------------------------|
| `java.nio.BufferOverflowException` | If there is insufficient space in this buffer |
| `java.lang.IndexOutOfBoundsException` | If the preconditions on the`offset`and`length`parameters do not hold |
| `java.nio.ReadOnlyBufferException` | If this buffer is read-only |
| --- | --- |

### reset

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun reset(): Buffer!
```

Resets this buffer's position to the previously-marked position.

Invoking this method neither changes nor discards the mark's value.

| Return ||
|---------------------------------------------------------------------------|-------------|
| [Buffer](Buffer.md)! | This buffer |

| Exceptions ||
|---------------------------------|------------------------------|
| `java.nio.InvalidMarkException` | If the mark has not been set |

### rewind

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun rewind(): Buffer!
```

Rewinds this buffer. The position is set to zero and the mark is discarded.

Invoke this method before a sequence of channel-write or*get*operations, assuming that the limit has already been set appropriately. For example: 

```kotlin
out.write(buf);    // Write remaining data
  buf.rewind();      // Rewind buffer
  buf.get(array);    // Copy data into array
```

| Return ||
|---------------------------------------------------------------------------|-------------|
| [Buffer](Buffer.md)! | This buffer |

### slice

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun slice(): LongBuffer!
```

Creates a new long buffer whose content is a shared subsequence of this buffer's content.

The content of the new buffer will start at this buffer's current position. Changes to this buffer's content will be visible in the new buffer, and vice versa; the two buffers' position, limit, and mark values will be independent.

The new buffer's position will be zero, its capacity and its limit will be the number of longs remaining in this buffer, its mark will be undefined, and its byte order will be identical to that of this buffer. The new buffer will be direct if, and only if, this buffer is direct, and it will be read-only if, and only if, this buffer is read-only.

| Return ||
|------------------------------------------------------------------------------------|---------------------|
| [LongBuffer](LongBuffer.md)! | The new long buffer |

### slice

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun slice(
    index: Int, 
    length: Int
): LongBuffer!
```

Creates a new long buffer whose content is a shared subsequence of this buffer's content.

The content of the new buffer will start at position`index`in this buffer, and will contain`length`elements. Changes to this buffer's content will be visible in the new buffer, and vice versa; the two buffers' position, limit, and mark values will be independent.

The new buffer's position will be zero, its capacity and its limit will be`length`, its mark will be undefined, and its byte order will be identical to that of this buffer. The new buffer will be direct if, and only if, this buffer is direct, and it will be read-only if, and only if, this buffer is read-only.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The position in this buffer at which the content of the new buffer will start; must be non-negative and no larger than [limit()](Buffer.md)) |
| `length` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The number of elements the new buffer will contain; must be non-negative and no larger than`limit() - index` |

| Return ||
|------------------------------------------------------------------------------------|----------------|
| [LongBuffer](LongBuffer.md)! | The new buffer |

| Exceptions ||
|---------------------------------------|-------------------------------------------------------------------------------------------------|
| `java.lang.IndexOutOfBoundsException` | If`index`is negative or greater than`limit()`,`length`is negative, or`length > limit() - index` |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

Returns a string summarizing the state of this buffer.

| Return ||
|----------------------------------------------------------------------------------|------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | A summary string |

### wrap

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun wrap(array: LongArray!): LongBuffer!
```

Wraps a long array into a buffer.

The new buffer will be backed by the given long array; that is, modifications to the buffer will cause the array to be modified and vice versa. The new buffer's capacity and limit will be`array.length`, its position will be zero, its mark will be undefined, and its byte order will be the [native order](ByteOrder.md))of the underlying hardware. Its [backing array](LongBuffer.md))will be the given array, and its [array offset](LongBuffer.md))will be zero.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------------|
| `array` | [LongArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html)!:The array that will back this buffer |

| Return ||
|------------------------------------------------------------------------------------|---------------------|
| [LongBuffer](LongBuffer.md)! | The new long buffer |

### wrap

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun wrap(
    array: LongArray!, 
    offset: Int, 
    length: Int
): LongBuffer!
```

Wraps a long array into a buffer.

The new buffer will be backed by the given long array; that is, modifications to the buffer will cause the array to be modified and vice versa. The new buffer's capacity will be`array.length`, its position will be`offset`, its limit will be`offset + length`, its mark will be undefined, and its byte order will be the [native order](ByteOrder.md))of the underlying hardware. Its [backing array](LongBuffer.md))will be the given array, and its [array offset](LongBuffer.md))will be zero.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `array` | [LongArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html)!:The array that will back the new buffer |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The offset of the subarray to be used; must be non-negative and no larger than`array.length`. The new buffer's position will be set to this value. |
| `length` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The length of the subarray to be used; must be non-negative and no larger than`array.length - offset`. The new buffer's limit will be set to`offset + length`. |
| --- | --- |

| Return ||
|------------------------------------------------------------------------------------|---------------------|
| [LongBuffer](LongBuffer.md)! | The new long buffer |

| Exceptions ||
|---------------------------------------|----------------------------------------------------------------------|
| `java.lang.IndexOutOfBoundsException` | If the preconditions on the`offset`and`length`parameters do not hold |
