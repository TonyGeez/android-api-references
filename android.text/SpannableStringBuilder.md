# SpannableStringBuilder

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SpannableStringBuilder

Kotlin| [Java](https://developer.android.com/reference/android/text/SpannableStringBuilder "View this page in Java") 

```
open class SpannableStringBuilder : Appendable, CharSequence, Editable, GetChars, Spannable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.text.SpannableStringBuilder](https://developer.android.com/reference/kotlin/android/text/SpannableStringBuilder#) |

This is the class for text whose content and markup can both be changed.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SpannableStringBuilder](https://developer.android.com/reference/kotlin/android/text/SpannableStringBuilder#SpannableStringBuilder())`()` Create a new SpannableStringBuilder with empty contents |
| [SpannableStringBuilder](https://developer.android.com/reference/kotlin/android/text/SpannableStringBuilder#SpannableStringBuilder(kotlin.CharSequence))`(`text:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` Create a new SpannableStringBuilder containing a copy of the specified text, including its spans if any. |
| [SpannableStringBuilder](https://developer.android.com/reference/kotlin/android/text/SpannableStringBuilder#SpannableStringBuilder(kotlin.CharSequence,%20kotlin.Int,%20kotlin.Int))`(`text:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `end:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Create a new SpannableStringBuilder containing a copy of the specified slice of the specified text, including its spans if any. |

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [SpannableStringBuilder](https://developer.android.com/reference/kotlin/android/text/SpannableStringBuilder#) | [append](https://developer.android.com/reference/kotlin/android/text/SpannableStringBuilder#append(kotlin.Char))`(`text:` ` [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)`)` <br /> |
| open [SpannableStringBuilder](https://developer.android.com/reference/kotlin/android/text/SpannableStringBuilder#) | [append](https://developer.android.com/reference/kotlin/android/text/SpannableStringBuilder#append(kotlin.CharSequence))`(`text:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)?`)` <br /> |
| open [SpannableStringBuilder](https://developer.android.com/reference/kotlin/android/text/SpannableStringBuilder#) | [append](https://developer.android.com/reference/kotlin/android/text/SpannableStringBuilder#append(kotlin.CharSequence,%20kotlin.Int,%20kotlin.Int))`(`text:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)?`, `start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `end:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [SpannableStringBuilder](https://developer.android.com/reference/kotlin/android/text/SpannableStringBuilder#)! | [append](https://developer.android.com/reference/kotlin/android/text/SpannableStringBuilder#append(kotlin.CharSequence,%20kotlin.Any,%20kotlin.Int))`(`text:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `what:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Appends the character sequence`text`and spans`what`over the appended part. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clear](https://developer.android.com/reference/kotlin/android/text/SpannableStringBuilder#clear())`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clearSpans](https://developer.android.com/reference/kotlin/android/text/SpannableStringBuilder#clearSpans())`()` <br /> |
| open [SpannableStringBuilder](https://developer.android.com/reference/kotlin/android/text/SpannableStringBuilder#)! | [delete](https://developer.android.com/reference/kotlin/android/text/SpannableStringBuilder#delete(kotlin.Int,%20kotlin.Int))`(`start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `end:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/text/SpannableStringBuilder#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Indicates whether some other object is "equal to" this one. |
| open [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | [get](https://developer.android.com/reference/kotlin/android/text/SpannableStringBuilder#get(kotlin.Int))`(`where:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return the char at the specified offset within the buffer. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [getChars](https://developer.android.com/reference/kotlin/android/text/SpannableStringBuilder#getChars(kotlin.Int,%20kotlin.Int,%20kotlin.CharArray,%20kotlin.Int))`(`start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `end:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `dest:` ` [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!`, `destoff:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Copy the specified range of chars from this buffer into the specified array, beginning at the specified offset. |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [InputFilter](https://developer.android.com/reference/kotlin/android/text/InputFilter)!\>! | [getFilters](https://developer.android.com/reference/kotlin/android/text/SpannableStringBuilder#getFilters())`()` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSpanEnd](https://developer.android.com/reference/kotlin/android/text/SpannableStringBuilder#getSpanEnd(kotlin.Any))`(`what:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Return the buffer offset of the end of the specified markup object, or -1 if it is not attached to this buffer. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSpanFlags](https://developer.android.com/reference/kotlin/android/text/SpannableStringBuilder#getSpanFlags(kotlin.Any))`(`what:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Return the flags of the end of the specified markup object, or 0 if it is not attached to this buffer. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSpanStart](https://developer.android.com/reference/kotlin/android/text/SpannableStringBuilder#getSpanStart(kotlin.Any))`(`what:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Return the buffer offset of the beginning of the specified markup object, or -1 if it is not attached to this buffer. |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\<T\>! | [getSpans](https://developer.android.com/reference/kotlin/android/text/SpannableStringBuilder#getSpans(kotlin.Int,%20kotlin.Int,%20java.lang.Class))`(`queryStart:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `queryEnd:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `kind:` ` [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)<T>?`)` Return an array of the spans of the specified type that overlap the specified range of the buffer. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getTextRunCursor](https://developer.android.com/reference/kotlin/android/text/SpannableStringBuilder#getTextRunCursor(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20android.graphics.Paint))`(`contextStart:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `contextEnd:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `dir:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `cursorOpt:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `p:` ` [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint.html#)!`)` Returns the next cursor position in the run. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getTextWatcherDepth](https://developer.android.com/reference/kotlin/android/text/SpannableStringBuilder#getTextWatcherDepth())`()` Returns the depth of TextWatcher callbacks. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/text/SpannableStringBuilder#hashCode())`()` <br /> |
| open [SpannableStringBuilder](https://developer.android.com/reference/kotlin/android/text/SpannableStringBuilder#)! | [insert](https://developer.android.com/reference/kotlin/android/text/SpannableStringBuilder#insert(kotlin.Int,%20kotlin.CharSequence))`(`where:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `tb:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` <br /> |
| open [SpannableStringBuilder](https://developer.android.com/reference/kotlin/android/text/SpannableStringBuilder#)! | [insert](https://developer.android.com/reference/kotlin/android/text/SpannableStringBuilder#insert(kotlin.Int,%20kotlin.CharSequence,%20kotlin.Int,%20kotlin.Int))`(`where:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `tb:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `end:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [nextSpanTransition](https://developer.android.com/reference/kotlin/android/text/SpannableStringBuilder#nextSpanTransition(kotlin.Int,%20kotlin.Int,%20java.lang.Class))`(`start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `limit:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `kind:` ` [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!>!`)` Return the next offset after`start`but less than or equal to`limit`where a span of the specified type begins or ends. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeSpan](https://developer.android.com/reference/kotlin/android/text/SpannableStringBuilder#removeSpan(kotlin.Any))`(`what:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Remove the specified markup object from the buffer. |
| open [SpannableStringBuilder](https://developer.android.com/reference/kotlin/android/text/SpannableStringBuilder#)! | [replace](https://developer.android.com/reference/kotlin/android/text/SpannableStringBuilder#replace(kotlin.Int,%20kotlin.Int,%20kotlin.CharSequence))`(`start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `end:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `tb:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` <br /> |
| open [SpannableStringBuilder](https://developer.android.com/reference/kotlin/android/text/SpannableStringBuilder#)! | [replace](https://developer.android.com/reference/kotlin/android/text/SpannableStringBuilder#replace(kotlin.Int,%20kotlin.Int,%20kotlin.CharSequence,%20kotlin.Int,%20kotlin.Int))`(`start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `end:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `tb:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `tbstart:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `tbend:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFilters](https://developer.android.com/reference/kotlin/android/text/SpannableStringBuilder#setFilters(kotlin.Array))`(`filters:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [InputFilter](https://developer.android.com/reference/kotlin/android/text/InputFilter)!>!`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSpan](https://developer.android.com/reference/kotlin/android/text/SpannableStringBuilder#setSpan(kotlin.Any,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`what:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`, `start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `end:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Mark the specified range of text with the specified object. |
| open [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html) | [subSequence](https://developer.android.com/reference/kotlin/android/text/SpannableStringBuilder#subSequence(kotlin.Int,%20kotlin.Int))`(`startIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `endIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return a new CharSequence containing a copy of the specified range of this buffer, including the overlapping spans. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/text/SpannableStringBuilder#toString())`()` Return a String containing a copy of the chars in this buffer. |
| openstatic [SpannableStringBuilder](https://developer.android.com/reference/kotlin/android/text/SpannableStringBuilder#)! | [valueOf](https://developer.android.com/reference/kotlin/android/text/SpannableStringBuilder#valueOf(kotlin.CharSequence))`(`source:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` <br /> |

| Properties ||
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [length](https://developer.android.com/reference/kotlin/android/text/SpannableStringBuilder#length:kotlin.Int) Return the number of chars in the buffer. |

## Public constructors

### SpannableStringBuilder

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SpannableStringBuilder()
```

Create a new SpannableStringBuilder with empty contents 

### SpannableStringBuilder

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SpannableStringBuilder(text: CharSequence!)
```

Create a new SpannableStringBuilder containing a copy of the specified text, including its spans if any. 

### SpannableStringBuilder

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SpannableStringBuilder(
    text: CharSequence!, 
    start: Int, 
    end: Int)
```

Create a new SpannableStringBuilder containing a copy of the specified slice of the specified text, including its spans if any.

## Public methods

### append

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun append(text: Char): SpannableStringBuilder
```

| Parameters ||
|-----|-------------------------|
| `c` | The character to append |

| Return ||
|---------------------------------------------------------------------------------------------------------------|---------------------------------|
| [SpannableStringBuilder](https://developer.android.com/reference/kotlin/android/text/SpannableStringBuilder#) | A reference to this`Appendable` |

| Exceptions ||
|-----------------------|------------------------|
| `java.io.IOException` | If an I/O error occurs |

### append

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun append(text: CharSequence?): SpannableStringBuilder
```

| Parameters ||
|-------|---------------------------------------------------------------------------------------------------------------------|
| `csq` | The character sequence to append. If`csq`is`null`, then the four characters`"null"`are appended to this Appendable. |

| Return ||
|---------------------------------------------------------------------------------------------------------------|---------------------------------|
| [SpannableStringBuilder](https://developer.android.com/reference/kotlin/android/text/SpannableStringBuilder#) | A reference to this`Appendable` |

| Exceptions ||
|-----------------------|------------------------|
| `java.io.IOException` | If an I/O error occurs |

### append

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun append(
    text: CharSequence?, 
    start: Int, 
    end: Int
): SpannableStringBuilder
```

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `csq` | The character sequence from which a subsequence will be appended. If`csq`is`null`, then characters will be appended as if`csq`contained the four characters`"null"`. |
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The index of the first character in the subsequence |
| `end` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The index of the character following the last character in the subsequence |

| Return ||
|---------------------------------------------------------------------------------------------------------------|---------------------------------|
| [SpannableStringBuilder](https://developer.android.com/reference/kotlin/android/text/SpannableStringBuilder#) | A reference to this`Appendable` |

| Exceptions ||
|---------------------------------------|------------------------------------------------------------------------------------------------|
| `java.lang.IndexOutOfBoundsException` | If`start`or`end`are negative,`start`is greater than`end`, or`end`is greater than`csq.length()` |
| `java.io.IOException` | If an I/O error occurs |

### append

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun append(
    text: CharSequence!, 
    what: Any!, 
    flags: Int
): SpannableStringBuilder!
```

Appends the character sequence`text`and spans`what`over the appended part. See [Spanned](https://developer.android.com/reference/kotlin/android/text/Spanned) for an explanation of what the flags mean.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `text` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:the character sequence to append. |
| `what` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:the object to be spanned over the appended text. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):see [Spanned](https://developer.android.com/reference/kotlin/android/text/Spanned). |

| Return ||
|----------------------------------------------------------------------------------------------------------------|-------------------------------|
| [SpannableStringBuilder](https://developer.android.com/reference/kotlin/android/text/SpannableStringBuilder#)! | this`SpannableStringBuilder`. |

### clear

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun clear(): Unit
```  

### clearSpans

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun clearSpans(): Unit
```  

### delete

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun delete(
    start: Int, 
    end: Int
): SpannableStringBuilder!
```  

### equals

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun equals(other: Any?): Boolean
```

Indicates whether some other object is "equal to" this one.

The`equals`method implements an equivalence relation on non-null object references:

- It is*reflexive* : for any non-null reference value`x`,`x.equals(x)`should return`true`.
- It is*symmetric* : for any non-null reference values`x`and`y`,`x.equals(y)`should return`true`if and only if`y.equals(x)`returns`true`.
- It is*transitive* : for any non-null reference values`x`,`y`, and`z`, if`x.equals(y)`returns`true`and`y.equals(z)`returns`true`, then`x.equals(z)`should return`true`.
- It is*consistent* : for any non-null reference values`x`and`y`, multiple invocations of`x.equals(y)`consistently return`true`or consistently return`false`, provided no information used in`equals`comparisons on the objects is modified.
- For any non-null reference value`x`,`x.equals(null)`should return`false`.

An equivalence relation partitions the elements it operates on into*equivalence classes*; all the members of an equivalence class are equal to each other. Members of an equivalence class are substitutable for each other, at least for some purposes.

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |
| `o` | This value may be`null`. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

### get

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun get(where: Int): Char
```

Return the char at the specified offset within the buffer.

| Parameters ||
|---------|--------------------------------------------|
| `index` | the index of the`char`value to be returned |

| Return ||
|------------------------------------------------------------------------------|--------------------------|
| [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | the specified`char`value |

| Exceptions ||
|---------------------------------------|--------------------------------------------------------------|
| `java.lang.IndexOutOfBoundsException` | if the`index`argument is negative or not less than`length()` |

### getChars

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getChars(
    start: Int, 
    end: Int, 
    dest: CharArray!, 
    destoff: Int
): Unit
```

Copy the specified range of chars from this buffer into the specified array, beginning at the specified offset. 

### getFilters

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getFilters(): Array<InputFilter!>!
```  

### getSpanEnd

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSpanEnd(what: Any!): Int
```

Return the buffer offset of the end of the specified markup object, or -1 if it is not attached to this buffer. 

### getSpanFlags

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSpanFlags(what: Any!): Int
```

Return the flags of the end of the specified markup object, or 0 if it is not attached to this buffer. 

### getSpanStart

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSpanStart(what: Any!): Int
```

Return the buffer offset of the beginning of the specified markup object, or -1 if it is not attached to this buffer. 

### getSpans

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun <T : Any!> getSpans(
    queryStart: Int, 
    queryEnd: Int, 
    kind: Class<T>?
): Array<T>!
```

Return an array of the spans of the specified type that overlap the specified range of the buffer. The kind may be Object.class to get a list of all the spans regardless of type.

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------|
| `kind` | [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)\<T\>?:This value may be`null`. |

### getTextRunCursor

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getTextRunCursor(
    contextStart: Int, 
    contextEnd: Int, 
    dir: Int, 
    offset: Int, 
    cursorOpt: Int, 
    p: Paint!
): Int
```

**Deprecated:** *This is an internal method, refrain from using it in your code*

Returns the next cursor position in the run. This avoids placing the cursor between surrogates, between characters that form conjuncts, between base characters and combining marks, or within a reordering cluster.

The context is the shaping context for cursor movement, generally the bounds of the metric span enclosing the cursor in the direction of movement.`contextStart`,`contextEnd`and`offset`are relative to the start of the string.

If cursorOpt is CURSOR_AT and the offset is not a valid cursor position, this returns -1. Otherwise this will never return a value before contextStart or after contextEnd.

| Parameters ||
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `contextStart` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the start index of the context |
| `contextEnd` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the (non-inclusive) end index of the context |
| `dir` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):1 if the run is RTL, otherwise 0 |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the cursor position to move from |
| `cursorOpt` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):how to move the cursor, one of CURSOR_AFTER, CURSOR_AT_OR_AFTER, CURSOR_BEFORE, CURSOR_AT_OR_BEFORE, or CURSOR_AT |
| `p` | [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint.html#)!:the Paint object that is requesting this information |

| Return ||
|----------------------------------------------------------------------------|----------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the offset of the next position, or -1 |

### getTextWatcherDepth

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getTextWatcherDepth(): Int
```

Returns the depth of TextWatcher callbacks. Returns 0 when the object is not handling TextWatchers. A return value greater than 1 implies that a TextWatcher caused a change that recursively triggered a TextWatcher. 

### hashCode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### insert

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun insert(
    where: Int, 
    tb: CharSequence!
): SpannableStringBuilder!
```  

### insert

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun insert(
    where: Int, 
    tb: CharSequence!, 
    start: Int, 
    end: Int
): SpannableStringBuilder!
```  

### nextSpanTransition

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun nextSpanTransition(
    start: Int, 
    limit: Int, 
    kind: Class<Any!>!
): Int
```

Return the next offset after`start`but less than or equal to`limit`where a span of the specified type begins or ends. 

### removeSpan

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun removeSpan(what: Any!): Unit
```

Remove the specified markup object from the buffer. 

### replace

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun replace(
    start: Int, 
    end: Int, 
    tb: CharSequence!
): SpannableStringBuilder!
```  

### replace

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun replace(
    start: Int, 
    end: Int, 
    tb: CharSequence!, 
    tbstart: Int, 
    tbend: Int
): SpannableStringBuilder!
```

| Return ||
|----------------------------------------------------------------------------------------------------------------|-----------------------------|
| [SpannableStringBuilder](https://developer.android.com/reference/kotlin/android/text/SpannableStringBuilder#)! | a reference to this object. |

### setFilters

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setFilters(filters: Array<InputFilter!>!): Unit
```  

### setSpan

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setSpan(
    what: Any!, 
    start: Int, 
    end: Int, 
    flags: Int
): Unit
```

Mark the specified range of text with the specified object. The flags determine how the span will behave when text is inserted at the start or end of the span's range. 

### subSequence

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun subSequence(
    startIndex: Int, 
    endIndex: Int
): CharSequence
```

Return a new CharSequence containing a copy of the specified range of this buffer, including the overlapping spans.

| Parameters ||
|---------|----------------------------|
| `start` | the start index, inclusive |
| `end` | the end index, exclusive |

| Return ||
|-----------------------------------------------------------------------------------------------|---------------------------|
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html) | the specified subsequence |

| Exceptions ||
|---------------------------------------|--------------------------------------------------------------------------------------------------|
| `java.lang.IndexOutOfBoundsException` | if`start`or`end`are negative, if`end`is greater than`length()`, or if`start`is greater than`end` |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

Return a String containing a copy of the chars in this buffer.

| Return ||
|----------------------------------------------------------------------------------|------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string consisting of exactly this sequence of characters |

### valueOf

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun valueOf(source: CharSequence!): SpannableStringBuilder!
```

## Properties

### length

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open val length: Int
```

Return the number of chars in the buffer.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of`char`s in this sequence |
