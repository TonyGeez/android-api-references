# CharBuffer

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CharBuffer

```
abstract class CharBuffer : Buffer, Appendable, CharSequence, Comparable<CharBuffer!>, Readable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| ↳ | [java.nio.Buffer](https://developer.android.com/reference/kotlin/java/nio/Buffer) ||
| | ↳ | [java.nio.CharBuffer](https://developer.android.com/reference/kotlin/java/nio/CharBuffer#) |

A char buffer.

This class defines four categories of operations upon char buffers:

- Absolute and relative [*get*](https://developer.android.com/reference/kotlin/java/nio/CharBuffer#get())and [*put*](https://developer.android.com/reference/kotlin/java/nio/CharBuffer#put(kotlin.Char))methods that read and write single chars;
- Absolute and relative [*bulk get*](https://developer.android.com/reference/kotlin/java/nio/CharBuffer#get(kotlin.CharArray))methods that transfer contiguous sequences of chars from this buffer into an array; and
- Absolute and relative [*bulk put*](https://developer.android.com/reference/kotlin/java/nio/CharBuffer#put(kotlin.CharArray))methods that transfer contiguous sequences of chars from a char array, string, or some other char buffer into this buffer; and
- A method for [compacting](https://developer.android.com/reference/kotlin/java/nio/CharBuffer#compact())a char buffer.

Char buffers can be created either by [*allocation*](https://developer.android.com/reference/kotlin/java/nio/CharBuffer#allocate(kotlin.Int)), which allocates space for the buffer's content, by [*wrapping*](https://developer.android.com/reference/kotlin/java/nio/CharBuffer#wrap(kotlin.CharArray))an existing char array or string into a buffer, or by creating a [*view*](https://developer.android.com/reference/kotlin/java/nio/ByteBuffer#views) of an existing byte buffer.

Like a byte buffer, a char buffer is either [*direct* or*non-direct*](https://developer.android.com/reference/kotlin/java/nio/ByteBuffer#direct). A char buffer created via the`wrap`methods of this class will be non-direct. A char buffer created as a view of a byte buffer will be direct if, and only if, the byte buffer itself is direct. Whether or not a char buffer is direct may be determined by invoking the [isDirect](https://developer.android.com/reference/kotlin/java/nio/CharBuffer#isDirect())method.

This class implements the [CharSequence](https://developer.android.com/reference/kotlin/java/lang/CharSequence.html#) interface so that character buffers may be used wherever character sequences are accepted, for example in the regular-expression package [java.util.regex](https://developer.android.com/reference/kotlin/java/util/regex/package-summary.html). The methods defined by`CharSequence`operate relative to the current position of the buffer when they are invoked.

Methods in this class that do not otherwise have a value to return are specified to return the buffer upon which they are invoked. This allows method invocations to be chained. The sequence of statements 

```kotlin
cb.put("text/");
  cb.put(subtype);
  cb.put("; charset=");
  cb.put(enc);
```
can, for example, be replaced by the single statement 

```kotlin
cb.put("text/").put(subtype).put("; charset=").put(enc);
```

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [CharBuffer](https://developer.android.com/reference/kotlin/java/nio/CharBuffer#)! | [allocate](https://developer.android.com/reference/kotlin/java/nio/CharBuffer#allocate(kotlin.Int))`(`capacity:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Allocates a new char buffer. |
| open [CharBuffer](https://developer.android.com/reference/kotlin/java/nio/CharBuffer#) | [append](https://developer.android.com/reference/kotlin/java/nio/CharBuffer#append(kotlin.Char))`(`c:` ` [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)`)` Appends the specified char to this buffer*(optional operation)*. |
| open [CharBuffer](https://developer.android.com/reference/kotlin/java/nio/CharBuffer#) | [append](https://developer.android.com/reference/kotlin/java/nio/CharBuffer#append(kotlin.CharSequence))`(`csq:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)?`)` Appends the specified character sequence to this buffer*(optional operation)*. |
| open [CharBuffer](https://developer.android.com/reference/kotlin/java/nio/CharBuffer#) | [append](https://developer.android.com/reference/kotlin/java/nio/CharBuffer#append(kotlin.CharSequence,%20kotlin.Int,%20kotlin.Int))`(`csq:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)?`, `start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `end:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Appends a subsequence of the specified character sequence to this buffer*(optional operation)*. |
| [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)! | [array](https://developer.android.com/reference/kotlin/java/nio/CharBuffer#array())`()` Returns the char array that backs this buffer*(optional operation)*. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [arrayOffset](https://developer.android.com/reference/kotlin/java/nio/CharBuffer#arrayOffset())`()` Returns the offset within this buffer's backing array of the first element of the buffer*(optional operation)*. |
| abstract [CharBuffer](https://developer.android.com/reference/kotlin/java/nio/CharBuffer#)! | [asReadOnlyBuffer](https://developer.android.com/reference/kotlin/java/nio/CharBuffer#asReadOnlyBuffer())`()` Creates a new, read-only char buffer that shares this buffer's content. |
| open [IntStream](https://developer.android.com/reference/kotlin/java/util/stream/IntStream.html#) | [chars](https://developer.android.com/reference/kotlin/java/nio/CharBuffer#chars())`()` <br /> |
| open [Buffer](https://developer.android.com/reference/kotlin/java/nio/Buffer)! | [clear](https://developer.android.com/reference/kotlin/java/nio/CharBuffer#clear())`()` Clears this buffer. |
| abstract [CharBuffer](https://developer.android.com/reference/kotlin/java/nio/CharBuffer#)! | [compact](https://developer.android.com/reference/kotlin/java/nio/CharBuffer#compact())`()` Compacts this buffer*(optional operation)*. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [compareTo](https://developer.android.com/reference/kotlin/java/nio/CharBuffer#compareTo(java.nio.CharBuffer))`(`other:` ` [CharBuffer](https://developer.android.com/reference/kotlin/java/nio/CharBuffer#)!`)` Compares this buffer to another. |
| abstract [CharBuffer](https://developer.android.com/reference/kotlin/java/nio/CharBuffer#)! | [duplicate](https://developer.android.com/reference/kotlin/java/nio/CharBuffer#duplicate())`()` Creates a new char buffer that shares this buffer's content. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/java/nio/CharBuffer#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Tells whether or not this buffer is equal to another object. |
| open [Buffer](https://developer.android.com/reference/kotlin/java/nio/Buffer)! | [flip](https://developer.android.com/reference/kotlin/java/nio/CharBuffer#flip())`()` Flips this buffer. |
| abstract [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | [get](https://developer.android.com/reference/kotlin/java/nio/CharBuffer#get())`()` Relative*get*method. |
| open [CharBuffer](https://developer.android.com/reference/kotlin/java/nio/CharBuffer#)! | [get](https://developer.android.com/reference/kotlin/java/nio/CharBuffer#get(kotlin.CharArray))`(`dst:` ` [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!`)` Relative bulk*get*method. |
| open [CharBuffer](https://developer.android.com/reference/kotlin/java/nio/CharBuffer#)! | [get](https://developer.android.com/reference/kotlin/java/nio/CharBuffer#get(kotlin.CharArray,%20kotlin.Int,%20kotlin.Int))`(`dst:` ` [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!`, `offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `length:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Relative bulk*get*method. |
| abstract [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | [get](https://developer.android.com/reference/kotlin/java/nio/CharBuffer#get(kotlin.Int))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Absolute*get*method. |
| open [CharBuffer](https://developer.android.com/reference/kotlin/java/nio/CharBuffer#)! | [get](https://developer.android.com/reference/kotlin/java/nio/CharBuffer#get(kotlin.Int,%20kotlin.CharArray))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `dst:` ` [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!`)` Absolute bulk*get*method. |
| open [CharBuffer](https://developer.android.com/reference/kotlin/java/nio/CharBuffer#)! | [get](https://developer.android.com/reference/kotlin/java/nio/CharBuffer#get(kotlin.Int,%20kotlin.CharArray,%20kotlin.Int,%20kotlin.Int))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `dst:` ` [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!`, `offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `length:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Absolute bulk*get*method. |
| [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | [get](https://developer.android.com/reference/kotlin/java/nio/CharBuffer#get(kotlin.Int))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasArray](https://developer.android.com/reference/kotlin/java/nio/CharBuffer#hasArray())`()` Tells whether or not this buffer is backed by an accessible char array. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/java/nio/CharBuffer#hashCode())`()` Returns the current hash code of this buffer. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isDirect](https://developer.android.com/reference/kotlin/java/nio/CharBuffer#isDirect())`()` Tells whether or not this char buffer is direct. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEmpty](https://developer.android.com/reference/kotlin/java/nio/CharBuffer#isEmpty())`()` Returns`true`if this character buffer is empty. |
| open [Buffer](https://developer.android.com/reference/kotlin/java/nio/Buffer)! | [limit](https://developer.android.com/reference/kotlin/java/nio/CharBuffer#limit(kotlin.Int))`(`newLimit:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets this buffer's limit. |
| open [Buffer](https://developer.android.com/reference/kotlin/java/nio/Buffer)! | [mark](https://developer.android.com/reference/kotlin/java/nio/CharBuffer#mark())`()` Sets this buffer's mark at its position. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [mismatch](https://developer.android.com/reference/kotlin/java/nio/CharBuffer#mismatch(java.nio.CharBuffer))`(`that:` ` [CharBuffer](https://developer.android.com/reference/kotlin/java/nio/CharBuffer#)!`)` Finds and returns the relative index of the first mismatch between this buffer and a given buffer. |
| abstract [ByteOrder](https://developer.android.com/reference/kotlin/java/nio/ByteOrder)! | [order](https://developer.android.com/reference/kotlin/java/nio/CharBuffer#order())`()` Retrieves this buffer's byte order. |
| open [Buffer](https://developer.android.com/reference/kotlin/java/nio/Buffer)! | [position](https://developer.android.com/reference/kotlin/java/nio/CharBuffer#position(kotlin.Int))`(`newPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets this buffer's position. |
| abstract [CharBuffer](https://developer.android.com/reference/kotlin/java/nio/CharBuffer#)! | [put](https://developer.android.com/reference/kotlin/java/nio/CharBuffer#put(kotlin.Char))`(`c:` ` [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)`)` Relative*put* method*(optional operation)*. |
| [CharBuffer](https://developer.android.com/reference/kotlin/java/nio/CharBuffer#)! | [put](https://developer.android.com/reference/kotlin/java/nio/CharBuffer#put(kotlin.CharArray))`(`src:` ` [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!`)` Relative bulk*put* method*(optional operation)*. |
| open [CharBuffer](https://developer.android.com/reference/kotlin/java/nio/CharBuffer#)! | [put](https://developer.android.com/reference/kotlin/java/nio/CharBuffer#put(kotlin.CharArray,%20kotlin.Int,%20kotlin.Int))`(`src:` ` [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!`, `offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `length:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Relative bulk*put* method*(optional operation)*. |
| abstract [CharBuffer](https://developer.android.com/reference/kotlin/java/nio/CharBuffer#)! | [put](https://developer.android.com/reference/kotlin/java/nio/CharBuffer#put(kotlin.Int,%20kotlin.Char))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `c:` ` [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)`)` Absolute*put* method*(optional operation)*. |
| open [CharBuffer](https://developer.android.com/reference/kotlin/java/nio/CharBuffer#)! | [put](https://developer.android.com/reference/kotlin/java/nio/CharBuffer#put(kotlin.Int,%20kotlin.CharArray))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `src:` ` [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!`)` Absolute bulk*put* method*(optional operation)*. |
| open [CharBuffer](https://developer.android.com/reference/kotlin/java/nio/CharBuffer#)! | [put](https://developer.android.com/reference/kotlin/java/nio/CharBuffer#put(kotlin.Int,%20kotlin.CharArray,%20kotlin.Int,%20kotlin.Int))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `src:` ` [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!`, `offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `length:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Absolute bulk*put* method*(optional operation)*. |
| open [CharBuffer](https://developer.android.com/reference/kotlin/java/nio/CharBuffer#)! | [put](https://developer.android.com/reference/kotlin/java/nio/CharBuffer#put(kotlin.Int,%20java.nio.CharBuffer,%20kotlin.Int,%20kotlin.Int))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `src:` ` [CharBuffer](https://developer.android.com/reference/kotlin/java/nio/CharBuffer#)!`, `offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `length:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Absolute bulk*put* method*(optional operation)*. |
| [CharBuffer](https://developer.android.com/reference/kotlin/java/nio/CharBuffer#)! | [put](https://developer.android.com/reference/kotlin/java/nio/CharBuffer#put(kotlin.String))`(`src:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Relative bulk*put* method*(optional operation)*. |
| open [CharBuffer](https://developer.android.com/reference/kotlin/java/nio/CharBuffer#)! | [put](https://developer.android.com/reference/kotlin/java/nio/CharBuffer#put(kotlin.String,%20kotlin.Int,%20kotlin.Int))`(`src:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `end:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Relative bulk*put* method*(optional operation)*. |
| open [CharBuffer](https://developer.android.com/reference/kotlin/java/nio/CharBuffer#)! | [put](https://developer.android.com/reference/kotlin/java/nio/CharBuffer#put(java.nio.CharBuffer))`(`src:` ` [CharBuffer](https://developer.android.com/reference/kotlin/java/nio/CharBuffer#)!`)` Relative bulk*put* method*(optional operation)*. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [read](https://developer.android.com/reference/kotlin/java/nio/CharBuffer#read(java.nio.CharBuffer))`(`target:` ` [CharBuffer](https://developer.android.com/reference/kotlin/java/nio/CharBuffer#)!`)` Attempts to read characters into the specified character buffer. |
| open [Buffer](https://developer.android.com/reference/kotlin/java/nio/Buffer)! | [reset](https://developer.android.com/reference/kotlin/java/nio/CharBuffer#reset())`()` Resets this buffer's position to the previously-marked position. |
| open [Buffer](https://developer.android.com/reference/kotlin/java/nio/Buffer)! | [rewind](https://developer.android.com/reference/kotlin/java/nio/CharBuffer#rewind())`()` Rewinds this buffer. |
| abstract [CharBuffer](https://developer.android.com/reference/kotlin/java/nio/CharBuffer#)! | [slice](https://developer.android.com/reference/kotlin/java/nio/CharBuffer#slice())`()` Creates a new char buffer whose content is a shared subsequence of this buffer's content. |
| abstract [CharBuffer](https://developer.android.com/reference/kotlin/java/nio/CharBuffer#)! | [slice](https://developer.android.com/reference/kotlin/java/nio/CharBuffer#slice(kotlin.Int,%20kotlin.Int))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `length:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a new char buffer whose content is a shared subsequence of this buffer's content. |
| abstract [CharBuffer](https://developer.android.com/reference/kotlin/java/nio/CharBuffer#) | [subSequence](https://developer.android.com/reference/kotlin/java/nio/CharBuffer#subSequence(kotlin.Int,%20kotlin.Int))`(`startIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `endIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a new character buffer that represents the specified subsequence of this buffer, relative to the current position. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/java/nio/CharBuffer#toString())`()` Returns a string containing the characters in this buffer. |
| openstatic [CharBuffer](https://developer.android.com/reference/kotlin/java/nio/CharBuffer#)! | [wrap](https://developer.android.com/reference/kotlin/java/nio/CharBuffer#wrap(kotlin.CharArray))`(`array:` ` [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!`)` Wraps a char array into a buffer. |
| openstatic [CharBuffer](https://developer.android.com/reference/kotlin/java/nio/CharBuffer#)! | [wrap](https://developer.android.com/reference/kotlin/java/nio/CharBuffer#wrap(kotlin.CharArray,%20kotlin.Int,%20kotlin.Int))`(`array:` ` [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!`, `offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `length:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Wraps a char array into a buffer. |
| openstatic [CharBuffer](https://developer.android.com/reference/kotlin/java/nio/CharBuffer#)! | [wrap](https://developer.android.com/reference/kotlin/java/nio/CharBuffer#wrap(kotlin.CharSequence))`(`csq:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` Wraps a character sequence into a buffer. |
| openstatic [CharBuffer](https://developer.android.com/reference/kotlin/java/nio/CharBuffer#)! | [wrap](https://developer.android.com/reference/kotlin/java/nio/CharBuffer#wrap(kotlin.CharSequence,%20kotlin.Int,%20kotlin.Int))`(`csq:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `end:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Wraps a character sequence into a buffer. |

| Inherited functions ||
|---|---|
| From class [Buffer](https://developer.android.com/reference/kotlin/java/nio/Buffer) |------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [capacity](https://developer.android.com/reference/kotlin/java/nio/Buffer#capacity())`()` <br /> Returns this buffer's capacity. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasRemaining](https://developer.android.com/reference/kotlin/java/nio/Buffer#hasRemaining())`()` <br /> Tells whether there are any elements between the current position and the limit. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isReadOnly](https://developer.android.com/reference/kotlin/java/nio/Buffer#isReadOnly())`()` <br /> Tells whether or not this buffer is read-only. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [limit](https://developer.android.com/reference/kotlin/java/nio/Buffer#limit())`()` <br /> Returns this buffer's limit. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [position](https://developer.android.com/reference/kotlin/java/nio/Buffer#position())`()` <br /> Returns this buffer's position. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [remaining](https://developer.android.com/reference/kotlin/java/nio/Buffer#remaining())`()` <br /> Returns the number of elements between the current position and the limit. <br /> | ||

| Properties ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [length](https://developer.android.com/reference/kotlin/java/nio/CharBuffer#length:kotlin.Int) Returns the length of this character buffer. |

## Public methods

### allocate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun allocate(capacity: Int): CharBuffer!
```

Allocates a new char buffer.

The new buffer's position will be zero, its limit will be its capacity, its mark will be undefined, each of its elements will be initialized to zero, and its byte order will be the [native order](https://developer.android.com/reference/kotlin/java/nio/ByteOrder#nativeOrder())of the underlying hardware. It will have a [backing array](https://developer.android.com/reference/kotlin/java/nio/CharBuffer#array()), and its [array offset](https://developer.android.com/reference/kotlin/java/nio/CharBuffer#arrayOffset())will be zero.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------|
| `capacity` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The new buffer's capacity, in chars |

| Return ||
|------------------------------------------------------------------------------------|---------------------|
| [CharBuffer](https://developer.android.com/reference/kotlin/java/nio/CharBuffer#)! | The new char buffer |

| Exceptions ||
|--------------------------------------|---------------------------------------|
| `java.lang.IllegalArgumentException` | If the`capacity`is a negative integer |

### append

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun append(c: Char): CharBuffer
```

Appends the specified char to this buffer*(optional operation)*.

An invocation of this method of the form`dst.append(c)`behaves in exactly the same way as the invocation 

```kotlin
dst.put(c) 
```

| Parameters ||
|-----|--------------------------------------------------------------------------------------------------------|
| `c` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html):The 16-bit char to append |

| Return ||
|-----------------------------------------------------------------------------------|-------------|
| [CharBuffer](https://developer.android.com/reference/kotlin/java/nio/CharBuffer#) | This buffer |

| Exceptions ||
|------------------------------------|-----------------------------------------------|
| `java.io.IOException` | If an I/O error occurs |
| `java.nio.BufferOverflowException` | If there is insufficient space in this buffer |
| `java.nio.ReadOnlyBufferException` | If this buffer is read-only |

### append

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun append(csq: CharSequence?): CharBuffer
```

Appends the specified character sequence to this buffer*(optional operation)*.

An invocation of this method of the form`dst.append(csq)`behaves in exactly the same way as the invocation 

```kotlin
dst.put(csq.toString()) 
```

Depending on the specification of`toString`for the character sequence`csq`, the entire sequence may not be appended. For instance, invoking the [toString](https://developer.android.com/reference/kotlin/java/nio/CharBuffer#toString())method of a character buffer will return a subsequence whose content depends upon the buffer's position and limit.

| Parameters ||
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `csq` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)?:The character sequence to append. If`csq`is`null`, then the four characters`"null"`are appended to this character buffer. |

| Return ||
|-----------------------------------------------------------------------------------|-------------|
| [CharBuffer](https://developer.android.com/reference/kotlin/java/nio/CharBuffer#) | This buffer |

| Exceptions ||
|------------------------------------|-----------------------------------------------|
| `java.io.IOException` | If an I/O error occurs |
| `java.nio.BufferOverflowException` | If there is insufficient space in this buffer |
| `java.nio.ReadOnlyBufferException` | If this buffer is read-only |

### append

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun append(
    csq: CharSequence?, 
    start: Int, 
    end: Int
): CharBuffer
```

Appends a subsequence of the specified character sequence to this buffer*(optional operation)*.

An invocation of this method of the form`dst.append(csq, start, end)`when`csq`is not`null`, behaves in exactly the same way as the invocation 

```kotlin
dst.put(csq.subSequence(start, end).toString()) 
```

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `csq` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)?:The character sequence from which a subsequence will be appended. If`csq`is`null`, then characters will be appended as if`csq`contained the four characters`"null"`. |
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The index of the first character in the subsequence |
| `end` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The index of the character following the last character in the subsequence |

| Return ||
|-----------------------------------------------------------------------------------|-------------|
| [CharBuffer](https://developer.android.com/reference/kotlin/java/nio/CharBuffer#) | This buffer |

| Exceptions ||
|---------------------------------------|------------------------------------------------------------------------------------------------|
| `java.lang.IndexOutOfBoundsException` | If`start`or`end`are negative,`start`is greater than`end`, or`end`is greater than`csq.length()` |
| `java.io.IOException` | If an I/O error occurs |
| `java.nio.BufferOverflowException` | If there is insufficient space in this buffer |
| `java.nio.ReadOnlyBufferException` | If this buffer is read-only |

### array

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun array(): CharArray!
```

Returns the char array that backs this buffer*(optional operation)*.

Modifications to this buffer's content will cause the returned array's content to be modified, and vice versa.

Invoke the [hasArray](https://developer.android.com/reference/kotlin/java/nio/CharBuffer#hasArray())method before invoking this method in order to ensure that this buffer has an accessible backing array.

| Return ||
|------------------------------------------------------------------------------------------|----------------------------------|
| [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)! | The array that backs this buffer |

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

Invoke the [hasArray](https://developer.android.com/reference/kotlin/java/nio/CharBuffer#hasArray())method before invoking this method in order to ensure that this buffer has an accessible backing array.

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
abstract fun asReadOnlyBuffer(): CharBuffer!
```

Creates a new, read-only char buffer that shares this buffer's content.

The content of the new buffer will be that of this buffer. Changes to this buffer's content will be visible in the new buffer; the new buffer itself, however, will be read-only and will not allow the shared content to be modified. The two buffers' position, limit, and mark values will be independent.

The new buffer's capacity, limit, position, mark values, and byte order will be identical to those of this buffer.

If this buffer is itself read-only then this method behaves in exactly the same way as the [duplicate](https://developer.android.com/reference/kotlin/java/nio/CharBuffer#duplicate())method.

| Return ||
|------------------------------------------------------------------------------------|--------------------------------|
| [CharBuffer](https://developer.android.com/reference/kotlin/java/nio/CharBuffer#)! | The new, read-only char buffer |

### chars

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun chars(): IntStream
```

| Return ||
|----------------------------------------------------------------------------------------------|------------------------------------------------|
| [IntStream](https://developer.android.com/reference/kotlin/java/util/stream/IntStream.html#) | an IntStream of char values from this sequence |

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
| [Buffer](https://developer.android.com/reference/kotlin/java/nio/Buffer)! | This buffer |

### compact

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun compact(): CharBuffer!
```

Compacts this buffer*(optional operation)*.

The chars between the buffer's current position and its limit, if any, are copied to the beginning of the buffer. That is, the char at index*p* =`position()`is copied to index zero, the char at index*p* + 1 is copied to index one, and so forth until the char at index`limit()`- 1 is copied to index*n* =`limit()`-`1`-*p* . The buffer's position is then set to*n+1*and its limit is set to its capacity. The mark, if defined, is discarded.

The buffer's position is set to the number of chars copied, rather than to zero, so that an invocation of this method can be followed immediately by an invocation of another relative*put*method.

| Return ||
|------------------------------------------------------------------------------------|-------------|
| [CharBuffer](https://developer.android.com/reference/kotlin/java/nio/CharBuffer#)! | This buffer |

| Exceptions ||
|------------------------------------|-----------------------------|
| `java.nio.ReadOnlyBufferException` | If this buffer is read-only |

### compareTo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun compareTo(other: CharBuffer!): Int
```

Compares this buffer to another.

Two char buffers are compared by comparing their sequences of remaining elements lexicographically, without regard to the starting position of each sequence within its corresponding buffer. Pairs of`char`elements are compared as if by invoking [Character.compare(char,char)](https://developer.android.com/reference/kotlin/java/lang/Character.html#compare(kotlin.Char,%20kotlin.Char)).

A char buffer is not comparable to any other type of object.

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
abstract fun duplicate(): CharBuffer!
```

Creates a new char buffer that shares this buffer's content.

The content of the new buffer will be that of this buffer. Changes to this buffer's content will be visible in the new buffer, and vice versa; the two buffers' position, limit, and mark values will be independent.

The new buffer's capacity, limit, position, mark values, and byte order will be identical to those of this buffer. The new buffer will be direct if, and only if, this buffer is direct, and it will be read-only if, and only if, this buffer is read-only.

| Return ||
|------------------------------------------------------------------------------------|---------------------|
| [CharBuffer](https://developer.android.com/reference/kotlin/java/nio/CharBuffer#)! | The new char buffer |

### equals

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun equals(other: Any?): Boolean
```

Tells whether or not this buffer is equal to another object.

Two char buffers are equal if, and only if,

1. They have the same element type,
2. They have the same number of remaining elements, and
3. The two sequences of remaining elements, considered independently of their starting positions, are pointwise equal.

A char buffer is not equal to any other type of object.

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

This method is often used in conjunction with the [compact](https://developer.android.com/reference/kotlin/java/nio/ByteBuffer#compact())method when transferring data from one place to another.

| Return ||
|---------------------------------------------------------------------------|-------------|
| [Buffer](https://developer.android.com/reference/kotlin/java/nio/Buffer)! | This buffer |

### get

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun get(): Char
```

Relative*get*method. Reads the char at this buffer's current position, and then increments the position.

| Return ||
|------------------------------------------------------------------------------|-------------------------------------------|
| [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | The char at the buffer's current position |

| Exceptions ||
|-------------------------------------|----------------------------------------------------------------|
| `java.nio.BufferUnderflowException` | If the buffer's current position is not smaller than its limit |

### get

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun get(dst: CharArray!): CharBuffer!
```

Relative bulk*get*method.

This method transfers chars from this buffer into the given destination array. An invocation of this method of the form`src.get(a)`behaves in exactly the same way as the invocation 

```kotlin
src.get(a, 0, a.length) 
```

| Parameters ||
|-------|----------------------------------------------------------------------------------------------------------------|
| `dst` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!:The destination array |

| Return ||
|------------------------------------------------------------------------------------|-------------|
| [CharBuffer](https://developer.android.com/reference/kotlin/java/nio/CharBuffer#)! | This buffer |

| Exceptions ||
|-------------------------------------|---------------------------------------------------------------|
| `java.nio.BufferUnderflowException` | If there are fewer than`length`chars remaining in this buffer |

### get

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun get(
    dst: CharArray!, 
    offset: Int, 
    length: Int
): CharBuffer!
```

Relative bulk*get*method.

This method transfers chars from this buffer into the given destination array. If there are fewer chars remaining in the buffer than are required to satisfy the request, that is, if`length``>``remaining()`, then no chars are transferred and a [BufferUnderflowException](https://developer.android.com/reference/kotlin/java/nio/BufferUnderflowException) is thrown.

Otherwise, this method copies`length`chars from this buffer into the given array, starting at the current position of this buffer and at the given offset in the array. The position of this buffer is then incremented by`length`.

In other words, an invocation of this method of the form`src.get(dst, off, len)`has exactly the same effect as the loop 

```kotlin
<code>for (int i = off; i &lt; off + len; i++)
          dst[i] = src.get();
  </code>
```
except that it first checks that there are sufficient chars in this buffer and it is potentially much more efficient.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dst` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!:The array into which chars are to be written |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The offset within the array of the first char to be written; must be non-negative and no larger than`dst.length` |
| `length` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The maximum number of chars to be written to the given array; must be non-negative and no larger than`dst.length - offset` |

| Return ||
|------------------------------------------------------------------------------------|-------------|
| [CharBuffer](https://developer.android.com/reference/kotlin/java/nio/CharBuffer#)! | This buffer |

| Exceptions ||
|---------------------------------------|----------------------------------------------------------------------|
| `java.nio.BufferUnderflowException` | If there are fewer than`length`chars remaining in this buffer |
| `java.lang.IndexOutOfBoundsException` | If the preconditions on the`offset`and`length`parameters do not hold |

### get

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun get(index: Int): Char
```

Absolute*get*method. Reads the char at the given index.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The index from which the char will be read |

| Return ||
|------------------------------------------------------------------------------|-----------------------------|
| [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | The char at the given index |

| Exceptions ||
|---------------------------------------|-------------------------------------------------------------|
| `java.lang.IndexOutOfBoundsException` | If`index`is negative or not smaller than the buffer's limit |

### get

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun get(
    index: Int, 
    dst: CharArray!
): CharBuffer!
```

Absolute bulk*get*method.

This method transfers chars from this buffer into the given destination array. The position of this buffer is unchanged. An invocation of this method of the form`src.get(index, dst)`behaves in exactly the same way as the invocation: 

```kotlin
src.get(index, dst, 0, dst.length) 
```

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The index in this buffer from which the first char will be read; must be non-negative and less than`limit()` |
| `dst` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!:The destination array |

| Return ||
|------------------------------------------------------------------------------------|-------------|
| [CharBuffer](https://developer.android.com/reference/kotlin/java/nio/CharBuffer#)! | This buffer |

| Exceptions ||
|---------------------------------------|-----------------------------------------------------------------------------------|
| `java.lang.IndexOutOfBoundsException` | If`index`is negative, not smaller than`limit()`, or`limit() - index < dst.length` |

### get

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun get(
    index: Int, 
    dst: CharArray!, 
    offset: Int, 
    length: Int
): CharBuffer!
```

Absolute bulk*get*method.

This method transfers`length`chars from this buffer into the given array, starting at the given index in this buffer and at the given offset in the array. The position of this buffer is unchanged.

An invocation of this method of the form`src.get(index, dst, offset, length)`has exactly the same effect as the following loop except that it first checks the consistency of the supplied parameters and it is potentially much more efficient: 

```kotlin
<code>for (int i = offset, j = index; i &lt; offset + length; i++, j++)
          dst[i] = src.get(j);
  </code>
```

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The index in this buffer from which the first char will be read; must be non-negative and less than`limit()` |
| `dst` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!:The destination array |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The offset within the array of the first char to be written; must be non-negative and less than`dst.length` |
| `length` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The number of chars to be written to the given array; must be non-negative and no larger than the smaller of`limit() - index`and`dst.length - offset` |

| Return ||
|------------------------------------------------------------------------------------|-------------|
| [CharBuffer](https://developer.android.com/reference/kotlin/java/nio/CharBuffer#)! | This buffer |

| Exceptions ||
|---------------------------------------|--------------------------------------------------------------------------------|
| `java.lang.IndexOutOfBoundsException` | If the preconditions on the`index`,`offset`, and`length`parameters do not hold |

### get

```
fun get(index: Int): Char
```  

### hasArray

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hasArray(): Boolean
```

Tells whether or not this buffer is backed by an accessible char array.

If this method returns`true`then the [array](https://developer.android.com/reference/kotlin/java/nio/CharBuffer#array())and [arrayOffset](https://developer.android.com/reference/kotlin/java/nio/CharBuffer#arrayOffset())methods may safely be invoked.

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if, and only if, this buffer is backed by an array and is not read-only |

### hashCode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hashCode(): Int
```

Returns the current hash code of this buffer.

The hash code of a char buffer depends only upon its remaining elements; that is, upon the elements from`position()`up to, and including, the element at`limit()`-`1`.

Because buffer hash codes are content-dependent, it is inadvisable to use buffers as keys in hash maps or similar data structures unless it is known that their contents will not change.

| Return ||
|----------------------------------------------------------------------------|--------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The current hash code of this buffer |

### isDirect

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isDirect(): Boolean
```

Tells whether or not this char buffer is direct.

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if, and only if, this buffer is direct |

### isEmpty

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isEmpty(): Boolean
```

Returns`true`if this character buffer is empty.

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if there are`0`remaining characters, otherwise`false` |

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
| [Buffer](https://developer.android.com/reference/kotlin/java/nio/Buffer)! | This buffer |

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
| [Buffer](https://developer.android.com/reference/kotlin/java/nio/Buffer)! | This buffer |

### mismatch

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun mismatch(that: CharBuffer!): Int
```

Finds and returns the relative index of the first mismatch between this buffer and a given buffer. The index is relative to the [position](https://developer.android.com/reference/kotlin/java/nio/Buffer#position())of each buffer and will be in the range of 0 (inclusive) up to the smaller of the [remaining](https://developer.android.com/reference/kotlin/java/nio/Buffer#remaining())elements in each buffer (exclusive).

If the two buffers share a common prefix then the returned index is the length of the common prefix and it follows that there is a mismatch between the two buffers at that index within the respective buffers. If one buffer is a proper prefix of the other then the returned index is the smaller of the remaining elements in each buffer, and it follows that the index is only valid for the buffer with the larger number of remaining elements. Otherwise, there is no mismatch.

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| `that` | [CharBuffer](https://developer.android.com/reference/kotlin/java/nio/CharBuffer#)!:The byte buffer to be tested for a mismatch with this buffer |

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The relative index of the first mismatch between this and the given buffer, otherwise -1 if no mismatch. |

### order

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun order(): ByteOrder!
```

Retrieves this buffer's byte order.

The byte order of a char buffer created by allocation or by wrapping an existing`char`array is the [native order](https://developer.android.com/reference/kotlin/java/nio/ByteOrder#nativeOrder())of the underlying hardware. The byte order of a char buffer created as a [view](https://developer.android.com/reference/kotlin/java/nio/ByteBuffer#views) of a byte buffer is that of the byte buffer at the moment that the view is created.

| Return ||
|---------------------------------------------------------------------------------|--------------------------|
| [ByteOrder](https://developer.android.com/reference/kotlin/java/nio/ByteOrder)! | This buffer's byte order |

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
| [Buffer](https://developer.android.com/reference/kotlin/java/nio/Buffer)! | This buffer |

| Exceptions ||
|--------------------------------------|-------------------------------------------------|
| `java.lang.IllegalArgumentException` | If the preconditions on`newPosition`do not hold |

### put

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun put(c: Char): CharBuffer!
```

Relative*put* method*(optional operation)*.

Writes the given char into this buffer at the current position, and then increments the position.

| Parameters ||
|-----|-----------------------------------------------------------------------------------------------------|
| `c` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html):The char to be written |

| Return ||
|------------------------------------------------------------------------------------|-------------|
| [CharBuffer](https://developer.android.com/reference/kotlin/java/nio/CharBuffer#)! | This buffer |

| Exceptions ||
|------------------------------------|-----------------------------------------------------------------|
| `java.nio.BufferOverflowException` | If this buffer's current position is not smaller than its limit |
| `java.nio.ReadOnlyBufferException` | If this buffer is read-only |

### put

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun put(src: CharArray!): CharBuffer!
```

Relative bulk*put* method*(optional operation)*.

This method transfers the entire content of the given source char array into this buffer. An invocation of this method of the form`dst.put(a)`behaves in exactly the same way as the invocation 

```kotlin
dst.put(a, 0, a.length) 
```

| Parameters ||
|-------|-----------------------------------------------------------------------------------------------------------|
| `src` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!:The source array |

| Return ||
|------------------------------------------------------------------------------------|-------------|
| [CharBuffer](https://developer.android.com/reference/kotlin/java/nio/CharBuffer#)! | This buffer |

| Exceptions ||
|------------------------------------|-----------------------------------------------|
| `java.nio.BufferOverflowException` | If there is insufficient space in this buffer |
| `java.nio.ReadOnlyBufferException` | If this buffer is read-only |

### put

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun put(
    src: CharArray!, 
    offset: Int, 
    length: Int
): CharBuffer!
```

Relative bulk*put* method*(optional operation)*.

This method transfers chars into this buffer from the given source array. If there are more chars to be copied from the array than remain in this buffer, that is, if`length``>``remaining()`, then no chars are transferred and a [BufferOverflowException](https://developer.android.com/reference/kotlin/java/nio/BufferOverflowException) is thrown.

Otherwise, this method copies`length`chars from the given array into this buffer, starting at the given offset in the array and at the current position of this buffer. The position of this buffer is then incremented by`length`.

In other words, an invocation of this method of the form`dst.put(src, off, len)`has exactly the same effect as the loop 

```kotlin
<code>for (int i = off; i &lt; off + len; i++)
          dst.put(src[i]);
  </code>
```
except that it first checks that there is sufficient space in this buffer and it is potentially much more efficient.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `src` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!:The array from which chars are to be read |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The offset within the array of the first char to be read; must be non-negative and no larger than`src.length` |
| `length` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The number of chars to be read from the given array; must be non-negative and no larger than`src.length - offset` |

| Return ||
|------------------------------------------------------------------------------------|-------------|
| [CharBuffer](https://developer.android.com/reference/kotlin/java/nio/CharBuffer#)! | This buffer |

| Exceptions ||
|---------------------------------------|----------------------------------------------------------------------|
| `java.nio.BufferOverflowException` | If there is insufficient space in this buffer |
| `java.lang.IndexOutOfBoundsException` | If the preconditions on the`offset`and`length`parameters do not hold |
| `java.nio.ReadOnlyBufferException` | If this buffer is read-only |

### put

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun put(
    index: Int, 
    c: Char
): CharBuffer!
```

Absolute*put* method*(optional operation)*.

Writes the given char into this buffer at the given index.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The index at which the char will be written |
| `c` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html):The char value to be written |

| Return ||
|------------------------------------------------------------------------------------|-------------|
| [CharBuffer](https://developer.android.com/reference/kotlin/java/nio/CharBuffer#)! | This buffer |

| Exceptions ||
|---------------------------------------|-------------------------------------------------------------|
| `java.lang.IndexOutOfBoundsException` | If`index`is negative or not smaller than the buffer's limit |
| `java.nio.ReadOnlyBufferException` | If this buffer is read-only |

### put

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun put(
    index: Int, 
    src: CharArray!
): CharBuffer!
```

Absolute bulk*put* method*(optional operation)*.

This method copies chars into this buffer from the given source array. The position of this buffer is unchanged. An invocation of this method of the form`dst.put(index, src)`behaves in exactly the same way as the invocation: 

```kotlin
dst.put(index, src, 0, src.length); 
```

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The index in this buffer at which the first char will be written; must be non-negative and less than`limit()` |
| `src` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!:The array from which chars are to be read |

| Return ||
|------------------------------------------------------------------------------------|-------------|
| [CharBuffer](https://developer.android.com/reference/kotlin/java/nio/CharBuffer#)! | This buffer |

| Exceptions ||
|---------------------------------------|-----------------------------------------------------------------------------------|
| `java.lang.IndexOutOfBoundsException` | If`index`is negative, not smaller than`limit()`, or`limit() - index < src.length` |
| `java.nio.ReadOnlyBufferException` | If this buffer is read-only |

### put

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun put(
    index: Int, 
    src: CharArray!, 
    offset: Int, 
    length: Int
): CharBuffer!
```

Absolute bulk*put* method*(optional operation)*.

This method transfers`length`chars from the given array, starting at the given offset in the array and at the given index in this buffer. The position of this buffer is unchanged.

An invocation of this method of the form`dst.put(index, src, offset, length)`has exactly the same effect as the following loop except that it first checks the consistency of the supplied parameters and it is potentially much more efficient: 

```kotlin
<code>for (int i = offset, j = index; i &lt; offset + length; i++, j++)
          dst.put(j, src[i]);
  </code>
```

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The index in this buffer at which the first char will be written; must be non-negative and less than`limit()` |
| `src` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!:The array from which chars are to be read |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The offset within the array of the first char to be read; must be non-negative and less than`src.length` |
| `length` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The number of chars to be read from the given array; must be non-negative and no larger than the smaller of`limit() - index`and`src.length - offset` |

| Return ||
|------------------------------------------------------------------------------------|-------------|
| [CharBuffer](https://developer.android.com/reference/kotlin/java/nio/CharBuffer#)! | This buffer |

| Exceptions ||
|---------------------------------------|--------------------------------------------------------------------------------|
| `java.lang.IndexOutOfBoundsException` | If the preconditions on the`index`,`offset`, and`length`parameters do not hold |
| `java.nio.ReadOnlyBufferException` | If this buffer is read-only |

### put

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun put(
    index: Int, 
    src: CharBuffer!, 
    offset: Int, 
    length: Int
): CharBuffer!
```

Absolute bulk*put* method*(optional operation)*.

This method transfers`length`chars into this buffer from the given source buffer, starting at the given`offset`in the source buffer and the given`index`in this buffer. The positions of both buffers are unchanged.

In other words, an invocation of this method of the form`dst.put(index, src, offset, length)`has exactly the same effect as the loop 

```kotlin
<code>for (int i = offset, j = index; i &lt; offset + length; i++, j++)
      dst.put(j, src.get(i));
  </code>
```
except that it first checks the consistency of the supplied parameters and it is potentially much more efficient. If this buffer and the source buffer share the same backing array or memory, then the result will be as if the source elements were first copied to an intermediate location before being written into this buffer.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The index in this buffer at which the first char will be written; must be non-negative and less than`limit()` |
| `src` | [CharBuffer](https://developer.android.com/reference/kotlin/java/nio/CharBuffer#)!:The buffer from which chars are to be read |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The index within the source buffer of the first char to be read; must be non-negative and less than`src.limit()` |
| `length` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The number of chars to be read from the given buffer; must be non-negative and no larger than the smaller of`limit() - index`and`src.limit() - offset` |

| Return ||
|------------------------------------------------------------------------------------|-------------|
| [CharBuffer](https://developer.android.com/reference/kotlin/java/nio/CharBuffer#)! | This buffer |

| Exceptions ||
|---------------------------------------|--------------------------------------------------------------------------------|
| `java.lang.IndexOutOfBoundsException` | If the preconditions on the`index`,`offset`, and`length`parameters do not hold |
| `java.nio.ReadOnlyBufferException` | If this buffer is read-only |

### put

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun put(src: String!): CharBuffer!
```

Relative bulk*put* method*(optional operation)*.

This method transfers the entire content of the given source string into this buffer. An invocation of this method of the form`dst.put(s)`behaves in exactly the same way as the invocation 

```kotlin
dst.put(s, 0, s.length()) 
```

| Parameters ||
|-------|-----------------------------------------------------------------------------------------------------|
| `src` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The source string |

| Return ||
|------------------------------------------------------------------------------------|-------------|
| [CharBuffer](https://developer.android.com/reference/kotlin/java/nio/CharBuffer#)! | This buffer |

| Exceptions ||
|------------------------------------|-----------------------------------------------|
| `java.nio.BufferOverflowException` | If there is insufficient space in this buffer |
| `java.nio.ReadOnlyBufferException` | If this buffer is read-only |

### put

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun put(
    src: String!, 
    start: Int, 
    end: Int
): CharBuffer!
```

Relative bulk*put* method*(optional operation)*.

This method transfers chars from the given string into this buffer. If there are more chars to be copied from the string than remain in this buffer, that is, if`end - start``>``remaining()`, then no chars are transferred and a [BufferOverflowException](https://developer.android.com/reference/kotlin/java/nio/BufferOverflowException) is thrown.

Otherwise, this method copies*n* =`end`-`start`chars from the given string into this buffer, starting at the given`start`index and at the current position of this buffer. The position of this buffer is then incremented by*n*.

In other words, an invocation of this method of the form`dst.put(src, start, end)`has exactly the same effect as the loop 

```kotlin
<code>for (int i = start; i &lt; end; i++)
          dst.put(src.charAt(i));
  </code>
```
except that it first checks that there is sufficient space in this buffer and it is potentially much more efficient.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `src` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The string from which chars are to be read |
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The offset within the string of the first char to be read; must be non-negative and no larger than`string.length()` |
| `end` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The offset within the string of the last char to be read, plus one; must be non-negative and no larger than`string.length()` |

| Return ||
|------------------------------------------------------------------------------------|-------------|
| [CharBuffer](https://developer.android.com/reference/kotlin/java/nio/CharBuffer#)! | This buffer |

| Exceptions ||
|---------------------------------------|------------------------------------------------------------------|
| `java.nio.BufferOverflowException` | If there is insufficient space in this buffer |
| `java.lang.IndexOutOfBoundsException` | If the preconditions on the`start`and`end`parameters do not hold |
| `java.nio.ReadOnlyBufferException` | If this buffer is read-only |

### put

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun put(src: CharBuffer!): CharBuffer!
```

Relative bulk*put* method*(optional operation)*.

This method transfers the chars remaining in the given source buffer into this buffer. If there are more chars remaining in the source buffer than in this buffer, that is, if`src.remaining()``>``remaining()`, then no chars are transferred and a [BufferOverflowException](https://developer.android.com/reference/kotlin/java/nio/BufferOverflowException) is thrown.

Otherwise, this method copies*n* =`src.remaining()`chars from the given buffer into this buffer, starting at each buffer's current position. The positions of both buffers are then incremented by*n*.

In other words, an invocation of this method of the form`dst.put(src)`has exactly the same effect as the loop 

```kotlin
while (src.hasRemaining())
          dst.put(src.get()); 
```
except that it first checks that there is sufficient space in this buffer and it is potentially much more efficient. If this buffer and the source buffer share the same backing array or memory, then the result will be as if the source elements were first copied to an intermediate location before being written into this buffer.

| Parameters ||
|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `src` | [CharBuffer](https://developer.android.com/reference/kotlin/java/nio/CharBuffer#)!:The source buffer from which chars are to be read; must not be this buffer |

| Return ||
|------------------------------------------------------------------------------------|-------------|
| [CharBuffer](https://developer.android.com/reference/kotlin/java/nio/CharBuffer#)! | This buffer |

| Exceptions ||
|--------------------------------------|--------------------------------------------------------------------------------------------|
| `java.nio.BufferOverflowException` | If there is insufficient space in this buffer for the remaining chars in the source buffer |
| `java.lang.IllegalArgumentException` | If the source buffer is this buffer |
| `java.nio.ReadOnlyBufferException` | If this buffer is read-only |

### read

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun read(target: CharBuffer!): Int
```

Attempts to read characters into the specified character buffer. The buffer is used as a repository of characters as-is: the only changes made are the results of a put operation. No flipping or rewinding of the buffer is performed.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------|
| `cb` | the buffer to read characters into |
| `target` | [CharBuffer](https://developer.android.com/reference/kotlin/java/nio/CharBuffer#)!:the buffer to read characters into |

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The number of characters added to the buffer, or -1 if this source of characters is at its end |

| Exceptions ||
|------------------------------------|---------------------------------|
| `java.io.IOException` | if an I/O error occurs |
| `java.lang.NullPointerException` | if target is null |
| `java.nio.ReadOnlyBufferException` | if target is a read only buffer |

### reset

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun reset(): Buffer!
```

Resets this buffer's position to the previously-marked position.

Invoking this method neither changes nor discards the mark's value.

| Return ||
|---------------------------------------------------------------------------|-------------|
| [Buffer](https://developer.android.com/reference/kotlin/java/nio/Buffer)! | This buffer |

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
| [Buffer](https://developer.android.com/reference/kotlin/java/nio/Buffer)! | This buffer |

### slice

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun slice(): CharBuffer!
```

Creates a new char buffer whose content is a shared subsequence of this buffer's content.

The content of the new buffer will start at this buffer's current position. Changes to this buffer's content will be visible in the new buffer, and vice versa; the two buffers' position, limit, and mark values will be independent.

The new buffer's position will be zero, its capacity and its limit will be the number of chars remaining in this buffer, its mark will be undefined, and its byte order will be identical to that of this buffer. The new buffer will be direct if, and only if, this buffer is direct, and it will be read-only if, and only if, this buffer is read-only.

| Return ||
|------------------------------------------------------------------------------------|---------------------|
| [CharBuffer](https://developer.android.com/reference/kotlin/java/nio/CharBuffer#)! | The new char buffer |

### slice

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun slice(
    index: Int, 
    length: Int
): CharBuffer!
```

Creates a new char buffer whose content is a shared subsequence of this buffer's content.

The content of the new buffer will start at position`index`in this buffer, and will contain`length`elements. Changes to this buffer's content will be visible in the new buffer, and vice versa; the two buffers' position, limit, and mark values will be independent.

The new buffer's position will be zero, its capacity and its limit will be`length`, its mark will be undefined, and its byte order will be identical to that of this buffer. The new buffer will be direct if, and only if, this buffer is direct, and it will be read-only if, and only if, this buffer is read-only.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The position in this buffer at which the content of the new buffer will start; must be non-negative and no larger than [limit()](https://developer.android.com/reference/kotlin/java/nio/Buffer#limit()) |
| `length` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The number of elements the new buffer will contain; must be non-negative and no larger than`limit() - index` |

| Return ||
|------------------------------------------------------------------------------------|----------------|
| [CharBuffer](https://developer.android.com/reference/kotlin/java/nio/CharBuffer#)! | The new buffer |

| Exceptions ||
|---------------------------------------|-------------------------------------------------------------------------------------------------|
| `java.lang.IndexOutOfBoundsException` | If`index`is negative or greater than`limit()`,`length`is negative, or`length > limit() - index` |

### subSequence

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun subSequence(
    startIndex: Int, 
    endIndex: Int
): CharBuffer
```

Creates a new character buffer that represents the specified subsequence of this buffer, relative to the current position.

The new buffer will share this buffer's content; that is, if the content of this buffer is mutable then modifications to one buffer will cause the other to be modified. The new buffer's capacity will be that of this buffer, its position will be`position()`+`start`, its limit will be`position()`+`end`, and its byte order will be identical to that of this buffer. The new buffer will be direct if, and only if, this buffer is direct, and it will be read-only if, and only if, this buffer is read-only.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `start` | The index, relative to the current position, of the first character in the subsequence; must be non-negative and no larger than`remaining()` |
| `end` | The index, relative to the current position, of the character following the last character in the subsequence; must be no smaller than`start`and no larger than`remaining()` |

| Return ||
|-----------------------------------------------------------------------------------|--------------------------|
| [CharBuffer](https://developer.android.com/reference/kotlin/java/nio/CharBuffer#) | The new character buffer |

| Exceptions ||
|---------------------------------------|---------------------------------------------------|
| `java.lang.IndexOutOfBoundsException` | If the preconditions on`start`and`end`do not hold |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

Returns a string containing the characters in this buffer.

The first character of the resulting string will be the character at this buffer's position, while the last character will be the character at index`limit()`- 1. Invoking this method does not change the buffer's position.

| Return ||
|----------------------------------------------------------------------------------|----------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | The specified string |

### wrap

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun wrap(array: CharArray!): CharBuffer!
```

Wraps a char array into a buffer.

The new buffer will be backed by the given char array; that is, modifications to the buffer will cause the array to be modified and vice versa. The new buffer's capacity and limit will be`array.length`, its position will be zero, its mark will be undefined, and its byte order will be the [native order](https://developer.android.com/reference/kotlin/java/nio/ByteOrder#nativeOrder())of the underlying hardware. Its [backing array](https://developer.android.com/reference/kotlin/java/nio/CharBuffer#array())will be the given array, and its [array offset](https://developer.android.com/reference/kotlin/java/nio/CharBuffer#arrayOffset())will be zero.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------------|
| `array` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!:The array that will back this buffer |

| Return ||
|------------------------------------------------------------------------------------|---------------------|
| [CharBuffer](https://developer.android.com/reference/kotlin/java/nio/CharBuffer#)! | The new char buffer |

### wrap

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun wrap(
    array: CharArray!, 
    offset: Int, 
    length: Int
): CharBuffer!
```

Wraps a char array into a buffer.

The new buffer will be backed by the given char array; that is, modifications to the buffer will cause the array to be modified and vice versa. The new buffer's capacity will be`array.length`, its position will be`offset`, its limit will be`offset + length`, its mark will be undefined, and its byte order will be the [native order](https://developer.android.com/reference/kotlin/java/nio/ByteOrder#nativeOrder())of the underlying hardware. Its [backing array](https://developer.android.com/reference/kotlin/java/nio/CharBuffer#array())will be the given array, and its [array offset](https://developer.android.com/reference/kotlin/java/nio/CharBuffer#arrayOffset())will be zero.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `array` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!:The array that will back the new buffer |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The offset of the subarray to be used; must be non-negative and no larger than`array.length`. The new buffer's position will be set to this value. |
| `length` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The length of the subarray to be used; must be non-negative and no larger than`array.length - offset`. The new buffer's limit will be set to`offset + length`. |

| Return ||
|------------------------------------------------------------------------------------|---------------------|
| [CharBuffer](https://developer.android.com/reference/kotlin/java/nio/CharBuffer#)! | The new char buffer |

| Exceptions ||
|---------------------------------------|----------------------------------------------------------------------|
| `java.lang.IndexOutOfBoundsException` | If the preconditions on the`offset`and`length`parameters do not hold |

### wrap

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun wrap(csq: CharSequence!): CharBuffer!
```

Wraps a character sequence into a buffer.

The content of the new, read-only buffer will be the content of the given character sequence. The new buffer's capacity and limit will be`csq.length()`, its position will be zero, and its mark will be undefined.

| Parameters ||
|-------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `csq` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:The character sequence from which the new character buffer is to be created |

| Return ||
|------------------------------------------------------------------------------------|--------------------------|
| [CharBuffer](https://developer.android.com/reference/kotlin/java/nio/CharBuffer#)! | The new character buffer |

### wrap

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun wrap(
    csq: CharSequence!, 
    start: Int, 
    end: Int
): CharBuffer!
```

Wraps a character sequence into a buffer.

The content of the new, read-only buffer will be the content of the given character sequence. The buffer's capacity will be`csq.length()`, its position will be`start`, its limit will be`end`, and its mark will be undefined.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `csq` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:The character sequence from which the new character buffer is to be created |
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The index of the first character to be used; must be non-negative and no larger than`csq.length()`. The new buffer's position will be set to this value. |
| `end` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The index of the character following the last character to be used; must be no smaller than`start`and no larger than`csq.length()`. The new buffer's limit will be set to this value. |

| Return ||
|------------------------------------------------------------------------------------|--------------------------|
| [CharBuffer](https://developer.android.com/reference/kotlin/java/nio/CharBuffer#)! | The new character buffer |

| Exceptions ||
|---------------------------------------|------------------------------------------------------------------|
| `java.lang.IndexOutOfBoundsException` | If the preconditions on the`start`and`end`parameters do not hold |

## Properties

### length

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
val length: Int
```

Returns the length of this character buffer.

When viewed as a character sequence, the length of a character buffer is simply the number of characters between the position (inclusive) and the limit (exclusive); that is, it is equivalent to`remaining()`.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The length of this character buffer |
