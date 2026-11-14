# Editable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Editable

Kotlin| [Java](https://developer.android.com/reference/android/text/Editable "View this page in Java") 

```
interface Editable : Appendable, CharSequence, GetChars, Spannable
```

| [android.text.Editable](https://developer.android.com/reference/kotlin/android/text/Editable#) |

| Known Direct Subclasses [SpannableStringBuilder](https://developer.android.com/reference/kotlin/android/text/SpannableStringBuilder) |--------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------| | [SpannableStringBuilder](https://developer.android.com/reference/kotlin/android/text/SpannableStringBuilder) | This is the class for text whose content and markup can both be changed. | |

This is the interface for text whose content and markup can be changed (as opposed to immutable text like Strings). If you make a [DynamicLayout](https://developer.android.com/reference/kotlin/android/text/DynamicLayout) of an Editable, the layout will be reflowed as the text is changed.

## Summary

| Nested classes ||
|------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open | [Factory](https://developer.android.com/reference/kotlin/android/text/Editable.Factory) Factory used by TextView to create new [Editables](https://developer.android.com/reference/kotlin/android/text/Editable#). |

| Inherited constants ||
|---|---|
| From class [Spanned](https://developer.android.com/reference/kotlin/android/text/Spanned) |----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SPAN_COMPOSING](https://developer.android.com/reference/kotlin/android/text/Spanned#SPAN_COMPOSING:kotlin.Int) <br /> This flag is set on spans that are being used to apply temporary styling information on the composing text of an input method, so that they can be found and removed when the composing text is being replaced. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SPAN_EXCLUSIVE_EXCLUSIVE](https://developer.android.com/reference/kotlin/android/text/Spanned#SPAN_EXCLUSIVE_EXCLUSIVE:kotlin.Int) <br /> Spans of type SPAN_EXCLUSIVE_EXCLUSIVE do not expand to include text inserted at either their starting or ending point. They can never have a length of 0 and are automatically removed from the buffer if all the text they cover is removed. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SPAN_EXCLUSIVE_INCLUSIVE](https://developer.android.com/reference/kotlin/android/text/Spanned#SPAN_EXCLUSIVE_INCLUSIVE:kotlin.Int) <br /> Non-0-length spans of type SPAN_EXCLUSIVE_INCLUSIVE expand to include text inserted at their ending point but not at their starting point. When 0-length, they behave like points. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SPAN_INCLUSIVE_EXCLUSIVE](https://developer.android.com/reference/kotlin/android/text/Spanned#SPAN_INCLUSIVE_EXCLUSIVE:kotlin.Int) <br /> Non-0-length spans of type SPAN_INCLUSIVE_EXCLUSIVE expand to include text inserted at their starting point but not at their ending point. When 0-length, they behave like marks. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SPAN_INCLUSIVE_INCLUSIVE](https://developer.android.com/reference/kotlin/android/text/Spanned#SPAN_INCLUSIVE_INCLUSIVE:kotlin.Int) <br /> Spans of type SPAN_INCLUSIVE_INCLUSIVE expand to include text inserted at either their starting or ending point. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SPAN_INTERMEDIATE](https://developer.android.com/reference/kotlin/android/text/Spanned#SPAN_INTERMEDIATE:kotlin.Int) <br /> This flag will be set for intermediate span changes, meaning there is guaranteed to be another change following it. Typically it is used for [Selection](https://developer.android.com/reference/kotlin/android/text/Selection) which automatically uses this with the first offset it sets when updating the selection. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SPAN_MARK_MARK](https://developer.android.com/reference/kotlin/android/text/Spanned#SPAN_MARK_MARK:kotlin.Int) <br /> 0-length spans with type SPAN_MARK_MARK behave like text marks: they remain at their original offset when text is inserted at that offset. Conceptually, the text is added after the mark. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SPAN_MARK_POINT](https://developer.android.com/reference/kotlin/android/text/Spanned#SPAN_MARK_POINT:kotlin.Int) <br /> SPAN_MARK_POINT is a synonym for [SPAN_INCLUSIVE_INCLUSIVE](https://developer.android.com/reference/kotlin/android/text/Spanned#SPAN_INCLUSIVE_INCLUSIVE:kotlin.Int). <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SPAN_PARAGRAPH](https://developer.android.com/reference/kotlin/android/text/Spanned#SPAN_PARAGRAPH:kotlin.Int) <br /> SPAN_PARAGRAPH behaves like SPAN_INCLUSIVE_EXCLUSIVE (SPAN_MARK_MARK), except that if either end of the span is at the end of the buffer, that end behaves like _POINT instead (so SPAN_INCLUSIVE_INCLUSIVE if it starts in the middle and ends at the end, or SPAN_EXCLUSIVE_INCLUSIVE if it both starts and ends at the end). Its endpoints must be the start or end of the buffer or immediately after a \\n character, and if the \\n that anchors it is deleted, the endpoint is pulled to the next \\n that follows in the buffer (or to the end of the buffer). If a span with SPAN_PARAGRAPH flag is pasted into another text and the paragraph boundary constraint is not satisfied, the span is discarded. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SPAN_POINT_MARK](https://developer.android.com/reference/kotlin/android/text/Spanned#SPAN_POINT_MARK:kotlin.Int) <br /> SPAN_POINT_MARK is a synonym for [SPAN_EXCLUSIVE_EXCLUSIVE](https://developer.android.com/reference/kotlin/android/text/Spanned#SPAN_EXCLUSIVE_EXCLUSIVE:kotlin.Int). <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SPAN_POINT_MARK_MASK](https://developer.android.com/reference/kotlin/android/text/Spanned#SPAN_POINT_MARK_MASK:kotlin.Int) <br /> Bitmask of bits that are relevent for controlling point/mark behavior of spans. MARK and POINT are conceptually located*between* two adjacent characters. A MARK is "attached" to the character before, while a POINT will stick to the character after. The insertion cursor is conceptually located between the MARK and the POINT. As a result, inserting a new character between a MARK and a POINT will leave the MARK unchanged, while the POINT will be shifted, now located after the inserted character and still glued to the same character after it. Depending on whether the insertion happens at the beginning or the end of a span, the span will hence be expanded to*include* the new character (when the span is using a MARK at its beginning or a POINT at its end) or it will be*excluded* . Note that*before* and*after*here refer to offsets in the String, which are independent from the visual representation of the text (left-to-right or right-to-left). <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SPAN_POINT_POINT](https://developer.android.com/reference/kotlin/android/text/Spanned#SPAN_POINT_POINT:kotlin.Int) <br /> 0-length spans with type SPAN_POINT_POINT behave like cursors: they are pushed forward by the length of the insertion when text is inserted at their offset. The text is conceptually inserted before the point. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SPAN_PRIORITY](https://developer.android.com/reference/kotlin/android/text/Spanned#SPAN_PRIORITY:kotlin.Int) <br /> The bits specified by the SPAN_PRIORITY bitmap determine the order of change notifications -- higher numbers go first. You probably don't need to set this; it is used so that when text changes, the text layout gets the chance to update itself before any other callbacks can inquire about the layout of the text. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SPAN_PRIORITY_SHIFT](https://developer.android.com/reference/kotlin/android/text/Spanned#SPAN_PRIORITY_SHIFT:kotlin.Int) <br /> The bits numbered just above SPAN_PRIORITY_SHIFT determine the order of change notifications -- higher numbers go first. You probably don't need to set this; it is used so that when text changes, the text layout gets the chance to update itself before any other callbacks can inquire about the layout of the text. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SPAN_USER](https://developer.android.com/reference/kotlin/android/text/Spanned#SPAN_USER:kotlin.Int) <br /> The bits specified by the SPAN_USER bitfield are available for callers to use to store scalar data associated with their span object. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SPAN_USER_SHIFT](https://developer.android.com/reference/kotlin/android/text/Spanned#SPAN_USER_SHIFT:kotlin.Int) <br /> The bits numbered SPAN_USER_SHIFT and above are available for callers to use to store scalar data associated with their span object. <br /> | ||

| Public methods ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Editable](https://developer.android.com/reference/kotlin/android/text/Editable#) | [append](https://developer.android.com/reference/kotlin/android/text/Editable#append(kotlin.Char))`(`text:` ` [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)`)` Convenience for append(String.valueOf(text)). |
| abstract [Editable](https://developer.android.com/reference/kotlin/android/text/Editable#) | [append](https://developer.android.com/reference/kotlin/android/text/Editable#append(kotlin.CharSequence))`(`text:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)?`)` Convenience for replace(length(), length(), text, 0, text. |
| abstract [Editable](https://developer.android.com/reference/kotlin/android/text/Editable#) | [append](https://developer.android.com/reference/kotlin/android/text/Editable#append(kotlin.CharSequence,%20kotlin.Int,%20kotlin.Int))`(`text:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)?`, `start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `end:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Convenience for replace(length(), length(), text, start, end) |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clear](https://developer.android.com/reference/kotlin/android/text/Editable#clear())`()` Convenience for replace(0, length(), "", 0, 0). |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clearSpans](https://developer.android.com/reference/kotlin/android/text/Editable#clearSpans())`()` Removes all spans from the Editable, as if by calling [removeSpan](https://developer.android.com/reference/kotlin/android/text/Spannable#removeSpan(kotlin.Any))on each of them. |
| abstract [Editable](https://developer.android.com/reference/kotlin/android/text/Editable#)! | [delete](https://developer.android.com/reference/kotlin/android/text/Editable#delete(kotlin.Int,%20kotlin.Int))`(`st:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `en:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Convenience for replace(st, en, "", 0, 0) |
| abstract [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [InputFilter](https://developer.android.com/reference/kotlin/android/text/InputFilter)!\>! | [getFilters](https://developer.android.com/reference/kotlin/android/text/Editable#getFilters())`()` Returns the array of input filters that are currently applied to changes to this Editable. |
| abstract [Editable](https://developer.android.com/reference/kotlin/android/text/Editable#)! | [insert](https://developer.android.com/reference/kotlin/android/text/Editable#insert(kotlin.Int,%20kotlin.CharSequence))`(`where:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `text:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` Convenience for replace(where, where, text, 0, text.length()); |
| abstract [Editable](https://developer.android.com/reference/kotlin/android/text/Editable#)! | [insert](https://developer.android.com/reference/kotlin/android/text/Editable#insert(kotlin.Int,%20kotlin.CharSequence,%20kotlin.Int,%20kotlin.Int))`(`where:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `text:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `end:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Convenience for replace(where, where, text, start, end) |
| abstract [Editable](https://developer.android.com/reference/kotlin/android/text/Editable#)! | [replace](https://developer.android.com/reference/kotlin/android/text/Editable#replace(kotlin.Int,%20kotlin.Int,%20kotlin.CharSequence))`(`st:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `en:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `text:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` Convenience for replace(st, en, text, 0, text.length()) |
| abstract [Editable](https://developer.android.com/reference/kotlin/android/text/Editable#)! | [replace](https://developer.android.com/reference/kotlin/android/text/Editable#replace(kotlin.Int,%20kotlin.Int,%20kotlin.CharSequence,%20kotlin.Int,%20kotlin.Int))`(`st:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `en:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `source:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `end:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Replaces the specified range (`st...en`) of text in this Editable with a copy of the slice`start...end`from`source`. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFilters](https://developer.android.com/reference/kotlin/android/text/Editable#setFilters(kotlin.Array))`(`filters:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [InputFilter](https://developer.android.com/reference/kotlin/android/text/InputFilter)!>!`)` Sets the series of filters that will be called in succession whenever the text of this Editable is changed, each of which has the opportunity to limit or transform the text that is being inserted. |

| Inherited functions ||
|---|---|
| From class [GetChars](https://developer.android.com/reference/kotlin/android/text/GetChars) |------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [getChars](https://developer.android.com/reference/kotlin/android/text/GetChars#getChars(kotlin.Int,%20kotlin.Int,%20kotlin.CharArray,%20kotlin.Int))`(`start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `end:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `dest:` ` [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!`, `destoff:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Exactly like String.getChars(): copy chars`start`through`end - 1`from this CharSequence into`dest`beginning at offset`destoff`. <br /> | ||
| From class [Spanned](https://developer.android.com/reference/kotlin/android/text/Spanned) |------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSpanEnd](https://developer.android.com/reference/kotlin/android/text/Spanned#getSpanEnd(kotlin.Any))`(`tag:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` <br /> Return the end of the range of text to which the specified markup object is attached, or -1 if the object is not attached. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSpanFlags](https://developer.android.com/reference/kotlin/android/text/Spanned#getSpanFlags(kotlin.Any))`(`tag:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` <br /> Return the flags that were specified when [Spannable.setSpan](https://developer.android.com/reference/kotlin/android/text/Spannable#setSpan(kotlin.Any,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int))was used to attach the specified markup object, or 0 if the specified object has not been attached. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSpanStart](https://developer.android.com/reference/kotlin/android/text/Spanned#getSpanStart(kotlin.Any))`(`tag:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` <br /> Return the beginning of the range of text to which the specified markup object is attached, or -1 if the object is not attached. <br /> | | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)<T>! | [getSpans](https://developer.android.com/reference/kotlin/android/text/Spanned#getSpans(kotlin.Int,%20kotlin.Int,%20java.lang.Class))`(`start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `end:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `type:` ` [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)<T>!`)` <br /> Return an array of the markup objects attached to the specified slice of this CharSequence and whose type is the specified type or a subclass of it. Specify Object.class for the type if you want all the objects regardless of type. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [nextSpanTransition](https://developer.android.com/reference/kotlin/android/text/Spanned#nextSpanTransition(kotlin.Int,%20kotlin.Int,%20java.lang.Class))`(`start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `limit:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `type:` ` [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!>!`)` <br /> Return the first offset greater than`start`where a markup object of class`type`begins or ends, or`limit`if there are no starts or ends greater than`start`but less than`limit`. Specify`null`or Object.class for the type if you want every transition regardless of type. <br /> | ||
| From class [Spannable](https://developer.android.com/reference/kotlin/android/text/Spannable) |------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeSpan](https://developer.android.com/reference/kotlin/android/text/Spannable#removeSpan(kotlin.Any))`(`what:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` <br /> Remove the specified object from the range of text to which it was attached, if any. It is OK to remove an object that was never attached in the first place. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSpan](https://developer.android.com/reference/kotlin/android/text/Spannable#setSpan(kotlin.Any,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`what:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`, `start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `end:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Attach the specified markup object to the range`start...end`of the text, or move the object to that range if it was already attached elsewhere. See [Spanned](https://developer.android.com/reference/kotlin/android/text/Spanned) for an explanation of what the flags mean. The object can be one that has meaning only within your application, or it can be one that the text system will use to affect text display or behavior. Some noteworthy ones are the subclasses of [android.text.style.CharacterStyle](https://developer.android.com/reference/kotlin/android/text/style/CharacterStyle) and [android.text.style.ParagraphStyle](https://developer.android.com/reference/kotlin/android/text/style/ParagraphStyle), and [android.text.TextWatcher](https://developer.android.com/reference/kotlin/android/text/TextWatcher) and [android.text.SpanWatcher](https://developer.android.com/reference/kotlin/android/text/SpanWatcher). <br /> | ||

## Public methods

### append

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun append(text: Char): Editable
```

Convenience for append(String.valueOf(text)).

| Parameters ||
|-----|-------------------------|
| `c` | The character to append |

| Return ||
|-----------------------------------------------------------------------------------|---------------------------------|
| [Editable](https://developer.android.com/reference/kotlin/android/text/Editable#) | A reference to this`Appendable` |

| Exceptions ||
|-----------------------|------------------------|
| `java.io.IOException` | If an I/O error occurs |

**See Also**

- [#replace(int, int, CharSequence, int, int)](https://developer.android.com/reference/kotlin/android/text/Editable#replace(kotlin.Int,%20kotlin.Int,%20kotlin.CharSequence,%20kotlin.Int,%20kotlin.Int)) 

### append

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun append(text: CharSequence?): Editable
```

Convenience for replace(length(), length(), text, 0, text.length())

| Parameters ||
|-------|---------------------------------------------------------------------------------------------------------------------|
| `csq` | The character sequence to append. If`csq`is`null`, then the four characters`"null"`are appended to this Appendable. |

| Return ||
|-----------------------------------------------------------------------------------|---------------------------------|
| [Editable](https://developer.android.com/reference/kotlin/android/text/Editable#) | A reference to this`Appendable` |

| Exceptions ||
|-----------------------|------------------------|
| `java.io.IOException` | If an I/O error occurs |

**See Also**

- [#replace(int, int, CharSequence, int, int)](https://developer.android.com/reference/kotlin/android/text/Editable#replace(kotlin.Int,%20kotlin.Int,%20kotlin.CharSequence,%20kotlin.Int,%20kotlin.Int)) 

### append

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun append(
    text: CharSequence?, 
    start: Int, 
    end: Int
): Editable
```

Convenience for replace(length(), length(), text, start, end)

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `csq` | The character sequence from which a subsequence will be appended. If`csq`is`null`, then characters will be appended as if`csq`contained the four characters`"null"`. |
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The index of the first character in the subsequence |
| `end` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The index of the character following the last character in the subsequence |

| Return ||
|-----------------------------------------------------------------------------------|---------------------------------|
| [Editable](https://developer.android.com/reference/kotlin/android/text/Editable#) | A reference to this`Appendable` |

| Exceptions ||
|---------------------------------------|------------------------------------------------------------------------------------------------|
| `java.lang.IndexOutOfBoundsException` | If`start`or`end`are negative,`start`is greater than`end`, or`end`is greater than`csq.length()` |
| `java.io.IOException` | If an I/O error occurs |

**See Also**

- [#replace(int, int, CharSequence, int, int)](https://developer.android.com/reference/kotlin/android/text/Editable#replace(kotlin.Int,%20kotlin.Int,%20kotlin.CharSequence,%20kotlin.Int,%20kotlin.Int)) 

### clear

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun clear(): Unit
```

Convenience for replace(0, length(), "", 0, 0). Note that this clears the text, not the spans; use [clearSpans](https://developer.android.com/reference/kotlin/android/text/Editable#clearSpans())if you need that. 
**See Also**

- [#replace(int, int, CharSequence, int, int)](https://developer.android.com/reference/kotlin/android/text/Editable#replace(kotlin.Int,%20kotlin.Int,%20kotlin.CharSequence,%20kotlin.Int,%20kotlin.Int)) 

### clearSpans

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun clearSpans(): Unit
```

Removes all spans from the Editable, as if by calling [removeSpan](https://developer.android.com/reference/kotlin/android/text/Spannable#removeSpan(kotlin.Any))on each of them. 

### delete

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun delete(
    st: Int, 
    en: Int
): Editable!
```

Convenience for replace(st, en, "", 0, 0) 
**See Also**

- [#replace(int, int, CharSequence, int, int)](https://developer.android.com/reference/kotlin/android/text/Editable#replace(kotlin.Int,%20kotlin.Int,%20kotlin.CharSequence,%20kotlin.Int,%20kotlin.Int)) 

### getFilters

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getFilters(): Array<InputFilter!>!
```

Returns the array of input filters that are currently applied to changes to this Editable. 

### insert

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun insert(
    where: Int, 
    text: CharSequence!
): Editable!
```

Convenience for replace(where, where, text, 0, text.length()); 
**See Also**

- [#replace(int, int, CharSequence, int, int)](https://developer.android.com/reference/kotlin/android/text/Editable#replace(kotlin.Int,%20kotlin.Int,%20kotlin.CharSequence,%20kotlin.Int,%20kotlin.Int)) 

### insert

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun insert(
    where: Int, 
    text: CharSequence!, 
    start: Int, 
    end: Int
): Editable!
```

Convenience for replace(where, where, text, start, end) 
**See Also**

- [#replace(int, int, CharSequence, int, int)](https://developer.android.com/reference/kotlin/android/text/Editable#replace(kotlin.Int,%20kotlin.Int,%20kotlin.CharSequence,%20kotlin.Int,%20kotlin.Int)) 

### replace

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun replace(
    st: Int, 
    en: Int, 
    text: CharSequence!
): Editable!
```

Convenience for replace(st, en, text, 0, text.length()) 
**See Also**

- [#replace(int, int, CharSequence, int, int)](https://developer.android.com/reference/kotlin/android/text/Editable#replace(kotlin.Int,%20kotlin.Int,%20kotlin.CharSequence,%20kotlin.Int,%20kotlin.Int)) 

### replace

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun replace(
    st: Int, 
    en: Int, 
    source: CharSequence!, 
    start: Int, 
    end: Int
): Editable!
```

Replaces the specified range (`st...en`) of text in this Editable with a copy of the slice`start...end`from`source`. The destination slice may be empty, in which case the operation is an insertion, or the source slice may be empty, in which case the operation is a deletion.

Before the change is committed, each filter that was set with [setFilters](https://developer.android.com/reference/kotlin/android/text/Editable#setFilters(kotlin.Array))is given the opportunity to modify the`source`text.

If`source`is Spanned, the spans from it are preserved into the Editable. Existing spans within the Editable that entirely cover the replaced range are retained, but any that were strictly within the range that was replaced are removed. If the`source`contains a span with [Spanned.SPAN_PARAGRAPH](https://developer.android.com/reference/kotlin/android/text/Spanned#SPAN_PARAGRAPH:kotlin.Int) flag, and it does not satisfy the paragraph boundary constraint, it is not retained. As a special case, the cursor position is preserved even when the entire range where it is located is replaced.

| Return ||
|------------------------------------------------------------------------------------|-----------------------------|
| [Editable](https://developer.android.com/reference/kotlin/android/text/Editable#)! | a reference to this object. |

**See Also**

- [android.text.Spanned#SPAN_PARAGRAPH](https://developer.android.com/reference/kotlin/android/text/Spanned#SPAN_PARAGRAPH:kotlin.Int) 

### setFilters

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setFilters(filters: Array<InputFilter!>!): Unit
```

Sets the series of filters that will be called in succession whenever the text of this Editable is changed, each of which has the opportunity to limit or transform the text that is being inserted.
