Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SpannedString

Kotlin | [Java](SpannedString.md)
| --- | --- |

```
class SpannedString : CharSequence, GetChars, Spanned
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.text.SpannedString](SpannedString.md) |

This is the class for text whose content and markup are immutable. For mutable markup, see `https://developer.android.com/reference/kotlin/android/text/SpannableString`; for mutable text, see `https://developer.android.com/reference/kotlin/android/text/SpannableStringBuilder`.

## Summary

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/text/Spanned` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/text/Spanned#SPAN_COMPOSING:kotlin.Int` This flag is set on spans that are being used to apply temporary styling information on the composing text of an input method, so that they can be found and removed when the composing text is being replaced. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/text/Spanned#SPAN_EXCLUSIVE_EXCLUSIVE:kotlin.Int` Spans of type SPAN_EXCLUSIVE_EXCLUSIVE do not expand to include text inserted at either their starting or ending point. They can never have a length of 0 and are automatically removed from the buffer if all the text they cover is removed. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/text/Spanned#SPAN_EXCLUSIVE_INCLUSIVE:kotlin.Int` Non-0-length spans of type SPAN_EXCLUSIVE_INCLUSIVE expand to include text inserted at their ending point but not at their starting point. When 0-length, they behave like points. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/text/Spanned#SPAN_INCLUSIVE_EXCLUSIVE:kotlin.Int` Non-0-length spans of type SPAN_INCLUSIVE_EXCLUSIVE expand to include text inserted at their starting point but not at their ending point. When 0-length, they behave like marks. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/text/Spanned#SPAN_INCLUSIVE_INCLUSIVE:kotlin.Int` Spans of type SPAN_INCLUSIVE_INCLUSIVE expand to include text inserted at either their starting or ending point. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/text/Spanned#SPAN_INTERMEDIATE:kotlin.Int` This flag will be set for intermediate span changes, meaning there is guaranteed to be another change following it. Typically it is used for `https://developer.android.com/reference/kotlin/android/text/Selection` which automatically uses this with the first offset it sets when updating the selection. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/text/Spanned#SPAN_MARK_MARK:kotlin.Int` 0-length spans with type SPAN_MARK_MARK behave like text marks: they remain at their original offset when text is inserted at that offset. Conceptually, the text is added after the mark. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/text/Spanned#SPAN_MARK_POINT:kotlin.Int` SPAN_MARK_POINT is a synonym for `https://developer.android.com/reference/kotlin/android/text/Spanned#SPAN_INCLUSIVE_INCLUSIVE:kotlin.Int`. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/text/Spanned#SPAN_PARAGRAPH:kotlin.Int` SPAN_PARAGRAPH behaves like SPAN_INCLUSIVE_EXCLUSIVE (SPAN_MARK_MARK), except that if either end of the span is at the end of the buffer, that end behaves like _POINT instead (so SPAN_INCLUSIVE_INCLUSIVE if it starts in the middle and ends at the end, or SPAN_EXCLUSIVE_INCLUSIVE if it both starts and ends at the end). Its endpoints must be the start or end of the buffer or immediately after a \\n character, and if the \\n that anchors it is deleted, the endpoint is pulled to the next \\n that follows in the buffer (or to the end of the buffer). If a span with SPAN_PARAGRAPH flag is pasted into another text and the paragraph boundary constraint is not satisfied, the span is discarded. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/text/Spanned#SPAN_POINT_MARK:kotlin.Int` SPAN_POINT_MARK is a synonym for `https://developer.android.com/reference/kotlin/android/text/Spanned#SPAN_EXCLUSIVE_EXCLUSIVE:kotlin.Int`. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/text/Spanned#SPAN_POINT_MARK_MASK:kotlin.Int` Bitmask of bits that are relevent for controlling point/mark behavior of spans. MARK and POINT are conceptually located *between* two adjacent characters. A MARK is "attached" to the character before, while a POINT will stick to the character after. The insertion cursor is conceptually located between the MARK and the POINT. As a result, inserting a new character between a MARK and a POINT will leave the MARK unchanged, while the POINT will be shifted, now located after the inserted character and still glued to the same character after it. Depending on whether the insertion happens at the beginning or the end of a span, the span will hence be expanded to *include* the new character (when the span is using a MARK at its beginning or a POINT at its end) or it will be *excluded* . Note that *before* and *after* here refer to offsets in the String, which are independent from the visual representation of the text (left-to-right or right-to-left). <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/text/Spanned#SPAN_POINT_POINT:kotlin.Int` 0-length spans with type SPAN_POINT_POINT behave like cursors: they are pushed forward by the length of the insertion when text is inserted at their offset. The text is conceptually inserted before the point. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/text/Spanned#SPAN_PRIORITY:kotlin.Int` The bits specified by the SPAN_PRIORITY bitmap determine the order of change notifications -- higher numbers go first. You probably don't need to set this; it is used so that when text changes, the text layout gets the chance to update itself before any other callbacks can inquire about the layout of the text. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/text/Spanned#SPAN_PRIORITY_SHIFT:kotlin.Int` The bits numbered just above SPAN_PRIORITY_SHIFT determine the order of change notifications -- higher numbers go first. You probably don't need to set this; it is used so that when text changes, the text layout gets the chance to update itself before any other callbacks can inquire about the layout of the text. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/text/Spanned#SPAN_USER:kotlin.Int` The bits specified by the SPAN_USER bitfield are available for callers to use to store scalar data associated with their span object. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/text/Spanned#SPAN_USER_SHIFT:kotlin.Int` The bits numbered SPAN_USER_SHIFT and above are available for callers to use to store scalar data associated with their span object. <br /> | ||

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/text/SpannedString#SpannedString(kotlin.CharSequence)(source: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!)` For the backward compatibility reasons, this constructor copies all spans including `https://developer.android.com/reference/kotlin/android/text/NoCopySpan`. |

| Public methods ||
|---|---|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/text/SpannedString#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Indicates whether some other object is "equal to" this one. |
| [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | `https://developer.android.com/reference/kotlin/android/text/SpannedString#get(kotlin.Int)(i: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/text/SpannedString#getChars(kotlin.Int,%20kotlin.Int,%20kotlin.CharArray,%20kotlin.Int)(start: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, end: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, dest: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html!, off: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` <br /> |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/text/SpannedString#getSpanEnd(kotlin.Any)(what: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!)` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/text/SpannedString#getSpanFlags(kotlin.Any)(what: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!)` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/text/SpannedString#getSpanStart(kotlin.Any)(what: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!)` <br /> |
| --- | --- |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\<T\>! | `https://developer.android.com/reference/kotlin/android/text/SpannedString#getSpans(kotlin.Int,%20kotlin.Int,%20java.lang.Class)(queryStart: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, queryEnd: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, kind: https://developer.android.com/reference/kotlin/java/lang/Class.html#<T>!)` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/text/SpannedString#hashCode()()` Returns a hash code value for the object. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/text/SpannedString#nextSpanTransition(kotlin.Int,%20kotlin.Int,%20java.lang.Class)(start: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, limit: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, kind: https://developer.android.com/reference/kotlin/java/lang/Class.html#<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!>!)` <br /> |
| --- | --- |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html) | `https://developer.android.com/reference/kotlin/android/text/SpannedString#subSequence(kotlin.Int,%20kotlin.Int)(startIndex: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, endIndex: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns a `CharSequence` that is a subsequence of this sequence. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/text/SpannedString#toString()()` Returns a string representation of the object. |
| static [SpannedString](SpannedString.md)! | `https://developer.android.com/reference/kotlin/android/text/SpannedString#valueOf(kotlin.CharSequence)(source: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!)` <br /> |
| --- | --- |

| Properties ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/text/SpannedString#length:kotlin.Int` <br /> |

## Public constructors

### SpannedString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
SpannedString(source: CharSequence!)
```

For the backward compatibility reasons, this constructor copies all spans including `https://developer.android.com/reference/kotlin/android/text/NoCopySpan`.

| Parameters ||
|---|---|
| `source` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!: source text |

## Public methods

### equals

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun equals(other: Any?): Boolean
```

Indicates whether some other object is "equal to" this one.

The `equals` method implements an equivalence relation on non-null object references:

- It is *reflexive* : for any non-null reference value `x`, `x.equals(x)` should return `true`.
- It is *symmetric* : for any non-null reference values `x` and `y`, `x.equals(y)` should return `true` if and only if `y.equals(x)` returns `true`.
- It is *transitive* : for any non-null reference values `x`, `y`, and `z`, if `x.equals(y)` returns `true` and `y.equals(z)` returns `true`, then `x.equals(z)` should return `true`.
- It is *consistent* : for any non-null reference values `x` and `y`, multiple invocations of `x.equals(y)` consistently return `true` or consistently return `false`, provided no information used in `equals` comparisons on the objects is modified.
- For any non-null reference value `x`, `x.equals(null)` should return `false`.

An equivalence relation partitions the elements it operates on into *equivalence classes*; all the members of an equivalence class are equal to each other. Members of an equivalence class are substitutable for each other, at least for some purposes.

| Parameters ||
|---|---|
| `obj` | the reference object with which to compare. |
| `o` | This value may be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this object is the same as the obj argument; `false` otherwise. |

### get

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun get(i: Int): Char
```

| Parameters ||
|---|---|
| `index` | the index of the `char` value to be returned |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html` | the specified `char` value |

| Exceptions ||
|---|---|
| `java.lang.IndexOutOfBoundsException` | if the `index` argument is negative or not less than `length()` |

### getChars

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getChars(
    start: Int, 
    end: Int, 
    dest: CharArray!, 
    off: Int
): Unit
```

### getSpanEnd

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getSpanEnd(what: Any!): Int
```

### getSpanFlags

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getSpanFlags(what: Any!): Int
```

### getSpanStart

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getSpanStart(what: Any!): Int
```

### getSpans

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun <T : Any!> getSpans(
    queryStart: Int, 
    queryEnd: Int, 
    kind: Class<T>!
): Array<T>!
```

### hashCode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hashCode(): Int
```

Returns a hash code value for the object. This method is supported for the benefit of hash tables such as those provided by `https://developer.android.com/reference/kotlin/java/util/HashMap.html#`.

The general contract of `hashCode` is:

- Whenever it is invoked on the same object more than once during an execution of a Java application, the `hashCode` method must consistently return the same integer, provided no information used in `equals` comparisons on the object is modified. This integer need not remain consistent from one execution of an application to another execution of the same application.
- If two objects are equal according to the `https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any)` method, then calling the `hashCode` method on each of the two objects must produce the same integer result.
- It is *not* required that if two objects are unequal according to the `https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any)` method, then calling the `hashCode` method on each of the two objects must produce distinct integer results. However, the programmer should be aware that producing distinct integer results for unequal objects may improve the performance of hash tables.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a hash code value for this object. |

### nextSpanTransition

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun nextSpanTransition(
    start: Int, 
    limit: Int, 
    kind: Class<Any!>!
): Int
```

### subSequence

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun subSequence(
    startIndex: Int, 
    endIndex: Int
): CharSequence
```

Returns a `CharSequence` that is a subsequence of this sequence. The subsequence starts with the `char` value at the specified index and ends with the `char` value at index `end - 1`. The length (in `char`s) of the returned sequence is `end - start`, so if `start == end` then an empty sequence is returned.

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

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toString(): String
```

Returns a string representation of the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string consisting of exactly this sequence of characters |

### valueOf

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun valueOf(source: CharSequence!): SpannedString!
```

## Properties

### length

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
val length: Int
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the number of `char`s in this sequence |
