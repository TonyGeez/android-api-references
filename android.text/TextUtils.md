# TextUtils

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TextUtils

Kotlin| [Java](../android/text/TextUtils.md) 
| --- | --- |

```
open class TextUtils
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.text.TextUtils](../android/text/TextUtils.md) |

## Summary

| Nested classes ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [EllipsizeCallback](../android/text/TextUtils.EllipsizeCallback.md) <br /> |
| open | [SimpleStringSplitter](../android/text/TextUtils.SimpleStringSplitter.md) A simple string splitter. |
| abstract | [StringSplitter](../android/text/TextUtils.StringSplitter.md) An interface for splitting strings according to rules that are opaque to the user of this interface. |
| --- | --- |
| | [TruncateAt](../android/text/TextUtils.TruncateAt.md) <br /> |

| Constants ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CAP_MODE_CHARACTERS](../android/text/TextUtils.md) Capitalization mode for [getCapsMode](../android/text/TextUtils.md)): capitalize all characters. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CAP_MODE_SENTENCES](../android/text/TextUtils.md) Capitalization mode for [getCapsMode](../android/text/TextUtils.md)): capitalize the first character of each sentence. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CAP_MODE_WORDS](../android/text/TextUtils.md) Capitalization mode for [getCapsMode](../android/text/TextUtils.md)): capitalize the first character of all words. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SAFE_STRING_FLAG_FIRST_LINE](../android/text/TextUtils.md) Return only first line of text (truncate at first newline). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SAFE_STRING_FLAG_SINGLE_LINE](../android/text/TextUtils.md) Force entire string into single line of text (no newlines). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SAFE_STRING_FLAG_TRIM](../android/text/TextUtils.md) Remove [whitespace](../java/lang/Character.md))and non-breaking spaces from the edges of the label. |
| --- | --- |

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | [commaEllipsize](../android/text/TextUtils.md))`(`text:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `p:` ` [TextPaint](../android/text/TextPaint.md)!`, `avail:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `oneMore:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `more:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Converts a CharSequence of the comma-separated form "Andy, Bob, Charles, David" that is too wide to fit into the specified width into one like "Andy, Bob, 2 more". |
| openstatic [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | [concat](../android/text/TextUtils.md))`(`vararg` `text:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` Returns a CharSequence concatenating the specified CharSequences, retaining their spans if any. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [copySpansFrom](../android/text/TextUtils.md))`(`source:` ` [Spanned](../android/text/Spanned.md)!`, `start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `end:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `kind:` ` [Class](../java/lang/Class.md)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!>!`, `dest:` ` [Spannable](../android/text/Spannable.md)!`, `destoff:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Copies the spans from the region`start...end`in`source`to the region`destoff...destoff+end-start`in`dest`. |
| --- | --- |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [dumpSpans](../android/text/TextUtils.md))`(`cs:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `printer:` ` [Printer](../android/util/Printer.md)!`, `prefix:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Debugging tool to print the spans in a CharSequence. |
| openstatic [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | [ellipsize](../android/text/TextUtils.md))`(`text:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `p:` ` [TextPaint](../android/text/TextPaint.md)!`, `avail:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `where:` ` [TextUtils.TruncateAt](../android/text/TextUtils.TruncateAt.md)!`)` Returns the original text if it fits in the specified width given the properties of the specified Paint, or, if it does not fit, a truncated copy with ellipsis character added at the specified edge or center. |
| openstatic [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | [ellipsize](../android/text/TextUtils.md))`(`text:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `paint:` ` [TextPaint](../android/text/TextPaint.md)!`, `avail:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `where:` ` [TextUtils.TruncateAt](../android/text/TextUtils.TruncateAt.md)!`, `preserveLength:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `callback:` ` [TextUtils.EllipsizeCallback](../android/text/TextUtils.EllipsizeCallback.md)?`)` Returns the original text if it fits in the specified width given the properties of the specified Paint, or, if it does not fit, a copy with ellipsis character added at the specified edge or center. |
| --- | --- |
| openstatic [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](../android/text/TextUtils.md))`(`a:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)?`, `b:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)?`)` Returns true if a and b are equal, including if they are both null. |
| openstatic [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | [expandTemplate](../android/text/TextUtils.md))`(`template:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `vararg` `values:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` Replace instances of "\^1", "\^2", etc. |
| openstatic [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getCapsMode](../android/text/TextUtils.md))`(`cs:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `off:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `reqModes:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Determine what caps mode should be in effect at the current offset in the text. |
| --- | --- |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [getChars](../android/text/TextUtils.md))`(`s:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `end:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `dest:` ` [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!`, `destoff:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| openstatic [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLayoutDirectionFromLocale](../android/text/TextUtils.md))`(`locale:` ` [Locale](../java/util/Locale.md)!`)` Return the layout direction for a given Locale |
| openstatic [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getOffsetAfter](../android/text/TextUtils.md))`(`text:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |
| openstatic [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getOffsetBefore](../android/text/TextUtils.md))`(`text:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| openstatic [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | [getReverse](../android/text/TextUtils.md))`(`source:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `end:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` This function only reverses individual`char`s and not their associated spans. |
| openstatic [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getTrimmedLength](../android/text/TextUtils.md))`(`s:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` Returns the length that the specified CharSequence would have if spaces and ASCII control characters were trimmed from the start and end, as by [String.trim](../java/lang/String.md)). |
| --- | --- |
| openstatic [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [htmlEncode](../android/text/TextUtils.md))`(`s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Html-encode the string. |
| openstatic [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [indexOf](../android/text/TextUtils.md))`(`s:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `ch:` ` [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)`)` <br /> |
| openstatic [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [indexOf](../android/text/TextUtils.md))`(`s:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `ch:` ` [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)`, `start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |
| openstatic [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [indexOf](../android/text/TextUtils.md))`(`s:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `ch:` ` [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)`, `start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `end:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| openstatic [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [indexOf](../android/text/TextUtils.md))`(`s:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `needle:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` <br /> |
| openstatic [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [indexOf](../android/text/TextUtils.md))`(`s:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `needle:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |
| openstatic [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [indexOf](../android/text/TextUtils.md))`(`s:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `needle:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `end:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| openstatic [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isDigitsOnly](../android/text/TextUtils.md))`(`str:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` Returns whether the given CharSequence contains only digits. |
| openstatic [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEmpty](../android/text/TextUtils.md))`(`str:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)?`)` Returns true if the string is null or 0-length. |
| --- | --- |
| openstatic [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isGraphic](../android/text/TextUtils.md))`(`c:` ` [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)`)` Returns whether this character is a printable character. |
| openstatic [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isGraphic](../android/text/TextUtils.md))`(`str:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` Returns whether the given CharSequence contains any printable characters. |
| openstatic [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [join](../android/text/TextUtils.md))`(`delimiter:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)`, `tokens:` ` [MutableIterable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterable/index.html)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?>`)` Returns a string containing the tokens joined by delimiters. |
| --- | --- |
| openstatic [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [join](../android/text/TextUtils.md))`(`delimiter:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)`, `tokens:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!>`)` Returns a string containing the tokens joined by delimiters. |
| openstatic [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [lastIndexOf](../android/text/TextUtils.md))`(`s:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `ch:` ` [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)`)` <br /> |
| openstatic [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [lastIndexOf](../android/text/TextUtils.md))`(`s:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `ch:` ` [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)`, `last:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |
| openstatic [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [lastIndexOf](../android/text/TextUtils.md))`(`s:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `ch:` ` [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)`, `start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `last:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| openstatic [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | [listEllipsize](../android/text/TextUtils.md))`(`context:` ` [Context](../android/content/Context.md)?`, `elements:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!>?`, `separator:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `paint:` ` [TextPaint](../android/text/TextPaint.md)`, `avail:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `moreId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Formats a list of CharSequences by repeatedly inserting the separator between them, but stopping when the resulting sequence is too wide for the specified width. |
| openstatic [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html) | [makeSafeForPresentation](../android/text/TextUtils.md))`(`unclean:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `maxCharactersToConsider:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `ellipsizeDip:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Remove html, remove bad characters, and truncate string. |
| --- | --- |
| openstatic [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [regionMatches](../android/text/TextUtils.md))`(`one:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `toffset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `two:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `ooffset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `len:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| openstatic [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | [replace](../android/text/TextUtils.md))`(`template:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `sources:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`, `destinations:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!>!`)` Return a new CharSequence in which each of the source strings is replaced by the corresponding element of the destinations. |
| openstatic [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [split](../android/text/TextUtils.md))`(`text:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `expression:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` This method yields the same result as`text.split(expression, -1)`except that if`text.isEmpty()`then this method returns an empty array whereas`"".split(expression, -1)`would have returned an array with a single`""`. |
| --- | --- |
| openstatic [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [split](../android/text/TextUtils.md))`(`text:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `pattern:` ` [Pattern](../java/util/regex/Pattern.md)!`)` Splits a string on a pattern. |
| openstatic [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | [stringOrSpannedString](../android/text/TextUtils.md))`(`source:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` <br /> |
| openstatic [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [substring](../android/text/TextUtils.md))`(`source:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `end:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Create a new String object containing the given range of characters from the source string. |
| --- | --- |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](../android/text/TextUtils.md))`(`cs:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)?`, `p:` ` [Parcel](../android/os/Parcel.md)`, `parcelableFlags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten a CharSequence and whatever styles can be copied across processes into the parcel. |

| Properties ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!\>! | [CHAR_SEQUENCE_CREATOR](../android/text/TextUtils.md) <br /> |

## Constants

### CAP_MODE_CHARACTERS

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CAP_MODE_CHARACTERS: Int
```

Capitalization mode for [getCapsMode](../android/text/TextUtils.md)): capitalize all characters. This value is explicitly defined to be the same as [InputType.TYPE_TEXT_FLAG_CAP_CHARACTERS](../android/text/InputType.md). 

 Value: 4096

### CAP_MODE_SENTENCES

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CAP_MODE_SENTENCES: Int
```

Capitalization mode for [getCapsMode](../android/text/TextUtils.md)): capitalize the first character of each sentence. This value is explicitly defined to be the same as [InputType.TYPE_TEXT_FLAG_CAP_SENTENCES](../android/text/InputType.md). 

 Value: 16384

### CAP_MODE_WORDS

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CAP_MODE_WORDS: Int
```

Capitalization mode for [getCapsMode](../android/text/TextUtils.md)): capitalize the first character of all words. This value is explicitly defined to be the same as [InputType.TYPE_TEXT_FLAG_CAP_WORDS](../android/text/InputType.md). 

 Value: 8192

### SAFE_STRING_FLAG_FIRST_LINE

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SAFE_STRING_FLAG_FIRST_LINE: Int
```

Return only first line of text (truncate at first newline). Cannot be set at the same time as [SAFE_STRING_FLAG_SINGLE_LINE](../android/text/TextUtils.md). 

 Value: 4

**See Also**

- [#makeSafeForPresentation(String, int, float, int)](../android/text/TextUtils.md)) 

### SAFE_STRING_FLAG_SINGLE_LINE

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SAFE_STRING_FLAG_SINGLE_LINE: Int
```

Force entire string into single line of text (no newlines). Cannot be set at the same time as [SAFE_STRING_FLAG_FIRST_LINE](../android/text/TextUtils.md). 

 Value: 2

**See Also**

- [#makeSafeForPresentation(String, int, float, int)](../android/text/TextUtils.md)) 

### SAFE_STRING_FLAG_TRIM

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SAFE_STRING_FLAG_TRIM: Int
```

Remove [whitespace](../java/lang/Character.md))and non-breaking spaces from the edges of the label. 

 Value: 1

**See Also**

- [#makeSafeForPresentation(String, int, float, int)](../android/text/TextUtils.md))

## Public methods

### commaEllipsize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun commaEllipsize(
    text: CharSequence!, 
    p: TextPaint!, 
    avail: Float, 
    oneMore: String!, 
    more: String!
): CharSequence!
```

**Deprecated:** *Do not use. This is not internationalized, and has known issues with right-to-left text, languages that have more than one plural form, languages that use a different character as a comma-like separator, etc. Use [listEllipsize](../android/text/TextUtils.md))instead.*

Converts a CharSequence of the comma-separated form "Andy, Bob, Charles, David" that is too wide to fit into the specified width into one like "Andy, Bob, 2 more".

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------------------------------|
| `text` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:the text to truncate |
| `p` | [TextPaint](../android/text/TextPaint.md)!:the Paint with which to measure the text |
| `avail` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):the horizontal width available for the text (in pixels) |
| --- | --- |
| `oneMore` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the string for "1 more" in the current locale |
| `more` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the string for "%d more" in the current locale |

### concat

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun concat(vararg text: CharSequence!): CharSequence!
```

Returns a CharSequence concatenating the specified CharSequences, retaining their spans if any. If there are no parameters, an empty string will be returned. If the number of parameters is exactly one, that parameter is returned as output, even if it is null. If the number of parameters is at least two, any null CharSequence among the parameters is treated as if it was the string`"null"`. If there are paragraph spans in the source CharSequences that satisfy paragraph boundary requirements in the sources but would no longer satisfy them in the concatenated CharSequence, they may get extended in the resulting CharSequence or not retained. 

### copySpansFrom

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun copySpansFrom(
    source: Spanned!, 
    start: Int, 
    end: Int, 
    kind: Class<Any!>!, 
    dest: Spannable!, 
    destoff: Int
): Unit
```

Copies the spans from the region`start...end`in`source`to the region`destoff...destoff+end-start`in`dest`. Spans in`source`that begin before`start`or end after`end`but overlap this range are trimmed as if they began at`start`or ended at`end`.

| Exceptions ||
|---------------------------------------|-------------------------------------------------------|
| `java.lang.IndexOutOfBoundsException` | if any of the copied spans are out of range in`dest`. |

### dumpSpans

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun dumpSpans(
    cs: CharSequence!, 
    printer: Printer!, 
    prefix: String!
): Unit
```

Debugging tool to print the spans in a CharSequence. The output will be printed one span per line. If the CharSequence is not a Spanned, then the entire string will be printed on a single line. 

### ellipsize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun ellipsize(
    text: CharSequence!, 
    p: TextPaint!, 
    avail: Float, 
    where: TextUtils.TruncateAt!
): CharSequence!
```

Returns the original text if it fits in the specified width given the properties of the specified Paint, or, if it does not fit, a truncated copy with ellipsis character added at the specified edge or center. 

### ellipsize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun ellipsize(
    text: CharSequence!, 
    paint: TextPaint!, 
    avail: Float, 
    where: TextUtils.TruncateAt!, 
    preserveLength: Boolean, 
    callback: TextUtils.EllipsizeCallback?
): CharSequence!
```

Returns the original text if it fits in the specified width given the properties of the specified Paint, or, if it does not fit, a copy with ellipsis character added at the specified edge or center. If`preserveLength`is specified, the returned copy will be padded with zero-width spaces to preserve the original length and offsets instead of truncating. If`callback`is non-null, it will be called to report the start and end of the ellipsized range. TextDirection is determined by the first strong directional character.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| `callback` | [TextUtils.EllipsizeCallback](../android/text/TextUtils.EllipsizeCallback.md)?:This value may be`null`. |

### equals

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun equals(
    a: CharSequence?, 
    b: CharSequence?
): Boolean
```

Returns true if a and b are equal, including if they are both null.

*Note: In platform versions 1.1 and earlier, this method only worked well if both the arguments were instances of String.*

| Parameters ||
|-----|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `a` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)?:first CharSequence to check This value may be`null`. |
| `b` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)?:second CharSequence to check This value may be`null`. |

| Return ||
|------------------------------------------------------------------------------------|---------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if a and b are equal |

### expandTemplate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun expandTemplate(
    template: CharSequence!, 
    vararg values: CharSequence!
): CharSequence!
```

Replace instances of "\^1", "\^2", etc. in the`template`CharSequence with the corresponding`values`. "\^\^" is used to produce a single caret in the output. Only up to 9 replacement values are supported, "\^10" will be produce the first replacement value followed by a '0'.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `template` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:the input text containing "\^1"-style placeholder values. This object is not modified; a copy is returned. |
| `values` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:CharSequences substituted into the template. The first is substituted for "\^1", the second for "\^2", and so on. |

| Return ||
|------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | the new CharSequence produced by doing the replacement |

| Exceptions ||
|--------------------------------------|------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the template requests a value that was not provided, or if more than 9 values are provided. |

### getCapsMode

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getCapsMode(
    cs: CharSequence!, 
    off: Int, 
    reqModes: Int
): Int
```

Determine what caps mode should be in effect at the current offset in the text. Only the mode bits set in reqModes will be checked. Note that the caps mode flags here are explicitly defined to match those in [InputType](../android/text/InputType.md).

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `cs` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:The text that should be checked for caps modes. |
| `off` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Location in the text at which to check. |
| `reqModes` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The modes to be checked: may be any combination of [CAP_MODE_CHARACTERS](../android/text/TextUtils.md), [CAP_MODE_WORDS](../android/text/TextUtils.md), and [CAP_MODE_SENTENCES](../android/text/TextUtils.md). |
| --- | --- |

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Returns the actual capitalization modes that can be in effect at the current position, which is any combination of [CAP_MODE_CHARACTERS](../android/text/TextUtils.md), [CAP_MODE_WORDS](../android/text/TextUtils.md), and [CAP_MODE_SENTENCES](../android/text/TextUtils.md). |

### getChars

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getChars(
    s: CharSequence!, 
    start: Int, 
    end: Int, 
    dest: CharArray!, 
    destoff: Int
): Unit
```  

### getLayoutDirectionFromLocale

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getLayoutDirectionFromLocale(locale: Locale!): Int
```

Return the layout direction for a given Locale

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| `locale` | [Locale](../java/util/Locale.md)!:the Locale for which we want the layout direction. Can be null. |

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the layout direction. This may be one of: [android.view.View#LAYOUT_DIRECTION_LTR](../android/view/View.md) or [android.view.View#LAYOUT_DIRECTION_RTL](../android/view/View.md). Be careful: this code will need to be updated when vertical scripts will be supported |

### getOffsetAfter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getOffsetAfter(
    text: CharSequence!, 
    offset: Int
): Int
```  

### getOffsetBefore

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getOffsetBefore(
    text: CharSequence!, 
    offset: Int
): Int
```  

### getReverse

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getReverse(
    source: CharSequence!, 
    start: Int, 
    end: Int
): CharSequence!
```

**Deprecated:** *Do not use.*

This function only reverses individual`char`s and not their associated spans. It doesn't support surrogate pairs (that correspond to non-BMP code points), combining sequences or conjuncts either. 

### getTrimmedLength

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getTrimmedLength(s: CharSequence!): Int
```

Returns the length that the specified CharSequence would have if spaces and ASCII control characters were trimmed from the start and end, as by [String.trim](../java/lang/String.md)). 

### htmlEncode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun htmlEncode(s: String!): String!
```

Html-encode the string.

| Parameters ||
|-----|------------------------------------------------------------------------------------------------------------|
| `s` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the string to be encoded |

| Return ||
|-----------------------------------------------------------------------------------|--------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the encoded string |

### indexOf

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun indexOf(
    s: CharSequence!, 
    ch: Char
): Int
```  

### indexOf

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun indexOf(
    s: CharSequence!, 
    ch: Char, 
    start: Int
): Int
```  

### indexOf

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun indexOf(
    s: CharSequence!, 
    ch: Char, 
    start: Int, 
    end: Int
): Int
```  

### indexOf

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun indexOf(
    s: CharSequence!, 
    needle: CharSequence!
): Int
```  

### indexOf

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun indexOf(
    s: CharSequence!, 
    needle: CharSequence!, 
    start: Int
): Int
```  

### indexOf

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun indexOf(
    s: CharSequence!, 
    needle: CharSequence!, 
    start: Int, 
    end: Int
): Int
```  

### isDigitsOnly

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun isDigitsOnly(str: CharSequence!): Boolean
```

Returns whether the given CharSequence contains only digits. 

### isEmpty

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun isEmpty(str: CharSequence?): Boolean
```

Returns true if the string is null or 0-length.

| Parameters ||
|-------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| `str` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)?:the string to be examined This value may be`null`. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if str is null or zero length |

### isGraphic

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun isGraphic(c: Char): Boolean
```

**Deprecated:** *Use [isGraphic(java.lang.CharSequence)](../android/text/TextUtils.md))instead.*

Returns whether this character is a printable character. This does not support non-BMP characters and should not be used. 

### isGraphic

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun isGraphic(str: CharSequence!): Boolean
```

Returns whether the given CharSequence contains any printable characters. 

### join

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun join(
    delimiter: CharSequence, 
    tokens: MutableIterable<Any?>
): String!
```

Returns a string containing the tokens joined by delimiters.

| Parameters ||
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `delimiter` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html):a CharSequence that will be inserted between the tokens. If null, the string "null" will be used as the delimiter. |
| `tokens` | [MutableIterable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterable/index.html)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?\>:an array objects to be joined. Strings will be formed from the objects by calling object.toString(). If tokens is null, a NullPointerException will be thrown. If tokens is empty, an empty string will be returned. |

### join

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun join(
    delimiter: CharSequence, 
    tokens: Array<Any!>
): String!
```

Returns a string containing the tokens joined by delimiters.

| Parameters ||
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `delimiter` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html):a CharSequence that will be inserted between the tokens. If null, the string "null" will be used as the delimiter. |
| `tokens` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\>:an array objects to be joined. Strings will be formed from the objects by calling object.toString(). If tokens is null, a NullPointerException will be thrown. If tokens is an empty array, an empty string will be returned. |

### lastIndexOf

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun lastIndexOf(
    s: CharSequence!, 
    ch: Char
): Int
```  

### lastIndexOf

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun lastIndexOf(
    s: CharSequence!, 
    ch: Char, 
    last: Int
): Int
```  

### lastIndexOf

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun lastIndexOf(
    s: CharSequence!, 
    ch: Char, 
    start: Int, 
    last: Int
): Int
```  

### listEllipsize

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun listEllipsize(
    context: Context?, 
    elements: MutableList<CharSequence!>?, 
    separator: String, 
    paint: TextPaint, 
    avail: Float, 
    moreId: Int
): CharSequence!
```

Formats a list of CharSequences by repeatedly inserting the separator between them, but stopping when the resulting sequence is too wide for the specified width. This method actually tries to fit the maximum number of elements. So if`"A, 11 more" fits`,`"A, B, 10 more"`doesn't fit, but`"A, B, C, 9 more"`fits again (due to the glyphs for the digits being very wide, for example), it returns`"A, B, C, 9 more"`. Because of this, this method may be inefficient for very long lists. Note that the elements of the returned value, as well as the string for`moreId`, will be bidi-wrapped using android.text.BidiFormatter#unicodeWrap based on the locale of the input Context. If the input`Context`is null, the default BidiFormatter from [BidiFormatter.getInstance()](../android/text/BidiFormatter.md))will be used.

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android/content/Context.md)?:the`Context`to get the`moreId`resource from. If`null`, an ellipsis (U+2026) would be used for`moreId`. |
| `elements` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!\>?:the list to format This value may be`null`. |
| `separator` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):a separator, such as`", "`This value cannot be`null`. |
| --- | --- |
| `paint` | [TextPaint](../android/text/TextPaint.md):the Paint with which to measure the text This value cannot be`null`. |
| `avail` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):the horizontal width available for the text (in pixels) Value is 0.0f or greater |
| `moreId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the resource ID for the pluralized string to insert at the end of sequence when some of the elements don't fit. |
| --- | --- |

| Return ||
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | the formatted CharSequence. If even the shortest sequence (e.g.`"A, 11 more"`) doesn't fit, it will return an empty string. |

### makeSafeForPresentation

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun makeSafeForPresentation(
    unclean: String, 
    maxCharactersToConsider: Int, 
    ellipsizeDip: Float, 
    flags: Int
): CharSequence
```

Remove html, remove bad characters, and truncate string.

This method is meant to remove common mistakes and nefarious formatting from strings that were loaded from untrusted sources (such as other packages).

This method first android.text.Html#fromHtml and then ...

- Removes new lines or truncates at first new line
- Trims the white-space off the end
- Truncates the string

... if specified.

| Parameters ||
|---------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `unclean` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The input string This value cannot be`null`. |
| `maxCharactersToConsider` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The maximum number of characters of`unclean`to consider from the input string.`0`disables this feature. Value is 0 or greater |
| `ellipsizeDip` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):Assuming maximum length of the string (in dip), assuming font size 42. This is roughly 50 characters for`ellipsizeDip == 1000`. Usually ellipsizing should be left to the view showing the string. If a string is used as an input to another string, it might be useful to control the length of the input string though.`0`disables this feature. Value is 0.0f or greater |
| --- | --- |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Flags controlling cleaning behavior (Can be [SAFE_STRING_FLAG_TRIM](../android/text/TextUtils.md), [SAFE_STRING_FLAG_SINGLE_LINE](../android/text/TextUtils.md), and [SAFE_STRING_FLAG_FIRST_LINE](../android/text/TextUtils.md)) Value is either`0`or a combination of [android.text.TextUtils#SAFE_STRING_FLAG_TRIM](../android/text/TextUtils.md), [android.text.TextUtils#SAFE_STRING_FLAG_SINGLE_LINE](../android/text/TextUtils.md), and [android.text.TextUtils#SAFE_STRING_FLAG_FIRST_LINE](../android/text/TextUtils.md) |

| Return ||
|-----------------------------------------------------------------------------------------------|------------------------------------------------|
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html) | The cleaned string This value cannot be`null`. |

### regionMatches

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun regionMatches(
    one: CharSequence!, 
    toffset: Int, 
    two: CharSequence!, 
    ooffset: Int, 
    len: Int
): Boolean
```  

### replace

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun replace(
    template: CharSequence!, 
    sources: Array<String!>!, 
    destinations: Array<CharSequence!>!
): CharSequence!
```

Return a new CharSequence in which each of the source strings is replaced by the corresponding element of the destinations. 

### split

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun split(
    text: String!, 
    expression: String!
): Array<String!>!
```

This method yields the same result as`text.split(expression, -1)`except that if`text.isEmpty()`then this method returns an empty array whereas`"".split(expression, -1)`would have returned an array with a single`""`. The`-1`means that trailing empty Strings are not removed from the result; for example split("a,", "," ) returns {"a", ""}. Note that whether a leading zero-width match can result in a leading`""`depends on whether your app [targets an SDK version](../android/content/pm/ApplicationInfo.md)`<= 28`; see [Pattern.split(CharSequence, int)](../java/util/regex/Pattern.md)).

| Parameters ||
|--------------|-------------------------------------------------------------------------------------------------------------------|
| `text` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the string to split |
| `expression` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the regular expression to match |

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>! | an array of strings. The array will be empty if text is empty |

| Exceptions ||
|----------------------------------|-------------------------------|
| `java.lang.NullPointerException` | if expression or text is null |

### split

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun split(
    text: String!, 
    pattern: Pattern!
): Array<String!>!
```

Splits a string on a pattern. This method yields the same result as`pattern.split(text, -1)`except that if`text.isEmpty()`then this method returns an empty array whereas`pattern.split("", -1)`would have returned an array with a single`""`. The`-1`means that trailing empty Strings are not removed from the result; Note that whether a leading zero-width match can result in a leading`""`depends on whether your app [targets](../android/content/pm/ApplicationInfo.md)`<= 28`; see [Pattern.split(CharSequence, int)](../java/util/regex/Pattern.md)).

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------|
| `text` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the string to split |
| `pattern` | [Pattern](../java/util/regex/Pattern.md)!:the regular expression to match |

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>! | an array of strings. The array will be empty if text is empty |

| Exceptions ||
|----------------------------------|-------------------------------|
| `java.lang.NullPointerException` | if expression or text is null |

### stringOrSpannedString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun stringOrSpannedString(source: CharSequence!): CharSequence!
```  

### substring

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun substring(
    source: CharSequence!, 
    start: Int, 
    end: Int
): String!
```

Create a new String object containing the given range of characters from the source string. This is different than simply calling [CharSequence.subSequence](../java/lang/CharSequence.md))in that it does not preserve any style runs in the source sequence, allowing a more efficient implementation. 

### writeToParcel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun writeToParcel(
    cs: CharSequence?, 
    p: Parcel, 
    parcelableFlags: Int
): Unit
```

Flatten a CharSequence and whatever styles can be copied across processes into the parcel.

| Parameters ||
|------|-------------------------------------------------------------------------------------------------------------------------|
| `cs` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)?:This value may be`null`. |
| `p` | [Parcel](../android/os/Parcel.md):This value cannot be`null`. |

## Properties

### CHAR_SEQUENCE_CREATOR

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CHAR_SEQUENCE_CREATOR: Parcelable.Creator<CharSequence!>!
```
