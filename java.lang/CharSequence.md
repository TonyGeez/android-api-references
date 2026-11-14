Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CharSequence

```
interface CharSequence
```

| [java.lang.CharSequence](CharSequence.md) |

A `CharSequence` is a readable sequence of `char` values. This interface provides uniform, read-only access to many different kinds of `char` sequences. A `char` value represents a character in the *Basic Multilingual Plane (BMP)* or a surrogate. Refer to [Unicode Character Representation](Character.md) for details.

This interface does not refine the general contracts of the equals and hashCode methods. The result of testing two objects that implement `CharSequence` for equality is therefore, in general, undefined. Each object may be implemented by a different class, and there is no guarantee that each class will be capable of testing its instances for equality with those of the other. It is therefore inappropriate to use arbitrary `CharSequence` instances as elements in a set or as keys in a map.

## Summary

| Public methods ||
|---|---|
| abstract [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | charAt Returns the `char` value at the specified index. |
| open [IntStream](../java.util.stream/IntStream.md) | chars Returns a stream of `int` zero-extending the `char` values from this sequence. |
| open [IntStream](../java.util.stream/IntStream.md) | codePoints Returns a stream of code point values from this sequence. |
| --- | --- |
| open static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | compare Compares two `CharSequence` instances lexicographically. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | getChars Copies characters from this sequence into the given destination array. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isEmpty Returns `true` if this character sequence is empty. |
| --- | --- |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | length Returns the length of this character sequence. |
| abstract [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html) | subSequence Returns a `CharSequence` that is a subsequence of this sequence. |

## Public methods

### charAt

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun charAt(index: Int): Char
```

Returns the `char` value at the specified index. An index ranges from zero to `length() - 1`. The first `char` value of the sequence is at index zero, the next at index one, and so on, as for array indexing.

If the `char` value specified by the index is a [surrogate](https://developer.android.com//reference/java/lang/Character.html#unicode), the surrogate value is returned.

| Parameters ||
|---|---|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index of the `char` value to be returned |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html` | the specified `char` value |

| Exceptions ||
|---|---|
| `java.lang.IndexOutOfBoundsException` | if the `index` argument is negative or not less than `length()` |

### chars

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun chars(): IntStream
```

Returns a stream of `int` zero-extending the `char` values from this sequence. Any char which maps to a [surrogate code point](https://developer.android.com//reference/java/lang/Character.html#unicode) is passed through uninterpreted.

The stream binds to this sequence when the terminal stream operation commences (specifically, for mutable sequences the spliterator for the stream is [*late-binding*](../java.util/Spliterator.md)). If the sequence is modified during that operation then the result is undefined.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/stream/IntStream.html#` | an IntStream of char values from this sequence |

### codePoints

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun codePoints(): IntStream
```

Returns a stream of code point values from this sequence. Any surrogate pairs encountered in the sequence are combined as if by [Character.toCodePoint](Character.md)) and the result is passed to the stream. Any other code units, including ordinary BMP characters, unpaired surrogates, and undefined code units, are zero-extended to `int` values which are then passed to the stream.

The stream binds to this sequence when the terminal stream operation commences (specifically, for mutable sequences the spliterator for the stream is [*late-binding*](../java.util/Spliterator.md)). If the sequence is modified during that operation then the result is undefined.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/stream/IntStream.html#` | an IntStream of Unicode code points from this sequence |

### compare

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun compare(
    cs1: CharSequence, 
    cs2: CharSequence
): Int
```

Compares two `CharSequence` instances lexicographically. Returns a negative value, zero, or a positive value if the first sequence is lexicographically less than, equal to, or greater than the second, respectively.

The lexicographical ordering of `CharSequence` is defined as follows. Consider a `CharSequence` *cs* of length *len* to be a sequence of char values, *cs\[0\]* to *cs\[len-1\]* . Suppose *k* is the lowest index at which the corresponding char values from each sequence differ. The lexicographic ordering of the sequences is determined by a numeric comparison of the char values *cs1\[k\]* with *cs2\[k\]* . If there is no such index *k*, the shorter sequence is considered lexicographically less than the other. If the sequences have the same length, the sequences are considered lexicographically equal.

| Parameters ||
|---|---|
| `cs1` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html): the first `CharSequence` |
| `cs2` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html): the second `CharSequence` |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the value `0` if the two `CharSequence` are equal; a negative integer if the first `CharSequence` is lexicographically less than the second; or a positive integer if the first `CharSequence` is lexicographically greater than the second. |

### getChars

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getChars(
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

### isEmpty

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isEmpty(): Boolean
```

Returns `true` if this character sequence is empty.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if length is `0`, otherwise `false` |

### length

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun length(): Int
```

Returns the length of this character sequence. The length is the number of 16-bit `char`s in the sequence.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the number of `char`s in this sequence |

### subSequence

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun subSequence(
    start: Int, 
    end: Int
): CharSequence
```

Returns a `CharSequence` that is a subsequence of this sequence. The subsequence starts with the `char` value at the specified index and ends with the `char` value at index `end - 1`. The length (in `char`s) of the returned sequence is `end - start`, so if `start == end` then an empty sequence is returned.

| Parameters ||
|---|---|
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the start index, inclusive |
| `end` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the end index, exclusive |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html` | the specified subsequence |

| Exceptions ||
|---|---|
| `java.lang.IndexOutOfBoundsException` | if `start` or `end` are negative, if `end` is greater than `length()`, or if `start` is greater than `end` |
