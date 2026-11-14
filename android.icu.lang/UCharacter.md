# UCharacter

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# UCharacter

Kotlin| [Java](../android/icu/lang/UCharacter.md) 
| --- | --- |

```
class UCharacter : UCharacterEnums.ECharacterCategory, UCharacterEnums.ECharacterDirection
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.icu.lang.UCharacter](../android/icu/lang/UCharacter.md) |

**\[icu enhancement\]** ICU's replacement for [java.lang.Character](../java/lang/Character.md). Methods, fields, and other functionality specific to ICU are labeled '**\[icu\]**'.

The UCharacter class provides extensions to the [java.lang.Character](../java/lang/Character.md) class. These extensions provide support for more Unicode properties. Each ICU release supports the latest version of Unicode available at that time.

For some time before Java 5 added support for supplementary Unicode code points, The ICU UCharacter class and many other ICU classes already supported them. Some UCharacter methods and constants were widened slightly differently than how the Character class methods and constants were widened later. In particular, [Character.MAX_VALUE](../java/lang/Character.md) is still a char with the value U+FFFF, while the [UCharacter.MAX_VALUE](../android/icu/lang/UCharacter.md) is an int with the value U+10FFFF.

Code points are represented in these API using ints. While it would be more convenient in Java to have a separate primitive datatype for them, ints suffice in the meantime.

Aside from the additions for UTF-16 support, and the updated Unicode properties, the main differences between UCharacter and Character are:

- UCharacter is not designed to be a char wrapper and does not have APIs to which involves management of that single char. 
 These include:
 - char charValue(),
 - int compareTo(java.lang.Character, java.lang.Character), etc.
- UCharacter does not include Character APIs that are deprecated, nor does it include the Java-specific character information, such as boolean isJavaIdentifierPart(char ch).
- Character maps characters 'A' - 'Z' and 'a' - 'z' to the numeric values '10' - '35'. UCharacter also does this in digit and getNumericValue, to adhere to the java semantics of these methods. New methods unicodeDigit, and getUnicodeNumericValue do not treat the above code points as having numeric values. This is a semantic change from ICU4J 1.3.1.

In addition to Java compatibility functions, which calculate derived properties, this API provides low-level access to the Unicode Character Database.

Unicode assigns each code point (not just assigned character) values for many properties. Most of them are simple boolean flags, or constants from a small enumerated list. For some properties, values are strings or other relatively more complex types.

For more information see ["About the Unicode Character Database"](http://www.unicode/org/ucd/)(http://www.unicode.org/ucd/) and the [ICU User Guide chapter on Properties](https://unicode-org.github.io/icu/userguide/strings/properties)(https://unicode-org.github.io/icu/userguide/strings/properties).

There are also functions that provide easy migration from C/POSIX functions like isblank(). Their use is generally discouraged because the C/POSIX standards do not define their semantics beyond the ASCII range, which means that different implementations exhibit very different behavior. Instead, Unicode properties should be used directly.

There are also only a few, broad C/POSIX character classes, and they tend to be used for conflicting purposes. For example, the "isalpha()" class is sometimes used to determine word boundaries, while a more sophisticated approach would at least distinguish initial letters from continuation characters (the latter including combining marks). (In ICU, BreakIterator is the most sophisticated API for word boundaries.) Another example: There is no "istitle()" class for titlecase characters.

ICU 3.4 and later provides API access for all twelve C/POSIX character classes. ICU implements them according to the Standard Recommendations in Annex C: Compatibility Properties of UTS #18 Unicode Regular Expressions (http://www.unicode.org/reports/tr18/#Compatibility_Properties).

API access for C/POSIX character classes is as follows: 

```kotlin
<code>- alpha:     isUAlphabetic(c) or hasBinaryProperty(c, UProperty.ALPHABETIC)
  - lower:     isULowercase(c) or hasBinaryProperty(c, UProperty.LOWERCASE)
  - upper:     isUUppercase(c) or hasBinaryProperty(c, UProperty.UPPERCASE)
  - punct:     ((1&lt;&lt;getType(c)) &amp; ((1&lt;&lt;DASH_PUNCTUATION)|(1&lt;&lt;START_PUNCTUATION)|
                (1&lt;&lt;END_PUNCTUATION)|(1&lt;&lt;CONNECTOR_PUNCTUATION)|(1&lt;&lt;OTHER_PUNCTUATION)|
                (1&lt;&lt;INITIAL_PUNCTUATION)|(1&lt;&lt;FINAL_PUNCTUATION)))!=0
  - digit:     isDigit(c) or getType(c)==DECIMAL_DIGIT_NUMBER
  - xdigit:    hasBinaryProperty(c, UProperty.POSIX_XDIGIT)
  - alnum:     hasBinaryProperty(c, UProperty.POSIX_ALNUM)
  - space:     isUWhiteSpace(c) or hasBinaryProperty(c, UProperty.WHITE_SPACE)
  - blank:     hasBinaryProperty(c, UProperty.POSIX_BLANK)
  - cntrl:     getType(c)==CONTROL
  - graph:     hasBinaryProperty(c, UProperty.POSIX_GRAPH)
  - print:     hasBinaryProperty(c, UProperty.POSIX_PRINT)</code>
```

The C/POSIX character classes are also available in UnicodeSet patterns, using patterns like \[:graph:\] or \\p{graph}.

**\[icu\] Note:**There are several ICU (and Java) whitespace functions. Comparison:

- isUWhiteSpace=UCHAR_WHITE_SPACE: Unicode White_Space property; most of general categories "Z" (separators) + most whitespace ISO controls (including no-break spaces, but excluding IS1..IS4)
- isWhitespace: Java isWhitespace; Z + whitespace ISO controls but excluding no-break spaces
- isSpaceChar: just Z (including no-break spaces)

This class is not subclassable.

## Summary

| Nested classes ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [BidiPairedBracketType](../android/icu/lang/UCharacter.BidiPairedBracketType.md) Bidi Paired Bracket Type constants. |
| abstract | [DecompositionType](../android/icu/lang/UCharacter.DecompositionType.md) Decomposition Type constants. |
| abstract | [EastAsianWidth](../android/icu/lang/UCharacter.EastAsianWidth.md) East Asian Width constants. |
| --- | --- |
| abstract | [GraphemeClusterBreak](../android/icu/lang/UCharacter.GraphemeClusterBreak.md) Grapheme Cluster Break constants. |
| abstract | [HangulSyllableType](../android/icu/lang/UCharacter.HangulSyllableType.md) Hangul Syllable Type constants. |
| abstract | [IndicPositionalCategory](../android/icu/lang/UCharacter.IndicPositionalCategory.md) Indic Positional Category constants. |
| --- | --- |
| abstract | [IndicSyllabicCategory](../android/icu/lang/UCharacter.IndicSyllabicCategory.md) Indic Syllabic Category constants. |
| abstract | [JoiningGroup](../android/icu/lang/UCharacter.JoiningGroup.md) Joining Group constants. |
| abstract | [JoiningType](../android/icu/lang/UCharacter.JoiningType.md) Joining Type constants. |
| --- | --- |
| abstract | [LineBreak](../android/icu/lang/UCharacter.LineBreak.md) Line Break constants. |
| abstract | [NumericType](../android/icu/lang/UCharacter.NumericType.md) Numeric Type constants. |
| abstract | [SentenceBreak](../android/icu/lang/UCharacter.SentenceBreak.md) Sentence Break constants. |
| --- | --- |
| | [UnicodeBlock](../android/icu/lang/UCharacter.UnicodeBlock.md) **\[icu enhancement\]** ICU's replacement for [java.lang.Character.UnicodeBlock](../java/lang/Character.UnicodeBlock.md). |
| abstract | [VerticalOrientation](../android/icu/lang/UCharacter.VerticalOrientation.md) Vertical Orientation constants. |
| abstract | [WordBreak](../android/icu/lang/UCharacter.WordBreak.md) Word Break constants. |
| --- | --- |

| Constants ||
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FOLD_CASE_DEFAULT](../android/icu/lang/UCharacter.md) **\[icu\]**Option value for case folding: use default mappings defined in CaseFolding. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FOLD_CASE_EXCLUDE_SPECIAL_I](../android/icu/lang/UCharacter.md) **\[icu\]**Option value for case folding: Use the modified set of mappings provided in CaseFolding. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MAX_CODE_POINT](../android/icu/lang/UCharacter.md) Constant U+10FFFF, same as [Character.MAX_CODE_POINT](../java/lang/Character.md). |
| --- | --- |
| static [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | [MAX_HIGH_SURROGATE](../android/icu/lang/UCharacter.md) Constant U+DBFF, same as [Character.MAX_HIGH_SURROGATE](../java/lang/Character.md). |
| static [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | [MAX_LOW_SURROGATE](../android/icu/lang/UCharacter.md) Constant U+DFFF, same as [Character.MAX_LOW_SURROGATE](../java/lang/Character.md). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MAX_RADIX](../android/icu/lang/UCharacter.md) Compatibility constant for Java Character's MAX_RADIX. |
| --- | --- |
| static [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | [MAX_SURROGATE](../android/icu/lang/UCharacter.md) Constant U+DFFF, same as [Character.MAX_SURROGATE](../java/lang/Character.md). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MAX_VALUE](../android/icu/lang/UCharacter.md) The highest Unicode code point value (scalar value), constant U+10FFFF (uses 21 bits). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MIN_CODE_POINT](../android/icu/lang/UCharacter.md) Constant U+0000, same as [Character.MIN_CODE_POINT](../java/lang/Character.md). |
| --- | --- |
| static [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | [MIN_HIGH_SURROGATE](../android/icu/lang/UCharacter.md) Constant U+D800, same as [Character.MIN_HIGH_SURROGATE](../java/lang/Character.md). |
| static [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | [MIN_LOW_SURROGATE](../android/icu/lang/UCharacter.md) Constant U+DC00, same as [Character.MIN_LOW_SURROGATE](../java/lang/Character.md). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MIN_RADIX](../android/icu/lang/UCharacter.md) Compatibility constant for Java Character's MIN_RADIX. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MIN_SUPPLEMENTARY_CODE_POINT](../android/icu/lang/UCharacter.md) Constant U+10000, same as [Character.MIN_SUPPLEMENTARY_CODE_POINT](../java/lang/Character.md). |
| static [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | [MIN_SURROGATE](../android/icu/lang/UCharacter.md) Constant U+D800, same as [Character.MIN_SURROGATE](../java/lang/Character.md). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MIN_VALUE](../android/icu/lang/UCharacter.md) The lowest Unicode code point value, constant 0. |
| --- | --- |
| static [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [NO_NUMERIC_VALUE](../android/icu/lang/UCharacter.md) Special value that is returned by getUnicodeNumericValue(int) when no numeric value is defined for a code point. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [REPLACEMENT_CHAR](../android/icu/lang/UCharacter.md) Unicode value used when translating into Unicode encoding form and there is no existing character. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SUPPLEMENTARY_MIN_VALUE](../android/icu/lang/UCharacter.md) The minimum value for Supplementary code points, constant U+10000. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TITLECASE_NO_BREAK_ADJUSTMENT](../android/icu/lang/UCharacter.md) Do not adjust the titlecasing indexes from BreakIterator::next() indexes; titlecase exactly the characters at breaks from the iterator. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TITLECASE_NO_LOWERCASE](../android/icu/lang/UCharacter.md) Do not lowercase non-initial parts of words when titlecasing. |

| Inherited constants ||
|---|---|
| From class [ECharacterDirection](../android/icu/lang/UCharacterEnums.ECharacterDirection.md) |------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ARABIC_NUMBER](../android/icu/lang/UCharacterEnums.ECharacterDirection.md) <br /> Directional type AN <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BLOCK_SEPARATOR](../android/icu/lang/UCharacterEnums.ECharacterDirection.md) <br /> Directional type B <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BOUNDARY_NEUTRAL](../android/icu/lang/UCharacterEnums.ECharacterDirection.md) <br /> Directional type BN <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [COMMON_NUMBER_SEPARATOR](../android/icu/lang/UCharacterEnums.ECharacterDirection.md) <br /> Directional type CS <br /> | | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [DIRECTIONALITY_ARABIC_NUMBER](../android/icu/lang/UCharacterEnums.ECharacterDirection.md) <br /> Equivalent to [java.lang.Character#DIRECTIONALITY_ARABIC_NUMBER](../java/lang/Character.md). Synonym of [ARABIC_NUMBER](../android/icu/lang/UCharacterEnums.ECharacterDirection.md). <br /> | | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [DIRECTIONALITY_BOUNDARY_NEUTRAL](../android/icu/lang/UCharacterEnums.ECharacterDirection.md) <br /> Equivalent to [java.lang.Character#DIRECTIONALITY_BOUNDARY_NEUTRAL](../java/lang/Character.md). Synonym of [BOUNDARY_NEUTRAL](../android/icu/lang/UCharacterEnums.ECharacterDirection.md). <br /> | | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [DIRECTIONALITY_COMMON_NUMBER_SEPARATOR](../android/icu/lang/UCharacterEnums.ECharacterDirection.md) <br /> Equivalent to [java.lang.Character#DIRECTIONALITY_COMMON_NUMBER_SEPARATOR](../java/lang/Character.md). Synonym of [COMMON_NUMBER_SEPARATOR](../android/icu/lang/UCharacterEnums.ECharacterDirection.md). <br /> | | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [DIRECTIONALITY_EUROPEAN_NUMBER](../android/icu/lang/UCharacterEnums.ECharacterDirection.md) <br /> Equivalent to [java.lang.Character#DIRECTIONALITY_EUROPEAN_NUMBER](../java/lang/Character.md). Synonym of [EUROPEAN_NUMBER](../android/icu/lang/UCharacterEnums.ECharacterDirection.md). <br /> | | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [DIRECTIONALITY_EUROPEAN_NUMBER_SEPARATOR](../android/icu/lang/UCharacterEnums.ECharacterDirection.md) <br /> Equivalent to [java.lang.Character#DIRECTIONALITY_EUROPEAN_NUMBER_SEPARATOR](../java/lang/Character.md). Synonym of [EUROPEAN_NUMBER_SEPARATOR](../android/icu/lang/UCharacterEnums.ECharacterDirection.md). <br /> | | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [DIRECTIONALITY_EUROPEAN_NUMBER_TERMINATOR](../android/icu/lang/UCharacterEnums.ECharacterDirection.md) <br /> Equivalent to [java.lang.Character#DIRECTIONALITY_EUROPEAN_NUMBER_TERMINATOR](../java/lang/Character.md). Synonym of [EUROPEAN_NUMBER_TERMINATOR](../android/icu/lang/UCharacterEnums.ECharacterDirection.md). <br /> | | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [DIRECTIONALITY_LEFT_TO_RIGHT](../android/icu/lang/UCharacterEnums.ECharacterDirection.md) <br /> Equivalent to [java.lang.Character#DIRECTIONALITY_LEFT_TO_RIGHT](../java/lang/Character.md). Synonym of [LEFT_TO_RIGHT](../android/icu/lang/UCharacterEnums.ECharacterDirection.md). <br /> | | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [DIRECTIONALITY_LEFT_TO_RIGHT_EMBEDDING](../android/icu/lang/UCharacterEnums.ECharacterDirection.md) <br /> Equivalent to [java.lang.Character#DIRECTIONALITY_LEFT_TO_RIGHT_EMBEDDING](../java/lang/Character.md). Synonym of [LEFT_TO_RIGHT_EMBEDDING](../android/icu/lang/UCharacterEnums.ECharacterDirection.md). <br /> | | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [DIRECTIONALITY_LEFT_TO_RIGHT_OVERRIDE](../android/icu/lang/UCharacterEnums.ECharacterDirection.md) <br /> Equivalent to [java.lang.Character#DIRECTIONALITY_LEFT_TO_RIGHT_OVERRIDE](../java/lang/Character.md). Synonym of [LEFT_TO_RIGHT_OVERRIDE](../android/icu/lang/UCharacterEnums.ECharacterDirection.md). <br /> | | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [DIRECTIONALITY_NONSPACING_MARK](../android/icu/lang/UCharacterEnums.ECharacterDirection.md) <br /> Equivalent to [java.lang.Character#DIRECTIONALITY_NONSPACING_MARK](../java/lang/Character.md). Synonym of [DIR_NON_SPACING_MARK](../android/icu/lang/UCharacterEnums.ECharacterDirection.md). <br /> | | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [DIRECTIONALITY_OTHER_NEUTRALS](../android/icu/lang/UCharacterEnums.ECharacterDirection.md) <br /> Equivalent to [java.lang.Character#DIRECTIONALITY_OTHER_NEUTRALS](../java/lang/Character.md). Synonym of [OTHER_NEUTRAL](../android/icu/lang/UCharacterEnums.ECharacterDirection.md). <br /> | | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [DIRECTIONALITY_PARAGRAPH_SEPARATOR](../android/icu/lang/UCharacterEnums.ECharacterDirection.md) <br /> Equivalent to [java.lang.Character#DIRECTIONALITY_PARAGRAPH_SEPARATOR](../java/lang/Character.md). Synonym of [BLOCK_SEPARATOR](../android/icu/lang/UCharacterEnums.ECharacterDirection.md). <br /> | | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [DIRECTIONALITY_POP_DIRECTIONAL_FORMAT](../android/icu/lang/UCharacterEnums.ECharacterDirection.md) <br /> Equivalent to [java.lang.Character#DIRECTIONALITY_POP_DIRECTIONAL_FORMAT](../java/lang/Character.md). Synonym of [POP_DIRECTIONAL_FORMAT](../android/icu/lang/UCharacterEnums.ECharacterDirection.md). <br /> | | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [DIRECTIONALITY_RIGHT_TO_LEFT](../android/icu/lang/UCharacterEnums.ECharacterDirection.md) <br /> Equivalent to [java.lang.Character#DIRECTIONALITY_RIGHT_TO_LEFT](../java/lang/Character.md). Synonym of [RIGHT_TO_LEFT](../android/icu/lang/UCharacterEnums.ECharacterDirection.md). <br /> | | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [DIRECTIONALITY_RIGHT_TO_LEFT_ARABIC](../android/icu/lang/UCharacterEnums.ECharacterDirection.md) <br /> Equivalent to [java.lang.Character#DIRECTIONALITY_RIGHT_TO_LEFT_ARABIC](../java/lang/Character.md). Synonym of [RIGHT_TO_LEFT_ARABIC](../android/icu/lang/UCharacterEnums.ECharacterDirection.md). <br /> | | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [DIRECTIONALITY_RIGHT_TO_LEFT_EMBEDDING](../android/icu/lang/UCharacterEnums.ECharacterDirection.md) <br /> Equivalent to [java.lang.Character#DIRECTIONALITY_RIGHT_TO_LEFT_EMBEDDING](../java/lang/Character.md). Synonym of [RIGHT_TO_LEFT_EMBEDDING](../android/icu/lang/UCharacterEnums.ECharacterDirection.md). <br /> | | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [DIRECTIONALITY_RIGHT_TO_LEFT_OVERRIDE](../android/icu/lang/UCharacterEnums.ECharacterDirection.md) <br /> Equivalent to [java.lang.Character#DIRECTIONALITY_RIGHT_TO_LEFT_OVERRIDE](../java/lang/Character.md). Synonym of [RIGHT_TO_LEFT_OVERRIDE](../android/icu/lang/UCharacterEnums.ECharacterDirection.md). <br /> | | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [DIRECTIONALITY_SEGMENT_SEPARATOR](../android/icu/lang/UCharacterEnums.ECharacterDirection.md) <br /> Equivalent to [java.lang.Character#DIRECTIONALITY_SEGMENT_SEPARATOR](../java/lang/Character.md). Synonym of [SEGMENT_SEPARATOR](../android/icu/lang/UCharacterEnums.ECharacterDirection.md). <br /> | | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [DIRECTIONALITY_UNDEFINED](../android/icu/lang/UCharacterEnums.ECharacterDirection.md) <br /> Undefined bidirectional character type. Undefined`char`values have undefined directionality in the Unicode specification. <br /> | | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [DIRECTIONALITY_WHITESPACE](../android/icu/lang/UCharacterEnums.ECharacterDirection.md) <br /> Equivalent to [java.lang.Character#DIRECTIONALITY_WHITESPACE](../java/lang/Character.md). Synonym of [WHITE_SPACE_NEUTRAL](../android/icu/lang/UCharacterEnums.ECharacterDirection.md). <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DIR_NON_SPACING_MARK](../android/icu/lang/UCharacterEnums.ECharacterDirection.md) <br /> Directional type NSM <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EUROPEAN_NUMBER](../android/icu/lang/UCharacterEnums.ECharacterDirection.md) <br /> Directional type EN <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EUROPEAN_NUMBER_SEPARATOR](../android/icu/lang/UCharacterEnums.ECharacterDirection.md) <br /> Directional type ES <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EUROPEAN_NUMBER_TERMINATOR](../android/icu/lang/UCharacterEnums.ECharacterDirection.md) <br /> Directional type ET <br /> | | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [FIRST_STRONG_ISOLATE](../android/icu/lang/UCharacterEnums.ECharacterDirection.md) <br /> Directional type FSI <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LEFT_TO_RIGHT](../android/icu/lang/UCharacterEnums.ECharacterDirection.md) <br /> Directional type L <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LEFT_TO_RIGHT_EMBEDDING](../android/icu/lang/UCharacterEnums.ECharacterDirection.md) <br /> Directional type LRE <br /> | | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [LEFT_TO_RIGHT_ISOLATE](../android/icu/lang/UCharacterEnums.ECharacterDirection.md) <br /> Directional type LRI <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LEFT_TO_RIGHT_OVERRIDE](../android/icu/lang/UCharacterEnums.ECharacterDirection.md) <br /> Directional type LRO <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [OTHER_NEUTRAL](../android/icu/lang/UCharacterEnums.ECharacterDirection.md) <br /> Directional type ON <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [POP_DIRECTIONAL_FORMAT](../android/icu/lang/UCharacterEnums.ECharacterDirection.md) <br /> Directional type PDF <br /> | | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [POP_DIRECTIONAL_ISOLATE](../android/icu/lang/UCharacterEnums.ECharacterDirection.md) <br /> Directional type PDI <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RIGHT_TO_LEFT](../android/icu/lang/UCharacterEnums.ECharacterDirection.md) <br /> Directional type R <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RIGHT_TO_LEFT_ARABIC](../android/icu/lang/UCharacterEnums.ECharacterDirection.md) <br /> Directional type AL <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RIGHT_TO_LEFT_EMBEDDING](../android/icu/lang/UCharacterEnums.ECharacterDirection.md) <br /> Directional type RLE <br /> | | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [RIGHT_TO_LEFT_ISOLATE](../android/icu/lang/UCharacterEnums.ECharacterDirection.md) <br /> Directional type RLI <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RIGHT_TO_LEFT_OVERRIDE](../android/icu/lang/UCharacterEnums.ECharacterDirection.md) <br /> Directional type RLO <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SEGMENT_SEPARATOR](../android/icu/lang/UCharacterEnums.ECharacterDirection.md) <br /> Directional type S <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [WHITE_SPACE_NEUTRAL](../android/icu/lang/UCharacterEnums.ECharacterDirection.md) <br /> Directional type WS <br /> | ||
| From class [ECharacterCategory](../android/icu/lang/UCharacterEnums.ECharacterCategory.md) |------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [COMBINING_SPACING_MARK](../android/icu/lang/UCharacterEnums.ECharacterCategory.md) <br /> Character type Mc <br /> | | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [CONNECTOR_PUNCTUATION](../android/icu/lang/UCharacterEnums.ECharacterCategory.md) <br /> Character type Pc <br /> | | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [CONTROL](../android/icu/lang/UCharacterEnums.ECharacterCategory.md) <br /> Character type Cc <br /> | | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [CURRENCY_SYMBOL](../android/icu/lang/UCharacterEnums.ECharacterCategory.md) <br /> Character type Sc <br /> | | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [DASH_PUNCTUATION](../android/icu/lang/UCharacterEnums.ECharacterCategory.md) <br /> Character type Pd <br /> | | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [DECIMAL_DIGIT_NUMBER](../android/icu/lang/UCharacterEnums.ECharacterCategory.md) <br /> Character type Nd <br /> | | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [ENCLOSING_MARK](../android/icu/lang/UCharacterEnums.ECharacterCategory.md) <br /> Character type Me <br /> | | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [END_PUNCTUATION](../android/icu/lang/UCharacterEnums.ECharacterCategory.md) <br /> Character type Pe <br /> | | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [FINAL_PUNCTUATION](../android/icu/lang/UCharacterEnums.ECharacterCategory.md) <br /> Character type Pf <br /> | | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [FINAL_QUOTE_PUNCTUATION](../android/icu/lang/UCharacterEnums.ECharacterCategory.md) <br /> Character type Pf This name is compatible with java.lang.Character's name for this type. <br /> | | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [FORMAT](../android/icu/lang/UCharacterEnums.ECharacterCategory.md) <br /> Character type Cf <br /> | | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [GENERAL_OTHER_TYPES](../android/icu/lang/UCharacterEnums.ECharacterCategory.md) <br /> Character type Cn Not Assigned (no characters in \[UnicodeData.txt\] have this property) <br /> | | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [INITIAL_PUNCTUATION](../android/icu/lang/UCharacterEnums.ECharacterCategory.md) <br /> Character type Pi <br /> | | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [INITIAL_QUOTE_PUNCTUATION](../android/icu/lang/UCharacterEnums.ECharacterCategory.md) <br /> Character type Pi This name is compatible with java.lang.Character's name for this type. <br /> | | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [LETTER_NUMBER](../android/icu/lang/UCharacterEnums.ECharacterCategory.md) <br /> Character type Nl <br /> | | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [LINE_SEPARATOR](../android/icu/lang/UCharacterEnums.ECharacterCategory.md) <br /> Character type Zl <br /> | | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [LOWERCASE_LETTER](../android/icu/lang/UCharacterEnums.ECharacterCategory.md) <br /> Character type Ll <br /> | | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [MATH_SYMBOL](../android/icu/lang/UCharacterEnums.ECharacterCategory.md) <br /> Character type Sm <br /> | | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [MODIFIER_LETTER](../android/icu/lang/UCharacterEnums.ECharacterCategory.md) <br /> Character type Lm <br /> | | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [MODIFIER_SYMBOL](../android/icu/lang/UCharacterEnums.ECharacterCategory.md) <br /> Character type Sk <br /> | | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [NON_SPACING_MARK](../android/icu/lang/UCharacterEnums.ECharacterCategory.md) <br /> Character type Mn <br /> | | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [OTHER_LETTER](../android/icu/lang/UCharacterEnums.ECharacterCategory.md) <br /> Character type Lo <br /> | | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [OTHER_NUMBER](../android/icu/lang/UCharacterEnums.ECharacterCategory.md) <br /> Character type No <br /> | | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [OTHER_PUNCTUATION](../android/icu/lang/UCharacterEnums.ECharacterCategory.md) <br /> Character type Po <br /> | | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [OTHER_SYMBOL](../android/icu/lang/UCharacterEnums.ECharacterCategory.md) <br /> Character type So <br /> | | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [PARAGRAPH_SEPARATOR](../android/icu/lang/UCharacterEnums.ECharacterCategory.md) <br /> Character type Zp <br /> | | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [PRIVATE_USE](../android/icu/lang/UCharacterEnums.ECharacterCategory.md) <br /> Character type Co <br /> | | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [SPACE_SEPARATOR](../android/icu/lang/UCharacterEnums.ECharacterCategory.md) <br /> Character type Zs <br /> | | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [START_PUNCTUATION](../android/icu/lang/UCharacterEnums.ECharacterCategory.md) <br /> Character type Ps <br /> | | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [SURROGATE](../android/icu/lang/UCharacterEnums.ECharacterCategory.md) <br /> Character type Cs <br /> | | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [TITLECASE_LETTER](../android/icu/lang/UCharacterEnums.ECharacterCategory.md) <br /> Character type Lt <br /> | | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [UNASSIGNED](../android/icu/lang/UCharacterEnums.ECharacterCategory.md) <br /> Unassigned character type <br /> | | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [UPPERCASE_LETTER](../android/icu/lang/UCharacterEnums.ECharacterCategory.md) <br /> Character type Lu <br /> | ||

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [charCount](../android/icu/lang/UCharacter.md))`(`cp:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Same as [Character.charCount](../java/lang/Character.md)). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [codePointAt](../android/icu/lang/UCharacter.md))`(`text:` ` [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!`, `index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Same as[Character.codePointAt(char[], int)](https://developer.android.com/reference/kotlin/java/lang/Character.html#codePointAt(kotlin.CharArray,%20kotlin.Int)). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [codePointAt](../android/icu/lang/UCharacter.md))`(`text:` ` [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!`, `index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `limit:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Same as[Character.codePointAt(char[], int, int)](https://developer.android.com/reference/kotlin/java/lang/Character.html#codePointAt(kotlin.CharArray,%20kotlin.Int,%20kotlin.Int)). |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [codePointAt](../android/icu/lang/UCharacter.md))`(`seq:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Same as [Character.codePointAt(CharSequence, int)](../java/lang/Character.md)). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [codePointBefore](../android/icu/lang/UCharacter.md))`(`text:` ` [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!`, `index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Same as[Character.codePointBefore(char[], int)](https://developer.android.com/reference/kotlin/java/lang/Character.html#codePointBefore(kotlin.CharArray,%20kotlin.Int)). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [codePointBefore](../android/icu/lang/UCharacter.md))`(`text:` ` [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!`, `index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `limit:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Same as[Character.codePointBefore(char[], int, int)](https://developer.android.com/reference/kotlin/java/lang/Character.html#codePointBefore(kotlin.CharArray,%20kotlin.Int,%20kotlin.Int)). |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [codePointBefore](../android/icu/lang/UCharacter.md))`(`seq:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Same as [Character.codePointBefore(CharSequence, int)](../java/lang/Character.md)). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [codePointCount](../android/icu/lang/UCharacter.md))`(`text:` ` [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!`, `start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `limit:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Equivalent to the[Character.codePointCount(char[], int, int)](https://developer.android.com/reference/kotlin/java/lang/Character.html#codePointCount(kotlin.CharArray,%20kotlin.Int,%20kotlin.Int))method, for convenience. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [codePointCount](../android/icu/lang/UCharacter.md))`(`text:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `limit:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Equivalent to the [Character.codePointCount(CharSequence, int, int)](../java/lang/Character.md))method, for convenience. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [digit](../android/icu/lang/UCharacter.md))`(`ch:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returnss the numeric value of a decimal digit code point. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [digit](../android/icu/lang/UCharacter.md))`(`ch:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `radix:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returnss the numeric value of a decimal digit code point. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [foldCase](../android/icu/lang/UCharacter.md))`(`ch:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `defaultmapping:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` **\[icu\]**The given character is mapped to its case folding equivalent according to UnicodeData. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [foldCase](../android/icu/lang/UCharacter.md))`(`ch:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `options:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` **\[icu\]**The given character is mapped to its case folding equivalent according to UnicodeData. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [foldCase](../android/icu/lang/UCharacter.md))`(`str:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `defaultmapping:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` **\[icu\]**The given string is mapped to its case folding equivalent according to UnicodeData. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [foldCase](../android/icu/lang/UCharacter.md))`(`str:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `options:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` **\[icu\]**The given string is mapped to its case folding equivalent according to UnicodeData. |
| --- | --- |
| static [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | [forDigit](../android/icu/lang/UCharacter.md))`(`digit:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `radix:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Provide the java. |
| static [VersionInfo](../android/icu/util/VersionInfo.md)! | [getAge](../android/icu/lang/UCharacter.md))`(`ch:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` **\[icu\]**Returns the "age" of the code point. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getBidiPairedBracket](../android/icu/lang/UCharacter.md))`(`c:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` **\[icu\]**Maps the specified character to its paired bracket character. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getCharFromExtendedName](../android/icu/lang/UCharacter.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` **\[icu\]** |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getCharFromName](../android/icu/lang/UCharacter.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` **\[icu\]** |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getCharFromNameAlias](../android/icu/lang/UCharacter.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` **\[icu\]** |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getCodePoint](../android/icu/lang/UCharacter.md))`(`char16:` ` [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)`)` **\[icu\]**Returns the code point corresponding to the BMP code point. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getCodePoint](../android/icu/lang/UCharacter.md))`(`lead:` ` [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)`, `trail:` ` [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)`)` **\[icu\]**Returns a code point corresponding to the two surrogate code units. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getCodePoint](../android/icu/lang/UCharacter.md))`(`lead:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `trail:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` **\[icu\]**Returns a code point corresponding to the two surrogate code units. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getCombiningClass](../android/icu/lang/UCharacter.md))`(`ch:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` **\[icu\]**Returns the combining class of the argument codepoint |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDirection](../android/icu/lang/UCharacter.md))`(`ch:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` **\[icu\]**Returns the Bidirection property of a code point. |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [getDirectionality](../android/icu/lang/UCharacter.md))`(`cp:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Equivalent to the [Character.getDirectionality(char)](../java/lang/Character.md))method, for convenience. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getExtendedName](../android/icu/lang/UCharacter.md))`(`ch:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` **\[icu\]**Returns a name for a valid codepoint. |
| static [ValueIterator](../android/icu/util/ValueIterator.md)! | [getExtendedNameIterator](../android/icu/lang/UCharacter.md))`()` **\[icu\]** |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getHanNumericValue](../android/icu/lang/UCharacter.md))`(`ch:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` **\[icu\]**Returns the numeric value of a Han character. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getIntPropertyMaxValue](../android/icu/lang/UCharacter.md))`(`type:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` **\[icu\]**Returns the maximum value for an integer/binary Unicode property. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getIntPropertyMinValue](../android/icu/lang/UCharacter.md))`(`type:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` **\[icu\]**Returns the minimum value for an integer/binary Unicode property type. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getIntPropertyValue](../android/icu/lang/UCharacter.md))`(`ch:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `type:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` **\[icu\]**Returns the property value for a Unicode property type of a code point. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMirror](../android/icu/lang/UCharacter.md))`(`ch:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` **\[icu\]**Maps the specified code point to a "mirror-image" code point. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getName](../android/icu/lang/UCharacter.md))`(`ch:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` **\[icu\]** Returns the most current Unicode name of the argument code point, or null if the character is unassigned or outside the range`UCharacter.MIN_VALUE`and`UCharacter.MAX_VALUE`or does not have a name. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getName](../android/icu/lang/UCharacter.md))`(`s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `separator:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` **\[icu\]**Returns the names for each of the characters in a string |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getNameAlias](../android/icu/lang/UCharacter.md))`(`ch:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` **\[icu\]**Returns the corrected name from NameAliases. |
| static [ValueIterator](../android/icu/util/ValueIterator.md)! | [getNameIterator](../android/icu/lang/UCharacter.md))`()` **\[icu\]** |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getNumericValue](../android/icu/lang/UCharacter.md))`(`ch:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the numeric value of the code point as a nonnegative integer. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPropertyEnum](../android/icu/lang/UCharacter.md))`(`propertyAlias:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` **\[icu\]**Return the UProperty selector for a given property name, as specified in the Unicode database file PropertyAliases. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getPropertyName](../android/icu/lang/UCharacter.md))`(`property:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `nameChoice:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` **\[icu\]**Return the Unicode name for a given property, as given in the Unicode database file PropertyAliases. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPropertyValueEnum](../android/icu/lang/UCharacter.md))`(`property:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `valueAlias:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` **\[icu\]**Return the property value integer for a given value name, as specified in the Unicode database file PropertyValueAliases. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getPropertyValueName](../android/icu/lang/UCharacter.md))`(`property:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `value:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `nameChoice:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` **\[icu\]**Return the Unicode name for a given property value, as given in the Unicode database file PropertyValueAliases. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getType](../android/icu/lang/UCharacter.md))`(`ch:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns a value indicating a code point's Unicode category. |
| static [RangeValueIterator](../android/icu/util/RangeValueIterator.md)! | [getTypeIterator](../android/icu/lang/UCharacter.md))`()` **\[icu\]** |
| --- | --- |
| static [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [getUnicodeNumericValue](../android/icu/lang/UCharacter.md))`(`ch:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` **\[icu\]**Returns the numeric value for a Unicode code point as defined in the Unicode Character Database. |
| static [VersionInfo](../android/icu/util/VersionInfo.md)! | [getUnicodeVersion](../android/icu/lang/UCharacter.md))`()` **\[icu\]**Returns the version of Unicode data used. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasBinaryProperty](../android/icu/lang/UCharacter.md))`(`ch:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `property:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` **\[icu\]**Check a binary Unicode property for a code point. |
| --- | --- |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasBinaryProperty](../android/icu/lang/UCharacter.md))`(`s:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `property:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` **\[icu\]**Returns true if the property is true for the string. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isBMP](../android/icu/lang/UCharacter.md))`(`ch:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` **\[icu\]**Determines if the code point is in the BMP plane. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isBaseForm](../android/icu/lang/UCharacter.md))`(`ch:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` **\[icu\]**Determines whether the specified code point is of base form. |
| --- | --- |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isDefined](../android/icu/lang/UCharacter.md))`(`ch:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Determines if a code point has a defined meaning in the up-to-date Unicode standard. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isDigit](../android/icu/lang/UCharacter.md))`(`ch:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Determines if a code point is a Java digit. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isHighSurrogate](../android/icu/lang/UCharacter.md))`(`ch:` ` [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)`)` Same as [Character.isHighSurrogate](../java/lang/Character.md)), |
| --- | --- |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isHighSurrogate](../android/icu/lang/UCharacter.md))`(`codePoint:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Same as [Character.isHighSurrogate](../java/lang/Character.md)), except that the ICU version accepts`int`for code points. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isISOControl](../android/icu/lang/UCharacter.md))`(`ch:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Determines if the specified code point is an ISO control character. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isIdentifierIgnorable](../android/icu/lang/UCharacter.md))`(`ch:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Determines if the specified code point should be regarded as an ignorable character in a Java identifier. |
| --- | --- |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isJavaIdentifierPart](../android/icu/lang/UCharacter.md))`(`cp:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Compatibility override of Java method, delegates to java. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isJavaIdentifierStart](../android/icu/lang/UCharacter.md))`(`cp:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Compatibility override of Java method, delegates to java. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isLegal](../android/icu/lang/UCharacter.md))`(`ch:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` **\[icu\]**A code point is illegal if and only if - Out of bounds, less than 0 or greater than UCharacter.MAX_VALUE - A surrogate value, 0xD800 to 0xDFFF - Not-a-character, having the form 0x xxFFFF or 0x xxFFFE Note: legal does not mean that it is assigned in this version of Unicode. <br /> |
| --- | --- |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isLegal](../android/icu/lang/UCharacter.md))`(`str:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` **\[icu\]**A string is legal iff all its code points are legal. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isLetter](../android/icu/lang/UCharacter.md))`(`ch:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Determines if the specified code point is a letter. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isLetterOrDigit](../android/icu/lang/UCharacter.md))`(`ch:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Determines if the specified code point is a letter or digit. |
| --- | --- |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isLowSurrogate](../android/icu/lang/UCharacter.md))`(`ch:` ` [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)`)` Same as [Character.isLowSurrogate](../java/lang/Character.md)), |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isLowSurrogate](../android/icu/lang/UCharacter.md))`(`codePoint:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Same as [Character.isLowSurrogate](../java/lang/Character.md)), except that the ICU version accepts`int`for code points. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isLowerCase](../android/icu/lang/UCharacter.md))`(`ch:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Determines if the specified code point is a lowercase character. |
| --- | --- |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isMirrored](../android/icu/lang/UCharacter.md))`(`ch:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Determines whether the code point has the "mirrored" property. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isPrintable](../android/icu/lang/UCharacter.md))`(`ch:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` **\[icu\]**Determines whether the specified code point is a printable character according to the Unicode standard. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSpaceChar](../android/icu/lang/UCharacter.md))`(`ch:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Determines if the specified code point is a Unicode specified space character, i. |
| --- | --- |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSupplementary](../android/icu/lang/UCharacter.md))`(`ch:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` **\[icu\]**Determines if the code point is a supplementary character. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSupplementaryCodePoint](../android/icu/lang/UCharacter.md))`(`cp:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Same as [Character.isSupplementaryCodePoint](../java/lang/Character.md)). |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSurrogatePair](../android/icu/lang/UCharacter.md))`(`high:` ` [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)`, `low:` ` [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)`)` Same as [Character.isSurrogatePair](../java/lang/Character.md)). |
| --- | --- |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSurrogatePair](../android/icu/lang/UCharacter.md))`(`high:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `low:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Same as [Character.isSurrogatePair](../java/lang/Character.md)), except that the ICU version accepts`int`for code points. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isTitleCase](../android/icu/lang/UCharacter.md))`(`ch:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Determines if the specified code point is a titlecase character. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isUAlphabetic](../android/icu/lang/UCharacter.md))`(`ch:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` **\[icu\]** |
| --- | --- |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isULowercase](../android/icu/lang/UCharacter.md))`(`ch:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` **\[icu\]** |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isUUppercase](../android/icu/lang/UCharacter.md))`(`ch:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` **\[icu\]** |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isUWhiteSpace](../android/icu/lang/UCharacter.md))`(`ch:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` **\[icu\]** |
| --- | --- |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isUnicodeIdentifierPart](../android/icu/lang/UCharacter.md))`(`ch:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Determines if the specified character is permissible as a non-initial character of an identifier according to UAX #31 Unicode Identifier and Pattern Syntax. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isUnicodeIdentifierStart](../android/icu/lang/UCharacter.md))`(`ch:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Determines if the specified character is permissible as the first character in an identifier according to UAX #31 Unicode Identifier and Pattern Syntax. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isUpperCase](../android/icu/lang/UCharacter.md))`(`ch:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Determines if the specified code point is an uppercase character. |
| --- | --- |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isValidCodePoint](../android/icu/lang/UCharacter.md))`(`cp:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Equivalent to [Character.isValidCodePoint](../java/lang/Character.md)). |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isWhitespace](../android/icu/lang/UCharacter.md))`(`ch:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Determines if the specified code point is a white space character. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [offsetByCodePoints](../android/icu/lang/UCharacter.md))`(`text:` ` [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!`, `start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `count:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `codePointOffset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Equivalent to the[Character.offsetByCodePoints(char[], int, int, int, int)](https://developer.android.com/reference/kotlin/java/lang/Character.html#offsetByCodePoints(kotlin.CharArray,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int))method, for convenience. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [offsetByCodePoints](../android/icu/lang/UCharacter.md))`(`text:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `codePointOffset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Equivalent to the [Character.offsetByCodePoints(CharSequence, int, int)](../java/lang/Character.md))method, for convenience. |
| static [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)! | [toChars](../android/icu/lang/UCharacter.md))`(`cp:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Same as [Character.toChars(int)](../java/lang/Character.md)). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [toChars](../android/icu/lang/UCharacter.md))`(`cp:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `dst:` ` [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!`, `dstIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Same as[Character.toChars(int, char[], int)](https://developer.android.com/reference/kotlin/java/lang/Character.html#toChars(kotlin.Int,%20kotlin.CharArray,%20kotlin.Int)). |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [toCodePoint](../android/icu/lang/UCharacter.md))`(`high:` ` [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)`, `low:` ` [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)`)` Same as [Character.toCodePoint](../java/lang/Character.md)). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [toCodePoint](../android/icu/lang/UCharacter.md))`(`high:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `low:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Same as [Character.toCodePoint](../java/lang/Character.md)), except that the ICU version accepts`int`for code points. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [toLowerCase](../android/icu/lang/UCharacter.md))`(`locale:` ` [ULocale](../android/icu/util/ULocale.md)!`, `str:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns the lowercase version of the argument string. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [toLowerCase](../android/icu/lang/UCharacter.md))`(`ch:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` The given code point is mapped to its lowercase equivalent; if the code point has no lowercase equivalent, the code point itself is returned. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [toLowerCase](../android/icu/lang/UCharacter.md))`(`str:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns the lowercase version of the argument string. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [toLowerCase](../android/icu/lang/UCharacter.md))`(`locale:` ` [Locale](../java/util/Locale.md)!`, `str:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns the lowercase version of the argument string. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [toString](../android/icu/lang/UCharacter.md))`(`ch:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Converts argument code point and returns a String object representing the code point's value in UTF-16 format. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [toTitleCase](../android/icu/lang/UCharacter.md))`(`locale:` ` [ULocale](../android/icu/util/ULocale.md)!`, `str:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `titleIter:` ` [BreakIterator](../android/icu/text/BreakIterator.md)!`)` Returns the titlecase version of the argument string. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [toTitleCase](../android/icu/lang/UCharacter.md))`(`locale:` ` [ULocale](../android/icu/util/ULocale.md)!`, `str:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `titleIter:` ` [BreakIterator](../android/icu/text/BreakIterator.md)!`, `options:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the titlecase version of the argument string. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [toTitleCase](../android/icu/lang/UCharacter.md))`(`ch:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Converts the code point argument to titlecase. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [toTitleCase](../android/icu/lang/UCharacter.md))`(`str:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `breakiter:` ` [BreakIterator](../android/icu/text/BreakIterator.md)!`)` Returns the titlecase version of the argument string. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [toTitleCase](../android/icu/lang/UCharacter.md))`(`locale:` ` [Locale](../java/util/Locale.md)!`, `str:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `breakiter:` ` [BreakIterator](../android/icu/text/BreakIterator.md)!`)` Returns the titlecase version of the argument string. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [toTitleCase](../android/icu/lang/UCharacter.md))`(`locale:` ` [Locale](../java/util/Locale.md)!`, `str:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `titleIter:` ` [BreakIterator](../android/icu/text/BreakIterator.md)!`, `options:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` **\[icu\]** |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [toUpperCase](../android/icu/lang/UCharacter.md))`(`locale:` ` [ULocale](../android/icu/util/ULocale.md)!`, `str:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns the uppercase version of the argument string. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [toUpperCase](../android/icu/lang/UCharacter.md))`(`ch:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Converts the character argument to uppercase. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [toUpperCase](../android/icu/lang/UCharacter.md))`(`str:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns the uppercase version of the argument string. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [toUpperCase](../android/icu/lang/UCharacter.md))`(`locale:` ` [Locale](../java/util/Locale.md)!`, `str:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns the uppercase version of the argument string. |

## Constants

### FOLD_CASE_DEFAULT

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FOLD_CASE_DEFAULT: Int
```

**\[icu\]**Option value for case folding: use default mappings defined in CaseFolding.txt. 

 Value: 0

### FOLD_CASE_EXCLUDE_SPECIAL_I

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FOLD_CASE_EXCLUDE_SPECIAL_I: Int
```

**\[icu\]**Option value for case folding: Use the modified set of mappings provided in CaseFolding.txt to handle dotted I and dotless i appropriately for Turkic languages (tr, az).

Before Unicode 3.2, CaseFolding.txt contains mappings marked with 'I' that are to be included for default mappings and excluded for the Turkic-specific mappings.

Unicode 3.2 CaseFolding.txt instead contains mappings marked with 'T' that are to be excluded for default mappings and included for the Turkic-specific mappings. 

 Value: 1

### MAX_CODE_POINT

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MAX_CODE_POINT: Int
```

Constant U+10FFFF, same as [Character.MAX_CODE_POINT](../java/lang/Character.md). 

 Value: 1114111

### MAX_HIGH_SURROGATE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MAX_HIGH_SURROGATE: Char
```

Constant U+DBFF, same as [Character.MAX_HIGH_SURROGATE](../java/lang/Character.md). 

 Value: '\udbff'

### MAX_LOW_SURROGATE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MAX_LOW_SURROGATE: Char
```

Constant U+DFFF, same as [Character.MAX_LOW_SURROGATE](../java/lang/Character.md). 

 Value: '\udfff'

### MAX_RADIX

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MAX_RADIX: Int
```

Compatibility constant for Java Character's MAX_RADIX. 

 Value: 36

### MAX_SURROGATE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MAX_SURROGATE: Char
```

Constant U+DFFF, same as [Character.MAX_SURROGATE](../java/lang/Character.md). 

 Value: '\udfff'

### MAX_VALUE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MAX_VALUE: Int
```

The highest Unicode code point value (scalar value), constant U+10FFFF (uses 21 bits). Same as [Character.MAX_CODE_POINT](../java/lang/Character.md).

Up-to-date Unicode implementation of [Character.MAX_VALUE](../java/lang/Character.md) which is still a char with the value U+FFFF. 

 Value: 1114111

### MIN_CODE_POINT

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MIN_CODE_POINT: Int
```

Constant U+0000, same as [Character.MIN_CODE_POINT](../java/lang/Character.md). 

 Value: 0

### MIN_HIGH_SURROGATE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MIN_HIGH_SURROGATE: Char
```

Constant U+D800, same as [Character.MIN_HIGH_SURROGATE](../java/lang/Character.md). 

 Value: '\ud800'

### MIN_LOW_SURROGATE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MIN_LOW_SURROGATE: Char
```

Constant U+DC00, same as [Character.MIN_LOW_SURROGATE](../java/lang/Character.md). 

 Value: '\udc00'

### MIN_RADIX

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MIN_RADIX: Int
```

Compatibility constant for Java Character's MIN_RADIX. 

 Value: 2

### MIN_SUPPLEMENTARY_CODE_POINT

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MIN_SUPPLEMENTARY_CODE_POINT: Int
```

Constant U+10000, same as [Character.MIN_SUPPLEMENTARY_CODE_POINT](../java/lang/Character.md). 

 Value: 65536

### MIN_SURROGATE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MIN_SURROGATE: Char
```

Constant U+D800, same as [Character.MIN_SURROGATE](../java/lang/Character.md). 

 Value: '\ud800'

### MIN_VALUE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MIN_VALUE: Int
```

The lowest Unicode code point value, constant 0. Same as [Character.MIN_CODE_POINT](../java/lang/Character.md), same integer value as [Character.MIN_VALUE](../java/lang/Character.md). 

 Value: 0

### NO_NUMERIC_VALUE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NO_NUMERIC_VALUE: Double
```

Special value that is returned by getUnicodeNumericValue(int) when no numeric value is defined for a code point. 

 Value: -1.23456789E8

**See Also**

- [#getUnicodeNumericValue](../android/icu/lang/UCharacter.md)) 

### REPLACEMENT_CHAR

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val REPLACEMENT_CHAR: Int
```

Unicode value used when translating into Unicode encoding form and there is no existing character. 

 Value: 65533

### SUPPLEMENTARY_MIN_VALUE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SUPPLEMENTARY_MIN_VALUE: Int
```

The minimum value for Supplementary code points, constant U+10000. Same as [Character.MIN_SUPPLEMENTARY_CODE_POINT](../java/lang/Character.md). 

 Value: 65536

### TITLECASE_NO_BREAK_ADJUSTMENT

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TITLECASE_NO_BREAK_ADJUSTMENT: Int
```

Do not adjust the titlecasing indexes from BreakIterator::next() indexes; titlecase exactly the characters at breaks from the iterator. Option bit for titlecasing APIs that take an options bit set. By default, titlecasing will take each break iterator index, adjust it by looking for the next cased character, and titlecase that one. Other characters are lowercased. This follows Unicode 4 \& 5 section 3.13 Default Case Operations: R3 toTitlecase(X): Find the word boundaries based on Unicode Standard Annex #29, "Text Boundaries." Between each pair of word boundaries, find the first cased character F. If F exists, map F to default_title(F); then map each subsequent character C to default_lower(C). 

 Value: 512

**See Also**

- [#TITLECASE_NO_LOWERCASE](../android/icu/lang/UCharacter.md) 

### TITLECASE_NO_LOWERCASE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TITLECASE_NO_LOWERCASE: Int
```

Do not lowercase non-initial parts of words when titlecasing. Option bit for titlecasing APIs that take an options bit set. By default, titlecasing will titlecase the first cased character of a word and lowercase all other characters. With this option, the other characters will not be modified. 

 Value: 256

**See Also**

## Public methods

### charCount

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun charCount(cp: Int): Int
```

Same as [Character.charCount](../java/lang/Character.md)). Returns the number of chars needed to represent the code point (1 or 2). This does not check the code point for validity.

| Parameters ||
|------|----------------------------------------------------------------------------------------------------|
| `cp` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the code point to check |

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of chars needed to represent the code point |

### codePointAt

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun codePointAt(
    text: CharArray!, 
    index: Int
): Int
```

Same as[Character.codePointAt(char[], int)](https://developer.android.com/reference/kotlin/java/lang/Character.html#codePointAt(kotlin.CharArray,%20kotlin.Int)). Returns the code point at index. This examines only the characters at index and index+1.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------|
| `text` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!:the characters to check |
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index of the first or only char forming the code point |

| Return ||
|----------------------------------------------------------------------------|-----------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the code point at the index |

### codePointAt

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun codePointAt(
    text: CharArray!, 
    index: Int, 
    limit: Int
): Int
```

Same as[Character.codePointAt(char[], int, int)](https://developer.android.com/reference/kotlin/java/lang/Character.html#codePointAt(kotlin.CharArray,%20kotlin.Int,%20kotlin.Int)). Returns the code point at index. This examines only the characters at index and index+1.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------|
| `text` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!:the characters to check |
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index of the first or only char forming the code point |
| `limit` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the limit of the valid text |
| --- | --- |

| Return ||
|----------------------------------------------------------------------------|-----------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the code point at the index |

### codePointAt

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun codePointAt(
    seq: CharSequence!, 
    index: Int
): Int
```

Same as [Character.codePointAt(CharSequence, int)](../java/lang/Character.md)). Returns the code point at index. This examines only the characters at index and index+1.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------|
| `seq` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:the characters to check |
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index of the first or only char forming the code point |

| Return ||
|----------------------------------------------------------------------------|-----------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the code point at the index |

### codePointBefore

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun codePointBefore(
    text: CharArray!, 
    index: Int
): Int
```

Same as[Character.codePointBefore(char[], int)](https://developer.android.com/reference/kotlin/java/lang/Character.html#codePointBefore(kotlin.CharArray,%20kotlin.Int)). Returns the code point before index. This examines only the characters at index-1 and index-2.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------------------------|
| `text` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!:the characters to check |
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index after the last or only char forming the code point |

| Return ||
|----------------------------------------------------------------------------|---------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the code point before the index |

### codePointBefore

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun codePointBefore(
    text: CharArray!, 
    index: Int, 
    limit: Int
): Int
```

Same as[Character.codePointBefore(char[], int, int)](https://developer.android.com/reference/kotlin/java/lang/Character.html#codePointBefore(kotlin.CharArray,%20kotlin.Int,%20kotlin.Int)). Return the code point before index. This examines only the characters at index-1 and index-2.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------------------------|
| `text` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!:the characters to check |
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index after the last or only char forming the code point |
| `limit` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the start of the valid text |
| --- | --- |

| Return ||
|----------------------------------------------------------------------------|---------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the code point before the index |

### codePointBefore

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun codePointBefore(
    seq: CharSequence!, 
    index: Int
): Int
```

Same as [Character.codePointBefore(CharSequence, int)](../java/lang/Character.md)). Return the code point before index. This examines only the characters at index-1 and index-2.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------------------------|
| `seq` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:the characters to check |
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index after the last or only char forming the code point |

| Return ||
|----------------------------------------------------------------------------|---------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the code point before the index |

### codePointCount

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun codePointCount(
    text: CharArray!, 
    start: Int, 
    limit: Int
): Int
```

Equivalent to the[Character.codePointCount(char[], int, int)](https://developer.android.com/reference/kotlin/java/lang/Character.html#codePointCount(kotlin.CharArray,%20kotlin.Int,%20kotlin.Int))method, for convenience. Counts the number of code points in the range of text.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------|
| `text` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!:the characters to check |
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the start of the range |
| `limit` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the limit of the range |
| --- | --- |

| Return ||
|----------------------------------------------------------------------------|----------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of code points in the range |

### codePointCount

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun codePointCount(
    text: CharSequence!, 
    start: Int, 
    limit: Int
): Int
```

Equivalent to the [Character.codePointCount(CharSequence, int, int)](../java/lang/Character.md))method, for convenience. Counts the number of code points in the range of text.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------|
| `text` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:the characters to check |
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the start of the range |
| `limit` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the limit of the range |
| --- | --- |

| Return ||
|----------------------------------------------------------------------------|----------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of code points in the range |

### digit

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun digit(ch: Int): Int
```

Returnss the numeric value of a decimal digit code point. 
This is a convenience overload of`digit(int, int)`that provides a decimal radix. 
*Semantic Change:*In release 1.3.1 and prior, this treated numeric letters and other numbers as digits. This has been changed to conform to the java semantics.

| Parameters ||
|------|----------------------------------------------------------------------------------------------------|
| `ch` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the code point to query |

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the numeric value represented by the code point, or -1 if the code point is not a decimal digit or if its value is too large for a decimal radix |

### digit

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun digit(
    ch: Int, 
    radix: Int
): Int
```

Returnss the numeric value of a decimal digit code point. 
This method observes the semantics of`java.lang.Character.digit()`. Note that this will return positive values for code points for which isDigit returns false, just like java.lang.Character. 
*Semantic Change:* In release 1.3.1 and prior, this did not treat the European letters as having a digit value, and also treated numeric letters and other numbers as digits. This has been changed to conform to the java semantics. 
A code point is a valid digit if and only if:

- ch is a decimal digit or one of the european letters, and
- the value of ch is less than the specified radix.

<br />

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------|
| `ch` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the code point to query |
| `radix` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the radix |

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the numeric value represented by the code point in the specified radix, or -1 if the code point is not a decimal digit or if its value is too large for the radix |

### foldCase

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun foldCase(
    ch: Int, 
    defaultmapping: Boolean
): Int
```

**\[icu\]**The given character is mapped to its case folding equivalent according to UnicodeData.txt and CaseFolding.txt; if the character has no case folding equivalent, the character itself is returned.

This function only returns the simple, single-code point case mapping. Full case mappings should be used whenever possible because they produce better results by working on whole strings. They can map to a result string with a different length as appropriate. Full case mappings are applied by the case mapping functions that take String parameters rather than code points (int). See also the User Guide chapter on C/POSIX migration: https://unicode-org.github.io/icu/userguide/icu/posix#case-mappings

| Parameters ||
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `ch` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the character to be converted |
| `defaultmapping` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):Indicates whether the default mappings defined in CaseFolding.txt are to be used, otherwise the mappings for dotted I and dotless i marked with 'T' in CaseFolding.txt are included. |

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the case folding equivalent of the character, if any; otherwise the character itself. |

**See Also**

- [#foldCase(String, boolean)](../android/icu/lang/UCharacter.md)) 

### foldCase

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun foldCase(
    ch: Int, 
    options: Int
): Int
```

**\[icu\]**The given character is mapped to its case folding equivalent according to UnicodeData.txt and CaseFolding.txt; if the character has no case folding equivalent, the character itself is returned.

This function only returns the simple, single-code point case mapping. Full case mappings should be used whenever possible because they produce better results by working on whole strings. They can map to a result string with a different length as appropriate. Full case mappings are applied by the case mapping functions that take String parameters rather than code points (int). See also the User Guide chapter on C/POSIX migration: https://unicode-org.github.io/icu/userguide/icu/posix#case-mappings

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `ch` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the character to be converted |
| `options` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):A bit set for special processing. Currently the recognised options are FOLD_CASE_EXCLUDE_SPECIAL_I and FOLD_CASE_DEFAULT |

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the case folding equivalent of the character, if any; otherwise the character itself. |

**See Also**

- [#foldCase(String, boolean)](../android/icu/lang/UCharacter.md)) 

### foldCase

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun foldCase(
    str: String!, 
    defaultmapping: Boolean
): String!
```

**\[icu\]**The given string is mapped to its case folding equivalent according to UnicodeData.txt and CaseFolding.txt; if any character has no case folding equivalent, the character itself is returned. "Full", multiple-code point case folding mappings are returned here. For "simple" single-code point mappings use the API foldCase(int ch, boolean defaultmapping).

| Parameters ||
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `str` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the String to be converted |
| `defaultmapping` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):Indicates whether the default mappings defined in CaseFolding.txt are to be used, otherwise the mappings for dotted I and dotless i marked with 'T' in CaseFolding.txt are included. |

| Return ||
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the case folding equivalent of the character, if any; otherwise the character itself. |

**See Also**

- [#foldCase(int, boolean)](../android/icu/lang/UCharacter.md)) 

### foldCase

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun foldCase(
    str: String!, 
    options: Int
): String!
```

**\[icu\]**The given string is mapped to its case folding equivalent according to UnicodeData.txt and CaseFolding.txt; if any character has no case folding equivalent, the character itself is returned. "Full", multiple-code point case folding mappings are returned here. For "simple" single-code point mappings use the API foldCase(int ch, boolean defaultmapping).

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `str` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the String to be converted |
| `options` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):A bit set for special processing. Currently the recognised options are FOLD_CASE_EXCLUDE_SPECIAL_I and FOLD_CASE_DEFAULT |

| Return ||
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the case folding equivalent of the character, if any; otherwise the character itself. |

**See Also**

- [#foldCase(int, boolean)](../android/icu/lang/UCharacter.md)) 

### forDigit

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun forDigit(
    digit: Int, 
    radix: Int
): Char
```

Provide the java.lang.Character forDigit API, for convenience. 

### getAge

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getAge(ch: Int): VersionInfo!
```

**\[icu\]**Returns the "age" of the code point.

The "age" is the Unicode version when the code point was first designated (as a non-character or for Private Use) or assigned a character.

This can be useful to avoid emitting code points to receiving processes that do not accept newer characters.

The data is from the UCD file DerivedAge.txt.

| Parameters ||
|------|--------------------------------------------------------------------------------------------|
| `ch` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The code point. |

| Return ||
|---------------------------------------------------------------------------------------------------|----------------------------|
| [VersionInfo](../android/icu/util/VersionInfo.md)! | the Unicode version number |

### getBidiPairedBracket

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getBidiPairedBracket(c: Int): Int
```

**\[icu\]**Maps the specified character to its paired bracket character. For Bidi_Paired_Bracket_Type!=None, this is the same as getMirror(int). Otherwise c itself is returned. See http://www.unicode.org/reports/tr9/

| Parameters ||
|-----|--------------------------------------------------------------------------------------------------------|
| `c` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the code point to be mapped |

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the paired bracket code point, or c itself if there is no such mapping (Bidi_Paired_Bracket_Type=None) |

**See Also**

- [android.icu.lang.UProperty#BIDI_PAIRED_BRACKET](../android/icu/lang/UProperty.md)
- [android.icu.lang.UProperty#BIDI_PAIRED_BRACKET_TYPE](../android/icu/lang/UProperty.md)
- [#getMirror(int)](../android/icu/lang/UCharacter.md)) 

### getCharFromExtendedName

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getCharFromExtendedName(name: String!): Int
```

**\[icu\]**

Find a Unicode character by either its name and return its code point value. All Unicode names are in uppercase. Extended names are all lowercase except for numbers and are contained within angle brackets. The names are searched in the following order

- Most current Unicode name if there is any
- Unicode 1.0 name if there is any
- Extended name in the form of "\<codepoint_type-codepoint_hex_digits\>". E.g. \<noncharacter-FFFE\>

Note calling any methods related to code point names, e.g.`getName()`incurs a one-time initialization cost to construct the name tables.

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:codepoint name |

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | code point associated with the name or -1 if the name is not found. |

### getCharFromName

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getCharFromName(name: String!): Int
```

**\[icu\]**

Finds a Unicode code point by its most current Unicode name and return its code point value. All Unicode names are in uppercase. Note calling any methods related to code point names, e.g.`getName()`incurs a one-time initialization cost to construct the name tables.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:most current Unicode character name whose code point is to be returned |

| Return ||
|----------------------------------------------------------------------------|---------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | code point or -1 if name is not found |

### getCharFromNameAlias

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getCharFromNameAlias(name: String!): Int
```

**\[icu\]**

Find a Unicode character by its corrected name alias and return its code point value. All Unicode names are in uppercase. Note calling any methods related to code point names, e.g.`getName()`incurs a one-time initialization cost to construct the name tables.

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:Unicode name alias whose code point is to be returned |

| Return ||
|----------------------------------------------------------------------------|---------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | code point or -1 if name is not found |

### getCodePoint

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getCodePoint(char16: Char): Int
```

**\[icu\]**Returns the code point corresponding to the BMP code point.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------|
| `char16` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html):the BMP code point |

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | code point if argument is a valid character. |

| Exceptions ||
|--------------------------------------|----------------------------------------------|
| `java.lang.IllegalArgumentException` | thrown when char16 is not a valid code point |

### getCodePoint

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getCodePoint(
    lead: Char, 
    trail: Char
): Int
```

**\[icu\]**Returns a code point corresponding to the two surrogate code units.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------|
| `lead` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html):the lead char |
| `trail` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html):the trail char |

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | code point if surrogate characters are valid. |

| Exceptions ||
|--------------------------------------|-----------------------------------------------------------|
| `java.lang.IllegalArgumentException` | thrown when the code units do not form a valid code point |

### getCodePoint

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getCodePoint(
    lead: Int, 
    trail: Int
): Int
```

**\[icu\]**Returns a code point corresponding to the two surrogate code units.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| `lead` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the lead unit (In ICU 2.1-69 the type of both parameters was`char`.) |
| `trail` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the trail unit |

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | code point if lead and trail form a valid surrogate pair. |

| Exceptions ||
|--------------------------------------|---------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | thrown when the code units do not form a valid surrogate pair |

**See Also**

- [#toCodePoint(int, int)](../android/icu/lang/UCharacter.md)) 

### getCombiningClass

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getCombiningClass(ch: Int): Int
```

**\[icu\]**Returns the combining class of the argument codepoint

| Parameters ||
|------|--------------------------------------------------------------------------------------------------------------------------|
| `ch` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):code point whose combining is to be retrieved |

| Return ||
|----------------------------------------------------------------------------|--------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the combining class of the codepoint |

### getDirection

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getDirection(ch: Int): Int
```

**\[icu\]** Returns the Bidirection property of a code point. For example, 0x0041 (letter A) has the LEFT_TO_RIGHT directional property. 
Result returned belongs to the interface [UCharacterDirection](../android/icu/lang/UCharacterDirection.md)

| Parameters ||
|------|--------------------------------------------------------------------------------------------------------------------------|
| `ch` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the code point to be determined its direction |

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | direction constant from UCharacterDirection. |

### getDirectionality

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getDirectionality(cp: Int): Byte
```

Equivalent to the [Character.getDirectionality(char)](../java/lang/Character.md))method, for convenience. Returns a byte representing the directionality of the character.**\[icu\] Note:** Unlike [Character.getDirectionality(char)](../java/lang/Character.md)), this returns DIRECTIONALITY_LEFT_TO_RIGHT for undefined or out-of-bounds characters.**\[icu\] Note:** The return value must be tested using the constants defined in [UCharacterDirection](../android/icu/lang/UCharacterDirection.md) and its interface [UCharacterEnums.ECharacterDirection](../android/icu/lang/UCharacterEnums.ECharacterDirection.md) since the values are different from the ones defined by`java.lang.Character`.

| Parameters ||
|------|----------------------------------------------------------------------------------------------------|
| `cp` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the code point to check |

| Return ||
|------------------------------------------------------------------------------|--------------------------------------|
| [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | the directionality of the code point |

**See Also**

- [#getDirection](../android/icu/lang/UCharacter.md)) 

### getExtendedName

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getExtendedName(ch: Int): String!
```

**\[icu\]**Returns a name for a valid codepoint. Unlike, getName(int) and getName1_0(int), this method will return a name even for codepoints that are not assigned a name in UnicodeData.txt.

The names are returned in the following order.

- Most current Unicode name if there is any
- Unicode 1.0 name if there is any
- Extended name in the form of "\<codepoint_type-codepoint_hex_digits\>". E.g., \<noncharacter-fffe\>

Note calling any methods related to code point names, e.g.`getName()`incurs a one-time initialization cost to construct the name tables.

| Parameters ||
|------|---------------------------------------------------------------------------------------------------------------------|
| `ch` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the code point for which to get the name |

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | a name for the argument codepoint |

### getExtendedNameIterator

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getExtendedNameIterator(): ValueIterator!
```

**\[icu\]**

Returns an iterator for character names, iterating over codepoints.

This API only gets the iterator for the extended names. For modern, most up-to-date Unicode names use getNameIterator() or for older 1.0 Unicode names use get1_0NameIterator().

Example of use: 

```kotlin
ValueIterator iterator = UCharacter.getExtendedNameIterator();
  ValueIterator.Element element = new ValueIterator.Element();
  while (iterator.next(element)) {
      System.out.println("Codepoint \\u" +
                         Integer.toHexString(element.codepoint) +
                         " has the name " + (String)element.value);
  }
  
```

The maximal range which the name iterator iterates is from

| Return ||
|-------------------------------------------------------------------------------------------------------|-------------|
| [ValueIterator](../android/icu/util/ValueIterator.md)! | an iterator |

### getHanNumericValue

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getHanNumericValue(ch: Int): Int
```

**\[icu\]**Returns the numeric value of a Han character.

This returns the value of Han 'numeric' code points, including those for zero, ten, hundred, thousand, ten thousand, and hundred million. This includes both the standard and 'checkwriting' characters, the 'big circle' zero character, and the standard zero character.

Note: The Unicode Standard has numeric values for more Han characters recognized by this method (see [getNumericValue(int)](../android/icu/lang/UCharacter.md))and the UCD file DerivedNumericValues.txt), and a [android.icu.text.NumberFormat](../android/icu/text/NumberFormat.md) can be used with a Chinese [android.icu.text.NumberingSystem](../android/icu/text/NumberingSystem.md).

| Parameters ||
|------|------------------------------------------------------------------------------------------------|
| `ch` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):code point to query |

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | value if it is a Han 'numeric character,' otherwise return -1. |

### getIntPropertyMaxValue

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getIntPropertyMaxValue(type: Int): Int
```

**\[icu\]**Returns the maximum value for an integer/binary Unicode property. Can be used together with UCharacter.getIntPropertyMinValue(int) to allocate arrays of android.icu.text.UnicodeSet or similar. Examples for min/max values (for Unicode 3.2):

- UProperty.BIDI_CLASS: 0/18 (UCharacterDirection.LEFT_TO_RIGHT/UCharacterDirection.BOUNDARY_NEUTRAL)
- UProperty.SCRIPT: 0/45 (UScript.COMMON/UScript.TAGBANWA)
- UProperty.IDEOGRAPHIC: 0/1 (false/true)

For undefined UProperty constant values, min/max values will be 0/-1.

<br />

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `type` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):UProperty selector constant, identifies which binary property to check. Must be UProperty.BINARY_START \<= type \< UProperty.BINARY_LIMIT or UProperty.INT_START \<= type \< UProperty.INT_LIMIT. |

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Maximum value returned by u_getIntPropertyValue for a Unicode property. \<= 0 if the property selector 'type' is out of range. |

**See Also**

- [android.icu.lang.UProperty](../android/icu/lang/UProperty.md)
- [#getUnicodeVersion](../android/icu/lang/UCharacter.md))
- [#getIntPropertyMaxValue](../android/icu/lang/UCharacter.md))
- [#getIntPropertyValue](../android/icu/lang/UCharacter.md)) 

### getIntPropertyMinValue

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getIntPropertyMinValue(type: Int): Int
```

**\[icu\]**Returns the minimum value for an integer/binary Unicode property type. Can be used together with UCharacter.getIntPropertyMaxValue(int) to allocate arrays of android.icu.text.UnicodeSet or similar.

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `type` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):UProperty selector constant, identifies which binary property to check. Must be UProperty.BINARY_START \<= type \< UProperty.BINARY_LIMIT or UProperty.INT_START \<= type \< UProperty.INT_LIMIT. |

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Minimum value returned by UCharacter.getIntPropertyValue(int) for a Unicode property. 0 if the property selector 'type' is out of range. |

**See Also**

- [android.icu.lang.UProperty](../android/icu/lang/UProperty.md)
- [#getUnicodeVersion](../android/icu/lang/UCharacter.md))
- [#getIntPropertyMaxValue](../android/icu/lang/UCharacter.md))
- [#getIntPropertyValue](../android/icu/lang/UCharacter.md)) 

### getIntPropertyValue

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getIntPropertyValue(
    ch: Int, 
    type: Int
): Int
```

**\[icu\]**Returns the property value for a Unicode property type of a code point. Also returns binary and mask property values.

Unicode, especially in version 3.2, defines many more properties than the original set in UnicodeData.txt.

The properties APIs are intended to reflect Unicode properties as defined in the Unicode Character Database (UCD) and Unicode Technical Reports (UTR). For details about the properties see http://www.unicode.org/.

For names of Unicode properties see the UCD file PropertyAliases.txt. 

```kotlin
Sample usage:
  int ea = UCharacter.getIntPropertyValue(c, UProperty.EAST_ASIAN_WIDTH);
  int ideo = UCharacter.getIntPropertyValue(c, UProperty.IDEOGRAPHIC);
  boolean b = (ideo == 1) ? true : false;
  
```

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `ch` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):code point to test. |
| `type` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):UProperty selector constant, identifies which binary property to check. Must be UProperty.BINARY_START \<= type \< UProperty.BINARY_LIMIT or UProperty.INT_START \<= type \< UProperty.INT_LIMIT or UProperty.MASK_START \<= type \< UProperty.MASK_LIMIT. |

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | numeric value that is directly the property value or, for enumerated properties, corresponds to the numeric value of the enumerated constant of the respective property value type ([ECharacterCategory](../android/icu/lang/UCharacterEnums.ECharacterCategory.md), [ECharacterDirection](../android/icu/lang/UCharacterEnums.ECharacterDirection.md), [DecompositionType](../android/icu/lang/UCharacter.DecompositionType.md), etc.). Returns 0 or 1 (for false / true) for binary Unicode properties. Returns a bit-mask for mask properties. Returns 0 if 'type' is out of bounds or if the Unicode version does not have data for the property at all, or not for this code point. |

**See Also**

- [android.icu.lang.UProperty](../android/icu/lang/UProperty.md)
- [#getIntPropertyMinValue](../android/icu/lang/UCharacter.md))
- [#getIntPropertyMaxValue](../android/icu/lang/UCharacter.md))
- [#getUnicodeVersion](../android/icu/lang/UCharacter.md)) 

### getMirror

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getMirror(ch: Int): Int
```

**\[icu\]** Maps the specified code point to a "mirror-image" code point. For code points with the "mirrored" property, implementations sometimes need a "poor man's" mapping to another code point such that the default glyph may serve as the mirror-image of the default glyph of the specified code point. 
This is useful for text conversion to and from codepages with visual order, and for displays without glyph selection capabilities.

| Parameters ||
|------|-----------------------------------------------------------------------------------------------------------------------|
| `ch` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):code point whose mirror is to be retrieved |

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | another code point that may serve as a mirror-image substitute, or ch itself if there is no such mapping or ch does not have the "mirrored" property |

### getName

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getName(ch: Int): String!
```

**\[icu\]** Returns the most current Unicode name of the argument code point, or null if the character is unassigned or outside the range`UCharacter.MIN_VALUE`and`UCharacter.MAX_VALUE`or does not have a name. 
Note calling any methods related to code point names, e.g.`getName()`incurs a one-time initialization cost to construct the name tables.

| Parameters ||
|------|---------------------------------------------------------------------------------------------------------------------|
| `ch` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the code point for which to get the name |

| Return ||
|-----------------------------------------------------------------------------------|---------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | most current Unicode name |

### getName

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getName(
    s: String!, 
    separator: String!
): String!
```

**\[icu\]**Returns the names for each of the characters in a string

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------------------|
| `s` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:string to format |
| `separator` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:string to go between names |

| Return ||
|-----------------------------------------------------------------------------------|-----------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | string of names |

### getNameAlias

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getNameAlias(ch: Int): String!
```

**\[icu\]** Returns the corrected name from NameAliases.txt if there is one. Returns null if the character is unassigned or outside the range UCharacter.MIN_VALUE and UCharacter.MAX_VALUE or does not have a name. 
Note calling any methods related to code point names, e.g.`getName()`incurs a one-time initialization cost to construct the name tables.

| Parameters ||
|------|---------------------------------------------------------------------------------------------------------------------------|
| `ch` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the code point for which to get the name alias |

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | Unicode name alias, or null |

### getNameIterator

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getNameIterator(): ValueIterator!
```

**\[icu\]**

Returns an iterator for character names, iterating over codepoints.

This API only gets the iterator for the modern, most up-to-date Unicode names. For older 1.0 Unicode names use get1_0NameIterator() or for extended names use getExtendedNameIterator().

Example of use: 

```kotlin
ValueIterator iterator = UCharacter.getNameIterator();
  ValueIterator.Element element = new ValueIterator.Element();
  while (iterator.next(element)) {
      System.out.println("Codepoint \\u" +
                         Integer.toHexString(element.codepoint) +
                         " has the name " + (String)element.value);
  }
  
```

The maximal range which the name iterator iterates is from UCharacter.MIN_VALUE to UCharacter.MAX_VALUE.

| Return ||
|-------------------------------------------------------------------------------------------------------|-------------|
| [ValueIterator](../android/icu/util/ValueIterator.md)! | an iterator |

### getNumericValue

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getNumericValue(ch: Int): Int
```

Returns the numeric value of the code point as a nonnegative integer. 
If the code point does not have a numeric value, then -1 is returned. 
If the code point has a numeric value that cannot be represented as a nonnegative integer (for example, a fractional value), then -2 is returned.

| Parameters ||
|------|----------------------------------------------------------------------------------------------------|
| `ch` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the code point to query |

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the numeric value of the code point, or -1 if it has no numeric value, or -2 if it has a numeric value that cannot be represented as a nonnegative integer |

### getPropertyEnum

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getPropertyEnum(propertyAlias: CharSequence!): Int
```

**\[icu\]**Return the UProperty selector for a given property name, as specified in the Unicode database file PropertyAliases.txt. Short, long, and any other variants are recognized. In addition, this function maps the synthetic names "gcm" / "General_Category_Mask" to the property UProperty.GENERAL_CATEGORY_MASK. These names are not in PropertyAliases.txt.

| Parameters ||
|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `propertyAlias` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:the property name to be matched. The name is compared using "loose matching" as described in PropertyAliases.txt. |

| Return ||
|----------------------------------------------------------------------------|-------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a UProperty enum. |

| Exceptions ||
|--------------------------------------|--------------------------------------------|
| `java.lang.IllegalArgumentException` | thrown if propertyAlias is not recognized. |

**See Also**

- [android.icu.lang.UProperty](../android/icu/lang/UProperty.md) 

### getPropertyName

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getPropertyName(
    property: Int, 
    nameChoice: Int
): String!
```

**\[icu\]**Return the Unicode name for a given property, as given in the Unicode database file PropertyAliases.txt. Most properties have more than one name. The nameChoice determines which one is returned. In addition, this function maps the property UProperty.GENERAL_CATEGORY_MASK to the synthetic names "gcm" / "General_Category_Mask". These names are not in PropertyAliases.txt.

| Parameters ||
|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `property` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):UProperty selector. |
| `nameChoice` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):UProperty.NameChoice selector for which name to get. All properties have a long name. Most have a short name, but some do not. Unicode allows for additional names; if present these will be returned by UProperty.NameChoice.LONG + i, where i=1, 2,... |

| Return ||
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | a name, or null if Unicode explicitly defines no name ("n/a") for a given property/nameChoice. If a given nameChoice throws an exception, then all larger values of nameChoice will throw an exception. If null is returned for a given nameChoice, then other nameChoice values may return non-null results. |

| Exceptions ||
|--------------------------------------|-----------------------------------------------|
| `java.lang.IllegalArgumentException` | thrown if property or nameChoice are invalid. |

**See Also**

- [android.icu.lang.UProperty](../android/icu/lang/UProperty.md)
- [android.icu.lang.UProperty.NameChoice](../android/icu/lang/UProperty.NameChoice.md) 

### getPropertyValueEnum

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getPropertyValueEnum(
    property: Int, 
    valueAlias: CharSequence!
): Int
```

**\[icu\]**Return the property value integer for a given value name, as specified in the Unicode database file PropertyValueAliases.txt. Short, long, and any other variants are recognized. Note: Some of the names in PropertyValueAliases.txt will only be recognized with UProperty.GENERAL_CATEGORY_MASK, not UProperty.GENERAL_CATEGORY. These include: "C" / "Other", "L" / "Letter", "LC" / "Cased_Letter", "M" / "Mark", "N" / "Number", "P" / "Punctuation", "S" / "Symbol", and "Z" / "Separator".

| Parameters ||
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `property` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):UProperty selector constant. UProperty.INT_START \<= property \< UProperty.INT_LIMIT or UProperty.BINARY_START \<= property \< UProperty.BINARY_LIMIT or UProperty.MASK_START \< = property \< UProperty.MASK_LIMIT. Only these properties can be enumerated. |
| `valueAlias` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:the value name to be matched. The name is compared using "loose matching" as described in PropertyValueAliases.txt. |

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a value integer. Note: UProperty.GENERAL_CATEGORY values are mask values produced by left-shifting 1 by UCharacter.getType(). This allows grouped categories such as \[:L:\] to be represented. |

| Exceptions ||
|--------------------------------------|---------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if property is not a valid UProperty selector or valueAlias is not a value of this property |

**See Also**

- [android.icu.lang.UProperty](../android/icu/lang/UProperty.md) 

### getPropertyValueName

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getPropertyValueName(
    property: Int, 
    value: Int, 
    nameChoice: Int
): String!
```

**\[icu\]**Return the Unicode name for a given property value, as given in the Unicode database file PropertyValueAliases.txt. Most values have more than one name. The nameChoice determines which one is returned. Note: Some of the names in PropertyValueAliases.txt can only be retrieved using UProperty.GENERAL_CATEGORY_MASK, not UProperty.GENERAL_CATEGORY. These include: "C" / "Other", "L" / "Letter", "LC" / "Cased_Letter", "M" / "Mark", "N" / "Number", "P" / "Punctuation", "S" / "Symbol", and "Z" / "Separator".

| Parameters ||
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `property` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):UProperty selector constant. UProperty.INT_START \<= property \< UProperty.INT_LIMIT or UProperty.BINARY_START \<= property \< UProperty.BINARY_LIMIT or UProperty.MASK_START \< = property \< UProperty.MASK_LIMIT. If out of range, null is returned. |
| `value` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):selector for a value for the given property. In general, valid values range from 0 up to some maximum. There are a few exceptions: (1.) UProperty.BLOCK values begin at the non-zero value BASIC_LATIN.getID(). (2.) UProperty.CANONICAL_COMBINING_CLASS values are not contiguous and range from 0..240. (3.) UProperty.GENERAL_CATEGORY_MASK values are mask values produced by left-shifting 1 by UCharacter.getType(). This allows grouped categories such as \[:L:\] to be represented. Mask values are non-contiguous. |
| `nameChoice` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):UProperty.NameChoice selector for which name to get. All values have a long name. Most have a short name, but some do not. Unicode allows for additional names; if present these will be returned by UProperty.NameChoice.LONG + i, where i=1, 2,... |
| --- | --- |

| Return ||
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | a name, or null if Unicode explicitly defines no name ("n/a") for a given property/value/nameChoice. If a given nameChoice throws an exception, then all larger values of nameChoice will throw an exception. If null is returned for a given nameChoice, then other nameChoice values may return non-null results. |

| Exceptions ||
|--------------------------------------|-------------------------------------------------------|
| `java.lang.IllegalArgumentException` | thrown if property, value, or nameChoice are invalid. |

**See Also**

- [android.icu.lang.UProperty](../android/icu/lang/UProperty.md)
- [android.icu.lang.UProperty.NameChoice](../android/icu/lang/UProperty.NameChoice.md) 

### getType

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getType(ch: Int): Int
```

Returns a value indicating a code point's Unicode category. Up-to-date Unicode implementation of java.lang.Character.getType() except for the above mentioned code points that had their category changed. 
Return results are constants from the interface [UCharacterCategory](../android/icu/lang/UCharacterCategory.md) 
*NOTE:* the UCharacterCategory values are*not*compatible with those returned by java.lang.Character.getType. UCharacterCategory values match the ones used in ICU4C, while java.lang.Character type values, though similar, skip the value 17.

| Parameters ||
|------|----------------------------------------------------------------------------------------------------------------------|
| `ch` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):code point whose type is to be determined |

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | category which is a value of UCharacterCategory |

### getTypeIterator

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getTypeIterator(): RangeValueIterator!
```

**\[icu\]**

Returns an iterator for character types, iterating over codepoints.

Example of use: 

```kotlin
RangeValueIterator iterator = UCharacter.getTypeIterator();
  RangeValueIterator.Element element = new RangeValueIterator.Element();
  while (iterator.next(element)) {
      System.out.println("Codepoint \\u" +
                         Integer.toHexString(element.start) +
                         " to codepoint \\u" +
                         Integer.toHexString(element.limit - 1) +
                         " has the character type " +
                         element.value);
  }
  
```

| Return ||
|-----------------------------------------------------------------------------------------------------------------|-------------|
| [RangeValueIterator](../android/icu/util/RangeValueIterator.md)! | an iterator |

### getUnicodeNumericValue

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getUnicodeNumericValue(ch: Int): Double
```

**\[icu\]**Returns the numeric value for a Unicode code point as defined in the Unicode Character Database.

A "double" return type is necessary because some numeric values are fractions, negative, or too large for int.

For characters without any numeric values in the Unicode Character Database, this function will return NO_NUMERIC_VALUE. Note: This is different from the Unicode Standard which specifies NaN as the default value.

*API Change:*In release 2.2 and prior, this API has a return type int and returns -1 when the argument ch does not have a corresponding numeric value. This has been changed to synch with ICU4C This corresponds to the ICU4C function u_getNumericValue.

| Parameters ||
|------|---------------------------------------------------------------------------------------------------------------------|
| `ch` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Code point to get the numeric value for. |

| Return ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------|
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | numeric value of ch, or NO_NUMERIC_VALUE if none is defined. |

### getUnicodeVersion

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getUnicodeVersion(): VersionInfo!
```

**\[icu\]**Returns the version of Unicode data used.

| Return ||
|---------------------------------------------------------------------------------------------------|---------------------------------|
| [VersionInfo](../android/icu/util/VersionInfo.md)! | the unicode version number used |

### hasBinaryProperty

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun hasBinaryProperty(
    ch: Int, 
    property: Int
): Boolean
```

**\[icu\]**Check a binary Unicode property for a code point.

Unicode, especially in version 3.2, defines many more properties than the original set in UnicodeData.txt.

This API is intended to reflect Unicode properties as defined in the Unicode Character Database (UCD) and Unicode Technical Reports (UTR).

For details about the properties see<http://www.unicode.org/>.

For names of Unicode properties see the UCD file PropertyAliases.txt.

This API does not check the validity of the codepoint.

Important: If ICU is built with UCD files from Unicode versions below 3.2, then properties marked with "new" are not or not fully available.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `ch` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):code point to test. |
| `property` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):selector constant from android.icu.lang.UProperty, identifies which binary property to check. |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true or false according to the binary Unicode property value for ch. Also false if property is out of bounds or if the Unicode version does not have data for the property at all, or not for this code point. |

**See Also**

- [android.icu.lang.UProperty](../android/icu/lang/UProperty.md) 

### hasBinaryProperty

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun hasBinaryProperty(
    s: CharSequence!, 
    property: Int
): Boolean
```

**\[icu\]** Returns true if the property is true for the string. Same as [hasBinaryProperty(int,int)](../android/icu/lang/UCharacter.md))if the string contains exactly one code point.

Most properties apply only to single code points. [UTS #51 Unicode Emoji](https://www.unicode.org/reports/tr51/#Emoji_Sets) defines several properties of strings.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `s` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:String to test. |
| `property` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):UProperty selector constant, identifies which binary property to check. Must be BINARY_START\<=which\<BINARY_LIMIT. |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true or false according to the binary Unicode property value for the string. Also false if`property`is out of bounds or if the Unicode version does not have data for the property at all. |

**See Also**

- [android.icu.lang.UProperty](../android/icu/lang/UProperty.md) 

### isBMP

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun isBMP(ch: Int): Boolean
```

**\[icu\]**Determines if the code point is in the BMP plane.

| Parameters ||
|------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| `ch` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):code point to be determined if it is not a supplementary character |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if code point is not a supplementary character |

### isBaseForm

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun isBaseForm(ch: Int): Boolean
```

**\[icu\]**Determines whether the specified code point is of base form. A code point of base form does not graphically combine with preceding characters, and is neither a control nor a format character.

| Parameters ||
|------|------------------------------------------------------------------------------------------------------------------------------|
| `ch` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):code point to be determined if it is of base form |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the code point is of base form |

### isDefined

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun isDefined(ch: Int): Boolean
```

Determines if a code point has a defined meaning in the up-to-date Unicode standard. E.g. supplementary code points though allocated space are not defined in Unicode yet. 
Up-to-date Unicode implementation of java.lang.Character.isDefined()

| Parameters ||
|------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `ch` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):code point to be determined if it is defined in the most current version of Unicode |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if this code point is defined in unicode |

### isDigit

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun isDigit(ch: Int): Boolean
```

Determines if a code point is a Java digit. 
This method observes the semantics of`java.lang.Character.isDigit()`. It returns true for decimal digits only. 
*Semantic Change:*In release 1.3.1 and prior, this treated numeric letters and other numbers as digits. This has been changed to conform to the java semantics.

| Parameters ||
|------|------------------------------------------------------------------------------------------------|
| `ch` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):code point to query |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if this code point is a digit |

### isHighSurrogate

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun isHighSurrogate(ch: Char): Boolean
```

Same as [Character.isHighSurrogate](../java/lang/Character.md)),

| Parameters ||
|------|------------------------------------------------------------------------------------------------|
| `ch` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html):the char to check |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if ch is a high (lead) surrogate |

### isHighSurrogate

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun isHighSurrogate(codePoint: Int): Boolean
```

Same as [Character.isHighSurrogate](../java/lang/Character.md)), except that the ICU version accepts`int`for code points.

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `codePoint` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the code point to check (In ICU 3.0-69 the type of this parameter was`char`.) |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if codePoint is a high (lead) surrogate |

### isISOControl

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun isISOControl(ch: Int): Boolean
```

Determines if the specified code point is an ISO control character. A code point is considered to be an ISO control character if it is in the range \\u0000 through \\u001F or in the range \\u007F through \\u009F. 
Up-to-date Unicode implementation of java.lang.Character.isISOControl()

| Parameters ||
|------|--------------------------------------------------------------------------------------------------------------------------------------|
| `ch` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):code point to determine if it is an ISO control character |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if code point is a ISO control character |

### isIdentifierIgnorable

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun isIdentifierIgnorable(ch: Int): Boolean
```

Determines if the specified code point should be regarded as an ignorable character in a Java identifier. A character is Java-identifier-ignorable if it has the general category Cf Formatting Control, or it is a non-Java-whitespace ISO control: U+0000..U+0008, U+000E..U+001B, U+007F..U+009F. 
Up-to-date Unicode implementation of java.lang.Character.isIdentifierIgnorable(). 
See [UTR #8](https://www.unicode.org/reports/tr8/).

Note that Unicode just recommends to ignore Cf (format controls).

| Parameters ||
|------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `ch` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):code point to be determined if it can be ignored in a Unicode identifier. |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the code point is ignorable |

### isJavaIdentifierPart

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun isJavaIdentifierPart(cp: Int): Boolean
```

Compatibility override of Java method, delegates to java.lang.Character.isJavaIdentifierPart.

| Parameters ||
|------|-------------------------------------------------------------------------------------------|
| `cp` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the code point |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the code point can continue a java identifier. |

### isJavaIdentifierStart

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun isJavaIdentifierStart(cp: Int): Boolean
```

Compatibility override of Java method, delegates to java.lang.Character.isJavaIdentifierStart.

| Parameters ||
|------|-------------------------------------------------------------------------------------------|
| `cp` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the code point |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the code point can start a java identifier. |

### isLegal

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun isLegal(ch: Int): Boolean
```

**\[icu\]**A code point is illegal if and only if

- Out of bounds, less than 0 or greater than UCharacter.MAX_VALUE
- A surrogate value, 0xD800 to 0xDFFF
- Not-a-character, having the form 0x xxFFFF or 0x xxFFFE

Note: legal does not mean that it is assigned in this version of Unicode.

<br />

| Parameters ||
|------|------------------------------------------------------------------------------------------------------------------------------------------|
| `ch` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):code point to determine if it is a legal code point by itself |

| Return ||
|------------------------------------------------------------------------------------|----------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if and only if legal. |

### isLegal

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun isLegal(str: String!): Boolean
```

**\[icu\]**A string is legal iff all its code points are legal. A code point is illegal if and only if

- Out of bounds, less than 0 or greater than UCharacter.MAX_VALUE
- A surrogate value, 0xD800 to 0xDFFF
- Not-a-character, having the form 0x xxFFFF or 0x xxFFFE

Note: legal does not mean that it is assigned in this version of Unicode.

<br />

| Parameters ||
|-------|--------------------------------------------------------------------------------------------------------------------|
| `str` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:containing code points to examin |

| Return ||
|------------------------------------------------------------------------------------|----------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if and only if legal. |

### isLetter

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun isLetter(ch: Int): Boolean
```

Determines if the specified code point is a letter. Up-to-date Unicode implementation of java.lang.Character.isLetter()

| Parameters ||
|------|----------------------------------------------------------------------------------------------------------------------|
| `ch` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):code point to determine if it is a letter |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if code point is a letter |

### isLetterOrDigit

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun isLetterOrDigit(ch: Int): Boolean
```

Determines if the specified code point is a letter or digit.**\[icu\] Note:**This method, unlike java.lang.Character does not regard the ascii characters 'A' - 'Z' and 'a' - 'z' as digits.

| Parameters ||
|------|---------------------------------------------------------------------------------------------------------------------------------|
| `ch` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):code point to determine if it is a letter or a digit |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if code point is a letter or a digit |

### isLowSurrogate

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun isLowSurrogate(ch: Char): Boolean
```

Same as [Character.isLowSurrogate](../java/lang/Character.md)),

| Parameters ||
|------|------------------------------------------------------------------------------------------------|
| `ch` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html):the char to check |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if ch is a low (trail) surrogate |

### isLowSurrogate

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun isLowSurrogate(codePoint: Int): Boolean
```

Same as [Character.isLowSurrogate](../java/lang/Character.md)), except that the ICU version accepts`int`for code points.

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `codePoint` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the code point to check (In ICU 3.0-69 the type of this parameter was`char`.) |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if codePoint is a low (trail) surrogate |

### isLowerCase

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun isLowerCase(ch: Int): Boolean
```

Determines if the specified code point is a lowercase character. UnicodeData only contains case mappings for code points where they are one-to-one mappings; it also omits information about context-sensitive case mappings. 
For more information about Unicode case mapping please refer to the [Technical report #21](https://www.unicode.org/reports/tr21/). 
Up-to-date Unicode implementation of java.lang.Character.isLowerCase()

| Parameters ||
|------|--------------------------------------------------------------------------------------------------------------------------|
| `ch` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):code point to determine if it is in lowercase |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if code point is a lowercase character |

### isMirrored

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun isMirrored(ch: Int): Boolean
```

Determines whether the code point has the "mirrored" property. This property is set for characters that are commonly used in Right-To-Left contexts and need to be displayed with a "mirrored" glyph.

| Parameters ||
|------|------------------------------------------------------------------------------------------------------------------------|
| `ch` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):code point whose mirror is to be determined |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the code point has the "mirrored" property |

### isPrintable

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun isPrintable(ch: Int): Boolean
```

**\[icu\]**Determines whether the specified code point is a printable character according to the Unicode standard.

| Parameters ||
|------|---------------------------------------------------------------------------------------------------------------------------|
| `ch` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):code point to be determined if it is printable |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the code point is a printable character |

### isSpaceChar

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun isSpaceChar(ch: Int): Boolean
```

Determines if the specified code point is a Unicode specified space character, i.e. if code point is in the category Zs, Zl and Zp. Up-to-date Unicode implementation of java.lang.Character.isSpaceChar().

| Parameters ||
|------|---------------------------------------------------------------------------------------------------------------------|
| `ch` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):code point to determine if it is a space |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the specified code point is a space character |

### isSupplementary

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun isSupplementary(ch: Int): Boolean
```

**\[icu\]** Determines if the code point is a supplementary character. A code point is a supplementary character if and only if it is greater than [SUPPLEMENTARY_MIN_VALUE](../android/icu/lang/UCharacter.md)

| Parameters ||
|------|--------------------------------------------------------------------------------------------------------------------------------------------|
| `ch` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):code point to be determined if it is in the supplementary plane |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if code point is a supplementary character |

### isSupplementaryCodePoint

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun isSupplementaryCodePoint(cp: Int): Boolean
```

Same as [Character.isSupplementaryCodePoint](../java/lang/Character.md)).

| Parameters ||
|------|----------------------------------------------------------------------------------------------------|
| `cp` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the code point to check |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if cp is a supplementary code point |

### isSurrogatePair

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun isSurrogatePair(
    high: Char, 
    low: Char
): Boolean
```

Same as [Character.isSurrogatePair](../java/lang/Character.md)).

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------|
| `high` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html):the high (lead) char |
| `low` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html):the low (trail) char |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if high, low form a surrogate pair |

### isSurrogatePair

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun isSurrogatePair(
    high: Int, 
    low: Int
): Boolean
```

Same as [Character.isSurrogatePair](../java/lang/Character.md)), except that the ICU version accepts`int`for code points.

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| `high` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the high (lead) unit (In ICU 3.0-69 the type of both parameters was`char`.) |
| `low` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the low (trail) unit |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if high, low form a surrogate pair |

### isTitleCase

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun isTitleCase(ch: Int): Boolean
```

Determines if the specified code point is a titlecase character. UnicodeData only contains case mappings for code points where they are one-to-one mappings; it also omits information about context-sensitive case mappings. 
For more information about Unicode case mapping please refer to the [Technical report #21](https://www.unicode.org/reports/tr21/). 
Up-to-date Unicode implementation of java.lang.Character.isTitleCase().

| Parameters ||
|------|---------------------------------------------------------------------------------------------------------------------------|
| `ch` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):code point to determine if it is in title case |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the specified code point is a titlecase character |

### isUAlphabetic

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun isUAlphabetic(ch: Int): Boolean
```

**\[icu\]**

Check if a code point has the Alphabetic Unicode property.

Same as UCharacter.hasBinaryProperty(ch, UProperty.ALPHABETIC).

Different from UCharacter.isLetter(ch)!

| Parameters ||
|------|---------------------------------------------------------------------------------------------------|
| `ch` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):codepoint to be tested |

### isULowercase

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun isULowercase(ch: Int): Boolean
```

**\[icu\]**

Check if a code point has the Lowercase Unicode property.

Same as UCharacter.hasBinaryProperty(ch, UProperty.LOWERCASE).

This is different from UCharacter.isLowerCase(ch)!

| Parameters ||
|------|---------------------------------------------------------------------------------------------------|
| `ch` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):codepoint to be tested |

### isUUppercase

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun isUUppercase(ch: Int): Boolean
```

**\[icu\]**

Check if a code point has the Uppercase Unicode property.

Same as UCharacter.hasBinaryProperty(ch, UProperty.UPPERCASE).

This is different from UCharacter.isUpperCase(ch)!

| Parameters ||
|------|---------------------------------------------------------------------------------------------------|
| `ch` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):codepoint to be tested |

### isUWhiteSpace

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun isUWhiteSpace(ch: Int): Boolean
```

**\[icu\]**

Check if a code point has the White_Space Unicode property.

Same as UCharacter.hasBinaryProperty(ch, UProperty.WHITE_SPACE).

This is different from both UCharacter.isSpace(ch) and UCharacter.isWhitespace(ch)!

| Parameters ||
|------|---------------------------------------------------------------------------------------------------|
| `ch` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):codepoint to be tested |

### isUnicodeIdentifierPart

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun isUnicodeIdentifierPart(ch: Int): Boolean
```

Determines if the specified character is permissible as a non-initial character of an identifier according to UAX #31 Unicode Identifier and Pattern Syntax.

Same as Unicode ID_Continue ([UProperty.ID_CONTINUE](../android/icu/lang/UProperty.md)).

Note that this differs from [java.lang.Character#isUnicodeIdentifierPart(char)](../java/lang/Character.md))which implements a different identifier profile.

| Parameters ||
|------|--------------------------------------------------------------------------------------------------------|
| `ch` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the code point to be tested |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the code point may occur as a non-initial character of an identifier |

### isUnicodeIdentifierStart

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun isUnicodeIdentifierStart(ch: Int): Boolean
```

Determines if the specified character is permissible as the first character in an identifier according to UAX #31 Unicode Identifier and Pattern Syntax.

Same as Unicode ID_Start ([UProperty.ID_START](../android/icu/lang/UProperty.md)).

Note that this differs from [java.lang.Character#isUnicodeIdentifierStart(char)](../java/lang/Character.md))which implements a different identifier profile.

| Parameters ||
|------|--------------------------------------------------------------------------------------------------------|
| `ch` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the code point to be tested |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the code point may start an identifier |

### isUpperCase

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun isUpperCase(ch: Int): Boolean
```

Determines if the specified code point is an uppercase character. UnicodeData only contains case mappings for code point where they are one-to-one mappings; it also omits information about context-sensitive case mappings. 
For language specific case conversion behavior, use toUpperCase(locale, str). 
For example, the case conversion for dot-less i and dotted I in Turkish, or for final sigma in Greek. For more information about Unicode case mapping please refer to the [Technical report #21](https://www.unicode.org/reports/tr21/). 
Up-to-date Unicode implementation of java.lang.Character.isUpperCase().

| Parameters ||
|------|--------------------------------------------------------------------------------------------------------------------------|
| `ch` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):code point to determine if it is in uppercase |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the code point is an uppercase character |

### isValidCodePoint

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun isValidCodePoint(cp: Int): Boolean
```

Equivalent to [Character.isValidCodePoint](../java/lang/Character.md)).

| Parameters ||
|------|----------------------------------------------------------------------------------------------------|
| `cp` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the code point to check |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if cp is a valid code point |

### isWhitespace

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun isWhitespace(ch: Int): Boolean
```

Determines if the specified code point is a white space character. A code point is considered to be an whitespace character if and only if it satisfies one of the following criteria:

- It is a Unicode Separator character (categories "Z" = "Zs" or "Zl" or "Zp"), but is not also a non-breaking space (\\u00A0 or \\u2007 or \\u202F).
- It is \\u0009, HORIZONTAL TABULATION.
- It is \\u000A, LINE FEED.
- It is \\u000B, VERTICAL TABULATION.
- It is \\u000C, FORM FEED.
- It is \\u000D, CARRIAGE RETURN.
- It is \\u001C, FILE SEPARATOR.
- It is \\u001D, GROUP SEPARATOR.
- It is \\u001E, RECORD SEPARATOR.
- It is \\u001F, UNIT SEPARATOR.

This API tries to sync with the semantics of Java's java.lang.Character.isWhitespace(), but it may not return the exact same results because of the Unicode version difference.

<br />

Note: Unicode 4.0.1 changed U+200B ZERO WIDTH SPACE from a Space Separator (Zs) to a Format Control (Cf). Since then, isWhitespace(0x200b) returns false. See http://www.unicode.org/versions/Unicode4.0.1/

| Parameters ||
|------|---------------------------------------------------------------------------------------------------------------------------|
| `ch` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):code point to determine if it is a white space |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the specified code point is a white space character |

### offsetByCodePoints

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun offsetByCodePoints(
    text: CharArray!, 
    start: Int, 
    count: Int, 
    index: Int, 
    codePointOffset: Int
): Int
```

Equivalent to the[Character.offsetByCodePoints(char[], int, int, int, int)](https://developer.android.com/reference/kotlin/java/lang/Character.html#offsetByCodePoints(kotlin.CharArray,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int))method, for convenience. Adjusts the char index by a code point offset.

| Parameters ||
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| `text` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!:the characters to check |
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the start of the range to check |
| `count` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the length of the range to check |
| --- | --- |
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index to adjust |
| `codePointOffset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of code points by which to offset the index |

| Return ||
|----------------------------------------------------------------------------|--------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the adjusted index |

### offsetByCodePoints

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun offsetByCodePoints(
    text: CharSequence!, 
    index: Int, 
    codePointOffset: Int
): Int
```

Equivalent to the [Character.offsetByCodePoints(CharSequence, int, int)](../java/lang/Character.md))method, for convenience. Adjusts the char index by a code point offset.

| Parameters ||
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| `text` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:the characters to check |
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index to adjust |
| `codePointOffset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of code points by which to offset the index |
| --- | --- |

| Return ||
|----------------------------------------------------------------------------|--------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the adjusted index |

### toChars

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun toChars(cp: Int): CharArray!
```

Same as [Character.toChars(int)](../java/lang/Character.md)). Returns a char array representing the code point.

| Parameters ||
|------|------------------------------------------------------------------------------------------------------|
| `cp` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the code point to convert |

| Return ||
|------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)! | an array containing the char(s) representing the code point |

| Exceptions ||
|--------------------------------------|---------------------------------|
| `java.lang.IllegalArgumentException` | if cp is not a valid code point |

### toChars

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun toChars(
    cp: Int, 
    dst: CharArray!, 
    dstIndex: Int
): Int
```

Same as[Character.toChars(int, char[], int)](https://developer.android.com/reference/kotlin/java/lang/Character.html#toChars(kotlin.Int,%20kotlin.CharArray,%20kotlin.Int)). Writes the chars representing the code point into the destination at the given index.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `cp` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the code point to convert |
| `dst` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!:the destination array into which to put the char(s) representing the code point |
| `dstIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index at which to put the first (or only) char |
| --- | --- |

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the count of the number of chars written (1 or 2) |

| Exceptions ||
|--------------------------------------|---------------------------------|
| `java.lang.IllegalArgumentException` | if cp is not a valid code point |

### toCodePoint

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun toCodePoint(
    high: Char, 
    low: Char
): Int
```

Same as [Character.toCodePoint](../java/lang/Character.md)). Returns the code point represented by the two surrogate code units. This does not check the surrogate pair for validity.

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------|
| `high` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html):the high (lead) surrogate |
| `low` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html):the low (trail) surrogate |

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the code point formed by the surrogate pair |

### toCodePoint

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun toCodePoint(
    high: Int, 
    low: Int
): Int
```

Same as [Character.toCodePoint](../java/lang/Character.md)), except that the ICU version accepts`int`for code points. Returns the code point represented by the two surrogate code units. This does not check the surrogate pair for validity.

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `high` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the high (lead) surrogate (In ICU 3.0-69 the type of both parameters was`char`.) |
| `low` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the low (trail) surrogate |

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the code point formed by the surrogate pair |

**See Also**

- [#getCodePoint(int, int)](../android/icu/lang/UCharacter.md)) 

### toLowerCase

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun toLowerCase(
    locale: ULocale!, 
    str: String!
): String!
```

Returns the lowercase version of the argument string. Casing is dependent on the argument locale and context-sensitive

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------|
| `locale` | [ULocale](../android/icu/util/ULocale.md)!:which string is to be converted in |
| `str` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:source string to be performed on |

| Return ||
|-----------------------------------------------------------------------------------|------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | lowercase version of the argument string |

### toLowerCase

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun toLowerCase(ch: Int): Int
```

The given code point is mapped to its lowercase equivalent; if the code point has no lowercase equivalent, the code point itself is returned. Up-to-date Unicode implementation of java.lang.Character.toLowerCase()

This function only returns the simple, single-code point case mapping. Full case mappings should be used whenever possible because they produce better results by working on whole strings. They take into account the string context and the language and can map to a result string with a different length as appropriate. Full case mappings are applied by the case mapping functions that take String parameters rather than code points (int). See also the User Guide chapter on C/POSIX migration: https://unicode-org.github.io/icu/userguide/icu/posix#case-mappings

| Parameters ||
|------|-------------------------------------------------------------------------------------------------------------------------------------|
| `ch` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):code point whose lowercase equivalent is to be retrieved |

| Return ||
|----------------------------------------------------------------------------|-------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the lowercase equivalent code point |

### toLowerCase

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun toLowerCase(str: String!): String!
```

Returns the lowercase version of the argument string. Casing is dependent on the default locale and context-sensitive

| Parameters ||
|-------|--------------------------------------------------------------------------------------------------------------------|
| `str` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:source string to be performed on |

| Return ||
|-----------------------------------------------------------------------------------|------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | lowercase version of the argument string |

### toLowerCase

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun toLowerCase(
    locale: Locale!, 
    str: String!
): String!
```

Returns the lowercase version of the argument string. Casing is dependent on the argument locale and context-sensitive

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------|
| `locale` | [Locale](../java/util/Locale.md)!:which string is to be converted in |
| `str` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:source string to be performed on |

| Return ||
|-----------------------------------------------------------------------------------|------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | lowercase version of the argument string |

### toString

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun toString(ch: Int): String!
```

Converts argument code point and returns a String object representing the code point's value in UTF-16 format. The result is a string whose length is 1 for BMP code points, 2 for supplementary ones.

Up-to-date Unicode implementation of java.lang.Character.toString().

| Parameters ||
|------|---------------------------------------------------------------------------------------|
| `ch` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):code point |

| Return ||
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | string representation of the code point, null if code point is not defined in unicode |

### toTitleCase

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun toTitleCase(
    locale: ULocale!, 
    str: String!, 
    titleIter: BreakIterator!
): String!
```

Returns the titlecase version of the argument string.

Position for titlecasing is determined by the argument break iterator, hence the user can customize his break iterator for a specialized titlecasing. In this case only the forward iteration needs to be implemented. If the break iterator passed in is null, the default Unicode algorithm will be used to determine the titlecase positions.

Only positions returned by the break iterator will be title cased, character in between the positions will all be in lower case.

Casing is dependent on the argument locale and context-sensitive

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `locale` | [ULocale](../android/icu/util/ULocale.md)!:which string is to be converted in |
| `str` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:source string to be performed on |
| `titleIter` | [BreakIterator](../android/icu/text/BreakIterator.md)!:break iterator to determine the positions in which the character should be title cased. |
| --- | --- |

| Return ||
|-----------------------------------------------------------------------------------|------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | titlecase version of the argument string |

### toTitleCase

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun toTitleCase(
    locale: ULocale!, 
    str: String!, 
    titleIter: BreakIterator!, 
    options: Int
): String!
```

Returns the titlecase version of the argument string.

Position for titlecasing is determined by the argument break iterator, hence the user can customize his break iterator for a specialized titlecasing. In this case only the forward iteration needs to be implemented. If the break iterator passed in is null, the default Unicode algorithm will be used to determine the titlecase positions.

Only positions returned by the break iterator will be title cased, character in between the positions will all be in lower case.

Casing is dependent on the argument locale and context-sensitive

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `locale` | [ULocale](../android/icu/util/ULocale.md)!:which string is to be converted in |
| `str` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:source string to be performed on |
| `titleIter` | [BreakIterator](../android/icu/text/BreakIterator.md)!:break iterator to determine the positions in which the character should be title cased. |
| --- | --- |
| `options` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):bit set to modify the titlecasing operation |

| Return ||
|-----------------------------------------------------------------------------------|------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | titlecase version of the argument string |

**See Also**

- [#TITLECASE_NO_LOWERCASE](../android/icu/lang/UCharacter.md)
- [#TITLECASE_NO_BREAK_ADJUSTMENT](../android/icu/lang/UCharacter.md) 

### toTitleCase

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun toTitleCase(ch: Int): Int
```

Converts the code point argument to titlecase. If no titlecase is available, the uppercase is returned. If no uppercase is available, the code point itself is returned. Up-to-date Unicode implementation of java.lang.Character.toTitleCase()

This function only returns the simple, single-code point case mapping. Full case mappings should be used whenever possible because they produce better results by working on whole strings. They take into account the string context and the language and can map to a result string with a different length as appropriate. Full case mappings are applied by the case mapping functions that take String parameters rather than code points (int). See also the User Guide chapter on C/POSIX migration: https://unicode-org.github.io/icu/userguide/icu/posix#case-mappings

| Parameters ||
|------|---------------------------------------------------------------------------------------------------------------------------|
| `ch` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):code point whose title case is to be retrieved |

| Return ||
|----------------------------------------------------------------------------|----------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | titlecase code point |

### toTitleCase

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun toTitleCase(
    str: String!, 
    breakiter: BreakIterator!
): String!
```

Returns the titlecase version of the argument string.

Position for titlecasing is determined by the argument break iterator, hence the user can customize his break iterator for a specialized titlecasing. In this case only the forward iteration needs to be implemented. If the break iterator passed in is null, the default Unicode algorithm will be used to determine the titlecase positions.

Only positions returned by the break iterator will be title cased, character in between the positions will all be in lower case.

Casing is dependent on the default locale and context-sensitive

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `str` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:source string to be performed on |
| `breakiter` | [BreakIterator](../android/icu/text/BreakIterator.md)!:break iterator to determine the positions in which the character should be title cased. |

| Return ||
|-----------------------------------------------------------------------------------|------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | titlecase version of the argument string |

### toTitleCase

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun toTitleCase(
    locale: Locale!, 
    str: String!, 
    breakiter: BreakIterator!
): String!
```

Returns the titlecase version of the argument string.

Position for titlecasing is determined by the argument break iterator, hence the user can customize his break iterator for a specialized titlecasing. In this case only the forward iteration needs to be implemented. If the break iterator passed in is null, the default Unicode algorithm will be used to determine the titlecase positions.

Only positions returned by the break iterator will be title cased, character in between the positions will all be in lower case.

Casing is dependent on the argument locale and context-sensitive

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `locale` | [Locale](../java/util/Locale.md)!:which string is to be converted in |
| `str` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:source string to be performed on |
| `breakiter` | [BreakIterator](../android/icu/text/BreakIterator.md)!:break iterator to determine the positions in which the character should be title cased. |
| --- | --- |

| Return ||
|-----------------------------------------------------------------------------------|------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | titlecase version of the argument string |

### toTitleCase

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun toTitleCase(
    locale: Locale!, 
    str: String!, 
    titleIter: BreakIterator!, 
    options: Int
): String!
```

**\[icu\]**

Returns the titlecase version of the argument string.

Position for titlecasing is determined by the argument break iterator, hence the user can customize his break iterator for a specialized titlecasing. In this case only the forward iteration needs to be implemented. If the break iterator passed in is null, the default Unicode algorithm will be used to determine the titlecase positions.

Only positions returned by the break iterator will be title cased, character in between the positions will all be in lower case.

Casing is dependent on the argument locale and context-sensitive

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `locale` | [Locale](../java/util/Locale.md)!:which string is to be converted in |
| `str` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:source string to be performed on |
| `titleIter` | [BreakIterator](../android/icu/text/BreakIterator.md)!:break iterator to determine the positions in which the character should be title cased. |
| --- | --- |
| `options` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):bit set to modify the titlecasing operation |

| Return ||
|-----------------------------------------------------------------------------------|------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | titlecase version of the argument string |

**See Also**

- [#TITLECASE_NO_LOWERCASE](../android/icu/lang/UCharacter.md)
- [#TITLECASE_NO_BREAK_ADJUSTMENT](../android/icu/lang/UCharacter.md) 

### toUpperCase

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun toUpperCase(
    locale: ULocale!, 
    str: String!
): String!
```

Returns the uppercase version of the argument string. Casing is dependent on the argument locale and context-sensitive.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------|
| `locale` | [ULocale](../android/icu/util/ULocale.md)!:which string is to be converted in |
| `str` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:source string to be performed on |

| Return ||
|-----------------------------------------------------------------------------------|------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | uppercase version of the argument string |

### toUpperCase

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun toUpperCase(ch: Int): Int
```

Converts the character argument to uppercase. If no uppercase is available, the character itself is returned. Up-to-date Unicode implementation of java.lang.Character.toUpperCase()

This function only returns the simple, single-code point case mapping. Full case mappings should be used whenever possible because they produce better results by working on whole strings. They take into account the string context and the language and can map to a result string with a different length as appropriate. Full case mappings are applied by the case mapping functions that take String parameters rather than code points (int). See also the User Guide chapter on C/POSIX migration: https://unicode-org.github.io/icu/userguide/icu/posix#case-mappings

| Parameters ||
|------|--------------------------------------------------------------------------------------------------------------------------|
| `ch` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):code point whose uppercase is to be retrieved |

| Return ||
|----------------------------------------------------------------------------|----------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | uppercase code point |

### toUpperCase

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun toUpperCase(str: String!): String!
```

Returns the uppercase version of the argument string. Casing is dependent on the default locale and context-sensitive.

| Parameters ||
|-------|--------------------------------------------------------------------------------------------------------------------|
| `str` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:source string to be performed on |

| Return ||
|-----------------------------------------------------------------------------------|------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | uppercase version of the argument string |

### toUpperCase

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun toUpperCase(
    locale: Locale!, 
    str: String!
): String!
```

Returns the uppercase version of the argument string. Casing is dependent on the argument locale and context-sensitive.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------|
| `locale` | [Locale](../java/util/Locale.md)!:which string is to be converted in |
| `str` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:source string to be performed on |

| Return ||
|-----------------------------------------------------------------------------------|------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | uppercase version of the argument string |
