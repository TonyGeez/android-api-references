# Buffer

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Buffer

```
abstract class Buffer
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.nio.Buffer](Buffer.md) |

| Known Direct Subclasses [ByteBuffer](ByteBuffer.md), [CharBuffer](CharBuffer.md), [DoubleBuffer](DoubleBuffer.md), [FloatBuffer](FloatBuffer.md), [IntBuffer](IntBuffer.md), [LongBuffer](LongBuffer.md), [ShortBuffer](ShortBuffer.md) |--------------------------------------------------------------------------------------|------------------| | [ByteBuffer](ByteBuffer.md) | A byte buffer. | | [CharBuffer](CharBuffer.md) | A char buffer. | | [DoubleBuffer](DoubleBuffer.md) | A double buffer. | | [FloatBuffer](FloatBuffer.md) | A float buffer. | | [IntBuffer](IntBuffer.md) | An int buffer. | | [LongBuffer](LongBuffer.md) | A long buffer. | | [ShortBuffer](ShortBuffer.md) | A short buffer. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [MappedByteBuffer](MappedByteBuffer.md) |----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------| | [MappedByteBuffer](MappedByteBuffer.md) | A direct byte buffer whose content is a memory-mapped region of a file. | |
| --- | --- | --- | --- | --- | --- | --- |

A container for data of a specific primitive type.

A buffer is a linear, finite sequence of elements of a specific primitive type. Aside from its content, the essential properties of a buffer are its capacity, limit, and position:

A buffer's*capacity*is the number of elements it contains. The capacity of a buffer is never negative and never changes.

A buffer's*limit*is the index of the first element that should not be read or written. A buffer's limit is never negative and is never greater than its capacity.

A buffer's*position*is the index of the next element to be read or written. A buffer's position is never negative and is never greater than its limit.

There is one subclass of this class for each non-boolean primitive type.

## Transferring data

Each subclass of this class defines two categories of*get* and*put*operations:

*Relative* operations read or write one or more elements starting at the current position and then increment the position by the number of elements transferred. If the requested transfer exceeds the limit then a relative*get* operation throws a [BufferUnderflowException](BufferUnderflowException.md) and a relative*put* operation throws a [BufferOverflowException](BufferOverflowException.md); in either case, no data is transferred.

*Absolute* operations take an explicit element index and do not affect the position. Absolute*get* and*put* operations throw an [IndexOutOfBoundsException](../java.lang/IndexOutOfBoundsException.md) if the index argument exceeds the limit.

Data may also, of course, be transferred in to or out of a buffer by the I/O operations of an appropriate channel, which are always relative to the current position.

## Marking and resetting

A buffer's*mark* is the index to which its position will be reset when the [reset](Buffer.md))method is invoked. The mark is not always defined, but when it is defined it is never negative and is never greater than the position. If the mark is defined then it is discarded when the position or the limit is adjusted to a value smaller than the mark. If the mark is not defined then invoking the [reset](Buffer.md))method causes an [InvalidMarkException](InvalidMarkException.md) to be thrown.

## Invariants

The following invariant holds for the mark, position, limit, and capacity values:
`0``<=`*mark* `<=`*position* `<=`*limit* `<=`*capacity*

A newly-created buffer always has a position of zero and a mark that is undefined. The initial limit may be zero, or it may be some other value that depends upon the type of the buffer and the manner in which it is constructed. Each element of a newly-allocated buffer is initialized to zero.

## Additional operations

In addition to methods for accessing the position, limit, and capacity values and for marking and resetting, this class also defines the following operations upon buffers:

- [clear](Buffer.md))makes a buffer ready for a new sequence of channel-read or relative*put*operations: It sets the limit to the capacity and the position to zero.
- [flip](Buffer.md))makes a buffer ready for a new sequence of channel-write or relative*get*operations: It sets the limit to the current position and then sets the position to zero.
- [rewind](Buffer.md))makes a buffer ready for re-reading the data that it already contains: It leaves the limit unchanged and sets the position to zero.
- The #slice and [slice(index,length)](Buffer.md))methods create a subsequence of a buffer: They leave the limit and the position unchanged.
- [duplicate](Buffer.md))creates a shallow copy of a buffer: It leaves the limit and the position unchanged.

## Read-only buffers

Every buffer is readable, but not every buffer is writable. The mutation methods of each buffer class are specified as*optional operations* that will throw a [ReadOnlyBufferException](ReadOnlyBufferException.md) when invoked upon a read-only buffer. A read-only buffer does not allow its content to be changed, but its mark, position, and limit values are mutable. Whether or not a buffer is read-only may be determined by invoking its [isReadOnly](Buffer.md))method.

## Thread safety

Buffers are not safe for use by multiple concurrent threads. If a buffer is to be used by more than one thread then access to the buffer should be controlled by appropriate synchronization.

## Invocation chaining

Methods in this class that do not otherwise have a value to return are specified to return the buffer upon which they are invoked. This allows method invocations to be chained; for example, the sequence of statements 

```kotlin
b.flip();
  b.position(23);
  b.limit(42);
```
can be replaced by the single, more compact statement 

```kotlin
b.flip().position(23).limit(42);
```

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [array](Buffer.md))`()` Returns the array that backs this buffer*(optional operation)*. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [arrayOffset](Buffer.md))`()` Returns the offset within this buffer's backing array of the first element of the buffer*(optional operation)*. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [capacity](Buffer.md))`()` Returns this buffer's capacity. |
| --- | --- |
| open [Buffer](Buffer.md)! | [clear](Buffer.md))`()` Clears this buffer. |
| abstract [Buffer](Buffer.md)! | [duplicate](Buffer.md))`()` Creates a new buffer that shares this buffer's content. |
| open [Buffer](Buffer.md)! | [flip](Buffer.md))`()` Flips this buffer. |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasArray](Buffer.md))`()` Tells whether or not this buffer is backed by an accessible array. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasRemaining](Buffer.md))`()` Tells whether there are any elements between the current position and the limit. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isDirect](Buffer.md))`()` Tells whether or not this buffer is [*direct*](ByteBuffer.md). |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isReadOnly](Buffer.md))`()` Tells whether or not this buffer is read-only. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [limit](Buffer.md))`()` Returns this buffer's limit. |
| open [Buffer](Buffer.md)! | [limit](Buffer.md))`(`newLimit:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets this buffer's limit. |
| --- | --- |
| open [Buffer](Buffer.md)! | [mark](Buffer.md))`()` Sets this buffer's mark at its position. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [position](Buffer.md))`()` Returns this buffer's position. |
| open [Buffer](Buffer.md)! | [position](Buffer.md))`(`newPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets this buffer's position. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [remaining](Buffer.md))`()` Returns the number of elements between the current position and the limit. |
| open [Buffer](Buffer.md)! | [reset](Buffer.md))`()` Resets this buffer's position to the previously-marked position. |
| open [Buffer](Buffer.md)! | [rewind](Buffer.md))`()` Rewinds this buffer. |
| --- | --- |
| abstract [Buffer](Buffer.md)! | [slice](Buffer.md))`()` Creates a new buffer whose content is a shared subsequence of this buffer's content. |
| abstract [Buffer](Buffer.md)! | [slice](Buffer.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `length:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a new buffer whose content is a shared subsequence of this buffer's content. |

## Public methods

### array

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun array(): Any!
```

Returns the array that backs this buffer*(optional operation)*.

This method is intended to allow array-backed buffers to be passed to native code more efficiently. Concrete subclasses provide more strongly-typed return values for this method.

Modifications to this buffer's content will cause the returned array's content to be modified, and vice versa.

Invoke the [hasArray](Buffer.md))method before invoking this method in order to ensure that this buffer has an accessible backing array.

| Return ||
|-----------------------------------------------------------------------------|----------------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | The array that backs this buffer |

| Exceptions ||
|-------------------------------------------|-------------------------------------------------------|
| `java.nio.ReadOnlyBufferException` | If this buffer is backed by an array but is read-only |
| `java.lang.UnsupportedOperationException` | If this buffer is not backed by an accessible array |

### arrayOffset

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun arrayOffset(): Int
```

Returns the offset within this buffer's backing array of the first element of the buffer*(optional operation)*.

If this buffer is backed by an array then buffer position*p* corresponds to array index*p* +`arrayOffset()`.

Invoke the [hasArray](Buffer.md))method before invoking this method in order to ensure that this buffer has an accessible backing array.

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The offset within this buffer's array of the first element of the buffer |

| Exceptions ||
|-------------------------------------------|-------------------------------------------------------|
| `java.nio.ReadOnlyBufferException` | If this buffer is backed by an array but is read-only |
| `java.lang.UnsupportedOperationException` | If this buffer is not backed by an accessible array |

### capacity

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun capacity(): Int
```

Returns this buffer's capacity.

| Return ||
|----------------------------------------------------------------------------|-----------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The capacity of this buffer |

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
|----------------------------------------------------------------------------|-------------|
| [Buffer](Buffer.md)! | This buffer |

### duplicate

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun duplicate(): Buffer!
```

Creates a new buffer that shares this buffer's content.

The content of the new buffer will be that of this buffer. Changes to this buffer's content will be visible in the new buffer, and vice versa; the two buffers' position, limit, and mark values will be independent.

The new buffer's capacity, limit, position and mark values will be identical to those of this buffer. The new buffer will be direct if, and only if, this buffer is direct, and it will be read-only if, and only if, this buffer is read-only.

| Return ||
|----------------------------------------------------------------------------|----------------|
| [Buffer](Buffer.md)! | The new buffer |

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
|----------------------------------------------------------------------------|-------------|
| [Buffer](Buffer.md)! | This buffer |

### hasArray

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun hasArray(): Boolean
```

Tells whether or not this buffer is backed by an accessible array.

If this method returns`true`then the [array](Buffer.md))and [arrayOffset](Buffer.md))methods may safely be invoked.

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if, and only if, this buffer is backed by an array and is not read-only |

### hasRemaining

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hasRemaining(): Boolean
```

Tells whether there are any elements between the current position and the limit.

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if, and only if, there is at least one element remaining in this buffer |

### isDirect

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isDirect(): Boolean
```

Tells whether or not this buffer is [*direct*](ByteBuffer.md).

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if, and only if, this buffer is direct |

### isReadOnly

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isReadOnly(): Boolean
```

Tells whether or not this buffer is read-only.

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if, and only if, this buffer is read-only |

### limit

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun limit(): Int
```

Returns this buffer's limit.

| Return ||
|----------------------------------------------------------------------------|--------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The limit of this buffer |

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
|----------------------------------------------------------------------------|-------------|
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
|----------------------------------------------------------------------------|-------------|
| [Buffer](Buffer.md)! | This buffer |

### position

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun position(): Int
```

Returns this buffer's position.

| Return ||
|----------------------------------------------------------------------------|-----------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The position of this buffer |

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
|----------------------------------------------------------------------------|-------------|
| [Buffer](Buffer.md)! | This buffer |

| Exceptions ||
|--------------------------------------|-------------------------------------------------|
| `java.lang.IllegalArgumentException` | If the preconditions on`newPosition`do not hold |

### remaining

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun remaining(): Int
```

Returns the number of elements between the current position and the limit.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The number of elements remaining in this buffer |

### reset

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun reset(): Buffer!
```

Resets this buffer's position to the previously-marked position.

Invoking this method neither changes nor discards the mark's value.

| Return ||
|----------------------------------------------------------------------------|-------------|
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
|----------------------------------------------------------------------------|-------------|
| [Buffer](Buffer.md)! | This buffer |

### slice

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun slice(): Buffer!
```

Creates a new buffer whose content is a shared subsequence of this buffer's content.

The content of the new buffer will start at this buffer's current position. Changes to this buffer's content will be visible in the new buffer, and vice versa; the two buffers' position, limit, and mark values will be independent.

The new buffer's position will be zero, its capacity and its limit will be the number of elements remaining in this buffer, its mark will be undefined. The new buffer will be direct if, and only if, this buffer is direct, and it will be read-only if, and only if, this buffer is read-only.

| Return ||
|----------------------------------------------------------------------------|----------------|
| [Buffer](Buffer.md)! | The new buffer |

### slice

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun slice(
    index: Int, 
    length: Int
): Buffer!
```

Creates a new buffer whose content is a shared subsequence of this buffer's content.

The content of the new buffer will start at position`index`in this buffer, and will contain`length`elements. Changes to this buffer's content will be visible in the new buffer, and vice versa; the two buffers' position, limit, and mark values will be independent.

The new buffer's position will be zero, its capacity and its limit will be`length`, its mark will be undefined. The new buffer will be direct if, and only if, this buffer is direct, and it will be read-only if, and only if, this buffer is read-only.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The position in this buffer at which the content of the new buffer will start; must be non-negative and no larger than [limit()](Buffer.md)) |
| `length` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The number of elements the new buffer will contain; must be non-negative and no larger than`limit() - index` |

| Return ||
|----------------------------------------------------------------------------|----------------|
| [Buffer](Buffer.md)! | The new buffer |

| Exceptions ||
|---------------------------------------|-------------------------------------------------------------------------------------------------|
| `java.lang.IndexOutOfBoundsException` | If`index`is negative or greater than`limit()`,`length`is negative, or`length > limit() - index` |
