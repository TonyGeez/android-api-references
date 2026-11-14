# Spanned

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Spanned

Kotlin| [Java](https://developer.android.com/reference/android/text/Spanned "View this page in Java") 
| --- | --- |

```
interface Spanned : CharSequence
```

| [android.text.Spanned](https://developer.android.com/reference/kotlin/android/text/Spanned#) |

| Known Direct Subclasses [Spannable](https://developer.android.com/reference/kotlin/android/text/Spannable), [SpannedString](https://developer.android.com/reference/kotlin/android/text/SpannedString) |--------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------| | [Spannable](https://developer.android.com/reference/kotlin/android/text/Spannable) | This is the interface for text to which markup objects can be attached and detached. | | [SpannedString](https://developer.android.com/reference/kotlin/android/text/SpannedString) | This is the class for text whose content and markup are immutable. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [Editable](https://developer.android.com/reference/kotlin/android/text/Editable), [PrecomputedText](https://developer.android.com/reference/kotlin/android/text/PrecomputedText), [SpannableString](https://developer.android.com/reference/kotlin/android/text/SpannableString), [SpannableStringBuilder](https://developer.android.com/reference/kotlin/android/text/SpannableStringBuilder) [SpannableStringBuilder](https://developer.android.com/reference/kotlin/android/text/SpannableStringBuilder) |--------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------| | [Editable](https://developer.android.com/reference/kotlin/android/text/Editable) | This is the interface for text whose content and markup can be changed (as opposed to immutable text like Strings). | | [PrecomputedText](https://developer.android.com/reference/kotlin/android/text/PrecomputedText) | A text which has the character metrics data. | | [SpannableString](https://developer.android.com/reference/kotlin/android/text/SpannableString) | This is the class for text whose content is immutable but to which markup objects can be attached and detached. | | [SpannableStringBuilder](https://developer.android.com/reference/kotlin/android/text/SpannableStringBuilder) | This is the class for text whose content and markup can both be changed. | | [SpannableStringBuilder](https://developer.android.com/reference/kotlin/android/text/SpannableStringBuilder) | This is the class for text whose content and markup can both be changed. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

This is the interface for text that has markup objects attached to ranges of it. Not all text classes have mutable markup or text; see [Spannable](https://developer.android.com/reference/kotlin/android/text/Spannable) for mutable markup and [Editable](https://developer.android.com/reference/kotlin/android/text/Editable) for mutable text.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SPAN_COMPOSING](https://developer.android.com/reference/kotlin/android/text/Spanned#SPAN_COMPOSING:kotlin.Int) This flag is set on spans that are being used to apply temporary styling information on the composing text of an input method, so that they can be found and removed when the composing text is being replaced. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SPAN_EXCLUSIVE_EXCLUSIVE](https://developer.android.com/reference/kotlin/android/text/Spanned#SPAN_EXCLUSIVE_EXCLUSIVE:kotlin.Int) Spans of type SPAN_EXCLUSIVE_EXCLUSIVE do not expand to include text inserted at either their starting or ending point. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SPAN_EXCLUSIVE_INCLUSIVE](https://developer.android.com/reference/kotlin/android/text/Spanned#SPAN_EXCLUSIVE_INCLUSIVE:kotlin.Int) Non-0-length spans of type SPAN_EXCLUSIVE_INCLUSIVE expand to include text inserted at their ending point but not at their starting point. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SPAN_INCLUSIVE_EXCLUSIVE](https://developer.android.com/reference/kotlin/android/text/Spanned#SPAN_INCLUSIVE_EXCLUSIVE:kotlin.Int) Non-0-length spans of type SPAN_INCLUSIVE_EXCLUSIVE expand to include text inserted at their starting point but not at their ending point. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SPAN_INCLUSIVE_INCLUSIVE](https://developer.android.com/reference/kotlin/android/text/Spanned#SPAN_INCLUSIVE_INCLUSIVE:kotlin.Int) Spans of type SPAN_INCLUSIVE_INCLUSIVE expand to include text inserted at either their starting or ending point. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SPAN_INTERMEDIATE](https://developer.android.com/reference/kotlin/android/text/Spanned#SPAN_INTERMEDIATE:kotlin.Int) This flag will be set for intermediate span changes, meaning there is guaranteed to be another change following it. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SPAN_MARK_MARK](https://developer.android.com/reference/kotlin/android/text/Spanned#SPAN_MARK_MARK:kotlin.Int) 0-length spans with type SPAN_MARK_MARK behave like text marks: they remain at their original offset when text is inserted at that offset. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SPAN_MARK_POINT](https://developer.android.com/reference/kotlin/android/text/Spanned#SPAN_MARK_POINT:kotlin.Int) SPAN_MARK_POINT is a synonym for [SPAN_INCLUSIVE_INCLUSIVE](https://developer.android.com/reference/kotlin/android/text/Spanned#SPAN_INCLUSIVE_INCLUSIVE:kotlin.Int). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SPAN_PARAGRAPH](https://developer.android.com/reference/kotlin/android/text/Spanned#SPAN_PARAGRAPH:kotlin.Int) SPAN_PARAGRAPH behaves like SPAN_INCLUSIVE_EXCLUSIVE (SPAN_MARK_MARK), except that if either end of the span is at the end of the buffer, that end behaves like _POINT instead (so SPAN_INCLUSIVE_INCLUSIVE if it starts in the middle and ends at the end, or SPAN_EXCLUSIVE_INCLUSIVE if it both starts and ends at the end). |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SPAN_POINT_MARK](https://developer.android.com/reference/kotlin/android/text/Spanned#SPAN_POINT_MARK:kotlin.Int) SPAN_POINT_MARK is a synonym for [SPAN_EXCLUSIVE_EXCLUSIVE](https://developer.android.com/reference/kotlin/android/text/Spanned#SPAN_EXCLUSIVE_EXCLUSIVE:kotlin.Int). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SPAN_POINT_MARK_MASK](https://developer.android.com/reference/kotlin/android/text/Spanned#SPAN_POINT_MARK_MASK:kotlin.Int) Bitmask of bits that are relevent for controlling point/mark behavior of spans. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SPAN_POINT_POINT](https://developer.android.com/reference/kotlin/android/text/Spanned#SPAN_POINT_POINT:kotlin.Int) 0-length spans with type SPAN_POINT_POINT behave like cursors: they are pushed forward by the length of the insertion when text is inserted at their offset. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SPAN_PRIORITY](https://developer.android.com/reference/kotlin/android/text/Spanned#SPAN_PRIORITY:kotlin.Int) The bits specified by the SPAN_PRIORITY bitmap determine the order of change notifications -- higher numbers go first. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SPAN_PRIORITY_SHIFT](https://developer.android.com/reference/kotlin/android/text/Spanned#SPAN_PRIORITY_SHIFT:kotlin.Int) The bits numbered just above SPAN_PRIORITY_SHIFT determine the order of change notifications -- higher numbers go first. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SPAN_USER](https://developer.android.com/reference/kotlin/android/text/Spanned#SPAN_USER:kotlin.Int) The bits specified by the SPAN_USER bitfield are available for callers to use to store scalar data associated with their span object. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SPAN_USER_SHIFT](https://developer.android.com/reference/kotlin/android/text/Spanned#SPAN_USER_SHIFT:kotlin.Int) The bits numbered SPAN_USER_SHIFT and above are available for callers to use to store scalar data associated with their span object. |

| Public methods ||
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSpanEnd](https://developer.android.com/reference/kotlin/android/text/Spanned#getSpanEnd(kotlin.Any))`(`tag:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Return the end of the range of text to which the specified markup object is attached, or -1 if the object is not attached. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSpanFlags](https://developer.android.com/reference/kotlin/android/text/Spanned#getSpanFlags(kotlin.Any))`(`tag:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Return the flags that were specified when [Spannable.setSpan](https://developer.android.com/reference/kotlin/android/text/Spannable#setSpan(kotlin.Any,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int))was used to attach the specified markup object, or 0 if the specified object has not been attached. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSpanStart](https://developer.android.com/reference/kotlin/android/text/Spanned#getSpanStart(kotlin.Any))`(`tag:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Return the beginning of the range of text to which the specified markup object is attached, or -1 if the object is not attached. |
| --- | --- |
| abstract [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\<T\>! | [getSpans](https://developer.android.com/reference/kotlin/android/text/Spanned#getSpans(kotlin.Int,%20kotlin.Int,%20java.lang.Class))`(`start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `end:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `type:` ` [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)<T>!`)` Return an array of the markup objects attached to the specified slice of this CharSequence and whose type is the specified type or a subclass of it. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [nextSpanTransition](https://developer.android.com/reference/kotlin/android/text/Spanned#nextSpanTransition(kotlin.Int,%20kotlin.Int,%20java.lang.Class))`(`start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `limit:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `type:` ` [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!>!`)` Return the first offset greater than`start`where a markup object of class`type`begins or ends, or`limit`if there are no starts or ends greater than`start`but less than`limit`. |

## Constants

### SPAN_COMPOSING

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SPAN_COMPOSING: Int
```

This flag is set on spans that are being used to apply temporary styling information on the composing text of an input method, so that they can be found and removed when the composing text is being replaced. 

 Value: 256

### SPAN_EXCLUSIVE_EXCLUSIVE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SPAN_EXCLUSIVE_EXCLUSIVE: Int
```

Spans of type SPAN_EXCLUSIVE_EXCLUSIVE do not expand to include text inserted at either their starting or ending point. They can never have a length of 0 and are automatically removed from the buffer if all the text they cover is removed. 

 Value: 33

### SPAN_EXCLUSIVE_INCLUSIVE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SPAN_EXCLUSIVE_INCLUSIVE: Int
```

Non-0-length spans of type SPAN_EXCLUSIVE_INCLUSIVE expand to include text inserted at their ending point but not at their starting point. When 0-length, they behave like points. 

 Value: 34

### SPAN_INCLUSIVE_EXCLUSIVE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SPAN_INCLUSIVE_EXCLUSIVE: Int
```

Non-0-length spans of type SPAN_INCLUSIVE_EXCLUSIVE expand to include text inserted at their starting point but not at their ending point. When 0-length, they behave like marks. 

 Value: 17

### SPAN_INCLUSIVE_INCLUSIVE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SPAN_INCLUSIVE_INCLUSIVE: Int
```

Spans of type SPAN_INCLUSIVE_INCLUSIVE expand to include text inserted at either their starting or ending point. 

 Value: 18

### SPAN_INTERMEDIATE

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SPAN_INTERMEDIATE: Int
```

This flag will be set for intermediate span changes, meaning there is guaranteed to be another change following it. Typically it is used for [Selection](https://developer.android.com/reference/kotlin/android/text/Selection) which automatically uses this with the first offset it sets when updating the selection. 

 Value: 512

### SPAN_MARK_MARK

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SPAN_MARK_MARK: Int
```

0-length spans with type SPAN_MARK_MARK behave like text marks: they remain at their original offset when text is inserted at that offset. Conceptually, the text is added after the mark. 

 Value: 17

### SPAN_MARK_POINT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SPAN_MARK_POINT: Int
```

SPAN_MARK_POINT is a synonym for [SPAN_INCLUSIVE_INCLUSIVE](https://developer.android.com/reference/kotlin/android/text/Spanned#SPAN_INCLUSIVE_INCLUSIVE:kotlin.Int). 

 Value: 18

### SPAN_PARAGRAPH

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SPAN_PARAGRAPH: Int
```

SPAN_PARAGRAPH behaves like SPAN_INCLUSIVE_EXCLUSIVE (SPAN_MARK_MARK), except that if either end of the span is at the end of the buffer, that end behaves like _POINT instead (so SPAN_INCLUSIVE_INCLUSIVE if it starts in the middle and ends at the end, or SPAN_EXCLUSIVE_INCLUSIVE if it both starts and ends at the end).

Its endpoints must be the start or end of the buffer or immediately after a \\n character, and if the \\n that anchors it is deleted, the endpoint is pulled to the next \\n that follows in the buffer (or to the end of the buffer). If a span with SPAN_PARAGRAPH flag is pasted into another text and the paragraph boundary constraint is not satisfied, the span is discarded. 

 Value: 51

### SPAN_POINT_MARK

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SPAN_POINT_MARK: Int
```

SPAN_POINT_MARK is a synonym for [SPAN_EXCLUSIVE_EXCLUSIVE](https://developer.android.com/reference/kotlin/android/text/Spanned#SPAN_EXCLUSIVE_EXCLUSIVE:kotlin.Int). 

 Value: 33

### SPAN_POINT_MARK_MASK

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SPAN_POINT_MARK_MASK: Int
```

Bitmask of bits that are relevent for controlling point/mark behavior of spans. MARK and POINT are conceptually located*between* two adjacent characters. A MARK is "attached" to the character before, while a POINT will stick to the character after. The insertion cursor is conceptually located between the MARK and the POINT. As a result, inserting a new character between a MARK and a POINT will leave the MARK unchanged, while the POINT will be shifted, now located after the inserted character and still glued to the same character after it. Depending on whether the insertion happens at the beginning or the end of a span, the span will hence be expanded to*include* the new character (when the span is using a MARK at its beginning or a POINT at its end) or it will be*excluded* . Note that*before* and*after*here refer to offsets in the String, which are independent from the visual representation of the text (left-to-right or right-to-left). 

 Value: 51

### SPAN_POINT_POINT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SPAN_POINT_POINT: Int
```

0-length spans with type SPAN_POINT_POINT behave like cursors: they are pushed forward by the length of the insertion when text is inserted at their offset. The text is conceptually inserted before the point. 

 Value: 34

### SPAN_PRIORITY

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SPAN_PRIORITY: Int
```

The bits specified by the SPAN_PRIORITY bitmap determine the order of change notifications -- higher numbers go first. You probably don't need to set this; it is used so that when text changes, the text layout gets the chance to update itself before any other callbacks can inquire about the layout of the text. 

 Value: 16711680

### SPAN_PRIORITY_SHIFT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SPAN_PRIORITY_SHIFT: Int
```

The bits numbered just above SPAN_PRIORITY_SHIFT determine the order of change notifications -- higher numbers go first. You probably don't need to set this; it is used so that when text changes, the text layout gets the chance to update itself before any other callbacks can inquire about the layout of the text. 

 Value: 16

### SPAN_USER

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SPAN_USER: Int
```

The bits specified by the SPAN_USER bitfield are available for callers to use to store scalar data associated with their span object. 

 Value: -16777216

### SPAN_USER_SHIFT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SPAN_USER_SHIFT: Int
```

The bits numbered SPAN_USER_SHIFT and above are available for callers to use to store scalar data associated with their span object. 

 Value: 24

## Public methods

### getSpanEnd

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getSpanEnd(tag: Any!): Int
```

Return the end of the range of text to which the specified markup object is attached, or -1 if the object is not attached. 

### getSpanFlags

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getSpanFlags(tag: Any!): Int
```

Return the flags that were specified when [Spannable.setSpan](https://developer.android.com/reference/kotlin/android/text/Spannable#setSpan(kotlin.Any,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int))was used to attach the specified markup object, or 0 if the specified object has not been attached. 

### getSpanStart

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getSpanStart(tag: Any!): Int
```

Return the beginning of the range of text to which the specified markup object is attached, or -1 if the object is not attached. 

### getSpans

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun <T : Any!> getSpans(
    start: Int, 
    end: Int, 
    type: Class<T>!
): Array<T>!
```

Return an array of the markup objects attached to the specified slice of this CharSequence and whose type is the specified type or a subclass of it. Specify Object.class for the type if you want all the objects regardless of type. 

### nextSpanTransition

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun nextSpanTransition(
    start: Int, 
    limit: Int, 
    type: Class<Any!>!
): Int
```

Return the first offset greater than`start`where a markup object of class`type`begins or ends, or`limit`if there are no starts or ends greater than`start`but less than`limit`. Specify`null`or Object.class for the type if you want every transition regardless of type.
