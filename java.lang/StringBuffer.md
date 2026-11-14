Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# StringBuffer

```
class StringBuffer : Appendable, CharSequence, Comparable<StringBuffer!>, Serializable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [java.lang.StringBuffer](https://developer.android.com/reference/kotlin/java/lang/StringBuffer#) |

A thread-safe, mutable sequence of characters. A string buffer is like a `https://developer.android.com/reference/kotlin/java/lang/String`, but can be modified. At any point in time it contains some particular sequence of characters, but the length and content of the sequence can be changed through certain method calls.

String buffers are safe for use by multiple threads. The methods are synchronized where necessary so that all the operations on any particular instance behave as if they occur in some serial order that is consistent with the order of the method calls made by each of the individual threads involved.

The principal operations on a `StringBuffer` are the `append` and `insert` methods, which are overloaded so as to accept data of any type. Each effectively converts a given datum to a string and then appends or inserts the characters of that string to the string buffer. The `append` method always adds these characters at the end of the buffer; the `insert` method adds the characters at a specified point.

For example, if `z` refers to a string buffer object whose current contents are `"start"`, then the method call `z.append("le")` would cause the string buffer to contain `"startle"`, whereas `z.insert(4, "le")` would alter the string buffer to contain `"starlet"`.

In general, if sb refers to an instance of a `StringBuffer`, then `sb.append(x)` has the same effect as `sb.insert(sb.length(), x)`.

Whenever an operation occurs involving a source sequence (such as appending or inserting from a source sequence), this class synchronizes only on the string buffer performing the operation, not on the source. Note that while `StringBuffer` is designed to be safe to use concurrently from multiple threads, if the constructor or the `append` or `insert` operation is passed a source sequence that is shared across threads, the calling code must ensure that the operation has a consistent and unchanging view of the source sequence for the duration of the operation. This could be satisfied by the caller holding a lock during the operation's call, by using an immutable source sequence, or by not sharing the source sequence across threads.

Every string buffer has a capacity. As long as the length of the character sequence contained in the string buffer does not exceed the capacity, it is not necessary to allocate a new internal buffer array. If the internal buffer overflows, it is automatically made larger.

Unless otherwise noted, passing a `null` argument to a constructor or method in this class will cause a `https://developer.android.com/reference/kotlin/java/lang/NullPointerException` to be thrown.

As of release JDK 5, this class has been supplemented with an equivalent class designed for use by a single thread, `https://developer.android.com/reference/kotlin/java/lang/StringBuilder`. The `StringBuilder` class should generally be used in preference to this one, as it supports all of the same operations but it is faster, as it performs no synchronization.

## Summary

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/lang/StringBuffer#StringBuffer()()` Constructs a string buffer with no characters in it and an initial capacity of 16 characters. |
| `https://developer.android.com/reference/kotlin/java/lang/StringBuffer#StringBuffer(kotlin.Int)(capacity: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Constructs a string buffer with no characters in it and the specified initial capacity. |
| `https://developer.android.com/reference/kotlin/java/lang/StringBuffer#StringBuffer(kotlin.CharSequence)(seq: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)` Constructs a string buffer that contains the same characters as the specified `CharSequence`. |
| `https://developer.android.com/reference/kotlin/java/lang/StringBuffer#StringBuffer(kotlin.String)(str: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Constructs a string buffer initialized to the contents of the specified string. |

| Public methods ||
|---|---|
| [StringBuffer](https://developer.android.com/reference/kotlin/java/lang/StringBuffer#) | `https://developer.android.com/reference/kotlin/java/lang/StringBuffer#append(kotlin.Boolean)(b: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` <br /> |
| [StringBuffer](https://developer.android.com/reference/kotlin/java/lang/StringBuffer#) | `https://developer.android.com/reference/kotlin/java/lang/StringBuffer#append(kotlin.Char)(c: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)` Appends the specified character to this `Appendable`. |
| [StringBuffer](https://developer.android.com/reference/kotlin/java/lang/StringBuffer#) | `https://developer.android.com/reference/kotlin/java/lang/StringBuffer#append(kotlin.CharArray)(str: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html!)` <br /> |
| [StringBuffer](https://developer.android.com/reference/kotlin/java/lang/StringBuffer#) | `https://developer.android.com/reference/kotlin/java/lang/StringBuffer#append(kotlin.CharArray,%20kotlin.Int,%20kotlin.Int)(str: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html!, offset: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, len: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` <br /> |
| [StringBuffer](https://developer.android.com/reference/kotlin/java/lang/StringBuffer#) | `https://developer.android.com/reference/kotlin/java/lang/StringBuffer#append(kotlin.Double)(d: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)` <br /> |
| [StringBuffer](https://developer.android.com/reference/kotlin/java/lang/StringBuffer#) | `https://developer.android.com/reference/kotlin/java/lang/StringBuffer#append(kotlin.Float)(f: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` <br /> |
| [StringBuffer](https://developer.android.com/reference/kotlin/java/lang/StringBuffer#) | `https://developer.android.com/reference/kotlin/java/lang/StringBuffer#append(kotlin.Int)(i: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` <br /> |
| [StringBuffer](https://developer.android.com/reference/kotlin/java/lang/StringBuffer#) | `https://developer.android.com/reference/kotlin/java/lang/StringBuffer#append(kotlin.CharSequence)(s: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html?)` Appends the specified `CharSequence` to this sequence. |
| [StringBuffer](https://developer.android.com/reference/kotlin/java/lang/StringBuffer#) | `https://developer.android.com/reference/kotlin/java/lang/StringBuffer#append(kotlin.CharSequence,%20kotlin.Int,%20kotlin.Int)(s: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html?, start: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, end: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` <br /> |
| [StringBuffer](https://developer.android.com/reference/kotlin/java/lang/StringBuffer#) | `https://developer.android.com/reference/kotlin/java/lang/StringBuffer#append(kotlin.Any)(obj: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` <br /> |
| [StringBuffer](https://developer.android.com/reference/kotlin/java/lang/StringBuffer#) | `https://developer.android.com/reference/kotlin/java/lang/StringBuffer#append(kotlin.String)(str: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?)` <br /> |
| [StringBuffer](https://developer.android.com/reference/kotlin/java/lang/StringBuffer#) | `https://developer.android.com/reference/kotlin/java/lang/StringBuffer#append(java.lang.StringBuffer)(sb: https://developer.android.com/reference/kotlin/java/lang/StringBuffer#?)` Appends the specified `StringBuffer` to this sequence. |
| [StringBuffer](https://developer.android.com/reference/kotlin/java/lang/StringBuffer#) | `https://developer.android.com/reference/kotlin/java/lang/StringBuffer#append(kotlin.Long)(lng: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` <br /> |
| [StringBuffer](https://developer.android.com/reference/kotlin/java/lang/StringBuffer#) | `https://developer.android.com/reference/kotlin/java/lang/StringBuffer#appendCodePoint(kotlin.Int)(codePoint: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/lang/StringBuffer#capacity()()` <br /> |
| [IntStream](https://developer.android.com/reference/kotlin/java/util/stream/IntStream.html#) | `https://developer.android.com/reference/kotlin/java/lang/StringBuffer#chars()()` Returns a stream of `int` zero-extending the `char` values from this sequence. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/lang/StringBuffer#codePointAt(kotlin.Int)(index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/lang/StringBuffer#codePointBefore(kotlin.Int)(index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/lang/StringBuffer#codePointCount(kotlin.Int,%20kotlin.Int)(beginIndex: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, endIndex: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` <br /> |
| [IntStream](https://developer.android.com/reference/kotlin/java/util/stream/IntStream.html#) | `https://developer.android.com/reference/kotlin/java/lang/StringBuffer#codePoints()()` Returns a stream of code point values from this sequence. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/lang/StringBuffer#compareTo(java.lang.StringBuffer)(other: https://developer.android.com/reference/kotlin/java/lang/StringBuffer#)` Compares two `StringBuffer` instances lexicographically. |
| [StringBuffer](https://developer.android.com/reference/kotlin/java/lang/StringBuffer#) | `https://developer.android.com/reference/kotlin/java/lang/StringBuffer#delete(kotlin.Int,%20kotlin.Int)(start: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, end: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` <br /> |
| [StringBuffer](https://developer.android.com/reference/kotlin/java/lang/StringBuffer#) | `https://developer.android.com/reference/kotlin/java/lang/StringBuffer#deleteCharAt(kotlin.Int)(index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/lang/StringBuffer#ensureCapacity(kotlin.Int)(minimumCapacity: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` <br /> |
| [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | `https://developer.android.com/reference/kotlin/java/lang/StringBuffer#get(kotlin.Int)(index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/lang/StringBuffer#getChars(kotlin.Int,%20kotlin.Int,%20kotlin.CharArray,%20kotlin.Int)(srcBegin: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, srcEnd: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, dst: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html, dstBegin: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/lang/StringBuffer#indexOf(kotlin.String)(str: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/lang/StringBuffer#indexOf(kotlin.String,%20kotlin.Int)(str: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, fromIndex: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` <br /> |
| [StringBuffer](https://developer.android.com/reference/kotlin/java/lang/StringBuffer#) | `https://developer.android.com/reference/kotlin/java/lang/StringBuffer#insert(kotlin.Int,%20kotlin.Boolean)(offset: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, b: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` <br /> |
| [StringBuffer](https://developer.android.com/reference/kotlin/java/lang/StringBuffer#) | `https://developer.android.com/reference/kotlin/java/lang/StringBuffer#insert(kotlin.Int,%20kotlin.Char)(offset: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, c: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)` <br /> |
| [StringBuffer](https://developer.android.com/reference/kotlin/java/lang/StringBuffer#) | `https://developer.android.com/reference/kotlin/java/lang/StringBuffer#insert(kotlin.Int,%20kotlin.CharArray)(offset: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, str: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html!)` <br /> |
| [StringBuffer](https://developer.android.com/reference/kotlin/java/lang/StringBuffer#) | `https://developer.android.com/reference/kotlin/java/lang/StringBuffer#insert(kotlin.Int,%20kotlin.CharArray,%20kotlin.Int,%20kotlin.Int)(index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, str: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html!, offset: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, len: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` <br /> |
| [StringBuffer](https://developer.android.com/reference/kotlin/java/lang/StringBuffer#) | `https://developer.android.com/reference/kotlin/java/lang/StringBuffer#insert(kotlin.Int,%20kotlin.Double)(offset: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, d: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)` <br /> |
| [StringBuffer](https://developer.android.com/reference/kotlin/java/lang/StringBuffer#) | `https://developer.android.com/reference/kotlin/java/lang/StringBuffer#insert(kotlin.Int,%20kotlin.Float)(offset: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, f: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` <br /> |
| [StringBuffer](https://developer.android.com/reference/kotlin/java/lang/StringBuffer#) | `https://developer.android.com/reference/kotlin/java/lang/StringBuffer#insert(kotlin.Int,%20kotlin.Int)(offset: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, i: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` <br /> |
| [StringBuffer](https://developer.android.com/reference/kotlin/java/lang/StringBuffer#) | `https://developer.android.com/reference/kotlin/java/lang/StringBuffer#insert(kotlin.Int,%20kotlin.CharSequence)(dstOffset: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, s: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html?)` <br /> |
| [StringBuffer](https://developer.android.com/reference/kotlin/java/lang/StringBuffer#) | `https://developer.android.com/reference/kotlin/java/lang/StringBuffer#insert(kotlin.Int,%20kotlin.CharSequence,%20kotlin.Int,%20kotlin.Int)(dstOffset: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, s: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html?, start: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, end: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` <br /> |
| [StringBuffer](https://developer.android.com/reference/kotlin/java/lang/StringBuffer#) | `https://developer.android.com/reference/kotlin/java/lang/StringBuffer#insert(kotlin.Int,%20kotlin.Any)(offset: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, obj: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` <br /> |
| [StringBuffer](https://developer.android.com/reference/kotlin/java/lang/StringBuffer#) | `https://developer.android.com/reference/kotlin/java/lang/StringBuffer#insert(kotlin.Int,%20kotlin.String)(offset: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, str: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?)` <br /> |
| [StringBuffer](https://developer.android.com/reference/kotlin/java/lang/StringBuffer#) | `https://developer.android.com/reference/kotlin/java/lang/StringBuffer#insert(kotlin.Int,%20kotlin.Long)(offset: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, l: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/lang/StringBuffer#lastIndexOf(kotlin.String)(str: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/lang/StringBuffer#lastIndexOf(kotlin.String,%20kotlin.Int)(str: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, fromIndex: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/lang/StringBuffer#offsetByCodePoints(kotlin.Int,%20kotlin.Int)(index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, codePointOffset: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` <br /> |
| [StringBuffer](https://developer.android.com/reference/kotlin/java/lang/StringBuffer#) | `https://developer.android.com/reference/kotlin/java/lang/StringBuffer#repeat(kotlin.Int,%20kotlin.Int)(codePoint: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, count: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` <br /> |
| [StringBuffer](https://developer.android.com/reference/kotlin/java/lang/StringBuffer#) | `https://developer.android.com/reference/kotlin/java/lang/StringBuffer#repeat(kotlin.CharSequence,%20kotlin.Int)(cs: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html, count: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` <br /> |
| [StringBuffer](https://developer.android.com/reference/kotlin/java/lang/StringBuffer#) | `https://developer.android.com/reference/kotlin/java/lang/StringBuffer#replace(kotlin.Int,%20kotlin.Int,%20kotlin.String)(start: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, end: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, str: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` <br /> |
| [StringBuffer](https://developer.android.com/reference/kotlin/java/lang/StringBuffer#) | `https://developer.android.com/reference/kotlin/java/lang/StringBuffer#reverse()()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/lang/StringBuffer#setCharAt(kotlin.Int,%20kotlin.Char)(index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, ch: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/lang/StringBuffer#setLength(kotlin.Int)(newLength: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` <br /> |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html) | `https://developer.android.com/reference/kotlin/java/lang/StringBuffer#subSequence(kotlin.Int,%20kotlin.Int)(startIndex: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, endIndex: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/java/lang/StringBuffer#substring(kotlin.Int)(start: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/java/lang/StringBuffer#substring(kotlin.Int,%20kotlin.Int)(start: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, end: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/java/lang/StringBuffer#toString()()` Returns a string representation of the object. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/lang/StringBuffer#trimToSize()()` <br /> |

| Properties ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/lang/StringBuffer#length:kotlin.Int` Returns the length of this character sequence. |

## Public constructors

### StringBuffer

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
StringBuffer()
```

Constructs a string buffer with no characters in it and an initial capacity of 16 characters.

### StringBuffer

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
StringBuffer(capacity: Int)
```

Constructs a string buffer with no characters in it and the specified initial capacity.

| Parameters ||
|---|---|
| `capacity` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the initial capacity. |

| Exceptions ||
|---|---|
| `java.lang.NegativeArraySizeException` | if the `capacity` argument is less than `0`. |

### StringBuffer

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
StringBuffer(seq: CharSequence)
```

Constructs a string buffer that contains the same characters as the specified `CharSequence`. The initial capacity of the string buffer is `16` plus the length of the `CharSequence` argument.

If the length of the specified `CharSequence` is less than or equal to zero, then an empty buffer of capacity `16` is returned.

| Parameters ||
|---|---|
| `seq` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html): the sequence to copy. |

### StringBuffer

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
StringBuffer(str: String)
```

Constructs a string buffer initialized to the contents of the specified string. The initial capacity of the string buffer is `16` plus the length of the string argument.

| Parameters ||
|---|---|
| `str` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the initial contents of the buffer. |

## Public methods

### append

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun append(b: Boolean): StringBuffer
```

### append

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun append(c: Char): StringBuffer
```

Appends the specified character to this `Appendable`.

| Parameters ||
|---|---|
| `c` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html): The character to append |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/lang/StringBuffer#` | A reference to this `Appendable` |

| Exceptions ||
|---|---|
| `java.io.IOException` | If an I/O error occurs |

### append

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun append(str: CharArray!): StringBuffer
```

### append

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun append(
    str: CharArray!, 
    offset: Int, 
    len: Int
): StringBuffer
```

| Exceptions ||
|---|---|
| `java.lang.IndexOutOfBoundsException` | |

### append

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun append(d: Double): StringBuffer
```

### append

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun append(f: Float): StringBuffer
```

### append

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun append(i: Int): StringBuffer
```

### append

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun append(s: CharSequence?): StringBuffer
```

Appends the specified `CharSequence` to this sequence.

The characters of the `CharSequence` argument are appended, in order, increasing the length of this sequence by the length of the argument.

The result of this method is exactly the same as if it were an invocation of this.append(s, 0, s.length());

This method synchronizes on `this`, the destination object, but does not synchronize on the source (`s`).

If `s` is `null`, then the four characters `"null"` are appended.

| Parameters ||
|---|---|
| `csq` | The character sequence to append. If `csq` is `null`, then the four characters `"null"` are appended to this Appendable. |
| `s` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)?: the `CharSequence` to append. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/lang/StringBuffer#` | a reference to this object. |

| Exceptions ||
|---|---|
| `java.io.IOException` | If an I/O error occurs |

### append

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun append(
    s: CharSequence?, 
    start: Int, 
    end: Int
): StringBuffer
```

| Parameters ||
|---|---|
| `csq` | The character sequence from which a subsequence will be appended. If `csq` is `null`, then characters will be appended as if `csq` contained the four characters `"null"`. |
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The index of the first character in the subsequence |
| `end` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The index of the character following the last character in the subsequence |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/lang/StringBuffer#` | A reference to this `Appendable` |

| Exceptions ||
|---|---|
| `java.io.IOException` | If an I/O error occurs |
| `java.lang.IndexOutOfBoundsException` | If `start` or `end` are negative, `start` is greater than `end`, or `end` is greater than `csq.length()` |

### append

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun append(obj: Any?): StringBuffer
```

### append

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun append(str: String?): StringBuffer
```

### append

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun append(sb: StringBuffer?): StringBuffer
```

Appends the specified `StringBuffer` to this sequence.

The characters of the `StringBuffer` argument are appended, in order, to the contents of this `StringBuffer`, increasing the length of this `StringBuffer` by the length of the argument. If `sb` is `null`, then the four characters `"null"` are appended to this `StringBuffer`.

Let *n* be the length of the old character sequence, the one contained in the `StringBuffer` just prior to execution of the `append` method. Then the character at index *k* in the new character sequence is equal to the character at index *k* in the old character sequence, if *k* is less than *n* ; otherwise, it is equal to the character at index *k-n* in the argument `sb`.

This method synchronizes on `this`, the destination object, but does not synchronize on the source (`sb`).

| Parameters ||
|---|---|
| `sb` | [StringBuffer](https://developer.android.com/reference/kotlin/java/lang/StringBuffer#)?: the `StringBuffer` to append. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/lang/StringBuffer#` | a reference to this object. |

### append

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun append(lng: Long): StringBuffer
```

### appendCodePoint

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun appendCodePoint(codePoint: Int): StringBuffer
```

### capacity

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun capacity(): Int
```

### chars

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun chars(): IntStream
```

Returns a stream of `int` zero-extending the `char` values from this sequence. Any char which maps to a [surrogate code point](https://developer.android.com//reference/java/lang/Character.html#unicode) is passed through uninterpreted.

The stream binds to this sequence when the terminal stream operation commences (specifically, for mutable sequences the spliterator for the stream is [*late-binding*](https://developer.android.com/reference/kotlin/java/util/Spliterator.html#binding)). If the sequence is modified during that operation then the result is undefined.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/stream/IntStream.html#` | an IntStream of char values from this sequence |

### codePointAt

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun codePointAt(index: Int): Int
```

| Exceptions ||
|---|---|
| `java.lang.IndexOutOfBoundsException` | |

### codePointBefore

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun codePointBefore(index: Int): Int
```

| Exceptions ||
|---|---|
| `java.lang.IndexOutOfBoundsException` | |

### codePointCount

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun codePointCount(
    beginIndex: Int, 
    endIndex: Int
): Int
```

| Exceptions ||
|---|---|
| `java.lang.IndexOutOfBoundsException` | |

### codePoints

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun codePoints(): IntStream
```

Returns a stream of code point values from this sequence. Any surrogate pairs encountered in the sequence are combined as if by [Character.toCodePoint](https://developer.android.com/reference/kotlin/java/lang/Character#toCodePoint(kotlin.Char,%20kotlin.Char)) and the result is passed to the stream. Any other code units, including ordinary BMP characters, unpaired surrogates, and undefined code units, are zero-extended to `int` values which are then passed to the stream.

The stream binds to this sequence when the terminal stream operation commences (specifically, for mutable sequences the spliterator for the stream is [*late-binding*](https://developer.android.com/reference/kotlin/java/util/Spliterator.html#binding)). If the sequence is modified during that operation then the result is undefined.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/stream/IntStream.html#` | an IntStream of Unicode code points from this sequence |

### compareTo

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun compareTo(other: StringBuffer): Int
```

Compares two `StringBuffer` instances lexicographically. This method follows the same rules for lexicographical comparison as defined in the [CharSequence.compare(this, another)](https://developer.android.com/reference/kotlin/java/lang/CharSequence#compare(kotlin.CharSequence,%20kotlin.CharSequence)) method.

For finer-grained, locale-sensitive String comparison, refer to `https://developer.android.com/reference/kotlin/java/text/Collator.html#`.

| Parameters ||
|---|---|
| `o` | the object to be compared. |
| `another` | the `StringBuffer` to be compared with |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the value `0` if this `StringBuffer` contains the same character sequence as that of the argument `StringBuffer`; a negative integer if this `StringBuffer` is lexicographically less than the `StringBuffer` argument; or a positive integer if this `StringBuffer` is lexicographically greater than the `StringBuffer` argument. |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the specified object's type prevents it from being compared to this object. |
| `java.lang.NullPointerException` | if the specified object is null |

### delete

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun delete(
    start: Int, 
    end: Int
): StringBuffer
```

| Exceptions ||
|---|---|
| `java.lang.StringIndexOutOfBoundsException` | |

### deleteCharAt

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun deleteCharAt(index: Int): StringBuffer
```

| Exceptions ||
|---|---|
| `java.lang.StringIndexOutOfBoundsException` | |

### ensureCapacity

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun ensureCapacity(minimumCapacity: Int): Unit
```

### get

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun get(index: Int): Char
```

| Parameters ||
|---|---|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index of the `char` value to be returned |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html` | the specified `char` value |

| Exceptions ||
|---|---|
| `java.lang.IndexOutOfBoundsException` | if the `index` argument is negative or not less than `length()` |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/StringBuffer#length:kotlin.Int`

### getChars

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getChars(
    srcBegin: Int, 
    srcEnd: Int, 
    dst: CharArray, 
    dstBegin: Int
): Unit
```

| Parameters ||
|---|---|
| `srcBegin` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): start copying at this offset. |
| `srcEnd` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): stop copying at this offset. |
| `dst` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html): the array to copy the data into. |
| `dstBegin` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): offset into `dst`. |

| Exceptions ||
|---|---|
| `java.lang.IndexOutOfBoundsException` | if any of the following is true: - `srcBegin` is negative - `dstBegin` is negative - the `srcBegin` argument is greater than the `srcEnd` argument. - `srcEnd` is greater than `this.length()`. - `dstBegin+srcEnd-srcBegin` is greater than `dst.length` |
| `java.lang.NullPointerException` | if `dst` is `null` |

### indexOf

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun indexOf(str: String): Int
```

### indexOf

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun indexOf(
    str: String, 
    fromIndex: Int
): Int
```

### insert

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun insert(
    offset: Int, 
    b: Boolean
): StringBuffer
```

| Exceptions ||
|---|---|
| `java.lang.StringIndexOutOfBoundsException` | |

### insert

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun insert(
    offset: Int, 
    c: Char
): StringBuffer
```

| Exceptions ||
|---|---|
| `java.lang.IndexOutOfBoundsException` | |

### insert

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun insert(
    offset: Int, 
    str: CharArray!
): StringBuffer
```

| Exceptions ||
|---|---|
| `java.lang.StringIndexOutOfBoundsException` | |

### insert

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun insert(
    index: Int, 
    str: CharArray!, 
    offset: Int, 
    len: Int
): StringBuffer
```

| Exceptions ||
|---|---|
| `java.lang.StringIndexOutOfBoundsException` | |

### insert

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun insert(
    offset: Int, 
    d: Double
): StringBuffer
```

| Exceptions ||
|---|---|
| `java.lang.StringIndexOutOfBoundsException` | |

### insert

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun insert(
    offset: Int, 
    f: Float
): StringBuffer
```

| Exceptions ||
|---|---|
| `java.lang.StringIndexOutOfBoundsException` | |

### insert

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun insert(
    offset: Int, 
    i: Int
): StringBuffer
```

| Exceptions ||
|---|---|
| `java.lang.StringIndexOutOfBoundsException` | |

### insert

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun insert(
    dstOffset: Int, 
    s: CharSequence?
): StringBuffer
```

| Exceptions ||
|---|---|
| `java.lang.IndexOutOfBoundsException` | |

### insert

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun insert(
    dstOffset: Int, 
    s: CharSequence?, 
    start: Int, 
    end: Int
): StringBuffer
```

| Exceptions ||
|---|---|
| `java.lang.IndexOutOfBoundsException` | |

### insert

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun insert(
    offset: Int, 
    obj: Any?
): StringBuffer
```

| Exceptions ||
|---|---|
| `java.lang.StringIndexOutOfBoundsException` | |

### insert

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun insert(
    offset: Int, 
    str: String?
): StringBuffer
```

| Exceptions ||
|---|---|
| `java.lang.StringIndexOutOfBoundsException` | |

### insert

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun insert(
    offset: Int, 
    l: Long
): StringBuffer
```

| Exceptions ||
|---|---|
| `java.lang.StringIndexOutOfBoundsException` | |

### lastIndexOf

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun lastIndexOf(str: String): Int
```

### lastIndexOf

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun lastIndexOf(
    str: String, 
    fromIndex: Int
): Int
```

### offsetByCodePoints

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun offsetByCodePoints(
    index: Int, 
    codePointOffset: Int
): Int
```

| Exceptions ||
|---|---|
| `java.lang.IndexOutOfBoundsException` | |

### repeat

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun repeat(
    codePoint: Int, 
    count: Int
): StringBuffer
```

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | |

### repeat

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun repeat(
    cs: CharSequence, 
    count: Int
): StringBuffer
```

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | |

### replace

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun replace(
    start: Int, 
    end: Int, 
    str: String
): StringBuffer
```

| Exceptions ||
|---|---|
| `java.lang.StringIndexOutOfBoundsException` | |

### reverse

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun reverse(): StringBuffer
```

### setCharAt

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setCharAt(
    index: Int, 
    ch: Char
): Unit
```

| Exceptions ||
|---|---|
| `java.lang.IndexOutOfBoundsException` | |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/StringBuffer#length:kotlin.Int`

### setLength

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setLength(newLength: Int): Unit
```

| Exceptions ||
|---|---|
| `java.lang.IndexOutOfBoundsException` | |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/StringBuffer#length:kotlin.Int`

### subSequence

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun subSequence(
    startIndex: Int, 
    endIndex: Int
): CharSequence
```

| Parameters ||
|---|---|
| `start` | the start index, inclusive |
| `end` | the end index, exclusive |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html` | the specified subsequence |

| Exceptions ||
|---|---|
| `java.lang.IndexOutOfBoundsException` | if `start` or `end` are negative, if `end` is greater than `length()`, or if `start` is greater than `end` |

### substring

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun substring(start: Int): String
```

| Exceptions ||
|---|---|
| `java.lang.StringIndexOutOfBoundsException` | |

### substring

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun substring(
    start: Int, 
    end: Int
): String
```

| Exceptions ||
|---|---|
| `java.lang.StringIndexOutOfBoundsException` | |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toString(): String
```

Returns a string representation of the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string consisting of exactly this sequence of characters |

### trimToSize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun trimToSize(): Unit
```

## Properties

### length

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
val length: Int
```

Returns the length of this character sequence. The length is the number of 16-bit `char`s in the sequence.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the number of `char`s in this sequence |
