# FloatBuffer

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# FloatBuffer

```
abstract class FloatBuffer : Buffer, Comparable<FloatBuffer!>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [java.nio.Buffer](../java/nio/Buffer.md) ||
| | ↳ | [java.nio.FloatBuffer](../java/nio/FloatBuffer.md) |

A float buffer.

This class defines four categories of operations upon float buffers:

- Absolute and relative [*get*](../java/nio/FloatBuffer.md))and [*put*](../java/nio/FloatBuffer.md))methods that read and write single floats;
- Absolute and relative [*bulk get*](../java/nio/FloatBuffer.md))methods that transfer contiguous sequences of floats from this buffer into an array; and
- Absolute and relative [*bulk put*](../java/nio/FloatBuffer.md))methods that transfer contiguous sequences of floats from a float array or some other float buffer into this buffer; and
- A method for [compacting](../java/nio/FloatBuffer.md))a float buffer.

Float buffers can be created either by [*allocation*](../java/nio/FloatBuffer.md)), which allocates space for the buffer's content, by [*wrapping*](../java/nio/FloatBuffer.md))an existing float array into a buffer, or by creating a [*view*](../java/nio/ByteBuffer.md) of an existing byte buffer.

Like a byte buffer, a float buffer is either [*direct* or*non-direct*](../java/nio/ByteBuffer.md). A float buffer created via the`wrap`methods of this class will be non-direct. A float buffer created as a view of a byte buffer will be direct if, and only if, the byte buffer itself is direct. Whether or not a float buffer is direct may be determined by invoking the [isDirect](../java/nio/FloatBuffer.md))method.

Methods in this class that do not otherwise have a value to return are specified to return the buffer upon which they are invoked. This allows method invocations to be chained.

## Summary

| Public methods ||
|------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [FloatBuffer](../java/nio/FloatBuffer.md)! | [allocate](../java/nio/FloatBuffer.md))`(`capacity:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Allocates a new float buffer. |
| [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)! | [array](../java/nio/FloatBuffer.md))`()` Returns the float array that backs this buffer*(optional operation)*. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [arrayOffset](../java/nio/FloatBuffer.md))`()` Returns the offset within this buffer's backing array of the first element of the buffer*(optional operation)*. |
| --- | --- |
| abstract [FloatBuffer](../java/nio/FloatBuffer.md)! | [asReadOnlyBuffer](../java/nio/FloatBuffer.md))`()` Creates a new, read-only float buffer that shares this buffer's content. |
| open [Buffer](../java/nio/Buffer.md)! | [clear](../java/nio/FloatBuffer.md))`()` Clears this buffer. |
| abstract [FloatBuffer](../java/nio/FloatBuffer.md)! | [compact](../java/nio/FloatBuffer.md))`()` Compacts this buffer*(optional operation)*. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [compareTo](../java/nio/FloatBuffer.md))`(`other:` ` [FloatBuffer](../java/nio/FloatBuffer.md)!`)` Compares this buffer to another. |
| abstract [FloatBuffer](../java/nio/FloatBuffer.md)! | [duplicate](../java/nio/FloatBuffer.md))`()` Creates a new float buffer that shares this buffer's content. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](../java/nio/FloatBuffer.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Tells whether or not this buffer is equal to another object. |
| --- | --- |
| open [Buffer](../java/nio/Buffer.md)! | [flip](../java/nio/FloatBuffer.md))`()` Flips this buffer. |
| abstract [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [get](../java/nio/FloatBuffer.md))`()` Relative*get*method. |
| open [FloatBuffer](../java/nio/FloatBuffer.md)! | [get](../java/nio/FloatBuffer.md))`(`dst:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!`)` Relative bulk*get*method. |
| --- | --- |
| open [FloatBuffer](../java/nio/FloatBuffer.md)! | [get](../java/nio/FloatBuffer.md))`(`dst:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!`, `offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `length:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Relative bulk*get*method. |
| abstract [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [get](../java/nio/FloatBuffer.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Absolute*get*method. |
| open [FloatBuffer](../java/nio/FloatBuffer.md)! | [get](../java/nio/FloatBuffer.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `dst:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!`)` Absolute bulk*get*method. |
| --- | --- |
| open [FloatBuffer](../java/nio/FloatBuffer.md)! | [get](../java/nio/FloatBuffer.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `dst:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!`, `offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `length:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Absolute bulk*get*method. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasArray](../java/nio/FloatBuffer.md))`()` Tells whether or not this buffer is backed by an accessible float array. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](../java/nio/FloatBuffer.md))`()` Returns the current hash code of this buffer. |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isDirect](../java/nio/FloatBuffer.md))`()` Tells whether or not this float buffer is direct. |
| open [Buffer](../java/nio/Buffer.md)! | [limit](../java/nio/FloatBuffer.md))`(`newLimit:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets this buffer's limit. |
| open [Buffer](../java/nio/Buffer.md)! | [mark](../java/nio/FloatBuffer.md))`()` Sets this buffer's mark at its position. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [mismatch](../java/nio/FloatBuffer.md))`(`that:` ` [FloatBuffer](../java/nio/FloatBuffer.md)!`)` Finds and returns the relative index of the first mismatch between this buffer and a given buffer. |
| abstract [ByteOrder](../java/nio/ByteOrder.md)! | [order](../java/nio/FloatBuffer.md))`()` Retrieves this buffer's byte order. |
| open [Buffer](../java/nio/Buffer.md)! | [position](../java/nio/FloatBuffer.md))`(`newPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets this buffer's position. |
| --- | --- |
| abstract [FloatBuffer](../java/nio/FloatBuffer.md)! | [put](../java/nio/FloatBuffer.md))`(`f:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Relative*put* method*(optional operation)*. |
| [FloatBuffer](../java/nio/FloatBuffer.md)! | [put](../java/nio/FloatBuffer.md))`(`src:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!`)` Relative bulk*put* method*(optional operation)*. |
| open [FloatBuffer](../java/nio/FloatBuffer.md)! | [put](../java/nio/FloatBuffer.md))`(`src:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!`, `offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `length:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Relative bulk*put* method*(optional operation)*. |
| --- | --- |
| abstract [FloatBuffer](../java/nio/FloatBuffer.md)! | [put](../java/nio/FloatBuffer.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `f:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Absolute*put* method*(optional operation)*. |
| open [FloatBuffer](../java/nio/FloatBuffer.md)! | [put](../java/nio/FloatBuffer.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `src:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!`)` Absolute bulk*put* method*(optional operation)*. |
| open [FloatBuffer](../java/nio/FloatBuffer.md)! | [put](../java/nio/FloatBuffer.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `src:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!`, `offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `length:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Absolute bulk*put* method*(optional operation)*. |
| --- | --- |
| open [FloatBuffer](../java/nio/FloatBuffer.md)! | [put](../java/nio/FloatBuffer.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `src:` ` [FloatBuffer](../java/nio/FloatBuffer.md)!`, `offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `length:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Absolute bulk*put* method*(optional operation)*. |
| open [FloatBuffer](../java/nio/FloatBuffer.md)! | [put](../java/nio/FloatBuffer.md))`(`src:` ` [FloatBuffer](../java/nio/FloatBuffer.md)!`)` Relative bulk*put* method*(optional operation)*. |
| open [Buffer](../java/nio/Buffer.md)! | [reset](../java/nio/FloatBuffer.md))`()` Resets this buffer's position to the previously-marked position. |
| --- | --- |
| open [Buffer](../java/nio/Buffer.md)! | [rewind](../java/nio/FloatBuffer.md))`()` Rewinds this buffer. |
| abstract [FloatBuffer](../java/nio/FloatBuffer.md)! | [slice](../java/nio/FloatBuffer.md))`()` Creates a new float buffer whose content is a shared subsequence of this buffer's content. |
| abstract [FloatBuffer](../java/nio/FloatBuffer.md)! | [slice](../java/nio/FloatBuffer.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `length:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a new float buffer whose content is a shared subsequence of this buffer's content. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../java/nio/FloatBuffer.md))`()` Returns a string summarizing the state of this buffer. |
| openstatic [FloatBuffer](../java/nio/FloatBuffer.md)! | [wrap](../java/nio/FloatBuffer.md))`(`array:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!`)` Wraps a float array into a buffer. |
| openstatic [FloatBuffer](../java/nio/FloatBuffer.md)! | [wrap](../java/nio/FloatBuffer.md))`(`array:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!`, `offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `length:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Wraps a float array into a buffer. |
| --- | --- |

| Inherited functions ||
|---|---|
| From class [Buffer](../java/nio/Buffer.md) |------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [capacity](../java/nio/Buffer.md))`()` <br /> Returns this buffer's capacity. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasRemaining](../java/nio/Buffer.md))`()` <br /> Tells whether there are any elements between the current position and the limit. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isReadOnly](../java/nio/Buffer.md))`()` <br /> Tells whether or not this buffer is read-only. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [limit](../java/nio/Buffer.md))`()` <br /> Returns this buffer's limit. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [position](../java/nio/Buffer.md))`()` <br /> Returns this buffer's position. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [remaining](../java/nio/Buffer.md))`()` <br /> Returns the number of elements between the current position and the limit. <br /> | ||

## Public methods

### allocate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun allocate(capacity: Int): FloatBuffer!
```

Allocates a new float buffer.

The new buffer's position will be zero, its limit will be its capacity, its mark will be undefined, each of its elements will be initialized to zero, and its byte order will be the [native order](../java/nio/ByteOrder.md))of the underlying hardware. It will have a [backing array](../java/nio/FloatBuffer.md)), and its [array offset](../java/nio/FloatBuffer.md))will be zero.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------|
| `capacity` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The new buffer's capacity, in floats |

| Return ||
|--------------------------------------------------------------------------------------|----------------------|
| [FloatBuffer](../java/nio/FloatBuffer.md)! | The new float buffer |

| Exceptions ||
|--------------------------------------|---------------------------------------|
| `java.lang.IllegalArgumentException` | If the`capacity`is a negative integer |

### array

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun array(): FloatArray!
```

Returns the float array that backs this buffer*(optional operation)*.

Modifications to this buffer's content will cause the returned array's content to be modified, and vice versa.

Invoke the [hasArray](../java/nio/FloatBuffer.md))method before invoking this method in order to ensure that this buffer has an accessible backing array.

| Return ||
|--------------------------------------------------------------------------------------------|----------------------------------|
| [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)! | The array that backs this buffer |

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

Invoke the [hasArray](../java/nio/FloatBuffer.md))method before invoking this method in order to ensure that this buffer has an accessible backing array.

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
abstract fun asReadOnlyBuffer(): FloatBuffer!
```

Creates a new, read-only float buffer that shares this buffer's content.

The content of the new buffer will be that of this buffer. Changes to this buffer's content will be visible in the new buffer; the new buffer itself, however, will be read-only and will not allow the shared content to be modified. The two buffers' position, limit, and mark values will be independent.

The new buffer's capacity, limit, position, mark values, and byte order will be identical to those of this buffer.

If this buffer is itself read-only then this method behaves in exactly the same way as the [duplicate](../java/nio/FloatBuffer.md))method.

| Return ||
|--------------------------------------------------------------------------------------|---------------------------------|
| [FloatBuffer](../java/nio/FloatBuffer.md)! | The new, read-only float buffer |

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
| [Buffer](../java/nio/Buffer.md)! | This buffer |

### compact

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun compact(): FloatBuffer!
```

Compacts this buffer*(optional operation)*.

The floats between the buffer's current position and its limit, if any, are copied to the beginning of the buffer. That is, the float at index*p* =`position()`is copied to index zero, the float at index*p* + 1 is copied to index one, and so forth until the float at index`limit()`- 1 is copied to index*n* =`limit()`-`1`-*p* . The buffer's position is then set to*n+1*and its limit is set to its capacity. The mark, if defined, is discarded.

The buffer's position is set to the number of floats copied, rather than to zero, so that an invocation of this method can be followed immediately by an invocation of another relative*put*method.

| Return ||
|--------------------------------------------------------------------------------------|-------------|
| [FloatBuffer](../java/nio/FloatBuffer.md)! | This buffer |

| Exceptions ||
|------------------------------------|-----------------------------|
| `java.nio.ReadOnlyBufferException` | If this buffer is read-only |

### compareTo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun compareTo(other: FloatBuffer!): Int
```

Compares this buffer to another.

Two float buffers are compared by comparing their sequences of remaining elements lexicographically, without regard to the starting position of each sequence within its corresponding buffer. Pairs of`float`elements are compared as if by invoking [Float.compare(float,float)](../java/lang/Float.md)), except that`-0.0`and`0.0`are considered to be equal.`Float.NaN`is considered by this method to be equal to itself and greater than all other`float`values (including`Float.POSITIVE_INFINITY`).

A float buffer is not comparable to any other type of object.

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
abstract fun duplicate(): FloatBuffer!
```

Creates a new float buffer that shares this buffer's content.

The content of the new buffer will be that of this buffer. Changes to this buffer's content will be visible in the new buffer, and vice versa; the two buffers' position, limit, and mark values will be independent.

The new buffer's capacity, limit, position, mark values, and byte order will be identical to those of this buffer. The new buffer will be direct if, and only if, this buffer is direct, and it will be read-only if, and only if, this buffer is read-only.

| Return ||
|--------------------------------------------------------------------------------------|----------------------|
| [FloatBuffer](../java/nio/FloatBuffer.md)! | The new float buffer |

### equals

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun equals(other: Any?): Boolean
```

Tells whether or not this buffer is equal to another object.

Two float buffers are equal if, and only if,

1. They have the same element type,
2. They have the same number of remaining elements, and
3. The two sequences of remaining elements, considered independently of their starting positions, are pointwise equal. This method considers two float elements`a`and`b`to be equal if`(a == b) || (Float.isNaN(a) && Float.isNaN(b))`. The values`-0.0`and`+0.0`are considered to be equal, unlike [Float.equals(Object)](../java/lang/Float.md)).
| --- | --- | --- |

A float buffer is not equal to any other type of object.

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

This method is often used in conjunction with the [compact](../java/nio/ByteBuffer.md))method when transferring data from one place to another.

| Return ||
|---------------------------------------------------------------------------|-------------|
| [Buffer](../java/nio/Buffer.md)! | This buffer |

### get

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun get(): Float
```

Relative*get*method. Reads the float at this buffer's current position, and then increments the position.

| Return ||
|--------------------------------------------------------------------------------|--------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | The float at the buffer's current position |

| Exceptions ||
|-------------------------------------|----------------------------------------------------------------|
| `java.nio.BufferUnderflowException` | If the buffer's current position is not smaller than its limit |

### get

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun get(dst: FloatArray!): FloatBuffer!
```

Relative bulk*get*method.

This method transfers floats from this buffer into the given destination array. An invocation of this method of the form`src.get(a)`behaves in exactly the same way as the invocation 

```kotlin
src.get(a, 0, a.length) 
```

| Parameters ||
|-------|------------------------------------------------------------------------------------------------------------------|
| `dst` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!:The destination array |

| Return ||
|--------------------------------------------------------------------------------------|-------------|
| [FloatBuffer](../java/nio/FloatBuffer.md)! | This buffer |

| Exceptions ||
|-------------------------------------|----------------------------------------------------------------|
| `java.nio.BufferUnderflowException` | If there are fewer than`length`floats remaining in this buffer |

### get

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun get(
    dst: FloatArray!, 
    offset: Int, 
    length: Int
): FloatBuffer!
```

Relative bulk*get*method.

This method transfers floats from this buffer into the given destination array. If there are fewer floats remaining in the buffer than are required to satisfy the request, that is, if`length``>``remaining()`, then no floats are transferred and a [BufferUnderflowException](../java/nio/BufferUnderflowException.md) is thrown.

Otherwise, this method copies`length`floats from this buffer into the given array, starting at the current position of this buffer and at the given offset in the array. The position of this buffer is then incremented by`length`.

In other words, an invocation of this method of the form`src.get(dst, off, len)`has exactly the same effect as the loop 

```kotlin
<code>for (int i = off; i &lt; off + len; i++)
          dst[i] = src.get();
  </code>
```
except that it first checks that there are sufficient floats in this buffer and it is potentially much more efficient.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dst` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!:The array into which floats are to be written |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The offset within the array of the first float to be written; must be non-negative and no larger than`dst.length` |
| `length` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The maximum number of floats to be written to the given array; must be non-negative and no larger than`dst.length - offset` |
| --- | --- |

| Return ||
|--------------------------------------------------------------------------------------|-------------|
| [FloatBuffer](../java/nio/FloatBuffer.md)! | This buffer |

| Exceptions ||
|---------------------------------------|----------------------------------------------------------------------|
| `java.nio.BufferUnderflowException` | If there are fewer than`length`floats remaining in this buffer |
| `java.lang.IndexOutOfBoundsException` | If the preconditions on the`offset`and`length`parameters do not hold |

### get

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun get(index: Int): Float
```

Absolute*get*method. Reads the float at the given index.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The index from which the float will be read |

| Return ||
|--------------------------------------------------------------------------------|------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | The float at the given index |

| Exceptions ||
|---------------------------------------|-------------------------------------------------------------|
| `java.lang.IndexOutOfBoundsException` | If`index`is negative or not smaller than the buffer's limit |

### get

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun get(
    index: Int, 
    dst: FloatArray!
): FloatBuffer!
```

Absolute bulk*get*method.

This method transfers floats from this buffer into the given destination array. The position of this buffer is unchanged. An invocation of this method of the form`src.get(index, dst)`behaves in exactly the same way as the invocation: 

```kotlin
src.get(index, dst, 0, dst.length) 
```

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The index in this buffer from which the first float will be read; must be non-negative and less than`limit()` |
| `dst` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!:The destination array |

| Return ||
|--------------------------------------------------------------------------------------|-------------|
| [FloatBuffer](../java/nio/FloatBuffer.md)! | This buffer |

| Exceptions ||
|---------------------------------------|-----------------------------------------------------------------------------------|
| `java.lang.IndexOutOfBoundsException` | If`index`is negative, not smaller than`limit()`, or`limit() - index < dst.length` |

### get

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun get(
    index: Int, 
    dst: FloatArray!, 
    offset: Int, 
    length: Int
): FloatBuffer!
```

Absolute bulk*get*method.

This method transfers`length`floats from this buffer into the given array, starting at the given index in this buffer and at the given offset in the array. The position of this buffer is unchanged.

An invocation of this method of the form`src.get(index, dst, offset, length)`has exactly the same effect as the following loop except that it first checks the consistency of the supplied parameters and it is potentially much more efficient: 

```kotlin
<code>for (int i = offset, j = index; i &lt; offset + length; i++, j++)
          dst[i] = src.get(j);
  </code>
```

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The index in this buffer from which the first float will be read; must be non-negative and less than`limit()` |
| `dst` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!:The destination array |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The offset within the array of the first float to be written; must be non-negative and less than`dst.length` |
| --- | --- |
| `length` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The number of floats to be written to the given array; must be non-negative and no larger than the smaller of`limit() - index`and`dst.length - offset` |

| Return ||
|--------------------------------------------------------------------------------------|-------------|
| [FloatBuffer](../java/nio/FloatBuffer.md)! | This buffer |

| Exceptions ||
|---------------------------------------|--------------------------------------------------------------------------------|
| `java.lang.IndexOutOfBoundsException` | If the preconditions on the`index`,`offset`, and`length`parameters do not hold |

### hasArray

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hasArray(): Boolean
```

Tells whether or not this buffer is backed by an accessible float array.

If this method returns`true`then the [array](../java/nio/FloatBuffer.md))and [arrayOffset](../java/nio/FloatBuffer.md))methods may safely be invoked.

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if, and only if, this buffer is backed by an array and is not read-only |

### hashCode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hashCode(): Int
```

Returns the current hash code of this buffer.

The hash code of a float buffer depends only upon its remaining elements; that is, upon the elements from`position()`up to, and including, the element at`limit()`-`1`.

Because buffer hash codes are content-dependent, it is inadvisable to use buffers as keys in hash maps or similar data structures unless it is known that their contents will not change.

| Return ||
|----------------------------------------------------------------------------|--------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The current hash code of this buffer |

### isDirect

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isDirect(): Boolean
```

Tells whether or not this float buffer is direct.

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
| [Buffer](../java/nio/Buffer.md)! | This buffer |

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
| [Buffer](../java/nio/Buffer.md)! | This buffer |

### mismatch

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun mismatch(that: FloatBuffer!): Int
```

Finds and returns the relative index of the first mismatch between this buffer and a given buffer. The index is relative to the [position](../java/nio/Buffer.md))of each buffer and will be in the range of 0 (inclusive) up to the smaller of the [remaining](../java/nio/Buffer.md))elements in each buffer (exclusive).

If the two buffers share a common prefix then the returned index is the length of the common prefix and it follows that there is a mismatch between the two buffers at that index within the respective buffers. If one buffer is a proper prefix of the other then the returned index is the smaller of the remaining elements in each buffer, and it follows that the index is only valid for the buffer with the larger number of remaining elements. Otherwise, there is no mismatch.

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| `that` | [FloatBuffer](../java/nio/FloatBuffer.md)!:The byte buffer to be tested for a mismatch with this buffer |

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The relative index of the first mismatch between this and the given buffer, otherwise -1 if no mismatch. |

### order

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun order(): ByteOrder!
```

Retrieves this buffer's byte order.

The byte order of a float buffer created by allocation or by wrapping an existing`float`array is the [native order](../java/nio/ByteOrder.md))of the underlying hardware. The byte order of a float buffer created as a [view](../java/nio/ByteBuffer.md) of a byte buffer is that of the byte buffer at the moment that the view is created.

| Return ||
|---------------------------------------------------------------------------------|--------------------------|
| [ByteOrder](../java/nio/ByteOrder.md)! | This buffer's byte order |

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
| [Buffer](../java/nio/Buffer.md)! | This buffer |

| Exceptions ||
|--------------------------------------|-------------------------------------------------|
| `java.lang.IllegalArgumentException` | If the preconditions on`newPosition`do not hold |

### put

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun put(f: Float): FloatBuffer!
```

Relative*put* method*(optional operation)*.

Writes the given float into this buffer at the current position, and then increments the position.

| Parameters ||
|-----|--------------------------------------------------------------------------------------------------------|
| `f` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The float to be written |

| Return ||
|--------------------------------------------------------------------------------------|-------------|
| [FloatBuffer](../java/nio/FloatBuffer.md)! | This buffer |

| Exceptions ||
|------------------------------------|-----------------------------------------------------------------|
| `java.nio.BufferOverflowException` | If this buffer's current position is not smaller than its limit |
| `java.nio.ReadOnlyBufferException` | If this buffer is read-only |

### put

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun put(src: FloatArray!): FloatBuffer!
```

Relative bulk*put* method*(optional operation)*.

This method transfers the entire content of the given source float array into this buffer. An invocation of this method of the form`dst.put(a)`behaves in exactly the same way as the invocation 

```kotlin
dst.put(a, 0, a.length) 
```

| Parameters ||
|-------|-------------------------------------------------------------------------------------------------------------|
| `src` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!:The source array |

| Return ||
|--------------------------------------------------------------------------------------|-------------|
| [FloatBuffer](../java/nio/FloatBuffer.md)! | This buffer |

| Exceptions ||
|------------------------------------|-----------------------------------------------|
| `java.nio.BufferOverflowException` | If there is insufficient space in this buffer |
| `java.nio.ReadOnlyBufferException` | If this buffer is read-only |

### put

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun put(
    src: FloatArray!, 
    offset: Int, 
    length: Int
): FloatBuffer!
```

Relative bulk*put* method*(optional operation)*.

This method transfers floats into this buffer from the given source array. If there are more floats to be copied from the array than remain in this buffer, that is, if`length``>``remaining()`, then no floats are transferred and a [BufferOverflowException](../java/nio/BufferOverflowException.md) is thrown.

Otherwise, this method copies`length`floats from the given array into this buffer, starting at the given offset in the array and at the current position of this buffer. The position of this buffer is then incremented by`length`.

In other words, an invocation of this method of the form`dst.put(src, off, len)`has exactly the same effect as the loop 

```kotlin
<code>for (int i = off; i &lt; off + len; i++)
          dst.put(src[i]);
  </code>
```
except that it first checks that there is sufficient space in this buffer and it is potentially much more efficient.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `src` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!:The array from which floats are to be read |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The offset within the array of the first float to be read; must be non-negative and no larger than`src.length` |
| `length` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The number of floats to be read from the given array; must be non-negative and no larger than`src.length - offset` |
| --- | --- |

| Return ||
|--------------------------------------------------------------------------------------|-------------|
| [FloatBuffer](../java/nio/FloatBuffer.md)! | This buffer |

| Exceptions ||
|---------------------------------------|----------------------------------------------------------------------|
| `java.nio.BufferOverflowException` | If there is insufficient space in this buffer |
| `java.lang.IndexOutOfBoundsException` | If the preconditions on the`offset`and`length`parameters do not hold |
| `java.nio.ReadOnlyBufferException` | If this buffer is read-only |
| --- | --- |

### put

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun put(
    index: Int, 
    f: Float
): FloatBuffer!
```

Absolute*put* method*(optional operation)*.

Writes the given float into this buffer at the given index.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The index at which the float will be written |
| `f` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The float value to be written |

| Return ||
|--------------------------------------------------------------------------------------|-------------|
| [FloatBuffer](../java/nio/FloatBuffer.md)! | This buffer |

| Exceptions ||
|---------------------------------------|-------------------------------------------------------------|
| `java.lang.IndexOutOfBoundsException` | If`index`is negative or not smaller than the buffer's limit |
| `java.nio.ReadOnlyBufferException` | If this buffer is read-only |

### put

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun put(
    index: Int, 
    src: FloatArray!
): FloatBuffer!
```

Absolute bulk*put* method*(optional operation)*.

This method copies floats into this buffer from the given source array. The position of this buffer is unchanged. An invocation of this method of the form`dst.put(index, src)`behaves in exactly the same way as the invocation: 

```kotlin
dst.put(index, src, 0, src.length); 
```

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The index in this buffer at which the first float will be written; must be non-negative and less than`limit()` |
| `src` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!:The array from which floats are to be read |

| Return ||
|--------------------------------------------------------------------------------------|-------------|
| [FloatBuffer](../java/nio/FloatBuffer.md)! | This buffer |

| Exceptions ||
|---------------------------------------|-----------------------------------------------------------------------------------|
| `java.lang.IndexOutOfBoundsException` | If`index`is negative, not smaller than`limit()`, or`limit() - index < src.length` |
| `java.nio.ReadOnlyBufferException` | If this buffer is read-only |

### put

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun put(
    index: Int, 
    src: FloatArray!, 
    offset: Int, 
    length: Int
): FloatBuffer!
```

Absolute bulk*put* method*(optional operation)*.

This method transfers`length`floats from the given array, starting at the given offset in the array and at the given index in this buffer. The position of this buffer is unchanged.

An invocation of this method of the form`dst.put(index, src, offset, length)`has exactly the same effect as the following loop except that it first checks the consistency of the supplied parameters and it is potentially much more efficient: 

```kotlin
<code>for (int i = offset, j = index; i &lt; offset + length; i++, j++)
          dst.put(j, src[i]);
  </code>
```

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The index in this buffer at which the first float will be written; must be non-negative and less than`limit()` |
| `src` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!:The array from which floats are to be read |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The offset within the array of the first float to be read; must be non-negative and less than`src.length` |
| --- | --- |
| `length` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The number of floats to be read from the given array; must be non-negative and no larger than the smaller of`limit() - index`and`src.length - offset` |

| Return ||
|--------------------------------------------------------------------------------------|-------------|
| [FloatBuffer](../java/nio/FloatBuffer.md)! | This buffer |

| Exceptions ||
|---------------------------------------|--------------------------------------------------------------------------------|
| `java.lang.IndexOutOfBoundsException` | If the preconditions on the`index`,`offset`, and`length`parameters do not hold |
| `java.nio.ReadOnlyBufferException` | If this buffer is read-only |

### put

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun put(
    index: Int, 
    src: FloatBuffer!, 
    offset: Int, 
    length: Int
): FloatBuffer!
```

Absolute bulk*put* method*(optional operation)*.

This method transfers`length`floats into this buffer from the given source buffer, starting at the given`offset`in the source buffer and the given`index`in this buffer. The positions of both buffers are unchanged.

In other words, an invocation of this method of the form`dst.put(index, src, offset, length)`has exactly the same effect as the loop 

```kotlin
<code>for (int i = offset, j = index; i &lt; offset + length; i++, j++)
      dst.put(j, src.get(i));
  </code>
```
except that it first checks the consistency of the supplied parameters and it is potentially much more efficient. If this buffer and the source buffer share the same backing array or memory, then the result will be as if the source elements were first copied to an intermediate location before being written into this buffer.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The index in this buffer at which the first float will be written; must be non-negative and less than`limit()` |
| `src` | [FloatBuffer](../java/nio/FloatBuffer.md)!:The buffer from which floats are to be read |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The index within the source buffer of the first float to be read; must be non-negative and less than`src.limit()` |
| --- | --- |
| `length` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The number of floats to be read from the given buffer; must be non-negative and no larger than the smaller of`limit() - index`and`src.limit() - offset` |

| Return ||
|--------------------------------------------------------------------------------------|-------------|
| [FloatBuffer](../java/nio/FloatBuffer.md)! | This buffer |

| Exceptions ||
|---------------------------------------|--------------------------------------------------------------------------------|
| `java.lang.IndexOutOfBoundsException` | If the preconditions on the`index`,`offset`, and`length`parameters do not hold |
| `java.nio.ReadOnlyBufferException` | If this buffer is read-only |

### put

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun put(src: FloatBuffer!): FloatBuffer!
```

Relative bulk*put* method*(optional operation)*.

This method transfers the floats remaining in the given source buffer into this buffer. If there are more floats remaining in the source buffer than in this buffer, that is, if`src.remaining()``>``remaining()`, then no floats are transferred and a [BufferOverflowException](../java/nio/BufferOverflowException.md) is thrown.

Otherwise, this method copies*n* =`src.remaining()`floats from the given buffer into this buffer, starting at each buffer's current position. The positions of both buffers are then incremented by*n*.

In other words, an invocation of this method of the form`dst.put(src)`has exactly the same effect as the loop 

```kotlin
while (src.hasRemaining())
          dst.put(src.get()); 
```
except that it first checks that there is sufficient space in this buffer and it is potentially much more efficient. If this buffer and the source buffer share the same backing array or memory, then the result will be as if the source elements were first copied to an intermediate location before being written into this buffer.

| Parameters ||
|-------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `src` | [FloatBuffer](../java/nio/FloatBuffer.md)!:The source buffer from which floats are to be read; must not be this buffer |

| Return ||
|--------------------------------------------------------------------------------------|-------------|
| [FloatBuffer](../java/nio/FloatBuffer.md)! | This buffer |

| Exceptions ||
|--------------------------------------|---------------------------------------------------------------------------------------------|
| `java.nio.BufferOverflowException` | If there is insufficient space in this buffer for the remaining floats in the source buffer |
| `java.lang.IllegalArgumentException` | If the source buffer is this buffer |
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
| [Buffer](../java/nio/Buffer.md)! | This buffer |

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
| [Buffer](../java/nio/Buffer.md)! | This buffer |

### slice

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun slice(): FloatBuffer!
```

Creates a new float buffer whose content is a shared subsequence of this buffer's content.

The content of the new buffer will start at this buffer's current position. Changes to this buffer's content will be visible in the new buffer, and vice versa; the two buffers' position, limit, and mark values will be independent.

The new buffer's position will be zero, its capacity and its limit will be the number of floats remaining in this buffer, its mark will be undefined, and its byte order will be identical to that of this buffer. The new buffer will be direct if, and only if, this buffer is direct, and it will be read-only if, and only if, this buffer is read-only.

| Return ||
|--------------------------------------------------------------------------------------|----------------------|
| [FloatBuffer](../java/nio/FloatBuffer.md)! | The new float buffer |

### slice

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun slice(
    index: Int, 
    length: Int
): FloatBuffer!
```

Creates a new float buffer whose content is a shared subsequence of this buffer's content.

The content of the new buffer will start at position`index`in this buffer, and will contain`length`elements. Changes to this buffer's content will be visible in the new buffer, and vice versa; the two buffers' position, limit, and mark values will be independent.

The new buffer's position will be zero, its capacity and its limit will be`length`, its mark will be undefined, and its byte order will be identical to that of this buffer. The new buffer will be direct if, and only if, this buffer is direct, and it will be read-only if, and only if, this buffer is read-only.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The position in this buffer at which the content of the new buffer will start; must be non-negative and no larger than [limit()](../java/nio/Buffer.md)) |
| `length` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The number of elements the new buffer will contain; must be non-negative and no larger than`limit() - index` |

| Return ||
|--------------------------------------------------------------------------------------|----------------|
| [FloatBuffer](../java/nio/FloatBuffer.md)! | The new buffer |

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
open static fun wrap(array: FloatArray!): FloatBuffer!
```

Wraps a float array into a buffer.

The new buffer will be backed by the given float array; that is, modifications to the buffer will cause the array to be modified and vice versa. The new buffer's capacity and limit will be`array.length`, its position will be zero, its mark will be undefined, and its byte order will be the [native order](../java/nio/ByteOrder.md))of the underlying hardware. Its [backing array](../java/nio/FloatBuffer.md))will be the given array, and its [array offset](../java/nio/FloatBuffer.md))will be zero.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------|
| `array` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!:The array that will back this buffer |

| Return ||
|--------------------------------------------------------------------------------------|----------------------|
| [FloatBuffer](../java/nio/FloatBuffer.md)! | The new float buffer |

### wrap

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun wrap(
    array: FloatArray!, 
    offset: Int, 
    length: Int
): FloatBuffer!
```

Wraps a float array into a buffer.

The new buffer will be backed by the given float array; that is, modifications to the buffer will cause the array to be modified and vice versa. The new buffer's capacity will be`array.length`, its position will be`offset`, its limit will be`offset + length`, its mark will be undefined, and its byte order will be the [native order](../java/nio/ByteOrder.md))of the underlying hardware. Its [backing array](../java/nio/FloatBuffer.md))will be the given array, and its [array offset](../java/nio/FloatBuffer.md))will be zero.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `array` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!:The array that will back the new buffer |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The offset of the subarray to be used; must be non-negative and no larger than`array.length`. The new buffer's position will be set to this value. |
| `length` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The length of the subarray to be used; must be non-negative and no larger than`array.length - offset`. The new buffer's limit will be set to`offset + length`. |
| --- | --- |

| Return ||
|--------------------------------------------------------------------------------------|----------------------|
| [FloatBuffer](../java/nio/FloatBuffer.md)! | The new float buffer |

| Exceptions ||
|---------------------------------------|----------------------------------------------------------------------|
| `java.lang.IndexOutOfBoundsException` | If the preconditions on the`offset`and`length`parameters do not hold |
