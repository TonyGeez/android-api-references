# UnicodeMatcher

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# UnicodeMatcher

Kotlin| [Java](https://developer.android.com/reference/android/icu/text/UnicodeMatcher "View this page in Java") 
| --- | --- |

```
interface UnicodeMatcher
```

| [android.icu.text.UnicodeMatcher](https://developer.android.com/reference/kotlin/android/icu/text/UnicodeMatcher#) |

| Known Direct Subclasses [UnicodeFilter](https://developer.android.com/reference/kotlin/android/icu/text/UnicodeFilter) |------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------| | [UnicodeFilter](https://developer.android.com/reference/kotlin/android/icu/text/UnicodeFilter) | `UnicodeFilter`defines a protocol for selecting a subset of the full range (U+0000 to U+FFFF) of Unicode characters. | |
| --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [UnicodeSet](https://developer.android.com/reference/kotlin/android/icu/text/UnicodeSet) |------------------------------------------------------------------------------------------|-----------------------------------------------------------------| | [UnicodeSet](https://developer.android.com/reference/kotlin/android/icu/text/UnicodeSet) | A mutable set of Unicode characters and multicharacter strings. | |
| --- | --- | --- | --- | --- | --- | --- |

`UnicodeMatcher`defines a protocol for objects that can match a range of characters in a Replaceable string.

## Summary

| Constants ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | [ETHER](https://developer.android.com/reference/kotlin/android/icu/text/UnicodeMatcher#ETHER:kotlin.Char) The character at index i, where i \< contextStart || i \>= contextLimit, is ETHER. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [U_MATCH](https://developer.android.com/reference/kotlin/android/icu/text/UnicodeMatcher#U_MATCH:kotlin.Int) Constant returned by`matches()`indicating a complete match between the text and this matcher. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [U_MISMATCH](https://developer.android.com/reference/kotlin/android/icu/text/UnicodeMatcher#U_MISMATCH:kotlin.Int) Constant returned by`matches()`indicating a mismatch between the text and this matcher. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [U_PARTIAL_MATCH](https://developer.android.com/reference/kotlin/android/icu/text/UnicodeMatcher#U_PARTIAL_MATCH:kotlin.Int) Constant returned by`matches()`indicating a partial match between the text and this matcher. |

| Public methods ||
|--------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addMatchSetTo](https://developer.android.com/reference/kotlin/android/icu/text/UnicodeMatcher#addMatchSetTo(android.icu.text.UnicodeSet))`(`toUnionTo:` ` [UnicodeSet](https://developer.android.com/reference/kotlin/android/icu/text/UnicodeSet)!`)` Union the set of all characters that may be matched by this object into the given set. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [matches](https://developer.android.com/reference/kotlin/android/icu/text/UnicodeMatcher#matches(android.icu.text.Replaceable,%20kotlin.IntArray,%20kotlin.Int,%20kotlin.Boolean))`(`text:` ` [Replaceable](https://developer.android.com/reference/kotlin/android/icu/text/Replaceable)!`, `offset:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!`, `limit:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `incremental:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Return a UMatchDegree value indicating the degree of match for the given text at the given offset. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [matchesIndexValue](https://developer.android.com/reference/kotlin/android/icu/text/UnicodeMatcher#matchesIndexValue(kotlin.Int))`(`v:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns true if this matcher will match a character c, where c \& 0xFF == v, at offset, in the forward direction (with limit \> offset). |
| --- | --- |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [toPattern](https://developer.android.com/reference/kotlin/android/icu/text/UnicodeMatcher#toPattern(kotlin.Boolean))`(`escapeUnprintable:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Returns a string representation of this matcher. |

## Constants

### ETHER

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ETHER: Char
```

The character at index i, where i \< contextStart || i \>= contextLimit, is ETHER. This allows explicit matching by rules and UnicodeSets of text outside the context. In traditional terms, this allows anchoring at the start and/or end. 
| --- | --- | --- |

 Value: '\uffff'

### U_MATCH

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val U_MATCH: Int
```

Constant returned by`matches()`indicating a complete match between the text and this matcher. For an incremental variable-length match, this value is returned if the given text matches, and it is known that additional characters would not alter the extent of the match. 

 Value: 2

### U_MISMATCH

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val U_MISMATCH: Int
```

Constant returned by`matches()`indicating a mismatch between the text and this matcher. The text contains a character which does not match, or the text does not contain all desired characters for a non-incremental match. 

 Value: 0

### U_PARTIAL_MATCH

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val U_PARTIAL_MATCH: Int
```

Constant returned by`matches()`indicating a partial match between the text and this matcher. This value is only returned for incremental match operations. All characters of the text match, but more characters are required for a complete match. Alternatively, for variable-length matchers, all characters of the text match, and if more characters were supplied at limit, they might also match. 

 Value: 1

## Public methods

### addMatchSetTo

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun addMatchSetTo(toUnionTo: UnicodeSet!): Unit
```

Union the set of all characters that may be matched by this object into the given set.

| Parameters ||
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| `toUnionTo` | [UnicodeSet](https://developer.android.com/reference/kotlin/android/icu/text/UnicodeSet)!:the set into which to union the source characters |

### matches

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun matches(
    text: Replaceable!, 
    offset: IntArray!, 
    limit: Int, 
    incremental: Boolean
): Int
```

Return a UMatchDegree value indicating the degree of match for the given text at the given offset. Zero, one, or more characters may be matched. Matching in the forward direction is indicated by limit \> offset. Characters from offset forwards to limit-1 will be considered for matching. Matching in the reverse direction is indicated by limit \< offset. Characters from offset backwards to limit+1 will be considered for matching. If limit == offset then the only match possible is a zero character match (which subclasses may implement if desired). If U_MATCH is returned, then as a side effect, advance the offset parameter to the limit of the matched substring. In the forward direction, this will be the index of the last matched character plus one. In the reverse direction, this will be the index of the last matched character minus one.

| Parameters ||
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `text` | [Replaceable](https://developer.android.com/reference/kotlin/android/icu/text/Replaceable)!:the text to be matched |
| `offset` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!:on input, the index into text at which to begin matching. On output, the limit of the matched text. The number of matched characters is the output value of offset minus the input value. Offset should always point to the HIGH SURROGATE (leading code unit) of a pair of surrogates, both on entry and upon return. |
| `limit` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the limit index of text to be matched. Greater than offset for a forward direction match, less than offset for a backward direction match. The last character to be considered for matching will be text.charAt(limit-1) in the forward direction or text.charAt(limit+1) in the backward direction. |
| --- | --- |
| `incremental` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):if true, then assume further characters may be inserted at limit and check for partial matching. Otherwise assume the text as given is complete. |

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a match degree value indicating a full match, a partial match, or a mismatch. If incremental is false then U_PARTIAL_MATCH should never be returned. |

### matchesIndexValue

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun matchesIndexValue(v: Int): Boolean
```

Returns true if this matcher will match a character c, where c \& 0xFF == v, at offset, in the forward direction (with limit \> offset). This is used by RuleBasedTransliterator for indexing.

Note: This API uses an int even though the value will be restricted to 8 bits in order to avoid complications with signedness (bytes convert to ints in the range -128..127). 

### toPattern

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun toPattern(escapeUnprintable: Boolean): String!
```

Returns a string representation of this matcher. If the result of calling this function is passed to the appropriate parser, it will produce another matcher that is equal to this one.

| Parameters ||
|---------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `escapeUnprintable` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):if true then convert unprintable character to their hex escape representations, \\\\uxxxx or \\\\Uxxxxxxxx. Unprintable characters are those other than U+000A, U+0020..U+007E. |
