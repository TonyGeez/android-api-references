Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# StringBuilder

```
class StringBuilder : Appendable, CharSequence, Comparable<StringBuilder!>, Serializable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.lang.StringBuilder](https://developer.android.com/reference/kotlin/java/lang/StringBuilder#) |

A mutable sequence of characters. This class provides an API compatible with `StringBuffer`, but with no guarantee of synchronization. This class is designed for use as a drop-in replacement for `StringBuffer` in places where the string buffer was being used by a single thread (as is generally the case). Where possible, it is recommended that this class be used in preference to `StringBuffer` as it will be faster under most implementations.

The principal operations on a `StringBuilder` are the `append` and `insert` methods, which are overloaded so as to accept data of any type. Each effectively converts a given datum to a string and then appends or inserts the characters of that string to the string builder. The `append` method always adds these characters at the end of the builder; the `insert` method adds the characters at a specified point.

For example, if `z` refers to a string builder object whose current contents are "`start`", then the method call `z.append("le")` would cause the string builder to contain "`startle`", whereas `z.insert(4, "le")` would alter the string builder to contain "`starlet`".

In general, if sb refers to an instance of a `StringBuilder`, then `sb.append(x)` has the same effect as `sb.insert(sb.length(), x)`.

Every string builder has a capacity. As long as the length of the character sequence contained in the string builder does not exceed the capacity, it is not necessary to allocate a new internal buffer. If the internal buffer overflows, it is automatically made larger.

Instances of `StringBuilder` are not safe for use by multiple threads. If such synchronization is required then it is recommended that `https://developer.android.com/reference/kotlin/java/lang/StringBuffer` be used.

Unless otherwise noted, passing a `null` argument to a constructor or method in this class will cause a `https://developer.android.com/reference/kotlin/java/lang/NullPointerException` to be thrown.

## Summary

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/lang/StringBuilder#StringBuilder()()` Constructs a string builder with no characters in it and an initial capacity of 16 characters. |
| `https://developer.android.com/reference/kotlin/java/lang/StringBuilder#StringBuilder(kotlin.Int)(capacity: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Constructs a string builder with no characters in it and an initial capacity specified by the `capacity` argument. |
| `https://developer.android.com/reference/kotlin/java/lang/StringBuilder#StringBuilder(kotlin.CharSequence)(seq: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)` Constructs a string builder that contains the same characters as the specified `CharSequence`. |
| `https://developer.android.com/reference/kotlin/java/lang/StringBuilder#StringBuilder(kotlin.String)(str: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Constructs a string builder initialized to the contents of the specified string. |

| Public methods ||
|---|---|
| [StringBuilder](https://developer.android.com/reference/kotlin/java/lang/StringBuilder#) | `https://developer.android.com/reference/kotlin/java/lang/StringBuilder#append(kotlin.Boolean)(b: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` <br /> |
| [StringBuilder](https://developer.android.com/reference/kotlin/java/lang/StringBuilder#) | `https://developer.android.com/reference/kotlin/java/lang/StringBuilder#append(kotlin.Char)(c: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)` Appends the specified character to this `Appendable`. |
| [StringBuilder](https://developer.android.com/reference/kotlin/java/lang/StringBuilder#) | `https://developer.android.com/reference/kotlin/java/lang/StringBuilder#append(kotlin.CharArray)(str: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html!)` <br /> |
| --- | --- |
| [StringBuilder](https://developer.android.com/reference/kotlin/java/lang/StringBuilder#) | `https://developer.android.com/reference/kotlin/java/lang/StringBuilder#append(kotlin.CharArray,%20kotlin.Int,%20kotlin.Int)(str: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html!, offset: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, len: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` <br /> |
| [StringBuilder](https://developer.android.com/reference/kotlin/java/lang/StringBuilder#) | `https://developer.android.com/reference/kotlin/java/lang/StringBuilder#append(kotlin.Double)(d: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)` <br /> |
| [StringBuilder](https://developer.android.com/reference/kotlin/java/lang/StringBuilder#) | `https://developer.android.com/reference/kotlin/java/lang/StringBuilder#append(kotlin.Float)(f: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` <br /> |
| --- | --- |
| [StringBuilder](https://developer.android.com/reference/kotlin/java/lang/StringBuilder#) | `https://developer.android.com/reference/kotlin/java/lang/StringBuilder#append(kotlin.Int)(i: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` <br /> |
| [StringBuilder](https://developer.android.com/reference/kotlin/java/lang/StringBuilder#) | `https://developer.android.com/reference/kotlin/java/lang/StringBuilder#append(kotlin.CharSequence)(s: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html?)` Appends the specified character sequence to this `Appendable`. |
| [StringBuilder](https://developer.android.com/reference/kotlin/java/lang/StringBuilder#) | `https://developer.android.com/reference/kotlin/java/lang/StringBuilder#append(kotlin.CharSequence,%20kotlin.Int,%20kotlin.Int)(s: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html?, start: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, end: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` <br /> |
| --- | --- |
| [StringBuilder](https://developer.android.com/reference/kotlin/java/lang/StringBuilder#) | `https://developer.android.com/reference/kotlin/java/lang/StringBuilder#append(kotlin.Any)(obj: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` <br /> |
| [StringBuilder](https://developer.android.com/reference/kotlin/java/lang/StringBuilder#) | `https://developer.android.com/reference/kotlin/java/lang/StringBuilder#append(kotlin.String)(str: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?)` <br /> |
| [StringBuilder](https://developer.android.com/reference/kotlin/java/lang/StringBuilder#) | `https://developer.android.com/reference/kotlin/java/lang/StringBuilder#append(java.lang.StringBuffer)(sb: https://developer.android.com/reference/kotlin/java/lang/StringBuffer?)` Appends the specified `StringBuffer` to this sequence. |
| --- | --- |
| [StringBuilder](https://developer.android.com/reference/kotlin/java/lang/StringBuilder#) | `https://developer.android.com/reference/kotlin/java/lang/StringBuilder#append(kotlin.Long)(lng: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` <br /> |
| [StringBuilder](https://developer.android.com/reference/kotlin/java/lang/StringBuilder#) | `https://developer.android.com/reference/kotlin/java/lang/StringBuilder#appendCodePoint(kotlin.Int)(codePoint: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/lang/StringBuilder#capacity()()` Returns the current capacity. |
| --- | --- |
| [IntStream](https://developer.android.com/reference/kotlin/java/util/stream/IntStream.html#) | `https://developer.android.com/reference/kotlin/java/lang/StringBuilder#chars()()` Returns a stream of `int` zero-extending the `char` values from this sequence. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/lang/StringBuilder#codePointAt(kotlin.Int)(index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the character (Unicode code point) at the specified index. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/lang/StringBuilder#codePointBefore(kotlin.Int)(index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the character (Unicode code point) before the specified index. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/lang/StringBuilder#codePointCount(kotlin.Int,%20kotlin.Int)(beginIndex: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, endIndex: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the number of Unicode code points in the specified text range of this sequence. |
| [IntStream](https://developer.android.com/reference/kotlin/java/util/stream/IntStream.html#) | `https://developer.android.com/reference/kotlin/java/lang/StringBuilder#codePoints()()` Returns a stream of code point values from this sequence. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/lang/StringBuilder#compareTo(java.lang.StringBuilder)(other: https://developer.android.com/reference/kotlin/java/lang/StringBuilder#)` Compares two `StringBuilder` instances lexicographically. |
| --- | --- |
| [StringBuilder](https://developer.android.com/reference/kotlin/java/lang/StringBuilder#) | `https://developer.android.com/reference/kotlin/java/lang/StringBuilder#delete(kotlin.Int,%20kotlin.Int)(start: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, end: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` <br /> |
| [StringBuilder](https://developer.android.com/reference/kotlin/java/lang/StringBuilder#) | `https://developer.android.com/reference/kotlin/java/lang/StringBuilder#deleteCharAt(kotlin.Int)(index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/lang/StringBuilder#ensureCapacity(kotlin.Int)(minimumCapacity: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Ensures that the capacity is at least equal to the specified minimum. |
| --- | --- |
| [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | `https://developer.android.com/reference/kotlin/java/lang/StringBuilder#get(kotlin.Int)(index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the `char` value in this sequence at the specified index. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/lang/StringBuilder#getChars(kotlin.Int,%20kotlin.Int,%20kotlin.CharArray,%20kotlin.Int)(srcBegin: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, srcEnd: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, dst: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html, dstBegin: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Copies characters from this sequence into the given destination array. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/lang/StringBuilder#indexOf(kotlin.String)(str: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` <br /> |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/lang/StringBuilder#indexOf(kotlin.String,%20kotlin.Int)(str: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, fromIndex: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` <br /> |
| [StringBuilder](https://developer.android.com/reference/kotlin/java/lang/StringBuilder#) | `https://developer.android.com/reference/kotlin/java/lang/StringBuilder#insert(kotlin.Int,%20kotlin.Boolean)(offset: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, b: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` <br /> |
| [StringBuilder](https://developer.android.com/reference/kotlin/java/lang/StringBuilder#) | `https://developer.android.com/reference/kotlin/java/lang/StringBuilder#insert(kotlin.Int,%20kotlin.Char)(offset: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, c: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)` <br /> |
| --- | --- |
| [StringBuilder](https://developer.android.com/reference/kotlin/java/lang/StringBuilder#) | `https://developer.android.com/reference/kotlin/java/lang/StringBuilder#insert(kotlin.Int,%20kotlin.CharArray)(offset: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, str: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html!)` <br /> |
| [StringBuilder](https://developer.android.com/reference/kotlin/java/lang/StringBuilder#) | `https://developer.android.com/reference/kotlin/java/lang/StringBuilder#insert(kotlin.Int,%20kotlin.CharArray,%20kotlin.Int,%20kotlin.Int)(index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, str: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html!, offset: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, len: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` <br /> |
| [StringBuilder](https://developer.android.com/reference/kotlin/java/lang/StringBuilder#) | `https://developer.android.com/reference/kotlin/java/lang/StringBuilder#insert(kotlin.Int,%20kotlin.Double)(offset: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, d: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)` <br /> |
| --- | --- |
| [StringBuilder](https://developer.android.com/reference/kotlin/java/lang/StringBuilder#) | `https://developer.android.com/reference/kotlin/java/lang/StringBuilder#insert(kotlin.Int,%20kotlin.Float)(offset: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, f: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` <br /> |
| [StringBuilder](https://developer.android.com/reference/kotlin/java/lang/StringBuilder#) | `https://developer.android.com/reference/kotlin/java/lang/StringBuilder#insert(kotlin.Int,%20kotlin.Int)(offset: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, i: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` <br /> |
| [StringBuilder](https://developer.android.com/reference/kotlin/java/lang/StringBuilder#) | `https://developer.android.com/reference/kotlin/java/lang/StringBuilder#insert(kotlin.Int,%20kotlin.CharSequence)(dstOffset: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, s: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html?)` <br /> |
| --- | --- |
| [StringBuilder](https://developer.android.com/reference/kotlin/java/lang/StringBuilder#) | `https://developer.android.com/reference/kotlin/java/lang/StringBuilder#insert(kotlin.Int,%20kotlin.CharSequence,%20kotlin.Int,%20kotlin.Int)(dstOffset: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, s: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html?, start: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, end: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` <br /> |
| [StringBuilder](https://developer.android.com/reference/kotlin/java/lang/StringBuilder#) | `https://developer.android.com/reference/kotlin/java/lang/StringBuilder#insert(kotlin.Int,%20kotlin.Any)(offset: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, obj: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` <br /> |
| [StringBuilder](https://developer.android.com/reference/kotlin/java/lang/StringBuilder#) | `https://developer.android.com/reference/kotlin/java/lang/StringBuilder#insert(kotlin.Int,%20kotlin.String)(offset: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, str: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?)` <br /> |
| --- | --- |
| [StringBuilder](https://developer.android.com/reference/kotlin/java/lang/StringBuilder#) | `https://developer.android.com/reference/kotlin/java/lang/StringBuilder#insert(kotlin.Int,%20kotlin.Long)(offset: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, l: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/lang/StringBuilder#lastIndexOf(kotlin.String)(str: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/lang/StringBuilder#lastIndexOf(kotlin.String,%20kotlin.Int)(str: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, fromIndex: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` <br /> |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/lang/StringBuilder#offsetByCodePoints(kotlin.Int,%20kotlin.Int)(index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, codePointOffset: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the index within this sequence that is offset from the given `index` by `codePointOffset` code points. |
| [StringBuilder](https://developer.android.com/reference/kotlin/java/lang/StringBuilder#) | `https://developer.android.com/reference/kotlin/java/lang/StringBuilder#repeat(kotlin.Int,%20kotlin.Int)(codePoint: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, count: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` <br /> |
| [StringBuilder](https://developer.android.com/reference/kotlin/java/lang/StringBuilder#) | `https://developer.android.com/reference/kotlin/java/lang/StringBuilder#repeat(kotlin.CharSequence,%20kotlin.Int)(cs: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html, count: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` <br /> |
| --- | --- |
| [StringBuilder](https://developer.android.com/reference/kotlin/java/lang/StringBuilder#) | `https://developer.android.com/reference/kotlin/java/lang/StringBuilder#replace(kotlin.Int,%20kotlin.Int,%20kotlin.String)(start: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, end: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, str: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` <br /> |
| [StringBuilder](https://developer.android.com/reference/kotlin/java/lang/StringBuilder#) | `https://developer.android.com/reference/kotlin/java/lang/StringBuilder#reverse()()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/lang/StringBuilder#setCharAt(kotlin.Int,%20kotlin.Char)(index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, ch: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)` The character at the specified index is set to `ch`. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/lang/StringBuilder#setLength(kotlin.Int)(newLength: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Sets the length of the character sequence. |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html) | `https://developer.android.com/reference/kotlin/java/lang/StringBuilder#subSequence(kotlin.Int,%20kotlin.Int)(startIndex: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, endIndex: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns a new character sequence that is a subsequence of this sequence. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/java/lang/StringBuilder#substring(kotlin.Int)(start: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns a new `String` that contains a subsequence of characters currently contained in this character sequence. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/java/lang/StringBuilder#substring(kotlin.Int,%20kotlin.Int)(start: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, end: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns a new `String` that contains a subsequence of characters currently contained in this sequence. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/java/lang/StringBuilder#toString()()` Returns a string representation of the object. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/lang/StringBuilder#trimToSize()()` Attempts to reduce storage used for the character sequence. |
| --- | --- |

| Properties ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/lang/StringBuilder#length:kotlin.Int` Returns the length (character count). |

## Public constructors

### StringBuilder

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
StringBuilder()
```

Constructs a string builder with no characters in it and an initial capacity of 16 characters.

### StringBuilder

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
StringBuilder(capacity: Int)
```

Constructs a string builder with no characters in it and an initial capacity specified by the `capacity` argument.

| Parameters ||
|---|---|
| `capacity` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the initial capacity. |

| Exceptions ||
|---|---|
| `java.lang.NegativeArraySizeException` | if the `capacity` argument is less than `0`. |

### StringBuilder

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
StringBuilder(seq: CharSequence)
```

Constructs a string builder that contains the same characters as the specified `CharSequence`. The initial capacity of the string builder is `16` plus the length of the `CharSequence` argument.

| Parameters ||
|---|---|
| `seq` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html): the sequence to copy. |

### StringBuilder

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
StringBuilder(str: String)
```

Constructs a string builder initialized to the contents of the specified string. The initial capacity of the string builder is `16` plus the length of the string argument.

| Parameters ||
|---|---|
| `str` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the initial contents of the buffer. |

## Public methods

### append

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun append(b: Boolean): StringBuilder
```

### append

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun append(c: Char): StringBuilder
```

Appends the specified character to this `Appendable`.

| Parameters ||
|---|---|
| `c` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html): The character to append |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/lang/StringBuilder#` | A reference to this `Appendable` |

| Exceptions ||
|---|---|
| `java.io.IOException` | If an I/O error occurs |

### append

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun append(str: CharArray!): StringBuilder
```

### append

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun append(
    str: CharArray!, 
    offset: Int, 
    len: Int
): StringBuilder
```

| Exceptions ||
|---|---|
| `java.lang.IndexOutOfBoundsException` | |

### append

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun append(d: Double): StringBuilder
```

### append

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun append(f: Float): StringBuilder
```

### append

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun append(i: Int): StringBuilder
```

### append

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun append(s: CharSequence?): StringBuilder
```

Appends the specified character sequence to this `Appendable`.

Depending on which class implements the character sequence `csq`, the entire sequence may not be appended. For instance, if `csq` is a `https://developer.android.com/reference/kotlin/java/nio/CharBuffer.html#` then the subsequence to append is defined by the buffer's position and limit.

| Parameters ||
|---|---|
| `csq` | The character sequence to append. If `csq` is `null`, then the four characters `"null"` are appended to this Appendable. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/lang/StringBuilder#` | A reference to this `Appendable` |

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
): StringBuilder
```

| Parameters ||
|---|---|
| `csq` | The character sequence from which a subsequence will be appended. If `csq` is `null`, then characters will be appended as if `csq` contained the four characters `"null"`. |
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The index of the first character in the subsequence |
| `end` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The index of the character following the last character in the subsequence |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/lang/StringBuilder#` | A reference to this `Appendable` |

| Exceptions ||
|---|---|
| `java.io.IOException` | If an I/O error occurs |
| `java.lang.IndexOutOfBoundsException` | If `start` or `end` are negative, `start` is greater than `end`, or `end` is greater than `csq.length()` |

### append

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun append(obj: Any?): StringBuilder
```

### append

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun append(str: String?): StringBuilder
```

### append

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun append(sb: StringBuffer?): StringBuilder
```

Appends the specified `StringBuffer` to this sequence.

The characters of the `StringBuffer` argument are appended, in order, to this sequence, increasing the length of this sequence by the length of the argument. If `sb` is `null`, then the four characters `"null"` are appended to this sequence.

Let *n* be the length of this character sequence just prior to execution of the `append` method. Then the character at index *k* in the new character sequence is equal to the character at index *k* in the old character sequence, if *k* is less than *n* ; otherwise, it is equal to the character at index *k-n* in the argument `sb`.

| Parameters ||
|---|---|
| `sb` | [StringBuffer](https://developer.android.com/reference/kotlin/java/lang/StringBuffer)?: the `StringBuffer` to append. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/lang/StringBuilder#` | a reference to this object. |

### append

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun append(lng: Long): StringBuilder
```

### appendCodePoint

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun appendCodePoint(codePoint: Int): StringBuilder
```

### capacity

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun capacity(): Int
```

Returns the current capacity. The capacity is the amount of storage available for newly inserted characters, beyond which an allocation will occur.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the current capacity |

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

Returns the character (Unicode code point) at the specified index. The index refers to `char` values (Unicode code units) and ranges from `0` to `https://developer.android.com/reference/kotlin/java/lang/StringBuilder#length:kotlin.Int``- 1`.

If the `char` value specified at the given index is in the high-surrogate range, the following index is less than the length of this sequence, and the `char` value at the following index is in the low-surrogate range, then the supplementary code point corresponding to this surrogate pair is returned. Otherwise, the `char` value at the given index is returned.

| Parameters ||
|---|---|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index to the `char` values |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the code point value of the character at the `index` |

| Exceptions ||
|---|---|
| `java.lang.IndexOutOfBoundsException` | if the `index` argument is negative or not less than the length of this sequence. |

### codePointBefore

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun codePointBefore(index: Int): Int
```

Returns the character (Unicode code point) before the specified index. The index refers to `char` values (Unicode code units) and ranges from `1` to `https://developer.android.com/reference/kotlin/java/lang/StringBuilder#length:kotlin.Int`.

If the `char` value at `(index - 1)` is in the low-surrogate range, `(index - 2)` is not negative, and the `char` value at `(index - 2)` is in the high-surrogate range, then the supplementary code point value of the surrogate pair is returned. If the `char` value at `index - 1` is an unpaired low-surrogate or a high-surrogate, the surrogate value is returned.

| Parameters ||
|---|---|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index following the code point that should be returned |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the Unicode code point value before the given index. |

| Exceptions ||
|---|---|
| `java.lang.IndexOutOfBoundsException` | if the `index` argument is less than 1 or greater than the length of this sequence. |

### codePointCount

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun codePointCount(
    beginIndex: Int, 
    endIndex: Int
): Int
```

Returns the number of Unicode code points in the specified text range of this sequence. The text range begins at the specified `beginIndex` and extends to the `char` at index `endIndex - 1`. Thus the length (in `char`s) of the text range is `endIndex-beginIndex`. Unpaired surrogates within this sequence count as one code point each.

| Parameters ||
|---|---|
| `beginIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index to the first `char` of the text range. |
| `endIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index after the last `char` of the text range. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the number of Unicode code points in the specified text range |

| Exceptions ||
|---|---|
| `java.lang.IndexOutOfBoundsException` | if the `beginIndex` is negative, or `endIndex` is larger than the length of this sequence, or `beginIndex` is larger than `endIndex`. |

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
fun compareTo(other: StringBuilder): Int
```

Compares two `StringBuilder` instances lexicographically. This method follows the same rules for lexicographical comparison as defined in the [CharSequence.compare(this, another)](https://developer.android.com/reference/kotlin/java/lang/CharSequence#compare(kotlin.CharSequence,%20kotlin.CharSequence)) method.

For finer-grained, locale-sensitive String comparison, refer to `https://developer.android.com/reference/kotlin/java/text/Collator.html#`.

| Parameters ||
|---|---|
| `o` | the object to be compared. |
| `another` | the `StringBuilder` to be compared with |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the value `0` if this `StringBuilder` contains the same character sequence as that of the argument `StringBuilder`; a negative integer if this `StringBuilder` is lexicographically less than the `StringBuilder` argument; or a positive integer if this `StringBuilder` is lexicographically greater than the `StringBuilder` argument. |

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
): StringBuilder
```

| Exceptions ||
|---|---|
| `java.lang.StringIndexOutOfBoundsException` | |

### deleteCharAt

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun deleteCharAt(index: Int): StringBuilder
```

| Exceptions ||
|---|---|
| `java.lang.StringIndexOutOfBoundsException` | |

### ensureCapacity

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun ensureCapacity(minimumCapacity: Int): Unit
```

Ensures that the capacity is at least equal to the specified minimum. If the current capacity is less than the argument, then a new internal array is allocated with greater capacity. The new capacity is the larger of:

- The `minimumCapacity` argument.
- Twice the old capacity, plus `2`.

If the `minimumCapacity` argument is nonpositive, this method takes no action and simply returns. Note that subsequent operations on this object can reduce the actual capacity below that requested here.

<br />

| Parameters ||
|---|---|
| `minimumCapacity` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the minimum desired capacity. |

### get

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun get(index: Int): Char
```

Returns the `char` value in this sequence at the specified index. The first `char` value is at index `0`, the next at index `1`, and so on, as in array indexing.

The index argument must be greater than or equal to `0`, and less than the length of this sequence.

If the `char` value specified by the index is a [surrogate](https://developer.android.com/reference/kotlin/java/lang/Character#unicode), the surrogate value is returned.

| Parameters ||
|---|---|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index of the desired `char` value. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html` | the `char` value at the specified index. |

| Exceptions ||
|---|---|
| `java.lang.IndexOutOfBoundsException` | if `index` is negative or greater than or equal to `length()`. |

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

Copies characters from this sequence into the given destination array. The first character to be copied is at index `srcBegin`; the last character to be copied is at index `srcEnd-1`. The total number of characters to be copied is `srcEnd-srcBegin`. The characters are copied into the subarray of `dst` starting at index `dstBegin` and ending at index:

```kotlin
<code>dstbegin + (srcEnd-srcBegin) - 1
  </code>
```

<br />

| Parameters ||
|---|---|
| `srcBegin` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): start copying at this offset. |
| `srcEnd` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): stop copying at this offset. |
| `dst` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html): the array to copy the data into. |
| --- | --- |
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
): StringBuilder
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
): StringBuilder
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
): StringBuilder
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
): StringBuilder
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
): StringBuilder
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
): StringBuilder
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
): StringBuilder
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
): StringBuilder
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
): StringBuilder
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
): StringBuilder
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
): StringBuilder
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
): StringBuilder
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

Returns the index within this sequence that is offset from the given `index` by `codePointOffset` code points. Unpaired surrogates within the text range given by `index` and `codePointOffset` count as one code point each.

| Parameters ||
|---|---|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index to be offset |
| `codePointOffset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the offset in code points |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the index within this sequence |

| Exceptions ||
|---|---|
| `java.lang.IndexOutOfBoundsException` | if `index` is negative or larger then the length of this sequence, or if `codePointOffset` is positive and the subsequence starting with `index` has fewer than `codePointOffset` code points, or if `codePointOffset` is negative and the subsequence before `index` has fewer than the absolute value of `codePointOffset` code points. |

### repeat

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun repeat(
    codePoint: Int, 
    count: Int
): StringBuilder
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
): StringBuilder
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
): StringBuilder
```

| Exceptions ||
|---|---|
| `java.lang.StringIndexOutOfBoundsException` | |

### reverse

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun reverse(): StringBuilder
```

### setCharAt

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setCharAt(
    index: Int, 
    ch: Char
): Unit
```

The character at the specified index is set to `ch`. This sequence is altered to represent a new character sequence that is identical to the old character sequence, except that it contains the character `ch` at position `index`.

The index argument must be greater than or equal to `0`, and less than the length of this sequence.

| Parameters ||
|---|---|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index of the character to modify. |
| `ch` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html): the new character. |

| Exceptions ||
|---|---|
| `java.lang.IndexOutOfBoundsException` | if `index` is negative or greater than or equal to `length()`. |

### setLength

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setLength(newLength: Int): Unit
```

Sets the length of the character sequence. The sequence is changed to a new character sequence whose length is specified by the argument. For every nonnegative index *k* less than `newLength`, the character at index *k* in the new character sequence is the same as the character at index *k* in the old sequence if *k* is less than the length of the old character sequence; otherwise, it is the null character `'\u005Cu0000'`. In other words, if the `newLength` argument is less than the current length, the length is changed to the specified length.

If the `newLength` argument is greater than or equal to the current length, sufficient null characters (`'\u005Cu0000'`) are appended so that length becomes the `newLength` argument.

The `newLength` argument must be greater than or equal to `0`.

| Parameters ||
|---|---|
| `newLength` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the new length |

| Exceptions ||
|---|---|
| `java.lang.IndexOutOfBoundsException` | if the `newLength` argument is negative. |

### subSequence

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun subSequence(
    startIndex: Int, 
    endIndex: Int
): CharSequence
```

Returns a new character sequence that is a subsequence of this sequence.

An invocation of this method of the form

```kotlin
<code>sb.subSequence(begin,&amp;nbsp;end)</code>
```
behaves in exactly the same way as the invocation

```kotlin
<code>sb.substring(begin,&amp;nbsp;end)</code>
```
This method is provided so that this class can implement the `https://developer.android.com/reference/kotlin/java/lang/CharSequence` interface.

| Parameters ||
|---|---|
| `start` | the start index, inclusive. |
| `end` | the end index, exclusive. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html` | the specified subsequence. |

| Exceptions ||
|---|---|
| `java.lang.IndexOutOfBoundsException` | if `start` or `end` are negative, if `end` is greater than `length()`, or if `start` is greater than `end` |

### substring

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun substring(start: Int): String
```

Returns a new `String` that contains a subsequence of characters currently contained in this character sequence. The substring begins at the specified index and extends to the end of this sequence.

| Parameters ||
|---|---|
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The beginning index, inclusive. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | The new string. |

| Exceptions ||
|---|---|
| `java.lang.StringIndexOutOfBoundsException` | if `start` is less than zero, or greater than the length of this object. |

### substring

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun substring(
    start: Int, 
    end: Int
): String
```

Returns a new `String` that contains a subsequence of characters currently contained in this sequence. The substring begins at the specified `start` and extends to the character at index `end - 1`.

| Parameters ||
|---|---|
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The beginning index, inclusive. |
| `end` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The ending index, exclusive. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | The new string. |

| Exceptions ||
|---|---|
| `java.lang.StringIndexOutOfBoundsException` | if `start` or `end` are negative or greater than `length()`, or `start` is greater than `end`. |

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

Attempts to reduce storage used for the character sequence. If the buffer is larger than necessary to hold its current sequence of characters, then it may be resized to become more space efficient. Calling this method may, but is not required to, affect the value returned by a subsequent call to the `https://developer.android.com/reference/kotlin/java/lang/StringBuilder#capacity()` method.

## Properties

### length

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
val length: Int
```

Returns the length (character count).

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the length of the sequence of characters currently represented by this object |
