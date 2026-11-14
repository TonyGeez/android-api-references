# UnicodeFilter

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# UnicodeFilter

Kotlin| [Java](../android/icu/text/UnicodeFilter.md) 
| --- | --- |

```
abstract class UnicodeFilter : UnicodeMatcher
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.icu.text.UnicodeFilter](../android/icu/text/UnicodeFilter.md) |

| Known Direct Subclasses [UnicodeSet](../android/icu/text/UnicodeSet.md) |------------------------------------------------------------------------------------------|-----------------------------------------------------------------| | [UnicodeSet](../android/icu/text/UnicodeSet.md) | A mutable set of Unicode characters and multicharacter strings. | |
| --- | --- | --- | --- | --- | --- | --- |

`UnicodeFilter`defines a protocol for selecting a subset of the full range (U+0000 to U+FFFF) of Unicode characters. Currently, filters are used in conjunction with classes like [android.icu.text.Transliterator](../android/icu/text/Transliterator.md) to only process selected characters through a transformation.

## Summary

| Inherited constants ||
|---|---|
| From class [UnicodeMatcher](../android/icu/text/UnicodeMatcher.md) |------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | [ETHER](../android/icu/text/UnicodeMatcher.md) <br /> The character at index i, where i \< contextStart || i \>= contextLimit, is ETHER. This allows explicit matching by rules and UnicodeSets of text outside the context. In traditional terms, this allows anchoring at the start and/or end. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [U_MATCH](../android/icu/text/UnicodeMatcher.md) <br /> Constant returned by`matches()`indicating a complete match between the text and this matcher. For an incremental variable-length match, this value is returned if the given text matches, and it is known that additional characters would not alter the extent of the match. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [U_MISMATCH](../android/icu/text/UnicodeMatcher.md) <br /> Constant returned by`matches()`indicating a mismatch between the text and this matcher. The text contains a character which does not match, or the text does not contain all desired characters for a non-incremental match. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [U_PARTIAL_MATCH](../android/icu/text/UnicodeMatcher.md) <br /> Constant returned by`matches()`indicating a partial match between the text and this matcher. This value is only returned for incremental match operations. All characters of the text match, but more characters are required for a complete match. Alternatively, for variable-length matchers, all characters of the text match, and if more characters were supplied at limit, they might also match. <br /> | ||

| Public methods ||
|--------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [contains](../android/icu/text/UnicodeFilter.md))`(`c:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns true for characters that are in the selected subset. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [matches](../android/icu/text/UnicodeFilter.md))`(`text:` ` [Replaceable](../android/icu/text/Replaceable.md)!`, `offset:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!`, `limit:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `incremental:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Default implementation of UnicodeMatcher::matches() for Unicode filters. |

| Inherited functions ||
|---|---|
| From class [UnicodeMatcher](../android/icu/text/UnicodeMatcher.md) |------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addMatchSetTo](../android/icu/text/UnicodeMatcher.md))`(`toUnionTo:` ` [UnicodeSet](../android/icu/text/UnicodeSet.md)!`)` <br /> Union the set of all characters that may be matched by this object into the given set. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [matchesIndexValue](../android/icu/text/UnicodeMatcher.md))`(`v:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Returns true if this matcher will match a character c, where c \& 0xFF == v, at offset, in the forward direction (with limit \> offset). This is used by RuleBasedTransliterator for indexing. Note: This API uses an int even though the value will be restricted to 8 bits in order to avoid complications with signedness (bytes convert to ints in the range -128..127). <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [toPattern](../android/icu/text/UnicodeMatcher.md))`(`escapeUnprintable:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Returns a string representation of this matcher. If the result of calling this function is passed to the appropriate parser, it will produce another matcher that is equal to this one. <br /> | ||

## Public methods

### contains

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun contains(c: Int): Boolean
```

Returns true for characters that are in the selected subset. In other words, if a character is**to be filtered** , then contains() returns**false**. 

### matches

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun matches(
    text: Replaceable!, 
    offset: IntArray!, 
    limit: Int, 
    incremental: Boolean
): Int
```

Default implementation of UnicodeMatcher::matches() for Unicode filters. Matches a single 16-bit code unit at offset.

| Parameters ||
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `text` | [Replaceable](../android/icu/text/Replaceable.md)!:the text to be matched |
| `offset` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!:on input, the index into text at which to begin matching. On output, the limit of the matched text. The number of matched characters is the output value of offset minus the input value. Offset should always point to the HIGH SURROGATE (leading code unit) of a pair of surrogates, both on entry and upon return. |
| `limit` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the limit index of text to be matched. Greater than offset for a forward direction match, less than offset for a backward direction match. The last character to be considered for matching will be text.charAt(limit-1) in the forward direction or text.charAt(limit+1) in the backward direction. |
| --- | --- |
| `incremental` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):if true, then assume further characters may be inserted at limit and check for partial matching. Otherwise assume the text as given is complete. |

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a match degree value indicating a full match, a partial match, or a mismatch. If incremental is false then U_PARTIAL_MATCH should never be returned. |
