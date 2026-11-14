# UProperty

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# UProperty

Kotlin| [Java](../android/icu/lang/UProperty.md) 
| --- | --- |

```
interface UProperty
```

| [android.icu.lang.UProperty](../android/icu/lang/UProperty.md) |

Selection constants for Unicode properties.

These constants are used in functions like UCharacter.hasBinaryProperty(int) to select one of the Unicode properties.

The properties APIs are intended to reflect Unicode properties as defined in the Unicode Character Database (UCD) and Unicode Technical Reports (UTR).

For details about the properties see [UAX #44: Unicode Character Database](http://www.unicode.org/reports/tr44/).

Important: If ICU is built with UCD files from Unicode versions below 3.2, then properties marked with "new" are not or not fully available. Check UCharacter.getUnicodeVersion() to be sure.

## Summary

| Nested classes ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [NameChoice](../android/icu/lang/UProperty.NameChoice.md) Selector constants for UCharacter. |

| Constants ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [AGE](../android/icu/lang/UProperty.md) String property Age. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ALPHABETIC](../android/icu/lang/UProperty.md) Binary property Alphabetic. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ASCII_HEX_DIGIT](../android/icu/lang/UProperty.md) Binary property ASCII_Hex_Digit (0-9 A-F a-f). |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BASIC_EMOJI](../android/icu/lang/UProperty.md) Binary property of strings Basic_Emoji. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BIDI_CLASS](../android/icu/lang/UProperty.md) Enumerated property Bidi_Class. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BIDI_CONTROL](../android/icu/lang/UProperty.md) Binary property Bidi_Control. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BIDI_MIRRORED](../android/icu/lang/UProperty.md) Binary property Bidi_Mirrored. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BIDI_MIRRORING_GLYPH](../android/icu/lang/UProperty.md) String property Bidi_Mirroring_Glyph. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BIDI_PAIRED_BRACKET](../android/icu/lang/UProperty.md) String property Bidi_Paired_Bracket (new in Unicode 6.3). |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BIDI_PAIRED_BRACKET_TYPE](../android/icu/lang/UProperty.md) Enumerated property Bidi_Paired_Bracket_Type (new in Unicode 6.3). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BINARY_START](../android/icu/lang/UProperty.md) First constant for binary Unicode properties. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BLOCK](../android/icu/lang/UProperty.md) Enumerated property Block. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CANONICAL_COMBINING_CLASS](../android/icu/lang/UProperty.md) Enumerated property Canonical_Combining_Class. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CASED](../android/icu/lang/UProperty.md) Binary property Cased. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CASE_FOLDING](../android/icu/lang/UProperty.md) String property Case_Folding. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CASE_IGNORABLE](../android/icu/lang/UProperty.md) Binary property Case_Ignorable. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CASE_SENSITIVE](../android/icu/lang/UProperty.md) Binary property Case_Sensitive. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CHANGES_WHEN_CASEFOLDED](../android/icu/lang/UProperty.md) Binary property Changes_When_Casefolded. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CHANGES_WHEN_CASEMAPPED](../android/icu/lang/UProperty.md) Binary property Changes_When_Casemapped. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CHANGES_WHEN_LOWERCASED](../android/icu/lang/UProperty.md) Binary property Changes_When_Lowercased. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CHANGES_WHEN_NFKC_CASEFOLDED](../android/icu/lang/UProperty.md) Binary property Changes_When_NFKC_Casefolded. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CHANGES_WHEN_TITLECASED](../android/icu/lang/UProperty.md) Binary property Changes_When_Titlecased. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CHANGES_WHEN_UPPERCASED](../android/icu/lang/UProperty.md) Binary property Changes_When_Uppercased. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DASH](../android/icu/lang/UProperty.md) Binary property Dash. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DECOMPOSITION_TYPE](../android/icu/lang/UProperty.md) Enumerated property Decomposition_Type. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DEFAULT_IGNORABLE_CODE_POINT](../android/icu/lang/UProperty.md) Binary property Default_Ignorable_Code_Point (new). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DEPRECATED](../android/icu/lang/UProperty.md) Binary property Deprecated (new). |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DIACRITIC](../android/icu/lang/UProperty.md) Binary property Diacritic. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DOUBLE_START](../android/icu/lang/UProperty.md) First constant for double Unicode properties. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EAST_ASIAN_WIDTH](../android/icu/lang/UProperty.md) Enumerated property East_Asian_Width. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EMOJI](../android/icu/lang/UProperty.md) Binary property Emoji. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EMOJI_COMPONENT](../android/icu/lang/UProperty.md) Binary property Emoji_Component. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EMOJI_KEYCAP_SEQUENCE](../android/icu/lang/UProperty.md) Binary property of strings Emoji_Keycap_Sequence. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EMOJI_MODIFIER](../android/icu/lang/UProperty.md) Binary property Emoji_Modifier. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EMOJI_MODIFIER_BASE](../android/icu/lang/UProperty.md) Binary property Emoji_Modifier_Base. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EMOJI_PRESENTATION](../android/icu/lang/UProperty.md) Binary property Emoji_Presentation. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EXTENDED_PICTOGRAPHIC](../android/icu/lang/UProperty.md) Binary property Extended_Pictographic. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EXTENDER](../android/icu/lang/UProperty.md) Binary property Extender. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FULL_COMPOSITION_EXCLUSION](../android/icu/lang/UProperty.md) Binary property Full_Composition_Exclusion. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [GENERAL_CATEGORY](../android/icu/lang/UProperty.md) Enumerated property General_Category. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [GENERAL_CATEGORY_MASK](../android/icu/lang/UProperty.md) Bitmask property General_Category_Mask. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [GRAPHEME_BASE](../android/icu/lang/UProperty.md) Binary property Grapheme_Base (new). |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [GRAPHEME_CLUSTER_BREAK](../android/icu/lang/UProperty.md) Enumerated property Grapheme_Cluster_Break (new in Unicode 4.1). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [GRAPHEME_EXTEND](../android/icu/lang/UProperty.md) Binary property Grapheme_Extend (new). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [GRAPHEME_LINK](../android/icu/lang/UProperty.md) Binary property Grapheme_Link (new). |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [HANGUL_SYLLABLE_TYPE](../android/icu/lang/UProperty.md) Enumerated property Hangul_Syllable_Type, new in Unicode 4. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [HEX_DIGIT](../android/icu/lang/UProperty.md) Binary property Hex_Digit. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [HYPHEN](../android/icu/lang/UProperty.md) Binary property Hyphen. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [IDEOGRAPHIC](../android/icu/lang/UProperty.md) Binary property Ideographic. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [IDS_BINARY_OPERATOR](../android/icu/lang/UProperty.md) Binary property IDS_Binary_Operator (new). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [IDS_TRINARY_OPERATOR](../android/icu/lang/UProperty.md) Binary property IDS_Trinary_Operator (new). |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [IDS_UNARY_OPERATOR](../android/icu/lang/UProperty.md) Binary property IDS_Unary_Operator. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ID_COMPAT_MATH_CONTINUE](../android/icu/lang/UProperty.md) Binary property ID_Compat_Math_Continue. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ID_COMPAT_MATH_START](../android/icu/lang/UProperty.md) Binary property ID_Compat_Math_Start. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ID_CONTINUE](../android/icu/lang/UProperty.md) Binary property ID_Continue. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ID_START](../android/icu/lang/UProperty.md) Binary property ID_Start. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [INDIC_POSITIONAL_CATEGORY](../android/icu/lang/UProperty.md) Enumerated property Indic_Positional_Category. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [INDIC_SYLLABIC_CATEGORY](../android/icu/lang/UProperty.md) Enumerated property Indic_Syllabic_Category. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [INT_START](../android/icu/lang/UProperty.md) First constant for enumerated/integer Unicode properties. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [JOINING_GROUP](../android/icu/lang/UProperty.md) Enumerated property Joining_Group. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [JOINING_TYPE](../android/icu/lang/UProperty.md) Enumerated property Joining_Type. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [JOIN_CONTROL](../android/icu/lang/UProperty.md) Binary property Join_Control. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LEAD_CANONICAL_COMBINING_CLASS](../android/icu/lang/UProperty.md) Enumerated property Lead_Canonical_Combining_Class. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LINE_BREAK](../android/icu/lang/UProperty.md) Enumerated property Line_Break. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LOGICAL_ORDER_EXCEPTION](../android/icu/lang/UProperty.md) Binary property Logical_Order_Exception (new). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LOWERCASE](../android/icu/lang/UProperty.md) Binary property Lowercase. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LOWERCASE_MAPPING](../android/icu/lang/UProperty.md) String property Lowercase_Mapping. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MASK_START](../android/icu/lang/UProperty.md) First constant for bit-mask Unicode properties. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MATH](../android/icu/lang/UProperty.md) Binary property Math. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [NAME](../android/icu/lang/UProperty.md) String property Name. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [NFC_INERT](../android/icu/lang/UProperty.md) Binary property NFC_Inert. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [NFC_QUICK_CHECK](../android/icu/lang/UProperty.md) Enumerated property NFC_Quick_Check. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [NFD_INERT](../android/icu/lang/UProperty.md) Binary property NFD_Inert. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [NFD_QUICK_CHECK](../android/icu/lang/UProperty.md) Enumerated property NFD_Quick_Check. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [NFKC_INERT](../android/icu/lang/UProperty.md) Binary property NFKC_Inert. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [NFKC_QUICK_CHECK](../android/icu/lang/UProperty.md) Enumerated property NFKC_Quick_Check. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [NFKD_INERT](../android/icu/lang/UProperty.md) Binary property NFKD_Inert. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [NFKD_QUICK_CHECK](../android/icu/lang/UProperty.md) Enumerated property NFKD_Quick_Check. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [NONCHARACTER_CODE_POINT](../android/icu/lang/UProperty.md) Binary property Noncharacter_Code_Point. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [NUMERIC_TYPE](../android/icu/lang/UProperty.md) Enumerated property Numeric_Type. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [NUMERIC_VALUE](../android/icu/lang/UProperty.md) Double property Numeric_Value. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [OTHER_PROPERTY_START](../android/icu/lang/UProperty.md) First constant for Unicode properties with unusual value types. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PATTERN_SYNTAX](../android/icu/lang/UProperty.md) Binary property Pattern_Syntax (new in Unicode 4.1). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PATTERN_WHITE_SPACE](../android/icu/lang/UProperty.md) Binary property Pattern_White_Space (new in Unicode 4.1). |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [POSIX_ALNUM](../android/icu/lang/UProperty.md) Binary property alnum (a C/POSIX character class). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [POSIX_BLANK](../android/icu/lang/UProperty.md) Binary property blank (a C/POSIX character class). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [POSIX_GRAPH](../android/icu/lang/UProperty.md) Binary property graph (a C/POSIX character class). |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [POSIX_PRINT](../android/icu/lang/UProperty.md) Binary property print (a C/POSIX character class). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [POSIX_XDIGIT](../android/icu/lang/UProperty.md) Binary property xdigit (a C/POSIX character class). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PREPENDED_CONCATENATION_MARK](../android/icu/lang/UProperty.md) Binary property Prepended_Concatenation_Mark. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [QUOTATION_MARK](../android/icu/lang/UProperty.md) Binary property Quotation_Mark. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RADICAL](../android/icu/lang/UProperty.md) Binary property Radical (new). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [REGIONAL_INDICATOR](../android/icu/lang/UProperty.md) Binary property Regional_Indicator. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RGI_EMOJI](../android/icu/lang/UProperty.md) Binary property of strings RGI_Emoji. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RGI_EMOJI_FLAG_SEQUENCE](../android/icu/lang/UProperty.md) Binary property of strings RGI_Emoji_Flag_Sequence. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RGI_EMOJI_MODIFIER_SEQUENCE](../android/icu/lang/UProperty.md) Binary property of strings RGI_Emoji_Modifier_Sequence. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RGI_EMOJI_TAG_SEQUENCE](../android/icu/lang/UProperty.md) Binary property of strings RGI_Emoji_Tag_Sequence. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RGI_EMOJI_ZWJ_SEQUENCE](../android/icu/lang/UProperty.md) Binary property of strings RGI_Emoji_ZWJ_Sequence. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SCRIPT](../android/icu/lang/UProperty.md) Enumerated property Script. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SCRIPT_EXTENSIONS](../android/icu/lang/UProperty.md) Miscellaneous property Script_Extensions (new in Unicode 6.0). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SEGMENT_STARTER](../android/icu/lang/UProperty.md) Binary Property Segment_Starter. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SENTENCE_BREAK](../android/icu/lang/UProperty.md) Enumerated property Sentence_Break (new in Unicode 4.1). |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SIMPLE_CASE_FOLDING](../android/icu/lang/UProperty.md) String property Simple_Case_Folding. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SIMPLE_LOWERCASE_MAPPING](../android/icu/lang/UProperty.md) String property Simple_Lowercase_Mapping. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SIMPLE_TITLECASE_MAPPING](../android/icu/lang/UProperty.md) String property Simple_Titlecase_Mapping. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SIMPLE_UPPERCASE_MAPPING](../android/icu/lang/UProperty.md) String property Simple_Uppercase_Mapping. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SOFT_DOTTED](../android/icu/lang/UProperty.md) Binary property Soft_Dotted (new). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STRING_START](../android/icu/lang/UProperty.md) First constant for string Unicode properties. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [S_TERM](../android/icu/lang/UProperty.md) Binary property STerm (new in Unicode 4.0.1). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TERMINAL_PUNCTUATION](../android/icu/lang/UProperty.md) Binary property Terminal_Punctuation. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TITLECASE_MAPPING](../android/icu/lang/UProperty.md) String property Titlecase_Mapping. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TRAIL_CANONICAL_COMBINING_CLASS](../android/icu/lang/UProperty.md) Enumerated property Trail_Canonical_Combining_Class. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [UNIFIED_IDEOGRAPH](../android/icu/lang/UProperty.md) Binary property Unified_Ideograph (new). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [UPPERCASE](../android/icu/lang/UProperty.md) Binary property Uppercase. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [UPPERCASE_MAPPING](../android/icu/lang/UProperty.md) String property Uppercase_Mapping. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [VARIATION_SELECTOR](../android/icu/lang/UProperty.md) Binary property Variation_Selector (new in Unicode 4.0.1). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [VERTICAL_ORIENTATION](../android/icu/lang/UProperty.md) Enumerated property Vertical_Orientation. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [WHITE_SPACE](../android/icu/lang/UProperty.md) Binary property White_Space. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [WORD_BREAK](../android/icu/lang/UProperty.md) Enumerated property Word_Break (new in Unicode 4.1). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [XID_CONTINUE](../android/icu/lang/UProperty.md) Binary property XID_Continue. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [XID_START](../android/icu/lang/UProperty.md) Binary property XID_Start. |

## Constants

### AGE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val AGE: Int
```

String property Age. Corresponds to UCharacter.getAge(int). 

 Value: 16384

### ALPHABETIC

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ALPHABETIC: Int
```

Binary property Alphabetic.

Property for UCharacter.isUAlphabetic(), different from the property in UCharacter.isalpha().

Lu + Ll + Lt + Lm + Lo + Nl + Other_Alphabetic. 

 Value: 0

### ASCII_HEX_DIGIT

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ASCII_HEX_DIGIT: Int
```

Binary property ASCII_Hex_Digit (0-9 A-F a-f). 

 Value: 1

### BASIC_EMOJI

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BASIC_EMOJI: Int
```

Binary property of strings Basic_Emoji. See https://www.unicode.org/reports/tr51/#Emoji_Sets 

 Value: 65

### BIDI_CLASS

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BIDI_CLASS: Int
```

Enumerated property Bidi_Class. Same as UCharacter.getDirection(int), returns UCharacterDirection values. 

 Value: 4096

### BIDI_CONTROL

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BIDI_CONTROL: Int
```

Binary property Bidi_Control.

Format controls which have specific functions in the Bidi Algorithm. 

 Value: 2

### BIDI_MIRRORED

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BIDI_MIRRORED: Int
```

Binary property Bidi_Mirrored.

Characters that may change display in RTL text.

Property for UCharacter.isMirrored().

See Bidi Algorithm; UTR 9. 

 Value: 3

### BIDI_MIRRORING_GLYPH

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BIDI_MIRRORING_GLYPH: Int
```

String property Bidi_Mirroring_Glyph. Corresponds to UCharacter.getMirror(int). 

 Value: 16385

### BIDI_PAIRED_BRACKET

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BIDI_PAIRED_BRACKET: Int
```

String property Bidi_Paired_Bracket (new in Unicode 6.3). Corresponds to UCharacter.getBidiPairedBracket. 

 Value: 16397

### BIDI_PAIRED_BRACKET_TYPE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BIDI_PAIRED_BRACKET_TYPE: Int
```

Enumerated property Bidi_Paired_Bracket_Type (new in Unicode 6.3). Used in UAX #9: Unicode Bidirectional Algorithm (http://www.unicode.org/reports/tr9/) Returns UCharacter.BidiPairedBracketType values. 

 Value: 4117

### BINARY_START

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BINARY_START: Int
```

First constant for binary Unicode properties. 

 Value: 0

### BLOCK

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BLOCK: Int
```

Enumerated property Block. Same as UCharacter.UnicodeBlock.of(int), returns UCharacter.UnicodeBlock values. 

 Value: 4097

### CANONICAL_COMBINING_CLASS

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CANONICAL_COMBINING_CLASS: Int
```

Enumerated property Canonical_Combining_Class. Same as UCharacter.getCombiningClass(int), returns 8-bit numeric values. 

 Value: 4098

### CASED

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CASED: Int
```

Binary property Cased. For Lowercase, Uppercase and Titlecase characters. 

 Value: 49

### CASE_FOLDING

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CASE_FOLDING: Int
```

String property Case_Folding. Corresponds to UCharacter.foldCase(String, boolean). 

 Value: 16386

### CASE_IGNORABLE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CASE_IGNORABLE: Int
```

Binary property Case_Ignorable. Used in context-sensitive case mappings. 

 Value: 50

### CASE_SENSITIVE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CASE_SENSITIVE: Int
```

Binary property Case_Sensitive.

Either the source of a case mapping or*in*the target of a case mapping. Not the same as the general category Cased_Letter. 

 Value: 34

### CHANGES_WHEN_CASEFOLDED

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CHANGES_WHEN_CASEFOLDED: Int
```

Binary property Changes_When_Casefolded. 

 Value: 54

### CHANGES_WHEN_CASEMAPPED

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CHANGES_WHEN_CASEMAPPED: Int
```

Binary property Changes_When_Casemapped. 

 Value: 55

### CHANGES_WHEN_LOWERCASED

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CHANGES_WHEN_LOWERCASED: Int
```

Binary property Changes_When_Lowercased. 

 Value: 51

### CHANGES_WHEN_NFKC_CASEFOLDED

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CHANGES_WHEN_NFKC_CASEFOLDED: Int
```

Binary property Changes_When_NFKC_Casefolded. 

 Value: 56

### CHANGES_WHEN_TITLECASED

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CHANGES_WHEN_TITLECASED: Int
```

Binary property Changes_When_Titlecased. 

 Value: 53

### CHANGES_WHEN_UPPERCASED

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CHANGES_WHEN_UPPERCASED: Int
```

Binary property Changes_When_Uppercased. 

 Value: 52

### DASH

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DASH: Int
```

Binary property Dash.

Variations of dashes. 

 Value: 4

### DECOMPOSITION_TYPE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DECOMPOSITION_TYPE: Int
```

Enumerated property Decomposition_Type. Returns UCharacter.DecompositionType values. 

 Value: 4099

### DEFAULT_IGNORABLE_CODE_POINT

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DEFAULT_IGNORABLE_CODE_POINT: Int
```

Binary property Default_Ignorable_Code_Point (new).

Property that indicates codepoint is ignorable in most processing.

Codepoints (2060..206F, FFF0..FFFB, E0000..E0FFF) + Other_Default_Ignorable_Code_Point + (Cf + Cc + Cs - White_Space) 

 Value: 5

### DEPRECATED

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DEPRECATED: Int
```

Binary property Deprecated (new).

The usage of deprecated characters is strongly discouraged. 

 Value: 6

### DIACRITIC

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DIACRITIC: Int
```

Binary property Diacritic.

Characters that linguistically modify the meaning of another character to which they apply. 

 Value: 7

### DOUBLE_START

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DOUBLE_START: Int
```

First constant for double Unicode properties. 

 Value: 12288

### EAST_ASIAN_WIDTH

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EAST_ASIAN_WIDTH: Int
```

Enumerated property East_Asian_Width. See http://www.unicode.org/reports/tr11/ Returns UCharacter.EastAsianWidth values. 

 Value: 4100

### EMOJI

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EMOJI: Int
```

Binary property Emoji. See http://www.unicode.org/reports/tr51/#Emoji_Properties 

 Value: 57

### EMOJI_COMPONENT

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EMOJI_COMPONENT: Int
```

Binary property Emoji_Component. See http://www.unicode.org/reports/tr51/#Emoji_Properties 

 Value: 61

### EMOJI_KEYCAP_SEQUENCE

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EMOJI_KEYCAP_SEQUENCE: Int
```

Binary property of strings Emoji_Keycap_Sequence. See https://www.unicode.org/reports/tr51/#Emoji_Sets 

 Value: 66

### EMOJI_MODIFIER

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EMOJI_MODIFIER: Int
```

Binary property Emoji_Modifier. See http://www.unicode.org/reports/tr51/#Emoji_Properties 

 Value: 59

### EMOJI_MODIFIER_BASE

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EMOJI_MODIFIER_BASE: Int
```

Binary property Emoji_Modifier_Base. See http://www.unicode.org/reports/tr51/#Emoji_Properties 

 Value: 60

### EMOJI_PRESENTATION

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EMOJI_PRESENTATION: Int
```

Binary property Emoji_Presentation. See http://www.unicode.org/reports/tr51/#Emoji_Properties 

 Value: 58

### EXTENDED_PICTOGRAPHIC

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTENDED_PICTOGRAPHIC: Int
```

Binary property Extended_Pictographic. See http://www.unicode.org/reports/tr51/#Emoji_Properties 

 Value: 64

### EXTENDER

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTENDER: Int
```

Binary property Extender.

Extend the value or shape of a preceding alphabetic character, e.g. length and iteration marks. 

 Value: 8

### FULL_COMPOSITION_EXCLUSION

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FULL_COMPOSITION_EXCLUSION: Int
```

Binary property Full_Composition_Exclusion.

CompositionExclusions.txt + Singleton Decompositions + Non-Starter Decompositions. 

 Value: 9

### GENERAL_CATEGORY

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val GENERAL_CATEGORY: Int
```

Enumerated property General_Category. Same as UCharacter.getType(int), returns UCharacterCategory values. 

 Value: 4101

### GENERAL_CATEGORY_MASK

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val GENERAL_CATEGORY_MASK: Int
```

Bitmask property General_Category_Mask. This is the General_Category property returned as a bit mask. When used in UCharacter.getIntPropertyValue(c), returns bit masks for UCharacterCategory values where exactly one bit is set. When used with UCharacter.getPropertyValueName() and UCharacter.getPropertyValueEnum(), a multi-bit mask is used for sets of categories like "Letters". 

 Value: 8192

### GRAPHEME_BASE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val GRAPHEME_BASE: Int
```

Binary property Grapheme_Base (new).

For programmatic determination of grapheme cluster boundaries. \[0..10FFFF\]-Cc-Cf-Cs-Co-Cn-Zl-Zp-Grapheme_Link-Grapheme_Extend-CGJ 

 Value: 10

### GRAPHEME_CLUSTER_BREAK

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val GRAPHEME_CLUSTER_BREAK: Int
```

Enumerated property Grapheme_Cluster_Break (new in Unicode 4.1). Used in UAX #29: Text Boundaries (http://www.unicode.org/reports/tr29/) Returns UCharacter.GraphemeClusterBreak values. 

 Value: 4114

### GRAPHEME_EXTEND

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val GRAPHEME_EXTEND: Int
```

Binary property Grapheme_Extend (new).

For programmatic determination of grapheme cluster boundaries.

Me+Mn+Mc+Other_Grapheme_Extend-Grapheme_Link-CGJ 

 Value: 11

### GRAPHEME_LINK

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val GRAPHEME_LINK: Int
```

Binary property Grapheme_Link (new).

For programmatic determination of grapheme cluster boundaries. 

 Value: 12

### HANGUL_SYLLABLE_TYPE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val HANGUL_SYLLABLE_TYPE: Int
```

Enumerated property Hangul_Syllable_Type, new in Unicode 4. Returns UCharacter.HangulSyllableType values. 

 Value: 4107

### HEX_DIGIT

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val HEX_DIGIT: Int
```

Binary property Hex_Digit.

Characters commonly used for hexadecimal numbers. 

 Value: 13

### HYPHEN

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val HYPHEN: Int
```

Binary property Hyphen.

Dashes used to mark connections between pieces of words, plus the Katakana middle dot. 

 Value: 14

### IDEOGRAPHIC

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val IDEOGRAPHIC: Int
```

Binary property Ideographic.

CJKV ideographs. 

 Value: 17

### IDS_BINARY_OPERATOR

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val IDS_BINARY_OPERATOR: Int
```

Binary property IDS_Binary_Operator (new).

For programmatic determination of Ideographic Description Sequences. 

 Value: 18

### IDS_TRINARY_OPERATOR

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val IDS_TRINARY_OPERATOR: Int
```

Binary property IDS_Trinary_Operator (new).

For programmatic determination of Ideographic Description Sequences. 

 Value: 19

### IDS_UNARY_OPERATOR

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val IDS_UNARY_OPERATOR: Int
```

Binary property IDS_Unary_Operator. For programmatic determination of Ideographic Description Sequences. 

 Value: 72

### ID_COMPAT_MATH_CONTINUE

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ID_COMPAT_MATH_CONTINUE: Int
```

Binary property ID_Compat_Math_Continue.

Used in mathematical identifier profile in UAX #31. 

 Value: 74

### ID_COMPAT_MATH_START

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ID_COMPAT_MATH_START: Int
```

Binary property ID_Compat_Math_Start.

Used in mathematical identifier profile in UAX #31. 

 Value: 73

### ID_CONTINUE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ID_CONTINUE: Int
```

Binary property ID_Continue.

Characters that can continue an identifier.

ID_Start+Mn+Mc+Nd+Pc 

 Value: 15

### ID_START

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ID_START: Int
```

Binary property ID_Start.

Characters that can start an identifier.

Lu+Ll+Lt+Lm+Lo+Nl 

 Value: 16

### INDIC_POSITIONAL_CATEGORY

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val INDIC_POSITIONAL_CATEGORY: Int
```

Enumerated property Indic_Positional_Category. New in Unicode 6.0 as provisional property Indic_Matra_Category; renamed and changed to informative in Unicode 8.0. See http://www.unicode.org/reports/tr44/#IndicPositionalCategory.txt 

 Value: 4118

### INDIC_SYLLABIC_CATEGORY

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val INDIC_SYLLABIC_CATEGORY: Int
```

Enumerated property Indic_Syllabic_Category. New in Unicode 6.0 as provisional; informative since Unicode 8.0. See http://www.unicode.org/reports/tr44/#IndicSyllabicCategory.txt 

 Value: 4119

### INT_START

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val INT_START: Int
```

First constant for enumerated/integer Unicode properties. 

 Value: 4096

### JOINING_GROUP

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val JOINING_GROUP: Int
```

Enumerated property Joining_Group. Returns UCharacter.JoiningGroup values. 

 Value: 4102

### JOINING_TYPE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val JOINING_TYPE: Int
```

Enumerated property Joining_Type. Returns UCharacter.JoiningType values. 

 Value: 4103

### JOIN_CONTROL

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val JOIN_CONTROL: Int
```

Binary property Join_Control.

Format controls for cursive joining and ligation. 

 Value: 20

### LEAD_CANONICAL_COMBINING_CLASS

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LEAD_CANONICAL_COMBINING_CLASS: Int
```

Enumerated property Lead_Canonical_Combining_Class. ICU-specific property for the ccc of the first code point of the decomposition, or lccc(c)=ccc(NFD(c)\[0\]). Useful for checking for canonically ordered text; see Normalizer.FCD and http://www.unicode.org/notes/tn5/#FCD . Returns 8-bit numeric values like CANONICAL_COMBINING_CLASS. 

 Value: 4112

### LINE_BREAK

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LINE_BREAK: Int
```

Enumerated property Line_Break. Returns UCharacter.LineBreak values. 

 Value: 4104

### LOGICAL_ORDER_EXCEPTION

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LOGICAL_ORDER_EXCEPTION: Int
```

Binary property Logical_Order_Exception (new).

Characters that do not use logical order and require special handling in most processing. 

 Value: 21

### LOWERCASE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LOWERCASE: Int
```

Binary property Lowercase.

Same as UCharacter.isULowercase(), different from UCharacter.islower().

Ll+Other_Lowercase 

 Value: 22

### LOWERCASE_MAPPING

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LOWERCASE_MAPPING: Int
```

String property Lowercase_Mapping. Corresponds to UCharacter.toLowerCase(String). 

 Value: 16388

### MASK_START

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MASK_START: Int
```

First constant for bit-mask Unicode properties. 

 Value: 8192

### MATH

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MATH: Int
```

Binary property Math.

Sm+Other_Math 

 Value: 23

### NAME

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NAME: Int
```

String property Name. Corresponds to UCharacter.getName(int). 

 Value: 16389

### NFC_INERT

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NFC_INERT: Int
```

Binary property NFC_Inert. ICU-specific property for characters that are inert under NFC, i.e., they do not interact with adjacent characters. Used for example in normalizing transforms in incremental mode to find the boundary of safely normalizable text despite possible text additions. 

 Value: 39

**See Also**

- [#NFD_INERT](../android/icu/lang/UProperty.md) 

### NFC_QUICK_CHECK

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NFC_QUICK_CHECK: Int
```

Enumerated property NFC_Quick_Check. Returns numeric values compatible with Normalizer.QuickCheckResult. 

 Value: 4110

### NFD_INERT

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NFD_INERT: Int
```

Binary property NFD_Inert. ICU-specific property for characters that are inert under NFD, i.e., they do not interact with adjacent characters. Used for example in normalizing transforms in incremental mode to find the boundary of safely normalizable text despite possible text additions. There is one such property per normalization form. These properties are computed as follows - an inert character is: a) unassigned, or ALL of the following: b) of combining class 0. c) not decomposed by this normalization form. AND if NFC or NFKC, d) can never compose with a previous character. e) can never compose with a following character. f) can never change if another character is added. Example: a-breve might satisfy all but f, but if you add an ogonek it changes to a-ogonek + breve See also com.ibm.text.UCD.NFSkippable in the ICU4J repository, and icu/source/common/unormimp.h . 

 Value: 37

### NFD_QUICK_CHECK

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NFD_QUICK_CHECK: Int
```

Enumerated property NFD_Quick_Check. Returns numeric values compatible with Normalizer.QuickCheckResult. 

 Value: 4108

### NFKC_INERT

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NFKC_INERT: Int
```

Binary property NFKC_Inert. ICU-specific property for characters that are inert under NFKC, i.e., they do not interact with adjacent characters. Used for example in normalizing transforms in incremental mode to find the boundary of safely normalizable text despite possible text additions. 

 Value: 40

**See Also**

- [#NFD_INERT](../android/icu/lang/UProperty.md) 

### NFKC_QUICK_CHECK

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NFKC_QUICK_CHECK: Int
```

Enumerated property NFKC_Quick_Check. Returns numeric values compatible with Normalizer.QuickCheckResult. 

 Value: 4111

### NFKD_INERT

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NFKD_INERT: Int
```

Binary property NFKD_Inert. ICU-specific property for characters that are inert under NFKD, i.e., they do not interact with adjacent characters. Used for example in normalizing transforms in incremental mode to find the boundary of safely normalizable text despite possible text additions. 

 Value: 38

**See Also**

- [#NFD_INERT](../android/icu/lang/UProperty.md) 

### NFKD_QUICK_CHECK

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NFKD_QUICK_CHECK: Int
```

Enumerated property NFKD_Quick_Check. Returns numeric values compatible with Normalizer.QuickCheckResult. 

 Value: 4109

### NONCHARACTER_CODE_POINT

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NONCHARACTER_CODE_POINT: Int
```

Binary property Noncharacter_Code_Point.

Code points that are explicitly defined as illegal for the encoding of characters. 

 Value: 24

### NUMERIC_TYPE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NUMERIC_TYPE: Int
```

Enumerated property Numeric_Type. Returns UCharacter.NumericType values. 

 Value: 4105

### NUMERIC_VALUE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NUMERIC_VALUE: Int
```

Double property Numeric_Value. Corresponds to UCharacter.getUnicodeNumericValue(int). 

 Value: 12288

### OTHER_PROPERTY_START

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val OTHER_PROPERTY_START: Int
```

First constant for Unicode properties with unusual value types. 

 Value: 28672

### PATTERN_SYNTAX

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PATTERN_SYNTAX: Int
```

Binary property Pattern_Syntax (new in Unicode 4.1). See UAX #31 Identifier and Pattern Syntax (http://www.unicode.org/reports/tr31/) 

 Value: 42

### PATTERN_WHITE_SPACE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PATTERN_WHITE_SPACE: Int
```

Binary property Pattern_White_Space (new in Unicode 4.1). See UAX #31 Identifier and Pattern Syntax (http://www.unicode.org/reports/tr31/) 

 Value: 43

### POSIX_ALNUM

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val POSIX_ALNUM: Int
```

Binary property alnum (a C/POSIX character class). Implemented according to the UTS #18 Annex C Standard Recommendation. See the UCharacter class documentation. 

 Value: 44

### POSIX_BLANK

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val POSIX_BLANK: Int
```

Binary property blank (a C/POSIX character class). Implemented according to the UTS #18 Annex C Standard Recommendation. See the UCharacter class documentation. 

 Value: 45

### POSIX_GRAPH

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val POSIX_GRAPH: Int
```

Binary property graph (a C/POSIX character class). Implemented according to the UTS #18 Annex C Standard Recommendation. See the UCharacter class documentation. 

 Value: 46

### POSIX_PRINT

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val POSIX_PRINT: Int
```

Binary property print (a C/POSIX character class). Implemented according to the UTS #18 Annex C Standard Recommendation. See the UCharacter class documentation. 

 Value: 47

### POSIX_XDIGIT

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val POSIX_XDIGIT: Int
```

Binary property xdigit (a C/POSIX character class). Implemented according to the UTS #18 Annex C Standard Recommendation. See the UCharacter class documentation. 

 Value: 48

### PREPENDED_CONCATENATION_MARK

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PREPENDED_CONCATENATION_MARK: Int
```

Binary property Prepended_Concatenation_Mark. 

 Value: 63

### QUOTATION_MARK

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val QUOTATION_MARK: Int
```

Binary property Quotation_Mark. 

 Value: 25

### RADICAL

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RADICAL: Int
```

Binary property Radical (new).

For programmatic determination of Ideographic Description Sequences. 

 Value: 26

### REGIONAL_INDICATOR

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val REGIONAL_INDICATOR: Int
```

Binary property Regional_Indicator. 

 Value: 62

### RGI_EMOJI

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RGI_EMOJI: Int
```

Binary property of strings RGI_Emoji. See https://www.unicode.org/reports/tr51/#Emoji_Sets 

 Value: 71

### RGI_EMOJI_FLAG_SEQUENCE

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RGI_EMOJI_FLAG_SEQUENCE: Int
```

Binary property of strings RGI_Emoji_Flag_Sequence. See https://www.unicode.org/reports/tr51/#Emoji_Sets 

 Value: 68

### RGI_EMOJI_MODIFIER_SEQUENCE

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RGI_EMOJI_MODIFIER_SEQUENCE: Int
```

Binary property of strings RGI_Emoji_Modifier_Sequence. See https://www.unicode.org/reports/tr51/#Emoji_Sets 

 Value: 67

### RGI_EMOJI_TAG_SEQUENCE

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RGI_EMOJI_TAG_SEQUENCE: Int
```

Binary property of strings RGI_Emoji_Tag_Sequence. See https://www.unicode.org/reports/tr51/#Emoji_Sets 

 Value: 69

### RGI_EMOJI_ZWJ_SEQUENCE

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RGI_EMOJI_ZWJ_SEQUENCE: Int
```

Binary property of strings RGI_Emoji_ZWJ_Sequence. See https://www.unicode.org/reports/tr51/#Emoji_Sets 

 Value: 70

### SCRIPT

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SCRIPT: Int
```

Enumerated property Script. Same as UScript.getScript(int), returns UScript values. 

 Value: 4106

### SCRIPT_EXTENSIONS

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SCRIPT_EXTENSIONS: Int
```

Miscellaneous property Script_Extensions (new in Unicode 6.0). Some characters are commonly used in multiple scripts. For more information, see UAX #24: http://www.unicode.org/reports/tr24/. Corresponds to UScript.hasScript and UScript.getScriptExtensions. 

 Value: 28672

### SEGMENT_STARTER

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SEGMENT_STARTER: Int
```

Binary Property Segment_Starter. ICU-specific property for characters that are starters in terms of Unicode normalization and combining character sequences. They have ccc=0 and do not occur in non-initial position of the canonical decomposition of any character (like " in NFD(a-umlaut) and a Jamo T in an NFD(Hangul LVT)). ICU uses this property for segmenting a string for generating a set of canonically equivalent strings, e.g. for canonical closure while processing collation tailoring rules. 

 Value: 41

### SENTENCE_BREAK

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SENTENCE_BREAK: Int
```

Enumerated property Sentence_Break (new in Unicode 4.1). Used in UAX #29: Text Boundaries (http://www.unicode.org/reports/tr29/) Returns UCharacter.SentenceBreak values. 

 Value: 4115

### SIMPLE_CASE_FOLDING

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SIMPLE_CASE_FOLDING: Int
```

String property Simple_Case_Folding. Corresponds to UCharacter.foldCase(int, boolean). 

 Value: 16390

### SIMPLE_LOWERCASE_MAPPING

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SIMPLE_LOWERCASE_MAPPING: Int
```

String property Simple_Lowercase_Mapping. Corresponds to UCharacter.toLowerCase(int). 

 Value: 16391

### SIMPLE_TITLECASE_MAPPING

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SIMPLE_TITLECASE_MAPPING: Int
```

String property Simple_Titlecase_Mapping. Corresponds to UCharacter.toTitleCase(int). 

 Value: 16392

### SIMPLE_UPPERCASE_MAPPING

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SIMPLE_UPPERCASE_MAPPING: Int
```

String property Simple_Uppercase_Mapping. Corresponds to UCharacter.toUpperCase(int). 

 Value: 16393

### SOFT_DOTTED

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SOFT_DOTTED: Int
```

Binary property Soft_Dotted (new).

Characters with a "soft dot", like i or j.

An accent placed on these characters causes the dot to disappear. 

 Value: 27

### STRING_START

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STRING_START: Int
```

First constant for string Unicode properties. 

 Value: 16384

### S_TERM

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val S_TERM: Int
```

Binary property STerm (new in Unicode 4.0.1). Sentence Terminal. Used in UAX #29: Text Boundaries (http://www.unicode.org/reports/tr29/) 

 Value: 35

### TERMINAL_PUNCTUATION

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TERMINAL_PUNCTUATION: Int
```

Binary property Terminal_Punctuation.

Punctuation characters that generally mark the end of textual units. 

 Value: 28

### TITLECASE_MAPPING

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TITLECASE_MAPPING: Int
```

String property Titlecase_Mapping. Corresponds to UCharacter.toTitleCase(String). 

 Value: 16394

### TRAIL_CANONICAL_COMBINING_CLASS

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TRAIL_CANONICAL_COMBINING_CLASS: Int
```

Enumerated property Trail_Canonical_Combining_Class. ICU-specific property for the ccc of the last code point of the decomposition, or lccc(c)=ccc(NFD(c)\[last\]). Useful for checking for canonically ordered text; see Normalizer.FCD and http://www.unicode.org/notes/tn5/#FCD . Returns 8-bit numeric values like CANONICAL_COMBINING_CLASS. 

 Value: 4113

### UNIFIED_IDEOGRAPH

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val UNIFIED_IDEOGRAPH: Int
```

Binary property Unified_Ideograph (new).

For programmatic determination of Ideographic Description Sequences. 

 Value: 29

### UPPERCASE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val UPPERCASE: Int
```

Binary property Uppercase.

Same as UCharacter.isUUppercase(), different from UCharacter.isUpperCase().

Lu+Other_Uppercase 

 Value: 30

### UPPERCASE_MAPPING

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val UPPERCASE_MAPPING: Int
```

String property Uppercase_Mapping. Corresponds to UCharacter.toUpperCase(String). 

 Value: 16396

### VARIATION_SELECTOR

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val VARIATION_SELECTOR: Int
```

Binary property Variation_Selector (new in Unicode 4.0.1). Indicates all those characters that qualify as Variation Selectors. For details on the behavior of these characters, see StandardizedVariants.html and 15.6 Variation Selectors. 

 Value: 36

### VERTICAL_ORIENTATION

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val VERTICAL_ORIENTATION: Int
```

Enumerated property Vertical_Orientation. Used for UAX #50 Unicode Vertical Text Layout (https://www.unicode.org/reports/tr50/). New as a UCD property in Unicode 10.0. 

 Value: 4120

### WHITE_SPACE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val WHITE_SPACE: Int
```

Binary property White_Space.

Same as UCharacter.isUWhiteSpace(), different from UCharacter.isSpace() and UCharacter.isWhitespace(). Space characters+TAB+CR+LF-ZWSP-ZWNBSP 

 Value: 31

### WORD_BREAK

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val WORD_BREAK: Int
```

Enumerated property Word_Break (new in Unicode 4.1). Used in UAX #29: Text Boundaries (http://www.unicode.org/reports/tr29/) Returns UCharacter.WordBreak values. 

 Value: 4116

### XID_CONTINUE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val XID_CONTINUE: Int
```

Binary property XID_Continue.

ID_Continue modified to allow closure under normalization forms NFKC and NFKD. 

 Value: 32

### XID_START

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val XID_START: Int
```

Binary property XID_Start.

ID_Start modified to allow closure under normalization forms NFKC and NFKD. 

 Value: 33
